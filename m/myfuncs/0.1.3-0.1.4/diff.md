# Comparing `tmp/myfuncs-0.1.3.tar.gz` & `tmp/myfuncs-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "myfuncs-0.1.3.tar", last modified: Sat May 13 19:54:05 2023, max compression
+gzip compressed data, was "myfuncs-0.1.4.tar", last modified: Sat May 13 21:11:12 2023, max compression
```

## Comparing `myfuncs-0.1.3.tar` & `myfuncs-0.1.4.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 19:54:05.931965 myfuncs-0.1.3/
--rw-r--r--   0 work       (501) staff       (20)     1068 2023-05-13 16:42:37.000000 myfuncs-0.1.3/LICENSE
--rw-r--r--   0 work       (501) staff       (20)     2554 2023-05-13 19:54:05.931830 myfuncs-0.1.3/PKG-INFO
--rw-r--r--   0 work       (501) staff       (20)     1815 2023-05-13 19:51:48.000000 myfuncs-0.1.3/README.md
-drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 19:54:05.931012 myfuncs-0.1.3/myfuncs/
--rw-r--r--   0 work       (501) staff       (20)       21 2023-05-13 18:23:34.000000 myfuncs-0.1.3/myfuncs/__init__.py
--rw-r--r--   0 work       (501) staff       (20)     3349 2023-05-13 19:26:19.000000 myfuncs-0.1.3/myfuncs/funcs.py
-drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 19:54:05.931650 myfuncs-0.1.3/myfuncs.egg-info/
--rw-r--r--   0 work       (501) staff       (20)     2554 2023-05-13 19:54:05.000000 myfuncs-0.1.3/myfuncs.egg-info/PKG-INFO
--rw-r--r--   0 work       (501) staff       (20)      187 2023-05-13 19:54:05.000000 myfuncs-0.1.3/myfuncs.egg-info/SOURCES.txt
--rw-r--r--   0 work       (501) staff       (20)        1 2023-05-13 19:54:05.000000 myfuncs-0.1.3/myfuncs.egg-info/dependency_links.txt
--rw-r--r--   0 work       (501) staff       (20)        8 2023-05-13 19:54:05.000000 myfuncs-0.1.3/myfuncs.egg-info/top_level.txt
--rw-r--r--   0 work       (501) staff       (20)       38 2023-05-13 19:54:05.932011 myfuncs-0.1.3/setup.cfg
--rw-r--r--   0 work       (501) staff       (20)      916 2023-05-13 19:52:03.000000 myfuncs-0.1.3/setup.py
+drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 21:11:12.466416 myfuncs-0.1.4/
+-rw-r--r--   0 work       (501) staff       (20)     1068 2023-05-13 16:42:37.000000 myfuncs-0.1.4/LICENSE
+-rw-r--r--   0 work       (501) staff       (20)     2426 2023-05-13 21:11:12.466290 myfuncs-0.1.4/PKG-INFO
+-rw-r--r--   0 work       (501) staff       (20)     1687 2023-05-13 21:07:45.000000 myfuncs-0.1.4/README.md
+drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 21:11:12.465480 myfuncs-0.1.4/myfuncs/
+-rw-r--r--   0 work       (501) staff       (20)       21 2023-05-13 18:23:34.000000 myfuncs-0.1.4/myfuncs/__init__.py
+-rw-r--r--   0 work       (501) staff       (20)     3349 2023-05-13 19:26:19.000000 myfuncs-0.1.4/myfuncs/funcs.py
+drwxr-xr-x   0 work       (501) staff       (20)        0 2023-05-13 21:11:12.466129 myfuncs-0.1.4/myfuncs.egg-info/
+-rw-r--r--   0 work       (501) staff       (20)     2426 2023-05-13 21:11:12.000000 myfuncs-0.1.4/myfuncs.egg-info/PKG-INFO
+-rw-r--r--   0 work       (501) staff       (20)      187 2023-05-13 21:11:12.000000 myfuncs-0.1.4/myfuncs.egg-info/SOURCES.txt
+-rw-r--r--   0 work       (501) staff       (20)        1 2023-05-13 21:11:12.000000 myfuncs-0.1.4/myfuncs.egg-info/dependency_links.txt
+-rw-r--r--   0 work       (501) staff       (20)        8 2023-05-13 21:11:12.000000 myfuncs-0.1.4/myfuncs.egg-info/top_level.txt
+-rw-r--r--   0 work       (501) staff       (20)       38 2023-05-13 21:11:12.466457 myfuncs-0.1.4/setup.cfg
+-rw-r--r--   0 work       (501) staff       (20)      916 2023-05-13 21:09:15.000000 myfuncs-0.1.4/setup.py
```

### Comparing `myfuncs-0.1.3/LICENSE` & `myfuncs-0.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `myfuncs-0.1.3/PKG-INFO` & `myfuncs-0.1.4/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: myfuncs
-Version: 0.1.3
+Version: 0.1.4
 Summary: Personal utility functions that I use across different codebases.
 Home-page: https://github.com/cc-d/myfuncs
 Author: Cary Carter
 Author-email: ccarterdev@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
@@ -16,15 +16,15 @@
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # myfuncs
 
-This Python package, `myfuncs`, is a collection of personal utility functions created by Cary Carter. It is primarily intended for Cary's personal use, providing easy access to frequently used functions across different projects and systems.
+This Python package, `myfuncs`, is a collection of personal utility functions created by myself. It is primarily intended for my personal use, providing easy access to frequently used functions across different projects and systems.
 
 ## Installation
 
 You can install the package via pip:
 
 ```bash
 pip install myfuncs
