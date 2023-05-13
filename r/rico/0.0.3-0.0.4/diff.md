# Comparing `tmp/rico-0.0.3.tar.gz` & `tmp/rico-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rico-0.0.3.tar", last modified: Tue May  9 10:30:38 2023, max compression
+gzip compressed data, was "rico-0.0.4.tar", last modified: Sat May 13 14:32:50 2023, max compression
```

## Comparing `rico-0.0.3.tar` & `rico-0.0.4.tar`

### file list

```diff
@@ -1,9 +1,11 @@
--rw-r--r--   0        0        0     1070 2023-05-09 10:30:07.597245 rico-0.0.3/LICENSE
--rw-r--r--   0        0        0       53 2023-05-09 10:30:07.597245 rico-0.0.3/README.md
--rw-r--r--   0        0        0     2489 2023-05-09 10:30:38.255143 rico-0.0.3/pyproject.toml
--rw-r--r--   0        0        0      101 2023-05-09 10:30:07.601245 rico-0.0.3/src/rico/__init__.py
--rw-r--r--   0        0        0       45 2023-05-09 10:30:07.601245 rico-0.0.3/src/rico/_version.py
--rw-r--r--   0        0        0     1075 2023-05-09 10:30:07.601245 rico-0.0.3/src/rico/core.py
--rw-r--r--   0        0        0       18 2023-05-09 10:30:07.601245 rico-0.0.3/tests/__init__.py
--rw-r--r--   0        0        0      751 2023-05-09 10:30:07.601245 rico-0.0.3/tests/test_core.py
--rw-r--r--   0        0        0     1279 1970-01-01 00:00:00.000000 rico-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0     1070 2023-05-13 14:32:24.337670 rico-0.0.4/LICENSE
+-rw-r--r--   0        0        0       53 2023-05-13 14:32:24.337670 rico-0.0.4/README.md
+-rw-r--r--   0        0        0     2692 2023-05-13 14:32:50.094163 rico-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0      106 2023-05-13 14:32:24.337670 rico-0.0.4/src/rico/__init__.py
+-rw-r--r--   0        0        0      340 2023-05-13 14:32:24.337670 rico-0.0.4/src/rico/_version.py
+-rw-r--r--   0        0        0     1075 2023-05-13 14:32:24.337670 rico-0.0.4/src/rico/core.py
+-rw-r--r--   0        0        0     5109 2023-05-13 14:32:24.337670 rico-0.0.4/src/rico/html.py
+-rw-r--r--   0        0        0       18 2023-05-13 14:32:24.337670 rico-0.0.4/tests/__init__.py
+-rw-r--r--   0        0        0      751 2023-05-13 14:32:24.337670 rico-0.0.4/tests/test_core.py
+-rw-r--r--   0        0        0     7879 2023-05-13 14:32:24.337670 rico-0.0.4/tests/test_html.py
+-rw-r--r--   0        0        0     1280 1970-01-01 00:00:00.000000 rico-0.0.4/PKG-INFO
```

### Comparing `rico-0.0.3/LICENSE` & `rico-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `rico-0.0.3/pyproject.toml` & `rico-0.0.4/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -5,29 +5,29 @@
 authors = [
     { name = "Evgeny Ivanov", email = "ivanov.evgeny.n@gmail.com" },
 ]
 dependencies = []
 requires-python = ">=3.10"
 readme = "README.md"
 classifiers = [
-    "Development Status :: 1 - Planning",
+    "Development Status :: 2 - Pre-Alpha",
     "Intended Audience :: Developers",
     "Intended Audience :: Science/Research",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
     "Programming Language :: Python",
     "Programming Language :: Python :: 3.10",
     "Programming Language :: Python :: 3.11",
     "Topic :: Scientific/Engineering",
     "Topic :: Scientific/Engineering :: Visualization",
     "Topic :: Text Processing",
     "Topic :: Text Processing :: Markup",
     "Topic :: Text Processing :: Markup :: HTML",
 ]
-version = "0.0.3"
+version = "0.0.4"
 
 [project.license]
 text = "MIT"
 
 [project.optional-dependencies]
 altair = [
     "altair>=4.2",
@@ -53,47 +53,58 @@
 lint = [
     "ruff",
     "pyright",
     "isort",
 ]
 test = [
     "pytest",
+    "coverage[toml]",
 ]
 
 [tool.pdm.scripts]
+test = "coverage run -m pytest"
 lint = "ruff check ."
 sort = "isort --check --diff ."
 type = "pyright"
-test = "pytest"
 
 [tool.pdm.build]
 package-dir = "src"
 
 [tool.pdm.version]
 source = "scm"
-write_to = "rico/_version.py"
-write_template = "__version__ = \"{}\""
+write_to = "rico/_version.txt"
+
+[tool.pytest.ini_options]
+testpaths = [
+    "tests",
+]
+
+[tool.coverage.run]
+source = [
+    "src/rico",
+]
+
+[tool.coverage.report]
+exclude_lines = [
+    "import",
+    "pragma: no cover",
+]
 
 [tool.isort]
 force_sort_within_sections = true
 include_trailing_comma = true
 lines_after_imports = 2
 multi_line_output = 3
 
 [tool.pyright]
 typeCheckingMode = "strict"
+reportIncompatibleMethodOverride = false
 reportMissingTypeStubs = false
 
-[tool.pytest.ini_options]
-testpaths = [
-    "tests",
-]
-
 [tool.ruff]
-line-length = 80
 select = [
     "A",
     "ANN",
     "ARG",
     "B",
     "C4",
     "C90",
@@ -119,31 +130,35 @@
     "TCH",
     "TID",
     "TRY",
     "UP",
     "W",
 ]
 ignore = [
+    "ANN101",
+    "ANN204",
     "ANN401",
     "B006",
+    "PT001",
+    "SLF001",
 ]
 
 [tool.ruff.per-file-ignores]
 "tests/*" = [
     "ANN201",
     "D100",
     "D103",
     "PLR2004",
 ]
 
 [tool.ruff.isort]
 force-sort-within-sections = true
 lines-after-imports = 2
-
-[tool.ruff.pycodestyle]
-max-doc-length = 80
+known-local-folder = [
+    "rico",
+]
 
 [tool.ruff.pydocstyle]
 convention = "google"
 ignore-decorators = [
     "typing.overload",
 ]
```

### Comparing `rico-0.0.3/src/rico/core.py` & `rico-0.0.4/src/rico/core.py`

 * *Files identical despite different names*

### Comparing `rico-0.0.3/tests/test_core.py` & `rico-0.0.4/tests/test_core.py`

 * *Files identical despite different names*

### Comparing `rico-0.0.3/PKG-INFO` & `rico-0.0.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 2.1
 Name: rico
-Version: 0.0.3
+Version: 0.0.4
 Summary: Rich content to HTML as easy as doc.print(x).
 Author-Email: Evgeny Ivanov <ivanov.evgeny.n@gmail.com>
 License: MIT
-Classifier: Development Status :: 1 - Planning
+Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
```

