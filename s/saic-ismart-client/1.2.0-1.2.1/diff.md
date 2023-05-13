# Comparing `tmp/saic_ismart_client-1.2.0.tar.gz` & `tmp/saic_ismart_client-1.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "saic_ismart_client-1.2.0.tar", last modified: Sat May 13 12:31:28 2023, max compression
+gzip compressed data, was "saic_ismart_client-1.2.1.tar", last modified: Sat May 13 15:23:50 2023, max compression
```

## Comparing `saic_ismart_client-1.2.0.tar` & `saic_ismart_client-1.2.1.tar`

### file list

```diff
@@ -1,50 +1,50 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.759611 saic_ismart_client-1.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      732 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:31:28.759611 saic_ismart_client-1.2.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.747610 saic_ismart_client-1.2.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.751610 saic_ismart_client-1.2.0/src/saic_ismart_client/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.747610 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.751610 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.751610 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     3230 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    20928 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/common_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17038 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15431 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/data_model.py
--rw-r--r--   0 runner    (1001) docker     (123)    27857 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/saic_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.751610 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1519 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_Message_v1_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_Message_v2_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_Message_v3_0.py
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    13108 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      732 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     3230 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20928 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/common_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17038 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15431 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/data_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28333 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/src/saic_ismart_client/saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.434594 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1519 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 15:23:50.000000 saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:23:50.438594 saic_ismart_client-1.2.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_Message_v1_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_Message_v2_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_Message_v3_0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13108 2023-05-13 15:23:39.000000 saic_ismart_client-1.2.1/tests/test_saic_api.py
```

### Comparing `saic_ismart_client-1.2.0/LICENSE` & `saic_ismart_client-1.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/PKG-INFO` & `saic_ismart_client-1.2.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: saic_ismart_client
-Version: 1.2.0
+Version: 1.2.1
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.2.0/README.md` & `saic_ismart_client-1.2.1/README.md`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/pyproject.toml` & `saic_ismart_client-1.2.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "saic_ismart_client"
-version = "1.2.0"
+version = "1.2.1"
 authors = [
     { name = "Thomas Salm", email="saic-python-client@devtom.de"},
 ]
 dependencies = [
     "asn1tools >= 0.165.0",
     "requests >= 2.28.2",
     "urllib3 >= 1.26.14",
```

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/abrp_api.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/common_model.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/common_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/Message.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/data_model.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v1_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/Message.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/data_model.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v2_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/Message.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/data_model.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/ota_v3_0/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client/saic_api.py` & `saic_ismart_client-1.2.1/src/saic_ismart_client/saic_api.py`

 * *Files 2% similar despite different names*

```diff
@@ -66,18 +66,22 @@
             self.message = msg
 
     def __str__(self):
         return self.message
 
 
 class SaicApi:
-    def __init__(self, saic_uri: str, saic_user: str, saic_password: str):
+    def __init__(self, saic_uri: str, saic_user: str, saic_password: str, relogin_delay: int = None):
         self.saic_uri = saic_uri
         self.saic_user = saic_user
         self.saic_password = saic_password
+        if relogin_delay is None:
+            self.relogin_delay = 0
+        else:
+            self.relogin_delay = relogin_delay
         self.message_v1_1_coder = MessageCoderV11()
         self.message_V2_1_coder = MessageCoderV21()
         self.message_V3_0_coder = MessageCoderV30()
         self.cookies = None
         self.uid = ''
         self.token = ''
         self.token_expiration = None
@@ -405,15 +409,16 @@
         else:
             rsp = func
         rsp_msg = cast(AbstractMessage, rsp)
         while rsp_msg.application_data is None:
             if rsp_msg.body.error_message is not None:
                 self.handle_error(rsp_msg.body)
             else:
-                raise SaicApiException('API request returned no application data and no error message.')
+                logging.debug('API request returned no application data and no error message.')
+                time.sleep(float(AVG_SMS_DELIVERY_TIME))
 
             rsp_msg = func
         return rsp_msg
 
     def send_vehicle_control_command(self, vin_info: VinInfo, rvc_req_type: bytes, rvc_params: list,
                                      event_id: str = None) -> MessageV2:
         vehicle_control_req = OtaRvcReq()
@@ -583,14 +588,18 @@
               + f' protocol version: {message_body.application_data_protocol_version},'\
               + f' message: {message_body.error_message.decode()}'\
               + f' result code: {message_body.result}'
 
         if message_body.result == 2:
             # re-login
             logging.debug(message)
+            if self.relogin_delay > 0:
+                logging.warning(f'The SAIC user has been logged out. '
+                                + f'Waiting {self.relogin_delay} seconds before attempting another login')
+                time.sleep(float(self.relogin_delay))
             self.login()
         elif message_body.result == 4:
             # please try again later
             logging.debug(message)
             time.sleep(float(AVG_SMS_DELIVERY_TIME))
         else:
             logging.error(message)
```

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/PKG-INFO` & `saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: saic-ismart-client
-Version: 1.2.0
+Version: 1.2.1
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/SOURCES.txt` & `saic_ismart_client-1.2.1/src/saic_ismart_client.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/tests/test_Message_v1_1.py` & `saic_ismart_client-1.2.1/tests/test_Message_v1_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/tests/test_Message_v2_1.py` & `saic_ismart_client-1.2.1/tests/test_Message_v2_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/tests/test_Message_v3_0.py` & `saic_ismart_client-1.2.1/tests/test_Message_v3_0.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/tests/test_abrp_api.py` & `saic_ismart_client-1.2.1/tests/test_abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.0/tests/test_saic_api.py` & `saic_ismart_client-1.2.1/tests/test_saic_api.py`

 * *Files identical despite different names*

