# Comparing `tmp/ipo_india-0.0.1.tar.gz` & `tmp/ipo_india-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ipo_india-0.0.1.tar", last modified: Sat May 13 12:08:04 2023, max compression
+gzip compressed data, was "ipo_india-0.0.2.tar", last modified: Sat May 13 13:57:43 2023, max compression
```

## Comparing `ipo_india-0.0.1.tar` & `ipo_india-0.0.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxr-x   0 quartic   (1000) quartic   (1000)        0 2023-05-13 12:08:04.552652 ipo_india-0.0.1/
--rw-rw-r--   0 quartic   (1000) quartic   (1000)      265 2023-05-13 12:08:04.552652 ipo_india-0.0.1/PKG-INFO
-drwxrwxr-x   0 quartic   (1000) quartic   (1000)        0 2023-05-13 12:08:04.552652 ipo_india-0.0.1/ipo_india/
--rw-rw-r--   0 quartic   (1000) quartic   (1000)       89 2023-05-13 11:41:36.000000 ipo_india-0.0.1/ipo_india/__init__.py
--rw-rw-r--   0 quartic   (1000) quartic   (1000)     2337 2023-05-13 11:33:48.000000 ipo_india-0.0.1/ipo_india/ipo.py
--rw-rw-r--   0 quartic   (1000) quartic   (1000)     5603 2023-05-13 11:33:48.000000 ipo_india-0.0.1/ipo_india/ipo_scraper.py
--rw-rw-r--   0 quartic   (1000) quartic   (1000)     1099 2023-05-13 11:52:42.000000 ipo_india-0.0.1/ipo_india/main.py
-drwxrwxr-x   0 quartic   (1000) quartic   (1000)        0 2023-05-13 12:08:04.552652 ipo_india-0.0.1/ipo_india.egg-info/
--rw-rw-r--   0 quartic   (1000) quartic   (1000)      265 2023-05-13 12:08:04.000000 ipo_india-0.0.1/ipo_india.egg-info/PKG-INFO
--rw-rw-r--   0 quartic   (1000) quartic   (1000)      254 2023-05-13 12:08:04.000000 ipo_india-0.0.1/ipo_india.egg-info/SOURCES.txt
--rw-rw-r--   0 quartic   (1000) quartic   (1000)        1 2023-05-13 12:08:04.000000 ipo_india-0.0.1/ipo_india.egg-info/dependency_links.txt
--rw-rw-r--   0 quartic   (1000) quartic   (1000)       95 2023-05-13 12:08:04.000000 ipo_india-0.0.1/ipo_india.egg-info/requires.txt
--rw-rw-r--   0 quartic   (1000) quartic   (1000)       10 2023-05-13 12:08:04.000000 ipo_india-0.0.1/ipo_india.egg-info/top_level.txt
--rw-rw-r--   0 quartic   (1000) quartic   (1000)       38 2023-05-13 12:08:04.552652 ipo_india-0.0.1/setup.cfg
--rw-rw-r--   0 quartic   (1000) quartic   (1000)      512 2023-05-13 12:08:03.000000 ipo_india-0.0.1/setup.py
+drwxrwxr-x   0 quartic   (1000) quartic   (1000)        0 2023-05-13 13:57:43.595608 ipo_india-0.0.2/
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)      265 2023-05-13 13:57:43.595608 ipo_india-0.0.2/PKG-INFO
+drwxrwxr-x   0 quartic   (1000) quartic   (1000)        0 2023-05-13 13:57:43.595608 ipo_india-0.0.2/ipo_india/
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)       89 2023-05-13 11:41:36.000000 ipo_india-0.0.2/ipo_india/__init__.py
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)     2337 2023-05-13 11:33:48.000000 ipo_india-0.0.2/ipo_india/ipo.py
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)     5603 2023-05-13 11:33:48.000000 ipo_india-0.0.2/ipo_india/ipo_scraper.py
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)      989 2023-05-13 13:55:54.000000 ipo_india-0.0.2/ipo_india/main.py
+drwxrwxr-x   0 quartic   (1000) quartic   (1000)        0 2023-05-13 13:57:43.595608 ipo_india-0.0.2/ipo_india.egg-info/
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)      265 2023-05-13 13:57:43.000000 ipo_india-0.0.2/ipo_india.egg-info/PKG-INFO
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)      254 2023-05-13 13:57:43.000000 ipo_india-0.0.2/ipo_india.egg-info/SOURCES.txt
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)        1 2023-05-13 13:57:43.000000 ipo_india-0.0.2/ipo_india.egg-info/dependency_links.txt
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)       95 2023-05-13 13:57:43.000000 ipo_india-0.0.2/ipo_india.egg-info/requires.txt
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)       10 2023-05-13 13:57:43.000000 ipo_india-0.0.2/ipo_india.egg-info/top_level.txt
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)       38 2023-05-13 13:57:43.595608 ipo_india-0.0.2/setup.cfg
+-rw-rw-r--   0 quartic   (1000) quartic   (1000)      512 2023-05-13 13:57:01.000000 ipo_india-0.0.2/setup.py
```

### Comparing `ipo_india-0.0.1/ipo_india/ipo.py` & `ipo_india-0.0.2/ipo_india/ipo.py`

 * *Files identical despite different names*

### Comparing `ipo_india-0.0.1/ipo_india/ipo_scraper.py` & `ipo_india-0.0.2/ipo_india/ipo_scraper.py`

 * *Files identical despite different names*

### Comparing `ipo_india-0.0.1/setup.py` & `ipo_india-0.0.2/setup.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from setuptools import setup, find_packages
-__version__ = '0.0.1'
+__version__ = '0.0.2'
 setup(
     name='ipo_india',
     version=__version__,
 
     url='https://github.com/MichaelKim0407/tutorial-pip-package',
     author='Aman Agarwal',
     author_email='aman.agarwal150@gmail.com',
```

