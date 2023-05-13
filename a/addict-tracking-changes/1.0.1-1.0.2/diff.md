# Comparing `tmp/addict-tracking-changes-1.0.1.tar.gz` & `tmp/addict-tracking-changes-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "addict-tracking-changes-1.0.1.tar", last modified: Thu May 11 12:42:30 2023, max compression
+gzip compressed data, was "addict-tracking-changes-1.0.2.tar", last modified: Sat May 13 11:08:02 2023, max compression
```

## Comparing `addict-tracking-changes-1.0.1.tar` & `addict-tracking-changes-1.0.2.tar`

### file list

```diff
@@ -1,33 +1,33 @@
--rw-r--r--   0        0        0      141 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.1/.flake8
--rw-r--r--   0        0        0     1886 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.1/.gitignore
--rw-r--r--   0        0        0     1070 2022-11-29 03:20:21.000000 addict-tracking-changes-1.0.1/LICENSE
--rw-r--r--   0        0        0      325 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.1/Pipfile
--rw-r--r--   0        0        0    41152 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.1/Pipfile.lock
--rw-r--r--   0        0        0     5078 2023-05-11 09:44:16.809627 addict-tracking-changes-1.0.1/README.md
--rw-r--r--   0        0        0     1146 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.1/badge_coverage.svg
--rw-r--r--   0        0        0     1177 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.1/badge_flake8.svg
--rw-r--r--   0        0        0     1115 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.1/badge_tests.svg
--rw-r--r--   0        0        0      634 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.1/docs/Makefile
--rw-r--r--   0        0        0     5873 2023-05-11 09:44:16.839627 addict-tracking-changes-1.0.1/docs/addict.rst
--rw-r--r--   0        0        0     1950 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.1/docs/conf.py
--rw-r--r--   0        0        0      503 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.1/docs/index.rst
--rw-r--r--   0        0        0      800 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.1/docs/make.bat
--rw-r--r--   0        0        0     1116 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.1/docs/usage.rst
--rw-r--r--   0        0        0      408 2023-05-11 09:44:16.789627 addict-tracking-changes-1.0.1/mkdocs.yml
--rw-r--r--   0        0        0     3544 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.1/noxfile.py
--rw-r--r--   0        0        0      795 2023-05-11 12:39:05.765919 addict-tracking-changes-1.0.1/pyproject.toml
--rw-r--r--   0        0        0     2245 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/back.svg
--rw-r--r--   0        0        0     2666 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/file.svg
--rw-r--r--   0        0        0     7400 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/flake8stats.txt
--rw-r--r--   0        0        0     1109 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/index.html
--rw-r--r--   0        0        0     3669 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/src.addict_tracking_changes.__init__.report.html
--rw-r--r--   0        0        0     8223 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/src.addict_tracking_changes.__init__.source.html
--rw-r--r--   0        0        0     2999 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/src.addict_tracking_changes.addict.report.html
--rw-r--r--   0        0        0    89377 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/src.addict_tracking_changes.addict.source.html
--rw-r--r--   0        0        0     7273 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/flake8/styles.css
--rw-r--r--   0        0        0     4565 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/reports/junit/junit.xml
--rw-r--r--   0        0        0     1471 2023-05-11 12:41:51.084309 addict-tracking-changes-1.0.1/src/addict_tracking_changes/__init__.py
--rw-r--r--   0        0        0    13290 2023-05-11 09:44:16.849627 addict-tracking-changes-1.0.1/src/addict_tracking_changes/addict.py
--rw-r--r--   0        0        0     1115 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.1/tests-badge.svg
--rw-r--r--   0        0        0    14497 2023-05-11 09:44:16.849627 addict-tracking-changes-1.0.1/tests/addict_test.py
--rw-r--r--   0        0        0     5603 1970-01-01 00:00:00.000000 addict-tracking-changes-1.0.1/PKG-INFO
+-rw-r--r--   0        0        0      141 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.2/.flake8
+-rw-r--r--   0        0        0     1886 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.2/.gitignore
+-rw-r--r--   0        0        0     1070 2022-11-29 03:20:21.000000 addict-tracking-changes-1.0.2/LICENSE
+-rw-r--r--   0        0        0      325 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.2/Pipfile
+-rw-r--r--   0        0        0    41152 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.2/Pipfile.lock
+-rw-r--r--   0        0        0     6182 2023-05-11 13:17:50.831187 addict-tracking-changes-1.0.2/README.md
+-rw-r--r--   0        0        0     1146 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.2/badge_coverage.svg
+-rw-r--r--   0        0        0     1177 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.2/badge_flake8.svg
+-rw-r--r--   0        0        0     1115 2023-05-11 09:44:16.859627 addict-tracking-changes-1.0.2/badge_tests.svg
+-rw-r--r--   0        0        0      634 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.2/docs/Makefile
+-rw-r--r--   0        0        0     5873 2023-05-11 09:44:16.839627 addict-tracking-changes-1.0.2/docs/addict.rst
+-rw-r--r--   0        0        0     1950 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.2/docs/conf.py
+-rw-r--r--   0        0        0      503 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.2/docs/index.rst
+-rw-r--r--   0        0        0      800 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.2/docs/make.bat
+-rw-r--r--   0        0        0     1116 2023-05-11 09:44:16.829627 addict-tracking-changes-1.0.2/docs/usage.rst
+-rw-r--r--   0        0        0      408 2023-05-11 09:44:16.789627 addict-tracking-changes-1.0.2/mkdocs.yml
+-rw-r--r--   0        0        0     3543 2023-05-11 13:19:16.630269 addict-tracking-changes-1.0.2/noxfile.py
+-rw-r--r--   0        0        0      831 2023-05-13 11:07:15.770065 addict-tracking-changes-1.0.2/pyproject.toml
+-rw-r--r--   0        0        0     2245 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/back.svg
+-rw-r--r--   0        0        0     2666 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/file.svg
+-rw-r--r--   0        0        0     7400 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/flake8stats.txt
+-rw-r--r--   0        0        0     1109 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/index.html
+-rw-r--r--   0        0        0     3669 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/src.addict_tracking_changes.__init__.report.html
+-rw-r--r--   0        0        0     8223 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/src.addict_tracking_changes.__init__.source.html
+-rw-r--r--   0        0        0     2999 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/src.addict_tracking_changes.addict.report.html
+-rw-r--r--   0        0        0    89377 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/src.addict_tracking_changes.addict.source.html
+-rw-r--r--   0        0        0     7273 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/flake8/styles.css
+-rw-r--r--   0        0        0     4565 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/reports/junit/junit.xml
+-rw-r--r--   0        0        0     1471 2023-05-13 11:07:33.399908 addict-tracking-changes-1.0.2/src/addict_tracking_changes/__init__.py
+-rw-r--r--   0        0        0    13290 2023-05-11 09:44:16.849627 addict-tracking-changes-1.0.2/src/addict_tracking_changes/addict.py
+-rw-r--r--   0        0        0     1115 2023-05-11 09:44:16.869627 addict-tracking-changes-1.0.2/tests-badge.svg
+-rw-r--r--   0        0        0    14497 2023-05-11 09:44:16.849627 addict-tracking-changes-1.0.2/tests/addict_test.py
+-rw-r--r--   0        0        0     6728 1970-01-01 00:00:00.000000 addict-tracking-changes-1.0.2/PKG-INFO
```

### Comparing `addict-tracking-changes-1.0.1/.gitignore` & `addict-tracking-changes-1.0.2/.gitignore`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/LICENSE` & `addict-tracking-changes-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/Pipfile.lock` & `addict-tracking-changes-1.0.2/Pipfile.lock`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/badge_coverage.svg` & `addict-tracking-changes-1.0.2/badge_coverage.svg`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/badge_flake8.svg` & `addict-tracking-changes-1.0.2/badge_flake8.svg`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/badge_tests.svg` & `addict-tracking-changes-1.0.2/badge_tests.svg`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/docs/Makefile` & `addict-tracking-changes-1.0.2/docs/Makefile`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/docs/addict.rst` & `addict-tracking-changes-1.0.2/docs/addict.rst`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/docs/conf.py` & `addict-tracking-changes-1.0.2/docs/conf.py`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/docs/make.bat` & `addict-tracking-changes-1.0.2/docs/make.bat`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/docs/usage.rst` & `addict-tracking-changes-1.0.2/docs/usage.rst`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/noxfile.py` & `addict-tracking-changes-1.0.2/noxfile.py`

 * *Files 0% similar despite different names*

```diff
@@ -63,15 +63,15 @@
     session.install("sphinx", "ghp-import", "git+https://github.com/bashtage/sphinx-material.git")
 
     # Build the documentation
     os.chdir("docs")
     session.run("sphinx-build", "-b", "html", ".", "_build/html")
 
     # Push the documentation to the gh-pages branch
