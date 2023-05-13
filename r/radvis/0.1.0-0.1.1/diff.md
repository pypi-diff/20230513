# Comparing `tmp/radvis-0.1.0.tar.gz` & `tmp/radvis-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "radvis-0.1.0.tar", last modified: Sat May 13 14:25:02 2023, max compression
+gzip compressed data, was "radvis-0.1.1.tar", last modified: Sat May 13 14:33:47 2023, max compression
```

## Comparing `radvis-0.1.0.tar` & `radvis-0.1.1.tar`

### file list

```diff
@@ -1,38 +1,38 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.224509 radvis-0.1.0/
--rw-rw-rw-   0        0        0     1089 2023-04-22 03:52:40.000000 radvis-0.1.0/LICENSE
--rw-rw-rw-   0        0        0     2084 2023-05-13 14:25:02.224509 radvis-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0     1781 2023-05-13 14:05:22.000000 radvis-0.1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.187744 radvis-0.1.0/radvis/
--rw-rw-rw-   0        0        0      152 2023-05-09 04:13:22.000000 radvis-0.1.0/radvis/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.210988 radvis-0.1.0/radvis/image/
--rw-rw-rw-   0        0        0       56 2023-04-23 13:31:34.000000 radvis-0.1.0/radvis/image/__init__.py
--rw-rw-rw-   0        0        0      720 2023-04-23 13:36:03.000000 radvis-0.1.0/radvis/image/load.py
--rw-rw-rw-   0        0        0     1345 2023-05-13 13:29:04.000000 radvis-0.1.0/radvis/image/rad_dicom_image.py
--rw-rw-rw-   0        0        0     3312 2023-05-13 13:23:44.000000 radvis-0.1.0/radvis/image/rad_image.py
--rw-rw-rw-   0        0        0     1375 2023-05-13 13:28:40.000000 radvis-0.1.0/radvis/image/rad_nifti_image.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.214989 radvis-0.1.0/radvis/mesh/
--rw-rw-rw-   0        0        0      115 2023-04-23 03:21:29.000000 radvis-0.1.0/radvis/mesh/__init__.py
--rw-rw-rw-   0        0        0     1638 2023-05-09 03:22:52.000000 radvis-0.1.0/radvis/mesh/compute_mesh.py
--rw-rw-rw-   0        0        0     4074 2023-04-23 04:59:23.000000 radvis-0.1.0/radvis/mesh/rad_mesh.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.217499 radvis-0.1.0/radvis/visualize/
--rw-rw-rw-   0        0        0       60 2023-04-29 06:26:05.000000 radvis-0.1.0/radvis/visualize/__init__.py
--rw-rw-rw-   0        0        0     6601 2023-05-13 13:56:23.000000 radvis-0.1.0/radvis/visualize/rad_slicer.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.206797 radvis-0.1.0/radvis.egg-info/
--rw-rw-rw-   0        0        0     2084 2023-05-13 14:25:02.000000 radvis-0.1.0/radvis.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      676 2023-05-13 14:25:02.000000 radvis-0.1.0/radvis.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:25:02.000000 radvis-0.1.0/radvis.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      112 2023-05-13 14:25:02.000000 radvis-0.1.0/radvis.egg-info/requires.txt
--rw-rw-rw-   0        0        0       13 2023-05-13 14:25:02.000000 radvis-0.1.0/radvis.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 14:25:02.225510 radvis-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0      748 2023-05-13 14:19:47.000000 radvis-0.1.0/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.218505 radvis-0.1.0/tests/
--rw-rw-rw-   0        0        0        0 2023-04-22 04:25:04.000000 radvis-0.1.0/tests/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.219509 radvis-0.1.0/tests/mocks/
--rw-rw-rw-   0        0        0       40 2023-04-30 09:03:02.000000 radvis-0.1.0/tests/mocks/__init__.py
--rw-rw-rw-   0        0        0      281 2023-05-09 03:12:06.000000 radvis-0.1.0/tests/mocks/mock_rad_image.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.221516 radvis-0.1.0/tests/test_mesh/
--rw-rw-rw-   0        0        0        0 2023-04-23 02:35:32.000000 radvis-0.1.0/tests/test_mesh/__init__.py
--rw-rw-rw-   0        0        0     2248 2023-05-09 03:23:13.000000 radvis-0.1.0/tests/test_mesh/test_compute_mesh.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:25:02.223510 radvis-0.1.0/tests/test_visualize/
--rw-rw-rw-   0        0        0        0 2023-04-30 08:55:21.000000 radvis-0.1.0/tests/test_visualize/__init__.py
--rw-rw-rw-   0        0        0      924 2023-05-09 03:13:53.000000 radvis-0.1.0/tests/test_visualize/test_rad_slicer.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.521878 radvis-0.1.1/
+-rw-rw-rw-   0        0        0     1089 2023-04-22 03:52:40.000000 radvis-0.1.1/LICENSE
+-rw-rw-rw-   0        0        0     2513 2023-05-13 14:33:47.520878 radvis-0.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0     2210 2023-05-13 14:31:12.000000 radvis-0.1.1/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.497308 radvis-0.1.1/radvis/
+-rw-rw-rw-   0        0        0      152 2023-05-09 04:13:22.000000 radvis-0.1.1/radvis/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.508823 radvis-0.1.1/radvis/image/
+-rw-rw-rw-   0        0        0       56 2023-04-23 13:31:34.000000 radvis-0.1.1/radvis/image/__init__.py
+-rw-rw-rw-   0        0        0      720 2023-04-23 13:36:03.000000 radvis-0.1.1/radvis/image/load.py
+-rw-rw-rw-   0        0        0     1345 2023-05-13 13:29:04.000000 radvis-0.1.1/radvis/image/rad_dicom_image.py
+-rw-rw-rw-   0        0        0     3312 2023-05-13 13:23:44.000000 radvis-0.1.1/radvis/image/rad_image.py
+-rw-rw-rw-   0        0        0     1375 2023-05-13 13:28:40.000000 radvis-0.1.1/radvis/image/rad_nifti_image.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.511824 radvis-0.1.1/radvis/mesh/
+-rw-rw-rw-   0        0        0      115 2023-04-23 03:21:29.000000 radvis-0.1.1/radvis/mesh/__init__.py
+-rw-rw-rw-   0        0        0     1638 2023-05-09 03:22:52.000000 radvis-0.1.1/radvis/mesh/compute_mesh.py
+-rw-rw-rw-   0        0        0     4074 2023-04-23 04:59:23.000000 radvis-0.1.1/radvis/mesh/rad_mesh.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.513823 radvis-0.1.1/radvis/visualize/
+-rw-rw-rw-   0        0        0       60 2023-04-29 06:26:05.000000 radvis-0.1.1/radvis/visualize/__init__.py
+-rw-rw-rw-   0        0        0     6601 2023-05-13 13:56:23.000000 radvis-0.1.1/radvis/visualize/rad_slicer.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.504308 radvis-0.1.1/radvis.egg-info/
+-rw-rw-rw-   0        0        0     2513 2023-05-13 14:33:47.000000 radvis-0.1.1/radvis.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      676 2023-05-13 14:33:47.000000 radvis-0.1.1/radvis.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:33:47.000000 radvis-0.1.1/radvis.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      112 2023-05-13 14:33:47.000000 radvis-0.1.1/radvis.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       13 2023-05-13 14:33:47.000000 radvis-0.1.1/radvis.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:33:47.521878 radvis-0.1.1/setup.cfg
+-rw-rw-rw-   0        0        0      748 2023-05-13 14:32:31.000000 radvis-0.1.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.514824 radvis-0.1.1/tests/
+-rw-rw-rw-   0        0        0        0 2023-04-22 04:25:04.000000 radvis-0.1.1/tests/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.515823 radvis-0.1.1/tests/mocks/
+-rw-rw-rw-   0        0        0       40 2023-04-30 09:03:02.000000 radvis-0.1.1/tests/mocks/__init__.py
+-rw-rw-rw-   0        0        0      281 2023-05-09 03:12:06.000000 radvis-0.1.1/tests/mocks/mock_rad_image.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.517879 radvis-0.1.1/tests/test_mesh/
+-rw-rw-rw-   0        0        0        0 2023-04-23 02:35:32.000000 radvis-0.1.1/tests/test_mesh/__init__.py
+-rw-rw-rw-   0        0        0     2248 2023-05-09 03:23:13.000000 radvis-0.1.1/tests/test_mesh/test_compute_mesh.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:33:47.519878 radvis-0.1.1/tests/test_visualize/
+-rw-rw-rw-   0        0        0        0 2023-04-30 08:55:21.000000 radvis-0.1.1/tests/test_visualize/__init__.py
+-rw-rw-rw-   0        0        0      924 2023-05-09 03:13:53.000000 radvis-0.1.1/tests/test_visualize/test_rad_slicer.py
```

### Comparing `radvis-0.1.0/LICENSE` & `radvis-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/PKG-INFO` & `radvis-0.1.1/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -1,18 +1,7 @@
-Metadata-Version: 2.1
-Name: radvis
-Version: 0.1.0
-Summary: A visualization tool for medical images
-Home-page: https://github.com/medlee-code/RadVis
-Author: Matthew lee
-Author-email: matthewlee@medlee.io
-Requires-Python: >=3.10
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 # RadVis
 RadVis (Radiology Visualization) is a visualization tool for medical images.
 
 > Work in progress
 
 Currently implemented features:
 - Load both DICOM and NIFTI images
