# Comparing `tmp/pypredictor-0.1.0.tar.gz` & `tmp/pypredictor-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pypredictor-0.1.0.tar", last modified: Sat May 13 12:48:57 2023, max compression
+gzip compressed data, was "pypredictor-0.1.1.tar", last modified: Sat May 13 12:56:25 2023, max compression
```

## Comparing `pypredictor-0.1.0.tar` & `pypredictor-0.1.1.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 12:48:57.728695 pypredictor-0.1.0/
--rw-rw-rw-   0        0        0    11542 2023-05-13 09:58:17.000000 pypredictor-0.1.0/LICENSE
--rw-rw-rw-   0        0        0     2631 2023-05-13 12:48:57.727728 pypredictor-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0     1853 2023-05-13 12:45:30.000000 pypredictor-0.1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 12:48:57.692278 pypredictor-0.1.0/pypredictor/
--rw-rw-rw-   0        0        0      131 2023-05-12 18:29:43.000000 pypredictor-0.1.0/pypredictor/__init__.py
--rw-rw-rw-   0        0        0      358 2023-05-12 18:47:38.000000 pypredictor-0.1.0/pypredictor/_exceptions.py
--rw-rw-rw-   0        0        0     1727 2023-05-13 09:29:24.000000 pypredictor-0.1.0/pypredictor/numgraph.py
--rw-rw-rw-   0        0        0     3565 2023-05-13 10:20:08.000000 pypredictor-0.1.0/pypredictor/numpredict.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:48:57.725703 pypredictor-0.1.0/pypredictor.egg-info/
--rw-rw-rw-   0        0        0     2631 2023-05-13 12:48:57.000000 pypredictor-0.1.0/pypredictor.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      301 2023-05-13 12:48:57.000000 pypredictor-0.1.0/pypredictor.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 12:48:57.000000 pypredictor-0.1.0/pypredictor.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       43 2023-05-13 12:48:57.000000 pypredictor-0.1.0/pypredictor.egg-info/requires.txt
--rw-rw-rw-   0        0        0       12 2023-05-13 12:48:57.000000 pypredictor-0.1.0/pypredictor.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 12:48:57.728695 pypredictor-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0     2907 2023-05-13 12:46:44.000000 pypredictor-0.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:56:25.774906 pypredictor-0.1.1/
+-rw-rw-rw-   0        0        0    11542 2023-05-13 09:58:17.000000 pypredictor-0.1.1/LICENSE
+-rw-rw-rw-   0        0        0     2631 2023-05-13 12:56:25.773906 pypredictor-0.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0     1859 2023-05-13 12:54:34.000000 pypredictor-0.1.1/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 12:56:25.747968 pypredictor-0.1.1/pypredictor/
+-rw-rw-rw-   0        0        0      155 2023-05-13 12:55:09.000000 pypredictor-0.1.1/pypredictor/__init__.py
+-rw-rw-rw-   0        0        0      358 2023-05-13 12:54:52.000000 pypredictor-0.1.1/pypredictor/_exceptions.py
+-rw-rw-rw-   0        0        0     1741 2023-05-13 12:54:49.000000 pypredictor-0.1.1/pypredictor/numgraph.py
+-rw-rw-rw-   0        0        0     3572 2023-05-13 12:54:46.000000 pypredictor-0.1.1/pypredictor/numpredict.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:56:25.771941 pypredictor-0.1.1/pypredictor.egg-info/
+-rw-rw-rw-   0        0        0     2631 2023-05-13 12:56:25.000000 pypredictor-0.1.1/pypredictor.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      301 2023-05-13 12:56:25.000000 pypredictor-0.1.1/pypredictor.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 12:56:25.000000 pypredictor-0.1.1/pypredictor.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       43 2023-05-13 12:56:25.000000 pypredictor-0.1.1/pypredictor.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2023-05-13 12:56:25.000000 pypredictor-0.1.1/pypredictor.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 12:56:25.774906 pypredictor-0.1.1/setup.cfg
+-rw-rw-rw-   0        0        0     2907 2023-05-13 12:54:41.000000 pypredictor-0.1.1/setup.py
```

### Comparing `pypredictor-0.1.0/LICENSE` & `pypredictor-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `pypredictor-0.1.0/PKG-INFO` & `pypredictor-0.1.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pypredictor
-Version: 0.1.0
+Version: 0.1.1
 Summary: The Python library that makes AI predictions simple.
 Home-page: UNKNOWN
 Author: codingboy_CW (Hamd Waseem)
 Author-email: codingboy.cw@gmail.com
 License: Apache-2.0
 Keywords: python,prediction,ai
 Platform: UNKNOWN
```

