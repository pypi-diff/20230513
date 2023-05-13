# Comparing `tmp/icalstatus-0.0.4-py3-none-any.whl.zip` & `tmp/icalstatus-0.0.5-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,11 @@
-Zip file size: 5556 bytes, number of entries: 7
--rwxr-xr-x  2.0 unx     1033 b- defN 80-Jan-01 00:00 icalstatus/parse.py
--rw-r--r--  2.0 unx     4868 b- defN 80-Jan-01 00:00 icalstatus/status.py
--rw-r--r--  2.0 unx      770 b- defN 80-Jan-01 00:00 icalstatus-0.0.4.dist-info/LICENSE
--rw-r--r--  2.0 unx     3261 b- defN 80-Jan-01 00:00 icalstatus-0.0.4.dist-info/METADATA
--rw-r--r--  2.0 unx       88 b- defN 80-Jan-01 00:00 icalstatus-0.0.4.dist-info/WHEEL
--rw-r--r--  2.0 unx      123 b- defN 80-Jan-01 00:00 icalstatus-0.0.4.dist-info/entry_points.txt
-?rw-r--r--  2.0 unx      557 b- defN 16-Jan-01 00:00 icalstatus-0.0.4.dist-info/RECORD
-7 files, 10700 bytes uncompressed, 4570 bytes compressed:  57.3%
+Zip file size: 6433 bytes, number of entries: 9
+-rw-r--r--  2.0 unx        0 b- defN 80-Jan-01 00:00 icalstatus/__init__.py
+-rw-r--r--  2.0 unx     1219 b- defN 80-Jan-01 00:00 icalstatus/date.py
+-rwxr-xr-x  2.0 unx     1036 b- defN 80-Jan-01 00:00 icalstatus/parse.py
+-rw-r--r--  2.0 unx     4677 b- defN 80-Jan-01 00:00 icalstatus/status.py
+-rw-r--r--  2.0 unx      770 b- defN 80-Jan-01 00:00 icalstatus-0.0.5.dist-info/LICENSE
+-rw-r--r--  2.0 unx     3318 b- defN 80-Jan-01 00:00 icalstatus-0.0.5.dist-info/METADATA
+-rw-r--r--  2.0 unx       88 b- defN 80-Jan-01 00:00 icalstatus-0.0.5.dist-info/WHEEL
+-rw-r--r--  2.0 unx      123 b- defN 80-Jan-01 00:00 icalstatus-0.0.5.dist-info/entry_points.txt
+?rw-r--r--  2.0 unx      708 b- defN 16-Jan-01 00:00 icalstatus-0.0.5.dist-info/RECORD
+9 files, 11939 bytes uncompressed, 5215 bytes compressed:  56.3%
```

## zipnote {}

```diff
@@ -1,22 +1,28 @@
+Filename: icalstatus/__init__.py
+Comment: 
+
+Filename: icalstatus/date.py
+Comment: 
+
 Filename: icalstatus/parse.py
 Comment: 
 
 Filename: icalstatus/status.py
 Comment: 
 
-Filename: icalstatus-0.0.4.dist-info/LICENSE
+Filename: icalstatus-0.0.5.dist-info/LICENSE
 Comment: 
 
-Filename: icalstatus-0.0.4.dist-info/METADATA
+Filename: icalstatus-0.0.5.dist-info/METADATA
 Comment: 
 
-Filename: icalstatus-0.0.4.dist-info/WHEEL
+Filename: icalstatus-0.0.5.dist-info/WHEEL
 Comment: 
 
-Filename: icalstatus-0.0.4.dist-info/entry_points.txt
+Filename: icalstatus-0.0.5.dist-info/entry_points.txt
 Comment: 
 
-Filename: icalstatus-0.0.4.dist-info/RECORD
+Filename: icalstatus-0.0.5.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## icalstatus/parse.py

