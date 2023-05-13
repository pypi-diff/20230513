# Comparing `tmp/barbell2_xnat-0.1.0.tar.gz` & `tmp/barbell2_xnat-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/barbell2_xnat-0.1.0.tar", last modified: Sat Apr 22 10:15:50 2023, max compression
+gzip compressed data, was "barbell2_xnat-0.2.0.tar", last modified: Sat May 13 08:32:48 2023, max compression
```

## Comparing `barbell2_xnat-0.1.0.tar` & `barbell2_xnat-0.2.0.tar`

### file list

```diff
@@ -1,12 +1,12 @@
-drwxr-xr-x   0 ralph      (501) staff       (20)        0 2023-04-22 10:15:50.677885 barbell2_xnat-0.1.0/
--rw-r--r--   0 ralph      (501) staff       (20)      773 2023-04-22 10:15:50.677640 barbell2_xnat-0.1.0/PKG-INFO
-drwxr-xr-x   0 ralph      (501) staff       (20)        0 2023-04-22 10:15:50.677349 barbell2_xnat-0.1.0/barbell2_xnat.egg-info/
--rw-r--r--   0 ralph      (501) staff       (20)      773 2023-04-22 10:15:50.000000 barbell2_xnat-0.1.0/barbell2_xnat.egg-info/PKG-INFO
--rw-r--r--   0 ralph      (501) staff       (20)      268 2023-04-22 10:15:50.000000 barbell2_xnat-0.1.0/barbell2_xnat.egg-info/SOURCES.txt
--rw-r--r--   0 ralph      (501) staff       (20)        1 2023-04-22 10:15:50.000000 barbell2_xnat-0.1.0/barbell2_xnat.egg-info/dependency_links.txt
--rw-r--r--   0 ralph      (501) staff       (20)       20 2023-04-22 10:15:50.000000 barbell2_xnat-0.1.0/barbell2_xnat.egg-info/entry_points.txt
--rw-r--r--   0 ralph      (501) staff       (20)        1 2023-04-22 10:15:50.000000 barbell2_xnat-0.1.0/barbell2_xnat.egg-info/not-zip-safe
--rw-r--r--   0 ralph      (501) staff       (20)        5 2023-04-22 10:15:50.000000 barbell2_xnat-0.1.0/barbell2_xnat.egg-info/requires.txt
--rw-r--r--   0 ralph      (501) staff       (20)        1 2023-04-22 10:15:50.000000 barbell2_xnat-0.1.0/barbell2_xnat.egg-info/top_level.txt
--rw-r--r--   0 ralph      (501) staff       (20)       38 2023-04-22 10:15:50.677956 barbell2_xnat-0.1.0/setup.cfg
--rw-r--r--   0 ralph      (501) staff       (20)     1314 2023-04-22 09:11:31.000000 barbell2_xnat-0.1.0/setup.py
+drwxr-xr-x   0 Ralph      (501) staff       (20)        0 2023-05-13 08:32:48.967969 barbell2_xnat-0.2.0/
+-rw-r--r--   0 Ralph      (501) staff       (20)      773 2023-05-13 08:32:48.967702 barbell2_xnat-0.2.0/PKG-INFO
+drwxr-xr-x   0 Ralph      (501) staff       (20)        0 2023-05-13 08:32:48.967243 barbell2_xnat-0.2.0/barbell2_xnat.egg-info/
+-rw-r--r--   0 Ralph      (501) staff       (20)      773 2023-05-13 08:32:48.000000 barbell2_xnat-0.2.0/barbell2_xnat.egg-info/PKG-INFO
+-rw-r--r--   0 Ralph      (501) staff       (20)      268 2023-05-13 08:32:48.000000 barbell2_xnat-0.2.0/barbell2_xnat.egg-info/SOURCES.txt
+-rw-r--r--   0 Ralph      (501) staff       (20)        1 2023-05-13 08:32:48.000000 barbell2_xnat-0.2.0/barbell2_xnat.egg-info/dependency_links.txt
+-rw-r--r--   0 Ralph      (501) staff       (20)       20 2023-05-13 08:32:48.000000 barbell2_xnat-0.2.0/barbell2_xnat.egg-info/entry_points.txt
+-rw-r--r--   0 Ralph      (501) staff       (20)        1 2023-05-13 08:32:48.000000 barbell2_xnat-0.2.0/barbell2_xnat.egg-info/not-zip-safe
+-rw-r--r--   0 Ralph      (501) staff       (20)        5 2023-05-13 08:32:48.000000 barbell2_xnat-0.2.0/barbell2_xnat.egg-info/requires.txt
+-rw-r--r--   0 Ralph      (501) staff       (20)        1 2023-05-13 08:32:48.000000 barbell2_xnat-0.2.0/barbell2_xnat.egg-info/top_level.txt
+-rw-r--r--   0 Ralph      (501) staff       (20)       38 2023-05-13 08:32:48.968065 barbell2_xnat-0.2.0/setup.cfg
+-rw-r--r--   0 Ralph      (501) staff       (20)     1314 2023-05-13 08:32:29.000000 barbell2_xnat-0.2.0/setup.py
```

### Comparing `barbell2_xnat-0.1.0/PKG-INFO` & `barbell2_xnat-0.2.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.2
 Name: barbell2_xnat
-Version: 0.1.0
+Version: 0.2.0
 Summary: components for interacting with XNAT
 Home-page: https://github.com/rbrecheisen/barbell2_xnat
 Author: Ralph Brecheisen
 Author-email: r.brecheisen@maastrichtuniversity.nl
 License: MIT license
 Description: UNKNOWN
 Keywords: barbell2_xnat
```

### Comparing `barbell2_xnat-0.1.0/barbell2_xnat.egg-info/PKG-INFO` & `barbell2_xnat-0.2.0/barbell2_xnat.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.2
 Name: barbell2-xnat
-Version: 0.1.0
+Version: 0.2.0
 Summary: components for interacting with XNAT
 Home-page: https://github.com/rbrecheisen/barbell2_xnat
 Author: Ralph Brecheisen
 Author-email: r.brecheisen@maastrichtuniversity.nl
 License: MIT license
 Description: UNKNOWN
 Keywords: barbell2_xnat
```

### Comparing `barbell2_xnat-0.1.0/setup.py` & `barbell2_xnat-0.2.0/setup.py`

 * *Files identical despite different names*

