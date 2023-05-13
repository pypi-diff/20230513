# Comparing `tmp/alacorder-80.4.91.tar.gz` & `tmp/alacorder-80.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "alacorder-80.4.91.tar", max compression
+gzip compressed data, was "alacorder-80.5.0.tar", max compression
```

## Comparing `alacorder-80.4.91.tar` & `alacorder-80.5.0.tar`

### file list

```diff
@@ -1,5 +1,8 @@
--rw-r--r--   0        0        0     1066 2023-02-07 05:47:31.000000 alacorder-80.4.91/LICENSE
--rw-r--r--   0        0        0     6592 2023-05-11 17:12:36.043202 alacorder-80.4.91/README.md
--rw-r--r--   0        0        0   218036 2023-05-13 17:06:43.893212 alacorder-80.4.91/alacorder.py
--rw-r--r--   0        0        0      747 2023-05-13 17:23:38.276435 alacorder-80.4.91/pyproject.toml
--rw-r--r--   0        0        0     7564 1970-01-01 00:00:00.000000 alacorder-80.4.91/PKG-INFO
+-rw-r--r--   0        0        0     1066 2023-02-07 05:47:31.000000 alacorder-80.5.0/LICENSE
+-rw-r--r--   0        0        0     6592 2023-05-11 17:12:36.043202 alacorder-80.5.0/README.md
+-rw-r--r--   0        0        0      746 2023-05-13 17:24:49.150698 alacorder-80.5.0/pyproject.toml
+-rw-r--r--   0        0        0     6148 2023-05-13 17:21:52.692111 alacorder-80.5.0/src/alacorder/.DS_Store
+-rw-r--r--   0        0        0        0 2023-05-02 17:21:37.916960 alacorder-80.5.0/src/alacorder/__init__.py
+-rw-r--r--   0        0        0   218037 2023-05-13 17:24:31.186328 alacorder-80.5.0/src/alacorder/__main__.py
+-rw-r--r--   0        0        0   218037 2023-05-13 17:24:35.983482 alacorder-80.5.0/src/alacorder/alac.py
+-rw-r--r--   0        0        0     7563 1970-01-01 00:00:00.000000 alacorder-80.5.0/PKG-INFO
```

### Comparing `alacorder-80.4.91/LICENSE` & `alacorder-80.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.91/README.md` & `alacorder-80.5.0/README.md`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.91/alacorder.py` & `alacorder-80.5.0/src/alacorder/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,17 +13,17 @@
 Optional dependencies:
     pyarrow required to export summary to .xls, .xlsx,
     Google Chrome required to fetch cases from Alacourt
 """
 
 name = "ALACORDER"
 long_version = "snowpalace"
-version = "80.4.8"
+version = "80.5.0"
 
-_autoload_graphical_user_interface = True
+_autoload_graphical_user_interface = False
 
 import polars as pl
 import os, sys, time, glob, re, math
 import click, fitz, selenium, xlsxwriter
 from tqdm.auto import tqdm
 from random import sample
 from datetime import datetime
```

### Comparing `alacorder-80.4.91/pyproject.toml` & `alacorder-80.5.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "alacorder"
-version = "80.4.91"
+version = "80.5.0"
 description = "Alacorder collects and processes Alacourt case detail PDFs into data tables suitable for research purposes."
 authors = ["Sam Robson <sbrobson@crimson.ua.edu>"]
 license = "MIT LICENSE"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.9"
```

### Comparing `alacorder-80.4.91/PKG-INFO` & `alacorder-80.5.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: alacorder
-Version: 80.4.91
+Version: 80.5.0
 Summary: Alacorder collects and processes Alacourt case detail PDFs into data tables suitable for research purposes.
 License: MIT
 Author: Sam Robson
 Author-email: sbrobson@crimson.ua.edu
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

