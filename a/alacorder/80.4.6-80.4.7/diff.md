# Comparing `tmp/alacorder-80.4.6.tar.gz` & `tmp/alacorder-80.4.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "alacorder-80.4.6.tar", max compression
+gzip compressed data, was "alacorder-80.4.7.tar", max compression
```

## Comparing `alacorder-80.4.6.tar` & `alacorder-80.4.7.tar`

### file list

```diff
@@ -1,7 +1,8 @@
--rw-r--r--   0        0        0     1066 2023-02-07 05:47:31.000000 alacorder-80.4.6/LICENSE
--rw-r--r--   0        0        0     6592 2023-05-11 17:12:36.043202 alacorder-80.4.6/README.md
--rw-r--r--   0        0        0      717 2023-05-13 01:10:57.891333 alacorder-80.4.6/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-02 17:21:37.916960 alacorder-80.4.6/src/alacorder/__init__.py
--rw-r--r--   0        0        0   216652 2023-05-13 01:12:46.616860 alacorder-80.4.6/src/alacorder/__main__.py
--rw-r--r--   0        0        0   216652 2023-05-13 01:12:39.854200 alacorder-80.4.6/src/alacorder/alac.py
--rw-r--r--   0        0        0     7563 1970-01-01 00:00:00.000000 alacorder-80.4.6/PKG-INFO
+-rw-r--r--   0        0        0     1066 2023-02-07 05:47:31.000000 alacorder-80.4.7/LICENSE
+-rw-r--r--   0        0        0     6592 2023-05-11 17:12:36.043202 alacorder-80.4.7/README.md
+-rw-r--r--   0        0        0      697 2023-05-13 16:09:39.732708 alacorder-80.4.7/pyproject.toml
+-rw-r--r--   0        0        0     6148 2023-05-13 16:09:36.590299 alacorder-80.4.7/src/alacorder/.DS_Store
+-rw-r--r--   0        0        0        0 2023-05-02 17:21:37.916960 alacorder-80.4.7/src/alacorder/__init__.py
+-rw-r--r--   0        0        0   216874 2023-05-13 15:55:42.639654 alacorder-80.4.7/src/alacorder/__main__.py
+-rw-r--r--   0        0        0   216874 2023-05-13 15:55:48.258391 alacorder-80.4.7/src/alacorder/alac.py
+-rw-r--r--   0        0        0     7521 1970-01-01 00:00:00.000000 alacorder-80.4.7/PKG-INFO
```

### Comparing `alacorder-80.4.6/LICENSE` & `alacorder-80.4.7/LICENSE`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.6/README.md` & `alacorder-80.4.7/README.md`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.6/src/alacorder/__main__.py` & `alacorder-80.4.7/src/alacorder/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,24 +3,24 @@
 ╔═╗╔╗╔╔═╗╦ ╦╔═╗╔═╗╦  ╔═╗╔═╗╔═╗
 ╚═╗║║║║ ║║║║╠═╝╠═╣║  ╠═╣║  ║╣ 
 ╚═╝╝╚╝╚═╝╚╩╝╩  ╩ ╩╩═╝╩ ╩╚═╝╚═╝
 (c) 2023 Sam Robson ----------
 
 Dependencies: 
     python 3.9+, brotli ^1.0.9, click ^8.1.3,
