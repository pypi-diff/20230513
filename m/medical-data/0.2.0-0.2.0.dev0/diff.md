# Comparing `tmp/medical_data-0.2.0.tar.gz` & `tmp/medical_data-0.2.0.dev0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "medical_data-0.2.0.tar", last modified: Sat May 13 17:53:33 2023, max compression
+gzip compressed data, was "medical_data-0.2.0.dev0.tar", last modified: Sat May 13 15:01:10 2023, max compression
```

## Comparing `medical_data-0.2.0.tar` & `medical_data-0.2.0.dev0.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:53:33.882869 medical_data-0.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-05-13 17:53:21.000000 medical_data-0.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    15862 2023-05-13 17:53:33.882869 medical_data-0.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2171 2023-05-13 17:53:21.000000 medical_data-0.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:53:33.878869 medical_data-0.2.0/medical_data/
--rw-r--r--   0 runner    (1001) docker     (123)     1403 2023-05-13 17:53:21.000000 medical_data-0.2.0/medical_data/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    55761 2023-05-13 17:53:21.000000 medical_data-0.2.0/medical_data/dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     3918 2023-05-13 17:53:21.000000 medical_data-0.2.0/medical_data/indexing.py
--rw-r--r--   0 runner    (1001) docker     (123)     1775 2023-05-13 17:53:21.000000 medical_data-0.2.0/medical_data/modality.py
--rw-r--r--   0 runner    (1001) docker     (123)     2813 2023-05-13 17:53:21.000000 medical_data-0.2.0/medical_data/moving_avg.py
--rw-r--r--   0 runner    (1001) docker     (123)     1312 2023-05-13 17:53:21.000000 medical_data-0.2.0/medical_data/single_class.py
--rw-r--r--   0 runner    (1001) docker     (123)    29773 2023-05-13 17:53:21.000000 medical_data-0.2.0/medical_data/transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     2300 2023-05-13 17:53:21.000000 medical_data-0.2.0/medical_data/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:53:33.882869 medical_data-0.2.0/medical_data.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    15862 2023-05-13 17:53:33.000000 medical_data-0.2.0/medical_data.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      483 2023-05-13 17:53:33.000000 medical_data-0.2.0/medical_data.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:53:33.000000 medical_data-0.2.0/medical_data.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      256 2023-05-13 17:53:33.000000 medical_data-0.2.0/medical_data.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 17:53:33.000000 medical_data-0.2.0/medical_data.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:53:33.000000 medical_data-0.2.0/medical_data.egg-info/zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)     1754 2023-05-13 17:53:21.000000 medical_data-0.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 17:53:33.882869 medical_data-0.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 17:53:21.000000 medical_data-0.2.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:53:33.878869 medical_data-0.2.0/tests/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:53:33.882869 medical_data-0.2.0/tests/data/
--rw-r--r--   0 runner    (1001) docker     (123)     1412 2023-05-13 17:53:21.000000 medical_data-0.2.0/tests/data/test_modality.py
+drwxrwxrwx   0 zeus      (1000) zeus      (1000)        0 2023-05-13 15:01:10.842398 medical_data-0.2.0.dev0/
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)    11357 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/LICENSE
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)    16294 2023-05-13 15:01:10.842398 medical_data-0.2.0.dev0/PKG-INFO
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     2598 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/README.md
+drwxrwxrwx   0 zeus      (1000) zeus      (1000)        0 2023-05-13 15:01:10.838398 medical_data-0.2.0.dev0/medical_data/
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     1406 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/medical_data/__init__.py
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)    55761 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/medical_data/dataset.py
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     3918 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/medical_data/indexing.py
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     1775 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/medical_data/modality.py
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     2813 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/medical_data/moving_avg.py
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     1312 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/medical_data/single_class.py
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)    29773 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/medical_data/transforms.py
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     2300 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/medical_data/utils.py
+drwxrwxrwx   0 zeus      (1000) zeus      (1000)        0 2023-05-13 15:01:10.842398 medical_data-0.2.0.dev0/medical_data.egg-info/
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)    16294 2023-05-13 15:01:10.000000 medical_data-0.2.0.dev0/medical_data.egg-info/PKG-INFO
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)      483 2023-05-13 15:01:10.000000 medical_data-0.2.0.dev0/medical_data.egg-info/SOURCES.txt
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)        1 2023-05-13 15:01:10.000000 medical_data-0.2.0.dev0/medical_data.egg-info/dependency_links.txt
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)      256 2023-05-13 15:01:10.000000 medical_data-0.2.0.dev0/medical_data.egg-info/requires.txt
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)       32 2023-05-13 15:01:10.000000 medical_data-0.2.0.dev0/medical_data.egg-info/top_level.txt
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)        1 2023-05-13 15:01:10.000000 medical_data-0.2.0.dev0/medical_data.egg-info/zip-safe
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     1754 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/pyproject.toml
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)       38 2023-05-13 15:01:10.842398 medical_data-0.2.0.dev0/setup.cfg
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)       38 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/setup.py
+drwxrwxrwx   0 zeus      (1000) zeus      (1000)        0 2023-05-13 15:01:10.830397 medical_data-0.2.0.dev0/tests/
+drwxrwxrwx   0 zeus      (1000) zeus      (1000)        0 2023-05-13 15:01:10.842398 medical_data-0.2.0.dev0/tests/data/
+-rw-rw-rw-   0 zeus      (1000) zeus      (1000)     1412 2023-05-13 15:00:10.000000 medical_data-0.2.0.dev0/tests/data/test_modality.py
```

### Comparing `medical_data-0.2.0/LICENSE` & `medical_data-0.2.0.dev0/LICENSE`

 * *Files identical despite different names*

### Comparing `medical_data-0.2.0/PKG-INFO` & `medical_data-0.2.0.dev0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: medical_data
-Version: 0.2.0
+Version: 0.2.0.dev0
 Summary: Helpful data utilities for deep learning in medical image analysis/medical image computing
 Author: Justus Schock
 Author-email: justus.schock@posteo.de
 Maintainer-email: Justus Schock <justus.schock@posteo.de>
 License:                                  Apache License
                                    Version 2.0, January 2004
                                 http://www.apache.org/licenses/
