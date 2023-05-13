# Comparing `tmp/pii-extract-base-0.4.0.tar.gz` & `tmp/pii-extract-base-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pii-extract-base-0.4.0.tar", last modified: Wed May 10 18:09:42 2023, max compression
+gzip compressed data, was "pii-extract-base-0.5.0.tar", last modified: Fri May 12 20:58:39 2023, max compression
```

## Comparing `pii-extract-base-0.4.0.tar` & `pii-extract-base-0.5.0.tar`

### file list

```diff
@@ -1,67 +1,67 @@
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.401250 pii-extract-base-0.4.0/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)    11357 2021-11-20 15:10:50.000000 pii-extract-base-0.4.0/LICENSE
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       25 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/MANIFEST.in
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2048 2023-05-10 18:09:42.401250 pii-extract-base-0.4.0/PKG-INFO
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2087 2023-03-20 21:07:56.000000 pii-extract-base-0.4.0/README.md
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       39 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/requirements.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-05-10 18:09:42.401250 pii-extract-base-0.4.0/setup.cfg
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2668 2023-03-20 21:07:56.000000 pii-extract-base-0.4.0/setup.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       18 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/api/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       68 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/api/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4470 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/api/file.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     9249 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/api/processor.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/app/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/app/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2234 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/app/detect.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4392 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/app/task_info.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/build/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       59 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/build/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1362 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/build/build.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/build/task/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      244 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/build/task/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4589 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/build/task/base.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1721 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/build/task/callable.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3527 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/build/task/multi.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1202 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/build/task/regex.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      238 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/defs.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/gather/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/gather/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/gather/collection/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      154 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1294 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/get.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      183 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3460 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/base.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      111 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/defs.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     6870 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/folder.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2551 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/json.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3826 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/plugin.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3094 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/utils.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     5785 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/task_collection.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2028 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/collection/utils.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/gather/parser/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       69 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/parser/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      257 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/gather/parser/defs.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     8060 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/parser/parser.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      247 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/gather/parser/utils.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/helper/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/helper/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3532 2023-03-20 21:07:56.000000 pii-extract-base-0.4.0/src/pii_extract/helper/context.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      289 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/helper/exception.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       59 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/helper/json.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       80 2023-03-22 21:59:33.000000 pii-extract-base-0.4.0/src/pii_extract/helper/logger.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      592 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/helper/normalizer.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract/helper/tasks/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/helper/tasks/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       70 2023-01-22 16:30:32.000000 pii-extract-base-0.4.0/src/pii_extract/helper/types.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1116 2023-05-10 16:02:09.000000 pii-extract-base-0.4.0/src/pii_extract/helper/utils.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:09:42.397250 pii-extract-base-0.4.0/src/pii_extract_base.egg-info/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2048 2023-05-10 18:09:42.000000 pii-extract-base-0.4.0/src/pii_extract_base.egg-info/PKG-INFO
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1858 2023-05-10 18:09:42.000000 pii-extract-base-0.4.0/src/pii_extract_base.egg-info/SOURCES.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-05-10 18:09:42.000000 pii-extract-base-0.4.0/src/pii_extract_base.egg-info/dependency_links.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      106 2023-05-10 18:09:42.000000 pii-extract-base-0.4.0/src/pii_extract_base.egg-info/entry_points.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       63 2023-05-10 18:09:42.000000 pii-extract-base-0.4.0/src/pii_extract_base.egg-info/requires.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       12 2023-05-10 18:09:42.000000 pii-extract-base-0.4.0/src/pii_extract_base.egg-info/top_level.txt
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)    11357 2021-11-20 15:10:50.000000 pii-extract-base-0.5.0/LICENSE
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       25 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/MANIFEST.in
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2048 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/PKG-INFO
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2087 2023-03-20 21:07:56.000000 pii-extract-base-0.5.0/README.md
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       39 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/requirements.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/setup.cfg
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2668 2023-03-20 21:07:56.000000 pii-extract-base-0.5.0/setup.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.664769 pii-extract-base-0.5.0/src/
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.664769 pii-extract-base-0.5.0/src/pii_extract/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       18 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.664769 pii-extract-base-0.5.0/src/pii_extract/api/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       68 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/api/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     4590 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/api/file.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     9651 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/api/processor.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/app/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/app/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2234 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/app/detect.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     4469 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/app/task_info.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/build/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       59 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/build/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1434 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/build/build.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/build/task/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      244 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/build/task/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     4589 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/build/task/base.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1721 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/build/task/callable.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3527 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/build/task/multi.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1202 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/build/task/regex.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      238 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/defs.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/gather/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/gather/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/gather/collection/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      154 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1523 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/get.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      183 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3495 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/base.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      111 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/defs.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     7096 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/folder.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2573 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/json.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3974 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/plugin.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3584 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/utils.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     6228 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/task_collection.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2033 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/collection/utils.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/gather/parser/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       69 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/gather/parser/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      257 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/gather/parser/defs.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     8163 2023-05-12 20:17:38.000000 pii-extract-base-0.5.0/src/pii_extract/gather/parser/parser.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      247 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/gather/parser/utils.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/helper/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/helper/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3532 2023-03-20 21:07:56.000000 pii-extract-base-0.5.0/src/pii_extract/helper/context.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      289 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/helper/exception.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       59 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/helper/json.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       80 2023-03-22 21:59:33.000000 pii-extract-base-0.5.0/src/pii_extract/helper/logger.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      592 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/helper/normalizer.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract/helper/tasks/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/helper/tasks/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       70 2023-01-22 16:30:32.000000 pii-extract-base-0.5.0/src/pii_extract/helper/types.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1116 2023-05-10 16:02:09.000000 pii-extract-base-0.5.0/src/pii_extract/helper/utils.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:58:39.668769 pii-extract-base-0.5.0/src/pii_extract_base.egg-info/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2048 2023-05-12 20:58:39.000000 pii-extract-base-0.5.0/src/pii_extract_base.egg-info/PKG-INFO
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1858 2023-05-12 20:58:39.000000 pii-extract-base-0.5.0/src/pii_extract_base.egg-info/SOURCES.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-05-12 20:58:39.000000 pii-extract-base-0.5.0/src/pii_extract_base.egg-info/dependency_links.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      106 2023-05-12 20:58:39.000000 pii-extract-base-0.5.0/src/pii_extract_base.egg-info/entry_points.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       63 2023-05-12 20:58:39.000000 pii-extract-base-0.5.0/src/pii_extract_base.egg-info/requires.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       12 2023-05-12 20:58:39.000000 pii-extract-base-0.5.0/src/pii_extract_base.egg-info/top_level.txt
```

### Comparing `pii-extract-base-0.4.0/LICENSE` & `pii-extract-base-0.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/PKG-INFO` & `pii-extract-base-0.5.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pii-extract-base
-Version: 0.4.0
+Version: 0.5.0
 Summary: Extraction of PII from text chunks
 Home-page: https://github.com/piisa/pii-extract-base
