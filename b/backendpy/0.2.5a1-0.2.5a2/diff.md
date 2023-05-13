# Comparing `tmp/backendpy-0.2.5a1.tar.gz` & `tmp/backendpy-0.2.5a2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "backendpy-0.2.5a1.tar", last modified: Thu May 11 10:58:33 2023, max compression
+gzip compressed data, was "backendpy-0.2.5a2.tar", last modified: Sat May 13 10:57:36 2023, max compression
```

## Comparing `backendpy-0.2.5a1.tar` & `backendpy-0.2.5a2.tar`

### file list

```diff
@@ -1,50 +1,50 @@
-drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-11 10:58:33.159316 backendpy-0.2.5a1/
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1517 2022-01-24 11:39:51.000000 backendpy-0.2.5a1/LICENSE
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3810 2023-05-11 10:58:33.159316 backendpy-0.2.5a1/PKG-INFO
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     2543 2022-12-24 20:09:28.000000 backendpy-0.2.5a1/README.md
-drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-11 10:58:33.143317 backendpy-0.2.5a1/backendpy/
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)       27 2022-02-20 19:27:36.000000 backendpy-0.2.5a1/backendpy/__init__.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1965 2022-08-26 21:11:09.000000 backendpy-0.2.5a1/backendpy/app.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    10027 2023-01-02 18:54:04.000000 backendpy-0.2.5a1/backendpy/asgi.py
-drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-11 10:58:33.151316 backendpy-0.2.5a1/backendpy/cli/
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        0 2020-06-05 08:33:23.000000 backendpy-0.2.5a1/backendpy/cli/__init__.py
--rwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)    15657 2022-12-27 08:15:36.000000 backendpy-0.2.5a1/backendpy/cli/admin.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     2601 2022-12-10 12:10:57.000000 backendpy-0.2.5a1/backendpy/config.py
-drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-11 10:58:33.155316 backendpy-0.2.5a1/backendpy/data_handler/
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        0 2020-08-27 14:31:27.000000 backendpy-0.2.5a1/backendpy/data_handler/__init__.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3476 2023-01-04 01:03:30.000000 backendpy-0.2.5a1/backendpy/data_handler/data.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     5370 2023-01-03 19:42:13.000000 backendpy-0.2.5a1/backendpy/data_handler/fields.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     4609 2023-01-12 22:24:35.000000 backendpy-0.2.5a1/backendpy/data_handler/filters.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    21377 2023-04-02 12:48:01.000000 backendpy-0.2.5a1/backendpy/data_handler/validators.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     4099 2022-12-10 12:07:53.000000 backendpy-0.2.5a1/backendpy/db.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     5125 2023-01-03 03:06:50.000000 backendpy-0.2.5a1/backendpy/error.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     5129 2023-01-03 03:06:50.000000 backendpy-0.2.5a1/backendpy/exception.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3090 2022-02-27 14:42:53.000000 backendpy-0.2.5a1/backendpy/hook.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1453 2022-08-26 21:56:05.000000 backendpy-0.2.5a1/backendpy/initializer.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1598 2022-05-20 16:53:26.000000 backendpy-0.2.5a1/backendpy/logging.py
-drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-11 10:58:33.155316 backendpy-0.2.5a1/backendpy/middleware/
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)       35 2022-12-27 07:51:13.000000 backendpy-0.2.5a1/backendpy/middleware/__init__.py
-drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-11 10:58:33.155316 backendpy-0.2.5a1/backendpy/middleware/defaults/
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        0 2022-12-27 07:51:11.000000 backendpy-0.2.5a1/backendpy/middleware/defaults/__init__.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     5825 2022-12-27 08:01:32.000000 backendpy-0.2.5a1/backendpy/middleware/defaults/cors.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3973 2022-12-27 08:01:32.000000 backendpy-0.2.5a1/backendpy/middleware/middleware.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     9319 2023-01-04 01:13:10.000000 backendpy-0.2.5a1/backendpy/request.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    17355 2023-05-11 10:44:24.000000 backendpy-0.2.5a1/backendpy/response.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    13275 2023-03-20 19:22:31.000000 backendpy-0.2.5a1/backendpy/router.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     2918 2022-06-04 13:28:58.000000 backendpy-0.2.5a1/backendpy/templating.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      908 2022-05-20 16:53:26.000000 backendpy-0.2.5a1/backendpy/unittest.py
-drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-11 10:58:33.159316 backendpy-0.2.5a1/backendpy/utils/
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        0 2019-10-11 09:00:54.000000 backendpy-0.2.5a1/backendpy/utils/__init__.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      258 2022-01-23 06:37:37.000000 backendpy-0.2.5a1/backendpy/utils/bytes.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    12916 2023-05-11 09:06:30.000000 backendpy-0.2.5a1/backendpy/utils/file.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     4630 2023-01-29 02:21:14.000000 backendpy-0.2.5a1/backendpy/utils/http.py
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      477 2022-02-27 20:01:42.000000 backendpy-0.2.5a1/backendpy/utils/json.py
-drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-11 10:58:33.147317 backendpy-0.2.5a1/backendpy.egg-info/
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3810 2023-05-11 10:58:33.000000 backendpy-0.2.5a1/backendpy.egg-info/PKG-INFO
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1042 2023-05-11 10:58:33.000000 backendpy-0.2.5a1/backendpy.egg-info/SOURCES.txt
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        1 2023-05-11 10:58:33.000000 backendpy-0.2.5a1/backendpy.egg-info/dependency_links.txt
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)       55 2023-05-11 10:58:33.000000 backendpy-0.2.5a1/backendpy.egg-info/entry_points.txt
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      100 2023-05-11 10:58:33.000000 backendpy-0.2.5a1/backendpy.egg-info/requires.txt
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)       10 2023-05-11 10:58:33.000000 backendpy-0.2.5a1/backendpy.egg-info/top_level.txt
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      105 2021-09-12 18:23:47.000000 backendpy-0.2.5a1/pyproject.toml
--rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1426 2023-05-11 10:58:33.163315 backendpy-0.2.5a1/setup.cfg
+drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-13 10:57:36.810663 backendpy-0.2.5a2/
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1517 2022-01-24 11:39:51.000000 backendpy-0.2.5a2/LICENSE
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3810 2023-05-13 10:57:36.814663 backendpy-0.2.5a2/PKG-INFO
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     2543 2022-12-24 20:09:28.000000 backendpy-0.2.5a2/README.md
+drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-13 10:57:36.662669 backendpy-0.2.5a2/backendpy/
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)       27 2022-02-20 19:27:36.000000 backendpy-0.2.5a2/backendpy/__init__.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1965 2022-08-26 21:11:09.000000 backendpy-0.2.5a2/backendpy/app.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    10027 2023-01-02 18:54:04.000000 backendpy-0.2.5a2/backendpy/asgi.py
+drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-13 10:57:36.678668 backendpy-0.2.5a2/backendpy/cli/
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        0 2020-06-05 08:33:23.000000 backendpy-0.2.5a2/backendpy/cli/__init__.py
+-rwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)    15657 2022-12-27 08:15:36.000000 backendpy-0.2.5a2/backendpy/cli/admin.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     2601 2022-12-10 12:10:57.000000 backendpy-0.2.5a2/backendpy/config.py
+drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-13 10:57:36.714667 backendpy-0.2.5a2/backendpy/data_handler/
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        0 2020-08-27 14:31:27.000000 backendpy-0.2.5a2/backendpy/data_handler/__init__.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3476 2023-01-04 01:03:30.000000 backendpy-0.2.5a2/backendpy/data_handler/data.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     5370 2023-01-03 19:42:13.000000 backendpy-0.2.5a2/backendpy/data_handler/fields.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     4609 2023-01-12 22:24:35.000000 backendpy-0.2.5a2/backendpy/data_handler/filters.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    21377 2023-04-02 12:48:01.000000 backendpy-0.2.5a2/backendpy/data_handler/validators.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     4099 2022-12-10 12:07:53.000000 backendpy-0.2.5a2/backendpy/db.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     5125 2023-01-03 03:06:50.000000 backendpy-0.2.5a2/backendpy/error.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     5129 2023-01-03 03:06:50.000000 backendpy-0.2.5a2/backendpy/exception.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3090 2022-02-27 14:42:53.000000 backendpy-0.2.5a2/backendpy/hook.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1453 2022-08-26 21:56:05.000000 backendpy-0.2.5a2/backendpy/initializer.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1598 2022-05-20 16:53:26.000000 backendpy-0.2.5a2/backendpy/logging.py
+drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-13 10:57:36.738666 backendpy-0.2.5a2/backendpy/middleware/
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)       35 2022-12-27 07:51:13.000000 backendpy-0.2.5a2/backendpy/middleware/__init__.py
+drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-13 10:57:36.754665 backendpy-0.2.5a2/backendpy/middleware/defaults/
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        0 2022-12-27 07:51:11.000000 backendpy-0.2.5a2/backendpy/middleware/defaults/__init__.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     5825 2022-12-27 08:01:32.000000 backendpy-0.2.5a2/backendpy/middleware/defaults/cors.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3973 2022-12-27 08:01:32.000000 backendpy-0.2.5a2/backendpy/middleware/middleware.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     9319 2023-01-04 01:13:10.000000 backendpy-0.2.5a2/backendpy/request.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    17355 2023-05-11 10:44:24.000000 backendpy-0.2.5a2/backendpy/response.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    13275 2023-03-20 19:22:31.000000 backendpy-0.2.5a2/backendpy/router.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     2918 2022-06-04 13:28:58.000000 backendpy-0.2.5a2/backendpy/templating.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      908 2022-05-20 16:53:26.000000 backendpy-0.2.5a2/backendpy/unittest.py
+drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-13 10:57:36.798663 backendpy-0.2.5a2/backendpy/utils/
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        0 2019-10-11 09:00:54.000000 backendpy-0.2.5a2/backendpy/utils/__init__.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      258 2022-01-23 06:37:37.000000 backendpy-0.2.5a2/backendpy/utils/bytes.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)    13121 2023-05-13 10:40:37.000000 backendpy-0.2.5a2/backendpy/utils/file.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     4630 2023-01-29 02:21:14.000000 backendpy-0.2.5a2/backendpy/utils/http.py
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      477 2022-02-27 20:01:42.000000 backendpy-0.2.5a2/backendpy/utils/json.py
+drwxrwxr-x   0 hamdollahi  (1000) hamdollahi  (1000)        0 2023-05-13 10:57:36.678668 backendpy-0.2.5a2/backendpy.egg-info/
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     3810 2023-05-13 10:57:36.000000 backendpy-0.2.5a2/backendpy.egg-info/PKG-INFO
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1042 2023-05-13 10:57:36.000000 backendpy-0.2.5a2/backendpy.egg-info/SOURCES.txt
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)        1 2023-05-13 10:57:36.000000 backendpy-0.2.5a2/backendpy.egg-info/dependency_links.txt
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)       55 2023-05-13 10:57:36.000000 backendpy-0.2.5a2/backendpy.egg-info/entry_points.txt
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      100 2023-05-13 10:57:36.000000 backendpy-0.2.5a2/backendpy.egg-info/requires.txt
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)       10 2023-05-13 10:57:36.000000 backendpy-0.2.5a2/backendpy.egg-info/top_level.txt
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)      105 2021-09-12 18:23:47.000000 backendpy-0.2.5a2/pyproject.toml
+-rw-rw-r--   0 hamdollahi  (1000) hamdollahi  (1000)     1426 2023-05-13 10:57:36.818663 backendpy-0.2.5a2/setup.cfg
```

### Comparing `backendpy-0.2.5a1/LICENSE` & `backendpy-0.2.5a2/LICENSE`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/PKG-INFO` & `backendpy-0.2.5a2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: backendpy
-Version: 0.2.5a1
+Version: 0.2.5a2
 Summary: Async (ASGI) Python web framework
 Home-page: https://github.com/savangco/backendpy
 Author: Savang Co.
 Author-email: backendpy@savang.com
 License: BSD 3-Clause License
 Project-URL: Bug Tracker, https://github.com/savangco/backendpy/issues
 Project-URL: Documentation, https://backendpy.readthedocs.io
```

