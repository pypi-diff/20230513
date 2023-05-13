# Comparing `tmp/circuitpython-displayio-listselect-1.0.1.tar.gz` & `tmp/circuitpython-displayio-listselect-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "circuitpython-displayio-listselect-1.0.1.tar", last modified: Mon Apr 10 15:15:51 2023, max compression
+gzip compressed data, was "circuitpython-displayio-listselect-1.0.2.tar", last modified: Sat May 13 14:40:40 2023, max compression
```

## Comparing `circuitpython-displayio-listselect-1.0.1.tar` & `circuitpython-displayio-listselect-1.0.2.tar`

### file list

```diff
@@ -1,50 +1,51 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.649086 circuitpython-displayio-listselect-1.0.1/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.641086 circuitpython-displayio-listselect-1.0.1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.645086 circuitpython-displayio-listselect-1.0.1/.github/PULL_REQUEST_TEMPLATE/
--rw-r--r--   0 runner    (1001) docker     (123)      880 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.645086 circuitpython-displayio-listselect-1.0.1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      303 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.github/workflows/build.yml
--rw-r--r--   0 runner    (1001) docker     (123)      479 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.github/workflows/failure-help-text.yml
--rw-r--r--   0 runner    (1001) docker     (123)      736 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.github/workflows/release_gh.yml
--rw-r--r--   0 runner    (1001) docker     (123)      494 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.github/workflows/release_pypi.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1654 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1239 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    13069 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.pylintrc
--rw-r--r--   0 runner    (1001) docker     (123)      405 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/.readthedocs.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     6717 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/CODE_OF_CONDUCT.md
--rw-r--r--   0 runner    (1001) docker     (123)     1085 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/LICENSE
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.645086 circuitpython-displayio-listselect-1.0.1/LICENSES/
--rw-r--r--   0 runner    (1001) docker     (123)    16814 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/LICENSES/CC-BY-4.0.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1108 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/LICENSES/MIT.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/LICENSES/Unlicense.txt
--rw-r--r--   0 runner    (1001) docker     (123)     4797 2023-04-10 15:15:51.649086 circuitpython-displayio-listselect-1.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3881 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/README.rst
--rw-r--r--   0 runner    (1001) docker     (123)      169 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/README.rst.license
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.649086 circuitpython-displayio-listselect-1.0.1/circuitpython_displayio_listselect.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4797 2023-04-10 15:15:51.000000 circuitpython-displayio-listselect-1.0.1/circuitpython_displayio_listselect.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1148 2023-04-10 15:15:51.000000 circuitpython-displayio-listselect-1.0.1/circuitpython_displayio_listselect.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-10 15:15:51.000000 circuitpython-displayio-listselect-1.0.1/circuitpython_displayio_listselect.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       64 2023-04-10 15:15:51.000000 circuitpython-displayio-listselect-1.0.1/circuitpython_displayio_listselect.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       21 2023-04-10 15:15:51.000000 circuitpython-displayio-listselect-1.0.1/circuitpython_displayio_listselect.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5881 2023-04-10 15:15:41.000000 circuitpython-displayio-listselect-1.0.1/displayio_listselect.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.649086 circuitpython-displayio-listselect-1.0.1/docs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.649086 circuitpython-displayio-listselect-1.0.1/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (123)     4414 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/_static/favicon.ico
--rw-r--r--   0 runner    (1001) docker     (123)      105 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/_static/favicon.ico.license
--rw-r--r--   0 runner    (1001) docker     (123)      271 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/api.rst
--rw-r--r--   0 runner    (1001) docker     (123)      170 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/api.rst.license
--rw-r--r--   0 runner    (1001) docker     (123)     5938 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      214 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/examples.rst
--rw-r--r--   0 runner    (1001) docker     (123)      170 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/examples.rst.license
--rw-r--r--   0 runner    (1001) docker     (123)      977 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      170 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/index.rst.license
--rw-r--r--   0 runner    (1001) docker     (123)      123 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 15:15:51.649086 circuitpython-displayio-listselect-1.0.1/examples/
--rw-r--r--   0 runner    (1001) docker     (123)     1236 2023-04-10 15:15:41.000000 circuitpython-displayio-listselect-1.0.1/examples/displayio_listselect_funhouse_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     2301 2023-04-10 15:15:41.000000 circuitpython-displayio-listselect-1.0.1/examples/displayio_listselect_joystick.py
--rw-r--r--   0 runner    (1001) docker     (123)     1175 2023-04-10 15:15:41.000000 circuitpython-displayio-listselect-1.0.1/examples/displayio_listselect_pygamedisplay_simpletest.py
--rw-r--r--   0 runner    (1001) docker     (123)      864 2023-04-10 15:15:41.000000 circuitpython-displayio-listselect-1.0.1/examples/displayio_listselect_simpletest.py
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/optional_requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1605 2023-04-10 15:15:41.000000 circuitpython-displayio-listselect-1.0.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      230 2023-04-10 15:15:27.000000 circuitpython-displayio-listselect-1.0.1/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-10 15:15:51.649086 circuitpython-displayio-listselect-1.0.1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.477796 circuitpython-displayio-listselect-1.0.2/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.473795 circuitpython-displayio-listselect-1.0.2/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.473795 circuitpython-displayio-listselect-1.0.2/.github/PULL_REQUEST_TEMPLATE/
+-rw-r--r--   0 runner    (1001) docker     (123)      880 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.473795 circuitpython-displayio-listselect-1.0.2/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      303 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.github/workflows/build.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      479 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.github/workflows/failure-help-text.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      736 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.github/workflows/release_gh.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      494 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.github/workflows/release_pypi.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1654 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1239 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    13069 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.pylintrc
+-rw-r--r--   0 runner    (1001) docker     (123)      405 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/.readthedocs.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     6717 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/CODE_OF_CONDUCT.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1085 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/LICENSE
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.473795 circuitpython-displayio-listselect-1.0.2/LICENSES/
+-rw-r--r--   0 runner    (1001) docker     (123)    16814 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/LICENSES/CC-BY-4.0.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1108 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/LICENSES/MIT.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/LICENSES/Unlicense.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     4797 2023-05-13 14:40:40.477796 circuitpython-displayio-listselect-1.0.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3881 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/README.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      169 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/README.rst.license
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.477796 circuitpython-displayio-listselect-1.0.2/circuitpython_displayio_listselect.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4797 2023-05-13 14:40:40.000000 circuitpython-displayio-listselect-1.0.2/circuitpython_displayio_listselect.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1188 2023-05-13 14:40:40.000000 circuitpython-displayio-listselect-1.0.2/circuitpython_displayio_listselect.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:40:40.000000 circuitpython-displayio-listselect-1.0.2/circuitpython_displayio_listselect.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 14:40:40.000000 circuitpython-displayio-listselect-1.0.2/circuitpython_displayio_listselect.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       21 2023-05-13 14:40:40.000000 circuitpython-displayio-listselect-1.0.2/circuitpython_displayio_listselect.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5881 2023-05-13 14:40:32.000000 circuitpython-displayio-listselect-1.0.2/displayio_listselect.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.477796 circuitpython-displayio-listselect-1.0.2/docs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.477796 circuitpython-displayio-listselect-1.0.2/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)     4414 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/_static/favicon.ico
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/_static/favicon.ico.license
+-rw-r--r--   0 runner    (1001) docker     (123)      271 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/api.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      170 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/api.rst.license
+-rw-r--r--   0 runner    (1001) docker     (123)     5963 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1230 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/examples.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      170 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/examples.rst.license
+-rw-r--r--   0 runner    (1001) docker     (123)      977 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      170 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/index.rst.license
+-rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/docs/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:40:40.477796 circuitpython-displayio-listselect-1.0.2/examples/
+-rw-r--r--   0 runner    (1001) docker     (123)     1236 2023-05-13 14:40:32.000000 circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_funhouse_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2301 2023-05-13 14:40:32.000000 circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_joystick.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1175 2023-05-13 14:40:32.000000 circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_pygamedisplay_simpletest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      864 2023-05-13 14:40:32.000000 circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_simpletest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1036 2023-05-13 14:40:32.000000 circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_styles.py
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/optional_requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1605 2023-05-13 14:40:32.000000 circuitpython-displayio-listselect-1.0.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      230 2023-05-13 14:40:17.000000 circuitpython-displayio-listselect-1.0.2/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:40:40.477796 circuitpython-displayio-listselect-1.0.2/setup.cfg
```

### Comparing `circuitpython-displayio-listselect-1.0.1/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md` & `circuitpython-displayio-listselect-1.0.2/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/.github/workflows/release_gh.yml` & `circuitpython-displayio-listselect-1.0.2/.github/workflows/release_gh.yml`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/.gitignore` & `circuitpython-displayio-listselect-1.0.2/.gitignore`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/.pre-commit-config.yaml` & `circuitpython-displayio-listselect-1.0.2/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/.pylintrc` & `circuitpython-displayio-listselect-1.0.2/.pylintrc`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/CODE_OF_CONDUCT.md` & `circuitpython-displayio-listselect-1.0.2/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/LICENSE` & `circuitpython-displayio-listselect-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/LICENSES/CC-BY-4.0.txt` & `circuitpython-displayio-listselect-1.0.2/LICENSES/CC-BY-4.0.txt`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/LICENSES/MIT.txt` & `circuitpython-displayio-listselect-1.0.2/LICENSES/MIT.txt`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/LICENSES/Unlicense.txt` & `circuitpython-displayio-listselect-1.0.2/LICENSES/Unlicense.txt`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/PKG-INFO` & `circuitpython-displayio-listselect-1.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: circuitpython-displayio-listselect
-Version: 1.0.1
+Version: 1.0.2
 Summary: ListSelect widget for circuitpython displayio. Display a list of strings with a selection indicator allow user to move selection up and down.
 Author-email: Adafruit Industries <circuitpython@adafruit.com>
 License: MIT
 Project-URL: Homepage, https://github.com/foamyguy/CircuitPython_DisplayIO_ListSelect
 Keywords: adafruit,blinka,circuitpython,micropython,displayio_listselect,list,select,listselect,dropdown,choice,choose,chooser,options,menu
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Libraries
```

### Comparing `circuitpython-displayio-listselect-1.0.1/README.rst` & `circuitpython-displayio-listselect-1.0.2/README.rst`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/circuitpython_displayio_listselect.egg-info/PKG-INFO` & `circuitpython-displayio-listselect-1.0.2/circuitpython_displayio_listselect.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: circuitpython-displayio-listselect
-Version: 1.0.1
+Version: 1.0.2
 Summary: ListSelect widget for circuitpython displayio. Display a list of strings with a selection indicator allow user to move selection up and down.
 Author-email: Adafruit Industries <circuitpython@adafruit.com>
 License: MIT
 Project-URL: Homepage, https://github.com/foamyguy/CircuitPython_DisplayIO_ListSelect
 Keywords: adafruit,blinka,circuitpython,micropython,displayio_listselect,list,select,listselect,dropdown,choice,choose,chooser,options,menu
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Libraries
```

