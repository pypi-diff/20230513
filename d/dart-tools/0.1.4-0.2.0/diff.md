# Comparing `tmp/dart-tools-0.1.4.tar.gz` & `tmp/dart-tools-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dart-tools-0.1.4.tar", last modified: Fri May 12 07:03:16 2023, max compression
+gzip compressed data, was "dart-tools-0.2.0.tar", last modified: Sat May 13 07:21:37 2023, max compression
```

## Comparing `dart-tools-0.1.4.tar` & `dart-tools-0.2.0.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 zack       (501) staff       (20)        0 2023-05-12 07:03:16.654452 dart-tools-0.1.4/
--rw-r--r--   0 zack       (501) staff       (20)     1061 2023-02-28 02:56:19.000000 dart-tools-0.1.4/LICENSE
--rw-r--r--   0 zack       (501) staff       (20)     4358 2023-05-12 07:03:16.653993 dart-tools-0.1.4/PKG-INFO
--rw-r--r--   0 zack       (501) staff       (20)     1510 2023-04-03 00:03:57.000000 dart-tools-0.1.4/README.md
-drwxr-xr-x   0 zack       (501) staff       (20)        0 2023-05-12 07:03:16.650816 dart-tools-0.1.4/dart/
--rw-r--r--   0 zack       (501) staff       (20)       64 2023-02-28 04:01:58.000000 dart-tools-0.1.4/dart/__init__.py
--rwxr-xr-x   0 zack       (501) staff       (20)    11756 2023-05-12 06:37:54.000000 dart-tools-0.1.4/dart/dart.py
--rw-r--r--   0 zack       (501) staff       (20)     1709 2023-02-28 02:57:20.000000 dart-tools-0.1.4/dart/order_manager.py
-drwxr-xr-x   0 zack       (501) staff       (20)        0 2023-05-12 07:03:16.653447 dart-tools-0.1.4/dart_tools.egg-info/
--rw-r--r--   0 zack       (501) staff       (20)     4358 2023-05-12 07:03:16.000000 dart-tools-0.1.4/dart_tools.egg-info/PKG-INFO
--rw-r--r--   0 zack       (501) staff       (20)      290 2023-05-12 07:03:16.000000 dart-tools-0.1.4/dart_tools.egg-info/SOURCES.txt
--rw-r--r--   0 zack       (501) staff       (20)        1 2023-05-12 07:03:16.000000 dart-tools-0.1.4/dart_tools.egg-info/dependency_links.txt
--rw-r--r--   0 zack       (501) staff       (20)       34 2023-05-12 07:03:16.000000 dart-tools-0.1.4/dart_tools.egg-info/entry_points.txt
--rw-r--r--   0 zack       (501) staff       (20)       14 2023-05-12 07:03:16.000000 dart-tools-0.1.4/dart_tools.egg-info/requires.txt
--rw-r--r--   0 zack       (501) staff       (20)        5 2023-05-12 07:03:16.000000 dart-tools-0.1.4/dart_tools.egg-info/top_level.txt
--rw-r--r--   0 zack       (501) staff       (20)     1744 2023-05-12 06:37:53.000000 dart-tools-0.1.4/pyproject.toml
--rw-r--r--   0 zack       (501) staff       (20)       38 2023-05-12 07:03:16.654573 dart-tools-0.1.4/setup.cfg
+drwxr-xr-x   0 zack       (501) staff       (20)        0 2023-05-13 07:21:37.184260 dart-tools-0.2.0/
+-rw-r--r--   0 zack       (501) staff       (20)     1061 2023-02-28 02:56:19.000000 dart-tools-0.2.0/LICENSE
+-rw-r--r--   0 zack       (501) staff       (20)     4358 2023-05-13 07:21:37.183916 dart-tools-0.2.0/PKG-INFO
+-rw-r--r--   0 zack       (501) staff       (20)     1510 2023-04-03 00:03:57.000000 dart-tools-0.2.0/README.md
+drwxr-xr-x   0 zack       (501) staff       (20)        0 2023-05-13 07:21:37.181131 dart-tools-0.2.0/dart/
+-rw-r--r--   0 zack       (501) staff       (20)       64 2023-02-28 04:01:58.000000 dart-tools-0.2.0/dart/__init__.py
+-rwxr-xr-x   0 zack       (501) staff       (20)    11703 2023-05-13 07:20:34.000000 dart-tools-0.2.0/dart/dart.py
+-rw-r--r--   0 zack       (501) staff       (20)     1709 2023-02-28 02:57:20.000000 dart-tools-0.2.0/dart/order_manager.py
+drwxr-xr-x   0 zack       (501) staff       (20)        0 2023-05-13 07:21:37.183406 dart-tools-0.2.0/dart_tools.egg-info/
+-rw-r--r--   0 zack       (501) staff       (20)     4358 2023-05-13 07:21:37.000000 dart-tools-0.2.0/dart_tools.egg-info/PKG-INFO
+-rw-r--r--   0 zack       (501) staff       (20)      290 2023-05-13 07:21:37.000000 dart-tools-0.2.0/dart_tools.egg-info/SOURCES.txt
+-rw-r--r--   0 zack       (501) staff       (20)        1 2023-05-13 07:21:37.000000 dart-tools-0.2.0/dart_tools.egg-info/dependency_links.txt
+-rw-r--r--   0 zack       (501) staff       (20)       34 2023-05-13 07:21:37.000000 dart-tools-0.2.0/dart_tools.egg-info/entry_points.txt
+-rw-r--r--   0 zack       (501) staff       (20)       14 2023-05-13 07:21:37.000000 dart-tools-0.2.0/dart_tools.egg-info/requires.txt
+-rw-r--r--   0 zack       (501) staff       (20)        5 2023-05-13 07:21:37.000000 dart-tools-0.2.0/dart_tools.egg-info/top_level.txt
+-rw-r--r--   0 zack       (501) staff       (20)     1744 2023-05-13 07:20:34.000000 dart-tools-0.2.0/pyproject.toml
+-rw-r--r--   0 zack       (501) staff       (20)       38 2023-05-13 07:21:37.184370 dart-tools-0.2.0/setup.cfg
```

### Comparing `dart-tools-0.1.4/LICENSE` & `dart-tools-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `dart-tools-0.1.4/PKG-INFO` & `dart-tools-0.2.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dart-tools
-Version: 0.1.4
+Version: 0.2.0
 Summary: The Dart CLI and Python Library
 Author-email: Dart Software Team <software@itsdart.com>
 License: MIT License
         
         Copyright (c) 2023 Dart
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: dart-tools Version: 0.1.4 Summary: The Dart CLI and
+Metadata-Version: 2.1 Name: dart-tools Version: 0.2.0 Summary: The Dart CLI and
 Python Library Author-email: Dart Software Team
 itsdart.com> License: MIT License Copyright (c) 2023 Dart Permission is hereby
 granted, free of charge, to any person obtaining a copy of this software and
 associated documentation files (the "Software"), to deal in the Software
 without restriction, including without limitation the rights to use, copy,
 modify, merge, publish, distribute, sublicense, and/or sell copies of the
 Software, and to permit persons to whom the Software is furnished to do so,
```

