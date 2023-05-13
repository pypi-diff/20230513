# Comparing `tmp/qg-botsdk-2.6.3.tar.gz` & `tmp/qg-botsdk-2.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "qg-botsdk-2.6.3.tar", last modified: Sun Feb 26 11:45:36 2023, max compression
+gzip compressed data, was "qg-botsdk-2.7.0.tar", last modified: Sat May 13 10:11:34 2023, max compression
```

## Comparing `qg-botsdk-2.6.3.tar` & `qg-botsdk-2.7.0.tar`

### file list

```diff
@@ -1,29 +1,29 @@
-drwxrwxrwx   0        0        0        0 2023-02-26 11:45:36.517131 qg-botsdk-2.6.3/
--rw-rw-rw-   0        0        0     1083 2022-05-05 08:39:00.000000 qg-botsdk-2.6.3/LICENSE
--rw-rw-rw-   0        0        0     7058 2023-02-26 11:45:36.517131 qg-botsdk-2.6.3/PKG-INFO
--rw-rw-rw-   0        0        0     6695 2023-01-06 03:21:47.000000 qg-botsdk-2.6.3/README.md
--rw-rw-rw-   0        0        0     6511 2023-01-06 03:21:47.000000 qg-botsdk-2.6.3/README.rst
-drwxrwxrwx   0        0        0        0 2023-02-26 11:45:36.513147 qg-botsdk-2.6.3/qg_botsdk/
--rw-rw-rw-   0        0        0      979 2023-01-14 05:41:49.000000 qg-botsdk-2.6.3/qg_botsdk/__init__.py
--rw-rw-rw-   0        0        0    22680 2023-01-14 05:41:49.000000 qg-botsdk-2.6.3/qg_botsdk/_api_model.py
--rw-rw-rw-   0        0        0      616 2023-02-05 14:08:39.000000 qg-botsdk-2.6.3/qg_botsdk/_queue.py
--rw-rw-rw-   0        0        0     1394 2023-01-05 02:29:18.000000 qg-botsdk-2.6.3/qg_botsdk/_statics.py
--rw-rw-rw-   0        0        0    13382 2023-02-26 07:33:31.000000 qg-botsdk-2.6.3/qg_botsdk/_utils.py
--rw-rw-rw-   0        0        0    44968 2023-01-20 12:42:23.000000 qg-botsdk-2.6.3/qg_botsdk/api.py
--rw-rw-rw-   0        0        0    73362 2023-01-20 12:42:23.000000 qg-botsdk-2.6.3/qg_botsdk/async_api.py
--rw-rw-rw-   0        0        0     5179 2023-02-26 11:45:25.000000 qg-botsdk-2.6.3/qg_botsdk/http.py
--rw-rw-rw-   0        0        0     6471 2023-01-14 05:41:49.000000 qg-botsdk-2.6.3/qg_botsdk/logger.py
--rw-rw-rw-   0        0        0    19717 2023-01-14 05:41:49.000000 qg-botsdk-2.6.3/qg_botsdk/model.py
--rw-rw-rw-   0        0        0     5678 2023-01-20 12:15:55.000000 qg-botsdk-2.6.3/qg_botsdk/plugins.py
--rw-rw-rw-   0        0        0    29080 2023-02-26 07:35:09.000000 qg-botsdk-2.6.3/qg_botsdk/qg_bot.py
--rw-rw-rw-   0        0        0    17827 2023-02-26 11:45:25.000000 qg-botsdk-2.6.3/qg_botsdk/qg_bot_ws.py
--rw-rw-rw-   0        0        0     1974 2023-01-14 05:41:49.000000 qg-botsdk-2.6.3/qg_botsdk/utils.py
--rw-rw-rw-   0        0        0       23 2023-01-20 12:40:07.000000 qg-botsdk-2.6.3/qg_botsdk/version.py
-drwxrwxrwx   0        0        0        0 2023-02-26 11:45:36.516135 qg-botsdk-2.6.3/qg_botsdk.egg-info/
--rw-rw-rw-   0        0        0     7058 2023-02-26 11:45:36.000000 qg-botsdk-2.6.3/qg_botsdk.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      520 2023-02-26 11:45:36.000000 qg-botsdk-2.6.3/qg_botsdk.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-02-26 11:45:36.000000 qg-botsdk-2.6.3/qg_botsdk.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-02-26 11:45:36.000000 qg-botsdk-2.6.3/qg_botsdk.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-02-26 11:45:36.000000 qg-botsdk-2.6.3/qg_botsdk.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      398 2023-02-26 11:45:36.518132 qg-botsdk-2.6.3/setup.cfg
--rw-rw-rw-   0        0        0      538 2022-10-15 14:51:31.000000 qg-botsdk-2.6.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:11:34.566653 qg-botsdk-2.7.0/
+-rw-rw-rw-   0        0        0     1083 2022-05-05 08:39:00.000000 qg-botsdk-2.7.0/LICENSE
+-rw-rw-rw-   0        0        0     7103 2023-05-13 10:11:34.566653 qg-botsdk-2.7.0/PKG-INFO
+-rw-rw-rw-   0        0        0     6740 2023-05-13 08:46:52.000000 qg-botsdk-2.7.0/README.md
+-rw-rw-rw-   0        0        0     6556 2023-05-13 08:47:07.000000 qg-botsdk-2.7.0/README.rst
+drwxrwxrwx   0        0        0        0 2023-05-13 10:11:34.559653 qg-botsdk-2.7.0/qg_botsdk/
+-rw-rw-rw-   0        0        0      980 2023-03-30 14:45:13.000000 qg-botsdk-2.7.0/qg_botsdk/__init__.py
+-rw-rw-rw-   0        0        0    23008 2023-05-13 09:58:12.000000 qg-botsdk-2.7.0/qg_botsdk/_api_model.py
+-rw-rw-rw-   0        0        0      616 2023-02-05 14:08:39.000000 qg-botsdk-2.7.0/qg_botsdk/_queue.py
+-rw-rw-rw-   0        0        0     1394 2023-01-05 02:29:18.000000 qg-botsdk-2.7.0/qg_botsdk/_statics.py
+-rw-rw-rw-   0        0        0    13382 2023-02-26 07:33:31.000000 qg-botsdk-2.7.0/qg_botsdk/_utils.py
+-rw-rw-rw-   0        0        0    47093 2023-05-13 10:04:40.000000 qg-botsdk-2.7.0/qg_botsdk/api.py
+-rw-rw-rw-   0        0        0    73647 2023-05-13 10:04:03.000000 qg-botsdk-2.7.0/qg_botsdk/async_api.py
+-rw-rw-rw-   0        0        0     5179 2023-02-26 11:45:25.000000 qg-botsdk-2.7.0/qg_botsdk/http.py
+-rw-rw-rw-   0        0        0     6471 2023-01-14 05:41:49.000000 qg-botsdk-2.7.0/qg_botsdk/logger.py
+-rw-rw-rw-   0        0        0    19717 2023-01-14 05:41:49.000000 qg-botsdk-2.7.0/qg_botsdk/model.py
+-rw-rw-rw-   0        0        0     5522 2023-05-13 09:58:12.000000 qg-botsdk-2.7.0/qg_botsdk/plugins.py
+-rw-rw-rw-   0        0        0    27014 2023-05-13 10:04:26.000000 qg-botsdk-2.7.0/qg_botsdk/qg_bot.py
+-rw-rw-rw-   0        0        0    17604 2023-05-13 09:58:09.000000 qg-botsdk-2.7.0/qg_botsdk/qg_bot_ws.py
+-rw-rw-rw-   0        0        0     1974 2023-01-14 05:41:49.000000 qg-botsdk-2.7.0/qg_botsdk/utils.py
+-rw-rw-rw-   0        0        0       23 2023-05-13 10:09:25.000000 qg-botsdk-2.7.0/qg_botsdk/version.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:11:34.565665 qg-botsdk-2.7.0/qg_botsdk.egg-info/
+-rw-rw-rw-   0        0        0     7103 2023-05-13 10:11:34.000000 qg-botsdk-2.7.0/qg_botsdk.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      520 2023-05-13 10:11:34.000000 qg-botsdk-2.7.0/qg_botsdk.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 10:11:34.000000 qg-botsdk-2.7.0/qg_botsdk.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-05-13 10:11:34.000000 qg-botsdk-2.7.0/qg_botsdk.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 10:11:34.000000 qg-botsdk-2.7.0/qg_botsdk.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      381 2023-05-13 10:11:34.567654 qg-botsdk-2.7.0/setup.cfg
+-rw-rw-rw-   0        0        0      607 2023-05-13 10:11:18.000000 qg-botsdk-2.7.0/setup.py
```

### Comparing `qg-botsdk-2.6.3/LICENSE` & `qg-botsdk-2.7.0/LICENSE`

 * *Files identical despite different names*

### Comparing `qg-botsdk-2.6.3/PKG-INFO` & `qg-botsdk-2.7.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: qg-botsdk
-Version: 2.6.3
+Version: 2.7.0
 Summary: easy-to-use SDK for Tencent QQ guild robot
 Home-page: https://github.com/GLGDLY/qg_botsdk
 Author: GDLY
 Author-email: tzlgdly@gmail.com
 Keywords: sample,example,setuptools
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
@@ -41,15 +41,15 @@
 
 
 亮点
 =====
 
 -   灵活的构建方式，即使官方删除或新增字段，SDK也不会规范于原来的数据格式，而会把真实数据反馈给你
 
