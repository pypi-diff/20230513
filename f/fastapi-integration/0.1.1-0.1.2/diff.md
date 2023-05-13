# Comparing `tmp/fastapi-integration-0.1.1.tar.gz` & `tmp/fastapi-integration-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fastapi-integration-0.1.1.tar", last modified: Sat May 13 15:58:30 2023, max compression
+gzip compressed data, was "fastapi-integration-0.1.2.tar", last modified: Sat May 13 16:03:23 2023, max compression
```

## Comparing `fastapi-integration-0.1.1.tar` & `fastapi-integration-0.1.2.tar`

### file list

```diff
@@ -1,54 +1,54 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.953468 fastapi-integration-0.1.1/
--rw-rw-rw-   0        0        0      301 2023-05-13 15:58:30.951962 fastapi-integration-0.1.1/PKG-INFO
--rw-rw-rw-   0        0        0     7236 2023-05-13 09:16:55.000000 fastapi-integration-0.1.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.927957 fastapi-integration-0.1.1/examples/
--rw-rw-rw-   0        0        0        0 2023-05-10 12:42:06.000000 fastapi-integration-0.1.1/examples/__init__.py
--rw-rw-rw-   0        0        0      157 2023-05-12 14:59:56.000000 fastapi-integration-0.1.1/examples/admin.py
--rw-rw-rw-   0        0        0      374 2023-05-12 14:08:35.000000 fastapi-integration-0.1.1/examples/base.py
--rw-rw-rw-   0        0        0     1306 2023-05-12 15:00:08.000000 fastapi-integration-0.1.1/examples/main.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.930956 fastapi-integration-0.1.1/fastapi_integration/
--rw-rw-rw-   0        0        0     6729 2023-05-13 10:13:13.000000 fastapi-integration-0.1.1/fastapi_integration/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.943961 fastapi-integration-0.1.1/fastapi_integration/admin/
--rw-rw-rw-   0        0        0     1078 2023-05-12 15:09:09.000000 fastapi-integration-0.1.1/fastapi_integration/admin/__init__.py
--rw-rw-rw-   0        0        0     1090 2023-05-12 16:12:12.000000 fastapi-integration-0.1.1/fastapi_integration/admin/generator.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.945962 fastapi-integration-0.1.1/fastapi_integration/auth/
--rw-rw-rw-   0        0        0     1694 2023-05-12 15:09:42.000000 fastapi-integration-0.1.1/fastapi_integration/auth/__init__.py
--rw-rw-rw-   0        0        0     4188 2023-05-12 16:02:33.000000 fastapi-integration-0.1.1/fastapi_integration/auth/routers.py
--rw-rw-rw-   0        0        0     1236 2023-05-12 16:02:47.000000 fastapi-integration-0.1.1/fastapi_integration/auth/schemas.py
--rw-rw-rw-   0        0        0     3360 2023-05-12 15:14:15.000000 fastapi-integration-0.1.1/fastapi_integration/auth/utils.py
--rw-rw-rw-   0        0        0      286 2023-05-12 16:09:08.000000 fastapi-integration-0.1.1/fastapi_integration/common.py
--rw-rw-rw-   0        0        0     3505 2023-05-13 08:58:12.000000 fastapi-integration-0.1.1/fastapi_integration/config.py
--rw-rw-rw-   0        0        0     5227 2023-05-12 16:43:57.000000 fastapi-integration-0.1.1/fastapi_integration/db.py
--rw-rw-rw-   0        0        0      909 2023-05-12 16:11:09.000000 fastapi-integration-0.1.1/fastapi_integration/dependencies.py
--rw-rw-rw-   0        0        0     1018 2023-05-12 16:07:33.000000 fastapi-integration-0.1.1/fastapi_integration/exceptions.py
--rw-rw-rw-   0        0        0      603 2023-05-12 16:07:52.000000 fastapi-integration-0.1.1/fastapi_integration/features.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.946962 fastapi-integration-0.1.1/fastapi_integration/generic/
--rw-rw-rw-   0        0        0        0 2023-04-01 15:15:50.000000 fastapi-integration-0.1.1/fastapi_integration/generic/__init__.py
--rw-rw-rw-   0        0        0     8968 2023-05-12 15:17:57.000000 fastapi-integration-0.1.1/fastapi_integration/generic/crud.py
--rw-rw-rw-   0        0        0        0 2023-04-01 12:17:01.000000 fastapi-integration-0.1.1/fastapi_integration/generic/views.py
--rw-rw-rw-   0        0        0     2635 2023-05-12 16:08:42.000000 fastapi-integration-0.1.1/fastapi_integration/models.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.949963 fastapi-integration-0.1.1/fastapi_integration/orm/
--rw-rw-rw-   0        0        0        0 2023-04-01 15:15:48.000000 fastapi-integration-0.1.1/fastapi_integration/orm/__init__.py
--rw-rw-rw-   0        0        0    10300 2023-05-10 14:45:33.000000 fastapi-integration-0.1.1/fastapi_integration/orm/base.py
--rw-rw-rw-   0        0        0      242 2023-05-12 16:45:11.000000 fastapi-integration-0.1.1/fastapi_integration/orm/models.py
--rw-rw-rw-   0        0        0    13436 2023-05-10 13:51:16.000000 fastapi-integration-0.1.1/fastapi_integration/orm/queries.py
--rw-rw-rw-   0        0        0     1251 2023-05-08 17:22:39.000000 fastapi-integration-0.1.1/fastapi_integration/orm/signals.py
--rw-rw-rw-   0        0        0        0 2023-04-04 13:39:29.000000 fastapi-integration-0.1.1/fastapi_integration/orm/transaction.py
--rw-rw-rw-   0        0        0      985 2023-05-07 14:59:54.000000 fastapi-integration-0.1.1/fastapi_integration/orm/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.949963 fastapi-integration-0.1.1/fastapi_integration/utils/
--rw-rw-rw-   0        0        0        0 2023-04-01 15:15:47.000000 fastapi-integration-0.1.1/fastapi_integration/utils/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.942963 fastapi-integration-0.1.1/fastapi_integration.egg-info/
--rw-rw-rw-   0        0        0      301 2023-05-13 15:58:30.000000 fastapi-integration-0.1.1/fastapi_integration.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1281 2023-05-13 15:58:30.000000 fastapi-integration-0.1.1/fastapi_integration.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 15:58:30.000000 fastapi-integration-0.1.1/fastapi_integration.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       94 2023-05-13 15:58:30.000000 fastapi-integration-0.1.1/fastapi_integration.egg-info/requires.txt
--rw-rw-rw-   0        0        0       35 2023-05-13 15:58:30.000000 fastapi-integration-0.1.1/fastapi_integration.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 15:58:30.953468 fastapi-integration-0.1.1/setup.cfg
--rw-rw-rw-   0        0        0      612 2023-05-13 15:53:02.000000 fastapi-integration-0.1.1/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.950962 fastapi-integration-0.1.1/tests/
--rw-rw-rw-   0        0        0        0 2023-05-10 12:42:06.000000 fastapi-integration-0.1.1/tests/__init__.py
--rw-rw-rw-   0        0        0      374 2023-05-12 15:00:58.000000 fastapi-integration-0.1.1/tests/base.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:58:30.951962 fastapi-integration-0.1.1/tests/query/
--rw-rw-rw-   0        0        0        0 2023-04-06 11:11:49.000000 fastapi-integration-0.1.1/tests/query/__init__.py
--rw-rw-rw-   0        0        0    10030 2023-05-13 08:59:48.000000 fastapi-integration-0.1.1/tests/query/test_complex.py
--rw-rw-rw-   0        0        0     7270 2023-05-09 16:07:05.000000 fastapi-integration-0.1.1/tests/query/test_simple.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.854580 fastapi-integration-0.1.2/
+-rw-rw-rw-   0        0        0      301 2023-05-13 16:03:23.854580 fastapi-integration-0.1.2/PKG-INFO
+-rw-rw-rw-   0        0        0     7236 2023-05-13 09:16:55.000000 fastapi-integration-0.1.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.832580 fastapi-integration-0.1.2/examples/
+-rw-rw-rw-   0        0        0        0 2023-05-10 12:42:06.000000 fastapi-integration-0.1.2/examples/__init__.py
+-rw-rw-rw-   0        0        0      157 2023-05-12 14:59:56.000000 fastapi-integration-0.1.2/examples/admin.py
+-rw-rw-rw-   0        0        0      374 2023-05-12 14:08:35.000000 fastapi-integration-0.1.2/examples/base.py
+-rw-rw-rw-   0        0        0     1306 2023-05-12 15:00:08.000000 fastapi-integration-0.1.2/examples/main.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.836579 fastapi-integration-0.1.2/fastapi_integration/
+-rw-rw-rw-   0        0        0     6729 2023-05-13 10:13:13.000000 fastapi-integration-0.1.2/fastapi_integration/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.845581 fastapi-integration-0.1.2/fastapi_integration/admin/
+-rw-rw-rw-   0        0        0     1078 2023-05-12 15:09:09.000000 fastapi-integration-0.1.2/fastapi_integration/admin/__init__.py
+-rw-rw-rw-   0        0        0     1090 2023-05-12 16:12:12.000000 fastapi-integration-0.1.2/fastapi_integration/admin/generator.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.847580 fastapi-integration-0.1.2/fastapi_integration/auth/
+-rw-rw-rw-   0        0        0     1694 2023-05-12 15:09:42.000000 fastapi-integration-0.1.2/fastapi_integration/auth/__init__.py
+-rw-rw-rw-   0        0        0     4188 2023-05-12 16:02:33.000000 fastapi-integration-0.1.2/fastapi_integration/auth/routers.py
+-rw-rw-rw-   0        0        0     1236 2023-05-12 16:02:47.000000 fastapi-integration-0.1.2/fastapi_integration/auth/schemas.py
+-rw-rw-rw-   0        0        0     3360 2023-05-12 15:14:15.000000 fastapi-integration-0.1.2/fastapi_integration/auth/utils.py
+-rw-rw-rw-   0        0        0      286 2023-05-12 16:09:08.000000 fastapi-integration-0.1.2/fastapi_integration/common.py
+-rw-rw-rw-   0        0        0     3505 2023-05-13 08:58:12.000000 fastapi-integration-0.1.2/fastapi_integration/config.py
+-rw-rw-rw-   0        0        0     5227 2023-05-12 16:43:57.000000 fastapi-integration-0.1.2/fastapi_integration/db.py
+-rw-rw-rw-   0        0        0      909 2023-05-12 16:11:09.000000 fastapi-integration-0.1.2/fastapi_integration/dependencies.py
+-rw-rw-rw-   0        0        0     1018 2023-05-12 16:07:33.000000 fastapi-integration-0.1.2/fastapi_integration/exceptions.py
+-rw-rw-rw-   0        0        0      603 2023-05-12 16:07:52.000000 fastapi-integration-0.1.2/fastapi_integration/features.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.848580 fastapi-integration-0.1.2/fastapi_integration/generic/
+-rw-rw-rw-   0        0        0        0 2023-04-01 15:15:50.000000 fastapi-integration-0.1.2/fastapi_integration/generic/__init__.py
+-rw-rw-rw-   0        0        0     8968 2023-05-12 15:17:57.000000 fastapi-integration-0.1.2/fastapi_integration/generic/crud.py
+-rw-rw-rw-   0        0        0        0 2023-04-01 12:17:01.000000 fastapi-integration-0.1.2/fastapi_integration/generic/views.py
+-rw-rw-rw-   0        0        0     2635 2023-05-12 16:08:42.000000 fastapi-integration-0.1.2/fastapi_integration/models.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.851580 fastapi-integration-0.1.2/fastapi_integration/orm/
+-rw-rw-rw-   0        0        0        0 2023-04-01 15:15:48.000000 fastapi-integration-0.1.2/fastapi_integration/orm/__init__.py
+-rw-rw-rw-   0        0        0    10300 2023-05-10 14:45:33.000000 fastapi-integration-0.1.2/fastapi_integration/orm/base.py
+-rw-rw-rw-   0        0        0      242 2023-05-12 16:45:11.000000 fastapi-integration-0.1.2/fastapi_integration/orm/models.py
+-rw-rw-rw-   0        0        0    13436 2023-05-10 13:51:16.000000 fastapi-integration-0.1.2/fastapi_integration/orm/queries.py
+-rw-rw-rw-   0        0        0     1251 2023-05-08 17:22:39.000000 fastapi-integration-0.1.2/fastapi_integration/orm/signals.py
+-rw-rw-rw-   0        0        0        0 2023-04-04 13:39:29.000000 fastapi-integration-0.1.2/fastapi_integration/orm/transaction.py
+-rw-rw-rw-   0        0        0      985 2023-05-07 14:59:54.000000 fastapi-integration-0.1.2/fastapi_integration/orm/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.851580 fastapi-integration-0.1.2/fastapi_integration/utils/
+-rw-rw-rw-   0        0        0        0 2023-04-01 15:15:47.000000 fastapi-integration-0.1.2/fastapi_integration/utils/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.843580 fastapi-integration-0.1.2/fastapi_integration.egg-info/
+-rw-rw-rw-   0        0        0      301 2023-05-13 16:03:23.000000 fastapi-integration-0.1.2/fastapi_integration.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1281 2023-05-13 16:03:23.000000 fastapi-integration-0.1.2/fastapi_integration.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 16:03:23.000000 fastapi-integration-0.1.2/fastapi_integration.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       94 2023-05-13 16:03:23.000000 fastapi-integration-0.1.2/fastapi_integration.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       35 2023-05-13 16:03:23.000000 fastapi-integration-0.1.2/fastapi_integration.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 16:03:23.854580 fastapi-integration-0.1.2/setup.cfg
+-rw-rw-rw-   0        0        0      612 2023-05-13 16:02:38.000000 fastapi-integration-0.1.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.852579 fastapi-integration-0.1.2/tests/
+-rw-rw-rw-   0        0        0        0 2023-05-10 12:42:06.000000 fastapi-integration-0.1.2/tests/__init__.py
+-rw-rw-rw-   0        0        0      374 2023-05-12 15:00:58.000000 fastapi-integration-0.1.2/tests/base.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:03:23.853580 fastapi-integration-0.1.2/tests/query/
+-rw-rw-rw-   0        0        0        0 2023-04-06 11:11:49.000000 fastapi-integration-0.1.2/tests/query/__init__.py
+-rw-rw-rw-   0        0        0    10030 2023-05-13 08:59:48.000000 fastapi-integration-0.1.2/tests/query/test_complex.py
+-rw-rw-rw-   0        0        0     7270 2023-05-09 16:07:05.000000 fastapi-integration-0.1.2/tests/query/test_simple.py
```

### Comparing `fastapi-integration-0.1.1/README.md` & `fastapi-integration-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/examples/main.py` & `fastapi-integration-0.1.2/examples/main.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/__init__.py` & `fastapi-integration-0.1.2/fastapi_integration/__init__.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/admin/__init__.py` & `fastapi-integration-0.1.2/fastapi_integration/admin/__init__.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/admin/generator.py` & `fastapi-integration-0.1.2/fastapi_integration/admin/generator.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/auth/__init__.py` & `fastapi-integration-0.1.2/fastapi_integration/auth/__init__.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/auth/routers.py` & `fastapi-integration-0.1.2/fastapi_integration/auth/routers.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/auth/schemas.py` & `fastapi-integration-0.1.2/fastapi_integration/auth/schemas.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/auth/utils.py` & `fastapi-integration-0.1.2/fastapi_integration/auth/utils.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/config.py` & `fastapi-integration-0.1.2/fastapi_integration/config.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/db.py` & `fastapi-integration-0.1.2/fastapi_integration/db.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/dependencies.py` & `fastapi-integration-0.1.2/fastapi_integration/dependencies.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/exceptions.py` & `fastapi-integration-0.1.2/fastapi_integration/exceptions.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/features.py` & `fastapi-integration-0.1.2/fastapi_integration/features.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/generic/crud.py` & `fastapi-integration-0.1.2/fastapi_integration/generic/crud.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/models.py` & `fastapi-integration-0.1.2/fastapi_integration/models.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/orm/base.py` & `fastapi-integration-0.1.2/fastapi_integration/orm/base.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/orm/queries.py` & `fastapi-integration-0.1.2/fastapi_integration/orm/queries.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/orm/signals.py` & `fastapi-integration-0.1.2/fastapi_integration/orm/signals.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration/orm/utils.py` & `fastapi-integration-0.1.2/fastapi_integration/orm/utils.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/fastapi_integration.egg-info/SOURCES.txt` & `fastapi-integration-0.1.2/fastapi_integration.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/setup.py` & `fastapi-integration-0.1.2/setup.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="fastapi-integration",
-    version="0.1.1",
+    version="0.1.2",
     author="Mani Mozaffar",
     author_email="mani.mozaffar@gmail.com",
     description="A PyPI package for simplifying FastAPI-ORM integration",
     packages=find_packages(),
     install_requires=[
         "fastapi",
         "asyncpg",
```

### Comparing `fastapi-integration-0.1.1/tests/query/test_complex.py` & `fastapi-integration-0.1.2/tests/query/test_complex.py`

 * *Files identical despite different names*

### Comparing `fastapi-integration-0.1.1/tests/query/test_simple.py` & `fastapi-integration-0.1.2/tests/query/test_simple.py`

 * *Files identical despite different names*

