# Comparing `tmp/nonebot-plugin-picmcstat-0.3.0.tar.gz` & `tmp/nonebot-plugin-picmcstat-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot-plugin-picmcstat-0.3.0.tar", last modified: Tue Apr  4 17:14:03 2023, max compression
+gzip compressed data, was "nonebot-plugin-picmcstat-0.3.1.tar", last modified: Sat May 13 15:29:43 2023, max compression
```

## Comparing `nonebot-plugin-picmcstat-0.3.0.tar` & `nonebot-plugin-picmcstat-0.3.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
--rw-r--r--   0        0        0     1069 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/LICENSE
--rw-r--r--   0        0        0     5758 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/README.md
--rw-r--r--   0        0        0      295 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/__init__.py
--rw-r--r--   0        0        0     1572 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/__main__.py
--rw-r--r--   0        0        0      452 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/config.py
--rw-r--r--   0        0        0     1457 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/const.py
--rw-r--r--   0        0        0     7748 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/draw.py
--rw-r--r--   0        0        0    12656 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/res/default.png
--rw-r--r--   0        0        0      335 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/res/dirt.png
--rw-r--r--   0        0        0      556 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/res/grass_side_carried.png
--rw-r--r--   0        0        0      399 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/res.py
--rw-r--r--   0        0        0     4078 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/util.py
--rw-r--r--   0        0        0     1194 2023-04-04 17:13:52.972054 nonebot-plugin-picmcstat-0.3.0/pyproject.toml
--rw-r--r--   0        0        0     6048 1970-01-01 00:00:00.000000 nonebot-plugin-picmcstat-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/LICENSE
+-rw-r--r--   0        0        0     5998 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/README.md
+-rw-r--r--   0        0        0      295 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/__init__.py
+-rw-r--r--   0        0        0     1572 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/__main__.py
+-rw-r--r--   0        0        0      452 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/config.py
+-rw-r--r--   0        0        0     1480 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/const.py
+-rw-r--r--   0        0        0     7748 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/draw.py
+-rw-r--r--   0        0        0    12656 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/res/default.png
+-rw-r--r--   0        0        0      335 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/res/dirt.png
+-rw-r--r--   0        0        0      556 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/res/grass_side_carried.png
+-rw-r--r--   0        0        0      399 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/res.py
+-rw-r--r--   0        0        0     4078 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/util.py
+-rw-r--r--   0        0        0     1194 2023-05-13 15:29:31.177832 nonebot-plugin-picmcstat-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0     6288 1970-01-01 00:00:00.000000 nonebot-plugin-picmcstat-0.3.1/PKG-INFO
```

### Comparing `nonebot-plugin-picmcstat-0.3.0/LICENSE` & `nonebot-plugin-picmcstat-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-picmcstat-0.3.0/README.md` & `nonebot-plugin-picmcstat-0.3.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,21 @@
+Metadata-Version: 2.1
+Name: nonebot-plugin-picmcstat
+Version: 0.3.1
+Summary: A NoneBot2 plugin generates a pic from a Minecraft server's MOTD
+License: MIT
+Author-email: student_2333 <lgc2333@126.com>
+Requires-Python: >=3.8,<4.0
+Provides-Extra: dev
+Description-Content-Type: text/markdown
+
 <!-- markdownlint-disable MD033 MD036 MD041 -->
 
 <div align="center">
-  <a href="https://v2.nonebot.dev/store"><img src="readme/picmcstat.png" width="180" height="180" alt="NoneBotPluginLogo"></a>
+  <a href="https://v2.nonebot.dev/store"><img src="https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/picmcstat.png" width="180" height="180" alt="NoneBotPluginLogo"></a>
   <br>
   <p><img src="https://raw.githubusercontent.com/A-kirami/nonebot-plugin-template/resources/NoneBotPlugin.svg" width="240" alt="NoneBotPluginText"></p>
 </div>
 
 <div align="center">
 
 # NoneBot-Plugin-PicMCStat
