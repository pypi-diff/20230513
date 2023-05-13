# Comparing `tmp/cat_dog_lib-0.0.1.tar.gz` & `tmp/cat_dog_lib-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cat_dog_lib-0.0.1.tar", last modified: Sat May 13 13:56:47 2023, max compression
+gzip compressed data, was "cat_dog_lib-0.0.2.tar", last modified: Sat May 13 14:05:59 2023, max compression
```

## Comparing `cat_dog_lib-0.0.1.tar` & `cat_dog_lib-0.0.2.tar`

### file list

```diff
@@ -1,20 +1,24 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 13:56:47.045756 cat_dog_lib-0.0.1/
--rw-rw-rw-   0        0        0      474 2023-05-13 13:56:47.044754 cat_dog_lib-0.0.1/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 13:56:47.007759 cat_dog_lib-0.0.1/app/
-drwxrwxrwx   0        0        0        0 2023-05-13 13:56:47.014754 cat_dog_lib-0.0.1/app/cat_dog_lib/
--rw-rw-rw-   0        0        0       50 2023-05-13 13:36:40.000000 cat_dog_lib-0.0.1/app/cat_dog_lib/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 13:56:47.037772 cat_dog_lib-0.0.1/app/cat_dog_lib/src/
--rw-rw-rw-   0        0        0        0 2023-05-13 13:34:34.000000 cat_dog_lib-0.0.1/app/cat_dog_lib/src/__init__.py
--rw-rw-rw-   0        0        0      134 2023-05-13 13:34:15.000000 cat_dog_lib-0.0.1/app/cat_dog_lib/src/cat.py
--rw-rw-rw-   0        0        0      132 2023-05-13 13:34:05.000000 cat_dog_lib-0.0.1/app/cat_dog_lib/src/dog.py
-drwxrwxrwx   0        0        0        0 2023-05-13 13:56:47.041773 cat_dog_lib-0.0.1/app/cat_dog_lib/test/
--rw-rw-rw-   0        0        0        0 2023-05-13 13:34:41.000000 cat_dog_lib-0.0.1/app/cat_dog_lib/test/__init__.py
--rw-rw-rw-   0        0        0      230 2023-05-13 13:36:00.000000 cat_dog_lib-0.0.1/app/cat_dog_lib/test/test_dog.py
-drwxrwxrwx   0        0        0        0 2023-05-13 13:56:47.030770 cat_dog_lib-0.0.1/app/cat_dog_lib.egg-info/
--rw-rw-rw-   0        0        0      474 2023-05-13 13:56:46.000000 cat_dog_lib-0.0.1/app/cat_dog_lib.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      382 2023-05-13 13:56:46.000000 cat_dog_lib-0.0.1/app/cat_dog_lib.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 13:56:46.000000 cat_dog_lib-0.0.1/app/cat_dog_lib.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       32 2023-05-13 13:56:46.000000 cat_dog_lib-0.0.1/app/cat_dog_lib.egg-info/requires.txt
--rw-rw-rw-   0        0        0       12 2023-05-13 13:56:46.000000 cat_dog_lib-0.0.1/app/cat_dog_lib.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 13:56:47.046755 cat_dog_lib-0.0.1/setup.cfg
--rw-rw-rw-   0        0        0      771 2023-05-13 13:54:36.000000 cat_dog_lib-0.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:05:59.358703 cat_dog_lib-0.0.2/
+-rw-rw-rw-   0        0        0      474 2023-05-13 14:05:59.357709 cat_dog_lib-0.0.2/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 14:05:59.309991 cat_dog_lib-0.0.2/app/
+drwxrwxrwx   0        0        0        0 2023-05-13 14:05:59.318004 cat_dog_lib-0.0.2/app/cat_dog_lib/
+-rw-rw-rw-   0        0        0       50 2023-05-13 13:36:40.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:05:59.341708 cat_dog_lib-0.0.2/app/cat_dog_lib/src/
+-rw-rw-rw-   0        0        0        0 2023-05-13 13:34:34.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/src/__init__.py
+-rw-rw-rw-   0        0        0      134 2023-05-13 13:34:15.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/src/cat.py
+-rw-rw-rw-   0        0        0      132 2023-05-13 13:34:05.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/src/dog.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:05:59.348701 cat_dog_lib-0.0.2/app/cat_dog_lib/src/laboratory/
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:04:12.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/src/laboratory/__init__.py
+-rw-rw-rw-   0        0        0      335 2023-05-13 14:02:19.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/src/laboratory/doctor.py
+-rw-rw-rw-   0        0        0      192 2023-05-13 14:02:16.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/src/laboratory/machine.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:05:59.353712 cat_dog_lib-0.0.2/app/cat_dog_lib/test/
+-rw-rw-rw-   0        0        0        0 2023-05-13 13:34:41.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/test/__init__.py
+-rw-rw-rw-   0        0        0      230 2023-05-13 13:36:00.000000 cat_dog_lib-0.0.2/app/cat_dog_lib/test/test_dog.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:05:59.334708 cat_dog_lib-0.0.2/app/cat_dog_lib.egg-info/
+-rw-rw-rw-   0        0        0      474 2023-05-13 14:05:59.000000 cat_dog_lib-0.0.2/app/cat_dog_lib.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      508 2023-05-13 14:05:59.000000 cat_dog_lib-0.0.2/app/cat_dog_lib.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:05:59.000000 cat_dog_lib-0.0.2/app/cat_dog_lib.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       32 2023-05-13 14:05:59.000000 cat_dog_lib-0.0.2/app/cat_dog_lib.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2023-05-13 14:05:59.000000 cat_dog_lib-0.0.2/app/cat_dog_lib.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:05:59.358703 cat_dog_lib-0.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      771 2023-05-13 14:04:10.000000 cat_dog_lib-0.0.2/setup.py
```

### Comparing `cat_dog_lib-0.0.1/setup.py` & `cat_dog_lib-0.0.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from setuptools import find_packages, setup
 
 
 setup(
     name="cat_dog_lib",
-    version="0.0.1",
+    version="0.0.2",
     description="Mô tả ngắn",
     package_dir={"": "app"},
     packages=find_packages(where="app"),
     long_description='Mô tả dài',
     long_description_content_type="text/markdown",
     url="https://github.com/anthule123/first_package_An",
     author="anthule123",
```

