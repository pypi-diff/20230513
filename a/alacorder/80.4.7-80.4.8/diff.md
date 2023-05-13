# Comparing `tmp/alacorder-80.4.7.tar.gz` & `tmp/alacorder-80.4.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "alacorder-80.4.7.tar", max compression
+gzip compressed data, was "alacorder-80.4.8.tar", max compression
```

## Comparing `alacorder-80.4.7.tar` & `alacorder-80.4.8.tar`

### file list

```diff
@@ -1,8 +1,5 @@
--rw-r--r--   0        0        0     1066 2023-02-07 05:47:31.000000 alacorder-80.4.7/LICENSE
--rw-r--r--   0        0        0     6592 2023-05-11 17:12:36.043202 alacorder-80.4.7/README.md
--rw-r--r--   0        0        0      697 2023-05-13 16:09:39.732708 alacorder-80.4.7/pyproject.toml
--rw-r--r--   0        0        0     6148 2023-05-13 16:09:36.590299 alacorder-80.4.7/src/alacorder/.DS_Store
--rw-r--r--   0        0        0        0 2023-05-02 17:21:37.916960 alacorder-80.4.7/src/alacorder/__init__.py
--rw-r--r--   0        0        0   216874 2023-05-13 15:55:42.639654 alacorder-80.4.7/src/alacorder/__main__.py
--rw-r--r--   0        0        0   216874 2023-05-13 15:55:48.258391 alacorder-80.4.7/src/alacorder/alac.py
--rw-r--r--   0        0        0     7521 1970-01-01 00:00:00.000000 alacorder-80.4.7/PKG-INFO
+-rw-r--r--   0        0        0     1066 2023-02-07 05:47:31.000000 alacorder-80.4.8/LICENSE
+-rw-r--r--   0        0        0     6592 2023-05-11 17:12:36.043202 alacorder-80.4.8/README.md
+-rw-r--r--   0        0        0   218036 2023-05-13 17:06:43.893212 alacorder-80.4.8/alacorder.py
+-rw-r--r--   0        0        0      746 2023-05-13 16:39:59.220362 alacorder-80.4.8/pyproject.toml
+-rw-r--r--   0        0        0     7563 1970-01-01 00:00:00.000000 alacorder-80.4.8/PKG-INFO
```

### Comparing `alacorder-80.4.7/LICENSE` & `alacorder-80.4.8/LICENSE`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.7/README.md` & `alacorder-80.4.8/README.md`

 * *Files identical despite different names*

### Comparing `alacorder-80.4.7/src/alacorder/__main__.py` & `alacorder-80.4.8/alacorder.py`

 * *Files 1% similar despite different names*

