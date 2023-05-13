# Comparing `tmp/validmind-1.9.2.tar.gz` & `tmp/validmind-1.9.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "validmind-1.9.2.tar", max compression
+gzip compressed data, was "validmind-1.9.3.tar", max compression
```

## Comparing `validmind-1.9.2.tar` & `validmind-1.9.3.tar`

### file list

```diff
@@ -1,62 +1,62 @@
--rw-r--r--   0        0        0     1295 2023-05-13 08:42:30.626940 validmind-1.9.2/pyproject.toml
--rw-r--r--   0        0        0     1443 2023-05-13 08:42:30.626940 validmind-1.9.2/validmind/__init__.py
--rw-r--r--   0        0        0    11353 2023-05-13 08:42:30.626940 validmind-1.9.2/validmind/api_client.py
--rw-r--r--   0        0        0     9190 2023-05-13 08:42:30.626940 validmind-1.9.2/validmind/client.py
--rw-r--r--   0        0        0      590 2023-05-13 08:42:30.626940 validmind-1.9.2/validmind/data_validation/__init__.py
--rw-r--r--   0        0        0    36506 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/data_validation/metrics.py
--rw-r--r--   0        0        0    24265 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/data_validation/threshold_tests.py
--rw-r--r--   0        0        0        0 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/datasets/__init__.py
--rw-r--r--   0        0        0     1539 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/datasets/classification/__init__.py
--rw-r--r--   0        0        0     1330 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/datasets/classification/customer_churn.py
--rw-r--r--   0        0        0   545707 2023-05-13 08:42:30.630940 validmind-1.9.2/validmind/datasets/classification/datasets/bank_customer_churn.csv
--rw-r--r--   0        0        0  2897191 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/classification/datasets/taiwan_credit.csv
--rw-r--r--   0        0        0     1280 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/classification/taiwan_credit.py
--rw-r--r--   0        0        0     1416 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/__init__.py
--rw-r--r--   0        0        0   107835 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates.csv
--rw-r--r--   0        0        0     2634 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv
--rw-r--r--   0        0        0     2634 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv
--rw-r--r--   0        0        0     2736 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv
--rw-r--r--   0        0        0     3355 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv
--rw-r--r--   0        0        0     3866 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv
--rw-r--r--   0        0        0    11624 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/datasets/lending_club_loan_rates.csv
--rw-r--r--   0        0        0     4378 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/fred.py
--rw-r--r--   0        0        0     2346 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/lending_club.py
--rw-r--r--   0        0        0    40067 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl
--rw-r--r--   0        0        0    48314 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl
--rw-r--r--   0        0        0    40063 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl
--rw-r--r--   0        0        0    48292 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl
--rw-r--r--   0        0        0    60343 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl
--rw-r--r--   0        0        0    10529 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_utils.py
--rw-r--r--   0        0        0     1290 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/__init__.py
--rw-r--r--   0        0        0     6712 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/model_metadata.py
--rw-r--r--   0        0        0        0 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/sklearn/__init__.py
--rw-r--r--   0        0        0    13048 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/sklearn/metrics.py
--rw-r--r--   0        0        0    31402 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/sklearn/threshold_tests.py
--rw-r--r--   0        0        0        0 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/statsmodels/__init__.py
--rw-r--r--   0        0        0    26596 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/statsmodels/metrics.py
--rw-r--r--   0        0        0     1317 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/statsmodels/threshold_tests.py
--rw-r--r--   0        0        0     1657 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/model_validation/utils.py
--rw-r--r--   0        0        0     5182 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/__init__.py
--rw-r--r--   0        0        0     2016 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/binary_classifier.py
--rw-r--r--   0        0        0     2836 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/statsmodels_timeseries.py
--rw-r--r--   0        0        0     1604 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/tabular_datasets.py
--rw-r--r--   0        0        0     6821 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_plans/time_series.py
--rw-r--r--   0        0        0     1894 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_suites/__init__.py
--rw-r--r--   0        0        0     1415 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/test_suites/test_suites.py
--rw-r--r--   0        0        0     6465 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/utils.py
--rw-r--r--   0        0        0     1116 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/__init__.py
--rw-r--r--   0        0        0    10425 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/dataset.py
--rw-r--r--   0        0        0     8287 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/dataset_utils.py
--rw-r--r--   0        0        0      592 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/figure.py
--rw-r--r--   0        0        0     3746 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/metric.py
--rw-r--r--   0        0        0     1757 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/metric_result.py
--rw-r--r--   0        0        0     6530 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/model.py
--rw-r--r--   0        0        0     3721 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/plot_utils.py
--rw-r--r--   0        0        0     1518 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/result_summary.py
--rw-r--r--   0        0        0     2501 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_context.py
--rw-r--r--   0        0        0    11803 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_plan.py
--rw-r--r--   0        0        0    18529 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_plan_result.py
--rw-r--r--   0        0        0     1698 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_result.py
--rw-r--r--   0        0        0     5019 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/test_suite.py
--rw-r--r--   0        0        0     3620 2023-05-13 08:42:30.650940 validmind-1.9.2/validmind/vm_models/threshold_test.py
--rw-r--r--   0        0        0     1385 1970-01-01 00:00:00.000000 validmind-1.9.2/PKG-INFO
+-rw-r--r--   0        0        0     1295 2023-05-13 15:54:34.670003 validmind-1.9.3/pyproject.toml
+-rw-r--r--   0        0        0     1443 2023-05-13 15:54:34.670003 validmind-1.9.3/validmind/__init__.py
+-rw-r--r--   0        0        0    11353 2023-05-13 15:54:34.670003 validmind-1.9.3/validmind/api_client.py
+-rw-r--r--   0        0        0     9190 2023-05-13 15:54:34.670003 validmind-1.9.3/validmind/client.py
+-rw-r--r--   0        0        0      590 2023-05-13 15:54:34.670003 validmind-1.9.3/validmind/data_validation/__init__.py
+-rw-r--r--   0        0        0    41101 2023-05-13 15:54:34.674003 validmind-1.9.3/validmind/data_validation/metrics.py
+-rw-r--r--   0        0        0    24265 2023-05-13 15:54:34.674003 validmind-1.9.3/validmind/data_validation/threshold_tests.py
+-rw-r--r--   0        0        0        0 2023-05-13 15:54:34.674003 validmind-1.9.3/validmind/datasets/__init__.py
+-rw-r--r--   0        0        0     1539 2023-05-13 15:54:34.674003 validmind-1.9.3/validmind/datasets/classification/__init__.py
+-rw-r--r--   0        0        0     1330 2023-05-13 15:54:34.674003 validmind-1.9.3/validmind/datasets/classification/customer_churn.py
+-rw-r--r--   0        0        0   545707 2023-05-13 15:54:34.674003 validmind-1.9.3/validmind/datasets/classification/datasets/bank_customer_churn.csv
+-rw-r--r--   0        0        0  2897191 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/classification/datasets/taiwan_credit.csv
+-rw-r--r--   0        0        0     1280 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/classification/taiwan_credit.py
+-rw-r--r--   0        0        0     1416 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/__init__.py
+-rw-r--r--   0        0        0   107835 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates.csv
+-rw-r--r--   0        0        0     2634 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv
+-rw-r--r--   0        0        0     2634 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv
+-rw-r--r--   0        0        0     2736 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv
+-rw-r--r--   0        0        0     3355 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv
+-rw-r--r--   0        0        0     3866 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv
+-rw-r--r--   0        0        0    11624 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/datasets/lending_club_loan_rates.csv
+-rw-r--r--   0        0        0     4378 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/fred.py
+-rw-r--r--   0        0        0     2346 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/lending_club.py
+-rw-r--r--   0        0        0    40067 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl
+-rw-r--r--   0        0        0    48314 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl
+-rw-r--r--   0        0        0    40063 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl
+-rw-r--r--   0        0        0    48292 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl
+-rw-r--r--   0        0        0    60343 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl
+-rw-r--r--   0        0        0    10529 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_utils.py
+-rw-r--r--   0        0        0     1290 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/__init__.py
+-rw-r--r--   0        0        0     6712 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/model_metadata.py
+-rw-r--r--   0        0        0        0 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/sklearn/__init__.py
+-rw-r--r--   0        0        0    13048 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/sklearn/metrics.py
+-rw-r--r--   0        0        0    31402 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/sklearn/threshold_tests.py
+-rw-r--r--   0        0        0        0 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/statsmodels/__init__.py
+-rw-r--r--   0        0        0    28873 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/statsmodels/metrics.py
+-rw-r--r--   0        0        0     1317 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/statsmodels/threshold_tests.py
+-rw-r--r--   0        0        0     1657 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/model_validation/utils.py
+-rw-r--r--   0        0        0     4788 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/test_plans/__init__.py
+-rw-r--r--   0        0        0     2016 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/test_plans/binary_classifier.py
+-rw-r--r--   0        0        0      811 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/test_plans/statsmodels_timeseries.py
+-rw-r--r--   0        0        0     1604 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/test_plans/tabular_datasets.py
+-rw-r--r--   0        0        0     3711 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/test_plans/time_series.py
+-rw-r--r--   0        0        0     1988 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/test_suites/__init__.py
+-rw-r--r--   0        0        0     1750 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/test_suites/test_suites.py
+-rw-r--r--   0        0        0     6465 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/utils.py
+-rw-r--r--   0        0        0     1116 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/__init__.py
+-rw-r--r--   0        0        0    10713 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/dataset.py
+-rw-r--r--   0        0        0     8287 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/dataset_utils.py
+-rw-r--r--   0        0        0      592 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/figure.py
+-rw-r--r--   0        0        0     3746 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/metric.py
+-rw-r--r--   0        0        0     1757 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/metric_result.py
+-rw-r--r--   0        0        0     6530 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/model.py
+-rw-r--r--   0        0        0     3721 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/plot_utils.py
+-rw-r--r--   0        0        0     1518 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/result_summary.py
+-rw-r--r--   0        0        0     2501 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/test_context.py
+-rw-r--r--   0        0        0    11803 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/test_plan.py
+-rw-r--r--   0        0        0    18529 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/test_plan_result.py
+-rw-r--r--   0        0        0     1698 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/test_result.py
+-rw-r--r--   0        0        0     5019 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/test_suite.py
+-rw-r--r--   0        0        0     3620 2023-05-13 15:54:34.694003 validmind-1.9.3/validmind/vm_models/threshold_test.py
+-rw-r--r--   0        0        0     1385 1970-01-01 00:00:00.000000 validmind-1.9.3/PKG-INFO
```

### Comparing `validmind-1.9.2/pyproject.toml` & `validmind-1.9.3/pyproject.toml`

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
-version = "1.9.2"
+version = "1.9.3"
 
 [tool.poetry.dependencies]
 arch = "^5.4.0"
 click = "^8.0.4"
 dython = "^0.7.1"
 ipython = "^8.11.0"
 myst-parser = "^1.0.0"
```

