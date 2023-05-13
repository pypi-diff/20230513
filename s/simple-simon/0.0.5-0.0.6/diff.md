# Comparing `tmp/simple-simon-0.0.5.tar.gz` & `tmp/simple-simon-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simple-simon-0.0.5.tar", last modified: Sat May 13 15:01:28 2023, max compression
+gzip compressed data, was "simple-simon-0.0.6.tar", last modified: Sat May 13 15:24:24 2023, max compression
```

## Comparing `simple-simon-0.0.5.tar` & `simple-simon-0.0.6.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 15:01:28.194393 simple-simon-0.0.5/
--rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simple-simon-0.0.5/LICENSE
--rw-rw-rw-   0        0        0     5838 2023-05-13 15:01:28.194393 simple-simon-0.0.5/PKG-INFO
--rw-rw-rw-   0        0        0     5534 2023-05-13 15:00:05.000000 simple-simon-0.0.5/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 15:01:28.194393 simple-simon-0.0.5/setup.cfg
--rw-rw-rw-   0        0        0     1239 2023-05-13 15:00:21.000000 simple-simon-0.0.5/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:01:28.194393 simple-simon-0.0.5/simon/
--rw-rw-rw-   0        0        0    29858 2023-05-13 14:45:40.000000 simple-simon-0.0.5/simon/simon.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:01:28.194393 simple-simon-0.0.5/simon/simple_simon.egg-info/
--rw-rw-rw-   0        0        0     5838 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      250 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       11 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 15:24:24.168151 simple-simon-0.0.6/
+-rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simple-simon-0.0.6/LICENSE
+-rw-rw-rw-   0        0        0     5828 2023-05-13 15:24:24.168151 simple-simon-0.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0     5524 2023-05-13 15:22:21.000000 simple-simon-0.0.6/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 15:24:24.168151 simple-simon-0.0.6/setup.cfg
+-rw-rw-rw-   0        0        0     1239 2023-05-13 15:24:14.000000 simple-simon-0.0.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:24:24.152558 simple-simon-0.0.6/simon/
+-rw-rw-rw-   0        0        0    29858 2023-05-13 14:45:40.000000 simple-simon-0.0.6/simon/simon.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:24:24.168151 simple-simon-0.0.6/simon/simple_simon.egg-info/
+-rw-rw-rw-   0        0        0     5828 2023-05-13 15:24:24.000000 simple-simon-0.0.6/simon/simple_simon.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      250 2023-05-13 15:24:24.000000 simple-simon-0.0.6/simon/simple_simon.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 15:24:24.000000 simple-simon-0.0.6/simon/simple_simon.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 15:24:24.000000 simple-simon-0.0.6/simon/simple_simon.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        6 2023-05-13 15:24:24.000000 simple-simon-0.0.6/simon/simple_simon.egg-info/top_level.txt
```

### Comparing `simple-simon-0.0.5/LICENSE` & `simple-simon-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `simple-simon-0.0.5/PKG-INFO` & `simple-simon-0.0.6/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: simple-simon
-Version: 0.0.5
+Version: 0.0.6
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-![Logo](https://github.com/roiezemel/simon/blob/main/assets/simon_expanded_logo.png?raw=true)
+![Logo](https://github.com/roiezemel/simon/raw/main/assets/simon_expanded_logo.png)
 
 # A simple monitor for simulations and other processes
 
 ## Overview
 This project provides a simple tool for tracking simulations and 
 other numeric processes. It provides a Monitor class that has 
 all the following functionality:
```

### Comparing `simple-simon-0.0.5/README.md` & `simple-simon-0.0.6/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-![Logo](https://github.com/roiezemel/simon/blob/main/assets/simon_expanded_logo.png?raw=true)
+![Logo](https://github.com/roiezemel/simon/raw/main/assets/simon_expanded_logo.png)
 
 # A simple monitor for simulations and other processes
 
 ## Overview
 This project provides a simple tool for tracking simulations and 
 other numeric processes. It provides a Monitor class that has 
 all the following functionality:
```

### Comparing `simple-simon-0.0.5/setup.py` & `simple-simon-0.0.6/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="simple-simon",                           # This is the name of the package
-    version="0.0.5",                               # The initial release version
+    version="0.0.6",                               # The initial release version
     author="Roie Zemel",                           # Full name of the author
     description="A simple simulation monitor",
     long_description=long_description,             # Long description read from the the readme file
     long_description_content_type="text/markdown",
     packages=setuptools.find_packages(),           # List of all python modules to be installed
     classifiers=[
         "Programming Language :: Python :: 3",
```

### Comparing `simple-simon-0.0.5/simon/simon.py` & `simple-simon-0.0.6/simon/simon.py`

 * *Files identical despite different names*

### Comparing `simple-simon-0.0.5/simon/simple_simon.egg-info/PKG-INFO` & `simple-simon-0.0.6/simon/simple_simon.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: simple-simon
-Version: 0.0.5
+Version: 0.0.6
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-![Logo](https://github.com/roiezemel/simon/blob/main/assets/simon_expanded_logo.png?raw=true)
+![Logo](https://github.com/roiezemel/simon/raw/main/assets/simon_expanded_logo.png)
 
 # A simple monitor for simulations and other processes
 
 ## Overview
 This project provides a simple tool for tracking simulations and 
 other numeric processes. It provides a Monitor class that has 
 all the following functionality:
```

