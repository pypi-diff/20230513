# Comparing `tmp/finite_difference-0.0.1.tar.gz` & `tmp/finite_difference-0.0.2.tar.gz`

## Comparing `finite_difference-0.0.1.tar` & `finite_difference-0.0.2.tar`

### file list

```diff
@@ -1,14 +1,8 @@
--rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 finite_difference-0.0.1/.gitattributes
--rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 finite_difference-0.0.1/build.bash
--rw-r--r--   0        0        0       19 2020-02-02 00:00:00.000000 finite_difference-0.0.1/test.py
--rw-r--r--   0        0        0      290 2020-02-02 00:00:00.000000 finite_difference-0.0.1/.vscode/settings.json
--rw-r--r--   0        0        0    42768 2020-02-02 00:00:00.000000 finite_difference-0.0.1/src/finite_difference/FD.py
--rw-r--r--   0        0        0       17 2020-02-02 00:00:00.000000 finite_difference-0.0.1/src/finite_difference/__init__.py
--rw-r--r--   0        0        0      352 2020-02-02 00:00:00.000000 finite_difference-0.0.1/src/finite_difference/profiler.py
--rw-r--r--   0        0        0      871 2020-02-02 00:00:00.000000 finite_difference-0.0.1/src/finite_difference/progress.txt
--rw-r--r--   0        0        0    30357 2020-02-02 00:00:00.000000 finite_difference-0.0.1/src/finite_difference/scratch.ipynb
--rw-r--r--   0        0        0    69497 2020-02-02 00:00:00.000000 finite_difference-0.0.1/src/finite_difference/simple_cases.ipynb
--rw-r--r--   0        0        0     1090 2020-02-02 00:00:00.000000 finite_difference-0.0.1/LICENSE
--rw-r--r--   0        0        0     2877 2020-02-02 00:00:00.000000 finite_difference-0.0.1/README.md
--rw-r--r--   0        0        0      763 2020-02-02 00:00:00.000000 finite_difference-0.0.1/pyproject.toml
--rw-r--r--   0        0        0     3347 2020-02-02 00:00:00.000000 finite_difference-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 finite_difference-0.0.2/.gitattributes
+-rw-r--r--   0        0        0    42768 2020-02-02 00:00:00.000000 finite_difference-0.0.2/src/finite_difference/FD.py
+-rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 finite_difference-0.0.2/src/finite_difference/__init__.py
+-rw-r--r--   0        0        0      871 2020-02-02 00:00:00.000000 finite_difference-0.0.2/src/finite_difference/progress.txt
+-rw-r--r--   0        0        0     1090 2020-02-02 00:00:00.000000 finite_difference-0.0.2/LICENSE
+-rw-r--r--   0        0        0     2811 2020-02-02 00:00:00.000000 finite_difference-0.0.2/README.md
+-rw-r--r--   0        0        0      763 2020-02-02 00:00:00.000000 finite_difference-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0     3286 2020-02-02 00:00:00.000000 finite_difference-0.0.2/PKG-INFO
```

### Comparing `finite_difference-0.0.1/src/finite_difference/FD.py` & `finite_difference-0.0.2/src/finite_difference/FD.py`

 * *Files identical despite different names*

### Comparing `finite_difference-0.0.1/src/finite_difference/progress.txt` & `finite_difference-0.0.2/src/finite_difference/progress.txt`

 * *Files identical despite different names*

### Comparing `finite_difference-0.0.1/LICENSE` & `finite_difference-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `finite_difference-0.0.1/README.md` & `finite_difference-0.0.2/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -3,56 +3,51 @@
 This is a library for setting up basic time-dependent finite difference problems. It handles the array manipulation and gives strict errors when a model isn't being set up correctly. However, it does not check for instability, nor does it check whether the model is actually physically accurate.
 
 I see this mainly as an educational tool, although if more features are added it might be helpful for some research.
 
 
 # Installation
 
-To install:
 ```
-pip install FiniteDiff
-```
-Then to import:
-```python
-# TODO need to figure out what the import will look like
+pip install finite_difference
 ```
 
 # Contributing
 Any contribution or feedback is very welcome -- feel free to create an issue on github. In particular, if you are getting unexpected behavior or unclear errors, or if there's something you would like to see added, I would want to hear.
 
 # Features
 The library can support:
 - Regular grid domains with arbitrary number of spatial dimensions
 - Periodic or fixed boundary conditions
 - Derivative approximations of arbitrary order and arbitrary sampled coordinates
 - Time-dependent scalar fields with values at cells or edges between cells
 
 # Example Use
 