### Comparing `backendpy-0.2.5a1/README.md` & `backendpy-0.2.5a2/README.md`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/app.py` & `backendpy-0.2.5a2/backendpy/app.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/asgi.py` & `backendpy-0.2.5a2/backendpy/asgi.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/cli/admin.py` & `backendpy-0.2.5a2/backendpy/cli/admin.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/config.py` & `backendpy-0.2.5a2/backendpy/config.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/data_handler/data.py` & `backendpy-0.2.5a2/backendpy/data_handler/data.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/data_handler/fields.py` & `backendpy-0.2.5a2/backendpy/data_handler/fields.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/data_handler/filters.py` & `backendpy-0.2.5a2/backendpy/data_handler/filters.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/data_handler/validators.py` & `backendpy-0.2.5a2/backendpy/data_handler/validators.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/db.py` & `backendpy-0.2.5a2/backendpy/db.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/error.py` & `backendpy-0.2.5a2/backendpy/error.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/exception.py` & `backendpy-0.2.5a2/backendpy/exception.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/hook.py` & `backendpy-0.2.5a2/backendpy/hook.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/initializer.py` & `backendpy-0.2.5a2/backendpy/initializer.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/logging.py` & `backendpy-0.2.5a2/backendpy/logging.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/middleware/defaults/cors.py` & `backendpy-0.2.5a2/backendpy/middleware/defaults/cors.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/middleware/middleware.py` & `backendpy-0.2.5a2/backendpy/middleware/middleware.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/request.py` & `backendpy-0.2.5a2/backendpy/request.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/response.py` & `backendpy-0.2.5a2/backendpy/response.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/router.py` & `backendpy-0.2.5a2/backendpy/router.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/templating.py` & `backendpy-0.2.5a2/backendpy/templating.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/unittest.py` & `backendpy-0.2.5a2/backendpy/unittest.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy/utils/file.py` & `backendpy-0.2.5a2/backendpy/utils/file.py`

 * *Files 3% similar despite different names*

