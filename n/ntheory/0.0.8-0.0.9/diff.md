# Comparing `tmp/ntheory-0.0.8.tar.gz` & `tmp/ntheory-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ntheory-0.0.8.tar", last modified: Sat May 13 12:45:34 2023, max compression
+gzip compressed data, was "ntheory-0.0.9.tar", last modified: Sat May 13 15:26:19 2023, max compression
```

## Comparing `ntheory-0.0.8.tar` & `ntheory-0.0.9.tar`

### file list

```diff
@@ -1,30 +1,37 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.215329 ntheory-0.0.8/
--rw-rw-rw-   0        0        0     1090 2023-05-12 21:31:16.000000 ntheory-0.0.8/LICENSE
--rw-rw-rw-   0        0        0     1797 2023-05-13 12:45:34.214330 ntheory-0.0.8/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-05-12 21:37:10.000000 ntheory-0.0.8/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.114597 ntheory-0.0.8/ntheory/
--rw-rw-rw-   0        0        0        0 2023-05-13 12:02:50.000000 ntheory-0.0.8/ntheory/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.189396 ntheory-0.0.8/ntheory/binary/
--rw-rw-rw-   0        0        0       24 2023-05-13 12:03:00.000000 ntheory-0.0.8/ntheory/binary/__init__.py
--rw-rw-rw-   0        0        0       66 2023-05-12 22:44:30.000000 ntheory-0.0.8/ntheory/binary/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.197375 ntheory-0.0.8/ntheory/modulo/
--rw-rw-rw-   0        0        0       91 2023-05-13 12:02:55.000000 ntheory-0.0.8/ntheory/modulo/__init__.py
--rw-rw-rw-   0        0        0     1318 2023-05-12 23:27:19.000000 ntheory-0.0.8/ntheory/modulo/modular_arithmetic.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.202364 ntheory-0.0.8/ntheory/primes/
--rw-rw-rw-   0        0        0        0 2023-05-13 12:03:26.000000 ntheory-0.0.8/ntheory/primes/__init__.py
--rw-rw-rw-   0        0        0      441 2023-05-13 12:03:23.000000 ntheory-0.0.8/ntheory/primes/prime_factors.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.184409 ntheory-0.0.8/ntheory.egg-info/
--rw-rw-rw-   0        0        0     1797 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      516 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       52 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      120 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/requires.txt
--rw-rw-rw-   0        0        0       14 2023-05-13 12:45:34.000000 ntheory-0.0.8/ntheory.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      909 2023-05-13 12:44:37.000000 ntheory-0.0.8/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-13 12:45:34.216326 ntheory-0.0.8/setup.cfg
--rw-rw-rw-   0        0        0      385 2023-05-13 12:45:28.000000 ntheory-0.0.8/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.205354 ntheory-0.0.8/tests/
--rw-rw-rw-   0        0        0        0 2023-05-12 21:39:23.000000 ntheory-0.0.8/tests/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:45:34.211337 ntheory-0.0.8/tests/test_modulo/
--rw-rw-rw-   0        0        0        0 2023-05-12 22:45:29.000000 ntheory-0.0.8/tests/test_modulo/__init__.py
--rw-rw-rw-   0        0        0      776 2023-05-12 23:01:02.000000 ntheory-0.0.8/tests/test_modulo/test_modular_arithmetic.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.148609 ntheory-0.0.9/
+-rw-rw-rw-   0        0        0     1090 2023-05-12 21:31:16.000000 ntheory-0.0.9/LICENSE
+-rw-rw-rw-   0        0        0     1797 2023-05-13 15:26:19.147612 ntheory-0.0.9/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-05-12 21:37:10.000000 ntheory-0.0.9/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.004007 ntheory-0.0.9/ntheory/
+-rw-rw-rw-   0        0        0      111 2023-05-13 15:25:40.000000 ntheory-0.0.9/ntheory/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.102732 ntheory-0.0.9/ntheory/binary/
+-rw-rw-rw-   0        0        0       34 2023-05-13 12:55:46.000000 ntheory-0.0.9/ntheory/binary/__init__.py
+-rw-rw-rw-   0        0        0       66 2023-05-12 22:44:30.000000 ntheory-0.0.9/ntheory/binary/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.110710 ntheory-0.0.9/ntheory/core/
+-rw-rw-rw-   0        0        0        0 2023-05-13 13:18:41.000000 ntheory-0.0.9/ntheory/core/__init__.py
+-rw-rw-rw-   0        0        0      894 2023-05-13 13:21:04.000000 ntheory-0.0.9/ntheory/core/tmp.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.119687 ntheory-0.0.9/ntheory/modulo/
+-rw-rw-rw-   0        0        0      103 2023-05-13 12:57:10.000000 ntheory-0.0.9/ntheory/modulo/__init__.py
+-rw-rw-rw-   0        0        0     1242 2023-05-13 13:16:20.000000 ntheory-0.0.9/ntheory/modulo/modular_arithmetic.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.129661 ntheory-0.0.9/ntheory/primes/
+-rw-rw-rw-   0        0        0       76 2023-05-13 15:24:58.000000 ntheory-0.0.9/ntheory/primes/__init__.py
+-rw-rw-rw-   0        0        0      437 2023-05-13 13:23:28.000000 ntheory-0.0.9/ntheory/primes/factors.py
+-rw-rw-rw-   0        0        0      632 2023-05-13 15:24:23.000000 ntheory-0.0.9/ntheory/primes/primes_range.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.091763 ntheory-0.0.9/ntheory.egg-info/
+-rw-rw-rw-   0        0        0     1797 2023-05-13 15:26:18.000000 ntheory-0.0.9/ntheory.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      650 2023-05-13 15:26:18.000000 ntheory-0.0.9/ntheory.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 15:26:18.000000 ntheory-0.0.9/ntheory.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       52 2023-05-13 15:26:18.000000 ntheory-0.0.9/ntheory.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      120 2023-05-13 15:26:18.000000 ntheory-0.0.9/ntheory.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-05-13 15:26:18.000000 ntheory-0.0.9/ntheory.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      909 2023-05-13 15:25:46.000000 ntheory-0.0.9/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 15:26:19.149613 ntheory-0.0.9/setup.cfg
+-rw-rw-rw-   0        0        0      385 2023-05-13 12:46:22.000000 ntheory-0.0.9/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.132667 ntheory-0.0.9/tests/
+-rw-rw-rw-   0        0        0        0 2023-05-12 21:39:23.000000 ntheory-0.0.9/tests/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.137639 ntheory-0.0.9/tests/test_modulo/
+-rw-rw-rw-   0        0        0        0 2023-05-12 22:45:29.000000 ntheory-0.0.9/tests/test_modulo/__init__.py
+-rw-rw-rw-   0        0        0      776 2023-05-13 13:16:11.000000 ntheory-0.0.9/tests/test_modulo/test_modular_arithmetic.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:26:19.143622 ntheory-0.0.9/tests/test_primes/
+-rw-rw-rw-   0        0        0        0 2023-05-13 13:00:58.000000 ntheory-0.0.9/tests/test_primes/__init__.py
+-rw-rw-rw-   0        0        0      262 2023-05-13 13:14:55.000000 ntheory-0.0.9/tests/test_primes/test_factors.py
```

### Comparing `ntheory-0.0.8/LICENSE` & `ntheory-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `ntheory-0.0.8/PKG-INFO` & `ntheory-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ntheory
-Version: 0.0.8
+Version: 0.0.9
 Summary: Read the latest Real Python tutorials
 Author: Kasper Arfman
 Author-email: KasperArfman <kasper.arf@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Kasper Arfman
```

