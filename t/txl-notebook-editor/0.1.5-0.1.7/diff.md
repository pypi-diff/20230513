# Comparing `tmp/txl_notebook_editor-0.1.5.tar.gz` & `tmp/txl_notebook_editor-0.1.7.tar.gz`

## Comparing `txl_notebook_editor-0.1.5.tar` & `txl_notebook_editor-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.5/txl_notebook_editor/__init__.py
--rw-r--r--   0        0        0     2016 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.5/txl_notebook_editor/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.5/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.5/README.md
--rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.5/pyproject.toml
--rw-r--r--   0        0        0      917 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.7/txl_notebook_editor/__init__.py
+-rw-r--r--   0        0        0     2017 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.7/txl_notebook_editor/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.7/README.md
+-rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      917 2020-02-02 00:00:00.000000 txl_notebook_editor-0.1.7/PKG-INFO
```

### Comparing `txl_notebook_editor-0.1.5/txl_notebook_editor/components.py` & `txl_notebook_editor-0.1.7/txl_notebook_editor/components.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from asphalt.core import Component, Context
 from textual.binding import Binding
 from textual.containers import Container
-from txl.base import CellFactory, Editor, Editors, Contents, FileOpenEvent
+
+from txl.base import CellFactory, Contents, Editor, Editors, FileOpenEvent
 from txl.hooks import register_component
 
 
 class NotebookEditorMeta(type(Editor), type(Container)):
     pass
```

### Comparing `txl_notebook_editor-0.1.5/LICENSE.txt` & `txl_notebook_editor-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_notebook_editor-0.1.5/pyproject.toml` & `txl_notebook_editor-0.1.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `txl_notebook_editor-0.1.5/PKG-INFO` & `txl_notebook_editor-0.1.7/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: txl_notebook_editor
-Version: 0.1.5
+Version: 0.1.7
 Summary: TXL plugin for a notebook editor
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/notebook_editor
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
```

