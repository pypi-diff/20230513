# Comparing `tmp/tybase-0.0.7.tar.gz` & `tmp/tybase-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tybase-0.0.7.tar", last modified: Sat May 13 04:52:31 2023, max compression
+gzip compressed data, was "tybase-0.0.8.tar", last modified: Sat May 13 05:29:49 2023, max compression
```

## Comparing `tybase-0.0.7.tar` & `tybase-0.0.8.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.028733 tybase-0.0.7/
--rw-r--r--   0 zhangte    (501) staff       (20)       28 2023-05-04 00:02:42.000000 tybase-0.0.7/MANIFEST.in
--rw-r--r--   0 zhangte    (501) staff       (20)      611 2023-05-13 04:52:31.028486 tybase-0.0.7/PKG-INFO
--rw-rw-rw-   0 zhangte    (501) staff       (20)      156 2023-05-08 08:46:36.000000 tybase-0.0.7/README.md
--rw-r--r--   0 zhangte    (501) staff       (20)       38 2023-05-13 04:52:31.028851 tybase-0.0.7/setup.cfg
--rw-rw-rw-   0 zhangte    (501) staff       (20)      947 2023-05-13 04:52:18.000000 tybase-0.0.7/setup.py
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.021388 tybase-0.0.7/tybase/
--rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-03 23:43:39.000000 tybase-0.0.7/tybase/__init__.py
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.024586 tybase-0.0.7/tybase/baidu/
--rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-04 01:26:22.000000 tybase-0.0.7/tybase/baidu/__init__.py
--rw-rw-rw-   0 zhangte    (501) staff       (20)     4364 2023-05-09 03:46:53.000000 tybase-0.0.7/tybase/baidu/kw_tool.py
--rw-r--r--   0 zhangte    (501) staff       (20)        6 2023-05-03 23:45:43.000000 tybase-0.0.7/tybase/datatest.txt
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.026893 tybase-0.0.7/tybase/dbtool/
--rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-13 02:41:28.000000 tybase-0.0.7/tybase/dbtool/__init__.py
--rw-r--r--   0 zhangte    (501) staff       (20)     4364 2023-05-13 04:50:10.000000 tybase-0.0.7/tybase/dbtool/data_import.py
--rw-r--r--   0 zhangte    (501) staff       (20)     2206 2023-05-13 03:56:34.000000 tybase-0.0.7/tybase/dbtool/mysql.py
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.027805 tybase-0.0.7/tybase/lc/
--rw-rw-rw-   0 zhangte    (501) staff       (20)        0 2023-05-08 08:41:12.000000 tybase-0.0.7/tybase/lc/__init__.py
--rw-rw-rw-   0 zhangte    (501) staff       (20)     2995 2023-05-08 10:37:41.000000 tybase-0.0.7/tybase/lc/eg1.py
--rw-r--r--   0 zhangte    (501) staff       (20)      205 2023-05-03 23:46:43.000000 tybase-0.0.7/tybase/tytest.py
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.023942 tybase-0.0.7/tybase.egg-info/
--rw-rw-rw-   0 zhangte    (501) staff       (20)      611 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/PKG-INFO
--rw-rw-rw-   0 zhangte    (501) staff       (20)      401 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/SOURCES.txt
--rw-r--r--   0 zhangte    (501) staff       (20)        1 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/dependency_links.txt
--rw-r--r--   0 zhangte    (501) staff       (20)       86 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/requires.txt
--rw-r--r--   0 zhangte    (501) staff       (20)        7 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/top_level.txt
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 05:29:49.827565 tybase-0.0.8/
+-rw-r--r--   0 zhangte    (501) staff       (20)       28 2023-05-04 00:02:42.000000 tybase-0.0.8/MANIFEST.in
+-rw-r--r--   0 zhangte    (501) staff       (20)      624 2023-05-13 05:29:49.827254 tybase-0.0.8/PKG-INFO
+-rw-rw-rw-   0 zhangte    (501) staff       (20)      156 2023-05-08 08:46:36.000000 tybase-0.0.8/README.md
+-rw-r--r--   0 zhangte    (501) staff       (20)       38 2023-05-13 05:29:49.827751 tybase-0.0.8/setup.cfg
+-rw-rw-rw-   0 zhangte    (501) staff       (20)      960 2023-05-13 05:29:43.000000 tybase-0.0.8/setup.py
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 05:29:49.821916 tybase-0.0.8/tybase/
+-rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-03 23:43:39.000000 tybase-0.0.8/tybase/__init__.py
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 05:29:49.824447 tybase-0.0.8/tybase/baidu/
+-rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-04 01:26:22.000000 tybase-0.0.8/tybase/baidu/__init__.py
+-rw-rw-rw-   0 zhangte    (501) staff       (20)     4364 2023-05-09 03:46:53.000000 tybase-0.0.8/tybase/baidu/kw_tool.py
+-rw-r--r--   0 zhangte    (501) staff       (20)        6 2023-05-03 23:45:43.000000 tybase-0.0.8/tybase/datatest.txt
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 05:29:49.825729 tybase-0.0.8/tybase/dbtool/
+-rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-13 02:41:28.000000 tybase-0.0.8/tybase/dbtool/__init__.py
+-rw-r--r--   0 zhangte    (501) staff       (20)     7368 2023-05-13 05:25:58.000000 tybase-0.0.8/tybase/dbtool/data_import.py
+-rw-r--r--   0 zhangte    (501) staff       (20)     2206 2023-05-13 03:56:34.000000 tybase-0.0.8/tybase/dbtool/mysql.py
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 05:29:49.826535 tybase-0.0.8/tybase/lc/
+-rw-rw-rw-   0 zhangte    (501) staff       (20)        0 2023-05-08 08:41:12.000000 tybase-0.0.8/tybase/lc/__init__.py
+-rw-rw-rw-   0 zhangte    (501) staff       (20)     2995 2023-05-08 10:37:41.000000 tybase-0.0.8/tybase/lc/eg1.py
+-rw-r--r--   0 zhangte    (501) staff       (20)      205 2023-05-03 23:46:43.000000 tybase-0.0.8/tybase/tytest.py
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 05:29:49.823938 tybase-0.0.8/tybase.egg-info/
+-rw-rw-rw-   0 zhangte    (501) staff       (20)      624 2023-05-13 05:29:49.000000 tybase-0.0.8/tybase.egg-info/PKG-INFO
+-rw-rw-rw-   0 zhangte    (501) staff       (20)      401 2023-05-13 05:29:49.000000 tybase-0.0.8/tybase.egg-info/SOURCES.txt
+-rw-r--r--   0 zhangte    (501) staff       (20)        1 2023-05-13 05:29:49.000000 tybase-0.0.8/tybase.egg-info/dependency_links.txt
+-rw-r--r--   0 zhangte    (501) staff       (20)       86 2023-05-13 05:29:49.000000 tybase-0.0.8/tybase.egg-info/requires.txt
+-rw-r--r--   0 zhangte    (501) staff       (20)        7 2023-05-13 05:29:49.000000 tybase-0.0.8/tybase.egg-info/top_level.txt
```

### Comparing `tybase-0.0.7/setup.py` & `tybase-0.0.8/setup.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from setuptools import setup, find_packages
 
 setup(
     name='tybase',
-    version='0.0.7',
+    version='0.0.8',
     include_package_data=True,
-    description='新增了data_import,和mysql的方法,方便数据进行导入',
+    description='又新增了批量文件导入的方法dbtool.data_import.DirectoryProcessor',
     long_description=open('README.md', 'r', encoding='utf-8').read(),
     long_description_content_type='text/markdown',  # 版本描述
     author='Tuya',
     author_email='353335447@qq.com',
     url='https://github.com/yourusername/your_package',
     packages=find_packages(),
     install_requires=[
```

### Comparing `tybase-0.0.7/tybase/baidu/kw_tool.py` & `tybase-0.0.8/tybase/baidu/kw_tool.py`

 * *Files identical despite different names*

### Comparing `tybase-0.0.7/tybase/dbtool/mysql.py` & `tybase-0.0.8/tybase/dbtool/mysql.py`

 * *Files identical despite different names*

### Comparing `tybase-0.0.7/tybase/lc/eg1.py` & `tybase-0.0.8/tybase/lc/eg1.py`

 * *Files identical despite different names*

