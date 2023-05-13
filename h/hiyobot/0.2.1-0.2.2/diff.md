# Comparing `tmp/hiyobot-0.2.1.tar.gz` & `tmp/hiyobot-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hiyobot-0.2.1.tar", last modified: Sat May 13 13:13:25 2023, max compression
+gzip compressed data, was "hiyobot-0.2.2.tar", last modified: Sat May 13 13:22:40 2023, max compression
```

## Comparing `hiyobot-0.2.1.tar` & `hiyobot-0.2.2.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:13:25.809784 hiyobot-0.2.1/
--rw-r--r--   0 runner    (1001) docker     (123)    18092 2023-05-13 13:13:14.000000 hiyobot-0.2.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 13:13:25.809784 hiyobot-0.2.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-05-13 13:13:14.000000 hiyobot-0.2.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:13:25.809784 hiyobot-0.2.1/hiyobot/
--rw-r--r--   0 runner    (1001) docker     (123)       58 2023-05-13 13:13:14.000000 hiyobot-0.2.1/hiyobot/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:13:25.809784 hiyobot-0.2.1/hiyobot/hackchat/
--rw-r--r--   0 runner    (1001) docker     (123)     8700 2023-05-13 13:13:14.000000 hiyobot-0.2.1/hiyobot/hackchat/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:13:25.809784 hiyobot-0.2.1/hiyobot/zhangchat/
--rw-r--r--   0 runner    (1001) docker     (123)     8830 2023-05-13 13:13:14.000000 hiyobot-0.2.1/hiyobot/zhangchat/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:13:25.809784 hiyobot-0.2.1/hiyobot.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 13:13:25.000000 hiyobot-0.2.1/hiyobot.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-13 13:13:25.000000 hiyobot-0.2.1/hiyobot.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:13:25.000000 hiyobot-0.2.1/hiyobot.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 13:13:25.000000 hiyobot-0.2.1/hiyobot.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 13:13:25.000000 hiyobot-0.2.1/hiyobot.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 13:13:25.809784 hiyobot-0.2.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-13 13:13:14.000000 hiyobot-0.2.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:22:40.843711 hiyobot-0.2.2/
+-rw-r--r--   0 runner    (1001) docker     (123)    18092 2023-05-13 13:22:21.000000 hiyobot-0.2.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 13:22:40.843711 hiyobot-0.2.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-05-13 13:22:21.000000 hiyobot-0.2.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:22:40.843711 hiyobot-0.2.2/hiyobot/
+-rw-r--r--   0 runner    (1001) docker     (123)       58 2023-05-13 13:22:21.000000 hiyobot-0.2.2/hiyobot/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:22:40.843711 hiyobot-0.2.2/hiyobot/hackchat/
+-rw-r--r--   0 runner    (1001) docker     (123)     8700 2023-05-13 13:22:21.000000 hiyobot-0.2.2/hiyobot/hackchat/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:22:40.843711 hiyobot-0.2.2/hiyobot/zhangchat/
+-rw-r--r--   0 runner    (1001) docker     (123)     8830 2023-05-13 13:22:21.000000 hiyobot-0.2.2/hiyobot/zhangchat/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:22:40.843711 hiyobot-0.2.2/hiyobot.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 13:22:40.000000 hiyobot-0.2.2/hiyobot.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-13 13:22:40.000000 hiyobot-0.2.2/hiyobot.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:22:40.000000 hiyobot-0.2.2/hiyobot.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 13:22:40.000000 hiyobot-0.2.2/hiyobot.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 13:22:40.000000 hiyobot-0.2.2/hiyobot.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 13:22:40.843711 hiyobot-0.2.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-13 13:22:21.000000 hiyobot-0.2.2/setup.py
```

### Comparing `hiyobot-0.2.1/LICENSE` & `hiyobot-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `hiyobot-0.2.1/PKG-INFO` & `hiyobot-0.2.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hiyobot
-Version: 0.2.1
+Version: 0.2.2
 Summary: A simple bot framework for Hack.chat.
 Home-page: https://github.com/Hiyoteam/hiyobot
 Author: MaggieLOL
 Author-email: tanhanzesnd@gmail.com
 License: GPL-2.0
 Keywords: bot hack.chat hack.chat-bot
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `hiyobot-0.2.1/README.md` & `hiyobot-0.2.2/README.md`

 * *Files identical despite different names*

### Comparing `hiyobot-0.2.1/hiyobot/hackchat/__init__.py` & `hiyobot-0.2.2/hiyobot/hackchat/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import websocket,ssl,json,threading,uuid,time,logging,re,traceback
 from functools import wraps
-HIYOBOT_VERSION=(0,2,1)
+HIYOBOT_VERSION=(0,2,2)
 MAX_RECV_LOG_LIMIT=100 #0 for no limit
 class Bot:
     """
     Simple Hack.chat bot class.
     """
     def __init__(self,channel,nick,password=None,joinoncreate=True) -> None:
         """
```

### Comparing `hiyobot-0.2.1/hiyobot/zhangchat/__init__.py` & `hiyobot-0.2.2/hiyobot/zhangchat/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import websocket,ssl,json,threading,uuid,time,logging,re,traceback
 from functools import wraps
-HIYOBOT_VERSION=(0,2,1)
+HIYOBOT_VERSION=(0,2,2)
 MAX_RECV_LOG_LIMIT=100 #0 for no limit
 class Bot:
     """
     Simple Hack.chat bot class.
     """
     def __init__(self,channel,nick,password=None,joinoncreate=True) -> None:
         """
@@ -28,17 +28,17 @@
     def on(self,matcher):
         """
         Add a new event.
         """
         def decorate(func):
             @wraps(func)
             def wrapper(session, data,*args, **kwargs):
-                if matcher.match_all(data):
+                if matcher.match_all(data.__dict__):
                     logging.debug(f"Matched! Function={func} Matcher={matcher}")
-                    return func(session=session, data=data.__dict__, *args, **kwargs)
+                    return func(session=session, data=data, *args, **kwargs)
                 else:
                     return None
             self.events.append(wrapper)
             return wrapper
         return decorate
     def _pingThread(self):
         while 1:
```

### Comparing `hiyobot-0.2.1/hiyobot.egg-info/PKG-INFO` & `hiyobot-0.2.2/hiyobot.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hiyobot
-Version: 0.2.1
+Version: 0.2.2
 Summary: A simple bot framework for Hack.chat.
 Home-page: https://github.com/Hiyoteam/hiyobot
 Author: MaggieLOL
 Author-email: tanhanzesnd@gmail.com
 License: GPL-2.0
 Keywords: bot hack.chat hack.chat-bot
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `hiyobot-0.2.1/setup.py` & `hiyobot-0.2.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='hiyobot', # 你的项目名称
-    version="0.2.1", # 你的项目版本
+    version="0.2.2", # 你的项目版本
     description='A simple bot framework for Hack.chat.', # 你的项目简介
     long_description=open('README.md').read(), # 你的项目详细介绍，一般从README.md文件中读取
     long_description_content_type='text/markdown', # 你的项目详细介绍的格式，一般为markdown格式
     url='https://github.com/Hiyoteam/hiyobot', # 你的项目主页，一般为github仓库地址
     author='MaggieLOL', # 你的姓名或者团队名称
     author_email='tanhanzesnd@gmail.com', # 你的邮箱或者团队邮箱
     license='GPL-2.0', # 你的项目使用的许可证，一般为MIT或者其他开源许可证
```

