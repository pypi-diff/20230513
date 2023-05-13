# Comparing `tmp/faster_whisper_cli-1.0.0.tar.gz` & `tmp/faster_whisper_cli-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "faster_whisper_cli-1.0.0.tar", max compression
+gzip compressed data, was "faster_whisper_cli-1.0.1.tar", max compression
```

## Comparing `faster_whisper_cli-1.0.0.tar` & `faster_whisper_cli-1.0.1.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0        0 2023-05-13 05:37:21.049722 faster_whisper_cli-1.0.0/faster_whisper_cli/__init__.py
--rw-r--r--   0        0        0     8774 2023-05-13 09:16:33.081448 faster_whisper_cli-1.0.0/faster_whisper_cli/cli.py
--rw-r--r--   0        0        0      456 2023-05-13 09:18:15.263791 faster_whisper_cli-1.0.0/pyproject.toml
--rw-r--r--   0        0        0     2318 2023-05-13 09:03:58.379166 faster_whisper_cli-1.0.0/README.md
--rw-r--r--   0        0        0     2719 1970-01-01 00:00:00.000000 faster_whisper_cli-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-05-13 05:37:21.049722 faster_whisper_cli-1.0.1/faster_whisper_cli/__init__.py
+-rw-r--r--   0        0        0     8774 2023-05-13 09:16:33.081448 faster_whisper_cli-1.0.1/faster_whisper_cli/cli.py
+-rw-r--r--   0        0        0      456 2023-05-13 10:19:04.984995 faster_whisper_cli-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0     2318 2023-05-13 09:03:58.379166 faster_whisper_cli-1.0.1/README.md
+-rw-r--r--   0        0        0     2869 1970-01-01 00:00:00.000000 faster_whisper_cli-1.0.1/PKG-INFO
```

### Comparing `faster_whisper_cli-1.0.0/faster_whisper_cli/cli.py` & `faster_whisper_cli-1.0.1/faster_whisper_cli/cli.py`

 * *Files identical despite different names*

### Comparing `faster_whisper_cli-1.0.0/README.md` & `faster_whisper_cli-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `faster_whisper_cli-1.0.0/PKG-INFO` & `faster_whisper_cli-1.0.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,18 @@
 Metadata-Version: 2.1
 Name: faster-whisper-cli
-Version: 1.0.0
+Version: 1.0.1
 Summary: 
 Author: paddy41601
 Author-email: 49016918+paddy41601@users.noreply.github.com
-Requires-Python: >=3.9,<4.0
+Requires-Python: >=3.6,<4.0
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.6
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: faster-whisper
 Description-Content-Type: text/markdown
 
 # Faster Whisper CLI
```

