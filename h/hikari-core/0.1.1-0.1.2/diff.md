# Comparing `tmp/hikari_core-0.1.1.tar.gz` & `tmp/hikari_core-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hikari_core-0.1.1.tar", max compression
+gzip compressed data, was "hikari_core-0.1.2.tar", max compression
```

## Comparing `hikari_core-0.1.1.tar` & `hikari_core-0.1.2.tar`

### file list

```diff
@@ -1,47 +1,47 @@
--rw-r--r--   0        0        0     2692 2023-05-12 18:08:13.864601 hikari_core-0.1.1/hikari_core/__init__.py
--rw-r--r--   0        0        0     4223 2023-05-12 15:43:23.576624 hikari_core-0.1.1/hikari_core/analyze.py
--rw-r--r--   0        0        0     3361 2023-05-12 16:59:43.442417 hikari_core-0.1.1/hikari_core/command_select.py
--rw-r--r--   0        0        0    12434 2023-05-12 18:09:43.557530 hikari_core-0.1.1/hikari_core/data_source.py
--rw-r--r--   0        0        0      719 2023-05-12 16:14:53.492016 hikari_core-0.1.1/hikari_core/Html_Render/__init__.py
--rw-r--r--   0        0        0     2901 2023-05-12 16:29:09.654986 hikari_core-0.1.1/hikari_core/Html_Render/browser.py
--rw-r--r--   0        0        0     5462 2023-05-12 16:27:10.898314 hikari_core-0.1.1/hikari_core/Html_Render/data_source.py
--rw-r--r--   0        0        0    18237 2023-05-12 16:01:25.071577 hikari_core-0.1.1/hikari_core/Html_Render/templates/github-markdown-light.css
--rw-r--r--   0        0        0  1458204 2023-05-12 16:01:25.084174 hikari_core-0.1.1/hikari_core/Html_Render/templates/katex/katex.min.b64_fonts.css
--rw-r--r--   0        0        0   270288 2023-05-12 16:01:25.123214 hikari_core-0.1.1/hikari_core/Html_Render/templates/katex/katex.min.js
--rw-r--r--   0        0        0     1290 2023-05-12 16:01:25.124230 hikari_core-0.1.1/hikari_core/Html_Render/templates/katex/mathtex-script-type.min.js
--rw-r--r--   0        0        0      662 2023-05-12 16:01:25.127272 hikari_core-0.1.1/hikari_core/Html_Render/templates/markdown.html
--rw-r--r--   0        0        0     4963 2023-05-12 16:01:25.128288 hikari_core-0.1.1/hikari_core/Html_Render/templates/pygments-default.css
--rw-r--r--   0        0        0      125 2023-05-12 16:01:25.129291 hikari_core-0.1.1/hikari_core/Html_Render/templates/text.css
--rw-r--r--   0        0        0      233 2023-05-12 16:01:25.129291 hikari_core-0.1.1/hikari_core/Html_Render/templates/text.html
--rw-r--r--   0        0        0      937 2023-05-12 17:40:06.718420 hikari_core-0.1.1/hikari_core/HttpClient_Pool.py
--rw-r--r--   0        0        0     2182 2023-05-12 17:35:57.360511 hikari_core-0.1.1/hikari_core/model.py
--rw-r--r--   0        0        0        0 2023-05-12 06:05:30.059172 hikari_core-0.1.1/hikari_core/moudle/__init__.py
--rw-r--r--   0        0        0      175 2023-05-12 06:05:32.348596 hikari_core-0.1.1/hikari_core/moudle/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0     5400 2023-05-12 06:07:09.234200 hikari_core-0.1.1/hikari_core/moudle/__pycache__/publicAPI.cpython-310.pyc
--rw-r--r--   0        0        0     2914 2023-05-12 06:06:54.456117 hikari_core-0.1.1/hikari_core/moudle/__pycache__/wws_info.cpython-310.pyc
--rw-r--r--   0        0        0     3105 2023-05-12 06:07:46.904239 hikari_core-0.1.1/hikari_core/moudle/__pycache__/wws_recent.cpython-310.pyc
--rw-r--r--   0        0        0     7226 2023-05-12 16:47:03.778682 hikari_core-0.1.1/hikari_core/moudle/publicAPI.py
--rw-r--r--   0        0        0     2517 2023-05-12 17:05:17.398997 hikari_core-0.1.1/hikari_core/moudle/wws_info.py
--rw-r--r--   0        0        0     4501 2023-05-12 16:56:20.219036 hikari_core-0.1.1/hikari_core/moudle/wws_recent.py
--rw-r--r--   0        0        0   173077 2023-05-12 03:16:55.137328 hikari_core-0.1.1/hikari_core/Template/Chart.min.js
--rw-r--r--   0        0        0    13279 2023-05-12 03:16:55.058560 hikari_core-0.1.1/hikari_core/Template/chartjs-plugin-datalabels@1.0.0.js
--rw-r--r--   0        0        0  3313391 2023-05-12 03:16:55.346040 hikari_core-0.1.1/hikari_core/Template/echarts.js
--rw-r--r--   0        0        0     3710 2023-05-12 03:16:55.039314 hikari_core-0.1.1/hikari_core/Template/select-ship.html
--rw-r--r--   0        0        0     5118 2023-05-12 03:16:55.034251 hikari_core-0.1.1/hikari_core/Template/ship-rank.html
--rw-r--r--   0        0        0      225 2023-05-12 03:16:55.063600 hikari_core-0.1.1/hikari_core/Template/text-help.css
--rw-r--r--   0        0        0     7293 2023-05-12 03:16:55.073236 hikari_core-0.1.1/hikari_core/Template/wws-ban.html
--rw-r--r--   0        0        0    16766 2023-05-12 03:16:55.041316 hikari_core-0.1.1/hikari_core/Template/wws-box-christmas.html
--rw-r--r--   0        0        0    18454 2023-05-12 03:16:55.029646 hikari_core-0.1.1/hikari_core/Template/wws-clan.html
--rw-r--r--   0        0        0    23636 2023-05-12 03:16:55.035273 hikari_core-0.1.1/hikari_core/Template/wws-info-recent.html
--rw-r--r--   0        0        0    25512 2023-05-12 03:16:55.078284 hikari_core-0.1.1/hikari_core/Template/wws-info.html
--rw-r--r--   0        0        0     2396 2023-05-12 03:16:55.070709 hikari_core-0.1.1/hikari_core/Template/wws-personalRecord.html
--rw-r--r--   0        0        0    21667 2023-05-12 03:16:55.042328 hikari_core-0.1.1/hikari_core/Template/wws-ship-recent.html
--rw-r--r--   0        0        0    20760 2023-05-12 03:16:55.061585 hikari_core-0.1.1/hikari_core/Template/wws-ship.html
--rw-r--r--   0        0        0     9455 2023-05-12 03:16:55.069704 hikari_core-0.1.1/hikari_core/Template/wws-sx.html
--rw-r--r--   0        0        0     5793 2023-05-12 03:16:55.077269 hikari_core-0.1.1/hikari_core/Template/wws-unban.html
--rw-r--r--   0        0        0     3537 2023-05-12 13:08:49.465546 hikari_core-0.1.1/hikari_core/utils.py
--rw-r--r--   0        0        0    35823 2023-05-12 02:05:38.427107 hikari_core-0.1.1/LICENSE
--rw-r--r--   0        0        0      521 2023-05-12 18:11:38.875774 hikari_core-0.1.1/pyproject.toml
--rw-r--r--   0        0        0       35 2023-05-12 02:05:38.429109 hikari_core-0.1.1/README.md
--rw-r--r--   0        0        0      948 1970-01-01 00:00:00.000000 hikari_core-0.1.1/setup.py
--rw-r--r--   0        0        0      781 1970-01-01 00:00:00.000000 hikari_core-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0     2979 2023-05-12 18:39:10.835100 hikari_core-0.1.2/hikari_core/__init__.py
+-rw-r--r--   0        0        0     4152 2023-05-12 18:40:02.649642 hikari_core-0.1.2/hikari_core/analyze.py
+-rw-r--r--   0        0        0     3361 2023-05-12 16:59:43.442417 hikari_core-0.1.2/hikari_core/command_select.py
+-rw-r--r--   0        0        0    12434 2023-05-12 18:09:43.557530 hikari_core-0.1.2/hikari_core/data_source.py
+-rw-r--r--   0        0        0      719 2023-05-12 16:14:53.492016 hikari_core-0.1.2/hikari_core/Html_Render/__init__.py
+-rw-r--r--   0        0        0     2901 2023-05-12 16:29:09.654986 hikari_core-0.1.2/hikari_core/Html_Render/browser.py
+-rw-r--r--   0        0        0     5462 2023-05-12 16:27:10.898314 hikari_core-0.1.2/hikari_core/Html_Render/data_source.py
+-rw-r--r--   0        0        0    18237 2023-05-12 16:01:25.071577 hikari_core-0.1.2/hikari_core/Html_Render/templates/github-markdown-light.css
+-rw-r--r--   0        0        0  1458204 2023-05-12 16:01:25.084174 hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/katex.min.b64_fonts.css
+-rw-r--r--   0        0        0   270288 2023-05-12 16:01:25.123214 hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/katex.min.js
+-rw-r--r--   0        0        0     1290 2023-05-12 16:01:25.124230 hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/mathtex-script-type.min.js
+-rw-r--r--   0        0        0      662 2023-05-12 16:01:25.127272 hikari_core-0.1.2/hikari_core/Html_Render/templates/markdown.html
+-rw-r--r--   0        0        0     4963 2023-05-12 16:01:25.128288 hikari_core-0.1.2/hikari_core/Html_Render/templates/pygments-default.css
+-rw-r--r--   0        0        0      125 2023-05-12 16:01:25.129291 hikari_core-0.1.2/hikari_core/Html_Render/templates/text.css
+-rw-r--r--   0        0        0      233 2023-05-12 16:01:25.129291 hikari_core-0.1.2/hikari_core/Html_Render/templates/text.html
+-rw-r--r--   0        0        0      937 2023-05-12 17:40:06.718420 hikari_core-0.1.2/hikari_core/HttpClient_Pool.py
+-rw-r--r--   0        0        0     2492 2023-05-12 18:38:28.768568 hikari_core-0.1.2/hikari_core/model.py
+-rw-r--r--   0        0        0        0 2023-05-12 06:05:30.059172 hikari_core-0.1.2/hikari_core/moudle/__init__.py
+-rw-r--r--   0        0        0      175 2023-05-12 06:05:32.348596 hikari_core-0.1.2/hikari_core/moudle/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     5400 2023-05-12 06:07:09.234200 hikari_core-0.1.2/hikari_core/moudle/__pycache__/publicAPI.cpython-310.pyc
+-rw-r--r--   0        0        0     2914 2023-05-12 06:06:54.456117 hikari_core-0.1.2/hikari_core/moudle/__pycache__/wws_info.cpython-310.pyc
+-rw-r--r--   0        0        0     3105 2023-05-12 06:07:46.904239 hikari_core-0.1.2/hikari_core/moudle/__pycache__/wws_recent.cpython-310.pyc
+-rw-r--r--   0        0        0     7226 2023-05-12 16:47:03.778682 hikari_core-0.1.2/hikari_core/moudle/publicAPI.py
+-rw-r--r--   0        0        0     2566 2023-05-12 18:34:05.942459 hikari_core-0.1.2/hikari_core/moudle/wws_info.py
+-rw-r--r--   0        0        0     4501 2023-05-12 16:56:20.219036 hikari_core-0.1.2/hikari_core/moudle/wws_recent.py
+-rw-r--r--   0        0        0   173077 2023-05-12 03:16:55.137328 hikari_core-0.1.2/hikari_core/Template/Chart.min.js
+-rw-r--r--   0        0        0    13279 2023-05-12 03:16:55.058560 hikari_core-0.1.2/hikari_core/Template/chartjs-plugin-datalabels@1.0.0.js
+-rw-r--r--   0        0        0  3313391 2023-05-12 03:16:55.346040 hikari_core-0.1.2/hikari_core/Template/echarts.js
+-rw-r--r--   0        0        0     3710 2023-05-12 03:16:55.039314 hikari_core-0.1.2/hikari_core/Template/select-ship.html
+-rw-r--r--   0        0        0     5118 2023-05-12 03:16:55.034251 hikari_core-0.1.2/hikari_core/Template/ship-rank.html
+-rw-r--r--   0        0        0      225 2023-05-12 03:16:55.063600 hikari_core-0.1.2/hikari_core/Template/text-help.css
+-rw-r--r--   0        0        0     7293 2023-05-12 03:16:55.073236 hikari_core-0.1.2/hikari_core/Template/wws-ban.html
+-rw-r--r--   0        0        0    16766 2023-05-12 03:16:55.041316 hikari_core-0.1.2/hikari_core/Template/wws-box-christmas.html
+-rw-r--r--   0        0        0    18454 2023-05-12 03:16:55.029646 hikari_core-0.1.2/hikari_core/Template/wws-clan.html
+-rw-r--r--   0        0        0    23636 2023-05-12 03:16:55.035273 hikari_core-0.1.2/hikari_core/Template/wws-info-recent.html
+-rw-r--r--   0        0        0    25512 2023-05-12 03:16:55.078284 hikari_core-0.1.2/hikari_core/Template/wws-info.html
+-rw-r--r--   0        0        0     2396 2023-05-12 03:16:55.070709 hikari_core-0.1.2/hikari_core/Template/wws-personalRecord.html
+-rw-r--r--   0        0        0    21667 2023-05-12 03:16:55.042328 hikari_core-0.1.2/hikari_core/Template/wws-ship-recent.html
+-rw-r--r--   0        0        0    20760 2023-05-12 03:16:55.061585 hikari_core-0.1.2/hikari_core/Template/wws-ship.html
+-rw-r--r--   0        0        0     9455 2023-05-12 03:16:55.069704 hikari_core-0.1.2/hikari_core/Template/wws-sx.html
+-rw-r--r--   0        0        0     5793 2023-05-12 03:16:55.077269 hikari_core-0.1.2/hikari_core/Template/wws-unban.html
+-rw-r--r--   0        0        0     3537 2023-05-12 13:08:49.465546 hikari_core-0.1.2/hikari_core/utils.py
+-rw-r--r--   0        0        0    35823 2023-05-12 02:05:38.427107 hikari_core-0.1.2/LICENSE
+-rw-r--r--   0        0        0      521 2023-05-13 05:47:53.255659 hikari_core-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0       35 2023-05-12 02:05:38.429109 hikari_core-0.1.2/README.md
+-rw-r--r--   0        0        0      948 1970-01-01 00:00:00.000000 hikari_core-0.1.2/setup.py
+-rw-r--r--   0        0        0      781 1970-01-01 00:00:00.000000 hikari_core-0.1.2/PKG-INFO
```

### Comparing `hikari_core-0.1.1/hikari_core/__init__.py` & `hikari_core-0.1.2/hikari_core/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -2,15 +2,16 @@
 import time
 import traceback
 
 import jinja2
 from loguru import logger
 
 from .analyze import analyze_command
