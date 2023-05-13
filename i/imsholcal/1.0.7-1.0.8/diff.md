# Comparing `tmp/imsholcal-1.0.7.tar.gz` & `tmp/imsholcal-1.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "imsholcal-1.0.7.tar", last modified: Sat May 13 11:14:06 2023, max compression
+gzip compressed data, was "imsholcal-1.0.8.tar", last modified: Sat May 13 11:19:53 2023, max compression
```

## Comparing `imsholcal-1.0.7.tar` & `imsholcal-1.0.8.tar`

### file list

```diff
@@ -1,18 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:14:06.984067 imsholcal-1.0.7/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:14:06.980067 imsholcal-1.0.7/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:14:06.984067 imsholcal-1.0.7/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-05-13 11:13:52.000000 imsholcal-1.0.7/.github/workflows/python-publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 11:13:52.000000 imsholcal-1.0.7/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-05-13 11:14:06.984067 imsholcal-1.0.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      474 2023-05-13 11:13:52.000000 imsholcal-1.0.7/README.md
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 11:13:52.000000 imsholcal-1.0.7/README.rst
--rw-r--r--   0 runner    (1001) docker     (123)      994 2023-05-13 11:13:52.000000 imsholcal-1.0.7/business_day.py
--rw-r--r--   0 runner    (1001) docker     (123)      252 2023-05-13 11:13:52.000000 imsholcal-1.0.7/exchange_holidays.csv
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:14:06.984067 imsholcal-1.0.7/imsholcal.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-05-13 11:14:06.000000 imsholcal-1.0.7/imsholcal.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      280 2023-05-13 11:14:06.000000 imsholcal-1.0.7/imsholcal.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:14:06.000000 imsholcal-1.0.7/imsholcal.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 11:14:06.000000 imsholcal-1.0.7/imsholcal.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:14:06.000000 imsholcal-1.0.7/imsholcal.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 11:14:06.984067 imsholcal-1.0.7/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      649 2023-05-13 11:13:52.000000 imsholcal-1.0.7/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:19:53.674363 imsholcal-1.0.8/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:19:53.670364 imsholcal-1.0.8/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:19:53.670364 imsholcal-1.0.8/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-05-13 11:19:40.000000 imsholcal-1.0.8/.github/workflows/python-publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 11:19:40.000000 imsholcal-1.0.8/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)      298 2023-05-13 11:19:53.674363 imsholcal-1.0.8/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      474 2023-05-13 11:19:40.000000 imsholcal-1.0.8/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 11:19:40.000000 imsholcal-1.0.8/README.rst
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:19:40.000000 imsholcal-1.0.8/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      994 2023-05-13 11:19:40.000000 imsholcal-1.0.8/business_day.py
+-rw-r--r--   0 runner    (1001) docker     (123)      252 2023-05-13 11:19:40.000000 imsholcal-1.0.8/exchange_holidays.csv
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:19:53.674363 imsholcal-1.0.8/imsholcal.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      298 2023-05-13 11:19:53.000000 imsholcal-1.0.8/imsholcal.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      292 2023-05-13 11:19:53.000000 imsholcal-1.0.8/imsholcal.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:19:53.000000 imsholcal-1.0.8/imsholcal.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 11:19:53.000000 imsholcal-1.0.8/imsholcal.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:19:53.000000 imsholcal-1.0.8/imsholcal.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 11:19:53.674363 imsholcal-1.0.8/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      649 2023-05-13 11:19:40.000000 imsholcal-1.0.8/setup.py
```

### Comparing `imsholcal-1.0.7/.github/workflows/python-publish.yml` & `imsholcal-1.0.8/.github/workflows/python-publish.yml`

 * *Files identical despite different names*

### Comparing `imsholcal-1.0.7/business_day.py` & `imsholcal-1.0.8/business_day.py`

 * *Files identical despite different names*

### Comparing `imsholcal-1.0.7/setup.py` & `imsholcal-1.0.8/setup.py`

 * *Files identical despite different names*

