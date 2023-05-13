# Comparing `tmp/yerbamate-0.9.236.tar.gz` & `tmp/yerbamate-0.9.237.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "yerbamate-0.9.236.tar", last modified: Wed May  3 22:52:08 2023, max compression
+gzip compressed data, was "yerbamate-0.9.237.tar", last modified: Sat May 13 17:04:44 2023, max compression
```

## Comparing `yerbamate-0.9.236.tar` & `yerbamate-0.9.237.tar`

### file list

```diff
@@ -1,88 +1,88 @@
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.604120 yerbamate-0.9.236/
--rw-r--r--   0 al        (1000) al        (1001)     1079 2023-04-08 19:56:23.000000 yerbamate-0.9.236/LICENSE
--rw-r--r--   0 al        (1000) al        (1001)       29 2023-04-08 19:56:23.000000 yerbamate-0.9.236/MANIFEST.in
--rw-r--r--   0 al        (1000) al        (1001)    11582 2023-05-03 22:52:08.604120 yerbamate-0.9.236/PKG-INFO
--rw-r--r--   0 al        (1000) al        (1001)    10948 2023-04-08 19:56:23.000000 yerbamate-0.9.236/README.md
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.590121 yerbamate-0.9.236/packages/
--rw-r--r--   0 al        (1000) al        (1001)      112 2023-04-22 15:20:01.000000 yerbamate-0.9.236/packages/requirements.txt
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.591121 yerbamate-0.9.236/packages/yerbamate/
--rw-r--r--   0 al        (1000) al        (1001)      130 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/__init__.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.593121 yerbamate-0.9.236/packages/yerbamate/__pycache__/
--rw-r--r--   0 al        (1000) al        (1001)      291 2023-04-08 19:57:52.000000 yerbamate-0.9.236/packages/yerbamate/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     4470 2023-05-03 21:23:06.000000 yerbamate-0.9.236/packages/yerbamate/__pycache__/environment.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     8269 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/__pycache__/mate.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     9389 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/__pycache__/mate_cli.cpython-310.pyc
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.594121 yerbamate-0.9.236/packages/yerbamate/api/
--rw-r--r--   0 al        (1000) al        (1001)        0 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/__init__.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.594121 yerbamate-0.9.236/packages/yerbamate/api/__pycache__/
--rw-r--r--   0 al        (1000) al        (1001)      153 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     1427 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/__pycache__/mate_api.cpython-310.pyc
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.595121 yerbamate-0.9.236/packages/yerbamate/api/data/
--rw-r--r--   0 al        (1000) al        (1001)       29 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/__init__.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.596120 yerbamate-0.9.236/packages/yerbamate/api/data/__pycache__/
--rw-r--r--   0 al        (1000) al        (1001)      197 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     5655 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/__pycache__/module_manager.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)    11926 2023-05-03 21:24:59.000000 yerbamate-0.9.236/packages/yerbamate/api/data/__pycache__/module_repository.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     3316 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/__pycache__/package.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     9460 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/module_manager.py
--rw-r--r--   0 al        (1000) al        (1001)    15485 2023-05-03 21:24:50.000000 yerbamate-0.9.236/packages/yerbamate/api/data/module_repository.py
--rw-r--r--   0 al        (1000) al        (1001)     3447 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/package.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.597120 yerbamate-0.9.236/packages/yerbamate/api/data/sources/
--rw-r--r--   0 al        (1000) al        (1001)        0 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/__init__.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.597120 yerbamate-0.9.236/packages/yerbamate/api/data/sources/__pycache__/
--rw-r--r--   0 al        (1000) al        (1001)      166 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     1127 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/__pycache__/source.cpython-310.pyc
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.598121 yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/
--rw-r--r--   0 al        (1000) al        (1001)       35 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/__init__.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.599120 yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/__pycache__/
--rw-r--r--   0 al        (1000) al        (1001)      217 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     5521 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/__pycache__/io.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     5734 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/__pycache__/local.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     5573 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/io.py
--rw-r--r--   0 al        (1000) al        (1001)     5130 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/local.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.599120 yerbamate-0.9.236/packages/yerbamate/api/data/sources/remote/
--rw-r--r--   0 al        (1000) al        (1001)       37 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/remote/__init__.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.600120 yerbamate-0.9.236/packages/yerbamate/api/data/sources/remote/__pycache__/
--rw-r--r--   0 al        (1000) al        (1001)      220 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/remote/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     2132 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/remote/__pycache__/remote.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     1078 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/remote/remote.py
--rw-r--r--   0 al        (1000) al        (1001)      365 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/sources/source.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.601120 yerbamate-0.9.236/packages/yerbamate/api/data/utils/
--rw-r--r--   0 al        (1000) al        (1001)        0 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/utils/__init__.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.602120 yerbamate-0.9.236/packages/yerbamate/api/data/utils/__pycache__/
--rw-r--r--   0 al        (1000) al        (1001)      164 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/utils/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)      540 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/utils/__pycache__/exp_util.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     1035 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/utils/__pycache__/git_util.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     4487 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/api/data/utils/__pycache__/gitdir.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)      326 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/utils/exp_util.py
--rw-r--r--   0 al        (1000) al        (1001)     1197 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/utils/git_util.py
--rw-r--r--   0 al        (1000) al        (1001)     7395 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/data/utils/gitdir.py
--rw-r--r--   0 al        (1000) al        (1001)      869 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/api/mate_api.py
--rw-r--r--   0 al        (1000) al        (1001)      294 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/constants.py
--rw-r--r--   0 al        (1000) al        (1001)     5944 2023-05-03 22:51:45.000000 yerbamate-0.9.236/packages/yerbamate/environment.py
--rw-r--r--   0 al        (1000) al        (1001)     7829 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/mate.py
--rw-r--r--   0 al        (1000) al        (1001)    10611 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/mate_cli.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.603120 yerbamate-0.9.236/packages/yerbamate/utils/
--rw-r--r--   0 al        (1000) al        (1001)     1433 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/utils/__init__.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.603120 yerbamate-0.9.236/packages/yerbamate/utils/__pycache__/
--rw-r--r--   0 al        (1000) al        (1001)     2016 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/utils/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)      814 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/utils/__pycache__/bunch.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     3761 2023-04-09 10:03:11.000000 yerbamate-0.9.236/packages/yerbamate/utils/__pycache__/utils.cpython-310.pyc
--rw-r--r--   0 al        (1000) al        (1001)     2145 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/utils/bunch.py
--rw-r--r--   0 al        (1000) al        (1001)     1386 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/utils/git_url_parser.py
--rw-r--r--   0 al        (1000) al        (1001)     4419 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/utils/utils.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.604120 yerbamate-0.9.236/packages/yerbamate/yerbamate.egg-info/
--rw-r--r--   0 al        (1000) al        (1001)      601 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/yerbamate.egg-info/PKG-INFO
--rw-r--r--   0 al        (1000) al        (1001)      342 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/yerbamate.egg-info/SOURCES.txt
--rw-r--r--   0 al        (1000) al        (1001)        1 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/yerbamate.egg-info/dependency_links.txt
--rw-r--r--   0 al        (1000) al        (1001)       10 2023-04-08 19:56:23.000000 yerbamate-0.9.236/packages/yerbamate/yerbamate.egg-info/top_level.txt
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.592121 yerbamate-0.9.236/packages/yerbamate.egg-info/
--rw-r--r--   0 al        (1000) al        (1001)    11582 2023-05-03 22:52:08.000000 yerbamate-0.9.236/packages/yerbamate.egg-info/PKG-INFO
--rw-r--r--   0 al        (1000) al        (1001)     3195 2023-05-03 22:52:08.000000 yerbamate-0.9.236/packages/yerbamate.egg-info/SOURCES.txt
--rw-r--r--   0 al        (1000) al        (1001)        1 2023-05-03 22:52:08.000000 yerbamate-0.9.236/packages/yerbamate.egg-info/dependency_links.txt
--rw-r--r--   0 al        (1000) al        (1001)       82 2023-05-03 22:52:08.000000 yerbamate-0.9.236/packages/yerbamate.egg-info/requires.txt
--rw-r--r--   0 al        (1000) al        (1001)       10 2023-05-03 22:52:08.000000 yerbamate-0.9.236/packages/yerbamate.egg-info/top_level.txt
--rw-r--r--   0 al        (1000) al        (1001)      107 2023-05-03 22:52:08.605120 yerbamate-0.9.236/setup.cfg
--rw-r--r--   0 al        (1000) al        (1001)     1279 2023-05-03 22:51:53.000000 yerbamate-0.9.236/setup.py
-drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-03 22:52:08.589121 yerbamate-0.9.236/src/
--rwxr-xr-x   0 al        (1000) al        (1001)       62 2023-04-08 19:56:23.000000 yerbamate-0.9.236/src/mate
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.703398 yerbamate-0.9.237/
+-rw-r--r--   0 al        (1000) al        (1001)     1079 2023-04-08 19:56:23.000000 yerbamate-0.9.237/LICENSE
+-rw-r--r--   0 al        (1000) al        (1001)       29 2023-04-08 19:56:23.000000 yerbamate-0.9.237/MANIFEST.in
+-rw-r--r--   0 al        (1000) al        (1001)    11582 2023-05-13 17:04:44.703398 yerbamate-0.9.237/PKG-INFO
+-rw-r--r--   0 al        (1000) al        (1001)    10948 2023-04-08 19:56:23.000000 yerbamate-0.9.237/README.md
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.697399 yerbamate-0.9.237/packages/
+-rw-r--r--   0 al        (1000) al        (1001)      112 2023-04-22 15:20:01.000000 yerbamate-0.9.237/packages/requirements.txt
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.698398 yerbamate-0.9.237/packages/yerbamate/
+-rw-r--r--   0 al        (1000) al        (1001)      130 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/__init__.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.698398 yerbamate-0.9.237/packages/yerbamate/__pycache__/
+-rw-r--r--   0 al        (1000) al        (1001)      291 2023-04-08 19:57:52.000000 yerbamate-0.9.237/packages/yerbamate/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     4679 2023-05-13 16:58:41.000000 yerbamate-0.9.237/packages/yerbamate/__pycache__/environment.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     8269 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/__pycache__/mate.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     9389 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/__pycache__/mate_cli.cpython-310.pyc
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.699399 yerbamate-0.9.237/packages/yerbamate/api/
+-rw-r--r--   0 al        (1000) al        (1001)        0 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/__init__.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.699399 yerbamate-0.9.237/packages/yerbamate/api/__pycache__/
+-rw-r--r--   0 al        (1000) al        (1001)      153 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     1427 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/__pycache__/mate_api.cpython-310.pyc
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.699399 yerbamate-0.9.237/packages/yerbamate/api/data/
+-rw-r--r--   0 al        (1000) al        (1001)       29 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/__init__.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.700399 yerbamate-0.9.237/packages/yerbamate/api/data/__pycache__/
+-rw-r--r--   0 al        (1000) al        (1001)      197 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     5655 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/__pycache__/module_manager.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)    11926 2023-05-03 21:24:59.000000 yerbamate-0.9.237/packages/yerbamate/api/data/__pycache__/module_repository.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     3316 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/__pycache__/package.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     9460 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/module_manager.py
+-rw-r--r--   0 al        (1000) al        (1001)    15485 2023-05-03 21:24:50.000000 yerbamate-0.9.237/packages/yerbamate/api/data/module_repository.py
+-rw-r--r--   0 al        (1000) al        (1001)     3447 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/package.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.700399 yerbamate-0.9.237/packages/yerbamate/api/data/sources/
+-rw-r--r--   0 al        (1000) al        (1001)        0 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/__init__.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.700399 yerbamate-0.9.237/packages/yerbamate/api/data/sources/__pycache__/
+-rw-r--r--   0 al        (1000) al        (1001)      166 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     1127 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/__pycache__/source.cpython-310.pyc
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.700399 yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/
+-rw-r--r--   0 al        (1000) al        (1001)       35 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/__init__.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.700399 yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/__pycache__/
+-rw-r--r--   0 al        (1000) al        (1001)      217 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     5521 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/__pycache__/io.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     5734 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/__pycache__/local.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     5573 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/io.py
+-rw-r--r--   0 al        (1000) al        (1001)     5130 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/local.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.701398 yerbamate-0.9.237/packages/yerbamate/api/data/sources/remote/
+-rw-r--r--   0 al        (1000) al        (1001)       37 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/remote/__init__.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.701398 yerbamate-0.9.237/packages/yerbamate/api/data/sources/remote/__pycache__/
+-rw-r--r--   0 al        (1000) al        (1001)      220 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/remote/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     2132 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/remote/__pycache__/remote.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     1078 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/remote/remote.py
+-rw-r--r--   0 al        (1000) al        (1001)      365 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/sources/source.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.701398 yerbamate-0.9.237/packages/yerbamate/api/data/utils/
+-rw-r--r--   0 al        (1000) al        (1001)        0 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/utils/__init__.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.702398 yerbamate-0.9.237/packages/yerbamate/api/data/utils/__pycache__/
+-rw-r--r--   0 al        (1000) al        (1001)      164 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/utils/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)      540 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/utils/__pycache__/exp_util.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     1035 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/utils/__pycache__/git_util.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     4487 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/api/data/utils/__pycache__/gitdir.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)      326 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/utils/exp_util.py
+-rw-r--r--   0 al        (1000) al        (1001)     1197 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/utils/git_util.py
+-rw-r--r--   0 al        (1000) al        (1001)     7395 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/data/utils/gitdir.py
+-rw-r--r--   0 al        (1000) al        (1001)      869 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/api/mate_api.py
+-rw-r--r--   0 al        (1000) al        (1001)      294 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/constants.py
+-rw-r--r--   0 al        (1000) al        (1001)     6984 2023-05-13 17:01:52.000000 yerbamate-0.9.237/packages/yerbamate/environment.py
+-rw-r--r--   0 al        (1000) al        (1001)     7829 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/mate.py
+-rw-r--r--   0 al        (1000) al        (1001)    10611 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/mate_cli.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.702398 yerbamate-0.9.237/packages/yerbamate/utils/
+-rw-r--r--   0 al        (1000) al        (1001)     1433 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/utils/__init__.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.702398 yerbamate-0.9.237/packages/yerbamate/utils/__pycache__/
+-rw-r--r--   0 al        (1000) al        (1001)     2016 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/utils/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)      814 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/utils/__pycache__/bunch.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     3761 2023-04-09 10:03:11.000000 yerbamate-0.9.237/packages/yerbamate/utils/__pycache__/utils.cpython-310.pyc
+-rw-r--r--   0 al        (1000) al        (1001)     2145 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/utils/bunch.py
+-rw-r--r--   0 al        (1000) al        (1001)     1386 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/utils/git_url_parser.py
+-rw-r--r--   0 al        (1000) al        (1001)     4419 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/utils/utils.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.703398 yerbamate-0.9.237/packages/yerbamate/yerbamate.egg-info/
+-rw-r--r--   0 al        (1000) al        (1001)      601 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/yerbamate.egg-info/PKG-INFO
+-rw-r--r--   0 al        (1000) al        (1001)      342 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/yerbamate.egg-info/SOURCES.txt
+-rw-r--r--   0 al        (1000) al        (1001)        1 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/yerbamate.egg-info/dependency_links.txt
+-rw-r--r--   0 al        (1000) al        (1001)       10 2023-04-08 19:56:23.000000 yerbamate-0.9.237/packages/yerbamate/yerbamate.egg-info/top_level.txt
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.698398 yerbamate-0.9.237/packages/yerbamate.egg-info/
+-rw-r--r--   0 al        (1000) al        (1001)    11582 2023-05-13 17:04:44.000000 yerbamate-0.9.237/packages/yerbamate.egg-info/PKG-INFO
+-rw-r--r--   0 al        (1000) al        (1001)     3195 2023-05-13 17:04:44.000000 yerbamate-0.9.237/packages/yerbamate.egg-info/SOURCES.txt
+-rw-r--r--   0 al        (1000) al        (1001)        1 2023-05-13 17:04:44.000000 yerbamate-0.9.237/packages/yerbamate.egg-info/dependency_links.txt
+-rw-r--r--   0 al        (1000) al        (1001)       82 2023-05-13 17:04:44.000000 yerbamate-0.9.237/packages/yerbamate.egg-info/requires.txt
+-rw-r--r--   0 al        (1000) al        (1001)       10 2023-05-13 17:04:44.000000 yerbamate-0.9.237/packages/yerbamate.egg-info/top_level.txt
+-rw-r--r--   0 al        (1000) al        (1001)      107 2023-05-13 17:04:44.703398 yerbamate-0.9.237/setup.cfg
+-rw-r--r--   0 al        (1000) al        (1001)     1279 2023-05-13 17:02:10.000000 yerbamate-0.9.237/setup.py
+drwxr-xr-x   0 al        (1000) al        (1001)        0 2023-05-13 17:04:44.697399 yerbamate-0.9.237/src/
+-rwxr-xr-x   0 al        (1000) al        (1001)       62 2023-04-08 19:56:23.000000 yerbamate-0.9.237/src/mate
```

### Comparing `yerbamate-0.9.236/LICENSE` & `yerbamate-0.9.237/LICENSE`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/PKG-INFO` & `yerbamate-0.9.237/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yerbamate
-Version: 0.9.236
+Version: 0.9.237
 Summary:  A python module and experiment manager for deep learning
 Home-page: https://github.com/oalee/yerbamate
 Author: Giulio Zani, Ali Rahimi
 Author-email: yerba.mate.dl@proton.me
 License: Apache License 2.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
```

