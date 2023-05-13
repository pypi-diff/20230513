# Comparing `tmp/image_augs-2.3.11.tar.gz` & `tmp/image_augs-2.3.12.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/image_augs-2.3.11.tar", last modified: Thu Apr 27 06:02:50 2023, max compression
+gzip compressed data, was "image_augs-2.3.12.tar", last modified: Sat May 13 14:22:11 2023, max compression
```

## Comparing `image_augs-2.3.11.tar` & `image_augs-2.3.12.tar`

### file list

```diff
@@ -1,30 +1,30 @@
-drwxrwxr-x   0 souviks   (1001) souviks   (1001)        0 2023-04-27 06:02:50.000000 image_augs-2.3.11/
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     8571 2023-04-27 06:02:50.000000 image_augs-2.3.11/PKG-INFO
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     7990 2023-04-27 05:12:07.000000 image_augs-2.3.11/README.md
-drwxrwxr-x   0 souviks   (1001) souviks   (1001)        0 2023-04-27 06:02:50.000000 image_augs-2.3.11/classification/
--rw-rw-r--   0 souviks   (1001) souviks   (1001)        0 2023-03-29 09:58:53.000000 image_augs-2.3.11/classification/__init__.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     9929 2023-04-26 10:51:29.000000 image_augs-2.3.11/classification/classification_.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)    15771 2023-04-26 11:03:13.000000 image_augs-2.3.11/classification/classification_combined.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     2006 2023-03-27 09:44:23.000000 image_augs-2.3.11/classification/logging_util.py
-drwxrwxr-x   0 souviks   (1001) souviks   (1001)        0 2023-04-27 06:02:50.000000 image_augs-2.3.11/image_augs.egg-info/
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     8571 2023-04-27 06:02:50.000000 image_augs-2.3.11/image_augs.egg-info/PKG-INFO
--rw-rw-r--   0 souviks   (1001) souviks   (1001)      723 2023-04-27 06:02:50.000000 image_augs-2.3.11/image_augs.egg-info/SOURCES.txt
--rw-rw-r--   0 souviks   (1001) souviks   (1001)        1 2023-04-27 06:02:50.000000 image_augs-2.3.11/image_augs.egg-info/dependency_links.txt
--rw-rw-r--   0 souviks   (1001) souviks   (1001)      363 2023-04-27 06:02:50.000000 image_augs-2.3.11/image_augs.egg-info/requires.txt
--rw-rw-r--   0 souviks   (1001) souviks   (1001)       49 2023-04-27 06:02:50.000000 image_augs-2.3.11/image_augs.egg-info/top_level.txt
-drwxrwxr-x   0 souviks   (1001) souviks   (1001)        0 2023-04-27 06:02:50.000000 image_augs-2.3.11/instance_seg/
--rw-rw-r--   0 souviks   (1001) souviks   (1001)        0 2023-03-29 09:58:39.000000 image_augs-2.3.11/instance_seg/__init__.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)    18793 2023-04-26 13:30:48.000000 image_augs-2.3.11/instance_seg/augment_poly.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)    28585 2023-04-27 05:52:13.000000 image_augs-2.3.11/instance_seg/json_reader_poly.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     2133 2023-03-29 13:20:57.000000 image_augs-2.3.11/instance_seg/logging_util.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     4725 2023-04-27 05:51:37.000000 image_augs-2.3.11/instance_seg/utils_poly.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)      513 2023-03-30 08:41:48.000000 image_augs-2.3.11/instance_seg/yml_writer_poly.py
-drwxrwxr-x   0 souviks   (1001) souviks   (1001)        0 2023-04-27 06:02:50.000000 image_augs-2.3.11/object_detection_new/
--rw-rw-r--   0 souviks   (1001) souviks   (1001)        0 2022-11-01 10:58:34.000000 image_augs-2.3.11/object_detection_new/__init__.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)    18848 2023-04-26 13:09:06.000000 image_augs-2.3.11/object_detection_new/augmentation_rect.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     2133 2023-04-23 18:52:17.000000 image_augs-2.3.11/object_detection_new/logging_util.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)    27789 2023-04-27 05:52:16.000000 image_augs-2.3.11/object_detection_new/txt_reader_rect.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)     4804 2023-04-27 05:50:13.000000 image_augs-2.3.11/object_detection_new/utils_poly.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)      510 2023-04-25 08:31:35.000000 image_augs-2.3.11/object_detection_new/yml_writer_poly.py
--rw-rw-r--   0 souviks   (1001) souviks   (1001)       38 2023-04-27 06:02:50.000000 image_augs-2.3.11/setup.cfg
--rw-rw-r--   0 souviks   (1001) souviks   (1001)      998 2023-03-29 09:59:13.000000 image_augs-2.3.11/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.619026 image_augs-2.3.12/
+-rw-r--r--   0 runner    (1001) docker     (123)     8920 2023-05-13 14:22:11.619026 image_augs-2.3.12/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8339 2023-05-13 14:21:58.000000 image_augs-2.3.12/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.615026 image_augs-2.3.12/classification/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:21:58.000000 image_augs-2.3.12/classification/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9929 2023-05-13 14:21:58.000000 image_augs-2.3.12/classification/classification_.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15771 2023-05-13 14:21:58.000000 image_augs-2.3.12/classification/classification_combined.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-05-13 14:21:58.000000 image_augs-2.3.12/classification/logging_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.619026 image_augs-2.3.12/image_augs.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     8920 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      723 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      363 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-13 14:22:11.000000 image_augs-2.3.12/image_augs.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.619026 image_augs-2.3.12/instance_seg/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18793 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/augment_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28586 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/json_reader_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/logging_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4725 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/utils_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)      513 2023-05-13 14:21:58.000000 image_augs-2.3.12/instance_seg/yml_writer_poly.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:22:11.619026 image_augs-2.3.12/object_detection_new/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18848 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/augmentation_rect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/logging_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27789 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/txt_reader_rect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4804 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/utils_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)      510 2023-05-13 14:21:58.000000 image_augs-2.3.12/object_detection_new/yml_writer_poly.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:22:11.619026 image_augs-2.3.12/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      998 2023-05-13 14:21:58.000000 image_augs-2.3.12/setup.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `image_augs-2.3.11/PKG-INFO` & `image_augs-2.3.12/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -1,29 +1,23 @@
-Metadata-Version: 2.1
-Name: image_augs
-Version: 2.3.11
-Summary: Image Augs supports Augmentation for Object Detection , Instance Segmentation and classification tasks.
-Author: Souvik Saha
-Author-email: ssouvik.191@gmail.com
-Keywords: machine_learning,development,data_augmentations
-Classifier: Intended Audience :: Developers
-Classifier: Operating System :: OS Independent
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3.8
-Classifier: License :: OSI Approved :: MIT License
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
 
-# Image Augmentations
+# Image Augmentations 🚀
+***
+<img src='images\logo.png'>
 
-This is a bounding box level image augmentation tool, it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
+***
+This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
 
-### Create a folder first, inside that folder keep your image annotation folder.
+***
+##  Code Starts from here 
 
-### Create a virtual environment
+### 👩🏼‍💻Create a folder first, inside that folder keep your image annotation folder 👩🏼‍💻
+***
+<img src='images\3.jpg'>
+
+### 👩🏼‍💻 Create a virtual environment 👩🏼‍💻
 
 ```python
 
 pip install virtualenv
 #name your environment
 python3 -m venv <your env name>
 
