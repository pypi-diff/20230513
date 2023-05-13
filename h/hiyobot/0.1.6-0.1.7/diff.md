# Comparing `tmp/hiyobot-0.1.6.tar.gz` & `tmp/hiyobot-0.1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hiyobot-0.1.6.tar", last modified: Sat May 13 12:03:12 2023, max compression
+gzip compressed data, was "hiyobot-0.1.7.tar", last modified: Sat May 13 12:23:27 2023, max compression
```

## Comparing `hiyobot-0.1.6.tar` & `hiyobot-0.1.7.tar`

### file list

```diff
@@ -1,14 +1,12 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:03:12.873775 hiyobot-0.1.6/
--rw-r--r--   0 runner    (1001) docker     (123)    18092 2023-05-13 12:02:53.000000 hiyobot-0.1.6/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     3302 2023-05-13 12:03:12.873775 hiyobot-0.1.6/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2725 2023-05-13 12:02:53.000000 hiyobot-0.1.6/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:03:12.869775 hiyobot-0.1.6/hiyobot/
--rw-r--r--   0 runner    (1001) docker     (123)     8662 2023-05-13 12:02:53.000000 hiyobot-0.1.6/hiyobot/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:03:12.873775 hiyobot-0.1.6/hiyobot.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3302 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      200 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 12:03:12.000000 hiyobot-0.1.6/hiyobot.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:03:12.873775 hiyobot-0.1.6/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-13 12:02:53.000000 hiyobot-0.1.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:23:27.760845 hiyobot-0.1.7/
+-rw-r--r--   0 runner    (1001) docker     (123)    18092 2023-05-13 12:23:12.000000 hiyobot-0.1.7/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 12:23:27.756845 hiyobot-0.1.7/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-05-13 12:23:12.000000 hiyobot-0.1.7/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:23:27.756845 hiyobot-0.1.7/hiyobot.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 12:23:27.000000 hiyobot-0.1.7/hiyobot.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      180 2023-05-13 12:23:27.000000 hiyobot-0.1.7/hiyobot.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:23:27.000000 hiyobot-0.1.7/hiyobot.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 12:23:27.000000 hiyobot-0.1.7/hiyobot.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:23:27.000000 hiyobot-0.1.7/hiyobot.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:23:27.760845 hiyobot-0.1.7/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-13 12:23:12.000000 hiyobot-0.1.7/setup.py
```

### Comparing `hiyobot-0.1.6/LICENSE` & `hiyobot-0.1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `hiyobot-0.1.6/setup.py` & `hiyobot-0.1.7/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='hiyobot', # 你的项目名称
-    version="0.1.6", # 你的项目版本
+    version="0.1.7", # 你的项目版本
     description='A simple bot framework for Hack.chat.', # 你的项目简介
     long_description=open('README.md').read(), # 你的项目详细介绍，一般从README.md文件中读取
     long_description_content_type='text/markdown', # 你的项目详细介绍的格式，一般为markdown格式
     url='https://github.com/Hiyoteam/hiyobot', # 你的项目主页，一般为github仓库地址
     author='MaggieLOL', # 你的姓名或者团队名称
     author_email='tanhanzesnd@gmail.com', # 你的邮箱或者团队邮箱
     license='GPL-2.0', # 你的项目使用的许可证，一般为MIT或者其他开源许可证
```