### Comparing `ntheory-0.0.8/ntheory/modulo/modular_arithmetic.py` & `ntheory-0.0.9/ntheory/modulo/modular_arithmetic.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,10 @@
-
 from ..binary import binary_digits
 
 
-# def binary_digits(num):
-#     return list(map(int, bin(num)[2:]))
-
-
 def modular_sum(*args, mod):
     """Compute (a+b)%modulo"""
     r = 0
     for x in args:
         r = (r + x) % mod
     return r
```

### Comparing `ntheory-0.0.8/ntheory.egg-info/PKG-INFO` & `ntheory-0.0.9/ntheory.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ntheory
-Version: 0.0.8
+Version: 0.0.9
 Summary: Read the latest Real Python tutorials
 Author: Kasper Arfman
 Author-email: KasperArfman <kasper.arf@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Kasper Arfman
```

### Comparing `ntheory-0.0.8/ntheory.egg-info/SOURCES.txt` & `ntheory-0.0.9/ntheory.egg-info/SOURCES.txt`

 * *Files 24% similar despite different names*

```diff
@@ -7,14 +7,19 @@
 ntheory.egg-info/SOURCES.txt
 ntheory.egg-info/dependency_links.txt
 ntheory.egg-info/entry_points.txt
 ntheory.egg-info/requires.txt
 ntheory.egg-info/top_level.txt
 ntheory/binary/__init__.py
 ntheory/binary/utils.py
+ntheory/core/__init__.py
+ntheory/core/tmp.py
 ntheory/modulo/__init__.py
 ntheory/modulo/modular_arithmetic.py
 ntheory/primes/__init__.py
-ntheory/primes/prime_factors.py
+ntheory/primes/factors.py
+ntheory/primes/primes_range.py
 tests/__init__.py
 tests/test_modulo/__init__.py
-tests/test_modulo/test_modular_arithmetic.py
+tests/test_modulo/test_modular_arithmetic.py
+tests/test_primes/__init__.py
+tests/test_primes/test_factors.py
```

### Comparing `ntheory-0.0.8/pyproject.toml` & `ntheory-0.0.9/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "ntheory"
-version = "0.0.8"
+version = "0.0.9"
 description = "Read the latest Real Python tutorials"
 readme = "README.md"
 authors = [{ name = "KasperArfman", email = "kasper.arf@gmail.com" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
```

### Comparing `ntheory-0.0.8/tests/test_modulo/test_modular_arithmetic.py` & `ntheory-0.0.9/tests/test_modulo/test_modular_arithmetic.py`

 * *Files identical despite different names*