@@ -31,50 +25,47 @@
 source <your env name>/bin/activate
 
 #activate the environment  --> for windows user
 <your env name>/Source/activate.ps1
 
 ```
 
-### Installation (for pip installation)
+### Installation (for pip installation) 🚀
 
 ```python
 pip install image_augs
 ```
 
-## After installation
+## After installation 🎯
+***
 
-**create a .py script inside your created folder**
+**Create a .py script inside your created folder**
 
 **This Script is for OBJECT DETECTION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 
 
 from object_detection_new.txt_reader_rect import RectAugmentation
 
-
-
-
-
 ################# image height and width combination  ##################
 
 # first combination --> for custom image size
 #  image_height = < custom image size > ; 640
 #  image_width = < custom image size > ; 320
 
 
 # second combination --> keep aspect ratio of the image
 #  image_height = 640
 #  image_width  = 'keep_aspect_ratio_False'
 
 # Third combination --> keeping original image height and width
-#  image_height = < keep_original_image_height >
-#  image_width = < keep_original_image_width >
+#  image_height = 'keep_original_image_height'
+#  image_width = 'keep_original_image_width'
 
 
 
 annotation_folder = 'your folder'
 new_aug_saved_folder = 'new saved folder'
 train_split = 0.90
 image_H = 640  #check above for height and width setting
@@ -126,44 +117,42 @@
 
                                  weather_change=True,weather_change_f=0.8), # add rain , fog , snow in your images
                                
                                 
 
 #results will be saved in < your given folder >
 ```
