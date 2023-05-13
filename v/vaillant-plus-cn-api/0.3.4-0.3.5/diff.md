# Comparing `tmp/vaillant_plus_cn_api-0.3.4.tar.gz` & `tmp/vaillant_plus_cn_api-0.3.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vaillant_plus_cn_api-0.3.4.tar", max compression
+gzip compressed data, was "vaillant_plus_cn_api-0.3.5.tar", max compression
```

## Comparing `vaillant_plus_cn_api-0.3.4.tar` & `vaillant_plus_cn_api-0.3.5.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0    35149 2022-12-03 10:22:28.002890 vaillant_plus_cn_api-0.3.4/LICENSE
--rw-r--r--   0        0        0      134 2022-12-03 10:22:28.003137 vaillant_plus_cn_api-0.3.4/README.md
--rw-r--r--   0        0        0      818 2023-03-02 14:40:33.313247 vaillant_plus_cn_api-0.3.4/pyproject.toml
--rw-r--r--   0        0        0      688 2023-01-29 13:38:56.236894 vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/__init__.py
--rw-r--r--   0        0        0     6268 2023-01-31 12:40:42.795949 vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/api.py
--rw-r--r--   0        0        0      912 2023-01-28 15:55:08.227661 vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/const.py
--rw-r--r--   0        0        0      942 2023-01-29 13:40:36.878398 vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/errors.py
--rw-r--r--   0        0        0     1638 2023-01-28 14:33:09.442589 vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/model.py
--rw-r--r--   0        0        0    11598 2023-01-30 14:18:05.742261 vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/websocket.py
--rw-r--r--   0        0        0      875 1970-01-01 00:00:00.000000 vaillant_plus_cn_api-0.3.4/setup.py
--rw-r--r--   0        0        0      714 1970-01-01 00:00:00.000000 vaillant_plus_cn_api-0.3.4/PKG-INFO
+-rw-r--r--   0        0        0    11356 2023-03-03 14:15:28.695483 vaillant_plus_cn_api-0.3.5/LICENSE
+-rw-r--r--   0        0        0      134 2022-12-03 10:22:28.003137 vaillant_plus_cn_api-0.3.5/README.md
+-rw-r--r--   0        0        0      818 2023-05-13 13:59:45.802446 vaillant_plus_cn_api-0.3.5/pyproject.toml
+-rw-r--r--   0        0        0      688 2023-01-29 13:38:56.236894 vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/__init__.py
+-rw-r--r--   0        0        0     6268 2023-01-31 12:40:42.795949 vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/api.py
+-rw-r--r--   0        0        0      912 2023-01-28 15:55:08.227661 vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/const.py
+-rw-r--r--   0        0        0      942 2023-01-29 13:40:36.878398 vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/errors.py
+-rw-r--r--   0        0        0     1638 2023-01-28 14:33:09.442589 vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/model.py
+-rw-r--r--   0        0        0    11650 2023-05-13 13:59:36.471401 vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/websocket.py
+-rw-r--r--   0        0        0      875 1970-01-01 00:00:00.000000 vaillant_plus_cn_api-0.3.5/setup.py
+-rw-r--r--   0        0        0      714 1970-01-01 00:00:00.000000 vaillant_plus_cn_api-0.3.5/PKG-INFO
```

### Comparing `vaillant_plus_cn_api-0.3.4/pyproject.toml` & `vaillant_plus_cn_api-0.3.5/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "vaillant-plus-cn-api"
-version = "0.3.4"
+version = "0.3.5"
 description = "Python package for interacting with Vaillant devices sold in China mainland using API"
 authors = ["daxingplay <daxingplay@gmail.com>"]
 readme = "README.md"
 packages = [{include = "vaillant_plus_cn_api"}]
 homepage = "https://github.com/daxingplay/vaillant-plus-cn-api"
 
 [tool.poetry.dependencies]