```diff
@@ -6,19 +6,22 @@
 (c) 2023 Sam Robson ----------
 
 Dependencies: 
     python 3.9+, brotli ^1.0.9, click ^8.1.3,
     polars ^0.17.6, PyMuPDF ^1.21.1,
     PySimpleGUI ^4.60.4, selenium ^4.8.3, 
     tqdm ^4.65.0, xlsx2csv ^0.8.1, XlsxWriter ^3.0.9
+Optional dependencies:
+    pyarrow required to export summary to .xls, .xlsx,
+    Google Chrome required to fetch cases from Alacourt
 """
 
 name = "ALACORDER"
 long_version = "snowpalace"
-version = "80.4.7"
+version = "80.4.8"
 
 _autoload_graphical_user_interface = True
 
 import polars as pl
 import os, sys, time, glob, re, math
 import click, fitz, selenium, xlsxwriter
 from tqdm.auto import tqdm
@@ -3260,15 +3263,15 @@
     login(driver, cID=cID, uID=uID, pwd=pwd, window=window)
 
     for i, r in enumerate(query.rows(named=True)):
         if query[i, "QUERY_COMPLETE"] == "Y":
             continue
         if driver.current_url == "https://v2.alacourt.com/frmlogin.aspx":
             login(driver, cID, uID, pwd, window=window)
-        driver.implicitly_wait(1)
+        # driver.implicitly_wait(1)
         results = party_search(
             driver,
             name=r["TEMP_NAME"],
             party_type=r["TEMP_PARTY_TYPE"],
             ssn=r["TEMP_SSN"],
             dob=r["TEMP_DOB"],
             county=r["TEMP_COUNTY"],
@@ -3391,15 +3394,14 @@
     Returns:
         List[str] of URLs to PDF
     """
 
     if "frmIndexSearchForm" not in driver.current_url:
         driver.get("https://v2.alacourt.com/frmIndexSearchForm.aspx")
 
-    driver.implicitly_wait(2)
     has_window = False if window == "None" else True
 
     # connection error
     try:
         party_name_box = driver.find_element(
             by=By.NAME, value="ctl00$ContentPlaceHolder1$txtName"
         )
@@ -3480,29 +3482,24 @@
         filed_before_box.send_keys(filed_before)
     if filed_after != "":
         filed_after_box = driver.find_element(
             by=By.NAME, value="ctl00$ContentPlaceHolder1$txtTo"
         )
         filed_after_box.send_keys(filed_after)
 
-    driver.implicitly_wait(1)
     # submit search
     search_button = driver.find_element(by=By.ID, value="searchButton")
 
-    driver.implicitly_wait(1)
     try:
         search_button.click()
     except:
-        driver.implicitly_wait(5)
-        time.sleep(5)
+        driver.implicitly_wait(2)
+        time.sleep(2)
 
-    if debug:
-        print("Submitted party search form...")
-
-    driver.implicitly_wait(1)
+    dlog("Submitted party search form...", cf=debug)
 
     # count pages
     try:
         page_counter = driver.find_element(
             by=By.ID, value="ContentPlaceHolder1_dg_tcPageXofY"
         ).text
         pages = int(page_counter.strip()[-1])
@@ -3516,46 +3513,40 @@
             by=By.ID, value="ContentPlaceHolder1_lblResultCount"
         )
         results_count = int(
             results_indicator.text.replace("Search Results: ", "")
             .replace(" records returned.", "")
             .strip()
         )
+        dlog(f"Found {results_count} results, fetching URLs and downloading PDFs...", cf=debug)
     except:
-        pass
+        results_count = 0
 
-    if debug:
-        print(f"Found {results_count} results, fetching URLs and downloading PDFs...")
 
     # get PDF links from each page
     pdflinks = []
     i = 0
     for i in range(0, pages):
-        driver.implicitly_wait(0.5)
         hovers = driver.find_elements(By.CLASS_NAME, "menuHover")
         for x in hovers:
             try:
                 a = x.get_attribute("href")
                 if "PDF" in a:
                     pdflinks.append(a)
             except:
                 pass
-        driver.implicitly_wait(0.5)
         try:
             pager_select = Select(
                 driver.find_element(
                     by=By.NAME, value="ctl00$ContentPlaceHolder1$dg$ctl18$ddlPages"
                 )
             )
             next_pg = int(pager_select.text) + 1
-            driver.implicitly_wait(0.5)
         except:
             try:
-                driver.implicitly_wait(0.5)
-                time.sleep(0.5)
                 next_button = driver.find_element(
                     by=By.ID, value="ContentPlaceHolder1_dg_ibtnNext"
                 )
                 next_button.click()
             except:
                 continue
     return pdflinks
@@ -3577,15 +3568,14 @@
         driver.current_url == "https://v2.alacourt.com/frmlogin.aspx"
         and cID != ""
         and uID != ""
         and pwd != ""
     ):
         login(driver, cID=cID, uID=uID, pwd=pwd, window=window)
     a = driver.get(url)
-    driver.implicitly_wait(0.5)
 
 
 def login(driver, cID, uID="", pwd="", path="", window=None):
     """Login to Alacourt.com using (driver) and auth (cID, username, pwd) for browser download to directory at (path)
 
     Args:
         driver (WebDriver): Google Chrome selenium.WebDriver() object
@@ -3612,49 +3602,41 @@
 
     print("Connecting to Alacourt...")
 
     login_screen = driver.get("https://v2.alacourt.com/frmlogin.aspx")
 
     print("Logging in...")
 
-    driver.implicitly_wait(1)
-
     cID_box = driver.find_element(by=By.NAME, value="ctl00$ContentPlaceHolder$txtCusid")
     username_box = driver.find_element(
         by=By.NAME, value="ctl00$ContentPlaceHolder$txtUserId"
     )
     pwd_box = driver.find_element(
         by=By.NAME, value="ctl00$ContentPlaceHolder$txtPassword"
     )
     login_button = driver.find_element(by=By.ID, value="ContentPlaceHolder_btLogin")
 
     cID_box.send_keys(cID)
     username_box.send_keys(uID)
     pwd_box.send_keys(pwd)
 
-    driver.implicitly_wait(1)
-
     login_button.click()
 
-    driver.implicitly_wait(1)
-
     try:
         continueLogIn = driver.find_element(
             by=By.NAME, value="ctl00$ContentPlaceHolder$btnContinueLogin"
         )
         continueLogIn.click()
     except:
         pass
 
     driver.get("https://v2.alacourt.com/frmIndexSearchForm.aspx")
 
     print("Successfully connected and logged into Alacourt!")
 
-    driver.implicitly_wait(1)
-
     return driver
 
 
 def empty_query(path):
     """Create empty spreadsheet to fill and import as query submit search list to retrieve matching case records from Alacourt.com.
 
     Args:
@@ -7074,7 +7056,63 @@
             "",
             out,
             re.DOTALL,
         )
         return out.strip()
     else:
         return ""
+
+def getBalanceByFeeCode(text, code):
+    pat = f"(ACTIVE[^\n]+{code}[^\n]+)"
+    rows = re.findall(pat, text)
+    tot = 0.0
+    for r in rows:
+        splr = re.findall(r"\$\d+\.\d{2}", r)
+        if len(splr) > 0:
+            bal = float(re.sub(r'\$','',splr[-1]))
+            tot += bal
+    if len(rows) == 0:
+        return None
+    if len(rows) > 0:
+        return tot
+
+def getAmtDueByFeeCode(text, code):
+    pat = f"(ACTIVE[^\n]+{code}[^\n]+)"
+    rows = re.findall(pat, text)
+    tot = 0.0
+    for r in rows:
+        splr = re.findall(r"\$\d+\.\d{2}", r)
+        if len(splr) > 0:
+            bal = float(re.sub(r'\$','',splr[0]))
+            tot += bal
+    if len(rows) == 0:
+        return None
+    if len(rows) > 0:
+        return tot
+
+def getAmtPaidByFeeCode(text, code):
+    pat = f"(ACTIVE[^\n]+{code}[^\n]+)"
+    rows = re.findall(pat, text)
+    tot = 0.0
+    for r in rows:
+        splr = re.findall(r"\$\d+\.\d{2}", r)
+        if len(splr) > 0:
+            bal = float(re.sub(r'\$','',splr[1]))
+            tot += bal
+    if len(rows) == 0:
+        return None
+    if len(rows) > 0:
+        return tot
+
+def getAmtHoldByFeeCode(text, code):
+    pat = f"(ACTIVE[^\n]+{code}[^\n]+)"
+    rows = re.findall(pat, text)
+    tot = 0.0
+    for r in rows:
+        splr = re.findall(r"\$\d+\.\d{2}", r)
+        if len(splr) > 0:
+            bal = float(re.sub(r'\$','',splr[2]))
+            tot += bal
+    if len(rows) == 0:
+        return None
+    if len(rows) > 0:
+        return tot
```

### Comparing `alacorder-80.4.7/PKG-INFO` & `alacorder-80.4.8/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: alacorder
-Version: 80.4.7
+Version: 80.4.8
 Summary: Alacorder collects and processes Alacourt case detail PDFs into data tables suitable for research purposes.
 License: MIT
 Author: Sam Robson
 Author-email: sbrobson@crimson.ua.edu
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -13,14 +13,15 @@
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: PyMuPDF (>=1.21.1,<2.0.0)
 Requires-Dist: PySimpleGUI (>=4.60.4,<5.0.0)
 Requires-Dist: XlsxWriter (>=3.0.9,<4.0.0)
 Requires-Dist: brotli (>=1.0.9,<2.0.0)
 Requires-Dist: click (>=8.1.3,<9.0.0)
 Requires-Dist: polars (>=0.17.6,<0.18.0)
+Requires-Dist: pyarrow (>=12.0.0,<13.0.0)
 Requires-Dist: selenium (>=4.8.3,<5.0.0)
 Requires-Dist: tqdm (>=4.65.0,<5.0.0)
 Requires-Dist: xlsx2csv (>=0.8.1,<0.9.0)
 Description-Content-Type: text/markdown
 
 ```
     ___    __                          __
```

