# Comparing `tmp/yetl-framework-1.3.2.tar.gz` & `tmp/yetl-framework-1.3.2.dev1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "yetl-framework-1.3.2.tar", last modified: Fri May 12 20:06:31 2023, max compression
+gzip compressed data, was "yetl-framework-1.3.2.dev1.tar", last modified: Thu May 11 08:04:29 2023, max compression
```

## Comparing `yetl-framework-1.3.2.tar` & `yetl-framework-1.3.2.dev1.tar`

### file list

```diff
@@ -1,42 +1,42 @@
-drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-12 20:06:31.291136 yetl-framework-1.3.2/
--rw-r--r--   0 vsts      (1001) docker     (123)     5196 2023-05-12 20:06:31.291136 yetl-framework-1.3.2/PKG-INFO
--rw-r--r--   0 vsts      (1001) docker     (123)     4699 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/README.md
--rw-r--r--   0 vsts      (1001) docker     (123)       38 2023-05-12 20:06:31.291136 yetl-framework-1.3.2/setup.cfg
--rw-r--r--   0 vsts      (1001) docker     (123)     1112 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/setup.py
-drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-12 20:06:31.287136 yetl-framework-1.3.2/yetl/
--rw-r--r--   0 vsts      (1001) docker     (123)      473 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/__init__.py
--rw-r--r--   0 vsts      (1001) docker     (123)      895 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/__main__.py
-drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-12 20:06:31.287136 yetl-framework-1.3.2/yetl/cli/
--rw-r--r--   0 vsts      (1001) docker     (123)     2775 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/cli/_init.py
-drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-12 20:06:31.291136 yetl-framework-1.3.2/yetl/config/
--rw-r--r--   0 vsts      (1001) docker     (123)      558 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/__init__.py
--rw-r--r--   0 vsts      (1001) docker     (123)     2966 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_config.py
--rw-r--r--   0 vsts      (1001) docker     (123)     2007 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_decorators.py
--rw-r--r--   0 vsts      (1001) docker     (123)     2033 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_logging_config.py
--rw-r--r--   0 vsts      (1001) docker     (123)     1893 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_project.py
--rw-r--r--   0 vsts      (1001) docker     (123)     1163 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_spark_context.py
--rw-r--r--   0 vsts      (1001) docker     (123)      194 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_stage_type.py
--rw-r--r--   0 vsts      (1001) docker     (123)      303 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_table_mapping.py
--rw-r--r--   0 vsts      (1001) docker     (123)     7544 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_tables.py
--rw-r--r--   0 vsts      (1001) docker     (123)     5706 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_timeslice.py
--rw-r--r--   0 vsts      (1001) docker     (123)     5040 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/_utils.py
--rw-r--r--   0 vsts      (1001) docker     (123)    16393 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/deltalake.py
-drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-12 20:06:31.291136 yetl-framework-1.3.2/yetl/config/table/
--rw-r--r--   0 vsts      (1001) docker     (123)      381 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/table/__init__.py
--rw-r--r--   0 vsts      (1001) docker     (123)     4195 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/table/_deltalake.py
--rw-r--r--   0 vsts      (1001) docker     (123)     1162 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/table/_factory.py
--rw-r--r--   0 vsts      (1001) docker     (123)     4935 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/table/_read.py
--rw-r--r--   0 vsts      (1001) docker     (123)     3671 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/table/_table.py
--rw-r--r--   0 vsts      (1001) docker     (123)      114 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/table/_table_type.py
--rw-r--r--   0 vsts      (1001) docker     (123)      253 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/config/table/_write.py
-drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-12 20:06:31.291136 yetl-framework-1.3.2/yetl/workflow/
--rw-r--r--   0 vsts      (1001) docker     (123)      122 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/workflow/__init__.py
--rw-r--r--   0 vsts      (1001) docker     (123)     2596 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/workflow/_multi_threaded.py
--rw-r--r--   0 vsts      (1001) docker     (123)      495 2023-05-12 20:05:39.000000 yetl-framework-1.3.2/yetl/workflow/_notebook.py
-drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-12 20:06:31.291136 yetl-framework-1.3.2/yetl_framework.egg-info/
--rw-r--r--   0 vsts      (1001) docker     (123)     5196 2023-05-12 20:06:31.000000 yetl-framework-1.3.2/yetl_framework.egg-info/PKG-INFO
--rw-r--r--   0 vsts      (1001) docker     (123)      902 2023-05-12 20:06:31.000000 yetl-framework-1.3.2/yetl_framework.egg-info/SOURCES.txt
--rw-r--r--   0 vsts      (1001) docker     (123)        1 2023-05-12 20:06:31.000000 yetl-framework-1.3.2/yetl_framework.egg-info/dependency_links.txt
--rw-r--r--   0 vsts      (1001) docker     (123)        1 2023-05-12 20:06:31.000000 yetl-framework-1.3.2/yetl_framework.egg-info/not-zip-safe
--rw-r--r--   0 vsts      (1001) docker     (123)       29 2023-05-12 20:06:31.000000 yetl-framework-1.3.2/yetl_framework.egg-info/requires.txt
--rw-r--r--   0 vsts      (1001) docker     (123)        5 2023-05-12 20:06:31.000000 yetl-framework-1.3.2/yetl_framework.egg-info/top_level.txt
+drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-11 08:04:29.863536 yetl-framework-1.3.2.dev1/
+-rw-r--r--   0 vsts      (1001) docker     (123)     5201 2023-05-11 08:04:29.863536 yetl-framework-1.3.2.dev1/PKG-INFO
+-rw-r--r--   0 vsts      (1001) docker     (123)     4699 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/README.md
+-rw-r--r--   0 vsts      (1001) docker     (123)       38 2023-05-11 08:04:29.863536 yetl-framework-1.3.2.dev1/setup.cfg
+-rw-r--r--   0 vsts      (1001) docker     (123)     1117 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/setup.py
+drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-11 08:04:29.859536 yetl-framework-1.3.2.dev1/yetl/
+-rw-r--r--   0 vsts      (1001) docker     (123)      473 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/__init__.py
+-rw-r--r--   0 vsts      (1001) docker     (123)      895 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/__main__.py
+drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-11 08:04:29.859536 yetl-framework-1.3.2.dev1/yetl/cli/
+-rw-r--r--   0 vsts      (1001) docker     (123)     2775 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/cli/_init.py
+drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-11 08:04:29.859536 yetl-framework-1.3.2.dev1/yetl/config/
+-rw-r--r--   0 vsts      (1001) docker     (123)      558 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/__init__.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     2966 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_config.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     2007 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_decorators.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     2033 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_logging_config.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     1893 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_project.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     1163 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_spark_context.py
+-rw-r--r--   0 vsts      (1001) docker     (123)      194 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_stage_type.py
+-rw-r--r--   0 vsts      (1001) docker     (123)      303 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_table_mapping.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     7544 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_tables.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     5706 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_timeslice.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     5016 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/_utils.py
+-rw-r--r--   0 vsts      (1001) docker     (123)    16393 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/deltalake.py
+drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-11 08:04:29.859536 yetl-framework-1.3.2.dev1/yetl/config/table/
+-rw-r--r--   0 vsts      (1001) docker     (123)      381 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/table/__init__.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     4580 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/table/_deltalake.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     1162 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/table/_factory.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     5142 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/table/_read.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     3380 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/table/_table.py
+-rw-r--r--   0 vsts      (1001) docker     (123)      114 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/table/_table_type.py
+-rw-r--r--   0 vsts      (1001) docker     (123)      253 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/config/table/_write.py
+drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-11 08:04:29.859536 yetl-framework-1.3.2.dev1/yetl/workflow/
+-rw-r--r--   0 vsts      (1001) docker     (123)      122 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/workflow/__init__.py
+-rw-r--r--   0 vsts      (1001) docker     (123)     2596 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/workflow/_multi_threaded.py
+-rw-r--r--   0 vsts      (1001) docker     (123)      495 2023-05-11 08:03:36.000000 yetl-framework-1.3.2.dev1/yetl/workflow/_notebook.py
+drwxr-xr-x   0 vsts      (1001) docker     (123)        0 2023-05-11 08:04:29.863536 yetl-framework-1.3.2.dev1/yetl_framework.egg-info/
+-rw-r--r--   0 vsts      (1001) docker     (123)     5201 2023-05-11 08:04:29.000000 yetl-framework-1.3.2.dev1/yetl_framework.egg-info/PKG-INFO
+-rw-r--r--   0 vsts      (1001) docker     (123)      902 2023-05-11 08:04:29.000000 yetl-framework-1.3.2.dev1/yetl_framework.egg-info/SOURCES.txt
+-rw-r--r--   0 vsts      (1001) docker     (123)        1 2023-05-11 08:04:29.000000 yetl-framework-1.3.2.dev1/yetl_framework.egg-info/dependency_links.txt
+-rw-r--r--   0 vsts      (1001) docker     (123)        1 2023-05-11 08:04:29.000000 yetl-framework-1.3.2.dev1/yetl_framework.egg-info/not-zip-safe
+-rw-r--r--   0 vsts      (1001) docker     (123)       29 2023-05-11 08:04:29.000000 yetl-framework-1.3.2.dev1/yetl_framework.egg-info/requires.txt
+-rw-r--r--   0 vsts      (1001) docker     (123)        5 2023-05-11 08:04:29.000000 yetl-framework-1.3.2.dev1/yetl_framework.egg-info/top_level.txt
```

### Comparing `yetl-framework-1.3.2/PKG-INFO` & `yetl-framework-1.3.2.dev1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yetl-framework
-Version: 1.3.2
+Version: 1.3.2.dev1
 Summary: yet (another spark) etl framework
 Home-page: https://www.yetl.io/
 Author: Shaun Ryan
 Author-email: shaun_chiburi@hotmail.com
 License: MIT
 Project-URL: GitHub, https://github.com/sibytes/yetl
 Project-URL: Documentation, https://www.yetl.io/