```diff
@@ -221,37 +221,38 @@
         (['xbm'], [(0, b'23646566696e6520')]),
         (['pbm'], [(0, b'503120'), (0, b'503109'), (0, b'50310a'), (0, b'50310d'), (0, b'503420'), (0, b'503409'),
                    (0, b'50340a'), (0, b'50340d')]),
         (['pgm'], [(0, b'503220'), (0, b'503209'), (0, b'50320a'), (0, b'50320d'), (0, b'503520'), (0, b'503509'),
                    (0, b'50350a'), (0, b'50350d')]),
         (['ppm'], [(0, b'503320'), (0, b'503309'), (0, b'50330a'), (0, b'50330d'), (0, b'503620'), (0, b'503609'),
                    (0, b'50360a'), (0, b'50360d')]),
+        (['heic'], [(8, b'6674797068656963'), (8, b'6674797068656978'), (8, b'667479706865696d'),
+                    (8, b'6674797068656973'), (8, b'667479706d696631')]),
         # video
         (['mpeg', 'mpg'], [(0, b'000001b3')]),
         (['mpeg', 'mpg', 'vob'], [(0, b'000001ba')]),
-        (['mp4'], [(0, b'000000146674797069736f6d'), (0, b'000000186674797033677035'),
-                   (0, b'0000001c667479704d534e56012900464d534e566d703432'), (8, b'6674797033677035'),
-                   (8, b'667479704d534e56'), (8, b'6674797069736f6d'), (0, b'00000018667479706d703432'),
-                   (8, b'667479706d703432')]),
-        # m4v
+        (['mp4'], [(8, b'6674797069736f6d'), (8, b'6674797033677035'), (8, b'667479704d534e56'),
+                   (8, b'667479706d703432'), (8, b'667479704d345620')]),
+        # Todo: (['m4v'], [(8, b'667479706d703432'), (8, b'667479704d345620')]),
         (['avi'], [(0, b'52494646', 16, b'415649204c495354')]),
         (['asf', 'wmv', 'wma'], [(0, b'3026b2758e66cf11a6d900aa0062ce6c')]),
-        (['mov'],
-         [(0, b'000000146674797071742020'), (8, b'6d6f6f76'), (8, b'66726565'), (8, b'6d646174'), (8, b'77696465'),
-          (8, b'706e6f74'), (8, b'736b6970'), (8, b'6674797071742020')]),
+        (['mov'], [(8, b'6674797071742020'), (8, b'6d6f6f76'), (8, b'66726565'), (8, b'6d646174'),
+                   (8, b'77696465'), (8, b'706e6f74'), (8, b'736b6970')]),
         (['3gp'], [(0, b'0000001466747970336770')]),
         (['3g2'], [(0, b'0000002066747970336770')]),
         (['flv'], [(0, b'464c5601')]),
         (['swf'], [(0, b'435753'), (0, b'465753'), (0, b'5a5753')]),
         (['ogg', 'ogv', 'oga', 'ogx'], [(0, b'4f67675300020000000000000000')]),
         (['rmvb', 'rm'], [(0, b'2e524d46')]),
         (['ivr'], [(0, b'2e524543')]),
         (['mkv'], [(0, b'1a45dfa393428288')]),
         (['webm'], [(0, b'1a45dfa3')]),
         (['ts', 'tsv', 'tsa'], [(0, b'47', 376, b'47')]),
+        (['hevc'], [(8, b'6674797068657663'), (8, b'6674797068657678'), (8, b'667479706865766d'),
+                    (8, b'6674797068657673'), (8, b'667479706d736631')]),
         # audio
         (['wave', 'wav'], [(0, b'52494646', 16, b'57415645666d7420')]),
         (['mp3'], [(0, b'494433')]),
         (['ra'], [(0, b'2e524d460000001200'), (0, b'2e7261fd00')]),
         (['midi', 'mid'], [(0, b'4d546864')]),
         (['cda'], [(0, b'52494646', 16, b'43444441666d7420')]),
         (['rmi'], [(0, b'52494646', 16, b'524d494464617461')]),
```

