# Comparing `tmp/nonebot_plugin_hoshino_sign-2.0.1.tar.gz` & `tmp/nonebot_plugin_hoshino_sign-2.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_hoshino_sign-2.0.1.tar", last modified: Sat May 13 14:02:14 2023, max compression
+gzip compressed data, was "nonebot_plugin_hoshino_sign-2.0.2.tar", last modified: Sat May 13 14:10:28 2023, max compression
```

## Comparing `nonebot_plugin_hoshino_sign-2.0.1.tar` & `nonebot_plugin_hoshino_sign-2.0.2.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:02:14.061360 nonebot_plugin_hoshino_sign-2.0.1/
--rw-rw-rw-   0        0        0    35184 2023-04-22 03:34:29.000000 nonebot_plugin_hoshino_sign-2.0.1/LICENSE
--rw-rw-rw-   0        0        0     4065 2023-05-13 14:02:14.061360 nonebot_plugin_hoshino_sign-2.0.1/PKG-INFO
--rw-rw-rw-   0        0        0     3335 2023-05-13 13:49:17.000000 nonebot_plugin_hoshino_sign-2.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 14:02:14.054922 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/
--rw-rw-rw-   0        0        0     6636 2023-05-13 11:44:09.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/__init__.py
--rw-rw-rw-   0        0        0     1750 2023-05-12 23:48:32.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/base.py
--rw-rw-rw-   0        0        0     1291 2023-05-12 23:48:32.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/text.py
--rw-rw-rw-   0        0        0     3160 2023-05-13 05:05:22.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:02:14.060361 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign.egg-info/
--rw-rw-rw-   0        0        0     4065 2023-05-13 14:02:13.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      429 2023-05-13 14:02:13.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:02:13.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       85 2023-05-13 14:02:13.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign.egg-info/requires.txt
--rw-rw-rw-   0        0        0       28 2023-05-13 14:02:13.000000 nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 14:02:14.062360 nonebot_plugin_hoshino_sign-2.0.1/setup.cfg
--rw-rw-rw-   0        0        0     4065 2023-05-13 14:02:04.000000 nonebot_plugin_hoshino_sign-2.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:10:28.314469 nonebot_plugin_hoshino_sign-2.0.2/
+-rw-rw-rw-   0        0        0    35184 2023-04-22 03:34:29.000000 nonebot_plugin_hoshino_sign-2.0.2/LICENSE
+-rw-rw-rw-   0        0        0     4065 2023-05-13 14:10:28.314469 nonebot_plugin_hoshino_sign-2.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0     3335 2023-05-13 13:49:17.000000 nonebot_plugin_hoshino_sign-2.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 14:10:28.299384 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/
+-rw-rw-rw-   0        0        0     6636 2023-05-13 11:44:09.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/__init__.py
+-rw-rw-rw-   0        0        0     1750 2023-05-12 23:48:32.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/base.py
+-rw-rw-rw-   0        0        0     1291 2023-05-12 23:48:32.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/text.py
+-rw-rw-rw-   0        0        0     3160 2023-05-13 05:05:22.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:10:28.303384 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign.egg-info/
+-rw-rw-rw-   0        0        0     4065 2023-05-13 14:10:28.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      429 2023-05-13 14:10:28.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:10:28.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       77 2023-05-13 14:10:28.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       28 2023-05-13 14:10:28.000000 nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:10:28.315475 nonebot_plugin_hoshino_sign-2.0.2/setup.cfg
+-rw-rw-rw-   0        0        0     4054 2023-05-13 14:10:10.000000 nonebot_plugin_hoshino_sign-2.0.2/setup.py
```

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/LICENSE` & `nonebot_plugin_hoshino_sign-2.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/PKG-INFO` & `nonebot_plugin_hoshino_sign-2.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot_plugin_hoshino_sign
-Version: 2.0.1
+Version: 2.0.2
 Summary: 一个从 hoshino 搬过来的 nonebot2 插件
 Home-page: https://github.com/zhulinyv/NJS/tree/Bot/src/plugins/sign_in
 Author: (๑•小丫头片子•๑)
 Author-email: zhulinyv2005@outlook.com
 License: MIT
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: nonebot_plugin_hoshino_sign Version: 2.0.1 Summary:
+Metadata-Version: 2.1 Name: nonebot_plugin_hoshino_sign Version: 2.0.2 Summary:
 ä¸ä¸ªä» hoshino æ¬è¿æ¥ç nonebot2 æä»¶ Home-page: https://github.com/
 zhulinyv/NJS/tree/Bot/src/plugins/sign_in Author: (à¹â¢å°ä¸«å¤´çå­â¢à¹)
 Author-email: zhulinyv2005@outlook.com License: MIT Classifier: License :: OSI
 Approved :: MIT License Classifier: Programming Language :: Python Classifier:
 Programming Language :: Python :: 3 Classifier: Programming Language :: Python
 :: 3.6 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy Requires-
```

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/README.md` & `nonebot_plugin_hoshino_sign-2.0.2/README.md`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/__init__.py` & `nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/base.py` & `nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/base.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/text.py` & `nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/text.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign/utils.py` & `nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign/utils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/nonebot_plugin_hoshino_sign.egg-info/PKG-INFO` & `nonebot_plugin_hoshino_sign-2.0.2/nonebot_plugin_hoshino_sign.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-hoshino-sign
-Version: 2.0.1
+Version: 2.0.2
 Summary: 一个从 hoshino 搬过来的 nonebot2 插件
 Home-page: https://github.com/zhulinyv/NJS/tree/Bot/src/plugins/sign_in
 Author: (๑•小丫头片子•๑)
 Author-email: zhulinyv2005@outlook.com
 License: MIT
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-hoshino-sign Version: 2.0.1 Summary:
+Metadata-Version: 2.1 Name: nonebot-plugin-hoshino-sign Version: 2.0.2 Summary:
 ä¸ä¸ªä» hoshino æ¬è¿æ¥ç nonebot2 æä»¶ Home-page: https://github.com/
 zhulinyv/NJS/tree/Bot/src/plugins/sign_in Author: (à¹â¢å°ä¸«å¤´çå­â¢à¹)
 Author-email: zhulinyv2005@outlook.com License: MIT Classifier: License :: OSI
 Approved :: MIT License Classifier: Programming Language :: Python Classifier:
 Programming Language :: Python :: 3 Classifier: Programming Language :: Python
 :: 3.6 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy Requires-
```

### Comparing `nonebot_plugin_hoshino_sign-2.0.1/setup.py` & `nonebot_plugin_hoshino_sign-2.0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -14,19 +14,19 @@
 # Package meta-data.
 NAME = 'nonebot_plugin_hoshino_sign'
 DESCRIPTION = '一个从 hoshino 搬过来的 nonebot2 插件'
 URL = 'https://github.com/zhulinyv/NJS/tree/Bot/src/plugins/sign_in'
 EMAIL = 'zhulinyv2005@outlook.com'
 AUTHOR = '(๑•小丫头片子•๑)'
 REQUIRES_PYTHON = '>=3.6.0'
-VERSION = '2.0.1'
+VERSION = '2.0.2'
 
 # What packages are required for this module to be executed?
 REQUIRED = [
-    'nonebot2', 'nonebot-adapter-onebot', 'nonebot_plugin_guild_patch', 'httpx', 'sqlite3', 'pytz', 'pillow'
+    'nonebot2', 'nonebot-adapter-onebot', 'nonebot_plugin_guild_patch', 'httpx', 'pytz', 'pillow'
 ]
 
 # What packages are optional?
 EXTRAS = {
     # 'fancy feature': ['django'],
 }
```

