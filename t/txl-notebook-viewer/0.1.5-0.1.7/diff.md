# Comparing `tmp/txl_notebook_viewer-0.1.5.tar.gz` & `tmp/txl_notebook_viewer-0.1.7.tar.gz`

## Comparing `txl_notebook_viewer-0.1.5.tar` & `txl_notebook_viewer-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.5/txl_notebook_viewer/__init__.py
--rw-r--r--   0        0        0     5126 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.5/txl_notebook_viewer/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.5/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.5/README.md
--rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.5/pyproject.toml
--rw-r--r--   0        0        0      893 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.7/txl_notebook_viewer/__init__.py
+-rw-r--r--   0        0        0     6481 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.7/txl_notebook_viewer/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.7/README.md
+-rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      893 2020-02-02 00:00:00.000000 txl_notebook_viewer-0.1.7/PKG-INFO
```

### Comparing `txl_notebook_viewer-0.1.5/txl_notebook_viewer/components.py` & `txl_notebook_viewer-0.1.7/txl_notebook_viewer/components.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,16 +1,18 @@
 from typing import Optional, Tuple
 
 from asphalt.core import Component, Context
 from rich.markdown import Markdown
 from rich.panel import Panel
 from rich.syntax import Syntax
 from rich.text import Text
+from textual import events
 from textual.widgets import DataTable
-from txl.base import Editor, Editors, Contents, FileOpenEvent
+
+from txl.base import Contents, Editor, Editors, FileOpenEvent, Kernels, NotebookFactory
 from txl.hooks import register_component
 
 
 def _line_range(
     head: Optional[int], tail: Optional[int], num_lines: int
 ) -> Optional[Tuple[int, int]]:
     if head and tail:
@@ -27,41 +29,56 @@
 
 
 class NotebookViewerMeta(type(Editor), type(DataTable)):
     pass
 
 
 class NotebookViewer(Editor, DataTable, metaclass=NotebookViewerMeta):
-    def __init__(self, contents: Contents) -> None:
+    def __init__(
+        self, contents: Contents, notebook: NotebookFactory, kernels: Kernels
+    ) -> None:
         super().__init__()
         self.contents = contents
+        self.notebook = notebook
+        self.kernels = kernels
+        self.kernel = None
+        self._row_to_cell_idx = []
+        self._selected_cell_idx = None
 
     async def on_open(self, event: FileOpenEvent) -> None:
         await self.open(event.path)
 
     async def open(self, path: str) -> None:
-        self.nb = await self.contents.get(path, type="json", on_change=self.on_change)
+        self.ynb = await self.contents.get(path, type="notebook")
+        ipynb = self.ynb.source
+        self.language = (
+            ipynb.get("metadata", {}).get("kernelspec", {}).get("language", "")
+        )
+        kernel_name = ipynb.get("metadata", {}).get("kernelspec", {}).get("name")
+        if kernel_name:
+            self.kernel = self.kernels(kernel_name)
         self.update_viewer()
+        self.ynb.observe(self.on_change)
 
     def update_viewer(self):
+        self.clear()
+
         self.add_column("", width=10)
         self.add_column("", width=100)
 
         head = None
         tail = None
-        lexer = None
-        lexer = lexer or self.nb.get("metadata", {}).get("kernelspec", {}).get(
-            "language", ""
-        )
         theme = "ansi_dark"
 
-        if "cells" not in self.nb:
+        if self.ynb.cell_number == 0:
             return
 
-        for cell in self.nb["cells"]:
+        self._row_to_cell_idx = []
+        for i_cell in range(self.ynb.cell_number):
+            cell = self.ynb.get_cell(i_cell)
             execution_count = (
                 f"[green]In [[#66ff00]{cell['execution_count'] or ' '}"
                 "[/#66ff00]]:[/green]"
                 if "execution_count" in cell
                 else ""
             )
 
@@ -70,15 +87,15 @@
             if cell["cell_type"] == "code":
                 if execution_count:
                     execution_count = "\n" + execution_count
                 line_range = _line_range(head, tail, num_lines)
                 renderable = Panel(
                     Syntax(
                         source,
-                        lexer,
+                        self.language,
                         theme=theme,
                         line_numbers=True,
                         indent_guides=True,
                         word_wrap=False,
                         line_range=line_range,
                     ),
                     border_style="dim",
@@ -86,14 +103,15 @@
                 num_lines += 2
             elif cell["cell_type"] == "markdown":
                 renderable = Markdown(source, code_theme=theme, hyperlinks=True)
             else:
                 renderable = Text(source)
 
             self.add_row(execution_count, renderable, height=num_lines)
+            self._row_to_cell_idx.append(i_cell)
 
             for output in cell.get("outputs", []):
                 output_type = output["output_type"]
                 execution_count = ""
                 if output_type == "stream":
                     text = "".join(output["text"])
                     renderable = Text.from_ansi(text)
@@ -114,34 +132,48 @@
                         text = data
                         renderable += Text.from_ansi(text)
                 else:
                     continue
 
                 num_lines = len(text.splitlines())
                 self.add_row(execution_count, renderable, height=num_lines)
+                self._row_to_cell_idx.append(i_cell)
 
-    def on_change(self, nb):
-        self.nb = nb
-        self.clear()
+    def on_click(self, event: events.Click) -> None:
+        DataTable.on_click(self, event)
+        if self.show_cursor and self.cursor_type != "none":
+            meta = self.get_style_at(event.x, event.y).meta
+            if meta:
+                self._selected_cell_idx = self._row_to_cell_idx[meta["row"]]
+
+    def on_change(self, target, event):
         self.update_viewer()
 
+    async def key_e(self) -> None:
+        if self.kernel:
+            ycell = self.ynb._ycells[self._selected_cell_idx]
+            await self.kernel.execute(self.ynb.ydoc, ycell)
+            print(f"Executed {ycell}")
+
 
 class NotebookViewerComponent(Component):
     def __init__(self, register: bool = True):
         super().__init__()
         self.register = register
 
     async def start(
         self,
         ctx: Context,
     ) -> None:
         contents = await ctx.request_resource(Contents, "contents")
+        notebook = await ctx.request_resource(NotebookFactory, "notebook")
+        kernels = await ctx.request_resource(Kernels, "kernels")
 
         def notebook_viewer_factory():
-            return NotebookViewer(contents)
+            return NotebookViewer(contents, notebook, kernels)
 
         if self.register:
             editors = await ctx.request_resource(Editors, "editors")
             editors.register_editor_factory(notebook_viewer_factory, [".ipynb"])
         else:
             notebook_viewer = notebook_viewer_factory()
             ctx.add_resource(notebook_viewer, name="notebook_viewer", types=Editor)
```

### Comparing `txl_notebook_viewer-0.1.5/LICENSE.txt` & `txl_notebook_viewer-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_notebook_viewer-0.1.5/pyproject.toml` & `txl_notebook_viewer-0.1.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `txl_notebook_viewer-0.1.5/PKG-INFO` & `txl_notebook_viewer-0.1.7/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: txl_notebook_viewer
-Version: 0.1.5
+Version: 0.1.7
 Summary: TXL plugin for a notebook viewer
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/notebook_viewer
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
```

