# Comparing `tmp/testcell-0.0.2.tar.gz` & `tmp/testcell-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "testcell-0.0.2.tar", last modified: Sat May 13 12:12:40 2023, max compression
+gzip compressed data, was "testcell-0.0.3.tar", last modified: Sat May 13 14:19:24 2023, max compression
```

## Comparing `testcell-0.0.2.tar` & `testcell-0.0.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 12:12:40.726096 testcell-0.0.2/
--rw-rw-r--   0 dldev     (1000) dldev     (1000)    11357 2023-05-01 12:51:46.000000 testcell-0.0.2/LICENSE
--rw-rw-r--   0 dldev     (1000) dldev     (1000)      111 2023-04-27 10:12:58.000000 testcell-0.0.2/MANIFEST.in
--rw-r--r--   0 dldev     (1000) dldev     (1000)     4346 2023-05-13 12:12:40.726096 testcell-0.0.2/PKG-INFO
--rw-r--r--   0 dldev     (1000) dldev     (1000)     3524 2023-05-08 10:20:53.000000 testcell-0.0.2/README.md
--rw-rw-r--   0 dldev     (1000) dldev     (1000)     1018 2023-05-13 12:06:15.000000 testcell-0.0.2/settings.ini
--rw-r--r--   0 dldev     (1000) dldev     (1000)       38 2023-05-13 12:12:40.726096 testcell-0.0.2/setup.cfg
--rw-rw-r--   0 dldev     (1000) dldev     (1000)     2596 2023-04-27 10:12:58.000000 testcell-0.0.2/setup.py
-drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 12:12:40.726096 testcell-0.0.2/testcell/
--rw-rw-r--   0 dldev     (1000) dldev     (1000)      989 2023-05-13 12:09:05.000000 testcell-0.0.2/testcell/__init__.py
--rw-rw-r--   0 dldev     (1000) dldev     (1000)     3046 2023-05-13 12:09:05.000000 testcell-0.0.2/testcell/_modidx.py
--rw-rw-r--   0 dldev     (1000) dldev     (1000)     2684 2023-05-13 12:09:05.000000 testcell-0.0.2/testcell/core.py
-drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 12:12:40.726096 testcell-0.0.2/testcell.egg-info/
--rw-r--r--   0 dldev     (1000) dldev     (1000)     4346 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/PKG-INFO
--rw-r--r--   0 dldev     (1000) dldev     (1000)      334 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/SOURCES.txt
--rw-r--r--   0 dldev     (1000) dldev     (1000)        1 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/dependency_links.txt
--rw-r--r--   0 dldev     (1000) dldev     (1000)       38 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/entry_points.txt
--rw-r--r--   0 dldev     (1000) dldev     (1000)        1 2023-05-01 13:54:05.000000 testcell-0.0.2/testcell.egg-info/not-zip-safe
--rw-r--r--   0 dldev     (1000) dldev     (1000)       25 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/requires.txt
--rw-r--r--   0 dldev     (1000) dldev     (1000)        9 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/top_level.txt
+drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 14:19:24.072882 testcell-0.0.3/
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)    11357 2023-05-01 12:51:46.000000 testcell-0.0.3/LICENSE
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)      111 2023-04-27 10:12:58.000000 testcell-0.0.3/MANIFEST.in
+-rw-r--r--   0 dldev     (1000) dldev     (1000)     5730 2023-05-13 14:19:24.072882 testcell-0.0.3/PKG-INFO
+-rw-r--r--   0 dldev     (1000) dldev     (1000)     4908 2023-05-13 14:15:36.000000 testcell-0.0.3/README.md
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)     1018 2023-05-13 14:17:06.000000 testcell-0.0.3/settings.ini
+-rw-r--r--   0 dldev     (1000) dldev     (1000)       38 2023-05-13 14:19:24.072882 testcell-0.0.3/setup.cfg
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)     2596 2023-04-27 10:12:58.000000 testcell-0.0.3/setup.py
+drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 14:19:24.072882 testcell-0.0.3/testcell/
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)     1289 2023-05-13 14:17:44.000000 testcell-0.0.3/testcell/__init__.py
+-rw-r--r--   0 dldev     (1000) dldev     (1000)     1506 2023-05-13 14:17:44.000000 testcell-0.0.3/testcell/_modidx.py
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)     2684 2023-05-13 14:17:44.000000 testcell-0.0.3/testcell/core.py
+drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 14:19:24.072882 testcell-0.0.3/testcell.egg-info/
+-rw-r--r--   0 dldev     (1000) dldev     (1000)     5730 2023-05-13 14:19:24.000000 testcell-0.0.3/testcell.egg-info/PKG-INFO
+-rw-r--r--   0 dldev     (1000) dldev     (1000)      334 2023-05-13 14:19:24.000000 testcell-0.0.3/testcell.egg-info/SOURCES.txt
+-rw-r--r--   0 dldev     (1000) dldev     (1000)        1 2023-05-13 14:19:24.000000 testcell-0.0.3/testcell.egg-info/dependency_links.txt
+-rw-r--r--   0 dldev     (1000) dldev     (1000)       38 2023-05-13 14:19:24.000000 testcell-0.0.3/testcell.egg-info/entry_points.txt
+-rw-r--r--   0 dldev     (1000) dldev     (1000)        1 2023-05-01 13:54:05.000000 testcell-0.0.3/testcell.egg-info/not-zip-safe
+-rw-r--r--   0 dldev     (1000) dldev     (1000)       25 2023-05-13 14:19:24.000000 testcell-0.0.3/testcell.egg-info/requires.txt
+-rw-r--r--   0 dldev     (1000) dldev     (1000)        9 2023-05-13 14:19:24.000000 testcell-0.0.3/testcell.egg-info/top_level.txt
```

### Comparing `testcell-0.0.2/LICENSE` & `testcell-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `testcell-0.0.2/PKG-INFO` & `testcell-0.0.3/README.md`

 * *Files 19% similar despite different names*