-Download-URL: https://github.com/piisa/pii-extract-base/tarball/v0.4.0
+Download-URL: https://github.com/piisa/pii-extract-base/tarball/v0.5.0
 Author: Paulo Villegas
 Author-email: paulo.vllgs@gmail.com
 License: Apache
 Keywords: PIISA, PII
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Development Status :: 4 - Beta
```

### Comparing `pii-extract-base-0.4.0/README.md` & `pii-extract-base-0.5.0/README.md`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/setup.py` & `pii-extract-base-0.5.0/setup.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract/api/file.py` & `pii-extract-base-0.5.0/src/pii_extract/api/file.py`

 * *Files 3% similar despite different names*

```diff
@@ -13,30 +13,31 @@
 from pii_data.types.doc.localdoc import LocalSrcDocumentFile
 
 from ..helper.types import TYPE_STR_LIST
 from ..defs import FMT_CONFIG_PLUGIN, FMT_CONFIG_TASKS
 from . import PiiProcessor
 
 
-def print_tasks(lang: str, proc: PiiProcessor, out: TextIO):
+def print_tasks(langlist: List[str], proc: PiiProcessor, out: TextIO):
     """
     Print out the list of built tasks
     """
     tw = TextWrapper(initial_indent="     ", subsequent_indent="     ", width=78)
-    print(f". Built tasks [language={lang}]", file=out)
+    print(f". Built tasks [language={','.join(langlist)}]", file=out)
     for (pii, subtype), tasklist in proc.task_info().items():
         print(f"\n {pii.name}   {subtype if subtype else ''}", file=out)
-        for n, (country, name, doc) in enumerate(tasklist):
+        for n, (lang, country, name, doc) in enumerate(tasklist):
             if n:
-                print()
-            print(f"   Country: {country}")
-            print(f"   Name: {name}")
+                print(file=out)
+            print(f"   Language: {lang}", file=out)
+            print(f"   Country: {country}", file=out)
+            print(f"   Name: {name}", file=out)
             if doc:
                 for ln in doc.splitlines():
-                    print(tw.fill(ln))
+                    print(tw.fill(ln), file=out)
 
 
 def print_stats(stats: Dict[str, Dict], out: TextIO):
     """
     Print out statistics for the detection process
     """
     print("\n. Statistics:", file=out)
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/api/processor.py` & `pii-extract-base-0.5.0/src/pii_extract/api/processor.py`

 * *Files 2% similar despite different names*

