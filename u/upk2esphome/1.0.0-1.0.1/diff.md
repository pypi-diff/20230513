# Comparing `tmp/upk2esphome-1.0.0.tar.gz` & `tmp/upk2esphome-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "upk2esphome-1.0.0.tar", max compression
+gzip compressed data, was "upk2esphome-1.0.1.tar", max compression
```

## Comparing `upk2esphome-1.0.0.tar` & `upk2esphome-1.0.1.tar`

### file list

```diff
@@ -1,30 +1,30 @@
--rw-r--r--   0        0        0     1076 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/LICENSE
--rw-r--r--   0        0        0      531 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/README.md
--rw-r--r--   0        0        0      455 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/pyproject.toml
--rw-r--r--   0        0        0      256 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/__init__.py
--rw-r--r--   0        0        0     1331 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/generator.py
--rw-r--r--   0        0        0     1442 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/input.py
--rw-r--r--   0        0        0      400 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/opts.py
--rw-r--r--   0        0        0       48 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/parts/__init__.py
--rw-r--r--   0        0        0     8367 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/parts/bulb.py
--rw-r--r--   0        0        0     1395 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/parts/module.py
--rw-r--r--   0        0        0     3248 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/parts/monitor.py
--rw-r--r--   0        0        0      775 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/parts/netled.py
--rw-r--r--   0        0        0     1355 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/parts/static.py
--rw-r--r--   0        0        0     3007 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/parts/switch.py
--rw-r--r--   0        0        0     1834 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/result.py
--rw-r--r--   0        0        0      651 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/test.py
--rw-r--r--   0        0        0      444 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/bulb_cw_pwm.txt
--rw-r--r--   0        0        0      563 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/bulb_rgbc_2135_2.txt
--rw-r--r--   0        0        0      430 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/bulb_rgbcw_2135.txt
--rw-r--r--   0        0        0      543 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/bulb_rgbcw_2135_ampere.txt
--rw-r--r--   0        0        0      599 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/bulb_rgbcw_2235.txt
--rw-r--r--   0        0        0      496 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/bulb_rgbcw_5758d.txt
--rw-r--r--   0        0        0        0 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/empty.txt
--rw-r--r--   0        0        0     2936 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/plug_monitor_bl0937.txt
--rw-r--r--   0        0        0      476 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/plug_monitor_bl0942.txt
--rw-r--r--   0        0        0      497 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/plug_monitor_hlw8032.txt
--rw-r--r--   0        0        0      914 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/plug_total.txt
--rw-r--r--   0        0        0      777 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/tests/switch_monitor.txt
--rw-r--r--   0        0        0      922 2023-05-13 15:28:08.231539 upk2esphome-1.0.0/upk2esphome/web.py
--rw-r--r--   0        0        0     1029 1970-01-01 00:00:00.000000 upk2esphome-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0     1076 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/LICENSE
+-rw-r--r--   0        0        0      531 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/README.md
+-rw-r--r--   0        0        0      455 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0      256 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/__init__.py
+-rw-r--r--   0        0        0     1650 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/generator.py
+-rw-r--r--   0        0        0     1442 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/input.py
+-rw-r--r--   0        0        0      400 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/opts.py
+-rw-r--r--   0        0        0       48 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/parts/__init__.py
+-rw-r--r--   0        0        0     8367 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/parts/bulb.py
+-rw-r--r--   0        0        0     1403 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/parts/module.py
+-rw-r--r--   0        0        0     3355 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/parts/monitor.py
+-rw-r--r--   0        0        0      775 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/parts/netled.py
+-rw-r--r--   0        0        0     1355 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/parts/static.py
+-rw-r--r--   0        0        0     3009 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/parts/switch.py
+-rw-r--r--   0        0        0     1834 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/result.py
+-rw-r--r--   0        0        0      651 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/test.py
+-rw-r--r--   0        0        0      444 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/bulb_cw_pwm.txt
+-rw-r--r--   0        0        0      563 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/bulb_rgbc_2135_2.txt
+-rw-r--r--   0        0        0      430 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/bulb_rgbcw_2135.txt
+-rw-r--r--   0        0        0      543 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/bulb_rgbcw_2135_ampere.txt
+-rw-r--r--   0        0        0      599 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/bulb_rgbcw_2235.txt
+-rw-r--r--   0        0        0      496 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/bulb_rgbcw_5758d.txt
+-rw-r--r--   0        0        0        0 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/empty.txt
+-rw-r--r--   0        0        0     2936 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/plug_monitor_bl0937.txt
+-rw-r--r--   0        0        0      476 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/plug_monitor_bl0942.txt
+-rw-r--r--   0        0        0      497 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/plug_monitor_hlw8032.txt
+-rw-r--r--   0        0        0      914 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/plug_total.txt
+-rw-r--r--   0        0        0      777 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/tests/switch_monitor.txt
+-rw-r--r--   0        0        0      922 2023-05-13 17:10:01.414842 upk2esphome-1.0.1/upk2esphome/web.py
+-rw-r--r--   0        0        0     1029 1970-01-01 00:00:00.000000 upk2esphome-1.0.1/PKG-INFO
```

### Comparing `upk2esphome-1.0.0/LICENSE` & `upk2esphome-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/README.md` & `upk2esphome-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/generator.py` & `upk2esphome-1.0.1/upk2esphome/generator.py`

 * *Files 18% similar despite different names*

```diff
@@ -13,14 +13,28 @@
     if inverted:
         data[key] = {
             "number": data[key],
             "inverted": True,
         }
 
 
