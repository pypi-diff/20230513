# Comparing `tmp/saic_ismart_client-1.2.1.tar.gz` & `tmp/saic_ismart_client-1.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "saic_ismart_client-1.2.1.tar", last modified: Sat May 13 15:23:50 2023, max compression
+gzip compressed data, was "saic_ismart_client-1.2.2.tar", last modified: Sat May 13 16:28:54 2023, max compression
```

## Comparing `saic_ismart_client-1.2.1.tar` & `saic_ismart_client-1.2.2.tar`

### file list

```diff
@@ -1,50 +1,50 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      732 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     3230 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    20928 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/common_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17038 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15431 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/data_model.py
--rw-r--r--   0 runner    (1001) docker     (123)    28333 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/saic_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1519 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_Message_v1_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_Message_v2_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_Message_v3_0.py
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    13108 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      732 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.581215 saic_ismart_client-1.2.2/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.581215 saic_ismart_client-1.2.2/src/saic_ismart_client/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.581215 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     3230 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20928 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/common_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17038 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15431 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/data_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28469 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1519 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_Message_v1_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_Message_v2_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_Message_v3_0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13108 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_saic_api.py
```

### Comparing `saic_ismart_client-1.2.1/LICENSE` & `saic_ismart_client-1.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/PKG-INFO` & `saic_ismart_client-1.2.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: saic_ismart_client
-Version: 1.2.1
+Version: 1.2.2
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.2.1/README.md` & `saic_ismart_client-1.2.2/README.md`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/pyproject.toml` & `saic_ismart_client-1.2.2/pyproject.toml`

 * *Files 24% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "saic_ismart_client"
-version = "1.2.1"
+version = "1.2.2"
 authors = [
     { name = "Thomas Salm", email="saic-python-client@devtom.de"},
 ]
 dependencies = [
     "asn1tools >= 0.165.0",
     "requests >= 2.28.2",
     "urllib3 >= 1.26.14",
```

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/abrp_api.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/common_model.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/common_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/Message.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/data_model.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/Message.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/data_model.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/Message.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/data_model.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client/saic_api.py` & `saic_ismart_client-1.2.2/src/saic_ismart_client/saic_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -403,24 +403,27 @@
                 result.append(convert(message))
         return result
 
     def handle_retry(self, func, vin_info: VinInfo = None):
         if vin_info:
             rsp = func(vin_info)
         else:
-            rsp = func
+            rsp = func()
         rsp_msg = cast(AbstractMessage, rsp)
         while rsp_msg.application_data is None:
             if rsp_msg.body.error_message is not None:
                 self.handle_error(rsp_msg.body)
             else:
                 logging.debug('API request returned no application data and no error message.')
                 time.sleep(float(AVG_SMS_DELIVERY_TIME))
 
-            rsp_msg = func
+            if vin_info:
+                rsp_msg = func(vin_info, rsp_msg.body.event_id)
+            else:
+                rsp_msg = func(rsp_msg.body.event_id)
         return rsp_msg
 
     def send_vehicle_control_command(self, vin_info: VinInfo, rvc_req_type: bytes, rvc_params: list,
                                      event_id: str = None) -> MessageV2:
         vehicle_control_req = OtaRvcReq()
         vehicle_control_req.rvc_req_type = rvc_req_type
         for p in rvc_params:
```

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/PKG-INFO` & `saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: saic-ismart-client
-Version: 1.2.1
+Version: 1.2.2
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/SOURCES.txt` & `saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/tests/test_Message_v1_1.py` & `saic_ismart_client-1.2.2/tests/test_Message_v1_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/tests/test_Message_v2_1.py` & `saic_ismart_client-1.2.2/tests/test_Message_v2_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/tests/test_Message_v3_0.py` & `saic_ismart_client-1.2.2/tests/test_Message_v3_0.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/tests/test_abrp_api.py` & `saic_ismart_client-1.2.2/tests/test_abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.1/tests/test_saic_api.py` & `saic_ismart_client-1.2.2/tests/test_saic_api.py`

 * *Files identical despite different names*

