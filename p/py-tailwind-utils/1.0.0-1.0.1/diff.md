# Comparing `tmp/py-tailwind-utils-1.0.0.tar.gz` & `tmp/py-tailwind-utils-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "py-tailwind-utils-1.0.0.tar", last modified: Sat May 13 08:19:42 2023, max compression
+gzip compressed data, was "py-tailwind-utils-1.0.1.tar", last modified: Sat May 13 10:51:37 2023, max compression
```

## Comparing `py-tailwind-utils-1.0.0.tar` & `py-tailwind-utils-1.0.1.tar`

### file list

```diff
@@ -1,34 +1,35 @@
--rw-r--r--   0        0        0      166 2023-05-12 14:37:16.471746 py-tailwind-utils-1.0.0/.flake8
--rw-r--r--   0        0        0     1874 2023-05-13 08:11:47.999782 py-tailwind-utils-1.0.0/.gitignore
--rw-r--r--   0        0        0     1070 2022-11-28 15:32:19.000000 py-tailwind-utils-1.0.0/LICENSE
--rw-r--r--   0        0        0      181 2023-05-13 02:30:54.356459 py-tailwind-utils-1.0.0/Pipfile
--rw-r--r--   0        0        0     1192 2023-05-13 02:30:58.126418 py-tailwind-utils-1.0.0/Pipfile.lock
--rw-r--r--   0        0        0    48228 2023-05-13 03:59:48.179237 py-tailwind-utils-1.0.0/README.md
--rw-r--r--   0        0        0     1149 2023-05-13 04:01:15.828338 py-tailwind-utils-1.0.0/badge_coverage.svg
--rw-r--r--   0        0        0     1173 2023-05-13 04:01:17.458322 py-tailwind-utils-1.0.0/badge_flake8.svg
--rw-r--r--   0        0        0     1119 2023-05-13 04:01:14.688350 py-tailwind-utils-1.0.0/badge_tests.svg
--rw-r--r--   0        0        0      638 2023-05-12 16:54:44.794438 py-tailwind-utils-1.0.0/docs/Makefile
--rw-r--r--   0        0        0   102288 2023-05-13 08:17:25.786155 py-tailwind-utils-1.0.0/docs/README.rst
--rw-r--r--   0        0        0      929 2023-05-12 16:55:42.903817 py-tailwind-utils-1.0.0/docs/conf.py
--rw-r--r--   0        0        0      476 2023-05-12 17:02:57.439176 py-tailwind-utils-1.0.0/docs/index.rst
--rw-r--r--   0        0        0      804 2023-05-12 16:54:44.794438 py-tailwind-utils-1.0.0/docs/make.bat
--rw-r--r--   0        0        0     3792 2023-05-13 03:58:37.719958 py-tailwind-utils-1.0.0/noxfile.py
--rw-r--r--   0        0        0      777 2023-05-13 08:13:46.798476 py-tailwind-utils-1.0.0/pyproject.toml
--rw-r--r--   0        0        0     5619 2023-05-13 04:01:13.608361 py-tailwind-utils-1.0.0/reports/flake8/flake8stats.txt
--rw-r--r--   0        0        0    32441 2023-05-13 04:01:12.128376 py-tailwind-utils-1.0.0/reports/junit/junit.xml
--rw-r--r--   0        0        0     3710 2023-05-13 04:16:02.419110 py-tailwind-utils-1.0.0/src/py_tailwind_utils/__init__.py
--rw-r--r--   0        0        0     4265 2023-05-13 04:09:55.782912 py-tailwind-utils-1.0.0/src/py_tailwind_utils/colors.py
--rw-r--r--   0        0        0    12014 2023-05-13 04:10:03.122832 py-tailwind-utils-1.0.0/src/py_tailwind_utils/common.py
--rw-r--r--   0        0        0     4865 2023-05-13 04:09:50.512969 py-tailwind-utils-1.0.0/src/py_tailwind_utils/dpathutils.py
--rw-r--r--   0        0        0     2555 2023-05-13 04:09:13.723368 py-tailwind-utils-1.0.0/src/py_tailwind_utils/modifiers.py
--rw-r--r--   0        0        0     6210 2022-11-28 15:33:41.000000 py-tailwind-utils-1.0.0/src/py_tailwind_utils/palette-v2x.json
--rw-r--r--   0        0        0     7083 2023-05-13 04:09:37.343112 py-tailwind-utils-1.0.0/src/py_tailwind_utils/styClause.py
--rw-r--r--   0        0        0     5789 2023-05-12 13:47:05.213962 py-tailwind-utils-1.0.0/src/py_tailwind_utils/style_tags.py
--rw-r--r--   0        0        0    10476 2023-05-13 04:08:17.493978 py-tailwind-utils-1.0.0/src/py_tailwind_utils/style_values.py
--rw-r--r--   0        0        0    20119 2023-05-13 04:09:45.703021 py-tailwind-utils-1.0.0/src/py_tailwind_utils/style_values_noop.py
--rw-r--r--   0        0        0     2420 2023-05-13 04:09:27.333220 py-tailwind-utils-1.0.0/src/py_tailwind_utils/utils.py
--rw-r--r--   0        0        0     1590 2023-05-13 04:08:26.413881 py-tailwind-utils-1.0.0/src/py_tailwind_utils/valuetags.py
--rw-r--r--   0        0        0    10357 2023-05-12 14:36:08.602433 py-tailwind-utils-1.0.0/tests/twtags_test.py
--rw-r--r--   0        0        0   190137 2023-01-27 11:36:15.294837 py-tailwind-utils-1.0.0/utils/tailwind_constructs_for_ofjustpy.png
--rw-r--r--   0        0        0     3859 2023-01-27 11:36:15.294837 py-tailwind-utils-1.0.0/utils/wp.py
--rw-r--r--   0        0        0    48676 1970-01-01 00:00:00.000000 py-tailwind-utils-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0      166 2023-05-12 14:37:16.471746 py-tailwind-utils-1.0.1/.flake8
+-rw-r--r--   0        0        0     1874 2023-05-13 08:11:47.999782 py-tailwind-utils-1.0.1/.gitignore
+-rw-r--r--   0        0        0     1070 2022-11-28 15:32:19.000000 py-tailwind-utils-1.0.1/LICENSE
+-rw-r--r--   0        0        0      181 2023-05-13 02:30:54.356459 py-tailwind-utils-1.0.1/Pipfile
+-rw-r--r--   0        0        0     1192 2023-05-13 02:30:58.126418 py-tailwind-utils-1.0.1/Pipfile.lock
+-rw-r--r--   0        0        0    48228 2023-05-13 03:59:48.179237 py-tailwind-utils-1.0.1/README.md
+-rw-r--r--   0        0        0     1149 2023-05-13 04:01:15.828338 py-tailwind-utils-1.0.1/badge_coverage.svg
+-rw-r--r--   0        0        0     1173 2023-05-13 04:01:17.458322 py-tailwind-utils-1.0.1/badge_flake8.svg
+-rw-r--r--   0        0        0     1119 2023-05-13 04:01:14.688350 py-tailwind-utils-1.0.1/badge_tests.svg
+-rw-r--r--   0        0        0      638 2023-05-12 16:54:44.794438 py-tailwind-utils-1.0.1/docs/Makefile
+-rw-r--r--   0        0        0   102288 2023-05-13 08:17:25.786155 py-tailwind-utils-1.0.1/docs/README.rst
+-rw-r--r--   0        0        0      929 2023-05-12 16:55:42.903817 py-tailwind-utils-1.0.1/docs/conf.py
+-rw-r--r--   0        0        0      476 2023-05-12 17:02:57.439176 py-tailwind-utils-1.0.1/docs/index.rst
+-rw-r--r--   0        0        0      804 2023-05-12 16:54:44.794438 py-tailwind-utils-1.0.1/docs/make.bat
+-rw-r--r--   0        0        0     3791 2023-05-13 10:39:50.376590 py-tailwind-utils-1.0.1/noxfile.py
+-rw-r--r--   0        0        0      777 2023-05-13 08:13:46.798476 py-tailwind-utils-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0     5619 2023-05-13 04:01:13.608361 py-tailwind-utils-1.0.1/reports/flake8/flake8stats.txt
+-rw-r--r--   0        0        0    32441 2023-05-13 04:01:12.128376 py-tailwind-utils-1.0.1/reports/junit/junit.xml
+-rw-r--r--   0        0        0       45 2023-05-13 10:49:37.560340 py-tailwind-utils-1.0.1/requirements.txt
+-rw-r--r--   0        0        0     3710 2023-05-13 10:50:02.520075 py-tailwind-utils-1.0.1/src/py_tailwind_utils/__init__.py
+-rw-r--r--   0        0        0     4265 2023-05-13 04:09:55.782912 py-tailwind-utils-1.0.1/src/py_tailwind_utils/colors.py
+-rw-r--r--   0        0        0    12014 2023-05-13 04:10:03.122832 py-tailwind-utils-1.0.1/src/py_tailwind_utils/common.py
+-rw-r--r--   0        0        0     4865 2023-05-13 04:09:50.512969 py-tailwind-utils-1.0.1/src/py_tailwind_utils/dpathutils.py
+-rw-r--r--   0        0        0     2555 2023-05-13 04:09:13.723368 py-tailwind-utils-1.0.1/src/py_tailwind_utils/modifiers.py
+-rw-r--r--   0        0        0     6210 2022-11-28 15:33:41.000000 py-tailwind-utils-1.0.1/src/py_tailwind_utils/palette-v2x.json
+-rw-r--r--   0        0        0     7083 2023-05-13 04:09:37.343112 py-tailwind-utils-1.0.1/src/py_tailwind_utils/styClause.py
+-rw-r--r--   0        0        0     5789 2023-05-12 13:47:05.213962 py-tailwind-utils-1.0.1/src/py_tailwind_utils/style_tags.py
+-rw-r--r--   0        0        0    10476 2023-05-13 04:08:17.493978 py-tailwind-utils-1.0.1/src/py_tailwind_utils/style_values.py
+-rw-r--r--   0        0        0    20119 2023-05-13 04:09:45.703021 py-tailwind-utils-1.0.1/src/py_tailwind_utils/style_values_noop.py
+-rw-r--r--   0        0        0     2420 2023-05-13 04:09:27.333220 py-tailwind-utils-1.0.1/src/py_tailwind_utils/utils.py
+-rw-r--r--   0        0        0     1590 2023-05-13 04:08:26.413881 py-tailwind-utils-1.0.1/src/py_tailwind_utils/valuetags.py
+-rw-r--r--   0        0        0    10357 2023-05-12 14:36:08.602433 py-tailwind-utils-1.0.1/tests/twtags_test.py
+-rw-r--r--   0        0        0   190137 2023-01-27 11:36:15.294837 py-tailwind-utils-1.0.1/utils/tailwind_constructs_for_ofjustpy.png
+-rw-r--r--   0        0        0     3859 2023-01-27 11:36:15.294837 py-tailwind-utils-1.0.1/utils/wp.py
+-rw-r--r--   0        0        0    48676 1970-01-01 00:00:00.000000 py-tailwind-utils-1.0.1/PKG-INFO
```

### Comparing `py-tailwind-utils-1.0.0/.gitignore` & `py-tailwind-utils-1.0.1/.gitignore`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/LICENSE` & `py-tailwind-utils-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/Pipfile.lock` & `py-tailwind-utils-1.0.1/Pipfile.lock`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/README.md` & `py-tailwind-utils-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/badge_coverage.svg` & `py-tailwind-utils-1.0.1/badge_coverage.svg`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/badge_flake8.svg` & `py-tailwind-utils-1.0.1/badge_flake8.svg`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/badge_tests.svg` & `py-tailwind-utils-1.0.1/badge_tests.svg`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/docs/Makefile` & `py-tailwind-utils-1.0.1/docs/Makefile`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/docs/README.rst` & `py-tailwind-utils-1.0.1/docs/README.rst`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/docs/conf.py` & `py-tailwind-utils-1.0.1/docs/conf.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/docs/make.bat` & `py-tailwind-utils-1.0.1/docs/make.bat`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/noxfile.py` & `py-tailwind-utils-1.0.1/noxfile.py`

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
 
     # we need the dependencies
```

