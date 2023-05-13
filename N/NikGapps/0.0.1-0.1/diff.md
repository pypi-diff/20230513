# Comparing `tmp/NikGapps-0.0.1.tar.gz` & `tmp/NikGapps-0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "NikGapps-0.0.1.tar", last modified: Fri May 12 23:04:02 2023, max compression
+gzip compressed data, was "NikGapps-0.1.tar", last modified: Sat May 13 00:04:01 2023, max compression
```

## Comparing `NikGapps-0.0.1.tar` & `NikGapps-0.1.tar`

### file list

```diff
@@ -1,56 +1,54 @@
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.093574 NikGapps-0.0.1/
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)    35149 2023-05-12 23:02:43.000000 NikGapps-0.0.1/LICENSE
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     5373 2023-05-12 23:04:02.089573 NikGapps-0.0.1/PKG-INFO
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     4870 2023-05-12 23:02:30.000000 NikGapps-0.0.1/README.md
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      576 2023-05-12 23:02:12.000000 NikGapps-0.0.1/pyproject.toml
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)       38 2023-05-12 23:04:02.093574 NikGapps-0.0.1/setup.cfg
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.081574 NikGapps-0.0.1/src/
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.081574 NikGapps-0.0.1/src/NikGapps/
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)        0 2023-05-03 21:48:00.000000 NikGapps-0.0.1/src/NikGapps/__init__.py
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.085574 NikGapps-0.0.1/src/NikGapps/build/
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     6538 2023-05-07 23:00:28.000000 NikGapps-0.0.1/src/NikGapps/build/Build.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)    48837 2023-05-09 22:37:10.000000 NikGapps-0.0.1/src/NikGapps/build/NikGappsPackages.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     5738 2023-05-12 03:01:15.000000 NikGapps-0.0.1/src/NikGapps/build/Operation.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     7598 2023-05-09 22:37:10.000000 NikGapps-0.0.1/src/NikGapps/build/Release.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)        0 2023-05-03 21:48:00.000000 NikGapps-0.0.1/src/NikGapps/build/__init__.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     1590 2023-05-12 20:24:04.000000 NikGapps-0.0.1/src/NikGapps/build/run.py
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.089573 NikGapps-0.0.1/src/NikGapps/helper/
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      358 2023-05-07 22:53:35.000000 NikGapps-0.0.1/src/NikGapps/helper/AppSet.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     2756 2023-05-07 20:21:19.000000 NikGapps-0.0.1/src/NikGapps/helper/Args.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     2139 2023-05-08 00:00:22.000000 NikGapps-0.0.1/src/NikGapps/helper/Assets.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      871 2023-05-03 03:58:54.000000 NikGapps-0.0.1/src/NikGapps/helper/B64.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)    13248 2023-05-03 04:08:45.000000 NikGapps-0.0.1/src/NikGapps/helper/Cmd.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     2584 2023-05-11 23:09:20.000000 NikGapps-0.0.1/src/NikGapps/helper/Config.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      462 2023-05-02 23:20:46.000000 NikGapps-0.0.1/src/NikGapps/helper/ConfigObj.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     6458 2023-05-09 23:16:18.000000 NikGapps-0.0.1/src/NikGapps/helper/FileOp.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)    11497 2023-05-10 21:46:26.000000 NikGapps-0.0.1/src/NikGapps/helper/NikGappsConfig.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      516 2023-05-03 03:56:00.000000 NikGapps-0.0.1/src/NikGapps/helper/P.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)    14351 2023-05-09 23:17:35.000000 NikGapps-0.0.1/src/NikGapps/helper/Package.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     3536 2023-05-09 23:17:02.000000 NikGapps-0.0.1/src/NikGapps/helper/Statics.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      864 2023-05-10 20:54:53.000000 NikGapps-0.0.1/src/NikGapps/helper/SystemStat.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     2212 2023-05-09 23:15:05.000000 NikGapps-0.0.1/src/NikGapps/helper/T.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     1130 2023-05-04 22:22:32.000000 NikGapps-0.0.1/src/NikGapps/helper/XmlOp.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)        0 2023-05-03 03:20:37.000000 NikGapps-0.0.1/src/NikGapps/helper/__init__.py
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.089573 NikGapps-0.0.1/src/NikGapps/helper/compression/
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      362 2023-05-07 23:45:46.000000 NikGapps-0.0.1/src/NikGapps/helper/compression/CompOps.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)    11077 2023-05-09 23:18:02.000000 NikGapps-0.0.1/src/NikGapps/helper/compression/Export.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)       71 2023-05-08 00:12:26.000000 NikGapps-0.0.1/src/NikGapps/helper/compression/Modes.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      799 2023-05-07 23:51:58.000000 NikGapps-0.0.1/src/NikGapps/helper/compression/Tar.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      449 2023-05-06 21:22:00.000000 NikGapps-0.0.1/src/NikGapps/helper/compression/Zip.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      486 2023-05-06 21:21:51.000000 NikGapps-0.0.1/src/NikGapps/helper/compression/Zsh.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)        0 2023-05-06 21:21:15.000000 NikGapps-0.0.1/src/NikGapps/helper/compression/__init__.py
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.089573 NikGapps-0.0.1/src/NikGapps/helper/git/
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     6281 2023-05-10 19:49:47.000000 NikGapps-0.0.1/src/NikGapps/helper/git/Git.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     3175 2023-05-11 23:27:36.000000 NikGapps-0.0.1/src/NikGapps/helper/git/GitOperations.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)      634 2023-05-09 23:02:32.000000 NikGapps-0.0.1/src/NikGapps/helper/git/GitStatics.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)        0 2023-05-06 15:57:33.000000 NikGapps-0.0.1/src/NikGapps/helper/git/__init__.py
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.089573 NikGapps-0.0.1/src/NikGapps/helper/web/
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     1472 2023-05-03 22:44:41.000000 NikGapps-0.0.1/src/NikGapps/helper/web/Requests.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     4661 2023-05-03 22:44:48.000000 NikGapps-0.0.1/src/NikGapps/helper/web/TelegramApi.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     4193 2023-05-09 23:20:54.000000 NikGapps-0.0.1/src/NikGapps/helper/web/Upload.py
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)        0 2023-05-03 22:06:12.000000 NikGapps-0.0.1/src/NikGapps/helper/web/__init__.py
-drwxrwxr-x   0 nikhil    (1000) nikhil    (1000)        0 2023-05-12 23:04:02.081574 NikGapps-0.0.1/src/NikGapps.egg-info/
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     5373 2023-05-12 23:04:02.000000 NikGapps-0.0.1/src/NikGapps.egg-info/PKG-INFO
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)     1445 2023-05-12 23:04:02.000000 NikGapps-0.0.1/src/NikGapps.egg-info/SOURCES.txt
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)        1 2023-05-12 23:04:02.000000 NikGapps-0.0.1/src/NikGapps.egg-info/dependency_links.txt
--rw-rw-r--   0 nikhil    (1000) nikhil    (1000)        9 2023-05-12 23:04:02.000000 NikGapps-0.0.1/src/NikGapps.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-05-13 00:03:50.000000 NikGapps-0.1/LICENSE
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.042800 NikGapps-0.1/NikGapps/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.042800 NikGapps-0.1/NikGapps/build/
+-rw-r--r--   0 runner    (1001) docker     (123)     6582 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/Build.py
+-rw-r--r--   0 runner    (1001) docker     (123)    48873 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/NikGappsPackages.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5801 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/Operation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7679 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/Release.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/NikGapps/helper/
+-rw-r--r--   0 runner    (1001) docker     (123)      352 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/AppSet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2750 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Args.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2139 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Assets.py
+-rw-r--r--   0 runner    (1001) docker     (123)      871 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/B64.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13248 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Cmd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2585 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      462 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/ConfigObj.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6458 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/FileOp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11463 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/NikGappsConfig.py
+-rw-r--r--   0 runner    (1001) docker     (123)      516 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/P.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14321 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Package.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3530 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Statics.py
+-rw-r--r--   0 runner    (1001) docker     (123)      852 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/SystemStat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2206 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/T.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1130 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/XmlOp.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/NikGapps/helper/compression/
+-rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/CompOps.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11052 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Export.py
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Modes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      794 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Tar.py
+-rw-r--r--   0 runner    (1001) docker     (123)      444 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Zip.py
+-rw-r--r--   0 runner    (1001) docker     (123)      481 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Zsh.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/NikGapps/helper/git/
+-rw-r--r--   0 runner    (1001) docker     (123)     6247 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/git/Git.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3145 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/git/GitOperations.py
+-rw-r--r--   0 runner    (1001) docker     (123)      629 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/git/GitStatics.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/git/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/NikGapps/helper/web/
+-rw-r--r--   0 runner    (1001) docker     (123)     1472 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/web/Requests.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4651 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/web/TelegramApi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4168 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/web/Upload.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/web/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.042800 NikGapps-0.1/NikGapps.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-05-13 00:04:01.000000 NikGapps-0.1/NikGapps.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1249 2023-05-13 00:04:01.000000 NikGapps-0.1/NikGapps.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:04:01.000000 NikGapps-0.1/NikGapps.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 00:04:01.000000 NikGapps-0.1/NikGapps.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-05-13 00:04:01.046800 NikGapps-0.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4870 2023-05-13 00:03:50.000000 NikGapps-0.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 00:04:01.046800 NikGapps-0.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 00:03:50.000000 NikGapps-0.1/setup.py
```

### Comparing `NikGapps-0.0.1/LICENSE` & `NikGapps-0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `NikGapps-0.0.1/PKG-INFO` & `NikGapps-0.1/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,21 +1,7 @@
-Metadata-Version: 2.1
-Name: NikGapps
-Version: 0.0.1
-Summary: A package that offers ability to build NikGapps
-Author-email: Nikhil Menghani <nikgapps@gmail.com>
-Project-URL: Homepage, https://nikgapps.com
-Project-URL: Bug Tracker, https://github.com/nikgapps/build/issues
-Classifier: Programming Language :: Python :: 3
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Operating System :: OS Independent
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 ![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/nikgapps-logo.webp)
 
 ## Introduction
 
 NikGapps project started with the goal to provide custom gapps packages that suits everyone's needs. A gapps package which is completely configurable, allows you to install exactly the set of google apps you want and It comes in 6 variants.   
 
 Here are some feature highlights:
```

