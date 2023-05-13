# Comparing `tmp/strongtyping-3.9.1.tar.gz` & `tmp/strongtyping-3.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "strongtyping-3.9.1.tar", last modified: Sun Aug 14 16:53:39 2022, max compression
+gzip compressed data, was "strongtyping-3.9.2.tar", last modified: Sat Aug 27 13:39:57 2022, max compression
```

## Comparing `strongtyping-3.9.1.tar` & `strongtyping-3.9.2.tar`

### file list

```diff
@@ -1,30 +1,30 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-14 16:53:39.596718 strongtyping-3.9.1/
--rw-r--r--   0 runner    (1001) docker     (121)     1804 2022-08-14 16:53:39.596718 strongtyping-3.9.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     1210 2022-08-14 16:53:29.000000 strongtyping-3.9.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-14 16:53:39.592718 strongtyping-3.9.1/easy_property/
--rw-r--r--   0 runner    (1001) docker     (121)     1250 2022-08-14 16:53:29.000000 strongtyping-3.9.1/easy_property/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      498 2022-08-14 16:53:29.000000 strongtyping-3.9.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-08-14 16:53:39.596718 strongtyping-3.9.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)      947 2022-08-14 16:53:29.000000 strongtyping-3.9.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-14 16:53:39.596718 strongtyping-3.9.1/strongtyping/
--rw-r--r--   0 runner    (1001) docker     (121)      250 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     3848 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/_utils.py
--rw-r--r--   0 runner    (1001) docker     (121)      658 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/cached_dict.py
--rw-r--r--   0 runner    (1001) docker     (121)      652 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/cached_set.py
--rw-r--r--   0 runner    (1001) docker     (121)      386 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/config.py
--rw-r--r--   0 runner    (1001) docker     (121)    11058 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/docs_from_typing.py
--rw-r--r--   0 runner    (1001) docker     (121)     8242 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/docstring_typing.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-14 16:53:39.596718 strongtyping-3.9.1/strongtyping/easy_property/
--rw-r--r--   0 runner    (1001) docker     (121)     1239 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/easy_property/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1872 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/mypy.py
--rw-r--r--   0 runner    (1001) docker     (121)     8503 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/strong_typing.py
--rw-r--r--   0 runner    (1001) docker     (121)    19400 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/strong_typing_utils.py
--rw-r--r--   0 runner    (1001) docker     (121)     7008 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/type_namedtuple.py
--rw-r--r--   0 runner    (1001) docker     (121)     5881 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping/types.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-14 16:53:39.596718 strongtyping-3.9.1/strongtyping-stubs/
--rw-r--r--   0 runner    (1001) docker     (121)       47 2022-08-14 16:53:29.000000 strongtyping-3.9.1/strongtyping-stubs/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-14 16:53:39.596718 strongtyping-3.9.1/strongtyping.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     1804 2022-08-14 16:53:39.000000 strongtyping-3.9.1/strongtyping.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      606 2022-08-14 16:53:39.000000 strongtyping-3.9.1/strongtyping.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-08-14 16:53:39.000000 strongtyping-3.9.1/strongtyping.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       46 2022-08-14 16:53:39.000000 strongtyping-3.9.1/strongtyping.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-27 13:39:57.530604 strongtyping-3.9.2/
+-rw-r--r--   0 runner    (1001) docker     (121)     1810 2022-08-27 13:39:57.530604 strongtyping-3.9.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     1210 2022-08-27 13:39:47.000000 strongtyping-3.9.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-27 13:39:57.526604 strongtyping-3.9.2/easy_property/
+-rw-r--r--   0 runner    (1001) docker     (121)     1250 2022-08-27 13:39:47.000000 strongtyping-3.9.2/easy_property/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      498 2022-08-27 13:39:47.000000 strongtyping-3.9.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-08-27 13:39:57.530604 strongtyping-3.9.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)      953 2022-08-27 13:39:47.000000 strongtyping-3.9.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-27 13:39:57.530604 strongtyping-3.9.2/strongtyping/
+-rw-r--r--   0 runner    (1001) docker     (121)      250 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3848 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/_utils.py
+-rw-r--r--   0 runner    (1001) docker     (121)      658 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/cached_dict.py
+-rw-r--r--   0 runner    (1001) docker     (121)      652 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/cached_set.py
+-rw-r--r--   0 runner    (1001) docker     (121)      386 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/config.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11058 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/docs_from_typing.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8242 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/docstring_typing.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-27 13:39:57.530604 strongtyping-3.9.2/strongtyping/easy_property/
+-rw-r--r--   0 runner    (1001) docker     (121)     1239 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/easy_property/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1872 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/mypy.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8503 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/strong_typing.py
+-rw-r--r--   0 runner    (1001) docker     (121)    19400 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/strong_typing_utils.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7008 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/type_namedtuple.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5881 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping/types.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-27 13:39:57.530604 strongtyping-3.9.2/strongtyping-stubs/
+-rw-r--r--   0 runner    (1001) docker     (121)       47 2022-08-27 13:39:47.000000 strongtyping-3.9.2/strongtyping-stubs/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-27 13:39:57.530604 strongtyping-3.9.2/strongtyping.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     1810 2022-08-27 13:39:57.000000 strongtyping-3.9.2/strongtyping.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      606 2022-08-27 13:39:57.000000 strongtyping-3.9.2/strongtyping.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-08-27 13:39:57.000000 strongtyping-3.9.2/strongtyping.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       46 2022-08-27 13:39:57.000000 strongtyping-3.9.2/strongtyping.egg-info/top_level.txt
```

### Comparing `strongtyping-3.9.1/PKG-INFO` & `strongtyping-3.9.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: strongtyping
-Version: 3.9.1
+Version: 3.9.2
 Summary: Decorator which checks whether the function is called with the correct type of parameters
 Home-page: https://strongtyping.readthedocs.io/en/latest/
 Author: FelixTheC
 Author-email: fberndt87@gmail.com
 License: MIT
 Description: [![PyPI version](https://badge.fury.io/py/strongtyping.svg)](https://badge.fury.io/py/strongtyping)
         ![Python application](https://github.com/FelixTheC/strongtyping/workflows/Python%20application/badge.svg)
@@ -21,9 +21,9 @@
         And <b><em>raises</em> TypeMisMatch</b> if the used parameters in a function call where invalid.</p>
         
         ## [Docs have been moved to 'readthedocs'](https://strongtyping.readthedocs.io/en/latest/#the-solution)
         
 Platform: UNKNOWN
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.9
-Requires-Python: ==3.9
+Requires-Python: >=3.9,<3.10
 Description-Content-Type: text/markdown
```

### Comparing `strongtyping-3.9.1/README.md` & `strongtyping-3.9.2/README.md`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/easy_property/__init__.py` & `strongtyping-3.9.2/easy_property/__init__.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/setup.py` & `strongtyping-3.9.2/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,23 +14,23 @@
 # The text of the README file
 README = (HERE / "README.md").read_text()
 
 packages = find_packages(exclude=["test_*", "*.tests"])
 
 setup(
     name="strongtyping",
-    version="3.9.1",
+    version="3.9.2",
     description="Decorator which checks whether the function is called with the correct type of parameters",
     long_description=README,
     long_description_content_type="text/markdown",
     url="https://strongtyping.readthedocs.io/en/latest/",
     author="FelixTheC",
     author_email="fberndt87@gmail.com",
     license="MIT",
     classifiers=[
         "License :: OSI Approved :: MIT License",
         "Programming Language :: Python :: 3.9",
     ],
     packages=packages,
-    python_requires="==3.9",
+    python_requires=">=3.9,<3.10",
     include_package_data=True,
 )
```

### Comparing `strongtyping-3.9.1/strongtyping/_utils.py` & `strongtyping-3.9.2/strongtyping/_utils.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/cached_dict.py` & `strongtyping-3.9.2/strongtyping/cached_dict.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/cached_set.py` & `strongtyping-3.9.2/strongtyping/cached_set.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/docs_from_typing.py` & `strongtyping-3.9.2/strongtyping/docs_from_typing.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/docstring_typing.py` & `strongtyping-3.9.2/strongtyping/docstring_typing.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/easy_property/__init__.py` & `strongtyping-3.9.2/strongtyping/easy_property/__init__.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/mypy.py` & `strongtyping-3.9.2/strongtyping/mypy.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/strong_typing.py` & `strongtyping-3.9.2/strongtyping/strong_typing.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/strong_typing_utils.py` & `strongtyping-3.9.2/strongtyping/strong_typing_utils.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/type_namedtuple.py` & `strongtyping-3.9.2/strongtyping/type_namedtuple.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping/types.py` & `strongtyping-3.9.2/strongtyping/types.py`

 * *Files identical despite different names*

### Comparing `strongtyping-3.9.1/strongtyping.egg-info/PKG-INFO` & `strongtyping-3.9.2/strongtyping.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: strongtyping
-Version: 3.9.1
+Version: 3.9.2
 Summary: Decorator which checks whether the function is called with the correct type of parameters
 Home-page: https://strongtyping.readthedocs.io/en/latest/
 Author: FelixTheC
 Author-email: fberndt87@gmail.com
 License: MIT
 Description: [![PyPI version](https://badge.fury.io/py/strongtyping.svg)](https://badge.fury.io/py/strongtyping)
         ![Python application](https://github.com/FelixTheC/strongtyping/workflows/Python%20application/badge.svg)
@@ -21,9 +21,9 @@
         And <b><em>raises</em> TypeMisMatch</b> if the used parameters in a function call where invalid.</p>
         
         ## [Docs have been moved to 'readthedocs'](https://strongtyping.readthedocs.io/en/latest/#the-solution)
         
 Platform: UNKNOWN
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.9
-Requires-Python: ==3.9
+Requires-Python: >=3.9,<3.10
 Description-Content-Type: text/markdown
```

### Comparing `strongtyping-3.9.1/strongtyping.egg-info/SOURCES.txt` & `strongtyping-3.9.2/strongtyping.egg-info/SOURCES.txt`

 * *Files identical despite different names*

