# Comparing `tmp/bluesteam-0.0.5.tar.gz` & `tmp/bluesteam-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bluesteam-0.0.5.tar", last modified: Sat May 13 20:14:44 2023, max compression
+gzip compressed data, was "bluesteam-0.0.6.tar", last modified: Sat May 13 20:18:40 2023, max compression
```

## Comparing `bluesteam-0.0.5.tar` & `bluesteam-0.0.6.tar`

### file list

```diff
@@ -1,21 +1,32 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 20:14:44.522032 bluesteam-0.0.5/
--rw-rw-rw-   0        0        0     1166 2023-05-13 19:23:25.000000 bluesteam-0.0.5/LICENSE.txt
--rw-rw-rw-   0        0        0      673 2023-05-13 20:14:44.521035 bluesteam-0.0.5/PKG-INFO
--rw-rw-rw-   0        0        0      162 2023-05-13 19:30:04.000000 bluesteam-0.0.5/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 20:14:44.503793 bluesteam-0.0.5/bluesteam/
--rw-rw-rw-   0        0        0      593 2023-05-13 20:14:34.000000 bluesteam-0.0.5/bluesteam/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 20:14:44.513073 bluesteam-0.0.5/bluesteam/bluesteam_biorefineries/
--rw-rw-rw-   0        0        0      356 2023-05-13 19:50:40.000000 bluesteam-0.0.5/bluesteam/bluesteam_biorefineries/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 20:14:44.519050 bluesteam-0.0.5/bluesteam/separability_tools/
--rw-rw-rw-   0        0        0      448 2023-05-13 19:29:05.000000 bluesteam-0.0.5/bluesteam/separability_tools/__init__.py
--rw-rw-rw-   0        0        0     6526 2023-05-13 19:03:50.000000 bluesteam-0.0.5/bluesteam/separability_tools/bluesteam_separability_results_2022.9.23-12.42.xlsx
--rw-rw-rw-   0        0        0     3853 2023-05-13 19:51:49.000000 bluesteam-0.0.5/bluesteam/separability_tools/estimate_separability.py
--rw-rw-rw-   0        0        0    13845 2023-05-13 19:22:49.000000 bluesteam-0.0.5/bluesteam/separability_tools/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-13 20:14:44.511073 bluesteam-0.0.5/bluesteam.egg-info/
--rw-rw-rw-   0        0        0      673 2023-05-13 20:14:44.000000 bluesteam-0.0.5/bluesteam.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      476 2023-05-13 20:14:44.000000 bluesteam-0.0.5/bluesteam.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 20:14:44.000000 bluesteam-0.0.5/bluesteam.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2023-05-13 20:14:44.000000 bluesteam-0.0.5/bluesteam.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 20:14:44.000000 bluesteam-0.0.5/bluesteam.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 20:14:44.522032 bluesteam-0.0.5/setup.cfg
--rw-rw-rw-   0        0        0     1379 2023-05-13 20:14:27.000000 bluesteam-0.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:40.345144 bluesteam-0.0.6/
+-rw-rw-rw-   0        0        0     1166 2023-05-13 19:23:25.000000 bluesteam-0.0.6/LICENSE.txt
+-rw-rw-rw-   0        0        0      673 2023-05-13 20:18:40.345144 bluesteam-0.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0      162 2023-05-13 19:30:04.000000 bluesteam-0.0.6/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:40.312059 bluesteam-0.0.6/bluesteam/
+-rw-rw-rw-   0        0        0      593 2023-05-13 20:18:30.000000 bluesteam-0.0.6/bluesteam/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:40.320759 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/
+-rw-rw-rw-   0        0        0      356 2023-05-13 19:50:40.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:40.336200 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/
+-rw-rw-rw-   0        0        0     2459 2023-05-13 19:21:22.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/__init__.py
+-rw-rw-rw-   0        0        0    12447 2023-05-13 19:39:05.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/_bluestea.py
+-rw-rw-rw-   0        0        0     2352 2023-05-13 19:39:36.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/_chemicals.py
+-rw-rw-rw-   0        0        0     2497 2023-05-13 19:41:26.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/_process_settings.py
+-rw-rw-rw-   0        0        0    14560 2023-05-13 19:54:01.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/_system.py
+-rw-rw-rw-   0        0        0     4803 2023-05-13 19:40:04.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/_tea.py
+-rw-rw-rw-   0        0        0    13100 2023-05-13 19:40:14.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/example_runs.py
+-rw-rw-rw-   0        0        0     2569 2023-05-13 19:40:21.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/load_generic.py
+-rw-rw-rw-   0        0        0     7717 2023-05-13 19:40:39.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/units.py
+-rw-rw-rw-   0        0        0     3021 2023-05-13 19:41:06.000000 bluesteam-0.0.6/bluesteam/bluesteam_biorefineries/generic/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:40.343183 bluesteam-0.0.6/bluesteam/separability_tools/
+-rw-rw-rw-   0        0        0      448 2023-05-13 19:29:05.000000 bluesteam-0.0.6/bluesteam/separability_tools/__init__.py
+-rw-rw-rw-   0        0        0     6526 2023-05-13 19:03:50.000000 bluesteam-0.0.6/bluesteam/separability_tools/bluesteam_separability_results_2022.9.23-12.42.xlsx
+-rw-rw-rw-   0        0        0     3853 2023-05-13 19:51:49.000000 bluesteam-0.0.6/bluesteam/separability_tools/estimate_separability.py
+-rw-rw-rw-   0        0        0    13845 2023-05-13 19:22:49.000000 bluesteam-0.0.6/bluesteam/separability_tools/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 20:18:40.319762 bluesteam-0.0.6/bluesteam.egg-info/
+-rw-rw-rw-   0        0        0      673 2023-05-13 20:18:40.000000 bluesteam-0.0.6/bluesteam.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1025 2023-05-13 20:18:40.000000 bluesteam-0.0.6/bluesteam.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 20:18:40.000000 bluesteam-0.0.6/bluesteam.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-13 20:18:40.000000 bluesteam-0.0.6/bluesteam.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 20:18:40.000000 bluesteam-0.0.6/bluesteam.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 20:18:40.346140 bluesteam-0.0.6/setup.cfg
+-rw-rw-rw-   0        0        0     1424 2023-05-13 20:18:25.000000 bluesteam-0.0.6/setup.py
```

### Comparing `bluesteam-0.0.5/LICENSE.txt` & `bluesteam-0.0.6/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `bluesteam-0.0.5/PKG-INFO` & `bluesteam-0.0.6/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bluesteam
-Version: 0.0.5
+Version: 0.0.6
 Summary: Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.
 Home-page: https://github.com/BluestemBiosciences/bluesteam
 Author: Sarang S. Bhagwat
 Author-email: sarang.bhagwat.git@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
```

