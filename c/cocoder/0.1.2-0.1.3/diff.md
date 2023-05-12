# Comparing `tmp/cocoder-0.1.2.tar.gz` & `tmp/cocoder-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cocoder-0.1.2.tar", last modified: Fri May 12 22:55:51 2023, max compression
+gzip compressed data, was "cocoder-0.1.3.tar", last modified: Fri May 12 23:02:12 2023, max compression
```

## Comparing `cocoder-0.1.2.tar` & `cocoder-0.1.3.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.884309 cocoder-0.1.2/
--rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.2/LICENSE
--rw-rw-rw-   0        0        0     1018 2023-05-12 22:55:51.882835 cocoder-0.1.2/PKG-INFO
--rw-rw-rw-   0        0        0      121 2023-05-12 15:23:47.000000 cocoder-0.1.2/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.836074 cocoder-0.1.2/cocoder/
--rw-rw-rw-   0        0        0      504 2023-05-12 22:53:33.000000 cocoder-0.1.2/cocoder/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.861317 cocoder-0.1.2/cocoder/chatbase/
--rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.2/cocoder/chatbase/__init__.py
--rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.2/cocoder/chatbase/bard_receiver.py
--rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.2/cocoder/chatbase/openai_receiver.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.872136 cocoder-0.1.2/cocoder/ipython/
--rw-rw-rw-   0        0        0      554 2023-05-12 22:53:43.000000 cocoder-0.1.2/cocoder/ipython/__init__.py
--rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.2/cocoder/ipython/core.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.881764 cocoder-0.1.2/cocoder/python/
--rw-rw-rw-   0        0        0      487 2023-05-12 22:53:46.000000 cocoder-0.1.2/cocoder/python/__init__.py
--rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.2/cocoder/python/core.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.853773 cocoder-0.1.2/cocoder.egg-info/
--rw-rw-rw-   0        0        0     1018 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      435 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       15 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 22:55:51.885317 cocoder-0.1.2/setup.cfg
--rw-rw-rw-   0        0        0     1775 2023-05-12 22:53:40.000000 cocoder-0.1.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.431957 cocoder-0.1.3/
+-rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.3/LICENSE
+-rw-rw-rw-   0        0        0     1018 2023-05-12 23:02:12.429960 cocoder-0.1.3/PKG-INFO
+-rw-rw-rw-   0        0        0      121 2023-05-12 15:23:47.000000 cocoder-0.1.3/README.md
+drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.378511 cocoder-0.1.3/cocoder/
+-rw-rw-rw-   0        0        0      504 2023-05-12 23:01:04.000000 cocoder-0.1.3/cocoder/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.405386 cocoder-0.1.3/cocoder/chatbase/
+-rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.3/cocoder/chatbase/__init__.py
+-rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.3/cocoder/chatbase/bard_receiver.py
+-rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.3/cocoder/chatbase/openai_receiver.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.417464 cocoder-0.1.3/cocoder/ipython/
+-rw-rw-rw-   0        0        0      583 2023-05-12 23:01:00.000000 cocoder-0.1.3/cocoder/ipython/__init__.py
+-rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.3/cocoder/ipython/core.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.427630 cocoder-0.1.3/cocoder/python/
+-rw-rw-rw-   0        0        0      487 2023-05-12 23:01:56.000000 cocoder-0.1.3/cocoder/python/__init__.py
+-rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.3/cocoder/python/core.py
+drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.398562 cocoder-0.1.3/cocoder.egg-info/
+-rw-rw-rw-   0        0        0     1018 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      435 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       15 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-12 23:02:12.431957 cocoder-0.1.3/setup.cfg
+-rw-rw-rw-   0        0        0     1775 2023-05-12 23:01:59.000000 cocoder-0.1.3/setup.py
```

### Comparing `cocoder-0.1.2/LICENSE` & `cocoder-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.2/PKG-INFO` & `cocoder-0.1.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cocoder
-Version: 0.1.2
+Version: 0.1.3
 Home-page: https://github.com/dsdanielpark/Co-Coder
 Author: daniel park
 Author-email: parkminwoo1991@gmail.com
 Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Natural Language :: English
```

### Comparing `cocoder-0.1.2/cocoder/chatbase/bard_receiver.py` & `cocoder-0.1.3/cocoder/chatbase/bard_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.2/cocoder/chatbase/openai_receiver.py` & `cocoder-0.1.3/cocoder/chatbase/openai_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.2/cocoder/ipython/__init__.py` & `cocoder-0.1.3/cocoder/ipython/__init__.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,12 +1,15 @@
 # -*- coding: utf-8 -*-
 # Copyright 2023 parkminwoo
 from cocoder.ipython.core import ExceptIpyCocoder
 from cocoder.chatbase.bard_receiver import receive_bard_advice
 from cocoder.chatbase.openai_receiver import receive_openai_advice
 from cocoder.chatbase.openai_receiver import get_resp_openai_advice
 
-get_ipython().set_custom_exc((Exception,), ExceptIpyCocoder)
+try:
+    get_ipython().set_custom_exc((Exception,), ExceptIpyCocoder)
+except:
+    pass
 
-__version__ = "0.1.2"
+__version__ = "0.1.3"
 __author__ = "daniel park <parkminwoo1991@gmail.com>"
 __all__ = ["ExceptIpyCocoder", "receive_bard_advice", "receive_openai_advice", "get_resp_openai_advice"]
```

### Comparing `cocoder-0.1.2/cocoder/ipython/core.py` & `cocoder-0.1.3/cocoder/ipython/core.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.2/cocoder/python/core.py` & `cocoder-0.1.3/cocoder/python/core.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.2/cocoder.egg-info/PKG-INFO` & `cocoder-0.1.3/cocoder.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cocoder
-Version: 0.1.2
+Version: 0.1.3
 Home-page: https://github.com/dsdanielpark/Co-Coder
 Author: daniel park
 Author-email: parkminwoo1991@gmail.com
 Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Natural Language :: English
```

### Comparing `cocoder-0.1.2/setup.py` & `cocoder-0.1.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 
 
 version = get_version()
 
 
 setup(
     name="cocoder",
-    version="0.1.2",
+    version="0.1.3",
     author="daniel park",
     author_email="parkminwoo1991@gmail.com",
     description="",
     long_description=get_long_description(),
     long_description_content_type="text/markdown",
     url="https://github.com/dsdanielpark/Co-Coder",
     packages=find_packages(exclude=[]),
```

