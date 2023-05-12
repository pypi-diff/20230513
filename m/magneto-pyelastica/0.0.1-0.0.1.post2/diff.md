# Comparing `tmp/magneto_pyelastica-0.0.1.tar.gz` & `tmp/magneto_pyelastica-0.0.1.post2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "magneto_pyelastica-0.0.1.tar", max compression
+gzip compressed data, was "magneto_pyelastica-0.0.1.post2.tar", max compression
```

## Comparing `magneto_pyelastica-0.0.1.tar` & `magneto_pyelastica-0.0.1.post2.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1071 2022-07-16 18:55:55.753084 magneto_pyelastica-0.0.1/LICENSE
--rw-r--r--   0        0        0      136 2022-07-26 22:53:11.032417 magneto_pyelastica-0.0.1/magneto_pyelastica/__init__.py
--rw-r--r--   0        0        0     6484 2022-07-22 04:25:32.476232 magneto_pyelastica-0.0.1/magneto_pyelastica/magnetic_field.py
--rw-r--r--   0        0        0     4115 2022-07-22 04:25:32.476458 magneto_pyelastica-0.0.1/magneto_pyelastica/magnetic_forces.py
--rw-r--r--   0        0        0      907 2022-07-22 04:25:32.476667 magneto_pyelastica-0.0.1/magneto_pyelastica/utils.py
--rw-r--r--   0        0        0       18 2022-07-27 03:36:04.557069 magneto_pyelastica-0.0.1/magneto_pyelastica/version.py
--rw-r--r--   0        0        0     1551 2022-07-28 04:12:47.049011 magneto_pyelastica-0.0.1/pyproject.toml
--rw-r--r--   0        0        0      910 2022-07-28 04:14:00.319654 magneto_pyelastica-0.0.1/setup.py
--rw-r--r--   0        0        0      837 2022-07-28 04:14:00.319802 magneto_pyelastica-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0     1088 2022-07-29 21:25:58.655307 magneto_pyelastica-0.0.1.post2/LICENSE
+-rw-r--r--   0        0        0     2834 2023-05-12 22:36:13.961735 magneto_pyelastica-0.0.1.post2/README.md
+-rw-r--r--   0        0        0      136 2022-07-26 22:53:11.032417 magneto_pyelastica-0.0.1.post2/magneto_pyelastica/__init__.py
+-rw-r--r--   0        0        0     6458 2022-08-04 15:21:07.847499 magneto_pyelastica-0.0.1.post2/magneto_pyelastica/magnetic_field.py
+-rw-r--r--   0        0        0     4115 2022-07-22 04:25:32.476458 magneto_pyelastica-0.0.1.post2/magneto_pyelastica/magnetic_forces.py
+-rw-r--r--   0        0        0      907 2022-07-22 04:25:32.476667 magneto_pyelastica-0.0.1.post2/magneto_pyelastica/utils.py
+-rw-r--r--   0        0        0       18 2022-07-27 03:36:04.557069 magneto_pyelastica-0.0.1.post2/magneto_pyelastica/version.py
+-rw-r--r--   0        0        0     1571 2023-05-12 23:42:54.344922 magneto_pyelastica-0.0.1.post2/pyproject.toml
+-rw-r--r--   0        0        0     3698 1970-01-01 00:00:00.000000 magneto_pyelastica-0.0.1.post2/PKG-INFO
```

### Comparing `magneto_pyelastica-0.0.1/LICENSE` & `magneto_pyelastica-0.0.1.post2/LICENSE`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 MIT License
 
-Copyright (c) 2022 Arman Tekinalp
+Copyright (c) 2022 Arman Tekinalp, Yashraj Bhosale
 
 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:
```

### Comparing `magneto_pyelastica-0.0.1/magneto_pyelastica/magnetic_field.py` & `magneto_pyelastica-0.0.1.post2/magneto_pyelastica/magnetic_field.py`

 * *Files 0% similar despite different names*

```diff
@@ -20,15 +20,14 @@
 
     """
 
     def __init__(self):
         """
         BaseMagneticField class does not need any input parameters.
         """
-        pass
 
     def value(self, time: np.float64 = 0.0):
         """Returns the value of the magnetic field vector.
 
         In BaseMagneticField class, this routine simply passes.
 
         Parameters
@@ -36,15 +35,14 @@
         time : float
             The time of simulation.
 
         Returns
         -------
 
         """
-        pass
 
 
 class ConstantMagneticField(BaseMagneticField):
     """
     This class represents a magnetic field constant in time.
 
         Attributes
```

### Comparing `magneto_pyelastica-0.0.1/magneto_pyelastica/magnetic_forces.py` & `magneto_pyelastica-0.0.1.post2/magneto_pyelastica/magnetic_forces.py`

 * *Files identical despite different names*

### Comparing `magneto_pyelastica-0.0.1/magneto_pyelastica/utils.py` & `magneto_pyelastica-0.0.1.post2/magneto_pyelastica/utils.py`

 * *Files identical despite different names*

### Comparing `magneto_pyelastica-0.0.1/pyproject.toml` & `magneto_pyelastica-0.0.1.post2/pyproject.toml`

 * *Files 13% similar despite different names*

```diff
@@ -1,46 +1,46 @@
 # Poetry pyproject.toml: https://python-poetry.org/docs/pyproject/
 [build-system]
 requires = ["poetry_core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "magneto_pyelastica"
-version = "0.0.1"
+version = "0.0.1.post2"
 description = "Python software for simulating magnetic Cosserat rods."
-#readme = "README.md"
-authors = ["Arman Tekinalp <armant2@illinois.edu>, Yashraj Bhosale <bhosale2@illinois.edu>"]
+readme = "README.md"
+authors = ["Arman Tekinalp <armant2@illinois.edu>", "Yashraj Bhosale <bhosale2@illinois.edu>"]
 license = "MIT"
 repository = "https://github.com/armantekinalp/MagnetoPyElastica"
 #documentation = "https://miv-os.readthedocs.io"
-#keywords = []
+keywords = ["python", "simulation", "elastica", "cosserat-rod", "magneto-elastodynamics"]
 
 # ...
 packages = [
     { include = "magneto_pyelastica" }
 ]
 
 [tool.poetry.dependencies]
 python = ">=3.8,<3.11"
-pyelastica = {git = "https://github.com/GazzolaLab/PyElastica.git", rev = "update-0.3.0"}
-cma = {version = "^3.2.2", optional = true, extras = ["examples"]}
-
+pyelastica = "^0.3"
+matplotlib = {version = "^3.3.2", optional = true}
 
 [tool.poetry.dev-dependencies]
 black = "^22.3.0"
 pytest = "^7.1.2"
 coverage = "^6.3.3"
 pytest-html = "^3.1.1"
 pytest-cov = "^3.0.0"
-flake8 = "^4.0.1"
+flake8 = "^3.8"
 pre-commit = "^2.19.0"
+autoflake8 = "^0.3"
 
 [tool.poetry.extras]
 examples = [
-  "cma",
+  "matplotlib",
 ]
 
 [tool.black]
 # https://github.com/psf/black
 target-version = ["py38"]
 line-length = 88
 color = true
```

