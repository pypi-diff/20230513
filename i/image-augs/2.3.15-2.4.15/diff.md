# Comparing `tmp/image_augs-2.3.15.tar.gz` & `tmp/image_augs-2.4.15.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "image_augs-2.3.15.tar", last modified: Sat May 13 14:56:54 2023, max compression
+gzip compressed data, was "image_augs-2.4.15.tar", last modified: Sat May 13 15:04:35 2023, max compression
```

## Comparing `image_augs-2.3.15.tar` & `image_augs-2.4.15.tar`

### file list

```diff
@@ -1,30 +1,30 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:56:54.281346 image_augs-2.3.15/
--rw-r--r--   0 runner    (1001) docker     (123)     9255 2023-05-13 14:56:54.281346 image_augs-2.3.15/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8674 2023-05-13 14:56:46.000000 image_augs-2.3.15/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:56:54.277346 image_augs-2.3.15/classification/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:56:46.000000 image_augs-2.3.15/classification/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9929 2023-05-13 14:56:46.000000 image_augs-2.3.15/classification/classification_.py
--rw-r--r--   0 runner    (1001) docker     (123)    15771 2023-05-13 14:56:46.000000 image_augs-2.3.15/classification/classification_combined.py
--rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-05-13 14:56:46.000000 image_augs-2.3.15/classification/logging_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:56:54.277346 image_augs-2.3.15/image_augs.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     9255 2023-05-13 14:56:54.000000 image_augs-2.3.15/image_augs.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      723 2023-05-13 14:56:54.000000 image_augs-2.3.15/image_augs.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:56:54.000000 image_augs-2.3.15/image_augs.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      363 2023-05-13 14:56:54.000000 image_augs-2.3.15/image_augs.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-13 14:56:54.000000 image_augs-2.3.15/image_augs.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:56:54.277346 image_augs-2.3.15/instance_seg/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:56:46.000000 image_augs-2.3.15/instance_seg/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18793 2023-05-13 14:56:46.000000 image_augs-2.3.15/instance_seg/augment_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)    28586 2023-05-13 14:56:46.000000 image_augs-2.3.15/instance_seg/json_reader_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 14:56:46.000000 image_augs-2.3.15/instance_seg/logging_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     4725 2023-05-13 14:56:46.000000 image_augs-2.3.15/instance_seg/utils_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)      513 2023-05-13 14:56:46.000000 image_augs-2.3.15/instance_seg/yml_writer_poly.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:56:54.281346 image_augs-2.3.15/object_detection_new/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:56:46.000000 image_augs-2.3.15/object_detection_new/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18848 2023-05-13 14:56:46.000000 image_augs-2.3.15/object_detection_new/augmentation_rect.py
--rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 14:56:46.000000 image_augs-2.3.15/object_detection_new/logging_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    27789 2023-05-13 14:56:46.000000 image_augs-2.3.15/object_detection_new/txt_reader_rect.py
--rw-r--r--   0 runner    (1001) docker     (123)     4804 2023-05-13 14:56:46.000000 image_augs-2.3.15/object_detection_new/utils_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)      510 2023-05-13 14:56:46.000000 image_augs-2.3.15/object_detection_new/yml_writer_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:56:54.281346 image_augs-2.3.15/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      998 2023-05-13 14:56:46.000000 image_augs-2.3.15/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:04:35.515274 image_augs-2.4.15/
+-rw-r--r--   0 runner    (1001) docker     (123)     9482 2023-05-13 15:04:35.515274 image_augs-2.4.15/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8901 2023-05-13 15:04:23.000000 image_augs-2.4.15/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:04:35.507274 image_augs-2.4.15/classification/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:04:23.000000 image_augs-2.4.15/classification/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9929 2023-05-13 15:04:23.000000 image_augs-2.4.15/classification/classification_.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15771 2023-05-13 15:04:23.000000 image_augs-2.4.15/classification/classification_combined.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-05-13 15:04:23.000000 image_augs-2.4.15/classification/logging_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:04:35.507274 image_augs-2.4.15/image_augs.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     9482 2023-05-13 15:04:35.000000 image_augs-2.4.15/image_augs.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      723 2023-05-13 15:04:35.000000 image_augs-2.4.15/image_augs.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 15:04:35.000000 image_augs-2.4.15/image_augs.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      363 2023-05-13 15:04:35.000000 image_augs-2.4.15/image_augs.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-13 15:04:35.000000 image_augs-2.4.15/image_augs.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:04:35.511273 image_augs-2.4.15/instance_seg/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:04:23.000000 image_augs-2.4.15/instance_seg/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18793 2023-05-13 15:04:23.000000 image_augs-2.4.15/instance_seg/augment_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28586 2023-05-13 15:04:23.000000 image_augs-2.4.15/instance_seg/json_reader_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 15:04:23.000000 image_augs-2.4.15/instance_seg/logging_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4725 2023-05-13 15:04:23.000000 image_augs-2.4.15/instance_seg/utils_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)      513 2023-05-13 15:04:23.000000 image_augs-2.4.15/instance_seg/yml_writer_poly.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 15:04:35.515274 image_augs-2.4.15/object_detection_new/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 15:04:23.000000 image_augs-2.4.15/object_detection_new/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18848 2023-05-13 15:04:23.000000 image_augs-2.4.15/object_detection_new/augmentation_rect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 15:04:23.000000 image_augs-2.4.15/object_detection_new/logging_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27789 2023-05-13 15:04:23.000000 image_augs-2.4.15/object_detection_new/txt_reader_rect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4804 2023-05-13 15:04:23.000000 image_augs-2.4.15/object_detection_new/utils_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)      510 2023-05-13 15:04:23.000000 image_augs-2.4.15/object_detection_new/yml_writer_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 15:04:35.515274 image_augs-2.4.15/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      998 2023-05-13 15:04:23.000000 image_augs-2.4.15/setup.py
```

### Comparing `image_augs-2.3.15/PKG-INFO` & `image_augs-2.4.15/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: image_augs
-Version: 2.3.15
+Version: 2.4.15
 Summary: Image Augs supports Augmentation for Object Detection , Instance Segmentation and classification tasks.
 Author: Souvik Saha
 Author-email: ssouvik.191@gmail.com
 Keywords: machine_learning,development,data_augmentations
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
@@ -17,18 +17,20 @@
 # Image Augmentations 🚀
 ***
 <img src='images\logo.png'>
 
 ***
 <img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/Souviksaha1998/Image_augmentations">
 
