# Comparing `tmp/jinsi-0.8.0.tar.gz` & `tmp/jinsi-0.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/jinsi-0.8.0.tar", last modified: Wed Jan 27 23:10:09 2021, max compression
+gzip compressed data, was "dist/jinsi-0.9.0.tar", last modified: Thu Jan 28 05:38:29 2021, max compression
```

## Comparing `jinsi-0.8.0.tar` & `jinsi-0.9.0.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-27 23:10:09.556282 jinsi-0.8.0/
--rw-r--r--   0 scravy     (501) staff       (20)     5816 2021-01-27 23:10:09.555552 jinsi-0.8.0/PKG-INFO
--rw-r--r--   0 scravy     (501) staff       (20)     3629 2021-01-24 21:58:27.000000 jinsi-0.8.0/README.md
-drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-27 23:10:09.521171 jinsi-0.8.0/bin/
--rwxr-xr-x   0 scravy     (501) staff       (20)       60 2020-12-30 14:33:09.000000 jinsi-0.8.0/bin/jinsi
-drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-27 23:10:09.539765 jinsi-0.8.0/jinsi/
--rw-r--r--   0 scravy     (501) staff       (20)     2748 2021-01-27 22:06:37.000000 jinsi-0.8.0/jinsi/__init__.py
--rw-r--r--   0 scravy     (501) staff       (20)       62 2020-12-30 14:04:52.000000 jinsi-0.8.0/jinsi/__main__.py
--rw-r--r--   0 scravy     (501) staff       (20)       18 2021-01-27 22:47:58.000000 jinsi-0.8.0/jinsi/__pkginfo__.py
--rw-r--r--   0 scravy     (501) staff       (20)      819 2020-12-06 03:43:28.000000 jinsi-0.8.0/jinsi/environment.py
--rw-r--r--   0 scravy     (501) staff       (20)      754 2020-11-29 02:55:29.000000 jinsi-0.8.0/jinsi/exceptions.py
--rw-r--r--   0 scravy     (501) staff       (20)     3074 2021-01-24 21:58:27.000000 jinsi-0.8.0/jinsi/expressions.py
--rw-r--r--   0 scravy     (501) staff       (20)     7431 2021-01-27 22:41:45.000000 jinsi-0.8.0/jinsi/functions.py
--rw-r--r--   0 scravy     (501) staff       (20)     3661 2021-01-24 21:58:27.000000 jinsi-0.8.0/jinsi/jsonutil.py
--rw-r--r--   0 scravy     (501) staff       (20)     1935 2021-01-27 22:49:48.000000 jinsi-0.8.0/jinsi/main.py
--rw-r--r--   0 scravy     (501) staff       (20)     7279 2021-01-27 22:06:22.000000 jinsi-0.8.0/jinsi/nodes.py
--rw-r--r--   0 scravy     (501) staff       (20)     7993 2021-01-27 23:06:16.000000 jinsi-0.8.0/jinsi/parser.py
--rw-r--r--   0 scravy     (501) staff       (20)    10355 2021-01-24 21:58:27.000000 jinsi-0.8.0/jinsi/util.py
--rw-r--r--   0 scravy     (501) staff       (20)     4297 2021-01-26 22:28:18.000000 jinsi-0.8.0/jinsi/yamlutil.py
-drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-27 23:10:09.543414 jinsi-0.8.0/jinsi.egg-info/
--rw-r--r--   0 scravy     (501) staff       (20)     5816 2021-01-27 23:10:09.000000 jinsi-0.8.0/jinsi.egg-info/PKG-INFO
--rw-r--r--   0 scravy     (501) staff       (20)      554 2021-01-27 23:10:09.000000 jinsi-0.8.0/jinsi.egg-info/SOURCES.txt
--rw-r--r--   0 scravy     (501) staff       (20)        1 2021-01-27 23:10:09.000000 jinsi-0.8.0/jinsi.egg-info/dependency_links.txt
--rw-r--r--   0 scravy     (501) staff       (20)       29 2021-01-27 23:10:09.000000 jinsi-0.8.0/jinsi.egg-info/requires.txt
--rw-r--r--   0 scravy     (501) staff       (20)       12 2021-01-27 23:10:09.000000 jinsi-0.8.0/jinsi.egg-info/top_level.txt
--rw-r--r--   0 scravy     (501) staff       (20)       38 2021-01-27 23:10:09.556506 jinsi-0.8.0/setup.cfg
--rw-r--r--   0 scravy     (501) staff       (20)      938 2021-01-24 21:58:27.000000 jinsi-0.8.0/setup.py
-drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-27 23:10:09.553433 jinsi-0.8.0/tests/
--rw-r--r--   0 scravy     (501) staff       (20)       64 2021-01-19 04:10:12.000000 jinsi-0.8.0/tests/__init__.py
--rw-r--r--   0 scravy     (501) staff       (20)     2489 2021-01-18 06:01:37.000000 jinsi-0.8.0/tests/test_examples.py
--rw-r--r--   0 scravy     (501) staff       (20)     1274 2021-01-27 22:17:44.000000 jinsi-0.8.0/tests/test_functions.py
--rw-r--r--   0 scravy     (501) staff       (20)      391 2021-01-19 11:41:17.000000 jinsi-0.8.0/tests/test_jsonutil.py
--rw-r--r--   0 scravy     (501) staff       (20)     1224 2021-01-27 23:05:13.000000 jinsi-0.8.0/tests/test_load.py
--rw-r--r--   0 scravy     (501) staff       (20)      238 2021-01-24 21:58:27.000000 jinsi-0.8.0/tests/test_util.py
--rw-r--r--   0 scravy     (501) staff       (20)      305 2021-01-26 22:28:34.000000 jinsi-0.8.0/tests/test_yamlutil.py
+drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-28 05:38:29.715472 jinsi-0.9.0/
+-rw-r--r--   0 scravy     (501) staff       (20)     5816 2021-01-28 05:38:29.714927 jinsi-0.9.0/PKG-INFO
+-rw-r--r--   0 scravy     (501) staff       (20)     3629 2021-01-24 21:58:27.000000 jinsi-0.9.0/README.md
+drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-28 05:38:29.672617 jinsi-0.9.0/bin/
+-rwxr-xr-x   0 scravy     (501) staff       (20)       60 2020-12-30 14:33:09.000000 jinsi-0.9.0/bin/jinsi
+drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-28 05:38:29.691988 jinsi-0.9.0/jinsi/
+-rw-r--r--   0 scravy     (501) staff       (20)     2748 2021-01-27 22:06:37.000000 jinsi-0.9.0/jinsi/__init__.py
+-rw-r--r--   0 scravy     (501) staff       (20)       62 2020-12-30 14:04:52.000000 jinsi-0.9.0/jinsi/__main__.py
+-rw-r--r--   0 scravy     (501) staff       (20)       18 2021-01-28 05:33:45.000000 jinsi-0.9.0/jinsi/__pkginfo__.py
+-rw-r--r--   0 scravy     (501) staff       (20)      819 2020-12-06 03:43:28.000000 jinsi-0.9.0/jinsi/environment.py
+-rw-r--r--   0 scravy     (501) staff       (20)      754 2020-11-29 02:55:29.000000 jinsi-0.9.0/jinsi/exceptions.py
+-rw-r--r--   0 scravy     (501) staff       (20)     3074 2021-01-24 21:58:27.000000 jinsi-0.9.0/jinsi/expressions.py
+-rw-r--r--   0 scravy     (501) staff       (20)     7525 2021-01-28 05:37:26.000000 jinsi-0.9.0/jinsi/functions.py
+-rw-r--r--   0 scravy     (501) staff       (20)     3705 2021-01-28 05:35:47.000000 jinsi-0.9.0/jinsi/jsonutil.py
+-rw-r--r--   0 scravy     (501) staff       (20)     1935 2021-01-27 22:49:48.000000 jinsi-0.9.0/jinsi/main.py
+-rw-r--r--   0 scravy     (501) staff       (20)     7279 2021-01-27 22:06:22.000000 jinsi-0.9.0/jinsi/nodes.py
+-rw-r--r--   0 scravy     (501) staff       (20)     7993 2021-01-27 23:06:16.000000 jinsi-0.9.0/jinsi/parser.py
+-rw-r--r--   0 scravy     (501) staff       (20)    10355 2021-01-24 21:58:27.000000 jinsi-0.9.0/jinsi/util.py
+-rw-r--r--   0 scravy     (501) staff       (20)     4297 2021-01-26 22:28:18.000000 jinsi-0.9.0/jinsi/yamlutil.py
+drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-28 05:38:29.702296 jinsi-0.9.0/jinsi.egg-info/
+-rw-r--r--   0 scravy     (501) staff       (20)     5816 2021-01-28 05:38:29.000000 jinsi-0.9.0/jinsi.egg-info/PKG-INFO
+-rw-r--r--   0 scravy     (501) staff       (20)      554 2021-01-28 05:38:29.000000 jinsi-0.9.0/jinsi.egg-info/SOURCES.txt
+-rw-r--r--   0 scravy     (501) staff       (20)        1 2021-01-28 05:38:29.000000 jinsi-0.9.0/jinsi.egg-info/dependency_links.txt
+-rw-r--r--   0 scravy     (501) staff       (20)       29 2021-01-28 05:38:29.000000 jinsi-0.9.0/jinsi.egg-info/requires.txt
+-rw-r--r--   0 scravy     (501) staff       (20)       12 2021-01-28 05:38:29.000000 jinsi-0.9.0/jinsi.egg-info/top_level.txt
+-rw-r--r--   0 scravy     (501) staff       (20)       38 2021-01-28 05:38:29.715635 jinsi-0.9.0/setup.cfg
+-rw-r--r--   0 scravy     (501) staff       (20)      938 2021-01-24 21:58:27.000000 jinsi-0.9.0/setup.py
+drwxr-xr-x   0 scravy     (501) staff       (20)        0 2021-01-28 05:38:29.712468 jinsi-0.9.0/tests/
+-rw-r--r--   0 scravy     (501) staff       (20)       64 2021-01-19 04:10:12.000000 jinsi-0.9.0/tests/__init__.py
+-rw-r--r--   0 scravy     (501) staff       (20)     2489 2021-01-18 06:01:37.000000 jinsi-0.9.0/tests/test_examples.py
+-rw-r--r--   0 scravy     (501) staff       (20)     1274 2021-01-27 22:17:44.000000 jinsi-0.9.0/tests/test_functions.py
+-rw-r--r--   0 scravy     (501) staff       (20)      391 2021-01-19 11:41:17.000000 jinsi-0.9.0/tests/test_jsonutil.py
+-rw-r--r--   0 scravy     (501) staff       (20)     1224 2021-01-27 23:05:13.000000 jinsi-0.9.0/tests/test_load.py
+-rw-r--r--   0 scravy     (501) staff       (20)      238 2021-01-24 21:58:27.000000 jinsi-0.9.0/tests/test_util.py
+-rw-r--r--   0 scravy     (501) staff       (20)      305 2021-01-26 22:28:34.000000 jinsi-0.9.0/tests/test_yamlutil.py
```

### Comparing `jinsi-0.8.0/PKG-INFO` & `jinsi-0.9.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jinsi
-Version: 0.8.0
+Version: 0.9.0
 Summary: JSON/YAML homoiconic templating language
 Home-page: https://github.com/scravy/jinsi
 Author: Julian Fleischer
 Author-email: tirednesscankill@warhog.net
 License: UNKNOWN
 Description: # JSON/YAML homoiconic templating language
