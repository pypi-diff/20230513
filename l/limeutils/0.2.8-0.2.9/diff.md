# Comparing `tmp/limeutils-0.2.8.tar.gz` & `tmp/limeutils-0.2.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "limeutils-0.2.8.tar", last modified: Tue Mar  8 16:34:03 2022, max compression
+gzip compressed data, was "limeutils-0.2.9.tar", last modified: Tue May 10 03:03:22 2022, max compression
```

## Comparing `limeutils-0.2.8.tar` & `limeutils-0.2.9.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-03-08 16:34:03.308777 limeutils-0.2.8/
--rw-r--r--   0 enchance  (1000) enchance  (1000)     1065 2021-01-04 07:10:32.000000 limeutils-0.2.8/LICENSE
--rw-rw-r--   0 enchance  (1000) enchance  (1000)     1425 2022-03-08 16:34:03.308777 limeutils-0.2.8/PKG-INFO
--rw-rw-r--   0 enchance  (1000) enchance  (1000)      873 2021-06-03 03:00:33.000000 limeutils-0.2.8/README.md
-drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-03-08 16:34:03.304777 limeutils-0.2.8/limeutils/
--rw-rw-r--   0 enchance  (1000) enchance  (1000)      137 2022-03-08 16:31:05.000000 limeutils-0.2.8/limeutils/__init__.py
--rw-r--r--   0 enchance  (1000) enchance  (1000)     1065 2021-04-11 12:21:56.000000 limeutils-0.2.8/limeutils/db.py
--rw-r--r--   0 enchance  (1000) enchance  (1000)      542 2021-04-11 12:21:56.000000 limeutils-0.2.8/limeutils/exceptions.py
-drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-03-08 16:34:03.308777 limeutils-0.2.8/limeutils/redis/
--rw-r--r--   0 enchance  (1000) enchance  (1000)        0 2021-04-11 12:21:56.000000 limeutils-0.2.8/limeutils/redis/__init__.py
--rw-r--r--   0 enchance  (1000) enchance  (1000)     2467 2021-04-11 12:21:56.000000 limeutils-0.2.8/limeutils/redis/models.py
--rw-rw-r--   0 enchance  (1000) enchance  (1000)     6860 2022-03-08 13:54:30.000000 limeutils-0.2.8/limeutils/redis/red.py
-drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-03-08 16:34:03.308777 limeutils-0.2.8/limeutils/tests/
--rw-r--r--   0 enchance  (1000) enchance  (1000)        0 2021-04-11 12:21:56.000000 limeutils-0.2.8/limeutils/tests/__init__.py
--rw-rw-r--   0 enchance  (1000) enchance  (1000)     1377 2021-06-03 03:00:33.000000 limeutils-0.2.8/limeutils/tests/conftest.py
--rw-rw-r--   0 enchance  (1000) enchance  (1000)     4694 2021-06-03 03:00:33.000000 limeutils-0.2.8/limeutils/tests/redis_test.py
--rw-rw-r--   0 enchance  (1000) enchance  (1000)     4557 2022-03-08 15:56:25.000000 limeutils-0.2.8/limeutils/tests/utils_test.py
--rw-rw-r--   0 enchance  (1000) enchance  (1000)     8449 2022-03-08 15:56:19.000000 limeutils-0.2.8/limeutils/utils.py
-drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-03-08 16:34:03.304777 limeutils-0.2.8/limeutils.egg-info/
--rw-r--r--   0 enchance  (1000) enchance  (1000)     1425 2022-03-08 16:34:03.000000 limeutils-0.2.8/limeutils.egg-info/PKG-INFO
--rw-r--r--   0 enchance  (1000) enchance  (1000)      464 2022-03-08 16:34:03.000000 limeutils-0.2.8/limeutils.egg-info/SOURCES.txt
--rw-r--r--   0 enchance  (1000) enchance  (1000)        1 2022-03-08 16:34:03.000000 limeutils-0.2.8/limeutils.egg-info/dependency_links.txt
--rw-r--r--   0 enchance  (1000) enchance  (1000)       15 2022-03-08 16:34:03.000000 limeutils-0.2.8/limeutils.egg-info/requires.txt
--rw-r--r--   0 enchance  (1000) enchance  (1000)       10 2022-03-08 16:34:03.000000 limeutils-0.2.8/limeutils.egg-info/top_level.txt
--rw-rw-r--   0 enchance  (1000) enchance  (1000)       38 2022-03-08 16:34:03.308777 limeutils-0.2.8/setup.cfg
--rw-rw-r--   0 enchance  (1000) enchance  (1000)      844 2022-03-08 16:30:57.000000 limeutils-0.2.8/setup.py
+drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-05-10 03:03:22.843634 limeutils-0.2.9/
+-rw-r--r--   0 enchance  (1000) enchance  (1000)     1065 2021-01-04 07:10:32.000000 limeutils-0.2.9/LICENSE
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)     1425 2022-05-10 03:03:22.843634 limeutils-0.2.9/PKG-INFO
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)      873 2022-05-10 02:58:26.000000 limeutils-0.2.9/README.md
+drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-05-10 03:03:22.839634 limeutils-0.2.9/limeutils/
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)      137 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/__init__.py
+-rw-r--r--   0 enchance  (1000) enchance  (1000)     1065 2021-04-11 12:21:56.000000 limeutils-0.2.9/limeutils/db.py
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)      542 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/exceptions.py
+drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-05-10 03:03:22.839634 limeutils-0.2.9/limeutils/redis/
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)        0 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/redis/__init__.py
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)     2467 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/redis/models.py
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)     6860 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/redis/red.py
+drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-05-10 03:03:22.843634 limeutils-0.2.9/limeutils/tests/
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)        0 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/tests/__init__.py
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)     1377 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/tests/conftest.py
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)     4694 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/tests/redis_test.py
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)     4557 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/tests/utils_test.py
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)     8478 2022-05-10 02:58:26.000000 limeutils-0.2.9/limeutils/utils.py
+drwxrwxr-x   0 enchance  (1000) enchance  (1000)        0 2022-05-10 03:03:22.839634 limeutils-0.2.9/limeutils.egg-info/
+-rw-r--r--   0 enchance  (1000) enchance  (1000)     1425 2022-05-10 03:03:21.000000 limeutils-0.2.9/limeutils.egg-info/PKG-INFO
+-rw-r--r--   0 enchance  (1000) enchance  (1000)      464 2022-05-10 03:03:22.000000 limeutils-0.2.9/limeutils.egg-info/SOURCES.txt
+-rw-r--r--   0 enchance  (1000) enchance  (1000)        1 2022-05-10 03:03:21.000000 limeutils-0.2.9/limeutils.egg-info/dependency_links.txt
+-rw-r--r--   0 enchance  (1000) enchance  (1000)       15 2022-05-10 03:03:22.000000 limeutils-0.2.9/limeutils.egg-info/requires.txt
+-rw-r--r--   0 enchance  (1000) enchance  (1000)       10 2022-05-10 03:03:22.000000 limeutils-0.2.9/limeutils.egg-info/top_level.txt
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)       38 2022-05-10 03:03:22.843634 limeutils-0.2.9/setup.cfg
+-rw-rw-r--   0 enchance  (1000) enchance  (1000)      844 2022-05-10 02:58:26.000000 limeutils-0.2.9/setup.py
```

### Comparing `limeutils-0.2.8/LICENSE` & `limeutils-0.2.9/LICENSE`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/PKG-INFO` & `limeutils-0.2.9/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: limeutils
-Version: 0.2.8
+Version: 0.2.9
 Summary: Utility functions for python. Functions were made and tested in FastAPI but are suitable for any python project.
 Home-page: https://github.com/dropkickdev/limeutils.git
 Author: dropickdev
 Author-email: enchance@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `limeutils-0.2.8/README.md` & `limeutils-0.2.9/README.md`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/limeutils/db.py` & `limeutils-0.2.9/limeutils/db.py`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/limeutils/exceptions.py` & `limeutils-0.2.9/limeutils/exceptions.py`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/limeutils/redis/models.py` & `limeutils-0.2.9/limeutils/redis/models.py`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/limeutils/redis/red.py` & `limeutils-0.2.9/limeutils/redis/red.py`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/limeutils/tests/conftest.py` & `limeutils-0.2.9/limeutils/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/limeutils/tests/redis_test.py` & `limeutils-0.2.9/limeutils/tests/redis_test.py`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/limeutils/tests/utils_test.py` & `limeutils-0.2.9/limeutils/tests/utils_test.py`

 * *Files identical despite different names*

### Comparing `limeutils-0.2.8/limeutils/utils.py` & `limeutils-0.2.9/limeutils/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -10,18 +10,18 @@
     """
     Check if the string is a valid timezone.
     :param val: String to check
     :return:    bool
     """
     # val = val.replace(':', '').strip()
     status = val in [
-        '-1200', '-1100', '-1000', '-0930', '-0900', '-0800', '-0700', '-0600', '-0500', '-0400',
-        '-0330', '-0300', '-0200', '-0100', '+0000', '+0100', '+0200', '+0300', '+0330', '+0400',
+        '−1200', '−1100', '−1000', '−0930', '−0900', '−0800', '−0700', '−0600', '−0500', '−0400',
+        '−0330', '−0300', '−0200', '−0100', '+0000', '+0100', '+0200', '+0300', '+0330', '+0400',
         '+0430', '+0500', '+0530', '+0545', '+0600', '+0630', '+0700', '+0800', '+0845', '+0900',
-        '+0930', '+1000', '+1030', '+1100', '+1200', '+1245', '+1300', '+1400'
+        '+0930', '+1000', '+1030', '+1100', '+1200', '+1245', '+1300', '+1400',
     ]
     return status
 
 
 def isfloat(val: Union[int, float, str]):
     """
     Checks if the contents of a string is a float.
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `limeutils-0.2.8/limeutils.egg-info/PKG-INFO` & `limeutils-0.2.9/limeutils.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: limeutils
-Version: 0.2.8
+Version: 0.2.9
 Summary: Utility functions for python. Functions were made and tested in FastAPI but are suitable for any python project.
 Home-page: https://github.com/dropkickdev/limeutils.git
 Author: dropickdev
 Author-email: enchance@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `limeutils-0.2.8/setup.py` & `limeutils-0.2.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="limeutils", # Replace with your own username
-    version="0.2.8",
+    version="0.2.9",
     author="dropickdev",
     author_email="enchance@gmail.com",
     description="Utility functions for python. Functions were made and tested in FastAPI but are "
                 "suitable for any python project.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/dropkickdev/limeutils.git",
```

