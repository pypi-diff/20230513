# Comparing `tmp/validmind-1.9.0.tar.gz` & `tmp/validmind-1.9.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "validmind-1.9.0.tar", max compression
+gzip compressed data, was "validmind-1.9.1.tar", max compression
```

## Comparing `validmind-1.9.0.tar` & `validmind-1.9.1.tar`

### file list

```diff
@@ -1,62 +1,62 @@
--rw-r--r--   0        0        0     1295 2023-05-12 07:24:11.424716 validmind-1.9.0/pyproject.toml
--rw-r--r--   0        0        0     1443 2023-05-12 07:24:11.424716 validmind-1.9.0/validmind/__init__.py
--rw-r--r--   0        0        0    11353 2023-05-12 07:24:11.424716 validmind-1.9.0/validmind/api_client.py
--rw-r--r--   0        0        0     9190 2023-05-12 07:24:11.424716 validmind-1.9.0/validmind/client.py
--rw-r--r--   0        0        0      590 2023-05-12 07:24:11.424716 validmind-1.9.0/validmind/data_validation/__init__.py
--rw-r--r--   0        0        0    35109 2023-05-12 07:24:11.428716 validmind-1.9.0/validmind/data_validation/metrics.py
--rw-r--r--   0        0        0    24265 2023-05-12 07:24:11.428716 validmind-1.9.0/validmind/data_validation/threshold_tests.py
--rw-r--r--   0        0        0        0 2023-05-12 07:24:11.428716 validmind-1.9.0/validmind/datasets/__init__.py
--rw-r--r--   0        0        0     1539 2023-05-12 07:24:11.428716 validmind-1.9.0/validmind/datasets/classification/__init__.py
--rw-r--r--   0        0        0     1330 2023-05-12 07:24:11.428716 validmind-1.9.0/validmind/datasets/classification/customer_churn.py
--rw-r--r--   0        0        0   545707 2023-05-12 07:24:11.428716 validmind-1.9.0/validmind/datasets/classification/datasets/bank_customer_churn.csv
--rw-r--r--   0        0        0  2897191 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/classification/datasets/taiwan_credit.csv
--rw-r--r--   0        0        0     1280 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/classification/taiwan_credit.py
--rw-r--r--   0        0        0     1645 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/__init__.py
--rw-r--r--   0        0        0   107835 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates.csv
--rw-r--r--   0        0        0     2634 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv
--rw-r--r--   0        0        0     2634 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv
--rw-r--r--   0        0        0     2736 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv
--rw-r--r--   0        0        0     3355 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv
--rw-r--r--   0        0        0     3866 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv
--rw-r--r--   0        0        0    11624 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/datasets/lending_club_loan_rates.csv
--rw-r--r--   0        0        0     4378 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/fred.py
--rw-r--r--   0        0        0     2346 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/lending_club.py
--rw-r--r--   0        0        0    40067 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl
--rw-r--r--   0        0        0    48314 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl
--rw-r--r--   0        0        0    40063 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl
--rw-r--r--   0        0        0    48292 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl
--rw-r--r--   0        0        0    60343 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl
--rw-r--r--   0        0        0    10529 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_utils.py
--rw-r--r--   0        0        0     1290 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/__init__.py
--rw-r--r--   0        0        0     6749 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/model_metadata.py
--rw-r--r--   0        0        0        0 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/sklearn/__init__.py
--rw-r--r--   0        0        0    13446 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/sklearn/metrics.py
--rw-r--r--   0        0        0    31402 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/sklearn/threshold_tests.py
--rw-r--r--   0        0        0        0 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/statsmodels/__init__.py
--rw-r--r--   0        0        0    28009 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/statsmodels/metrics.py
--rw-r--r--   0        0        0     1317 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/statsmodels/threshold_tests.py
--rw-r--r--   0        0        0     1657 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/model_validation/utils.py
--rw-r--r--   0        0        0     5251 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/test_plans/__init__.py
--rw-r--r--   0        0        0     1985 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/test_plans/binary_classifier.py
--rw-r--r--   0        0        0     2836 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/test_plans/statsmodels_timeseries.py
--rw-r--r--   0        0        0     1822 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/test_plans/tabular_datasets.py
--rw-r--r--   0        0        0     6821 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/test_plans/time_series.py
--rw-r--r--   0        0        0     1825 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/test_suites/__init__.py
--rw-r--r--   0        0        0     1119 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/test_suites/test_suites.py
--rw-r--r--   0        0        0     6465 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/utils.py
--rw-r--r--   0        0        0     1116 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/__init__.py
--rw-r--r--   0        0        0    10425 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/dataset.py
--rw-r--r--   0        0        0     8287 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/dataset_utils.py
--rw-r--r--   0        0        0      592 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/figure.py
--rw-r--r--   0        0        0     3674 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/metric.py
--rw-r--r--   0        0        0     1757 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/metric_result.py
--rw-r--r--   0        0        0     6530 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/model.py
--rw-r--r--   0        0        0     3721 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/plot_utils.py
--rw-r--r--   0        0        0     1518 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/result_summary.py
--rw-r--r--   0        0        0     2501 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/test_context.py
--rw-r--r--   0        0        0    11386 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/test_plan.py
--rw-r--r--   0        0        0    19100 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/test_plan_result.py
--rw-r--r--   0        0        0     1698 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/test_result.py
--rw-r--r--   0        0        0     4958 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/test_suite.py
--rw-r--r--   0        0        0     3621 2023-05-12 07:24:11.448716 validmind-1.9.0/validmind/vm_models/threshold_test.py
--rw-r--r--   0        0        0     1385 1970-01-01 00:00:00.000000 validmind-1.9.0/PKG-INFO
+-rw-r--r--   0        0        0     1295 2023-05-12 23:35:53.257568 validmind-1.9.1/pyproject.toml
+-rw-r--r--   0        0        0     1443 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/__init__.py
+-rw-r--r--   0        0        0    11353 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/api_client.py
+-rw-r--r--   0        0        0     9190 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/client.py
+-rw-r--r--   0        0        0      590 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/data_validation/__init__.py
+-rw-r--r--   0        0        0    34771 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/data_validation/metrics.py
+-rw-r--r--   0        0        0    24265 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/data_validation/threshold_tests.py
+-rw-r--r--   0        0        0        0 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/datasets/__init__.py
+-rw-r--r--   0        0        0     1539 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/datasets/classification/__init__.py
+-rw-r--r--   0        0        0     1330 2023-05-12 23:35:53.257568 validmind-1.9.1/validmind/datasets/classification/customer_churn.py
+-rw-r--r--   0        0        0   545707 2023-05-12 23:35:53.261569 validmind-1.9.1/validmind/datasets/classification/datasets/bank_customer_churn.csv
+-rw-r--r--   0        0        0  2897191 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/classification/datasets/taiwan_credit.csv
+-rw-r--r--   0        0        0     1280 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/classification/taiwan_credit.py
+-rw-r--r--   0        0        0     1645 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/__init__.py
+-rw-r--r--   0        0        0   107835 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates.csv
+-rw-r--r--   0        0        0     2634 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv
+-rw-r--r--   0        0        0     2634 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv
+-rw-r--r--   0        0        0     2736 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv
+-rw-r--r--   0        0        0     3355 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv
+-rw-r--r--   0        0        0     3866 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv
+-rw-r--r--   0        0        0    11624 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/datasets/lending_club_loan_rates.csv
+-rw-r--r--   0        0        0     4378 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/fred.py
+-rw-r--r--   0        0        0     2346 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/lending_club.py
+-rw-r--r--   0        0        0    40067 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl
+-rw-r--r--   0        0        0    48314 2023-05-12 23:35:53.281572 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl
+-rw-r--r--   0        0        0    40063 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl
+-rw-r--r--   0        0        0    48292 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl
+-rw-r--r--   0        0        0    60343 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl
+-rw-r--r--   0        0        0    10529 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_utils.py
+-rw-r--r--   0        0        0     1290 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/__init__.py
+-rw-r--r--   0        0        0     6712 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/model_metadata.py
+-rw-r--r--   0        0        0        0 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/sklearn/__init__.py
+-rw-r--r--   0        0        0    13048 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/sklearn/metrics.py
+-rw-r--r--   0        0        0    31402 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/sklearn/threshold_tests.py
+-rw-r--r--   0        0        0        0 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/statsmodels/__init__.py
+-rw-r--r--   0        0        0    26596 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/statsmodels/metrics.py
+-rw-r--r--   0        0        0     1317 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/statsmodels/threshold_tests.py
+-rw-r--r--   0        0        0     1657 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/model_validation/utils.py
+-rw-r--r--   0        0        0     5182 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/__init__.py
+-rw-r--r--   0        0        0     2016 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/binary_classifier.py
+-rw-r--r--   0        0        0     2836 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/statsmodels_timeseries.py
+-rw-r--r--   0        0        0     1604 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/tabular_datasets.py
+-rw-r--r--   0        0        0     6821 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_plans/time_series.py
+-rw-r--r--   0        0        0     1894 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_suites/__init__.py
+-rw-r--r--   0        0        0     1344 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/test_suites/test_suites.py
+-rw-r--r--   0        0        0     6465 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/utils.py
+-rw-r--r--   0        0        0     1116 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/__init__.py
+-rw-r--r--   0        0        0    10425 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/dataset.py
+-rw-r--r--   0        0        0     8287 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/dataset_utils.py
+-rw-r--r--   0        0        0      592 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/figure.py
+-rw-r--r--   0        0        0     3746 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/metric.py
+-rw-r--r--   0        0        0     1757 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/metric_result.py
+-rw-r--r--   0        0        0     6530 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/model.py
+-rw-r--r--   0        0        0     3721 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/plot_utils.py
+-rw-r--r--   0        0        0     1518 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/result_summary.py
+-rw-r--r--   0        0        0     2501 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_context.py
+-rw-r--r--   0        0        0    11803 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_plan.py
+-rw-r--r--   0        0        0    18529 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_plan_result.py
+-rw-r--r--   0        0        0     1698 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_result.py
+-rw-r--r--   0        0        0     5019 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/test_suite.py
+-rw-r--r--   0        0        0     3620 2023-05-12 23:35:53.285573 validmind-1.9.1/validmind/vm_models/threshold_test.py
+-rw-r--r--   0        0        0     1385 1970-01-01 00:00:00.000000 validmind-1.9.1/PKG-INFO
```

### Comparing `validmind-1.9.0/pyproject.toml` & `validmind-1.9.1/pyproject.toml`

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
-version = "1.9.0"
+version = "1.9.1"
 
 [tool.poetry.dependencies]
 arch = "^5.4.0"
 click = "^8.0.4"
 dython = "^0.7.1"
 ipython = "^8.11.0"
 myst-parser = "^1.0.0"
```