```diff
@@ -80,26 +80,28 @@
 
 # --------------------------------------------------------------------------
 
 
 class PiiProcessor:
 
     def __init__(self, config: Dict = None, skip_plugins: bool = False,
-                 debug: bool = False):
+                 languages: Iterable[str] = None, debug: bool = False):
         """
         Initialize a PII Processor object
           :param config: configuration file, possibly containing a
             "pii-extract:tasks" section and/or a "pii-extract:plugins" section
           :param skip_plugins: skip loaginf pii-extract plugins
+          :param languages: define all languages that will be used
         """
         self._debug = debug
         self._log = PiiLogger(__name__, debug)
         self._tasks = {}
         self._stats = {"num": defaultdict(int), "entities": defaultdict(int)}
         self._ptc = get_task_collection(load_plugins=not skip_plugins,
+                                        languages=languages,
                                         config=config, debug=debug)
 
 
     def __repr__(self) -> str:
         return f"<PiiProcessor #{len(self._ptc)}>"
 
 
@@ -126,14 +128,15 @@
          :param lang: language to build tasks for
          :param country: countri(es) to build task for; if unspecified all
             possible countries will be built
          :param tasks: a specific set of pii types to build detectors for
             (otherwise build all available types)
          :param add_any: when setting a specific lang and/or country, add also
             tasks valid for "any"
+         :return: the number of tasks obtained
         """
         # Sanitize input
         lang = lang.lower() if lang else None
         self._log(". Build tasks: %s", lang)
         if isinstance(country, str):
             country = [country]
         self._country = [c.lower() for c in country] if country else None
@@ -144,33 +147,41 @@
         return len(self._tasks[lang])
 
 
     def task_info(self, lang: str = None) -> Dict[Tuple, Tuple]:
         """
         Return a dictionary with all the instantiated tasks:
           - keys are tuples (task id, subtype)
-          - values are lists of tuples (country, task name, task doc)
+          - values are lists of tuples (language, country, task name, task doc)
         """
         if not self._tasks:
             raise ProcException("no detector tasks have been built")
         elif lang and lang not in self._tasks:
             raise InvArgException("no detector tasks have been built for {}", lang)
 
         tasklist = self._tasks[lang] if lang else chain.from_iterable(self._tasks.values())
 
-        info = defaultdict(list)
+        out = defaultdict(list)
+        tset = set()
         for t in tasklist:
-            pii_list = t.pii_info
-            if isinstance(pii_list, PiiEntityInfo):
-                pii_list = [pii_list]
-            for pii in pii_list:
-                info[(pii.pii, pii.subtype)].append(
-                    (pii.country, t.task_info.name, t.task_info.doc)
+
+            tid = id(t)
+            if tid in tset:
+                continue
+            tset.add(tid)
+
+            pii_info_list = t.pii_info
+            if isinstance(pii_info_list, PiiEntityInfo):
+                pii_info_list = [pii_info_list]
+            for info in pii_info_list:
+                out[(info.pii, info.subtype)].append(
+                    (info.lang, info.country,
+                     t.task_info.name, t.task_info.doc)
                 )
-        return info
+        return out
 
 
     def detect_chunk(self, chunk: DocumentChunk, piic: PiiCollectionBuilder,
                      default_lang: str = None) -> int:
         """
         Process a document chunk, calling all defined processors and performing
         PII extraction
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/app/detect.py` & `pii-extract-base-0.5.0/src/pii_extract/app/detect.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract/app/task_info.py` & `pii-extract-base-0.5.0/src/pii_extract/app/task_info.py`

 * *Files 2% similar despite different names*

