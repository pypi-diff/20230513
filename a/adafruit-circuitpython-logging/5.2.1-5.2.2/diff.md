# Comparing `tmp/adafruit-circuitpython-logging-5.2.1.tar.gz` & `tmp/adafruit-circuitpython-logging-5.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "adafruit-circuitpython-logging-5.2.1.tar", last modified: Fri Jan  6 00:12:20 2023, max compression
+gzip compressed data, was "adafruit-circuitpython-logging-5.2.2.tar", last modified: Fri May 12 22:45:12 2023, max compression
```

## Comparing `adafruit-circuitpython-logging-5.2.1.tar` & `adafruit-circuitpython-logging-5.2.2.tar`

### file list

```diff
@@ -1,49 +1,49 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.728186 adafruit-circuitpython-logging-5.2.1/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.716186 adafruit-circuitpython-logging-5.2.1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.724186 adafruit-circuitpython-logging-5.2.1/.github/PULL_REQUEST_TEMPLATE/
--rw-r--r--   0 runner    (1001) docker     (123)      880 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.724186 adafruit-circuitpython-logging-5.2.1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      303 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.github/workflows/build.yml
--rw-r--r--   0 runner    (1001) docker     (123)      479 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.github/workflows/failure-help-text.yml
--rw-r--r--   0 runner    (1001) docker     (123)      423 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.github/workflows/release_gh.yml
--rw-r--r--   0 runner    (1001) docker     (123)      475 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.github/workflows/release_pypi.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1654 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1239 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    13069 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.pylintrc
--rw-r--r--   0 runner    (1001) docker     (123)      388 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/.readthedocs.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     6147 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/CODE_OF_CONDUCT.md
--rw-r--r--   0 runner    (1001) docker     (123)     1102 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/LICENSE
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.724186 adafruit-circuitpython-logging-5.2.1/LICENSES/
--rw-r--r--   0 runner    (1001) docker     (123)    16814 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/LICENSES/CC-BY-4.0.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1108 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/LICENSES/MIT.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/LICENSES/Unlicense.txt
--rw-r--r--   0 runner    (1001) docker     (123)     2678 2023-01-06 00:12:20.728186 adafruit-circuitpython-logging-5.2.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1952 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/README.rst
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/README.rst.license
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.728186 adafruit-circuitpython-logging-5.2.1/adafruit_circuitpython_logging.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2678 2023-01-06 00:12:20.000000 adafruit-circuitpython-logging-5.2.1/adafruit_circuitpython_logging.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1029 2023-01-06 00:12:20.000000 adafruit-circuitpython-logging-5.2.1/adafruit_circuitpython_logging.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-01-06 00:12:20.000000 adafruit-circuitpython-logging-5.2.1/adafruit_circuitpython_logging.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       46 2023-01-06 00:12:20.000000 adafruit-circuitpython-logging-5.2.1/adafruit_circuitpython_logging.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-01-06 00:12:20.000000 adafruit-circuitpython-logging-5.2.1/adafruit_circuitpython_logging.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)    12221 2023-01-06 00:12:10.000000 adafruit-circuitpython-logging-5.2.1/adafruit_logging.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.728186 adafruit-circuitpython-logging-5.2.1/docs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.728186 adafruit-circuitpython-logging-5.2.1/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (123)     4414 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/_static/favicon.ico
--rw-r--r--   0 runner    (1001) docker     (123)      105 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/_static/favicon.ico.license
--rw-r--r--   0 runner    (1001) docker     (123)      266 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/api.rst
--rw-r--r--   0 runner    (1001) docker     (123)       96 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/api.rst.license
--rw-r--r--   0 runner    (1001) docker     (123)     5639 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      188 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/examples.rst
--rw-r--r--   0 runner    (1001) docker     (123)       96 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/examples.rst.license
--rw-r--r--   0 runner    (1001) docker     (123)      971 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)       96 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/index.rst.license
--rw-r--r--   0 runner    (1001) docker     (123)      123 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 00:12:20.728186 adafruit-circuitpython-logging-5.2.1/examples/
--rw-r--r--   0 runner    (1001) docker     (123)      934 2023-01-06 00:12:10.000000 adafruit-circuitpython-logging-5.2.1/examples/logging_filehandler.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2449 2023-01-06 00:12:10.000000 adafruit-circuitpython-logging-5.2.1/examples/logging_mqtt_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)     1210 2023-01-06 00:12:10.000000 adafruit-circuitpython-logging-5.2.1/examples/logging_simpletest.py
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/optional_requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-01-06 00:12:10.000000 adafruit-circuitpython-logging-5.2.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      143 2023-01-06 00:12:00.000000 adafruit-circuitpython-logging-5.2.1/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-01-06 00:12:20.728186 adafruit-circuitpython-logging-5.2.1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.802101 adafruit-circuitpython-logging-5.2.2/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.794101 adafruit-circuitpython-logging-5.2.2/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.798101 adafruit-circuitpython-logging-5.2.2/.github/PULL_REQUEST_TEMPLATE/
+-rw-r--r--   0 runner    (1001) docker     (123)      880 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.798101 adafruit-circuitpython-logging-5.2.2/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      303 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.github/workflows/build.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      479 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.github/workflows/failure-help-text.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      482 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.github/workflows/release_gh.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      475 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.github/workflows/release_pypi.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1654 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1238 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    13069 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.pylintrc
+-rw-r--r--   0 runner    (1001) docker     (123)      388 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/.readthedocs.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     6147 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/CODE_OF_CONDUCT.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1102 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/LICENSE
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.798101 adafruit-circuitpython-logging-5.2.2/LICENSES/
+-rw-r--r--   0 runner    (1001) docker     (123)    16814 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/LICENSES/CC-BY-4.0.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1108 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/LICENSES/MIT.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/LICENSES/Unlicense.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2678 2023-05-12 22:45:12.802101 adafruit-circuitpython-logging-5.2.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1952 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/README.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/README.rst.license
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.798101 adafruit-circuitpython-logging-5.2.2/adafruit_circuitpython_logging.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2678 2023-05-12 22:45:12.000000 adafruit-circuitpython-logging-5.2.2/adafruit_circuitpython_logging.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1029 2023-05-12 22:45:12.000000 adafruit-circuitpython-logging-5.2.2/adafruit_circuitpython_logging.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:45:12.000000 adafruit-circuitpython-logging-5.2.2/adafruit_circuitpython_logging.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       46 2023-05-12 22:45:12.000000 adafruit-circuitpython-logging-5.2.2/adafruit_circuitpython_logging.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-12 22:45:12.000000 adafruit-circuitpython-logging-5.2.2/adafruit_circuitpython_logging.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    12262 2023-05-12 22:45:03.000000 adafruit-circuitpython-logging-5.2.2/adafruit_logging.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.798101 adafruit-circuitpython-logging-5.2.2/docs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.802101 adafruit-circuitpython-logging-5.2.2/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)     4414 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/_static/favicon.ico
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/_static/favicon.ico.license
+-rw-r--r--   0 runner    (1001) docker     (123)      266 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/api.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       96 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/api.rst.license
+-rw-r--r--   0 runner    (1001) docker     (123)     5639 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      188 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/examples.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       96 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/examples.rst.license
+-rw-r--r--   0 runner    (1001) docker     (123)      971 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       96 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/index.rst.license
+-rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/docs/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:45:12.802101 adafruit-circuitpython-logging-5.2.2/examples/
+-rw-r--r--   0 runner    (1001) docker     (123)      934 2023-05-12 22:45:03.000000 adafruit-circuitpython-logging-5.2.2/examples/logging_filehandler.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2449 2023-05-12 22:45:03.000000 adafruit-circuitpython-logging-5.2.2/examples/logging_mqtt_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1210 2023-05-12 22:45:03.000000 adafruit-circuitpython-logging-5.2.2/examples/logging_simpletest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/optional_requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-05-12 22:45:03.000000 adafruit-circuitpython-logging-5.2.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-05-12 22:44:52.000000 adafruit-circuitpython-logging-5.2.2/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 22:45:12.802101 adafruit-circuitpython-logging-5.2.2/setup.cfg
```

### Comparing `adafruit-circuitpython-logging-5.2.1/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md` & `adafruit-circuitpython-logging-5.2.2/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/.gitignore` & `adafruit-circuitpython-logging-5.2.2/.gitignore`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/.pre-commit-config.yaml` & `adafruit-circuitpython-logging-5.2.2/.pre-commit-config.yaml`

 * *Files 3% similar despite different names*

