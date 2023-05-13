# Comparing `tmp/hypothesis_geometry-7.3.0.tar.gz` & `tmp/hypothesis_geometry-8.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hypothesis_geometry-7.3.0.tar", last modified: Wed Jun 15 04:54:54 2022, max compression
+gzip compressed data, was "hypothesis_geometry-8.0.0.tar", last modified: Sat May 13 21:43:19 2023, max compression
```

## Comparing `hypothesis_geometry-7.3.0.tar` & `hypothesis_geometry-8.0.0.tar`

### file list

```diff
@@ -1,28 +1,45 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-15 04:54:54.729540 hypothesis_geometry-7.3.0/
--rw-r--r--   0 runner    (1001) docker     (121)     1069 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       41 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)    18173 2022-06-15 04:54:54.729540 hypothesis_geometry-7.3.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)    17225 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-15 04:54:54.725540 hypothesis_geometry-7.3.0/hypothesis_geometry/
--rw-r--r--   0 runner    (1001) docker     (121)       71 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-15 04:54:54.729540 hypothesis_geometry-7.3.0/hypothesis_geometry/core/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    47545 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/base.py
--rw-r--r--   0 runner    (1001) docker     (121)      293 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/constants.py
--rw-r--r--   0 runner    (1001) docker     (121)     4807 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/contracts.py
--rw-r--r--   0 runner    (1001) docker     (121)    21703 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/factories.py
--rw-r--r--   0 runner    (1001) docker     (121)      550 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/hints.py
--rw-r--r--   0 runner    (1001) docker     (121)     4963 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/subdivisional.py
--rw-r--r--   0 runner    (1001) docker     (121)     8715 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/triangular.py
--rw-r--r--   0 runner    (1001) docker     (121)     1788 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/core/utils.py
--rw-r--r--   0 runner    (1001) docker     (121)       97 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/hints.py
--rw-r--r--   0 runner    (1001) docker     (121)    83003 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/hypothesis_geometry/planar.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-15 04:54:54.729540 hypothesis_geometry-7.3.0/hypothesis_geometry.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)    18173 2022-06-15 04:54:54.000000 hypothesis_geometry-7.3.0/hypothesis_geometry.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      693 2022-06-15 04:54:54.000000 hypothesis_geometry-7.3.0/hypothesis_geometry.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-06-15 04:54:54.000000 hypothesis_geometry-7.3.0/hypothesis_geometry.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)      150 2022-06-15 04:54:54.000000 hypothesis_geometry-7.3.0/hypothesis_geometry.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       20 2022-06-15 04:54:54.000000 hypothesis_geometry-7.3.0/hypothesis_geometry.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)      150 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-06-15 04:54:54.729540 hypothesis_geometry-7.3.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1431 2022-06-15 04:54:35.000000 hypothesis_geometry-7.3.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:43:19.945950 hypothesis_geometry-8.0.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    19426 2023-05-13 21:43:19.945950 hypothesis_geometry-8.0.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    17225 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:43:19.937950 hypothesis_geometry-8.0.0/hypothesis_geometry/
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:43:19.941950 hypothesis_geometry-8.0.0/hypothesis_geometry/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    47545 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      293 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4807 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/contracts.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21729 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/factories.py
+-rw-r--r--   0 runner    (1001) docker     (123)      550 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/hints.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4963 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/subdivisional.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8715 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/triangular.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1788 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/core/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)       97 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/hints.py
+-rw-r--r--   0 runner    (1001) docker     (123)    83003 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/hypothesis_geometry/planar.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:43:19.941950 hypothesis_geometry-8.0.0/hypothesis_geometry.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    19426 2023-05-13 21:43:19.000000 hypothesis_geometry-8.0.0/hypothesis_geometry.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1120 2023-05-13 21:43:19.000000 hypothesis_geometry-8.0.0/hypothesis_geometry.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 21:43:19.000000 hypothesis_geometry-8.0.0/hypothesis_geometry.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      181 2023-05-13 21:43:19.000000 hypothesis_geometry-8.0.0/hypothesis_geometry.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 21:43:19.000000 hypothesis_geometry-8.0.0/hypothesis_geometry.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1398 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 21:43:19.945950 hypothesis_geometry-8.0.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      294 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:43:19.945950 hypothesis_geometry-8.0.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_boxes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5368 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_concave_contours.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5081 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_contours.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5298 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_convex_contours.py
+-rw-r--r--   0 runner    (1001) docker     (123)      511 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_empty_geometries.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15109 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_mixes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7474 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_multicontours.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4205 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_multipoints.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11754 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_multipolygons.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4345 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_multisegments.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2660 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_points.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9050 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_polygons.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3781 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_rectangular_contours.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2786 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_segments.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5273 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_star_contours.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-05-13 21:43:07.000000 hypothesis_geometry-8.0.0/tests/test_triangular_contours.py
```

### Comparing `hypothesis_geometry-7.3.0/LICENSE` & `hypothesis_geometry-8.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/PKG-INFO` & `hypothesis_geometry-8.0.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,28 +1,48 @@
 Metadata-Version: 2.1
 Name: hypothesis_geometry
-Version: 7.3.0
-Summary: ``hypothesis`` strategies for geometries.
+Version: 8.0.0
 Home-page: https://github.com/lycantropos/hypothesis_geometry/
 Download-URL: https://github.com/lycantropos/hypothesis_geometry/archive/master.zip
-Author: Azat Ibrakov
-Author-email: azatibrakov@gmail.com
+Author-email: Azat Ibrakov <azatibrakov@gmail.com>
 License: MIT License
