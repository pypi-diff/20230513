# Comparing `tmp/locus-8.2.0.tar.gz` & `tmp/locus-9.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "locus-8.2.0.tar", last modified: Tue Jun 14 21:37:02 2022, max compression
+gzip compressed data, was "locus-9.0.0.tar", last modified: Sat May 13 15:10:13 2023, max compression
```

## Comparing `locus-8.2.0.tar` & `locus-9.0.0.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 21:37:02.272280 locus-8.2.0/
--rw-r--r--   0 runner    (1001) docker     (121)     1069 2022-06-14 21:36:45.000000 locus-8.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       41 2022-06-14 21:36:45.000000 locus-8.2.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)     4922 2022-06-14 21:37:02.268280 locus-8.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     4101 2022-06-14 21:36:45.000000 locus-8.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 21:37:02.268280 locus-8.2.0/locus/
--rw-r--r--   0 runner    (1001) docker     (121)       66 2022-06-14 21:36:45.000000 locus-8.2.0/locus/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 21:37:02.268280 locus-8.2.0/locus/core/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-06-14 21:36:45.000000 locus-8.2.0/locus/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      586 2022-06-14 21:36:45.000000 locus-8.2.0/locus/core/box.py
--rw-r--r--   0 runner    (1001) docker     (121)     1367 2022-06-14 21:36:45.000000 locus-8.2.0/locus/core/hilbert.py
--rw-r--r--   0 runner    (1001) docker     (121)     2223 2022-06-14 21:36:45.000000 locus-8.2.0/locus/core/kd.py
--rw-r--r--   0 runner    (1001) docker     (121)     4333 2022-06-14 21:36:45.000000 locus-8.2.0/locus/core/r.py
--rw-r--r--   0 runner    (1001) docker     (121)     5360 2022-06-14 21:36:45.000000 locus-8.2.0/locus/core/segmental.py
--rw-r--r--   0 runner    (1001) docker     (121)       90 2022-06-14 21:36:45.000000 locus-8.2.0/locus/core/utils.py
--rw-r--r--   0 runner    (1001) docker     (121)    15627 2022-06-14 21:36:45.000000 locus-8.2.0/locus/kd.py
--rw-r--r--   0 runner    (1001) docker     (121)    18470 2022-06-14 21:36:45.000000 locus-8.2.0/locus/r.py
--rw-r--r--   0 runner    (1001) docker     (121)    20938 2022-06-14 21:36:45.000000 locus-8.2.0/locus/segmental.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 21:37:02.268280 locus-8.2.0/locus.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     4922 2022-06-14 21:37:01.000000 locus-8.2.0/locus.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      399 2022-06-14 21:37:02.000000 locus-8.2.0/locus.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-06-14 21:37:01.000000 locus-8.2.0/locus.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-06-14 21:37:01.000000 locus-8.2.0/locus.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)        6 2022-06-14 21:37:02.000000 locus-8.2.0/locus.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-06-14 21:36:45.000000 locus-8.2.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-06-14 21:37:02.272280 locus-8.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1279 2022-06-14 21:36:45.000000 locus-8.2.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:10:13.126985 locus-9.0.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 15:10:00.000000 locus-9.0.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 15:10:00.000000 locus-9.0.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     6260 2023-05-13 15:10:13.126985 locus-9.0.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4101 2023-05-13 15:10:00.000000 locus-9.0.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:10:13.126985 locus-9.0.0/locus/
+-rw-r--r--   0 runner    (1001) docker     (123)       66 2023-05-13 15:10:00.000000 locus-9.0.0/locus/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:10:13.126985 locus-9.0.0/locus/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:10:00.000000 locus-9.0.0/locus/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      586 2023-05-13 15:10:00.000000 locus-9.0.0/locus/core/box.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1367 2023-05-13 15:10:00.000000 locus-9.0.0/locus/core/hilbert.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2223 2023-05-13 15:10:00.000000 locus-9.0.0/locus/core/kd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4333 2023-05-13 15:10:00.000000 locus-9.0.0/locus/core/r.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5378 2023-05-13 15:10:00.000000 locus-9.0.0/locus/core/segmental.py
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 15:10:00.000000 locus-9.0.0/locus/core/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15627 2023-05-13 15:10:00.000000 locus-9.0.0/locus/kd.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18470 2023-05-13 15:10:00.000000 locus-9.0.0/locus/r.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20938 2023-05-13 15:10:00.000000 locus-9.0.0/locus/segmental.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:10:13.126985 locus-9.0.0/locus.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6260 2023-05-13 15:10:13.000000 locus-9.0.0/locus.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      397 2023-05-13 15:10:13.000000 locus-9.0.0/locus.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 15:10:13.000000 locus-9.0.0/locus.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 15:10:13.000000 locus-9.0.0/locus.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-13 15:10:13.000000 locus-9.0.0/locus.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1237 2023-05-13 15:10:00.000000 locus-9.0.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 15:10:13.126985 locus-9.0.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      280 2023-05-13 15:10:00.000000 locus-9.0.0/setup.py
```

### Comparing `locus-8.2.0/LICENSE` & `locus-9.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `locus-8.2.0/PKG-INFO` & `locus-9.0.0/README.md`

 * *Files 27% similar despite different names*

