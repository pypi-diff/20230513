# Comparing `tmp/NikGapps-0.1.tar.gz` & `tmp/NikGapps-1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "NikGapps-0.1.tar", last modified: Sat May 13 00:04:01 2023, max compression
+gzip compressed data, was "NikGapps-1.0.tar", last modified: Sat May 13 00:52:27 2023, max compression
```

## Comparing `NikGapps-0.1.tar` & `NikGapps-1.0.tar`

### file list

```diff
@@ -1,54 +1,54 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/
--rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-05-13 00:03:50.000000 NikGapps-0.1/LICENSE
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.042800 NikGapps-0.1/NikGapps/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.042800 NikGapps-0.1/NikGapps/build/
--rw-r--r--   0 runner    (1001) docker     (123)     6582 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/Build.py
--rw-r--r--   0 runner    (1001) docker     (123)    48873 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/NikGappsPackages.py
--rw-r--r--   0 runner    (1001) docker     (123)     5801 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/Operation.py
--rw-r--r--   0 runner    (1001) docker     (123)     7679 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/Release.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/build/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/NikGapps/helper/
--rw-r--r--   0 runner    (1001) docker     (123)      352 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/AppSet.py
--rw-r--r--   0 runner    (1001) docker     (123)     2750 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Args.py
--rw-r--r--   0 runner    (1001) docker     (123)     2139 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Assets.py
--rw-r--r--   0 runner    (1001) docker     (123)      871 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/B64.py
--rw-r--r--   0 runner    (1001) docker     (123)    13248 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Cmd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2585 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Config.py
--rw-r--r--   0 runner    (1001) docker     (123)      462 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/ConfigObj.py
--rw-r--r--   0 runner    (1001) docker     (123)     6458 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/FileOp.py
--rw-r--r--   0 runner    (1001) docker     (123)    11463 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/NikGappsConfig.py
--rw-r--r--   0 runner    (1001) docker     (123)      516 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/P.py
--rw-r--r--   0 runner    (1001) docker     (123)    14321 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Package.py
--rw-r--r--   0 runner    (1001) docker     (123)     3530 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/Statics.py
--rw-r--r--   0 runner    (1001) docker     (123)      852 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/SystemStat.py
--rw-r--r--   0 runner    (1001) docker     (123)     2206 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/T.py
--rw-r--r--   0 runner    (1001) docker     (123)     1130 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/XmlOp.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/NikGapps/helper/compression/
--rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/CompOps.py
--rw-r--r--   0 runner    (1001) docker     (123)    11052 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Export.py
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Modes.py
--rw-r--r--   0 runner    (1001) docker     (123)      794 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Tar.py
--rw-r--r--   0 runner    (1001) docker     (123)      444 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Zip.py
--rw-r--r--   0 runner    (1001) docker     (123)      481 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/Zsh.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/compression/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/NikGapps/helper/git/
--rw-r--r--   0 runner    (1001) docker     (123)     6247 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/git/Git.py
--rw-r--r--   0 runner    (1001) docker     (123)     3145 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/git/GitOperations.py
--rw-r--r--   0 runner    (1001) docker     (123)      629 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/git/GitStatics.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/git/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.046800 NikGapps-0.1/NikGapps/helper/web/
--rw-r--r--   0 runner    (1001) docker     (123)     1472 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/web/Requests.py
--rw-r--r--   0 runner    (1001) docker     (123)     4651 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/web/TelegramApi.py
--rw-r--r--   0 runner    (1001) docker     (123)     4168 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/web/Upload.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:03:50.000000 NikGapps-0.1/NikGapps/helper/web/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:04:01.042800 NikGapps-0.1/NikGapps.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-05-13 00:04:01.000000 NikGapps-0.1/NikGapps.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1249 2023-05-13 00:04:01.000000 NikGapps-0.1/NikGapps.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:04:01.000000 NikGapps-0.1/NikGapps.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 00:04:01.000000 NikGapps-0.1/NikGapps.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-05-13 00:04:01.046800 NikGapps-0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4870 2023-05-13 00:03:50.000000 NikGapps-0.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 00:04:01.046800 NikGapps-0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 00:03:50.000000 NikGapps-0.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:27.619042 NikGapps-1.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-05-13 00:52:08.000000 NikGapps-1.0/LICENSE
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:27.611041 NikGapps-1.0/NikGapps/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:27.615042 NikGapps-1.0/NikGapps/build/
+-rw-r--r--   0 runner    (1001) docker     (123)     6582 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/build/Build.py
+-rw-r--r--   0 runner    (1001) docker     (123)    48873 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/build/NikGappsPackages.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5801 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/build/Operation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7679 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/build/Release.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/build/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:27.615042 NikGapps-1.0/NikGapps/helper/
+-rw-r--r--   0 runner    (1001) docker     (123)      352 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/AppSet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2750 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/Args.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2139 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/Assets.py
+-rw-r--r--   0 runner    (1001) docker     (123)      871 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/B64.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13248 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/Cmd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2585 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/Config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      462 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/ConfigObj.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6458 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/FileOp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11463 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/NikGappsConfig.py
+-rw-r--r--   0 runner    (1001) docker     (123)      516 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/P.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14321 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/Package.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3530 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/Statics.py
+-rw-r--r--   0 runner    (1001) docker     (123)      852 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/SystemStat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2206 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/T.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1130 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/XmlOp.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:27.615042 NikGapps-1.0/NikGapps/helper/compression/
+-rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/compression/CompOps.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11052 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/compression/Export.py
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/compression/Modes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      794 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/compression/Tar.py
+-rw-r--r--   0 runner    (1001) docker     (123)      444 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/compression/Zip.py
+-rw-r--r--   0 runner    (1001) docker     (123)      481 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/compression/Zsh.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/compression/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:27.615042 NikGapps-1.0/NikGapps/helper/git/
+-rw-r--r--   0 runner    (1001) docker     (123)     6247 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/git/Git.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3145 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/git/GitOperations.py
+-rw-r--r--   0 runner    (1001) docker     (123)      629 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/git/GitStatics.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/git/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:27.619042 NikGapps-1.0/NikGapps/helper/web/
+-rw-r--r--   0 runner    (1001) docker     (123)     1472 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/web/Requests.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4651 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/web/TelegramApi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4168 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/web/Upload.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:08.000000 NikGapps-1.0/NikGapps/helper/web/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:52:27.611041 NikGapps-1.0/NikGapps.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-05-13 00:52:27.000000 NikGapps-1.0/NikGapps.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1249 2023-05-13 00:52:27.000000 NikGapps-1.0/NikGapps.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:52:27.000000 NikGapps-1.0/NikGapps.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 00:52:27.000000 NikGapps-1.0/NikGapps.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-05-13 00:52:27.619042 NikGapps-1.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4870 2023-05-13 00:52:08.000000 NikGapps-1.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 00:52:27.619042 NikGapps-1.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      542 2023-05-13 00:52:19.000000 NikGapps-1.0/setup.py
```

### Comparing `NikGapps-0.1/LICENSE` & `NikGapps-1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/build/Build.py` & `NikGapps-1.0/NikGapps/build/Build.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/build/NikGappsPackages.py` & `NikGapps-1.0/NikGapps/build/NikGappsPackages.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/build/Operation.py` & `NikGapps-1.0/NikGapps/build/Operation.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/build/Release.py` & `NikGapps-1.0/NikGapps/build/Release.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/Args.py` & `NikGapps-1.0/NikGapps/helper/Args.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/Assets.py` & `NikGapps-1.0/NikGapps/helper/Assets.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/B64.py` & `NikGapps-1.0/NikGapps/helper/B64.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/Cmd.py` & `NikGapps-1.0/NikGapps/helper/Cmd.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/Config.py` & `NikGapps-1.0/NikGapps/helper/Config.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/FileOp.py` & `NikGapps-1.0/NikGapps/helper/FileOp.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/NikGappsConfig.py` & `NikGapps-1.0/NikGapps/helper/NikGappsConfig.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/P.py` & `NikGapps-1.0/NikGapps/helper/P.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/Package.py` & `NikGapps-1.0/NikGapps/helper/Package.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/Statics.py` & `NikGapps-1.0/NikGapps/helper/Statics.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/SystemStat.py` & `NikGapps-1.0/NikGapps/helper/SystemStat.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/T.py` & `NikGapps-1.0/NikGapps/helper/T.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/XmlOp.py` & `NikGapps-1.0/NikGapps/helper/XmlOp.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/compression/Export.py` & `NikGapps-1.0/NikGapps/helper/compression/Export.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/compression/Tar.py` & `NikGapps-1.0/NikGapps/helper/compression/Tar.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/git/Git.py` & `NikGapps-1.0/NikGapps/helper/git/Git.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/git/GitOperations.py` & `NikGapps-1.0/NikGapps/helper/git/GitOperations.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/git/GitStatics.py` & `NikGapps-1.0/NikGapps/helper/git/GitStatics.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/web/Requests.py` & `NikGapps-1.0/NikGapps/helper/web/Requests.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/web/TelegramApi.py` & `NikGapps-1.0/NikGapps/helper/web/TelegramApi.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps/helper/web/Upload.py` & `NikGapps-1.0/NikGapps/helper/web/Upload.py`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/NikGapps.egg-info/PKG-INFO` & `NikGapps-1.0/NikGapps.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: NikGapps
-Version: 0.1
+Version: 1.0
 Summary: A short description of your project
 Home-page: https://github.com/nikgapps/project
 Author: Nikhil Menghani
 Author-email: nikgapps@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.10
```

### Comparing `NikGapps-0.1/NikGapps.egg-info/SOURCES.txt` & `NikGapps-1.0/NikGapps.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/PKG-INFO` & `NikGapps-1.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: NikGapps
-Version: 0.1
+Version: 1.0
 Summary: A short description of your project
 Home-page: https://github.com/nikgapps/project
 Author: Nikhil Menghani
 Author-email: nikgapps@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.10
```

### Comparing `NikGapps-0.1/README.md` & `NikGapps-1.0/README.md`

 * *Files identical despite different names*

### Comparing `NikGapps-0.1/setup.py` & `NikGapps-1.0/setup.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="NikGapps",
-    version="0.1",
+version="v1.0",
     packages=find_packages(),
     author="Nikhil Menghani",
     author_email="nikgapps@gmail.com",
     description="A short description of your project",
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/nikgapps/project",
```

