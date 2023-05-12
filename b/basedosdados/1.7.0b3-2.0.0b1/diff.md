# Comparing `tmp/basedosdados-1.7.0b3.tar.gz` & `tmp/basedosdados-2.0.0b1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "basedosdados-1.7.0b3.tar", max compression
+gzip compressed data, was "basedosdados-2.0.0b1.tar", max compression
```

## Comparing `basedosdados-1.7.0b3.tar` & `basedosdados-2.0.0b1.tar`

### file list

```diff
@@ -1,26 +1,29 @@
--rw-r--r--   0        0        0     2517 2022-03-31 23:18:16.947755 basedosdados-1.7.0b3/README.md
--rw-r--r--   0        0        0      805 2022-12-01 14:25:39.413453 basedosdados-1.7.0b3/basedosdados/__init__.py
--rw-r--r--   0        0        0      155 2022-07-08 15:44:50.195670 basedosdados-1.7.0b3/basedosdados/__main__.py
--rw-r--r--   0        0        0    30628 2022-11-03 15:26:28.913572 basedosdados-1.7.0b3/basedosdados/cli/cli.py
--rw-r--r--   0        0        0      633 2022-02-13 03:48:24.650168 basedosdados-1.7.0b3/basedosdados/configs/config.toml
--rw-r--r--   0        0        0      469 2022-02-13 03:48:24.650258 basedosdados-1.7.0b3/basedosdados/configs/templates/dataset/README.md
--rw-r--r--   0        0        0      856 2022-02-13 03:48:24.650328 basedosdados-1.7.0b3/basedosdados/configs/templates/dataset/dataset_description.txt
--rw-r--r--   0        0        0     1036 2022-02-13 03:48:24.650411 basedosdados-1.7.0b3/basedosdados/configs/templates/table/publish.sql
--rw-r--r--   0        0        0     2511 2022-03-17 20:15:08.504177 basedosdados-1.7.0b3/basedosdados/configs/templates/table/table_description.txt
--rw-r--r--   0        0        0      664 2022-07-08 15:44:50.196933 basedosdados-1.7.0b3/basedosdados/constants.py
--rw-r--r--   0        0        0        0 2022-02-13 03:48:24.650584 basedosdados-1.7.0b3/basedosdados/download/__init__.py
--rw-r--r--   0        0        0     1645 2022-11-01 14:34:58.094855 basedosdados-1.7.0b3/basedosdados/download/base.py
--rw-r--r--   0        0        0    17789 2022-11-01 14:34:58.095025 basedosdados-1.7.0b3/basedosdados/download/download.py
--rw-r--r--   0        0        0    13660 2022-11-01 14:34:58.095223 basedosdados-1.7.0b3/basedosdados/download/metadata.py
--rw-r--r--   0        0        0     3901 2022-07-08 15:44:50.198423 basedosdados-1.7.0b3/basedosdados/exceptions.py
--rw-r--r--   0        0        0        0 2022-02-13 03:48:24.650914 basedosdados-1.7.0b3/basedosdados/upload/__init__.py
--rw-r--r--   0        0        0    17150 2022-12-01 16:39:18.672376 basedosdados-1.7.0b3/basedosdados/upload/base.py
--rw-r--r--   0        0        0     5020 2022-12-01 16:56:15.752836 basedosdados-1.7.0b3/basedosdados/upload/connection.py
--rw-r--r--   0        0        0    10413 2022-11-01 14:34:58.095507 basedosdados-1.7.0b3/basedosdados/upload/dataset.py
--rw-r--r--   0        0        0     3247 2022-12-12 20:47:27.302114 basedosdados-1.7.0b3/basedosdados/upload/datatypes.py
--rw-r--r--   0        0        0    28275 2022-11-01 14:34:58.095805 basedosdados-1.7.0b3/basedosdados/upload/metadata.py
--rw-r--r--   0        0        0    18123 2022-11-01 14:34:58.096004 basedosdados-1.7.0b3/basedosdados/upload/storage.py
--rw-r--r--   0        0        0    39634 2022-12-12 20:45:18.428403 basedosdados-1.7.0b3/basedosdados/upload/table.py
--rw-r--r--   0        0        0     1523 2022-12-12 20:48:41.056291 basedosdados-1.7.0b3/pyproject.toml
--rw-r--r--   0        0        0     4171 2022-12-12 20:49:53.702515 basedosdados-1.7.0b3/setup.py
--rw-r--r--   0        0        0     4061 2022-12-12 20:49:53.702877 basedosdados-1.7.0b3/PKG-INFO
+-rw-r--r--   0        0        0     2514 2023-05-04 15:04:40.695846 basedosdados-2.0.0b1/README.md
+-rw-r--r--   0        0        0      827 2023-05-12 22:53:21.043886 basedosdados-2.0.0b1/basedosdados/__init__.py
+-rw-r--r--   0        0        0      156 2023-05-10 00:48:26.910378 basedosdados-2.0.0b1/basedosdados/__main__.py
+-rw-r--r--   0        0        0     8562 2023-05-11 18:29:32.124461 basedosdados-2.0.0b1/basedosdados/backend/__init__.py
+-rw-r--r--   0        0        0     6737 2023-05-12 22:20:15.182110 basedosdados-2.0.0b1/basedosdados/cli/cli.py
+-rw-r--r--   0        0        0      277 2023-05-10 18:22:29.189209 basedosdados-2.0.0b1/basedosdados/configs/config.toml
+-rw-r--r--   0        0        0      469 2022-02-13 03:48:24.650258 basedosdados-2.0.0b1/basedosdados/configs/templates/dataset/README.md
+-rw-r--r--   0        0        0      856 2022-02-13 03:48:24.650328 basedosdados-2.0.0b1/basedosdados/configs/templates/dataset/dataset_description.txt
+-rw-r--r--   0        0        0     1036 2022-02-13 03:48:24.650411 basedosdados-2.0.0b1/basedosdados/configs/templates/table/publish.sql
+-rw-r--r--   0        0        0     2511 2022-03-17 20:15:08.504177 basedosdados-2.0.0b1/basedosdados/configs/templates/table/table_description.txt
+-rw-r--r--   0        0        0      895 2023-05-10 00:48:26.956830 basedosdados-2.0.0b1/basedosdados/constants.py
+-rw-r--r--   0        0        0        0 2022-02-13 03:48:24.650584 basedosdados-2.0.0b1/basedosdados/download/__init__.py
+-rw-r--r--   0        0        0     1641 2023-05-10 00:48:26.938508 basedosdados-2.0.0b1/basedosdados/download/base.py
+-rw-r--r--   0        0        0    17788 2023-05-10 00:48:27.143327 basedosdados-2.0.0b1/basedosdados/download/download.py
+-rw-r--r--   0        0        0    13689 2023-05-10 00:48:27.186769 basedosdados-2.0.0b1/basedosdados/download/metadata.py
+-rw-r--r--   0        0        0     3903 2023-05-10 00:48:26.993068 basedosdados-2.0.0b1/basedosdados/exceptions.py
+-rw-r--r--   0        0        0     6779 2023-05-04 15:04:40.696211 basedosdados-2.0.0b1/basedosdados/schemas/columns_schema.json
+-rw-r--r--   0        0        0    65118 2023-05-04 15:04:40.696404 basedosdados-2.0.0b1/basedosdados/schemas/dataset_schema.json
+-rw-r--r--   0        0        0    30753 2023-05-04 15:04:40.696511 basedosdados-2.0.0b1/basedosdados/schemas/table_schema.json
+-rw-r--r--   0        0        0        0 2022-02-13 03:48:24.650914 basedosdados-2.0.0b1/basedosdados/upload/__init__.py
+-rw-r--r--   0        0        0    15586 2023-05-12 22:28:30.811753 basedosdados-2.0.0b1/basedosdados/upload/base.py
+-rw-r--r--   0        0        0     4957 2023-05-10 01:30:14.254761 basedosdados-2.0.0b1/basedosdados/upload/connection.py
+-rw-r--r--   0        0        0     8821 2023-05-12 22:28:04.742108 basedosdados-2.0.0b1/basedosdados/upload/dataset.py
+-rw-r--r--   0        0        0     3228 2023-05-12 21:24:41.585549 basedosdados-2.0.0b1/basedosdados/upload/datatypes.py
+-rw-r--r--   0        0        0    18917 2023-05-12 21:58:31.960998 basedosdados-2.0.0b1/basedosdados/upload/storage.py
+-rw-r--r--   0        0        0    30312 2023-05-12 22:26:47.897766 basedosdados-2.0.0b1/basedosdados/upload/table.py
+-rw-r--r--   0        0        0     3434 2023-05-12 22:26:30.059112 basedosdados-2.0.0b1/basedosdados/upload/utils.py
+-rw-r--r--   0        0        0     1404 2023-05-12 22:53:22.557176 basedosdados-2.0.0b1/pyproject.toml
+-rw-r--r--   0        0        0     3901 1970-01-01 00:00:00.000000 basedosdados-2.0.0b1/PKG-INFO
```

### Comparing `basedosdados-1.7.0b3/README.md` & `basedosdados-2.0.0b1/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -94,10 +94,7 @@
     poetry version [python-version]
     poetry publish --build
     ```
 
 7. Faz merge da branch para a master
 8. Faz release usando a UI do GitHub
 9. Atualizar versão do pacote usada internamente
-
-
-
```

### Comparing `basedosdados-1.7.0b3/basedosdados/__init__.py` & `basedosdados-2.0.0b1/basedosdados/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,27 @@
-'''
+"""
 Importing the module will automatically import the submodules.
-'''
+"""
 
 
 import sys
 import os
 
+__version__ = "2.0.0-beta.1"
+
 sys.path.append(f"{os.getcwd()}/python-package")
 
-#pylint: disable=C0413
+# pylint: disable=C0413
 
+from basedosdados.backend import Backend
 from basedosdados.constants import constants, config
 from basedosdados.upload.connection import Connection
 from basedosdados.upload.dataset import Dataset
 from basedosdados.upload.storage import Storage
 from basedosdados.upload.table import Table
-from basedosdados.upload.metadata import Metadata
 from basedosdados.download.base import reauth
 from basedosdados.download.download import (
     read_sql,
     download,
     read_table,
 )
 from basedosdados.download.metadata import (
```

### Comparing `basedosdados-1.7.0b3/basedosdados/configs/templates/dataset/dataset_description.txt` & `basedosdados-2.0.0b1/basedosdados/configs/templates/dataset/dataset_description.txt`

 * *Files identical despite different names*

### Comparing `basedosdados-1.7.0b3/basedosdados/configs/templates/table/publish.sql` & `basedosdados-2.0.0b1/basedosdados/configs/templates/table/publish.sql`

 * *Files identical despite different names*

### Comparing `basedosdados-1.7.0b3/basedosdados/configs/templates/table/table_description.txt` & `basedosdados-2.0.0b1/basedosdados/configs/templates/table/table_description.txt`

 * *Files identical despite different names*

### Comparing `basedosdados-1.7.0b3/basedosdados/constants.py` & `basedosdados-2.0.0b1/basedosdados/constants.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,29 +1,36 @@
-'''
+"""
 Constants for the project.
-'''
+"""
 # pylint: disable=C0103
 __all__ = ["config", "constants"]
 
 from enum import Enum
 from dataclasses import dataclass
 
 
 @dataclass
 class config:
-    '''
+    """
     Configuration for the project.
-    '''
+    """
+
     verbose: bool = True
     billing_project_id: str = None
     project_config_path: str = None
     from_file: bool = False
 
 
 class constants(Enum):
-    '''
+    """
     Constants for the project.
-    '''
+    """
+
     ENV_CONFIG: str = "BASEDOSDADOS_CONFIG"
     ENV_CREDENTIALS_PREFIX: str = "BASEDOSDADOS_CREDENTIALS_"
     ENV_CREDENTIALS_PROD: str = "BASEDOSDADOS_CREDENTIALS_PROD"
     ENV_CREDENTIALS_STAGING: str = "BASEDOSDADOS_CREDENTIALS_STAGING"
+    TOKEN_FILE: str = ".token.json"
+    TOKEN_URL: str = "/api/token/"
+    REFRESH_TOKEN_URL: str = "/api/token/refresh/"
+    VERIFY_TOKEN_URL: str = "/api/token/verify/"
+    TEST_ENDPOINT: str = "/api/v1/private/bigquerytypes/"
```

### Comparing `basedosdados-1.7.0b3/basedosdados/download/base.py` & `basedosdados-2.0.0b1/basedosdados/download/base.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-'''
+"""
 Functions for manage auth and credentials
-'''
+"""
 # pylint: disable=redefined-outer-name, protected-access, no-name-in-module, import-error,line-too-long
 from functools import lru_cache
 
 import sys
 
 from google.cloud import bigquery, storage
 
@@ -15,29 +15,29 @@
 
 SCOPES = [
     "https://www.googleapis.com/auth/cloud-platform",
 ]
 
 
 def reauth():
-    '''
+    """
     Reauth user credentials
-    '''
+    """
 
     pydata_google_auth.get_user_credentials(
         SCOPES, credentials_cache=pydata_google_auth.cache.REAUTH
     )
 
 
 def credentials(from_file=False, reauth=False):
-    '''
+    """
     Get user credentials
-    '''
+    """
 
-    #check if is running in colab
+    # check if is running in colab
     if "google.colab" in sys.modules:
         from google.colab import auth  # pylint: disable=import-outside-toplevel
 
         auth.authenticate_user()
         return None
 
     if from_file:
@@ -45,24 +45,23 @@
 
     if reauth:
         return pydata_google_auth.get_user_credentials(
             SCOPES, credentials_cache=pydata_google_auth.cache.REAUTH
         )
 
     return pydata_google_auth.get_user_credentials(
-            SCOPES,
+        SCOPES,
     )
 
 
-
 @lru_cache(256)
 def google_client(billing_project_id, from_file, reauth):
-    '''
+    """
     Get Google Cloud client for bigquery and storage
