# Comparing `tmp/cognite_gql_pygen-0.5.0.tar.gz` & `tmp/cognite_gql_pygen-0.6.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cognite_gql_pygen-0.5.0.tar", max compression
+gzip compressed data, was "cognite_gql_pygen-0.6.0.tar", max compression
```

## Comparing `cognite_gql_pygen-0.5.0.tar` & `cognite_gql_pygen-0.6.0.tar`

### file list

```diff
@@ -1,33 +1,33 @@
--rw-r--r--   0        0        0    11349 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/LICENSE
--rw-r--r--   0        0        0     4486 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/README.md
--rw-r--r--   0        0        0     8651 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/README.md
--rw-r--r--   0        0        0        0 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/__init__.py
--rw-r--r--   0        0        0      167 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/cdf/__init__.py
--rw-r--r--   0        0        0    19000 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/cdf/client_dm_v3.py
--rw-r--r--   0        0        0     3909 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/cdf/data_classes_dm_v3.py
--rw-r--r--   0        0        0     2593 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/cdf/get_client.py
--rwxr-xr-x   0        0        0      399 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/config.py
--rw-r--r--   0        0        0      192 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/custom_types/__init__.py
--rw-r--r--   0        0        0      236 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/custom_types/_scalars.py
--rw-r--r--   0        0        0      760 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/custom_types/jsonobject.py
--rw-r--r--   0        0        0     4724 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/custom_types/timestamp.py
--rw-r--r--   0        0        0      196 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/__init__.py
--rw-r--r--   0        0        0     6471 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/domain_client.py
--rw-r--r--   0        0        0     4065 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/domain_model.py
--rw-r--r--   0        0        0    19106 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/domain_model_api.py
--rw-r--r--   0        0        0     5929 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/relationship_api.py
--rw-r--r--   0        0        0     7060 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/schema.py
--rw-r--r--   0        0        0     3595 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/testing.py
--rw-r--r--   0        0        0     1423 2023-05-11 14:24:04.734456 cognite_gql_pygen-0.5.0/cognite/dm_clients/misc.py
--rw-r--r--   0        0        0        0 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/dm_clients/py.typed
--rw-r--r--   0        0        0       76 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/__init__.py
--rw-r--r--   0        0        0     1904 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/data_classes.py
--rw-r--r--   0        0        0     1560 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/generator.py
--rw-r--r--   0        0        0     7890 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/main.py
--rw-r--r--   0        0        0      596 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/misc.py
--rw-r--r--   0        0        0     1425 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/parser.py
--rw-r--r--   0        0        0     1334 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/templates/client.txt
--rw-r--r--   0        0        0      807 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/templates/schema.txt
--rw-r--r--   0        0        0       22 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/cognite/gqlpygen/version.py
--rw-r--r--   0        0        0     2059 2023-05-11 14:24:04.738456 cognite_gql_pygen-0.5.0/pyproject.toml
--rw-r--r--   0        0        0     5663 1970-01-01 00:00:00.000000 cognite_gql_pygen-0.5.0/PKG-INFO
+-rw-r--r--   0        0        0    11349 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/LICENSE
+-rw-r--r--   0        0        0     4493 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/README.md
+-rw-r--r--   0        0        0     8651 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/__init__.py
+-rw-r--r--   0        0        0      167 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/cdf/__init__.py
+-rw-r--r--   0        0        0    19000 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/cdf/client_dm_v3.py
+-rw-r--r--   0        0        0     3909 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/cdf/data_classes_dm_v3.py
+-rw-r--r--   0        0        0     2593 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/cdf/get_client.py
+-rwxr-xr-x   0        0        0      399 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/config.py
+-rw-r--r--   0        0        0      192 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/custom_types/__init__.py
+-rw-r--r--   0        0        0      236 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/custom_types/_scalars.py
+-rw-r--r--   0        0        0      760 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/custom_types/jsonobject.py
+-rw-r--r--   0        0        0     4724 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/custom_types/timestamp.py
+-rw-r--r--   0        0        0      196 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/__init__.py
+-rw-r--r--   0        0        0     6471 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/domain_client.py
+-rw-r--r--   0        0        0     4065 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/domain_model.py
+-rw-r--r--   0        0        0    19106 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/domain_model_api.py
+-rw-r--r--   0        0        0     5929 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/relationship_api.py
+-rw-r--r--   0        0        0     7060 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/schema.py
+-rw-r--r--   0        0        0     3595 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/testing.py
+-rw-r--r--   0        0        0     1423 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/misc.py
+-rw-r--r--   0        0        0        0 2023-05-13 21:34:12.633500 cognite_gql_pygen-0.6.0/cognite/dm_clients/py.typed
+-rw-r--r--   0        0        0       76 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/__init__.py
+-rw-r--r--   0        0        0     1904 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/data_classes.py
+-rw-r--r--   0        0        0     1560 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/generator.py
+-rw-r--r--   0        0        0     7890 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/main.py
+-rw-r--r--   0        0        0      596 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/misc.py
+-rw-r--r--   0        0        0     1425 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/parser.py
+-rw-r--r--   0        0        0     1334 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/templates/client.txt
+-rw-r--r--   0        0        0      807 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/templates/schema.txt
+-rw-r--r--   0        0        0       22 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/cognite/gqlpygen/version.py
+-rw-r--r--   0        0        0     2228 2023-05-13 21:34:12.637500 cognite_gql_pygen-0.6.0/pyproject.toml
+-rw-r--r--   0        0        0     5664 1970-01-01 00:00:00.000000 cognite_gql_pygen-0.6.0/PKG-INFO
```

### Comparing `cognite_gql_pygen-0.5.0/LICENSE` & `cognite_gql_pygen-0.6.0/LICENSE`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/README.md` & `cognite_gql_pygen-0.6.0/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -7,20 +7,20 @@
 This is the Cognite GraphQL Python Generator, `gqlpygen`. The purpose of this package is to help developers to
 work with Cognite Data Fusion's (CDF) Data Models (DM) in Python.
 
 **[DISCLAIMER!]** This project is in a highly experimental no guarantees are made for consistency between versions. The
 project may also become deprecated if the experimentation turns out to be a dead end.
 
 
-The core functionality is to provide a Python client that match a data model. This enables the developer the following
+The core functionality is to provide a Python client that matches a data model. This enables the developer the following
 benefits
 
 * Client side validation of the data before writing it to CDF.
-* Autocompletion matching the data model in the integrated developer environment (IDE). This is important as it enables:
-  * Discoverability of data model through Python.
+* Autocompletion is matching the data model in the integrated developer environment (IDE). This is important as it enables:
+  * Discoverability of a data model through Python.
   * Reduced typing errors in development.
 * Keeping the language domain specific for the developer. Instead of working with generic concepts such as instances,
   nodes, edges, the developer can work with the concepts in the data model.
 
 
 ## Installation
```

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/README.md` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/README.md`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/cdf/client_dm_v3.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/cdf/client_dm_v3.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/cdf/data_classes_dm_v3.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/cdf/data_classes_dm_v3.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/cdf/get_client.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/cdf/get_client.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/custom_types/jsonobject.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/custom_types/jsonobject.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/custom_types/timestamp.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/custom_types/timestamp.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/domain_client.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/domain_client.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/domain_model.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/domain_model.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/domain_model_api.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/domain_model_api.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/relationship_api.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/relationship_api.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/schema.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/schema.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/domain_modeling/testing.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/domain_modeling/testing.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/dm_clients/misc.py` & `cognite_gql_pygen-0.6.0/cognite/dm_clients/misc.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/gqlpygen/data_classes.py` & `cognite_gql_pygen-0.6.0/cognite/gqlpygen/data_classes.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/gqlpygen/generator.py` & `cognite_gql_pygen-0.6.0/cognite/gqlpygen/generator.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/gqlpygen/main.py` & `cognite_gql_pygen-0.6.0/cognite/gqlpygen/main.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/gqlpygen/misc.py` & `cognite_gql_pygen-0.6.0/cognite/gqlpygen/misc.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/gqlpygen/parser.py` & `cognite_gql_pygen-0.6.0/cognite/gqlpygen/parser.py`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/gqlpygen/templates/client.txt` & `cognite_gql_pygen-0.6.0/cognite/gqlpygen/templates/client.txt`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/cognite/gqlpygen/templates/schema.txt` & `cognite_gql_pygen-0.6.0/cognite/gqlpygen/templates/schema.txt`

 * *Files identical despite different names*

### Comparing `cognite_gql_pygen-0.5.0/pyproject.toml` & `cognite_gql_pygen-0.6.0/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "cognite-gql-pygen"
-version = "0.5.0"
+version = "0.6.0"
 description = "Cognite graphQL Python generation SDK"
 readme = "README.md"
 authors = ["Cognite <support@cognite.com>"]
 license = "Apache-2.0"
 
 packages = [{ include="cognite", from="." }]
 exclude = ["cognite/dm_clients/*.toml"]
