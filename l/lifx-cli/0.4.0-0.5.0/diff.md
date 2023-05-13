# Comparing `tmp/lifx_cli-0.4.0.tar.gz` & `tmp/lifx_cli-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lifx_cli-0.4.0.tar", max compression
+gzip compressed data, was "lifx_cli-0.5.0.tar", max compression
```

## Comparing `lifx_cli-0.4.0.tar` & `lifx_cli-0.5.0.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0     1070 2023-04-28 01:37:25.530395 lifx_cli-0.4.0/LICENSE
--rw-r--r--   0        0        0     1734 2023-05-12 19:29:07.003049 lifx_cli-0.4.0/README.md
--rwxr-xr-x   0        0        0    10047 2023-05-12 22:27:11.987268 lifx_cli-0.4.0/lifx
--rw-r--r--   0        0        0      505 2023-05-13 02:29:48.979604 lifx_cli-0.4.0/pyproject.toml
--rw-r--r--   0        0        0     2370 1970-01-01 00:00:00.000000 lifx_cli-0.4.0/PKG-INFO
+-rw-r--r--   0        0        0     1070 2023-04-28 01:37:25.530395 lifx_cli-0.5.0/LICENSE
+-rw-r--r--   0        0        0     1734 2023-05-12 19:29:07.003049 lifx_cli-0.5.0/README.md
+-rwxr-xr-x   0        0        0    10047 2023-05-12 22:27:11.987268 lifx_cli-0.5.0/lifx
+-rw-r--r--   0        0        0      501 2023-05-13 02:30:49.852562 lifx_cli-0.5.0/pyproject.toml
+-rw-r--r--   0        0        0     2370 1970-01-01 00:00:00.000000 lifx_cli-0.5.0/PKG-INFO
```

### Comparing `lifx_cli-0.4.0/LICENSE` & `lifx_cli-0.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.4.0/README.md` & `lifx_cli-0.5.0/README.md`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.4.0/lifx` & `lifx_cli-0.5.0/lifx`

 * *Files identical despite different names*

### Comparing `lifx_cli-0.4.0/PKG-INFO` & `lifx_cli-0.5.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lifx-cli
-Version: 0.4.0
+Version: 0.5.0
 Summary: The Unofficial LIFX CLI
 Home-page: https://github.com/necrux/lifx-cli
 License: MIT
 Keywords: LIFX,lifx-cli
 Author: Wes Henderson
 Author-email: info@necrux.com
 Requires-Python: >=3.10,<4.0
```

