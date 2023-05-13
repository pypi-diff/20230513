# Comparing `tmp/nonebot_plugin_watermarker-0.1.5.tar.gz` & `tmp/nonebot_plugin_watermarker-0.1.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_watermarker-0.1.5.tar", last modified: Sat May 13 13:22:41 2023, max compression
+gzip compressed data, was "nonebot_plugin_watermarker-0.1.5.1.tar", last modified: Sat May 13 13:43:23 2023, max compression
```

## Comparing `nonebot_plugin_watermarker-0.1.5.tar` & `nonebot_plugin_watermarker-0.1.5.1.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 13:22:41.456201 nonebot_plugin_watermarker-0.1.5/
--rw-rw-rw-   0        0        0     1087 2023-05-01 12:04:12.000000 nonebot_plugin_watermarker-0.1.5/LICENSE
--rw-rw-rw-   0        0        0     4000 2023-05-13 13:22:41.455202 nonebot_plugin_watermarker-0.1.5/PKG-INFO
--rw-rw-rw-   0        0        0     3644 2023-05-02 00:05:20.000000 nonebot_plugin_watermarker-0.1.5/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 13:22:41.443233 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker/
--rw-rw-rw-   0        0        0     2125 2023-05-13 13:15:02.000000 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker/__init__.py
--rw-rw-rw-   0        0        0      842 2023-05-01 09:25:17.000000 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker/config.py
--rw-rw-rw-   0        0        0     2365 2023-05-07 02:46:14.000000 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker/fuctions.py
-drwxrwxrwx   0        0        0        0 2023-05-13 13:22:41.453207 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker.egg-info/
--rw-rw-rw-   0        0        0     4000 2023-05-13 13:22:41.000000 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      390 2023-05-13 13:22:41.000000 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 13:22:41.000000 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       16 2023-05-13 13:22:41.000000 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker.egg-info/requires.txt
--rw-rw-rw-   0        0        0       27 2023-05-13 13:22:41.000000 nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 13:22:41.456201 nonebot_plugin_watermarker-0.1.5/setup.cfg
--rw-rw-rw-   0        0        0     4208 2023-05-13 13:22:21.000000 nonebot_plugin_watermarker-0.1.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:43:23.408734 nonebot_plugin_watermarker-0.1.5.1/
+-rw-rw-rw-   0        0        0     1087 2023-05-01 12:04:12.000000 nonebot_plugin_watermarker-0.1.5.1/LICENSE
+-rw-rw-rw-   0        0        0     4002 2023-05-13 13:43:23.403748 nonebot_plugin_watermarker-0.1.5.1/PKG-INFO
+-rw-rw-rw-   0        0        0     3644 2023-05-02 00:05:20.000000 nonebot_plugin_watermarker-0.1.5.1/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 13:43:23.375825 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker/
+-rw-rw-rw-   0        0        0     2125 2023-05-13 13:15:02.000000 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker/__init__.py
+-rw-rw-rw-   0        0        0      842 2023-05-01 09:25:17.000000 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker/config.py
+-rw-rw-rw-   0        0        0     2366 2023-05-13 13:40:22.000000 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker/fuctions.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:43:23.400756 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker.egg-info/
+-rw-rw-rw-   0        0        0     4002 2023-05-13 13:43:23.000000 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      390 2023-05-13 13:43:23.000000 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 13:43:23.000000 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       16 2023-05-13 13:43:23.000000 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       27 2023-05-13 13:43:23.000000 nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 13:43:23.408734 nonebot_plugin_watermarker-0.1.5.1/setup.cfg
+-rw-rw-rw-   0        0        0     4210 2023-05-13 13:43:18.000000 nonebot_plugin_watermarker-0.1.5.1/setup.py
```

### Comparing `nonebot_plugin_watermarker-0.1.5/LICENSE` & `nonebot_plugin_watermarker-0.1.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_watermarker-0.1.5/PKG-INFO` & `nonebot_plugin_watermarker-0.1.5.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot_plugin_watermarker
-Version: 0.1.5
+Version: 0.1.5.1
 Summary: 为nonebot机器人发送的图片加上水印
 Home-page: https://github.com/X-Skirt-X/nonebot-plugin-watermarker
 Author: XU
 Author-email: Woyerpa@outlook.com
 License: MIT License
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

#### html2text {}

```diff
@@ -1,12 +1,12 @@
-Metadata-Version: 2.1 Name: nonebot_plugin_watermarker Version: 0.1.5 Summary:
-ä¸ºnonebotæºå¨äººåéçå¾çå ä¸æ°´å° Home-page: https://github.com/X-
-Skirt-X/nonebot-plugin-watermarker Author: XU Author-email: Woyerpa@outlook.com
-License: MIT License Platform: UNKNOWN Description-Content-Type: text/markdown
-License-File: LICENSE
+Metadata-Version: 2.1 Name: nonebot_plugin_watermarker Version: 0.1.5.1
+Summary: ä¸ºnonebotæºå¨äººåéçå¾çå ä¸æ°´å° Home-page: https://
+github.com/X-Skirt-X/nonebot-plugin-watermarker Author: XU Author-email:
+Woyerpa@outlook.com License: MIT License Platform: UNKNOWN Description-Content-
+Type: text/markdown License-File: LICENSE
                             [PoweredByNonebotLogo]
                              [NoneBotPluginLogo]
                               [NoneBotPluginText]
 # nonebot-plugin-watermarker _â¨ ä¸ºä½ çbotååºçå¾çæ·»å æ°´å°! â¨_
                            [license] [pypi] [python]
  * [ðç®ä»](#ç®ä») * [ð¿ å®è£æ¹æ³](#å®è£æ¹æ³) *
 [âï¸æä»¶éç½®é¡¹](#æä»¶éç½®é¡¹) * [ðç®åå·²å®ç°çåè½]
```

