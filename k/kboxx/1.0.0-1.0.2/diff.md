# Comparing `tmp/kboxx-1.0.0.tar.gz` & `tmp/kboxx-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\kboxx-1.0.0.tar", last modified: Thu May 11 08:56:47 2023, max compression
+gzip compressed data, was "dist\kboxx-1.0.2.tar", last modified: Sat May 13 16:34:32 2023, max compression
```

## Comparing `kboxx-1.0.0.tar` & `kboxx-1.0.2.tar`

### file list

```diff
@@ -1,24 +1,36 @@
-drwxrwxrwx   0        0        0        0 2023-05-11 08:56:47.000000 kboxx-1.0.0/
--rw-rw-rw-   0        0        0      934 2023-05-11 08:56:47.000000 kboxx-1.0.0/PKG-INFO
--rw-rw-rw-   0        0        0      369 2023-05-11 08:56:42.000000 kboxx-1.0.0/README.md
-drwxrwxrwx   0        0        0        0 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx/
--rw-rw-rw-   0        0        0       23 2023-05-11 05:14:17.000000 kboxx-1.0.0/kboxx/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx/vit/
--rw-rw-rw-   0        0        0      247 2023-05-11 08:53:13.000000 kboxx-1.0.0/kboxx/vit/__init__.py
--rw-rw-rw-   0        0        0     1295 2023-05-10 08:39:18.000000 kboxx-1.0.0/kboxx/vit/config.py
-drwxrwxrwx   0        0        0        0 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx/vit/layers/
--rw-rw-rw-   0        0        0      317 2023-05-11 08:55:27.000000 kboxx-1.0.0/kboxx/vit/layers/__init__.py
--rw-rw-rw-   0        0        0     4960 2023-05-10 06:29:39.000000 kboxx-1.0.0/kboxx/vit/layers/layers.py
-drwxrwxrwx   0        0        0        0 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx/vit/models/
--rw-rw-rw-   0        0        0      221 2023-05-11 08:55:15.000000 kboxx-1.0.0/kboxx/vit/models/__init__.py
--rw-rw-rw-   0        0        0    15472 2023-05-11 08:03:14.000000 kboxx-1.0.0/kboxx/vit/models/models.py
-drwxrwxrwx   0        0        0        0 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx/vit/utils/
--rw-rw-rw-   0        0        0      115 2023-05-11 08:53:26.000000 kboxx-1.0.0/kboxx/vit/utils/__init__.py
--rw-rw-rw-   0        0        0     5425 2023-05-11 08:24:56.000000 kboxx-1.0.0/kboxx/vit/utils/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx.egg-info/
--rw-rw-rw-   0        0        0      934 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      359 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        6 2023-05-11 08:56:47.000000 kboxx-1.0.0/kboxx.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-11 08:56:47.000000 kboxx-1.0.0/setup.cfg
--rw-rw-rw-   0        0        0      694 2023-05-11 08:56:29.000000 kboxx-1.0.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/
+-rw-rw-rw-   0        0        0      934 2023-05-13 16:34:32.000000 kboxx-1.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0      369 2023-05-11 08:56:42.000000 kboxx-1.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/
+-rw-rw-rw-   0        0        0       23 2023-05-13 16:34:00.000000 kboxx-1.0.2/kboxx/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/transformer/
+-rw-rw-rw-   0        0        0      129 2023-05-13 05:18:39.000000 kboxx-1.0.2/kboxx/transformer/__init__.py
+-rw-rw-rw-   0        0        0        2 2023-01-20 13:12:54.000000 kboxx-1.0.2/kboxx/transformer/config.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/transformer/layers/
+-rw-rw-rw-   0        0        0      481 2023-05-13 12:15:05.000000 kboxx-1.0.2/kboxx/transformer/layers/__init__.py
+-rw-rw-rw-   0        0        0     8334 2023-05-13 12:15:05.000000 kboxx-1.0.2/kboxx/transformer/layers/layers.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/transformer/models/
+-rw-rw-rw-   0        0        0       55 2023-05-12 14:07:03.000000 kboxx-1.0.2/kboxx/transformer/models/__init__.py
+-rw-rw-rw-   0        0        0     4878 2023-05-13 12:29:03.000000 kboxx-1.0.2/kboxx/transformer/models/models.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/transformer/utils/
+-rw-rw-rw-   0        0        0      188 2023-05-13 06:07:51.000000 kboxx-1.0.2/kboxx/transformer/utils/__init__.py
+-rw-rw-rw-   0        0        0     1959 2023-05-13 06:36:44.000000 kboxx-1.0.2/kboxx/transformer/utils/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/vit/
+-rw-rw-rw-   0        0        0      247 2023-05-11 08:53:13.000000 kboxx-1.0.2/kboxx/vit/__init__.py
+-rw-rw-rw-   0        0        0     1295 2023-05-10 08:39:18.000000 kboxx-1.0.2/kboxx/vit/config.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/vit/layers/
+-rw-rw-rw-   0        0        0      317 2023-05-11 08:55:27.000000 kboxx-1.0.2/kboxx/vit/layers/__init__.py
+-rw-rw-rw-   0        0        0     4960 2023-05-10 06:29:39.000000 kboxx-1.0.2/kboxx/vit/layers/layers.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/vit/models/
+-rw-rw-rw-   0        0        0      221 2023-05-11 08:55:15.000000 kboxx-1.0.2/kboxx/vit/models/__init__.py
+-rw-rw-rw-   0        0        0    15472 2023-05-11 08:03:14.000000 kboxx-1.0.2/kboxx/vit/models/models.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx/vit/utils/
+-rw-rw-rw-   0        0        0      115 2023-05-11 08:53:26.000000 kboxx-1.0.2/kboxx/vit/utils/__init__.py
+-rw-rw-rw-   0        0        0     5425 2023-05-11 08:24:56.000000 kboxx-1.0.2/kboxx/vit/utils/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx.egg-info/
+-rw-rw-rw-   0        0        0      934 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      630 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        6 2023-05-13 16:34:32.000000 kboxx-1.0.2/kboxx.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 16:34:32.000000 kboxx-1.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      694 2023-05-13 16:33:42.000000 kboxx-1.0.2/setup.py
```

### Comparing `kboxx-1.0.0/PKG-INFO` & `kboxx-1.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kboxx
-Version: 1.0.0
+Version: 1.0.2
 Summary: Implementation of pre-trained model based on Keras
 Home-page: https://github.com/djsaber/Keras-ViT
 Author: djsaber
 Author-email: 479719615@qq.com
 License: UNKNOWN
 Description: # kboxx
