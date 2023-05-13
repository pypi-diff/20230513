# Comparing `tmp/pyportfolioanalytics-0.1.2.tar.gz` & `tmp/pyportfolioanalytics-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyportfolioanalytics-0.1.2.tar", last modified: Sat May 13 15:37:06 2023, max compression
+gzip compressed data, was "pyportfolioanalytics-0.1.3.tar", last modified: Sat May 13 16:06:14 2023, max compression
```

## Comparing `pyportfolioanalytics-0.1.2.tar` & `pyportfolioanalytics-0.1.3.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 15:37:06.872862 pyportfolioanalytics-0.1.2/
--rw-rw-rw-   0        0        0     1104 2023-05-05 02:24:24.000000 pyportfolioanalytics-0.1.2/LICENSE
--rw-rw-rw-   0        0        0      394 2023-05-13 15:37:06.872268 pyportfolioanalytics-0.1.2/PKG-INFO
--rw-rw-rw-   0        0        0     4628 2023-05-13 15:31:51.000000 pyportfolioanalytics-0.1.2/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 15:37:06.844771 pyportfolioanalytics-0.1.2/pyportfolioanalytics/
--rw-rw-rw-   0        0        0     1307 2023-05-12 02:23:51.000000 pyportfolioanalytics-0.1.2/pyportfolioanalytics/__init__.py
--rw-rw-rw-   0        0        0    10699 2023-05-11 03:07:38.000000 pyportfolioanalytics-0.1.2/pyportfolioanalytics/report.py
--rw-rw-rw-   0        0        0    30680 2023-05-13 15:31:44.000000 pyportfolioanalytics-0.1.2/pyportfolioanalytics/utils.py
-drwxrwxrwx   0        0        0        0 2023-05-13 15:37:06.870222 pyportfolioanalytics-0.1.2/pyportfolioanalytics.egg-info/
--rw-rw-rw-   0        0        0      394 2023-05-13 15:37:06.000000 pyportfolioanalytics-0.1.2/pyportfolioanalytics.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      354 2023-05-13 15:37:06.000000 pyportfolioanalytics-0.1.2/pyportfolioanalytics.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 15:37:06.000000 pyportfolioanalytics-0.1.2/pyportfolioanalytics.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       51 2023-05-13 15:37:06.000000 pyportfolioanalytics-0.1.2/pyportfolioanalytics.egg-info/requires.txt
--rw-rw-rw-   0        0        0       21 2023-05-13 15:37:06.000000 pyportfolioanalytics-0.1.2/pyportfolioanalytics.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       91 2023-05-08 17:58:57.000000 pyportfolioanalytics-0.1.2/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-13 15:37:06.872862 pyportfolioanalytics-0.1.2/setup.cfg
--rw-rw-rw-   0        0        0      918 2023-05-13 15:36:59.000000 pyportfolioanalytics-0.1.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:06:14.409198 pyportfolioanalytics-0.1.3/
+-rw-rw-rw-   0        0        0     1104 2023-05-05 02:24:24.000000 pyportfolioanalytics-0.1.3/LICENSE
+-rw-rw-rw-   0        0        0      394 2023-05-13 16:06:14.407140 pyportfolioanalytics-0.1.3/PKG-INFO
+-rw-rw-rw-   0        0        0     4628 2023-05-13 15:31:51.000000 pyportfolioanalytics-0.1.3/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 16:06:14.349446 pyportfolioanalytics-0.1.3/pyportfolioanalytics/
+-rw-rw-rw-   0        0        0     1307 2023-05-12 02:23:51.000000 pyportfolioanalytics-0.1.3/pyportfolioanalytics/__init__.py
+-rw-rw-rw-   0        0        0    10699 2023-05-11 03:07:38.000000 pyportfolioanalytics-0.1.3/pyportfolioanalytics/report.py
+-rw-rw-rw-   0        0        0    30638 2023-05-13 16:05:42.000000 pyportfolioanalytics-0.1.3/pyportfolioanalytics/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:06:14.402945 pyportfolioanalytics-0.1.3/pyportfolioanalytics.egg-info/
+-rw-rw-rw-   0        0        0      394 2023-05-13 16:06:14.000000 pyportfolioanalytics-0.1.3/pyportfolioanalytics.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      354 2023-05-13 16:06:14.000000 pyportfolioanalytics-0.1.3/pyportfolioanalytics.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 16:06:14.000000 pyportfolioanalytics-0.1.3/pyportfolioanalytics.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       51 2023-05-13 16:06:14.000000 pyportfolioanalytics-0.1.3/pyportfolioanalytics.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       21 2023-05-13 16:06:14.000000 pyportfolioanalytics-0.1.3/pyportfolioanalytics.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       91 2023-05-08 17:58:57.000000 pyportfolioanalytics-0.1.3/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 16:06:14.409198 pyportfolioanalytics-0.1.3/setup.cfg
+-rw-rw-rw-   0        0        0      918 2023-05-13 16:05:57.000000 pyportfolioanalytics-0.1.3/setup.py
```

### Comparing `pyportfolioanalytics-0.1.2/LICENSE` & `pyportfolioanalytics-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `pyportfolioanalytics-0.1.2/README.md` & `pyportfolioanalytics-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `pyportfolioanalytics-0.1.2/pyportfolioanalytics/__init__.py` & `pyportfolioanalytics-0.1.3/pyportfolioanalytics/__init__.py`

 * *Files identical despite different names*

### Comparing `pyportfolioanalytics-0.1.2/pyportfolioanalytics/report.py` & `pyportfolioanalytics-0.1.3/pyportfolioanalytics/report.py`

 * *Files identical despite different names*

### Comparing `pyportfolioanalytics-0.1.2/pyportfolioanalytics/utils.py` & `pyportfolioanalytics-0.1.3/pyportfolioanalytics/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -88,15 +88,14 @@
     right_side = ax.spines["right"]
     right_side.set_visible(False)
     top_side = ax.spines["top"]
     top_side.set_visible(False)
     ax.set_axisbelow(True)
     ax.grid(color='gray', linewidth=1, axis='y', alpha=0.4)
     plt.show()
