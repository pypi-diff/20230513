# Comparing `tmp/tyba_client-0.2.2.tar.gz` & `tmp/tyba_client-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tyba_client-0.2.2.tar", max compression
+gzip compressed data, was "tyba_client-0.2.3.tar", max compression
```

## Comparing `tyba_client-0.2.2.tar` & `tyba_client-0.2.3.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1079 2021-11-05 19:13:19.360928 tyba_client-0.2.2/LICENSE
--rw-r--r--   0        0        0       17 2023-03-20 18:44:14.006817 tyba_client-0.2.2/README.md
--rw-r--r--   0        0        0      626 2023-05-05 20:51:39.595475 tyba_client-0.2.2/pyproject.toml
--rw-r--r--   0        0        0       22 2021-11-05 19:13:19.364928 tyba_client-0.2.2/tyba_client/__init__.py
--rw-r--r--   0        0        0     5526 2023-05-05 20:51:05.755185 tyba_client-0.2.2/tyba_client/client.py
--rw-r--r--   0        0        0    17644 2023-03-28 18:50:42.287839 tyba_client-0.2.2/tyba_client/models.py
--rw-r--r--   0        0        0     2037 2021-11-10 00:29:24.081096 tyba_client-0.2.2/tyba_client/utils.py
--rw-r--r--   0        0        0      857 1970-01-01 00:00:00.000000 tyba_client-0.2.2/setup.py
--rw-r--r--   0        0        0      889 1970-01-01 00:00:00.000000 tyba_client-0.2.2/PKG-INFO
+-rw-r--r--   0        0        0     1079 2021-11-05 19:13:19.360928 tyba_client-0.2.3/LICENSE
+-rw-r--r--   0        0        0       17 2023-03-20 18:44:14.006817 tyba_client-0.2.3/README.md
+-rw-r--r--   0        0        0      626 2023-05-12 22:36:04.307840 tyba_client-0.2.3/pyproject.toml
+-rw-r--r--   0        0        0       22 2021-11-05 19:13:19.364928 tyba_client-0.2.3/tyba_client/__init__.py
+-rw-r--r--   0        0        0     5526 2023-05-05 20:51:05.755185 tyba_client-0.2.3/tyba_client/client.py
+-rw-r--r--   0        0        0    17644 2023-03-28 18:50:42.287839 tyba_client-0.2.3/tyba_client/models.py
+-rw-r--r--   0        0        0     2037 2021-11-10 00:29:24.081096 tyba_client-0.2.3/tyba_client/utils.py
+-rw-r--r--   0        0        0      857 1970-01-01 00:00:00.000000 tyba_client-0.2.3/setup.py
+-rw-r--r--   0        0        0      889 1970-01-01 00:00:00.000000 tyba_client-0.2.3/PKG-INFO
```

### Comparing `tyba_client-0.2.2/LICENSE` & `tyba_client-0.2.3/LICENSE`

 * *Files identical despite different names*

### Comparing `tyba_client-0.2.2/pyproject.toml` & `tyba_client-0.2.3/pyproject.toml`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "tyba-client"
-version = "0.2.2"
+version = "0.2.3"
 description = "A Python API client for the Tyba Public API"
 authors = ["Tyler Nisonoff <tyler@tybaenergy.com>"]
 license = "MIT"
 readme = "README.md"
 include = [
     "LICENSE",
 ]
@@ -12,15 +12,15 @@
 [tool.poetry.dependencies]
 python = "^3.8"
 requests = "^2.25.1"
 dataclasses-json = "^0.5.4"
 marshmallow = "^3.12.1"
 pandas = "^1.3.2"
 tyba-financial-model = "^0.1.0"
-generation-models = "^0.1.0"
+generation-models = "^0.2.0"
 structlog = "^23.1.0"
 
 [tool.poetry.dev-dependencies]
 pytest = "^5.2"
 ipython = "^7.29.0"
 ipdb = "^0.13.9"
```

### Comparing `tyba_client-0.2.2/tyba_client/client.py` & `tyba_client-0.2.3/tyba_client/client.py`

 * *Files identical despite different names*

### Comparing `tyba_client-0.2.2/tyba_client/models.py` & `tyba_client-0.2.3/tyba_client/models.py`

 * *Files identical despite different names*

### Comparing `tyba_client-0.2.2/tyba_client/utils.py` & `tyba_client-0.2.3/tyba_client/utils.py`

 * *Files identical despite different names*

### Comparing `tyba_client-0.2.2/setup.py` & `tyba_client-0.2.3/setup.py`

 * *Files 13% similar despite different names*

```diff
@@ -5,24 +5,24 @@
 ['tyba_client']
 
 package_data = \
 {'': ['*']}
 
 install_requires = \
 ['dataclasses-json>=0.5.4,<0.6.0',
- 'generation-models>=0.1.0,<0.2.0',
+ 'generation-models>=0.2.0,<0.3.0',
  'marshmallow>=3.12.1,<4.0.0',
  'pandas>=1.3.2,<2.0.0',
  'requests>=2.25.1,<3.0.0',
  'structlog>=23.1.0,<24.0.0',
  'tyba-financial-model>=0.1.0,<0.2.0']
 
 setup_kwargs = {
     'name': 'tyba-client',
-    'version': '0.2.2',
+    'version': '0.2.3',
     'description': 'A Python API client for the Tyba Public API',
     'long_description': '# Tyba API Client',
     'author': 'Tyler Nisonoff',
     'author_email': 'tyler@tybaenergy.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

### Comparing `tyba_client-0.2.2/PKG-INFO` & `tyba_client-0.2.3/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 Metadata-Version: 2.1
 Name: tyba-client
-Version: 0.2.2
+Version: 0.2.3
 Summary: A Python API client for the Tyba Public API
 License: MIT
 Author: Tyler Nisonoff
 Author-email: tyler@tybaenergy.com
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: dataclasses-json (>=0.5.4,<0.6.0)
-Requires-Dist: generation-models (>=0.1.0,<0.2.0)
+Requires-Dist: generation-models (>=0.2.0,<0.3.0)
 Requires-Dist: marshmallow (>=3.12.1,<4.0.0)
 Requires-Dist: pandas (>=1.3.2,<2.0.0)
 Requires-Dist: requests (>=2.25.1,<3.0.0)
 Requires-Dist: structlog (>=23.1.0,<24.0.0)
 Requires-Dist: tyba-financial-model (>=0.1.0,<0.2.0)
 Description-Content-Type: text/markdown
```