-    #session.run("ghp-import", "-n", "-p", "-f", "_build/html")
+    session.run("ghp-import", "-n", "-p", "-f", "_build/html")
         
 
 
 @nox.session(python="3.11")
 def badges(session):
     # Install pytest, pytest-cov, flake8 and genbadge
     session.install("pytest", "pytest-cov", "flake8", "flake8-html",   "genbadge[all]")
```

### Comparing `addict-tracking-changes-1.0.1/pyproject.toml` & `addict-tracking-changes-1.0.2/pyproject.toml`

 * *Files 23% similar despite different names*

```diff
@@ -10,15 +10,17 @@
 maintainers = [
  { name="Kabira K", email= "kabira@monallabs.in"}
 ]
 readme= "README.md"
 license = { file="LICENSE" }
 dynamic = ["version", "description"]
 requires-python = ">3.11"
-
+dependencies = [
+ 	       'dpath',
+]
 
 [tool.hatch.version]
 path = "src/addict_tracking_changes/__init__.py"
 
 [project.urls]
 Home = "https://webworks.monallabs.in/ofjustpy/addict-tracking-changes"
 Documentation = "https://ofjustpy.github.io/addict-tracking-changes/"
```

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/back.svg` & `addict-tracking-changes-1.0.2/reports/flake8/back.svg`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/file.svg` & `addict-tracking-changes-1.0.2/reports/flake8/file.svg`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/flake8stats.txt` & `addict-tracking-changes-1.0.2/reports/flake8/flake8stats.txt`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/index.html` & `addict-tracking-changes-1.0.2/reports/flake8/index.html`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/src.addict_tracking_changes.__init__.report.html` & `addict-tracking-changes-1.0.2/reports/flake8/src.addict_tracking_changes.__init__.report.html`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/src.addict_tracking_changes.__init__.source.html` & `addict-tracking-changes-1.0.2/reports/flake8/src.addict_tracking_changes.__init__.source.html`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/src.addict_tracking_changes.addict.report.html` & `addict-tracking-changes-1.0.2/reports/flake8/src.addict_tracking_changes.addict.report.html`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/src.addict_tracking_changes.addict.source.html` & `addict-tracking-changes-1.0.2/reports/flake8/src.addict_tracking_changes.addict.source.html`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/flake8/styles.css` & `addict-tracking-changes-1.0.2/reports/flake8/styles.css`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/reports/junit/junit.xml` & `addict-tracking-changes-1.0.2/reports/junit/junit.xml`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/src/addict_tracking_changes/__init__.py` & `addict-tracking-changes-1.0.2/src/addict_tracking_changes/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -32,8 +32,8 @@
 """
 
 from .addict import Dict
 from .addict import Dict as Addict
 from .addict import walker
 
 
-__version__ = "1.0.1"
+__version__ = "1.0.2"
```

