# Comparing `tmp/beewi_smartclim_ble-0.0.5.tar.gz` & `tmp/beewi_smartclim_ble-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "beewi_smartclim_ble-0.0.5.tar", max compression
+gzip compressed data, was "beewi_smartclim_ble-0.1.0.tar", max compression
```

## Comparing `beewi_smartclim_ble-0.0.5.tar` & `beewi_smartclim_ble-0.1.0.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0     1067 2023-05-09 10:00:56.448175 beewi_smartclim_ble-0.0.5/LICENSE
--rw-r--r--   0        0        0      103 2023-05-13 20:49:03.998583 beewi_smartclim_ble-0.0.5/README.md
--rw-r--r--   0        0        0     2256 2023-05-13 20:22:24.847406 beewi_smartclim_ble-0.0.5/pyproject.toml
--rw-r--r--   0        0        0      101 2023-05-12 08:34:10.858126 beewi_smartclim_ble-0.0.5/src/smartclim_ble/__init__.py
--rw-r--r--   0        0        0     6718 2023-05-13 20:22:24.851408 beewi_smartclim_ble-0.0.5/src/smartclim_ble/parser.py
--rw-r--r--   0        0        0        0 2023-05-10 09:24:36.332678 beewi_smartclim_ble-0.0.5/src/smartclim_ble/py.typed
--rw-r--r--   0        0        0     1377 1970-01-01 00:00:00.000000 beewi_smartclim_ble-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-05-09 10:00:56.448175 beewi_smartclim_ble-0.1.0/LICENSE
+-rw-r--r--   0        0        0     2477 2023-05-13 21:19:58.053147 beewi_smartclim_ble-0.1.0/README.md
+-rw-r--r--   0        0        0     2256 2023-05-13 21:19:58.053147 beewi_smartclim_ble-0.1.0/pyproject.toml
+-rw-r--r--   0        0        0      101 2023-05-13 21:19:58.053147 beewi_smartclim_ble-0.1.0/src/smartclim_ble/__init__.py
+-rw-r--r--   0        0        0     6718 2023-05-13 20:22:24.851408 beewi_smartclim_ble-0.1.0/src/smartclim_ble/parser.py
+-rw-r--r--   0        0        0        0 2023-05-10 09:24:36.332678 beewi_smartclim_ble-0.1.0/src/smartclim_ble/py.typed
+-rw-r--r--   0        0        0     3751 1970-01-01 00:00:00.000000 beewi_smartclim_ble-0.1.0/PKG-INFO
```

### Comparing `beewi_smartclim_ble-0.0.5/LICENSE` & `beewi_smartclim_ble-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `beewi_smartclim_ble-0.0.5/pyproject.toml` & `beewi_smartclim_ble-0.1.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "beewi-smartclim-ble"
-version = "0.0.5"
+version = "0.1.0"
 description = "Parser for the BeeWi SmartClim device"
 authors = ["f-davin <none@none.com>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/f-davin/hassis_beewi_smartclim.git"
 classifiers = [
     "Development Status :: 1 - Planning",
```

### Comparing `beewi_smartclim_ble-0.0.5/src/smartclim_ble/parser.py` & `beewi_smartclim_ble-0.1.0/src/smartclim_ble/parser.py`

 * *Files identical despite different names*