### Comparing `validmind-1.9.0/validmind/__init__.py` & `validmind-1.9.1/validmind/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/api_client.py` & `validmind-1.9.1/validmind/api_client.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/client.py` & `validmind-1.9.1/validmind/client.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/data_validation/__init__.py` & `validmind-1.9.1/validmind/data_validation/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/data_validation/metrics.py` & `validmind-1.9.1/validmind/data_validation/metrics.py`

 * *Files 7% similar despite different names*

```diff
@@ -77,16 +77,15 @@
     Extracts the correlation matrix for a dataset. The following coefficients
     are calculated:
     - Pearson's R for numerical variables
     - Cramer's V for categorical variables
     - Correlation ratios for categorical-numerical variables
     """
 
-    type = "dataset"
-    key = "dataset_correlations"
+    name = "dataset_correlations"
     required_context = ["dataset"]
 
     # TODO: allow more metric metadata to be set, not just scope
     def __post_init__(self):
         self.scope = self.dataset.type
 
     def run(self):
@@ -98,16 +97,15 @@
 
 @dataclass
 class DatasetDescription(Metric):
     """
     Collects a set of descriptive statistics for a dataset
     """
 
-    type = "dataset"
-    key = "dataset_description"
+    name = "dataset_description"
     required_context = ["dataset"]
 
     def __post_init__(self):
         self.scope = self.dataset.type
 
     def run(self):
         # This will populate the "fields" attribute in the dataset object
@@ -118,16 +116,15 @@
 @dataclass
 class DescriptiveStatistics(Metric):
     """
     Collects a set of descriptive statistics for a dataset, both for
     numerical and categorical variables
     """
 
-    type = "dataset"
-    key = "descriptive_statistics"
+    name = "descriptive_statistics"
     required_context = ["dataset"]
 
     def get_summary_statistics_numerical(self, numerical_fields):
         percentiles = [0.25, 0.5, 0.75, 0.90, 0.95]
         summary_stats = self.df[numerical_fields].describe(percentiles=percentiles).T
         summary_stats = summary_stats[
             ["count", "mean", "std", "min", "25%", "50%", "75%", "90%", "95%", "max"]
@@ -197,16 +194,15 @@
 
 class DatasetSplit(Metric):
     """
     Attempts to extract information about the dataset split from the
     provided training, test and validation datasets.
     """
 
-    type = "dataset"
-    key = "dataset_split"
+    name = "dataset_split"
     required_context = ["model"]
 
     dataset_labels = {
         "train_ds": "Training",
         "test_ds": "Test",
         "validation_ds": "Validation",
         "total": "Total",
@@ -264,15 +260,15 @@
         for dataset_name in available_datasets:
             dataset = getattr(self.model, dataset_name, None)
             if dataset is not None:
                 total_size += len(dataset.df)
 
         # Then calculate the proportion of each dataset
         for dataset_name in available_datasets:
-            dataset = getattr(self, dataset_name, None)
+            dataset = getattr(self.model, dataset_name, None)
             if dataset is not None:
                 results[f"{dataset_name}_size"] = len(dataset.df)
                 results[f"{dataset_name}_proportion"] = len(dataset.df) / total_size
 
         results["total_size"] = total_size
 
         return self.cache_results(results)
@@ -281,16 +277,15 @@
 class TimeSeriesLinePlot(Metric):
     """
     Generates a visual analysis of time series data by plotting the
     raw time series. The input dataset can have multiple time series
     if necessary. In this case we produce a separate plot for each time series.
     """
 
-    type = "dataset"
-    key = "time_series_line_plot"
+    name = "time_series_line_plot"
     required_context = ["dataset"]
 
     def run(self):
         if "columns" not in self.params:
             raise ValueError("Time series columns must be provided in params")
 
         # Check if index is datetime
@@ -330,16 +325,15 @@
 class TimeSeriesHistogram(Metric):
     """
     Generates a visual analysis of time series data by plotting the
     histogram. The input dataset can have multiple time series if
     necessary. In this case we produce a separate plot for each time series.
     """
 
-    type = "dataset"
-    key = "time_series_histogram"
+    name = "time_series_histogram"
     required_context = ["dataset"]
 
     def run(self):
         if "columns" not in self.params:
             raise ValueError("Time series columns must be provided in params")
 
         # Check if index is datetime
@@ -372,16 +366,15 @@
 
 class ScatterPlot(Metric):
     """
     Generates a visual analysis of data by plotting a scatter plot matrix for all columns
     in the dataset. The input dataset can have multiple columns (features) if necessary.
     """
 
-    type = "dataset"
-    key = "scatter_plot"
+    name = "scatter_plot"
     required_context = ["dataset"]
 
     def run(self):
         if "columns" not in self.params:
             raise ValueError("Columns must be provided in params")
 
         columns = self.params["columns"]
@@ -409,16 +402,15 @@
 
 
 class LaggedCorrelationHeatmap(Metric):
     """
     Generates a heatmap of correlations between the target variable and the lags of independent variables in the dataset.
     """
 
-    type = "dataset"
-    key = "lagged_correlation_heatmap"
+    name = "lagged_correlation_heatmap"
     required_context = ["dataset"]
 
     def _compute_correlations(self, df, target_col, independent_vars, num_lags):
         correlations = np.zeros((len(independent_vars), num_lags + 1))
 
         for i, ind_var_col in enumerate(independent_vars):
             for lag in range(num_lags + 1):
@@ -489,16 +481,15 @@
 
 
 class AutoAR(Metric):
     """
     Automatically detects the AR order of a time series using both BIC and AIC.
     """
 
-    type = "dataset"  # assume this value
-    key = "auto_ar"
+    name = "auto_ar"
     required_context = ["dataset"]
 
     def run(self):
         if "max_ar_order" not in self.params:
             raise ValueError("max_ar_order must be provided in params")
 
         max_ar_order = self.params["max_ar_order"]
@@ -542,16 +533,15 @@
 
 
 class AutoMA(Metric):
     """
     Automatically detects the MA order of a time series using both BIC and AIC.
     """
 
-    type = "dataset"
-    key = "auto_ma"
+    name = "auto_ma"
     required_context = ["dataset"]
 
     def run(self):
         if "max_ma_order" not in self.params:
             raise ValueError("max_ma_order must be provided in params")
 
         max_ma_order = self.params["max_ma_order"]
@@ -595,16 +585,15 @@
 
 
 class SeasonalDecompose(Metric):
     """
     Calculates seasonal_decompose metric for each of the dataset features
     """
 
-    type = "dataset"
-    key = "seasonal_decompose"
+    name = "seasonal_decompose"
     required_context = ["dataset"]
     default_params = {"seasonal_model": "additive"}
 
     def store_seasonal_decompose(self, column, sd_one_column):
         """
         Stores the seasonal decomposition results in the test context so they
         can be re-used by other tests. Note we store one `sd` at a time for every
@@ -724,16 +713,15 @@
 
 class AutoSeasonality(Metric):
     """
     Automatically detects the optimal seasonal order for a time series dataset
     using the seasonal_decompose method.
     """
 
-    type = "dataset"
-    key = "auto_seasonality"
+    name = "auto_seasonality"
     required_context = ["dataset"]
     default_params = {"min_period": 1, "max_period": 4}
 
     def evaluate_seasonal_periods(self, series, min_period, max_period):
         seasonal_periods = []
         residual_errors = []
 
@@ -785,16 +773,15 @@
 
 
 class ACFandPACFPlot(Metric):
     """
     Plots ACF and PACF for a given time series dataset.
     """
 
-    type = "evaluation"
-    key = "acf_pacf_plot"
+    name = "acf_pacf_plot"
     required_context = ["dataset"]
 
     def run(self):
         if "columns" not in self.params:
             raise ValueError("Time series columns must be provided in params")
 
         # Check if index is datetime
@@ -889,16 +876,15 @@
 
 
 class RollingStatsPlot(Metric):
     """
     This class provides a metric to visualize the stationarity of a given time series dataset by plotting the rolling mean and rolling standard deviation. The rolling mean represents the average of the time series data over a fixed-size sliding window, which helps in identifying trends in the data. The rolling standard deviation measures the variability of the data within the sliding window, showing any changes in volatility over time. By analyzing these plots, users can gain insights into the stationarity of the time series data and determine if any transformations or differencing operations are required before applying time series models.
     """
 
-    type = "dataset"
-    key = "rolling_stats_plot"
+    name = "rolling_stats_plot"
     required_context = ["dataset"]
     default_params = {"window_size": 12}
 
     @staticmethod
     def plot_rolling_statistics(series, window_size=12, ax1=None, ax2=None):
         """
         Plot rolling mean and rolling standard deviation in different subplots for a given series.
@@ -963,16 +949,15 @@
 
 
 class EngleGrangerCoint(Metric):
     """
     Test for cointegration between pairs of time series variables in a given dataset using the Engle-Granger test.
     """
 
-    type = "dataset"
-    key = "engle_granger_coint"
+    name = "engle_granger_coint"
     required_context = ["dataset"]
     default_params = {"threshold": 0.05}
 
     def run(self):
         threshold = self.params["threshold"]
         df = self.dataset.df.dropna()
 
@@ -1009,16 +994,15 @@
 
 
 class SpreadPlot(Metric):
     """
     This class provides a metric to visualize the spread between pairs of time series variables in a given dataset. By plotting the spread of each pair of variables in separate figures, users can assess the relationship between the variables and determine if any cointegration or other time series relationships exist between them.
     """
 
-    type = "dataset"
-    key = "spread_plot"
+    name = "spread_plot"
     required_context = ["dataset"]
 
     @staticmethod
     def plot_spread(series1, series2, ax=None):
         """
         Plot the spread between two time series variables.
```

