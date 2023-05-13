# Comparing `tmp/aionotion-3.0.1.tar.gz` & `tmp/aionotion-3.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aionotion-3.0.1.tar", max compression
+gzip compressed data, was "aionotion-3.0.2.tar", max compression
```

## Comparing `aionotion-3.0.1.tar` & `aionotion-3.0.2.tar`

### file list

```diff
@@ -1,13 +1,13 @@
--rw-r--r--   0        0        0     1067 2021-02-26 21:48:31.043315 aionotion-3.0.1/LICENSE
--rw-r--r--   0        0        0     5829 2021-02-26 21:48:31.043315 aionotion-3.0.1/README.md
--rw-r--r--   0        0        0       81 2021-02-26 21:48:31.043315 aionotion-3.0.1/aionotion/__init__.py
--rw-r--r--   0        0        0     1714 2021-02-26 21:48:31.043315 aionotion-3.0.1/aionotion/bridge.py
--rw-r--r--   0        0        0     2743 2021-02-26 21:48:31.043315 aionotion-3.0.1/aionotion/client.py
--rw-r--r--   0        0        0     1084 2021-02-26 21:48:31.043315 aionotion-3.0.1/aionotion/device.py
--rw-r--r--   0        0        0      314 2021-02-26 21:48:31.043315 aionotion-3.0.1/aionotion/errors.py
--rw-r--r--   0        0        0     1362 2021-02-26 21:48:31.043315 aionotion-3.0.1/aionotion/sensor.py
--rw-r--r--   0        0        0     1373 2021-02-26 21:48:31.043315 aionotion-3.0.1/aionotion/system.py
--rw-r--r--   0        0        0     1683 2021-02-26 21:48:31.043315 aionotion-3.0.1/aionotion/task.py
--rw-r--r--   0        0        0     1451 2021-02-26 21:48:31.043315 aionotion-3.0.1/pyproject.toml
--rw-r--r--   0        0        0     6676 2021-02-26 21:48:39.588365 aionotion-3.0.1/setup.py
--rw-r--r--   0        0        0     6716 2021-02-26 21:48:39.588923 aionotion-3.0.1/PKG-INFO
+-rw-r--r--   0        0        0     1067 2021-07-22 17:14:10.686280 aionotion-3.0.2/LICENSE
+-rw-r--r--   0        0        0     5829 2021-07-22 17:14:10.686280 aionotion-3.0.2/README.md
+-rw-r--r--   0        0        0       81 2021-07-22 17:14:10.686280 aionotion-3.0.2/aionotion/__init__.py
+-rw-r--r--   0        0        0     1903 2021-07-22 17:14:10.686280 aionotion-3.0.2/aionotion/bridge.py
+-rw-r--r--   0        0        0     2782 2021-07-22 17:14:10.686280 aionotion-3.0.2/aionotion/client.py
+-rw-r--r--   0        0        0     1175 2021-07-22 17:14:10.686280 aionotion-3.0.2/aionotion/device.py
+-rw-r--r--   0        0        0      314 2021-07-22 17:14:10.686280 aionotion-3.0.2/aionotion/errors.py
+-rw-r--r--   0        0        0     1503 2021-07-22 17:14:10.686280 aionotion-3.0.2/aionotion/sensor.py
+-rw-r--r--   0        0        0     1514 2021-07-22 17:14:10.686280 aionotion-3.0.2/aionotion/system.py
+-rw-r--r--   0        0        0     1842 2021-07-22 17:14:10.686280 aionotion-3.0.2/aionotion/task.py
+-rw-r--r--   0        0        0     1959 2021-07-22 17:14:10.686280 aionotion-3.0.2/pyproject.toml
+-rw-r--r--   0        0        0     6676 2021-07-22 17:14:20.722788 aionotion-3.0.2/setup.py
+-rw-r--r--   0        0        0     6716 2021-07-22 17:14:20.723284 aionotion-3.0.2/PKG-INFO
```

### Comparing `aionotion-3.0.1/LICENSE` & `aionotion-3.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `aionotion-3.0.1/README.md` & `aionotion-3.0.2/README.md`

 * *Files identical despite different names*

### Comparing `aionotion-3.0.1/aionotion/bridge.py` & `aionotion-3.0.2/aionotion/bridge.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,43 +1,45 @@
 """Define endpoints for interacting with bridges."""
-from typing import Callable
+from typing import Any, Callable, Dict, List, cast
 
 
 class Bridge:  # pylint: disable=too-few-public-methods
     """Define an object to interact with all endpoints."""
 
     def __init__(self, request: Callable) -> None:
         """Initialize."""
