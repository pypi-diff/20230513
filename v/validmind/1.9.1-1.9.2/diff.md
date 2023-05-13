# Comparing `tmp/validmind-1.9.1.tar.gz` & `tmp/validmind-1.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "validmind-1.9.1.tar", max compression
+gzip compressed data, was "validmind-1.9.2.tar", max compression
```

## Comparing `validmind-1.9.1.tar` & `validmind-1.9.2.tar`

### file list

```diff
@@ -1,62 +1,62 @@
--rw-r--r--   0        0        0     1295 2023-05-12 23:35:53.257568 validmind-1.9.1/pyproject.toml
--rw-r--r--   0        0        0     1443 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/__init__.py
--rw-r--r--   0        0        0    11353 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/api_client.py
--rw-r--r--   0        0        0     9190 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/client.py
--rw-r--r--   0        0        0      590 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/data_validation/__init__.py
--rw-r--r--   0        0        0    34771 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/data_validation/metrics.py
--rw-r--r--   0        0        0    24265 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/data_validation/threshold_tests.py
--rw-r--r--   0        0        0        0 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/datasets/__init__.py
--rw-r--r--   0        0        0     1539 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/datasets/classification/__init__.py
--rw-r--r--   0        0        0     1330 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/datasets/classification/customer_churn.py
--rw-r--r--   0        0        0   545707 2023-05-12 23:35:53.261569 validmind-1.9.1/validmind/datasets/classification/datasets/bank_customer_churn.csv
--rw-r--r--   0        0        0  2897191 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/classification/datasets/taiwan_credit.csv
--rw-r--r--   0        0        0     1280 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/classification/taiwan_credit.py
--rw-r--r--   0        0        0     1645 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/__init__.py
--rw-r--r--   0        0        0   107835 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates.csv
--rw-r--r--   0        0        0     2634 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv
--rw-r--r--   0        0        0     2634 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv
--rw-r--r--   0        0        0     2736 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv
--rw-r--r--   0        0        0     3355 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv
--rw-r--r--   0        0        0     3866 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv
--rw-r--r--   0        0        0    11624 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/lending_club_loan_rates.csv
--rw-r--r--   0        0        0     4378 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/fred.py
--rw-r--r--   0        0        0     2346 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/lending_club.py
--rw-r--r--   0        0        0    40067 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl
--rw-r--r--   0        0        0    48314 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl
--rw-r--r--   0        0        0    40063 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl
--rw-r--r--   0        0        0    48292 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl
--rw-r--r--   0        0        0    60343 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl
--rw-r--r--   0        0        0    10529 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_utils.py
--rw-r--r--   0        0        0     1290 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/__init__.py
--rw-r--r--   0        0        0     6712 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/model_metadata.py
--rw-r--r--   0        0        0        0 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/sklearn/__init__.py
--rw-r--r--   0        0        0    13048 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/sklearn/metrics.py
--rw-r--r--   0        0        0    31402 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/sklearn/threshold_tests.py
--rw-r--r--   0        0        0        0 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/statsmodels/__init__.py
--rw-r--r--   0        0        0    26596 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/statsmodels/metrics.py
--rw-r--r--   0        0        0     1317 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/statsmodels/threshold_tests.py
--rw-r--r--   0        0        0     1657 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/utils.py
--rw-r--r--   0        0        0     5182 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/__init__.py
--rw-r--r--   0        0        0     2016 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/binary_classifier.py
--rw-r--r--   0        0        0     2836 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/statsmodels_timeseries.py
--rw-r--r--   0        0        0     1604 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/tabular_datasets.py
--rw-r--r--   0        0        0     6821 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/time_series.py
--rw-r--r--   0        0        0     1894 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_suites/__init__.py
--rw-r--r--   0        0        0     1344 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_suites/test_suites.py
--rw-r--r--   0        0        0     6465 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/utils.py
--rw-r--r--   0        0        0     1116 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/__init__.py
--rw-r--r--   0        0        0    10425 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/dataset.py
--rw-r--r--   0        0        0     8287 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/dataset_utils.py
--rw-r--r--   0        0        0      592 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/figure.py
--rw-r--r--   0        0        0     3746 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/metric.py
--rw-r--r--   0        0        0     1757 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/metric_result.py
--rw-r--r--   0        0        0     6530 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/model.py
--rw-r--r--   0        0        0     3721 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/plot_utils.py
--rw-r--r--   0        0        0     1518 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/result_summary.py
--rw-r--r--   0        0        0     2501 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_context.py
--rw-r--r--   0        0        0    11803 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_plan.py
--rw-r--r--   0        0        0    18529 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_plan_result.py
--rw-r--r--   0        0        0     1698 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_result.py
--rw-r--r--   0        0        0     5019 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_suite.py
--rw-r--r--   0        0        0     3620 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/threshold_test.py
--rw-r--r--   0        0        0     1385 1970-01-01 00:00:00.000000 validmind-1.9.1/PKG-INFO
+-rw-r--r--   0        0        0     1295 2023-05-13 08:42:30.626940 validmind-1.9.2/pyproject.toml
+-rw-r--r--   0        0        0     1443 2023-05-13 08:42:30.626940 validmind-1.9.2/validmind/__init__.py
+-rw-r--r--   0        0        0    11353 2023-05-13 08:42:30.626940 validmind-1.9.2/validmind/api_client.py
+-rw-r--r--   0        0        0     9190 2023-05-13 08:42:30.626940 validmind-1.9.2/validmind/client.py
+-rw-r--r--   0        0        0      590 2023-05-13 08:42:30.626940 validmind-1.9.2/validmind/data_validation/__init__.py
+-rw-r--r--   0        0        0    36506 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/data_validation/metrics.py
+-rw-r--r--   0        0        0    24265 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/data_validation/threshold_tests.py
+-rw-r--r--   0        0        0        0 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/datasets/__init__.py
+-rw-r--r--   0        0        0     1539 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/datasets/classification/__init__.py
+-rw-r--r--   0        0        0     1330 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/datasets/classification/customer_churn.py
+-rw-r--r--   0        0        0   545707 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/datasets/classification/datasets/bank_customer_churn.csv
+-rw-r--r--   0        0        0  2897191 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/classification/datasets/taiwan_credit.csv
+-rw-r--r--   0        0        0     1280 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/classification/taiwan_credit.py
+-rw-r--r--   0        0        0     1416 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/__init__.py
+-rw-r--r--   0        0        0   107835 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates.csv
+-rw-r--r--   0        0        0     2634 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv
+-rw-r--r--   0        0        0     2634 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv
+-rw-r--r--   0        0        0     2736 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv
+-rw-r--r--   0        0        0     3355 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv
+-rw-r--r--   0        0        0     3866 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv
+-rw-r--r--   0        0        0    11624 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/lending_club_loan_rates.csv
+-rw-r--r--   0        0        0     4378 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/fred.py
+-rw-r--r--   0        0        0     2346 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/lending_club.py
+-rw-r--r--   0        0        0    40067 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl
+-rw-r--r--   0        0        0    48314 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl
+-rw-r--r--   0        0        0    40063 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl
+-rw-r--r--   0        0        0    48292 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl
+-rw-r--r--   0        0        0    60343 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl
+-rw-r--r--   0        0        0    10529 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_utils.py
+-rw-r--r--   0        0        0     1290 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/__init__.py
+-rw-r--r--   0        0        0     6712 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/model_metadata.py
+-rw-r--r--   0        0        0        0 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/sklearn/__init__.py
+-rw-r--r--   0        0        0    13048 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/sklearn/metrics.py
+-rw-r--r--   0        0        0    31402 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/sklearn/threshold_tests.py
+-rw-r--r--   0        0        0        0 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/statsmodels/__init__.py
+-rw-r--r--   0        0        0    26596 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/statsmodels/metrics.py
+-rw-r--r--   0        0        0     1317 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/statsmodels/threshold_tests.py
+-rw-r--r--   0        0        0     1657 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/utils.py
+-rw-r--r--   0        0        0     5182 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/__init__.py
+-rw-r--r--   0        0        0     2016 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/binary_classifier.py
+-rw-r--r--   0        0        0     2836 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/statsmodels_timeseries.py
+-rw-r--r--   0        0        0     1604 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/tabular_datasets.py
+-rw-r--r--   0        0        0     6821 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/time_series.py
+-rw-r--r--   0        0        0     1894 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_suites/__init__.py
+-rw-r--r--   0        0        0     1415 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_suites/test_suites.py
+-rw-r--r--   0        0        0     6465 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/utils.py
+-rw-r--r--   0        0        0     1116 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/__init__.py
+-rw-r--r--   0        0        0    10425 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/dataset.py
+-rw-r--r--   0        0        0     8287 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/dataset_utils.py
+-rw-r--r--   0        0        0      592 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/figure.py
+-rw-r--r--   0        0        0     3746 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/metric.py
+-rw-r--r--   0        0        0     1757 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/metric_result.py
+-rw-r--r--   0        0        0     6530 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/model.py
+-rw-r--r--   0        0        0     3721 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/plot_utils.py
+-rw-r--r--   0        0        0     1518 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/result_summary.py
+-rw-r--r--   0        0        0     2501 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_context.py
+-rw-r--r--   0        0        0    11803 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_plan.py
+-rw-r--r--   0        0        0    18529 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_plan_result.py
+-rw-r--r--   0        0        0     1698 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_result.py
+-rw-r--r--   0        0        0     5019 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_suite.py
+-rw-r--r--   0        0        0     3620 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/threshold_test.py
+-rw-r--r--   0        0        0     1385 1970-01-01 00:00:00.000000 validmind-1.9.2/PKG-INFO
```

### Comparing `validmind-1.9.1/pyproject.toml` & `validmind-1.9.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 # include = [
 #   "validmind/**/*.c",
 #   "validmind/**/*.pyx",
 #   "validmind/**/*.pyd",
 #   "validmind/**/*.so",
 # ]
 name = "validmind"
