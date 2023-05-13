# Comparing `tmp/sessypy-0.0.7.tar.gz` & `tmp/sessypy-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sessypy-0.0.7.tar", last modified: Thu Apr  6 18:33:13 2023, max compression
+gzip compressed data, was "sessypy-0.0.8.tar", last modified: Sat May 13 19:08:21 2023, max compression
```

## Comparing `sessypy-0.0.7.tar` & `sessypy-0.0.8.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 18:33:13.028389 sessypy-0.0.7/
--rw-r--r--   0 runner    (1001) docker     (123)    35148 2023-04-06 18:33:01.000000 sessypy-0.0.7/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      782 2023-04-06 18:33:13.028389 sessypy-0.0.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      486 2023-04-06 18:33:01.000000 sessypy-0.0.7/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-04-06 18:33:01.000000 sessypy-0.0.7/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      355 2023-04-06 18:33:13.028389 sessypy-0.0.7/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 18:33:13.020389 sessypy-0.0.7/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 18:33:13.024389 sessypy-0.0.7/src/sessypy/
--rw-r--r--   0 runner    (1001) docker     (123)       27 2023-04-06 18:33:01.000000 sessypy-0.0.7/src/sessypy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1518 2023-04-06 18:33:01.000000 sessypy-0.0.7/src/sessypy/api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2059 2023-04-06 18:33:01.000000 sessypy-0.0.7/src/sessypy/const.py
--rw-r--r--   0 runner    (1001) docker     (123)     2763 2023-04-06 18:33:01.000000 sessypy-0.0.7/src/sessypy/devices.py
--rw-r--r--   0 runner    (1001) docker     (123)      155 2023-04-06 18:33:01.000000 sessypy-0.0.7/src/sessypy/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 18:33:13.028389 sessypy-0.0.7/src/sessypy.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      782 2023-04-06 18:33:13.000000 sessypy-0.0.7/src/sessypy.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      323 2023-04-06 18:33:13.000000 sessypy-0.0.7/src/sessypy.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-06 18:33:13.000000 sessypy-0.0.7/src/sessypy.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-04-06 18:33:13.000000 sessypy-0.0.7/src/sessypy.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-04-06 18:33:13.000000 sessypy-0.0.7/src/sessypy.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:08:21.697957 sessypy-0.0.8/
+-rw-r--r--   0 runner    (1001) docker     (123)    35148 2023-05-13 19:08:05.000000 sessypy-0.0.8/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      782 2023-05-13 19:08:21.697957 sessypy-0.0.8/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      486 2023-05-13 19:08:05.000000 sessypy-0.0.8/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      298 2023-05-13 19:08:05.000000 sessypy-0.0.8/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      355 2023-05-13 19:08:21.697957 sessypy-0.0.8/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:08:21.693957 sessypy-0.0.8/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:08:21.693957 sessypy-0.0.8/src/sessypy/
+-rw-r--r--   0 runner    (1001) docker     (123)       27 2023-05-13 19:08:05.000000 sessypy-0.0.8/src/sessypy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1518 2023-05-13 19:08:05.000000 sessypy-0.0.8/src/sessypy/api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2179 2023-05-13 19:08:05.000000 sessypy-0.0.8/src/sessypy/const.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3194 2023-05-13 19:08:05.000000 sessypy-0.0.8/src/sessypy/devices.py
+-rw-r--r--   0 runner    (1001) docker     (123)      155 2023-05-13 19:08:05.000000 sessypy-0.0.8/src/sessypy/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:08:21.697957 sessypy-0.0.8/src/sessypy.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      782 2023-05-13 19:08:21.000000 sessypy-0.0.8/src/sessypy.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      323 2023-05-13 19:08:21.000000 sessypy-0.0.8/src/sessypy.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 19:08:21.000000 sessypy-0.0.8/src/sessypy.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 19:08:21.000000 sessypy-0.0.8/src/sessypy.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 19:08:21.000000 sessypy-0.0.8/src/sessypy.egg-info/top_level.txt
```

### Comparing `sessypy-0.0.7/LICENSE` & `sessypy-0.0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `sessypy-0.0.7/PKG-INFO` & `sessypy-0.0.8/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sessypy
-Version: 0.0.7
+Version: 0.0.8
 Summary: Python wrapper for Sessy REST API
 Home-page: https://github.com/PimDoos/sessypy
 Author: PimDoos
 License: GNU GPLv3
 Project-URL: Homepage, https://github.com/PimDoos/sessypy
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `sessypy-0.0.7/src/sessypy/api.py` & `sessypy-0.0.8/src/sessypy/api.py`

 * *Files identical despite different names*

### Comparing `sessypy-0.0.7/src/sessypy/const.py` & `sessypy-0.0.8/src/sessypy/const.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,17 +7,21 @@
     OTA_CHECK = f"{API_VERSION_1}/ota/check"
     OTA_START = f"{API_VERSION_1}/ota/start"
     OTA_STATUS = f"{API_VERSION_1}/ota/status"
     
     POWER_SETPOINT = f"{API_VERSION_1}/power/setpoint"
     POWER_STATUS = f"{API_VERSION_1}/power/status"
     POWER_STRATEGY = f"{API_VERSION_1}/power/active_strategy"
