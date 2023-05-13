# Comparing `tmp/bentley_ottmann-7.3.0.tar.gz` & `tmp/bentley_ottmann-8.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bentley_ottmann-7.3.0.tar", last modified: Tue Jun 14 21:11:15 2022, max compression
+gzip compressed data, was "bentley_ottmann-8.0.0.tar", last modified: Sat May 13 00:01:49 2023, max compression
```

## Comparing `bentley_ottmann-7.3.0.tar` & `bentley_ottmann-8.0.0.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 21:11:15.186267 bentley_ottmann-7.3.0/
--rw-r--r--   0 runner    (1001) docker     (121)     1069 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       41 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)     4615 2022-06-14 21:11:15.186267 bentley_ottmann-7.3.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     3746 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 21:11:15.186267 bentley_ottmann-7.3.0/bentley_ottmann/
--rw-r--r--   0 runner    (1001) docker     (121)       84 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/bentley_ottmann/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 21:11:15.186267 bentley_ottmann-7.3.0/bentley_ottmann/core/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/bentley_ottmann/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     4419 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/bentley_ottmann/core/base.py
--rw-r--r--   0 runner    (1001) docker     (121)     5853 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/bentley_ottmann/core/event.py
--rw-r--r--   0 runner    (1001) docker     (121)     7574 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/bentley_ottmann/core/events_queue.py
--rw-r--r--   0 runner    (1001) docker     (121)     4007 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/bentley_ottmann/core/sweep_line.py
--rw-r--r--   0 runner    (1001) docker     (121)     1501 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/bentley_ottmann/core/utils.py
--rw-r--r--   0 runner    (1001) docker     (121)     5828 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/bentley_ottmann/planar.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 21:11:15.186267 bentley_ottmann-7.3.0/bentley_ottmann.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     4615 2022-06-14 21:11:14.000000 bentley_ottmann-7.3.0/bentley_ottmann.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      497 2022-06-14 21:11:15.000000 bentley_ottmann-7.3.0/bentley_ottmann.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-06-14 21:11:14.000000 bentley_ottmann-7.3.0/bentley_ottmann.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       77 2022-06-14 21:11:14.000000 bentley_ottmann-7.3.0/bentley_ottmann.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       16 2022-06-14 21:11:15.000000 bentley_ottmann-7.3.0/bentley_ottmann.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       77 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-06-14 21:11:15.186267 bentley_ottmann-7.3.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1329 2022-06-14 21:11:01.000000 bentley_ottmann-7.3.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:01:49.213438 bentley_ottmann-8.0.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     5935 2023-05-13 00:01:49.213438 bentley_ottmann-8.0.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3746 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:01:49.209438 bentley_ottmann-8.0.0/bentley_ottmann/
+-rw-r--r--   0 runner    (1001) docker     (123)       84 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/bentley_ottmann/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:01:49.213438 bentley_ottmann-8.0.0/bentley_ottmann/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/bentley_ottmann/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4603 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/bentley_ottmann/core/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6423 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/bentley_ottmann/core/event.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7716 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/bentley_ottmann/core/events_queue.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4115 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/bentley_ottmann/core/sweep_line.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1748 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/bentley_ottmann/core/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5668 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/bentley_ottmann/planar.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:01:49.209438 bentley_ottmann-8.0.0/bentley_ottmann.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5935 2023-05-13 00:01:49.000000 bentley_ottmann-8.0.0/bentley_ottmann.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      495 2023-05-13 00:01:49.000000 bentley_ottmann-8.0.0/bentley_ottmann.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:01:49.000000 bentley_ottmann-8.0.0/bentley_ottmann.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 00:01:49.000000 bentley_ottmann-8.0.0/bentley_ottmann.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 00:01:49.000000 bentley_ottmann-8.0.0/bentley_ottmann.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1294 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 00:01:49.213438 bentley_ottmann-8.0.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      290 2023-05-13 00:01:33.000000 bentley_ottmann-8.0.0/setup.py
```

### Comparing `bentley_ottmann-7.3.0/LICENSE` & `bentley_ottmann-8.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `bentley_ottmann-7.3.0/PKG-INFO` & `bentley_ottmann-8.0.0/README.md`

 * *Files 25% similar despite different names*

