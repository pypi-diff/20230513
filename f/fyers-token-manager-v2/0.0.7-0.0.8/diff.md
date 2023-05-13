# Comparing `tmp/fyers_token_manager_v2-0.0.7.tar.gz` & `tmp/fyers_token_manager_v2-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fyers_token_manager_v2-0.0.7.tar", last modified: Wed May 10 05:36:55 2023, max compression
+gzip compressed data, was "fyers_token_manager_v2-0.0.8.tar", last modified: Sat May 13 04:04:11 2023, max compression
```

## Comparing `fyers_token_manager_v2-0.0.7.tar` & `fyers_token_manager_v2-0.0.8.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxr-x   0 krunaldodiya  (1000) krunaldodiya  (1000)        0 2023-05-10 05:36:55.975710 fyers_token_manager_v2-0.0.7/
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)       11 2022-10-12 11:09:01.000000 fyers_token_manager_v2-0.0.7/LICENSE
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)     1120 2023-05-10 05:36:55.975710 fyers_token_manager_v2-0.0.7/PKG-INFO
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)      786 2023-05-10 05:26:39.000000 fyers_token_manager_v2-0.0.7/README.md
-drwxrwxr-x   0 krunaldodiya  (1000) krunaldodiya  (1000)        0 2023-05-10 05:36:55.971711 fyers_token_manager_v2-0.0.7/fyers_token_manager_v2/
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)     4588 2023-05-10 05:36:04.000000 fyers_token_manager_v2-0.0.7/fyers_token_manager_v2/__init__.py
-drwxrwxr-x   0 krunaldodiya  (1000) krunaldodiya  (1000)        0 2023-05-10 05:36:55.975710 fyers_token_manager_v2-0.0.7/fyers_token_manager_v2.egg-info/
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)     1120 2023-05-10 05:36:55.000000 fyers_token_manager_v2-0.0.7/fyers_token_manager_v2.egg-info/PKG-INFO
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)      290 2023-05-10 05:36:55.000000 fyers_token_manager_v2-0.0.7/fyers_token_manager_v2.egg-info/SOURCES.txt
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)        1 2023-05-10 05:36:55.000000 fyers_token_manager_v2-0.0.7/fyers_token_manager_v2.egg-info/dependency_links.txt
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)       15 2023-05-10 05:36:55.000000 fyers_token_manager_v2-0.0.7/fyers_token_manager_v2.egg-info/requires.txt
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)       23 2023-05-10 05:36:55.000000 fyers_token_manager_v2-0.0.7/fyers_token_manager_v2.egg-info/top_level.txt
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)       38 2023-05-10 05:36:55.975710 fyers_token_manager_v2-0.0.7/setup.cfg
--rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)      682 2023-05-10 05:26:27.000000 fyers_token_manager_v2-0.0.7/setup.py
+drwxrwxr-x   0 krunaldodiya  (1000) krunaldodiya  (1000)        0 2023-05-13 04:04:11.724230 fyers_token_manager_v2-0.0.8/
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)       11 2022-10-12 11:09:01.000000 fyers_token_manager_v2-0.0.8/LICENSE
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)     1120 2023-05-13 04:04:11.724230 fyers_token_manager_v2-0.0.8/PKG-INFO
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)      786 2023-05-10 05:26:39.000000 fyers_token_manager_v2-0.0.8/README.md
+drwxrwxr-x   0 krunaldodiya  (1000) krunaldodiya  (1000)        0 2023-05-13 04:04:11.724230 fyers_token_manager_v2-0.0.8/fyers_token_manager_v2/
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)     4806 2023-05-12 00:50:04.000000 fyers_token_manager_v2-0.0.8/fyers_token_manager_v2/__init__.py
+drwxrwxr-x   0 krunaldodiya  (1000) krunaldodiya  (1000)        0 2023-05-13 04:04:11.724230 fyers_token_manager_v2-0.0.8/fyers_token_manager_v2.egg-info/
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)     1120 2023-05-13 04:04:11.000000 fyers_token_manager_v2-0.0.8/fyers_token_manager_v2.egg-info/PKG-INFO
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)      290 2023-05-13 04:04:11.000000 fyers_token_manager_v2-0.0.8/fyers_token_manager_v2.egg-info/SOURCES.txt
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)        1 2023-05-13 04:04:11.000000 fyers_token_manager_v2-0.0.8/fyers_token_manager_v2.egg-info/dependency_links.txt
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)       15 2023-05-13 04:04:11.000000 fyers_token_manager_v2-0.0.8/fyers_token_manager_v2.egg-info/requires.txt
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)       23 2023-05-13 04:04:11.000000 fyers_token_manager_v2-0.0.8/fyers_token_manager_v2.egg-info/top_level.txt
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)       38 2023-05-13 04:04:11.724230 fyers_token_manager_v2-0.0.8/setup.cfg
+-rw-rw-r--   0 krunaldodiya  (1000) krunaldodiya  (1000)      682 2023-05-12 00:58:49.000000 fyers_token_manager_v2-0.0.8/setup.py
```

### Comparing `fyers_token_manager_v2-0.0.7/PKG-INFO` & `fyers_token_manager_v2-0.0.8/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fyers_token_manager_v2
-Version: 0.0.7
+Version: 0.0.8
 Summary: Fyers Token Manager
 Home-page: https://github.com/krunaldodiya/fyers_token_manager
 Author: Krunal Dodiya
 Author-email: kunal.dodiya1@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
