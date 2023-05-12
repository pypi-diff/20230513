# Comparing `tmp/PatryksAutoAI-0.4.3.tar.gz` & `tmp/PatryksAutoAI-0.4.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PatryksAutoAI-0.4.3.tar", last modified: Fri May 12 21:11:57 2023, max compression
+gzip compressed data, was "PatryksAutoAI-0.4.4.tar", last modified: Fri May 12 21:57:44 2023, max compression
```

## Comparing `PatryksAutoAI-0.4.3.tar` & `PatryksAutoAI-0.4.4.tar`

### file list

```diff
@@ -1,68 +1,74 @@
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.645256 PatryksAutoAI-0.4.3/
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.637256 PatryksAutoAI-0.4.3/KaggleAutoAI/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      210 2023-05-12 20:28:11.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/__init__.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.637256 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      101 2023-05-12 20:27:46.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/__init__.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.637256 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/algorithms/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)       97 2023-05-12 19:31:03.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/algorithms/__init__.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     1893 2023-05-12 21:11:33.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/algorithms/complexity_level0.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2166 2023-05-12 21:11:42.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/algorithms/complexity_level1.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.637256 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      534 2023-05-12 19:33:34.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/__init__.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      849 2023-05-12 19:35:36.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/cat_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      880 2023-05-12 19:35:47.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/extra_trees.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      910 2023-05-12 19:35:56.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/gradient_boosting_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      882 2023-05-12 19:36:07.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/hist_gradient_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      860 2023-05-12 19:36:17.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/lgb_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      920 2023-05-12 19:36:29.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/logistic_regression_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      890 2023-05-12 19:36:40.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/random_forest_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      844 2023-05-12 19:36:55.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/xgb_automated.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.641256 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      308 2023-05-12 19:57:48.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/__init__.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      840 2023-05-12 19:54:22.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/cat_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      905 2023-05-12 19:55:05.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/gradient_boosting_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      840 2023-05-12 19:55:24.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/lgb_automated.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      840 2023-05-12 19:56:32.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/xgb_automated.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.641256 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)       72 2023-05-10 18:02:22.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/__init__.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      648 2023-04-17 06:33:02.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/metrics.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.641256 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      317 2023-05-10 18:02:39.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/__init__.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     7950 2023-05-12 17:08:00.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/cat.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     6313 2023-05-12 17:08:04.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/extra_trees.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     5279 2023-05-12 17:08:07.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/gradient_boosting.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     5950 2023-05-12 17:08:11.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/hist_gradient.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2205 2023-05-11 13:59:17.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/kneighbours.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     7276 2023-05-12 17:08:16.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/light_lgb.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2301 2023-05-11 13:59:23.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/linear_svc.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     4867 2023-05-12 17:08:23.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/logistic_regression.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     6345 2023-05-12 17:08:27.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/random_forest.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2320 2023-05-11 13:59:44.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/sgd_classifier.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2255 2023-05-11 13:59:40.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/svc.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     5743 2023-05-12 17:08:33.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/xgb.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      920 2023-03-10 12:07:04.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/helper_function.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.641256 PatryksAutoAI-0.4.3/KaggleAutoAI/model_data/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      110 2023-05-10 18:02:54.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/model_data/__init__.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     6075 2023-04-18 06:00:32.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/model_data/model_data.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.641256 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)       89 2023-05-12 20:27:28.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/__init__.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      607 2023-05-09 13:49:56.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/metrics_regression.py
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.641256 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      216 2023-05-12 20:11:18.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/__init__.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     6159 2023-05-12 17:08:40.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/cat.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2632 2023-05-12 17:08:49.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/elastic_net.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     6078 2023-05-12 17:08:53.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/gradient_boosting.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2559 2023-05-11 15:12:20.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/lasso.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     5511 2023-05-12 17:09:00.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/lgb.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2849 2023-05-11 15:11:48.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/sgd.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2633 2023-05-11 15:10:56.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/svr.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     7320 2023-05-12 17:09:07.000000 PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/xgb.py
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      602 2023-05-12 21:11:57.645256 PatryksAutoAI-0.4.3/PKG-INFO
-drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:11:57.641256 PatryksAutoAI-0.4.3/PatryksAutoAI.egg-info/
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      602 2023-05-12 21:11:57.000000 PatryksAutoAI-0.4.3/PatryksAutoAI.egg-info/PKG-INFO
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     2683 2023-05-12 21:11:57.000000 PatryksAutoAI-0.4.3/PatryksAutoAI.egg-info/SOURCES.txt
--rw-rw-r--   0 patryk    (1000) patryk    (1000)        1 2023-05-12 21:11:57.000000 PatryksAutoAI-0.4.3/PatryksAutoAI.egg-info/dependency_links.txt
--rw-rw-r--   0 patryk    (1000) patryk    (1000)      162 2023-05-12 21:11:57.000000 PatryksAutoAI-0.4.3/PatryksAutoAI.egg-info/requires.txt
--rw-rw-r--   0 patryk    (1000) patryk    (1000)       13 2023-05-12 21:11:57.000000 PatryksAutoAI-0.4.3/PatryksAutoAI.egg-info/top_level.txt
--rw-rw-r--   0 patryk    (1000) patryk    (1000)       38 2023-05-12 21:11:57.645256 PatryksAutoAI-0.4.3/setup.cfg
--rw-rw-r--   0 patryk    (1000) patryk    (1000)     1050 2023-05-12 21:11:53.000000 PatryksAutoAI-0.4.3/setup.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.742038 PatryksAutoAI-0.4.4/KaggleAutoAI/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      210 2023-05-12 20:28:11.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/__init__.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.742038 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      101 2023-05-12 20:27:46.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/__init__.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.742038 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/algorithms/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)       97 2023-05-12 19:31:03.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/algorithms/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     1893 2023-05-12 21:11:33.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/algorithms/complexity_level0.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2168 2023-05-12 21:57:20.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/algorithms/complexity_level1.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.742038 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      534 2023-05-12 19:33:34.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      849 2023-05-12 19:35:36.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/cat_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      880 2023-05-12 19:35:47.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/extra_trees.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      910 2023-05-12 19:35:56.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/gradient_boosting_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      882 2023-05-12 19:36:07.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/hist_gradient_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      860 2023-05-12 19:36:17.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/lgb_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      920 2023-05-12 19:36:29.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/logistic_regression_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      890 2023-05-12 19:36:40.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/random_forest_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      844 2023-05-12 19:36:55.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/xgb_automated.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.742038 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      308 2023-05-12 19:57:48.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      840 2023-05-12 21:49:08.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/cat_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      905 2023-05-12 19:55:05.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/gradient_boosting_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      840 2023-05-12 19:55:24.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/lgb_automated.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      840 2023-05-12 19:56:32.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/xgb_automated.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.742038 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)       72 2023-05-10 18:02:22.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      648 2023-04-17 06:33:02.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/metrics.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      317 2023-05-10 18:02:39.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     7950 2023-05-12 17:08:00.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/cat.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     6313 2023-05-12 17:08:04.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/extra_trees.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     5279 2023-05-12 17:08:07.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/gradient_boosting.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     5950 2023-05-12 17:08:11.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/hist_gradient.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2205 2023-05-11 13:59:17.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/kneighbours.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     7276 2023-05-12 17:08:16.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/light_lgb.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2301 2023-05-11 13:59:23.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/linear_svc.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     4867 2023-05-12 17:08:23.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/logistic_regression.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     6345 2023-05-12 17:08:27.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/random_forest.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2320 2023-05-11 13:59:44.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/sgd_classifier.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2255 2023-05-11 13:59:40.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/svc.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     5743 2023-05-12 17:08:33.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/xgb.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      920 2023-03-10 12:07:04.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/helper_function.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/KaggleAutoAI/language_processing/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)       50 2023-05-12 21:44:04.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/language_processing/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      654 2023-05-12 21:36:49.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/language_processing/metrics.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/KaggleAutoAI/language_processing/models/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)       30 2023-05-12 21:43:41.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/language_processing/models/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     1957 2023-05-12 21:44:08.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/language_processing/models/baseline.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/KaggleAutoAI/model_data/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      110 2023-05-10 18:02:54.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/model_data/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     6075 2023-04-18 06:00:32.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/model_data/model_data.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)       89 2023-05-12 20:27:28.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      607 2023-05-09 13:49:56.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/metrics_regression.py
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      216 2023-05-12 20:11:18.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/__init__.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     6213 2023-05-12 21:50:24.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/cat.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2686 2023-05-12 21:51:01.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/elastic_net.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     6132 2023-05-12 21:50:58.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/gradient_boosting.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2613 2023-05-12 21:50:52.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/lasso.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     5569 2023-05-12 21:50:46.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/lgb.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2903 2023-05-12 21:50:40.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/sgd.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2691 2023-05-12 21:50:36.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/svr.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     7374 2023-05-12 21:50:31.000000 PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/xgb.py
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      602 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/PKG-INFO
+drwxrwxr-x   0 patryk    (1000) patryk    (1000)        0 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/PatryksAutoAI.egg-info/
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      602 2023-05-12 21:57:44.000000 PatryksAutoAI-0.4.4/PatryksAutoAI.egg-info/PKG-INFO
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     2876 2023-05-12 21:57:44.000000 PatryksAutoAI-0.4.4/PatryksAutoAI.egg-info/SOURCES.txt
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)        1 2023-05-12 21:57:44.000000 PatryksAutoAI-0.4.4/PatryksAutoAI.egg-info/dependency_links.txt
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)      162 2023-05-12 21:57:44.000000 PatryksAutoAI-0.4.4/PatryksAutoAI.egg-info/requires.txt
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)       13 2023-05-12 21:57:44.000000 PatryksAutoAI-0.4.4/PatryksAutoAI.egg-info/top_level.txt
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)       38 2023-05-12 21:57:44.746038 PatryksAutoAI-0.4.4/setup.cfg
+-rw-rw-r--   0 patryk    (1000) patryk    (1000)     1050 2023-05-12 21:57:27.000000 PatryksAutoAI-0.4.4/setup.py
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/algorithms/complexity_level0.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/algorithms/complexity_level0.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/algorithms/complexity_level1.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/algorithms/complexity_level1.py`

 * *Files 11% similar despite different names*

```diff
@@ -25,15 +25,15 @@
                 standard_columns.append(col)
             else:
                 min_max_columns.append(col)
     print(f"Completed", end=" ")
 
     for col in X.columns:
         if X[col].dtype == "object" and X[col].nunique() < 10:
-            model_data.dummies(col)
+            model_data.dummies([col])
     model_data.min_max_scaler(min_max_columns)
     model_data.standard_scaler(standard_columns)
     
     X = model_data.return_dataframe()
 
     ## Train model in diffrent samples to extract importance of columns
     kfold = KFold(n_splits=5, shuffle=True, random_state=42)
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/__init__.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/__init__.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/cat_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/cat_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/extra_trees.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/extra_trees.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/gradient_boosting_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/gradient_boosting_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/hist_gradient_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/hist_gradient_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/lgb_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/lgb_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/logistic_regression_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/logistic_regression_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/random_forest_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/random_forest_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/classification_automated/xgb_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/classification_automated/xgb_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/cat_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/cat_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/gradient_boosting_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/gradient_boosting_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/lgb_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/lgb_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/automated_ai/regression_automated/xgb_automated.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/automated_ai/regression_automated/xgb_automated.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/metrics.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/metrics.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/cat.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/cat.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/extra_trees.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/extra_trees.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/gradient_boosting.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/gradient_boosting.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/hist_gradient.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/hist_gradient.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/kneighbours.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/kneighbours.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/light_lgb.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/light_lgb.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/linear_svc.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/linear_svc.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/logistic_regression.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/logistic_regression.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/random_forest.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/random_forest.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/sgd_classifier.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/sgd_classifier.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/svc.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/svc.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/classification/models/xgb.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/classification/models/xgb.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/helper_function.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/helper_function.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/model_data/model_data.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/model_data/model_data.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/metrics_regression.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/metrics_regression.py`

 * *Files identical despite different names*

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/cat.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/cat.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,14 +8,17 @@
 
 
 class Cat(Metrics):
     def __init__(self):
         self.model = None
         self.parameters = None
 
+    def put(self, model):
+        self.model = model
+
     def create(self, X, y, params=None):
         if params == None:
             gbm = CatBoostRegressor()
             gbm.fit(X,y)
             self.model = gbm
         else:
             gbm = CatBoostRegressor(**params)
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/elastic_net.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/elastic_net.py`

 * *Files 3% similar despite different names*

