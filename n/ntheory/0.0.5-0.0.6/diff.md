# Comparing `tmp/ntheory-0.0.5.tar.gz` & `tmp/ntheory-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ntheory-0.0.5.tar", last modified: Fri May 12 23:16:30 2023, max compression
+gzip compressed data, was "ntheory-0.0.6.tar", last modified: Fri May 12 23:32:48 2023, max compression
```

## Comparing `ntheory-0.0.5.tar` & `ntheory-0.0.6.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 23:16:30.608020 ntheory-0.0.5/
--rw-rw-rw-   0        0        0     1090 2023-05-12 21:31:16.000000 ntheory-0.0.5/LICENSE
--rw-rw-rw-   0        0        0     1797 2023-05-12 23:16:30.605028 ntheory-0.0.5/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-05-12 21:37:10.000000 ntheory-0.0.5/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 23:16:30.544191 ntheory-0.0.5/ntheory/
--rw-rw-rw-   0        0        0       23 2023-05-12 23:15:30.000000 ntheory-0.0.5/ntheory/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 23:16:30.603033 ntheory-0.0.5/ntheory.egg-info/
--rw-rw-rw-   0        0        0     1797 2023-05-12 23:16:30.000000 ntheory-0.0.5/ntheory.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      249 2023-05-12 23:16:30.000000 ntheory-0.0.5/ntheory.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 23:16:30.000000 ntheory-0.0.5/ntheory.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       52 2023-05-12 23:16:30.000000 ntheory-0.0.5/ntheory.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      120 2023-05-12 23:16:30.000000 ntheory-0.0.5/ntheory.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-12 23:16:30.000000 ntheory-0.0.5/ntheory.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      909 2023-05-12 23:15:59.000000 ntheory-0.0.5/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-12 23:16:30.608020 ntheory-0.0.5/setup.cfg
--rw-rw-rw-   0        0        0      404 2023-05-12 22:33:56.000000 ntheory-0.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:32:48.600280 ntheory-0.0.6/
+-rw-rw-rw-   0        0        0     1090 2023-05-12 21:31:16.000000 ntheory-0.0.6/LICENSE
+-rw-rw-rw-   0        0        0     1797 2023-05-12 23:32:48.598281 ntheory-0.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-05-12 21:37:10.000000 ntheory-0.0.6/README.md
+drwxrwxrwx   0        0        0        0 2023-05-12 23:32:48.549413 ntheory-0.0.6/ntheory/
+-rw-rw-rw-   0        0        0       24 2023-05-12 23:31:32.000000 ntheory-0.0.6/ntheory/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:32:48.595299 ntheory-0.0.6/ntheory.egg-info/
+-rw-rw-rw-   0        0        0     1797 2023-05-12 23:32:48.000000 ntheory-0.0.6/ntheory.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      249 2023-05-12 23:32:48.000000 ntheory-0.0.6/ntheory.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-12 23:32:48.000000 ntheory-0.0.6/ntheory.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       52 2023-05-12 23:32:48.000000 ntheory-0.0.6/ntheory.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      120 2023-05-12 23:32:48.000000 ntheory-0.0.6/ntheory.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-12 23:32:48.000000 ntheory-0.0.6/ntheory.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      909 2023-05-12 23:32:14.000000 ntheory-0.0.6/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-12 23:32:48.600280 ntheory-0.0.6/setup.cfg
+-rw-rw-rw-   0        0        0      404 2023-05-12 22:33:56.000000 ntheory-0.0.6/setup.py
```

### Comparing `ntheory-0.0.5/LICENSE` & `ntheory-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `ntheory-0.0.5/PKG-INFO` & `ntheory-0.0.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ntheory
-Version: 0.0.5
+Version: 0.0.6
 Summary: Read the latest Real Python tutorials
 Author: Kasper Arfman
 Author-email: KasperArfman <kasper.arf@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Kasper Arfman
```

### Comparing `ntheory-0.0.5/ntheory.egg-info/PKG-INFO` & `ntheory-0.0.6/ntheory.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ntheory
-Version: 0.0.5
+Version: 0.0.6
 Summary: Read the latest Real Python tutorials
 Author: Kasper Arfman
 Author-email: KasperArfman <kasper.arf@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Kasper Arfman
```

### Comparing `ntheory-0.0.5/pyproject.toml` & `ntheory-0.0.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "ntheory"
-version = "0.0.5"
+version = "0.0.6"
 description = "Read the latest Real Python tutorials"
 readme = "README.md"
 authors = [{ name = "KasperArfman", email = "kasper.arf@gmail.com" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
```

