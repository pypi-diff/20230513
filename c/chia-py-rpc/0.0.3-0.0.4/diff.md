# Comparing `tmp/chia_py_rpc-0.0.3.tar.gz` & `tmp/chia_py_rpc-0.0.4.tar.gz`

## Comparing `chia_py_rpc-0.0.3.tar` & `chia_py_rpc-0.0.4.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/src/chia_py_rpc/__init__.py
--rw-r--r--   0        0        0     2792 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/src/chia_py_rpc/rpc_connect.py
--rw-r--r--   0        0        0    80547 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/src/chia_py_rpc/wallet.py
--rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/LICENSE
--rw-r--r--   0        0        0     2330 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/README.md
--rw-r--r--   0        0        0      697 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/pyproject.toml
--rw-r--r--   0        0        0     2885 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.4/src/chia_py_rpc/__init__.py
+-rw-r--r--   0        0        0     2792 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.4/src/chia_py_rpc/rpc_connect.py
+-rw-r--r--   0        0        0    80559 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.4/src/chia_py_rpc/wallet.py
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.4/LICENSE
+-rw-r--r--   0        0        0     2330 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.4/README.md
+-rw-r--r--   0        0        0      697 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0     2885 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.4/PKG-INFO
```

### Comparing `chia_py_rpc-0.0.3/src/chia_py_rpc/rpc_connect.py` & `chia_py_rpc-0.0.4/src/chia_py_rpc/rpc_connect.py`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.3/src/chia_py_rpc/wallet.py` & `chia_py_rpc-0.0.4/src/chia_py_rpc/wallet.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 import json
-from rpc_connect import WalletRPCConnect as WalletRPC
+from chia_py_rpc.rpc_connect import WalletRPCConnect as WalletRPC
 from typing import Dict, Union, List
 
 
 class SharedMethods:
     """Methods shared by all services."""
 
     def __init__(self, url: str = None, cert: str = None):
```

### Comparing `chia_py_rpc-0.0.3/LICENSE` & `chia_py_rpc-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.3/README.md` & `chia_py_rpc-0.0.4/README.md`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.3/pyproject.toml` & `chia_py_rpc-0.0.4/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "chia_py_rpc"
-version = "0.0.3"
+version = "0.0.4"
 authors = [
   { name="L4bb3rs", email="king@the300.net" },
 ]
 description = "Chia-Py-RPC is a Python library that provides a convenient way to interact with the Chia blockchain using the Chia RPC (Remote Procedure Call) protocol."
 readme = "README.md"
 requires-python = ">=3.9"
 classifiers = [
```

### Comparing `chia_py_rpc-0.0.3/PKG-INFO` & `chia_py_rpc-0.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chia_py_rpc
-Version: 0.0.3
+Version: 0.0.4
 Summary: Chia-Py-RPC is a Python library that provides a convenient way to interact with the Chia blockchain using the Chia RPC (Remote Procedure Call) protocol.
 Project-URL: Homepage, https://github.com/L4bb3rs/Chia-Py-RPC
 Project-URL: Bug Tracker, https://github.com/L4bb3rs/Chia-Py-RPC
 Author-email: L4bb3rs <king@the300.net>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