--   轻量，简洁，统一的代码结构，10行即可构建一个简单的程序
+-   轻量，简洁，统一的代码结构，通过录入回调函数处理不同事件，10行即可构建一个简单的程序
 
 -   容易入门，无需学会asyncio、类继承等编程技巧也可使用，同时保留较高并发能力
 
 -   保留官方http API中Json数据的结构字段，带你学习官方结构，日后可自行开发适合自己的SDK
 
 -   迅速的更新速度，跟上最新潮流（v2.5.5已更新音视频/直播子频道成员进出事件、公域论坛事件）
```

### Comparing `qg-botsdk-2.6.3/README.md` & `qg-botsdk-2.7.0/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -26,15 +26,15 @@
 为此，qg_botsdk相应提供了另一个选择，这一款sdk虽然同样使用asyncio编写sdk底层，但其同时提供了threading和asyncio封装下的应用层调用，以抽象化封装的库编写方式，极大地降低应用层的开发难度。 
 
 
 #### 亮点
 
 ##### -   灵活的构建方式，即使官方删除或新增字段，SDK也不会规范于原来的数据格式，而会把真实数据反馈给你
 
-##### -   轻量，简洁，统一的代码结构，10行即可构建一个简单的程序
+##### -   轻量，简洁，统一的代码结构，通过录入回调函数处理不同事件，10行即可构建一个简单的程序
 
 ##### -   容易入门，无需学会asyncio、类继承等编程技巧也可使用，同时保留较高并发能力
 
 ##### -   保留官方http API中Json数据的结构字段，带你学习官方结构，日后可自行开发适合自己的SDK
 
 ##### -   迅速的更新速度，跟上最新潮流（v2.5.5已更新音视频/直播子频道成员进出事件、公域论坛事件）
```

### Comparing `qg-botsdk-2.6.3/README.rst` & `qg-botsdk-2.7.0/README.rst`

 * *Files 2% similar despite different names*

```diff
@@ -25,15 +25,15 @@
 
 
 亮点
 =====
 
 -   灵活的构建方式，即使官方删除或新增字段，SDK也不会规范于原来的数据格式，而会把真实数据反馈给你
 
--   轻量，简洁，统一的代码结构，10行即可构建一个简单的程序
+-   轻量，简洁，统一的代码结构，通过录入回调函数处理不同事件，10行即可构建一个简单的程序
 
 -   容易入门，无需学会asyncio、类继承等编程技巧也可使用，同时保留较高并发能力
 
 -   保留官方http API中Json数据的结构字段，带你学习官方结构，日后可自行开发适合自己的SDK
 
 -   迅速的更新速度，跟上最新潮流（v2.5.5已更新音视频/直播子频道成员进出事件、公域论坛事件）
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk/__init__.py` & `qg-botsdk-2.7.0/qg_botsdk/__init__.py`

 * *Files 10% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 
 from .logger import Logger
 from .model import EmojiID, EmojiString, Model
 from .plugins import Plugins
 from .qg_bot import BOT
 from .version import __version__
 
-__title__ = "requests"
+__title__ = "qg_botsdk"
 __description__ = "easy-to-use SDK for Tencent QQ guild robot"
 __url__ = "https://github.com/GLGDLY/qg_botsdk"
 __author__ = "GDLY"
 __author_email__ = "tzlgdly@gmail.com"
 __license__ = "MIT"
 __copyright__ = "Copyright (c) 2022 GLGDLY"
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk/_api_model.py` & `qg-botsdk-2.7.0/qg_botsdk/_api_model.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,27 @@
 #!/usr/bin/env python3
 # -*- coding: utf-8 -*-
-from typing import List, Optional
+from re import Pattern
+from typing import List, Optional, TypedDict
 
 from ._utils import object_class
+from .model import Model
+
+
+class Bot_Command_Obj(TypedDict, total=False):
+    command: list[str]
+    regex: Pattern
+    func: Model.MESSAGE
+    treat: bool
+    at: bool
+    short_circuit: bool
+    is_custom_short_circuit: bool
+    admin: bool
+    admin_error_msg: Optional[str]
+
 
 apis = {
     ("获取用户ID", "get_bot_id"): [False, "此API不需要请求权限"],
     ("获取用户信息", "get_bot_info"): ["GET", "/users/@me"],
     ("获取用户频道列表", "get_bot_guilds"): ["GET", "/users/@me/guilds"],
     ("获取频道详情", "get_guild_info"): ["GET", "/guilds/{guild_id}"],
     ("获取子频道列表", "get_guild_channels"): ["GET", "/guilds/{guild_id}/channels"],
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk/_queue.py` & `qg-botsdk-2.7.0/qg_botsdk/_queue.py`

 * *Files identical despite different names*

### Comparing `qg-botsdk-2.6.3/qg_botsdk/_statics.py` & `qg-botsdk-2.7.0/qg_botsdk/_statics.py`

 * *Files identical despite different names*

### Comparing `qg-botsdk-2.6.3/qg_botsdk/_utils.py` & `qg-botsdk-2.7.0/qg_botsdk/_utils.py`

 * *Files identical despite different names*

### Comparing `qg-botsdk-2.6.3/qg_botsdk/api.py` & `qg-botsdk-2.7.0/qg_botsdk/api.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,34 +1,42 @@
 #!/usr/bin/env python3
 # -*- coding: utf-8 -*-
 from asyncio import AbstractEventLoop, run_coroutine_threadsafe
+from time import sleep
 from typing import BinaryIO, Dict, List, Optional, Tuple, Union
 
 from . import _api_model
 from .async_api import AsyncAPI
 
 
 class API:
     def __init__(self, api: AsyncAPI, loop: AbstractEventLoop):
         self._api = api
         self._loop = loop
 