@@ -32,15 +21,15 @@
 # Creates a 'RadImage' object containing the image data
 image = rv.load_image('path/to/image.nii.gz')
 
 slicer = rv.RadSlicer(image, axis=0)
 
 slicer.display()
 ```
-![](images/example_0.gif)
+![](https://raw.githubusercontent.com/medlee-code/RadVis/main/images/example_0.gif?token=GHSAT0AAAAAACBJZC7OUK4KUWZ4QWBJIGJ6ZC7T4HA)
 
 Adding masks to the image
 ```python
 import radvis as rv
 import numpy as np
 
 image = rv.load_image('path/to/image.nii.gz')
@@ -55,15 +44,15 @@
 blue_mask[70:150, 70:150, 70:150] = 1
 
 slicer.add_mask(red_mask, color="red")
 slicer.add_mask(blue_mask, color="blue")
 
 slicer.display()
 ```
-![](images/example_mask_0.gif)
+![](https://raw.githubusercontent.com/medlee-code/RadVis/main/images/example_mask_0.gif?token=GHSAT0AAAAAACBJZC7OHBDQFXT7KM5L42NUZC7T4SQ))
 
 Mask can be another RadImage object so you can load up your masks from a DICOM or NIFTI
 ```python
 import radvis as rv
 import numpy as np
 
 AXIS = 1