### Comparing `NikGapps-0.0.1/README.md` & `NikGapps-0.1/NikGapps.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,7 +1,20 @@
+Metadata-Version: 2.1
+Name: NikGapps
+Version: 0.1
+Summary: A short description of your project
+Home-page: https://github.com/nikgapps/project
+Author: Nikhil Menghani
+Author-email: nikgapps@gmail.com
+Classifier: Programming Language :: Python :: 3
+Classifier: License :: OSI Approved :: MIT License
+Requires-Python: >=3.10
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
 ![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/nikgapps-logo.webp)
 
 ## Introduction
 
 NikGapps project started with the goal to provide custom gapps packages that suits everyone's needs. A gapps package which is completely configurable, allows you to install exactly the set of google apps you want and It comes in 6 variants.   
 
 Here are some feature highlights:
```

### Comparing `NikGapps-0.0.1/src/NikGapps/build/Build.py` & `NikGapps-0.1/NikGapps/build/Build.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,15 +1,14 @@
 import os
 from pathlib import Path
-from helper.Package import Package
-from helper.FileOp import FileOp
-from helper.Cmd import Cmd
-from helper.AppSet import AppSet
-
-from helper.Statics import Statics
+from NikGapps.helper.Package import Package
+from NikGapps.helper.FileOp import FileOp
+from NikGapps.helper.Cmd import Cmd
+from NikGapps.helper.AppSet import AppSet
+from NikGapps.helper.Statics import Statics
 
 
 class Build:
     project_name = "NikGapps"
 
     # Just provide the package list, and it will pick them up from the directory and build them for you
     @staticmethod
