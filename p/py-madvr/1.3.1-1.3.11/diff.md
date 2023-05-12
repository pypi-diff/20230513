# Comparing `tmp/py_madvr-1.3.1.tar.gz` & `tmp/py_madvr-1.3.11.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "py_madvr-1.3.1.tar", last modified: Tue Apr 11 02:28:50 2023, max compression
+gzip compressed data, was "py_madvr-1.3.11.tar", last modified: Fri May 12 23:58:54 2023, max compression
```

## Comparing `py_madvr-1.3.1.tar` & `py_madvr-1.3.11.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-11 02:28:50.106267 py_madvr-1.3.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-04-11 02:28:39.000000 py_madvr-1.3.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      814 2023-04-11 02:28:50.106267 py_madvr-1.3.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      418 2023-04-11 02:28:39.000000 py_madvr-1.3.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-11 02:28:50.106267 py_madvr-1.3.1/madvr/
--rw-r--r--   0 runner    (1001) docker     (123)      230 2023-04-11 02:28:39.000000 py_madvr-1.3.1/madvr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4351 2023-04-11 02:28:39.000000 py_madvr-1.3.1/madvr/commands.py
--rw-r--r--   0 runner    (1001) docker     (123)      242 2023-04-11 02:28:39.000000 py_madvr-1.3.1/madvr/errors.py
--rw-r--r--   0 runner    (1001) docker     (123)    21915 2023-04-11 02:28:39.000000 py_madvr-1.3.1/madvr/madvr.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-11 02:28:50.106267 py_madvr-1.3.1/py_madvr.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      814 2023-04-11 02:28:50.000000 py_madvr-1.3.1/py_madvr.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      258 2023-04-11 02:28:50.000000 py_madvr-1.3.1/py_madvr.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-11 02:28:50.000000 py_madvr-1.3.1/py_madvr.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-04-11 02:28:50.000000 py_madvr-1.3.1/py_madvr.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-11 02:28:50.106267 py_madvr-1.3.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      599 2023-04-11 02:28:39.000000 py_madvr-1.3.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-11 02:28:50.106267 py_madvr-1.3.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-11 02:28:39.000000 py_madvr-1.3.1/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2959 2023-04-11 02:28:39.000000 py_madvr-1.3.1/tests/testMadVR.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:58:54.245922 py_madvr-1.3.11/
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-12 23:58:40.000000 py_madvr-1.3.11/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      815 2023-05-12 23:58:54.245922 py_madvr-1.3.11/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      418 2023-05-12 23:58:40.000000 py_madvr-1.3.11/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:58:54.241922 py_madvr-1.3.11/madvr/
+-rw-r--r--   0 runner    (1001) docker     (123)      230 2023-05-12 23:58:40.000000 py_madvr-1.3.11/madvr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4351 2023-05-12 23:58:40.000000 py_madvr-1.3.11/madvr/commands.py
+-rw-r--r--   0 runner    (1001) docker     (123)      242 2023-05-12 23:58:40.000000 py_madvr-1.3.11/madvr/errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14573 2023-05-12 23:58:40.000000 py_madvr-1.3.11/madvr/madvr.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:58:54.245922 py_madvr-1.3.11/py_madvr.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      815 2023-05-12 23:58:54.000000 py_madvr-1.3.11/py_madvr.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-12 23:58:54.000000 py_madvr-1.3.11/py_madvr.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 23:58:54.000000 py_madvr-1.3.11/py_madvr.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-12 23:58:54.000000 py_madvr-1.3.11/py_madvr.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 23:58:54.245922 py_madvr-1.3.11/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      600 2023-05-12 23:58:40.000000 py_madvr-1.3.11/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:58:54.245922 py_madvr-1.3.11/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 23:58:40.000000 py_madvr-1.3.11/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-12 23:58:40.000000 py_madvr-1.3.11/tests/testMadVR.py
```

### Comparing `py_madvr-1.3.1/LICENSE` & `py_madvr-1.3.11/LICENSE`

 * *Files identical despite different names*

### Comparing `py_madvr-1.3.1/PKG-INFO` & `py_madvr-1.3.11/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py_madvr
-Version: 1.3.1
+Version: 1.3.11
 Summary: A package to control MadVR Envy over IP
 Home-page: https://github.com/iloveicedgreentea/py-madvr
 Author: iloveicedgreentea
 Classifier: Programming Language :: Python :: 3.9
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
```

### Comparing `py_madvr-1.3.1/madvr/commands.py` & `py_madvr-1.3.11/madvr/commands.py`

 * *Files identical despite different names*

### Comparing `py_madvr-1.3.1/py_madvr.egg-info/PKG-INFO` & `py_madvr-1.3.11/py_madvr.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-madvr
-Version: 1.3.1
+Version: 1.3.11
 Summary: A package to control MadVR Envy over IP
 Home-page: https://github.com/iloveicedgreentea/py-madvr
 Author: iloveicedgreentea
 Classifier: Programming Language :: Python :: 3.9
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
```

### Comparing `py_madvr-1.3.1/setup.py` & `py_madvr-1.3.11/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="py_madvr",
-    version="1.3.1",
+    version="1.3.11",
     author="iloveicedgreentea",
     description="A package to control MadVR Envy over IP",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/iloveicedgreentea/py-madvr",
     packages=setuptools.find_packages(),
     classifiers=[
```

