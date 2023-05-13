# Comparing `tmp/cleanlab-2.3.0.tar.gz` & `tmp/cleanlab-2.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cleanlab-2.3.0.tar", last modified: Wed Mar  1 23:03:48 2023, max compression
+gzip compressed data, was "cleanlab-2.3.1.tar", last modified: Tue Mar 28 06:29:47 2023, max compression
```

## Comparing `cleanlab-2.3.0.tar` & `cleanlab-2.3.1.tar`

### file list

```diff
@@ -1,72 +1,58 @@
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.095132 cleanlab-2.3.0/
--rw-r--r--   0 jonas      (501) staff       (20)     5373 2023-03-01 09:12:13.000000 cleanlab-2.3.0/CODE_OF_CONDUCT.md
--rw-r--r--   0 jonas      (501) staff       (20)     3222 2023-03-01 09:12:13.000000 cleanlab-2.3.0/CONTRIBUTING.md
--rw-r--r--   0 jonas      (501) staff       (20)    10470 2023-03-01 09:12:13.000000 cleanlab-2.3.0/DEVELOPMENT.md
--rw-r--r--   0 jonas      (501) staff       (20)    34524 2023-03-01 09:12:13.000000 cleanlab-2.3.0/LICENSE
--rw-r--r--   0 jonas      (501) staff       (20)       76 2023-03-01 09:12:13.000000 cleanlab-2.3.0/MANIFEST.in
--rw-r--r--   0 jonas      (501) staff       (20)    37435 2023-03-01 23:03:48.095253 cleanlab-2.3.0/PKG-INFO
--rw-r--r--   0 jonas      (501) staff       (20)    35685 2023-03-01 09:12:13.000000 cleanlab-2.3.0/README.md
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.087762 cleanlab-2.3.0/cleanlab/
--rw-r--r--   0 jonas      (501) staff       (20)      297 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/__init__.py
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.088480 cleanlab-2.3.0/cleanlab/benchmarking/
--rw-r--r--   0 jonas      (501) staff       (20)       31 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/benchmarking/__init__.py
--rw-r--r--   0 jonas      (501) staff       (20)    17564 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/benchmarking/noise_generation.py
--rw-r--r--   0 jonas      (501) staff       (20)    49769 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/classification.py
--rw-r--r--   0 jonas      (501) staff       (20)    69037 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/count.py
--rw-r--r--   0 jonas      (501) staff       (20)    21556 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/dataset.py
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.089162 cleanlab-2.3.0/cleanlab/experimental/
--rw-r--r--   0 jonas      (501) staff       (20)        0 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/experimental/__init__.py
--rw-r--r--   0 jonas      (501) staff       (20)     3950 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/experimental/cifar_cnn.py
--rw-r--r--   0 jonas      (501) staff       (20)     8670 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/experimental/coteaching.py
--rw-r--r--   0 jonas      (501) staff       (20)    34388 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/experimental/label_issues_batched.py
--rw-r--r--   0 jonas      (501) staff       (20)    14111 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/experimental/mnist_pytorch.py
--rw-r--r--   0 jonas      (501) staff       (20)    50441 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/filter.py
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.090614 cleanlab-2.3.0/cleanlab/internal/
--rw-r--r--   0 jonas      (501) staff       (20)        0 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/__init__.py
--rw-r--r--   0 jonas      (501) staff       (20)     5296 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/label_quality_utils.py
--rw-r--r--   0 jonas      (501) staff       (20)    14552 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/latent_algebra.py
--rw-r--r--   0 jonas      (501) staff       (20)    14690 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/multiannotator_utils.py
--rw-r--r--   0 jonas      (501) staff       (20)    24190 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/multilabel_scorer.py
--rw-r--r--   0 jonas      (501) staff       (20)     3807 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/multilabel_utils.py
--rw-r--r--   0 jonas      (501) staff       (20)     8849 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/token_classification_utils.py
--rw-r--r--   0 jonas      (501) staff       (20)    28265 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/util.py
--rw-r--r--   0 jonas      (501) staff       (20)     8408 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/internal/validation.py
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.090990 cleanlab-2.3.0/cleanlab/models/
--rw-r--r--   0 jonas      (501) staff       (20)        0 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/models/__init__.py
--rw-r--r--   0 jonas      (501) staff       (20)    12093 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/models/fasttext.py
--rw-r--r--   0 jonas      (501) staff       (20)    11516 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/models/keras.py
--rw-r--r--   0 jonas      (501) staff       (20)    80002 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/multiannotator.py
--rw-r--r--   0 jonas      (501) staff       (20)     6481 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/multilabel_classification.py
--rw-r--r--   0 jonas      (501) staff       (20)    26479 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/outlier.py
--rw-r--r--   0 jonas      (501) staff       (20)    25716 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/rank.py
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.091530 cleanlab-2.3.0/cleanlab/token_classification/
--rw-r--r--   0 jonas      (501) staff       (20)       62 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/token_classification/__init__.py
--rw-r--r--   0 jonas      (501) staff       (20)     4205 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/token_classification/filter.py
--rw-r--r--   0 jonas      (501) staff       (20)    12446 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/token_classification/rank.py
--rw-r--r--   0 jonas      (501) staff       (20)    14184 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/token_classification/summary.py
--rw-r--r--   0 jonas      (501) staff       (20)      264 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/typing.py
--rw-r--r--   0 jonas      (501) staff       (20)     8233 2023-03-01 09:12:13.000000 cleanlab-2.3.0/cleanlab/version.py
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.088274 cleanlab-2.3.0/cleanlab.egg-info/
--rw-r--r--   0 jonas      (501) staff       (20)    37435 2023-03-01 23:03:48.000000 cleanlab-2.3.0/cleanlab.egg-info/PKG-INFO
--rw-r--r--   0 jonas      (501) staff       (20)     1742 2023-03-01 23:03:48.000000 cleanlab-2.3.0/cleanlab.egg-info/SOURCES.txt
--rw-r--r--   0 jonas      (501) staff       (20)        1 2023-03-01 23:03:48.000000 cleanlab-2.3.0/cleanlab.egg-info/dependency_links.txt
--rw-r--r--   0 jonas      (501) staff       (20)       76 2023-03-01 23:03:48.000000 cleanlab-2.3.0/cleanlab.egg-info/requires.txt
--rw-r--r--   0 jonas      (501) staff       (20)        9 2023-03-01 23:03:48.000000 cleanlab-2.3.0/cleanlab.egg-info/top_level.txt
--rw-r--r--   0 jonas      (501) staff       (20)      230 2023-03-01 09:12:13.000000 cleanlab-2.3.0/pyproject.toml
--rw-r--r--   0 jonas      (501) staff       (20)      250 2023-03-01 23:03:48.095497 cleanlab-2.3.0/setup.cfg
--rw-r--r--   0 jonas      (501) staff       (20)     3735 2023-03-01 09:12:13.000000 cleanlab-2.3.0/setup.py
-drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-01 23:03:48.094995 cleanlab-2.3.0/tests/
--rw-r--r--   0 jonas      (501) staff       (20)    25800 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_classification.py
--rw-r--r--   0 jonas      (501) staff       (20)    11564 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_dataset.py
--rw-r--r--   0 jonas      (501) staff       (20)    45349 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_filter_count.py
--rw-r--r--   0 jonas      (501) staff       (20)    14649 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_frameworks.py
--rw-r--r--   0 jonas      (501) staff       (20)     4357 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_latent_algebra.py
--rw-r--r--   0 jonas      (501) staff       (20)     3635 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_model_pytorch_cnn.py
--rw-r--r--   0 jonas      (501) staff       (20)    24240 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_multiannotator.py
--rw-r--r--   0 jonas      (501) staff       (20)    18396 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_multilabel_classification.py
--rw-r--r--   0 jonas      (501) staff       (20)     6828 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_noise_generation.py
--rw-r--r--   0 jonas      (501) staff       (20)    24860 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_outlier.py
--rw-r--r--   0 jonas      (501) staff       (20)    16170 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_rank.py
--rw-r--r--   0 jonas      (501) staff       (20)    11369 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_token_classification.py
--rw-r--r--   0 jonas      (501) staff       (20)     3792 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_util.py
--rw-r--r--   0 jonas      (501) staff       (20)      925 2023-03-01 09:12:13.000000 cleanlab-2.3.0/tests/test_validation.py
+drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-28 06:29:47.546232 cleanlab-2.3.1/
+-rw-r--r--   0 jonas      (501) staff       (20)     5373 2023-03-28 06:27:48.000000 cleanlab-2.3.1/CODE_OF_CONDUCT.md
+-rw-r--r--   0 jonas      (501) staff       (20)     3222 2023-03-28 06:27:48.000000 cleanlab-2.3.1/CONTRIBUTING.md
+-rw-r--r--   0 jonas      (501) staff       (20)    10470 2023-03-28 06:27:48.000000 cleanlab-2.3.1/DEVELOPMENT.md
+-rw-r--r--   0 jonas      (501) staff       (20)    34524 2023-03-28 06:27:48.000000 cleanlab-2.3.1/LICENSE
+-rw-r--r--   0 jonas      (501) staff       (20)       76 2023-03-28 06:27:48.000000 cleanlab-2.3.1/MANIFEST.in
+-rw-r--r--   0 jonas      (501) staff       (20)    34714 2023-03-28 06:29:47.546334 cleanlab-2.3.1/PKG-INFO
+-rw-r--r--   0 jonas      (501) staff       (20)    32964 2023-03-28 06:27:48.000000 cleanlab-2.3.1/README.md
+drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-28 06:29:47.540891 cleanlab-2.3.1/cleanlab/
+-rw-r--r--   0 jonas      (501) staff       (20)      297 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/__init__.py
+drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-28 06:29:47.541619 cleanlab-2.3.1/cleanlab/benchmarking/
+-rw-r--r--   0 jonas      (501) staff       (20)       31 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/benchmarking/__init__.py
+-rw-r--r--   0 jonas      (501) staff       (20)    17651 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/benchmarking/noise_generation.py
+-rw-r--r--   0 jonas      (501) staff       (20)    49769 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/classification.py
+-rw-r--r--   0 jonas      (501) staff       (20)    69355 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/count.py
+-rw-r--r--   0 jonas      (501) staff       (20)    21793 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/dataset.py
+drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-28 06:29:47.542288 cleanlab-2.3.1/cleanlab/experimental/
+-rw-r--r--   0 jonas      (501) staff       (20)        0 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/experimental/__init__.py
+-rw-r--r--   0 jonas      (501) staff       (20)     3950 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/experimental/cifar_cnn.py
+-rw-r--r--   0 jonas      (501) staff       (20)     8670 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/experimental/coteaching.py
+-rw-r--r--   0 jonas      (501) staff       (20)    34705 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/experimental/label_issues_batched.py
+-rw-r--r--   0 jonas      (501) staff       (20)    14111 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/experimental/mnist_pytorch.py
+-rw-r--r--   0 jonas      (501) staff       (20)    50441 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/filter.py
+drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-28 06:29:47.544718 cleanlab-2.3.1/cleanlab/internal/
+-rw-r--r--   0 jonas      (501) staff       (20)        0 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/__init__.py
+-rw-r--r--   0 jonas      (501) staff       (20)     1122 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/constants.py
+-rw-r--r--   0 jonas      (501) staff       (20)     5379 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/label_quality_utils.py
+-rw-r--r--   0 jonas      (501) staff       (20)    14645 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/latent_algebra.py
+-rw-r--r--   0 jonas      (501) staff       (20)    15163 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/multiannotator_utils.py
+-rw-r--r--   0 jonas      (501) staff       (20)    24190 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/multilabel_scorer.py
+-rw-r--r--   0 jonas      (501) staff       (20)     3807 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/multilabel_utils.py
+-rw-r--r--   0 jonas      (501) staff       (20)     8849 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/token_classification_utils.py
+-rw-r--r--   0 jonas      (501) staff       (20)    28342 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/util.py
+-rw-r--r--   0 jonas      (501) staff       (20)     8552 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/internal/validation.py
+drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-28 06:29:47.545160 cleanlab-2.3.1/cleanlab/models/
+-rw-r--r--   0 jonas      (501) staff       (20)        0 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/models/__init__.py
+-rw-r--r--   0 jonas      (501) staff       (20)    12093 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/models/fasttext.py
+-rw-r--r--   0 jonas      (501) staff       (20)    11516 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/models/keras.py
+-rw-r--r--   0 jonas      (501) staff       (20)    84802 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/multiannotator.py
+-rw-r--r--   0 jonas      (501) staff       (20)     6481 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/multilabel_classification.py
+-rw-r--r--   0 jonas      (501) staff       (20)    26479 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/outlier.py
+-rw-r--r--   0 jonas      (501) staff       (20)    25698 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/rank.py
+drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-28 06:29:47.546115 cleanlab-2.3.1/cleanlab/token_classification/
+-rw-r--r--   0 jonas      (501) staff       (20)       62 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/token_classification/__init__.py
+-rw-r--r--   0 jonas      (501) staff       (20)     4205 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/token_classification/filter.py
+-rw-r--r--   0 jonas      (501) staff       (20)    12446 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/token_classification/rank.py
+-rw-r--r--   0 jonas      (501) staff       (20)    14184 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/token_classification/summary.py
+-rw-r--r--   0 jonas      (501) staff       (20)      264 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/typing.py
+-rw-r--r--   0 jonas      (501) staff       (20)     8346 2023-03-28 06:27:48.000000 cleanlab-2.3.1/cleanlab/version.py
+drwxr-xr-x   0 jonas      (501) staff       (20)        0 2023-03-28 06:29:47.541403 cleanlab-2.3.1/cleanlab.egg-info/
+-rw-r--r--   0 jonas      (501) staff       (20)    34714 2023-03-28 06:29:47.000000 cleanlab-2.3.1/cleanlab.egg-info/PKG-INFO
+-rw-r--r--   0 jonas      (501) staff       (20)     1389 2023-03-28 06:29:47.000000 cleanlab-2.3.1/cleanlab.egg-info/SOURCES.txt
+-rw-r--r--   0 jonas      (501) staff       (20)        1 2023-03-28 06:29:47.000000 cleanlab-2.3.1/cleanlab.egg-info/dependency_links.txt
+-rw-r--r--   0 jonas      (501) staff       (20)       76 2023-03-28 06:29:47.000000 cleanlab-2.3.1/cleanlab.egg-info/requires.txt
+-rw-r--r--   0 jonas      (501) staff       (20)        9 2023-03-28 06:29:47.000000 cleanlab-2.3.1/cleanlab.egg-info/top_level.txt
+-rw-r--r--   0 jonas      (501) staff       (20)      230 2023-03-28 06:27:48.000000 cleanlab-2.3.1/pyproject.toml
+-rw-r--r--   0 jonas      (501) staff       (20)      250 2023-03-28 06:29:47.546563 cleanlab-2.3.1/setup.cfg
+-rw-r--r--   0 jonas      (501) staff       (20)     3735 2023-03-28 06:27:48.000000 cleanlab-2.3.1/setup.py
```

### Comparing `cleanlab-2.3.0/CODE_OF_CONDUCT.md` & `cleanlab-2.3.1/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/CONTRIBUTING.md` & `cleanlab-2.3.1/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/DEVELOPMENT.md` & `cleanlab-2.3.1/DEVELOPMENT.md`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/LICENSE` & `cleanlab-2.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/PKG-INFO` & `cleanlab-2.3.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cleanlab
-Version: 2.3.0
+Version: 2.3.1
 Summary: The standard package for data-centric AI, machine learning with label errors, and automatically finding and fixing dataset issues in Python.
 Home-page: https://cleanlab.ai
 Author: Cleanlab Inc.
 Author-email: team@cleanlab.ai
 License: AGPLv3+
 Project-URL: Documentation, https://docs.cleanlab.ai
 Project-URL: Bug Tracker, https://github.com/cleanlab/cleanlab/issues
@@ -29,21 +29,24 @@
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Topic :: Software Development :: Libraries
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/cleanlab_logo_open_source_transparent_optimized_size.png)
+<p align="center">
+  <img src="https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/cleanlab_logo_open_source_transparent_optimized_size.png" width=60% height=60%>
+</p>
 
-cleanlab automatically detects problems in a ML dataset. This data-centric AI package facilitates **machine learning with messy, real-world data** by providing **clean lab**els for robust training and flagging errors in your data.
+
+cleanlab helps you **clean** data and **lab**els by automatically detecting issues in a ML dataset. To facilitate **machine learning with messy, real-world data**, this data-centric AI package uses your *existing* models to estimate dataset problems that can be fixed to train even *better* models.
 
 ```python
 
-# cleanlab works with **any classifier**. Yup, you can use sklearn/PyTorch/TensorFlow/XGBoost/etc.
+# cleanlab works with **any classifier**. Yup, you can use PyTorch/TensorFlow/OpenAI/XGBoost/etc.
 cl = cleanlab.classification.CleanLearning(sklearn.YourFavoriteClassifier())
 
 # cleanlab finds data and label issues in **any dataset**... in ONE line of code!
 label_issues = cl.find_label_issues(data, labels)
 
 # cleanlab trains a robust version of your model that works more reliably with noisy data.
 cl.fit(data, labels)
