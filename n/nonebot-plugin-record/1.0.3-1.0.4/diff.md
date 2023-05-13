# Comparing `tmp/nonebot_plugin_record-1.0.3.tar.gz` & `tmp/nonebot_plugin_record-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_record-1.0.3.tar", max compression
+gzip compressed data, was "nonebot_plugin_record-1.0.4.tar", max compression
```

## Comparing `nonebot_plugin_record-1.0.3.tar` & `nonebot_plugin_record-1.0.4.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1062 2023-01-15 14:15:53.000000 nonebot_plugin_record-1.0.3/LICENSE
--rw-r--r--   0        0        0     2534 2023-01-27 08:56:25.130914 nonebot_plugin_record-1.0.3/nonebot_plugin_record/__init__.py
--rw-r--r--   0        0        0     1090 2023-01-15 09:33:51.056141 nonebot_plugin_record-1.0.3/nonebot_plugin_record/baidu.py
--rw-r--r--   0        0        0      381 2023-01-15 15:10:41.532083 nonebot_plugin_record-1.0.3/nonebot_plugin_record/config.py
--rw-r--r--   0        0        0     3360 2023-01-15 11:41:42.303511 nonebot_plugin_record-1.0.3/nonebot_plugin_record/tencent.py
--rw-r--r--   0        0        0      847 2023-01-27 08:58:42.691170 nonebot_plugin_record-1.0.3/pyproject.toml
--rw-r--r--   0        0        0     4691 2023-01-27 08:58:28.160027 nonebot_plugin_record-1.0.3/README.md
--rw-r--r--   0        0        0     5574 1970-01-01 00:00:00.000000 nonebot_plugin_record-1.0.3/setup.py
--rw-r--r--   0        0        0     5561 1970-01-01 00:00:00.000000 nonebot_plugin_record-1.0.3/PKG-INFO
+-rw-r--r--   0        0        0     1062 2023-01-15 14:15:53.000000 nonebot_plugin_record-1.0.4/LICENSE
+-rw-r--r--   0        0        0     3390 2023-05-13 07:11:57.207255 nonebot_plugin_record-1.0.4/nonebot_plugin_record/__init__.py
+-rw-r--r--   0        0        0     1590 2023-05-13 06:55:12.204661 nonebot_plugin_record-1.0.4/nonebot_plugin_record/baidu.py
+-rw-r--r--   0        0        0      381 2023-01-15 15:10:41.532083 nonebot_plugin_record-1.0.4/nonebot_plugin_record/config.py
+-rw-r--r--   0        0        0     3870 2023-05-13 06:55:24.424835 nonebot_plugin_record-1.0.4/nonebot_plugin_record/tencent.py
+-rw-r--r--   0        0        0      847 2023-05-13 08:02:01.220758 nonebot_plugin_record-1.0.4/pyproject.toml
+-rw-r--r--   0        0        0     5425 2023-05-13 07:57:03.354354 nonebot_plugin_record-1.0.4/README.md
+-rw-r--r--   0        0        0     6309 1970-01-01 00:00:00.000000 nonebot_plugin_record-1.0.4/setup.py
+-rw-r--r--   0        0        0     6280 1970-01-01 00:00:00.000000 nonebot_plugin_record-1.0.4/PKG-INFO
```

### Comparing `nonebot_plugin_record-1.0.3/LICENSE` & `nonebot_plugin_record-1.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_record-1.0.3/nonebot_plugin_record/__init__.py` & `nonebot_plugin_record-1.0.4/nonebot_plugin_record/__init__.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,15 +1,19 @@
-from nonebot import on_message
 from nonebot.matcher import Matcher
 from nonebot.rule import Rule
 from nonebot.typing import T_RuleChecker
