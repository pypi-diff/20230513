# Comparing `tmp/jvc_projector_remote_improved2-3.5.8.tar.gz` & `tmp/jvc_projector_remote_improved2-3.6.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jvc_projector_remote_improved2-3.5.8.tar", last modified: Sat Apr  8 00:17:15 2023, max compression
+gzip compressed data, was "jvc_projector_remote_improved2-3.6.0.tar", last modified: Fri May 12 22:56:30 2023, max compression
```

## Comparing `jvc_projector_remote_improved2-3.5.8.tar` & `jvc_projector_remote_improved2-3.6.0.tar`

### file list

```diff
@@ -1,21 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-08 00:17:15.803913 jvc_projector_remote_improved2-3.5.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5904 2023-04-08 00:17:15.803913 jvc_projector_remote_improved2-3.5.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5469 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-08 00:17:15.799913 jvc_projector_remote_improved2-3.5.8/jvc_projector/
--rw-r--r--   0 runner    (1001) docker     (123)      151 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/jvc_projector/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6344 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/jvc_projector/commands.py
--rw-r--r--   0 runner    (1001) docker     (123)    20940 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/jvc_projector/jvc_projector.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-08 00:17:15.803913 jvc_projector_remote_improved2-3.5.8/jvc_projector_remote_improved2.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5904 2023-04-08 00:17:15.000000 jvc_projector_remote_improved2-3.5.8/jvc_projector_remote_improved2.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      400 2023-04-08 00:17:15.000000 jvc_projector_remote_improved2-3.5.8/jvc_projector_remote_improved2.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-08 00:17:15.000000 jvc_projector_remote_improved2-3.5.8/jvc_projector_remote_improved2.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-04-08 00:17:15.000000 jvc_projector_remote_improved2-3.5.8/jvc_projector_remote_improved2.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-08 00:17:15.803913 jvc_projector_remote_improved2-3.5.8/mock/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/mock/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3403 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/mock/mochrie.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-08 00:17:15.803913 jvc_projector_remote_improved2-3.5.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      639 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-08 00:17:15.803913 jvc_projector_remote_improved2-3.5.8/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1784 2023-04-08 00:17:05.000000 jvc_projector_remote_improved2-3.5.8/tests/testLowLatency.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:56:30.084529 jvc_projector_remote_improved2-3.6.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-12 22:56:18.000000 jvc_projector_remote_improved2-3.6.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5903 2023-05-12 22:56:30.084529 jvc_projector_remote_improved2-3.6.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5468 2023-05-12 22:56:18.000000 jvc_projector_remote_improved2-3.6.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:56:30.080529 jvc_projector_remote_improved2-3.6.0/jvc_projector/
+-rw-r--r--   0 runner    (1001) docker     (123)      151 2023-05-12 22:56:18.000000 jvc_projector_remote_improved2-3.6.0/jvc_projector/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6849 2023-05-12 22:56:18.000000 jvc_projector_remote_improved2-3.6.0/jvc_projector/commands.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22344 2023-05-12 22:56:18.000000 jvc_projector_remote_improved2-3.6.0/jvc_projector/jvc_projector.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:56:30.080529 jvc_projector_remote_improved2-3.6.0/jvc_projector_remote_improved2.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5903 2023-05-12 22:56:30.000000 jvc_projector_remote_improved2-3.6.0/jvc_projector_remote_improved2.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      367 2023-05-12 22:56:30.000000 jvc_projector_remote_improved2-3.6.0/jvc_projector_remote_improved2.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:56:30.000000 jvc_projector_remote_improved2-3.6.0/jvc_projector_remote_improved2.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-12 22:56:30.000000 jvc_projector_remote_improved2-3.6.0/jvc_projector_remote_improved2.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 22:56:30.084529 jvc_projector_remote_improved2-3.6.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      639 2023-05-12 22:56:18.000000 jvc_projector_remote_improved2-3.6.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:56:30.084529 jvc_projector_remote_improved2-3.6.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:56:18.000000 jvc_projector_remote_improved2-3.6.0/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1784 2023-05-12 22:56:18.000000 jvc_projector_remote_improved2-3.6.0/tests/testLowLatency.py
```

### Comparing `jvc_projector_remote_improved2-3.5.8/LICENSE` & `jvc_projector_remote_improved2-3.6.0/LICENSE`

 * *Files identical despite different names*

### Comparing `jvc_projector_remote_improved2-3.5.8/PKG-INFO` & `jvc_projector_remote_improved2-3.6.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 Metadata-Version: 2.1
 Name: jvc_projector_remote_improved2