### Comparing `yerbamate-0.9.236/README.md` & `yerbamate-0.9.237/README.md`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/__pycache__/environment.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/__pycache__/environment.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Wed May  3 21:03:55 2023 UTC, .py size: 5857 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 13% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 3bcc 5264 e116 0000  o.......;.Rd....
+00000000: 6f0d 0d0a 0000 0000 98c1 5f64 9218 0000  o........._d....
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 4000 0000 6400  .....@...s@...d.
 00000030: 6401 6c00 5a00 6400 6401 6c01 5a01 6400  d.l.Z.d.d.l.Z.d.
 00000040: 6401 6c02 5a02 6400 6401 6c03 5a03 6400  d.l.Z.d.d.l.Z.d.
 00000050: 6401 6c04 5a04 6402 5a05 4700 6403 6404  d.l.Z.d.Z.G.d.d.
 00000060: 8400 6404 6506 8303 5a07 6401 5300 2905  ..d.e...Z.d.S.).
 00000070: e900 0000 004e da03 656e 7663 0000 0000  .....N..envc....
@@ -10,271 +10,284 @@
 00000090: 0000 0000 7344 0000 0065 005a 0164 005a  ....sD...e.Z.d.Z
 000000a0: 0264 0164 0284 005a 0364 0364 0484 005a  .d.d...Z.d.d...Z
 000000b0: 0464 0564 0684 005a 0564 0764 0884 005a  .d.d...Z.d.d...Z
 000000c0: 0664 0964 0a84 005a 0787 0066 0164 0b64  .d.d...Z...f.d.d
 000000d0: 0c84 085a 0887 0004 005a 0953 0029 0dda  ...Z.....Z.S.)..
 000000e0: 0b45 6e76 6972 6f6e 6d65 6e74 6301 0000  .Environmentc...
 000000f0: 0000 0000 0000 0000 0004 0000 0007 0000  ................
-00000100: 0043 0000 0073 3e01 0000 6401 7c00 5f00  .C...s>...d.|._.
+00000100: 0043 0000 0073 5401 0000 6401 7c00 5f00  .C...sT...d.|._.
 00000110: 6401 7c00 5f01 6401 7c00 5f02 6401 7c00  d.|._.d.|._.d.|.
 00000120: 5f03 6900 7c00 5f04 7a0b 7405 7c00 7406  _.i.|._.z.t.|.t.
 00000130: 6a07 6402 1900 6403 8303 0100 5700 6e04  j.d...d.....W.n.
 00000140: 0100 0100 0100 5900 7406 6a07 6402 6400  ......Y.t.j.d.d.
 00000150: 8502 1900 7c00 5f08 7c00 a009 a100 7c00  ....|._.|.....|.
-00000160: 5f0a 7406 6a07 4400 5d1e 7d01 6404 7c01  _.t.j.D.].}.d.|.
+00000160: 5f0a 7406 6a07 4400 5d29 7d01 6404 7c01  _.t.j.D.])}.d.|.
 00000170: 7601 7236 712f 7c01 a00b 6404 a101 5c02  v.r6q/|...d...\.
