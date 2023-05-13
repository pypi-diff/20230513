# Comparing `tmp/PyTraffic-1.0.0.tar.gz` & `tmp/PyTraffic-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyTraffic-1.0.0.tar", last modified: Sat May 13 06:06:33 2023, max compression
+gzip compressed data, was "PyTraffic-1.0.1.tar", last modified: Sat May 13 06:42:45 2023, max compression
```

## Comparing `PyTraffic-1.0.0.tar` & `PyTraffic-1.0.1.tar`

### file list

```diff
@@ -1,13 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 06:06:33.750846 PyTraffic-1.0.0/
--rw-rw-rw-   0        0        0     1091 2023-05-10 06:48:15.000000 PyTraffic-1.0.0/LICENSE.txt
--rw-rw-rw-   0        0        0     2527 2023-05-13 06:06:33.749847 PyTraffic-1.0.0/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 06:06:33.624184 PyTraffic-1.0.0/PyTraffic/
--rw-rw-rw-   0        0        0       59 2023-05-13 05:58:41.000000 PyTraffic-1.0.0/PyTraffic/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 06:06:33.745859 PyTraffic-1.0.0/PyTraffic.egg-info/
--rw-rw-rw-   0        0        0     2527 2023-05-13 06:06:32.000000 PyTraffic-1.0.0/PyTraffic.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      184 2023-05-13 06:06:32.000000 PyTraffic-1.0.0/PyTraffic.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 06:06:32.000000 PyTraffic-1.0.0/PyTraffic.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 06:06:32.000000 PyTraffic-1.0.0/PyTraffic.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     2005 2023-05-13 05:57:52.000000 PyTraffic-1.0.0/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 06:06:33.750846 PyTraffic-1.0.0/setup.cfg
--rw-rw-rw-   0        0        0      920 2023-05-13 05:51:41.000000 PyTraffic-1.0.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:42:45.508238 PyTraffic-1.0.1/
+-rw-rw-rw-   0        0        0     1091 2023-05-10 06:48:15.000000 PyTraffic-1.0.1/LICENSE.txt
+-rw-rw-rw-   0        0        0       55 2023-05-13 06:38:51.000000 PyTraffic-1.0.1/MANIFEST.in
+-rw-rw-rw-   0        0        0     2527 2023-05-13 06:42:45.507241 PyTraffic-1.0.1/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 06:42:45.477321 PyTraffic-1.0.1/PyTraffic/
+-rw-rw-rw-   0        0        0      653 2023-05-13 06:31:28.000000 PyTraffic-1.0.1/PyTraffic/Density.py
+-rw-rw-rw-   0        0        0       59 2023-05-13 05:58:41.000000 PyTraffic-1.0.1/PyTraffic/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:42:45.501258 PyTraffic-1.0.1/PyTraffic/models/
+-rw-rw-rw-   0        0        0   118802 2023-03-06 15:47:42.000000 PyTraffic-1.0.1/PyTraffic/models/cars.xml
+drwxrwxrwx   0        0        0        0 2023-05-13 06:42:45.499262 PyTraffic-1.0.1/PyTraffic.egg-info/
+-rw-rw-rw-   0        0        0     2527 2023-05-13 06:42:45.000000 PyTraffic-1.0.1/PyTraffic.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      275 2023-05-13 06:42:45.000000 PyTraffic-1.0.1/PyTraffic.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 06:42:45.000000 PyTraffic-1.0.1/PyTraffic.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       14 2023-05-13 06:42:45.000000 PyTraffic-1.0.1/PyTraffic.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 06:42:45.000000 PyTraffic-1.0.1/PyTraffic.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     2005 2023-05-13 06:41:33.000000 PyTraffic-1.0.1/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 06:42:45.509235 PyTraffic-1.0.1/setup.cfg
+-rw-rw-rw-   0        0        0     1015 2023-05-13 06:40:50.000000 PyTraffic-1.0.1/setup.py
```

### Comparing `PyTraffic-1.0.0/LICENSE.txt` & `PyTraffic-1.0.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.0/PKG-INFO` & `PyTraffic-1.0.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyTraffic
-Version: 1.0.0
+Version: 1.0.1
 Summary: PyTraffic is a Python module to work on traffic-related functions and use cases.
 Home-page: https://github.com/Anikethc/PyTraffic
 Download-URL: https://pypi.org/project/PyTraffic
 Author: Aniketh Chavare
 Author-email: anikethchavare@outlook.com
 License: MIT
 Keywords: Traffic,Traffic Density,License Plates,Speed,Speed Calculation
@@ -18,15 +18,15 @@
 PyTraffic is a Python module to work on traffic-related functions and use cases.
 
 Read the docs on GitBook [here](https://aniketh-chavare.gitbook.io/pytraffic-docs).
 
 ## Module Information
 
 **Name** - PyTraffic</br>
-**Version** - 1.0.0</br>
+**Version** - 1.0.1</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
```

### Comparing `PyTraffic-1.0.0/PyTraffic.egg-info/PKG-INFO` & `PyTraffic-1.0.1/PyTraffic.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyTraffic
-Version: 1.0.0
+Version: 1.0.1
 Summary: PyTraffic is a Python module to work on traffic-related functions and use cases.
 Home-page: https://github.com/Anikethc/PyTraffic
 Download-URL: https://pypi.org/project/PyTraffic
 Author: Aniketh Chavare
 Author-email: anikethchavare@outlook.com
 License: MIT
 Keywords: Traffic,Traffic Density,License Plates,Speed,Speed Calculation
@@ -18,15 +18,15 @@
 PyTraffic is a Python module to work on traffic-related functions and use cases.
 
 Read the docs on GitBook [here](https://aniketh-chavare.gitbook.io/pytraffic-docs).
 
 ## Module Information
 
 **Name** - PyTraffic</br>
-**Version** - 1.0.0</br>
+**Version** - 1.0.1</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
```

### Comparing `PyTraffic-1.0.0/README.md` & `PyTraffic-1.0.1/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 PyTraffic is a Python module to work on traffic-related functions and use cases.
 
 Read the docs on GitBook [here](https://aniketh-chavare.gitbook.io/pytraffic-docs).
 
 ## Module Information
 
 **Name** - PyTraffic</br>
-**Version** - 1.0.0</br>
+**Version** - 1.0.1</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
```

### Comparing `PyTraffic-1.0.0/setup.py` & `PyTraffic-1.0.1/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -8,24 +8,27 @@
 # README.md
 with open("README.md") as readme_file:
     README = readme_file.read()
 
 # Setup Arguements
 setup_args = dict (
     name="PyTraffic",
-    version="1.0.0",
+    version="1.0.1",
     description="PyTraffic is a Python module to work on traffic-related functions and use cases.",
     long_description_content_type="text/markdown",
     long_description=README,
     license="MIT",
     packages=find_packages(),
     include_package_data=True,
     author="Aniketh Chavare",
     author_email="anikethchavare@outlook.com",
     keywords=["Traffic", "Traffic Density", "License Plates", "Speed", "Speed Calculation"],
     url="https://github.com/Anikethc/PyTraffic",
     download_url="https://pypi.org/project/PyTraffic"
 )
 
+# Install Requires
+install_requires = ["opencv-python"]
+
 # Run the Setup File
 if __name__ == "__main__":
-    setup(**setup_args)
+    setup(**setup_args, install_requires=install_requires)
```