-Version: 3.5.8
+Version: 3.6.0
 Summary: A package to control JVC projectors over IP
 Home-page: https://github.com/iloveicedgreentea/jvc_projector_improved
 Author: iloveicedgreentea
 Classifier: Programming Language :: Python :: 3.9
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-# JVC Projector Remote Improved
+# JVC Projector Python Library
 
 This implements new features, improvements, and optimizations inspired by https://github.com/bezmi/jvc_projector. This was made with NZ models in mind. Almost every function will work with NX models but I do not guarantee operability for them.
 
 This is designed to work with my Home Assistant plugin: https://github.com/iloveicedgreentea/jvc_homeassistant
 
 ## Installation
```

### Comparing `jvc_projector_remote_improved2-3.5.8/README.md` & `jvc_projector_remote_improved2-3.6.0/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# JVC Projector Remote Improved
+# JVC Projector Python Library
 
 This implements new features, improvements, and optimizations inspired by https://github.com/bezmi/jvc_projector. This was made with NZ models in mind. Almost every function will work with NX models but I do not guarantee operability for them.
 
 This is designed to work with my Home Assistant plugin: https://github.com/iloveicedgreentea/jvc_homeassistant
 
 ## Installation
```

### Comparing `jvc_projector_remote_improved2-3.5.8/jvc_projector/commands.py` & `jvc_projector_remote_improved2-3.6.0/jvc_projector/commands.py`

 * *Files 8% similar despite different names*

```diff
@@ -25,16 +25,17 @@
     picture_ack = b"PM"
     lens_ack = b"IN"
     greeting = b"PJ_OK"
     pj_ack = b"PJACK"
     pj_req = b"PJREQ"
     install_acks = b"IN"
     hdmi_ack = b"IS"
-    hdr_ack = b"IF"
+    info_ack = b"IF"
     model = b"MD"
+    source_ack = b"SC"
 
 
 class InputModes(Enum):
     """
     HMDMI inputs 1 and 2
     """
 
@@ -243,21 +244,35 @@
     sdr = b"0"
     hdr = b"1"
     smpte = b"2"
     hybridlog = b"3"
     hdr10_plus = b"4"
     none = b"F"
 
+class HdrLevel(Enum):
+    auto = b"0"
+    min2 = b"1"
+    min1 = b"2"
+    zero = b"3"
+    plus1 = b"4"
+    plus2 = b"5"
+
 
 class AspectRatioModes(Enum):
     zoom = b"2"
     auto = b"3"
     native = b"4"
 
 
+class SourceStatuses(Enum):
+    logo = b"\x00"
+    no_signal = b"0"
+    signal = b"1"
+
+
 class Commands(Enum):
 
     # these use ! unless otherwise indicated
     # power commands
     power = b"PW", PowerModes, ACKs.power_ack
 
     # lens memory /installation mode commands
@@ -272,22 +287,26 @@
     current_output = b"IP"
     info = b"RC7374"
 
     # Checking for model code
     # response -> \x40\x89\x01\x4D\x44(the model code)\x0A
     get_model = b"MD"
 
+    # software version
+    get_software_version = b"IFSV", str, ACKs.info_ack
+
     # content type
     content_type = b"PMAT", ContentTypes, ACKs.picture_ack
 
     # hdr processing (like frame by frame)
     hdr_processing = b"PMHP", HdrProcessing, ACKs.picture_ack
+    hdr_level = b"PMHL", HdrLevel, ACKs.picture_ack
 
     # hdr data
