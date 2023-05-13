# Comparing `tmp/dxsp-2.2.6.tar.gz` & `tmp/dxsp-2.2.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dxsp-2.2.6.tar", max compression
+gzip compressed data, was "dxsp-2.2.7.tar", max compression
```

## Comparing `dxsp-2.2.6.tar` & `dxsp-2.2.7.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1064 2023-05-13 15:56:00.452687 dxsp-2.2.6/LICENSE
--rw-r--r--   0        0        0     2605 2023-05-13 15:56:00.452687 dxsp-2.2.6/README.md
--rw-r--r--   0        0        0       86 2023-05-13 15:56:01.372760 dxsp-2.2.6/dxsp/__init__.py
--rw-r--r--   0        0        0        1 2023-05-13 15:56:00.452687 dxsp-2.2.6/dxsp/assets/__init__.py
--rw-r--r--   0        0        0     8887 2023-05-13 15:56:00.452687 dxsp-2.2.6/dxsp/assets/blockchains.py
--rw-r--r--   0        0        0      388 2023-05-13 15:56:00.452687 dxsp-2.2.6/dxsp/config.py
--rw-r--r--   0        0        0     3139 2023-05-13 15:56:00.452687 dxsp-2.2.6/dxsp/default_settings.toml
--rw-r--r--   0        0        0    29388 2023-05-13 15:56:00.452687 dxsp-2.2.6/dxsp/main.py
--rw-r--r--   0        0        0     1811 2023-05-13 15:56:01.372760 dxsp-2.2.6/pyproject.toml
--rw-r--r--   0        0        0     3368 1970-01-01 00:00:00.000000 dxsp-2.2.6/PKG-INFO
+-rw-r--r--   0        0        0     1064 2023-05-13 19:29:51.043585 dxsp-2.2.7/LICENSE
+-rw-r--r--   0        0        0     2605 2023-05-13 19:29:51.043585 dxsp-2.2.7/README.md
+-rw-r--r--   0        0        0       86 2023-05-13 19:29:51.991632 dxsp-2.2.7/dxsp/__init__.py
+-rw-r--r--   0        0        0        1 2023-05-13 19:29:51.043585 dxsp-2.2.7/dxsp/assets/__init__.py
+-rw-r--r--   0        0        0     8887 2023-05-13 19:29:51.043585 dxsp-2.2.7/dxsp/assets/blockchains.py
+-rw-r--r--   0        0        0      388 2023-05-13 19:29:51.043585 dxsp-2.2.7/dxsp/config.py
+-rw-r--r--   0        0        0     3139 2023-05-13 19:29:51.043585 dxsp-2.2.7/dxsp/default_settings.toml
+-rw-r--r--   0        0        0    29552 2023-05-13 19:29:51.043585 dxsp-2.2.7/dxsp/main.py
+-rw-r--r--   0        0        0     1811 2023-05-13 19:29:51.991632 dxsp-2.2.7/pyproject.toml
+-rw-r--r--   0        0        0     3368 1970-01-01 00:00:00.000000 dxsp-2.2.7/PKG-INFO
```

### Comparing `dxsp-2.2.6/LICENSE` & `dxsp-2.2.7/LICENSE`

 * *Files identical despite different names*

### Comparing `dxsp-2.2.6/README.md` & `dxsp-2.2.7/README.md`

 * *Files identical despite different names*

### Comparing `dxsp-2.2.6/dxsp/assets/blockchains.py` & `dxsp-2.2.7/dxsp/assets/blockchains.py`

 * *Files identical despite different names*

### Comparing `dxsp-2.2.6/dxsp/default_settings.toml` & `dxsp-2.2.7/dxsp/default_settings.toml`

 * *Files identical despite different names*

### Comparing `dxsp-2.2.6/dxsp/main.py` & `dxsp-2.2.7/dxsp/main.py`

 * *Files 1% similar despite different names*

```diff
@@ -28,15 +28,16 @@
         except Exception as e:
             self.logger.error("connectivity failed %s", e)
             return
 
         self.protocol_type = settings.dex_protocol_type
         self.chain_id = settings.dex_chain_id
         # USER