+***
 
 **This Script is for INSTANCE SEGMENTATION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 from instance_seg.json_reader_poly import PolygonAugmentation
 
 
-
-
 ################# image height and width combination  ##################
 
 # first combination --> for custom image size
 #  image_height = < custom image size > ; 640
 #  image_width = < custom image size > ; 320
 
 
 # second combination --> keep aspect ratio of the image
 #  image_height = 640
 #  image_width  = 'keep_aspect_ratio_False'
 
 # Third combination --> keeping original image height and width
-#  image_height = < keep_original_image_height >
-#  image_width = < keep_original_image_width >
+#  image_height = 'keep_original_image_height'
+#  image_width = 'keep_original_image_width'
 
 
 #### yolo ####
 # if yolo False then it will normalize all images and save it as txt , if false augmentations will be saved as json.
 
-
 annotation_folder = 'your data'
 new_aug_saved_folder = 'new saved dataset name'
 train_split = 0.70
 image_H = 640  #check above for height and width setting
 image_W = 'keep_aspect_ratio'
 yolo = True
 
@@ -210,14 +199,16 @@
                                     
                                  mix_aug=True, mix_aug_f=0.7,
                                     
                                  temperature_change=True, temperature_change_f=0.5,
                                  
                                  weather_change=True,weather_change_f=0.3)
 #results will be saved in < your given folder >
+***
+
 ```
 
 **This Script is for IMAGE CLASSIFICATION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 from classification.classification_combined import ImageAugmentHelper
@@ -262,18 +253,19 @@
     translation=True, translation_f=1.0,
 
     sharpen=True, sharpen_f=1.0,
     
     randomShadow=True, randomShadow_f=1.0
 )
 ```
