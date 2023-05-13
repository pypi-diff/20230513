# Comparing `tmp/cocoder-0.1.3.tar.gz` & `tmp/cocoder-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cocoder-0.1.3.tar", last modified: Fri May 12 23:02:12 2023, max compression
+gzip compressed data, was "cocoder-0.1.4.tar", last modified: Sat May 13 01:54:41 2023, max compression
```

## Comparing `cocoder-0.1.3.tar` & `cocoder-0.1.4.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.431957 cocoder-0.1.3/
--rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.3/LICENSE
--rw-rw-rw-   0        0        0     1018 2023-05-12 23:02:12.429960 cocoder-0.1.3/PKG-INFO
--rw-rw-rw-   0        0        0      121 2023-05-12 15:23:47.000000 cocoder-0.1.3/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.378511 cocoder-0.1.3/cocoder/
--rw-rw-rw-   0        0        0      504 2023-05-12 23:01:04.000000 cocoder-0.1.3/cocoder/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.405386 cocoder-0.1.3/cocoder/chatbase/
--rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.3/cocoder/chatbase/__init__.py
--rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.3/cocoder/chatbase/bard_receiver.py
--rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.3/cocoder/chatbase/openai_receiver.py
-drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.417464 cocoder-0.1.3/cocoder/ipython/
--rw-rw-rw-   0        0        0      583 2023-05-12 23:01:00.000000 cocoder-0.1.3/cocoder/ipython/__init__.py
--rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.3/cocoder/ipython/core.py
-drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.427630 cocoder-0.1.3/cocoder/python/
--rw-rw-rw-   0        0        0      487 2023-05-12 23:01:56.000000 cocoder-0.1.3/cocoder/python/__init__.py
--rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.3/cocoder/python/core.py
-drwxrwxrwx   0        0        0        0 2023-05-12 23:02:12.398562 cocoder-0.1.3/cocoder.egg-info/
--rw-rw-rw-   0        0        0     1018 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      435 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       15 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-12 23:02:12.000000 cocoder-0.1.3/cocoder.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 23:02:12.431957 cocoder-0.1.3/setup.cfg
--rw-rw-rw-   0        0        0     1775 2023-05-12 23:01:59.000000 cocoder-0.1.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.598137 cocoder-0.1.4/
+-rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.4/LICENSE
+-rw-rw-rw-   0        0        0     7271 2023-05-13 01:54:41.596639 cocoder-0.1.4/PKG-INFO
+-rw-rw-rw-   0        0        0     6374 2023-05-13 01:53:39.000000 cocoder-0.1.4/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.547228 cocoder-0.1.4/cocoder/
+-rw-rw-rw-   0        0        0      504 2023-05-13 01:54:09.000000 cocoder-0.1.4/cocoder/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.574656 cocoder-0.1.4/cocoder/chatbase/
+-rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.4/cocoder/chatbase/__init__.py
+-rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.4/cocoder/chatbase/bard_receiver.py
+-rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.4/cocoder/chatbase/openai_receiver.py
+drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.584956 cocoder-0.1.4/cocoder/ipython/
+-rw-rw-rw-   0        0        0      583 2023-05-13 01:54:03.000000 cocoder-0.1.4/cocoder/ipython/__init__.py
+-rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.4/cocoder/ipython/core.py
+drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.594640 cocoder-0.1.4/cocoder/python/
+-rw-rw-rw-   0        0        0      487 2023-05-13 01:54:06.000000 cocoder-0.1.4/cocoder/python/__init__.py
+-rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.4/cocoder/python/core.py
+drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.567654 cocoder-0.1.4/cocoder.egg-info/
+-rw-rw-rw-   0        0        0     7271 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      435 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       15 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 01:54:41.598137 cocoder-0.1.4/setup.cfg
+-rw-rw-rw-   0        0        0     1775 2023-05-13 01:54:00.000000 cocoder-0.1.4/setup.py
```

### Comparing `cocoder-0.1.3/LICENSE` & `cocoder-0.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.3/cocoder/chatbase/bard_receiver.py` & `cocoder-0.1.4/cocoder/chatbase/bard_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.3/cocoder/chatbase/openai_receiver.py` & `cocoder-0.1.4/cocoder/chatbase/openai_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.3/cocoder/ipython/__init__.py` & `cocoder-0.1.4/cocoder/ipython/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -6,10 +6,10 @@
 from cocoder.chatbase.openai_receiver import get_resp_openai_advice
 
 try:
     get_ipython().set_custom_exc((Exception,), ExceptIpyCocoder)
 except:
     pass
 
-__version__ = "0.1.3"
+__version__ = "0.1.4"
 __author__ = "daniel park <parkminwoo1991@gmail.com>"
 __all__ = ["ExceptIpyCocoder", "receive_bard_advice", "receive_openai_advice", "get_resp_openai_advice"]
```

### Comparing `cocoder-0.1.3/cocoder/ipython/core.py` & `cocoder-0.1.4/cocoder/ipython/core.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.3/cocoder/python/core.py` & `cocoder-0.1.4/cocoder/python/core.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.3/setup.py` & `cocoder-0.1.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 
 
 version = get_version()
 
 
 setup(
     name="cocoder",
-    version="0.1.3",
+    version="0.1.4",
     author="daniel park",
     author_email="parkminwoo1991@gmail.com",
     description="",
     long_description=get_long_description(),
     long_description_content_type="text/markdown",
     url="https://github.com/dsdanielpark/Co-Coder",
     packages=find_packages(exclude=[]),
```

