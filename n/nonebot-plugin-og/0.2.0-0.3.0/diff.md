# Comparing `tmp/nonebot_plugin_og-0.2.0.tar.gz` & `tmp/nonebot_plugin_og-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_og-0.2.0.tar", max compression
+gzip compressed data, was "nonebot_plugin_og-0.3.0.tar", max compression
```

## Comparing `nonebot_plugin_og-0.2.0.tar` & `nonebot_plugin_og-0.3.0.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0     1062 2023-04-30 08:00:49.030113 nonebot_plugin_og-0.2.0/LICENSE
--rw-r--r--   0        0        0     2072 2023-04-30 08:00:49.030113 nonebot_plugin_og-0.2.0/README.md
--rw-r--r--   0        0        0      873 2023-04-30 08:00:49.030113 nonebot_plugin_og-0.2.0/nonebot_plugin_og/__init__.py
--rw-r--r--   0        0        0      768 2023-04-30 08:00:49.030113 nonebot_plugin_og-0.2.0/nonebot_plugin_og/utils.py
--rw-r--r--   0        0        0      973 2023-04-30 08:00:49.030113 nonebot_plugin_og-0.2.0/pyproject.toml
--rw-r--r--   0        0        0     2602 1970-01-01 00:00:00.000000 nonebot_plugin_og-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0     1062 2023-05-13 08:37:35.840152 nonebot_plugin_og-0.3.0/LICENSE
+-rw-r--r--   0        0        0     2259 2023-05-13 08:37:35.844152 nonebot_plugin_og-0.3.0/README.md
+-rw-r--r--   0        0        0      912 2023-05-13 08:37:35.844152 nonebot_plugin_og-0.3.0/nonebot_plugin_og/__init__.py
+-rw-r--r--   0        0        0      768 2023-05-13 08:37:35.844152 nonebot_plugin_og-0.3.0/nonebot_plugin_og/utils.py
+-rw-r--r--   0        0        0     1126 2023-05-13 08:37:35.844152 nonebot_plugin_og-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0     2888 1970-01-01 00:00:00.000000 nonebot_plugin_og-0.3.0/PKG-INFO
```

### Comparing `nonebot_plugin_og-0.2.0/LICENSE` & `nonebot_plugin_og-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_og-0.2.0/README.md` & `nonebot_plugin_og-0.3.0/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -12,54 +12,62 @@
     <img src="https://img.shields.io/pypi/v/nonebot_plugin_og.svg" alt="pypi">
 </a>
 <img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="python">
 
 
 </div>
 
-    ## 📖 介绍
+## 📖 介绍
 
