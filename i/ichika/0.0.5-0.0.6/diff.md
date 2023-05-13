# Comparing `tmp/ichika-0.0.5.tar.gz` & `tmp/ichika-0.0.6.tar.gz`

## Comparing `ichika-0.0.5.tar` & `ichika-0.0.6.tar`

### file list

```diff
@@ -1,48 +1,51 @@
--rw-r--r--   0        0        0      253 1970-01-01 00:00:00.000000 ichika-0.0.5/local_dependencies/pyo3-repr/Cargo.toml
--rw-r--r--   0     1001      123     4379 2023-05-03 10:21:17.000000 ichika-0.0.5/local_dependencies/pyo3-repr/src/lib.rs
--rw-r--r--   0        0        0     1324 1970-01-01 00:00:00.000000 ichika-0.0.5/Cargo.toml
--rw-r--r--   0     1001      123     2004 2023-05-03 10:21:17.000000 ichika-0.0.5/README.md
--rw-r--r--   0     1001      123     3028 2023-05-03 10:21:17.000000 ichika-0.0.5/pyproject.toml
--rw-r--r--   0     1001      123      231 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/__init__.py
--rw-r--r--   0     1001      123     1052 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/build_info.py
--rw-r--r--   0     1001      123     7580 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/client.py
--rw-r--r--   0     1001      123    19567 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/core.pyi
--rw-r--r--   0     1001      123     4138 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/event_defs.py
--rw-r--r--   0     1001      123      266 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/exceptions.py
--rw-r--r--   0     1001      123     5086 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/graia/__init__.py
--rw-r--r--   0     1001      123     6990 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/graia/event.py
--rw-r--r--   0     1001      123     4303 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/login/__init__.py
--rw-r--r--   0     1001      123     3864 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/login/password.py
--rw-r--r--   0     1001      123     4115 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/login/qrcode/__init__.py
--rw-r--r--   0     1001      123      249 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/login/qrcode/render/__init__.py
--rw-r--r--   0     1001      123      794 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/login/qrcode/render/dense1x2.py
--rw-r--r--   0     1001      123     1016 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/message/__init__.py
--rw-r--r--   0     1001      123      290 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/message/_sealed.py
--rw-r--r--   0     1001      123    13312 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/message/elements.py
--rw-r--r--   0     1001      123     1913 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/message/serializer.py
--rw-r--r--   0     1001      123        0 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/scripts/__init__.py
--rw-r--r--   0     1001      123     1227 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/scripts/device/__init__.py
--rw-r--r--   0     1001      123     1903 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/scripts/device/converter.py
--rw-r--r--   0     1001      123     5163 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/scripts/device/data.json
--rw-r--r--   0     1001      123     2305 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/scripts/device/generator.py
--rw-r--r--   0     1001      123     1934 2023-05-03 10:21:17.000000 ichika-0.0.5/python/ichika/utils.py
--rw-r--r--   0     1001      123     1036 2023-05-03 10:21:17.000000 ichika-0.0.5/src/build_info.rs
--rw-r--r--   0     1001      123     4961 2023-05-03 10:21:17.000000 ichika-0.0.5/src/client/cached.rs
--rw-r--r--   0     1001      123     2995 2023-05-03 10:21:17.000000 ichika-0.0.5/src/client/friend.rs
--rw-r--r--   0     1001      123     2640 2023-05-03 10:21:17.000000 ichika-0.0.5/src/client/group.rs
--rw-r--r--   0     1001      123     1926 2023-05-03 10:21:17.000000 ichika-0.0.5/src/client/http.rs
--rw-r--r--   0     1001      123    24702 2023-05-03 10:21:17.000000 ichika-0.0.5/src/client/mod.rs
--rw-r--r--   0     1001      123     8028 2023-05-03 10:21:17.000000 ichika-0.0.5/src/client/structs.rs
--rw-r--r--   0     1001      123    12659 2023-05-03 10:21:17.000000 ichika-0.0.5/src/events/converter.rs
--rw-r--r--   0     1001      123     3897 2023-05-03 10:21:17.000000 ichika-0.0.5/src/events/mod.rs
--rw-r--r--   0     1001      123     2035 2023-05-03 10:21:17.000000 ichika-0.0.5/src/exc.rs
--rw-r--r--   0     1001      123     1509 2023-05-03 10:21:17.000000 ichika-0.0.5/src/lib.rs
--rw-r--r--   0     1001      123     1918 2023-05-03 10:21:17.000000 ichika-0.0.5/src/login/connector.rs
--rw-r--r--   0     1001      123    17476 2023-05-03 10:21:17.000000 ichika-0.0.5/src/login/mod.rs
--rw-r--r--   0     1001      123     6514 2023-05-03 10:21:17.000000 ichika-0.0.5/src/loguru.rs
--rw-r--r--   0     1001      123     9823 2023-05-03 10:21:17.000000 ichika-0.0.5/src/message/convert.rs
--rw-r--r--   0     1001      123     1667 2023-05-03 10:21:17.000000 ichika-0.0.5/src/message/elements.rs
--rw-r--r--   0     1001      123       35 2023-05-03 10:21:17.000000 ichika-0.0.5/src/message/mod.rs
--rw-r--r--   0     1001      123     5393 2023-05-03 10:21:17.000000 ichika-0.0.5/src/utils.rs
--rw-r--r--   0     1001      123    55974 2023-05-03 10:21:17.000000 ichika-0.0.5/Cargo.lock
--rw-r--r--   0        0        0     3388 1970-01-01 00:00:00.000000 ichika-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0      253 1970-01-01 00:00:00.000000 ichika-0.0.6/local_dependencies/pyo3-repr/Cargo.toml
+-rw-r--r--   0     1001      123     4379 2023-05-13 14:38:16.000000 ichika-0.0.6/local_dependencies/pyo3-repr/src/lib.rs
+-rw-r--r--   0        0        0      177 1970-01-01 00:00:00.000000 ichika-0.0.6/local_dependencies/t544_enc/Cargo.toml
+-rw-r--r--   0     1001      123       19 2023-05-13 14:38:24.000000 ichika-0.0.6/local_dependencies/t544_enc/src/lib.rs
+-rw-r--r--   0     1001      123       86 2023-05-13 14:38:24.000000 ichika-0.0.6/local_dependencies/t544_enc/src/t544_sign.rs
+-rw-r--r--   0        0        0     1471 1970-01-01 00:00:00.000000 ichika-0.0.6/Cargo.toml
+-rw-r--r--   0     1001      123     2004 2023-05-13 14:38:16.000000 ichika-0.0.6/README.md
+-rw-r--r--   0     1001      123     3028 2023-05-13 14:38:16.000000 ichika-0.0.6/pyproject.toml
+-rw-r--r--   0     1001      123      231 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/__init__.py
+-rw-r--r--   0     1001      123     1052 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/build_info.py
+-rw-r--r--   0     1001      123     7580 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/client.py
+-rw-r--r--   0     1001      123    19186 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/core.pyi
+-rw-r--r--   0     1001      123     4138 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/event_defs.py
+-rw-r--r--   0     1001      123      266 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/exceptions.py
+-rw-r--r--   0     1001      123     6253 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/graia/__init__.py
+-rw-r--r--   0     1001      123     7214 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/graia/event.py
+-rw-r--r--   0     1001      123     4541 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/login/__init__.py
+-rw-r--r--   0     1001      123     3864 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/login/password.py
+-rw-r--r--   0     1001      123     4115 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/login/qrcode/__init__.py
+-rw-r--r--   0     1001      123      249 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/login/qrcode/render/__init__.py
+-rw-r--r--   0     1001      123      794 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/login/qrcode/render/dense1x2.py
+-rw-r--r--   0     1001      123     1017 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/message/__init__.py
+-rw-r--r--   0     1001      123      290 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/message/_sealed.py
+-rw-r--r--   0     1001      123     1935 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/message/_serializer.py
+-rw-r--r--   0     1001      123    13577 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/message/elements.py
+-rw-r--r--   0     1001      123        0 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/scripts/__init__.py
+-rw-r--r--   0     1001      123     1227 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/scripts/device/__init__.py
+-rw-r--r--   0     1001      123     1903 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/scripts/device/converter.py
+-rw-r--r--   0     1001      123     5163 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/scripts/device/data.json
+-rw-r--r--   0     1001      123     2305 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/scripts/device/generator.py
+-rw-r--r--   0     1001      123      741 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/structs.py
+-rw-r--r--   0     1001      123     1934 2023-05-13 14:38:16.000000 ichika-0.0.6/python/ichika/utils.py
+-rw-r--r--   0     1001      123     1036 2023-05-13 14:38:16.000000 ichika-0.0.6/src/build_info.rs
+-rw-r--r--   0     1001      123     5602 2023-05-13 14:38:16.000000 ichika-0.0.6/src/client/cached.rs
+-rw-r--r--   0     1001      123     1834 2023-05-13 14:38:16.000000 ichika-0.0.6/src/client/http.rs
+-rw-r--r--   0     1001      123    26119 2023-05-13 14:38:16.000000 ichika-0.0.6/src/client/mod.rs
+-rw-r--r--   0     1001      123     4489 2023-05-13 14:38:16.000000 ichika-0.0.6/src/client/params.rs
+-rw-r--r--   0     1001      123    10304 2023-05-13 14:38:16.000000 ichika-0.0.6/src/client/structs.rs
+-rw-r--r--   0     1001      123    12632 2023-05-13 14:38:16.000000 ichika-0.0.6/src/events/converter.rs
+-rw-r--r--   0     1001      123     3897 2023-05-13 14:38:16.000000 ichika-0.0.6/src/events/mod.rs
+-rw-r--r--   0     1001      123     2301 2023-05-13 14:38:16.000000 ichika-0.0.6/src/exc.rs
+-rw-r--r--   0     1001      123     1895 2023-05-13 14:38:16.000000 ichika-0.0.6/src/lib.rs
+-rw-r--r--   0     1001      123     1779 2023-05-13 14:38:16.000000 ichika-0.0.6/src/login/connector.rs
+-rw-r--r--   0     1001      123    20578 2023-05-13 14:38:16.000000 ichika-0.0.6/src/login/mod.rs
+-rw-r--r--   0     1001      123     6625 2023-05-13 14:38:16.000000 ichika-0.0.6/src/loguru.rs
+-rw-r--r--   0     1001      123    10122 2023-05-13 14:38:16.000000 ichika-0.0.6/src/message/convert.rs
+-rw-r--r--   0     1001      123     1667 2023-05-13 14:38:16.000000 ichika-0.0.6/src/message/elements.rs
+-rw-r--r--   0     1001      123       35 2023-05-13 14:38:16.000000 ichika-0.0.6/src/message/mod.rs
+-rw-r--r--   0     1001      123     5649 2023-05-13 14:38:16.000000 ichika-0.0.6/src/utils.rs
+-rw-r--r--   0     1001      123    57725 2023-05-13 14:38:47.000000 ichika-0.0.6/Cargo.lock
+-rw-r--r--   0        0        0     3388 1970-01-01 00:00:00.000000 ichika-0.0.6/PKG-INFO
```

