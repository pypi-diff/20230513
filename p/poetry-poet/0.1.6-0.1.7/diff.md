# Comparing `tmp/poetry_poet-0.1.6.tar.gz` & `tmp/poetry_poet-0.1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "poetry_poet-0.1.6.tar", max compression
+gzip compressed data, was "poetry_poet-0.1.7.tar", max compression
```

## Comparing `poetry_poet-0.1.6.tar` & `poetry_poet-0.1.7.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0        0 2023-05-13 06:41:55.080123 poetry_poet-0.1.6/README.md
--rw-r--r--   0        0        0      284 2023-05-13 06:47:32.868465 poetry_poet-0.1.6/poet/plug/plug.py
--rw-r--r--   0        0        0      445 2023-05-13 06:49:38.658080 poetry_poet-0.1.6/poet/plug/poet.py
--rw-r--r--   0        0        0      579 2023-05-13 07:11:52.759395 poetry_poet-0.1.6/pyproject.toml
--rw-r--r--   0        0        0      536 1970-01-01 00:00:00.000000 poetry_poet-0.1.6/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-05-13 06:41:55.080123 poetry_poet-0.1.7/README.md
+-rw-r--r--   0        0        0      284 2023-05-13 06:47:32.868465 poetry_poet-0.1.7/poet/plug/plug.py
+-rw-r--r--   0        0        0      445 2023-05-13 06:49:38.658080 poetry_poet-0.1.7/poet/plug/poet.py
+-rw-r--r--   0        0        0      577 2023-05-13 07:13:47.584889 poetry_poet-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      536 1970-01-01 00:00:00.000000 poetry_poet-0.1.7/PKG-INFO
```

### Comparing `poetry_poet-0.1.6/pyproject.toml` & `poetry_poet-0.1.7/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -1,26 +1,26 @@
 [tool.poetry]
 name = "poetry-poet"
-version = "0.1.6"
+version = "0.1.7"
 description = ""
 authors = ["Phillip Sitbon <phillip.sitbon@gmail.com>"]
 readme = "README.md"
 
 packages = [
     { include = "poet" }
 ]
 
 [tool.poetry.plugins."poetry.plugin"]
 demo = "poet.plug.plug:PoetPlugin"
 
 [tool.poetry.plugins."poetry.application.plugin"]
 foo-command = "poet.plug.poet:PoetApplicationPlugin"
 
-#[tool.poetry.scripts]
-#poet = "poetry.console.application:main"
+[tool.poetry.scripts]
+poet = "poetry.console.application:main"
 
 [tool.poetry.dependencies]
 python = "^3.7"
 poetry = "^1.4.0"
 
 [build-system]
 requires = ["poetry-core"]
```

### Comparing `poetry_poet-0.1.6/PKG-INFO` & `poetry_poet-0.1.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: poetry-poet
-Version: 0.1.6
+Version: 0.1.7
 Summary: 
 Author: Phillip Sitbon
 Author-email: phillip.sitbon@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

