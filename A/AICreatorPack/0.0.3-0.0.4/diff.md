# Comparing `tmp/AICreatorPack-0.0.3.tar.gz` & `tmp/AICreatorPack-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "AICreatorPack-0.0.3.tar", last modified: Sat May 13 08:32:40 2023, max compression
+gzip compressed data, was "AICreatorPack-0.0.4.tar", last modified: Sat May 13 08:38:14 2023, max compression
```

## Comparing `AICreatorPack-0.0.3.tar` & `AICreatorPack-0.0.4.tar`

### file list

```diff
@@ -1,26 +1,21 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 08:32:40.363621 AICreatorPack-0.0.3/
-drwxrwxrwx   0        0        0        0 2023-05-13 08:32:40.342375 AICreatorPack-0.0.3/AICreatorPack.egg-info/
--rw-rw-rw-   0        0        0      563 2023-05-13 08:32:40.000000 AICreatorPack-0.0.3/AICreatorPack.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      556 2023-05-13 08:32:40.000000 AICreatorPack-0.0.3/AICreatorPack.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 08:32:40.000000 AICreatorPack-0.0.3/AICreatorPack.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-05-13 08:32:40.000000 AICreatorPack-0.0.3/AICreatorPack.egg-info/requires.txt
--rw-rw-rw-   0        0        0       17 2023-05-13 08:32:40.000000 AICreatorPack-0.0.3/AICreatorPack.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-05-13 08:32:40.343894 AICreatorPack-0.0.3/AICreatorPackage/
--rw-rw-rw-   0        0        0      156 2023-05-12 13:45:59.000000 AICreatorPack-0.0.3/AICreatorPackage/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 08:32:40.358600 AICreatorPack-0.0.3/AICreatorPackage/functions/
--rw-rw-rw-   0        0        0      906 2023-05-13 08:07:16.000000 AICreatorPack-0.0.3/AICreatorPackage/functions/AICreatorPackage.py
--rw-rw-rw-   0        0        0        0 2022-04-25 10:59:44.000000 AICreatorPack-0.0.3/AICreatorPackage/functions/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 08:32:40.359597 AICreatorPack-0.0.3/AICreatorPackage/functions/ini/
--rw-rw-rw-   0        0        0        0 2023-05-13 08:10:15.000000 AICreatorPack-0.0.3/AICreatorPackage/functions/ini/ini.py
-drwxrwxrwx   0        0        0        0 2023-05-13 08:32:40.355075 AICreatorPack-0.0.3/AICreatorPackage.egg-info/
--rw-rw-rw-   0        0        0      380 2023-05-12 16:37:15.000000 AICreatorPack-0.0.3/AICreatorPackage.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 16:37:15.000000 AICreatorPack-0.0.3/AICreatorPackage.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-05-12 16:37:15.000000 AICreatorPack-0.0.3/AICreatorPackage.egg-info/requires.txt
--rw-rw-rw-   0        0        0       17 2023-05-12 16:37:15.000000 AICreatorPack-0.0.3/AICreatorPackage.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1078 2022-04-24 17:23:55.000000 AICreatorPack-0.0.3/LICENCE.txt
--rw-rw-rw-   0        0        0       25 2021-08-13 08:55:17.000000 AICreatorPack-0.0.3/MANIFEST.in
--rw-rw-rw-   0        0        0      563 2023-05-13 08:32:40.362111 AICreatorPack-0.0.3/PKG-INFO
--rw-rw-rw-   0        0        0       73 2023-05-12 13:45:34.000000 AICreatorPack-0.0.3/README.txt
--rw-rw-rw-   0        0        0        0 2022-04-24 17:21:54.000000 AICreatorPack-0.0.3/__init__.py
--rw-rw-rw-   0        0        0       42 2023-05-13 08:32:40.363621 AICreatorPack-0.0.3/setup.cfg
--rw-rw-rw-   0        0        0      679 2023-05-13 08:32:18.000000 AICreatorPack-0.0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 08:38:14.004252 AICreatorPack-0.0.4/
+drwxrwxrwx   0        0        0        0 2023-05-13 08:38:13.976147 AICreatorPack-0.0.4/AICreatorPack/
+-rw-rw-rw-   0        0        0      150 2023-05-13 08:37:03.000000 AICreatorPack-0.0.4/AICreatorPack/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 08:38:13.999736 AICreatorPack-0.0.4/AICreatorPack/functions/
+-rw-rw-rw-   0        0        0      906 2023-05-13 08:07:16.000000 AICreatorPack-0.0.4/AICreatorPack/functions/AICreatorPack.py
+-rw-rw-rw-   0        0        0        0 2022-04-25 10:59:44.000000 AICreatorPack-0.0.4/AICreatorPack/functions/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 08:38:14.000743 AICreatorPack-0.0.4/AICreatorPack/functions/ini/
+-rw-rw-rw-   0        0        0    52493 2023-05-13 08:36:07.000000 AICreatorPack-0.0.4/AICreatorPack/functions/ini/ini.py
+drwxrwxrwx   0        0        0        0 2023-05-13 08:38:13.995223 AICreatorPack-0.0.4/AICreatorPack.egg-info/
+-rw-rw-rw-   0        0        0      563 2023-05-13 08:38:13.000000 AICreatorPack-0.0.4/AICreatorPack.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      377 2023-05-13 08:38:13.000000 AICreatorPack-0.0.4/AICreatorPack.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 08:38:13.000000 AICreatorPack-0.0.4/AICreatorPack.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 08:38:13.000000 AICreatorPack-0.0.4/AICreatorPack.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-05-13 08:38:13.000000 AICreatorPack-0.0.4/AICreatorPack.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1078 2022-04-24 17:23:55.000000 AICreatorPack-0.0.4/LICENCE.txt
+-rw-rw-rw-   0        0        0       25 2021-08-13 08:55:17.000000 AICreatorPack-0.0.4/MANIFEST.in
+-rw-rw-rw-   0        0        0      563 2023-05-13 08:38:14.002743 AICreatorPack-0.0.4/PKG-INFO
+-rw-rw-rw-   0        0        0       73 2023-05-12 13:45:34.000000 AICreatorPack-0.0.4/README.txt
+-rw-rw-rw-   0        0        0        0 2022-04-24 17:21:54.000000 AICreatorPack-0.0.4/__init__.py
+-rw-rw-rw-   0        0        0       42 2023-05-13 08:38:14.004252 AICreatorPack-0.0.4/setup.cfg
+-rw-rw-rw-   0        0        0      679 2023-05-13 08:38:10.000000 AICreatorPack-0.0.4/setup.py
```

### Comparing `AICreatorPack-0.0.3/AICreatorPack.egg-info/PKG-INFO` & `AICreatorPack-0.0.4/AICreatorPack.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AICreatorPack
-Version: 0.0.3
+Version: 0.0.4
 Summary: AI Creator Package By - oren
 Home-page: 
 Author: oren
 Author-email: orennadle@gmail.com
 License: MIT
 Keywords: ai
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `AICreatorPack-0.0.3/AICreatorPackage/functions/AICreatorPackage.py` & `AICreatorPack-0.0.4/AICreatorPack/functions/AICreatorPack.py`

 * *Files identical despite different names*

### Comparing `AICreatorPack-0.0.3/LICENCE.txt` & `AICreatorPack-0.0.4/LICENCE.txt`

 * *Files identical despite different names*

### Comparing `AICreatorPack-0.0.3/PKG-INFO` & `AICreatorPack-0.0.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AICreatorPack
-Version: 0.0.3
+Version: 0.0.4
 Summary: AI Creator Package By - oren
 Home-page: 
 Author: oren
 Author-email: orennadle@gmail.com
 License: MIT
 Keywords: ai
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `AICreatorPack-0.0.3/setup.py` & `AICreatorPack-0.0.4/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     'Operating System :: Microsoft :: Windows :: Windows 10',
     'License :: OSI Approved :: MIT License',
     'Programming Language :: Python :: 3'
 ]
 
 setup(
     name='AICreatorPack',
-    version='0.0.3',
+    version='0.0.4',
     description='AI Creator Package By - oren',
     long_description=open('README.txt').read(),
     url='',
     author='oren',
     author_email='orennadle@gmail.com',
     license='MIT',
     classifiers=classifiers,
```