```

### Comparing `yetl-framework-1.3.2/README.md` & `yetl-framework-1.3.2.dev1/README.md`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/setup.py` & `yetl-framework-1.3.2.dev1/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 
 # The text of the README file
 README = (HERE / "README.md").read_text()
 
 # This call to setup() does all the work
 setup(
     name="yetl-framework",
-    version="1.3.2",
+    version="1.3.2.dev1",
     description="yet (another spark) etl framework",
     long_description=README,
     long_description_content_type="text/markdown",
     url="https://www.yetl.io/",
     project_urls={
         "GitHub": "https://github.com/sibytes/yetl",
         "Documentation": "https://www.yetl.io/",
```

### Comparing `yetl-framework-1.3.2/yetl/__main__.py` & `yetl-framework-1.3.2.dev1/yetl/__main__.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/cli/_init.py` & `yetl-framework-1.3.2.dev1/yetl/cli/_init.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/__init__.py` & `yetl-framework-1.3.2.dev1/yetl/config/__init__.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/_config.py` & `yetl-framework-1.3.2.dev1/yetl/config/_config.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/_decorators.py` & `yetl-framework-1.3.2.dev1/yetl/config/_decorators.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/_logging_config.py` & `yetl-framework-1.3.2.dev1/yetl/config/_logging_config.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/_project.py` & `yetl-framework-1.3.2.dev1/yetl/config/_project.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/_spark_context.py` & `yetl-framework-1.3.2.dev1/yetl/config/_spark_context.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/_tables.py` & `yetl-framework-1.3.2.dev1/yetl/config/_tables.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/_timeslice.py` & `yetl-framework-1.3.2.dev1/yetl/config/_timeslice.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/_utils.py` & `yetl-framework-1.3.2.dev1/yetl/config/_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -24,15 +24,14 @@
     TABLE = "table"
     CHECKPOINT = "checkpoint"
     FILENAME_DATE_FORMAT = "filename_date_format"
     PATH_DATE_FORMAT = "path_date_format"
     CONTAINER = "container"
     DELTA_PROPERTIES = "delta_properties"
     LOCATION = "location"
