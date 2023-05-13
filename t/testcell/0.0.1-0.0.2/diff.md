# Comparing `tmp/testcell-0.0.1.tar.gz` & `tmp/testcell-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "testcell-0.0.1.tar", last modified: Sun May  7 15:37:23 2023, max compression
+gzip compressed data, was "testcell-0.0.2.tar", last modified: Sat May 13 12:12:40 2023, max compression
```

## Comparing `testcell-0.0.1.tar` & `testcell-0.0.2.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-07 15:37:23.535862 testcell-0.0.1/
--rw-rw-r--   0 dldev     (1000) dldev     (1000)    11357 2023-05-01 12:51:46.000000 testcell-0.0.1/LICENSE
--rw-rw-r--   0 dldev     (1000) dldev     (1000)      111 2023-04-27 10:12:58.000000 testcell-0.0.1/MANIFEST.in
--rw-r--r--   0 dldev     (1000) dldev     (1000)     4346 2023-05-07 15:37:23.535862 testcell-0.0.1/PKG-INFO
--rw-r--r--   0 dldev     (1000) dldev     (1000)     3524 2023-05-07 15:22:51.000000 testcell-0.0.1/README.md
--rw-r--r--   0 dldev     (1000) dldev     (1000)     1018 2023-05-07 07:30:36.000000 testcell-0.0.1/settings.ini
--rw-r--r--   0 dldev     (1000) dldev     (1000)       38 2023-05-07 15:37:23.535862 testcell-0.0.1/setup.cfg
--rw-rw-r--   0 dldev     (1000) dldev     (1000)     2596 2023-04-27 10:12:58.000000 testcell-0.0.1/setup.py
-drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-07 15:37:23.535862 testcell-0.0.1/testcell/
--rw-r--r--   0 dldev     (1000) dldev     (1000)      989 2023-05-07 15:22:50.000000 testcell-0.0.1/testcell/__init__.py
--rw-r--r--   0 dldev     (1000) dldev     (1000)     1398 2023-05-07 15:22:50.000000 testcell-0.0.1/testcell/_modidx.py
--rw-r--r--   0 dldev     (1000) dldev     (1000)     2329 2023-05-07 15:22:50.000000 testcell-0.0.1/testcell/core.py
-drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-07 15:37:23.535862 testcell-0.0.1/testcell.egg-info/
--rw-r--r--   0 dldev     (1000) dldev     (1000)     4346 2023-05-07 15:37:23.000000 testcell-0.0.1/testcell.egg-info/PKG-INFO
--rw-r--r--   0 dldev     (1000) dldev     (1000)      334 2023-05-07 15:37:23.000000 testcell-0.0.1/testcell.egg-info/SOURCES.txt
--rw-r--r--   0 dldev     (1000) dldev     (1000)        1 2023-05-07 15:37:23.000000 testcell-0.0.1/testcell.egg-info/dependency_links.txt
--rw-r--r--   0 dldev     (1000) dldev     (1000)       38 2023-05-07 15:37:23.000000 testcell-0.0.1/testcell.egg-info/entry_points.txt
--rw-r--r--   0 dldev     (1000) dldev     (1000)        1 2023-05-01 13:54:05.000000 testcell-0.0.1/testcell.egg-info/not-zip-safe
--rw-r--r--   0 dldev     (1000) dldev     (1000)       25 2023-05-07 15:37:23.000000 testcell-0.0.1/testcell.egg-info/requires.txt
--rw-r--r--   0 dldev     (1000) dldev     (1000)        9 2023-05-07 15:37:23.000000 testcell-0.0.1/testcell.egg-info/top_level.txt
+drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 12:12:40.726096 testcell-0.0.2/
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)    11357 2023-05-01 12:51:46.000000 testcell-0.0.2/LICENSE
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)      111 2023-04-27 10:12:58.000000 testcell-0.0.2/MANIFEST.in
+-rw-r--r--   0 dldev     (1000) dldev     (1000)     4346 2023-05-13 12:12:40.726096 testcell-0.0.2/PKG-INFO
+-rw-r--r--   0 dldev     (1000) dldev     (1000)     3524 2023-05-08 10:20:53.000000 testcell-0.0.2/README.md
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)     1018 2023-05-13 12:06:15.000000 testcell-0.0.2/settings.ini
+-rw-r--r--   0 dldev     (1000) dldev     (1000)       38 2023-05-13 12:12:40.726096 testcell-0.0.2/setup.cfg
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)     2596 2023-04-27 10:12:58.000000 testcell-0.0.2/setup.py
+drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 12:12:40.726096 testcell-0.0.2/testcell/
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)      989 2023-05-13 12:09:05.000000 testcell-0.0.2/testcell/__init__.py
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)     3046 2023-05-13 12:09:05.000000 testcell-0.0.2/testcell/_modidx.py
+-rw-rw-r--   0 dldev     (1000) dldev     (1000)     2684 2023-05-13 12:09:05.000000 testcell-0.0.2/testcell/core.py
+drwxr-xr-x   0 dldev     (1000) dldev     (1000)        0 2023-05-13 12:12:40.726096 testcell-0.0.2/testcell.egg-info/
+-rw-r--r--   0 dldev     (1000) dldev     (1000)     4346 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/PKG-INFO
+-rw-r--r--   0 dldev     (1000) dldev     (1000)      334 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/SOURCES.txt
+-rw-r--r--   0 dldev     (1000) dldev     (1000)        1 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/dependency_links.txt
+-rw-r--r--   0 dldev     (1000) dldev     (1000)       38 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/entry_points.txt
+-rw-r--r--   0 dldev     (1000) dldev     (1000)        1 2023-05-01 13:54:05.000000 testcell-0.0.2/testcell.egg-info/not-zip-safe
+-rw-r--r--   0 dldev     (1000) dldev     (1000)       25 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/requires.txt
+-rw-r--r--   0 dldev     (1000) dldev     (1000)        9 2023-05-13 12:12:40.000000 testcell-0.0.2/testcell.egg-info/top_level.txt
```

### Comparing `testcell-0.0.1/LICENSE` & `testcell-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `testcell-0.0.1/PKG-INFO` & `testcell-0.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: testcell
-Version: 0.0.1
+Version: 0.0.2
 Summary: testcell prevents your testing cells from affecting the global namespace
 Home-page: https://github.com/artste/testcell
 Author: Stefano Giomo
 Author-email: artste@users.noreply.github.com
 License: Apache Software License 2.0
 Keywords: nbdev jupyter notebook python
 Classifier: Development Status :: 4 - Beta
```

