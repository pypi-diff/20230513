# Comparing `tmp/mleko-0.1.2.tar.gz` & `tmp/mleko-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mleko-0.1.2.tar", max compression
+gzip compressed data, was "mleko-0.1.3.tar", max compression
```

## Comparing `mleko-0.1.2.tar` & `mleko-0.1.3.tar`

### file list

```diff
@@ -1,27 +1,27 @@
--rw-r--r--   0        0        0     1073 2023-05-13 18:18:16.955109 mleko-0.1.2/LICENSE
--rw-r--r--   0        0        0     2561 2023-05-13 18:18:16.955109 mleko-0.1.2/README.md
--rw-r--r--   0        0        0     2644 2023-05-13 18:18:32.627419 mleko-0.1.2/pyproject.toml
--rw-r--r--   0        0        0     1286 2023-05-13 18:18:32.627419 mleko-0.1.2/src/mleko/__init__.py
--rw-r--r--   0        0        0     1123 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/cache/__init__.py
--rw-r--r--   0        0        0    12625 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/cache/cache.py
--rw-r--r--   0        0        0     3098 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/cache/fingerprinters.py
--rw-r--r--   0        0        0      502 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/__init__.py
--rw-r--r--   0        0        0    12181 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/converters.py
--rw-r--r--   0        0        0      676 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/sources/__init__.py
--rw-r--r--   0        0        0     2778 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/sources/base_data_source.py
--rw-r--r--   0        0        0    17258 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/sources/kaggle_data_source.py
--rw-r--r--   0        0        0     8650 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/data/sources/s3_data_source.py
--rw-r--r--   0        0        0      608 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/__init__.py
--rw-r--r--   0        0        0     1061 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/data_container.py
--rw-r--r--   0        0        0     3578 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/pipeline.py
--rw-r--r--   0        0        0     1577 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/pipeline_step.py
--rw-r--r--   0        0        0      473 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/steps/__init__.py
--rw-r--r--   0        0        0     1685 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/steps/convert.py
--rw-r--r--   0        0        0     1548 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/steps/ingest.py
--rw-r--r--   0        0        0        0 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/py.typed
--rw-r--r--   0        0        0      581 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/__init__.py
--rw-r--r--   0        0        0     4523 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/custom_logger.py
--rw-r--r--   0        0        0     2698 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/decorators.py
--rw-r--r--   0        0        0      742 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/file_helpers.py
--rw-r--r--   0        0        0     1176 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/tqdm.py
--rw-r--r--   0        0        0     3482 1970-01-01 00:00:00.000000 mleko-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0     1073 2023-05-13 20:42:48.653768 mleko-0.1.3/LICENSE
+-rw-r--r--   0        0        0     2561 2023-05-13 20:42:48.653768 mleko-0.1.3/README.md
+-rw-r--r--   0        0        0     2707 2023-05-13 20:43:22.029558 mleko-0.1.3/pyproject.toml
+-rw-r--r--   0        0        0     1286 2023-05-13 20:43:21.981559 mleko-0.1.3/src/mleko/__init__.py
+-rw-r--r--   0        0        0     1309 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/cache/__init__.py
+-rw-r--r--   0        0        0    12625 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/cache/cache.py
+-rw-r--r--   0        0        0     3098 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/cache/fingerprinters.py
+-rw-r--r--   0        0        0      502 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/data/__init__.py
+-rw-r--r--   0        0        0    12181 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/data/converters.py
+-rw-r--r--   0        0        0      676 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/data/sources/__init__.py
+-rw-r--r--   0        0        0     2778 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/data/sources/base_data_source.py
+-rw-r--r--   0        0        0    17258 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/data/sources/kaggle_data_source.py
+-rw-r--r--   0        0        0     8650 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/data/sources/s3_data_source.py
+-rw-r--r--   0        0        0      608 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/pipeline/__init__.py
+-rw-r--r--   0        0        0     1061 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/pipeline/data_container.py
+-rw-r--r--   0        0        0     3578 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/pipeline/pipeline.py
+-rw-r--r--   0        0        0     1577 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/pipeline/pipeline_step.py
+-rw-r--r--   0        0        0      473 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/pipeline/steps/__init__.py
+-rw-r--r--   0        0        0     1685 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/pipeline/steps/convert.py
+-rw-r--r--   0        0        0     1548 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/pipeline/steps/ingest.py
+-rw-r--r--   0        0        0        0 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/py.typed
+-rw-r--r--   0        0        0      581 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/utils/__init__.py
+-rw-r--r--   0        0        0     4523 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/utils/custom_logger.py
+-rw-r--r--   0        0        0     2698 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/utils/decorators.py
+-rw-r--r--   0        0        0      742 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/utils/file_helpers.py
+-rw-r--r--   0        0        0     1176 2023-05-13 20:42:48.657768 mleko-0.1.3/src/mleko/utils/tqdm.py
+-rw-r--r--   0        0        0     3482 1970-01-01 00:00:00.000000 mleko-0.1.3/PKG-INFO
```

### Comparing `mleko-0.1.2/LICENSE` & `mleko-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/README.md` & `mleko-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/pyproject.toml` & `mleko-0.1.3/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "mleko"
-version = "0.1.2"
+version = "0.1.3"
 description = "ML-Ekosystem"
 authors = ["Erik Båvenstrand <erik@bavenstrand.se>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/ErikBavenstrand/mleko"
 repository = "https://github.com/ErikBavenstrand/mleko"
 documentation = "https://mleko.readthedocs.io"
@@ -111,7 +111,8 @@
 version_toml = "pyproject.toml:tool.poetry.version"
 version_source = "tag"
 commit_version_number = true
 tag_commit = true
 upload_to_pypi = false
 upload_to_release = false
 hvcs = "github"
+commit_message = "chore(release): release {version} [skip ci]"
```

### Comparing `mleko-0.1.2/src/mleko/__init__.py` & `mleko-0.1.3/src/mleko/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,8 +16,8 @@
    caching of method call results and tracking changes in data.
 
 * Utilities: A collection of utility functions for logging, decorating, file management, and TQDM wrappers.
 
 Each subpackage is designed to be modular and extensible, making it easy to customize and adapt the library to a wide
 range of model building processes and requirements.
 """
-__version__ = "0.1.2"
+__version__ = "0.1.3"
```

### Comparing `mleko-0.1.2/src/mleko/cache/__init__.py` & `mleko-0.1.3/src/mleko/cache/__init__.py`

 * *Files 19% similar despite different names*

```diff
@@ -11,7 +11,12 @@
    and file types such as Vaex DataFrames or CSV files. These fingerprints help in tracking changes in data,
    and when used in combination with the caching mixins, can enhance the caching mechanisms by providing
    more unique and consistent cache keys.
 
 Together, these components allow efficient caching of method call results, reduce processing time and
 resource usage, and make it easier to identify and manage changes in data.
 """
+from .cache import CacheMixin, LRUCacheMixin
+from .fingerprinters import CSVFingerprinter, Fingerprinter
+
+
+__all__ = ["CacheMixin", "LRUCacheMixin", "CSVFingerprinter", "Fingerprinter"]
```

### Comparing `mleko-0.1.2/src/mleko/cache/cache.py` & `mleko-0.1.3/src/mleko/cache/cache.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/cache/fingerprinters.py` & `mleko-0.1.3/src/mleko/cache/fingerprinters.py`

 * *Files 0% similar despite different names*

```diff
@@ -30,15 +30,15 @@
 
         Returns:
             str: The fingerprint as a hexadecimal string.
         """
         raise NotImplementedError
 
 
-class CsvFingerprinter(Fingerprinter):
+class CSVFingerprinter(Fingerprinter):
     """A fingerprinter for CSV files supporting Gzipped and raw CSV files."""
 
     def __init__(self, n_rows: int = 1000):
         """Initialize the CSVFingerprinter.
 
         Args:
             n_rows: The number of rows to sample from each CSV file for fingerprinting. Defaults to 1000.
```

### Comparing `mleko-0.1.2/src/mleko/data/converters.py` & `mleko-0.1.3/src/mleko/data/converters.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 from pathlib import Path
 
 import vaex
 from pyarrow import csv as arrow_csv
 from tqdm import tqdm
 
 from mleko.cache.cache import LRUCacheMixin
-from mleko.cache.fingerprinters import CsvFingerprinter
+from mleko.cache.fingerprinters import CSVFingerprinter
 from mleko.utils.custom_logger import CustomLogger
 from mleko.utils.decorators import auto_repr
 from mleko.utils.tqdm import set_tqdm_percent_wrapper
 
 
 logger = CustomLogger()
 """A CustomLogger instance that's used throughout the module for logging."""
@@ -146,15 +146,15 @@
                 self._forced_categorical_columns,
                 self._forced_boolean_columns,
                 self._drop_columns,
                 self._na_values,
                 self._true_values,
                 self._false_values,
                 self._downcast_float,
-                (file_paths, CsvFingerprinter(n_rows=100_000 // len(file_paths))),
+                (file_paths, CSVFingerprinter(n_rows=100_000 // len(file_paths))),
             ],
             force_recompute=force_recompute,
         )
 
     @staticmethod
     def _convert_csv_file_to_arrow(
         file_path: Path | str,
```

### Comparing `mleko-0.1.2/src/mleko/data/sources/__init__.py` & `mleko-0.1.3/src/mleko/data/sources/__init__.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/data/sources/base_data_source.py` & `mleko-0.1.3/src/mleko/data/sources/base_data_source.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/data/sources/kaggle_data_source.py` & `mleko-0.1.3/src/mleko/data/sources/kaggle_data_source.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/data/sources/s3_data_source.py` & `mleko-0.1.3/src/mleko/data/sources/s3_data_source.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/pipeline/__init__.py` & `mleko-0.1.3/src/mleko/pipeline/__init__.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/pipeline/data_container.py` & `mleko-0.1.3/src/mleko/pipeline/data_container.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/pipeline/pipeline.py` & `mleko-0.1.3/src/mleko/pipeline/pipeline.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/pipeline/pipeline_step.py` & `mleko-0.1.3/src/mleko/pipeline/pipeline_step.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/pipeline/steps/convert.py` & `mleko-0.1.3/src/mleko/pipeline/steps/convert.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/pipeline/steps/ingest.py` & `mleko-0.1.3/src/mleko/pipeline/steps/ingest.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/utils/__init__.py` & `mleko-0.1.3/src/mleko/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/utils/custom_logger.py` & `mleko-0.1.3/src/mleko/utils/custom_logger.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/utils/decorators.py` & `mleko-0.1.3/src/mleko/utils/decorators.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/utils/file_helpers.py` & `mleko-0.1.3/src/mleko/utils/file_helpers.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/src/mleko/utils/tqdm.py` & `mleko-0.1.3/src/mleko/utils/tqdm.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.2/PKG-INFO` & `mleko-0.1.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mleko
-Version: 0.1.2
+Version: 0.1.3
 Summary: ML-Ekosystem
 Home-page: https://github.com/ErikBavenstrand/mleko
 License: MIT
 Author: Erik Båvenstrand
 Author-email: erik@bavenstrand.se
 Requires-Python: >=3.8.0,<3.11.0
 Classifier: Development Status :: 3 - Alpha
```

