# Comparing `tmp/PY_PACKAGE_NAME-0.0.1.tar.gz` & `tmp/PY_PACKAGE_NAME-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PY_PACKAGE_NAME-0.0.1.tar", last modified: Fri May 12 15:48:23 2023, max compression
+gzip compressed data, was "PY_PACKAGE_NAME-0.0.2.tar", last modified: Sat May 13 08:24:10 2023, max compression
```

## Comparing `PY_PACKAGE_NAME-0.0.1.tar` & `PY_PACKAGE_NAME-0.0.2.tar`

### file list

```diff
@@ -1,18 +1,17 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 15:48:23.775015 PY_PACKAGE_NAME-0.0.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-05-12 15:48:04.000000 PY_PACKAGE_NAME-0.0.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      672 2023-05-12 15:48:23.775015 PY_PACKAGE_NAME-0.0.1/PKG-INFO
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 15:48:23.775015 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME/
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-12 15:48:22.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       96 2023-05-12 15:48:04.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME/core.py
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-12 15:48:04.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 15:48:23.775015 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      672 2023-05-12 15:48:23.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      356 2023-05-12 15:48:23.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 15:48:23.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       62 2023-05-12 15:48:23.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       42 2023-05-12 15:48:23.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-12 15:48:23.000000 PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-12 15:48:04.000000 PY_PACKAGE_NAME-0.0.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     1048 2023-05-12 15:48:04.000000 PY_PACKAGE_NAME-0.0.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 15:48:23.775015 PY_PACKAGE_NAME-0.0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1297 2023-05-12 15:48:22.000000 PY_PACKAGE_NAME-0.0.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:24:10.097657 PY_PACKAGE_NAME-0.0.2/
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-05-13 08:23:32.000000 PY_PACKAGE_NAME-0.0.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      672 2023-05-13 08:24:10.097657 PY_PACKAGE_NAME-0.0.2/PKG-INFO
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:24:10.097657 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME/
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 08:24:08.000000 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       96 2023-05-13 08:23:32.000000 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME/core.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:24:10.097657 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      672 2023-05-13 08:24:10.000000 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      329 2023-05-13 08:24:10.000000 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:24:10.000000 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       62 2023-05-13 08:24:10.000000 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       42 2023-05-13 08:24:10.000000 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 08:24:10.000000 PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 08:23:32.000000 PY_PACKAGE_NAME-0.0.2/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1048 2023-05-13 08:23:32.000000 PY_PACKAGE_NAME-0.0.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 08:24:10.097657 PY_PACKAGE_NAME-0.0.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1297 2023-05-13 08:24:08.000000 PY_PACKAGE_NAME-0.0.2/setup.py
```

### Comparing `PY_PACKAGE_NAME-0.0.1/LICENSE` & `PY_PACKAGE_NAME-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `PY_PACKAGE_NAME-0.0.1/PKG-INFO` & `PY_PACKAGE_NAME-0.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PY_PACKAGE_NAME
-Version: 0.0.1
+Version: 0.0.2
 Summary: SHORT_DESCRIPTION
 Home-page: https://github.com/AUTHOR_NAME/YOUR_PACKAGE_NAME
 Author: AUTHOR_NAME
 Author-email: AUTHOR_EMAIL@gmail.com
 License: MIT License
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `PY_PACKAGE_NAME-0.0.1/PY_PACKAGE_NAME.egg-info/PKG-INFO` & `PY_PACKAGE_NAME-0.0.2/PY_PACKAGE_NAME.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PY-PACKAGE-NAME
-Version: 0.0.1
+Version: 0.0.2
 Summary: SHORT_DESCRIPTION
 Home-page: https://github.com/AUTHOR_NAME/YOUR_PACKAGE_NAME
 Author: AUTHOR_NAME
 Author-email: AUTHOR_EMAIL@gmail.com
 License: MIT License
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `PY_PACKAGE_NAME-0.0.1/pyproject.toml` & `PY_PACKAGE_NAME-0.0.2/pyproject.toml`

 * *Files identical despite different names*

### Comparing `PY_PACKAGE_NAME-0.0.1/setup.py` & `PY_PACKAGE_NAME-0.0.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 this_directory = path.abspath(path.dirname(__file__))
 with open(path.join(this_directory, "README.md"), encoding="utf-8") as f:
     long_description = f.read()
 
 setup(
     name='PY_PACKAGE_NAME',
     license="MIT License",
-    version='0.0.1',
+    version='0.0.2',
     author='AUTHOR_NAME',
     author_email='AUTHOR_EMAIL@gmail.com',
     description='SHORT_DESCRIPTION',
     long_description=long_description,
     long_description_content_type="text/markdown",
     url='https://github.com/AUTHOR_NAME/YOUR_PACKAGE_NAME',
     packages=find_packages(exclude=["tests*"]),
```

