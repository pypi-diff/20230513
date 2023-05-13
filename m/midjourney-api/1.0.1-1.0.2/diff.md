# Comparing `tmp/midjourney_api-1.0.1.tar.gz` & `tmp/midjourney_api-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "midjourney_api-1.0.1.tar", last modified: Sat May 13 21:05:14 2023, max compression
+gzip compressed data, was "midjourney_api-1.0.2.tar", last modified: Sat May 13 21:06:37 2023, max compression
```

## Comparing `midjourney_api-1.0.1.tar` & `midjourney_api-1.0.2.tar`

### file list

```diff
@@ -1,6 +1,5 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 21:05:14.675527 midjourney_api-1.0.1/
--rw-rw-rw-   0        0        0      862 2023-05-13 21:05:14.676559 midjourney_api-1.0.1/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 21:05:14.675527 midjourney_api-1.0.1/midjourney_api/
--rw-rw-rw-   0        0        0     5916 2023-05-13 18:17:05.835466 midjourney_api-1.0.1/midjourney_api/__init__.py
--rw-rw-rw-   0        0        0       63 2023-05-13 19:38:37.971746 midjourney_api-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1702 2023-05-13 21:05:10.500613 midjourney_api-1.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.631140 midjourney_api-1.0.2/
+-rw-rw-rw-   0        0        0      862 2023-05-13 21:06:37.631140 midjourney_api-1.0.2/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.630130 midjourney_api-1.0.2/midjourney_api/
+-rw-rw-rw-   0        0        0     5916 2023-05-13 18:17:05.835466 midjourney_api-1.0.2/midjourney_api/__init__.py
+-rw-rw-rw-   0        0        0     1702 2023-05-13 21:06:28.107535 midjourney_api-1.0.2/setup.py
```

### Comparing `midjourney_api-1.0.1/PKG-INFO` & `midjourney_api-1.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.1
 Name: midjourney_api
-Version: 1.0.1
+Version: 1.0.2
 Summary: Midjourney API wrapper by The Next Leg
 Home-page: https://github.com/midjourney-api-the-next-leg/python-midjourney-api
 Author: The Next leg
 Author-email: support@thenextleg.io
 License: MIT
 Download-URL: https://github.com/midjourney-api-the-next-leg/python-midjourney-api/archive/refs/tags/v1.0.0.tar.gz
 Description: UNKNOWN
```

### Comparing `midjourney_api-1.0.1/midjourney_api/__init__.py` & `midjourney_api-1.0.2/midjourney_api/__init__.py`

 * *Files identical despite different names*

### Comparing `midjourney_api-1.0.1/setup.py` & `midjourney_api-1.0.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from distutils.core import setup
 setup(
   name = 'midjourney_api',         # How you named your package folder (MyLib)
   packages = ['midjourney_api'],   # Chose the same as "name"
-  version = '1.0.1',      # Start with a small number and increase it with every change you make
+  version = '1.0.2',      # Start with a small number and increase it with every change you make
   license='MIT',        # Chose a license from here: https://help.github.com/articles/licensing-a-repository
   description = 'Midjourney API wrapper by The Next Leg',   # Give a short description about your library
   author = 'The Next leg',                   # Type in your name
   author_email = 'support@thenextleg.io',      # Type in your E-Mail
   url = 'https://github.com/midjourney-api-the-next-leg/python-midjourney-api',   # Provide either the link to your github or to your website
   download_url = 'https://github.com/midjourney-api-the-next-leg/python-midjourney-api/archive/refs/tags/v1.0.0.tar.gz',    # I explain this later on
   keywords = ['MIDJOURNEY', 'API', 'THE_NEXT_LEG'],   # Keywords that define your package best
```