### Comparing `nonebot_plugin_watermarker-0.1.5/README.md` & `nonebot_plugin_watermarker-0.1.5.1/README.md`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker/__init__.py` & `nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker/config.py` & `nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker/fuctions.py` & `nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker/fuctions.py`

 * *Files 0% similar despite different names*

```diff
@@ -18,15 +18,15 @@
     Returns:
         Union[Image.Image, None]: _description_
     """
     base64_pattern = r"base64://[a-zA-Z0-9+/]+"
     other_pattern = r"(?:http|https)://\S+"
     file_pattern = r"file:///\S+"
     image1 = None
-    breakpoint()
+    #breakpoint()
     if matcher := re.search(base64_pattern, string):
         string = matcher.group()
         string = string.replace("base64://", "")
         image_bytes = base64.b64decode(string)
         image_stream = io.BytesIO(image_bytes)
         image1 = Image.open(image_stream)
     elif matcher := re.search(other_pattern, string):
```

### Comparing `nonebot_plugin_watermarker-0.1.5/nonebot_plugin_watermarker.egg-info/PKG-INFO` & `nonebot_plugin_watermarker-0.1.5.1/nonebot_plugin_watermarker.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-watermarker
-Version: 0.1.5
+Version: 0.1.5.1
 Summary: 为nonebot机器人发送的图片加上水印
 Home-page: https://github.com/X-Skirt-X/nonebot-plugin-watermarker
 Author: XU
 Author-email: Woyerpa@outlook.com
 License: MIT License
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

#### html2text {}

```diff
@@ -1,12 +1,12 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-watermarker Version: 0.1.5 Summary:
-ä¸ºnonebotæºå¨äººåéçå¾çå ä¸æ°´å° Home-page: https://github.com/X-
-Skirt-X/nonebot-plugin-watermarker Author: XU Author-email: Woyerpa@outlook.com
-License: MIT License Platform: UNKNOWN Description-Content-Type: text/markdown
-License-File: LICENSE
+Metadata-Version: 2.1 Name: nonebot-plugin-watermarker Version: 0.1.5.1
+Summary: ä¸ºnonebotæºå¨äººåéçå¾çå ä¸æ°´å° Home-page: https://
+github.com/X-Skirt-X/nonebot-plugin-watermarker Author: XU Author-email:
+Woyerpa@outlook.com License: MIT License Platform: UNKNOWN Description-Content-
+Type: text/markdown License-File: LICENSE
                             [PoweredByNonebotLogo]
                              [NoneBotPluginLogo]
                               [NoneBotPluginText]
 # nonebot-plugin-watermarker _â¨ ä¸ºä½ çbotååºçå¾çæ·»å æ°´å°! â¨_
                            [license] [pypi] [python]
  * [ðç®ä»](#ç®ä») * [ð¿ å®è£æ¹æ³](#å®è£æ¹æ³) *
 [âï¸æä»¶éç½®é¡¹](#æä»¶éç½®é¡¹) * [ðç®åå·²å®ç°çåè½]
```

### Comparing `nonebot_plugin_watermarker-0.1.5/setup.py` & `nonebot_plugin_watermarker-0.1.5.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from setuptools import setup, find_packages
 
     
 setup(
     name='nonebot_plugin_watermarker',
 
-    version="0.1.5",
+    version="0.1.5.1",
     description=(
         '为nonebot机器人发送的图片加上水印'
 
     ),
     long_description="""<div align="center">
   <p><img src="https://user-images.githubusercontent.com/91937041/235443858-85949be1-08d6-4d7a-b132-b1aed71ab943.png" width="560" alt="PoweredByNonebotLogo"></p>
   <a href="https://v2.nonebot.dev/store"><img src="https://ghproxy.com/https://github.com/A-kirami/nonebot-plugin-template/blob/resources/nbp_logo.png" width="180" height="180" alt="NoneBotPluginLogo"></a>
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
 from setuptools import setup, find_packages setup
-( name='nonebot_plugin_watermarker', version="0.1.5", description=
+( name='nonebot_plugin_watermarker', version="0.1.5.1", description=
 ( 'ä¸ºnonebotæºå¨äººåéçå¾çå ä¸æ°´å°' ), long_description="""
                             [PoweredByNonebotLogo]
                              [NoneBotPluginLogo]
                               [NoneBotPluginText]
 # nonebot-plugin-watermarker _â¨ ä¸ºä½ çbotååºçå¾çæ·»å æ°´å°! â¨_
                            [license] [pypi] [python]
  * [ðç®ä»](#ç®ä») * [ð¿ å®è£æ¹æ³](#å®è£æ¹æ³) *
```

