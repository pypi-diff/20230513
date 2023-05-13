# Comparing `tmp/saic_ismart_client-1.2.2.tar.gz` & `tmp/saic_ismart_client-1.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "saic_ismart_client-1.2.2.tar", last modified: Sat May 13 16:28:54 2023, max compression
+gzip compressed data, was "saic_ismart_client-1.2.3.tar", last modified: Sat May 13 20:40:35 2023, max compression
```

## Comparing `saic_ismart_client-1.2.2.tar` & `saic_ismart_client-1.2.3.tar`

### file list

```diff
@@ -1,50 +1,50 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      732 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.581215 saic_ismart_client-1.2.2/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.581215 saic_ismart_client-1.2.2/src/saic_ismart_client/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.581215 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     3230 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    20928 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/common_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17038 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15431 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/data_model.py
--rw-r--r--   0 runner    (1001) docker     (123)    28469 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/src/saic_ismart_client/saic_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1519 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 16:28:54.000000 saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:28:54.585215 saic_ismart_client-1.2.2/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_Message_v1_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_Message_v2_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_Message_v3_0.py
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    13108 2023-05-13 16:28:43.000000 saic_ismart_client-1.2.2/tests/test_saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.500617 saic_ismart_client-1.2.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 20:40:35.500617 saic_ismart_client-1.2.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      732 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 20:40:35.500617 saic_ismart_client-1.2.3/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.492617 saic_ismart_client-1.2.3/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/src/saic_ismart_client/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.492617 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     3230 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20928 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/common_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v1_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v1_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v1_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v2_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v2_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18407 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v2_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v3_0/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v3_0/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15431 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v3_0/data_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28614 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/src/saic_ismart_client/saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/src/saic_ismart_client.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 20:40:35.000000 saic_ismart_client-1.2.3/src/saic_ismart_client.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1519 2023-05-13 20:40:35.000000 saic_ismart_client-1.2.3/src/saic_ismart_client.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 20:40:35.000000 saic_ismart_client-1.2.3/src/saic_ismart_client.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 20:40:35.000000 saic_ismart_client-1.2.3/src/saic_ismart_client.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 20:40:35.000000 saic_ismart_client-1.2.3/src/saic_ismart_client.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:40:35.496617 saic_ismart_client-1.2.3/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/tests/test_Message_v1_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/tests/test_Message_v2_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/tests/test_Message_v3_0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/tests/test_abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16491 2023-05-13 20:40:24.000000 saic_ismart_client-1.2.3/tests/test_saic_api.py
```

### Comparing `saic_ismart_client-1.2.2/LICENSE` & `saic_ismart_client-1.2.3/LICENSE`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/PKG-INFO` & `saic_ismart_client-1.2.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: saic_ismart_client
-Version: 1.2.2
+Version: 1.2.3
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.2.2/README.md` & `saic_ismart_client-1.2.3/README.md`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/pyproject.toml` & `saic_ismart_client-1.2.3/pyproject.toml`

 * *Files 24% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "saic_ismart_client"
-version = "1.2.2"
+version = "1.2.3"
 authors = [
     { name = "Thomas Salm", email="saic-python-client@devtom.de"},
 ]
 dependencies = [
     "asn1tools >= 0.165.0",
     "requests >= 2.28.2",
     "urllib3 >= 1.26.14",
```

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/abrp_api.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/common_model.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/common_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/Message.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v1_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v1_1/data_model.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v1_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/Message.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v2_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v2_1/data_model.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v2_1/data_model.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,13 @@
 from typing import cast
 
 from saic_ismart_client.common_model import Asn1Type, ApplicationData
 
+FIELD_FAILURE_TYPE = 'failureType'
+FIELD_RVC_REQ_STS = 'rvcReqSts'
 FIELD_VALUE = 'value'
 FIELD_ID = 'id'
 FIELD_VEHICLE_ALERTS = 'vehicleAlerts'
 FIELD_SECONDS = 'seconds'
 FIELD_ALTITUDE = 'altitude'
 FIELD_LONGITUDE = 'longitude'
 FIELD_LATITUDE = 'latitude'
@@ -409,7 +411,37 @@
         return (
                 self.get_basic_vehicle_status().engine_status != 1
                 or self.get_basic_vehicle_status().hand_brake
         )
 
     def is_engine_running(self) -> bool:
         return self.get_basic_vehicle_status().engine_status == 1
