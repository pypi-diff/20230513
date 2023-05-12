# Comparing `tmp/chia_py_rpc-0.0.5.tar.gz` & `tmp/chia_py_rpc-0.0.6.tar.gz`

## Comparing `chia_py_rpc-0.0.5.tar` & `chia_py_rpc-0.0.6.tar`

### file list

```diff
@@ -1,7 +1,8 @@
--rw-r--r--   0        0        0       64 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.5/src/chia_py_rpc/__init__.py
--rw-r--r--   0        0        0     2792 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.5/src/chia_py_rpc/rpc_connect.py
--rw-r--r--   0        0        0    80559 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.5/src/chia_py_rpc/wallet.py
--rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.5/LICENSE
--rw-r--r--   0        0        0     2330 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.5/README.md
--rw-r--r--   0        0        0      697 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.5/pyproject.toml
--rw-r--r--   0        0        0     2885 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0      510 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.6/.vscode/launch.json
+-rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.6/src/chia_py_rpc/__init__.py
+-rw-r--r--   0        0        0     2792 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.6/src/chia_py_rpc/rpc_connect.py
+-rw-r--r--   0        0        0    80559 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.6/src/chia_py_rpc/wallet.py
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.6/LICENSE
+-rw-r--r--   0        0        0     2331 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.6/README.md
+-rw-r--r--   0        0        0      698 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.6/pyproject.toml
+-rw-r--r--   0        0        0     2887 2020-02-02 00:00:00.000000 chia_py_rpc-0.0.6/PKG-INFO
```

### Comparing `chia_py_rpc-0.0.5/src/chia_py_rpc/rpc_connect.py` & `chia_py_rpc-0.0.6/src/chia_py_rpc/rpc_connect.py`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.5/src/chia_py_rpc/wallet.py` & `chia_py_rpc-0.0.6/src/chia_py_rpc/wallet.py`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.5/LICENSE` & `chia_py_rpc-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `chia_py_rpc-0.0.5/README.md` & `chia_py_rpc-0.0.6/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 pip install chia-py-rpc
 ```
 
 ## Usage
 Here's an example of how you can use Chia-Py-RPC to send transactions to multiple recipients in a single transaction:
 
 ```
-from chia_py_rpc import Wallet
+from chia_py_rpc.wallet import Wallet
 
 # Create an instance of Wallet
 chia_wallet = Wallet()
 
 # Specify the wallet ID, additions (recipients), fee, and optional parameters
 wallet_id = 1
 additions = [
@@ -45,15 +45,15 @@
 # Parse the result and handle the transaction ID and status
 transaction_id = result['transaction_id']
 status = result['status']
 print(f"Transaction ID: {transaction_id}")
 print(f"Status: {status}")
 ```
 
-For more examples and documentation, please refer to the official documentation (TBC).
+For more examples and documentation, please refer to the official documentation.
 
 ## Contributing
 If you would like to contribute to Chia-Py-RPC, please open an issue or submit a pull request on GitHub. We welcome any contributions, including bug fixes, feature enhancements, and documentation improvements.
 
 ## License
 Chia-Py-RPC is open-source software licensed under the MIT License.
```

### Comparing `chia_py_rpc-0.0.5/pyproject.toml` & `chia_py_rpc-0.0.6/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "chia_py_rpc"
-version = "0.0.5"
+version = "0.0.6"
 authors = [
   { name="L4bb3rs", email="king@the300.net" },
 ]
 description = "Chia-Py-RPC is a Python library that provides a convenient way to interact with the Chia blockchain using the Chia RPC (Remote Procedure Call) protocol."
 readme = "README.md"
-requires-python = ">=3.9"
+requires-python = ">=3.11"
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 
 [project.urls]
```

### Comparing `chia_py_rpc-0.0.5/PKG-INFO` & `chia_py_rpc-0.0.6/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: chia_py_rpc
-Version: 0.0.5
+Version: 0.0.6
 Summary: Chia-Py-RPC is a Python library that provides a convenient way to interact with the Chia blockchain using the Chia RPC (Remote Procedure Call) protocol.
 Project-URL: Homepage, https://github.com/L4bb3rs/Chia-Py-RPC
 Project-URL: Bug Tracker, https://github.com/L4bb3rs/Chia-Py-RPC
 Author-email: L4bb3rs <king@the300.net>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
-Requires-Python: >=3.9
+Requires-Python: >=3.11
 Description-Content-Type: text/markdown
 
 # Chia-Py-RPC
 
 Chia-Py-RPC is a Python library that provides a convenient way to interact with the Chia blockchain using the Chia RPC (Remote Procedure Call) protocol. It allows you to send transactions, check balances, and perform other Chia-related operations programmatically from Python.
 
 ## Features
@@ -33,15 +33,15 @@
 pip install chia-py-rpc
 ```
 
 ## Usage
 Here's an example of how you can use Chia-Py-RPC to send transactions to multiple recipients in a single transaction:
 
 ```
-from chia_py_rpc import Wallet
+from chia_py_rpc.wallet import Wallet
 
 # Create an instance of Wallet
 chia_wallet = Wallet()
 
 # Specify the wallet ID, additions (recipients), fee, and optional parameters
 wallet_id = 1
 additions = [
@@ -59,15 +59,15 @@
 # Parse the result and handle the transaction ID and status
 transaction_id = result['transaction_id']
 status = result['status']
 print(f"Transaction ID: {transaction_id}")
 print(f"Status: {status}")
 ```
 
-For more examples and documentation, please refer to the official documentation (TBC).
+For more examples and documentation, please refer to the official documentation.
 
 ## Contributing
 If you would like to contribute to Chia-Py-RPC, please open an issue or submit a pull request on GitHub. We welcome any contributions, including bug fixes, feature enhancements, and documentation improvements.
 
 ## License
 Chia-Py-RPC is open-source software licensed under the MIT License.
```

