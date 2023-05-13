# Comparing `tmp/neuko-device-sdk-1.1.1.tar.gz` & `tmp/neuko-device-sdk-1.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "neuko-device-sdk-1.1.1.tar", last modified: Sat May  6 07:07:33 2023, max compression
+gzip compressed data, was "neuko-device-sdk-1.1.2.tar", last modified: Sat May 13 05:22:23 2023, max compression
```

## Comparing `neuko-device-sdk-1.1.1.tar` & `neuko-device-sdk-1.1.2.tar`

### file list

```diff
@@ -1,56 +1,56 @@
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.556115 neuko-device-sdk-1.1.1/
--rw-r--r--   0 popoimaevi   (501) staff       (20)     1073 2022-02-09 06:51:49.000000 neuko-device-sdk-1.1.1/LICENSE
--rw-r--r--   0 popoimaevi   (501) staff       (20)     7748 2023-05-06 07:07:33.556349 neuko-device-sdk-1.1.1/PKG-INFO
--rw-r--r--   0 popoimaevi   (501) staff       (20)     6981 2023-05-06 07:07:27.000000 neuko-device-sdk-1.1.1/README.md
--rw-r--r--   0 popoimaevi   (501) staff       (20)       76 2023-05-06 07:07:33.557195 neuko-device-sdk-1.1.1/setup.cfg
--rw-r--r--   0 popoimaevi   (501) staff       (20)     1448 2023-05-06 07:07:27.000000 neuko-device-sdk-1.1.1/setup.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     1448 2023-05-06 07:04:14.000000 neuko-device-sdk-1.1.1/setupdev.py
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.531387 neuko-device-sdk-1.1.1/src/
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.533472 neuko-device-sdk-1.1.1/src/neuko/
--rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/__init__.py
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.536261 neuko-device-sdk-1.1.1/src/neuko/connection/
--rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/connection/__init__.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     2435 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/connection/certificateManagement.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     3369 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/src/neuko/connection/certificateStore.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     6192 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/src/neuko/connection/connectionManagement.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     2833 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/connection/connectionStore.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     1821 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/connection/model.py
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.540417 neuko-device-sdk-1.1.1/src/neuko/device/
--rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/device/__init__.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)    40025 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/src/neuko/device/device.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     2137 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/device/deviceManagement.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     5770 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/src/neuko/device/identifierStore.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     2005 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/device/model.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)    13093 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/src/neuko/device/telemetricState.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     7393 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/src/neuko/device/telemetricWorker.py
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.543380 neuko-device-sdk-1.1.1/src/neuko/iot/
--rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/iot/__init__.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     5041 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/iot/bootstrap.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)    14338 2022-04-27 03:44:53.000000 neuko-device-sdk-1.1.1/src/neuko/iot/iot.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)      745 2022-04-26 04:06:04.000000 neuko-device-sdk-1.1.1/src/neuko/iot/model.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)    18373 2023-05-06 07:04:14.000000 neuko-device-sdk-1.1.1/src/neuko/iot/neuko.py
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.544371 neuko-device-sdk-1.1.1/src/neuko/lifecycle/
--rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/lifecycle/__init__.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     4768 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/src/neuko/lifecycle/connectionStateMachine.py
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.546166 neuko-device-sdk-1.1.1/src/neuko/utility/
--rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/utility/__init__.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)      539 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/utility/logger.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)      111 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/src/neuko/utility/utils.py
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.549049 neuko-device-sdk-1.1.1/src/neuko_device_sdk.egg-info/
--rw-r--r--   0 popoimaevi   (501) staff       (20)     7748 2023-05-06 07:07:33.000000 neuko-device-sdk-1.1.1/src/neuko_device_sdk.egg-info/PKG-INFO
--rw-r--r--   0 popoimaevi   (501) staff       (20)     1377 2023-05-06 07:07:33.000000 neuko-device-sdk-1.1.1/src/neuko_device_sdk.egg-info/SOURCES.txt
--rw-r--r--   0 popoimaevi   (501) staff       (20)        1 2023-05-06 07:07:33.000000 neuko-device-sdk-1.1.1/src/neuko_device_sdk.egg-info/dependency_links.txt
--rw-r--r--   0 popoimaevi   (501) staff       (20)       67 2023-05-06 07:07:33.000000 neuko-device-sdk-1.1.1/src/neuko_device_sdk.egg-info/requires.txt
--rw-r--r--   0 popoimaevi   (501) staff       (20)        6 2023-05-06 07:07:33.000000 neuko-device-sdk-1.1.1/src/neuko_device_sdk.egg-info/top_level.txt
-drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-06 07:07:33.555576 neuko-device-sdk-1.1.1/tests/
--rw-r--r--   0 popoimaevi   (501) staff       (20)     5278 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/tests/test_01_identifierStore.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     4138 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/tests/test_02_deviceManagement.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     2206 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/tests/test_03_certificateStore.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     4898 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/tests/test_04_certificateManagement.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)      706 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/tests/test_05_connectionStore.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     6831 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/tests/test_06_connectionManagement.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)     4021 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.1/tests/test_07_worker.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)    13693 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/tests/test_08_telemetricState.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)    12636 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.1/tests/test_09_bootstrap.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)    14716 2023-05-06 07:04:14.000000 neuko-device-sdk-1.1.1/tests/test_10_neuko.py
--rw-r--r--   0 popoimaevi   (501) staff       (20)    17860 2023-05-06 07:04:14.000000 neuko-device-sdk-1.1.1/tests/test_11_device.py
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.954471 neuko-device-sdk-1.1.2/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     1073 2022-02-09 06:51:49.000000 neuko-device-sdk-1.1.2/LICENSE
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     7748 2023-05-13 05:22:23.954692 neuko-device-sdk-1.1.2/PKG-INFO
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     6981 2023-05-13 05:22:17.000000 neuko-device-sdk-1.1.2/README.md
+-rw-r--r--   0 popoimaevi   (501) staff       (20)       76 2023-05-13 05:22:23.955719 neuko-device-sdk-1.1.2/setup.cfg
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     1448 2023-05-13 05:22:17.000000 neuko-device-sdk-1.1.2/setup.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     1448 2023-05-13 05:21:06.000000 neuko-device-sdk-1.1.2/setupdev.py
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.919294 neuko-device-sdk-1.1.2/src/
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.923102 neuko-device-sdk-1.1.2/src/neuko/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/__init__.py
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.931728 neuko-device-sdk-1.1.2/src/neuko/connection/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/connection/__init__.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     2435 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/connection/certificateManagement.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     3369 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/src/neuko/connection/certificateStore.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     6192 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/src/neuko/connection/connectionManagement.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     2833 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/connection/connectionStore.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     1821 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/connection/model.py
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.936536 neuko-device-sdk-1.1.2/src/neuko/device/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/device/__init__.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)    41313 2023-05-13 04:27:48.000000 neuko-device-sdk-1.1.2/src/neuko/device/device.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     2137 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/device/deviceManagement.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     5770 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/src/neuko/device/identifierStore.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     2005 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/device/model.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)    14288 2023-05-13 04:27:04.000000 neuko-device-sdk-1.1.2/src/neuko/device/telemetricState.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     7393 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/src/neuko/device/telemetricWorker.py
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.940193 neuko-device-sdk-1.1.2/src/neuko/iot/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/iot/__init__.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     5041 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/iot/bootstrap.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)    14338 2022-04-27 03:44:53.000000 neuko-device-sdk-1.1.2/src/neuko/iot/iot.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)      745 2022-04-26 04:06:04.000000 neuko-device-sdk-1.1.2/src/neuko/iot/model.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)    18373 2023-05-06 07:09:11.000000 neuko-device-sdk-1.1.2/src/neuko/iot/neuko.py
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.941555 neuko-device-sdk-1.1.2/src/neuko/lifecycle/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/lifecycle/__init__.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     4768 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/src/neuko/lifecycle/connectionStateMachine.py
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.943779 neuko-device-sdk-1.1.2/src/neuko/utility/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)        0 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/utility/__init__.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)      539 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/utility/logger.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)      111 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/src/neuko/utility/utils.py
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.947366 neuko-device-sdk-1.1.2/src/neuko_device_sdk.egg-info/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     7748 2023-05-13 05:22:23.000000 neuko-device-sdk-1.1.2/src/neuko_device_sdk.egg-info/PKG-INFO
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     1377 2023-05-13 05:22:23.000000 neuko-device-sdk-1.1.2/src/neuko_device_sdk.egg-info/SOURCES.txt
+-rw-r--r--   0 popoimaevi   (501) staff       (20)        1 2023-05-13 05:22:23.000000 neuko-device-sdk-1.1.2/src/neuko_device_sdk.egg-info/dependency_links.txt
+-rw-r--r--   0 popoimaevi   (501) staff       (20)       67 2023-05-13 05:22:23.000000 neuko-device-sdk-1.1.2/src/neuko_device_sdk.egg-info/requires.txt
+-rw-r--r--   0 popoimaevi   (501) staff       (20)        6 2023-05-13 05:22:23.000000 neuko-device-sdk-1.1.2/src/neuko_device_sdk.egg-info/top_level.txt
+drwxr-xr-x   0 popoimaevi   (501) staff       (20)        0 2023-05-13 05:22:23.953831 neuko-device-sdk-1.1.2/tests/
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     5278 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/tests/test_01_identifierStore.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     4138 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/tests/test_02_deviceManagement.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     2206 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/tests/test_03_certificateStore.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     4898 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/tests/test_04_certificateManagement.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)      706 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/tests/test_05_connectionStore.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     6831 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/tests/test_06_connectionManagement.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)     4021 2022-03-14 04:06:47.000000 neuko-device-sdk-1.1.2/tests/test_07_worker.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)    13693 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/tests/test_08_telemetricState.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)    12636 2022-11-28 09:17:03.000000 neuko-device-sdk-1.1.2/tests/test_09_bootstrap.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)    14716 2023-05-06 07:09:11.000000 neuko-device-sdk-1.1.2/tests/test_10_neuko.py
+-rw-r--r--   0 popoimaevi   (501) staff       (20)    19610 2023-05-13 05:10:00.000000 neuko-device-sdk-1.1.2/tests/test_11_device.py
```

### Comparing `neuko-device-sdk-1.1.1/LICENSE` & `neuko-device-sdk-1.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/PKG-INFO` & `neuko-device-sdk-1.1.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: neuko-device-sdk
-Version: 1.1.1
+Version: 1.1.2
 Summary: Neuko device SDK for Python hardware
 Author: neuko.io
 Author-email: hello@neuko.io
 License: MIT
 Keywords: iot,device,thing,cloud,mqtt,development,neuko
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
```

### Comparing `neuko-device-sdk-1.1.1/README.md` & `neuko-device-sdk-1.1.2/README.md`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/setup.py` & `neuko-device-sdk-1.1.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     long_description = long_description.replace("\r","")
 except(IOError, ImportError):
     long_description = open('README.md').read()
 
 
 setup(
     name='neuko-device-sdk',
-    version='1.1.1',
+    version='1.1.2',
     license='MIT',
     description="Neuko device SDK for Python hardware",
     long_description= long_description,
     long_description_content_type="text/markdown",
     author="neuko.io",
     author_email='hello@neuko.io',
     packages=find_packages('src'),
```