### Comparing `circuitpython-displayio-listselect-1.0.1/circuitpython_displayio_listselect.egg-info/SOURCES.txt` & `circuitpython-displayio-listselect-1.0.2/circuitpython_displayio_listselect.egg-info/SOURCES.txt`

 * *Files 6% similar despite different names*

```diff
@@ -32,8 +32,9 @@
 docs/index.rst.license
 docs/requirements.txt
 docs/_static/favicon.ico
 docs/_static/favicon.ico.license
 examples/displayio_listselect_funhouse_test.py
 examples/displayio_listselect_joystick.py
 examples/displayio_listselect_pygamedisplay_simpletest.py
-examples/displayio_listselect_simpletest.py
+examples/displayio_listselect_simpletest.py
+examples/displayio_listselect_styles.py
```

### Comparing `circuitpython-displayio-listselect-1.0.1/displayio_listselect.py` & `circuitpython-displayio-listselect-1.0.2/displayio_listselect.py`

 * *Files 0% similar despite different names*

```diff
@@ -27,15 +27,15 @@
 """
 
 import terminalio
 from adafruit_display_text.bitmap_label import Label
 from displayio import Group
 
 
-__version__ = "1.0.1"
+__version__ = "1.0.2"
 __repo__ = "https://github.com/foamyguy/CircuitPython_DisplayIO_ListSelect.git"
 
 
 class ListSelect(Group):
     """
     ListSelect widget for CircuitPython DisplayIO.
     Display a list of strings with a selection indicator allow
```

