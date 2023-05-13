# Comparing `tmp/lifx_cli-0.2.0.tar.gz` & `tmp/lifx_cli-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lifx_cli-0.2.0.tar", max compression
+gzip compressed data, was "lifx_cli-0.3.0.tar", max compression
```

## Comparing `lifx_cli-0.2.0.tar` & `lifx_cli-0.3.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0     1070 2023-04-28 01:37:25.530395 lifx_cli-0.2.0/LICENSE
--rw-r--r--   0        0        0     1734 2023-05-12 19:29:07.003049 lifx_cli-0.2.0/README.md
--rw-r--r--   0        0        0      418 2023-05-13 01:59:35.383068 lifx_cli-0.2.0/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-13 00:17:00.154648 lifx_cli-0.2.0/src/__init__.py
--rwxr-xr-x   0        0        0     1847 2023-05-12 15:55:35.323908 lifx_cli-0.2.0/src/auth.py
--rw-r--r--   0        0        0     1773 2023-05-12 18:38:54.871775 lifx_cli-0.2.0/src/colors.py
--rwxr-xr-x   0        0        0     1026 2023-05-12 03:58:54.184422 lifx_cli-0.2.0/src/devices.py
--rwxr-xr-x   0        0        0    10047 2023-05-12 22:27:11.987268 lifx_cli-0.2.0/src/lifx.py
--rwxr-xr-x   0        0        0     3499 2023-05-12 17:14:54.776308 lifx_cli-0.2.0/src/lights.py
--rwxr-xr-x   0        0        0      946 2023-05-12 04:01:42.847083 lifx_cli-0.2.0/src/scenes.py
--rw-r--r--   0        0        0     2240 1970-01-01 00:00:00.000000 lifx_cli-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0     1070 2023-04-28 01:37:25.530395 lifx_cli-0.3.0/LICENSE
+-rw-r--r--   0        0        0     1734 2023-05-12 19:29:07.003049 lifx_cli-0.3.0/README.md
+-rw-r--r--   0        0        0      422 2023-05-13 02:12:21.203099 lifx_cli-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-13 00:17:00.154648 lifx_cli-0.3.0/src/__init__.py
+-rwxr-xr-x   0        0        0     1847 2023-05-12 15:55:35.323908 lifx_cli-0.3.0/src/auth.py
+-rw-r--r--   0        0        0     1773 2023-05-12 18:38:54.871775 lifx_cli-0.3.0/src/colors.py
+-rwxr-xr-x   0        0        0     1026 2023-05-12 03:58:54.184422 lifx_cli-0.3.0/src/devices.py
+-rwxr-xr-x   0        0        0    10047 2023-05-12 22:27:11.987268 lifx_cli-0.3.0/src/lifx.py
+-rwxr-xr-x   0        0        0     3499 2023-05-12 17:14:54.776308 lifx_cli-0.3.0/src/lights.py
+-rwxr-xr-x   0        0        0      946 2023-05-12 04:01:42.847083 lifx_cli-0.3.0/src/scenes.py
+-rw-r--r--   0        0        0     2240 1970-01-01 00:00:00.000000 lifx_cli-0.3.0/PKG-INFO
```

### Comparing `lifx_cli-0.2.0/LICENSE` & `lifx_cli-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.2.0/README.md` & `lifx_cli-0.3.0/README.md`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.2.0/src/auth.py` & `lifx_cli-0.3.0/src/auth.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.2.0/src/colors.py` & `lifx_cli-0.3.0/src/colors.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.2.0/src/devices.py` & `lifx_cli-0.3.0/src/devices.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.2.0/src/lifx.py` & `lifx_cli-0.3.0/src/lifx.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.2.0/src/lights.py` & `lifx_cli-0.3.0/src/lights.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.2.0/src/scenes.py` & `lifx_cli-0.3.0/src/scenes.py`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.2.0/PKG-INFO` & `lifx_cli-0.3.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lifx-cli
-Version: 0.2.0
+Version: 0.3.0
 Summary: The Unofficial LIFX CLI
 License: MIT
 Author: Wes Henderson
 Author-email: info@necrux.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

