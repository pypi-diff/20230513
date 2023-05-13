# Comparing `tmp/PyTraffic-1.0.5.tar.gz` & `tmp/PyTraffic-1.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyTraffic-1.0.5.tar", last modified: Sat May 13 10:03:12 2023, max compression
+gzip compressed data, was "PyTraffic-1.0.6.tar", last modified: Sat May 13 11:15:48 2023, max compression
```

## Comparing `PyTraffic-1.0.5.tar` & `PyTraffic-1.0.6.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 10:03:12.866756 PyTraffic-1.0.5/
--rw-rw-rw-   0        0        0     1091 2023-05-10 06:48:15.000000 PyTraffic-1.0.5/LICENSE.txt
--rw-rw-rw-   0        0        0      126 2023-05-13 07:33:47.000000 PyTraffic-1.0.5/MANIFEST.in
--rw-rw-rw-   0        0        0     4020 2023-05-13 10:03:12.864760 PyTraffic-1.0.5/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 10:03:12.840826 PyTraffic-1.0.5/PyTraffic/
--rw-rw-rw-   0        0        0      733 2023-05-13 10:01:39.000000 PyTraffic-1.0.5/PyTraffic/Density.py
--rw-rw-rw-   0        0        0     4063 2023-05-13 10:01:44.000000 PyTraffic-1.0.5/PyTraffic/LicensePlate.py
--rw-rw-rw-   0        0        0       59 2023-05-13 05:58:41.000000 PyTraffic-1.0.5/PyTraffic/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 10:03:12.859775 PyTraffic-1.0.5/PyTraffic/models/
--rw-rw-rw-   0        0        0   118802 2023-03-06 15:47:42.000000 PyTraffic-1.0.5/PyTraffic/models/cars.xml
--rw-rw-rw-   0        0        0    78136 2023-05-13 06:54:47.000000 PyTraffic-1.0.5/PyTraffic/models/license_plate_opencv.xml
-drwxrwxrwx   0        0        0        0 2023-05-13 10:03:12.854788 PyTraffic-1.0.5/PyTraffic.egg-info/
--rw-rw-rw-   0        0        0     4020 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      343 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       40 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 10:03:12.000000 PyTraffic-1.0.5/PyTraffic.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     3464 2023-05-13 10:02:03.000000 PyTraffic-1.0.5/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 10:03:12.866756 PyTraffic-1.0.5/setup.cfg
--rw-rw-rw-   0        0        0     1050 2023-05-13 10:01:59.000000 PyTraffic-1.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:15:48.765765 PyTraffic-1.0.6/
+-rw-rw-rw-   0        0        0     1091 2023-05-10 06:48:15.000000 PyTraffic-1.0.6/LICENSE.txt
+-rw-rw-rw-   0        0        0      126 2023-05-13 07:33:47.000000 PyTraffic-1.0.6/MANIFEST.in
+-rw-rw-rw-   0        0        0     3994 2023-05-13 11:15:48.764769 PyTraffic-1.0.6/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 11:15:48.738838 PyTraffic-1.0.6/PyTraffic/
+-rw-rw-rw-   0        0        0      800 2023-05-13 11:13:39.000000 PyTraffic-1.0.6/PyTraffic/Density.py
+-rw-rw-rw-   0        0        0     4126 2023-05-13 11:14:06.000000 PyTraffic-1.0.6/PyTraffic/LicensePlate.py
+-rw-rw-rw-   0        0        0       59 2023-05-13 05:58:41.000000 PyTraffic-1.0.6/PyTraffic/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:15:48.760781 PyTraffic-1.0.6/PyTraffic/models/
+-rw-rw-rw-   0        0        0   118802 2023-03-06 15:47:42.000000 PyTraffic-1.0.6/PyTraffic/models/cars.xml
+-rw-rw-rw-   0        0        0    78136 2023-05-13 06:54:47.000000 PyTraffic-1.0.6/PyTraffic/models/license_plate_opencv.xml
+drwxrwxrwx   0        0        0        0 2023-05-13 11:15:48.752800 PyTraffic-1.0.6/PyTraffic.egg-info/
+-rw-rw-rw-   0        0        0     3994 2023-05-13 11:15:48.000000 PyTraffic-1.0.6/PyTraffic.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      343 2023-05-13 11:15:48.000000 PyTraffic-1.0.6/PyTraffic.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 11:15:48.000000 PyTraffic-1.0.6/PyTraffic.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       40 2023-05-13 11:15:48.000000 PyTraffic-1.0.6/PyTraffic.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 11:15:48.000000 PyTraffic-1.0.6/PyTraffic.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     3438 2023-05-13 11:14:49.000000 PyTraffic-1.0.6/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 11:15:48.765765 PyTraffic-1.0.6/setup.cfg
+-rw-rw-rw-   0        0        0     1050 2023-05-13 11:14:45.000000 PyTraffic-1.0.6/setup.py
```

### Comparing `PyTraffic-1.0.5/LICENSE.txt` & `PyTraffic-1.0.6/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.5/PKG-INFO` & `PyTraffic-1.0.6/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyTraffic
-Version: 1.0.5
+Version: 1.0.6
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
-**Version** - 1.0.5</br>
+**Version** - 1.0.6</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
@@ -53,43 +53,43 @@
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 SOFTWARE.
 
 ## Credits
 
 This Python module uses open source components, libraries, modules, and packages. You can find the source code and license of their open source projects below, along with other information. I'm grateful to these developers for their contribution.
 
