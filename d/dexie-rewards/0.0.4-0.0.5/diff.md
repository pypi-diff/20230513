# Comparing `tmp/dexie_rewards-0.0.4.tar.gz` & `tmp/dexie_rewards-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dexie_rewards-0.0.4.tar", max compression
+gzip compressed data, was "dexie_rewards-0.0.5.tar", max compression
```

## Comparing `dexie_rewards-0.0.4.tar` & `dexie_rewards-0.0.5.tar`

### file list

```diff
@@ -1,19 +1,19 @@
--rw-r--r--   0        0        0    11357 2023-05-02 08:44:23.355168 dexie_rewards-0.0.4/LICENSE
--rw-r--r--   0        0        0    11000 2023-05-12 12:43:50.717491 dexie_rewards-0.0.4/README.md
--rw-r--r--   0        0        0      768 2023-05-12 12:25:59.777811 dexie_rewards-0.0.4/pyproject.toml
--rw-r--r--   0        0        0      219 2023-05-04 04:23:21.607369 dexie_rewards-0.0.4/src/dexie_rewards/__init__.py
--rw-r--r--   0        0        0     1102 2023-05-12 11:45:41.221311 dexie_rewards-0.0.4/src/dexie_rewards/config.py
--rw-r--r--   0        0        0      822 2023-05-12 12:18:23.796037 dexie_rewards-0.0.4/src/dexie_rewards/decorators/with_db_connection.py
--rw-r--r--   0        0        0     1207 2023-05-11 04:12:56.210275 dexie_rewards-0.0.4/src/dexie_rewards/decorators/with_wallet_rpc_client.py
--rw-r--r--   0        0        0      234 2023-05-08 10:51:08.009870 dexie_rewards-0.0.4/src/dexie_rewards/main.py
--rw-r--r--   0        0        0     3312 2023-05-12 12:45:24.360778 dexie_rewards-0.0.4/src/dexie_rewards/rewards/claim.py
--rw-r--r--   0        0        0     1429 2023-05-12 13:27:55.283939 dexie_rewards-0.0.4/src/dexie_rewards/rewards/list.py
--rw-r--r--   0        0        0      272 2023-05-08 10:18:31.545940 dexie_rewards-0.0.4/src/dexie_rewards/rewards/main.py
--rw-r--r--   0        0        0     4636 2023-05-12 13:31:03.208683 dexie_rewards-0.0.4/src/dexie_rewards/rewards/utils.py
--rw-r--r--   0        0        0     2292 2023-05-09 13:07:18.656197 dexie_rewards-0.0.4/src/dexie_rewards/services/dexie_api.py
--rw-r--r--   0        0        0     4433 2023-05-12 12:12:02.337962 dexie_rewards-0.0.4/src/dexie_rewards/services/dexie_db.py
--rw-r--r--   0        0        0     1713 2023-05-11 04:36:56.173403 dexie_rewards-0.0.4/src/dexie_rewards/services/wallet_rpc_client.py
--rw-r--r--   0        0        0      911 2023-05-09 07:34:28.541774 dexie_rewards-0.0.4/src/dexie_rewards/types/offer_reward.py
--rw-r--r--   0        0        0      229 2023-05-09 11:06:14.984159 dexie_rewards-0.0.4/src/dexie_rewards/types/utils.py
--rw-r--r--   0        0        0     1851 2023-05-12 13:28:19.018840 dexie_rewards-0.0.4/src/dexie_rewards/utils.py
--rw-r--r--   0        0        0    11755 1970-01-01 00:00:00.000000 dexie_rewards-0.0.4/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-05-02 08:44:23.355168 dexie_rewards-0.0.5/LICENSE
+-rw-r--r--   0        0        0    12145 2023-05-13 02:37:26.609073 dexie_rewards-0.0.5/README.md
+-rw-r--r--   0        0        0      768 2023-05-13 03:28:15.075554 dexie_rewards-0.0.5/pyproject.toml
+-rw-r--r--   0        0        0      219 2023-05-04 04:23:21.607369 dexie_rewards-0.0.5/src/dexie_rewards/__init__.py
+-rw-r--r--   0        0        0     1126 2023-05-13 02:26:45.947358 dexie_rewards-0.0.5/src/dexie_rewards/config.py
+-rw-r--r--   0        0        0      822 2023-05-12 12:18:23.796037 dexie_rewards-0.0.5/src/dexie_rewards/decorators/with_db_connection.py
+-rw-r--r--   0        0        0     1207 2023-05-11 04:12:56.210275 dexie_rewards-0.0.5/src/dexie_rewards/decorators/with_wallet_rpc_client.py
+-rw-r--r--   0        0        0      234 2023-05-08 10:51:08.009870 dexie_rewards-0.0.5/src/dexie_rewards/main.py
+-rw-r--r--   0        0        0     3419 2023-05-13 02:46:45.159289 dexie_rewards-0.0.5/src/dexie_rewards/rewards/claim.py
+-rw-r--r--   0        0        0     1645 2023-05-13 02:35:05.501457 dexie_rewards-0.0.5/src/dexie_rewards/rewards/list.py
+-rw-r--r--   0        0        0      272 2023-05-08 10:18:31.545940 dexie_rewards-0.0.5/src/dexie_rewards/rewards/main.py
+-rw-r--r--   0        0        0     4561 2023-05-13 03:26:40.963961 dexie_rewards-0.0.5/src/dexie_rewards/rewards/utils.py
+-rw-r--r--   0        0        0     2292 2023-05-09 13:07:18.656197 dexie_rewards-0.0.5/src/dexie_rewards/services/dexie_api.py
+-rw-r--r--   0        0        0     4433 2023-05-12 12:12:02.337962 dexie_rewards-0.0.5/src/dexie_rewards/services/dexie_db.py
+-rw-r--r--   0        0        0     1713 2023-05-11 04:36:56.173403 dexie_rewards-0.0.5/src/dexie_rewards/services/wallet_rpc_client.py
+-rw-r--r--   0        0        0      911 2023-05-09 07:34:28.541774 dexie_rewards-0.0.5/src/dexie_rewards/types/offer_reward.py
+-rw-r--r--   0        0        0      229 2023-05-09 11:06:14.984159 dexie_rewards-0.0.5/src/dexie_rewards/types/utils.py
+-rw-r--r--   0        0        0     1851 2023-05-12 13:28:19.018840 dexie_rewards-0.0.5/src/dexie_rewards/utils.py
+-rw-r--r--   0        0        0    12900 1970-01-01 00:00:00.000000 dexie_rewards-0.0.5/PKG-INFO
```

### Comparing `dexie_rewards-0.0.4/LICENSE` & `dexie_rewards-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `dexie_rewards-0.0.4/README.md` & `dexie_rewards-0.0.5/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -102,15 +102,27 @@
 
 ╭─ Options ───────────────────────────────────────────────────────────────────────────────────────────────╮
 │ --fingerprint  -f  INTEGER  Set the fingerprint to specify which wallet to use                          │
 │ --json         -j           Displays offers as JSON                                                     │
 │ --help                      Show this message and exit.                                                 │
 ╰─────────────────────────────────────────────────────────────────────────────────────────────────────────╯
 
-❯ dexie rewards list -f 2149823282
+❯ dexie rewards list --help
+
+ Usage: dexie rewards list [OPTIONS]
+
+╭─ Options ──────────────────────────────────────────────────────────────────────────────────────────────╮
+│ --fingerprint  -f  INTEGER  Set the fingerprint to specify which wallet to use                         │
+│ --json         -j           Displays offers as JSON                                                    │
+│ --verbose      -v           Display verbose output                                                     │
+│ --help                      Show this message and exit.                                                │
+╰────────────────────────────────────────────────────────────────────────────────────────────────────────╯
+
+
+❯ dexie rewards list -f 2149823282 --verbose
 24 new offers
 0 updated offers
 24 claimable offers
 2 offers with rewards
 ╭──────────────────────────────────────────────┬───────────────╮
 │                    Offer                     │ Rewards (DBX) │
 ├──────────────────────────────────────────────┼───────────────┤
```