-Shown is all the code required for setting up a thermal diffusion model. For more examples, see [the Google Colab](https://colab.research.google.com/drive/1RL2nIeBTFvzbeLya2Qv0NR_kOcZW_Tr9#scrollTo=StZOQhW4wIzp)
+Shown is all the code required for setting up a thermal diffusion model. For more examples, see [the Google Colab](https://colab.research.google.com/drive/1RL2nIeBTFvzbeLya2Qv0NR_kOcZW_Tr9#scrollTo=StZOQhW4wIzp).
 
 1. Create a single Model object for the domain, with a time dimension and space dimension(s).
 
 ```python
-
-m = FD.Model({"x": range(1,100,4), "t": range(1,10)}, time_axis = "t")
+import finite_difference as fd
+m = fd.Model({"x": range(1,100,4), "t": range(1,10)}, time_axis = "t")
 ```
 
 2. Create fields representing a property that changes over time as a scalar field. 
 
 ```python
 
-T = FD.Field(m, "Temperature", n_time_ders = 1)
+T = fd.Field(m, "Temperature", n_time_ders = 1)
 ```
 
 3. Create stencils for numerical approximations of spatial derivatives.
 
 ```python
 
-diff_2 = FD.Stencil([-1,0,1],der_order=2)
+diff_2 = fd.Stencil([-1,0,1],der_order=2)
 ```
 
 
 4. Apply boundary conditions and initial conditions.
 
 ```python
```

### Comparing `finite_difference-0.0.1/pyproject.toml` & `finite_difference-0.0.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 [project]
 name = "finite_difference"
-version = "0.0.1"
+version = "0.0.2"
 authors = [
   { name="Ephraim Bryski", email="ebryski1@gmail.com"},
 ]
 description = "Library for setting up finite difference problems"
 readme = "README.md"
 requires-python = ">=3"
 classifiers = [
```

### Comparing `finite_difference-0.0.1/PKG-INFO` & `finite_difference-0.0.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: finite_difference
-Version: 0.0.1
+Version: 0.0.2
 Summary: Library for setting up finite difference problems
 Project-URL: Homepage, https://github.com/Ephraim-Bryski/Finite-Difference
 Project-URL: Bug Tracker, https://github.com/Ephraim-Bryski/Finite-Difference/issues
 Author-email: Ephraim Bryski <ebryski1@gmail.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -17,56 +17,51 @@
 This is a library for setting up basic time-dependent finite difference problems. It handles the array manipulation and gives strict errors when a model isn't being set up correctly. However, it does not check for instability, nor does it check whether the model is actually physically accurate.
 
 I see this mainly as an educational tool, although if more features are added it might be helpful for some research.
 
 
 # Installation
 
-To install:
 ```
-pip install FiniteDiff
-```
-Then to import:
-```python
-# TODO need to figure out what the import will look like
+pip install finite_difference
 ```
 
 # Contributing
 Any contribution or feedback is very welcome -- feel free to create an issue on github. In particular, if you are getting unexpected behavior or unclear errors, or if there's something you would like to see added, I would want to hear.
 
 # Features
 The library can support:
 - Regular grid domains with arbitrary number of spatial dimensions
 - Periodic or fixed boundary conditions
 - Derivative approximations of arbitrary order and arbitrary sampled coordinates
 - Time-dependent scalar fields with values at cells or edges between cells
 
 # Example Use
 
-Shown is all the code required for setting up a thermal diffusion model. For more examples, see [the Google Colab](https://colab.research.google.com/drive/1RL2nIeBTFvzbeLya2Qv0NR_kOcZW_Tr9#scrollTo=StZOQhW4wIzp)
+Shown is all the code required for setting up a thermal diffusion model. For more examples, see [the Google Colab](https://colab.research.google.com/drive/1RL2nIeBTFvzbeLya2Qv0NR_kOcZW_Tr9#scrollTo=StZOQhW4wIzp).
 
 1. Create a single Model object for the domain, with a time dimension and space dimension(s).
 
 ```python
-
-m = FD.Model({"x": range(1,100,4), "t": range(1,10)}, time_axis = "t")
+import finite_difference as fd
+m = fd.Model({"x": range(1,100,4), "t": range(1,10)}, time_axis = "t")
 ```
 
 2. Create fields representing a property that changes over time as a scalar field. 
 
 ```python
 
-T = FD.Field(m, "Temperature", n_time_ders = 1)
+T = fd.Field(m, "Temperature", n_time_ders = 1)
 ```
 
 3. Create stencils for numerical approximations of spatial derivatives.
 
 ```python
 
-diff_2 = FD.Stencil([-1,0,1],der_order=2)
+diff_2 = fd.Stencil([-1,0,1],der_order=2)
 ```
 
 
 4. Apply boundary conditions and initial conditions.
 
 ```python
```

