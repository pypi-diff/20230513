# Comparing `tmp/alacorder-80.4.4.tar.gz` & `tmp/alacorder-80.4.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "alacorder-80.4.4.tar", max compression
+gzip compressed data, was "alacorder-80.4.5.tar", max compression
```

## Comparing `alacorder-80.4.4.tar` & `alacorder-80.4.5.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0     1066 2023-02-07 05:47:31.000000 alacorder-80.4.4/LICENSE
--rw-r--r--   0        0        0     6592 2023-05-11 17:12:36.043202 alacorder-80.4.4/README.md
--rw-r--r--   0        0        0      697 2023-05-12 18:33:16.155816 alacorder-80.4.4/pyproject.toml
--rw-r--r--   0        0        0     6148 2023-05-12 18:32:14.158198 alacorder-80.4.4/src/alacorder/.DS_Store
--rw-r--r--   0        0        0        0 2023-05-02 17:21:37.916960 alacorder-80.4.4/src/alacorder/__init__.py
--rw-r--r--   0        0        0   214884 2023-05-12 18:33:19.717988 alacorder-80.4.4/src/alacorder/__main__.py
--rw-r--r--   0        0        0   214884 2023-05-12 18:33:23.767750 alacorder-80.4.4/src/alacorder/alac.py
--rw-r--r--   0        0        0     7521 1970-01-01 00:00:00.000000 alacorder-80.4.4/PKG-INFO
+-rw-r--r--   0        0        0     1066 2023-02-07 05:47:31.000000 alacorder-80.4.5/LICENSE
+-rw-r--r--   0        0        0     6592 2023-05-11 17:12:36.043202 alacorder-80.4.5/README.md
+-rw-r--r--   0        0        0      697 2023-05-13 00:25:53.254280 alacorder-80.4.5/pyproject.toml
+-rw-r--r--   0        0        0     6148 2023-05-12 20:56:24.759768 alacorder-80.4.5/src/alacorder/.DS_Store
+-rw-r--r--   0        0        0        0 2023-05-02 17:21:37.916960 alacorder-80.4.5/src/alacorder/__init__.py
+-rw-r--r--   0        0        0   216607 2023-05-13 00:24:46.913968 alacorder-80.4.5/src/alacorder/__main__.py
+-rw-r--r--   0        0        0   216607 2023-05-13 00:24:25.240970 alacorder-80.4.5/src/alacorder/alac.py
+-rw-r--r--   0        0        0     7521 1970-01-01 00:00:00.000000 alacorder-80.4.5/PKG-INFO
```

### Comparing `alacorder-80.4.4/LICENSE` & `alacorder-80.4.5/LICENSE`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.4/README.md` & `alacorder-80.4.5/README.md`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.4/pyproject.toml` & `alacorder-80.4.5/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "alacorder"
-version = "80.4.4"
+version = "80.4.5"
 description = "Alacorder collects and processes Alacourt case detail PDFs into data tables suitable for research purposes."
 authors = ["Sam Robson <sbrobson@crimson.ua.edu>"]
 license = "MIT LICENSE"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.9"
