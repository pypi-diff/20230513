# Comparing `tmp/django-utilitas-1.3.2.tar.gz` & `tmp/django-utilitas-1.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-utilitas-1.3.2.tar", last modified: Sat May 13 00:53:08 2023, max compression
+gzip compressed data, was "django-utilitas-1.3.3.tar", last modified: Sat May 13 00:56:06 2023, max compression
```

## Comparing `django-utilitas-1.3.2.tar` & `django-utilitas-1.3.3.tar`

### file list

```diff
@@ -1,32 +1,32 @@
-drwxr-xr-x   0 jamesthiha   (501) staff       (20)        0 2023-05-13 00:53:08.541970 django-utilitas-1.3.2/
--rw-r--r--   0 jamesthiha   (501) staff       (20)    35149 2022-12-05 07:45:37.000000 django-utilitas-1.3.2/LICENSE
--rw-r--r--   0 jamesthiha   (501) staff       (20)     4713 2023-05-13 00:53:08.542432 django-utilitas-1.3.2/PKG-INFO
--rw-r--r--   0 jamesthiha   (501) staff       (20)     4468 2023-05-13 00:52:31.000000 django-utilitas-1.3.2/README.md
-drwxr-xr-x   0 jamesthiha   (501) staff       (20)        0 2023-05-13 00:53:08.525094 django-utilitas-1.3.2/django_utilitas.egg-info/
--rw-r--r--   0 jamesthiha   (501) staff       (20)     4713 2023-05-13 00:53:08.000000 django-utilitas-1.3.2/django_utilitas.egg-info/PKG-INFO
--rw-r--r--   0 jamesthiha   (501) staff       (20)      642 2023-05-13 00:53:08.000000 django-utilitas-1.3.2/django_utilitas.egg-info/SOURCES.txt
--rw-r--r--   0 jamesthiha   (501) staff       (20)        1 2023-05-13 00:53:08.000000 django-utilitas-1.3.2/django_utilitas.egg-info/dependency_links.txt
--rw-r--r--   0 jamesthiha   (501) staff       (20)       80 2023-05-13 00:53:08.000000 django-utilitas-1.3.2/django_utilitas.egg-info/requires.txt
--rw-r--r--   0 jamesthiha   (501) staff       (20)        9 2023-05-13 00:53:08.000000 django-utilitas-1.3.2/django_utilitas.egg-info/top_level.txt
--rw-r--r--   0 jamesthiha   (501) staff       (20)      428 2023-05-13 00:53:08.543602 django-utilitas-1.3.2/setup.cfg
--rw-r--r--   0 jamesthiha   (501) staff       (20)      263 2022-12-05 08:04:03.000000 django-utilitas-1.3.2/setup.py
-drwxr-xr-x   0 jamesthiha   (501) staff       (20)        0 2023-05-13 00:53:08.539868 django-utilitas-1.3.2/utilitas/
--rw-r--r--   0 jamesthiha   (501) staff       (20)        0 2022-11-28 18:11:49.000000 django-utilitas-1.3.2/utilitas/__init__.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)       63 2022-11-28 18:11:49.000000 django-utilitas-1.3.2/utilitas/admin.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)      148 2022-11-28 18:11:50.000000 django-utilitas-1.3.2/utilitas/apps.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)      349 2022-12-05 07:27:09.000000 django-utilitas-1.3.2/utilitas/exception_handler.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)        0 2022-11-28 19:38:13.000000 django-utilitas-1.3.2/utilitas/exceptions.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)       76 2022-12-05 07:26:41.000000 django-utilitas-1.3.2/utilitas/managers.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)      778 2022-12-05 03:43:29.000000 django-utilitas-1.3.2/utilitas/metadata.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)      591 2023-01-25 15:05:12.000000 django-utilitas-1.3.2/utilitas/middlewares.py
-drwxr-xr-x   0 jamesthiha   (501) staff       (20)        0 2023-05-13 00:53:08.541349 django-utilitas-1.3.2/utilitas/migrations/
--rw-r--r--   0 jamesthiha   (501) staff       (20)        0 2022-11-28 18:11:49.000000 django-utilitas-1.3.2/utilitas/migrations/__init__.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)     1454 2022-12-05 07:25:03.000000 django-utilitas-1.3.2/utilitas/models.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)     1031 2023-02-22 06:50:16.000000 django-utilitas-1.3.2/utilitas/pagination.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)      366 2022-11-28 19:43:27.000000 django-utilitas-1.3.2/utilitas/renderer.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)     1450 2023-02-19 23:16:44.000000 django-utilitas-1.3.2/utilitas/serializers.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)      945 2022-12-05 08:14:19.000000 django-utilitas-1.3.2/utilitas/swagger_query_params.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)      347 2022-11-28 19:35:23.000000 django-utilitas-1.3.2/utilitas/swagger_serializers.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)       60 2022-11-28 18:11:49.000000 django-utilitas-1.3.2/utilitas/tests.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)       18 2022-11-28 18:28:32.000000 django-utilitas-1.3.2/utilitas/urls.py
--rw-r--r--   0 jamesthiha   (501) staff       (20)    17502 2023-05-13 00:52:47.000000 django-utilitas-1.3.2/utilitas/views.py
+drwxr-xr-x   0 jamesthiha   (501) staff       (20)        0 2023-05-13 00:56:06.461783 django-utilitas-1.3.3/
+-rw-r--r--   0 jamesthiha   (501) staff       (20)    35149 2022-12-05 07:45:37.000000 django-utilitas-1.3.3/LICENSE
+-rw-r--r--   0 jamesthiha   (501) staff       (20)     4759 2023-05-13 00:56:06.461933 django-utilitas-1.3.3/PKG-INFO
+-rw-r--r--   0 jamesthiha   (501) staff       (20)     4514 2023-05-13 00:55:43.000000 django-utilitas-1.3.3/README.md
+drwxr-xr-x   0 jamesthiha   (501) staff       (20)        0 2023-05-13 00:56:06.449281 django-utilitas-1.3.3/django_utilitas.egg-info/
+-rw-r--r--   0 jamesthiha   (501) staff       (20)     4759 2023-05-13 00:56:06.000000 django-utilitas-1.3.3/django_utilitas.egg-info/PKG-INFO
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      642 2023-05-13 00:56:06.000000 django-utilitas-1.3.3/django_utilitas.egg-info/SOURCES.txt
+-rw-r--r--   0 jamesthiha   (501) staff       (20)        1 2023-05-13 00:56:06.000000 django-utilitas-1.3.3/django_utilitas.egg-info/dependency_links.txt
+-rw-r--r--   0 jamesthiha   (501) staff       (20)       80 2023-05-13 00:56:06.000000 django-utilitas-1.3.3/django_utilitas.egg-info/requires.txt
+-rw-r--r--   0 jamesthiha   (501) staff       (20)        9 2023-05-13 00:56:06.000000 django-utilitas-1.3.3/django_utilitas.egg-info/top_level.txt
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      428 2023-05-13 00:56:06.462540 django-utilitas-1.3.3/setup.cfg
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      263 2022-12-05 08:04:03.000000 django-utilitas-1.3.3/setup.py
+drwxr-xr-x   0 jamesthiha   (501) staff       (20)        0 2023-05-13 00:56:06.461055 django-utilitas-1.3.3/utilitas/
+-rw-r--r--   0 jamesthiha   (501) staff       (20)        0 2022-11-28 18:11:49.000000 django-utilitas-1.3.3/utilitas/__init__.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)       63 2022-11-28 18:11:49.000000 django-utilitas-1.3.3/utilitas/admin.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      148 2022-11-28 18:11:50.000000 django-utilitas-1.3.3/utilitas/apps.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      349 2022-12-05 07:27:09.000000 django-utilitas-1.3.3/utilitas/exception_handler.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)        0 2022-11-28 19:38:13.000000 django-utilitas-1.3.3/utilitas/exceptions.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)       76 2022-12-05 07:26:41.000000 django-utilitas-1.3.3/utilitas/managers.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      778 2022-12-05 03:43:29.000000 django-utilitas-1.3.3/utilitas/metadata.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      591 2023-01-25 15:05:12.000000 django-utilitas-1.3.3/utilitas/middlewares.py
+drwxr-xr-x   0 jamesthiha   (501) staff       (20)        0 2023-05-13 00:56:06.461522 django-utilitas-1.3.3/utilitas/migrations/
+-rw-r--r--   0 jamesthiha   (501) staff       (20)        0 2022-11-28 18:11:49.000000 django-utilitas-1.3.3/utilitas/migrations/__init__.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)     1454 2022-12-05 07:25:03.000000 django-utilitas-1.3.3/utilitas/models.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)     1031 2023-02-22 06:50:16.000000 django-utilitas-1.3.3/utilitas/pagination.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      366 2022-11-28 19:43:27.000000 django-utilitas-1.3.3/utilitas/renderer.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)     1450 2023-02-19 23:16:44.000000 django-utilitas-1.3.3/utilitas/serializers.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      945 2022-12-05 08:14:19.000000 django-utilitas-1.3.3/utilitas/swagger_query_params.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)      347 2022-11-28 19:35:23.000000 django-utilitas-1.3.3/utilitas/swagger_serializers.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)       60 2022-11-28 18:11:49.000000 django-utilitas-1.3.3/utilitas/tests.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)       18 2022-11-28 18:28:32.000000 django-utilitas-1.3.3/utilitas/urls.py
+-rw-r--r--   0 jamesthiha   (501) staff       (20)    17512 2023-05-13 00:55:17.000000 django-utilitas-1.3.3/utilitas/views.py
```

### Comparing `django-utilitas-1.3.2/LICENSE` & `django-utilitas-1.3.3/LICENSE`

 * *Files identical despite different names*

### Comparing `django-utilitas-1.3.2/PKG-INFO` & `django-utilitas-1.3.3/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-utilitas
-Version: 1.3.2
+Version: 1.3.3
 Summary: Django package with useful utility classes
 Home-page: https://github.com/ninnroot/utilitas
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Django Utilitas
@@ -116,17 +116,18 @@
 
 requests.get("api/books?csv=true")
 ```
 
 
 ## Changelog
 
+- 1.3.3
+    - forgot to add csv library. hehe.
 - 1.3.2
     - added a csv-returning functionality.
-
 - 1.3.1
     - now, the API won't return 500 if missing foreign keys are provided in the `expand` parameter.
 - 1.3.0
     - removed the need for `related_fields` parameter. Prefetching related fields is now done automatically using the `expand` parameter provided by the client.
 - 1.2.9
     - renamed file from `migrations.py` to `middlewares.py` (my stupid mistake in the first place)
 - 1.2.8
```

