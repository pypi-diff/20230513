# Comparing `tmp/google-sheet-downloader-1.0.5.tar.gz` & `tmp/google-sheet-downloader-1.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "google-sheet-downloader-1.0.5.tar", last modified: Sat May 13 01:52:50 2023, max compression
+gzip compressed data, was "google-sheet-downloader-1.0.6.tar", last modified: Sat May 13 02:34:51 2023, max compression
```

## Comparing `google-sheet-downloader-1.0.5.tar` & `google-sheet-downloader-1.0.6.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 01:52:50.662193 google-sheet-downloader-1.0.5/
--rw-r--r--   0 chiubowen   (501) staff       (20)     4694 2023-05-13 01:52:50.662083 google-sheet-downloader-1.0.5/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)     4513 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/README.md
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 01:52:50.661916 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/
--rw-r--r--   0 chiubowen   (501) staff       (20)     4694 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)      329 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/SOURCES.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/dependency_links.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       74 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/entry_points.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       75 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/requires.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       24 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/top_level.txt
--rwxr-xr-x   0 chiubowen   (501) staff       (20)     3127 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.py
--rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-13 01:52:50.662231 google-sheet-downloader-1.0.5/setup.cfg
--rw-r--r--   0 chiubowen   (501) staff       (20)      556 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/setup.py
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 02:34:51.657940 google-sheet-downloader-1.0.6/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     4694 2023-05-13 02:34:51.657832 google-sheet-downloader-1.0.6/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)     4513 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/README.md
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 02:34:51.657652 google-sheet-downloader-1.0.6/google_sheet_downloader.egg-info/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     4694 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/google_sheet_downloader.egg-info/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)      329 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/google_sheet_downloader.egg-info/SOURCES.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/google_sheet_downloader.egg-info/dependency_links.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       74 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/google_sheet_downloader.egg-info/entry_points.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       75 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/google_sheet_downloader.egg-info/requires.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       24 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/google_sheet_downloader.egg-info/top_level.txt
+-rwxr-xr-x   0 chiubowen   (501) staff       (20)     3133 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/google_sheet_downloader.py
+-rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-13 02:34:51.657977 google-sheet-downloader-1.0.6/setup.cfg
+-rw-r--r--   0 chiubowen   (501) staff       (20)      556 2023-05-13 02:34:51.000000 google-sheet-downloader-1.0.6/setup.py
```

### Comparing `google-sheet-downloader-1.0.5/PKG-INFO` & `google-sheet-downloader-1.0.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: google-sheet-downloader
-Version: 1.0.5
+Version: 1.0.6
 Summary: UNKNOWN
 Home-page: UNKNOWN
 License: UNKNOWN
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # 積木塊：Google Sheets 下載器 v1.0.4 by Bowen Chiu 2023-05-12 15:32
```

### Comparing `google-sheet-downloader-1.0.5/README.md` & `google-sheet-downloader-1.0.6/README.md`

 * *Files identical despite different names*

### Comparing `google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/PKG-INFO` & `google-sheet-downloader-1.0.6/google_sheet_downloader.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: google-sheet-downloader
-Version: 1.0.5
+Version: 1.0.6
 Summary: UNKNOWN
 Home-page: UNKNOWN
 License: UNKNOWN
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # 積木塊：Google Sheets 下載器 v1.0.4 by Bowen Chiu 2023-05-12 15:32
```

### Comparing `google-sheet-downloader-1.0.5/google_sheet_downloader.py` & `google-sheet-downloader-1.0.6/google_sheet_downloader.py`

 * *Files 1% similar despite different names*

```diff
@@ -60,29 +60,29 @@
 
 
 def download_google_sheets(key_file, sheet_ids, output_folder, force):
     gspread_client = None
 
     for sheet_id in sheet_ids.split(','):
         if not force and is_downloaded(output_folder, sheet_id):
-            print(f"Skipping: Sheet ID {sheet_id} (Already downloaded)")
+            # print(f"Skipping: Sheet ID {sheet_id} (Already downloaded)")
             continue
 
         if gspread_client is None:
             gspread_client = init_gspread(key_file)
 
         sheet = gspread_client.open_by_key(sheet_id)
         for worksheet in sheet.worksheets():
             sheet_name = sheet.title
             worksheet_name = worksheet.title
-            print(f"Checking: {sheet_name} - {worksheet_name}")
+            # print(f"Checking: {sheet_name} - {worksheet_name}")
 
             data = get_all_values(gspread_client, sheet_id, worksheet_name)
             save_to_csv(data, output_folder, sheet_name, worksheet_name, sheet_id)
-            print(f"Saved: {sheet_name} - {worksheet_name}")
+            # print(f"Saved: {sheet_name} - {worksheet_name}")
 
 
 def main():
     args = parse_arguments()
     download_google_sheets(args.key_file, args.sheet_ids, args.output_folder, args.force)
```

### Comparing `google-sheet-downloader-1.0.5/setup.py` & `google-sheet-downloader-1.0.6/setup.py`

 * *Files 25% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from setuptools import setup, find_packages
 
 with open('requirements.txt') as f:
     requirements = [line.strip() for line in f.readlines()]
 
 setup(
     name="google-sheet-downloader",
-    version="1.0.5",
+    version="1.0.6",
     packages=find_packages(),
     py_modules=['google_sheet_downloader'],
     install_requires=requirements,
     entry_points={
         'console_scripts': [
             'google_sheet_downloader = google_sheet_downloader:main',
         ],
```

