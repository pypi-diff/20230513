# Comparing `tmp/ntheory-0.0.7.tar.gz` & `tmp/ntheory-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ntheory-0.0.7.tar", last modified: Sat May 13 12:05:23 2023, max compression
+gzip compressed data, was "ntheory-0.0.8.tar", last modified: Sat May 13 12:45:34 2023, max compression
```

## Comparing `ntheory-0.0.7.tar` & `ntheory-0.0.8.tar`

### file list

```diff
@@ -1,16 +1,30 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 12:05:23.538159 ntheory-0.0.7/
--rw-rw-rw-   0        0        0     1090 2023-05-12 21:31:16.000000 ntheory-0.0.7/LICENSE
--rw-rw-rw-   0        0        0     1797 2023-05-13 12:05:23.537162 ntheory-0.0.7/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-05-12 21:37:10.000000 ntheory-0.0.7/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 12:05:23.473333 ntheory-0.0.7/ntheory/
--rw-rw-rw-   0        0        0        0 2023-05-13 12:02:50.000000 ntheory-0.0.7/ntheory/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:05:23.534172 ntheory-0.0.7/ntheory.egg-info/
--rw-rw-rw-   0        0        0     1797 2023-05-13 12:05:23.000000 ntheory-0.0.7/ntheory.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      249 2023-05-13 12:05:23.000000 ntheory-0.0.7/ntheory.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 12:05:23.000000 ntheory-0.0.7/ntheory.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       52 2023-05-13 12:05:23.000000 ntheory-0.0.7/ntheory.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      120 2023-05-13 12:05:23.000000 ntheory-0.0.7/ntheory.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-13 12:05:23.000000 ntheory-0.0.7/ntheory.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      909 2023-05-13 12:04:59.000000 ntheory-0.0.7/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-13 12:05:23.538159 ntheory-0.0.7/setup.cfg
--rw-rw-rw-   0        0        0      404 2023-05-12 22:33:56.000000 ntheory-0.0.7/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.215329 ntheory-0.0.8/
+-rw-rw-rw-   0        0        0     1090 2023-05-12 21:31:16.000000 ntheory-0.0.8/LICENSE
+-rw-rw-rw-   0        0        0     1797 2023-05-13 12:45:34.214330 ntheory-0.0.8/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-05-12 21:37:10.000000 ntheory-0.0.8/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.114597 ntheory-0.0.8/ntheory/
+-rw-rw-rw-   0        0        0        0 2023-05-13 12:02:50.000000 ntheory-0.0.8/ntheory/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.189396 ntheory-0.0.8/ntheory/binary/
+-rw-rw-rw-   0        0        0       24 2023-05-13 12:03:00.000000 ntheory-0.0.8/ntheory/binary/__init__.py
+-rw-rw-rw-   0        0        0       66 2023-05-12 22:44:30.000000 ntheory-0.0.8/ntheory/binary/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.197375 ntheory-0.0.8/ntheory/modulo/
+-rw-rw-rw-   0        0        0       91 2023-05-13 12:02:55.000000 ntheory-0.0.8/ntheory/modulo/__init__.py
+-rw-rw-rw-   0        0        0     1318 2023-05-12 23:27:19.000000 ntheory-0.0.8/ntheory/modulo/modular_arithmetic.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.202364 ntheory-0.0.8/ntheory/primes/
+-rw-rw-rw-   0        0        0        0 2023-05-13 12:03:26.000000 ntheory-0.0.8/ntheory/primes/__init__.py
+-rw-rw-rw-   0        0        0      441 2023-05-13 12:03:23.000000 ntheory-0.0.8/ntheory/primes/prime_factors.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.184409 ntheory-0.0.8/ntheory.egg-info/
+-rw-rw-rw-   0        0        0     1797 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      516 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       52 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      120 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      909 2023-05-13 12:44:37.000000 ntheory-0.0.8/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 12:45:34.216326 ntheory-0.0.8/setup.cfg
+-rw-rw-rw-   0        0        0      385 2023-05-13 12:45:28.000000 ntheory-0.0.8/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.205354 ntheory-0.0.8/tests/
+-rw-rw-rw-   0        0        0        0 2023-05-12 21:39:23.000000 ntheory-0.0.8/tests/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.211337 ntheory-0.0.8/tests/test_modulo/
+-rw-rw-rw-   0        0        0        0 2023-05-12 22:45:29.000000 ntheory-0.0.8/tests/test_modulo/__init__.py
+-rw-rw-rw-   0        0        0      776 2023-05-12 23:01:02.000000 ntheory-0.0.8/tests/test_modulo/test_modular_arithmetic.py
```

### Comparing `ntheory-0.0.7/LICENSE` & `ntheory-0.0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `ntheory-0.0.7/PKG-INFO` & `ntheory-0.0.8/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ntheory
-Version: 0.0.7
+Version: 0.0.8
 Summary: Read the latest Real Python tutorials
 Author: Kasper Arfman
 Author-email: KasperArfman <kasper.arf@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Kasper Arfman
```

### Comparing `ntheory-0.0.7/ntheory.egg-info/PKG-INFO` & `ntheory-0.0.8/ntheory.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ntheory
-Version: 0.0.7
+Version: 0.0.8
 Summary: Read the latest Real Python tutorials
 Author: Kasper Arfman
 Author-email: KasperArfman <kasper.arf@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Kasper Arfman
```

### Comparing `ntheory-0.0.7/pyproject.toml` & `ntheory-0.0.8/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "ntheory"
-version = "0.0.7"
+version = "0.0.8"
 description = "Read the latest Real Python tutorials"
 readme = "README.md"
 authors = [{ name = "KasperArfman", email = "kasper.arf@gmail.com" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
```