### Comparing `pypredictor-0.1.0/README.md` & `pypredictor-0.1.1/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 <div align="center">
   <picture>
     <source media="(prefers-color-scheme: dark)" srcset="https://github.com/hamdivazim/pypredictor/raw/main/logo_dark.png">
     <img src="https://github.com/hamdivazim/pypredictor/raw/main/logo.png" alt="pypredictor logo">
   </picture>
 </div>
 
-# pypredictor
+# pypredictor 0.1.1
 <p>
   <img src="https://img.shields.io/badge/Python-3.8 | 3.9 | 3.10 | 3.11 -blue.svg" alt="py versions">
   <img src="https://img.shields.io/badge/PyPi package-0.1.0-green.svg" alt="pypi version">
   <img src="https://img.shields.io/badge/License-Apache License 2.0-green.svg" alt="license">
   <img src="https://img.shields.io/badge/Libraries-tensorflow | numpy | seaborn | pandas-green.svg" alt="libs">
 </p>
```

### Comparing `pypredictor-0.1.0/pypredictor/numgraph.py` & `pypredictor-0.1.1/pypredictor/numgraph.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 """
-pypredictor 0.1.0
+pypredictor 0.1.1
 
 © Hamd Waseem under the Apache Licence 2.0
 
 numgraph.py - Using `NumPredictor`, generates a seaborn plot.
 """
 
 import pandas as pd
 import matplotlib.pyplot as plt
 import seaborn as sns
-import numpredict
-import _exceptions
+from . import numpredict
+from . import _exceptions
 
 class NumGraph:
     """ Base class for generating seaborn plots. """
 
     def __init__(self, data=[]):
         self.set_data(data)
```

### Comparing `pypredictor-0.1.0/pypredictor/numpredict.py` & `pypredictor-0.1.1/pypredictor/numpredict.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 """
-pypredictor 0.1.0
+pypredictor 0.1.1
 
 © Hamd Waseem under the Apache Licence 2.0
 
 numpredict.py - Predicts the next n numbers in a list.
 """
 
 import logging
 import numpy as np
 import pandas as pd
-import _exceptions
+from . import _exceptions
 from tensorflow.keras.models import Sequential
 from tensorflow.keras.layers import Dense, LSTM
 
 class NumPredictor:
     """ Base NumPredictor class that generates the next values in a list. """
 
     def __init__(self, epochs=500):
```

### Comparing `pypredictor-0.1.0/pypredictor.egg-info/PKG-INFO` & `pypredictor-0.1.1/pypredictor.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pypredictor
-Version: 0.1.0
+Version: 0.1.1
 Summary: The Python library that makes AI predictions simple.
 Home-page: UNKNOWN
 Author: codingboy_CW (Hamd Waseem)
 Author-email: codingboy.cw@gmail.com
 License: Apache-2.0
 Keywords: python,prediction,ai
 Platform: UNKNOWN
```

### Comparing `pypredictor-0.1.0/setup.py` & `pypredictor-0.1.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '0.1.0'
+VERSION = '0.1.1'
 DESCRIPTION = 'The Python library that makes AI predictions simple.'
 LONG_DESCRIPTION = """
 <div align="center">
   <picture>
     <source media="(prefers-color-scheme: dark)" srcset="https://github.com/hamdivazim/pypredictor/raw/main/logo_dark.png">
     <img src="https://github.com/hamdivazim/pypredictor/raw/main/logo.png" alt="pypredictor logo">
   </picture>
```