@@ -77,10 +66,10 @@
 slicer.add_mask(mask, color="red", alpha=0.3)
 
 slicer.display()
 # slicer.save_animation(f"images/axis_{AXIS}_brain_seg.gif", fps=30)
 ```
 
 <p float="left">
-  <img src="images/axis_1_brain_seg.gif" width="49%" /> 
-  <img src="images/axis_2_brain_seg.gif" width="49%" />
-</p>
+  <img src="https://raw.githubusercontent.com/medlee-code/RadVis/main/images/axis_1_brain_seg.gif?token=GHSAT0AAAAAACBJZC7PZ2WT3CJ26PONDN2YZC7T46Q" width="49%" /> 
+  <img src="https://raw.githubusercontent.com/medlee-code/RadVis/main/images/axis_2_brain_seg.gif?token=GHSAT0AAAAAACBJZC7PDVRWL2CW2OCTUV3CZC7T5BQ" width="49%" />
+</p>
```

### Comparing `radvis-0.1.0/radvis/image/load.py` & `radvis-0.1.1/radvis/image/load.py`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/radvis/image/rad_dicom_image.py` & `radvis-0.1.1/radvis/image/rad_dicom_image.py`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/radvis/image/rad_image.py` & `radvis-0.1.1/radvis/image/rad_image.py`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/radvis/image/rad_nifti_image.py` & `radvis-0.1.1/radvis/image/rad_nifti_image.py`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/radvis/mesh/compute_mesh.py` & `radvis-0.1.1/radvis/mesh/compute_mesh.py`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/radvis/mesh/rad_mesh.py` & `radvis-0.1.1/radvis/mesh/rad_mesh.py`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/radvis/visualize/rad_slicer.py` & `radvis-0.1.1/radvis/visualize/rad_slicer.py`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/radvis.egg-info/PKG-INFO` & `radvis-0.1.1/PKG-INFO`

 * *Files 26% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: radvis
