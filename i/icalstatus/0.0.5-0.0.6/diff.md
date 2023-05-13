# Comparing `tmp/icalstatus-0.0.5-py3-none-any.whl.zip` & `tmp/icalstatus-0.0.6-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,11 +1,11 @@
-Zip file size: 6433 bytes, number of entries: 9
+Zip file size: 6439 bytes, number of entries: 9
 -rw-r--r--  2.0 unx        0 b- defN 80-Jan-01 00:00 icalstatus/__init__.py
--rw-r--r--  2.0 unx     1219 b- defN 80-Jan-01 00:00 icalstatus/date.py
+-rw-r--r--  2.0 unx     1234 b- defN 80-Jan-01 00:00 icalstatus/date.py
 -rwxr-xr-x  2.0 unx     1036 b- defN 80-Jan-01 00:00 icalstatus/parse.py
--rw-r--r--  2.0 unx     4677 b- defN 80-Jan-01 00:00 icalstatus/status.py
--rw-r--r--  2.0 unx      770 b- defN 80-Jan-01 00:00 icalstatus-0.0.5.dist-info/LICENSE
--rw-r--r--  2.0 unx     3318 b- defN 80-Jan-01 00:00 icalstatus-0.0.5.dist-info/METADATA
--rw-r--r--  2.0 unx       88 b- defN 80-Jan-01 00:00 icalstatus-0.0.5.dist-info/WHEEL
--rw-r--r--  2.0 unx      123 b- defN 80-Jan-01 00:00 icalstatus-0.0.5.dist-info/entry_points.txt
-?rw-r--r--  2.0 unx      708 b- defN 16-Jan-01 00:00 icalstatus-0.0.5.dist-info/RECORD
-9 files, 11939 bytes uncompressed, 5215 bytes compressed:  56.3%
+-rw-r--r--  2.0 unx     4691 b- defN 80-Jan-01 00:00 icalstatus/status.py
+-rw-r--r--  2.0 unx      770 b- defN 80-Jan-01 00:00 icalstatus-0.0.6.dist-info/LICENSE
+-rw-r--r--  2.0 unx     3318 b- defN 80-Jan-01 00:00 icalstatus-0.0.6.dist-info/METADATA
+-rw-r--r--  2.0 unx       88 b- defN 80-Jan-01 00:00 icalstatus-0.0.6.dist-info/WHEEL
+-rw-r--r--  2.0 unx      123 b- defN 80-Jan-01 00:00 icalstatus-0.0.6.dist-info/entry_points.txt
+?rw-r--r--  2.0 unx      708 b- defN 16-Jan-01 00:00 icalstatus-0.0.6.dist-info/RECORD
+9 files, 11968 bytes uncompressed, 5221 bytes compressed:  56.4%
```

## zipnote {}

```diff
@@ -6,23 +6,23 @@
 
 Filename: icalstatus/parse.py
 Comment: 
 
 Filename: icalstatus/status.py
 Comment: 
 
-Filename: icalstatus-0.0.5.dist-info/LICENSE
+Filename: icalstatus-0.0.6.dist-info/LICENSE
 Comment: 
 
-Filename: icalstatus-0.0.5.dist-info/METADATA
+Filename: icalstatus-0.0.6.dist-info/METADATA
 Comment: 
 
-Filename: icalstatus-0.0.5.dist-info/WHEEL
+Filename: icalstatus-0.0.6.dist-info/WHEEL
 Comment: 
 
-Filename: icalstatus-0.0.5.dist-info/entry_points.txt
+Filename: icalstatus-0.0.6.dist-info/entry_points.txt
 Comment: 
 
-Filename: icalstatus-0.0.5.dist-info/RECORD
+Filename: icalstatus-0.0.6.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## icalstatus/date.py

```diff
@@ -24,22 +24,22 @@
 
     future = True if seconds > 0 else False
 
     seconds = abs(seconds)
 
     if seconds >= 3600:
         hours = seconds // 3600
-        human_delta = f"{hours} hour{single(hours)}"
+        human_delta = f"{int(hours)} hour{single(hours)}"
 
     elif seconds >= 60:
         minutes = seconds // 60
-        human_delta = f"{minutes} minute{single(minutes)}"
+        human_delta = f"{int(minutes)} minute{single(minutes)}"
 
     else:
-        human_delta = f"{seconds} second{single(seconds)}"
+        human_delta = f"{int(seconds)} second{single(seconds)}"
 
     return f"in {human_delta}" if future else f"{human_delta} ago"
 
 
 def get_event_dt(
     event: icalendar.Event, tzinfo: pytz.BaseTzInfo, obj: str = "DTSTART"
 ) -> datetime:
```

## icalstatus/status.py

```diff
@@ -135,15 +135,15 @@
         return None
 
     # If meeteing is soon to begin or we have chosen to include
     # meetings for the next days+, show time in "human format", e.g. `in 5 minutes`
     if (now + timedelta(seconds=config.humanize_after_sec) > begin) or (
         now.date() != begin.date()
     ):
-        begin_str = humanize((now - begin).seconds)
+        begin_str = humanize(begin.timestamp() - now.timestamp())
     else:
         begin_str = f"@{begin.strftime('%H:%M')}"
 
     return Event(
         name=next.get("SUMMARY", "Unknown").strip(),
         begin=begin_str,
         alert=now - timedelta(seconds=config.alert_sec_before) > begin,
```

## Comparing `icalstatus-0.0.5.dist-info/LICENSE` & `icalstatus-0.0.6.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `icalstatus-0.0.5.dist-info/METADATA` & `icalstatus-0.0.6.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: icalstatus
-Version: 0.0.5
+Version: 0.0.6
 Summary: icalstatus
 Home-page: https://github.com/frbor/icalstatus
 License: ISC
 Author: Fredrik Borg
 Author-email: fredrikb.borg@gmail.com
 Requires-Python: >=3.9.0,<4.0.0
 Classifier: Development Status :: 4 - Beta
```