+***
+Use github to clone [image_augmentations](https://github.com/Souviksaha1998/Image_augmentations) repo 🖥️
+Use instanceSeg_aug_script.py / classification_aug_script.py / objectDetection_augScript.py according to your needs.
 
-Use github to clone [image_augmentations](https://github.com/Souviksaha1998/Image_augmentations) repo.
-
-
+***
 
 
 ## Contributing
 Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
 
 ## License
 [MIT](https://choosealicense.com/licenses/mit/)
```

### Comparing `image_augs-2.3.11/README.md` & `image_augs-2.3.12/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,14 +1,38 @@
-# Image Augmentations
+Metadata-Version: 2.1
+Name: image_augs
+Version: 2.3.12
+Summary: Image Augs supports Augmentation for Object Detection , Instance Segmentation and classification tasks.
+Author: Souvik Saha
+Author-email: ssouvik.191@gmail.com
+Keywords: machine_learning,development,data_augmentations
+Classifier: Intended Audience :: Developers
+Classifier: Operating System :: OS Independent
+Classifier: Programming Language :: Python
+Classifier: Programming Language :: Python :: 3.8
+Classifier: License :: OSI Approved :: MIT License
+Requires-Python: >=3.7
+Description-Content-Type: text/markdown
+
+
+# Image Augmentations 🚀
+***
+<img src='images\logo.png'>
+
+***
+This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
+
+***
+##  Code Starts from here 
+
+### 👩🏼‍💻Create a folder first, inside that folder keep your image annotation folder 👩🏼‍💻
+***
+<img src='images\3.jpg'>
 
-This is a bounding box level image augmentation tool, it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
-
-### Create a folder first, inside that folder keep your image annotation folder.
-
-### Create a virtual environment
+### 👩🏼‍💻 Create a virtual environment 👩🏼‍💻
 
 ```python
 
 pip install virtualenv
 #name your environment
 python3 -m venv <your env name>
 
@@ -16,50 +40,47 @@
 source <your env name>/bin/activate
 
 #activate the environment  --> for windows user
 <your env name>/Source/activate.ps1
 
 ```
 
-### Installation (for pip installation)
+### Installation (for pip installation) 🚀
 
 ```python
 pip install image_augs
 ```
 
-## After installation
+## After installation 🎯
+***
 
-**create a .py script inside your created folder**
+**Create a .py script inside your created folder**
 
 **This Script is for OBJECT DETECTION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 
 
 from object_detection_new.txt_reader_rect import RectAugmentation
 
-
-
-
-
 ################# image height and width combination  ##################
 
 # first combination --> for custom image size
 #  image_height = < custom image size > ; 640
 #  image_width = < custom image size > ; 320
 
 
 # second combination --> keep aspect ratio of the image
 #  image_height = 640
 #  image_width  = 'keep_aspect_ratio_False'
 
 # Third combination --> keeping original image height and width
-#  image_height = < keep_original_image_height >
-#  image_width = < keep_original_image_width >
+#  image_height = 'keep_original_image_height'
+#  image_width = 'keep_original_image_width'
 
 
 
 annotation_folder = 'your folder'
 new_aug_saved_folder = 'new saved folder'
 train_split = 0.90
 image_H = 640  #check above for height and width setting
@@ -111,44 +132,42 @@
 
                                  weather_change=True,weather_change_f=0.8), # add rain , fog , snow in your images
                                
                                 
 
 #results will be saved in < your given folder >
 ```
+***
 
 **This Script is for INSTANCE SEGMENTATION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 from instance_seg.json_reader_poly import PolygonAugmentation
 
 
-
-
 ################# image height and width combination  ##################
 
 # first combination --> for custom image size
 #  image_height = < custom image size > ; 640
 #  image_width = < custom image size > ; 320
 
 
 # second combination --> keep aspect ratio of the image
 #  image_height = 640
 #  image_width  = 'keep_aspect_ratio_False'
 
 # Third combination --> keeping original image height and width
-#  image_height = < keep_original_image_height >
-#  image_width = < keep_original_image_width >
+#  image_height = 'keep_original_image_height'
+#  image_width = 'keep_original_image_width'
 
 
 #### yolo ####
 # if yolo False then it will normalize all images and save it as txt , if false augmentations will be saved as json.
 
-
 annotation_folder = 'your data'
 new_aug_saved_folder = 'new saved dataset name'
 train_split = 0.70
 image_H = 640  #check above for height and width setting
 image_W = 'keep_aspect_ratio'
 yolo = True
 
@@ -195,14 +214,16 @@
                                     
                                  mix_aug=True, mix_aug_f=0.7,
                                     
                                  temperature_change=True, temperature_change_f=0.5,
                                  
                                  weather_change=True,weather_change_f=0.3)
 #results will be saved in < your given folder >
+***
+
 ```
 
 **This Script is for IMAGE CLASSIFICATION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 from classification.classification_combined import ImageAugmentHelper
@@ -247,18 +268,19 @@
     translation=True, translation_f=1.0,
 
     sharpen=True, sharpen_f=1.0,
     
     randomShadow=True, randomShadow_f=1.0
 )
 ```
+***
+Use github to clone [image_augmentations](https://github.com/Souviksaha1998/Image_augmentations) repo 🖥️
+Use instanceSeg_aug_script.py / classification_aug_script.py / objectDetection_augScript.py according to your needs.
 
-Use github to clone [image_augmentations](https://github.com/Souviksaha1998/Image_augmentations) repo.
-
-
+***
 
 
 ## Contributing
 Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
 
 ## License
 [MIT](https://choosealicense.com/licenses/mit/)
```

### Comparing `image_augs-2.3.11/classification/classification_.py` & `image_augs-2.3.12/classification/classification_.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/classification/classification_combined.py` & `image_augs-2.3.12/classification/classification_combined.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/classification/logging_util.py` & `image_augs-2.3.12/classification/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/image_augs.egg-info/PKG-INFO` & `image_augs-2.3.12/image_augs.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,29 +1,38 @@
 Metadata-Version: 2.1
 Name: image-augs
-Version: 2.3.11
+Version: 2.3.12
 Summary: Image Augs supports Augmentation for Object Detection , Instance Segmentation and classification tasks.
 Author: Souvik Saha
 Author-email: ssouvik.191@gmail.com
 Keywords: machine_learning,development,data_augmentations
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.8
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 
-# Image Augmentations
 
-This is a bounding box level image augmentation tool, it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
+# Image Augmentations 🚀
+***
+<img src='images\logo.png'>
 
-### Create a folder first, inside that folder keep your image annotation folder.
+***
+This is a augemntation tool for Object Detection , Image classification and Instance Segmentation , it can perform 14 annotations. The important ones are rotation, affine, zooming in and out, noise, and blur. The augmentations were applied to a fraction of the data (40 - 50 percent of the images out of 100 can be augmented).When rotating or zooming in and out, the bounding box coordinates will also change as the image is rotated or zoomed.
 
-### Create a virtual environment
+***
+##  Code Starts from here 
+
+### 👩🏼‍💻Create a folder first, inside that folder keep your image annotation folder 👩🏼‍💻
+***
+<img src='images\3.jpg'>
+
+### 👩🏼‍💻 Create a virtual environment 👩🏼‍💻
 
 ```python
 
 pip install virtualenv
 #name your environment
 python3 -m venv <your env name>
 
@@ -31,50 +40,47 @@
 source <your env name>/bin/activate
 
 #activate the environment  --> for windows user
 <your env name>/Source/activate.ps1
 
 ```
 
-### Installation (for pip installation)
+### Installation (for pip installation) 🚀
 
 ```python
 pip install image_augs
 ```
 
-## After installation
+## After installation 🎯
+***
 
-**create a .py script inside your created folder**
+**Create a .py script inside your created folder**
 
 **This Script is for OBJECT DETECTION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 
 
 from object_detection_new.txt_reader_rect import RectAugmentation
 
-
-
-
-
 ################# image height and width combination  ##################
 
 # first combination --> for custom image size
 #  image_height = < custom image size > ; 640
 #  image_width = < custom image size > ; 320
 
 
 # second combination --> keep aspect ratio of the image
 #  image_height = 640
 #  image_width  = 'keep_aspect_ratio_False'
 
 # Third combination --> keeping original image height and width
-#  image_height = < keep_original_image_height >
-#  image_width = < keep_original_image_width >
+#  image_height = 'keep_original_image_height'
+#  image_width = 'keep_original_image_width'
 
 
 
 annotation_folder = 'your folder'
 new_aug_saved_folder = 'new saved folder'
 train_split = 0.90
 image_H = 640  #check above for height and width setting
@@ -126,44 +132,42 @@
 
                                  weather_change=True,weather_change_f=0.8), # add rain , fog , snow in your images
                                
                                 
 
 #results will be saved in < your given folder >
 ```
+***
 
 **This Script is for INSTANCE SEGMENTATION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 from instance_seg.json_reader_poly import PolygonAugmentation
 
 
-
-
 ################# image height and width combination  ##################
 
 # first combination --> for custom image size
 #  image_height = < custom image size > ; 640
 #  image_width = < custom image size > ; 320
 
 
 # second combination --> keep aspect ratio of the image
 #  image_height = 640
 #  image_width  = 'keep_aspect_ratio_False'
 
 # Third combination --> keeping original image height and width
-#  image_height = < keep_original_image_height >
-#  image_width = < keep_original_image_width >
+#  image_height = 'keep_original_image_height'
+#  image_width = 'keep_original_image_width'
 
 
 #### yolo ####
 # if yolo False then it will normalize all images and save it as txt , if false augmentations will be saved as json.
 
-
 annotation_folder = 'your data'
 new_aug_saved_folder = 'new saved dataset name'
 train_split = 0.70
 image_H = 640  #check above for height and width setting
 image_W = 'keep_aspect_ratio'
 yolo = True
 
@@ -210,14 +214,16 @@
                                     
                                  mix_aug=True, mix_aug_f=0.7,
                                     
                                  temperature_change=True, temperature_change_f=0.5,
                                  
                                  weather_change=True,weather_change_f=0.3)
 #results will be saved in < your given folder >
+***
+
 ```
 
 **This Script is for IMAGE CLASSIFICATION**
 
 ```python
 #import these modules in your created <scriptname>.py file
 from classification.classification_combined import ImageAugmentHelper
@@ -262,18 +268,19 @@
     translation=True, translation_f=1.0,
 
     sharpen=True, sharpen_f=1.0,
     
     randomShadow=True, randomShadow_f=1.0
 )
 ```