```

### Comparing `jinsi-0.8.0/README.md` & `jinsi-0.9.0/README.md`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/__init__.py` & `jinsi-0.9.0/jinsi/__init__.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/environment.py` & `jinsi-0.9.0/jinsi/environment.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/exceptions.py` & `jinsi-0.9.0/jinsi/exceptions.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/expressions.py` & `jinsi-0.9.0/jinsi/expressions.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/functions.py` & `jinsi-0.9.0/jinsi/functions.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import hashlib
 
 from dezimal import Dezimal
 
-from . import dumpjson
+from .jsonutil import dumpjson, loadjson
 from .util import parse_name, empty
 
 
 class Functions:
 
     @staticmethod
     def range_inclusive(from_, to):
@@ -176,14 +176,18 @@
             return value
         return [value]
 
     @staticmethod
     def json_serialize(value):
         return dumpjson(value)
 
+    @staticmethod
+    def json_read(value):
+        return loadjson(value)
+
     # aggregation
 
     @staticmethod
     def sum(*args):
         result = Dezimal(0)
         for arg in args:
             result += Dezimal(arg)
```

### Comparing `jinsi-0.8.0/jinsi/jsonutil.py` & `jinsi-0.9.0/jinsi/jsonutil.py`

 * *Files 5% similar despite different names*

