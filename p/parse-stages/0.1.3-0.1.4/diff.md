# Comparing `tmp/parse_stages-0.1.3.tar.gz` & `tmp/parse_stages-0.1.4.tar.gz`

## Comparing `parse_stages-0.1.3.tar` & `parse_stages-0.1.4.tar`

### file list

```diff
@@ -1,30 +1,32 @@
--rw-r--r--   0        0        0      622 2020-02-02 00:00:00.000000 parse_stages-0.1.3/.editorconfig
--rw-r--r--   0        0        0     1253 2020-02-02 00:00:00.000000 parse_stages-0.1.3/mkdocs.yml
--rw-r--r--   0        0        0      215 2020-02-02 00:00:00.000000 parse_stages-0.1.3/setup.cfg
--rw-r--r--   0        0        0     3166 2020-02-02 00:00:00.000000 parse_stages-0.1.3/tox.ini
--rw-r--r--   0        0        0     1267 2020-02-02 00:00:00.000000 parse_stages-0.1.3/LICENSES/BSD-2-Clause.txt
--rw-r--r--   0        0        0      169 2020-02-02 00:00:00.000000 parse_stages-0.1.3/config/ruff-all/pyproject.toml
--rw-r--r--   0        0        0      587 2020-02-02 00:00:00.000000 parse_stages-0.1.3/config/ruff-base/pyproject.toml
--rw-r--r--   0        0        0      601 2020-02-02 00:00:00.000000 parse_stages-0.1.3/config/ruff-most/pyproject.toml
--rw-r--r--   0        0        0      528 2020-02-02 00:00:00.000000 parse_stages-0.1.3/docs/api.md
--rw-r--r--   0        0        0     4865 2020-02-02 00:00:00.000000 parse_stages-0.1.3/docs/changes.md
--rw-r--r--   0        0        0     4358 2020-02-02 00:00:00.000000 parse_stages-0.1.3/docs/index.md
--rw-r--r--   0        0        0      860 2020-02-02 00:00:00.000000 parse_stages-0.1.3/docs/language.md
--rw-r--r--   0        0        0      517 2020-02-02 00:00:00.000000 parse_stages-0.1.3/nix/mkdocs.nix
--rw-r--r--   0        0        0      470 2020-02-02 00:00:00.000000 parse_stages-0.1.3/nix/python-pytest.nix
--rwxr-xr-x   0        0        0      266 2020-02-02 00:00:00.000000 parse_stages-0.1.3/nix/reformat.sh
--rwxr-xr-x   0        0        0      735 2020-02-02 00:00:00.000000 parse_stages-0.1.3/nix/run-pytest.sh
--rw-r--r--   0        0        0      121 2020-02-02 00:00:00.000000 parse_stages-0.1.3/requirements/install.txt
--rw-r--r--   0        0        0      118 2020-02-02 00:00:00.000000 parse_stages-0.1.3/requirements/test.txt
--rw-r--r--   0        0        0     4284 2020-02-02 00:00:00.000000 parse_stages-0.1.3/src/parse_stages/__init__.py
--rw-r--r--   0        0        0     1339 2020-02-02 00:00:00.000000 parse_stages-0.1.3/src/parse_stages/defs.py
--rw-r--r--   0        0        0     2621 2020-02-02 00:00:00.000000 parse_stages-0.1.3/src/parse_stages/expr.py
--rw-r--r--   0        0        0     4552 2020-02-02 00:00:00.000000 parse_stages-0.1.3/src/parse_stages/p_pyp.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 parse_stages-0.1.3/src/parse_stages/py.typed
--rw-r--r--   0        0        0      152 2020-02-02 00:00:00.000000 parse_stages-0.1.3/unit_tests/__init__.py
--rw-r--r--   0        0        0     1876 2020-02-02 00:00:00.000000 parse_stages-0.1.3/unit_tests/test_eval.py
--rw-r--r--   0        0        0     2381 2020-02-02 00:00:00.000000 parse_stages-0.1.3/unit_tests/test_parse.py
--rw-r--r--   0        0        0      129 2020-02-02 00:00:00.000000 parse_stages-0.1.3/.gitignore
--rw-r--r--   0        0        0     4450 2020-02-02 00:00:00.000000 parse_stages-0.1.3/README.md
--rw-r--r--   0        0        0     2436 2020-02-02 00:00:00.000000 parse_stages-0.1.3/pyproject.toml
--rw-r--r--   0        0        0     5000 2020-02-02 00:00:00.000000 parse_stages-0.1.3/PKG-INFO
+-rw-r--r--   0        0        0      622 2020-02-02 00:00:00.000000 parse_stages-0.1.4/.editorconfig
+-rw-r--r--   0        0        0      219 2020-02-02 00:00:00.000000 parse_stages-0.1.4/.readthedocs.yaml
+-rw-r--r--   0        0        0     1253 2020-02-02 00:00:00.000000 parse_stages-0.1.4/mkdocs.yml
+-rw-r--r--   0        0        0      215 2020-02-02 00:00:00.000000 parse_stages-0.1.4/setup.cfg
+-rw-r--r--   0        0        0     3066 2020-02-02 00:00:00.000000 parse_stages-0.1.4/tox.ini
+-rw-r--r--   0        0        0     1267 2020-02-02 00:00:00.000000 parse_stages-0.1.4/LICENSES/BSD-2-Clause.txt
+-rw-r--r--   0        0        0      169 2020-02-02 00:00:00.000000 parse_stages-0.1.4/config/ruff-all/pyproject.toml
+-rw-r--r--   0        0        0      587 2020-02-02 00:00:00.000000 parse_stages-0.1.4/config/ruff-base/pyproject.toml
+-rw-r--r--   0        0        0      610 2020-02-02 00:00:00.000000 parse_stages-0.1.4/config/ruff-most/pyproject.toml
+-rw-r--r--   0        0        0      562 2020-02-02 00:00:00.000000 parse_stages-0.1.4/docs/api.md
+-rw-r--r--   0        0        0     5496 2020-02-02 00:00:00.000000 parse_stages-0.1.4/docs/changes.md
+-rw-r--r--   0        0        0     4517 2020-02-02 00:00:00.000000 parse_stages-0.1.4/docs/index.md
+-rw-r--r--   0        0        0      860 2020-02-02 00:00:00.000000 parse_stages-0.1.4/docs/language.md
+-rw-r--r--   0        0        0      517 2020-02-02 00:00:00.000000 parse_stages-0.1.4/nix/mkdocs.nix
+-rw-r--r--   0        0        0      470 2020-02-02 00:00:00.000000 parse_stages-0.1.4/nix/python-pytest.nix
+-rwxr-xr-x   0        0        0      266 2020-02-02 00:00:00.000000 parse_stages-0.1.4/nix/reformat.sh
+-rwxr-xr-x   0        0        0      735 2020-02-02 00:00:00.000000 parse_stages-0.1.4/nix/run-pytest.sh
+-rw-r--r--   0        0        0      214 2020-02-02 00:00:00.000000 parse_stages-0.1.4/requirements/docs.txt
+-rw-r--r--   0        0        0      121 2020-02-02 00:00:00.000000 parse_stages-0.1.4/requirements/install.txt
+-rw-r--r--   0        0        0      118 2020-02-02 00:00:00.000000 parse_stages-0.1.4/requirements/test.txt
+-rw-r--r--   0        0        0     4324 2020-02-02 00:00:00.000000 parse_stages-0.1.4/src/parse_stages/__init__.py
+-rw-r--r--   0        0        0     1339 2020-02-02 00:00:00.000000 parse_stages-0.1.4/src/parse_stages/defs.py
+-rw-r--r--   0        0        0     2621 2020-02-02 00:00:00.000000 parse_stages-0.1.4/src/parse_stages/expr.py
+-rw-r--r--   0        0        0     5239 2020-02-02 00:00:00.000000 parse_stages-0.1.4/src/parse_stages/p_pyp.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 parse_stages-0.1.4/src/parse_stages/py.typed
+-rw-r--r--   0        0        0      152 2020-02-02 00:00:00.000000 parse_stages-0.1.4/unit_tests/__init__.py
+-rw-r--r--   0        0        0     1876 2020-02-02 00:00:00.000000 parse_stages-0.1.4/unit_tests/test_eval.py
+-rw-r--r--   0        0        0     2790 2020-02-02 00:00:00.000000 parse_stages-0.1.4/unit_tests/test_parse.py
+-rw-r--r--   0        0        0      129 2020-02-02 00:00:00.000000 parse_stages-0.1.4/.gitignore
+-rw-r--r--   0        0        0     4609 2020-02-02 00:00:00.000000 parse_stages-0.1.4/README.md
+-rw-r--r--   0        0        0     2341 2020-02-02 00:00:00.000000 parse_stages-0.1.4/pyproject.toml
+-rw-r--r--   0        0        0     5159 2020-02-02 00:00:00.000000 parse_stages-0.1.4/PKG-INFO
```

