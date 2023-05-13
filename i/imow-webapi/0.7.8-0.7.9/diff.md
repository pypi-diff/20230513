# Comparing `tmp/imow-webapi-0.7.8.tar.gz` & `tmp/imow-webapi-0.7.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "imow-webapi-0.7.8.tar", last modified: Sun Mar  6 11:36:40 2022, max compression
+gzip compressed data, was "imow-webapi-0.7.9.tar", last modified: Sat May 13 09:52:58 2023, max compression
```

## Comparing `imow-webapi-0.7.8.tar` & `imow-webapi-0.7.9.tar`

### file list

```diff
@@ -1,26 +1,29 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-06 11:36:40.670834 imow-webapi-0.7.8/
--rw-r--r--   0 runner    (1001) docker     (121)     1101 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)    12550 2022-03-06 11:36:40.670834 imow-webapi-0.7.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     6507 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-06 11:36:40.666834 imow-webapi-0.7.8/imow/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-06 11:36:40.666834 imow-webapi-0.7.8/imow/api/
--rw-r--r--   0 runner    (1001) docker     (121)    21511 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/imow/api/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-06 11:36:40.670834 imow-webapi-0.7.8/imow/common/
--rw-r--r--   0 runner    (1001) docker     (121)        9 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/imow/common/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      151 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/imow/common/actions.py
--rw-r--r--   0 runner    (1001) docker     (121)       93 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/imow/common/consts.py
--rw-r--r--   0 runner    (1001) docker     (121)      188 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/imow/common/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (121)    44227 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/imow/common/messages.py
--rw-r--r--   0 runner    (1001) docker     (121)     6458 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/imow/common/mowerstate.py
--rw-r--r--   0 runner    (1001) docker     (121)       82 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/imow/common/package_descriptions.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-06 11:36:40.670834 imow-webapi-0.7.8/imow_webapi.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)    12550 2022-03-06 11:36:40.000000 imow-webapi-0.7.8/imow_webapi.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      518 2022-03-06 11:36:40.000000 imow-webapi-0.7.8/imow_webapi.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-03-06 11:36:40.000000 imow-webapi-0.7.8/imow_webapi.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       44 2022-03-06 11:36:40.000000 imow-webapi-0.7.8/imow_webapi.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (121)        5 2022-03-06 11:36:40.000000 imow-webapi-0.7.8/imow_webapi.egg-info/namespace_packages.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-03-06 11:36:38.000000 imow-webapi-0.7.8/imow_webapi.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (121)       69 2022-03-06 11:36:40.000000 imow-webapi-0.7.8/imow_webapi.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)        5 2022-03-06 11:36:40.000000 imow-webapi-0.7.8/imow_webapi.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-03-06 11:36:40.670834 imow-webapi-0.7.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     2027 2022-03-06 11:36:19.000000 imow-webapi-0.7.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:52:58.347703 imow-webapi-0.7.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1101 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    12626 2023-05-13 09:52:58.347703 imow-webapi-0.7.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     6507 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:52:58.343703 imow-webapi-0.7.9/imow/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:52:58.343703 imow-webapi-0.7.9/imow/api/
+-rw-r--r--   0 runner    (1001) docker     (123)    21429 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/imow/api/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:52:58.343703 imow-webapi-0.7.9/imow/common/
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/imow/common/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      151 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/imow/common/actions.py
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/imow/common/consts.py
+-rw-r--r--   0 runner    (1001) docker     (123)      188 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/imow/common/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44227 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/imow/common/messages.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6456 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/imow/common/mowerstate.py
+-rw-r--r--   0 runner    (1001) docker     (123)       82 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/imow/common/package_descriptions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:52:58.347703 imow-webapi-0.7.9/imow_webapi.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    12626 2023-05-13 09:52:58.000000 imow-webapi-0.7.9/imow_webapi.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-05-13 09:52:58.000000 imow-webapi-0.7.9/imow_webapi.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 09:52:58.000000 imow-webapi-0.7.9/imow_webapi.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 09:52:58.000000 imow-webapi-0.7.9/imow_webapi.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 09:52:58.000000 imow-webapi-0.7.9/imow_webapi.egg-info/namespace_packages.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 09:52:57.000000 imow-webapi-0.7.9/imow_webapi.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 09:52:58.000000 imow-webapi-0.7.9/imow_webapi.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 09:52:58.000000 imow-webapi-0.7.9/imow_webapi.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 09:52:58.347703 imow-webapi-0.7.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2077 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:52:58.347703 imow-webapi-0.7.9/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     6291 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/tests/test_integration_imow.py
+-rw-r--r--   0 runner    (1001) docker     (123)      490 2023-05-13 09:52:39.000000 imow-webapi-0.7.9/tests/test_unit_imow.py
```

### Comparing `imow-webapi-0.7.8/LICENSE` & `imow-webapi-0.7.9/LICENSE`

 * *Files identical despite different names*

### Comparing `imow-webapi-0.7.8/PKG-INFO` & `imow-webapi-0.7.9/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 Metadata-Version: 2.1
 Name: imow-webapi
