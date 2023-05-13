# Comparing `tmp/callableabc-1.1.0.tar.gz` & `tmp/callableabc-2.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "callableabc-1.1.0.tar", last modified: Mon Dec 12 19:01:03 2022, max compression
+gzip compressed data, was "callableabc-2.0.0.tar", last modified: Sat May 13 13:20:59 2023, max compression
```

## Comparing `callableabc-1.1.0.tar` & `callableabc-2.0.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0       14 2022-12-10 23:14:39.255406 callableabc-1.1.0/.envrc
--rw-r--r--   0        0        0       53 2022-12-10 23:18:08.132507 callableabc-1.1.0/.gitignore
--rw-r--r--   0        0        0      136 2022-12-11 21:34:38.381010 callableabc-1.1.0/.vscode/settings.json
--rw-r--r--   0        0        0      147 2022-12-12 15:56:16.574765 callableabc-1.1.0/CHANGELOG.md
--rw-r--r--   0        0        0     9161 2022-12-10 05:49:10.633279 callableabc-1.1.0/LICENSE
--rw-r--r--   0        0        0      463 2022-12-11 11:43:17.759576 callableabc-1.1.0/README.md
--rw-r--r--   0        0        0      262 2022-12-12 16:01:12.934024 callableabc-1.1.0/callableabc/__init__.py
--rw-r--r--   0        0        0     2294 2022-12-12 18:34:56.539034 callableabc-1.1.0/callableabc/callableabc.py
--rw-r--r--   0        0        0        0 2022-12-11 17:13:05.940043 callableabc-1.1.0/callableabc/py.typed
--rw-r--r--   0        0        0      472 2022-12-10 22:09:32.750164 callableabc-1.1.0/pyproject.toml
--rw-r--r--   0        0        0      852 1970-01-01 00:00:00.000000 callableabc-1.1.0/PKG-INFO
+-rw-r--r--   0        0        0       14 2023-05-04 20:43:10.969014 callableabc-2.0.0/.envrc
+-rw-r--r--   0        0        0       53 2023-05-04 20:43:10.969014 callableabc-2.0.0/.gitignore
+-rw-r--r--   0        0        0       91 2023-05-13 13:04:31.878747 callableabc-2.0.0/.vscode/settings.json
+-rw-r--r--   0        0        0      147 2023-05-04 20:43:10.969014 callableabc-2.0.0/CHANGELOG.md
+-rw-r--r--   0        0        0     9161 2023-05-04 20:43:10.969014 callableabc-2.0.0/LICENSE
+-rw-r--r--   0        0        0      463 2023-05-04 20:43:10.969014 callableabc-2.0.0/README.md
+-rw-r--r--   0        0        0      183 2023-05-13 13:04:31.878747 callableabc-2.0.0/callableabc/__init__.py
+-rw-r--r--   0        0        0     1187 2023-05-13 13:12:45.703012 callableabc-2.0.0/callableabc/callableabc.py
+-rw-r--r--   0        0        0        0 2023-05-04 20:43:10.969014 callableabc-2.0.0/callableabc/py.typed
+-rw-r--r--   0        0        0      472 2023-05-04 20:43:10.969014 callableabc-2.0.0/pyproject.toml
+-rw-r--r--   0        0        0      852 1970-01-01 00:00:00.000000 callableabc-2.0.0/PKG-INFO
```

### Comparing `callableabc-1.1.0/LICENSE` & `callableabc-2.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `callableabc-1.1.0/PKG-INFO` & `callableabc-2.0.0/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: callableabc
-Version: 1.1.0
+Version: 2.0.0
 Summary: A variant of ABC that allows customizing the call behavior via _class_call()
 Author-email: Anselm Schüler <mail@anselmschueler.com>
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 Classifier: License :: OSI Approved :: Apache Software License
 Project-URL: Home, https://github.com/schuelermine/callableabc
```