### Comparing `neuko-device-sdk-1.1.1/setupdev.py` & `neuko-device-sdk-1.1.2/setupdev.py`

 * *Files 4% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     long_description = long_description.replace("\r","")
 except(IOError, ImportError):
     long_description = open('README.md').read()
 
 
 setup(
     name='neuko-device-sdk',
-    version='1.1.1',
+    version='1.1.2',
     license='MIT',
     description="Neuko device SDK for Python hardware",
     long_description= long_description,
     long_description_content_type="text/markdown",
     author="neuko.io",
     author_email='hello@neuko.io',
     packages=find_packages('src'),
```

### Comparing `neuko-device-sdk-1.1.1/src/neuko/connection/certificateManagement.py` & `neuko-device-sdk-1.1.2/src/neuko/connection/certificateManagement.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/connection/certificateStore.py` & `neuko-device-sdk-1.1.2/src/neuko/connection/certificateStore.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/connection/connectionManagement.py` & `neuko-device-sdk-1.1.2/src/neuko/connection/connectionManagement.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/connection/connectionStore.py` & `neuko-device-sdk-1.1.2/src/neuko/connection/connectionStore.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/connection/model.py` & `neuko-device-sdk-1.1.2/src/neuko/connection/model.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/device/device.py` & `neuko-device-sdk-1.1.2/src/neuko/device/device.py`

 * *Files 2% similar despite different names*

```diff
@@ -677,33 +677,50 @@
         try:
             self.useEffect(context, listener, f'DEVICE_LIFECYCLE_{str(deviceLifecycle)}', "*")
             logger.debug(f'listenLifecycleState: Added worker for lifecycle {str(deviceLifecycle)}')
         except Exception as ex:
             logger.error(ex)
             raise Exception(ex)
 
-    def updateTelemetricState(self, stateName: str, value: object) -> None:
+    async def updateTelemetricState(self, stateName: str, value: object, updateVirtualTwin: bool = False) -> None:
         """
-        It takes a state name and a value, and flattens the value, and then reports the flattened value
-        to the telemetric state
+        This function updates the telemetric state of a device and optionally updates the virtual twin
+        and stores the data in timestream storage.
         
-        :param stateName: The name of the state to report
+        :param stateName: The name of the telemetric state being updated
         :type stateName: str
-        :param value: object
+        :param value: The value parameter is an object that represents the telemetry data to be updated.
+        It can be of any data type, and will be flattened into a dictionary of key-value pairs before
+        being reported
         :type value: object
-        :param overwriteTimestamp: The timestamp of the data. We discourage to use this argument except the data is an history data and you really know what you are doing
-        :type stateName: int
+        :param updateVirtualTwin: The `updateVirtualTwin` parameter is a boolean flag that indicates
+        whether or not to update the device's virtual twin with the new telemetric state. If set to
+        `True`, the function will update the virtual twin with the latest telemetric state. If set to
+        `False`, the, defaults to False
+        :type updateVirtualTwin: bool (optional)
         """
         try:
             flatValue = TelemetricState.flattening(value)
             for attributeTree in flatValue:
                 logger.debug(f'updateTelemetricState: attributeTree: {attributeTree}')
                 logger.debug(f'updateTelemetricState: attributeTree value: {flatValue[attributeTree]}')
                 self._localTelemetricState.report(stateName, attributeTree, flatValue[attributeTree], int(time.time()))
+                self._localTelemetricState.desire(stateName, attributeTree, flatValue[attributeTree], int(time.time()))
                 logger.debug(f'updateTelemetricState: Reported state {stateName}/{attributeTree}')
+
+            if updateVirtualTwin:
+                logger.debug(f'updateTelemetricState: Force update Virtual Twin')
+                self._localTelemetricState.updateNewTime()
+                await self._deviceClient.pushTelemetricState(stateName, self._localTelemetricState.snapshot(stateName, False, True))
+
+                # timestream storage if any
+                if stateName in self._features['timestreamStorage']['value'] or '*' in self._features['timestreamStorage']['value']:
+                    logger.debug(f'_tick: Timestream storage enabled for {stateName}')
+                    await self._deviceClient.timestreamStorage(stateName, self._localTelemetricState.snapshot(stateName, True))
+
         except Exception as ex:
             logger.error(ex)
             raise Exception(ex)
 
     def getLocalTelemetricStateValue(self, stateName: str, stateType: TelemetricStateType = TelemetricStateType.Reported, attributeTree: str = "*"):
         try:
             return self._localTelemetricState.value(stateName, stateType, attributeTree)
```

### Comparing `neuko-device-sdk-1.1.1/src/neuko/device/deviceManagement.py` & `neuko-device-sdk-1.1.2/src/neuko/device/deviceManagement.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/device/identifierStore.py` & `neuko-device-sdk-1.1.2/src/neuko/device/identifierStore.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/device/model.py` & `neuko-device-sdk-1.1.2/src/neuko/device/model.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/device/telemetricState.py` & `neuko-device-sdk-1.1.2/src/neuko/device/telemetricState.py`

 * *Files 9% similar despite different names*

```diff
@@ -218,32 +218,51 @@
         for key in flat:
             logger.debug(f'getPendingDesire: Pending {key}')
             return {
                 'attributeTree': key,
                 'value': get(self.states[TelemetricStateType.Desired][stateName], key)
             }
 
-    def snapshot(self, stateName: str, attributesOnly: bool = False) -> object:
+    def snapshot(self, stateName: str, attributesOnly: bool = False, withDesire: bool = False) -> object:
         """
-        This function returns the latest value for a given state
+        This function returns a snapshot of the current state of an object, including reported and
+        desired attributes if specified.
         
-        :param stateName: The name of the state to be retrieved
+        :param stateName: The name of the state for which a snapshot is being taken
         :type stateName: str
-        :param attributesOnly: If true, only the attributes of the state are returned, defaults to False
+        :param attributesOnly: A boolean parameter that determines whether to return the entire state or
+        just the attributes of the state, defaults to False
         :type attributesOnly: bool (optional)
-        :return: The latest value for the state.
+        :param withDesire: `withDesire` is a boolean parameter that determines whether the returned
+        object should include the desired state in addition to the reported state. If `withDesire` is
+        `True`, the returned object will have a `state` key with both `reported` and `desired` keys. If
+        `, defaults to False
+        :type withDesire: bool (optional)
+        :return: an object that contains a snapshot of the current state of the device. The contents of
+        the object depend on the values of the parameters passed to the function. If `attributesOnly` is
+        `False`, the object will contain the reported state of the device, and if `withDesire` is
+        `True`, it will also contain the desired state. If `attributesOnly` is `
         """
         latest = get(self.states[TelemetricStateType.Reported], stateName)
         logger.debug(f'snapshot: Value for {stateName} = {json.dumps(latest)}')
         if attributesOnly == False:
-            return {
-                'state': {
-                    'reported': latest
+
+            if withDesire:
+                return {
+                    'state': {
+                        'reported': latest,
+                        'desired': get(self.states[TelemetricStateType.Desired], stateName)
+                    }
+                }
+            else:
+                return {
+                    'state': {
+                        'reported': latest
+                    }
                 }
-            }
         else:
             return latest
 
     def getLastTime(self):
         """
         Return the last time the push button was pressed
         :return: The last time the button was pushed.
```

### Comparing `neuko-device-sdk-1.1.1/src/neuko/device/telemetricWorker.py` & `neuko-device-sdk-1.1.2/src/neuko/device/telemetricWorker.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/iot/bootstrap.py` & `neuko-device-sdk-1.1.2/src/neuko/iot/bootstrap.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/iot/iot.py` & `neuko-device-sdk-1.1.2/src/neuko/iot/iot.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/iot/model.py` & `neuko-device-sdk-1.1.2/src/neuko/iot/model.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/iot/neuko.py` & `neuko-device-sdk-1.1.2/src/neuko/iot/neuko.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/lifecycle/connectionStateMachine.py` & `neuko-device-sdk-1.1.2/src/neuko/lifecycle/connectionStateMachine.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko/utility/logger.py` & `neuko-device-sdk-1.1.2/src/neuko/utility/logger.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/src/neuko_device_sdk.egg-info/PKG-INFO` & `neuko-device-sdk-1.1.2/src/neuko_device_sdk.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: neuko-device-sdk
-Version: 1.1.1
+Version: 1.1.2
 Summary: Neuko device SDK for Python hardware
 Author: neuko.io
 Author-email: hello@neuko.io
 License: MIT
 Keywords: iot,device,thing,cloud,mqtt,development,neuko
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
```

### Comparing `neuko-device-sdk-1.1.1/src/neuko_device_sdk.egg-info/SOURCES.txt` & `neuko-device-sdk-1.1.2/src/neuko_device_sdk.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_01_identifierStore.py` & `neuko-device-sdk-1.1.2/tests/test_01_identifierStore.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_02_deviceManagement.py` & `neuko-device-sdk-1.1.2/tests/test_02_deviceManagement.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_03_certificateStore.py` & `neuko-device-sdk-1.1.2/tests/test_03_certificateStore.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_04_certificateManagement.py` & `neuko-device-sdk-1.1.2/tests/test_04_certificateManagement.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_05_connectionStore.py` & `neuko-device-sdk-1.1.2/tests/test_05_connectionStore.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_06_connectionManagement.py` & `neuko-device-sdk-1.1.2/tests/test_06_connectionManagement.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_07_worker.py` & `neuko-device-sdk-1.1.2/tests/test_07_worker.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_08_telemetricState.py` & `neuko-device-sdk-1.1.2/tests/test_08_telemetricState.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_09_bootstrap.py` & `neuko-device-sdk-1.1.2/tests/test_09_bootstrap.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_10_neuko.py` & `neuko-device-sdk-1.1.2/tests/test_10_neuko.py`

 * *Files identical despite different names*

### Comparing `neuko-device-sdk-1.1.1/tests/test_11_device.py` & `neuko-device-sdk-1.1.2/tests/test_11_device.py`

 * *Files 3% similar despite different names*

```diff
@@ -208,15 +208,69 @@
                 ))
                 
             self.asyncloop.run_until_complete(asyncio.sleep(1))
 
         self.asyncloop.run_until_complete(device.stop())
         self.assertTrue(True)
 
-    def test_05_sync_useEffect_state_of_array(self):
+    def test_05_listen_to_device_lifecycle(self):
+
+        self.INTERNET_CONNECTED: bool = False
+        self.PERPETUAL_CONNECTED: bool = False
+        self.TELEMETRIC_STATE_INITED: bool = False
+        self.TELEMETRIC_STATE_SYNCED: bool = False
+        self.GOODBYE: bool = False
+        
+        def callback(data: TelemetricStateChangeParameter):
+            logger.info(f'masuk callback: {data.stateName}::{data.context}')
+            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.INTERNET_CONNECTED}': 
+                data.context.INTERNET_CONNECTED = True
+
+            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.PERPETUAL_CONNECTED}': 
+                data.context.PERPETUAL_CONNECTED = True
+
+            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.TELEMETRIC_STATE_INITED}': 
+                data.context.TELEMETRIC_STATE_INITED = True
+
+            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.TELEMETRIC_STATE_SYNCED}': 
+                data.context.TELEMETRIC_STATE_SYNCED = True
+
+            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.GOODBYE}': 
+                data.context.GOODBYE = True
+
+            return True
+
+        device = Device(deviceIdentifierStore=DeviceIdentifierStoreTestObject(), certificateStore=CertificateStoreTestObject(), connectionStore=ConnectionStoreTest())
+        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.INTERNET_CONNECTED)
+        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.PERPETUAL_CONNECTED)
+        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.TELEMETRIC_STATE_INITED)
+        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.TELEMETRIC_STATE_SYNCED)
+        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.GOODBYE)
+        device.start_threadsafe()
+        waitTime = 0
+        timeoutTime = 20
+        value = uuid.uuid4().hex
+        while waitTime < timeoutTime:
+            waitTime += 1
+            self.asyncloop.run_until_complete(asyncio.sleep(1))
+
+        self.asyncloop.run_until_complete(device.stop())
+
+        with self.subTest():
+            self.assertEqual(self.INTERNET_CONNECTED, True)
+        with self.subTest():
+            self.assertEqual(self.PERPETUAL_CONNECTED, True)
+        with self.subTest():
+            self.assertEqual(self.TELEMETRIC_STATE_INITED, True)
+        with self.subTest():
+            self.assertEqual(self.TELEMETRIC_STATE_SYNCED, True)
+        with self.subTest():
+            self.assertEqual(self.GOODBYE, True)
+    
+    def test_06_sync_useEffect_state_of_array(self):
         
         def callback(data: TelemetricStateChangeParameter):
             logger.info(f'masuk callback: {data.value}')
             return True
 
         device = Device(deviceIdentifierStore=DeviceIdentifierStoreTestObject(), certificateStore=CertificateStoreTestObject(), connectionStore=ConnectionStoreTest())
         device.useEffect(self, callback, 'state_c', 'att.upward')
@@ -257,15 +311,15 @@
                 ))
                 
             self.asyncloop.run_until_complete(asyncio.sleep(1))
 
         self.asyncloop.run_until_complete(device.stop())
         self.assertTrue(True)
 
-    def test_06_get_current_reported_value(self):
+    def test_07_get_current_reported_value(self):
         
         def callback(data: TelemetricStateChangeParameter):
             logger.info(f'masuk callback: {data}')
             return True
 
         device = Device(deviceIdentifierStore=DeviceIdentifierStoreTestObject(), certificateStore=CertificateStoreTestObject(), connectionStore=ConnectionStoreTest())
         device.useEffect(self, callback, 'state_a', 'att.deep')
@@ -297,51 +351,14 @@
         self.assertEqual(stateValue, {
             "att": {
                 "deep": value,
                 "deep2": False
             }
         })
 
-    def test_07_get_internal_configuration(self):
-        
-        def callback(data: TelemetricStateChangeParameter):
-            logger.info(f'masuk callback: {data}')
-            return True
-
-        device = Device(deviceIdentifierStore=DeviceIdentifierStoreTestObject(), certificateStore=CertificateStoreTestObject(), connectionStore=ConnectionStoreTest())
-        device.useEffect(self, callback, 'internal_configuration')
-        device.start_threadsafe()
-        waitTime = 0
-        timeoutTime = 15
-        value = uuid.uuid4().hex
-        while waitTime < timeoutTime:
-            logger.debug(f'Test end in {timeoutTime - waitTime}')
-            waitTime += 1
-            self.asyncloop.run_until_complete(asyncio.sleep(1))
-
-        stateValue = device.getLocalTelemetricStateValue("internal_configuration", TelemetricStateType.Reported)
-        self.asyncloop.run_until_complete(device.stop())
-        logger.debug(stateValue)
-        with self.subTest():
-            self.assertEqual(stateValue["features"]["interval"]["version"], 1)
-        with self.subTest():
-            self.assertEqual(stateValue["features"]["interval"]["value"], 60000)
-        with self.subTest():
-            self.assertEqual(stateValue["features"]["timestreamStorage"]["version"], 1)
-        with self.subTest():
-            self.assertEqual(stateValue["features"]["timestreamStorage"]["value"], ["*"])
-        with self.subTest():
-            self.assertEqual(stateValue["features"]["backupStorage"]["version"], 1)
-        with self.subTest():
-            self.assertEqual(stateValue["features"]["backupStorage"]["value"], [])
-        with self.subTest():
-            self.assertEqual(stateValue["features"]["relay"]["version"], 1)
-        with self.subTest():
-            self.assertEqual(stateValue["features"]["relay"]["value"], [])
-
     def test_08_report_value(self):
         
         def callback(data: TelemetricStateChangeParameter):
             logger.info(f'masuk callback: {data}')
             return True
 
         device = Device(deviceIdentifierStore=DeviceIdentifierStoreTestObject(), certificateStore=CertificateStoreTestObject(), connectionStore=ConnectionStoreTest())
@@ -365,74 +382,103 @@
             #                 }
             #             }
             #         })
             #     ))
                 
             self.asyncloop.run_until_complete(asyncio.sleep(1))
         self.asyncloop.run_until_complete(asyncio.sleep(1))
-        device.updateTelemetricState("state_a", {
+        self.asyncloop.run_until_complete(device.updateTelemetricState("state_a", {
             "att": {
                 "deep": value
             }
-        })
+        }, False))
         stateValue = device.getLocalTelemetricStateValue("state_a", TelemetricStateType.Reported)
         self.asyncloop.run_until_complete(device.stop())
         self.assertEqual(stateValue, {
             "att": {
                 "deep": value,
                 "deep2": False
             }
         })
 
-    def test_09_listen_to_device_lifecycle(self):
-
-        self.INTERNET_CONNECTED: bool = False
-        self.PERPETUAL_CONNECTED: bool = False
-        self.TELEMETRIC_STATE_INITED: bool = False
-        self.TELEMETRIC_STATE_SYNCED: bool = False
-        self.GOODBYE: bool = False
+    def test_09_force_update_virtual_twin(self):
         
         def callback(data: TelemetricStateChangeParameter):
-            logger.info(f'masuk callback: {data.stateName}::{data.context}')
-            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.INTERNET_CONNECTED}': 
-                data.context.INTERNET_CONNECTED = True
+            logger.info(f'masuk callback: {data}')
+            return True
 
-            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.PERPETUAL_CONNECTED}': 
-                data.context.PERPETUAL_CONNECTED = True
+        device = Device(deviceIdentifierStore=DeviceIdentifierStoreTestObject(), certificateStore=CertificateStoreTestObject(), connectionStore=ConnectionStoreTest())
+        device.useEffect(self, callback, 'state_a', 'att.deep')
+        device.start_threadsafe()
+        waitTime = 0
+        timeoutTime = 30
+        value = random.random()
 
-            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.TELEMETRIC_STATE_INITED}': 
-                data.context.TELEMETRIC_STATE_INITED = True
+        while waitTime < timeoutTime:
+            logger.debug(f'Test end in {timeoutTime - waitTime}')
+            waitTime += 1  
+            self.asyncloop.run_until_complete(asyncio.sleep(1))
 
-            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.TELEMETRIC_STATE_SYNCED}': 
-                data.context.TELEMETRIC_STATE_SYNCED = True
+        self.asyncloop.run_until_complete(asyncio.sleep(1))
+        self.asyncloop.run_until_complete(device.updateTelemetricState("state_a", {
+            "att": {
+                "deep": value
+            }
+        }, True))
 
-            if data.stateName == f'DEVICE_LIFECYCLE_{ConnectionStateNachineLifecycle.GOODBYE}': 
-                data.context.GOODBYE = True
+        # # lets wait for 2 seconds
+        # waitTime = 0
+        # while waitTime < 2:
+        #     logger.debug(f'Wait end in {timeoutTime - waitTime}')
+        #     waitTime += 1   
+        #     self.asyncloop.run_until_complete(asyncio.sleep(1))
 
+        # let pull the data
+        # self.asyncloop.run_until_complete(device._deviceClient.pullTelemetricState('state_a'))
+        stateValue = device.getLocalTelemetricStateValue("state_a", TelemetricStateType.Reported)
+        self.asyncloop.run_until_complete(device.stop())
+        logger.debug(f'Random value = {value}')
+        self.assertEqual(stateValue, {
+            "att": {
+                "deep": value,
+                "deep2": False
+            }
+        })
+    
+    def test_10_get_internal_configuration(self):
+        
+        def callback(data: TelemetricStateChangeParameter):
+            logger.info(f'masuk callback: {data}')
             return True
 
         device = Device(deviceIdentifierStore=DeviceIdentifierStoreTestObject(), certificateStore=CertificateStoreTestObject(), connectionStore=ConnectionStoreTest())
-        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.INTERNET_CONNECTED)
-        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.PERPETUAL_CONNECTED)
-        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.TELEMETRIC_STATE_INITED)
-        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.TELEMETRIC_STATE_SYNCED)
-        device.listenLifecycleState(self, callback, ConnectionStateNachineLifecycle.GOODBYE)
+        device.useEffect(self, callback, 'internal_configuration')
         device.start_threadsafe()
         waitTime = 0
-        timeoutTime = 20
+        timeoutTime = 15
         value = uuid.uuid4().hex
         while waitTime < timeoutTime:
+            logger.debug(f'Test end in {timeoutTime - waitTime}')
             waitTime += 1
             self.asyncloop.run_until_complete(asyncio.sleep(1))
 
+        stateValue = device.getLocalTelemetricStateValue("internal_configuration", TelemetricStateType.Reported)
         self.asyncloop.run_until_complete(device.stop())
-
+        logger.debug(stateValue)
         with self.subTest():
-            self.assertEqual(self.INTERNET_CONNECTED, True)
+            self.assertEqual(stateValue["features"]["interval"]["version"], 1)
         with self.subTest():
-            self.assertEqual(self.PERPETUAL_CONNECTED, True)
+            self.assertEqual(stateValue["features"]["interval"]["value"], 60000)
         with self.subTest():
-            self.assertEqual(self.TELEMETRIC_STATE_INITED, True)
+            self.assertEqual(stateValue["features"]["timestreamStorage"]["version"], 1)
         with self.subTest():
-            self.assertEqual(self.TELEMETRIC_STATE_SYNCED, True)
+            self.assertEqual(stateValue["features"]["timestreamStorage"]["value"], ["*"])
+        with self.subTest():
+            self.assertEqual(stateValue["features"]["backupStorage"]["version"], 1)
+        with self.subTest():
+            self.assertEqual(stateValue["features"]["backupStorage"]["value"], [])
         with self.subTest():
-            self.assertEqual(self.GOODBYE, True)
+            self.assertEqual(stateValue["features"]["relay"]["version"], 1)
+        with self.subTest():
+            self.assertEqual(stateValue["features"]["relay"]["value"], [])
+
+
```