```diff
@@ -1,28 +1,7 @@
-Metadata-Version: 2.1
-Name: locus
-Version: 8.2.0
-Summary: Data structures for spatial queries.
-Home-page: https://github.com/lycantropos/locus/
-Download-URL: https://github.com/lycantropos/locus/archive/master.zip
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
 locus
 =====
 
 [![](https://github.com/lycantropos/locus/workflows/CI/badge.svg)](https://github.com/lycantropos/locus/actions/workflows/ci.yml "Github Actions")
 [![](https://readthedocs.org/projects/locus/badge/?version=latest)](https://locus.readthedocs.io/en/latest "Documentation")
 [![](https://codecov.io/gh/lycantropos/locus/branch/master/graph/badge.svg)](https://codecov.io/gh/lycantropos/locus "Codecov")
 [![](https://img.shields.io/github/license/lycantropos/locus.svg)](https://github.com/lycantropos/locus/blob/master/LICENSE "License")
```

### Comparing `locus-8.2.0/locus/core/box.py` & `locus-9.0.0/locus/core/box.py`

 * *Files identical despite different names*

### Comparing `locus-8.2.0/locus/core/hilbert.py` & `locus-9.0.0/locus/core/hilbert.py`

 * *Files identical despite different names*

### Comparing `locus-8.2.0/locus/core/kd.py` & `locus-9.0.0/locus/core/kd.py`

 * *Files identical despite different names*

### Comparing `locus-8.2.0/locus/core/r.py` & `locus-9.0.0/locus/core/r.py`

 * *Files identical despite different names*

### Comparing `locus-8.2.0/locus/core/segmental.py` & `locus-9.0.0/locus/core/segmental.py`

 * *Files 0% similar despite different names*

```diff
@@ -31,19 +31,21 @@
                  children: Optional[Sequence['Node']],
                  box_point_metric: Callable[[Box, Point], Scalar],
                  box_segment_metric: Callable[[Box, Segment], Scalar],
                  segment_point_metric: Callable[[Segment, Point], Scalar],
                  segments_metric: Callable[[Segment, Segment], Scalar]
                  ) -> None:
         self.box, self.children, self.index, self.segment = (
-            box, children, index, segment)
+            box, children, index, segment
+        )
         (self.box_point_metric, self.box_segment_metric,
          self.segment_point_metric, self.segments_metric) = (
             box_point_metric, box_segment_metric, segment_point_metric,
-            segments_metric)
+            segments_metric
+        )
 
     __repr__ = generate_repr(__init__)
 
     @property
     def is_leaf(self) -> bool:
         return self.children is None
```

### Comparing `locus-8.2.0/locus/kd.py` & `locus-9.0.0/locus/kd.py`

 * *Files identical despite different names*

### Comparing `locus-8.2.0/locus/r.py` & `locus-9.0.0/locus/r.py`

 * *Files identical despite different names*

### Comparing `locus-8.2.0/locus/segmental.py` & `locus-9.0.0/locus/segmental.py`

 * *Files identical despite different names*