+    def __check_ready(self):
+        if not self._loop.is_running():
+            raise RuntimeError(
+                "Event loop is not running，请先通过BOT()实例的start()或block()方法启动bot并运行事件循环"
+            )
+
     def security_setup(self, mini_id: str, mini_secret: str):
         self._api._mini_id = mini_id
         self._api._mini_secret = mini_secret
 
     def security_check(self, content: str) -> bool:
         """
         腾讯小程序侧内容安全检测接口，使用此接口必须填入bot_secret密钥
 
         :param content: 需要检测的内容
         :return: True或False（bool），代表是否通过安全检测
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.security_check(**_args), self._loop
         )
         return future_.result()
 
     @staticmethod
     def get_bot_id():
@@ -36,63 +44,69 @@
 
     def get_bot_info(self) -> _api_model.get_bot_info():
         """
         获取机器人详情
 
         :return:返回的.data中为解析后的json数据
         """
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.get_bot_info(), self._loop)
         return future_.result()
 
     def get_bot_guilds(self) -> _api_model.get_bot_guilds():
         """
         获取机器人所在的所有频道列表
 
         :return: 返回的.data中为包含所有数据的一个list，列表每个项均为object数据
         """
+        self.__check_ready()
+        print(self._loop.is_running())
         future_ = run_coroutine_threadsafe(self._api.get_bot_guilds(), self._loop)
         return future_.result()
 
     def get_guild_info(self, guild_id: str) -> _api_model.get_guild_info():
         """
         获取频道详情信息
 
         :param guild_id: 频道id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_guild_info(**_args), self._loop
         )
         return future_.result()
 
     def get_guild_channels(self, guild_id: str) -> _api_model.get_guild_channels():
         """
         获取频道的所有子频道列表数据
 
         :param guild_id: 频道id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_guild_channels(**_args), self._loop
         )
         return future_.result()
 
     def get_channels_info(self, channel_id: str) -> _api_model.get_channels_info():
         """
         获取子频道数据
 
         :param channel_id: 子频道id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_channels_info(**_args), self._loop
         )
         return future_.result()
 
     def create_channels(
         self,
@@ -120,14 +134,15 @@
         :param private_user_ids: 需要创建的子频道私密类型成员ID列表
         :param speak_permission: 需要创建的子频道发言权限
         :param application_id: 需要创建的应用类型子频道应用 AppID，仅应用子频道需要该字段
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.create_channels(**_args), self._loop
         )
         return future_.result()
 
     def patch_channels(
         self,
@@ -147,42 +162,45 @@
         :param parent_id: 子频道所属分组id
         :param private_type: 子频道私密类型
         :param speak_permission: 子频道发言权限
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.patch_channels(**_args), self._loop
         )
         return future_.result()
 
     def delete_channels(self, channel_id) -> _api_model.delete_channels():
         """
         用于删除 channel_id 指定的子频道
 
         :param channel_id: 子频道id
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.delete_channels(**_args), self._loop
         )
         return future_.result()
 
     def get_guild_members(self, guild_id: str) -> _api_model.get_guild_members():
         """
         用于获取 guild_id 指定的频道中所有成员的详情列表
 
         :param guild_id: 频道id
         :return: 返回的.data中为包含所有数据的一个list，列表每个项均为object数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_guild_members(**_args), self._loop
         )
         return future_.result()
 
     def get_role_members(
         self, guild_id: str, role_id: str
@@ -192,14 +210,15 @@
 
         :param guild_id: 频道id
         :param role_id: 身份组id
         :return: 返回的.data中为包含所有数据的一个list，列表每个项均为object数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_role_members(**_args), self._loop
         )
         return future_.result()
 
     def get_member_info(
         self, guild_id: str, user_id: str
@@ -209,14 +228,15 @@
 
         :param guild_id: 频道id
         :param user_id: 成员id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_member_info(**_args), self._loop
         )
         return future_.result()
 
     def delete_member(
         self,
@@ -232,26 +252,28 @@
         :param user_id: 目标用户ID
         :param add_blacklist: 是否同时添加黑名单
         :param delete_history_msg_days: 用于撤回该成员的消息，可以指定撤回消息的时间范围
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.delete_member(**_args), self._loop)
         return future_.result()
 
     def get_guild_roles(self, guild_id: str) -> _api_model.get_guild_roles():
         """
         用于获取 guild_id指定的频道下的身份组列表
 
         :param guild_id: 频道id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_guild_roles(**_args), self._loop
         )
         return future_.result()
 
     def create_role(
         self,
@@ -267,14 +289,15 @@
         :param name: 身份组名（选填)
         :param hoist: 是否在成员列表中单独展示（选填）
         :param color: 身份组颜色，支持输入RGB的三位tuple或HEX的sting颜色（选填)
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.create_role(**_args), self._loop)
         return future_.result()
 
     def patch_role(
         self,
         guild_id: str,
         role_id: str,
@@ -290,27 +313,29 @@
         :param name: 身份组名（选填)
         :param hoist: 是否在成员列表中单独展示（选填）
         :param color: 身份组颜色，支持输入RGB的三位tuple或HEX的sting颜色（选填)
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.patch_role(**_args), self._loop)
         return future_.result()
 
     def delete_role(self, guild_id: str, role_id: str) -> _api_model.delete_role():
         """
         用于删除频道 guild_id下 role_id 对应的身份组
 
         :param guild_id: 频道ID
         :param role_id: 需要删除的身份组ID
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.delete_role(**_args), self._loop)
         return future_.result()
 
     def create_role_member(
         self,
         user_id: str,
         guild_id: str,
@@ -324,14 +349,15 @@
         :param guild_id: 目标频道guild id
         :param role_id: 身份组编号，可从例如get_roles函数获取
         :param channel_id: 如果要增加的身份组ID是5-子频道管理员，需要输入此项来指定具体是哪个子频道
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.create_role_member(**_args), self._loop
         )
         return future_.result()
 
     def delete_role_member(
         self,
@@ -347,14 +373,15 @@
         :param guild_id: 目标频道guild id
         :param role_id: 身份组编号，可从例如get_roles函数获取
         :param channel_id: 如果要增加的身份组ID是5-子频道管理员，需要输入此项来指定具体是哪个子频道
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.delete_role_member(**_args), self._loop
         )
         return future_.result()
 
     def get_channel_member_permission(
         self, channel_id: str, user_id: str
@@ -364,14 +391,15 @@
 
         :param channel_id: 子频道id
         :param user_id: 用户id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_channel_member_permission(**_args), self._loop
         )
         return future_.result()
 
     def put_channel_member_permission(
         self,
@@ -387,14 +415,15 @@
         :param user_id: 用户id
         :param add: 需要添加的权限，string格式，可选：1，2，4，8
         :param remove:需要删除的权限，string格式，可选：1，2，4，8
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.put_channel_member_permission(**_args), self._loop
         )
         return future_.result()
 
     def get_channel_role_permission(
         self, channel_id: str, role_id: str
@@ -404,14 +433,15 @@
 
         :param channel_id: 子频道id
         :param role_id: 身份组id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_channel_role_permission(**_args), self._loop
         )
         return future_.result()
 
     def put_channel_role_permission(
         self,
@@ -427,14 +457,15 @@
         :param role_id: 身份组id
         :param add: 需要添加的权限，string格式，可选：1，2，4，8
         :param remove:需要删除的权限，string格式，可选：1，2，4，8
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.put_channel_role_permission(**_args), self._loop
         )
         return future_.result()
 
     def get_message_info(
         self, channel_id: str, message_id: str
@@ -444,14 +475,15 @@
 
         :param channel_id: 频道ID
         :param message_id: 目标消息ID
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_message_info(**_args), self._loop
         )
         return future_.result()
 
     def send_msg(
         self,
@@ -475,14 +507,15 @@
         :param event_id: 事件id（选填）
         :param message_reference_id: 引用消息的id（选填）
         :param ignore_message_reference_error: 是否忽略获取引用消息详情错误，默认否（选填）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.send_msg(**_args), self._loop)
         return future_.result()
 
     def send_embed(
         self,
         channel_id: str,
         title: Optional[str] = None,
@@ -502,14 +535,15 @@
         :param prompt: 消息弹窗通知的文本内容（选填）
         :param message_id: 消息id（选填）
         :param event_id: 事件id（选填）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.send_embed(**_args), self._loop)
         return future_.result()
 
     def send_ark_23(
         self,
         channel_id: str,
         content: List[str],
@@ -529,14 +563,15 @@
         :param prompt: 消息弹窗通知的文本内容（选填）
         :param message_id: 消息id（选填）
         :param event_id: 事件id（选填）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.send_ark_23(**_args), self._loop)
         return future_.result()
 
     def send_ark_24(
         self,
         channel_id: str,
         title: Optional[str] = None,
@@ -562,14 +597,15 @@
         :param prompt: 消息弹窗通知的文本内容（选填）
         :param message_id: 消息id（选填）
         :param event_id: 事件id（选填）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.send_ark_24(**_args), self._loop)
         return future_.result()
 
     def send_ark_37(
         self,
         channel_id: str,
         title: Optional[str] = None,
@@ -591,14 +627,15 @@
         :param prompt: 消息弹窗通知的文本内容（选填）
         :param message_id: 消息id（选填）
         :param event_id: 事件id（选填）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.send_ark_37(**_args), self._loop)
         return future_.result()
 
     def send_markdown(
         self,
         channel_id: str,
         template_id: Optional[str] = None,
@@ -624,14 +661,15 @@
         :param keyboard_content: 原生 keyboard 内容（选填，与keyboard_id不可同时存在）
         :param message_id: 消息id（选填）
         :param event_id: 事件id（选填）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.send_markdown(**_args), self._loop)
         return future_.result()
 
     def delete_msg(
         self, channel_id: str, message_id: str, hidetip: bool = False
     ) -> _api_model.delete_msg():
         """
@@ -640,26 +678,28 @@
         :param channel_id: 子频道id
         :param message_id: 需撤回消息的消息id
         :param hidetip: 是否隐藏提示小灰条，True为隐藏，False为显示（选填）
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.delete_msg(**_args), self._loop)
         return future_.result()
 
     def get_guild_setting(self, guild_id: str) -> _api_model.get_guild_setting():
         """
         用于获取机器人在频道 guild_id 内的消息频率设置
 
         :param guild_id: 频道id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_guild_setting(**_args), self._loop
         )
         return future_.result()
 
     def create_dm_guild(
         self, target_id: str, guild_id: str
@@ -669,14 +709,15 @@
 
         :param target_id: 目标用户id
         :param guild_id: 机器人跟目标用户所在的频道id
         :return: 返回的.data中为解析后的json数据，注意发送私信仅需要使用guild_id这一项虚拟频道id的数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.create_dm_guild(**_args), self._loop
         )
         return future_.result()
 
     def send_dm(
         self,
@@ -700,14 +741,15 @@
         :param event_id: 事件id（选填）
         :param message_reference_id: 引用消息的id（选填）
         :param ignore_message_reference_error: 是否忽略获取引用消息详情错误，默认否（选填）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.send_dm(**_args), self._loop)
         return future_.result()
 
     def delete_dm_msg(
         self, guild_id: str, message_id: str, hidetip: bool = False
     ) -> _api_model.delete_msg():
         """
@@ -716,14 +758,15 @@
         :param guild_id: 虚拟频道id（非子频道id），从用户主动私信机器人的事件、或机器人主动创建私信的API中获取
         :param message_id: 需撤回消息的消息id
         :param hidetip: 是否隐藏提示小灰条，True为隐藏，False为显示（选填）
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.delete_dm_msg(**_args), self._loop)
         return future_.result()
 
     def mute_all_member(
         self,
         guild_id: str,
         mute_end_timestamp: Optional[str],
@@ -735,14 +778,15 @@
         :param guild_id: 频道id
         :param mute_end_timestamp: 禁言到期时间戳，绝对时间戳，单位：秒（与 mute_seconds 字段同时赋值的话，以该字段为准）
         :param mute_seconds: 禁言多少秒（两个字段二选一，默认以 mute_end_timestamp 为准）
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.mute_all_member(**_args), self._loop
         )
         return future_.result()
 
     def mute_member(
         self,
@@ -758,14 +802,15 @@
         :param user_id: 目标成员的用户ID
         :param mute_end_timestamp: 禁言到期时间戳，绝对时间戳，单位：秒（与 mute_seconds 字段同时赋值的话，以该字段为准）
         :param mute_seconds: 禁言多少秒（两个字段二选一，默认以 mute_end_timestamp 为准）
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.mute_member(**_args), self._loop)
         return future_.result()
 
     def mute_members(
         self,
         guild_id: str,
         user_id: List[str],
@@ -779,14 +824,15 @@
         :param user_id: 目标成员的用户ID列表
         :param mute_end_timestamp: 禁言到期时间戳，绝对时间戳，单位：秒（与 mute_seconds 字段同时赋值的话，以该字段为准）
         :param mute_seconds: 禁言多少秒（两个字段二选一，默认以 mute_end_timestamp 为准）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.mute_members(**_args), self._loop)
         return future_.result()
 
     def create_announce(
         self,
         guild_id,
         channel_id: Optional[str] = None,
@@ -804,14 +850,15 @@
         :param announces_type: 公告类别 0：成员公告，1：欢迎公告，默认为成员公告
         :param recommend_channels_id: 推荐子频道id列表，会一次全部替换推荐子频道列表
         :param recommend_channels_introduce: 推荐子频道推荐语列表，列表长度应与recommend_channels_id一致
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.create_announce(**_args), self._loop
         )
         return future_.result()
 
     def delete_announce(
         self, guild_id: str, message_id: str = "all"
@@ -821,14 +868,15 @@
 
         :param guild_id: 频道id
         :param message_id: message_id有值时会校验message_id合法性；若不校验，请将message_id设置为all（默认为all）
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.delete_announce(**_args), self._loop
         )
         return future_.result()
 
     def create_pinmsg(self, channel_id: str, message_id: str) -> _api_model.pinmsg():
         """