-    PROJECT = "project"
 
 
 def is_databricks():
     return "DATABRICKS_RUNTIME_VERSION" in os.environ
 
 
 def check_version(data: dict):
```

### Comparing `yetl-framework-1.3.2/yetl/config/deltalake.py` & `yetl-framework-1.3.2.dev1/yetl/config/deltalake.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/table/_deltalake.py` & `yetl-framework-1.3.2.dev1/yetl/config/table/_deltalake.py`

 * *Files 9% similar despite different names*

```diff
@@ -10,14 +10,21 @@
 from typing import Any, Dict, Union, List
 from .._timeslice import Timeslice
 import os
 from .._stage_type import StageType
 from ._table import Table
 from ..deltalake import DeltaLakeFn
 
+# from ..datallake import create_database, create_table
+
+# try:
+#     from databricks.sdk.runtime import *  # noqa F403
+# except ModuleNotFoundError:
+#     pass
+
 
 class DeltaLake(Table):
     def __init__(self, **data: Any) -> None:
         super().__init__(**data)
         self._logger = logging.getLogger(self.__class__.__name__)
         self._spark = DeltaLakeFn(project=self.project)
         self._render()
@@ -49,15 +56,20 @@
 
     def _load_sql(self, path: str):
         path = abs_config_path(self.config_path, path)
         sql = load_text(path)
         return sql
 
     def _render(self):