### Comparing `addict-tracking-changes-1.0.1/src/addict_tracking_changes/addict.py` & `addict-tracking-changes-1.0.2/src/addict_tracking_changes/addict.py`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/tests-badge.svg` & `addict-tracking-changes-1.0.2/tests-badge.svg`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/tests/addict_test.py` & `addict-tracking-changes-1.0.2/tests/addict_test.py`

 * *Files identical despite different names*

### Comparing `addict-tracking-changes-1.0.1/PKG-INFO` & `addict-tracking-changes-1.0.2/README.md`

 * *Files 17% similar despite different names*

```diff
@@ -1,20 +1,22 @@
-Metadata-Version: 2.1
-Name: addict-tracking-changes
-Version: 1.0.1
-Summary: Addict dictionary enhanced with ability to track changes -- currently only supports field additions
-Maintainer-email: Kabira K <kabira@monallabs.in>
-Requires-Python: >3.11
-Description-Content-Type: text/markdown
-Project-URL: Documentation, https://ofjustpy.github.io/addict-tracking-changes/
-Project-URL: Home, https://webworks.monallabs.in/ofjustpy/addict-tracking-changes
-Project-URL: Source, https://github.com/ofjustpy/addict-tracking-changes
-
 # [addict-tracking-changes](https://github.com/Monallabs-org/addict-tracking-changes)
 
+
+[![Python versions](https://img.shields.io/badge/Python-3.11-green)](https://pypi.python.org/pypi/addict-tracking-changes)
+[![Tests Status](https://github.com/ofjustpy/addict-tracking-changes/blob/main/badge_tests.svg)](https://github.com/ofjustpy/addict-tracking-changes/actions)
+[![Coverage Status](https://github.com/ofjustpy/addict-tracking-changes/blob/main/badge_coverage.svg)](https://github.com/ofjustpy/addict-tracking-changes/actions)
+[![Flake8 Status](https://github.com/ofjustpy/addict-tracking-changes/blob/main/badge_flake8.svg)](https://github.com/ofjustpy/addict-tracking-changes/actions)
+
+[![Documentation](https://img.shields.io/badge/doc-latest-blue.svg)](https://ofjustpy.github.io/addict-tracking-changes/)
+[![PyPI](https://img.shields.io/pypi/v/addict-tracking-changes.svg)](https://pypi.python.org/pypi/addict-tracking-changes)
+[![Downloads](https://pepy.tech/badge/addict-tracking-changes)](https://pepy.tech/project/addict-tracking-changes)
+[![Downloads per week](https://pepy.tech/badge/addict-tracking-changes/week)](https://pepy.tech/project/addict-tracking-changes)
+[![GitHub stars](https://img.shields.io/github/stars/ofjustpy/addict-tracking-changes.svg)](https://github.com/ofjustpy/addict-tracking-changes/stargazers)
+
+
 ## Introduction
 
 Originally, this repository was a fork of [addict](https://github.com/mewwts/addict) by Mats Julian Olsen.
 Overtime, it has substatially diverged in functionality and codebase that it seemed to make
 sense to breakout as its own repository. 
 
 The original addict:  provides an alternative and succient interface to manipulate a dictionary. This is especially
@@ -137,25 +139,24 @@
     x = pickle.load(fh)
 for _ in oj.dictWalker(x):
     oj.dnew(cjs_cfg, _[0], _[1])
 
 ```
 
 ## APIs