### Comparing `ichika-0.0.5/local_dependencies/pyo3-repr/src/lib.rs` & `ichika-0.0.6/local_dependencies/pyo3-repr/src/lib.rs`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/README.md` & `ichika-0.0.6/README.md`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/pyproject.toml` & `ichika-0.0.6/pyproject.toml`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/build_info.py` & `ichika-0.0.6/python/ichika/build_info.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/client.py` & `ichika-0.0.6/python/ichika/client.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/event_defs.py` & `ichika-0.0.6/python/ichika/event_defs.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/graia/__init__.py` & `ichika-0.0.6/python/ichika/graia/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -10,15 +10,21 @@
 from graia.broadcast.entities.dispatcher import BaseDispatcher
 from graia.broadcast.interfaces.dispatcher import DispatcherInterface as DI
 from launart import Launart, Launchable
 from loguru import logger
 
 from ichika import core
 from ichika.client import Client
-from ichika.login import BaseLoginCredentialStore, login_password, login_qrcode
+from ichika.exceptions import LoginError
+from ichika.login import (
+    BaseLoginCredentialStore,
+    PasswordProtocol,
+    login_password,
+    login_qrcode,
+)
 from ichika.login.password import PasswordLoginCallbacks
 from ichika.login.qrcode import QRCodeLoginCallbacks
 from ichika.utils import generic_issubclass
 
 BROADCAST_EVENT = ContextVar("ICHIKA_BROADCAST_EVENT")
 CLIENT_INSTANCE = ContextVar("ICHIKA_CLIENT_INSTANCE")
 
@@ -34,15 +40,15 @@
     broadcast: Broadcast
 
     def __init__(self, broadcast: Optional[Broadcast] = None) -> None:
         loop = asyncio.get_running_loop()
         if not broadcast:
             broadcast = Broadcast(loop=loop)
         if broadcast.loop is not loop:
-            raise ValueError("Graia Broadcast had a different event loop!")
+            raise ValueError("Graia Broadcast 被绑定至不同事件循环!")
         self.broadcast = broadcast
         if IchikaClientDispatcher not in broadcast.prelude_dispatchers:
             broadcast.prelude_dispatchers.append(IchikaClientDispatcher)
 
     async def put(self, data: Any) -> None:
         from .event import EVENT_TYPES
 
@@ -53,24 +59,31 @@
         event_token = BROADCAST_EVENT.set(e)
         await self.broadcast.postEvent(e)
         BROADCAST_EVENT.reset(event_token)
         CLIENT_INSTANCE.reset(client_token)
 
 
 class IchikaComponent(Launchable):
+    """可用于 Launart 的 Ichika 组件"""
+
     class _LoginPartial(Protocol):
         def __call__(
             self,
             *,
             store: BaseLoginCredentialStore,
             event_callbacks: list[core.EventCallback],
         ) -> Awaitable[Client]:
             ...
 
     def __init__(self, store: BaseLoginCredentialStore, broadcast: Optional[Broadcast] = None) -> None:
+        """初始化 Ichika 组件
+
+        :param store: 登录凭据存储, 可以使用 `ichika.login.PathCredentialStore`
+        :param broadcast: Graia Broadcast 实例
+        """
         self.broadcast = broadcast
         self.store: BaseLoginCredentialStore = store
         self.login_partials: dict[int, IchikaComponent._LoginPartial] = {}
         self.client_hb_map: dict[int, tuple[Client, Awaitable[None]]] = {}
         super().__init__()
 
     id = "ichika.main"
@@ -84,20 +97,20 @@
         return set()
 
     def add_password_login(
         self,
         uin: int,
         credential: str | bytes,
         /,
-        protocol: str = "AndroidPad",
+        protocol: PasswordProtocol = "AndroidPad",
         callbacks: PasswordLoginCallbacks | None = None,
         use_sms: bool = True,
     ) -> Self:
         if uin in self.login_partials:
-            raise ValueError(f"uin {uin} already exists")
+            raise ValueError(f"账号 {uin} 已经存在")
         self.login_partials[uin] = partial(
             login_password,
             uin,
             credential,
             protocol=protocol,
             login_callbacks=callbacks,
             use_sms=use_sms,
@@ -108,35 +121,50 @@
         self,
         uin: int,
         /,
         protocol: Literal["AndroidWatch"] = "AndroidWatch",
         callbacks: QRCodeLoginCallbacks | None = None,
     ) -> Self:
         if uin in self.login_partials:
-            raise ValueError(f"uin {uin} already exists")
+            raise ValueError(f"账号 {uin} 已经存在")
         self.login_partials[uin] = partial(login_qrcode, uin, protocol=protocol, login_callbacks=callbacks)
         return self
 
     async def launch(self, mgr: Launart):
         if self.broadcast is None:
             self.broadcast = Broadcast(loop=asyncio.get_running_loop())
         elif self.broadcast.loop is not asyncio.get_running_loop():
-            raise ValueError("Graia Broadcast had a different event loop!")
+            raise ValueError("Graia Broadcast 被绑定至不同事件循环!")
         broadcast_cb = BroadcastCallback(self.broadcast)
+        event_cbs: list[core.EventCallback] = [broadcast_cb]
         async with self.stage("preparing"):
             for uin, login_fn in self.login_partials.items():
                 try:
-                    logger.info(f"Trying to login: {uin}")
-                    client = await login_fn(store=self.store, event_callbacks=[broadcast_cb])
+                    logger.info(f"尝试登录账号: {uin}")
+                    client = await login_fn(store=self.store, event_callbacks=event_cbs)
+                    if not client.online:
+                        raise LoginError(f"账号 {uin} 被服务器断开连接。")
                     self.client_hb_map[uin] = (client, client.keep_alive())
                 except Exception as e:
-                    logger.exception(f"Login failed: {uin}", e)
+                    logger.exception(f"账号 {uin} 登录失败: ", e)
+            if not self.client_hb_map:
+                raise LoginError(f"所有账号均登录失败: {list(self.login_partials.keys())}")
 
         async with self.stage("blocking"):
             await mgr.status.wait_for_sigexit()
+            # 清空事件回调
+            event_cbs.clear()  # LINK: https://github.com/BlueGlassBlock/Ichika/issues/61
+            logger.info("事件监听已终止。")
 
         async with self.stage("cleanup"):
             for uin, (client, hb) in self.client_hb_map.items():
-                logger.info(f"Stopping client: {uin}")
-                await client.stop()
+                logger.info(f"正在停止账号 {uin}。")
+                if client.online:
+                    try:
+                        await client.stop()
+                    except Exception as e:
+                        logger.exception(f"账号 {uin} 停止失败: ", e)
+                    else:
+                        logger.success(f"客户端 {uin} 已停止。")
+                else:
+                    logger.info(f"客户端 {uin} 已离线。")
                 await hb
