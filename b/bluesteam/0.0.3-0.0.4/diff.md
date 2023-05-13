# Comparing `tmp/bluesteam-0.0.3.tar.gz` & `tmp/bluesteam-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bluesteam-0.0.3.tar", last modified: Sat May 13 19:58:24 2023, max compression
+gzip compressed data, was "bluesteam-0.0.4.tar", last modified: Sat May 13 20:10:35 2023, max compression
```

## Comparing `bluesteam-0.0.3.tar` & `bluesteam-0.0.4.tar`

### file list

```diff
@@ -1,14 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 19:58:24.809111 bluesteam-0.0.3/
--rw-rw-rw-   0        0        0     1166 2023-05-13 19:23:25.000000 bluesteam-0.0.3/LICENSE.txt
--rw-rw-rw-   0        0        0      673 2023-05-13 19:58:24.808130 bluesteam-0.0.3/PKG-INFO
--rw-rw-rw-   0        0        0      162 2023-05-13 19:30:04.000000 bluesteam-0.0.3/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 19:58:24.799137 bluesteam-0.0.3/bluesteam/
--rw-rw-rw-   0        0        0      593 2023-05-13 19:58:07.000000 bluesteam-0.0.3/bluesteam/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 19:58:24.806118 bluesteam-0.0.3/bluesteam.egg-info/
--rw-rw-rw-   0        0        0      673 2023-05-13 19:58:24.000000 bluesteam-0.0.3/bluesteam.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      216 2023-05-13 19:58:24.000000 bluesteam-0.0.3/bluesteam.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 19:58:24.000000 bluesteam-0.0.3/bluesteam.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2023-05-13 19:58:24.000000 bluesteam-0.0.3/bluesteam.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 19:58:24.000000 bluesteam-0.0.3/bluesteam.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 19:58:24.809111 bluesteam-0.0.3/setup.cfg
--rw-rw-rw-   0        0        0     1230 2023-05-13 19:58:15.000000 bluesteam-0.0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:10:35.486117 bluesteam-0.0.4/
+-rw-rw-rw-   0        0        0     1166 2023-05-13 19:23:25.000000 bluesteam-0.0.4/LICENSE.txt
+-rw-rw-rw-   0        0        0      673 2023-05-13 20:10:35.485097 bluesteam-0.0.4/PKG-INFO
+-rw-rw-rw-   0        0        0      162 2023-05-13 19:30:04.000000 bluesteam-0.0.4/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 20:10:35.470146 bluesteam-0.0.4/bluesteam/
+-rw-rw-rw-   0        0        0      593 2023-05-13 20:07:37.000000 bluesteam-0.0.4/bluesteam/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:10:35.483139 bluesteam-0.0.4/bluesteam/separability_tools/
+-rw-rw-rw-   0        0        0      448 2023-05-13 19:29:05.000000 bluesteam-0.0.4/bluesteam/separability_tools/__init__.py
+-rw-rw-rw-   0        0        0     6526 2023-05-13 19:03:50.000000 bluesteam-0.0.4/bluesteam/separability_tools/bluesteam_separability_results_2022.9.23-12.42.xlsx
+-rw-rw-rw-   0        0        0     3853 2023-05-13 19:51:49.000000 bluesteam-0.0.4/bluesteam/separability_tools/estimate_separability.py
+-rw-rw-rw-   0        0        0    13845 2023-05-13 19:22:49.000000 bluesteam-0.0.4/bluesteam/separability_tools/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:10:35.477153 bluesteam-0.0.4/bluesteam.egg-info/
+-rw-rw-rw-   0        0        0      673 2023-05-13 20:10:35.000000 bluesteam-0.0.4/bluesteam.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      430 2023-05-13 20:10:35.000000 bluesteam-0.0.4/bluesteam.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 20:10:35.000000 bluesteam-0.0.4/bluesteam.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-13 20:10:35.000000 bluesteam-0.0.4/bluesteam.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 20:10:35.000000 bluesteam-0.0.4/bluesteam.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 20:10:35.487092 bluesteam-0.0.4/setup.cfg
+-rw-rw-rw-   0        0        0     1380 2023-05-13 20:10:08.000000 bluesteam-0.0.4/setup.py
```

### Comparing `bluesteam-0.0.3/LICENSE.txt` & `bluesteam-0.0.4/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `bluesteam-0.0.3/PKG-INFO` & `bluesteam-0.0.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bluesteam
-Version: 0.0.3
+Version: 0.0.4
 Summary: Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.
 Home-page: https://github.com/BluestemBiosciences/bluesteam
 Author: Sarang S. Bhagwat
 Author-email: sarang.bhagwat.git@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
```

### Comparing `bluesteam-0.0.3/bluesteam/__init__.py` & `bluesteam-0.0.4/bluesteam/__init__.py`

 * *Files 25% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # 		       Yoel Cortes-Pena <yoelcortes@gmail.com>
 # 
 # This module is under the MIT open-source license. See 
 # github.com/BluestemBiosciences/bluesteam/LICENSE.txt
 # for license details.
 """
 """
-__version__ = '0.0.3'
+__version__ = '0.0.4'
 __author__ = 'Sarang S. Bhagwat'
 
 # %% Initialize Bluesteam
 
 from . import bluesteam_biorefineries, separability_tools
```

### Comparing `bluesteam-0.0.3/bluesteam.egg-info/PKG-INFO` & `bluesteam-0.0.4/bluesteam.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bluesteam
-Version: 0.0.3
+Version: 0.0.4
 Summary: Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.
 Home-page: https://github.com/BluestemBiosciences/bluesteam
 Author: Sarang S. Bhagwat
 Author-email: sarang.bhagwat.git@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
```

### Comparing `bluesteam-0.0.3/setup.py` & `bluesteam-0.0.4/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -10,25 +10,29 @@
 """
 
 from setuptools import setup
 
 setup(
     name='bluesteam',
     packages=['bluesteam'],
-    version='0.0.3',    
+    version='0.0.4',    
     description='Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.',
     url='https://github.com/BluestemBiosciences/bluesteam',
     author='Sarang S. Bhagwat',
     author_email='sarang.bhagwat.git@gmail.com',
     license='MIT',
     install_requires=[
                       'biorefineries==2.23.18',   
                       'autosynthesis==0.0.17',
                       ],
-
+    package_data=
+        {'bluesteam': ['bluesteam_biorefineriest/*',
+                      'separability_tools/*',
+                      ]},
+   
     classifiers=[
         'Development Status :: 3 - Alpha',
         'Intended Audience :: Science/Research',
         'License :: OSI Approved :: University of Illinois/NCSA Open Source License',  
         'Operating System :: Microsoft :: Windows',        
         'Programming Language :: Python :: 3.9'
     ],
```