-Classifier: Framework :: Hypothesis
-Classifier: Intended Audience :: Developers
+        
+        Copyright (c) 2020 Azat Ibrakov
+        
+        Permission is hereby granted, free of charge, to any person obtaining a copy
+        of this software and associated documentation files (the "Software"), to deal
+        in the Software without restriction, including without limitation the rights
+        to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+        copies of the Software, and to permit persons to whom the Software is
+        furnished to do so, subject to the following conditions:
+        
+        The above copyright notice and this permission notice shall be included in all
+        copies or substantial portions of the Software.
+        
+        THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+        IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+        FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+        AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+        LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+        OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+        SOFTWARE.
+        
 Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
-Requires-Python: >=3.6
+Classifier: Programming Language :: Python :: Implementation :: CPython
+Classifier: Programming Language :: Python :: Implementation :: PyPy
+Requires-Python: >=3.7
 Description-Content-Type: text/markdown
+Provides-Extra: tests
 License-File: LICENSE
 
 hypothesis_geometry
 ===================
 
 [![](https://github.com/lycantropos/hypothesis_geometry/workflows/CI/badge.svg)](https://github.com/lycantropos/hypothesis_geometry/actions/workflows/ci.yml "Github Actions")
 [![](https://readthedocs.org/projects/hypothesis_geometry/badge/?version=latest)](https://hypothesis-geometry.readthedocs.io/en/latest "Documentation")
```

### Comparing `hypothesis_geometry-7.3.0/README.md` & `hypothesis_geometry-8.0.0/README.md`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry/core/base.py` & `hypothesis_geometry-8.0.0/hypothesis_geometry/core/base.py`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry/core/contracts.py` & `hypothesis_geometry-8.0.0/hypothesis_geometry/core/contracts.py`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry/core/factories.py` & `hypothesis_geometry-8.0.0/hypothesis_geometry/core/factories.py`

 * *Files 1% similar despite different names*

```diff
@@ -464,18 +464,20 @@
             - 1)
 
 
 def _is_convex_quadrilateral_diagonal(edge: QuadEdge) -> bool:
     return (edge.right_from_start.orientation_of(edge.end)
             is Orientation.COUNTERCLOCKWISE
             is edge.right_from_end.opposite.orientation_of(
-                    edge.left_from_start.end)
+                    edge.left_from_start.end
+            )
             is edge.left_from_end.orientation_of(edge.start)
             is edge.left_from_start.opposite.orientation_of(
-                    edge.right_from_start.end))
+                    edge.right_from_start.end
+            ))
 
 
 def _is_ear(edge: QuadEdge) -> bool:
     return ((edge.orientation_of(edge.right_from_end.end)
              is Orientation.COUNTERCLOCKWISE)
             and _is_convex_quadrilateral_diagonal(
                     edge.left_from_start
```

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry/core/hints.py` & `hypothesis_geometry-8.0.0/hypothesis_geometry/core/hints.py`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry/core/subdivisional.py` & `hypothesis_geometry-8.0.0/hypothesis_geometry/core/subdivisional.py`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry/core/triangular.py` & `hypothesis_geometry-8.0.0/hypothesis_geometry/core/triangular.py`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry/core/utils.py` & `hypothesis_geometry-8.0.0/hypothesis_geometry/core/utils.py`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry/planar.py` & `hypothesis_geometry-8.0.0/hypothesis_geometry/planar.py`

 * *Files identical despite different names*

### Comparing `hypothesis_geometry-7.3.0/hypothesis_geometry.egg-info/PKG-INFO` & `hypothesis_geometry-8.0.0/hypothesis_geometry.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,28 +1,48 @@
 Metadata-Version: 2.1
 Name: hypothesis-geometry
-Version: 7.3.0
-Summary: ``hypothesis`` strategies for geometries.
+Version: 8.0.0
 Home-page: https://github.com/lycantropos/hypothesis_geometry/
 Download-URL: https://github.com/lycantropos/hypothesis_geometry/archive/master.zip
-Author: Azat Ibrakov
-Author-email: azatibrakov@gmail.com
+Author-email: Azat Ibrakov <azatibrakov@gmail.com>
 License: MIT License
-Classifier: Framework :: Hypothesis
-Classifier: Intended Audience :: Developers
+        
+        Copyright (c) 2020 Azat Ibrakov
+        
+        Permission is hereby granted, free of charge, to any person obtaining a copy
+        of this software and associated documentation files (the "Software"), to deal
+        in the Software without restriction, including without limitation the rights
+        to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+        copies of the Software, and to permit persons to whom the Software is
+        furnished to do so, subject to the following conditions:
+        
+        The above copyright notice and this permission notice shall be included in all
+        copies or substantial portions of the Software.
+        
+        THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+        IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+        FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+        AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+        LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+        OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+        SOFTWARE.
+        
 Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
-Requires-Python: >=3.6
+Classifier: Programming Language :: Python :: Implementation :: CPython
+Classifier: Programming Language :: Python :: Implementation :: PyPy
+Requires-Python: >=3.7
 Description-Content-Type: text/markdown
+Provides-Extra: tests
 License-File: LICENSE
 
 hypothesis_geometry
 ===================
 
 [![](https://github.com/lycantropos/hypothesis_geometry/workflows/CI/badge.svg)](https://github.com/lycantropos/hypothesis_geometry/actions/workflows/ci.yml "Github Actions")
 [![](https://readthedocs.org/projects/hypothesis_geometry/badge/?version=latest)](https://hypothesis-geometry.readthedocs.io/en/latest "Documentation")
```

