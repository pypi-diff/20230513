# Comparing `tmp/nonebot_plugin_segbuilder-0.1.1.tar.gz` & `tmp/nonebot_plugin_segbuilder-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_segbuilder-0.1.1.tar", last modified: Thu May 11 15:07:53 2023, max compression
+gzip compressed data, was "nonebot_plugin_segbuilder-0.2.0.tar", last modified: Sat May 13 06:53:55 2023, max compression
```

## Comparing `nonebot_plugin_segbuilder-0.1.1.tar` & `nonebot_plugin_segbuilder-0.2.0.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rw-r--r--   0        0        0     1064 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/LICENSE
--rw-r--r--   0        0        0     5229 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/README.md
--rw-r--r--   0        0        0       95 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/__init__.py
--rw-r--r--   0        0        0     1664 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/archive/kaiheila.py
--rw-r--r--   0        0        0     1789 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/mirai2.py
--rw-r--r--   0        0        0     1011 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/onebot_v11.py
--rw-r--r--   0        0        0     1503 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/onebot_v12.py
--rw-r--r--   0        0        0     1367 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/qqguild.py
--rw-r--r--   0        0        0     2768 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/base.py
--rw-r--r--   0        0        0      569 2023-05-11 15:07:38.655869 nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/utils.py
--rw-r--r--   0        0        0      758 2023-05-11 15:07:53.627935 nonebot_plugin_segbuilder-0.1.1/pyproject.toml
--rw-r--r--   0        0        0     5983 1970-01-01 00:00:00.000000 nonebot_plugin_segbuilder-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0     1064 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/LICENSE
+-rw-r--r--   0        0        0     6321 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/README.md
+-rw-r--r--   0        0        0       95 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/__init__.py
+-rw-r--r--   0        0        0     1664 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/archive/kaiheila.py
+-rw-r--r--   0        0        0     1789 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/mirai2.py
+-rw-r--r--   0        0        0     1011 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/onebot_v11.py
+-rw-r--r--   0        0        0     1503 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/onebot_v12.py
+-rw-r--r--   0        0        0     1367 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/qqguild.py
+-rw-r--r--   0        0        0     2543 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/base.py
+-rw-r--r--   0        0        0      569 2023-05-13 06:53:45.604260 nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/utils.py
+-rw-r--r--   0        0        0      758 2023-05-13 06:53:55.308322 nonebot_plugin_segbuilder-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0     7075 1970-01-01 00:00:00.000000 nonebot_plugin_segbuilder-0.2.0/PKG-INFO
```

### Comparing `nonebot_plugin_segbuilder-0.1.1/LICENSE` & `nonebot_plugin_segbuilder-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_segbuilder-0.1.1/README.md` & `nonebot_plugin_segbuilder-0.2.0/README.md`

 * *Files 25% similar despite different names*

```diff
@@ -57,14 +57,33 @@
 
 ## 📖 介绍
 
 `nonebot-plugin-segbuilder` 是帮助**开发者**快速构建跨平台消息段的应用的工具。相较于 saa ([nonebot-plugin-send-anything-anywhere](https://github.com/felinae98/nonebot-plugin-send-anything-anywhere)) 包办了消息构建与发送，本插件仅实现了消息段构建，更加符合 NoneBot2 原生的编写流程，同时也更易拓展与理解。
 
 但与之相对的，面对与 QQ 消息类型相差越大的平台，这种发送方式的兼容性也会越差，而本插件由于仅负责了消息段构建而不少问题是发送时才会抛出，因此本插件的使用体验下限将远低于 saa。但如果你能接受一定程度的平台相关处理或仅在类 qq 的平台(如 OB11 和 OB12)，本插件的上限也将高于 saa。
 
+## 🥳 适配器支持状态
+
+~~屑屑 msgbuf 的 README(https://github.com/NCBM/nonebot-plugin-msgbuf)~~
+
+- ✅: 完全支持
+- 🟨: 部分支持，由于平台限制需要用户额外分平台处理
+- 🚧: 临时不支持，但后续可能会修复
+- ❌: 永久不支持，通常是平台不支持此功能或实现过于复杂
+- 🔧: 预期支持
+
+|  Adapters  | Text | image | at(@) | reply(quote) | face | voice | video | file | share | location |
+| :--------: | :--: | :---: | :---: | :----------: | :--: | :---: | :---: | :--: | :---: | :------: |
+| OneBot V11 |  ✅  |  ✅   |  ✅   |      ✅      |  🔧  |  🔧   |  🔧   |  🔧  |  🔧   |    🔧    |
+| OneBot V12 |  ✅  |  ✅   |  ✅   |      ✅      |  🔧  |  🔧   |  🔧   |  🔧  |  🔧   |    🔧    |
+|   mirai2   |  ✅  |  ✅   |  ✅   |      🚧      |  🔧  |  🔧   |  🔧   |  🔧  |  🔧   |    🔧    |
+|  qqguild   |  ✅  |  ✅   |  ✅   |      🚧      |  🔧  |  ❌   |  ❌   |  ❌  |  ❌   |    ❌    |
+
+对于不支持的适配器，将会统一转为文字回复
+
 ## 💿 安装
 
 <details>
 <summary>使用 nb-cli 安装</summary>
 在 nonebot2 项目的根目录下打开命令行, 输入以下指令即可安装
 
     nb plugin install nonebot-plugin-segbuilder
```

#### html2text {}

```diff
@@ -12,16 +12,29 @@
 saa ([nonebot-plugin-send-anything-anywhere](https://github.com/felinae98/
 nonebot-plugin-send-anything-anywhere))
 ååäºæ¶æ¯æå»ºä¸åéï¼æ¬æä»¶ä»å®ç°äºæ¶æ¯æ®µæå»ºï¼æ´å ç¬¦å
 NoneBot2 åççç¼åæµç¨ï¼åæ¶ä¹æ´ææå±ä¸çè§£ã
 ä½ä¸ä¹ç¸å¯¹çï¼é¢å¯¹ä¸ QQ
 æ¶æ¯ç±»åç¸å·®è¶å¤§çå¹³å°ï¼è¿ç§åéæ¹å¼çå¼å®¹æ§ä¹ä¼è¶å·®ï¼èæ¬æä»¶ç±äºä»è´è´£äºæ¶æ¯æ®µæå»ºèä¸å°é®é¢æ¯åéæ¶æä¼æåºï¼å æ­¤æ¬æä»¶çä½¿ç¨ä½éªä¸éå°è¿ä½äº
 saaãä½å¦æä½ è½æ¥åä¸å®ç¨åº¦çå¹³å°ç¸å³å¤çæä»å¨ç±» qq
-çå¹³å°(å¦ OB11 å OB12)ï¼æ¬æä»¶çä¸éä¹å°é«äº saaã ## ð¿
-å®è£  ä½¿ç¨ nb-cli å®è£ å¨ nonebot2 é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡,
+çå¹³å°(å¦ OB11 å OB12)ï¼æ¬æä»¶çä¸éä¹å°é«äº saaã ## ð¥³
+ééå¨æ¯æç¶æ ~~å±å± msgbuf ç README(https://github.com/NCBM/
+nonebot-plugin-msgbuf)~~ - â: å®å¨æ¯æ - ð¨:
+é¨åæ¯æï¼ç±äºå¹³å°éå¶éè¦ç¨æ·é¢å¤åå¹³å°å¤ç - ð§:
+ä¸´æ¶ä¸æ¯æï¼ä½åç»­å¯è½ä¼ä¿®å¤ - â:
+æ°¸ä¹ä¸æ¯æï¼éå¸¸æ¯å¹³å°ä¸æ¯ææ­¤åè½æå®ç°è¿äºå¤æ -
+ð§: é¢ææ¯æ | Adapters | Text | image | at(@) | reply(quote) | face |
+voice | video | file | share | location | | :--------: | :--: | :---: | :---: |
+:----------: | :--: | :---: | :---: | :--: | :---: | :------: | | OneBot V11 |
+â | â | â | â | ð§ | ð§ | ð§ | ð§ | ð§ | ð§ | | OneBot V12
+| â | â | â | â | ð§ | ð§ | ð§ | ð§ | ð§ | ð§ | | mirai2 |
+â | â | â | ð§ | ð§ | ð§ | ð§ | ð§ | ð§ | ð§ | | qqguild |
+â | â | â | ð§ | ð§ | â | â | â | â | â |
+å¯¹äºä¸æ¯æçééå¨ï¼å°ä¼ç»ä¸è½¬ä¸ºæå­åå¤ ## ð¿ å®è£
+ä½¿ç¨ nb-cli å®è£ å¨ nonebot2 é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡,
 è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ nb plugin install nonebot-plugin-segbuilder
 æå¼ nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç `pyproject.toml` æä»¶, å¨ `
 [tool.nonebot]` é¨å**å»ææ¬æä»¶**,
 å¦åå°æ¦çå¯è½é æå è½½å¤±è´¥   ä½¿ç¨åç®¡çå¨å®è£ å¨ nonebot2
 é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, æ ¹æ®ä½ ä½¿ç¨çåç®¡çå¨,
 è¾å¥ç¸åºçå®è£å½ä»¤  pip pip install nonebot-plugin-segbuilder   pdm
 pdm add nonebot-plugin-segbuilder   poetry poetry add nonebot-plugin-segbuilder
```

### Comparing `nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/archive/kaiheila.py` & `nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/archive/kaiheila.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/mirai2.py` & `nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/mirai2.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/onebot_v11.py` & `nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/onebot_v11.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/onebot_v12.py` & `nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/onebot_v12.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/adapters/qqguild.py` & `nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/adapters/qqguild.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_segbuilder-0.1.1/nonebot_plugin_segbuilder/utils.py` & `nonebot_plugin_segbuilder-0.2.0/nonebot_plugin_segbuilder/utils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_segbuilder-0.1.1/pyproject.toml` & `nonebot_plugin_segbuilder-0.2.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 [tool.pdm]
 
 [project]
 name = "nonebot-plugin-segbuilder"
-version = "0.1.1"
+version = "0.2.0"
 description = "为不同的适配器提供更通用且简易的消息段构建方式"
 authors = [
     { name = "Well404", email = "well_404@outlook.com" },
 ]
 dependencies = [
     "anyio>=3.4.0",
     "nonebot-adapter-onebot>=2.2.2",
```

### Comparing `nonebot_plugin_segbuilder-0.1.1/PKG-INFO` & `nonebot_plugin_segbuilder-0.2.0/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-segbuilder
-Version: 0.1.1
+Version: 0.2.0
 Summary: 为不同的适配器提供更通用且简易的消息段构建方式
 Author-Email: Well404 <well_404@outlook.com>
 License: MIT
 Requires-Python: >=3.8
 Requires-Dist: anyio>=3.4.0
 Requires-Dist: nonebot-adapter-onebot>=2.2.2
 Requires-Dist: nonebot-adapter-qqguild>=0.2.1
@@ -77,14 +77,33 @@
 
 ## 📖 介绍
 
 `nonebot-plugin-segbuilder` 是帮助**开发者**快速构建跨平台消息段的应用的工具。相较于 saa ([nonebot-plugin-send-anything-anywhere](https://github.com/felinae98/nonebot-plugin-send-anything-anywhere)) 包办了消息构建与发送，本插件仅实现了消息段构建，更加符合 NoneBot2 原生的编写流程，同时也更易拓展与理解。
 
 但与之相对的，面对与 QQ 消息类型相差越大的平台，这种发送方式的兼容性也会越差，而本插件由于仅负责了消息段构建而不少问题是发送时才会抛出，因此本插件的使用体验下限将远低于 saa。但如果你能接受一定程度的平台相关处理或仅在类 qq 的平台(如 OB11 和 OB12)，本插件的上限也将高于 saa。
 
+## 🥳 适配器支持状态
+
+~~屑屑 msgbuf 的 README(https://github.com/NCBM/nonebot-plugin-msgbuf)~~
+
+- ✅: 完全支持
+- 🟨: 部分支持，由于平台限制需要用户额外分平台处理
+- 🚧: 临时不支持，但后续可能会修复
+- ❌: 永久不支持，通常是平台不支持此功能或实现过于复杂
+- 🔧: 预期支持
+
+|  Adapters  | Text | image | at(@) | reply(quote) | face | voice | video | file | share | location |
+| :--------: | :--: | :---: | :---: | :----------: | :--: | :---: | :---: | :--: | :---: | :------: |
+| OneBot V11 |  ✅  |  ✅   |  ✅   |      ✅      |  🔧  |  🔧   |  🔧   |  🔧  |  🔧   |    🔧    |
+| OneBot V12 |  ✅  |  ✅   |  ✅   |      ✅      |  🔧  |  🔧   |  🔧   |  🔧  |  🔧   |    🔧    |
+|   mirai2   |  ✅  |  ✅   |  ✅   |      🚧      |  🔧  |  🔧   |  🔧   |  🔧  |  🔧   |    🔧    |
+|  qqguild   |  ✅  |  ✅   |  ✅   |      🚧      |  🔧  |  ❌   |  ❌   |  ❌  |  ❌   |    ❌    |
+
+对于不支持的适配器，将会统一转为文字回复
+
 ## 💿 安装
 
 <details>
 <summary>使用 nb-cli 安装</summary>
 在 nonebot2 项目的根目录下打开命令行, 输入以下指令即可安装
 
     nb plugin install nonebot-plugin-segbuilder
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-segbuilder Version: 0.1.1 Summary:
+Metadata-Version: 2.1 Name: nonebot-plugin-segbuilder Version: 0.2.0 Summary:
 ä¸ºä¸åçééå¨æä¾æ´éç¨ä¸ç®æçæ¶æ¯æ®µæå»ºæ¹å¼ Author-
 Email: Well404
 outlook.com> License: MIT Requires-Python: >=3.8 Requires-Dist: anyio>=3.4.0
 Requires-Dist: nonebot-adapter-onebot>=2.2.2 Requires-Dist: nonebot-adapter-
 qqguild>=0.2.1 Requires-Dist: nonebot-adapter-mirai2>=0.0.22 Requires-Dist:
 httpx>=0.20.0 Requires-Dist: nonebot2[fastapi,websockets]>=2.0.0rc4; extra ==
 "dev" Requires-Dist: pytest-asyncio>=0.21.0; extra == "dev" Requires-Dist:
@@ -22,16 +22,29 @@
 saa ([nonebot-plugin-send-anything-anywhere](https://github.com/felinae98/
 nonebot-plugin-send-anything-anywhere))
 ååäºæ¶æ¯æå»ºä¸åéï¼æ¬æä»¶ä»å®ç°äºæ¶æ¯æ®µæå»ºï¼æ´å ç¬¦å
 NoneBot2 åççç¼åæµç¨ï¼åæ¶ä¹æ´ææå±ä¸çè§£ã
 ä½ä¸ä¹ç¸å¯¹çï¼é¢å¯¹ä¸ QQ
 æ¶æ¯ç±»åç¸å·®è¶å¤§çå¹³å°ï¼è¿ç§åéæ¹å¼çå¼å®¹æ§ä¹ä¼è¶å·®ï¼èæ¬æä»¶ç±äºä»è´è´£äºæ¶æ¯æ®µæå»ºèä¸å°é®é¢æ¯åéæ¶æä¼æåºï¼å æ­¤æ¬æä»¶çä½¿ç¨ä½éªä¸éå°è¿ä½äº
 saaãä½å¦æä½ è½æ¥åä¸å®ç¨åº¦çå¹³å°ç¸å³å¤çæä»å¨ç±» qq
-çå¹³å°(å¦ OB11 å OB12)ï¼æ¬æä»¶çä¸éä¹å°é«äº saaã ## ð¿
-å®è£  ä½¿ç¨ nb-cli å®è£ å¨ nonebot2 é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡,
+çå¹³å°(å¦ OB11 å OB12)ï¼æ¬æä»¶çä¸éä¹å°é«äº saaã ## ð¥³
+ééå¨æ¯æç¶æ ~~å±å± msgbuf ç README(https://github.com/NCBM/
+nonebot-plugin-msgbuf)~~ - â: å®å¨æ¯æ - ð¨:
+é¨åæ¯æï¼ç±äºå¹³å°éå¶éè¦ç¨æ·é¢å¤åå¹³å°å¤ç - ð§:
+ä¸´æ¶ä¸æ¯æï¼ä½åç»­å¯è½ä¼ä¿®å¤ - â:
+æ°¸ä¹ä¸æ¯æï¼éå¸¸æ¯å¹³å°ä¸æ¯ææ­¤åè½æå®ç°è¿äºå¤æ -
+ð§: é¢ææ¯æ | Adapters | Text | image | at(@) | reply(quote) | face |
+voice | video | file | share | location | | :--------: | :--: | :---: | :---: |
+:----------: | :--: | :---: | :---: | :--: | :---: | :------: | | OneBot V11 |
+â | â | â | â | ð§ | ð§ | ð§ | ð§ | ð§ | ð§ | | OneBot V12
+| â | â | â | â | ð§ | ð§ | ð§ | ð§ | ð§ | ð§ | | mirai2 |
+â | â | â | ð§ | ð§ | ð§ | ð§ | ð§ | ð§ | ð§ | | qqguild |
+â | â | â | ð§ | ð§ | â | â | â | â | â |
+å¯¹äºä¸æ¯æçééå¨ï¼å°ä¼ç»ä¸è½¬ä¸ºæå­åå¤ ## ð¿ å®è£
+ä½¿ç¨ nb-cli å®è£ å¨ nonebot2 é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡,
 è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ nb plugin install nonebot-plugin-segbuilder
 æå¼ nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç `pyproject.toml` æä»¶, å¨ `
 [tool.nonebot]` é¨å**å»ææ¬æä»¶**,
 å¦åå°æ¦çå¯è½é æå è½½å¤±è´¥   ä½¿ç¨åç®¡çå¨å®è£ å¨ nonebot2
 é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, æ ¹æ®ä½ ä½¿ç¨çåç®¡çå¨,
 è¾å¥ç¸åºçå®è£å½ä»¤  pip pip install nonebot-plugin-segbuilder   pdm
 pdm add nonebot-plugin-segbuilder   poetry poetry add nonebot-plugin-segbuilder
```

