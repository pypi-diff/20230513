# Comparing `tmp/be-micropython-nextion-0.14.0.tar.gz` & `tmp/be-micropython-nextion-0.15.0.tar.gz`

## Comparing `be-micropython-nextion-0.14.0.tar` & `be-micropython-nextion-0.15.0.tar`

### file list

```diff
@@ -1,23 +1,23 @@
--rw-r--r--   0 runner    (1001) docker     (123)     3933 2023-03-01 21:45:08.000000 be-micropython-nextion-0.14.0/be_micropython_nextion.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)       21 2023-03-01 21:45:08.000000 be-micropython-nextion-0.14.0/be_micropython_nextion.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)      725 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9138 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/common.py
--rw-r--r--   0 runner    (1001) docker     (123)     1356 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/const.py
--rw-r--r--   0 runner    (1001) docker     (123)     2625 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_button.py
--rw-r--r--   0 runner    (1001) docker     (123)     1186 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_checkbox.py
--rw-r--r--   0 runner    (1001) docker     (123)     2787 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_dual_state_button.py
--rw-r--r--   0 runner    (1001) docker     (123)     1205 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_gauge.py
--rw-r--r--   0 runner    (1001) docker     (123)     3978 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_gpio.py
--rw-r--r--   0 runner    (1001) docker     (123)    10098 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_hardware.py
--rw-r--r--   0 runner    (1001) docker     (123)     1892 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_number.py
--rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_page.py
--rw-r--r--   0 runner    (1001) docker     (123)     1207 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_progressbar.py
--rw-r--r--   0 runner    (1001) docker     (123)     1165 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_radio.py
--rw-r--r--   0 runner    (1001) docker     (123)     7211 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_rtc.py
--rw-r--r--   0 runner    (1001) docker     (123)     3593 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_slider.py
--rw-r--r--   0 runner    (1001) docker     (123)      979 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_text.py
--rw-r--r--   0 runner    (1001) docker     (123)     8931 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_upload.py
--rw-r--r--   0 runner    (1001) docker     (123)      887 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_variable.py
--rw-r--r--   0 runner    (1001) docker     (123)     5303 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/nextion_waveform.py
--rw-r--r--   0 runner    (1001) docker     (123)     2093 2023-03-01 21:45:00.000000 be-micropython-nextion-0.14.0/nextion/typing.py
--rw-r--r--   0 runner    (1001) docker     (123)      125 2023-03-01 21:45:08.000000 be-micropython-nextion-0.14.0/nextion/version.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5573 2023-05-13 11:59:56.000000 be-micropython-nextion-0.15.0/be_micropython_nextion.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)       21 2023-05-13 11:59:56.000000 be-micropython-nextion-0.15.0/be_micropython_nextion.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      725 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9138 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1356 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/const.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2625 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_button.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1186 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_checkbox.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2787 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_dual_state_button.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1205 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_gauge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3978 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_gpio.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10139 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_hardware.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1892 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_number.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_page.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1207 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_progressbar.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1165 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_radio.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7211 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_rtc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3593 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_slider.py
+-rw-r--r--   0 runner    (1001) docker     (123)      979 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_text.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8931 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_upload.py
+-rw-r--r--   0 runner    (1001) docker     (123)      887 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_variable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5303 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/nextion_waveform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2093 2023-05-13 11:59:42.000000 be-micropython-nextion-0.15.0/nextion/typing.py
+-rw-r--r--   0 runner    (1001) docker     (123)      125 2023-05-13 11:59:55.000000 be-micropython-nextion-0.15.0/nextion/version.py
```

### Comparing `be-micropython-nextion-0.14.0/be_micropython_nextion.egg-info/PKG-INFO` & `be-micropython-nextion-0.15.0/be_micropython_nextion.egg-info/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 Metadata-Version: 2.1
 Name: be-micropython-nextion