-    return fig
     
 
 
 def histogram_yield(list_stocks, start = '2022-01-01', end = '2023-01-01'):
     return_stock = return_daily(list_stock = list_stocks, start = start, end = end)
     red_color = sns.cubehelix_palette(start=2,rot=0, dark=0, light=.95)
     sns.set_palette(red_color)
@@ -113,15 +112,14 @@
     top_side.set_visible(False)
     ax.set_axisbelow(True)
     ax.grid(color='gray', linewidth=1, axis='y', alpha=0.4)
     plt.title(f"Histograma del rendimiento\nlogarítmico de las acciones", size = 15)
     plt.xlabel("Rendimiento")
     plt.ylabel("Frecuencia")
     plt.show()
-    return fig
     
 def plot_yield_deviation_mean(list_stocks, start = '2022-01-01', end = '2023-01-01'):
     return_stock = pd.DataFrame(return_daily(list_stock = list_stocks, start = start, end = end).mean()).rename(columns = {
         0:'Rendimiento promedio anualizado %'
     }).reset_index()
     return_stock = return_stock.rename(columns = {'index':"Acción"})
     return_stock["Rendimiento promedio anualizado %"] = return_stock["Rendimiento promedio anualizado %"]
@@ -157,15 +155,15 @@
 
 def plot_cov_matrix(list_stock, start = '2022-01-01', end = '2023-01-01'):
     covmatrix = covariance_matrix(list_stock, start = start, end = end)
     fig, ax = plt.subplots(figsize = (15,8), dpi = 80)
     plt.title("Matriz de varianza y covarianza", size = 15)
     ax = sns.heatmap(covmatrix, cmap = 'Blues', annot = True)
     plt.show()
-    return fig
+    
     
 
 def plot_corr_matrix(list_stock, start = '2022-01-01', end = '2023-01-01'):
     return_stock = return_daily(list_stock, start = start, end = end)
     fig, ax = plt.subplots(figsize = (15,8), dpi = 80)
     ax = sns.heatmap(data = return_stock.corr(), annot = True, cmap = 'YlGnBu')
     plt.title("Matriz de Correlación", size = 15)
```

### Comparing `pyportfolioanalytics-0.1.2/setup.py` & `pyportfolioanalytics-0.1.3/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import pathlib
 from setuptools import find_packages, setup
 
 HERE = pathlib.Path(__file__).parent
 
-VERSION = '0.1.2'
+VERSION = '0.1.3'
 PACKAGE_NAME = 'pyportfolioanalytics'
 AUTHOR = 'Sebastian Marat Urdanegui Bisalaya'
 AUTHOR_EMAIL = 'sebasurdanegui@gmail.com'
 URL = 'https://github.com/SebastianUrdaneguiBisalaya/py-portfolioanalytics'
 
 LICENSE = 'MIT'
 DESCRIPTION = 'Librería para leer ficheros PDFs y extraer la información en formato str'
```

