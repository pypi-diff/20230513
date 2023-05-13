# Comparing `tmp/example_package_FabioScielzoOrtiz-0.0.1.tar.gz` & `tmp/example_package_FabioScielzoOrtiz-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "example_package_FabioScielzoOrtiz-0.0.1.tar", last modified: Sat May 13 17:53:21 2023, max compression
+gzip compressed data, was "example_package_FabioScielzoOrtiz-0.0.2.tar", last modified: Sat May 13 18:31:07 2023, max compression
```

## Comparing `example_package_FabioScielzoOrtiz-0.0.1.tar` & `example_package_FabioScielzoOrtiz-0.0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 17:53:21.711412 example_package_FabioScielzoOrtiz-0.0.1/
--rw-rw-rw-   0        0        0     1091 2023-05-13 15:25:04.000000 example_package_FabioScielzoOrtiz-0.0.1/LICENSE
--rw-rw-rw-   0        0        0      546 2023-05-13 17:53:21.710392 example_package_FabioScielzoOrtiz-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0       55 2023-05-13 17:07:08.000000 example_package_FabioScielzoOrtiz-0.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 17:53:21.699379 example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz/
--rw-rw-rw-   0        0        0        3 2023-05-13 15:13:50.000000 example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz/__init__.py
--rw-rw-rw-   0        0        0       43 2023-05-13 15:14:01.000000 example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz/example.py
-drwxrwxrwx   0        0        0        0 2023-05-13 17:53:21.709441 example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz.egg-info/
--rw-rw-rw-   0        0        0      546 2023-05-13 17:53:21.000000 example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      345 2023-05-13 17:53:21.000000 example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 17:53:21.000000 example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       34 2023-05-13 17:53:21.000000 example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 17:53:21.711412 example_package_FabioScielzoOrtiz-0.0.1/setup.cfg
--rw-rw-rw-   0        0        0      764 2023-05-13 17:30:24.000000 example_package_FabioScielzoOrtiz-0.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 18:31:07.613358 example_package_FabioScielzoOrtiz-0.0.2/
+-rw-rw-rw-   0        0        0     1091 2023-05-13 15:25:04.000000 example_package_FabioScielzoOrtiz-0.0.2/LICENSE
+-rw-rw-rw-   0        0        0      546 2023-05-13 18:31:07.612360 example_package_FabioScielzoOrtiz-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0       55 2023-05-13 17:07:08.000000 example_package_FabioScielzoOrtiz-0.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 18:31:07.603386 example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz/
+-rw-rw-rw-   0        0        0       32 2023-05-13 18:21:29.000000 example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz/__init__.py
+-rw-rw-rw-   0        0        0       43 2023-05-13 15:14:01.000000 example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz/example.py
+drwxrwxrwx   0        0        0        0 2023-05-13 18:31:07.611364 example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz.egg-info/
+-rw-rw-rw-   0        0        0      546 2023-05-13 18:31:07.000000 example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      345 2023-05-13 18:31:07.000000 example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 18:31:07.000000 example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       34 2023-05-13 18:31:07.000000 example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 18:31:07.613358 example_package_FabioScielzoOrtiz-0.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      764 2023-05-13 18:30:56.000000 example_package_FabioScielzoOrtiz-0.0.2/setup.py
```

### Comparing `example_package_FabioScielzoOrtiz-0.0.1/LICENSE` & `example_package_FabioScielzoOrtiz-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `example_package_FabioScielzoOrtiz-0.0.1/PKG-INFO` & `example_package_FabioScielzoOrtiz-0.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: example_package_FabioScielzoOrtiz
-Version: 0.0.1
+Version: 0.0.2
 Summary: A small example package
 Home-page: https://github.com/FabioScielzoOrtiz/Distances_Package
 Author: Fabio Scielzo Ortiz
 Author-email: fabioscielzo98@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `example_package_FabioScielzoOrtiz-0.0.1/example_package_FabioScielzoOrtiz.egg-info/PKG-INFO` & `example_package_FabioScielzoOrtiz-0.0.2/example_package_FabioScielzoOrtiz.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: example-package-FabioScielzoOrtiz
-Version: 0.0.1
+Version: 0.0.2
 Summary: A small example package
 Home-page: https://github.com/FabioScielzoOrtiz/Distances_Package
 Author: Fabio Scielzo Ortiz
 Author-email: fabioscielzo98@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `example_package_FabioScielzoOrtiz-0.0.1/setup.py` & `example_package_FabioScielzoOrtiz-0.0.2/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setup(
     name="example_package_FabioScielzoOrtiz",
-    version="0.0.1",
+    version="0.0.2",
     author="Fabio Scielzo Ortiz",
     author_email="fabioscielzo98@gmail.com",
     description="A small example package",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/FabioScielzoOrtiz/Distances_Package",  # add your project URL here
     packages=find_packages(),
```