+
+
+class OtaRvcStatus25857(ApplicationData):
+    def __init__(self):
+        super().__init__('OTARVCStatus25857')
+        self.rvcReqType = None  # OCTET STRING(SIZE(1)),
+        self.rvcReqSts = None  # OCTET STRING(SIZE(1)),
+        self.failureType = None  # INTEGER(0..255) OPTIONAL,
+        self.gpsPosition = None  # RvsPosition(1),
+        self.basicVehicleStatus = None  # RvsBasicStatus25857(1)
+
+    def get_data(self) -> dict:
+        data = {
+            FIELD_RVC_REQ_TYPE: self.rvcReqType,
+            FIELD_RVC_REQ_STS: self.rvcReqSts,
+            FIELD_GPS_POSITION: self.gpsPosition.get_data(),
+            FIELD_BASIC_VEHICLE_STATUS: self.basicVehicleStatus.get_data()
+        }
+        self.add_optional_field_to_data(data, FIELD_FAILURE_TYPE, self.failureType)
+        return data
+
+    def init_from_dict(self, data: dict):
+        self.rvcReqType = data.get(FIELD_RVC_REQ_TYPE)
+        self.rvcReqSts = data.get(FIELD_RVC_REQ_STS)
+        self.gpsPosition = RvsPosition()
+        self.gpsPosition.init_from_dict(data.get(FIELD_GPS_POSITION))
+        self.basicVehicleStatus = RvsBasicStatus25857()
+        self.basicVehicleStatus.init_from_dict(data.get(FIELD_BASIC_VEHICLE_STATUS))
+        if FIELD_FAILURE_TYPE in data:
+            self.failureType = data.get(FIELD_FAILURE_TYPE)
```

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/Message.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v3_0/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/ota_v3_0/data_model.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/ota_v3_0/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client/saic_api.py` & `saic_ismart_client-1.2.3/src/saic_ismart_client/saic_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 from saic_ismart_client.common_model import MessageV2, MessageBodyV2, Header, AbstractMessageBody, AbstractMessage
 from saic_ismart_client.ota_v1_1.Message import MessageCoderV11
 from saic_ismart_client.ota_v1_1.data_model import VinInfo, MpUserLoggingInReq, MpUserLoggingInRsp, AlarmSwitchReq, \
     MpAlarmSettingType, AlarmSwitch, MessageBodyV11, MessageV11, MessageListReq, StartEndNumber, MessageListResp, \
     Timestamp, Message, AbortSendMessageReq
 from saic_ismart_client.ota_v2_1.Message import MessageCoderV21
 from saic_ismart_client.ota_v2_1.data_model import OtaRvmVehicleStatusReq, OtaRvmVehicleStatusResp25857, OtaRvcReq,\
-    RvcReqParam
+    RvcReqParam, OtaRvcStatus25857
 from saic_ismart_client.ota_v3_0.Message import MessageCoderV30, MessageV30, MessageBodyV30
 from saic_ismart_client.ota_v3_0.data_model import OtaChrgMangDataResp
 
 UID_INIT = '0000000000000000000000000000000000000000000000000#'
 AVG_SMS_DELIVERY_TIME = 15
 logging.basicConfig(format='%(asctime)s %(message)s', level=logging.INFO)
 
@@ -176,19 +176,19 @@
         self.message_V2_1_coder.decode_response(vehicle_status_rsp_hex, vehicle_status_rsp_msg)
         self.publish_json_response(application_id, application_data_protocol_version, vehicle_status_rsp_msg.get_data())
         return vehicle_status_rsp_msg
 
     def get_vehicle_status_with_retry(self, vin_info: VinInfo) -> MessageV2:
         return self.handle_retry(self.get_vehicle_status, vin_info)
 
-    def lock_vehicle(self, vin_info: VinInfo) -> None:
+    def lock_vehicle(self, vin_info: VinInfo) -> MessageV2:
         rvc_params = []
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x01', rvc_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x01', rvc_params)
 
-    def unlock_vehicle(self, vin_info: VinInfo) -> None:
+    def unlock_vehicle(self, vin_info: VinInfo) -> MessageV2:
         rvc_params = []
         param1 = RvcReqParam()
         param1.param_id = 4
         param1.param_value = b'\x00'
         rvc_params.append(param1)
 
         param2 = RvcReqParam()
@@ -207,45 +207,45 @@
         rvc_params.append(param4)
 
         param5 = RvcReqParam()
         param5.param_id = 255
         param5.param_value = b'\x00'
         rvc_params.append(param5)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x02', rvc_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x02', rvc_params)
 
-    def start_rear_window_heat(self, vin_info: VinInfo):
+    def start_rear_window_heat(self, vin_info: VinInfo) -> MessageV2:
         rvc_params = []
         param1 = RvcReqParam()
         param1.param_id = 23
         param1.param_value = b'\x01'
         rvc_params.append(param1)
 
         param2 = RvcReqParam()
         param2.param_id = 255
         param2.param_value = b'\x00'
         rvc_params.append(param2)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x20', rvc_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x20', rvc_params)
 
-    def stop_rear_window_heat(self, vin_info: VinInfo):
+    def stop_rear_window_heat(self, vin_info: VinInfo) -> MessageV2:
         rvc_params = []
         param1 = RvcReqParam()
         param1.param_id = 23
         param1.param_value = b'\x00'
         rvc_params.append(param1)
 
         param2 = RvcReqParam()
         param2.param_id = 255
         param2.param_value = b'\x00'
         rvc_params.append(param2)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x20', rvc_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x20', rvc_params)
 
-    def start_ac(self, vin_info: VinInfo):
+    def start_ac(self, vin_info: VinInfo) -> MessageV2:
         rcv_params = []
         param1 = RvcReqParam()
         param1.param_id = 19
         param1.param_value = b'\x02'
         rcv_params.append(param1)
 
         param2 = RvcReqParam()
@@ -254,17 +254,17 @@
         rcv_params.append(param2)
 
         param3 = RvcReqParam()
         param3.param_id = 255
         param3.param_value = b'\x00'
         rcv_params.append(param3)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
 
-    def stop_ac(self, vin_info: VinInfo):
+    def stop_ac(self, vin_info: VinInfo) -> MessageV2:
         rcv_params = []
         param1 = RvcReqParam()
         param1.param_id = 19
         param1.param_value = b'\x00'
         rcv_params.append(param1)
 
         param2 = RvcReqParam()
@@ -273,17 +273,17 @@
         rcv_params.append(param2)
 
         param3 = RvcReqParam()
         param3.param_id = 255
         param3.param_value = b'\x00'
         rcv_params.append(param3)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
 
-    def start_ac_blowing(self, vin_info: VinInfo):
+    def start_ac_blowing(self, vin_info: VinInfo) -> MessageV2:
         rcv_params = []
         param1 = RvcReqParam()
         param1.param_id = 19
         param1.param_value = b'\x01'
         rcv_params.append(param1)
 
         param2 = RvcReqParam()
@@ -297,17 +297,17 @@
         rcv_params.append(param3)
 
         param4 = RvcReqParam()
         param4.param_id = 255
         param4.param_value = b'\x00'
         rcv_params.append(param4)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
 
-    def stop_ac_blowing(self, vin_info: VinInfo):
+    def stop_ac_blowing(self, vin_info: VinInfo) -> MessageV2:
         rcv_params = []
         param1 = RvcReqParam()
         param1.param_id = 19
         param1.param_value = b'\x00'
         rcv_params.append(param1)
 
         param2 = RvcReqParam()
@@ -321,17 +321,17 @@
         rcv_params.append(param3)
 
         param4 = RvcReqParam()
         param4.param_id = 255
         param4.param_value = b'\x00'
         rcv_params.append(param4)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
 
-    def start_front_defrost(self, vin_info: VinInfo):
+    def start_front_defrost(self, vin_info: VinInfo) -> MessageV2:
         rcv_params = []
         param1 = RvcReqParam()
         param1.param_id = 19
         param1.param_value = b'\x05'
         rcv_params.append(param1)
 
         param2 = RvcReqParam()
@@ -345,17 +345,17 @@
         rcv_params.append(param3)
 
         param4 = RvcReqParam()
         param4.param_id = 255
         param4.param_value = b'\x00'
         rcv_params.append(param4)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
 
-    def stop_front_defrost(self, vin_info: VinInfo):
+    def stop_front_defrost(self, vin_info: VinInfo) -> MessageV2:
         rcv_params = []
         param1 = RvcReqParam()
         param1.param_id = 19
         param1.param_value = b'\x00'
         rcv_params.append(param1)
 
         param2 = RvcReqParam()
@@ -369,33 +369,28 @@
         rcv_params.append(param3)
 
         param4 = RvcReqParam()
         param4.param_id = 255
         param4.param_value = b'\x00'
         rcv_params.append(param4)
 
-        self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
+        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params)
 
-    def send_vehicle_ctrl_cmd_with_retry(self, vin_info: VinInfo, rvc_req_type: bytes, rvc_params: list) -> None:
+    def send_vehicle_ctrl_cmd_with_retry(self, vin_info: VinInfo, rvc_req_type: bytes, rvc_params: list) -> MessageV2:
         vehicle_control_cmd_rsp_msg = self.send_vehicle_control_command(vin_info, rvc_req_type, rvc_params)
-        retry = 1
-        while (
-                vehicle_control_cmd_rsp_msg.body.error_message is not None
-                and retry < 3
-        ):
-            self.handle_error(vehicle_control_cmd_rsp_msg.body)
+        while vehicle_control_cmd_rsp_msg.application_data is None:
+            if vehicle_control_cmd_rsp_msg.body.error_message is not None:
+                self.handle_error(vehicle_control_cmd_rsp_msg.body)
+            else:
+                logging.debug('API request returned no application data and no error message.')
+                time.sleep(float(AVG_SMS_DELIVERY_TIME))
 
-            event_id = vehicle_control_cmd_rsp_msg.body.event_id
             vehicle_control_cmd_rsp_msg = self.send_vehicle_control_command(vin_info, rvc_req_type, rvc_params,
-                                                                            event_id)
-            retry += 1
-
-        if vehicle_control_cmd_rsp_msg.body.error_message is not None:
-            raise SaicApiException(vehicle_control_cmd_rsp_msg.body.error_message.decode(),
-                                   vehicle_control_cmd_rsp_msg.body.result)
+                                                                            vehicle_control_cmd_rsp_msg.body.event_id)
+        return vehicle_control_cmd_rsp_msg
 
     def get_message_list_with_retry(self) -> list:
         message_list_rsp_msg = self.handle_retry(self.get_message_list)
 
         result = []
         if message_list_rsp_msg.application_data is not None:
             message_list_rsp = cast(MessageListResp, message_list_rsp_msg.application_data)
@@ -440,15 +435,15 @@
         self.publish_json_request(application_id, application_data_protocol_version,
                                   vehicle_control_cmd_req_msg.get_data())
         vehicle_control_cmd_req_msg_hex = self.message_V2_1_coder.encode_request(vehicle_control_cmd_req_msg)
         self.publish_raw_request(application_id, application_data_protocol_version, vehicle_control_cmd_req_msg_hex)
         vehicle_control_cmd_rsp_msg_hex = self.send_request(vehicle_control_cmd_req_msg_hex,
                                                             urllib.parse.urljoin(self.saic_uri, '/TAP.Web/ota.mpv21'))
         self.publish_raw_response(application_id, application_data_protocol_version, vehicle_control_cmd_rsp_msg_hex)
-        vehicle_control_cmd_rsp_msg = MessageV2(MessageBodyV2())
+        vehicle_control_cmd_rsp_msg = MessageV2(MessageBodyV2(), OtaRvcStatus25857())
         self.message_V2_1_coder.decode_response(vehicle_control_cmd_rsp_msg_hex, vehicle_control_cmd_rsp_msg)
         self.publish_json_response(application_id, application_data_protocol_version,
                                    vehicle_control_cmd_rsp_msg.get_data())
         return vehicle_control_cmd_rsp_msg
 
     def get_charging_status(self, vin_info: VinInfo, event_id: str = None) -> MessageV30:
         chrg_mgmt_data_req_msg = MessageV30(MessageBodyV30())
```

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/PKG-INFO` & `saic_ismart_client-1.2.3/src/saic_ismart_client.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: saic-ismart-client
-Version: 1.2.2
+Version: 1.2.3
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.2.2/src/saic_ismart_client.egg-info/SOURCES.txt` & `saic_ismart_client-1.2.3/src/saic_ismart_client.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/tests/test_Message_v1_1.py` & `saic_ismart_client-1.2.3/tests/test_Message_v1_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/tests/test_Message_v2_1.py` & `saic_ismart_client-1.2.3/tests/test_Message_v2_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/tests/test_Message_v3_0.py` & `saic_ismart_client-1.2.3/tests/test_Message_v3_0.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.2.2/tests/test_abrp_api.py` & `saic_ismart_client-1.2.3/tests/test_abrp_api.py`

 * *Files identical despite different names*