### Comparing `validmind-1.9.2/validmind/__init__.py` & `validmind-1.9.3/validmind/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/api_client.py` & `validmind-1.9.3/validmind/api_client.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/client.py` & `validmind-1.9.3/validmind/client.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/data_validation/__init__.py` & `validmind-1.9.3/validmind/data_validation/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/data_validation/metrics.py` & `validmind-1.9.3/validmind/data_validation/metrics.py`

 * *Files 4% similar despite different names*

```diff
@@ -496,113 +496,151 @@
 
 
 class AutoAR(Metric):
     """
     Automatically detects the AR order of a time series using both BIC and AIC.
     """
 
+    type = "dataset"
     name = "auto_ar"
     required_context = ["dataset"]
     default_params = {"max_ar_order": 3}
 
     def run(self):
         if "max_ar_order" not in self.params:
             raise ValueError("max_ar_order must be provided in params")
 
         max_ar_order = self.params["max_ar_order"]
 
         df = self.dataset.df
 
-        results = []
+        # Create an empty DataFrame to store the results
+        summary_ar_analysis = pd.DataFrame()
 
         for col in df.columns:
             series = df[col].dropna()
 
             # Check for stationarity using the Augmented Dickey-Fuller test
             adf_test = adfuller(series)
             if adf_test[1] > 0.05:
                 print(f"Warning: {col} is not stationary. Results may be inaccurate.")
 
-            ar_orders = []
-            bic_values = []
-            aic_values = []
-
             for ar_order in range(0, max_ar_order + 1):
                 try:
                     model = AutoReg(series, lags=ar_order, old_names=False)
                     model_fit = model.fit()
 
-                    ar_orders.append(ar_order)
-                    bic_values.append(model_fit.bic)
-                    aic_values.append(model_fit.aic)
+                    # Append the result of each AR order directly into the DataFrame
+                    summary_ar_analysis = summary_ar_analysis.append(
+                        {
+                            "Variable": col,
+                            "AR Order": ar_order,
+                            "BIC": model_fit.bic,
+                            "AIC": model_fit.aic,
+                        },
+                        ignore_index=True,
+                    )
                 except Exception as e:
                     print(f"Error fitting AR({ar_order}) model for {col}: {e}")
 
-            result = {
-                "Variable": col,
-                "AR orders": ar_orders,
-                "BIC": bic_values,
-                "AIC": aic_values,
+        # Convert the 'AR Order' column to integer
+        summary_ar_analysis["AR Order"] = summary_ar_analysis["AR Order"].astype(int)
+
+        return self.cache_results(
+            {
+                "auto_ar_analysis": summary_ar_analysis.to_dict(orient="records"),
             }
-            results.append(result)
+        )
+
+    def summary(self, metric_value):
+        """
+        Build one table for summarizing the auto AR results
+        """
+        summary_ar_analysis = metric_value["auto_ar_analysis"]
 
-        return self.cache_results(results)
+        return ResultSummary(
+            results=[
+                ResultTable(
+                    data=summary_ar_analysis,
+                    metadata=ResultTableMetadata(title="Auto AR Analysis Results"),
+                ),
+            ]
+        )
 
 
 class AutoMA(Metric):
     """
     Automatically detects the MA order of a time series using both BIC and AIC.
     """
 
+    type = "dataset"
     name = "auto_ma"
     required_context = ["dataset"]
     default_params = {"max_ma_order": 3}
 
     def run(self):
         if "max_ma_order" not in self.params:
             raise ValueError("max_ma_order must be provided in params")
 
         max_ma_order = self.params["max_ma_order"]
 
         df = self.dataset.df
 
-        results = []
+        # Create an empty DataFrame to store the results
+        summary_ma_analysis = pd.DataFrame()
 
         for col in df.columns:
             series = df[col].dropna()
 
             # Check for stationarity using the Augmented Dickey-Fuller test
             adf_test = adfuller(series)
             if adf_test[1] > 0.05:
                 print(f"Warning: {col} is not stationary. Results may be inaccurate.")
 
-            ma_orders = []
-            bic_values = []
-            aic_values = []
-
             for ma_order in range(0, max_ma_order + 1):
                 try:
                     model = ARIMA(series, order=(0, 0, ma_order))
                     model_fit = model.fit()
 
-                    ma_orders.append(ma_order)
-                    bic_values.append(model_fit.bic)
-                    aic_values.append(model_fit.aic)
+                    # Append the result of each MA order directly into the DataFrame
+                    summary_ma_analysis = summary_ma_analysis.append(
+                        {
+                            "Variable": col,
+                            "MA Order": ma_order,
+                            "BIC": model_fit.bic,
+                            "AIC": model_fit.aic,
+                        },
+                        ignore_index=True,
+                    )
                 except Exception as e:
                     print(f"Error fitting MA({ma_order}) model for {col}: {e}")
 
-            result = {
-                "Variable": col,
-                "MA orders": ma_orders,
-                "BIC": bic_values,
-                "AIC": aic_values,
+        # Convert the 'MA Order' column to integer
+        summary_ma_analysis["MA Order"] = summary_ma_analysis["MA Order"].astype(int)
+
+        return self.cache_results(
+            {
+                "auto_ma_analysis": summary_ma_analysis.to_dict(orient="records"),
             }
-            results.append(result)
+        )
+
+    def summary(self, metric_value):
+        """
+        Build one table for summarizing the auto MA results
+        """
+        summary_ma_analysis = metric_value["auto_ma_analysis"]
 
-        return self.cache_results(results)
+        return ResultSummary(
+            results=[
+                ResultTable(
+                    data=summary_ma_analysis,
+                    metadata=ResultTableMetadata(title="Auto MA Analysis Results"),
+                ),
+            ]
+        )
 
 
 class SeasonalDecompose(Metric):
     """
     Calculates seasonal_decompose metric for each of the dataset features
     """
 
@@ -777,35 +815,61 @@
 
         if "max_period" not in self.params:
             raise ValueError("max_period must be provided in params")
         max_period = self.params["max_period"]
 
         df = self.dataset.df
 
-        results = []
+        # Create an empty DataFrame to store the results
+        summary_auto_seasonality = pd.DataFrame()
 
         for col_name, col in df.iteritems():
             series = col.dropna()
+
+            # Directly insert the results into the DataFrame
             seasonal_periods, residual_errors = self.evaluate_seasonal_periods(
                 series, min_period, max_period
             )
-
             best_seasonal_period = seasonal_periods[np.argmin(residual_errors)]
-            decision = "Seasonality" if best_seasonal_period > 1 else "Not Seasonality"
+            decision = "Seasonality" if best_seasonal_period > 1 else "No Seasonality"
 
-            result = {
-                "Variable": col_name,
-                "Seasonal Periods": seasonal_periods,
-                "Residual Errors": residual_errors,
-                "Best Period": best_seasonal_period,
-                "Decision": decision,
+            summary_auto_seasonality = summary_auto_seasonality.append(
+                {
+                    "Variable": col_name,
+                    "Tested Seasonal Periods": seasonal_periods,
+                    "Best Period": best_seasonal_period,
+                    "Decision": decision,
+                },
+                ignore_index=True,
+            )
+            # Convert the 'Best Period' column to integer
+            summary_auto_seasonality["Best Period"] = summary_auto_seasonality[
+                "Best Period"
+            ].astype(int)
+
+        return self.cache_results(
+            {
+                "auto_seasonality": summary_auto_seasonality.to_dict(orient="records"),
             }
-            results.append(result)
+        )
 
-        return self.cache_results(results)
+    def summary(self, metric_value):
+        """
+        Build one table for summarizing the auto seasonality results
+        """
+        summary_auto_seasonality = metric_value["auto_seasonality"]
+
+        return ResultSummary(
+            results=[
+                ResultTable(
+                    data=summary_auto_seasonality,
+                    metadata=ResultTableMetadata(title="Auto Seasonality Results"),
+                ),
+            ]
+        )
 
 
 class ACFandPACFPlot(Metric):
     """
     Plots ACF and PACF for a given time series dataset.
     """
 
@@ -857,29 +921,31 @@
 class AutoStationarity(Metric):
     """
     Automatically detects stationarity for each time series in a DataFrame
     using the Augmented Dickey-Fuller (ADF) test.
     """
 
     type = "dataset"
-    key = "auto_stationarity"
+    name = "auto_stationarity"
     required_context = ["dataset"]
     default_params = {"max_order": 5, "threshold": 0.05}
 
     def run(self):
         if "max_order" not in self.params:
             raise ValueError("max_order must be provided in params")
         max_order = self.params["max_order"]
 
         if "threshold" not in self.params:
             raise ValueError("threshold must be provided in params")
         threshold = self.params["threshold"]
 
         df = self.dataset.df.dropna()
-        results = []
+
+        # Create an empty DataFrame to store the results
+        summary_stationarity = pd.DataFrame()
 
         # Loop over each column in the input DataFrame and perform stationarity tests
         for col in df.columns:
             is_stationary = False
             order = 0
 
             while not is_stationary and order <= max_order:
@@ -890,31 +956,58 @@
                 else:
                     adf_result = adfuller(np.diff(series, n=order - 1))
 
                 adf_pvalue = adf_result[1]
                 adf_pass_fail = adf_pvalue < threshold
                 adf_decision = "Stationary" if adf_pass_fail else "Non-stationary"
 
-                result = {
-                    "Variable": col,
-                    "Integration Order": order,
-                    "Test": "ADF",
-                    "p-value": adf_pvalue,
-                    "Threshold": threshold,
-                    "Pass/Fail": "Pass" if adf_pass_fail else "Fail",
-                    "Decision": adf_decision,
-                }
-                results.append(result)
+                # Append the result of each test directly into the DataFrame
+                summary_stationarity = summary_stationarity.append(
+                    {
+                        "Variable": col,
+                        "Integration Order": order,
+                        "Test": "ADF",
+                        "p-value": adf_pvalue,
+                        "Threshold": threshold,
+                        "Pass/Fail": "Pass" if adf_pass_fail else "Fail",
+                        "Decision": adf_decision,
+                    },
+                    ignore_index=True,
+                )
 
                 if adf_pass_fail:
                     is_stationary = True
 
                 order += 1
 
-        return self.cache_results(results)
+        # Convert the 'Integration Order' column to integer
+        summary_stationarity["Integration Order"] = summary_stationarity[
+            "Integration Order"
+        ].astype(int)
+
+        return self.cache_results(
+            {
+                "stationarity_analysis": summary_stationarity.to_dict(orient="records"),
+            }
+        )
+
+    def summary(self, metric_value):
+        """
+        Build one table for summarizing the stationarity results
+        """
+        summary_stationarity = metric_value["stationarity_analysis"]
+
+        return ResultSummary(
+            results=[
+                ResultTable(
+                    data=summary_stationarity,
+                    metadata=ResultTableMetadata(title="Stationarity Analysis Results"),
+                ),
+            ]
+        )
 
 
 class RollingStatsPlot(Metric):
     """
     This class provides a metric to visualize the stationarity of a given time series dataset by plotting the rolling mean and rolling standard deviation. The rolling mean represents the average of the time series data over a fixed-size sliding window, which helps in identifying trends in the data. The rolling standard deviation measures the variability of the data within the sliding window, showing any changes in volatility over time. By analyzing these plots, users can gain insights into the stationarity of the time series data and determine if any transformations or differencing operations are required before applying time series models.
     """
 
@@ -987,23 +1080,26 @@
 
 
 class EngleGrangerCoint(Metric):
     """
     Test for cointegration between pairs of time series variables in a given dataset using the Engle-Granger test.
     """
 
+    type = "dataset"
     name = "engle_granger_coint"
     required_context = ["dataset"]
     default_params = {"threshold": 0.05}
 
     def run(self):
         threshold = self.params["threshold"]
         df = self.dataset.df.dropna()
 
-        results = []
+        # Create an empty DataFrame to store the results
+        summary_cointegration = pd.DataFrame()
+
         columns = df.columns
         num_vars = len(columns)
 
         for i in range(num_vars):
             for j in range(i + 1, num_vars):
                 var1 = columns[i]
                 var2 = columns[j]
@@ -1013,26 +1109,52 @@
 
                 # Determine the decision based on the p-value and the significance level
                 decision = (
                     "Cointegrated" if p_value <= threshold else "Not cointegrated"
                 )
                 pass_fail = "Pass" if p_value <= threshold else "Fail"
 
-                result = {
-                    "Variable 1": var1,
-                    "Variable 2": var2,
-                    "Test": "Engle-Granger",
-                    "p-value": p_value,
-                    "Threshold": threshold,
-                    "Pass/Fail": pass_fail,
-                    "Decision": decision,
-                }
-                results.append(result)
+                # Append the result of each test directly into the DataFrame
+                summary_cointegration = summary_cointegration.append(
+                    {
+                        "Variable 1": var1,
+                        "Variable 2": var2,
+                        "Test": "Engle-Granger",
+                        "p-value": p_value,
+                        "Threshold": threshold,
+                        "Pass/Fail": pass_fail,
+                        "Decision": decision,
+                    },
+                    ignore_index=True,
+                )
 
-        return self.cache_results(results)
+        return self.cache_results(
+            {
+                "cointegration_analysis": summary_cointegration.to_dict(
+                    orient="records"
+                ),
+            }
+        )
+
+    def summary(self, metric_value):
+        """
+        Build one table for summarizing the cointegration results
+        """
+        summary_cointegration = metric_value["cointegration_analysis"]
+
+        return ResultSummary(
+            results=[
+                ResultTable(
+                    data=summary_cointegration,
+                    metadata=ResultTableMetadata(
+                        title="Cointegration Analysis Results"
+                    ),
+                ),
+            ]
+        )
 
 
 class SpreadPlot(Metric):
     """
     This class provides a metric to visualize the spread between pairs of time series variables in a given dataset. By plotting the spread of each pair of variables in separate figures, users can assess the relationship between the variables and determine if any cointegration or other time series relationships exist between them.
     """
```

