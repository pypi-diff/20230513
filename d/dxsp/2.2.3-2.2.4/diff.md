# Comparing `tmp/dxsp-2.2.3.tar.gz` & `tmp/dxsp-2.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dxsp-2.2.3.tar", max compression
+gzip compressed data, was "dxsp-2.2.4.tar", max compression
```

## Comparing `dxsp-2.2.3.tar` & `dxsp-2.2.4.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1064 2023-05-12 05:31:33.453496 dxsp-2.2.3/LICENSE
--rw-r--r--   0        0        0     2605 2023-05-12 05:31:33.453496 dxsp-2.2.3/README.md
--rw-r--r--   0        0        0       86 2023-05-12 05:31:34.301524 dxsp-2.2.3/dxsp/__init__.py
--rw-r--r--   0        0        0        1 2023-05-12 05:31:33.453496 dxsp-2.2.3/dxsp/assets/__init__.py
--rw-r--r--   0        0        0     8887 2023-05-12 05:31:33.453496 dxsp-2.2.3/dxsp/assets/blockchains.py
--rw-r--r--   0        0        0      388 2023-05-12 05:31:33.453496 dxsp-2.2.3/dxsp/config.py
--rw-r--r--   0        0        0     3139 2023-05-12 05:31:33.453496 dxsp-2.2.3/dxsp/default_settings.toml
--rw-r--r--   0        0        0    29260 2023-05-12 05:31:33.453496 dxsp-2.2.3/dxsp/main.py
--rw-r--r--   0        0        0     1811 2023-05-12 05:31:34.301524 dxsp-2.2.3/pyproject.toml
--rw-r--r--   0        0        0     3368 1970-01-01 00:00:00.000000 dxsp-2.2.3/PKG-INFO
+-rw-r--r--   0        0        0     1064 2023-05-13 13:26:08.787342 dxsp-2.2.4/LICENSE
+-rw-r--r--   0        0        0     2605 2023-05-13 13:26:08.787342 dxsp-2.2.4/README.md
+-rw-r--r--   0        0        0       86 2023-05-13 13:26:09.423334 dxsp-2.2.4/dxsp/__init__.py
+-rw-r--r--   0        0        0        1 2023-05-13 13:26:08.787342 dxsp-2.2.4/dxsp/assets/__init__.py
+-rw-r--r--   0        0        0     8887 2023-05-13 13:26:08.791342 dxsp-2.2.4/dxsp/assets/blockchains.py
+-rw-r--r--   0        0        0      388 2023-05-13 13:26:08.791342 dxsp-2.2.4/dxsp/config.py
+-rw-r--r--   0        0        0     3139 2023-05-13 13:26:08.791342 dxsp-2.2.4/dxsp/default_settings.toml
+-rw-r--r--   0        0        0    29316 2023-05-13 13:26:08.791342 dxsp-2.2.4/dxsp/main.py
+-rw-r--r--   0        0        0     1811 2023-05-13 13:26:09.423334 dxsp-2.2.4/pyproject.toml
+-rw-r--r--   0        0        0     3368 1970-01-01 00:00:00.000000 dxsp-2.2.4/PKG-INFO
```

### Comparing `dxsp-2.2.3/LICENSE` & `dxsp-2.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `dxsp-2.2.3/README.md` & `dxsp-2.2.4/README.md`

 * *Files identical despite different names*

### Comparing `dxsp-2.2.3/dxsp/assets/blockchains.py` & `dxsp-2.2.4/dxsp/assets/blockchains.py`

 * *Files identical despite different names*

### Comparing `dxsp-2.2.3/dxsp/default_settings.toml` & `dxsp-2.2.4/dxsp/default_settings.toml`

 * *Files identical despite different names*

### Comparing `dxsp-2.2.3/dxsp/main.py` & `dxsp-2.2.4/dxsp/main.py`

 * *Files 0% similar despite different names*

```diff
@@ -38,15 +38,15 @@
         # UNISWAP 🦄
         if self.protocol_type in ["uniswap_v2", "uniswap_v3"]:
             self.uniswap = Uniswap(
                 address=self.wallet_address,
                 private_key=self.private_key,
                 version=2 if self.protocol_type == "uniswap_v2" else 3,
                 web3=self.w3,
-                default_slippage=settings.slippage)
+                default_slippage=settings.dex_trading_slippage)
 
         # COINGECKO 🦎
         try:
             self.cg = CoinGeckoAPI()
             assetplatform = self.cg.get_asset_platforms()
             output_dict = [x for x in assetplatform if x['chain_identifier']
                            == int(self.chain_id)]
@@ -267,15 +267,16 @@
                     token_contract = await self.get_contract_address(
                         settings.token_mainnet_list,
                         token)
                     if token_contract is None:
                         token_contract = await self.search_cg_contract(
                             token)
             if token_contract is not None:
-                self.logger.info("token_contract found %s", token_contract)
+                self.logger.info("%s token: contract found %s",
+                                 token, token_contract)
                 return self.w3.to_checksum_address(token_contract)
             return f"no contract found for {token}"
         except Exception as e:
             self.logger.error("search_contract %s", e)
             return
 
     async def search_cg(self, token):
```

### Comparing `dxsp-2.2.3/pyproject.toml` & `dxsp-2.2.4/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dxsp"
-version = "2.2.3"
+version = "2.2.4"
 description = "DXSP (DeX SwaP), A defi swap helper package. Swap made easy."
 authors = ["mraniki <8766259+mraniki@users.noreply.github.com>"]
 license = "MIT License"
 readme = "README.md"
 
 
 [tool.poetry.urls]
```

### Comparing `dxsp-2.2.3/PKG-INFO` & `dxsp-2.2.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dxsp
-Version: 2.2.3
+Version: 2.2.4
 Summary: DXSP (DeX SwaP), A defi swap helper package. Swap made easy.
 License: MIT
 Author: mraniki
 Author-email: 8766259+mraniki@users.noreply.github.com
 Requires-Python: >=3.10,<3.11
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