-00000180: 7d02 7d03 7c00 a00c 7c03 a101 7d03 7405  }.}.|...|...}.t.
-00000190: 7c00 7c02 7c03 8303 0100 7c03 7c00 6a04  |.|.|.....|.|.j.
-000001a0: 7c02 3c00 712f 7406 6a07 6405 1900 7c00  |.<.q/t.j.d...|.
-000001b0: 5f0d 6406 7c00 6a0d 7600 7279 740e 6a0f  _.d.|.j.v.ryt.j.
-000001c0: 6a10 7406 6a07 6407 6408 8502 1900 8e00  j.t.j.d.d.......
-000001d0: 7c00 5f11 740e 6a0f a010 7c00 6a0a 6409  |._.t.j...|.j.d.
-000001e0: 7406 6a07 6407 1900 7406 6a07 640a 1900  t.j.d...t.j.d...
-000001f0: 640b 1700 a104 7c00 5f0d 6e17 7c00 6a0d  d.....|._.n.|.j.
-00000200: a00b 640c a101 640d 6400 8502 1900 7c00  ..d...d.d.....|.
-00000210: 5f11 740e 6a0f 6a10 7c00 6a11 8e00 6400  _.t.j.j.|.j...d.
-00000220: 640e 8502 1900 7c00 5f11 7c00 a012 a100  d.....|._.|.....
-00000230: 0100 7c00 6a02 729d 7c00 a013 a100 0100  ..|.j.r.|.......
-00000240: 6400 5300 6400 5300 290f 4e46 e901 0000  d.S.d.S.).NF....
-00000250: 0054 fa01 3d72 0100 0000 7a08 6269 6e2f  .T..=r....z.bin/
-00000260: 6d61 7465 e902 0000 00e9 0400 0000 5a0b  mate..........Z.
-00000270: 6578 7065 7269 6d65 6e74 73e9 0300 0000  experiments.....
-00000280: 7a03 2e70 79fa 012f e9fe ffff ffe9 fdff  z..py../........
-00000290: ffff 2914 5a07 7265 7374 6172 74da 0474  ..).Z.restart..t
-000002a0: 6573 745a 0574 7261 696e da06 7361 6d70  estZ.train..samp
-000002b0: 6c65 da07 6870 6172 616d 73da 0773 6574  le..hparams..set
-000002c0: 6174 7472 da03 7379 73da 0461 7267 76da  attr..sys..argv.
-000002d0: 0461 7267 73da 175f 456e 7669 726f 6e6d  .args.._Environm
-000002e0: 656e 745f 5f66 696e 645f 726f 6f74 da05  ent__find_root..
-000002f0: 5f72 6f6f 74da 0573 706c 6974 da13 636f  _root..split..co
-00000300: 6e76 6572 745f 7374 725f 746f 5f64 6174  nvert_str_to_dat
-00000310: 61da 055f 7061 7468 da02 6f73 da04 7061  a.._path..os..pa
-00000320: 7468 da04 6a6f 696e da04 6e61 6d65 da15  th..join..name..
-00000330: 5f45 6e76 6972 6f6e 6d65 6e74 5f5f 7365  _Environment__se
-00000340: 745f 656e 76da 215f 456e 7669 726f 6e6d  t_env.!_Environm
-00000350: 656e 745f 5f67 656e 6572 6174 655f 6578  ent__generate_ex
-00000360: 7065 7269 6d65 6e74 2904 da04 7365 6c66  periment)...self
-00000370: da03 6172 67da 036b 6579 da05 7661 6c75  ..arg..key..valu
-00000380: 65a9 0072 2200 0000 fa3b 2f68 6f6d 652f  e..r"....;/home/
-00000390: 616c 2f47 6974 4875 622f 7965 7262 616d  al/GitHub/yerbam
-000003a0: 6174 652f 7061 636b 6167 6573 2f79 6572  ate/packages/yer
-000003b0: 6261 6d61 7465 2f65 6e76 6972 6f6e 6d65  bamate/environme
-000003c0: 6e74 2e70 79da 085f 5f69 6e69 745f 5f0e  nt.py..__init__.
-000003d0: 0000 0073 3c00 0000 0603 0601 0601 0601  ...s<...........
-000003e0: 0601 0203 1601 0601 0201 1002 0a02 0a03  ................
-000003f0: 0801 0201 0e01 0a01 0c01 0c01 0c02 0a01  ................
-00000400: 1801 0601 1a01 08ff 1604 1801 0802 0602  ................
-00000410: 0c01 04ff 7a14 456e 7669 726f 6e6d 656e  ....z.Environmen
-00000420: 742e 5f5f 696e 6974 5f5f 6302 0000 0000  t.__init__c.....
-00000430: 0000 0000 0000 0002 0000 000b 0000 0043  ...............C
-00000440: 0000 0073 6000 0000 7a05 7400 7c01 8301  ...s`...z.t.|...
-00000450: 5700 5300 0400 7401 792f 0100 0100 0100  W.S...t.y/......
-00000460: 7a07 7402 7c01 8301 5700 0600 5900 5300  z.t.|...W...Y.S.
-00000470: 0400 7401 792e 0100 0100 0100 7c01 6401  ..t.y.......|.d.
-00000480: 7600 7222 5900 5900 6402 5300 7c01 6403  v.r"Y.Y.d.S.|.d.
-00000490: 7600 722a 5900 5900 6404 5300 5900 5900  v.r*Y.Y.d.S.Y.Y.
-000004a0: 7c01 5300 7700 7700 2905 4e29 02da 0454  |.S.w.w.).N)...T
-000004b0: 7275 65da 0474 7275 6554 2902 da05 4661  rue..trueT)...Fa
-000004c0: 6c73 65da 0566 616c 7365 4629 03da 0369  lse..falseF)...i
-000004d0: 6e74 da0a 5661 6c75 6545 7272 6f72 da05  nt..ValueError..
-000004e0: 666c 6f61 7429 0272 1e00 0000 da05 696e  float).r......in
-000004f0: 7075 7472 2200 0000 7222 0000 0072 2300  putr"...r"...r#.
-00000500: 0000 7216 0000 0039 0000 0073 1c00 0000  ..r....9...s....
-00000510: 0201 0a01 0c01 0201 0e01 0c01 0801 0801  ................
-00000520: 0801 0801 04ff 0403 02fa 02fd 7a1f 456e  ............z.En
-00000530: 7669 726f 6e6d 656e 742e 636f 6e76 6572  vironment.conver
-00000540: 745f 7374 725f 746f 5f64 6174 6163 0100  t_str_to_datac..
-00000550: 0000 0000 0000 0000 0000 0300 0000 0700  ................
-00000560: 0000 4300 0000 734e 0000 0074 00a0 01a1  ..C...sN...t....
-00000570: 007d 0174 006a 02a0 0374 006a 02a0 047c  .}.t.j...t.j...|
-00000580: 0164 01a1 02a1 0172 2574 05a0 0674 0774  .d.....r%t...t.t
-00000590: 006a 02a0 047c 0164 01a1 0264 0283 02a1  .j...|.d...d....
-000005a0: 017d 0274 006a 02a0 047c 017c 0264 0319  .}.t.j...|.|.d..
-000005b0: 00a1 0253 0064 0053 0029 044e fa09 6d61  ...S.d.S.).N..ma
-000005c0: 7465 2e6a 736f 6eda 0172 da07 7072 6f6a  te.json..r..proj
-000005d0: 6563 7429 0872 1800 0000 da06 6765 7463  ect).r......getc
-000005e0: 7764 7219 0000 00da 0665 7869 7374 7372  wdr......existsr
-000005f0: 1a00 0000 da04 6a73 6f6e da04 6c6f 6164  ......json..load
-00000600: da04 6f70 656e 2903 721e 0000 0072 1900  ..open).r....r..
-00000610: 0000 da04 636f 6e66 7222 0000 0072 2200  ....confr"...r".
-00000620: 0000 7223 0000 005a 0b5f 5f66 696e 645f  ..r#...Z.__find_
-00000630: 726f 6f74 4700 0000 730a 0000 0008 0316  rootG...s.......
-00000640: 021a 0112 0204 027a 1745 6e76 6972 6f6e  .......z.Environ
-00000650: 6d65 6e74 2e5f 5f66 696e 645f 726f 6f74  ment.__find_root
-00000660: 6301 0000 0000 0000 0000 0000 0007 0000  c...............
-00000670: 0008 0000 0043 0000 0073 d200 0000 6700  .....C...s....g.
-00000680: 6401 a201 7d01 6400 7d02 7c01 4400 5d0e  d...}.d.}.|.D.].
-00000690: 7d03 7c03 7c00 6a00 7600 7216 7c00 6a00  }.|.|.j.v.r.|.j.
-000006a0: 7c03 1900 7d02 0100 6e01 7108 7c02 6400  |...}...n.q.|.d.
-000006b0: 7500 721d 6400 5300 7401 6a02 a003 7c02  u.r.d.S.t.j...|.
-000006c0: a101 732a 7401 6a04 7c02 6402 6403 8d02  ..s*t.j.|.d.d...
-000006d0: 0100 7401 6a02 a005 7c02 6404 a102 7d04  ..t.j...|.d...}.
-000006e0: 7406 a007 7c00 6a08 7c04 a102 0100 7c00  t...|.j.|.....|.
-000006f0: 6a09 6900 6b03 7267 7401 6a02 a005 7c02  j.i.k.rgt.j...|.
-00000700: 6405 a102 7d05 740a 7c05 6406 8302 8f14  d...}.t.|.d.....
-00000710: 7d06 740b 6a0c 740d 7c00 6a09 8301 7c06  }.t.j.t.|.j...|.
-00000720: 6407 6408 8d03 0100 5700 6400 0400 0400  d.d.....W.d.....
-00000730: 8303 0100 6400 5300 3100 7360 7701 0100  ....d.S.1.s`w...
-00000740: 0100 0100 5900 0100 6400 5300 6400 5300  ....Y...d.S.d.S.
-00000750: 2909 4e29 06da 0772 6573 756c 7473 5a0c  ).N)...resultsZ.
-00000760: 7265 7375 6c74 735f 7061 7468 5a0b 7265  results_pathZ.re
-00000770: 7375 6c74 735f 6469 725a 0473 6176 655a  sults_dirZ.saveZ
-00000780: 0973 6176 655f 7061 7468 5a08 7361 7665  .save_pathZ.save
-00000790: 5f64 6972 5429 01da 0865 7869 7374 5f6f  _dirT)...exist_o
-000007a0: 6b7a 0d65 7870 6572 696d 656e 742e 7079  kz.experiment.py
-000007b0: 7a0f 6578 7065 7269 6d65 6e74 2e6a 736f  z.experiment.jso
-000007c0: 6eda 0177 7207 0000 00a9 01da 0669 6e64  n..wr........ind
-000007d0: 656e 7429 0e72 0200 0000 7218 0000 0072  ent).r....r....r
-000007e0: 1900 0000 7231 0000 00da 086d 616b 6564  ....r1.....maked
-000007f0: 6972 7372 1a00 0000 da06 7368 7574 696c  irsr......shutil
-00000800: da08 636f 7079 6669 6c65 7217 0000 0072  ..copyfiler....r
-00000810: 0e00 0000 7234 0000 0072 3200 0000 da04  ....r4...r2.....
-00000820: 6475 6d70 da04 6469 6374 2907 721e 0000  dump..dict).r...
-00000830: 0072 3600 0000 da06 7265 7375 6c74 7220  .r6.....resultr 
-00000840: 0000 005a 0973 6176 655f 6669 6c65 5a0b  ...Z.save_fileZ.
-00000850: 7061 7261 6d73 5f66 696c 65da 0166 7222  params_file..fr"
-00000860: 0000 0072 2200 0000 7223 0000 005a 155f  ...r"...r#...Z._
-00000870: 5f67 656e 6572 6174 655f 6578 7065 7269  _generate_experi
-00000880: 6d65 6e74 5300 0000 7326 0000 0008 0204  mentS...s&......
-00000890: 0208 010a 010a 0104 0102 fe08 0304 010c  ................
-000008a0: 010e 010e 020e 020a 040e 010c 0318 0122  ..............."
-000008b0: ff04 fc7a 2145 6e76 6972 6f6e 6d65 6e74  ...z!Environment
-000008c0: 2e5f 5f67 656e 6572 6174 655f 6578 7065  .__generate_expe
-000008d0: 7269 6d65 6e74 6301 0000 0000 0000 0000  rimentc.........
-000008e0: 0000 000d 0000 0009 0000 0043 0000 0073  ...........C...s
-000008f0: 6002 0000 7400 6a01 a002 6401 a101 7d01  `...t.j...d...}.
-00000900: 7403 a004 7405 7c01 6402 8302 a101 7d02  t...t.|.d.....}.
-00000910: 7400 6a01 a002 6403 a101 7d03 7400 6a01  t.j...d...}.t.j.
-00000920: a006 7c03 a101 7350 7407 6404 8301 0100  ..|...sPt.d.....
-00000930: 7408 7c02 7600 7229 7c02 7408 1900 a009  t.|.v.r)|.t.....
-00000940: a100 7d04 6e03 6405 6701 7d04 6406 6407  ..}.n.d.g.}.d.d.
-00000950: 8400 7c04 4400 8301 7d05 7405 7c03 6408  ..|.D...}.t.|.d.
-00000960: 8302 8f10 7d06 7403 6a0a 7c05 7c06 6409  ....}.t.j.|.|.d.
-00000970: 640a 8d03 0100 5700 6400 0400 0400 8303  d.....W.d.......
-00000980: 0100 6e08 3100 734b 7701 0100 0100 0100  ..n.1.sKw.......
-00000990: 5900 0100 7405 7c03 6402 8302 8f1f 7d06  Y...t.|.d.....}.
-000009a0: 7a07 7403 a004 7c06 a101 7d07 5700 6e0f  z.t...|...}.W.n.
-000009b0: 0400 7403 6a0b 6a0c 796c 0100 0100 0100  ..t.j.j.yl......
-000009c0: 6405 640b 6901 7d07 5900 6e01 7700 5700  d.d.i.}.Y.n.w.W.
-000009d0: 6400 0400 0400 8303 0100 6e08 3100 7377  d.........n.1.sw
-000009e0: 7701 0100 0100 0100 5900 0100 6700 7d08  w.......Y...g.}.
-000009f0: 7408 7c02 7600 72a7 7c07 a00d a100 4400  t.|.v.r.|.....D.
-00000a00: 5d20 5c02 7d09 7d0a 7c07 7c09 1900 640b  ] \.}.}.|.|...d.
-00000a10: 6b02 72a6 7c09 7400 6a0e 7600 729d 7400  k.r.|.t.j.v.r.t.
-00000a20: 6a0e 7c09 1900 7c07 7c09 3c00 7186 7c08  j.|...|.|.<.q.|.
-00000a30: a00f 7c09 a101 0100 7c0a 7c07 7c09 3c00  ..|.....|.|.|.<.
-00000a40: 7186 7410 7c08 8301 640c 6b04 72d6 7407  q.t.|...d.k.r.t.
-00000a50: 640d 8301 0100 7c08 4400 5d19 7d09 7c09  d.....|.D.].}.|.
-00000a60: 7c02 7408 1900 7600 72c1 7c02 7408 1900  |.t...v.r.|.t...
-00000a70: 7c09 1900 6e01 640e 7d0b 7407 7c09 9b00  |...n.d.}.t.|...
-00000a80: 640f 7c0b 9b00 9d03 8301 0100 71b3 7407  d.|.........q.t.
-00000a90: 6410 8301 0100 7411 a012 6411 a101 0100  d.....t...d.....
-00000aa0: 6412 6701 7d0c 7c0c 4400 5d38 7d09 7c09  d.g.}.|.D.]8}.|.
-00000ab0: 7c07 7600 72f5 7400 6a01 6a02 7c07 7c09  |.v.r.t.j.j.|.|.
-00000ac0: 1900 6701 7c00 6a13 a014 6413 a101 a201  ..g.|.j...d.....
-00000ad0: 5200 8e00 7c07 7c09 3c00 0100 6e1f 7400  R...|.|.<...n.t.
-00000ae0: 6a0e a015 7c09 6400 a102 6400 7501 9001  j...|.d...d.u...
-00000af0: 7213 7400 6a0e a015 7c09 6400 a102 640b  r.t.j...|.d...d.
-00000b00: 6b03 9001 7213 7400 6a0e a015 7c09 a101  k...r.t.j...|...
-00000b10: 7c07 7c09 3c00 0100 6e01 71db 7410 7c07  |.|.<...n.q.t.|.
-00000b20: 8301 640c 6b02 9001 7228 7407 6414 8301  ..d.k...r(t.d...
-00000b30: 0100 7407 6410 8301 0100 7411 a012 6411  ..t.d.....t...d.
-00000b40: a101 0100 7416 7c00 6415 7c07 8303 0100  ....t.|.d.|.....
-00000b50: 6400 5300 2916 4e72 2d00 0000 722e 0000  d.S.).Nr-...r...
-00000b60: 007a 0865 6e76 2e6a 736f 6e7a 4045 6e76  .z.env.jsonz@Env
-00000b70: 6972 6f6e 6d65 6e74 2066 696c 6520 6e6f  ironment file no
-00000b80: 7420 666f 756e 642c 2063 7265 6174 696e  t found, creatin
-00000b90: 6720 6f6e 6520 7769 7468 2064 6566 6175  g one with defau
-00000ba0: 6c74 733a 2065 6e76 2e6a 736f 6e72 3600  lts: env.jsonr6.
-00000bb0: 0000 6301 0000 0000 0000 0000 0000 0002  ..c.............
-00000bc0: 0000 0004 0000 0053 0000 0073 1200 0000  .......S...s....
-00000bd0: 6900 7c00 5d05 7d01 7c01 6400 9302 7102  i.|.].}.|.d...q.
-00000be0: 5300 2901 da00 7222 0000 0029 02da 022e  S.)...r"...)....
-00000bf0: 3072 2000 0000 7222 0000 0072 2200 0000  0r ...r"...r"...
-00000c00: 7223 0000 00da 0a3c 6469 6374 636f 6d70  r#.....<dictcomp
-00000c10: 3e7b 0000 0073 0200 0000 1200 7a29 456e  >{...s......z)En
-00000c20: 7669 726f 6e6d 656e 742e 5f5f 7365 745f  vironment.__set_
-00000c30: 656e 762e 3c6c 6f63 616c 733e 2e3c 6469  env.<locals>.<di
-00000c40: 6374 636f 6d70 3e72 3800 0000 7207 0000  ctcomp>r8...r...
-00000c50: 0072 3900 0000 7242 0000 0072 0100 0000  .r9...rB...r....
-00000c60: 7a47 456e 7669 726f 6e6d 656e 7420 7661  zGEnvironment va
-00000c70: 7269 6162 6c65 7320 6e6f 7420 666f 756e  riables not foun
-00000c80: 642e 2053 6574 2074 6865 6d20 696e 2065  d. Set them in e
-00000c90: 6e76 2e6a 736f 6e20 6f72 2069 6e20 796f  nv.json or in yo
-00000ca0: 7572 2073 6865 6c6c 2e7a 1d52 6571 7569  ur shell.z.Requi
-00000cb0: 7265 6420 656e 7669 726f 6e6d 656e 7420  red environment 
-00000cc0: 7661 7269 6162 6c65 7a03 203a 20fa 0a45  variablez. : ..E
-00000cd0: 7869 7469 6e67 2e2e 2e72 0400 0000 5a09  xiting...r....Z.
-00000ce0: 6175 746f 5f73 6176 6572 0900 0000 7a59  auto_saver....zY
-00000cf0: 7265 7375 6c74 732f 7361 7665 5f64 6972  results/save_dir
-00000d00: 2f73 6176 6520 656e 7669 726f 6e6d 656e  /save environmen
-00000d10: 7420 7661 7269 6162 6c65 2069 7320 656d  t variable is em
-00000d20: 7074 792e 2053 6574 2069 7420 696e 2065  pty. Set it in e
-00000d30: 6e76 2e6a 736f 6e20 6f72 2069 6e20 796f  nv.json or in yo
-00000d40: 7572 2073 6865 6c6c 2e72 0200 0000 2917  ur shell.r....).
-00000d50: 7218 0000 0072 1900 0000 721a 0000 0072  r....r....r....r
-00000d60: 3200 0000 7233 0000 0072 3400 0000 7231  2...r3...r4...r1
-00000d70: 0000 00da 0570 7269 6e74 da07 454e 565f  .....print..ENV_
-00000d80: 4b45 59da 046b 6579 7372 3e00 0000 da07  KEY..keysr>.....
-00000d90: 6465 636f 6465 725a 0f4a 534f 4e44 6563  decoderZ.JSONDec
-00000da0: 6f64 6545 7272 6f72 da05 6974 656d 73da  odeError..items.
-00000db0: 0765 6e76 6972 6f6e da06 6170 7065 6e64  .environ..append
-00000dc0: da03 6c65 6e72 1000 0000 da04 6578 6974  ..lenr......exit
-00000dd0: 721b 0000 0072 1500 0000 da03 6765 7472  r....r......getr
-00000de0: 0f00 0000 290d 721e 0000 005a 0e6d 6174  ....).r....Z.mat
-00000df0: 655f 636f 6e66 5f70 6174 6872 3500 0000  e_conf_pathr5...
-00000e00: 5a08 656e 765f 7061 7468 da0d 7265 7175  Z.env_path..requ
-00000e10: 6972 6564 5f6b 6579 735a 0b64 6566 7561  ired_keysZ.defua
-00000e20: 6c74 5f65 6e76 7241 0000 0072 0200 0000  lt_envrA...r....
-00000e30: 5a0d 656e 765f 6e6f 745f 666f 756e 6472  Z.env_not_foundr
-00000e40: 2000 0000 7221 0000 005a 0464 6573 635a   ...r!...Z.descZ
-00000e50: 0e73 6561 7263 685f 7265 7375 6c74 7372  .search_resultsr
-00000e60: 2200 0000 7222 0000 0072 2300 0000 5a09  "...r"...r#...Z.
-00000e70: 5f5f 7365 745f 656e 766e 0000 0073 6e00  __set_envn...sn.
-00000e80: 0000 0c01 1001 0c02 0c01 0801 0802 0e01  ................
-00000e90: 0602 0e02 0c02 1201 1cff 0c03 0201 0e01  ................
-00000ea0: 1001 0402 08ff 02ff 0280 1cfd 0408 0802  ................
-00000eb0: 1001 0c01 0a01 1001 0a03 0801 0280 0c02  ................
-00000ec0: 0201 0201 04ff 0802 1c01 1401 0802 0a01  ................
-00000ed0: 0603 0801 0801 2401 0402 2801 1001 0402  ......$...(.....
-00000ee0: 0280 0e02 0201 0201 04ff 0802 0a01 1002  ................
-00000ef0: 7a15 456e 7669 726f 6e6d 656e 742e 5f5f  z.Environment.__
-00000f00: 7365 745f 656e 7663 0200 0000 0000 0000  set_envc........
-00000f10: 0000 0000 0300 0000 0400 0000 0300 0000  ................
-00000f20: 736e 0000 007c 017c 0076 0172 317c 017c  sn...|.|.v.r1|.|
-00000f30: 006a 0076 0072 0e7c 006a 007c 0119 0053  .j.v.r.|.j.|...S
-00000f40: 0074 016a 02a0 037c 0164 00a1 027d 027c  .t.j...|.d...}.|
-00000f50: 0264 0075 0073 1d7c 0264 016b 0272 2f74  .d.u.s.|.d.k.r/t
-00000f60: 0464 027c 019b 0064 039d 0383 0101 0074  .d.|...d.......t
-00000f70: 0464 0483 0101 0074 05a0 0664 05a1 0101  .d.....t...d....
-00000f80: 006e 027c 0253 0074 0783 00a0 087c 01a1  .n.|.S.t.....|..
-00000f90: 0153 0029 064e 7242 0000 007a 1545 6e76  .S.).NrB...z.Env
-00000fa0: 6972 6f6e 6d65 6e74 2076 6172 6961 626c  ironment variabl
-00000fb0: 6520 7a30 206e 6f74 2066 6f75 6e64 2e20  e z0 not found. 
-00000fc0: 5365 7420 6974 2069 6e20 656e 762e 6a73  Set it in env.js
-00000fd0: 6f6e 206f 7220 696e 2079 6f75 7220 7368  on or in your sh
-00000fe0: 656c 6c2e 7245 0000 0072 0400 0000 2909  ell.rE...r....).
-00000ff0: 7202 0000 0072 1800 0000 724b 0000 0072  r....r....rK...r
-00001000: 4f00 0000 7246 0000 0072 1000 0000 724e  O...rF...r....rN
-00001010: 0000 00da 0573 7570 6572 da0b 5f5f 6765  .....super..__ge
-00001020: 7469 7465 6d5f 5f29 0372 1e00 0000 7220  titem__).r....r 
-00001030: 0000 00da 0372 6573 a901 da09 5f5f 636c  .....res....__cl
-00001040: 6173 735f 5f72 2200 0000 7223 0000 0072  ass__r"...r#...r
-00001050: 5200 0000 b200 0000 7318 0000 0008 010a  R.......s.......
-00001060: 020a 010e 0110 0202 010a 0104 ff08 020c  ................
-00001070: 0104 020c 027a 1745 6e76 6972 6f6e 6d65  .....z.Environme
-00001080: 6e74 2e5f 5f67 6574 6974 656d 5f5f 290a  nt.__getitem__).
-00001090: da08 5f5f 6e61 6d65 5f5f da0a 5f5f 6d6f  ..__name__..__mo
-000010a0: 6475 6c65 5f5f da0c 5f5f 7175 616c 6e61  dule__..__qualna
-000010b0: 6d65 5f5f 7224 0000 0072 1600 0000 7213  me__r$...r....r.
-000010c0: 0000 0072 1d00 0000 721c 0000 0072 5200  ...r....r....rR.
-000010d0: 0000 da0d 5f5f 636c 6173 7363 656c 6c5f  ....__classcell_
-000010e0: 5f72 2200 0000 7222 0000 0072 5400 0000  _r"...r"...rT...
-000010f0: 7223 0000 0072 0300 0000 0c00 0000 730e  r#...r........s.
-00001100: 0000 0008 0008 0208 2b08 0e08 0c08 1b14  ........+.......
-00001110: 4472 0300 0000 2908 7232 0000 0072 1800  Dr....).r2...r..
-00001120: 0000 723c 0000 0072 1000 0000 5a04 6970  ..r<...r....Z.ip
-00001130: 6462 7247 0000 0072 3f00 0000 7203 0000  dbrG...r?...r...
-00001140: 0072 2200 0000 7222 0000 0072 2200 0000  .r"...r"...r"...
-00001150: 7223 0000 00da 083c 6d6f 6475 6c65 3e01  r#.....<module>.
-00001160: 0000 0073 0e00 0000 0801 0801 0801 0801  ...s............
-00001170: 0801 0403 1403                           ......
+00000180: 7d02 7d03 7c00 a00c 7c03 a101 7d03 7c02  }.}.|...|...}.|.
+00000190: a00d 6405 a101 724d 7c02 6406 6400 8502  ..d...rM|.d.d...
+000001a0: 1900 7d02 7405 7c00 7c02 7c03 8303 0100  ..}.t.|.|.|.....
+000001b0: 7c03 7c00 6a04 7c02 3c00 712f 7406 6a07  |.|.j.|.<.q/t.j.
+000001c0: 6407 1900 7c00 5f0e 6408 7c00 6a0e 7600  d...|._.d.|.j.v.
+000001d0: 7284 740f 6a10 6a11 7406 6a07 6406 6409  r.t.j.j.t.j.d.d.
+000001e0: 8502 1900 8e00 7c00 5f12 740f 6a10 a011  ......|._.t.j...
+000001f0: 7c00 6a0a 640a 7406 6a07 6406 1900 7406  |.j.d.t.j.d...t.
+00000200: 6a07 640b 1900 640c 1700 a104 7c00 5f0e  j.d...d.....|._.
+00000210: 6e17 7c00 6a0e a00b 640d a101 640e 6400  n.|.j...d...d.d.
+00000220: 8502 1900 7c00 5f12 740f 6a10 6a11 7c00  ....|._.t.j.j.|.
+00000230: 6a12 8e00 6400 640f 8502 1900 7c00 5f12  j...d.d.....|._.
+00000240: 7c00 a013 a100 0100 7c00 6a02 72a8 7c00  |.......|.j.r.|.
+00000250: a014 a100 0100 6400 5300 6400 5300 2910  ......d.S.d.S.).
+00000260: 4e46 e901 0000 0054 fa01 3d7a 022d 2de9  NF.....T..=z.--.
+00000270: 0200 0000 7201 0000 007a 0862 696e 2f6d  ....r....z.bin/m
+00000280: 6174 65e9 0400 0000 5a0b 6578 7065 7269  ate.....Z.experi
+00000290: 6d65 6e74 73e9 0300 0000 7a03 2e70 79fa  ments.....z..py.
+000002a0: 012f e9fe ffff ffe9 fdff ffff 2915 5a07  ./..........).Z.
+000002b0: 7265 7374 6172 74da 0474 6573 745a 0574  restart..testZ.t
+000002c0: 7261 696e da06 7361 6d70 6c65 da07 6870  rain..sample..hp
+000002d0: 6172 616d 73da 0773 6574 6174 7472 da03  arams..setattr..
+000002e0: 7379 73da 0461 7267 76da 0461 7267 73da  sys..argv..args.
+000002f0: 175f 456e 7669 726f 6e6d 656e 745f 5f66  ._Environment__f
+00000300: 696e 645f 726f 6f74 da05 5f72 6f6f 74da  ind_root.._root.
+00000310: 0573 706c 6974 da13 636f 6e76 6572 745f  .split..convert_
+00000320: 7374 725f 746f 5f64 6174 61da 0a73 7461  str_to_data..sta
+00000330: 7274 7377 6974 68da 055f 7061 7468 da02  rtswith.._path..
+00000340: 6f73 da04 7061 7468 da04 6a6f 696e da04  os..path..join..
+00000350: 6e61 6d65 da15 5f45 6e76 6972 6f6e 6d65  name.._Environme
+00000360: 6e74 5f5f 7365 745f 656e 76da 215f 456e  nt__set_env.!_En
+00000370: 7669 726f 6e6d 656e 745f 5f67 656e 6572  vironment__gener
+00000380: 6174 655f 6578 7065 7269 6d65 6e74 2904  ate_experiment).
+00000390: da04 7365 6c66 da03 6172 67da 036b 6579  ..self..arg..key
+000003a0: da05 7661 6c75 65a9 0072 2300 0000 fa3b  ..value..r#....;
+000003b0: 2f68 6f6d 652f 616c 2f47 6974 4875 622f  /home/al/GitHub/
+000003c0: 7965 7262 616d 6174 652f 7061 636b 6167  yerbamate/packag
+000003d0: 6573 2f79 6572 6261 6d61 7465 2f65 6e76  es/yerbamate/env
+000003e0: 6972 6f6e 6d65 6e74 2e70 79da 085f 5f69  ironment.py..__i
+000003f0: 6e69 745f 5f0e 0000 0073 4000 0000 0603  nit__....s@.....
+00000400: 0601 0601 0601 0601 0203 1601 0601 0201  ................
+00000410: 1002 0a02 0a03 0801 0201 0e01 0a01 0a02  ................
+00000420: 0c01 0c02 0c01 0c02 0a01 1801 0601 1a01  ................
+00000430: 08ff 1604 1801 0802 0602 0c01 04ff 7a14  ..............z.
+00000440: 456e 7669 726f 6e6d 656e 742e 5f5f 696e  Environment.__in
+00000450: 6974 5f5f 6302 0000 0000 0000 0000 0000  it__c...........
+00000460: 0002 0000 000b 0000 0043 0000 0073 6000  .........C...s`.
+00000470: 0000 7a05 7400 7c01 8301 5700 5300 0400  ..z.t.|...W.S...
+00000480: 7401 792f 0100 0100 0100 7a07 7402 7c01  t.y/......z.t.|.
+00000490: 8301 5700 0600 5900 5300 0400 7401 792e  ..W...Y.S...t.y.
+000004a0: 0100 0100 0100 7c01 6401 7600 7222 5900  ......|.d.v.r"Y.
+000004b0: 5900 6402 5300 7c01 6403 7600 722a 5900  Y.d.S.|.d.v.r*Y.
+000004c0: 5900 6404 5300 5900 5900 7c01 5300 7700  Y.d.S.Y.Y.|.S.w.
+000004d0: 7700 2905 4e29 02da 0454 7275 65da 0474  w.).N)...True..t
+000004e0: 7275 6554 2902 da05 4661 6c73 65da 0566  rueT)...False..f
+000004f0: 616c 7365 4629 03da 0369 6e74 da0a 5661  alseF)...int..Va
+00000500: 6c75 6545 7272 6f72 da05 666c 6f61 7429  lueError..float)
+00000510: 0272 1f00 0000 da05 696e 7075 7472 2300  .r......inputr#.
+00000520: 0000 7223 0000 0072 2400 0000 7216 0000  ..r#...r$...r...
+00000530: 003d 0000 0073 1c00 0000 0201 0a01 0c01  .=...s..........
+00000540: 0201 0e01 0c01 0801 0801 0801 0801 04ff  ................
+00000550: 0403 02fa 02fd 7a1f 456e 7669 726f 6e6d  ......z.Environm
+00000560: 656e 742e 636f 6e76 6572 745f 7374 725f  ent.convert_str_
+00000570: 746f 5f64 6174 6163 0100 0000 0000 0000  to_datac........
+00000580: 0000 0000 0300 0000 0700 0000 4300 0000  ............C...
+00000590: 734e 0000 0074 00a0 01a1 007d 0174 006a  sN...t.....}.t.j
+000005a0: 02a0 0374 006a 02a0 047c 0164 01a1 02a1  ...t.j...|.d....
+000005b0: 0172 2574 05a0 0674 0774 006a 02a0 047c  .r%t...t.t.j...|
+000005c0: 0164 01a1 0264 0283 02a1 017d 0274 006a  .d...d.....}.t.j
+000005d0: 02a0 047c 017c 0264 0319 00a1 0253 0064  ...|.|.d.....S.d
+000005e0: 0053 0029 044e fa09 6d61 7465 2e6a 736f  .S.).N..mate.jso
+000005f0: 6eda 0172 da07 7072 6f6a 6563 7429 0872  n..r..project).r
+00000600: 1900 0000 da06 6765 7463 7764 721a 0000  ......getcwdr...
+00000610: 00da 0665 7869 7374 7372 1b00 0000 da04  ...existsr......
+00000620: 6a73 6f6e da04 6c6f 6164 da04 6f70 656e  json..load..open
+00000630: 2903 721f 0000 0072 1a00 0000 da04 636f  ).r....r......co
+00000640: 6e66 7223 0000 0072 2300 0000 7224 0000  nfr#...r#...r$..
+00000650: 005a 0b5f 5f66 696e 645f 726f 6f74 4b00  .Z.__find_rootK.
+00000660: 0000 730a 0000 0008 0316 021a 0112 0204  ..s.............
+00000670: 027a 1745 6e76 6972 6f6e 6d65 6e74 2e5f  .z.Environment._
+00000680: 5f66 696e 645f 726f 6f74 6301 0000 0000  _find_rootc.....
+00000690: 0000 0000 0000 0007 0000 0008 0000 0043  ...............C
+000006a0: 0000 0073 d200 0000 6700 6401 a201 7d01  ...s....g.d...}.
+000006b0: 6400 7d02 7c01 4400 5d0e 7d03 7c03 7c00  d.}.|.D.].}.|.|.
+000006c0: 6a00 7600 7216 7c00 6a00 7c03 1900 7d02  j.v.r.|.j.|...}.
+000006d0: 0100 6e01 7108 7c02 6400 7500 721d 6400  ..n.q.|.d.u.r.d.
+000006e0: 5300 7401 6a02 a003 7c02 a101 732a 7401  S.t.j...|...s*t.
+000006f0: 6a04 7c02 6402 6403 8d02 0100 7401 6a02  j.|.d.d.....t.j.
+00000700: a005 7c02 6404 a102 7d04 7406 a007 7c00  ..|.d...}.t...|.
+00000710: 6a08 7c04 a102 0100 7c00 6a09 6900 6b03  j.|.....|.j.i.k.
+00000720: 7267 7401 6a02 a005 7c02 6405 a102 7d05  rgt.j...|.d...}.
+00000730: 740a 7c05 6406 8302 8f14 7d06 740b 6a0c  t.|.d.....}.t.j.
+00000740: 740d 7c00 6a09 8301 7c06 6407 6408 8d03  t.|.j...|.d.d...
+00000750: 0100 5700 6400 0400 0400 8303 0100 6400  ..W.d.........d.
+00000760: 5300 3100 7360 7701 0100 0100 0100 5900  S.1.s`w.......Y.
+00000770: 0100 6400 5300 6400 5300 2909 4e29 06da  ..d.S.d.S.).N)..
+00000780: 0772 6573 756c 7473 5a0c 7265 7375 6c74  .resultsZ.result
+00000790: 735f 7061 7468 5a0b 7265 7375 6c74 735f  s_pathZ.results_
+000007a0: 6469 725a 0473 6176 655a 0973 6176 655f  dirZ.saveZ.save_
+000007b0: 7061 7468 5a08 7361 7665 5f64 6972 5429  pathZ.save_dirT)
+000007c0: 01da 0865 7869 7374 5f6f 6b7a 0d65 7870  ...exist_okz.exp
+000007d0: 6572 696d 656e 742e 7079 7a0f 6578 7065  eriment.pyz.expe
+000007e0: 7269 6d65 6e74 2e6a 736f 6eda 0177 7207  riment.json..wr.
+000007f0: 0000 00a9 01da 0669 6e64 656e 7429 0e72  .......indent).r
+00000800: 0200 0000 7219 0000 0072 1a00 0000 7232  ....r....r....r2
+00000810: 0000 00da 086d 616b 6564 6972 7372 1b00  .....makedirsr..
+00000820: 0000 da06 7368 7574 696c da08 636f 7079  ....shutil..copy
+00000830: 6669 6c65 7218 0000 0072 0e00 0000 7235  filer....r....r5
+00000840: 0000 0072 3300 0000 da04 6475 6d70 da04  ...r3.....dump..
+00000850: 6469 6374 2907 721f 0000 0072 3700 0000  dict).r....r7...
+00000860: da06 7265 7375 6c74 7221 0000 005a 0973  ..resultr!...Z.s
+00000870: 6176 655f 6669 6c65 5a0b 7061 7261 6d73  ave_fileZ.params
+00000880: 5f66 696c 65da 0166 7223 0000 0072 2300  _file..fr#...r#.
+00000890: 0000 7224 0000 005a 155f 5f67 656e 6572  ..r$...Z.__gener
+000008a0: 6174 655f 6578 7065 7269 6d65 6e74 5700  ate_experimentW.
+000008b0: 0000 7326 0000 0008 0204 0208 010a 010a  ..s&............
+000008c0: 0104 0102 fe08 0304 010c 010e 010e 020e  ................
+000008d0: 020a 040e 010c 0318 0122 ff04 fc7a 2145  ........."...z!E
+000008e0: 6e76 6972 6f6e 6d65 6e74 2e5f 5f67 656e  nvironment.__gen
+000008f0: 6572 6174 655f 6578 7065 7269 6d65 6e74  erate_experiment
+00000900: 6301 0000 0000 0000 0000 0000 000d 0000  c...............
+00000910: 0009 0000 0043 0000 0073 6002 0000 7400  .....C...s`...t.
+00000920: 6a01 a002 6401 a101 7d01 7403 a004 7405  j...d...}.t...t.
+00000930: 7c01 6402 8302 a101 7d02 7400 6a01 a002  |.d.....}.t.j...
+00000940: 6403 a101 7d03 7400 6a01 a006 7c03 a101  d...}.t.j...|...
+00000950: 7350 7407 6404 8301 0100 7408 7c02 7600  sPt.d.....t.|.v.
+00000960: 7229 7c02 7408 1900 a009 a100 7d04 6e03  r)|.t.......}.n.
+00000970: 6405 6701 7d04 6406 6407 8400 7c04 4400  d.g.}.d.d...|.D.
+00000980: 8301 7d05 7405 7c03 6408 8302 8f10 7d06  ..}.t.|.d.....}.
+00000990: 7403 6a0a 7c05 7c06 6409 640a 8d03 0100  t.j.|.|.d.d.....
+000009a0: 5700 6400 0400 0400 8303 0100 6e08 3100  W.d.........n.1.
+000009b0: 734b 7701 0100 0100 0100 5900 0100 7405  sKw.......Y...t.
+000009c0: 7c03 6402 8302 8f1f 7d06 7a07 7403 a004  |.d.....}.z.t...
+000009d0: 7c06 a101 7d07 5700 6e0f 0400 7403 6a0b  |...}.W.n...t.j.
+000009e0: 6a0c 796c 0100 0100 0100 6405 640b 6901  j.yl......d.d.i.
+000009f0: 7d07 5900 6e01 7700 5700 6400 0400 0400  }.Y.n.w.W.d.....
+00000a00: 8303 0100 6e08 3100 7377 7701 0100 0100  ....n.1.sww.....
+00000a10: 0100 5900 0100 6700 7d08 7408 7c02 7600  ..Y...g.}.t.|.v.
+00000a20: 72a7 7c07 a00d a100 4400 5d20 5c02 7d09  r.|.....D.] \.}.
+00000a30: 7d0a 7c07 7c09 1900 640b 6b02 72a6 7c09  }.|.|...d.k.r.|.
+00000a40: 7400 6a0e 7600 729d 7400 6a0e 7c09 1900  t.j.v.r.t.j.|...
+00000a50: 7c07 7c09 3c00 7186 7c08 a00f 7c09 a101  |.|.<.q.|...|...
+00000a60: 0100 7c0a 7c07 7c09 3c00 7186 7410 7c08  ..|.|.|.<.q.t.|.
+00000a70: 8301 640c 6b04 72d6 7407 640d 8301 0100  ..d.k.r.t.d.....
+00000a80: 7c08 4400 5d19 7d09 7c09 7c02 7408 1900  |.D.].}.|.|.t...
+00000a90: 7600 72c1 7c02 7408 1900 7c09 1900 6e01  v.r.|.t...|...n.
+00000aa0: 640e 7d0b 7407 7c09 9b00 640f 7c0b 9b00  d.}.t.|...d.|...
+00000ab0: 9d03 8301 0100 71b3 7407 6410 8301 0100  ......q.t.d.....
+00000ac0: 7411 a012 6411 a101 0100 6412 6701 7d0c  t...d.....d.g.}.
+00000ad0: 7c0c 4400 5d38 7d09 7c09 7c07 7600 72f5  |.D.]8}.|.|.v.r.
+00000ae0: 7400 6a01 6a02 7c07 7c09 1900 6701 7c00  t.j.j.|.|...g.|.
+00000af0: 6a13 a014 6413 a101 a201 5200 8e00 7c07  j...d.....R...|.
+00000b00: 7c09 3c00 0100 6e1f 7400 6a0e a015 7c09  |.<...n.t.j...|.
+00000b10: 6400 a102 6400 7501 9001 7213 7400 6a0e  d...d.u...r.t.j.
+00000b20: a015 7c09 6400 a102 640b 6b03 9001 7213  ..|.d...d.k...r.
+00000b30: 7400 6a0e a015 7c09 a101 7c07 7c09 3c00  t.j...|...|.|.<.
+00000b40: 0100 6e01 71db 7410 7c07 8301 640c 6b02  ..n.q.t.|...d.k.
+00000b50: 9001 7228 7407 6414 8301 0100 7407 6410  ..r(t.d.....t.d.
+00000b60: 8301 0100 7411 a012 6411 a101 0100 7416  ....t...d.....t.
+00000b70: 7c00 6415 7c07 8303 0100 6400 5300 2916  |.d.|.....d.S.).
+00000b80: 4e72 2e00 0000 722f 0000 007a 0865 6e76  Nr....r/...z.env
+00000b90: 2e6a 736f 6e7a 4045 6e76 6972 6f6e 6d65  .jsonz@Environme
+00000ba0: 6e74 2066 696c 6520 6e6f 7420 666f 756e  nt file not foun
+00000bb0: 642c 2063 7265 6174 696e 6720 6f6e 6520  d, creating one 
+00000bc0: 7769 7468 2064 6566 6175 6c74 733a 2065  with defaults: e
+00000bd0: 6e76 2e6a 736f 6e72 3700 0000 6301 0000  nv.jsonr7...c...
+00000be0: 0000 0000 0000 0000 0002 0000 0004 0000  ................
+00000bf0: 0053 0000 0073 1200 0000 6900 7c00 5d05  .S...s....i.|.].
+00000c00: 7d01 7c01 6400 9302 7102 5300 2901 da00  }.|.d...q.S.)...
+00000c10: 7223 0000 0029 02da 022e 3072 2100 0000  r#...)....0r!...
+00000c20: 7223 0000 0072 2300 0000 7224 0000 00da  r#...r#...r$....
+00000c30: 0a3c 6469 6374 636f 6d70 3e7f 0000 0073  .<dictcomp>....s
+00000c40: 0200 0000 1200 7a29 456e 7669 726f 6e6d  ......z)Environm
+00000c50: 656e 742e 5f5f 7365 745f 656e 762e 3c6c  ent.__set_env.<l
+00000c60: 6f63 616c 733e 2e3c 6469 6374 636f 6d70  ocals>.<dictcomp
+00000c70: 3e72 3900 0000 7207 0000 0072 3a00 0000  >r9...r....r:...
+00000c80: 7243 0000 0072 0100 0000 7a47 456e 7669  rC...r....zGEnvi
+00000c90: 726f 6e6d 656e 7420 7661 7269 6162 6c65  ronment variable
+00000ca0: 7320 6e6f 7420 666f 756e 642e 2053 6574  s not found. Set
+00000cb0: 2074 6865 6d20 696e 2065 6e76 2e6a 736f   them in env.jso
+00000cc0: 6e20 6f72 2069 6e20 796f 7572 2073 6865  n or in your she
+00000cd0: 6c6c 2e7a 1d52 6571 7569 7265 6420 656e  ll.z.Required en
+00000ce0: 7669 726f 6e6d 656e 7420 7661 7269 6162  vironment variab
+00000cf0: 6c65 7a03 203a 20fa 0a45 7869 7469 6e67  lez. : ..Exiting
+00000d00: 2e2e 2e72 0400 0000 5a09 6175 746f 5f73  ...r....Z.auto_s
+00000d10: 6176 6572 0900 0000 7a59 7265 7375 6c74  aver....zYresult
+00000d20: 732f 7361 7665 5f64 6972 2f73 6176 6520  s/save_dir/save 
+00000d30: 656e 7669 726f 6e6d 656e 7420 7661 7269  environment vari
+00000d40: 6162 6c65 2069 7320 656d 7074 792e 2053  able is empty. S
+00000d50: 6574 2069 7420 696e 2065 6e76 2e6a 736f  et it in env.jso
+00000d60: 6e20 6f72 2069 6e20 796f 7572 2073 6865  n or in your she
+00000d70: 6c6c 2e72 0200 0000 2917 7219 0000 0072  ll.r....).r....r
+00000d80: 1a00 0000 721b 0000 0072 3300 0000 7234  ....r....r3...r4
+00000d90: 0000 0072 3500 0000 7232 0000 00da 0570  ...r5...r2.....p
+00000da0: 7269 6e74 da07 454e 565f 4b45 59da 046b  rint..ENV_KEY..k
+00000db0: 6579 7372 3f00 0000 da07 6465 636f 6465  eysr?.....decode
+00000dc0: 725a 0f4a 534f 4e44 6563 6f64 6545 7272  rZ.JSONDecodeErr
+00000dd0: 6f72 da05 6974 656d 73da 0765 6e76 6972  or..items..envir
+00000de0: 6f6e da06 6170 7065 6e64 da03 6c65 6e72  on..append..lenr
+00000df0: 1000 0000 da04 6578 6974 721c 0000 0072  ......exitr....r
+00000e00: 1500 0000 da03 6765 7472 0f00 0000 290d  ......getr....).
+00000e10: 721f 0000 005a 0e6d 6174 655f 636f 6e66  r....Z.mate_conf
+00000e20: 5f70 6174 6872 3600 0000 5a08 656e 765f  _pathr6...Z.env_
+00000e30: 7061 7468 da0d 7265 7175 6972 6564 5f6b  path..required_k
+00000e40: 6579 735a 0b64 6566 7561 6c74 5f65 6e76  eysZ.defualt_env
+00000e50: 7242 0000 0072 0200 0000 5a0d 656e 765f  rB...r....Z.env_
+00000e60: 6e6f 745f 666f 756e 6472 2100 0000 7222  not_foundr!...r"
+00000e70: 0000 005a 0464 6573 635a 0e73 6561 7263  ...Z.descZ.searc
+00000e80: 685f 7265 7375 6c74 7372 2300 0000 7223  h_resultsr#...r#
+00000e90: 0000 0072 2400 0000 5a09 5f5f 7365 745f  ...r$...Z.__set_
+00000ea0: 656e 7672 0000 0073 6e00 0000 0c01 1001  envr...sn.......
+00000eb0: 0c02 0c01 0801 0802 0e01 0602 0e02 0c02  ................
+00000ec0: 1201 1cff 0c03 0201 0e01 1001 0402 08ff  ................
+00000ed0: 02ff 0280 1cfd 0408 0802 1001 0c01 0a01  ................
+00000ee0: 1001 0a03 0801 0280 0c02 0201 0201 04ff  ................
+00000ef0: 0802 1c01 1401 0802 0a01 0603 0801 0801  ................
+00000f00: 2401 0402 2801 1001 0402 0280 0e02 0201  $...(...........
+00000f10: 0201 04ff 0802 0a01 1002 7a15 456e 7669  ..........z.Envi
+00000f20: 726f 6e6d 656e 742e 5f5f 7365 745f 656e  ronment.__set_en
+00000f30: 7663 0200 0000 0000 0000 0000 0000 0300  vc..............
+00000f40: 0000 0400 0000 0300 0000 73aa 0000 0074  ..........s....t
+00000f50: 006a 01a0 027c 0164 00a1 027d 027c 0264  .j...|.d...}.|.d
+00000f60: 0075 0172 0d7c 0253 007c 017c 0076 0172  .u.r.|.S.|.|.v.r
+00000f70: 4f7c 017c 006a 0376 0072 1b7c 006a 037c  O|.|.j.v.r.|.j.|
+00000f80: 0119 0053 007c 017c 006a 0476 0072 257c  ...S.|.|.j.v.r%|
+00000f90: 006a 047c 0119 0053 007c 017c 006a 0576  .j.|...S.|.|.j.v
+00000fa0: 0072 2f7c 006a 057c 0119 0053 007c 0264  .r/|.j.|...S.|.d
+00000fb0: 0075 0073 377c 0264 016b 0272 4d74 0664  .u.s7|.d.k.rMt.d
+00000fc0: 027c 019b 0064 039d 0383 0101 0074 0664  .|...d.......t.d
+00000fd0: 0483 0101 0074 0664 0583 0101 0074 07a0  .....t.d.....t..
+00000fe0: 0864 06a1 0101 006e 027c 0253 0074 0983  .d.....n.|.S.t..
+00000ff0: 00a0 0a7c 01a1 0153 0029 074e 7243 0000  ...|...S.).NrC..
+00001000: 007a 1545 6e76 6972 6f6e 6d65 6e74 2076  .z.Environment v
+00001010: 6172 6961 626c 6520 7a30 206e 6f74 2066  ariable z0 not f
+00001020: 6f75 6e64 2e20 5365 7420 6974 2069 6e20  ound. Set it in 
+00001030: 656e 762e 6a73 6f6e 206f 7220 696e 2079  env.json or in y
+00001040: 6f75 7220 7368 656c 6c2e 7a48 4f72 2073  our shell.zHOr s
+00001050: 6574 2061 7320 616e 2061 7267 756d 656e  et as an argumen
+00001060: 7420 746f 2074 6865 2073 6372 6970 743a  t to the script:
+00001070: 2070 7974 686f 6e20 2d6d 206d 6f64 756c   python -m modul
+00001080: 652e 7472 6169 6e20 6172 673d 3120 6172  e.train arg=1 ar
+00001090: 6732 3d32 7246 0000 0072 0400 0000 290b  g2=2rF...r....).
+000010a0: 7219 0000 0072 4c00 0000 7250 0000 0072  r....rL...rP...r
+000010b0: 0200 0000 720e 0000 00da 085f 5f64 6963  ....r......__dic
+000010c0: 745f 5f72 4700 0000 7210 0000 0072 4f00  t__rG...r....rO.
+000010d0: 0000 da05 7375 7065 72da 0b5f 5f67 6574  ....super..__get
+000010e0: 6974 656d 5f5f 2903 721f 0000 0072 2100  item__).r....r!.
+000010f0: 0000 da03 7265 73a9 01da 095f 5f63 6c61  ....res....__cla
+00001100: 7373 5f5f 7223 0000 0072 2400 0000 7254  ss__r#...r$...rT
+00001110: 0000 00b6 0000 0073 2a00 0000 0e04 0802  .......s*.......
+00001120: 0401 0802 0a03 0a01 0a02 0a01 0a02 0a01  ................
+00001130: 1002 0201 0a01 04ff 0202 0201 04ff 0802  ................
+00001140: 0c01 0402 0c02 7a17 456e 7669 726f 6e6d  ......z.Environm
+00001150: 656e 742e 5f5f 6765 7469 7465 6d5f 5f29  ent.__getitem__)
+00001160: 0ada 085f 5f6e 616d 655f 5fda 0a5f 5f6d  ...__name__..__m
+00001170: 6f64 756c 655f 5fda 0c5f 5f71 7561 6c6e  odule__..__qualn
+00001180: 616d 655f 5f72 2500 0000 7216 0000 0072  ame__r%...r....r
+00001190: 1300 0000 721e 0000 0072 1d00 0000 7254  ....r....r....rT
+000011a0: 0000 00da 0d5f 5f63 6c61 7373 6365 6c6c  .....__classcell
+000011b0: 5f5f 7223 0000 0072 2300 0000 7256 0000  __r#...r#...rV..
+000011c0: 0072 2400 0000 7203 0000 000c 0000 0073  .r$...r........s
+000011d0: 0e00 0000 0800 0802 082f 080e 080c 081b  ........./......
+000011e0: 1444 7203 0000 0029 0872 3300 0000 7219  .Dr....).r3...r.
+000011f0: 0000 0072 3d00 0000 7210 0000 005a 0469  ...r=...r....Z.i
+00001200: 7064 6272 4800 0000 7240 0000 0072 0300  pdbrH...r@...r..
+00001210: 0000 7223 0000 0072 2300 0000 7223 0000  ..r#...r#...r#..
+00001220: 0072 2400 0000 da08 3c6d 6f64 756c 653e  .r$.....<module>
+00001230: 0100 0000 730e 0000 0008 0108 0108 0108  ....s...........
+00001240: 0108 0104 0314 03                        .......
```

### Comparing `yerbamate-0.9.236/packages/yerbamate/__pycache__/mate.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/__pycache__/mate.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/__pycache__/mate_cli.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/__pycache__/mate_cli.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/__pycache__/mate_api.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/__pycache__/mate_api.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/__pycache__/module_manager.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/__pycache__/module_manager.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/__pycache__/module_repository.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/__pycache__/module_repository.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/__pycache__/package.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/__pycache__/package.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/module_manager.py` & `yerbamate-0.9.237/packages/yerbamate/api/data/module_manager.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/module_repository.py` & `yerbamate-0.9.237/packages/yerbamate/api/data/module_repository.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/package.py` & `yerbamate-0.9.237/packages/yerbamate/api/data/package.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/sources/__pycache__/source.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/sources/__pycache__/source.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/__pycache__/io.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/__pycache__/io.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/__pycache__/local.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/__pycache__/local.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/io.py` & `yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/io.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/sources/local/local.py` & `yerbamate-0.9.237/packages/yerbamate/api/data/sources/local/local.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/sources/remote/__pycache__/remote.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/sources/remote/__pycache__/remote.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/sources/remote/remote.py` & `yerbamate-0.9.237/packages/yerbamate/api/data/sources/remote/remote.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/utils/__pycache__/exp_util.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/utils/__pycache__/exp_util.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/utils/__pycache__/git_util.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/utils/__pycache__/git_util.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/utils/__pycache__/gitdir.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/api/data/utils/__pycache__/gitdir.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/utils/git_util.py` & `yerbamate-0.9.237/packages/yerbamate/api/data/utils/git_util.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/data/utils/gitdir.py` & `yerbamate-0.9.237/packages/yerbamate/api/data/utils/gitdir.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/api/mate_api.py` & `yerbamate-0.9.237/packages/yerbamate/api/mate_api.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/environment.py` & `yerbamate-0.9.237/packages/yerbamate/environment.py`

 * *Files 17% similar despite different names*

```diff
@@ -32,14 +32,18 @@
 
         # parse python -m module train arg=1 arg2=2
         for arg in sys.argv:
             if "=" not in arg:
                 continue
             key, value = arg.split("=")
             value = self.convert_str_to_data(value)
