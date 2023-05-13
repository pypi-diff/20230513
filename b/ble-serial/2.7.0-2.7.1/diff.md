# Comparing `tmp/ble-serial-2.7.0.tar.gz` & `tmp/ble-serial-2.7.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ble-serial-2.7.0.tar", last modified: Thu Jan 26 01:05:18 2023, max compression
+gzip compressed data, was "ble-serial-2.7.1.tar", last modified: Sat May 13 21:49:21 2023, max compression
```

## Comparing `ble-serial-2.7.0.tar` & `ble-serial-2.7.1.tar`

### file list

```diff
@@ -1,41 +1,41 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:18.489303 ble-serial-2.7.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-01-26 01:05:07.000000 ble-serial-2.7.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       59 2023-01-26 01:05:07.000000 ble-serial-2.7.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)    25279 2023-01-26 01:05:18.489303 ble-serial-2.7.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    24350 2023-01-26 01:05:07.000000 ble-serial-2.7.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:18.485303 ble-serial-2.7.0/ble_serial/
--rw-r--r--   0 runner    (1001) docker     (123)      476 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       75 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/__main__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:18.485303 ble-serial-2.7.0/ble_serial/bluetooth/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/bluetooth/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5228 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/bluetooth/ble_interface.py
--rw-r--r--   0 runner    (1001) docker     (123)      395 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/bluetooth/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     3430 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:18.485303 ble-serial-2.7.0/ble_serial/log/
--rw-r--r--   0 runner    (1001) docker     (123)      886 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/log/console_log.py
--rw-r--r--   0 runner    (1001) docker     (123)      761 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/log/fs_log.py
--rw-r--r--   0 runner    (1001) docker     (123)     3367 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/main.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:18.489303 ble-serial-2.7.0/ble_serial/ports/
--rw-r--r--   0 runner    (1001) docker     (123)      437 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/ports/interface.py
--rw-r--r--   0 runner    (1001) docker     (123)     1819 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/ports/linux_pty.py
--rw-r--r--   0 runner    (1001) docker     (123)      699 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/ports/print_dummy.py
--rw-r--r--   0 runner    (1001) docker     (123)     2134 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/ports/tcp_socket.py
--rw-r--r--   0 runner    (1001) docker     (123)     2596 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/ports/windows_com0com.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:18.489303 ble-serial-2.7.0/ble_serial/scan/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/scan/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       80 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/scan/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3039 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/scan/main.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:18.489303 ble-serial-2.7.0/ble_serial/setup_com0com/
--rw-r--r--   0 runner    (1001) docker     (123)      706 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/setup_com0com/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       80 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/setup_com0com/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1501 2023-01-26 01:05:07.000000 ble-serial-2.7.0/ble_serial/setup_com0com/windows_priv_setupc.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-26 01:05:18.485303 ble-serial-2.7.0/ble_serial.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    25279 2023-01-26 01:05:18.000000 ble-serial-2.7.0/ble_serial.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      865 2023-01-26 01:05:18.000000 ble-serial-2.7.0/ble_serial.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-01-26 01:05:18.000000 ble-serial-2.7.0/ble_serial.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       93 2023-01-26 01:05:18.000000 ble-serial-2.7.0/ble_serial.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       81 2023-01-26 01:05:18.000000 ble-serial-2.7.0/ble_serial.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-01-26 01:05:18.000000 ble-serial-2.7.0/ble_serial.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       83 2023-01-26 01:05:07.000000 ble-serial-2.7.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-01-26 01:05:18.489303 ble-serial-2.7.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1696 2023-01-26 01:05:07.000000 ble-serial-2.7.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:21.882350 ble-serial-2.7.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-05-13 21:49:12.000000 ble-serial-2.7.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       59 2023-05-13 21:49:12.000000 ble-serial-2.7.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    25279 2023-05-13 21:49:21.878350 ble-serial-2.7.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    24350 2023-05-13 21:49:12.000000 ble-serial-2.7.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:21.878350 ble-serial-2.7.1/ble_serial/
+-rw-r--r--   0 runner    (1001) docker     (123)      476 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       75 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/__main__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:21.878350 ble-serial-2.7.1/ble_serial/bluetooth/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/bluetooth/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5228 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/bluetooth/ble_interface.py
+-rw-r--r--   0 runner    (1001) docker     (123)      395 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/bluetooth/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3430 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:21.878350 ble-serial-2.7.1/ble_serial/log/
+-rw-r--r--   0 runner    (1001) docker     (123)      886 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/log/console_log.py
+-rw-r--r--   0 runner    (1001) docker     (123)      761 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/log/fs_log.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3367 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:21.878350 ble-serial-2.7.1/ble_serial/ports/
+-rw-r--r--   0 runner    (1001) docker     (123)      437 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/ports/interface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1819 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/ports/linux_pty.py
+-rw-r--r--   0 runner    (1001) docker     (123)      699 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/ports/print_dummy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2134 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/ports/tcp_socket.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2596 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/ports/windows_com0com.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:21.878350 ble-serial-2.7.1/ble_serial/scan/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/scan/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/scan/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3363 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/scan/main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:21.878350 ble-serial-2.7.1/ble_serial/setup_com0com/
+-rw-r--r--   0 runner    (1001) docker     (123)      706 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/setup_com0com/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/setup_com0com/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1501 2023-05-13 21:49:12.000000 ble-serial-2.7.1/ble_serial/setup_com0com/windows_priv_setupc.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:49:21.878350 ble-serial-2.7.1/ble_serial.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    25279 2023-05-13 21:49:21.000000 ble-serial-2.7.1/ble_serial.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      865 2023-05-13 21:49:21.000000 ble-serial-2.7.1/ble_serial.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 21:49:21.000000 ble-serial-2.7.1/ble_serial.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-05-13 21:49:21.000000 ble-serial-2.7.1/ble_serial.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-13 21:49:21.000000 ble-serial-2.7.1/ble_serial.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-13 21:49:21.000000 ble-serial-2.7.1/ble_serial.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       83 2023-05-13 21:49:12.000000 ble-serial-2.7.1/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 21:49:21.882350 ble-serial-2.7.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1696 2023-05-13 21:49:12.000000 ble-serial-2.7.1/setup.py
```

### Comparing `ble-serial-2.7.0/LICENSE` & `ble-serial-2.7.1/LICENSE`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/PKG-INFO` & `ble-serial-2.7.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ble-serial
-Version: 2.7.0
+Version: 2.7.1
 Summary: A package to connect BLE serial adapters
 Home-page: https://github.com/Jakeler/ble-serial
 Author: Jake
 Author-email: ble-serial-pypi@ja-ke.tech
 License: MIT
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Communications
```