-Version: 0.7.8
+Version: 0.7.9
 Summary: A library to authenticate and interact with STIHL iMow mowers using their WebAPI
 Home-page: https://github.com/ChrisHaPunkt/stihl-imow-webapi
 Author: ChrisHaPunkt
 License: GPL
 Keywords: stihl imow mower api
-Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # STIHL iMow unofficial Python API wrapper
 
 [![PyPI version shields.io](https://img.shields.io/pypi/v/imow-webapi)](https://pypi.python.org/pypi/imow-webapi/)
 [![Docs on GitHub pages](https://img.shields.io/badge/docs-GitHub%20Pages-blue)](hhttps://chrishapunkt.github.io/stihl-imow-webapi/imow)
@@ -192,14 +192,16 @@
 * https://github.com/OpenXbox/xbox-webapi-python
 
 for repo structure inspiration
 
 
 # Changelog
 
+## Version 0.7.9 (2023-05-13)
+- remove unnecessary http_session closes
 ## Version 0.7.8 (2022-03-06)
 - Implement a logout function `ImowAPI.api_logout()`. Use within re-authentication
 ## Version 0.7.7 (2022-03-06)
 - Use more `async with`s
 ## Version 0.7.6 (2022-03-05)
 
 ### Dependency updates
@@ -221,52 +223,52 @@
 ```
 ### Features
 - Possibility to update a specific settings for a mower like gpsProtection on/off
 ## Version 0.7.0 (2021-06-30)
 ### Breaking Changes
 - `IMowApi.intent` Parameter `mower_action_id` is renamed to `mower_external_id` to match the upstream api expectation.
 ### Features
-- If an `api_request` is intended, and the used `access_token` expires in less than one day, it's automatically renewed. 
-  
+- If an `api_request` is intended, and the used `access_token` expires in less than one day, it's automatically renewed.
+
 ## Version 0.6.0 (2021-06-28)
 - ```python
   mower.machineError = 'M1120',
   mower.machineState = 'HOOD_BLOCKED',
   mower.stateMessage: dict = {
-      'short': 'Hood blocked', 
-      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).', 
-      'legacyMessage': 'Abschaltung Automatikmode durch Bumper', 
-      'errorId': 'M1120', 
+      'short': 'Hood blocked',
+      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).',
+      'legacyMessage': 'Abschaltung Automatikmode durch Bumper',
+      'errorId': 'M1120',
       'error': True
   }
   ```
-  
+
 ### Breaking Changes
 - Migrated all own MowerState attributes to camelCase to match the upstream attributes style.
   ```
   - MowerState.stateMessage = None
   - MowerState.machineError = None
   - MowerState.machineState = None
   ```
 ## Version 0.5.2 (2021-06-15)
 
 ## Bugfixes
-- Also quote password string in auth request to support more special chars 
+- Also quote password string in auth request to support more special chars
 
 ## Version 0.5.1 (2021-06-13)
 
 ## Features
 - ```python
   mower.machine_error = 'M1120',
   mower.machine_state = 'HOOD_BLOCKED',
   mower.state_message: dict = {
-      'short': 'Hood blocked', 
-      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).', 
-      'legacyMessage': 'Abschaltung Automatikmode durch Bumper', 
-      'errorId': 'M1120', 
+      'short': 'Hood blocked',
+      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).',
+      'legacyMessage': 'Abschaltung Automatikmode durch Bumper',
+      'errorId': 'M1120',
       'error': True
   }
   ```
   Provide a machine usable string from the short message in english
 
 ## Version 0.5.0 (2021-06-12)
 
@@ -277,34 +279,34 @@
   property and is now longer an ``async`` method.
 
 ### Features
 
 - ```python
   mower.state_message -> dict
   {
-      'short': 'Hood blocked', 
-      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).', 
-      'errorId': 'M1120', 
+      'short': 'Hood blocked',
+      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).',
+      'errorId': 'M1120',
       'error': True
   }
   ```
   The MowerState Class now provides a ```state_message``` property which gives a ``short`` and``long`` text for
   description (Besides an error indication and errorId). All error and status codes are now dynamically matched and
-  human readable available.  
+  human readable available.
   **This makes the ``MowerTask`` obsolete and it is removed with this release.**
-- ``api = IMowApi(lang="en")``  
-  The imow api can now be instanced with a language code (fallback to ``en``).   
+- ``api = IMowApi(lang="en")``
+  The imow api can now be instanced with a language code (fallback to ``en``).
   The ``state_message`` property displays the messages in the corresponding language.
 
 ## Version 0.4.5 (2021-06-01)
 
 ### Features
 
 - Add 2 new identified Tasks within `MowerTask` (Thanks to @lausser)
-- Add `check_api_maintenance()` method to `IMowAPI` Class. Check if the api server is currently under maintenance.  
+- Add `check_api_maintenance()` method to `IMowAPI` Class. Check if the api server is currently under maintenance.
   This method is automatically called if the api server returns a 500 error response for any request.
 - One should call the new `close()` method for the `IMowAPI` Class when finishing the api interactions to correctly
   close the http session.
 
 ### Bugfixes
 
 - [Issue #8](https://github.com/ChrisHaPunkt/stihl-imow-webapi/issues/8) - Example not working
@@ -351,9 +353,7 @@
 ### Bugfixes
 
 - Return a valid error message and raise if provided login credentials are wrong
 
 ## Version 0.2.2 (2021-05-00)
 
 - Initial release
-
-
```

