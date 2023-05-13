# Comparing `tmp/pythoncryptpkgsV2-1.0.0.tar.gz` & `tmp/pythoncryptpkgsV2-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pythoncryptpkgsV2-1.0.0.tar", last modified: Fri May 12 22:26:01 2023, max compression
+gzip compressed data, was "pythoncryptpkgsV2-1.1.0.tar", last modified: Fri May 12 22:28:06 2023, max compression
```

## Comparing `pythoncryptpkgsV2-1.0.0.tar` & `pythoncryptpkgsV2-1.1.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 22:26:01.502619 pythoncryptpkgsV2-1.0.0/
--rw-r--r--   0 root         (0) root         (0)      350 2023-05-12 22:26:01.502619 pythoncryptpkgsV2-1.0.0/PKG-INFO
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 22:26:01.502619 pythoncryptpkgsV2-1.0.0/pythoncryptpkgsV2/
--rw-r--r--   0 root         (0) root         (0)       21 2023-05-12 22:26:01.000000 pythoncryptpkgsV2-1.0.0/pythoncryptpkgsV2/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 22:26:01.502619 pythoncryptpkgsV2-1.0.0/pythoncryptpkgsV2.egg-info/
--rw-r--r--   0 root         (0) root         (0)      350 2023-05-12 22:26:01.000000 pythoncryptpkgsV2-1.0.0/pythoncryptpkgsV2.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      202 2023-05-12 22:26:01.000000 pythoncryptpkgsV2-1.0.0/pythoncryptpkgsV2.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-12 22:26:01.000000 pythoncryptpkgsV2-1.0.0/pythoncryptpkgsV2.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       18 2023-05-12 22:26:01.000000 pythoncryptpkgsV2-1.0.0/pythoncryptpkgsV2.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-12 22:26:01.502619 pythoncryptpkgsV2-1.0.0/setup.cfg
--rw-r--r--   0 root         (0) root         (0)      563 2023-05-12 22:26:01.000000 pythoncryptpkgsV2-1.0.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 22:28:06.825264 pythoncryptpkgsV2-1.1.0/
+-rw-r--r--   0 root         (0) root         (0)      350 2023-05-12 22:28:06.825264 pythoncryptpkgsV2-1.1.0/PKG-INFO
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 22:28:06.821264 pythoncryptpkgsV2-1.1.0/pythoncryptpkgsV2/
+-rw-r--r--   0 root         (0) root         (0)    97161 2023-05-12 22:28:06.000000 pythoncryptpkgsV2-1.1.0/pythoncryptpkgsV2/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 22:28:06.825264 pythoncryptpkgsV2-1.1.0/pythoncryptpkgsV2.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      350 2023-05-12 22:28:06.000000 pythoncryptpkgsV2-1.1.0/pythoncryptpkgsV2.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      202 2023-05-12 22:28:06.000000 pythoncryptpkgsV2-1.1.0/pythoncryptpkgsV2.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-12 22:28:06.000000 pythoncryptpkgsV2-1.1.0/pythoncryptpkgsV2.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       18 2023-05-12 22:28:06.000000 pythoncryptpkgsV2-1.1.0/pythoncryptpkgsV2.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-12 22:28:06.825264 pythoncryptpkgsV2-1.1.0/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)      563 2023-05-12 22:28:06.000000 pythoncryptpkgsV2-1.1.0/setup.py
```

### Comparing `pythoncryptpkgsV2-1.0.0/setup.py` & `pythoncryptpkgsV2-1.1.0/setup.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '1.0.0'
+VERSION = '1.1.0'
 DESCRIPTION = "Usefull utility package"
 LONG_DESCRIPTION = "Usefull utility package"
 
 # Setting up
 setup(
     name="pythoncryptpkgsV2",
     version=VERSION,
```

