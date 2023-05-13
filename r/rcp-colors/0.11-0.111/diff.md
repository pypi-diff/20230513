# Comparing `tmp/rcp-colors-0.11.tar.gz` & `tmp/rcp-colors-0.111.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rcp-colors-0.11.tar", last modified: Sat May 13 02:50:25 2023, max compression
+gzip compressed data, was "rcp-colors-0.111.tar", last modified: Sat May 13 03:01:22 2023, max compression
```

## Comparing `rcp-colors-0.11.tar` & `rcp-colors-0.111.tar`

### file list

```diff
@@ -1,11 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 02:50:25.716033 rcp-colors-0.11/
--rw-rw-rw-   0        0        0      613 2023-05-13 02:50:25.715031 rcp-colors-0.11/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 02:50:25.713658 rcp-colors-0.11/rcp_colors.egg-info/
--rw-rw-rw-   0        0        0      613 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      214 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       33 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       16 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/requires.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 02:50:25.000000 rcp-colors-0.11/rcp_colors.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 02:50:25.717052 rcp-colors-0.11/setup.cfg
--rw-rw-rw-   0        0        0      981 2023-05-13 02:49:44.000000 rcp-colors-0.11/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 03:01:22.545354 rcp-colors-0.111/
+-rw-rw-rw-   0        0        0      614 2023-05-13 03:01:22.542304 rcp-colors-0.111/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 03:01:22.518291 rcp-colors-0.111/rcp/
+-rw-rw-rw-   0        0        0       21 2023-05-13 02:58:35.000000 rcp-colors-0.111/rcp/__init__.py
+-rw-rw-rw-   0        0        0    28287 2023-05-13 02:56:30.000000 rcp-colors-0.111/rcp/rcp.py
+drwxrwxrwx   0        0        0        0 2023-05-13 03:01:22.539270 rcp-colors-0.111/rcp_colors.egg-info/
+-rw-rw-rw-   0        0        0      614 2023-05-13 03:01:22.000000 rcp-colors-0.111/rcp_colors.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      241 2023-05-13 03:01:22.000000 rcp-colors-0.111/rcp_colors.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 03:01:22.000000 rcp-colors-0.111/rcp_colors.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       37 2023-05-13 03:01:22.000000 rcp-colors-0.111/rcp_colors.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       16 2023-05-13 03:01:22.000000 rcp-colors-0.111/rcp_colors.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        4 2023-05-13 03:01:22.000000 rcp-colors-0.111/rcp_colors.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 03:01:22.546351 rcp-colors-0.111/setup.cfg
+-rw-rw-rw-   0        0        0      986 2023-05-13 03:01:16.000000 rcp-colors-0.111/setup.py
```

### Comparing `rcp-colors-0.11/PKG-INFO` & `rcp-colors-0.111/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rcp-colors
-Version: 0.11
+Version: 0.111
 Summary: A Rich Color Picker app
 Home-page: https://github.com/PlusPlusMan/rcp
 Author: PlusPlusMan
 Author-email: contact@plusplusman.com
 Project-URL: Source, https://github.com/PlusPlusMan/rcp/
 Keywords: color picker,terminal app rgb hsl hex colors
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `rcp-colors-0.11/rcp_colors.egg-info/PKG-INFO` & `rcp-colors-0.111/rcp_colors.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rcp-colors
-Version: 0.11
+Version: 0.111
 Summary: A Rich Color Picker app
 Home-page: https://github.com/PlusPlusMan/rcp
 Author: PlusPlusMan
 Author-email: contact@plusplusman.com
 Project-URL: Source, https://github.com/PlusPlusMan/rcp/
 Keywords: color picker,terminal app rgb hsl hex colors
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `rcp-colors-0.11/setup.py` & `rcp-colors-0.111/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='rcp-colors',
-    version='0.11',
+    version='0.111',
     packages=find_packages(),
     description='A Rich Color Picker app',
     long_description='Terminal based rich color picker app',
     long_description_content_type='text/markdown',
     url='https://github.com/PlusPlusMan/rcp',
     author='PlusPlusMan',
     author_email='contact@plusplusman.com',
@@ -20,14 +20,14 @@
     python_requires='>=3.6, <4',
     install_requires=[
         'textual',
         'appdirs',
     ],
     entry_points={
         'console_scripts': [
-            'rcp=rcp:main',
+            'rcp=rcp.rcp:main',
         ],
     },
     project_urls={
         'Source': 'https://github.com/PlusPlusMan/rcp/',
     },
 )
```