```diff
@@ -48,17 +48,20 @@
 
 def task_info(args: argparse.Namespace, out: TextIO):
     """
     Show info about tasks
     """
     config = load_config(args.config) if args.config else None
     proc = PiiProcessor(config=config, skip_plugins=args.skip_plugins,
-                        debug=args.debug)
-    proc.build_tasks(args.lang, args.country, pii=args.tasks,
-                     add_any=not args.strict)
+                        languages=args.lang, debug=args.debug)
+
+    for lang in args.lang or [None]:
+        proc.build_tasks(lang, args.country, pii=args.tasks,
+                         add_any=not args.strict)
+
     print_tasks(args.lang, proc, out)
 
 
 def parse_args(args: List[str]) -> argparse.Namespace:
     parser = argparse.ArgumentParser(
         description=f"Show information about usable PII tasks (version {VERSION})")
 
@@ -67,15 +70,15 @@
     c3.add_argument("--config", nargs="+",
                     help="PIISA configuration file(s) to load")
     c3.add_argument("--skip-plugins", action="store_true",
                     help="do not load pii-extract plugins")
 
     opt_com2 = argparse.ArgumentParser(add_help=False)
     c1 = opt_com2.add_argument_group('Task selection options')
-    c1.add_argument("--lang", help="language to select")
+    c1.add_argument("--lang", nargs="+", help="language(s) to select")
     c1.add_argument("--country", nargs="+", help="countries to select")
     c1.add_argument("--strict", action="store_true",
                     help="Include only tasks that comply strictly with selection")
 
 
     opt_com3 = argparse.ArgumentParser(add_help=False)
     c2 = opt_com3.add_argument_group("Other")
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/build/build.py` & `pii-extract-base-0.5.0/src/pii_extract/build/build.py`

 * *Files 11% similar despite different names*

```diff
@@ -15,14 +15,15 @@
     """
     return isinstance(obj, type) and issubclass(obj, BasePiiTask)
 
 
 def build_task(taskd: Dict) -> BasePiiTask:
     """
     Build a task object from its task definition
+      :param taskd: a task definition (i.e. a *parsed* task descriptor)
     """
     # Prepare standard arguments
     try:
         odef = taskd["obj"]
         tclass, tobj = odef["class"], odef["task"]
         base_args = {"task": taskd["info"], "pii": taskd["piid"]}
     except KeyError as e:
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/build/task/base.py` & `pii-extract-base-0.5.0/src/pii_extract/build/task/base.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract/build/task/callable.py` & `pii-extract-base-0.5.0/src/pii_extract/build/task/callable.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract/build/task/multi.py` & `pii-extract-base-0.5.0/src/pii_extract/build/task/multi.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract/build/task/regex.py` & `pii-extract-base-0.5.0/src/pii_extract/build/task/regex.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/base.py` & `pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/base.py`

 * *Files 2% similar despite different names*

