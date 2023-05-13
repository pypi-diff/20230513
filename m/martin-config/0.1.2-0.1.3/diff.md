# Comparing `tmp/martin-config-0.1.2.tar.gz` & `tmp/martin-config-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "martin-config-0.1.2.tar", last modified: Thu Oct 27 21:40:47 2022, max compression
+gzip compressed data, was "martin-config-0.1.3.tar", last modified: Sat May 13 21:12:17 2023, max compression
```

## Comparing `martin-config-0.1.2.tar` & `martin-config-0.1.3.tar`

### file list

```diff
@@ -1,44 +1,44 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-27 21:40:47.059725 martin-config-0.1.2/
--rw-r--r--   0 runner    (1001) docker     (121)     4347 2022-10-27 21:40:47.059725 martin-config-0.1.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     3899 2022-10-27 21:40:30.000000 martin-config-0.1.2/README.md
--rw-r--r--   0 runner    (1001) docker     (121)      925 2022-10-27 21:40:30.000000 martin-config-0.1.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-10-27 21:40:47.059725 martin-config-0.1.2/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-27 21:40:47.055725 martin-config-0.1.2/src/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-27 21:40:47.055725 martin-config-0.1.2/src/martin_config/
--rw-r--r--   0 runner    (1001) docker     (121)      117 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     4134 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/__main__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1186 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/azfile.py
--rw-r--r--   0 runner    (1001) docker     (121)     6421 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/config.py
--rw-r--r--   0 runner    (1001) docker     (121)    27091 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/db.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-27 21:40:47.059725 martin-config-0.1.2/src/martin_config/sql/
--rw-r--r--   0 runner    (1001) docker     (121)       94 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/column_is_accessible.sql
--rw-r--r--   0 runner    (1001) docker     (121)       43 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/delete_col_comment.sql
--rw-r--r--   0 runner    (1001) docker     (121)       33 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/delete_table_comment.sql
--rw-r--r--   0 runner    (1001) docker     (121)       29 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/drop_table.sql
--rw-r--r--   0 runner    (1001) docker     (121)      406 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/func_sources.sql
--rw-r--r--   0 runner    (1001) docker     (121)      174 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/function_is_accessible.sql
--rw-r--r--   0 runner    (1001) docker     (121)      416 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/get_col_comment.sql
--rw-r--r--   0 runner    (1001) docker     (121)      283 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/get_computed_bbox.sql
--rw-r--r--   0 runner    (1001) docker     (121)      320 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/get_estimated_bbox.sql
--rw-r--r--   0 runner    (1001) docker     (121)     1206 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/get_table_columns.sql
--rw-r--r--   0 runner    (1001) docker     (121)       55 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/get_table_comment.sql
--rw-r--r--   0 runner    (1001) docker     (121)      406 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/get_table_primary_key.sql
--rw-r--r--   0 runner    (1001) docker     (121)       60 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/list_databases.sql
--rw-r--r--   0 runner    (1001) docker     (121)       65 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/list_schema_tables.sql
--rw-r--r--   0 runner    (1001) docker     (121)       52 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/list_schemas.sql
--rw-r--r--   0 runner    (1001) docker     (121)      107 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/list_tables.sql
--rw-r--r--   0 runner    (1001) docker     (121)       81 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/schema_is_accessible.sql
--rw-r--r--   0 runner    (1001) docker     (121)       60 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/set_col_comment.sql
--rw-r--r--   0 runner    (1001) docker     (121)       50 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/set_table_comment.sql
--rw-r--r--   0 runner    (1001) docker     (121)       30 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/table_exists.sql
--rw-r--r--   0 runner    (1001) docker     (121)       81 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/sql/table_is_accessible.sql
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-27 21:40:47.059725 martin-config-0.1.2/src/martin_config/test/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/test/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     3562 2022-10-27 21:40:30.000000 martin-config-0.1.2/src/martin_config/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-27 21:40:47.059725 martin-config-0.1.2/src/martin_config.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     4347 2022-10-27 21:40:47.000000 martin-config-0.1.2/src/martin_config.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     1386 2022-10-27 21:40:47.000000 martin-config-0.1.2/src/martin_config.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-10-27 21:40:47.000000 martin-config-0.1.2/src/martin_config.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       54 2022-10-27 21:40:47.000000 martin-config-0.1.2/src/martin_config.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (121)       63 2022-10-27 21:40:47.000000 martin-config-0.1.2/src/martin_config.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       14 2022-10-27 21:40:47.000000 martin-config-0.1.2/src/martin_config.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:17.206803 martin-config-0.1.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     4347 2023-05-13 21:12:17.206803 martin-config-0.1.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3899 2023-05-13 21:11:57.000000 martin-config-0.1.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      925 2023-05-13 21:11:57.000000 martin-config-0.1.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 21:12:17.206803 martin-config-0.1.3/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:17.202803 martin-config-0.1.3/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:17.202803 martin-config-0.1.3/src/martin_config/
+-rw-r--r--   0 runner    (1001) docker     (123)      117 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4134 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1186 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/azfile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6421 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27103 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/db.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:17.206803 martin-config-0.1.3/src/martin_config/sql/
+-rw-r--r--   0 runner    (1001) docker     (123)       94 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/column_is_accessible.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       43 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/delete_col_comment.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/delete_table_comment.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/drop_table.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      406 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/func_sources.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/function_is_accessible.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      416 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/get_col_comment.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      283 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/get_computed_bbox.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      320 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/get_estimated_bbox.sql
+-rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/get_table_columns.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/get_table_comment.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      406 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/get_table_primary_key.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       60 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/list_databases.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       65 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/list_schema_tables.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/list_schemas.sql
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/list_tables.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/schema_is_accessible.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       60 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/set_col_comment.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       50 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/set_table_comment.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/table_exists.sql
+-rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/sql/table_is_accessible.sql
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:17.206803 martin-config-0.1.3/src/martin_config/test/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/test/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3562 2023-05-13 21:11:57.000000 martin-config-0.1.3/src/martin_config/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:17.206803 martin-config-0.1.3/src/martin_config.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4347 2023-05-13 21:12:17.000000 martin-config-0.1.3/src/martin_config.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1386 2023-05-13 21:12:17.000000 martin-config-0.1.3/src/martin_config.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 21:12:17.000000 martin-config-0.1.3/src/martin_config.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       54 2023-05-13 21:12:17.000000 martin-config-0.1.3/src/martin_config.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       63 2023-05-13 21:12:17.000000 martin-config-0.1.3/src/martin_config.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-13 21:12:17.000000 martin-config-0.1.3/src/martin_config.egg-info/top_level.txt
```

### Comparing `martin-config-0.1.2/PKG-INFO` & `martin-config-0.1.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: martin-config
-Version: 0.1.2
+Version: 0.1.3
 Summary: Generate configuration files for martin vector tile server
 Author-email: Ioan Ferencik <ioan.ferencik@undp.org>, Jin Igarashi <jin.igarashi@undp.org>
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
```

### Comparing `martin-config-0.1.2/README.md` & `martin-config-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `martin-config-0.1.2/pyproject.toml` & `martin-config-0.1.3/pyproject.toml`

 * *Files identical despite different names*

