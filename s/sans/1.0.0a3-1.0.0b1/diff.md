# Comparing `tmp/sans-1.0.0a3.tar.gz` & `tmp/sans-1.0.0b1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sans-1.0.0a3.tar", last modified: Sat May 13 02:22:57 2023, max compression
+gzip compressed data, was "sans-1.0.0b1.tar", last modified: Sat May 13 06:36:22 2023, max compression
```

## Comparing `sans-1.0.0a3.tar` & `sans-1.0.0b1.tar`

### file list

```diff
@@ -1,49 +1,49 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.493552 sans-1.0.0a3/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.489552 sans-1.0.0a3/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.489552 sans-1.0.0a3/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-05-13 02:22:45.000000 sans-1.0.0a3/.github/workflows/codeql-analysis.yml
--rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-13 02:22:45.000000 sans-1.0.0a3/.github/workflows/pythonpublish.yml
--rw-r--r--   0 runner    (1001) docker     (123)     3101 2023-05-13 02:22:45.000000 sans-1.0.0a3/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1263 2023-05-13 02:22:45.000000 sans-1.0.0a3/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 02:22:45.000000 sans-1.0.0a3/.readthedocs.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-13 02:22:45.000000 sans-1.0.0a3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5831 2023-05-13 02:22:57.493552 sans-1.0.0a3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3329 2023-05-13 02:22:45.000000 sans-1.0.0a3/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.489552 sans-1.0.0a3/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      581 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/auth.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6127 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/errors.rst
--rw-r--r--   0 runner    (1001) docker     (123)      237 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      115 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/limiter.rst
--rw-r--r--   0 runner    (1001) docker     (123)       94 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/lock.rst
--rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)      106 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/response.rst
--rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/url.rst
--rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/utils.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2236 2023-05-13 02:22:45.000000 sans-1.0.0a3/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      239 2023-05-13 02:22:45.000000 sans-1.0.0a3/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.493552 sans-1.0.0a3/sans/
--rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)      803 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/_state.py
--rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/auth.py
--rw-r--r--   0 runner    (1001) docker     (123)     1310 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/client.py
--rw-r--r--   0 runner    (1001) docker     (123)    29355 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/client.pyi
--rw-r--r--   0 runner    (1001) docker     (123)     4276 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/decoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/errors.py
--rw-r--r--   0 runner    (1001) docker     (123)     6689 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/limiter.py
--rw-r--r--   0 runner    (1001) docker     (123)     5056 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/lock.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)     4163 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2310 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/url.py
--rw-r--r--   0 runner    (1001) docker     (123)     3213 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.493552 sans-1.0.0a3/sans.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5831 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      135 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 02:22:57.493552 sans-1.0.0a3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 02:22:45.000000 sans-1.0.0a3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.314650 sans-1.0.0b1/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.306650 sans-1.0.0b1/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.310650 sans-1.0.0b1/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-05-13 06:36:10.000000 sans-1.0.0b1/.github/workflows/codeql-analysis.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-13 06:36:10.000000 sans-1.0.0b1/.github/workflows/pythonpublish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     3101 2023-05-13 06:36:10.000000 sans-1.0.0b1/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1236 2023-05-13 06:36:10.000000 sans-1.0.0b1/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 06:36:10.000000 sans-1.0.0b1/.readthedocs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-13 06:36:10.000000 sans-1.0.0b1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5675 2023-05-13 06:36:22.314650 sans-1.0.0b1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3174 2023-05-13 06:36:10.000000 sans-1.0.0b1/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.310650 sans-1.0.0b1/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      581 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/auth.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6127 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/errors.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      237 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      115 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/limiter.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       94 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/lock.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)      106 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/response.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/url.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/utils.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2233 2023-05-13 06:36:10.000000 sans-1.0.0b1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      237 2023-05-13 06:36:10.000000 sans-1.0.0b1/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.310650 sans-1.0.0b1/sans/
+-rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      803 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/_state.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/auth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1310 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29256 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/client.pyi
+-rw-r--r--   0 runner    (1001) docker     (123)     4276 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/decoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6689 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/limiter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5056 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/lock.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     4163 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2310 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/url.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3279 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.314650 sans-1.0.0b1/sans.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5675 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      133 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 06:36:22.314650 sans-1.0.0b1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 06:36:10.000000 sans-1.0.0b1/setup.py
```

### Comparing `sans-1.0.0a3/.github/workflows/codeql-analysis.yml` & `sans-1.0.0b1/.github/workflows/codeql-analysis.yml`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/.github/workflows/pythonpublish.yml` & `sans-1.0.0b1/.github/workflows/pythonpublish.yml`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/.gitignore` & `sans-1.0.0b1/.gitignore`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/.pre-commit-config.yaml` & `sans-1.0.0b1/.pre-commit-config.yaml`

 * *Files 25% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 # See https://pre-commit.com for more information
 # See https://pre-commit.com/hooks.html for more hooks
