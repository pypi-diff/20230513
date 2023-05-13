# Comparing `tmp/pythoncolouringpkgV1-1.0.0.tar.gz` & `tmp/pythoncolouringpkgV1-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pythoncolouringpkgV1-1.0.0.tar", last modified: Sat May 13 18:10:29 2023, max compression
+gzip compressed data, was "pythoncolouringpkgV1-1.1.0.tar", last modified: Sat May 13 18:12:34 2023, max compression
```

## Comparing `pythoncolouringpkgV1-1.0.0.tar` & `pythoncolouringpkgV1-1.1.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:10:29.883951 pythoncolouringpkgV1-1.0.0/
--rw-r--r--   0 root         (0) root         (0)      353 2023-05-13 18:10:29.883951 pythoncolouringpkgV1-1.0.0/PKG-INFO
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:10:29.883951 pythoncolouringpkgV1-1.0.0/pythoncolouringpkgV1/
--rw-r--r--   0 root         (0) root         (0)       21 2023-05-13 18:10:29.000000 pythoncolouringpkgV1-1.0.0/pythoncolouringpkgV1/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:10:29.883951 pythoncolouringpkgV1-1.0.0/pythoncolouringpkgV1.egg-info/
--rw-r--r--   0 root         (0) root         (0)      353 2023-05-13 18:10:29.000000 pythoncolouringpkgV1-1.0.0/pythoncolouringpkgV1.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      217 2023-05-13 18:10:29.000000 pythoncolouringpkgV1-1.0.0/pythoncolouringpkgV1.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 18:10:29.000000 pythoncolouringpkgV1-1.0.0/pythoncolouringpkgV1.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       21 2023-05-13 18:10:29.000000 pythoncolouringpkgV1-1.0.0/pythoncolouringpkgV1.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 18:10:29.883951 pythoncolouringpkgV1-1.0.0/setup.cfg
--rw-r--r--   0 root         (0) root         (0)      566 2023-05-13 18:10:29.000000 pythoncolouringpkgV1-1.0.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:12:34.990559 pythoncolouringpkgV1-1.1.0/
+-rw-r--r--   0 root         (0) root         (0)      353 2023-05-13 18:12:34.990559 pythoncolouringpkgV1-1.1.0/PKG-INFO
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:12:34.990559 pythoncolouringpkgV1-1.1.0/pythoncolouringpkgV1/
+-rw-r--r--   0 root         (0) root         (0)    96635 2023-05-13 18:12:34.000000 pythoncolouringpkgV1-1.1.0/pythoncolouringpkgV1/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 18:12:34.990559 pythoncolouringpkgV1-1.1.0/pythoncolouringpkgV1.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      353 2023-05-13 18:12:34.000000 pythoncolouringpkgV1-1.1.0/pythoncolouringpkgV1.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      217 2023-05-13 18:12:34.000000 pythoncolouringpkgV1-1.1.0/pythoncolouringpkgV1.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 18:12:34.000000 pythoncolouringpkgV1-1.1.0/pythoncolouringpkgV1.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       21 2023-05-13 18:12:34.000000 pythoncolouringpkgV1-1.1.0/pythoncolouringpkgV1.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 18:12:34.990559 pythoncolouringpkgV1-1.1.0/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)      566 2023-05-13 18:12:34.000000 pythoncolouringpkgV1-1.1.0/setup.py
```

### Comparing `pythoncolouringpkgV1-1.0.0/setup.py` & `pythoncolouringpkgV1-1.1.0/setup.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '1.0.0'
+VERSION = '1.1.0'
 DESCRIPTION = "Usefull utility package"
 LONG_DESCRIPTION = "Usefull utility package"
 
 # Setting up
 setup(
     name="pythoncolouringpkgV1",
     version=VERSION,
```