```diff
@@ -1,29 +1,7 @@
-Metadata-Version: 2.1
-Name: testcell
-Version: 0.0.2
-Summary: testcell prevents your testing cells from affecting the global namespace
-Home-page: https://github.com/artste/testcell
-Author: Stefano Giomo
-Author-email: artste@users.noreply.github.com
-License: Apache Software License 2.0
-Keywords: nbdev jupyter notebook python
-Classifier: Development Status :: 4 - Beta
-Classifier: Intended Audience :: Developers
-Classifier: Natural Language :: English
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: License :: OSI Approved :: Apache Software License
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-Provides-Extra: dev
-License-File: LICENSE
-
 # testcell
 
 <!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! -->
 
 **TL;DR**: `%%testcell` prevents your testing cells from affecting the
 global namespace.
 
@@ -74,15 +52,17 @@
 ```
 
 
     ### BEGIN
     def _test_cell_():
         #| echo: false
         a = "'a' is not polluting global scope"
-        display(a)
+        display( # %%testcell
+        a
+        ) # %%testcell
     try:
         _test_cell_()
     finally:
         del _test_cell_
     ### END
 
     "'a' is not polluting global scope"
@@ -97,15 +77,17 @@
 ```
 
 
     ### BEGIN
     def _test_cell_():
         #| echo: false
         a = "'a' is not polluting global scope"
-        display(a)
+        display( # %%testcell
+        a
+        ) # %%testcell
     try:
         _test_cell_()
     finally:
         del _test_cell_
     ### END
 
 On top of *wrapping* your cell’s code, it will optinally add a
@@ -151,17 +133,91 @@
     try:
         _test_cell_()
     finally:
         del _test_cell_
     ### END
     'a' is not polluting global scope
 
+### Run in isolation
+
+`%%testcelln` is a shourtcut for `%%testcell noglobals` and executes the
+cell in complete isolation from global scope. This is very useful when
+you want to be sure that global variables or namespace should be part of
+the cell.
+
+## Run in isolation
+
+`%%testcelln` is a shortcut for `%%testcell noglobals` and executes the
+cell in complete isolation from the global scope.
+
+This is very useful when you want to ensure that global variables or
+namespaces are not accessible within the cell.
+
+``` python
+aaa = 'global variable'
+```
+
+``` python
+%%testcell
+'aaa' in globals()
+```
+
+    True
+
+``` python
+%%testcell noglobals
+'aaa' in globals()
+```
+
+    False
+
+``` python
+%%testcelln
+'aaa' in globals()
+```
+
+    False
+
+``` python
+%%testcelln
+globals().keys()
+```
+
+    dict_keys(['__builtins__', '_test_cell_'])
+
+Inside the cell, from the *global scope*, only these two items are
+available: + `__builtins__` : built in python’s functions. +
+`_test_cell_` : `%%testcell` wrapped function executed (we can’t avoid
+this).
+
 **IMPORTANT**: this is *just wrapping your cell* and so it’s still
 running on your main kernel. If you modify variables that has been
 created outside of this cell (aka: if you have side effects) this will
 not protect you.
 
+``` python
+aaa
+```
+
+    'global variable'
+
+``` python
+%%testcell 
+# WARNING: this will alter the state of global variable:
+globals().update({'aaa' : 'modified global variable'});
+```
+
+``` python
+aaa
+```
+
+    'modified global variable'
+
+``` python
+del aaa
+```
+
 ## TODO:
 
 - Install as a plugin to enable it by default like other cell’s magic.
 - Eval possibility to run code on a new kernel to reduce even more
   possible side effects.
```

