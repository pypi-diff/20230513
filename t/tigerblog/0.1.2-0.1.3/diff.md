# Comparing `tmp/tigerblog-0.1.2.tar.gz` & `tmp/tigerblog-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tigerblog-0.1.2.tar", last modified: Sat May 13 20:43:26 2023, max compression
+gzip compressed data, was "tigerblog-0.1.3.tar", last modified: Sat May 13 20:49:38 2023, max compression
```

## Comparing `tigerblog-0.1.2.tar` & `tigerblog-0.1.3.tar`

### file list

```diff
@@ -1,19 +1,17 @@
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:43:26.974154 tigerblog-0.1.2/
--rw-r--r--   0 user      (1000) user      (1000)    11358 2023-05-13 19:28:39.000000 tigerblog-0.1.2/LICENSE.txt
--rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:43:26.974154 tigerblog-0.1.2/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1000)      358 2023-05-13 19:37:09.000000 tigerblog-0.1.2/README.md
--rw-r--r--   0 user      (1000) user      (1000)      344 2023-05-13 20:43:26.975154 tigerblog-0.1.2/setup.cfg
--rw-r--r--   0 user      (1000) user      (1000)      981 2023-05-13 20:43:20.000000 tigerblog-0.1.2/setup.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:43:26.964154 tigerblog-0.1.2/tigerblog/
--rw-r--r--   0 user      (1000) user      (1000)      163 2023-05-13 19:36:22.000000 tigerblog-0.1.2/tigerblog/config.json
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:43:26.974154 tigerblog-0.1.2/tigerblog/themes/
--rw-r--r--   0 user      (1000) user      (1000)      163 2023-05-13 19:46:59.000000 tigerblog-0.1.2/tigerblog/themes/config.json
--rwxr-xr-x   0 user      (1000) user      (1000)    11633 2023-05-13 20:41:31.000000 tigerblog-0.1.2/tigerblog/tigerblog.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:43:26.974154 tigerblog-0.1.2/tigerblog.egg-info/
--rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1000)      342 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1000)       54 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/entry_points.txt
--rw-r--r--   0 user      (1000) user      (1000)      108 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1000)       10 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:05:19.000000 tigerblog-0.1.2/tigerblog.egg-info/zip-safe
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:49:38.393877 tigerblog-0.1.3/
+-rw-r--r--   0 user      (1000) user      (1000)    11358 2023-05-13 19:28:39.000000 tigerblog-0.1.3/LICENSE.txt
+-rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:49:38.393877 tigerblog-0.1.3/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1000)      358 2023-05-13 19:37:09.000000 tigerblog-0.1.3/README.md
+-rw-r--r--   0 user      (1000) user      (1000)      344 2023-05-13 20:49:38.393877 tigerblog-0.1.3/setup.cfg
+-rw-r--r--   0 user      (1000) user      (1000)      994 2023-05-13 20:49:25.000000 tigerblog-0.1.3/setup.py
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:49:38.392877 tigerblog-0.1.3/tigerblog/
+-rw-r--r--   0 user      (1000) user      (1000)      163 2023-05-13 19:36:22.000000 tigerblog-0.1.3/tigerblog/config.json
+-rwxr-xr-x   0 user      (1000) user      (1000)    11633 2023-05-13 20:41:31.000000 tigerblog-0.1.3/tigerblog/tigerblog.py
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:49:38.393877 tigerblog-0.1.3/tigerblog.egg-info/
+-rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:49:38.000000 tigerblog-0.1.3/tigerblog.egg-info/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1000)      313 2023-05-13 20:49:38.000000 tigerblog-0.1.3/tigerblog.egg-info/SOURCES.txt
+-rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:49:38.000000 tigerblog-0.1.3/tigerblog.egg-info/dependency_links.txt
+-rw-r--r--   0 user      (1000) user      (1000)       54 2023-05-13 20:49:38.000000 tigerblog-0.1.3/tigerblog.egg-info/entry_points.txt
+-rw-r--r--   0 user      (1000) user      (1000)      108 2023-05-13 20:49:38.000000 tigerblog-0.1.3/tigerblog.egg-info/requires.txt
+-rw-r--r--   0 user      (1000) user      (1000)       10 2023-05-13 20:49:38.000000 tigerblog-0.1.3/tigerblog.egg-info/top_level.txt
+-rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:05:19.000000 tigerblog-0.1.3/tigerblog.egg-info/zip-safe
```

### Comparing `tigerblog-0.1.2/LICENSE.txt` & `tigerblog-0.1.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `tigerblog-0.1.2/PKG-INFO` & `tigerblog-0.1.3/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tigerblog
-Version: 0.1.2
+Version: 0.1.3
 Summary: Simplest Blog Engine for Developers
 Home-page: https://github.com/tigerteamx/tigerblog
 Author: Martin F
 Author-email: pypi.org@tigerteamx.com
 Keywords: blog,productivity,bottlepy,peewee
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `tigerblog-0.1.2/setup.py` & `tigerblog-0.1.3/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -3,19 +3,19 @@
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 
 setuptools.setup(
     name="tigerblog",
     packages=["tigerblog"],
-    # package_dir=["themes/"],
+    package_dir={"tigerblog": "tigerblog"},
     package_data={
         'tigerblog': ['config.json', "themes/*"]
     },
-    version="0.1.2",
+    version="0.1.3",
     author="Martin F",
     author_email="pypi.org@tigerteamx.com",
     description="Simplest Blog Engine for Developers",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/tigerteamx/tigerblog",
     install_requires=[],  # Used for dependencies
```

### Comparing `tigerblog-0.1.2/tigerblog/tigerblog.py` & `tigerblog-0.1.3/tigerblog/tigerblog.py`

 * *Files identical despite different names*

### Comparing `tigerblog-0.1.2/tigerblog.egg-info/PKG-INFO` & `tigerblog-0.1.3/tigerblog.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tigerblog
-Version: 0.1.2
+Version: 0.1.3
 Summary: Simplest Blog Engine for Developers
 Home-page: https://github.com/tigerteamx/tigerblog
 Author: Martin F
 Author-email: pypi.org@tigerteamx.com
 Keywords: blog,productivity,bottlepy,peewee
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