-        self.wallet_address = settings.dex_wallet_address
+        self.wallet_address = self.w3.to_checksum_address(
+            settings.dex_wallet_address)
         self.private_key = settings.dex_private_key
 
         # UNISWAP 🦄
         if self.protocol_type in ["uniswap_v2", "uniswap_v3"]:
             self.uniswap = Uniswap(
                 address=self.wallet_address,
                 private_key=self.private_key,
@@ -66,30 +67,30 @@
         asset_out_address = await self.search_contract(asset_out_symbol)
         if asset_out_address is None:
             self.logger.warning("No Valid Contract")
             return
         try:
             if self.protocol_type in ["1inch", "1inch_limit"]:
                 self.logger.debug("1inch getquote")
-                await self.get_quote_1inch(
+                return await self.get_quote_1inch(
                     asset_in_address,
                     asset_out_address)
             if self.protocol_type in ["uniswap_v2", "uniswap_v3"]:
                 self.logger.debug("uniswap getquote")
-                await self.get_quote_uniswap(
+                return await self.get_quote_uniswap(
                     asset_in_address,
                     asset_out_address)
             if self.protocol_type == "0x":
                 self.logger.debug("0x getquote")
-                await self.get_quote_0x(
+                return await self.get_quote_0x(
                     symbol,
                     asset_out_symbol,)
             if self.protocol_type == "apollo":
                 self.logger.debug("apollo getquote")
-                await self.get_quote_apollo()
+                return await self.get_quote_apollo()
 
         except Exception as e:
             self.logger.error("get_quote %s", e)
             return
 
     async def get_swap(
                 self,
@@ -339,22 +340,22 @@
     async def _get(
         self,
         url,
         params=None,
         headers=None
             ):
         try:
-            self.logger.debug("url: %s", url)
-            self.logger.debug("_header: %s", settings.headers)
+            # self.logger.debug("url: %s", url)
+            # self.logger.debug("_header: %s", settings.headers)
             response = requests.get(
                 url,
                 params=params,
                 headers=headers,
                 timeout=10)
-            self.logger.debug("_response: %s", response)
+            # self.logger.debug("_response: %s", response)
             if response:
                 # self.logger.debug("_json: %s", response.json())
                 return response.json()
 
         except Exception as e:
             self.logger.error("_get: %s", e)
 
@@ -559,18 +560,20 @@
             # order_path_dex = [asset_out_address, asset_in_address]
             # router_instance = await self.router()
             # get_amount = router_instance.functions.getAmountsIn(
             #     amount,
             #     order_path_dex).call()
             # self.logger.debug("get_amount: %s", get_amount)
             # return get_amount[0]
-            self.uniswap.get_price_output(
+            quote = self.uniswap.get_price_output(
                 token0=asset_out_address,
                 token1=asset_in_address,
                 qty=amount)
+            self.logger.info("quoteuniswap %s", quote)
+            return quote
         except Exception as e:
             self.logger.error("get_quote_uniswap %s", e)
             return
 
     async def get_approve_uniswap(self, asset_out_address):
 
         try:
```

### Comparing `dxsp-2.2.6/pyproject.toml` & `dxsp-2.2.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dxsp"
-version = "2.2.6"
+version = "2.2.7"
 description = "DXSP (DeX SwaP), A defi swap helper package. Swap made easy."
 authors = ["mraniki <8766259+mraniki@users.noreply.github.com>"]
 license = "MIT License"
 readme = "README.md"
 
 
 [tool.poetry.urls]
```

### Comparing `dxsp-2.2.6/PKG-INFO` & `dxsp-2.2.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dxsp
-Version: 2.2.6
+Version: 2.2.7
 Summary: DXSP (DeX SwaP), A defi swap helper package. Swap made easy.
 License: MIT
 Author: mraniki
 Author-email: 8766259+mraniki@users.noreply.github.com
 Requires-Python: >=3.10,<3.11
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

