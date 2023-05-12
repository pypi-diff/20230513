# Comparing `tmp/altimate_dataminion-0.0.1.tar.gz` & `tmp/altimate_dataminion-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "altimate_dataminion-0.0.1.tar", max compression
+gzip compressed data, was "altimate_dataminion-0.0.2.tar", max compression
```

## Comparing `altimate_dataminion-0.0.1.tar` & `altimate_dataminion-0.0.2.tar`

### file list

```diff
@@ -1,47 +1,47 @@
--rw-r--r--   0        0        0       67 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/README.md
--rw-r--r--   0        0        0      197 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/__init__.py
--rw-r--r--   0        0        0        0 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/base/__init__.py
--rw-r--r--   0        0        0     6641 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/base/dialect.py
--rw-r--r--   0        0        0     2022 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/base/extractor.py
--rw-r--r--   0        0        0     4767 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/base/metadata_profiler.py
--rw-r--r--   0        0        0     4400 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/base/profiler.py
--rw-r--r--   0        0        0     1554 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/base/source.py
--rw-r--r--   0        0        0     1549 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/config_factory.py
--rw-r--r--   0        0        0        0 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/postgresql/__init__.py
--rw-r--r--   0        0        0     7331 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/postgresql/dialect.py
--rw-r--r--   0        0        0      515 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/postgresql/extractor.py
--rw-r--r--   0        0        0      940 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/postgresql/profiler.py
--rw-r--r--   0        0        0     6053 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/postgresql/source.py
--rw-r--r--   0        0        0        0 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/s3/__init__.py
--rw-r--r--   0        0        0     7685 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/s3/source.py
--rw-r--r--   0        0        0     1261 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/shared_models.py
--rw-r--r--   0        0        0        0 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/snowflake/__init__.py
--rw-r--r--   0        0        0    13760 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/snowflake/dialect.py
--rw-r--r--   0        0        0      770 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/snowflake/profiler.py
--rw-r--r--   0        0        0     7118 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_models/snowflake/source.py
--rw-r--r--   0        0        0      151 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/__init__.py
--rw-r--r--   0        0        0        0 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/__init__.py
--rw-r--r--   0        0        0      134 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/base_builder.py
--rw-r--r--   0        0        0     4269 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/column_metrics_query_builder.py
--rw-r--r--   0        0        0      548 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/custom_query_builder.py
--rw-r--r--   0        0        0     1146 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/metadata_query_builder.py
--rw-r--r--   0        0        0      912 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/performance_query_builder.py
--rw-r--r--   0        0        0     2091 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/schema_query_builder.py
--rw-r--r--   0        0        0     1381 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/table_query_builder.py
--rw-r--r--   0        0        0      999 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/builders/utils.py
--rw-r--r--   0        0        0     1280 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/exceptions.py
--rw-r--r--   0        0        0     4246 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/factory.py
--rw-r--r--   0        0        0     2271 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/main.py
--rw-r--r--   0        0        0        0 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/metrics/__init__.py
--rw-r--r--   0        0        0     2101 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/metrics/column_metric_type.py
--rw-r--r--   0        0        0      385 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/metrics/metadata_metric_type.py
--rw-r--r--   0        0        0      390 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/metrics/performance_metric_type.py
--rw-r--r--   0        0        0      363 2023-05-11 21:55:01.847900 altimate_dataminion-0.0.1/altimate_profiler/metrics/schema_metric_type.py
--rw-r--r--   0        0        0      256 2023-05-11 21:55:01.851900 altimate_dataminion-0.0.1/altimate_profiler/metrics/table_metric_type.py
--rw-r--r--   0        0        0        0 2023-05-11 21:55:01.851900 altimate_dataminion-0.0.1/altimate_profiler/transformer/__init__.py
--rw-r--r--   0        0        0     1716 2023-05-11 21:55:01.851900 altimate_dataminion-0.0.1/altimate_profiler/transformer/base.py
--rw-r--r--   0        0        0     2295 2023-05-11 21:55:01.851900 altimate_dataminion-0.0.1/altimate_profiler/transformer/metrics.py
--rw-r--r--   0        0        0     2129 2023-05-11 21:55:01.851900 altimate_dataminion-0.0.1/altimate_profiler/transformer/schema.py
--rw-r--r--   0        0        0      394 2023-05-11 21:55:01.851900 altimate_dataminion-0.0.1/altimate_profiler/utils.py
--rw-r--r--   0        0        0      690 2023-05-11 21:55:01.855900 altimate_dataminion-0.0.1/pyproject.toml
--rw-r--r--   0        0        0      975 1970-01-01 00:00:00.000000 altimate_dataminion-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0       67 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/README.md
+-rw-r--r--   0        0        0      197 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/base/__init__.py
+-rw-r--r--   0        0        0     6641 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/base/dialect.py
+-rw-r--r--   0        0        0     2022 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/base/extractor.py
+-rw-r--r--   0        0        0     4767 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/base/metadata_profiler.py
+-rw-r--r--   0        0        0     4400 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/base/profiler.py
+-rw-r--r--   0        0        0     1554 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/base/source.py
+-rw-r--r--   0        0        0     1549 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/config_factory.py
+-rw-r--r--   0        0        0        0 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/postgresql/__init__.py
+-rw-r--r--   0        0        0     7331 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/postgresql/dialect.py
+-rw-r--r--   0        0        0      515 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/postgresql/extractor.py
+-rw-r--r--   0        0        0      940 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/postgresql/profiler.py
+-rw-r--r--   0        0        0     6053 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/postgresql/source.py
+-rw-r--r--   0        0        0        0 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/s3/__init__.py
+-rw-r--r--   0        0        0     7685 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/s3/source.py
+-rw-r--r--   0        0        0     1261 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/shared_models.py
+-rw-r--r--   0        0        0        0 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/snowflake/__init__.py
+-rw-r--r--   0        0        0    13760 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/snowflake/dialect.py
+-rw-r--r--   0        0        0      770 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/snowflake/profiler.py
+-rw-r--r--   0        0        0     7118 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_models/snowflake/source.py
+-rw-r--r--   0        0        0      208 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/__init__.py
+-rw-r--r--   0        0        0      134 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/base_builder.py
+-rw-r--r--   0        0        0     4269 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/column_metrics_query_builder.py
+-rw-r--r--   0        0        0      548 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/custom_query_builder.py
+-rw-r--r--   0        0        0     1146 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/metadata_query_builder.py
+-rw-r--r--   0        0        0      912 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/performance_query_builder.py
+-rw-r--r--   0        0        0     2091 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/schema_query_builder.py
+-rw-r--r--   0        0        0     1381 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/table_query_builder.py
+-rw-r--r--   0        0        0      999 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/builders/utils.py
+-rw-r--r--   0        0        0     1280 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/exceptions.py
+-rw-r--r--   0        0        0     4246 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/factory.py
+-rw-r--r--   0        0        0     2271 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/main.py
+-rw-r--r--   0        0        0        0 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/metrics/__init__.py
+-rw-r--r--   0        0        0     2101 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/metrics/column_metric_type.py
+-rw-r--r--   0        0        0      385 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/metrics/metadata_metric_type.py
+-rw-r--r--   0        0        0      390 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/metrics/performance_metric_type.py
+-rw-r--r--   0        0        0      363 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/metrics/schema_metric_type.py
+-rw-r--r--   0        0        0      256 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/metrics/table_metric_type.py
+-rw-r--r--   0        0        0        0 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/transformer/__init__.py
+-rw-r--r--   0        0        0     1716 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/transformer/base.py
+-rw-r--r--   0        0        0     2295 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/transformer/metrics.py
+-rw-r--r--   0        0        0     2129 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/transformer/schema.py
+-rw-r--r--   0        0        0      394 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/altimate_profiler/utils.py
+-rw-r--r--   0        0        0      690 2023-05-12 22:45:07.796947 altimate_dataminion-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0      975 1970-01-01 00:00:00.000000 altimate_dataminion-0.0.2/PKG-INFO
```

### Comparing `altimate_dataminion-0.0.1/altimate_models/base/dialect.py` & `altimate_dataminion-0.0.2/altimate_models/base/dialect.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/base/extractor.py` & `altimate_dataminion-0.0.2/altimate_models/base/extractor.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/base/metadata_profiler.py` & `altimate_dataminion-0.0.2/altimate_models/base/metadata_profiler.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/base/profiler.py` & `altimate_dataminion-0.0.2/altimate_models/base/profiler.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/base/source.py` & `altimate_dataminion-0.0.2/altimate_models/base/source.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/config_factory.py` & `altimate_dataminion-0.0.2/altimate_models/config_factory.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/postgresql/dialect.py` & `altimate_dataminion-0.0.2/altimate_models/postgresql/dialect.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/postgresql/extractor.py` & `altimate_dataminion-0.0.2/altimate_models/postgresql/extractor.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/postgresql/profiler.py` & `altimate_dataminion-0.0.2/altimate_models/postgresql/profiler.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/postgresql/source.py` & `altimate_dataminion-0.0.2/altimate_models/postgresql/source.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/s3/source.py` & `altimate_dataminion-0.0.2/altimate_models/s3/source.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/shared_models.py` & `altimate_dataminion-0.0.2/altimate_models/shared_models.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/snowflake/dialect.py` & `altimate_dataminion-0.0.2/altimate_models/snowflake/dialect.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/snowflake/profiler.py` & `altimate_dataminion-0.0.2/altimate_models/snowflake/profiler.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_models/snowflake/source.py` & `altimate_dataminion-0.0.2/altimate_models/snowflake/source.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/builders/column_metrics_query_builder.py` & `altimate_dataminion-0.0.2/altimate_profiler/builders/column_metrics_query_builder.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/builders/custom_query_builder.py` & `altimate_dataminion-0.0.2/altimate_profiler/builders/custom_query_builder.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/builders/metadata_query_builder.py` & `altimate_dataminion-0.0.2/altimate_profiler/builders/metadata_query_builder.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/builders/performance_query_builder.py` & `altimate_dataminion-0.0.2/altimate_profiler/builders/performance_query_builder.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/builders/schema_query_builder.py` & `altimate_dataminion-0.0.2/altimate_profiler/builders/schema_query_builder.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/builders/table_query_builder.py` & `altimate_dataminion-0.0.2/altimate_profiler/builders/table_query_builder.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/builders/utils.py` & `altimate_dataminion-0.0.2/altimate_profiler/builders/utils.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/exceptions.py` & `altimate_dataminion-0.0.2/altimate_profiler/exceptions.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/factory.py` & `altimate_dataminion-0.0.2/altimate_profiler/factory.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/main.py` & `altimate_dataminion-0.0.2/altimate_profiler/main.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/metrics/column_metric_type.py` & `altimate_dataminion-0.0.2/altimate_profiler/metrics/column_metric_type.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/transformer/base.py` & `altimate_dataminion-0.0.2/altimate_profiler/transformer/base.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/transformer/metrics.py` & `altimate_dataminion-0.0.2/altimate_profiler/transformer/metrics.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/altimate_profiler/transformer/schema.py` & `altimate_dataminion-0.0.2/altimate_profiler/transformer/schema.py`

 * *Files identical despite different names*

### Comparing `altimate_dataminion-0.0.1/pyproject.toml` & `altimate_dataminion-0.0.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "altimate-dataminion"
-version = "0.0.1"
+version = "0.0.2"
 description = "Internal package. Use this at your own risk, support not guaranteed"
 authors = ["Shardul Sardesai <shardul@altimate.ai>"]
 readme = "README.md"
 packages = [{include = "altimate_profiler"}, {include = "altimate_models"}]
 
 [tool.poetry.dependencies]
 python = "^3.8.1"
```

### Comparing `altimate_dataminion-0.0.1/PKG-INFO` & `altimate_dataminion-0.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: altimate-dataminion
-Version: 0.0.1
+Version: 0.0.2
 Summary: Internal package. Use this at your own risk, support not guaranteed
 Author: Shardul Sardesai
 Author-email: shardul@altimate.ai
 Requires-Python: >=3.8.1,<4.0.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

