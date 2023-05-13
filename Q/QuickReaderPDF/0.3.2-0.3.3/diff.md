# Comparing `tmp/QuickReaderPDF-0.3.2.tar.gz` & `tmp/QuickReaderPDF-0.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "QuickReaderPDF-0.3.2.tar", last modified: Sat May 13 08:07:28 2023, max compression
+gzip compressed data, was "QuickReaderPDF-0.3.3.tar", last modified: Sat May 13 08:20:12 2023, max compression
```

## Comparing `QuickReaderPDF-0.3.2.tar` & `QuickReaderPDF-0.3.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxr-x   0 shreyas   (1000) shreyas   (1000)        0 2023-05-13 08:07:28.761858 QuickReaderPDF-0.3.2/
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     1069 2023-03-26 20:58:41.000000 QuickReaderPDF-0.3.2/LICENSE
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     6184 2023-05-13 08:07:28.761858 QuickReaderPDF-0.3.2/PKG-INFO
-drwxrwxr-x   0 shreyas   (1000) shreyas   (1000)        0 2023-05-13 08:07:28.761858 QuickReaderPDF-0.3.2/QuickReaderPDF/
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      160 2023-05-12 22:40:40.000000 QuickReaderPDF-0.3.2/QuickReaderPDF/__init__.py
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      228 2023-05-12 04:36:32.000000 QuickReaderPDF-0.3.2/QuickReaderPDF/__main__.py
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     7027 2023-05-12 04:36:32.000000 QuickReaderPDF-0.3.2/QuickReaderPDF/pdfeditor.py
-drwxrwxr-x   0 shreyas   (1000) shreyas   (1000)        0 2023-05-13 08:07:28.761858 QuickReaderPDF-0.3.2/QuickReaderPDF/tests/
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)        0 2023-04-14 06:09:42.000000 QuickReaderPDF-0.3.2/QuickReaderPDF/tests/__init__.py
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     3458 2023-05-12 04:04:49.000000 QuickReaderPDF-0.3.2/QuickReaderPDF/tests/test_all.py
-drwxrwxr-x   0 shreyas   (1000) shreyas   (1000)        0 2023-05-13 08:07:28.761858 QuickReaderPDF-0.3.2/QuickReaderPDF.egg-info/
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     6184 2023-05-13 08:07:28.000000 QuickReaderPDF-0.3.2/QuickReaderPDF.egg-info/PKG-INFO
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      378 2023-05-13 08:07:28.000000 QuickReaderPDF-0.3.2/QuickReaderPDF.egg-info/SOURCES.txt
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)        1 2023-05-13 08:07:28.000000 QuickReaderPDF-0.3.2/QuickReaderPDF.egg-info/dependency_links.txt
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      156 2023-05-13 08:07:28.000000 QuickReaderPDF-0.3.2/QuickReaderPDF.egg-info/requires.txt
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)       15 2023-05-13 08:07:28.000000 QuickReaderPDF-0.3.2/QuickReaderPDF.egg-info/top_level.txt
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     3908 2023-05-12 22:24:16.000000 QuickReaderPDF-0.3.2/README.md
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     2397 2023-05-13 08:05:22.000000 QuickReaderPDF-0.3.2/pyproject.toml
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)       38 2023-05-13 08:07:28.761858 QuickReaderPDF-0.3.2/setup.cfg
--rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      340 2023-05-13 08:05:22.000000 QuickReaderPDF-0.3.2/setup.py
+drwxrwxr-x   0 shreyas   (1000) shreyas   (1000)        0 2023-05-13 08:20:12.673834 QuickReaderPDF-0.3.3/
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     1069 2023-03-26 20:58:41.000000 QuickReaderPDF-0.3.3/LICENSE
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     6184 2023-05-13 08:20:12.673834 QuickReaderPDF-0.3.3/PKG-INFO
+drwxrwxr-x   0 shreyas   (1000) shreyas   (1000)        0 2023-05-13 08:20:12.673834 QuickReaderPDF-0.3.3/QuickReaderPDF/
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      160 2023-05-13 08:17:39.000000 QuickReaderPDF-0.3.3/QuickReaderPDF/__init__.py
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      228 2023-05-12 04:36:32.000000 QuickReaderPDF-0.3.3/QuickReaderPDF/__main__.py
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     7027 2023-05-12 04:36:32.000000 QuickReaderPDF-0.3.3/QuickReaderPDF/pdfeditor.py
+drwxrwxr-x   0 shreyas   (1000) shreyas   (1000)        0 2023-05-13 08:20:12.673834 QuickReaderPDF-0.3.3/QuickReaderPDF/tests/
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)        0 2023-04-14 06:09:42.000000 QuickReaderPDF-0.3.3/QuickReaderPDF/tests/__init__.py
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     3458 2023-05-12 04:04:49.000000 QuickReaderPDF-0.3.3/QuickReaderPDF/tests/test_all.py
+drwxrwxr-x   0 shreyas   (1000) shreyas   (1000)        0 2023-05-13 08:20:12.673834 QuickReaderPDF-0.3.3/QuickReaderPDF.egg-info/
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     6184 2023-05-13 08:20:12.000000 QuickReaderPDF-0.3.3/QuickReaderPDF.egg-info/PKG-INFO
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      378 2023-05-13 08:20:12.000000 QuickReaderPDF-0.3.3/QuickReaderPDF.egg-info/SOURCES.txt
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)        1 2023-05-13 08:20:12.000000 QuickReaderPDF-0.3.3/QuickReaderPDF.egg-info/dependency_links.txt
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      156 2023-05-13 08:20:12.000000 QuickReaderPDF-0.3.3/QuickReaderPDF.egg-info/requires.txt
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)       15 2023-05-13 08:20:12.000000 QuickReaderPDF-0.3.3/QuickReaderPDF.egg-info/top_level.txt
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     3908 2023-05-12 22:24:16.000000 QuickReaderPDF-0.3.3/README.md
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)     2397 2023-05-13 08:17:39.000000 QuickReaderPDF-0.3.3/pyproject.toml
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)       38 2023-05-13 08:20:12.673834 QuickReaderPDF-0.3.3/setup.cfg
+-rw-rw-r--   0 shreyas   (1000) shreyas   (1000)      340 2023-05-13 08:17:39.000000 QuickReaderPDF-0.3.3/setup.py
```

### Comparing `QuickReaderPDF-0.3.2/LICENSE` & `QuickReaderPDF-0.3.3/LICENSE`

 * *Files identical despite different names*

### Comparing `QuickReaderPDF-0.3.2/PKG-INFO` & `QuickReaderPDF-0.3.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: QuickReaderPDF
-Version: 0.3.2
+Version: 0.3.3
 Summary: This package converts a pdf or a html file that the user wants to read to an new pdf file, which can be read faster! The idea is bionic reading, where we bold the first three letters of every word. We hope you enjoy reading your files faster!
 Author-email: Shreyas Bhat <shreyasbhat92@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Shreyas Bhat
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `QuickReaderPDF-0.3.2/QuickReaderPDF/pdfeditor.py` & `QuickReaderPDF-0.3.3/QuickReaderPDF/pdfeditor.py`

 * *Files identical despite different names*