-version = "1.9.1"
+version = "1.9.2"
 
 [tool.poetry.dependencies]
 arch = "^5.4.0"
 click = "^8.0.4"
 dython = "^0.7.1"
 ipython = "^8.11.0"
 myst-parser = "^1.0.0"
```

### Comparing `validmind-1.9.1/validmind/__init__.py` & `validmind-1.9.2/validmind/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/api_client.py` & `validmind-1.9.2/validmind/api_client.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/client.py` & `validmind-1.9.2/validmind/client.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/data_validation/__init__.py` & `validmind-1.9.2/validmind/data_validation/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/data_validation/metrics.py` & `validmind-1.9.2/validmind/data_validation/metrics.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 """
 Metrics functions for any Pandas-compatible datasets
 """
 
 from dataclasses import dataclass
 from typing import ClassVar
+import warnings
 
 import pandas as pd
 import numpy as np
 from scipy import stats
 import seaborn as sns
 import matplotlib.pyplot as plt
 import matplotlib.dates as mdates
@@ -279,24 +280,30 @@
     Generates a visual analysis of time series data by plotting the
     raw time series. The input dataset can have multiple time series
     if necessary. In this case we produce a separate plot for each time series.
     """
 
     name = "time_series_line_plot"
     required_context = ["dataset"]
+    default_params = {"columns": None}
 
     def run(self):
         if "columns" not in self.params:
             raise ValueError("Time series columns must be provided in params")
 
         # Check if index is datetime
         if not pd.api.types.is_datetime64_any_dtype(self.dataset.df.index):
             raise ValueError("Index must be a datetime type")
 
-        columns = self.params["columns"]
+        # If no columns are specified in the config, we plot all columns
+        if self.params["columns"] is None:
+            columns = list(self.dataset.df.columns)
+        else:
+            columns = self.params["columns"]
+
         df = self.dataset.df
 
         if not set(columns).issubset(set(df.columns)):
             raise ValueError("Provided 'columns' must exist in the dataset")
 
         figures = []
         for col in columns:
@@ -327,24 +334,30 @@
     Generates a visual analysis of time series data by plotting the
     histogram. The input dataset can have multiple time series if
     necessary. In this case we produce a separate plot for each time series.
     """
 
     name = "time_series_histogram"
     required_context = ["dataset"]