```diff
@@ -130,7 +130,11 @@
                     yield from _iterencode(encode_other(o))
 
     return _iterencode
 
 
 def dumpjson(obj, **kwargs) -> str:
     return json.dumps(obj, cls=Encoder, **kwargs)
+
+
+def loadjson(s):
+    return json.loads(s)
```

### Comparing `jinsi-0.8.0/jinsi/main.py` & `jinsi-0.9.0/jinsi/main.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/nodes.py` & `jinsi-0.9.0/jinsi/nodes.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/parser.py` & `jinsi-0.9.0/jinsi/parser.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/util.py` & `jinsi-0.9.0/jinsi/util.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi/yamlutil.py` & `jinsi-0.9.0/jinsi/yamlutil.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/jinsi.egg-info/PKG-INFO` & `jinsi-0.9.0/jinsi.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jinsi
-Version: 0.8.0
+Version: 0.9.0
 Summary: JSON/YAML homoiconic templating language
 Home-page: https://github.com/scravy/jinsi
 Author: Julian Fleischer
 Author-email: tirednesscankill@warhog.net
 License: UNKNOWN
 Description: # JSON/YAML homoiconic templating language
```

### Comparing `jinsi-0.8.0/jinsi.egg-info/SOURCES.txt` & `jinsi-0.9.0/jinsi.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/setup.py` & `jinsi-0.9.0/setup.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/tests/test_examples.py` & `jinsi-0.9.0/tests/test_examples.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/tests/test_functions.py` & `jinsi-0.9.0/tests/test_functions.py`

 * *Files identical despite different names*

### Comparing `jinsi-0.8.0/tests/test_load.py` & `jinsi-0.9.0/tests/test_load.py`

 * *Files identical despite different names*

