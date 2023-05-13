# Comparing `tmp/uc_browser-0.3.2.tar.gz` & `tmp/uc_browser-0.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "uc_browser-0.3.2.tar", max compression
+gzip compressed data, was "uc_browser-0.3.3.tar", max compression
```

## Comparing `uc_browser-0.3.2.tar` & `uc_browser-0.3.3.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       63 2022-10-11 19:35:12.176241 uc_browser-0.3.2/README.md
--rw-r--r--   0        0        0      503 2023-04-05 16:50:47.814184 uc_browser-0.3.2/pyproject.toml
--rw-r--r--   0        0        0        0 2022-10-11 19:35:12.176241 uc_browser-0.3.2/uc_browser/__init__.py
--rw-r--r--   0        0        0     8159 2023-01-17 19:09:01.710189 uc_browser-0.3.2/uc_browser/browser.py
--rw-r--r--   0        0        0    10230 2023-04-05 16:37:25.456215 uc_browser-0.3.2/uc_browser/browser_v2.py
--rw-r--r--   0        0        0      802 1970-01-01 00:00:00.000000 uc_browser-0.3.2/setup.py
--rw-r--r--   0        0        0      868 1970-01-01 00:00:00.000000 uc_browser-0.3.2/PKG-INFO
+-rw-r--r--   0        0        0       63 2022-10-11 19:35:12.176241 uc_browser-0.3.3/README.md
+-rw-r--r--   0        0        0      503 2023-05-13 13:54:07.183297 uc_browser-0.3.3/pyproject.toml
+-rw-r--r--   0        0        0        0 2022-10-11 19:35:12.176241 uc_browser-0.3.3/uc_browser/__init__.py
+-rw-r--r--   0        0        0     8159 2023-01-17 19:09:01.710189 uc_browser-0.3.3/uc_browser/browser.py
+-rw-r--r--   0        0        0    10590 2023-05-13 13:54:07.175297 uc_browser-0.3.3/uc_browser/browser_v2.py
+-rw-r--r--   0        0        0      802 1970-01-01 00:00:00.000000 uc_browser-0.3.3/setup.py
+-rw-r--r--   0        0        0      868 1970-01-01 00:00:00.000000 uc_browser-0.3.3/PKG-INFO
```

### Comparing `uc_browser-0.3.2/uc_browser/browser.py` & `uc_browser-0.3.3/uc_browser/browser.py`

 * *Files identical despite different names*

### Comparing `uc_browser-0.3.2/uc_browser/browser_v2.py` & `uc_browser-0.3.3/uc_browser/browser_v2.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 import undetected_chromedriver as uc
 
 from selenium.webdriver.common.by import By
 from selenium.webdriver.support.ui import WebDriverWait
 from selenium.webdriver.support import expected_conditions as EC
 from selenium.webdriver.common.action_chains import ActionChains
+from selenium.webdriver.common.actions.wheel_input import ScrollOrigin
 
 from time import sleep
 
 import os
 from random import choice, uniform
 
 
@@ -165,21 +166,28 @@
             if window_handle != original_tab:
                 self.driver.switch_to.window(window_handle)
                 break
 
     def click_reCaptcha(
             self,
             iframe_selector="iframe[name^='a-'][src^='https://www.google.com/recaptcha/api2/anchor?']",
-            anchor = '//*[@id="recaptcha-anchor"]',
+            anchor='//*[@id="recaptcha-anchor"]',
             time=10):
         WebDriverWait(self.driver, time).until(EC.frame_to_be_available_and_switch_to_it(
             (By.CSS_SELECTOR, iframe_selector)))
         WebDriverWait(self.driver, time).until(
             EC.element_to_be_clickable((By.XPATH, anchor))).click()
 
+    def scroll_to_element(self, xpath, offset=100):
+        element = self.driver.find_element(By.XPATH, xpath)
+        scroll_origin = ScrollOrigin.from_element(element)
+        ActionChains(self.driver) \
+            .scroll_from_origin(scroll_origin, 0, offset) \
+            .perform()
+
 
 class ChecksBypass(BrowserV2):
     def __init__(self, profile_path=None, rotative_agent=None, active_sleep=False):
         self.__profile_path = profile_path
         self.__active_sleep = active_sleep
         self.__rotative_agent = rotative_agent
```

### Comparing `uc_browser-0.3.2/setup.py` & `uc_browser-0.3.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 ['selenium-wire>=5.1.0,<6.0.0',
  'stem>=1.8.0,<2.0.0',
  'undetected-chromedriver>=3.1.5,<4.0.0',
  'webdriver-manager>=3.5.4,<4.0.0']
 
 setup_kwargs = {
     'name': 'uc-browser',
-    'version': '0.3.2',
+    'version': '0.3.3',
     'description': '',
     'long_description': '# browser\nModulo que implementa metodos para uso com selenium.\n',
     'author': 'Thiago Oliveira',
     'author_email': 'thiceconelo@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/ceconelo/browser',
```

### Comparing `uc_browser-0.3.2/PKG-INFO` & `uc_browser-0.3.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: uc-browser
-Version: 0.3.2
+Version: 0.3.3
 Summary: 
 Home-page: https://github.com/ceconelo/browser
 License: MIT
 Author: Thiago Oliveira
 Author-email: thiceconelo@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

