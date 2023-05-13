# Comparing `tmp/frostaura-1.0.8.tar.gz` & `tmp/frostaura-1.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "frostaura-1.0.8.tar", last modified: Thu Aug 11 20:57:35 2022, max compression
+gzip compressed data, was "frostaura-1.0.9.tar", last modified: Thu Aug 11 22:53:10 2022, max compression
```

## Comparing `frostaura-1.0.8.tar` & `frostaura-1.0.9.tar`

### file list

```diff
@@ -1,38 +1,40 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:35.168813 frostaura-1.0.8/
--rw-r--r--   0 runner    (1001) docker     (121)     1065 2022-08-11 20:57:24.000000 frostaura-1.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       25 2022-08-11 20:57:24.000000 frostaura-1.0.8/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)     2319 2022-08-11 20:57:35.168813 frostaura-1.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     1567 2022-08-11 20:57:24.000000 frostaura-1.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:35.164813 frostaura-1.0.8/frostaura/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:35.168813 frostaura-1.0.8/frostaura/data_access/
--rw-r--r--   0 runner    (1001) docker     (121)      708 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/data_access/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      478 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/data_access/personal_asset_data_access.py
--rw-r--r--   0 runner    (1001) docker     (121)     3366 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/data_access/personal_asset_data_access__easy_equities.py
--rw-r--r--   0 runner    (1001) docker     (121)      347 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/data_access/public_asset_data_access.py
--rw-r--r--   0 runner    (1001) docker     (121)      635 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/data_access/public_asset_data_access__yahoo_finance.py
--rw-r--r--   0 runner    (1001) docker     (121)      295 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/data_access/resources_data_access.py
--rw-r--r--   0 runner    (1001) docker     (121)      925 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/data_access/resources_data_access__embedded.py
--rw-r--r--   0 runner    (1001) docker     (121)     1326 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/data_access/resources_data_access__html.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:35.168813 frostaura-1.0.8/frostaura/engines/
--rw-r--r--   0 runner    (1001) docker     (121)      406 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/engines/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      656 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/engines/asset_calculations_engine.py
--rw-r--r--   0 runner    (1001) docker     (121)     3019 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/engines/asset_calculations_engine__simple.py
--rw-r--r--   0 runner    (1001) docker     (121)      365 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/engines/asset_valuation_engine.py
--rw-r--r--   0 runner    (1001) docker     (121)     4640 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/engines/asset_valuation_engine__finviz.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:35.168813 frostaura-1.0.8/frostaura/managers/
--rw-r--r--   0 runner    (1001) docker     (121)      116 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/managers/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:35.168813 frostaura-1.0.8/frostaura/models/
--rw-r--r--   0 runner    (1001) docker     (121)      198 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      291 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/models/profit_calculation_result.py
--rw-r--r--   0 runner    (1001) docker     (121)      881 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/models/valuation_result.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:35.168813 frostaura-1.0.8/frostaura/resources/
--rw-r--r--   0 runner    (1001) docker     (121)    21657 2022-08-11 20:57:24.000000 frostaura-1.0.8/frostaura/resources/easy_equities_us_stocks.json
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 20:57:35.168813 frostaura-1.0.8/frostaura.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     2319 2022-08-11 20:57:35.000000 frostaura-1.0.8/frostaura.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     1052 2022-08-11 20:57:35.000000 frostaura-1.0.8/frostaura.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-08-11 20:57:35.000000 frostaura-1.0.8/frostaura.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       10 2022-08-11 20:57:35.000000 frostaura-1.0.8/frostaura.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)      103 2022-08-11 20:57:24.000000 frostaura-1.0.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-08-11 20:57:35.168813 frostaura-1.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1236 2022-08-11 20:57:24.000000 frostaura-1.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 22:53:10.615135 frostaura-1.0.9/
+-rw-r--r--   0 runner    (1001) docker     (121)     1065 2022-08-11 22:52:55.000000 frostaura-1.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (121)       25 2022-08-11 22:52:55.000000 frostaura-1.0.9/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (121)     2319 2022-08-11 22:53:10.615135 frostaura-1.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     1567 2022-08-11 22:52:55.000000 frostaura-1.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 22:53:10.607135 frostaura-1.0.9/frostaura/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 22:53:10.611135 frostaura-1.0.9/frostaura/data_access/
+-rw-r--r--   0 runner    (1001) docker     (121)      708 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/data_access/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      478 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/data_access/personal_asset_data_access.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3366 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/data_access/personal_asset_data_access__easy_equities.py
+-rw-r--r--   0 runner    (1001) docker     (121)      347 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/data_access/public_asset_data_access.py
+-rw-r--r--   0 runner    (1001) docker     (121)      635 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/data_access/public_asset_data_access__yahoo_finance.py
+-rw-r--r--   0 runner    (1001) docker     (121)      295 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/data_access/resources_data_access.py
+-rw-r--r--   0 runner    (1001) docker     (121)      925 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/data_access/resources_data_access__embedded.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1326 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/data_access/resources_data_access__html.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 22:53:10.611135 frostaura-1.0.9/frostaura/engines/
+-rw-r--r--   0 runner    (1001) docker     (121)      573 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/engines/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      861 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/engines/asset_calculations_engine.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3853 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/engines/asset_calculations_engine__simple.py
+-rw-r--r--   0 runner    (1001) docker     (121)      434 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/engines/asset_projection_engine.py
+-rw-r--r--   0 runner    (1001) docker     (121)      573 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/engines/asset_projection_engine__simple.py
+-rw-r--r--   0 runner    (1001) docker     (121)      365 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/engines/asset_valuation_engine.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4769 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/engines/asset_valuation_engine__finviz.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 22:53:10.611135 frostaura-1.0.9/frostaura/managers/
+-rw-r--r--   0 runner    (1001) docker     (121)      116 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/managers/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 22:53:10.615135 frostaura-1.0.9/frostaura/models/
+-rw-r--r--   0 runner    (1001) docker     (121)      198 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      291 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/models/profit_calculation_result.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1002 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/models/valuation_result.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 22:53:10.615135 frostaura-1.0.9/frostaura/resources/
+-rw-r--r--   0 runner    (1001) docker     (121)    21657 2022-08-11 22:52:55.000000 frostaura-1.0.9/frostaura/resources/easy_equities_us_stocks.json
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-11 22:53:10.611135 frostaura-1.0.9/frostaura.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     2319 2022-08-11 22:53:10.000000 frostaura-1.0.9/frostaura.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     1150 2022-08-11 22:53:10.000000 frostaura-1.0.9/frostaura.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-08-11 22:53:10.000000 frostaura-1.0.9/frostaura.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       10 2022-08-11 22:53:10.000000 frostaura-1.0.9/frostaura.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)      103 2022-08-11 22:52:55.000000 frostaura-1.0.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-08-11 22:53:10.615135 frostaura-1.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     1236 2022-08-11 22:52:55.000000 frostaura-1.0.9/setup.py
```

### Comparing `frostaura-1.0.8/LICENSE` & `frostaura-1.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `frostaura-1.0.8/PKG-INFO` & `frostaura-1.0.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: frostaura
-Version: 1.0.8
+Version: 1.0.9
 Summary: FrostAura provides a range of open-source components provide a variety of problem domains.
 Home-page: https://github.com/faGH/fa.intelligence.notebooks
 Author: Dean Martin
 Author-email: dean.martin@frostaura.net
 Keywords: frostaura,deep learning,machine learning,market analysis,bots,visualization,data exploration,data analysis,statistics,neural networks
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

### Comparing `frostaura-1.0.8/README.md` & `frostaura-1.0.9/README.md`

 * *Files identical despite different names*

### Comparing `frostaura-1.0.8/frostaura/data_access/__init__.py` & `frostaura-1.0.9/frostaura/data_access/__init__.py`

 * *Files identical despite different names*

### Comparing `frostaura-1.0.8/frostaura/data_access/personal_asset_data_access__easy_equities.py` & `frostaura-1.0.9/frostaura/data_access/personal_asset_data_access__easy_equities.py`

 * *Files identical despite different names*

### Comparing `frostaura-1.0.8/frostaura/data_access/public_asset_data_access__yahoo_finance.py` & `frostaura-1.0.9/frostaura/data_access/public_asset_data_access__yahoo_finance.py`

 * *Files identical despite different names*

### Comparing `frostaura-1.0.8/frostaura/data_access/resources_data_access__embedded.py` & `frostaura-1.0.9/frostaura/data_access/resources_data_access__embedded.py`

 * *Files identical despite different names*

### Comparing `frostaura-1.0.8/frostaura/data_access/resources_data_access__html.py` & `frostaura-1.0.9/frostaura/data_access/resources_data_access__html.py`

 * *Files identical despite different names*

### Comparing `frostaura-1.0.8/frostaura/engines/asset_calculations_engine__simple.py` & `frostaura-1.0.9/frostaura/engines/asset_calculations_engine__simple.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 '''This module defines calculations engine components.'''
 from datetime import datetime