### Comparing `testcell-0.0.1/README.md` & `testcell-0.0.2/README.md`

 * *Files identical despite different names*

### Comparing `testcell-0.0.1/settings.ini` & `testcell-0.0.2/settings.ini`

 * *Files 14% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 [DEFAULT]
 # All sections below are required unless otherwise specified.
 # See https://github.com/fastai/nbdev/blob/master/settings.ini for examples.
 
 ### Python library ###
 repo = testcell
 lib_name = %(repo)s
-version = 0.0.1
+version = 0.0.2
 min_python = 3.7
 license = apache2
 black_formatting = False
 
 ### nbdev ###
 doc_path = _docs
 lib_path = testcell
```

### Comparing `testcell-0.0.1/setup.py` & `testcell-0.0.2/setup.py`

 * *Files identical despite different names*

### Comparing `testcell-0.0.1/testcell/__init__.py` & `testcell-0.0.2/testcell/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-__version__ = "0.0.1"
+__version__ = "0.0.2"
 # AUTOGENERATED! DO NOT EDIT! File to edit: ../nbs/02_testcell.ipynb.
 
 # %% auto 0
 __all__ = ['testcell']
 
 # %% ../nbs/02_testcell.ipynb 4
 import ast
```

### Comparing `testcell-0.0.1/testcell/core.py` & `testcell-0.0.2/testcell/core.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # AUTOGENERATED! DO NOT EDIT! File to edit: ../nbs/01_ast.ipynb.
 
 # %% auto 0