```diff
@@ -1,39 +1,18 @@
-Metadata-Version: 2.1
-Name: bentley_ottmann
-Version: 7.3.0
-Summary: Searching line segments & polygon edges intersections.
-Home-page: https://github.com/lycantropos/bentley_ottmann/
-Download-URL: https://github.com/lycantropos/bentley_ottmann/archive/master.zip
-Author: Azat Ibrakov
-Author-email: azatibrakov@gmail.com
-License: MIT License
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: Implementation :: CPython
-Classifier: Programming Language :: Python :: Implementation :: PyPy
-Requires-Python: >=3.6
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 bentley_ottmann
 ===============
 
 [![](https://github.com/lycantropos/bentley_ottmann/workflows/CI/badge.svg?branch=master)](https://github.com/lycantropos/bentley_ottmann/actions/workflows/ci.yml "Github Actions")
 [![](https://readthedocs.org/projects/bentley_ottmann/badge/?version=latest)](https://bentley-ottmann.readthedocs.io/en/latest "Documentation")
 [![](https://codecov.io/gh/lycantropos/bentley_ottmann/branch/master/graph/badge.svg)](https://codecov.io/gh/lycantropos/bentley_ottmann "Codecov")
 [![](https://img.shields.io/github/license/lycantropos/bentley_ottmann.svg)](https://github.com/lycantropos/bentley_ottmann/blob/master/LICENSE "License")
 [![](https://badge.fury.io/py/bentley-ottmann.svg)](https://badge.fury.io/py/bentley-ottmann "PyPI")
 
-In what follows `python` is an alias for `python3.6` or `pypy3.6`
-or any later version (`python3.7`, `pypy3.7` and so on).
+In what follows `python` is an alias for `python3.7` or `pypy3.7`
+or any later version (`python3.8`, `pypy3.8` and so on).
 
 Installation
 ------------
 
 Install the latest `pip` & `setuptools` packages versions
 ```bash
 python -m pip install --upgrade pip setuptools
```

### Comparing `bentley_ottmann-7.3.0/bentley_ottmann/core/base.py` & `bentley_ottmann-8.0.0/bentley_ottmann/core/base.py`

 * *Files 10% similar despite different names*

```diff
@@ -17,26 +17,27 @@
 
 def sweep(segments: Sequence[Segment],
           *,
           context: Context) -> Iterable[LeftEvent]:
     events_queue = EventsQueue.from_segments(segments,
                                              context=context)
     sweep_line = SweepLine(context)
-    start = (events_queue.peek().start
-             if events_queue
-             else None)  # type: Optional[Point]
-    same_start_events = []  # type: List[Event]
+    start: Optional[Point] = (events_queue.peek().start
+                              if events_queue
+                              else None)
+    same_start_events: List[Event] = []
     while events_queue:
         event = events_queue.pop()
         if event.start == start:
             same_start_events.append(event)
         else:
             yield from complete_events_relations(same_start_events)
             same_start_events, start = [event], event.start
         if event.is_left:
+            assert isinstance(event, LeftEvent), event
             equal_segment_event = sweep_line.find_equal(event)
             if equal_segment_event is None:
                 sweep_line.add(event)
                 below_event = sweep_line.below(event)
                 if below_event is not None:
                     events_queue.detect_intersection(below_event, event,
                                                      sweep_line)
@@ -60,23 +61,26 @@
                     events_queue.detect_intersection(below_event, above_event,
                                                      sweep_line)
                 if event is not equal_segment_event:
                     equal_segment_event.merge_with(event)
     yield from complete_events_relations(same_start_events)
 
 
-def complete_events_relations(same_start_events: Sequence[Event]
-                              ) -> Iterable[Event]:
+def complete_events_relations(
+        same_start_events: Sequence[Event]
+) -> Iterable[LeftEvent]:
     for offset, first in enumerate(same_start_events,
                                    start=1):
         first_left = first if first.is_left else first.left
+        assert isinstance(first_left, LeftEvent), first_left
         first_ids = first_left.segments_ids
         for second_index in range(offset, len(same_start_events)):
             second = same_start_events[second_index]
             second_left = second if second.is_left else second.left