-| API                                                    | Description                                           |
-|--------------------------------------------------------+-------------------------------------------------------|
-| Dict(*args, **kwargs)                                  | Initializes a new Dict object                         |
-| to_dict(self)                                          | Converts the Dict object to a regular dictionary      |
-| freeze(self, shouldFreeze=True)                        | Freezes the Dict object, making it immutable          |
-| unfreeze(self)                                         | Unfreezes the Dict object, making it mutable again    |
-| get_changed_history(self, prefix="", path_guards=None) | Returns an iterator with the changed history of keys  |
-| clear_changed_history(self)                            | Clears the changed history of the Dict object         |
-| set_tracker(self, track_changes=False)                 | Sets or resets the change tracker for the Dict object |
-|--------------------------------------------------------+-------------------------------------------------------|
+| API                                                  | Description                                        |
+|------------------------------------------------------|----------------------------------------------------|
+| `Dict(*args, **kwargs)`                              | Initializes a new Dict object                      |
+| `to_dict(self)`                                      | Converts the Dict object to a regular dictionary   |
+| `freeze(self, shouldFreeze=True)`                    | Freezes the Dict object, making it immutable       |
+| `unfreeze(self)`                                     | Unfreezes the Dict object, making it mutable again |
+| `get_changed_history(self, prefix="", path_guards=None)` | Returns an iterator with the changed history of keys |
+| `clear_changed_history(self)`                        | Clears the changed history of the Dict object      |
+| `set_tracker(self, track_changes=False)`             | Sets or resets the change tracker for the Dict object |
+
 
 
 ### EndNotes
 - Docs (in readthedocs format): https://monallabs-org.github.io/addict-tracking-changes/#introduction, https://webworks.monallabs.in/addict-tracking-changes
 
 - Developed By: webworks.monallabs.in
 
-
```