### Comparing `validmind-1.9.2/validmind/data_validation/threshold_tests.py` & `validmind-1.9.3/validmind/data_validation/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/classification/__init__.py` & `validmind-1.9.3/validmind/datasets/classification/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/classification/customer_churn.py` & `validmind-1.9.3/validmind/datasets/classification/customer_churn.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/classification/datasets/bank_customer_churn.csv` & `validmind-1.9.3/validmind/datasets/classification/datasets/bank_customer_churn.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/classification/datasets/taiwan_credit.csv` & `validmind-1.9.3/validmind/datasets/classification/datasets/taiwan_credit.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/classification/taiwan_credit.py` & `validmind-1.9.3/validmind/datasets/classification/taiwan_credit.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/__init__.py` & `validmind-1.9.3/validmind/datasets/regression/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates.csv` & `validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv` & `validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_1.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv` & `validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_2.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv` & `validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_3.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv` & `validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_4.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv` & `validmind-1.9.3/validmind/datasets/regression/datasets/fred_loan_rates_test_5.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/datasets/lending_club_loan_rates.csv` & `validmind-1.9.3/validmind/datasets/regression/datasets/lending_club_loan_rates.csv`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/fred.py` & `validmind-1.9.3/validmind/datasets/regression/fred.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/lending_club.py` & `validmind-1.9.3/validmind/datasets/regression/lending_club.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl` & `validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_1.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl` & `validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_2.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl` & `validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_3.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl` & `validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_4.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl` & `validmind-1.9.3/validmind/datasets/regression/models/fred_loan_rates_model_5.pkl`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/model_utils.py` & `validmind-1.9.3/validmind/model_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/model_validation/__init__.py` & `validmind-1.9.3/validmind/model_validation/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/model_validation/model_metadata.py` & `validmind-1.9.3/validmind/model_validation/model_metadata.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/model_validation/sklearn/metrics.py` & `validmind-1.9.3/validmind/model_validation/sklearn/metrics.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/model_validation/sklearn/threshold_tests.py` & `validmind-1.9.3/validmind/model_validation/sklearn/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/model_validation/statsmodels/metrics.py` & `validmind-1.9.3/validmind/model_validation/statsmodels/metrics.py`

 * *Files 4% similar despite different names*

