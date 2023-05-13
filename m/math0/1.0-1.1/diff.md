# Comparing `tmp/math0-1.0.tar.gz` & `tmp/math0-1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "math0-1.0.tar", last modified: Fri May 12 11:08:11 2023, max compression
+gzip compressed data, was "math0-1.1.tar", last modified: Sat May 13 01:45:09 2023, max compression
```

## Comparing `math0-1.0.tar` & `math0-1.1.tar`

### file list

```diff
@@ -1,9 +1,9 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 11:08:11.339847 math0-1.0/
--rw-rw-rw-   0        0        0      353 2023-05-12 11:08:11.338883 math0-1.0/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-12 11:08:11.336846 math0-1.0/math0.egg-info/
--rw-rw-rw-   0        0        0      353 2023-05-12 11:08:11.000000 math0-1.0/math0.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      124 2023-05-12 11:08:11.000000 math0-1.0/math0.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 11:08:11.000000 math0-1.0/math0.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 11:08:11.000000 math0-1.0/math0.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 11:08:11.339847 math0-1.0/setup.cfg
--rw-rw-rw-   0        0        0      977 2023-05-12 11:07:38.000000 math0-1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 01:45:09.416440 math0-1.1/
+-rw-rw-rw-   0        0        0      397 2023-05-13 01:45:09.416440 math0-1.1/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 01:45:09.416440 math0-1.1/math0.egg-info/
+-rw-rw-rw-   0        0        0      397 2023-05-13 01:45:09.000000 math0-1.1/math0.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      124 2023-05-13 01:45:09.000000 math0-1.1/math0.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 01:45:09.000000 math0-1.1/math0.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 01:45:09.000000 math0-1.1/math0.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 01:45:09.416440 math0-1.1/setup.cfg
+-rw-rw-rw-   0        0        0     1021 2023-05-13 01:44:56.000000 math0-1.1/setup.py
```

### Comparing `math0-1.0/setup.py` & `math0-1.1/setup.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import setuptools
 
 setuptools.setup(
     # 项目的名称
     name="math0",
     # 项目的版本
-    version="1.0",
+    version="1.1",
     # 项目的作者
     author="高乐喆",
     # 作者的邮箱
     author_email="gaolezhe@outlook.com",
     # 项目描述
     description="数学函数库",
     # 项目的长描述
@@ -19,11 +19,11 @@
     # 项目主页
     url="",
     # 项目中包含的子包，find_packages() 是自动发现根目录中的所有的子包。
     packages=setuptools.find_packages(),
     # 其他信息，这里写了使用 Python3，MIT License许可证，不依赖操作系统。
     classifiers=[
         "Programming Language :: Python :: 3",
-        "License :: OSI Approved :: MIT License",
+        "License :: OSI Approved :: GNU Affero General Public License v3 or later (AGPLv3+)",
         "Operating System :: OS Independent",
     ],
 )
```