-    '''
+    """
 
     return dict(
         bigquery=bigquery.Client(
             credentials=credentials(from_file=from_file, reauth=reauth),
             project=billing_project_id,
         ),
         storage=storage.Client(
```

### Comparing `basedosdados-1.7.0b3/basedosdados/download/download.py` & `basedosdados-2.0.0b1/basedosdados/download/download.py`

 * *Files 0% similar despite different names*

```diff
@@ -151,15 +151,14 @@
 
     if (dataset_id is not None) and (table_id is not None):
         query = f"""
         SELECT * 
         FROM `{query_project_id}.{dataset_id}.{table_id}`"""
 
         if limit is not None:
-
             query += f" LIMIT {limit}"
     else:
         raise BaseDosDadosException("Both table_id and dataset_id should be filled.")
 
     return read_sql(
         query,
         billing_project_id=billing_project_id,
```

### Comparing `basedosdados-1.7.0b3/basedosdados/download/metadata.py` & `basedosdados-2.0.0b1/basedosdados/download/metadata.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,18 +1,19 @@
-'''
+"""
 Functions to get metadata from BD's API
-'''
+"""
 # pylint: disable=invalid-name,use-maxsplit-arg,line-too-long
 from collections import defaultdict
 import math
 
 from google.cloud import bigquery
 import pandas as pd
 import requests
 
+
 def _safe_fetch(url: str):
     """
     Safely fetchs urls and, if somehting goes wrong, informs user what is the possible cause
     """
     response = None
     try:
         response = requests.get(url, timeout=10)
@@ -43,15 +44,14 @@
         ],
     }
 
     return temp_dict
 
 
 def _fix_size(s, step=80):
-
     final = ""
 
     for l in s.split(" "):
         final += (l + " ") if len(final.split("\n")[-1]) < step else "\n"
 
     return final
 
@@ -78,15 +78,15 @@
     Args:
         verbose (bool): amount of verbosity
         output_type (str): type of output
         df (pd.DataFrame, bigquery.Dataset or bigquery.Table): table containing datasets metadata
         col_name (str): name of column with id's data
     """
 
-    df_is_dataframe = isinstance(df,pd.DataFrame)
+    df_is_dataframe = isinstance(df, pd.DataFrame)
     df_is_bq_dataset_or_table = isinstance(df, bigquery.Table)
     df_is_bq_dataset_or_table |= isinstance(df, bigquery.Dataset)
 
     if verbose is True and df_is_dataframe:
         _print_output(df)
 
     elif verbose is True and df_is_bq_dataset_or_table:
@@ -99,14 +99,15 @@
             return df.description
         if output_type == "records":
             return df.to_dict("records")
         msg = '`output_type` argument must be set to "list", "str" or "records".'
         raise ValueError(msg)
     raise TypeError("`verbose` argument must be of `bool` type.")
 
+
 def list_datasets(with_description=False, verbose=True):
     """
     This function uses `bd_dataset_search` website API
     enpoint to retrieve a list of available datasets.
 
     Args:
         with_description (bool): Optional
@@ -160,15 +161,17 @@
         return [
             {
                 "dataset_id": dataset_dict["dataset_id"][k],
                 "description": dataset_dict["description"][k],
             }
             for k in range(len(dataset_dict["dataset_id"]))
         ]
-    raise ValueError("`verbose` and `with_description` argument must be of `bool` type.")
+    raise ValueError(
+        "`verbose` and `with_description` argument must be of `bool` type."
+    )
 
 
 def list_dataset_tables(
     dataset_id,
     with_description=False,
     verbose=True,
 ):
@@ -227,15 +230,17 @@
             {
                 "table_id": table_dict["table_id"][k],
                 "description": table_dict["description"][k],
             }
             for k in range(len(table_dict["table_id"]))
         ]
 
-    raise ValueError("`verbose` and `with_description` argument must be of `bool` type.")
+    raise ValueError(
+        "`verbose` and `with_description` argument must be of `bool` type."
+    )
 
 
 def get_dataset_description(
     dataset_id,
     verbose=True,
 ):
     """
@@ -297,15 +302,14 @@
 
 
 def get_table_columns(
     dataset_id,
     table_id,
     verbose=True,
 ):
-
     """
         Fetch the names, types and descriptions for the columns in the specified table. Prints
         information on screen.
     Args:
         dataset_id (str): Required.
             Dataset id available in list_datasets.
         table_id (str): Required.
```

### Comparing `basedosdados-1.7.0b3/basedosdados/exceptions.py` & `basedosdados-2.0.0b1/basedosdados/exceptions.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 """
 Exception classes for the package.
 """
 
-#pylint: disable=C0301
+# pylint: disable=C0301
+
 
 class BaseDosDadosException(Exception):
     """Exclusive Exception from Base dos Dados"""
 
 
 class BaseDosDadosAccessDeniedException(BaseDosDadosException):
     """Exception raised if the user provides a wrong GCP project ID."""
```

### Comparing `basedosdados-1.7.0b3/basedosdados/upload/base.py` & `basedosdados-2.0.0b1/basedosdados/upload/base.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,12 @@
 """
 Module for manage dataset using local credentials and config files
 """
+from datetime import datetime
+
 # pylint: disable=line-too-long, invalid-name, too-many-arguments, invalid-envvar-value,line-too-long
 from pathlib import Path
 import sys
 from os import getenv
 import shutil
 import warnings
 import base64
@@ -12,55 +14,50 @@
 from functools import lru_cache
 from typing import Dict, List, Union
 
 from google.cloud import bigquery, bigquery_connection_v1, storage
 from google.oauth2 import service_account
 import googleapiclient.discovery
 from loguru import logger
-import yaml
-from jinja2 import Template
 import tomlkit
 
+from basedosdados.backend import Backend
 from basedosdados.constants import config, constants
 
 warnings.filterwarnings("ignore")
 
 
-class Base:
+class Base:  # pylint: disable=too-many-instance-attributes
     """
     Base class for all datasets
     """
 
     def __init__(
         self,
         config_path=".basedosdados",
-        templates=None,
         bucket_name=None,
-        metadata_path=None,
         overwrite_cli_config=False,
     ):
         """
         Initialize the class
         """
         # standard config_path configuration
         config_path = (
             Path(config.project_config_path)
             if config.project_config_path is not None
             else Path.home() / config_path
         )
 
-        self.config_path =  config_path
+        self.config_path = config_path
         self._init_config(force=overwrite_cli_config)
         self.config = self._load_config()
         self._config_log(config.verbose)
-
-        self.templates = Path(templates or self.config["templates_path"])
-        self.metadata_path = Path(metadata_path or self.config["metadata_path"])
         self.bucket_name = bucket_name or self.config["bucket_name"]
         self.uri = f"gs://{self.bucket_name}" + "/staging/{dataset}/{table}/*"
+        self._backend = Backend(self.config["api"]["url"])
 
     @staticmethod
     def _decode_env(env: str) -> str:
         """
         Decode environment variable
         """
         return base64.b64decode(getenv(env).encode("utf-8")).decode("utf-8")
@@ -109,25 +106,14 @@
             ),
             storage_staging=storage.Client(
                 credentials=self._load_credentials("staging"),
                 project=self.config["gcloud-projects"]["staging"]["name"],
             ),
         )
 
-    @property
-    def main_vars(self):
-        """
-        Variables for main templates
-        """
-        return dict(
-            templates=self.templates,
-            metadata_path=self.metadata_path,
-            bucket_name=self.bucket_name,
-        )
-
     @staticmethod
     def _input_validator(context, default="", with_lower=True):
         """
         Validate input
         """
 
         var = input(context)
@@ -150,15 +136,14 @@
         with_lower=True,
     ):
         """
         Selection with yes/no
         """
 
         while True:
-
             res = self._input_validator(first_question, default_yn, with_lower)
 
             if res == "y":
                 return default_return
 
             if res == "n":
                 return self._input_validator(no_question, default_no, with_lower)
@@ -206,17 +191,14 @@
 
         config_file = self.config_path / "config.toml"
 
         # Create credentials folder
         credentials_folder = self.config_path / "credentials"
         credentials_folder.mkdir(exist_ok=True, parents=True)
 
-        # Create template folder
-        self._refresh_templates()
-
         # If environments are set but no files exist
         if (
             (not config_file.exists())
             and (getenv(constants.ENV_CONFIG.value))
             and (getenv(constants.ENV_CREDENTIALS_PROD.value))
             and (getenv(constants.ENV_CREDENTIALS_STAGING.value))
         ):
@@ -228,15 +210,14 @@
                 f.write(self._decode_env(constants.ENV_CREDENTIALS_PROD.value))
                 f.close()
             with open(credentials_folder / "staging.json", "w", encoding="utf-8") as f:
                 f.write(self._decode_env(constants.ENV_CREDENTIALS_STAGING.value))
                 f.close()
 
         if (not config_file.exists()) or (force):
-
             # Load config file
             c_file = tomlkit.parse(
                 (Path(__file__).resolve().parents[1] / "configs" / "config.toml")
                 .open("r", encoding="utf-8")
                 .read()
             )
 
@@ -244,72 +225,55 @@
                 "\n\nApparently, that is the first time that you are using "
                 "basedosdados :)\n"
                 "Before you go, we need to setup your workspace.\n"
                 "It will not take long, I promise!\n"
                 "[press enter to continue]"
             )
 
-            ############# STEP 1 - METADATA PATH #######################
-
-            metadata_path = self._selection_yn(
-                first_question=(
-                    "\n********* STEP 1 **********\n"
-                    "Where are you going to save the metadata files of "
-                    "datasets and tables?\n"
-                    f"Is it at the current path ({Path.cwd()})? [Y/n]\n"
-                ),
-                default_yn="y",
-                default_return=Path.cwd(),
-                no_question=("\nWhere would you like to save it?\n" "metadata path: "),
-                with_lower=False,
-            )
-
-            c_file["metadata_path"] = str(Path(metadata_path) / "bases")
-
-            ############# STEP 2 - CREDENTIALS PATH ######################
+            ############# STEP 1 - CREDENTIALS PATH ######################
 
             credentials_path = self.config_path / "credentials"
             credentials_path = Path(
                 self._selection_yn(
                     first_question=(
-                        "\n********* STEP 2 **********\n"
+                        "\n********* STEP 1 **********\n"
                         "Where do you want to save your Google Cloud credentials?\n"
                         f"Is it at the {credentials_path}? [Y/n]\n"
                     ),
                     default_yn="y",
                     default_return=credentials_path,
                     no_question=(
                         "\nWhere would you like to save it?\n" "credentials path: "
                     ),
                     with_lower=False,
                 )
             )
 
-            ############# STEP 3 - STAGING CREDS. #######################
+            ############# STEP 2 - STAGING CREDS. #######################
             project_staging = self._input_validator(
-                "\n********* STEP 3 **********\n"
+                "\n********* STEP 2 **********\n"
                 "What is the Google Cloud Project that you are going to use "
                 "to upload and treat data?\nIt might be something with 'staging'"
                 "in the name. If you just have one project, put its name.\n"
                 "Project id [basedosdados-staging]: ",
                 "basedosdados-staging",
             )
 
             self._check_credentials(project_staging, "staging", credentials_path)
 
             c_file["gcloud-projects"]["staging"]["credentials_path"] = str(
                 credentials_path / "staging.json"
             )
             c_file["gcloud-projects"]["staging"]["name"] = project_staging
 
