# Comparing `tmp/nonebot_plugin_gscode-0.1.6.tar.gz` & `tmp/nonebot_plugin_gscode-0.1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_gscode-0.1.6.tar", max compression
+gzip compressed data, was "nonebot_plugin_gscode-0.1.7.tar", max compression
```

## Comparing `nonebot_plugin_gscode-0.1.6.tar` & `nonebot_plugin_gscode-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,6 @@
--rw-r--r--   0        0        0     1067 2023-02-16 12:47:41.950554 nonebot_plugin_gscode-0.1.6/LICENSE
--rw-r--r--   0        0        0     1950 2023-02-16 12:47:41.950554 nonebot_plugin_gscode-0.1.6/README.md
--rw-r--r--   0        0        0     1032 2023-02-16 12:47:41.950554 nonebot_plugin_gscode-0.1.6/nonebot_plugin_gscode/__init__.py
--rw-r--r--   0        0        0     5226 2023-02-16 12:47:41.950554 nonebot_plugin_gscode-0.1.6/nonebot_plugin_gscode/data_source.py
--rw-r--r--   0        0        0     1739 2023-02-16 12:47:41.950554 nonebot_plugin_gscode-0.1.6/pyproject.toml
--rw-r--r--   0        0        0     2753 1970-01-01 00:00:00.000000 nonebot_plugin_gscode-0.1.6/setup.py
--rw-r--r--   0        0        0     2780 1970-01-01 00:00:00.000000 nonebot_plugin_gscode-0.1.6/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-05-13 17:01:10.822822 nonebot_plugin_gscode-0.1.7/LICENSE
+-rw-r--r--   0        0        0     1950 2023-05-13 17:01:10.822822 nonebot_plugin_gscode-0.1.7/README.md
+-rw-r--r--   0        0        0     1032 2023-05-13 17:01:10.822822 nonebot_plugin_gscode-0.1.7/nonebot_plugin_gscode/__init__.py
+-rw-r--r--   0        0        0     5219 2023-05-13 17:01:10.822822 nonebot_plugin_gscode-0.1.7/nonebot_plugin_gscode/data_source.py
+-rw-r--r--   0        0        0     1739 2023-05-13 17:01:10.822822 nonebot_plugin_gscode-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0     2780 1970-01-01 00:00:00.000000 nonebot_plugin_gscode-0.1.7/PKG-INFO
```

### Comparing `nonebot_plugin_gscode-0.1.6/LICENSE` & `nonebot_plugin_gscode-0.1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_gscode-0.1.6/README.md` & `nonebot_plugin_gscode-0.1.7/README.md`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_gscode-0.1.6/nonebot_plugin_gscode/__init__.py` & `nonebot_plugin_gscode-0.1.7/nonebot_plugin_gscode/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_gscode-0.1.6/nonebot_plugin_gscode/data_source.py` & `nonebot_plugin_gscode-0.1.7/nonebot_plugin_gscode/data_source.py`

 * *Files 2% similar despite different names*

```diff
@@ -46,15 +46,15 @@
             continue
         if not all(word in post["subject"] for word in keywords):
             continue
         shit = json.loads(post["structured_content"])
         for segment in shit:
             link = segment.get("attributes", {}).get("link", "")
             if "观看直播" in segment.get("insert", "") and link:
-                matched = findall(r"act_id=(\d{8}ys\d{4})", link)
+                matched = findall(r"act_id=(.*?)\&", link)
                 if matched:
                     actId = matched[0]
         if actId:
             break
 
     return actId
```

### Comparing `nonebot_plugin_gscode-0.1.6/pyproject.toml` & `nonebot_plugin_gscode-0.1.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "nonebot-plugin-gscode"
-version = "0.1.6"
+version = "0.1.7"
 description = "Genshin live codes plugin for NoneBot2"
 authors = ["monsterxcn <monsterxcn@gmail.com>"]
 documentation = "https://github.com/monsterxcn/nonebot-plugin-gscode#readme"
 license = "MIT"
 homepage = "https://github.com/monsterxcn/nonebot-plugin-gscode"
 readme = "README.md"
 keywords = ["nonebot", "nonebot2", "genshin", "live", "code", "redeem"]
