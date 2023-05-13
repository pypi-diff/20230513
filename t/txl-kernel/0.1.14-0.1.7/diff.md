# Comparing `tmp/txl_kernel-0.1.14.tar.gz` & `tmp/txl_kernel-0.1.7.tar.gz`

## Comparing `txl_kernel-0.1.14.tar` & `txl_kernel-0.1.7.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0       23 2020-02-02 00:00:00.000000 txl_kernel-0.1.14/txl_kernel/__init__.py
--rw-r--r--   0        0        0     8075 2020-02-02 00:00:00.000000 txl_kernel-0.1.14/txl_kernel/driver.py
--rw-r--r--   0        0        0     1517 2020-02-02 00:00:00.000000 txl_kernel-0.1.14/txl_kernel/message.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_kernel-0.1.14/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_kernel-0.1.14/LICENSE.txt
--rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 txl_kernel-0.1.14/README.md
--rw-r--r--   0        0        0      852 2020-02-02 00:00:00.000000 txl_kernel-0.1.14/pyproject.toml
--rw-r--r--   0        0        0      791 2020-02-02 00:00:00.000000 txl_kernel-0.1.14/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_kernel-0.1.7/txl_kernel/__init__.py
+-rw-r--r--   0        0        0     8050 2020-02-02 00:00:00.000000 txl_kernel-0.1.7/txl_kernel/driver.py
+-rw-r--r--   0        0        0     1518 2020-02-02 00:00:00.000000 txl_kernel-0.1.7/txl_kernel/message.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_kernel-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_kernel-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 txl_kernel-0.1.7/README.md
+-rw-r--r--   0        0        0      831 2020-02-02 00:00:00.000000 txl_kernel-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      760 2020-02-02 00:00:00.000000 txl_kernel-0.1.7/PKG-INFO
```

### Comparing `txl_kernel-0.1.14/txl_kernel/driver.py` & `txl_kernel-0.1.7/txl_kernel/driver.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,21 +1,22 @@
 import asyncio
 import time
 from typing import Dict, List
 
 import y_py as Y
 
-from .message import create_message
+from .message import create_message, str_to_date
 
 
 def deadline_to_timeout(deadline: float) -> float:
     return max(0, deadline - time.monotonic())
 
 
 class Comm:
+
     def __init__(self, comm_id: str, shell_channel, session_id: str, send_message):
         self.comm_id = comm_id
         self.shell_channel = shell_channel
         self.session_id = session_id
         self.send_message = send_message
         self.msg_cnt = 0
 
@@ -24,20 +25,19 @@
             "comm_msg",
             content={"comm_id": self.comm_id},
             session_id=self.session_id,
             msg_id=self.msg_cnt,
             buffers=buffers,
         )
         self.msg_cnt += 1
-        asyncio.create_task(
-            self.send_message(msg, self.shell_channel, change_date_to_str=True)
-        )
+        asyncio.create_task(self.send_message(msg, self.shell_channel, change_date_to_str=True))
 
 
 class KernelMixin:
+
     def __init__(self):
         self.msg_cnt = 0
         self.execute_requests: Dict[str, Dict[str, List[asyncio.Future]]] = {}
         self.recv_queue = asyncio.Queue()
         self.started = asyncio.Event()
         asyncio.create_task(self.recv())
 
@@ -50,15 +50,17 @@
         while True:
             msg = create_message(
                 "kernel_info_request",
                 session_id=self.session_id,
                 msg_id=str(self.msg_cnt),
             )
             self.msg_cnt += 1
-            await self.send_message(msg, self.shell_channel, change_date_to_str=True)
+            await self.send_message(
+                msg, self.shell_channel, change_date_to_str=True
+            )
             msg_id = msg["header"]["msg_id"]
             self.execute_requests[msg_id] = {
                 "iopub": [asyncio.Future()],
                 "shell": [asyncio.Future()],
             }
             try:
                 msg = await asyncio.wait_for(
@@ -84,25 +86,23 @@
         while True:
             msg = await self.recv_queue.get()
             channel = msg.pop("channel")
             msg_type = msg["header"]["msg_type"]
             if msg_type == "comm_open":
                 for comm_handler in self.comm_handlers:
                     comm_id = msg["content"]["comm_id"]
-                    comm = Comm(
-                        comm_id, self.shell_channel, self.session_id, self.send_message
-                    )
+                    comm = Comm(comm_id, self.shell_channel, self.session_id, self.send_message)
                     comm_handler.comm_open(msg, comm)
             elif msg_type == "comm_msg":
                 for comm_handler in self.comm_handlers:
                     comm_handler.comm_msg(msg)
             msg_id = msg["parent_header"].get("msg_id")
             if msg_id in self.execute_requests:
-                # msg["header"] = str_to_date(msg["header"])
-                # msg["parent_header"] = str_to_date(msg["parent_header"])
+                #msg["header"] = str_to_date(msg["header"])
+                #msg["parent_header"] = str_to_date(msg["parent_header"])
                 future_msgs = self.execute_requests[msg_id][channel]
                 if future_msgs:
                     fut = future_msgs[-1]
                     if fut.done():
                         fut = asyncio.Future()
                         future_msgs.append(fut)
                 else:
```

### Comparing `txl_kernel-0.1.14/txl_kernel/message.py` & `txl_kernel-0.1.7/txl_kernel/message.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from datetime import datetime, timezone
 from typing import Any, Dict, List
 from uuid import uuid4
 
 from dateutil.parser import parse as dateutil_parse
 
+
 PROTOCOL_VERSION = "5.3"
 
 
 def utcnow() -> datetime:
     return datetime.utcnow().replace(tzinfo=timezone.utc)
```

### Comparing `txl_kernel-0.1.14/LICENSE.txt` & `txl_kernel-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_kernel-0.1.14/pyproject.toml` & `txl_kernel-0.1.7/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -19,15 +19,14 @@
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "txl",
   "python-dateutil >=2.8.2",
-  "y-py >=0.6.0,<1",
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/plugins/kernel"
 
 [tool.hatch.version]
```

### Comparing `txl_kernel-0.1.14/PKG-INFO` & `txl_kernel-0.1.7/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,21 +1,20 @@
 Metadata-Version: 2.1
 Name: txl_kernel
-Version: 0.1.14
+Version: 0.1.7
 Summary: TXL plugin for a kernel driver
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/kernel
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Requires-Python: >=3.10
 Requires-Dist: python-dateutil>=2.8.2
 Requires-Dist: txl
-Requires-Dist: y-py<1,>=0.6.0
 Description-Content-Type: text/markdown
 
 # TXL plugin for a kernel driver
```

