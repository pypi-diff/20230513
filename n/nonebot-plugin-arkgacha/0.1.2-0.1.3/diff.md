# Comparing `tmp/nonebot_plugin_arkgacha-0.1.2.tar.gz` & `tmp/nonebot_plugin_arkgacha-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_arkgacha-0.1.2.tar", last modified: Fri May 12 14:18:41 2023, max compression
+gzip compressed data, was "nonebot_plugin_arkgacha-0.1.3.tar", last modified: Sat May 13 02:38:34 2023, max compression
```

## Comparing `nonebot_plugin_arkgacha-0.1.2.tar` & `nonebot_plugin_arkgacha-0.1.3.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0    34522 2021-09-10 07:59:22.042000 nonebot_plugin_arkgacha-0.1.2/LICENSE
--rw-r--r--   0        0        0     1553 2023-05-12 12:55:04.474163 nonebot_plugin_arkgacha-0.1.2/README.md
--rw-r--r--   0        0        0     4670 2023-05-12 14:17:30.984598 nonebot_plugin_arkgacha-0.1.2/nonebot_plugin_arkgacha/__init__.py
--rw-r--r--   0        0        0      175 2023-05-12 12:54:47.496416 nonebot_plugin_arkgacha-0.1.2/nonebot_plugin_arkgacha/config.py
--rw-r--r--   0        0        0      631 2023-05-12 14:18:41.034677 nonebot_plugin_arkgacha-0.1.2/pyproject.toml
--rw-r--r--   0        0        0     1968 1970-01-01 00:00:00.000000 nonebot_plugin_arkgacha-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0    34522 2021-09-10 07:59:22.042000 nonebot_plugin_arkgacha-0.1.3/LICENSE
+-rw-r--r--   0        0        0     1772 2023-05-13 02:18:11.841037 nonebot_plugin_arkgacha-0.1.3/README.md
+-rw-r--r--   0        0        0     4705 2023-05-13 02:12:25.739927 nonebot_plugin_arkgacha-0.1.3/nonebot_plugin_arkgacha/__init__.py
+-rw-r--r--   0        0        0      175 2023-05-12 12:54:47.496416 nonebot_plugin_arkgacha-0.1.3/nonebot_plugin_arkgacha/config.py
+-rw-r--r--   0        0        0      631 2023-05-13 02:38:34.676684 nonebot_plugin_arkgacha-0.1.3/pyproject.toml
+-rw-r--r--   0        0        0     2183 1970-01-01 00:00:00.000000 nonebot_plugin_arkgacha-0.1.3/PKG-INFO
```

### Comparing `nonebot_plugin_arkgacha-0.1.2/LICENSE` & `nonebot_plugin_arkgacha-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_arkgacha-0.1.2/README.md` & `nonebot_plugin_arkgacha-0.1.3/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -57,8 +57,12 @@
 > 方舟卡池更新
 
 
 ## 效果
 
 > 方舟十连
 
-![res](./test.png)
+![res](./test.png)
+
+## 注意事项
+1. `方舟抽卡` 不需要图片资源, 可在不经过 `arkkit init` 的情况下使用
+2. `方舟十连` 需要图片资源, 需要先执行 `arkkit init` 初始化资源，否则会出现错误
```

#### html2text {}

```diff
@@ -6,8 +6,11 @@
 anywhere) æä»¶ééå¤å¹³å° ## å®è£ ```bash pip install nonebot-plugin-
 arkgacha ``` ```bash nb plugin install nonebot-plugin-arkgacha ```
 **å¨ä½¿ç¨è¯¥æä»¶ä¹åï¼éè¦ååå§åèµæº** ```bash arkkit init ```
 ## éç½® - ARKGACHA_POOL_FILE: æ½å¡æ± æä»¶è·¯å¾, ä¸å¡«åä½¿ç¨
 [`localstore`](https://github.com/nonebot/plugin-localstore) ä¿å­æ½å¡æ±  -
 ARKGACHA_MAX: æ½å¡æå¤§æ¬¡æ°, é»è®¤ä¸º 300 ## ä½¿ç¨æ¹æ³ æä»¤å¦ä¸: >
 æ¹èæ½å¡ > > æ¹èæ½å¡ 200 > > æ¹èåè¿ > > æ¹èå¡æ± æ´æ° ##
-ææ > æ¹èåè¿ ![res](./test.png)
+ææ > æ¹èåè¿ ![res](./test.png) ## æ³¨æäºé¡¹ 1. `æ¹èæ½å¡`
+ä¸éè¦å¾çèµæº, å¯å¨ä¸ç»è¿ `arkkit init` çæåµä¸ä½¿ç¨ 2.
+`æ¹èåè¿` éè¦å¾çèµæº, éè¦åæ§è¡ `arkkit init`
+åå§åèµæºï¼å¦åä¼åºç°éè¯¯
```

