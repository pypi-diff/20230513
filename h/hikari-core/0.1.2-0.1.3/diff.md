# Comparing `tmp/hikari_core-0.1.2.tar.gz` & `tmp/hikari_core-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hikari_core-0.1.2.tar", max compression
+gzip compressed data, was "hikari_core-0.1.3.tar", max compression
```

## Comparing `hikari_core-0.1.2.tar` & `hikari_core-0.1.3.tar`

### file list

```diff
@@ -1,47 +1,47 @@
--rw-r--r--   0        0        0     2979 2023-05-12 18:39:10.835100 hikari_core-0.1.2/hikari_core/__init__.py
--rw-r--r--   0        0        0     4152 2023-05-12 18:40:02.649642 hikari_core-0.1.2/hikari_core/analyze.py
--rw-r--r--   0        0        0     3361 2023-05-12 16:59:43.442417 hikari_core-0.1.2/hikari_core/command_select.py
--rw-r--r--   0        0        0    12434 2023-05-12 18:09:43.557530 hikari_core-0.1.2/hikari_core/data_source.py
--rw-r--r--   0        0        0      719 2023-05-12 16:14:53.492016 hikari_core-0.1.2/hikari_core/Html_Render/__init__.py
--rw-r--r--   0        0        0     2901 2023-05-12 16:29:09.654986 hikari_core-0.1.2/hikari_core/Html_Render/browser.py
--rw-r--r--   0        0        0     5462 2023-05-12 16:27:10.898314 hikari_core-0.1.2/hikari_core/Html_Render/data_source.py
--rw-r--r--   0        0        0    18237 2023-05-12 16:01:25.071577 hikari_core-0.1.2/hikari_core/Html_Render/templates/github-markdown-light.css
--rw-r--r--   0        0        0  1458204 2023-05-12 16:01:25.084174 hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/katex.min.b64_fonts.css
--rw-r--r--   0        0        0   270288 2023-05-12 16:01:25.123214 hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/katex.min.js
--rw-r--r--   0        0        0     1290 2023-05-12 16:01:25.124230 hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/mathtex-script-type.min.js
--rw-r--r--   0        0        0      662 2023-05-12 16:01:25.127272 hikari_core-0.1.2/hikari_core/Html_Render/templates/markdown.html
--rw-r--r--   0        0        0     4963 2023-05-12 16:01:25.128288 hikari_core-0.1.2/hikari_core/Html_Render/templates/pygments-default.css
--rw-r--r--   0        0        0      125 2023-05-12 16:01:25.129291 hikari_core-0.1.2/hikari_core/Html_Render/templates/text.css
--rw-r--r--   0        0        0      233 2023-05-12 16:01:25.129291 hikari_core-0.1.2/hikari_core/Html_Render/templates/text.html
--rw-r--r--   0        0        0      937 2023-05-12 17:40:06.718420 hikari_core-0.1.2/hikari_core/HttpClient_Pool.py
--rw-r--r--   0        0        0     2492 2023-05-12 18:38:28.768568 hikari_core-0.1.2/hikari_core/model.py
--rw-r--r--   0        0        0        0 2023-05-12 06:05:30.059172 hikari_core-0.1.2/hikari_core/moudle/__init__.py
--rw-r--r--   0        0        0      175 2023-05-12 06:05:32.348596 hikari_core-0.1.2/hikari_core/moudle/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0     5400 2023-05-12 06:07:09.234200 hikari_core-0.1.2/hikari_core/moudle/__pycache__/publicAPI.cpython-310.pyc
--rw-r--r--   0        0        0     2914 2023-05-12 06:06:54.456117 hikari_core-0.1.2/hikari_core/moudle/__pycache__/wws_info.cpython-310.pyc
--rw-r--r--   0        0        0     3105 2023-05-12 06:07:46.904239 hikari_core-0.1.2/hikari_core/moudle/__pycache__/wws_recent.cpython-310.pyc
--rw-r--r--   0        0        0     7226 2023-05-12 16:47:03.778682 hikari_core-0.1.2/hikari_core/moudle/publicAPI.py
--rw-r--r--   0        0        0     2566 2023-05-12 18:34:05.942459 hikari_core-0.1.2/hikari_core/moudle/wws_info.py
--rw-r--r--   0        0        0     4501 2023-05-12 16:56:20.219036 hikari_core-0.1.2/hikari_core/moudle/wws_recent.py
--rw-r--r--   0        0        0   173077 2023-05-12 03:16:55.137328 hikari_core-0.1.2/hikari_core/Template/Chart.min.js
--rw-r--r--   0        0        0    13279 2023-05-12 03:16:55.058560 hikari_core-0.1.2/hikari_core/Template/chartjs-plugin-datalabels@1.0.0.js
--rw-r--r--   0        0        0  3313391 2023-05-12 03:16:55.346040 hikari_core-0.1.2/hikari_core/Template/echarts.js
--rw-r--r--   0        0        0     3710 2023-05-12 03:16:55.039314 hikari_core-0.1.2/hikari_core/Template/select-ship.html
--rw-r--r--   0        0        0     5118 2023-05-12 03:16:55.034251 hikari_core-0.1.2/hikari_core/Template/ship-rank.html
--rw-r--r--   0        0        0      225 2023-05-12 03:16:55.063600 hikari_core-0.1.2/hikari_core/Template/text-help.css
--rw-r--r--   0        0        0     7293 2023-05-12 03:16:55.073236 hikari_core-0.1.2/hikari_core/Template/wws-ban.html
--rw-r--r--   0        0        0    16766 2023-05-12 03:16:55.041316 hikari_core-0.1.2/hikari_core/Template/wws-box-christmas.html
--rw-r--r--   0        0        0    18454 2023-05-12 03:16:55.029646 hikari_core-0.1.2/hikari_core/Template/wws-clan.html
--rw-r--r--   0        0        0    23636 2023-05-12 03:16:55.035273 hikari_core-0.1.2/hikari_core/Template/wws-info-recent.html
--rw-r--r--   0        0        0    25512 2023-05-12 03:16:55.078284 hikari_core-0.1.2/hikari_core/Template/wws-info.html
--rw-r--r--   0        0        0     2396 2023-05-12 03:16:55.070709 hikari_core-0.1.2/hikari_core/Template/wws-personalRecord.html
--rw-r--r--   0        0        0    21667 2023-05-12 03:16:55.042328 hikari_core-0.1.2/hikari_core/Template/wws-ship-recent.html
--rw-r--r--   0        0        0    20760 2023-05-12 03:16:55.061585 hikari_core-0.1.2/hikari_core/Template/wws-ship.html
--rw-r--r--   0        0        0     9455 2023-05-12 03:16:55.069704 hikari_core-0.1.2/hikari_core/Template/wws-sx.html
--rw-r--r--   0        0        0     5793 2023-05-12 03:16:55.077269 hikari_core-0.1.2/hikari_core/Template/wws-unban.html
--rw-r--r--   0        0        0     3537 2023-05-12 13:08:49.465546 hikari_core-0.1.2/hikari_core/utils.py
--rw-r--r--   0        0        0    35823 2023-05-12 02:05:38.427107 hikari_core-0.1.2/LICENSE
--rw-r--r--   0        0        0      521 2023-05-13 05:47:53.255659 hikari_core-0.1.2/pyproject.toml
--rw-r--r--   0        0        0       35 2023-05-12 02:05:38.429109 hikari_core-0.1.2/README.md
--rw-r--r--   0        0        0      948 1970-01-01 00:00:00.000000 hikari_core-0.1.2/setup.py
--rw-r--r--   0        0        0      781 1970-01-01 00:00:00.000000 hikari_core-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0     3427 2023-05-13 06:35:40.192792 hikari_core-0.1.3/hikari_core/__init__.py
+-rw-r--r--   0        0        0     4152 2023-05-12 18:40:02.649642 hikari_core-0.1.3/hikari_core/analyze.py
+-rw-r--r--   0        0        0     3361 2023-05-12 16:59:43.442417 hikari_core-0.1.3/hikari_core/command_select.py
+-rw-r--r--   0        0        0    12076 2023-05-13 06:36:00.880449 hikari_core-0.1.3/hikari_core/data_source.py
+-rw-r--r--   0        0        0      719 2023-05-12 16:14:53.492016 hikari_core-0.1.3/hikari_core/Html_Render/__init__.py
+-rw-r--r--   0        0        0     2901 2023-05-12 16:29:09.654986 hikari_core-0.1.3/hikari_core/Html_Render/browser.py
+-rw-r--r--   0        0        0     5462 2023-05-12 16:27:10.898314 hikari_core-0.1.3/hikari_core/Html_Render/data_source.py
+-rw-r--r--   0        0        0    18237 2023-05-12 16:01:25.071577 hikari_core-0.1.3/hikari_core/Html_Render/templates/github-markdown-light.css
+-rw-r--r--   0        0        0  1458204 2023-05-12 16:01:25.084174 hikari_core-0.1.3/hikari_core/Html_Render/templates/katex/katex.min.b64_fonts.css
+-rw-r--r--   0        0        0   270288 2023-05-12 16:01:25.123214 hikari_core-0.1.3/hikari_core/Html_Render/templates/katex/katex.min.js
+-rw-r--r--   0        0        0     1290 2023-05-12 16:01:25.124230 hikari_core-0.1.3/hikari_core/Html_Render/templates/katex/mathtex-script-type.min.js
+-rw-r--r--   0        0        0      662 2023-05-12 16:01:25.127272 hikari_core-0.1.3/hikari_core/Html_Render/templates/markdown.html
+-rw-r--r--   0        0        0     4963 2023-05-12 16:01:25.128288 hikari_core-0.1.3/hikari_core/Html_Render/templates/pygments-default.css
+-rw-r--r--   0        0        0      125 2023-05-12 16:01:25.129291 hikari_core-0.1.3/hikari_core/Html_Render/templates/text.css
+-rw-r--r--   0        0        0      233 2023-05-12 16:01:25.129291 hikari_core-0.1.3/hikari_core/Html_Render/templates/text.html
+-rw-r--r--   0        0        0      937 2023-05-12 17:40:06.718420 hikari_core-0.1.3/hikari_core/HttpClient_Pool.py
+-rw-r--r--   0        0        0     2492 2023-05-12 18:38:28.768568 hikari_core-0.1.3/hikari_core/model.py
+-rw-r--r--   0        0        0        0 2023-05-12 06:05:30.059172 hikari_core-0.1.3/hikari_core/moudle/__init__.py
+-rw-r--r--   0        0        0      175 2023-05-12 06:05:32.348596 hikari_core-0.1.3/hikari_core/moudle/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     5400 2023-05-12 06:07:09.234200 hikari_core-0.1.3/hikari_core/moudle/__pycache__/publicAPI.cpython-310.pyc
+-rw-r--r--   0        0        0     2914 2023-05-12 06:06:54.456117 hikari_core-0.1.3/hikari_core/moudle/__pycache__/wws_info.cpython-310.pyc
+-rw-r--r--   0        0        0     3105 2023-05-12 06:07:46.904239 hikari_core-0.1.3/hikari_core/moudle/__pycache__/wws_recent.cpython-310.pyc
+-rw-r--r--   0        0        0     7226 2023-05-12 16:47:03.778682 hikari_core-0.1.3/hikari_core/moudle/publicAPI.py
+-rw-r--r--   0        0        0     2566 2023-05-12 18:34:05.942459 hikari_core-0.1.3/hikari_core/moudle/wws_info.py
+-rw-r--r--   0        0        0     4501 2023-05-12 16:56:20.219036 hikari_core-0.1.3/hikari_core/moudle/wws_recent.py
+-rw-r--r--   0        0        0   173077 2023-05-12 03:16:55.137328 hikari_core-0.1.3/hikari_core/Template/Chart.min.js
+-rw-r--r--   0        0        0    13279 2023-05-12 03:16:55.058560 hikari_core-0.1.3/hikari_core/Template/chartjs-plugin-datalabels@1.0.0.js
+-rw-r--r--   0        0        0  3313391 2023-05-12 03:16:55.346040 hikari_core-0.1.3/hikari_core/Template/echarts.js
+-rw-r--r--   0        0        0     3710 2023-05-12 03:16:55.039314 hikari_core-0.1.3/hikari_core/Template/select-ship.html
+-rw-r--r--   0        0        0     5118 2023-05-12 03:16:55.034251 hikari_core-0.1.3/hikari_core/Template/ship-rank.html
+-rw-r--r--   0        0        0      225 2023-05-12 03:16:55.063600 hikari_core-0.1.3/hikari_core/Template/text-help.css
+-rw-r--r--   0        0        0     7293 2023-05-12 03:16:55.073236 hikari_core-0.1.3/hikari_core/Template/wws-ban.html
+-rw-r--r--   0        0        0    16766 2023-05-12 03:16:55.041316 hikari_core-0.1.3/hikari_core/Template/wws-box-christmas.html
+-rw-r--r--   0        0        0    18454 2023-05-12 03:16:55.029646 hikari_core-0.1.3/hikari_core/Template/wws-clan.html
+-rw-r--r--   0        0        0    23636 2023-05-12 03:16:55.035273 hikari_core-0.1.3/hikari_core/Template/wws-info-recent.html
+-rw-r--r--   0        0        0    25512 2023-05-12 03:16:55.078284 hikari_core-0.1.3/hikari_core/Template/wws-info.html
+-rw-r--r--   0        0        0     2396 2023-05-12 03:16:55.070709 hikari_core-0.1.3/hikari_core/Template/wws-personalRecord.html
+-rw-r--r--   0        0        0    21667 2023-05-12 03:16:55.042328 hikari_core-0.1.3/hikari_core/Template/wws-ship-recent.html
+-rw-r--r--   0        0        0    20760 2023-05-12 03:16:55.061585 hikari_core-0.1.3/hikari_core/Template/wws-ship.html
+-rw-r--r--   0        0        0     9455 2023-05-12 03:16:55.069704 hikari_core-0.1.3/hikari_core/Template/wws-sx.html
+-rw-r--r--   0        0        0     5793 2023-05-12 03:16:55.077269 hikari_core-0.1.3/hikari_core/Template/wws-unban.html
+-rw-r--r--   0        0        0     3537 2023-05-12 13:08:49.465546 hikari_core-0.1.3/hikari_core/utils.py
+-rw-r--r--   0        0        0    35823 2023-05-12 02:05:38.427107 hikari_core-0.1.3/LICENSE
+-rw-r--r--   0        0        0      521 2023-05-13 06:41:12.837144 hikari_core-0.1.3/pyproject.toml
+-rw-r--r--   0        0        0       35 2023-05-12 02:05:38.429109 hikari_core-0.1.3/README.md
+-rw-r--r--   0        0        0      948 1970-01-01 00:00:00.000000 hikari_core-0.1.3/setup.py
+-rw-r--r--   0        0        0      781 1970-01-01 00:00:00.000000 hikari_core-0.1.3/PKG-INFO
```

### Comparing `hikari_core-0.1.2/hikari_core/__init__.py` & `hikari_core-0.1.3/hikari_core/__init__.py`

 * *Files 20% similar despite different names*

```diff
@@ -22,21 +22,27 @@
 )
 
 
 async def init_hikari(
     platform: str,
     PlatformId: str,
     command_text: str = None,
+    auto_rendering: bool = True,
+    auto_image: bool = True,
+    use_broswer: str = "chromium"
 ) -> Hikari:
-    """Hikari初始化
+    """Hikari初始化，如果进行过set_config，则会覆盖这边的对应配置
 
     Args:
         platform (str): 平台类型
         PlatformId (str): 平台ID
         command_text (str): 传入指令，不带wws
+        auto_rendering (bool): 自动填充模板，默认启用
+        auto_image (bool): 是否自动渲染，默认启用，若auto_rending未启用则该项配置无效
+        use_broswer (str): chromium/firefox，默认chromium，性能大约为firefox三倍
 
     Returns:
         Hikari: 可通过Hikari.Output.Data内数据判断是否输出
     """
     try:
         userinfo = UserInfo(Platform=platform, PlatformId=PlatformId)
         ship = Ship()
@@ -47,20 +53,21 @@
         hikari = await analyze_command(hikari)
         if not hikari.Status == "error" and hikari.Function:
             hikari: Hikari = await hikari.Function(hikari)
             if hikari.Output.Data_Type == '''<class 'str'>''':
                 logger.info(hikari.Output.Data)
                 return hikari
             else:
-                if hikari_config.auto_rendering:
+                if auto_rendering:
                     template = env.get_template(hikari.Output.Template)
                     template_data = await set_render_params(hikari.Output.Data)
                     content = await template.render_async(template_data)
-                    hikari.success(
-                        await html_to_pic(content, wait=0, viewport={"width": hikari.Output.Width, "height": hikari.Output.Height}, use_browser=hikari_config.use_browser))
+                    if auto_image:
+                        hikari.success(
+                            await html_to_pic(content, wait=0, viewport={"width": hikari.Output.Width, "height": hikari.Output.Height}, use_browser=use_broswer))
                 logger.info(hikari.Output.Data_Type)
         if hikari.Output.Data_Type == '''<class 'str'>''':
             logger.info(hikari.Output.Data)
         return hikari
     except Exception:
         logger.error(traceback.format_exc())
         return hikari.error("解析指令时发生错误，请确认输入参数无误")
```

### Comparing `hikari_core-0.1.2/hikari_core/analyze.py` & `hikari_core-0.1.3/hikari_core/analyze.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/command_select.py` & `hikari_core-0.1.3/hikari_core/command_select.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/data_source.py` & `hikari_core-0.1.3/hikari_core/data_source.py`

 * *Files 3% similar despite different names*

```diff
@@ -9,39 +9,33 @@
 yuyuko_url = "https://api.wows.shinoaki.com"
 
 
 class config:
     proxy: str = None
     http2: bool = True
     token: str = None
-    auto_rendering: bool = True
-    use_browser: str = "chromium"
 
 
 hikari_config = config()
 
 
-async def set_config(proxy: str = None, http2: bool = True, token: str = None, auto_rendering: bool = True, use_browser: str = "chromium"):
+async def set_config(proxy: str = None, http2: bool = True, token: str = None):
     """配置Hikari-core
 
     Args:
         proxy (str): 访问WG使用的代理，格式http://localhost:7890
         http2 (bool): 是否开启http2，默认启用
         token (str): #请加群联系雨季获取api_key和token Q群:967546463
