# Comparing `tmp/txl_remote_contents-0.1.5.tar.gz` & `tmp/txl_remote_contents-0.1.7.tar.gz`

## Comparing `txl_remote_contents-0.1.5.tar` & `txl_remote_contents-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.5/txl_remote_contents/__init__.py
--rw-r--r--   0        0        0     5431 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.5/txl_remote_contents/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.5/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.5/README.md
--rw-r--r--   0        0        0     1151 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.5/pyproject.toml
--rw-r--r--   0        0        0     1028 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.7/txl_remote_contents/__init__.py
+-rw-r--r--   0        0        0     4801 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.7/txl_remote_contents/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.7/README.md
+-rw-r--r--   0        0        0     1148 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0     1025 2020-02-02 00:00:00.000000 txl_remote_contents-0.1.7/PKG-INFO
```

### Comparing `txl_remote_contents-0.1.5/txl_remote_contents/components.py` & `txl_remote_contents-0.1.7/txl_remote_contents/components.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,22 +1,21 @@
 import asyncio
-import base64
 import json
-from functools import partial
-from typing import Any, Callable, Dict, List, Optional, Union
+from typing import Any, Dict, List, Union
 from urllib import parse
 
 import httpx
 import y_py as Y
 from asphalt.core import Component, Context
 from httpx_ws import aconnect_ws
 from jupyter_ydoc import ydocs
+from ypy_websocket import WebsocketProvider
+
 from txl.base import Contents
 from txl.hooks import register_component
-from ypy_websocket import WebsocketProvider
 
 
 class Websocket:
     def __init__(self, websocket, roomid: str):
         self.websocket = websocket
         self.roomid = roomid
 
@@ -79,76 +78,63 @@
         i = base_url.find(":")
         self.ws_url = ("wss" if base_url[i - 1] == "s" else "ws") + base_url[i:]
 
     async def get(
         self,
         path: str,
         is_dir: bool = False,
-        type: str = "text",
-        on_change: Optional[Callable] = None,
-    ) -> Union[List, str, bytes, Dict[str, Any]]:
+        type: str = "unicode",
+    ) -> Union[List, Y.YDoc]:
         path = "" if path == "." else path
         if is_dir or not self.collaborative:
             async with httpx.AsyncClient() as client:
                 r = await client.get(
                     f"{self.base_url}/api/contents/{path}",
                     params={**{"content": 1}, **self.query_params},
                     cookies=self.cookies,
                 )
             self.cookies.update(r.cookies)
             model = r.json()
-            if model["type"] == "file":
-                document = model["content"]
-            elif model["type"] == "notebook":
-                document = model["content"]
-                if isinstance(model["content"], (str, bytes)):
-                    document = json.loads(model["content"])
-            elif model["type"] == "directory":
+            if model["type"] == "directory":
                 dir_list = [Entry(entry) for entry in model["content"]]
-                document = sorted(
+                return sorted(
                     dir_list, key=lambda entry: (not entry.is_dir(), entry.name)
                 )
-            if model["format"] == "base64":
-                document = document.encode()
-                document = base64.b64decode(document)
-            return document
+            document = model["content"]
+            if type == "notebook":
+                if isinstance(model["content"], (str, bytes)):
+                    # jupyverse doesn't return JSON
+                    document = json.loads(model["content"])
+            jupyter_ydoc = ydocs[type]()
+            jupyter_ydoc.source = document
+            return jupyter_ydoc
 
         else:
-            # it's a collaborative document
-            doc_format = "json" if path.endswith(".ipynb") else "text"
-            doc_type = "notebook" if path.endswith(".ipynb") else "file"
+            doc_format = {"blob": "base64"}.get(type, "text")
+            doc_type = type  # if type == "notebook" else "file"
             async with httpx.AsyncClient() as client:
                 r = await client.put(
                     f"{self.base_url}/api/yjs/roomid/{path}",
                     json={"format": doc_format, "type": doc_type},
                     params={**self.query_params},
                     cookies=self.cookies,
                 )
             self.cookies.update(r.cookies)
             roomid = r.text
             ydoc = Y.YDoc()
-            jupyter_ydoc = ydocs[doc_type](ydoc)
-            if on_change:
-                jupyter_ydoc.observe(partial(self.on_change, jupyter_ydoc, on_change))
+            jupyter_ydoc = ydocs[type](ydoc)
             asyncio.create_task(self._websocket_provider(roomid, ydoc))
-            if doc_type == "notebook":
-                return {}
-            else:
-                return ""
+            return jupyter_ydoc
 
     async def _websocket_provider(self, roomid, ydoc):
         ws_url = f"{self.ws_url}/api/yjs/{roomid}"
         async with aconnect_ws(ws_url, cookies=self.cookies) as websocket:
             WebsocketProvider(ydoc, Websocket(websocket, roomid))
             await asyncio.Future()
 
-    def on_change(self, jupyter_ydoc, on_change: Callable, events) -> None:
-        content = jupyter_ydoc.get()
-        on_change(content)
-
 
 class ContentsComponent(Component):
     def __init__(self, url: str = "http://127.0.0.1:8000", collaborative: bool = True):
         super().__init__()
         self.url = url
         self.collaborative = collaborative
```

### Comparing `txl_remote_contents-0.1.5/LICENSE.txt` & `txl_remote_contents-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_remote_contents-0.1.5/pyproject.toml` & `txl_remote_contents-0.1.7/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -22,17 +22,17 @@
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "txl",
   "httpx>=0.23.1",
-  "httpx-ws>=0.2.4",
-  "jupyter_ydoc >=0.3.0a1,<1",
-  "ypy-websocket >=0.3.2,<1",
+  "httpx-ws>=0.2.6",
+  "jupyter_ydoc >=0.3.0a4",
+  "ypy-websocket >=0.8.2,<1",
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/plugins/remote_contents"
 
 [project.entry-points.txl_component]
```

### Comparing `txl_remote_contents-0.1.5/PKG-INFO` & `txl_remote_contents-0.1.7/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: txl_remote_contents
-Version: 0.1.5
+Version: 0.1.7
 Summary: TXL plugin for remote contents
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/remote_contents
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
@@ -12,15 +12,15 @@
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Requires-Python: >=3.7
-Requires-Dist: httpx-ws>=0.2.4
+Requires-Dist: httpx-ws>=0.2.6
 Requires-Dist: httpx>=0.23.1
-Requires-Dist: jupyter-ydoc<1,>=0.3.0a1
+Requires-Dist: jupyter-ydoc>=0.3.0a4
 Requires-Dist: txl
-Requires-Dist: ypy-websocket<1,>=0.3.2
+Requires-Dist: ypy-websocket<1,>=0.8.2
 Description-Content-Type: text/markdown
 
 # TXL plugin for remote contents
```