### Comparing `nonebot_plugin_arkgacha-0.1.2/nonebot_plugin_arkgacha/__init__.py` & `nonebot_plugin_arkgacha-0.1.3/nonebot_plugin_arkgacha/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 from arclet.alconna import Alconna, Args, CommandMeta
 from arknights_toolkit.gacha import ArknightsGacha, GachaUser
 
 require("nonebot_plugin_alconna")
 require("nonebot_plugin_localstore")
 require("nonebot_plugin_saa")
 
-from nonebot_plugin_alconna import on_alconna, AlcMatches
+from nonebot_plugin_alconna import on_alconna, AlconnaMatch, Match
 from nonebot_plugin_localstore import get_cache_file, get_data_file
 from nonebot_plugin_saa import MessageFactory, Image
 
 from .config import Config
 
 driver = get_driver()
 global_config = driver.config
@@ -47,20 +47,20 @@
             usage=f"方舟抽卡 [count = 10], count不会超过{config.arkgacha_max}",
             example="方舟抽卡 10",
             compact=True
         )
     ),
     auto_send_output=True,
     comp_config={'timeout': 30},
-    priority=16,
+    priority=15,
     block=True
 )
-simulate_regex = on_fullmatch(r"方舟十连", priority=16, block=True)
-help_regex = on_fullmatch(r"方舟抽卡帮助", priority=16, block=True)
-update_regex = on_fullmatch(r"方舟卡池更新", priority=16, block=True)
+simulate_regex = on_fullmatch("方舟十连", priority=16, block=True)
+help_regex = on_fullmatch("方舟抽卡帮助", priority=16, block=True)
+update_regex = on_fullmatch("方舟卡池更新", priority=16, block=True)
 
 
 @driver.on_shutdown
 async def _():
     with user_cache_file.open("w+", encoding="utf-8") as _f:
         json.dump(userdata, _f, ensure_ascii=False)
 
@@ -87,22 +87,22 @@
             "\n".join(f"{i.name} {'【限定】' if i.limit else '【常驻】'}" for i in new.five_chars)
         )
     else:
         await update_regex.finish("卡池已是最新")
 
 
 @gacha_regex.handle()
-async def _(event: Event, arp: AlcMatches):
+async def _(event: Event, count: Match[int] = AlconnaMatch("count")):
     session = event.get_user_id()
     if session not in userdata:
         user = GachaUser()
         userdata[session] = asdict(user)
     else:
         user = GachaUser(**userdata[session])
-    count = min(max(int(arp.count), 1), config.arkgacha_max)
+    count = min(max(int(count.result), 1), config.arkgacha_max)
 
     img = gacha.gacha_with_img(user, count)
     try:
         await MessageFactory(Image(img)).send()
     except RuntimeError:
         data = gacha.gacha(user, count)
         get_six = {}
```

### Comparing `nonebot_plugin_arkgacha-0.1.2/pyproject.toml` & `nonebot_plugin_arkgacha-0.1.3/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 [project]
 name = "nonebot-plugin-arkgacha"
-version = "0.1.2"
+version = "0.1.3"
 description = "Plugin for Arknights gacha, support multi platform"
 authors = [
     { name = "RF-Tar-Railt", email = "3165388245@qq.com" },
 ]
 dependencies = [
     "nonebot2>=2.0.0rc4",
-    "nonebot-plugin-alconna>=0.4.1",
+    "nonebot-plugin-alconna>=0.4.2",
     "nonebot-plugin-send-anything-anywhere>=0.2.4",
-    "arknights-toolkit>=0.5.1",
+    "arknights-toolkit>=0.5.2",
     "nonebot-plugin-localstore>=0.4.1",
 ]
 requires-python = ">=3.8"
 readme = "README.md"
 
 [project.license]
 text = "MIT"
```

### Comparing `nonebot_plugin_arkgacha-0.1.2/PKG-INFO` & `nonebot_plugin_arkgacha-0.1.3/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-arkgacha
-Version: 0.1.2
+Version: 0.1.3
 Summary: Plugin for Arknights gacha, support multi platform
 Author-Email: RF-Tar-Railt <3165388245@qq.com>
 License: MIT
 Requires-Python: >=3.8
 Requires-Dist: nonebot2>=2.0.0rc4