```

### Comparing `alacorder-80.4.4/src/alacorder/.DS_Store` & `alacorder-80.4.5/src/alacorder/.DS_Store`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.4/src/alacorder/__main__.py` & `alacorder-80.4.5/src/alacorder/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,24 +10,24 @@
     polars ^0.17.6, PyMuPDF ^1.21.1, 
     PySimpleGUI ^4.60.4, selenium ^4.8.3, 
     tqdm ^4.65.0, xlsx2csv ^0.8.1, XlsxWriter ^3.0.9
 """
 
 name = "ALACORDER"
 long_version = "snowpalace"
-version = "80.4.4"
+version = "80.4.5"
 
 _autoload_graphical_user_interface = False
 
 import polars as pl
 import os, sys, time, glob, re, math
 import click, fitz, selenium, xlsxwriter
 from tqdm.auto import tqdm
-from datetime import datetime
 from random import sample
+from datetime import datetime
 from selenium import webdriver
 from selenium.webdriver.common.by import By
 from selenium.webdriver.support.ui import Select
 from selenium.webdriver.chrome.options import Options
 
 
 #   #   #   #                LOGS                #   #   #   #
@@ -401,25 +401,28 @@
 
 def vrr_summary(cf):
     """
     Summarize voting rights status from pairs using configuration object `cf`.
     """
     start = time.time()
     print("Creating voting rights summary...", cf=cf)
-    vr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"])
-    if not cf["NO_WRITE"]:
-        print("Writing to output path...", cf=cf)
-        write(
-            vr, sheet_names=["VRR"], path=cf["OUTPUT_PATH"], overwrite=cf["OVERWRITE"]
-        )
+    if not cf["NO_WRITE"] and cf["OUTPUT_PATH"] != None:
+        if os.path.splitext(cf["OUTPUT_PATH"])[1] in (".xls",".xlsx",".json",".parquet",".csv"):
+            if os.path.isfile(cf["OUTPUT_PATH"]) and not cf["OVERWRITE"]:
+                error("File already exists! Repeat in overwrite mode.")
+            vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"], cf["OUTPUT_PATH"])
+        else:
+            error("File extension not supported!")
+    if cf["NO_WRITE"] or cf["OUTPUT_PATH"] == None:
+        vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"])
     elapsed = math.floor(time.time() - start)
     print(f"Completed in {elapsed} seconds.", cf=cf)
     if cf["WINDOW"]:
         cf["WINDOW"].write_event_value("VRR-COMPLETE", True)
-    return vr
+    return vrr
 
 
 #   #   #   #         CONFIGURATION & I/O        #   #   #   #
 
 
 def set(
     inputs,
@@ -626,14 +629,15 @@
             cf={"WINDOW": window, "FORCE": force},
         )
 
     if (  # raise no table selection
         support_multitable == False
         and archive == False
         and fetch == False
+        and vrr_summary == False
         and table
         not in (
             "cases",
             "charges",
             "fees",
             "financial-history",
             "history",
@@ -1234,115 +1238,142 @@
             ]
         )
     )
     names = names.sort("Name")
     return names
 
 
-def _vrr_summary_from_pairs(src, pairs, debug=False):
+def _vrr_summary_from_pairs(src, pairs, dest=None, debug=False):
     if isinstance(src, str):
         cases = cf(src, table="cases", now=True)
         charges = cf(src, table="charges", now=True)
     if isinstance(pairs, str):
         pairs = read(pairs)
     cases = cases.select("CaseNumber", "Name", "DOB", "Race", "Sex")
     cases = cases.with_columns(
         [
             pl.col("Race").cast(pl.Utf8, strict=False),
             pl.col("Sex").cast(pl.Utf8, strict=False),
         ]
     )
-
-    fch = charges.filter(pl.col("Filing")).groupby("CaseNumber").all()
-
+    fch = charges.filter(pl.col("Filing"))
+    fch = fch.join(pairs, on="Name", how="outer")
+    fch = fch.groupby("AIS / Unique ID").all()
     fch = fch.select(
         [
-            pl.col("CaseNumber"),
+            pl.col("AIS / Unique ID"),
             pl.col("CERVDisqCharge").arr.count_match(True).alias("CERVChargesCount"),
             pl.col("PardonDisqCharge")
             .arr.count_match(True)
             .alias("PardonToVoteChargesCount"),
             pl.col("PermanentDisqCharge")
             .arr.count_match(True)
             .alias("PermanentDisqChargesCount"),
-        ]
-    )
+            pl.col("ChargesSummary").arr.join(", ")
+            .str.replace_all(r"null,?", "")
+            .str.strip()
+            .str.replace(r",$", "")
+            .str.replace_all(r"\s+", " ")
+            .alias("FilingCharges"),
 
-    dch = (
-        charges.filter(pl.col("Disposition") & pl.col("Conviction"))
-        .groupby("CaseNumber")
-        .all()
+        ]
     )
-
-    dch = dch.select(
+    conv = charges.filter(pl.col("Disposition") & pl.col("Conviction"))
+    conv = conv.join(pairs, on="Name", how="outer")
+    conv = conv.groupby("AIS / Unique ID").all()
+    conv = conv.select(
         [
-            pl.col("CaseNumber"),
-            pl.col("Conviction").arr.count_match(True).alias("ConvictionCount"),
+            pl.col("AIS / Unique ID"),
+            pl.col("Conviction")
+            .arr.count_match(True)
+            .alias("ConvictionCount"),
             pl.col("CERVDisqConviction")
             .arr.count_match(True)
             .alias("CERVConvictionCount"),
             pl.col("PardonDisqConviction")
             .arr.count_match(True)
             .alias("PardonToVoteConvictionCount"),
             pl.col("PermanentDisqConviction")
             .arr.count_match(True)
             .alias("PermanentDisqConvictionCount"),
             pl.col("PaymentToRestore").arr.mean(),
+            pl.col("ChargesSummary").arr.join(", ")
+            .str.replace_all(r"null,?", "")
+            .str.strip()
+            .str.replace(r",$", "")
+            .str.replace_all(r"\s+", " ")
+            .alias("Convictions"),
         ]
     )
-
-    vrr = (
-        charges.filter(
-            pl.col("CERVDisqConviction")
-            | pl.col("PardonDisqConviction")
-            | pl.col("PermanentDisqConviction")
-        )
-        .groupby("CaseNumber")
-        .all()
+    vrr = charges.filter(
+        pl.col("CERVDisqConviction")
+        | pl.col("PardonDisqConviction")
+        | pl.col("PermanentDisqConviction")
     )
-
+    vrr = vrr.join(pairs, on="Name", how="outer")
+    vrr = vrr.groupby("AIS / Unique ID").all()
     vrr = vrr.select(
         [
-            pl.col("CaseNumber"),
-            pl.col("ChargesSummary").arr.join(", ").alias("DisqualifyingConvictions"),
+            pl.col("AIS / Unique ID"),
+            pl.col("ChargesSummary").arr.join(", ")
+            .str.replace_all(r"null,?", "")
+            .str.strip()
+            .str.replace(r",$", "")
+            .str.replace_all(r"\s+", " ")
+            .alias("DisqualifyingConvictions")
         ]
     )
-
-    cases = cases.join(fch, on="CaseNumber", how="outer")
-    cases = cases.join(dch, on="CaseNumber", how="outer")
-    cases = cases.join(vrr, on="CaseNumber", how="outer")
     cases = cases.join(pairs, on="Name", how="outer")
-
     cases = cases.groupby("AIS / Unique ID").all()
-
-    summary = cases.select(
+    cases = cases.join(vrr, on="AIS / Unique ID", how="outer")
+    cases = cases.join(conv, on="AIS / Unique ID", how="outer")
+    cases = cases.join(fch, on="AIS / Unique ID", how="outer")
+    cases = cases.select(
         [
             pl.col("AIS / Unique ID"),
-            pl.col("Name").arr.get(0),
-            pl.col("DOB").arr.get(0),
-            pl.col("Race").arr.get(0),
-            pl.col("Sex").arr.get(0),
-            pl.col("PaymentToRestore").arr.sum(),
-            pl.col("ConvictionCount").arr.sum(),
-            pl.col("CERVChargesCount").arr.sum(),
-            pl.col("PardonToVoteChargesCount").arr.sum(),
-            pl.col("PermanentDisqChargesCount").arr.sum(),
-            pl.col("CERVConvictionCount").arr.sum(),
-            pl.col("PardonToVoteConvictionCount").arr.sum(),
-            pl.col("PermanentDisqConvictionCount").arr.sum(),
-            pl.col("DisqualifyingConvictions")
-            .arr.join(", ")
+            pl.col("Name").arr.first(),
+            pl.col("DOB").arr.first(),
+            pl.col("Race").arr.first(),
+            pl.col("Sex").arr.first(),
+            pl.col("PaymentToRestore"),
+            pl.col("ConvictionCount"),
+            pl.col("CERVChargesCount"),
+            pl.col("CERVConvictionCount"),
+            pl.col("PardonToVoteChargesCount"),
+            pl.col("PardonToVoteConvictionCount"),
+            pl.col("PermanentDisqChargesCount"),
+            pl.col("PermanentDisqConvictionCount"),
+            pl.col("DisqualifyingConvictions"),
+            pl.col("Convictions"),
+            pl.col("FilingCharges"),
+            pl.col("CaseNumber").arr.join(", ")            
             .str.replace_all(r"null,?", "")
             .str.strip()
             .str.replace(r",$", "")
-            .str.replace_all(r"\s+", " "),
+            .str.replace_all(r"\s+", " ")
+            .alias("Cases")
         ]
     )
-    summary = summary.sort("Name")
-    return summary
+    cases = cases.sort("Name")
+    if dest == None:
+        pass
+    elif os.path.splitext(dest)[1] == '.csv':
+        cases.write_csv(dest)
+    elif os.path.splitext(dest)[1] in ('.xls','.xlsx'):
+        cases = cases.with_columns(
+            [
+                pl.col("DOB").cast(pl.Utf8, strict=False)
+            ]
+        )
+        cases.to_pandas().to_excel(dest)
+    elif os.path.splitext(dest)[1] == '.parquet':
+        cases.write_parquet(dest)
+    elif os.path.splitext(dest)[1] == '.json':
+        cases.write_json(dest)
+    return cases
 
 
 def _explode_charges(df, debug=False):
     all_charges = df.with_columns(
         [
             pl.concat_str(
                 [
```

