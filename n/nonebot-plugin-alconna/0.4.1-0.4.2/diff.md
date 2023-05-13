# Comparing `tmp/nonebot-plugin-alconna-0.4.1.tar.gz` & `tmp/nonebot-plugin-alconna-0.4.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot-plugin-alconna-0.4.1.tar", last modified: Thu May 11 16:08:24 2023, max compression
+gzip compressed data, was "nonebot-plugin-alconna-0.4.2.tar", last modified: Sat May 13 01:54:28 2023, max compression
```

## Comparing `nonebot-plugin-alconna-0.4.1.tar` & `nonebot-plugin-alconna-0.4.2.tar`

### file list

```diff
@@ -1,31 +1,31 @@
--rw-r--r--   0        0        0     1091 2022-01-24 11:14:57.524011 nonebot-plugin-alconna-0.4.1/LICENSE
--rw-r--r--   0        0        0     1135 2023-05-11 15:54:27.386623 nonebot-plugin-alconna-0.4.1/pyproject.toml
--rw-r--r--   0        0        0     8579 2023-05-11 05:49:49.600962 nonebot-plugin-alconna-0.4.1/README.md
--rw-r--r--   0        0        0     1208 2023-05-10 08:50:46.247626 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/__init__.py
--rw-r--r--   0        0        0      383 2023-05-11 04:41:26.166268 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/__init__.py
--rw-r--r--   0        0        0      523 2023-05-10 10:09:15.599546 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/bilibili.py
--rw-r--r--   0        0        0     1007 2023-05-10 10:09:15.573188 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/console.py
--rw-r--r--   0        0        0     1661 2023-05-10 10:09:15.609172 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/ding.py
--rw-r--r--   0        0        0     2141 2023-05-10 10:09:15.564123 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/feishu.py
--rw-r--r--   0        0        0      519 2023-05-10 10:09:15.541809 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/github.py
--rw-r--r--   0        0        0     1163 2023-05-10 10:09:15.636179 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/kook.py
--rw-r--r--   0        0        0      761 2023-05-10 10:09:15.651191 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/minecraft.py
--rw-r--r--   0        0        0     3155 2023-05-10 10:09:15.519983 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/mirai.py
--rw-r--r--   0        0        0     1088 2023-05-10 10:09:15.628175 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/ntchat.py
--rw-r--r--   0        0        0     3177 2023-05-10 10:09:15.618177 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/onebot11.py
--rw-r--r--   0        0        0     2517 2023-05-10 10:09:15.661217 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/onebot12.py
--rw-r--r--   0        0        0     3227 2023-05-10 10:09:15.529594 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/qqguild.py
--rw-r--r--   0        0        0     3126 2023-05-10 10:09:15.670151 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/telegram.py
--rw-r--r--   0        0        0      581 2023-05-10 10:09:15.553296 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/argv.py
--rw-r--r--   0        0        0      405 2023-05-10 09:00:57.054628 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/config.py
--rw-r--r--   0        0        0      180 2023-05-10 08:33:24.079951 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/consts.py
--rw-r--r--   0        0        0      109 2023-05-11 15:42:43.320472 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/i18n/.config.json
--rw-r--r--   0        0        0      301 2023-05-11 15:42:18.920450 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/i18n/en-US.json
--rw-r--r--   0        0        0      262 2023-05-11 15:42:18.885191 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/i18n/zh-CN.json
--rw-r--r--   0        0        0     3812 2023-05-10 09:00:57.030628 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/matcher.py
--rw-r--r--   0        0        0     1499 2023-05-10 08:54:25.558632 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/matcher.pyi
--rw-r--r--   0        0        0     1448 2023-05-11 15:34:24.694684 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/model.py
--rw-r--r--   0        0        0     2187 2023-04-02 14:03:55.798752 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/params.py
--rw-r--r--   0        0        0     9235 2023-05-11 15:42:18.951219 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/rule.py
--rw-r--r--   0        0        0     1967 2023-05-11 04:48:52.932671 nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/typings.py
--rw-r--r--   0        0        0     8658 1970-01-01 00:00:00.000000 nonebot-plugin-alconna-0.4.1/PKG-INFO
+-rw-r--r--   0        0        0     1091 2022-01-24 11:14:57.524011 nonebot-plugin-alconna-0.4.2/LICENSE
+-rw-r--r--   0        0        0     1135 2023-05-13 01:53:49.312142 nonebot-plugin-alconna-0.4.2/pyproject.toml
+-rw-r--r--   0        0        0     8579 2023-05-11 05:49:49.600962 nonebot-plugin-alconna-0.4.2/README.md
+-rw-r--r--   0        0        0     1208 2023-05-10 08:50:46.247626 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/__init__.py
+-rw-r--r--   0        0        0      383 2023-05-11 04:41:26.166268 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/__init__.py
+-rw-r--r--   0        0        0      523 2023-05-10 10:09:15.599546 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/bilibili.py
+-rw-r--r--   0        0        0     1007 2023-05-10 10:09:15.573188 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/console.py
+-rw-r--r--   0        0        0     1661 2023-05-10 10:09:15.609172 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/ding.py
+-rw-r--r--   0        0        0     2141 2023-05-10 10:09:15.564123 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/feishu.py
+-rw-r--r--   0        0        0      519 2023-05-10 10:09:15.541809 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/github.py
+-rw-r--r--   0        0        0     1163 2023-05-10 10:09:15.636179 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/kook.py
+-rw-r--r--   0        0        0      761 2023-05-10 10:09:15.651191 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/minecraft.py
+-rw-r--r--   0        0        0     3155 2023-05-10 10:09:15.519983 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/mirai.py
+-rw-r--r--   0        0        0     1088 2023-05-10 10:09:15.628175 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/ntchat.py
+-rw-r--r--   0        0        0     3177 2023-05-10 10:09:15.618177 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/onebot11.py
+-rw-r--r--   0        0        0     2517 2023-05-10 10:09:15.661217 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/onebot12.py
+-rw-r--r--   0        0        0     3227 2023-05-10 10:09:15.529594 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/qqguild.py
+-rw-r--r--   0        0        0     3126 2023-05-10 10:09:15.670151 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/telegram.py
+-rw-r--r--   0        0        0      581 2023-05-10 10:09:15.553296 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/argv.py
+-rw-r--r--   0        0        0      405 2023-05-10 09:00:57.054628 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/config.py
+-rw-r--r--   0        0        0      180 2023-05-10 08:33:24.079951 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/consts.py
+-rw-r--r--   0        0        0      109 2023-05-11 15:42:43.320472 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/i18n/.config.json
+-rw-r--r--   0        0        0      301 2023-05-11 15:42:18.920450 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/i18n/en-US.json
+-rw-r--r--   0        0        0      262 2023-05-11 15:42:18.885191 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/i18n/zh-CN.json
+-rw-r--r--   0        0        0     3812 2023-05-10 09:00:57.030628 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/matcher.py
+-rw-r--r--   0        0        0     1499 2023-05-10 08:54:25.558632 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/matcher.pyi
+-rw-r--r--   0        0        0     1448 2023-05-11 15:34:24.694684 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/model.py
+-rw-r--r--   0        0        0     2187 2023-04-02 14:03:55.798752 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/params.py
+-rw-r--r--   0        0        0     9210 2023-05-13 01:50:44.284586 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/rule.py
+-rw-r--r--   0        0        0     1967 2023-05-11 04:48:52.932671 nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/typings.py
+-rw-r--r--   0        0        0     8658 1970-01-01 00:00:00.000000 nonebot-plugin-alconna-0.4.2/PKG-INFO
```

### Comparing `nonebot-plugin-alconna-0.4.1/LICENSE` & `nonebot-plugin-alconna-0.4.2/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/pyproject.toml` & `nonebot-plugin-alconna-0.4.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "nonebot-plugin-alconna"
-version = "0.4.1"
+version = "0.4.2"
 description = "Alconna Adapter for Nonebot"
 authors = [
     { name = "RF-Tar-Railt", email = "rf_tar_railt@qq.com" },
 ]
 dependencies = [
     "nonebot2>=2.0.0rc4",
     "arclet-alconna<2.0.0, >=1.7.0",
```

### Comparing `nonebot-plugin-alconna-0.4.1/README.md` & `nonebot-plugin-alconna-0.4.2/README.md`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/__init__.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/bilibili.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/bilibili.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/console.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/console.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/ding.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/ding.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/feishu.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/feishu.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/github.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/github.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/kook.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/kook.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/minecraft.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/minecraft.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/mirai.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/mirai.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/ntchat.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/ntchat.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/onebot11.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/onebot11.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/onebot12.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/onebot12.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/qqguild.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/qqguild.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/adapters/telegram.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/adapters/telegram.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/argv.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/argv.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/matcher.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/matcher.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/matcher.pyi` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/matcher.pyi`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/model.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/model.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/params.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/params.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/rule.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/rule.py`

 * *Files 1% similar despite different names*

```diff
@@ -181,15 +181,15 @@
         with output_manager.capture(self.command.name) as cap:
             output_manager.set_action(lambda x: x, self.command.name)
             try:
                 arp = await self.handle(bot, event, msg)
             except Exception as e:
                 arp = Arparma(self.command.path, msg, False, error_info=repr(e))
             may_help_text: Optional[str] = cap.get("output", None)
-        if not may_help_text and not arp.matched and not arp.head_matched and self.skip:
+        if not arp.matched and not may_help_text and self.skip:
             return False
         if self.auto_send and may_help_text:
             await bot.send(event, await self._convert(may_help_text, event, arp))
             return False
         for checker in self.checkers:
             if not checker(arp):
                 return False
```

### Comparing `nonebot-plugin-alconna-0.4.1/src/nonebot_plugin_alconna/typings.py` & `nonebot-plugin-alconna-0.4.2/src/nonebot_plugin_alconna/typings.py`

 * *Files identical despite different names*

### Comparing `nonebot-plugin-alconna-0.4.1/PKG-INFO` & `nonebot-plugin-alconna-0.4.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-alconna
-Version: 0.4.1
+Version: 0.4.2
 Summary: Alconna Adapter for Nonebot
 License: MIT
 Keywords: command,argparse,cli,alconna,nonebot
 Author-email: RF-Tar-Railt <rf_tar_railt@qq.com>
 Requires-Python: >=3.8
 Project-URL: repository, https://github.com/ArcletProject/nonebot-plugin-alconna
 Description-Content-Type: text/markdown
```