-Requires-Dist: nonebot-plugin-alconna>=0.4.1
+Requires-Dist: nonebot-plugin-alconna>=0.4.2
 Requires-Dist: nonebot-plugin-send-anything-anywhere>=0.2.4
-Requires-Dist: arknights-toolkit>=0.5.1
+Requires-Dist: arknights-toolkit>=0.5.2
 Requires-Dist: nonebot-plugin-localstore>=0.4.1
 Description-Content-Type: text/markdown
 
 <p align="center">
   <a href="https://v2.nonebot.dev/"><img src="https://v2.nonebot.dev/logo.png" width="200" height="200" alt="nonebot"></a>
 </p>
 
@@ -71,8 +71,12 @@
 > 方舟卡池更新
 
 
 ## 效果
 
 > 方舟十连
 
-![res](./test.png)
+![res](./test.png)
+
+## 注意事项
+1. `方舟抽卡` 不需要图片资源, 可在不经过 `arkkit init` 的情况下使用
+2. `方舟十连` 需要图片资源, 需要先执行 `arkkit init` 初始化资源，否则会出现错误
```

#### html2text {}

```diff
@@ -1,20 +1,23 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-arkgacha Version: 0.1.2 Summary:
+Metadata-Version: 2.1 Name: nonebot-plugin-arkgacha Version: 0.1.3 Summary:
 Plugin for Arknights gacha, support multi platform Author-Email: RF-Tar-Railt
 <3165388245@qq.com> License: MIT Requires-Python: >=3.8 Requires-Dist:
-nonebot2>=2.0.0rc4 Requires-Dist: nonebot-plugin-alconna>=0.4.1 Requires-Dist:
+nonebot2>=2.0.0rc4 Requires-Dist: nonebot-plugin-alconna>=0.4.2 Requires-Dist:
 nonebot-plugin-send-anything-anywhere>=0.2.4 Requires-Dist: arknights-
-toolkit>=0.5.1 Requires-Dist: nonebot-plugin-localstore>=0.4.1 Description-
+toolkit>=0.5.2 Requires-Dist: nonebot-plugin-localstore>=0.4.1 Description-
 Content-Type: text/markdown
                                    [nonebot]
         # NoneBot Plugin Arkgacha _â¨ ææ¥æ¹èæ½å¡æ¨¡æå¨ â¨_
                            [license] [pypi] [python]
 è¯¥æä»¶æä¾äºæ¨¡æææ¥æ¹èæ½å¡çåè½ï¼åæ¬æ å¤´å½¢å¼çæ½å¡æ¨¡æä¸æ¨¡æåè¿
 éè¿ä½¿ç¨ [`saa`](https://github.com/felinae98/nonebot-plugin-send-anything-
 anywhere) æä»¶ééå¤å¹³å° ## å®è£ ```bash pip install nonebot-plugin-
 arkgacha ``` ```bash nb plugin install nonebot-plugin-arkgacha ```
 **å¨ä½¿ç¨è¯¥æä»¶ä¹åï¼éè¦ååå§åèµæº** ```bash arkkit init ```
 ## éç½® - ARKGACHA_POOL_FILE: æ½å¡æ± æä»¶è·¯å¾, ä¸å¡«åä½¿ç¨
 [`localstore`](https://github.com/nonebot/plugin-localstore) ä¿å­æ½å¡æ±  -
 ARKGACHA_MAX: æ½å¡æå¤§æ¬¡æ°, é»è®¤ä¸º 300 ## ä½¿ç¨æ¹æ³ æä»¤å¦ä¸: >
 æ¹èæ½å¡ > > æ¹èæ½å¡ 200 > > æ¹èåè¿ > > æ¹èå¡æ± æ´æ° ##
-ææ > æ¹èåè¿ ![res](./test.png)
+ææ > æ¹èåè¿ ![res](./test.png) ## æ³¨æäºé¡¹ 1. `æ¹èæ½å¡`
+ä¸éè¦å¾çèµæº, å¯å¨ä¸ç»è¿ `arkkit init` çæåµä¸ä½¿ç¨ 2.
+`æ¹èåè¿` éè¦å¾çèµæº, éè¦åæ§è¡ `arkkit init`
+åå§åèµæºï¼å¦åä¼åºç°éè¯¯
```