```diff
@@ -18,15 +18,21 @@
 from statsmodels.stats.diagnostic import kstest_normal
 from statsmodels.stats.diagnostic import lilliefors
 from statsmodels.stats.stattools import jarque_bera
 from statsmodels.graphics.tsaplots import plot_acf
 from arch.unitroot import PhillipsPerron
 from arch.unitroot import ZivotAndrews
 from arch.unitroot import DFGLS
-from ...vm_models import Figure, Metric
+from ...vm_models import (
+    Figure,
+    Metric,
+    ResultSummary,
+    ResultTable,
+    ResultTableMetadata,
+)
 
 
 @dataclass
 class ResidualsVisualInspection(Metric):
     """
     Log plots for visual inspection of residuals
     """
@@ -572,22 +578,45 @@
         r2 = lib_model.rsquared
         adj_r2 = lib_model.rsquared_adj
 
         # Calculate the Mean Squared Error (MSE) and Root Mean Squared Error (RMSE)
         mse = lib_model.mse_resid
         rmse = mse**0.5
 
-        results = {
-            "Independent Variables": X_columns,
-            "R-Squared": r2,
-            "Adjusted R-Squared": adj_r2,
-            "MSE": mse,
-            "RMSE": rmse,
-        }
-        return self.cache_results(results)
+        # Create a DataFrame for the results
+        summary_regression = pd.DataFrame(
+            {
+                "Independent Variables": [X_columns],
+                "R-Squared": [r2],
+                "Adjusted R-Squared": [adj_r2],
+                "MSE": [mse],
+                "RMSE": [rmse],
+            }
+        )
+
+        return self.cache_results(
+            {
+                "regression_analysis": summary_regression.to_dict(orient="records"),
+            }
+        )
+
+    def summary(self, metric_value):
+        """
+        Build one table for summarizing the regression analysis results
+        """
+        summary_regression = metric_value["regression_analysis"]
+
+        return ResultSummary(
+            results=[
+                ResultTable(
+                    data=summary_regression,
+                    metadata=ResultTableMetadata(title="Regression Analysis Results"),
+                ),
+            ]
+        )
 
 
 @dataclass
 class RegressionModelInsampleComparison(Metric):
     """
     Test that output the comparison of stats library regression models.
     """
@@ -617,15 +646,21 @@
         for model in all_models:
             if model.model.__class__.__name__ != "RegressionResultsWrapper":
                 raise ValueError(
                     "Only RegressionResultsWrapper models of statsmodels library supported"
                 )
 
         results = self._in_sample_performance_ols(all_models)
-        return self.cache_results(results)
+        return self.cache_results(
+            {
+                "in_sample_performance": pd.DataFrame(results).to_dict(
+                    orient="records"
+                ),
+            }
+        )
 
     def _in_sample_performance_ols(self, models):
         """
         Computes the in-sample performance evaluation metrics for a list of OLS models.
 
         Args:
         models (list): A list of statsmodels OLS models.
@@ -662,14 +697,29 @@
                     "MSE": mse,
                     "RMSE": rmse,
                 }
             )
 
         return evaluation_results
 
+    def summary(self, metric_value):
+        """
+        Build one table for summarizing the in-sample performance results
+        """
+        summary_in_sample_performance = metric_value["in_sample_performance"]
+
+        return ResultSummary(
+            results=[
+                ResultTable(
+                    data=summary_in_sample_performance,
+                    metadata=ResultTableMetadata(title="In-Sample Performance Results"),
+                ),
+            ]
+        )
+
 
 @dataclass
 class RegressionModelOutsampleComparison(Metric):
     """
     Test that evaluates the performance of different regression models on a separate test dataset
     that was not used to train the models.
     """
@@ -705,15 +755,19 @@
                 raise ValueError(
                     "Test dataset is missing in the ValidMind Model object"
                 )
 
         results = self._out_sample_performance_ols(
             all_models,
         )
-        return self.cache_results(results.to_dict("records"))
+        return self.cache_results(
+            {
+                "out_sample_performance": results.to_dict(orient="records"),
+            }
+        )
 
     def _out_sample_performance_ols(self, model_list):
         """
         Returns the out-of-sample performance evaluation metrics of a list of OLS regression models.
 
         Args:
         model_list (list): A list of OLS models to evaluate.
@@ -744,21 +798,44 @@
 
             # Calculate the mean squared error and root mean squared error
             mse = np.mean(residuals**2)
             rmse_val = np.sqrt(mse)
 
             # Store the results
             model_name_with_vars = f"({', '.join(independent_vars)})"
-            results.append([model_name_with_vars, mse, rmse_val])
+            results.append(
+                {
+                    "Model": model_name_with_vars,
+                    "MSE": mse,
+                    "RMSE": rmse_val,
+                }
+            )
 
         # Create a DataFrame to display the results
-        results_df = pd.DataFrame(results, columns=["Model", "MSE", "RMSE"])
+        results_df = pd.DataFrame(results)
 
         return results_df
 
+    def summary(self, metric_value):
+        """
+        Build one table for summarizing the out-of-sample performance results
+        """
+        summary_out_sample_performance = metric_value["out_sample_performance"]
+
+        return ResultSummary(
+            results=[
+                ResultTable(
+                    data=summary_out_sample_performance,
+                    metadata=ResultTableMetadata(
+                        title="Out-of-Sample Performance Results"
+                    ),
+                ),
+            ]
+        )
+
 
 @dataclass
 class RegressionModelForecastPlot(Metric):
     """
     This metric creates a plot of forecast vs observed for each model in the list.
     """
 
@@ -767,21 +844,17 @@
 
     def description(self):
         return """
         This section shows plots of training and test datasets vs forecast trainining and forecast test.
         """
 
     def run(self):
-        print(self.params)
-
         start_date = self.params["start_date"]
         end_date = self.params["end_date"]
 
-        print(self.params)
-
         # Check models list is not empty
         if not self.models:
             raise ValueError("List of models must be provided in the models parameter")
         all_models = []
         for model in self.models:
             if model.model.__class__.__name__ != "RegressionResultsWrapper":
                 raise ValueError(
@@ -790,28 +863,35 @@
             all_models.append(model)
 
         figures = self._plot_forecast(all_models, start_date, end_date)
 
         return self.cache_results(figures=figures)
 
     def _plot_forecast(self, model_list, start_date=None, end_date=None):
-        # Convert start_date and end_date to pandas Timestamp for comparison
-        start_date = pd.Timestamp(start_date)
-        end_date = pd.Timestamp(end_date)
-
         # Initialize a list to store figures
         figures = []
 
         for fitted_model in model_list:
             train_ds = fitted_model.train_ds
             test_ds = fitted_model.test_ds
 
             # Check that start_date and end_date are within the data range
             all_dates = pd.concat([pd.Series(train_ds.index), pd.Series(test_ds.index)])
-            print(all_dates)
+
+            # If start_date or end_date are None, set them to the min/max of all_dates
+            if start_date is None:
+                start_date = all_dates.min()
+            else:
+                start_date = pd.Timestamp(start_date)
+
+            if end_date is None:
+                end_date = all_dates.max()
+            else:
+                end_date = pd.Timestamp(end_date)
+
             if start_date < all_dates.min() or end_date > all_dates.max():
                 raise ValueError(
                     "start_date and end_date must be within the range of dates in the data"
                 )
 
             fig, ax = plt.subplots()
             sns.lineplot(
```

