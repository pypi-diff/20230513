# Comparing `tmp/realtouch-0.1.1.tar.gz` & `tmp/realtouch-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "realtouch-0.1.1.tar", last modified: Sat May 13 00:43:57 2023, max compression
+gzip compressed data, was "realtouch-0.1.2.tar", last modified: Sat May 13 02:52:01 2023, max compression
```

## Comparing `realtouch-0.1.1.tar` & `realtouch-0.1.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 k          (501) staff       (20)        0 2023-05-13 00:43:57.773179 realtouch-0.1.1/
--rw-r--r--   0 k          (501) staff       (20)    35148 2023-05-12 00:09:36.000000 realtouch-0.1.1/LICENSE
--rw-r--r--   0 k          (501) staff       (20)      539 2023-05-13 00:43:57.772804 realtouch-0.1.1/PKG-INFO
-drwxr-xr-x   0 k          (501) staff       (20)        0 2023-05-13 00:43:57.767857 realtouch-0.1.1/realtouch/
-drwxr-xr-x   0 k          (501) staff       (20)        0 2023-05-13 00:43:57.769805 realtouch-0.1.1/realtouch/src/
-drwxr-xr-x   0 k          (501) staff       (20)        0 2023-05-13 00:43:57.772149 realtouch-0.1.1/realtouch/src/realtouch.egg-info/
--rw-r--r--   0 k          (501) staff       (20)      539 2023-05-13 00:43:57.000000 realtouch-0.1.1/realtouch/src/realtouch.egg-info/PKG-INFO
--rw-r--r--   0 k          (501) staff       (20)      277 2023-05-13 00:43:57.000000 realtouch-0.1.1/realtouch/src/realtouch.egg-info/SOURCES.txt
--rw-r--r--   0 k          (501) staff       (20)        1 2023-05-13 00:43:57.000000 realtouch-0.1.1/realtouch/src/realtouch.egg-info/dependency_links.txt
--rw-r--r--   0 k          (501) staff       (20)       16 2023-05-13 00:43:57.000000 realtouch-0.1.1/realtouch/src/realtouch.egg-info/requires.txt
--rw-r--r--   0 k          (501) staff       (20)       10 2023-05-13 00:43:57.000000 realtouch-0.1.1/realtouch/src/realtouch.egg-info/top_level.txt
--rw-r--r--   0 k          (501) staff       (20)    18378 2023-05-13 00:43:28.000000 realtouch-0.1.1/realtouch/src/realtouch.py
--rw-r--r--   0 k          (501) staff       (20)       38 2023-05-13 00:43:57.773304 realtouch-0.1.1/setup.cfg
--rw-r--r--   0 k          (501) staff       (20)      852 2023-05-12 06:54:36.000000 realtouch-0.1.1/setup.py
+drwxr-xr-x   0 k          (501) staff       (20)        0 2023-05-13 02:52:01.077028 realtouch-0.1.2/
+-rw-r--r--   0 k          (501) staff       (20)    35148 2023-05-12 00:09:36.000000 realtouch-0.1.2/LICENSE
+-rw-r--r--   0 k          (501) staff       (20)      539 2023-05-13 02:52:01.076574 realtouch-0.1.2/PKG-INFO
+drwxr-xr-x   0 k          (501) staff       (20)        0 2023-05-13 02:52:01.069774 realtouch-0.1.2/realtouch/
+drwxr-xr-x   0 k          (501) staff       (20)        0 2023-05-13 02:52:01.072533 realtouch-0.1.2/realtouch/src/
+drwxr-xr-x   0 k          (501) staff       (20)        0 2023-05-13 02:52:01.075765 realtouch-0.1.2/realtouch/src/realtouch.egg-info/
+-rw-r--r--   0 k          (501) staff       (20)      539 2023-05-13 02:52:00.000000 realtouch-0.1.2/realtouch/src/realtouch.egg-info/PKG-INFO
+-rw-r--r--   0 k          (501) staff       (20)      277 2023-05-13 02:52:01.000000 realtouch-0.1.2/realtouch/src/realtouch.egg-info/SOURCES.txt
+-rw-r--r--   0 k          (501) staff       (20)        1 2023-05-13 02:52:00.000000 realtouch-0.1.2/realtouch/src/realtouch.egg-info/dependency_links.txt
+-rw-r--r--   0 k          (501) staff       (20)       16 2023-05-13 02:52:00.000000 realtouch-0.1.2/realtouch/src/realtouch.egg-info/requires.txt
+-rw-r--r--   0 k          (501) staff       (20)       10 2023-05-13 02:52:00.000000 realtouch-0.1.2/realtouch/src/realtouch.egg-info/top_level.txt
+-rw-r--r--   0 k          (501) staff       (20)    18488 2023-05-13 01:54:08.000000 realtouch-0.1.2/realtouch/src/realtouch.py
+-rw-r--r--   0 k          (501) staff       (20)       38 2023-05-13 02:52:01.077193 realtouch-0.1.2/setup.cfg
+-rw-r--r--   0 k          (501) staff       (20)      852 2023-05-13 02:51:32.000000 realtouch-0.1.2/setup.py
```

### Comparing `realtouch-0.1.1/LICENSE` & `realtouch-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `realtouch-0.1.1/PKG-INFO` & `realtouch-0.1.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: realtouch
-Version: 0.1.1
+Version: 0.1.2
 Summary: realTouch Robot SDK
 Home-page: https://realtouch.dev
 Author: realTouch Dev
 Author-email: contact@realtouch.dev
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
```

### Comparing `realtouch-0.1.1/realtouch/src/realtouch.egg-info/PKG-INFO` & `realtouch-0.1.2/realtouch/src/realtouch.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: realtouch
-Version: 0.1.1
+Version: 0.1.2
 Summary: realTouch Robot SDK
 Home-page: https://realtouch.dev
 Author: realTouch Dev
 Author-email: contact@realtouch.dev
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
```

### Comparing `realtouch-0.1.1/realtouch/src/realtouch.py` & `realtouch-0.1.2/realtouch/src/realtouch.py`

 * *Files 0% similar despite different names*

```diff
@@ -379,14 +379,18 @@
         :return:
         """
         return self.phone.robot.call_func(
             self.phone.position,
             'screen/clear_folder', folder=folder
         )
 
+    def clear_midea(self):
+        for folder in ['DCIM', 'Pictures']:
+            self.clear_folder(folder)
+
 
 class Phone:
     def __init__(
             self,
             position: int,
             robot: Robot,
             data: dict
```

### Comparing `realtouch-0.1.1/setup.py` & `realtouch-0.1.2/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="realtouch",
-    version="0.1.1",
+    version="0.1.2",
     author="realTouch Dev",
     author_email="contact@realtouch.dev",
     description="realTouch Robot SDK",
     long_description="realTouch Robot SDK",
     long_description_content_type="text/markdown",
     url="https://realtouch.dev",
     packages=find_packages(),
```