### Comparing `dexie_rewards-0.0.4/pyproject.toml` & `dexie_rewards-0.0.5/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dexie-rewards"
-version = "0.0.4"
+version = "0.0.5"
 description = "An open source Python tool which runs locally and will automatically claim rewards for all your created offers on dexie."
 authors = ["Dexie Contributors <pypi@dexie.space>"]
 license = "Apache-2.0"
 readme = "README.md"
 packages = [{ include = "dexie_rewards", from = "src" }]
 
 [tool.poetry.dependencies]
```

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/config.py` & `dexie_rewards-0.0.5/src/dexie_rewards/config.py`

 * *Files 10% similar despite different names*

```diff
@@ -30,7 +30,9 @@
 
 dexie_api_url = os.environ.get(
     "DEXIE_API_URL",
     dexie_api_mainnet if selected_network == "mainnet" else dexie_api_testnet,
 )
 
 dexie_db_path = os.environ.get("DEXIE_DB_PATH", ".")
+
+dexie_blue = "#4655FF"
```

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/decorators/with_db_connection.py` & `dexie_rewards-0.0.5/src/dexie_rewards/decorators/with_db_connection.py`

 * *Files identical despite different names*

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/decorators/with_wallet_rpc_client.py` & `dexie_rewards-0.0.5/src/dexie_rewards/decorators/with_wallet_rpc_client.py`

 * *Files identical despite different names*

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/rewards/claim.py` & `dexie_rewards-0.0.5/src/dexie_rewards/rewards/claim.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 import asyncio
+from io import StringIO
 import json
 import rich_click as click
 
 from rich.console import Console
 from rich.prompt import Confirm
 from typing import Any, List, Optional
 
