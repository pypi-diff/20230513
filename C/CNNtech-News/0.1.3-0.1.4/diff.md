# Comparing `tmp/CNNtech_News-0.1.3.tar.gz` & `tmp/CNNtech_News-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "CNNtech_News-0.1.3.tar", last modified: Tue May  9 09:28:32 2023, max compression
+gzip compressed data, was "CNNtech_News-0.1.4.tar", last modified: Sat May 13 13:23:48 2023, max compression
```

## Comparing `CNNtech_News-0.1.3.tar` & `CNNtech_News-0.1.4.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 hasanrachmatullah   (501) staff       (20)        0 2023-05-09 09:28:32.938093 CNNtech_News-0.1.3/
-drwxr-xr-x   0 hasanrachmatullah   (501) staff       (20)        0 2023-05-09 09:28:32.936453 CNNtech_News-0.1.3/CNNtech_News.egg-info/
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)     1152 2023-05-09 09:28:32.000000 CNNtech_News-0.1.3/CNNtech_News.egg-info/PKG-INFO
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)      197 2023-05-09 09:28:32.000000 CNNtech_News-0.1.3/CNNtech_News.egg-info/SOURCES.txt
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)        1 2023-05-09 09:28:32.000000 CNNtech_News-0.1.3/CNNtech_News.egg-info/dependency_links.txt
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)       15 2023-05-09 09:28:32.000000 CNNtech_News-0.1.3/CNNtech_News.egg-info/top_level.txt
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)    35149 2023-05-08 23:18:31.000000 CNNtech_News-0.1.3/LICENSE
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)     1152 2023-05-09 09:28:32.937788 CNNtech_News-0.1.3/PKG-INFO
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)      548 2023-05-09 09:27:09.000000 CNNtech_News-0.1.3/README.md
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)       38 2023-05-09 09:28:32.938185 CNNtech_News-0.1.3/setup.cfg
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)      984 2023-05-09 09:28:08.000000 CNNtech_News-0.1.3/setup.py
-drwxr-xr-x   0 hasanrachmatullah   (501) staff       (20)        0 2023-05-09 09:28:32.936908 CNNtech_News-0.1.3/updateTechnews/
--rw-r--r--   0 hasanrachmatullah   (501) staff       (20)     2262 2023-05-08 23:51:22.000000 CNNtech_News-0.1.3/updateTechnews/__init__.py
+drwxr-xr-x   0 hasanrachmatullah   (501) staff       (20)        0 2023-05-13 13:23:48.494399 CNNtech_News-0.1.4/
+drwxr-xr-x   0 hasanrachmatullah   (501) staff       (20)        0 2023-05-13 13:23:48.493103 CNNtech_News-0.1.4/CNNtech_News.egg-info/
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)     1152 2023-05-13 13:23:48.000000 CNNtech_News-0.1.4/CNNtech_News.egg-info/PKG-INFO
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)      197 2023-05-13 13:23:48.000000 CNNtech_News-0.1.4/CNNtech_News.egg-info/SOURCES.txt
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)        1 2023-05-13 13:23:48.000000 CNNtech_News-0.1.4/CNNtech_News.egg-info/dependency_links.txt
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)       15 2023-05-13 13:23:48.000000 CNNtech_News-0.1.4/CNNtech_News.egg-info/top_level.txt
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)    35149 2023-05-08 23:18:31.000000 CNNtech_News-0.1.4/LICENSE
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)     1152 2023-05-13 13:23:48.494062 CNNtech_News-0.1.4/PKG-INFO
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)      548 2023-05-09 09:27:09.000000 CNNtech_News-0.1.4/README.md
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)       38 2023-05-13 13:23:48.494480 CNNtech_News-0.1.4/setup.cfg
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)      984 2023-05-13 13:22:51.000000 CNNtech_News-0.1.4/setup.py
+drwxr-xr-x   0 hasanrachmatullah   (501) staff       (20)        0 2023-05-13 13:23:48.493495 CNNtech_News-0.1.4/updateTechnews/
+-rw-r--r--   0 hasanrachmatullah   (501) staff       (20)     2262 2023-05-08 23:51:22.000000 CNNtech_News-0.1.4/updateTechnews/__init__.py
```

### Comparing `CNNtech_News-0.1.3/CNNtech_News.egg-info/PKG-INFO` & `CNNtech_News-0.1.4/CNNtech_News.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: CNNtech-News
-Version: 0.1.3
+Version: 0.1.4
 Summary: This package will provide you the most update of CNN Tech News
 Home-page: https://github.com/ganirh0612/CNNtech_News
 Author: Hasan Gani Rachmatullah
 Author-email: ganirh0612@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 2 - Pre-Alpha
```

### Comparing `CNNtech_News-0.1.3/LICENSE` & `CNNtech_News-0.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `CNNtech_News-0.1.3/PKG-INFO` & `CNNtech_News-0.1.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: CNNtech_News
-Version: 0.1.3
+Version: 0.1.4
 Summary: This package will provide you the most update of CNN Tech News
 Home-page: https://github.com/ganirh0612/CNNtech_News
 Author: Hasan Gani Rachmatullah
 Author-email: ganirh0612@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 2 - Pre-Alpha
```

### Comparing `CNNtech_News-0.1.3/README.md` & `CNNtech_News-0.1.4/README.md`

 * *Files identical despite different names*

### Comparing `CNNtech_News-0.1.3/setup.py` & `CNNtech_News-0.1.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="CNNtech_News",
-    version="0.1.3",
+    version="0.1.4",
     author="Hasan Gani Rachmatullah",
     author_email="ganirh0612@gmail.com",
     description="This package will provide you the most update of CNN Tech News",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/ganirh0612/CNNtech_News",
     project_urls={
```

### Comparing `CNNtech_News-0.1.3/updateTechnews/__init__.py` & `CNNtech_News-0.1.4/updateTechnews/__init__.py`

 * *Files identical despite different names*