```

### Comparing `nonebot_plugin_gscode-0.1.6/setup.py` & `nonebot_plugin_gscode-0.1.7/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,30 +1,68 @@
-# -*- coding: utf-8 -*-
-from setuptools import setup
+Metadata-Version: 2.1
+Name: nonebot-plugin-gscode
+Version: 0.1.7
+Summary: Genshin live codes plugin for NoneBot2
+Home-page: https://github.com/monsterxcn/nonebot-plugin-gscode
+License: MIT
+Keywords: nonebot,nonebot2,genshin,live,code,redeem
+Author: monsterxcn
+Author-email: monsterxcn@gmail.com
+Requires-Python: >=3.8.1,<4.0
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Dist: httpx (>=0.20.0,<1.0.0)
+Requires-Dist: nonebot-adapter-onebot (>=2.0.0b1)
+Requires-Dist: nonebot2 (>=2.0.0b3)
+Project-URL: Documentation, https://github.com/monsterxcn/nonebot-plugin-gscode#readme
+Description-Content-Type: text/markdown
 
-packages = \
-['nonebot_plugin_gscode']
+<h1 align="center">NoneBot Plugin GsCode</h1></br>
 
-package_data = \
-{'': ['*']}
 
-install_requires = \
-['httpx>=0.20.0,<1.0.0', 'nonebot-adapter-onebot>=2.0.0b1', 'nonebot2>=2.0.0b3']
-
-setup_kwargs = {
-    'name': 'nonebot-plugin-gscode',
-    'version': '0.1.6',
-    'description': 'Genshin live codes plugin for NoneBot2',
-    'long_description': '<h1 align="center">NoneBot Plugin GsCode</h1></br>\n\n\n<p align="center">🤖 用于查询原神前瞻直播兑换码的 NoneBot2 插件</p></br>\n\n\n<p align="center">\n  <a href="https://raw.githubusercontent.com/monsterxcn/nonebot-plugin-gscode/master/LICENSE"><img src="https://img.shields.io/github/license/monsterxcn/nonebot-plugin-gscode?style=flat-square" alt="license" /></a>\n  <a href="https://pypi.python.org/pypi/nonebot-plugin-gscode"><img src="https://img.shields.io/pypi/v/nonebot-plugin-gscode?style=flat-square" alt="pypi" /></a>\n  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/python-3.8+-blue?style=flat-square" alt="python" /></a>\n  <a href="https://jq.qq.com/?_wv=1027&k=GF2vqPgf"><img src="https://img.shields.io/badge/QQ%E7%BE%A4-662597191-orange?style=flat-square" alt="QQ Chat Group" /></a><br />\n</p></br>\n\n\n| ![image](https://user-images.githubusercontent.com/22407052/204017447-84f300f4-0df2-44df-ac3e-4bc72a47d816.png) | ![image](https://user-images.githubusercontent.com/22407052/204016397-2c2063cb-9e0d-4060-808d-32b2bb84bc69.png) |\n|:--:|:--:|\n\n\n## 安装方法\n\n\n如果你正在使用 2.0.0.beta1 以上版本 NoneBot，推荐使用以下命令安装：\n\n\n```bash\n# 从 nb_cli 安装\nnb plugin install nonebot-plugin-gscode\n```\n\n\n## 使用说明\n\n\n插件响应 `gscode` / `兑换码`，返回一组包含兑换码信息的合并转发消息。\n\n\n经测试，兑换码接口返回与前瞻直播有 2 分钟左右延迟，应为正常现象，请耐心等待。\n\n\n插件依赖 [@Mrs4s/go-cqhttp](https://github.com/Mrs4s/go-cqhttp) 的合并转发接口，如需启用私聊响应请务必安装 [v1.0.0-rc2](https://github.com/Mrs4s/go-cqhttp/releases/tag/v1.0.0-rc2) 以上版本的 go-cqhttp。\n\n\n## 特别鸣谢\n\n\n[@nonebot/nonebot2](https://github.com/nonebot/nonebot2/) | [@Mrs4s/go-cqhttp](https://github.com/Mrs4s/go-cqhttp) | [@Le-niao/Yunzai-Bot](https://github.com/Le-niao/Yunzai-Bot)\n',
-    'author': 'monsterxcn',
-    'author_email': 'monsterxcn@gmail.com',
-    'maintainer': 'None',
-    'maintainer_email': 'None',
-    'url': 'https://github.com/monsterxcn/nonebot-plugin-gscode',
-    'packages': packages,
-    'package_data': package_data,
-    'install_requires': install_requires,
-    'python_requires': '>=3.8.1,<4.0',
-}
+<p align="center">🤖 用于查询原神前瞻直播兑换码的 NoneBot2 插件</p></br>
 
 
-setup(**setup_kwargs)
+<p align="center">
+  <a href="https://raw.githubusercontent.com/monsterxcn/nonebot-plugin-gscode/master/LICENSE"><img src="https://img.shields.io/github/license/monsterxcn/nonebot-plugin-gscode?style=flat-square" alt="license" /></a>
+  <a href="https://pypi.python.org/pypi/nonebot-plugin-gscode"><img src="https://img.shields.io/pypi/v/nonebot-plugin-gscode?style=flat-square" alt="pypi" /></a>
+  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/python-3.8+-blue?style=flat-square" alt="python" /></a>
+  <a href="https://jq.qq.com/?_wv=1027&k=GF2vqPgf"><img src="https://img.shields.io/badge/QQ%E7%BE%A4-662597191-orange?style=flat-square" alt="QQ Chat Group" /></a><br />
+</p></br>
+
+
+| ![image](https://user-images.githubusercontent.com/22407052/204017447-84f300f4-0df2-44df-ac3e-4bc72a47d816.png) | ![image](https://user-images.githubusercontent.com/22407052/204016397-2c2063cb-9e0d-4060-808d-32b2bb84bc69.png) |
+|:--:|:--:|
+
+
+## 安装方法
+
+
+如果你正在使用 2.0.0.beta1 以上版本 NoneBot，推荐使用以下命令安装：
+
+
+```bash
+# 从 nb_cli 安装
+nb plugin install nonebot-plugin-gscode
+```
+
+
+## 使用说明
+
+
+插件响应 `gscode` / `兑换码`，返回一组包含兑换码信息的合并转发消息。
+
+
+经测试，兑换码接口返回与前瞻直播有 2 分钟左右延迟，应为正常现象，请耐心等待。
+
+
+插件依赖 [@Mrs4s/go-cqhttp](https://github.com/Mrs4s/go-cqhttp) 的合并转发接口，如需启用私聊响应请务必安装 [v1.0.0-rc2](https://github.com/Mrs4s/go-cqhttp/releases/tag/v1.0.0-rc2) 以上版本的 go-cqhttp。
+
+
+## 特别鸣谢
+
+
+[@nonebot/nonebot2](https://github.com/nonebot/nonebot2/) | [@Mrs4s/go-cqhttp](https://github.com/Mrs4s/go-cqhttp) | [@Le-niao/Yunzai-Bot](https://github.com/Le-niao/Yunzai-Bot)
+
```

#### html2text {}

```diff
@@ -1,34 +1,31 @@
-# -*- coding: utf-8 -*- from setuptools import setup packages = \
-['nonebot_plugin_gscode'] package_data = \ {'': ['*']} install_requires = \
-['httpx>=0.20.0,<1.0.0', 'nonebot-adapter-onebot>=2.0.0b1',
-'nonebot2>=2.0.0b3'] setup_kwargs = { 'name': 'nonebot-plugin-gscode',
-'version': '0.1.6', 'description': 'Genshin live codes plugin for NoneBot2',
-'long_description': '
+Metadata-Version: 2.1 Name: nonebot-plugin-gscode Version: 0.1.7 Summary:
+Genshin live codes plugin for NoneBot2 Home-page: https://github.com/
+monsterxcn/nonebot-plugin-gscode License: MIT Keywords:
+nonebot,nonebot2,genshin,live,code,redeem Author: monsterxcn Author-email:
+monsterxcn@gmail.com Requires-Python: >=3.8.1,<4.0 Classifier: License :: OSI
+Approved :: MIT License Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.9 Classifier: Programming
+Language :: Python :: 3.10 Classifier: Programming Language :: Python :: 3.11
+Requires-Dist: httpx (>=0.20.0,<1.0.0) Requires-Dist: nonebot-adapter-onebot
+(>=2.0.0b1) Requires-Dist: nonebot2 (>=2.0.0b3) Project-URL: Documentation,
+https://github.com/monsterxcn/nonebot-plugin-gscode#readme Description-Content-
+Type: text/markdown
                       ****** NoneBot Plugin GsCode ******
-\n\n\n
         ð¤ ç¨äºæ¥è¯¢åç¥åç»ç´æ­åæ¢ç ç NoneBot2 æä»¶
-\n\n\n
-              \n [license]\n [pypi]\n [python]\n [QQ_Chat_Group]
-                                      \n
-\n\n\n| ![image](https://user-images.githubusercontent.com/22407052/204017447-
+                   [license] [pypi] [python] [QQ_Chat_Group]
+| ![image](https://user-images.githubusercontent.com/22407052/204017447-
 84f300f4-0df2-44df-ac3e-4bc72a47d816.png) | ![image](https://user-
 images.githubusercontent.com/22407052/204016397-2c2063cb-9e0d-4060-808d-
-32b2bb84bc69.png) |\n|:--:|:--:|\n\n\n##
-å®è£æ¹æ³\n\n\nå¦æä½ æ­£å¨ä½¿ç¨ 2.0.0.beta1 ä»¥ä¸çæ¬
-NoneBotï¼æ¨èä½¿ç¨ä»¥ä¸å½ä»¤å®è£ï¼\n\n\n```bash\n# ä» nb_cli
-å®è£\nnb plugin install nonebot-plugin-gscode\n```\n\n\n##
-ä½¿ç¨è¯´æ\n\n\næä»¶ååº `gscode` /
-`åæ¢ç `ï¼è¿åä¸ç»åå«åæ¢ç ä¿¡æ¯çåå¹¶è½¬åæ¶æ¯ã\n\n\nç»æµè¯ï¼åæ¢ç æ¥å£è¿åä¸åç»ç´æ­æ
-2
-åéå·¦å³å»¶è¿ï¼åºä¸ºæ­£å¸¸ç°è±¡ï¼è¯·èå¿ç­å¾ã\n\n\næä»¶ä¾èµ
+32b2bb84bc69.png) | |:--:|:--:| ## å®è£æ¹æ³ å¦æä½ æ­£å¨ä½¿ç¨
+2.0.0.beta1 ä»¥ä¸çæ¬ NoneBotï¼æ¨èä½¿ç¨ä»¥ä¸å½ä»¤å®è£ï¼ ```bash #
+ä» nb_cli å®è£ nb plugin install nonebot-plugin-gscode ``` ## ä½¿ç¨è¯´æ
+æä»¶ååº `gscode` /
+`åæ¢ç `ï¼è¿åä¸ç»åå«åæ¢ç ä¿¡æ¯çåå¹¶è½¬åæ¶æ¯ã
+ç»æµè¯ï¼åæ¢ç æ¥å£è¿åä¸åç»ç´æ­æ 2
+åéå·¦å³å»¶è¿ï¼åºä¸ºæ­£å¸¸ç°è±¡ï¼è¯·èå¿ç­å¾ã æä»¶ä¾èµ
 [@Mrs4s/go-cqhttp](https://github.com/Mrs4s/go-cqhttp)
 çåå¹¶è½¬åæ¥å£ï¼å¦éå¯ç¨ç§èååºè¯·å¡å¿å®è£ [v1.0.0-rc2]
 (https://github.com/Mrs4s/go-cqhttp/releases/tag/v1.0.0-rc2) ä»¥ä¸çæ¬ç
-go-cqhttpã\n\n\n## ç¹å«é¸£è°¢\n\n\n[@nonebot/nonebot2](https://github.com/
-nonebot/nonebot2/) | [@Mrs4s/go-cqhttp](https://github.com/Mrs4s/go-cqhttp) |
-[@Le-niao/Yunzai-Bot](https://github.com/Le-niao/Yunzai-Bot)\n', 'author':
-'monsterxcn', 'author_email': 'monsterxcn@gmail.com', 'maintainer': 'None',
-'maintainer_email': 'None', 'url': 'https://github.com/monsterxcn/nonebot-
-plugin-gscode', 'packages': packages, 'package_data': package_data,
-'install_requires': install_requires, 'python_requires': '>=3.8.1,<4.0', }
-setup(**setup_kwargs)
+go-cqhttpã ## ç¹å«é¸£è°¢ [@nonebot/nonebot2](https://github.com/nonebot/
+nonebot2/) | [@Mrs4s/go-cqhttp](https://github.com/Mrs4s/go-cqhttp) | [@Le-
+niao/Yunzai-Bot](https://github.com/Le-niao/Yunzai-Bot)
```