### Comparing `validmind-1.9.0/validmind/data_validation/threshold_tests.py` & `validmind-1.9.1/validmind/data_validation/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/classification/__init__.py` & `validmind-1.9.1/validmind/datasets/classification/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/classification/customer_churn.py` & `validmind-1.9.1/validmind/datasets/classification/customer_churn.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/classification/datasets/bank_customer_churn.csv` & `validmind-1.9.1/validmind/datasets/classification/datasets/bank_customer_churn.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/classification/datasets/taiwan_credit.csv` & `validmind-1.9.1/validmind/datasets/classification/datasets/taiwan_credit.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/classification/taiwan_credit.py` & `validmind-1.9.1/validmind/datasets/classification/taiwan_credit.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/__init__.py` & `validmind-1.9.1/validmind/datasets/regression/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates.csv` & `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv` & `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv` & `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv` & `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv` & `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv` & `validmind-1.9.1/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/datasets/lending_club_loan_rates.csv` & `validmind-1.9.1/validmind/datasets/regression/datasets/lending_club_loan_rates.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/fred.py` & `validmind-1.9.1/validmind/datasets/regression/fred.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/lending_club.py` & `validmind-1.9.1/validmind/datasets/regression/lending_club.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl` & `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl` & `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl` & `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl` & `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl` & `validmind-1.9.1/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/model_utils.py` & `validmind-1.9.1/validmind/model_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/model_validation/__init__.py` & `validmind-1.9.1/validmind/model_validation/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/model_validation/model_metadata.py` & `validmind-1.9.1/validmind/model_validation/model_metadata.py`

 * *Files 2% similar despite different names*

```diff
@@ -173,17 +173,15 @@
     """
     Custom class to collect the following metadata for a model:
     - Model architecture
     - Model hyperparameters
     - Model task type
     """
 
-    type = "model"
-    scope = "test"
-    key = "model_metadata"
+    name = "model_metadata"
     required_context = ["model"]
 
     column_labels = {
         "architecture": "Modeling Technique",
         "framework": "Modeling Framework",
         "framework_version": "Framework Version",
         "language": "Programming Language",
```

### Comparing `validmind-1.9.0/validmind/model_validation/sklearn/metrics.py` & `validmind-1.9.1/validmind/model_validation/sklearn/metrics.py`

 * *Files 10% similar despite different names*