### Comparing `imow-webapi-0.7.8/README.md` & `imow-webapi-0.7.9/README.md`

 * *Files identical despite different names*

### Comparing `imow-webapi-0.7.8/imow/api/__init__.py` & `imow-webapi-0.7.9/imow/api/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -49,15 +49,14 @@
         self,
         email: str = None,
         password: str = None,
         token: str = None,
         aiohttp_session: ClientSession = None,
         lang: str = "en",
     ) -> None:
-
         self.http_session: ClientSession = aiohttp_session
         self.csrf_token: str = ""
         self.requestId: str = ""
         self.access_token: str = token
         self.token_expires: datetime = None
         self.api_email: str = email
         self.api_password: str = password
@@ -67,30 +66,28 @@
 
     async def close(self):
         """Cleanup the aiohttp Session"""
         await asyncio.sleep(0.250)
         await self.http_session.close()
 
     async def check_api_maintenance(self) -> None:
-
         url = "https://app-api-maintenance-r-euwe-4bf2d8.azurewebsites.net/maintenance/"
 
         headers = {
             "Authorization": "",
         }
         response = await self.api_request(url, "GET", headers=headers)
         status = json.loads(await response.text())
         logger.debug(status)
         if status["serverDisrupted"] or status["serverDown"]:
             msg = (
                 f"iMow API is under Maintenance -> "
                 f'serverDisrupted: {status["serverDisrupted"]}, serverDown: {status["serverDown"]}, '
                 f'affectedTill {status["affectedTill"]}'
             )
