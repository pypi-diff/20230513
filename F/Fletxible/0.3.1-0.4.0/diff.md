# Comparing `tmp/Fletxible-0.3.1.tar.gz` & `tmp/Fletxible-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Fletxible-0.3.1.tar", last modified: Wed May 10 13:03:13 2023, max compression
+gzip compressed data, was "Fletxible-0.4.0.tar", last modified: Sat May 13 13:45:57 2023, max compression
```

## Comparing `Fletxible-0.3.1.tar` & `Fletxible-0.4.0.tar`

### file list

```diff
@@ -1,23 +1,21 @@
-drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-10 13:03:13.807184 Fletxible-0.3.1/
-drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-10 13:03:13.803251 Fletxible-0.3.1/Fletxible.egg-info/
--rw-r--r--   0 ahmad      (501) staff       (20)      830 2023-05-10 13:03:13.000000 Fletxible-0.3.1/Fletxible.egg-info/PKG-INFO
--rw-r--r--   0 ahmad      (501) staff       (20)      357 2023-05-10 13:03:13.000000 Fletxible-0.3.1/Fletxible.egg-info/SOURCES.txt
--rw-r--r--   0 ahmad      (501) staff       (20)        1 2023-05-10 13:03:13.000000 Fletxible-0.3.1/Fletxible.egg-info/dependency_links.txt
--rw-r--r--   0 ahmad      (501) staff       (20)       50 2023-05-10 13:03:13.000000 Fletxible-0.3.1/Fletxible.egg-info/entry_points.txt
--rw-r--r--   0 ahmad      (501) staff       (20)       53 2023-05-10 13:03:13.000000 Fletxible-0.3.1/Fletxible.egg-info/requires.txt
--rw-r--r--   0 ahmad      (501) staff       (20)        6 2023-05-10 13:03:13.000000 Fletxible-0.3.1/Fletxible.egg-info/top_level.txt
--rw-r--r--   0 ahmad      (501) staff       (20)     1079 2023-04-29 15:25:05.000000 Fletxible-0.3.1/LICENSE
--rw-r--r--   0 ahmad      (501) staff       (20)      830 2023-05-10 13:03:13.806912 Fletxible-0.3.1/PKG-INFO
--rw-r--r--   0 ahmad      (501) staff       (20)     4106 2023-05-01 16:06:19.000000 Fletxible-0.3.1/README.md
-drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-10 13:03:13.805901 Fletxible-0.3.1/logic/
--rw-r--r--   0 ahmad      (501) staff       (20)        0 2023-05-01 13:39:08.000000 Fletxible-0.3.1/logic/__init__.py
--rw-r--r--   0 ahmad      (501) staff       (20)     1288 2023-05-01 13:50:27.000000 Fletxible-0.3.1/logic/cli.py
--rw-r--r--   0 ahmad      (501) staff       (20)      164 2023-05-02 14:50:14.000000 Fletxible-0.3.1/logic/main.py
--rw-r--r--   0 ahmad      (501) staff       (20)      243 2023-05-02 14:50:26.000000 Fletxible-0.3.1/logic/mapped.py
--rw-r--r--   0 ahmad      (501) staff       (20)      343 2023-05-02 14:50:26.000000 Fletxible-0.3.1/logic/route.py
--rw-r--r--   0 ahmad      (501) staff       (20)     6566 2023-05-02 11:51:56.000000 Fletxible-0.3.1/logic/script.py
--rw-r--r--   0 ahmad      (501) staff       (20)     1860 2023-05-01 13:04:12.000000 Fletxible-0.3.1/logic/utilities.py
--rw-r--r--   0 ahmad      (501) staff       (20)       38 2023-05-10 13:03:13.807267 Fletxible-0.3.1/setup.cfg
--rw-r--r--   0 ahmad      (501) staff       (20)     1130 2023-05-10 13:02:35.000000 Fletxible-0.3.1/setup.py
-drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-10 13:03:13.806359 Fletxible-0.3.1/tests/
--rw-r--r--   0 ahmad      (501) staff       (20)        5 2023-05-01 14:25:50.000000 Fletxible-0.3.1/tests/test_route.py
+drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:45:57.787034 Fletxible-0.4.0/
+drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:45:57.784049 Fletxible-0.4.0/Fletxible.egg-info/
+-rw-r--r--   0 ahmad      (501) staff       (20)      830 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/PKG-INFO
+-rw-r--r--   0 ahmad      (501) staff       (20)      326 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/SOURCES.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)        1 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/dependency_links.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)       50 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/entry_points.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)       37 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/requires.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)        6 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/top_level.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)     1079 2023-04-29 15:25:05.000000 Fletxible-0.4.0/LICENSE
+-rw-r--r--   0 ahmad      (501) staff       (20)      830 2023-05-13 13:45:57.786799 Fletxible-0.4.0/PKG-INFO
+-rw-r--r--   0 ahmad      (501) staff       (20)     4106 2023-05-01 16:06:19.000000 Fletxible-0.4.0/README.md
+drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:45:57.785849 Fletxible-0.4.0/logic/
+-rw-r--r--   0 ahmad      (501) staff       (20)        0 2023-05-01 13:39:08.000000 Fletxible-0.4.0/logic/__init__.py
+-rw-r--r--   0 ahmad      (501) staff       (20)     2171 2023-05-13 13:43:07.000000 Fletxible-0.4.0/logic/cli.py
+-rw-r--r--   0 ahmad      (501) staff       (20)      164 2023-05-13 13:31:46.000000 Fletxible-0.4.0/logic/main.py
+-rw-r--r--   0 ahmad      (501) staff       (20)     6555 2023-05-13 13:45:23.000000 Fletxible-0.4.0/logic/script.py
+-rw-r--r--   0 ahmad      (501) staff       (20)     2093 2023-05-13 13:40:00.000000 Fletxible-0.4.0/logic/utilities.py
+-rw-r--r--   0 ahmad      (501) staff       (20)       38 2023-05-13 13:45:57.787101 Fletxible-0.4.0/setup.cfg
+-rw-r--r--   0 ahmad      (501) staff       (20)     1110 2023-05-13 13:45:18.000000 Fletxible-0.4.0/setup.py
+drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:45:57.786307 Fletxible-0.4.0/tests/
+-rw-r--r--   0 ahmad      (501) staff       (20)        5 2023-05-01 14:25:50.000000 Fletxible-0.4.0/tests/test_route.py
```

### Comparing `Fletxible-0.3.1/Fletxible.egg-info/PKG-INFO` & `Fletxible-0.4.0/Fletxible.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Fletxible
-Version: 0.3.1
+Version: 0.4.0
 Summary: Web Boilerplate for Flet Library
 Home-page: https://github.com/LineIndent/fletxible
 Author: S. Ahmad P. Hakimi
 Author-email: pourhakimi@pm.me
 Keywords: python web template,web application,development
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `Fletxible-0.3.1/LICENSE` & `Fletxible-0.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `Fletxible-0.3.1/PKG-INFO` & `Fletxible-0.4.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Fletxible
-Version: 0.3.1
+Version: 0.4.0
 Summary: Web Boilerplate for Flet Library
 Home-page: https://github.com/LineIndent/fletxible
 Author: S. Ahmad P. Hakimi
 Author-email: pourhakimi@pm.me
 Keywords: python web template,web application,development
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `Fletxible-0.3.1/README.md` & `Fletxible-0.4.0/README.md`

 * *Files identical despite different names*

