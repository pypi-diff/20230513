# Comparing `tmp/numba-integrators-0.0.2.tar.gz` & `tmp/numba-integrators-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "numba-integrators-0.0.2.tar", last modified: Sun May  7 20:40:24 2023, max compression
+gzip compressed data, was "numba-integrators-0.0.3.tar", last modified: Sat May 13 21:19:01 2023, max compression
```

## Comparing `numba-integrators-0.0.2.tar` & `numba-integrators-0.0.3.tar`

### file list

```diff
@@ -1,18 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 20:40:24.652508 numba-integrators-0.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-07 20:39:49.000000 numba-integrators-0.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1575 2023-05-07 20:40:24.652508 numba-integrators-0.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      720 2023-05-07 20:40:21.000000 numba-integrators-0.0.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-07 20:39:49.000000 numba-integrators-0.0.2/dependencies.txt
--rw-r--r--   0 runner    (1001) docker     (123)      294 2023-05-07 20:39:49.000000 numba-integrators-0.0.2/dependencies_dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1247 2023-05-07 20:40:21.000000 numba-integrators-0.0.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-07 20:40:24.652508 numba-integrators-0.0.2/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 20:40:24.648508 numba-integrators-0.0.2/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 20:40:24.652508 numba-integrators-0.0.2/src/numba_integrators/
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-07 20:39:49.000000 numba-integrators-0.0.2/src/numba_integrators/_API.py
--rw-r--r--   0 runner    (1001) docker     (123)       66 2023-05-07 20:39:49.000000 numba-integrators-0.0.2/src/numba_integrators/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 20:40:24.652508 numba-integrators-0.0.2/src/numba_integrators.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1575 2023-05-07 20:40:24.000000 numba-integrators-0.0.2/src/numba_integrators.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      358 2023-05-07 20:40:24.000000 numba-integrators-0.0.2/src/numba_integrators.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-07 20:40:24.000000 numba-integrators-0.0.2/src/numba_integrators.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      296 2023-05-07 20:40:24.000000 numba-integrators-0.0.2/src/numba_integrators.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-07 20:40:24.000000 numba-integrators-0.0.2/src/numba_integrators.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:19:01.992125 numba-integrators-0.0.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 21:18:29.000000 numba-integrators-0.0.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2241 2023-05-13 21:19:01.992125 numba-integrators-0.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1313 2023-05-13 21:18:29.000000 numba-integrators-0.0.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:19:01.992125 numba-integrators-0.0.3/dependencies/
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 21:18:29.000000 numba-integrators-0.0.3/dependencies/build.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-05-13 21:18:29.000000 numba-integrators-0.0.3/dependencies/dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-05-13 21:18:29.000000 numba-integrators-0.0.3/dependencies/main.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1241 2023-05-13 21:18:54.000000 numba-integrators-0.0.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 21:19:01.992125 numba-integrators-0.0.3/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:19:01.988125 numba-integrators-0.0.3/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:19:01.992125 numba-integrators-0.0.3/src/numba_integrators/
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 21:18:29.000000 numba-integrators-0.0.3/src/numba_integrators/_API.py
+-rw-r--r--   0 runner    (1001) docker     (123)       66 2023-05-13 21:18:29.000000 numba-integrators-0.0.3/src/numba_integrators/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:19:01.992125 numba-integrators-0.0.3/src/numba_integrators.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2241 2023-05-13 21:19:01.000000 numba-integrators-0.0.3/src/numba_integrators.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      386 2023-05-13 21:19:01.000000 numba-integrators-0.0.3/src/numba_integrators.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 21:19:01.000000 numba-integrators-0.0.3/src/numba_integrators.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      201 2023-05-13 21:19:01.000000 numba-integrators-0.0.3/src/numba_integrators.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-13 21:19:01.000000 numba-integrators-0.0.3/src/numba_integrators.egg-info/top_level.txt
```

### Comparing `numba-integrators-0.0.2/LICENSE` & `numba-integrators-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `numba-integrators-0.0.2/pyproject.toml` & `numba-integrators-0.0.3/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,12 +1,7 @@
-[master-info]
-organisation = "https://github.com/Limespy"
-package_name = "numba-integrators"
-description = "Numerical integrators using Numba"
-
 [build-system]
 requires = [
     "setuptools>=64.0",
 ]
 build-backend = "setuptools.build_meta"
 
 [project]
@@ -17,31 +12,35 @@
     "License :: OSI Approved :: MIT License",
     "Operating System :: Unix",
     "Operating System :: POSIX",
     "Operating System :: Microsoft :: Windows",
     "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3 :: Only",
     "Programming Language :: Python :: 3.10",
+    "Programming Language :: Python :: 3.11",
 ]
 authors = [
     { name = "Limespy" },
 ]
 requires-python = ">=3.10"
 readme = "README.md"
-version = "0.0.2"
+version = "0.0.3"
 dynamic = [
     "dependencies",
     "optional-dependencies",
 ]
 
 [project.urls]
 Homepage = "https://github.com/Limespy/numba-integrators"
 Changelog = "https://github.com/Limespy/numba-integrators/blob/main/README.md#Changelog"
 "Issue Tracker" = "https://github.com/Limespy/numba-integrators/issues"
 
 [tool.setuptools.dynamic.dependencies]
 file = [
-    "dependencies.txt",
+    "dependencies/main.txt",
 ]
 
 [tool.setuptools.dynamic.optional-dependencies.dev]
-file = "dependencies_dev.txt"
+file = "dependencies/dev.txt"
+
+[tool.setuptools.dynamic.optional-dependencies.build]
+file = "dependencies/build.txt"
```

