# Comparing `tmp/simple-simon-0.0.1.tar.gz` & `tmp/simple-simon-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simple-simon-0.0.1.tar", last modified: Sat May 13 14:24:05 2023, max compression
+gzip compressed data, was "simple-simon-0.0.2.tar", last modified: Sat May 13 14:28:58 2023, max compression
```

## Comparing `simple-simon-0.0.1.tar` & `simple-simon-0.0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:24:05.256562 simple-simon-0.0.1/
--rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simple-simon-0.0.1/LICENSE
--rw-rw-rw-   0        0        0     5849 2023-05-13 14:24:05.256519 simple-simon-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0     5545 2023-05-13 14:15:50.000000 simple-simon-0.0.1/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 14:24:05.256562 simple-simon-0.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1239 2023-05-13 14:24:02.000000 simple-simon-0.0.1/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:24:05.248562 simple-simon-0.0.1/simon/
--rw-rw-rw-   0        0        0    29618 2023-05-13 14:07:05.000000 simple-simon-0.0.1/simon/simon.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:24:05.255522 simple-simon-0.0.1/simon/simple_simon.egg-info/
--rw-rw-rw-   0        0        0     5849 2023-05-13 14:24:05.000000 simple-simon-0.0.1/simon/simple_simon.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      250 2023-05-13 14:24:05.000000 simple-simon-0.0.1/simon/simple_simon.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:24:05.000000 simple-simon-0.0.1/simon/simple_simon.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       11 2023-05-13 14:24:05.000000 simple-simon-0.0.1/simon/simple_simon.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2023-05-13 14:24:05.000000 simple-simon-0.0.1/simon/simple_simon.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 14:28:58.910947 simple-simon-0.0.2/
+-rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simple-simon-0.0.2/LICENSE
+-rw-rw-rw-   0        0        0     5856 2023-05-13 14:28:58.910947 simple-simon-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0     5552 2023-05-13 14:25:47.000000 simple-simon-0.0.2/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:28:58.910947 simple-simon-0.0.2/setup.cfg
+-rw-rw-rw-   0        0        0     1239 2023-05-13 14:28:35.000000 simple-simon-0.0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:28:58.910947 simple-simon-0.0.2/simon/
+-rw-rw-rw-   0        0        0    29618 2023-05-13 14:07:05.000000 simple-simon-0.0.2/simon/simon.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:28:58.910947 simple-simon-0.0.2/simon/simple_simon.egg-info/
+-rw-rw-rw-   0        0        0     5856 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      250 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        6 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/top_level.txt
```

### Comparing `simple-simon-0.0.1/LICENSE` & `simple-simon-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `simple-simon-0.0.1/PKG-INFO` & `simple-simon-0.0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-simon
-Version: 0.0.1
+Version: 0.0.2
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -28,15 +28,15 @@
   - A config file with configuration constants
   - A summary text file
 - Loading an output directory to continue working with a simulation that's been terminated.
 
 ## Installation
 Install with `pip`:
 ```commandline
-pip install simon
+pip install simple-simon
 ```
 
 ## Usage
 Here's a quick example of the `Monitor` class used to track a moving object simulation:
 
 ```python
 from simon.simon import Monitor
```

### Comparing `simple-simon-0.0.1/README.md` & `simple-simon-0.0.2/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -17,15 +17,15 @@
   - A config file with configuration constants
   - A summary text file
 - Loading an output directory to continue working with a simulation that's been terminated.
 
 ## Installation
 Install with `pip`:
 ```commandline
-pip install simon
+pip install simple-simon
 ```
 
 ## Usage
 Here's a quick example of the `Monitor` class used to track a moving object simulation:
 
 ```python
 from simon.simon import Monitor
```

### Comparing `simple-simon-0.0.1/setup.py` & `simple-simon-0.0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="simple-simon",                           # This is the name of the package
-    version="0.0.1",                               # The initial release version
+    version="0.0.2",                               # The initial release version
     author="Roie Zemel",                           # Full name of the author
     description="A simple simulation monitor",
     long_description=long_description,             # Long description read from the the readme file
     long_description_content_type="text/markdown",
     packages=setuptools.find_packages(),           # List of all python modules to be installed
     classifiers=[
         "Programming Language :: Python :: 3",
```

### Comparing `simple-simon-0.0.1/simon/simon.py` & `simple-simon-0.0.2/simon/simon.py`

 * *Files identical despite different names*

### Comparing `simple-simon-0.0.1/simon/simple_simon.egg-info/PKG-INFO` & `simple-simon-0.0.2/simon/simple_simon.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-simon
-Version: 0.0.1
+Version: 0.0.2
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -28,15 +28,15 @@
   - A config file with configuration constants
   - A summary text file
 - Loading an output directory to continue working with a simulation that's been terminated.
 
 ## Installation
 Install with `pip`:
 ```commandline
-pip install simon
+pip install simple-simon
 ```
 
 ## Usage
 Here's a quick example of the `Monitor` class used to track a moving object simulation:
 
 ```python
 from simon.simon import Monitor
```