@@ -217,15 +217,15 @@
 Provides-Extra: test
 License-File: LICENSE
 
 # Medical Data
 
 [![UnitTest](https://github.com/justusschock/medical-data/actions/workflows/unittests.yaml/badge.svg)](https://github.com/justusschock/medicaldata/actions/workflows/unittests.yaml) [![Build Package](https://github.com/justusschock/medical-data/actions/workflows/package_build.yaml/badge.svg)](https://github.com/justusschock/medical-data/actions/workflows/package_build.yaml) ![PyPI](https://img.shields.io/pypi/v/medical-data?color=grene) [![pre-commit.ci status](https://results.pre-commit.ci/badge/github/justusschock/medical-data/main.svg)](https://results.pre-commit.ci/latest/github/justusschock/medical-data/main)
 
-This repository contains utilities for handling data in medical image analysis that are not specific to certain tasks.
+This repository contains utilities for training and evaluating deep learning models in medical image analysis that are not specific to certain tasks.
 
 So far it consists of 2 major parts:
 An abstract Dataset API built on top of `torch.utils.data.Dataset` and `torchio.data.Subject` as well as general transforms for this kind of data.
 
 To use the dataset classes, you basically only need to implement the `parse_subjects` method to return a list of samples and everything else will work automatically.
 You will automatically get image statistics such as median spacing or median shape. For label statistics, you either need to subclass the `AbstractDiscreteLabelDataset` or implement the `get_single_label_stats` and `aggregate_label_stats` methods.
 
@@ -237,28 +237,35 @@
 
 This project can be installed either from PyPI or by cloning the repository from GitHub.
 
 For an install of published packages, use the command
 
 ```bash
 
-    pip install medical-data
+    pip install medical-dl-utils
 
 ```
 
 To install from the (cloned) repository, use the command
 
 ```bash
 
-    pip install PATH/TO/medical-data
+    pip install PATH/TO/medical-dl-utils
 
 ```
 
 You can also add `-e` to the command to make an editable install in case you want to modify the code.
 
 You can also install the package directly from GitHub by running
 
 ```bash
 
-    pip install git+https://github.com/justusschock/medical-data.git
+    pip install git+https://github.com/justusschock/medical-dl-utils.git
 
 ```
+
+## Docker Images
+
+We provide a docker image for easy usage of the package and as a base image for other projects.
+
+The file for this image can be found at `dockers/Dockerfile`. We provide both, a CPU-only and a CUDA-enabled image based on the NVIDIA NGC PyTorch image.
+These images can be found on [DockerHub](https://hub.docker.com/repository/docker/justusschock/medical-dl-utils).
```

### Comparing `medical_data-0.2.0/README.md` & `medical_data-0.2.0.dev0/README.md`

 * *Files 25% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # Medical Data
 
 [![UnitTest](https://github.com/justusschock/medical-data/actions/workflows/unittests.yaml/badge.svg)](https://github.com/justusschock/medicaldata/actions/workflows/unittests.yaml) [![Build Package](https://github.com/justusschock/medical-data/actions/workflows/package_build.yaml/badge.svg)](https://github.com/justusschock/medical-data/actions/workflows/package_build.yaml) ![PyPI](https://img.shields.io/pypi/v/medical-data?color=grene) [![pre-commit.ci status](https://results.pre-commit.ci/badge/github/justusschock/medical-data/main.svg)](https://results.pre-commit.ci/latest/github/justusschock/medical-data/main)
 
-This repository contains utilities for handling data in medical image analysis that are not specific to certain tasks.
+This repository contains utilities for training and evaluating deep learning models in medical image analysis that are not specific to certain tasks.
 
 So far it consists of 2 major parts:
 An abstract Dataset API built on top of `torch.utils.data.Dataset` and `torchio.data.Subject` as well as general transforms for this kind of data.
 
 To use the dataset classes, you basically only need to implement the `parse_subjects` method to return a list of samples and everything else will work automatically.
 You will automatically get image statistics such as median spacing or median shape. For label statistics, you either need to subclass the `AbstractDiscreteLabelDataset` or implement the `get_single_label_stats` and `aggregate_label_stats` methods.
 
@@ -18,28 +18,35 @@
 
 This project can be installed either from PyPI or by cloning the repository from GitHub.
 
 For an install of published packages, use the command
 
 ```bash
 
-    pip install medical-data
+    pip install medical-dl-utils
 
 ```
 
 To install from the (cloned) repository, use the command
 
 ```bash
 
-    pip install PATH/TO/medical-data
+    pip install PATH/TO/medical-dl-utils
 
 ```
 
 You can also add `-e` to the command to make an editable install in case you want to modify the code.
 
 You can also install the package directly from GitHub by running
 
 ```bash
 
-    pip install git+https://github.com/justusschock/medical-data.git
+    pip install git+https://github.com/justusschock/medical-dl-utils.git
 
 ```
+
+## Docker Images
+
+We provide a docker image for easy usage of the package and as a base image for other projects.
+
+The file for this image can be found at `dockers/Dockerfile`. We provide both, a CPU-only and a CUDA-enabled image based on the NVIDIA NGC PyTorch image.
+These images can be found on [DockerHub](https://hub.docker.com/repository/docker/justusschock/medical-dl-utils).
```

### Comparing `medical_data-0.2.0/medical_data/__init__.py` & `medical_data-0.2.0.dev0/medical_data/__init__.py`

 * *Files 9% similar despite different names*

```diff
@@ -35,8 +35,8 @@
     "NNUnetNormalization",
     "ResampleAndCropOrPad",
     "ResampleOnehot",
     "RescaleIntensityPercentiles",
     "SingleClassMetric",
 ]
 
-__version__ = "0.2.0"
+__version__ = "0.2.0dev"
```

### Comparing `medical_data-0.2.0/medical_data/dataset.py` & `medical_data-0.2.0.dev0/medical_data/dataset.py`

 * *Files identical despite different names*

### Comparing `medical_data-0.2.0/medical_data/indexing.py` & `medical_data-0.2.0.dev0/medical_data/indexing.py`

 * *Files identical despite different names*

### Comparing `medical_data-0.2.0/medical_data/modality.py` & `medical_data-0.2.0.dev0/medical_data/modality.py`

 * *Files identical despite different names*

### Comparing `medical_data-0.2.0/medical_data/moving_avg.py` & `medical_data-0.2.0.dev0/medical_data/moving_avg.py`

 * *Files identical despite different names*

### Comparing `medical_data-0.2.0/medical_data/single_class.py` & `medical_data-0.2.0.dev0/medical_data/single_class.py`

 * *Files identical despite different names*

### Comparing `medical_data-0.2.0/medical_data/transforms.py` & `medical_data-0.2.0.dev0/medical_data/transforms.py`

 * *Files identical despite different names*

### Comparing `medical_data-0.2.0/medical_data/utils.py` & `medical_data-0.2.0.dev0/medical_data/utils.py`

 * *Files identical despite different names*

### Comparing `medical_data-0.2.0/medical_data.egg-info/PKG-INFO` & `medical_data-0.2.0.dev0/medical_data.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: medical-data
-Version: 0.2.0
+Version: 0.2.0.dev0
 Summary: Helpful data utilities for deep learning in medical image analysis/medical image computing
 Author: Justus Schock
 Author-email: justus.schock@posteo.de
 Maintainer-email: Justus Schock <justus.schock@posteo.de>
 License:                                  Apache License
                                    Version 2.0, January 2004
                                 http://www.apache.org/licenses/
@@ -217,15 +217,15 @@
 Provides-Extra: test
 License-File: LICENSE
 
 # Medical Data
 
 [![UnitTest](https://github.com/justusschock/medical-data/actions/workflows/unittests.yaml/badge.svg)](https://github.com/justusschock/medicaldata/actions/workflows/unittests.yaml) [![Build Package](https://github.com/justusschock/medical-data/actions/workflows/package_build.yaml/badge.svg)](https://github.com/justusschock/medical-data/actions/workflows/package_build.yaml) ![PyPI](https://img.shields.io/pypi/v/medical-data?color=grene) [![pre-commit.ci status](https://results.pre-commit.ci/badge/github/justusschock/medical-data/main.svg)](https://results.pre-commit.ci/latest/github/justusschock/medical-data/main)
 
-This repository contains utilities for handling data in medical image analysis that are not specific to certain tasks.
+This repository contains utilities for training and evaluating deep learning models in medical image analysis that are not specific to certain tasks.
 
 So far it consists of 2 major parts:
 An abstract Dataset API built on top of `torch.utils.data.Dataset` and `torchio.data.Subject` as well as general transforms for this kind of data.
 
 To use the dataset classes, you basically only need to implement the `parse_subjects` method to return a list of samples and everything else will work automatically.
 You will automatically get image statistics such as median spacing or median shape. For label statistics, you either need to subclass the `AbstractDiscreteLabelDataset` or implement the `get_single_label_stats` and `aggregate_label_stats` methods.
 
@@ -237,28 +237,35 @@
 
 This project can be installed either from PyPI or by cloning the repository from GitHub.
 
 For an install of published packages, use the command
 
 ```bash
 
-    pip install medical-data
+    pip install medical-dl-utils
 
 ```
 
 To install from the (cloned) repository, use the command
 
 ```bash
 
-    pip install PATH/TO/medical-data
+    pip install PATH/TO/medical-dl-utils
 
 ```
 
 You can also add `-e` to the command to make an editable install in case you want to modify the code.
 
 You can also install the package directly from GitHub by running
 
 ```bash
 
-    pip install git+https://github.com/justusschock/medical-data.git
+    pip install git+https://github.com/justusschock/medical-dl-utils.git
 
 ```
+
+## Docker Images
+
+We provide a docker image for easy usage of the package and as a base image for other projects.
+
+The file for this image can be found at `dockers/Dockerfile`. We provide both, a CPU-only and a CUDA-enabled image based on the NVIDIA NGC PyTorch image.
+These images can be found on [DockerHub](https://hub.docker.com/repository/docker/justusschock/medical-dl-utils).
```

### Comparing `medical_data-0.2.0/pyproject.toml` & `medical_data-0.2.0.dev0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -17,15 +17,15 @@
   "Programming Language :: Python :: 3"
 ]
 
 dependencies = [
     "torch >= 1.9, < 3.0",
     "psutil < 5.9.2",
     "torchio > 0.18.56, < 0.18.79",
-    "lightning >= 2.0, < 3.0",
+    "lightning >= 1.5, < 2.0",
     "lightning-utilities >=0.5, <0.9",
     "monai >= 0.7, < 1.1.1",
     "loguru == 0.7.0",
     "psutil < 5.9.6",
     "torchio > 0.18.56, < 0.18.92",
     "pytorch-lightning >=1.5",
     "loguru >= 0.6.0",
```

### Comparing `medical_data-0.2.0/tests/data/test_modality.py` & `medical_data-0.2.0.dev0/tests/data/test_modality.py`

 * *Files identical despite different names*

