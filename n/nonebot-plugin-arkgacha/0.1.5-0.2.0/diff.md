# Comparing `tmp/nonebot_plugin_arkgacha-0.1.5.tar.gz` & `tmp/nonebot_plugin_arkgacha-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_arkgacha-0.1.5.tar", last modified: Sat May 13 03:08:46 2023, max compression
+gzip compressed data, was "nonebot_plugin_arkgacha-0.2.0.tar", last modified: Sat May 13 08:22:31 2023, max compression
```

## Comparing `nonebot_plugin_arkgacha-0.1.5.tar` & `nonebot_plugin_arkgacha-0.2.0.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0    34522 2021-09-10 07:59:22.042000 nonebot_plugin_arkgacha-0.1.5/LICENSE
--rw-r--r--   0        0        0     1865 2023-05-13 03:00:40.184542 nonebot_plugin_arkgacha-0.1.5/README.md
--rw-r--r--   0        0        0     4820 2023-05-13 03:03:37.167500 nonebot_plugin_arkgacha-0.1.5/nonebot_plugin_arkgacha/__init__.py
--rw-r--r--   0        0        0      212 2023-05-13 03:00:40.224079 nonebot_plugin_arkgacha-0.1.5/nonebot_plugin_arkgacha/config.py
--rw-r--r--   0        0        0      631 2023-05-13 03:08:46.389972 nonebot_plugin_arkgacha-0.1.5/pyproject.toml
--rw-r--r--   0        0        0     2276 1970-01-01 00:00:00.000000 nonebot_plugin_arkgacha-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0    34522 2021-09-10 07:59:22.042000 nonebot_plugin_arkgacha-0.2.0/LICENSE
+-rw-r--r--   0        0        0     2131 2023-05-13 08:16:56.047078 nonebot_plugin_arkgacha-0.2.0/README.md
+-rw-r--r--   0        0        0     5968 2023-05-13 08:21:01.859005 nonebot_plugin_arkgacha-0.2.0/nonebot_plugin_arkgacha/__init__.py
+-rw-r--r--   0        0        0      250 2023-05-13 08:21:01.844002 nonebot_plugin_arkgacha-0.2.0/nonebot_plugin_arkgacha/config.py
+-rw-r--r--   0        0        0      696 2023-05-13 08:22:31.130615 nonebot_plugin_arkgacha-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0     2617 1970-01-01 00:00:00.000000 nonebot_plugin_arkgacha-0.2.0/PKG-INFO
```

### Comparing `nonebot_plugin_arkgacha-0.1.5/LICENSE` & `nonebot_plugin_arkgacha-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_arkgacha-0.1.5/README.md` & `nonebot_plugin_arkgacha-0.2.0/README.md`

 * *Files 20% similar despite different names*

```diff
@@ -23,32 +23,41 @@
 该插件提供了模拟明日方舟抽卡的功能，包括无头形式的抽卡模拟与模拟十连
 
 通过使用 [`saa`](https://github.com/felinae98/nonebot-plugin-send-anything-anywhere) 插件适配多平台
 
 ## 安装
 
 ```bash
-pip install nonebot-plugin-arkgacha
+$ pip install nonebot-plugin-arkgacha
 ```
 
 ```bash
-nb plugin install nonebot-plugin-arkgacha
+$ nb plugin install nonebot-plugin-arkgacha
 ```
 
 **在使用该插件之前，需要先初始化资源**
 
+命令行输入：
 ```bash
-arkkit init
+$ arkkit init -SIMG
 ```
 
 ## 配置
 
 - ARKGACHA_POOL_FILE: 抽卡池文件路径, 不填则使用 [`localstore`](https://github.com/nonebot/plugin-localstore) 保存抽卡池
 - ARKGACHA_MAX: 抽卡最大次数, 默认为 300
 - ARKGACHA_PURE_TEXT: 是否使用纯文本, 默认为 False (十连模拟必须使用图片)
+- ARKGACHA_AUTO_UPDATE: 是否自动更新，默认为 True
+
+## 注意事项
+1. `方舟抽卡` 不需要图片资源, 可在不经过 `arkkit init` 的情况下使用
+2. `方舟十连` 需要图片资源, 需要先在命令行中执行 `arkkit init -SIMG` 初始化资源，否则会出现错误
+3. 若配置，每天 16 点将自动更新卡池资源
+4. 如果获取资源时出现网络错误，请检查代理设置，或尝试访问 PRTS
+
 ## 使用方法
 
 指令如下: 
 > 方舟抽卡
 > 
 > 方舟抽卡 200
 > 
@@ -58,11 +67,7 @@
 
 
 ## 效果
 
 > 方舟十连
 
 ![res](./test.png)
-
-## 注意事项
-1. `方舟抽卡` 不需要图片资源, 可在不经过 `arkkit init` 的情况下使用
-2. `方舟十连` 需要图片资源, 需要先执行 `arkkit init` 初始化资源，否则会出现错误
```

#### html2text {}

```diff
@@ -1,17 +1,21 @@
                                    [nonebot]
         # NoneBot Plugin Arkgacha _â¨ ææ¥æ¹èæ½å¡æ¨¡æå¨ â¨_
                            [license] [pypi] [python]
 è¯¥æä»¶æä¾äºæ¨¡æææ¥æ¹èæ½å¡çåè½ï¼åæ¬æ å¤´å½¢å¼çæ½å¡æ¨¡æä¸æ¨¡æåè¿
 éè¿ä½¿ç¨ [`saa`](https://github.com/felinae98/nonebot-plugin-send-anything-
-anywhere) æä»¶ééå¤å¹³å° ## å®è£ ```bash pip install nonebot-plugin-
-arkgacha ``` ```bash nb plugin install nonebot-plugin-arkgacha ```
-**å¨ä½¿ç¨è¯¥æä»¶ä¹åï¼éè¦ååå§åèµæº** ```bash arkkit init ```
-## éç½® - ARKGACHA_POOL_FILE: æ½å¡æ± æä»¶è·¯å¾, ä¸å¡«åä½¿ç¨
-[`localstore`](https://github.com/nonebot/plugin-localstore) ä¿å­æ½å¡æ±  -
-ARKGACHA_MAX: æ½å¡æå¤§æ¬¡æ°, é»è®¤ä¸º 300 - ARKGACHA_PURE_TEXT:
-æ¯å¦ä½¿ç¨çº¯ææ¬, é»è®¤ä¸º False (åè¿æ¨¡æå¿é¡»ä½¿ç¨å¾ç) ##
-ä½¿ç¨æ¹æ³ æä»¤å¦ä¸: > æ¹èæ½å¡ > > æ¹èæ½å¡ 200 > > æ¹èåè¿
-> > æ¹èå¡æ± æ´æ° ## ææ > æ¹èåè¿ ![res](./test.png) ##
-æ³¨æäºé¡¹ 1. `æ¹èæ½å¡` ä¸éè¦å¾çèµæº, å¯å¨ä¸ç»è¿ `arkkit
-init` çæåµä¸ä½¿ç¨ 2. `æ¹èåè¿` éè¦å¾çèµæº, éè¦åæ§è¡
-`arkkit init` åå§åèµæºï¼å¦åä¼åºç°éè¯¯
+anywhere) æä»¶ééå¤å¹³å° ## å®è£ ```bash $ pip install nonebot-plugin-
+arkgacha ``` ```bash $ nb plugin install nonebot-plugin-arkgacha ```
+**å¨ä½¿ç¨è¯¥æä»¶ä¹åï¼éè¦ååå§åèµæº** å½ä»¤è¡è¾å¥ï¼
+```bash $ arkkit init -SIMG ``` ## éç½® - ARKGACHA_POOL_FILE:
+æ½å¡æ± æä»¶è·¯å¾, ä¸å¡«åä½¿ç¨ [`localstore`](https://github.com/
+nonebot/plugin-localstore) ä¿å­æ½å¡æ±  - ARKGACHA_MAX: æ½å¡æå¤§æ¬¡æ°,
+é»è®¤ä¸º 300 - ARKGACHA_PURE_TEXT: æ¯å¦ä½¿ç¨çº¯ææ¬, é»è®¤ä¸º False
+(åè¿æ¨¡æå¿é¡»ä½¿ç¨å¾ç) - ARKGACHA_AUTO_UPDATE:
+æ¯å¦èªå¨æ´æ°ï¼é»è®¤ä¸º True ## æ³¨æäºé¡¹ 1. `æ¹èæ½å¡`
+ä¸éè¦å¾çèµæº, å¯å¨ä¸ç»è¿ `arkkit init` çæåµä¸ä½¿ç¨ 2.
+`æ¹èåè¿` éè¦å¾çèµæº, éè¦åå¨å½ä»¤è¡ä¸­æ§è¡ `arkkit init
+-SIMG` åå§åèµæºï¼å¦åä¼åºç°éè¯¯ 3. è¥éç½®ï¼æ¯å¤© 16
+ç¹å°èªå¨æ´æ°å¡æ± èµæº 4.
+å¦æè·åèµæºæ¶åºç°ç½ç»éè¯¯ï¼è¯·æ£æ¥ä»£çè®¾ç½®ï¼æå°è¯è®¿é®
+PRTS ## ä½¿ç¨æ¹æ³ æä»¤å¦ä¸: > æ¹èæ½å¡ > > æ¹èæ½å¡ 200 > >
+æ¹èåè¿ > > æ¹èå¡æ± æ´æ° ## ææ > æ¹èåè¿ ![res](./test.png)
```

### Comparing `nonebot_plugin_arkgacha-0.1.5/nonebot_plugin_arkgacha/__init__.py` & `nonebot_plugin_arkgacha-0.2.0/nonebot_plugin_arkgacha/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,22 +1,30 @@
+import asyncio
 import json
 from dataclasses import asdict
-from nonebot import get_driver, require, on_fullmatch
-from nonebot.adapters import Event
-from nonebot.plugin import PluginMetadata
+from pathlib import Path
+import sys
+
 from arclet.alconna import Alconna, Args, CommandMeta
+from arknights_toolkit import need_init
 from arknights_toolkit.gacha import ArknightsGacha, GachaUser
+from httpx import AsyncClient, ConnectError, TimeoutException
+from nonebot import get_driver, on_fullmatch, require
+from nonebot.adapters import Event
+from nonebot.plugin import PluginMetadata
 
 require("nonebot_plugin_alconna")
 require("nonebot_plugin_localstore")
 require("nonebot_plugin_saa")
+require("nonebot_plugin_apscheduler")
 
-from nonebot_plugin_alconna import on_alconna, AlconnaMatch, Match
+from nonebot_plugin_alconna import AlconnaMatch, Match, on_alconna
 from nonebot_plugin_localstore import get_cache_file, get_data_file
-from nonebot_plugin_saa import MessageFactory, Image
+from nonebot_plugin_saa import Image, MessageFactory, Text
+from nonebot_plugin_apscheduler import scheduler
 
 from .config import Config
 
 driver = get_driver()
 global_config = driver.config
 config = Config.parse_obj(global_config)
 
@@ -54,14 +62,32 @@
     priority=15,
     block=True
 )
 simulate_regex = on_fullmatch("方舟十连", priority=16, block=True)
 help_regex = on_fullmatch("方舟抽卡帮助", priority=16, block=True)
 update_regex = on_fullmatch("方舟卡池更新", priority=16, block=True)
 
+if config.arkgacha_auto_update:
+    @scheduler.scheduled_job("cron", hour=16)
+    async def update_pool():
+        await gacha.update()
+
+
+@driver.on_startup
+async def _():
+    if need_init():
+        process = await asyncio.create_subprocess_shell(
+            f"{Path(sys.executable).parent / 'arkkit'} init -SIMG",
+        )
+        try:
+            await process.communicate()
+        except Exception:
+            process.kill()
+            await process.communicate()
+
 
 @driver.on_shutdown
 async def _():
     with user_cache_file.open("w+", encoding="utf-8") as _f:
         json.dump(userdata, _f, ensure_ascii=False)
 
 
@@ -75,21 +101,31 @@
         "方舟卡池更新\n"
     )
 
 
 @update_regex.handle()
 async def _():
     if new := (await gacha.update()):
