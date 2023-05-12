# Comparing `tmp/chia_py_rpc-0.0.2.tar.gz` & `tmp/chia_py_rpc-0.0.3.tar.gz`

## Comparing `chia_py_rpc-0.0.2.tar` & `chia_py_rpc-0.0.3.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.2/src/chia_py_rpc/__init__.py
--rw-r--r--   0        0        0     2792 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.2/src/chia_py_rpc/rpc_connect.py
--rw-r--r--   0        0        0    80547 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.2/src/chia_py_rpc/wallet.py
--rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.2/LICENSE
--rw-r--r--   0        0        0     2329 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.2/README.md
--rw-r--r--   0        0        0      697 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.2/pyproject.toml
--rw-r--r--   0        0        0     2884 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/src/chia_py_rpc/__init__.py
+-rw-r--r--   0        0        0     2792 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/src/chia_py_rpc/rpc_connect.py
+-rw-r--r--   0        0        0    80547 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/src/chia_py_rpc/wallet.py
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/LICENSE
+-rw-r--r--   0        0        0     2330 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/README.md
+-rw-r--r--   0        0        0      697 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0     2885 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.3/PKG-INFO
```

### Comparing `chia_py_rpc-0.0.2/src/chia_py_rpc/rpc_connect.py` & `chia_py_rpc-0.0.3/src/chia_py_rpc/rpc_connect.py`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.2/src/chia_py_rpc/wallet.py` & `chia_py_rpc-0.0.3/src/chia_py_rpc/wallet.py`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.2/LICENSE` & `chia_py_rpc-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.2/README.md` & `chia_py_rpc-0.0.3/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -21,16 +21,16 @@
 
 ## Usage
 Here's an example of how you can use Chia-Py-RPC to send transactions to multiple recipients in a single transaction:
 
 ```
 from chia_py_rpc import Wallet
 
-# Create an instance of ChiaWallet
-wallet = Wallet()
+# Create an instance of Wallet
+chia_wallet = Wallet()
 
 # Specify the wallet ID, additions (recipients), fee, and optional parameters
 wallet_id = 1
 additions = [
     {'amount': 1000000000000, 'puzzle_hash': '0x...'},  # Recipient 1
     {'amount': 500000000000, 'puzzle_hash': '0x...'},  # Recipient 2
 ]
```

### Comparing `chia_py_rpc-0.0.2/pyproject.toml` & `chia_py_rpc-0.0.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "chia_py_rpc"
-version = "0.0.2"
+version = "0.0.3"
 authors = [
   { name="L4bb3rs", email="king@the300.net" },
 ]
 description = "Chia-Py-RPC is a Python library that provides a convenient way to interact with the Chia blockchain using the Chia RPC (Remote Procedure Call) protocol."
 readme = "README.md"
 requires-python = ">=3.9"
 classifiers = [
```

### Comparing `chia_py_rpc-0.0.2/PKG-INFO` & `chia_py_rpc-0.0.3/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chia_py_rpc
-Version: 0.0.2
+Version: 0.0.3
 Summary: Chia-Py-RPC is a Python library that provides a convenient way to interact with the Chia blockchain using the Chia RPC (Remote Procedure Call) protocol.
 Project-URL: Homepage, https://github.com/L4bb3rs/Chia-Py-RPC
 Project-URL: Bug Tracker, https://github.com/L4bb3rs/Chia-Py-RPC
 Author-email: L4bb3rs <king@the300.net>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -35,16 +35,16 @@
 
 ## Usage
 Here's an example of how you can use Chia-Py-RPC to send transactions to multiple recipients in a single transaction:
 
 ```
 from chia_py_rpc import Wallet
 
-# Create an instance of ChiaWallet
-wallet = Wallet()
+# Create an instance of Wallet
+chia_wallet = Wallet()
 
 # Specify the wallet ID, additions (recipients), fee, and optional parameters
 wallet_id = 1
 additions = [
     {'amount': 1000000000000, 'puzzle_hash': '0x...'},  # Recipient 1
     {'amount': 500000000000, 'puzzle_hash': '0x...'},  # Recipient 2
 ]
```