```diff
@@ -86,17 +86,15 @@
 
 @dataclass
 class AccuracyScore(Metric):
     """
     Accuracy Score
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "accuracy"
+    name = "accuracy"
     required_context = ["model"]
 
     def run(self):
         y_true = self.model.test_ds.y
         class_pred = self.model.class_predictions(self.model.y_test_predict)
         accuracy_score = metrics.accuracy_score(y_true, class_pred)
 
@@ -105,16 +103,15 @@
 
 @dataclass
 class CharacteristicStabilityIndex(Metric):
     """
     Characteristic Stability Index between two datasets
     """
 
-    type = "training"
-    key = "csi"
+    name = "csi"
     required_context = ["model"]
     value_formatter = "key_values"
 
     def run(self):
         """
         Calculates PSI for each of the dataset features
         """
@@ -137,19 +134,20 @@
 
 @dataclass
 class ConfusionMatrix(Metric):
     """
     Confusion Matrix
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "confusion_matrix"
+    name = "confusion_matrix"
     required_context = ["model"]
 
+    def summary(self, metric_value):
+        return None
+
     def run(self):
         y_true = self.model.test_ds.y
         y_labels = list(map(lambda x: x.item(), y_true.unique()))
         y_labels.sort()
 
         class_pred = self.model.class_predictions(self.model.y_test_predict)
 
@@ -179,17 +177,15 @@
 
 @dataclass
 class F1Score(Metric):
     """
     F1 Score
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "f1_score"
+    name = "f1_score"
     required_context = ["model"]
 
     def run(self):
         y_true = self.model.test_ds.y
         class_pred = self.model.class_predictions(self.model.y_test_predict)
         f1_score = metrics.f1_score(y_true, class_pred)
 
@@ -198,17 +194,15 @@
 
 @dataclass
 class PermutationFeatureImportance(Metric):
     """
     Permutation Feature Importance
     """
 
-    type = "training"
-    scope = "training_dataset"
-    key = "pfi"
+    name = "pfi"
     required_context = ["model"]
 
     def run(self):
         x = self.model.train_ds.x
         y = self.model.train_ds.y
 
         model_instance = self.model.model
@@ -256,17 +250,15 @@
 
 @dataclass
 class PrecisionRecallCurve(Metric):
     """
     Precision Recall Curve
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "pr_curve"
+    name = "pr_curve"
     required_context = ["model"]
 
     def run(self):
         y_true = self.model.test_ds.df[self.model.test_ds.target_column]
         precision, recall, pr_thresholds = metrics.precision_recall_curve(
             y_true, self.model.y_test_predict
         )
@@ -288,17 +280,15 @@
 
 @dataclass
 class PrecisionScore(Metric):
     """
     Precision Score
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "precision"
+    name = "precision"
     required_context = ["model"]
 
     def run(self):
         y_true = self.model.test_ds.df[self.model.test_ds.target_column]
         class_pred = self.model.class_predictions(self.model.y_test_predict)
         precision = metrics.precision_score(y_true, class_pred)
 
@@ -307,17 +297,15 @@
 
 @dataclass
 class RecallScore(Metric):
     """
     Recall Score
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "recall"
+    name = "recall"
     required_context = ["model"]
 
     def run(self):
         y_true = self.model.test_ds.df[self.model.test_ds.target_column]
         class_pred = self.model.class_predictions(self.model.y_test_predict)
         recall = metrics.recall_score(y_true, class_pred)
 
@@ -326,17 +314,15 @@
 
 @dataclass
 class ROCAUCScore(Metric):
     """
     ROC AUC Score
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "roc_auc"
+    name = "roc_auc"
     required_context = ["model"]
 
     def run(self):
         return self.cache_results(
             metric_value=metrics.roc_auc_score(
                 self.model.test_ds.df[self.model.test_ds.target_column],
                 self.model.class_predictions(self.model.y_test_predict),
@@ -346,17 +332,15 @@
 
 @dataclass
 class ROCCurve(Metric):
     """
     ROC Curve
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "roc_curve"
+    name = "roc_curve"
     required_context = ["model"]
 
     def run(self):
         y_true = self.model.test_ds.df[self.model.test_ds.target_column]
         class_pred = self.model.class_predictions(self.model.y_test_predict)
         fpr, tpr, roc_thresholds = metrics.roc_curve(
             y_true, self.model.y_test_predict, drop_intermediate=True
@@ -383,16 +367,14 @@
 @dataclass
 class SHAPGlobalImportance(Metric):
     """
     SHAP Global Importance
     """
 
     required_context = ["model"]
-
-    # Instance Variables
     name = "shap"
 
     def _generate_shap_plot(self, type_, shap_values, x_test):
         """
         Plots two types of SHAP global importance (SHAP).
         :params type: mean, summary
         :params shap_values: a matrix
@@ -455,16 +437,15 @@
 
 @dataclass
 class PopulationStabilityIndex(Metric):
     """
     Population Stability Index between two datasets
     """
 
-    type = "training"
-    key = "psi"
+    name = "psi"
     required_context = ["model"]
     value_formatter = "records"
 
     def run(self):
         model_library = Model.model_library(self.model.model)
         if model_library == "statsmodels" or model_library == "pytorch":
             print(f"Skiping PSI for {model_library} models")
```

### Comparing `validmind-1.9.0/validmind/model_validation/sklearn/threshold_tests.py` & `validmind-1.9.1/validmind/model_validation/sklearn/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/model_validation/statsmodels/metrics.py` & `validmind-1.9.1/validmind/model_validation/statsmodels/metrics.py`

 * *Files 15% similar despite different names*

```diff
@@ -27,16 +27,15 @@
 
 @dataclass
 class ResidualsVisualInspection(Metric):
     """
     Log plots for visual inspection of residuals
     """
 
-    type = "evaluation"
-    key = "residuals_visual_inspection"
+    name = "residuals_visual_inspection"
 
     def get_residuals(self, column, series):
         """
         Get the seasonal decomposition residuals from the test
         context or re-compute them if not available. This allows
         running the test individually or as part of a test plan.
         """
@@ -100,16 +99,15 @@
 
 class ADF(Metric):
     """
     Augmented Dickey-Fuller unit root test for establishing the order of integration of
     time series
     """
 
-    type = "dataset"  # assume this value
-    key = "adf"
+    name = "adf"
 
     def run(self):
         """
         Calculates ADF metric for each of the dataset features
         """
         dataset = self.dataset.df
 
@@ -133,17 +131,15 @@
 @dataclass
 class KolmogorovSmirnov(Metric):
     """
     The Kolmogorov-Smirnov metric is a statistical test used to determine
     whether a given set of data follows a normal distribution.
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "kolmogorov_smirnov"
+    name = "kolmogorov_smirnov"
 
     def run(self):
         """
         Calculates KS for each of the dataset features
         """
         x_train = self.train_ds.df
         x_train = self.train_ds.df
@@ -158,17 +154,15 @@
 
 class ShapiroWilk(Metric):
     """
     The Shapiro-Wilk test is a statistical test used to determine
     whether a given set of data follows a normal distribution.
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "shapiro_wilk"
+    name = "shapiro_wilk"
 
     def run(self):
         """
         Calculates Shapiro-Wilk test for each of the dataset features.
         """
         x_train = self.train_ds.df
         x_train = self.train_ds.df
@@ -188,17 +182,15 @@
 @dataclass
 class Lilliefors(Metric):
     """
     The Lilliefors test is a statistical test used to determine
     whether a given set of data follows a normal distribution.
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "lilliefors_test"
+    name = "lilliefors_test"
 
     def run(self):
         """
         Calculates Lilliefors test for each of the dataset features
         """
         x_train = self.train_ds.df
         x_train = self.train_ds.df
@@ -216,17 +208,15 @@
 
 class JarqueBera(Metric):
     """
     The Jarque-Bera test is a statistical test used to determine
     whether a given set of data follows a normal distribution.
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "jarque_bera"
+    name = "jarque_bera"
 
     def run(self):
         """
         Calculates JB for each of the dataset features
         """
         x_train = self.train_ds.df
         x_train = self.train_ds.df
@@ -248,17 +238,15 @@
 class LJungBox(Metric):
     """
     The Ljung-Box test is a statistical test used to determine
     whether a given set of data has autocorrelations
     that are different from zero.
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "ljung_box"
+    name = "ljung_box"
 
     def run(self):
         """
         Calculates Ljung-Box test for each of the dataset features
         """
         x_train = self.train_ds.df
         x_train = self.train_ds.df
@@ -278,17 +266,15 @@
 class BoxPierce(Metric):
     """
     The Box-Pierce test is a statistical test used to determine
     whether a given set of data has autocorrelations
     that are different from zero.
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "box_pierce"
+    name = "box_pierce"
 
     def run(self):
         """
         Calculates Box-Pierce test for each of the dataset features
         """
         x_train = self.train_ds.df
         x_train = self.train_ds.df
@@ -309,17 +295,15 @@
 class RunsTest(Metric):
     """
     The runs test is a statistical test used to determine whether a given set
     of data has runs of positive and negative values that are longer than expected
     under the null hypothesis of randomness.
     """
 
-    type = "evaluation"
-    scope = "test"
-    key = "runs_test"
+    name = "runs_test"
 
     def run(self):
         """
         Calculates the run test for each of the dataset features
         """
         x_train = self.train_ds.df
         x_train = self.train_ds.df
@@ -339,17 +323,15 @@
 @dataclass
 class DurbinWatsonTest(Metric):
     """
     The Durbin-Watson Metric is a statistical test that
     can be used to detect autocorrelation in a time series.
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "durbin_watson"
+    name = "durbin_watson"
 
     def run(self):
         """
         Calculates DB for each of the dataset features
         """
         x_train = self.train_ds.df
         x_train = self.train_ds.df
@@ -364,17 +346,15 @@
 @dataclass
 class PhillipsPerronArch(Metric):
     """
     Phillips-Perron (PP) unit root test for
     establishing the order of integration of time series
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "phillips_perron"
+    name = "phillips_perron"
 
     def run(self):
         """
         Calculates PP metric for each of the dataset features
         """
         dataset = self.dataset.df
 
@@ -394,17 +374,15 @@
 @dataclass
 class ZivotAndrewsArch(Metric):
     """
     Zivot-Andrews unit root test for
     establishing the order of integration of time series
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "zivot_andrews"
+    name = "zivot_andrews"
 
     def run(self):
         """
         Calculates Zivot-Andrews metric for each of the dataset features
         """
         dataset = self.dataset.df
 
@@ -424,17 +402,15 @@
 @dataclass
 class DFGLSArch(Metric):
     """
     Dickey-Fuller GLS unit root test for
     establishing the order of integration of time series
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "dickey_fuller_gls"
+    name = "dickey_fuller_gls"
 
     def run(self):
         """
         Calculates Dickey-Fuller GLS metric for each of the dataset features
         """
         dataset = self.dataset.df
 
@@ -454,17 +430,15 @@
 @dataclass
 class KPSS(Metric):
     """
     Kwiatkowski-Phillips-Schmidt-Shin (KPSS) unit root test for
     establishing the order of integration of time series
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "kpss"
+    name = "kpss"
 
     def run(self):
         """
         Calculates KPSS for each of the dataset features
         """
         dataset = self.dataset.df
 
@@ -486,17 +460,15 @@
     """
     This class calculates the order of integration for each feature
     in a dataset using the Augmented Dickey-Fuller (ADF) test.
     The order of integration is the number of times a series
     needs to be differenced to make it stationary.
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "integration_order_adf"
+    name = "integration_order_adf"
     default_params = {"max_order": 3}
 
     def run(self):
         """
         Calculates the ADF order of integration for each of the dataset features.
         """
         x_train = self.train_ds.df
@@ -520,17 +492,15 @@
 
 
 class AutoARIMA(Metric):
     """
     Automatically fits multiple ARIMA models for each variable and ranks them by BIC and AIC.
     """
 
-    type = "evaluation"  # assume this value
-    scope = "test"  # assume this value (could be "train")
-    key = "auto_arima"
+    name = "auto_arima"
 
     max_p = 3
     max_d = 2
     max_q = 3
 
     def run(self):
         x_train = self.train_ds.df
@@ -577,16 +547,14 @@
 
 @dataclass
 class RegressionModelSummary(Metric):
     """
     Test that output the summary of regression models of statsmodel library.
     """
 
-    category = "model_performance"
-    scope = "test"
     name = "regression_model_summary"
 
     def run(self):
         # statsmodels library information
         module_name = self.model.model.__class__.__module__
         library_name = module_name.split(".")[0]
         model_name = self.model.model.__class__.__name__
@@ -620,16 +588,14 @@
 
 @dataclass
 class RegressionModelInsampleComparison(Metric):
     """
     Test that output the comparison of stats library regression models.
     """
 
-    category = "model_performance"
-    scope = "test"
     name = "regression_insample_performance"
 
     def description(self):
         return """
         This section shows In-sample comparison of regression models involves comparing
         the performance of different regression models on the same dataset that was used
         to train the models. This is typically done by calculating a goodness-of-fit statistic
@@ -704,16 +670,14 @@
 @dataclass
 class RegressionModelOutsampleComparison(Metric):
     """
     Test that evaluates the performance of different regression models on a separate test dataset
     that was not used to train the models.
     """
 
-    category = "model_performance"
-    scope = "test"
     name = "regression_outsample_performance"
 
     def description(self):
         return """
         This section shows Out-of-sample comparison of regression models involves evaluating
         the performance of different regression models on a separate test dataset that was not
         used to train the models. This is typically done by calculating a goodness-of-fit statistic
@@ -794,17 +758,15 @@
 
 @dataclass
 class RegressionModelForecastPlot(Metric):
     """
     This metric creates a plot of forecast vs observed for each model in the list.
     """
 
-    category = "model_forecast"
-    scope = "test"
-    key = "regression_forecast_plot"
+    name = "regression_forecast_plot"
     default_params = {"start_date": None, "end_date": None}
 
     def description(self):
         return """
         This section shows plots of training and test datasets vs forecast trainining and forecast test.
         """
```

