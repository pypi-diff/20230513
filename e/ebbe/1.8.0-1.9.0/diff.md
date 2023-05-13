# Comparing `tmp/ebbe-1.8.0.tar.gz` & `tmp/ebbe-1.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/ebbe-1.8.0.tar", last modified: Thu Mar 24 08:20:26 2022, max compression
+gzip compressed data, was "dist/ebbe-1.9.0.tar", last modified: Fri Jul 22 15:00:47 2022, max compression
```

## Comparing `ebbe-1.8.0.tar` & `ebbe-1.9.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxrwxr-x   0 yomguithereal  (1000) yomguithereal  (1000)        0 2022-03-24 08:20:26.000000 ebbe-1.8.0/
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)      651 2022-03-24 08:20:07.000000 ebbe-1.8.0/setup.py
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)    17652 2022-03-24 08:20:26.000000 ebbe-1.8.0/PKG-INFO
-drwxrwxr-x   0 yomguithereal  (1000) yomguithereal  (1000)        0 2022-03-24 08:20:26.000000 ebbe-1.8.0/ebbe.egg-info/
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)        1 2022-03-24 08:20:26.000000 ebbe-1.8.0/ebbe.egg-info/zip-safe
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)        1 2022-03-24 08:20:26.000000 ebbe-1.8.0/ebbe.egg-info/dependency_links.txt
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)    17652 2022-03-24 08:20:26.000000 ebbe-1.8.0/ebbe.egg-info/PKG-INFO
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)        5 2022-03-24 08:20:26.000000 ebbe-1.8.0/ebbe.egg-info/top_level.txt
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)      249 2022-03-24 08:20:26.000000 ebbe-1.8.0/ebbe.egg-info/SOURCES.txt
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)    12600 2022-03-24 08:15:44.000000 ebbe-1.8.0/README.md
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)       38 2022-03-24 08:20:26.000000 ebbe-1.8.0/setup.cfg
-drwxrwxr-x   0 yomguithereal  (1000) yomguithereal  (1000)        0 2022-03-24 08:20:26.000000 ebbe-1.8.0/ebbe/
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)     5966 2022-03-23 20:15:49.000000 ebbe-1.8.0/ebbe/utils.py
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)     1000 2022-03-24 08:09:21.000000 ebbe-1.8.0/ebbe/benchmark.py
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)      685 2022-03-24 08:08:49.000000 ebbe-1.8.0/ebbe/__init__.py
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)      804 2022-03-23 20:15:49.000000 ebbe-1.8.0/ebbe/decorators.py
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)     3320 2022-03-23 20:15:49.000000 ebbe-1.8.0/ebbe/iter.py
--rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)     3262 2022-03-24 08:08:46.000000 ebbe-1.8.0/ebbe/format.py
+drwxrwxr-x   0 yomguithereal  (1000) yomguithereal  (1000)        0 2022-07-22 15:00:47.000000 ebbe-1.9.0/
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)      651 2022-07-22 14:59:41.000000 ebbe-1.9.0/setup.py
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)    18629 2022-07-22 15:00:47.000000 ebbe-1.9.0/PKG-INFO
+drwxrwxr-x   0 yomguithereal  (1000) yomguithereal  (1000)        0 2022-07-22 15:00:47.000000 ebbe-1.9.0/ebbe.egg-info/
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)        1 2022-07-22 15:00:47.000000 ebbe-1.9.0/ebbe.egg-info/zip-safe
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)        1 2022-07-22 15:00:47.000000 ebbe-1.9.0/ebbe.egg-info/dependency_links.txt
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)    18629 2022-07-22 15:00:47.000000 ebbe-1.9.0/ebbe.egg-info/PKG-INFO
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)        5 2022-07-22 15:00:47.000000 ebbe-1.9.0/ebbe.egg-info/top_level.txt
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)      249 2022-07-22 15:00:47.000000 ebbe-1.9.0/ebbe.egg-info/SOURCES.txt
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)    13305 2022-07-22 14:59:15.000000 ebbe-1.9.0/README.md
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)       38 2022-07-22 15:00:47.000000 ebbe-1.9.0/setup.cfg
+drwxrwxr-x   0 yomguithereal  (1000) yomguithereal  (1000)        0 2022-07-22 15:00:47.000000 ebbe-1.9.0/ebbe/
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)     6369 2022-07-22 14:55:25.000000 ebbe-1.9.0/ebbe/utils.py
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)     1000 2022-03-24 08:09:21.000000 ebbe-1.9.0/ebbe/benchmark.py
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)      705 2022-07-22 14:51:06.000000 ebbe-1.9.0/ebbe/__init__.py
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)      804 2022-03-23 20:15:49.000000 ebbe-1.9.0/ebbe/decorators.py
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)     3320 2022-05-17 12:35:59.000000 ebbe-1.9.0/ebbe/iter.py
+-rw-rw-r--   0 yomguithereal  (1000) yomguithereal  (1000)     3262 2022-03-24 08:08:46.000000 ebbe-1.9.0/ebbe/format.py
```

### Comparing `ebbe-1.8.0/setup.py` & `ebbe-1.9.0/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 with open("./README.md", "r") as f:
     long_description = f.read()
 
 setup(
     name="ebbe",
-    version="1.8.0",
+    version="1.9.0",
     description="A collection of iterator-related functions for python.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="http://github.com/Yomguithereal/ebbe",
     license="MIT",
     author="Guillaume Plique",
     author_email="kropotkinepiotr@gmail.com",
```

### Comparing `ebbe-1.8.0/PKG-INFO` & `ebbe-1.9.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ebbe
-Version: 1.8.0
+Version: 1.9.0
 Summary: A collection of iterator-related functions for python.
 Home-page: http://github.com/Yomguithereal/ebbe
 Author: Guillaume Plique
 Author-email: kropotkinepiotr@gmail.com
 License: MIT
 Description: [![Build Status](https://github.com/Yomguithereal/ebbe/workflows/Tests/badge.svg)](https://github.com/Yomguithereal/ebbe/actions)
         
@@ -43,14 +43,16 @@
         * [getpath](#getpath)
         * [pathgetter](#pathgetter)
         * [noop](#noop)
         * [indexed](#indexed)
         * [grouped](#grouped)
         * [partitioned](#partitioned)
         * [sorted_uniq](#sorted_uniq)
+        * [pick](#pick)
+        * [omit](#omit)
         
         *Formatting*
         
         * [and_join](#and_join)
         * [format_int](#format_int)
         * [format_time](#format_time)
         
@@ -469,14 +471,46 @@
         >>> [-1, 1, 3, 4, 5, 17]
         
         # It accepts all of `sorted` kwargs:
         sorted_uniq(numbers, reverse=True)
         >>> [17, 5, 4, 3, 1, -1]
         ```
         
+        ### pick
+        
+        Function returning the given dictionary with only the selected keys.
+        
+        ```python
+        from ebbe import pick
+        
+        # Selected keys must be an iterable:
+        pick({'a': 1, 'b': 2, 'c': 3}, ['a', 'c'])
+        >>> {'a': 1, 'c': 3}
+        
+        # If you need the function to raise of one of the picked keys is not found:
+        pick({'a': 1, 'b': 2, 'c': 3}, ['a', 'd'])
+        >>> TypeError
+        ```
+        
+        ### omit
+        
+        Function returning the given dictionary without the selected keys.
+        
+        ```python
+        from ebbe import omit
+        
+        # Selected keys must be a container:
+        omit({'a': 1, 'b': 2, 'c': 3}, ['a', 'c'])
+        >>> {'b': 2}
+        
+        # If need to select large numbers of keys, use a set:
+        omit({'a': 1, 'b': 2, 'c': 3}, {'a', 'c'})
+        >>> {'b': 2}
+        ```
+        
         ### and_join
         
         Join function able to group the last items with a custom copula such as "and".
         
         ```python
         from ebbe import and_join
```

### Comparing `ebbe-1.8.0/ebbe.egg-info/PKG-INFO` & `ebbe-1.9.0/ebbe.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ebbe
-Version: 1.8.0
+Version: 1.9.0
 Summary: A collection of iterator-related functions for python.
 Home-page: http://github.com/Yomguithereal/ebbe
 Author: Guillaume Plique
 Author-email: kropotkinepiotr@gmail.com
 License: MIT
 Description: [![Build Status](https://github.com/Yomguithereal/ebbe/workflows/Tests/badge.svg)](https://github.com/Yomguithereal/ebbe/actions)
         
@@ -43,14 +43,16 @@
         * [getpath](#getpath)
         * [pathgetter](#pathgetter)
         * [noop](#noop)
         * [indexed](#indexed)
         * [grouped](#grouped)
         * [partitioned](#partitioned)
         * [sorted_uniq](#sorted_uniq)
+        * [pick](#pick)
+        * [omit](#omit)
         
         *Formatting*
         
         * [and_join](#and_join)
         * [format_int](#format_int)
         * [format_time](#format_time)
         
@@ -469,14 +471,46 @@
         >>> [-1, 1, 3, 4, 5, 17]
         
         # It accepts all of `sorted` kwargs:
         sorted_uniq(numbers, reverse=True)
         >>> [17, 5, 4, 3, 1, -1]
         ```
         
+        ### pick
+        
+        Function returning the given dictionary with only the selected keys.
+        
+        ```python
+        from ebbe import pick
+        
+        # Selected keys must be an iterable:
+        pick({'a': 1, 'b': 2, 'c': 3}, ['a', 'c'])
+        >>> {'a': 1, 'c': 3}
+        
+        # If you need the function to raise of one of the picked keys is not found:
+        pick({'a': 1, 'b': 2, 'c': 3}, ['a', 'd'])
+        >>> TypeError
+        ```
+        
+        ### omit
+        
+        Function returning the given dictionary without the selected keys.
+        
+        ```python
+        from ebbe import omit
+        
+        # Selected keys must be a container:
+        omit({'a': 1, 'b': 2, 'c': 3}, ['a', 'c'])
+        >>> {'b': 2}
+        
+        # If need to select large numbers of keys, use a set:
+        omit({'a': 1, 'b': 2, 'c': 3}, {'a', 'c'})
+        >>> {'b': 2}
+        ```
+        
         ### and_join
         
         Join function able to group the last items with a custom copula such as "and".
         
         ```python
         from ebbe import and_join
```

### Comparing `ebbe-1.8.0/README.md` & `ebbe-1.9.0/README.md`

 * *Files 7% similar despite different names*

```diff
@@ -35,14 +35,16 @@
 * [getpath](#getpath)
 * [pathgetter](#pathgetter)
 * [noop](#noop)
 * [indexed](#indexed)
 * [grouped](#grouped)
 * [partitioned](#partitioned)
 * [sorted_uniq](#sorted_uniq)
+* [pick](#pick)
+* [omit](#omit)
 
 *Formatting*
 
 * [and_join](#and_join)
 * [format_int](#format_int)
 * [format_time](#format_time)
 
@@ -461,14 +463,46 @@
 >>> [-1, 1, 3, 4, 5, 17]
 
 # It accepts all of `sorted` kwargs:
 sorted_uniq(numbers, reverse=True)
 >>> [17, 5, 4, 3, 1, -1]
 ```
 
+### pick
+
+Function returning the given dictionary with only the selected keys.
+
+```python
+from ebbe import pick
+
+# Selected keys must be an iterable:
+pick({'a': 1, 'b': 2, 'c': 3}, ['a', 'c'])
+>>> {'a': 1, 'c': 3}
+
+# If you need the function to raise of one of the picked keys is not found:
+pick({'a': 1, 'b': 2, 'c': 3}, ['a', 'd'])
+>>> TypeError
+```
+
+### omit
+
+Function returning the given dictionary without the selected keys.
+
+```python
+from ebbe import omit
+
+# Selected keys must be a container:
+omit({'a': 1, 'b': 2, 'c': 3}, ['a', 'c'])
+>>> {'b': 2}
+
+# If need to select large numbers of keys, use a set:
+omit({'a': 1, 'b': 2, 'c': 3}, {'a', 'c'})
+>>> {'b': 2}
+```
+
 ### and_join
 
 Join function able to group the last items with a custom copula such as "and".
 
 ```python
 from ebbe import and_join
```

### Comparing `ebbe-1.8.0/ebbe/utils.py` & `ebbe-1.9.0/ebbe/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 #
 from sys import version_info
 from collections import OrderedDict
 from collections.abc import Iterable
 
 AT_LEAST_PY37 = version_info >= (3, 7)
 DEFAULT_ORDERED_DICT = dict if AT_LEAST_PY37 else OrderedDict
+NOT_FOUND = object()
 
 
 def noop(*args, **kwargs):
     pass
 
 
 def get(target, key, default=None):
@@ -243,7 +244,34 @@
 
     return groups
 
 
 def partitioned_items(iterable, factory=DEFAULT_ORDERED_DICT, container=list):
     groups = grouped_items(iterable, factory, container)
     return list(groups.values())
+
+
+def pick(d, keys, *, strict=False):
+    n = {}
+
+    for k in keys:
+        v = d.get(k, NOT_FOUND)
+
+        if v is NOT_FOUND:
+            if strict:
+                raise KeyError(k)
+            else:
+                continue
+
+        n[k] = v
+
+    return n
+
+
+def omit(d, keys):
+    n = {}
+
+    for k, v in d.items():
+        if k not in keys:
+            n[k] = v
+
+    return n
```

### Comparing `ebbe-1.8.0/ebbe/benchmark.py` & `ebbe-1.9.0/ebbe/benchmark.py`

 * *Files identical despite different names*

### Comparing `ebbe-1.8.0/ebbe/__init__.py` & `ebbe-1.9.0/ebbe/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -25,8 +25,10 @@
     pathgetter,
     sorted_uniq,
     indexed,
     grouped,
     partitioned,
     grouped_items,
     partitioned_items,
+    pick,
+    omit,
 )
```

### Comparing `ebbe-1.8.0/ebbe/decorators.py` & `ebbe-1.9.0/ebbe/decorators.py`

 * *Files identical despite different names*

### Comparing `ebbe-1.8.0/ebbe/iter.py` & `ebbe-1.9.0/ebbe/iter.py`

 * *Files identical despite different names*

### Comparing `ebbe-1.8.0/ebbe/format.py` & `ebbe-1.9.0/ebbe/format.py`

 * *Files identical despite different names*