+from logging import debug
 import pandas as pd
 from frostaura.data_access.public_asset_data_access import IPublicAssetDataAccess
 from frostaura.engines.asset_calculations_engine import IAssetCalculationsEngine
 from frostaura.models import ProfitCalculationResult
 
 class SimpleAssetCalculationsEngine(IAssetCalculationsEngine):
     '''Calculations-related functionality using some maths under-the-hood.'''
@@ -13,25 +14,29 @@
 
     def interpolate_holdings_profits(self, holdings: dict) -> dict:
         '''Determine individual asset profit ratio & profit USD and interpolate them into a copy of the given holdings.'''
 
         __holdings__: dict = holdings.copy()
 
         for holding_symbol in __holdings__:
+            debug(f'Calculating profit for asset "{holding_symbol}".')
+
             context: dict = __holdings__[holding_symbol]
             history: pd.DataFrame = self.public_asset_data_access.get_symbol_history(symbol=context['symbol'])
             transactions_by_date_asc: list = sorted(context['transactions'], key=lambda i: i['date'])
             total_purchased_usd: float = 0
             total_purchased_shares: float = 0
 
             for transaction in transactions_by_date_asc:
                 transaction_date: datetime = transaction['date']
                 transaction_value: float = transaction['value']
                 transaction_close: float = history.loc[transaction_date].Close
 