@@ -71,19 +72,21 @@
 async def claim_cmds_async(
     fingerprint: Optional[int],
     verify_only: bool,
     skip_confirm: bool,
     verbose: bool,
 ) -> None:
     try:
+        console = Console(file=StringIO()) if not verbose else Console()
+
         synced_fingerprint = await wait_for_synced_wallet(fingerprint)
         await dexie_db.create_db(synced_fingerprint)
 
         offers_rewards_dict = await get_offers_with_claimable_rewards(
-            synced_fingerprint
+            synced_fingerprint, console
         )
         offers_rewards = list(map(OfferReward.from_json_dict, offers_rewards_dict))
         if len(offers_rewards) == 0:
             console.print("No rewards to claim", style="bold red")
             return
 
         display_rewards(offers_rewards)
```

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/rewards/list.py` & `dexie_rewards-0.0.5/src/dexie_rewards/rewards/list.py`

 * *Files 13% similar despite different names*

```diff
@@ -28,20 +28,31 @@
     "--json",
     "as_json",
     help="Displays offers as JSON",
     is_flag=True,
     default=False,
     show_default=True,
 )
-def list_cmds(fingerprint: Optional[int], as_json: bool) -> None:
-    asyncio.run(list_cmds_async(fingerprint, as_json))
+@click.option(
+    "-v",
+    "--verbose",
+    "verbose",
+    help="Display verbose output",
+    is_flag=True,
+    default=False,
+    show_default=True,
+)
+def list_cmds(fingerprint: Optional[int], as_json: bool, verbose: bool) -> None:
+    asyncio.run(list_cmds_async(fingerprint, as_json, verbose))
 
 
-async def list_cmds_async(fingerprint: Optional[int], as_json: bool) -> None:
-    console = Console(file=StringIO()) if as_json else Console()
+async def list_cmds_async(
+    fingerprint: Optional[int], as_json: bool, verbose: bool
+) -> None:
+    console = Console(file=StringIO()) if as_json or (not verbose) else Console()
 
     synced_fingerprint = await wait_for_synced_wallet(fingerprint, console)
     await create_db(synced_fingerprint)
 
     offers_rewards_dict = await get_offers_with_claimable_rewards(
         synced_fingerprint, console
     )
```

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/rewards/utils.py` & `dexie_rewards-0.0.5/src/dexie_rewards/rewards/utils.py`

 * *Files 3% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 from rich.text import Text
 
 from typing import Any, Dict, List, Tuple
 
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.wallet.trading.offer import Offer
 
-from ..config import dexie_api_url, dexie_url
+from ..config import dexie_api_url, dexie_blue, dexie_url
 from ..services import wallet_rpc_client as wallet_rpc_client
 from ..services.dexie_api import Api, get_dexie_bs58_offer_hash
 from ..services import dexie_db as dexie_db
 from ..types.offer_reward import OfferReward
 from ..types.utils import from_datetime
 
 
@@ -111,31 +111,28 @@
 
     table = Table(
         box=box.ROUNDED,
         show_footer=True,
     )
 
     table.add_column(
-        "Offer",
+        "Offer ID",
         justify="center",
         no_wrap=True,
-        footer=Text(
-            f"Found {num_offers} offers with total rewards", style="bold green"
-        ),
+        footer=Text(f"Found {num_offers} offers with total rewards"),
     )
     table.add_column(
         "Rewards (DBX)",
         justify="right",
-        style="bright_cyan",
-        footer=Text(f"{total_rewards}", style="bold green"),
+        footer=Text(f"{total_rewards}"),
     )
 
     for offer_reward in offers_rewards:
         offer_hash = Text(offer_reward.offer_id)
-        offer_hash.stylize("bold dodger_blue2")
+        offer_hash.stylize(f"bold {dexie_blue}")
         offer_hash.stylize(f"link {dexie_url}/offers/{offer_reward.offer_id}")
         amount = "{0:0.3f}".format(offer_reward.claimable_rewards)
         table.add_row(
             offer_hash,
             amount,
         )
```

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/services/dexie_api.py` & `dexie_rewards-0.0.5/src/dexie_rewards/services/dexie_api.py`

 * *Files identical despite different names*

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/services/dexie_db.py` & `dexie_rewards-0.0.5/src/dexie_rewards/services/dexie_db.py`

 * *Files identical despite different names*

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/services/wallet_rpc_client.py` & `dexie_rewards-0.0.5/src/dexie_rewards/services/wallet_rpc_client.py`

 * *Files identical despite different names*

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/types/offer_reward.py` & `dexie_rewards-0.0.5/src/dexie_rewards/types/offer_reward.py`

 * *Files identical despite different names*