```diff
@@ -1,46 +1,48 @@
 #!/usr/bin/env python3
 
 
 import caep
-import ics
+import icalendar  # type: ignore
+import pytz
 from pydantic import BaseModel, Field
 
+from icalstatus.date import get_event_dt
 
-class Config(BaseModel):
 
-    timezone: str = Field("Europe/Oslo", description="Timezone")
+class Config(BaseModel):
+    timezone: str = Field("CET", description="Timezone")
     file: str = Field(description="File to parse")
 
 
 def parse(config: Config, data: str) -> None:
-    for e in ics.Calendar(data).events:
-        e.begin = e.begin.replace(tzinfo=config.timezone)
-        e.end = e.end.replace(tzinfo=config.timezone)
-        name = e.name if e.name else "Unknown"
-        organizer = e.organizer if e.organizer else "Unknown"
-        location = e.location if e.location else "Unknown"
-        description = e.description if e.description else "No description"
+    tzinfo = pytz.timezone(config.timezone)
+
+    cal = icalendar.Calendar.from_ical(data)
+    for e in cal.walk():
+        if not e.name == "VEVENT":
+            continue
+        begin = get_event_dt(e, tzinfo)
+        end = get_event_dt(e, tzinfo, "DTEND")
         print(
             f"""
-{name}
+{e.get('SUMMARY', 'Unknown')}
 
-Organizer: {organizer}
-Location: {location}
+Organizer: {e.get('ORGANIZER', 'Unknown')}
+Location: {e.get('LOCATION', 'Unknown')}
 
-Start: {e.begin}
-End:   {e.end}
+Start: {begin}
+End:   {end}
 
-{description}"""
+{e.get('DESCRIPTION', 'Unknown')}"""
         )
 
 
 def main() -> None:
-
     config: Config = caep.load(Config, "ICAL parse", "icalstatus", "config", "parse")
 
-    data = open(config.file, "r").read()
+    data = open(config.file).read()
     parse(config, data)
 
 
 if __name__ == "__main__":
     main()
```

## icalstatus/status.py