+    default_params = {"columns": None}
 
     def run(self):
         if "columns" not in self.params:
             raise ValueError("Time series columns must be provided in params")
 
         # Check if index is datetime
         if not pd.api.types.is_datetime64_any_dtype(self.dataset.df.index):
             raise ValueError("Index must be a datetime type")
 
-        columns = self.params["columns"]
+        # If no columns are specified in the config, we plot all columns
+        if self.params["columns"] is None:
+            columns = list(self.dataset.df.columns)
+        else:
+            columns = self.params["columns"]
+
         df = self.dataset.df
 
         if not set(columns).issubset(set(df.columns)):
             raise ValueError("Provided 'columns' must exist in the dataset")
 
         figures = []
         for col in columns:
@@ -368,20 +381,26 @@
     """
     Generates a visual analysis of data by plotting a scatter plot matrix for all columns
     in the dataset. The input dataset can have multiple columns (features) if necessary.
     """
 
     name = "scatter_plot"
     required_context = ["dataset"]
+    default_params = {"columns": None}
 
     def run(self):
         if "columns" not in self.params:
             raise ValueError("Columns must be provided in params")
 
-        columns = self.params["columns"]
+        # If no columns are specified in the config, we plot all columns
+        if self.params["columns"] is None:
+            columns = list(self.dataset.df.columns)
+        else:
+            columns = self.params["columns"]
+
         df = self.dataset.df[columns]
 
         if not set(columns).issubset(set(df.columns)):
             raise ValueError("Provided 'columns' must exist in the dataset")
 
         sns.pairplot(data=df, diag_kind="kde")
 