+from nonebot import (
+    on_message,
+    logger
+)
 from nonebot.adapters.onebot.v11 import (
     Message,
     Event,
-    Bot
+    Bot,
+    MessageSegment
 )
 
 import base64
 import pilk
 import os
 from typing import (
     Type,
@@ -44,14 +48,15 @@
         handlers: 事件处理函数列表
         temp: 是否为临时事件响应器（仅执行一次）
         expire_time: 事件响应器最终有效时间点，过时即被删除
         priority: 事件响应器优先级
         block: 是否阻止事件向更低优先级传递
         state: 默认 state
     """
+    logger.debug("Starting To Register The Voice Event Responder")
     return on_message(rule=Rule(type_checker) & rule, **kwargs)
 
 
 async def get_text(bot: Bot, event: Event):
     """通过语音识别获取语音中的文本，仅支持普通话。
 
     依赖参数:
@@ -65,24 +70,37 @@
         path_amr = "./data/voices/" + event.get_message()[0].data["file"]
     path_pcm = path_amr[0:-4] + ".pcm"
     pilk.decode(path_amr, path_pcm)
     with open(path_pcm, 'rb') as f:
         speech = base64.b64encode(f.read()).decode('utf-8')
     length = os.path.getsize(path_pcm)
     os.remove(path_pcm)
-    if plugin_config.asr_api_provider == "baidu":
-        text = await baidu_get_text(speech, length)
-    elif plugin_config.asr_api_provider == "tencent":
-        text = await tencent_get_text(speech, length)
-    else:
+    if length == 0:
+        logger.error("加载音频文件失败，请检查nonebot_plugin_gocqhttp配置项是否填写正确")
         return None
-    return text
+    else:
+        logger.debug("Successfully Load The Audio file")
+        if plugin_config.asr_api_provider == "baidu":
+            text = await baidu_get_text(speech, length)
+            logger.debug("Using Baidu API")
+            return text
+        elif plugin_config.asr_api_provider == "tencent":
+            text = await tencent_get_text(speech, length)
+            logger.debug("Using Tencent API")
+            return text
+        elif plugin_config.asr_api_provider == None:
+            logger.error("获取配置失败，请检查asr_api_provider配置项是否正确填写")
+            return None
+        else:
+            logger.error("配置填写错误，asr_api_provider配置只能填写“baidu”或“tencent”")
+            return None
 
 
 def record_tts(pattern: str):
     """获取字符串转换的语音的Message对象。
     调用的TX的接口，采用的音源与登录账号的性别有关
 
     参数:
         pattern: 要进行转换的字符串
     """
-    return Message("[CQ:tts,text=" + pattern + "]")
+    logger.debug("Starting To Retrieve TTS (Text-to-Speech) Message Object")
+    return MessageSegment("tts", {"text": pattern})
```

### Comparing `nonebot_plugin_record-1.0.3/nonebot_plugin_record/tencent.py` & `nonebot_plugin_record-1.0.4/nonebot_plugin_record/tencent.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+from nonebot import logger
 from datetime import datetime
 import httpx
 import hashlib
 import hmac
 import json
 import time
 
@@ -53,14 +54,15 @@
     signature = hmac.new(secret_signing, string_to_sign.encode("utf-8"), hashlib.sha256).hexdigest()
 
     # ************* 步骤 4：拼接 Authorization *************
     authorization = (algorithm + " " +
                      "Credential=" + secret_id + "/" + credential_scope + ", " +
                      "SignedHeaders=" + signed_headers + ", " +
                      "Signature=" + signature)
+    logger.debug("get_authorization Succeeded")
     return authorization
 
 
 async def tencent_get_text(speech, length):
     timestamp = int(time.time())
     url = "https://asr.tencentcloudapi.com"
     data = {
@@ -78,10 +80,19 @@
         "Content-Type": "application/json; charset=utf-8",
         "Host": "asr.tencentcloudapi.com",
         "X-TC-Action": "SentenceRecognition",
         "X-TC-Version": "2019-06-14",
         "X-TC-Timestamp": str(timestamp),
     }
     async with httpx.AsyncClient() as client:
-        resp = await client.post(url, headers=headers, json=data)
-        text = json.loads(resp.text)["Response"]["Result"]
-    return text
+        try:
+            resp = await client.post(url, headers=headers, json=data)
+            if "error" not in json.loads(resp.text)["Response"]:
+                text = json.loads(resp.text)["Response"]["Result"]
+                logger.debug("tencent_get_text Succeeded")
+                return text
+            else:
+                logger.error(f"语音识别接口报错，返回内容：{resp.text}")
+                return None
+        except:
+            logger.error("请求语音识别接口失败，请检查网络环境或重试")
+            return None
```

### Comparing `nonebot_plugin_record-1.0.3/pyproject.toml` & `nonebot_plugin_record-1.0.4/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "nonebot-plugin-record"
-version = "1.0.3"
+version = "1.0.4"
 description = "基于 Nonebot2 的语音功能适配插件，包括语音事件响应器，语音识别、语音合成等功能"
 authors = ["ITSevin <itsevin@qq.com>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/itsevin/nonebot_plugin_record"
 repository = "https://github.com/itsevin/nonebot_plugin_record"
 documentation = "https://github.com/itsevin/nonebot_plugin_record#readme"
```

### Comparing `nonebot_plugin_record-1.0.3/README.md` & `nonebot_plugin_record-1.0.4/README.md`

 * *Files 15% similar despite different names*

```diff
@@ -115,14 +115,16 @@
 from nonebot_plugin_record import get_text
 from nonebot.adapters.onebot.v11 import Event, Bot
 
 # 事件处理中获取文本
 text = await get_text(bot=bot, event=event)
 ```
 
+> 当函数出错时会返回None，具体报错信息请前往Nonebot2进程日志查看
+
 ### 获取文本转换的语音的```Message```对象
 
 获取文本转换的语音的Message对象的异步函数：```record_tts```()
 
 必填参数：
 ```
 patter: 要进行转换的字符串
@@ -177,16 +179,29 @@
         resp = await client.get(url)
         get_dic = json.loads(resp.text)
     data = get_dic['content']
     return data
 
 ```
 
+## 有问题怎么办？
+
+1. 确认是不是你自己的插件的问题
+2. 确认是否正确按照本插件使用说明使用
+3. 排查日志，通过日志内容尝试找出问题并自行解决
+4. 在配置文件中配置```LOG_LEVEL=DEBUG```，然后在日志中查看debug日志，并同时根据本插件源码尝试找出问题并自行解决（确认是本插件的问题可以提issue或者pr）
+5. 问题仍未解决可以提issue，要求提供详细问题描述和较为完整的debug级别的相关日志
+
 ## 更新日志
 
+### 2023/5/13 \[v1.0.4]
+
+- 重构代码，舍弃CQ码过时写法
+- 增加dubug和info级别的日志输出
+
 ### 2023/1/27 \[v1.0.3]
 
 - 修复错误
 
 ### 2023/1/15 \[v1.0.2]
 
 - 修复错误
```

### Comparing `nonebot_plugin_record-1.0.3/setup.py` & `nonebot_plugin_record-1.0.4/setup.py`

 * *Files 20% similar despite different names*

```diff
@@ -11,17 +11,17 @@
 ['httpx>=0.23.3,<0.24.0',
  'nonebot-adapter-onebot>=2.0.0-beta.1,<3.0.0',
  'nonebot2>=2.0.0-beta.1,<3.0.0',
  'pilk>=0.2.3,<0.3.0']
 
 setup_kwargs = {
     'name': 'nonebot-plugin-record',
-    'version': '1.0.3',
+    'version': '1.0.4',
     'description': '基于 Nonebot2 的语音功能适配插件，包括语音事件响应器，语音识别、语音合成等功能',
-    'long_description': '<div align="center">\n  <a href="https://v2.nonebot.dev/store"><img src="https://s2.loli.net/2022/06/16/opBDE8Swad5rU3n.png" width="180" height="180" alt="NoneBotPluginLogo"></a>\n  <br>\n  <p><img src="https://s2.loli.net/2022/06/16/xsVUGRrkbn1ljTD.png" width="240" alt="NoneBotPluginText"></p>\n</div>\n\n<div align="center">\n\n# Nonebot-Plugin-Record\n\n_✨ 基于 [NoneBot2](https://v2.nonebot.dev/) 的语音功能适配插件 ✨_\n\n<p align="center">\n  <img src="https://img.shields.io/github/license/itsevin/nonebot_plugin_record" alt="license">\n  <img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="Python">\n  <img src="https://img.shields.io/badge/nonebot-2.0.0b4+-red.svg" alt="NoneBot">\n  <a href="https://pypi.org/project/nonebot-plugin-record">\n    <img src="https://badgen.net/pypi/v/nonebot-plugin-record" alt="pypi">\n  </a>\n</p>\n\n</div>\n\n## 功能\n\n- 语音事件响应器（仅限私聊）\n- 语音识别（仅限私聊，支持百度智能云、腾讯云接口）\n- 语音合成（利用TX的tts接口）\n\n## 安装\n\n- 使用 nb-cli\n\n```\nnb plugin install nonebot-plugin-record\n```\n\n- 使用 pip\n\n```\npip install nonebot_plugin_record\n```\n\n## 配置项\n\n```\nasr_api_provider="" #必填，API提供商，填写“baidu”或“tencent”\nasr_api_key="" #必填，百度智能云的API_KRY或腾讯云的SECRET_ID\nasr_secret_key="" #必填，百度智能云的SECRET_KRY或腾讯云的SECRET_KEY\nnonebot_plugin_gocqhttp=False #选填，是否使用nonebot2插件版本的go-cqhttp，默认为False\n```\n\n## API选择与配置\n\n### 选什么API?\n\n- 百度智能云-短语音识别标准版：5并发，15万次免费调用量，期限180天\n- 腾讯云-一句话识别：每月5000次免费调用量（推荐）\n\n### 获取密钥\n\n- 百度智能云：https://ai.baidu.com/tech/speech\n- 腾讯云：https://cloud.tencent.com/document/product/1093\n\n## 如何使用？\n\n### 语音事件响应器的使用\n\n语音事件响应器：```on_record()```\n\n说明：语音事件响应器继承自```on_message```，在其上增加了自定义的相应事件响应规则\n\n选填参数：\n\n```\nrule: 事件响应规则\npermission: 事件响应权限\nhandlers: 事件处理函数列表\ntemp: 是否为临时事件响应器（仅执行一次）\nexpire_time: 事件响应器最终有效时间点，过时即被删除\npriority: 事件响应器优先级\nblock: 是否阻止事件向更低优先级传递\nstate: 默认 state\n```\n\n代码示例：\n\n```python\n# 导入依赖包\nfrom nonebot import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import on_record\n\n# 注册语音事件响应器\nmatcher = on_record()\n```\n\n### 获取语音中的文本\n\n获取文本的异步函数：```get_text```()\n\n必填参数：\n\n```\nbot: Bot 对象\nevent: Event 对象\n```\n\n代码示例：\n\n```python\n# 导入依赖包\nfrom nonebot import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import get_text\nfrom nonebot.adapters.onebot.v11 import Event, Bot\n\n# 事件处理中获取文本\ntext = await get_text(bot=bot, event=event)\n```\n\n### 获取文本转换的语音的```Message```对象\n\n获取文本转换的语音的Message对象的异步函数：```record_tts```()\n\n必填参数：\n```\npatter: 要进行转换的字符串\n```\n\n代码示例：\n\n```python\n# 导入依赖包\nfrom nonebot import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import record_tts\n\n# 事件处理中获取文本转换的语音的Message对象\nrecord_tts(pattern=pattern)\n```\n\n### 插件示例\n\n私聊语音聊天插件：\n\n```python\nfrom nonebot.adapters.onebot.v11 import (\n    Event,\n    Bot\n)\nfrom nonebot import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import (\n    on_record,\n    get_text,\n    record_tts\n)\n\nimport httpx\nimport json\n\n\nchat = on_record()\n\n\n@chat.handle()\nasync def main(bot: Bot, event: Event):\n    text = await get_text(bot, event)\n    msg = await get_data(text)\n    await chat.finish(record_tts(msg))\n\n\nasync def get_data(msg):\n    url = f\'http://api.qingyunke.com/api.php?key=free&appid=0&msg={msg}\'\n    async with httpx.AsyncClient() as client:\n        resp = await client.get(url)\n        get_dic = json.loads(resp.text)\n    data = get_dic[\'content\']\n    return data\n\n```\n\n## 更新日志\n\n### 2023/1/27 \\[v1.0.3]\n\n- 修复错误\n\n### 2023/1/15 \\[v1.0.2]\n\n- 修复错误\n\n### 2023/1/15 \\[v1.0.1]\n\n- 适配Nonebot2商店插件自动检测，删除配置文件报错提醒\n\n### 2023/1/15 \\[v1.0.0]\n\n- 发布插件\n',
+    'long_description': '<div align="center">\n  <a href="https://v2.nonebot.dev/store"><img src="https://s2.loli.net/2022/06/16/opBDE8Swad5rU3n.png" width="180" height="180" alt="NoneBotPluginLogo"></a>\n  <br>\n  <p><img src="https://s2.loli.net/2022/06/16/xsVUGRrkbn1ljTD.png" width="240" alt="NoneBotPluginText"></p>\n</div>\n\n<div align="center">\n\n# Nonebot-Plugin-Record\n\n_✨ 基于 [NoneBot2](https://v2.nonebot.dev/) 的语音功能适配插件 ✨_\n\n<p align="center">\n  <img src="https://img.shields.io/github/license/itsevin/nonebot_plugin_record" alt="license">\n  <img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="Python">\n  <img src="https://img.shields.io/badge/nonebot-2.0.0b4+-red.svg" alt="NoneBot">\n  <a href="https://pypi.org/project/nonebot-plugin-record">\n    <img src="https://badgen.net/pypi/v/nonebot-plugin-record" alt="pypi">\n  </a>\n</p>\n\n</div>\n\n## 功能\n\n- 语音事件响应器（仅限私聊）\n- 语音识别（仅限私聊，支持百度智能云、腾讯云接口）\n- 语音合成（利用TX的tts接口）\n\n## 安装\n\n- 使用 nb-cli\n\n```\nnb plugin install nonebot-plugin-record\n```\n\n- 使用 pip\n\n```\npip install nonebot_plugin_record\n```\n\n## 配置项\n\n```\nasr_api_provider="" #必填，API提供商，填写“baidu”或“tencent”\nasr_api_key="" #必填，百度智能云的API_KRY或腾讯云的SECRET_ID\nasr_secret_key="" #必填，百度智能云的SECRET_KRY或腾讯云的SECRET_KEY\nnonebot_plugin_gocqhttp=False #选填，是否使用nonebot2插件版本的go-cqhttp，默认为False\n```\n\n## API选择与配置\n\n### 选什么API?\n\n- 百度智能云-短语音识别标准版：5并发，15万次免费调用量，期限180天\n- 腾讯云-一句话识别：每月5000次免费调用量（推荐）\n\n### 获取密钥\n\n- 百度智能云：https://ai.baidu.com/tech/speech\n- 腾讯云：https://cloud.tencent.com/document/product/1093\n\n## 如何使用？\n\n### 语音事件响应器的使用\n\n语音事件响应器：```on_record()```\n\n说明：语音事件响应器继承自```on_message```，在其上增加了自定义的相应事件响应规则\n\n选填参数：\n\n```\nrule: 事件响应规则\npermission: 事件响应权限\nhandlers: 事件处理函数列表\ntemp: 是否为临时事件响应器（仅执行一次）\nexpire_time: 事件响应器最终有效时间点，过时即被删除\npriority: 事件响应器优先级\nblock: 是否阻止事件向更低优先级传递\nstate: 默认 state\n```\n\n代码示例：\n\n```python\n# 导入依赖包\nfrom nonebot import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import on_record\n\n# 注册语音事件响应器\nmatcher = on_record()\n```\n\n### 获取语音中的文本\n\n获取文本的异步函数：```get_text```()\n\n必填参数：\n\n```\nbot: Bot 对象\nevent: Event 对象\n```\n\n代码示例：\n\n```python\n# 导入依赖包\nfrom nonebot import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import get_text\nfrom nonebot.adapters.onebot.v11 import Event, Bot\n\n# 事件处理中获取文本\ntext = await get_text(bot=bot, event=event)\n```\n\n> 当函数出错时会返回None，具体报错信息请前往Nonebot2进程日志查看\n\n### 获取文本转换的语音的```Message```对象\n\n获取文本转换的语音的Message对象的异步函数：```record_tts```()\n\n必填参数：\n```\npatter: 要进行转换的字符串\n```\n\n代码示例：\n\n```python\n# 导入依赖包\nfrom nonebot import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import record_tts\n\n# 事件处理中获取文本转换的语音的Message对象\nrecord_tts(pattern=pattern)\n```\n\n### 插件示例\n\n私聊语音聊天插件：\n\n```python\nfrom nonebot.adapters.onebot.v11 import (\n    Event,\n    Bot\n)\nfrom nonebot import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import (\n    on_record,\n    get_text,\n    record_tts\n)\n\nimport httpx\nimport json\n\n\nchat = on_record()\n\n\n@chat.handle()\nasync def main(bot: Bot, event: Event):\n    text = await get_text(bot, event)\n    msg = await get_data(text)\n    await chat.finish(record_tts(msg))\n\n\nasync def get_data(msg):\n    url = f\'http://api.qingyunke.com/api.php?key=free&appid=0&msg={msg}\'\n    async with httpx.AsyncClient() as client:\n        resp = await client.get(url)\n        get_dic = json.loads(resp.text)\n    data = get_dic[\'content\']\n    return data\n\n```\n\n## 有问题怎么办？\n\n1. 确认是不是你自己的插件的问题\n2. 确认是否正确按照本插件使用说明使用\n3. 排查日志，通过日志内容尝试找出问题并自行解决\n4. 在配置文件中配置```LOG_LEVEL=DEBUG```，然后在日志中查看debug日志，并同时根据本插件源码尝试找出问题并自行解决（确认是本插件的问题可以提issue或者pr）\n5. 问题仍未解决可以提issue，要求提供详细问题描述和较为完整的debug级别的相关日志\n\n## 更新日志\n\n### 2023/5/13 \\[v1.0.4]\n\n- 重构代码，舍弃CQ码过时写法\n- 增加dubug和info级别的日志输出\n\n### 2023/1/27 \\[v1.0.3]\n\n- 修复错误\n\n### 2023/1/15 \\[v1.0.2]\n\n- 修复错误\n\n### 2023/1/15 \\[v1.0.1]\n\n- 适配Nonebot2商店插件自动检测，删除配置文件报错提醒\n\n### 2023/1/15 \\[v1.0.0]\n\n- 发布插件\n',
     'author': 'ITSevin',
     'author_email': 'itsevin@qq.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/itsevin/nonebot_plugin_record',
     'packages': packages,
     'package_data': package_data,
```

#### html2text {}

```diff
@@ -1,12 +1,12 @@
 # -*- coding: utf-8 -*- from setuptools import setup packages = \
 ['nonebot_plugin_record'] package_data = \ {'': ['*']} install_requires = \
 ['httpx>=0.23.3,<0.24.0', 'nonebot-adapter-onebot>=2.0.0-beta.1,<3.0.0',
 'nonebot2>=2.0.0-beta.1,<3.0.0', 'pilk>=0.2.3,<0.3.0'] setup_kwargs = { 'name':
-'nonebot-plugin-record', 'version': '1.0.3', 'description': 'åºäº Nonebot2
+'nonebot-plugin-record', 'version': '1.0.4', 'description': 'åºäº Nonebot2
 çè¯­é³åè½ééæä»¶ï¼åæ¬è¯­é³äºä»¶ååºå¨ï¼è¯­é³è¯å«ãè¯­é³åæç­åè½',
 'long_description': '
                            \n [NoneBotPluginLogo]\n
                                       \n
                               [NoneBotPluginText]
                                       \n
 \n\n
@@ -45,15 +45,16 @@
 ()\n```\n\n###
 è·åè¯­é³ä¸­çææ¬\n\nè·åææ¬çå¼æ­¥å½æ°ï¼```get_text```
 ()\n\nå¿å¡«åæ°ï¼\n\n```\nbot: Bot å¯¹è±¡\nevent: Event
 å¯¹è±¡\n```\n\nä»£ç ç¤ºä¾ï¼\n\n```python\n# å¯¼å¥ä¾èµå\nfrom nonebot
 import require\nrequire(\'nonebot_plugin_record\')\nfrom nonebot_plugin_record
 import get_text\nfrom nonebot.adapters.onebot.v11 import Event, Bot\n\n#
 äºä»¶å¤çä¸­è·åææ¬\ntext = await get_text(bot=bot,
-event=event)\n```\n\n###
+event=event)\n```\n\n>
+å½å½æ°åºéæ¶ä¼è¿åNoneï¼å·ä½æ¥éä¿¡æ¯è¯·åå¾Nonebot2è¿ç¨æ¥å¿æ¥ç\n\n###
 è·åææ¬è½¬æ¢çè¯­é³ç```Message```å¯¹è±¡\n\nè·åææ¬è½¬æ¢çè¯­é³çMessageå¯¹è±¡çå¼æ­¥å½æ°ï¼```record_tts```
 ()\n\nå¿å¡«åæ°ï¼\n```\npatter:
 è¦è¿è¡è½¬æ¢çå­ç¬¦ä¸²\n```\n\nä»£ç ç¤ºä¾ï¼\n\n```python\n#
 å¯¼å¥ä¾èµå\nfrom nonebot import require\nrequire
 (\'nonebot_plugin_record\')\nfrom nonebot_plugin_record import record_tts\n\n#
 äºä»¶å¤çä¸­è·åææ¬è½¬æ¢çè¯­é³çMessageå¯¹è±¡\nrecord_tts
 (pattern=pattern)\n```\n\n###
@@ -63,15 +64,23 @@
 (\n on_record,\n get_text,\n record_tts\n)\n\nimport httpx\nimport
 json\n\n\nchat = on_record()\n\n\n@chat.handle()\nasync def main(bot: Bot,
 event: Event):\n text = await get_text(bot, event)\n msg = await get_data
 (text)\n await chat.finish(record_tts(msg))\n\n\nasync def get_data(msg):\n url
 = f\'http://api.qingyunke.com/api.php?key=free&appid=0&msg={msg}\'\n async with
 httpx.AsyncClient() as client:\n resp = await client.get(url)\n get_dic =
 json.loads(resp.text)\n data = get_dic[\'content\']\n return data\n\n```\n\n##
-æ´æ°æ¥å¿\n\n### 2023/1/27 \\[v1.0.3]\n\n- ä¿®å¤éè¯¯\n\n### 2023/1/15 \\
-[v1.0.2]\n\n- ä¿®å¤éè¯¯\n\n### 2023/1/15 \\[v1.0.1]\n\n-
+æé®é¢æä¹åï¼\n\n1. ç¡®è®¤æ¯ä¸æ¯ä½ èªå·±çæä»¶çé®é¢\n2.
+ç¡®è®¤æ¯å¦æ­£ç¡®æç§æ¬æä»¶ä½¿ç¨è¯´æä½¿ç¨\n3.
+ææ¥æ¥å¿ï¼éè¿æ¥å¿åå®¹å°è¯æ¾åºé®é¢å¹¶èªè¡è§£å³\n4.
+å¨éç½®æä»¶ä¸­éç½®```LOG_LEVEL=DEBUG```ï¼ç¶åå¨æ¥å¿ä¸­æ¥çdebugæ¥å¿ï¼å¹¶åæ¶æ ¹æ®æ¬æä»¶æºç å°è¯æ¾åºé®é¢å¹¶èªè¡è§£å³ï¼ç¡®è®¤æ¯æ¬æä»¶çé®é¢å¯ä»¥æissueæèprï¼\n5.
+é®é¢ä»æªè§£å³å¯ä»¥æissueï¼è¦æ±æä¾è¯¦ç»é®é¢æè¿°åè¾ä¸ºå®æ´çdebugçº§å«çç¸å³æ¥å¿\n\n##
+æ´æ°æ¥å¿\n\n### 2023/5/13 \\[v1.0.4]\n\n-
+éæä»£ç ï¼èå¼CQç è¿æ¶åæ³\n-
+å¢å dubugåinfoçº§å«çæ¥å¿è¾åº\n\n### 2023/1/27 \\[v1.0.3]\n\n-
+ä¿®å¤éè¯¯\n\n### 2023/1/15 \\[v1.0.2]\n\n- ä¿®å¤éè¯¯\n\n### 2023/1/15 \\
+[v1.0.1]\n\n-
 ééNonebot2ååºæä»¶èªå¨æ£æµï¼å é¤éç½®æä»¶æ¥éæé\n\n###
 2023/1/15 \\[v1.0.0]\n\n- åå¸æä»¶\n', 'author': 'ITSevin', 'author_email':
 'itsevin@qq.com', 'maintainer': 'None', 'maintainer_email': 'None', 'url':
 'https://github.com/itsevin/nonebot_plugin_record', 'packages': packages,
 'package_data': package_data, 'install_requires': install_requires,
 'python_requires': '>=3.8,<4.0', } setup(**setup_kwargs)
```

### Comparing `nonebot_plugin_record-1.0.3/PKG-INFO` & `nonebot_plugin_record-1.0.4/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-record
-Version: 1.0.3
+Version: 1.0.4
 Summary: 基于 Nonebot2 的语音功能适配插件，包括语音事件响应器，语音识别、语音合成等功能
 Home-page: https://github.com/itsevin/nonebot_plugin_record
 License: MIT
 Keywords: nonebot,nonebot2,nonebot_plugin_record
 Author: ITSevin
 Author-email: itsevin@qq.com
 Requires-Python: >=3.8,<4.0
@@ -139,14 +139,16 @@
 from nonebot_plugin_record import get_text
 from nonebot.adapters.onebot.v11 import Event, Bot
 
 # 事件处理中获取文本
 text = await get_text(bot=bot, event=event)
 ```
 
+> 当函数出错时会返回None，具体报错信息请前往Nonebot2进程日志查看
+
 ### 获取文本转换的语音的```Message```对象
 
 获取文本转换的语音的Message对象的异步函数：```record_tts```()
 
 必填参数：
 ```
 patter: 要进行转换的字符串
@@ -201,16 +203,29 @@
         resp = await client.get(url)
         get_dic = json.loads(resp.text)
     data = get_dic['content']
     return data
 
 ```
 
+## 有问题怎么办？
+
+1. 确认是不是你自己的插件的问题
+2. 确认是否正确按照本插件使用说明使用
+3. 排查日志，通过日志内容尝试找出问题并自行解决
+4. 在配置文件中配置```LOG_LEVEL=DEBUG```，然后在日志中查看debug日志，并同时根据本插件源码尝试找出问题并自行解决（确认是本插件的问题可以提issue或者pr）
+5. 问题仍未解决可以提issue，要求提供详细问题描述和较为完整的debug级别的相关日志
+
 ## 更新日志
 
+### 2023/5/13 \[v1.0.4]
+
+- 重构代码，舍弃CQ码过时写法
+- 增加dubug和info级别的日志输出
+
 ### 2023/1/27 \[v1.0.3]
 
 - 修复错误
 
 ### 2023/1/15 \[v1.0.2]
 
 - 修复错误
```