```

### Comparing `NikGapps-0.0.1/src/NikGapps/build/NikGappsPackages.py` & `NikGapps-0.1/NikGapps/build/NikGappsPackages.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
-from helper import Config
-from helper.Statics import Statics
-from helper.Package import Package
-from helper.AppSet import AppSet
+from NikGapps.helper import Config
+from NikGapps.helper.Statics import Statics
+from NikGapps.helper.Package import Package
+from NikGapps.helper.AppSet import AppSet
 
 
 class NikGappsPackages:
     all_packages = "full"
 
     @staticmethod
     def get_packages(package_type):
```

### Comparing `NikGapps-0.0.1/src/NikGapps/build/Operation.py` & `NikGapps-0.1/NikGapps/build/Operation.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,15 @@
-from helper.NikGappsConfig import NikGappsConfig
-from helper.git.GitOperations import GitOperations
-from helper.Statics import Statics
-from helper.web.TelegramApi import TelegramApi
-from helper.web.Upload import Upload
+from NikGapps.helper.NikGappsConfig import NikGappsConfig
+from NikGapps.helper.git.GitOperations import GitOperations
+from NikGapps.helper.Statics import Statics
+from NikGapps.helper.web.TelegramApi import TelegramApi
+from NikGapps.helper.web.Upload import Upload
 from Release import Release