@@ -443,31 +462,27 @@
         )
         plt.xlabel("Lags")
         plt.ylabel("Independent Variables")
 
         return plt.gcf()
 
     def run(self):
-        if "target_col" not in self.params or "independent_vars" not in self.params:
-            raise ValueError(
-                "Both 'target_col' and 'independent_vars' must be provided in params"
-            )
+        target_col = [self.dataset.y.name]
+        independent_vars = list(self.dataset.x.columns)
+
+        num_lags = self.params.get("num_lags", 10)
 
-        target_col = self.params["target_col"]
         if isinstance(target_col, list) and len(target_col) == 1:
             target_col = target_col[0]
 
         if not isinstance(target_col, str):
             raise ValueError(
                 "The 'target_col' must be a single string or a list containing a single string"
             )
 
-        independent_vars = self.params["independent_vars"]
-        num_lags = self.params.get("num_lags", 10)
-
         df = self.dataset.df
 
         correlations = self._compute_correlations(
             df, target_col, independent_vars, num_lags
         )
         fig = self._plot_heatmap(correlations, independent_vars, num_lags)
 
@@ -483,14 +498,15 @@
 class AutoAR(Metric):
     """
     Automatically detects the AR order of a time series using both BIC and AIC.
     """
 
     name = "auto_ar"
     required_context = ["dataset"]
+    default_params = {"max_ar_order": 3}
 
     def run(self):
         if "max_ar_order" not in self.params:
             raise ValueError("max_ar_order must be provided in params")
 
         max_ar_order = self.params["max_ar_order"]
 
@@ -535,14 +551,15 @@
 class AutoMA(Metric):
     """
     Automatically detects the MA order of a time series using both BIC and AIC.
     """
 
     name = "auto_ma"
     required_context = ["dataset"]