### Comparing `testcell-0.0.2/settings.ini` & `testcell-0.0.3/settings.ini`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 [DEFAULT]
 # All sections below are required unless otherwise specified.
 # See https://github.com/fastai/nbdev/blob/master/settings.ini for examples.
 
 ### Python library ###
 repo = testcell
 lib_name = %(repo)s
-version = 0.0.2
+version = 0.0.3
 min_python = 3.7
 license = apache2
 black_formatting = False
 
 ### nbdev ###
 doc_path = _docs
 lib_path = testcell
```

### Comparing `testcell-0.0.2/setup.py` & `testcell-0.0.3/setup.py`

 * *Files identical despite different names*

### Comparing `testcell-0.0.2/testcell/core.py` & `testcell-0.0.3/testcell/core.py`

 * *Files identical despite different names*

### Comparing `testcell-0.0.2/testcell.egg-info/PKG-INFO` & `testcell-0.0.3/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: testcell
-Version: 0.0.2
+Version: 0.0.3
 Summary: testcell prevents your testing cells from affecting the global namespace
 Home-page: https://github.com/artste/testcell
 Author: Stefano Giomo
 Author-email: artste@users.noreply.github.com
 License: Apache Software License 2.0
 Keywords: nbdev jupyter notebook python
 Classifier: Development Status :: 4 - Beta
@@ -74,15 +74,17 @@
 ```
 
 
     ### BEGIN
     def _test_cell_():
         #| echo: false
         a = "'a' is not polluting global scope"
-        display(a)
+        display( # %%testcell
+        a
+        ) # %%testcell
     try:
         _test_cell_()
     finally:
         del _test_cell_
     ### END
 
     "'a' is not polluting global scope"
@@ -97,15 +99,17 @@
 ```
 
 
     ### BEGIN
     def _test_cell_():
         #| echo: false
         a = "'a' is not polluting global scope"
-        display(a)
+        display( # %%testcell
+        a
+        ) # %%testcell
     try:
         _test_cell_()
     finally:
         del _test_cell_
     ### END
 
 On top of *wrapping* your cell’s code, it will optinally add a
@@ -151,17 +155,91 @@
     try:
         _test_cell_()
     finally:
         del _test_cell_
     ### END
     'a' is not polluting global scope
 
+### Run in isolation
+
+`%%testcelln` is a shourtcut for `%%testcell noglobals` and executes the
+cell in complete isolation from global scope. This is very useful when
+you want to be sure that global variables or namespace should be part of
+the cell.
+
+## Run in isolation
+
+`%%testcelln` is a shortcut for `%%testcell noglobals` and executes the
+cell in complete isolation from the global scope.
+
+This is very useful when you want to ensure that global variables or
+namespaces are not accessible within the cell.
+
+``` python
+aaa = 'global variable'
+```
+
+``` python
+%%testcell
+'aaa' in globals()
+```
+
+    True
+
+``` python
+%%testcell noglobals
+'aaa' in globals()
+```
+
+    False
+
+``` python
+%%testcelln
+'aaa' in globals()
+```
+
+    False
+
+``` python
+%%testcelln
+globals().keys()
+```
+
+    dict_keys(['__builtins__', '_test_cell_'])
+
+Inside the cell, from the *global scope*, only these two items are
+available: + `__builtins__` : built in python’s functions. +
+`_test_cell_` : `%%testcell` wrapped function executed (we can’t avoid
+this).
+
 **IMPORTANT**: this is *just wrapping your cell* and so it’s still
 running on your main kernel. If you modify variables that has been
 created outside of this cell (aka: if you have side effects) this will
 not protect you.
 
+``` python
+aaa
+```
+
+    'global variable'
+
+``` python
+%%testcell 
+# WARNING: this will alter the state of global variable:
+globals().update({'aaa' : 'modified global variable'});
+```
+
+``` python
+aaa
+```
+
+    'modified global variable'
+
+``` python
+del aaa
+```
+
 ## TODO:
 
 - Install as a plugin to enable it by default like other cell’s magic.
 - Eval possibility to run code on a new kernel to reduce even more
   possible side effects.
```