-default_language_version:
-    python: python3.7
 repos:
 -   repo: https://github.com/pre-commit/pre-commit-hooks
     rev: v3.2.0
     hooks:
     -   id: trailing-whitespace
     -   id: end-of-file-fixer
     -   id: check-yaml
+    -   id: check-toml
     -   id: check-added-large-files
 -   repo: https://github.com/charliermarsh/ruff-pre-commit
     rev: v0.0.265
     hooks:
     -   id: ruff
         args: [ --fix, --exit-non-zero-on-fix ]
 -   repo: https://github.com/psf/black
@@ -21,15 +20,15 @@
     -   id: black
 -   repo: https://github.com/RobertCraigie/pyright-python
     rev: v1.1.306
     hooks:
     -   id: pyright
         additional_dependencies:
             # required dependencies
-        -   httpx ~= 0.21.1
+        -   httpx ~= 0.23
         -   importlib_metadata >= 1.4.0; python_version < "3.8"
 
             # optional dependencies
             # [lxml]
         -   lxml ~= 4.9.2
 
             # [json]
```

### Comparing `sans-1.0.0a3/LICENSE` & `sans-1.0.0b1/LICENSE`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/PKG-INFO` & `sans-1.0.0b1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sans
-Version: 1.0.0a3
+Version: 1.0.0b1
 Summary: Synchronous / Asynchronous HTTPX extension for NationStates
 Author: Zephyrkul
 License: MIT License
         
         Copyright (c) 2018 - 2023
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -24,15 +24,15 @@
         LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
         OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
         SOFTWARE.
         
 Project-URL: homepage, https://github.com/Zephyrkul/sans
 Project-URL: documentation, https://sans.readthedocs.io/en/stable/
 Project-URL: repository, https://github.com/Zephyrkul/sans.git
-Classifier: Development Status :: 3 - Alpha
+Classifier: Development Status :: 4 - Beta
 Classifier: Framework :: AsyncIO
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Intended Audience :: Developers
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.7
@@ -53,23 +53,17 @@
 License-File: LICENSE
 
 sans
 ====
 
 |pypi| |Code style: black| |Build Status| |Documentation Status|
 
-Synchronous / Asynchronous NationStates (Python wrapper for the
-NationStates API)
+**S**\ ynchronous / **A**\ synchronous **N**\ ation\ **S**\ tates
 
-Note
-~~~~
-While this library can be run in a single-threaded, synchronous environment,
-it is highly recommended to use Dolph's pynationstates
-(`GitHub <https://github.com/DolphDev/pynationstates>`_
-| `PyPI <https://pypi.org/project/nationstates/>`_) for simpler scripts.
+An extension for `HTTPX <https://www.python-httpx.org/>`_ for the `NationStates API <https://www.nationstates.net/pages/api.html>`_
 
 Installing
 ----------
 
 .. code::
 
    python3 -m pip install -U sans
```

### Comparing `sans-1.0.0a3/README.rst` & `sans-1.0.0b1/README.rst`

 * *Files 12% similar despite different names*

```diff
@@ -1,21 +1,15 @@
 sans
 ====
 
 |pypi| |Code style: black| |Build Status| |Documentation Status|
 
-Synchronous / Asynchronous NationStates (Python wrapper for the
-NationStates API)
+**S**\ ynchronous / **A**\ synchronous **N**\ ation\ **S**\ tates
 
-Note
-~~~~
-While this library can be run in a single-threaded, synchronous environment,
-it is highly recommended to use Dolph's pynationstates
-(`GitHub <https://github.com/DolphDev/pynationstates>`_
-| `PyPI <https://pypi.org/project/nationstates/>`_) for simpler scripts.
+An extension for `HTTPX <https://www.python-httpx.org/>`_ for the `NationStates API <https://www.nationstates.net/pages/api.html>`_
 
 Installing
 ----------
 
 .. code::
 
    python3 -m pip install -U sans
