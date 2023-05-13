# Comparing `tmp/PyTraffic-1.0.4.tar.gz` & `tmp/PyTraffic-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyTraffic-1.0.4.tar", last modified: Sat May 13 09:51:39 2023, max compression
+gzip compressed data, was "PyTraffic-1.0.5.tar", last modified: Sat May 13 10:03:12 2023, max compression
```

## Comparing `PyTraffic-1.0.4.tar` & `PyTraffic-1.0.5.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 09:51:39.877000 PyTraffic-1.0.4/
--rw-rw-rw-   0        0        0     1091 2023-05-10 06:48:15.000000 PyTraffic-1.0.4/LICENSE.txt
--rw-rw-rw-   0        0        0      126 2023-05-13 07:33:47.000000 PyTraffic-1.0.4/MANIFEST.in
--rw-rw-rw-   0        0        0     4020 2023-05-13 09:51:39.875999 PyTraffic-1.0.4/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 09:51:39.852070 PyTraffic-1.0.4/PyTraffic/
--rw-rw-rw-   0        0        0      653 2023-05-13 06:31:28.000000 PyTraffic-1.0.4/PyTraffic/Density.py
--rw-rw-rw-   0        0        0     3991 2023-05-13 09:50:13.000000 PyTraffic-1.0.4/PyTraffic/LicensePlate.py
--rw-rw-rw-   0        0        0       59 2023-05-13 05:58:41.000000 PyTraffic-1.0.4/PyTraffic/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 09:51:39.872012 PyTraffic-1.0.4/PyTraffic/models/
--rw-rw-rw-   0        0        0   118802 2023-03-06 15:47:42.000000 PyTraffic-1.0.4/PyTraffic/models/cars.xml
--rw-rw-rw-   0        0        0    78136 2023-05-13 06:54:47.000000 PyTraffic-1.0.4/PyTraffic/models/license_plate_opencv.xml
-drwxrwxrwx   0        0        0        0 2023-05-13 09:51:39.866025 PyTraffic-1.0.4/PyTraffic.egg-info/
--rw-rw-rw-   0        0        0     4020 2023-05-13 09:51:39.000000 PyTraffic-1.0.4/PyTraffic.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      343 2023-05-13 09:51:39.000000 PyTraffic-1.0.4/PyTraffic.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 09:51:39.000000 PyTraffic-1.0.4/PyTraffic.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       40 2023-05-13 09:51:39.000000 PyTraffic-1.0.4/PyTraffic.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 09:51:39.000000 PyTraffic-1.0.4/PyTraffic.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     3464 2023-05-13 09:47:06.000000 PyTraffic-1.0.4/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 09:51:39.877993 PyTraffic-1.0.4/setup.cfg
--rw-rw-rw-   0        0        0     1050 2023-05-13 09:47:01.000000 PyTraffic-1.0.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:03:12.866756 PyTraffic-1.0.5/
+-rw-rw-rw-   0        0        0     1091 2023-05-10 06:48:15.000000 PyTraffic-1.0.5/LICENSE.txt
+-rw-rw-rw-   0        0        0      126 2023-05-13 07:33:47.000000 PyTraffic-1.0.5/MANIFEST.in
+-rw-rw-rw-   0        0        0     4020 2023-05-13 10:03:12.864760 PyTraffic-1.0.5/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 10:03:12.840826 PyTraffic-1.0.5/PyTraffic/
+-rw-rw-rw-   0        0        0      733 2023-05-13 10:01:39.000000 PyTraffic-1.0.5/PyTraffic/Density.py
+-rw-rw-rw-   0        0        0     4063 2023-05-13 10:01:44.000000 PyTraffic-1.0.5/PyTraffic/LicensePlate.py
+-rw-rw-rw-   0        0        0       59 2023-05-13 05:58:41.000000 PyTraffic-1.0.5/PyTraffic/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:03:12.859775 PyTraffic-1.0.5/PyTraffic/models/
+-rw-rw-rw-   0        0        0   118802 2023-03-06 15:47:42.000000 PyTraffic-1.0.5/PyTraffic/models/cars.xml
+-rw-rw-rw-   0        0        0    78136 2023-05-13 06:54:47.000000 PyTraffic-1.0.5/PyTraffic/models/license_plate_opencv.xml
+drwxrwxrwx   0        0        0        0 2023-05-13 10:03:12.854788 PyTraffic-1.0.5/PyTraffic.egg-info/
+-rw-rw-rw-   0        0        0     4020 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      343 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       40 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     3464 2023-05-13 10:02:03.000000 PyTraffic-1.0.5/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 10:03:12.866756 PyTraffic-1.0.5/setup.cfg
+-rw-rw-rw-   0        0        0     1050 2023-05-13 10:01:59.000000 PyTraffic-1.0.5/setup.py
```

### Comparing `PyTraffic-1.0.4/LICENSE.txt` & `PyTraffic-1.0.5/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.4/PKG-INFO` & `PyTraffic-1.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyTraffic
-Version: 1.0.4
+Version: 1.0.5
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
-**Version** - 1.0.4</br>
+**Version** - 1.0.5</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
```

### Comparing `PyTraffic-1.0.4/PyTraffic/Density.py` & `PyTraffic-1.0.5/PyTraffic/Density.py`

 * *Files 14% similar despite different names*

```diff
@@ -3,15 +3,18 @@
 # Imports
 import cv2
 import os
 
 # Function 1 - Check Density
 def checkDensity(path):
     if (os.path.exists(path)):