-                logger.success(f"Client {uin} stopped")
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `ichika-0.0.5/python/ichika/graia/event.py` & `ichika-0.0.6/python/ichika/graia/event.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import contextlib
 from dataclasses import dataclass
 from datetime import datetime, timedelta
-from typing import Dict, Literal, Optional, Type, TypedDict, Union
+from typing import Dict, Literal, Optional, Type, TypedDict, TypeVar, Union
 from typing_extensions import get_type_hints
 
 from graia.amnesia.message import MessageChain
 from graia.broadcast.entities.event import BaseDispatcher, Dispatchable
 from graia.broadcast.entities.signatures import Force
 from graia.broadcast.interfaces.dispatcher import DispatcherInterface as DI
 
@@ -63,20 +63,22 @@
 
 _DISPATCHER_MAP: Dict[type, Type[BaseDispatcher]] = {
     MessageSource: SourceDispatcher,
     MessageChain: MessageChainDispatcher,
     Group: GroupDispatcher,
 }
 
+_Dispatch_T = TypeVar("_Dispatch_T", bound=Dispatchable)
 
-def auto_dispatch(cls):
+
+def auto_dispatch(event_cls: Type[_Dispatch_T]) -> Type[_Dispatch_T]:
     mixins: set[Type[BaseDispatcher]] = {NoneDispatcher}
     type_map: dict[type, set[str]] = {}
 
-    for name, typ in get_type_hints(cls).items():
+    for name, typ in get_type_hints(event_cls).items():
         if name == "sender":
             mixins.add(SenderDispatcher)
         elif dispatcher := _DISPATCHER_MAP.get(typ):
             mixins.add(dispatcher)
         else:
             type_map.setdefault(typ, set()).add(name)
 
@@ -86,23 +88,25 @@
         _name_dispatch: Dict[str, type] = {n: t for t, ns in type_map.items() if len(ns) > 1 for n in ns}
 
         @classmethod
         async def catch(cls, interface: DI):
             anno, name, event = interface.annotation, interface.name, interface.event
             if name in cls._name_dispatch and generic_issubclass(cls._name_dispatch[name], anno):
                 return getattr(event, name)
+            if generic_issubclass(event_cls, anno):
+                return event
             for t, target_name in cls._type_dispatch.items():
                 if generic_issubclass(t, anno):
                     return getattr(event, target_name)
 
-    Dispatcher.__module__ = cls.__module__
-    Dispatcher.__qualname__ = f"{cls.__qualname__}.Dispatcher"
+    Dispatcher.__module__ = event_cls.__module__
+    Dispatcher.__qualname__ = f"{event_cls.__qualname__}.Dispatcher"
 
-    cls.Dispatcher = Dispatcher
-    return cls
+    event_cls.Dispatcher = Dispatcher
+    return event_cls
 
 
 class MessageEvent(Dispatchable):
     source: MessageSource
     content: MessageChain
     sender: Union[Member, Friend]
```

### Comparing `ichika-0.0.5/python/ichika/login/__init__.py` & `ichika-0.0.6/python/ichika/login/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -70,61 +70,71 @@
         return token.read_bytes() if token.exists() else None
 
     def write_token(self, uin: int, protocol: str, token: bytes) -> None:
         token_path = self.uin_path(uin) / f"token-{protocol}.bin"
         token_path.write_bytes(token)
 
 