```

### Comparing `vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/__init__.py` & `vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/__init__.py`

 * *Files identical despite different names*

### Comparing `vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/api.py` & `vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/api.py`

 * *Files identical despite different names*

### Comparing `vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/const.py` & `vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/const.py`

 * *Files identical despite different names*

### Comparing `vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/errors.py` & `vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/errors.py`

 * *Files identical despite different names*

### Comparing `vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/model.py` & `vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/model.py`

 * *Files identical despite different names*

### Comparing `vaillant_plus_cn_api-0.3.4/vaillant_plus_cn_api/websocket.py` & `vaillant_plus_cn_api-0.3.5/vaillant_plus_cn_api/websocket.py`

 * *Files 2% similar despite different names*

```diff
@@ -137,39 +137,38 @@
                         "token": self._token.token,
                         "p0_type": "attrs_v4",
                         "heartbeat_interval": 180,
                         "auto_subscribe": False,
                     },
                 })
 
-                login_ret = await ws_client.receive_json()
-                if login_ret["cmd"] != "login_res" or login_ret["data"]["success"] is not True:
-                    self._logger.error("login failed")
-                    self._state = STATE_STOPPED
-                    raise InvalidTokenError
-
-                await ws_client.send_json({"cmd": "subscribe_req", "data": [{"did": self._device.id}]})
-                await ws_client.send_json({"cmd": "c2s_read", "data": {"did": self._device.id}})
-
-                self._state = STATE_CONNECTED
-
-                await self._watchdog.trigger()
-
                 async for message in ws_client:
                     if self.state == STATE_STOPPED:
                         break
 
                     if message.type == aiohttp.WSMsgType.TEXT:
                         msg: dict = message.json()
                         cmd = msg.get("cmd", "")
                         data = msg.get("data", {})
 
                         self._logger.debug("Recv: %s", message)
 
-                        if cmd == "s2c_noti":
+                        if cmd == "login_res":
+                            if data["success"] is not True:
+                                self._logger.error("login failed. ret: %s", data)
+                                self._state = STATE_STOPPED
+                                raise InvalidTokenError
+
+                            await ws_client.send_json({"cmd": "subscribe_req", "data": [{"did": self._device.id}]})
+                            await ws_client.send_json({"cmd": "c2s_read", "data": {"did": self._device.id}})
+
+                            self._state = STATE_CONNECTED
+
+                            await self._watchdog.trigger()
+                        elif cmd == "s2c_noti":
                             if data["did"] == self._device.id:
                                 device_attrs = data["attrs"]
                                 self._logger.debug(
                                     "Recv atrrs for device %s => %s", data["did"], device_attrs)
                                 if self.state != STATE_SUBSCRIBED:
                                     if self._async_on_subscribe_handler is not None:
                                         await self._async_on_subscribe_handler(device_attrs)
```

### Comparing `vaillant_plus_cn_api-0.3.4/setup.py` & `vaillant_plus_cn_api-0.3.5/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 {'': ['*']}
 
 install_requires = \
 ['aiohttp>=3.8.0,<4.0.0']
 
 setup_kwargs = {
     'name': 'vaillant-plus-cn-api',
-    'version': '0.3.4',
+    'version': '0.3.5',
     'description': 'Python package for interacting with Vaillant devices sold in China mainland using API',
     'long_description': '# vaillant-plus-cn-api\nPython package for interacting with Vaillant devices sold in China mainland through APIs in Vaillant plus app.\n',
     'author': 'daxingplay',
     'author_email': 'daxingplay@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/daxingplay/vaillant-plus-cn-api',
```

### Comparing `vaillant_plus_cn_api-0.3.4/PKG-INFO` & `vaillant_plus_cn_api-0.3.5/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vaillant-plus-cn-api
-Version: 0.3.4
+Version: 0.3.5
 Summary: Python package for interacting with Vaillant devices sold in China mainland using API
 Home-page: https://github.com/daxingplay/vaillant-plus-cn-api
 Author: daxingplay
 Author-email: daxingplay@gmail.com
 Requires-Python: >=3.9
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
```