-            await self.http_session.close()
             raise ApiMaintenanceError(msg)
 
     async def get_token(
         self,
         email: str = "",
         password: str = "",
         force_reauth=False,
@@ -102,15 +99,14 @@
         :param email: stihl webapp login email non-url-encoded
         :param password: stihl webapp login password
         :param force_reauth: Force a re-authentication with username and password
         :return: tuple, the access token and a datetime object containing the expire date
         """
 
         if not self.access_token or force_reauth:
-
             if email and password:
                 self.api_password = password
                 self.api_email = email
             if force_reauth:
                 await self.api_logout()
                 self.csrf_token = ""
                 self.requestId = ""
@@ -250,15 +246,14 @@
                     i18n_user = json.loads(await response_user.text())
                     self.messages_user = Messages(i18n_user)
             else:
                 self.messages_user = self.messages_en
 
         except ClientResponseError as e:
             if e.status == 404:
-                await self.close()
                 raise LanguageNotFoundError(
                     f"Language-File '{self.lang}.json' not found on imow upstream ("
                     f"https://app.imow.stihl.com/assets/i18n/animations/{self.lang}.json)"
                 )
 
     async def api_request(
         self, url, method, payload=None, headers=None
```

### Comparing `imow-webapi-0.7.8/imow/common/messages.py` & `imow-webapi-0.7.9/imow/common/messages.py`

 * *Files identical despite different names*

### Comparing `imow-webapi-0.7.8/imow/common/mowerstate.py` & `imow-webapi-0.7.9/imow/common/mowerstate.py`

 * *Files 1% similar despite different names*

```diff
@@ -30,30 +30,28 @@
 
     async def update_setting(self, setting, new_value):
         await self.imow.update_setting(
             mower_id=self.id, setting=setting, new_value=new_value
         )
 
     def update_state_messages(self):
-
         if self.status["mainState"] != self.ERROR_MAINSTATE_CODE:
             (
                 self.stateMessage["short"],
                 self.stateMessage["long"],
             ) = self.imow.messages_user.get_status_message(
                 short_code=self.status["mainState"]
             )
 
             # Reset error indication
             self.stateMessage["error"] = False
             self.machineError = None
             self.stateMessage["errorId"] = ""
 
         else:
-
             (
                 self.stateMessage["short"],
                 self.stateMessage["long"],
                 self.stateMessage["errorId"],
                 self.stateMessage["legacyMessage"],
             ) = self.imow.messages_user.get_error_message(
                 short_code=self.status["extraStatus"]
```

### Comparing `imow-webapi-0.7.8/imow_webapi.egg-info/PKG-INFO` & `imow-webapi-0.7.9/imow_webapi.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 Metadata-Version: 2.1
 Name: imow-webapi
-Version: 0.7.8
+Version: 0.7.9
 Summary: A library to authenticate and interact with STIHL iMow mowers using their WebAPI
 Home-page: https://github.com/ChrisHaPunkt/stihl-imow-webapi
 Author: ChrisHaPunkt
 License: GPL
 Keywords: stihl imow mower api
-Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # STIHL iMow unofficial Python API wrapper
 
 [![PyPI version shields.io](https://img.shields.io/pypi/v/imow-webapi)](https://pypi.python.org/pypi/imow-webapi/)
 [![Docs on GitHub pages](https://img.shields.io/badge/docs-GitHub%20Pages-blue)](hhttps://chrishapunkt.github.io/stihl-imow-webapi/imow)
@@ -192,14 +192,16 @@
 * https://github.com/OpenXbox/xbox-webapi-python
 
 for repo structure inspiration
 
 
 # Changelog
 
+## Version 0.7.9 (2023-05-13)
+- remove unnecessary http_session closes
 ## Version 0.7.8 (2022-03-06)
 - Implement a logout function `ImowAPI.api_logout()`. Use within re-authentication
 ## Version 0.7.7 (2022-03-06)
 - Use more `async with`s
 ## Version 0.7.6 (2022-03-05)
 
 ### Dependency updates
@@ -221,52 +223,52 @@
 ```
 ### Features
 - Possibility to update a specific settings for a mower like gpsProtection on/off
 ## Version 0.7.0 (2021-06-30)
 ### Breaking Changes
 - `IMowApi.intent` Parameter `mower_action_id` is renamed to `mower_external_id` to match the upstream api expectation.
 ### Features
-- If an `api_request` is intended, and the used `access_token` expires in less than one day, it's automatically renewed. 
-  
+- If an `api_request` is intended, and the used `access_token` expires in less than one day, it's automatically renewed.
+
 ## Version 0.6.0 (2021-06-28)
 - ```python
   mower.machineError = 'M1120',
   mower.machineState = 'HOOD_BLOCKED',
   mower.stateMessage: dict = {
-      'short': 'Hood blocked', 
-      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).', 
-      'legacyMessage': 'Abschaltung Automatikmode durch Bumper', 
-      'errorId': 'M1120', 
+      'short': 'Hood blocked',
+      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).',
+      'legacyMessage': 'Abschaltung Automatikmode durch Bumper',
+      'errorId': 'M1120',
       'error': True
   }
   ```
-  
+
 ### Breaking Changes
 - Migrated all own MowerState attributes to camelCase to match the upstream attributes style.
   ```
   - MowerState.stateMessage = None
   - MowerState.machineError = None
   - MowerState.machineState = None
   ```
 ## Version 0.5.2 (2021-06-15)
 
 ## Bugfixes
-- Also quote password string in auth request to support more special chars 
+- Also quote password string in auth request to support more special chars
 
 ## Version 0.5.1 (2021-06-13)
 
 ## Features
 - ```python
   mower.machine_error = 'M1120',
   mower.machine_state = 'HOOD_BLOCKED',
   mower.state_message: dict = {
-      'short': 'Hood blocked', 
-      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).', 
-      'legacyMessage': 'Abschaltung Automatikmode durch Bumper', 
-      'errorId': 'M1120', 
+      'short': 'Hood blocked',
+      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).',
+      'legacyMessage': 'Abschaltung Automatikmode durch Bumper',
+      'errorId': 'M1120',
       'error': True
   }
   ```
   Provide a machine usable string from the short message in english
 
 ## Version 0.5.0 (2021-06-12)
 
@@ -277,34 +279,34 @@
   property and is now longer an ``async`` method.
 
 ### Features
 
 - ```python
   mower.state_message -> dict
   {
-      'short': 'Hood blocked', 
-      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).', 
-      'errorId': 'M1120', 
+      'short': 'Hood blocked',
+      'long': 'The hood is blocked. Please check the hood and press the OK button on your machine (M1120).',
+      'errorId': 'M1120',
       'error': True
   }
   ```
   The MowerState Class now provides a ```state_message``` property which gives a ``short`` and``long`` text for
   description (Besides an error indication and errorId). All error and status codes are now dynamically matched and
-  human readable available.  
+  human readable available.
   **This makes the ``MowerTask`` obsolete and it is removed with this release.**
-- ``api = IMowApi(lang="en")``  
-  The imow api can now be instanced with a language code (fallback to ``en``).   
+- ``api = IMowApi(lang="en")``
+  The imow api can now be instanced with a language code (fallback to ``en``).
   The ``state_message`` property displays the messages in the corresponding language.
 
 ## Version 0.4.5 (2021-06-01)
 
 ### Features
 
 - Add 2 new identified Tasks within `MowerTask` (Thanks to @lausser)
-- Add `check_api_maintenance()` method to `IMowAPI` Class. Check if the api server is currently under maintenance.  
+- Add `check_api_maintenance()` method to `IMowAPI` Class. Check if the api server is currently under maintenance.
   This method is automatically called if the api server returns a 500 error response for any request.
 - One should call the new `close()` method for the `IMowAPI` Class when finishing the api interactions to correctly
   close the http session.
 
 ### Bugfixes
 
 - [Issue #8](https://github.com/ChrisHaPunkt/stihl-imow-webapi/issues/8) - Example not working
@@ -351,9 +353,7 @@
 ### Bugfixes
 
 - Return a valid error message and raise if provided login credentials are wrong
 
 ## Version 0.2.2 (2021-05-00)
 
 - Initial release
-
-
```

### Comparing `imow-webapi-0.7.8/imow_webapi.egg-info/SOURCES.txt` & `imow-webapi-0.7.9/imow_webapi.egg-info/SOURCES.txt`

 * *Files 6% similar despite different names*

```diff
@@ -12,8 +12,10 @@
 imow_webapi.egg-info/PKG-INFO
 imow_webapi.egg-info/SOURCES.txt
 imow_webapi.egg-info/dependency_links.txt
 imow_webapi.egg-info/entry_points.txt
 imow_webapi.egg-info/namespace_packages.txt
 imow_webapi.egg-info/not-zip-safe
 imow_webapi.egg-info/requires.txt
-imow_webapi.egg-info/top_level.txt
+imow_webapi.egg-info/top_level.txt
+tests/test_integration_imow.py
+tests/test_unit_imow.py
```

### Comparing `imow-webapi-0.7.8/setup.py` & `imow-webapi-0.7.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -29,14 +29,15 @@
         "Intended Audience :: Developers",
         "License :: OSI Approved :: MIT License",
         "Topic :: Software Development :: Libraries :: Python Modules",
         "Programming Language :: Python :: 3",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
         "Programming Language :: Python :: 3.9",
+        "Programming Language :: Python :: 3.10",
     ],
     test_suite="tests",
     install_requires=packages,
     setup_requires=["pytest-runner"],
     entry_points={
         'console_scripts': ['%s=%s.__init__:main' % (package_name, package_name)]
     },
```

