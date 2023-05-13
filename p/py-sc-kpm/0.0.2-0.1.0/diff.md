# Comparing `tmp/py-sc-kpm-0.0.2.tar.gz` & `tmp/py-sc-kpm-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "py-sc-kpm-0.0.2.tar", last modified: Sat May 13 08:36:04 2023, max compression
+gzip compressed data, was "py-sc-kpm-0.1.0.tar", last modified: Sat May 13 08:47:06 2023, max compression
```

## Comparing `py-sc-kpm-0.0.2.tar` & `py-sc-kpm-0.1.0.tar`

### file list

```diff
@@ -1,36 +1,36 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:36:04.171487 py-sc-kpm-0.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    25873 2023-05-13 08:36:04.171487 py-sc-kpm-0.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    25014 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      404 2023-05-13 08:36:04.175487 py-sc-kpm-0.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1939 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:36:04.167487 py-sc-kpm-0.0.2/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:36:04.167487 py-sc-kpm-0.0.2/src/py_sc_kpm.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    25873 2023-05-13 08:36:04.000000 py-sc-kpm-0.0.2/src/py_sc_kpm.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      759 2023-05-13 08:36:04.000000 py-sc-kpm-0.0.2/src/py_sc_kpm.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:36:04.000000 py-sc-kpm-0.0.2/src/py_sc_kpm.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 08:36:04.000000 py-sc-kpm-0.0.2/src/py_sc_kpm.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 08:36:04.000000 py-sc-kpm-0.0.2/src/py_sc_kpm.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:36:04.171487 py-sc-kpm-0.0.2/src/sc_kpm/
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2841 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/identifiers.py
--rw-r--r--   0 runner    (1001) docker     (123)      355 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/logging.py
--rw-r--r--   0 runner    (1001) docker     (123)     4139 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_agent.py
--rw-r--r--   0 runner    (1001) docker     (123)     3060 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_keynodes.py
--rw-r--r--   0 runner    (1001) docker     (123)     2534 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_module.py
--rw-r--r--   0 runner    (1001) docker     (123)      902 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_result.py
--rw-r--r--   0 runner    (1001) docker     (123)     6008 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_server.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:36:04.171487 py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/
--rw-r--r--   0 runner    (1001) docker     (123)      206 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2485 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/sc_numbered_set.py
--rw-r--r--   0 runner    (1001) docker     (123)     5341 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/sc_oriented_set.py
--rw-r--r--   0 runner    (1001) docker     (123)     3459 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/sc_set.py
--rw-r--r--   0 runner    (1001) docker     (123)      864 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/sc_structure.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:36:04.171487 py-sc-kpm-0.0.2/src/sc_kpm/utils/
--rw-r--r--   0 runner    (1001) docker     (123)      709 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5363 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/utils/action_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     5447 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/utils/common_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      603 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/src/sc_kpm/utils/iteration_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:36:04.171487 py-sc-kpm-0.0.2/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     5215 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/tests/test_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     1851 2023-05-13 08:35:51.000000 py-sc-kpm-0.0.2/tests/test_keynodes.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:47:06.073975 py-sc-kpm-0.1.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    25873 2023-05-13 08:47:06.073975 py-sc-kpm-0.1.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    25014 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      404 2023-05-13 08:47:06.073975 py-sc-kpm-0.1.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1939 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:47:06.069975 py-sc-kpm-0.1.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:47:06.069975 py-sc-kpm-0.1.0/src/py_sc_kpm.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    25873 2023-05-13 08:47:06.000000 py-sc-kpm-0.1.0/src/py_sc_kpm.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      759 2023-05-13 08:47:06.000000 py-sc-kpm-0.1.0/src/py_sc_kpm.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:47:06.000000 py-sc-kpm-0.1.0/src/py_sc_kpm.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 08:47:06.000000 py-sc-kpm-0.1.0/src/py_sc_kpm.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 08:47:06.000000 py-sc-kpm-0.1.0/src/py_sc_kpm.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:47:06.069975 py-sc-kpm-0.1.0/src/sc_kpm/
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2841 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/identifiers.py
+-rw-r--r--   0 runner    (1001) docker     (123)      355 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4139 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_agent.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3060 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_keynodes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2534 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_module.py
+-rw-r--r--   0 runner    (1001) docker     (123)      902 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_result.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6008 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_server.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:47:06.069975 py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/
+-rw-r--r--   0 runner    (1001) docker     (123)      206 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2485 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/sc_numbered_set.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5341 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/sc_oriented_set.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3459 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/sc_set.py
+-rw-r--r--   0 runner    (1001) docker     (123)      864 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/sc_structure.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:47:06.073975 py-sc-kpm-0.1.0/src/sc_kpm/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)      709 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5363 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/utils/action_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5447 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/utils/common_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      603 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/src/sc_kpm/utils/iteration_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:47:06.073975 py-sc-kpm-0.1.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     5215 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/tests/test_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1851 2023-05-13 08:46:53.000000 py-sc-kpm-0.1.0/tests/test_keynodes.py
```

### Comparing `py-sc-kpm-0.0.2/LICENSE` & `py-sc-kpm-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/PKG-INFO` & `py-sc-kpm-0.1.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-sc-kpm
-Version: 0.0.2
+Version: 0.1.0
 Summary: The Python implementation of the knowledge processing module for knowledge manipulations
 Home-page: https://github.com/ostis-ai/py-sc-kpm
 Author: ostis-ai
 License: MIT
 Project-URL: Bug Reports, https://github.com/ostis-ai/py-sc-kpm/issues
 Project-URL: Source, https://github.com/ostis-ai/py-sc-kpm
 Keywords: sc-kpm,kpm,knowledge processing
