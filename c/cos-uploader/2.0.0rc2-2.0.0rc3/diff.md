# Comparing `tmp/cos_uploader-2.0.0rc2.tar.gz` & `tmp/cos_uploader-2.0.0rc3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cos_uploader-2.0.0rc2.tar", max compression
+gzip compressed data, was "cos_uploader-2.0.0rc3.tar", max compression
```

## Comparing `cos_uploader-2.0.0rc2.tar` & `cos_uploader-2.0.0rc3.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1091 2023-05-07 17:55:26.777619 cos_uploader-2.0.0rc2/LICENSE
--rw-r--r--   0        0        0     4761 2023-05-07 18:08:41.052601 cos_uploader-2.0.0rc2/README.md
--rw-r--r--   0        0        0     4597 2023-05-07 18:08:32.724769 cos_uploader-2.0.0rc2/cos_uploader/__init__.py
--rw-r--r--   0        0        0      716 2023-05-07 17:55:26.778063 cos_uploader-2.0.0rc2/cos_uploader/common.py
--rw-r--r--   0        0        0      631 2023-05-07 18:07:55.273444 cos_uploader-2.0.0rc2/cos_uploader/config.toml
--rw-r--r--   0        0        0     2083 2023-05-07 18:07:37.244130 cos_uploader-2.0.0rc2/cos_uploader/history.py
--rw-r--r--   0        0        0     1237 2023-05-07 17:55:26.778434 cos_uploader-2.0.0rc2/cos_uploader/install.py
--rw-r--r--   0        0        0      858 2023-05-07 18:07:47.353705 cos_uploader-2.0.0rc2/pyproject.toml
--rw-r--r--   0        0        0     5650 1970-01-01 00:00:00.000000 cos_uploader-2.0.0rc2/PKG-INFO
+-rw-r--r--   0        0        0     1091 2023-05-13 10:21:28.622093 cos_uploader-2.0.0rc3/LICENSE
+-rw-r--r--   0        0        0     4761 2023-05-13 10:21:28.622263 cos_uploader-2.0.0rc3/README.md
+-rw-r--r--   0        0        0     4597 2023-05-13 10:21:28.622459 cos_uploader-2.0.0rc3/cos_uploader/__init__.py
+-rw-r--r--   0        0        0      716 2023-05-13 10:21:28.622571 cos_uploader-2.0.0rc3/cos_uploader/common.py
+-rw-r--r--   0        0        0      631 2023-05-13 10:21:28.622675 cos_uploader-2.0.0rc3/cos_uploader/config.toml
+-rw-r--r--   0        0        0     2086 2023-05-13 10:21:50.824321 cos_uploader-2.0.0rc3/cos_uploader/history.py
+-rw-r--r--   0        0        0     1237 2023-05-13 10:21:28.622891 cos_uploader-2.0.0rc3/cos_uploader/install.py
+-rw-r--r--   0        0        0      858 2023-05-13 10:22:09.035458 cos_uploader-2.0.0rc3/pyproject.toml
+-rw-r--r--   0        0        0     5650 1970-01-01 00:00:00.000000 cos_uploader-2.0.0rc3/PKG-INFO
```

### Comparing `cos_uploader-2.0.0rc2/LICENSE` & `cos_uploader-2.0.0rc3/LICENSE`

 * *Files identical despite different names*

### Comparing `cos_uploader-2.0.0rc2/README.md` & `cos_uploader-2.0.0rc3/README.md`

 * *Files identical despite different names*

### Comparing `cos_uploader-2.0.0rc2/cos_uploader/__init__.py` & `cos_uploader-2.0.0rc3/cos_uploader/__init__.py`

 * *Files identical despite different names*

### Comparing `cos_uploader-2.0.0rc2/cos_uploader/common.py` & `cos_uploader-2.0.0rc3/cos_uploader/common.py`

 * *Files identical despite different names*

### Comparing `cos_uploader-2.0.0rc2/cos_uploader/config.toml` & `cos_uploader-2.0.0rc3/cos_uploader/config.toml`

 * *Files identical despite different names*

### Comparing `cos_uploader-2.0.0rc2/cos_uploader/history.py` & `cos_uploader-2.0.0rc3/cos_uploader/history.py`

 * *Files 1% similar despite different names*

```diff
@@ -19,15 +19,15 @@
     if year < 2000 or year > 2100 or month < 1 or month > 12:
         print("ERROR: Invalid Year or Month", file=sys.stderr)
         sys.exit(1)
     year = str(year)
     month = str(month).zfill(2)
 
     config = load_config()
-    file = os.path.join(config["base"], f"history-{year}-{month}.log")
+    file = os.path.join(config["base"], f"history-{year}-{month}.ndjson")
     if not os.path.exists(file):
         print(f"ERROR: History File '{file}' Not Found, maybe you have not uploaded any files in {year}-{month} ?", file=sys.stderr)
         sys.exit(1)
     
     lines = []
     with open(file, "r", encoding="utf-8") as f:
         if args.limit == 0:
```

### Comparing `cos_uploader-2.0.0rc2/cos_uploader/install.py` & `cos_uploader-2.0.0rc3/cos_uploader/install.py`

 * *Files identical despite different names*

### Comparing `cos_uploader-2.0.0rc2/pyproject.toml` & `cos_uploader-2.0.0rc3/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "cos-uploader"
-version = "2.0.0-rc.2"
+version = "2.0.0-rc.3"
 description = "CLI tool for uploading files to Tencent COS"
 authors = ["Joseph Chris <joseph@josephcz.xyz>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "cos_uploader"}]
 include = ["cos_uploader/config.toml"]
 homepage = "https://github.com/baobao1270/cos-uploader"
```

### Comparing `cos_uploader-2.0.0rc2/PKG-INFO` & `cos_uploader-2.0.0rc3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cos-uploader
-Version: 2.0.0rc2
+Version: 2.0.0rc3
 Summary: CLI tool for uploading files to Tencent COS
 Home-page: https://github.com/baobao1270/cos-uploader
 License: MIT
 Keywords: tencent-cos,uploader
 Author: Joseph Chris
 Author-email: joseph@josephcz.xyz
 Requires-Python: >=3.8,<4.0
```

