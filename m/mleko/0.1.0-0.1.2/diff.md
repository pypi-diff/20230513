# Comparing `tmp/mleko-0.1.0.tar.gz` & `tmp/mleko-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mleko-0.1.0.tar", max compression
+gzip compressed data, was "mleko-0.1.2.tar", max compression
```

## Comparing `mleko-0.1.0.tar` & `mleko-0.1.2.tar`

### file list

```diff
@@ -1,27 +1,27 @@
--rw-r--r--   0        0        0     1073 2023-05-12 23:53:09.113170 mleko-0.1.0/LICENSE
--rw-r--r--   0        0        0     2561 2023-05-12 23:53:09.113170 mleko-0.1.0/README.md
--rw-r--r--   0        0        0     2378 2023-05-12 23:53:27.053806 mleko-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     1286 2023-05-12 23:53:27.053806 mleko-0.1.0/src/mleko/__init__.py
--rw-r--r--   0        0        0     1123 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/cache/__init__.py
--rw-r--r--   0        0        0    12625 2023-05-12 23:53:27.053806 mleko-0.1.0/src/mleko/cache/cache.py
--rw-r--r--   0        0        0     3098 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/cache/fingerprinters.py
--rw-r--r--   0        0        0      502 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/data/__init__.py
--rw-r--r--   0        0        0    12181 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/data/converters.py
--rw-r--r--   0        0        0      676 2023-05-12 23:53:27.053806 mleko-0.1.0/src/mleko/data/sources/__init__.py
--rw-r--r--   0        0        0     2778 2023-05-12 23:53:27.053806 mleko-0.1.0/src/mleko/data/sources/base_data_source.py
--rw-r--r--   0        0        0    17258 2023-05-12 23:53:27.053806 mleko-0.1.0/src/mleko/data/sources/kaggle_data_source.py
--rw-r--r--   0        0        0     8650 2023-05-12 23:53:27.053806 mleko-0.1.0/src/mleko/data/sources/s3_data_source.py
--rw-r--r--   0        0        0      608 2023-05-12 23:53:27.053806 mleko-0.1.0/src/mleko/pipeline/__init__.py
--rw-r--r--   0        0        0     1061 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/pipeline/data_container.py
--rw-r--r--   0        0        0     3578 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/pipeline/pipeline.py
--rw-r--r--   0        0        0     1577 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/pipeline/pipeline_step.py
--rw-r--r--   0        0        0      473 2023-05-12 23:53:27.053806 mleko-0.1.0/src/mleko/pipeline/steps/__init__.py
--rw-r--r--   0        0        0     1685 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/pipeline/steps/convert.py
--rw-r--r--   0        0        0     1548 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/pipeline/steps/ingest.py
--rw-r--r--   0        0        0        0 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/py.typed
--rw-r--r--   0        0        0      581 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/utils/__init__.py
--rw-r--r--   0        0        0     4523 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/utils/custom_logger.py
--rw-r--r--   0        0        0     2698 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/utils/decorators.py
--rw-r--r--   0        0        0      742 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/utils/file_helpers.py
--rw-r--r--   0        0        0     1176 2023-05-12 23:53:09.117170 mleko-0.1.0/src/mleko/utils/tqdm.py
--rw-r--r--   0        0        0     3482 1970-01-01 00:00:00.000000 mleko-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1073 2023-05-13 18:18:16.955109 mleko-0.1.2/LICENSE
+-rw-r--r--   0        0        0     2561 2023-05-13 18:18:16.955109 mleko-0.1.2/README.md
+-rw-r--r--   0        0        0     2644 2023-05-13 18:18:32.627419 mleko-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0     1286 2023-05-13 18:18:32.627419 mleko-0.1.2/src/mleko/__init__.py
+-rw-r--r--   0        0        0     1123 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/cache/__init__.py
+-rw-r--r--   0        0        0    12625 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/cache/cache.py
+-rw-r--r--   0        0        0     3098 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/cache/fingerprinters.py
+-rw-r--r--   0        0        0      502 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/__init__.py
+-rw-r--r--   0        0        0    12181 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/converters.py
+-rw-r--r--   0        0        0      676 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/sources/__init__.py
+-rw-r--r--   0        0        0     2778 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/sources/base_data_source.py
+-rw-r--r--   0        0        0    17258 2023-05-13 18:18:16.955109 mleko-0.1.2/src/mleko/data/sources/kaggle_data_source.py
+-rw-r--r--   0        0        0     8650 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/data/sources/s3_data_source.py
+-rw-r--r--   0        0        0      608 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/__init__.py
+-rw-r--r--   0        0        0     1061 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/data_container.py
+-rw-r--r--   0        0        0     3578 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/pipeline.py
+-rw-r--r--   0        0        0     1577 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/pipeline_step.py
+-rw-r--r--   0        0        0      473 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/steps/__init__.py
+-rw-r--r--   0        0        0     1685 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/steps/convert.py
+-rw-r--r--   0        0        0     1548 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/pipeline/steps/ingest.py
+-rw-r--r--   0        0        0        0 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/py.typed
+-rw-r--r--   0        0        0      581 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/__init__.py
+-rw-r--r--   0        0        0     4523 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/custom_logger.py
+-rw-r--r--   0        0        0     2698 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/decorators.py
+-rw-r--r--   0        0        0      742 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/file_helpers.py
+-rw-r--r--   0        0        0     1176 2023-05-13 18:18:16.959109 mleko-0.1.2/src/mleko/utils/tqdm.py
+-rw-r--r--   0        0        0     3482 1970-01-01 00:00:00.000000 mleko-0.1.2/PKG-INFO
```

### Comparing `mleko-0.1.0/LICENSE` & `mleko-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/README.md` & `mleko-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/pyproject.toml` & `mleko-0.1.2/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "mleko"
-version = "0.1.0"
+version = "0.1.2"
 description = "ML-Ekosystem"
 authors = ["Erik Båvenstrand <erik@bavenstrand.se>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/ErikBavenstrand/mleko"
 repository = "https://github.com/ErikBavenstrand/mleko"
 documentation = "https://mleko.readthedocs.io"
@@ -50,17 +50,15 @@
 myst-parser = {version = ">=0.16.1"}
 ipykernel = "^6.21.3"
 mypy-boto3-s3 = "^1.26.116"
 nox = "^2023.4.22"
 nox-poetry = "^1.0.2"
 sphinx-autodoc-typehints = "^1.23.0"
 sphinx-autoapi = "^2.1.0"
-
-[tool.poetry.scripts]
-mleko = "mleko.__main__:main"
+python-semantic-release = "^7.33.3"
 
 [tool.coverage.paths]
 source = ["src", "*/site-packages"]
 tests = ["tests", "*/tests"]
 
 [tool.coverage.run]
 branch = false
@@ -102,7 +100,18 @@
     "requests.auth"
 ]
 ignore_missing_imports = true
 
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
+
+[tool.semantic_release]
+branch = "main"
+version_variable = "src/mleko/__init__.py:__version__"
+version_toml = "pyproject.toml:tool.poetry.version"
+version_source = "tag"
+commit_version_number = true
+tag_commit = true
+upload_to_pypi = false
+upload_to_release = false
+hvcs = "github"
```

### Comparing `mleko-0.1.0/src/mleko/__init__.py` & `mleko-0.1.2/src/mleko/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,8 +16,8 @@
    caching of method call results and tracking changes in data.
 
 * Utilities: A collection of utility functions for logging, decorating, file management, and TQDM wrappers.
 
 Each subpackage is designed to be modular and extensible, making it easy to customize and adapt the library to a wide
 range of model building processes and requirements.
 """
-__version__ = "0.1.0"
+__version__ = "0.1.2"
```

### Comparing `mleko-0.1.0/src/mleko/cache/__init__.py` & `mleko-0.1.2/src/mleko/cache/__init__.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/cache/cache.py` & `mleko-0.1.2/src/mleko/cache/cache.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/cache/fingerprinters.py` & `mleko-0.1.2/src/mleko/cache/fingerprinters.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/data/converters.py` & `mleko-0.1.2/src/mleko/data/converters.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/data/sources/__init__.py` & `mleko-0.1.2/src/mleko/data/sources/__init__.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/data/sources/base_data_source.py` & `mleko-0.1.2/src/mleko/data/sources/base_data_source.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/data/sources/kaggle_data_source.py` & `mleko-0.1.2/src/mleko/data/sources/kaggle_data_source.py`

 * *Files 0% similar despite different names*

```diff
@@ -17,19 +17,20 @@
 from pathlib import Path
 from typing import NamedTuple
 
 import requests
 from requests.auth import HTTPBasicAuth
 from tqdm import tqdm
 
-from mleko.data.sources import BaseDataSource
 from mleko.utils.custom_logger import CustomLogger
 from mleko.utils.decorators import auto_repr
 from mleko.utils.file_helpers import clear_directory
 
+from .base_data_source import BaseDataSource
+
 
 logger = CustomLogger()
 """A CustomLogger instance that's used throughout the module for logging."""
 
 
 class KaggleCredentials(NamedTuple):
     """Represents a set of Kaggle API credentials, including a username and API key."""
