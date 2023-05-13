# Comparing `tmp/nonebot_plugin_arkgacha-0.1.3.tar.gz` & `tmp/nonebot_plugin_arkgacha-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_arkgacha-0.1.3.tar", last modified: Sat May 13 02:38:34 2023, max compression
+gzip compressed data, was "nonebot_plugin_arkgacha-0.1.4.tar", last modified: Sat May 13 02:43:34 2023, max compression
```

## Comparing `nonebot_plugin_arkgacha-0.1.3.tar` & `nonebot_plugin_arkgacha-0.1.4.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0    34522 2021-09-10 07:59:22.042000 nonebot_plugin_arkgacha-0.1.3/LICENSE
--rw-r--r--   0        0        0     1772 2023-05-13 02:18:11.841037 nonebot_plugin_arkgacha-0.1.3/README.md
--rw-r--r--   0        0        0     4705 2023-05-13 02:12:25.739927 nonebot_plugin_arkgacha-0.1.3/nonebot_plugin_arkgacha/__init__.py
--rw-r--r--   0        0        0      175 2023-05-12 12:54:47.496416 nonebot_plugin_arkgacha-0.1.3/nonebot_plugin_arkgacha/config.py
--rw-r--r--   0        0        0      631 2023-05-13 02:38:34.676684 nonebot_plugin_arkgacha-0.1.3/pyproject.toml
--rw-r--r--   0        0        0     2183 1970-01-01 00:00:00.000000 nonebot_plugin_arkgacha-0.1.3/PKG-INFO
+-rw-r--r--   0        0        0    34522 2021-09-10 07:59:22.042000 nonebot_plugin_arkgacha-0.1.4/LICENSE
+-rw-r--r--   0        0        0     1772 2023-05-13 02:18:11.841037 nonebot_plugin_arkgacha-0.1.4/README.md
+-rw-r--r--   0        0        0     4705 2023-05-13 02:42:53.800211 nonebot_plugin_arkgacha-0.1.4/nonebot_plugin_arkgacha/__init__.py
+-rw-r--r--   0        0        0      175 2023-05-12 12:54:47.496416 nonebot_plugin_arkgacha-0.1.4/nonebot_plugin_arkgacha/config.py
+-rw-r--r--   0        0        0      631 2023-05-13 02:43:34.479845 nonebot_plugin_arkgacha-0.1.4/pyproject.toml
+-rw-r--r--   0        0        0     2183 1970-01-01 00:00:00.000000 nonebot_plugin_arkgacha-0.1.4/PKG-INFO
```

### Comparing `nonebot_plugin_arkgacha-0.1.3/LICENSE` & `nonebot_plugin_arkgacha-0.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_arkgacha-0.1.3/README.md` & `nonebot_plugin_arkgacha-0.1.4/README.md`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_arkgacha-0.1.3/nonebot_plugin_arkgacha/__init__.py` & `nonebot_plugin_arkgacha-0.1.4/nonebot_plugin_arkgacha/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -68,15 +68,15 @@
 @help_regex.handle()
 async def _():
     await help_regex.finish(
         "可用命令：\n"
         "方舟抽卡 [count = 10]\n"
         "方舟十连\n"
         "方舟抽卡帮助\n"
-        "方舟抽卡更新\n"
+        "方舟卡池更新\n"
     )
 
 
 @update_regex.handle()
 async def _():
     if new := (await gacha.update()):
         await update_regex.finish(
```

### Comparing `nonebot_plugin_arkgacha-0.1.3/pyproject.toml` & `nonebot_plugin_arkgacha-0.1.4/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "nonebot-plugin-arkgacha"
-version = "0.1.3"
+version = "0.1.4"
 description = "Plugin for Arknights gacha, support multi platform"
 authors = [
     { name = "RF-Tar-Railt", email = "3165388245@qq.com" },
 ]
 dependencies = [
     "nonebot2>=2.0.0rc4",
     "nonebot-plugin-alconna>=0.4.2",
```

### Comparing `nonebot_plugin_arkgacha-0.1.3/PKG-INFO` & `nonebot_plugin_arkgacha-0.1.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-arkgacha
-Version: 0.1.3
+Version: 0.1.4
 Summary: Plugin for Arknights gacha, support multi platform
 Author-Email: RF-Tar-Railt <3165388245@qq.com>
 License: MIT
 Requires-Python: >=3.8
 Requires-Dist: nonebot2>=2.0.0rc4
 Requires-Dist: nonebot-plugin-alconna>=0.4.2
 Requires-Dist: nonebot-plugin-send-anything-anywhere>=0.2.4
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-arkgacha Version: 0.1.3 Summary:
+Metadata-Version: 2.1 Name: nonebot-plugin-arkgacha Version: 0.1.4 Summary:
 Plugin for Arknights gacha, support multi platform Author-Email: RF-Tar-Railt
 <3165388245@qq.com> License: MIT Requires-Python: >=3.8 Requires-Dist:
 nonebot2>=2.0.0rc4 Requires-Dist: nonebot-plugin-alconna>=0.4.2 Requires-Dist:
 nonebot-plugin-send-anything-anywhere>=0.2.4 Requires-Dist: arknights-
 toolkit>=0.5.2 Requires-Dist: nonebot-plugin-localstore>=0.4.1 Description-
 Content-Type: text/markdown
                                    [nonebot]
```