-    检测链接并生成预览图，基于 [Open Graph](https://ogp.me/) 协议
+检测链接并生成预览图，基于 [Open Graph](https://ogp.me/) 协议
 
 ## 💿 安装
 
 <details>
 <summary>使用 nb-cli 安装</summary>
 在 nonebot2 项目的根目录下打开命令行, 输入以下指令即可安装
 
     nb plugin install nonebot-plugin-og
 
 </details>
 
 <details>
-<summary>使用pip安装</summary>
+<summary>使用 pip 安装</summary>
 在 nonebot2 项目的插件目录下, 打开命令行, 输入以下指令即可安装
 
-    pip iqnstall nonebot-plugin-og
+    pip install nonebot-plugin-og
+
+</details>
+
+<details>
+<summary>使用 Poetry 安装</summary>
+在 nonebot2 项目的插件目录下, 打开命令行, 输入以下指令即可安装
+
+    poetry add nonebot-plugin-og
 
 </details>
 
 
 打开 nonebot2 项目根目录下的 `pyproject.toml` 文件, 在 `[tool.nonebot]` 部分追加写入
 
     plugins = ["nonebot_plugin_og"]
 
 
 ## 🎉 使用
 
 直接发送任意链接，只要是支持 Open Graph 协议的网站，此插件都会自动发送预览图。
 
-## 鸣谢
+## 🙏 鸣谢
 
 * [`nonebot/noenbot2`](https://github.com/nonebot/nonebot2)：跨平台Python异步机器人框架
 * [`Mrs4s/go-cqhttp`](https://github.com/Mrs4s/go-cqhttp)：cqhttp的golang实现，轻量、原生跨平台.
 * [`koishijs/koishi-plugin-og`](https://github.com/koishijs/koishi-plugin-og)：本项目直接参考 ~~（直接开抄~~
 
 
-## 开源许可证
+## 📄 开源许可证
 
 使用 [MIT](./LICENSE) 许可证发布。
 
 ```
 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
 IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
 FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
```

#### html2text {}

```diff
@@ -1,23 +1,25 @@
 # Nonebot-plugin-og _â¨ æ£æµé¾æ¥å¹¶çæé¢è§å¾ â¨_ [license] [pypi]
                                    [python]
 ## ð ä»ç» æ£æµé¾æ¥å¹¶çæé¢è§å¾ï¼åºäº [Open Graph](https://
 ogp.me/) åè®® ## ð¿ å®è£  ä½¿ç¨ nb-cli å®è£ å¨ nonebot2
 é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡, è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ nb plugin
-install nonebot-plugin-og   ä½¿ç¨pipå®è£ å¨ nonebot2
+install nonebot-plugin-og   ä½¿ç¨ pip å®è£ å¨ nonebot2
 é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ pip
-iqnstall nonebot-plugin-og  æå¼ nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç
+install nonebot-plugin-og   ä½¿ç¨ Poetry å®è£ å¨ nonebot2
+é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, è¾å¥ä»¥ä¸æä»¤å³å¯å®è£
+poetry add nonebot-plugin-og  æå¼ nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç
 `pyproject.toml` æä»¶, å¨ `[tool.nonebot]` é¨åè¿½å åå¥ plugins =
 ["nonebot_plugin_og"] ## ð ä½¿ç¨ ç´æ¥åéä»»æé¾æ¥ï¼åªè¦æ¯æ¯æ
-Open Graph åè®®çç½ç«ï¼æ­¤æä»¶é½ä¼èªå¨åéé¢è§å¾ã ## é¸£è°¢
-* [`nonebot/noenbot2`](https://github.com/nonebot/
+Open Graph åè®®çç½ç«ï¼æ­¤æä»¶é½ä¼èªå¨åéé¢è§å¾ã ## ð
+é¸£è°¢ * [`nonebot/noenbot2`](https://github.com/nonebot/
 nonebot2)ï¼è·¨å¹³å°Pythonå¼æ­¥æºå¨äººæ¡æ¶ * [`Mrs4s/go-cqhttp`](https://
 github.com/Mrs4s/go-cqhttp)ï¼cqhttpçgolangå®ç°ï¼è½»éãåçè·¨å¹³å°.
 * [`koishijs/koishi-plugin-og`](https://github.com/koishijs/koishi-plugin-
-og)ï¼æ¬é¡¹ç®ç´æ¥åè ~~ï¼ç´æ¥å¼æ~~ ## å¼æºè®¸å¯è¯ ä½¿ç¨ [MIT]
-(./LICENSE) è®¸å¯è¯åå¸ã ``` THE SOFTWARE IS PROVIDED "AS IS", WITHOUT
-WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
-WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
+og)ï¼æ¬é¡¹ç®ç´æ¥åè ~~ï¼ç´æ¥å¼æ~~ ## ð å¼æºè®¸å¯è¯ ä½¿ç¨
+[MIT](./LICENSE) è®¸å¯è¯åå¸ã ``` THE SOFTWARE IS PROVIDED "AS IS",
+WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO
+THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
 NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE
 FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
 TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR
 THE USE OR OTHER DEALINGS IN THE SOFTWARE. ```
```

### Comparing `nonebot_plugin_og-0.2.0/nonebot_plugin_og/__init__.py` & `nonebot_plugin_og-0.3.0/nonebot_plugin_og/__init__.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,30 +1,30 @@
 from nonebot import on_message
 from nonebot.plugin import PluginMetadata
-from nonebot.adapters.onebot.v11 import Bot, MessageEvent
+from nonebot.adapters.onebot.v11 import Bot, MessageEvent, MessageSegment
 from .utils import get_og_info
 
 __plugin_meta__ = PluginMetadata(
     name="og",
     description="检测链接并发送网站简介及预览图",
     usage="无",
     extra={
         "Author": "mute. <mute231010@gmail.com>",
-        "version": "v0.2.0"
+        "version": "v0.3.0"
     },
 )
 
 
 get_og = on_message(priority=99)
 
 @get_og.handle()
 async def get_og(bot: Bot, event: MessageEvent):
     og_info = await get_og_info(event.message)
     if og_info:
         title = og_info.get('title', '未知标题')
         desc = og_info.get('description', '未提供描述信息')
         img = og_info.get('image', None)
         if img:
-            msg = f'{img}\n{title}\n{desc}'
+            msg = MessageSegment.image(img) + f'\n{title}\n{desc}'
         else:
             msg = f'{title}\n{desc}'
         await bot.send(event, message=msg)
```

### Comparing `nonebot_plugin_og-0.2.0/nonebot_plugin_og/utils.py` & `nonebot_plugin_og-0.3.0/nonebot_plugin_og/utils.py`

 * *Ordering differences only*

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import re
-from typing import Any, Dict, Optional
 import httpx
+from typing import Any, Dict, Optional
 from pyquery import PyQuery as pq
 
 async def get_og_info(msg: Any) -> Optional[Dict[str, Any]]:
     url = re.search(r'(https?://\S+)', str(msg))
     if not url:
         return None
```

### Comparing `nonebot_plugin_og-0.2.0/pyproject.toml` & `nonebot_plugin_og-0.3.0/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "nonebot-plugin-og"
-version = "0.2.0"
+version = "0.3.0"
 description = "检测链接并发送网站简介及预览图"
 authors = [
     {name = "mute.", email = "mute231010@gmail.com"},
 ]
 dependencies = ["httpx", "nonebot2", "pyquery", "nonebot-adapter-onebot"]
 requires-python = ">=3.10"
 readme = "README.md"
@@ -15,23 +15,28 @@
     "Programming Language :: Python :: 3",
 ]
 [project.urls]
 Homepage = "https://github.com/mute23-code/nonebot_plugin_og"
 
 [tool.poetry]
 name = "nonebot-plugin-og"
-version = "0.2.0"
+version = "0.3.0"
 description = "检测链接并发送网站简介及预览图"
 authors = ["mute. <mute231010@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "nonebot_plugin_og"}]
 
 [tool.poetry.dependencies]
 python = "^3.10"
 pyquery = "^2.0.0"
 httpx = "^0.24.0"
+nonebot2 = "^2.0.0rc4"
+nonebot-adapter-onebot = "^2.2.3"
 
 
+
+[tool.nonebot]
+adapters = [{name = "OneBot V11", module_name = "nonebot.adapters.onebot.v11"}]
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `nonebot_plugin_og-0.2.0/PKG-INFO` & `nonebot_plugin_og-0.3.0/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,20 +1,22 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-og
-Version: 0.2.0
+Version: 0.3.0
 Summary: 检测链接并发送网站简介及预览图
 License: MIT
 Author: mute.
 Author-email: mute231010@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: httpx (>=0.24.0,<0.25.0)
+Requires-Dist: nonebot-adapter-onebot (>=2.2.3,<3.0.0)
+Requires-Dist: nonebot2 (>=2.0.0rc4,<3.0.0)
 Requires-Dist: pyquery (>=2.0.0,<3.0.0)
 Description-Content-Type: text/markdown
 
 
 <div align="center">
 
 # Nonebot-plugin-og
@@ -28,54 +30,62 @@
     <img src="https://img.shields.io/pypi/v/nonebot_plugin_og.svg" alt="pypi">
 </a>
 <img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="python">
 
 
 </div>
 
-    ## 📖 介绍
+## 📖 介绍
 
-    检测链接并生成预览图，基于 [Open Graph](https://ogp.me/) 协议
+检测链接并生成预览图，基于 [Open Graph](https://ogp.me/) 协议
 
 ## 💿 安装
 
 <details>
 <summary>使用 nb-cli 安装</summary>
 在 nonebot2 项目的根目录下打开命令行, 输入以下指令即可安装
 
     nb plugin install nonebot-plugin-og
 
 </details>
 
 <details>
-<summary>使用pip安装</summary>
+<summary>使用 pip 安装</summary>
 在 nonebot2 项目的插件目录下, 打开命令行, 输入以下指令即可安装
 
-    pip iqnstall nonebot-plugin-og
+    pip install nonebot-plugin-og
+
+</details>
+
+<details>
+<summary>使用 Poetry 安装</summary>
+在 nonebot2 项目的插件目录下, 打开命令行, 输入以下指令即可安装
+
+    poetry add nonebot-plugin-og
 
 </details>
 
 
 打开 nonebot2 项目根目录下的 `pyproject.toml` 文件, 在 `[tool.nonebot]` 部分追加写入
 
     plugins = ["nonebot_plugin_og"]
 
 
 ## 🎉 使用
 
 直接发送任意链接，只要是支持 Open Graph 协议的网站，此插件都会自动发送预览图。
 
-## 鸣谢
+## 🙏 鸣谢
 
 * [`nonebot/noenbot2`](https://github.com/nonebot/nonebot2)：跨平台Python异步机器人框架
 * [`Mrs4s/go-cqhttp`](https://github.com/Mrs4s/go-cqhttp)：cqhttp的golang实现，轻量、原生跨平台.
 * [`koishijs/koishi-plugin-og`](https://github.com/koishijs/koishi-plugin-og)：本项目直接参考 ~~（直接开抄~~
 
 
-## 开源许可证
+## 📄 开源许可证
 
 使用 [MIT](./LICENSE) 许可证发布。
 
 ```
 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
 IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
 FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
```

#### html2text {}

```diff
@@ -1,30 +1,34 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-og Version: 0.2.0 Summary:
+Metadata-Version: 2.1 Name: nonebot-plugin-og Version: 0.3.0 Summary:
 æ£æµé¾æ¥å¹¶åéç½ç«ç®ä»åé¢è§å¾ License: MIT Author: mute.
 Author-email: mute231010@gmail.com Requires-Python: >=3.10,<4.0 Classifier:
 License :: OSI Approved :: MIT License Classifier: Programming Language ::
 Python :: 3 Classifier: Programming Language :: Python :: 3.10 Classifier:
 Programming Language :: Python :: 3.11 Requires-Dist: httpx (>=0.24.0,<0.25.0)
-Requires-Dist: pyquery (>=2.0.0,<3.0.0) Description-Content-Type: text/markdown
+Requires-Dist: nonebot-adapter-onebot (>=2.2.3,<3.0.0) Requires-Dist: nonebot2
+(>=2.0.0rc4,<3.0.0) Requires-Dist: pyquery (>=2.0.0,<3.0.0) Description-
+Content-Type: text/markdown
 # Nonebot-plugin-og _â¨ æ£æµé¾æ¥å¹¶çæé¢è§å¾ â¨_ [license] [pypi]
                                    [python]
 ## ð ä»ç» æ£æµé¾æ¥å¹¶çæé¢è§å¾ï¼åºäº [Open Graph](https://
 ogp.me/) åè®® ## ð¿ å®è£  ä½¿ç¨ nb-cli å®è£ å¨ nonebot2
 é¡¹ç®çæ ¹ç®å½ä¸æå¼å½ä»¤è¡, è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ nb plugin
-install nonebot-plugin-og   ä½¿ç¨pipå®è£ å¨ nonebot2
+install nonebot-plugin-og   ä½¿ç¨ pip å®è£ å¨ nonebot2
 é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, è¾å¥ä»¥ä¸æä»¤å³å¯å®è£ pip
-iqnstall nonebot-plugin-og  æå¼ nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç
+install nonebot-plugin-og   ä½¿ç¨ Poetry å®è£ å¨ nonebot2
+é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, è¾å¥ä»¥ä¸æä»¤å³å¯å®è£
+poetry add nonebot-plugin-og  æå¼ nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç
 `pyproject.toml` æä»¶, å¨ `[tool.nonebot]` é¨åè¿½å åå¥ plugins =
 ["nonebot_plugin_og"] ## ð ä½¿ç¨ ç´æ¥åéä»»æé¾æ¥ï¼åªè¦æ¯æ¯æ
-Open Graph åè®®çç½ç«ï¼æ­¤æä»¶é½ä¼èªå¨åéé¢è§å¾ã ## é¸£è°¢
-* [`nonebot/noenbot2`](https://github.com/nonebot/
+Open Graph åè®®çç½ç«ï¼æ­¤æä»¶é½ä¼èªå¨åéé¢è§å¾ã ## ð
+é¸£è°¢ * [`nonebot/noenbot2`](https://github.com/nonebot/
 nonebot2)ï¼è·¨å¹³å°Pythonå¼æ­¥æºå¨äººæ¡æ¶ * [`Mrs4s/go-cqhttp`](https://
 github.com/Mrs4s/go-cqhttp)ï¼cqhttpçgolangå®ç°ï¼è½»éãåçè·¨å¹³å°.
 * [`koishijs/koishi-plugin-og`](https://github.com/koishijs/koishi-plugin-
-og)ï¼æ¬é¡¹ç®ç´æ¥åè ~~ï¼ç´æ¥å¼æ~~ ## å¼æºè®¸å¯è¯ ä½¿ç¨ [MIT]
-(./LICENSE) è®¸å¯è¯åå¸ã ``` THE SOFTWARE IS PROVIDED "AS IS", WITHOUT
-WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
-WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
+og)ï¼æ¬é¡¹ç®ç´æ¥åè ~~ï¼ç´æ¥å¼æ~~ ## ð å¼æºè®¸å¯è¯ ä½¿ç¨
+[MIT](./LICENSE) è®¸å¯è¯åå¸ã ``` THE SOFTWARE IS PROVIDED "AS IS",
+WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO
+THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
 NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE
 FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
 TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR
 THE USE OR OTHER DEALINGS IN THE SOFTWARE. ```
```