### Comparing `validmind-1.9.0/validmind/model_validation/statsmodels/threshold_tests.py` & `validmind-1.9.1/validmind/model_validation/statsmodels/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/model_validation/utils.py` & `validmind-1.9.1/validmind/model_validation/utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/test_plans/__init__.py` & `validmind-1.9.1/validmind/test_plans/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,15 +11,14 @@
     BinaryClassifierPerformance,
     BinaryClassifierDiagnosis,
 )
 from .tabular_datasets import (
     TabularDataQuality,
     TabularDatasetDescription,
     TimeSeriesDataQuality,
-    TimeSeriesDataset,
 )
 from .statsmodels_timeseries import (
     NormalityTestPlan,
     AutocorrelationTestPlan,
     SesonalityTestPlan,
     UnitRoot,
     StationarityTestPlan,
@@ -42,15 +41,14 @@
     "normality_test_plan": NormalityTestPlan,
     "autocorrelation_test_plan": AutocorrelationTestPlan,
     "seasonality_test_plan": SesonalityTestPlan,
     "unit_root": UnitRoot,
     "stationarity_test_plan": StationarityTestPlan,
     "timeseries": TimeSeries,
     "time_series_data_quality": TimeSeriesDataQuality,
-    "time_series_dataset": TimeSeriesDataset,
     "time_series_univariate": TimeSeriesUnivariate,
     "time_series_multivariate": TimeSeriesMultivariate,
     "time_series_forecast": TimeSeriesForecast,
     "regression_model_performance": RegressionModelPerformance,
     "regression_models_comparison": RegressionModelsComparison,
 }
```

### Comparing `validmind-1.9.0/validmind/test_plans/binary_classifier.py` & `validmind-1.9.1/validmind/test_plans/binary_classifier.py`

 * *Files 6% similar despite different names*

```diff
@@ -76,8 +76,12 @@
 class BinaryClassifierDiagnosis(TestPlan):
     """
     Test plan for sklearn classifier model diagnosis tests
     """
 
     name = "binary_classifier_model_diagnosis"
     required_context = ["model"]
-    tests = [OverfitDiagnosis, WeakspotsDiagnosis, RobustnessDiagnosis]
+    tests = [
+        OverfitDiagnosis,
+        WeakspotsDiagnosis,
+        RobustnessDiagnosis,
+    ]
```

### Comparing `validmind-1.9.0/validmind/test_plans/statsmodels_timeseries.py` & `validmind-1.9.1/validmind/test_plans/statsmodels_timeseries.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/test_plans/tabular_datasets.py` & `validmind-1.9.1/validmind/test_plans/tabular_datasets.py`

 * *Files 7% similar despite different names*

```diff
@@ -66,19 +66,7 @@
     """
     Test plan for data quality on time series datasets
     """
 
     name = "time_series_data_quality"
     required_context = ["dataset"]
     tests = [TimeSeriesOutliers, TimeSeriesMissingValues, TimeSeriesFrequency]