-        super()._render()
+        self._replacements = {
+            JinjaVariables.TABLE: self.table,
+            JinjaVariables.DATABASE: self.database,
+            JinjaVariables.CONTAINER: self.container,
+            JinjaVariables.CHECKPOINT: self.checkpoint,
+        }
         if not self._rendered:
             if self.delta_properties:
                 delta_properties_sql = self._spark.get_delta_properties_sql(
                     self.delta_properties
                 )
                 self._replacements[
                     JinjaVariables.DELTA_PROPERTIES
```

### Comparing `yetl-framework-1.3.2/yetl/config/table/_factory.py` & `yetl-framework-1.3.2.dev1/yetl/config/table/_factory.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl/config/table/_read.py` & `yetl-framework-1.3.2.dev1/yetl/config/table/_read.py`

 * *Files 5% similar despite different names*

```diff
@@ -37,21 +37,26 @@
     format: str = Field(...)
     spark_schema: Union[StructType, str] = Field(default=None)
     ddl: List[str] = Field(default=None)
     headerless_ddl: List[str] = Field(default=None)
     stage: StageType = Field(...)
 
     def _render(self):
-        super()._render()
-        self._replacements[
-            JinjaVariables.FILENAME_DATE_FORMAT
-        ] = self.timeslice.strftime(self.filename_date_format)
-        self._replacements[JinjaVariables.PATH_DATE_FORMAT] = self.timeslice.strftime(
-            self.path_date_format
-        )
+        self._replacements = {
+            JinjaVariables.FILENAME_DATE_FORMAT: self.timeslice.strftime(
+                self.filename_date_format
+            ),
+            JinjaVariables.PATH_DATE_FORMAT: self.timeslice.strftime(
+                self.path_date_format
+            ),
+            JinjaVariables.TABLE: self.table,
+            JinjaVariables.DATABASE: self.database,
+            JinjaVariables.CONTAINER: self.container,
+            JinjaVariables.CHECKPOINT: self.checkpoint,
+        }
         if not self._rendered:
             self.location = render_jinja(self.location, self._replacements)
             self.filename = render_jinja(self.filename, self._replacements)
             self.database = render_jinja(self.database, self._replacements)
             self.table = render_jinja(self.table, self._replacements)
             self.trigger = render_jinja(self.trigger, self._replacements)
```

### Comparing `yetl-framework-1.3.2/yetl/config/table/_table.py` & `yetl-framework-1.3.2.dev1/yetl/config/table/_table.py`

 * *Files 7% similar despite different names*

```diff
@@ -83,21 +83,15 @@
     path: str = Field(default=None)
     options: dict = Field(...)
     timeslice: Timeslice = Field(...)
     checkpoint: str = Field(default=None)
     config_path: str = Field(...)
 
     def _render(self):
-        self._replacements = {
-            JinjaVariables.TABLE: self.table,
-            JinjaVariables.DATABASE: self.database,
-            JinjaVariables.CONTAINER: self.container,
-            JinjaVariables.CHECKPOINT: self.checkpoint,
-            JinjaVariables.PROJECT: self.project.name,
-        }
+        pass
 
     def thresholds_select_sql(self, threshold_type: ValidationThresholdType):
         if threshold_type == ValidationThresholdType.exception:
             if self.exception_thresholds:
                 return self.exception_thresholds.select_sql()
             else:
                 return ValidationThreshold.default_select_sql()
```

### Comparing `yetl-framework-1.3.2/yetl/workflow/_multi_threaded.py` & `yetl-framework-1.3.2.dev1/yetl/workflow/_multi_threaded.py`

 * *Files identical despite different names*

### Comparing `yetl-framework-1.3.2/yetl_framework.egg-info/PKG-INFO` & `yetl-framework-1.3.2.dev1/yetl_framework.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yetl-framework
-Version: 1.3.2
+Version: 1.3.2.dev1
 Summary: yet (another spark) etl framework
 Home-page: https://www.yetl.io/
 Author: Shaun Ryan
 Author-email: shaun_chiburi@hotmail.com
 License: MIT
 Project-URL: GitHub, https://github.com/sibytes/yetl
 Project-URL: Documentation, https://www.yetl.io/
```

### Comparing `yetl-framework-1.3.2/yetl_framework.egg-info/SOURCES.txt` & `yetl-framework-1.3.2.dev1/yetl_framework.egg-info/SOURCES.txt`

 * *Files identical despite different names*