```

### Comparing `fyers_token_manager_v2-0.0.7/README.md` & `fyers_token_manager_v2-0.0.8/README.md`

 * *Files identical despite different names*

### Comparing `fyers_token_manager_v2-0.0.7/fyers_token_manager_v2/__init__.py` & `fyers_token_manager_v2-0.0.8/fyers_token_manager_v2/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -3,78 +3,82 @@
 import pyotp
 import requests
 import pathlib
 
 from datetime import datetime
 from urllib.parse import parse_qs, urlparse
 
-current_directory = os.path.dirname(os.path.realpath(__file__))
-
-data_path = pathlib.Path(f"{current_directory}/data")
-logs_path = pathlib.Path(f"{current_directory}/logs")
-
 
 class FyersTokenManager:
     def __init__(self, config, accessToken, fyersModel, ws):
         self.username = config["username"]
         self.totp_key = config["totp_key"]
         self.pin = config["pin"]
         self.client_id = config["client_id"]
         self.secret_key = config["secret_key"]
         self.redirect_uri = config["redirect_uri"]
 
         self.__accessToken = accessToken
         self.__fyersModel = fyersModel
         self.__ws = ws
 
+        self.__data_path = None
+        self.__logs_path = None
+        self.__access_token_file_name = None
+
         self.__set_access_token_file_name()
         self.__initialize()
 
     def __set_access_token_file_name(self):
-        if not data_path.exists():
-            data_path.mkdir()
+        current_directory = os.path.dirname(os.path.realpath(__file__))
 
-        if not logs_path.exists():
-            logs_path.mkdir()
+        self.__data_path = pathlib.Path(f"{current_directory}/data/{self.username}")
+        self.__logs_path = pathlib.Path(f"{current_directory}/logs")
 
-        today = datetime.now().strftime("%Y-%m-%d")
+        if not self.__data_path.exists():
+            self.__data_path.mkdir(parents=True, exist_ok=True)
 
-        data_file = f"{today}-{self.username}"
+        if not self.__logs_path.exists():
+            self.__logs_path.mkdir()
 
-        self.access_token_file_name = os.path.join(data_path, data_file)
+        self.__access_token_file_name = os.path.join(
+            self.__data_path, datetime.now().strftime("%Y-%m-%d")
+        )
 
     def __set_initial_values(self, token):
         self.http_access_token = token
 
         self.ws_access_token = f"{self.client_id}:{self.http_access_token}"
 
         self.http_client = self.__fyersModel.FyersModel(
-            client_id=self.client_id, token=token, log_path=logs_path
+            client_id=self.client_id, token=token, log_path=self.__logs_path
         )
 
         self.ws_client = self.__ws.FyersSocket(
-            access_token=self.ws_access_token, run_background=False, log_path=logs_path
+            access_token=self.ws_access_token,
+            run_background=False,
+            log_path=self.__logs_path,
         )
 
     def __initialize(self):
         try:
             token = self.__read_file()
             self.__set_initial_values(token)
         except FileNotFoundError:
             token = self.__setup()
             self.__set_initial_values(token)
 
     def __read_file(self):
-        with open(f"{self.access_token_file_name}", "r") as f:
+        with open(f"{self.__access_token_file_name}", "r") as f:
             token = f.read()
 
         return token
 
     def __write_file(self, token):
-        with open(f"{self.access_token_file_name}", "w") as f:
+        with open(f"{self.__access_token_file_name}", "w") as f:
             f.write(token)
 
     def __get_token(self):
         headers = {
             "Accept": "application/json",
             "Accept-Language": "en-US,en;q=0.9",
             "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/112.0.0.0 Safari/537.36",
```

### Comparing `fyers_token_manager_v2-0.0.7/fyers_token_manager_v2.egg-info/PKG-INFO` & `fyers_token_manager_v2-0.0.8/fyers_token_manager_v2.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fyers-token-manager-v2
-Version: 0.0.7
+Version: 0.0.8
 Summary: Fyers Token Manager
 Home-page: https://github.com/krunaldodiya/fyers_token_manager
 Author: Krunal Dodiya
 Author-email: kunal.dodiya1@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
```

### Comparing `fyers_token_manager_v2-0.0.7/setup.py` & `fyers_token_manager_v2-0.0.8/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 with open("README.md", "r") as f:
     long_description = f.read()
 
 setuptools.setup(
     include_package_data=True,
     name="fyers_token_manager_v2",
-    version="0.0.7",
+    version="0.0.8",
     description="Fyers Token Manager",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/krunaldodiya/fyers_token_manager",
     author="Krunal Dodiya",
     author_email="kunal.dodiya1@gmail.com",
     packages=setuptools.find_packages(),
```

