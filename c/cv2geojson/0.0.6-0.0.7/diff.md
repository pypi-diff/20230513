# Comparing `tmp/cv2geojson-0.0.6.tar.gz` & `tmp/cv2geojson-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cv2geojson-0.0.6.tar", last modified: Sat May 13 12:37:23 2023, max compression
+gzip compressed data, was "cv2geojson-0.0.7.tar", last modified: Sat May 13 12:49:39 2023, max compression
```

## Comparing `cv2geojson-0.0.6.tar` & `cv2geojson-0.0.7.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 12:37:23.597352 cv2geojson-0.0.6/
--rw-rw-rw-   0        0        0     1090 2023-04-04 10:50:06.000000 cv2geojson-0.0.6/LICENSE
--rw-rw-rw-   0        0        0     2902 2023-05-13 12:37:23.597352 cv2geojson-0.0.6/PKG-INFO
--rw-rw-rw-   0        0        0     2165 2023-05-13 12:26:09.000000 cv2geojson-0.0.6/README.md
--rw-rw-rw-   0        0        0      774 2023-05-13 12:37:02.000000 cv2geojson-0.0.6/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-13 12:37:23.597352 cv2geojson-0.0.6/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-05-13 12:37:23.581721 cv2geojson-0.0.6/src/
-drwxrwxrwx   0        0        0        0 2023-05-13 12:37:23.581721 cv2geojson-0.0.6/src/cv2geojson/
--rw-rw-rw-   0        0        0    12518 2023-05-13 11:18:59.000000 cv2geojson-0.0.6/src/cv2geojson/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 12:37:23.597352 cv2geojson-0.0.6/src/cv2geojson.egg-info/
--rw-rw-rw-   0        0        0     2902 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      248 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       28 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 12:49:39.192893 cv2geojson-0.0.7/
+-rw-rw-rw-   0        0        0     1090 2023-04-04 10:50:06.000000 cv2geojson-0.0.7/LICENSE
+-rw-rw-rw-   0        0        0     2989 2023-05-13 12:49:39.192893 cv2geojson-0.0.7/PKG-INFO
+-rw-rw-rw-   0        0        0     2252 2023-05-13 12:45:01.000000 cv2geojson-0.0.7/README.md
+-rw-rw-rw-   0        0        0      774 2023-05-13 12:46:38.000000 cv2geojson-0.0.7/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 12:49:39.192893 cv2geojson-0.0.7/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 12:49:39.168217 cv2geojson-0.0.7/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 12:49:39.168217 cv2geojson-0.0.7/src/cv2geojson/
+-rw-rw-rw-   0        0        0    12518 2023-05-13 11:18:59.000000 cv2geojson-0.0.7/src/cv2geojson/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:49:39.192893 cv2geojson-0.0.7/src/cv2geojson.egg-info/
+-rw-rw-rw-   0        0        0     2989 2023-05-13 12:49:39.000000 cv2geojson-0.0.7/src/cv2geojson.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      248 2023-05-13 12:49:39.000000 cv2geojson-0.0.7/src/cv2geojson.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 12:49:39.000000 cv2geojson-0.0.7/src/cv2geojson.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       28 2023-05-13 12:49:39.000000 cv2geojson-0.0.7/src/cv2geojson.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 12:49:39.000000 cv2geojson-0.0.7/src/cv2geojson.egg-info/top_level.txt
```

### Comparing `cv2geojson-0.0.6/LICENSE` & `cv2geojson-0.0.7/LICENSE`

 * *Files identical despite different names*

### Comparing `cv2geojson-0.0.6/PKG-INFO` & `cv2geojson-0.0.7/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cv2geojson
-Version: 0.0.6
+Version: 0.0.7
 Summary: Export contour annotations as geojson formatted data
 Author-email: Mohsen Farzi <mhnfarzi@gmail.com>
 Project-URL: Homepage, https://github.com/mfarzi/cv2geojson
 Project-URL: Bug Tracker, https://github.com/mfarzi/cv2geojson/issues
 Keywords: python,geojson,opencv,contours,polygons
 Classifier: Development Status :: 1 - Planning
 Classifier: Programming Language :: Python :: 3
