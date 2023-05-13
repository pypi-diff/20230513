# Comparing `tmp/pyfirebird-0.0.42.tar.gz` & `tmp/pyfirebird-0.0.43.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyfirebird-0.0.42.tar", last modified: Tue May  9 06:43:04 2023, max compression
+gzip compressed data, was "pyfirebird-0.0.43.tar", last modified: Sat May 13 05:37:33 2023, max compression
```

## Comparing `pyfirebird-0.0.42.tar` & `pyfirebird-0.0.43.tar`

### file list

```diff
@@ -1,65 +1,65 @@
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      368 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/PKG-INFO
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        8 2023-04-30 05:34:25.000000 pyfirebird-0.0.42/README.md
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       38 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/setup.cfg
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     1301 2023-05-09 06:43:01.000000 pyfirebird-0.0.42/setup.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.966431 pyfirebird-0.0.42/src/
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.966431 pyfirebird-0.0.42/src/firebird/
--rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)      169 2023-04-30 06:39:02.000000 pyfirebird-0.0.42/src/firebird/__init__.py
--rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)    10313 2023-05-09 05:29:15.000000 pyfirebird-0.0.42/src/firebird/base.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.966431 pyfirebird-0.0.42/src/firebird/cmd_tools/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-04-30 05:45:15.000000 pyfirebird-0.0.42/src/firebird/cmd_tools/__init__.py
--rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     2903 2023-05-07 02:10:48.000000 pyfirebird-0.0.42/src/firebird/cmd_tools/executor.py
--rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     4964 2023-05-05 03:26:12.000000 pyfirebird-0.0.42/src/firebird/cmd_tools/executor_impl.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      649 2023-05-06 21:14:34.000000 pyfirebird-0.0.42/src/firebird/cmd_tools/fbconsole.py
--rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     3083 2023-05-09 02:04:29.000000 pyfirebird-0.0.42/src/firebird/cmd_tools/pipeline.py
--rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     2590 2023-05-09 06:26:30.000000 pyfirebird-0.0.42/src/firebird/cmd_tools/pipeline_impl.py
--rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     2972 2023-04-30 05:32:50.000000 pyfirebird-0.0.42/src/firebird/rabbitmq.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebird/utils/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       60 2023-05-05 02:58:25.000000 pyfirebird-0.0.42/src/firebird/utils/__init__.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     4359 2023-05-05 02:56:50.000000 pyfirebird-0.0.42/src/firebird/utils/checkpoint.py
--rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     6340 2023-05-09 06:14:51.000000 pyfirebird-0.0.42/src/firebird/zkdb.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-06 20:57:08.000000 pyfirebird-0.0.42/src/firebirdconsole/__init__.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/firebirdconsole/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-06 20:05:23.000000 pyfirebird-0.0.42/src/firebirdconsole/firebirdconsole/__init__.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      407 2023-05-06 20:05:23.000000 pyfirebird-0.0.42/src/firebirdconsole/firebirdconsole/asgi.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     3803 2023-05-07 02:13:47.000000 pyfirebird-0.0.42/src/firebirdconsole/firebirdconsole/settings.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      836 2023-05-06 20:43:13.000000 pyfirebird-0.0.42/src/firebirdconsole/firebirdconsole/urls.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      407 2023-05-06 20:05:23.000000 pyfirebird-0.0.42/src/firebirdconsole/firebirdconsole/wsgi.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/ui/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-06 20:06:08.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/__init__.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       63 2023-05-06 20:06:08.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/admin.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      152 2023-05-06 20:35:46.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/apps.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/ui/migrations/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-06 20:06:08.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/migrations/__init__.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       57 2023-05-06 20:06:08.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/models.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.966431 pyfirebird-0.0.42/src/firebirdconsole/ui/static/
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/ui/static/images/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)   126365 2023-05-04 00:03:29.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/static/images/logo.jpeg
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/ui/static/js-bundle/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)  1549452 2023-05-09 06:41:38.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/static/js-bundle/home.js
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)  1549361 2023-05-09 06:16:02.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/static/js-bundle/pipeline.js
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/ui/templates/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     3817 2023-05-08 02:11:53.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/templates/application.html
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      217 2023-05-06 20:12:44.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/templates/index.html
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/ui/templatetags/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 00:25:05.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/templatetags/__init__.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      639 2023-05-09 00:25:31.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/templatetags/app_filters.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       60 2023-05-06 20:06:08.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/tests.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      372 2023-05-09 03:57:30.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/urls.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      571 2023-05-08 02:38:33.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/view_tools.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/ui/views/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       54 2023-05-09 04:03:37.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/views/__init__.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/firebirdconsole/ui/views/apis/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       48 2023-05-09 04:06:17.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/views/apis/__init__.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     1682 2023-05-09 05:33:17.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/views/apis/main.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      288 2023-05-09 00:32:38.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/views/home.py
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      387 2023-05-09 04:03:49.000000 pyfirebird-0.0.42/src/firebirdconsole/ui/views/pipeline.py
-drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 06:43:04.970431 pyfirebird-0.0.42/src/pyfirebird.egg-info/
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      368 2023-05-09 06:43:04.000000 pyfirebird-0.0.42/src/pyfirebird.egg-info/PKG-INFO
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     1709 2023-05-09 06:43:04.000000 pyfirebird-0.0.42/src/pyfirebird.egg-info/SOURCES.txt
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        1 2023-05-09 06:43:04.000000 pyfirebird-0.0.42/src/pyfirebird.egg-info/dependency_links.txt
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      152 2023-05-09 06:43:04.000000 pyfirebird-0.0.42/src/pyfirebird.egg-info/entry_points.txt
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       70 2023-05-09 06:43:04.000000 pyfirebird-0.0.42/src/pyfirebird.egg-info/requires.txt
--rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       25 2023-05-09 06:43:04.000000 pyfirebird-0.0.42/src/pyfirebird.egg-info/top_level.txt
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.121022 pyfirebird-0.0.43/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      368 2023-05-13 05:37:33.121022 pyfirebird-0.0.43/PKG-INFO
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        8 2023-04-30 05:34:25.000000 pyfirebird-0.0.43/README.md
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       38 2023-05-13 05:37:33.121022 pyfirebird-0.0.43/setup.cfg
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     1301 2023-05-13 05:28:19.000000 pyfirebird-0.0.43/setup.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.113022 pyfirebird-0.0.43/src/
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.113022 pyfirebird-0.0.43/src/firebird/
+-rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)      169 2023-04-30 06:39:02.000000 pyfirebird-0.0.43/src/firebird/__init__.py
+-rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)    11544 2023-05-13 05:36:52.000000 pyfirebird-0.0.43/src/firebird/base.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.113022 pyfirebird-0.0.43/src/firebird/cmd_tools/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-04-30 05:45:15.000000 pyfirebird-0.0.43/src/firebird/cmd_tools/__init__.py
+-rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     2903 2023-05-07 02:10:48.000000 pyfirebird-0.0.43/src/firebird/cmd_tools/executor.py
+-rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     4964 2023-05-05 03:26:12.000000 pyfirebird-0.0.43/src/firebird/cmd_tools/executor_impl.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      649 2023-05-06 21:14:34.000000 pyfirebird-0.0.43/src/firebird/cmd_tools/fbconsole.py
+-rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     3083 2023-05-09 02:04:29.000000 pyfirebird-0.0.43/src/firebird/cmd_tools/pipeline.py
+-rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     2590 2023-05-09 06:26:30.000000 pyfirebird-0.0.43/src/firebird/cmd_tools/pipeline_impl.py
+-rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     2972 2023-04-30 05:32:50.000000 pyfirebird-0.0.43/src/firebird/rabbitmq.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.113022 pyfirebird-0.0.43/src/firebird/utils/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       60 2023-05-05 02:58:25.000000 pyfirebird-0.0.43/src/firebird/utils/__init__.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     4359 2023-05-05 02:56:50.000000 pyfirebird-0.0.43/src/firebird/utils/checkpoint.py
+-rw-r--r--   0 stonezhong  (1000) stonezhong  (1000)     6340 2023-05-09 06:14:51.000000 pyfirebird-0.0.43/src/firebird/zkdb.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.113022 pyfirebird-0.0.43/src/firebirdconsole/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-06 20:57:08.000000 pyfirebird-0.0.43/src/firebirdconsole/__init__.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/firebirdconsole/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-06 20:05:23.000000 pyfirebird-0.0.43/src/firebirdconsole/firebirdconsole/__init__.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      407 2023-05-06 20:05:23.000000 pyfirebird-0.0.43/src/firebirdconsole/firebirdconsole/asgi.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     3803 2023-05-07 02:13:47.000000 pyfirebird-0.0.43/src/firebirdconsole/firebirdconsole/settings.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      836 2023-05-06 20:43:13.000000 pyfirebird-0.0.43/src/firebirdconsole/firebirdconsole/urls.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      407 2023-05-06 20:05:23.000000 pyfirebird-0.0.43/src/firebirdconsole/firebirdconsole/wsgi.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/ui/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-06 20:06:08.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/__init__.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       63 2023-05-06 20:06:08.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/admin.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      152 2023-05-06 20:35:46.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/apps.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/ui/migrations/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-06 20:06:08.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/migrations/__init__.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       57 2023-05-06 20:06:08.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/models.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.113022 pyfirebird-0.0.43/src/firebirdconsole/ui/static/
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/ui/static/images/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)   126365 2023-05-04 00:03:29.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/static/images/logo.jpeg
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/ui/static/js-bundle/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)  1549452 2023-05-09 06:41:38.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/static/js-bundle/home.js
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)  1549361 2023-05-09 06:16:02.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/static/js-bundle/pipeline.js
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/ui/templates/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     3817 2023-05-08 02:11:53.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/templates/application.html
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      217 2023-05-06 20:12:44.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/templates/index.html
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/ui/templatetags/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-09 00:25:05.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/templatetags/__init__.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      639 2023-05-09 00:25:31.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/templatetags/app_filters.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       60 2023-05-06 20:06:08.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/tests.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      372 2023-05-09 03:57:30.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/urls.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      571 2023-05-08 02:38:33.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/view_tools.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/ui/views/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       54 2023-05-09 04:03:37.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/views/__init__.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.117022 pyfirebird-0.0.43/src/firebirdconsole/ui/views/apis/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       48 2023-05-09 04:06:17.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/views/apis/__init__.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     1682 2023-05-09 05:33:17.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/views/apis/main.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      288 2023-05-09 00:32:38.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/views/home.py
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      387 2023-05-09 04:03:49.000000 pyfirebird-0.0.43/src/firebirdconsole/ui/views/pipeline.py
+drwxrwxr-x   0 stonezhong  (1000) stonezhong  (1000)        0 2023-05-13 05:37:33.121022 pyfirebird-0.0.43/src/pyfirebird.egg-info/
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      368 2023-05-13 05:37:33.000000 pyfirebird-0.0.43/src/pyfirebird.egg-info/PKG-INFO
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)     1709 2023-05-13 05:37:33.000000 pyfirebird-0.0.43/src/pyfirebird.egg-info/SOURCES.txt
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)        1 2023-05-13 05:37:33.000000 pyfirebird-0.0.43/src/pyfirebird.egg-info/dependency_links.txt
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)      152 2023-05-13 05:37:33.000000 pyfirebird-0.0.43/src/pyfirebird.egg-info/entry_points.txt
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       70 2023-05-13 05:37:33.000000 pyfirebird-0.0.43/src/pyfirebird.egg-info/requires.txt
+-rw-rw-r--   0 stonezhong  (1000) stonezhong  (1000)       25 2023-05-13 05:37:33.000000 pyfirebird-0.0.43/src/pyfirebird.egg-info/top_level.txt
```

### Comparing `pyfirebird-0.0.42/setup.py` & `pyfirebird-0.0.43/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # The text of the README file
 with open(os.path.join(HERE, "README.md"), "r") as f:
     README = f.read()
 
 # This call to setup() does all the work
 setup(
     name="pyfirebird",
-    version="0.0.42",
+    version="0.0.43",
     description="Streaming Data Processing Framework",
     long_description=README,
     long_description_content_type="text/markdown",
     url="https://github.com/stonezhong/firebird",
     author="Stone Zhong",
     author_email="stonezhong@hotmail.com",
     license="MIT",
```

### Comparing `pyfirebird-0.0.42/src/firebird/base.py` & `pyfirebird-0.0.43/src/firebird/base.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 from abc import ABC, abstractmethod
 from typing import List, Any, Optional, Dict, Set, Union, Tuple
 from enum import Enum
-from queue import PriorityQueue, Empty
-from collections import deque
+from multiprocessing.sharedctypes import Synchronized
 
 from firebird.rabbitmq import RabbitMQ
 ########################################################################
 # Node:         a node of a pipeline
 # Sink:         a node without output ports
 # Generator:    a node without input ports
 # Port:         input port can connect to output port
@@ -16,96 +15,107 @@
 
 DEFAULT_INPUT_PORT_ID   = "input"
 DEFAULT_OUTPUT_PORT_ID  = "output"
 
 class PortType(Enum):
     INPUT = 1
     OUTPUT = 2
-
-class _PORT_DICT:
-    def __init__(self, v):
-        self.v = v
-        for port_name, port in v.items():
-            setattr(self, port_name, port)
-    
-    def __getitem__(self, key):
-        return self.v[key]
-    
-    
     
 class Node(ABC):
     # Each input port has a unique name among input ports
     # Each output port has a unique name among output ports
     # Sink does not have output ports
     # Source does not have input ports
     def __init__(self, 
         *, 
         id:str,
         pipeline:"Pipeline", 
         input_port_ids:List[str]=[DEFAULT_INPUT_PORT_ID], 
         output_port_ids:List[str]=[DEFAULT_OUTPUT_PORT_ID],
+        title:str="",
         description:str="",
     ):
         # validate input port ids and output port ids
         all_port_id_set = set(input_port_ids + output_port_ids)
         if len(all_port_id_set) < len(input_port_ids) + len(output_port_ids):
             raise Exception(f"Duplicate port ids found!")
 
         self._ports_dict:Dict[str, "Port"] = {}
-        self.id = id
-        self.pipeline = pipeline
-        self.description = description
+        self._id:str = id
+        self._pipeline:"Pipeline" = pipeline
+        self._description:str = description
+        if title:
+            self._title = title
+        else:
+            self._title = id
         
-        self._input_port_ids = tuple(input_port_ids)
-        self._output_port_ids = tuple(output_port_ids)
+        self._input_port_ids:Tuple["Node"] = tuple(input_port_ids)
+        self._output_port_ids:Tuple["Node"] = tuple(output_port_ids)
 
         for port_id in input_port_ids:
             self._ports_dict[port_id] = Port(PortType.INPUT, port_id, self)
 
         for port_id in output_port_ids:
             self._ports_dict[port_id] = Port(PortType.OUTPUT, port_id, self)
         
         pipeline._add_node(self)
     
     def to_json(self):
         ret = {
             "id": self.id,
+            "title": self.title,
             "description": self.description,
             "ports": [port.to_json() for port in self._ports_dict.values()]
         }
         return ret
     
     def __getitem__(self, port_id:str) -> Optional["Port"]:
-        return self.get_port(port_id)
+        return self._get_port(port_id)
+
+    @property
+    def id(self) -> str:
+        return self._id
+
+    @property
+    def pipeline(self) -> "Pipeline":
+        return self._pipeline
+
+    @property
+    def description(self) -> str:
+        return self._description
+
+    @property
+    def title(self) -> str:
+        return self._title
 
     @property
-    def input_port_ids(self):
+    def input_port_ids(self) -> Tuple["Node"]:
         return self._input_port_ids
 
     @property
-    def output_port_ids(self):
+    def output_port_ids(self) -> Tuple["Node"]:
         return self._output_port_ids
     
     @property
-    def input(self):
+    def input(self) -> Optional["Port"]:
         # return default input port
-        return self.get_port(DEFAULT_INPUT_PORT_ID)
+        return self._get_port(DEFAULT_INPUT_PORT_ID)
     
     @property
-    def output(self):
+    def output(self) -> Optional["Port"]:
         # return default output port
-        return self.get_port(DEFAULT_OUTPUT_PORT_ID)
+        return self._get_port(DEFAULT_OUTPUT_PORT_ID)
    
-    def get_port(self, id:str) -> Optional["Port"]:
+    def _get_port(self, id:str) -> Optional["Port"]:
         # get input port by name
         return self._ports_dict.get(id)
 
     @abstractmethod
-    def on_message(self, name:str, data:Any):
-        # data arrives form input port with port name
+    def on_message(self, port_id:str, data:Any):
+        # data arrives form input port with port_id
         pass
 
     def __lshift__(self, other:Union["Node", "Port", Tuple[Union["Node", "Port"]], List[Union["Node", "Port"]]]):
         # for self << other
         assert other is not None
         if isinstance(other, tuple) or isinstance(other, list):
             for t in other:
@@ -145,72 +155,102 @@
         else:
             assert isinstance(other, Node)
             dst = other.input
         
         src._connect(dst)
     
     def emit(self, json_data:Any, port_id:str=DEFAULT_OUTPUT_PORT_ID):
-        self.get_port(port_id).emit(json_data)
+        self._get_port(port_id).emit(json_data)
     
     def show_info(self, prefix=""):
         print(f"{prefix}node: id={self.id}")
         for port_id in self.input_port_ids:
-            self.get_port(port_id).show_info(prefix=prefix+"    ")
+            self._get_port(port_id).show_info(prefix=prefix+"    ")
         for port_id in self.output_port_ids:
-            self.get_port(port_id).show_info(prefix=prefix+"    ")
+            self._get_port(port_id).show_info(prefix=prefix+"    ")
     
     def is_generator(self):
         return isinstance(self, Generator)
 
 class Sink(Node):
     def __init__(self, 
         *,
         id:str,
         pipeline:"Pipeline", 
         input_port_ids:List[str]=[DEFAULT_INPUT_PORT_ID],
+        title:str="",
         description:str="",
     ):
-        super().__init__(id=id, pipeline=pipeline, input_port_ids=input_port_ids, output_port_ids=[], description=description)
+        super().__init__(
+            id=id, 
+            pipeline=pipeline, 
+            input_port_ids=input_port_ids, 
+            output_port_ids=[], 
+            title=title,
+            description=description
+        )
 
 class Generator(Node):
     def __init__(self, 
         *,
         id:str,
         pipeline:"Pipeline", 
         output_port_ids:List[str]=[DEFAULT_OUTPUT_PORT_ID],
+        title:str="",
         description:str="",
     ):
-        super().__init__(id=id, pipeline=pipeline, input_port_ids=[], output_port_ids=output_port_ids, description=description)
+        super().__init__(
+            id=id, 
+            pipeline=pipeline, 
+            input_port_ids=[], 
+            output_port_ids=output_port_ids,
+            title=title,
+            description=description
+        )
 
     def on_message(self, name:str, data:Any):
         raise Exception("Generator cannot process data")
 
     @abstractmethod
-    def pump(self, quit_requested):
+    def pump(self, quit_requested: Synchronized):
         """
         Let the source to collect data and emit data
+
+        quit_requested: a boolean shared value
         """
         pass
 
 
 class Port:
     def __init__(self, type:PortType, id:str, owner:Node):
-        self.type:PortType  = type
-        self.id:str         = id
-        self.owner:Node     = owner
+        self._id:str        = id
+        self._type:PortType = type
+        self._owner:Node    = owner
         self._connected_ports:Set["Port"] = set()
 
     def to_json(self):
         ret = {
+            "id": self.id,
             "type": self.type.name,
-            "connected_ports": [],
+            "connected_ports": [f"{port.owner.id}:{port.id}" for port in self._connected_ports],
         }
-        ret["connected_ports"].extend([f"{port.owner.id}:{port.id}" for port in self._connected_ports])
         return ret
-    
+
+    @property
+    def id(self) -> str:
+        return self._id
+
+    @property
+    def type(self) -> PortType:
+        return self._type
+
+    @property
+    def owner(self) -> Node:
+        return self._owner
+
     def __lshift__(self, other:Union["Port", Tuple["Port"], List["Port"]]):
         # for self << other
         assert other is not None
         if isinstance(other, tuple) or isinstance(other, list):
             for t in other:
                 t._connect(self)
             return other
@@ -284,29 +324,46 @@
         else:
             connect_str = f"to: {t}"
         print(f"{prefix}port: id={self.id}, type={self.type}, {connect_str}")
 
 
     
 class Pipeline:
-    def __init__(self, *, id:str, mq:RabbitMQ, description:str=""):
-        self.id = id
-        self.description = description
-        self.mq = mq
+    def __init__(self, *, id:str, mq:RabbitMQ, title:str="", description:str=""):
+        self._id:str = id
+        self._description:str = description
+        if title:
+            self._title:str = title
+        else:
+            self._title:str = id
+        self._mq:RabbitMQ  = mq
         self._node_dict:Dict[str, Node] = {}
 
     def to_json(self):
         ret = {
             "id": self.id,
+            "title": self.title,
             "description": self.description,
             "nodes": [node.to_json() for node in self._node_dict.values()]
         }
         return ret
 
-    def message_loop(self, quit_requested):
+    @property
+    def id(self) -> str:
+        return self._id
+
+    @property
+    def description(self) -> str:
+        return self._description
+
+    @property
+    def title(self) -> str:
+        return self._title
+
+    def message_loop(self, quit_requested: Synchronized):
         self.mq.consume(self.on_message, quit_requested)
     
     def on_message(self, envelope):
         node = self._node_dict[envelope['to']['node']]
         node.on_message(
             envelope["to"]["port"],
             envelope["payload"]
```

### Comparing `pyfirebird-0.0.42/src/firebird/cmd_tools/executor.py` & `pyfirebird-0.0.43/src/firebird/cmd_tools/executor.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebird/cmd_tools/executor_impl.py` & `pyfirebird-0.0.43/src/firebird/cmd_tools/executor_impl.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebird/cmd_tools/fbconsole.py` & `pyfirebird-0.0.43/src/firebird/cmd_tools/fbconsole.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebird/cmd_tools/pipeline.py` & `pyfirebird-0.0.43/src/firebird/cmd_tools/pipeline.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebird/cmd_tools/pipeline_impl.py` & `pyfirebird-0.0.43/src/firebird/cmd_tools/pipeline_impl.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebird/rabbitmq.py` & `pyfirebird-0.0.43/src/firebird/rabbitmq.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebird/utils/checkpoint.py` & `pyfirebird-0.0.43/src/firebird/utils/checkpoint.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebird/zkdb.py` & `pyfirebird-0.0.43/src/firebird/zkdb.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/firebirdconsole/settings.py` & `pyfirebird-0.0.43/src/firebirdconsole/firebirdconsole/settings.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/firebirdconsole/urls.py` & `pyfirebird-0.0.43/src/firebirdconsole/firebirdconsole/urls.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/ui/static/images/logo.jpeg` & `pyfirebird-0.0.43/src/firebirdconsole/ui/static/images/logo.jpeg`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/ui/static/js-bundle/home.js` & `pyfirebird-0.0.43/src/firebirdconsole/ui/static/js-bundle/home.js`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/ui/static/js-bundle/pipeline.js` & `pyfirebird-0.0.43/src/firebirdconsole/ui/static/js-bundle/pipeline.js`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/ui/templates/application.html` & `pyfirebird-0.0.43/src/firebirdconsole/ui/templates/application.html`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/ui/templatetags/app_filters.py` & `pyfirebird-0.0.43/src/firebirdconsole/ui/templatetags/app_filters.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/ui/view_tools.py` & `pyfirebird-0.0.43/src/firebirdconsole/ui/view_tools.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/firebirdconsole/ui/views/apis/main.py` & `pyfirebird-0.0.43/src/firebirdconsole/ui/views/apis/main.py`

 * *Files identical despite different names*

### Comparing `pyfirebird-0.0.42/src/pyfirebird.egg-info/SOURCES.txt` & `pyfirebird-0.0.43/src/pyfirebird.egg-info/SOURCES.txt`

 * *Files identical despite different names*

