# Comparing `tmp/aws-ket-0.1.5.tar.gz` & `tmp/aws-ket-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aws-ket-0.1.5.tar", last modified: Fri May  5 04:15:27 2023, max compression
+gzip compressed data, was "aws-ket-0.1.6.tar", last modified: Sat May 13 03:25:31 2023, max compression
```

## Comparing `aws-ket-0.1.5.tar` & `aws-ket-0.1.6.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 sayefiqbal   (502) staff       (20)        0 2023-05-05 04:15:27.248945 aws-ket-0.1.5/
--rw-r--r--   0 sayefiqbal   (502) staff       (20)     1452 2023-03-18 01:01:48.000000 aws-ket-0.1.5/CONTRIBUTING.md
--rw-r--r--   0 sayefiqbal   (502) staff       (20)    11357 2023-02-09 13:04:42.000000 aws-ket-0.1.5/LICENSE
--rw-r--r--   0 sayefiqbal   (502) staff       (20)      396 2023-03-24 00:07:58.000000 aws-ket-0.1.5/MANIFEST.in
--rw-r--r--   0 sayefiqbal   (502) staff       (20)     2150 2023-04-14 14:05:00.000000 aws-ket-0.1.5/Makefile
--rw-r--r--   0 sayefiqbal   (502) staff       (20)     4318 2023-05-05 04:15:27.248542 aws-ket-0.1.5/PKG-INFO
--rw-r--r--   0 sayefiqbal   (502) staff       (20)     3956 2023-05-05 03:04:42.000000 aws-ket-0.1.5/README.md
-drwxr-xr-x   0 sayefiqbal   (502) staff       (20)        0 2023-05-05 04:15:27.246582 aws-ket-0.1.5/aws_ket.egg-info/
--rw-r--r--   0 sayefiqbal   (502) staff       (20)     4318 2023-05-05 04:15:27.000000 aws-ket-0.1.5/aws_ket.egg-info/PKG-INFO
--rw-r--r--   0 sayefiqbal   (502) staff       (20)      230 2023-05-05 04:15:27.000000 aws-ket-0.1.5/aws_ket.egg-info/SOURCES.txt
--rw-r--r--   0 sayefiqbal   (502) staff       (20)        1 2023-05-05 04:15:27.000000 aws-ket-0.1.5/aws_ket.egg-info/dependency_links.txt
--rw-r--r--   0 sayefiqbal   (502) staff       (20)        1 2023-05-05 04:15:27.000000 aws-ket-0.1.5/aws_ket.egg-info/top_level.txt
-drwxr-xr-x   0 sayefiqbal   (502) staff       (20)        0 2023-05-05 04:15:27.247627 aws-ket-0.1.5/awsket/
--rwxr-xr-x   0 sayefiqbal   (502) staff       (20)     2882 2023-05-04 02:24:22.000000 aws-ket-0.1.5/awsket/app.py
--rw-r--r--   0 sayefiqbal   (502) staff       (20)    15104 2023-04-14 14:05:00.000000 aws-ket-0.1.5/awsket/ket.py
--rw-r--r--   0 sayefiqbal   (502) staff       (20)     2253 2023-05-05 04:12:35.000000 aws-ket-0.1.5/pyproject.toml
--rw-r--r--   0 sayefiqbal   (502) staff       (20)       38 2023-05-05 04:15:27.249072 aws-ket-0.1.5/setup.cfg
--rw-r--r--   0 sayefiqbal   (502) staff       (20)      772 2023-05-05 04:12:35.000000 aws-ket-0.1.5/setup.py
+drwxr-xr-x   0 sayefiqbal   (502) staff       (20)        0 2023-05-13 03:25:31.084755 aws-ket-0.1.6/
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)     1452 2023-03-18 01:01:48.000000 aws-ket-0.1.6/CONTRIBUTING.md
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)    11357 2023-02-09 13:04:42.000000 aws-ket-0.1.6/LICENSE
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)      396 2023-03-24 00:07:58.000000 aws-ket-0.1.6/MANIFEST.in
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)     2150 2023-04-14 14:05:00.000000 aws-ket-0.1.6/Makefile
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)     4318 2023-05-13 03:25:31.084462 aws-ket-0.1.6/PKG-INFO
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)     3956 2023-05-05 03:04:42.000000 aws-ket-0.1.6/README.md
+drwxr-xr-x   0 sayefiqbal   (502) staff       (20)        0 2023-05-13 03:25:31.082974 aws-ket-0.1.6/aws_ket.egg-info/
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)     4318 2023-05-13 03:25:30.000000 aws-ket-0.1.6/aws_ket.egg-info/PKG-INFO
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)      230 2023-05-13 03:25:31.000000 aws-ket-0.1.6/aws_ket.egg-info/SOURCES.txt
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)        1 2023-05-13 03:25:30.000000 aws-ket-0.1.6/aws_ket.egg-info/dependency_links.txt
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)        1 2023-05-13 03:25:31.000000 aws-ket-0.1.6/aws_ket.egg-info/top_level.txt
+drwxr-xr-x   0 sayefiqbal   (502) staff       (20)        0 2023-05-13 03:25:31.083828 aws-ket-0.1.6/awsket/
+-rwxr-xr-x   0 sayefiqbal   (502) staff       (20)     2882 2023-05-04 02:24:22.000000 aws-ket-0.1.6/awsket/app.py
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)    15104 2023-04-14 14:05:00.000000 aws-ket-0.1.6/awsket/ket.py
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)     2253 2023-05-13 03:18:56.000000 aws-ket-0.1.6/pyproject.toml
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)       38 2023-05-13 03:25:31.084857 aws-ket-0.1.6/setup.cfg
+-rw-r--r--   0 sayefiqbal   (502) staff       (20)      772 2023-05-13 03:18:56.000000 aws-ket-0.1.6/setup.py
```

### Comparing `aws-ket-0.1.5/CONTRIBUTING.md` & `aws-ket-0.1.6/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `aws-ket-0.1.5/LICENSE` & `aws-ket-0.1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `aws-ket-0.1.5/Makefile` & `aws-ket-0.1.6/Makefile`

 * *Files identical despite different names*

### Comparing `aws-ket-0.1.5/PKG-INFO` & `aws-ket-0.1.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aws-ket
-Version: 0.1.5
+Version: 0.1.6
 Summary: Utility tool to encrypt data using AWS KMS and store it in preferred backend.
 Home-page: https://github.com/sayefiqb/aws-ket
 Author: Sayef Iqbal
 Author-email: s2400@columbia.edu
 Maintainer: Sayef Iqbal
 License: UNKNOWN
 Platform: UNKNOWN