-    hdr_data = b"IFHR", HdrData, ACKs.hdr_ack
+    hdr_data = b"IFHR", HdrData, ACKs.info_ack
 
     # theater optimizer on/off
     theater_optimizer = b"PMNM", TheaterOptimizer, ACKs.picture_ack
 
     # picture mode commands
     picture_mode = b"PMPM", PictureModes, ACKs.picture_ack
 
@@ -320,16 +339,22 @@
 
     # NZ Series Laser Dimming commands
     laser_mode = b"PMDC", LaserDimModes, ACKs.picture_ack
 
     # Lamp power
     lamp_power = b"PMLP", LampPowerModes, ACKs.picture_ack
 
+    # Lamp time
+    lamp_time = b"IFLT", int, ACKs.info_ack
+
     # Lens Aperture commands
     aperture = b"PMDI", ApertureModes, ACKs.picture_ack
 
     # Anamorphic commands
     # I don't use this, untested
     anamorphic = b"INVS", AnamorphicModes, ACKs.lens_ack
 
     # e-shift
     eshift_mode = b"PMUS", EshiftModes, ACKs.picture_ack
+
+    # source status
+    source_status = b"SC", SourceStatuses, ACKs.source_ack
```

### Comparing `jvc_projector_remote_improved2-3.5.8/jvc_projector/jvc_projector.py` & `jvc_projector_remote_improved2-3.6.0/jvc_projector/jvc_projector.py`

 * *Files 5% similar despite different names*

```diff
@@ -19,19 +19,22 @@
     InstallationModes,
     InputModes,
     LaserDimModes,
     Enum,
     LowLatencyModes,
     ContentTypes,
     HdrProcessing,
+    SourceStatuses,
     TheaterOptimizer,
     HdrData,
     LampPowerModes,
     LaserPowerModes,
-    AspectRatioModes
+    AspectRatioModes,
+    MaskModes,
+    HdrLevel
 )
 
 
 class JVCProjector:
     """JVC Projector Control"""
 
     def __init__(
@@ -467,14 +470,15 @@
         )
 
         if success:
             msg = self._replace_headers(msg)
 
         return msg, success
 
+    # its possible to write one generic func to do all of these but there is different support per model so its easier to just split it up
     def get_low_latency_state(self) -> str:
         """
         Get the current state of LL
         """
         state, _ = self._do_reference_op("low_latency", ACKs.picture_ack)
 
         return LowLatencyModes(state.replace(ACKs.picture_ack.value, b"")).name
@@ -495,14 +499,21 @@
 
     def get_input_mode(self) -> str:
         """
         Get the current input mode
         """
         state, _ = self._do_reference_op("input_mode", ACKs.input_ack)
         return InputModes(state.replace(ACKs.input_ack.value, b"")).name
+    
+    def get_mask_mode(self) -> str:
+        """
+        Get the current mask mode
+        """
+        state, _ = self._do_reference_op("mask", ACKs.hdmi_ack)
+        return MaskModes(state.replace(ACKs.hdmi_ack.value, b"")).name
 
     def get_laser_mode(self) -> str:
         """
         Get the current laser mode
         """
         state, _ = self._do_reference_op("laser_mode", ACKs.picture_ack)
         return LaserDimModes(state.replace(ACKs.picture_ack.value, b"")).name
@@ -523,43 +534,64 @@
 
     def get_input_level(self) -> str:
         """
         Get the current input level
         """
         state, _ = self._do_reference_op("input_level", ACKs.hdmi_ack)
         return InputLevel(state.replace(ACKs.hdmi_ack.value, b"")).name
+    
+    def get_software_version(self) -> str:
+        """
+        Get the current software version
+        """
+        state, _ = self._do_reference_op("get_software_version", ACKs.info_ack)
+        return state.replace(ACKs.info_ack.value, b"")
 
     def get_content_type(self) -> str:
         """
         Get the current content type
         """
         state, _ = self._do_reference_op("content_type", ACKs.picture_ack)
         return ContentTypes(state.replace(ACKs.picture_ack.value, b"")).name
 
     def get_hdr_processing(self) -> str:
         """
         Get the current hdr processing setting like frame by frame. Will fail if not in HDR mode!
         """
         state, _ = self._do_reference_op("hdr_processing", ACKs.picture_ack)
         return HdrProcessing(state.replace(ACKs.picture_ack.value, b"")).name