### Comparing `django-utilitas-1.3.2/README.md` & `django-utilitas-1.3.3/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -107,17 +107,18 @@
 
 requests.get("api/books?csv=true")
 ```
 
 
 ## Changelog
 
+- 1.3.3
+    - forgot to add csv library. hehe.
 - 1.3.2
     - added a csv-returning functionality.
-
 - 1.3.1
     - now, the API won't return 500 if missing foreign keys are provided in the `expand` parameter.
 - 1.3.0
     - removed the need for `related_fields` parameter. Prefetching related fields is now done automatically using the `expand` parameter provided by the client.
 - 1.2.9
     - renamed file from `migrations.py` to `middlewares.py` (my stupid mistake in the first place)
 - 1.2.8
```

### Comparing `django-utilitas-1.3.2/django_utilitas.egg-info/PKG-INFO` & `django-utilitas-1.3.3/django_utilitas.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-utilitas
-Version: 1.3.2
+Version: 1.3.3
 Summary: Django package with useful utility classes
 Home-page: https://github.com/ninnroot/utilitas
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Django Utilitas
@@ -116,17 +116,18 @@
 
 requests.get("api/books?csv=true")
 ```
 
 
 ## Changelog
 
+- 1.3.3
+    - forgot to add csv library. hehe.
 - 1.3.2
     - added a csv-returning functionality.
-
 - 1.3.1
     - now, the API won't return 500 if missing foreign keys are provided in the `expand` parameter.
 - 1.3.0
     - removed the need for `related_fields` parameter. Prefetching related fields is now done automatically using the `expand` parameter provided by the client.
 - 1.2.9
     - renamed file from `migrations.py` to `middlewares.py` (my stupid mistake in the first place)
 - 1.2.8
```