+            assert isinstance(second_left, LeftEvent), second_left
             second_ids = second_left.segments_ids
             first_extra_ids_count, second_extra_ids_count = (
                 len(first_ids - second_ids), len(second_ids - first_ids)
             )
             if first_extra_ids_count and second_extra_ids_count:
                 relation = (Relation.TOUCH
                             if (first.start == first.original_start
```

### Comparing `bentley_ottmann-7.3.0/bentley_ottmann/core/event.py` & `bentley_ottmann-8.0.0/bentley_ottmann/core/event.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,14 @@
+from __future__ import annotations
+
 from abc import (ABC,
                  abstractmethod)
 from reprlib import recursive_repr
-from typing import (Dict,
+from typing import (ClassVar,
+                    Dict,
                     List,
                     Optional,
                     Sequence,
                     Set,
                     Tuple)
 
 from ground.base import Relation
@@ -16,17 +19,17 @@
 from .utils import (classify_overlap,
                     to_sorted_pair)
 
 
 class Event(ABC):
     __slots__ = ()
 
-    is_left = False
-    left = None  # type: Optional['LeftEvent']
-    right = None  # type: Optional['RightEvent']
+    is_left: ClassVar[bool]
+    left: LeftEvent
+    right: RightEvent
 
     @property
     @abstractmethod
     def end(self) -> Point:
         """Returns end of the event."""
 
     @property
@@ -57,18 +60,18 @@
     @abstractmethod
     def tangents(self) -> Sequence['Event']:
         """Returns tangents of the event."""
 
 
 class LeftEvent(Event):
     @classmethod
-    def from_segment(cls, segment: Segment, segment_id: int) -> 'LeftEvent':
+    def from_segment(cls, segment: Segment, segment_id: int) -> LeftEvent:
         start, end = to_sorted_pair(segment.start, segment.end)
         result = LeftEvent(start, None, start, {start: {end: {segment_id}}})
-        result.right = RightEvent(end, result, end)
+        result._right = RightEvent(end, result, end)
         return result
 
     is_left = True
 
     @property
     def end(self) -> Point:
         return self.right.start
@@ -82,58 +85,70 @@
         return self.right.original_start
 
     @property
     def segments_ids(self) -> Set[int]:
         return self.parts_ids[self.start][self.end]
 
     @property
+    def right(self) -> RightEvent:
+        result = self._right
+        assert result is not None, self
+        return result
+
+    @right.setter
+    def right(self, value: RightEvent) -> None:
+        self._right = value
+
+    @property
     def start(self) -> Point:
         return self._start
 
     @property
     def tangents(self) -> Sequence[Event]:
         return self._tangents
 
-    __slots__ = ('parts_ids', 'right', '_original_start', '_relations_mask',
+    _right: Optional[RightEvent]
+
+    __slots__ = ('parts_ids', '_original_start', '_relations_mask', '_right',
                  '_start', '_tangents')
 
     def __init__(self,
                  start: Point,
-                 right: Optional['RightEvent'],
+                 right: Optional[RightEvent],
                  original_start: Point,
                  parts_ids: Dict[Point, Dict[Point, Set[int]]]) -> None:
-        self.right, self.parts_ids, self._original_start, self._start = (
+        self._right, self.parts_ids, self._original_start, self._start = (
             right, parts_ids, original_start, start
         )
         self._relations_mask = 0
         self._tangents = []  # type: List[Event]
 
     __repr__ = recursive_repr()(generate_repr(__init__))
 
-    def divide(self, point: Point) -> Tuple['RightEvent', 'LeftEvent']:
+    def divide(self, point: Point) -> Tuple[RightEvent, LeftEvent]:
         """Divides the event at given break point and returns tail."""
         segments_ids = self.segments_ids
         (self.parts_ids.setdefault(self.start, {})
          .setdefault(point, set()).update(segments_ids))
         (self.parts_ids.setdefault(point, {})
          .setdefault(self.end, set()).update(segments_ids))
         point_to_end_event = self.right.left = LeftEvent(
                 point, self.right, self.original_start, self.parts_ids
         )
-        point_to_start_event = self.right = RightEvent(point, self,
-                                                       self.original_end)
+        point_to_start_event = self._right = RightEvent(point, self,
+                                                        self.original_end)
         return point_to_start_event, point_to_end_event
 
     def has_only_relations(self, *relations: Relation) -> bool:
         mask = self._relations_mask
         for relation in relations:
             mask &= ~(1 << relation)
         return not mask
 
-    def merge_with(self, other: 'LeftEvent') -> None:
+    def merge_with(self, other: LeftEvent) -> None:
         assert self.start == other.start and self.end == other.end
         full_relation = classify_overlap(
                 other.original_start, other.original_end,
                 self.original_start, self.original_end
         )
         self.register_relation(full_relation)
         other.register_relation(full_relation.complement)
@@ -147,19 +162,31 @@
         self._tangents.append(tangent)
 
     def register_relation(self, relation: Relation) -> None:
         self._relations_mask |= 1 << relation
 
 
 class RightEvent(Event):
+    is_left = False
+
     @property
     def end(self) -> Point:
         return self.left.start
 
     @property
+    def left(self) -> LeftEvent:
+        result = self._left
+        assert result is not None, self
+        return result
+
+    @left.setter
+    def left(self, value: LeftEvent) -> None:
+        self._left = value
+
+    @property
     def original_end(self) -> Point:
         return self.left.original_start
 
     @property
     def original_start(self) -> Point:
         return self._original_start
 
@@ -171,22 +198,24 @@
     def start(self) -> Point:
         return self._start
 
     @property
     def tangents(self) -> Sequence[Event]:
         return self._tangents
 
-    __slots__ = 'left', '_original_start', '_start', '_tangents'
+    _left: Optional[LeftEvent]
+
+    __slots__ = '_left', '_original_start', '_start', '_tangents'
 
     def __init__(self,
                  start: Point,
                  left: Optional[LeftEvent],
                  original_start: Point) -> None:
-        self.left, self._original_start, self._start = (left, original_start,
-                                                        start)
+        self._left, self._original_start, self._start = (left, original_start,
+                                                         start)
         self._tangents = []  # type: List[Event]
 
     __repr__ = recursive_repr()(generate_repr(__init__))
 
     def register_tangent(self, tangent: 'Event') -> None:
         assert self.start == tangent.start
         self._tangents.append(tangent)
```

### Comparing `bentley_ottmann-7.3.0/bentley_ottmann/core/events_queue.py` & `bentley_ottmann-8.0.0/bentley_ottmann/core/events_queue.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,8 +1,11 @@
-from typing import Sequence
+from __future__ import annotations
+
+from typing import (Any,
+                    Sequence)
 
 from ground.base import (Context,
                          Relation)
 from ground.hints import Segment
 from prioq.base import PriorityQueue
 from reprit.base import generate_repr
 
@@ -24,15 +27,17 @@
             result.push(event.right)
         return result
 
     __slots__ = 'context', '_queue'
 
     def __init__(self, context: Context) -> None:
         self.context = context
-        self._queue = PriorityQueue(key=EventsQueueKey)
+        self._queue: PriorityQueue[EventsQueueKey, Event] = PriorityQueue(
+                key=EventsQueueKey
+        )
 
     __repr__ = generate_repr(__init__)
 
     def __bool__(self) -> bool:
         return bool(self._queue)
 
     def detect_intersection(self,
@@ -143,22 +148,24 @@
             raise ValueError('Degenerate segment found '
                              'with both endpoints being: {}.'
                              .format(event.start))
         self._queue.push(event)
 
 
 class EventsQueueKey:
+    event: Event
+
     __slots__ = 'event',
 
     def __init__(self, event: Event) -> None:
         self.event = event
 
     __repr__ = generate_repr(__init__)
 
-    def __lt__(self, other: 'EventsQueueKey') -> bool:
+    def __lt__(self, other: EventsQueueKey) -> Any:
         """
         Checks if the event should be processed before the other.
         """
         event, other_event = self.event, other.event
         start_x, start_y = event.start.x, event.start.y
         other_start_x, other_start_y = other_event.start.x, other_event.start.y
         if start_x != other_start_x:
```

### Comparing `bentley_ottmann-7.3.0/bentley_ottmann/core/sweep_line.py` & `bentley_ottmann-8.0.0/bentley_ottmann/core/sweep_line.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,27 +1,32 @@
+from __future__ import annotations
+
 from functools import partial
-from typing import (Callable,
+from typing import (Any,
+                    Callable,
                     Optional)
 
 from dendroid import red_black
+from dendroid.hints import KeyedSet
 from ground.base import (Context,
                          Orientation)
 from ground.hints import Point
 from reprit.base import generate_repr
 
 from .event import LeftEvent
 
 
 class SweepLine:
     __slots__ = 'context', '_set'
 
     def __init__(self, context: Context) -> None:
         self.context = context
-        self._set = red_black.set_(key=partial(SweepLineKey,
-                                               context.angle_orientation))
+        self._set: KeyedSet[SweepLineKey, LeftEvent] = red_black.set_(
+                key=partial(SweepLineKey, context.angle_orientation)
+        )
 
     __repr__ = generate_repr(__init__)
 
     def add(self, event: LeftEvent) -> None:
         self._set.add(event)
 
     def find_equal(self, event: LeftEvent) -> Optional[LeftEvent]:
@@ -57,15 +62,15 @@
     def __init__(self,
                  orienteer: Callable[[Point, Point, Point], Orientation],
                  event: LeftEvent) -> None:
         self.event, self.orienteer = event, orienteer
 
     __repr__ = generate_repr(__init__)
 
-    def __lt__(self, other: 'SweepLineKey') -> bool:
+    def __lt__(self, other: SweepLineKey) -> Any:
         """
         Checks if the segment (or at least the point) associated with event
         is lower than other's.
         """
         event, other_event = self.event, other.event
         if event is other_event:
             return False
```

### Comparing `bentley_ottmann-7.3.0/bentley_ottmann/core/utils.py` & `bentley_ottmann-8.0.0/bentley_ottmann/core/utils.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,20 +1,19 @@
-from typing import (Hashable,
-                    Iterable,
-                    Tuple,
-                    TypeVar)
+import typing as t
 
+import typing_extensions as te
 from ground.base import Relation
 from ground.hints import Point
 
-_T = TypeVar('_T')
+_HashableT = t.TypeVar('_HashableT',
+                       bound=t.Hashable)
 
 
-def all_unique(values: Iterable[Hashable]) -> bool:
-    seen = set()
+def all_unique(values: t.Iterable[_HashableT]) -> bool:
+    seen: t.Set[_HashableT] = set()
     seen_add = seen.add
     for value in values:
         if value in seen:
             return False
         else:
             seen_add(value)
     return True
@@ -43,9 +42,20 @@
     else:
         assert test_start < goal_start < test_end
         return (Relation.COMPOSITE
                 if goal_end < test_end
                 else Relation.OVERLAP)
 
 
-def to_sorted_pair(start: _T, end: _T) -> Tuple[_T, _T]:
+class _Comparable(te.Protocol):
+    def __lt__(self, other: te.Self) -> bool:
+        ...
+
+
+_ComparableT = t.TypeVar('_ComparableT',
+                         bound=_Comparable)
+
+
+def to_sorted_pair(
+        start: _ComparableT, end: _ComparableT
+) -> t.Tuple[_ComparableT, _ComparableT]:
     return (start, end) if start < end else (end, start)
```

### Comparing `bentley_ottmann-7.3.0/bentley_ottmann/planar.py` & `bentley_ottmann-8.0.0/bentley_ottmann/planar.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,25 +1,22 @@
-from itertools import product as _product
-from typing import (Optional as _Optional,
-                    Sequence as _Sequence)
+import typing as _t
 
 from ground.base import (Context as _Context,
                          Relation as _Relation,
                          get_context as _get_context)
 from ground.hints import (Contour as _Contour,
                           Segment as _Segment)
 
 from .core.base import sweep as _sweep
-from .core.utils import (all_unique as _all_unique,
-                         to_sorted_pair as _to_sorted_pair)
+from .core.utils import all_unique as _all_unique
 
 
 def contour_self_intersects(contour: _Contour,
                             *,
-                            context: _Optional[_Context] = None) -> bool:
+                            context: _t.Optional[_Context] = None) -> bool:
     """
     Checks if contour has self-intersection.
 
     Based on Bentley-Ottmann algorithm.
 
     Time complexity:
         ``O(len(contour.vertices) * log len(contour.vertices))``
@@ -65,17 +62,17 @@
     return not all(event.has_only_relations(_Relation.DISJOINT,
                                             _Relation.TOUCH)
                    and len(event.tangents) == 1
                    for event in _sweep(segments,
                                        context=context))
 
 
-def segments_intersect(segments: _Sequence[_Segment],
+def segments_intersect(segments: _t.Sequence[_Segment],
                        *,
-                       context: _Optional[_Context] = None) -> bool:
+                       context: _t.Optional[_Context] = None) -> bool:
     """
     Checks if segments have at least one intersection.
 
     Based on Shamos-Hoey algorithm.
 
     Time complexity:
         ``O(len(segments) * log len(segments))``
@@ -108,17 +105,17 @@
     return not all(event.has_only_relations(_Relation.DISJOINT)
                    for event in _sweep(segments,
                                        context=(_get_context()
                                                 if context is None
                                                 else context)))
 
 
-def segments_cross_or_overlap(segments: _Sequence[_Segment],
+def segments_cross_or_overlap(segments: _t.Sequence[_Segment],
                               *,
-                              context: _Optional[_Context] = None) -> bool:
+                              context: _t.Optional[_Context] = None) -> bool:
     """
     Checks if at least one pair of segments crosses or overlaps.
 
     Based on Bentley-Ottmann algorithm.
 
     Time complexity:
         ``O(len(segments) * log len(segments))``
```