@@ -836,14 +884,15 @@
 
         :param channel_id: 子频道id
         :param message_id: 目标消息id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.create_pinmsg(**_args), self._loop)
         return future_.result()
 
     def delete_pinmsg(
         self, channel_id: str, message_id: str
     ) -> _api_model.delete_pinmsg():
         """
@@ -851,26 +900,28 @@
 
         :param channel_id: 子频道id
         :param message_id: 目标消息id
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.delete_pinmsg(**_args), self._loop)
         return future_.result()
 
     def get_pinmsg(self, channel_id: str) -> _api_model.pinmsg():
         """
         用于获取子频道 channel_id 内的精华消息
 
         :param channel_id: 子频道id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.get_pinmsg(**_args), self._loop)
         return future_.result()
 
     def get_schedules(
         self, channel_id: str, since: Optional[int] = None
     ) -> _api_model.get_schedules():
         """
@@ -878,14 +929,15 @@
 
         :param channel_id: 日程子频道id
         :param since: 起始时间戳(ms)
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.get_schedules(**_args), self._loop)
         return future_.result()
 
     def get_schedule_info(
         self, channel_id: str, schedule_id: str
     ) -> _api_model.schedule_info():
         """
@@ -893,14 +945,15 @@
 
         :param channel_id: 日程子频道id
         :param schedule_id: 日程id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_schedule_info(**_args), self._loop
         )
         return future_.result()
 
     def create_schedule(
         self,
@@ -920,14 +973,15 @@
         :param end_timestamp: 日程结束时间戳(ms)
         :param jump_channel_id: 日程开始时跳转到的子频道id
         :param remind_type: 日程提醒类型
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.create_schedule(**_args), self._loop
         )
         return future_.result()
 
     def patch_schedule(
         self,
@@ -949,14 +1003,15 @@
         :param end_timestamp: 日程结束时间戳(ms)
         :param jump_channel_id: 日程开始时跳转到的子频道id
         :param remind_type: 日程提醒类型
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.patch_schedule(**_args), self._loop
         )
         return future_.result()
 
     def delete_schedule(
         self, channel_id: str, schedule_id: str
@@ -966,14 +1021,15 @@
 
         :param channel_id: 日程子频道id
         :param schedule_id: 日程id
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.delete_schedule(**_args), self._loop
         )
         return future_.result()
 
     def create_reaction(
         self, channel_id: str, message_id: str, type_: str, id_: str
@@ -985,14 +1041,15 @@
         :param message_id: 目标消息id
         :param type_: 表情类型
         :param id_: 表情id
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.create_reaction(**_args), self._loop
         )
         return future_.result()
 
     def delete_reaction(
         self, channel_id: str, message_id: str, type_: str, id_: str
@@ -1004,14 +1061,15 @@
         :param message_id: 目标消息id
         :param type_: 表情类型
         :param id_: 表情id
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.delete_reaction(**_args), self._loop
         )
         return future_.result()
 
     def get_reaction_users(
         self, channel_id: str, message_id: str, type_: str, id_: str
@@ -1023,14 +1081,15 @@
         :param message_id: 目标消息id
         :param type_: 表情类型
         :param id_: 表情id
         :return: 返回的.data中为解析后的json数据列表
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_reaction_users(**_args), self._loop
         )
         return future_.result()
 
     def control_audio(
         self,
@@ -1046,50 +1105,54 @@
         :param status: 播放状态
         :param audio_url: 音频数据的url，可选，status为0时传
         :param text: 状态文本（比如：简单爱-周杰伦），可选，status为0时传，其他操作不传
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.control_audio(**_args), self._loop)
         return future_.result()
 
     def bot_on_mic(self, channel_id: str) -> _api_model.audio():
         """
         机器人在 channel_id 对应的语音子频道上麦
 
         :param channel_id: 子频道id
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.bot_on_mic(**_args), self._loop)
         return future_.result()
 
     def bot_off_mic(self, channel_id: str) -> _api_model.audio():
         """
         机器人在 channel_id 对应的语音子频道下麦
 
         :param channel_id: 子频道id
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.bot_off_mic(**_args), self._loop)
         return future_.result()
 
     def get_threads(self, channel_id: str) -> _api_model.get_threads():
         """
         获取子频道下的帖子列表
 
         :param channel_id: 目标论坛子频道id
         :return: 返回的.data中为解析后的json数据列表
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.get_threads(**_args), self._loop)
         return future_.result()
 
     def get_thread_info(
         self, channel_id: str, thread_id: str
     ) -> _api_model.get_thread_info():
         """
@@ -1097,33 +1160,35 @@
 
         :param channel_id: 目标论坛子频道id
         :param thread_id: 帖子id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_thread_info(**_args), self._loop
         )
         return future_.result()
 
     def create_thread(
-        self, channel_id: str, title: str, content: str, format_: int
+        self, channel_id: str, title: str, content: Union[str, dict], format_: int
     ) -> _api_model.create_thread():
         """
         创建帖子，创建成功后，返回创建成功的任务ID
 
         :param channel_id: 目标论坛子频道id
         :param title: 帖子标题
         :param content: 帖子内容（具体格式根据format_判断）
         :param format_: 帖子文本格式（1：普通文本、2：HTML、3：Markdown、4：Json）
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.create_thread(**_args), self._loop)
         return future_.result()
 
     def delete_thread(
         self, channel_id: str, thread_id: str
     ) -> _api_model.delete_thread():
         """
@@ -1131,28 +1196,30 @@
 
         :param channel_id: 目标论坛子频道id
         :param thread_id: 帖子id
         :return: 返回的.result显示是否成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(self._api.delete_thread(**_args), self._loop)
         return future_.result()
 
     def get_guild_permissions(
         self, guild_id: str
     ) -> _api_model.get_guild_permissions():
         """
         获取机器人在频道 guild_id 内可以使用的权限列表
 
         :param guild_id: 频道id
         :return: 返回的.data中为解析后的json数据
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.get_guild_permissions(**_args), self._loop
         )
         return future_.result()
 
     def create_permission_demand(
         self, guild_id: str, channel_id: str, api: str, desc: Optional[str]
@@ -1164,11 +1231,12 @@
         :param channel_id: 子频道id
         :param api: 需求权限的API在sdk的名字
         :param desc: 机器人申请对应的API接口权限后可以使用功能的描述
         :return: 返回成功或不成功
         """
         _args = locals()
         _args.pop("self")
+        self.__check_ready()
         future_ = run_coroutine_threadsafe(
             self._api.create_permission_demand(**_args), self._loop
         )
         return future_.result()
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk/async_api.py` & `qg-botsdk-2.7.0/qg_botsdk/async_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python3
 # -*- coding: utf-8 -*-
 from io import BufferedReader