```diff
@@ -1,28 +1,28 @@
 # SPDX-FileCopyrightText: 2020 Diego Elio Pettenò
 #
 # SPDX-License-Identifier: Unlicense
 
 repos:
   - repo: https://github.com/python/black
-    rev: 22.3.0
+    rev: 23.3.0
     hooks:
       - id: black
   - repo: https://github.com/fsfe/reuse-tool
-    rev: v0.14.0
+    rev: v1.1.2
     hooks:
       - id: reuse
   - repo: https://github.com/pre-commit/pre-commit-hooks
-    rev: v4.2.0
+    rev: v4.4.0
     hooks:
       - id: check-yaml
       - id: end-of-file-fixer
       - id: trailing-whitespace
   - repo: https://github.com/pycqa/pylint
-    rev: v2.15.5
+    rev: v2.17.4
     hooks:
       - id: pylint
         name: pylint (library code)
         types: [python]
         args:
           - --disable=consider-using-f-string
         exclude: "^(docs/|examples/|tests/|setup.py$)"
```

### Comparing `adafruit-circuitpython-logging-5.2.1/.pylintrc` & `adafruit-circuitpython-logging-5.2.2/.pylintrc`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/CODE_OF_CONDUCT.md` & `adafruit-circuitpython-logging-5.2.2/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/LICENSE` & `adafruit-circuitpython-logging-5.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/LICENSES/CC-BY-4.0.txt` & `adafruit-circuitpython-logging-5.2.2/LICENSES/CC-BY-4.0.txt`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/LICENSES/MIT.txt` & `adafruit-circuitpython-logging-5.2.2/LICENSES/MIT.txt`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/LICENSES/Unlicense.txt` & `adafruit-circuitpython-logging-5.2.2/LICENSES/Unlicense.txt`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/PKG-INFO` & `adafruit-circuitpython-logging-5.2.2/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: adafruit-circuitpython-logging
-Version: 5.2.1
+Version: 5.2.2
 Summary: Logging module for CircuitPython
 Author-email: Adafruit Industries <circuitpython@adafruit.com>
 License: MIT
 Project-URL: Homepage, https://github.com/adafruit/Adafruit_CircuitPython_Logging
 Keywords: adafruit,blinka,circuitpython,micropython,logging,logger
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Libraries
```

### Comparing `adafruit-circuitpython-logging-5.2.1/README.rst` & `adafruit-circuitpython-logging-5.2.2/README.rst`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/adafruit_circuitpython_logging.egg-info/PKG-INFO` & `adafruit-circuitpython-logging-5.2.2/adafruit_circuitpython_logging.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: adafruit-circuitpython-logging
-Version: 5.2.1
+Version: 5.2.2
 Summary: Logging module for CircuitPython
 Author-email: Adafruit Industries <circuitpython@adafruit.com>
 License: MIT
 Project-URL: Homepage, https://github.com/adafruit/Adafruit_CircuitPython_Logging
 Keywords: adafruit,blinka,circuitpython,micropython,logging,logger
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Libraries
```