+***
+Use github to clone [image_augmentations](https://github.com/Souviksaha1998/Image_augmentations) repo 🖥️
+Use instanceSeg_aug_script.py / classification_aug_script.py / objectDetection_augScript.py according to your needs.
 
-Use github to clone [image_augmentations](https://github.com/Souviksaha1998/Image_augmentations) repo.
-
-
+***
 
 
 ## Contributing
 Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
 
 ## License
 [MIT](https://choosealicense.com/licenses/mit/)
```

### Comparing `image_augs-2.3.11/image_augs.egg-info/SOURCES.txt` & `image_augs-2.3.12/image_augs.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/instance_seg/augment_poly.py` & `image_augs-2.3.12/instance_seg/augment_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/instance_seg/json_reader_poly.py` & `image_augs-2.3.12/instance_seg/json_reader_poly.py`

 * *Files 0% similar despite different names*

```diff
@@ -118,15 +118,15 @@
                     
                         yield im_read , poly_on_image
 
         except Exception as e:
             logger.error(f'problem : Json converter  desc : {e}')       
                    
                   
-    def Combined_augmentation(self,im_read , poly_on_image, no_track,image_height=640 , image_width:Union[int,keep_aspect_ratio]=640, blur=True , blur_f = 0.5 , motionBlur = True , motion_blur_f = 0.5, rotate=True , rotate_f = 0.5 , noise=True,noise_f=0.5,perspective=True,perspective_f = 0.5,affine=True,affine_f=0.5,
+    def Combined_augmentation(self,im_read , poly_on_image, no_track,image_height=640 , image_width:Union[int,keep_aspect_ratio]=640,  blur=True , blur_f = 0.5 , motionBlur = True , motion_blur_f = 0.5, rotate=True , rotate_f = 0.5 , noise=True,noise_f=0.5,perspective=True,perspective_f = 0.5,affine=True,affine_f=0.5,
                               brightness=True,brightness_f=0.5,hue=True,hue_f=0.5,removesaturation=True,removesaturation_f=0.5,contrast=True,contrast_f=0.5,upflip=True,upflip_f=0.5,
                               shear=True ,shear_f=0.5, rotate90=True,rotate90_f = 0.5,blur_and_noise=True,blur_and_noise_f=0.5,image_cutout = True,image_cutout_f=0.5,
                               mix_aug=True,mix_aug_f=0.5,temperature_change=True,temperature_change_f=0.5,weather_change=True,weather_change_f=0.5):
         
         
         # combining all the augmentations here
         with concurrent.futures.ThreadPoolExecutor(max_workers=20) as executor:
```

### Comparing `image_augs-2.3.11/instance_seg/logging_util.py` & `image_augs-2.3.12/instance_seg/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/instance_seg/utils_poly.py` & `image_augs-2.3.12/instance_seg/utils_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/instance_seg/yml_writer_poly.py` & `image_augs-2.3.12/instance_seg/yml_writer_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/object_detection_new/augmentation_rect.py` & `image_augs-2.3.12/object_detection_new/augmentation_rect.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/object_detection_new/logging_util.py` & `image_augs-2.3.12/object_detection_new/logging_util.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/object_detection_new/txt_reader_rect.py` & `image_augs-2.3.12/object_detection_new/txt_reader_rect.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/object_detection_new/utils_poly.py` & `image_augs-2.3.12/object_detection_new/utils_poly.py`

 * *Files identical despite different names*

### Comparing `image_augs-2.3.11/setup.py` & `image_augs-2.3.12/setup.py`

 * *Files identical despite different names*