### Comparing `parse_stages-0.1.3/.editorconfig` & `parse_stages-0.1.4/.editorconfig`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/mkdocs.yml` & `parse_stages-0.1.4/mkdocs.yml`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/tox.ini` & `parse_stages-0.1.4/tox.ini`

 * *Files 4% similar despite different names*

```diff
@@ -21,46 +21,46 @@
   unit_tests
 
 [testenv:ruff]
 skip_install = True
 tags =
   check
 deps =
-  ruff >= 0.0.265, < 0.1
+  ruff >= 0.0.267, < 0.1
 commands =
   ruff check --config config/ruff-most/pyproject.toml -- {[defs]pyfiles}
 
 [testenv:ruff-all]
 skip_install = True
 tags =
   check
 deps =
-  ruff == 0.0.265
+  ruff == 0.0.267
 commands =
   ruff check --config config/ruff-all/pyproject.toml -- {[defs]pyfiles}
 
 [testenv:format]
 skip_install = True
 tags =
   check
 deps =
   black >= 23, < 24
-  ruff >= 0.0.265, < 0.1
+  ruff >= 0.0.267, < 0.1
 commands =
   ruff check --config config/ruff-base/pyproject.toml --select=I --diff -- {[defs]pyfiles}
   black --check {[defs]pyfiles}
 
 [testenv:reformat]
 skip_install = True
 tags =
   format
   manual
 deps =
   black >= 23, < 24
-  ruff >= 0.0.265, < 0.1
+  ruff >= 0.0.267, < 0.1
 commands =
   ruff check --config config/ruff-base/pyproject.toml --select=I --fix -- {[defs]pyfiles}
   black {[defs]pyfiles}
 
 # Add flake8-import-conventions if it ever hits PyPI
 [testenv:pep8]
 skip_install = True
@@ -151,18 +151,15 @@
 
 [testenv:docs]
 skip_install = True
 tags =
   docs
   manual
 deps =
-  mkdocs >= 1.4.2, < 2
-  mkdocs-material >= 9.1.2, < 10
-  mkdocstrings >= 0.21.2, < 0.22
-  mkdocstrings-python >= 0.10, < 0.11
+  -r requirements/docs.txt
 commands =
   mkdocs build
 
 [testenv:reuse]
 skip_install = True
 tags =
   check
```

