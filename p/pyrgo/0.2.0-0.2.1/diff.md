# Comparing `tmp/pyrgo-0.2.0.tar.gz` & `tmp/pyrgo-0.2.1.tar.gz`

## Comparing `pyrgo-0.2.0.tar` & `pyrgo-0.2.1.tar`

### file list

```diff
@@ -1,41 +1,41 @@
--rw-r--r--   0        0        0       26 2020-02-02 00:00:00.000000 pyrgo-0.2.0/.tool-versions
--rw-r--r--   0        0        0     1497 2020-02-02 00:00:00.000000 pyrgo-0.2.0/Makefile
--rw-r--r--   0        0        0       19 2020-02-02 00:00:00.000000 pyrgo-0.2.0/mkdocs.yml
--rw-r--r--   0        0        0      923 2020-02-02 00:00:00.000000 pyrgo-0.2.0/.github/workflows/release.yml
--rw-r--r--   0        0        0     1040 2020-02-02 00:00:00.000000 pyrgo-0.2.0/.github/workflows/test.yml
--rw-r--r--   0        0        0      491 2020-02-02 00:00:00.000000 pyrgo-0.2.0/docs/index.md
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/__init__.py
--rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/__main__.py
--rw-r--r--   0        0        0      828 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/cli.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/py.typed
--rw-r--r--   0        0        0      251 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/utils.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/__init__.py
--rw-r--r--   0        0        0      131 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/add.py
--rw-r--r--   0        0        0      342 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/build.py
--rw-r--r--   0        0        0      595 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/check.py
--rw-r--r--   0        0        0      140 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/clean.py
--rw-r--r--   0        0        0      636 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/fmt.py
--rw-r--r--   0        0        0      137 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/init.py
--rw-r--r--   0        0        0      101 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/lock.py
--rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/new.py
--rw-r--r--   0        0        0      130 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/remove.py
--rw-r--r--   0        0        0     1099 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/test.py
--rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/venv.py
--rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/__init__.py
--rw-r--r--   0        0        0     1171 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/build.py
--rw-r--r--   0        0        0      727 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/new.py
--rw-r--r--   0        0        0      363 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/root.py
--rw-r--r--   0        0        0     1468 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/command/docs/serve.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/utilities/__init__.py
--rw-r--r--   0        0        0     1177 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/utilities/command.py
--rw-r--r--   0        0        0      901 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyrgo/utilities/project.py
--rw-r--r--   0        0        0     3642 2020-02-02 00:00:00.000000 pyrgo-0.2.0/requirements/core.lock
--rw-r--r--   0        0        0     3653 2020-02-02 00:00:00.000000 pyrgo-0.2.0/requirements/dev.lock
--rw-r--r--   0        0        0      928 2020-02-02 00:00:00.000000 pyrgo-0.2.0/scripts/new_release.py
--rw-r--r--   0        0        0      155 2020-02-02 00:00:00.000000 pyrgo-0.2.0/tests/integration/resources/pyproject.toml
--rw-r--r--   0        0        0      731 2020-02-02 00:00:00.000000 pyrgo-0.2.0/tests/unit/utilities/test_command.py
--rw-r--r--   0        0        0      715 2020-02-02 00:00:00.000000 pyrgo-0.2.0/.gitignore
--rw-r--r--   0        0        0     1076 2020-02-02 00:00:00.000000 pyrgo-0.2.0/LICENSE
--rw-r--r--   0        0        0        7 2020-02-02 00:00:00.000000 pyrgo-0.2.0/README.md
--rw-r--r--   0        0        0     2173 2020-02-02 00:00:00.000000 pyrgo-0.2.0/pyproject.toml
--rw-r--r--   0        0        0      781 2020-02-02 00:00:00.000000 pyrgo-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0       26 2020-02-02 00:00:00.000000 pyrgo-0.2.1/.tool-versions
+-rw-r--r--   0        0        0     1497 2020-02-02 00:00:00.000000 pyrgo-0.2.1/Makefile
+-rw-r--r--   0        0        0       19 2020-02-02 00:00:00.000000 pyrgo-0.2.1/mkdocs.yml
+-rw-r--r--   0        0        0      923 2020-02-02 00:00:00.000000 pyrgo-0.2.1/.github/workflows/release.yml
+-rw-r--r--   0        0        0     1040 2020-02-02 00:00:00.000000 pyrgo-0.2.1/.github/workflows/test.yml
+-rw-r--r--   0        0        0      491 2020-02-02 00:00:00.000000 pyrgo-0.2.1/docs/index.md
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/__init__.py
+-rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/__main__.py
+-rw-r--r--   0        0        0      828 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/cli.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/py.typed
+-rw-r--r--   0        0        0      251 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/utils.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/__init__.py
+-rw-r--r--   0        0        0      131 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/add.py
+-rw-r--r--   0        0        0      342 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/build.py
+-rw-r--r--   0        0        0      714 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/check.py
+-rw-r--r--   0        0        0      140 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/clean.py
+-rw-r--r--   0        0        0      756 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/fmt.py
+-rw-r--r--   0        0        0      137 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/init.py
+-rw-r--r--   0        0        0      101 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/lock.py
+-rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/new.py
+-rw-r--r--   0        0        0      130 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/remove.py
+-rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/test.py
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/venv.py
+-rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/docs/__init__.py
+-rw-r--r--   0        0        0     1171 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/docs/build.py
+-rw-r--r--   0        0        0      727 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/docs/new.py
+-rw-r--r--   0        0        0      363 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/docs/root.py
+-rw-r--r--   0        0        0     1468 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/command/docs/serve.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/utilities/__init__.py
+-rw-r--r--   0        0        0     1177 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/utilities/command.py
+-rw-r--r--   0        0        0     1168 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyrgo/utilities/project.py
+-rw-r--r--   0        0        0     3673 2020-02-02 00:00:00.000000 pyrgo-0.2.1/requirements/core.lock
+-rw-r--r--   0        0        0     3684 2020-02-02 00:00:00.000000 pyrgo-0.2.1/requirements/dev.lock
+-rw-r--r--   0        0        0      928 2020-02-02 00:00:00.000000 pyrgo-0.2.1/scripts/new_release.py
+-rw-r--r--   0        0        0      155 2020-02-02 00:00:00.000000 pyrgo-0.2.1/tests/integration/resources/pyproject.toml
+-rw-r--r--   0        0        0      731 2020-02-02 00:00:00.000000 pyrgo-0.2.1/tests/unit/utilities/test_command.py
+-rw-r--r--   0        0        0      728 2020-02-02 00:00:00.000000 pyrgo-0.2.1/.gitignore
+-rw-r--r--   0        0        0     1076 2020-02-02 00:00:00.000000 pyrgo-0.2.1/LICENSE
+-rw-r--r--   0        0        0        7 2020-02-02 00:00:00.000000 pyrgo-0.2.1/README.md
+-rw-r--r--   0        0        0     2186 2020-02-02 00:00:00.000000 pyrgo-0.2.1/pyproject.toml
+-rw-r--r--   0        0        0      802 2020-02-02 00:00:00.000000 pyrgo-0.2.1/PKG-INFO
```

