# Comparing `tmp/rootutils-1.0.5.tar.gz` & `tmp/rootutils-1.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rootutils-1.0.5.tar", last modified: Sat May 13 17:17:44 2023, max compression
+gzip compressed data, was "rootutils-1.0.6.tar", last modified: Sat May 13 17:54:25 2023, max compression
```

## Comparing `rootutils-1.0.5.tar` & `rootutils-1.0.6.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:17:44.601578 rootutils-1.0.5/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 17:17:33.000000 rootutils-1.0.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     4653 2023-05-13 17:17:44.601578 rootutils-1.0.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4345 2023-05-13 17:17:33.000000 rootutils-1.0.5/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      442 2023-05-13 17:17:33.000000 rootutils-1.0.5/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:17:44.597577 rootutils-1.0.5/rootutils/
--rw-r--r--   0 runner    (1001) docker     (123)      106 2023-05-13 17:17:33.000000 rootutils-1.0.5/rootutils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4774 2023-05-13 17:17:33.000000 rootutils-1.0.5/rootutils/rootutils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:17:44.601578 rootutils-1.0.5/rootutils.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4653 2023-05-13 17:17:44.000000 rootutils-1.0.5/rootutils.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      310 2023-05-13 17:17:44.000000 rootutils-1.0.5/rootutils.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:17:44.000000 rootutils-1.0.5/rootutils.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 17:17:44.000000 rootutils-1.0.5/rootutils.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 17:17:44.000000 rootutils-1.0.5/rootutils.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 17:17:44.601578 rootutils-1.0.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      615 2023-05-13 17:17:33.000000 rootutils-1.0.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:17:44.601578 rootutils-1.0.5/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:17:33.000000 rootutils-1.0.5/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:17:33.000000 rootutils-1.0.5/tests/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     1837 2023-05-13 17:17:33.000000 rootutils-1.0.5/tests/test_rootutils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:54:25.455986 rootutils-1.0.6/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 17:54:12.000000 rootutils-1.0.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4657 2023-05-13 17:54:25.455986 rootutils-1.0.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4349 2023-05-13 17:54:12.000000 rootutils-1.0.6/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      442 2023-05-13 17:54:12.000000 rootutils-1.0.6/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:54:25.455986 rootutils-1.0.6/rootutils/
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 17:54:12.000000 rootutils-1.0.6/rootutils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5779 2023-05-13 17:54:12.000000 rootutils-1.0.6/rootutils/rootutils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:54:25.455986 rootutils-1.0.6/rootutils.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4657 2023-05-13 17:54:25.000000 rootutils-1.0.6/rootutils.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      310 2023-05-13 17:54:25.000000 rootutils-1.0.6/rootutils.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:54:25.000000 rootutils-1.0.6/rootutils.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 17:54:25.000000 rootutils-1.0.6/rootutils.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 17:54:25.000000 rootutils-1.0.6/rootutils.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 17:54:25.455986 rootutils-1.0.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      615 2023-05-13 17:54:12.000000 rootutils-1.0.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:54:25.455986 rootutils-1.0.6/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:54:12.000000 rootutils-1.0.6/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:54:12.000000 rootutils-1.0.6/tests/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1837 2023-05-13 17:54:12.000000 rootutils-1.0.6/tests/test_rootutils.py
```

### Comparing `rootutils-1.0.5/LICENSE` & `rootutils-1.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `rootutils-1.0.5/PKG-INFO` & `rootutils-1.0.6/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rootutils
-Version: 1.0.5
+Version: 1.0.6
 Summary: Simple package for easy project root setup
 Home-page: https://github.com/ashleve/rootutils
 Author: ashleve
 Author-email: ashlevegalaxy@gmail.com
 License: MIT
 Requires-Python: >=3.7.0
 Description-Content-Type: text/markdown
@@ -14,16 +14,16 @@
 
 [![Python](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-370/)
 [![Tests](https://github.com/ashleve/rootutils/actions/workflows/test.yml/badge.svg?branch=main&event=push)](https://github.com/ashleve/rootutils/actions/workflows/test.yml)
 [![Codecov](https://codecov.io/gh/ashleve/rootutils/branch/main/graph/badge.svg)](https://codecov.io/gh/ashleve/rootutils)
 [![Build](https://github.com/ashleve/rootutils/actions/workflows/publish_package.yml/badge.svg)](https://github.com/ashleve/rootutils/actions/workflows/publish_package.yml)
 [![Issues](https://img.shields.io/github/issues/ashleve/rootutils)](https://github.com/ashleve/rootutils/issues)
 [![License](https://img.shields.io/github/license/ashleve/rootutils)](https://github.com/ashleve/rootutils/blob/main/LICENSE)
-[![Release](https://img.shields.io/pypi/v/rootutils)](pypi.org/project/rootutils/1.0.5/)
-[![PyPi](https://img.shields.io/pypi/dm/rootutils)](pypi.org/project/rootutils/1.0.5/)
+[![Release](https://img.shields.io/pypi/v/rootutils)](https://pypi.org/project/rootutils/)
+[![PyPi](https://img.shields.io/pypi/dm/rootutils)](https://pypi.org/project/rootutils/)
 
 A simple python package to solve all your problems with pythonpath, working directory, file paths, module imports and environment variables.
 
 ## Why rootutils?
 
 **Problem:** I would like to be able to:
```

