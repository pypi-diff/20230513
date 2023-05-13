# Comparing `tmp/mutwo.timeline-0.1.0.tar.gz` & `tmp/mutwo.timeline-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mutwo.timeline-0.1.0.tar", last modified: Sun Nov  6 22:24:15 2022, max compression
+gzip compressed data, was "mutwo.timeline-0.4.0.tar", last modified: Sat May 13 11:17:37 2023, max compression
```

## Comparing `mutwo.timeline-0.1.0.tar` & `mutwo.timeline-0.4.0.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-11-06 22:24:15.133260 mutwo.timeline-0.1.0/
--rw-r--r--   0 circleci  (1001) circleci  (1002)    35149 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/LICENSE
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1733 2022-11-06 22:24:15.133260 mutwo.timeline-0.1.0/PKG-INFO
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1275 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/README.md
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-11-06 22:24:15.129260 mutwo.timeline-0.1.0/mutwo/
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-11-06 22:24:15.133260 mutwo.timeline-0.1.0/mutwo/timeline_converters/
--rw-r--r--   0 circleci  (1001) circleci  (1002)     3666 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/mutwo/timeline_converters/__init__.py
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-11-06 22:24:15.133260 mutwo.timeline-0.1.0/mutwo/timeline_events/
--rw-r--r--   0 circleci  (1001) circleci  (1002)    15581 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/mutwo/timeline_events/__init__.py
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-11-06 22:24:15.133260 mutwo.timeline-0.1.0/mutwo/timeline_utilities/
--rw-r--r--   0 circleci  (1001) circleci  (1002)       26 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/mutwo/timeline_utilities/__init__.py
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1060 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/mutwo/timeline_utilities/exceptions.py
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-11-06 22:24:15.133260 mutwo.timeline-0.1.0/mutwo/timeline_version/
--rw-r--r--   0 circleci  (1001) circleci  (1002)      146 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/mutwo/timeline_version/__init__.py
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-11-06 22:24:15.133260 mutwo.timeline-0.1.0/mutwo.timeline.egg-info/
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1733 2022-11-06 22:24:15.000000 mutwo.timeline-0.1.0/mutwo.timeline.egg-info/PKG-INFO
--rw-r--r--   0 circleci  (1001) circleci  (1002)      413 2022-11-06 22:24:15.000000 mutwo.timeline-0.1.0/mutwo.timeline.egg-info/SOURCES.txt
--rw-r--r--   0 circleci  (1001) circleci  (1002)        1 2022-11-06 22:24:15.000000 mutwo.timeline-0.1.0/mutwo.timeline.egg-info/dependency_links.txt
--rw-r--r--   0 circleci  (1001) circleci  (1002)       96 2022-11-06 22:24:15.000000 mutwo.timeline-0.1.0/mutwo.timeline.egg-info/requires.txt
--rw-r--r--   0 circleci  (1001) circleci  (1002)        6 2022-11-06 22:24:15.000000 mutwo.timeline-0.1.0/mutwo.timeline.egg-info/top_level.txt
--rw-r--r--   0 circleci  (1001) circleci  (1002)      200 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/pyproject.toml
--rw-r--r--   0 circleci  (1001) circleci  (1002)       38 2022-11-06 22:24:15.133260 mutwo.timeline-0.1.0/setup.cfg
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1212 2022-11-06 22:24:04.000000 mutwo.timeline-0.1.0/setup.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-05-13 11:17:37.699196 mutwo.timeline-0.4.0/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)    35149 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/LICENSE
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1737 2023-05-13 11:17:37.699196 mutwo.timeline-0.4.0/PKG-INFO
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1279 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/README.md
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-05-13 11:17:37.695196 mutwo.timeline-0.4.0/mutwo/
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-05-13 11:17:37.695196 mutwo.timeline-0.4.0/mutwo/timeline_converters/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)    12070 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/mutwo/timeline_converters/__init__.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-05-13 11:17:37.695196 mutwo.timeline-0.4.0/mutwo/timeline_interfaces/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)    24269 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/mutwo/timeline_interfaces/__init__.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-05-13 11:17:37.695196 mutwo.timeline-0.4.0/mutwo/timeline_utilities/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)       26 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/mutwo/timeline_utilities/__init__.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1975 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/mutwo/timeline_utilities/exceptions.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-05-13 11:17:37.699196 mutwo.timeline-0.4.0/mutwo/timeline_version/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      146 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/mutwo/timeline_version/__init__.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-05-13 11:17:37.695196 mutwo.timeline-0.4.0/mutwo.timeline.egg-info/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1737 2023-05-13 11:17:37.000000 mutwo.timeline-0.4.0/mutwo.timeline.egg-info/PKG-INFO
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      417 2023-05-13 11:17:37.000000 mutwo.timeline-0.4.0/mutwo.timeline.egg-info/SOURCES.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)        1 2023-05-13 11:17:37.000000 mutwo.timeline-0.4.0/mutwo.timeline.egg-info/dependency_links.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)       96 2023-05-13 11:17:37.000000 mutwo.timeline-0.4.0/mutwo.timeline.egg-info/requires.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)        6 2023-05-13 11:17:37.000000 mutwo.timeline-0.4.0/mutwo.timeline.egg-info/top_level.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      200 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/pyproject.toml
+-rw-r--r--   0 circleci  (1001) circleci  (1002)       38 2023-05-13 11:17:37.699196 mutwo.timeline-0.4.0/setup.cfg
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1212 2023-05-13 11:17:27.000000 mutwo.timeline-0.4.0/setup.py
```

### Comparing `mutwo.timeline-0.1.0/LICENSE` & `mutwo.timeline-0.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `mutwo.timeline-0.1.0/PKG-INFO` & `mutwo.timeline-0.4.0/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mutwo.timeline
-Version: 0.1.0
+Version: 0.4.0
 Summary: timeline extension for event based framework for generative art
 Home-page: https://github.com/mutwo-org/mutwo.timeline
 Author: Levin Eric Zimmermann
 Author-email: levin.eric.zimmermann@posteo.eu
 License: GPL
 Project-URL: Documentation, https://mutwo.readthedocs.io/en/latest/
 Requires-Python: >=3.10, <4
@@ -27,15 +27,15 @@
 and end time of any event dependent on all events which happens before the
 given event. This extension implements the possibility to model events with
 independent start and end times in `mutwo`.
 
 This extension implements:
 
 - `mutwo.timeline_converters`
-- `mutwo.timeline_events`
+- `mutwo.timeline_interfaces`
 - `mutwo.timeline_utilities`
 
 ### Installation
 
 mutwo.timeline is available on [pypi](https://pypi.org/project/mutwo.timeline/) and can be installed via pip:
 
 ```sh