### Comparing `pyrgo-0.2.0/Makefile` & `pyrgo-0.2.1/Makefile`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/.github/workflows/release.yml` & `pyrgo-0.2.1/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/.github/workflows/test.yml` & `pyrgo-0.2.1/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/pyrgo/cli.py` & `pyrgo-0.2.1/pyrgo/cli.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/pyrgo/command/test.py` & `pyrgo-0.2.1/pyrgo/command/test.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,26 +1,35 @@
 """test command."""
 
-from typing import Optional
+import pathlib
+from typing import List, Optional
 
 import click
 
 from pyrgo.utilities.command import PythonExecCommand, inform_and_run_program
+from pyrgo.utilities.project import (
+    list_pytest_markers,
+    read_pyproject,
+)
+
+
+def dynamic_marker_choices() -> List[str]:
+    """Dynamic markers for options."""
+    cwd = pathlib.Path().cwd()
+    content = read_pyproject(cwd=cwd)
+    return list_pytest_markers(content=content)
 
 
 @click.command()
 @click.option(
     "-m",
     "--marked",
     "marker",
     type=click.Choice(
-        choices=[
-            "unit",
-            "integration",
-        ],
+        choices=dynamic_marker_choices(),
     ),
     default=None,
     help="Run tests based on marks. By default all tests are executed.",
 )
 @click.option(
     "--no-strict-markers",
     "no_strict_markers",
@@ -31,17 +40,15 @@
 )
 def test(
     *,
     no_strict_markers: bool,
     marker: Optional[str],
 ) -> None:
     """Execute tests using `pytest`."""
