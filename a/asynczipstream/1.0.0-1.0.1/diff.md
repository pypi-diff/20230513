# Comparing `tmp/asynczipstream-1.0.0.tar.gz` & `tmp/asynczipstream-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/Users/20182177/python-zipstream-aio/dist/.tmp-yhz00fjo/asynczipstream-1.0.0.tar", last modified: Sat May 13 20:45:12 2023, max compression
+gzip compressed data, was "/Users/20182177/python-zipstream-aio/dist/.tmp-eyg5lzg2/asynczipstream-1.0.1.tar", last modified: Sat May 13 20:47:57 2023, max compression
```

## Comparing `asynczipstream-1.0.0.tar` & `asynczipstream-1.0.1.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 20182177 (193159553) 646495703        0 2023-05-13 20:45:12.021531 asynczipstream-1.0.0/
--rw-r--r--   0 20182177 (193159553) 646495703    35147 2023-05-13 18:07:28.000000 asynczipstream-1.0.0/LICENSE
--rw-r--r--   0 20182177 (193159553) 646495703     4226 2023-05-13 20:45:12.021221 asynczipstream-1.0.0/PKG-INFO
--rw-r--r--   0 20182177 (193159553) 646495703     3659 2023-05-13 20:43:34.000000 asynczipstream-1.0.0/README.md
-drwxr-xr-x   0 20182177 (193159553) 646495703        0 2023-05-13 20:45:12.018382 asynczipstream-1.0.0/asynczipstream/
--rw-r--r--   0 20182177 (193159553) 646495703    20220 2023-05-13 20:43:34.000000 asynczipstream-1.0.0/asynczipstream/__init__.py
--rw-r--r--   0 20182177 (193159553) 646495703     1220 2023-05-13 18:07:28.000000 asynczipstream-1.0.0/asynczipstream/compat.py
-drwxr-xr-x   0 20182177 (193159553) 646495703        0 2023-05-13 20:45:12.020033 asynczipstream-1.0.0/asynczipstream.egg-info/
--rw-r--r--   0 20182177 (193159553) 646495703     4226 2023-05-13 20:45:12.000000 asynczipstream-1.0.0/asynczipstream.egg-info/PKG-INFO
--rw-r--r--   0 20182177 (193159553) 646495703      315 2023-05-13 20:45:12.000000 asynczipstream-1.0.0/asynczipstream.egg-info/SOURCES.txt
--rw-r--r--   0 20182177 (193159553) 646495703        1 2023-05-13 20:45:12.000000 asynczipstream-1.0.0/asynczipstream.egg-info/dependency_links.txt
--rw-r--r--   0 20182177 (193159553) 646495703       16 2023-05-13 20:45:12.000000 asynczipstream-1.0.0/asynczipstream.egg-info/requires.txt
--rw-r--r--   0 20182177 (193159553) 646495703       15 2023-05-13 20:45:12.000000 asynczipstream-1.0.0/asynczipstream.egg-info/top_level.txt
--rw-r--r--   0 20182177 (193159553) 646495703       38 2023-05-13 20:45:12.021632 asynczipstream-1.0.0/setup.cfg
--rw-r--r--   0 20182177 (193159553) 646495703      868 2023-05-13 20:42:35.000000 asynczipstream-1.0.0/setup.py
-drwxr-xr-x   0 20182177 (193159553) 646495703        0 2023-05-13 20:45:12.020810 asynczipstream-1.0.0/tests/
--rw-r--r--   0 20182177 (193159553) 646495703     2352 2023-05-13 20:43:34.000000 asynczipstream-1.0.0/tests/test_pointerio.py
--rw-r--r--   0 20182177 (193159553) 646495703     4615 2023-05-13 20:43:34.000000 asynczipstream-1.0.0/tests/test_zipstream.py
+drwxr-xr-x   0 20182177 (193159553) 646495703        0 2023-05-13 20:47:57.816945 asynczipstream-1.0.1/
+-rw-r--r--   0 20182177 (193159553) 646495703    35147 2023-05-13 18:07:28.000000 asynczipstream-1.0.1/LICENSE
+-rw-r--r--   0 20182177 (193159553) 646495703     4227 2023-05-13 20:47:57.816608 asynczipstream-1.0.1/PKG-INFO
+-rw-r--r--   0 20182177 (193159553) 646495703     3660 2023-05-13 20:47:34.000000 asynczipstream-1.0.1/README.md
+drwxr-xr-x   0 20182177 (193159553) 646495703        0 2023-05-13 20:47:57.812527 asynczipstream-1.0.1/asynczipstream/
+-rw-r--r--   0 20182177 (193159553) 646495703    20220 2023-05-13 20:43:34.000000 asynczipstream-1.0.1/asynczipstream/__init__.py
+-rw-r--r--   0 20182177 (193159553) 646495703     1220 2023-05-13 18:07:28.000000 asynczipstream-1.0.1/asynczipstream/compat.py
+drwxr-xr-x   0 20182177 (193159553) 646495703        0 2023-05-13 20:47:57.814747 asynczipstream-1.0.1/asynczipstream.egg-info/
+-rw-r--r--   0 20182177 (193159553) 646495703     4227 2023-05-13 20:47:57.000000 asynczipstream-1.0.1/asynczipstream.egg-info/PKG-INFO
+-rw-r--r--   0 20182177 (193159553) 646495703      315 2023-05-13 20:47:57.000000 asynczipstream-1.0.1/asynczipstream.egg-info/SOURCES.txt
+-rw-r--r--   0 20182177 (193159553) 646495703        1 2023-05-13 20:47:57.000000 asynczipstream-1.0.1/asynczipstream.egg-info/dependency_links.txt
+-rw-r--r--   0 20182177 (193159553) 646495703       16 2023-05-13 20:47:57.000000 asynczipstream-1.0.1/asynczipstream.egg-info/requires.txt
+-rw-r--r--   0 20182177 (193159553) 646495703       15 2023-05-13 20:47:57.000000 asynczipstream-1.0.1/asynczipstream.egg-info/top_level.txt
+-rw-r--r--   0 20182177 (193159553) 646495703       38 2023-05-13 20:47:57.817057 asynczipstream-1.0.1/setup.cfg
+-rw-r--r--   0 20182177 (193159553) 646495703      868 2023-05-13 20:47:45.000000 asynczipstream-1.0.1/setup.py
+drwxr-xr-x   0 20182177 (193159553) 646495703        0 2023-05-13 20:47:57.815796 asynczipstream-1.0.1/tests/
+-rw-r--r--   0 20182177 (193159553) 646495703     2352 2023-05-13 20:43:34.000000 asynczipstream-1.0.1/tests/test_pointerio.py
+-rw-r--r--   0 20182177 (193159553) 646495703     4615 2023-05-13 20:43:34.000000 asynczipstream-1.0.1/tests/test_zipstream.py
```

### Comparing `asynczipstream-1.0.0/LICENSE` & `asynczipstream-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `asynczipstream-1.0.0/PKG-INFO` & `asynczipstream-1.0.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: asynczipstream
-Version: 1.0.0
+Version: 1.0.1
 Summary: Asynchronous Zipfile generator that takes input files as well as streams
 Home-page: https://github.com/lososkin/python-zipstream-aio
 Author: lososkin
 Author-email: yalososka@gmail.com
 Keywords: async zip streaming
 Classifier: Programming Language :: Python
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
@@ -88,20 +88,20 @@
 
 If the zlib module is available, asynczipstream.ZipFile can generate compressed zip
 archives.
 
 ## Installation
 
 ```
