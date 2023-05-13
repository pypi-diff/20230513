# Comparing `tmp/pyPLNmodels-0.0.8.tar.gz` & `tmp/pyPLNmodels-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyPLNmodels-0.0.8.tar", last modified: Wed Feb  1 11:47:44 2023, max compression
+gzip compressed data, was "pyPLNmodels-0.0.9.tar", last modified: Wed Feb  1 14:12:40 2023, max compression
```

## Comparing `pyPLNmodels-0.0.8.tar` & `pyPLNmodels-0.0.9.tar`

### file list

```diff
@@ -1,30 +1,30 @@
-drwxrwxr-x   0 bastien   (1001) bastien   (1001)        0 2023-02-01 11:47:44.119625 pyPLNmodels-0.0.8/
--rw-rw-r--   0 bastien   (1001) bastien   (1001)     1058 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/LICENSE.txt
--rw-rw-r--   0 bastien   (1001) bastien   (1001)       74 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/MANIFEST.in
--rw-rw-r--   0 bastien   (1001) bastien   (1001)    16997 2023-02-01 11:47:44.119625 pyPLNmodels-0.0.8/PKG-INFO
--rw-rw-r--   0 bastien   (1001) bastien   (1001)    16540 2023-02-01 11:41:31.000000 pyPLNmodels-0.0.8/README.md
-drwxrwxr-x   0 bastien   (1001) bastien   (1001)        0 2023-02-01 11:47:44.115625 pyPLNmodels-0.0.8/images/
--rw-rw-r--   0 bastien   (1001) bastien   (1001)    55113 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/images/Comparison_GT_2algs_n=1000,p=10000,q=10.png
--rw-rw-r--   0 bastien   (1001) bastien   (1001)   198478 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/images/Comparison_GT_algs.png
--rw-rw-r--   0 bastien   (1001) bastien   (1001)    13620 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/images/Comparison_fastPLN_vs_fastPLNPCA_n=1000.png
--rw-rw-r--   0 bastien   (1001) bastien   (1001)    12739 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/images/Comparison_fastPLN_vs_fastPLNPCA_p=1000.png
--rw-rw-r--   0 bastien   (1001) bastien   (1001)    42242 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/images/ELBOvslikelihood.png
--rw-rw-r--   0 bastien   (1001) bastien   (1001)   125453 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/images/IMPS_screenshot.png
--rw-rw-r--   0 bastien   (1001) bastien   (1001)   136582 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/images/fastPLNPCA_screenshot.png
--rw-rw-r--   0 bastien   (1001) bastien   (1001)   125653 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.8/images/fastPLN_screenshot.png
-drwxrwxr-x   0 bastien   (1001) bastien   (1001)        0 2023-02-01 11:47:44.115625 pyPLNmodels-0.0.8/pyPLNmodels/
--rw-rw-r--   0 bastien   (1001) bastien   (1001)     9948 2023-02-01 11:19:30.000000 pyPLNmodels-0.0.8/pyPLNmodels/VEM.py
--rw-rw-r--   0 bastien   (1001) bastien   (1001)       24 2023-02-01 09:13:32.000000 pyPLNmodels-0.0.8/pyPLNmodels/__init__.py
--rw-rw-r--   0 bastien   (1001) bastien   (1001)      796 2023-02-01 08:57:24.000000 pyPLNmodels-0.0.8/pyPLNmodels/closedForms.py
--rw-rw-r--   0 bastien   (1001) bastien   (1001)     3101 2023-02-01 10:05:21.000000 pyPLNmodels-0.0.8/pyPLNmodels/elbos.py
--rw-rw-r--   0 bastien   (1001) bastien   (1001)      603 2023-02-01 11:42:25.000000 pyPLNmodels-0.0.8/pyPLNmodels/test.py
--rw-rw-r--   0 bastien   (1001) bastien   (1001)    14176 2023-02-01 10:52:00.000000 pyPLNmodels-0.0.8/pyPLNmodels/utils.py
-drwxrwxr-x   0 bastien   (1001) bastien   (1001)        0 2023-02-01 11:47:44.115625 pyPLNmodels-0.0.8/pyPLNmodels.egg-info/
--rw-rw-r--   0 bastien   (1001) bastien   (1001)    16997 2023-02-01 11:47:43.000000 pyPLNmodels-0.0.8/pyPLNmodels.egg-info/PKG-INFO
--rw-rw-r--   0 bastien   (1001) bastien   (1001)      666 2023-02-01 11:47:44.000000 pyPLNmodels-0.0.8/pyPLNmodels.egg-info/SOURCES.txt
--rw-rw-r--   0 bastien   (1001) bastien   (1001)        1 2023-02-01 11:47:43.000000 pyPLNmodels-0.0.8/pyPLNmodels.egg-info/dependency_links.txt
--rw-rw-r--   0 bastien   (1001) bastien   (1001)      292 2023-02-01 11:47:43.000000 pyPLNmodels-0.0.8/pyPLNmodels.egg-info/requires.txt
--rw-rw-r--   0 bastien   (1001) bastien   (1001)       81 2023-02-01 11:47:43.000000 pyPLNmodels-0.0.8/pyPLNmodels.egg-info/top_level.txt
--rw-rw-r--   0 bastien   (1001) bastien   (1001)      292 2023-02-01 11:24:53.000000 pyPLNmodels-0.0.8/requirements.txt
--rw-rw-r--   0 bastien   (1001) bastien   (1001)       38 2023-02-01 11:47:44.119625 pyPLNmodels-0.0.8/setup.cfg
--rw-rw-r--   0 bastien   (1001) bastien   (1001)      941 2023-02-01 11:45:28.000000 pyPLNmodels-0.0.8/setup.py
+drwxrwxr-x   0 bastien   (1001) bastien   (1001)        0 2023-02-01 14:12:40.511260 pyPLNmodels-0.0.9/
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)     1058 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/LICENSE.txt
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)       74 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/MANIFEST.in
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)    16997 2023-02-01 14:12:40.507260 pyPLNmodels-0.0.9/PKG-INFO
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)    16540 2023-02-01 11:41:31.000000 pyPLNmodels-0.0.9/README.md
+drwxrwxr-x   0 bastien   (1001) bastien   (1001)        0 2023-02-01 14:12:40.507260 pyPLNmodels-0.0.9/images/
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)    55113 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/images/Comparison_GT_2algs_n=1000,p=10000,q=10.png
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)   198478 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/images/Comparison_GT_algs.png
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)    13620 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/images/Comparison_fastPLN_vs_fastPLNPCA_n=1000.png
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)    12739 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/images/Comparison_fastPLN_vs_fastPLNPCA_p=1000.png
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)    42242 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/images/ELBOvslikelihood.png
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)   125453 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/images/IMPS_screenshot.png
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)   136582 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/images/fastPLNPCA_screenshot.png
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)   125653 2022-04-26 07:42:45.000000 pyPLNmodels-0.0.9/images/fastPLN_screenshot.png
+drwxrwxr-x   0 bastien   (1001) bastien   (1001)        0 2023-02-01 14:12:40.507260 pyPLNmodels-0.0.9/pyPLNmodels/
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)     9948 2023-02-01 14:09:23.000000 pyPLNmodels-0.0.9/pyPLNmodels/VEM.py
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)       24 2023-02-01 14:11:11.000000 pyPLNmodels-0.0.9/pyPLNmodels/__init__.py
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)      796 2023-02-01 08:57:24.000000 pyPLNmodels-0.0.9/pyPLNmodels/closedForms.py
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)     3101 2023-02-01 10:05:21.000000 pyPLNmodels-0.0.9/pyPLNmodels/elbos.py
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)      603 2023-02-01 11:42:25.000000 pyPLNmodels-0.0.9/pyPLNmodels/test.py
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)    14176 2023-02-01 10:52:00.000000 pyPLNmodels-0.0.9/pyPLNmodels/utils.py
+drwxrwxr-x   0 bastien   (1001) bastien   (1001)        0 2023-02-01 14:12:40.507260 pyPLNmodels-0.0.9/pyPLNmodels.egg-info/
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)    16997 2023-02-01 14:12:40.000000 pyPLNmodels-0.0.9/pyPLNmodels.egg-info/PKG-INFO
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)      666 2023-02-01 14:12:40.000000 pyPLNmodels-0.0.9/pyPLNmodels.egg-info/SOURCES.txt
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)        1 2023-02-01 14:12:40.000000 pyPLNmodels-0.0.9/pyPLNmodels.egg-info/dependency_links.txt
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)      292 2023-02-01 14:12:40.000000 pyPLNmodels-0.0.9/pyPLNmodels.egg-info/requires.txt
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)       81 2023-02-01 14:12:40.000000 pyPLNmodels-0.0.9/pyPLNmodels.egg-info/top_level.txt
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)      292 2023-02-01 11:24:53.000000 pyPLNmodels-0.0.9/requirements.txt
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)       38 2023-02-01 14:12:40.511260 pyPLNmodels-0.0.9/setup.cfg
+-rw-rw-r--   0 bastien   (1001) bastien   (1001)      941 2023-02-01 11:45:28.000000 pyPLNmodels-0.0.9/setup.py
```

### Comparing `pyPLNmodels-0.0.8/LICENSE.txt` & `pyPLNmodels-0.0.9/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/PKG-INFO` & `pyPLNmodels-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyPLNmodels
-Version: 0.0.8
+Version: 0.0.9
 Summary: Package implementing PLN models
 Home-page: https://github.com/PLN-team/PLNpy/tree/master/pyPLNmodels
 Author: Bastien Batardière, Julien Chiquet, Joon Kwon
 Author-email: bastien.batardiere@gmail.com
 License: UNKNOWN
 Keywords: python,count,data,count data,high dimension,scRNAseq,PLN
 Platform: UNKNOWN