-**Project**: Tutorial (Web Page)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Shahid Akhtar Khan<br>
-**Link**: Visit [here](https://www.tutorialspoint.com/how-to-detect-license-plates-using-opencv-python) to check out the tutorial.<br>
-
-**Project**: Tutorial (Web Page)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Denis Kuria<br>
-**Link**: Visit [here](https://www.makeuseof.com/python-car-license-plates-detect-and-recognize).<br>
-
-**Project**: Python Module (opencv-python)<br>
-**Used For**: LicensePlate and Density (Sub-Modules)<br>
-**Author**: OpenCV<br>
-**Link**: Visit [here](https://github.com/opencv/opencv-python).<br>
-
-**Project**: Python Module (imutils)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: PyImageSearch<br>
-**Link**: Visit [here](https://github.com/PyImageSearch/imutils).<br>
-
-**Project**: Python Module (Numpy)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Numpy.org<br>
-**Link**: Visit [here](https://github.com/numpy/numpy).<br>
-
-**Project**: Python Module (PyTesseract)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: madmaze<br>
-**Link**: Visit [here](https://github.com/madmaze/pytesseract).<br>
+**Project:** Tutorial (Web Page)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Shahid Akhtar Khan<br>
+**Link:** Visit [here](https://www.tutorialspoint.com/how-to-detect-license-plates-using-opencv-python).<br>
+
+**Project:** Tutorial (Web Page)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Denis Kuria<br>
+**Link:** Visit [here](https://www.makeuseof.com/python-car-license-plates-detect-and-recognize).<br>
+
+**Project:** Python Module (opencv-python)<br>
+**Used For:** LicensePlate and Density (Sub-Modules)<br>
+**Author:** OpenCV<br>
+**Link:** Visit [here](https://github.com/opencv/opencv-python).<br>
+
+**Project:** Python Module (imutils)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** PyImageSearch<br>
+**Link:** Visit [here](https://github.com/PyImageSearch/imutils).<br>
+
+**Project:** Python Module (Numpy)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Numpy.org<br>
+**Link:** Visit [here](https://github.com/numpy/numpy).<br>
+
+**Project:** Python Module (PyTesseract)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** madmaze<br>
+**Link:** Visit [here](https://github.com/madmaze/pytesseract).<br>
 
 ## Issues & Bugs
 
 If you encounter any issues or bugs, visit the 'Issues' tab and create an issue. I'll look into it and resolve it ASAP.
 
 ## Conclusion
```

### Comparing `PyTraffic-1.0.5/PyTraffic/Density.py` & `PyTraffic-1.0.6/PyTraffic/Density.py`

 * *Files 20% similar despite different names*

```diff
@@ -4,17 +4,18 @@
 import cv2
 import os
 
 # Function 1 - Check Density
 def checkDensity(path):
     if (os.path.exists(path)):
         # Set Directory
-        os.chdir(os.path.dirname(os.path.realpath(__file__)))
+        directory = os.path.dirname(os.path.realpath(__file__))
+        directory = directory.replace(os.sep, "/")
 
-        carsXml = cv2.CascadeClassifier("models/cars.xml")
+        carsXml = cv2.CascadeClassifier(directory + "/models/cars.xml")
 
         count = 0
         frame = cv2.imread(path)
         gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
         cars = carsXml.detectMultiScale(gray, 1.1, 1)
 
         for (x,y,w,h) in cars:
```

### Comparing `PyTraffic-1.0.5/PyTraffic/LicensePlate.py` & `PyTraffic-1.0.6/PyTraffic/LicensePlate.py`

 * *Files 4% similar despite different names*

```diff
@@ -19,24 +19,25 @@
         programs.append(item.name)
 
     return "Tesseract-OCR - open source OCR engine" in programs
 
 # Function 2 - Check License Plate
 def checkLicensePlate(method, imagePath, tesseractPath="None"):
     # Set Directory
-    os.chdir(os.path.dirname(os.path.realpath(__file__)))
+    directory = os.path.dirname(os.path.realpath(__file__))
+    directory = directory.replace(os.sep, "/")
 
     if (os.path.exists(imagePath)):
         if (method == "OpenCV"): # OpenCV
             # Reading the Image
             img = cv2.imread(imagePath)
 
             # Converting the Images to Grayscale
             gray = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
-            cascade = cv2.CascadeClassifier('models/license_plate_opencv.xml')
+            cascade = cv2.CascadeClassifier(directory + "/models/license_plate_opencv.xml")
 
             # Finding the Plates
             plates = cascade.detectMultiScale(gray, 1.2, 5)
             print('Number of Detected License Plates:', len(plates))
 
             # Displaying Each License Plate
             for (x,y,w,h) in plates:
```

### Comparing `PyTraffic-1.0.5/PyTraffic/models/cars.xml` & `PyTraffic-1.0.6/PyTraffic/models/cars.xml`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.5/PyTraffic/models/license_plate_opencv.xml` & `PyTraffic-1.0.6/PyTraffic/models/license_plate_opencv.xml`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.5/PyTraffic.egg-info/PKG-INFO` & `PyTraffic-1.0.6/PyTraffic.egg-info/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyTraffic
-Version: 1.0.5
+Version: 1.0.6
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
-**Version** - 1.0.5</br>
+**Version** - 1.0.6</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
@@ -53,43 +53,43 @@
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 SOFTWARE.
 
 ## Credits
 
 This Python module uses open source components, libraries, modules, and packages. You can find the source code and license of their open source projects below, along with other information. I'm grateful to these developers for their contribution.
 
-**Project**: Tutorial (Web Page)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Shahid Akhtar Khan<br>
-**Link**: Visit [here](https://www.tutorialspoint.com/how-to-detect-license-plates-using-opencv-python) to check out the tutorial.<br>
-
-**Project**: Tutorial (Web Page)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Denis Kuria<br>
-**Link**: Visit [here](https://www.makeuseof.com/python-car-license-plates-detect-and-recognize).<br>
-
-**Project**: Python Module (opencv-python)<br>
-**Used For**: LicensePlate and Density (Sub-Modules)<br>
-**Author**: OpenCV<br>
-**Link**: Visit [here](https://github.com/opencv/opencv-python).<br>
-
-**Project**: Python Module (imutils)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: PyImageSearch<br>
-**Link**: Visit [here](https://github.com/PyImageSearch/imutils).<br>
-
-**Project**: Python Module (Numpy)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Numpy.org<br>
-**Link**: Visit [here](https://github.com/numpy/numpy).<br>
-
-**Project**: Python Module (PyTesseract)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: madmaze<br>
-**Link**: Visit [here](https://github.com/madmaze/pytesseract).<br>
+**Project:** Tutorial (Web Page)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Shahid Akhtar Khan<br>
+**Link:** Visit [here](https://www.tutorialspoint.com/how-to-detect-license-plates-using-opencv-python).<br>
+
+**Project:** Tutorial (Web Page)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Denis Kuria<br>
+**Link:** Visit [here](https://www.makeuseof.com/python-car-license-plates-detect-and-recognize).<br>
+
+**Project:** Python Module (opencv-python)<br>
+**Used For:** LicensePlate and Density (Sub-Modules)<br>
+**Author:** OpenCV<br>
+**Link:** Visit [here](https://github.com/opencv/opencv-python).<br>
+
+**Project:** Python Module (imutils)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** PyImageSearch<br>
+**Link:** Visit [here](https://github.com/PyImageSearch/imutils).<br>
+
+**Project:** Python Module (Numpy)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Numpy.org<br>
+**Link:** Visit [here](https://github.com/numpy/numpy).<br>
+
+**Project:** Python Module (PyTesseract)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** madmaze<br>
+**Link:** Visit [here](https://github.com/madmaze/pytesseract).<br>
 
 ## Issues & Bugs
 
 If you encounter any issues or bugs, visit the 'Issues' tab and create an issue. I'll look into it and resolve it ASAP.
 
 ## Conclusion
```

### Comparing `PyTraffic-1.0.5/README.md` & `PyTraffic-1.0.6/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 PyTraffic is a Python module to work on traffic-related functions and use cases.
 
 Read the docs on GitBook [here](https://aniketh-chavare.gitbook.io/pytraffic-docs).
 
 ## Module Information
 
 **Name** - PyTraffic</br>
-**Version** - 1.0.5</br>
+**Version** - 1.0.6</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
@@ -40,43 +40,43 @@
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 SOFTWARE.
 
 ## Credits
 
 This Python module uses open source components, libraries, modules, and packages. You can find the source code and license of their open source projects below, along with other information. I'm grateful to these developers for their contribution.
 
-**Project**: Tutorial (Web Page)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Shahid Akhtar Khan<br>
-**Link**: Visit [here](https://www.tutorialspoint.com/how-to-detect-license-plates-using-opencv-python) to check out the tutorial.<br>
-
-**Project**: Tutorial (Web Page)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Denis Kuria<br>
-**Link**: Visit [here](https://www.makeuseof.com/python-car-license-plates-detect-and-recognize).<br>
-
-**Project**: Python Module (opencv-python)<br>
-**Used For**: LicensePlate and Density (Sub-Modules)<br>
-**Author**: OpenCV<br>
-**Link**: Visit [here](https://github.com/opencv/opencv-python).<br>
-
-**Project**: Python Module (imutils)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: PyImageSearch<br>
-**Link**: Visit [here](https://github.com/PyImageSearch/imutils).<br>
-
-**Project**: Python Module (Numpy)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: Numpy.org<br>
-**Link**: Visit [here](https://github.com/numpy/numpy).<br>
-
-**Project**: Python Module (PyTesseract)<br>
-**Used For**: LicensePlate (Sub-Module)<br>
-**Author**: madmaze<br>
-**Link**: Visit [here](https://github.com/madmaze/pytesseract).<br>
+**Project:** Tutorial (Web Page)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Shahid Akhtar Khan<br>
+**Link:** Visit [here](https://www.tutorialspoint.com/how-to-detect-license-plates-using-opencv-python).<br>
+
+**Project:** Tutorial (Web Page)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Denis Kuria<br>
+**Link:** Visit [here](https://www.makeuseof.com/python-car-license-plates-detect-and-recognize).<br>
+
+**Project:** Python Module (opencv-python)<br>
+**Used For:** LicensePlate and Density (Sub-Modules)<br>
+**Author:** OpenCV<br>
+**Link:** Visit [here](https://github.com/opencv/opencv-python).<br>
+
+**Project:** Python Module (imutils)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** PyImageSearch<br>
+**Link:** Visit [here](https://github.com/PyImageSearch/imutils).<br>
+
+**Project:** Python Module (Numpy)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** Numpy.org<br>
+**Link:** Visit [here](https://github.com/numpy/numpy).<br>
+
+**Project:** Python Module (PyTesseract)<br>
+**Used For:** LicensePlate (Sub-Module)<br>
+**Author:** madmaze<br>
+**Link:** Visit [here](https://github.com/madmaze/pytesseract).<br>
 
 ## Issues & Bugs
 
 If you encounter any issues or bugs, visit the 'Issues' tab and create an issue. I'll look into it and resolve it ASAP.
 
 ## Conclusion
```

### Comparing `PyTraffic-1.0.5/setup.py` & `PyTraffic-1.0.6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 # README.md
 with open("README.md") as readme_file:
     README = readme_file.read()
 
 # Setup Arguements
 setup_args = dict (
     name="PyTraffic",
-    version="1.0.5",
+    version="1.0.6",
     description="PyTraffic is a Python module to work on traffic-related functions and use cases.",
     long_description_content_type="text/markdown",
     long_description=README,
     license="MIT",
     packages=find_packages(),
     include_package_data=True,
     author="Aniketh Chavare",
```

