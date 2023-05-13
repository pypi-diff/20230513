# Comparing `tmp/eos_downloader-0.8.1.tar.gz` & `tmp/eos_downloader-0.8.1.dev1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "eos_downloader-0.8.1.tar", last modified: Sat May 13 13:57:06 2023, max compression
+gzip compressed data, was "eos_downloader-0.8.1.dev1.tar", last modified: Wed Apr 26 09:37:25 2023, max compression
```

## Comparing `eos_downloader-0.8.1.tar` & `eos_downloader-0.8.1.dev1.tar`

### file list

```diff
@@ -1,36 +1,36 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/
--rw-r--r--   0 runner    (1001) docker     (123)    11403 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    20713 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     6244 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/eos_downloader/
--rw-r--r--   0 runner    (1001) docker     (123)     1470 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/eos_downloader/cli/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1882 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cli/cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/eos_downloader/cli/debug/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cli/debug/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1697 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cli/debug/commands.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/eos_downloader/cli/get/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cli/get/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6063 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cli/get/commands.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/eos_downloader/cli/info/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cli/info/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3662 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cli/info/commands.py
--rw-r--r--   0 runner    (1001) docker     (123)     8861 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/cvp.py
--rw-r--r--   0 runner    (1001) docker     (123)     2206 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/data.py
--rw-r--r--   0 runner    (1001) docker     (123)     2627 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/download.py
--rw-r--r--   0 runner    (1001) docker     (123)     6968 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/eos.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/eos_downloader/models/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8993 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/models/version.py
--rw-r--r--   0 runner    (1001) docker     (123)    18478 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/object_downloader.py
--rw-r--r--   0 runner    (1001) docker     (123)      288 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/eos_downloader/tools.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/eos_downloader.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    20713 2023-05-13 13:57:06.000000 eos_downloader-0.8.1/eos_downloader.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      783 2023-05-13 13:57:06.000000 eos_downloader-0.8.1/eos_downloader.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:57:06.000000 eos_downloader-0.8.1/eos_downloader.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-13 13:57:06.000000 eos_downloader-0.8.1/eos_downloader.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      466 2023-05-13 13:57:06.000000 eos_downloader-0.8.1/eos_downloader.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-05-13 13:57:06.000000 eos_downloader-0.8.1/eos_downloader.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     4446 2023-05-13 13:56:56.000000 eos_downloader-0.8.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 13:57:06.739239 eos_downloader-0.8.1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:25.000287 eos_downloader-0.8.1.dev1/
+-rw-r--r--   0 runner    (1001) docker     (123)    11403 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    20718 2023-04-26 09:37:25.000287 eos_downloader-0.8.1.dev1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     6244 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:24.996287 eos_downloader-0.8.1.dev1/eos_downloader/
+-rw-r--r--   0 runner    (1001) docker     (123)     1470 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:24.996287 eos_downloader-0.8.1.dev1/eos_downloader/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1882 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cli/cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:24.996287 eos_downloader-0.8.1.dev1/eos_downloader/cli/debug/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cli/debug/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1697 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cli/debug/commands.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:25.000287 eos_downloader-0.8.1.dev1/eos_downloader/cli/get/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cli/get/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6063 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cli/get/commands.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:25.000287 eos_downloader-0.8.1.dev1/eos_downloader/cli/info/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cli/info/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3662 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cli/info/commands.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8861 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/cvp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2206 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2627 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6968 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/eos.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:25.000287 eos_downloader-0.8.1.dev1/eos_downloader/models/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8993 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/models/version.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18478 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/object_downloader.py
+-rw-r--r--   0 runner    (1001) docker     (123)      288 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/eos_downloader/tools.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-26 09:37:24.996287 eos_downloader-0.8.1.dev1/eos_downloader.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    20718 2023-04-26 09:37:24.000000 eos_downloader-0.8.1.dev1/eos_downloader.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      783 2023-04-26 09:37:24.000000 eos_downloader-0.8.1.dev1/eos_downloader.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-26 09:37:24.000000 eos_downloader-0.8.1.dev1/eos_downloader.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       86 2023-04-26 09:37:24.000000 eos_downloader-0.8.1.dev1/eos_downloader.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      466 2023-04-26 09:37:24.000000 eos_downloader-0.8.1.dev1/eos_downloader.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-04-26 09:37:24.000000 eos_downloader-0.8.1.dev1/eos_downloader.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     4451 2023-04-26 09:37:12.000000 eos_downloader-0.8.1.dev1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-26 09:37:25.000287 eos_downloader-0.8.1.dev1/setup.cfg
```

### Comparing `eos_downloader-0.8.1/LICENSE` & `eos_downloader-0.8.1.dev1/LICENSE`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/PKG-INFO` & `eos_downloader-0.8.1.dev1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: eos_downloader
-Version: 0.8.1
+Version: 0.8.1.dev1
 Summary: Arista EOS/CVP downloader script
 Author-email: Thomas Grimonet <thomas.grimonet@gmail.com>
 Maintainer-email: Thomas Grimonet <thomas.grimonet@gmail.com>
 License: Copyright (c) 2019, Arista Networks
         All rights reserved.
         
                                          Apache License
```

### Comparing `eos_downloader-0.8.1/README.md` & `eos_downloader-0.8.1.dev1/README.md`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/__init__.py` & `eos_downloader-0.8.1.dev1/eos_downloader/__init__.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/cli/cli.py` & `eos_downloader-0.8.1.dev1/eos_downloader/cli/cli.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/cli/debug/commands.py` & `eos_downloader-0.8.1.dev1/eos_downloader/cli/debug/commands.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/cli/get/commands.py` & `eos_downloader-0.8.1.dev1/eos_downloader/cli/get/commands.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/cli/info/commands.py` & `eos_downloader-0.8.1.dev1/eos_downloader/cli/info/commands.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/cvp.py` & `eos_downloader-0.8.1.dev1/eos_downloader/cvp.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/data.py` & `eos_downloader-0.8.1.dev1/eos_downloader/data.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/download.py` & `eos_downloader-0.8.1.dev1/eos_downloader/download.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/eos.py` & `eos_downloader-0.8.1.dev1/eos_downloader/eos.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/models/version.py` & `eos_downloader-0.8.1.dev1/eos_downloader/models/version.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader/object_downloader.py` & `eos_downloader-0.8.1.dev1/eos_downloader/object_downloader.py`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/eos_downloader.egg-info/PKG-INFO` & `eos_downloader-0.8.1.dev1/eos_downloader.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: eos-downloader
-Version: 0.8.1
+Version: 0.8.1.dev1
 Summary: Arista EOS/CVP downloader script
 Author-email: Thomas Grimonet <thomas.grimonet@gmail.com>
 Maintainer-email: Thomas Grimonet <thomas.grimonet@gmail.com>
 License: Copyright (c) 2019, Arista Networks
         All rights reserved.
         
                                          Apache License
```

### Comparing `eos_downloader-0.8.1/eos_downloader.egg-info/SOURCES.txt` & `eos_downloader-0.8.1.dev1/eos_downloader.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `eos_downloader-0.8.1/pyproject.toml` & `eos_downloader-0.8.1.dev1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 [build-system]
 requires = ["setuptools>=64.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "eos_downloader"
-version = "v0.8.1"
+version = "v0.8.1-dev1"
 readme = "README.md"
 authors = [{ name = "Thomas Grimonet", email = "thomas.grimonet@gmail.com" }]
 maintainers = [
   { name = "Thomas Grimonet", email = "thomas.grimonet@gmail.com" },
 ]
 description = "Arista EOS/CVP downloader script"
 license = { file = "LICENSE" }
```

