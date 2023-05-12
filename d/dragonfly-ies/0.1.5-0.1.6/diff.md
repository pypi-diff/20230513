# Comparing `tmp/dragonfly-ies-0.1.5.tar.gz` & `tmp/dragonfly-ies-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/dragonfly-ies-0.1.5.tar", last modified: Fri Oct 28 23:00:29 2022, max compression
+gzip compressed data, was "dist/dragonfly-ies-0.1.6.tar", last modified: Fri May 12 23:03:11 2023, max compression
```

## Comparing `dragonfly-ies-0.1.5.tar` & `dragonfly-ies-0.1.6.tar`

### file list

```diff
@@ -1,57 +1,57 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/.github/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (121)     2808 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/.github/workflows/ci.yaml
--rw-r--r--   0 runner    (1001) docker     (121)      142 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/.gitignore
--rw-r--r--   0 runner    (1001) docker     (121)      294 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/.releaserc.json
--rw-r--r--   0 runner    (1001) docker     (121)      279 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/CODE_OF_CONDUCT.md
--rw-r--r--   0 runner    (1001) docker     (121)      445 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (121)    34523 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)     1608 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     1026 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/README.md
--rw-r--r--   0 runner    (1001) docker     (121)      165 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/deploy.sh
--rw-r--r--   0 runner    (1001) docker     (121)      245 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/dev-requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/docs/
--rw-r--r--   0 runner    (1001) docker     (121)      362 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/docs/_build/
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/_build/.nojekyll
--rw-r--r--   0 runner    (1001) docker     (121)       16 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/_build/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/docs/_build/docs/
--rw-r--r--   0 runner    (1001) docker     (121)       16 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/_build/docs/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (121)      899 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/_static/custom.css
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/docs/_templates/
--rw-r--r--   0 runner    (1001) docker     (121)     3668 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/_templates/layout.html
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/docs/cli/
--rw-r--r--   0 runner    (1001) docker     (121)      127 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/cli/index.rst
--rw-r--r--   0 runner    (1001) docker     (121)    21479 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (121)      391 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (121)       80 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/docs/modules.rst
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies/
--rw-r--r--   0 runner    (1001) docker     (121)       69 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/dragonfly_ies/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)       73 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/dragonfly_ies/__main__.py
--rw-r--r--   0 runner    (1001) docker     (121)       70 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/dragonfly_ies/_extend_dragonfly.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies/cli/
--rw-r--r--   0 runner    (1001) docker     (121)      394 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/dragonfly_ies/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1761 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/dragonfly_ies/cli/translate.py
--rw-r--r--   0 runner    (1001) docker     (121)     1099 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/dragonfly_ies/writer.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     1608 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      975 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       57 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (121)       44 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       14 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/dragonfly_ies.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       44 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)      102 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1045 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/tests/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/tests/assets/
--rw-r--r--   0 runner    (1001) docker     (121)  1974885 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/tests/assets/model_invalid_adj.dfjson
--rw-r--r--   0 runner    (1001) docker     (121)   129414 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/tests/assets/simple_model.dfjson
--rw-r--r--   0 runner    (1001) docker     (121)   293668 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/tests/assets/university_campus.dfjson
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 23:00:29.000000 dragonfly-ies-0.1.5/tests/cli/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/tests/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      999 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/tests/cli/translate_cli_test.py
--rw-r--r--   0 runner    (1001) docker     (121)      354 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/tests/extend_test.py
--rw-r--r--   0 runner    (1001) docker     (121)      412 2022-10-28 22:59:12.000000 dragonfly-ies-0.1.5/tests/writer_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     2808 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/.github/workflows/ci.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      142 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      294 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/.releaserc.json
+-rw-r--r--   0 runner    (1001) docker     (123)      279 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/CODE_OF_CONDUCT.md
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)    34523 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1608 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1026 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      165 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/deploy.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      245 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/dev-requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/docs/_build/
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/_build/.nojekyll
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/_build/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/docs/_build/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/_build/docs/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)      899 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/_static/custom.css
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/docs/_templates/
+-rw-r--r--   0 runner    (1001) docker     (123)     3668 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/_templates/layout.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/docs/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/cli/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    21479 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      391 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/docs/modules.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/dragonfly_ies/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/dragonfly_ies/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/dragonfly_ies/_extend_dragonfly.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)      394 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/dragonfly_ies/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1761 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/dragonfly_ies/cli/translate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1099 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/dragonfly_ies/writer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1608 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       57 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       43 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/dragonfly_ies.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       43 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1045 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/tests/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/tests/assets/
+-rw-r--r--   0 runner    (1001) docker     (123)  1974885 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/tests/assets/model_invalid_adj.dfjson
+-rw-r--r--   0 runner    (1001) docker     (123)   129414 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/tests/assets/simple_model.dfjson
+-rw-r--r--   0 runner    (1001) docker     (123)   293668 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/tests/assets/university_campus.dfjson
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:03:11.000000 dragonfly-ies-0.1.6/tests/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/tests/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      999 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/tests/cli/translate_cli_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      354 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/tests/extend_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      412 2023-05-12 23:02:11.000000 dragonfly-ies-0.1.6/tests/writer_test.py
```

### Comparing `dragonfly-ies-0.1.5/.github/workflows/ci.yaml` & `dragonfly-ies-0.1.6/.github/workflows/ci.yaml`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/LICENSE` & `dragonfly-ies-0.1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/PKG-INFO` & `dragonfly-ies-0.1.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dragonfly-ies
-Version: 0.1.5
+Version: 0.1.6
 Summary: Dragonfly extension for export to IES-VE GEM file format
 Home-page: https://github.com/ladybug-tools/dragonfly-ies
 Author: Ladybug Tools
 Author-email: info@ladybug.tools
 License: AGPL-3.0
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `dragonfly-ies-0.1.5/README.md` & `dragonfly-ies-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/docs/_static/custom.css` & `dragonfly-ies-0.1.6/docs/_static/custom.css`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/docs/_templates/layout.html` & `dragonfly-ies-0.1.6/docs/_templates/layout.html`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/docs/conf.py` & `dragonfly-ies-0.1.6/docs/conf.py`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/dragonfly_ies/cli/translate.py` & `dragonfly-ies-0.1.6/dragonfly_ies/cli/translate.py`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/dragonfly_ies/writer.py` & `dragonfly-ies-0.1.6/dragonfly_ies/writer.py`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/dragonfly_ies.egg-info/PKG-INFO` & `dragonfly-ies-0.1.6/dragonfly_ies.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dragonfly-ies
-Version: 0.1.5
+Version: 0.1.6
 Summary: Dragonfly extension for export to IES-VE GEM file format
 Home-page: https://github.com/ladybug-tools/dragonfly-ies
 Author: Ladybug Tools
 Author-email: info@ladybug.tools
 License: AGPL-3.0
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `dragonfly-ies-0.1.5/dragonfly_ies.egg-info/SOURCES.txt` & `dragonfly-ies-0.1.6/dragonfly_ies.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/setup.py` & `dragonfly-ies-0.1.6/setup.py`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/tests/assets/model_invalid_adj.dfjson` & `dragonfly-ies-0.1.6/tests/assets/model_invalid_adj.dfjson`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/tests/assets/simple_model.dfjson` & `dragonfly-ies-0.1.6/tests/assets/simple_model.dfjson`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/tests/assets/university_campus.dfjson` & `dragonfly-ies-0.1.6/tests/assets/university_campus.dfjson`

 * *Files identical despite different names*

### Comparing `dragonfly-ies-0.1.5/tests/cli/translate_cli_test.py` & `dragonfly-ies-0.1.6/tests/cli/translate_cli_test.py`

 * *Files identical despite different names*

