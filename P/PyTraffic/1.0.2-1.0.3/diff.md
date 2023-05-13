# Comparing `tmp/PyTraffic-1.0.2.tar.gz` & `tmp/PyTraffic-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyTraffic-1.0.2.tar", last modified: Sat May 13 07:52:37 2023, max compression
+gzip compressed data, was "PyTraffic-1.0.3.tar", last modified: Sat May 13 09:35:07 2023, max compression
```

## Comparing `PyTraffic-1.0.2.tar` & `PyTraffic-1.0.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 07:52:37.622362 PyTraffic-1.0.2/
--rw-rw-rw-   0        0        0     1091 2023-05-10 06:48:15.000000 PyTraffic-1.0.2/LICENSE.txt
--rw-rw-rw-   0        0        0      126 2023-05-13 07:33:47.000000 PyTraffic-1.0.2/MANIFEST.in
--rw-rw-rw-   0        0        0     3252 2023-05-13 07:52:37.621364 PyTraffic-1.0.2/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 07:52:37.592444 PyTraffic-1.0.2/PyTraffic/
--rw-rw-rw-   0        0        0      653 2023-05-13 06:31:28.000000 PyTraffic-1.0.2/PyTraffic/Density.py
--rw-rw-rw-   0        0        0     3345 2023-05-13 07:48:03.000000 PyTraffic-1.0.2/PyTraffic/LicensePlate.py
--rw-rw-rw-   0        0        0       59 2023-05-13 05:58:41.000000 PyTraffic-1.0.2/PyTraffic/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 07:52:37.617375 PyTraffic-1.0.2/PyTraffic/models/
--rw-rw-rw-   0        0        0   118802 2023-03-06 15:47:42.000000 PyTraffic-1.0.2/PyTraffic/models/cars.xml
--rw-rw-rw-   0        0        0    78136 2023-05-13 06:54:47.000000 PyTraffic-1.0.2/PyTraffic/models/license_plate_opencv.xml
-drwxrwxrwx   0        0        0        0 2023-05-13 07:52:37.610393 PyTraffic-1.0.2/PyTraffic.egg-info/
--rw-rw-rw-   0        0        0     3252 2023-05-13 07:52:37.000000 PyTraffic-1.0.2/PyTraffic.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      343 2023-05-13 07:52:37.000000 PyTraffic-1.0.2/PyTraffic.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 07:52:37.000000 PyTraffic-1.0.2/PyTraffic.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       40 2023-05-13 07:52:37.000000 PyTraffic-1.0.2/PyTraffic.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 07:52:37.000000 PyTraffic-1.0.2/PyTraffic.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     2716 2023-05-13 07:52:25.000000 PyTraffic-1.0.2/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 07:52:37.623359 PyTraffic-1.0.2/setup.cfg
--rw-rw-rw-   0        0        0     1050 2023-05-13 07:47:01.000000 PyTraffic-1.0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 09:35:07.926568 PyTraffic-1.0.3/
+-rw-rw-rw-   0        0        0     1091 2023-05-10 06:48:15.000000 PyTraffic-1.0.3/LICENSE.txt
+-rw-rw-rw-   0        0        0      126 2023-05-13 07:33:47.000000 PyTraffic-1.0.3/MANIFEST.in
+-rw-rw-rw-   0        0        0     4020 2023-05-13 09:35:07.924531 PyTraffic-1.0.3/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 09:35:07.902590 PyTraffic-1.0.3/PyTraffic/
+-rw-rw-rw-   0        0        0      653 2023-05-13 06:31:28.000000 PyTraffic-1.0.3/PyTraffic/Density.py
+-rw-rw-rw-   0        0        0     3964 2023-05-13 09:31:29.000000 PyTraffic-1.0.3/PyTraffic/LicensePlate.py
+-rw-rw-rw-   0        0        0       59 2023-05-13 05:58:41.000000 PyTraffic-1.0.3/PyTraffic/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 09:35:07.921539 PyTraffic-1.0.3/PyTraffic/models/
+-rw-rw-rw-   0        0        0   118802 2023-03-06 15:47:42.000000 PyTraffic-1.0.3/PyTraffic/models/cars.xml
+-rw-rw-rw-   0        0        0    78136 2023-05-13 06:54:47.000000 PyTraffic-1.0.3/PyTraffic/models/license_plate_opencv.xml
+drwxrwxrwx   0        0        0        0 2023-05-13 09:35:07.916554 PyTraffic-1.0.3/PyTraffic.egg-info/
+-rw-rw-rw-   0        0        0     4020 2023-05-13 09:35:07.000000 PyTraffic-1.0.3/PyTraffic.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      343 2023-05-13 09:35:07.000000 PyTraffic-1.0.3/PyTraffic.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 09:35:07.000000 PyTraffic-1.0.3/PyTraffic.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       40 2023-05-13 09:35:07.000000 PyTraffic-1.0.3/PyTraffic.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 09:35:07.000000 PyTraffic-1.0.3/PyTraffic.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     3464 2023-05-13 09:32:18.000000 PyTraffic-1.0.3/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 09:35:07.927524 PyTraffic-1.0.3/setup.cfg
+-rw-rw-rw-   0        0        0     1050 2023-05-13 09:26:16.000000 PyTraffic-1.0.3/setup.py
```

### Comparing `PyTraffic-1.0.2/LICENSE.txt` & `PyTraffic-1.0.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.2/PyTraffic/Density.py` & `PyTraffic-1.0.3/PyTraffic/Density.py`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.2/PyTraffic/LicensePlate.py` & `PyTraffic-1.0.3/PyTraffic/LicensePlate.py`

 * *Files 17% similar despite different names*

