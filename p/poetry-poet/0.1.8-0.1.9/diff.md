# Comparing `tmp/poetry_poet-0.1.8.tar.gz` & `tmp/poetry_poet-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "poetry_poet-0.1.8.tar", max compression
+gzip compressed data, was "poetry_poet-0.1.9.tar", max compression
```

## Comparing `poetry_poet-0.1.8.tar` & `poetry_poet-0.1.9.tar`

### file list

```diff
@@ -1,8 +1,6 @@
--rw-r--r--   0        0        0        0 2023-05-13 06:41:55.080123 poetry_poet-0.1.8/README.md
--rw-r--r--   0        0        0        0 2023-05-13 07:25:07.101712 poetry_poet-0.1.8/poet/__init__.py
--rw-r--r--   0        0        0        0 2023-05-13 07:25:17.169842 poetry_poet-0.1.8/poet/plug/__init__.py
--rw-r--r--   0        0        0     1495 2023-05-13 07:24:17.577070 poetry_poet-0.1.8/poet/plug/__pycache__/poet.cpython-311.pyc
--rw-r--r--   0        0        0      284 2023-05-13 06:47:32.868465 poetry_poet-0.1.8/poet/plug/plug.py
--rw-r--r--   0        0        0      445 2023-05-13 06:49:38.658080 poetry_poet-0.1.8/poet/plug/poet.py
--rw-r--r--   0        0        0      577 2023-05-13 07:27:42.687728 poetry_poet-0.1.8/pyproject.toml
--rw-r--r--   0        0        0      536 1970-01-01 00:00:00.000000 poetry_poet-0.1.8/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-05-13 06:41:55.080123 poetry_poet-0.1.9/README.md
+-rw-r--r--   0        0        0     1495 2023-05-13 07:24:17.577070 poetry_poet-0.1.9/poet/plug/__pycache__/poet.cpython-311.pyc
+-rw-r--r--   0        0        0      284 2023-05-13 06:47:32.868465 poetry_poet-0.1.9/poet/plug/plug.py
+-rw-r--r--   0        0        0      445 2023-05-13 06:49:38.658080 poetry_poet-0.1.9/poet/plug/poet.py
+-rw-r--r--   0        0        0      570 2023-05-13 07:49:42.517206 poetry_poet-0.1.9/pyproject.toml
+-rw-r--r--   0        0        0      536 1970-01-01 00:00:00.000000 poetry_poet-0.1.9/PKG-INFO
```

### Comparing `poetry_poet-0.1.8/poet/plug/__pycache__/poet.cpython-311.pyc` & `poetry_poet-0.1.9/poet/plug/__pycache__/poet.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `poetry_poet-0.1.8/pyproject.toml` & `poetry_poet-0.1.9/pyproject.toml`

 * *Files 15% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 [tool.poetry]
 name = "poetry-poet"
-version = "0.1.8"
+version = "0.1.9"
 description = ""
 authors = ["Phillip Sitbon <phillip.sitbon@gmail.com>"]
 readme = "README.md"
 
 packages = [
     { include = "poet" }
 ]
 
 [tool.poetry.plugins."poetry.plugin"]
-demo = "poet.plug.plug:PoetPlugin"
+poet = "poet.plug.plug:PoetPlugin"
 
 [tool.poetry.plugins."poetry.application.plugin"]
-foo-command = "poet.plug.poet:PoetApplicationPlugin"
+poet = "poet.plug.poet:PoetApplicationPlugin"
 
 [tool.poetry.scripts]
 poet = "poetry.console.application:main"
 
 [tool.poetry.dependencies]
 python = "^3.7"
 poetry = "^1.4.0"
```

### Comparing `poetry_poet-0.1.8/PKG-INFO` & `poetry_poet-0.1.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: poetry-poet
-Version: 0.1.8
+Version: 0.1.9
 Summary: 
 Author: Phillip Sitbon
 Author-email: phillip.sitbon@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