```diff
@@ -22,22 +22,22 @@
     iterable of *normalized* raw task descriptors (possibly restricted to a
     given language)
     They can also reimplement language_list(), country_list() and/or
     gather_tasks(), if they can be made more efficient than the base class
     implementations.
     """
 
-    def __init__(self, debug: bool = False):
+    def __init__(self, languages: Iterable[str] = None, debug: bool = False):
         """
-          :param pkg: basename for the package
-          :param basedir: base directory where the task implementations are
+          :param languages: restrict collection to some languages
           :param debug: print out debug information
         """
         self._debug = debug
         self._country = None
+        self._lang = set(languages) if languages else None
         self._log = PiiLogger(__name__, debug)
 
 
     def language_list(self) -> List[str]:
         """
         Return all languages defined
         """
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/folder.py` & `pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/folder.py`

 * *Files 2% similar despite different names*

```diff
@@ -60,30 +60,30 @@
 # --------------------------------------------------------------------------
 
 
 class FolderTaskCollector(BaseTaskCollector):
 
     def __init__(self, pkg: str, basedir: Path, source: str,
                  version: str = None, pii_filter: List[PiiEnum] = None,
-                 debug: bool = False):
+                 languages: Iterable[str] = None, debug: bool = False):
         """
           :param pkg: basename for the package
           :param basedir: base directory where the task implementations are
           :param source: source for the tasks (vendor/organization/package)
           :param version: version for the tasks
           :param pii_filter: collect only tasks for these PII types
+          :param languages: currently unused
           :param debug: print out debug information
         """
-        super().__init__(debug=debug)
-        self.basedir = Path(basedir)
-        self._debug = debug
+        super().__init__(languages=languages, debug=debug)
         self._pkg = pkg
         self._defaults = {'source': source or pkg}
         if version:
             self._defaults['version'] = version
+        self.basedir = Path(basedir)
         self._log(".. Folder task collector (%s, version=%s): init",
                   self.__class__.__name__, version)
 
         # PII filter
         if not pii_filter:
             self._pii_filter = None
         else:
@@ -151,15 +151,19 @@
             self._log("... NO PII TASKS for %s", pkg)
 
 
     def language_list(self) -> List[str]:
         """
         Return all languages defined in the package
         """
-        return mod_subdir(self.basedir)
+        all_lang = mod_subdir(self.basedir)
+        if not self._lang:
+            return all_lang
+        else:
+            return [ln for ln in all_lang if ln in self._lang or ln == LANG_ANY]
 
 
     def country_list(self, lang: str = None) -> List[str]:
         """
         For a given language(s), return all countries with defined tasks
         """
         # A specific language
@@ -174,15 +178,15 @@
 
 
     def gather_tasks(self, lang: str = None,
                      country: str = None) -> Iterable[Dict]:
         """
         Import all task processors available for a given lang & country
         """
-        self._log(". gather-tasks lang=%s", lang)
+        self._log(".. gather-tasks lang=%s", lang)
         self._log(".. %s import from: %s/%s", self.__class__.__name__,
                   lang, country or "<all>")
         if lang is None or not isinstance(lang, str):
             if lang is None:
                 lang = self.language_list()
             for ln in lang:
                 yield from self.gather_tasks(ln, country)
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/json.py` & `pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/json.py`

 * *Files 1% similar despite different names*