### Comparing `martin-config-0.1.2/src/martin_config/__main__.py` & `martin-config-0.1.3/src/martin_config/__main__.py`

 * *Files identical despite different names*

### Comparing `martin-config-0.1.2/src/martin_config/azfile.py` & `martin-config-0.1.3/src/martin_config/azfile.py`

 * *Files identical despite different names*

### Comparing `martin-config-0.1.2/src/martin_config/config.py` & `martin-config-0.1.3/src/martin_config/config.py`

 * *Files identical despite different names*

### Comparing `martin-config-0.1.2/src/martin_config/db.py` & `martin-config-0.1.3/src/martin_config/db.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 try:
     import urlparse
 except ImportError:
     import urllib.parse as urlparse
 
 logger = logging.getLogger(__name__)
 
-ALLOWED_METHODS = 'execute', 'fetch', 'fetchval'
+ALLOWED_METHODS = 'execute', 'fetch', 'fetchval', 'fetchrow'
 
 
 async def run_query(conn_obj=None, sql_query=None, method='execute'):
     """
     Run a SQL query represented by sql_query against the context represented by conn_obj
     :param conn_obj: asyncpg connection object
     :param sql_query: str, SQL query
```

### Comparing `martin-config-0.1.2/src/martin_config/sql/get_table_columns.sql` & `martin-config-0.1.3/src/martin_config/sql/get_table_columns.sql`

 * *Files identical despite different names*

### Comparing `martin-config-0.1.2/src/martin_config/utils.py` & `martin-config-0.1.3/src/martin_config/utils.py`

 * *Files identical despite different names*

### Comparing `martin-config-0.1.2/src/martin_config.egg-info/PKG-INFO` & `martin-config-0.1.3/src/martin_config.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: martin-config
-Version: 0.1.2
+Version: 0.1.3
 Summary: Generate configuration files for martin vector tile server
 Author-email: Ioan Ferencik <ioan.ferencik@undp.org>, Jin Igarashi <jin.igarashi@undp.org>
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
```

### Comparing `martin-config-0.1.2/src/martin_config.egg-info/SOURCES.txt` & `martin-config-0.1.3/src/martin_config.egg-info/SOURCES.txt`

 * *Files identical despite different names*