```diff
@@ -1,37 +1,41 @@
 #!/usr/bin/env python3
 """Statusbar ics calendar"""
 
 import html
 import json
 import sys
 from dataclasses import dataclass
+from datetime import datetime, timedelta
 from typing import Optional
 
-import arrow
 import caep
-import ics
+import icalendar  # type: ignore
+import pytz
+import recurring_ical_events  # type: ignore
 import requests
-from dateutil import rrule  # type: ignore
+
+# from dateutil import rrule
 from pydantic import BaseModel, Field
 from urllib3 import disable_warnings
 from urllib3.exceptions import InsecureRequestWarning
 
+from icalstatus.date import get_event_dt, humanize
+
 disable_warnings(InsecureRequestWarning)
 
 
 @dataclass
 class Event:
     name: str
     begin: str
     alert: bool
 
 
 class Config(BaseModel):
-
     calendar_url: str = Field(description="URI for ICS Calendar")
     timezone: str = Field("CET", description="Timezone (default=CET)")
     no_verify: bool = Field(False, description="Ignore SSL verification errors")
     proxy: Optional[str] = Field(description="Proxy for ICS url")
 
     all: bool = Field(False, description="Include events that are not today")
 
@@ -54,108 +58,99 @@
     proxies = {"http": proxy_string, "https": proxy_string} if proxy_string else None
 
     req = requests.get(url, timeout=10, verify=(not no_verify), proxies=proxies)
 
     return req.text
 
 
-def is_recurring(event: ics.Event) -> bool:
-    """Check if it is a recurring event"""
-
-    return any(filter(lambda x: x.name == "RRULE", event.extra))  # type: ignore
-
-
-def get_rrule(event: ics.Event) -> tuple[str, bool]:
-    """Extract the rrule text from an event"""
-
-    for extra in event.extra:
-        if extra.name == "RRULE":
-            return extra.value, True
-
-    return "", False
-
-
-def get_next_datetime(event: ics.Event, now: arrow) -> arrow.Arrow:
-    """Check if it is a recurring event, and if so get next event time"""
-
-    if is_recurring(event):
-
-        ruletext, ok = get_rrule(event)
-        if not ok:
-            return event.begin
-        rule = rrule.rrulestr(ruletext, dtstart=event.begin.datetime)
-        nextrule = rule.after(now.datetime)
-        if not nextrule:
-            return event.begin
-        return arrow.get(nextrule)
+def get_next_datetime(
+    recurring_event: icalendar.Event, now: datetime, tzinfo: pytz.BaseTzInfo
+) -> Optional[datetime]:
+    begin = None
+    for event in recurring_ical_events.of(recurring_event).between(
+        now - timedelta(minutes=5), now + timedelta(days=7)
+    ):
+        begin = get_event_dt(event, tzinfo)
 
-    return event.begin
+    return begin
 
 
-def ics_next_event(ics_data: str, now: arrow, timezone: str) -> Optional[ics.Event]:
+def ics_next_event(
+    ics_data: str, now: datetime, tzinfo: pytz.BaseTzInfo
+) -> Optional[icalendar.Event]:
     curr = None
     diff = None
 
-    cal = ics.Calendar(ics_data)
+    cal = icalendar.Calendar.from_ical(ics_data)
 
     event = None
-    for event in cal.events:
-        # Set correct timezone
-        event.begin = event.begin.replace(tzinfo=timezone)
-        if event.begin.datetime < now:
-            if is_recurring(event):
-                nextrule = get_next_datetime(event, now)
+    for event in cal.walk():
+        if not event.name == "VEVENT":
+            continue
+
+        begin = get_event_dt(event, tzinfo)
+
+        if begin < now:
+            if event.get("RRULE"):
+                nextrule = get_next_datetime(event, now, tzinfo)
+                if not nextrule:
+                    continue
+
                 if nextrule < now:
                     continue
                 thisdiff = nextrule - now
                 if not curr or thisdiff < diff:
                     diff = thisdiff
                     curr = event
             continue
-        thisdiff = event.begin.datetime - now
-        if not curr or thisdiff < diff:
+
+        thisdiff = begin - now
+
+        if not curr or (diff and (thisdiff < diff)):
             diff = thisdiff
             curr = event
 
     return curr
 
 
 def upcoming_event() -> Optional[Event]:
     """Get the next event closest in time"""
 
     config: Config = caep.load(Config, "ICAL Status", "icalstatus", "config", "status")
 
-    now = arrow.now().replace(tzinfo=config.timezone)
+    # now = arrow.now().replace(tzinfo=config.timezone)
+    tzinfo = pytz.timezone(config.timezone)
+    now = datetime.now().replace(tzinfo=tzinfo)
     next = ics_next_event(
         get_data(config.calendar_url, config.no_verify, config.proxy),
         now,
-        config.timezone,
+        tzinfo,
     )
 
     if not next:
         return None
 
-    begin = get_next_datetime(next, now).replace(tzinfo=config.timezone)
+    begin = get_event_dt(next, tzinfo)
 
     if (now.date() != begin.date()) and not config.all:
         return None
 
     # If meeteing is soon to begin or we have chosen to include
     # meetings for the next days+, show time in "human format", e.g. `in 5 minutes`
-    if (now.shift(seconds=config.humanize_after_sec) > begin) or (
+    if (now + timedelta(seconds=config.humanize_after_sec) > begin) or (
         now.date() != begin.date()
     ):
-        begin_str = begin.humanize()
+        begin_str = humanize((now - begin).seconds)
     else:
-        begin_str = f"@{begin.format('HH:mm')}"
+        begin_str = f"@{begin.strftime('%H:%M')}"
 
     return Event(
-        name=next.name.strip(),
+        name=next.get("SUMMARY", "Unknown").strip(),
         begin=begin_str,
-        alert=now.shift(seconds=config.alert_sec_before) > begin,
+        alert=now - timedelta(seconds=config.alert_sec_before) > begin,
     )
 
 
 def status() -> None:
     """main"""
 
     event = upcoming_event()
```

## Comparing `icalstatus-0.0.4.dist-info/LICENSE` & `icalstatus-0.0.5.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `icalstatus-0.0.4.dist-info/METADATA` & `icalstatus-0.0.5.dist-info/METADATA`

 * *Files 5% similar despite different names*

