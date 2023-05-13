# Comparing `tmp/txl_widgets-0.1.14.tar.gz` & `tmp/txl_widgets-0.1.7.tar.gz`

## Comparing `txl_widgets-0.1.14.tar` & `txl_widgets-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       23 2020-02-02 00:00:00.000000 txl_widgets-0.1.14/txl_widgets/__init__.py
--rw-r--r--   0        0        0     1971 2020-02-02 00:00:00.000000 txl_widgets-0.1.14/txl_widgets/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_widgets-0.1.14/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_widgets-0.1.14/LICENSE.txt
--rw-r--r--   0        0        0       25 2020-02-02 00:00:00.000000 txl_widgets-0.1.14/README.md
--rw-r--r--   0        0        0      957 2020-02-02 00:00:00.000000 txl_widgets-0.1.14/pyproject.toml
--rw-r--r--   0        0        0      790 2020-02-02 00:00:00.000000 txl_widgets-0.1.14/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_widgets-0.1.7/txl_widgets/__init__.py
+-rw-r--r--   0        0        0     2100 2020-02-02 00:00:00.000000 txl_widgets-0.1.7/txl_widgets/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_widgets-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_widgets-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       25 2020-02-02 00:00:00.000000 txl_widgets-0.1.7/README.md
+-rw-r--r--   0        0        0     1033 2020-02-02 00:00:00.000000 txl_widgets-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      897 2020-02-02 00:00:00.000000 txl_widgets-0.1.7/PKG-INFO
```

### Comparing `txl_widgets-0.1.14/txl_widgets/components.py` & `txl_widgets-0.1.7/txl_widgets/components.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,68 +1,62 @@
+import asyncio
 import pkg_resources
-import y_py as Y
+from functools import partial
+
 from asphalt.core import Component, Context
-from ypywidgets.utils import (
-    YMessageType,
-    YSyncMessageType,
-    create_update_message,
-    process_sync_message,
-    sync,
-)
 
+from txl.hooks import register_component
 from txl.base import Kernels, Widgets
+from ypywidgets.yutils import YMessageType, YSyncMessageType, create_update_message, process_sync_message, put_updates, sync
 
 
 class _Widgets:
+
     def __init__(self):
-        self.ydocs = {
-            ep.name: ep.load()
-            for ep in pkg_resources.iter_entry_points(group="ypywidgets")
-        }
+        self.ydocs = {ep.name: ep.load() for ep in pkg_resources.iter_entry_points(group="ypywidgets")}
         self.widgets = {}
+        self._update_queue = asyncio.Queue()  # FIXME: one per widget
+        self.synced = asyncio.Event()  # FIXME
 
     def comm_open(self, msg, comm) -> None:
-        target_name = msg["content"]["target_name"]
-        if target_name != "ywidget":
-            return
-
-        name = msg["metadata"]["ymodel_name"]
+        name = msg["content"]["target_name"]
         comm_id = msg["content"]["comm_id"]
         self.comm = comm
-        model = self.ydocs[name](primary=False)
+        model = self.ydocs[name](open_comm=False)
         self.widgets[comm_id] = {"model": model, "comm": comm}
-        msg = sync(model._ydoc)
-        comm.send(**msg)
+        sync(model.ydoc, comm)
+        asyncio.create_task(self._send(model.ydoc))
 
     def comm_msg(self, msg) -> None:
         comm_id = msg["content"]["comm_id"]
         message = bytes(msg["buffers"][0])
         if message[0] == YMessageType.SYNC:
-            ydoc = self.widgets[comm_id]["model"]._ydoc
-            reply = process_sync_message(
-                message[1:],
-                ydoc,
-            )
-            if reply:
-                self.widgets[comm_id]["comm"].send(buffers=[reply])
+            process_sync_message(message[1:], self.widgets[comm_id]["model"].ydoc, self.widgets[comm_id]["comm"])
             if message[1] == YSyncMessageType.SYNC_STEP2:
-                ydoc.observe_after_transaction(self._send)
+                self.synced.set()
 
-    def _send(self, event: Y.AfterTransactionEvent):
-        update = event.get_update()
-        message = create_update_message(update)
-        try:
-            self.comm.send(buffers=[message])
-        except BaseException:
-            pass
+    async def _send(self, ydoc):
+        await self.synced.wait()
+        ydoc.observe_after_transaction(partial(put_updates, self._update_queue))
+        while True:
+            update = await self._update_queue.get()
+            message = create_update_message(update)
+            try:
+                self.comm.send(buffers=[message])
+            except BaseException:
+                pass
 
 
 class WidgetsComponent(Component):
+
     async def start(
         self,
         ctx: Context,
     ) -> None:
-        kernels = await ctx.request_resource(Kernels)
+        kernels = await ctx.request_resource(Kernels, "kernels")
         widgets = _Widgets()
         kernels.comm_handlers.append(widgets)
 
-        ctx.add_resource(widgets, types=Widgets)
+        ctx.add_resource(widgets, name="widgets", types=Widgets)
+
+
+c = register_component("widgets", WidgetsComponent)
```

### Comparing `txl_widgets-0.1.14/LICENSE.txt` & `txl_widgets-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_widgets-0.1.14/pyproject.toml` & `txl_widgets-0.1.7/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -2,36 +2,38 @@
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "txl_widgets"
 description = "TXL plugin for kernel widgets"
 readme = "README.md"
-requires-python = ">=3.10"
+requires-python = ">=3.7"
 license = "MIT"
 keywords = []
 authors = [
   { name = "David Brochart", email = "david.brochart@gmail.com" },
 ]
 classifiers = [
   "Development Status :: 4 - Beta",
   "Programming Language :: Python",
+  "Programming Language :: Python :: 3.7",
+  "Programming Language :: Python :: 3.8",
+  "Programming Language :: Python :: 3.9",
   "Programming Language :: Python :: 3.10",
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "txl",
-  "ypywidgets >=0.4.0",
-  "ypywidgets-textual >=0.1.2",
+  "ypywidgets >=0.1.1",
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/plugins/widgets"
 
-[project.entry-points."asphalt.components"]
-widgets = "txl_widgets.components:WidgetsComponent"
+[project.entry-points.txl_component]
+txl_widgets = "txl_widgets.components"
 
 [tool.hatch.version]
 path = "txl_widgets/__init__.py"
```

### Comparing `txl_widgets-0.1.14/PKG-INFO` & `txl_widgets-0.1.7/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,21 +1,23 @@
 Metadata-Version: 2.1
 Name: txl_widgets
-Version: 0.1.14
+Version: 0.1.7
 Summary: TXL plugin for kernel widgets
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/widgets
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
-Requires-Python: >=3.10
+Requires-Python: >=3.7
 Requires-Dist: txl
-Requires-Dist: ypywidgets-textual>=0.1.2
-Requires-Dist: ypywidgets>=0.4.0
+Requires-Dist: ypywidgets>=0.1.1
 Description-Content-Type: text/markdown
 
 # TXL plugin for widgets
```

