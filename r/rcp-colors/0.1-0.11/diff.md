# Comparing `tmp/rcp-colors-0.1.tar.gz` & `tmp/rcp-colors-0.11.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rcp-colors-0.1.tar", last modified: Sat May 13 02:41:14 2023, max compression
+gzip compressed data, was "rcp-colors-0.11.tar", last modified: Sat May 13 02:50:25 2023, max compression
```

## Comparing `rcp-colors-0.1.tar` & `rcp-colors-0.11.tar`

### file list

```diff
@@ -1,11 +1,11 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 02:41:14.330803 rcp-colors-0.1/
--rw-rw-rw-   0        0        0      612 2023-05-13 02:41:14.329802 rcp-colors-0.1/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 02:41:14.327812 rcp-colors-0.1/rcp_colors.egg-info/
--rw-rw-rw-   0        0        0      612 2023-05-13 02:41:14.000000 rcp-colors-0.1/rcp_colors.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      214 2023-05-13 02:41:14.000000 rcp-colors-0.1/rcp_colors.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 02:41:14.000000 rcp-colors-0.1/rcp_colors.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       33 2023-05-13 02:41:14.000000 rcp-colors-0.1/rcp_colors.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       16 2023-05-13 02:41:14.000000 rcp-colors-0.1/rcp_colors.egg-info/requires.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 02:41:14.000000 rcp-colors-0.1/rcp_colors.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 02:41:14.330803 rcp-colors-0.1/setup.cfg
--rw-rw-rw-   0        0        0      980 2023-05-13 02:40:47.000000 rcp-colors-0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 02:50:25.716033 rcp-colors-0.11/
+-rw-rw-rw-   0        0        0      613 2023-05-13 02:50:25.715031 rcp-colors-0.11/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 02:50:25.713658 rcp-colors-0.11/rcp_colors.egg-info/
+-rw-rw-rw-   0        0        0      613 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      214 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       33 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       16 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 02:50:25.717052 rcp-colors-0.11/setup.cfg
+-rw-rw-rw-   0        0        0      981 2023-05-13 02:49:44.000000 rcp-colors-0.11/setup.py
```

### Comparing `rcp-colors-0.1/PKG-INFO` & `rcp-colors-0.11/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rcp-colors
-Version: 0.1
+Version: 0.11
 Summary: A Rich Color Picker app
 Home-page: https://github.com/PlusPlusMan/rcp
 Author: PlusPlusMan
 Author-email: contact@plusplusman.com
 Project-URL: Source, https://github.com/PlusPlusMan/rcp/
 Keywords: color picker,terminal app rgb hsl hex colors
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `rcp-colors-0.1/rcp_colors.egg-info/PKG-INFO` & `rcp-colors-0.11/rcp_colors.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rcp-colors
-Version: 0.1
+Version: 0.11
 Summary: A Rich Color Picker app
 Home-page: https://github.com/PlusPlusMan/rcp
 Author: PlusPlusMan
 Author-email: contact@plusplusman.com
 Project-URL: Source, https://github.com/PlusPlusMan/rcp/
 Keywords: color picker,terminal app rgb hsl hex colors
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `rcp-colors-0.1/setup.py` & `rcp-colors-0.11/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='rcp-colors',
-    version='0.1',
+    version='0.11',
     packages=find_packages(),
     description='A Rich Color Picker app',
     long_description='Terminal based rich color picker app',
     long_description_content_type='text/markdown',
     url='https://github.com/PlusPlusMan/rcp',
     author='PlusPlusMan',
     author_email='contact@plusplusman.com',
```