+PasswordProtocol = Literal["AndroidPhone", "AndroidPad", "IPad", "MacOS", "QiDian"]
+"""可用密码登录的协议
+
+登录成功率较大的:
+
+- AndroidPad (默认)
+- AndroidPhone
+"""
+
+
 @overload
 async def login_password(
     uin: int,
     password: str,
     /,
-    protocol: str,
+    protocol: PasswordProtocol,
     store: BaseLoginCredentialStore,
     event_callbacks: Sequence[_core.EventCallback],
     login_callbacks: PasswordLoginCallbacks | None = None,
     use_sms: bool = ...,
 ) -> Client:
     ...
 
 
 @overload
 async def login_password(
     uin: int,
     password_md5: bytes,
     /,
-    protocol: str,
+    protocol: PasswordProtocol,
     store: BaseLoginCredentialStore,
     event_callbacks: Sequence[_core.EventCallback],
     login_callbacks: PasswordLoginCallbacks | None = None,
     use_sms: bool = ...,
 ) -> Client:
     ...
 
 
 @overload
 async def login_password(
     uin: int,
     credential: str | bytes,
     /,
-    protocol: str,
+    protocol: PasswordProtocol,
     store: BaseLoginCredentialStore,
     event_callbacks: Sequence[_core.EventCallback],
     login_callbacks: PasswordLoginCallbacks | None = None,
     use_sms: bool = ...,
 ) -> Client:
     ...
 
 
 async def login_password(
     uin: int,
     credential: str | bytes,
     /,
-    protocol: str,
+    protocol: PasswordProtocol,
     store: BaseLoginCredentialStore,
     event_callbacks: Sequence[_core.EventCallback],
     login_callbacks: PasswordLoginCallbacks | None = None,
     use_sms: bool = True,
 ) -> Client:
     return await _core.password_login(
         uin, credential, use_sms, protocol, store, event_callbacks, login_callbacks or PasswordLoginCallbacks.default()
```

### Comparing `ichika-0.0.5/python/ichika/login/password.py` & `ichika-0.0.6/python/ichika/login/password.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/login/qrcode/__init__.py` & `ichika-0.0.6/python/ichika/login/qrcode/__init__.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/login/qrcode/render/dense1x2.py` & `ichika-0.0.6/python/ichika/login/qrcode/render/dense1x2.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/message/__init__.py` & `ichika-0.0.6/python/ichika/message/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,16 +2,16 @@
 
 from typing import Any
 
 from graia.amnesia.message import MessageChain
 from graia.amnesia.message.element import Element, Unknown
 from loguru import logger
 
+from ._serializer import _SERIALIZE_INV
 from .elements import _DESERIALIZE_INV
-from .serializer import _SERIALIZE_INV
 
 
 def _deserialize_message(elements: list[dict[str, Any]]) -> MessageChain:
     elem_seq: list[Element] = []
     for e_data in elements:
         cls = _DESERIALIZE_INV.get(e_data.pop("type"), None)
         if cls is None:
```

### Comparing `ichika-0.0.5/python/ichika/message/elements.py` & `ichika-0.0.6/python/ichika/message/elements.py`

 * *Files 2% similar despite different names*

```diff
@@ -39,18 +39,23 @@
 @dataclass
 class At(Element):
     """@元素"""
 
     target: int
     """@的目标 QQ 号"""
     display: str | None = None
-    """@的目标的显示名"""
+    """@ 的目标的显示名，包括前导 @
+
+    注意: 如果构造时不传入此参数，则会在手Q上显示为 “@{target}”，不过仍会起到通知效果。
+
+    参见 [#59](https://github.com/BlueGlassBlock/Ichika/issues/59)
+    """
 
     def __str__(self) -> str:
-        return f"@{self.target}"
+        return self.display or f"@{self.target}"
 
 
 @dataclass
 class AtAll(Element):
     """@全体成员元素"""
 
     def __str__(self) -> str:
@@ -454,15 +459,17 @@
         return f"[商城表情:{self.name}]"
 
     def __repr__(self) -> str:
         return f"MarketFace(name={self.name})"
 
 
 _DESERIALIZE_INV: dict[str, Callable[..., Element]] = {
-    cls.__name__: cls for cls in Element.__subclasses__() if cls.__module__.startswith(("ichika", "graia.amnesia"))
+    cls.__name__: cls
+    for cls in Element.__subclasses__()
+    if cls.__module__.startswith(("ichika", "graia.amnesia")) and cls is not Video
 }
 
 __MUSIC_SHARE_APPID_MAP: dict[int, Literal["QQ", "Netease", "Migu", "Kugou", "Kuwo"]] = {
     100497308: "QQ",
     100495085: "Netease",
     1101053067: "Migu",
     205141: "Kugou",
```

### Comparing `ichika-0.0.5/python/ichika/message/serializer.py` & `ichika-0.0.6/python/ichika/message/_serializer.py`

 * *Files 3% similar despite different names*

```diff
@@ -42,15 +42,15 @@
 
     return func_register
 
 
 _serialize(Reply)(lambda t: {"seq": t.seq, "sender": t.sender, "time": int(t.time.timestamp()), "content": t.content})
 _serialize(Text)(lambda t: {"text": t.text})
 _serialize(AtAll)(lambda _: {})
-_serialize(At)(lambda t: {"target": t.target})
+_serialize(At)(lambda t: {"target": t.target, "display": t.display})
 _serialize(Dice)(lambda t: {"value": t.value})
 _serialize(FingerGuessing)(lambda t: {"choice": t.choice.name})
 _serialize(Face)(lambda t: {"index": t.index})
 _serialize(MarketFace)(lambda t: {"raw": t.raw})
 _serialize(LightApp)(lambda t: {"content": t.content})
 _serialize(RichMessage)(lambda t: {"service_id": t.service_id, "content": t.content})
 _serialize(ForwardCard)(lambda t: {"service_id": 35, "content": t.content})
```

### Comparing `ichika-0.0.5/python/ichika/scripts/device/__init__.py` & `ichika-0.0.6/python/ichika/scripts/device/__init__.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/scripts/device/converter.py` & `ichika-0.0.6/python/ichika/scripts/device/converter.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/scripts/device/data.json` & `ichika-0.0.6/python/ichika/scripts/device/data.json`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/scripts/device/generator.py` & `ichika-0.0.6/python/ichika/scripts/device/generator.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/python/ichika/utils.py` & `ichika-0.0.6/python/ichika/utils.py`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/src/build_info.rs` & `ichika-0.0.6/src/build_info.rs`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/src/client/cached.rs` & `ichika-0.0.6/src/client/cached.rs`

 * *Files 14% similar despite different names*

```diff
@@ -1,27 +1,36 @@
 use std::borrow::Borrow;
 use std::collections::HashMap;
 use std::default::Default;
-use std::hash::Hash;
 use std::sync::Arc;
 use std::time::{Duration, Instant};
 
+use backon::{ExponentialBuilder, Retryable as _};
+use lru_time_cache::LruCache;
 use once_cell::sync::Lazy;
-use ricq::{Client, RQError, RQResult};
+use ricq::{Client, RQError};
 use tokio::sync::Mutex;
 
-use super::friend::FriendList;
-use super::group::{Group, Member};
+use super::structs::{FriendList, Group, Member};
+use crate::exc::IckResult;
 
 static CACHE_DURATION: Duration = Duration::from_secs(600);
 
 static CACHE: Lazy<Mutex<HashMap<i64, Arc<Mutex<DetachedCache>>>>> = Lazy::new(Mutex::default);
 
+static RETRY_BUILDER: Lazy<ExponentialBuilder> = Lazy::new(|| {
+    ExponentialBuilder::default()
+        .with_factor(1.5)
+        .with_min_delay(Duration::from_secs(1))
+        .with_max_delay(Duration::from_secs(5))
+        .with_max_times(3)
+});
+
 #[repr(transparent)]
-struct VarCache<T> {
+pub(crate) struct VarCache<T> {
     val: Option<(Instant, Arc<T>)>,
 }
 
 impl<T> Default for VarCache<T> {
     fn default() -> Self {
         Self { val: None }
     }
@@ -45,133 +54,136 @@
 
     fn clear(&mut self) {
         self.val = None;
     }
 }
 
 #[repr(transparent)]
-struct MapCache<K, V> {
-    map: HashMap<K, (Instant, Arc<V>)>,
+pub(crate) struct MapCache<K, V> {
+    map: LruCache<K, Arc<V>>,
 }
 
-impl<K, V> Default for MapCache<K, V> {
+impl<K, V> Default for MapCache<K, V>
+where
+    K: Ord + Clone,
+{
     fn default() -> Self {
         Self {
-            map: HashMap::default(),
+            map: LruCache::with_expiry_duration_and_capacity(CACHE_DURATION, 1024),
         }
     }
 }
 
 impl<K, V> MapCache<K, V>
 where
-    K: Eq + Hash,
+    K: Ord + Clone,
 {
-    fn get<Q>(&mut self, key: &Q) -> Option<Arc<V>>
+    pub(crate) fn get<Q>(&mut self, key: &Q) -> Option<Arc<V>>
     where
         K: Borrow<Q>,
-        Q: Hash + Eq,
+        Q: Ord,
     {
-        if let Some((ref last_upd, ref arc)) = self.map.get(key) {
-            if last_upd.elapsed() <= CACHE_DURATION {
-                return Some(arc.clone());
-            }
-            self.map.remove(key);
-        }
-        None
+        self.map.get(key).cloned()
     }
 
-    fn set(&mut self, key: K, val: Arc<V>) -> Arc<V> {
-        self.map.insert(key, (Instant::now(), val.clone()));
+    pub(crate) fn set(&mut self, key: K, val: Arc<V>) -> Arc<V> {
+        self.map.insert(key, val.clone());
         val
     }
 
-    fn remove<Q>(&mut self, key: &Q) -> Option<Arc<V>>
+    pub(crate) fn remove<Q>(&mut self, key: &Q) -> Option<Arc<V>>
     where
         K: Borrow<Q>,
-        Q: Hash + Eq,
+        Q: Ord,
     {
-        self.map.remove(key).map(|v| v.1)
+        self.map.remove(key)
     }
 }
 
 #[derive(Default)]
-struct DetachedCache {
-    friends: VarCache<FriendList>,
-    groups: MapCache<i64, Group>,
-    members: MapCache<(i64, i64), Member>,
+pub(crate) struct DetachedCache {
+    pub(crate) friends: VarCache<FriendList>,
+    pub(crate) groups: MapCache<i64, Group>,
+    pub(crate) members: MapCache<(i64, i64), Member>,
 }
 
 impl VarCache<FriendList> {
-    async fn fetch(&mut self, client: &Arc<Client>) -> RQResult<Arc<FriendList>> {
+    async fn fetch(&mut self, client: &Arc<Client>) -> IckResult<Arc<FriendList>> {
         if let Some(val) = self.get() {
             return Ok(val);
         }
-        let val = Arc::new(client.get_friend_list().await?.into());
+        let fetch_closure =
+            async move || -> IckResult<FriendList> { Ok(client.get_friend_list().await?.into()) };
+        let val = Arc::new(fetch_closure.retry(&*RETRY_BUILDER).await?);
         Ok(self.set(val))
     }
 }
 
 impl MapCache<i64, Group> {
-    async fn fetch(&mut self, client: &Arc<Client>, uin: i64) -> RQResult<Arc<Group>> {
+    async fn fetch(&mut self, client: &Arc<Client>, uin: i64) -> IckResult<Arc<Group>> {
         if let Some(val) = self.get(&uin) {
             return Ok(val);
         }
-        let val = Arc::new(
-            client
+        let fetch_closure = async move || -> IckResult<Group> {
+            Ok(client
                 .get_group_info(uin)
                 .await?
                 .ok_or_else(|| RQError::EmptyField("group"))?
-                .into(),
-        );
+                .into())
+        };
+        let val = Arc::new(fetch_closure.retry(&*RETRY_BUILDER).await?);
         Ok(self.set(uin, val))
     }
 }
 
 impl MapCache<(i64, i64), Member> {
     async fn fetch(
         &mut self,
         client: &Arc<Client>,
         group_uin: i64,
         uin: i64,
-    ) -> RQResult<Arc<Member>> {
+    ) -> IckResult<Arc<Member>> {
         if let Some(val) = self.get(&(group_uin, uin)) {
             return Ok(val);
         }
-        let val = Arc::new(client.get_group_member_info(group_uin, uin).await?.into());
+        let fetch_closure = async move || -> IckResult<Member> {
+            Ok(client.get_group_member_info(group_uin, uin).await?.into())
+        };
+        let val = Arc::new(fetch_closure.retry(&*RETRY_BUILDER).await?);
         Ok(self.set((group_uin, uin), val))
     }
 }
 
 pub struct ClientCache {
-    client: Arc<Client>,
-    detached: Arc<Mutex<DetachedCache>>,
+    pub(crate) client: Arc<Client>,
+    pub(crate) detached: Arc<Mutex<DetachedCache>>,
 }
 
 impl ClientCache {
-    pub async fn fetch_friend_list(&mut self) -> RQResult<Arc<FriendList>> {
+    pub async fn fetch_friend_list(&mut self) -> IckResult<Arc<FriendList>> {
         let mut guard = self.detached.lock().await;
         guard.friends.fetch(&self.client).await
     }
 
     pub async fn flush_friend_list(&mut self) {
         let mut guard = self.detached.lock().await;
         guard.friends.clear();
     }
 
-    pub async fn fetch_group(&mut self, uin: i64) -> RQResult<Arc<Group>> {
+    pub async fn fetch_group(&mut self, uin: i64) -> IckResult<Arc<Group>> {
         let mut guard = self.detached.lock().await;
         guard.groups.fetch(&self.client, uin).await
     }
 
     pub async fn flush_group(&mut self, uin: i64) {
         let mut guard = self.detached.lock().await;
         guard.groups.remove(&uin);
     }
 
-    pub async fn fetch_member(&mut self, group_uin: i64, uin: i64) -> RQResult<Arc<Member>> {
+    pub async fn fetch_member(&mut self, group_uin: i64, uin: i64) -> IckResult<Arc<Member>> {
         let mut guard = self.detached.lock().await;
         guard.members.fetch(&self.client, group_uin, uin).await
     }
 
     pub async fn flush_member(&mut self, group_uin: i64, uin: i64) {
         let mut guard = self.detached.lock().await;
         guard.members.remove(&(group_uin, uin));
```

### Comparing `ichika-0.0.5/src/client/http.rs` & `ichika-0.0.6/src/client/http.rs`

 * *Files 8% similar despite different names*

```diff
@@ -22,16 +22,14 @@
     locals: TaskLocals,
 }
 
 fn http_method_to_string(method: RQHttpMethod) -> String {
     match method {
         RQHttpMethod::GET => "get".into(),
         RQHttpMethod::POST => "post".into(),
-        RQHttpMethod::PUT => "put".into(),
-        RQHttpMethod::DELETE => "delete".into(),
     }
 }
 
 #[async_trait]
 impl RQHttpClient for PyHttpClient {
     async fn make_request(
         &mut self,
```

### Comparing `ichika-0.0.5/src/client/mod.rs` & `ichika-0.0.6/src/client/mod.rs`

 * *Files 4% similar despite different names*

```diff
@@ -1,36 +1,36 @@
 mod cached;
-pub mod friend;
-pub mod group;
 mod http;
+mod params;
 pub mod structs;
+
 use std::sync::Arc;
 use std::time::Duration;
 
 pub use cached::{cache, ClientCache};
-use group::Group;
-use http::get_rust_client;
 use pyo3::exceptions::PyRuntimeError;
 use pyo3::prelude::*;
 use pyo3::types::*;
 use ricq::msg::elem::RQElem;
 use ricq::structs::{ForwardMessage, FriendAudio, GroupAudio, ProfileDetailUpdate, Status};
-use structs::*;
 use tokio::task::JoinHandle;
 
+use self::http::get_rust_client;
+use self::params::*;
+use self::structs::*;
 use crate::login::{reconnect, TokenRW};
 use crate::message::convert::{
     deserialize_message_chain,
     render_forward,
     serialize_audio_dict,
     serialize_element,
     serialize_forward,
 };
 use crate::message::elements::SealedAudio;
-use crate::utils::{py_future, py_none, py_try, py_use, AsPython};
+use crate::utils::{py_future, py_none, py_try, py_use, to_py_gender, to_py_permission, AsPython};
 
 #[pyclass(subclass, weakref, module = "ichika.core")]
 pub struct PlumbingClient {
     client: Arc<ricq::client::Client>,
     alive: Option<JoinHandle<()>>,
     #[pyo3(get)]
     uin: i64,
@@ -79,15 +79,15 @@
                     if let Some(handle) = reconnect(&client, &token_rw).await? {
                         alive = handle;
                     } else {
                         break;
                     }
                 }
             }
-            tracing::info!("客户端 {} 连接断开", uin);
+            tracing::info!("客户端 {} 被迫断开连接", uin);
             Ok(py_none())
         })
     }
 
     #[getter]
     pub fn online(&self) -> bool {
         self.client
@@ -102,22 +102,30 @@
                 .update_online_status(ricq::structs::OnlineStatus::Offline)
                 .await?;
             client.stop(ricq::client::NetworkStatus::Stop);
             Ok(())
         })
     }
 
+    pub fn get_profile<'py>(&self, py: Python<'py>, uin: i64) -> PyResult<&'py PyAny> {
+        let client = self.client.clone();
+        py_future(py, async move {
+            let profile = client.get_summary_info(uin).await?;
+            Ok(Profile::from(profile))
+        })
+    }
+
     pub fn get_account_info<'py>(&self, py: Python<'py>) -> PyResult<&'py PyAny> {
         let client = self.client.clone();
         py_future(py, async move {
             let info = client.account_info.read().await;
             Ok(AccountInfo {
                 nickname: info.nickname.clone(),
                 age: info.age,
-                gender: info.gender,
+                gender: to_py_gender(info.gender),
             })
         })
     }
 
     #[pyo3(signature = (*, name=None, email=None, personal_note=None, company=None,college=None,signature=None))]
     #[allow(clippy::too_many_arguments, reason = "Readable")]
     pub fn set_account_info<'py>(
@@ -211,27 +219,25 @@
             Ok(OCRResult::from(resp).obj())
         })
     }
 }
 
 #[pymethods]
 impl PlumbingClient {
-    pub fn get_friend_list<'py>(&self, py: Python<'py>) -> PyResult<&'py PyAny> {
-        let client = self.client.clone();
-        py_future(py, async move {
-            let friend_list = cache(client).await.fetch_friend_list().await?;
-            Ok((*friend_list).clone().obj())
-        })
-    }
+    #[pyo3(signature = (cache=true))]
+    pub fn get_friend_list<'py>(&self, py: Python<'py>, cache: bool) -> PyResult<&'py PyAny> {
+        use self::cache as get_cache;
 
-    pub fn get_friend_list_raw<'py>(&self, py: Python<'py>) -> PyResult<&'py PyAny> {
+        let use_cache = cache;
         let client = self.client.clone();
         py_future(py, async move {
-            let mut cache = cache(client).await;
-            cache.flush_friend_list().await;
+            let mut cache = get_cache(client).await;
+            if !use_cache {
+                cache.flush_friend_list().await;
+            }
             let friend_list = cache.fetch_friend_list().await?;
             Ok((*friend_list).clone().obj())
         })
     }
 
     pub fn get_friends<'py>(&self, py: Python<'py>) -> PyResult<&'py PyAny> {
         let client = self.client.clone();
@@ -264,27 +270,25 @@
             Ok(())
         })
     }
 }
 
 #[pymethods]
 impl PlumbingClient {
-    pub fn get_group<'py>(&self, py: Python<'py>, uin: i64) -> PyResult<&'py PyAny> {
-        let client = self.client.clone();
-        py_future(py, async move {
-            let group = cache(client).await.fetch_group(uin).await?;
-            Ok((*group).clone().obj())
-        })
-    }
+    #[pyo3(signature = (uin, cache=true))]
+    pub fn get_group<'py>(&self, py: Python<'py>, uin: i64, cache: bool) -> PyResult<&'py PyAny> {
+        use self::cache as get_cache;
+        let use_cache = cache;
 
-    pub fn get_group_raw<'py>(&self, py: Python<'py>, uin: i64) -> PyResult<&'py PyAny> {
         let client = self.client.clone();
         py_future(py, async move {
-            let mut cache = cache(client).await;
-            cache.flush_group(uin).await;
+            let mut cache = get_cache(client).await;
+            if !use_cache {
+                cache.flush_group(uin).await;
+            }
             let group = cache.fetch_group(uin).await?;
             Ok((*group).clone().obj())
         })
     }
 
     pub fn find_group<'py>(&self, py: Python<'py>, uin: i64) -> PyResult<&'py PyAny> {
         let client = self.client.clone();
@@ -308,23 +312,29 @@
                 )
                 .obj()
             }))
         })
     }
 
     pub fn get_group_admins<'py>(&self, py: Python<'py>, uin: i64) -> PyResult<&'py PyAny> {
+        use self::cache as get_cache;
         let client = self.client.clone();
         py_future(py, async move {
-            let admins = client
-                .get_group_admin_list(uin)
-                .await?
-                .into_iter()
-                .map(|(member_uin, perm)| (member_uin, perm as u8))
-                .collect::<Vec<(i64, u8)>>(); // TODO: Better Perm handling
-            Ok(admins)
+            let admins = client.get_group_admin_list(uin).await?;
+            let mut cache = get_cache(client).await;
+            let mut admin_list: Vec<Member> = vec![];
+            for (member_uin, perm) in admins.iter() {
+                let mut member = cache.fetch_member(uin, *member_uin).await?;
+                if !member.permission.is(&to_py_permission(perm.clone())) {
+                    cache.flush_member(uin, *member_uin).await;
+                    member = cache.fetch_member(uin, *member_uin).await?;
+                }
+                admin_list.push((*member).clone());
+            }
+            Ok(admin_list)
         })
     }
 
     pub fn mute_group<'py>(&self, py: Python<'py>, uin: i64, mute: bool) -> PyResult<&'py PyAny> {
         let client = self.client.clone();
         py_future(py, async move {
             client.group_mute_all(uin, mute).await?;
@@ -367,39 +377,66 @@
             Ok(())
         })
     }
 }
 
 #[pymethods]
 impl PlumbingClient {
+    #[pyo3(signature = (group_uin, uin, cache=true))]
     pub fn get_member<'py>(
         &self,
         py: Python<'py>,
         group_uin: i64,
         uin: i64,
+        cache: bool,
     ) -> PyResult<&'py PyAny> {
+        use self::cache as get_cache;
+        let use_cache = cache;
         let client = self.client.clone();
         py_future(py, async move {
-            let member = cache(client).await.fetch_member(group_uin, uin).await?;
+            let mut cache = get_cache(client).await;
+            if !use_cache {
+                cache.flush_member(group_uin, uin).await;
+            }
+            let member = cache.fetch_member(group_uin, uin).await?;
             Ok((*member).clone().obj())
         })
     }
 
-    pub fn get_member_raw<'py>(
+    #[pyo3(signature = (group_uin, cache=true))]
+    pub fn get_member_list<'py>(
         &self,
         py: Python<'py>,
         group_uin: i64,
-        uin: i64,
+        cache: bool,
     ) -> PyResult<&'py PyAny> {
+        use self::cache as get_cache;
+        let use_cache = cache;
         let client = self.client.clone();
         py_future(py, async move {
-            let mut cache = cache(client).await;
-            cache.flush_member(group_uin, uin).await;
-            let member = cache.fetch_member(group_uin, uin).await?;
-            Ok((*member).clone().obj())
+            let mut cache = get_cache(client).await;
+            if !use_cache {
+                cache.flush_group(group_uin).await;
+            }
+            let group = cache.fetch_group(group_uin).await?;
+            let members = cache
+                .client
+                .get_group_member_list(group.uin, group.owner_uin)
+                .await?;
+            let mut guard = cache.detached.lock().await;
+            let members = members
+                .into_iter()
+                .map(|m| {
+                    let m = Member::from(m);
+                    guard.members.set((group.uin, m.uin), Arc::new(m.clone()));
+                    m
+                })
+                .collect::<Vec<_>>();
+            std::mem::drop(guard);
+            Ok(members)
         })
     }
 
     pub fn nudge_member<'py>(
         &self,
         py: Python<'py>,
         group_uin: i64,
```

### Comparing `ichika-0.0.5/src/events/converter.rs` & `ichika-0.0.6/src/events/converter.rs`

 * *Files 0% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 use pyo3::exceptions::PyValueError;
 use pyo3::prelude::*;
 use pyo3::types::PyDict;
 use ricq::client::event as rce;
 use ricq::handler::QEvent;
 
 use super::MessageSource;
-use crate::client::friend::Friend;
-use crate::client::group::{Group, Member};
+use crate::client::structs::{Friend, Group, Member};
 use crate::client::{cache, ClientCache};
 use crate::dict_obj;
 use crate::exc::MapPyErr;
 use crate::message::convert::{serialize_as_py_chain, serialize_audio};
 use crate::utils::{datetime_from_ts, py_try, timedelta_from_secs};
 
 type PyDictRet = PyResult<Py<PyDict>>;
@@ -259,15 +258,15 @@
     let operator = fetch_member(&mut cache, event.group_code, event.operator_uin).await?;
 
     if event.target_uin == 0 {
         return dict_obj! {
             type_name: "GroupMute",
             group: group,
             operator: operator,
-            duration: event.duration.as_secs() == 0
+            status: event.duration.as_secs() == 0
         };
     }
     let duration = event.duration.as_secs();
     let duration = py_try(|py| {
         Ok(if duration != 0 {
             timedelta_from_secs(py, duration)?.into_py(py)
         } else {
```

### Comparing `ichika-0.0.5/src/events/mod.rs` & `ichika-0.0.6/src/events/mod.rs`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/src/exc.rs` & `ichika-0.0.6/src/exc.rs`

 * *Files 6% similar despite different names*

```diff
@@ -19,14 +19,23 @@
 
 #[derive(Debug)]
 pub struct Error {
     inner: InnerError,
     backtrace: Backtrace,
 }
 
+impl From<std::io::Error> for Error {
+    fn from(value: std::io::Error) -> Self {
+        Self {
+            inner: InnerError::RQ(RQError::IO(value)),
+            backtrace: Backtrace::force_capture(),
+        }
+    }
+}
+
 impl From<RQError> for Error {
     fn from(value: RQError) -> Self {
         Self {
             inner: InnerError::RQ(value),
             backtrace: Backtrace::force_capture(),
         }
     }
@@ -84,7 +93,9 @@
             Err(e) => Err({
                 let e: Error = e.into();
                 e.into()
             }),
         }
     }
 }
+
+pub type IckResult<T> = Result<T, Error>;
```

### Comparing `ichika-0.0.5/src/lib.rs` & `ichika-0.0.6/src/lib.rs`

 * *Files 11% similar despite different names*

```diff
@@ -29,31 +29,41 @@
 }
 
 #[pymodule]
 #[doc(hidden)]
 pub fn core(py: Python, m: &PyModule) -> PyResult<()> {
     m.add("__version__", env!("CARGO_PKG_VERSION"))?;
     m.add("__build__", build_info::get_info(py)?)?;
+    let tokio_thread_count = std::env::var("ICHIKA_RUNTIME_THREAD_COUNT")
+        .ok()
+        .and_then(|s| s.parse().ok().filter(|v| *v > 0))
+        .unwrap_or(4);
+    pyo3_asyncio::tokio::init({
+        let mut rt = tokio::runtime::Builder::new_multi_thread();
+        rt.worker_threads(tokio_thread_count).enable_all();
+        rt
+    });
     add_batch!(@fun m,
         loguru::getframe,
         message::elements::face_id_from_name,
         message::elements::face_name_from_id,
         login::password_login,
         login::qrcode_login
     );
     add_batch!(@cls m,
         client::PlumbingClient,
-        client::friend::Friend,
-        client::friend::FriendGroup,
-        client::friend::FriendList,
-        client::group::Group,
-        client::group::Member,
+        client::structs::Friend,
+        client::structs::FriendGroup,
+        client::structs::FriendList,
+        client::structs::Group,
+        client::structs::Member,
         client::structs::AccountInfo,
         client::structs::OtherClientInfo,
         client::structs::RawMessageReceipt,
         client::structs::OCRResult,
         client::structs::OCRText,
+        client::structs::Profile,
         events::MessageSource
     );
     loguru::init(m)?;
     Ok(())
 }
```

### Comparing `ichika-0.0.5/src/login/connector.rs` & `ichika-0.0.6/src/login/connector.rs`

 * *Files 3% similar despite different names*

```diff
@@ -52,14 +52,10 @@
 }
 
 pub struct IchikaConnector;
 
 #[async_trait]
 impl Connector<TcpStream> for IchikaConnector {
     async fn connect(&self, client: &Client) -> io::Result<TcpStream> {
-        let addrs = client.get_address_list().await;
-        for addr in addrs {
-            tracing::info!("地址: {}", addr);
-        }
         tcp_connect_fastest(client.get_address_list().await, Duration::from_secs(5)).await
     }
 }
```

### Comparing `ichika-0.0.5/src/login/mod.rs` & `ichika-0.0.6/src/login/mod.rs`

 * *Files 14% similar despite different names*

```diff
@@ -5,15 +5,14 @@
 use connector::IchikaConnector;
 use pyo3::exceptions::*;
 use pyo3::prelude::*;
 use pyo3::types::*;
 use pyo3_asyncio::{into_future_with_locals, TaskLocals};
 use pythonize::depythonize;
 use ricq::client::{Client, Connector, NetworkStatus, Token};
-use ricq::ext::common::after_login;
 use ricq::version::Version;
 use ricq::{
     Device,
     LoginDeviceLocked,
     LoginNeedCaptcha,
     LoginResponse,
     LoginSuccess,
@@ -22,20 +21,93 @@
 };
 use tokio::task::JoinHandle;
 
 use crate::events::PyHandler;
 use crate::exc::MapPyErr;
 use crate::utils::{partial, py_bytes, py_client_refs, py_future, py_try, py_use};
 use crate::{exc, import_call, PyRet};
+
+#[cfg(feature = "t544")]
+pub(crate) mod t544 {
+    use bytes::{BufMut, Bytes, BytesMut};
+    use ricq::Client;
+    use ricq_core::binary::BinaryWriter;
+    use ricq_core::wtlogin::T544Provider;
+    use t544_enc::t544_sign::sign;
+
+    #[derive(Debug)]
+    struct NativeT544Provider {
+        uin: i64,
+        guid: Bytes,
+        version: Bytes,
+    }
+
+    impl NativeT544Provider {
+        async fn new(client: &Client) -> Self {
+            let uin = client.uin().await;
+            let guid = client.device().await.guid();
+            let version = client.version().await.sdk_version;
+
+            Self {
+                uin,
+                guid,
+                version: Bytes::copy_from_slice(version.as_bytes()),
+            }
+        }
+    }
+
+    impl T544Provider for NativeT544Provider {
+        fn t544(&self, command: String) -> Bytes {
+            let mut salt = BytesMut::new();
+            let cmd = command.split("_").last().unwrap();
+            let cmd = u32::from_str_radix(cmd, 16).unwrap();
+            match cmd {
+                2 | 7 => {
+                    // T544v1
+                    salt.put_u64(self.uin as u64);
+                    salt.write_bytes_short(&self.guid[..]);
+                    salt.write_bytes_short(&self.version[..]);
+                    salt.put_u32(cmd);
+                }
+                _ => {
+                    // T544v2
+                    salt.put_u32(0);
+                    salt.write_bytes_short(&self.guid[..]);
+                    salt.write_bytes_short(&self.version[..]);
+                    salt.put_u32(cmd);
+                    salt.put_u32(0);
+                }
+            }
+            let curr = std::time::UNIX_EPOCH.elapsed().unwrap().as_micros();
+            let res = sign(curr as u64, &salt.freeze()[..]);
+            Bytes::copy_from_slice(&res)
+        }
+    }
+
+    pub(crate) async fn inject_t544(client: &mut Client) {
+        client.engine.write().await.ex_provider.t544 =
+            Some(Box::new(NativeT544Provider::new(client).await));
+    }
+}
+
+
 async fn prepare_client(
     device: Device,
     app_ver: Version,
     handler: PyHandler,
 ) -> PyResult<(Arc<Client>, JoinHandle<()>)> {
-    let client = Arc::new(Client::new(device, app_ver, handler));
+    #[allow(unused_mut)]
+    let mut client = Client::new(device, app_ver, handler);
+
+    #[cfg(feature = "t544")]
+    {
+        t544::inject_t544(&mut client).await;
+    }
+
+    let client = Arc::new(client);
     let alive = tokio::spawn({
         let client = client.clone();
         // 连接最快的服务器
         let stream = IchikaConnector
             .connect(&client)
             .await
             .map_err(|e| PyIOError::new_err(e.to_string()))?;
@@ -171,58 +243,72 @@
     py_use(|py| into_future_with_locals(locals, obj.as_ref(py)))?.await
 }
 
 pub async fn reconnect(
     client: &Arc<Client>,
     token_rw: &TokenRW,
 ) -> PyResult<Option<JoinHandle<()>>> {
-    crate::utils::py_retry(
-        10,
-        || async {
-            // 如果不是网络原因掉线，不重连（服务端强制下线/被踢下线/用户手动停止）
-            if client.get_status() != (NetworkStatus::NetworkOffline as u8) {
-                tracing::warn!("客户端因非网络原因下线，不再重连");
-                return Ok(None);
-            }
-            client.stop(NetworkStatus::NetworkOffline);
+    use std::time::Duration;
 
-            tracing::error!("客户端连接中断，将在 10 秒后重连");
-            tokio::time::sleep(std::time::Duration::from_secs(10)).await;
+    use backon::{ExponentialBuilder, Retryable as _};
 
-            let alive = tokio::spawn({
-                let client = client.clone();
-                // 连接最快的服务器
-                let stream = IchikaConnector.connect(&client).await?;
-
-                #[allow(
-                    clippy::redundant_async_block,
-                    reason = "FP: rust-lang/rust-clippy#10482"
-                )]
-                async move {
-                    client.start(stream).await;
-                }
-            });
-            tokio::task::yield_now().await; // 等一下，确保连上了
+    let uin = client.uin().await;
+
+    let retry_builder = ExponentialBuilder::default()
+        .with_factor(1.2)
+        .with_min_delay(Duration::from_secs(3))
+        .with_max_delay(Duration::from_secs(60))
+        .with_max_times(usize::MAX);
+    let retry_closure = || async {
+        // 如果不是网络原因掉线，不重连（服务端强制下线/被踢下线/用户手动停止）
+        if client.get_status() != (NetworkStatus::NetworkOffline as u8) {
+            tracing::warn!("账号 {} 因非网络原因下线，不再重连", uin);
+            return Ok(None);
+        }
+        client.stop(NetworkStatus::NetworkOffline);
 
-            // 启动接收后，再发送登录请求，否则报错 NetworkError
-            if !token_rw.try_login(client).await? {
-                client.stop(NetworkStatus::NetworkOffline);
-                return Ok(None);
+        let alive = tokio::spawn({
+            let client = client.clone();
+            // 连接最快的服务器
+            let stream = IchikaConnector.connect(&client).await?;
+
+            #[allow(
+                clippy::redundant_async_block,
+                reason = "FP: rust-lang/rust-clippy#10482"
+            )]
+            async move {
+                client.start(stream).await;
             }
+        });
+        tokio::task::yield_now().await; // 等一下，确保连上了
 
-            after_login(client).await;
+        // 启动接收后，再发送登录请求，否则报错 NetworkError
+        if !token_rw.try_login(client).await? {
+            client.stop(NetworkStatus::NetworkOffline);
+            return Err(ricq_core::error::RQError::Network).py_res();
+        }
 
-            tracing::info!("客户端重连成功");
-            Ok(Some(alive))
-        },
-        |e, c| async move {
-            tracing::error!("客户端重连失败，原因：{}，剩余尝试 {} 次", e, c);
-        },
-    )
-    .await
+        after_login(client).await?;
+
+        tracing::info!("客户端重连成功");
+        Ok(Some(alive))
+    };
+    let retry_closure = || async move { retry_closure().await.map_err(|e| (uin, e)) };
+    retry_closure
+        .retry(&retry_builder)
+        .notify(|e, dur: Duration| {
+            tracing::error!(
+                "客户端 {} 重连失败，原因：{}，将在 {:.2} 秒后重试",
+                e.0,
+                e.1,
+                dur.as_secs_f64()
+            );
+        })
+        .await
+        .map_err(|e| e.1)
 }
 
 async fn make_password_login_req(
     uin: i64,
     client: &Client,
     credential: &PasswordCredential,
 ) -> ricq::RQResult<LoginResponse> {
@@ -350,16 +436,42 @@
             }
         }
     }
 
     Ok(())
 }
 
+
+async fn after_login(client: &Arc<Client>) -> PyResult<()> {
+    client
+        .register_client()
+        .await
+        .map_err(|e| exc::RICQError::new_err(format!("注册客户端失败: {e:?}")))?;
+
+    if !client
+        .heartbeat_enabled
+        .load(std::sync::atomic::Ordering::Relaxed)
+    {
+        let client = client.clone();
+        tokio::spawn(async move {
+            client.do_heartbeat().await;
+        });
+    }
+
+    client
+        .refresh_status()
+        .await
+        .map_err(|e| exc::RICQError::new_err(format!("刷新状态失败: {e:?}")))?;
+
+    Ok(())
+}
+
 async fn post_login(client: Arc<Client>, alive: JoinHandle<()>, token_rw: TokenRW) -> PyRet {
-    after_login(&client).await;
+    after_login(&client).await?;
+
     token_rw.set(&client).await?;
     let uin = client.uin().await;
     let init = crate::client::ClientInitializer {
         uin,
         client,
         alive: Arc::new(std::sync::Mutex::new(Some(alive))),
         token_rw,
```

### Comparing `ichika-0.0.5/src/loguru.rs` & `ichika-0.0.6/src/loguru.rs`

 * *Files 1% similar despite different names*

```diff
@@ -22,15 +22,15 @@
     let layer = LoguruLayer::new()?;
     tracing_subscriber::registry()
         .with(layer)
         .with(
             // 筛选不同包的日志级别
             tracing_subscriber::filter::Targets::new()
                 .with_target("ricq", Level::DEBUG)
-                .with_target("core", Level::DEBUG),
+                .with_target("ichika", Level::DEBUG),
         )
         .init();
     // 注入 getframe
     Python::with_gil(|py| -> PyResult<()> {
         let logger_module = py.import("loguru")?.getattr("_logger")?;
         logger_module.setattr("get_frame", module.getattr("_getframe")?)
     })?;
@@ -62,22 +62,26 @@
     fn on_event(&self, event: &tracing::Event, _ctx: tracing_subscriber::layer::Context<'_, S>) {
         // 记录日志发生的位置，保存为伪 Python 堆栈
         Python::with_gil(|py| {
             if let Ok(mut frame) = LAST_RUST_FRAME
                 .get_or_init(py, || Arc::new(std::sync::RwLock::new(None)))
                 .write()
             {
+                let meta = event.metadata();
+
                 *frame = FakePyFrame::new(
-                    event
-                        .metadata()
+                    &meta
                         .module_path()
-                        .unwrap_or_else(|| event.metadata().target()),
-                    event.metadata().file().unwrap_or("<rust>"),
-                    "",
-                    event.metadata().line().unwrap_or(0),
+                        .unwrap_or_else(|| event.metadata().target())
+                        .split("::")
+                        .collect::<Vec<_>>()
+                        .join("."),
+                    meta.file().unwrap_or("<rust>"),
+                    "<rust>",
+                    meta.line().unwrap_or(0),
                 )
                 .ok();
             }
         });
 
         let message = {
             let mut visiter = LoguruVisiter::new();
```

### Comparing `ichika-0.0.5/src/message/convert.rs` & `ichika-0.0.6/src/message/convert.rs`

 * *Files 5% similar despite different names*

```diff
@@ -211,17 +211,26 @@
     Ok(py_fn
         .call1((serialize_message_chain(py, chain)?,))?
         .into_py(py))
 }
 
 pub fn deserialize_element(chain: &mut MessageChain, ident: &str, store: &PyAny) -> PyResult<()> {
     match ident {
-        "AtAll" => chain.push(At::new(0)),
+        "AtAll" => chain.push(At {
+            target: 0,
+            display: "@全体成员".into(),
+        }),
         "At" => {
-            chain.push(At::new(store.get_item("target")?.extract::<i64>()?));
+            let target = store.get_item("target")?.extract::<i64>()?;
+            let display = store
+                .get_item("display")?
+                .extract::<String>()
+                .ok()
+                .unwrap_or_else(|| format!("@{target}"));
+            chain.push(At { target, display });
         }
         "Text" => {
             chain.push(Text::new(store.get_item("text")?.extract::<String>()?));
         }
         "Dice" => {
             chain.push(Dice::new(store.get_item("value")?.extract::<i32>()?));
         }
```

### Comparing `ichika-0.0.5/src/message/elements.rs` & `ichika-0.0.6/src/message/elements.rs`

 * *Files identical despite different names*

### Comparing `ichika-0.0.5/src/utils.rs` & `ichika-0.0.6/src/utils.rs`

 * *Files 8% similar despite different names*

```diff
@@ -89,38 +89,14 @@
 where
     F: Future<Output = Result<T, crate::exc::Error>> + Send + 'static,
     T: IntoPy<PyObject>,
 {
     pyo3_asyncio::tokio::future_into_py(py, async move { future.await.map_err(|e| e.into()) })
 }
 
-/// 自动重试直到得到 `Ok(..)`。
-pub async fn py_retry<F, T, D>(
-    mut max_count: usize,
-    mut f: impl FnMut() -> F,
-    mut on_retry: impl FnMut(PyErr, usize) -> D,
-) -> PyResult<T>
-where
-    F: Future<Output = PyResult<T>>,
-    D: Future<Output = ()>,
-{
-    loop {
-        match f().await {
-            Ok(t) => return Ok(t),
-            Err(e) => {
-                if max_count == 0 {
-                    return Err(e);
-                }
-                max_count -= 1;
-                on_retry(e, max_count).await;
-            }
-        }
-    }
-}
-
 pub fn py_try<F, R>(f: F) -> PyResult<R>
 where
     F: for<'py> FnOnce(Python<'py>) -> PyResult<R>,
 {
     Python::with_gil(f)
 }
 
@@ -193,14 +169,47 @@
 static_py_fn!(
     py_client_refs,
     __CLIENT_WEAKREFS_CELL,
     "ichika.client",
     ["CLIENT_REFS"]
 );
 
+static_py_fn!(
+    _to_py_gender,
+    __PY_GENDER_ENUM_CELL,
+    "ichika.structs",
+    ["Gender"]
+);
+
+pub fn to_py_gender(gender: u8) -> PyObject {
+    let gender_str = match gender {
+        0 => "Male",
+        1 => "Female",
+        _ => "Unknown",
+    };
+    py_use(|py| _to_py_gender(py).call1((gender_str,)).unwrap().into_py(py))
+}
+
+static_py_fn!(
+    _to_py_perm,
+    __PY_GROUP_PERMISSION_CELL,
+    "ichika.structs",
+    ["GroupPermission"]
+);
+
+pub fn to_py_permission(perm: ricq_core::structs::GroupMemberPermission) -> PyObject {
+    use ricq_core::structs::GroupMemberPermission as Perm;
+    let perm_str = match perm {
+        Perm::Owner => "Owner",
+        Perm::Administrator => "Admin",
+        Perm::Member => "Member",
+    };
+    py_use(|py| _to_py_perm(py).call1((perm_str,)).unwrap().into_py(py))
+}
+
 #[macro_export]
 macro_rules! dict_obj {
     {$py:ident ! $($key:ident : $val:expr),* $(,)?} => {
         ::pyo3::Python::with_gil(|$py| -> ::pyo3::PyResult<_> {
             let dict = ::pyo3::types::PyDict::new($py);
             $(
                 let _val: ::pyo3::PyObject = $val.into_py($py);
```

### Comparing `ichika-0.0.5/Cargo.lock` & `ichika-0.0.6/Cargo.lock`

 * *Files 2% similar despite different names*

```diff
@@ -57,14 +57,26 @@
 [[package]]
 name = "autocfg"
 version = "1.1.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "d468802bab17cbc0cc575e9b053f41e72aa36bfa6b7f55e3529ffa43161b97fa"
 
 [[package]]
+name = "backon"
+version = "0.4.0"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "f34fac4d7cdaefa2deded0eda2d5d59dbfd43370ff3f856209e72340ae84c294"
+dependencies = [
+ "futures",
+ "pin-project",
+ "rand",
+ "tokio",
+]
+
+[[package]]
 name = "base16ct"
 version = "0.1.1"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "349a06037c7bf932dd7e7d1f653678b2038b9ad46a74102f1fc7bd7872678cce"
 
 [[package]]
 name = "bit_field"
@@ -75,14 +87,23 @@
 [[package]]
 name = "bitflags"
 version = "1.3.2"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "bef38d45163c2f1dde094a7dfd33ccf595c92905c8f8f4fdc18d06fb1037718a"
 
 [[package]]
+name = "block-buffer"
+version = "0.10.4"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "3078c7629b62d3f0439517fa394996acacc5cbc91c5a20d8c658e77abd503a71"
+dependencies = [
+ "generic-array",
+]
+
+[[package]]
 name = "built"
 version = "0.6.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "96f9cdd34d6eb553f9ea20e5bf84abb7b13c729f113fc1d8e49dc00ad9fa8738"
 dependencies = [
  "cargo-lock",
  "chrono",
@@ -190,14 +211,23 @@
 [[package]]
 name = "core-foundation-sys"
 version = "0.8.4"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "e496a50fda8aacccc86d7529e2c1e0892dbd0f898a6b5645b5561b89c3210efa"
 
 [[package]]
+name = "cpufeatures"
+version = "0.2.7"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "3e4c1eaa2012c47becbbad2ab175484c2a84d1185b566fb2cc5b8707343dfe58"
+dependencies = [
+ "libc",
+]
+
+[[package]]
 name = "crc32fast"
 version = "1.3.2"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "b540bd8bc810d3885c6ea91e2018302f68baba2129ab3e88f32389ee9370880d"
 dependencies = [
  "cfg-if",
 ]
@@ -260,14 +290,24 @@
  "generic-array",
  "rand_core",
  "subtle",
  "zeroize",
 ]
 
 [[package]]
+name = "crypto-common"
+version = "0.1.6"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "1bfb12502f3fc46cca1bb51ac28df9d618d813cdc3d2f25b9fe775a34af26bb3"
+dependencies = [
+ "generic-array",
+ "typenum",
+]
+
+[[package]]
 name = "ctor"
 version = "0.2.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "dd4056f63fce3b82d852c3da92b08ea59959890813a7f4ce9c0ff85b10cf301b"
 dependencies = [
  "quote",
  "syn 2.0.15",
@@ -334,14 +374,24 @@
 dependencies = [
  "proc-macro2",
  "quote",
  "syn 1.0.109",
 ]
 
 [[package]]
+name = "digest"
+version = "0.10.6"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "8168378f4e5023e7218c89c891c0fd8ecdb5e5e4f18cb78f38cf245dd021e76f"
+dependencies = [
+ "block-buffer",
+ "crypto-common",
+]
+
+[[package]]
 name = "either"
 version = "1.8.1"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "7fcaabb2fef8c910e7f4c7ce9f67a1283a1715879a7c230ca9d6d1ae31f16d91"
 
 [[package]]
 name = "elliptic-curve"
@@ -712,33 +762,36 @@
 dependencies = [
  "cxx",
  "cxx-build",
 ]
 
 [[package]]
 name = "ichika"
-version = "0.0.5"
+version = "0.0.6"
 dependencies = [
  "async-trait",
+ "backon",
  "built",
  "bytes",
  "futures-util",
  "hex",
  "image 0.24.6",
+ "lru_time_cache",
  "once_cell",
  "pyo3",
  "pyo3-asyncio",
  "pyo3-repr",
  "pythonize",
  "qrcode",
  "ricq",
  "ricq-core",
  "rqrr",
  "serde",
  "serde_json",
+ "t544_enc",
  "tokio",
  "tokio-stream",
  "tokio-util",
  "tracing",
  "tracing-subscriber",
 ]
 
@@ -943,14 +996,20 @@
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "71e7d46de488603ffdd5f30afbc64fbba2378214a2c3a2fb83abf3d33126df17"
 dependencies = [
  "hashbrown 0.13.2",
 ]
 
 [[package]]
+name = "lru_time_cache"
+version = "0.11.11"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "9106e1d747ffd48e6be5bb2d97fa706ed25b144fbee4d5c02eae110cd8d6badd"
+
+[[package]]
 name = "md5"
 version = "0.7.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "490cc448043f947bae3cbee9c203358d62dbee0db12107a74be5c30ccfd09771"
 
 [[package]]
 name = "memchr"
@@ -1467,15 +1526,15 @@
 version = "0.6.29"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "f162c6dd7b008981e4d40210aca20b4bd0f9b60ca9271061b07f78537722f2e1"
 
 [[package]]
 name = "ricq"
 version = "0.1.20"
-source = "git+https://github.com/BlueGlassBlock/ricq.git?branch=ichika-snapshot#637203cbd700626905cb089fc38bd056769abe9c"
+source = "git+https://github.com/BlueGlassBlock/ricq.git?branch=ichika-snapshot#ef8f04b90abe22c612ad5ecf3ee7f2d3c998400d"
 dependencies = [
  "async-trait",
  "bytes",
  "cached",
  "derivative",
  "flate2",
  "futures-util",
@@ -1490,29 +1549,30 @@
  "tokio-util",
  "tracing",
 ]
 
 [[package]]
 name = "ricq-core"
 version = "0.1.20"
-source = "git+https://github.com/BlueGlassBlock/ricq.git?branch=ichika-snapshot#637203cbd700626905cb089fc38bd056769abe9c"
+source = "git+https://github.com/BlueGlassBlock/ricq.git?branch=ichika-snapshot#ef8f04b90abe22c612ad5ecf3ee7f2d3c998400d"
 dependencies = [
  "byteorder",
  "bytes",
  "derivative",
  "flate2",
  "generic-array",
  "jcers",
  "md5",
  "p256",
  "prost",
  "prost-build",
  "prost-types",
  "rand",
  "serde",
+ "sha2",
  "thiserror",
 ]
 
 [[package]]
 name = "rqrr"
 version = "0.6.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
@@ -1574,26 +1634,26 @@
 checksum = "bebd363326d05ec3e2f532ab7660680f3b02130d780c299bca73469d521bc0ed"
 dependencies = [
  "serde",
 ]
 
 [[package]]
 name = "serde"
-version = "1.0.160"
+version = "1.0.162"
 source = "registry+https://github.com/rust-lang/crates.io-index"
-checksum = "bb2f3770c8bce3bcda7e149193a069a0f4365bda1fa5cd88e03bca26afc1216c"
+checksum = "71b2f6e1ab5c2b98c05f0f35b236b22e8df7ead6ffbf51d7808da7f8817e7ab6"
 dependencies = [
  "serde_derive",
 ]
 
 [[package]]
 name = "serde_derive"
-version = "1.0.160"
+version = "1.0.162"
 source = "registry+https://github.com/rust-lang/crates.io-index"
-checksum = "291a097c63d8497e00160b166a967a4a79c64f3facdd01cbd7502231688d77df"
+checksum = "a2a0814352fd64b58489904a44ea8d90cb1a91dcb6b4f5ebabc32c8318e93cb6"
 dependencies = [
  "proc-macro2",
  "quote",
  "syn 2.0.15",
 ]
 
 [[package]]
@@ -1604,14 +1664,25 @@
 dependencies = [
  "itoa",
  "ryu",
  "serde",
 ]
 
 [[package]]
+name = "sha2"
+version = "0.10.6"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "82e6b795fe2e3b1e845bafcb27aa35405c4d47cdfc92af5fc8d3002f76cebdc0"
+dependencies = [
+ "cfg-if",
+ "cpufeatures",
+ "digest",
+]
+
+[[package]]
 name = "sharded-slab"
 version = "0.1.4"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "900fba806f70c630b0a382d0d825e17a0f19fcd059a2ade1ff237bcddf446b31"
 dependencies = [
  "lazy_static",
 ]
@@ -1681,14 +1752,18 @@
 dependencies = [
  "proc-macro2",
  "quote",
  "unicode-ident",
 ]
 
 [[package]]
+name = "t544_enc"
+version = "0.1.0"
+
+[[package]]
 name = "target-lexicon"
 version = "0.12.6"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "8ae9980cab1db3fceee2f6c6f643d5d8de2997c58ee8d25fb0cc8a9e9e7348e5"
 
 [[package]]
 name = "tempfile"
```

### Comparing `ichika-0.0.5/PKG-INFO` & `ichika-0.0.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ichika
-Version: 0.0.5
+Version: 0.0.6
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Classifier: Natural Language :: Chinese (Simplified)
 Classifier: Programming Language :: Rust
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Topic :: Communications
 Classifier: Programming Language :: Python :: 3
```