### Comparing `dexie_rewards-0.0.4/src/dexie_rewards/utils.py` & `dexie_rewards-0.0.5/src/dexie_rewards/utils.py`

 * *Files identical despite different names*

### Comparing `dexie_rewards-0.0.4/PKG-INFO` & `dexie_rewards-0.0.5/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dexie-rewards
-Version: 0.0.4
+Version: 0.0.5
 Summary: An open source Python tool which runs locally and will automatically claim rewards for all your created offers on dexie.
 License: Apache-2.0
 Author: Dexie Contributors
 Author-email: pypi@dexie.space
 Requires-Python: >=3.11,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3
@@ -121,15 +121,27 @@
 
 ╭─ Options ───────────────────────────────────────────────────────────────────────────────────────────────╮
 │ --fingerprint  -f  INTEGER  Set the fingerprint to specify which wallet to use                          │
 │ --json         -j           Displays offers as JSON                                                     │
 │ --help                      Show this message and exit.                                                 │
 ╰─────────────────────────────────────────────────────────────────────────────────────────────────────────╯
 
-❯ dexie rewards list -f 2149823282
+❯ dexie rewards list --help
+
+ Usage: dexie rewards list [OPTIONS]
+
+╭─ Options ──────────────────────────────────────────────────────────────────────────────────────────────╮
+│ --fingerprint  -f  INTEGER  Set the fingerprint to specify which wallet to use                         │
+│ --json         -j           Displays offers as JSON                                                    │
+│ --verbose      -v           Display verbose output                                                     │
+│ --help                      Show this message and exit.                                                │
+╰────────────────────────────────────────────────────────────────────────────────────────────────────────╯
+
+
+❯ dexie rewards list -f 2149823282 --verbose
 24 new offers
 0 updated offers
 24 claimable offers
 2 offers with rewards
 ╭──────────────────────────────────────────────┬───────────────╮
 │                    Offer                     │ Rewards (DBX) │
 ├──────────────────────────────────────────────┼───────────────┤
```