@@ -33,16 +43,16 @@
 插件实际上是可以展示 **玩家列表**、**Mod 端信息 以及 Mod 列表（还未测试）** 的，这里没有找到合适的例子所以没在效果图里展示出来，如果遇到问题可以发 issue
 
 插件包体内并没有自带图片内 Unifont 字体，需要的话请参考 [这里](#字体) 安装字体
 
 <details open>
 <summary>效果图</summary>
 
-![example](readme/example.png)  
-![example](readme/example_je.png)
+![example](https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/example.png)  
+![example](https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/example_je.png)
 
 </details>
 
 ## 💿 安装
 
 ### 插件
 
@@ -143,15 +153,15 @@
 MCSTAT_SHORTCUTS=[{"regex":"^查服$","host":"asia.easecation.net","type":"be"}]
 ```
 
 ## 🎉 使用
 
 发送 `motd` 指令 查看使用指南
 
-![usage](readme/usage.png)
+![usage](https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/usage.png)
 
 ## 📞 联系
 
 QQ：3076823485  
 Telegram：[@lgc2333](https://t.me/lgc2333)  
 吹水群：[1105946125](https://jq.qq.com/?_wv=1027&k=Z3n1MpEp)  
 邮箱：<lgc2333@126.com>
@@ -216,7 +226,8 @@
 - 加入快捷指令，详见配置项
 - 修复某些 JE 服无法正确显示 Motd 的问题
 -
 
 ### 0.1.1
 
 - 将查 JE 服时的 `游戏延迟` 字样 改为 `测试延迟`
+
```

#### html2text {}

```diff
@@ -1,31 +1,37 @@
+Metadata-Version: 2.1 Name: nonebot-plugin-picmcstat Version: 0.3.1 Summary: A
+NoneBot2 plugin generates a pic from a Minecraft server's MOTD License: MIT
+Author-email: student_2333
+126.com> Requires-Python: >=3.8,<4.0 Provides-Extra: dev Description-Content-
+Type: text/markdown
                              [NoneBotPluginLogo]
                               [NoneBotPluginText]
 # NoneBot-Plugin-PicMCStat _â¨ Minecraft æå¡å¨ MOTD æ¥è¯¢ å¾çç â¨_
              [license] [pypi] [python] [pypi_download] [wakatime]
 ## ð ä»ç» æä»¶å®éä¸æ¯å¯ä»¥å±ç¤º **ç©å®¶åè¡¨**ã**Mod
 ç«¯ä¿¡æ¯ ä»¥å Mod åè¡¨ï¼è¿æªæµè¯ï¼**
 çï¼è¿éæ²¡ææ¾å°åéçä¾å­æä»¥æ²¡å¨ææå¾éå±ç¤ºåºæ¥ï¼å¦æéå°é®é¢å¯ä»¥å
 issue æä»¶åä½åå¹¶æ²¡æèªå¸¦å¾çå Unifont
 å­ä½ï¼éè¦çè¯è¯·åè [è¿é](#å­ä½) å®è£å­ä½  ææå¾ !
-[example](readme/example.png) ![example](readme/example_je.png)  ## ð¿ å®è£
-### æä»¶ ä»¥ä¸æå°çæ¹æ³ ä»»é**å¶ä¸** å³å¯  [æ¨è] ä½¿ç¨ nb-
-cli å®è£ å¨ nonebot2 é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡,
-è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ ```bash nb plugin install nonebot-plugin-
-picmcstat ```   ä½¿ç¨åç®¡çå¨å®è£ å¨ nonebot2 é¡¹ç®çæä»¶ç®å½ä¸,
-æå¼å½ä»¤è¡, æ ¹æ®ä½ ä½¿ç¨çåç®¡çå¨, è¾å¥ç¸åºçå®è£å½ä»¤
-pip ```bash pip install nonebot-plugin-picmcstat ```   pdm ```bash pdm add
-nonebot-plugin-picmcstat ```   poetry ```bash poetry add nonebot-plugin-
-picmcstat ```   conda ```bash conda install nonebot-plugin-picmcstat ```
-æå¼ nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç `pyproject.toml` æä»¶, å¨ `
-[tool.nonebot]` é¨åç `plugins` é¡¹éè¿½å åå¥ ```toml [tool.nonebot]
-plugins = [ # ... "nonebot_plugin_picmcstat" ] ```  ### å­ä½
-å­ä½æä»¶è¯·èªè¡å»èªè¡å» [è¿é](http://ftp.gnu.org/gnu/unifont/
-unifont-15.0.01/unifont-15.0.01.ttf) ä¸è½½
-å°å­ä½æä»¶ç´æ¥å®è£å¨ç³»ç»ä¸­å³å¯
+[example](https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/
+example.png) ![example](https://raw.githubusercontent.com/lgc-NB2Dev/readme/
+main/picmcstat/example_je.png)  ## ð¿ å®è£ ### æä»¶ ä»¥ä¸æå°çæ¹æ³
+ä»»é**å¶ä¸** å³å¯  [æ¨è] ä½¿ç¨ nb-cli å®è£ å¨ nonebot2
+é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡, è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ ```bash nb
+plugin install nonebot-plugin-picmcstat ```   ä½¿ç¨åç®¡çå¨å®è£ å¨
+nonebot2 é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡,
+æ ¹æ®ä½ ä½¿ç¨çåç®¡çå¨, è¾å¥ç¸åºçå®è£å½ä»¤  pip ```bash pip
+install nonebot-plugin-picmcstat ```   pdm ```bash pdm add nonebot-plugin-
+picmcstat ```   poetry ```bash poetry add nonebot-plugin-picmcstat ```   conda
+```bash conda install nonebot-plugin-picmcstat ```  æå¼ nonebot2
+é¡¹ç®æ ¹ç®å½ä¸ç `pyproject.toml` æä»¶, å¨ `[tool.nonebot]` é¨åç
+`plugins` é¡¹éè¿½å åå¥ ```toml [tool.nonebot] plugins = [ # ...
+"nonebot_plugin_picmcstat" ] ```  ### å­ä½ å­ä½æä»¶è¯·èªè¡å»èªè¡å»
+[è¿é](http://ftp.gnu.org/gnu/unifont/unifont-15.0.01/unifont-15.0.01.ttf)
+ä¸è½½ å°å­ä½æä»¶ç´æ¥å®è£å¨ç³»ç»ä¸­å³å¯
 å¦æä¸è¡ï¼è¯·å°è¯å³é®å­ä½æä»¶ç¹å» `ä¸ºææç¨æ·å®è£`
 å¦æè¿æ¯ä¸è¡ï¼è¯·å°è¯ä¿®æ¹æä»¶å­ä½éç½® ## âï¸ éç½® ###
 `MCSTAT_FONT` - ä½¿ç¨çå­ä½åç§° / è·¯å¾ é»è®¤ï¼`unifont-15.0.01.ttf`
 è¯·æéèªè¡æ´æ¹ ### `MCSTAT_SHORTCUTS` - å¿«æ·æä»¤åè¡¨
 è¿ä¸ªéç½®é¡¹è½å¤å¸®å©ä½ ç®åä¸äºæ¥è¯¢æä»¤
 æ­¤éç½®é¡¹çç±»åæ¯ä¸ä¸ªåè¡¨ï¼éé¢çåç´ éè¦ä¸ºä¸ä¸ªç¹å®ç»æçå­å¸
 è¿ä¸ªå­å¸éè¦æä¸ä¸ªåç´  - `regex` -
@@ -36,17 +42,17 @@
 è¦æ¥è¯¢æå¡å¨çç±»åï¼`je` è¡¨ç¤º Java çæï¼`be` è¡¨ç¤ºåºå²©çæ
 - `whitelist` -
 ç¾¤èç½ååï¼åªæéé¢ååºçç¾¤å·å¯ä»¥æ¥è¯¢ï¼å¯ä»¥ä¸å¡«æ¥å¯¹ææç¾¤å¼æ¾æ¥è¯¢
 æç»çéç½®é¡¹çèµ·æ¥æ¯è¿æ ·å­çï¼å½ä½ åé `æ¥æ`
 æ¶ï¼æºå¨äººä¼æ EaseCation æå¡å¨çç¶æåéåºæ¥ ```env
 MCSTAT_SHORTCUTS=[{"regex":"^æ¥æ$","host":"asia.easecation.net","type":
 "be"}] ``` ## ð ä½¿ç¨ åé `motd` æä»¤ æ¥çä½¿ç¨æå ![usage]
-(readme/usage.png) ## ð èç³» QQï¼3076823485 Telegramï¼[@lgc2333](https:/
-/t.me/lgc2333) å¹æ°´ç¾¤ï¼[1105946125](https://jq.qq.com/?_wv=1027&k=Z3n1MpEp)
-é®ç®±ï¼
+(https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/usage.png)
+## ð èç³» QQï¼3076823485 Telegramï¼[@lgc2333](https://t.me/lgc2333)
+å¹æ°´ç¾¤ï¼[1105946125](https://jq.qq.com/?_wv=1027&k=Z3n1MpEp) é®ç®±ï¼
 126.com> ## ð¡ é¸£è°¢ ### [pil-utils](https://github.com/MeetWq/pil-utils)
 è¶å¥½ç¨ç Pillow è¾å©åºï¼wq ä½¬æ¯å ï¼å¿«å»ç¨ awa ## ð° èµå©
 æè°¢å¤§å®¶çèµå©ï¼ä½ ä»¬çèµå©å°æ¯æç»§ç»­åä½çå¨åï¼ -
 [ç±åçµ](https://afdian.net/@lgc2333) -  èµå©äºç»´ç ï¼ç¹å»å±å¼ï¼ !
 [è®¨é¥­](https://raw.githubusercontent.com/lgc2333/ShigureBotMenu/master/src/
 imgs/sponsor.png)  ## ð æ´æ°æ¥å¿ ### 0.3.0 - å¼ç¨ `nonebot-plugin-
 imageutils`ï¼æ¢ç¨ `pil-utils` - æ¯æäºæ´å¤å­ä½æ ·å¼ -
```

### Comparing `nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/__main__.py` & `nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/__main__.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/const.py` & `nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/const.py`

 * *Files 7% similar despite different names*

```diff
@@ -59,14 +59,15 @@
     "light_purple": "d",
     "yellow": "e",
     "white": "f",
     "bold": "l",
     "italic": "o",
     "underlined": "n",
     "strikethrough": "m",
+    "obfuscated": "k",
 }
 
 STYLE_BBCODE = {
     "l": ["[b]", "[/b]"],
     "m": ["[del]", "[/del]"],
     "n": ["[u]", "[/u]"],
     "o": ["[i]", "[/i]"],
```

### Comparing `nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/draw.py` & `nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/draw.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/res/default.png` & `nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/res/default.png`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/res/grass_side_carried.png` & `nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/res/grass_side_carried.png`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-picmcstat-0.3.0/nonebot_plugin_picmcstat/util.py` & `nonebot-plugin-picmcstat-0.3.1/nonebot_plugin_picmcstat/util.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-picmcstat-0.3.0/pyproject.toml` & `nonebot-plugin-picmcstat-0.3.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "nonebot-plugin-picmcstat"
-version = "0.3.0"
+version = "0.3.1"
 description = "A NoneBot2 plugin generates a pic from a Minecraft server's MOTD"
 authors = [
     { name = "student_2333", email = "lgc2333@126.com" },
 ]
 dependencies = [
     "mcstatus<11.0.0,>=10.0.1",
     "nonebot2<3.0.0,>=2.0.0rc2",
```

### Comparing `nonebot-plugin-picmcstat-0.3.0/PKG-INFO` & `nonebot-plugin-picmcstat-0.3.1/README.md`

 * *Files 20% similar despite different names*

```diff
@@ -1,21 +1,11 @@
-Metadata-Version: 2.1
-Name: nonebot-plugin-picmcstat
-Version: 0.3.0
-Summary: A NoneBot2 plugin generates a pic from a Minecraft server's MOTD
-License: MIT
-Author-email: student_2333 <lgc2333@126.com>
-Requires-Python: >=3.8,<4.0
-Provides-Extra: dev
-Description-Content-Type: text/markdown
-
 <!-- markdownlint-disable MD033 MD036 MD041 -->
 
 <div align="center">
-  <a href="https://v2.nonebot.dev/store"><img src="readme/picmcstat.png" width="180" height="180" alt="NoneBotPluginLogo"></a>
+  <a href="https://v2.nonebot.dev/store"><img src="https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/picmcstat.png" width="180" height="180" alt="NoneBotPluginLogo"></a>
   <br>
   <p><img src="https://raw.githubusercontent.com/A-kirami/nonebot-plugin-template/resources/NoneBotPlugin.svg" width="240" alt="NoneBotPluginText"></p>
 </div>
 
 <div align="center">
 
 # NoneBot-Plugin-PicMCStat
@@ -43,16 +33,16 @@
 插件实际上是可以展示 **玩家列表**、**Mod 端信息 以及 Mod 列表（还未测试）** 的，这里没有找到合适的例子所以没在效果图里展示出来，如果遇到问题可以发 issue
 
 插件包体内并没有自带图片内 Unifont 字体，需要的话请参考 [这里](#字体) 安装字体
 
 <details open>
 <summary>效果图</summary>
 
-![example](readme/example.png)  
-![example](readme/example_je.png)
+![example](https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/example.png)  
+![example](https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/example_je.png)
 
 </details>
 
 ## 💿 安装
 
 ### 插件
 
@@ -153,15 +143,15 @@
 MCSTAT_SHORTCUTS=[{"regex":"^查服$","host":"asia.easecation.net","type":"be"}]
 ```
 
 ## 🎉 使用
 
 发送 `motd` 指令 查看使用指南
 
-![usage](readme/usage.png)
+![usage](https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/usage.png)
 
 ## 📞 联系
 
 QQ：3076823485  
 Telegram：[@lgc2333](https://t.me/lgc2333)  
 吹水群：[1105946125](https://jq.qq.com/?_wv=1027&k=Z3n1MpEp)  
 邮箱：<lgc2333@126.com>
@@ -226,8 +216,7 @@
 - 加入快捷指令，详见配置项
 - 修复某些 JE 服无法正确显示 Motd 的问题
 -
 
 ### 0.1.1
 
 - 将查 JE 服时的 `游戏延迟` 字样 改为 `测试延迟`
-
```

#### html2text {}

```diff
@@ -1,36 +1,32 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-picmcstat Version: 0.3.0 Summary: A
-NoneBot2 plugin generates a pic from a Minecraft server's MOTD License: MIT
-Author-email: student_2333
-126.com> Requires-Python: >=3.8,<4.0 Provides-Extra: dev Description-Content-
-Type: text/markdown
                              [NoneBotPluginLogo]
                               [NoneBotPluginText]
 # NoneBot-Plugin-PicMCStat _â¨ Minecraft æå¡å¨ MOTD æ¥è¯¢ å¾çç â¨_
              [license] [pypi] [python] [pypi_download] [wakatime]
 ## ð ä»ç» æä»¶å®éä¸æ¯å¯ä»¥å±ç¤º **ç©å®¶åè¡¨**ã**Mod
 ç«¯ä¿¡æ¯ ä»¥å Mod åè¡¨ï¼è¿æªæµè¯ï¼**
 çï¼è¿éæ²¡ææ¾å°åéçä¾å­æä»¥æ²¡å¨ææå¾éå±ç¤ºåºæ¥ï¼å¦æéå°é®é¢å¯ä»¥å
 issue æä»¶åä½åå¹¶æ²¡æèªå¸¦å¾çå Unifont
 å­ä½ï¼éè¦çè¯è¯·åè [è¿é](#å­ä½) å®è£å­ä½  ææå¾ !
-[example](readme/example.png) ![example](readme/example_je.png)  ## ð¿ å®è£
-### æä»¶ ä»¥ä¸æå°çæ¹æ³ ä»»é**å¶ä¸** å³å¯  [æ¨è] ä½¿ç¨ nb-
-cli å®è£ å¨ nonebot2 é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡,
-è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ ```bash nb plugin install nonebot-plugin-
-picmcstat ```   ä½¿ç¨åç®¡çå¨å®è£ å¨ nonebot2 é¡¹ç®çæä»¶ç®å½ä¸,
-æå¼å½ä»¤è¡, æ ¹æ®ä½ ä½¿ç¨çåç®¡çå¨, è¾å¥ç¸åºçå®è£å½ä»¤
-pip ```bash pip install nonebot-plugin-picmcstat ```   pdm ```bash pdm add
-nonebot-plugin-picmcstat ```   poetry ```bash poetry add nonebot-plugin-
-picmcstat ```   conda ```bash conda install nonebot-plugin-picmcstat ```
-æå¼ nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç `pyproject.toml` æä»¶, å¨ `
-[tool.nonebot]` é¨åç `plugins` é¡¹éè¿½å åå¥ ```toml [tool.nonebot]
-plugins = [ # ... "nonebot_plugin_picmcstat" ] ```  ### å­ä½
-å­ä½æä»¶è¯·èªè¡å»èªè¡å» [è¿é](http://ftp.gnu.org/gnu/unifont/
-unifont-15.0.01/unifont-15.0.01.ttf) ä¸è½½
-å°å­ä½æä»¶ç´æ¥å®è£å¨ç³»ç»ä¸­å³å¯
+[example](https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/
+example.png) ![example](https://raw.githubusercontent.com/lgc-NB2Dev/readme/
+main/picmcstat/example_je.png)  ## ð¿ å®è£ ### æä»¶ ä»¥ä¸æå°çæ¹æ³
+ä»»é**å¶ä¸** å³å¯  [æ¨è] ä½¿ç¨ nb-cli å®è£ å¨ nonebot2
+é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡, è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ ```bash nb
+plugin install nonebot-plugin-picmcstat ```   ä½¿ç¨åç®¡çå¨å®è£ å¨
+nonebot2 é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡,
+æ ¹æ®ä½ ä½¿ç¨çåç®¡çå¨, è¾å¥ç¸åºçå®è£å½ä»¤  pip ```bash pip
+install nonebot-plugin-picmcstat ```   pdm ```bash pdm add nonebot-plugin-
+picmcstat ```   poetry ```bash poetry add nonebot-plugin-picmcstat ```   conda
+```bash conda install nonebot-plugin-picmcstat ```  æå¼ nonebot2
+é¡¹ç®æ ¹ç®å½ä¸ç `pyproject.toml` æä»¶, å¨ `[tool.nonebot]` é¨åç
+`plugins` é¡¹éè¿½å åå¥ ```toml [tool.nonebot] plugins = [ # ...
+"nonebot_plugin_picmcstat" ] ```  ### å­ä½ å­ä½æä»¶è¯·èªè¡å»èªè¡å»
+[è¿é](http://ftp.gnu.org/gnu/unifont/unifont-15.0.01/unifont-15.0.01.ttf)
+ä¸è½½ å°å­ä½æä»¶ç´æ¥å®è£å¨ç³»ç»ä¸­å³å¯
 å¦æä¸è¡ï¼è¯·å°è¯å³é®å­ä½æä»¶ç¹å» `ä¸ºææç¨æ·å®è£`
 å¦æè¿æ¯ä¸è¡ï¼è¯·å°è¯ä¿®æ¹æä»¶å­ä½éç½® ## âï¸ éç½® ###
 `MCSTAT_FONT` - ä½¿ç¨çå­ä½åç§° / è·¯å¾ é»è®¤ï¼`unifont-15.0.01.ttf`
 è¯·æéèªè¡æ´æ¹ ### `MCSTAT_SHORTCUTS` - å¿«æ·æä»¤åè¡¨
 è¿ä¸ªéç½®é¡¹è½å¤å¸®å©ä½ ç®åä¸äºæ¥è¯¢æä»¤
 æ­¤éç½®é¡¹çç±»åæ¯ä¸ä¸ªåè¡¨ï¼éé¢çåç´ éè¦ä¸ºä¸ä¸ªç¹å®ç»æçå­å¸
 è¿ä¸ªå­å¸éè¦æä¸ä¸ªåç´  - `regex` -
@@ -41,17 +37,17 @@
 è¦æ¥è¯¢æå¡å¨çç±»åï¼`je` è¡¨ç¤º Java çæï¼`be` è¡¨ç¤ºåºå²©çæ
 - `whitelist` -
 ç¾¤èç½ååï¼åªæéé¢ååºçç¾¤å·å¯ä»¥æ¥è¯¢ï¼å¯ä»¥ä¸å¡«æ¥å¯¹ææç¾¤å¼æ¾æ¥è¯¢
 æç»çéç½®é¡¹çèµ·æ¥æ¯è¿æ ·å­çï¼å½ä½ åé `æ¥æ`
 æ¶ï¼æºå¨äººä¼æ EaseCation æå¡å¨çç¶æåéåºæ¥ ```env
 MCSTAT_SHORTCUTS=[{"regex":"^æ¥æ$","host":"asia.easecation.net","type":
 "be"}] ``` ## ð ä½¿ç¨ åé `motd` æä»¤ æ¥çä½¿ç¨æå ![usage]
-(readme/usage.png) ## ð èç³» QQï¼3076823485 Telegramï¼[@lgc2333](https:/
-/t.me/lgc2333) å¹æ°´ç¾¤ï¼[1105946125](https://jq.qq.com/?_wv=1027&k=Z3n1MpEp)
-é®ç®±ï¼
+(https://raw.githubusercontent.com/lgc-NB2Dev/readme/main/picmcstat/usage.png)
+## ð èç³» QQï¼3076823485 Telegramï¼[@lgc2333](https://t.me/lgc2333)
+å¹æ°´ç¾¤ï¼[1105946125](https://jq.qq.com/?_wv=1027&k=Z3n1MpEp) é®ç®±ï¼
 126.com> ## ð¡ é¸£è°¢ ### [pil-utils](https://github.com/MeetWq/pil-utils)
 è¶å¥½ç¨ç Pillow è¾å©åºï¼wq ä½¬æ¯å ï¼å¿«å»ç¨ awa ## ð° èµå©
 æè°¢å¤§å®¶çèµå©ï¼ä½ ä»¬çèµå©å°æ¯æç»§ç»­åä½çå¨åï¼ -
 [ç±åçµ](https://afdian.net/@lgc2333) -  èµå©äºç»´ç ï¼ç¹å»å±å¼ï¼ !
 [è®¨é¥­](https://raw.githubusercontent.com/lgc2333/ShigureBotMenu/master/src/
 imgs/sponsor.png)  ## ð æ´æ°æ¥å¿ ### 0.3.0 - å¼ç¨ `nonebot-plugin-
 imageutils`ï¼æ¢ç¨ `pil-utils` - æ¯æäºæ´å¤å­ä½æ ·å¼ -
```