```diff
@@ -7,16 +7,25 @@
 import numpy as np
 import pytesseract
 
 # Variables
 OpenCV = "OpenCV"
 Tesseract = "Tesseract"
 
-# Function 1 - Check License Plate
-def checkLicensePlate(method, path):
+# Function 1 - Check Tesseract
+def checkTesseract():
+    programs = []
+
+    for item in winapps.list_installed():
+        programs.append(item.name)
+
+    return "Tesseract-OCR - open source OCR engine" in programs
+
+# Function 2 - Check License Plate
+def checkLicensePlate(method, tesseractPath, path):
     if (os.path.exists(path)):
         if (method == "OpenCV"): # OpenCV
             # Reading the Image
             img = cv2.imread(path)
 
             # Converting the Images to Grayscale
             gray = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
@@ -32,63 +41,67 @@
                 gray_plates = gray[y:y+h, x:x+w]
                 color_plates = img[y:y+h, x:x+w]
 
                 cv2.imshow('Number Plate', gray_plates)
                 cv2.imshow('Number Plate Image', img)
                 cv2.waitKey(0)
         elif (method == "Tesseract"): # Tesseract
-            # Connecting to Tesseract
-            pytesseract.pytesseract.tesseract_cmd = "C:/Program Files/Tesseract-OCR/tesseract.exe"
+            # Check for Tesseract
+            if (os.path.exists(tesseractPath)):
+                # Connecting to Tesseract
+                pytesseract.pytesseract.tesseract_cmd = tesseractPath
+
+                # Reading the Image
+                img = cv2.imread(path, cv2.IMREAD_COLOR)
+                img = cv2.resize(img, (600,400))
+
+                # Converting the Images to Grayscale
+                gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) 
+                gray = cv2.bilateralFilter(gray, 13, 15, 15) 
+
+                # Finding Contours
+                edged = cv2.Canny(gray, 30, 200) 
+                contours = cv2.findContours(edged.copy(), cv2.RETR_TREE, cv2.CHAIN_APPROX_SIMPLE)
+                contours = imutils.grab_contours(contours)
+                contours = sorted(contours, key = cv2.contourArea, reverse = True)[:10]
+                screenCnt = None
+
+                for c in contours:
+                    peri = cv2.arcLength(c, True)
+                    approx = cv2.approxPolyDP(c, 0.018 * peri, True)
+
+                    if len(approx) == 4:
+                        screenCnt = approx
+                        break
+
+                if screenCnt is None:
+                    detected = 0
+                else:
+                    detected = 1
+
+                if detected == 1:
+                    cv2.drawContours(img, [screenCnt], -1, (0, 0, 255), 3)
+
+                mask = np.zeros(gray.shape,np.uint8)
+                new_image = cv2.drawContours(mask,[screenCnt],0,255,-1,)
+                new_image = cv2.bitwise_and(img,img,mask=mask)
+
+                (x, y) = np.where(mask == 255)
+                (topx, topy) = (np.min(x), np.min(y))
+                (bottomx, bottomy) = (np.max(x), np.max(y))
+                Cropped = gray[topx:bottomx+1, topy:bottomy+1]
 
-            # Reading the Image
-            img = cv2.imread(path, cv2.IMREAD_COLOR)
-            img = cv2.resize(img, (600,400))
+                # License Plate Number
+                text = pytesseract.image_to_string(Cropped, config='--psm 11')
 
-            # Converting the Images to Grayscale
-            gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) 
-            gray = cv2.bilateralFilter(gray, 13, 15, 15) 
-
-            # Finding Contours
-            edged = cv2.Canny(gray, 30, 200) 
-            contours = cv2.findContours(edged.copy(), cv2.RETR_TREE, cv2.CHAIN_APPROX_SIMPLE)
-            contours = imutils.grab_contours(contours)
-            contours = sorted(contours, key = cv2.contourArea, reverse = True)[:10]
-            screenCnt = None
-
-            for c in contours:
-                peri = cv2.arcLength(c, True)
-                approx = cv2.approxPolyDP(c, 0.018 * peri, True)
-
-                if len(approx) == 4:
-                    screenCnt = approx
-                    break
+                # Close OpenCV
+                cv2.waitKey(0)
+                cv2.destroyAllWindows()
 
-            if screenCnt is None:
-                detected = 0
+                # Return the License Plate Number
+                return text
             else:
-                detected = 1
-
-            if detected == 1:
-                cv2.drawContours(img, [screenCnt], -1, (0, 0, 255), 3)
-
-            mask = np.zeros(gray.shape,np.uint8)
-            new_image = cv2.drawContours(mask,[screenCnt],0,255,-1,)
-            new_image = cv2.bitwise_and(img,img,mask=mask)
-
-            (x, y) = np.where(mask == 255)
-            (topx, topy) = (np.min(x), np.min(y))
-            (bottomx, bottomy) = (np.max(x), np.max(y))
-            Cropped = gray[topx:bottomx+1, topy:bottomy+1]
-
-            # License Plate Number
-            text = pytesseract.image_to_string(Cropped, config='--psm 11')
-
-            # Close OpenCV
-            cv2.waitKey(0)
-            cv2.destroyAllWindows()
-
-            # Return the License Plate Number
-            return text
+                raise Exception("The 'tesseract.exe' file path does not exist. Make sure Tesseract-OCR is installed and the path given is correct.")
         else:
             raise Exception("Please use a valid method for identifying the license plate numbers.")
     else:
         raise Exception("The file path does not exist.")
```