-from helper.Config import FETCH_PACKAGE
-from helper import Config
+from NikGapps.helper.Config import FETCH_PACKAGE
+from NikGapps.helper import Config
 from colorama import Fore
 from ondemand.ConfigOperations import ConfigOperations
 
 
 class Operation:
 
     @staticmethod
```

### Comparing `NikGapps-0.0.1/src/NikGapps/build/Release.py` & `NikGapps-0.1/NikGapps/build/Release.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 import os
-from helper import Config
+from NikGapps.helper import Config
 from Build import Build
-from helper.NikGappsConfig import NikGappsConfig
-from helper.Statics import Statics
-from helper.T import T
-from helper.web.Upload import Upload
+from NikGapps.helper.NikGappsConfig import NikGappsConfig
+from NikGapps.helper.Statics import Statics
+from NikGapps.helper.T import T
+from NikGapps.helper.web.Upload import Upload
 from NikGappsPackages import NikGappsPackages
-from helper.compression.Export import Export
-from helper.Cmd import Cmd
-from helper.AppSet import AppSet
-from helper.Package import Package
+from NikGapps.helper.compression.Export import Export
+from NikGapps.helper.Cmd import Cmd
+from NikGapps.helper.AppSet import AppSet
+from NikGapps.helper.Package import Package
 
 
 class Release:
     @staticmethod
     def zip(build_package_list, android_version, sign_zip, send_zip_device, fresh_build, telegram,
             upload: Upload = None):
         release_directory = Statics.get_release_directory(android_version)
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/Args.py` & `NikGapps-0.1/NikGapps/helper/Args.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import argparse
 
-from helper.Statics import Statics
+from .Statics import Statics
 
 
 # from helper.B64 import B64
 
 
 class Args:
     def __init__(self) -> None:
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/Assets.py` & `NikGapps-0.1/NikGapps/helper/Assets.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/B64.py` & `NikGapps-0.1/NikGapps/helper/B64.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/Cmd.py` & `NikGapps-0.1/NikGapps/helper/Cmd.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/Config.py` & `NikGapps-0.1/NikGapps/helper/Config.py`

 * *Files 0% similar despite different names*

```diff
@@ -37,15 +37,15 @@
 if ENVIRONMENT_TYPE.__eq__("production"):
     DEBUG_MODE = False
 
 # True if we want the files to upload as soon as they get created
 UPLOAD_FILES = True
 
 # Override the execution if we re-trigger the workflow
