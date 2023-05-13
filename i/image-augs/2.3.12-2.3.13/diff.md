# Comparing `tmp/image_augs-2.3.12.tar.gz` & `tmp/image_augs-2.3.13.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "image_augs-2.3.12.tar", last modified: Sat May 13 14:22:11 2023, max compression
+gzip compressed data, was "image_augs-2.3.13.tar", last modified: Sat May 13 14:33:41 2023, max compression
```

## Comparing `image_augs-2.3.12.tar` & `image_augs-2.3.13.tar`

### file list

```diff
@@ -1,30 +1,30 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.619026 image_augs-2.3.12/
--rw-r--r--   0 runner    (1001) docker     (123)     8920 2023-05-13 14:22:11.619026 image_augs-2.3.12/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8339 2023-05-13 14:21:58.000000 image_augs-2.3.12/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.615026 image_augs-2.3.12/classification/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:21:58.000000 image_augs-2.3.12/classification/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9929 2023-05-13 14:21:58.000000 image_augs-2.3.12/classification/classification_.py
--rw-r--r--   0 runner    (1001) docker     (123)    15771 2023-05-13 14:21:58.000000 image_augs-2.3.12/classification/classification_combined.py
--rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-05-13 14:21:58.000000 image_augs-2.3.12/classification/logging_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.619026 image_augs-2.3.12/image_augs.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     8920 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      723 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      363 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.619026 image_augs-2.3.12/instance_seg/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18793 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/augment_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)    28586 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/json_reader_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/logging_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     4725 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/utils_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)      513 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/yml_writer_poly.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.619026 image_augs-2.3.12/object_detection_new/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18848 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/augmentation_rect.py
--rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/logging_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    27789 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/txt_reader_rect.py
--rw-r--r--   0 runner    (1001) docker     (123)     4804 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/utils_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)      510 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/yml_writer_poly.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:22:11.619026 image_augs-2.3.12/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      998 2023-05-13 14:21:58.000000 image_augs-2.3.12/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:41.097731 image_augs-2.3.13/
+-rw-r--r--   0 runner    (1001) docker     (123)     8921 2023-05-13 14:33:41.097731 image_augs-2.3.13/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8340 2023-05-13 14:33:31.000000 image_augs-2.3.13/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:41.093731 image_augs-2.3.13/classification/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:31.000000 image_augs-2.3.13/classification/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9929 2023-05-13 14:33:31.000000 image_augs-2.3.13/classification/classification_.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15771 2023-05-13 14:33:31.000000 image_augs-2.3.13/classification/classification_combined.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-05-13 14:33:31.000000 image_augs-2.3.13/classification/logging_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:41.093731 image_augs-2.3.13/image_augs.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     8921 2023-05-13 14:33:41.000000 image_augs-2.3.13/image_augs.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      723 2023-05-13 14:33:41.000000 image_augs-2.3.13/image_augs.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:33:41.000000 image_augs-2.3.13/image_augs.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      363 2023-05-13 14:33:41.000000 image_augs-2.3.13/image_augs.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-13 14:33:41.000000 image_augs-2.3.13/image_augs.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:41.093731 image_augs-2.3.13/instance_seg/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:31.000000 image_augs-2.3.13/instance_seg/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18793 2023-05-13 14:33:31.000000 image_augs-2.3.13/instance_seg/augment_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28586 2023-05-13 14:33:31.000000 image_augs-2.3.13/instance_seg/json_reader_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 14:33:31.000000 image_augs-2.3.13/instance_seg/logging_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4725 2023-05-13 14:33:31.000000 image_augs-2.3.13/instance_seg/utils_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)      513 2023-05-13 14:33:31.000000 image_augs-2.3.13/instance_seg/yml_writer_poly.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:41.093731 image_augs-2.3.13/object_detection_new/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:31.000000 image_augs-2.3.13/object_detection_new/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18848 2023-05-13 14:33:31.000000 image_augs-2.3.13/object_detection_new/augmentation_rect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 14:33:31.000000 image_augs-2.3.13/object_detection_new/logging_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27789 2023-05-13 14:33:31.000000 image_augs-2.3.13/object_detection_new/txt_reader_rect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4804 2023-05-13 14:33:31.000000 image_augs-2.3.13/object_detection_new/utils_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)      510 2023-05-13 14:33:31.000000 image_augs-2.3.13/object_detection_new/yml_writer_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:33:41.097731 image_augs-2.3.13/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      998 2023-05-13 14:33:31.000000 image_augs-2.3.13/setup.py
```

### Comparing `image_augs-2.3.12/PKG-INFO` & `image_augs-2.3.13/image_augs.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: image_augs
-Version: 2.3.12
+Name: image-augs
+Version: 2.3.13
 Summary: Image Augs supports Augmentation for Object Detection , Instance Segmentation and classification tasks.
 Author: Souvik Saha
 Author-email: ssouvik.191@gmail.com
 Keywords: machine_learning,development,data_augmentations
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
@@ -12,15 +12,16 @@
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 
 
 # Image Augmentations 🚀
 ***
-<img src='images\logo.png'>
+![Image 1](images\logo.png)
+
 
 ***
 This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
 
 ***
 ##  Code Starts from here
```

### Comparing `image_augs-2.3.12/README.md` & `image_augs-2.3.13/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 
 # Image Augmentations 🚀
 ***
-<img src='images\logo.png'>
+![Image 1](images\logo.png)
+
 
 ***
 This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
 
 ***
 ##  Code Starts from here
```

### Comparing `image_augs-2.3.12/classification/classification_.py` & `image_augs-2.3.13/classification/classification_.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/classification/classification_combined.py` & `image_augs-2.3.13/classification/classification_combined.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/classification/logging_util.py` & `image_augs-2.3.13/classification/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/image_augs.egg-info/PKG-INFO` & `image_augs-2.3.13/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: image-augs
-Version: 2.3.12
+Name: image_augs
+Version: 2.3.13
 Summary: Image Augs supports Augmentation for Object Detection , Instance Segmentation and classification tasks.
 Author: Souvik Saha
 Author-email: ssouvik.191@gmail.com
 Keywords: machine_learning,development,data_augmentations
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
@@ -12,15 +12,16 @@
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 
 
 # Image Augmentations 🚀
 ***
-<img src='images\logo.png'>
+![Image 1](images\logo.png)
+
 
 ***
 This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
 
 ***
 ##  Code Starts from here
```

### Comparing `image_augs-2.3.12/image_augs.egg-info/SOURCES.txt` & `image_augs-2.3.13/image_augs.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/instance_seg/augment_poly.py` & `image_augs-2.3.13/instance_seg/augment_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/instance_seg/json_reader_poly.py` & `image_augs-2.3.13/instance_seg/json_reader_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/instance_seg/logging_util.py` & `image_augs-2.3.13/instance_seg/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/instance_seg/utils_poly.py` & `image_augs-2.3.13/instance_seg/utils_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/instance_seg/yml_writer_poly.py` & `image_augs-2.3.13/instance_seg/yml_writer_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/object_detection_new/augmentation_rect.py` & `image_augs-2.3.13/object_detection_new/augmentation_rect.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/object_detection_new/logging_util.py` & `image_augs-2.3.13/object_detection_new/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/object_detection_new/txt_reader_rect.py` & `image_augs-2.3.13/object_detection_new/txt_reader_rect.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/object_detection_new/utils_poly.py` & `image_augs-2.3.13/object_detection_new/utils_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.12/setup.py` & `image_augs-2.3.13/setup.py`

 * *Files identical despite different names*

