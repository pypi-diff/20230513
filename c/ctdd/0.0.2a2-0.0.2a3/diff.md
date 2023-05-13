# Comparing `tmp/ctdd-0.0.2a2.tar.gz` & `tmp/ctdd-0.0.2a3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ctdd-0.0.2a2.tar", max compression
+gzip compressed data, was "ctdd-0.0.2a3.tar", max compression
```

## Comparing `ctdd-0.0.2a2.tar` & `ctdd-0.0.2a3.tar`

### file list

```diff
@@ -1,7 +1,10 @@
--rw-r--r--   0        0        0     1108 2023-05-03 17:25:05.122292 ctdd-0.0.2a2/LICENSE
--rw-r--r--   0        0        0     2025 2023-05-08 01:05:44.511002 ctdd-0.0.2a2/README.md
--rw-r--r--   0        0        0       28 2023-05-03 18:15:09.070117 ctdd-0.0.2a2/ctdd/__init__.py
--rw-r--r--   0        0        0       55 2023-05-03 18:26:42.187993 ctdd-0.0.2a2/ctdd/factory.py
--rw-r--r--   0        0        0     2450 2023-05-08 00:41:47.727104 ctdd-0.0.2a2/ctdd/tester.py
--rw-r--r--   0        0        0      738 2023-05-08 01:12:56.336365 ctdd-0.0.2a2/pyproject.toml
--rw-r--r--   0        0        0     2784 1970-01-01 00:00:00.000000 ctdd-0.0.2a2/PKG-INFO
+-rw-r--r--   0        0        0     1108 2023-05-03 17:25:05.122292 ctdd-0.0.2a3/LICENSE
+-rw-r--r--   0        0        0     2025 2023-05-08 01:05:44.511002 ctdd-0.0.2a3/README.md
+-rw-r--r--   0        0        0       65 2023-05-13 15:01:41.630543 ctdd-0.0.2a3/ctdd/__init__.py
+-rw-r--r--   0        0        0     3075 2023-05-13 14:24:30.101636 ctdd-0.0.2a3/ctdd/__main__.py
+-rw-r--r--   0        0        0     1167 2023-05-13 15:05:16.441656 ctdd-0.0.2a3/ctdd/ffi_factory.py
+-rw-r--r--   0        0        0     1780 2023-05-13 14:55:04.404025 ctdd-0.0.2a3/ctdd/mocker.py
+-rw-r--r--   0        0        0     2253 2023-05-13 15:00:31.125767 ctdd-0.0.2a3/ctdd/tester.py
+-rw-r--r--   0        0        0     2510 2023-05-13 15:04:05.896870 ctdd-0.0.2a3/ctdd/tester_state.py
+-rw-r--r--   0        0        0      738 2023-05-13 18:17:23.102739 ctdd-0.0.2a3/pyproject.toml
+-rw-r--r--   0        0        0     2784 1970-01-01 00:00:00.000000 ctdd-0.0.2a3/PKG-INFO
```

### Comparing `ctdd-0.0.2a2/LICENSE` & `ctdd-0.0.2a3/LICENSE`

 * *Files identical despite different names*

### Comparing `ctdd-0.0.2a2/README.md` & `ctdd-0.0.2a3/README.md`

 * *Files identical despite different names*

### Comparing `ctdd-0.0.2a2/pyproject.toml` & `ctdd-0.0.2a3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "ctdd"
-version = "0.0.2a2"
+version = "0.0.2a3"
 description = "C test-driven development framework implemented in Python"
 authors = [
   "WideOpenTech <fossie@wideopentech.co.uk>",
 ]
 readme = "README.md"
 classifiers = [
     "Programming Language :: Python :: 3",
```

### Comparing `ctdd-0.0.2a2/PKG-INFO` & `ctdd-0.0.2a3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ctdd
-Version: 0.0.2a2
+Version: 0.0.2a3
 Summary: C test-driven development framework implemented in Python
 Home-page: https://github.com/wideopensource/ctdd
 Author: WideOpenTech
 Author-email: fossie@wideopentech.co.uk
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