+    default_params = {"max_ma_order": 3}
 
     def run(self):
         if "max_ma_order" not in self.params:
             raise ValueError("max_ma_order must be provided in params")
 
         max_ma_order = self.params["max_ma_order"]
 
@@ -645,72 +662,87 @@
         # Parse input parameters
         if "seasonal_model" not in self.params:
             raise ValueError("seasonal_model must be provided in params")
         seasonal_model = self.params["seasonal_model"]
 
         df = self.dataset.df
 
-        # Drop rows with missing values
-        df = df.dropna()
-
         results = {}
         figures = []
 
         for col in df.columns:
-            sd = seasonal_decompose(df[col], model=seasonal_model)
-            self.store_seasonal_decompose(col, sd)
+            series = df[col].dropna()
 
-            results[col] = self.serialize_seasonal_decompose(sd)
+            # Check for non-finite values and handle them
+            if not series[np.isfinite(series)].empty:
+                inferred_freq = pd.infer_freq(series.index)
+
+                if inferred_freq is not None:
+                    print(f"Frequency of {col}: {inferred_freq}")
+
+                    # Only take finite values to seasonal_decompose
+                    sd = seasonal_decompose(
+                        series[np.isfinite(series)], model=seasonal_model
+                    )
+                    self.store_seasonal_decompose(col, sd)
 
-            # Create subplots
-            fig, axes = plt.subplots(nrows=4, ncols=2)
-            fig.subplots_adjust(hspace=1)
-            fig.suptitle(
-                f"Seasonal Decomposition and Residual Diagnostics for {col}",
-                fontsize=24,
-            )
+                    results[col] = self.serialize_seasonal_decompose(sd)
 
-            # Original seasonal decomposition plots
-            axes[0, 0].set_title("Observed")
-            sd.observed.plot(ax=axes[0, 0])
+                    # Create subplots
+                    fig, axes = plt.subplots(nrows=4, ncols=2)
+                    fig.subplots_adjust(hspace=1)
+                    fig.suptitle(
+                        f"Seasonal Decomposition and Residual Diagnostics for {col}",
+                        fontsize=24,
+                    )
 
-            axes[0, 1].set_title("Trend")
-            sd.trend.plot(ax=axes[0, 1])
+                    # Original seasonal decomposition plots
+                    axes[0, 0].set_title("Observed")
+                    sd.observed.plot(ax=axes[0, 0])
 
-            axes[1, 0].set_title("Seasonal")
-            sd.seasonal.plot(ax=axes[1, 0])
+                    axes[0, 1].set_title("Trend")
+                    sd.trend.plot(ax=axes[0, 1])
 
-            axes[1, 1].set_title("Residuals")
-            sd.resid.plot(ax=axes[1, 1])
-            axes[1, 1].set_xlabel("Date")
+                    axes[1, 0].set_title("Seasonal")
+                    sd.seasonal.plot(ax=axes[1, 0])
 
-            # Residual diagnostics plots
-            residuals = sd.resid.dropna()
+                    axes[1, 1].set_title("Residuals")
+                    sd.resid.plot(ax=axes[1, 1])
+                    axes[1, 1].set_xlabel("Date")
 
-            # Histogram with KDE
-            sns.histplot(residuals, kde=True, ax=axes[2, 0])
-            axes[2, 0].set_title("Histogram and KDE of Residuals")
+                    # Residual diagnostics plots
+                    residuals = sd.resid.dropna()
 
-            # Normal Q-Q plot
-            stats.probplot(residuals, plot=axes[2, 1])
-            axes[2, 1].set_title("Normal Q-Q Plot of Residuals")
+                    # Histogram with KDE
+                    sns.histplot(residuals, kde=True, ax=axes[2, 0])
+                    axes[2, 0].set_title("Histogram and KDE of Residuals")
 
-            # ACF plot
-            plot_acf(residuals, ax=axes[3, 0], title="ACF of Residuals")
+                    # Normal Q-Q plot
+                    stats.probplot(residuals, plot=axes[2, 1])
+                    axes[2, 1].set_title("Normal Q-Q Plot of Residuals")
 
