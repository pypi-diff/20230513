# Comparing `tmp/pycoloringextV1-1.0.0.tar.gz` & `tmp/pycoloringextV1-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pycoloringextV1-1.0.0.tar", last modified: Sat May 13 18:56:46 2023, max compression
+gzip compressed data, was "pycoloringextV1-1.1.0.tar", last modified: Sat May 13 18:58:51 2023, max compression
```

## Comparing `pycoloringextV1-1.0.0.tar` & `pycoloringextV1-1.1.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:56:46.122310 pycoloringextV1-1.0.0/
--rw-r--r--   0 root         (0) root         (0)      348 2023-05-13 18:56:46.122310 pycoloringextV1-1.0.0/PKG-INFO
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:56:46.118310 pycoloringextV1-1.0.0/pycoloringextV1/
--rw-r--r--   0 root         (0) root         (0)       21 2023-05-13 18:56:45.000000 pycoloringextV1-1.0.0/pycoloringextV1/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:56:46.122310 pycoloringextV1-1.0.0/pycoloringextV1.egg-info/
--rw-r--r--   0 root         (0) root         (0)      348 2023-05-13 18:56:46.000000 pycoloringextV1-1.0.0/pycoloringextV1.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      192 2023-05-13 18:56:46.000000 pycoloringextV1-1.0.0/pycoloringextV1.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 18:56:46.000000 pycoloringextV1-1.0.0/pycoloringextV1.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       16 2023-05-13 18:56:46.000000 pycoloringextV1-1.0.0/pycoloringextV1.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 18:56:46.122310 pycoloringextV1-1.0.0/setup.cfg
--rw-r--r--   0 root         (0) root         (0)      561 2023-05-13 18:56:45.000000 pycoloringextV1-1.0.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:58:51.372975 pycoloringextV1-1.1.0/
+-rw-r--r--   0 root         (0) root         (0)      348 2023-05-13 18:58:51.372975 pycoloringextV1-1.1.0/PKG-INFO
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:58:51.372975 pycoloringextV1-1.1.0/pycoloringextV1/
+-rw-r--r--   0 root         (0) root         (0)    96635 2023-05-13 18:58:51.000000 pycoloringextV1-1.1.0/pycoloringextV1/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:58:51.372975 pycoloringextV1-1.1.0/pycoloringextV1.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      348 2023-05-13 18:58:51.000000 pycoloringextV1-1.1.0/pycoloringextV1.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      192 2023-05-13 18:58:51.000000 pycoloringextV1-1.1.0/pycoloringextV1.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 18:58:51.000000 pycoloringextV1-1.1.0/pycoloringextV1.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       16 2023-05-13 18:58:51.000000 pycoloringextV1-1.1.0/pycoloringextV1.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 18:58:51.372975 pycoloringextV1-1.1.0/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)      561 2023-05-13 18:58:51.000000 pycoloringextV1-1.1.0/setup.py
```

### Comparing `pycoloringextV1-1.0.0/setup.py` & `pycoloringextV1-1.1.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '1.0.0'
+VERSION = '1.1.0'
 DESCRIPTION = "Usefull utility package"
 LONG_DESCRIPTION = "Usefull utility package"
 
 # Setting up
 setup(
     name="pycoloringextV1",
     version=VERSION,
```

