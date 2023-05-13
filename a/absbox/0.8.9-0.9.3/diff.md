# Comparing `tmp/AbsBox-0.8.9.tar.gz` & `tmp/AbsBox-0.9.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "AbsBox-0.8.9.tar", last modified: Sun Feb 26 17:27:16 2023, max compression
+gzip compressed data, was "AbsBox-0.9.3.tar", last modified: Sat Mar 18 16:16:46 2023, max compression
```

## Comparing `AbsBox-0.8.9.tar` & `AbsBox-0.9.3.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 17:27:16.850741 AbsBox-0.8.9/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 17:27:16.846741 AbsBox-0.8.9/AbsBox.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-02-26 17:27:16.000000 AbsBox-0.8.9/AbsBox.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      335 2023-02-26 17:27:16.000000 AbsBox-0.8.9/AbsBox.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-26 17:27:16.000000 AbsBox-0.8.9/AbsBox.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       76 2023-02-26 17:27:16.000000 AbsBox-0.8.9/AbsBox.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-02-26 17:27:16.000000 AbsBox-0.8.9/AbsBox.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)    11346 2023-02-26 17:27:03.000000 AbsBox-0.8.9/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-02-26 17:27:16.850741 AbsBox-0.8.9/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      785 2023-02-26 17:27:03.000000 AbsBox-0.8.9/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 17:27:16.846741 AbsBox-0.8.9/absbox/
--rw-r--r--   0 runner    (1001) docker     (123)      360 2023-02-26 17:27:03.000000 AbsBox-0.8.9/absbox/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    12355 2023-02-26 17:27:03.000000 AbsBox-0.8.9/absbox/client.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-26 17:27:16.850741 AbsBox-0.8.9/absbox/local/
--rw-r--r--   0 runner    (1001) docker     (123)     1810 2023-02-26 17:27:03.000000 AbsBox-0.8.9/absbox/local/base.py
--rw-r--r--   0 runner    (1001) docker     (123)    14216 2023-02-26 17:27:03.000000 AbsBox-0.8.9/absbox/local/china.py
--rw-r--r--   0 runner    (1001) docker     (123)    43633 2023-02-26 17:27:03.000000 AbsBox-0.8.9/absbox/local/component.py
--rw-r--r--   0 runner    (1001) docker     (123)     5886 2023-02-26 17:27:03.000000 AbsBox-0.8.9/absbox/local/generic.py
--rw-r--r--   0 runner    (1001) docker     (123)     9354 2023-02-26 17:27:03.000000 AbsBox-0.8.9/absbox/local/util.py
--rw-r--r--   0 runner    (1001) docker     (123)       79 2023-02-26 17:27:16.850741 AbsBox-0.8.9/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1647 2023-02-26 17:27:03.000000 AbsBox-0.8.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-18 16:16:46.031669 AbsBox-0.9.3/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-18 16:16:46.027669 AbsBox-0.9.3/AbsBox.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1743 2023-03-18 16:16:46.000000 AbsBox-0.9.3/AbsBox.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      335 2023-03-18 16:16:46.000000 AbsBox-0.9.3/AbsBox.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-18 16:16:46.000000 AbsBox-0.9.3/AbsBox.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       75 2023-03-18 16:16:46.000000 AbsBox-0.9.3/AbsBox.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-03-18 16:16:46.000000 AbsBox-0.9.3/AbsBox.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    11346 2023-03-18 16:16:31.000000 AbsBox-0.9.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1743 2023-03-18 16:16:46.031669 AbsBox-0.9.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      957 2023-03-18 16:16:31.000000 AbsBox-0.9.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-18 16:16:46.027669 AbsBox-0.9.3/absbox/
+-rw-r--r--   0 runner    (1001) docker     (123)      360 2023-03-18 16:16:31.000000 AbsBox-0.9.3/absbox/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12306 2023-03-18 16:16:31.000000 AbsBox-0.9.3/absbox/client.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-18 16:16:46.031669 AbsBox-0.9.3/absbox/local/
+-rw-r--r--   0 runner    (1001) docker     (123)     1810 2023-03-18 16:16:31.000000 AbsBox-0.9.3/absbox/local/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14282 2023-03-18 16:16:31.000000 AbsBox-0.9.3/absbox/local/china.py
+-rw-r--r--   0 runner    (1001) docker     (123)    45071 2023-03-18 16:16:31.000000 AbsBox-0.9.3/absbox/local/component.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5683 2023-03-18 16:16:31.000000 AbsBox-0.9.3/absbox/local/generic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9354 2023-03-18 16:16:31.000000 AbsBox-0.9.3/absbox/local/util.py
+-rw-r--r--   0 runner    (1001) docker     (123)       79 2023-03-18 16:16:46.031669 AbsBox-0.9.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1646 2023-03-18 16:16:32.000000 AbsBox-0.9.3/setup.py
```

### Comparing `AbsBox-0.8.9/AbsBox.egg-info/PKG-INFO` & `AbsBox-0.9.3/AbsBox.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AbsBox
-Version: 0.8.9
+Version: 0.9.3
 Summary: an analytical library for cashflow modeling on ABS/MBS products
 Home-page: https://github.com/yellowbean/PyABS
 Download-URL: https://github.com/yellowbean/PyABS/archive/refs/tags/pre-release.tar.gz
 Author: xiaoyu,zhang
 Author-email: always.zhang@gmail.com
 License: Apache
 Keywords: MBS,ABS,Modelling,StructuredFinance,Cashflow