```diff
@@ -6,14 +6,17 @@
 
 
 class ElasticNetM(Metrics):
     def __init__(self):
         self.model = None
         self.parameters = None
 
+    def put(self, model):
+        self.model = model
+
     def create(self, X, y, params=None):
         if params == None:
             gbm = ElasticNet()
             gbm.fit(X,y)
             self.model = gbm
         else:
             gbm = ElasticNet(**params)
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/gradient_boosting.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/gradient_boosting.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,14 +8,17 @@
 
 
 class GradientBoosting(Metrics):
     def __init__(self):
         self.model = None
         self.parameters = None
 
+    def put(self, model):
+        self.model = model
+
     def create(self, X, y, params=None):
         if params == None:
           gbm = GradientBoostingRegressor()
           gbm.fit(X,y)
           self.model = gbm
         else:
             gbm = GradientBoostingRegressor(**params)
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/lasso.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/lasso.py`

 * *Files 4% similar despite different names*

```diff
@@ -5,14 +5,17 @@
 import numpy as np
 
 class LassoM(Metrics):
     def __init__(self):
         self.model = None
         self.parameters = None
 
+    def put(self, model):
+        self.model = model
+
     def create(self, X, y, params=None):
         if params == None:
             gbm = Lasso()
             gbm.fit(X,y)
             self.model = gbm
         else:
             gbm = Lasso(**params)
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/lgb.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/lgb.py`

 * *Files 4% similar despite different names*

