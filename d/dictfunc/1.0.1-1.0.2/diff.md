# Comparing `tmp/dictfunc-1.0.1.tar.gz` & `tmp/dictfunc-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dictfunc-1.0.1.tar", last modified: Sat May 13 14:32:49 2023, max compression
+gzip compressed data, was "dictfunc-1.0.2.tar", last modified: Sat May 13 14:35:18 2023, max compression
```

## Comparing `dictfunc-1.0.1.tar` & `dictfunc-1.0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:32:49.547737 dictfunc-1.0.1/
--rw-rw-rw-   0        0        0     1091 2023-05-08 14:09:39.000000 dictfunc-1.0.1/LICENSE
--rw-rw-rw-   0        0        0      659 2023-05-13 14:32:49.546736 dictfunc-1.0.1/PKG-INFO
--rw-rw-rw-   0        0        0       60 2023-05-08 14:09:39.000000 dictfunc-1.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 14:32:49.534738 dictfunc-1.0.1/dictfunc/
--rw-rw-rw-   0        0        0       24 2023-05-08 14:12:59.000000 dictfunc-1.0.1/dictfunc/__init__.py
--rw-rw-rw-   0        0        0     4724 2023-05-08 14:04:54.000000 dictfunc-1.0.1/dictfunc/dictfunc.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:32:49.544738 dictfunc-1.0.1/dictfunc.egg-info/
--rw-rw-rw-   0        0        0      659 2023-05-13 14:32:49.000000 dictfunc-1.0.1/dictfunc.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      196 2023-05-13 14:32:49.000000 dictfunc-1.0.1/dictfunc.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:32:49.000000 dictfunc-1.0.1/dictfunc.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-05-13 14:32:49.000000 dictfunc-1.0.1/dictfunc.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 14:32:49.547737 dictfunc-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1106 2023-05-13 14:32:11.000000 dictfunc-1.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:35:18.829815 dictfunc-1.0.2/
+-rw-rw-rw-   0        0        0     1091 2023-05-08 14:09:39.000000 dictfunc-1.0.2/LICENSE
+-rw-rw-rw-   0        0        0      698 2023-05-13 14:35:18.828813 dictfunc-1.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0       60 2023-05-08 14:09:39.000000 dictfunc-1.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 14:35:18.811814 dictfunc-1.0.2/dictfunc/
+-rw-rw-rw-   0        0        0       24 2023-05-08 14:12:59.000000 dictfunc-1.0.2/dictfunc/__init__.py
+-rw-rw-rw-   0        0        0     4724 2023-05-08 14:04:54.000000 dictfunc-1.0.2/dictfunc/dictfunc.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:35:18.826825 dictfunc-1.0.2/dictfunc.egg-info/
+-rw-rw-rw-   0        0        0      698 2023-05-13 14:35:18.000000 dictfunc-1.0.2/dictfunc.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      196 2023-05-13 14:35:18.000000 dictfunc-1.0.2/dictfunc.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:35:18.000000 dictfunc-1.0.2/dictfunc.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 14:35:18.000000 dictfunc-1.0.2/dictfunc.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:35:18.829815 dictfunc-1.0.2/setup.cfg
+-rw-rw-rw-   0        0        0     1145 2023-05-13 14:34:55.000000 dictfunc-1.0.2/setup.py
```

### Comparing `dictfunc-1.0.1/LICENSE` & `dictfunc-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `dictfunc-1.0.1/PKG-INFO` & `dictfunc-1.0.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: dictfunc
-Version: 1.0.1
-Summary: Python dictionary functions.
+Version: 1.0.2
+Summary: Python dictionary functions. (https://github.com/YHordijk/dictfunc)
 Home-page: UNKNOWN
 Author: YHordijk (Yuman Hordijk)
 Author-email: <yumanhordijk@gmail.com>
 License: UNKNOWN
 Description: 
         # dictfunc
         Helper functions for Python dictionary objects
```

### Comparing `dictfunc-1.0.1/dictfunc/dictfunc.py` & `dictfunc-1.0.2/dictfunc/dictfunc.py`

 * *Files identical despite different names*

### Comparing `dictfunc-1.0.1/dictfunc.egg-info/PKG-INFO` & `dictfunc-1.0.2/dictfunc.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: dictfunc
-Version: 1.0.1
-Summary: Python dictionary functions.
+Version: 1.0.2
+Summary: Python dictionary functions. (https://github.com/YHordijk/dictfunc)
 Home-page: UNKNOWN
 Author: YHordijk (Yuman Hordijk)
 Author-email: <yumanhordijk@gmail.com>
 License: UNKNOWN
 Description: 
         # dictfunc
         Helper functions for Python dictionary objects
```

### Comparing `dictfunc-1.0.1/setup.py` & `dictfunc-1.0.2/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -3,16 +3,16 @@
 import os
 
 here = os.path.abspath(os.path.dirname(__file__))
 
 with codecs.open(os.path.join(here, "README.md"), encoding="utf-8") as fh:
     long_description = "\n" + fh.read()
 
-VERSION = '1.0.1'
-DESCRIPTION = 'Python dictionary functions.'
+VERSION = '1.0.2'
+DESCRIPTION = 'Python dictionary functions. (https://github.com/YHordijk/dictfunc)'
 LONG_DESCRIPTION = 'Helper functions for Python dictionary objects.\nGithub repository here: https://github.com/YHordijk/dictfunc'
 
 # Setting up
 setup(
     name="dictfunc",
     version=VERSION,
     author="YHordijk (Yuman Hordijk)",
```