### Comparing `circuitpython-displayio-listselect-1.0.1/docs/_static/favicon.ico` & `circuitpython-displayio-listselect-1.0.2/docs/_static/favicon.ico`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/docs/conf.py` & `circuitpython-displayio-listselect-1.0.2/docs/conf.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
     "sphinx.ext.napoleon",
     "sphinx.ext.todo",
 ]
 
 # Uncomment the below if you use native CircuitPython modules such as
 # digitalio, micropython and busio. List the modules you use. Without it, the
 # autodoc module docs will fail to generate with a warning.
-autodoc_mock_imports = ["displayio", "terminalio"]
+autodoc_mock_imports = ["displayio", "terminalio", "adafruit_display_text"]
 
 autodoc_preserve_defaults = True
 
 
 intersphinx_mapping = {
     "python": ("https://docs.python.org/3", None),
     "CircuitPython": ("https://docs.circuitpython.org/en/latest/", None),
```

### Comparing `circuitpython-displayio-listselect-1.0.1/docs/index.rst` & `circuitpython-displayio-listselect-1.0.2/docs/index.rst`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/examples/displayio_listselect_funhouse_test.py` & `circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_funhouse_test.py`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/examples/displayio_listselect_joystick.py` & `circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_joystick.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # SPDX-FileCopyrightText: 2020 Tim C
 #
 # SPDX-License-Identifier: MIT
 """
-FunHouse example for ListSelect
+Joystick example for ListSelect
 Make a ListSelect and use up, down, and select buttons to interact with it.
 """
 import time
 import board
 import displayio
 import analogio
 from displayio_listselect import ListSelect
```

### Comparing `circuitpython-displayio-listselect-1.0.1/examples/displayio_listselect_pygamedisplay_simpletest.py` & `circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_pygamedisplay_simpletest.py`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/examples/displayio_listselect_simpletest.py` & `circuitpython-displayio-listselect-1.0.2/examples/displayio_listselect_simpletest.py`

 * *Files identical despite different names*

### Comparing `circuitpython-displayio-listselect-1.0.1/pyproject.toml` & `circuitpython-displayio-listselect-1.0.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -9,15 +9,15 @@
     "wheel",
     "setuptools-scm",
 ]
 
 [project]
 name = "circuitpython-displayio-listselect"
 description = "ListSelect widget for circuitpython displayio. Display a list of strings with a selection indicator allow user to move selection up and down."
-version = "1.0.1"
+version = "1.0.2"
 readme = "README.rst"
 authors = [
     {name = "Adafruit Industries", email = "circuitpython@adafruit.com"}
 ]
 urls = {Homepage = "https://github.com/foamyguy/CircuitPython_DisplayIO_ListSelect"}
 keywords = [
     "adafruit",
```