-OVERRIDE_RELEASE = True
+OVERRIDE_RELEASE = False
 
 # Git Check enables controlled releases.
 # If this is set to True, new release will only happen when there is a change in the source repo or apk is updated
 GIT_CHECK = True
 GIT_PUSH = False
 
 # Enabling this will enable the feature of building NikGapps using config file
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/FileOp.py` & `NikGapps-0.1/NikGapps/helper/FileOp.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/NikGappsConfig.py` & `NikGapps-0.1/NikGapps/helper/NikGappsConfig.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,13 @@
-import json
-
-from helper.ConfigObj import ConfigObj
-from helper.FileOp import FileOp
-from helper.AppSet import AppSet
-from helper.Package import Package
-from build.NikGappsPackages import NikGappsPackages
-from helper.Statics import Statics
+from .ConfigObj import ConfigObj
+from .FileOp import FileOp
+from .AppSet import AppSet
+from .Package import Package
+from NikGapps.build.NikGappsPackages import NikGappsPackages
+from .Statics import Statics
 
 
 class NikGappsConfig:
 
     def __init__(self, android_version, config_path=None, config_version=None, use_zip_config=None, raw_config=None):
         self.config_version = Statics.config_versions[android_version]
         self.android_version = android_version
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/P.py` & `NikGapps-0.1/NikGapps/helper/P.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/Package.py` & `NikGapps-0.1/NikGapps/helper/Package.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import os.path
 from pathlib import Path
-from helper.Assets import Assets
-from helper.Statics import Statics
-from helper.XmlOp import XmlOp
-from helper.Cmd import Cmd
-from helper.FileOp import FileOp
+from .Assets import Assets
+from .Statics import Statics
+from .XmlOp import XmlOp
+from .Cmd import Cmd
+from .FileOp import FileOp
 
 
 class Package:
     def __init__(self, title, package_name, app_type, package_title=None, partition=None):
         self.package_name = package_name
         self.title = title
         self.package_title = package_title
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/Statics.py` & `NikGapps-0.1/NikGapps/helper/Statics.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import math
 import os
 from pathlib import Path
 
