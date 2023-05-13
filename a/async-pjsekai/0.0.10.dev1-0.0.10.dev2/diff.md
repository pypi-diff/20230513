# Comparing `tmp/async_pjsekai-0.0.10.dev1.tar.gz` & `tmp/async_pjsekai-0.0.10.dev2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "async_pjsekai-0.0.10.dev1.tar", max compression
+gzip compressed data, was "async_pjsekai-0.0.10.dev2.tar", max compression
```

## Comparing `async_pjsekai-0.0.10.dev1.tar` & `async_pjsekai-0.0.10.dev2.tar`

### file list

```diff
@@ -1,21 +1,21 @@
--rw-r--r--   0        0        0      679 2023-04-30 12:42:40.730476 async_pjsekai-0.0.10.dev1/README.md
--rw-r--r--   0        0        0    25762 2023-05-04 16:57:48.864214 async_pjsekai-0.0.10.dev1/async_pjsekai/api.py
--rw-r--r--   0        0        0     2711 2023-05-04 15:51:11.814207 async_pjsekai-0.0.10.dev1/async_pjsekai/asset.py
--rw-r--r--   0        0        0     1133 2023-04-18 05:14:42.794216 async_pjsekai-0.0.10.dev1/async_pjsekai/asset_bundle.py
--rw-r--r--   0        0        0    38661 2023-05-04 17:04:41.634214 async_pjsekai-0.0.10.dev1/async_pjsekai/client.py
--rw-r--r--   0        0        0    23209 2023-05-04 16:57:48.834214 async_pjsekai-0.0.10.dev1/async_pjsekai/enums/enums.py
--rw-r--r--   0        0        0      577 2023-05-04 16:57:48.494214 async_pjsekai-0.0.10.dev1/async_pjsekai/enums/information.py
--rw-r--r--   0        0        0     2433 2023-05-04 16:57:48.534214 async_pjsekai-0.0.10.dev1/async_pjsekai/enums/platform.py
--rw-r--r--   0        0        0     1593 2023-05-04 16:57:48.514214 async_pjsekai-0.0.10.dev1/async_pjsekai/enums/tutorial_status.py
--rw-r--r--   0        0        0      847 2023-05-04 16:57:48.504214 async_pjsekai-0.0.10.dev1/async_pjsekai/enums/unknown.py
--rw-r--r--   0        0        0     2205 2023-05-04 16:57:48.534214 async_pjsekai-0.0.10.dev1/async_pjsekai/exceptions.py
--rw-r--r--   0        0        0     5914 2023-05-04 16:57:48.614214 async_pjsekai-0.0.10.dev1/async_pjsekai/live.py
--rw-r--r--   0        0        0     1159 2023-05-04 16:48:32.164213 async_pjsekai-0.0.10.dev1/async_pjsekai/models/asset_bundle_info.py
--rw-r--r--   0        0        0     2921 2023-05-04 16:57:48.564214 async_pjsekai-0.0.10.dev1/async_pjsekai/models/converters.py
--rw-r--r--   0        0        0      680 2023-05-04 16:57:48.524214 async_pjsekai-0.0.10.dev1/async_pjsekai/models/game_version.py
--rw-r--r--   0        0        0     1232 2023-05-04 16:57:48.544214 async_pjsekai-0.0.10.dev1/async_pjsekai/models/information.py
--rw-r--r--   0        0        0   111626 2023-05-04 16:57:50.874214 async_pjsekai-0.0.10.dev1/async_pjsekai/models/master_data.py
--rw-r--r--   0        0        0     1106 2023-05-04 16:48:32.164213 async_pjsekai-0.0.10.dev1/async_pjsekai/models/system_info.py
--rw-r--r--   0        0        0     2023 2023-05-04 16:57:48.574214 async_pjsekai-0.0.10.dev1/async_pjsekai/utilities.py
--rw-r--r--   0        0        0      896 2023-05-04 17:10:31.814215 async_pjsekai-0.0.10.dev1/pyproject.toml
--rw-r--r--   0        0        0     1911 1970-01-01 00:00:00.000000 async_pjsekai-0.0.10.dev1/PKG-INFO
+-rw-r--r--   0        0        0      679 2023-04-30 12:42:40.730476 async_pjsekai-0.0.10.dev2/README.md
+-rw-r--r--   0        0        0    25762 2023-05-06 11:40:48.479444 async_pjsekai-0.0.10.dev2/async_pjsekai/api.py
+-rw-r--r--   0        0        0     5499 2023-05-13 08:12:37.955186 async_pjsekai-0.0.10.dev2/async_pjsekai/asset.py
+-rw-r--r--   0        0        0     1133 2023-04-18 05:14:42.794216 async_pjsekai-0.0.10.dev2/async_pjsekai/asset_bundle.py
+-rw-r--r--   0        0        0    47703 2023-05-13 08:12:44.115186 async_pjsekai-0.0.10.dev2/async_pjsekai/client.py
+-rw-r--r--   0        0        0    23209 2023-05-04 16:57:48.834214 async_pjsekai-0.0.10.dev2/async_pjsekai/enums/enums.py
+-rw-r--r--   0        0        0      577 2023-05-04 16:57:48.494214 async_pjsekai-0.0.10.dev2/async_pjsekai/enums/information.py
+-rw-r--r--   0        0        0     2433 2023-05-04 16:57:48.534214 async_pjsekai-0.0.10.dev2/async_pjsekai/enums/platform.py
+-rw-r--r--   0        0        0     1593 2023-05-04 16:57:48.514214 async_pjsekai-0.0.10.dev2/async_pjsekai/enums/tutorial_status.py
+-rw-r--r--   0        0        0      847 2023-05-04 16:57:48.504214 async_pjsekai-0.0.10.dev2/async_pjsekai/enums/unknown.py
+-rw-r--r--   0        0        0     2205 2023-05-04 16:57:48.534214 async_pjsekai-0.0.10.dev2/async_pjsekai/exceptions.py
+-rw-r--r--   0        0        0     5914 2023-05-04 16:57:48.614214 async_pjsekai-0.0.10.dev2/async_pjsekai/live.py
+-rw-r--r--   0        0        0     1159 2023-05-04 16:48:32.164213 async_pjsekai-0.0.10.dev2/async_pjsekai/models/asset_bundle_info.py
+-rw-r--r--   0        0        0     2921 2023-05-04 16:57:48.564214 async_pjsekai-0.0.10.dev2/async_pjsekai/models/converters.py
+-rw-r--r--   0        0        0      680 2023-05-04 16:57:48.524214 async_pjsekai-0.0.10.dev2/async_pjsekai/models/game_version.py
+-rw-r--r--   0        0        0     1232 2023-05-04 16:57:48.544214 async_pjsekai-0.0.10.dev2/async_pjsekai/models/information.py
+-rw-r--r--   0        0        0   111626 2023-05-04 16:57:50.874214 async_pjsekai-0.0.10.dev2/async_pjsekai/models/master_data.py
+-rw-r--r--   0        0        0     1106 2023-05-04 16:48:32.164213 async_pjsekai-0.0.10.dev2/async_pjsekai/models/system_info.py
+-rw-r--r--   0        0        0     2023 2023-05-06 11:40:41.739444 async_pjsekai-0.0.10.dev2/async_pjsekai/utilities.py
+-rw-r--r--   0        0        0      917 2023-05-13 08:20:59.035174 async_pjsekai-0.0.10.dev2/pyproject.toml
+-rw-r--r--   0        0        0     1954 1970-01-01 00:00:00.000000 async_pjsekai-0.0.10.dev2/PKG-INFO
```

### Comparing `async_pjsekai-0.0.10.dev1/README.md` & `async_pjsekai-0.0.10.dev2/README.md`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/api.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/api.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/asset_bundle.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/asset_bundle.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/client.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/client.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,23 +1,26 @@
 # SPDX-FileCopyrightText: 2022-2023 Erik Chan <erikchan002@gmail.com>
 # SPDX-FileCopyrightText: 2023-present TheerapakG <theerapakg@gmail.com>
 #
 # SPDX-License-Identifier: MIT
 
+import aiofiles
+import aiofiles.os
+from aiohttp.abc import AbstractCookieJar
 from asyncio.locks import Lock
 from contextlib import asynccontextmanager
 import dataclasses
 from functools import wraps
-from typing import AsyncIterator, Coroutine, Callable, Optional, TypeVar, Union
+import logging
+from types import TracebackType
+from typing import AsyncIterator, Coroutine, Callable, Optional, Type, TypeVar, Union
 from typing_extensions import ParamSpec, Concatenate
-from json import load, dump, JSONDecodeError
+from json import loads, dumps, JSONDecodeError
 from pathlib import Path
 
-from aiohttp.abc import AbstractCookieJar
-
 from async_pjsekai.enums.tutorial_status import TutorialStatus, Unit
 from async_pjsekai.models.master_data import MasterData
 from async_pjsekai.models.system_info import SystemInfo, AppVersionStatus
 from async_pjsekai.models.game_version import GameVersion
 from async_pjsekai.models.information import Information
 from async_pjsekai.api import API, Platform
 from async_pjsekai.asset import Asset
@@ -36,14 +39,313 @@
 
 from .models.converters import msgpack_converter
 
 P = ParamSpec("P")
 R = TypeVar("R")
 
 
+log = logging.getLogger(__name__)
+
+
+class SystemInfoMutex:
+    _lock: Lock
+    _system_info: SystemInfo
+    _system_info_file_path: Optional[Path]
+
+    def __init__(self, system_info_file_path: Optional[Path]) -> None:
+        self._lock = Lock()
+        self._system_info = SystemInfo().create()
+        self._system_info_file_path = system_info_file_path
+
+    @property
+    def system_info_file_path(self):
+        return self._system_info_file_path
+
+    async def __aenter__(self):
+        await self._lock.acquire()
+        return self._system_info
+
+    async def __aexit__(
+        self,
+        exc_type: Optional[Type[BaseException]],
+        exc_val: Optional[BaseException],
+        exc_tb: Optional[TracebackType],
+    ):
+        self._lock.release()
+
+    async def _loads(
+        self,
+        data: bytes,
+        app_version: Optional[str] = None,
+        app_hash: Optional[str] = None,
+        multi_play_version: Optional[str] = None,
+    ):
+        del self._system_info
+        await self._set_value(msgpack_converter.loads(data, SystemInfo))
+        if app_version is not None and app_hash is not None:
+            await self._replace_value(
+                app_version=app_version,
+                app_hash=app_hash,
+                multi_play_version=multi_play_version,
+            )
+
+    @asynccontextmanager
+    async def loads(
+        self,
+        data: bytes,
+        app_version: Optional[str] = None,
+        app_hash: Optional[str] = None,
+        multi_play_version: Optional[str] = None,
+    ):
+        async with self._lock:
+            await self._loads(data, app_version, app_hash, multi_play_version)
+            yield self._system_info
+
+    async def _loads_coro(
+        self,
+        data: Coroutine[None, None, bytes],
+        app_version: Optional[str] = None,
+        app_hash: Optional[str] = None,
+        multi_play_version: Optional[str] = None,
+    ):
+        self._system_info = SystemInfo().create()
+        await self._set_value(msgpack_converter.loads(await data, SystemInfo))
+        if app_version is not None and app_hash is not None:
+            await self._replace_value(
+                app_version=app_version,
+                app_hash=app_hash,
+                multi_play_version=multi_play_version,
+            )
+
+    @asynccontextmanager
+    async def loads_coro(
+        self,
+        data: Coroutine[None, None, bytes],
+        app_version: Optional[str] = None,
+        app_hash: Optional[str] = None,
+        multi_play_version: Optional[str] = None,
+    ):
+        async with self._lock:
+            await self._loads_coro(data, app_version, app_hash, multi_play_version)
+            yield self._system_info
+
+    async def load(
+        self,
+        app_version: Optional[str] = None,
+        app_hash: Optional[str] = None,
+        multi_play_version: Optional[str] = None,
+    ):
+        async with self._lock:
+            if self.system_info_file_path is not None:
+                try:
+                    async with aiofiles.open(self.system_info_file_path, "rb") as f:
+                        await self._loads_coro(f.read())
+                except FileNotFoundError:
+                    await self._set_value(SystemInfo.create())
+            else:
+                await self._set_value(SystemInfo.create())
+
+            if app_version is not None and app_hash is not None:
+                await self._replace_value(
+                    app_version=app_version,
+                    app_hash=app_hash,
+                    multi_play_version=multi_play_version,
+                )
+
+    async def _write(self):
+        if self.system_info_file_path is not None:
+            await aiofiles.os.makedirs(self.system_info_file_path.parent, exist_ok=True)
+            temp_path = self.system_info_file_path.with_suffix(
+                self.system_info_file_path.suffix + ".tmp"
+            )
+            async with aiofiles.open(temp_path, "wb") as f:
+                await f.write(msgpack_converter.dumps(self._system_info, SystemInfo))
+            await aiofiles.os.replace(temp_path, self.system_info_file_path)
+
+    async def _set_value(self, new_value: SystemInfo):
+        self._system_info = new_value
+        log.info(
+            f"system version: app: {new_value.app_version} multi play: {new_value.multi_play_version} data: {new_value.data_version} asset: {new_value.asset_version}"
+        )
+        await self._write()
+
+    async def set_value(self, new_value: SystemInfo):
+        async with self._lock:
+            await self._set_value(new_value)
+
+    async def _replace_value(self, **changes):
+        self._system_info = dataclasses.replace(self._system_info, **changes)
+        log.info(
+            f"system version: app: {self._system_info.app_version} multi play: {self._system_info.multi_play_version} data: {self._system_info.data_version} asset: {self._system_info.asset_version}"
+        )
+        await self._write()
+        return self._system_info
+
+    @asynccontextmanager
+    async def replace_value(self, **changes):
+        async with self._lock:
+            yield await self._replace_value(**changes)
+
+
+class MasterDataMutex:
+    _lock: Lock
+    _sync: bool
+    _master_data: MasterData
+    _master_data_file_path: Optional[Path]
+
+    def __init__(self, master_data_file_path: Optional[Path]) -> None:
+        self._lock = Lock()
+        self._sync = False
+        self._master_data = MasterData().create()
+        self._master_data_file_path = master_data_file_path
+
+    @property
+    def sync(self):
+        return self._sync
+
+    @property
+    def master_data(self):
+        return self._master_data
+
+    @property
+    def master_data_file_path(self):
+        return self._master_data_file_path
+
+    async def __aenter__(self):
+        await self._lock.acquire()
+        return self._master_data, self._sync
+
+    async def __aexit__(
+        self,
+        exc_type: Optional[Type[BaseException]],
+        exc_val: Optional[BaseException],
+        exc_tb: Optional[TracebackType],
+    ):
+        self._lock.release()
+
+    async def _loads(self, data: bytes, write=True):
+        await self._set_value(MasterData.create(), write=False)
+        await self._set_value(msgpack_converter.loads(data, MasterData), write=write)
+
+    @asynccontextmanager
+    async def loads(self, data: bytes, write=True):
+        async with self._lock:
+            await self._loads(data, write=write)
+            yield self._master_data
+
+    async def _loads_coro(self, data: Coroutine[None, None, bytes], write=True):
+        await self._set_value(MasterData.create(), write=False)
+        await self._set_value(
+            msgpack_converter.loads(await data, MasterData), write=write
+        )
+
+    @asynccontextmanager
+    async def loads_coro(self, data: Coroutine[None, None, bytes], write=True):
+        async with self._lock:
+            await self._loads_coro(data, write=write)
+            yield self._master_data
+
+    async def load(self):
+        async with self._lock:
+            if self.master_data_file_path is not None:
+                try:
+                    async with aiofiles.open(self.master_data_file_path, "rb") as f:
+                        await self._loads_coro(f.read(), write=False)
+                        self._sync = True
+                except FileNotFoundError:
+                    await self._set_value(MasterData.create())
+            else:
+                await self._set_value(MasterData.create())
+
+    async def _write(self):
+        if self.master_data_file_path is not None:
+            await aiofiles.os.makedirs(self.master_data_file_path.parent, exist_ok=True)
+            temp_path = self.master_data_file_path.with_suffix(
+                self.master_data_file_path.suffix + ".tmp"
+            )
+            async with aiofiles.open(temp_path, "wb") as f:
+                await f.write(msgpack_converter.dumps(self._master_data, MasterData))
+            await aiofiles.os.replace(temp_path, self.master_data_file_path)
+        self._sync = True
+
+    async def _set_value(self, new_value: MasterData, write=True):
+        self._sync = False
+        self._master_data = new_value
+        if write:
+            await self._write()
+
+    async def set_value(self, new_value: MasterData, write=True):
+        async with self._lock:
+            await self._set_value(new_value, write=write)
+
+
+class UserDataMutex:
+    _lock: Lock
+    _user_data: dict
+    _user_data_file_path: Optional[Path]
+
+    def __init__(self, user_data_file_path: Optional[Path]) -> None:
+        self._lock = Lock()
+        self._user_data = dict()
+        self._user_data_file_path = user_data_file_path
+
+    @property
+    def user_data_file_path(self):
+        return self._user_data_file_path
+
+    async def __aenter__(self):
+        await self._lock.acquire()
+        return self._user_data
+
+    async def __aexit__(
+        self,
+        exc_type: Optional[Type[BaseException]],
+        exc_val: Optional[BaseException],
+        exc_tb: Optional[TracebackType],
+    ):
+        self._lock.release()
+
+    async def load(self):
+        async with self._lock:
+            if self.user_data_file_path is not None:
+                try:
+                    async with aiofiles.open(self.user_data_file_path, "r") as f:
+                        await self._set_value(loads(await f.read()))
+                except (FileNotFoundError, JSONDecodeError):
+                    await self._set_value(dict())
+            else:
+                await self._set_value(dict())
+
+    async def _write(self):
+        if self.user_data_file_path is not None:
+            await aiofiles.os.makedirs(self.user_data_file_path.parent, exist_ok=True)
+            temp_path = self.user_data_file_path.with_suffix(
+                self.user_data_file_path.suffix + ".tmp"
+            )
+            async with aiofiles.open(temp_path, "w") as f:
+                await f.write(dumps(self._user_data, indent=2, ensure_ascii=False))
+            await aiofiles.os.replace(temp_path, self.user_data_file_path)
+
+    async def _set_value(self, new_value: dict):
+        self._user_data = new_value
+        await self._write()
+
+    async def set_value(self, new_value: dict):
+        async with self._lock:
+            await self._set_value(new_value)
+
+    async def _update_value(self, update: dict):
+        self._user_data = {**self._user_data, **update}
+        await self._write()
+
+    async def update_value(self, update: dict):
+        async with self._lock:
+            await self._update_value(update)
+
+
 class Client:
     def _auth_required(func: Callable[Concatenate["Client", P], R]) -> Callable[Concatenate["Client", P], R]:  # type: ignore[misc]
         @wraps(func)
         def wrapper_auth_required(
             self: "Client", *args: P.args, **kwargs: P.kwargs
         ) -> R:
             if not self.is_logged_in:
@@ -106,31 +408,25 @@
 
         return wrapper_auto_update
 
     hca_key: Optional[bytes]
     auto_session_refresh: bool
     auto_update: bool
 
-    _system_info_file_path: Optional[Path]
-
     @property
     def system_info_file_path(self) -> Optional[Path]:
-        return self._system_info_file_path
-
-    _master_data_file_path: Optional[Path]
+        return self._system_info.system_info_file_path
 
     @property
     def master_data_file_path(self) -> Optional[Path]:
-        return self._master_data_file_path
-
-    _user_data_file_path: Optional[Path]
+        return self._master_data.master_data_file_path
 
     @property
     def user_data_file_path(self) -> Optional[Path]:
-        return self._user_data_file_path
+        return self._user_data.user_data_file_path
 
     _asset_directory: Optional[Path]
 
     @property
     def asset_directory(self) -> Optional[Path]:
         return self._asset_directory
 
@@ -154,102 +450,115 @@
 
     _credential: Optional[str]
 
     @property
     def credential(self) -> Optional[str]:
         return self._credential
 
-    _system_info: SystemInfo
-    _system_info_lock: Lock
+    _system_info: SystemInfoMutex
 
     @property
     @asynccontextmanager
     async def system_info(self):
-        async with self._system_info_lock:
-            yield self._system_info
+        async with self._system_info as system_info:
+            yield system_info
 
-    @system_info.setter
-    def system_info(self, new_value: SystemInfo) -> None:
-        self._system_info = new_value
-        if self.system_info_file_path is not None:
-            self.system_info_file_path.parent.mkdir(parents=True, exist_ok=True)
-            with self.system_info_file_path.open("wb") as f:
-                f.write(msgpack_converter.dumps(new_value, SystemInfo))
+    @asynccontextmanager
+    async def loads_system_info(self, data: bytes):
+        async with self._system_info.loads(data) as system_info:
+            yield system_info
 
-    _master_data: MasterData
-    _master_data_lock: Lock
+    @asynccontextmanager
+    async def loads_coro_system_info(self, data: Coroutine[None, None, bytes]):
+        async with self._system_info.loads_coro(data) as system_info:
+            yield system_info
+
+    async def set_system_info(self, new_value: SystemInfo):
+        await self._system_info.set_value(new_value)
+
+    @asynccontextmanager
+    async def replace_system_info(self, **changes):
+        async with self._system_info.replace_value(**changes) as system_info:
+            yield system_info
+
+    _master_data: MasterDataMutex
 
     @property
     @asynccontextmanager
     async def master_data(self):
-        async with self._master_data_lock:
-            yield self._master_data
+        async with self._master_data as (master_data, sync):
+            yield master_data, sync
 
-    @master_data.setter
-    def master_data(self, new_value: MasterData) -> None:
-        self._master_data = new_value
-        if self.master_data_file_path is not None:
-            self.master_data_file_path.parent.mkdir(parents=True, exist_ok=True)
-            with self.master_data_file_path.open("wb") as f:
-                f.write(msgpack_converter.dumps(new_value, MasterData))
+    @asynccontextmanager
+    async def loads_master_data(self, data: bytes, write=True):
+        async with self._master_data.loads(data, write=write) as master_data:
+            yield master_data
 
-    _user_data: dict
-    _user_data_lock: Lock
+    @asynccontextmanager
+    async def loads_coro_master_data(
+        self, data: Coroutine[None, None, bytes], write=True
+    ):
+        async with self._master_data.loads_coro(data, write=write) as master_data:
+            yield master_data
+
+    async def set_master_data(self, new_value: MasterData, write=True):
+        await self._master_data.set_value(new_value, write=write)
+
+    _user_data: UserDataMutex
 
     @property
     @asynccontextmanager
     async def user_data(self):
-        async with self._user_data_lock:
-            yield self._user_data
+        async with self._user_data as user_data:
+            yield user_data
 
-    def _update_user_resources(self, response) -> dict:
-        self._user_data = {
-            **self._user_data,
-            **response["updatedResources"],
-        }
-        if self.user_data_file_path is not None:
-            self.user_data_file_path.parent.mkdir(parents=True, exist_ok=True)
-            with self.user_data_file_path.open("w") as f:
-                dump(self._user_data, f, indent=2, ensure_ascii=False)
+    async def set_user_data(self, new_value: dict):
+        await self._user_data.set_value(new_value)
+
+    async def _update_user_resources(self, response: dict) -> dict:
+        await self._user_data.update_value(response["updatedResources"])
         del response["updatedResources"]
         return response
 
     @property
     @asynccontextmanager
     async def now(self) -> AsyncIterator[Optional[int]]:
         async with self.user_data as user_data:
             yield user_data["now"]
 
     @property
+    @asynccontextmanager
     @_auth_required
     async def friends(self) -> AsyncIterator[Optional[list[dict]]]:
         async with self.user_data as user_data:
             if "userFriends" not in user_data:
                 yield None
             else:
                 yield [
                     friend
                     for friend in user_data["userFriends"]
                     if friend["friendStatus"] == "friend"
                 ]
 
     @property
+    @asynccontextmanager
     @_auth_required
     async def received_friend_requests(self) -> AsyncIterator[Optional[list[dict]]]:
         async with self.user_data as user_data:
             if "userFriends" not in user_data:
                 yield None
             else:
                 yield [
                     friend
                     for friend in user_data["userFriends"]
                     if friend["friendStatus"] == "pending_request"
                 ]
 
     @property
+    @asynccontextmanager
     @_auth_required
     async def sent_friend_requests(self) -> AsyncIterator[Optional[list[dict]]]:
         async with self.user_data as user_data:
             if "userFriends" not in user_data:
                 yield None
             else:
                 yield [
@@ -411,85 +720,42 @@
         auto_session_refresh: bool = True,
         auto_update: bool = False,
     ) -> None:
         self.hca_key = hca_key
         self.auto_session_refresh = auto_session_refresh
         self.auto_update = auto_update
 
-        self._system_info_file_path = None
-        self._master_data_file_path = None
-        self._user_data_file_path = None
+        _system_info_file_path = None
+        _master_data_file_path = None
+        _user_data_file_path = None
         self._asset_directory = None
         if system_info_file_path is not None:
-            self._system_info_file_path = Path(system_info_file_path)
+            _system_info_file_path = Path(system_info_file_path)
         if master_data_file_path is not None:
-            self._master_data_file_path = Path(master_data_file_path)
+            _master_data_file_path = Path(master_data_file_path)
         if user_data_file_path is not None:
-            self._user_data_file_path = Path(user_data_file_path)
+            _user_data_file_path = Path(user_data_file_path)
         if asset_directory is not None:
             self._asset_directory = Path(asset_directory)
         self._asset = None
 
-        self._system_info_lock = Lock()
-
-        if self.system_info_file_path is not None:
-            try:
-                with self.system_info_file_path.open("rb") as f:
-                    self._system_info = msgpack_converter.loads(f.read(), SystemInfo)
-            except FileNotFoundError:
-                self.system_info = SystemInfo.create()
-        else:
-            self.system_info = SystemInfo.create()
-        if app_version is not None and app_hash is not None:
-            self.system_info = dataclasses.replace(
-                self._system_info,
-                app_version=app_version,
-                app_hash=app_hash,
-                multi_play_version=multi_play_version,
-            )
-
-        self._master_data_lock = Lock()
-
-        if self.master_data_file_path is not None:
-            try:
-                with self.master_data_file_path.open("rb") as f:
-                    self._master_data = msgpack_converter.loads(f.read(), MasterData)
-            except FileNotFoundError:
-                self.master_data = MasterData.create()
-        else:
-            self.master_data = MasterData.create()
-
-        self._user_data_lock = Lock()
-
-        self._user_data = {}
-        if self.user_data_file_path is not None:
-            try:
-                with self.user_data_file_path.open("r") as f:
-                    self._user_data = load(f)
-            except (FileNotFoundError, JSONDecodeError):
-                with self.user_data_file_path.open("w") as f:
-                    dump(self.user_data, f, indent=2, ensure_ascii=False)
+        self._system_info = SystemInfoMutex(_system_info_file_path)
+        self._master_data = MasterDataMutex(_master_data_file_path)
+        self._user_data = UserDataMutex(_user_data_file_path)
 
         self._user_id = None
         self._credential = None
-        if (
-            self._system_info.asset_version is not None
-            and self._system_info.asset_hash is not None
-            and asset_directory is not None
-        ):
-            self._asset = Asset(
-                self._system_info.asset_version,
-                self._system_info.asset_hash,
-                asset_directory,
-            )
 
         self._platform = platform
         self._key = key
         self._iv = iv
         self._jwt_secret = jwt_secret
+        self._app_version = app_version
+        self._app_hash = app_hash
+        self._multi_play_version = multi_play_version
         self._api_domain = api_domain
         self._asset_bundle_domain = asset_bundle_domain
         self._asset_bundle_info_domain = asset_bundle_info_domain
         self._game_version_domain = game_version_domain
         self._signature_domain = signature_domain
         self._enable_api_encryption = enable_api_encryption
         self._enable_asset_bundle_encryption = enable_asset_bundle_encryption
@@ -497,39 +763,61 @@
         self._enable_game_version_encryption = enable_game_version_encryption
         self._enable_signature_encryption = enable_signature_encryption
         self._server_number = server_number
 
         self._update_all_on_init = update_all_on_init
 
     async def start(self):
-        self._api_manager = API(
-            platform=self._platform,
-            key=self._key,
-            iv=self._iv,
-            jwt_secret=self._jwt_secret,
-            system_info=self._system_info,
-            api_domain=self._api_domain or API.DEFAULT_API_DOMAIN,
-            asset_bundle_domain=self._asset_bundle_domain,
-            asset_bundle_info_domain=self._asset_bundle_info_domain,
-            game_version_domain=self._game_version_domain,
-            signature_domain=self._signature_domain,
-            enable_api_encryption=self._enable_api_encryption,
-            enable_asset_bundle_encryption=self._enable_asset_bundle_encryption,
-            enable_asset_bundle_info_encryption=self._enable_asset_bundle_info_encryption,
-            enable_game_version_encryption=self._enable_game_version_encryption,
-            enable_signature_encryption=self._enable_signature_encryption,
-            server_number=self._server_number,
-        )
+        await self._system_info.load()
+        await self._master_data.load()
+        await self._user_data.load()
+
+        update_app = False
+        async with self.system_info as system_info:
+            if system_info.app_version is None or system_info.app_hash is None:
+                update_app = True
+
+            if (
+                system_info.asset_version is not None
+                and system_info.asset_hash is not None
+                and self.asset_directory is not None
+            ):
+                self._asset = Asset(
+                    system_info.asset_version,
+                    system_info.asset_hash,
+                    self.asset_directory,
+                )
+
+                await self._asset.load()
+
+            self._api_manager = API(
+                platform=self._platform,
+                key=self._key,
+                iv=self._iv,
+                jwt_secret=self._jwt_secret,
+                system_info=system_info,
+                api_domain=self._api_domain or API.DEFAULT_API_DOMAIN,
+                asset_bundle_domain=self._asset_bundle_domain,
+                asset_bundle_info_domain=self._asset_bundle_info_domain,
+                game_version_domain=self._game_version_domain,
+                signature_domain=self._signature_domain,
+                enable_api_encryption=self._enable_api_encryption,
+                enable_asset_bundle_encryption=self._enable_asset_bundle_encryption,
+                enable_asset_bundle_info_encryption=self._enable_asset_bundle_info_encryption,
+                enable_game_version_encryption=self._enable_game_version_encryption,
+                enable_signature_encryption=self._enable_signature_encryption,
+                server_number=self._server_number,
+            )
 
         await self.refresh_signed_cookie()
 
         if self.api_manager.key is None or self.api_manager.iv is None:
             return
 
-        if self._system_info.app_version is None or self._system_info.app_hash is None:
+        if update_app:
             await self.update_app()
 
         self.game_version = msgpack_converter.loads(
             await self.api_manager.get_game_version_packed(), GameVersion
         )
         if self._api_domain is not None:
             self.api_domain = self._api_domain
@@ -538,28 +826,29 @@
                 self.api_domain = self.game_version.domain
             else:
                 self.api_domain = API.DEFAULT_API_DOMAIN
 
         if self._update_all_on_init:
             await self.update_all()
 
+        log.info("client is ready")
+
     async def close(self):
         await self.api_manager.close()
 
     @_auto_update
     @_auto_session_refresh
     async def register(self) -> dict:
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.register()
-            return self._update_user_resources(response)
+        response: dict = await self.api_manager.register()
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     async def login(self, user_id: Union[int, str], credential: str) -> dict:
-        async with self.system_info as system_info, self._user_data_lock:
+        async with self.system_info as system_info:
             response: dict = await self.api_manager.authenticate(user_id, credential)
             self._user_id = user_id
             self._credential = credential
 
             info: SystemInfo = msgpack_converter.structure(response, SystemInfo)
 
             if info.app_version_status is AppVersionStatus.MAINTENANCE:
@@ -594,26 +883,27 @@
                     raise AssetUpdateRequired(info.asset_version, info.asset_hash)
                 elif (
                     info.data_version is not None
                     and system_info.data_version != info.data_version
                 ):
                     raise DataUpdateRequired(info.data_version, info.app_version_status.value)  # type: ignore
 
-            self._user_data = await self.api_manager.get_user_data(user_id)
-            self._update_user_resources(await self.api_manager.get_login_bonus(user_id))
+            await self.set_user_data(await self.api_manager.get_user_data(user_id))
+            await self._update_user_resources(
+                await self.api_manager.get_login_bonus(user_id)
+            )
             return response
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def reload_user_data(self, name: Optional[str] = None) -> dict:
-        async with self._user_data_lock:
-            user_data = await self.api_manager.get_user_data(self.user_id, name)  # type: ignore[arg-type]
-            self._user_data = user_data
-            return user_data
+        user_data = await self.api_manager.get_user_data(self.user_id, name)  # type: ignore[arg-type]
+        await self.set_user_data(user_data)
+        return user_data
 
     @_auto_update
     @_auto_session_refresh
     async def check_version(self, bypass_availability: bool = False) -> SystemInfo:
         response: dict = await self.api_manager.get_system_info()
         app_versions: list[SystemInfo] = [
             app_version_info
@@ -630,20 +920,22 @@
                     app_version_info
                     for app_version_info in app_versions
                     if app_version_info.app_version == system_info.app_version
                 ]
                 if len(matching_app_version_info) > 0:
                     info: SystemInfo = matching_app_version_info[-1]
                     if info.system_profile != system_info.system_profile:
-                        self.system_info = SystemInfo(
-                            system_profile=info.system_profile,
-                            app_version=system_info.app_version,
-                            app_hash=system_info.app_hash,
-                            multi_play_version=system_info.multi_play_version,
-                            app_version_status=info.app_version_status,
+                        await self._system_info._set_value(
+                            SystemInfo(
+                                system_profile=info.system_profile,
+                                app_version=system_info.app_version,
+                                app_hash=system_info.app_hash,
+                                multi_play_version=system_info.multi_play_version,
+                                app_version_status=info.app_version_status,
+                            )
                         )
                     status: str = "" if info.app_version_status is None else info.app_version_status.value  # type: ignore
                     asset_update_required: bool = (
                         system_info.asset_version != info.asset_version
                         or self.asset is None
                         or self.asset.version != info.asset_version
                     )
@@ -705,53 +997,51 @@
             except (
                 ServerInMaintenance,
                 MultipleUpdatesRequired,
                 AssetUpdateRequired,
                 DataUpdateRequired,
             ):
                 return
-        async with self.system_info as system_info:
-            new_system_info = dataclasses.replace(
-                system_info,
-                app_version=app_version,
-                app_hash=app_hash,
-                multi_play_version=multi_play_version,
-            )
-            self.system_info = new_system_info
-            self.api_manager.system_info = new_system_info
+
+        async with self.replace_system_info(
+            app_version=app_version,
+            app_hash=app_hash,
+            multi_play_version=multi_play_version,
+        ) as system_info:
+            log.info(f"updated app: {app_version}")
+            self.api_manager.system_info = system_info
 
     @_auto_session_refresh
     async def update_data(self, data_version: str, app_version_status: str) -> None:
-        async with self._master_data_lock, self.system_info as system_info:
-            del self._master_data
-            response = await self.api_manager.get_master_data_packed(data_version)
-            self.master_data = msgpack_converter.loads(response, MasterData)
-            new_system_info = dataclasses.replace(
-                system_info,
-                data_version=data_version,
-                app_version_status=app_version_status,
-            )
-            self.system_info = new_system_info
-            self.api_manager.system_info = new_system_info
+        async with self.loads_coro_master_data(
+            self.api_manager.get_master_data_packed(data_version)
+        ):
+            pass
+
+        async with self.replace_system_info(
+            data_version=data_version,
+            app_version_status=app_version_status,
+        ) as system_info:
+            log.info(f"updated data: {data_version}")
+            self.api_manager.system_info = system_info
 
     @_auto_session_refresh
     async def update_asset(self, asset_version: str, asset_hash: str) -> None:
-        async with self.system_info as system_info:
-            if self.asset_directory is None:
-                self._asset = Asset(asset_version, asset_hash)
-            else:
-                self._asset = Asset(
-                    asset_version, asset_hash, str(self.asset_directory)
-                )
-            await self._asset.get_asset_bundle_info(self.api_manager)
-            new_system_info = dataclasses.replace(
-                system_info, asset_version=asset_version, asset_hash=asset_hash
-            )
-            self.system_info = new_system_info
-            self.api_manager.system_info = new_system_info
+        if self.asset_directory is None:
+            self._asset = Asset(asset_version, asset_hash)
+        else:
+            self._asset = Asset(asset_version, asset_hash, self.asset_directory)
+
+        async with self._asset.get_asset_bundle_info(
+            self.api_manager
+        ), self.replace_system_info(
+            asset_version=asset_version, asset_hash=asset_hash
+        ) as system_info:
+            log.info(f"updated asset: {asset_version}")
+            self.api_manager.system_info = system_info
 
     async def update_all(self) -> bool:
         try:
             await self.check_version()
         except AppUpdateRequired as e:
             await self.update_app(e.app_version, e.app_hash, e.multi_play_version)
             await self.update_all()
@@ -797,20 +1087,19 @@
             for information in (await self.api_manager.get_notices())["informations"]
         ]
 
     @_auto_update
     @_auth_required
     @_auto_session_refresh
     async def transfer_out(self, password: str) -> dict:
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.generate_transfer_code(
-                self.user_id,  # type: ignore[arg-type]
-                password,
-            )
-            return self._update_user_resources(response)
+        response: dict = await self.api_manager.generate_transfer_code(
+            self.user_id,  # type: ignore[arg-type]
+            password,
+        )
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     async def transfer_check(self, transfer_code: str, password: str) -> dict:
         response: dict = await self.api_manager.checkTransferCode(
             transfer_code, password
         )
@@ -826,100 +1115,94 @@
         credential: str = response["credential"]
         return await self.login(user_id, credential)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def advance_tutorial(self, unit: Unit = Unit.LN) -> dict:
-        async with self.user_data as user_data, self._user_data_lock:
+        async with self.user_data as user_data:
             current_tutorial_status: TutorialStatus = TutorialStatus(
                 user_data["userTutorial"]["tutorialStatus"]
             )
-            response: dict = await self.api_manager.set_tutorial_status(
-                self.user_id,  # type: ignore[arg-type]
-                current_tutorial_status.next(unit),
-            )
-            return self._update_user_resources(response)
+        response: dict = await self.api_manager.set_tutorial_status(
+            self.user_id,  # type: ignore[arg-type]
+            current_tutorial_status.next(unit),
+        )
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def receive_present(self, present_id) -> dict:
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.receive_presents(
-                self.user_id,  # type: ignore[arg-type]
-                [present_id],
-            )
-            return self._update_user_resources(response)
+        response: dict = await self.api_manager.receive_presents(
+            self.user_id,  # type: ignore[arg-type]
+            [present_id],
+        )
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def receive_all_presents(self) -> dict:
         async with self.user_data as user_data:
             response: dict = await self.api_manager.receive_presents(
                 self.user_id,  # type: ignore[arg-type]
                 [present["presentId"] for present in user_data["userPresents"]],
             )
-            return self._update_user_resources(response)
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def gacha(self, gacha_id: int, gach_behavior_id: int) -> dict:
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.gacha(
-                self.user_id, gacha_id, gach_behavior_id  # type: ignore[arg-type]
-            )
-            return self._update_user_resources(response)
+        response: dict = await self.api_manager.gacha(
+            self.user_id, gacha_id, gach_behavior_id  # type: ignore[arg-type]
+        )
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def start_solo_live(self, live: SoloLive):
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.start_solo_live(
-                self.user_id,  # type: ignore[arg-type]
-                live.music_id,
-                live.music_difficulty_id,
-                live.music_vocal_id,
-                live.deck_id,
-                live.boost_count,
-                live.is_auto,
-            )
-            live.start(
-                response["userLiveId"], response["skills"], response["comboCutins"]
-            )
-            return self._update_user_resources(response)
+        response: dict = await self.api_manager.start_solo_live(
+            self.user_id,  # type: ignore[arg-type]
+            live.music_id,
+            live.music_difficulty_id,
+            live.music_vocal_id,
+            live.deck_id,
+            live.boost_count,
+            live.is_auto,
+        )
+        live.start(response["userLiveId"], response["skills"], response["comboCutins"])
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def end_solo_live(self, live: SoloLive) -> dict:
-        async with self._user_data_lock:
-            if not live.is_active or live.live_id is None:
-                raise LiveNotActive
-            if live.life <= 0:
-                raise LiveDead
-            response: dict = await self.api_manager.end_solo_live(
-                self.user_id,  # type: ignore[arg-type]
-                live.live_id,
-                live.score,
-                live.perfect_count,
-                live.great_count,
-                live.good_count,
-                live.bad_count,
-                live.miss_count,
-                live.max_combo,
-                live.life,
-                live.tap_count,
-                live.continue_count,
-            )
-            live.end()
-            return self._update_user_resources(response)
+        if not live.is_active or live.live_id is None:
+            raise LiveNotActive
+        if live.life <= 0:
+            raise LiveDead
+        response: dict = await self.api_manager.end_solo_live(
+            self.user_id,  # type: ignore[arg-type]
+            live.live_id,
+            live.score,
+            live.perfect_count,
+            live.great_count,
+            live.good_count,
+            live.bad_count,
+            live.miss_count,
+            live.max_combo,
+            live.life,
+            live.tap_count,
+            live.continue_count,
+        )
+        live.end()
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def get_event_rankings(
         self,
         event_id: int,
@@ -973,34 +1256,30 @@
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def send_friend_request(
         self, user_id: Union[int, str], message: Optional[str] = None
     ) -> None:
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.send_friend_request(self.user_id, user_id, message)  # type: ignore[arg-type]
-            self._update_user_resources(response)
+        response: dict = await self.api_manager.send_friend_request(self.user_id, user_id, message)  # type: ignore[arg-type]
+        await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def reject_friend_request(self, request_user_id: Union[int, str]) -> None:
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.reject_friend_request(self.user_id, request_user_id)  # type: ignore[arg-type]
-            self._update_user_resources(response)
+        response: dict = await self.api_manager.reject_friend_request(self.user_id, request_user_id)  # type: ignore[arg-type]
+        await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def accept_friend_request(self, request_user_id: Union[int, str]) -> dict:
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.accept_friend_request(self.user_id, request_user_id)  # type: ignore[arg-type]
-            return self._update_user_resources(response)
+        response: dict = await self.api_manager.accept_friend_request(self.user_id, request_user_id)  # type: ignore[arg-type]
+        return await self._update_user_resources(response)
 
     @_auto_update
     @_auto_session_refresh
     @_auth_required
     async def remove_friend(self, friend_user_id: Union[int, str]) -> dict:
-        async with self._user_data_lock:
-            response: dict = await self.api_manager.remove_friend(self.user_id, friend_user_id)  # type: ignore[arg-type]
-            return self._update_user_resources(response)
+        response: dict = await self.api_manager.remove_friend(self.user_id, friend_user_id)  # type: ignore[arg-type]
+        return await self._update_user_resources(response)
```

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/enums/enums.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/enums/enums.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/enums/information.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/enums/information.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/enums/platform.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/enums/platform.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/enums/tutorial_status.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/enums/tutorial_status.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/enums/unknown.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/enums/unknown.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/exceptions.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/exceptions.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/live.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/live.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/models/asset_bundle_info.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/models/asset_bundle_info.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/models/converters.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/models/converters.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/models/game_version.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/models/game_version.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/models/information.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/models/information.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/models/master_data.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/models/master_data.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/models/system_info.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/models/system_info.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/async_pjsekai/utilities.py` & `async_pjsekai-0.0.10.dev2/async_pjsekai/utilities.py`

 * *Files identical despite different names*

### Comparing `async_pjsekai-0.0.10.dev1/pyproject.toml` & `async_pjsekai-0.0.10.dev2/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "async-pjsekai"
-version = "0.0.10.dev1"
+version = "0.0.10.dev2"
 description = "Asynchronous reverse engineered client for the game Project SEKAI COLORFUL STAGE! feat. Hatsune Miku"
 readme = "README.md"
 repository = "https://github.com/TheerapakG/sekai-monorepo"
 license = "MIT"
 authors = [
     "TheerapakG <theerapakg@gmail.com>",
 ]