@@ -69,95 +72,56 @@
 [![docs](https://img.shields.io/static/v1?logo=github&style=flat&color=pink&label=docs&message=cleanlab)](https://docs.cleanlab.ai/)
 [![Slack Community](https://img.shields.io/static/v1?logo=slack&style=flat&color=white&label=slack&message=community)](https://cleanlab.ai/slack)
 [![Twitter](https://img.shields.io/twitter/follow/CleanlabAI?style=social)](https://twitter.com/CleanlabAI)
 [![Cleanlab Studio](https://raw.githubusercontent.com/cleanlab/assets/master/shields/cl-studio-shield.svg)](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio)
 
 -----
 
-<details><summary><b>News! (2022) </b> -- cleanlab made accessible for everybody, not just ML researchers (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Nov 2022 📖</b> cleanlab 2.2.0 released! Added better algorithms for: label issues in multi-label classification, data with some classes absent, and estimating the number of label errors in a dataset. </li>
-<li> <b>Sep 2022 📖</b> cleanlab 2.1.0 released! Added support for: data labeled by multiple annotators in cleanlab.multiannotator, token classification with text data in cleanlab.token_classification, out-of-distribution detection in cleanlab.outlier, and CleanLearning with non-numpy-array data (e.g. pandas dataframes, tensorflow/pytorch datasets, etc) in cleanlab.classification.CleanLearning. </li>
-<li> <b>April 2022 📖</b> cleanlab 2.0.0 released! Lays foundations for this library to grow into a general-purpose data-centric AI toolkit. </li>
-<li> <b>March 2022 📖</b>  Documentation migrated to new website: <a href="https://docs.cleanlab.ai/">docs.cleanlab.ai</a> with quickstart tutorials for image/text/audio/tabular data.</li>
-<li> <b>Feb 2022 💻</b> <a href="https://docs.cleanlab.ai/master/migrating/migrate_v2.html">APIs simplified</a> to make cleanlab accessible for everybody, not just ML researchers </li>
-<li> <b>Long-time cleanlab user?</b> Here's <a href="https://docs.cleanlab.ai/stable/migrating/migrate_v2.html">how to migrate</a> to cleanlab versions >= 2.0.0. </li>
-</ul>
-</p>
-</details>
-
-<details><summary><b>News! (2021) </b> -- cleanlab finds pervasive label errors in the most common ML datasets (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Dec 2021 🎉</b>  NeurIPS published the <a href="https://arxiv.org/abs/2103.14749">label errors paper (Northcutt, Athalye, & Mueller, 2021)</a>.</li>
-<li> <b>Apr 2021 🎉</b>  Journal of AI Research published the <a href="https://jair.org/index.php/jair/article/view/12125">confident learning paper (Northcutt, Jiang, & Chuang, 2021)</a>.</li>
-<li> <b>Mar 2021 😲</b>  cleanlab used to find and fix label issues in 10 of the most common ML benchmark datasets, published in: <a href="https://neurips.cc/Conferences/2021/ScheduleMultitrack?event=22763">NeurIPS 2021</a>. Along with <a href="https://arxiv.org/abs/2103.14749">the paper (Northcutt, Athalye, & Mueller, 2021)</a>, the authors launched <a href="https://labelerrors.com">labelerrors.com</a> where you can view the label issues in these datasets.</li>
-</ul>
-</p>
-</details>
-
-<details><summary><b>News! (2020) </b> -- cleanlab supports all OS, achieves state-of-the-art performance (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Dec 2020 🎉</b>  cleanlab supports NeurIPS workshop paper <a href="https://securedata.lol/camera_ready/28.pdf">(Northcutt, Athalye, & Lin, 2020)</a>.</li>
-<li> <b>Dec 2020 🤖</b>  cleanlab supports <a href="https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L215">PU learning</a>.</li>
-<li> <b>Feb 2020 🤖</b>  cleanlab now natively supports Mac, Linux, and Windows.</li>
-<li> <b>Feb 2020 🤖</b>  cleanlab now supports <a href="https://github.com/cleanlab/cleanlab/blob/master/cleanlab/experimental/coteaching.py">Co-Teaching</a> <a href="https://arxiv.org/abs/1804.06872">(Han et al., 2018)</a>.</li>
-<li> <b>Jan 2020 🎉</b> cleanlab achieves state-of-the-art on CIFAR-10 with noisy labels. Code to reproduce:  <a href="https://github.com/cleanlab/examples/tree/master/contrib/v1/cifar10">examples/cifar10</a>. This is a great place to see how to use cleanlab on real datasets (with predicted probabilities from trained model already precomputed for you).</li>
-</ul>
-</p>
-</details>
-
-Release notes for past versions are [here](https://github.com/cleanlab/cleanlab/releases).
-Details behind updates are explained in our [blog](https://cleanlab.ai/blog/) and [research papers](https://cleanlab.ai/research/).
-
-
 ## So fresh, so cleanlab
 
-cleanlab **clean**s your data's **lab**els via state-of-the-art *confident learning* algorithms, published in this [paper](https://jair.org/index.php/jair/article/view/12125) and [blog](https://l7.curtisnorthcutt.com/confident-learning). See some of the datasets cleaned with cleanlab at [labelerrors.com](https://labelerrors.com). This package helps you find data and label issues so you can train reliable ML models.
+cleanlab **clean**s your data's **lab**els via state-of-the-art *confident learning* algorithms, published in this [paper](https://jair.org/index.php/jair/article/view/12125) and [blog](https://l7.curtisnorthcutt.com/confident-learning). See some of the datasets cleaned with cleanlab at [labelerrors.com](https://labelerrors.com). This package helps you find label issues and other data issues, so you can train reliable ML models.
 
 cleanlab is:
 
 1. **backed by theory**
    - with [provable guarantees](https://arxiv.org/abs/1911.00068) of exact estimation of noise and label errors, even with imperfect models.
 2. **fast**
-   - Code is parallelized (< 1 second to find label issues in ImageNet with pre-computed predictions).
+   - Code is parallelized and scalable.
 4. **easy-to-use**
-   - Find label issues or train noise-robust models in one line of code (no hyperparameters by default).
+   - Find mislabeled data, bad annotators, outliers, or train noise-robust models -- all in one line of code.
 6. **general**
-   - Works with **[any dataset](https://labelerrors.com/)** and **any model**, e.g., TensorFlow, PyTorch, sklearn, XGBoost, Huggingface, etc.
+   - Works with **[any dataset](https://labelerrors.com/)** (text, image, tabular, audio, ...) and **any model** (TensorFlow, PyTorch, JAX, HuggingFace,  OpenAI, XGBoost, scikit-learn, ...)
 <br/>
 
 ![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/label-errors-examples.png)
 <p align="center">
 Examples of incorrect given labels in various image datasets <a href="https://l7.curtisnorthcutt.com/label-errors">found and corrected</a> using cleanlab.
 </p>
 
 ## Run cleanlab
 
 cleanlab supports Linux, macOS, and Windows and runs on Python 3.7+.
 
 - Get started [here](https://docs.cleanlab.ai/)! Install via `pip` or `conda` as described [here](https://docs.cleanlab.ai/).
 - Developers who install the bleeding-edge from source should refer to [this master branch documentation](https://docs.cleanlab.ai/master/index.html).
-
+- For help, check out our detailed [FAQ](https://docs.cleanlab.ai/stable/tutorials/faq.html), [Github Issues](https://github.com/cleanlab/cleanlab/issues?q=is%3Aissue), or [Slack](https://cleanlab.ai/slack). We welcome any questions!
 
 ## Use cleanlab with any model for most ML tasks
 
-All features of cleanlab work with **any dataset** and **any model**. Yes, any model: scikit-learn, PyTorch, Tensorflow, Keras, JAX, HuggingFace, MXNet, XGBoost, etc.
+All features of cleanlab work with **any dataset** and **any model**. Yes, any model: PyTorch, Tensorflow, Keras, JAX, HuggingFace, OpenAI, XGBoost, scikit-learn, etc.
 If you use a sklearn-compatible classifier, all cleanlab methods work out-of-the-box.
 
 <details><summary>
 It’s also easy to use your favorite non-sklearn-compatible model (<b>click to learn more</b>)
 </summary>
 <br/>
 
 cleanlab can find label issues from any model's predicted class probabilities if you can produce them yourself.
 
-Some other cleanlab functionality requires your model to be sklearn-compatible.
+Some cleanlab functionality may require your model to be sklearn-compatible.
 There's nothing you need to do if your model already has `.fit()`, `.predict()`, and `.predict_proba()` methods.
 Otherwise, just wrap your custom model into a Python class that inherits the `sklearn.base.BaseEstimator`:
 
 ``` python
 from sklearn.base import BaseEstimator
 class YourFavoriteModel(BaseEstimator): # Inherits sklearn base classifier
     def __init__(self, ):
@@ -182,15 +146,15 @@
 cl.predict(test_data)
 ```
 
 #### Want to see a working example? [Here’s a compliant PyTorch MNIST CNN class](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/experimental/mnist_pytorch.py)
 
 More details are provided in documentation of [cleanlab.classification.CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html).
 
-Note, some libraries exist to give you sklearn-compatibility for free. For PyTorch, check out the [skorch](https://skorch.readthedocs.io/) Python library which will wrap your PyTorch model into a sklearn-compatible model ([example](https://docs.cleanlab.ai/stable/tutorials/image.html)). For TensorFlow/Keras, check out [SciKeras](https://www.adriangb.com/scikeras/) ([example](https://docs.cleanlab.ai/stable/tutorials/text.html)) or [our own Keras wrapper](https://docs.cleanlab.ai/stable/cleanlab/experimental/keras.html). Many libraries also already offer a special scikit-learn API, for example: [XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_api.html#module-xgboost.sklearn) or [LightGBM](https://lightgbm.readthedocs.io/en/latest/pythonapi/lightgbm.LGBMClassifier.html).
+Note, some libraries exist to give you sklearn-compatibility for free. For PyTorch, check out the [skorch](https://skorch.readthedocs.io/) Python library which will wrap your PyTorch model into a sklearn-compatible model ([example](https://docs.cleanlab.ai/stable/tutorials/image.html)). For TensorFlow/Keras, check out our [Keras wrapper](https://docs.cleanlab.ai/stable/cleanlab/models/keras.html). Many libraries also already offer a special scikit-learn API, for example: [XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_api.html#module-xgboost.sklearn) or [LightGBM](https://lightgbm.readthedocs.io/en/latest/pythonapi/lightgbm.LGBMClassifier.html).
 
 <br/>
 </details>
 
 cleanlab is useful across a wide variety of Machine Learning tasks. Specific tasks this package offers dedicated functionality for include:
 1. [Binary and multi-class classification](https://docs.cleanlab.ai/stable/tutorials/indepth_overview.html)
 2. [Multi-label classification](https://docs.cleanlab.ai/stable/tutorials/multilabel_classification.html) (e.g. image/document tagging)
@@ -248,15 +212,15 @@
 </summary>
 <br/>
 
 cleanlab is a general tool that can learn with noisy labels regardless of dataset distribution or classifier type: [examples/classifier\_comparison](https://github.com/cleanlab/examples/blob/master/classifier_comparison/classifier_comparison.ipynb).
 
 ![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/demo_cleanlab_across_datasets_and_classifiers.png)
 
-Each sub-figure above depicts the decision boundary learned using [cleanlab.classification.CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) in the presence of extreme (\~35%) label errors (circled in green). Label noise is class-conditional (not uniformly random). Columns are organized by the classifier used, except the left-most column which depicts the ground-truth data distribution. Rows are organized by dataset.
+Each sub-figure above depicts the decision boundary learned using [cleanlab.classification.CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) in the presence of extreme (\~35%) label errors (circled in green). Label noise is class-conditional (not uniformly random). Columns are organized by the classifier used, except the left-most column which depicts the ground-truth data distribution. Rows are organized by dataset.
 
 Each sub-figure depicts accuracy scores on a test set (with correct non-noisy labels) as decimal values:
 
 * LEFT (in black): The classifier test accuracy trained with perfect labels (no label errors).
 * MIDDLE (in blue): The classifier test accuracy trained with noisy labels using cleanlab.
 * RIGHT (in white): The baseline classifier test accuracy trained with noisy labels.
 
@@ -320,20 +284,20 @@
 
 <details><summary>
 cleanlab for advanced users
 (<b>click to learn more</b>)
 </summary>
 <br/>
 
-Many methods and their default parameters are not covered here. Check out the [documentation for the master branch version](https://docs.cleanlab.ai/master/) for the full suite of features supported by the cleanlab API.
+Many methods and their default parameters are not covered here. Check out the [documentation for the developer version (aka master branch)](https://docs.cleanlab.ai/master/) for the full suite of features supported by the cleanlab API.
 
 ## Use any custom model's predicted probabilities to find label errors in 1 line of code
 
 pred_probs (num_examples x num_classes matrix of predicted probabilities) should already be computed on your own, with any classifier. For best results, pred_probs should be obtained in a holdout/out-of-sample manner (e.g. via cross-validation).
-* cleanlab can do this for you via [`cleanlab.count.estimate_cv_predicted_probabilities`](https://docs.cleanlab.ai/master/cleanlab/count.html)]
+* cleanlab can do this for you via [`cleanlab.count.estimate_cv_predicted_probabilities`](https://docs.cleanlab.ai/stable/cleanlab/count.html)]
 * Tutorial with more info: [[here](https://docs.cleanlab.ai/stable/tutorials/pred_probs_cross_val.html)]
 * Examples how to compute pred_probs with: [[CNN image classifier (PyTorch)](https://docs.cleanlab.ai/stable/tutorials/image.html)], [[NN text classifier (TensorFlow)](https://docs.cleanlab.ai/stable/tutorials/text.html)]
 
 ```python
 # label issues are ordered by likelihood of being an error. First index is most likely error.
 from cleanlab.filter import find_label_issues
 
@@ -418,33 +382,33 @@
 
 <details><summary>
 Positive-Unlabeled Learning
 (<b>click to learn more</b>)
 </summary>
 <br/>
 
-Positive-Unlabeled (PU) learning (in which your data only contains a few positively labeled examples with the rest unlabeled) is just a special case of [CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) when one of the classes has no error. `P` stands for the positive class and **is assumed to have zero label errors** and `U` stands for unlabeled data, but in practice, we just assume the `U` class is a noisy negative class that actually contains some positive examples. Thus, the goal of PU learning is to (1) estimate the proportion of negatively labeled examples that actually belong to the positive class (see`fraction\_noise\_in\_unlabeled\_class` in the last example), (2) find the errors (see last example), and (3) train on clean data (see first example below). cleanlab does all three, taking into account that there are no label errors in whichever class you specify as positive.
+Positive-Unlabeled (PU) learning (in which your data only contains a few positively labeled examples with the rest unlabeled) is just a special case of [CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) when one of the classes has no error. `P` stands for the positive class and **is assumed to have zero label errors** and `U` stands for unlabeled data, but in practice, we just assume the `U` class is a noisy negative class that actually contains some positive examples. Thus, the goal of PU learning is to (1) estimate the proportion of negatively labeled examples that actually belong to the positive class (see`fraction\_noise\_in\_unlabeled\_class` in the last example), (2) find the errors (see last example), and (3) train on clean data (see first example below). cleanlab does all three, taking into account that there are no label errors in whichever class you specify as positive.
 
 There are two ways to use cleanlab for PU learning. We'll look at each here.
 
-Method 1. If you are using the cleanlab classifier [CleanLearning()](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141), and your dataset has exactly two classes (positive = 1, and negative = 0), PU
+Method 1. If you are using the cleanlab classifier [CleanLearning()](https://docs.cleanlab.ai/stable/cleanlab/classification.html), and your dataset has exactly two classes (positive = 1, and negative = 0), PU
 learning is supported directly in cleanlab. You can perform PU learning like this:
 
 ``` python
 from cleanlab.classification import CleanLearning
 from sklearn.linear_model import LogisticRegression
 # Wrap around any classifier. Yup, you can use sklearn/pyTorch/TensorFlow/FastText/etc.
 pu_class = 0 # Should be 0 or 1. Label of class with NO ERRORS. (e.g., P class in PU)
 cl = CleanLearning(clf=LogisticRegression(), pulearning=pu_class)
 cl.fit(X=X_train_data, labels=train_noisy_labels)
 # Estimate the predictions you would have gotten by training with *no* label errors.
 predicted_test_labels = cl.predict(X_test)
 ```
 
-Method 2. However, you might be using a more complicated classifier that doesn't work well with [CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) (see this example for CIFAR-10). Or you might have 3 or more classes. Here's how to use cleanlab for PU learning in this situation. To let cleanlab know which class has no error (in standard PU learning, this is the P class), you need to set the threshold for that class to 1 (1 means the probability that the labels of that class are correct is 1, i.e. that class has no
+Method 2. However, you might be using a more complicated classifier that doesn't work well with [CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) (see this example for CIFAR-10). Or you might have 3 or more classes. Here's how to use cleanlab for PU learning in this situation. To let cleanlab know which class has no error (in standard PU learning, this is the P class), you need to set the threshold for that class to 1 (1 means the probability that the labels of that class are correct is 1, i.e. that class has no
 error). Here's the code:
 
 ``` python
 import numpy as np
 # K is the number of classes in your dataset
 # pred_probs are the cross-validated predicted probabilities.
 # s is the array/list/iterable of noisy labels
@@ -554,26 +518,50 @@
         author={Goh, Hui Wen and Tkachenko, Ulyana and Mueller, Jonas},
         booktitle={NeurIPS Human in the Loop Learning Workshop},
         year={2022}
     }
 
 </details>
 
+<details><summary><a href="https://arxiv.org/abs/2301.11856"> ActiveLab: Active learning with data re-labeling (ICLR '23)</a> (<b>click to show bibtex</b>) </summary>
+
+    @inproceedings{goh2023activelab,
+        title={ActiveLab: Active Learning with Re-Labeling by Multiple Annotators},
+        author={Goh, Hui Wen and Mueller, Jonas},
+        booktitle={ICLR Workshop on Trustworthy ML},
+        year={2023}
+    }
+
+</details>
+
+<details><summary><a href="https://arxiv.org/abs/2211.13895"> Incorrect Annotations in Multi-Label Classification (ICLR '23)</a> (<b>click to show bibtex</b>) </summary>
+
+    @inproceedings{thyagarajan2023multilabel,
+        title={Identifying Incorrect Annotations in Multi-Label Classification Data},
+        author={Thyagarajan, Aditya and Snorrason, Elías and Northcutt, Curtis and Mueller, Jonas},
+        booktitle={ICLR Workshop on Trustworthy ML},
+        year={2023}
+    }
+
+</details>
+
 
 To understand/cite other cleanlab functionality not described above, check out our [additional publications](https://cleanlab.ai/research/).
 
 
 ## Other resources
 
 - [Cleanlab Blog](https://cleanlab.ai/blog/)
 
 - [Blog post: Introduction to Confident Learning](https://l7.curtisnorthcutt.com/confident-learning)
 
 - [NeurIPS 2021 paper: Pervasive Label Errors in Test Sets Destabilize Machine Learning Benchmarks](https://arxiv.org/abs/2103.14749)
 
+- [Release notes for past versions](https://github.com/cleanlab/cleanlab/releases)
+
 - [Cleanlab Studio](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio): No-code Data Improvement
 
 While this open-source library **finds** data issues, an interface is needed to efficiently **fix** these issues in your dataset. [Cleanlab Studio](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio) is a no-code platform to find and fix problems in real-world ML datasets. Studio automatically runs optimized versions of the algorithms from this open-source library on top of AutoML models fit to your data, and presents detected issues in a smart data editing interface. Think of it like a data cleaning assistant that helps you quickly improve the quality of your data (via AI/automation + streamlined UX).
 
 ## Join our community
 
 * The best place to learn is [our Slack community](https://cleanlab.ai/slack).
@@ -583,18 +571,19 @@
 * Interested in contributing? See the [contributing guide](CONTRIBUTING.md) and [ideas on useful contributions](https://github.com/cleanlab/cleanlab/wiki#ideas-for-contributing-to-cleanlab). We welcome your help building a standard open-source library for data-centric AI!
 
 * Have code improvements for cleanlab? See the [development guide](DEVELOPMENT.md).
 
 * Have an issue with cleanlab? [Search existing issues](https://github.com/cleanlab/cleanlab/issues?q=is%3Aissue) or [submit a new issue](https://github.com/cleanlab/cleanlab/issues/new).
 
 * Need professional help with cleanlab?
-Join our [\#help Slack channel](https://cleanlab.ai/slack) and message one of our core developers, Jonas Mueller, or schedule a meeting via email: team@cleanlab.ai
+Join our [\#help Slack channel](https://cleanlab.ai/slack) and message us there, or reach out via email: team@cleanlab.ai
 
 ## License
 
-Copyright (c) 2017-2023 Cleanlab Inc.
+Copyright (c) 2017 Cleanlab Inc.
 
 cleanlab is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
 
 cleanlab is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
 
 See [GNU Affero General Public LICENSE](https://github.com/cleanlab/cleanlab/blob/master/LICENSE) for details.
+You can email us to discuss licensing: team@cleanlab.ai
```

### Comparing `cleanlab-2.3.0/README.md` & `cleanlab-2.3.1/cleanlab.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,52 @@
-![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/cleanlab_logo_open_source_transparent_optimized_size.png)
+Metadata-Version: 2.1
+Name: cleanlab
+Version: 2.3.1
+Summary: The standard package for data-centric AI, machine learning with label errors, and automatically finding and fixing dataset issues in Python.
+Home-page: https://cleanlab.ai
+Author: Cleanlab Inc.
+Author-email: team@cleanlab.ai
+License: AGPLv3+
+Project-URL: Documentation, https://docs.cleanlab.ai
+Project-URL: Bug Tracker, https://github.com/cleanlab/cleanlab/issues
+Project-URL: Source Code, https://github.com/cleanlab/cleanlab
+Keywords: machine_learning data_cleaning confident_learning classification weak_supervision learning_with_noisy_labels unsupervised_learning datacentric_ai,datacentric
+Classifier: Development Status :: 4 - Beta
+Classifier: Intended Audience :: Developers
+Classifier: Intended Audience :: Education
+Classifier: Intended Audience :: Science/Research
+Classifier: Intended Audience :: Information Technology
+Classifier: License :: OSI Approved :: GNU Affero General Public License v3 or later (AGPLv3+)
+Classifier: Natural Language :: English
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python
+Classifier: Topic :: Software Development
+Classifier: Topic :: Scientific/Engineering
+Classifier: Topic :: Scientific/Engineering :: Mathematics
+Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
+Classifier: Topic :: Software Development :: Libraries
+Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Requires-Python: >=3.7
+Description-Content-Type: text/markdown
+License-File: LICENSE
 
-cleanlab automatically detects problems in a ML dataset. This data-centric AI package facilitates **machine learning with messy, real-world data** by providing **clean lab**els for robust training and flagging errors in your data.
+<p align="center">
+  <img src="https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/cleanlab_logo_open_source_transparent_optimized_size.png" width=60% height=60%>
+</p>
+
+
+cleanlab helps you **clean** data and **lab**els by automatically detecting issues in a ML dataset. To facilitate **machine learning with messy, real-world data**, this data-centric AI package uses your *existing* models to estimate dataset problems that can be fixed to train even *better* models.
 
 ```python
 
-# cleanlab works with **any classifier**. Yup, you can use sklearn/PyTorch/TensorFlow/XGBoost/etc.
+# cleanlab works with **any classifier**. Yup, you can use PyTorch/TensorFlow/OpenAI/XGBoost/etc.
 cl = cleanlab.classification.CleanLearning(sklearn.YourFavoriteClassifier())
 
 # cleanlab finds data and label issues in **any dataset**... in ONE line of code!
 label_issues = cl.find_label_issues(data, labels)
 
 # cleanlab trains a robust version of your model that works more reliably with noisy data.
 cl.fit(data, labels)
@@ -34,95 +72,56 @@
 [![docs](https://img.shields.io/static/v1?logo=github&style=flat&color=pink&label=docs&message=cleanlab)](https://docs.cleanlab.ai/)
 [![Slack Community](https://img.shields.io/static/v1?logo=slack&style=flat&color=white&label=slack&message=community)](https://cleanlab.ai/slack)
 [![Twitter](https://img.shields.io/twitter/follow/CleanlabAI?style=social)](https://twitter.com/CleanlabAI)
 [![Cleanlab Studio](https://raw.githubusercontent.com/cleanlab/assets/master/shields/cl-studio-shield.svg)](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio)
 
 -----
 
-<details><summary><b>News! (2022) </b> -- cleanlab made accessible for everybody, not just ML researchers (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Nov 2022 📖</b> cleanlab 2.2.0 released! Added better algorithms for: label issues in multi-label classification, data with some classes absent, and estimating the number of label errors in a dataset. </li>
-<li> <b>Sep 2022 📖</b> cleanlab 2.1.0 released! Added support for: data labeled by multiple annotators in cleanlab.multiannotator, token classification with text data in cleanlab.token_classification, out-of-distribution detection in cleanlab.outlier, and CleanLearning with non-numpy-array data (e.g. pandas dataframes, tensorflow/pytorch datasets, etc) in cleanlab.classification.CleanLearning. </li>
-<li> <b>April 2022 📖</b> cleanlab 2.0.0 released! Lays foundations for this library to grow into a general-purpose data-centric AI toolkit. </li>
-<li> <b>March 2022 📖</b>  Documentation migrated to new website: <a href="https://docs.cleanlab.ai/">docs.cleanlab.ai</a> with quickstart tutorials for image/text/audio/tabular data.</li>
-<li> <b>Feb 2022 💻</b> <a href="https://docs.cleanlab.ai/master/migrating/migrate_v2.html">APIs simplified</a> to make cleanlab accessible for everybody, not just ML researchers </li>
-<li> <b>Long-time cleanlab user?</b> Here's <a href="https://docs.cleanlab.ai/stable/migrating/migrate_v2.html">how to migrate</a> to cleanlab versions >= 2.0.0. </li>
-</ul>
-</p>
-</details>
-
-<details><summary><b>News! (2021) </b> -- cleanlab finds pervasive label errors in the most common ML datasets (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Dec 2021 🎉</b>  NeurIPS published the <a href="https://arxiv.org/abs/2103.14749">label errors paper (Northcutt, Athalye, & Mueller, 2021)</a>.</li>
-<li> <b>Apr 2021 🎉</b>  Journal of AI Research published the <a href="https://jair.org/index.php/jair/article/view/12125">confident learning paper (Northcutt, Jiang, & Chuang, 2021)</a>.</li>
-<li> <b>Mar 2021 😲</b>  cleanlab used to find and fix label issues in 10 of the most common ML benchmark datasets, published in: <a href="https://neurips.cc/Conferences/2021/ScheduleMultitrack?event=22763">NeurIPS 2021</a>. Along with <a href="https://arxiv.org/abs/2103.14749">the paper (Northcutt, Athalye, & Mueller, 2021)</a>, the authors launched <a href="https://labelerrors.com">labelerrors.com</a> where you can view the label issues in these datasets.</li>
-</ul>
-</p>
-</details>
-
-<details><summary><b>News! (2020) </b> -- cleanlab supports all OS, achieves state-of-the-art performance (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Dec 2020 🎉</b>  cleanlab supports NeurIPS workshop paper <a href="https://securedata.lol/camera_ready/28.pdf">(Northcutt, Athalye, & Lin, 2020)</a>.</li>
-<li> <b>Dec 2020 🤖</b>  cleanlab supports <a href="https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L215">PU learning</a>.</li>
-<li> <b>Feb 2020 🤖</b>  cleanlab now natively supports Mac, Linux, and Windows.</li>
-<li> <b>Feb 2020 🤖</b>  cleanlab now supports <a href="https://github.com/cleanlab/cleanlab/blob/master/cleanlab/experimental/coteaching.py">Co-Teaching</a> <a href="https://arxiv.org/abs/1804.06872">(Han et al., 2018)</a>.</li>
-<li> <b>Jan 2020 🎉</b> cleanlab achieves state-of-the-art on CIFAR-10 with noisy labels. Code to reproduce:  <a href="https://github.com/cleanlab/examples/tree/master/contrib/v1/cifar10">examples/cifar10</a>. This is a great place to see how to use cleanlab on real datasets (with predicted probabilities from trained model already precomputed for you).</li>
-</ul>
-</p>
-</details>
-
-Release notes for past versions are [here](https://github.com/cleanlab/cleanlab/releases).
-Details behind updates are explained in our [blog](https://cleanlab.ai/blog/) and [research papers](https://cleanlab.ai/research/).
-
-
 ## So fresh, so cleanlab
 
-cleanlab **clean**s your data's **lab**els via state-of-the-art *confident learning* algorithms, published in this [paper](https://jair.org/index.php/jair/article/view/12125) and [blog](https://l7.curtisnorthcutt.com/confident-learning). See some of the datasets cleaned with cleanlab at [labelerrors.com](https://labelerrors.com). This package helps you find data and label issues so you can train reliable ML models.
+cleanlab **clean**s your data's **lab**els via state-of-the-art *confident learning* algorithms, published in this [paper](https://jair.org/index.php/jair/article/view/12125) and [blog](https://l7.curtisnorthcutt.com/confident-learning). See some of the datasets cleaned with cleanlab at [labelerrors.com](https://labelerrors.com). This package helps you find label issues and other data issues, so you can train reliable ML models.
 
 cleanlab is:
 
 1. **backed by theory**
    - with [provable guarantees](https://arxiv.org/abs/1911.00068) of exact estimation of noise and label errors, even with imperfect models.
 2. **fast**
-   - Code is parallelized (< 1 second to find label issues in ImageNet with pre-computed predictions).
+   - Code is parallelized and scalable.
 4. **easy-to-use**
-   - Find label issues or train noise-robust models in one line of code (no hyperparameters by default).
+   - Find mislabeled data, bad annotators, outliers, or train noise-robust models -- all in one line of code.
 6. **general**
-   - Works with **[any dataset](https://labelerrors.com/)** and **any model**, e.g., TensorFlow, PyTorch, sklearn, XGBoost, Huggingface, etc.
+   - Works with **[any dataset](https://labelerrors.com/)** (text, image, tabular, audio, ...) and **any model** (TensorFlow, PyTorch, JAX, HuggingFace,  OpenAI, XGBoost, scikit-learn, ...)
 <br/>
 
 ![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/label-errors-examples.png)
 <p align="center">
 Examples of incorrect given labels in various image datasets <a href="https://l7.curtisnorthcutt.com/label-errors">found and corrected</a> using cleanlab.
 </p>
 
 ## Run cleanlab
 
 cleanlab supports Linux, macOS, and Windows and runs on Python 3.7+.
 
 - Get started [here](https://docs.cleanlab.ai/)! Install via `pip` or `conda` as described [here](https://docs.cleanlab.ai/).
 - Developers who install the bleeding-edge from source should refer to [this master branch documentation](https://docs.cleanlab.ai/master/index.html).
-
+- For help, check out our detailed [FAQ](https://docs.cleanlab.ai/stable/tutorials/faq.html), [Github Issues](https://github.com/cleanlab/cleanlab/issues?q=is%3Aissue), or [Slack](https://cleanlab.ai/slack). We welcome any questions!
 
 ## Use cleanlab with any model for most ML tasks
 
-All features of cleanlab work with **any dataset** and **any model**. Yes, any model: scikit-learn, PyTorch, Tensorflow, Keras, JAX, HuggingFace, MXNet, XGBoost, etc.
+All features of cleanlab work with **any dataset** and **any model**. Yes, any model: PyTorch, Tensorflow, Keras, JAX, HuggingFace, OpenAI, XGBoost, scikit-learn, etc.
 If you use a sklearn-compatible classifier, all cleanlab methods work out-of-the-box.
 
 <details><summary>
 It’s also easy to use your favorite non-sklearn-compatible model (<b>click to learn more</b>)
 </summary>
 <br/>
 
 cleanlab can find label issues from any model's predicted class probabilities if you can produce them yourself.
 
-Some other cleanlab functionality requires your model to be sklearn-compatible.
+Some cleanlab functionality may require your model to be sklearn-compatible.
 There's nothing you need to do if your model already has `.fit()`, `.predict()`, and `.predict_proba()` methods.
 Otherwise, just wrap your custom model into a Python class that inherits the `sklearn.base.BaseEstimator`:
 
 ``` python
 from sklearn.base import BaseEstimator
 class YourFavoriteModel(BaseEstimator): # Inherits sklearn base classifier
     def __init__(self, ):
@@ -147,15 +146,15 @@
 cl.predict(test_data)
 ```
 
 #### Want to see a working example? [Here’s a compliant PyTorch MNIST CNN class](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/experimental/mnist_pytorch.py)
 
 More details are provided in documentation of [cleanlab.classification.CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html).
 
-Note, some libraries exist to give you sklearn-compatibility for free. For PyTorch, check out the [skorch](https://skorch.readthedocs.io/) Python library which will wrap your PyTorch model into a sklearn-compatible model ([example](https://docs.cleanlab.ai/stable/tutorials/image.html)). For TensorFlow/Keras, check out [SciKeras](https://www.adriangb.com/scikeras/) ([example](https://docs.cleanlab.ai/stable/tutorials/text.html)) or [our own Keras wrapper](https://docs.cleanlab.ai/stable/cleanlab/experimental/keras.html). Many libraries also already offer a special scikit-learn API, for example: [XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_api.html#module-xgboost.sklearn) or [LightGBM](https://lightgbm.readthedocs.io/en/latest/pythonapi/lightgbm.LGBMClassifier.html).
+Note, some libraries exist to give you sklearn-compatibility for free. For PyTorch, check out the [skorch](https://skorch.readthedocs.io/) Python library which will wrap your PyTorch model into a sklearn-compatible model ([example](https://docs.cleanlab.ai/stable/tutorials/image.html)). For TensorFlow/Keras, check out our [Keras wrapper](https://docs.cleanlab.ai/stable/cleanlab/models/keras.html). Many libraries also already offer a special scikit-learn API, for example: [XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_api.html#module-xgboost.sklearn) or [LightGBM](https://lightgbm.readthedocs.io/en/latest/pythonapi/lightgbm.LGBMClassifier.html).
 
 <br/>
 </details>
 
 cleanlab is useful across a wide variety of Machine Learning tasks. Specific tasks this package offers dedicated functionality for include:
 1. [Binary and multi-class classification](https://docs.cleanlab.ai/stable/tutorials/indepth_overview.html)
 2. [Multi-label classification](https://docs.cleanlab.ai/stable/tutorials/multilabel_classification.html) (e.g. image/document tagging)
@@ -213,15 +212,15 @@
 </summary>
 <br/>
 
 cleanlab is a general tool that can learn with noisy labels regardless of dataset distribution or classifier type: [examples/classifier\_comparison](https://github.com/cleanlab/examples/blob/master/classifier_comparison/classifier_comparison.ipynb).
 
 ![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/demo_cleanlab_across_datasets_and_classifiers.png)
 
-Each sub-figure above depicts the decision boundary learned using [cleanlab.classification.CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) in the presence of extreme (\~35%) label errors (circled in green). Label noise is class-conditional (not uniformly random). Columns are organized by the classifier used, except the left-most column which depicts the ground-truth data distribution. Rows are organized by dataset.
+Each sub-figure above depicts the decision boundary learned using [cleanlab.classification.CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) in the presence of extreme (\~35%) label errors (circled in green). Label noise is class-conditional (not uniformly random). Columns are organized by the classifier used, except the left-most column which depicts the ground-truth data distribution. Rows are organized by dataset.
 
 Each sub-figure depicts accuracy scores on a test set (with correct non-noisy labels) as decimal values:
 
 * LEFT (in black): The classifier test accuracy trained with perfect labels (no label errors).
 * MIDDLE (in blue): The classifier test accuracy trained with noisy labels using cleanlab.
 * RIGHT (in white): The baseline classifier test accuracy trained with noisy labels.
 
@@ -285,20 +284,20 @@
 
 <details><summary>
 cleanlab for advanced users
 (<b>click to learn more</b>)
 </summary>
 <br/>
 
-Many methods and their default parameters are not covered here. Check out the [documentation for the master branch version](https://docs.cleanlab.ai/master/) for the full suite of features supported by the cleanlab API.
+Many methods and their default parameters are not covered here. Check out the [documentation for the developer version (aka master branch)](https://docs.cleanlab.ai/master/) for the full suite of features supported by the cleanlab API.
 
 ## Use any custom model's predicted probabilities to find label errors in 1 line of code
 
 pred_probs (num_examples x num_classes matrix of predicted probabilities) should already be computed on your own, with any classifier. For best results, pred_probs should be obtained in a holdout/out-of-sample manner (e.g. via cross-validation).
-* cleanlab can do this for you via [`cleanlab.count.estimate_cv_predicted_probabilities`](https://docs.cleanlab.ai/master/cleanlab/count.html)]
+* cleanlab can do this for you via [`cleanlab.count.estimate_cv_predicted_probabilities`](https://docs.cleanlab.ai/stable/cleanlab/count.html)]
 * Tutorial with more info: [[here](https://docs.cleanlab.ai/stable/tutorials/pred_probs_cross_val.html)]
 * Examples how to compute pred_probs with: [[CNN image classifier (PyTorch)](https://docs.cleanlab.ai/stable/tutorials/image.html)], [[NN text classifier (TensorFlow)](https://docs.cleanlab.ai/stable/tutorials/text.html)]
 
 ```python
 # label issues are ordered by likelihood of being an error. First index is most likely error.
 from cleanlab.filter import find_label_issues
 
@@ -383,33 +382,33 @@
 
 <details><summary>
 Positive-Unlabeled Learning
 (<b>click to learn more</b>)
 </summary>
 <br/>
 
-Positive-Unlabeled (PU) learning (in which your data only contains a few positively labeled examples with the rest unlabeled) is just a special case of [CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) when one of the classes has no error. `P` stands for the positive class and **is assumed to have zero label errors** and `U` stands for unlabeled data, but in practice, we just assume the `U` class is a noisy negative class that actually contains some positive examples. Thus, the goal of PU learning is to (1) estimate the proportion of negatively labeled examples that actually belong to the positive class (see`fraction\_noise\_in\_unlabeled\_class` in the last example), (2) find the errors (see last example), and (3) train on clean data (see first example below). cleanlab does all three, taking into account that there are no label errors in whichever class you specify as positive.
+Positive-Unlabeled (PU) learning (in which your data only contains a few positively labeled examples with the rest unlabeled) is just a special case of [CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) when one of the classes has no error. `P` stands for the positive class and **is assumed to have zero label errors** and `U` stands for unlabeled data, but in practice, we just assume the `U` class is a noisy negative class that actually contains some positive examples. Thus, the goal of PU learning is to (1) estimate the proportion of negatively labeled examples that actually belong to the positive class (see`fraction\_noise\_in\_unlabeled\_class` in the last example), (2) find the errors (see last example), and (3) train on clean data (see first example below). cleanlab does all three, taking into account that there are no label errors in whichever class you specify as positive.
 
 There are two ways to use cleanlab for PU learning. We'll look at each here.
 
-Method 1. If you are using the cleanlab classifier [CleanLearning()](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141), and your dataset has exactly two classes (positive = 1, and negative = 0), PU
+Method 1. If you are using the cleanlab classifier [CleanLearning()](https://docs.cleanlab.ai/stable/cleanlab/classification.html), and your dataset has exactly two classes (positive = 1, and negative = 0), PU
 learning is supported directly in cleanlab. You can perform PU learning like this:
 
 ``` python
 from cleanlab.classification import CleanLearning
 from sklearn.linear_model import LogisticRegression
 # Wrap around any classifier. Yup, you can use sklearn/pyTorch/TensorFlow/FastText/etc.
 pu_class = 0 # Should be 0 or 1. Label of class with NO ERRORS. (e.g., P class in PU)
 cl = CleanLearning(clf=LogisticRegression(), pulearning=pu_class)
 cl.fit(X=X_train_data, labels=train_noisy_labels)
 # Estimate the predictions you would have gotten by training with *no* label errors.
 predicted_test_labels = cl.predict(X_test)
 ```
 
-Method 2. However, you might be using a more complicated classifier that doesn't work well with [CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) (see this example for CIFAR-10). Or you might have 3 or more classes. Here's how to use cleanlab for PU learning in this situation. To let cleanlab know which class has no error (in standard PU learning, this is the P class), you need to set the threshold for that class to 1 (1 means the probability that the labels of that class are correct is 1, i.e. that class has no
+Method 2. However, you might be using a more complicated classifier that doesn't work well with [CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) (see this example for CIFAR-10). Or you might have 3 or more classes. Here's how to use cleanlab for PU learning in this situation. To let cleanlab know which class has no error (in standard PU learning, this is the P class), you need to set the threshold for that class to 1 (1 means the probability that the labels of that class are correct is 1, i.e. that class has no
 error). Here's the code:
 
 ``` python
 import numpy as np
 # K is the number of classes in your dataset
 # pred_probs are the cross-validated predicted probabilities.
 # s is the array/list/iterable of noisy labels
@@ -519,26 +518,50 @@
         author={Goh, Hui Wen and Tkachenko, Ulyana and Mueller, Jonas},
         booktitle={NeurIPS Human in the Loop Learning Workshop},
         year={2022}
     }
 
 </details>
 
+<details><summary><a href="https://arxiv.org/abs/2301.11856"> ActiveLab: Active learning with data re-labeling (ICLR '23)</a> (<b>click to show bibtex</b>) </summary>
+
+    @inproceedings{goh2023activelab,
+        title={ActiveLab: Active Learning with Re-Labeling by Multiple Annotators},
+        author={Goh, Hui Wen and Mueller, Jonas},
+        booktitle={ICLR Workshop on Trustworthy ML},
+        year={2023}
+    }
+
+</details>
+
+<details><summary><a href="https://arxiv.org/abs/2211.13895"> Incorrect Annotations in Multi-Label Classification (ICLR '23)</a> (<b>click to show bibtex</b>) </summary>
+
+    @inproceedings{thyagarajan2023multilabel,
+        title={Identifying Incorrect Annotations in Multi-Label Classification Data},
+        author={Thyagarajan, Aditya and Snorrason, Elías and Northcutt, Curtis and Mueller, Jonas},
+        booktitle={ICLR Workshop on Trustworthy ML},
+        year={2023}
+    }
+
+</details>
+
 
 To understand/cite other cleanlab functionality not described above, check out our [additional publications](https://cleanlab.ai/research/).
 
 
 ## Other resources
 
 - [Cleanlab Blog](https://cleanlab.ai/blog/)
 
 - [Blog post: Introduction to Confident Learning](https://l7.curtisnorthcutt.com/confident-learning)
 
 - [NeurIPS 2021 paper: Pervasive Label Errors in Test Sets Destabilize Machine Learning Benchmarks](https://arxiv.org/abs/2103.14749)
 
+- [Release notes for past versions](https://github.com/cleanlab/cleanlab/releases)
+
 - [Cleanlab Studio](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio): No-code Data Improvement
 
 While this open-source library **finds** data issues, an interface is needed to efficiently **fix** these issues in your dataset. [Cleanlab Studio](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio) is a no-code platform to find and fix problems in real-world ML datasets. Studio automatically runs optimized versions of the algorithms from this open-source library on top of AutoML models fit to your data, and presents detected issues in a smart data editing interface. Think of it like a data cleaning assistant that helps you quickly improve the quality of your data (via AI/automation + streamlined UX).
 
 ## Join our community
 
 * The best place to learn is [our Slack community](https://cleanlab.ai/slack).
@@ -548,18 +571,19 @@
 * Interested in contributing? See the [contributing guide](CONTRIBUTING.md) and [ideas on useful contributions](https://github.com/cleanlab/cleanlab/wiki#ideas-for-contributing-to-cleanlab). We welcome your help building a standard open-source library for data-centric AI!
 
 * Have code improvements for cleanlab? See the [development guide](DEVELOPMENT.md).
 
 * Have an issue with cleanlab? [Search existing issues](https://github.com/cleanlab/cleanlab/issues?q=is%3Aissue) or [submit a new issue](https://github.com/cleanlab/cleanlab/issues/new).
 
 * Need professional help with cleanlab?
-Join our [\#help Slack channel](https://cleanlab.ai/slack) and message one of our core developers, Jonas Mueller, or schedule a meeting via email: team@cleanlab.ai
+Join our [\#help Slack channel](https://cleanlab.ai/slack) and message us there, or reach out via email: team@cleanlab.ai
 
 ## License
 
-Copyright (c) 2017-2023 Cleanlab Inc.
+Copyright (c) 2017 Cleanlab Inc.
 
 cleanlab is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
 
 cleanlab is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
 
 See [GNU Affero General Public LICENSE](https://github.com/cleanlab/cleanlab/blob/master/LICENSE) for details.
+You can email us to discuss licensing: team@cleanlab.ai
```

### Comparing `cleanlab-2.3.0/cleanlab/benchmarking/noise_generation.py` & `cleanlab-2.3.1/cleanlab/benchmarking/noise_generation.py`

 * *Files 3% similar despite different names*

```diff
@@ -22,14 +22,15 @@
 generating noisy labels given a noise matrix, generating valid noise matrices with a specific trace value, and more.
 """
 
 from typing import Optional
 
 import numpy as np
 from cleanlab.internal.util import value_counts
+from cleanlab.internal.constants import FLOATING_POINT_COMPARISON
 
 
 def noise_matrix_is_valid(noise_matrix, py, *, verbose=False) -> bool:
     """Given a prior `py` representing ``p(true_label=k)``, checks if the given `noise_matrix` is a
     learnable matrix. Learnability means that it is possible to achieve
     better than random performance, on average, for the amount of noise in
     `noise_matrix`.
@@ -61,15 +62,15 @@
 
     ps = np.dot(noise_matrix, py)  # P(true_label=k)
 
     # P(label=k, true_label=k')
     joint_noise = np.multiply(noise_matrix, py)  # / float(N)
 
     # Check that joint_probs is valid probability matrix
-    if not (abs(joint_noise.sum() - 1.0) < 1e-6):
+    if not (abs(joint_noise.sum() - 1.0) < FLOATING_POINT_COMPARISON):
         return False
 
     # Check that noise_matrix is a valid matrix
     # i.e. check p(label=k)*p(true_label=k) < p(label=k, true_label=k)
     for i in range(K):
         C = N * joint_noise[i][i]
         E1 = N * joint_noise[i].sum() - C
@@ -382,31 +383,29 @@
 
     Returns
     -------
     probabilities : np.ndarray
       An array of probabilities.
     """
 
-    epsilon = 1e-6  # Imprecision allowed for inequalities with floats
-
     if n == 0:
         return np.array([])
-    if (max_prob + epsilon) < m / float(n):
+    if (max_prob + FLOATING_POINT_COMPARISON) < m / float(n):
         raise ValueError(
             "max_prob must be greater or equal to m / n, but "
             + "max_prob = "
             + str(max_prob)
             + ", m = "
             + str(m)
             + ", n = "
             + str(n)
             + ", m / n = "
             + str(m / float(n))
         )
-    if min_prob > (m + epsilon) / float(n):
+    if min_prob > (m + FLOATING_POINT_COMPARISON) / float(n):
         raise ValueError(
             "min_prob must be less or equal to m / n, but "
             + "max_prob = "
             + str(max_prob)
             + ", m = "
             + str(m)
             + ", n = "
@@ -418,26 +417,26 @@
     # When max_prob = 1, min_prob = 0, the next two lines are equivalent to:
     #   intermediate = np.sort(np.append(np.random.uniform(0, 1, n-1), [0, 1]))
     #   result = (intermediate[1:] - intermediate[:-1]) * m
     result = np.random.dirichlet(np.ones(n)) * m
 
     min_val = min(result)
     max_val = max(result)
-    while max_val > (max_prob + epsilon):
+    while max_val > (max_prob + FLOATING_POINT_COMPARISON):
         new_min = min_val + (max_val - max_prob)
         # This adjustment prevents the new max from always being max_prob.
         adjustment = (max_prob - new_min) * np.random.rand()
         result[np.argmin(result)] = new_min + adjustment
         result[np.argmax(result)] = max_prob - adjustment
         min_val = min(result)
         max_val = max(result)
 
     min_val = min(result)
     max_val = max(result)
-    while min_val < (min_prob - epsilon):
+    while min_val < (min_prob - FLOATING_POINT_COMPARISON):
         min_val = min(result)
         max_val = max(result)
         new_max = max_val - (min_prob - min_val)
         # This adjustment prevents the new min from always being min_prob.
         adjustment = (new_max - min_prob) * np.random.rand()
         result[np.argmax(result)] = new_max - adjustment
         result[np.argmin(result)] = min_prob + adjustment
```

### Comparing `cleanlab-2.3.0/cleanlab/classification.py` & `cleanlab-2.3.1/cleanlab/classification.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/count.py` & `cleanlab-2.3.1/cleanlab/count.py`

 * *Files 1% similar despite different names*

```diff
@@ -34,26 +34,27 @@
 import sklearn.base
 import numpy as np
 import warnings
 from typing import Tuple, Union, Optional
 
 from cleanlab.typing import LabelLike
 from cleanlab.internal.multilabel_utils import stack_complement, get_onehot_num_classes
+from cleanlab.internal.constants import TINY_VALUE, CONFIDENT_THRESHOLDS_LOWER_BOUND
+
 from cleanlab.internal.util import (
     value_counts_fill_missing_classes,
     clip_values,
     clip_noise_rates,
     round_preserving_row_totals,
     append_extra_datapoint,
     train_val_split,
     get_num_classes,
     get_unique_classes,
     is_torch_dataset,
     is_tensorflow_dataset,
-    TINY_VALUE,
 )
 from cleanlab.internal.latent_algebra import (
     compute_inv_noise_matrix,
     compute_py,
     compute_noise_matrix_from_inverse,
 )
 from cleanlab.internal.validation import (
@@ -384,15 +385,20 @@
         calibrated_cj = compute_confident_joint(
             labels,
             pred_probs,
             calibrate=True,
             multi_label=multi_label,
         )
     else:
-        calibrated_cj = calibrate_confident_joint(confident_joint, labels, multi_label=multi_label)
+        if labels is not None:
+            calibrated_cj = calibrate_confident_joint(
+                confident_joint, labels, multi_label=multi_label
+            )
+        else:
+            calibrated_cj = confident_joint
 
     assert isinstance(calibrated_cj, np.ndarray)
     if multi_label:
         if not isinstance(labels, list):
             raise TypeError("`labels` must be list when `multi_label=True`.")
         else:
             return _estimate_joint_multilabel(
@@ -1445,15 +1451,18 @@
         all_classes = range(pred_probs.shape[1])
         unique_classes = get_unique_classes(labels)
         BIG_VALUE = 2
         confident_thresholds = [
             np.mean(pred_probs[:, k][labels == k]) if k in unique_classes else BIG_VALUE
             for k in all_classes
         ]
-        return np.array(confident_thresholds)
+        confident_thresholds = np.clip(
+            confident_thresholds, a_min=CONFIDENT_THRESHOLDS_LOWER_BOUND, a_max=None
+        )
+        return confident_thresholds
 
 
 def _get_confident_thresholds_multilabel(
     labels: list,
     pred_probs: np.ndarray,
 ):
     """Returns expected (average) "self-confidence" for each class.
```

### Comparing `cleanlab-2.3.0/cleanlab/dataset.py` & `cleanlab-2.3.1/cleanlab/dataset.py`

 * *Files 3% similar despite different names*

```diff
@@ -18,14 +18,15 @@
 """
 Provides dataset-level and class-level overviews of issues in your classification dataset.
 If your task allows you to modify the classes in your dataset, this module can help you determine
 which classes to remove (see :py:func:`rank_classes_by_label_quality <cleanlab.dataset.rank_classes_by_label_quality>`)
 and which classes to merge (see :py:func:`find_overlapping_classes <cleanlab.dataset.find_overlapping_classes>`).
 """
 
+from typing import Optional, cast
 import numpy as np
 import pandas as pd
 from cleanlab.count import estimate_joint
 
 
 def rank_classes_by_label_quality(
     labels=None,
@@ -244,15 +245,15 @@
         joint = estimate_joint(
             labels=labels,
             pred_probs=pred_probs,
             confident_joint=confident_joint,
             multi_label=multi_label,
         )
     if num_examples is None:
-        num_examples = _get_num_examples(labels=labels)
+        num_examples = _get_num_examples(labels=labels, confident_joint=confident_joint)
     if asymmetric:
         rcv_list = _2d_matrix_to_row_column_value_list(joint)
         # Remove diagonal elements
         rcv_list = [tup for tup in rcv_list if tup[0] != tup[1]]
     else:  # symmetric
         # Sum the upper and lower triangles and remove the lower triangle and the diagonal
         sym_joint = np.triu(joint) + np.tril(joint).T
@@ -440,15 +441,15 @@
         "overall_label_health_score": health_score,
         "joint": joint,
         "classes_by_label_quality": df_class_label_quality,
         "overlapping_classes": df_overlapping_classes,
     }
 
 
-def _get_num_examples(labels=None) -> int:
+def _get_num_examples(labels=None, confident_joint: Optional[np.ndarray] = None) -> int:
     """Helper method that finds the number of examples from the parameters or throws an error
     if neither parameter is provided.
 
     Parameters
     ----------
     For parameter info, see the docstring of `dataset.find_overlapping_classes`
 
@@ -458,15 +459,15 @@
         The number of examples in the dataset.
 
     Raises
     ------
     ValueError
         If `labels` is None."""
 
-    if labels is not None:
-        num_examples = len(labels)
-    else:
+    if labels is None and confident_joint is None:
         raise ValueError(
-            "Error: num_examples is None. You must provide a value for num_examples "
-            "when calling this method using the joint as an input parameter."
+            "Error: num_examples is None. You must either provide confident_joint, "
+            "or provide both num_example and joint as input parameters."
         )
+    _confident_joint = cast(np.ndarray, confident_joint)
+    num_examples = len(labels) if labels is not None else cast(int, np.sum(_confident_joint))
     return num_examples
```

### Comparing `cleanlab-2.3.0/cleanlab/experimental/cifar_cnn.py` & `cleanlab-2.3.1/cleanlab/experimental/cifar_cnn.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/experimental/coteaching.py` & `cleanlab-2.3.1/cleanlab/experimental/coteaching.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/experimental/label_issues_batched.py` & `cleanlab-2.3.1/cleanlab/experimental/label_issues_batched.py`

 * *Files 2% similar despite different names*

```diff
@@ -30,27 +30,30 @@
 import numpy as np
 from typing import Optional, List, Tuple, Any
 
 from cleanlab.count import get_confident_thresholds
 from cleanlab.rank import find_top_issues, _compute_label_quality_scores
 from cleanlab.typing import LabelLike
 from cleanlab.internal.util import value_counts_fill_missing_classes
+from cleanlab.internal.constants import (
+    CONFIDENT_THRESHOLDS_LOWER_BOUND,
+    FLOATING_POINT_COMPARISON,
+    CLIPPING_LOWER_BOUND,
+)
 
 import platform
 import multiprocessing as mp
 
 try:
     import psutil
 
     PSUTIL_EXISTS = True
 except ImportError:  # pragma: no cover
     PSUTIL_EXISTS = False
 
-EPS = 1e-6  # small number
-
 # global variable for multiproc on linux
 adj_confident_thresholds_shared: np.ndarray
 labels_shared: LabelLike
 pred_probs_shared: np.ndarray
 
 
 def find_label_issues_batched(
@@ -419,15 +422,15 @@
                 print(
                     f"Total number of examples whose labels have been evaluated: {self.examples_processed_quality}"
                 )
             if self.off_diagonal_calibrated:
                 calibrated_prune_counts = (
                     self.prune_counts
                     * self.class_counts
-                    / np.clip(self.normalization, a_min=EPS, a_max=None)
+                    / np.clip(self.normalization, a_min=CLIPPING_LOWER_BOUND, a_max=None)
                 )  # avoid division by 0
                 return np.rint(np.sum(calibrated_prune_counts)).astype("int")
             else:  # not calibrated
                 return self.prune_count
 
     def get_quality_scores(self) -> np.ndarray:
         """
@@ -505,14 +508,17 @@
         batch_class_counts = value_counts_fill_missing_classes(labels, num_classes=self.num_class)
         self.confident_thresholds = (
             self.examples_per_class * self.confident_thresholds
             + batch_class_counts * batch_thresholds
         ) / np.clip(
             self.examples_per_class + batch_class_counts, a_min=1, a_max=None
         )  # avoid division by 0
+        self.confident_thresholds = np.clip(
+            self.confident_thresholds, a_min=CONFIDENT_THRESHOLDS_LOWER_BOUND, a_max=None
+        )
         self.examples_per_class += batch_class_counts
         self.examples_processed_thresh += batch_size
 
     def score_label_quality(
         self,
         labels: LabelLike,
         pred_probs: np.ndarray,
@@ -577,15 +583,15 @@
         thorough = False
         if self.examples_processed_thresh < 1:
             raise ValueError(
                 "Have not computed any confident_thresholds yet. Call `update_confident_thresholds()` first."
             )
 
         if self.n_jobs == 1:
-            adj_confident_thresholds = self.confident_thresholds - EPS
+            adj_confident_thresholds = self.confident_thresholds - FLOATING_POINT_COMPARISON
             pred_class = np.argmax(pred_probs, axis=1)
             batch_size = len(labels)
             if thorough:
                 # add margin for floating point comparison operations:
                 pred_gt_thresholds = pred_probs >= adj_confident_thresholds
                 max_ind = np.argmax(pred_probs * pred_gt_thresholds, axis=1)
                 if not self.off_diagonal_calibrated:
@@ -622,15 +628,15 @@
                         & to_increment
                         & (max_ind != labels)
                         # & (pred_class != labels)
                         # This is not applied in num_label_issues(..., estimation_method="off_diagonal_custom"). Do we want to add it?
                     )
         else:  # multiprocessing implementation
             global adj_confident_thresholds_shared
-            adj_confident_thresholds_shared = self.confident_thresholds - EPS
+            adj_confident_thresholds_shared = self.confident_thresholds - FLOATING_POINT_COMPARISON
 
             global labels_shared, pred_probs_shared
             labels_shared = labels
             pred_probs_shared = pred_probs
 
             # good values for this are ~1000-10000 in benchmarks where pred_probs has 1B entries:
             processes = 5000
```

### Comparing `cleanlab-2.3.0/cleanlab/experimental/mnist_pytorch.py` & `cleanlab-2.3.1/cleanlab/experimental/mnist_pytorch.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/filter.py` & `cleanlab-2.3.1/cleanlab/filter.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/internal/label_quality_utils.py` & `cleanlab-2.3.1/cleanlab/internal/label_quality_utils.py`

 * *Files 5% similar despite different names*

```diff
@@ -18,14 +18,15 @@
 Helper methods used internally for computing label quality scores
 """
 
 import numpy as np
 from typing import Optional
 
 from cleanlab.count import get_confident_thresholds
+from cleanlab.internal.constants import CLIPPING_LOWER_BOUND
 
 
 def _subtract_confident_thresholds(
     labels: Optional[np.ndarray],
     pred_probs: np.ndarray,
     multi_label: bool = False,
     confident_thresholds: Optional[np.ndarray] = None,
@@ -79,15 +80,17 @@
     pred_probs_adj /= pred_probs_adj.sum(axis=1)[
         :, None
     ]  # The [:, None] adds a dimension to make the /= operator work for broadcasting.
 
     return pred_probs_adj
 
 
-def get_normalized_entropy(pred_probs: np.ndarray, min_allowed_prob: float = 1e-6) -> np.ndarray:
+def get_normalized_entropy(
+    pred_probs: np.ndarray, min_allowed_prob: float = CLIPPING_LOWER_BOUND
+) -> np.ndarray:
     """Returns the normalized entropy of pred_probs.
 
     Normalized entropy is between 0 and 1. Higher values of entropy indicate higher uncertainty in the model's prediction of the correct label.
 
     Read more about normalized entropy `on Wikipedia <https://en.wikipedia.org/wiki/Entropy_(information_theory)>`_.
 
     Normalized entropy is used in active learning for uncertainty sampling: https://towardsdatascience.com/uncertainty-sampling-cheatsheet-ec57bc067c0b
```

### Comparing `cleanlab-2.3.0/cleanlab/internal/latent_algebra.py` & `cleanlab-2.3.1/cleanlab/internal/latent_algebra.py`

 * *Files 2% similar despite different names*

```diff
@@ -24,15 +24,16 @@
 Throughout `K` denotes the number of classes in the classification task.
 """
 
 import warnings
 import numpy as np
 from typing import Tuple
 
-from cleanlab.internal.util import value_counts, clip_values, clip_noise_rates, TINY_VALUE
+from cleanlab.internal.util import value_counts, clip_values, clip_noise_rates
+from cleanlab.internal.constants import TINY_VALUE, CLIPPING_LOWER_BOUND
 
 
 def compute_ps_py_inv_noise_matrix(
     labels, noise_matrix
 ) -> Tuple[np.ndarray, np.ndarray, np.ndarray]:
     """Compute ``ps := P(labels=k), py := P(true_labels=k)``, and the inverse noise matrix.
 
@@ -69,15 +70,15 @@
     # 'py' is p(true_labels=k) = noise_matrix^(-1) * p(labels=k)
     # because in *vector computation*: P(label=k|true_label=k) * p(true_label=k) = P(label=k)
     # The pseudo-inverse is used when noise_matrix is not invertible.
     py = np.linalg.inv(noise_matrix).dot(ps)
 
     # No class should have probability 0, so we use .000001
     # Make sure valid probabilities that sum to 1.0
-    py = clip_values(py, low=1e-6, high=1.0, new_sum=1.0)
+    py = clip_values(py, low=CLIPPING_LOWER_BOUND, high=1.0, new_sum=1.0)
 
     # All the work is done in this function (below)
     return py, compute_inv_noise_matrix(py=py, noise_matrix=noise_matrix, ps=ps)
 
 
 def compute_inv_noise_matrix(py, noise_matrix, *, ps=None) -> np.ndarray:
     """Compute the inverse noise matrix if py := P(true_label=k) is given.
@@ -263,16 +264,16 @@
     elif py_method == "marginal_ps":
         py = np.dot(inverse_noise_matrix, ps)
     else:
         err = "py_method {}".format(py_method)
         err += " should be in [cnt, eqn, marginal, marginal_ps]"
         raise ValueError(err)
 
-    # Clip py (0,1), s.t. no class should have prob 0, hence 1e-5
-    py = clip_values(py, low=1e-5, high=1.0, new_sum=1.0)
+    # Clip py (0,1), s.t. no class should have prob 0, hence 1e-6
+    py = clip_values(py, low=CLIPPING_LOWER_BOUND, high=1.0, new_sum=1.0)
     return py
 
 
 def compute_pyx(pred_probs, noise_matrix, inverse_noise_matrix):
     """Compute ``pyx := P(true_label=k|x)`` from ``pred_probs := P(label=k|x)``, `noise_matrix` and
     `inverse_noise_matrix`.
```

### Comparing `cleanlab-2.3.0/cleanlab/internal/multiannotator_utils.py` & `cleanlab-2.3.1/cleanlab/internal/multiannotator_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -125,54 +125,61 @@
                 f"pred_probs must have at least {int(highest_class)} columns based on the largest class label "
                 "which appears in labels_multiannotator. Perhaps some rarely-annotated classes were lost while "
                 "establishing consensus labels used to train your classifier."
             )
 
 
 def assert_valid_pred_probs(
-    pred_probs: np.ndarray,
+    pred_probs: Optional[np.ndarray] = None,
     pred_probs_unlabeled: Optional[np.ndarray] = None,
     ensemble: bool = False,
 ):
-    """Validate format of pred_probs for multiannotator functions"""
+    """Validate format of pred_probs for multiannotator active learning functions"""
+    if pred_probs is None and pred_probs_unlabeled is None:
+        raise ValueError(
+            "pred_probs and pred_probs_unlabeled cannot both be None, specify at least one of the two."
+        )
+
     if ensemble:
-        if pred_probs.ndim != 3:
-            error_message = "pred_probs must be a 3d array."
-            if pred_probs.ndim == 2:  # pragma: no cover
-                error_message += " If you have a 2d pred_probs array, use the non-ensemble version of this function."
-            raise ValueError(error_message)
+        if pred_probs is not None:
+            if pred_probs.ndim != 3:
+                error_message = "pred_probs must be a 3d array."
+                if pred_probs.ndim == 2:  # pragma: no cover
+                    error_message += " If you have a 2d pred_probs array (ie. only one predictor), use the non-ensemble version of this function."
+                raise ValueError(error_message)
 
         if pred_probs_unlabeled is not None:
             if pred_probs_unlabeled.ndim != 3:
                 error_message = "pred_probs_unlabeled must be a 3d array."
                 if pred_probs_unlabeled.ndim == 2:  # pragma: no cover
                     error_message += " If you have a 2d pred_probs_unlabeled array, use the non-ensemble version of this function."
                 raise ValueError(error_message)
 
+        if pred_probs is not None and pred_probs_unlabeled is not None:
             if pred_probs.shape[2] != pred_probs_unlabeled.shape[2]:
                 raise ValueError(
                     "pred_probs and pred_probs_unlabeled must have the same number of classes"
                 )
 
     else:
-        if pred_probs.ndim != 2:
-            error_message = "pred_probs must be a 2d array."
-            if pred_probs.ndim == 3:  # pragma: no cover
-                error_message += (
-                    " If you have a 3d pred_probs array, use the ensemble version of this function."
-                )
-            raise ValueError(error_message)
+        if pred_probs is not None:
+            if pred_probs.ndim != 2:
+                error_message = "pred_probs must be a 2d array."
+                if pred_probs.ndim == 3:  # pragma: no cover
+                    error_message += " If you have a 3d pred_probs array, use the ensemble version of this function."
+                raise ValueError(error_message)
 
         if pred_probs_unlabeled is not None:
             if pred_probs_unlabeled.ndim != 2:
                 error_message = "pred_probs_unlabeled must be a 2d array."
                 if pred_probs_unlabeled.ndim == 3:  # pragma: no cover
                     error_message += " If you have a 3d pred_probs_unlabeled array, use the non-ensemble version of this function."
                 raise ValueError(error_message)
 
+        if pred_probs is not None and pred_probs_unlabeled is not None:
             if pred_probs.shape[1] != pred_probs_unlabeled.shape[1]:
                 raise ValueError(
                     "pred_probs and pred_probs_unlabeled must have the same number of classes"
                 )
 
 
 def format_multiannotator_labels(labels: LabelLike) -> Tuple[pd.DataFrame, dict]:
```

### Comparing `cleanlab-2.3.0/cleanlab/internal/multilabel_scorer.py` & `cleanlab-2.3.1/cleanlab/internal/multilabel_scorer.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/internal/multilabel_utils.py` & `cleanlab-2.3.1/cleanlab/internal/multilabel_utils.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/internal/token_classification_utils.py` & `cleanlab-2.3.1/cleanlab/internal/token_classification_utils.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/internal/util.py` & `cleanlab-2.3.1/cleanlab/internal/util.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,17 +21,15 @@
 import warnings
 import numpy as np
 import pandas as pd
 from typing import Union, Tuple
 
 from cleanlab.typing import DatasetLike, LabelLike
 from cleanlab.internal.validation import labels_to_array
-
-
-TINY_VALUE = 1e-100
+from cleanlab.internal.constants import FLOATING_POINT_COMPARISON, TINY_VALUE
 
 
 def remove_noise_from_class(noise_matrix, class_without_noise) -> np.ndarray:
     """A helper function in the setting of PU learning.
     Sets all P(label=class_without_noise|true_label=any_other_class) = 0
     in noise_matrix for pulearning setting, where we have
     generalized the positive class in PU learning to be any
@@ -230,15 +228,15 @@
         The iterable rounded to int, preserving sum."""
 
     floats = np.asarray(iterable, dtype=float)
     ints = floats.round()
     orig_sum = np.sum(floats).round()
     int_sum = np.sum(ints).round()
     # Adjust the integers so that they sum to orig_sum
-    while abs(int_sum - orig_sum) > 1e-6:
+    while abs(int_sum - orig_sum) > FLOATING_POINT_COMPARISON:
         diff = np.round(orig_sum - int_sum)
         increment = -1 if int(diff < 0.0) else 1
         changes = min(int(abs(diff)), len(iterable))
         # Orders indices by difference. Increments # of changes.
         indices = np.argsort(floats - ints)[::-increment][:changes]
         for i in indices:
             ints[i] = ints[i] + increment
```

### Comparing `cleanlab-2.3.0/cleanlab/internal/validation.py` & `cleanlab-2.3.1/cleanlab/internal/validation.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,14 +15,15 @@
 # along with cleanlab.  If not, see <https://www.gnu.org/licenses/>.
 
 """
 Checks to ensure valid inputs for various methods.
 """
 
 from cleanlab.typing import LabelLike, DatasetLike
+from cleanlab.internal.constants import FLOATING_POINT_COMPARISON
 from typing import Any, List, Optional, Union
 import warnings
 import numpy as np
 import pandas as pd
 
 
 def assert_valid_inputs(
@@ -91,15 +92,17 @@
             assert all(isinstance(y_i, list) for y_i in y)
             highest_class = max([max(y_i) for y_i in y if len(y_i) != 0]) + 1
         if pred_probs.shape[1] < highest_class:
             raise ValueError(
                 f"pred_probs must have at least {highest_class} columns, based on the largest class index which appears in labels."
             )
         # Check for valid probabilities.
-        if (np.min(pred_probs) < 0) or (np.max(pred_probs) > 1):
+        if (np.min(pred_probs) < 0 - FLOATING_POINT_COMPARISON) or (
+            np.max(pred_probs) > 1 + FLOATING_POINT_COMPARISON
+        ):
             raise ValueError("Values in pred_probs must be between 0 and 1.")
         if X is not None:
             warnings.warn("When X and pred_probs are both provided, the former may be ignored.")
 
 
 def assert_valid_class_labels(
     y: np.ndarray,
```

### Comparing `cleanlab-2.3.0/cleanlab/models/fasttext.py` & `cleanlab-2.3.1/cleanlab/models/fasttext.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/models/keras.py` & `cleanlab-2.3.1/cleanlab/models/keras.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/multiannotator.py` & `cleanlab-2.3.1/cleanlab/multiannotator.py`

 * *Files 2% similar despite different names*

```diff
@@ -21,36 +21,40 @@
 :py:func:`get_label_quality_multiannotator <cleanlab.multiannotator.get_label_quality_multiannotator>` function which estimates:
 
 * A consensus label for each example that aggregates the individual annotations more accurately than alternative aggregation via majority-vote or other algorithms used in crowdsourcing like Dawid-Skene.
 * A quality score for each consensus label which measures our confidence that this label is correct.
 * An analogous label quality score for each individual label chosen by one annotator for a particular example.
 * An overall quality score for each annotator which measures our confidence in the overall correctness of labels obtained from this annotator.
 
-The underlying algorithms used to compute the statistics are described in `the CROWDLAB paper <https://arxiv.org/abs/2210.06812>`_.
+The algorithms to compute these estimates are described in `the CROWDLAB paper <https://arxiv.org/abs/2210.06812>`_.
 
 If you have some labeled and unlabeled data (with multiple annotators for some labeled examples) and want to decide what data to collect additional labels for,
 use the :py:func:`get_active_learning_scores <cleanlab.multiannotator.get_active_learning_scores>` function, which is intended for active learning. 
-This function estimates an active learning quality score for each example,
+This function estimates an ActiveLab quality score for each example,
 which can be used to prioritize which examples are most informative to collect additional labels for.
 This function is effective for settings where some examples have been labeled by one or more annotators and other examples can have no labels at all so far,
 as well as settings where new labels are collected either in batches of examples or one at a time. 
-Here is an `example notebook <https://github.com/cleanlab/examples/blob/master/active_learning_multiannotator/active_learning.ipynb>`_ showcasing the use of this function in multiple active learning rounds.
+Here is an `example notebook <https://github.com/cleanlab/examples/blob/master/active_learning_multiannotator/active_learning.ipynb>`_ showcasing the use of this ActiveLab method for active learning with data re-labeling.
+
+The algorithms to compute these active learning scores are described in `the ActiveLab paper <https://arxiv.org/abs/2301.11856>`_.
 
 Each of the main functions in this module utilizes any trained classifier model.
 Variants of these functions are provided for settings where you have trained an ensemble of multiple models.
 """
 
 import warnings
 import numpy as np
 import pandas as pd
 
 from typing import List, Dict, Any, Union, Tuple, Optional
 
 from cleanlab.rank import get_label_quality_scores
 from cleanlab.internal.util import get_num_classes, value_counts
+from cleanlab.internal.constants import CLIPPING_LOWER_BOUND
+
 from cleanlab.internal.multiannotator_utils import (
     assert_valid_inputs_multiannotator,
     assert_valid_pred_probs,
     check_consensus_label_classes,
     find_best_temp_scaler,
     temp_scale_pred_probs,
 )
@@ -65,26 +69,26 @@
     calibrate_probs: bool = False,
     return_detailed_quality: bool = True,
     return_annotator_stats: bool = True,
     return_weights: bool = False,
     verbose: bool = True,
     label_quality_score_kwargs: dict = {},
 ) -> Dict[str, Any]:
-    """Returns label quality scores for each example and for each annotator.
+    """Returns label quality scores for each example and for each annotator in a dataset labeled by multiple annotators.
 
     This function is for multiclass classification datasets where examples have been labeled by
     multiple annotators (not necessarily the same number of annotators per example).
 
     It computes one consensus label for each example that best accounts for the labels chosen by each
     annotator (and their quality), as well as a consensus quality score for how confident we are that this consensus label is actually correct.
     It also computes similar quality scores for each annotator's individual labels, and the quality of each annotator.
-    Scores are between 0 and 1; lower scores indicate labels/annotators less likely to be correct.
+    Scores are between 0 and 1 (estimated via methods like CROWDLAB); lower scores indicate labels/annotators less likely to be correct.
 
     To decide what data to collect additional labels for, try the :py:func:`get_active_learning_scores <cleanlab.multiannotator.get_active_learning_scores>`
-    function, which is intended for active learning with multiple annotators.
+    (ActiveLab) function, which is intended for active learning with multiple annotators.
 
     Parameters
     ----------
     labels_multiannotator : pd.DataFrame of np.ndarray
         2D pandas DataFrame or array of multiple given labels for each example with shape ``(N, M)``,
         where N is the number of examples and M is the number of annotators.
         ``labels_multiannotator[n][m]`` = label for n-th example given by m-th annotator.
@@ -531,113 +535,143 @@
         labels_info["model_weight"] = model_weight
         labels_info["annotator_weight"] = annotator_weight
 
     return labels_info
 
 
 def get_active_learning_scores(
-    labels_multiannotator: Union[pd.DataFrame, np.ndarray],
-    pred_probs: np.ndarray,
+    labels_multiannotator: Optional[Union[pd.DataFrame, np.ndarray]] = None,
+    pred_probs: Optional[np.ndarray] = None,
     pred_probs_unlabeled: Optional[np.ndarray] = None,
 ) -> Tuple[np.ndarray, np.ndarray]:
-    """Returns an active learning quality score for each example in the dataset.
+    """Returns an ActiveLab quality score for each example in the dataset, to estimate which examples are most informative to (re)label next in active learning.
 
     We consider settings where one example can be labeled by one or more annotators and some examples have no labels at all so far.
 
     The score is in between 0 and 1, and can be used to prioritize what data to collect additional labels for.
     Lower scores indicate examples whose true label we are least confident about based on the current data;
     collecting additional labels for these low-scoring examples will be more informative than collecting labels for other examples.
     To use an annotation budget most efficiently, select a batch of examples with the lowest scores and collect one additional label for each example,
     and repeat this process after retraining your classifier.
 
+    You can use this function to get active learning scores for: examples that already have one or more labels (specify ``labels_multiannotator`` and ``pred_probs``
+    as arguments), or for unlabeled examples (specify ``pred_probs_unlabeled``), or for both types of examples (specify all of the above arguments).
+
     To analyze a fixed dataset labeled by multiple annotators rather than collecting additional labels, try the
-    :py:func:`get_label_quality_multiannotator <cleanlab.multiannotator.get_label_quality_multiannotator>` function instead.
+    :py:func:`get_label_quality_multiannotator <cleanlab.multiannotator.get_label_quality_multiannotator>` (CROWDLAB) function instead.
 
     Parameters
     ----------
-    labels_multiannotator : pd.DataFrame of np.ndarray
+    labels_multiannotator : pd.DataFrame of np.ndarray, optional
         2D pandas DataFrame or array of multiple given labels for each example with shape ``(N, M)``,
         where N is the number of examples and M is the number of annotators. Note that this function also works with
         datasets where there is only one annotator (M=1).
         For more details, labels in the same format expected by the :py:func:`get_label_quality_multiannotator <cleanlab.multiannotator.get_label_quality_multiannotator>`.
         Note that examples that have no annotator labels should not be included in this DataFrame/array.
-    pred_probs : np.ndarray
+        This argument is optional if ``pred_probs`` is not provided (you might only provide ``pred_probs_unlabeled`` to only get active learning scores for the unlabeled examples).
+    pred_probs : np.ndarray, optional
         An array of shape ``(N, K)`` of predicted class probabilities from a trained classifier model.
         Predicted probabilities in the same format expected by the :py:func:`get_label_quality_scores <cleanlab.rank.get_label_quality_scores>`.
+        This argument is optional if you only want to get active learning scores for unlabeled examples (specify only ``pred_probs_unlabeled`` instead).
     pred_probs_unlabeled : np.ndarray, optional
         An array of shape ``(N, K)`` of predicted class probabilities from a trained classifier model for examples that have no annotator labels.
         Predicted probabilities in the same format expected by the :py:func:`get_label_quality_scores <cleanlab.rank.get_label_quality_scores>`.
+        This argument is optional if you only want to get active learning scores for already-labeled examples (specify only ``pred_probs`` instead).
 
     Returns
     -------
     active_learning_scores : np.ndarray
-        Array of shape ``(N,)`` indicating the active learning quality scores for each example.
+        Array of shape ``(N,)`` indicating the ActiveLab quality scores for each example.
+        This array is empty if no already-labeled data was provided via ``labels_multiannotator``.
         Examples with the lowest scores are those we should label next in order to maximally improve our classifier model.
 
     active_learning_scores_unlabeled : np.ndarray
         Array of shape ``(N,)`` indicating the active learning quality scores for each unlabeled example.
         Returns an empty array if no unlabeled data is provided.
         Examples with the lowest scores are those we should label next in order to maximally improve our classifier model
         (scores for unlabeled data are directly comparable with the `active_learning_scores` for labeled data).
     """
 
-    if isinstance(labels_multiannotator, np.ndarray):
-        labels_multiannotator = pd.DataFrame(labels_multiannotator)
-
     assert_valid_pred_probs(pred_probs=pred_probs, pred_probs_unlabeled=pred_probs_unlabeled)
 
-    num_classes = get_num_classes(pred_probs=pred_probs)
+    # compute multiannotator stats if labeled data is provided
+    if pred_probs is not None:
+        if labels_multiannotator is None:
+            raise ValueError(
+                "labels_multiannotator cannot be None when passing in pred_probs. ",
+                "Either provide labels_multiannotator to obtain active learning scores for the labeled examples, "
+                "or just pass in pred_probs_unlabeled to get active learning scores for unlabeled examples.",
+            )
 
-    # if all examples are only labeled by a single annotator
-    if labels_multiannotator.apply(lambda s: len(s.dropna()) == 1, axis=1).all():
-        optimal_temp = 1.0  # do not temp scale for single annotator case, temperature is defined here for later use
+        if isinstance(labels_multiannotator, np.ndarray):
+            labels_multiannotator = pd.DataFrame(labels_multiannotator)
 
-        assert_valid_inputs_multiannotator(
-            labels_multiannotator, pred_probs, allow_single_label=True
-        )
+        num_classes = get_num_classes(pred_probs=pred_probs)
 
-        consensus_label = get_majority_vote_label(
-            labels_multiannotator=labels_multiannotator,
-            pred_probs=pred_probs,
-            verbose=False,
-        )
-        quality_of_consensus_labeled = get_label_quality_scores(consensus_label, pred_probs)
-        model_weight = 1
-        annotator_weight = np.full(labels_multiannotator.shape[1], 1)
-        avg_annotator_weight = np.mean(annotator_weight)
+        # if all examples are only labeled by a single annotator
+        if labels_multiannotator.apply(lambda s: len(s.dropna()) == 1, axis=1).all():
+            optimal_temp = 1.0  # do not temp scale for single annotator case, temperature is defined here for later use
 
-    else:
-        optimal_temp = find_best_temp_scaler(labels_multiannotator, pred_probs)
-        pred_probs = temp_scale_pred_probs(pred_probs, optimal_temp)
+            assert_valid_inputs_multiannotator(
+                labels_multiannotator, pred_probs, allow_single_label=True
+            )
 
-        multiannotator_info = get_label_quality_multiannotator(
-            labels_multiannotator,
-            pred_probs,
-            return_annotator_stats=False,
-            return_detailed_quality=False,
-            return_weights=True,
-        )
+            consensus_label = get_majority_vote_label(
+                labels_multiannotator=labels_multiannotator,
+                pred_probs=pred_probs,
+                verbose=False,
+            )
+            quality_of_consensus_labeled = get_label_quality_scores(consensus_label, pred_probs)
+            model_weight = 1
+            annotator_weight = np.full(labels_multiannotator.shape[1], 1)
+            avg_annotator_weight = np.mean(annotator_weight)
 
-        quality_of_consensus_labeled = multiannotator_info["label_quality"][
-            "consensus_quality_score"
-        ]
-        model_weight = multiannotator_info["model_weight"]
-        annotator_weight = multiannotator_info["annotator_weight"]
-        avg_annotator_weight = np.mean(annotator_weight)
-
-    # compute scores for labeled data
-    active_learning_scores = np.full(len(labels_multiannotator), np.nan)
-    for i in range(len(active_learning_scores)):
-        annotator_labels = labels_multiannotator.iloc[i]
-        active_learning_scores[i] = np.average(
-            (quality_of_consensus_labeled[i], 1 / num_classes),
-            weights=(
-                np.sum(annotator_weight[annotator_labels.notna()]) + model_weight,
-                avg_annotator_weight,
-            ),
+        # examples are annotated by multiple annotators
+        else:
+            optimal_temp = find_best_temp_scaler(labels_multiannotator, pred_probs)
+            pred_probs = temp_scale_pred_probs(pred_probs, optimal_temp)
+
+            multiannotator_info = get_label_quality_multiannotator(
+                labels_multiannotator,
+                pred_probs,
+                return_annotator_stats=False,
+                return_detailed_quality=False,
+                return_weights=True,
+            )
+
+            quality_of_consensus_labeled = multiannotator_info["label_quality"][
+                "consensus_quality_score"
+            ]
+            model_weight = multiannotator_info["model_weight"]
+            annotator_weight = multiannotator_info["annotator_weight"]
+            avg_annotator_weight = np.mean(annotator_weight)
+
+        # compute scores for labeled data
+        active_learning_scores = np.full(len(labels_multiannotator), np.nan)
+        for i in range(len(active_learning_scores)):
+            annotator_labels = labels_multiannotator.iloc[i]
+            active_learning_scores[i] = np.average(
+                (quality_of_consensus_labeled[i], 1 / num_classes),
+                weights=(
+                    np.sum(annotator_weight[annotator_labels.notna()]) + model_weight,
+                    avg_annotator_weight,
+                ),
+            )
+
+    # no labeled data provided so do not estimate temperature and model/annotator weights
+    elif pred_probs_unlabeled is not None:
+        num_classes = get_num_classes(pred_probs=pred_probs_unlabeled)
+        optimal_temp = 1
+        model_weight = 1
+        avg_annotator_weight = 1
+        active_learning_scores = np.array([])
+
+    else:
+        raise ValueError(
+            "pred_probs and pred_probs_unlabeled cannot both be None, specify at least one of the two."
         )
 
     # compute scores for unlabeled data
     if pred_probs_unlabeled is not None:
         pred_probs_unlabeled = temp_scale_pred_probs(pred_probs_unlabeled, optimal_temp)
         quality_of_consensus_unlabeled = np.max(pred_probs_unlabeled, axis=1)
 
@@ -655,112 +689,136 @@
     else:
         active_learning_scores_unlabeled = np.array([])
 
     return active_learning_scores, active_learning_scores_unlabeled
 
 
 def get_active_learning_scores_ensemble(
-    labels_multiannotator: Union[pd.DataFrame, np.ndarray],
-    pred_probs: np.ndarray,
+    labels_multiannotator: Optional[Union[pd.DataFrame, np.ndarray]] = None,
+    pred_probs: Optional[np.ndarray] = None,
     pred_probs_unlabeled: Optional[np.ndarray] = None,
 ) -> Tuple[np.ndarray, np.ndarray]:
-    """Returns an active learning quality score for each example in the dataset, based on predictions from an ensemble of models.
+    """Returns an ActiveLab quality score for each example in the dataset, based on predictions from an ensemble of models.
 
     This function is similar to :py:func:`get_active_learning_scores <cleanlab.multiannotator.get_active_learning_scores>` but allows for an
-    ensemble of multiple classifier models to be trained and will aggregate predictions from the models to compute the active learning quality score.
+    ensemble of multiple classifier models to be trained and will aggregate predictions from the models to compute the ActiveLab quality score.
 
     Parameters
     ----------
     labels_multiannotator : pd.DataFrame or np.ndarray
         Multiannotator labels in the same format expected by :py:func:`get_active_learning_scores <cleanlab.multiannotator.get_active_learning_scores>`.
+        This argument is optional if ``pred_probs`` is not provided (in cases where you only provide ``pred_probs_unlabeled`` to get active learning scores for unlabeled examples).
     pred_probs : np.ndarray
         An array of shape ``(P, N, K)`` where P is the number of models, consisting of predicted class probabilities from the ensemble models.
         Note that this function also works with datasets where there is only one annotator (M=1).
         Each set of predicted probabilities with shape ``(N, K)`` is in the same format expected by the :py:func:`get_label_quality_scores <cleanlab.rank.get_label_quality_scores>`.
+        This argument is optional if you only want to get active learning scores for unlabeled examples (pass in ``pred_probs_unlabeled`` instead).
     pred_probs_unlabeled : np.ndarray, optional
         An array of shape ``(P, N, K)`` where P is the number of models, consisting of predicted class probabilities from a trained classifier model
         for examples that have no annotated labels so far (but which we may want to label in the future, and hence compute active learning quality scores for).
         Each set of predicted probabilities with shape ``(N, K)`` is in the same format expected by the :py:func:`get_label_quality_scores <cleanlab.rank.get_label_quality_scores>`.
+        This argument is optional if you only want to get active learning scores for labeled examples (pass in ``pred_probs`` instead).
 
     Returns
     -------
     active_learning_scores : np.ndarray
         Similar to output as :py:func:`get_label_quality_scores <cleanlab.multiannotator.get_label_quality_scores>`.
     active_learning_scores_unlabeled : np.ndarray
         Similar to output as :py:func:`get_label_quality_scores <cleanlab.multiannotator.get_label_quality_scores>`.
 
     See Also
     --------
     get_active_learning_scores
     """
 
-    if isinstance(labels_multiannotator, np.ndarray):
-        labels_multiannotator = pd.DataFrame(labels_multiannotator)
-
     assert_valid_pred_probs(
         pred_probs=pred_probs, pred_probs_unlabeled=pred_probs_unlabeled, ensemble=True
     )
 
-    num_classes = get_num_classes(pred_probs=pred_probs[0])
+    # compute multiannotator stats if labeled data is provided
+    if pred_probs is not None:
+        if labels_multiannotator is None:
+            raise ValueError(
+                "labels_multiannotator cannot be None when passing in pred_probs. ",
+                "You can either provide labels_multiannotator to obtain active learning scores for the labeled examples, "
+                "or just pass in pred_probs_unlabeled to get active learning scores for unlabeled examples.",
+            )
 
-    # temp scale pred_probs
+        if isinstance(labels_multiannotator, np.ndarray):
+            labels_multiannotator = pd.DataFrame(labels_multiannotator)
 
-    # if all examples are only labeled by a single annotator
-    if labels_multiannotator.apply(lambda s: len(s.dropna()) == 1, axis=1).all():
-        # do not temp scale for single annotator case, temperature is defined here for later use
-        optimal_temp = np.full(len(pred_probs), 1.0)
+        num_classes = get_num_classes(pred_probs=pred_probs[0])
 
-        assert_valid_inputs_multiannotator(
-            labels_multiannotator, pred_probs, ensemble=True, allow_single_label=True
-        )
+        # if all examples are only labeled by a single annotator
+        if labels_multiannotator.apply(lambda s: len(s.dropna()) == 1, axis=1).all():
+            # do not temp scale for single annotator case, temperature is defined here for later use
+            optimal_temp = np.full(len(pred_probs), 1.0)
 
-        avg_pred_probs = np.mean(pred_probs, axis=0)
-        consensus_label = get_majority_vote_label(
-            labels_multiannotator=labels_multiannotator,
-            pred_probs=avg_pred_probs,
-            verbose=False,
-        )
-        quality_of_consensus_labeled = get_label_quality_scores(consensus_label, avg_pred_probs)
-        model_weight = np.full(len(pred_probs), 1)
-        annotator_weight = np.full(labels_multiannotator.shape[1], 1)
-        avg_annotator_weight = np.mean(annotator_weight)
+            assert_valid_inputs_multiannotator(
+                labels_multiannotator, pred_probs, ensemble=True, allow_single_label=True
+            )
 
-    else:
-        optimal_temp = np.full(len(pred_probs), np.NaN)
-        for i in range(len(pred_probs)):
-            curr_pred_probs = pred_probs[i]
-            curr_optimal_temp = find_best_temp_scaler(labels_multiannotator, curr_pred_probs)
-            pred_probs[i] = temp_scale_pred_probs(curr_pred_probs, curr_optimal_temp)
-            optimal_temp[i] = curr_optimal_temp
-
-        multiannotator_info = get_label_quality_multiannotator_ensemble(
-            labels_multiannotator,
-            pred_probs,
-            return_annotator_stats=False,
-            return_detailed_quality=False,
-            return_weights=True,
-        )
+            avg_pred_probs = np.mean(pred_probs, axis=0)
+            consensus_label = get_majority_vote_label(
+                labels_multiannotator=labels_multiannotator,
+                pred_probs=avg_pred_probs,
+                verbose=False,
+            )
+            quality_of_consensus_labeled = get_label_quality_scores(consensus_label, avg_pred_probs)
+            model_weight = np.full(len(pred_probs), 1)
+            annotator_weight = np.full(labels_multiannotator.shape[1], 1)
+            avg_annotator_weight = np.mean(annotator_weight)
 
-        quality_of_consensus_labeled = multiannotator_info["label_quality"][
-            "consensus_quality_score"
-        ]
-        model_weight = multiannotator_info["model_weight"]
-        annotator_weight = multiannotator_info["annotator_weight"]
-        avg_annotator_weight = np.mean(annotator_weight)
-
-    # compute scores for labeled data
-    active_learning_scores = np.full(len(labels_multiannotator), np.nan)
-    for i in range(len(active_learning_scores)):
-        annotator_labels = labels_multiannotator.iloc[i]
-        active_learning_scores[i] = np.average(
-            (quality_of_consensus_labeled[i], 1 / num_classes),
-            weights=(
-                np.sum(annotator_weight[annotator_labels.notna()]) + np.sum(model_weight),
-                avg_annotator_weight,
-            ),
+        # examples are annotated by multiple annotators
+        else:
+            optimal_temp = np.full(len(pred_probs), np.NaN)
+            for i in range(len(pred_probs)):
+                curr_pred_probs = pred_probs[i]
+                curr_optimal_temp = find_best_temp_scaler(labels_multiannotator, curr_pred_probs)
+                pred_probs[i] = temp_scale_pred_probs(curr_pred_probs, curr_optimal_temp)
+                optimal_temp[i] = curr_optimal_temp
+
+            multiannotator_info = get_label_quality_multiannotator_ensemble(
+                labels_multiannotator,
+                pred_probs,
+                return_annotator_stats=False,
+                return_detailed_quality=False,
+                return_weights=True,
+            )
+
+            quality_of_consensus_labeled = multiannotator_info["label_quality"][
+                "consensus_quality_score"
+            ]
+            model_weight = multiannotator_info["model_weight"]
+            annotator_weight = multiannotator_info["annotator_weight"]
+            avg_annotator_weight = np.mean(annotator_weight)
+
+        # compute scores for labeled data
+        active_learning_scores = np.full(len(labels_multiannotator), np.nan)
+        for i in range(len(active_learning_scores)):
+            annotator_labels = labels_multiannotator.iloc[i]
+            active_learning_scores[i] = np.average(
+                (quality_of_consensus_labeled[i], 1 / num_classes),
+                weights=(
+                    np.sum(annotator_weight[annotator_labels.notna()]) + np.sum(model_weight),
+                    avg_annotator_weight,
+                ),
+            )
+
+    # no labeled data provided so do not estimate temperature and model/annotator weights
+    elif pred_probs_unlabeled is not None:
+        num_classes = get_num_classes(pred_probs=pred_probs_unlabeled[0])
+        optimal_temp = np.full(len(pred_probs_unlabeled), 1.0)
+        model_weight = np.full(len(pred_probs_unlabeled), 1)
+        avg_annotator_weight = 1
+        active_learning_scores = np.array([])
+
+    else:
+        raise ValueError(
+            "pred_probs and pred_probs_unlabeled cannot both be None, specify at least one of the two."
         )
 
     # compute scores for unlabeled data
     if pred_probs_unlabeled is not None:
         for i in range(len(pred_probs_unlabeled)):
             pred_probs_unlabeled[i] = temp_scale_pred_probs(
                 pred_probs_unlabeled[i], optimal_temp[i]
@@ -853,42 +911,49 @@
             if len(max_pred_probs) == 1:
                 majority_vote_label[idx] = label_mode[max_pred_probs[0]]
                 del tied_idx[idx]
             else:
                 tied_idx[idx] = label_mode[max_pred_probs]
 
     # tiebreak 2: using empirical class frequencies
+    # current tiebreak will select the minority class (to prevent larger class imbalance)
     if len(tied_idx) > 0:
         if pred_probs is not None:
             num_classes = pred_probs.shape[1]
         else:
             num_classes = int(
                 np.nanmax(labels_multiannotator.replace({pd.NA: np.NaN}).astype(float).values) + 1
             )
         class_frequencies = labels_multiannotator.apply(
             lambda s: pd.Series(np.bincount(s[s.notna()], minlength=num_classes)), axis=1
         ).sum()
         for idx, label_mode in tied_idx.copy().items():
-            max_frequency = np.where(
-                class_frequencies[label_mode] == np.max(class_frequencies[label_mode])
+            min_frequency = np.where(
+                class_frequencies[label_mode] == np.min(class_frequencies[label_mode])
             )[0]
-            if len(max_frequency) == 1:
-                majority_vote_label[idx] = label_mode[max_frequency[0]]
+            if len(min_frequency) == 1:
+                majority_vote_label[idx] = label_mode[min_frequency[0]]
                 del tied_idx[idx]
             else:
-                tied_idx[idx] = label_mode[max_frequency]
+                tied_idx[idx] = label_mode[min_frequency]
 
     # tiebreak 3: using initial annotator quality scores
     if len(tied_idx) > 0:
         nontied_majority_vote_label = majority_vote_label[nontied_idx]
         nontied_labels_multiannotator = labels_multiannotator.iloc[nontied_idx]
         annotator_agreement_with_consensus = nontied_labels_multiannotator.apply(
             lambda s: np.mean(s[pd.notna(s)] == nontied_majority_vote_label[pd.notna(s)]),
             axis=0,
-        ).to_numpy()
+        )
+
+        # impute average annotator accuracy for any annotator that do not overlap with consensus
+        mask = annotator_agreement_with_consensus.isna()
+        avg_annotator_agreement = np.mean(annotator_agreement_with_consensus[~mask])
+        annotator_agreement_with_consensus[mask] = avg_annotator_agreement
+
         for idx, label_mode in tied_idx.copy().items():
             label_quality_score = np.array(
                 [
                     np.mean(
                         annotator_agreement_with_consensus[
                             labels_multiannotator.iloc[idx][
                                 labels_multiannotator.iloc[idx] == label
@@ -1290,32 +1355,32 @@
 
         # compute most likely class error
         most_likely_class_error = np.clip(
             np.mean(
                 consensus_label_subset
                 != np.argmax(np.bincount(consensus_label_subset, minlength=num_classes))
             ),
-            a_min=1e-6,
+            a_min=CLIPPING_LOWER_BOUND,
             a_max=None,
         )
 
         # compute adjusted annotator agreement (used as annotator weights)
         annotator_agreement_with_annotators = _get_annotator_agreement_with_annotators(
             labels_multiannotator, num_annotations, verbose
         )
         annotator_error = 1 - annotator_agreement_with_annotators
         adjusted_annotator_agreement = np.clip(
-            1 - (annotator_error / most_likely_class_error), a_min=1e-6, a_max=None
+            1 - (annotator_error / most_likely_class_error), a_min=CLIPPING_LOWER_BOUND, a_max=None
         )
 
         # compute model weight
         model_error = np.mean(np.argmax(prior_pred_probs_subset, axis=1) != consensus_label_subset)
-        model_weight = np.max([(1 - (model_error / most_likely_class_error)), 1e-6]) * np.sqrt(
-            np.mean(num_annotations)
-        )
+        model_weight = np.max(
+            [(1 - (model_error / most_likely_class_error)), CLIPPING_LOWER_BOUND]
+        ) * np.sqrt(np.mean(num_annotations))
 
         # compute weighted average
         post_pred_probs = np.full(prior_pred_probs.shape, np.nan)
         for i in range(len(labels_multiannotator)):
             example_mask = labels_multiannotator.iloc[i].notna()
             example = labels_multiannotator.iloc[i][example_mask]
             post_pred_probs[i] = [
@@ -1416,36 +1481,36 @@
 
     # compute most likely class error
     most_likely_class_error = np.clip(
         np.mean(
             consensus_label_subset
             != np.argmax(np.bincount(consensus_label_subset, minlength=num_classes))
         ),
-        a_min=1e-6,
+        a_min=CLIPPING_LOWER_BOUND,
         a_max=None,
     )
 
     # compute adjusted annotator agreement (used as annotator weights)
     annotator_agreement_with_annotators = _get_annotator_agreement_with_annotators(
         labels_multiannotator, num_annotations, verbose
     )
     annotator_error = 1 - annotator_agreement_with_annotators
     adjusted_annotator_agreement = np.clip(
-        1 - (annotator_error / most_likely_class_error), a_min=1e-6, a_max=None
+        1 - (annotator_error / most_likely_class_error), a_min=CLIPPING_LOWER_BOUND, a_max=None
     )
 
     # compute model weight
     model_weight = np.full(prior_pred_probs.shape[0], np.nan)
     for idx in range(prior_pred_probs.shape[0]):
         prior_pred_probs_subset = prior_pred_probs[idx][mask]
 
         model_error = np.mean(np.argmax(prior_pred_probs_subset, axis=1) != consensus_label_subset)
-        model_weight[idx] = np.max([(1 - (model_error / most_likely_class_error)), 1e-6]) * np.sqrt(
-            np.mean(num_annotations)
-        )
+        model_weight[idx] = np.max(
+            [(1 - (model_error / most_likely_class_error)), CLIPPING_LOWER_BOUND]
+        ) * np.sqrt(np.mean(num_annotations))
 
     # compute weighted average
     post_pred_probs = np.full(prior_pred_probs[0].shape, np.nan)
     for i in range(len(labels_multiannotator)):
         example_mask = labels_multiannotator.iloc[i].notna()
         example = labels_multiannotator.iloc[i][example_mask]
         post_pred_probs[i] = [
```

### Comparing `cleanlab-2.3.0/cleanlab/multilabel_classification.py` & `cleanlab-2.3.1/cleanlab/multilabel_classification.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/outlier.py` & `cleanlab-2.3.1/cleanlab/outlier.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/rank.py` & `cleanlab-2.3.1/cleanlab/rank.py`

 * *Files 0% similar despite different names*

```diff
@@ -33,14 +33,18 @@
 
 import numpy as np
 from sklearn.metrics import log_loss
 from typing import List, Optional
 import warnings
 
 from cleanlab.internal.validation import assert_valid_inputs
+from cleanlab.internal.constants import (
+    CLIPPING_LOWER_BOUND,
+)  # lower-bound clipping threshold to prevents 0 in logs and division
+
 from cleanlab.internal.label_quality_utils import (
     _subtract_confident_thresholds,
     get_normalized_entropy,
 )
 
 
 def get_label_quality_scores(
@@ -232,16 +236,14 @@
       Lower scores indicate more likely mislabeled examples.
 
     See Also
     --------
     get_label_quality_scores
     """
 
-    MIN_ALLOWED = 1e-6  # lower-bound clipping threshold to prevents 0 in logs and division
-
     # Check pred_probs_list for errors
     assert isinstance(
         pred_probs_list, list
     ), f"pred_probs_list needs to be a list. Provided pred_probs_list is a {type(pred_probs_list)}"
 
     assert len(pred_probs_list) > 0, "pred_probs_list is empty."
 
@@ -273,15 +275,15 @@
 
         for t in log_loss_search_T_values:
             neg_log_loss_list = []
 
             # pred_probs for each model
             for pred_probs in pred_probs_list:
                 pred_probs_clipped = np.clip(
-                    pred_probs, a_min=MIN_ALLOWED, a_max=None
+                    pred_probs, a_min=CLIPPING_LOWER_BOUND, a_max=None
                 )  # lower-bound clipping threshold to prevents 0 in logs when calculating log loss
                 pred_probs_clipped /= pred_probs_clipped.sum(axis=1)[:, np.newaxis]  # renormalize
 
                 neg_log_loss = np.exp(-t * log_loss(labels, pred_probs_clipped))
                 neg_log_loss_list.append(neg_log_loss)
 
             # weights using negative log loss
@@ -570,19 +572,18 @@
     Returns
     -------
     label_quality_scores : np.ndarray
       Contains one score (between 0 and 1) per example.
       Lower scores indicate more likely mislabeled examples.
     """
 
-    MIN_ALLOWED = 1e-6  # lower-bound clipping threshold to prevents 0 in logs and division
     self_confidence = get_self_confidence_for_each_label(labels, pred_probs)
-    self_confidence = np.clip(self_confidence, a_min=MIN_ALLOWED, a_max=None)
+    self_confidence = np.clip(self_confidence, a_min=CLIPPING_LOWER_BOUND, a_max=None)
 
     # Divide entropy by self confidence
     label_quality_scores = get_normalized_entropy(pred_probs) / self_confidence
 
     # Rescale
-    clipped_scores = np.clip(label_quality_scores, a_min=MIN_ALLOWED, a_max=None)
+    clipped_scores = np.clip(label_quality_scores, a_min=CLIPPING_LOWER_BOUND, a_max=None)
     label_quality_scores = np.log(label_quality_scores + 1) / clipped_scores
 
     return label_quality_scores
```

### Comparing `cleanlab-2.3.0/cleanlab/token_classification/filter.py` & `cleanlab-2.3.1/cleanlab/token_classification/filter.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/token_classification/rank.py` & `cleanlab-2.3.1/cleanlab/token_classification/rank.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/token_classification/summary.py` & `cleanlab-2.3.1/cleanlab/token_classification/summary.py`

 * *Files identical despite different names*

### Comparing `cleanlab-2.3.0/cleanlab/version.py` & `cleanlab-2.3.1/cleanlab/version.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,28 +11,28 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU Affero General Public License for more details.
 #
 # You should have received a copy of the GNU Affero General Public License
 # along with cleanlab.  If not, see <https://www.gnu.org/licenses/>.
 
 
-__version__ = "2.3.0"
+__version__ = "2.3.1"
+
+# 2.3.2 - Not yet released, you are using bleeding-edge developer version. See its documentation at: https://docs.cleanlab.ai/master/
+
+# ------------------------------------------------
+# | PREVIOUS MAJOR VERSION RELEASE NOTES SUMMARY |
+# ------------------------------------------------
 
 # 2.3.0 - Extending cleanlab beyond label errors into a complete library for data-centric AI
 #
 #   Major new functionalities include:
 #   - Active learning with data re-labeling (ActiveLab)
 #   - KerasWrapperModel and KerasSequentialWrapper to make arbitrary Keras models compatible with scikit-learn
 #   - Computational improvements for detecting label issues (better efficiency and mini-batch estimation that works with lower memory)
-#
-#   See release for a full changelog.
-
-# ------------------------------------------
-# | PREVIOUS VERSION RELEASE NOTES SUMMARY |
-# ------------------------------------------
 
 # 2.2.0 - Re-invented algorithms for multi-label classification and support for datasets with missing classes
 #
 #   For detecting label errors in multi-label classification datasets (e.g. image/document tagging):
 #   - Added cleanlab.multilabel_classification module for label quality scoring.
 #   - Re-invented better algorithms and published paper describing how the new algorithms work and benchmarking their effectiveness.
 #   - Provided new quickstart tutorials and examples on how to use cleanlab for multi-label datasets and train effective models for them.
```

### Comparing `cleanlab-2.3.0/cleanlab.egg-info/PKG-INFO` & `cleanlab-2.3.1/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -1,49 +1,17 @@
-Metadata-Version: 2.1
-Name: cleanlab
-Version: 2.3.0
-Summary: The standard package for data-centric AI, machine learning with label errors, and automatically finding and fixing dataset issues in Python.
-Home-page: https://cleanlab.ai
-Author: Cleanlab Inc.
-Author-email: team@cleanlab.ai
-License: AGPLv3+
-Project-URL: Documentation, https://docs.cleanlab.ai
-Project-URL: Bug Tracker, https://github.com/cleanlab/cleanlab/issues
-Project-URL: Source Code, https://github.com/cleanlab/cleanlab
-Keywords: machine_learning data_cleaning confident_learning classification weak_supervision learning_with_noisy_labels unsupervised_learning datacentric_ai,datacentric
-Classifier: Development Status :: 4 - Beta
-Classifier: Intended Audience :: Developers
-Classifier: Intended Audience :: Education
-Classifier: Intended Audience :: Science/Research
-Classifier: Intended Audience :: Information Technology
-Classifier: License :: OSI Approved :: GNU Affero General Public License v3 or later (AGPLv3+)
-Classifier: Natural Language :: English
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python
-Classifier: Topic :: Software Development
-Classifier: Topic :: Scientific/Engineering
-Classifier: Topic :: Scientific/Engineering :: Mathematics
-Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
-Classifier: Topic :: Software Development :: Libraries
-Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-License-File: LICENSE
+<p align="center">
+  <img src="https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/cleanlab_logo_open_source_transparent_optimized_size.png" width=60% height=60%>
+</p>
 
-![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/cleanlab_logo_open_source_transparent_optimized_size.png)
 
-cleanlab automatically detects problems in a ML dataset. This data-centric AI package facilitates **machine learning with messy, real-world data** by providing **clean lab**els for robust training and flagging errors in your data.
+cleanlab helps you **clean** data and **lab**els by automatically detecting issues in a ML dataset. To facilitate **machine learning with messy, real-world data**, this data-centric AI package uses your *existing* models to estimate dataset problems that can be fixed to train even *better* models.
 
 ```python
 
-# cleanlab works with **any classifier**. Yup, you can use sklearn/PyTorch/TensorFlow/XGBoost/etc.
+# cleanlab works with **any classifier**. Yup, you can use PyTorch/TensorFlow/OpenAI/XGBoost/etc.
 cl = cleanlab.classification.CleanLearning(sklearn.YourFavoriteClassifier())
 
 # cleanlab finds data and label issues in **any dataset**... in ONE line of code!
 label_issues = cl.find_label_issues(data, labels)
 
 # cleanlab trains a robust version of your model that works more reliably with noisy data.
 cl.fit(data, labels)
@@ -69,95 +37,56 @@
 [![docs](https://img.shields.io/static/v1?logo=github&style=flat&color=pink&label=docs&message=cleanlab)](https://docs.cleanlab.ai/)
 [![Slack Community](https://img.shields.io/static/v1?logo=slack&style=flat&color=white&label=slack&message=community)](https://cleanlab.ai/slack)
 [![Twitter](https://img.shields.io/twitter/follow/CleanlabAI?style=social)](https://twitter.com/CleanlabAI)
 [![Cleanlab Studio](https://raw.githubusercontent.com/cleanlab/assets/master/shields/cl-studio-shield.svg)](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio)
 
 -----
 
-<details><summary><b>News! (2022) </b> -- cleanlab made accessible for everybody, not just ML researchers (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Nov 2022 📖</b> cleanlab 2.2.0 released! Added better algorithms for: label issues in multi-label classification, data with some classes absent, and estimating the number of label errors in a dataset. </li>
-<li> <b>Sep 2022 📖</b> cleanlab 2.1.0 released! Added support for: data labeled by multiple annotators in cleanlab.multiannotator, token classification with text data in cleanlab.token_classification, out-of-distribution detection in cleanlab.outlier, and CleanLearning with non-numpy-array data (e.g. pandas dataframes, tensorflow/pytorch datasets, etc) in cleanlab.classification.CleanLearning. </li>
-<li> <b>April 2022 📖</b> cleanlab 2.0.0 released! Lays foundations for this library to grow into a general-purpose data-centric AI toolkit. </li>
-<li> <b>March 2022 📖</b>  Documentation migrated to new website: <a href="https://docs.cleanlab.ai/">docs.cleanlab.ai</a> with quickstart tutorials for image/text/audio/tabular data.</li>
-<li> <b>Feb 2022 💻</b> <a href="https://docs.cleanlab.ai/master/migrating/migrate_v2.html">APIs simplified</a> to make cleanlab accessible for everybody, not just ML researchers </li>
-<li> <b>Long-time cleanlab user?</b> Here's <a href="https://docs.cleanlab.ai/stable/migrating/migrate_v2.html">how to migrate</a> to cleanlab versions >= 2.0.0. </li>
-</ul>
-</p>
-</details>
-
-<details><summary><b>News! (2021) </b> -- cleanlab finds pervasive label errors in the most common ML datasets (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Dec 2021 🎉</b>  NeurIPS published the <a href="https://arxiv.org/abs/2103.14749">label errors paper (Northcutt, Athalye, & Mueller, 2021)</a>.</li>
-<li> <b>Apr 2021 🎉</b>  Journal of AI Research published the <a href="https://jair.org/index.php/jair/article/view/12125">confident learning paper (Northcutt, Jiang, & Chuang, 2021)</a>.</li>
-<li> <b>Mar 2021 😲</b>  cleanlab used to find and fix label issues in 10 of the most common ML benchmark datasets, published in: <a href="https://neurips.cc/Conferences/2021/ScheduleMultitrack?event=22763">NeurIPS 2021</a>. Along with <a href="https://arxiv.org/abs/2103.14749">the paper (Northcutt, Athalye, & Mueller, 2021)</a>, the authors launched <a href="https://labelerrors.com">labelerrors.com</a> where you can view the label issues in these datasets.</li>
-</ul>
-</p>
-</details>
-
-<details><summary><b>News! (2020) </b> -- cleanlab supports all OS, achieves state-of-the-art performance (<b>click to learn more</b>) </summary>
-<p>
-<ul>
-<li> <b>Dec 2020 🎉</b>  cleanlab supports NeurIPS workshop paper <a href="https://securedata.lol/camera_ready/28.pdf">(Northcutt, Athalye, & Lin, 2020)</a>.</li>
-<li> <b>Dec 2020 🤖</b>  cleanlab supports <a href="https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L215">PU learning</a>.</li>
-<li> <b>Feb 2020 🤖</b>  cleanlab now natively supports Mac, Linux, and Windows.</li>
-<li> <b>Feb 2020 🤖</b>  cleanlab now supports <a href="https://github.com/cleanlab/cleanlab/blob/master/cleanlab/experimental/coteaching.py">Co-Teaching</a> <a href="https://arxiv.org/abs/1804.06872">(Han et al., 2018)</a>.</li>
-<li> <b>Jan 2020 🎉</b> cleanlab achieves state-of-the-art on CIFAR-10 with noisy labels. Code to reproduce:  <a href="https://github.com/cleanlab/examples/tree/master/contrib/v1/cifar10">examples/cifar10</a>. This is a great place to see how to use cleanlab on real datasets (with predicted probabilities from trained model already precomputed for you).</li>
-</ul>
-</p>
-</details>
-
-Release notes for past versions are [here](https://github.com/cleanlab/cleanlab/releases).
-Details behind updates are explained in our [blog](https://cleanlab.ai/blog/) and [research papers](https://cleanlab.ai/research/).
-
-
 ## So fresh, so cleanlab
 
-cleanlab **clean**s your data's **lab**els via state-of-the-art *confident learning* algorithms, published in this [paper](https://jair.org/index.php/jair/article/view/12125) and [blog](https://l7.curtisnorthcutt.com/confident-learning). See some of the datasets cleaned with cleanlab at [labelerrors.com](https://labelerrors.com). This package helps you find data and label issues so you can train reliable ML models.
+cleanlab **clean**s your data's **lab**els via state-of-the-art *confident learning* algorithms, published in this [paper](https://jair.org/index.php/jair/article/view/12125) and [blog](https://l7.curtisnorthcutt.com/confident-learning). See some of the datasets cleaned with cleanlab at [labelerrors.com](https://labelerrors.com). This package helps you find label issues and other data issues, so you can train reliable ML models.
 
 cleanlab is:
 
 1. **backed by theory**
    - with [provable guarantees](https://arxiv.org/abs/1911.00068) of exact estimation of noise and label errors, even with imperfect models.
 2. **fast**
-   - Code is parallelized (< 1 second to find label issues in ImageNet with pre-computed predictions).
+   - Code is parallelized and scalable.
 4. **easy-to-use**
-   - Find label issues or train noise-robust models in one line of code (no hyperparameters by default).
+   - Find mislabeled data, bad annotators, outliers, or train noise-robust models -- all in one line of code.
 6. **general**
-   - Works with **[any dataset](https://labelerrors.com/)** and **any model**, e.g., TensorFlow, PyTorch, sklearn, XGBoost, Huggingface, etc.
+   - Works with **[any dataset](https://labelerrors.com/)** (text, image, tabular, audio, ...) and **any model** (TensorFlow, PyTorch, JAX, HuggingFace,  OpenAI, XGBoost, scikit-learn, ...)
 <br/>
 
 ![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/label-errors-examples.png)
 <p align="center">
 Examples of incorrect given labels in various image datasets <a href="https://l7.curtisnorthcutt.com/label-errors">found and corrected</a> using cleanlab.
 </p>
 
 ## Run cleanlab
 
 cleanlab supports Linux, macOS, and Windows and runs on Python 3.7+.
 
 - Get started [here](https://docs.cleanlab.ai/)! Install via `pip` or `conda` as described [here](https://docs.cleanlab.ai/).
 - Developers who install the bleeding-edge from source should refer to [this master branch documentation](https://docs.cleanlab.ai/master/index.html).
-
+- For help, check out our detailed [FAQ](https://docs.cleanlab.ai/stable/tutorials/faq.html), [Github Issues](https://github.com/cleanlab/cleanlab/issues?q=is%3Aissue), or [Slack](https://cleanlab.ai/slack). We welcome any questions!
 
 ## Use cleanlab with any model for most ML tasks
 
-All features of cleanlab work with **any dataset** and **any model**. Yes, any model: scikit-learn, PyTorch, Tensorflow, Keras, JAX, HuggingFace, MXNet, XGBoost, etc.
+All features of cleanlab work with **any dataset** and **any model**. Yes, any model: PyTorch, Tensorflow, Keras, JAX, HuggingFace, OpenAI, XGBoost, scikit-learn, etc.
 If you use a sklearn-compatible classifier, all cleanlab methods work out-of-the-box.
 
 <details><summary>
 It’s also easy to use your favorite non-sklearn-compatible model (<b>click to learn more</b>)
 </summary>
 <br/>
 
 cleanlab can find label issues from any model's predicted class probabilities if you can produce them yourself.
 
-Some other cleanlab functionality requires your model to be sklearn-compatible.
+Some cleanlab functionality may require your model to be sklearn-compatible.
 There's nothing you need to do if your model already has `.fit()`, `.predict()`, and `.predict_proba()` methods.
 Otherwise, just wrap your custom model into a Python class that inherits the `sklearn.base.BaseEstimator`:
 
 ``` python
 from sklearn.base import BaseEstimator
 class YourFavoriteModel(BaseEstimator): # Inherits sklearn base classifier
     def __init__(self, ):
@@ -182,15 +111,15 @@
 cl.predict(test_data)
 ```
 
 #### Want to see a working example? [Here’s a compliant PyTorch MNIST CNN class](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/experimental/mnist_pytorch.py)
 
 More details are provided in documentation of [cleanlab.classification.CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html).
 
-Note, some libraries exist to give you sklearn-compatibility for free. For PyTorch, check out the [skorch](https://skorch.readthedocs.io/) Python library which will wrap your PyTorch model into a sklearn-compatible model ([example](https://docs.cleanlab.ai/stable/tutorials/image.html)). For TensorFlow/Keras, check out [SciKeras](https://www.adriangb.com/scikeras/) ([example](https://docs.cleanlab.ai/stable/tutorials/text.html)) or [our own Keras wrapper](https://docs.cleanlab.ai/stable/cleanlab/experimental/keras.html). Many libraries also already offer a special scikit-learn API, for example: [XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_api.html#module-xgboost.sklearn) or [LightGBM](https://lightgbm.readthedocs.io/en/latest/pythonapi/lightgbm.LGBMClassifier.html).
+Note, some libraries exist to give you sklearn-compatibility for free. For PyTorch, check out the [skorch](https://skorch.readthedocs.io/) Python library which will wrap your PyTorch model into a sklearn-compatible model ([example](https://docs.cleanlab.ai/stable/tutorials/image.html)). For TensorFlow/Keras, check out our [Keras wrapper](https://docs.cleanlab.ai/stable/cleanlab/models/keras.html). Many libraries also already offer a special scikit-learn API, for example: [XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_api.html#module-xgboost.sklearn) or [LightGBM](https://lightgbm.readthedocs.io/en/latest/pythonapi/lightgbm.LGBMClassifier.html).
 
 <br/>
 </details>
 
 cleanlab is useful across a wide variety of Machine Learning tasks. Specific tasks this package offers dedicated functionality for include:
 1. [Binary and multi-class classification](https://docs.cleanlab.ai/stable/tutorials/indepth_overview.html)
 2. [Multi-label classification](https://docs.cleanlab.ai/stable/tutorials/multilabel_classification.html) (e.g. image/document tagging)
@@ -248,15 +177,15 @@
 </summary>
 <br/>
 
 cleanlab is a general tool that can learn with noisy labels regardless of dataset distribution or classifier type: [examples/classifier\_comparison](https://github.com/cleanlab/examples/blob/master/classifier_comparison/classifier_comparison.ipynb).
 
 ![](https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/demo_cleanlab_across_datasets_and_classifiers.png)
 
-Each sub-figure above depicts the decision boundary learned using [cleanlab.classification.CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) in the presence of extreme (\~35%) label errors (circled in green). Label noise is class-conditional (not uniformly random). Columns are organized by the classifier used, except the left-most column which depicts the ground-truth data distribution. Rows are organized by dataset.
+Each sub-figure above depicts the decision boundary learned using [cleanlab.classification.CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) in the presence of extreme (\~35%) label errors (circled in green). Label noise is class-conditional (not uniformly random). Columns are organized by the classifier used, except the left-most column which depicts the ground-truth data distribution. Rows are organized by dataset.
 
 Each sub-figure depicts accuracy scores on a test set (with correct non-noisy labels) as decimal values:
 
 * LEFT (in black): The classifier test accuracy trained with perfect labels (no label errors).
 * MIDDLE (in blue): The classifier test accuracy trained with noisy labels using cleanlab.
 * RIGHT (in white): The baseline classifier test accuracy trained with noisy labels.
 
@@ -320,20 +249,20 @@
 
 <details><summary>
 cleanlab for advanced users
 (<b>click to learn more</b>)
 </summary>
 <br/>
 
-Many methods and their default parameters are not covered here. Check out the [documentation for the master branch version](https://docs.cleanlab.ai/master/) for the full suite of features supported by the cleanlab API.
+Many methods and their default parameters are not covered here. Check out the [documentation for the developer version (aka master branch)](https://docs.cleanlab.ai/master/) for the full suite of features supported by the cleanlab API.
 
 ## Use any custom model's predicted probabilities to find label errors in 1 line of code
 
 pred_probs (num_examples x num_classes matrix of predicted probabilities) should already be computed on your own, with any classifier. For best results, pred_probs should be obtained in a holdout/out-of-sample manner (e.g. via cross-validation).
-* cleanlab can do this for you via [`cleanlab.count.estimate_cv_predicted_probabilities`](https://docs.cleanlab.ai/master/cleanlab/count.html)]
+* cleanlab can do this for you via [`cleanlab.count.estimate_cv_predicted_probabilities`](https://docs.cleanlab.ai/stable/cleanlab/count.html)]
 * Tutorial with more info: [[here](https://docs.cleanlab.ai/stable/tutorials/pred_probs_cross_val.html)]
 * Examples how to compute pred_probs with: [[CNN image classifier (PyTorch)](https://docs.cleanlab.ai/stable/tutorials/image.html)], [[NN text classifier (TensorFlow)](https://docs.cleanlab.ai/stable/tutorials/text.html)]
 
 ```python
 # label issues are ordered by likelihood of being an error. First index is most likely error.
 from cleanlab.filter import find_label_issues
 
@@ -418,33 +347,33 @@
 
 <details><summary>
 Positive-Unlabeled Learning
 (<b>click to learn more</b>)
 </summary>
 <br/>
 
-Positive-Unlabeled (PU) learning (in which your data only contains a few positively labeled examples with the rest unlabeled) is just a special case of [CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) when one of the classes has no error. `P` stands for the positive class and **is assumed to have zero label errors** and `U` stands for unlabeled data, but in practice, we just assume the `U` class is a noisy negative class that actually contains some positive examples. Thus, the goal of PU learning is to (1) estimate the proportion of negatively labeled examples that actually belong to the positive class (see`fraction\_noise\_in\_unlabeled\_class` in the last example), (2) find the errors (see last example), and (3) train on clean data (see first example below). cleanlab does all three, taking into account that there are no label errors in whichever class you specify as positive.
+Positive-Unlabeled (PU) learning (in which your data only contains a few positively labeled examples with the rest unlabeled) is just a special case of [CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) when one of the classes has no error. `P` stands for the positive class and **is assumed to have zero label errors** and `U` stands for unlabeled data, but in practice, we just assume the `U` class is a noisy negative class that actually contains some positive examples. Thus, the goal of PU learning is to (1) estimate the proportion of negatively labeled examples that actually belong to the positive class (see`fraction\_noise\_in\_unlabeled\_class` in the last example), (2) find the errors (see last example), and (3) train on clean data (see first example below). cleanlab does all three, taking into account that there are no label errors in whichever class you specify as positive.
 
 There are two ways to use cleanlab for PU learning. We'll look at each here.
 
-Method 1. If you are using the cleanlab classifier [CleanLearning()](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141), and your dataset has exactly two classes (positive = 1, and negative = 0), PU
+Method 1. If you are using the cleanlab classifier [CleanLearning()](https://docs.cleanlab.ai/stable/cleanlab/classification.html), and your dataset has exactly two classes (positive = 1, and negative = 0), PU
 learning is supported directly in cleanlab. You can perform PU learning like this:
 
 ``` python
 from cleanlab.classification import CleanLearning
 from sklearn.linear_model import LogisticRegression
 # Wrap around any classifier. Yup, you can use sklearn/pyTorch/TensorFlow/FastText/etc.
 pu_class = 0 # Should be 0 or 1. Label of class with NO ERRORS. (e.g., P class in PU)
 cl = CleanLearning(clf=LogisticRegression(), pulearning=pu_class)
 cl.fit(X=X_train_data, labels=train_noisy_labels)
 # Estimate the predictions you would have gotten by training with *no* label errors.
 predicted_test_labels = cl.predict(X_test)
 ```
 
-Method 2. However, you might be using a more complicated classifier that doesn't work well with [CleanLearning](https://github.com/cleanlab/cleanlab/blob/master/cleanlab/classification.py#L141) (see this example for CIFAR-10). Or you might have 3 or more classes. Here's how to use cleanlab for PU learning in this situation. To let cleanlab know which class has no error (in standard PU learning, this is the P class), you need to set the threshold for that class to 1 (1 means the probability that the labels of that class are correct is 1, i.e. that class has no
+Method 2. However, you might be using a more complicated classifier that doesn't work well with [CleanLearning](https://docs.cleanlab.ai/stable/cleanlab/classification.html) (see this example for CIFAR-10). Or you might have 3 or more classes. Here's how to use cleanlab for PU learning in this situation. To let cleanlab know which class has no error (in standard PU learning, this is the P class), you need to set the threshold for that class to 1 (1 means the probability that the labels of that class are correct is 1, i.e. that class has no
 error). Here's the code:
 
 ``` python
 import numpy as np
 # K is the number of classes in your dataset
 # pred_probs are the cross-validated predicted probabilities.
 # s is the array/list/iterable of noisy labels
@@ -554,26 +483,50 @@
         author={Goh, Hui Wen and Tkachenko, Ulyana and Mueller, Jonas},
         booktitle={NeurIPS Human in the Loop Learning Workshop},
         year={2022}
     }
 
 </details>
 
+<details><summary><a href="https://arxiv.org/abs/2301.11856"> ActiveLab: Active learning with data re-labeling (ICLR '23)</a> (<b>click to show bibtex</b>) </summary>
+
+    @inproceedings{goh2023activelab,
+        title={ActiveLab: Active Learning with Re-Labeling by Multiple Annotators},
+        author={Goh, Hui Wen and Mueller, Jonas},
+        booktitle={ICLR Workshop on Trustworthy ML},
+        year={2023}
+    }
+
+</details>
+
+<details><summary><a href="https://arxiv.org/abs/2211.13895"> Incorrect Annotations in Multi-Label Classification (ICLR '23)</a> (<b>click to show bibtex</b>) </summary>
+
+    @inproceedings{thyagarajan2023multilabel,
+        title={Identifying Incorrect Annotations in Multi-Label Classification Data},
+        author={Thyagarajan, Aditya and Snorrason, Elías and Northcutt, Curtis and Mueller, Jonas},
+        booktitle={ICLR Workshop on Trustworthy ML},
+        year={2023}
+    }
+
+</details>
+
 
 To understand/cite other cleanlab functionality not described above, check out our [additional publications](https://cleanlab.ai/research/).
 
 
 ## Other resources
 
 - [Cleanlab Blog](https://cleanlab.ai/blog/)
 
 - [Blog post: Introduction to Confident Learning](https://l7.curtisnorthcutt.com/confident-learning)
 
 - [NeurIPS 2021 paper: Pervasive Label Errors in Test Sets Destabilize Machine Learning Benchmarks](https://arxiv.org/abs/2103.14749)
 
+- [Release notes for past versions](https://github.com/cleanlab/cleanlab/releases)
+
 - [Cleanlab Studio](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio): No-code Data Improvement
 
 While this open-source library **finds** data issues, an interface is needed to efficiently **fix** these issues in your dataset. [Cleanlab Studio](https://cleanlab.ai/studio/?utm_source=github&utm_medium=readme&utm_campaign=clostostudio) is a no-code platform to find and fix problems in real-world ML datasets. Studio automatically runs optimized versions of the algorithms from this open-source library on top of AutoML models fit to your data, and presents detected issues in a smart data editing interface. Think of it like a data cleaning assistant that helps you quickly improve the quality of your data (via AI/automation + streamlined UX).
 
 ## Join our community
 
 * The best place to learn is [our Slack community](https://cleanlab.ai/slack).
@@ -583,18 +536,19 @@
 * Interested in contributing? See the [contributing guide](CONTRIBUTING.md) and [ideas on useful contributions](https://github.com/cleanlab/cleanlab/wiki#ideas-for-contributing-to-cleanlab). We welcome your help building a standard open-source library for data-centric AI!
 
 * Have code improvements for cleanlab? See the [development guide](DEVELOPMENT.md).
 
 * Have an issue with cleanlab? [Search existing issues](https://github.com/cleanlab/cleanlab/issues?q=is%3Aissue) or [submit a new issue](https://github.com/cleanlab/cleanlab/issues/new).
 
 * Need professional help with cleanlab?
-Join our [\#help Slack channel](https://cleanlab.ai/slack) and message one of our core developers, Jonas Mueller, or schedule a meeting via email: team@cleanlab.ai
+Join our [\#help Slack channel](https://cleanlab.ai/slack) and message us there, or reach out via email: team@cleanlab.ai
 
 ## License
 
-Copyright (c) 2017-2023 Cleanlab Inc.
+Copyright (c) 2017 Cleanlab Inc.
 
 cleanlab is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
 
 cleanlab is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
 
 See [GNU Affero General Public LICENSE](https://github.com/cleanlab/cleanlab/blob/master/LICENSE) for details.
+You can email us to discuss licensing: team@cleanlab.ai
```

### Comparing `cleanlab-2.3.0/cleanlab.egg-info/SOURCES.txt` & `cleanlab-2.3.1/cleanlab.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -27,36 +27,23 @@
 cleanlab/benchmarking/noise_generation.py
 cleanlab/experimental/__init__.py
 cleanlab/experimental/cifar_cnn.py
 cleanlab/experimental/coteaching.py
 cleanlab/experimental/label_issues_batched.py
 cleanlab/experimental/mnist_pytorch.py
 cleanlab/internal/__init__.py
+cleanlab/internal/constants.py
 cleanlab/internal/label_quality_utils.py
 cleanlab/internal/latent_algebra.py
 cleanlab/internal/multiannotator_utils.py
 cleanlab/internal/multilabel_scorer.py
 cleanlab/internal/multilabel_utils.py
 cleanlab/internal/token_classification_utils.py
 cleanlab/internal/util.py
 cleanlab/internal/validation.py
 cleanlab/models/__init__.py
 cleanlab/models/fasttext.py
 cleanlab/models/keras.py
 cleanlab/token_classification/__init__.py
 cleanlab/token_classification/filter.py
 cleanlab/token_classification/rank.py
-cleanlab/token_classification/summary.py
-tests/test_classification.py
-tests/test_dataset.py
-tests/test_filter_count.py
-tests/test_frameworks.py
-tests/test_latent_algebra.py
-tests/test_model_pytorch_cnn.py
-tests/test_multiannotator.py
-tests/test_multilabel_classification.py
-tests/test_noise_generation.py
-tests/test_outlier.py
-tests/test_rank.py
-tests/test_token_classification.py
-tests/test_util.py
-tests/test_validation.py
+cleanlab/token_classification/summary.py
```

### Comparing `cleanlab-2.3.0/setup.py` & `cleanlab-2.3.1/setup.py`

 * *Files identical despite different names*

