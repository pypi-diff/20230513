# Comparing `tmp/hyperparameter-tuning-0.2.0.tar.gz` & `tmp/hyperparameter-tuning-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hyperparameter-tuning-0.2.0.tar", last modified: Wed May 10 11:46:56 2023, max compression
+gzip compressed data, was "hyperparameter-tuning-0.2.1.tar", last modified: Sat May 13 09:23:46 2023, max compression
```

## Comparing `hyperparameter-tuning-0.2.0.tar` & `hyperparameter-tuning-0.2.1.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 11:46:56.095421 hyperparameter-tuning-0.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     3343 2023-05-10 11:46:56.095421 hyperparameter-tuning-0.2.0/PKG-INFO
--rwxr-xr-x   0 runner    (1001) docker     (123)     2420 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 11:46:56.091421 hyperparameter-tuning-0.2.0/requirements/
--rwxr-xr-x   0 runner    (1001) docker     (123)       46 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/requirements/main.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/requirements/plotting.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/requirements/test.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-10 11:46:56.095421 hyperparameter-tuning-0.2.0/setup.cfg
--rwxr-xr-x   0 runner    (1001) docker     (123)     3723 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 11:46:56.091421 hyperparameter-tuning-0.2.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 11:46:56.091421 hyperparameter-tuning-0.2.0/src/hpt/
--rwxr-xr-x   0 runner    (1001) docker     (123)      149 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)    12540 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/binarize.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     7083 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/evaluation.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     7252 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/suggest.py
--rw-r--r--   0 runner    (1001) docker     (123)     7270 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/thresholding_evaluation.py
--rwxr-xr-x   0 runner    (1001) docker     (123)    11728 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/tuner.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 11:46:56.091421 hyperparameter-tuning-0.2.0/src/hpt/utils/
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/utils/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (123)      510 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/utils/api.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     1172 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/utils/classpath.py
--rw-r--r--   0 runner    (1001) docker     (123)     1452 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/utils/dict.py
--rw-r--r--   0 runner    (1001) docker     (123)    11702 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/utils/fairness_criteria.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     5473 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/utils/load_yaml.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     3518 2023-05-10 11:46:41.000000 hyperparameter-tuning-0.2.0/src/hpt/utils/trial.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 11:46:56.095421 hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3343 2023-05-10 11:46:56.000000 hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      734 2023-05-10 11:46:56.000000 hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 11:46:56.000000 hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 11:46:55.000000 hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-10 11:46:56.000000 hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-10 11:46:56.000000 hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:23:46.124651 hyperparameter-tuning-0.2.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     3343 2023-05-13 09:23:46.124651 hyperparameter-tuning-0.2.1/PKG-INFO
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2420 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:23:46.120651 hyperparameter-tuning-0.2.1/requirements/
+-rwxr-xr-x   0 runner    (1001) docker     (123)       46 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/requirements/main.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/requirements/plotting.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/requirements/test.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 09:23:46.124651 hyperparameter-tuning-0.2.1/setup.cfg
+-rwxr-xr-x   0 runner    (1001) docker     (123)     3723 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:23:46.120651 hyperparameter-tuning-0.2.1/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:23:46.120651 hyperparameter-tuning-0.2.1/src/hpt/
+-rwxr-xr-x   0 runner    (1001) docker     (123)      149 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12540 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/binarize.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     7122 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/evaluation.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     7252 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/suggest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7270 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/thresholding_evaluation.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)    11728 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/tuner.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:23:46.120651 hyperparameter-tuning-0.2.1/src/hpt/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/utils/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)      510 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/utils/api.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1172 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/utils/classpath.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1452 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/utils/dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11702 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/utils/fairness_criteria.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     5473 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/utils/load_yaml.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     3518 2023-05-13 09:23:35.000000 hyperparameter-tuning-0.2.1/src/hpt/utils/trial.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 09:23:46.124651 hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3343 2023-05-13 09:23:46.000000 hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      734 2023-05-13 09:23:46.000000 hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 09:23:46.000000 hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 09:23:45.000000 hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      129 2023-05-13 09:23:46.000000 hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-13 09:23:46.000000 hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/top_level.txt
```

### Comparing `hyperparameter-tuning-0.2.0/LICENSE` & `hyperparameter-tuning-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/PKG-INFO` & `hyperparameter-tuning-0.2.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hyperparameter-tuning
-Version: 0.2.0
+Version: 0.2.1
 Summary: A minimal framework for running hyperparameter tuning
 Home-page: https://github.com/AndreFCruz/hpt
 Author: AndreFCruz
 License: MIT
 Keywords: ml,optimization,hyperparameter,tuning,fairness
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `hyperparameter-tuning-0.2.0/README.md` & `hyperparameter-tuning-0.2.1/README.md`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/setup.py` & `hyperparameter-tuning-0.2.1/setup.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/binarize.py` & `hyperparameter-tuning-0.2.1/src/hpt/binarize.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/evaluation.py` & `hyperparameter-tuning-0.2.1/src/hpt/evaluation.py`

 * *Files 5% similar despite different names*

```diff
@@ -208,15 +208,15 @@
 
     # Compute global performance metrics
     results = evaluate_performance(y_true, y_pred_binary)
 
     # Compute loss metrics
     results.update({
         "squared_loss": mean_squared_error(y_true, y_pred_scores),
-        "log_loss": log_loss(y_true, y_pred_scores),
+        "log_loss": log_loss(y_true, y_pred_scores, eps=np.finfo(y_pred_scores.dtype).eps),
     })
 
     # (Optionally) Compute fairness metrics
     if sensitive_attribute is not None:
         results.update(evaluate_fairness(
             y_true, y_pred_binary, sensitive_attribute,
             return_groupwise_metrics=return_groupwise_metrics,
```

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/suggest.py` & `hyperparameter-tuning-0.2.1/src/hpt/suggest.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/thresholding_evaluation.py` & `hyperparameter-tuning-0.2.1/src/hpt/thresholding_evaluation.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/tuner.py` & `hyperparameter-tuning-0.2.1/src/hpt/tuner.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/utils/classpath.py` & `hyperparameter-tuning-0.2.1/src/hpt/utils/classpath.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/utils/dict.py` & `hyperparameter-tuning-0.2.1/src/hpt/utils/dict.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/utils/fairness_criteria.py` & `hyperparameter-tuning-0.2.1/src/hpt/utils/fairness_criteria.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/utils/load_yaml.py` & `hyperparameter-tuning-0.2.1/src/hpt/utils/load_yaml.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hpt/utils/trial.py` & `hyperparameter-tuning-0.2.1/src/hpt/utils/trial.py`

 * *Files identical despite different names*

### Comparing `hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/PKG-INFO` & `hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hyperparameter-tuning
-Version: 0.2.0
+Version: 0.2.1
 Summary: A minimal framework for running hyperparameter tuning
 Home-page: https://github.com/AndreFCruz/hpt
 Author: AndreFCruz
 License: MIT
 Keywords: ml,optimization,hyperparameter,tuning,fairness
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `hyperparameter-tuning-0.2.0/src/hyperparameter_tuning.egg-info/SOURCES.txt` & `hyperparameter-tuning-0.2.1/src/hyperparameter_tuning.egg-info/SOURCES.txt`

 * *Files identical despite different names*

