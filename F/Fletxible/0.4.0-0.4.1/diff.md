# Comparing `tmp/Fletxible-0.4.0.tar.gz` & `tmp/Fletxible-0.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Fletxible-0.4.0.tar", last modified: Sat May 13 13:45:57 2023, max compression
+gzip compressed data, was "Fletxible-0.4.1.tar", last modified: Sat May 13 13:56:08 2023, max compression
```

## Comparing `Fletxible-0.4.0.tar` & `Fletxible-0.4.1.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:45:57.787034 Fletxible-0.4.0/
-drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:45:57.784049 Fletxible-0.4.0/Fletxible.egg-info/
--rw-r--r--   0 ahmad      (501) staff       (20)      830 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/PKG-INFO
--rw-r--r--   0 ahmad      (501) staff       (20)      326 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/SOURCES.txt
--rw-r--r--   0 ahmad      (501) staff       (20)        1 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/dependency_links.txt
--rw-r--r--   0 ahmad      (501) staff       (20)       50 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/entry_points.txt
--rw-r--r--   0 ahmad      (501) staff       (20)       37 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/requires.txt
--rw-r--r--   0 ahmad      (501) staff       (20)        6 2023-05-13 13:45:57.000000 Fletxible-0.4.0/Fletxible.egg-info/top_level.txt
--rw-r--r--   0 ahmad      (501) staff       (20)     1079 2023-04-29 15:25:05.000000 Fletxible-0.4.0/LICENSE
--rw-r--r--   0 ahmad      (501) staff       (20)      830 2023-05-13 13:45:57.786799 Fletxible-0.4.0/PKG-INFO
--rw-r--r--   0 ahmad      (501) staff       (20)     4106 2023-05-01 16:06:19.000000 Fletxible-0.4.0/README.md
-drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:45:57.785849 Fletxible-0.4.0/logic/
--rw-r--r--   0 ahmad      (501) staff       (20)        0 2023-05-01 13:39:08.000000 Fletxible-0.4.0/logic/__init__.py
--rw-r--r--   0 ahmad      (501) staff       (20)     2171 2023-05-13 13:43:07.000000 Fletxible-0.4.0/logic/cli.py
--rw-r--r--   0 ahmad      (501) staff       (20)      164 2023-05-13 13:31:46.000000 Fletxible-0.4.0/logic/main.py
--rw-r--r--   0 ahmad      (501) staff       (20)     6555 2023-05-13 13:45:23.000000 Fletxible-0.4.0/logic/script.py
--rw-r--r--   0 ahmad      (501) staff       (20)     2093 2023-05-13 13:40:00.000000 Fletxible-0.4.0/logic/utilities.py
--rw-r--r--   0 ahmad      (501) staff       (20)       38 2023-05-13 13:45:57.787101 Fletxible-0.4.0/setup.cfg
--rw-r--r--   0 ahmad      (501) staff       (20)     1110 2023-05-13 13:45:18.000000 Fletxible-0.4.0/setup.py
-drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:45:57.786307 Fletxible-0.4.0/tests/
--rw-r--r--   0 ahmad      (501) staff       (20)        5 2023-05-01 14:25:50.000000 Fletxible-0.4.0/tests/test_route.py
+drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:56:08.551626 Fletxible-0.4.1/
+drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:56:08.548640 Fletxible-0.4.1/Fletxible.egg-info/
+-rw-r--r--   0 ahmad      (501) staff       (20)      830 2023-05-13 13:56:08.000000 Fletxible-0.4.1/Fletxible.egg-info/PKG-INFO
+-rw-r--r--   0 ahmad      (501) staff       (20)      326 2023-05-13 13:56:08.000000 Fletxible-0.4.1/Fletxible.egg-info/SOURCES.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)        1 2023-05-13 13:56:08.000000 Fletxible-0.4.1/Fletxible.egg-info/dependency_links.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)       50 2023-05-13 13:56:08.000000 Fletxible-0.4.1/Fletxible.egg-info/entry_points.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)       37 2023-05-13 13:56:08.000000 Fletxible-0.4.1/Fletxible.egg-info/requires.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)        6 2023-05-13 13:56:08.000000 Fletxible-0.4.1/Fletxible.egg-info/top_level.txt
+-rw-r--r--   0 ahmad      (501) staff       (20)     1079 2023-04-29 15:25:05.000000 Fletxible-0.4.1/LICENSE
+-rw-r--r--   0 ahmad      (501) staff       (20)      830 2023-05-13 13:56:08.551396 Fletxible-0.4.1/PKG-INFO
+-rw-r--r--   0 ahmad      (501) staff       (20)     4106 2023-05-01 16:06:19.000000 Fletxible-0.4.1/README.md
+drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:56:08.550493 Fletxible-0.4.1/logic/
+-rw-r--r--   0 ahmad      (501) staff       (20)        0 2023-05-01 13:39:08.000000 Fletxible-0.4.1/logic/__init__.py
+-rw-r--r--   0 ahmad      (501) staff       (20)     2168 2023-05-13 13:50:26.000000 Fletxible-0.4.1/logic/cli.py
+-rw-r--r--   0 ahmad      (501) staff       (20)      164 2023-05-13 13:31:46.000000 Fletxible-0.4.1/logic/main.py
+-rw-r--r--   0 ahmad      (501) staff       (20)     6555 2023-05-13 13:45:23.000000 Fletxible-0.4.1/logic/script.py
+-rw-r--r--   0 ahmad      (501) staff       (20)     2094 2023-05-13 13:48:57.000000 Fletxible-0.4.1/logic/utilities.py
+-rw-r--r--   0 ahmad      (501) staff       (20)       38 2023-05-13 13:56:08.551693 Fletxible-0.4.1/setup.cfg
+-rw-r--r--   0 ahmad      (501) staff       (20)     1110 2023-05-13 13:53:17.000000 Fletxible-0.4.1/setup.py
+drwxr-xr-x   0 ahmad      (501) staff       (20)        0 2023-05-13 13:56:08.550930 Fletxible-0.4.1/tests/
+-rw-r--r--   0 ahmad      (501) staff       (20)        5 2023-05-01 14:25:50.000000 Fletxible-0.4.1/tests/test_route.py
```

### Comparing `Fletxible-0.4.0/Fletxible.egg-info/PKG-INFO` & `Fletxible-0.4.1/Fletxible.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Fletxible
-Version: 0.4.0
+Version: 0.4.1
 Summary: Web Boilerplate for Flet Library
 Home-page: https://github.com/LineIndent/fletxible
 Author: S. Ahmad P. Hakimi
 Author-email: pourhakimi@pm.me
 Keywords: python web template,web application,development
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `Fletxible-0.4.0/LICENSE` & `Fletxible-0.4.1/LICENSE`

 * *Files identical despite different names*