```diff
@@ -33,15 +33,15 @@
             raise ConfigException("invalid task config: no task spec")
 
         fmt = task_spec.get("format")
         if fmt != FMT_CONFIG_PREFIX + FMT_CONFIG_TASKS:
             raise ConfigException("invalid format field '{}' in task spec", fmt)
 
         header = task_spec.get("header", {})
-        reformat = RawTaskDefaults(header, normalize=True)
+        reformat = RawTaskDefaults(header, normalize=True, languages=self._lang)
         rawlist = task_spec.get("tasklist", [])
         try:
             yield from reformat(rawlist)
         except Exception as e:
             raise InvArgException("error in task spec: {}", e) from e
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/plugin.py` & `pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/plugin.py`

 * *Files 6% similar despite different names*

```diff
@@ -27,35 +27,38 @@
 
 
 # --------------------------------------------------------------------------
 
 
 class PluginTaskCollector(BaseTaskCollector):
 
-    def __init__(self, config: Dict = None, debug: bool = False):
+    def __init__(self, config: Dict = None, debug: bool = False,
+                 languages: Iterable[str] = None):
         """
         Check available plugins and create an instance
          :param config: a dictionary possibly containing:
             (a) configuration for the collector (options for plugin loaders)
             (b) configuration to pass to each loader class
         """
-        super().__init__(debug=debug)
+        super().__init__(languages=languages, debug=debug)
         self._tasks = None
         self._plugins = []
 
         # Configuration for plugins
         plugin_cfg = config.get(FMT_CONFIG_PLUGIN, {}) if config else {}
 
         for entry in entry_points().get(PII_EXTRACT_PLUGIN_ID, []):
 
             # See if we have specific options to instantiate this plugin
             cfg = plugin_cfg.get(entry.name, {})
             if not cfg.get("load", True):
                 continue        # plugin is not to be activated
             options = cfg.get("options", {})
+            if self._lang:
+                options["languages"] = self._lang
 
             # Get the class for the plugin loader
             LoaderClass = entry.load()
             self._log(". load plugin: %s", entry.name)
 
             # Instantiate it
             try:
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/gather/collection/sources/utils.py` & `pii-extract-base-0.5.0/src/pii_extract/gather/collection/sources/utils.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,16 +1,19 @@
 from collections.abc import Iterable as AbcIterable
 
 from typing import Dict, Iterable
 
 from pii_data.types import PiiEnum
 
+from pii_extract.defs import LANG_ANY
 from pii_extract.build import is_pii_class
+from pii_extract.helper.utils import taskd_field
 from pii_extract.gather.parser import defs
 from pii_extract.gather.parser.utils import InvPiiTask
+from ..utils import piid_ok
 
 # ------------------------------------------------------------------------
 
 
 def normalize_rawtaskd(raw: defs.TYPE_TASKD) -> Dict:
     """
     Ensure a raw task descriptor is a dictionary with a "pii" field
@@ -58,33 +61,40 @@
 
 
 class RawTaskDefaults:
     """
     A class to add defaults to missing fields in a raw task descriptor
     """
 
-    def __init__(self, defaults: Dict = None, normalize: bool = True):
+    def __init__(self, defaults: Dict = None, normalize: bool = True,
+                 languages: Iterable[str] = None):
         """
           :param defaults: fields to add to the descriptor if they are missing
           :param normalize: ensure the descriptor is a proper dict
+          :param languages: restrict task descriptors to those languages
         """
         self._norm = normalize
+        self._lang = set(languages) if languages else None
         if defaults is None:
             defaults = {}
         self._piid = {k: v for k, v in defaults.items()
                       if k in ("lang", "country")}
         self._info = {k: v for k, v in defaults.items()
                       if k in ("source", "version")}
 
 
     def __call__(self, raw_list: Iterable[Dict]) -> Iterable[Dict]:
         """
         Normalize and add defaults to a list of tasks
         """
         for raw in raw_list:
+            if self._lang:
+                lang = raw.get("lang") or raw.get("pii", {}).get("lang")
+                if lang != LANG_ANY and lang not in self._lang:
+                    continue
             if self._norm:
                 raw = normalize_rawtaskd(raw)
             if self._info:
                 raw.update((k, v) for k,v in self._info.items() if k not in raw)
             if self._piid:
                 piid = raw["pii"]
                 if isinstance(piid, dict):      # not normalized
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/gather/collection/task_collection.py` & `pii-extract-base-0.5.0/src/pii_extract/gather/collection/task_collection.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,39 +1,48 @@
 """
 Build collections of task definitions
 """
 
-from typing import Dict, List, Iterable
+from typing import Dict, List, Iterable, Union
 
 from pii_data.helper.logger import PiiLogger
 
 from ...defs import LANG_ANY, COUNTRY_ANY
 from ...helper.utils import field_set, taskd_field, union_sets
 from ...build.task import BasePiiTask
 from ...build import build_task
 from ..parser import parse_task_descriptor
 from .sources.base import BaseTaskCollector
 from .utils import ensure_enum_list, filter_piid, TYPE_TASKENUM
 
 
+def is_lang_any(piid: Union[List, Dict]) -> bool:
+    """
+    See if a PII definition (or a list of them) is for the "any" language
+    """
+    if isinstance(piid, dict):
+        return piid["lang"] == LANG_ANY
+    else:
+        return any(t["lang"] == LANG_ANY for t in piid)
+
 
 class PiiTaskCollection:
     """
     An object holding a set of task definitions, which can then be
     instantiated into task objects
     """
 
     def __init__(self, debug: bool = False):
         """
         """
-        self.task_def = []
-        self._lang = None
-        self._countries = None
         self._log = PiiLogger(__name__, debug)
-        self._num = 0
+        self._lang = None       # languages with collected tasks
+        self._countries = None  # countries with collected tasks
+        self._built = {}        # all built tasks
+        self.task_def = []      # list of task definitions collected
 
 
     def __repr__(self) -> str:
         return f"<PiiTaskCollection #{len(self)}>"
 
 
     def __len__(self) -> int:
@@ -45,15 +54,15 @@
 
     def num(self, built: bool = False) -> int:
         """
         Return the number of tasks, either
           - the number available task definitions
           - the number of built task objects
         """
-        return self._num if built else len(self.task_def)
+        return len(self._built) if built else len(self.task_def)
 
 
     def add_collector(self, tc: BaseTaskCollector) -> int:
         """
         Fetch all raw tasks descriptors gathered by a task collector,
         convert them to task definitions and add them to the object list
         """
@@ -135,37 +144,34 @@
                 yield {"obj": taskd["obj"], "info": taskd["info"], "piid": piid}
 
 
     def build_tasks(self, lang: str = None, country: Iterable[str] = None,
                     pii: TYPE_TASKENUM = None,
                     add_any: bool = True) -> Iterable[BasePiiTask]:
         """
-        Build a list of tasks from their definitions stored in the collection.
+        Build and return a list of tasks from their definitions stored in
+        the collection.
           :param lang: select tasks to build for these languages
           :param country: select tasks to build for these countries
           :param country: select tasks to build for these PII types
           :param add_any: when restricting language/country, add also language-
              and country-independent tasks
           :return: an iterable yielding the built task objects.
 
         """
         # Get the list of tasks to build
         tasklist = self.taskdef_list(lang, country, pii=pii, add_any=add_any)
 
         # Build and return them
-        built = set()
         for td in tasklist:
 
-            # See if we have already been ask to build this task in this call
-            objid = td["obj"]["task"]
-            if objid in built:
-                continue  # we don't deliver the same task twice
-
-            # Build it
-            task = build_task(td)
+            # Define a language-specific identifier for the task
+            langid = LANG_ANY if is_lang_any(td["piid"]) else lang
+            objid = f"{langid}-{id(td['obj']['task'])}"
+
+            # Build it, if we don't have it yet
+            if objid not in self._built:
+                task = build_task(td)
+                self._built[objid] = task
 
             # Deliver it
-            if task:
-                built.add(objid)
-                yield task
-
-        self._num += len(built)
+            yield self._built[objid]
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/gather/collection/utils.py` & `pii-extract-base-0.5.0/src/pii_extract/gather/collection/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -36,15 +36,15 @@
     else:
         return [ensure_enum(pii)]
 
 
 def piid_ok(piid: Dict, lang: Set[str], country: Set[str],
             pii: Set[PiiEnum]) -> bool:
     """
-    Decide if a PII descriptor agrees with a language/country filter
+    Decide if a PII descriptor agrees with a type/language/country filter
     """
     if pii and not pii & taskd_field(piid, "pii"):
         return False
 
     if lang and not lang & taskd_field(piid, "lang"):
         return False
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/gather/parser/parser.py` & `pii-extract-base-0.5.0/src/pii_extract/gather/parser/parser.py`

 * *Files 1% similar despite different names*