```diff
@@ -7,14 +7,17 @@
 optuna.logging.disable_default_handler()
 
 
 class LGB(Metrics):
     def __init__(self):
         self.model = None
         self.parameters = None
+    
+    def put(self, model):
+        self.model = model
 
     def create(self, X, y, params=None):
         if params == None:
             gbm = lgb.LGBMRegressor()
             gbm.fit(X,y)
             self.model = gbm
         else:
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/sgd.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/sgd.py`

 * *Files 5% similar despite different names*

```diff
@@ -5,14 +5,17 @@
 import numpy as np
 
 class SGD(Metrics):
     def __init__(self):
         self.model = None
         self.parameters = None
 
+    def put(self, model):
+        self.model = model
+
     def create(self, X, y, params=None):
         if params == None:
             gbm = SGDRegressor()
             gbm.fit(X,y)
             self.model = gbm
         else:
             gbm = SGDRegressor(**params)
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/svr.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/svr.py`

 * *Files 6% similar despite different names*

```diff
@@ -5,14 +5,17 @@
 import numpy as np
 
 
 class SVRM(Metrics):
     def __init__(self):
         self.model = None
         self.parameters = None
+    
+    def put(self, model):
+        self.model = model
 
     def create(self, X, y, params=None):
         if params == None:
             gbm = SVR()
             gbm.fit(X,y)
             self.model = gbm
         else:
```

### Comparing `PatryksAutoAI-0.4.3/KaggleAutoAI/regression/models/xgb.py` & `PatryksAutoAI-0.4.4/KaggleAutoAI/regression/models/xgb.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,14 +8,17 @@
 
 
 class XGB(Metrics):
     def __init__(self):
         self.model = None
         self.parameters = None
 
+    def put(self, model):
+        self.model = model
+
     def create(self, X, y, params=None):
         if params == None:
             gbm = xgb.XGBRegressor()
             gbm.fit(X,y)
             self.model = gbm
         else:
             gbm = xgb.XGBRegressor(**params)
```

### Comparing `PatryksAutoAI-0.4.3/PatryksAutoAI.egg-info/SOURCES.txt` & `PatryksAutoAI-0.4.4/PatryksAutoAI.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -30,14 +30,18 @@
 KaggleAutoAI/classification/models/light_lgb.py
 KaggleAutoAI/classification/models/linear_svc.py
 KaggleAutoAI/classification/models/logistic_regression.py
 KaggleAutoAI/classification/models/random_forest.py
 KaggleAutoAI/classification/models/sgd_classifier.py
 KaggleAutoAI/classification/models/svc.py
 KaggleAutoAI/classification/models/xgb.py
+KaggleAutoAI/language_processing/__init__.py
+KaggleAutoAI/language_processing/metrics.py
+KaggleAutoAI/language_processing/models/__init__.py
+KaggleAutoAI/language_processing/models/baseline.py
 KaggleAutoAI/model_data/__init__.py
 KaggleAutoAI/model_data/model_data.py
 KaggleAutoAI/regression/__init__.py
 KaggleAutoAI/regression/metrics_regression.py
 KaggleAutoAI/regression/models/__init__.py
 KaggleAutoAI/regression/models/cat.py
 KaggleAutoAI/regression/models/elastic_net.py
```

### Comparing `PatryksAutoAI-0.4.3/setup.py` & `PatryksAutoAI-0.4.4/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from setuptools import setup, find_packages
 import codecs
 import os
 
 here = os.path.abspath(os.path.dirname(__file__))
 
-VERSION = '0.4.3'
+VERSION = '0.4.4'
 DESCRIPTION = 'Auto_AI_patryk'
 LONG_DESCRIPTION = 'Package contains helping functions for creating ML models'
 
 # Read the requirements from requirements.txt
 with open('./KaggleAutoAI/requirements.txt') as f:
     requirements = f.read().splitlines()
```

