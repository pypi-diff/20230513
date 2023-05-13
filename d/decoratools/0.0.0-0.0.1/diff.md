# Comparing `tmp/decoratools-0.0.0.tar.gz` & `tmp/decoratools-0.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "decoratools-0.0.0.tar", last modified: Sat May 13 11:45:15 2023, max compression
+gzip compressed data, was "decoratools-0.0.1.tar", last modified: Sat May 13 11:58:44 2023, max compression
```

## Comparing `decoratools-0.0.0.tar` & `decoratools-0.0.1.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:45:15.371701 decoratools-0.0.0/
--rw-rw-rw-   0 root         (0) root         (0)       94 2023-05-13 11:44:57.000000 decoratools-0.0.0/.gitignore
--rw-rw-rw-   0 root         (0) root         (0)     4303 2023-05-13 11:44:57.000000 decoratools-0.0.0/.gitlab-ci.yml
--rw-rw-rw-   0 root         (0) root         (0)      717 2023-05-13 11:44:57.000000 decoratools-0.0.0/.pre-commit-config.yaml
--rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 11:44:57.000000 decoratools-0.0.0/LICENSE
--rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 11:45:15.371701 decoratools-0.0.0/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)      306 2023-05-13 11:44:57.000000 decoratools-0.0.0/Pipfile
--rw-rw-rw-   0 root         (0) root         (0)    43703 2023-05-13 11:44:57.000000 decoratools-0.0.0/Pipfile.lock
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:45:15.363700 decoratools-0.0.0/decoratools/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:45:15.369701 decoratools-0.0.0/decoratools/capi/
--rw-rw-rw-   0 root         (0) root         (0)     4084 2023-05-13 11:44:57.000000 decoratools-0.0.0/decoratools/capi/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:45:15.369701 decoratools-0.0.0/decoratools.egg-info/
--rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 11:45:15.000000 decoratools-0.0.0/decoratools.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      327 2023-05-13 11:45:15.000000 decoratools-0.0.0/decoratools.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 11:45:15.000000 decoratools-0.0.0/decoratools.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       12 2023-05-13 11:45:15.000000 decoratools-0.0.0/decoratools.egg-info/top_level.txt
--rw-rw-rw-   0 root         (0) root         (0)     1368 2023-05-13 11:44:57.000000 decoratools-0.0.0/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 11:45:15.371701 decoratools-0.0.0/setup.cfg
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:45:15.370701 decoratools-0.0.0/tests/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 11:44:57.000000 decoratools-0.0.0/tests/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:45:15.371701 decoratools-0.0.0/tests/unit/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 11:44:57.000000 decoratools-0.0.0/tests/unit/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     8926 2023-05-13 11:44:57.000000 decoratools-0.0.0/tests/unit/test_capi.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.837163 decoratools-0.0.1/
+-rw-rw-rw-   0 root         (0) root         (0)       94 2023-05-13 11:58:27.000000 decoratools-0.0.1/.gitignore
+-rw-rw-rw-   0 root         (0) root         (0)     4303 2023-05-13 11:58:27.000000 decoratools-0.0.1/.gitlab-ci.yml
+-rw-rw-rw-   0 root         (0) root         (0)      717 2023-05-13 11:58:27.000000 decoratools-0.0.1/.pre-commit-config.yaml
+-rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 11:58:27.000000 decoratools-0.0.1/LICENSE
+-rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 11:58:44.836163 decoratools-0.0.1/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)      306 2023-05-13 11:58:27.000000 decoratools-0.0.1/Pipfile
+-rw-rw-rw-   0 root         (0) root         (0)    43703 2023-05-13 11:58:27.000000 decoratools-0.0.1/Pipfile.lock
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.830163 decoratools-0.0.1/decoratools/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.835163 decoratools-0.0.1/decoratools/capi/
+-rw-rw-rw-   0 root         (0) root         (0)     4084 2023-05-13 11:58:27.000000 decoratools-0.0.1/decoratools/capi/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.835163 decoratools-0.0.1/decoratools.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 11:58:44.000000 decoratools-0.0.1/decoratools.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      327 2023-05-13 11:58:44.000000 decoratools-0.0.1/decoratools.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 11:58:44.000000 decoratools-0.0.1/decoratools.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       12 2023-05-13 11:58:44.000000 decoratools-0.0.1/decoratools.egg-info/top_level.txt
+-rw-rw-rw-   0 root         (0) root         (0)     1368 2023-05-13 11:58:27.000000 decoratools-0.0.1/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 11:58:44.837163 decoratools-0.0.1/setup.cfg
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.835163 decoratools-0.0.1/tests/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 11:58:27.000000 decoratools-0.0.1/tests/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.836163 decoratools-0.0.1/tests/unit/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 11:58:27.000000 decoratools-0.0.1/tests/unit/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     8919 2023-05-13 11:58:27.000000 decoratools-0.0.1/tests/unit/test_capi.py
```

### Comparing `decoratools-0.0.0/.gitlab-ci.yml` & `decoratools-0.0.1/.gitlab-ci.yml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.0/.pre-commit-config.yaml` & `decoratools-0.0.1/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.0/LICENSE` & `decoratools-0.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.0/PKG-INFO` & `decoratools-0.0.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: decoratools
-Version: 0.0.0
+Version: 0.0.1
 Summary: Collection of useful decorators
 Author-email: Quentin Bouget <ypsah@devyard.org>
 License: MIT
 Project-URL: homepage, https://gitlab.com/ypsah/decoratools
 Project-URL: repository, https://gitlab.com/ypsah/decoratools
 Keywords: decorator,utility,library
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `decoratools-0.0.0/Pipfile.lock` & `decoratools-0.0.1/Pipfile.lock`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.0/decoratools/capi/__init__.py` & `decoratools-0.0.1/decoratools/capi/__init__.py`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.0/decoratools.egg-info/PKG-INFO` & `decoratools-0.0.1/decoratools.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: decoratools
-Version: 0.0.0
+Version: 0.0.1
 Summary: Collection of useful decorators
 Author-email: Quentin Bouget <ypsah@devyard.org>
 License: MIT
 Project-URL: homepage, https://gitlab.com/ypsah/decoratools
 Project-URL: repository, https://gitlab.com/ypsah/decoratools
 Keywords: decorator,utility,library
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `decoratools-0.0.0/pyproject.toml` & `decoratools-0.0.1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.0/tests/unit/test_capi.py` & `decoratools-0.0.1/tests/unit/test_capi.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,11 @@
 from __future__ import annotations
 
 import ctypes
-from contextlib import suppress
 from dataclasses import is_dataclass
-from inspect import get_annotations
 from types import GenericAlias
 from typing import Annotated
 
 import pytest
 
 from decoratools.capi import POINTER, bind, structure, union
 
@@ -256,23 +254,23 @@
     )
 
 
 def test_union_some_bindings_must_be_delayed():
     with pytest.raises(NameError, match="TBD"):
         @union
         class _:
-            previous: TBD
-            next: TBD
+            backward: TBD  # noqa: F821
+            forward: TBD   # noqa: F821
 
 
 def test_union_delayed_bindings():
     @union(autobind=False)
     class Direction:
-        backward: TBD
-        forward: TBD
+        backward: TBD  # noqa: F821
+        forward: TBD   # noqa: F821
 
     bind(Direction, locals={"TBD": POINTER[Direction]})
 
 
 def test_union_delayed_binding_with_custom_global_type_resolution():
     @structure
     class Point:
```