@@ -30,7 +30,8 @@
 python = "^3.8"
 
 aiohttp = "~3.8.4"
 cattrs = "~22.2.0"
 msgpack = "~1.0.5"
 pycryptodome = "~3.17"
 PyJWT = "~2.6.0"
+aiofiles = "~23.1.0"
```

### Comparing `async_pjsekai-0.0.10.dev1/PKG-INFO` & `async_pjsekai-0.0.10.dev2/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: async-pjsekai
-Version: 0.0.10.dev1
+Version: 0.0.10.dev2
 Summary: Asynchronous reverse engineered client for the game Project SEKAI COLORFUL STAGE! feat. Hatsune Miku
 Home-page: https://github.com/TheerapakG/sekai-monorepo
 License: MIT
 Author: TheerapakG
 Author-email: theerapakg@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Development Status :: 2 - Pre-Alpha
@@ -16,14 +16,15 @@
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Requires-Dist: PyJWT (>=2.6.0,<2.7.0)
+Requires-Dist: aiofiles (>=23.1.0,<23.2.0)
 Requires-Dist: aiohttp (>=3.8.4,<3.9.0)
 Requires-Dist: cattrs (>=22.2.0,<22.3.0)
 Requires-Dist: msgpack (>=1.0.5,<1.1.0)
 Requires-Dist: pycryptodome (>=3.17,<3.18)
 Project-URL: Repository, https://github.com/TheerapakG/sekai-monorepo
 Description-Content-Type: text/markdown
```