+    
+    def get_hdr_level(self) -> str:
+        """
+        Get the current hdr quantization level
+        """
+        state, _ = self._do_reference_op("hdr_level", ACKs.picture_ack)
+        return HdrLevel(state.replace(ACKs.picture_ack.value, b"")).name
 
     def get_hdr_data(self) -> str:
         """
         Get the current hdr mode -> sdr, hdr10_plus, etc
         """
-        state, _ = self._do_reference_op("hdr_data", ACKs.hdr_ack)
-        return HdrData(state.replace(ACKs.hdr_ack.value, b"")).name
+        state, _ = self._do_reference_op("hdr_data", ACKs.info_ack)
+        return HdrData(state.replace(ACKs.info_ack.value, b"")).name
 
     def get_lamp_power(self) -> str:
         """
         Get the current lamp power non-NZ only
         """
         state, _ = self._do_reference_op("lamp_power", ACKs.picture_ack)
         return LampPowerModes(state.replace(ACKs.picture_ack.value, b"")).name
 
+    def get_lamp_time(self) -> int:
+        """
+        Get the current lamp time
+        """
+        state, _ = self._do_reference_op("lamp_time", ACKs.info_ack)
+        return int(state.replace(ACKs.info_ack.value, b""), 16)
+
     def get_laser_power(self) -> str:
         """
         Get the current laser power NZ only
         """
         state, _ = self._do_reference_op("laser_power", ACKs.picture_ack)
         return LaserPowerModes(state.replace(ACKs.picture_ack.value, b"")).name
 
@@ -573,14 +605,21 @@
     def get_aspect_ratio(self) -> str:
         """
         Return aspect ratio
         """
         state, _ = self._do_reference_op("aspect_ratio", ACKs.hdmi_ack)
         return AspectRatioModes(state.replace(ACKs.hdmi_ack.value, b"")).name
 
+    def get_source_status(self) -> str:
+        """
+        Return source status
+        """
+        state, _ = self._do_reference_op("source_status", ACKs.source_ack)
+        return SourceStatuses(state.replace(ACKs.source_ack.value, b"")).name
+
     def _get_power_state(self) -> str:
         """
         Return the current power state
 
         Returns str: values of PowerStates
         """
         # remove the headers
```

### Comparing `jvc_projector_remote_improved2-3.5.8/jvc_projector_remote_improved2.egg-info/PKG-INFO` & `jvc_projector_remote_improved2-3.6.0/jvc_projector_remote_improved2.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 Metadata-Version: 2.1
 Name: jvc-projector-remote-improved2
-Version: 3.5.8
+Version: 3.6.0
 Summary: A package to control JVC projectors over IP
 Home-page: https://github.com/iloveicedgreentea/jvc_projector_improved
 Author: iloveicedgreentea
 Classifier: Programming Language :: Python :: 3.9
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-# JVC Projector Remote Improved
+# JVC Projector Python Library
 
 This implements new features, improvements, and optimizations inspired by https://github.com/bezmi/jvc_projector. This was made with NZ models in mind. Almost every function will work with NX models but I do not guarantee operability for them.
 
 This is designed to work with my Home Assistant plugin: https://github.com/iloveicedgreentea/jvc_homeassistant
 
 ## Installation
```

### Comparing `jvc_projector_remote_improved2-3.5.8/setup.py` & `jvc_projector_remote_improved2-3.6.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="jvc_projector_remote_improved2",
-    version="3.5.8",
+    version="3.6.0",
     author="iloveicedgreentea",
     description="A package to control JVC projectors over IP",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/iloveicedgreentea/jvc_projector_improved",
     packages=setuptools.find_packages(),
     classifiers=[
```

### Comparing `jvc_projector_remote_improved2-3.5.8/tests/testLowLatency.py` & `jvc_projector_remote_improved2-3.6.0/tests/testLowLatency.py`

 * *Files identical despite different names*