-        await update_regex.finish(
+        text = (
             f"更新成功，卡池已更新至{new.title}\n"
             "六星角色：\n" +
             "\n".join(f"{i.name} {'【限定】' if i.limit else '【常驻】'}" for i in new.six_chars) +
             "\n五星角色：\n" +
             "\n".join(f"{i.name} {'【限定】' if i.limit else '【常驻】'}" for i in new.five_chars)
         )
+        if config.arkgacha_pure_text:
+            await update_regex.send(text)
+        else:
+            try:
+                async with AsyncClient() as client:
+                    data = await client.get(new.pool)
+                await MessageFactory([Text(text), Image(data.content)]).send()
+            except (TimeoutException, ConnectError, RuntimeError):
+                await update_regex.send(text)
+        await update_regex.finish()
     else:
         await update_regex.finish("卡池已是最新")
 
 
 @gacha_regex.handle()
 async def _(event: Event, count: Match[int] = AlconnaMatch("count")):
     session = event.get_user_id()
```

### Comparing `nonebot_plugin_arkgacha-0.1.5/pyproject.toml` & `nonebot_plugin_arkgacha-0.2.0/pyproject.toml`

 * *Files 23% similar despite different names*

```diff
@@ -1,20 +1,22 @@
 [project]
 name = "nonebot-plugin-arkgacha"
-version = "0.1.5"
+version = "0.2.0"
 description = "Plugin for Arknights gacha, support multi platform"
 authors = [
     { name = "RF-Tar-Railt", email = "3165388245@qq.com" },
 ]
 dependencies = [
     "nonebot2>=2.0.0rc4",
     "nonebot-plugin-alconna>=0.4.2",
     "nonebot-plugin-send-anything-anywhere>=0.2.4",
-    "arknights-toolkit>=0.5.2",
+    "arknights-toolkit>=0.5.4",
     "nonebot-plugin-localstore>=0.4.1",
+    "nonebot-plugin-apscheduler>=0.2.0",
+    "nepattern>=0.5.7",
 ]
 requires-python = ">=3.8"
 readme = "README.md"
 
 [project.license]
 text = "MIT"
```

### Comparing `nonebot_plugin_arkgacha-0.1.5/PKG-INFO` & `nonebot_plugin_arkgacha-0.2.0/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,19 +1,21 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-arkgacha
-Version: 0.1.5
+Version: 0.2.0
 Summary: Plugin for Arknights gacha, support multi platform
 Author-Email: RF-Tar-Railt <3165388245@qq.com>
 License: MIT
 Requires-Python: >=3.8
 Requires-Dist: nonebot2>=2.0.0rc4
 Requires-Dist: nonebot-plugin-alconna>=0.4.2
 Requires-Dist: nonebot-plugin-send-anything-anywhere>=0.2.4
-Requires-Dist: arknights-toolkit>=0.5.2
+Requires-Dist: arknights-toolkit>=0.5.4
 Requires-Dist: nonebot-plugin-localstore>=0.4.1
+Requires-Dist: nonebot-plugin-apscheduler>=0.2.0
+Requires-Dist: nepattern>=0.5.7
 Description-Content-Type: text/markdown
 
 <p align="center">
   <a href="https://v2.nonebot.dev/"><img src="https://v2.nonebot.dev/logo.png" width="200" height="200" alt="nonebot"></a>
 </p>
 
 <div align="center">
@@ -37,32 +39,41 @@
 该插件提供了模拟明日方舟抽卡的功能，包括无头形式的抽卡模拟与模拟十连
 
 通过使用 [`saa`](https://github.com/felinae98/nonebot-plugin-send-anything-anywhere) 插件适配多平台
 
 ## 安装
 
 ```bash
-pip install nonebot-plugin-arkgacha
+$ pip install nonebot-plugin-arkgacha
 ```
 
 ```bash
-nb plugin install nonebot-plugin-arkgacha
+$ nb plugin install nonebot-plugin-arkgacha
 ```
 
 **在使用该插件之前，需要先初始化资源**
 
+命令行输入：
 ```bash
-arkkit init
+$ arkkit init -SIMG
 ```
 
 ## 配置
 
 - ARKGACHA_POOL_FILE: 抽卡池文件路径, 不填则使用 [`localstore`](https://github.com/nonebot/plugin-localstore) 保存抽卡池
 - ARKGACHA_MAX: 抽卡最大次数, 默认为 300
 - ARKGACHA_PURE_TEXT: 是否使用纯文本, 默认为 False (十连模拟必须使用图片)
+- ARKGACHA_AUTO_UPDATE: 是否自动更新，默认为 True
+
+## 注意事项
+1. `方舟抽卡` 不需要图片资源, 可在不经过 `arkkit init` 的情况下使用
+2. `方舟十连` 需要图片资源, 需要先在命令行中执行 `arkkit init -SIMG` 初始化资源，否则会出现错误
+3. 若配置，每天 16 点将自动更新卡池资源
+4. 如果获取资源时出现网络错误，请检查代理设置，或尝试访问 PRTS
+
 ## 使用方法
 
 指令如下: 
 > 方舟抽卡
 > 
 > 方舟抽卡 200
 > 
@@ -72,11 +83,7 @@
 
 
 ## 效果
 
 > 方舟十连
 
 ![res](./test.png)
-
-## 注意事项
-1. `方舟抽卡` 不需要图片资源, 可在不经过 `arkkit init` 的情况下使用
-2. `方舟十连` 需要图片资源, 需要先执行 `arkkit init` 初始化资源，否则会出现错误
```

#### html2text {}

```diff
@@ -1,24 +1,29 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-arkgacha Version: 0.1.5 Summary:
+Metadata-Version: 2.1 Name: nonebot-plugin-arkgacha Version: 0.2.0 Summary:
 Plugin for Arknights gacha, support multi platform Author-Email: RF-Tar-Railt
 <3165388245@qq.com> License: MIT Requires-Python: >=3.8 Requires-Dist:
 nonebot2>=2.0.0rc4 Requires-Dist: nonebot-plugin-alconna>=0.4.2 Requires-Dist:
 nonebot-plugin-send-anything-anywhere>=0.2.4 Requires-Dist: arknights-
-toolkit>=0.5.2 Requires-Dist: nonebot-plugin-localstore>=0.4.1 Description-
+toolkit>=0.5.4 Requires-Dist: nonebot-plugin-localstore>=0.4.1 Requires-Dist:
+nonebot-plugin-apscheduler>=0.2.0 Requires-Dist: nepattern>=0.5.7 Description-
 Content-Type: text/markdown
                                    [nonebot]
         # NoneBot Plugin Arkgacha _â¨ ææ¥æ¹èæ½å¡æ¨¡æå¨ â¨_
                            [license] [pypi] [python]
 è¯¥æä»¶æä¾äºæ¨¡æææ¥æ¹èæ½å¡çåè½ï¼åæ¬æ å¤´å½¢å¼çæ½å¡æ¨¡æä¸æ¨¡æåè¿
 éè¿ä½¿ç¨ [`saa`](https://github.com/felinae98/nonebot-plugin-send-anything-
-anywhere) æä»¶ééå¤å¹³å° ## å®è£ ```bash pip install nonebot-plugin-
-arkgacha ``` ```bash nb plugin install nonebot-plugin-arkgacha ```
-**å¨ä½¿ç¨è¯¥æä»¶ä¹åï¼éè¦ååå§åèµæº** ```bash arkkit init ```
-## éç½® - ARKGACHA_POOL_FILE: æ½å¡æ± æä»¶è·¯å¾, ä¸å¡«åä½¿ç¨
-[`localstore`](https://github.com/nonebot/plugin-localstore) ä¿å­æ½å¡æ±  -
-ARKGACHA_MAX: æ½å¡æå¤§æ¬¡æ°, é»è®¤ä¸º 300 - ARKGACHA_PURE_TEXT:
-æ¯å¦ä½¿ç¨çº¯ææ¬, é»è®¤ä¸º False (åè¿æ¨¡æå¿é¡»ä½¿ç¨å¾ç) ##
-ä½¿ç¨æ¹æ³ æä»¤å¦ä¸: > æ¹èæ½å¡ > > æ¹èæ½å¡ 200 > > æ¹èåè¿
-> > æ¹èå¡æ± æ´æ° ## ææ > æ¹èåè¿ ![res](./test.png) ##
-æ³¨æäºé¡¹ 1. `æ¹èæ½å¡` ä¸éè¦å¾çèµæº, å¯å¨ä¸ç»è¿ `arkkit
-init` çæåµä¸ä½¿ç¨ 2. `æ¹èåè¿` éè¦å¾çèµæº, éè¦åæ§è¡
-`arkkit init` åå§åèµæºï¼å¦åä¼åºç°éè¯¯
+anywhere) æä»¶ééå¤å¹³å° ## å®è£ ```bash $ pip install nonebot-plugin-
+arkgacha ``` ```bash $ nb plugin install nonebot-plugin-arkgacha ```
+**å¨ä½¿ç¨è¯¥æä»¶ä¹åï¼éè¦ååå§åèµæº** å½ä»¤è¡è¾å¥ï¼
+```bash $ arkkit init -SIMG ``` ## éç½® - ARKGACHA_POOL_FILE:
+æ½å¡æ± æä»¶è·¯å¾, ä¸å¡«åä½¿ç¨ [`localstore`](https://github.com/
+nonebot/plugin-localstore) ä¿å­æ½å¡æ±  - ARKGACHA_MAX: æ½å¡æå¤§æ¬¡æ°,
+é»è®¤ä¸º 300 - ARKGACHA_PURE_TEXT: æ¯å¦ä½¿ç¨çº¯ææ¬, é»è®¤ä¸º False
+(åè¿æ¨¡æå¿é¡»ä½¿ç¨å¾ç) - ARKGACHA_AUTO_UPDATE:
+æ¯å¦èªå¨æ´æ°ï¼é»è®¤ä¸º True ## æ³¨æäºé¡¹ 1. `æ¹èæ½å¡`
+ä¸éè¦å¾çèµæº, å¯å¨ä¸ç»è¿ `arkkit init` çæåµä¸ä½¿ç¨ 2.
+`æ¹èåè¿` éè¦å¾çèµæº, éè¦åå¨å½ä»¤è¡ä¸­æ§è¡ `arkkit init
+-SIMG` åå§åèµæºï¼å¦åä¼åºç°éè¯¯ 3. è¥éç½®ï¼æ¯å¤© 16
+ç¹å°èªå¨æ´æ°å¡æ± èµæº 4.
+å¦æè·åèµæºæ¶åºç°ç½ç»éè¯¯ï¼è¯·æ£æ¥ä»£çè®¾ç½®ï¼æå°è¯è®¿é®
+PRTS ## ä½¿ç¨æ¹æ³ æä»¤å¦ä¸: > æ¹èæ½å¡ > > æ¹èæ½å¡ 200 > >
+æ¹èåè¿ > > æ¹èå¡æ± æ´æ° ## ææ > æ¹èåè¿ ![res](./test.png)
```