### Comparing `validmind-1.9.2/validmind/model_validation/statsmodels/threshold_tests.py` & `validmind-1.9.3/validmind/model_validation/statsmodels/threshold_tests.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/model_validation/utils.py` & `validmind-1.9.3/validmind/model_validation/utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/test_plans/__init__.py` & `validmind-1.9.3/validmind/test_plans/__init__.py`

 * *Files 22% similar despite different names*

```diff
@@ -13,20 +13,14 @@
 )
 from .tabular_datasets import (
     TabularDataQuality,
     TabularDatasetDescription,
     TimeSeriesDataQuality,
 )
 from .statsmodels_timeseries import (
-    NormalityTestPlan,
-    AutocorrelationTestPlan,
-    SesonalityTestPlan,
-    UnitRoot,
-    StationarityTestPlan,
-    TimeSeries,
     RegressionModelPerformance,
     RegressionModelsComparison,
 )
 from .time_series import (
     TimeSeriesUnivariate,
     TimeSeriesMultivariate,
     TimeSeriesForecast,
@@ -34,20 +28,14 @@
 
 core_test_plans = {
     "binary_classifier_metrics": BinaryClassifierMetrics,
     "binary_classifier_validation": BinaryClassifierPerformance,
     "binary_classifier_model_diagnosis": BinaryClassifierDiagnosis,
     "tabular_dataset_description": TabularDatasetDescription,
     "tabular_data_quality": TabularDataQuality,
-    "normality_test_plan": NormalityTestPlan,
-    "autocorrelation_test_plan": AutocorrelationTestPlan,
-    "seasonality_test_plan": SesonalityTestPlan,
-    "unit_root": UnitRoot,
-    "stationarity_test_plan": StationarityTestPlan,
-    "timeseries": TimeSeries,
     "time_series_data_quality": TimeSeriesDataQuality,
     "time_series_univariate": TimeSeriesUnivariate,
     "time_series_multivariate": TimeSeriesMultivariate,
     "time_series_forecast": TimeSeriesForecast,
     "regression_model_performance": RegressionModelPerformance,
     "regression_models_comparison": RegressionModelsComparison,
 }
```

