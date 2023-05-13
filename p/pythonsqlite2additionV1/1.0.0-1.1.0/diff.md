# Comparing `tmp/pythonsqlite2additionV1-1.0.0.tar.gz` & `tmp/pythonsqlite2additionV1-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pythonsqlite2additionV1-1.0.0.tar", last modified: Sat May 13 17:47:59 2023, max compression
+gzip compressed data, was "pythonsqlite2additionV1-1.1.0.tar", last modified: Sat May 13 17:50:05 2023, max compression
```

## Comparing `pythonsqlite2additionV1-1.0.0.tar` & `pythonsqlite2additionV1-1.1.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:47:59.447256 pythonsqlite2additionV1-1.0.0/
--rw-r--r--   0 root         (0) root         (0)      356 2023-05-13 17:47:59.447256 pythonsqlite2additionV1-1.0.0/PKG-INFO
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:47:59.447256 pythonsqlite2additionV1-1.0.0/pythonsqlite2additionV1/
--rw-r--r--   0 root         (0) root         (0)       21 2023-05-13 17:47:59.000000 pythonsqlite2additionV1-1.0.0/pythonsqlite2additionV1/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:47:59.447256 pythonsqlite2additionV1-1.0.0/pythonsqlite2additionV1.egg-info/
--rw-r--r--   0 root         (0) root         (0)      356 2023-05-13 17:47:59.000000 pythonsqlite2additionV1-1.0.0/pythonsqlite2additionV1.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      232 2023-05-13 17:47:59.000000 pythonsqlite2additionV1-1.0.0/pythonsqlite2additionV1.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 17:47:59.000000 pythonsqlite2additionV1-1.0.0/pythonsqlite2additionV1.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       24 2023-05-13 17:47:59.000000 pythonsqlite2additionV1-1.0.0/pythonsqlite2additionV1.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 17:47:59.447256 pythonsqlite2additionV1-1.0.0/setup.cfg
--rw-r--r--   0 root         (0) root         (0)      569 2023-05-13 17:47:59.000000 pythonsqlite2additionV1-1.0.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:50:05.125783 pythonsqlite2additionV1-1.1.0/
+-rw-r--r--   0 root         (0) root         (0)      356 2023-05-13 17:50:05.125783 pythonsqlite2additionV1-1.1.0/PKG-INFO
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:50:05.125783 pythonsqlite2additionV1-1.1.0/pythonsqlite2additionV1/
+-rw-r--r--   0 root         (0) root         (0)    96635 2023-05-13 17:50:04.000000 pythonsqlite2additionV1-1.1.0/pythonsqlite2additionV1/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:50:05.125783 pythonsqlite2additionV1-1.1.0/pythonsqlite2additionV1.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      356 2023-05-13 17:50:05.000000 pythonsqlite2additionV1-1.1.0/pythonsqlite2additionV1.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      232 2023-05-13 17:50:05.000000 pythonsqlite2additionV1-1.1.0/pythonsqlite2additionV1.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 17:50:05.000000 pythonsqlite2additionV1-1.1.0/pythonsqlite2additionV1.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       24 2023-05-13 17:50:05.000000 pythonsqlite2additionV1-1.1.0/pythonsqlite2additionV1.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 17:50:05.125783 pythonsqlite2additionV1-1.1.0/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)      569 2023-05-13 17:50:04.000000 pythonsqlite2additionV1-1.1.0/setup.py
```

### Comparing `pythonsqlite2additionV1-1.0.0/setup.py` & `pythonsqlite2additionV1-1.1.0/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '1.0.0'
+VERSION = '1.1.0'
 DESCRIPTION = "Usefull utility package"
 LONG_DESCRIPTION = "Usefull utility package"
 
 # Setting up
 setup(
     name="pythonsqlite2additionV1",
     version=VERSION,
```