```diff
@@ -1,27 +1,28 @@
 Metadata-Version: 2.1
 Name: icalstatus
-Version: 0.0.4
+Version: 0.0.5
 Summary: icalstatus
 Home-page: https://github.com/frbor/icalstatus
 License: ISC
 Author: Fredrik Borg
 Author-email: fredrikb.borg@gmail.com
 Requires-Python: >=3.9.0,<4.0.0
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved
 Classifier: License :: OSI Approved :: ISC License (ISCL)
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Utilities
-Requires-Dist: caep (>=0.1.1,<0.2.0)
-Requires-Dist: ics (>=0.7.0,<0.8.0)
+Requires-Dist: caep (>=0.1.8,<0.2.0)
+Requires-Dist: icalendar (>=5.0.0,<6.0.0)
 Requires-Dist: pytz
+Requires-Dist: recurring-ical-events (>=2.0.0,<3.0.0)
 Requires-Dist: requests (>=2.28.1,<3.0.0)
 Description-Content-Type: text/markdown
 
 # ICAL Status - Status bar for ICS Calenders
 
 # Installation
 
@@ -34,15 +35,15 @@
 To run, one of:
 
 - `icalstatus`
 - `icalwaybar`
 
 ## Configuration
 
-For the status you must specify you calendar URL either on the commandline or in the 
+For the status you must specify you calendar URL either on the commandline or in the
 configuration file `~/.config/icalstatus/config`:
 
 E.g, for OWA:
 
 ```
 [DEFAULT]
 calendar-url=https://(HOST)/owa/calendar/(...)/calendar.ics
@@ -60,18 +61,18 @@
   --calendar-url CALENDAR_URL
                         URI for ICS Calendar
   --timezone TIMEZONE   Timezone (default=CET)
   --no-verify           Ignore SSL verification errors
   --proxy PROXY         Proxy for ICS url
   --all                 Include events that are not today
   --humanize-after-sec HUMANIZE_AFTER
-                        Humanize meeting date if less than this many seconds 
+                        Humanize meeting date if less than this many seconds
                         until meeting
   --alert-sec-before ALERT_SEC_BEFORE
-                        Alert meeting at specified seconds before start. 
+                        Alert meeting at specified seconds before start.
                         This will switch class for output on waybar.
 ```
 
 Options:
 
 ### `all`
```

## Comparing `icalstatus-0.0.4.dist-info/RECORD` & `icalstatus-0.0.5.dist-info/RECORD`

 * *Files 27% similar despite different names*

```diff
@@ -1,7 +1,9 @@
-icalstatus/parse.py,sha256=DEe8AswAfH3xjt--ZyD6ATkfKw56D1mlhAUwJheMhp4,1033
-icalstatus/status.py,sha256=9NhU9MOQFA4qBCAQFjc_Qp_lTiBgi_GzH9ViIqazPlA,4868
-icalstatus-0.0.4.dist-info/LICENSE,sha256=4DFZPzsHvBwvMFiW1m_3QilusGT6jMBlP6zHFNhQ7A8,770
-icalstatus-0.0.4.dist-info/METADATA,sha256=PIsuTK6AJ1KE-yHD3jB9kEeuMYWPIQRzXIS8iNcOZXs,3261
-icalstatus-0.0.4.dist-info/WHEEL,sha256=vVCvjcmxuUltf8cYhJ0sJMRDLr1XsPuxEId8YDzbyCY,88
-icalstatus-0.0.4.dist-info/entry_points.txt,sha256=V4B_F6lqqyg1AL-OIRmQ9hj3lJO5mkI_6xUCvrtjTJY,123
-icalstatus-0.0.4.dist-info/RECORD,,
+icalstatus/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
+icalstatus/date.py,sha256=zSDxAHLnHvKV-39SwBrp0EYDIVVde9iacYrQIVxR7TE,1219
+icalstatus/parse.py,sha256=jXnFHzFDAYnjTCD0Rfj9yilcQ6Vozd9h4VDq3jpEerA,1036
+icalstatus/status.py,sha256=UdepC6Ct4mn_RIH7-3TmZEudKKMYbBuCNToYqdmUybo,4677
+icalstatus-0.0.5.dist-info/LICENSE,sha256=4DFZPzsHvBwvMFiW1m_3QilusGT6jMBlP6zHFNhQ7A8,770
+icalstatus-0.0.5.dist-info/METADATA,sha256=kx3z7R_0lFUHDJmVBYhTPD-CSFlYla3kyYAza8NJuhs,3318
+icalstatus-0.0.5.dist-info/WHEEL,sha256=7Z8_27uaHI_UZAc4Uox4PpBhQ9Y5_modZXWMxtUi4NU,88
+icalstatus-0.0.5.dist-info/entry_points.txt,sha256=V4B_F6lqqyg1AL-OIRmQ9hj3lJO5mkI_6xUCvrtjTJY,123
+icalstatus-0.0.5.dist-info/RECORD,,
```