### Comparing `validmind-1.9.2/validmind/test_plans/binary_classifier.py` & `validmind-1.9.3/validmind/test_plans/binary_classifier.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/test_plans/tabular_datasets.py` & `validmind-1.9.3/validmind/test_plans/tabular_datasets.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/test_suites/__init__.py` & `validmind-1.9.3/validmind/test_suites/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -4,22 +4,24 @@
 import tabulate
 
 from .test_suites import (
     BinaryClassifierFullSuite,
     BinaryClassifierModelValidation,
     TabularDataset,
     TimeSeriesDataset,
+    TimeSeriesModelValidation,
 )
 from ..vm_models import TestSuite
 
 core_test_suites = {
     "binary_classifier_full_suite": BinaryClassifierFullSuite,
     "binary_classifier_model_validation": BinaryClassifierModelValidation,
     "tabular_dataset": TabularDataset,
     "time_series_dataset": TimeSeriesDataset,
+    "time_series_model_validation": TimeSeriesModelValidation,
 }
 
 # These test suites can be added by the user
 custom_test_suites = {}
 
 
 def _get_all_test_suites():
```

### Comparing `validmind-1.9.2/validmind/test_suites/test_suites.py` & `validmind-1.9.3/validmind/test_suites/test_suites.py`

 * *Files 26% similar despite different names*

```diff
@@ -60,7 +60,22 @@
     required_context = ["dataset"]
 
     test_plans = [
         "time_series_data_quality",
         "time_series_univariate",
         "time_series_multivariate",
     ]
