# Comparing `tmp/balrogo-1.6.4.tar.gz` & `tmp/balrogo-1.6.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "balrogo-1.6.4.tar", max compression
+gzip compressed data, was "balrogo-1.6.5.tar", max compression
```

## Comparing `balrogo-1.6.4.tar` & `balrogo-1.6.5.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0     1090 2020-11-09 15:43:31.991839 balrogo-1.6.4/LICENSE
--rw-r--r--   0        0        0     5130 2021-07-03 09:08:14.177776 balrogo-1.6.4/README.md
--rw-r--r--   0        0        0      153 2020-12-16 16:58:29.555231 balrogo-1.6.4/balrogo/__init__.py
--rwxr-xr-x   0        0        0    31313 2022-08-24 16:32:38.816567 balrogo-1.6.4/balrogo/angle.py
--rw-r--r--   0        0        0    88936 2023-01-13 17:55:58.300460 balrogo-1.6.4/balrogo/dynamics.py
--rwxr-xr-x   0        0        0    33850 2022-08-24 16:32:38.768567 balrogo-1.6.4/balrogo/gaia.py
--rwxr-xr-x   0        0        0     5538 2021-01-29 14:16:08.816985 balrogo-1.6.4/balrogo/hrd.py
--rwxr-xr-x   0        0        0    27818 2021-06-26 17:29:21.281211 balrogo-1.6.4/balrogo/marginals.py
--rw-r--r--   0        0        0    10097 2021-06-26 12:16:33.674788 balrogo-1.6.4/balrogo/mock.py
--rwxr-xr-x   0        0        0     5745 2021-01-29 14:16:08.816985 balrogo-1.6.4/balrogo/parallax.py
--rw-r--r--   0        0        0    52354 2023-01-28 01:17:37.176233 balrogo-1.6.4/balrogo/pm.py
--rw-r--r--   0        0        0   109400 2023-01-16 01:13:59.473054 balrogo-1.6.4/balrogo/position.py
--rw-r--r--   0        0        0      875 2023-01-28 01:17:37.176233 balrogo-1.6.4/pyproject.toml
--rw-r--r--   0        0        0     6178 2023-01-28 01:17:43.022861 balrogo-1.6.4/setup.py
--rw-r--r--   0        0        0     6111 2023-01-28 01:17:43.023162 balrogo-1.6.4/PKG-INFO
+-rw-r--r--   0        0        0     1090 2020-11-09 15:43:31.991839 balrogo-1.6.5/LICENSE
+-rw-r--r--   0        0        0     5130 2021-07-03 09:08:14.177776 balrogo-1.6.5/README.md
+-rw-r--r--   0        0        0      153 2020-12-16 16:58:29.555231 balrogo-1.6.5/balrogo/__init__.py
+-rwxr-xr-x   0        0        0    31398 2023-05-13 20:06:47.596043 balrogo-1.6.5/balrogo/angle.py
+-rw-r--r--   0        0        0    88940 2023-05-13 20:06:47.596043 balrogo-1.6.5/balrogo/dynamics.py
+-rwxr-xr-x   0        0        0    33854 2023-05-13 20:06:47.596043 balrogo-1.6.5/balrogo/gaia.py
+-rwxr-xr-x   0        0        0     5538 2021-01-29 14:16:08.816985 balrogo-1.6.5/balrogo/hrd.py
+-rwxr-xr-x   0        0        0    27818 2021-06-26 17:29:21.281211 balrogo-1.6.5/balrogo/marginals.py
+-rw-r--r--   0        0        0    10097 2021-06-26 12:16:33.674788 balrogo-1.6.5/balrogo/mock.py
+-rwxr-xr-x   0        0        0     5745 2021-01-29 14:16:08.816985 balrogo-1.6.5/balrogo/parallax.py
+-rw-r--r--   0        0        0    52358 2023-05-13 20:06:47.596043 balrogo-1.6.5/balrogo/pm.py
+-rw-r--r--   0        0        0   109400 2023-01-16 01:13:59.473054 balrogo-1.6.5/balrogo/position.py
+-rw-r--r--   0        0        0      875 2023-05-13 20:06:47.596043 balrogo-1.6.5/pyproject.toml
+-rw-r--r--   0        0        0     6178 2023-05-13 20:07:00.158173 balrogo-1.6.5/setup.py
+-rw-r--r--   0        0        0     6111 2023-05-13 20:07:00.158669 balrogo-1.6.5/PKG-INFO
```

### Comparing `balrogo-1.6.4/LICENSE` & `balrogo-1.6.5/LICENSE`

 * *Files identical despite different names*

### Comparing `balrogo-1.6.4/README.md` & `balrogo-1.6.5/README.md`

 * *Files identical despite different names*

### Comparing `balrogo-1.6.4/balrogo/angle.py` & `balrogo-1.6.5/balrogo/angle.py`

 * *Files 1% similar despite different names*

```diff
@@ -399,15 +399,19 @@
             B[i] = np.arcsin(v_f[i][2])
             cosA = v_f[i][0] / np.cos(B[i])
             sinA = v_f[i][1] / np.cos(B[i])
 
             A[i] = np.arctan2(sinA, cosA)
 
             if debug is True and i < 10:
-                print("A, B [degrees]:", A[i] * (180 / np.pi), B[i] * (180 / np.pi))
+                print(
+                    "A, B [degrees]:",
+                    A[i] * (180 / np.pi),
+                    B[i] * (180 / np.pi),
+                )
     else:
         print("You did not give a valid input for the Rodrigues formula.")
         return
 
     return A * (180 / np.pi), B * (180 / np.pi)
 
 
@@ -514,15 +518,15 @@
 
     phi = np.nanmean(pf - p0)
 
     v_i, v0_i, v0_f = sky_vector(a, d, af, df, af, df)
 
     a, d = sky_coord_rotate(v_i, v0_i, v0_f, theta=phi)
 
-    return a, d
+    return a % 360, d
 
 
 def rotate_axis(x, y, theta, mu_x=0, mu_y=0):
     """
     Rotates and translates the two main cartesian axis.
 
     Parameters
```

### Comparing `balrogo-1.6.4/balrogo/dynamics.py` & `balrogo-1.6.5/balrogo/dynamics.py`

 * *Files 0% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 # June 2021, Paris
 #
 # This file contains the main functions concerning the dispersion functions,
 # (i.e., velocity disperstion and anisotropy). It also converts plane of sky
 # velocities (and uncertainties) from (RA,Dec) to polar coordinates.
 #
 # Documentation is provided on Vitral, 2021.
-# If you have any further questions please email vitral@iap.fr
+# If you have any further questions please email evitral@stsci.edu
 #
 ###############################################################################
 
 from . import position
 from . import angle
 
 import numpy as np
```

### Comparing `balrogo-1.6.4/balrogo/gaia.py` & `balrogo-1.6.5/balrogo/gaia.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 #
 # November 2020, Paris
 #
 # This file contains the main functions concerning the handling of the
 # Gaia mission data.
 #
 # Documentation is provided on Vitral, 2021.
-# If you have any further questions please email vitral@iap.fr
+# If you have any further questions please email evitral@stsci.edu
 #
 ###############################################################################
 
 import numpy as np
 import matplotlib.pyplot as plt
 import matplotlib.colors as mc
 from astropy.io import fits
```

### Comparing `balrogo-1.6.4/balrogo/hrd.py` & `balrogo-1.6.5/balrogo/hrd.py`

 * *Files identical despite different names*

### Comparing `balrogo-1.6.4/balrogo/marginals.py` & `balrogo-1.6.5/balrogo/marginals.py`

 * *Files identical despite different names*

### Comparing `balrogo-1.6.4/balrogo/mock.py` & `balrogo-1.6.5/balrogo/mock.py`

 * *Files identical despite different names*

### Comparing `balrogo-1.6.4/balrogo/parallax.py` & `balrogo-1.6.5/balrogo/parallax.py`

 * *Files identical despite different names*

### Comparing `balrogo-1.6.4/balrogo/pm.py` & `balrogo-1.6.5/balrogo/pm.py`

 * *Files 0% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 # November 2020, Paris
 #
 # This file contains the main functions concerning proper motion data.
 # It provides MCMC and maximum likelihood fits of proper motions data,
 # as well as robust initial guesses for those fits.
 #
 # Documentation is provided on Vitral, 2021.
-# If you have any further questions please email vitral@iap.fr
+# If you have any further questions please email evitral@stsci.edu
 #
 ###############################################################################
 
 import numpy as np
 from scipy.optimize import minimize
 from scipy.optimize import differential_evolution
 from scipy import integrate
```

### Comparing `balrogo-1.6.4/balrogo/position.py` & `balrogo-1.6.5/balrogo/position.py`

 * *Files identical despite different names*

### Comparing `balrogo-1.6.4/pyproject.toml` & `balrogo-1.6.5/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "balrogo"
-version = "1.6.4"
+version = "1.6.5"
 description = "Bayesian Astrometric Likelihood Recovery of Galactic Objects"
 authors = ["Eduardo Vitral <vitral@iap.fr>", "Alexandre Macedo <arj.macedo@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://gitlab.com/eduardo-vitral/balrogo"
 
 [tool.poetry.dependencies]
```

### Comparing `balrogo-1.6.4/setup.py` & `balrogo-1.6.5/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -17,15 +17,15 @@
  'shapely>=1.6.4,<2.0.0']
 
 extras_require = \
 {':python_version < "3.8"': ['importlib_metadata>=3.3.0,<4.0.0']}
 
 setup_kwargs = {
     'name': 'balrogo',
-    'version': '1.6.4',
+    'version': '1.6.5',
     'description': 'Bayesian Astrometric Likelihood Recovery of Galactic Objects',
     'long_description': '# BALRoGO\n\n[![pipeline status](https://gitlab.com/eduardo-vitral/balrogo/badges/master/pipeline.svg)](https://gitlab.com/eduardo-vitral/balrogo/-/commits/master)\n[![coverage report](https://gitlab.com/eduardo-vitral/balrogo/badges/master/coverage.svg)](https://gitlab.com/eduardo-vitral/balrogo/-/commits/master)\n[![pypi](https://img.shields.io/pypi/v/balrogo.svg)](https://pypi.python.org/pypi/balrogo/)\n[![python](https://img.shields.io/pypi/pyversions/balrogo.svg)](https://pypi.python.org/pypi/balrogo)\n[![license](http://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)\n\n<!-- markdownlint-disable-next-line no-inline-html -->\n<img alt="logo" align="right" src="https://gitlab.com/eduardo-vitral/balrogo/-/raw/master/logo.png" width="20%" />\n\nBALRoGO: Bayesian Astrometric Likelihood Recovery of Galactic Objects.\n\n- Specially developed to handle data from the Gaia space mission.\n- Extracts galactic objects such as globular clusters and dwarf galaxies from data contaminated by interlopers.\n- Uses a combination of Bayesian and non-Bayesian approaches.\n- Provides:\n  - Fits of proper motion space.\n  - Fits of surface density.\n  - Fits of object center.\n  - Confidence regions for the color-magnitude diagram and parallaxes.\n\nIf something does not work, please [file an issue](https://gitlab.com/eduardo-vitral/balrogo/-/issues).\n\n## Attribution\n\nPlease cite [us](https://academic.oup.com/mnras/article-abstract/504/1/1355/6237524?redirectedFrom=fulltext) if you find this code useful in your research. The BibTeX entry for the paper is:\n\n```bibtex\n@ARTICLE{Vitral21,\n   author = {{Vitral}, Eduardo},\n    title = "BALRoGO: Bayesian Astrometric Likelihood Recovery of Galactic Objects - Global properties of over one hundred globular clusters with Gaia EDR3",\n  journal = {\\mnras},\n     year = 2021,\n    month = jun,\n   volume = {504},\n   number = {1},\n    pages = {1355-1369},\n      doi = {10.1093/mnras/stab947},\n   eprint = {2102.04841},\n   adsurl = {https://ui.adsabs.harvard.edu/abs/2021MNRAS.504.1355V},\n}\n```\n\n## Quick overview\n\nBALRoGO has nine modules that perform different tasks:\n\n- ***angle.py*** : This module contains the main functions concerning angular tansformations, sky projections and spherical trigonomtry.\n- ***gaia.py*** : This module contains the main functions concerning the handling of the Gaia mission data.\n- ***hrd.py*** : This module contains the main functions concerning the color magnitude diagram (CMD). It provides a Kernel Density Estimation (KDE) of the CMD distribution.\n- ***marginals.py*** : This module is based on the Python corner package (Copyright 2013-2016 Dan Foreman-Mackey & contributors, The Journal of Open Source Software): https://joss.theoj.org/papers/10.21105/joss.00024\nI have done some modifications on it so it allows some new features and so it takes into account some choices as default. I thank Gary Mamon for his good suggestions concerning the plot visualization.\n-  ***parallax.py*** : This module contains the main functions concerning parallax information. It provides a kernel density estimation of the distance distribution, as well as a fit of the mode of this distribution.\n- ***pm.py*** : This module contains the main functions concerning proper motion data. It provides MCMC and maximum likelihood fits of proper motions data, as well as robust initial guesses for those fits.\n- ***position.py*** : This module contains the main functions concerning positional information. It provides MCMC and maximum likelihood fits of surface density, as well as robust initial guesses for the (RA,Dec) center of the source.\n- ***mock.py*** : This module handles mock data sets. It converts 3D coordinates to sky coordinates and is able to add realistic errors to proper motions. It is also able to generate Milky Way interlopers.\n- ***dynamics.py*** : This module handles conversions from celestial coordinates to plane of sky coordinates (vPOSr,vPOSt), as well as allows computation of dispersion profiles in different ways. Also computes the velocity anisotropy from cartesian data.\n\n## Installation\n\nBALRoGO is available through [pip](https://pypi.org/project/balrogo/). The quickiest way to install it is to type the following command in your terminal:\n\n```terminal\npip install balrogo\n```\n\nIf you are using [Anaconda](https://www.anaconda.com/), you might want to install it directly in your Anaconda bin path:\n\n```terminal\ncd path/anaconda3/bin/\npip install balrogo\n```\n\nFor updated versions of the code, you can do the same as above, but instead of using `pip install balrogo`, you should type:\n\n```terminal\npip install --upgrade balrogo\n```\n\n### Using BALRoGO on [*Gaia*](https://www.cosmos.esa.int/web/gaia/data-access) data\n\nFor quick tutorial of BALRoGO applied to *Gaia* data, please click [here](https://gitlab.com/eduardo-vitral/balrogo/-/blob/master/GAIA.md).\n\n## License\n\nCopyright (c) 2020 Eduardo Vitral & Alexandre Macedo.\n\nBALRoGO is free software made available under the [MIT License](LICENSE). The BALRoGO logo is licensed under a [Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).\n',
     'author': 'Eduardo Vitral',
     'author_email': 'vitral@iap.fr',
     'maintainer': None,
     'maintainer_email': None,
     'url': 'https://gitlab.com/eduardo-vitral/balrogo',
```

### Comparing `balrogo-1.6.4/PKG-INFO` & `balrogo-1.6.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: balrogo
-Version: 1.6.4
+Version: 1.6.5
 Summary: Bayesian Astrometric Likelihood Recovery of Galactic Objects
 Home-page: https://gitlab.com/eduardo-vitral/balrogo
 License: MIT
 Author: Eduardo Vitral
 Author-email: vitral@iap.fr
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