```

### Comparing `mleko-0.1.0/src/mleko/data/sources/s3_data_source.py` & `mleko-0.1.2/src/mleko/data/sources/s3_data_source.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,19 +13,20 @@
 from typing import Any
 
 import boto3
 from boto3.s3.transfer import TransferConfig as BotoTransferConfig
 from botocore.config import Config as BotoConfig
 from tqdm import tqdm
 
-from mleko.data.sources import BaseDataSource
 from mleko.utils.custom_logger import CustomLogger
 from mleko.utils.decorators import auto_repr
 from mleko.utils.file_helpers import clear_directory
 
+from .base_data_source import BaseDataSource
+
 
 logger = CustomLogger()
 """A CustomLogger instance that's used throughout the module for logging."""
 
 
 class S3DataSource(BaseDataSource):
     """S3DataSource provides a convenient interface for fetching data from AWS S3 buckets and storing it locally.
```

### Comparing `mleko-0.1.0/src/mleko/pipeline/__init__.py` & `mleko-0.1.2/src/mleko/pipeline/__init__.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/pipeline/data_container.py` & `mleko-0.1.2/src/mleko/pipeline/data_container.py`

 * *Files 11% similar despite different names*

```diff
@@ -13,20 +13,18 @@
 
 @dataclass
 class DataContainer:
     """Class for holding data used in the pipeline.
 
     This class serves as a common interface and can be extended to enforce
     a shared structure or behavior across different types of data.