### Comparing `backendpy-0.2.5a1/backendpy/utils/http.py` & `backendpy-0.2.5a2/backendpy/utils/http.py`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/backendpy.egg-info/PKG-INFO` & `backendpy-0.2.5a2/backendpy.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: backendpy
-Version: 0.2.5a1
+Version: 0.2.5a2
 Summary: Async (ASGI) Python web framework
 Home-page: https://github.com/savangco/backendpy
 Author: Savang Co.
 Author-email: backendpy@savang.com
 License: BSD 3-Clause License
 Project-URL: Bug Tracker, https://github.com/savangco/backendpy/issues
 Project-URL: Documentation, https://backendpy.readthedocs.io
```

### Comparing `backendpy-0.2.5a1/backendpy.egg-info/SOURCES.txt` & `backendpy-0.2.5a2/backendpy.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `backendpy-0.2.5a1/setup.cfg` & `backendpy-0.2.5a2/setup.cfg`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = backendpy
-version = v0.2.5-alpha.1
+version = v0.2.5-alpha.2
 author = Savang Co.
 author_email = backendpy@savang.com
 description = Async (ASGI) Python web framework
 long_description = file: README.md
 long_description_content_type = text/markdown
 keywords = Backendpy, Web, Framework, Python, Async, ASGI
 license = BSD 3-Clause License
```

