# Comparing `tmp/ntheory-0.0.3.tar.gz` & `tmp/ntheory-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ntheory-0.0.3.tar", last modified: Fri May 12 22:35:31 2023, max compression
+gzip compressed data, was "ntheory-0.0.4.tar", last modified: Fri May 12 23:07:50 2023, max compression
```

## Comparing `ntheory-0.0.3.tar` & `ntheory-0.0.4.tar`

### file list

```diff
@@ -1,19 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 22:35:31.012322 ntheory-0.0.3/
--rw-rw-rw-   0        0        0     1090 2023-05-12 21:31:16.000000 ntheory-0.0.3/LICENSE
--rw-rw-rw-   0        0        0     1797 2023-05-12 22:35:31.011314 ntheory-0.0.3/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-05-12 21:37:10.000000 ntheory-0.0.3/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 22:35:30.950477 ntheory-0.0.3/ntheory/
--rw-rw-rw-   0        0        0       22 2023-05-12 21:45:43.000000 ntheory-0.0.3/ntheory/__init__.py
--rw-rw-rw-   0        0        0       80 2023-05-12 22:27:15.000000 ntheory-0.0.3/ntheory/greet.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:35:31.004333 ntheory-0.0.3/ntheory.egg-info/
--rw-rw-rw-   0        0        0     1797 2023-05-12 22:35:30.000000 ntheory-0.0.3/ntheory.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      286 2023-05-12 22:35:30.000000 ntheory-0.0.3/ntheory.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 22:35:30.000000 ntheory-0.0.3/ntheory.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       52 2023-05-12 22:35:30.000000 ntheory-0.0.3/ntheory.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      120 2023-05-12 22:35:30.000000 ntheory-0.0.3/ntheory.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-12 22:35:30.000000 ntheory-0.0.3/ntheory.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      909 2023-05-12 22:34:43.000000 ntheory-0.0.3/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-12 22:35:31.013308 ntheory-0.0.3/setup.cfg
--rw-rw-rw-   0        0        0      404 2023-05-12 22:33:56.000000 ntheory-0.0.3/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:35:31.008327 ntheory-0.0.3/tests/
--rw-rw-rw-   0        0        0       79 2023-05-12 21:45:00.000000 ntheory-0.0.3/tests/test_greet.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:07:50.637220 ntheory-0.0.4/
+-rw-rw-rw-   0        0        0     1090 2023-05-12 21:31:16.000000 ntheory-0.0.4/LICENSE
+-rw-rw-rw-   0        0        0     1797 2023-05-12 23:07:50.635226 ntheory-0.0.4/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-05-12 21:37:10.000000 ntheory-0.0.4/README.md
+drwxrwxrwx   0        0        0        0 2023-05-12 23:07:50.583369 ntheory-0.0.4/ntheory/
+-rw-rw-rw-   0        0        0       25 2023-05-12 23:00:06.000000 ntheory-0.0.4/ntheory/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:07:50.632234 ntheory-0.0.4/ntheory.egg-info/
+-rw-rw-rw-   0        0        0     1797 2023-05-12 23:07:50.000000 ntheory-0.0.4/ntheory.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      249 2023-05-12 23:07:50.000000 ntheory-0.0.4/ntheory.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-12 23:07:50.000000 ntheory-0.0.4/ntheory.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       52 2023-05-12 23:07:50.000000 ntheory-0.0.4/ntheory.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      120 2023-05-12 23:07:50.000000 ntheory-0.0.4/ntheory.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-12 23:07:50.000000 ntheory-0.0.4/ntheory.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      909 2023-05-12 23:07:26.000000 ntheory-0.0.4/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-12 23:07:50.637220 ntheory-0.0.4/setup.cfg
+-rw-rw-rw-   0        0        0      404 2023-05-12 22:33:56.000000 ntheory-0.0.4/setup.py
```

### Comparing `ntheory-0.0.3/LICENSE` & `ntheory-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `ntheory-0.0.3/PKG-INFO` & `ntheory-0.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ntheory
-Version: 0.0.3
+Version: 0.0.4
 Summary: Read the latest Real Python tutorials
 Author: Kasper Arfman
 Author-email: KasperArfman <kasper.arf@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Kasper Arfman
```

### Comparing `ntheory-0.0.3/ntheory.egg-info/PKG-INFO` & `ntheory-0.0.4/ntheory.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ntheory
-Version: 0.0.3
+Version: 0.0.4
 Summary: Read the latest Real Python tutorials
 Author: Kasper Arfman
 Author-email: KasperArfman <kasper.arf@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Kasper Arfman
```

### Comparing `ntheory-0.0.3/pyproject.toml` & `ntheory-0.0.4/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "ntheory"
-version = "0.0.3"
+version = "0.0.4"
 description = "Read the latest Real Python tutorials"
 readme = "README.md"
 authors = [{ name = "KasperArfman", email = "kasper.arf@gmail.com" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
```