-
-    Attributes:
-        data: The stored data.
     """
 
     data: list[Path] | vaex.DataFrame | None = None
+    """The data stored in the DataContainer."""
 
     def __repr__(self) -> str:
         """Get string representation of DataContainer.
 
         Returns:
             String representation of the DataContainer, including data type and stored data.
         """
```

### Comparing `mleko-0.1.0/src/mleko/pipeline/pipeline.py` & `mleko-0.1.2/src/mleko/pipeline/pipeline.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/pipeline/pipeline_step.py` & `mleko-0.1.2/src/mleko/pipeline/pipeline_step.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/pipeline/steps/convert.py` & `mleko-0.1.2/src/mleko/pipeline/steps/convert.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/pipeline/steps/ingest.py` & `mleko-0.1.2/src/mleko/pipeline/steps/ingest.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/utils/__init__.py` & `mleko-0.1.2/src/mleko/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/utils/custom_logger.py` & `mleko-0.1.2/src/mleko/utils/custom_logger.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/utils/decorators.py` & `mleko-0.1.2/src/mleko/utils/decorators.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/utils/file_helpers.py` & `mleko-0.1.2/src/mleko/utils/file_helpers.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/src/mleko/utils/tqdm.py` & `mleko-0.1.2/src/mleko/utils/tqdm.py`

 * *Files identical despite different names*

### Comparing `mleko-0.1.0/PKG-INFO` & `mleko-0.1.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mleko
-Version: 0.1.0
+Version: 0.1.2
 Summary: ML-Ekosystem
 Home-page: https://github.com/ErikBavenstrand/mleko
 License: MIT
 Author: Erik Båvenstrand
 Author-email: erik@bavenstrand.se
 Requires-Python: >=3.8.0,<3.11.0
 Classifier: Development Status :: 3 - Alpha
```