-    polars ^0.17.6, PyMuPDF ^1.21.1, pyarrow ^12.0.0
+    polars ^0.17.6, PyMuPDF ^1.21.1,
     PySimpleGUI ^4.60.4, selenium ^4.8.3, 
     tqdm ^4.65.0, xlsx2csv ^0.8.1, XlsxWriter ^3.0.9
 """
 
 name = "ALACORDER"
 long_version = "snowpalace"
-version = "80.4.6"
+version = "80.4.7"
 
-_autoload_graphical_user_interface = False
+_autoload_graphical_user_interface = True
 
 import polars as pl
 import os, sys, time, glob, re, math
 import click, fitz, selenium, xlsxwriter
 from tqdm.auto import tqdm
 from random import sample
 from datetime import datetime
@@ -114,19 +114,21 @@
 
 
 def popup(*msg, cf=None):
     message = ""
     for m in msg:
         message += f"{m} "
     message = message.strip()
-    if cf:
+    if isinstance(cf, dict):
         if cf["WINDOW"]:
             cf["WINDOW"].write_event_value("POPUP", message)
         else:
             print(message)
+    elif cf != None: # if Window
+        cf.write_event_value("POPUP", message)
     else:
         print(message)
 
 
 #   #   #   #            TABLE PARSERS           #   #   #   #
 
 
@@ -405,19 +407,19 @@
     """
     start = time.time()
     print("Creating voting rights summary...", cf=cf)
     if not cf["NO_WRITE"] and cf["OUTPUT_PATH"] != None:
         if os.path.splitext(cf["OUTPUT_PATH"])[1] in (".xls",".xlsx",".json",".parquet",".csv"):
             if os.path.isfile(cf["OUTPUT_PATH"]) and not cf["OVERWRITE"]:
                 error("File already exists! Repeat in overwrite mode.")
-            vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"], cf["OUTPUT_PATH"])
+            vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"], cf["OUTPUT_PATH"], cf["WINDOW"])
         else:
             error("File extension not supported!")
     if cf["NO_WRITE"] or cf["OUTPUT_PATH"] == None:
-        vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"])
+        vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"], None, cf['WINDOW'])
     elapsed = math.floor(time.time() - start)
     print(f"Completed in {elapsed} seconds.", cf=cf)
     if cf["WINDOW"]:
         cf["WINDOW"].write_event_value("VRR-COMPLETE", True)
     return vrr
 
 
@@ -1238,15 +1240,15 @@
             ]
         )
     )
     names = names.sort("Name")
     return names
 
 
-def _vrr_summary_from_pairs(src, pairs, dest=None, debug=False):
+def _vrr_summary_from_pairs(src, pairs, dest=None, window=None, debug=False):
     if isinstance(src, str):
         cases = cf(src, table="cases", now=True)
         charges = cf(src, table="charges", now=True)
     if isinstance(pairs, str):
         pairs = read(pairs)
     cases = cases.select("CaseNumber", "Name", "DOB", "Race", "Sex")
     cases = cases.with_columns(
@@ -1363,15 +1365,16 @@
             cases = cases.with_columns(
                 [
                     pl.col("DOB").cast(pl.Utf8, strict=False)
                 ]
             )
             cases.to_pandas().to_excel(dest)
         except:
-            cases.write_excel(dest)
+            popup("Warning: failsafe exported to .csv.", cf=window)
+            cases.write_csv(os.path.splitext(dest)[0]+".csv")
     elif os.path.splitext(dest)[1] == '.parquet':
         cases.write_parquet(dest)
     elif os.path.splitext(dest)[1] == '.json':
         cases.write_json(dest)
     return cases
```

### Comparing `alacorder-80.4.6/src/alacorder/alac.py` & `alacorder-80.4.7/src/alacorder/alac.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,24 +3,24 @@
 ╔═╗╔╗╔╔═╗╦ ╦╔═╗╔═╗╦  ╔═╗╔═╗╔═╗
 ╚═╗║║║║ ║║║║╠═╝╠═╣║  ╠═╣║  ║╣ 
 ╚═╝╝╚╝╚═╝╚╩╝╩  ╩ ╩╩═╝╩ ╩╚═╝╚═╝
 (c) 2023 Sam Robson ----------
 
 Dependencies: 
     python 3.9+, brotli ^1.0.9, click ^8.1.3,
-    polars ^0.17.6, PyMuPDF ^1.21.1, pyarrow ^12.0.0
+    polars ^0.17.6, PyMuPDF ^1.21.1,
     PySimpleGUI ^4.60.4, selenium ^4.8.3, 
     tqdm ^4.65.0, xlsx2csv ^0.8.1, XlsxWriter ^3.0.9
 """
 
 name = "ALACORDER"
 long_version = "snowpalace"
-version = "80.4.6"
+version = "80.4.7"
 
-_autoload_graphical_user_interface = False
+_autoload_graphical_user_interface = True
 
 import polars as pl
 import os, sys, time, glob, re, math
 import click, fitz, selenium, xlsxwriter
 from tqdm.auto import tqdm
 from random import sample
 from datetime import datetime
@@ -114,19 +114,21 @@
 
 
 def popup(*msg, cf=None):
     message = ""
     for m in msg:
         message += f"{m} "
     message = message.strip()
-    if cf:
+    if isinstance(cf, dict):
         if cf["WINDOW"]:
             cf["WINDOW"].write_event_value("POPUP", message)
         else:
             print(message)
+    elif cf != None: # if Window
+        cf.write_event_value("POPUP", message)
     else:
         print(message)
 
 
 #   #   #   #            TABLE PARSERS           #   #   #   #
 
 
@@ -405,19 +407,19 @@
     """
     start = time.time()
     print("Creating voting rights summary...", cf=cf)
     if not cf["NO_WRITE"] and cf["OUTPUT_PATH"] != None:
         if os.path.splitext(cf["OUTPUT_PATH"])[1] in (".xls",".xlsx",".json",".parquet",".csv"):
             if os.path.isfile(cf["OUTPUT_PATH"]) and not cf["OVERWRITE"]:
                 error("File already exists! Repeat in overwrite mode.")
-            vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"], cf["OUTPUT_PATH"])
+            vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"], cf["OUTPUT_PATH"], cf["WINDOW"])
         else:
             error("File extension not supported!")
     if cf["NO_WRITE"] or cf["OUTPUT_PATH"] == None:
-        vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"])
+        vrr = _vrr_summary_from_pairs(cf["INPUTS"], cf["PAIRS"], None, cf['WINDOW'])
     elapsed = math.floor(time.time() - start)
     print(f"Completed in {elapsed} seconds.", cf=cf)
     if cf["WINDOW"]:
         cf["WINDOW"].write_event_value("VRR-COMPLETE", True)
     return vrr
 
 
@@ -1238,15 +1240,15 @@
             ]
         )
     )
     names = names.sort("Name")
     return names
 
 