-            # PACF plot
-            plot_pacf(residuals, ax=axes[3, 1], title="PACF of Residuals")
+                    # ACF plot
+                    plot_acf(residuals, ax=axes[3, 0], title="ACF of Residuals")
 
-            # Adjust the layout
-            plt.tight_layout()
+                    # PACF plot
+                    plot_pacf(residuals, ax=axes[3, 1], title="PACF of Residuals")
 
-            # Do this if you want to prevent the figure from being displayed
-            plt.close("all")
+                    # Adjust the layout
+                    plt.tight_layout()
 
-            figures.append(Figure(key=f"{self.key}:{col}", figure=fig, metadata={}))
+                    # Do this if you want to prevent the figure from being displayed
+                    plt.close("all")
+
+                    figures.append(
+                        Figure(key=f"{self.key}:{col}", figure=fig, metadata={})
+                    )
+                else:
+                    warnings.warn(
+                        f"No frequency could be inferred for variable '{col}'. Skipping seasonal decomposition and plots for this variable."
+                    )
 
         return self.cache_results(results, figures=figures)
 
 
 class AutoSeasonality(Metric):
     """
     Automatically detects the optimal seasonal order for a time series dataset
@@ -775,24 +807,30 @@
 class ACFandPACFPlot(Metric):
     """
     Plots ACF and PACF for a given time series dataset.
     """
 
     name = "acf_pacf_plot"
     required_context = ["dataset"]
+    default_params = {"columns": None}
 
     def run(self):
         if "columns" not in self.params:
             raise ValueError("Time series columns must be provided in params")
 
         # Check if index is datetime
         if not pd.api.types.is_datetime64_any_dtype(self.dataset.df.index):
             raise ValueError("Index must be a datetime type")
 
-        columns = self.params["columns"]
+        # If no columns are specified in the config, we plot all columns
+        if self.params["columns"] is None:
+            columns = list(self.dataset.df.columns)
+        else:
+            columns = self.params["columns"]
+
         df = self.dataset.df.dropna()
 
         if not set(columns).issubset(set(df.columns)):
             raise ValueError("Provided 'columns' must exist in the dataset")
 
         figures = []
```

### Comparing `validmind-1.9.1/validmind/data_validation/threshold_tests.py` & `validmind-1.9.2/validmind/data_validation/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/classification/__init__.py` & `validmind-1.9.2/validmind/datasets/classification/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/classification/customer_churn.py` & `validmind-1.9.2/validmind/datasets/classification/customer_churn.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/classification/datasets/bank_customer_churn.csv` & `validmind-1.9.2/validmind/datasets/classification/datasets/bank_customer_churn.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/classification/datasets/taiwan_credit.csv` & `validmind-1.9.2/validmind/datasets/classification/datasets/taiwan_credit.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/classification/taiwan_credit.py` & `validmind-1.9.2/validmind/datasets/classification/taiwan_credit.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/__init__.py` & `validmind-1.9.2/validmind/datasets/regression/__init__.py`

 * *Files 10% similar despite different names*

```diff
@@ -12,22 +12,15 @@
     :return: DataFrame with two columns: 'Variable' and 'Frequency'
     """
     frequencies = []
     for column in df.columns:
         series = df[column].dropna()
         if not series.empty:
             freq = pd.infer_freq(series.index)
-            if freq == "MS" or freq == "M":
-                label = "Monthly"
-            elif freq == "Q":
-                label = "Quarterly"
-            elif freq == "A":
-                label = "Yearly"
-            else:
-                label = freq
+            label = freq
         else:
             label = None
 
         frequencies.append({"Variable": column, "Frequency": label})
 
     freq_df = pd.DataFrame(frequencies)