@@ -21,25 +21,31 @@
 # AbsBox 
 a structured finance cashflow engine wrapper
 
 [![Python version](https://img.shields.io/pypi/pyversions/absbox)](https://img.shields.io/pypi/pyversions/absbox)
 [![PyPI version](https://badge.fury.io/py/absbox.svg)](https://badge.fury.io/py/absbox)
 [![PyPI download](https://img.shields.io/pypi/dm/absbox)](https://img.shields.io/pypi/dm/absbox)
 
-
 ## installation
 
     pip install absbox
 
 ## Goals
 * Provide building blocks to create cashflow models for ABS/MBS
-* Adapt to multiple asset class
+* Adapt to multiple asset classes
     * Residential Mortgage / Auto Loans
     * Corp Loans
     * Consumer Credit
+    * Lease
 * Features
   * Sensitivity Analysis on different scenarios
   * Bond Cashflow Forecast, Pricing
+  * Tweaking on deal components
+
+## Data flow
+
+![image](https://user-images.githubusercontent.com/1008321/221366747-5e37fc9e-dfaa-44b5-ab00-f5c8a3b26d79.png)
+
 
 ## Documentation
 * English -> https://absbox-doc.readthedocs.io
 * Chinese -> https://absbox.readthedocs.io
```

### Comparing `AbsBox-0.8.9/LICENSE` & `AbsBox-0.9.3/LICENSE`

 * *Files identical despite different names*

### Comparing `AbsBox-0.8.9/PKG-INFO` & `AbsBox-0.9.3/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AbsBox
-Version: 0.8.9
+Version: 0.9.3
 Summary: an analytical library for cashflow modeling on ABS/MBS products
 Home-page: https://github.com/yellowbean/PyABS
 Download-URL: https://github.com/yellowbean/PyABS/archive/refs/tags/pre-release.tar.gz
 Author: xiaoyu,zhang
 Author-email: always.zhang@gmail.com
 License: Apache
 Keywords: MBS,ABS,Modelling,StructuredFinance,Cashflow
@@ -21,25 +21,31 @@
 # AbsBox 
 a structured finance cashflow engine wrapper
 
 [![Python version](https://img.shields.io/pypi/pyversions/absbox)](https://img.shields.io/pypi/pyversions/absbox)
 [![PyPI version](https://badge.fury.io/py/absbox.svg)](https://badge.fury.io/py/absbox)
 [![PyPI download](https://img.shields.io/pypi/dm/absbox)](https://img.shields.io/pypi/dm/absbox)
 
-
 ## installation
 
     pip install absbox
 
 ## Goals
 * Provide building blocks to create cashflow models for ABS/MBS
-* Adapt to multiple asset class
+* Adapt to multiple asset classes
     * Residential Mortgage / Auto Loans
     * Corp Loans
     * Consumer Credit
+    * Lease
 * Features
   * Sensitivity Analysis on different scenarios
   * Bond Cashflow Forecast, Pricing
+  * Tweaking on deal components
+
+## Data flow
+
+![image](https://user-images.githubusercontent.com/1008321/221366747-5e37fc9e-dfaa-44b5-ab00-f5c8a3b26d79.png)
+
 
 ## Documentation
 * English -> https://absbox-doc.readthedocs.io
 * Chinese -> https://absbox.readthedocs.io
```

### Comparing `AbsBox-0.8.9/README.md` & `AbsBox-0.9.3/README.md`

 * *Files 17% similar despite different names*

```diff
@@ -1,25 +1,31 @@
 # AbsBox 
 a structured finance cashflow engine wrapper
 
 [![Python version](https://img.shields.io/pypi/pyversions/absbox)](https://img.shields.io/pypi/pyversions/absbox)
 [![PyPI version](https://badge.fury.io/py/absbox.svg)](https://badge.fury.io/py/absbox)
 [![PyPI download](https://img.shields.io/pypi/dm/absbox)](https://img.shields.io/pypi/dm/absbox)
 
-
 ## installation
 
     pip install absbox
 
 ## Goals
 * Provide building blocks to create cashflow models for ABS/MBS
-* Adapt to multiple asset class
+* Adapt to multiple asset classes
     * Residential Mortgage / Auto Loans
     * Corp Loans
     * Consumer Credit
+    * Lease
 * Features
   * Sensitivity Analysis on different scenarios
   * Bond Cashflow Forecast, Pricing
+  * Tweaking on deal components
+
+## Data flow
+
+![image](https://user-images.githubusercontent.com/1008321/221366747-5e37fc9e-dfaa-44b5-ab00-f5c8a3b26d79.png)
+
 
 ## Documentation
 * English -> https://absbox-doc.readthedocs.io
 * Chinese -> https://absbox.readthedocs.io
```

### Comparing `AbsBox-0.8.9/absbox/client.py` & `AbsBox-0.9.3/absbox/client.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,18 +11,17 @@
 from pyspecter import S,query
 
 urllib3.disable_warnings()
 
 @dataclass
 class API:
     url:str
-    #lang = field(repr=False, default="chinese")
     lang:str = "chinese"
     server_info = {}
-    version:tuple = "0","8","1"
+    version:tuple = "0","9","1"
     hdrs = {'Content-type': 'application/json', 'Accept': 'text/plain'}
 
     def __post_init__(self):
         try:
             _r = requests.get(f"{self.url}/version",verify=False).text
         except (ConnectionRefusedError, ConnectionError):
             logging.error(f"Error: Can't not connect to API server {self.url}")
```

### Comparing `AbsBox-0.8.9/absbox/local/base.py` & `AbsBox-0.9.3/absbox/local/base.py`

 * *Files identical despite different names*

### Comparing `AbsBox-0.8.9/absbox/local/china.py` & `AbsBox-0.9.3/absbox/local/china.py`

 * *Files 2% similar despite different names*

```diff
@@ -135,15 +135,15 @@
     def read_assump(self, assump):
         if assump:
             return [mkAssumption(a) for a in assump]
         return None
 
     def read_pricing(self, pricing):
         if pricing:
-            return mkComponent(pricing)
+            return mkPricingAssump(pricing)
         return None
 
     def read(self, resp, position=None):
         read_paths = {'bonds': ('bndStmt', china_bondflow_fields, "债券")
                     , 'fees': ('feeStmt', china_fee_flow_fields_d, "费用")
                     , 'accounts': ('accStmt', china_acc_flow_fields_d , "账户")
                     , 'liqProvider': ('liqStmt', china_liq_flow_fields_d, "流动性支持")
@@ -185,17 +185,18 @@
 
         _pool_cf_header,_ = guess_pool_flow_header(resp[0]['pool']['futureCf'][0],"chinese")
         output['pool']['flow'] = pd.DataFrame([_['contents'] for _ in resp[0]['pool']['futureCf']]
                                               , columns=_pool_cf_header)
         output['pool']['flow'] = output['pool']['flow'].set_index("日期")
         output['pool']['flow'].index.rename("日期", inplace=True)
 
-        output['pricing'] = pd.DataFrame.from_dict(resp[3]
-                                                   , orient='index'
-                                                   , columns=["估值", "票面估值", "WAL", "久期", "应计利息"]).sort_index() if resp[3] else None
+        #output['pricing'] = pd.DataFrame.from_dict(resp[3]
+        #                                          , orient='index'
+        #                                          , columns=["估值", "票面估值", "WAL", "久期", "应计利息"]).sort_index() if resp[3] else None
+        output['pricing'] = readPricingResult(resp[3], 'cn')
         if position:
             output['position'] = {}
             for k,v in position.items():
                 if k in output['bonds']:
                     b = self._get_bond(k)
                     factor = v / b["初始余额"] / 100
                     if factor > 1.0:
```

### Comparing `AbsBox-0.8.9/absbox/local/component.py` & `AbsBox-0.9.3/absbox/local/component.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 from absbox.local.util import mkTag,DC,mkTs
 from enum import Enum
 import itertools
 
-from pyspecter import query
+import pandas as pd
+from pyspecter import query,S
 
 datePattern = {"月末":"MonthEnd"
               ,"季度末":"QuarterEnd"
               ,"年末":"YearEnd"
               ,"月初":"MonthFirst"
               ,"季度初":"QuarterFirst"
               ,"年初":"YearFirst"
@@ -114,14 +115,16 @@
                     raise RuntimeError(f"Failed to match on 百分比费率：{desc,rate}")
         case {"固定费用": amt} | {"fixFee": amt}:
             return mkTag(("FixFee", amt))
         case {"周期费用": [p, amt]} | {"recurFee": [p, amt]}:
             return mkTag(("RecurFee", [mkDatePattern(p), amt]))
         case {"自定义": fflow} | {"customFee": fflow}:
             return mkTag(("FeeFlow",mkTs("BalanceCurve",fflow)))
+        case {"计数费用": [p,s,amt]} | {"numFee": [p,s,amt]}:
+            return mkTag(("NumFee",[mkDatePattern(p),mkDs(s),amt]))
         case _ :
             raise RuntimeError(f"Failed to match on fee type:{x}")
 
 def mkDateVector(x):
     match x:
         case dp if isinstance(dp,str):
             return mkTag(datePattern[dp])
@@ -162,14 +165,16 @@
             return mkTag(("Factor",[mkDs(ds),f]))
         case ("债券待付利息",*bnds) | ("bondDueInt",*bnds):
             return mkTag(("CurrentDueBondInt",bnds))
         case ("债券已付利息",*bnds) | ("lastBondIntPaid",*bnds):
             return mkTag(("LastBondIntPaid",bnds))
         case ("债券低于目标余额",bn) | ("behindTargetBalance",bn):
             return mkTag(("BondBalanceGap",bn))
+        case ("债务人数量",) | ("borrowerNumber",):
+            return mkTag(("CurrentPoolBorrowerNum"))
         
         #   , "当期已付债券利息":"LastBondIntPaid"
         #   , "当期已付费用" :"LastFeePaid"
         #   , "当期未付债券利息" :"CurrentDueBondInt"
         #   , "当期未付费用": "CurrentDueFee"
   
         case ("待付费用",*fns) | ("feeDue",*fns):
@@ -717,29 +722,30 @@
                                       } | mkTag("LoanOriginalInfo"),
                                      currentBalance,
                                      currentRate,
                                      remainTerms,
                                      _statusMapping[status]]))       
         case ["分期"
             ,{"放款金额": originBalance, "放款费率": originRate, "初始期限": originTerm
-                  ,"频率": freq, "类型": _type, "放款日": startDate}
+                  ,"频率": freq, "类型": _type, "放款日": startDate, "剩余期限":remainTerms}
             ,{"当前余额":currentBalance, "状态": status}] \
             |["Installment"
             ,{"originBalance": originBalance, "feeRate": originRate, "originTerm": originTerm
-                  ,"freq": freq, "type": _type, "originDate": startDate}
+                  ,"freq": freq, "type": _type, "originDate": startDate, "remainTerm":remainTerms}
             ,{"currentBalance":currentBalance,"status": status}]:
             return mkTag(("Installment",[
                                       {"originBalance": originBalance,
                                       "originRate": mkAssetRate(originRate),
                                       "originTerm": originTerm,
                                       "period": freqMap[freq],
                                       "startDate": startDate,
                                       "prinType": mkAmortPlan(_type)
                                       } | mkTag("LoanOriginalInfo"),
                                      currentBalance,
+                                     remainTerms,
                                      _statusMapping[status]]))       
         case ["租赁"
                 ,{"固定租金": dailyRate, "初始期限": originTerm
                   ,"频率": dp, "起始日": startDate,"状态":status,"剩余期限":remainTerms}] \
             |["Lease"
                 ,{"fixRental": dailyRate, "originTerm": originTerm
                   ,"freq": dp, "originDate": startDate, "status":status,"remainTerm":remainTerms}]:
@@ -942,24 +948,45 @@
             return mkBnd(bndName, bnd)
         case ["归集规则", collection]:
             return mkCollection(collection)
         #case ["清仓回购", calls]:
         #    return mkCall(calls)
 
 
-def mkComponent(x):
+def mkPricingAssump(x):
     match x:
-        case {"贴现日": pricingDay, "贴现曲线": xs}:
-            return [pricingDay, {"tag": "PricingCurve", "contents": xs}]
-        case {"PVDate": pricingDay, "PVCurve": xs}:
-            return [pricingDay, {"tag": "PricingCurve", "contents": xs}]
+        case {"贴现日": pricingDay, "贴现曲线": xs} | {"PVDate": pricingDay, "PVCurve": xs}:
+            # return [pricingDay, {"tag": "PricingCurve", "contents": xs}]
+            return mkTag(("DiscountCurve",[pricingDay, mkTs("IRateCurve",xs)]))
+        case {"债券":bnd_with_price,"利率曲线":rdps} | {"bonds":bnd_with_price,"curve":rdps}:
+            return mkTag(("RunZSpread",[mkTs("IRateCurve",rdps) ,bnd_with_price ]))
         case _:
-            None
+            raise RuntimeError(f"Failed to match pricing assumption: {x}")
+
+# "{\"tag\":\"RunZSpread\",\"contents\":[{\"tag\":\"IRateCurve\",\"contents\":[[\"2020-01-01\",1.0e-2]]}
+#                                        ,{\"A\":[\"2021-01-01\",100.3]}]}"
 
 def mkLiqProviderType(x):
     match x:
         case {"总额度": amt} | {"Total": amt}:
             return mkTag(("FixSupport"))
         case {"日期":dp, "限额":amt} | {"Reset":dp, "Quota":amt}:
             return mkTag(("ReplenishSupport", [mkDatePattern(dp),amt]))
         case {}:
-            return mkTag(("UnLimit"))            
+            return mkTag(("UnLimit"))            
+
+
+def readPricingResult(x, locale)->dict:
+    if x is None:
+        return None
+    h = None
+
+    tag = query(x,[S.MVALS,S.ALL,"tag"])[0]
+    if tag=="PriceResult":
+        h = {"cn": ["估值", "票面估值", "WAL", "久期", "凸性", "应计利息"],
+                "en":["pricing", "face", "WAL", "duration","convexity", "accure interest"]}
+    elif tag=="ZSpread":
+        h = {"cn":["静态利差"], "en":["Z-spread"]}
+    else:
+        raise RuntimeError(f"Failed to read princing result: {x} with tag={tag}")
+
+    return pd.DataFrame.from_dict({k:v['contents'] for k,v in x.items()} , orient='index', columns=h[locale]).sort_index()
```

### Comparing `AbsBox-0.8.9/absbox/local/generic.py` & `AbsBox-0.9.3/absbox/local/generic.py`

 * *Files 6% similar despite different names*

```diff
@@ -78,15 +78,15 @@
     def read_assump(self, assump):
         if assump:
             return [mkAssumption(a) for a in assump]
         return None
 
     def read_pricing(self, pricing):
         if pricing:
-            return mkComponent(pricing)
+            return mkPricingAssump(pricing)
         return None
 
     def read(self, resp, position=None):
         read_paths = {'bonds': ('bndStmt' , english_bondflow_fields , "bond")
                      , 'fees': ('feeStmt' , english_fee_flow_fields_d , "fee")
                      , 'accounts': ('accStmt' , english_acc_flow_fields_d , "account")}
         output = {}
@@ -122,12 +122,10 @@
         output['pool'] = {}
         output['pool']['flow'] = pd.DataFrame([_['contents'] for _ in resp[0]['pool']['futureCf']]
                                               , columns=english_mortgage_flow_fields_d)
         pool_idx = 'Date'
         output['pool']['flow'] = output['pool']['flow'].set_index(pool_idx)
         output['pool']['flow'].index.rename(pool_idx, inplace=True)
 
-        output['pricing'] = pd.DataFrame.from_dict(resp[3]
-                                                   , orient='index'
-                                                   , columns=["pricing", "face", "WAL", "duration", "accure interest"]) if resp[3] else None
+        output['pricing'] = readPricingResult(resp[3], 'en')
 
         return output
```

### Comparing `AbsBox-0.8.9/absbox/local/util.py` & `AbsBox-0.9.3/absbox/local/util.py`

 * *Files identical despite different names*

### Comparing `AbsBox-0.8.9/setup.py` & `AbsBox-0.9.3/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -11,15 +11,15 @@
     setup(
         name = 'AbsBox',
         package_dir = {
             'absbox':'absbox',
             'absbox.local':local
         },
         packages = ['absbox','absbox.local'],
-        version = '0.8.9',
+        version = '0.9.3',
         license='Apache',
         description = 'an analytical library for cashflow modeling on ABS/MBS products',
         long_description_content_type='text/markdown',
         long_description = long_description,
         author = 'xiaoyu,zhang',
         author_email = 'always.zhang@gmail.com',
         url = 'https://github.com/yellowbean/PyABS',
@@ -28,15 +28,15 @@
         install_requires=[
             'requests',
             'pandas',
             'pyxirr',
             'matplotlib',
             'pyspecter',
             'numpy',
-            'pystest',
+            'pytest',
             'jsondiff',
             'deepdiff'
         ],
         classifiers=[
             'Development Status :: 3 - Alpha',
             'Intended Audience :: Developers',
             'Intended Audience :: Financial and Insurance Industry',
```

