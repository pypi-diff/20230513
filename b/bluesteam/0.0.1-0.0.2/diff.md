# Comparing `tmp/bluesteam-0.0.1.tar.gz` & `tmp/bluesteam-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bluesteam-0.0.1.tar", last modified: Sat May 13 19:30:28 2023, max compression
+gzip compressed data, was "bluesteam-0.0.2.tar", last modified: Sat May 13 19:43:14 2023, max compression
```

## Comparing `bluesteam-0.0.1.tar` & `bluesteam-0.0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 19:30:28.402922 bluesteam-0.0.1/
--rw-rw-rw-   0        0        0     1166 2023-05-13 19:23:25.000000 bluesteam-0.0.1/LICENSE.txt
--rw-rw-rw-   0        0        0      673 2023-05-13 19:30:28.401917 bluesteam-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0      162 2023-05-13 19:30:04.000000 bluesteam-0.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 19:30:28.388951 bluesteam-0.0.1/bluesteam/
--rw-rw-rw-   0        0        0      567 2023-05-13 19:28:14.000000 bluesteam-0.0.1/bluesteam/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 19:30:28.399921 bluesteam-0.0.1/bluesteam.egg-info/
--rw-rw-rw-   0        0        0      673 2023-05-13 19:30:28.000000 bluesteam-0.0.1/bluesteam.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      216 2023-05-13 19:30:28.000000 bluesteam-0.0.1/bluesteam.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 19:30:28.000000 bluesteam-0.0.1/bluesteam.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2023-05-13 19:30:28.000000 bluesteam-0.0.1/bluesteam.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 19:30:28.000000 bluesteam-0.0.1/bluesteam.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 19:30:28.402922 bluesteam-0.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1230 2023-05-13 19:23:07.000000 bluesteam-0.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:43:14.919719 bluesteam-0.0.2/
+-rw-rw-rw-   0        0        0     1166 2023-05-13 19:23:25.000000 bluesteam-0.0.2/LICENSE.txt
+-rw-rw-rw-   0        0        0      673 2023-05-13 19:43:14.918732 bluesteam-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0      162 2023-05-13 19:30:04.000000 bluesteam-0.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 19:43:14.908562 bluesteam-0.0.2/bluesteam/
+-rw-rw-rw-   0        0        0      593 2023-05-13 19:42:36.000000 bluesteam-0.0.2/bluesteam/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:43:14.916727 bluesteam-0.0.2/bluesteam.egg-info/
+-rw-rw-rw-   0        0        0      673 2023-05-13 19:43:14.000000 bluesteam-0.0.2/bluesteam.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      216 2023-05-13 19:43:14.000000 bluesteam-0.0.2/bluesteam.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 19:43:14.000000 bluesteam-0.0.2/bluesteam.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-13 19:43:14.000000 bluesteam-0.0.2/bluesteam.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 19:43:14.000000 bluesteam-0.0.2/bluesteam.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 19:43:14.919719 bluesteam-0.0.2/setup.cfg
+-rw-rw-rw-   0        0        0     1230 2023-05-13 19:42:44.000000 bluesteam-0.0.2/setup.py
```

### Comparing `bluesteam-0.0.1/LICENSE.txt` & `bluesteam-0.0.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `bluesteam-0.0.1/PKG-INFO` & `bluesteam-0.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bluesteam
-Version: 0.0.1
+Version: 0.0.2
 Summary: Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.
 Home-page: https://github.com/BluestemBiosciences/bluesteam
 Author: Sarang S. Bhagwat
 Author-email: sarang.bhagwat.git@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
```

### Comparing `bluesteam-0.0.1/bluesteam.egg-info/PKG-INFO` & `bluesteam-0.0.2/bluesteam.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bluesteam
-Version: 0.0.1
+Version: 0.0.2
 Summary: Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.
 Home-page: https://github.com/BluestemBiosciences/bluesteam
 Author: Sarang S. Bhagwat
 Author-email: sarang.bhagwat.git@gmail.com
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
```

### Comparing `bluesteam-0.0.1/setup.py` & `bluesteam-0.0.2/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 """
 
 from setuptools import setup
 
 setup(
     name='bluesteam',
     packages=['bluesteam'],
-    version='0.0.1',    
+    version='0.0.2',    
     description='Bluestem leverages AutoSynthesis, BioSTEAM, and biorefineries in BioIndustrial-Park for automated process synthesis and design of biorefineries.',
     url='https://github.com/BluestemBiosciences/bluesteam',
     author='Sarang S. Bhagwat',
     author_email='sarang.bhagwat.git@gmail.com',
     license='MIT',
     install_requires=[
                       'biorefineries==2.23.18',
```