+                debug(f'[{holding_symbol}] Processing transaction value ${transaction_value} on {transaction_date}.')
+
                 transaction['usd'] = transaction_close * transaction_value
                 total_purchased_usd += transaction_close * transaction_value
                 total_purchased_shares += transaction_value
 
             total_current_usd: float = history.iloc[-1].Close * total_purchased_shares
             context['total_purchased_usd'] = total_purchased_usd
             context['total_purchased_shares'] = total_purchased_shares
@@ -40,14 +45,29 @@
             context['total_profit_usd'] = total_current_usd - total_purchased_usd
 
         return __holdings__
 
     def calculate_holdings_profit(self, holdings: dict) -> ProfitCalculationResult:
         '''Determine the holdings profit percentage & profit USD, given the holdings.'''
 
+        debug('Calculating overall holdings profits.')
+
         holdings: dict = self.interpolate_holdings_profits(holdings=holdings)
         total_purchased_usd: float = sum([holdings[k]['total_purchased_usd'] for k in holdings])
         total_current_usd: float = sum([holdings[k]['total_current_usd'] for k in holdings])
         total_profit_ratio: float = (1 - min(total_purchased_usd, total_current_usd) / max(total_purchased_usd, total_current_usd)) * 100
         total_profit_usd: float = total_current_usd - total_purchased_usd
 
         return ProfitCalculationResult(percentage=total_profit_ratio, value=total_profit_usd)
+
+    def calculate_holdings_ratios(self, holdings: dict) -> dict:
+        '''Determine the ratios that each asset makes up of the overall portfolio adding up to 1.'''
+
+        labels: list = [h for h in holdings]
+        transactions = [holdings[h]['transactions'] for h in holdings]
+        transactions = [sum([ti['usd'] for ti in t]) for t in transactions]
+        holding_ratios: dict = {}
+
+        for label_index, label in enumerate(labels):
+            holding_ratios[label] = transactions[label_index] / sum(transactions)
+
+        return holding_ratios
```

### Comparing `frostaura-1.0.8/frostaura/engines/asset_valuation_engine__finviz.py` & `frostaura-1.0.9/frostaura/engines/asset_valuation_engine__finviz.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 '''This module defines valuation engine components.'''
+from logging import debug
 from frostaura.data_access import IResourcesDataAccess
 from frostaura.models.valuation_result import ValuationResult
 from frostaura.engines.asset_valuation_engine import IAssetValuationEngine
 
 class FinvizAssetValuationEngine(IAssetValuationEngine):
     '''Valuation-related functionality using Finviz under-the-hood.'''
 
@@ -67,24 +68,27 @@
                                             .find_next(class_='snapshot-td2')
                                             .text
                                             .split('%')[0])
 
         if '-' not in annual_dividend_percentage_str:
             annual_dividend_percentage = float(annual_dividend_percentage_str)
 
