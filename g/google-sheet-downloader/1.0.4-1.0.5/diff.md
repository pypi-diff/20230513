# Comparing `tmp/google-sheet-downloader-1.0.4.tar.gz` & `tmp/google-sheet-downloader-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "google-sheet-downloader-1.0.4.tar", last modified: Fri May 12 07:34:40 2023, max compression
+gzip compressed data, was "google-sheet-downloader-1.0.5.tar", last modified: Sat May 13 01:52:50 2023, max compression
```

## Comparing `google-sheet-downloader-1.0.4.tar` & `google-sheet-downloader-1.0.5.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 07:34:40.837172 google-sheet-downloader-1.0.4/
--rw-r--r--   0 chiubowen   (501) staff       (20)     4694 2023-05-12 07:34:40.837065 google-sheet-downloader-1.0.4/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)     4513 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/README.md
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 07:34:40.836887 google-sheet-downloader-1.0.4/google_sheet_downloader.egg-info/
--rw-r--r--   0 chiubowen   (501) staff       (20)     4694 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/google_sheet_downloader.egg-info/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)      329 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/google_sheet_downloader.egg-info/SOURCES.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/google_sheet_downloader.egg-info/dependency_links.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)      130 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/google_sheet_downloader.egg-info/entry_points.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       75 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/google_sheet_downloader.egg-info/requires.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       44 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/google_sheet_downloader.egg-info/top_level.txt
--rwxr-xr-x   0 chiubowen   (501) staff       (20)     3051 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/google_sheet_downloader.py
--rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-12 07:34:40.837205 google-sheet-downloader-1.0.4/setup.cfg
--rw-r--r--   0 chiubowen   (501) staff       (20)      638 2023-05-12 07:34:40.000000 google-sheet-downloader-1.0.4/setup.py
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 01:52:50.662193 google-sheet-downloader-1.0.5/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     4694 2023-05-13 01:52:50.662083 google-sheet-downloader-1.0.5/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)     4513 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/README.md
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 01:52:50.661916 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     4694 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)      329 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/SOURCES.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/dependency_links.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       74 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/entry_points.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       75 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/requires.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       24 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/top_level.txt
+-rwxr-xr-x   0 chiubowen   (501) staff       (20)     3127 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/google_sheet_downloader.py
+-rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-13 01:52:50.662231 google-sheet-downloader-1.0.5/setup.cfg
+-rw-r--r--   0 chiubowen   (501) staff       (20)      556 2023-05-13 01:52:50.000000 google-sheet-downloader-1.0.5/setup.py
```

### Comparing `google-sheet-downloader-1.0.4/PKG-INFO` & `google-sheet-downloader-1.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: google-sheet-downloader
-Version: 1.0.4
+Version: 1.0.5
 Summary: UNKNOWN
 Home-page: UNKNOWN
 License: UNKNOWN
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # 積木塊：Google Sheets 下載器 v1.0.4 by Bowen Chiu 2023-05-12 15:32
```

### Comparing `google-sheet-downloader-1.0.4/README.md` & `google-sheet-downloader-1.0.5/README.md`

 * *Files identical despite different names*

### Comparing `google-sheet-downloader-1.0.4/google_sheet_downloader.egg-info/PKG-INFO` & `google-sheet-downloader-1.0.5/google_sheet_downloader.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: google-sheet-downloader
-Version: 1.0.4
+Version: 1.0.5
 Summary: UNKNOWN
 Home-page: UNKNOWN
 License: UNKNOWN
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # 積木塊：Google Sheets 下載器 v1.0.4 by Bowen Chiu 2023-05-12 15:32
```

### Comparing `google-sheet-downloader-1.0.4/google_sheet_downloader.py` & `google-sheet-downloader-1.0.5/google_sheet_downloader.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,17 +1,19 @@
 #!/usr/bin/env python
+# google_sheet_downloader.py
 import argparse
 import csv
 import glob
 import json
 import os
 
 import gspread
 from google.oauth2.service_account import Credentials
 
+
 def init_gspread(key_file):
     scopes = [
         "https://spreadsheets.google.com/feeds",
         'https://www.googleapis.com/auth/spreadsheets',
         "https://www.googleapis.com/auth/drive.file",
         "https://www.googleapis.com/auth/drive"
     ]
@@ -35,14 +37,15 @@
     pattern = os.path.join(output_folder, f"doc-id_{sheet_id}*.csv")
     matching_files = glob.glob(pattern)
 
     return len(matching_files) > 0
 
 
 def save_to_csv(data, output_folder, sheet_name, worksheet_name, sheet_id):
+    os.makedirs(output_folder, exist_ok=True)
     output_file = os.path.join(output_folder,
                                f"doc-id_{sheet_id}_spreadsheet_{sheet_name}_worksheet_{worksheet_name}.csv")
     with open(output_file, 'w', newline='', encoding='utf-8') as f:
         writer = csv.writer(f)
         writer.writerows(data)
```

### Comparing `google-sheet-downloader-1.0.4/setup.py` & `google-sheet-downloader-1.0.5/setup.py`

 * *Files 27% similar despite different names*

```diff
@@ -2,18 +2,18 @@
 from setuptools import setup, find_packages
 
 with open('requirements.txt') as f:
     requirements = [line.strip() for line in f.readlines()]
 
 setup(
     name="google-sheet-downloader",
-    version="1.0.4",
+    version="1.0.5",
     packages=find_packages(),
-    py_modules=['google_sheet_downloader', 'requirements', 'README'],
+    py_modules=['google_sheet_downloader'],
     install_requires=requirements,
     entry_points={
         'console_scripts': [
-            'google_sheet_downloader = google_sheet_downloader:main, requirements = requirements:main, README = README:main',
+            'google_sheet_downloader = google_sheet_downloader:main',
         ],
     },
     long_description=open('README.md', 'r').read(),
     long_description_content_type='text/markdown',)
```