### Comparing `django-utilitas-1.3.2/django_utilitas.egg-info/SOURCES.txt` & `django-utilitas-1.3.3/django_utilitas.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `django-utilitas-1.3.2/utilitas/metadata.py` & `django-utilitas-1.3.3/utilitas/metadata.py`

 * *Files identical despite different names*

### Comparing `django-utilitas-1.3.2/utilitas/middlewares.py` & `django-utilitas-1.3.3/utilitas/middlewares.py`

 * *Files identical despite different names*

### Comparing `django-utilitas-1.3.2/utilitas/models.py` & `django-utilitas-1.3.3/utilitas/models.py`

 * *Files identical despite different names*

### Comparing `django-utilitas-1.3.2/utilitas/pagination.py` & `django-utilitas-1.3.3/utilitas/pagination.py`

 * *Files identical despite different names*

### Comparing `django-utilitas-1.3.2/utilitas/serializers.py` & `django-utilitas-1.3.3/utilitas/serializers.py`

 * *Files identical despite different names*

### Comparing `django-utilitas-1.3.2/utilitas/swagger_query_params.py` & `django-utilitas-1.3.3/utilitas/swagger_query_params.py`

 * *Files identical despite different names*

### Comparing `django-utilitas-1.3.2/utilitas/views.py` & `django-utilitas-1.3.3/utilitas/views.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import base64
 import json
-
+import csv
 
 from django.core.exceptions import BadRequest
 from drf_yasg.utils import swagger_auto_schema
 from rest_framework.renderers import BrowsableAPIRenderer
 from rest_framework.views import APIView, Request, Response, status
 from django.db.models import (
     QuerySet,
```