@@ -40,26 +40,32 @@
 docopt = "^0.6.2"
 cachelib = "^0.10.2"
 retry = "^0.9.2"
 loguru = "^0.6.0"
 dynaconf = "^3.1.12"
 graphql-core = ">=3.2"
 Jinja2 = ">=3.1"
-packaging = "^23.1"
+packaging = ">=21.3"
 typing-extensions = "^4.5.0"
 
 [tool.poetry.dev-dependencies]
 twine = "*"
 pre-commit = "*"
 toml = "*"
 python-dotenv = "*"
 pytest = "*"
 pytest-cov = "*"
 pytest-mock = "*"
 faker = "*"
+mkdocs = "*"
+mkdocs-jupyter = "*"
+mkdocs-material-extensions = "*"
+mkdocs-git-revision-date-localized-plugin = "*"
+mkdocs-git-authors-plugin = "*"
+mkdocs-gitbook = "*"
 
 [tool.pytest.ini_options]
 filterwarnings = [
   "ignore::DeprecationWarning:pkg_resources",  # TODO check again with dynaconf>=3.2.0 (introduced in setuptools==67.5.0)
 ]
 addopts = "--doctest-modules"
```

### Comparing `cognite_gql_pygen-0.5.0/PKG-INFO` & `cognite_gql_pygen-0.6.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cognite-gql-pygen
-Version: 0.5.0
+Version: 0.6.0
 Summary: Cognite graphQL Python generation SDK
 License: Apache-2.0
 Author: Cognite
 Author-email: support@cognite.com
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3
@@ -18,15 +18,15 @@
 Requires-Dist: cognite-sdk[pandas] (>5.9.0)
 Requires-Dist: docopt (>=0.6.2,<0.7.0)
 Requires-Dist: dynaconf (>=3.1.12,<4.0.0)
 Requires-Dist: graphql-core (>=3.2)
 Requires-Dist: loguru (>=0.6.0,<0.7.0)
 Requires-Dist: msal (>=1.16.0,<2.0.0)
 Requires-Dist: numpy (>=1.23.2,<2.0.0)