-def _vrr_summary_from_pairs(src, pairs, dest=None, debug=False):
+def _vrr_summary_from_pairs(src, pairs, dest=None, window=None, debug=False):
     if isinstance(src, str):
         cases = cf(src, table="cases", now=True)
         charges = cf(src, table="charges", now=True)
     if isinstance(pairs, str):
         pairs = read(pairs)
     cases = cases.select("CaseNumber", "Name", "DOB", "Race", "Sex")
     cases = cases.with_columns(
@@ -1363,15 +1365,16 @@
             cases = cases.with_columns(
                 [
                     pl.col("DOB").cast(pl.Utf8, strict=False)
                 ]
             )
             cases.to_pandas().to_excel(dest)
         except:
-            cases.write_excel(dest)
+            popup("Warning: failsafe exported to .csv.", cf=window)
+            cases.write_csv(os.path.splitext(dest)[0]+".csv")
     elif os.path.splitext(dest)[1] == '.parquet':
         cases.write_parquet(dest)
     elif os.path.splitext(dest)[1] == '.json':
         cases.write_json(dest)
     return cases
```

### Comparing `alacorder-80.4.6/PKG-INFO` & `alacorder-80.4.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: alacorder
-Version: 80.4.6
+Version: 80.4.7
 Summary: Alacorder collects and processes Alacourt case detail PDFs into data tables suitable for research purposes.
 License: MIT
 Author: Sam Robson
 Author-email: sbrobson@crimson.ua.edu
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -13,15 +13,14 @@
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: PyMuPDF (>=1.21.1,<2.0.0)
 Requires-Dist: PySimpleGUI (>=4.60.4,<5.0.0)
 Requires-Dist: XlsxWriter (>=3.0.9,<4.0.0)
 Requires-Dist: brotli (>=1.0.9,<2.0.0)
 Requires-Dist: click (>=8.1.3,<9.0.0)
 Requires-Dist: polars (>=0.17.6,<0.18.0)
-Requires-Dist: pyarrow (>=12.0.0,<13.0.0)
 Requires-Dist: selenium (>=4.8.3,<5.0.0)
 Requires-Dist: tqdm (>=4.65.0,<5.0.0)
 Requires-Dist: xlsx2csv (>=0.8.1,<0.9.0)
 Description-Content-Type: text/markdown
 
 ```
     ___    __                          __
```