-        auto_rendering (bool): 是否自动渲染图片，默认启用
-        use_broswer (str): chromium/firefox，默认chromium
 
     Returns:
         Hikari: 可通过Hikari.Output.Data内数据判断是否输出
     """
     hikari_config.proxy = proxy
     hikari_config.http2 = http2
     hikari_config.token = token
-    hikari_config.auto_rendering = auto_rendering
-    hikari_config.use_browser = use_browser
 
 
 @dataclass
 class matching:
     keywords: Tuple[str, ...]
     match_keywords: str
```

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/__init__.py` & `hikari_core-0.1.3/hikari_core/Html_Render/__init__.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/browser.py` & `hikari_core-0.1.3/hikari_core/Html_Render/browser.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/data_source.py` & `hikari_core-0.1.3/hikari_core/Html_Render/data_source.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/templates/github-markdown-light.css` & `hikari_core-0.1.3/hikari_core/Html_Render/templates/github-markdown-light.css`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/katex.min.b64_fonts.css` & `hikari_core-0.1.3/hikari_core/Html_Render/templates/katex/katex.min.b64_fonts.css`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/katex.min.js` & `hikari_core-0.1.3/hikari_core/Html_Render/templates/katex/katex.min.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/templates/katex/mathtex-script-type.min.js` & `hikari_core-0.1.3/hikari_core/Html_Render/templates/katex/mathtex-script-type.min.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/templates/markdown.html` & `hikari_core-0.1.3/hikari_core/Html_Render/templates/markdown.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Html_Render/templates/pygments-default.css` & `hikari_core-0.1.3/hikari_core/Html_Render/templates/pygments-default.css`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/HttpClient_Pool.py` & `hikari_core-0.1.3/hikari_core/HttpClient_Pool.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/model.py` & `hikari_core-0.1.3/hikari_core/model.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/moudle/__pycache__/publicAPI.cpython-310.pyc` & `hikari_core-0.1.3/hikari_core/moudle/__pycache__/publicAPI.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/moudle/__pycache__/wws_info.cpython-310.pyc` & `hikari_core-0.1.3/hikari_core/moudle/__pycache__/wws_info.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/moudle/__pycache__/wws_recent.cpython-310.pyc` & `hikari_core-0.1.3/hikari_core/moudle/__pycache__/wws_recent.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/moudle/publicAPI.py` & `hikari_core-0.1.3/hikari_core/moudle/publicAPI.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/moudle/wws_info.py` & `hikari_core-0.1.3/hikari_core/moudle/wws_info.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/moudle/wws_recent.py` & `hikari_core-0.1.3/hikari_core/moudle/wws_recent.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/Chart.min.js` & `hikari_core-0.1.3/hikari_core/Template/Chart.min.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/chartjs-plugin-datalabels@1.0.0.js` & `hikari_core-0.1.3/hikari_core/Template/chartjs-plugin-datalabels@1.0.0.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/echarts.js` & `hikari_core-0.1.3/hikari_core/Template/echarts.js`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/select-ship.html` & `hikari_core-0.1.3/hikari_core/Template/select-ship.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/ship-rank.html` & `hikari_core-0.1.3/hikari_core/Template/ship-rank.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-ban.html` & `hikari_core-0.1.3/hikari_core/Template/wws-ban.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-box-christmas.html` & `hikari_core-0.1.3/hikari_core/Template/wws-box-christmas.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-clan.html` & `hikari_core-0.1.3/hikari_core/Template/wws-clan.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-info-recent.html` & `hikari_core-0.1.3/hikari_core/Template/wws-info-recent.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-info.html` & `hikari_core-0.1.3/hikari_core/Template/wws-info.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-personalRecord.html` & `hikari_core-0.1.3/hikari_core/Template/wws-personalRecord.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-ship-recent.html` & `hikari_core-0.1.3/hikari_core/Template/wws-ship-recent.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-ship.html` & `hikari_core-0.1.3/hikari_core/Template/wws-ship.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-sx.html` & `hikari_core-0.1.3/hikari_core/Template/wws-sx.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/Template/wws-unban.html` & `hikari_core-0.1.3/hikari_core/Template/wws-unban.html`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/hikari_core/utils.py` & `hikari_core-0.1.3/hikari_core/utils.py`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/LICENSE` & `hikari_core-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `hikari_core-0.1.2/pyproject.toml` & `hikari_core-0.1.3/pyproject.toml`

 * *Files 26% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [tool.poetry]
 name = "hikari-core"
-version = "0.1.2"
+version = "0.1.3"
 description = ""
 authors = ["benx1n <1119809439@qq.com>"]
 readme = "README.md"
 packages = [{include = "hikari_core"}]
 
 [tool.poetry.dependencies]
 python = "^3.8"
 httpx = { version = ">=0.24.0", extras = ["http2"] }
 orjson = "^3.8.11"
 asyncio = "^3.4.3"
 APScheduler = "^3.10.1"
-jinja2 = "^3.1.2"
+jinja2 = "^3.0.0"
 pydantic = "^1.10.7"
 playwright = ">=1.17.2"
 aiofiles = ">=0.8.0"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `hikari_core-0.1.2/setup.py` & `hikari_core-0.1.3/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -10,22 +10,22 @@
  'hikari_core.Html_Render': ['templates/*', 'templates/katex/*']}
 
 install_requires = \
 ['APScheduler>=3.10.1,<4.0.0',
  'aiofiles>=0.8.0',
  'asyncio>=3.4.3,<4.0.0',
  'httpx[http2]>=0.24.0',
- 'jinja2>=3.1.2,<4.0.0',
+ 'jinja2>=3.0.0,<4.0.0',
  'orjson>=3.8.11,<4.0.0',
  'playwright>=1.17.2',
  'pydantic>=1.10.7,<2.0.0']
 
 setup_kwargs = {
     'name': 'hikari-core',
-    'version': '0.1.2',
+    'version': '0.1.3',
     'description': '',
     'long_description': '# Hikari-core\nSDK for yuyuko API\n',
     'author': 'benx1n',
     'author_email': '1119809439@qq.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

### Comparing `hikari_core-0.1.2/PKG-INFO` & `hikari_core-0.1.3/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 Metadata-Version: 2.1
 Name: hikari-core
-Version: 0.1.2
+Version: 0.1.3
 Summary: 
 Author: benx1n
 Author-email: 1119809439@qq.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: APScheduler (>=3.10.1,<4.0.0)
 Requires-Dist: aiofiles (>=0.8.0)
 Requires-Dist: asyncio (>=3.4.3,<4.0.0)
 Requires-Dist: httpx[http2] (>=0.24.0)
-Requires-Dist: jinja2 (>=3.1.2,<4.0.0)
+Requires-Dist: jinja2 (>=3.0.0,<4.0.0)
 Requires-Dist: orjson (>=3.8.11,<4.0.0)
 Requires-Dist: playwright (>=1.17.2)
 Requires-Dist: pydantic (>=1.10.7,<2.0.0)
 Description-Content-Type: text/markdown
 
 # Hikari-core
 SDK for yuyuko API
```