### Comparing `ble-serial-2.7.0/README.md` & `ble-serial-2.7.1/README.md`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/bluetooth/ble_interface.py` & `ble-serial-2.7.1/ble_serial/bluetooth/ble_interface.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/cli.py` & `ble-serial-2.7.1/ble_serial/cli.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/log/console_log.py` & `ble-serial-2.7.1/ble_serial/log/console_log.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/log/fs_log.py` & `ble-serial-2.7.1/ble_serial/log/fs_log.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/main.py` & `ble-serial-2.7.1/ble_serial/main.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/ports/linux_pty.py` & `ble-serial-2.7.1/ble_serial/ports/linux_pty.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/ports/print_dummy.py` & `ble-serial-2.7.1/ble_serial/ports/print_dummy.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/ports/tcp_socket.py` & `ble-serial-2.7.1/ble_serial/ports/tcp_socket.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/ports/windows_com0com.py` & `ble-serial-2.7.1/ble_serial/ports/windows_com0com.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/scan/main.py` & `ble-serial-2.7.1/ble_serial/scan/main.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,44 +1,48 @@
 from bleak import BleakScanner, BleakClient
 from bleak.backends.service import BleakGATTServiceCollection
 from bleak.backends.device import BLEDevice
 from bleak.exc import BleakError
 import argparse, asyncio
 
 
-async def scan(adapter: str, timeout: float, service_uuid: str) -> [BLEDevice]:
-    base_kwargs = dict(adapter=adapter, timeout=timeout)
+async def scan(adapter: str, timeout: float, service_uuid: str) -> dict:
+    base_kwargs = dict(adapter=adapter, timeout=timeout, return_adv=True)
 
     if service_uuid:
         devices = await BleakScanner.discover(**base_kwargs, service_uuids=[service_uuid])
     else:
         devices = await BleakScanner.discover(**base_kwargs)
 
     return devices
 