-
-
-class TimeSeriesDataset(TestPlan):
-    """
-    Test plan for time series  datasets
-    """
-
-    name = "time_series_dataset"
-    required_context = ["dataset"]
-    test_plans = [
-        TimeSeriesDataQuality,
-    ]
```

### Comparing `validmind-1.9.0/validmind/test_plans/time_series.py` & `validmind-1.9.1/validmind/test_plans/time_series.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/test_suites/__init__.py` & `validmind-1.9.1/validmind/test_suites/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,21 +3,23 @@
 """
 import tabulate
 
 from .test_suites import (
     BinaryClassifierFullSuite,
     BinaryClassifierModelValidation,
     TabularDataset,
+    TimeSeriesDataset,
 )
 from ..vm_models import TestSuite
 
 core_test_suites = {
     "binary_classifier_full_suite": BinaryClassifierFullSuite,
     "binary_classifier_model_validation": BinaryClassifierModelValidation,
     "tabular_dataset": TabularDataset,
+    "time_series_dataset": TimeSeriesDataset,
 }
 
 # These test suites can be added by the user
 custom_test_suites = {}
 
 
 def _get_all_test_suites():
```

### Comparing `validmind-1.9.0/validmind/test_suites/test_suites.py` & `validmind-1.9.1/validmind/test_suites/test_suites.py`

 * *Files 8% similar despite different names*

```diff
@@ -45,7 +45,19 @@
     test_plans = [
         "tabular_dataset_description",
         "tabular_data_quality",
         "binary_classifier_metrics",
         "binary_classifier_validation",
         "binary_classifier_model_diagnosis",
     ]
+
+
+class TimeSeriesDataset(TestSuite):
+    """
+    Test suite for time series datasets.
+    """
+    name = "time_series_dataset"
+    required_context = ["dataset"]
+
+    test_plans = [
+        "time_series_data_quality",
+    ]
```

### Comparing `validmind-1.9.0/validmind/utils.py` & `validmind-1.9.1/validmind/utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/__init__.py` & `validmind-1.9.1/validmind/vm_models/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/dataset.py` & `validmind-1.9.1/validmind/vm_models/dataset.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/dataset_utils.py` & `validmind-1.9.1/validmind/vm_models/dataset_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/figure.py` & `validmind-1.9.1/validmind/vm_models/figure.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/metric.py` & `validmind-1.9.1/validmind/vm_models/metric.py`

 * *Files 5% similar despite different names*

```diff
@@ -25,15 +25,15 @@
     # Test Context
     test_context: TestContext
 
     # Class Variables
     test_type: ClassVar[str] = "Metric"
     type: ClassVar[str] = ""  # type of metric: "training", "evaluation", etc.
     scope: ClassVar[str] = ""  # scope of metric: "training_dataset"
-    key: ClassVar[str] = ""  # unique identifer for metric: "accuracy"
+    name: ClassVar[str] = ""  # unique identifer for metric: "accuracy"
     value_formatter: ClassVar[Optional[str]] = None  # "records" or "key_values"
     default_params: ClassVar[dict] = {}
 
     # Instance Variables
     params: dict = None
     result: TestPlanMetricResult = None
 
@@ -41,16 +41,19 @@
         """
         Set default params if not provided
         """
         if self.params is None:
             self.params = self.default_params
 
     @property
-    def name(self):
-        return self.key
+    def key(self):
+        """
+        Keep the key for compatibility reasons
+        """
+        return self.name
 
     def description(self):
         """
         Return the metric description. Should be overridden by subclasses. Defaults
         to returning the class' docstring
         """
         return self.__doc__.strip()
```

### Comparing `validmind-1.9.0/validmind/vm_models/metric_result.py` & `validmind-1.9.1/validmind/vm_models/metric_result.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/model.py` & `validmind-1.9.1/validmind/vm_models/model.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/plot_utils.py` & `validmind-1.9.1/validmind/vm_models/plot_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/result_summary.py` & `validmind-1.9.1/validmind/vm_models/result_summary.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/test_context.py` & `validmind-1.9.1/validmind/vm_models/test_context.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/test_plan.py` & `validmind-1.9.1/validmind/vm_models/test_plan.py`

 * *Files 2% similar despite different names*

```diff
@@ -176,27 +176,27 @@
             test_params = self.get_config_params_for_test(test_name)
             test_instance = test(self.test_context, params=test_params)
 
             self.pbar_description.value = (
                 f"Running {test.test_type}: {test_instance.name}"
             )
 
-            result = test_instance.run()
+            test_instance.run()
 
-            if result is None:
+            if test_instance.result is None:
                 self.pbar_description.value = "Test returned None, skipping..."
                 self.pbar.value += 1
                 continue
 
-            if not isinstance(result, TestPlanResult):
+            if not isinstance(test_instance.result, TestPlanResult):
                 raise ValueError(
                     f"'{test_instance.name}' must return an instance of TestPlanResult Base Class"
                 )
 
-            self.results.append(result)
+            self.results.append(test_instance.result)
             self.pbar.value += 1
 
         if send:
             self.log_results()
 
         # TODO: remove
         for test_plan in self.test_plans:
@@ -222,15 +222,17 @@
         collected. This method will log the results to ValidMind.
         """
         self.pbar_description.value = (
             f"Sending results of test plan '{self.name}' to ValidMind..."
         )
 
         for result in self.results:
-            self.pbar_description.value = f"Logging result: {result.result_id}"
+            self.pbar_description.value = (
+                f"Sending result to ValidMind: {result.result_id}..."
+            )
 
             try:
                 result.log()
             except Exception as e:
                 self.pbar.set_description(
                     f"Failed to log result: {result} for test plan result '{str(result)}'"
                 )
@@ -252,21 +254,25 @@
         """
         return f'<div class="result">{clean_docstring(self.description())}</div>'
 
     def _results_summary(self) -> str:
         """
         Builds a summary of the results for each of the tests in the test plan
         """
-        accordions = []
+        accordions = {}
+        id = 0
         for result in self.results:
-            result_html = result._to_html()
-            if result_html:
-                accordions.append(
-                    widgets.HTML(value=f'<div class="result">{result_html}</div>')
-                )
+            result_widget = result._to_widget()
+            if result_widget:
+                accordions[result.result_id] = {
+                    "id": id,
+                    "widget": result_widget,
+                    "result": result,
+                }
+                id += 1
 
         return accordions
 
     def summarize(self, render_summary: bool = True):
         """Summarizes the results of the test plan
 
         This method will be called after the test plan has been run and all results have been
@@ -285,19 +291,22 @@
         # Only show the title if we are rendering the summary here
         if render_summary:
             vbox_children.append(widgets.HTML(value=self._results_title()))
 
         vbox_children.append(widgets.HTML(value=self._results_description()))
 
         accordion_contents = self._results_summary()