### Comparing `QuickReaderPDF-0.3.2/QuickReaderPDF/tests/test_all.py` & `QuickReaderPDF-0.3.3/QuickReaderPDF/tests/test_all.py`

 * *Files identical despite different names*

### Comparing `QuickReaderPDF-0.3.2/QuickReaderPDF.egg-info/PKG-INFO` & `QuickReaderPDF-0.3.3/QuickReaderPDF.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: QuickReaderPDF
-Version: 0.3.2
+Version: 0.3.3
 Summary: This package converts a pdf or a html file that the user wants to read to an new pdf file, which can be read faster! The idea is bionic reading, where we bold the first three letters of every word. We hope you enjoy reading your files faster!
 Author-email: Shreyas Bhat <shreyasbhat92@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Shreyas Bhat
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `QuickReaderPDF-0.3.2/README.md` & `QuickReaderPDF-0.3.3/README.md`

 * *Files identical despite different names*

### Comparing `QuickReaderPDF-0.3.2/pyproject.toml` & `QuickReaderPDF-0.3.3/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 build-backend="setuptools.build_meta"
 
 [project]
 name = "QuickReaderPDF"
 authors = [{name = "Shreyas Bhat", email = "shreyasbhat92@gmail.com"}]
 description="This package converts a pdf or a html file that the user wants to read to an new pdf file, which can be read faster! The idea is bionic reading, where we bold the first three letters of every word. We hope you enjoy reading your files faster!"
 readme = "README.md"
-version = "0.3.2"
+version = "0.3.3"
 requires-python = ">=3.7"
 
 dependencies = []
 
 classifiers = [
     "Development Status :: 2 - Pre-Alpha",
     "Programming Language :: Python :: Implementation :: CPython",
```