-async def deep_scan(addr: str, devices: [BLEDevice]) -> BleakGATTServiceCollection:
-
+async def deep_scan(addr: str, devices: dict) -> BleakGATTServiceCollection:
+    devices = [data[0] for data in devices.values()]
     devices = filter(lambda dev: dev.address == addr, devices)
     devices_list = list(devices)
     if len(devices_list) > 0:
         device = devices_list[0]
         print(f'Found device {device} (out of {len(devices_list)})')
     else:
         print('Found no device with matching address')
         return []
 
     async with BleakClient(device) as client:
-        return await client.get_services()
+        return client.services
 
 
-def print_list(devices: [BLEDevice]):
-    sorted_devices = sorted(devices, key=lambda dev: dev.rssi, reverse=True)
+def print_list(devices: dict, verbose: bool):
+    for (dev, adv) in devices.values():
+        print(f'{dev.address} (rssi={adv.rssi}): {dev.name}')
+        if verbose:
+            for entry_pair in adv._asdict().items():
+                print('    %s=%s' % entry_pair)
+            print() # linebreak
+            
 
-    for d in sorted_devices:
-        print(f'{d.address} (RSSI={d.rssi}): {d.name}')
 
 def print_details(serv: BleakGATTServiceCollection):
     INDENT = '    '
     for s in serv:
         print('SERVICE', s)
         for char in s.characteristics:
             print(INDENT, 'CHARACTERISTIC', char, char.properties)
@@ -48,15 +52,15 @@
 
 async def run_from_args(args):
     print("Started general BLE scan\n")
     devices = await scan(args.adapter, args.sec, args.service_uuid)
     if len(devices) == 0:
         print('No devices found')
         return # no point in finishing / deep scan
-    print_list(devices)
+    print_list(devices, args.verbose)
     print("\nFinished general BLE scan")
 
     if args.addr:
         print(f"\nStarted deep scan of {args.addr}\n")
         services = await deep_scan(args.addr, devices)
         print_details(services)
         print(f"\nCompleted deep scan of {args.addr}")
@@ -71,13 +75,16 @@
         help='Duration of the scan in seconds')
     parser.add_argument('-i', '--interface', dest='adapter', required=False, default='hci0',
         help='BLE host adapter number to use')
     parser.add_argument('-d', '--deep-scan', dest='addr', type=str,
         help='Try to connect to device and read out service/characteristic UUIDs')
     parser.add_argument('-s', '--service-uuid', dest='service_uuid', required=False,
         help='The service used for scanning of potential devices')
+    parser.add_argument('-v', '--verbose', dest='verbose', required=False, action='store_true',
+        help='Print all infos from advertisement data')
     args = parser.parse_args()
 
     try:
         asyncio.run(run_from_args(args))
     except BleakError as be:
         print('ERROR:', be)
+
```

### Comparing `ble-serial-2.7.0/ble_serial/setup_com0com/__init__.py` & `ble-serial-2.7.1/ble_serial/setup_com0com/__init__.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial/setup_com0com/windows_priv_setupc.py` & `ble-serial-2.7.1/ble_serial/setup_com0com/windows_priv_setupc.py`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/ble_serial.egg-info/PKG-INFO` & `ble-serial-2.7.1/ble_serial.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ble-serial
-Version: 2.7.0
+Version: 2.7.1
 Summary: A package to connect BLE serial adapters
 Home-page: https://github.com/Jakeler/ble-serial
 Author: Jake
 Author-email: ble-serial-pypi@ja-ke.tech
 License: MIT
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Communications
```

### Comparing `ble-serial-2.7.0/ble_serial.egg-info/SOURCES.txt` & `ble-serial-2.7.1/ble_serial.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `ble-serial-2.7.0/setup.py` & `ble-serial-2.7.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
     long_description = fh.read()
 
 with open("requirements.txt", "r") as fr:
     REQUIRES = fr.read()
 
 setuptools.setup(
     name="ble-serial",
-    version="2.7.0",
+    version="2.7.1",
     author="Jake",
     author_email="ble-serial-pypi@ja-ke.tech",
     description="A package to connect BLE serial adapters",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/Jakeler/ble-serial",
     packages=[
```