@@ -92,9 +92,7 @@
 OK
 
 ```
 
 This output indicates that all the tests have passed.
 
 ---
-
-With these updates, the `README.md` file now includes information on how to run the tests for your `myfuncs` package.
```

### Comparing `myfuncs-0.1.3/README.md` & `myfuncs-0.1.4/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # myfuncs
 
-This Python package, `myfuncs`, is a collection of personal utility functions created by Cary Carter. It is primarily intended for Cary's personal use, providing easy access to frequently used functions across different projects and systems.
+This Python package, `myfuncs`, is a collection of personal utility functions created by myself. It is primarily intended for my personal use, providing easy access to frequently used functions across different projects and systems.
 
 ## Installation
 
 You can install the package via pip:
 
 ```bash
 pip install myfuncs
@@ -71,10 +71,8 @@
 
 OK
 
 ```
 
 This output indicates that all the tests have passed.
 
----
-
-With these updates, the `README.md` file now includes information on how to run the tests for your `myfuncs` package.
+---
```

### Comparing `myfuncs-0.1.3/myfuncs/funcs.py` & `myfuncs-0.1.4/myfuncs/funcs.py`

 * *Files identical despite different names*

### Comparing `myfuncs-0.1.3/myfuncs.egg-info/PKG-INFO` & `myfuncs-0.1.4/myfuncs.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: myfuncs
-Version: 0.1.3
+Version: 0.1.4
 Summary: Personal utility functions that I use across different codebases.
 Home-page: https://github.com/cc-d/myfuncs
 Author: Cary Carter
 Author-email: ccarterdev@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
@@ -16,15 +16,15 @@
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # myfuncs
 
-This Python package, `myfuncs`, is a collection of personal utility functions created by Cary Carter. It is primarily intended for Cary's personal use, providing easy access to frequently used functions across different projects and systems.
+This Python package, `myfuncs`, is a collection of personal utility functions created by myself. It is primarily intended for my personal use, providing easy access to frequently used functions across different projects and systems.
 
 ## Installation
 
 You can install the package via pip:
 
 ```bash
 pip install myfuncs
@@ -92,9 +92,7 @@
 OK
 
 ```
 
 This output indicates that all the tests have passed.
 
 ---
-
-With these updates, the `README.md` file now includes information on how to run the tests for your `myfuncs` package.
```

### Comparing `myfuncs-0.1.3/setup.py` & `myfuncs-0.1.4/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='myfuncs',
-    version='0.1.3',
+    version='0.1.4',
     packages=find_packages(),
     install_requires=[],
     author='Cary Carter',
     author_email='ccarterdev@gmail.com',
     description='Personal utility functions that I use across different codebases.',
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
```