```

### Comparing `pyPLNmodels-0.0.8/README.md` & `pyPLNmodels-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/images/Comparison_GT_2algs_n=1000,p=10000,q=10.png` & `pyPLNmodels-0.0.9/images/Comparison_GT_2algs_n=1000,p=10000,q=10.png`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/images/Comparison_GT_algs.png` & `pyPLNmodels-0.0.9/images/Comparison_GT_algs.png`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/images/Comparison_fastPLN_vs_fastPLNPCA_n=1000.png` & `pyPLNmodels-0.0.9/images/Comparison_fastPLN_vs_fastPLNPCA_n=1000.png`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/images/Comparison_fastPLN_vs_fastPLNPCA_p=1000.png` & `pyPLNmodels-0.0.9/images/Comparison_fastPLN_vs_fastPLNPCA_p=1000.png`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/images/ELBOvslikelihood.png` & `pyPLNmodels-0.0.9/images/ELBOvslikelihood.png`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/images/IMPS_screenshot.png` & `pyPLNmodels-0.0.9/images/IMPS_screenshot.png`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/images/fastPLNPCA_screenshot.png` & `pyPLNmodels-0.0.9/images/fastPLNPCA_screenshot.png`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/images/fastPLN_screenshot.png` & `pyPLNmodels-0.0.9/images/fastPLN_screenshot.png`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/pyPLNmodels/VEM.py` & `pyPLNmodels-0.0.9/pyPLNmodels/VEM.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from elbos import ELBOnoPCA, ELBOPCA, ELBOZI
 from closedForms import closed_formula_beta, closed_formula_Sigma, closed_formula_pi