-__all__ = ['last_node', 'node_source', 'is_assignment', 'is_function_call', 'is_import_statement', 'need_display', 'wrap_node',
-           'last_statement_has_semicolon', 'code_till_node', 'auto_display']
+__all__ = ['last_node', 'node_source', 'is_assignment', 'extract_call', 'is_function_call', 'is_import_statement', 'need_display',
+           'wrap_node', 'last_statement_has_semicolon', 'code_till_node', 'auto_display']
 
 # %% ../nbs/01_ast.ipynb 3
 import ast
 
 # %% ../nbs/01_ast.ipynb 5
 def last_node(code):
     tree = ast.parse(code)
@@ -21,56 +21,65 @@
     return ast.get_source_segment(code,node)
 
 # %% ../nbs/01_ast.ipynb 9
 def is_assignment(node):
     return isinstance(node, ast.Assign)
 
 # %% ../nbs/01_ast.ipynb 11
+def extract_call(node):
+    if not isinstance(node, ast.Expr): return None
+    node = node.value # step in
+    if isinstance(node, ast.Name): return None # "fn"
+    if isinstance(node, ast.Call):
+        n = node.func # step in
+        if isinstance(n, ast.Name): return n.id # "fn()"
+        if isinstance(n, ast.Attribute): return n.attr
+    return None # all the rest is not supported
+
+# %% ../nbs/01_ast.ipynb 13
 def is_function_call(node,names):
-    if not isinstance(node, ast.Expr): return False # this is not a function call
-    node = node.value # step in
-    if not hasattr(node,'func'): return False
-    function_name = node.func.id
+    function_name = extract_call(node)
+    if function_name is None: return False # this is not a function call
     return function_name in names
 
-# %% ../nbs/01_ast.ipynb 13
+# %% ../nbs/01_ast.ipynb 15
 def is_import_statement(node):
     return isinstance(node, (ast.Import, ast.ImportFrom))
 
-# %% ../nbs/01_ast.ipynb 15
+# %% ../nbs/01_ast.ipynb 17
 def need_display(node):
     if node is None: return False
     if is_function_call(node,names=['print','display']): return False
     if is_import_statement(node): return False
     return True
 
-# %% ../nbs/01_ast.ipynb 17
+# %% ../nbs/01_ast.ipynb 19
 def wrap_node(node,function_name):
     return ast.Expr(
         value=ast.Call(
             func=ast.Name(id=function_name, ctx=ast.Load()),
             args=[node],
             keywords=[])
         )
 
-# %% ../nbs/01_ast.ipynb 20
+# %% ../nbs/01_ast.ipynb 22
 def last_statement_has_semicolon(code):
     t = [x.strip() for x in code.splitlines()]
     t = [x for x in t if not x.startswith('#')]
     return t[-1].endswith(';')
 
-# %% ../nbs/01_ast.ipynb 22
+# %% ../nbs/01_ast.ipynb 24
 def code_till_node(code:str,node):
     t = code.splitlines()
     t = t[:node.lineno]
     t[-1] = t[-1][:node.col_offset]
     if len(t[-1])==0: t = t[:-1]
     return '\n'.join(t)
 
-# %% ../nbs/01_ast.ipynb 25
+# %% ../nbs/01_ast.ipynb 27
 def auto_display(code):
     if last_statement_has_semicolon(code): return code
     
     n = last_node(code)
     if not need_display(n): return code
     
     ns = node_source(n,code)
```

### Comparing `testcell-0.0.1/testcell.egg-info/PKG-INFO` & `testcell-0.0.2/testcell.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: testcell
-Version: 0.0.1
+Version: 0.0.2
 Summary: testcell prevents your testing cells from affecting the global namespace
 Home-page: https://github.com/artste/testcell
 Author: Stefano Giomo
 Author-email: artste@users.noreply.github.com
 License: Apache Software License 2.0
 Keywords: nbdev jupyter notebook python
 Classifier: Development Status :: 4 - Beta
```