```

### Comparing `kboxx-1.0.0/kboxx/vit/config.py` & `kboxx-1.0.2/kboxx/vit/config.py`

 * *Files identical despite different names*

### Comparing `kboxx-1.0.0/kboxx/vit/layers/layers.py` & `kboxx-1.0.2/kboxx/vit/layers/layers.py`

 * *Files identical despite different names*

### Comparing `kboxx-1.0.0/kboxx/vit/models/models.py` & `kboxx-1.0.2/kboxx/vit/models/models.py`

 * *Files identical despite different names*

### Comparing `kboxx-1.0.0/kboxx/vit/utils/utils.py` & `kboxx-1.0.2/kboxx/vit/utils/utils.py`

 * *Files identical despite different names*

### Comparing `kboxx-1.0.0/kboxx.egg-info/PKG-INFO` & `kboxx-1.0.2/kboxx.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kboxx
-Version: 1.0.0
+Version: 1.0.2
 Summary: Implementation of pre-trained model based on Keras
 Home-page: https://github.com/djsaber/Keras-ViT
 Author: djsaber
 Author-email: 479719615@qq.com
 License: UNKNOWN
 Description: # kboxx
```

### Comparing `kboxx-1.0.0/setup.py` & `kboxx-1.0.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
  
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
  
 setuptools.setup(
     name="kboxx",
-    version="1.0.0",
+    version="1.0.2",
     author="djsaber",
     author_email="479719615@qq.com",
     description="Implementation of pre-trained model based on Keras",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/djsaber/Keras-ViT",
     packages=setuptools.find_packages(),
```

