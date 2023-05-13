# Comparing `tmp/hiyobot-0.1.8.tar.gz` & `tmp/hiyobot-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hiyobot-0.1.8.tar", last modified: Sat May 13 12:33:46 2023, max compression
+gzip compressed data, was "hiyobot-0.1.9.tar", last modified: Sat May 13 12:47:54 2023, max compression
```

## Comparing `hiyobot-0.1.8.tar` & `hiyobot-0.1.9.tar`

### file list

```diff
@@ -1,12 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:33:46.195529 hiyobot-0.1.8/
--rw-r--r--   0 runner    (1001) docker     (123)    18092 2023-05-13 12:33:35.000000 hiyobot-0.1.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 12:33:46.195529 hiyobot-0.1.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-05-13 12:33:35.000000 hiyobot-0.1.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:33:46.195529 hiyobot-0.1.8/hiyobot.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 12:33:46.000000 hiyobot-0.1.8/hiyobot.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      180 2023-05-13 12:33:46.000000 hiyobot-0.1.8/hiyobot.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:33:46.000000 hiyobot-0.1.8/hiyobot.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 12:33:46.000000 hiyobot-0.1.8/hiyobot.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:33:46.000000 hiyobot-0.1.8/hiyobot.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:33:46.195529 hiyobot-0.1.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-13 12:33:35.000000 hiyobot-0.1.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:47:54.920214 hiyobot-0.1.9/
+-rw-r--r--   0 runner    (1001) docker     (123)    18092 2023-05-13 12:47:41.000000 hiyobot-0.1.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 12:47:54.920214 hiyobot-0.1.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-05-13 12:47:41.000000 hiyobot-0.1.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:47:54.916214 hiyobot-0.1.9/hiyobot/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 12:47:41.000000 hiyobot-0.1.9/hiyobot/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:47:54.920214 hiyobot-0.1.9/hiyobot/hackchat/
+-rw-r--r--   0 runner    (1001) docker     (123)     8700 2023-05-13 12:47:41.000000 hiyobot-0.1.9/hiyobot/hackchat/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:47:54.920214 hiyobot-0.1.9/hiyobot/zhangchat/
+-rw-r--r--   0 runner    (1001) docker     (123)     8821 2023-05-13 12:47:41.000000 hiyobot-0.1.9/hiyobot/zhangchat/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:47:54.920214 hiyobot-0.1.9/hiyobot.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 12:47:54.000000 hiyobot-0.1.9/hiyobot.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-05-13 12:47:54.000000 hiyobot-0.1.9/hiyobot.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:47:54.000000 hiyobot-0.1.9/hiyobot.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 12:47:54.000000 hiyobot-0.1.9/hiyobot.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 12:47:54.000000 hiyobot-0.1.9/hiyobot.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:47:54.920214 hiyobot-0.1.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-13 12:47:41.000000 hiyobot-0.1.9/setup.py
```

### Comparing `hiyobot-0.1.8/LICENSE` & `hiyobot-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `hiyobot-0.1.8/PKG-INFO` & `hiyobot-0.1.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hiyobot
-Version: 0.1.8
+Version: 0.1.9
 Summary: A simple bot framework for Hack.chat.
 Home-page: https://github.com/Hiyoteam/hiyobot
 Author: MaggieLOL
 Author-email: tanhanzesnd@gmail.com
 License: GPL-2.0
 Keywords: bot hack.chat hack.chat-bot
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `hiyobot-0.1.8/README.md` & `hiyobot-0.1.9/README.md`

 * *Files identical despite different names*

### Comparing `hiyobot-0.1.8/hiyobot.egg-info/PKG-INFO` & `hiyobot-0.1.9/hiyobot.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hiyobot
-Version: 0.1.8
+Version: 0.1.9
 Summary: A simple bot framework for Hack.chat.
 Home-page: https://github.com/Hiyoteam/hiyobot
 Author: MaggieLOL
 Author-email: tanhanzesnd@gmail.com
 License: GPL-2.0
 Keywords: bot hack.chat hack.chat-bot
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `hiyobot-0.1.8/setup.py` & `hiyobot-0.1.9/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='hiyobot', # 你的项目名称
-    version="0.1.8", # 你的项目版本
+    version="0.1.9", # 你的项目版本
     description='A simple bot framework for Hack.chat.', # 你的项目简介
     long_description=open('README.md').read(), # 你的项目详细介绍，一般从README.md文件中读取
     long_description_content_type='text/markdown', # 你的项目详细介绍的格式，一般为markdown格式
     url='https://github.com/Hiyoteam/hiyobot', # 你的项目主页，一般为github仓库地址
     author='MaggieLOL', # 你的姓名或者团队名称
     author_email='tanhanzesnd@gmail.com', # 你的邮箱或者团队邮箱
     license='GPL-2.0', # 你的项目使用的许可证，一般为MIT或者其他开源许可证
```