-pip install aio-zipstream
+pip install asynczipstream
 ```
 
 ## Requirements
 
-  * Python 3.5+
+  * Python 3.8+
 
 
 ### aiohttp Example
 
 ```python
 from aiohttp import web, hdrs
 import asynczipstream
```

### Comparing `asynczipstream-1.0.0/README.md` & `asynczipstream-1.0.1/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -73,20 +73,20 @@
 
 If the zlib module is available, asynczipstream.ZipFile can generate compressed zip
 archives.
 
 ## Installation
 
 ```
-pip install aio-zipstream
+pip install asynczipstream
 ```
 
 ## Requirements
 
-  * Python 3.5+
+  * Python 3.8+
 
 
 ### aiohttp Example
 
 ```python
 from aiohttp import web, hdrs
 import asynczipstream
```

### Comparing `asynczipstream-1.0.0/asynczipstream/__init__.py` & `asynczipstream-1.0.1/asynczipstream/__init__.py`

 * *Files identical despite different names*

### Comparing `asynczipstream-1.0.0/asynczipstream/compat.py` & `asynczipstream-1.0.1/asynczipstream/compat.py`

 * *Files identical despite different names*

### Comparing `asynczipstream-1.0.0/asynczipstream.egg-info/PKG-INFO` & `asynczipstream-1.0.1/asynczipstream.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: asynczipstream
-Version: 1.0.0
+Version: 1.0.1
 Summary: Asynchronous Zipfile generator that takes input files as well as streams
 Home-page: https://github.com/lososkin/python-zipstream-aio
 Author: lososkin
 Author-email: yalososka@gmail.com
 Keywords: async zip streaming
 Classifier: Programming Language :: Python
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
@@ -88,20 +88,20 @@
 
 If the zlib module is available, asynczipstream.ZipFile can generate compressed zip
 archives.
 
 ## Installation
 
 ```
-pip install aio-zipstream
+pip install asynczipstream
 ```
 
 ## Requirements
 
-  * Python 3.5+
+  * Python 3.8+
 
 
 ### aiohttp Example
 
 ```python
 from aiohttp import web, hdrs
 import asynczipstream
```

### Comparing `asynczipstream-1.0.0/setup.py` & `asynczipstream-1.0.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setup(
     name='asynczipstream',
-    version='1.0.0',
+    version='1.0.1',
     description='Asynchronous Zipfile generator that takes input files as well as streams',
     long_description=long_description,
     long_description_content_type="text/markdown",
     author='lososkin',
     author_email='yalososka@gmail.com',
     url='https://github.com/lososkin/python-zipstream-aio',
     packages=find_packages(exclude=['tests']),
```

### Comparing `asynczipstream-1.0.0/tests/test_pointerio.py` & `asynczipstream-1.0.1/tests/test_pointerio.py`

 * *Files identical despite different names*

### Comparing `asynczipstream-1.0.0/tests/test_zipstream.py` & `asynczipstream-1.0.1/tests/test_zipstream.py`

 * *Files identical despite different names*