### Comparing `Fletxible-0.3.1/logic/script.py` & `Fletxible-0.4.0/logic/script.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import os, importlib.util
 import yaml
-import pickle5 as pickle
+import pickle
 import flet as ft
 
 from utilities import (
     route_string_method,
     set_app_route_method,
     set_app_default_pages,
     navigation_example_method,
```

### Comparing `Fletxible-0.3.1/logic/utilities.py` & `Fletxible-0.4.0/logic/utilities.py`

 * *Files 12% similar despite different names*

```diff
@@ -78,7 +78,24 @@
 
 nav:
   - Home: "index.py"
   - About: "about.py"
 
 """
     return string
+
+
+def set_up_main_method():
+    string = """import flet as ft
+from script import script
+
+
+def main(page: ft.Page):
+    script(page)
+    page.update()
+
+
+if __name__ == "__main__":
+    ft.flet.app(target=main)  
+"""
+
+    return string
```

### Comparing `Fletxible-0.3.1/setup.py` & `Fletxible-0.4.0/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 from setuptools import setup
 
 setup(
     name="Fletxible",
-    version="0.3.1",
+    version="0.4.0",
     author="S. Ahmad P. Hakimi",
     author_email="pourhakimi@pm.me",
     description="Web Boilerplate for Flet Library",
     long_description="Fletxible is a Python web boilerplate project designed to provide a solid foundation for building web applications with Python and Flet. The project comes pre-configured with a range of tools and features to make it easy for developers to get started building their applications, without the need to spend time setting up infrastructure or configuring tools.",
     long_description_content_type="text/markdown",
     url="https://github.com/LineIndent/fletxible",
     packages=["logic"],
-    install_requires=["click==8.1.3", "flet==0.6.2", " pickle5==0.0.12", "PyYAML==6.0"],
+    install_requires=["click>=8.1.3", "flet>=0.6.2", "PyYAML>=6.0"],
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
     ],
     entry_points={
         "console_scripts": ["fletxible-init=logic.cli:init"],
```