### Comparing `parse_stages-0.1.3/LICENSES/BSD-2-Clause.txt` & `parse_stages-0.1.4/LICENSES/BSD-2-Clause.txt`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/config/ruff-base/pyproject.toml` & `parse_stages-0.1.4/config/ruff-base/pyproject.toml`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/config/ruff-most/pyproject.toml` & `parse_stages-0.1.4/config/ruff-most/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -18,14 +18,15 @@
   "DTZ",
   "E",
   "EM",
   "ERA",
   "EXE",
   "F",
   "FBT",
+  "FLY",
   "G",
   "I",
   "ICN",
   "INP",
   "INT",
   "ISC",
   "N",
```

### Comparing `parse_stages-0.1.3/docs/api.md` & `parse_stages-0.1.4/docs/api.md`

 * *Files 13% similar despite different names*

```diff
@@ -25,10 +25,12 @@
 
 ::: parse_stages.TagExpr
 
 ::: parse_stages.KeywordExpr
 
 ## The helper functions
 
+::: parse_stages.EMPTY_SET_SPECS
+
 ::: parse_stages.parse_spec
 
 ::: parse_stages.parse_stage_ids
```

### Comparing `parse_stages-0.1.3/docs/changes.md` & `parse_stages-0.1.4/docs/changes.md`

 * *Files 4% similar despite different names*

```diff
@@ -8,14 +8,34 @@
 All notable changes to the parse-stages project will be documented in this file.
 
 The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
 and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
 
 ## [Unreleased]
 
