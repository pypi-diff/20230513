# Comparing `tmp/pyportfolioanalytics-0.1.4.tar.gz` & `tmp/pyportfolioanalytics-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyportfolioanalytics-0.1.4.tar", last modified: Sat May 13 16:26:16 2023, max compression
+gzip compressed data, was "pyportfolioanalytics-0.1.5.tar", last modified: Sat May 13 16:30:29 2023, max compression
```

## Comparing `pyportfolioanalytics-0.1.4.tar` & `pyportfolioanalytics-0.1.5.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 16:26:16.842645 pyportfolioanalytics-0.1.4/
--rw-rw-rw-   0        0        0     1104 2023-05-05 02:24:24.000000 pyportfolioanalytics-0.1.4/LICENSE
--rw-rw-rw-   0        0        0      394 2023-05-13 16:26:16.842516 pyportfolioanalytics-0.1.4/PKG-INFO
--rw-rw-rw-   0        0        0     4628 2023-05-13 15:31:51.000000 pyportfolioanalytics-0.1.4/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 16:26:16.811390 pyportfolioanalytics-0.1.4/pyportfolioanalytics/
--rw-rw-rw-   0        0        0     1307 2023-05-12 02:23:51.000000 pyportfolioanalytics-0.1.4/pyportfolioanalytics/__init__.py
--rw-rw-rw-   0        0        0    10699 2023-05-11 03:07:38.000000 pyportfolioanalytics-0.1.4/pyportfolioanalytics/report.py
--rw-rw-rw-   0        0        0    30531 2023-05-13 16:25:45.000000 pyportfolioanalytics-0.1.4/pyportfolioanalytics/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-13 16:26:16.839460 pyportfolioanalytics-0.1.4/pyportfolioanalytics.egg-info/
--rw-rw-rw-   0        0        0      394 2023-05-13 16:26:16.000000 pyportfolioanalytics-0.1.4/pyportfolioanalytics.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      354 2023-05-13 16:26:16.000000 pyportfolioanalytics-0.1.4/pyportfolioanalytics.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 16:26:16.000000 pyportfolioanalytics-0.1.4/pyportfolioanalytics.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       51 2023-05-13 16:26:16.000000 pyportfolioanalytics-0.1.4/pyportfolioanalytics.egg-info/requires.txt
--rw-rw-rw-   0        0        0       21 2023-05-13 16:26:16.000000 pyportfolioanalytics-0.1.4/pyportfolioanalytics.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       91 2023-05-08 17:58:57.000000 pyportfolioanalytics-0.1.4/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-13 16:26:16.843798 pyportfolioanalytics-0.1.4/setup.cfg
--rw-rw-rw-   0        0        0      918 2023-05-13 16:26:02.000000 pyportfolioanalytics-0.1.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:30:29.027181 pyportfolioanalytics-0.1.5/
+-rw-rw-rw-   0        0        0     1104 2023-05-05 02:24:24.000000 pyportfolioanalytics-0.1.5/LICENSE
+-rw-rw-rw-   0        0        0      394 2023-05-13 16:30:29.025181 pyportfolioanalytics-0.1.5/PKG-INFO
+-rw-rw-rw-   0        0        0     4628 2023-05-13 15:31:51.000000 pyportfolioanalytics-0.1.5/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 16:30:29.002598 pyportfolioanalytics-0.1.5/pyportfolioanalytics/
+-rw-rw-rw-   0        0        0     1371 2023-05-13 16:30:05.000000 pyportfolioanalytics-0.1.5/pyportfolioanalytics/__init__.py
+-rw-rw-rw-   0        0        0    10699 2023-05-11 03:07:38.000000 pyportfolioanalytics-0.1.5/pyportfolioanalytics/report.py
+-rw-rw-rw-   0        0        0    30531 2023-05-13 16:25:45.000000 pyportfolioanalytics-0.1.5/pyportfolioanalytics/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:30:29.023168 pyportfolioanalytics-0.1.5/pyportfolioanalytics.egg-info/
+-rw-rw-rw-   0        0        0      394 2023-05-13 16:30:28.000000 pyportfolioanalytics-0.1.5/pyportfolioanalytics.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      354 2023-05-13 16:30:28.000000 pyportfolioanalytics-0.1.5/pyportfolioanalytics.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 16:30:28.000000 pyportfolioanalytics-0.1.5/pyportfolioanalytics.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       51 2023-05-13 16:30:28.000000 pyportfolioanalytics-0.1.5/pyportfolioanalytics.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       21 2023-05-13 16:30:28.000000 pyportfolioanalytics-0.1.5/pyportfolioanalytics.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       91 2023-05-08 17:58:57.000000 pyportfolioanalytics-0.1.5/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 16:30:29.027181 pyportfolioanalytics-0.1.5/setup.cfg
+-rw-rw-rw-   0        0        0      918 2023-05-13 16:30:21.000000 pyportfolioanalytics-0.1.5/setup.py
```

### Comparing `pyportfolioanalytics-0.1.4/LICENSE` & `pyportfolioanalytics-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `pyportfolioanalytics-0.1.4/README.md` & `pyportfolioanalytics-0.1.5/README.md`

 * *Files identical despite different names*

### Comparing `pyportfolioanalytics-0.1.4/pyportfolioanalytics/__init__.py` & `pyportfolioanalytics-0.1.5/pyportfolioanalytics/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 from pyportfolioanalytics.utils import covariance_matrix
 from pyportfolioanalytics.utils import plot_price_close
 from pyportfolioanalytics.utils import histogram_yield
 from pyportfolioanalytics.utils import plot_yield_deviation_mean
 from pyportfolioanalytics.utils import plot_cov_matrix
 from pyportfolioanalytics.utils import plot_corr_matrix
 from pyportfolioanalytics.utils import plot_logarithmic_yield
+from pyportfolioanalytics.utils import stock_chart_candlestick
 from pyportfolioanalytics.utils import get_stock_price_close
 from pyportfolioanalytics.utils import get_name_columns
 from pyportfolioanalytics.utils import get_date_start
 from pyportfolioanalytics.utils import get_date_end
 from pyportfolioanalytics.utils import plot_return_log
 from pyportfolioanalytics.utils import histogram_stock_returns
 from pyportfolioanalytics.utils import return_log_mean_and_standard_deviation
```

### Comparing `pyportfolioanalytics-0.1.4/pyportfolioanalytics/report.py` & `pyportfolioanalytics-0.1.5/pyportfolioanalytics/report.py`

 * *Files identical despite different names*

### Comparing `pyportfolioanalytics-0.1.4/pyportfolioanalytics/utils.py` & `pyportfolioanalytics-0.1.5/pyportfolioanalytics/utils.py`

 * *Files identical despite different names*

### Comparing `pyportfolioanalytics-0.1.4/setup.py` & `pyportfolioanalytics-0.1.5/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import pathlib
 from setuptools import find_packages, setup
 
 HERE = pathlib.Path(__file__).parent
 
-VERSION = '0.1.4'
+VERSION = '0.1.5'
 PACKAGE_NAME = 'pyportfolioanalytics'
 AUTHOR = 'Sebastian Marat Urdanegui Bisalaya'
 AUTHOR_EMAIL = 'sebasurdanegui@gmail.com'
 URL = 'https://github.com/SebastianUrdaneguiBisalaya/py-portfolioanalytics'
 
 LICENSE = 'MIT'
 DESCRIPTION = 'Librería para leer ficheros PDFs y extraer la información en formato str'
```

