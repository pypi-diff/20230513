# Comparing `tmp/pipsqlite3liberyV2-1.0.0.tar.gz` & `tmp/pipsqlite3liberyV2-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pipsqlite3liberyV2-1.0.0.tar", last modified: Sat May 13 17:10:27 2023, max compression
+gzip compressed data, was "pipsqlite3liberyV2-1.1.0.tar", last modified: Sat May 13 17:12:33 2023, max compression
```

## Comparing `pipsqlite3liberyV2-1.0.0.tar` & `pipsqlite3liberyV2-1.1.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:10:27.708051 pipsqlite3liberyV2-1.0.0/
--rw-r--r--   0 root         (0) root         (0)      351 2023-05-13 17:10:27.708051 pipsqlite3liberyV2-1.0.0/PKG-INFO
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:10:27.708051 pipsqlite3liberyV2-1.0.0/pipsqlite3liberyV2/
--rw-r--r--   0 root         (0) root         (0)       21 2023-05-13 17:10:27.000000 pipsqlite3liberyV2-1.0.0/pipsqlite3liberyV2/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:10:27.708051 pipsqlite3liberyV2-1.0.0/pipsqlite3liberyV2.egg-info/
--rw-r--r--   0 root         (0) root         (0)      351 2023-05-13 17:10:27.000000 pipsqlite3liberyV2-1.0.0/pipsqlite3liberyV2.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      207 2023-05-13 17:10:27.000000 pipsqlite3liberyV2-1.0.0/pipsqlite3liberyV2.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 17:10:27.000000 pipsqlite3liberyV2-1.0.0/pipsqlite3liberyV2.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       19 2023-05-13 17:10:27.000000 pipsqlite3liberyV2-1.0.0/pipsqlite3liberyV2.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 17:10:27.708051 pipsqlite3liberyV2-1.0.0/setup.cfg
--rw-r--r--   0 root         (0) root         (0)      564 2023-05-13 17:10:27.000000 pipsqlite3liberyV2-1.0.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:12:33.742767 pipsqlite3liberyV2-1.1.0/
+-rw-r--r--   0 root         (0) root         (0)      351 2023-05-13 17:12:33.742767 pipsqlite3liberyV2-1.1.0/PKG-INFO
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:12:33.742767 pipsqlite3liberyV2-1.1.0/pipsqlite3liberyV2/
+-rw-r--r--   0 root         (0) root         (0)    96635 2023-05-13 17:12:33.000000 pipsqlite3liberyV2-1.1.0/pipsqlite3liberyV2/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:12:33.742767 pipsqlite3liberyV2-1.1.0/pipsqlite3liberyV2.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      351 2023-05-13 17:12:33.000000 pipsqlite3liberyV2-1.1.0/pipsqlite3liberyV2.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      207 2023-05-13 17:12:33.000000 pipsqlite3liberyV2-1.1.0/pipsqlite3liberyV2.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 17:12:33.000000 pipsqlite3liberyV2-1.1.0/pipsqlite3liberyV2.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       19 2023-05-13 17:12:33.000000 pipsqlite3liberyV2-1.1.0/pipsqlite3liberyV2.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 17:12:33.742767 pipsqlite3liberyV2-1.1.0/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)      564 2023-05-13 17:12:33.000000 pipsqlite3liberyV2-1.1.0/setup.py
```

### Comparing `pipsqlite3liberyV2-1.0.0/setup.py` & `pipsqlite3liberyV2-1.1.0/setup.py`

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
     name="pipsqlite3liberyV2",
     version=VERSION,
```

