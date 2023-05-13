# Comparing `tmp/dash-connectivity-viewer-2.0.2.tar.gz` & `tmp/dash-connectivity-viewer-2.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dash-connectivity-viewer-2.0.2.tar", last modified: Fri May 12 20:31:58 2023, max compression
+gzip compressed data, was "dash-connectivity-viewer-2.0.3.tar", last modified: Fri May 12 20:42:00 2023, max compression
```

## Comparing `dash-connectivity-viewer-2.0.2.tar` & `dash-connectivity-viewer-2.0.3.tar`

### file list

```diff
@@ -1,51 +1,51 @@
-drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:31:58.536596 dash-connectivity-viewer-2.0.2/
--rw-r--r--   0 caseysm    (501) staff       (20)     1842 2023-05-09 18:49:42.000000 dash-connectivity-viewer-2.0.2/LICENSE.txt
--rw-r--r--   0 caseysm    (501) staff       (20)       71 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.2/MANIFEST.in
--rw-r--r--   0 caseysm    (501) staff       (20)      525 2023-05-12 20:31:58.536428 dash-connectivity-viewer-2.0.2/PKG-INFO
--rw-r--r--   0 caseysm    (501) staff       (20)      216 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.2/README.md
-drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:31:58.517652 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/
--rw-r--r--   0 caseysm    (501) staff       (20)       22 2023-05-12 20:31:47.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/__init__.py
-drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:31:58.525434 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/
--rw-r--r--   0 caseysm    (501) staff       (20)      568 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/__init__.py
--rw-r--r--   0 caseysm    (501) staff       (20)    24414 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/callbacks.py
--rw-r--r--   0 caseysm    (501) staff       (20)     5453 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/config.py
--rw-r--r--   0 caseysm    (501) staff       (20)     3461 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/cortex_panels.py
--rw-r--r--   0 caseysm    (501) staff       (20)     6156 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/cortex_plots.py
--rw-r--r--   0 caseysm    (501) staff       (20)       82 2023-03-18 18:57:32.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/external_stylesheets.py
--rw-r--r--   0 caseysm    (501) staff       (20)    20418 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/layout.py
--rw-r--r--   0 caseysm    (501) staff       (20)     4439 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/neuron_data_cortex.py
-drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:31:58.528204 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/
--rw-r--r--   0 caseysm    (501) staff       (20)      711 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/__init__.py
--rw-r--r--   0 caseysm    (501) staff       (20)    14456 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/callbacks.py
--rw-r--r--   0 caseysm    (501) staff       (20)     1347 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/config.py
--rw-r--r--   0 caseysm    (501) staff       (20)      210 2023-02-08 23:15:09.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/ct_utils.py
--rw-r--r--   0 caseysm    (501) staff       (20)    14861 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/layout.py
-drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:31:58.533715 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/
--rw-r--r--   0 caseysm    (501) staff       (20)       17 2023-04-13 06:43:13.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/__init__.py
--rw-r--r--   0 caseysm    (501) staff       (20)     5184 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/config.py
--rw-r--r--   0 caseysm    (501) staff       (20)     2914 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/dash_url_helper.py
-drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:31:58.534644 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/data/
--rw-r--r--   0 caseysm    (501) staff       (20)      144 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/data/height_bounds_v1.npy
--rw-r--r--   0 caseysm    (501) staff       (20)      168 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/data/layer_bounds_v1.npy
--rw-r--r--   0 caseysm    (501) staff       (20)    10103 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/dataframe_utilities.py
--rw-r--r--   0 caseysm    (501) staff       (20)      294 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/external_stylesheets.py
--rw-r--r--   0 caseysm    (501) staff       (20)    13477 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/link_utilities.py
--rw-r--r--   0 caseysm    (501) staff       (20)     4043 2023-04-25 19:19:28.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/lookup_utilities.py
--rw-r--r--   0 caseysm    (501) staff       (20)    11384 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/neuron_data_base.py
--rw-r--r--   0 caseysm    (501) staff       (20)     3756 2023-04-25 19:21:22.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/schema_utils.py
--rw-r--r--   0 caseysm    (501) staff       (20)     3950 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/table_lookup.py
--rw-r--r--   0 caseysm    (501) staff       (20)      762 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/transform_utils.py
-drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:31:58.536181 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/
--rw-r--r--   0 caseysm    (501) staff       (20)      591 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/__init__.py
--rw-r--r--   0 caseysm    (501) staff       (20)    13817 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/callbacks.py
--rw-r--r--   0 caseysm    (501) staff       (20)      523 2023-02-08 23:15:09.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/config.py
--rw-r--r--   0 caseysm    (501) staff       (20)     9093 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/layout.py
-drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:31:58.518728 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer.egg-info/
--rw-r--r--   0 caseysm    (501) staff       (20)      525 2023-05-12 20:31:58.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer.egg-info/PKG-INFO
--rw-r--r--   0 caseysm    (501) staff       (20)     1990 2023-05-12 20:31:58.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer.egg-info/SOURCES.txt
--rw-r--r--   0 caseysm    (501) staff       (20)        1 2023-05-12 20:31:58.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer.egg-info/dependency_links.txt
--rw-r--r--   0 caseysm    (501) staff       (20)      174 2023-05-12 20:31:58.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer.egg-info/requires.txt
--rw-r--r--   0 caseysm    (501) staff       (20)       25 2023-05-12 20:31:58.000000 dash-connectivity-viewer-2.0.2/dash_connectivity_viewer.egg-info/top_level.txt
--rw-r--r--   0 caseysm    (501) staff       (20)      173 2023-05-12 20:30:51.000000 dash-connectivity-viewer-2.0.2/requirements.txt
--rw-r--r--   0 caseysm    (501) staff       (20)       38 2023-05-12 20:31:58.536688 dash-connectivity-viewer-2.0.2/setup.cfg
--rw-r--r--   0 caseysm    (501) staff       (20)     1153 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.2/setup.py
+drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:42:00.591463 dash-connectivity-viewer-2.0.3/
+-rw-r--r--   0 caseysm    (501) staff       (20)     1842 2023-05-09 18:49:42.000000 dash-connectivity-viewer-2.0.3/LICENSE.txt
+-rw-r--r--   0 caseysm    (501) staff       (20)       71 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.3/MANIFEST.in
+-rw-r--r--   0 caseysm    (501) staff       (20)      525 2023-05-12 20:42:00.591299 dash-connectivity-viewer-2.0.3/PKG-INFO
+-rw-r--r--   0 caseysm    (501) staff       (20)      216 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.3/README.md
+drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:42:00.578749 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/
+-rw-r--r--   0 caseysm    (501) staff       (20)       22 2023-05-12 20:41:35.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/__init__.py
+drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:42:00.583502 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/
+-rw-r--r--   0 caseysm    (501) staff       (20)      568 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/__init__.py
+-rw-r--r--   0 caseysm    (501) staff       (20)    24414 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/callbacks.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     5453 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/config.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     3461 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/cortex_panels.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     6156 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/cortex_plots.py
+-rw-r--r--   0 caseysm    (501) staff       (20)       82 2023-03-18 18:57:32.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/external_stylesheets.py
+-rw-r--r--   0 caseysm    (501) staff       (20)    20418 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/layout.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     4439 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/neuron_data_cortex.py
+drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:42:00.586389 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/
+-rw-r--r--   0 caseysm    (501) staff       (20)      711 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/__init__.py
+-rw-r--r--   0 caseysm    (501) staff       (20)    14456 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/callbacks.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     1347 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/config.py
+-rw-r--r--   0 caseysm    (501) staff       (20)      210 2023-02-08 23:15:09.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/ct_utils.py
+-rw-r--r--   0 caseysm    (501) staff       (20)    14861 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/layout.py
+drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:42:00.589388 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/
+-rw-r--r--   0 caseysm    (501) staff       (20)       17 2023-04-13 06:43:13.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/__init__.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     5184 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/config.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     2914 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/dash_url_helper.py
+drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:42:00.589952 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/data/
+-rw-r--r--   0 caseysm    (501) staff       (20)      144 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/data/height_bounds_v1.npy
+-rw-r--r--   0 caseysm    (501) staff       (20)      168 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/data/layer_bounds_v1.npy
+-rw-r--r--   0 caseysm    (501) staff       (20)    10103 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/dataframe_utilities.py
+-rw-r--r--   0 caseysm    (501) staff       (20)      294 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/external_stylesheets.py
+-rw-r--r--   0 caseysm    (501) staff       (20)    13477 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/link_utilities.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     4043 2023-04-25 19:19:28.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/lookup_utilities.py
+-rw-r--r--   0 caseysm    (501) staff       (20)    11384 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/neuron_data_base.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     3756 2023-04-25 19:21:22.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/schema_utils.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     3950 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/table_lookup.py
+-rw-r--r--   0 caseysm    (501) staff       (20)      762 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/transform_utils.py
+drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:42:00.591014 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/
+-rw-r--r--   0 caseysm    (501) staff       (20)      591 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/__init__.py
+-rw-r--r--   0 caseysm    (501) staff       (20)    13817 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/callbacks.py
+-rw-r--r--   0 caseysm    (501) staff       (20)      523 2023-02-08 23:15:09.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/config.py
+-rw-r--r--   0 caseysm    (501) staff       (20)     9093 2023-04-13 06:41:46.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/layout.py
+drwxr-xr-x   0 caseysm    (501) staff       (20)        0 2023-05-12 20:42:00.580405 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer.egg-info/
+-rw-r--r--   0 caseysm    (501) staff       (20)      525 2023-05-12 20:42:00.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer.egg-info/PKG-INFO
+-rw-r--r--   0 caseysm    (501) staff       (20)     1990 2023-05-12 20:42:00.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer.egg-info/SOURCES.txt
+-rw-r--r--   0 caseysm    (501) staff       (20)        1 2023-05-12 20:42:00.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer.egg-info/dependency_links.txt
+-rw-r--r--   0 caseysm    (501) staff       (20)      174 2023-05-12 20:42:00.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer.egg-info/requires.txt
+-rw-r--r--   0 caseysm    (501) staff       (20)       25 2023-05-12 20:42:00.000000 dash-connectivity-viewer-2.0.3/dash_connectivity_viewer.egg-info/top_level.txt
+-rw-r--r--   0 caseysm    (501) staff       (20)      173 2023-05-12 20:41:16.000000 dash-connectivity-viewer-2.0.3/requirements.txt
+-rw-r--r--   0 caseysm    (501) staff       (20)       38 2023-05-12 20:42:00.591515 dash-connectivity-viewer-2.0.3/setup.cfg
+-rw-r--r--   0 caseysm    (501) staff       (20)     1153 2022-11-16 18:21:07.000000 dash-connectivity-viewer-2.0.3/setup.py
```

### Comparing `dash-connectivity-viewer-2.0.2/LICENSE.txt` & `dash-connectivity-viewer-2.0.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/PKG-INFO` & `dash-connectivity-viewer-2.0.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dash-connectivity-viewer
-Version: 2.0.2
+Version: 2.0.3
 Summary: Dash connectivity viewer for CAVE data
 Home-page: https://github.com/ceesem/dash-connectivity-viewer
 Author: Casey Schneider-Mizell
 Author-email: caseysm@gmail.com
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
```

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/__init__.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/__init__.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/callbacks.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/callbacks.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/config.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/config.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/cortex_panels.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/cortex_panels.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/cortex_plots.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/cortex_plots.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/layout.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/layout.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_connectivity/neuron_data_cortex.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_connectivity/neuron_data_cortex.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/__init__.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/__init__.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/callbacks.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/callbacks.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/config.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/config.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/cell_type_table/layout.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/cell_type_table/layout.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/config.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/config.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/dash_url_helper.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/dash_url_helper.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/dataframe_utilities.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/dataframe_utilities.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/link_utilities.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/link_utilities.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/lookup_utilities.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/lookup_utilities.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/neuron_data_base.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/neuron_data_base.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/schema_utils.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/schema_utils.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/table_lookup.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/table_lookup.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/common/transform_utils.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/common/transform_utils.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/__init__.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/__init__.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/callbacks.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/callbacks.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/config.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/config.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer/connectivity_table/layout.py` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer/connectivity_table/layout.py`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer.egg-info/PKG-INFO` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dash-connectivity-viewer
-Version: 2.0.2
+Version: 2.0.3
 Summary: Dash connectivity viewer for CAVE data
 Home-page: https://github.com/ceesem/dash-connectivity-viewer
 Author: Casey Schneider-Mizell
 Author-email: caseysm@gmail.com
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
```

### Comparing `dash-connectivity-viewer-2.0.2/dash_connectivity_viewer.egg-info/SOURCES.txt` & `dash-connectivity-viewer-2.0.3/dash_connectivity_viewer.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `dash-connectivity-viewer-2.0.2/setup.py` & `dash-connectivity-viewer-2.0.3/setup.py`

 * *Files identical despite different names*

