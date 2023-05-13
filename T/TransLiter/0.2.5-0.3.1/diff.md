# Comparing `tmp/TransLiter-0.2.5.tar.gz` & `tmp/TransLiter-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "TransLiter-0.2.5.tar", last modified: Tue Apr 18 18:16:02 2023, max compression
+gzip compressed data, was "TransLiter-0.3.1.tar", last modified: Sat May 13 13:08:12 2023, max compression
```

## Comparing `TransLiter-0.2.5.tar` & `TransLiter-0.3.1.tar`

### file list

```diff
@@ -1,20 +1,22 @@
-drwxr-xr-x   0 hoyeolkim   (501) staff       (20)        0 2023-04-18 18:16:02.399041 TransLiter-0.2.5/
--rw-r--r--   0 hoyeolkim   (501) staff       (20)     1067 2023-04-07 00:09:21.000000 TransLiter-0.2.5/LICENSE
--rw-r--r--   0 hoyeolkim   (501) staff       (20)     4451 2023-04-18 18:16:02.398933 TransLiter-0.2.5/PKG-INFO
--rw-r--r--   0 hoyeolkim   (501) staff       (20)     4101 2023-04-18 17:41:29.000000 TransLiter-0.2.5/README.md
-drwxr-xr-x   0 hoyeolkim   (501) staff       (20)        0 2023-04-18 18:16:02.398116 TransLiter-0.2.5/TransLiter/
--rw-r--r--   0 hoyeolkim   (501) staff       (20)      110 2023-04-12 17:26:39.000000 TransLiter-0.2.5/TransLiter/__init__.py
--rw-r--r--   0 hoyeolkim   (501) staff       (20)     3414 2023-04-18 18:13:28.000000 TransLiter-0.2.5/TransLiter/jp_list.py
--rw-r--r--   0 hoyeolkim   (501) staff       (20)     1832 2023-04-18 17:11:04.000000 TransLiter-0.2.5/TransLiter/ko_jamo.py
--rw-r--r--   0 hoyeolkim   (501) staff       (20)      370 2023-04-12 17:31:03.000000 TransLiter-0.2.5/TransLiter/spacing.py
--rw-r--r--   0 hoyeolkim   (501) staff       (20)     1920 2023-04-18 18:14:28.000000 TransLiter-0.2.5/TransLiter/transliter_jp.py
--rw-r--r--   0 hoyeolkim   (501) staff       (20)     2990 2023-04-18 17:40:57.000000 TransLiter-0.2.5/TransLiter/transliter_ko.py
-drwxr-xr-x   0 hoyeolkim   (501) staff       (20)        0 2023-04-18 18:16:02.398775 TransLiter-0.2.5/TransLiter.egg-info/
--rw-r--r--   0 hoyeolkim   (501) staff       (20)     4451 2023-04-18 18:16:02.000000 TransLiter-0.2.5/TransLiter.egg-info/PKG-INFO
--rw-r--r--   0 hoyeolkim   (501) staff       (20)      373 2023-04-18 18:16:02.000000 TransLiter-0.2.5/TransLiter.egg-info/SOURCES.txt
--rw-r--r--   0 hoyeolkim   (501) staff       (20)        1 2023-04-18 18:16:02.000000 TransLiter-0.2.5/TransLiter.egg-info/dependency_links.txt
--rw-r--r--   0 hoyeolkim   (501) staff       (20)        1 2023-04-18 18:16:02.000000 TransLiter-0.2.5/TransLiter.egg-info/not-zip-safe
--rw-r--r--   0 hoyeolkim   (501) staff       (20)       16 2023-04-18 18:16:02.000000 TransLiter-0.2.5/TransLiter.egg-info/requires.txt
--rw-r--r--   0 hoyeolkim   (501) staff       (20)       11 2023-04-18 18:16:02.000000 TransLiter-0.2.5/TransLiter.egg-info/top_level.txt
--rw-r--r--   0 hoyeolkim   (501) staff       (20)       38 2023-04-18 18:16:02.399078 TransLiter-0.2.5/setup.cfg
--rw-r--r--   0 hoyeolkim   (501) staff       (20)      647 2023-04-18 17:37:02.000000 TransLiter-0.2.5/setup.py
+drwxr-xr-x   0 hoyeolkim   (501) staff       (20)        0 2023-05-13 13:08:12.819326 TransLiter-0.3.1/
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     1067 2023-05-13 04:20:03.000000 TransLiter-0.3.1/LICENSE
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     6637 2023-05-13 13:08:12.819194 TransLiter-0.3.1/PKG-INFO
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     6307 2023-05-13 04:20:03.000000 TransLiter-0.3.1/README.md
+drwxr-xr-x   0 hoyeolkim   (501) staff       (20)        0 2023-05-13 13:08:12.818211 TransLiter-0.3.1/TransLiter/
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)      155 2023-05-13 13:05:00.000000 TransLiter-0.3.1/TransLiter/__init__.py
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     1533 2023-05-13 04:20:03.000000 TransLiter-0.3.1/TransLiter/cyrillic_list.py
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     3414 2023-05-13 04:20:03.000000 TransLiter-0.3.1/TransLiter/jp_list.py
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     1832 2023-05-13 04:20:03.000000 TransLiter-0.3.1/TransLiter/ko_jamo.py
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)      370 2023-05-13 04:20:03.000000 TransLiter-0.3.1/TransLiter/spacing.py
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     2792 2023-05-13 13:07:36.000000 TransLiter-0.3.1/TransLiter/transliter_cyrillic.py
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     1920 2023-05-13 04:20:03.000000 TransLiter-0.3.1/TransLiter/transliter_jp.py
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     2990 2023-05-13 04:20:03.000000 TransLiter-0.3.1/TransLiter/transliter_ko.py
+drwxr-xr-x   0 hoyeolkim   (501) staff       (20)        0 2023-05-13 13:08:12.818996 TransLiter-0.3.1/TransLiter.egg-info/
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)     6637 2023-05-13 13:08:12.000000 TransLiter-0.3.1/TransLiter.egg-info/PKG-INFO
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)      435 2023-05-13 13:08:12.000000 TransLiter-0.3.1/TransLiter.egg-info/SOURCES.txt
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)        1 2023-05-13 13:08:12.000000 TransLiter-0.3.1/TransLiter.egg-info/dependency_links.txt
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)        1 2023-05-13 13:08:12.000000 TransLiter-0.3.1/TransLiter.egg-info/not-zip-safe
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)       16 2023-05-13 13:08:12.000000 TransLiter-0.3.1/TransLiter.egg-info/requires.txt
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)       11 2023-05-13 13:08:12.000000 TransLiter-0.3.1/TransLiter.egg-info/top_level.txt
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)       38 2023-05-13 13:08:12.819364 TransLiter-0.3.1/setup.cfg
+-rw-r--r--   0 hoyeolkim   (501) staff       (20)      647 2023-05-13 13:05:14.000000 TransLiter-0.3.1/setup.py
```

### Comparing `TransLiter-0.2.5/LICENSE` & `TransLiter-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `TransLiter-0.2.5/TransLiter/jp_list.py` & `TransLiter-0.3.1/TransLiter/jp_list.py`

 * *Files identical despite different names*

### Comparing `TransLiter-0.2.5/TransLiter/ko_jamo.py` & `TransLiter-0.3.1/TransLiter/ko_jamo.py`

 * *Files identical despite different names*

### Comparing `TransLiter-0.2.5/TransLiter/transliter_jp.py` & `TransLiter-0.3.1/TransLiter/transliter_jp.py`

 * *Files identical despite different names*

### Comparing `TransLiter-0.2.5/TransLiter/transliter_ko.py` & `TransLiter-0.3.1/TransLiter/transliter_ko.py`

 * *Files identical despite different names*

### Comparing `TransLiter-0.2.5/setup.py` & `TransLiter-0.3.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup
 
 with open("README.md", "r", encoding="utf-8") as f:
     long_description = f.read()
 
 setup(name='TransLiter',
     python_requires='>=3.6',
-    version='0.2.5',
+    version='0.3.1',
     url='https://github.com/elibooklover/TransLiter',
     license='MIT',
     author='Hoyeol Kim',
     author_email='elibooklover@gmail.com',
     description='TransLiter transliterates multilingual text into English.',
     packages=['TransLiter', ],
     long_description=long_description,
```