### Comparing `Fletxible-0.4.0/PKG-INFO` & `Fletxible-0.4.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Fletxible
-Version: 0.4.0
+Version: 0.4.1
 Summary: Web Boilerplate for Flet Library
 Home-page: https://github.com/LineIndent/fletxible
 Author: S. Ahmad P. Hakimi
 Author-email: pourhakimi@pm.me
 Keywords: python web template,web application,development
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `Fletxible-0.4.0/README.md` & `Fletxible-0.4.1/README.md`

 * *Files identical despite different names*

### Comparing `Fletxible-0.4.0/logic/cli.py` & `Fletxible-0.4.1/logic/cli.py`

 * *Files 1% similar despite different names*

```diff
@@ -63,15 +63,15 @@
     for files in file_list:
         click.echo(f"● {files}")
     click.echo("Status: OK")
     click.echo()
 
     click.echo("Configuring main.py ...")
     init_main_method()
-    subprocess.run(["flet", "-r", "logic/main.py"], capture_output=True, text=True)
+    subprocess.run(["python3", "logic/main.py"], capture_output=True, text=True)
     click.echo("Status: OK")
 
 
 @click.group()
 def flet_template():
     pass
```

### Comparing `Fletxible-0.4.0/logic/script.py` & `Fletxible-0.4.1/logic/script.py`

 * *Files identical despite different names*

### Comparing `Fletxible-0.4.0/logic/utilities.py` & `Fletxible-0.4.1/logic/utilities.py`

 * *Files 1% similar despite different names*

```diff
@@ -69,15 +69,15 @@
 def set_up_yaml_file():
     string = """
 site-name: ""
 repo-url: ""
 
 theme:
   - bgcolor: "#2e2f3e"
-  - primary: "red"
+  - primary: "teal"
   - accent: "blue300"
 
 nav:
   - Home: "index.py"
   - About: "about.py"
 
 """
```

### Comparing `Fletxible-0.4.0/setup.py` & `Fletxible-0.4.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 setup(
     name="Fletxible",
-    version="0.4.0",
+    version="0.4.1",
     author="S. Ahmad P. Hakimi",
     author_email="pourhakimi@pm.me",
     description="Web Boilerplate for Flet Library",
     long_description="Fletxible is a Python web boilerplate project designed to provide a solid foundation for building web applications with Python and Flet. The project comes pre-configured with a range of tools and features to make it easy for developers to get started building their applications, without the need to spend time setting up infrastructure or configuring tools.",
     long_description_content_type="text/markdown",
     url="https://github.com/LineIndent/fletxible",
     packages=["logic"],
```

