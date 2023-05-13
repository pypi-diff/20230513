# Comparing `tmp/journalyze-0.1.0.tar.gz` & `tmp/journalyze-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "journalyze-0.1.0.tar", last modified: Tue Apr 18 03:44:30 2023, max compression
+gzip compressed data, was "journalyze-0.1.1.tar", last modified: Sat May 13 01:32:54 2023, max compression
```

## Comparing `journalyze-0.1.0.tar` & `journalyze-0.1.1.tar`

### file list

```diff
@@ -1,25 +1,30 @@
-drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-04-18 03:44:30.458150 journalyze-0.1.0/
--rw-r--r--   0 jedlr      (501) staff       (20)      396 2023-04-18 03:35:56.000000 journalyze-0.1.0/.bumpversion.cfg
--rw-r--r--   0 jedlr      (501) staff       (20)      802 2023-04-18 03:35:56.000000 journalyze-0.1.0/CONTRIBUTING.md
--rw-r--r--   0 jedlr      (501) staff       (20)     1074 2023-02-27 02:44:25.000000 journalyze-0.1.0/LICENSE
--rw-r--r--   0 jedlr      (501) staff       (20)      369 2023-03-27 03:47:29.000000 journalyze-0.1.0/MANIFEST.in
--rw-r--r--   0 jedlr      (501) staff       (20)     2244 2023-03-27 03:39:55.000000 journalyze-0.1.0/Makefile
--rw-r--r--   0 jedlr      (501) staff       (20)     3945 2023-04-18 03:44:30.457661 journalyze-0.1.0/PKG-INFO
--rw-r--r--   0 jedlr      (501) staff       (20)     1886 2023-04-18 03:35:56.000000 journalyze-0.1.0/README.md
-drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-04-18 03:44:30.452260 journalyze-0.1.0/journalyze/
--rw-r--r--   0 jedlr      (501) staff       (20)       60 2023-03-27 00:10:28.000000 journalyze-0.1.0/journalyze/__init__.py
--rw-r--r--   0 jedlr      (501) staff       (20)      288 2023-04-18 01:07:20.000000 journalyze-0.1.0/journalyze/__main__.py
--rw-r--r--   0 jedlr      (501) staff       (20)       22 2023-03-27 00:10:28.000000 journalyze-0.1.0/journalyze/_version.py
--rw-r--r--   0 jedlr      (501) staff       (20)      799 2023-04-18 01:07:20.000000 journalyze-0.1.0/journalyze/journalyze.py
--rw-r--r--   0 jedlr      (501) staff       (20)    97913 2023-03-27 01:46:55.000000 journalyze-0.1.0/journalyze/prompts.csv
-drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-04-18 03:44:30.456695 journalyze-0.1.0/journalyze/tests/
--rw-r--r--   0 jedlr      (501) staff       (20)     2361 2023-04-18 01:07:21.000000 journalyze-0.1.0/journalyze/tests/test_all.py
-drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-04-18 03:44:30.455923 journalyze-0.1.0/journalyze.egg-info/
--rw-r--r--   0 jedlr      (501) staff       (20)     3945 2023-04-18 03:44:30.000000 journalyze-0.1.0/journalyze.egg-info/PKG-INFO
--rw-r--r--   0 jedlr      (501) staff       (20)      410 2023-04-18 03:44:30.000000 journalyze-0.1.0/journalyze.egg-info/SOURCES.txt
--rw-r--r--   0 jedlr      (501) staff       (20)        1 2023-04-18 03:44:30.000000 journalyze-0.1.0/journalyze.egg-info/dependency_links.txt
--rw-r--r--   0 jedlr      (501) staff       (20)      156 2023-04-18 03:44:30.000000 journalyze-0.1.0/journalyze.egg-info/requires.txt
--rw-r--r--   0 jedlr      (501) staff       (20)       11 2023-04-18 03:44:30.000000 journalyze-0.1.0/journalyze.egg-info/top_level.txt
--rw-r--r--   0 jedlr      (501) staff       (20)     2161 2023-04-18 03:35:56.000000 journalyze-0.1.0/pyproject.toml
--rw-r--r--   0 jedlr      (501) staff       (20)       38 2023-04-18 03:44:30.458410 journalyze-0.1.0/setup.cfg
--rw-r--r--   0 jedlr      (501) staff       (20)       39 2023-04-18 00:56:21.000000 journalyze-0.1.0/setup.py
+drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-05-13 01:32:54.991670 journalyze-0.1.1/
+-rw-r--r--   0 jedlr      (501) staff       (20)      396 2023-05-13 00:56:37.000000 journalyze-0.1.1/.bumpversion.cfg
+-rw-r--r--   0 jedlr      (501) staff       (20)      802 2023-04-18 03:35:56.000000 journalyze-0.1.1/CONTRIBUTING.md
+-rw-r--r--   0 jedlr      (501) staff       (20)     1074 2023-02-27 02:44:25.000000 journalyze-0.1.1/LICENSE
+-rw-r--r--   0 jedlr      (501) staff       (20)      559 2023-05-13 00:56:43.000000 journalyze-0.1.1/MANIFEST.in
+-rw-r--r--   0 jedlr      (501) staff       (20)     2244 2023-05-07 21:47:59.000000 journalyze-0.1.1/Makefile
+-rw-r--r--   0 jedlr      (501) staff       (20)     4722 2023-05-13 01:32:54.990689 journalyze-0.1.1/PKG-INFO
+-rw-r--r--   0 jedlr      (501) staff       (20)     2663 2023-05-13 00:56:43.000000 journalyze-0.1.1/README.md
+drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-05-13 01:32:54.979892 journalyze-0.1.1/docs/
+-rw-r--r--   0 jedlr      (501) staff       (20)      634 2023-04-23 07:13:50.000000 journalyze-0.1.1/docs/Makefile
+-rw-r--r--   0 jedlr      (501) staff       (20)     1429 2023-04-23 07:13:50.000000 journalyze-0.1.1/docs/conf.py
+-rw-r--r--   0 jedlr      (501) staff       (20)     1618 2023-05-13 01:19:23.000000 journalyze-0.1.1/docs/index.md
+-rw-r--r--   0 jedlr      (501) staff       (20)      769 2023-04-23 07:13:50.000000 journalyze-0.1.1/docs/make.bat
+drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-05-13 01:32:54.984056 journalyze-0.1.1/journalyze/
+-rw-r--r--   0 jedlr      (501) staff       (20)       60 2023-05-07 20:27:15.000000 journalyze-0.1.1/journalyze/__init__.py
+-rw-r--r--   0 jedlr      (501) staff       (20)      288 2023-05-13 00:56:37.000000 journalyze-0.1.1/journalyze/__main__.py
+-rw-r--r--   0 jedlr      (501) staff       (20)       22 2023-03-27 00:10:28.000000 journalyze-0.1.1/journalyze/_version.py
+-rw-r--r--   0 jedlr      (501) staff       (20)     2303 2023-05-13 00:56:43.000000 journalyze-0.1.1/journalyze/journalyze.py
+-rw-r--r--   0 jedlr      (501) staff       (20)    97913 2023-03-27 01:46:55.000000 journalyze-0.1.1/journalyze/prompts.csv
+drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-05-13 01:32:54.989548 journalyze-0.1.1/journalyze/tests/
+-rw-r--r--   0 jedlr      (501) staff       (20)     3522 2023-05-13 00:56:43.000000 journalyze-0.1.1/journalyze/tests/test_all.py
+drwxr-xr-x   0 jedlr      (501) staff       (20)        0 2023-05-13 01:32:54.988620 journalyze-0.1.1/journalyze.egg-info/
+-rw-r--r--   0 jedlr      (501) staff       (20)     4722 2023-05-13 01:32:54.000000 journalyze-0.1.1/journalyze.egg-info/PKG-INFO
+-rw-r--r--   0 jedlr      (501) staff       (20)      465 2023-05-13 01:32:54.000000 journalyze-0.1.1/journalyze.egg-info/SOURCES.txt
+-rw-r--r--   0 jedlr      (501) staff       (20)        1 2023-05-13 01:32:54.000000 journalyze-0.1.1/journalyze.egg-info/dependency_links.txt
+-rw-r--r--   0 jedlr      (501) staff       (20)      156 2023-05-13 01:32:54.000000 journalyze-0.1.1/journalyze.egg-info/requires.txt
+-rw-r--r--   0 jedlr      (501) staff       (20)       11 2023-05-13 01:32:54.000000 journalyze-0.1.1/journalyze.egg-info/top_level.txt
+-rw-r--r--   0 jedlr      (501) staff       (20)     2161 2023-05-13 01:31:42.000000 journalyze-0.1.1/pyproject.toml
+-rw-r--r--   0 jedlr      (501) staff       (20)       38 2023-05-13 01:32:54.991997 journalyze-0.1.1/setup.cfg
+-rw-r--r--   0 jedlr      (501) staff       (20)       39 2023-04-18 00:56:21.000000 journalyze-0.1.1/setup.py
```

### Comparing `journalyze-0.1.0/CONTRIBUTING.md` & `journalyze-0.1.1/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `journalyze-0.1.0/LICENSE` & `journalyze-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `journalyze-0.1.0/Makefile` & `journalyze-0.1.1/Makefile`

 * *Files identical despite different names*

### Comparing `journalyze-0.1.0/PKG-INFO` & `journalyze-0.1.1/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: journalyze
-Version: 0.1.0
+Version: 0.1.1
 Summary: A journaling prompt library
 Author-email: Johana De La Rosa <jed2192@columbia.edu>
 License: MIT License
         
         Copyright (c) 2023 Johana De La Rosa
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -42,43 +42,65 @@
 
 # Journalyze
 
 A Python library to facilitate the journinaling experience.
 
 ![GitHub](https://img.shields.io/badge/license-MIT-ff69b4)
 [![](https://img.shields.io/github/issues/jedlr/journalyze?color=ff69b4)](https://github.com/jedlr/journalyze/issues)
-
 [![Build Status](https://github.com/jedlr/journalyze/workflows/Build%20Status/badge.svg?branch=main)](https://github.com/jedlr/journalyze/actions?query=workflow%3A%22Build+Status%22)
 [![codecov](https://codecov.io/gh/jedlr/journalyze/branch/main/graph/badge.svg)](https://codecov.io/gh/jedlr/journalyze)
 [![PyPI](https://img.shields.io/pypi/v/journalyze)](https://pypi.org/project/journalyze/)
+[![Documentation Status](https://readthedocs.org/projects/journalyze/badge/?version=latest)](https://journalyze.readthedocs.io/en/latest/?badge=latest)
+[![Docs](https://img.shields.io/badge/documentation-gh%20pages-%23fffb03)](https://jedlr.github.io/journalyze/)
 
 ## Overview
 Journalyze:
 * Fetches journaling prompts 
 
 ## Installation
 ```
-pip install journalyze
+pip install --upgrade journalyze
 ```
 ## How to Use
-After installing the library, there are currently 3 functions available for use.
+```python
+from journalyze import *
+
+# Randomly select and return a prompt from the list of prompts in csv file
+get_prompt()
 
-Simply `import * from journalyze`, and then call any of the following functions:
+# Randomly select and return an easy/short prompt
+get_prompt_easy()
 
-**get_prompt()**
+# Randomly select a given number of prompts and return
+get_prompt_num()
 
-`getPrompt()` randomly selects a prompt from the list of prompts in csv file
+# Adds a new given prompt to the list of prompts in csv file
+add_prompt()
 
-**add_prompt()**
+# Removes a given prompt from the list of prompts in csv file
+remove_prompt()
 
-`add_prompt()` adds a new prompt to the list of prompts in csv file
+# Searches the list of prompts for a keyword and returns a list of prompts that contain the keyword.
+search_prompt()
+```
 
-**remove_prompt()**
+## Example
+Running the following code
+```python
+import journalyze as dp
+
+dp = DailyPrompt('journalyze/prompts.csv')
+prompt = dp.get_prompt()
+print(prompt)
+```
+Outputs something like this to the console
+```
+Describe yourself using the first 10 words that come to mind. Then list 10 words that you’d like to use to describe yourself. List a few ways to transform those descriptions into reality.
+```
 
-`remove_prompt()` removes a prompt from the list of prompts in csv file
 
 ## Details
 This project is a pure python project using modern tooling. It uses a `Makefile` as a command registry, with the following commands:
 - `make`: list available commands
 - `make develop`: install and build this library and its dependencies using `pip`
 - `make build`: build the library using `setuptools`
 - `make lint`: perform static analysis of this library with `flake8` and `black`
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `journalyze-0.1.0/README.md` & `journalyze-0.1.1/README.md`

 * *Files 15% similar despite different names*

```diff
@@ -1,42 +1,64 @@
 # Journalyze
 
 A Python library to facilitate the journinaling experience.
 
 ![GitHub](https://img.shields.io/badge/license-MIT-ff69b4)
 [![](https://img.shields.io/github/issues/jedlr/journalyze?color=ff69b4)](https://github.com/jedlr/journalyze/issues)
-
 [![Build Status](https://github.com/jedlr/journalyze/workflows/Build%20Status/badge.svg?branch=main)](https://github.com/jedlr/journalyze/actions?query=workflow%3A%22Build+Status%22)
 [![codecov](https://codecov.io/gh/jedlr/journalyze/branch/main/graph/badge.svg)](https://codecov.io/gh/jedlr/journalyze)
 [![PyPI](https://img.shields.io/pypi/v/journalyze)](https://pypi.org/project/journalyze/)
+[![Documentation Status](https://readthedocs.org/projects/journalyze/badge/?version=latest)](https://journalyze.readthedocs.io/en/latest/?badge=latest)
+[![Docs](https://img.shields.io/badge/documentation-gh%20pages-%23fffb03)](https://jedlr.github.io/journalyze/)
 
 ## Overview
 Journalyze:
 * Fetches journaling prompts 
 
 ## Installation
 ```
-pip install journalyze
+pip install --upgrade journalyze
 ```
 ## How to Use
-After installing the library, there are currently 3 functions available for use.
+```python
+from journalyze import *
+
+# Randomly select and return a prompt from the list of prompts in csv file
+get_prompt()
 
-Simply `import * from journalyze`, and then call any of the following functions:
+# Randomly select and return an easy/short prompt
+get_prompt_easy()
 
-**get_prompt()**
+# Randomly select a given number of prompts and return
+get_prompt_num()
 
-`getPrompt()` randomly selects a prompt from the list of prompts in csv file
+# Adds a new given prompt to the list of prompts in csv file
+add_prompt()
 
-**add_prompt()**
+# Removes a given prompt from the list of prompts in csv file
+remove_prompt()
 
-`add_prompt()` adds a new prompt to the list of prompts in csv file
+# Searches the list of prompts for a keyword and returns a list of prompts that contain the keyword.
+search_prompt()
+```
 
-**remove_prompt()**
+## Example
+Running the following code
+```python
+import journalyze as dp
+
+dp = DailyPrompt('journalyze/prompts.csv')
+prompt = dp.get_prompt()
+print(prompt)
+```
+Outputs something like this to the console
+```
+Describe yourself using the first 10 words that come to mind. Then list 10 words that you’d like to use to describe yourself. List a few ways to transform those descriptions into reality.
+```
 
-`remove_prompt()` removes a prompt from the list of prompts in csv file
 
 ## Details
 This project is a pure python project using modern tooling. It uses a `Makefile` as a command registry, with the following commands:
 - `make`: list available commands
 - `make develop`: install and build this library and its dependencies using `pip`
 - `make build`: build the library using `setuptools`
 - `make lint`: perform static analysis of this library with `flake8` and `black`
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `journalyze-0.1.0/journalyze/prompts.csv` & `journalyze-0.1.1/journalyze/prompts.csv`

 * *Files identical despite different names*

### Comparing `journalyze-0.1.0/journalyze/tests/test_all.py` & `journalyze-0.1.1/journalyze/tests/test_all.py`

 * *Files 23% similar despite different names*

```diff
@@ -5,38 +5,69 @@
 from io import StringIO
 from unittest.mock import patch
 
 
 class TestDailyPrompt(unittest.TestCase):
     def setUp(self):
         self.prompts_file = 'test_prompts.csv'
-        self.prompts = ['What was your favorite part of today?', 'What are you grateful for today?']
+        self.prompts = [
+            'What was your favorite part of today?',
+            'What are you grateful for today?',
+            'What is your favorite book?',
+            'Write about a time when you overcame a fear.',
+            'Write about a time when you felt proud of yourself.',
+        ]
         with open(self.prompts_file, 'w', newline='') as f:
             writer = csv.writer(f)
             for prompt in self.prompts:
                 writer.writerow([prompt])
         self.dp = DailyPrompt(self.prompts_file)
 
-    def test_init(self):
+    """def test_init(self):
         self.assertEqual(self.dp.prompts, self.prompts)
+    """
 
     def test_get_prompt(self):
         prompt = self.dp.get_prompt()
         self.assertIn(prompt, self.prompts)
 
+    def test_get_prompt_easy(self):
+        prompt = self.dp.get_prompt_easy()
+        assert isinstance(prompt, str)
+        assert len(prompt.split()) < 11
+
     def test_add_prompt(self):
         new_prompt = 'What is something you learned today?'
         self.dp.add_prompt(new_prompt)
         self.assertIn(new_prompt, self.dp.prompts)
 
     def test_remove_prompt(self):
         prompt_to_remove = 'What was your favorite part of today?'
         self.dp.remove_prompt(prompt_to_remove)
         self.assertNotIn(prompt_to_remove, self.dp.prompts)
 
+    def test_search_prompt(self):
+        prompts_file = "test_prompts.csv"
+        daily_prompt = DailyPrompt(prompts_file)
+
+        # Test search for "time"
+        expected_result = [
+            'Write about a time when you overcame a fear.',
+            'Write about a time when you felt proud of yourself.',
+        ]
+        self.assertEqual(daily_prompt.search_prompt("time"), expected_result)
+
+        # Test search for "favorite"
+        expected_result = ['What was your favorite part of today?', 'What is your favorite book?']
+        self.assertEqual(daily_prompt.search_prompt("favorite"), expected_result)
+
+        # Test search for "dog" (not present in prompts)
+        expected_result = []
+        self.assertEqual(daily_prompt.search_prompt("dog"), expected_result)
+
 
 class TestDailyPromptIntegration(unittest.TestCase):
     def setUp(self):
         self.prompts_file = 'test_prompts.csv'
         self.prompts = ['What was your favorite part of today?', 'What are you grateful for today?']
         with open(self.prompts_file, 'w', newline='') as f:
             writer = csv.writer(f)
```

### Comparing `journalyze-0.1.0/journalyze.egg-info/PKG-INFO` & `journalyze-0.1.1/journalyze.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: journalyze
-Version: 0.1.0
+Version: 0.1.1
 Summary: A journaling prompt library
 Author-email: Johana De La Rosa <jed2192@columbia.edu>
 License: MIT License
         
         Copyright (c) 2023 Johana De La Rosa
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -42,43 +42,65 @@
 
 # Journalyze
 
 A Python library to facilitate the journinaling experience.
 
 ![GitHub](https://img.shields.io/badge/license-MIT-ff69b4)
 [![](https://img.shields.io/github/issues/jedlr/journalyze?color=ff69b4)](https://github.com/jedlr/journalyze/issues)
-
 [![Build Status](https://github.com/jedlr/journalyze/workflows/Build%20Status/badge.svg?branch=main)](https://github.com/jedlr/journalyze/actions?query=workflow%3A%22Build+Status%22)
 [![codecov](https://codecov.io/gh/jedlr/journalyze/branch/main/graph/badge.svg)](https://codecov.io/gh/jedlr/journalyze)
 [![PyPI](https://img.shields.io/pypi/v/journalyze)](https://pypi.org/project/journalyze/)
+[![Documentation Status](https://readthedocs.org/projects/journalyze/badge/?version=latest)](https://journalyze.readthedocs.io/en/latest/?badge=latest)
+[![Docs](https://img.shields.io/badge/documentation-gh%20pages-%23fffb03)](https://jedlr.github.io/journalyze/)
 
 ## Overview
 Journalyze:
 * Fetches journaling prompts 
 
 ## Installation
 ```
-pip install journalyze
+pip install --upgrade journalyze
 ```
 ## How to Use
-After installing the library, there are currently 3 functions available for use.
+```python
+from journalyze import *
+
+# Randomly select and return a prompt from the list of prompts in csv file
+get_prompt()
 
-Simply `import * from journalyze`, and then call any of the following functions:
+# Randomly select and return an easy/short prompt
+get_prompt_easy()
 
-**get_prompt()**
+# Randomly select a given number of prompts and return
+get_prompt_num()
 
-`getPrompt()` randomly selects a prompt from the list of prompts in csv file
+# Adds a new given prompt to the list of prompts in csv file
+add_prompt()
 
-**add_prompt()**
+# Removes a given prompt from the list of prompts in csv file
+remove_prompt()
 
-`add_prompt()` adds a new prompt to the list of prompts in csv file
+# Searches the list of prompts for a keyword and returns a list of prompts that contain the keyword.
+search_prompt()
+```
 
-**remove_prompt()**
+## Example
+Running the following code
+```python
+import journalyze as dp
+
+dp = DailyPrompt('journalyze/prompts.csv')
+prompt = dp.get_prompt()
+print(prompt)
+```
+Outputs something like this to the console
+```
+Describe yourself using the first 10 words that come to mind. Then list 10 words that you’d like to use to describe yourself. List a few ways to transform those descriptions into reality.
+```
 
-`remove_prompt()` removes a prompt from the list of prompts in csv file
 
 ## Details
 This project is a pure python project using modern tooling. It uses a `Makefile` as a command registry, with the following commands:
 - `make`: list available commands
 - `make develop`: install and build this library and its dependencies using `pip`
 - `make build`: build the library using `setuptools`
 - `make lint`: perform static analysis of this library with `flake8` and `black`
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `journalyze-0.1.0/pyproject.toml` & `journalyze-0.1.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 build-backend="setuptools.build_meta"
 
 [project]
 name = "journalyze"
 authors = [{name = "Johana De La Rosa", email = "jed2192@columbia.edu"}]
 description="A journaling prompt library"
 readme = "README.md"
-version = "0.1.0"
+version = "0.1.1"
 requires-python = ">=3.7"
 
 dependencies = []
 
 classifiers = [
     "Development Status :: 2 - Pre-Alpha",
     "Programming Language :: Python :: Implementation :: CPython",
```