-from json import loads
+from json import dumps, loads
 from json.decoder import JSONDecodeError
 from os.path import exists
 from time import time
 from typing import BinaryIO, Dict, List, Optional, Tuple, Union
 
 from . import _api_model
 from ._utils import (
@@ -1713,27 +1713,32 @@
         self.check_warning("获取帖子详情")
         return_ = await self._session.get(
             f"{self.bot_url}/channels/{channel_id}/threads/{thread_id}"
         )
         return await regular_temp(return_)
 
     async def create_thread(
-        self, channel_id: str, title: str, content: str, format_: int
+        self, channel_id: str, title: str, content: Union[str, dict], format_: int
     ) -> _api_model.create_thread():
         """
         创建帖子，创建成功后，返回创建成功的任务ID
 
         :param channel_id: 目标论坛子频道id
         :param title: 帖子标题
         :param content: 帖子内容（具体格式根据format_判断）
         :param format_: 帖子文本格式（1：普通文本、2：HTML、3：Markdown、4：Json）
         :return: 返回的.data中为解析后的json数据
         """
         self.check_warning("发表帖子")
-        json_ = {"title": title, "content": content, "format": format_}
+        if isinstance(content, dict):
+            json_ = {"title": title, "content": dumps(content), "format": format_}
+        elif isinstance(content, str):
+            json_ = {"title": title, "content": content, "format": format_}
+        else:
+            return sdk_error_temp("content参数类型错误，应为str或dict")
         return_ = await self._session.put(
             f"{self.bot_url}/channels/{channel_id}/threads", json=json_
         )
         return await regular_temp(return_)
 
     async def delete_thread(
         self, channel_id: str, thread_id: str
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk/http.py` & `qg-botsdk-2.7.0/qg_botsdk/http.py`

 * *Files identical despite different names*

### Comparing `qg-botsdk-2.6.3/qg_botsdk/logger.py` & `qg-botsdk-2.7.0/qg_botsdk/logger.py`

 * *Files identical despite different names*

### Comparing `qg-botsdk-2.6.3/qg_botsdk/model.py` & `qg-botsdk-2.7.0/qg_botsdk/model.py`

 * *Files identical despite different names*

### Comparing `qg-botsdk-2.6.3/qg_botsdk/plugins.py` & `qg-botsdk-2.7.0/qg_botsdk/plugins.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 #!/usr/bin/env python3
 # -*- coding: utf-8 -*-
 from re import compile as re_compile
 from typing import List, Optional, Pattern, Union
 
+from ._api_model import Bot_Command_Obj
 from .api import API
 from .async_api import AsyncAPI
 from .model import Model
 
 
 class Plugins:
-    _commands = []
-    _preprocessors = []
+    _commands: list[Bot_Command_Obj] = []
+    _preprocessors: list[Model.MESSAGE] = []
     api: Union[API, AsyncAPI] = None
 
-    def __new__(cls) -> tuple:
+    def __new__(cls) -> tuple[list, list]:
         commands, preprocessors = cls._commands, cls._preprocessors
         cls._commands, cls._preprocessors = [], []
         return commands, preprocessors
 
     @classmethod
     def get_preprocessor_names(cls):
         return (func.__name__ for func in cls._preprocessors)
@@ -66,66 +67,59 @@
         def wrap(func: Model.MESSAGE):
             if is_short_circuit and is_custom_short_circuit:
                 raise AttributeError(
                     "注意is_short_circuit与is_custom_short_circuit存在冲突，不可同时为True"
                 )
             if command:
                 if isinstance(command, str):
-                    cls._commands.append(
-                        {
-                            "command": [command],
-                            "func": func,
-                            "treat": is_treat,
-                            "at": is_require_at,
-                            "short_circuit": is_short_circuit,
-                            "is_custom_short_circuit": is_custom_short_circuit,
-                            "admin": is_require_admin,
-                            "admin_error_msg": admin_error_msg,
-                        }
-                    )
+                    command_obj: Bot_Command_Obj = {
+                        "command": [command],
+                        "func": func,
+                        "treat": is_treat,
+                        "at": is_require_at,
+                        "short_circuit": is_short_circuit,
+                        "is_custom_short_circuit": is_custom_short_circuit,
+                        "admin": is_require_admin,
+                        "admin_error_msg": admin_error_msg,
+                    }
                 elif isinstance(command, list):
-                    cls._commands.append(
-                        {
-                            "command": command,
-                            "func": func,
-                            "treat": is_treat,
-                            "at": is_require_at,
-                            "short_circuit": is_short_circuit,
-                            "is_custom_short_circuit": is_custom_short_circuit,
-                            "admin": is_require_admin,
-                            "admin_error_msg": admin_error_msg,
-                        }
-                    )
+                    command_obj: Bot_Command_Obj = {
+                        "command": command,
+                        "func": func,
+                        "treat": is_treat,
+                        "at": is_require_at,
+                        "short_circuit": is_short_circuit,
+                        "is_custom_short_circuit": is_custom_short_circuit,
+                        "admin": is_require_admin,
+                        "admin_error_msg": admin_error_msg,
+                    }
                 else:
                     raise TypeError("command参数仅接受str或list类型的指令内容")
             else:
                 if isinstance(regex, str):
-                    cls._commands.append(
-                        {
-                            "regex": re_compile(regex),
-                            "func": func,
-                            "treat": is_treat,
-                            "at": is_require_at,
-                            "short_circuit": is_short_circuit,
-                            "is_custom_short_circuit": is_custom_short_circuit,
-                            "admin": is_require_admin,
-                            "admin_error_msg": admin_error_msg,
-                        }
-                    )
+                    command_obj: Bot_Command_Obj = {
+                        "regex": re_compile(regex),
+                        "func": func,
+                        "treat": is_treat,
+                        "at": is_require_at,
+                        "short_circuit": is_short_circuit,
+                        "is_custom_short_circuit": is_custom_short_circuit,
+                        "admin": is_require_admin,
+                        "admin_error_msg": admin_error_msg,
+                    }
                 elif isinstance(regex, Pattern):
-                    cls._commands.append(
-                        {
-                            "regex": regex,
-                            "func": func,
-                            "treat": is_treat,
-                            "at": is_require_at,
-                            "short_circuit": is_short_circuit,
-                            "is_custom_short_circuit": is_custom_short_circuit,
-                            "admin": is_require_admin,
-                            "admin_error_msg": admin_error_msg,
-                        }
-                    )
+                    command_obj: Bot_Command_Obj = {
+                        "regex": regex,
+                        "func": func,
+                        "treat": is_treat,
+                        "at": is_require_at,
+                        "short_circuit": is_short_circuit,
+                        "is_custom_short_circuit": is_custom_short_circuit,
+                        "admin": is_require_admin,
+                        "admin_error_msg": admin_error_msg,
+                    }
                 else:
                     raise TypeError("regex参数仅接受re.compile返回的实例或str类型的正则表达式")
+            cls._commands.append(command_obj)
             return func
 
         return wrap
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk/qg_bot.py` & `qg-botsdk-2.7.0/qg_botsdk/qg_bot.py`

 * *Files 10% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 from os.path import split as path_split
 from re import Pattern
 from threading import Lock as TLock
 from time import sleep as t_sleep
 from typing import Any, Callable, List, Optional, Union
 
 from ._api_model import robot_model
-from ._utils import check_func, exception_processor
+from ._utils import check_func
 from .api import API
 from .async_api import AsyncAPI
 from .http import Session
 from .logger import Logger
 from .model import Model
 from .plugins import Plugins
 from .qg_bot_ws import BotWs as _BotWs
@@ -87,30 +87,18 @@
             self._loop = get_event_loop()
         except RuntimeError:
             self._loop = new_event_loop()
         self._intents = 0
         self._shard_no = shard_no
         self._total_shard = total_shard
         self._bot_class = None
-        self._on_delete_function = None
-        self._on_msg_function = None
-        self._on_dm_function = None
-        self._on_guild_event_function = None
-        self._on_channel_event_function = None
-        self._on_guild_member_function = None
-        self._on_reaction_function = None
-        self._on_interaction_function = None
-        self._on_audit_function = None
-        self._on_forum_function = None
-        self._on_open_forum_function = None
-        self._on_audio_function = None
-        self._on_live_channel_member_function = None
+        self._func_registers = {}
         self._repeat_function = None
         self._on_start_function = None
-        self.is_filter_self = True
+        self.del_is_filter_self = True
         self.check_interval = 10
         self.__running = False
         self.__await_closure = False
         self.auth = f"Bot {bot_id}.{bot_token}"
         self.bot_headers = {"Authorization": self.auth}
         self._session = Session(
             self._loop,
@@ -165,26 +153,14 @@
             self.logger.info(
                 f"收到频道 {data.guild_id} 用户 {data.author.username}({data.author.id}) "
                 f"的消息：{data.treated_msg}"
             )
 
         Plugins.before_command()(__sdk_default_logger)
 
-    @exception_processor
-    def __time_event_run(self):
-        if self.is_async:
-            self._loop.create_task(self._repeat_function())
-        else:
-            self._repeat_function()
-
-    async def __time_event_check(self):
-        while self.__running:
-            await sleep(self.check_interval)
-            self.__time_event_run()
-
     def __register_msg_intents(self, is_log=True):
         if not self._intents >> 9 & 1 and not self._intents >> 30 & 1:
             if self.is_private:
                 self._intents = self._intents | 1 << 9
                 if is_log:
                     self.logger.info("消息（所有消息）接收函数订阅成功")
             else:
@@ -254,314 +230,298 @@
         :param is_require_at: 是否要求必须艾特机器人才能触发指令，默认否
         :param is_short_circuit: 如果触发指令成功是否短路不运行后续指令（将根据注册顺序排序指令的短路机制），默认是
         :param is_custom_short_circuit: 如果触发指令成功而返回True则不运行后续指令，与is_short_circuit不能同时存在，默认否
         :param is_require_admin: 是否要求频道主或或管理才可触发指令，默认否
         :param admin_error_msg: 当is_require_admin为True，而触发用户的权限不足时，如此项不为None，返回此消息并短路；否则不进行短路
         """
 
-        def wrap(func: Model.MESSAGE):
+        def wrap(callback: Model.MESSAGE):
             Plugins.on_command(
                 command,
                 regex,
                 is_treat,
                 is_require_at,
                 is_short_circuit,
                 is_custom_short_circuit,
                 is_require_admin,
                 admin_error_msg,
-            )(func)
-            return func
+            )(callback)
+            return callback
 
         return wrap
 
     def bind_msg(
         self,
-        on_msg_function: Callable[[Model.MESSAGE], Any] = None,
+        callback: Callable[[Model.MESSAGE], Any] = None,
         treated_data: bool = True,
         all_msg: bool = None,
     ):
         """
         用作绑定接收消息的函数，将根据机器人是否公域自动判断接收艾特或所有消息
 
-        :param on_msg_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         :param treated_data: 是否返回经转义处理的文本，如是则会在返回的Object中添加一个treated_msg的子类，默认True
         :param all_msg: 是否无视公私域限制，强制开启全部消息接收，默认None（不判断此项参数）
         """
 
         def wraps(func):
             check_func(func, Model.MESSAGE, is_async=self.is_async)
-            self._on_msg_function = func
+            self._func_registers["on_msg"] = func
             if not treated_data:
                 self.msg_treat = False
             if all_msg is None:
                 self.__register_msg_intents()
             elif all_msg:
                 self._intents = self._intents | 1 << 9
                 self.logger.info("消息（所有消息）接收函数订阅成功")
             else:
                 self._intents = self._intents | 1 << 30
                 self.logger.info("消息（艾特消息）接收函数订阅成功")
 
-        if not on_msg_function:
+        if not callback:
             return wraps
-        wraps(on_msg_function)
+        wraps(callback)
 
     def bind_dm(
         self,
-        on_dm_function: Callable[[Model.DIRECT_MESSAGE], Any] = None,
+        callback: Callable[[Model.DIRECT_MESSAGE], Any] = None,
         treated_data: bool = True,
     ):
         """
         用作绑定接收私信消息的函数
 
-        :param on_dm_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         :param treated_data: 是否返回经转义处理的文本，如是则会在返回的Object中添加一个treated_msg的子类，默认True
         """
 
         def wraps(func):
             check_func(func, Model.DIRECT_MESSAGE, is_async=self.is_async)
-            self._on_dm_function = func
+            self._func_registers["on_dm"] = func
             self._intents = self._intents | 1 << 12
             if treated_data:
                 self.dm_treat = True
             self.logger.info("私信接收函数订阅成功")
 
-        if not on_dm_function:
+        if not callback:
             return wraps
-        wraps(on_dm_function)
+        wraps(callback)
 
     def bind_msg_delete(
         self,
-        on_delete_function: Callable[[Model.MESSAGE_DELETE], Any] = None,
+        callback: Callable[[Model.MESSAGE_DELETE], Any] = None,
         is_filter_self: bool = True,
     ):
         """
-        用作绑定接收消息撤回事件的函数，注册时将自动根据公域私域注册艾特或全部消息，但不会主动注册私信事件
+        用作绑定接收消息撤回事件的回调函数，注册时将自动根据公域私域注册艾特或全部消息，但不会主动注册私信事件
 
-        :param on_delete_function:类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback:类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         :param is_filter_self: 是否过滤用户自行撤回的消息，只接受管理撤回事件
         """
 
         def wraps(func):
             check_func(func, Model.MESSAGE_DELETE, is_async=self.is_async)
-            self._on_delete_function = func
-            self.is_filter_self = is_filter_self
+            self._func_registers["on_delete"] = func
+            self._func_registers["del_is_filter_self"] = is_filter_self
             self.__register_msg_intents(False)
             self.logger.info("撤回事件订阅成功")
 
-        if not on_delete_function:
+        if not callback:
             return wraps
-        wraps(on_delete_function)
+        wraps(callback)
 
-    def bind_guild_event(
-        self, on_guild_event_function: Callable[[Model.GUILDS], Any] = None
-    ):
+    def bind_guild_event(self, callback: Callable[[Model.GUILDS], Any] = None):
         """
         用作绑定接收频道信息的函数
 
-        :param on_guild_event_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.GUILDS, is_async=self.is_async)
-            self._on_guild_event_function = func
+            self._func_registers["on_guild_event"] = func
             self._intents = self._intents | 1
             self.logger.info("频道事件订阅成功")
 
-        if not on_guild_event_function:
+        if not callback:
             return wraps
-        wraps(on_guild_event_function)
+        wraps(callback)
 
-    def bind_channel_event(
-        self, on_channel_event_function: Callable[[Model.CHANNELS], Any] = None
-    ):
+    def bind_channel_event(self, callback: Callable[[Model.CHANNELS], Any] = None):
         """
         用作绑定接收子频道信息的函数
 
-        :param on_channel_event_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.CHANNELS, is_async=self.is_async)
-            self._on_channel_event_function = func
+            self._func_registers["on_channel_event"] = func
             self._intents = self._intents | 1
             self.logger.info("子频道事件订阅成功")
 
-        if not on_channel_event_function:
+        if not callback:
             return wraps
-        wraps(on_channel_event_function)
+        wraps(callback)
 
-    def bind_guild_member(
-        self, on_guild_member_function: Callable[[Model.GUILD_MEMBERS], Any] = None
-    ):
+    def bind_guild_member(self, callback: Callable[[Model.GUILD_MEMBERS], Any] = None):
         """
         用作绑定接收频道成员信息的函数
 
-        :param on_guild_member_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.GUILD_MEMBERS, is_async=self.is_async)
-            self._on_guild_member_function = func
+            self._func_registers["on_guild_member"] = func
             self._intents = self._intents | 1 << 1
             self.logger.info("频道成员事件订阅成功")
 
-        if not on_guild_member_function:
+        if not callback:
             return wraps
-        wraps(on_guild_member_function)
+        wraps(callback)
 
-    def bind_reaction(
-        self, on_reaction_function: Callable[[Model.REACTION], Any] = None
-    ):
+    def bind_reaction(self, callback: Callable[[Model.REACTION], Any] = None):
         """
         用作绑定接收表情表态信息的函数
 
-        :param on_reaction_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.REACTION, is_async=self.is_async)
-            self._on_reaction_function = func
+            self._func_registers["on_reaction"] = func
             self._intents = self._intents | 1 << 10
             self.logger.info("表情表态事件订阅成功")
 
-        if not on_reaction_function:
+        if not callback:
             return wraps
-        wraps(on_reaction_function)
+        wraps(callback)
 
-    def bind_interaction(
-        self, on_interaction_function: Callable[[Model.INTERACTION], Any] = None
-    ):
+    def bind_interaction(self, callback: Callable[[Model.INTERACTION], Any] = None):
         """
-        用作绑定接收互动事件的函数
+        用作绑定接收互动事件的回调函数
 
-        :param on_interaction_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.INTERACTION, is_async=self.is_async)
-            self._on_interaction_function = func
+            self._func_registers["on_interaction"] = func
             self._intents = self._intents | 1 << 26
             self.logger.info("互动事件订阅成功")
 
-        if not on_interaction_function:
+        if not callback:
             return wraps
-        wraps(on_interaction_function)
+        wraps(callback)
 
-    def bind_audit(
-        self, on_audit_function: Callable[[Model.MESSAGE_AUDIT], Any] = None
-    ):
+    def bind_audit(self, callback: Callable[[Model.MESSAGE_AUDIT], Any] = None):
         """
-        用作绑定接收审核事件的函数
+        用作绑定接收审核事件的回调函数
 
-        :param on_audit_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.MESSAGE_AUDIT, is_async=self.is_async)
-            self._on_audit_function = func
+            self._func_registers["on_audit"] = func
             self._intents = self._intents | 1 << 27
             self.logger.info("审核事件订阅成功")
 
-        if not on_audit_function:
+        if not callback:
             return wraps
-        wraps(on_audit_function)
+        wraps(callback)
 
-    def bind_forum(self, on_forum_function: Callable[[Model.FORUMS_EVENT], Any] = None):
+    def bind_forum(self, callback: Callable[[Model.FORUMS_EVENT], Any] = None):
         """
-        用作绑定接收论坛事件的函数，一般仅私域机器人能注册此事件
+        用作绑定接收论坛事件的回调函数，一般仅私域机器人能注册此事件
 
         .. note::
             当前仅可以接收FORUM_THREAD_CREATE、FORUM_THREAD_UPDATE、FORUM_THREAD_DELETE三个事件
 
-        :param on_forum_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.FORUMS_EVENT, is_async=self.is_async)
-            self._on_forum_function = func
+            self._func_registers["on_forum"] = func
             self._intents = self._intents | 1 << 28
             self.logger.info("论坛事件订阅成功")
             if not self.is_private and self.no_permission_warning:
                 self.logger.warning("请注意，一般公域机器人并不能注册论坛事件，请检查自身是否拥有相关权限")
 
-        if not on_forum_function:
+        if not callback:
             return wraps
-        wraps(on_forum_function)
+        wraps(callback)
 
-    def bind_open_forum(
-        self, on_open_forum_function: Callable[[Model.OPEN_FORUMS], Any] = None
-    ):
+    def bind_open_forum(self, callback: Callable[[Model.OPEN_FORUMS], Any] = None):
         """
-        用作绑定接收公域论坛事件的函数
+        用作绑定接收公域论坛事件的回调函数
 
         .. note::
-            当前仅可以接收FORUM_THREAD_CREATE、FORUM_THREAD_UPDATE、FORUM_THREAD_DELETE三个事件
+            当前仅可以接收OPEN_FORUM_THREAD_CREATE、OPEN_FORUM_THREAD_UPDATE、OPEN_FORUM_THREAD_DELETE三个事件
 
-        :param on_open_forum_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.OPEN_FORUMS, is_async=self.is_async)
-            self._on_open_forum_function = func
+            self._func_registers["on_open_forum"] = func
             self._intents = self._intents | 1 << 18
             self.logger.info("论坛事件订阅成功")
 
-        if not on_open_forum_function:
+        if not callback:
             return wraps
-        wraps(on_open_forum_function)
+        wraps(callback)
 
-    def bind_audio(self, on_audio_function: Callable[[Model.AUDIO_ACTION], Any] = None):
+    def bind_audio(self, callback: Callable[[Model.AUDIO_ACTION], Any] = None):
         """
-        用作绑定接收论坛事件的函数
+        用作绑定接收论坛事件的回调函数
 
-        :param on_audio_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.AUDIO_ACTION, is_async=self.is_async)
-            self._on_audio_function = func
+            self._func_registers["on_audio"] = func
             self._intents = self._intents | 1 << 29
             self.logger.info("音频事件订阅成功")
             if self.no_permission_warning:
                 self.logger.warning("请注意，一般机器人并不能注册音频事件（需先进行申请），请检查自身是否拥有相关权限")
 
-        if not on_audio_function:
+        if not callback:
             return wraps
-        wraps(on_audio_function)
+        wraps(callback)
 
     def bind_live_channel_member(
         self,
-        on_live_channel_member_function: Callable[
-            [Model.LIVE_CHANNEL_MEMBER], Any
-        ] = None,
+        callback: Callable[[Model.LIVE_CHANNEL_MEMBER], Any] = None,
     ):
         """
-        用作绑定接收音视频/直播子频道成员进出事件的函数
+        用作绑定接收音视频/直播子频道成员进出事件的回调函数
 
-        :param on_live_channel_member_function: 类型为function，该函数应包含一个参数以接收Object消息数据进行处理
+        :param callback: 类型为function，该回调函数应包含一个参数以接收Object消息数据进行处理
         """
 
         def wraps(func):
             check_func(func, Model.LIVE_CHANNEL_MEMBER, is_async=self.is_async)
-            self._on_live_channel_member_function = func
+            self._func_registers["on_live_channel_member"] = func
             self._intents = self._intents | 1 << 19
             self.logger.info("音视频/直播子频道成员进出事件订阅成功")
 
-        if not on_live_channel_member_function:
+        if not callback:
             return wraps
-        wraps(on_live_channel_member_function)
+        wraps(callback)
 
     def register_repeat_event(
         self,
         time_function: Callable[[], Any] = None,
         check_interval: Union[float, int] = 10,
     ):
         """
-        用作注册重复事件的函数，注册并开始机器人后，会根据间隔时间不断调用注册的函数
+        用作注册重复事件的回调函数，注册并开始机器人后，会根据间隔时间不断调用该回调函数
 
         :param time_function: 类型为function，该函数不应包含任何参数
         :param check_interval: 每多少秒检查调用一次时间事件函数，默认10
         """
 
         def wraps(func):
             check_func(func, is_async=self.is_async)
@@ -571,15 +531,15 @@
 
         if not time_function:
             return wraps
         wraps(time_function)
 
     def register_start_event(self, on_start_function: Callable[[], Any] = None):
         """
-        用作注册机器人开始时运行的函数，此函数不应有无限重复的内容
+        用作注册机器人开始时运行的函数，此函数不应有无限重复的内容，会在机器人完成登录后调用该回调函数
 
         :param on_start_function: 类型为function，该函数不应包含任何参数
         """
 
         def wraps(func):
             check_func(func, is_async=self.is_async)
             self._on_start_function = func
@@ -627,64 +587,52 @@
                 if not url:
                     raise type("IdTokenError", (Exception,), {})(
                         "你输入的 bot_id 和/或 bot_token 错误，无法连接使用机器人\n如尚未有相关票据，"
                         "请参阅 https://qg-botsdk.readthedocs.io/zh_CN/latest/quick_start 了解相关详情"
                     )
                 self.logger.debug("[机器人ws地址] " + url)
                 commands, preprocessors = self._get_plugins()
-                if self._repeat_function is not None:
-                    self._loop.create_task(self.__time_event_check())
                 self._bot_class = _BotWs(
+                    self._loop,
                     self._session,
                     self.logger,
                     self._total_shard,
                     self._shard_no,
                     url,
                     self.auth,
-                    self._on_msg_function,
-                    self._on_dm_function,
-                    self._on_delete_function,
-                    self.is_filter_self,
-                    self._on_guild_event_function,
-                    self._on_channel_event_function,
-                    self._on_guild_member_function,
-                    self._on_reaction_function,
-                    self._on_interaction_function,
-                    self._on_audit_function,
-                    self._on_forum_function,
-                    self._on_open_forum_function,
-                    self._on_audio_function,
-                    self._on_live_channel_member_function,
+                    self._func_registers,
                     self._intents,
                     self.msg_treat,
                     self.dm_treat,
                     self._on_start_function,
+                    self.check_interval,
+                    self._repeat_function,
                     self.is_async,
                     self.max_workers,
                     self.api,
                     commands,
                     preprocessors,
                 )
+                self._loop.create_task(self._bot_class.starter())
                 if is_blocking:
-                    self._loop.run_until_complete(self._bot_class.starter())
-                else:
-                    self._loop.create_task(self._bot_class.starter())
+
+                    self._loop.run_forever()
             else:
                 self.logger.error("当前机器人已在运行中！")
         except KeyboardInterrupt:
             self.logger.info("结束运行机器人（KeyboardInterrupt）")
             exit()
 
     def block(self):
         """
         当BOT.start()选择is_blocking=False的非阻塞性运行时，此函数能在后续阻塞主进程而继续运行机器人
         """
         try:
-            while self.__running or self.__await_closure:
-                self._loop.run_until_complete(sleep(1))
+            if self.__running or self.__await_closure:
+                self._loop.run_forever()
         except KeyboardInterrupt:
             self.logger.info("结束运行机器人（KeyboardInterrupt）")
             exit()
 
     def close(self):
         """
         结束运行机器人的函数
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk/qg_bot_ws.py` & `qg-botsdk-2.7.0/qg_botsdk/qg_bot_ws.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,19 +1,20 @@
 #!/usr/bin/env python3
 # -*- coding: utf-8 -*-
-from asyncio import all_tasks, get_event_loop, new_event_loop, sleep
+from asyncio import AbstractEventLoop, all_tasks, sleep
 from concurrent.futures import ThreadPoolExecutor
 from copy import copy, deepcopy
 from json import dumps, loads
 from ssl import create_default_context
 from typing import Any, Callable, Union
 from unittest.mock import PropertyMock, patch
 
 from aiohttp import ClientSession, WSMsgType, WSServerHandshakeError
 
+from ._api_model import Bot_Command_Obj
 from ._statics import EVENTS
 from ._utils import (
     exception_handler,
     exception_processor,
     object_class,
     objectize,
     treat_msg,
@@ -26,43 +27,33 @@
 from .model import Model
 from .plugins import Plugins
 
 
 class BotWs:
     def __init__(
         self,
+        loop: AbstractEventLoop,
         session: Session,
         logger: Logger,
         total_shard: int,
         shard_no: int,
         ws_url: str,
         auth: str,
-        on_msg_function: Callable[[Any], Any],
-        on_dm_function: Callable[[Any], Any],
-        on_delete_function: Callable[[Any], Any],
-        is_filter_self: bool,
-        on_guild_event_function: Callable[[Any], Any],
-        on_channel_event_function: Callable[[Any], Any],
-        on_guild_member_function: Callable[[Any], Any],
-        on_reaction_function: Callable[[Any], Any],
-        on_interaction_function: Callable[[Any], Any],
-        on_audit_function: Callable[[Any], Any],
-        on_forum_function: Callable[[Any], Any],
-        on_open_forum_function: Callable[[Any], Any],
-        on_audio_function: Callable[[Any], Any],
-        on_live_channel_member_function: Callable[[Any], Any],
+        func_registers: dict,
         intents: int,
         msg_treat: bool,
         dm_treat: bool,
         on_start_function: Callable[[], Any],
+        check_interval: int,
+        repeat_function: Callable[[], Any],
         is_async: bool,
         max_workers: int,
         api: Union[AsyncAPI, API],
-        commands,
-        preprocessors,
+        commands: list[Bot_Command_Obj],
+        preprocessors: list[Model.MESSAGE],
     ):
         """
         此为SDK内部使用类，注册机器人请使用from qg_botsdk.qg_bot import BOT
 
         .. seealso::
             更多教程和相关资讯可参阅：
             https://qg-botsdk.readthedocs.io/zh_CN/latest/快速入门.html
@@ -71,87 +62,90 @@
         self._ssl = create_default_context()
         self.logger = logger
         self.total_shard = total_shard
         self.shard_no = shard_no
         self.ws_url = ws_url
         self.auth = auth
         self.on_start_function = on_start_function
-        self.on_msg_function = on_msg_function
-        self.on_dm_function = on_dm_function
-        self.on_delete_function = on_delete_function
-        self.is_filter_self = is_filter_self
-        self.on_forum_function = on_forum_function
+        self.check_interval = check_interval
+        self.repeat_function = repeat_function
+        self.func_registers = func_registers
         if not intents:
             self.logger.warning("当前未订阅任何事件，将无法接收任何消息，只能使用主动消息功能")
             intents = 1
         self.intents = intents
         self.msg_treat = msg_treat
         self.dm_treat = dm_treat
         self.robot = None
         self.heartbeat_time = 0
-        try:
-            self.loop = get_event_loop()
-        except RuntimeError:
-            self.loop = new_event_loop()
+        self.loop = loop
         self.s = None
         self.reconnect_times = 0
         self.is_reconnect = False
         self.running = True
         self.session_id = 0
         self.is_first_run = False
         self.heartbeat = None
         self.is_async = is_async
         self.events = {
-            **dict(zip(EVENTS.GUILD, [on_guild_event_function] * len(EVENTS.GUILD))),
-            **dict(
-                zip(EVENTS.CHANNEL, [on_channel_event_function] * len(EVENTS.CHANNEL))
-            ),
+            **dict(zip(EVENTS.GUILD, ["on_guild_event"] * len(EVENTS.GUILD))),
+            **dict(zip(EVENTS.CHANNEL, ["on_channel_event"] * len(EVENTS.CHANNEL))),
             **dict(
                 zip(
                     EVENTS.GUILD_MEMBER,
-                    [on_guild_member_function] * len(EVENTS.GUILD_MEMBER),
+                    ["on_guild_member"] * len(EVENTS.GUILD_MEMBER),
                 )
             ),
-            **dict(zip(EVENTS.REACTION, [on_reaction_function] * len(EVENTS.REACTION))),
+            **dict(zip(EVENTS.REACTION, ["on_reaction"] * len(EVENTS.REACTION))),
             **dict(
                 zip(
                     EVENTS.INTERACTION,
-                    [on_interaction_function] * len(EVENTS.INTERACTION),
-                )
-            ),
-            **dict(zip(EVENTS.AUDIT, [on_audit_function] * len(EVENTS.AUDIT))),
-            **dict(
-                zip(
-                    EVENTS.OPEN_FORUM, [on_open_forum_function] * len(EVENTS.OPEN_FORUM)
+                    ["on_interaction"] * len(EVENTS.INTERACTION),
                 )
             ),
-            **dict(zip(EVENTS.AUDIO, [on_audio_function] * len(EVENTS.AUDIO))),
+            **dict(zip(EVENTS.AUDIT, ["on_audit"] * len(EVENTS.AUDIT))),
+            **dict(zip(EVENTS.OPEN_FORUM, ["on_open_forum"] * len(EVENTS.OPEN_FORUM))),
+            **dict(zip(EVENTS.AUDIO, ["on_audio"] * len(EVENTS.AUDIO))),
             **dict(
                 zip(
                     EVENTS.ALC_MEMBER,
-                    [on_live_channel_member_function] * len(EVENTS.ALC_MEMBER),
+                    ["on_live_channel_member"] * len(EVENTS.ALC_MEMBER),
                 )
             ),
         }
         self.threads = ThreadPoolExecutor(max_workers) if not self.is_async else None
         self.api = api
         self.commands = commands
         self.preprocessors = preprocessors
         self.at = "<@!%s>"
 
+    @exception_processor
+    async def _time_event_run(self):
+        if self.is_async:
+            self.loop.create_task(self.repeat_function())
+        else:
+            self.threads.submit(self.repeat_function)
+
+    async def _time_event_check(self):
+        while self.running:
+            await sleep(self.check_interval)
+            await self._time_event_run()
+
     async def _start_event(self):
         self.is_first_run = True
         self.robot = await self.get_robot_info()
         self.at = self.at % self.robot.id
         self.logger.info(f"机器人频道用户ID：{self.robot.id}")
         if self.on_start_function is not None:
             if self.is_async:
                 self.loop.create_task(self.on_start_function())
             else:
                 self.threads.submit(self.start_task, self.on_start_function)
+        if self.repeat_function is not None:
+            self.loop.create_task(self._time_event_check())
 
     async def send_connect(self):
         connect_paras = {
             "op": 2,
             "d": {
                 "token": self.auth,
                 "intents": self.intents,
@@ -225,30 +219,34 @@
         self, objectized_data: Model.MESSAGE, treated_msg, command=None, regex=None
     ):
         if self.msg_treat:
             msg = treated_msg
             # deepcopy treated_msg with just shallow copy others
             # resulting that changing of treated msg will not affect other commands
             memo = {}
-            for x in objectized_data.__dict__.keys():
+            for x in objectized_data.__dict__:
                 if x != "treated_msg":
                     memo[id(getattr(objectized_data, x))] = copy(
                         getattr(objectized_data, x)
                     )
             objectized_data = deepcopy(objectized_data, memo)
             objectized_data.treated_msg = (
                 msg[msg.find(command) + len(command) :].strip()
                 if command
                 else regex.groups()
             )
         return objectized_data
 
     @exception_processor
     async def check_command(
-        self, objectized_data: Model.MESSAGE, treated_msg, command_obj, **kwargs
+        self,
+        objectized_data: Model.MESSAGE,
+        treated_msg: str,
+        command_obj: Bot_Command_Obj,
+        **kwargs,
     ):
         # command: {command or regex, func, treat, at, short_circuit, admin, admin_error_msg}
         if command_obj["admin"]:
             try:
                 roles = objectized_data.member.roles
             except Exception:
                 command_str = kwargs.get("command") or getattr(
@@ -282,15 +280,15 @@
                 return command_obj["short_circuit"]  # True or False
             else:
                 while not task.done():
                     await sleep(0.5)
                 return task.result()  # True or False
 
     @exception_processor
-    async def distribute_commands(self, data, treated_msg):
+    async def distribute_commands(self, data: dict, treated_msg: str):
         objectized_data = objectize(data.get("d", {}), self.api, self.is_async)
         # run preprocessors
         for func in self.preprocessors:
             await self.distribute(func, objectized_data=objectized_data)
         # check commands
         msg = data.get("d", {}).get("content", "")
         # commands = [{command or regex, func, treat, at, short_circuit, admin, admin_error_msg}]
@@ -308,54 +306,55 @@
                 if regex and (not items["at"] or self.at in msg):
                     if await self.check_command(
                         objectized_data, treated_msg, items, regex=regex
                     ):
                         return True
 
     @exception_processor
-    async def data_process(self, data):
+    async def data_process(self, data: dict):
         # initialize values
         t = data.get("t")
         d = data.get("d", {})
         if not d:
             data["d"] = d
         data["d"]["t"] = t
         data["d"]["event_id"] = data.get("id")
         # process and distribute data
         if t in self.events:
-            await self.distribute(self.events[t], data)
+            _key = self.events[t]
+            await self.distribute(self.func_registers[_key], data)
         elif t in EVENTS.MESSAGE_CREATE:
             if self.msg_treat:
                 raw_msg = d.get("content", "").strip()
                 treated_msg = treat_msg(raw_msg, self.at)
                 data["d"]["treated_msg"] = treated_msg
             else:
                 treated_msg = ""
             # distribute_commands return True when short circuit
             if not await self.distribute_commands(data, treated_msg):
-                await self.distribute(self.on_msg_function, data)
+                await self.distribute(self.func_registers["on_msg"], data)
         elif t in EVENTS.MESSAGE_DELETE:
-            if self.is_filter_self:
+            if self.func_registers["del_is_filter_self"]:
                 target = d.get("message", {}).get("author", {}).get("id")
                 op_user = d.get("op_user", {}).get("id")
                 if op_user == target:
                     return
-            await self.distribute(self.on_delete_function, data)
+            await self.distribute(self.func_registers["on_delete"], data)
         elif t in EVENTS.DM_CREATE:
             if self.dm_treat:
                 raw_msg = d.get("content", "").strip()
                 data["d"]["treated_msg"] = treat_msg(raw_msg, self.at)
-            await self.distribute(self.on_dm_function, data)
+            await self.distribute(self.func_registers["on_dm"], data)
         elif t in EVENTS.FORUM:
             treat_thread(data)
-            await self.distribute(self.on_forum_function, data)
+            await self.distribute(self.func_registers["on_forum"], data)
         else:
             self.logger.warning(f"unknown event type: [{t}]")
 
-    async def dispatch_events(self, msg):
+    async def dispatch_events(self, msg: str):
         data = loads(msg)
         op = data.get("op")
         if "s" in data:
             self.s = data["s"]
         if op == 11:
             self.logger.debug("心跳发送成功")
         elif op == 9:
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk/utils.py` & `qg-botsdk-2.7.0/qg_botsdk/utils.py`

 * *Files identical despite different names*

### Comparing `qg-botsdk-2.6.3/qg_botsdk.egg-info/PKG-INFO` & `qg-botsdk-2.7.0/qg_botsdk.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: qg-botsdk
-Version: 2.6.3
+Version: 2.7.0
 Summary: easy-to-use SDK for Tencent QQ guild robot
 Home-page: https://github.com/GLGDLY/qg_botsdk
 Author: GDLY
 Author-email: tzlgdly@gmail.com
 Keywords: sample,example,setuptools
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
@@ -41,15 +41,15 @@
 
 
 亮点
 =====
 
 -   灵活的构建方式，即使官方删除或新增字段，SDK也不会规范于原来的数据格式，而会把真实数据反馈给你
 
--   轻量，简洁，统一的代码结构，10行即可构建一个简单的程序
+-   轻量，简洁，统一的代码结构，通过录入回调函数处理不同事件，10行即可构建一个简单的程序
 
 -   容易入门，无需学会asyncio、类继承等编程技巧也可使用，同时保留较高并发能力
 
 -   保留官方http API中Json数据的结构字段，带你学习官方结构，日后可自行开发适合自己的SDK
 
 -   迅速的更新速度，跟上最新潮流（v2.5.5已更新音视频/直播子频道成员进出事件、公域论坛事件）
```

### Comparing `qg-botsdk-2.6.3/qg_botsdk.egg-info/SOURCES.txt` & `qg-botsdk-2.7.0/qg_botsdk.egg-info/SOURCES.txt`

 * *Files identical despite different names*