### Comparing `py-tailwind-utils-1.0.0/pyproject.toml` & `py-tailwind-utils-1.0.1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/reports/flake8/flake8stats.txt` & `py-tailwind-utils-1.0.1/reports/flake8/flake8stats.txt`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/reports/junit/junit.xml` & `py-tailwind-utils-1.0.1/reports/junit/junit.xml`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/__init__.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -80,8 +80,8 @@
 from .style_values_noop import TextTransform as tt
 from .style_values_noop import VerticalAlign as va
 from .style_values_noop import Visibility as visibility
 from .style_values_noop import WrapAround as wa
 from .utils import gradient
 from .valuetags import *
 
-__version__ = "1.0.0"
+__version__ = "1.0.1"
```

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/colors.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/colors.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/common.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/common.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/dpathutils.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/dpathutils.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/modifiers.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/modifiers.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/palette-v2x.json` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/palette-v2x.json`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/styClause.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/styClause.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/style_tags.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/style_tags.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/style_values.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/style_values.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/style_values_noop.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/style_values_noop.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/utils.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/utils.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/src/py_tailwind_utils/valuetags.py` & `py-tailwind-utils-1.0.1/src/py_tailwind_utils/valuetags.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/tests/twtags_test.py` & `py-tailwind-utils-1.0.1/tests/twtags_test.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/utils/tailwind_constructs_for_ofjustpy.png` & `py-tailwind-utils-1.0.1/utils/tailwind_constructs_for_ofjustpy.png`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/utils/wp.py` & `py-tailwind-utils-1.0.1/utils/wp.py`

 * *Files identical despite different names*

### Comparing `py-tailwind-utils-1.0.0/PKG-INFO` & `py-tailwind-utils-1.0.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-tailwind-utils
-Version: 1.0.0
+Version: 1.0.1
 Summary: tailwind utility classes as first class python objects
 Maintainer-email: Kabira K <kabira@monallabs.in>
 Description-Content-Type: text/markdown
 Project-URL: Documentation, https://monallabs-org.github.io/py-tailwind-utils
 Project-URL: Home, https://webworks.monallabs.in/ofjustpy/addict-tracking-changes
 Project-URL: Source, https://github.com/monallabs-org/py-tailwind-utils
```