```

### Comparing `aws-ket-0.1.5/README.md` & `aws-ket-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `aws-ket-0.1.5/aws_ket.egg-info/PKG-INFO` & `aws-ket-0.1.6/aws_ket.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aws-ket
-Version: 0.1.5
+Version: 0.1.6
 Summary: Utility tool to encrypt data using AWS KMS and store it in preferred backend.
 Home-page: https://github.com/sayefiqb/aws-ket
 Author: Sayef Iqbal
 Author-email: s2400@columbia.edu
 Maintainer: Sayef Iqbal
 License: UNKNOWN
 Platform: UNKNOWN
```

### Comparing `aws-ket-0.1.5/awsket/app.py` & `aws-ket-0.1.6/awsket/app.py`

 * *Files identical despite different names*

### Comparing `aws-ket-0.1.5/awsket/ket.py` & `aws-ket-0.1.6/awsket/ket.py`

 * *Files identical despite different names*

### Comparing `aws-ket-0.1.5/pyproject.toml` & `aws-ket-0.1.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 build-backend="setuptools.build_meta"
 
 [project]
 name = "aws-ket"
 authors = [{name = "Sayef Iqbal", email = "si2400@columbia.edu"}]
 description="Utility tool to encrypt data using AWS KMS and store it in preferred backend."
 readme = "README.md"
-version = "0.1.5"
+version = "0.1.6"
 requires-python = ">=3.9"
 
 dependencies = []
 
 classifiers = [
     "Development Status :: 2 - Pre-Alpha",
     "Programming Language :: Python :: Implementation :: CPython",
```

### Comparing `aws-ket-0.1.5/setup.py` & `aws-ket-0.1.6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from setuptools import setup
 
 from pathlib import Path
 this_directory = Path(__file__).parent
 long_description = (this_directory / "README.md").read_text()
 
-VERSION = "0.1.5"
+VERSION = "0.1.6"
 setup(
     name             = 'aws-ket',
     author           = 'Sayef Iqbal',
     author_email     = 's2400@columbia.edu',
     maintainer       = 'Sayef Iqbal',
     url              = 'https://github.com/sayefiqb/aws-ket',
     description      = 'Utility tool to encrypt data using AWS KMS and store it in preferred backend.',
```

