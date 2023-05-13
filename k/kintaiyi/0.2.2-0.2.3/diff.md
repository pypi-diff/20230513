# Comparing `tmp/kintaiyi-0.2.2.tar.gz` & `tmp/kintaiyi-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "kintaiyi-0.2.2.tar", last modified: Fri Sep 16 16:24:48 2022, max compression
+gzip compressed data, was "kintaiyi-0.2.3.tar", last modified: Sat May 13 03:51:48 2023, max compression
```

## Comparing `kintaiyi-0.2.2.tar` & `kintaiyi-0.2.3.tar`

### file list

```diff
@@ -1,13 +1,16 @@
-drwxrwxrwx   0        0        0        0 2022-09-16 16:24:48.856617 kintaiyi-0.2.2/
--rw-rw-rw-   0        0        0     4684 2022-09-16 16:24:48.854615 kintaiyi-0.2.2/PKG-INFO
--rw-rw-rw-   0        0        0     4144 2022-09-16 16:12:12.000000 kintaiyi-0.2.2/README.md
-drwxrwxrwx   0        0        0        0 2022-09-16 16:24:48.794827 kintaiyi-0.2.2/kintaiyi/
--rw-rw-rw-   0        0        0        3 2019-08-16 07:28:34.000000 kintaiyi-0.2.2/kintaiyi/__init__.py
--rw-rw-rw-   0        0        0    35535 2022-09-13 13:52:38.000000 kintaiyi-0.2.2/kintaiyi/kintaiyi.py
-drwxrwxrwx   0        0        0        0 2022-09-16 16:24:48.848620 kintaiyi-0.2.2/kintaiyi.egg-info/
--rw-rw-rw-   0        0        0     4684 2022-09-16 16:24:46.000000 kintaiyi-0.2.2/kintaiyi.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      188 2022-09-16 16:24:48.000000 kintaiyi-0.2.2/kintaiyi.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-09-16 16:24:46.000000 kintaiyi-0.2.2/kintaiyi.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2022-09-16 16:24:46.000000 kintaiyi-0.2.2/kintaiyi.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2022-09-16 16:24:48.856617 kintaiyi-0.2.2/setup.cfg
--rw-rw-rw-   0        0        0      828 2022-09-16 16:24:23.000000 kintaiyi-0.2.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:48.546819 kintaiyi-0.2.3/
+-rw-rw-rw-   0        0        0     7407 2023-05-13 03:51:48.543820 kintaiyi-0.2.3/PKG-INFO
+-rw-rw-rw-   0        0        0     6924 2023-05-13 03:32:41.000000 kintaiyi-0.2.3/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:48.427825 kintaiyi-0.2.3/kintaiyi/
+-rw-rw-rw-   0        0        0        3 2019-08-16 07:28:34.000000 kintaiyi-0.2.3/kintaiyi/__init__.py
+-rw-rw-rw-   0        0        0    20552 2023-05-13 03:21:11.000000 kintaiyi-0.2.3/kintaiyi/config.py
+-rw-rw-rw-   0        0        0     3741 2023-05-13 03:07:53.000000 kintaiyi-0.2.3/kintaiyi/jieqi.py
+-rw-rw-rw-   0        0        0    35077 2023-05-13 03:32:19.000000 kintaiyi-0.2.3/kintaiyi/kintaiyi.py
+-rw-rw-rw-   0        0        0     3745 2023-05-13 03:07:53.000000 kintaiyi-0.2.3/kintaiyi/taiyidict.py
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:48.535824 kintaiyi-0.2.3/kintaiyi.egg-info/
+-rw-rw-rw-   0        0        0     7407 2023-05-13 03:51:45.000000 kintaiyi-0.2.3/kintaiyi.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      247 2023-05-13 03:51:47.000000 kintaiyi-0.2.3/kintaiyi.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 03:51:45.000000 kintaiyi-0.2.3/kintaiyi.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 03:51:45.000000 kintaiyi-0.2.3/kintaiyi.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 03:51:48.547817 kintaiyi-0.2.3/setup.cfg
+-rw-rw-rw-   0        0        0      818 2023-05-13 03:48:00.000000 kintaiyi-0.2.3/setup.py
```

### Comparing `kintaiyi-0.2.2/setup.py` & `kintaiyi-0.2.3/setup.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 import setuptools 
 
 with open("README.md", "r", encoding='utf-8') as fh:
     long_description = fh.read()
    
 setuptools.setup(
     name="kintaiyi",
-    version="0.2.2",
+    version="0.2.3",
     author="Ken Tang",
     author_email="kinyeah@gmail.com",
     install_requires=[            
       ],
-	description="Taiyi(太乙) is one of the three greatest Chinese Divination systems (三式) ever. This package mainy includes hour-based Taiyi divination system.",
+	description="Taiyi(太乙) is one of the three greatest Chinese Divination systems (三式) ever. ",
 	long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/kentang2017/kintaiyi",
 	packages=setuptools.find_packages(),
-	package_data = {},
+	package_data = {'kintaiyi': ['config.py', 'jieqi.py', 'taiyidict.py']},
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
     ],
 )
```

