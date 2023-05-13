# Comparing `tmp/saic_ismart_client-1.1.7.tar.gz` & `tmp/saic_ismart_client-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "saic_ismart_client-1.1.7.tar", last modified: Tue May  2 17:21:11 2023, max compression
+gzip compressed data, was "saic_ismart_client-1.2.0.tar", last modified: Sat May 13 12:31:28 2023, max compression
```

## Comparing `saic_ismart_client-1.1.7.tar` & `saic_ismart_client-1.2.0.tar`

### file list

```diff
@@ -1,50 +1,50 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.439565 saic_ismart_client-1.1.7/
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      732 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-02 17:21:11.439565 saic_ismart_client-1.1.7/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.431565 saic_ismart_client-1.1.7/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.431565 saic_ismart_client-1.1.7/src/saic_ismart_client/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.431565 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     3230 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    20928 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/common_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v1_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v1_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v1_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v2_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v2_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17038 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v2_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v3_0/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v3_0/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15431 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v3_0/data_model.py
--rw-r--r--   0 runner    (1001) docker     (123)    23737 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/src/saic_ismart_client/saic_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/src/saic_ismart_client.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-02 17:21:11.000000 saic_ismart_client-1.1.7/src/saic_ismart_client.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1517 2023-05-02 17:21:11.000000 saic_ismart_client-1.1.7/src/saic_ismart_client.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-02 17:21:11.000000 saic_ismart_client-1.1.7/src/saic_ismart_client.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-02 17:21:11.000000 saic_ismart_client-1.1.7/src/saic_ismart_client.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-02 17:21:11.000000 saic_ismart_client-1.1.7/src/saic_ismart_client.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 17:21:11.435565 saic_ismart_client-1.1.7/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/tests/test_Message_v1_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/tests/test_Message_v2_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/tests/test_Message_v3_0.py
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/tests/test_abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    13061 2023-05-02 17:21:00.000000 saic_ismart_client-1.1.7/tests/test_ws_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.759611 saic_ismart_client-1.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      598 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      732 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:31:28.759611 saic_ismart_client-1.2.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.747610 saic_ismart_client-1.2.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.751610 saic_ismart_client-1.2.0/src/saic_ismart_client/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.747610 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.751610 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.751610 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     3230 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20928 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/common_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17038 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15431 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/data_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27857 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/src/saic_ismart_client/saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.751610 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1519 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 12:31:28.000000 saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:31:28.755611 saic_ismart_client-1.2.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_Message_v1_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_Message_v2_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_Message_v3_0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13108 2023-05-13 12:31:14.000000 saic_ismart_client-1.2.0/tests/test_saic_api.py
```

### Comparing `saic_ismart_client-1.1.7/LICENSE` & `saic_ismart_client-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/PKG-INFO` & `saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: saic_ismart_client
-Version: 1.1.7
+Name: saic-ismart-client
+Version: 1.2.0
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.1.7/README.md` & `saic_ismart_client-1.2.0/README.md`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/pyproject.toml` & `saic_ismart_client-1.2.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "saic_ismart_client"
-version = "1.1.7"
+version = "1.2.0"
 authors = [
     { name = "Thomas Salm", email="saic-python-client@devtom.de"},
 ]
 dependencies = [
     "asn1tools >= 0.165.0",
     "requests >= 2.28.2",
     "urllib3 >= 1.26.14",
```

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/abrp_api.py` & `saic_ismart_client-1.2.0/src/saic_ismart_client/abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/common_model.py` & `saic_ismart_client-1.2.0/src/saic_ismart_client/common_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v1_1/Message.py` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v1_1/data_model.py` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v1_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v2_1/Message.py` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v2_1/data_model.py` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v2_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v3_0/Message.py` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client/ota_v3_0/data_model.py` & `saic_ismart_client-1.2.0/src/saic_ismart_client/ota_v3_0/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client.egg-info/PKG-INFO` & `saic_ismart_client-1.2.0/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: saic-ismart-client
-Version: 1.1.7
+Name: saic_ismart_client
+Version: 1.2.0
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.1.7/src/saic_ismart_client.egg-info/SOURCES.txt` & `saic_ismart_client-1.2.0/src/saic_ismart_client.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -29,8 +29,8 @@
 src/saic_ismart_client/ota_v3_0/Message.py
 src/saic_ismart_client/ota_v3_0/__init__.py
 src/saic_ismart_client/ota_v3_0/data_model.py
 tests/test_Message_v1_1.py
 tests/test_Message_v2_1.py
 tests/test_Message_v3_0.py
 tests/test_abrp_api.py
-tests/test_ws_api.py
+tests/test_saic_api.py
```

