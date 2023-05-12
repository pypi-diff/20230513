# Comparing `tmp/lineagex-0.0.1a1.tar.gz` & `tmp/lineagex-0.0.2a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lineagex-0.0.1a1.tar", max compression
+gzip compressed data, was "lineagex-0.0.2a1.tar", max compression
```

## Comparing `lineagex-0.0.1a1.tar` & `lineagex-0.0.2a1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
--rw-r--r--   0        0        0       55 2023-05-12 01:58:21.769698 lineagex-0.0.1a1/lineagex/__init__.py
--rw-r--r--   0        0        0    54175 2023-04-22 19:33:20.371862 lineagex-0.0.1a1/lineagex/app.js
--rw-r--r--   0        0        0    34528 2023-05-12 01:56:56.456690 lineagex-0.0.1a1/lineagex/ColumnLineage.py
--rw-r--r--   0        0        0    17230 2023-05-11 22:25:23.093987 lineagex-0.0.1a1/lineagex/ColumnLineageNoConn.py
--rw-r--r--   0        0        0      974 2023-05-12 22:15:42.232574 lineagex-0.0.1a1/lineagex/lineagex.py
--rw-r--r--   0        0        0     2355 2023-05-12 02:16:08.034372 lineagex-0.0.1a1/lineagex/LineageXNoConn.py
--rw-r--r--   0        0        0     9896 2023-05-12 22:15:49.236456 lineagex-0.0.1a1/lineagex/LineageXWithConn.py
--rw-r--r--   0        0        0     6556 2023-05-12 02:16:38.442999 lineagex-0.0.1a1/lineagex/SqlToDict.py
--rw-r--r--   0        0        0     1460 2023-05-08 20:36:59.378380 lineagex-0.0.1a1/lineagex/stack.py
--rw-r--r--   0        0        0     6760 2023-05-11 19:49:20.736279 lineagex-0.0.1a1/lineagex/utils.py
--rw-r--r--   0        0        0  3761177 2023-04-22 19:33:20.645016 lineagex-0.0.1a1/lineagex/vendor.js
--rw-r--r--   0        0        0      449 2023-05-12 23:00:08.932473 lineagex-0.0.1a1/pyproject.toml
--rw-r--r--   0        0        0     3492 2023-05-12 22:58:42.152661 lineagex-0.0.1a1/README.md
--rw-r--r--   0        0        0     4192 1970-01-01 00:00:00.000000 lineagex-0.0.1a1/PKG-INFO
+-rw-r--r--   0        0        0       55 2023-05-12 01:58:21.769698 lineagex-0.0.2a1/lineagex/__init__.py
+-rw-r--r--   0        0        0    54175 2023-04-22 19:33:20.371862 lineagex-0.0.2a1/lineagex/app.js
+-rw-r--r--   0        0        0    34528 2023-05-12 01:56:56.456690 lineagex-0.0.2a1/lineagex/ColumnLineage.py
+-rw-r--r--   0        0        0    17230 2023-05-11 22:25:23.093987 lineagex-0.0.2a1/lineagex/ColumnLineageNoConn.py
+-rw-r--r--   0        0        0      974 2023-05-12 22:15:42.232574 lineagex-0.0.2a1/lineagex/lineagex.py
+-rw-r--r--   0        0        0     2355 2023-05-12 02:16:08.034372 lineagex-0.0.2a1/lineagex/LineageXNoConn.py
+-rw-r--r--   0        0        0     9896 2023-05-12 22:15:49.236456 lineagex-0.0.2a1/lineagex/LineageXWithConn.py
+-rw-r--r--   0        0        0     6556 2023-05-12 02:16:38.442999 lineagex-0.0.2a1/lineagex/SqlToDict.py
+-rw-r--r--   0        0        0     1460 2023-05-08 20:36:59.378380 lineagex-0.0.2a1/lineagex/stack.py
+-rw-r--r--   0        0        0     6760 2023-05-11 19:49:20.736279 lineagex-0.0.2a1/lineagex/utils.py
+-rw-r--r--   0        0        0  3761177 2023-04-22 19:33:20.645016 lineagex-0.0.2a1/lineagex/vendor.js
+-rw-r--r--   0        0        0      449 2023-05-12 23:06:59.162026 lineagex-0.0.2a1/pyproject.toml
+-rw-r--r--   0        0        0     3492 2023-05-12 22:58:42.152661 lineagex-0.0.2a1/README.md
+-rw-r--r--   0        0        0     4192 1970-01-01 00:00:00.000000 lineagex-0.0.2a1/PKG-INFO
```

### Comparing `lineagex-0.0.1a1/lineagex/app.js` & `lineagex-0.0.2a1/lineagex/app.js`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/ColumnLineage.py` & `lineagex-0.0.2a1/lineagex/ColumnLineage.py`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/ColumnLineageNoConn.py` & `lineagex-0.0.2a1/lineagex/ColumnLineageNoConn.py`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/lineagex.py` & `lineagex-0.0.2a1/lineagex/lineagex.py`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/LineageXNoConn.py` & `lineagex-0.0.2a1/lineagex/LineageXNoConn.py`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/LineageXWithConn.py` & `lineagex-0.0.2a1/lineagex/LineageXWithConn.py`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/SqlToDict.py` & `lineagex-0.0.2a1/lineagex/SqlToDict.py`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/stack.py` & `lineagex-0.0.2a1/lineagex/stack.py`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/utils.py` & `lineagex-0.0.2a1/lineagex/utils.py`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/lineagex/vendor.js` & `lineagex-0.0.2a1/lineagex/vendor.js`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/README.md` & `lineagex-0.0.2a1/README.md`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1a1/PKG-INFO` & `lineagex-0.0.2a1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lineagex
-Version: 0.0.1a1
+Version: 0.0.2a1
 Summary: A column lineage tool
 License: MIT
 Author: zshandy
 Author-email: zshandy@gmail.com
 Requires-Python: >=3.6,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