-<img alt="GitHub code size in bytes" src="https://static.pepy.tech/personalized-badge/image-augs?period=total&units=international_system&left_color=black&right_color=brightgreen&left_text=Downloadsq">
-
+<img alt="GitHub code size in bytes" src="https://static.pepy.tech/personalized-badge/image-augs?period=total&units=international_system&left_color=black&right_color=brightgreen&left_text=Downloads">
 
+<img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/Souviksaha1998/Image_augmentations?style=plastic">
+<img alt="GitHub followers" src="https://img.shields.io/github/followers/Souviksaha1998?style=plastic">
 
+***
 
 This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
 
 ***
 ##  Code Starts from here 
 
 ### 👩🏼‍💻Create a folder first, inside that folder keep your image annotation folder 👩🏼‍💻
```

### Comparing `image_augs-2.3.15/README.md` & `image_augs-2.4.15/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -2,18 +2,20 @@
 # Image Augmentations 🚀
 ***
 <img src='images\logo.png'>
 
 ***
 <img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/Souviksaha1998/Image_augmentations">
 
-<img alt="GitHub code size in bytes" src="https://static.pepy.tech/personalized-badge/image-augs?period=total&units=international_system&left_color=black&right_color=brightgreen&left_text=Downloadsq">
-
+<img alt="GitHub code size in bytes" src="https://static.pepy.tech/personalized-badge/image-augs?period=total&units=international_system&left_color=black&right_color=brightgreen&left_text=Downloads">
 
+<img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/Souviksaha1998/Image_augmentations?style=plastic">
+<img alt="GitHub followers" src="https://img.shields.io/github/followers/Souviksaha1998?style=plastic">
 
+***
 
 This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
 
 ***
 ##  Code Starts from here 
 
 ### 👩🏼‍💻Create a folder first, inside that folder keep your image annotation folder 👩🏼‍💻
```

### Comparing `image_augs-2.3.15/classification/classification_.py` & `image_augs-2.4.15/classification/classification_.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/classification/classification_combined.py` & `image_augs-2.4.15/classification/classification_combined.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/classification/logging_util.py` & `image_augs-2.4.15/classification/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/image_augs.egg-info/PKG-INFO` & `image_augs-2.4.15/image_augs.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: image-augs
-Version: 2.3.15
+Version: 2.4.15
 Summary: Image Augs supports Augmentation for Object Detection , Instance Segmentation and classification tasks.
 Author: Souvik Saha
 Author-email: ssouvik.191@gmail.com
 Keywords: machine_learning,development,data_augmentations
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
@@ -17,18 +17,20 @@
 # Image Augmentations 🚀
 ***
 <img src='images\logo.png'>
 
 ***
 <img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/Souviksaha1998/Image_augmentations">
 
-<img alt="GitHub code size in bytes" src="https://static.pepy.tech/personalized-badge/image-augs?period=total&units=international_system&left_color=black&right_color=brightgreen&left_text=Downloadsq">
-
+<img alt="GitHub code size in bytes" src="https://static.pepy.tech/personalized-badge/image-augs?period=total&units=international_system&left_color=black&right_color=brightgreen&left_text=Downloads">
 
+<img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/Souviksaha1998/Image_augmentations?style=plastic">
+<img alt="GitHub followers" src="https://img.shields.io/github/followers/Souviksaha1998?style=plastic">
 
+***
 
 This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
 
 ***
 ##  Code Starts from here 
 
 ### 👩🏼‍💻Create a folder first, inside that folder keep your image annotation folder 👩🏼‍💻
```

### Comparing `image_augs-2.3.15/image_augs.egg-info/SOURCES.txt` & `image_augs-2.4.15/image_augs.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/instance_seg/augment_poly.py` & `image_augs-2.4.15/instance_seg/augment_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/instance_seg/json_reader_poly.py` & `image_augs-2.4.15/instance_seg/json_reader_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/instance_seg/logging_util.py` & `image_augs-2.4.15/instance_seg/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/instance_seg/utils_poly.py` & `image_augs-2.4.15/instance_seg/utils_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/instance_seg/yml_writer_poly.py` & `image_augs-2.4.15/instance_seg/yml_writer_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/object_detection_new/augmentation_rect.py` & `image_augs-2.4.15/object_detection_new/augmentation_rect.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/object_detection_new/logging_util.py` & `image_augs-2.4.15/object_detection_new/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/object_detection_new/txt_reader_rect.py` & `image_augs-2.4.15/object_detection_new/txt_reader_rect.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/object_detection_new/utils_poly.py` & `image_augs-2.4.15/object_detection_new/utils_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.15/setup.py` & `image_augs-2.4.15/setup.py`

 * *Files identical despite different names*