+from elbos import ELBOnoPCA, ELBOPCA, ELBOZI
 from abc import ABC, abstractmethod
 import torch
 import pandas as pd
 import numpy as np
 from utils import PLNPlotArgs , init_Sigma, init_C, init_beta, getOFromSumOfY
 import time
 import seaborn as sns
```

### Comparing `pyPLNmodels-0.0.8/pyPLNmodels/closedForms.py` & `pyPLNmodels-0.0.9/pyPLNmodels/closedForms.py`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/pyPLNmodels/elbos.py` & `pyPLNmodels-0.0.9/pyPLNmodels/elbos.py`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/pyPLNmodels/test.py` & `pyPLNmodels-0.0.9/pyPLNmodels/test.py`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/pyPLNmodels/utils.py` & `pyPLNmodels-0.0.9/pyPLNmodels/utils.py`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/pyPLNmodels.egg-info/PKG-INFO` & `pyPLNmodels-0.0.9/pyPLNmodels.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyPLNmodels
-Version: 0.0.8
+Version: 0.0.9
 Summary: Package implementing PLN models
 Home-page: https://github.com/PLN-team/PLNpy/tree/master/pyPLNmodels
 Author: Bastien Batardière, Julien Chiquet, Joon Kwon
 Author-email: bastien.batardiere@gmail.com
 License: UNKNOWN
 Keywords: python,count,data,count data,high dimension,scRNAseq,PLN
 Platform: UNKNOWN
```

### Comparing `pyPLNmodels-0.0.8/pyPLNmodels.egg-info/SOURCES.txt` & `pyPLNmodels-0.0.9/pyPLNmodels.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyPLNmodels-0.0.8/setup.py` & `pyPLNmodels-0.0.9/setup.py`

 * *Files identical despite different names*