-from helper.T import T
+from .T import T
 
 
 class Statics:
     android_versions = {
         '10': {'sdk': '29', 'code': 'Q'},
         '11': {'sdk': '30', 'code': 'R'},
         '12': {'sdk': '31', 'code': 'S'},
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/SystemStat.py` & `NikGapps-0.1/NikGapps/helper/SystemStat.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import platform
 import psutil
-from helper.P import P
-from helper.T import T
+from .P import P
+from .T import T
 
 
 class SystemStat:
 
     @staticmethod
     def show_stats():
         mem = psutil.virtual_memory()
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/T.py` & `NikGapps-0.1/NikGapps/helper/T.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import math
 import os
 import time
 from datetime import datetime
 
 import pytz
 
-from helper.P import P
+from .P import P
 
 
 class T:
 
     def __init__(self):
         self.t = time.time()
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/XmlOp.py` & `NikGapps-0.1/NikGapps/helper/XmlOp.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/compression/Export.py` & `NikGapps-0.1/NikGapps/helper/compression/Export.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-from helper.FileOp import FileOp
-from helper.Assets import Assets
-from helper.Package import Package
-from helper.AppSet import AppSet
-from helper.Cmd import Cmd
+from ..FileOp import FileOp
+from ..Assets import Assets
+from ..Package import Package
+from ..AppSet import AppSet
+from ..Cmd import Cmd
 import os
 from .Zip import Zip
 from .CompOps import CompOps
 from .Modes import Modes
 from ..Statics import Statics
 from ..T import T
 from ..web.TelegramApi import TelegramApi
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/compression/Tar.py` & `NikGapps-0.1/NikGapps/helper/compression/Tar.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import tarfile
 from io import BytesIO
-from helper.FileOp import FileOp
+from ..FileOp import FileOp
 
 
 class Tar:
 
     def __init__(self, file_name, folder_to_compress=None):
         if folder_to_compress is None:
             self.folder = folder_to_compress
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/git/Git.py` & `NikGapps-0.1/NikGapps/helper/git/Git.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 import git.exc
 from git import Repo, Commit
 from shutil import copyfile
-from helper import Config
-from helper.FileOp import FileOp
-from helper.Assets import Assets
+from .. import Config
+from ..FileOp import FileOp
+from ..Assets import Assets
 import os
 import time
 import datetime
 from datetime import datetime
 import pytz
-from helper.git.GitStatics import GitStatics
-from helper.P import P
-from helper.T import T
+from .GitStatics import GitStatics
+from ..P import P
+from ..T import T
 
 
 class Git:
 
     def __init__(self, working_tree_dir, enable_push=Config.GIT_PUSH):
         self.enable_push = enable_push
         self.working_tree_dir = working_tree_dir
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/git/GitOperations.py` & `NikGapps-0.1/NikGapps/helper/git/GitOperations.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
-from helper.FileOp import FileOp
-from helper.git.Git import Git
-from helper.git.GitStatics import GitStatics
-from helper.Statics import Statics
+from ..FileOp import FileOp
+from .Git import Git
+from .GitStatics import GitStatics
+from ..Statics import Statics
 
 
 class GitOperations:
 
     @staticmethod
     def setup_tracker_repo(fresh_clone=True):
         print()
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/git/GitStatics.py` & `NikGapps-0.1/NikGapps/helper/git/GitStatics.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from helper.Statics import Statics
+from ..Statics import Statics
 
 
 class GitStatics:
     tracker_repo_url = "git@github.com:nikgapps/tracker.git"
     tracker_repo_dir = Statics.pwd + Statics.dir_sep + "tracker"
     apk_source_repo = f"https://gitlab.com/nikgapps/"
     release_repo_url = "git@github.com:nikgapps/release.git"
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/web/Requests.py` & `NikGapps-0.1/NikGapps/helper/web/Requests.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/web/TelegramApi.py` & `NikGapps-0.1/NikGapps/helper/web/TelegramApi.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import time
 
 import requests
 import yaml
 
-from helper.web.Requests import Requests
+from .Requests import Requests
 
 
 class TelegramApi:
 
     def __init__(self, token, chat_id, message_thread_id=None):
         self.token = token
         self.base = "https://api.telegram.org"
```

### Comparing `NikGapps-0.0.1/src/NikGapps/helper/web/Upload.py` & `NikGapps-0.1/NikGapps/helper/web/Upload.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import os
 import platform
 from pathlib import Path
 import pysftp
-from helper.FileOp import FileOp
-from helper.Statics import Statics
-from helper.T import T
-from helper.web.TelegramApi import TelegramApi
+from ..FileOp import FileOp
+from ..Statics import Statics
+from ..T import T
+from .TelegramApi import TelegramApi
 
 
 class Upload:
     def __init__(self, android_version, release_type, upload_files):
         self.android_version_code = Statics.get_android_code(android_version)
         self.upload_files = upload_files
         self.host = "frs.sourceforge.net"
```

### Comparing `NikGapps-0.0.1/src/NikGapps.egg-info/PKG-INFO` & `NikGapps-0.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 Metadata-Version: 2.1
 Name: NikGapps
-Version: 0.0.1
-Summary: A package that offers ability to build NikGapps
-Author-email: Nikhil Menghani <nikgapps@gmail.com>
-Project-URL: Homepage, https://nikgapps.com
-Project-URL: Bug Tracker, https://github.com/nikgapps/build/issues
+Version: 0.1
+Summary: A short description of your project
+Home-page: https://github.com/nikgapps/project
+Author: Nikhil Menghani
+Author-email: nikgapps@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
-Classifier: Operating System :: OS Independent
-Requires-Python: >=3.7
+Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 ![](https://raw.githubusercontent.com/nikgapps/nikgapps.github.io/master/images/nikgapps-logo.webp)
 
 ## Introduction
```

