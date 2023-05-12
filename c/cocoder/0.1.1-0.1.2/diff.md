# Comparing `tmp/cocoder-0.1.1.tar.gz` & `tmp/cocoder-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cocoder-0.1.1.tar", last modified: Fri May 12 22:41:10 2023, max compression
+gzip compressed data, was "cocoder-0.1.2.tar", last modified: Fri May 12 22:55:51 2023, max compression
```

## Comparing `cocoder-0.1.1.tar` & `cocoder-0.1.2.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.258509 cocoder-0.1.1/
--rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.1/LICENSE
--rw-rw-rw-   0        0        0     1018 2023-05-12 22:41:10.257510 cocoder-0.1.1/PKG-INFO
--rw-rw-rw-   0        0        0      121 2023-05-12 15:23:47.000000 cocoder-0.1.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.205744 cocoder-0.1.1/cocoder/
--rw-rw-rw-   0        0        0      504 2023-05-12 22:40:21.000000 cocoder-0.1.1/cocoder/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.232977 cocoder-0.1.1/cocoder/chatbase/
--rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.1/cocoder/chatbase/__init__.py
--rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.1/cocoder/chatbase/bard_receiver.py
--rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.1/cocoder/chatbase/openai_receiver.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.242998 cocoder-0.1.1/cocoder/ipython/
--rw-rw-rw-   0        0        0      554 2023-05-12 22:40:24.000000 cocoder-0.1.1/cocoder/ipython/__init__.py
--rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.1/cocoder/ipython/core.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.254502 cocoder-0.1.1/cocoder/python/
--rw-rw-rw-   0        0        0      544 2023-05-12 22:40:26.000000 cocoder-0.1.1/cocoder/python/__init__.py
--rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.1/cocoder/python/core.py
-drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.227163 cocoder-0.1.1/cocoder.egg-info/
--rw-rw-rw-   0        0        0     1018 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      435 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       15 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 22:41:10.258509 cocoder-0.1.1/setup.cfg
--rw-rw-rw-   0        0        0     1775 2023-05-12 22:40:18.000000 cocoder-0.1.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.884309 cocoder-0.1.2/
+-rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.2/LICENSE
+-rw-rw-rw-   0        0        0     1018 2023-05-12 22:55:51.882835 cocoder-0.1.2/PKG-INFO
+-rw-rw-rw-   0        0        0      121 2023-05-12 15:23:47.000000 cocoder-0.1.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.836074 cocoder-0.1.2/cocoder/
+-rw-rw-rw-   0        0        0      504 2023-05-12 22:53:33.000000 cocoder-0.1.2/cocoder/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.861317 cocoder-0.1.2/cocoder/chatbase/
+-rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.2/cocoder/chatbase/__init__.py
+-rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.2/cocoder/chatbase/bard_receiver.py
+-rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.2/cocoder/chatbase/openai_receiver.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.872136 cocoder-0.1.2/cocoder/ipython/
+-rw-rw-rw-   0        0        0      554 2023-05-12 22:53:43.000000 cocoder-0.1.2/cocoder/ipython/__init__.py
+-rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.2/cocoder/ipython/core.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.881764 cocoder-0.1.2/cocoder/python/
+-rw-rw-rw-   0        0        0      487 2023-05-12 22:53:46.000000 cocoder-0.1.2/cocoder/python/__init__.py
+-rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.2/cocoder/python/core.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:55:51.853773 cocoder-0.1.2/cocoder.egg-info/
+-rw-rw-rw-   0        0        0     1018 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      435 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       15 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-12 22:55:51.000000 cocoder-0.1.2/cocoder.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-12 22:55:51.885317 cocoder-0.1.2/setup.cfg
+-rw-rw-rw-   0        0        0     1775 2023-05-12 22:53:40.000000 cocoder-0.1.2/setup.py
```

### Comparing `cocoder-0.1.1/LICENSE` & `cocoder-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.1/PKG-INFO` & `cocoder-0.1.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cocoder
-Version: 0.1.1
+Version: 0.1.2
 Home-page: https://github.com/dsdanielpark/Co-Coder
 Author: daniel park
 Author-email: parkminwoo1991@gmail.com
 Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Natural Language :: English
```

### Comparing `cocoder-0.1.1/cocoder/chatbase/bard_receiver.py` & `cocoder-0.1.2/cocoder/chatbase/bard_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.1/cocoder/chatbase/openai_receiver.py` & `cocoder-0.1.2/cocoder/chatbase/openai_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.1/cocoder/ipython/__init__.py` & `cocoder-0.1.2/cocoder/ipython/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,10 +3,10 @@
 from cocoder.ipython.core import ExceptIpyCocoder
 from cocoder.chatbase.bard_receiver import receive_bard_advice
 from cocoder.chatbase.openai_receiver import receive_openai_advice
 from cocoder.chatbase.openai_receiver import get_resp_openai_advice
 
 get_ipython().set_custom_exc((Exception,), ExceptIpyCocoder)
 
-__version__ = "0.1.1"
+__version__ = "0.1.2"
 __author__ = "daniel park <parkminwoo1991@gmail.com>"
 __all__ = ["ExceptIpyCocoder", "receive_bard_advice", "receive_openai_advice", "get_resp_openai_advice"]
```

### Comparing `cocoder-0.1.1/cocoder/ipython/core.py` & `cocoder-0.1.2/cocoder/ipython/core.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.1/cocoder/python/core.py` & `cocoder-0.1.2/cocoder/python/core.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.1/cocoder.egg-info/PKG-INFO` & `cocoder-0.1.2/cocoder.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cocoder
-Version: 0.1.1
+Version: 0.1.2
 Home-page: https://github.com/dsdanielpark/Co-Coder
 Author: daniel park
 Author-email: parkminwoo1991@gmail.com
 Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Natural Language :: English
```

### Comparing `cocoder-0.1.1/setup.py` & `cocoder-0.1.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 
 
 version = get_version()
 
 
 setup(
     name="cocoder",
-    version="0.1.1",
+    version="0.1.2",
     author="daniel park",
     author_email="parkminwoo1991@gmail.com",
     description="",
     long_description=get_long_description(),
     long_description_content_type="text/markdown",
     url="https://github.com/dsdanielpark/Co-Coder",
     packages=find_packages(exclude=[]),
```