### Comparing `rootutils-1.0.5/README.md` & `rootutils-1.0.6/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -2,16 +2,16 @@
 
 [![Python](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-370/)
 [![Tests](https://github.com/ashleve/rootutils/actions/workflows/test.yml/badge.svg?branch=main&event=push)](https://github.com/ashleve/rootutils/actions/workflows/test.yml)
 [![Codecov](https://codecov.io/gh/ashleve/rootutils/branch/main/graph/badge.svg)](https://codecov.io/gh/ashleve/rootutils)
 [![Build](https://github.com/ashleve/rootutils/actions/workflows/publish_package.yml/badge.svg)](https://github.com/ashleve/rootutils/actions/workflows/publish_package.yml)
 [![Issues](https://img.shields.io/github/issues/ashleve/rootutils)](https://github.com/ashleve/rootutils/issues)
 [![License](https://img.shields.io/github/license/ashleve/rootutils)](https://github.com/ashleve/rootutils/blob/main/LICENSE)
-[![Release](https://img.shields.io/pypi/v/rootutils)](pypi.org/project/rootutils/1.0.5/)
-[![PyPi](https://img.shields.io/pypi/dm/rootutils)](pypi.org/project/rootutils/1.0.5/)
+[![Release](https://img.shields.io/pypi/v/rootutils)](https://pypi.org/project/rootutils/)
+[![PyPi](https://img.shields.io/pypi/dm/rootutils)](https://pypi.org/project/rootutils/)
 
 A simple python package to solve all your problems with pythonpath, working directory, file paths, module imports and environment variables.
 
 ## Why rootutils?
 
 **Problem:** I would like to be able to:
```

### Comparing `rootutils-1.0.5/rootutils/rootutils.py` & `rootutils-1.0.6/rootutils/rootutils.py`

 * *Files 10% similar despite different names*

```diff
@@ -150,7 +150,40 @@
         path=path,
         project_root_env_var=project_root_env_var,
         dotenv=dotenv,
         pythonpath=pythonpath,
         cwd=cwd,
     )
     return path
+
+
+def autosetup(
+    indicator=".project-root",
+    project_root_env_var=True,
+    dotenv=True,
+    pythonpath=True,
+    cwd=False,
+) -> Path:
+    """Experimental method for less friction. Automatically inferrs `search_from` path."""
+
+    # this line finds the absolute path of the original python script that is being run
+    startfile = os.path.abspath(sys.argv[0])
+
+    # if we are in notebook or pytest, just use current working directory
+    if startfile.endswith("ipykernel_launcher.py") or startfile.endswith("pytest"):
+        startfile = os.getcwd()
+
+    # convert to Path object
+    startfile = Path(startfile)
+
+    # this line recursively searches for ".project-root" file
+    # starting from folder containing the entry python script and going up until it finds it
+    path = setup_root(
+        search_from=startfile,
+        indicator=indicator,
+        project_root_env_var=project_root_env_var,
+        dotenv=dotenv,
+        pythonpath=pythonpath,
+        cwd=cwd,
+    )
+
+    return path
```

### Comparing `rootutils-1.0.5/rootutils.egg-info/PKG-INFO` & `rootutils-1.0.6/rootutils.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rootutils
-Version: 1.0.5
+Version: 1.0.6
 Summary: Simple package for easy project root setup
 Home-page: https://github.com/ashleve/rootutils
 Author: ashleve
 Author-email: ashlevegalaxy@gmail.com
 License: MIT
 Requires-Python: >=3.7.0
 Description-Content-Type: text/markdown
@@ -14,16 +14,16 @@
 
 [![Python](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-370/)
 [![Tests](https://github.com/ashleve/rootutils/actions/workflows/test.yml/badge.svg?branch=main&event=push)](https://github.com/ashleve/rootutils/actions/workflows/test.yml)
 [![Codecov](https://codecov.io/gh/ashleve/rootutils/branch/main/graph/badge.svg)](https://codecov.io/gh/ashleve/rootutils)
 [![Build](https://github.com/ashleve/rootutils/actions/workflows/publish_package.yml/badge.svg)](https://github.com/ashleve/rootutils/actions/workflows/publish_package.yml)
 [![Issues](https://img.shields.io/github/issues/ashleve/rootutils)](https://github.com/ashleve/rootutils/issues)
 [![License](https://img.shields.io/github/license/ashleve/rootutils)](https://github.com/ashleve/rootutils/blob/main/LICENSE)
-[![Release](https://img.shields.io/pypi/v/rootutils)](pypi.org/project/rootutils/1.0.5/)
-[![PyPi](https://img.shields.io/pypi/dm/rootutils)](pypi.org/project/rootutils/1.0.5/)
+[![Release](https://img.shields.io/pypi/v/rootutils)](https://pypi.org/project/rootutils/)
+[![PyPi](https://img.shields.io/pypi/dm/rootutils)](https://pypi.org/project/rootutils/)
 
 A simple python package to solve all your problems with pythonpath, working directory, file paths, module imports and environment variables.
 
 ## Why rootutils?
 
 **Problem:** I would like to be able to:
```

### Comparing `rootutils-1.0.5/setup.py` & `rootutils-1.0.6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 with open("README.md") as f:
     long_description = f.read()
 
 
 setup(
     name="rootutils",
-    version="1.0.5",
+    version="1.0.6",
     license="MIT",
     description="Simple package for easy project root setup",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/ashleve/rootutils",
     author="ashleve",
     author_email="ashlevegalaxy@gmail.com",
```

### Comparing `rootutils-1.0.5/tests/test_rootutils.py` & `rootutils-1.0.6/tests/test_rootutils.py`

 * *Files identical despite different names*