```diff
@@ -184,15 +184,15 @@
         sall.add(n)
 
     return obj_data[FIELD_CLASS] + " for " + "/".join(sorted(sall))
 
 
 def _demux_field(pii_list: List[Dict], field: str) -> List[Dict]:
     """
-    Demultiplex a field that can be multiple from a PII dict
+    Demultiplex a field from a PII dict that can be multiple
     """
     out = []
     for pii in pii_list:
         value = pii.get(field)
 
         # If not a multiple field, add the instance & continue
         if not isinstance(value, (list, tuple)):
@@ -215,25 +215,27 @@
     Check the fields in a task descriptor. Complete missing fields, if possible
     Expand multiple-pii entries into separate dicts.
     """
     if not isinstance(taskd, dict):
         raise InvPiiTask("task descriptor is not a dict")
 
     try:
+        # Get the object & info dicts
         obj_data, task_info = _parse_taskdict(taskd, defaults)
         #print("\nDATA", obj_data, task_info, taskd, sep="\n")
 
-        # Traverse the PII information and build the object fields
+        # Traverse the PII information and build the PII field
         pii_data = [_parse_piidict(t, obj_data, defaults)
                     for t in taskd.get("pii")]
 
-        # Demultiplex fields than can be multiple
+        # Demultiplex PII subfields than can be multiple
         for field in ("subtype", "lang", "country"):
             pii_data = _demux_field(pii_data, field)
 
+        # If we've got a single PII element, flatten the list
         if len(pii_data) == 1:
             pii_data = pii_data[0]
 
         # Add a name for the task, if we do not have one yet
         if "name" not in task_info:
             task_info["name"] = _build_task_name(obj_data, pii_data)
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract/helper/context.py` & `pii-extract-base-0.5.0/src/pii_extract/helper/context.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract/helper/normalizer.py` & `pii-extract-base-0.5.0/src/pii_extract/helper/normalizer.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract/helper/utils.py` & `pii-extract-base-0.5.0/src/pii_extract/helper/utils.py`

 * *Files identical despite different names*

### Comparing `pii-extract-base-0.4.0/src/pii_extract_base.egg-info/PKG-INFO` & `pii-extract-base-0.5.0/src/pii_extract_base.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pii-extract-base
-Version: 0.4.0
+Version: 0.5.0
 Summary: Extraction of PII from text chunks
 Home-page: https://github.com/piisa/pii-extract-base
-Download-URL: https://github.com/piisa/pii-extract-base/tarball/v0.4.0
+Download-URL: https://github.com/piisa/pii-extract-base/tarball/v0.5.0
 Author: Paulo Villegas
 Author-email: paulo.vllgs@gmail.com
 License: Apache
 Keywords: PIISA, PII
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Development Status :: 4 - Beta
```

### Comparing `pii-extract-base-0.4.0/src/pii_extract_base.egg-info/SOURCES.txt` & `pii-extract-base-0.5.0/src/pii_extract_base.egg-info/SOURCES.txt`

 * *Files identical despite different names*

