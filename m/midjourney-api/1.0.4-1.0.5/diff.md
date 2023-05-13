# Comparing `tmp/midjourney_api-1.0.4.tar.gz` & `tmp/midjourney_api-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "midjourney_api-1.0.4.tar", last modified: Sat May 13 21:36:18 2023, max compression
+gzip compressed data, was "midjourney_api-1.0.5.tar", last modified: Sat May 13 21:48:59 2023, max compression
```

## Comparing `midjourney_api-1.0.4.tar` & `midjourney_api-1.0.5.tar`

### file list

```diff
@@ -1,5 +1,12 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 21:36:18.267820 midjourney_api-1.0.4/
--rw-rw-rw-   0        0        0     9284 2023-05-13 21:36:18.269292 midjourney_api-1.0.4/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 21:36:18.263470 midjourney_api-1.0.4/midjourney_api/
--rw-rw-rw-   0        0        0     5916 2023-05-13 18:17:05.835466 midjourney_api-1.0.4/midjourney_api/__init__.py
--rw-rw-rw-   0        0        0     1836 2023-05-13 21:36:12.579497 midjourney_api-1.0.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:48:59.217827 midjourney_api-1.0.5/
+-rw-rw-rw-   0        0        0     7388 2023-05-13 21:48:59.216846 midjourney_api-1.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0     6002 2023-05-13 21:22:12.000000 midjourney_api-1.0.5/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 21:48:59.206271 midjourney_api-1.0.5/midjourney_api/
+-rw-rw-rw-   0        0        0     5916 2023-05-13 18:17:05.000000 midjourney_api-1.0.5/midjourney_api/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:48:59.214830 midjourney_api-1.0.5/midjourney_api.egg-info/
+-rw-rw-rw-   0        0        0     7388 2023-05-13 21:48:59.000000 midjourney_api-1.0.5/midjourney_api.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      197 2023-05-13 21:48:59.000000 midjourney_api-1.0.5/midjourney_api.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 21:48:59.000000 midjourney_api-1.0.5/midjourney_api.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       15 2023-05-13 21:48:59.000000 midjourney_api-1.0.5/midjourney_api.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 21:48:59.217827 midjourney_api-1.0.5/setup.cfg
+-rw-rw-rw-   0        0        0     1798 2023-05-13 21:48:43.000000 midjourney_api-1.0.5/setup.py
```

### Comparing `midjourney_api-1.0.4/midjourney_api/__init__.py` & `midjourney_api-1.0.5/midjourney_api/__init__.py`

 * *Files identical despite different names*

### Comparing `midjourney_api-1.0.4/setup.py` & `midjourney_api-1.0.5/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,19 +1,16 @@
-from distutils.core import setup
-
 import pypandoc
+import setuptools
 
-setup(
+setuptools.setup(
     name="midjourney_api",  # How you named your package folder (MyLib)
     packages=["midjourney_api"],  # Chose the same as "name"
-    version="1.0.4",  # Start with a small number and increase it with every change you make
+    version="1.0.5",  # Start with a small number and increase it with every change you make
     license="MIT",  # Chose a license from here: https://help.github.com/articles/licensing-a-repository
-    long_description=pypandoc.convert_file("midjourney_api\\README.md", "rst").replace(
-        "\r", ""
-    ),
+    long_description=pypandoc.convert_file("README.md", "rst").replace("\r", ""),
     description="Midjourney API wrapper by The Next Leg",  # Give a short description about your library
     author="The Next leg",  # Type in your name
     author_email="support@thenextleg.io",  # Type in your E-Mail
     url="https://github.com/midjourney-api-the-next-leg/python-midjourney-api",  # Provide either the link to your github or to your website
     download_url="https://github.com/midjourney-api-the-next-leg/python-midjourney-api/archive/refs/tags/v1.0.0.tar.gz",  # I explain this later on
     keywords=[
         "MIDJOURNEY",
```