-        accordion_widget = widgets.Accordion(children=accordion_contents)
-        for i, _ in enumerate(accordion_widget.children):
-            result_id = self.results[i].result_id
-            title = f'{result_id.title().replace("_", " ")} ({result_id})'
-            accordion_widget.set_title(i, title)
+        accordion_items = [v["widget"] for v in accordion_contents.values()]
+        accordion_widget = widgets.Accordion(children=accordion_items)
+
+        for result_id, accordion_item in accordion_contents.items():
+            result = accordion_item["result"]
+            result_name = f"{result.name}: " if result.name else ""
+            title = f'{result_name }{result_id.title().replace("_", " ")} ({result_id})'
+            accordion_widget.set_title(accordion_item["id"], title)
 
         vbox_children.append(accordion_widget)
 
         style_footer = widgets.HTML(
             value="""
         <style>
             .result {
@@ -315,14 +324,15 @@
         if render_summary:
             vbox_children.append(style_footer)
 
         self.summary = widgets.VBox(vbox_children)
 
         if render_summary:
             display(self.summary)
+            self.pbar_description.value = "Test plan complete!"
 
     def _get_all_subtest_plan_results(self) -> List[TestPlanResult]:
         """
         Recursively gets all sub test plan results since a test plan
         can have sub test plans which can have sub test plans and so on.
         """
         results = []
```

### Comparing `validmind-1.9.0/validmind/vm_models/test_plan_result.py` & `validmind-1.9.1/validmind/vm_models/test_plan_result.py`

 * *Files 16% similar despite different names*

```diff
@@ -3,33 +3,36 @@
 """
 # TODO: we are probably going to want to move all this html generation into an html template file
 # and use something like jinja to render it. This is fine for now, but the html is a bit messy
 import os
 
 from abc import ABC, abstractmethod
 from dataclasses import dataclass
-from io import BytesIO, StringIO
+from io import BytesIO
 from typing import List, Optional
 import base64
 
-from IPython.display import display, HTML
+from IPython.display import display
+import ipywidgets as widgets
+import pandas as pd
 
 from ..api_client import (
     get_metadata,
     log_dataset,
     log_figure,
     log_metadata,
     log_metrics,
     log_model,
     log_test_result,
 )
 from .dataset import Dataset
 from .figure import Figure
 from .metric_result import MetricResult
 from .model import Model
+from .result_summary import ResultSummary
 from .test_result import TestResults
 
 
 def update_metadata(content_id: str, text: str) -> None:
     """
     Update the metadata of a content item. By default we don't
     override the existing metadata, but we can override it by
@@ -42,136 +45,113 @@
         existing_metadata is None
         or VM_OVERRIDE_METADATA == "True"
         or VM_OVERRIDE_METADATA is True
     ):
         log_metadata(content_id, text)
 
 
-def plot_figures(html: StringIO, figures: List[Figure]) -> None:
+def plot_figures(figures: List[Figure]) -> None:
     """
-    Plot figures to html
+    Plot figures to a ipywidgets GridBox
     """
 
-    plot_htmls = []
+    plots = []
 
     for fig in figures:
         tmpfile = BytesIO()
         fig.figure.savefig(tmpfile, format="png")
         encoded = base64.b64encode(tmpfile.getvalue()).decode("utf-8")
-        plot_htmls.append(
-            f"""
-        <div class="metric-plot">
-            <img src="data:image/png;base64,{encoded}"/>
-        </div>
-        """
+        plots.append(
+            widgets.HTML(
+                value=f"""
+                <img src="data:image/png;base64,{encoded}"/>
+                """
+            )
         )
 
-    if len(plot_htmls) > 2:
-        # if theres a lot of plots, we want to only show the first
-        # one and then have an expand button to show the rest
-        html.write(
-            f"""
-        <div class="metric-value">
-            <div class="metric-value-title">
-                Metric Plots
-            </div>
-            <div class="metric-value-value">
-                <a onclick="showMetricPlots(this)" style="cursor: pointer; color: blue;">
-                Show All Plots
-                </a>
-            </div>
-            <div class="metric-value-value">
-                {plot_htmls[0]}
-                <div class="allplots" style="display: none;">
-                    {"".join(plot_htmls[1:])}
-                </div>
-            </div>
-        </div>
-        <script>
-            function showMetricPlots(btn) {{
-                const plots = btn.parentElement.parentElement.querySelector(".allplots");
-                if (plots.style.display === "none") {{
-                    plots.style.display = "block";
-                    btn.innerHTML = "Collapse";
-                }} else {{
-                    plots.style.display = "none";
-                    btn.innerHTML = "Show All Plots";
-                }}
-            }}
-        </script>
-        """
-        )
-    else:
-        html.write(
-            f"""
-        <div class="metric-value">
-            <div class="metric-value-title">Metric Plots</div>
-            <div class="metric-value-value">
-                {"".join(plot_htmls)}
-            </div>
-        </div>
-        """
-        )
+    num_columns = len(figures) if len(figures) <= 3 else 3
+
+    return widgets.GridBox(
+        plots,
+        layout=widgets.Layout(grid_template_columns=f"repeat({num_columns}, 1fr)"),
+    )
 
 
 @dataclass
 class TestPlanResult(ABC):
     """Base Class for test plan results"""
 
+    name: str = "TestPlanResult"
     # id of the result, can be set by the subclass. This helps
     # looking up results later on
     result_id: str = None
     # Text metadata about the result, can include description, etc.
     result_metadata: List[dict] = None
 
     def __str__(self) -> str:
         """May be overridden by subclasses"""
         return self.__class__.__name__
 
     @abstractmethod
-    def _to_html(self):
-        """Create an html representation of the result... Must be overridden by subclasses"""
+    def _to_widget(self):
+        """Create an ipywdiget representation of the result... Must be overridden by subclasses"""
         raise NotImplementedError
 
+    def _summary_tables_to_widget(self, summary: ResultSummary):
+        """
+        Create an ipywdiget representation of the summary tables
+        """
+        tables = []
+        for table in summary.results:
+            summary_table = pd.DataFrame(
+                table.data
+            ).to_html()  # table.data is an orient=records dump
+
+            if table.metadata and table.metadata.title:
+                tables.append(widgets.HTML(value=f"<h3>{table.metadata.title}</h3>"))
+            tables.append(widgets.HTML(value=summary_table))
+        return tables
+
     def show(self):
         """Display the result... May be overridden by subclasses"""
-        display(HTML(self._to_html()))
+        display(self._to_widget())
 
     @abstractmethod
     def log(self):
         """Log the result... Must be overridden by subclasses"""
         raise NotImplementedError
 
 
 @dataclass
 class TestPlanDatasetResult(TestPlanResult):
     """
     Result wrapper for datasets that run as part of a test plan
     """
 
+    name: str = "Metric"
     result_id: str = None
     dataset: Dataset = None
 
     def __repr__(self) -> str:
         return f'TestPlanDatasetResult(result_id="{self.result_id}")'
 
-    def _to_html(self):
-        html = "<h4>Logged the following dataset to the ValidMind platform:</h4>"
-        return html + self.dataset.df.describe().to_html()
+    def _to_widget(self):
+        return widgets.HTML(value=self.dataset.df.describe().to_html())
 
     def log(self):
         log_dataset(self.dataset)
 
 
 @dataclass
 class TestPlanMetricResult(TestPlanResult):
     """
     Result wrapper for metrics that run as part of a test plan
     """
 
+    name: str = "Metric"
     figures: Optional[List[Figure]] = None
     metric: Optional[MetricResult] = None
 
     def __repr__(self) -> str:
         if self.metric:
             return f'{self.__class__.__name__}(result_id="{self.result_id}", metric, figures)'
         else:
@@ -179,72 +159,87 @@
 
     def __str__(self) -> str:
         if self.metric:
             return f'{self.__class__.__name__}(result_id="{self.result_id}", metric, figures)'
         else:
             return f"{self.__class__.__name__}(result_id={self.result_id}, figures)"
 
-    def _to_html(self):
+    def _to_widget(self):
         if self.metric and self.metric.key == "dataset_description":
             return ""
 
-        html = StringIO()
+        vbox_children = []
 
-        if self.metric:
-            html.write(
-                f"""
-            <h4>Logged the following {self.metric.type} metric to the ValidMind platform:</h4>
-            """
-            )
-        else:
-            html.write(
-                f"""
-            <h4>Logged the following plot{"s" if len(self.figures) > 1 else ""}
-            to the ValidMind platform:</h4>
-            """
+        if self.result_metadata:
+            metric_description = self.result_metadata[0]
+            vbox_children.append(
+                widgets.HTML(value=f"<p>{metric_description.get('text', '')}</p>")
             )
 
         if self.metric:
-            metric_value = self.metric.value
-            # Don't log the entire metric if it has more than 1000 characters
-            if len(metric_value.__str__()) > 1024:
-                metric_value = metric_value.__str__()[:1024] + "..."
-
-            html.write(
-                f"""
-            <div class="metric-result">
-                <div class="metric-result-body">
-                    <div class="metric-body-column">
-                        <div class="metric-body-column-title">Metric Name</div>
-                        <div class="metric-body-column-value">{self.metric.key}</div>
-                    </div>
-                    <div class="metric-body-column">
-                        <div class="metric-body-column-title">Metric Type</div>
-                        <div class="metric-body-column-value">{self.metric.type}</div>
-                    </div>
-                    <div class="metric-body-column">
-                        <div class="metric-body-column-title">Metric Scope</div>
-                        <div class="metric-body-column-value">{self.metric.scope}</div>
-                    </div>
-                </div>
-                <div class="metric-value">
-                    <div class="metric-value-title">Metric Value</div>
-                    <div class="metric-value-value">
-                        <pre>{metric_value}</pre>
-                    </div>
-                </div>
-            """
-            )
+            if self.metric.summary:
+                tables = self._summary_tables_to_widget(self.metric.summary)
+                vbox_children.extend(tables)
+            # else:
+            # vbox_children.append(
+            #     widgets.HTML(
+            #         value=f"""<h4>Unable to display metric summary for {self.result_id}. Please make sure the summary() method is implemented for this metric</h4>"""
+            #     )
+            # )
+
+            # Disable for now and fix later
+            #
+            # view_raw_data_button = widgets.Button(description="View Raw Data")
+
+            # # Hide raw data by default
+            # output = widgets.Output()
+            # output.layout.display = "none"
+
+            # metric_value = self.metric.value
+            # metric_output = (
+            #     json.dumps(metric_value, indent=2, cls=NumpyEncoder)
+            #     if type(metric_value) == dict
+            #     else str(metric_value)
+            # )
+
+            # with output:
+            #     display(
+            #         widgets.HTML(
+            #             value=f"""
+            #         <div class="metric-result">
+            #             <div class="metric-value">
+            #                 <div class="metric-value-title">Raw Metric Value</div>
+            #                 <div class="metric-value-value">
+            #                     <pre>{metric_output}</pre>
+            #                 </div>
+            #             </div>
+            #         </div>
+            #         """
+            #         )
+            #     )
+
+            # def on_button_clicked(b):
+            #     if output.layout.display == "none":
+            #         output.layout.display = "block"
+            #     else:
+            #         output.layout.display = "none"
 
-        if self.figures:
-            plot_figures(html, self.figures)
+            # view_raw_data_button.on_click(on_button_clicked)
 
-        html.write(
-            """
-        </div>
+            # vbox_children.append(view_raw_data_button)
+            # vbox_children.append(output)
+
+        if self.figures:
+            vbox_children.append(widgets.HTML(value="<h3>Plots</h3>"))
+            plot_widgets = plot_figures(self.figures)
+            vbox_children.append(plot_widgets)
+
+        vbox_children.append(
+            widgets.HTML(
+                value="""
         <style>
             .metric-result {
                 background-color: #F5F5F5;
                 border: 1px solid #e0e0e0;
                 border-radius: 4px;
                 padding: 10px;
                 margin: 10px 0;
@@ -276,27 +271,20 @@
                 font-weight: 600;
             }
             .metric-value-value {
                 font-size: 14px;
                 font-weight: 500;
                 margin-top: 10px;
             }
-            .metric-plot img {
-                margin-left: auto !important;
-                margin-right: auto !important;
-                max-height: 500px !important;
-                height: 100%;
-                width: auto;
-                max-width: 800px;
-            }
         </style>
         """
+            )
         )
 
-        return html.getvalue()
+        return widgets.VBox(vbox_children)
 
     def log(self):
         if self.metric:
             log_metrics([self.metric])
         if self.figures:
             for fig in self.figures:
                 log_figure(fig.figure, fig.key, fig.metadata)
@@ -307,19 +295,20 @@
 
 @dataclass
 class TestPlanModelResult(TestPlanResult):
     """
     Result wrapper for models that run as part of a test plan
     """
 
+    name: str = "Metric"
     model: Model = None
 
-    def _to_html(self):
-        return f"""
-        <h4>Logged the following model to the ValidMind platform:</h4>
+    def _to_widget(self):
+        return widgets.HTML(
+            value=f"""
         <div class="model-result">
             <div class="model-result-header">
                 <div class="model-result-header-title">
                     <span class="model-result-header-title-text">
                         {self.model.model.__class__.__name__} ({self.model.model_id})
                     </span>
                     <span class="model-result-header-title-icon">📦</span>
@@ -379,25 +368,27 @@
                 padding: 5px;
             }}
             .model-body-column-title {{
                 font-weight: bold;
             }}
         </style>
         """
+        )
 
     def log(self):
         log_model(self.model)
 
 
 @dataclass
 class TestPlanTestResult(TestPlanResult):
     """
     Result wrapper for test results produced by the tests that run as part of a test plan
     """
 
+    name: str = "Threshold Test"
     figures: Optional[List[Figure]] = None
     test_results: TestResults = None
 
     def __repr__(self) -> str:
         if self.test_results:
             return (
                 f'{self.__class__.__name__}(result_id="{self.result_id}", test_results)'
@@ -409,19 +400,19 @@
         if self.test_results:
             return (
                 f'{self.__class__.__name__}(result_id="{self.result_id}", test_results)'
             )
         else:
             return f'{self.__class__.__name__}(result_id="{self.result_id}", figures)'
 
-    def _to_html(self):
-        html = StringIO()
-        html.write(
-            f"""
-        <h4>Logged the following test result to the ValidMind platform:</h4>
+    def _to_widget(self):
+        vbox_children = []
+        vbox_children.append(
+            widgets.HTML(
+                value=f"""
         <div class="metric-result">
             <div class="metric-result-body">
                 <div class="test-result-header-title">
                     <span class="test-result-header-title-text">
                         {" ".join(self.test_results.test_name.split("_")).title()}
                     </span>
                     <span class="test-result-header-title-icon">
@@ -452,25 +443,27 @@
                 <div class="results-objs-body">{self.test_results.results}</div>
             </div>
             <div class="metric-result-body">
                 <a onclick="toggleTestResults(this)" style="margin-top: 10px; cursor: pointer; color: blue;">
                     See Result Details
                 </a>
             </div>
-            <div class="metric-result-body">
+        </div>
         """
+            )
         )
 
         if self.figures:
-            plot_figures(html, self.figures)
-
-        html.write(
-            """
-            </div>
-        </div>
+            vbox_children.append(widgets.HTML(value="<h3>Plots</h3>"))
+            plot_widgets = plot_figures(self.figures)
+            vbox_children.append(plot_widgets)
+
+        vbox_children.append(
+            widgets.HTML(
+                value="""
         <style>
             .metric-result {
                 background-color: #F5F5F5;
                 border: 1px solid #e0e0e0;
                 border-radius: 4px;
                 padding: 10px;
                 margin: 10px 0;
@@ -502,22 +495,14 @@
                 font-weight: 600;
             }
             .metric-value-value {
                 font-size: 14px;
                 font-weight: 500;
                 margin-top: 10px;
             }
-            .metric-plot img {
-                margin-left: auto !important;
-                margin-right: auto !important;
-                max-height: 500px !important;
-                height: 100%;
-                width: auto;
-                max-width: 800px;
-            }
             .test-result {
                 border: 1px solid #ccc;
                 border-radius: 5px;
                 margin-bottom: 10px;
             }
             .test-result-header {
                 display: flex;
@@ -556,17 +541,18 @@
                 }} else {{
                     rslts.style.display = 'none';
                     btn.innerHTML = 'See Result Details';
                 }}
             }}
         </script>
         """
+            )
         )
 
-        return html.getvalue()
+        return widgets.VBox(vbox_children)
 
     def log(self):
         log_test_result(self.test_results)
         if self.figures:
             for fig in self.figures:
                 log_figure(fig.figure, fig.key, fig.metadata)
         if hasattr(self, "result_metadata") and self.result_metadata:
```

### Comparing `validmind-1.9.0/validmind/vm_models/test_result.py` & `validmind-1.9.1/validmind/vm_models/test_result.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.0/validmind/vm_models/test_suite.py` & `validmind-1.9.1/validmind/vm_models/test_suite.py`

 * *Files 2% similar despite different names*

```diff
@@ -94,14 +94,15 @@
                 pbar_description=self.pbar_description,
                 pbar_box=self.pbar_box,
             )
             test_plan_instance.run(render_summary=False, send=send)
             self._test_plan_instances.append(test_plan_instance)
 
         self.summarize()
+        self.pbar_description.value = "Test suite complete!"
 
     def _results_title(self) -> str:
         """
         Builds the title for the results of the test plan
         """
         return f'<h2>Test Suite Results: <i style="color: #DE257E">{self.title()}</i></h2><hr>'
```

### Comparing `validmind-1.9.0/validmind/vm_models/threshold_test.py` & `validmind-1.9.1/validmind/vm_models/threshold_test.py`

 * *Files 3% similar despite different names*

```diff
@@ -33,15 +33,15 @@
     test_type: ClassVar[str] = "ThresholdTest"
     category: ClassVar[str] = ""
     name: ClassVar[str] = ""
     default_params: ClassVar[dict] = {}
 
     # Instance Variables
     params: dict = None
-    test_results: TestResults = None
+    result: TestResults = None
 
     def __post_init__(self):
         """
         Set default params if not provided
         """
         if self.params is None:
             self.params = self.default_params
@@ -51,15 +51,15 @@
     def description(self):
         """
         Return the test description. Should be overridden by subclasses. Defaults
         to returning the class' docstring
         """
         return self.__doc__.strip()
 
-    def summary(self, test_results: Optional[TestResults] = None):
+    def summary(self, result: Optional[TestResults] = None):
         """
         Return the threshold test summary. Should be overridden by subclasses. Defaults to None.
         The test summary allows renderers (e.g. Word and ValidMind UI) to display a
         short summary of the test results.
 
         We return None here because the test summary is optional.
         """
@@ -69,50 +69,50 @@
         """
         Run the test and cache its results
         """
         raise NotImplementedError
 
     def cache_results(
         self,
-        results: List[TestResult],
+        test_results_list: List[TestResult],
         passed: bool,
         figures: Optional[List[Figure]] = None,
     ):
         """
         Cache the individual results of the threshold test as a list of TestResult objects
 
         Args:
-            results (List[TestResult]): The results of the threshold test
+            result (List[TestResult]): The results of the threshold test
             passed (bool): Whether the threshold test passed or failed
 
         Returns:
             TestPlanResult: The test plan result object
         """
         # Rename to self.result
         # At a minimum, send the test description
         result_metadata = [
             {
                 "content_id": f"test_description:{self.name}",
                 "text": clean_docstring(self.description()),
             }
         ]
 
-        result_summary = self.summary(results)
+        result_summary = self.summary(test_results_list)
 
-        self.test_results = TestPlanTestResult(
+        self.result = TestPlanTestResult(
             result_id=self.name,
             result_metadata=result_metadata,
             test_results=TestResults(
                 category=self.category,
                 test_name=self.name,
                 params=self.params,
                 passed=passed,
-                results=results,
+                results=test_results_list,
                 summary=result_summary,
             ),
         )
 
         # Allow test results to attach figures to the test plan result
         if figures:
-            self.test_results.figures = figures
+            self.result.figures = figures
 
-        return self.test_results
+        return self.result
```

### Comparing `validmind-1.9.0/PKG-INFO` & `validmind-1.9.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: validmind
-Version: 1.9.0
+Version: 1.9.1
 Summary: ValidMind Developer Framework
 Author: Andres Rodriguez
 Author-email: andres@validmind.ai
 Requires-Python: >=3.8,<3.11
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