-from .data_source import set_render_params, template_path, hikari_config, set_config
+from .data_source import (hikari_config, set_config, set_render_params,
+                          template_path)
 from .Html_Render import html_to_pic
 from .model import Hikari, Input, Output, Ship, UserInfo
 from .utils import startup
 
 env = jinja2.Environment(
     loader=jinja2.FileSystemLoader(template_path), enable_async=True
 )
@@ -40,34 +41,39 @@
         userinfo = UserInfo(Platform=platform, PlatformId=PlatformId)
         ship = Ship()
         input = Input(Command_Text=command_text, ShipInfo=ship)
         output = Output()
         hikari = Hikari(UserInfo=userinfo,
                         Input=input, Output=output)
         hikari = await analyze_command(hikari)
-        hikari: Hikari = await hikari.Function(hikari)
+        if not hikari.Status == "error" and hikari.Function:
+            hikari: Hikari = await hikari.Function(hikari)
+            if hikari.Output.Data_Type == '''<class 'str'>''':
+                logger.info(hikari.Output.Data)
+                return hikari
+            else:
+                if hikari_config.auto_rendering:
+                    template = env.get_template(hikari.Output.Template)
+                    template_data = await set_render_params(hikari.Output.Data)
+                    content = await template.render_async(template_data)
+                    hikari.success(
+                        await html_to_pic(content, wait=0, viewport={"width": hikari.Output.Width, "height": hikari.Output.Height}, use_browser=hikari_config.use_browser))
+                logger.info(hikari.Output.Data_Type)
         if hikari.Output.Data_Type == '''<class 'str'>''':