+
+    P1_DETAILS = f"{API_VERSION_1}/p1/details"
     P1_STATUS = f"{API_VERSION_1}/p1/status"
+    
     SYSTEM_SETTINGS = f"{API_VERSION_1}/system/settings"
     SYSTEM_INFO = f"{API_VERSION_1}/system/info"
+    WIFI_STA_CREDENTIALS = f"{API_VERSION_1}/wifi_sta/credentials"
 
 
 class SessyPowerStrategy(str, Enum):
     API = "POWER_STRATEGY_API"
     NOM = "POWER_STRATEGY_NOM"
     ROI = "POWER_STRATEGY_ROI"
     IDLE = "POWER_STRATEGY_IDLE"
```

### Comparing `sessypy-0.0.7/src/sessypy/devices.py` & `sessypy-0.0.8/src/sessypy/devices.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,41 +1,52 @@
 from .const import SessyApiCommand, SessyOtaTarget, SessyPowerStrategy
 from .api import SessyApi
 from .util import SessyConnectionException, SessyNotSupportedException
 
 class SessyDevice():
     def __init__(self, host, username: str, password: str):
         self._serial_number = username.upper()
-        self.api = SessyApi(host, username, password)
-        self.host = host
+        self._api = SessyApi(host, username, password)
+        self._host = host
     
     def __init__(self, api: SessyApi):
         self._serial_number = api.username.upper()
-        self.api = api
-        self.host = api.host
+        self._api = api
+        self._host = api.host
 
     @property
-    def serial_number(self):
+    def serial_number(self) -> str:
         return self._serial_number
     
     @property
-    def name(self):
+    def name(self) -> str:
         return f"Sessy-{ self.serial_number[0:4] }"
+    
+    @property
+    def host(self) -> str:
+        return self._host
+
+    @property
+    def api(self) -> SessyApi:
+        return self._api
 
     async def get_ota_status(self):
         return await self.api.get(SessyApiCommand.OTA_STATUS)
     
     async def check_ota(self):
         return await self.api.get(SessyApiCommand.OTA_CHECK)
     
     async def install_ota(self, target: SessyOtaTarget):
         return await self.api.post(SessyApiCommand.OTA_START, {"target": target.value})
     
     async def get_network_status(self):
-        return await self.api.get(SessyApiCommand.NETWORK_STATUS)   
+        return await self.api.get(SessyApiCommand.NETWORK_STATUS)
+
+    async def set_wifi_credentials(self, ssid: str, password: str):
+        return await self.api.post(SessyApiCommand.WIFI_STA_CREDENTIALS, {"ssid":ssid, "pass":password})
 
     async def close(self):
         await self.api.close()
     
 class SessyBattery(SessyDevice):
     async def get_power_status(self):
         return await self.api.get(SessyApiCommand.POWER_STATUS)
@@ -52,14 +63,17 @@
     async def get_system_settings(self):
         return await self.api.get(SessyApiCommand.SYSTEM_SETTINGS)
 
 class SessyP1Meter(SessyDevice):
     async def get_p1_status(self):
         return await self.api.get(SessyApiCommand.P1_STATUS)
 
+    async def get_p1_details(self):
+        return await self.api.get(SessyApiCommand.P1_DETAILS)
+
 class SessyCTMeter(SessyDevice):
     pass    
 	
 
 """Connect to the API and determine the device type"""
 async def get_sessy_device(host: str, username: str, password: str) -> SessyDevice:
```

### Comparing `sessypy-0.0.7/src/sessypy.egg-info/PKG-INFO` & `sessypy-0.0.8/src/sessypy.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sessypy
-Version: 0.0.7
+Version: 0.0.8
 Summary: Python wrapper for Sessy REST API
 Home-page: https://github.com/PimDoos/sessypy
 Author: PimDoos
 License: GNU GPLv3
 Project-URL: Homepage, https://github.com/PimDoos/sessypy
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

