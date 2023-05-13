# Comparing `tmp/internetarchivesync-1.0.0.tar.gz` & `tmp/internetarchivesync-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "internetarchivesync-1.0.0.tar", max compression
+gzip compressed data, was "internetarchivesync-1.0.1.tar", max compression
```

## Comparing `internetarchivesync-1.0.0.tar` & `internetarchivesync-1.0.1.tar`

### file list

```diff
@@ -1,9 +1,10 @@
--rw-r--r--   0        0        0       22 2023-05-13 14:49:48.824474 internetarchivesync-1.0.0/internetarchivesync/__init__.py
--rw-r--r--   0        0        0     3395 2023-05-13 14:49:48.824474 internetarchivesync-1.0.0/internetarchivesync/archive_download.py
--rw-r--r--   0        0        0     8127 2023-05-13 14:49:48.824474 internetarchivesync-1.0.0/internetarchivesync/archive_sync.py
--rw-r--r--   0        0        0     4097 2023-05-13 14:49:48.824474 internetarchivesync-1.0.0/internetarchivesync/download.py
--rw-r--r--   0        0        0     1665 2023-05-13 14:49:48.824474 internetarchivesync-1.0.0/internetarchivesync/io.py
--rw-r--r--   0        0        0     6943 2023-05-13 14:49:48.824474 internetarchivesync-1.0.0/internetarchivesync/observer.py
--rw-r--r--   0        0        0     3910 2023-05-13 14:49:48.824474 internetarchivesync-1.0.0/internetarchivesync/sync.py
--rw-r--r--   0        0        0      847 2023-05-13 14:53:35.942144 internetarchivesync-1.0.0/pyproject.toml
--rw-r--r--   0        0        0      558 1970-01-01 00:00:00.000000 internetarchivesync-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0       22 2023-05-13 14:49:48.824474 internetarchivesync-1.0.1/internetarchivesync/__init__.py
+-rw-r--r--   0        0        0     3395 2023-05-13 14:49:48.824474 internetarchivesync-1.0.1/internetarchivesync/archive_download.py
+-rw-r--r--   0        0        0     8127 2023-05-13 14:49:48.824474 internetarchivesync-1.0.1/internetarchivesync/archive_sync.py
+-rw-r--r--   0        0        0     4097 2023-05-13 14:49:48.824474 internetarchivesync-1.0.1/internetarchivesync/download.py
+-rw-r--r--   0        0        0     1665 2023-05-13 14:49:48.824474 internetarchivesync-1.0.1/internetarchivesync/io.py
+-rw-r--r--   0        0        0     6943 2023-05-13 14:49:48.824474 internetarchivesync-1.0.1/internetarchivesync/observer.py
+-rw-r--r--   0        0        0     3910 2023-05-13 14:49:48.824474 internetarchivesync-1.0.1/internetarchivesync/sync.py
+-rw-r--r--   0        0        0      664 2023-05-13 14:49:48.824474 internetarchivesync-1.0.1/logging_config.ini
+-rw-r--r--   0        0        0      879 2023-05-13 15:14:16.456885 internetarchivesync-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0      558 1970-01-01 00:00:00.000000 internetarchivesync-1.0.1/PKG-INFO
```

### Comparing `internetarchivesync-1.0.0/internetarchivesync/archive_download.py` & `internetarchivesync-1.0.1/internetarchivesync/archive_download.py`

 * *Files identical despite different names*

### Comparing `internetarchivesync-1.0.0/internetarchivesync/archive_sync.py` & `internetarchivesync-1.0.1/internetarchivesync/archive_sync.py`

 * *Files identical despite different names*

### Comparing `internetarchivesync-1.0.0/internetarchivesync/download.py` & `internetarchivesync-1.0.1/internetarchivesync/download.py`

 * *Files identical despite different names*

### Comparing `internetarchivesync-1.0.0/internetarchivesync/io.py` & `internetarchivesync-1.0.1/internetarchivesync/io.py`

 * *Files identical despite different names*

### Comparing `internetarchivesync-1.0.0/internetarchivesync/observer.py` & `internetarchivesync-1.0.1/internetarchivesync/observer.py`

 * *Files identical despite different names*

### Comparing `internetarchivesync-1.0.0/internetarchivesync/sync.py` & `internetarchivesync-1.0.1/internetarchivesync/sync.py`

 * *Files identical despite different names*

### Comparing `internetarchivesync-1.0.0/pyproject.toml` & `internetarchivesync-1.0.1/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 [tool.poetry]
 name = "InternetArchiveSync"
-version = "1.0.0"
+version = "1.0.1"
 description = "A python tool to donwload an internet archive."
 authors = ["Mathieu <git@bigbisous.org>"]
+include = ["logging_config.ini"]
 
 [tool.poetry.dependencies]
 python = "^3.9"
 requests = "^2.26.0"
 defusedxml = "^0.7.1"
 rich = "^13.3.5"
 pytest = "^7.3.1"
@@ -34,8 +35,8 @@
 [tool.pylint.format]
 max-line-length = "88"
 
 [tool.pylint.'MESSAGES CONTROL']
 disable =  ["logging-fstring-interpolation"]
 
 [tool.isort]
-profile = "black"
+profile = "black"
```

### Comparing `internetarchivesync-1.0.0/PKG-INFO` & `internetarchivesync-1.0.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: internetarchivesync
-Version: 1.0.0
+Version: 1.0.1
 Summary: A python tool to donwload an internet archive.
 Author: Mathieu
 Author-email: git@bigbisous.org
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

