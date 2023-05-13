# Comparing `tmp/txl_remote_terminals-0.1.5.tar.gz` & `tmp/txl_remote_terminals-0.1.7.tar.gz`

## Comparing `txl_remote_terminals-0.1.5.tar` & `txl_remote_terminals-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.5/txl_remote_terminals/__init__.py
--rw-r--r--   0        0        0     3639 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.5/txl_remote_terminals/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.5/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0       34 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.5/README.md
--rw-r--r--   0        0        0     1096 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.5/pyproject.toml
--rw-r--r--   0        0        0      953 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.7/txl_remote_terminals/__init__.py
+-rw-r--r--   0        0        0     3813 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.7/txl_remote_terminals/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       34 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.7/README.md
+-rw-r--r--   0        0        0     1096 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      953 2020-02-02 00:00:00.000000 txl_remote_terminals-0.1.7/PKG-INFO
```

### Comparing `txl_remote_terminals-0.1.5/txl_remote_terminals/components.py` & `txl_remote_terminals-0.1.7/txl_remote_terminals/components.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,18 +1,20 @@
 import asyncio
 from typing import Dict, List
+from urllib import parse
 
 import httpx
+import httpx_ws
 from asphalt.core import Component, Context
 from httpx_ws import aconnect_ws
 from textual.widget import Widget
 from textual.widgets._header import HeaderTitle
-from txl.base import TerminalFactory, Terminals, Header, Launcher
+
+from txl.base import Header, Launcher, TerminalFactory, Terminals
 from txl.hooks import register_component
-from urllib import parse
 
 
 class TerminalsMeta(type(Terminals), type(Widget)):
     pass
 
 
 class RemoteTerminals(Terminals, Widget, metaclass=TerminalsMeta):
@@ -56,29 +58,33 @@
             terminal.focus()
             await self.mount(terminal)
             terminal.set_size(self.size)
             async with aconnect_ws(
                 f"{self.ws_url}/terminals/websocket/{name}", cookies=self.cookies
             ) as self.websocket:
                 asyncio.create_task(self._recv())
-                asyncio.create_task(self._send())
+                self.send_task = asyncio.create_task(self._send())
                 await self._done.wait()
 
     async def _send(self):
         while True:
             message = await self._send_queue.get()
             try:
                 await self.websocket.send_json(message)
             except BaseException:
                 self._done.set()
                 break
 
     async def _recv(self):
         while True:
-            message = await self.websocket.receive_json()
+            try:
+                message = await self.websocket.receive_json()
+            except httpx_ws._api.WebSocketNetworkError:
+                self.send_task.cancel()
+                return
             await self._recv_queue.put(message)
 
 
 class RemoteTerminalsComponent(Component):
     def __init__(self, url: str = "http://127.0.0.1:8000"):
         super().__init__()
         self.url = url
```

### Comparing `txl_remote_terminals-0.1.5/LICENSE.txt` & `txl_remote_terminals-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_remote_terminals-0.1.5/pyproject.toml` & `txl_remote_terminals-0.1.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -22,15 +22,15 @@
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "txl",
   "httpx>=0.23.1",
-  "httpx-ws>=0.2.4",
+  "httpx-ws>=0.2.6",
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/plugins/remote_terminals"
 
 [project.entry-points.txl_component]
```

### Comparing `txl_remote_terminals-0.1.5/PKG-INFO` & `txl_remote_terminals-0.1.7/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: txl_remote_terminals
-Version: 0.1.5
+Version: 0.1.7
 Summary: TXL plugin for remote terminals
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/remote_terminals
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
@@ -12,13 +12,13 @@
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
 Requires-Dist: txl
 Description-Content-Type: text/markdown
 
 # TXL plugin for remote terminals
```