-            ############# STEP 4 - PROD CREDS. #######################
+            ############# STEP 3 - PROD CREDS. #######################
 
             project_prod = self._selection_yn(
                 first_question=(
-                    "\n********* STEP 4 **********\n"
+                    "\n********* STEP 3 **********\n"
                     "Is your production project the same as the staging? [y/N]\n"
                 ),
                 default_yn="n",
                 default_return=project_staging,
                 no_question=(
                     "What is the production Google Cloud Project then?\n"
                     "Project id [basedosdados]: "
@@ -326,28 +290,35 @@
                 self._check_credentials(project_prod, "prod", credentials_path)
 
             c_file["gcloud-projects"]["prod"]["credentials_path"] = str(
                 credentials_path / "prod.json"
             )
             c_file["gcloud-projects"]["prod"]["name"] = project_prod
 
-            ############# STEP 5 - BUCKET NAME #######################
+            ############# STEP 4 - BUCKET NAME #######################
 
             bucket_name = self._input_validator(
-                "\n********* STEP 5 **********\n"
+                "\n********* STEP 4 **********\n"
                 "What is the Storage Bucket that you are going to be using to save the data?\n"
                 "Bucket name [basedosdados]: ",
                 "basedosdados",
             )
 
             c_file["bucket_name"] = bucket_name
 
-            ############# STEP 6 - SET TEMPLATES #######################
+            ############# STEP 5 - CONFIGURE API #######################
 
-            c_file["templates_path"] = str(self.config_path / "templates")
+            api_base_url = self._input_validator(
+                "\n********* STEP 5 **********\n"
+                "What is the URL of the API that you are going to use?\n"
+                "API url [https://staging.api.basedosdados.org/api/v1/graphql]: ",
+                "https://staging.api.basedosdados.org/api/v1/graphql",
+            )
+
+            c_file["api"]["url"] = api_base_url
 
             config_file.open("w", encoding="utf-8").write(tomlkit.dumps(c_file))
 
     @staticmethod
     def _config_log(verbose: bool):
         """
         Logging configuration
@@ -364,40 +335,18 @@
         """
         Loads the configuration file
         """
 
         if getenv(constants.ENV_CONFIG.value):
             return tomlkit.parse(self._decode_env(constants.ENV_CONFIG.value))
         return tomlkit.parse(
-            (self.config_path / "config.toml")
-            .open("r", encoding="utf-8")
-            .read()
+            (self.config_path / "config.toml").open("r", encoding="utf-8").read()
         )
 
     @staticmethod
-    def _load_yaml(file):
-        """
-        Loads a yaml file
-        """
-
-        try:
-            return yaml.load(open(file, "r", encoding="utf-8"), Loader=yaml.SafeLoader)
-        except FileNotFoundError:
-            return None
-
-    def _render_template(self, template_file, kargs):
-        """
-        Render a template file
-        """
-
-        return Template(
-            (self.templates / template_file).open("r", encoding="utf-8").read()
-        ).render(**kargs)
-
-    @staticmethod
     def _check_mode(mode):
         """
         Checks if the mode is valid
         """
         ACCEPTED_MODES = [
             "all",
             "staging",
@@ -412,24 +361,14 @@
 
         raise Exception(
             f"Argument {mode} not supported. "
             f"Enter one of the following: "
             f'{",".join(ACCEPTED_MODES)}'
         )
 
-    def _refresh_templates(self):
-        """
-        Refreshes the templates
-        """
-        shutil.rmtree((self.config_path / "templates"), ignore_errors=True)
-        shutil.copytree(
-            (Path(__file__).resolve().parents[1] / "configs" / "templates"),
-            (self.config_path / "templates"),
-        )
-
     def _get_project_id(self, mode: str) -> str:
         """
         Get the project ID.
         """
         return self.config["gcloud-projects"][mode]["name"]
 
     def _get_project_number(self, mode: str) -> str:
@@ -438,43 +377,51 @@
         """
         credentials = self._load_credentials(mode)
         crm_service = googleapiclient.discovery.build(
             "cloudresourcemanager", "v1", credentials=credentials
         )
         project_id = self._get_project_id(mode)
         # pylint: disable=no-member
-        return crm_service.projects().get(projectId=project_id).execute()["projectNumber"]
+        return (
+            crm_service.projects().get(projectId=project_id).execute()["projectNumber"]
+        )
 
-    def _get_project_iam_policy(self, mode: str) -> Dict[str, Union[str, int, List[Dict[str, Union[str, List[str]]]]]]:
+    def _get_project_iam_policy(
+        self, mode: str
+    ) -> Dict[str, Union[str, int, List[Dict[str, Union[str, List[str]]]]]]:
         """
         Get the project IAM policy.
         """
         credentials = self._load_credentials(mode)
         service = googleapiclient.discovery.build(
             "cloudresourcemanager", "v1", credentials=credentials
         )
         policy = (
-            service.projects() # pylint: disable=no-member
+            service.projects()  # pylint: disable=no-member
             .getIamPolicy(
                 resource=self._get_project_id(mode),
                 body={"options": {"requestedPolicyVersion": 1}},
             )
             .execute()
         )
         return policy
 
-    def _set_project_iam_policy(self, policy: Dict[str, Union[str, int, List[Dict[str, Union[str, List[str]]]]]], mode: str):
+    def _set_project_iam_policy(
+        self,
+        policy: Dict[str, Union[str, int, List[Dict[str, Union[str, List[str]]]]]],
+        mode: str,
+    ):
         """
         Set the project IAM policy.
         """
         credentials = self._load_credentials(mode)
         service = googleapiclient.discovery.build(
             "cloudresourcemanager", "v1", credentials=credentials
         )
-        service.projects().setIamPolicy( # pylint: disable=no-member
+        service.projects().setIamPolicy(  # pylint: disable=no-member
             resource=self._get_project_id(mode), body={"policy": policy}
         ).execute()
 
     def _grant_role(self, role: str, member: str, mode: str):
         """
         Grant a role to a member.
         """
```

### Comparing `basedosdados-1.7.0b3/basedosdados/upload/connection.py` & `basedosdados-2.0.0b1/basedosdados/upload/connection.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,41 +2,46 @@
 Module for managing BigQuery Connections.
 """
 # pylint: disable=line-too-long, fixme, invalid-name,line-too-long,unnecessary-lambda-assignment
 
 from typing import Union
 
 import google.auth
-from google.cloud import bigquery_connection_v1
 from google.cloud.bigquery_connection_v1.types import CloudResourceProperties
-from google.cloud.bigquery_connection_v1.types.connection import Connection as BQConnection
+from google.cloud.bigquery_connection_v1.types.connection import (
+    Connection as BQConnection,
+    CreateConnectionRequest,
+    DeleteConnectionRequest,
+    GetConnectionRequest,
+)
 
 from basedosdados.upload.base import Base
 
+
 class Connection(Base):
     """
     Manages BigQuery Connections.
     """
 
-    def __init__ ( # pylint: disable=too-many-arguments
+    def __init__(  # pylint: disable=too-many-arguments
         self,
         name: str,
         location: str = None,
         mode: str = "staging",
         friendly_name: str = None,
         description: str = None,
-        **kwargs
+        **kwargs,
     ):
         super().__init__(**kwargs)
         self._name = name
         self._location = location or "US"
         self._mode = mode
         self._friendly_name = friendly_name
         self._description = description
-        self._project = self.config['gcloud-projects'][self._mode]['name']
+        self._project = self.config["gcloud-projects"][self._mode]["name"]
         self._parent = f"projects/{self._project}/locations/{self._location}"
 
     @property
     def exists(self) -> bool:
         """
         Checks if connection exists.
         """
@@ -46,17 +51,15 @@
 
     @property
     def connection(self) -> Union[BQConnection, None]:
         """
         Returns connection object.
         """
         client = self.client[f"bigquery_connection_{self._mode}"]
-        request = bigquery_connection_v1.GetConnectionRequest(
-            name=f"{self._parent}/connections/{self._name}"
-        )
+        request = GetConnectionRequest(name=f"{self._parent}/connections/{self._name}")
         try:
             return client.get_connection(request=request)
         except google.api_core.exceptions.NotFound:
             return None
         except Exception as e:
             raise e
 
@@ -72,31 +75,31 @@
     @property
     def service_account(self) -> str:
         """
         Returns the service account associated with the connection.
         """
         conn = self.connection
         if conn:
-            return conn.cloud_resource.service_account_id # pylint: disable=no-member
+            return conn.cloud_resource.service_account_id  # pylint: disable=no-member
         raise ValueError("Connection does not exist.")
 
     def create(self):
         """
         Creates a new connection.
         """
         client = self.client[f"bigquery_connection_{self._mode}"]
-        request = bigquery_connection_v1.CreateConnectionRequest(
+        request = CreateConnectionRequest(
             parent=self._parent,
             connection_id=self._name,
-            connection=bigquery_connection_v1.Connection(
+            connection=BQConnection(
                 name=self._name,
                 friendly_name=self._friendly_name or self._name,
                 description=self._description or self._name,
                 cloud_resource=CloudResourceProperties(),
-            )
+            ),
         )
         client.create_connection(request=request)
 
     def set_biglake_permissions(self):
         """
         Grants all needed roles to the connection service account to be able to
         access BigLake:
@@ -135,11 +138,11 @@
 
     def delete(self):
         """
         Deletes a connection.
         """
         self.revoke_biglake_permissions()
         client = self.client[f"bigquery_connection_{self._mode}"]
-        request = bigquery_connection_v1.DeleteConnectionRequest(
+        request = DeleteConnectionRequest(
             name=f"{self._parent}/connections/{self._name}"
         )
         client.delete_connection(request=request)
```

### Comparing `basedosdados-1.7.0b3/basedosdados/upload/dataset.py` & `basedosdados-2.0.0b1/basedosdados/upload/dataset.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,143 +1,91 @@
 """
 Module for manage dataset to the server.
 """
-# pylint: disable=line-too-long, fixme, invalid-name,line-too-long,unnecessary-lambda-assignment
+# pylint: disable=line-too-long, fixme, invalid-name,line-too-long
+from functools import lru_cache
 from pathlib import Path
 from loguru import logger
 
 from google.cloud import bigquery
 from google.api_core.exceptions import Conflict
 
 from basedosdados.upload.base import Base
-from basedosdados.upload.metadata import Metadata
 
 
 class Dataset(Base):
     """
     Manage datasets in BigQuery.
     """
 
     def __init__(self, dataset_id, **kwargs):
         super().__init__(**kwargs)
-
         self.dataset_id = dataset_id.replace("-", "_")
-        self.dataset_folder = Path(self.metadata_path / self.dataset_id)
-        self.metadata = Metadata(self.dataset_id, **kwargs)
 
     @property
+    @lru_cache
     def dataset_config(self):
         """
         Dataset config file.
         """
-
-        return self._load_yaml(
-            self.metadata_path / self.dataset_id / "dataset_config.yaml"
-        )
+        return self._backend.get_dataset_config(self.dataset_id)
 
     def _loop_modes(self, mode="all"):
         """
         Loop modes.
         """
 
         mode = ["prod", "staging"] if mode == "all" else [mode]
         dataset_tag = lambda m: f"_{m}" if m == "staging" else ""
-
         return (
             {
                 "client": self.client[f"bigquery_{m}"],
                 "id": f"{self.client[f'bigquery_{m}'].project}.{self.dataset_id}{dataset_tag(m)}",
+                "mode": m,
             }
             for m in mode
         )
 
-    @staticmethod
-    def _setup_dataset_object(dataset_id, location=None):
+    def _setup_dataset_object(self, dataset_id, location=None, mode="staging"):
         """
         Setup dataset object.
         """
 
         dataset = bigquery.Dataset(dataset_id)
+        if mode == "staging":
+            dataset_path = dataset_id.replace("_staging", "")
+            description = f"staging dataset for `{dataset_path}`"
+            labels = {"staging": True}
+        else:
+            try:
+                description = self.dataset_config.get("descriptionPt", "")
+                labels = {
+                    tag.get("namePt"): True for tag in self.dataset_config.get("tags")
+                }
+            except BaseException:
+                logger.warning(
+                    f"dataset {dataset_id} does not have a description in the API."
+                )
+                description = "description not available in the API."
+                labels = {}
 
-        ## TODO: not being used since 1.6.0 - need to redo the description tha goes to bigquery
-        dataset.description = "Para saber mais acesse https://basedosdados.org/"
-        # dataset.description = self._render_template(
-        #     Path("dataset/dataset_description.txt"), self.dataset_config
-        # )
-
+        dataset.description = description
+        dataset.labels = labels
         dataset.location = location
-
         return dataset
 
-    def _write_readme_file(self):
-        """
-        Write README.md file.
-        """
-
-        readme_content = (
-            f"Como capturar os dados de {self.dataset_id}?\n\nPara cap"
-            f"turar esses dados, basta verificar o link dos dados orig"
-            f"inais indicado em dataset_config.yaml no item website.\n"
-            f"\nCaso tenha sido utilizado algum código de captura ou t"
-            f"ratamento, estes estarão contidos em code/. Se o dado pu"
-            f"blicado for em sua versão bruta, não existirá a pasta co"
-            f"de/.\n\nOs dados publicados estão disponíveis em: https:"
-            f"//basedosdados.org/dataset/{self.dataset_id.replace('_','-')}"
-        )
-
-        readme_path = Path(self.metadata_path / self.dataset_id / "README.md")
-
-        with open(readme_path, "w", encoding="utf-8") as readmefile:
-            readmefile.write(readme_content)
-
-    def init(self, replace=False):
-        """Initialize dataset folder at metadata_path at `metadata_path/<dataset_id>`.
-
-        The folder should contain:
-
-        * `dataset_config.yaml`
-        * `README.md`
-
-        Args:
-            replace (str): Optional. Whether to replace existing folder.
-
-        Raises:
-            FileExistsError: If dataset folder already exists and replace is False
-        """
-
-        # Create dataset folder
-        try:
-            self.dataset_folder.mkdir(exist_ok=replace, parents=True)
-        except FileExistsError as e:
-            raise FileExistsError(
-                f"Dataset {str(self.dataset_folder.stem)} folder does not exists. "
-                "Set replace=True to replace current files."
-            ) from e
-
-        # create dataset_config.yaml with metadata
-        self.metadata.create(if_exists="replace")
-
-        # create README.md file
-        self._write_readme_file()
-
-        # Add code folder
-        (self.dataset_folder / "code").mkdir(exist_ok=replace, parents=True)
-
-        return self
-
     def publicize(self, mode="all", dataset_is_public=True):
         """Changes IAM configuration to turn BigQuery dataset public.
 
         Args:
             mode (bool): Which dataset to create [prod|staging|all].
             dataset_is_public (bool): Control if prod dataset is public or not. By default staging datasets like `dataset_id_staging` are not public.
         """
 
         for m in self._loop_modes(mode):
-
             dataset = m["client"].get_dataset(m["id"])
             entries = dataset.access_entries
             # TODO https://github.com/basedosdados/mais/pull/1020
             # TODO if staging dataset is private, the prod view can't acess it: if dataset_is_public and "staging" not in dataset.dataset_id:
             if dataset_is_public:
                 if "staging" not in dataset.dataset_id:
                     entries.extend(
@@ -167,21 +115,22 @@
                                 entity_type="iamMember",
                                 entity_id="allUsers",
                             ),
                         ]
                     )
                 dataset.access_entries = entries
             m["client"].update_dataset(dataset, ["access_entries"])
-        logger.success(
-            " {object} {object_id}_{mode} was {action}!",
-            object_id=self.dataset_id,
-            mode=mode,
-            object="Dataset",
-            action="publicized",
-        )
+
+            logger.success(
+                " {object} {object_id}_{mode} was {action}!",
+                object_id=self.dataset_id,
+                mode=m["mode"],
+                object="Dataset",
+                action="publicized",
+            )
 
     def create(
         self, mode="all", if_exists="raise", dataset_is_public=True, location=None
     ):
         """Creates BigQuery datasets given `dataset_id`.
 
         It can create two datasets:
@@ -209,33 +158,33 @@
         Raises:
             Warning: Dataset already exists and if_exists is set to `raise`
         """
 
         if if_exists == "replace":
             self.delete(mode)
         elif if_exists == "update":
-
             self.update()
             return
 
         # Set dataset_id to the ID of the dataset to create.
         for m in self._loop_modes(mode):
-
             # Construct a full Dataset object to send to the API.
-            dataset_obj = self._setup_dataset_object(m["id"], location=location)
+            dataset_obj = self._setup_dataset_object(
+                dataset_id=m["id"], location=location, mode=m["mode"]
+            )
 
             # Send the dataset to the API for creation, with an explicit timeout.
             # Raises google.api_core.exceptions.Conflict if the Dataset already
             # exists within the project.
             try:
                 m["client"].create_dataset(dataset_obj)  # Make an API request.
                 logger.success(
                     " {object} {object_id}_{mode} was {action}!",
                     object_id=self.dataset_id,
-                    mode=mode,
+                    mode=m["mode"],
                     object="Dataset",
                     action="created",
                 )
 
             except Conflict as e:
                 if if_exists == "pass":
                     return
@@ -248,47 +197,42 @@
         """Deletes dataset in BigQuery. Toogle mode to choose which dataset to delete.
 
         Args:
             mode (str): Optional.  Which dataset to delete [prod|staging|all]
         """
 
         for m in self._loop_modes(mode):
-
             m["client"].delete_dataset(m["id"], delete_contents=True, not_found_ok=True)
-        logger.info(
-            " {object} {object_id}_{mode} was {action}!",
-            object_id=self.dataset_id,
-            mode=mode,
-            object="Dataset",
-            action="deleted",
-        )
+            logger.info(
+                " {object} {object_id}_{mode} was {action}!",
+                object_id=self.dataset_id,
+                mode=m["mode"],
+                object="Dataset",
+                action="deleted",
+            )
 
     def update(self, mode="all", location=None):
         """Update dataset description. Toogle mode to choose which dataset to update.
 
         Args:
             mode (str): Optional. Which dataset to update [prod|staging|all]
             location (str): Optional. Location of dataset data.
                 List of possible region names locations: https://cloud.google.com/bigquery/docs/locations
 
         """
 
         for m in self._loop_modes(mode):
-
             # Send the dataset to the API to update, with an explicit timeout.
             # Raises google.api_core.exceptions.Conflict if the Dataset already
             # exists within the project.
             m["client"].update_dataset(
-                self._setup_dataset_object(
-                    m["id"],
-                    location=location,
-                ),
+                self._setup_dataset_object(m["id"], location=location, mode=m["mode"]),
                 fields=["description"],
             )  # Make an API request.
 
-        logger.success(
-            " {object} {object_id}_{mode} was {action}!",
-            object_id=self.dataset_id,
-            mode=mode,
-            object="Dataset",
-            action="updated",
-        )
+            logger.success(
+                " {object} {object_id}_{mode} was {action}!",
+                object_id=self.dataset_id,
+                mode=m["mode"],
+                object="Dataset",
+                action="updated",
+            )
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `basedosdados-1.7.0b3/basedosdados/upload/datatypes.py` & `basedosdados-2.0.0b1/basedosdados/upload/datatypes.py`

 * *Files 22% similar despite different names*

```diff
@@ -12,24 +12,28 @@
 class Datatype:
     """
     Manage external and partition config
     """
 
     def __init__(  # pylint: disable=too-many-arguments
         self,
-        table_obj,
+        dataset_id="",
+        table_id="",
+        schema=None,
         source_format="csv",
         mode="staging",
+        bucket_name=None,
         partitioned=False,
         biglake_connection_id=None,
     ):
-
-        self.table_obj = table_obj
+        self.dataset_id = dataset_id.replace("_staging", "")
+        self.schema = schema
         self.source_format = source_format
         self.mode = mode
+        self.uri = f"gs://{bucket_name}/staging/{self.dataset_id}/{table_id}/*"
         self.partitioned = partitioned
         self.biglake_connection_id = biglake_connection_id
 
     def header(self, data_sample_path):
         """
         Retrieve the header of the data sample
         """
@@ -48,42 +52,39 @@
 
     def partition(self):
         """
         Configure the partitioning of the table
         """
         hive_partitioning = bigquery.external_config.HivePartitioningOptions()
         hive_partitioning.mode = "STRINGS"
-        hive_partitioning.source_uri_prefix = self.table_obj.uri.format(
-            dataset=self.table_obj.dataset_id, table=self.table_obj.table_id
-        ).replace("*", "")
+        hive_partitioning.source_uri_prefix = self.uri.replace("*", "")
 
         return hive_partitioning
 
     @property
     def external_config(self):
         """
         Configure the external table
         """
         if self.source_format == "csv":
             _external_config = bigquery.ExternalConfig("CSV")
             _external_config.options.skip_leading_rows = 1
             _external_config.options.allow_quoted_newlines = True
             _external_config.options.allow_jagged_rows = True
             _external_config.autodetect = False
-            _external_config.schema = self.table_obj._load_schema(self.mode)
+            _external_config.schema = self.schema
         elif self.source_format == "avro":
             _external_config = bigquery.ExternalConfig("AVRO")
         elif self.source_format == "parquet":
             _external_config = bigquery.ExternalConfig("PARQUET")
         else:
             raise NotImplementedError(
                 "Base dos Dados just supports csv, avro and parquet files"
             )
-
-        _external_config.source_uris = f"gs://{self.table_obj.bucket_name}/staging/{self.table_obj.dataset_id}/{self.table_obj.table_id}/*"
+        _external_config.source_uris = self.uri
         if self.partitioned:
             _external_config.hive_partitioning = self.partition()
 
         if self.biglake_connection_id:
             _external_config.connection_id = self.biglake_connection_id
             # When using BigLake tables, schema must be provided to the `Table` object, not the
             # `ExternalConfig` object.
```

### Comparing `basedosdados-1.7.0b3/basedosdados/upload/metadata.py` & `basedosdados-2.0.0b1/basedosdados/upload/table.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,749 +1,794 @@
 """
-Class to manage the metadata of datasets and tables
+Class for manage tables in Storage and Big Query
 """
-# pylint: disable=fixme, invalid-name, redefined-builtin, too-many-arguments, undefined-loop-variable
-from __future__ import annotations
 
+import contextlib
+
+# pylint: disable=invalid-name, too-many-locals, too-many-branches, too-many-arguments,line-too-long,R0801,consider-using-f-string
+from pathlib import Path
 from copy import deepcopy
+import textwrap
+import inspect
 from functools import lru_cache
-from loguru import logger
 
-import requests
-from ckanapi import RemoteCKAN
-from ckanapi.errors import NotAuthorized, ValidationError
-from ruamel.yaml.comments import CommentedMap
-from ruamel.yaml.compat import ordereddict
-import ruamel.yaml as ryaml
+from loguru import logger
+from google.cloud import bigquery
+from google.cloud.bigquery import SchemaField
+import google.api_core.exceptions
 
-from basedosdados.exceptions import BaseDosDadosException
 from basedosdados.upload.base import Base
+from basedosdados.upload.connection import Connection
+from basedosdados.upload.storage import Storage
+from basedosdados.upload.dataset import Dataset
+from basedosdados.upload.datatypes import Datatype
+from basedosdados.exceptions import BaseDosDadosException
 
 
-class Metadata(Base):
+class Table(Base):
     """
-    Manage metadata in CKAN backend.
+    Manage tables in Google Cloud Storage and BigQuery.
     """
 
-    def __init__(self, dataset_id, table_id=None, **kwargs):
+    def __init__(self, dataset_id, table_id, **kwargs):
         super().__init__(**kwargs)
 
-        self.table_id = table_id
-        self.dataset_id = dataset_id
-
-        if self.table_id:
-            self.dataset_metadata_obj = Metadata(self.dataset_id, **kwargs)
-
-        url = "https://basedosdados.org"
-        self.CKAN_API_KEY = self.config.get("ckan", {}).get("api_key")
-        self.CKAN_URL = self.config.get("ckan", {}).get("url", "") or url
+        self.table_id = table_id.replace("-", "_")
+        self.dataset_id = dataset_id.replace("-", "_")
+        # self.dataset_folder = Path(self.metadata_path / self.dataset_id)
+        # self.table_folder = self.dataset_folder / table_id
+        self.table_full_name = dict(
+            prod=f"{self.client['bigquery_prod'].project}.{self.dataset_id}.{self.table_id}",
+            staging=f"{self.client['bigquery_staging'].project}.{self.dataset_id}_staging.{self.table_id}",
+        )
+        self.table_full_name.update(dict(all=deepcopy(self.table_full_name)))
+        # self.metadata = Metadata(self.dataset_id, self.table_id, **kwargs)
 
     @property
-    def filepath(self) -> str:
-        """Build the dataset or table filepath"""
+    @lru_cache(256)
+    def table_config(self):
+        """
+        Load table config
+        """
+        # return self._load_yaml(self.table_folder / "table_config.yaml")
+        return self._backend.get_table_config(self.dataset_id, self.table_id)
 
-        filename = "dataset_config.yaml"
-        if self.table_id:
-            filename = f"{self.table_id}/table_config.yaml"
-        return self.metadata_path / self.dataset_id / filename
+    def _get_table_obj(self, mode):
+        """
+        Get table object from BigQuery
+        """
 
-    @property
-    def local_metadata(self) -> dict:
-        """Load dataset or table local metadata"""
+        return self.client[f"bigquery_{mode}"].get_table(self.table_full_name[mode])
 
-        if self.filepath.exists():
-            with open(self.filepath, "r", encoding="utf-8") as file:
-                return ryaml.safe_load(file.read())
-        return {}
+    def _is_partitioned(self, data_sample_path=None, source_format=None):
+        if data_sample_path is not None:
+            table_columns = self._get_columns_from_data(
+                data_sample_path=data_sample_path,
+                source_format=source_format,
+                mode="staging",
+            )
+        else:
+            table_columns = self._get_columns_metadata_from_api()
 
-    @property
-    def ckan_metadata(self) -> dict:
-        """Load dataset or table metadata from Base dos Dados CKAN"""
+        return bool(table_columns.get("partition_columns", []))
 
-        ckan_dataset, ckan_table = self.ckan_metadata_extended
-        return ckan_table or ckan_dataset
+    def _load_schema_from_json(
+        self,
+        columns=None,
+    ):
+        return [
+            ## ref: https://cloud.google.com/python/docs/reference/bigquery/latest/google.cloud.bigquery.schema.SchemaField
+            SchemaField(
+                name=col.get("name"),
+                field_type=col.get("type"),
+                description=col.get("description", None),
+            )
+            for col in columns
+        ]
 
-    @property
-    def ckan_metadata_extended(self) -> dict:
-        """Load dataset and table metadata from Base dos Dados CKAN"""
+    def _load_staging_schema_from_data(
+        self, data_sample_path=None, source_format="csv"
+    ):
+        """
+        Generate schema from columns metadata in data sample
+        """
 
-        dataset_id = self.dataset_id.replace("_", "-")
-        url = f"{self.CKAN_URL}/api/3/action/package_show?id={dataset_id}"
+        if self.table_exists(mode="staging"):
+            logger.warning(
+                " {object} {object_id} allready exists, replacing schema!",
+                object_id=self.table_id,
+                object="Table",
+            )
+            # table_columns = [
+            #     {"name": c.name, "type": c.field_type}
+            #     for c in self._get_table_obj(mode="staging").schema
+            # ]
+        table_columns = self._get_columns_from_data(
+            data_sample_path=data_sample_path,
+            source_format=source_format,
+            mode="staging",
+        )
+        # table_columns = table_columns.get("partition_columns") + table_columns.get(
+        #     "columns"
+        # )
+        return self._load_schema_from_json(columns=table_columns.get("columns"))
 
-        ckan_response = requests.get(url, timeout=10).json()
-        dataset = ckan_response.get("result")
+    def _load_schema_from_bq(self, mode="staging"):
+        """Load schema from table config
 
-        if not ckan_response.get("success"):
-            return {}, {}
+        Args:
+            mode (bool): Which dataset to create [prod|staging].
 
-        if self.table_id:
-            for resource in dataset["resources"]:
-                if resource["name"] == self.table_id:
-                    return dataset, resource
+        """
+        table_columns = self._get_columns_from_bq()
+        columns = table_columns.get("partition_columns") + table_columns.get("columns")
+        return self._load_schema_from_json(columns=columns)
 
-        return dataset, {}
+    def _load_schema_from_api(self, mode="staging"):
+        """Load schema from table config
 
-    @property
-    def owner_org(self):
-        """
-        Build `owner_org` field for each use case: table, dataset, new
-        or existing.
-        """
+        Args:
+            mode (bool): Which dataset to create [prod|staging].
 
-        # in case `self` refers to a CKAN table's metadata
-        if self.table_id and self.exists_in_ckan():
-            return self.dataset_metadata_obj.ckan_metadata.get("owner_org")
+        """
+        if self.table_exists(mode=mode):
+            logger.warning(
+                " {object} {object_id} allready exists, replacing schema!",
+                object_id=self.table_id,
+                object="Table",
+            )
 
-        # in case `self` refers to a new table's metadata
-        if self.table_id and not self.exists_in_ckan():
-            if self.dataset_metadata_obj.exists_in_ckan():
-                return self.dataset_metadata_obj.ckan_metadata.get("owner_org")
-            # mock `owner_org` for validation
-            return "3626e93d-165f-42b8-bde1-2e0972079694"
+        table_columns = self._get_columns_metadata_from_api()
+        columns = table_columns.get("partition_columns") + table_columns.get("columns")
 
-        # for datasets, `owner_org` must come from the YAML file
-        organization_id = "".join(self.local_metadata.get("organization") or [])
-        url = f"{self.CKAN_URL}/api/3/action/organization_show?id={organization_id}"
-        response = requests.get(url, timeout=10).json()
+        return self._load_schema_from_json(columns=columns)
 
-        if not response.get("success"):
-            raise BaseDosDadosException("Organization not found")
+    def _get_columns_from_data(
+        self,
+        data_sample_path=None,
+        source_format="csv",
+        mode="staging",
+    ):  # sourcery skip: low-code-quality
+        """
+        Get the partition columns from the structure of data_sample_path.
 
-        owner_org = response.get("result", {}).get("id")
+        Args:
+            data_sample_path (str, pathlib.PosixPath): Optional.
+                Data sample path to auto complete columns names
+                It supports Comma Delimited CSV, Apache Avro and
+                Apache Parquet.
+            source_format (str): Optional
+                Data source format. Only 'csv', 'avro' and 'parquet'
+                are supported. Defaults to 'csv'.
+        """
 
-        return owner_org
+        partition_columns = []
+        if isinstance(
+            data_sample_path,
+            (
+                str,
+                Path,
+            ),
+        ):
+            # Check if partitioned and get data sample and partition columns
+            data_sample_path = Path(data_sample_path)
+
+            if data_sample_path.is_dir():
+                data_sample_path = [
+                    f
+                    for f in data_sample_path.glob("**/*")
+                    if f.is_file() and f.suffix == f".{source_format}"
+                ][0]
+
+                partition_columns = [
+                    k.split("=")[0]
+                    for k in data_sample_path.as_posix().split("/")
+                    if "=" in k
+                ]
+
+            columns = Datatype(source_format).header(data_sample_path)
+
+        return {
+            "columns": [{"name": col, "type": "STRING"} for col in columns],
+            "partition_columns": [
+                {"name": col, "type": "STRING"} for col in partition_columns
+            ],
+        }
 
-    @property
-    def ckan_data_dict(self) -> dict:
-        """Helper function that structures local metadata for validation"""
+    def _get_columns_metadata_from_api(
+        self,
+    ):
+        """
+        Get columns and partition columns from API.
+        """
 
-        ckan_dataset, ckan_table = self.ckan_metadata_extended
+        columns = [
+            col
+            for col in self.table_config.get("columns")
+            if col.get("isPartition") is False
+        ]
+
+        partition_columns = [
+            col
+            for col in self.table_config.get("columns")
+            if col.get("isPartition") is True
+        ]
 
-        metadata = {
-            "id": ckan_dataset.get("id"),
-            "name": ckan_dataset.get("name") or self.dataset_id.replace("_", "-"),
-            "type": ckan_dataset.get("type") or "dataset",
-            "title": self.local_metadata.get("title"),
-            "private": ckan_dataset.get("private") or False,
-            "owner_org": self.owner_org,
-            "resources": ckan_dataset.get("resources", [])
-            or [{"resource_type": "external_link", "name": ""}]
-            or [{"resource_type": "information_request", "name": ""}],
-            "groups": [
-                {"name": group} for group in self.local_metadata.get("groups", []) or []
-            ],
-            "tags": [
-                {"name": tag} for tag in self.local_metadata.get("tags", []) or []
+        return {
+            "columns": [
+                {
+                    "name": col.get("name"),
+                    "type": col.get("bigqueryType").get("name"),
+                    "description": col.get("descriptionPt"),
+                }
+                for col in columns
             ],
-            "organization": {"name": self.local_metadata.get("organization")},
-            "extras": [
+            "partition_columns": [
                 {
-                    "key": "dataset_args",
-                    "value": {
-                        "short_description": self.local_metadata.get(
-                            "short_description"
-                        ),
-                        "description": self.local_metadata.get("description"),
-                        "ckan_url": self.local_metadata.get("ckan_url"),
-                        "github_url": self.local_metadata.get("github_url"),
-                    },
+                    "name": col.get("name"),
+                    "type": col.get("bigqueryType").get("name"),
+                    "description": col.get("descriptionPt"),
                 }
+                for col in partition_columns
             ],
         }
 
-        if self.table_id:
-            metadata["resources"] = [
+    def _parser_blobs_to_partition_dict(self) -> dict:
+        """
+        Extracts the partition information from the blobs.
+        """
+
+        if not self.table_exists(mode="staging"):
+            return
+        blobs = (
+            self.client["storage_staging"]
+            .bucket(self.bucket_name)
+            .list_blobs(prefix=f"staging/{self.dataset_id}/{self.table_id}/")
+        )
+        partitions_dict = {}
+        for blob in blobs:
+            for folder in blob.name.split("/"):
+                if "=" in folder:
+                    key = folder.split("=")[0]
+                    value = folder.split("=")[1]
+                    try:
+                        partitions_dict[key].append(value)
+                    except KeyError:
+                        partitions_dict[key] = [value]
+        return partitions_dict
+
+    def _get_columns_from_bq(self, mode="staging"):
+        if mode == "staging" and self.table_exists(mode="staging"):
+            schema = self._get_table_obj(mode="staging").schema
+        if mode == "prod" and self.table_exists(mode="prod"):
+            schema = self._get_table_obj(mode="prod").schema
+
+        partition_columns = list(self._parser_blobs_to_partition_dict().keys())
+
+        return {
+            "columns": [
                 {
-                    "id": ckan_table.get("id"),
-                    "description": self.local_metadata.get("description"),
-                    "name": self.local_metadata.get("table_id"),
-                    "resource_type": ckan_table.get("resource_type") or "bdm_table",
-                    "version": self.local_metadata.get("version"),
-                    "dataset_id": self.local_metadata.get("dataset_id"),
-                    "table_id": self.local_metadata.get("table_id"),
-                    "spatial_coverage": self.local_metadata.get("spatial_coverage"),
-                    "temporal_coverage": self.local_metadata.get("temporal_coverage"),
-                    "update_frequency": self.local_metadata.get("update_frequency"),
-                    "observation_level": self.local_metadata.get("observation_level"),
-                    "last_updated": self.local_metadata.get("last_updated"),
-                    "published_by": self.local_metadata.get("published_by"),
-                    "data_cleaned_by": self.local_metadata.get("data_cleaned_by"),
-                    "data_cleaning_description": self.local_metadata.get(
-                        "data_cleaning_description"
-                    ),
-                    "data_cleaning_code_url": self.local_metadata.get(
-                        "data_cleaning_code_url"
-                    ),
-                    "partner_organization": self.local_metadata.get(
-                        "partner_organization"
-                    ),
-                    "raw_files_url": self.local_metadata.get("raw_files_url"),
-                    "auxiliary_files_url": self.local_metadata.get(
-                        "auxiliary_files_url"
-                    ),
-                    "architecture_url": self.local_metadata.get("architecture_url"),
-                    "source_bucket_name": self.local_metadata.get("source_bucket_name"),
-                    "project_id_prod": self.local_metadata.get("project_id_prod"),
-                    "project_id_staging": self.local_metadata.get("project_id_staging"),
-                    "partitions": self.local_metadata.get("partitions"),
-                    "uncompressed_file_size": self.local_metadata.get(
-                        "uncompressed_file_size"
-                    ),
-                    "compressed_file_size": self.local_metadata.get(
-                        "compressed_file_size"
-                    ),
-                    "columns": self.local_metadata.get("columns"),
-                    "metadata_modified": self.local_metadata.get("metadata_modified"),
-                    "package_id": ckan_dataset.get("id"),
+                    "name": col.name,
+                    "type": col.field_type,
+                    "description": col.description,
                 }
-            ]
-
-        return metadata
+                for col in schema
+                if col.name not in partition_columns
+            ],
+            "partition_columns": [
+                {
+                    "name": col.name,
+                    "type": col.field_type,
+                    "description": col.description,
+                }
+                for col in schema
+                if col.name in partition_columns
+            ],
+        }
 
-    @property
-    @lru_cache(256)
-    def columns_schema(self) -> dict:
-        """Returns a dictionary with the schema of the columns"""
+    def _make_publish_sql(self):
+        """Create publish.sql with columns and bigquery_type"""
 
-        url = f"{self.CKAN_URL}/api/3/action/bd_bdm_columns_schema"
+        ### publish.sql header and instructions
+        publish_txt = """
+        /*
+        Query para publicar a tabela.
+
+        Esse é o lugar para:
+            - modificar nomes, ordem e tipos de colunas
+            - dar join com outras tabelas
+            - criar colunas extras (e.g. logs, proporções, etc.)
+
+        Qualquer coluna definida aqui deve também existir em `table_config.yaml`.
+
+        # Além disso, sinta-se à vontade para alterar alguns nomes obscuros
+        # para algo um pouco mais explícito.
+
+        TIPOS:
+            - Para modificar tipos de colunas, basta substituir STRING por outro tipo válido.
+            - Exemplo: `SAFE_CAST(column_name AS NUMERIC) column_name`
+            - Mais detalhes: https://cloud.google.com/bigquery/docs/reference/standard-sql/data-types
+        */
+        """
 
-        return requests.get(url, timeout=10).json().get("result")
+        table_columns = self._get_columns_from_bq(mode="staging")
+        columns = table_columns.get("partition_columns") + table_columns.get("columns")
 
-    @property
-    @lru_cache(256)
-    def metadata_schema(self) -> dict:
-        """Get metadata schema from CKAN API endpoint"""
+        # remove triple quotes extra space
+        publish_txt = inspect.cleandoc(publish_txt)
+        publish_txt = textwrap.dedent(publish_txt)
+
+        # add create table statement
+        project_id_prod = self.client["bigquery_prod"].project
+        publish_txt += f"\n\nCREATE OR REPLACE VIEW {project_id_prod}.{self.dataset_id}.{self.table_id} AS\nSELECT \n"
+
+        # sort columns by is_partition, partitions_columns come first
+
+        # add columns in publish.sql
+        for col in columns:
+            name = col.get("name")
+            bigquery_type = (
+                "STRING" if col.get("type") is None else col.get("type").upper()
+            )
 
-        if self.table_id:
-            table_url = f"{self.CKAN_URL}/api/3/action/bd_bdm_table_schema"
-            return requests.get(table_url, timeout=10).json().get("result")
+            publish_txt += f"SAFE_CAST({name} AS {bigquery_type}) {name},\n"
+        ## remove last comma
+        publish_txt = publish_txt[:-2] + "\n"
+
+        # add from statement
+        project_id_staging = self.client["bigquery_staging"].project
+        publish_txt += (
+            f"FROM {project_id_staging}.{self.dataset_id}_staging.{self.table_id} AS t"
+        )
 
-        dataset_url = f"{self.CKAN_URL}/api/3/action/bd_dataset_schema"
-        return requests.get(dataset_url, timeout=10).json().get("result")
+        return publish_txt
 
-    def exists_in_ckan(self) -> bool:
-        """Check if Metadata object refers to an existing CKAN package or reso
-        urce.
+    def table_exists(self, mode):
+        """Check if table exists in BigQuery.
 
-        Returns:
-            bool: The existence condition of the metadata in CKAN. `True` if i
-            t exists, `False` otherwise.
+        Args:
+            mode (str): Which dataset to check [prod|staging].
         """
 
-        if self.table_id:
-            url = f"{self.CKAN_URL}/api/3/action/bd_bdm_table_show?"
-            url += f"dataset_id={self.dataset_id}&table_id={self.table_id}"
-        else:
-            id = self.dataset_id.replace("_", "-")
-            # TODO: use `bd_bdm_dataset_show` when it's available for empty packages
-            url = f"{self.CKAN_URL}/api/3/action/package_show?id={id}"
-
-        exists_in_ckan = requests.get(url, timeout=10).json().get("success")
+        try:
+            ref = self._get_table_obj(mode=mode)
+        except google.api_core.exceptions.NotFound:
+            ref = None
+
+        return bool(ref)
+
+    def _get_biglake_connection(
+        self, set_biglake_connection_permissions=True, location=None, mode="staging"
+    ):
+        connection = Connection(name="biglake", location=location, mode="staging")
+        if not connection.exists:
+            try:
+                logger.info("Creating BigLake connection...")
+                connection.create()
+                logger.success("BigLake connection created!")
+            except google.api_core.exceptions.Forbidden as exc:
+                logger.error(
+                    "You don't have permission to create a BigLake connection. "
+                    "Please contact an admin to create one for you."
+                )
+                raise BaseDosDadosException(
+                    "You don't have permission to create a BigLake connection. "
+                    "Please contact an admin to create one for you."
+                ) from exc
+            except Exception as exc:
+                logger.error(
+                    "Something went wrong while creating the BigLake connection. "
+                    "Please contact an admin to create one for you."
+                )
+                raise BaseDosDadosException(
+                    "Something went wrong while creating the BigLake connection. "
+                    "Please contact an admin to create one for you."
+                ) from exc
+        if set_biglake_connection_permissions:
+            try:
+                logger.info("Setting permissions for BigLake service account...")
+                connection.set_biglake_permissions()
+                logger.success("Permissions set successfully!")
+            except google.api_core.exceptions.Forbidden as exc:
+                logger.error(
+                    "Could not set permissions for BigLake service account. "
+                    "Please make sure you have permissions to grant roles/storage.objectViewer"
+                    f" to the BigLake service account. ({connection.service_account})."
+                    " If you don't, please ask an admin to do it for you or set "
+                    "set_biglake_connection_permissions=False."
+                )
+                raise BaseDosDadosException(
+                    "Could not set permissions for BigLake service account. "
+                    "Please make sure you have permissions to grant roles/storage.objectViewer"
+                    f" to the BigLake service account. ({connection.service_account})."
+                    " If you don't, please ask an admin to do it for you or set "
+                    "set_biglake_connection_permissions=False."
+                ) from exc
+            except Exception as exc:
+                logger.error(
+                    "Something went wrong while setting permissions for BigLake service account. "
+                    "Please make sure you have permissions to grant roles/storage.objectViewer"
+                    f" to the BigLake service account. ({connection.service_account})."
+                    " If you don't, please ask an admin to do it for you or set "
+                    "set_biglake_connection_permissions=False."
+                )
+                raise BaseDosDadosException(
+                    "Something went wrong while setting permissions for BigLake service account. "
+                    "Please make sure you have permissions to grant roles/storage.objectViewer"
+                    f" to the BigLake service account. ({connection.service_account})."
+                    " If you don't, please ask an admin to do it for you or set "
+                    "set_biglake_connection_permissions=False."
+                ) from exc
 
-        return exists_in_ckan
+        return connection
 
-    def is_updated(self) -> bool:
-        """Check if a dataset or table is updated
+    def _get_table_description(self, mode="staging"):
+        """Adds table description to BigQuery table.
 
-        Returns:
-            bool: The update condition of local metadata. `True` if it corresp
-            onds to the most recent version of the given table or dataset's me
-            tadata in CKAN, `False` otherwise.
+        Args:
+            table_obj (google.cloud.bigquery.table.Table): Table object.
+            mode (str): Which dataset to check [prod|staging].
         """
+        table_path = self.table_full_name["prod"]
+        if mode == "staging":
+            description = f"staging table for `{table_path}`"
+        else:
+            try:
+                description = self.table_config.get("descriptionPt", "")
+            except BaseException:
+                logger.warning(
+                    f"table {self.table_id} does not have a description in the API."
+                )
+                description = "description not available in the API."
 
-        if not self.local_metadata.get("metadata_modified"):
-            return bool(not self.exists_in_ckan())
-        ckan_modified = self.ckan_metadata.get("metadata_modified")
-        local_modified = self.local_metadata.get("metadata_modified")
-        return ckan_modified == local_modified
+        return description
 
-    def create(
+    def create(  # pylint: disable=too-many-statements
         self,
-        if_exists: str = "raise",
-        columns: list = None,
-        partition_columns: list = None,
-        force_columns: bool = False,
-        table_only: bool = True,
-    ) -> Metadata:
-        """Create metadata file based on the current version saved to CKAN database
+        path=None,
+        source_format="csv",
+        if_table_exists="raise",
+        if_storage_data_exists="raise",
+        if_dataset_exists="pass",
+        dataset_is_public=True,
+        location=None,
+        chunk_size=None,
+        biglake_table=False,
+        set_biglake_connection_permissions=True,
+    ):
+        """Creates a BigQuery table in the staging dataset.
+
+        If a path is provided, data is automatically saved in storage,
+        and a datasets folder and BigQuery location are created, in addition to creating
+        the table and its configuration files.
+
+        The new table is located at `<dataset_id>_staging.<table_id>` in BigQuery.
+
+        Data can be found in Storage at `<bucket_name>/staging/<dataset_id>/<table_id>/*`
+        and is used to build the table.
+
+        The following data types are supported:
+
+        - Comma-Delimited CSV
+        - Apache Avro
+        - Apache Parquet
+
+        Data can also be partitioned following the Hive partitioning scheme
+        `<key1>=<value1>/<key2>=<value2>`; for example,
+        `year=2012/country=BR`. The partition is automatically detected by searching for `partitions`
+        in the `table_config.yaml` file.
 
         Args:
-            if_exists (str): Optional. What to do if config exists
-                * raise : Raises Conflict exception
-                * replace : Replaces config file with most recent
-                * pass : Do nothing
-            columns (list): Optional.
-                A `list` with the table columns' names.
-            partition_columns(list): Optional.
-                A `list` with the name of the table columns that partition the
-                 data.
-            force_columns (bool): Optional.
-                If set to `True`, overwrite CKAN's columns with the ones provi
-                ded.
-                If set to `False`, keep CKAN's columns instead of the ones pro
-                vided.
-            table_only (bool): Optional. If set to `True`, only `table_config.
-                yaml` is created, even if there is no `dataset_config.yaml` fo
-                r the correspondent dataset metadata. If set to `False`, both
-                files are created if `dataset_config.yaml` doesn't exist yet.
-                Defaults to `True`.
-
-        Returns:
-            Metadata: An instance of the `Metadata` class.
-
-        Raises:
-            FileExistsError: If the correspodent YAML configuration file alrea
-            dy exists and `if_exists` is set to `"raise"`.
-        """
-
-        # see: https://docs.python.org/3/reference/compound_stmts.html#function-definitions
-        columns = [] if columns is None else columns
-        partition_columns = [] if partition_columns is None else partition_columns
-
-        if self.filepath.exists() and if_exists == "raise":
-            raise FileExistsError(
-                f"{self.filepath} already exists."
-                + " Set the arg `if_exists` to `replace` to replace it."
-            )
-        if if_exists != "pass":
-            ckan_metadata = self.ckan_metadata
-
-            # Add local columns if
-            # 1. columns is empty and
-            # 2. force_columns is True
-
-            # TODO: Is this sufficient to add columns?
-            if self.table_id and (force_columns or not ckan_metadata.get("columns")):
-                ckan_metadata["columns"] = [{"name": c} for c in columns]
-
-            yaml_obj = build_yaml_object(
-                dataset_id=self.dataset_id,
-                table_id=self.table_id,
-                config=self.config,
-                schema=self.metadata_schema,
-                metadata=ckan_metadata,
-                columns_schema=self.columns_schema,
-                partition_columns=partition_columns,
-            )
-
-            self.filepath.parent.mkdir(parents=True, exist_ok=True)
-
-            with open(self.filepath, "w", encoding="utf-8") as file:
-                ruamel = ryaml.YAML()
-                ruamel.preserve_quotes = True
-                ruamel.indent(mapping=4, sequence=6, offset=4)
-                ruamel.dump(yaml_obj, file)
-
-            # if `dataset_config.yaml` doesn't exist but user wants to create
-            # it alongside `table_config.yaml`
-            dataset_config_exists = (
-                self.metadata_path / self.dataset_id / "dataset_config.yaml"
-            ).exists()
-            if self.table_id and not table_only and not dataset_config_exists:
-                self.dataset_metadata_obj.create(if_exists=if_exists)
-
-            logger.success(
-                " {object} {object_id} was {action}!",
-                object_id=self.table_id,
-                object="Metadata",
-                action="created",
-            )
+            path (str or pathlib.PosixPath): The path to the file to be uploaded to create the table.
+            source_format (str): Optional. The format of the data source. Only 'csv', 'avro', and 'parquet'
+                are supported. Defaults to 'csv'.
+            if_table_exists (str): Optional. Determines what to do if the table already exists:
+
+                * 'raise' : Raises a Conflict exception
+                * 'replace' : Replaces the table
+                * 'pass' : Does nothing
+            if_storage_data_exists (str): Optional. Determines what to do if the data already exists on your bucket:
+
+                * 'raise' : Raises a Conflict exception
+                * 'replace' : Replaces the table
+                * 'pass' : Does nothing
+            if_dataset_exists (str): Optional. Determines what to do if the dataset already exists:
+
+                * 'raise' : Raises a Conflict exception
+                * 'replace' : Replaces the dataset
+                * 'pass' : Does nothing
+            dataset_is_public (bool): Optional. Controls if the prod dataset is public or not. By default, staging datasets like `dataset_id_staging` are not public.
+            location (str): Optional. The location of the dataset data. List of possible region names locations: https://cloud.google.com/bigquery/docs/locations
+            chunk_size (int): Optional. The size of a chunk of data whenever iterating (in bytes). This must be a multiple of 256 KB per the API specification.
+                If not specified, the chunk_size of the blob itself is used. If that is not specified, a default value of 40 MB is used.
+            biglake_table (bool): Optional. Sets this as a BigLake table. BigLake tables allow end-users to query from external data (such as GCS) even if
+                they don't have access to the source data. IAM is managed like any other BigQuery native table. See https://cloud.google.com/bigquery/docs/biglake-intro for more on BigLake.
+            set_biglake_connection_permissions (bool): Optional. If set to `True`, attempts to grant the BigLake connection service account access to the table's data in GCS.
 
-        return self
+        """
 
-    def validate(self) -> bool:
-        """Validate dataset_config.yaml or table_config.yaml files.
-        The yaml file should be located at
-        metadata_path/dataset_id[/table_id/],
-        as defined in your config.toml
+        if path is None:
+            # Look if table data already exists at Storage
+            data = self.client["storage_staging"].list_blobs(
+                self.bucket_name, prefix=f"staging/{self.dataset_id}/{self.table_id}"
+            )
 
-        Returns:
-            bool:
-                True if the metadata is valid. False if it is invalid.
+            # Raise: Cannot create table without external data
+            if not data:
+                raise BaseDosDadosException(
+                    "You must provide a path for uploading data"
+                )
 
-        Raises:
-            BaseDosDadosException:
-                when the file has validation errors.
-        """
+        # Add data to storage
+        if isinstance(
+            path,
+            (
+                str,
+                Path,
+            ),
+        ):
+            Storage(self.dataset_id, self.table_id).upload(
+                path=path,
+                mode="staging",
+                if_exists=if_storage_data_exists,
+                chunk_size=chunk_size,
+            )
 
-        ckan = RemoteCKAN(self.CKAN_URL, user_agent="", apikey=None)
-        response = ckan.action.bd_dataset_validate(**self.ckan_data_dict)
+        # Create Dataset if it doesn't exist
 
-        if response.get("errors"):
-            error = {self.ckan_data_dict.get("name"): response["errors"]}
-            message = f"{self.filepath} has validation errors: {error}"
-            raise BaseDosDadosException(message)
+        dataset_obj = Dataset(
+            self.dataset_id,
+        )
 
-        logger.success(
-            " {object} {object_id} was {action}!",
-            object_id=self.table_id,
-            object="Metadata",
-            action="validated",
+        dataset_obj.create(
+            if_exists=if_dataset_exists,
+            mode="all",
+            location=location,
+            dataset_is_public=dataset_is_public,
         )
 
-        return True
+        if biglake_table:
+            biglake_connection = self._get_biglake_connection(
+                set_biglake_connection_permissions=set_biglake_connection_permissions,
+                location=location,
+                mode="staging",
+            )
+            biglake_connection_id = biglake_connection.connection_id
 
-    def publish(
-        self,
-        all: bool = False,
-        if_exists: str = "raise",
-        update_locally: bool = False,
-    ) -> dict:
-        """Publish local metadata modifications.
-        `Metadata.validate` is used to make sure no local invalid metadata is
-        published to CKAN. The `config.toml` `api_key` variable must be set
-        at the `[ckan]` section for this method to work.
+        table = bigquery.Table(self.table_full_name["staging"])
 
-        Args:
-            all (bool): Optional. If set to `True`, both `dataset_config.yaml`
-                and `table_config.yaml` are published for the given dataset_id
-                and table_id.
-            if_exists (str): Optional. What to do if config exists
-                * raise : Raises BaseDosDadosException if metadata already exi
-                sts in CKAN
-                * replace : Overwrite metadata in CKAN if it exists
-                * pass : Do nothing
-            update_locally (bool): Optional. If set to `True`, update the local
-                metadata with the one published to CKAN.
-
-        Returns:
-            dict:
-                In case of success, a `dict` with the modified data
-                is returned.
-
-        Raises:
-            BaseDosDadosException:
-                In case of CKAN's ValidationError or
-                NotAuthorized exceptions.
-        """
+        table.description = self._get_table_description(mode="staging")
 
-        # alert user if they don't have an api_key set up yet
-        if not self.CKAN_API_KEY:
-            raise BaseDosDadosException(
-                "You can't use `Metadata.publish` without setting an `api_key`"
-                "in your ~/.basedosdados/config.toml. Please set it like this:"
-                '\n\n```\n[ckan]\nurl="<CKAN_URL>"\napi_key="<API_KEY>"\n```'
+        table.external_data_configuration = Datatype(
+            dataset_id=self.dataset_id,
+            table_id=self.table_id,
+            schema=self._load_staging_schema_from_data(
+                data_sample_path=path, source_format=source_format
+            ),
+            source_format=source_format,
+            mode="staging",
+            bucket_name=self.bucket_name,
+            partitioned=self._is_partitioned(
+                data_sample_path=path, source_format=source_format
+            ),
+            biglake_connection_id=biglake_connection_id if biglake_table else None,
+        ).external_config
+
+        # When using BigLake tables, schema must be provided to the `Table` object
+        if biglake_table:
+            table.schema = self._load_staging_schema_from_data(
+                data_sample_path=path, source_format=source_format
             )
+            logger.info(f"Using BigLake connection {biglake_connection_id}")
 
-        # check if metadata exists in CKAN and handle if_exists options
-        if self.exists_in_ckan():
-            if if_exists == "raise":
-                raise BaseDosDadosException(
-                    f"{self.dataset_id or self.table_id} already exists in CKAN."
-                    f" Set the arg `if_exists` to `replace` to replace it."
+        # Lookup if table alreay exists
+        table_ref = None
+        with contextlib.suppress(google.api_core.exceptions.NotFound):
+            table_ref = self.client["bigquery_staging"].get_table(
+                self.table_full_name["staging"]
+            )
+
+        if isinstance(table_ref, google.cloud.bigquery.table.Table):
+            if if_table_exists == "pass":
+                return None
+
+            if if_table_exists == "raise":
+                raise FileExistsError(
+                    "Table already exists, choose replace if you want to overwrite it"
                 )
-            if if_exists == "pass":
-                return {}
 
-        ckan = RemoteCKAN(self.CKAN_URL, user_agent="", apikey=self.CKAN_API_KEY)
+        if if_table_exists == "replace" and self.table_exists(mode="staging"):
+            self.delete(mode="staging")
 
         try:
-            self.validate()
-
-            assert self.is_updated(), (
-                f"Could not publish metadata due to out-of-date config file. "
-                f"Please run `basedosdados metadata create {self.dataset_id} "
-                f"{self.table_id or ''}` to get the most recently updated met"
-                f"adata and apply your changes to it."
-            )
+            self.client["bigquery_staging"].create_table(table)
+        except google.api_core.exceptions.Forbidden as exc:
+            if biglake_table:
+                raise BaseDosDadosException(
+                    "Permission denied. The service account used to create the BigLake connection"
+                    " does not have permission to read data from the source bucket. Please grant"
+                    f" the service account {biglake_connection.service_account} the Storage Object Viewer"
+                    " (roles/storage.objectViewer) role on the source bucket (or on the project)."
+                    " Or, you can try running this again with set_biglake_connection_permissions=True."
+                ) from exc
+            raise BaseDosDadosException(
+                "Something went wrong when creating the table. Please check the logs for more information."
+            ) from exc
+        except Exception as exc:
+            raise BaseDosDadosException(
+                "Something went wrong when creating the table. Please check the logs for more information."
+            ) from exc
 
-            data_dict = self.ckan_data_dict.copy()
+        logger.success(
+            "{object} {object_id} was {action} in {mode}!",
+            object_id=self.table_id,
+            mode="staging",
+            object="Table",
+            action="created",
+        )
+        # return None
 
-            if self.table_id:
+    def update(self, mode="prod", custom_schema=None):
+        """Updates BigQuery schema and description.
+        Args:
+            mode (str): Optional.
+                Table of which table to update [prod]
+            not_found_ok (bool): Optional.
+                What to do if table is not found
+        """
 
-                # publish dataset metadata first if user wants to publish both
-                if all:
-                    self.dataset_metadata_obj.publish(if_exists=if_exists)
+        self._check_mode(mode)
 
-                data_dict = data_dict["resources"][0]
+        table = self._get_table_obj(mode)
 
-                published = ckan.call_action(
-                    action="resource_patch"
-                    if self.exists_in_ckan()
-                    else "resource_create",
-                    data_dict=data_dict,
-                )
+        table.description = self._get_table_description()
 
-            else:
-                data_dict["resources"] = []
+        # when mode is staging the table schema already exists
+        if mode == "prod" and custom_schema is None:
+            table.schema = self._load_schema_from_bq()
+        if mode == "prod" and custom_schema is not None:
+            table.schema = self._load_schema_from_json(custom_schema)
 
-                published = ckan.call_action(
-                    action="package_patch"
-                    if self.exists_in_ckan()
-                    else "package_create",
-                    data_dict=data_dict,
-                )
+        fields = ["description", "schema"]
 
-            # recreate local metadata YAML file with the published data
-            if published and update_locally:
-                self.create(if_exists="replace")
-                self.dataset_metadata_obj.create(if_exists="replace")
+        self.client[f"bigquery_prod"].update_table(table, fields=fields)
 
-            logger.success(
-                " {object} {object_id} was {action}!",
-                object_id=data_dict,
-                object="Metadata",
-                action="published",
-            )
+        logger.success(
+            " {object} {object_id} was {action} in {mode}!",
+            object_id=self.table_id,
+            mode=mode,
+            object="Table",
+            action="updated",
+        )
 
-            return published
+    def publish(self, if_exists="raise", custon_publish_sql=None, custom_schema=None):
+        """Creates BigQuery table at production dataset.
 
-        except (BaseDosDadosException, ValidationError) as e:
-            message = (
-                f"Could not publish metadata due to a validation error. Pleas"
-                f"e see the traceback below to get information on how to corr"
-                f"ect it.\n\n{repr(e)}"
-            )
-            raise BaseDosDadosException(message) from e
+        Table should be located at `<dataset_id>.<table_id>`.
 
-        except NotAuthorized as e:
-            message = (
-                "Could not publish metadata due to an authorization error. Pl"
-                "ease check if you set the `api_key` at the `[ckan]` section "
-                "of your ~/.basedosdados/config.toml correctly. You must be a"
-                "n authorized user to publish modifications to a dataset or t"
-                "able's metadata."
-            )
-            raise BaseDosDadosException(message) from e
+        It creates a view that uses the query from
+        `<metadata_path>/<dataset_id>/<table_id>/publish.sql`.
 
+        Make sure that all columns from the query also exists at
+        `<metadata_path>/<dataset_id>/<table_id>/table_config.sql`, including
+        the partitions.
 
-###############################################################################
-# Helper Functions
-###############################################################################
+        Args:
+            if_exists (str): Optional.
+                What to do if table exists.
 
+                * 'raise' : Raises Conflict exception
+                * 'replace' : Replace table
+                * 'pass' : Do nothing
 
-def handle_data(k, data, local_default=None):
-    """Parse API's response data so that it is used in the YAML configuration
-    files.
+        Todo:
 
-    Args:
-        k (str): a key of the CKAN API's response metadata dictionary.
-        data (dict): a dictionary of metadata generated from the API.
-        local_default (Any): the default value of the given key in ca
-            se its value is set to `None` in CKAN.
+            * Check if all required fields are filled
+        """
+        # TODO: review this method
 
-    Returns:
-        list: a list of metadata values
-    """
+        if if_exists == "replace" and self.table_exists(mode="prod"):
+            self.delete(mode="prod")
+        publish_sql = self._make_publish_sql()
+
+        ## create view using API metadata
+        if custon_publish_sql is None:
+            self.client["bigquery_prod"].query(publish_sql).result()
+            self.update()
+
+        ## create view using custon query
+        if custon_publish_sql is not None:
+            self.client["bigquery_prod"].query(custon_publish_sql).result()
+            ## update schema using a custom schema
+            if custom_schema is not None:
+                self.update(custom_schema=custom_schema)
 
-    # If no data is None then return a empty dict
-    data = data if data is not None else {}
-    # If no data is found for that key, uses local default
-    selected = data.get(k, local_default)
-
-    # In some cases like `tags`, `groups`, `organization`
-    # the API default is to return a dict or list[dict] with all info.
-    # But, we just use `name` to build the yaml
-    _selected = deepcopy(selected)
-
-    if _selected == []:
-        return _selected
-
-    if not isinstance(_selected, list):
-        _selected = [_selected]
-
-    if isinstance(_selected[0], dict):
-        if _selected[0].get("id") is not None:
-            return [s.get("name") for s in _selected]
-
-    return selected
-
-
-def handle_complex_fields(yaml_obj, k, properties, definitions, data):
-    """Parse complex fields and send each part of them to `handle_data`.
-
-    Args:
-        yaml_obj (ruamel.yaml.CommentedMap): A YAML object with complex fields
-            .
-        k (str): The name of the key of the complex field.
-        properties (dict): A dictionary that contains the description of the c
-            omplex field.
-        definitions (dict): A dictionary with the schemas of the each component
-            of the complex field.
-        data (dict): A dictionary with the metadata of the complex field.
+        logger.success(
+            " {object} {object_id} was {action}!",
+            object_id=self.table_id,
+            object="Table",
+            action="published",
+        )
 
-    Returns:
-        CommentedMap: A YAML object augmented with the complex field.
-    """
+    def delete(self, mode="all"):
+        """Deletes table in BigQuery.
 
-    yaml_obj[k] = ryaml.CommentedMap()
+        Args:
+            mode (str): Table of which table to delete [prod|staging]
+        """
 
-    # Parsing 'allOf': [{'$ref': '#/definitions/PublishedBy'}]
-    # To get PublishedBy
-    d = properties[k]["allOf"][0]["$ref"].split("/")[-1]
-    if "properties" in definitions[d].keys():
-        for dk, _ in definitions[d]["properties"].items():
-
-            yaml_obj[k][dk] = handle_data(
-                k=dk,
-                data=data.get(k, {}),
-            )
-
-    return yaml_obj
-
-
-def add_yaml_property(
-    yaml: CommentedMap,
-    properties: dict = None,
-    definitions: dict = None,
-    metadata: dict = None,
-    goal=None,
-    has_column=False,
-):
-    """Recursivelly adds properties to yaml to maintain order.
-
-    Args:
-        yaml (CommentedMap): A YAML object with complex fields.
-        properties (dict): A dictionary that contains the description of the c
-            omplex field.
-        definitions (dict): A dictionary with the schemas of each complex fiel
-            d.
-        metadata (dict): A dictionary with the metadata to fill the YAML.
-        goal (str): The next key to be added to the YAML.
-        has_column (bool): If the goal is a column, no comments are written.
-    """
+        self._check_mode(mode)
 
-    # see: https://docs.python.org/3/reference/compound_stmts.html#function-definitions
-    properties = {} if properties is None else properties
-    definitions = {} if definitions is None else definitions
-    metadata = {} if metadata is None else metadata
-
-    # Looks for the key
-    # If goal is none has to look for id_before == None
-    for key, property in properties.items():
-        goal_was_reached = key == goal
-        goal_was_reached |= property["yaml_order"]["id_before"] is None
-
-        if goal_was_reached:
-            if "allOf" in property:
-                yaml = handle_complex_fields(
-                    yaml_obj=yaml,
-                    k=key,
-                    properties=properties,
-                    definitions=definitions,
-                    data=metadata,
+        if mode == "all":
+            for m, n in self.table_full_name[mode].items():
+                self.client[f"bigquery_{m}"].delete_table(n, not_found_ok=True)
+                logger.info(
+                    " {object} {object_id}_{mode} was {action}!",
+                    object_id=self.table_id,
+                    mode=m["mode"],
+                    object="Table",
+                    action="deleted",
                 )
+        else:
+            self.client[f"bigquery_{mode}"].delete_table(
+                self.table_full_name[mode], not_found_ok=True
+            )
+            logger.info(
+                " {object} {object_id}_{mode} was {action}!",
+                object_id=self.table_id,
+                mode=mode,
+                object="Table",
+                action="deleted",
+            )
 
-                if yaml[key] == ordereddict():
-                    yaml[key] = handle_data(k=key, data=metadata)
-            else:
-                yaml[key] = handle_data(k=key, data=metadata)
-
-            # Add comments
-            comment = None
-            if not has_column:
-                description = properties[key].get("description", [])
-                comment = "\n" + "".join(description)
-            yaml.yaml_set_comment_before_after_key(key, before=comment)
-            break
-
-    # Return a ruaml object when property doesn't point to any other property
-    id_after = properties[key]["yaml_order"]["id_after"]
-
-    if id_after is None:
-        return yaml
-    if id_after not in properties.keys():
-        raise BaseDosDadosException(
-            f"Inconsistent YAML ordering: {id_after} is pointed to by {key}"
-            f" but doesn't have itself a `yaml_order` field in the JSON S"
-            f"chema."
-        )
-    updated_props = deepcopy(properties)
-    updated_props.pop(key)
-    return add_yaml_property(
-        yaml=yaml,
-        properties=updated_props,
-        definitions=definitions,
-        metadata=metadata,
-        goal=id_after,
-        has_column=has_column,
-    )
-
-
-def build_yaml_object(
-    dataset_id: str,
-    table_id: str,
-    config: dict,
-    schema: dict,
-    metadata: dict = None,
-    columns_schema: dict = None,
-    partition_columns: list = None,
-):
-    """Build a dataset_config.yaml or table_config.yaml
-
-    Args:
-        dataset_id (str): The dataset id.
-        table_id (str): The table id.
-        config (dict): A dict with the `basedosdados` client configurations.
-        schema (dict): A dict with the JSON Schema of the dataset or table.
-        metadata (dict): A dict with the metadata of the dataset or table.
-        columns_schema (dict): A dict with the JSON Schema of the columns of
-            the table.
-        partition_columns (list): A list with the partition columns of the
-            table.
+    def append(
+        self,
+        filepath,
+        partitions=None,
+        if_exists="replace",
+        chunk_size=None,
+        **upload_args,
+    ):
+        """Appends new data to existing BigQuery table.
 
-    Returns:
-        CommentedMap: A YAML object with the dataset or table metadata.
-    """
+        As long as the data has the same schema. It appends the data in the
+        filepath to the existing table.
 
-    # see: https://docs.python.org/3/reference/compound_stmts.html#function-definitions
-    metadata = {} if metadata is None else metadata
-    columns_schema = {} if columns_schema is None else columns_schema
-    partition_columns = [] if partition_columns is None else partition_columns
-
-    properties: dict = schema["properties"]
-    definitions: dict = schema["definitions"]
-
-    # Drop all properties without yaml_order
-    properties = {
-        key: value for key, value in properties.items() if value.get("yaml_order")
-    }
-
-    # Add properties
-    yaml = add_yaml_property(
-        yaml=ryaml.CommentedMap(),
-        properties=properties,
-        definitions=definitions,
-        metadata=metadata,
-    )
-
-    # Add columns
-    if metadata.get("columns"):
-        yaml["columns"] = []
-        for metadatum in metadata.get("columns"):
-            properties = add_yaml_property(
-                yaml=ryaml.CommentedMap(),
-                properties=columns_schema["properties"],
-                definitions=columns_schema["definitions"],
-                metadata=metadatum,
-                has_column=True,
-            )
-            yaml["columns"].append(properties)
-
-    # Add partitions in case of new dataset/talbe or local overwriting
-    if partition_columns and partition_columns != ["[]"]:
-        yaml["partitions"] = ""
-        for local_column in partition_columns:
-            for remote_column in yaml["columns"]:
-                if remote_column["name"] == local_column:
-                    remote_column["is_partition"] = True
-        yaml["partitions"] = partition_columns
-
-    # Nullify `partitions` field in case of other-than-None empty values
-    if yaml.get("partitions") == "":
-        yaml["partitions"] = None
-
-    if table_id:
-        # Add dataset_id and table_id
-        yaml["dataset_id"] = dataset_id
-        yaml["table_id"] = table_id
-
-        # Add gcloud config variables
-        yaml["source_bucket_name"] = str(config.get("bucket_name"))
-        yaml["project_id_prod"] = str(
-            config.get("gcloud-projects", {}).get("prod", {}).get("name")
+        Args:
+            filepath (str or pathlib.PosixPath): Where to find the file that you want to upload to create a table with
+            partitions (str, pathlib.PosixPath, dict): Optional.
+                Hive structured partition as a string or dict
+
+                * str : `<key>=<value>/<key2>=<value2>`
+                * dict: `dict(key=value, key2=value2)`
+            if_exists (str): 0ptional.
+                What to do if data with same name exists in storage
+
+                * 'raise' : Raises Conflict exception
+                * 'replace' : Replace table
+                * 'pass' : Do nothing
+            chunk_size (int): Optional
+                The size of a chunk of data whenever iterating (in bytes).
+                This must be a multiple of 256 KB per the API specification.
+                If not specified, the chunk_size of the blob itself is used. If that is not specified, a default value of 40 MB is used.
+        """
+        if not self.table_exists("staging"):
+            raise BaseDosDadosException(
+                "You cannot append to a table that does not exist"
+            )
+        Storage(
+            self.dataset_id,
+            self.table_id,
+        ).upload(
+            filepath,
+            mode="staging",
+            partitions=partitions,
+            if_exists=if_exists,
+            chunk_size=chunk_size,
+            **upload_args,
         )
-        yaml["project_id_staging"] = str(
-            config.get("gcloud-projects", {}).get("staging", {}).get("name")
+        logger.success(
+            " {object} {object_id} was {action}!",
+            object_id=self.table_id,
+            object="Table",
+            action="appended",
         )
-
-    return yaml
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `basedosdados-1.7.0b3/basedosdados/upload/storage.py` & `basedosdados-2.0.0b1/basedosdados/upload/storage.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-'''
+"""
 Class for managing the files in cloud storage.
-'''
+"""
 # pylint: disable=invalid-name, too-many-arguments, undefined-loop-variable,line-too-long,broad-except,R0801
 import time
 from pathlib import Path
 import sys
 import traceback
 
 from tqdm import tqdm
@@ -17,59 +17,57 @@
 
 
 class Storage(Base):
     """
     Manage files on Google Cloud Storage.
     """
 
-    def __init__(self, dataset_id=None, table_id=None, **kwargs):
+    def __init__(self, dataset_id, table_id, **kwargs):
         super().__init__(**kwargs)
 
         self.bucket = self.client["storage_staging"].bucket(self.bucket_name)
         self.dataset_id = dataset_id.replace("-", "_")
         self.table_id = table_id.replace("-", "_")
 
     @staticmethod
     def _resolve_partitions(partitions):
-
         if isinstance(partitions, dict):
-
             return "/".join(f"{k}={v}" for k, v in partitions.items()) + "/"
 
         if isinstance(partitions, str):
-
             if partitions.endswith("/"):
                 partitions = partitions[:-1]
 
             # If there is no partition
             if len(partitions) == 0:
                 return ""
 
             # It should fail if there is folder which is not a partition
             try:
                 # check if it fits rule
                 {b.split("=")[0]: b.split("=")[1] for b in partitions.split("/")}
             except IndexError as e:
-                raise Exception(f"The path {partitions} is not a valid partition") from e
+                raise Exception(
+                    f"The path {partitions} is not a valid partition"
+                ) from e
 
             return partitions + "/"
 
         raise Exception(f"Partitions format or type not accepted: {partitions}")
 
     def _build_blob_name(self, filename, mode, partitions=None):
-        '''
+        """
         Builds the blob name.
-        '''
+        """
 
         # table folder
         blob_name = f"{mode}/{self.dataset_id}/{self.table_id}/"
 
         # add partition folder
         if partitions is not None:
-
             blob_name += self._resolve_partitions(partitions)
 
         # add file name
         blob_name += filename
 
         return blob_name
 
@@ -102,15 +100,14 @@
                     "********************************************************"
                 )
             self.bucket.delete(force=True)
 
         self.client["storage_staging"].create_bucket(self.bucket)
 
         for folder in ["staging/", "raw/"]:
-
             self.bucket.blob(folder).upload_from_string("")
 
     def upload(
         self,
         path,
         mode="all",
         partitions=None,
@@ -199,57 +196,52 @@
 
         mode = (
             ["raw", "staging", "header", "auxiliary_files", "architecture"]
             if mode == "all"
             else [mode]
         )
         for m in mode:
-
             for filepath, part in tqdm(list(zip(paths, parts)), desc="Uploading files"):
-
                 blob_name = self._build_blob_name(filepath.name, m, part)
 
                 blob = self.bucket.blob(blob_name, chunk_size=chunk_size)
 
                 if not blob.exists() or if_exists == "replace":
-
                     upload_args["timeout"] = upload_args.get("timeout", None)
 
                     blob.upload_from_filename(str(filepath), **upload_args)
 
                 elif if_exists == "pass":
-
                     pass
 
                 else:
                     raise BaseDosDadosException(
                         f"Data already exists at {self.bucket_name}/{blob_name}. "
                         "If you are using Storage.upload then set if_exists to "
                         "'replace' to overwrite data \n"
                         "If you are using Table.create then set if_storage_data_exists "
                         "to 'replace' to overwrite data."
                     )
 
-        logger.success(
-            " {object} {filename}_{mode} was {action}!",
-            filename=filepath.name,
-            mode=mode,
-            object="File",
-            action="uploaded",
-        )
+            logger.success(
+                " {object} {filename}_{mode} was {action}!",
+                filename=filepath.name,
+                mode=m,
+                object="File",
+                action="uploaded",
+            )
 
     def download(
         self,
         filename="*",
-        savepath="",
+        savepath=".",
         partitions=None,
-        mode="raw",
+        mode="staging",
         if_not_exists="raise",
     ):
-
         """Download files from Google Storage from path `mode`/`dataset_id`/`table_id`/`partitions`/`filename` and replicate folder hierarchy
         on save,
 
         There are 5 modes:
         * `raw` : should contain raw files from datasource
         * `staging` : should contain pre-treated files ready to upload to BiqQuery
         * `header`: should contain the header of the tables
@@ -302,33 +294,37 @@
         if not blob_list:
             if if_not_exists == "raise":
                 raise FileNotFoundError(f"Could not locate files at {prefix}")
             return
 
         # download all blobs matching the search to given savepath
         for blob in tqdm(blob_list, desc="Download Blob"):
-
             # parse blob.name and get the csv file name
             csv_name = blob.name.split("/")[-1]
 
             # build folder path replicating storage hierarchy
             blob_folder = blob.name.replace(csv_name, "")
 
             # replicate folder hierarchy
-            (Path(savepath) / blob_folder).mkdir(parents=True, exist_ok=True)
+            savepath = Path(savepath)
+            (savepath / blob_folder).mkdir(parents=True, exist_ok=True)
 
             # download blob to savepath
-            blob.download_to_filename(filename=f"{savepath}/{blob.name}")
+            save_file_path = savepath / blob.name
+            print(save_file_path)
+
+            blob.download_to_filename(filename=save_file_path)
 
         logger.success(
-            " {object} {object_id}_{mode} was {action}!",
+            " {object} {object_id}_{mode} was {action} at: {path}!",
             object_id=self.dataset_id,
             mode=mode,
             object="File",
             action="downloaded",
+            path={str(savepath)},
         )
 
     def delete_file(self, filename, mode, partitions=None, not_found_ok=False):
         """Deletes file from path `<bucket_name>/<mode>/<dataset_id>/<table_id>/<partitions>/<filename>`.
 
         Args:
             filename (str): Name of the file to be deleted
@@ -350,15 +346,14 @@
         mode = (
             ["raw", "staging", "header", "auxiliary_files", "architecture"]
             if mode == "all"
             else [mode]
         )
 
         for m in mode:
-
             blob = self.bucket.blob(self._build_blob_name(filename, m, partitions))
 
             if blob.exists() or not blob.exists() and not not_found_ok:
                 blob.delete()
             else:
                 return
 
@@ -385,23 +380,21 @@
                 What to do if table not found
 
         """
 
         prefix = f"{mode}/{self.dataset_id}/{self.table_id}/"
 
         if bucket_name is not None:
-
             table_blobs = list(
                 self.client["storage_staging"]
                 .bucket(f"{bucket_name}")
                 .list_blobs(prefix=prefix)
             )
 
         else:
-
             table_blobs = list(self.bucket.list_blobs(prefix=prefix))
 
         if not table_blobs:
             if not_found_ok:
                 return
             raise FileNotFoundError(
                 f"Could not find the requested table {self.dataset_id}.{self.table_id}"
@@ -437,14 +430,15 @@
         )
 
     def copy_table(
         self,
         source_bucket_name="basedosdados",
         destination_bucket_name=None,
         mode="staging",
+        new_table_id=None,
     ):
         """Copies table from a source bucket to your bucket, sends request in batches.
 
         Args:
             source_bucket_name (str):
                 The bucket name from which to copy data. You can change it
                 to copy from other external bucket.
@@ -452,33 +446,33 @@
             destination_bucket_name (str): Optional
                 The bucket name where data will be copied to.
                 If None, defaults to the bucket initialized when instantiating the Storage object (You can check it with the
                 Storage().bucket property)
 
             mode (str): Folder of which dataset to update [raw|staging|header|auxiliary_files|architecture]
                 Folder of which dataset to update. Defaults to "staging".
+            new_table_id (str): Optional.
+                New table id to be copied to. If None, defaults to the table id initialized when instantiating the Storage object.
         """
 
         source_table_ref = list(
             self.client["storage_staging"]
             .bucket(source_bucket_name)
             .list_blobs(prefix=f"{mode}/{self.dataset_id}/{self.table_id}/")
         )
 
         if not source_table_ref:
             raise FileNotFoundError(
                 f"Could not find the requested table {self.dataset_id}.{self.table_id}"
             )
 
         if destination_bucket_name is None:
-
             destination_bucket = self.bucket
 
         else:
-
             destination_bucket = self.client["storage_staging"].bucket(
                 destination_bucket_name
             )
 
         # Divides source_table_ref list for maximum batch request size
         source_table_ref_chunks = [
             source_table_ref[i : i + 999] for i in range(0, len(source_table_ref), 999)
@@ -488,26 +482,33 @@
             tqdm(source_table_ref_chunks, desc="Copy Table Chunk")
         ):
             counter = 0
             while counter < 10:
                 try:
                     with self.client["storage_staging"].batch():
                         for blob in source_table:
+                            new_name = None
+                            if new_table_id:
+                                new_name = blob.name.replace(
+                                    self.table_id, new_table_id
+                                )
                             self.bucket.copy_blob(
                                 blob,
                                 destination_bucket=destination_bucket,
+                                new_name=new_name,
                             )
                     break
                 except Exception:
                     print(
                         f"Copy Table Chunk {i} | Attempt {counter}: copy operation starts again in 5 seconds...",
                     )
                     counter += 1
                     time.sleep(5)
                     traceback.print_exc(file=sys.stderr)
         logger.success(
-            " {object} {object_id}_{mode} was {action}!",
+            " {object} {object_id}_{mode} was {action} to {new_object_id}_{mode}!",
             object_id=self.table_id,
+            new_object_id=new_table_id if new_table_id else self.table_id,
             mode=mode,
             object="Table",
             action="copied",
         )
```

### Comparing `basedosdados-1.7.0b3/pyproject.toml` & `basedosdados-2.0.0b1/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -9,40 +9,33 @@
 license = "MIT"
 name = "basedosdados"
 packages = [
   {include = "basedosdados"},
 ]
 readme = "README.md"
 repository = "https://github.com/base-dos-dados/bases"
-version = "1.7.0-beta.3"
+version = "2.0.0-beta.1"
 
 [tool.poetry.scripts]
 basedosdados = 'basedosdados.cli.cli:cli'
 
 [tool.poetry.dependencies]
-Jinja2 = "3.0.3"
-ckanapi = "4.6"
-click = "8.0.3"
-google-api-python-client = "^2.66.0"
-google-cloud-bigquery = "2.30.1"
-google-cloud-bigquery-connection = "^1.7.3"
-google-cloud-bigquery-storage = "1.1.0"
-google-cloud-storage = "1.42.3"
-importlib-metadata = "^4.11.3"
-loguru = "^0.6.0"
-pandas = "^1.3.5"
-pandas-gbq = "^0.17.4"
-pandavro = "^1.6.0"
-pyaml = "20.4.0"
-pyarrow = "6.0.0"
-python = ">=3.7.1,<3.11"
-'ruamel.yaml' = "0.17.10"
-toml = "^0.10.2"
-tomlkit = "0.7.0"
-tqdm = "4.50.2"
+google-api-python-client = "^2.86.0"
+google-cloud-bigquery = "^3.10.0"
+google-cloud-bigquery-connection = "^1.12.0"
+google-cloud-bigquery-storage = "^2.19.1"
+google-cloud-storage = "^2.9.0"
+gql = "^3.4.1"
+loguru = "^0.7.0"
+pandas = "^2.0.1"
+pandas-gbq = "^0.19.2"
+pandavro = "^1.7.2"
+pydata-google-auth = "^1.8.0"
+python = ">=3.8, <3.11"
+tqdm = "^4.65.0"
 
 [tool.black]
 # Use the more relaxed max line length permitted in PEP8.
 exclude = '''
 /(
     \.eggs
   | \.git
@@ -51,15 +44,15 @@
   | \venv
   | build
   | dist
   | htmlcov
 )/
 '''
 line-length = 88
-target-version = ["py36", "py37", "py38"]
+target-version = ["py36", "py37", "py38", "py39"]
 
 [build-system]
 build-backend = "poetry.masonry.api"
 requires = ["poetry>=0.12"]
 
 [pytest]
 addopts = "-p no:warnings"
```

### Comparing `basedosdados-1.7.0b3/PKG-INFO` & `basedosdados-2.0.0b1/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,41 +1,35 @@
 Metadata-Version: 2.1
 Name: basedosdados
-Version: 1.7.0b3
+Version: 2.0.0b1
 Summary: Organizar e facilitar o acesso a dados brasileiros através de tabelas públicas no BigQuery.
 Home-page: https://github.com/base-dos-dados/bases
 License: MIT
 Author: Joao Carabetta
 Author-email: joao.carabetta@gmail.com
-Requires-Python: >=3.7.1,<3.11
+Requires-Python: >=3.8,<3.11
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
 Classifier: Topic :: Software Development :: Build Tools
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Requires-Dist: Jinja2 (==3.0.3)
-Requires-Dist: ckanapi (==4.6)
-Requires-Dist: click (==8.0.3)
-Requires-Dist: google-api-python-client (>=2.66.0,<3.0.0)
-Requires-Dist: google-cloud-bigquery (==2.30.1)
-Requires-Dist: google-cloud-bigquery-connection (>=1.7.3,<2.0.0)
-Requires-Dist: google-cloud-bigquery-storage (==1.1.0)
-Requires-Dist: google-cloud-storage (==1.42.3)
-Requires-Dist: importlib-metadata (>=4.11.3,<5.0.0)
-Requires-Dist: loguru (>=0.6.0,<0.7.0)
-Requires-Dist: pandas (>=1.3.5,<2.0.0)
-Requires-Dist: pandas-gbq (>=0.17.4,<0.18.0)
-Requires-Dist: pandavro (>=1.6.0,<2.0.0)
-Requires-Dist: pyaml (==20.4.0)
-Requires-Dist: pyarrow (==6.0.0)
-Requires-Dist: ruamel.yaml (==0.17.10)
-Requires-Dist: toml (>=0.10.2,<0.11.0)
-Requires-Dist: tomlkit (==0.7.0)
-Requires-Dist: tqdm (==4.50.2)
+Requires-Dist: google-api-python-client (>=2.86.0,<3.0.0)
+Requires-Dist: google-cloud-bigquery (>=3.10.0,<4.0.0)
+Requires-Dist: google-cloud-bigquery-connection (>=1.12.0,<2.0.0)
+Requires-Dist: google-cloud-bigquery-storage (>=2.19.1,<3.0.0)
+Requires-Dist: google-cloud-storage (>=2.9.0,<3.0.0)
+Requires-Dist: gql (>=3.4.1,<4.0.0)
+Requires-Dist: loguru (>=0.7.0,<0.8.0)
+Requires-Dist: pandas (>=2.0.1,<3.0.0)
+Requires-Dist: pandas-gbq (>=0.19.2,<0.20.0)
+Requires-Dist: pandavro (>=1.7.2,<2.0.0)
+Requires-Dist: pydata-google-auth (>=1.8.0,<2.0.0)
+Requires-Dist: tqdm (>=4.65.0,<5.0.0)
 Project-URL: Repository, https://github.com/base-dos-dados/bases
 Description-Content-Type: text/markdown
 
 # Python Package
 
 ## Desenvolvimento Linux e Mac: 
 
@@ -132,10 +126,7 @@
     poetry publish --build
     ```
 
 7. Faz merge da branch para a master
 8. Faz release usando a UI do GitHub
 9. Atualizar versão do pacote usada internamente
 
-
-
-
```