-        self._request: Callable = request
+        self._request = request
 
-    async def async_all(self) -> list:
+    async def async_all(self) -> List[Dict[str, Any]]:
         """Get all bridges."""
-        resp: dict = await self._request("get", "base_stations")
-        return resp["base_stations"]
+        resp = await self._request("get", "base_stations")
+        return cast(List[Dict[str, Any]], resp["base_stations"])
 
-    async def async_create(self, attributes: dict) -> dict:
+    async def async_create(self, attributes: Dict[str, Any]) -> Dict[str, Any]:
         """Create a bridge with a specific attribute payload."""
-        resp: dict = await self._request(
+        resp = await self._request(
             "post", "base_stations", json={"base_stations": attributes}
         )
-        return resp["base_stations"]
+        return cast(Dict[str, Any], resp["base_stations"])
 
     async def async_delete(self, bridge_id: int) -> None:
         """Delete a bridge by ID."""
         await self._request("delete", f"base_stations/{bridge_id}")
 
-    async def async_get(self, bridge_id: int) -> dict:
+    async def async_get(self, bridge_id: int) -> Dict[str, Any]:
         """Get a bridge by ID."""
-        resp: dict = await self._request("get", f"base_stations/{bridge_id}")
-        return resp["base_stations"]
+        resp = await self._request("get", f"base_stations/{bridge_id}")
+        return cast(Dict[str, Any], resp["base_stations"])
 
-    async def async_reset(self, bridge_id: int) -> dict:
+    async def async_reset(self, bridge_id: int) -> Dict[str, Any]:
         """Reset a bridge (clear its wifi credentials) by ID."""
-        resp: dict = await self._request("put", f"base_stations/{bridge_id}/reset")
-        return resp["base_stations"]
+        resp = await self._request("put", f"base_stations/{bridge_id}/reset")
+        return cast(Dict[str, Any], resp["base_stations"])
 
-    async def async_update(self, bridge_id: int, new_attributes: dict) -> dict:
+    async def async_update(
+        self, bridge_id: int, new_attributes: Dict[str, Any]
+    ) -> Dict[str, Any]:
         """Update a bridge with a specific attribute payload."""
-        resp: dict = await self._request(
+        resp = await self._request(
             "put", f"base_stations/{bridge_id}", json={"base_stations": new_attributes}
         )
-        return resp["base_stations"]
+        return cast(Dict[str, Any], resp["base_stations"])
```

### Comparing `aionotion-3.0.1/aionotion/client.py` & `aionotion-3.0.2/aionotion/client.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 """Define a base client for interacting with Notion."""
-from typing import Optional
+from typing import Any, Dict, Optional
 
 from aiohttp import ClientSession, ClientTimeout
 from aiohttp.client_exceptions import ClientError
 
 from .bridge import Bridge
 from .device import Device
 from .errors import InvalidCredentialsError, RequestError
@@ -17,54 +17,61 @@
 
 
 class Client:  # pylint: disable=too-few-public-methods
     """Define the API object."""
 
     def __init__(self, *, session: Optional[ClientSession] = None) -> None:
         """Initialize."""
-        self._session: ClientSession = session
+        self._session: Optional[ClientSession] = session
         self._token: Optional[str] = None
 
-        self.bridge: Bridge = Bridge(self._request)
-        self.device: Device = Device(self._request)
-        self.sensor: Sensor = Sensor(self._request)
-        self.system: System = System(self._request)
-        self.task: Task = Task(self._request)
-
-    async def _request(self, method: str, endpoint: str, **kwargs) -> dict:
-        """Make a request the API.com."""
+        self.bridge = Bridge(self._request)
+        self.device = Device(self._request)
+        self.sensor = Sensor(self._request)
+        self.system = System(self._request)
+        self.task = Task(self._request)
+
+    async def _request(
+        self, method: str, endpoint: str, **kwargs: Dict[str, Any]
+    ) -> Dict[str, Any]:
+        """Make an API request."""
         url: str = f"{API_BASE}/{endpoint}"
 
         kwargs.setdefault("headers", {})
         if self._token:
             kwargs["headers"]["Authorization"] = f"Token token={self._token}"
 
         use_running_session = self._session and not self._session.closed
 
         if use_running_session:
             session = self._session
         else:
             session = ClientSession(timeout=ClientTimeout(total=DEFAULT_TIMEOUT))
 
+        assert session
+
+        data: Dict[str, Any] = {}
+
         try:
             async with session.request(method, url, **kwargs) as resp:
-                data: dict = await resp.json(content_type=None)
+                data = await resp.json()
                 resp.raise_for_status()
-                return data
         except ClientError as err:
             if "401" in str(err):
                 raise InvalidCredentialsError("Invalid credentials") from err
             raise RequestError(data["errors"][0]["title"]) from err
         finally:
             if not use_running_session:
                 await session.close()
 
+        return data
+
     async def async_authenticate(self, email: str, password: str) -> None:
         """Authenticate the user and retrieve an authentication token."""
-        auth_response: dict = await self._request(
+        auth_response = await self._request(
             "post",
             "users/sign_in",
             json={"sessions": {"email": email, "password": password}},
         )
 
         self._token = auth_response["session"]["authentication_token"]
```

### Comparing `aionotion-3.0.1/aionotion/device.py` & `aionotion-3.0.2/aionotion/device.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,31 +1,29 @@
 """Define endpoints for interacting with devices (phones, etc. with Notion)."""
-from typing import Callable
+from typing import Any, Callable, Dict, List, cast
 
 
 class Device:
     """Define an object to interact with all endpoints."""
 
     def __init__(self, request: Callable) -> None:
         """Initialize."""
-        self._request: Callable = request
+        self._request = request
 
-    async def async_all(self) -> list:
+    async def async_all(self) -> List[Dict[str, Any]]:
         """Get all devices."""
-        resp: dict = await self._request("get", "devices")
-        return resp["devices"]
+        resp = await self._request("get", "devices")
+        return cast(List[Dict[str, Any]], resp["devices"])
 
-    async def async_create(self, attributes: dict) -> dict:
+    async def async_create(self, attributes: Dict[str, Any]) -> Dict[str, Any]:
         """Create a device with a specific attribute payload."""
-        resp: dict = await self._request(
-            "post", "devices", json={"devices": attributes}
-        )
-        return resp["devices"]
+        resp = await self._request("post", "devices", json={"devices": attributes})
+        return cast(Dict[str, Any], resp["devices"])
 
     async def async_delete(self, device_id: int) -> None:
         """Delete a device by ID."""
         await self._request("delete", f"devices/{device_id}")
 
-    async def async_get(self, device_id: int) -> dict:
+    async def async_get(self, device_id: int) -> Dict[str, Any]:
         """Get a device by ID."""
-        resp: dict = await self._request("get", f"devices/{device_id}")
-        return resp["devices"]
+        resp = await self._request("get", f"devices/{device_id}")
+        return cast(Dict[str, Any], resp["devices"])
```

### Comparing `aionotion-3.0.1/aionotion/system.py` & `aionotion-3.0.2/aionotion/system.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,38 +1,38 @@
 """Define endpoints for interacting with systems (accounts)."""
-from typing import Callable
+from typing import Any, Callable, Dict, List, cast
 
 
 class System:
     """Define an object to interact with all endpoints."""
 
     def __init__(self, request: Callable) -> None:
         """Initialize."""
-        self._request: Callable = request
+        self._request = request
 
-    async def async_all(self) -> list:
+    async def async_all(self) -> List[Dict[str, Any]]:
         """Get all systems."""
-        resp: dict = await self._request("get", "systems")
-        return resp["systems"]
+        resp = await self._request("get", "systems")
+        return cast(List[Dict[str, Any]], resp["systems"])
 
-    async def async_create(self, attributes: dict) -> dict:
+    async def async_create(self, attributes: Dict[str, Any]) -> Dict[str, Any]:
         """Create a system with a specific attribute payload."""
-        resp: dict = await self._request(
-            "post", "systems", json={"systems": attributes}
-        )
-        return resp["systems"]
+        resp = await self._request("post", "systems", json={"systems": attributes})
+        return cast(Dict[str, Any], resp["systems"])
 
     async def async_delete(self, system_id: int) -> None:
         """Delete a system by ID."""
         await self._request("delete", f"systems/{system_id}")
 
-    async def async_get(self, system_id: int) -> dict:
+    async def async_get(self, system_id: int) -> Dict[str, Any]:
         """Get a system by ID."""
-        resp: dict = await self._request("get", f"systems/{system_id}")
-        return resp["systems"]
+        resp = await self._request("get", f"systems/{system_id}")
+        return cast(Dict[str, Any], resp["systems"])
 
-    async def async_update(self, system_id: int, new_attributes: dict) -> dict:
+    async def async_update(
+        self, system_id: int, new_attributes: Dict[str, Any]
+    ) -> Dict[str, Any]:
         """Update a system with a specific attribute payload."""
-        resp: dict = await self._request(
+        resp = await self._request(
             "put", f"systems/{system_id}", json={"systems": new_attributes}
         )
-        return resp["systems"]
+        return cast(Dict[str, Any], resp["systems"])
```

### Comparing `aionotion-3.0.1/pyproject.toml` & `aionotion-3.0.2/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -13,17 +13,37 @@
 known_first_party = "aionotion,examples,tests"
 line_length = 88
 multi_line_output = 3
 not_skip = "__init__.py"
 sections = "FUTURE,STDLIB,INBETWEENS,THIRDPARTY,FIRSTPARTY,LOCALFOLDER"
 use_parentheses = true
 
+[tool.mypy]
+check_untyped_defs = true
+disallow_incomplete_defs = true
+disallow_subclassing_any = true
+disallow_untyped_calls = true
+disallow_untyped_decorators = true
+disallow_untyped_defs = true
+follow_imports = "silent"
+ignore_missing_imports = true
+no_implicit_optional = true
+python_version = "3.8"
+show_error_codes = true
+strict_equality = true
+warn_incomplete_stub = true
+warn_redundant_casts = true
+warn_return_any = true
+warn_unreachable = true
+warn_unused_configs = true
+warn_unused_ignores = true
+
 [tool.poetry]
 name = "aionotion"
-version = "3.0.1"
+version = "3.0.2"
 description = "A simple Python 3 library for Notion Home Monitoring"
 readme = "README.md"
 authors = ["Aaron Bach <bachya1208@gmail.com>"]
 license = "MIT"
 repository = "https://github.com/bachya/aionotion"
 classifiers = [
     "License :: OSI Approved :: MIT License",
```

### Comparing `aionotion-3.0.1/setup.py` & `aionotion-3.0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 {'': ['*']}
 
 install_requires = \
 ['aiohttp>=3.7.4,<4.0.0']
 
 setup_kwargs = {
     'name': 'aionotion',
-    'version': '3.0.1',
+    'version': '3.0.2',
     'description': 'A simple Python 3 library for Notion Home Monitoring',
     'long_description': '# 📟 aionotion: a Python3, asyncio-friendly library for Notion® Home Monitoring\n\n[![CI](https://github.com/bachya/aionotion/workflows/CI/badge.svg)](https://github.com/bachya/aionotion/actions)\n[![PyPi](https://img.shields.io/pypi/v/aionotion.svg)](https://pypi.python.org/pypi/aionotion)\n[![Version](https://img.shields.io/pypi/pyversions/aionotion.svg)](https://pypi.python.org/pypi/aionotion)\n[![License](https://img.shields.io/pypi/l/aionotion.svg)](https://github.com/bachya/aionotion/blob/master/LICENSE)\n[![Code Coverage](https://codecov.io/gh/bachya/aionotion/branch/master/graph/badge.svg)](https://codecov.io/gh/bachya/aionotion)\n[![Maintainability](https://api.codeclimate.com/v1/badges/bd79edca07c8e4529cba/maintainability)](https://codeclimate.com/github/bachya/aionotion/maintainability)\n[![Say Thanks](https://img.shields.io/badge/SayThanks-!-1EAEDB.svg)](https://saythanks.io/to/bachya)\n\n`aionotion` is a Python 3, asyncio-friendly library for interacting with\n[Notion](https://getnotion.com) home monitoring sensors.\n\n# Python Versions\n\n`aionotion` is currently supported on:\n\n* Python 3.6\n* Python 3.7\n* Python 3.8\n* Python 3.9\n\n# Installation\n\n```python\npip install aionotion\n```\n\n# Usage\n\n```python\nimport asyncio\n\nfrom aiohttp import ClientSession\n\nfrom aionotion import async_get_client\n\n\nasync def main() -> None:\n    """Create the aiohttp session and run the example."""\n    client = await async_get_client("<EMAIL>", "<PASSWORD>", session=session)\n\n    # Get all "households" associated with the account:\n    systems = await client.system.async_all()\n\n    # Get a system by ID:\n    system = await client.system.async_get(12345)\n\n    # Create a system (with associated parameters):\n    await client.system.async_create({"system_id": 12345, "name": "Test"})\n\n    # Update a system with new parameters:\n    await client.system.async_update(12345, {"name": "Test"})\n\n    # Delete a system by ID:\n    await client.system.async_delete(12345)\n\n    # Get all bridges associated with the account:\n    bridges = await client.bridge.async_all()\n\n    # Get a bridge by ID:\n    bridge = await client.bridge.async_get(12345)\n\n    # Create a bridge (with associated parameters):\n    await client.bridge.async_create({"system_id": 12345, "name": "Test"})\n\n    # Update a bridge with new parameters:\n    await client.bridge.async_update(12345, {"name": "Test"})\n\n    # Reset a bridge (deprovision its WiFi credentials):\n    await client.bridge.async_reset(12345)\n\n    # Delete a bridge by ID:\n    await client.bridge.async_delete(12345)\n\n    # Get all devices associated with the account:\n    devices = await client.device.async_all()\n\n    # Get a device by ID:\n    device = await client.device.async_get(12345)\n\n    # Create a device (with associated parameters):\n    await client.device.async_create({"id": 12345})\n\n    # Delete a device by ID:\n    await client.device.async_delete(12345)\n\n    # Get all sensors:\n    sensors = await client.sensor.async_all()\n\n    # Get a sensor by ID:\n    sensor = await client.sensor.async_get(12345)\n\n    # Create a sensor (with associated parameters):\n    await client.sensor.async_create({"sensor_id": 12345, "name": "Test"})\n\n    # Update a sensor with new parameters:\n    await client.sensor.async_update(12345, {"name": "Test"})\n\n    # Delete a sensor by ID:\n    await client.sensor.async_delete(12345)\n\n    # Get all "tasks" (conditions monitored by sensors) associated with the account:\n    tasks = await client.task.async_all()\n\n    # Get a task by ID:\n    task = await client.task.async_get("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")\n\n    # Get a task\'s value history between two datetimes:\n    import datetime\n\n    history = await client.task.async_history(\n        "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",\n        data_before=datetime.datetime.now(),\n        data_after=datetime.datetime.now() - datetime.timedelta(days=3),\n    )\n\n    # Create a list of tasks for a particular sensor (e.g., sensor # 12345):\n    await client.task.async_create(\n        12345, [{"id": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "type": "missing"}]\n    )\n\n    # Delete a task for a particular sensor (e.g., sensor # 12345):\n    await client.task.async_delete(12345, "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")\n\n\nasyncio.run(main())\n```\n\nBy default, the library creates a new connection to Notion with each coroutine. If you\nare calling a large number of coroutines (or merely want to squeeze out every second of\nruntime savings possible), an\n[`aiohttp`](https://github.com/aio-libs/aiohttp) `ClientSession` can be used for connection\npooling:\n\n```python\nimport asyncio\n\nfrom aiohttp import ClientSession\n\nfrom aionotion import async_get_client\n\n\nasync def main() -> None:\n    """Create the aiohttp session and run the example."""\n    async with ClientSession() as session:\n        # Create a Notion API client:\n        client = await async_get_client("<EMAIL>", "<PASSWORD>", session=session)\n\n        # Get to work...\n\n\nasyncio.run(main())\n```\n\nCheck out the examples, the tests, and the source files themselves for method\nsignatures and more examples.\n\n# Contributing\n\n1. [Check for open features/bugs](https://github.com/bachya/aionotion/issues)\n  or [initiate a discussion on one](https://github.com/bachya/aionotion/issues/new).\n2. [Fork the repository](https://github.com/bachya/aionotion/fork).\n3. (_optional, but highly recommended_) Create a virtual environment: `python3 -m venv .venv`\n4. (_optional, but highly recommended_) Enter the virtual environment: `source ./venv/bin/activate`\n5. Install the dev environment: `script/setup`\n6. Code your new feature or bug fix.\n7. Write tests that cover your new functionality.\n8. Run tests and ensure 100% code coverage: `script/test`\n9. Update `README.md` with any new documentation.\n10. Add yourself to `AUTHORS.md`.\n11. Submit a pull request!\n',
     'author': 'Aaron Bach',
     'author_email': 'bachya1208@gmail.com',
     'maintainer': None,
     'maintainer_email': None,
     'url': 'https://github.com/bachya/aionotion',
```

### Comparing `aionotion-3.0.1/PKG-INFO` & `aionotion-3.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aionotion
-Version: 3.0.1
+Version: 3.0.2
 Summary: A simple Python 3 library for Notion Home Monitoring
 Home-page: https://github.com/bachya/aionotion
 License: MIT
 Author: Aaron Bach
 Author-email: bachya1208@gmail.com
 Requires-Python: >=3.6.0,<4.0.0
 Classifier: License :: OSI Approved :: MIT License
```

