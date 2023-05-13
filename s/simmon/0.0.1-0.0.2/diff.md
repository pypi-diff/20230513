# Comparing `tmp/simmon-0.0.1.tar.gz` & `tmp/simmon-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simmon-0.0.1.tar", last modified: Sat May 13 17:42:14 2023, max compression
+gzip compressed data, was "simmon-0.0.2.tar", last modified: Sat May 13 17:50:22 2023, max compression
```

## Comparing `simmon-0.0.1.tar` & `simmon-0.0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 17:42:14.245702 simmon-0.0.1/
--rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simmon-0.0.1/LICENSE
--rw-rw-rw-   0        0        0     6044 2023-05-13 17:42:14.245702 simmon-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0     5746 2023-05-13 17:41:41.000000 simmon-0.0.1/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 17:42:14.245702 simmon-0.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1241 2023-05-13 17:42:13.000000 simmon-0.0.1/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 17:42:14.245702 simmon-0.0.1/simmon/
-drwxrwxrwx   0        0        0        0 2023-05-13 17:42:14.245702 simmon-0.0.1/simmon/simmon.egg-info/
--rw-rw-rw-   0        0        0     6044 2023-05-13 17:42:14.000000 simmon-0.0.1/simmon/simmon.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      227 2023-05-13 17:42:14.000000 simmon-0.0.1/simmon/simmon.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 17:42:14.000000 simmon-0.0.1/simmon/simmon.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       11 2023-05-13 17:42:14.000000 simmon-0.0.1/simmon/simmon.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-05-13 17:42:14.000000 simmon-0.0.1/simmon/simmon.egg-info/top_level.txt
--rw-rw-rw-   0        0        0    29858 2023-05-13 14:45:40.000000 simmon-0.0.1/simmon/simmon.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:50:22.074420 simmon-0.0.2/
+-rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simmon-0.0.2/LICENSE
+-rw-rw-rw-   0        0        0     6055 2023-05-13 17:50:22.074420 simmon-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0     5757 2023-05-13 17:49:08.000000 simmon-0.0.2/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 17:50:22.074420 simmon-0.0.2/setup.cfg
+-rw-rw-rw-   0        0        0     1241 2023-05-13 17:50:12.000000 simmon-0.0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:50:22.058811 simmon-0.0.2/simmon/
+drwxrwxrwx   0        0        0        0 2023-05-13 17:50:22.074420 simmon-0.0.2/simmon/simmon.egg-info/
+-rw-rw-rw-   0        0        0     6055 2023-05-13 17:50:21.000000 simmon-0.0.2/simmon/simmon.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      227 2023-05-13 17:50:21.000000 simmon-0.0.2/simmon/simmon.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 17:50:21.000000 simmon-0.0.2/simmon/simmon.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 17:50:21.000000 simmon-0.0.2/simmon/simmon.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 17:50:21.000000 simmon-0.0.2/simmon/simmon.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0    29858 2023-05-13 14:45:40.000000 simmon-0.0.2/simmon/simmon.py
```

### Comparing `simmon-0.0.1/LICENSE` & `simmon-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `simmon-0.0.1/PKG-INFO` & `simmon-0.0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: simmon
-Version: 0.0.1
+Version: 0.0.2
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-![Logo](https://github.com/roiezemel/simmon/raw/main/assets/simmon_expanded_logo.png)
+![Logo](https://raw.githubusercontent.com/roiezemel/simmon/main/assets/simmon_expanded_logo.png)
 
 [![PyPI version](https://badge.fury.io/py/simmon.svg)](https://badge.fury.io/py/simmon)
 [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://choosealicense.com/licenses/mit/)
 
 # A simple monitor for simulations and other numeric processes
 
 ## Overview
```

### Comparing `simmon-0.0.1/README.md` & `simmon-0.0.2/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-![Logo](https://github.com/roiezemel/simmon/raw/main/assets/simmon_expanded_logo.png)
+![Logo](https://raw.githubusercontent.com/roiezemel/simmon/main/assets/simmon_expanded_logo.png)
 
 [![PyPI version](https://badge.fury.io/py/simmon.svg)](https://badge.fury.io/py/simmon)
 [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://choosealicense.com/licenses/mit/)
 
 # A simple monitor for simulations and other numeric processes
 
 ## Overview
```

### Comparing `simmon-0.0.1/setup.py` & `simmon-0.0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="simmon",                                 # This is the name of the package
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

### Comparing `simmon-0.0.1/simmon/simmon.egg-info/PKG-INFO` & `simmon-0.0.2/simmon/simmon.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: simmon
-Version: 0.0.1
+Version: 0.0.2
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-![Logo](https://github.com/roiezemel/simmon/raw/main/assets/simmon_expanded_logo.png)
+![Logo](https://raw.githubusercontent.com/roiezemel/simmon/main/assets/simmon_expanded_logo.png)
 
 [![PyPI version](https://badge.fury.io/py/simmon.svg)](https://badge.fury.io/py/simmon)
 [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://choosealicense.com/licenses/mit/)
 
 # A simple monitor for simulations and other numeric processes
 
 ## Overview
```

### Comparing `simmon-0.0.1/simmon/simmon.py` & `simmon-0.0.2/simmon/simmon.py`

 * *Files identical despite different names*