-Version: 0.1.0
+Version: 0.1.1
 Summary: A visualization tool for medical images
 Home-page: https://github.com/medlee-code/RadVis
 Author: Matthew lee
 Author-email: matthewlee@medlee.io
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -32,15 +32,15 @@
 # Creates a 'RadImage' object containing the image data
 image = rv.load_image('path/to/image.nii.gz')
 
 slicer = rv.RadSlicer(image, axis=0)
 
 slicer.display()
 ```
-![](images/example_0.gif)
+![](https://raw.githubusercontent.com/medlee-code/RadVis/main/images/example_0.gif?token=GHSAT0AAAAAACBJZC7OUK4KUWZ4QWBJIGJ6ZC7T4HA)
 
 Adding masks to the image
 ```python
 import radvis as rv
 import numpy as np
 
 image = rv.load_image('path/to/image.nii.gz')
@@ -55,15 +55,15 @@
 blue_mask[70:150, 70:150, 70:150] = 1
 
 slicer.add_mask(red_mask, color="red")
 slicer.add_mask(blue_mask, color="blue")
 
 slicer.display()
 ```
-![](images/example_mask_0.gif)
+![](https://raw.githubusercontent.com/medlee-code/RadVis/main/images/example_mask_0.gif?token=GHSAT0AAAAAACBJZC7OHBDQFXT7KM5L42NUZC7T4SQ))
 
 Mask can be another RadImage object so you can load up your masks from a DICOM or NIFTI
 ```python
 import radvis as rv
 import numpy as np
 
 AXIS = 1
@@ -77,10 +77,10 @@
 slicer.add_mask(mask, color="red", alpha=0.3)
 
 slicer.display()
 # slicer.save_animation(f"images/axis_{AXIS}_brain_seg.gif", fps=30)
 ```
 
 <p float="left">
-  <img src="images/axis_1_brain_seg.gif" width="49%" /> 
-  <img src="images/axis_2_brain_seg.gif" width="49%" />
+  <img src="https://raw.githubusercontent.com/medlee-code/RadVis/main/images/axis_1_brain_seg.gif?token=GHSAT0AAAAAACBJZC7PZ2WT3CJ26PONDN2YZC7T46Q" width="49%" /> 
+  <img src="https://raw.githubusercontent.com/medlee-code/RadVis/main/images/axis_2_brain_seg.gif?token=GHSAT0AAAAAACBJZC7PDVRWL2CW2OCTUV3CZC7T5BQ" width="49%" />
 </p>
```

### Comparing `radvis-0.1.0/radvis.egg-info/SOURCES.txt` & `radvis-0.1.1/radvis.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/setup.py` & `radvis-0.1.1/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setup(
     name='radvis',
-    version='0.1.0',
+    version='0.1.1',
     url='https://github.com/medlee-code/RadVis',
     author='Matthew lee',
     author_email='matthewlee@medlee.io',
     description='A visualization tool for medical images',
     long_description=long_description,
     long_description_content_type="text/markdown",
     packages=find_packages(),
```

### Comparing `radvis-0.1.0/tests/test_mesh/test_compute_mesh.py` & `radvis-0.1.1/tests/test_mesh/test_compute_mesh.py`

 * *Files identical despite different names*

### Comparing `radvis-0.1.0/tests/test_visualize/test_rad_slicer.py` & `radvis-0.1.1/tests/test_visualize/test_rad_slicer.py`

 * *Files identical despite different names*

