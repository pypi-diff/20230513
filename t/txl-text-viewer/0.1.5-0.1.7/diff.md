# Comparing `tmp/txl_text_viewer-0.1.5.tar.gz` & `tmp/txl_text_viewer-0.1.7.tar.gz`

## Comparing `txl_text_viewer-0.1.5.tar` & `txl_text_viewer-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.5/txl_text_viewer/__init__.py
--rw-r--r--   0        0        0     2217 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.5/txl_text_viewer/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.5/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.5/README.md
--rw-r--r--   0        0        0     1027 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.5/pyproject.toml
--rw-r--r--   0        0        0      877 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.7/txl_text_viewer/__init__.py
+-rw-r--r--   0        0        0     2299 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.7/txl_text_viewer/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.7/README.md
+-rw-r--r--   0        0        0     1027 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      877 2020-02-02 00:00:00.000000 txl_text_viewer-0.1.7/PKG-INFO
```

### Comparing `txl_text_viewer-0.1.5/txl_text_viewer/components.py` & `txl_text_viewer-0.1.7/txl_text_viewer/components.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 from asphalt.core import Component, Context
 from rich.syntax import Syntax
 from rich.traceback import Traceback
 from textual.widgets import Static
-from txl.base import Editor, Editors, Contents, FileOpenEvent
+
+from txl.base import Contents, Editor, Editors, FileOpenEvent
 from txl.hooks import register_component
 
 
 class TextViewerMeta(type(Editor), type(Static)):
     pass
 
 
@@ -21,16 +22,18 @@
         self.contents = contents
 
     async def on_open(self, event: FileOpenEvent) -> None:
         await self.open(event.path)
 
     async def open(self, path: str) -> None:
         self.path = path
-        self.text = await self.contents.get(path, type="text", on_change=self.on_change)
+        self.ytext = await self.contents.get(path, type="unicode")
+        self.text = self.ytext.source
         self.update_viewer()
+        self.ytext.observe(self.on_change)
 
     def update_viewer(self):
         try:
             lexer = Syntax.guess_lexer(self.path, code=self.text)
             syntax = Syntax(
                 self.text,
                 lexer=lexer,
@@ -44,16 +47,16 @@
         else:
             self.update(syntax)
             self.sub_title = self.path
 
     def on_mount(self):
         self.expand
 
-    def on_change(self, text):
-        self.text = text
+    def on_change(self, target, event):
+        self.text = self.ytext.source
         self.update_viewer()
 
 
 class TextViewerComponent(Component):
     def __init__(self, register: bool = True):
         super().__init__()
         self.register = register
```

### Comparing `txl_text_viewer-0.1.5/LICENSE.txt` & `txl_text_viewer-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_text_viewer-0.1.5/pyproject.toml` & `txl_text_viewer-0.1.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `txl_text_viewer-0.1.5/PKG-INFO` & `txl_text_viewer-0.1.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: txl_text_viewer
-Version: 0.1.5
+Version: 0.1.7
 Summary: TXL plugin for a text viewer
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/text_viewer
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
```

