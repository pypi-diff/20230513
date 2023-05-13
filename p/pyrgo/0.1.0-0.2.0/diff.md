# Comparing `tmp/pyrgo-0.1.0.tar.gz` & `tmp/pyrgo-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data
+gzip compressed data, last modified: Sun Feb  2 00:00:00 2020, max compression
```

## Comparing `pyrgo-0.1.0.tar` & `pyrgo-0.2.0.tar`

### file list

```diff
@@ -1,27 +1,41 @@
--rw-r--r--   0        0        0      283 1970-01-01 00:00:00.000000 pyrgo-0.1.0/Cargo.toml
--rw-r--r--   0     1001      123     2687 2023-05-11 22:39:11.000000 pyrgo-0.1.0/.github/workflows/release.yml
--rw-r--r--   0     1001      123      685 2023-05-11 22:39:11.000000 pyrgo-0.1.0/.gitignore
--rw-r--r--   0     1001      123       26 2023-05-11 22:39:11.000000 pyrgo-0.1.0/.tool-versions
--rw-r--r--   0     1001      123     1076 2023-05-11 22:39:11.000000 pyrgo-0.1.0/LICENSE
--rw-r--r--   0     1001      123     1497 2023-05-11 22:39:11.000000 pyrgo-0.1.0/Makefile
--rw-r--r--   0     1001      123        7 2023-05-11 22:39:11.000000 pyrgo-0.1.0/README.md
--rw-r--r--   0     1001      123     1909 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyproject.toml
--rw-r--r--   0     1001      123        0 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/__init__.py
--rw-r--r--   0     1001      123       73 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/__main__.py
--rw-r--r--   0     1001      123      137 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/_pyrgo.pyi
--rw-r--r--   0     1001      123      512 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/cli.py
--rw-r--r--   0     1001      123        0 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/command/__init__.py
--rw-r--r--   0     1001      123      137 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/command/check.py
--rw-r--r--   0     1001      123      159 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/command/clean.py
--rw-r--r--   0     1001      123      417 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/command/fmt.py
--rw-r--r--   0     1001      123      209 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/command/lock.py
--rw-r--r--   0     1001      123     1091 2023-05-11 22:39:11.000000 pyrgo-0.1.0/pyrgo/command/venv.py
--rw-r--r--   0     1001      123      375 2023-05-11 22:39:11.000000 pyrgo-0.1.0/requirements/core.lock
--rw-r--r--   0     1001      123     1196 2023-05-11 22:39:11.000000 pyrgo-0.1.0/requirements/dev.lock
--rw-r--r--   0     1001      123     1283 2023-05-11 22:39:11.000000 pyrgo-0.1.0/scripts/new_release.py
--rw-r--r--   0     1001      123      216 2023-05-11 22:39:11.000000 pyrgo-0.1.0/src/file_system.rs
--rw-r--r--   0     1001      123      247 2023-05-11 22:39:11.000000 pyrgo-0.1.0/src/lib.rs
--rw-r--r--   0     1001      123       15 2023-05-11 22:39:11.000000 pyrgo-0.1.0/src/utilities/mod.rs
--rw-r--r--   0     1001      123      284 2023-05-11 22:39:11.000000 pyrgo-0.1.0/src/utilities/pyproject.rs
--rw-r--r--   0     1001      123    17698 2023-05-11 22:39:11.000000 pyrgo-0.1.0/Cargo.lock
--rw-r--r--   0        0        0      712 1970-01-01 00:00:00.000000 pyrgo-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0       26 2020-02-02 00:00:00.000000 pyrgo-0.2.0/.tool-versions
+-rw-r--r--   0        0        0     1497 2020-02-02 00:00:00.000000 pyrgo-0.2.0/Makefile
+-rw-r--r--   0        0        0       19 2020-02-02 00:00:00.000000 pyrgo-0.2.0/mkdocs.yml
+-rw-r--r--   0        0        0      923 2020-02-02 00:00:00.000000 pyrgo-0.2.0/.github/workflows/release.yml
+-rw-r--r--   0        0        0     1040 2020-02-02 00:00:00.000000 pyrgo-0.2.0/.github/workflows/test.yml
+-rw-r--r--   0        0        0      491 2020-02-02 00:00:00.000000 pyrgo-0.2.0/docs/index.md
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/__init__.py
+-rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/__main__.py
+-rw-r--r--   0        0        0      828 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/cli.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/py.typed
+-rw-r--r--   0        0        0      251 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/utils.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/__init__.py
+-rw-r--r--   0        0        0      131 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/add.py
+-rw-r--r--   0        0        0      342 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/build.py
+-rw-r--r--   0        0        0      595 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/check.py
+-rw-r--r--   0        0        0      140 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/clean.py
+-rw-r--r--   0        0        0      636 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/fmt.py
+-rw-r--r--   0        0        0      137 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/init.py
+-rw-r--r--   0        0        0      101 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/lock.py
+-rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/new.py
+-rw-r--r--   0        0        0      130 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/remove.py
+-rw-r--r--   0        0        0     1099 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/test.py
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/venv.py
+-rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/__init__.py
+-rw-r--r--   0        0        0     1171 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/build.py
+-rw-r--r--   0        0        0      727 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/new.py
+-rw-r--r--   0        0        0      363 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/root.py
+-rw-r--r--   0        0        0     1468 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/serve.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/utilities/__init__.py
+-rw-r--r--   0        0        0     1177 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/utilities/command.py
+-rw-r--r--   0        0        0      901 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/utilities/project.py
+-rw-r--r--   0        0        0     3642 2020-02-02 00:00:00.000000 pyrgo-0.2.0/requirements/core.lock
+-rw-r--r--   0        0        0     3653 2020-02-02 00:00:00.000000 pyrgo-0.2.0/requirements/dev.lock
+-rw-r--r--   0        0        0      928 2020-02-02 00:00:00.000000 pyrgo-0.2.0/scripts/new_release.py
+-rw-r--r--   0        0        0      155 2020-02-02 00:00:00.000000 pyrgo-0.2.0/tests/integration/resources/pyproject.toml
+-rw-r--r--   0        0        0      731 2020-02-02 00:00:00.000000 pyrgo-0.2.0/tests/unit/utilities/test_command.py
+-rw-r--r--   0        0        0      715 2020-02-02 00:00:00.000000 pyrgo-0.2.0/.gitignore
+-rw-r--r--   0        0        0     1076 2020-02-02 00:00:00.000000 pyrgo-0.2.0/LICENSE
+-rw-r--r--   0        0        0        7 2020-02-02 00:00:00.000000 pyrgo-0.2.0/README.md
+-rw-r--r--   0        0        0     2173 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0      781 2020-02-02 00:00:00.000000 pyrgo-0.2.0/PKG-INFO
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `pyrgo-0.1.0/.gitignore` & `pyrgo-0.2.0/.gitignore`

 * *Files 16% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 /target
 
 # Byte-compiled / optimized / DLL files
 __pycache__/
 .pytest_cache/
 *.py[cod]