+def pull(data: dict, inverted: bool, key: str = "pin"):
+    if inverted:
+        data[key] = {
+            "number": data[key],
+            "inverted": True,
+            "mode": "INPUT_PULLUP",
+        }
+    else:
+        data[key] = {
+            "number": data[key],
+            "mode": "INPUT_PULLDOWN",
+        }
+
+
 def generate_yaml(config: str, opts: Opts) -> YamlResult:
     from .parts import bulb, module, monitor, netled, static, switch
 
     parts = [module, static, bulb, switch, netled, monitor]
     yr = YamlResult()
 
     try:
```

### Comparing `upk2esphome-1.0.0/upk2esphome/input.py` & `upk2esphome-1.0.1/upk2esphome/input.py`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/parts/bulb.py` & `upk2esphome-1.0.1/upk2esphome/parts/bulb.py`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/parts/module.py` & `upk2esphome-1.0.1/upk2esphome/parts/module.py`

 * *Files 3% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 def generate(yr: YamlResult, config: dict, opts: Opts):
     if "module" in config:
         module = config["module"]
     else:
         yr.warn("No module type found! You have to set the board: manually")
         if opts.esphome_block:
             yr.data["esphome"] = {
-                "name": "UPK2ESPHome",
+                "name": "upk2esphome",
             }
             if opts.name_mac:
                 yr.data["esphome"]["name_add_mac_suffix"] = True
             yr.data["libretiny"] = {
                 "board": "FIX_ME",
                 "framework": {
                     "version": "dev",
@@ -32,15 +32,15 @@
             yr.warn("Only BK7231T and BK7231N chips are currently supported")
             return
 
     yr.log(f"Found {module} config!")
 
     if opts.esphome_block:
         yr.data["esphome"] = {
-            "name": config["module"],
+            "name": config["module"].lower(),
         }
         if opts.name_mac:
             yr.data["esphome"]["name_add_mac_suffix"] = True
         yr.data["libretiny"] = {
             "board": board,
             "framework": {
                 "version": "dev",
```

### Comparing `upk2esphome-1.0.0/upk2esphome/parts/monitor.py` & `upk2esphome-1.0.1/upk2esphome/parts/monitor.py`

 * *Files 9% similar despite different names*