-        print(f'EPS: {eps_ttm}, EPS Next 5 Years: {eps_five_years}%')
-        print(f'P/E Ratio: {avg_pe_ratio}, Current Price: $ {current_price}')
+        debug(f'EPS: {eps_ttm}, EPS Next 5 Years: {eps_five_years}%')
+        debug(f'P/E Ratio: {avg_pe_ratio}, Current Price: $ {current_price}')
 
         intrinsic_value: float = self.__determine_intrinsic_value__(eps_ttm=eps_ttm,
                             growth_rate=eps_five_years,
                             pe_ratio=avg_pe_ratio,
                             margin_of_safety=0.3)
 
-        print(f'Intrinsic Value: $ {intrinsic_value} vs. Current Price: $ {current_price}')
+        debug(f'Intrinsic Value: $ {intrinsic_value} vs. Current Price: $ {current_price}')
 
         return ValuationResult(
             symbol=symbol,
             company_name=company_name,
             current_price=current_price,
             valuation_price=intrinsic_value,
-            annual_dividend_percentage=annual_dividend_percentage
+            annual_dividend_percentage=annual_dividend_percentage,
+            eps_ttm=eps_ttm,
+            eps_five_years=eps_five_years,
+            pe_ratio=pe_ratio
         )
```

### Comparing `frostaura-1.0.8/frostaura/models/valuation_result.py` & `frostaura-1.0.9/frostaura/models/valuation_result.py`

 * *Files 20% similar despite different names*

```diff
@@ -5,16 +5,20 @@
 
     def __init__(self,
                  symbol: str,
                  company_name: str,
                  current_price: float,
                  valuation_price: float,
                  annual_dividend_percentage: float,
-                 purchased_price: float = None):
+                 eps_ttm: float,
+                 eps_five_years: float,
+                 pe_ratio: float):
         self.symbol = symbol
         self.company_name = company_name
         self.current_price = current_price
         self.valuation_price = valuation_price
         self.absolute_current_v_valuation_delta = 1 - (min(valuation_price, current_price) / max(valuation_price, current_price))
         self.is_overvalued = valuation_price < current_price
         self.annual_dividend_percentage = annual_dividend_percentage
-        self.purchased_price = purchased_price
+        self.eps_ttm = eps_ttm
+        self.eps_five_years = eps_five_years
+        self.pe_ratio = pe_ratio
```

### Comparing `frostaura-1.0.8/frostaura/resources/easy_equities_us_stocks.json` & `frostaura-1.0.9/frostaura/resources/easy_equities_us_stocks.json`

 * *Files identical despite different names*

### Comparing `frostaura-1.0.8/frostaura.egg-info/PKG-INFO` & `frostaura-1.0.9/frostaura.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: frostaura
-Version: 1.0.8
+Version: 1.0.9
 Summary: FrostAura provides a range of open-source components provide a variety of problem domains.
 Home-page: https://github.com/faGH/fa.intelligence.notebooks
 Author: Dean Martin
 Author-email: dean.martin@frostaura.net
 Keywords: frostaura,deep learning,machine learning,market analysis,bots,visualization,data exploration,data analysis,statistics,neural networks
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

### Comparing `frostaura-1.0.8/frostaura.egg-info/SOURCES.txt` & `frostaura-1.0.9/frostaura.egg-info/SOURCES.txt`

 * *Files 9% similar despite different names*

```diff
@@ -15,14 +15,16 @@
 frostaura/data_access/public_asset_data_access__yahoo_finance.py
 frostaura/data_access/resources_data_access.py
 frostaura/data_access/resources_data_access__embedded.py
 frostaura/data_access/resources_data_access__html.py
 frostaura/engines/__init__.py
 frostaura/engines/asset_calculations_engine.py
 frostaura/engines/asset_calculations_engine__simple.py
+frostaura/engines/asset_projection_engine.py
+frostaura/engines/asset_projection_engine__simple.py
 frostaura/engines/asset_valuation_engine.py
 frostaura/engines/asset_valuation_engine__finviz.py
 frostaura/managers/__init__.py
 frostaura/models/__init__.py
 frostaura/models/profit_calculation_result.py
 frostaura/models/valuation_result.py
 frostaura/resources/easy_equities_us_stocks.json
```

### Comparing `frostaura-1.0.8/setup.py` & `frostaura-1.0.9/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 from pathlib import Path
 
 ROOT_DIR = Path(__file__).parent
-VERSION = '1.0.8' 
+VERSION = '1.0.9' 
 DESCRIPTION = 'FrostAura provides a range of open-source components provide a variety of problem domains.'
 LONG_DESCRIPTION = (ROOT_DIR / 'README.md').read_text()
 
 setup(
     name='frostaura', 
     version=VERSION,
     author='Dean Martin',
```

