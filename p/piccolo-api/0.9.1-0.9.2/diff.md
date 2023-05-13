# Comparing `tmp/piccolo_api-0.9.1.tar.gz` & `tmp/piccolo_api-0.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/piccolo_api-0.9.1.tar", last modified: Wed Jun 17 12:39:06 2020, max compression
+gzip compressed data, was "dist/piccolo_api-0.9.2.tar", last modified: Fri Jun 26 11:06:07 2020, max compression
```

## Comparing `piccolo_api-0.9.1.tar` & `piccolo_api-0.9.2.tar`

### file list

```diff
@@ -1,58 +1,62 @@
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/
--rw-r--r--   0 dantownsend   (501) staff       (20)     1531 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/PKG-INFO
--rw-r--r--   0 dantownsend   (501) staff       (20)      727 2020-05-24 19:48:40.000000 piccolo_api-0.9.1/README.md
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/
--rw-r--r--   0 dantownsend   (501) staff       (20)       22 2020-06-17 12:34:35.000000 piccolo_api-0.9.1/piccolo_api/__init__.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/crud/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:01.000000 piccolo_api-0.9.1/piccolo_api/crud/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)    19569 2020-06-17 10:54:43.000000 piccolo_api-0.9.1/piccolo_api/crud/endpoints.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     2819 2020-06-17 11:46:55.000000 piccolo_api-0.9.1/piccolo_api/crud/serializers.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/csp/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:01.000000 piccolo_api-0.9.1/piccolo_api/csp/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     1217 2020-05-28 07:24:01.000000 piccolo_api-0.9.1/piccolo_api/csp/middleware.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/csrf/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:01.000000 piccolo_api-0.9.1/piccolo_api/csrf/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     5002 2020-05-28 07:24:01.000000 piccolo_api-0.9.1/piccolo_api/csrf/middleware.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/jwt_auth/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:01.000000 piccolo_api-0.9.1/piccolo_api/jwt_auth/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     1498 2020-05-28 07:24:01.000000 piccolo_api-0.9.1/piccolo_api/jwt_auth/endpoints.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     3030 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/jwt_auth/middleware.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/rate_limiting/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/rate_limiting/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     4478 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/rate_limiting/middleware.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/session_auth/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/session_auth/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)      348 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/session_auth/commands.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     5509 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/session_auth/endpoints.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     2431 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/session_auth/middleware.py
--rw-r--r--   0 dantownsend   (501) staff       (20)      417 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/session_auth/piccolo_app.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/session_auth/piccolo_migrations/
--rw-r--r--   0 dantownsend   (501) staff       (20)     1776 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/session_auth/piccolo_migrations/2019-11-12T20:47:17.py
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/session_auth/piccolo_migrations/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     3322 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/session_auth/tables.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/shared/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/shared/__init__.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/shared/auth/
--rw-r--r--   0 dantownsend   (501) staff       (20)      129 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/shared/auth/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)      940 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/shared/auth/junction.py
--rw-r--r--   0 dantownsend   (501) staff       (20)      628 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/shared/auth/user.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/shared/middleware/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/shared/middleware/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)      883 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/shared/middleware/junction.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/token_auth/
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/token_auth/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     1943 2020-06-17 11:57:39.000000 piccolo_api-0.9.1/piccolo_api/token_auth/endpoints.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     3067 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/token_auth/middleware.py
--rw-r--r--   0 dantownsend   (501) staff       (20)      390 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/token_auth/piccolo_app.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api/token_auth/piccolo_migrations/
--rw-r--r--   0 dantownsend   (501) staff       (20)     1167 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/token_auth/piccolo_migrations/2019-11-18T22:24:41.py
--rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/token_auth/piccolo_migrations/__init__.py
--rw-r--r--   0 dantownsend   (501) staff       (20)     1914 2020-05-28 07:24:02.000000 piccolo_api-0.9.1/piccolo_api/token_auth/tables.py
-drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api.egg-info/
--rw-r--r--   0 dantownsend   (501) staff       (20)     1531 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api.egg-info/PKG-INFO
--rw-r--r--   0 dantownsend   (501) staff       (20)     1471 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api.egg-info/SOURCES.txt
--rw-r--r--   0 dantownsend   (501) staff       (20)        1 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api.egg-info/dependency_links.txt
--rw-r--r--   0 dantownsend   (501) staff       (20)      117 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api.egg-info/requires.txt
--rw-r--r--   0 dantownsend   (501) staff       (20)       12 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/piccolo_api.egg-info/top_level.txt
--rw-r--r--   0 dantownsend   (501) staff       (20)       38 2020-06-17 12:39:06.000000 piccolo_api-0.9.1/setup.cfg
--rw-r--r--   0 dantownsend   (501) staff       (20)     1249 2020-05-24 19:46:40.000000 piccolo_api-0.9.1/setup.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1555 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/PKG-INFO
+-rw-r--r--   0 dantownsend   (501) staff       (20)      727 2020-05-24 19:48:40.000000 piccolo_api-0.9.2/README.md
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/
+-rw-r--r--   0 dantownsend   (501) staff       (20)       22 2020-06-26 11:03:39.000000 piccolo_api-0.9.2/piccolo_api/__init__.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/crud/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:01.000000 piccolo_api-0.9.2/piccolo_api/crud/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)    20792 2020-06-26 10:57:55.000000 piccolo_api-0.9.2/piccolo_api/crud/endpoints.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)      265 2020-06-21 18:53:16.000000 piccolo_api-0.9.2/piccolo_api/crud/exceptions.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     2819 2020-06-17 11:46:55.000000 piccolo_api-0.9.2/piccolo_api/crud/serializers.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/csp/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:01.000000 piccolo_api-0.9.2/piccolo_api/csp/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1217 2020-05-28 07:24:01.000000 piccolo_api-0.9.2/piccolo_api/csp/middleware.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/csrf/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:01.000000 piccolo_api-0.9.2/piccolo_api/csrf/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     5002 2020-05-28 07:24:01.000000 piccolo_api-0.9.2/piccolo_api/csrf/middleware.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/fastapi/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-06-26 10:57:55.000000 piccolo_api-0.9.2/piccolo_api/fastapi/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)    10599 2020-06-26 10:57:55.000000 piccolo_api-0.9.2/piccolo_api/fastapi/endpoints.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/jwt_auth/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:01.000000 piccolo_api-0.9.2/piccolo_api/jwt_auth/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1498 2020-05-28 07:24:01.000000 piccolo_api-0.9.2/piccolo_api/jwt_auth/endpoints.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     3030 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/jwt_auth/middleware.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/rate_limiting/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/rate_limiting/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     4478 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/rate_limiting/middleware.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/session_auth/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/session_auth/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)      348 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/session_auth/commands.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     5509 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/session_auth/endpoints.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     2431 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/session_auth/middleware.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)      417 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/session_auth/piccolo_app.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/session_auth/piccolo_migrations/
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1776 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/session_auth/piccolo_migrations/2019-11-12T20:47:17.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/session_auth/piccolo_migrations/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     3322 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/session_auth/tables.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/shared/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/shared/__init__.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/shared/auth/
+-rw-r--r--   0 dantownsend   (501) staff       (20)      129 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/shared/auth/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)      940 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/shared/auth/junction.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)      628 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/shared/auth/user.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/shared/middleware/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/shared/middleware/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)      883 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/shared/middleware/junction.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/token_auth/
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/token_auth/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1943 2020-06-17 11:57:39.000000 piccolo_api-0.9.2/piccolo_api/token_auth/endpoints.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     3067 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/token_auth/middleware.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)      390 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/token_auth/piccolo_app.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api/token_auth/piccolo_migrations/
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1167 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/token_auth/piccolo_migrations/2019-11-18T22:24:41.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)        0 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/token_auth/piccolo_migrations/__init__.py
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1914 2020-05-28 07:24:02.000000 piccolo_api-0.9.2/piccolo_api/token_auth/tables.py
+drwxr-xr-x   0 dantownsend   (501) staff       (20)        0 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api.egg-info/
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1555 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api.egg-info/PKG-INFO
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1567 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api.egg-info/SOURCES.txt
+-rw-r--r--   0 dantownsend   (501) staff       (20)        1 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api.egg-info/dependency_links.txt
+-rw-r--r--   0 dantownsend   (501) staff       (20)      144 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api.egg-info/requires.txt
+-rw-r--r--   0 dantownsend   (501) staff       (20)       12 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/piccolo_api.egg-info/top_level.txt
+-rw-r--r--   0 dantownsend   (501) staff       (20)       38 2020-06-26 11:06:07.000000 piccolo_api-0.9.2/setup.cfg
+-rw-r--r--   0 dantownsend   (501) staff       (20)     1302 2020-06-26 10:57:55.000000 piccolo_api-0.9.2/setup.py
```

### Comparing `piccolo_api-0.9.1/PKG-INFO` & `piccolo_api-0.9.2/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: piccolo_api
-Version: 0.9.1
+Version: 0.9.2
 Summary: Utilities for using Piccolo in ASGI apps.
 Home-page: https://github.com/piccolo-orm/piccolo_api
 Author: Daniel Townsend
 Author-email: dan@dantownsend.co.uk
 License: MIT
 Description: [![Build Status](https://travis-ci.com/piccolo-orm/piccolo_api.svg?branch=master)](https://travis-ci.com/piccolo-orm/piccolo_api)
         
@@ -32,7 +32,8 @@
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Requires-Python: >=3.7.0
 Description-Content-Type: text/markdown
+Provides-Extra: fastapi
```

### Comparing `piccolo_api-0.9.1/README.md` & `piccolo_api-0.9.2/README.md`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/crud/endpoints.py` & `piccolo_api-0.9.2/piccolo_api/crud/endpoints.py`

 * *Files 4% similar despite different names*

```diff
@@ -19,40 +19,41 @@
 from piccolo.table import Table
 import pydantic
 from pydantic.error_wrappers import ValidationError
 from starlette.routing import Router, Route
 from starlette.responses import JSONResponse, Response
 from starlette.requests import Request
 
+from .exceptions import MalformedQuery
 from .serializers import create_pydantic_model, Config
 
 if t.TYPE_CHECKING:
     from piccolo.query.base import Query
     from starlette.routing import BaseRoute
 
 
 logger = logging.getLogger(__file__)
 
 
-class CustomJSONResponse(Response):
-    media_type = "application/json"
-
-
 OPERATOR_MAP = {
     "lt": LessThan,
     "lte": LessEqualThan,
     "gt": GreaterThan,
     "gte": GreaterEqualThan,
     "e": Equal,
 }
 
 
 MATCH_TYPES = ("contains", "exact", "starts", "ends")
 
 
+class CustomJSONResponse(Response):
+    media_type = "application/json"
+
+
 @dataclass
 class OrderBy:
     ascending: bool = False
     property_name: str = "id"
 
 
 @dataclass
@@ -91,14 +92,16 @@
             If True, allows a delete request to the root to delete all matching
             records. It is dangerous, so is disabled by default.
         :param page_size:
             The number of results shown on each page by default.
         """
         self.table = table
         self.page_size = page_size
+        self.read_only = read_only
+        self.allow_bulk_delete = allow_bulk_delete
 
         root_methods = ["GET"]
         if not read_only:
             root_methods += (
                 ["POST", "DELETE"] if allow_bulk_delete else ["POST"]
             )
 
@@ -132,42 +135,52 @@
     ###########################################################################
 
     @property
     def pydantic_model(self) -> t.Type[pydantic.BaseModel]:
         """
         Useful for serialising inbound data from POST and PUT requests.
         """
-        return create_pydantic_model(self.table)
+        return create_pydantic_model(
+            self.table, model_name=f"{self.table.__name__}In"
+        )
 
     @property
     def pydantic_model_output(self) -> t.Type[pydantic.BaseModel]:
         """
         Contains the default columns, which is required when exporting
         data (for example, in a GET request).
         """
-        return create_pydantic_model(self.table, include_default_columns=True)
+        return create_pydantic_model(
+            self.table,
+            include_default_columns=True,
+            model_name=f"{self.table.__name__}Output",
+        )
 
     @property
     def pydantic_model_optional(self) -> t.Type[pydantic.BaseModel]:
         """
         All fields are optional, which is useful for serialising filters,
         where a user can filter on any number of fields.
         """
         return create_pydantic_model(
-            self.table, include_default_columns=True, all_optional=True
+            self.table,
+            include_default_columns=True,
+            all_optional=True,
+            model_name=f"{self.table.__name__}Optional",
         )
 
     def pydantic_model_plural(self, include_readable=False):
         """
         This is for when we want to serialise many copies of the model.
         """
         base_model = create_pydantic_model(
             self.table,
             include_default_columns=True,
             include_readable=include_readable,
+            model_name=f"{self.table.__name__}Item",
         )
         return pydantic.create_model(
             str(self.table.__name__) + "Plural",
             __config__=Config,
             rows=(t.List[base_model], None),
         )
 
@@ -213,52 +226,58 @@
             }
             for i in self.table._meta.foreign_key_references
         ]
         return JSONResponse({"references": references})
 
     ###########################################################################
 
-    async def get_count(self, request: Request) -> JSONResponse:
+    async def get_count(self, request: Request) -> Response:
         """
         Returns the total number of rows in the table.
         """
         params = dict(request.query_params)
         split_params = self._split_params(params)
-        query = self._apply_filters(self.table.count(), split_params)
+
+        try:
+            query = self._apply_filters(self.table.count(), split_params)
+        except MalformedQuery as exception:
+            return Response(str(exception), status_code=400)
+
         count = await query.run()
         return JSONResponse({"count": count, "page_size": self.page_size})
 
     ###########################################################################
 
     async def root(self, request: Request) -> Response:
         if request.method == "GET":
             params = dict(request.query_params)
             return await self._get_all(params=params)
         elif request.method == "POST":
             data = await request.json()
             return await self._post_single(data)
         elif request.method == "DELETE":
-            return await self._delete_all()
+            params = dict(request.query_params)
+            return await self._delete_all(params=params)
         else:
             return Response(status_code=405)
 
     ###########################################################################
 
     @staticmethod
     def _split_params(params: t.Dict[str, t.Any]) -> Params:
         """
         Some parameters reference fields, and others provide instructions
         on how to perform the query (e.g. which operator to use).
 
         An example of an operator parameter is {'age__operator': 'gte'}.
 
         You can specify how to match text fields:
-        {'__name__match': 'exact'}.
+        {'name__match': 'exact'}.
 
-        Sorting is specified like: {'__sorting': '-name'}.
+        Ordering is specified like: {'__order': '-name'}.
 
         To include readable representations of foreign keys, use:
         {'__readable': 'true'}.
 
         For pagination, you can override the default page size:
         {'__page_size': 15}.
 
@@ -324,15 +343,19 @@
         Objects etc.
         """
         fields = params.fields
 
         if fields:
             model_dict = self.pydantic_model_optional(**fields).dict()
             for field_name in fields.keys():
-                value = model_dict[field_name]
+                value = model_dict.get(field_name, ...)
+                if value is ...:
+                    raise MalformedQuery(
+                        f"{field_name} isn't a valid field name."
+                    )
                 column: Column = getattr(self.table, field_name)
                 if isinstance(
                     self.table._meta.get_column_by_name(field_name),
                     (Varchar, Text),
                 ):
                     match_type = params.match_types[field_name]
                     if match_type == "exact":
@@ -349,15 +372,15 @@
                     query = query.where(
                         Where(column=column, value=value, operator=operator)
                     )
         return query
 
     async def _get_all(
         self, params: t.Optional[t.Dict[str, t.Any]] = None
-    ) -> CustomJSONResponse:
+    ) -> Response:
         """
         Get all rows - query parameters are used for filtering.
         """
         params = self._clean_data(params) if params else {}
 
         split_params = self._split_params(params)
 
@@ -369,15 +392,18 @@
             ]
             columns = self.table._meta.columns + readable_columns
             query = self.table.select(*columns)
         else:
             query = self.table.select()
 
         # Apply filters
-        query = self._apply_filters(query, split_params)
+        try:
+            query = self._apply_filters(query, split_params)
+        except MalformedQuery as exception:
+            return Response(str(exception), status_code=400)
 
         # Ordering
         order_by = split_params.order_by
         if order_by:
             column = getattr(self.table, order_by.property_name)
             query = query.order_by(column, ascending=order_by.ascending)
         else:
@@ -414,30 +440,41 @@
         """
         Adds a single row, if the id doesn't already exist.
         """
         cleaned_data = self._clean_data(data)
         try:
             model = self.pydantic_model(**cleaned_data)
         except ValidationError as exception:
-            # TODO - use exception.json()
             return Response(str(exception), status_code=400)
 
         try:
             row = self.table(**model.dict())
             response = await row.save().run()
             # Returns the id of the inserted row.
             return JSONResponse(response, status_code=201)
         except ValueError:
             return Response("Unable to save the resource.", status_code=500)
 
-    async def _delete_all(self) -> Response:
+    async def _delete_all(
+        self, params: t.Optional[t.Dict[str, t.Any]] = None
+    ) -> Response:
         """
         Deletes all rows - query parameters are used for filtering.
         """
-        await self.table.delete().run()
+        params = self._clean_data(params) if params else {}
+        split_params = self._split_params(params)
+
+        try:
+            query = self._apply_filters(
+                self.table.delete(force=True), split_params
+            )
+        except MalformedQuery as exception:
+            return Response(str(exception), status_code=400)
+
+        await query.run()
         return Response(status_code=204)
 
     ###########################################################################
 
     async def new(self, request: Request) -> CustomJSONResponse:
         """
         This endpoint is used when creating new rows in a UI. It provides
```

### Comparing `piccolo_api-0.9.1/piccolo_api/crud/serializers.py` & `piccolo_api-0.9.2/piccolo_api/crud/serializers.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/csp/middleware.py` & `piccolo_api-0.9.2/piccolo_api/csp/middleware.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/csrf/middleware.py` & `piccolo_api-0.9.2/piccolo_api/csrf/middleware.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/jwt_auth/endpoints.py` & `piccolo_api-0.9.2/piccolo_api/jwt_auth/endpoints.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/jwt_auth/middleware.py` & `piccolo_api-0.9.2/piccolo_api/jwt_auth/middleware.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/rate_limiting/middleware.py` & `piccolo_api-0.9.2/piccolo_api/rate_limiting/middleware.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/session_auth/endpoints.py` & `piccolo_api-0.9.2/piccolo_api/session_auth/endpoints.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/session_auth/middleware.py` & `piccolo_api-0.9.2/piccolo_api/session_auth/middleware.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/session_auth/piccolo_migrations/2019-11-12T20:47:17.py` & `piccolo_api-0.9.2/piccolo_api/session_auth/piccolo_migrations/2019-11-12T20:47:17.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/session_auth/tables.py` & `piccolo_api-0.9.2/piccolo_api/session_auth/tables.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/shared/auth/junction.py` & `piccolo_api-0.9.2/piccolo_api/shared/auth/junction.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/shared/auth/user.py` & `piccolo_api-0.9.2/piccolo_api/shared/auth/user.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/shared/middleware/junction.py` & `piccolo_api-0.9.2/piccolo_api/shared/middleware/junction.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/token_auth/endpoints.py` & `piccolo_api-0.9.2/piccolo_api/token_auth/endpoints.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/token_auth/middleware.py` & `piccolo_api-0.9.2/piccolo_api/token_auth/middleware.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/token_auth/piccolo_migrations/2019-11-18T22:24:41.py` & `piccolo_api-0.9.2/piccolo_api/token_auth/piccolo_migrations/2019-11-18T22:24:41.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api/token_auth/tables.py` & `piccolo_api-0.9.2/piccolo_api/token_auth/tables.py`

 * *Files identical despite different names*

### Comparing `piccolo_api-0.9.1/piccolo_api.egg-info/PKG-INFO` & `piccolo_api-0.9.2/piccolo_api.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: piccolo-api
-Version: 0.9.1
+Version: 0.9.2
 Summary: Utilities for using Piccolo in ASGI apps.
 Home-page: https://github.com/piccolo-orm/piccolo_api
 Author: Daniel Townsend
 Author-email: dan@dantownsend.co.uk
 License: MIT
 Description: [![Build Status](https://travis-ci.com/piccolo-orm/piccolo_api.svg?branch=master)](https://travis-ci.com/piccolo-orm/piccolo_api)
         
@@ -32,7 +32,8 @@
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Requires-Python: >=3.7.0
 Description-Content-Type: text/markdown
+Provides-Extra: fastapi
```

### Comparing `piccolo_api-0.9.1/piccolo_api.egg-info/SOURCES.txt` & `piccolo_api-0.9.2/piccolo_api.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -4,19 +4,22 @@
 piccolo_api.egg-info/PKG-INFO
 piccolo_api.egg-info/SOURCES.txt
 piccolo_api.egg-info/dependency_links.txt
 piccolo_api.egg-info/requires.txt
 piccolo_api.egg-info/top_level.txt
 piccolo_api/crud/__init__.py
 piccolo_api/crud/endpoints.py
+piccolo_api/crud/exceptions.py
 piccolo_api/crud/serializers.py
 piccolo_api/csp/__init__.py
 piccolo_api/csp/middleware.py
 piccolo_api/csrf/__init__.py
 piccolo_api/csrf/middleware.py
+piccolo_api/fastapi/__init__.py
+piccolo_api/fastapi/endpoints.py
 piccolo_api/jwt_auth/__init__.py
 piccolo_api/jwt_auth/endpoints.py
 piccolo_api/jwt_auth/middleware.py
 piccolo_api/rate_limiting/__init__.py
 piccolo_api/rate_limiting/middleware.py
 piccolo_api/session_auth/__init__.py
 piccolo_api/session_auth/commands.py
```

### Comparing `piccolo_api-0.9.1/setup.py` & `piccolo_api-0.9.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -27,14 +27,15 @@
     long_description_content_type="text/markdown",
     author="Daniel Townsend",
     author_email="dan@dantownsend.co.uk",
     python_requires=">=3.7.0",
     url="https://github.com/piccolo-orm/piccolo_api",
     packages=find_packages(exclude=("tests",)),
     install_requires=REQUIREMENTS,
+    extras_require={"fastapi": ["fastapi>=0.58.0"]},
     license="MIT",
     classifiers=[
         "License :: OSI Approved :: MIT License",
         "Programming Language :: Python",
         "Programming Language :: Python :: 3",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
```