### Comparing `adafruit-circuitpython-logging-5.2.1/adafruit_circuitpython_logging.egg-info/SOURCES.txt` & `adafruit-circuitpython-logging-5.2.2/adafruit_circuitpython_logging.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/adafruit_logging.py` & `adafruit-circuitpython-logging-5.2.2/adafruit_logging.py`

 * *Files 0% similar despite different names*

```diff
@@ -72,15 +72,15 @@
 
             :param str buf: The string data to write to the stream
             """
 
 except ImportError:
     pass
 
-__version__ = "5.2.1"
+__version__ = "5.2.2"
 __repo__ = "https://github.com/adafruit/Adafruit_CircuitPython_Logger.git"
 
 # pylint:disable=undefined-all-variable
 __all__ = [
     "LEVELS",
     "NOTSET",
     "DEBUG",
@@ -320,15 +320,17 @@
         self._handlers.remove(hdlr)
 
     def hasHandlers(self) -> bool:
         """Whether any handlers have been set for this logger"""
         return len(self._handlers) > 0
 
     def _log(self, level: int, msg: str, *args) -> None:
-        record = _logRecordFactory(self.name, level, msg % args, args)
+        record = _logRecordFactory(
+            self.name, level, (msg % args) if args else msg, args
+        )
         self.handle(record)
 
     def handle(self, record: LogRecord) -> None:
         """Pass the record to all handlers registered with this logger.
 
         :param LogRecord record: log record
         """
```

### Comparing `adafruit-circuitpython-logging-5.2.1/docs/_static/favicon.ico` & `adafruit-circuitpython-logging-5.2.2/docs/_static/favicon.ico`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/docs/conf.py` & `adafruit-circuitpython-logging-5.2.2/docs/conf.py`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/docs/index.rst` & `adafruit-circuitpython-logging-5.2.2/docs/index.rst`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/examples/logging_filehandler.py` & `adafruit-circuitpython-logging-5.2.2/examples/logging_filehandler.py`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/examples/logging_mqtt_handler.py` & `adafruit-circuitpython-logging-5.2.2/examples/logging_mqtt_handler.py`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/examples/logging_simpletest.py` & `adafruit-circuitpython-logging-5.2.2/examples/logging_simpletest.py`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-logging-5.2.1/pyproject.toml` & `adafruit-circuitpython-logging-5.2.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -8,15 +8,15 @@
     "wheel",
     "setuptools-scm",
 ]
 
 [project]
 name = "adafruit-circuitpython-logging"
 description = "Logging module for CircuitPython"
-version = "5.2.1"
+version = "5.2.2"
 readme = "README.rst"
 authors = [
     {name = "Adafruit Industries", email = "circuitpython@adafruit.com"}
 ]
 urls = {Homepage = "https://github.com/adafruit/Adafruit_CircuitPython_Logging"}
 keywords = [
     "adafruit",
```