+## [0.1.4] - 2023-05-13
+
+### Additions
+
+- Documentation:
+    - add a [ReadTheDocs mirror](https://parse-stages.readthedocs.io/)
+- Main source:
+    - `parse_stage_ids()`: allow an empty set to be specified by the exact
+      strings "", "0", or "none"
+
+### Other changes
+
+- Build system:
+    - drop the obsolete `tool.setuptools.*` sections from the `pyproject.toml` file
+- Documentation:
+    - bump the version of `mkdocstrings-python` with no changes
+- Test suite:
+    - Ruff:
+        - use Ruff 0.0.267, enable the `FLY` checks area
+
 ## [0.1.3] - 2023-05-07
 
 ### Fixes
 
 - Add a blank line to a docstring section (ruff D214).
 - Drop the text in a `NotImplementedError` raised in an abstract method;
   it should be obvious (ruff EM101)
@@ -116,12 +136,13 @@
 
 ## [0.1.0] - 2023-01-25
 
 ### Started
 
 - First public release.
 
-[Unreleased]: https://gitlab.com/ppentchev/parse-stages/-/compare/release%2F0.1.3...main
+[Unreleased]: https://gitlab.com/ppentchev/parse-stages/-/compare/release%2F0.1.4...main
+[0.1.4]: https://gitlab.com/ppentchev/parse-stages/-/compare/release%2F0.1.3...release%2F0.1.4
 [0.1.3]: https://gitlab.com/ppentchev/parse-stages/-/compare/release%2F0.1.2...release%2F0.1.3
 [0.1.2]: https://gitlab.com/ppentchev/parse-stages/-/compare/release%2F0.1.1...release%2F0.1.2
 [0.1.1]: https://gitlab.com/ppentchev/parse-stages/-/compare/release%2F0.1.0...release%2F0.1.1
 [0.1.0]: https://gitlab.com/ppentchev/parse-stages/-/tags/release%2F0.1.0
```

### Comparing `parse_stages-0.1.3/docs/index.md` & `parse_stages-0.1.4/docs/index.md`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 <!--
 SPDX-FileCopyrightText: Peter Pentchev <roam@ringlet.net>
 SPDX-License-Identifier: BSD-2-Clause
 -->
 
 # Parse a mini-language for selecting objects by tag or name
 
-\[[Home][ringlet-parse-stages] | [GitLab][gitlab] | [PyPI][pypi]\]
+\[[Home][ringlet-parse-stages] | [GitLab][gitlab] | [PyPI][pypi] | [ReadTheDocs][readthedocs]\]
 
 ## Overview
 
 The `parse-stages` Python library may be used by other tools to group
 objects (e.g. [Tox] or [Nox] test environments) for step-by-step processing
 (e.g. running some tests in parallel, then only running others if the first
 group passes).
@@ -22,15 +22,15 @@
 [nox]: https://nox.thea.codes/en/stable/ "The nox flexible automation tool"
 
 ## Installation
 
 A program that uses the `parse-stages` library should specify it in
 its list of requirements, e.g. using [PEP508][pep508] syntax:
 
-    parse-stages >= 0.1.3, < 0.2
+    parse-stages >= 0.1.4, < 0.2
 
 [pep508]: https://peps.python.org/pep-0508/ "PEP 508 – Dependency specification for Python Software Packages"
 
 ## Parsing a stage specification
 
 The `parse_spec()` function parses a string specification into
 a [BoolExpr][parse_stages.BoolExpr] object that may later be used to
@@ -96,13 +96,14 @@
     quick_names = [env.name for env in all_envs if e_check_quick.evaluate(env)]
 ```
 
 ## Contact
 
 The `parse-stages` library was written by [Peter Pentchev][roam].
 It is developed in [a GitLab repository][gitlab]. This documentation is
-hosted at [Ringlet][ringlet-parse-stages].
+hosted at [Ringlet][ringlet-parse-stages] with a copy at [ReadTheDocs][readthedocs].
 
 [roam]: mailto:roam@ringlet.net "Peter Pentchev"
 [gitlab]: https://gitlab.com/ppentchev/parse-stages "The parse-stages GitLab repository"
 [pypi]: https://pypi.org/project/parse-stages/ "The parse-stages Python Package Index page"
+[readthedocs]: https://parse-stages.readthedocs.io/ "The parse-stages ReadTheDocs page"
 [ringlet-parse-stages]: https://devel.ringlet.net/devel/parse-stages/ "The Ringlet parse-stages homepage"
```

### Comparing `parse_stages-0.1.3/docs/language.md` & `parse_stages-0.1.4/docs/language.md`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/nix/mkdocs.nix` & `parse_stages-0.1.4/nix/mkdocs.nix`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/nix/run-pytest.sh` & `parse_stages-0.1.4/nix/run-pytest.sh`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/src/parse_stages/__init__.py` & `parse_stages-0.1.4/src/parse_stages/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -96,23 +96,24 @@
     # Or if we only care about the names...
     quick_names = [env.name for env in all_envs if e_check_quick.evaluate(env)]
 
 """
 
 from .defs import VERSION, Tagged, TaggedFrozen  # isort: skip
 from .expr import AndExpr, BoolExpr, KeywordExpr, NotExpr, OrExpr, TagExpr  # isort: skip
-from .p_pyp import parse_spec, parse_stage_ids  # isort: skip
+from .p_pyp import EMPTY_SET_SPECS, parse_spec, parse_stage_ids  # isort: skip
 
 
 __all__ = [
     "VERSION",
     "Tagged",
     "TaggedFrozen",
     "AndExpr",
     "BoolExpr",
     "KeywordExpr",
     "NotExpr",
     "OrExpr",
     "TagExpr",
+    "EMPTY_SET_SPECS",
     "parse_spec",
     "parse_stage_ids",
 ]
```

### Comparing `parse_stages-0.1.3/src/parse_stages/defs.py` & `parse_stages-0.1.4/src/parse_stages/defs.py`

 * *Files 1% similar despite different names*

```diff
@@ -42,8 +42,8 @@
         """Get the strings to look for keywords in.
 
         Default: the object's `name` attribute.
         """
         return [self.name]
 
 
-VERSION = "0.1.3"
+VERSION = "0.1.4"
```

### Comparing `parse_stages-0.1.3/src/parse_stages/expr.py` & `parse_stages-0.1.4/src/parse_stages/expr.py`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/src/parse_stages/p_pyp.py` & `parse_stages-0.1.4/src/parse_stages/p_pyp.py`

 * *Files 17% similar despite different names*

```diff
@@ -8,14 +8,18 @@
 from __future__ import annotations
 
 import pyparsing as pyp
 
 from . import expr
 
 
+EMPTY_SET_SPECS = ["", "0", "none"]
+"""The list of exact strings that `parse_stage_ids()` will return an empty list for."""
+
+
 _p_ws = pyp.White()[...]
 
 _p_tag = pyp.Char("@").suppress() + pyp.Word(pyp.alphanums + "_-")
 
 _p_keyword = pyp.Word(pyp.alphanums + "_-")
 
 _p_atom = _p_tag | _p_keyword
@@ -126,12 +130,25 @@
     ), repr(tokens)
     return list(range(tokens[0], tokens[1] + 1))
 
 
 _p_stage_ids_complete = _p_stage_ids.leave_whitespace()
 
 
-def parse_stage_ids(spec: str) -> list[int]:
-    """Parse a list of stage ranges, return them as zero-based indices."""
+def parse_stage_ids(spec: str, *, empty_set_specs: list[str] | None = None) -> list[int]:
+    """Parse a list of stage ranges, return them as zero-based indices.
+
+    As a special case, the exact strings "" (an empty string), "0", and "none" will
+    produce an empty list. Note that none of these strings are considered valid
+    stage ranges, so they cannot be combined with any others (e.g. "0,3" is invalid).
+
+    The default list of strings that signify an empty set ("", "0", "none") may be
+    overridden by the `empty_set_specs` parameter.
+    """
+    if empty_set_specs is None:
+        empty_set_specs = EMPTY_SET_SPECS
+    if spec in empty_set_specs:
+        return []
+
     res: list[int] = _p_stage_ids_complete.parse_string(spec, parse_all=True).as_list()
     assert all(isinstance(item, int) and item >= 0 for item in res), repr(res)
     return res
```

### Comparing `parse_stages-0.1.3/unit_tests/test_eval.py` & `parse_stages-0.1.4/unit_tests/test_eval.py`

 * *Files identical despite different names*

### Comparing `parse_stages-0.1.3/README.md` & `parse_stages-0.1.4/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 <!--
 SPDX-FileCopyrightText: Peter Pentchev <roam@ringlet.net>
 SPDX-License-Identifier: BSD-2-Clause
 -->
 
 # Parse a mini-language for selecting objects by tag or name
 
-\[[Home][ringlet-parse-stages] | [GitLab][gitlab] | [PyPI][pypi]\]
+\[[Home][ringlet-parse-stages] | [GitLab][gitlab] | [PyPI][pypi] | [ReadTheDocs][readthedocs]\]
 
 This library is mostly useful for command-line parsing by other tools like
 `tox-stages` and `nox-stages`. It may be used to parse e.g. a command-line
 specification like `@check and not pylint` or `@tests or ruff` and then
 match it against a list of objects that have names and lists of tags.
 
 ## Parse stage specifications
@@ -103,13 +103,14 @@
     quick_names = [env.name for env in all_envs if e_check_quick.evaluate(env)]
 
 
 ## Contact
 
 The `parse-stages` library was written by [Peter Pentchev][roam].
 It is developed in [a GitLab repository][gitlab]. This documentation is
-hosted at [Ringlet][ringlet-parse-stages].
+hosted at [Ringlet][ringlet-parse-stages] with a copy at [ReadTheDocs][readthedocs].
 
 [roam]: mailto:roam@ringlet.net "Peter Pentchev"
 [gitlab]: https://gitlab.com/ppentchev/parse-stages "The parse-stages GitLab repository"
 [pypi]: https://pypi.org/project/parse-stages/ "The parse-stages Python Package Index page"
+[readthedocs]: https://parse-stages.readthedocs.io/ "The parse-stages ReadTheDocs page"
 [ringlet-parse-stages]: https://devel.ringlet.net/devel/parse-stages/ "The Ringlet parse-stages homepage"
```

### Comparing `parse_stages-0.1.3/pyproject.toml` & `parse_stages-0.1.4/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -30,20 +30,14 @@
 
 [tool.hatch.metadata.hooks.requirements_txt]
 files = ["requirements/install.txt"]
 
 [tool.hatch.version]
 path = "src/parse_stages/defs.py"
 
-[tool.setuptools]
-zip-safe = true
-
-[tool.setuptools.package-data]
-parse_stages = ["py.typed"]
-
 [tool.black]
 target-version = ["py38", "py39", "py310", "py311"]
 line-length = 100
 
 [tool.mypy]
 strict = true
 python_version = "3.8"
```

### Comparing `parse_stages-0.1.3/PKG-INFO` & `parse_stages-0.1.4/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: parse_stages
-Version: 0.1.3
+Version: 0.1.4
 Summary: Parse an expression for selecting stages and tags
 Project-URL: Homepage, https://devel.ringlet.net/devel/parse-stages/
 Project-URL: Changes, https://devel.ringlet.net/devel/parse-stages/changes/
 Project-URL: Issue Tracker, https://gitlab.com/ppentchev/parse-stages/-/issues
 Project-URL: Source Code, https://gitlab.com/ppentchev/parse-stages
 Author-email: Peter Pentchev <roam@ringlet.net>
 Requires-Python: >=3.8
@@ -14,15 +14,15 @@
 <!--
 SPDX-FileCopyrightText: Peter Pentchev <roam@ringlet.net>
 SPDX-License-Identifier: BSD-2-Clause
 -->
 
 # Parse a mini-language for selecting objects by tag or name
 
-\[[Home][ringlet-parse-stages] | [GitLab][gitlab] | [PyPI][pypi]\]
+\[[Home][ringlet-parse-stages] | [GitLab][gitlab] | [PyPI][pypi] | [ReadTheDocs][readthedocs]\]
 
 This library is mostly useful for command-line parsing by other tools like
 `tox-stages` and `nox-stages`. It may be used to parse e.g. a command-line
 specification like `@check and not pylint` or `@tests or ruff` and then
 match it against a list of objects that have names and lists of tags.
 
 ## Parse stage specifications
@@ -116,13 +116,14 @@
     quick_names = [env.name for env in all_envs if e_check_quick.evaluate(env)]
 
 
 ## Contact
 
 The `parse-stages` library was written by [Peter Pentchev][roam].
 It is developed in [a GitLab repository][gitlab]. This documentation is
-hosted at [Ringlet][ringlet-parse-stages].
+hosted at [Ringlet][ringlet-parse-stages] with a copy at [ReadTheDocs][readthedocs].
 
 [roam]: mailto:roam@ringlet.net "Peter Pentchev"
 [gitlab]: https://gitlab.com/ppentchev/parse-stages "The parse-stages GitLab repository"
 [pypi]: https://pypi.org/project/parse-stages/ "The parse-stages Python Package Index page"
+[readthedocs]: https://parse-stages.readthedocs.io/ "The parse-stages ReadTheDocs page"
 [ringlet-parse-stages]: https://devel.ringlet.net/devel/parse-stages/ "The Ringlet parse-stages homepage"
```