+
+
+class TimeSeriesModelValidation(TestSuite):
+    """
+    Test suite for time series model validation.
+    """
+
+    name = "time_series_model_validation"
+    required_context = ["model", "models"]
+
+    test_plans = [
+        "regression_model_performance",
+        "regression_models_comparison",
+        "time_series_forecast",
+    ]
```

### Comparing `validmind-1.9.2/validmind/utils.py` & `validmind-1.9.3/validmind/utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/__init__.py` & `validmind-1.9.3/validmind/vm_models/__init__.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/dataset.py` & `validmind-1.9.3/validmind/vm_models/dataset.py`

 * *Files 1% similar despite different names*

```diff
@@ -84,14 +84,24 @@
     @property
     def index(self):
         """
         Returns the dataset's index.
         """
         return self.raw_dataset.index
 
+    @property
+    def isnull(self):
+        """
+        Returns True if there are any null values in the dataset or the index, False otherwise.
+        """
+        return (
+            self.raw_dataset.isnull().values.any()
+            or self.raw_dataset.index.isnull().any()
+        )
+
     def get_feature_by_id(self, feature_id):
         """
         Returns the feature with the given id. We also build a lazy
         lookup cache in case the same feature is requested multiple times.
 
         Args:
             feature_id (str): The id of the feature to return
```

### Comparing `validmind-1.9.2/validmind/vm_models/dataset_utils.py` & `validmind-1.9.3/validmind/vm_models/dataset_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/figure.py` & `validmind-1.9.3/validmind/vm_models/figure.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/metric.py` & `validmind-1.9.3/validmind/vm_models/metric.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/metric_result.py` & `validmind-1.9.3/validmind/vm_models/metric_result.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/model.py` & `validmind-1.9.3/validmind/vm_models/model.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/plot_utils.py` & `validmind-1.9.3/validmind/vm_models/plot_utils.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/result_summary.py` & `validmind-1.9.3/validmind/vm_models/result_summary.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/test_context.py` & `validmind-1.9.3/validmind/vm_models/test_context.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/test_plan.py` & `validmind-1.9.3/validmind/vm_models/test_plan.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/test_plan_result.py` & `validmind-1.9.3/validmind/vm_models/test_plan_result.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/test_result.py` & `validmind-1.9.3/validmind/vm_models/test_result.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/test_suite.py` & `validmind-1.9.3/validmind/vm_models/test_suite.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/validmind/vm_models/threshold_test.py` & `validmind-1.9.3/validmind/vm_models/threshold_test.py`

 * *Files identical despite different names*

### Comparing `validmind-1.9.2/PKG-INFO` & `validmind-1.9.3/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: validmind
-Version: 1.9.2
+Version: 1.9.3
 Summary: ValidMind Developer Framework
 Author: Andres Rodriguez
 Author-email: andres@validmind.ai
 Requires-Python: >=3.8,<3.11
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