### Comparing `bluesteam-0.0.5/bluesteam/__init__.py` & `bluesteam-0.0.6/bluesteam/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # 		       Yoel Cortes-Pena <yoelcortes@gmail.com>
 # 
 # This module is under the MIT open-source license. See 
 # github.com/BluestemBiosciences/bluesteam/LICENSE.txt
 # for license details.
 """
 """
-__version__ = '0.0.5'
+__version__ = '0.0.6'
 __author__ = 'Sarang S. Bhagwat'
 
 # %% Initialize Bluesteam
 
 from . import bluesteam_biorefineries, separability_tools
```

### Comparing `bluesteam-0.0.5/bluesteam/separability_tools/bluesteam_separability_results_2022.9.23-12.42.xlsx` & `bluesteam-0.0.6/bluesteam/separability_tools/bluesteam_separability_results_2022.9.23-12.42.xlsx`

 * *Files identical despite different names*

### Comparing `bluesteam-0.0.5/bluesteam/separability_tools/estimate_separability.py` & `bluesteam-0.0.6/bluesteam/separability_tools/estimate_separability.py`

 * *Files identical despite different names*

### Comparing `bluesteam-0.0.5/bluesteam/separability_tools/utils.py` & `bluesteam-0.0.6/bluesteam/separability_tools/utils.py`

 * *Files identical despite different names*

### Comparing `bluesteam-0.0.5/bluesteam.egg-info/PKG-INFO` & `bluesteam-0.0.6/bluesteam.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bluesteam
-Version: 0.0.5
+Version: 0.0.6
 Summary: Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.
 Home-page: https://github.com/BluestemBiosciences/bluesteam
 Author: Sarang S. Bhagwat
 Author-email: sarang.bhagwat.git@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
```

### Comparing `bluesteam-0.0.5/setup.py` & `bluesteam-0.0.6/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -10,27 +10,28 @@
 """
 
 from setuptools import setup
 
 setup(
     name='bluesteam',
     packages=['bluesteam'],
-    version='0.0.5',    
+    version='0.0.6',    
     description='Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.',
     url='https://github.com/BluestemBiosciences/bluesteam',
     author='Sarang S. Bhagwat',
     author_email='sarang.bhagwat.git@gmail.com',
     license='MIT',
     install_requires=[
                       'biorefineries==2.23.18',   
                       'autosynthesis==0.0.17',
                       ],
     package_data=
         {'bluesteam': ['bluesteam_biorefineries/*',
                       'separability_tools/*',
+		      'bluesteam_biorefineries/generic/*'
                       ]},
    
     classifiers=[
         'Development Status :: 3 - Alpha',
         'Intended Audience :: Science/Research',
         'License :: OSI Approved :: University of Illinois/NCSA Open Source License',  
         'Operating System :: Microsoft :: Windows',
```

