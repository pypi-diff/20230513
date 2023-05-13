# Comparing `tmp/checkify-0.4.tar.gz` & `tmp/checkify-0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "checkify-0.4.tar", last modified: Sat May 13 14:31:07 2023, max compression
+gzip compressed data, was "checkify-0.5.tar", last modified: Sat May 13 14:43:23 2023, max compression
```

## Comparing `checkify-0.4.tar` & `checkify-0.5.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:31:07.478750 checkify-0.4/
--rw-rw-rw-   0        0        0     1101 2023-05-13 13:47:43.000000 checkify-0.4/LICENSE
--rw-rw-rw-   0        0        0     1143 2023-05-13 14:31:07.476752 checkify-0.4/PKG-INFO
--rw-rw-rw-   0        0        0      587 2023-05-13 14:30:49.000000 checkify-0.4/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 14:31:07.430730 checkify-0.4/checkify/
--rw-rw-rw-   0        0        0        0 2023-05-13 13:57:56.000000 checkify-0.4/checkify/__init__.py
--rw-rw-rw-   0        0        0      798 2023-05-13 14:10:02.000000 checkify-0.4/checkify/code_checker.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:31:07.473764 checkify-0.4/checkify.egg-info/
--rw-rw-rw-   0        0        0     1143 2023-05-13 14:31:06.000000 checkify-0.4/checkify.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      231 2023-05-13 14:31:07.000000 checkify-0.4/checkify.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:31:06.000000 checkify-0.4/checkify.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        7 2023-05-13 14:31:06.000000 checkify-0.4/checkify.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-05-13 14:31:06.000000 checkify-0.4/checkify.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 14:31:07.478750 checkify-0.4/setup.cfg
--rw-rw-rw-   0        0        0     1053 2023-05-13 14:30:58.000000 checkify-0.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:43:23.709805 checkify-0.5/
+-rw-rw-rw-   0        0        0     1101 2023-05-13 13:47:43.000000 checkify-0.5/LICENSE
+-rw-rw-rw-   0        0        0     1143 2023-05-13 14:43:23.707800 checkify-0.5/PKG-INFO
+-rw-rw-rw-   0        0        0      587 2023-05-13 14:30:49.000000 checkify-0.5/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 14:43:23.671795 checkify-0.5/checkify/
+-rw-rw-rw-   0        0        0        0 2023-05-13 13:57:56.000000 checkify-0.5/checkify/__init__.py
+-rw-rw-rw-   0        0        0      792 2023-05-13 14:43:08.000000 checkify-0.5/checkify/code_checker.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:43:23.704794 checkify-0.5/checkify.egg-info/
+-rw-rw-rw-   0        0        0     1143 2023-05-13 14:43:23.000000 checkify-0.5/checkify.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      231 2023-05-13 14:43:23.000000 checkify-0.5/checkify.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:43:23.000000 checkify-0.5/checkify.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 14:43:23.000000 checkify-0.5/checkify.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 14:43:23.000000 checkify-0.5/checkify.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:43:23.709805 checkify-0.5/setup.cfg
+-rw-rw-rw-   0        0        0     1053 2023-05-13 14:43:16.000000 checkify-0.5/setup.py
```

### Comparing `checkify-0.4/LICENSE` & `checkify-0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `checkify-0.4/PKG-INFO` & `checkify-0.5/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: checkify
-Version: 0.4
+Version: 0.5
 Summary: Python package that utilizes the GPT API to check for errors in code and explain the code.
 Home-page: https://github.com/aditya0072001/checkify
 Author: Tripathi Aditya Prakash
 Project-URL: Download Statistics, https://pepy.tech/project/checkify/month
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `checkify-0.4/README.md` & `checkify-0.5/README.md`

 * *Files identical despite different names*

### Comparing `checkify-0.4/checkify/code_checker.py` & `checkify-0.5/checkify/code_checker.py`

 * *Files 2% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
 def check_code(code):
     # Set up the GPT API credentials
     openai.api_key = api_key
 
     # Call the GPT API to check the code and get the response
     response = openai.Completion.create(
-        engine='davinci-codex',
+        engine='davinci',
         prompt=code,
         max_tokens=100,
         n=1,
         stop=None,
         temperature=0.8,
         top_p=1,
         frequency_penalty=0,
```

### Comparing `checkify-0.4/checkify.egg-info/PKG-INFO` & `checkify-0.5/checkify.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: checkify
-Version: 0.4
+Version: 0.5
 Summary: Python package that utilizes the GPT API to check for errors in code and explain the code.
 Home-page: https://github.com/aditya0072001/checkify
 Author: Tripathi Aditya Prakash
 Project-URL: Download Statistics, https://pepy.tech/project/checkify/month
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `checkify-0.4/setup.py` & `checkify-0.5/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup
 
 with open('README.md', 'r', encoding='utf-8') as f:
     long_description = f.read()
 
 setup(
     name='checkify',
-    version='0.4',
+    version='0.5',
     packages=['checkify'],
     install_requires=[
         'openai'
     ],
     author="Tripathi Aditya Prakash",                     # Full name of the author
     description="Python package that utilizes the GPT API to check for errors in code and explain the code.",
     long_description=long_description,
```