```diff
@@ -51,14 +51,16 @@
                 "power": {"name": f"{chip} Power"},
                 "energy": {"name": f"{chip} Energy"},
             }
             if resistor is not None:
                 yr.log(f" - shunt resistor: {resistor} mΩ")
                 sensor["current_resistor"] = f"{resistor/1000:.03f} ohm"
             invert(sensor, sel_inv, "sel_pin")
+            invert(sensor, chip_type == 0, "cf_pin")
+            invert(sensor, chip_type == 0, "cf1_pin")
             yr.sensor(sensor)
 
         case 2:  # HLW8032
             yr.warn("HLW8032 is not supported")
 
         case 3:  # BL0942
             rx_pin = config.get("ele_rx", None)
```

### Comparing `upk2esphome-1.0.0/upk2esphome/parts/netled.py` & `upk2esphome-1.0.1/upk2esphome/parts/netled.py`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/parts/static.py` & `upk2esphome-1.0.1/upk2esphome/parts/static.py`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/parts/switch.py` & `upk2esphome-1.0.1/upk2esphome/parts/switch.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 #  Copyright (c) Kuba Szczodrzyński 2023-4-21.
 
-from upk2esphome.generator import invert
+from upk2esphome.generator import invert, pull
 from upk2esphome.opts import Opts
 from upk2esphome.result import YamlResult
 
 
 def generate(yr: YamlResult, config: dict, opts: Opts):
     keys = [
         "bt1_pin",
@@ -73,15 +73,15 @@
                 "pin": f"P{bt_pin}",
                 "on_press": {
                     "then": [
                         {"switch.toggle": switch["id"]},
                     ],
                 },
             }
-            invert(binary, bt_inv)
+            pull(binary, bt_inv)
             yr.binary(binary)
         switches.append(switch["id"])
         yr.switch(switch)
 
     bt_pin = config.get(f"total_bt_pin", None)
     bt_inv = config.get(f"total_bt_lv", None) == 0
     if bt_pin is not None:
@@ -89,11 +89,11 @@
         yr.found = True
         binary = {
             "platform": "gpio",
             "id": f"binary_switch_all",
             "pin": f"P{bt_pin}",
             "on_press": {"then": []},
         }
-        invert(binary, bt_inv)
+        pull(binary, bt_inv)
         for switch in switches:
             binary["on_press"]["then"].append({"switch.toggle": switch})
         yr.binary(binary)
```

### Comparing `upk2esphome-1.0.0/upk2esphome/result.py` & `upk2esphome-1.0.1/upk2esphome/result.py`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/test.py` & `upk2esphome-1.0.1/upk2esphome/test.py`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/tests/bulb_rgbc_2135_2.txt` & `upk2esphome-1.0.1/upk2esphome/tests/bulb_rgbc_2135_2.txt`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/tests/bulb_rgbcw_2135_ampere.txt` & `upk2esphome-1.0.1/upk2esphome/tests/bulb_rgbcw_2135_ampere.txt`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/tests/bulb_rgbcw_2235.txt` & `upk2esphome-1.0.1/upk2esphome/tests/bulb_rgbcw_2235.txt`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/tests/plug_monitor_bl0937.txt` & `upk2esphome-1.0.1/upk2esphome/tests/plug_monitor_bl0937.txt`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/tests/plug_total.txt` & `upk2esphome-1.0.1/upk2esphome/tests/plug_total.txt`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/tests/switch_monitor.txt` & `upk2esphome-1.0.1/upk2esphome/tests/switch_monitor.txt`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/upk2esphome/web.py` & `upk2esphome-1.0.1/upk2esphome/web.py`

 * *Files identical despite different names*

### Comparing `upk2esphome-1.0.0/PKG-INFO` & `upk2esphome-1.0.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: upk2esphome
-Version: 1.0.0
+Version: 1.0.1
 Summary: Convert Tuya device configuration to ESPHome YAML
 License: MIT
 Author: Kuba Szczodrzyński
 Author-email: kuba@szczodrzynski.pl
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