-Requires-Dist: packaging (>=23.1,<24.0)
+Requires-Dist: packaging (>=21.3)
 Requires-Dist: pydantic (>=1.10)
 Requires-Dist: retry (>=0.9.2,<0.10.0)
 Requires-Dist: strawberry-graphql (>=0.156.4,<0.157.0)
 Requires-Dist: typer[all]
 Requires-Dist: typing-extensions (>=4.5.0,<5.0.0)
 Description-Content-Type: text/markdown
 
@@ -39,20 +39,20 @@
 This is the Cognite GraphQL Python Generator, `gqlpygen`. The purpose of this package is to help developers to
 work with Cognite Data Fusion's (CDF) Data Models (DM) in Python.
 
 **[DISCLAIMER!]** This project is in a highly experimental no guarantees are made for consistency between versions. The
 project may also become deprecated if the experimentation turns out to be a dead end.
 
 
-The core functionality is to provide a Python client that match a data model. This enables the developer the following
+The core functionality is to provide a Python client that matches a data model. This enables the developer the following
 benefits
 
 * Client side validation of the data before writing it to CDF.
-* Autocompletion matching the data model in the integrated developer environment (IDE). This is important as it enables:
-  * Discoverability of data model through Python.
+* Autocompletion is matching the data model in the integrated developer environment (IDE). This is important as it enables:
+  * Discoverability of a data model through Python.
   * Reduced typing errors in development.
 * Keeping the language domain specific for the developer. Instead of working with generic concepts such as instances,
   nodes, edges, the developer can work with the concepts in the data model.
 
 
 ## Installation
```