```

### Comparing `sans-1.0.0a3/docs/Makefile` & `sans-1.0.0b1/docs/Makefile`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/docs/conf.py` & `sans-1.0.0b1/docs/conf.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/docs/make.bat` & `sans-1.0.0b1/docs/make.bat`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/pyproject.toml` & `sans-1.0.0b1/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 
 [project]
     name = 'sans'
     description = 'Synchronous / Asynchronous HTTPX extension for NationStates'
     readme = 'README.rst'
     requires-python = '>=3.7.0,<4.0'
     classifiers = [
-        'Development Status :: 3 - Alpha',
+        'Development Status :: 4 - Beta',
         'Framework :: AsyncIO',
         'License :: OSI Approved :: MIT License',
         'Intended Audience :: Developers',
         'Natural Language :: English',
         'Operating System :: OS Independent',
         'Programming Language :: Python :: 3 :: Only',
         'Programming Language :: Python :: 3.7',
@@ -28,15 +28,15 @@
         'Topic :: Internet',
         'Topic :: Software Development :: Libraries',
         'Topic :: Software Development :: Libraries :: Python Modules',
         'Topic :: Utilities',
         'Typing :: Typed'
     ]
     dependencies = [
-        'httpx ~= 0.21.1',
+        'httpx ~= 0.23',
         'importlib_metadata >= 1.4.0; python_version < "3.8"'
     ]
     dynamic = ['version']
 
 [project.license]
 file = 'LICENSE'
```

### Comparing `sans-1.0.0a3/sans/__init__.py` & `sans-1.0.0b1/sans/__init__.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/__main__.py` & `sans-1.0.0b1/sans/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -77,15 +77,15 @@
                     else:
                         parameters.setdefault(key, []).append(arg)
                         key = "q"
                 if key != "q":
                     print("No value provided for key {!r}".format(key), file=sys.stderr)
                 with client.stream(
                     "GET",
-                    sans.World(**{k: "+".join(v) for k, v in parameters.items()}),
+                    sans.World(**{k: " ".join(v) for k, v in parameters.items()}),
                 ) as response:
                     if known.url:
                         print(response.url, end="\n\n")
                     if known.headers:
                         print(response.headers, end="\n\n")
                     for element in response.iter_xml():
                         pretty_print(element)
```

### Comparing `sans-1.0.0a3/sans/_state.py` & `sans-1.0.0b1/sans/_state.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/auth.py` & `sans-1.0.0b1/sans/auth.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/client.py` & `sans-1.0.0b1/sans/client.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/client.pyi` & `sans-1.0.0b1/sans/client.pyi`

 * *Files 0% similar despite different names*

```diff
@@ -1,39 +1,35 @@
 from __future__ import annotations
 
 from typing import (
-    TYPE_CHECKING,
     Any,
     AsyncContextManager,
     Callable,
     Collection,
     ContextManager,
     Mapping,
     overload,
 )
+from typing_extensions import TypedDict
 
 import httpx