```

### Comparing `mutwo.timeline-0.1.0/README.md` & `mutwo.timeline-0.4.0/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 and end time of any event dependent on all events which happens before the
 given event. This extension implements the possibility to model events with
 independent start and end times in `mutwo`.
 
 This extension implements:
 
 - `mutwo.timeline_converters`
-- `mutwo.timeline_events`
+- `mutwo.timeline_interfaces`
 - `mutwo.timeline_utilities`
 
 ### Installation
 
 mutwo.timeline is available on [pypi](https://pypi.org/project/mutwo.timeline/) and can be installed via pip:
 
 ```sh
```

### Comparing `mutwo.timeline-0.1.0/mutwo/timeline_events/__init__.py` & `mutwo.timeline-0.4.0/mutwo/timeline_converters/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,400 +1,297 @@
-"""Place events with absolute start and end times on a time line.
+"""Convert :class:`mutwo.timeline_interfaces.TimeLine` to objects useable by other parts of `mutwo`."""
 
-`Mutwo` events usually follow an approach of relative placement in time.
-This means each event has a duration, and if there is a sequence of events
-the second event will start after the first event finishes. So the start
-and end time of any event dependent on all events which happens before the
-given event. This package implements the possibility to model events with
-independent start and end times in `mutwo`.
-"""
-
-from __future__ import annotations
-
-import bisect
-import copy
-import statistics
 import typing
 
+import numpy as np
 import ranges
 
+from mutwo import core_converters
 from mutwo import core_events
 from mutwo import core_parameters
 from mutwo import core_utilities
-from mutwo import timeline_utilities
+from mutwo import timeline_interfaces
 
-UnspecificTime: typing.TypeAlias = "core_parameters.abc.Duration | typing.Any"
-UnspecificTimeOrTimeRange: typing.TypeAlias = "UnspecificTime | ranges.Range"
-TimeOrTimeRange: typing.TypeAlias = "core_parameters.abc.Duration | ranges.Range"
-
-__all__ = ("EventPlacement", "TimeLine")
-
-
-class EventPlacement(object):
-    """Place any event at specific start and end times.
-
-    :param event: The event to be placed on a :class:`TimeLine`. This needs to
-        be an event with a `tag` property. The tag is necessary to concatenate
-        two events on a `TimeLine` which belong to the same object (e.g.
-        same instrument or same player).
-    :type event: core_events.TaggedSimpleEvent | core_events.TaggedSequentialEvent | core_events.SimultaneousEvent
-    :param start_or_start_range: Sets when the event starts. This can
-        be a single :class:`mutwo.core_parameters.abc.Duration` or a
-        :class:`ranges.Range` of two durations. In the second case
-        the placement is flexible within the given area.
-    :type start_or_start_range: UnspecificTimeOrTimeRange
-    :param end_or_end_range: Sets when the event ends. This can
-        be a single :class:`mutwo.core_parameters.abc.Duration` or a
-        :class:`ranges.Range` of two durations. In the second case
-        the placement is flexible within the given area.
-    :type end_or_end_range: UnspecificTimeOrTimeRange
+__all__ = ("TimeLineToEventPlacementDict", "TimeLineToSimultaneousEvent")
 
-    **Warning:**
+Tag: typing.TypeAlias = "str"
 
-    An :class:`EventPlacement` itself is not an event and can't be treated
-    like an event.
+
+class TimeLineToEventPlacementDict(core_converters.abc.Converter):
+    def convert(
+        self, timeline_to_convert: timeline_interfaces.TimeLine
+    ) -> dict[Tag, tuple[timeline_interfaces.EventPlacement, ...]]:
+        timeline_to_convert.sort()
+        tag_to_event_placement_list = {tag: [] for tag in timeline_to_convert.tag_set}
+        for event_placement in timeline_to_convert.event_placement_tuple:
+            for tag in event_placement.tag_tuple:
+                # TODO(Add checks for overlaps!)
+                tag_to_event_placement_list[tag].append(event_placement)
+        return {
+            tag: tuple(event_placement_list)
+            for tag, event_placement_list in tag_to_event_placement_list.items()
+        }
+
+
+class TimeLineToSimultaneousEvent(core_converters.abc.Converter):
+    """Create event with SimultaneousEvent for each tag.
+
+    :param random_seed: Seed for random operation in case
+        `start_or_start_range` or `end_or_end_range` of an
+        :class:`mutwo.timeline_interfaces.EventPlacement` is a
+        `ranges.Range` and :class:`TimeLineToSimultaneousEvent`
+        needs to pick a value within the given range.
+    :type random_seed: int
+
+    The main intention of this converter is to convert a
+    :class:`TimeLine` into a representation which is useable
+    for concrete third party converters like
+    :class:`mutwo.midi_converters.EventToMidiFile`.
+
+    To be successful the tagged events in the
+    :class:`mutwo.timeline_interfaces.EventPlacement` in the
+    :class:`mutwo.timeline_interfaces.TimeLine` which is
+    converted need a specific structure: the deepest nested
+    structure they can follow is:
+
+        core_events.SimultaneousEvent[
+            core_events.SequentialEvent[
+                core_events.SimpleEvent
+            ]
+        ]
+
+    Because this will be the final structure. This clean
+    ordering is necessary to be functional with various third
+    party converters as e.g.
+    :class:`mutwo.midi_converters.EventToMidiFile`.
     """
 
-    def __init__(
-        self,
-        event: core_events.TaggedSimpleEvent
-        | core_events.TaggedSequentialEvent
-        | core_events.SimultaneousEvent,
-        start_or_start_range: UnspecificTimeOrTimeRange,
-        end_or_end_range: UnspecificTimeOrTimeRange,
-    ):
-        # Ensure we get ranges filled with Duration objects or single
-        # duration objects.
-        self.start_or_start_range = start_or_start_range
-        self.end_or_end_range = end_or_end_range
-        self.event = event
-
-    # ###################################################################### #
-    #                       private static methods                           #
-    # ###################################################################### #
-
-    @staticmethod
-    def _unspecified_to_specified_time_or_time_range(
-        unspecified_time_or_time_range: UnspecificTimeOrTimeRange,
-    ) -> TimeOrTimeRange:
-        if isinstance(unspecified_time_or_time_range, ranges.Range):
-            return ranges.Range(
-                *tuple(
-                    core_events.configurations.UNKNOWN_OBJECT_TO_DURATION(
-                        unknown_object
-                    )
-                    for unknown_object in (
-                        unspecified_time_or_time_range.start,
-                        unspecified_time_or_time_range.end,
-                    )
-                )
-            )
-        else:
-            return core_events.configurations.UNKNOWN_OBJECT_TO_DURATION(
-                unspecified_time_or_time_range
-            )
+    def __init__(self, random_seed: int = 100):
+        self._random = np.random.default_rng(random_seed)
 
-    @staticmethod
-    def _get_mean_of_time_or_time_range(
-        time_or_time_range: TimeOrTimeRange,
+    def _time_or_time_range_to_time(
+        self, time_or_time_range: ranges.Range | core_parameters.abc.Duration
     ) -> core_parameters.abc.Duration:
         if isinstance(time_or_time_range, ranges.Range):
             return core_parameters.DirectDuration(
-                statistics.mean(
-                    (time_or_time_range.start.duration, time_or_time_range.end.duration)
+                self._random.uniform(
+                    float(time_or_time_range.start), float(time_or_time_range.end)
                 )
             )
-        else:
-            return time_or_time_range
-
-    @staticmethod
-    def _get_extrema_of_time_or_time_range(
-        time_or_time_range: TimeOrTimeRange,
-        operation: typing.Callable[[typing.Sequence], core_parameters.abc.Duration],
-    ):
-        if isinstance(time_or_time_range, ranges.Range):
-            return operation((time_or_time_range.start, time_or_time_range.end))
-        else:
-            return time_or_time_range
-
-    @staticmethod
-    def _move_time_or_time_range(
-        time_or_time_range: TimeOrTimeRange, duration: core_parameters.abc.Duration
-    ) -> TimeOrTimeRange:
-        if isinstance(time_or_time_range, ranges.Range):
-            time_or_time_range.start += duration
-            time_or_time_range.end += duration
-            return time_or_time_range
-        else:
-            return time_or_time_range + duration
-
-    # ###################################################################### #
-    #                          magic methods                                 #
-    # ###################################################################### #
-
-    def __eq__(self, other: typing.Any) -> bool:
-        return core_utilities.test_if_objects_are_equal_by_parameter_tuple(
-            self, other, ("event", "start_or_start_range", "end_or_end_range")
-        )
+        return time_or_time_range
 
-    def __str__(self) -> str:
+    def _event_placement_to_start_and_end(
+        self, event_placement: timeline_interfaces.EventPlacement
+    ) -> tuple[core_parameters.abc.Duration, core_parameters.abc.Duration]:
         return (
-            f"{type(self).__name__}(event = '{self.event}', "
-            f"start_or_start_range = '{self.start_or_start_range}', "
-            f"end_or_end_range = '{self.end_or_end_range}'"
+            self._time_or_time_range_to_time(event_placement.start_or_start_range),
+            self._time_or_time_range_to_time(event_placement.end_or_end_range),
         )
 
-    # ###################################################################### #
-    #                          public properties                             #
-    # ###################################################################### #
-
-    @property
-    def start_or_start_range(self) -> TimeOrTimeRange:
-        return self._start_or_start_range
-
-    @start_or_start_range.setter
-    def start_or_start_range(self, start_or_start_range: UnspecificTimeOrTimeRange):
-        self._start_or_start_range = (
-            EventPlacement._unspecified_to_specified_time_or_time_range(
-                start_or_start_range
-            )
-        )
+    def _append_to_simultaneous_event(
+        self,
+        start: core_parameters.abc.Duration,
+        simultaneous_event: core_events.TaggedSimultaneousEvent,
+        event_to_append: core_events.SimultaneousEvent[
+            core_events.SequentialEvent[core_events.SimpleEvent]
+        ],
+    ):
+        if start > (simultaneous_event_duration := simultaneous_event.duration):
+            # In case our simultaneous event is still empty, 'extend_until'
+            # will do nothing (because it only extends sequential events,
+            # but ignores simultaneous events). Therefore we need to explicitly
+            # add a sequential event before extending.
+            if not simultaneous_event:
+                simultaneous_event.append(core_events.SequentialEvent([]))
+            simultaneous_event.extend_until(start)
+        # We have an overlap
+        elif start < simultaneous_event_duration:
+            # TODO(We need to check for overlaps. If we find overlaps:
+            #       (a) with prohibit flag
+            #       (b) with allow flag
+            #
+            #       (a) raise Exception
+            #       (b) check for all other SequentialEvents,
+            #           how many are they where we don't have
+            #           any conflicts? Where are they? (save in list)
+            #           If there aren't enough, add new sequential events.
+            #           Then: only append to the sequential events without
+            #           conflicts.
+            # elif rest_duration < 0
+            raise NotImplementedError("Overlap handler isn't implemented yet!")
 
-    @property
-    def end_or_end_range(self) -> TimeOrTimeRange:
-        return self._end_or_end_range
-
-    @end_or_end_range.setter
-    def end_or_end_range(self, end_or_end_range: UnspecificTimeOrTimeRange):
-        self._end_or_end_range = (
-            EventPlacement._unspecified_to_specified_time_or_time_range(
-                end_or_end_range
-            )
-        )
+        try:
+            simultaneous_event.concatenate_by_tag(event_to_append)
+        except core_utilities.NoTagError:
+            simultaneous_event.concatenate_by_index(event_to_append)
 
-    @property
-    def duration(self) -> core_parameters.abc.Duration:
-        return self.max_end - self.min_start
-
-    @property
-    def mean_start(self) -> core_parameters.abc.Duration:
-        return EventPlacement._get_mean_of_time_or_time_range(self.start_or_start_range)
-
-    @property
-    def mean_end(self) -> core_parameters.abc.Duration:
-        return EventPlacement._get_mean_of_time_or_time_range(self.end_or_end_range)
-
-    @property
-    def min_start(self) -> core_parameters.abc.Duration:
-        return EventPlacement._get_extrema_of_time_or_time_range(
-            self.start_or_start_range, min
-        )
+    def _add_tagged_event_to_simultaneous_event(
+        self,
+        start: core_parameters.abc.Duration,
+        simultaneous_event: core_events.TaggedSimultaneousEvent,
+        tagged_event: core_events.TaggedSimpleEvent
+        | core_events.TaggedSequentialEvent
+        | core_events.TaggedSimultaneousEvent,
+    ):
+        if isinstance(tagged_event, core_events.SimpleEvent):
+            tagged_event = core_events.SimultaneousEvent(
+                [core_events.SequentialEvent([tagged_event])]
+            )
+        elif isinstance(tagged_event, core_events.SequentialEvent):
+            tagged_event = core_events.SimultaneousEvent([tagged_event])
+        self._append_to_simultaneous_event(start, simultaneous_event, tagged_event)
 
-    @property
-    def max_start(self) -> core_parameters.abc.Duration:
-        return EventPlacement._get_extrema_of_time_or_time_range(
-            self.start_or_start_range, max
-        )
+    def _event_placement_to_event(
+        self,
+        event_placement: timeline_interfaces.EventPlacement,
+        start: core_parameters.abc.Duration,
+        end: core_parameters.abc.Duration,
+    ) -> core_events.SimultaneousEvent:
+        event_duration = end - start
+        event = event_placement.event.set("duration", event_duration, mutate=False)
+        return event
+
+    def convert(
+        self, timeline_to_convert: timeline_interfaces.TimeLine
+    ) -> core_events.SimultaneousEvent[
+        core_events.TaggedSimultaneousEvent[
+            core_events.SequentialEvent[core_events.SimpleEvent]
+        ]
+    ]:
+        duration = timeline_to_convert.duration
+        tag_set = timeline_to_convert.tag_set
 
-    @property
-    def min_end(self) -> core_parameters.abc.Duration:
-        return EventPlacement._get_extrema_of_time_or_time_range(
-            self.end_or_end_range, min
-        )
+        tag_to_tagged_simultaneous_event = {
+            tag: core_events.TaggedSimultaneousEvent([], tag=tag) for tag in tag_set
+        }
 
-    @property
-    def max_end(self) -> core_parameters.abc.Duration:
-        return EventPlacement._get_extrema_of_time_or_time_range(
-            self.end_or_end_range, max
-        )
+        timeline_to_convert.sort()
+        for event_placement in timeline_to_convert.event_placement_tuple:
+            start, end = self._event_placement_to_start_and_end(event_placement)
+            for tagged_event in self._event_placement_to_event(
+                event_placement, start, end
+            ):
+                tag = tagged_event.tag
+                self._add_tagged_event_to_simultaneous_event(
+                    start,
+                    tag_to_tagged_simultaneous_event[tag],
+                    tagged_event,
+                )
 
-    @property
-    def time_range(self) -> ranges.Range:
-        return ranges.Range(self.min_start, self.max_end)
-
-    # ###################################################################### #
-    #                          public methods                                #
-    # ###################################################################### #
-
-    def is_overlapping(self, other: EventPlacement) -> bool:
-        return not self.time_range.isdisjoint(other.time_range)
-
-    @core_utilities.add_copy_option
-    def move_by(self, duration: UnspecificTime) -> EventPlacement:
-        duration = core_events.configurations.UNKNOWN_OBJECT_TO_DURATION(duration)
-        self.start_or_start_range, self.end_or_end_range = (
-            EventPlacement._move_time_or_time_range(time_or_time_range, duration)
-            for time_or_time_range in (self.start_or_start_range, self.end_or_end_range)
+        duration = duration or max(
+            (e.duration for e in tag_to_tagged_simultaneous_event.values())
         )
-        return self
+        [e.extend_until(duration) for e in tag_to_tagged_simultaneous_event.values()]
 
-    def copy(self) -> EventPlacement:
-        return type(self)(
-            self.event.copy(),
-            copy.copy(self.start_or_start_range),
-            copy.copy(self.end_or_end_range),
+        return core_events.SimultaneousEvent(
+            tuple(tag_to_tagged_simultaneous_event.values())
         )
 
 
-class TimeLine(object):
-    """Timeline to place events on.
-
-    :param duration: If this is set to `None` the ``duration``
-        property of the `TimeLine` is dynamically calculated
-        (by the end times of all registered :class:`EventPlacement`.
-        If the duration is not `None`, then the duration is statically
-        set to this time. If the user tries to register an
-        :class:`EventPlacement` with end > duration this would raise
-        an error. Default to ``None``.
-    :type duration: typing.Optional[UnspecificTime]
-    :param prohibit_overlaps: If set to ``True`` the :class:`TimeLine`
-        will prohibit any action which creates overlapping
-        :class:`EventPlacement` with the same tag. Default to ``True``.
-    :type prohibit_overlaps: bool
+class TimeLineToEventPlacementTuple(core_converters.abc.Converter):
+    """Fetch from :class:`~mutwo.timeline_interfaces.TimeLine` all :class:`~mutwo.timeline_interfaces.EventPlacement` which contains of user defined tags.
 
-    **Warning:**
-
-    An :class:`TimeLine` itself is not an event and can't be treated
-    like an event.
+    Unlike :class:`TimeLineToEventPlacementDict` this converter
+    doesn't split the fetched :class:`mutwo.timeline_interfaces.EventPlacement`s
+    into different `tuples`, but returns all of them in one common `tuple`.
     """
 
-    MinStartTime: typing.TypeAlias = "Time"
-    TimeRange: typing.TypeAlias = ranges.Range
-    # In this way we can easily and very fast register
-    # new EventPlacements.
-    EventContainer: typing.TypeAlias = tuple[
-        list[MinStartTime], list[TimeRange], list[EventPlacement]
-    ]
-
-    def __init__(
+    def convert(
         self,
-        duration: typing.Optional[UnspecificTime] = None,
-        prohibit_overlaps: bool = True,
-        *args,
-        **kwargs,
-    ):
+        timeline_to_convert: timeline_interfaces.TimeLine,
+        tag_tuple: tuple[Tag, ...],
+    ) -> tuple[timeline_interfaces.EventPlacement, ...]:
+        timeline_to_convert.sort()
+
+        # XXX: Should we add any checks for overlaps?
+        event_placement_list: list[timeline_interfaces.EventPlacement] = []
+        for event_placement in timeline_to_convert.event_placement_tuple:
+            if any([tag in tag_tuple for tag in event_placement.tag_tuple]):
+                event_placement_list.append(event_placement.copy())
+
+        return tuple(event_placement_list)
+
+
+class EventPlacementTupleToSplitEventPlacementDict(core_converters.abc.Converter):
+    """Split :class:`~mutwo.timeline_interfaces.EventPlacement` into new `EventPlacement`s by tags.
+
+    So the returned `event` attribute of each returned
+    :class:`mutwo.timeline_interfaces.EventPlacement` only
+    contains one specific tagged event.
+    """
 
-        self._dynamic_duration = duration is None
-        self._duration = duration
-        self._tag_to_event_container: dict[str, TimeLine.EventContainer] = {}
-        self._prohibit_overlaps = prohibit_overlaps
-
-    # ###################################################################### #
-    #                          public properties                             #
-    # ###################################################################### #
-
-    @property
-    def duration(self) -> core_parameters.abc.Duration:
-        if self._dynamic_duration:
-            try:
-                return max(
-                    [
-                        event_container[1][-1].end
-                        for event_container in self._tag_to_event_container.values()
-                    ]
+    def convert(
+        self,
+        event_placement_tuple_to_convert: tuple[
+            timeline_interfaces.EventPlacement, ...
+        ],
+    ) -> dict[Tag, tuple[timeline_interfaces.EventPlacement, ...]]:
+        tag_to_event_placement_list: dict[
+            str, list[timeline_interfaces.EventPlacement]
+        ] = {}
+        for event_placement in event_placement_tuple_to_convert:
+            for event_index, event in enumerate(event_placement.event):
+                try:
+                    event_placement_list = tag_to_event_placement_list[event.tag]
+                except KeyError:
+                    event_placement_list = []
+                    tag_to_event_placement_list.update(
+                        {event.tag: event_placement_list}
+                    )
+                new_event_placement = event_placement.copy()
+                new_event_placement.event = core_events.SimultaneousEvent(
+                    [new_event_placement.event[event_index]]
                 )
-            # If there isn't any registered EventPlacement yet.
-            except ValueError:
-                return 0
-        else:
-            return self._duration
-
-    @property
-    def prohibit_overlaps(self) -> bool:
-        return self._prohibit_overlaps
-
-    # ###################################################################### #
-    #                          public methods                                #
-    # ###################################################################### #
-
-    def register(self, event_placement: EventPlacement):
-        """Register a new :class:`EventPlacement` on given :class:`TimeLine`.
-
-        :param event_placement: The :class:`EventPlacement` which should be
-            placed on the :class:`TimeLine`.
-        :type event_placement: EventPlacement
-
-        When registering an `EventPlacement`, a copy of the `EventPlacement`
-        is saved. The registered `EventPlacement` will only be changeable by
-        methods provided by :class:`TimeLine`. In this way, :class:`TimeLine`
-        can internally easily and in an performant way register new
-        :class:`EventPlacement`s and check if any :class:`EventPlacement`
-        is overlapping with any already defined one.
-        """
-        event_placement = event_placement.copy()
-        tag = event_placement.event.tag
-        time_range = event_placement.time_range
-        start = time_range.start
-
-        if not self._dynamic_duration:
-            if time_range.end > (duration := self.duration):
-                raise timeline_utilities.ExceedDurationError(event_placement, duration)
-
-        try:
-            (
-                start_list,
-                time_range_list,
-                event_placement_list,
-            ) = self._tag_to_event_container[tag]
-        except KeyError:
-            self._tag_to_event_container.update(
-                {tag: ([start], [time_range], [event_placement])}
-            )
-            return
+                event_placement_list.append(new_event_placement)
+        return {
+            tag: tuple(event_placement_list)
+            for tag, event_placement_list in tag_to_event_placement_list.items()
+        }
 
-        insert_index = bisect.bisect_left(start_list, start)
 
-        try:
-            event_placement_after = event_placement_list[insert_index]
-        except IndexError:
-            event_placement_after = None
-
-        if self.prohibit_overlaps:
-            before_insert_index = insert_index - 1
-            event_placement_to_compare_list = (
-                [event_placement_list[before_insert_index]]
-                if before_insert_index >= 0
-                else []
-            )
-            if event_placement_after is not None:
-                event_placement_to_compare_list.append(event_placement_after)
-            for event_placement_to_compare in event_placement_to_compare_list:
-                if event_placement.is_overlapping(event_placement_to_compare):
-                    raise timeline_utilities.OverlappingEventPlacementError(
-                        event_placement, event_placement_to_compare
-                    )
+class EventPlacementTupleToGaplessEventPlacementTuple(core_converters.abc.Converter):
+    """Fill empty :class:`~mutwo.timeline_interfaces.EventPlacement` into the gaps between two `EventPlacement`."""
 
-        # If both EventPlacement are at the same time,
-        # we will move the EventPlacement with the later end
-        # time to the second position.
-        if (
-            event_placement_after is not None
-            and start_list[insert_index] == start
-            and time_range.end > time_range_list[insert_index].end
+    def convert(
+        self,
+        event_placement_tuple_to_convert: tuple[
+            timeline_interfaces.EventPlacement, ...
+        ],
+        duration: typing.Optional[core_parameters.abc.Duration] = None,
+    ) -> tuple[timeline_interfaces.EventPlacement, ...]:
+        def add_rest(
+            start: core_parameters.abc.Duration, end: core_parameters.abc.Duration
         ):
-            insert_index += 1
-
-        start_list.insert(insert_index, start)
-        time_range_list.insert(insert_index, time_range)
-        event_placement_list.insert(insert_index, event_placement)
+            new_event_placement_list.append(
+                timeline_interfaces.EventPlacement(
+                    core_events.SimultaneousEvent(
+                        [core_events.TaggedSimpleEvent(0, tag=tag)]
+                    ),
+                    start,
+                    end,
+                )
+            )
 
-    def fetch_tag_to_event_placement_dict(
-        self,
-    ) -> dict[str, tuple[EventPlacement, ...]]:
-        """Fetch a tag -> tuple[event_placement, ...] dict.
+        event_placement_list = sorted(
+            event_placement_tuple_to_convert,
+            key=lambda event_placement: (
+                event_placement.min_start,
+                event_placement.max_end,
+            ),
+        )
 
-        **Warning:**
+        new_event_placement_list = []
+        last_end = 0
+        tag = None
+        for event_placement in event_placement_list:
+            if tag is None:
+                tag = event_placement.event[0].tag
+            start, end = event_placement.min_start, event_placement.max_end
+            if start > last_end:
+                add_rest(last_end, start)
+            new_event_placement_list.append(event_placement.copy())
+            last_end = end
 
-        The returned :class:`EventPlacement`s are copies of the
-        internal :class:`EventPlacement`s of the :class:`TimeLine`.
-        In this way the :class:`TimeLine` can ensure internal consistency.
-        This means that `fetch_tag_to_event_placement_dict` is
-        an expensive operation, because it needs to copy all
-        :class:`EventPlacement`. It also means that any changes
-        on the returned objects won't affect any objects
-        inside the :class:`TimeLine`.
-        """
+        if duration is not None and last_end < duration:
+            add_rest(last_end, duration)
 
-        return {
-            tag: tuple(event_placement.copy() for event_placement in event_container[2])
-            for tag, event_container in self._tag_to_event_container.items()
-        }
+        return tuple(new_event_placement_list)
```

### Comparing `mutwo.timeline-0.1.0/mutwo.timeline.egg-info/PKG-INFO` & `mutwo.timeline-0.4.0/mutwo.timeline.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mutwo.timeline
-Version: 0.1.0
+Version: 0.4.0
 Summary: timeline extension for event based framework for generative art
 Home-page: https://github.com/mutwo-org/mutwo.timeline
 Author: Levin Eric Zimmermann
 Author-email: levin.eric.zimmermann@posteo.eu
 License: GPL
 Project-URL: Documentation, https://mutwo.readthedocs.io/en/latest/
 Requires-Python: >=3.10, <4
@@ -27,15 +27,15 @@
 and end time of any event dependent on all events which happens before the
 given event. This extension implements the possibility to model events with
 independent start and end times in `mutwo`.
 
 This extension implements:
 
 - `mutwo.timeline_converters`
-- `mutwo.timeline_events`
+- `mutwo.timeline_interfaces`
 - `mutwo.timeline_utilities`
 
 ### Installation
 
 mutwo.timeline is available on [pypi](https://pypi.org/project/mutwo.timeline/) and can be installed via pip:
 
 ```sh
```

### Comparing `mutwo.timeline-0.1.0/setup.py` & `mutwo.timeline-0.4.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -29,14 +29,14 @@
         for package in setuptools.find_namespace_packages(
             include=["mutwo.*", "mutwo_third_party.*"]
         )
         if package[:5] != "tests"
     ],
     setup_requires=[],
     install_requires=[
-        "mutwo.core>=1.0.0, <2.0.0",
+        "mutwo.core>=1.2.1, <2.0.0",
         "python-ranges>=1.2.0, <2.0.0",
         "numpy>=1.18, <2.00",
     ],
     extras_require=extras_require,
     python_requires=">=3.10, <4",
 )
```