### Comparing `saic_ismart_client-1.1.7/tests/test_Message_v1_1.py` & `saic_ismart_client-1.2.0/tests/test_Message_v1_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/tests/test_Message_v2_1.py` & `saic_ismart_client-1.2.0/tests/test_Message_v2_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/tests/test_Message_v3_0.py` & `saic_ismart_client-1.2.0/tests/test_Message_v3_0.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/tests/test_abrp_api.py` & `saic_ismart_client-1.2.0/tests/test_abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.1.7/tests/test_ws_api.py` & `saic_ismart_client-1.2.0/tests/test_saic_api.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,15 +11,15 @@
     MpAlarmSettingType
 from saic_ismart_client.ota_v2_1.Message import MessageCoderV21
 from saic_ismart_client.ota_v2_1.data_model import OtaRvmVehicleStatusResp25857, RvsPosition, RvsWayPoint,\
     RvsWgs84Point, Timestamp4Short, RvsBasicStatus25857
 from saic_ismart_client.ota_v3_0.Message import MessageBodyV30, MessageV30, MessageCoderV30
 from saic_ismart_client.ota_v3_0.data_model import OtaChrgMangDataResp, RvsChargingStatus
 
-from saic_ismart_client.saic_api import SaicApi
+from saic_ismart_client.saic_api import SaicApi, SaicApiException
 
 TOKEN = '99X9999X-90XX-99X9-99X9-9XX9XX0X9X9XXX9X'
 UID = '00000000000000000000000000000000000090000000099999'
 VIN = 'vin10000000000000'
 
 
 def mock_login_response_hex(message_coder: MessageCoderV11) -> str:
@@ -226,27 +226,27 @@
         mock_response(mocked_post, mock_alarm_switch_response_hex(self.message_coder_v1_1))
 
         try:
             alarm_switches = []
             for alarm_setting_type in MpAlarmSettingType:
                 alarm_switches.append(saic_ismart_client.saic_api.create_alarm_switch(alarm_setting_type))
             self.saic_api.set_alarm_switches(alarm_switches)
-        except Exception:
+        except SaicApiException:
             self.fail()
 
     @patch.object(requests, 'post')
     def test_get_vehicle_status(self, mocked_post):
         vin_info = create_vin_info(VIN)
         mock_response(mocked_post, mock_vehicle_status_response(self.message_coder_v2_1, UID, TOKEN, vin_info))
 
-        vehicle_status_rsp_msg = self.saic_api.get_vehicle_status(vin_info)
+        vehicle_status_rsp_msg = self.saic_api.get_vehicle_status_with_retry(vin_info)
         app_data = cast(OtaRvmVehicleStatusResp25857, vehicle_status_rsp_msg.application_data)
         self.assertEqual(1000000000, app_data.status_time)
 
     @patch.object(requests, 'post')
     def test_get_charging_status(self, mocked_post):
         vin_info = create_vin_info(VIN)
         mock_response(mocked_post, mock_chrg_mgmt_data_rsp(self.message_coder_v3_0, UID, TOKEN, vin_info))
 
-        chrg_mgmt_data_rsp_msg = self.saic_api.get_charging_status(vin_info)
+        chrg_mgmt_data_rsp_msg = self.saic_api.get_charging_status_with_retry(vin_info)
         app_data = cast(OtaChrgMangDataResp, chrg_mgmt_data_rsp_msg.application_data)
         self.assertEqual(1023, app_data.bmsChrgOtptCrntReq)
```