-            return hikari
-        else:
-            if hikari_config.auto_rendering:
-                template = env.get_template(hikari.Output.Template)
-                template_data = await set_render_params(hikari.Output.Data)
-                content = await template.render_async(template_data)
-                hikari.success(
-                    await html_to_pic(content, wait=0, viewport={"width": hikari.Output.Width, "height": hikari.Output.Height}, use_browser=hikari_config.use_browser))
-            logger.info(hikari.Output.Data_Type)
-            return hikari
+            logger.info(hikari.Output.Data)
+        return hikari
     except Exception:
         logger.error(traceback.format_exc())
         return hikari.error("解析指令时发生错误，请确认输入参数无误")
 
 
 mtime = os.path.getmtime(template_path/"wws-info.html")
 if time.time()-mtime > 86400:
     startup()
+
 logger.add(
     "hikari-core-logs/error.log",
     rotation="00:00",
     retention="1 week",
     diagnose=False,
     level="ERROR",
     encoding="utf-8",
```

### Comparing `hikari_core-0.1.1/hikari_core/analyze.py` & `hikari_core-0.1.2/hikari_core/analyze.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,28 +1,27 @@
 import html
 import re
 import traceback
 from datetime import datetime
-from typing import List, Tuple
 
 from loguru import logger
 
-from .command_select import Func, select_command
-from .model import Hikari, Input, Output, Ship, UserInfo
-from .moudle.wws_recent import get_RecentInfo
+from .command_select import select_command
+from .data_source import servers
+from .model import Hikari
 from .moudle.wws_info import get_AccountInfo
+from .moudle.wws_recent import get_RecentInfo
 from .utils import match_keywords
-from .data_source import servers
 
 
 async def analyze_command(hikari: Hikari) -> Hikari:
     try:
         if hikari.Status == 'init':  # 状态为init时才解析
             if not hikari.Input.Command_Text:
-                return hikari.success("请发送wws help查看帮助")
+                return hikari.error("请发送wws help查看帮助")
             hikari.Input.Command_Text = html.unescape(
                 str(hikari.Input.Command_Text)).strip()
             hikari = await extract_with_special_name(hikari)
             hikari.Function, hikari.Input.Command_List = await select_command(hikari.Input.Command_List)
             hikari = await extract_with_me_or_at(hikari)
             hikari = await extract_with_function(hikari)
         return hikari
```

### Comparing `hikari_core-0.1.1/hikari_core/command_select.py` & `hikari_core-0.1.2/hikari_core/command_select.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/data_source.py` & `hikari_core-0.1.2/hikari_core/data_source.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/__init__.py` & `hikari_core-0.1.2/hikari_core/Html_Render/__init__.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/browser.py` & `hikari_core-0.1.2/hikari_core/Html_Render/browser.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/data_source.py` & `hikari_core-0.1.2/hikari_core/Html_Render/data_source.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/templates/github-markdown-light.css` & `hikari_core-0.1.2/hikari_core/Html_Render/templates/github-markdown-light.css`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/templates/katex/katex.min.b64_fonts.css` & `hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/katex.min.b64_fonts.css`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/templates/katex/katex.min.js` & `hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/katex.min.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/templates/katex/mathtex-script-type.min.js` & `hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/mathtex-script-type.min.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/templates/markdown.html` & `hikari_core-0.1.2/hikari_core/Html_Render/templates/markdown.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Html_Render/templates/pygments-default.css` & `hikari_core-0.1.2/hikari_core/Html_Render/templates/pygments-default.css`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/HttpClient_Pool.py` & `hikari_core-0.1.2/hikari_core/HttpClient_Pool.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/model.py` & `hikari_core-0.1.2/hikari_core/model.py`

 * *Files 5% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 
 
 @runtime_checkable
 class Func(Protocol):
     async def __call__(self, **kwargs):
         ...
 
+
 class UserInfo(BaseModel):
     Platform: str
     PlatformId: str
 
 
 class Ship(BaseModel):
     Ship_Nation: Optional[str]
@@ -45,15 +46,15 @@
     Data: Union[str, int, bytes] = Field("初始化", description="返回的数据")
     Template: Optional[str]
     Width: Optional[int]
     Height: Optional[int]
 
 
 class Hikari(BaseModel):
-    Status: str = "init"
+    Status: str = "init"            #init:初始化 success:请求成功  failed:请求成功但API有错误或空返回  error:异常及本地错误
     UserInfo: UserInfo
     Function: Func = None
     Input: Optional[Input]
     Output: Optional[Output]
 
     class Config:
         arbitrary_types_allowed = True
@@ -66,15 +67,19 @@
 
     def success(self, success_data):
         self.Status = "success"
         self.Output.Data = success_data
         self.Output.Data_Type = str(type(success_data))
         return self
 
+    def failed(self, failed_data):
+        self.Status = "failed"
+        self.Output.Data = failed_data
+        self.Output.Data_Type = str(type(failed_data))
+        return self
+
     def wait(self, select_data: List):
         self.Status = "wait"
         self.Input.Select_Data = select_data
         self.Output.Data = "等待选择"
         self.Output.Data_Type = str(type(self.Output.Data))
         return self
-
-
```

### Comparing `hikari_core-0.1.1/hikari_core/moudle/__pycache__/publicAPI.cpython-310.pyc` & `hikari_core-0.1.2/hikari_core/moudle/__pycache__/publicAPI.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/moudle/__pycache__/wws_info.cpython-310.pyc` & `hikari_core-0.1.2/hikari_core/moudle/__pycache__/wws_info.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/moudle/__pycache__/wws_recent.cpython-310.pyc` & `hikari_core-0.1.2/hikari_core/moudle/__pycache__/wws_recent.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/moudle/publicAPI.py` & `hikari_core-0.1.2/hikari_core/moudle/publicAPI.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/moudle/wws_info.py` & `hikari_core-0.1.2/hikari_core/moudle/wws_info.py`

 * *Files 7% similar despite different names*

```diff
@@ -31,24 +31,25 @@
         else:
             params = {"server": hikari.Input.Platform,
                       "accountId": hikari.Input.PlatformId}
         resp = await client_yuyuko.get(url, params=params, timeout=None)
         result = orjson.loads(resp.content)
         logger.success(
             f"本次请求总耗时{resp.elapsed.total_seconds()*1000}，服务器计算耗时:{result['queryTime']}")
+        hikari.Output.Yuyuko_Code = result["code"]
         if result["code"] == 200 and result["data"]:
             hikari.Output.Template = "wws-info.html"
             hikari.Output.Width = 920
             hikari.Output.Height = 1000
             return hikari.success(result["data"])
         elif result["code"] == 403:
-            return hikari.success(f"{result['message']}\n请先绑定账号")
+            return hikari.failed(f"{result['message']}\n请先绑定账号")
         elif result["code"] == 500:
-            return hikari.success(f"{result['message']}\n这是服务器问题，请联系雨季麻麻")
+            return hikari.failed(f"{result['message']}\n这是服务器问题，请联系雨季麻麻")
         else:
-            return hikari.success(f"{result['message']}")
+            return hikari.failed(f"{result['message']}")
     except (TimeoutError, ConnectTimeout):
         logger.warning(traceback.format_exc())
         return hikari.erroe("请求超时了，请过会儿再尝试哦~")
     except Exception:
         logger.error(traceback.format_exc())
         return hikari.error("wuwuwu出了点问题，请联系麻麻解决")
```

### Comparing `hikari_core-0.1.1/hikari_core/moudle/wws_recent.py` & `hikari_core-0.1.2/hikari_core/moudle/wws_recent.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/Chart.min.js` & `hikari_core-0.1.2/hikari_core/Template/Chart.min.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/chartjs-plugin-datalabels@1.0.0.js` & `hikari_core-0.1.2/hikari_core/Template/chartjs-plugin-datalabels@1.0.0.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/echarts.js` & `hikari_core-0.1.2/hikari_core/Template/echarts.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/select-ship.html` & `hikari_core-0.1.2/hikari_core/Template/select-ship.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/ship-rank.html` & `hikari_core-0.1.2/hikari_core/Template/ship-rank.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-ban.html` & `hikari_core-0.1.2/hikari_core/Template/wws-ban.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-box-christmas.html` & `hikari_core-0.1.2/hikari_core/Template/wws-box-christmas.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-clan.html` & `hikari_core-0.1.2/hikari_core/Template/wws-clan.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-info-recent.html` & `hikari_core-0.1.2/hikari_core/Template/wws-info-recent.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-info.html` & `hikari_core-0.1.2/hikari_core/Template/wws-info.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-personalRecord.html` & `hikari_core-0.1.2/hikari_core/Template/wws-personalRecord.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-ship-recent.html` & `hikari_core-0.1.2/hikari_core/Template/wws-ship-recent.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-ship.html` & `hikari_core-0.1.2/hikari_core/Template/wws-ship.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-sx.html` & `hikari_core-0.1.2/hikari_core/Template/wws-sx.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/Template/wws-unban.html` & `hikari_core-0.1.2/hikari_core/Template/wws-unban.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/hikari_core/utils.py` & `hikari_core-0.1.2/hikari_core/utils.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/LICENSE` & `hikari_core-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.1/pyproject.toml` & `hikari_core-0.1.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "hikari-core"
-version = "0.1.1"
+version = "0.1.2"
 description = ""
 authors = ["benx1n <1119809439@qq.com>"]
 readme = "README.md"
 packages = [{include = "hikari_core"}]
 
 [tool.poetry.dependencies]
 python = "^3.8"
```

### Comparing `hikari_core-0.1.1/setup.py` & `hikari_core-0.1.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -17,15 +17,15 @@
  'jinja2>=3.1.2,<4.0.0',
  'orjson>=3.8.11,<4.0.0',
  'playwright>=1.17.2',
  'pydantic>=1.10.7,<2.0.0']
 
 setup_kwargs = {
     'name': 'hikari-core',
-    'version': '0.1.1',
+    'version': '0.1.2',
     'description': '',
     'long_description': '# Hikari-core\nSDK for yuyuko API\n',
     'author': 'benx1n',
     'author_email': '1119809439@qq.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

### Comparing `hikari_core-0.1.1/PKG-INFO` & `hikari_core-0.1.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hikari-core
-Version: 0.1.1
+Version: 0.1.2
 Summary: 
 Author: benx1n
 Author-email: 1119809439@qq.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