### Comparing `PyTraffic-1.0.2/PyTraffic/models/cars.xml` & `PyTraffic-1.0.3/PyTraffic/models/cars.xml`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.2/PyTraffic/models/license_plate_opencv.xml` & `PyTraffic-1.0.3/PyTraffic/models/license_plate_opencv.xml`

 * *Files identical despite different names*

### Comparing `PyTraffic-1.0.2/README.md` & `PyTraffic-1.0.3/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 PyTraffic is a Python module to work on traffic-related functions and use cases.
 
 Read the docs on GitBook [here](https://aniketh-chavare.gitbook.io/pytraffic-docs).
 
 ## Module Information
 
 **Name** - PyTraffic</br>
-**Version** - 1.0.2</br>
+**Version** - 1.0.3</br>
 **Description** - PyTraffic is a Python module to work on traffic-related functions and use cases.</br>
 **Author** - Aniketh Chavare</br>
 **GitHub URL** - [https://github.com/Anikethc/PyTraffic](https://github.com/Anikethc/PyTraffic)</br>
 **Pypi.org URL** - [https://pypi.org/project/PyTraffic](https://pypi.org/project/PyTraffic)</br>
 **Docs URL** - [https://aniketh-chavare.gitbook.io/pytraffic-docs](https://aniketh-chavare.gitbook.io/pytraffic-docs)
 
 ## License
@@ -38,25 +38,45 @@
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 SOFTWARE.
 
 ## Credits
 
-This Python module uses open source components and packages. You can find the source code of their open source projects along with the license info below. I'm grateful to these developers for their contribution.
+This Python module uses open source components, libraries, modules, and packages. You can find the source code and license of their open source projects below, along with other information. I'm grateful to these developers for their contribution.
 
 **Project**: Tutorial (Web Page)<br>
 **Used For**: LicensePlate (Sub-Module)<br>
 **Author**: Shahid Akhtar Khan<br>
 **Link**: Visit [here](https://www.tutorialspoint.com/how-to-detect-license-plates-using-opencv-python) to check out the tutorial.<br>
 
 **Project**: Tutorial (Web Page)<br>
 **Used For**: LicensePlate (Sub-Module)<br>
 **Author**: Denis Kuria<br>
-**Link**: Visit [here](https://www.makeuseof.com/python-car-license-plates-detect-and-recognize) to check out the tutorial.
+**Link**: Visit [here](https://www.makeuseof.com/python-car-license-plates-detect-and-recognize).<br>
+
+**Project**: Python Module (opencv-python)<br>
+**Used For**: LicensePlate and Density (Sub-Modules)<br>
+**Author**: OpenCV<br>
+**Link**: Visit [here](https://github.com/opencv/opencv-python).<br>
+
+**Project**: Python Module (imutils)<br>
+**Used For**: LicensePlate (Sub-Module)<br>
+**Author**: PyImageSearch<br>
+**Link**: Visit [here](https://github.com/PyImageSearch/imutils).<br>
+
+**Project**: Python Module (Numpy)<br>
+**Used For**: LicensePlate (Sub-Module)<br>
+**Author**: Numpy.org<br>
+**Link**: Visit [here](https://github.com/numpy/numpy).<br>
+
+**Project**: Python Module (PyTesseract)<br>
+**Used For**: LicensePlate (Sub-Module)<br>
+**Author**: madmaze<br>
+**Link**: Visit [here](https://github.com/madmaze/pytesseract).<br>
 
 ## Issues & Bugs
 
 If you encounter any issues or bugs, visit the 'Issues' tab and create an issue. I'll look into it and resolve it ASAP.
 
 ## Conclusion
```

### Comparing `PyTraffic-1.0.2/setup.py` & `PyTraffic-1.0.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 # README.md
 with open("README.md") as readme_file:
     README = readme_file.read()
 
 # Setup Arguements
 setup_args = dict (
     name="PyTraffic",
-    version="1.0.2",
+    version="1.0.3",
     description="PyTraffic is a Python module to work on traffic-related functions and use cases.",
     long_description_content_type="text/markdown",
     long_description=README,
     license="MIT",
     packages=find_packages(),
     include_package_data=True,
     author="Aniketh Chavare",
```