@@ -13,20 +13,20 @@
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # cv2geojson
-cv2geojson is an open source project to export annotation contours extracted using [OpenCV-python](https://github.com/opencv/opencv-python) package to [GeoJSON](https://pypi.org/project/geojson/) format.
+cv2geojson is an open-source project to export annotation contours extracted using [OpenCV-python](https://github.com/opencv/opencv-python) package to [GeoJSON](https://pypi.org/project/geojson/) format.
 
 ## Introduction
-In digital pathology, images are often quite large and dedicated software tools like [QuPath](https://qupath.github.io/) are required to aid visualisation. The python package cv2geojson export contours detected using `cv2.findContours` as polygons using GeoJSON format for visualisation in QuPath. For example, download the whole slide image with tissue sample ID _GTEX-12584-1526_ from [histology page](https://gtexportal.org/home/histologyPage). This image has 45,815x38,091 pixels which requires about 5GB of storage uncompressed. Rather than storing a binary mask for the foreground segmentation, the mask can be converted to polygons and stored as a geojson file. The image below shows a snapshot from the QuPath software. The foreground contour is in blue.
+In digital pathology, images are often quite large and dedicated software tools like [QuPath](https://qupath.github.io/) are required to aid visualisation. The python package cv2geojson export contours detected using `cv2.findContours` as polygons using GeoJSON format for visualisation in QuPath. For example, download the whole slide image with tissue sample ID _GTEX-12584-1526_ from [histology page](https://gtexportal.org/home/histologyPage). This image has 45,815x38,091 pixels which requires about 5GB of storage uncompressed. Rather than storing a binary mask for the foreground segmentation, the mask can be converted to polygons and stored as a geojson file. The image below shows a snapshot from the QuPath software. The foreground contour is blue.
 <figure style="margin:0; padding:0;">
-  <img src="./example/GTEX-12584-1526-snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
+  <img src="https://github.com/mfarzi/cv2geojson/blob/main/example/GTEX-12584-1526-snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
   <figcaption>Snapshot from QuPath software visualising foreground segmentation</figcaption>
 </figure>
 
 ## Installation
 The recommended way to install is via pip:
 
 `pip install cv2geojson`
@@ -46,10 +46,10 @@
 
 # convert geocontours to geojson.Feature format
 features = [contour.export_feature(color=(0, 255, 0), label='roi') for contour in geocontours]
 export_annotations(features, './example/img_01.geojson')
 ```
 
 <figure style="margin:0; padding:0;">
-  <img src="./example/img_01_snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
+  <img src="https://github.com/mfarzi/cv2geojson/blob/main/example/img_01_snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
   <figcaption>Snapshot from QuPath software visualising foreground segmentation</figcaption>
 </figure>
```

### Comparing `cv2geojson-0.0.6/README.md` & `cv2geojson-0.0.7/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 # cv2geojson
-cv2geojson is an open source project to export annotation contours extracted using [OpenCV-python](https://github.com/opencv/opencv-python) package to [GeoJSON](https://pypi.org/project/geojson/) format.
+cv2geojson is an open-source project to export annotation contours extracted using [OpenCV-python](https://github.com/opencv/opencv-python) package to [GeoJSON](https://pypi.org/project/geojson/) format.
 
 ## Introduction
-In digital pathology, images are often quite large and dedicated software tools like [QuPath](https://qupath.github.io/) are required to aid visualisation. The python package cv2geojson export contours detected using `cv2.findContours` as polygons using GeoJSON format for visualisation in QuPath. For example, download the whole slide image with tissue sample ID _GTEX-12584-1526_ from [histology page](https://gtexportal.org/home/histologyPage). This image has 45,815x38,091 pixels which requires about 5GB of storage uncompressed. Rather than storing a binary mask for the foreground segmentation, the mask can be converted to polygons and stored as a geojson file. The image below shows a snapshot from the QuPath software. The foreground contour is in blue.
+In digital pathology, images are often quite large and dedicated software tools like [QuPath](https://qupath.github.io/) are required to aid visualisation. The python package cv2geojson export contours detected using `cv2.findContours` as polygons using GeoJSON format for visualisation in QuPath. For example, download the whole slide image with tissue sample ID _GTEX-12584-1526_ from [histology page](https://gtexportal.org/home/histologyPage). This image has 45,815x38,091 pixels which requires about 5GB of storage uncompressed. Rather than storing a binary mask for the foreground segmentation, the mask can be converted to polygons and stored as a geojson file. The image below shows a snapshot from the QuPath software. The foreground contour is blue.
 <figure style="margin:0; padding:0;">
-  <img src="./example/GTEX-12584-1526-snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
+  <img src="https://github.com/mfarzi/cv2geojson/blob/main/example/GTEX-12584-1526-snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
   <figcaption>Snapshot from QuPath software visualising foreground segmentation</figcaption>
 </figure>
 
 ## Installation
 The recommended way to install is via pip:
 
 `pip install cv2geojson`
@@ -28,10 +28,10 @@
 
 # convert geocontours to geojson.Feature format
 features = [contour.export_feature(color=(0, 255, 0), label='roi') for contour in geocontours]
 export_annotations(features, './example/img_01.geojson')
 ```
 
 <figure style="margin:0; padding:0;">
-  <img src="./example/img_01_snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
+  <img src="https://github.com/mfarzi/cv2geojson/blob/main/example/img_01_snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
   <figcaption>Snapshot from QuPath software visualising foreground segmentation</figcaption>
 </figure>
```

### Comparing `cv2geojson-0.0.6/pyproject.toml` & `cv2geojson-0.0.7/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "cv2geojson"
-version = "0.0.6"
+version = "0.0.7"
 authors = [
   { name="Mohsen Farzi", email="mhnfarzi@gmail.com" },
 ]
 description = "Export contour annotations as geojson formatted data"
 readme = "README.md"
 requires-python = ">=3.7"
 dependencies=['opencv-python', 'numpy', 'geojson']
```

### Comparing `cv2geojson-0.0.6/src/cv2geojson/__init__.py` & `cv2geojson-0.0.7/src/cv2geojson/__init__.py`

 * *Files identical despite different names*

### Comparing `cv2geojson-0.0.6/src/cv2geojson.egg-info/PKG-INFO` & `cv2geojson-0.0.7/src/cv2geojson.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cv2geojson
-Version: 0.0.6
+Version: 0.0.7
 Summary: Export contour annotations as geojson formatted data
 Author-email: Mohsen Farzi <mhnfarzi@gmail.com>
 Project-URL: Homepage, https://github.com/mfarzi/cv2geojson
 Project-URL: Bug Tracker, https://github.com/mfarzi/cv2geojson/issues
 Keywords: python,geojson,opencv,contours,polygons
 Classifier: Development Status :: 1 - Planning
 Classifier: Programming Language :: Python :: 3
@@ -13,20 +13,20 @@
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # cv2geojson
-cv2geojson is an open source project to export annotation contours extracted using [OpenCV-python](https://github.com/opencv/opencv-python) package to [GeoJSON](https://pypi.org/project/geojson/) format.
+cv2geojson is an open-source project to export annotation contours extracted using [OpenCV-python](https://github.com/opencv/opencv-python) package to [GeoJSON](https://pypi.org/project/geojson/) format.
 
 ## Introduction
-In digital pathology, images are often quite large and dedicated software tools like [QuPath](https://qupath.github.io/) are required to aid visualisation. The python package cv2geojson export contours detected using `cv2.findContours` as polygons using GeoJSON format for visualisation in QuPath. For example, download the whole slide image with tissue sample ID _GTEX-12584-1526_ from [histology page](https://gtexportal.org/home/histologyPage). This image has 45,815x38,091 pixels which requires about 5GB of storage uncompressed. Rather than storing a binary mask for the foreground segmentation, the mask can be converted to polygons and stored as a geojson file. The image below shows a snapshot from the QuPath software. The foreground contour is in blue.
+In digital pathology, images are often quite large and dedicated software tools like [QuPath](https://qupath.github.io/) are required to aid visualisation. The python package cv2geojson export contours detected using `cv2.findContours` as polygons using GeoJSON format for visualisation in QuPath. For example, download the whole slide image with tissue sample ID _GTEX-12584-1526_ from [histology page](https://gtexportal.org/home/histologyPage). This image has 45,815x38,091 pixels which requires about 5GB of storage uncompressed. Rather than storing a binary mask for the foreground segmentation, the mask can be converted to polygons and stored as a geojson file. The image below shows a snapshot from the QuPath software. The foreground contour is blue.
 <figure style="margin:0; padding:0;">
-  <img src="./example/GTEX-12584-1526-snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
+  <img src="https://github.com/mfarzi/cv2geojson/blob/main/example/GTEX-12584-1526-snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
   <figcaption>Snapshot from QuPath software visualising foreground segmentation</figcaption>
 </figure>
 
 ## Installation
 The recommended way to install is via pip:
 
 `pip install cv2geojson`
@@ -46,10 +46,10 @@
 
 # convert geocontours to geojson.Feature format
 features = [contour.export_feature(color=(0, 255, 0), label='roi') for contour in geocontours]
 export_annotations(features, './example/img_01.geojson')
 ```
 
 <figure style="margin:0; padding:0;">
-  <img src="./example/img_01_snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
+  <img src="https://github.com/mfarzi/cv2geojson/blob/main/example/img_01_snapshot.png" alt="Image 1" style="width:30%; margin-right:10px;" />
   <figcaption>Snapshot from QuPath software visualising foreground segmentation</figcaption>
 </figure>
```