### Comparing `alacorder-80.4.4/src/alacorder/alac.py` & `alacorder-80.4.5/src/alacorder/alac.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,24 +10,24 @@
     polars ^0.17.6, PyMuPDF ^1.21.1, 
     PySimpleGUI ^4.60.4, selenium ^4.8.3, 
     tqdm ^4.65.0, xlsx2csv ^0.8.1, XlsxWriter ^3.0.9
 """
 
 name = "ALACORDER"
 long_version = "snowpalace"
-version = "80.4.4"
+version = "80.4.5"
 
 _autoload_graphical_user_interface = False
 
 import polars as pl
 import os, sys, time, glob, re, math
 import click, fitz, selenium, xlsxwriter
 from tqdm.auto import tqdm
-from datetime import datetime
 from random import sample
+from datetime import datetime
 from selenium import webdriver
 from selenium.webdriver.common.by import By
 from selenium.webdriver.support.ui import Select
 from selenium.webdriver.chrome.options import Options
 
 
 #   #   #   #                LOGS                #   #   #   #
@@ -401,25 +401,28 @@
 
 def vrr_summary(cf):
     """
     Summarize voting rights status from pairs using configuration object `cf`.
     """
     start = time.time()
     print("Creating voting rights summary...", cf=cf)
-    vr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"])
-    if not cf["NO_WRITE"]:
-        print("Writing to output path...", cf=cf)
-        write(
-            vr, sheet_names=["VRR"], path=cf["OUTPUT_PATH"], overwrite=cf["OVERWRITE"]
-        )
+    if not cf["NO_WRITE"] and cf["OUTPUT_PATH"] != None:
+        if os.path.splitext(cf["OUTPUT_PATH"])[1] in (".xls",".xlsx",".json",".parquet",".csv"):
+            if os.path.isfile(cf["OUTPUT_PATH"]) and not cf["OVERWRITE"]:
+                error("File already exists! Repeat in overwrite mode.")
+            vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"], cf["OUTPUT_PATH"])
+        else:
+            error("File extension not supported!")
+    if cf["NO_WRITE"] or cf["OUTPUT_PATH"] == None:
+        vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"])
     elapsed = math.floor(time.time() - start)
     print(f"Completed in {elapsed} seconds.", cf=cf)
     if cf["WINDOW"]:
         cf["WINDOW"].write_event_value("VRR-COMPLETE", True)
-    return vr
+    return vrr
 
 
 #   #   #   #         CONFIGURATION & I/O        #   #   #   #
 
 
 def set(
     inputs,
@@ -626,14 +629,15 @@
             cf={"WINDOW": window, "FORCE": force},
         )
 
     if (  # raise no table selection
         support_multitable == False
         and archive == False
         and fetch == False
+        and vrr_summary == False
         and table
         not in (
             "cases",
             "charges",
             "fees",
             "financial-history",
             "history",
@@ -1234,115 +1238,142 @@
             ]
         )
     )
     names = names.sort("Name")
     return names
 
 
-def _vrr_summary_from_pairs(src, pairs, debug=False):
+def _vrr_summary_from_pairs(src, pairs, dest=None, debug=False):
     if isinstance(src, str):
         cases = cf(src, table="cases", now=True)
         charges = cf(src, table="charges", now=True)
     if isinstance(pairs, str):
         pairs = read(pairs)
     cases = cases.select("CaseNumber", "Name", "DOB", "Race", "Sex")
     cases = cases.with_columns(
         [
             pl.col("Race").cast(pl.Utf8, strict=False),
             pl.col("Sex").cast(pl.Utf8, strict=False),
         ]
     )
-
-    fch = charges.filter(pl.col("Filing")).groupby("CaseNumber").all()
-
+    fch = charges.filter(pl.col("Filing"))
+    fch = fch.join(pairs, on="Name", how="outer")
+    fch = fch.groupby("AIS / Unique ID").all()
     fch = fch.select(
         [
-            pl.col("CaseNumber"),
+            pl.col("AIS / Unique ID"),
             pl.col("CERVDisqCharge").arr.count_match(True).alias("CERVChargesCount"),
             pl.col("PardonDisqCharge")
             .arr.count_match(True)
             .alias("PardonToVoteChargesCount"),
             pl.col("PermanentDisqCharge")
             .arr.count_match(True)
             .alias("PermanentDisqChargesCount"),
-        ]
-    )
+            pl.col("ChargesSummary").arr.join(", ")
+            .str.replace_all(r"null,?", "")
+            .str.strip()
+            .str.replace(r",$", "")
+            .str.replace_all(r"\s+", " ")
+            .alias("FilingCharges"),
 
-    dch = (
-        charges.filter(pl.col("Disposition") & pl.col("Conviction"))
-        .groupby("CaseNumber")
-        .all()
+        ]
     )
-
-    dch = dch.select(
+    conv = charges.filter(pl.col("Disposition") & pl.col("Conviction"))
+    conv = conv.join(pairs, on="Name", how="outer")
+    conv = conv.groupby("AIS / Unique ID").all()
+    conv = conv.select(
         [
-            pl.col("CaseNumber"),
-            pl.col("Conviction").arr.count_match(True).alias("ConvictionCount"),
+            pl.col("AIS / Unique ID"),
+            pl.col("Conviction")
+            .arr.count_match(True)
+            .alias("ConvictionCount"),
             pl.col("CERVDisqConviction")
             .arr.count_match(True)
             .alias("CERVConvictionCount"),
             pl.col("PardonDisqConviction")
             .arr.count_match(True)
             .alias("PardonToVoteConvictionCount"),
             pl.col("PermanentDisqConviction")
             .arr.count_match(True)
             .alias("PermanentDisqConvictionCount"),
             pl.col("PaymentToRestore").arr.mean(),
+            pl.col("ChargesSummary").arr.join(", ")
+            .str.replace_all(r"null,?", "")
+            .str.strip()
+            .str.replace(r",$", "")
+            .str.replace_all(r"\s+", " ")
+            .alias("Convictions"),
         ]
     )
-
-    vrr = (
-        charges.filter(
-            pl.col("CERVDisqConviction")
-            | pl.col("PardonDisqConviction")
-            | pl.col("PermanentDisqConviction")
-        )
-        .groupby("CaseNumber")
-        .all()
+    vrr = charges.filter(
+        pl.col("CERVDisqConviction")
+        | pl.col("PardonDisqConviction")
+        | pl.col("PermanentDisqConviction")
     )
-
+    vrr = vrr.join(pairs, on="Name", how="outer")
+    vrr = vrr.groupby("AIS / Unique ID").all()
     vrr = vrr.select(
         [
-            pl.col("CaseNumber"),
-            pl.col("ChargesSummary").arr.join(", ").alias("DisqualifyingConvictions"),
+            pl.col("AIS / Unique ID"),
+            pl.col("ChargesSummary").arr.join(", ")
+            .str.replace_all(r"null,?", "")
+            .str.strip()
+            .str.replace(r",$", "")
+            .str.replace_all(r"\s+", " ")
+            .alias("DisqualifyingConvictions")
         ]
     )
-
-    cases = cases.join(fch, on="CaseNumber", how="outer")
-    cases = cases.join(dch, on="CaseNumber", how="outer")
-    cases = cases.join(vrr, on="CaseNumber", how="outer")
     cases = cases.join(pairs, on="Name", how="outer")
-
     cases = cases.groupby("AIS / Unique ID").all()
-
-    summary = cases.select(
+    cases = cases.join(vrr, on="AIS / Unique ID", how="outer")
+    cases = cases.join(conv, on="AIS / Unique ID", how="outer")
+    cases = cases.join(fch, on="AIS / Unique ID", how="outer")
+    cases = cases.select(
         [
             pl.col("AIS / Unique ID"),
-            pl.col("Name").arr.get(0),
-            pl.col("DOB").arr.get(0),
-            pl.col("Race").arr.get(0),
-            pl.col("Sex").arr.get(0),
-            pl.col("PaymentToRestore").arr.sum(),
-            pl.col("ConvictionCount").arr.sum(),
-            pl.col("CERVChargesCount").arr.sum(),
-            pl.col("PardonToVoteChargesCount").arr.sum(),
-            pl.col("PermanentDisqChargesCount").arr.sum(),
-            pl.col("CERVConvictionCount").arr.sum(),
-            pl.col("PardonToVoteConvictionCount").arr.sum(),
-            pl.col("PermanentDisqConvictionCount").arr.sum(),
-            pl.col("DisqualifyingConvictions")
-            .arr.join(", ")
+            pl.col("Name").arr.first(),
+            pl.col("DOB").arr.first(),
+            pl.col("Race").arr.first(),
+            pl.col("Sex").arr.first(),
+            pl.col("PaymentToRestore"),
+            pl.col("ConvictionCount"),
+            pl.col("CERVChargesCount"),
+            pl.col("CERVConvictionCount"),
+            pl.col("PardonToVoteChargesCount"),
+            pl.col("PardonToVoteConvictionCount"),
+            pl.col("PermanentDisqChargesCount"),
+            pl.col("PermanentDisqConvictionCount"),
+            pl.col("DisqualifyingConvictions"),
+            pl.col("Convictions"),
+            pl.col("FilingCharges"),
+            pl.col("CaseNumber").arr.join(", ")            
             .str.replace_all(r"null,?", "")
             .str.strip()
             .str.replace(r",$", "")
-            .str.replace_all(r"\s+", " "),
+            .str.replace_all(r"\s+", " ")
+            .alias("Cases")
         ]
     )
-    summary = summary.sort("Name")
-    return summary
+    cases = cases.sort("Name")
+    if dest == None:
+        pass
+    elif os.path.splitext(dest)[1] == '.csv':
+        cases.write_csv(dest)
+    elif os.path.splitext(dest)[1] in ('.xls','.xlsx'):
+        cases = cases.with_columns(
+            [
+                pl.col("DOB").cast(pl.Utf8, strict=False)
+            ]
+        )
+        cases.to_pandas().to_excel(dest)
+    elif os.path.splitext(dest)[1] == '.parquet':
+        cases.write_parquet(dest)
+    elif os.path.splitext(dest)[1] == '.json':
+        cases.write_json(dest)
+    return cases
 
 
 def _explode_charges(df, debug=False):
     all_charges = df.with_columns(
         [
             pl.concat_str(
                 [
```

### Comparing `alacorder-80.4.4/PKG-INFO` & `alacorder-80.4.5/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: alacorder
-Version: 80.4.4
+Version: 80.4.5
 Summary: Alacorder collects and processes Alacourt case detail PDFs into data tables suitable for research purposes.
 License: MIT
 Author: Sam Robson
 Author-email: sbrobson@crimson.ua.edu
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