-Version: 0.14.0
+Version: 0.15.0
 Summary: MicroPython Nextion serial displays library
 Home-page: https://github.com/brainelectronics/micropython-nextion
 Author: brainelectronics
 Author-email: info@brainelectronics.de
 License: MIT
 Project-URL: Bug Reports, https://github.com/brainelectronics/micropython-nextion/issues
 Project-URL: Source, https://github.com/brainelectronics/micropython-nextion
 Keywords: micropython,nextion,display,nextion-display,nextion-communication,uart,library
 Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: Implementation :: MicroPython
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # MicroPython Nextion library
 
 [![Downloads](https://pepy.tech/badge/micropython-nextion)](https://pepy.tech/project/micropython-nextion)
 ![Release](https://img.shields.io/github/v/release/brainelectronics/micropython-nextion?include_prereleases&color=success)
@@ -59,25 +60,78 @@
 ### Install package with upip
 
 Connect the MicroPython device to a network (if possible)
 
 ```python
 import network
 station = network.WLAN(network.STA_IF)
+station.active(True)
 station.connect('SSID', 'PASSWORD')
 station.isconnected()
 ```
 
-and install this lib on the MicroPython device like this
+#### General
+
+Install the latest package version of this lib on the MicroPython device
+
+```python
+import mip
+mip.install("github:brainelectronics/micropython-nextion")
+```
+
+For MicroPython versions below 1.19.1 use the `upip` package instead of `mip`
+
+```python
+import upip
+upip.install('micropython-nextion')
+```
+
+#### Specific version
+
+Install a specific, fixed package version of this lib on the MicroPython device
+
+```python
+import mip
+# install a verions of a specific branch
+mip.install("github:brainelectronics/micropython-nextion", version="feature/add-mip-package-file")
+# install a tag version
+mip.install("github:brainelectronics/micropython-nextion", version="0.15.0")
+```
+
+For MicroPython versions below 1.19.1 use the `upip` package instead of `mip`
+
+```python
+import upip
+upip.install('micropython-nextion')
+```
+
+#### Test version
+
+Install a specific release candidate version uploaded to
+[Test Python Package Index](https://test.pypi.org/) on every PR on the
+MicroPython device. If no specific version is set, the latest stable version
+will be used.
+
+```python
+import mip
+mip.install("github:brainelectronics/micropython-nextion", version="0.15.0-rc1.dev29")
+```
+
+For MicroPython versions below 1.19.1 use the `upip` package instead of `mip`
 
 ```python
 import upip
+# overwrite index_urls to only take artifacts from test.pypi.org
+upip.index_urls = ['https://test.pypi.org/pypi']
 upip.install('micropython-nextion')
 ```
 
+See also [brainelectronics Test PyPi Server in Docker][ref-brainelectronics-test-pypiserver]
+for a test PyPi server running on Docker.
+
 ### Manually
 
 #### Upload files to board
 
 Copy the module to the MicroPython board and import them as shown below
 using [Remote MicroPython shell][ref-remote-upy-shell]
 
@@ -135,11 +189,12 @@
 Big thank you to [ITEAD Studio][ref-itead-github] for the implementation
 of the Arduino library.
 
 <!-- Links -->
 [ref-nextion-wiki]: https://wiki.iteadstudio.com/Nextion_HMI_Solution
 [ref-itead-nextion-github]: https://github.com/itead/ITEADLIB_Arduino_Nextion
 [ref-remote-upy-shell]: https://github.com/dhylands/rshell
+[ref-brainelectronics-test-pypiserver]: https://github.com/brainelectronics/test-pypiserver
 [ref-github-be-mircopython-modules]: https://github.com/brainelectronics/micropython-modules
 [ref-itead-github]: https://github.com/itead
```

### Comparing `be-micropython-nextion-0.14.0/nextion/__init__.py` & `be-micropython-nextion-0.15.0/nextion/__init__.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/common.py` & `be-micropython-nextion-0.15.0/nextion/common.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/const.py` & `be-micropython-nextion-0.15.0/nextion/const.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_button.py` & `be-micropython-nextion-0.15.0/nextion/nextion_button.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_checkbox.py` & `be-micropython-nextion-0.15.0/nextion/nextion_checkbox.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_dual_state_button.py` & `be-micropython-nextion-0.15.0/nextion/nextion_dual_state_button.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_gauge.py` & `be-micropython-nextion-0.15.0/nextion/nextion_gauge.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_gpio.py` & `be-micropython-nextion-0.15.0/nextion/nextion_gpio.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_hardware.py` & `be-micropython-nextion-0.15.0/nextion/nextion_hardware.py`

 * *Files 1% similar despite different names*

```diff
@@ -27,14 +27,15 @@
 
 
 class NexHardware(object):
     """docstring for NexHardware"""
     def __init__(self,
                  rx_pin: int,
                  tx_pin: int,
+                 uart_id: int = 1,
                  baudrate: Optional[int] = 9600,
                  timeout: Optional[int] = 100,
                  invert: Optional[int] = 0,
                  logger: Optional[logging.Logger] = None) -> None:
         """
         Init hardware interface
 
@@ -61,15 +62,15 @@
         self._tx_pin = tx_pin
         self._rx_pin = rx_pin
         self._baudrate = baudrate
         self._timeout = timeout
         self._invert = invert
 
         self._uart = UART(
-            1,
+            uart_id,
             tx=self._tx_pin,
             rx=self._rx_pin,
             baudrate=self._baudrate,
             timeout=self._timeout,
             invert=self._invert)
 
         self._initialized = False
```

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_number.py` & `be-micropython-nextion-0.15.0/nextion/nextion_number.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_page.py` & `be-micropython-nextion-0.15.0/nextion/nextion_page.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_progressbar.py` & `be-micropython-nextion-0.15.0/nextion/nextion_progressbar.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_radio.py` & `be-micropython-nextion-0.15.0/nextion/nextion_radio.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_rtc.py` & `be-micropython-nextion-0.15.0/nextion/nextion_rtc.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_slider.py` & `be-micropython-nextion-0.15.0/nextion/nextion_slider.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_text.py` & `be-micropython-nextion-0.15.0/nextion/nextion_text.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_upload.py` & `be-micropython-nextion-0.15.0/nextion/nextion_upload.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_variable.py` & `be-micropython-nextion-0.15.0/nextion/nextion_variable.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/nextion_waveform.py` & `be-micropython-nextion-0.15.0/nextion/nextion_waveform.py`

 * *Files identical despite different names*

### Comparing `be-micropython-nextion-0.14.0/nextion/typing.py` & `be-micropython-nextion-0.15.0/nextion/typing.py`

 * *Files identical despite different names*