### Comparing `dart-tools-0.1.4/README.md` & `dart-tools-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `dart-tools-0.1.4/dart/dart.py` & `dart-tools-0.2.0/dart/dart.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,14 @@
 import json
 import os
 import random
 import re
 import string
 import subprocess
 import sys
-from uuid import uuid4
 
 from pick import pick
 import requests
 
 from .order_manager import get_orders_between
 
 
@@ -325,33 +324,32 @@
 def create_task(title):
     config = _Config()
     session = _Session(config)
 
     user_bundle = _get_full_user_bundle(session)
 
     user_email = user_bundle["user"]["email"]
-    active_uuid = next(
-        e["uuid"] for e in user_bundle["dartboards"] if e["kind"] == "Active"
+    active_duid = next(
+        e["duid"] for e in user_bundle["dartboards"] if e["kind"] == "Active"
     )
     first_order = min(
-        e["order"] for e in user_bundle["tasks"] if e["dartboardUuid"] == active_uuid
+        e["order"] for e in user_bundle["tasks"] if e["dartboardDuid"] == active_duid
     )
     order = get_orders_between(None, first_order, 1)[0]
     status_duid = next(
         e["duid"]
         for e in user_bundle["statuses"]
         if e["kind"] == "Unstarted" and e["locked"]
     )
 
     print("Creating task")
     task = {
         "duid": _make_duid(),
-        "uuid": str(uuid4()),
         "drafterEmail": None,
-        "dartboardUuid": active_uuid,
+        "dartboardDuid": active_duid,
         "order": order,
         "title": title,
         "description": _DEFAULT_DESCRIPTION,
         "statusDuid": status_duid,
         "assigneeEmails": [user_email],
         "subscriberEmails": [user_email],
         "tagDuids": [],
```

### Comparing `dart-tools-0.1.4/dart/order_manager.py` & `dart-tools-0.2.0/dart/order_manager.py`

 * *Files identical despite different names*

### Comparing `dart-tools-0.1.4/dart_tools.egg-info/PKG-INFO` & `dart-tools-0.2.0/dart_tools.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dart-tools
-Version: 0.1.4
+Version: 0.2.0
 Summary: The Dart CLI and Python Library
 Author-email: Dart Software Team <software@itsdart.com>
 License: MIT License
         
         Copyright (c) 2023 Dart
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: dart-tools Version: 0.1.4 Summary: The Dart CLI and
+Metadata-Version: 2.1 Name: dart-tools Version: 0.2.0 Summary: The Dart CLI and
 Python Library Author-email: Dart Software Team
 itsdart.com> License: MIT License Copyright (c) 2023 Dart Permission is hereby
 granted, free of charge, to any person obtaining a copy of this software and
 associated documentation files (the "Software"), to deal in the Software
 without restriction, including without limitation the rights to use, copy,
 modify, merge, publish, distribute, sublicense, and/or sell copies of the
 Software, and to permit persons to whom the Software is furnished to do so,
```

### Comparing `dart-tools-0.1.4/pyproject.toml` & `dart-tools-0.2.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "dart-tools"
-version = "0.1.4"
+version = "0.2.0"
 description = "The Dart CLI and Python Library"
 readme = "README.md"
 requires-python = ">=3.8"
 
 license = {file = "LICENSE"}
 keywords = ["dart", "cli", "projectmanagement", "taskmanagement"]
 authors = [
```