+
+            if key.startswith("--"):
+                key = key[2:]
+
             setattr(self, key, value)
             self.hparams[key] = value
 
         self._path = sys.argv[0]
         if "bin/mate" in self._path:
             self.name = os.path.join(*sys.argv[2:4])
             self._path = os.path.join(
@@ -186,16 +190,54 @@
 
         if not key in self:
             # ipdb.set_trace()
 
             if key in self.env:
                 return self.env[key]
 
+            if key in self.hparams:
+                return self.hparams[key]
+
+            if key in self.__dict__:
+                return self.__dict__[key]
+
             if res is None or res == "":
                 print(
                     f"Environment variable {key} not found. Set it in env.json or in your shell.")
+                print(
+                    "Or set as an argument to the script: python -m module.train arg=1 arg2=2")
                 print("Exiting...")
                 sys.exit(1)
             else:
                 return res
 
         return super().__getitem__(key)
+
+    def __getitem__(self, key, default=None):
+
+        # default to environment variables
+        res = os.environ.get(key, None)
+
+        if res is not None:
+            return res
+
+        if key in self:
+            return super().__getitem__(key)
+
+            # ipdb.set_trace()
+
+        if key in self.env:
+            return self.env[key]
+
+        if key in self.hparams:
+            return self.hparams[key]
+
+        if key in self.__dict__:
+            return self.__dict__[key]
+
+        return default
+
+    def get_item(self, key, default=None):
+        return self.__getitem__(key, default)
+
+    def get_hparam(self, key, default=None):
+        return self.__getitem__(key, default)
```

### Comparing `yerbamate-0.9.236/packages/yerbamate/mate.py` & `yerbamate-0.9.237/packages/yerbamate/mate.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/mate_cli.py` & `yerbamate-0.9.237/packages/yerbamate/mate_cli.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/utils/__init__.py` & `yerbamate-0.9.237/packages/yerbamate/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/utils/__pycache__/__init__.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/utils/__pycache__/__init__.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/utils/__pycache__/bunch.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/utils/__pycache__/bunch.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/utils/__pycache__/utils.cpython-310.pyc` & `yerbamate-0.9.237/packages/yerbamate/utils/__pycache__/utils.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/utils/bunch.py` & `yerbamate-0.9.237/packages/yerbamate/utils/bunch.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/utils/git_url_parser.py` & `yerbamate-0.9.237/packages/yerbamate/utils/git_url_parser.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/utils/utils.py` & `yerbamate-0.9.237/packages/yerbamate/utils/utils.py`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate/yerbamate.egg-info/PKG-INFO` & `yerbamate-0.9.237/packages/yerbamate/yerbamate.egg-info/PKG-INFO`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/packages/yerbamate.egg-info/PKG-INFO` & `yerbamate-0.9.237/packages/yerbamate.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yerbamate
-Version: 0.9.236
+Version: 0.9.237
 Summary:  A python module and experiment manager for deep learning
 Home-page: https://github.com/oalee/yerbamate
 Author: Giulio Zani, Ali Rahimi
 Author-email: yerba.mate.dl@proton.me
 License: Apache License 2.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
```

### Comparing `yerbamate-0.9.236/packages/yerbamate.egg-info/SOURCES.txt` & `yerbamate-0.9.237/packages/yerbamate.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `yerbamate-0.9.236/setup.py` & `yerbamate-0.9.237/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 setup(
     name="yerbamate",
     description=" A python module and experiment manager for deep learning",
     author="Giulio Zani, Ali Rahimi",
     author_email="yerba.mate.dl@proton.me",
     url="https://github.com/oalee/yerbamate",
     python_requires=">=3.6",
-    version="0.9.236",
+    version="0.9.237",
     packages=find_packages("packages", exclude=["tests"]),
     include_package_data=True,
     package_dir={"": "packages/"},
     license="Apache License 2.0",
     license_files=("LICENSE",),
     long_description=long_description,
     long_description_content_type='text/markdown',
```