-
-if TYPE_CHECKING:
-    from typing_extensions import TypedDict
-
-    from httpx._types import (
-        AuthTypes,
-        CertTypes,
-        CookieTypes,
-        HeaderTypes,
-        ProxiesTypes,
-        QueryParamTypes,
-        RequestContent,
-        RequestData,
-        RequestFiles,
-        TimeoutTypes,
-        URLTypes,
-        VerifyTypes,
-    )
+from httpx._types import (
+    AuthTypes,
+    CertTypes,
+    CookieTypes,
+    HeaderTypes,
+    ProxiesTypes,
+    QueryParamTypes,
+    RequestContent,
+    RequestData,
+    RequestFiles,
+    TimeoutTypes,
+    URLTypes,
+    VerifyTypes,
+)
 
 from .limiter import RateLimiter
 from .response import Response
 
 __all__ = [
     "Client",
     "AsyncClient",
```

### Comparing `sans-1.0.0a3/sans/decoder.py` & `sans-1.0.0b1/sans/decoder.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/errors.py` & `sans-1.0.0b1/sans/errors.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/limiter.py` & `sans-1.0.0b1/sans/limiter.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/lock.py` & `sans-1.0.0b1/sans/lock.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/response.py` & `sans-1.0.0b1/sans/response.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a3/sans/url.py` & `sans-1.0.0b1/sans/url.py`

 * *Files 1% similar despite different names*

```diff
@@ -37,15 +37,15 @@
         try:
             shard = dict(shard)  # type: ignore
         except (TypeError, ValueError):
             q.append(str(shard))
         else:
             q.append(shard.pop("q", None))  # type: ignore
             query.update(shard)  # type: ignore
-    query.update(parameters, q="+".join(map(str, filter(None, q))))
+    query.update(parameters, q=" ".join(map(str, filter(None, q))))
     if query.get("a", "").lower() == "sendtg":
         raise RuntimeError("sans does not currently support the telegram API.")
     return API_URL.copy_with(params=query)
 
 
 def WA(wa: Literal[1, "1", 2, "2"], *shards: str, **parameters: str) -> httpx.URL:
     return World(*shards, wa=str(wa), **parameters)
```

### Comparing `sans-1.0.0a3/sans/utils.py` & `sans-1.0.0b1/sans/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -30,24 +30,26 @@
     *shards: str | Mapping[str, str],
     **parameters: str,
 ) -> Response | Coroutine[Any, Any, Response]:
     if isinstance(client, AsyncClientType):
         return _prepare_async(client, *shards, **parameters)
     request = World(*shards, **parameters, mode="prepare")
     response = client.get(request)
+    response.raise_for_status()
     token: str = response.xml.find("SUCCESS").text  # type: ignore
     request = World(*shards, **parameters, mode="execute", token=token)
     return client.get(request)
 
 
 async def _prepare_async(
     client: AsyncClientType, *shards: str | Mapping[str, str], **parameters: str
 ) -> Response:
     request = World(*shards, **parameters, mode="prepare")
     response = await client.get(request)
+    response.raise_for_status()
     token: str = response.xml.find("SUCCESS").text  # type: ignore
     request = World(*shards, **parameters, mode="execute", token=token)
     return await client.get(request)
 
 
 if sys.version_info < (3, 9):
     # from: https://github.com/python/cpython/blob/3.11/Lib/xml/etree/ElementTree.py#L1154
```

### Comparing `sans-1.0.0a3/sans.egg-info/PKG-INFO` & `sans-1.0.0b1/sans.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sans
-Version: 1.0.0a3
+Version: 1.0.0b1
 Summary: Synchronous / Asynchronous HTTPX extension for NationStates
 Author: Zephyrkul
 License: MIT License
         
         Copyright (c) 2018 - 2023
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -24,15 +24,15 @@
         LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
         OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
         SOFTWARE.
         
 Project-URL: homepage, https://github.com/Zephyrkul/sans
 Project-URL: documentation, https://sans.readthedocs.io/en/stable/
 Project-URL: repository, https://github.com/Zephyrkul/sans.git
-Classifier: Development Status :: 3 - Alpha
+Classifier: Development Status :: 4 - Beta
 Classifier: Framework :: AsyncIO
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Intended Audience :: Developers
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.7
@@ -53,23 +53,17 @@
 License-File: LICENSE
 
 sans
 ====
 
 |pypi| |Code style: black| |Build Status| |Documentation Status|
 
-Synchronous / Asynchronous NationStates (Python wrapper for the
-NationStates API)
+**S**\ ynchronous / **A**\ synchronous **N**\ ation\ **S**\ tates
 
-Note
-~~~~
-While this library can be run in a single-threaded, synchronous environment,
-it is highly recommended to use Dolph's pynationstates
-(`GitHub <https://github.com/DolphDev/pynationstates>`_
-| `PyPI <https://pypi.org/project/nationstates/>`_) for simpler scripts.
+An extension for `HTTPX <https://www.python-httpx.org/>`_ for the `NationStates API <https://www.nationstates.net/pages/api.html>`_
 
 Installing
 ----------
 
 .. code::
 
    python3 -m pip install -U sans
```

### Comparing `sans-1.0.0a3/sans.egg-info/SOURCES.txt` & `sans-1.0.0b1/sans.egg-info/SOURCES.txt`

 * *Files identical despite different names*