```

### Comparing `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates.csv` & `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv` & `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv` & `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv` & `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv` & `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv` & `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/datasets/lending_club_loan_rates.csv` & `validmind-1.9.2/validmind/datasets/regression/datasets/lending_club_loan_rates.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/fred.py` & `validmind-1.9.2/validmind/datasets/regression/fred.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/lending_club.py` & `validmind-1.9.2/validmind/datasets/regression/lending_club.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl` & `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl` & `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl` & `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl` & `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl` & `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/model_utils.py` & `validmind-1.9.2/validmind/model_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/model_validation/__init__.py` & `validmind-1.9.2/validmind/model_validation/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/model_validation/model_metadata.py` & `validmind-1.9.2/validmind/model_validation/model_metadata.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/model_validation/sklearn/metrics.py` & `validmind-1.9.2/validmind/model_validation/sklearn/metrics.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/model_validation/sklearn/threshold_tests.py` & `validmind-1.9.2/validmind/model_validation/sklearn/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/model_validation/statsmodels/metrics.py` & `validmind-1.9.2/validmind/model_validation/statsmodels/metrics.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/model_validation/statsmodels/threshold_tests.py` & `validmind-1.9.2/validmind/model_validation/statsmodels/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/model_validation/utils.py` & `validmind-1.9.2/validmind/model_validation/utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/test_plans/__init__.py` & `validmind-1.9.2/validmind/test_plans/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/test_plans/binary_classifier.py` & `validmind-1.9.2/validmind/test_plans/binary_classifier.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/test_plans/statsmodels_timeseries.py` & `validmind-1.9.2/validmind/test_plans/statsmodels_timeseries.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/test_plans/tabular_datasets.py` & `validmind-1.9.2/validmind/test_plans/tabular_datasets.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/test_plans/time_series.py` & `validmind-1.9.2/validmind/test_plans/time_series.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/test_suites/__init__.py` & `validmind-1.9.2/validmind/test_suites/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/test_suites/test_suites.py` & `validmind-1.9.2/validmind/test_suites/test_suites.py`

 * *Files 4% similar despite different names*

```diff
@@ -51,13 +51,16 @@
     ]
 
 
 class TimeSeriesDataset(TestSuite):
     """
     Test suite for time series datasets.
     """
+
     name = "time_series_dataset"
     required_context = ["dataset"]
 
     test_plans = [
         "time_series_data_quality",
+        "time_series_univariate",
+        "time_series_multivariate",
     ]
```

### Comparing `validmind-1.9.1/validmind/utils.py` & `validmind-1.9.2/validmind/utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/__init__.py` & `validmind-1.9.2/validmind/vm_models/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/dataset.py` & `validmind-1.9.2/validmind/vm_models/dataset.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/dataset_utils.py` & `validmind-1.9.2/validmind/vm_models/dataset_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/figure.py` & `validmind-1.9.2/validmind/vm_models/figure.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/metric.py` & `validmind-1.9.2/validmind/vm_models/metric.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/metric_result.py` & `validmind-1.9.2/validmind/vm_models/metric_result.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/model.py` & `validmind-1.9.2/validmind/vm_models/model.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/plot_utils.py` & `validmind-1.9.2/validmind/vm_models/plot_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/result_summary.py` & `validmind-1.9.2/validmind/vm_models/result_summary.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/test_context.py` & `validmind-1.9.2/validmind/vm_models/test_context.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/test_plan.py` & `validmind-1.9.2/validmind/vm_models/test_plan.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/test_plan_result.py` & `validmind-1.9.2/validmind/vm_models/test_plan_result.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/test_result.py` & `validmind-1.9.2/validmind/vm_models/test_result.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/test_suite.py` & `validmind-1.9.2/validmind/vm_models/test_suite.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/validmind/vm_models/threshold_test.py` & `validmind-1.9.2/validmind/vm_models/threshold_test.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.1/PKG-INFO` & `validmind-1.9.2/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: validmind
-Version: 1.9.1
+Version: 1.9.2
 Summary: ValidMind Developer Framework
 Author: Andres Rodriguez
 Author-email: andres@validmind.ai
 Requires-Python: >=3.8,<3.11
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