-    args_to_add = [
-        "tests",
-    ]
+    args_to_add: List[str] = []
     if not no_strict_markers:
         args_to_add.append("--strict-markers")
 
     if marker:
         args_to_add.extend(["-m", marker])
 
     inform_and_run_program(
```

### Comparing `pyrgo-0.2.0/pyrgo/command/venv.py` & `pyrgo-0.2.1/pyrgo/command/venv.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/pyrgo/command/docs/build.py` & `pyrgo-0.2.1/pyrgo/command/docs/build.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/pyrgo/command/docs/new.py` & `pyrgo-0.2.1/pyrgo/command/docs/new.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/pyrgo/command/docs/serve.py` & `pyrgo-0.2.1/pyrgo/command/docs/serve.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/pyrgo/utilities/command.py` & `pyrgo-0.2.1/pyrgo/utilities/command.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/requirements/core.lock` & `pyrgo-0.2.1/requirements/core.lock`

 * *Files 1% similar despite different names*

```diff
@@ -166,14 +166,15 @@
 tomli==2.0.1
     # via
     #   black
     #   build
     #   hatchling
     #   mypy
     #   pyproject-hooks
+    #   pyrgo (pyproject.toml)
     #   pytest
 tomli-w==1.0.0
     # via hatch
 tomlkit==0.11.8
     # via hatch
 trove-classifiers==2023.5.2
     # via hatchling
```

### Comparing `pyrgo-0.2.0/requirements/dev.lock` & `pyrgo-0.2.1/requirements/dev.lock`

 * *Files 1% similar despite different names*

```diff
@@ -166,14 +166,15 @@
 tomli==2.0.1
     # via
     #   black
     #   build
     #   hatchling
     #   mypy
     #   pyproject-hooks
+    #   pyrgo (pyproject.toml)
     #   pytest
 tomli-w==1.0.0
     # via hatch
 tomlkit==0.11.8
     # via hatch
 trove-classifiers==2023.5.2
     # via hatchling
```

### Comparing `pyrgo-0.2.0/scripts/new_release.py` & `pyrgo-0.2.1/scripts/new_release.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/tests/unit/utilities/test_command.py` & `pyrgo-0.2.1/tests/unit/utilities/test_command.py`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/.gitignore` & `pyrgo-0.2.1/.gitignore`

 * *Files 17% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 /target
 
 # Byte-compiled / optimized / DLL files
 __pycache__/
 .pytest_cache/
 *.py[cod]
 .mypy_cache/
+.ruff_cache/
 
 # C extensions
 *.so
 
 # Distribution / packaging
 .Python
 .venv/
```

### Comparing `pyrgo-0.2.0/LICENSE` & `pyrgo-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `pyrgo-0.2.0/pyproject.toml` & `pyrgo-0.2.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "pyrgo"
-version = "0.2.0"
+version = "0.2.1"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
     "Programming Language :: Rust",
     "Programming Language :: Python :: Implementation :: CPython",
     "Programming Language :: Python :: Implementation :: PyPy",
 ]
@@ -16,15 +16,16 @@
     "click",
     "ruff",
     "mypy",
     "black",
     "pip-tools",
     "pytest",
     "mkdocs-material",
-    "hatch"
+    "hatch",
+    "tomli"
 ]
 
 [[project.authors]]
 name = "Tomas Perez Alvarez"
 email = "tomasperezalvarez@gmail.com"
 
 [project.optional-dependencies]
```

### Comparing `pyrgo-0.2.0/PKG-INFO` & `pyrgo-0.2.1/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyrgo
-Version: 0.2.0
+Version: 0.2.1
 Project-URL: Documentation, https://github.com/Tomperez98/pyrgo#readme
 Project-URL: Issues, https://github.com/Tomperez98/pyrgo/issues
 Project-URL: Source, https://github.com/Tomperez98/pyrgo
 Author-email: Tomas Perez Alvarez <tomasperezalvarez@gmail.com>
 License-File: LICENSE
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
@@ -14,11 +14,12 @@
 Requires-Dist: click
 Requires-Dist: hatch
 Requires-Dist: mkdocs-material
 Requires-Dist: mypy
 Requires-Dist: pip-tools
 Requires-Dist: pytest
 Requires-Dist: ruff
+Requires-Dist: tomli
 Provides-Extra: dev
 Description-Content-Type: text/markdown
 
 # pyrgo
```

