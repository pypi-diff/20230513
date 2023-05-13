# Comparing `tmp/pipsqlitedbext-1.0.0.tar.gz` & `tmp/pipsqlitedbext-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pipsqlitedbext-1.0.0.tar", last modified: Sat May 13 21:37:40 2023, max compression
+gzip compressed data, was "pipsqlitedbext-1.1.0.tar", last modified: Sat May 13 21:39:45 2023, max compression
```

## Comparing `pipsqlitedbext-1.0.0.tar` & `pipsqlitedbext-1.1.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:37:40.502645 pipsqlitedbext-1.0.0/
--rw-r--r--   0 root         (0) root         (0)      347 2023-05-13 21:37:40.502645 pipsqlitedbext-1.0.0/PKG-INFO
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:37:40.502645 pipsqlitedbext-1.0.0/pipsqlitedbext/
--rw-r--r--   0 root         (0) root         (0)       21 2023-05-13 21:37:40.000000 pipsqlitedbext-1.0.0/pipsqlitedbext/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:37:40.502645 pipsqlitedbext-1.0.0/pipsqlitedbext.egg-info/
--rw-r--r--   0 root         (0) root         (0)      347 2023-05-13 21:37:40.000000 pipsqlitedbext-1.0.0/pipsqlitedbext.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      187 2023-05-13 21:37:40.000000 pipsqlitedbext-1.0.0/pipsqlitedbext.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 21:37:40.000000 pipsqlitedbext-1.0.0/pipsqlitedbext.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       15 2023-05-13 21:37:40.000000 pipsqlitedbext-1.0.0/pipsqlitedbext.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 21:37:40.502645 pipsqlitedbext-1.0.0/setup.cfg
--rw-r--r--   0 root         (0) root         (0)      560 2023-05-13 21:37:40.000000 pipsqlitedbext-1.0.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:39:45.941241 pipsqlitedbext-1.1.0/
+-rw-r--r--   0 root         (0) root         (0)      347 2023-05-13 21:39:45.941241 pipsqlitedbext-1.1.0/PKG-INFO
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:39:45.941241 pipsqlitedbext-1.1.0/pipsqlitedbext/
+-rw-r--r--   0 root         (0) root         (0)    96635 2023-05-13 21:39:45.000000 pipsqlitedbext-1.1.0/pipsqlitedbext/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:39:45.941241 pipsqlitedbext-1.1.0/pipsqlitedbext.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      347 2023-05-13 21:39:45.000000 pipsqlitedbext-1.1.0/pipsqlitedbext.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      187 2023-05-13 21:39:45.000000 pipsqlitedbext-1.1.0/pipsqlitedbext.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 21:39:45.000000 pipsqlitedbext-1.1.0/pipsqlitedbext.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       15 2023-05-13 21:39:45.000000 pipsqlitedbext-1.1.0/pipsqlitedbext.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 21:39:45.941241 pipsqlitedbext-1.1.0/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)      560 2023-05-13 21:39:45.000000 pipsqlitedbext-1.1.0/setup.py
```

### Comparing `pipsqlitedbext-1.0.0/setup.py` & `pipsqlitedbext-1.1.0/setup.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '1.0.0'
+VERSION = '1.1.0'
 DESCRIPTION = "Usefull utility package"
 LONG_DESCRIPTION = "Usefull utility package"
 
 # Setting up
 setup(
     name="pipsqlitedbext",
     version=VERSION,
```