-        carsXml = cv2.CascadeClassifier("PyTraffic/models/cars.xml")
+        # Set Directory
+        os.chdir(os.path.dirname(os.path.realpath(__file__)))
+
+        carsXml = cv2.CascadeClassifier("models/cars.xml")
 
         count = 0
         frame = cv2.imread(path)
         gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
         cars = carsXml.detectMultiScale(gray, 1.1, 1)
 
         for (x,y,w,h) in cars:
```

### Comparing `PyTraffic-1.0.4/PyTraffic/LicensePlate.py` & `PyTraffic-1.0.5/PyTraffic/LicensePlate.py`

 * *Files 11% similar despite different names*

```diff
@@ -18,22 +18,25 @@
     for item in winapps.list_installed():
         programs.append(item.name)
 
     return "Tesseract-OCR - open source OCR engine" in programs
 
 # Function 2 - Check License Plate
 def checkLicensePlate(method, imagePath, tesseractPath="None"):
+    # Set Directory
+    os.chdir(os.path.dirname(os.path.realpath(__file__)))
+
     if (os.path.exists(imagePath)):
         if (method == "OpenCV"): # OpenCV
             # Reading the Image
             img = cv2.imread(imagePath)
 
             # Converting the Images to Grayscale
             gray = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
-            cascade = cv2.CascadeClassifier('PyTraffic/models/license_plate_opencv.xml')
+            cascade = cv2.CascadeClassifier('models/license_plate_opencv.xml')
 
             # Finding the Plates
             plates = cascade.detectMultiScale(gray, 1.2, 5)
             print('Number of Detected License Plates:', len(plates))
 
             # Displaying Each License Plate
             for (x,y,w,h) in plates:
```

### Comparing `PyTraffic-1.0.4/PyTraffic/models/cars.xml` & `PyTraffic-1.0.5/PyTraffic/models/cars.xml`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.4/PyTraffic/models/license_plate_opencv.xml` & `PyTraffic-1.0.5/PyTraffic/models/license_plate_opencv.xml`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.4/PyTraffic.egg-info/PKG-INFO` & `PyTraffic-1.0.5/PyTraffic.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyTraffic
-Version: 1.0.4
+Version: 1.0.5
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
-**Version** - 1.0.4</br>
+**Version** - 1.0.5</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
```

### Comparing `PyTraffic-1.0.4/README.md` & `PyTraffic-1.0.5/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 PyTraffic is a Python module to work on traffic-related functions and use cases.
 
 Read the docs on GitBook [here](https://aniketh-chavare.gitbook.io/pytraffic-docs).
 
 ## Module Information
 
 **Name** - PyTraffic</br>
-**Version** - 1.0.4</br>
+**Version** - 1.0.5</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
```

### Comparing `PyTraffic-1.0.4/setup.py` & `PyTraffic-1.0.5/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 # README.md
 with open("README.md") as readme_file:
     README = readme_file.read()
 
 # Setup Arguements
 setup_args = dict (
     name="PyTraffic",
-    version="1.0.4",
+    version="1.0.5",
     description="PyTraffic is a Python module to work on traffic-related functions and use cases.",
     long_description_content_type="text/markdown",
     long_description=README,
     license="MIT",
     packages=find_packages(),
     include_package_data=True,
     author="Aniketh Chavare",
```