+.mypy_cache/
 
 # C extensions
 *.so
 
 # Distribution / packaging
 .Python
 .venv/
@@ -65,8 +66,11 @@
 # PyCharm
 .idea/
 
 # VSCode
 .vscode/
 
 # Pyenv
-.python-version
+.python-version
+
+# Mkdocs
+site/
```

### Comparing `pyrgo-0.1.0/LICENSE` & `pyrgo-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pyrgo-0.1.0/Makefile` & `pyrgo-0.2.0/Makefile`

 * *Files identical despite different names*

### Comparing `pyrgo-0.1.0/pyrgo/command/venv.py` & `pyrgo-0.2.0/pyrgo/command/venv.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.1.0/PKG-INFO` & `pyrgo-0.2.0/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,21 +1,24 @@
 Metadata-Version: 2.1
 Name: pyrgo
-Version: 0.1.0
-Classifier: Programming Language :: Rust
+Version: 0.2.0
+Project-URL: Documentation, https://github.com/Tomperez98/pyrgo#readme
+Project-URL: Issues, https://github.com/Tomperez98/pyrgo/issues
+Project-URL: Source, https://github.com/Tomperez98/pyrgo
+Author-email: Tomas Perez Alvarez <tomasperezalvarez@gmail.com>
+License-File: LICENSE
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
+Classifier: Programming Language :: Rust
+Requires-Python: >=3.7
+Requires-Dist: black
 Requires-Dist: click
-Requires-Dist: ruff
+Requires-Dist: hatch
+Requires-Dist: mkdocs-material
 Requires-Dist: mypy
-Requires-Dist: black
 Requires-Dist: pip-tools
-Requires-Dist: maturin ; extra == 'dev'
+Requires-Dist: pytest
+Requires-Dist: ruff
 Provides-Extra: dev
-License-File: LICENSE
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown; charset=UTF-8; variant=GFM
-Project-URL: Documentation, https://github.com/Tomperez98/pyrgo#readme
-Project-URL: Issues, https://github.com/Tomperez98/pyrgo/issues
-Project-URL: Source, https://github.com/Tomperez98/pyrgo
+Description-Content-Type: text/markdown
 
-# pyrgo
+# pyrgo
```