```

### Comparing `py-sc-kpm-0.0.2/README.md` & `py-sc-kpm-0.1.0/README.md`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/setup.py` & `py-sc-kpm-0.1.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from pathlib import Path
 
 from setuptools import find_packages, setup
 
 DIRECTORY_PATH = Path(__file__).parent
 README = (DIRECTORY_PATH / "README.md").read_text()
 
-VERSION = "0.0.2"
+VERSION = "0.1.0"
 INSTALL_REQUIRES = ["py-sc-client>=0.2.6"]
 CURRENT_PYTHON = sys.version_info[:2]
 REQUIRED_PYTHON = (3, 8)
 
 
 if CURRENT_PYTHON < REQUIRED_PYTHON:
     sys.stderr.write(
```

### Comparing `py-sc-kpm-0.0.2/src/py_sc_kpm.egg-info/PKG-INFO` & `py-sc-kpm-0.1.0/src/py_sc_kpm.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-sc-kpm
-Version: 0.0.2
+Version: 0.1.0
 Summary: The Python implementation of the knowledge processing module for knowledge manipulations
 Home-page: https://github.com/ostis-ai/py-sc-kpm
 Author: ostis-ai
 License: MIT
 Project-URL: Bug Reports, https://github.com/ostis-ai/py-sc-kpm/issues
 Project-URL: Source, https://github.com/ostis-ai/py-sc-kpm
 Keywords: sc-kpm,kpm,knowledge processing
```

### Comparing `py-sc-kpm-0.0.2/src/py_sc_kpm.egg-info/SOURCES.txt` & `py-sc-kpm-0.1.0/src/py_sc_kpm.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/__init__.py` & `py-sc-kpm-0.1.0/src/sc_kpm/__init__.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/identifiers.py` & `py-sc-kpm-0.1.0/src/sc_kpm/identifiers.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_agent.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_agent.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_keynodes.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_keynodes.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_module.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_module.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_result.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_result.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_server.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_server.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/sc_numbered_set.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/sc_numbered_set.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/sc_oriented_set.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/sc_oriented_set.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/sc_set.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/sc_set.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/sc_sets/sc_structure.py` & `py-sc-kpm-0.1.0/src/sc_kpm/sc_sets/sc_structure.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/utils/__init__.py` & `py-sc-kpm-0.1.0/src/sc_kpm/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/utils/action_utils.py` & `py-sc-kpm-0.1.0/src/sc_kpm/utils/action_utils.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/utils/common_utils.py` & `py-sc-kpm-0.1.0/src/sc_kpm/utils/common_utils.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/src/sc_kpm/utils/iteration_utils.py` & `py-sc-kpm-0.1.0/src/sc_kpm/utils/iteration_utils.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/tests/test_classes.py` & `py-sc-kpm-0.1.0/tests/test_classes.py`

 * *Files identical despite different names*

### Comparing `py-sc-kpm-0.0.2/tests/test_keynodes.py` & `py-sc-kpm-0.1.0/tests/test_keynodes.py`

 * *Files identical despite different names*

