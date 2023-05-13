# Comparing `tmp/geonum-1.4.5rc1.tar.gz` & `tmp/geonum-1.5.0.dev9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "geonum-1.4.5rc1.tar", last modified: Wed Feb 24 17:07:18 2021, max compression
+gzip compressed data, was "geonum-1.5.0.dev9.tar", last modified: Sat May 13 11:22:18 2023, max compression
```

## Comparing `geonum-1.4.5rc1.tar` & `geonum-1.5.0.dev9.tar`

### file list

```diff
@@ -1,37 +1,46 @@
-drwxr-xr-x   0 jonasg   (421188) jonasg   (421188)        0 2021-02-24 17:07:18.380554 geonum-1.4.5rc1/
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)    35141 2020-01-23 08:55:25.000000 geonum-1.4.5rc1/LICENSE
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)      110 2020-01-23 08:55:25.000000 geonum-1.4.5rc1/MANIFEST.in
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     7166 2021-02-24 17:07:18.380554 geonum-1.4.5rc1/PKG-INFO
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     5704 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/README.rst
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)       10 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/VERSION.rst
-drwxr-xr-x   0 jonasg   (421188) jonasg   (421188)        0 2021-02-24 17:07:18.380554 geonum-1.4.5rc1/geonum/
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     2772 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/__init__.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)    18318 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/atmosphere.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     1038 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/conftest.py
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)    16494 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/elevationprofile.py
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)      946 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/exceptions.py
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)    22189 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/geopoint.py
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)    25367 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/geosetup.py
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)     8812 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/geovector3d.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     5997 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/helpers.py
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)    37381 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/mapping.py
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)     6837 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/processing.py
-drwxr-xr-x   0 jonasg   (421188) jonasg   (421188)        0 2021-02-24 17:07:18.380554 geonum-1.4.5rc1/geonum/test/
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)        0 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/test/__init__.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)    10713 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/test/test_atmosphere.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     1496 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/test/test_base_classes.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     1309 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/test/test_elevationprofile.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     2240 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/test/test_helpers.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)      748 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/test/test_srtm_access.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)      595 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/test/test_srtmpy_lib.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     1140 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/test/test_topodata.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)    22012 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/topoaccessbase.py
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)    12475 2021-02-24 17:03:04.000000 geonum-1.4.5rc1/geonum/topodata.py
--rwxr-xr-x   0 jonasg   (421188) jonasg   (421188)     5151 2020-01-23 08:55:28.000000 geonum-1.4.5rc1/geonum/topodataaccess.py
-drwxr-xr-x   0 jonasg   (421188) jonasg   (421188)        0 2021-02-24 17:07:18.380554 geonum-1.4.5rc1/geonum.egg-info/
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     7166 2021-02-24 17:07:18.000000 geonum-1.4.5rc1/geonum.egg-info/PKG-INFO
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)      709 2021-02-24 17:07:18.000000 geonum-1.4.5rc1/geonum.egg-info/SOURCES.txt
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)        1 2021-02-24 17:07:18.000000 geonum-1.4.5rc1/geonum.egg-info/dependency_links.txt
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)        7 2021-02-24 17:07:18.000000 geonum-1.4.5rc1/geonum.egg-info/top_level.txt
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)       38 2021-02-24 17:07:18.380554 geonum-1.4.5rc1/setup.cfg
--rw-r--r--   0 jonasg   (421188) jonasg   (421188)     2170 2021-02-24 17:06:04.000000 geonum-1.4.5rc1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:22:18.418721 geonum-1.5.0.dev9/
+-rw-r--r--   0 runner    (1001) docker     (123)    35141 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1445 2023-05-13 11:22:18.414720 geonum-1.5.0.dev9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      834 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:22:18.414720 geonum-1.5.0.dev9/geonum/
+-rw-r--r--   0 runner    (1001) docker     (123)     1508 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/_init_helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17180 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/atmosphere.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1027 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26403 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/elevationprofile.py
+-rw-r--r--   0 runner    (1001) docker     (123)      974 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23189 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/geopoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27825 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/geosetup.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11325 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/geovector3d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6928 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6945 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/lineongrid.py
+-rw-r--r--   0 runner    (1001) docker     (123)    36515 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/mapping.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6743 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/plot_helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18351 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/topoaccessbase.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13699 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/topodata.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5108 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/topodataaccess.py
+-rw-r--r--   0 runner    (1001) docker     (123)      471 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/geonum/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:22:18.414720 geonum-1.5.0.dev9/geonum.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1445 2023-05-13 11:22:18.000000 geonum-1.5.0.dev9/geonum.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      873 2023-05-13 11:22:18.000000 geonum-1.5.0.dev9/geonum.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:22:18.000000 geonum-1.5.0.dev9/geonum.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-13 11:22:18.000000 geonum-1.5.0.dev9/geonum.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 11:22:18.418721 geonum-1.5.0.dev9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1360 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:22:18.414720 geonum-1.5.0.dev9/test/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10776 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_atmosphere.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1561 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_base_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8819 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_elevationprofile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8476 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_geopoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12595 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_geosetup.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1365 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_geovector3d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2250 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1089 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_lineongrid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1210 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_plot_helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_srtmpy_lib.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3584 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_topoaccessbase.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4066 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_topodata.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_topodataaccess.py
+-rw-r--r--   0 runner    (1001) docker     (123)      459 2023-05-13 11:22:07.000000 geonum-1.5.0.dev9/test/test_utils.py
```

### Comparing `geonum-1.4.5rc1/LICENSE` & `geonum-1.5.0.dev9/LICENSE`

 * *Files identical despite different names*

### Comparing `geonum-1.4.5rc1/geonum/atmosphere.py` & `geonum-1.5.0.dev9/geonum/atmosphere.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-# -*- coding: utf-8 -*-
-#
 # Geonum is a Python library for geographical calculations in 3D
 # Copyright (C) 2017 Jonas Gliss (jonasgliss@gmail.com)
 #
 # This program is free software: you can redistribute it and/or
 # modify it under the terms of the GNU General Public License a
 # published by the Free Software Foundation, either version 3 of
 # the License, or (at your option) any later version.
@@ -12,125 +10,127 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
 # General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program. If not, see <http://www.gnu.org/licenses/>.
 
-"""
-Module for atmospheric calculations relevant for geonum
-"""
-
-from numpy import deg2rad, cos, ndarray, meshgrid, pi, exp, log
+import numpy as np
 
-#: Pressure at sea level [Pa]
+#: Pressure at sea level, Unit [Pa]
 p0 = 101325.0
 
-#: Avogadro constant [mol-1]
+#: Avogadro constant, Unit [mol-1]
 NA = 6.022140857e+23
 
-#: Standard sea level temperature [K]
+#: Standard sea level temperature, Unit [K]
 T0_STD = 288.15
 
-#: Average molar mass of air, Unit: [g mol-1]
+#: Average molar mass of air, Unit [g mol-1]
 M_AIR_AVG = 28.9645
 
-#: Gas constant (U.S. standard atmosphere) [Nm mol-1 K-1]
+#: Gas constant (U.S. standard atmosphere), Unit [Nm mol-1 K-1]
 R_STD = 8.31432
 
-#: Atmospheric lapse rate (Standard atmosphere) [K m-1]
+#: Atmospheric lapse rate (Standard atmosphere), Unit [K m-1]
 L_STD_ATM = -6.5e-3
-#: Atmospheric lapse rate (dry atmosphere) [K m-1]
+#: Atmospheric lapse rate (dry atmosphere), Unit [K m-1]
 L_DRY_AIR = -9.8e-3
 
+
 def _g0(phi=0.0):
     """Gravitational accelaration at sea level (function of latitude)
 
     From Bodhaine et al., 1999, *On Rayleigh Optical Depth Calculations*
 
 
     Parameters
     ----------
-    phi : float or ndarray
+    phi : float or np.ndarray
         latitude(s) in rads
 
     Returns
     -------
-    float or ndarray
-        value(s) of Earth gravitational accelaration at sea level for input
+    float or np.ndarray
+        value(s) of Earth gravitational acceleration at sea level for input
         latitude(s)
     """
-    return 9.806160 * (1 - 0.0026373 * cos(2 * phi)
-                         + 0.0000059 * cos(2 * phi)**2)
+    return 9.806160 * (1 - 0.0026373 * np.cos(2 * phi)
+                       + 0.0000059 * np.cos(2 * phi) ** 2)
+
 
 def _g_acc(phi, alt):
-    return (_g0(phi) - (3.085e-4  + 2.27e-7 * cos(2 * phi)) * alt
-                     + (7.254e-11 + 1e-13   * cos(2 * phi)) * alt ** 2
-                     + (1.517e-17 + 6e-20   * cos(2 * phi)) * alt ** 3)
+    return (_g0(phi) - (3.085e-4 + 2.27e-7 * np.cos(2 * phi)) * alt
+            + (7.254e-11 + 1e-13 * np.cos(2 * phi)) * alt ** 2
+            + (1.517e-17 + 6e-20 * np.cos(2 * phi)) * alt ** 3)
+
 
 def g(lat=45.0, alt=0.0):
     """Gravitational accelaration as function of latitude and altitude
 
     From Bodhaine et al., 1999, *On Rayleigh Optical Depth Calculations* who
     have it from `List et al. 1968 <http://agris.fao.org/agris-search/search.
     do?recordID=US201300011727>`_.
 
     Parameters
     ----------
-    lat : float or ndarray
+    lat : float or np.ndarray
         latitude(s) in degrees
-    alt : float or ndarray
+    alt : float or np.ndarray
         altitude(s) in m
 
     Returns
     -------
-    float or ndarray
-        value(s) of Earth gravitational accelaration at sea level for input
+    float or np.ndarray
+        Value(s) of Earth gravitational accelaration at sea level for input
         latitude(s) and altitude(s). If both inputs are arrays, then a 2D array
         is returned with the first axis (index 0) corresponding to altitudes
         and second axis to latitude
 
     Examples
     --------
 
     >>> import geonum
+    >>> import numpy as np
     >>> lats = np.linspace(0, 90, 200)
     >>> alts = np.linspace(0, 1000, 100)
     >>> dat = geonum.atmosphere.g(lats, alts)
     >>> dat.shape
     (100, 200)
     """
-    phi = deg2rad(lat)
-    if all([isinstance(x, ndarray) for x in [phi, alt]]):
-        phi, alt = meshgrid(phi, alt)
+    phi = np.deg2rad(lat)
+    if all([isinstance(x, np.ndarray) for x in [phi, alt]]):
+        phi, alt = np.meshgrid(phi, alt)
 
     return _g_acc(phi, alt)
 
+
 def g0(lat=45.0):
     """Gravitational accelaration at sealevel as function of latitude
 
     See also :func:`g` for details
 
     Parameters
     ----------
-    lat : float or ndarray
+    lat : float or np.ndarray
         latitude(s) in degrees
-    alt : float or ndarray
+    alt : float or np.ndarray
         altitude(s) in m
 
     Returns
     -------
-    float or ndarray
-        value(s) of Earth gravitational accelaration at sea level for input
+    float or np.ndarray
+        Value(s) of Earth gravitational accelaration at sea level for input
         latitude(s) and altitude(s). If both inputs are arrays, then a 2D array
         is returned with the first axis (index 0) corresponding to altitudes
         and second axis to latitude
     """
     return g(lat, alt=0.0)
 
+
 def temperature(alt=0.0, ref_temp=T0_STD, ref_alt=0.0, lapse_rate=L_STD_ATM):
     """Get temperature for a certain altitude (or altitude array)
 
     **Formula:**
 
     .. math::
 
@@ -141,37 +141,38 @@
         - :math:`$T_{ref}$` is a reference temperature
         - :math:`$L$` is the atmospheric lapse-rate
         - :math:`$h$` is the altitude in m
         - :math:`$h_{ref}$` is a reference altitude
 
     Parameters
     ----------
-    alt : float or ndarray
+    alt : float or np.ndarray
         altitude(s) in m
     ref_temp : float, optional
         reference temperature in K (default is std atm sea level)
     ref_alt : float, optional
         altitude corresponding to reference temperature (in m)
     lapse_rate : float, optional
         atmospheric lapse rate (in K m-1)
 
     Returns
     -------
-    float or ndarray
-        temperature(s) in K corresponding to altitudes
+    float or np.ndarray
+        Temperature(s) in K corresponding to altitudes
     """
     return float(ref_temp) + float(lapse_rate) * (alt - float(ref_alt))
 
+
 def beta_exp(mol_mass=M_AIR_AVG, lapse_rate=L_STD_ATM, lat=45.0):
     """Exponent for conversion of atmosperic temperatures and pressures
 
     Based on barometric height formula (see e.g. `wikipedia <https://en.
     wikipedia.org/wiki/Barometric_formula>`__) for details.
 
-    **Formula: **
+    **Formula:**
 
     .. math::
 
         \\beta\,=\,\\frac{g_0 M_{air}}{R L}
 
     where:
 
@@ -192,14 +193,15 @@
     Returns
     -------
     float
         Beta Exponent for formula
     """
     return g0(lat) * mol_mass / (1000 * R_STD * lapse_rate)
 
+
 def pressure(alt=0.0, ref_p=p0, ref_temp=T0_STD, ref_alt=0.0,
              lapse_rate=L_STD_ATM, mol_mass=M_AIR_AVG, lat=45.0):
     """Get atmospheric pressure in units of Pascal
 
     **Formula:**
 
     .. math::
@@ -212,77 +214,65 @@
         - :math:`$p_{ref}$` is a reference pressure
         - :math:`$T$` is the temperature  (cf. :func:`temperature`)
         - :math:`$T_{ref}$` is a reference temperature
         - :math:`$L_{ref}$` is the atmospheric lapse-rate
         - :math:`$h$` is the altitude in m
         - :math:`$h_{ref}$` is a reference altitude
 
-
-
     Parameters
     ----------
-    alt : float or ndarray
+    alt : float or np.ndarray
         altitude(s) in m
     ref_p : float, optional
         reference pressure (default is std atm sea level)
     ref_temp : float, optional
         reference temperature in K corresponding to `ref_p`
         (default is std atm sea level)
     ref_alt : float, optional
         altitude corresponding to `ref_p`
     lapse_rate : float, optional
-        atmospheric lapse rate (in K / m)
+        atmospheric lapse rate (in K m-1)
     mol_mass : float, optional
-        molar mass of air
+        molar mass of air (in g mol-1)
     lat : float, optional
-        latitude for calculation of gravitational constant
+        latitude in decimal degrees for calculation of gravitational constant
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         pressure(s) corresponding to input altitude(s)
     """
     temp = temperature(alt, ref_temp, ref_alt, lapse_rate)
     exp = beta_exp(mol_mass, lapse_rate, lat)
     return ref_p * (ref_temp / temp) ** exp
 
+
 def pressure_hPa(alt=0.0, *args, **kwargs):
     """Calls :func:`pressure` using provided input and returns in unit of hPa
 
     Defaults to standard atmosphere. This can be changed using further input
     parameters, for details see :func:`pressure`.
 
     Parameters
     ----------
-    alt : float or ndarray
+    alt : float or np.ndarray
         altitude(s) in m
-    ref_p : float, optional
-        reference pressure (default is std atm sea level)
-    ref_temp : float, optional
-        reference temperature in K corresponding to `ref_p`
-        (default is std atm sea level)
-    ref_alt : float, optional
-        altitude corresponding to `ref_p`
-    lapse_rate : float, optional
-        atmospheric lapse rate (in K / m)
-    mol_mass : float, optional
-        molar mass of air
-    lat : float, optional
-        latitude for calculation of gravitational constant
-    temp : float, optional
-        if unspecified (default), the temperature is calculated using
-        :func:`temperature`
+    *args
+        non-keyword args parsed to :func:`pressure`
+    **kwargs
+        keyword args parsed to :func:`pressure`
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         pressure(s) in units of hPa corresponding to input altitude(s)
     """
     return pressure(alt, *args, **kwargs) / 100
 
+
 def pressure2altitude(p, ref_p=p0, ref_temp=T0_STD, ref_alt=0.0,
                       lapse_rate=L_STD_ATM, mol_mass=M_AIR_AVG, lat=45.0):
     """General formula to convert atm. pressure to altitude
 
     **Formula:**
 
     .. math::
@@ -327,18 +317,20 @@
     >>> import geonum.atmosphere as atm
     >>> p = atm.pressure(2000) # pressure at 2000 m standard atm
     >>> int(atm.pressure2altitude(p))
     2000
     """
 
     beta = beta_exp(mol_mass, lapse_rate, lat=lat)
-    return (ref_temp / lapse_rate * (exp(-log(p / ref_p) / beta) - 1) + ref_alt)
+    return (ref_temp / lapse_rate * (
+                np.exp(-np.log(p / ref_p) / beta) - 1) + ref_alt)
+
 
 def air_density(alt=0.0, temp=None, ref_p=p0, ref_temp=T0_STD, ref_alt=0.0,
-            lapse_rate=L_STD_ATM, mol_mass=M_AIR_AVG, lat=45.0):
+                lapse_rate=L_STD_ATM, mol_mass=M_AIR_AVG, lat=45.0):
     """Get atmospheric density in units of :math:`$g\,m^-3$`
 
     **Formula:**
 
     .. math::
 
         \\rho = p \\cdot \\frac{M_{Air}} {RT} \\quad \\left[ \\frac{g}{m^-3} \\right]
@@ -348,15 +340,15 @@
         - :math:`$p$` is the atm. pressure (cf. :func:`pressure`)
         - :math:`$M_{Air}$` is the molar mass of air (defaults to standard atm)
         - :math:`$R$` is the gas constant (:attr:`R_STD`)
         - :math:`$T$` is the temperature  (cf. :func:`temperature`)
 
     Parameters
     ----------
-    alt : float or ndarray
+    alt : float or np.ndarray
         altitude(s) in m
     temp : float, optional
         temperature in K, if None, :func:`temperature` is used to compute
         temperature.
     ref_p : float, optional
         reference pressure (default is std atm sea level)
     ref_temp : float, optional
@@ -369,29 +361,31 @@
     mol_mass : float, optional
         molar mass of air
     lat : float, optional
         latitude for calculation of gravitational constant
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         density corresponding to input altitude (in g m-3)
     """
     if temp is None:
         temp = temperature(alt, ref_temp, ref_alt, lapse_rate)
-    p = pressure(alt, ref_p, ref_temp, ref_alt, lapse_rate,mol_mass, lat)
+    p = pressure(alt, ref_p, ref_temp, ref_alt, lapse_rate, mol_mass, lat)
     return p * mol_mass / (R_STD * temp)
 
-def air_number_density(alt=0.0, temp=None, ref_p=p0, ref_temp=T0_STD, ref_alt=0.0,
-                   lapse_rate=L_STD_ATM, mol_mass=M_AIR_AVG, lat=45.0):
+
+def air_number_density(alt=0.0, temp=None, ref_p=p0, ref_temp=T0_STD,
+                       ref_alt=0.0, lapse_rate=L_STD_ATM,
+                       mol_mass=M_AIR_AVG, lat=45.0):
     """Get atmospheric number density in m-3
 
     Parameters
     ----------
-    alt : float or ndarray
+    alt : float or np.ndarray
         altitude(s) in m
     temp : float, optional
         temperature in K, if None, :func:`temperature` is used to compute
         temperature.
     ref_p : float, optional
         reference pressure (default is std atm sea level)
     ref_temp : float, optional
@@ -404,195 +398,174 @@
     mol_mass : float, optional
         molar mass of air
     lat : float, optional
         latitude for calculation of gravitational constant
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         number density of air in #particles m-3 corresponding to altitude
     """
-    rho = air_density(alt, temp, ref_p, ref_temp, ref_alt, lapse_rate, mol_mass, lat)
+    rho = air_density(alt, temp, ref_p, ref_temp, ref_alt, lapse_rate,
+                      mol_mass, lat)
     return rho * NA / mol_mass
 
+
 def refr_idx_300ppm_co2(lbda_mu=0.300):
     """Get refractive index of air using eq. of Peck and Reeder, 1972
 
     Uses either of two parametrisations for wavelengths above or below 0.23
     microns using parametrisations from `Peck and Reeder, 1972, Dispersion of
     air <https://www.osapublishing.org/josa/abstract.cfm?uri=josa-62-8-958>`_.
 
     Parameters
     ----------
-    lbda_mu : float or ndarray
+    lbda_mu : float or np.ndarray
         wavelength in microns
 
     Returns
     -------
     float
         refractive index
     """
     if lbda_mu >= 0.23:
         return 1 + (5791817 / (238.0185 - (1 / lbda_mu) ** 2) +
-                    167909  / (57.362   - (1 / lbda_mu) ** 2)
-                   ) * 10 ** (-8)
-    else:
-        return 1 + (8060.51 +
-                    2480990 / (132.274  - (1 / lbda_mu) ** 2) +
-                    17455.7 / (39.32957 - (1 / lbda_mu) ** 2)
-                   ) * 10 ** (-8)
+                    167909 / (57.362 - (1 / lbda_mu) ** 2)
+                    ) * 10 ** (-8)
+
+    return 1 + (8060.51 +
+                2480990 / (132.274 - (1 / lbda_mu) ** 2) +
+                17455.7 / (39.32957 - (1 / lbda_mu) ** 2)
+                ) * 10 ** (-8)
+
 
 def refr_idx(lbda_mu=0.300, co2_ppm=400.0):
     """Calculate refr. index of atm for varying CO2 amount
 
     Uses either of two parametrisations for wavelengths above or below 0.23
     microns from `Peck and Reeder, 1972, Dispersion of
     air <https://www.osapublishing.org/josa/abstract.cfm?uri=josa-62-8-958>`_
     to retrieve the refractive index for CO2 concentrations at 300ppm and
     the parametrisation for varying CO2 amounts from Bodhaine et al., 1999,
     *On Rayleigh Optical Depth Calculations*.
 
     Parameters
     ----------
-    lbda_mu : float or ndarray
+    lbda_mu : float or np.ndarray
         wavelength in micrometers
     co2_ppm : float
         atmospheric CO2 volume mixing ratio in ppm
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         refractive index
     """
     n_300 = refr_idx_300ppm_co2(lbda_mu)
-    return 1 + (n_300 - 1) * (1 + 0.54 * (co2_ppm * 10**(-6) - 0.0003))
+    return 1 + (n_300 - 1) * (1 + 0.54 * (co2_ppm * 10 ** (-6) - 0.0003))
+
 
 def _F_N2(lbda_mu=0.300):
     """Depolarisation factor of N2 for Rayleigh scattering cross section
 
     Taken from `Bates 1984 <http://www.sciencedirect.com/science/article/pii/
     0032063384901028>`_
 
     Parameters
     ----------
-    lbda_mu : float or ndarray
+    lbda_mu : float or np.ndarray
         wavelength in micrometers
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         depolarisation factor of N2
     """
     return 1.034 + 3.17e-4 / lbda_mu ** 2
 
+
 def _F_O2(lbda_mu=0.300):
     """Depolarisation factor of O2 for Rayleigh scattering cross section
 
     Taken from `Bates 1984 <http://www.sciencedirect.com/science/article/pii/
     0032063384901028>`_
 
     Parameters
     ----------
-    lbda_mu : float or ndarray
+    lbda_mu : float or np.ndarray
         wavelength in micrometers
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         depolarisation factor of O2
 
     """
-    return 1.096 + 1.385e-3 / lbda_mu ** 2 + 1.448e-4 / lbda_mu**4
+    return 1.096 + 1.385e-3 / lbda_mu ** 2 + 1.448e-4 / lbda_mu ** 4
+
 
 def F_AIR(lbda_mu=0.300, co2_ppm=400.0):
     """Depolarisation factor of air for Rayleigh scattering cross section
 
     Taken from Bodhaine et al., 1999, *On Rayleigh Optical Depth Calculations*
 
     Parameters
     ----------
-    lbda_mu : float or ndarray
+    lbda_mu : float or np.ndarray
         wavelength in micrometers
     co2_ppm : float
         atmospheric CO2 volume mixing ratio in ppm
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         depolarisation factor of O2
     """
-    co2 = co2_ppm * 10**(-6)
+    co2 = co2_ppm * 10 ** (-6)
     return (78.084 * _F_N2(lbda_mu) +
             20.946 * _F_O2(lbda_mu) +
             0.934 + co2 * 1.15) / (78.084 + 20.946 + 0.934 + co2)
 
+
 def sigma_rayleigh(lbda_mu=0.300, co2_ppm=400.0):
     """Rayleigh scattering cross section
 
     Parameters
     ----------
     lbda_mu : float
         wavelength in micrometers
     co2_ppm : float
         atmospheric CO2 volume mixing ratio in ppm
 
     Returns
     -------
     float
-        value of Rayleigh scattering cross section in cm-2
+        value of Rayleigh scattering cross section in cm2
     """
     n = refr_idx(lbda_mu, co2_ppm)
-    lbda = lbda_mu * 10**(-6)
-    num_dens = number_density()
-    refr_fac = (n**2 - 1)**2 / (n**2 + 2)**2
+    lbda = lbda_mu * 10 ** (-6)
+    num_dens = air_number_density()
+    refr_fac = (n ** 2 - 1) ** 2 / (n ** 2 + 2) ** 2
     F = F_AIR(lbda_mu, co2_ppm)
-    return 24 * pi**3 / (lbda**4 * num_dens**2) * refr_fac * F * 100 ** 2
+    return 24 * np.pi ** 3 / (
+                lbda ** 4 * num_dens ** 2) * refr_fac * F * 100 ** 2
 
 
 def rayleigh_vol_sc_coeff(alt=0.0, lbda_mu=0.300, co2_ppm=400.0, **kwargs):
     """Rayleigh volume scattering coefficient :math:`\\beta(z,\\lambda)`
 
     Parameters
     ----------
-    alt : float or ndarray
+    alt : float or np.ndarray
         altitude(s) in m
     lbda_mu : float
         wavelength in micrometers
     co2_ppm : float
         atmospheric CO2 volume mixing ratio in ppm
 
     Returns
     -------
-    float or ndarray
+    float or np.ndarray
         vol. scattering coeff. in cm-1 corresponding to altitudes
     """
-    num_dens = number_density(alt, **kwargs) * 100**(-3) # cm^-3
-    return num_dens * sigma_rayleigh(lbda_mu, co2_ppm)
-
-### deprecated stuff
-def density(*args,**kwargs):
-    from warnings import warn
-    warn(DeprecationWarning(
-        'method geonum.atmosphere.density was renamed to '
-        'geonum.atmosphere.air_density, please use the new name'
-        ))
-    return air_density(*args, **kwargs)
-
-def number_density(*args,**kwargs):
-    from warnings import warn
-    warn(DeprecationWarning(
-        'method geonum.atmosphere.number_density was renamed to '
-        'geonum.atmosphere.air_number_density, please use the new name'
-        ))
-    return air_density(*args, **kwargs)
-
-if __name__ == '__main__':
-    print('No input temp')
-    print(density(0))
-
-    T1 = 273
-    print('input temp', T1)
-    print(density(0, temp=T1))
-
-    T2 = 253
-    print('input temp', T2)
-    print(density(0, temp=T2))
+    num_dens = air_number_density(alt, **kwargs) * 100 ** (-3)  # cm^-3
+    return num_dens * sigma_rayleigh(lbda_mu, co2_ppm)
```

### Comparing `geonum-1.4.5rc1/geonum/conftest.py` & `geonum-1.5.0.dev9/geonum/conftest.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,8 +1,10 @@
 # -*- coding: utf-8 -*-
+import matplotlib
+matplotlib.use('Agg')
 import pytest
 from contextlib import contextmanager
 from geonum import NETCDF_AVAILABLE
 
 
 # custom skipif marker that is used below for test functions that
 # require SRTM.py to be installed
@@ -28,10 +30,7 @@
 skip_netcdf4 = pytest.mark.skipif(NETCDF_AVAILABLE==False,
                                   reason='Skipping tests requiring NetCDF4 library.')
 
 
 @contextmanager
 def does_not_raise_exception():
     yield
-
-if __name__ == '__main__':
-    print(srtm_works())
```

### Comparing `geonum-1.4.5rc1/geonum/elevationprofile.py` & `geonum-1.5.0.dev9/geonum/topoaccessbase.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-# -*- coding: utf-8 -*-
-#
 # Geonum is a Python library for geographical calculations in 3D
 # Copyright (C) 2017 Jonas Gliss (jonasgliss@gmail.com)
 #
 # This program is free software: you can redistribute it and/or
 # modify it under the terms of the GNU General Public License a
 # published by the Free Software Foundation, either version 3 of
 # the License, or (at your option) any later version.
@@ -11,388 +9,485 @@
 # This program is distributed in the hope that it will be useful,
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
 # General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program. If not, see <http://www.gnu.org/licenses/>.
-import numpy as np
+
+import abc
+import os
 from warnings import warn
-from scipy.interpolate import interp1d
 
-from geonum.geopoint import GeoPoint
+import numpy as np
+import srtm
+
+from geonum import NETCDF_AVAILABLE, LOCAL_TOPO_DIR
+from geonum.exceptions import (TopoAccessError, SRTMNotCoveredError)
 
-class ElevationProfile(object):
-    """Class for calculating elevation profiles
-    
-    This class can be used to compute elevation profiles for arbitrary 
-    locations on earth. This is done by using topographic data which is 
-    provided (instance of :class:`geonum.TopoData`). Profiles are computed with respect to 
-    input location (:attr:`observer`) and the azimuthal direction of the 
-    profile is specified via the provided enpoint location (:attr:`endpoint`).
-    The profile is calculated between two :class:`GeoPoint` objects using a 
-    provided topographic data grid which must cover the range spanned by 
-    both points. 
+
+class TopoAccessBase(abc.ABC):
+    """Abstract base class for topgraphy file implementations
+
+    Defines minimum interface for derived access classes of different
+    topographic datasets.
     
-    Parameters
-    ----------
-    topo_data : TopoData 
-        topography data object
-    observer : :obj:`GeoPoint`
-        starting point of profile 
-    endpoint : :obj:`GeoPoint`
-        stop point of profile 
-    interpolate : bool
-        if True, the profile is interpolated to a certain horizontal resolution
-    resolution : float
-        desired grid resolution in m for interpolation. Interpolation is 
-        performed if :attr:`interpolate` is True and if the actual 
-        resolution of the topo data is smaller than input, else, nothing is done
-    itp_type : str
-        interpolation type (e.g. "linear", "cubic")
-    mapping_opts
-        additional keyword args that are passed to :func:`det_profile`
-    """        
-    def __init__(self, topo_data, observer, endpoint, interpolate=True, 
-                 resolution=5.0, itp_type="linear", **mapping_opts):
-     
-        self.topo_data = topo_data
-        self.observer = observer #: coordinate of observer (start of profile)
-        self.endpoint = endpoint #: coordinate of endpoint of profile
-        
-        self._observer_topogrid = None #: closest to observer on topo data grid
-        self._endpoint_topogrid = None #: closest to endpoint in topo data grid
-        
-        # In the following parameters the results will be stored
-        self.line = None
-        self.profile = None
-        self.dists = None
+    """
+    #: A coordinate for which data should be available
+    _TESTLAT = 45
+    _TESTLON = 15
+
+    @abc.abstractmethod
+    def get_data(self, lat0, lon0, lat1=None, lon1=None):
+        """Declaration of data access method
+
+        It is obligatory to implement this method into derived classes.
+
+        Parameters
+        ----------
+        lat0 : float
+            first latitude coordinate of topographic range (lower left coord)
+        lon0 : float
+            first longitude coordinate of topographic range (lower left coord)
+        lat1 : int or float, optional
+            second latitude coordinate of topographic range (upper right
+            coord). If None only data around lon0, lat0 will be extracted.
+        lon1 : int or float, optional
+            second longitude coordinate of topographic range (upper right
+            coord). If None only data around lon0, lat0 will be extracted.
+
+        Returns
+        -------
+        TopoData
+            instance of TopoData class
+        """
+        pass # pragma: no cover
 
+    def check_access(self):
+        """Check if topography data can be accessed"""
         try:
-            self.det_profile(interpolate, resolution, itp_type, **mapping_opts)
+            self.get_data(self._TESTLAT, self._TESTLON)
+            return True
         except Exception as e:
-            warn("Failed to compute elevation profile. Error msg: %s"
-                 %repr(e))
-        
-    @property
-    def dist_hor(self):
-        """Returns the horizontal distance between the 2 points"""
-        return (self._endpoint_topogrid - self._observer_topogrid).dist_hor
-        
-    
-    @property
-    def azimuth(self):
-        """Returns the azimuth angle of the profile"""
-        return (self._endpoint_topogrid - self._observer_topogrid).azimuth
-        
-    @property
-    def resolution(self):
-        """Get profile x (distance) resolution (averaged from distance array)
-        
-        Note
-        ----
-        Only works if profile was already determined
-            
-        """
-        return abs((self.dists[1:] - self.dists[:-1]).mean())
-    
-    @property
-    def gradient(self):
-        """Return gradient of profile
-        
-        Uses numpy function ``gradient``
-        """
-        return np.gradient(self.profile)
-    
-    @property
-    def slope(self):
-        """Returns slope of profile 
-        
-        Determines dx and dy arrays and returns slope vector::
-        
-            slope = dy / dx = gradient(self.profile) / 
-                (gradient(self.dists) * 1000.0)
-            
+            print('Could not access topodata: {}'.format(repr(e)))
+        return False
+
+    def _prep_borders(self, lat0, lon0, lat1, lon1):
+        """Sort by longitudes and determines LL and TR coordinates
+
+        Parameters
+        ----------
+        lat0 : float
+            first latitude coordinate of topographic range (lower left coord)
+        lon0 : float
+            first longitude coordinate of topographic range (lower left coord)
+        lat1 : float
+            second latitude coordinate of topographic range (upper right coord)
+        lon1 : float
+            second longitude coordinate of topographic range (upper right coord)
+
+        Returns
+        -------
+        tuple
+            4-element tuple, containing:
+
+            - float, smallest latitude (LL corner)
+            - float, smallest longitude (LL corner)
+            - float, largest latitude (TR corner)
+            - float, largest longitude (TR corner)
+        """
+        lats, lons = np.asarray([lat0, lat1]), np.asarray([lon0, lon1])
+        return (np.nanmin(lats), np.nanmin(lons),
+                np.nanmax(lats), np.nanmax(lons))
+
+    def _init_lons_lats(self, lats_all, lons_all, lat0, lon0, lat1=None,
+                        lon1=None):
+        """Get all latitudes and longitudes on a topodata grid
+
+        Parameters
+        ----------
+        lats_all : ndarray
+            numpy array containing available latitudes of the accessed topo
+            dataset
+        lons_all : ndarray
+            numpy array containing available longitudes of the accessed topo
+            dataset
+        lat0 : float
+            first latitude coordinate of topographic range (lower left coord)
+        lon0 : float
+            first longitude coordinate of topographic range (lower left coord)
+        lat1 : float, optional
+            second latitude coordinate of topographic range (upper right coord)
+        lon1 : float, optional
+            second longitude coordinate of topographic range (upper right coord)
+
+        Returns
+        -------
+        tuple
+            2-element tuple, containing
+
+            - ndarray, topodata latitudes overlapping with input range
+            - ndarray, topodata longitudes overlapping with input range
         """
-        return np.gradient(self.profile)/(np.gradient(self.dists)*1000)
-    
-    @property
-    def start_point(self):
-        """Return position of observer"""
-        return self.observer
-        
+        if any([x is None for x in [lat1, lon1]]):
+            lat1, lon1 = lat0, lon0
+
+        if lon0 > lon1:
+            lon0, lon1 = lon1, lon0
+        if lat0 > lat1:
+            lat0, lat1 = lat1, lat0
+
+        # closest indices
+        idx_lons = [np.argmin(abs(lons_all - lon0)),
+                    np.argmin(abs(lons_all - lon1))]
+        idx_lats = [np.argmin(abs(lats_all - lat0)),
+                    np.argmin(abs(lats_all - lat1))]
+
+        # Make sure that the retrieved indices actually INCLUDE the input ranges
+        if idx_lons[0] == 0 and lons_all[0] > lon0:
+            warn("Error: Lon0 smaller than range covered by file, using first"
+                 " available index in topodata..")
+            idx_lons[0] = 0
+        elif lons_all[idx_lons[0]] > lon0:
+            idx_lons[0] -= 1
+        if idx_lons[1] == len(lons_all) - 1 and lons_all[-1] < lon1:
+            warn("Error: Lon1 larger than range covered by file, using last"
+                 " available index in topodata..")
+            idx_lons[1] = len(lons_all) - 1
+        elif lons_all[idx_lons[1]] < lon1:
+            idx_lons[1] += 1
+        if idx_lats[0] == 0 and lats_all[0] > lat0:
+            warn("Error: Lat0 smaller than range covered by file, using first"
+                 " available index in topodata..")
+            idx_lats[0] = 0
+        elif lats_all[idx_lats[0]] > lat0:
+            idx_lats[0] -= 1
+        if idx_lats[1] == len(lats_all) - 1 and lats_all[-1] < lat1:
+            warn("Error: Lat1 larger than range covered by file, using last"
+                 " available index in topodata..")
+            idx_lats[1] = len(lats_all) - 1
+        elif lats_all[idx_lats[1]] < lat1:
+            idx_lats[1] += 1
+
+        return (lats_all[idx_lats[0]: idx_lats[1] + 1],
+                lons_all[idx_lons[0]: idx_lons[1] + 1],
+                idx_lats, idx_lons)
+
+
+class Etopo1Access(TopoAccessBase):
+    """A class representing netCDF4 data access of Etopo1 data
+
+    See `here <https://github.com/jgliss/geonum#supported-etopo1-files>`_ for
+    instructions on the data access.
+
+    Attributes
+    ----------
+    loader
+        data loader (:class:`netCDF4.Dataset`)
+
+    Parameters
+    ----------
+    local_path : str
+        directory where Etopo1 data files are stored
+    file_name :  str
+        file name of etopo data file
+    check_access : bool
+        if True, then access to topography data is checked on init and an
+        error is raised if no dataset can be accessed
+    search_database : bool
+        if True and topodata file :attr:`file_path` does not exist, then
+        a valid topography file is searched in all paths that are specified
+        in file `~/.geonum/LOCAL_TOPO_PATHS`.
+
+    Raises
+    ------
+    TopoAccessError
+        if input arg `check_access` is True and if no supported data file
+        can be found
+
+    """
+    #: ID of dataset
+    topo_id = "etopo1"
+
+    #: filenames of supported topographic datasets in preferred order
+    supported_topo_files = ["ETOPO1_Ice_g_gmt4.grd",
+                            "ETOPO1_Bed_g_gmt4.grd"]
+
+    def __init__(self, local_path=None, file_name=None, check_access=False,
+                 search_database=True):
+        if file_name is None:
+            file_name = "ETOPO1_Ice_g_gmt4.grd"
+        if not NETCDF_AVAILABLE: # pragma: no cover
+            raise ModuleNotFoundError(
+                "Etopo1Access class cannot be initiated. "
+                "Please install netCDF4 library first")
+        if local_path is None:
+            local_path = LOCAL_TOPO_DIR
+        self._local_path = local_path
+        self._file_name = file_name
+
+        from netCDF4 import Dataset
+
+        self.loader = Dataset
+
+        if not os.path.exists(self.file_path) and search_database:
+            self.search_topo_file_database()
+
+        # check if file exists
+        if check_access:
+            if not os.path.exists(self.file_path):
+                raise TopoAccessError('File {} could not be found in local '
+                                      'topo directory: {}'.format(
+                    self.file_name,
+                    self.local_path))
+            elif not self.check_access():
+                raise TopoAccessError('Failed to extract topography data for '
+                                      'Etopo dataset')
+
     @property
-    def min(self):
-        """Return minimum altitude in profile"""
-        return np.nanmin(self.profile)
-        
+    def local_path(self):
+        """Directory containing ETOPO1 gridded data files"""
+        return self._local_path
+
+    @local_path.setter
+    def local_path(self, val):
+        if not os.path.exists(val) or not os.path.isdir(val):
+            raise ValueError(f'Input directory {val} does not exist or is not '
+                             f'a directory...')
+        self._check_topo_path(val)
+        self._local_path = val
+
     @property
-    def max(self):
-        """Return maximum altitude in profile"""
-        return np.nanmax(self.profile)
-    
+    def file_name(self):
+        """File name of topographic dataset used"""
+        return self._file_name
+
+    @file_name.setter
+    def file_name(self, val):
+        if not val in self.supported_topo_files:
+            raise ValueError(
+                f'Invalid file name for Etopo1 dataset {val}. Valid filenames '
+                f'are: {self.supported_topo_files}')
+        self._file_name = val
+
     @property
-    def alt_range(self):
-        """Return altitude range of profile
-        """
-        return self.max - self.min
-    
-    def slope_angles(self, decimal_degrees=True):
-        """Returns slope angle of profile (in each sample point)
-        
-        :param bool decimal_degrees: rad or degrees (default True)
+    def file_path(self):
+        """Return full file path of current topography file"""
+        return os.path.join(self.local_path, self.file_name)
+
+    @file_path.setter
+    def file_path(self, val):
+        self.set_file_location(val)
+
+    def _check_topo_path(self, path):
+        """Check if path exists and if it is already included in database
+
+        Parameters
+        ----------
+        path : str
+            path to be checked
         """
-        a = np.tan(self.slope)
-        if decimal_degrees:
-            a = np.rad2deg(a)
-        return a
-        
-    def slope_angle(self, dist):
-        """Returns slope angle of profile at input distance
-        
-        :param float dist: distance in km
+        from geonum.helpers import check_and_add_topodir
+        check_and_add_topodir(path)
+
+    def _get_all_local_topo_paths(self):
+        """Get all search paths for topography files"""
+        from geonum.helpers import all_topodata_search_dirs
+        return all_topodata_search_dirs()
+
+    def _search_topo_file(self, path=None):
+        """Checks if a valid etopo data file can be found in local folder
+
+        Searches in ``self.local_path`` for any of the file names specified
+        in ``supported_topo_files``
+
         """
-        idx = np.argmin(abs(self.dists - dist))
-        return self.slope_angles()[idx]
-        
-    def det_profile(self, interpolate=True, resolution=5.0, itp_type="linear",
-                    **mapping_opts):
-        """Determines the elevation profile
-        
-        Searches the closest tiles in the topo data grid for both observer and
-        endpoint and based on these two points the elevation profile is
-        extracted using a :class:`LineOnGrid` object (which extracts altitudes 
-        from the topo data along the connection vector of the 2 points using 
-        2D spline intepolation)
-        
+        if path is None:
+            path = self.local_path
+        print(f'Searching valid topo file in folder: {path}')
+        fnames = os.listdir(path)
+        for name in fnames:
+            if name in self.supported_topo_files:
+                self.file_name = name
+                self.local_path = path
+                print(("Found match, setting current filepath: %s"
+                       % self.file_path))
+                return True
+        return False
+
+    def _find_supported_files(self):
+        """Look for all supported files in ``self.local_path```and return list"""
+        files = os.listdir(self.local_path)
+        lst = []
+        for name in files:
+            if name in self.supported_topo_files:
+                lst.append(name)
+        return lst
+
+    def search_topo_file_database(self):
+        """Checks if a valid topo file can be found in database"""
+        all_paths = self._get_all_local_topo_paths()
+        for path in all_paths:
+            if self._search_topo_file(path):
+                return True
+        return False
+
+    def get_data(self, lat0, lon0, lat1=None, lon1=None):
+        """Retrieve data from topography file
+
         Parameters
         ----------
-        interpolate : bool
-            if True, the profile is interpolated to a certain horizontal resolution
-        resolution : float
-            desired grid resolution in m for interpolation. Interpolation is 
-            performed if :attr:`interpolate` is True and if the actual 
-            resolution of the topo data is smaller than input, else, nothing is done
-        itp_type : str
-            interpolation type (e.g. "linear", "cubic")
-        **mapping_opts
-            additional keyword arguments that are passed to 
-            :func:`LineOnGrid.get_line_profile`
-        
+        lat0 : float
+            first latitude coordinate of topographic range (lower left coord)
+        lon0 : float
+            first longitude coordinate of topographic range (lower left coord)
+        lat1 : int or float, optional
+            second latitude coordinate of topographic range (upper right
+            coord). If None only data around lon0, lat0 will be extracted.
+        lon1 : int or float, optional
+            second longitude coordinate of topographic range (upper right
+            coord). If None only data around lon0, lat0 will be extracted.
+
         Returns
         -------
-        ndarray
-            the array containing the retrieved altitude levels along the 
-            retrieval direction (from the observer)
-        """
-        from geonum.processing import LineOnGrid
-        data = self.topo_data
-        idx_lon_0 = np.argmin(abs(data.lons - self.observer.lon.decimal_degree))
-        idx_lat_0 = np.argmin(abs(data.lats - self.observer.lat.decimal_degree))
-        idx_lon_1 = np.argmin(abs(data.lons - self.endpoint.lon.decimal_degree))
-        idx_lat_1 = np.argmin(abs(data.lats - self.endpoint.lat.decimal_degree))
-        
-        self.line = l = LineOnGrid(idx_lon_0, idx_lat_0, 
-                                   idx_lon_1, idx_lat_1)
-        
-        z = l.get_line_profile(data.data, **mapping_opts)
-        self._observer_topogrid = GeoPoint(data.lats[idx_lat_0],
-                                           data.lons[idx_lon_0], 
-                                           topo_data=data)
-        self._endpoint_topogrid = GeoPoint(data.lats[idx_lat_1],
-                                           data.lons[idx_lon_1], 
-                                           topo_data=data)
-        dists = np.linspace(0, self.dist_hor, l.length + 1)
-        if interpolate:
-            try:
-                res0 = (dists[1] - dists[0]) * 1000
-                fac = int(np.ceil(res0 / resolution))
-                if fac > 1:
-                    fz = interp1d(dists, z, kind=itp_type)
-                    dists = np.linspace(0, self.dist_hor, l.length * fac)
-                    z = fz(dists)
-            except Exception as e:
-                warn("Failed to perform interpolation of retrieved elevation "
-                     "profile. Error msg: %s" %repr(e))
-        self.dists = dists
-        self.profile = z
-        return z
-     
-    def get_altitudes_view_dir(self, elev_angle, view_above_topo_m=1.5):
-        """Get vector containing altitudes for a viewing direction 
-        
-        The viewing direction is specified by the azimuth angle of the 
-        connection vector between observer and endpoint, the elevation angle
-        needs to be specified via the input parameters, and the start point
-        (first elevation value) corresponds to the altitude at the observer
-        position plus an offset in m which can be specified.
-        
-        :param float elev_angle: elevation angle of viewing direction
-        :param float view_above_topo_m (1.5): altitude offset of start point 
-            in m
-        :return:
-            - vector with altitude values (same length as ``self.profile``)
-            
-        """
-        return (1000 * np.tan(np.radians(elev_angle)) * self.dists + 
-                self.profile[0] + view_above_topo_m)
-    
-    def find_horizon_elev(self, elev_start=0.0, elev_stop=60.0, step_deg=0.1,
-                          **kwargs):
-        """Find first elevation angle which does not intersect with topo
-        
-        :param float elev_start: start search elevation angle
-        :param float elev_stop: stop search elevation angle
-        :param float step_deg: angle step for search (coarser is faster)
-        :param **kwargs: additional keyword agruments passed to 
-            :func:`get_first_intersection`
+        TopoData
+            instance of TopoData class
         """
-        elevs = np.arange(elev_start, elev_stop + step_deg, step_deg)
-        elev_sects = []
-        dists_sects = []
-        for elev in elevs:
-            (dist, 
-             dist_err, 
-             intersect, 
-             view_elevations, 
-             _) = self.get_first_intersection(elev, **kwargs)
-            if dist is None:
-                return elev, elev_sects, dists_sects
-            else:
-                dists_sects.append(dist), elev_sects.append(elev)
-        raise Exception("Unexpected exception..")
-        
-    def get_first_intersection(self, elev_angle, view_above_topo_m=1.5,
-                               min_dist=None, local_tolerance=3, plot=False):
-                                
-        """Finds first intersection of a viewing direction with topography
-        
-        Start point of the viewing vector is the observer position (or more
-        accurately, the center position of the closest topography tile in 
-        the topography data set). The relative altitude of the start point 
-        with respect to the topography altitude at the observer position 
-        can be controlled on input (arg ``view_above_topo_m``) as well as 
-        the elevation angle of the viewing direction. The azimuth angle 
-        corresponds to the profile azimuth (i.e. azimuth between observer 
-        position and endpoint of this profile).
-        
-        The signal analysed for finding the intersection is a vector 
-        containing relative elevation positions of the viewing direction 
-        with respect to the profile altitude::
-        
-            diff_signal = self.get_altitudes_view_dir - self.profile
-            
-        The first intersection of the viewing direction with the topography
-        is identified by the first zero crossing of this ``diff_signal``.
-        
-        :param float elev_angle: elevation angle of viewing direction (in 
-            decimal degrees)
-        :param int view_above_topo_m: altitude offset of start point 
-            (``observer``) in m (default: 1.5)
-        :param float min_dist: minimum distance (in km) of first 
-            considered intersection with topography from observer. If None, 
-            use 1% of distance between ``observer`` and ``endpoint``.
-        :param float local_tolerance: tolerance factor to estimate 
-            distance uncertainty based on topo grid resolution  (default: 3)
-        :param bool plot: creates a plot of the profile including the
-            intersection information
+        from geonum import TopoData
+        etopo1 = self.loader(self.file_path)
 
-        
-        """
-         
-        if min_dist == None:
-            min_dist = self.dist_hor*.01
-        max_diff = self.resolution * 1000 
-        view_elevations = self.get_altitudes_view_dir(elev_angle,
-                                                      view_above_topo_m)
-        
-        #: determine the difference signal
-        diff_signal = view_elevations - self.profile 
-        #: First condition: consider only points in certain distance from observer
-        cond1 = self.dists > min_dist
-        #: Second condition: consider only "close to zero" points (this might be
-        #: redundant, I'll leave it for now because it works)
-        cond2 = abs(diff_signal) < max_diff 
-        
-        #: create array with all distances matching the 2 conditions
-        dists_0 = self.dists[cond1 * cond2] 
-        dist, dist_err, intersect = None, None, None
-        #: relax condition 2 if nothing was found 
-        if not len(dists_0) > 0:
-            max_diff = self.resolution * 1000 * local_tolerance
-            cond2 = abs(diff_signal) < max_diff
-            dists_0 = self.dists[cond1 * cond2]
-                   
-        try:
-            #: get all diff vals matching the 2 conditions
-            diff_vals = diff_signal[cond1 * cond2]
-            #: get the index of the first zero crossing
-            first_idx = np.where(np.diff(np.sign(diff_vals)))[0][0]
-            
-            #: get distance and local tolerance value
-            dist, tol = dists_0[first_idx], self.resolution * local_tolerance
-            #: make mask to access all distances within tolerance range
-            cond4 = np.logical_and(dist - tol <= dists_0, dist + tol >= dists_0)
-            #: estimate distance error from standard deviation of all 
-            #: distances within tolerance range
-            dist_err = dists_0[cond4].std()
-            
-            #: create geopoint corresponding to intersection
-            intersect = self._observer_topogrid.offset(self.azimuth, dist)
-            
-            #: set the altitude of this point (retrieved from profile)
-            intersect.altitude = self.get_altitude_at_distance(dist) # / 1000.
-           
-        except IndexError as e:
-            print(("No intersections could be detected, err: %s" %repr(e)))
-        
-        ax = None
-        if plot:
-            ax = self._plot_intersect_search_result(view_elevations, dist)
-            if dist == None:
-                dist = np.nan
-            ax.set_title("Azim: %.1f, Elev: %.1f, Intersect @ "
-                "dist =%.1f km" %(self.azimuth, elev_angle, dist))
-            
-        return dist, dist_err, intersect, view_elevations, ax
-    
-    def _plot_intersect_search_result(self, view_elevations, dist=None):
-        ax = self.plot()
-        ax.plot(self.dists, view_elevations, label = "Viewing direction")
-        try:
-            ax.axvline(dist, ls = "--", label = "Intersection")
-        except:
-            pass
-        ax.legend(loc="best", fancybox=True, framealpha=0.4)
-        return ax
-        
-        
-    def get_altitude_at_distance(self, dist):
-        """Returns altitude at a ceratain distance from observer
-        
-        :param float dist: horizontal distance from obsever along profile        
-        """
-        idx = np.argmin(abs(self.dists - dist))
-        return self.profile[idx]
-        
-    def __call__(self, dist):
-        """Returns altitude at a certain distance
-        
-        :param float dist: distance in km
+        lons = etopo1.variables["x"][:]
+        lats = etopo1.variables["y"][:]
+
+        lats, lons, idx_lats, idx_lons = self._init_lons_lats(lats, lons, lat0,
+                                                              lon0, lat1, lon1)
+
+        vals = np.asarray(etopo1.variables["z"][idx_lats[0]: idx_lats[1] + 1,
+                          idx_lons[0]: idx_lons[1] + 1],
+                          dtype=float)
+        etopo1.close()
+
+        return TopoData(lats, lons, vals, data_id=self.topo_id)
+
+
+class SRTMAccess(TopoAccessBase):
+    """Class for SRTM topographic data access
+
+    Uses library `srtm.py <https://pypi.python.org/pypi/SRTM.py/0.3.1>`_
+    for online access of data.
+
+    Note
+    ----
+    :mod:`srtm.py` downloads the topo data from `this source <http://
+    dds.cr.usgs.gov/srtm/version2_1/>`_ and stores a copy of the unzipped data
+    files in the current cache directory found in home.
+
+    Whenever data access is requested, the :mod:`srtm.py` checks if the file
+    already exists on the local machine and if not downloads it online. The
+    online access is rather slow, so do not be surprised, if things take a
+    while when accessing a specific location for the first time.
+
+    **Deleting cached SRTM files**:
+        use :func:`geonum.topoaccess.delete_all_local_srtm_files`
+
+    Parameters
+    ----------
+    check_access : bool
+        check if data can be accessed on class initialisation
+    **kwargs
+        additional keyword arguments that are passed through (irrelevant for
+        this class but relevant for factory loader class
+        :class:`TopoDataAccess`, particularly :func:`set_mode` therein.
+    """
+
+    def __init__(self, check_access=False, **kwargs):
+        """Class initialisation"""
+        self.loader = srtm
+        self.topo_id = "srtm"
+
+        if check_access:
+            self.check_access()
+
+    def _coordinate_covered(self, access_obj, lat, lon):
+        """Checks if SRTM data is available for input coordinate
+
+        Parameters
+        ----------
+        access_obj : GeoElevationData
+            data access object from :mod:`srtm.py` module
+            (can be created calling ``srtm.get_data()``)
+        lat : float
+            latitude of point
+        lon : float
+            longitude of point
+
+        Returns
+        -------
+        bool
+            True, if SRTM data is available for coordinate, else False.
         """
-        return self.get_altitude_at_distance(dist)
-        
-    def plot(self, ax = None):
-        """Plot the profile into an axis object
-        
-        :param ax: matplotlib axis object
+        if access_obj.get_file_name(lat, lon) is None:
+            return False
+        return True
+
+    def get_data(self, lat0, lon0, lat1=None, lon1=None):
+        """Load SRTM topographic subset for input range
+
+        Parameters
+        ----------
+        lat0 : float
+            first latitude coordinate of topographic range (lower left coord)
+        lon0 : float
+            first longitude coordinate of topographic range (lower left coord)
+        lat1 : int or float, optional
+            second latitude coordinate of topographic range (upper right
+            coord). If None only data around lon0, lat0 will be extracted.
+        lon1 : int or float, optional
+            second longitude coordinate of topographic range (upper right
+            coord). If None only data around lon0, lat0 will be extracted.
+
+        Returns
+        -------
+        TopoData
+            instance of TopoData class
         """
-        if ax is None:
-            from matplotlib.pyplot import subplots
-            fig, ax = subplots(1,1)
-        ax.fill_between(self.dists, self.profile, facecolor="#994d00",
-                        alpha=0.20)
-        ax.set_xlabel("Distance [km]")
-        ax.set_ylabel("Altitude [m]")
-        ax.set_ylim([self.min - .1 * self.alt_range, 
-                     self.max + .1 * self.alt_range])
-        return ax
+        from geonum import TopoData
+        print("Retrieving SRTM data (this might take a while) ... ")
+        # create GeoElevationData object for data access
+        dat = self.loader.get_data()
+        # check if second input point is specified and set equal first point if
+        # not
+        if any([x is None for x in [lat1, lon1]]):
+            lat1, lon1 = lat0, lon0
+        # Check if first point is covered by dataset
+        if not self._coordinate_covered(dat, lat0, lon0):
+            raise SRTMNotCoveredError('Point (lat={:.2f}, lon={:.2f}) not '
+                                      'covered by SRTM'.format(lat0, lon0))
+        # check if second point is covered by dataset
+        if not self._coordinate_covered(dat, lat1, lon1):
+            raise SRTMNotCoveredError('Endpoint coordinate (lat={:.2f}, '
+                                      'lon={:.2f}) not covered by SRTM'
+                                      .format(lat1, lon1))
+        # prepare borders of covered lon / lat regime
+        lat_ll, lon_ll, lat_tr, lon_tr = self._prep_borders(lat0, lon0,
+                                                            lat1, lon1)
+        # get SRTM file for lower left corner of regime
+        f_ll = dat.get_file(lat_ll, lon_ll)
+        # get SRTM file for top right corner of regime
+        f_tr = dat.get_file(lat_tr, lon_tr)
+        # create array of longitude values for regime
+        lons_all = np.linspace(f_ll.longitude, f_tr.longitude + 1,
+                               f_ll.square_side)
+        # create array of latitude values for regime
+        lats_all = np.linspace(f_ll.latitude, f_tr.latitude + 1,
+                               f_ll.square_side)
+        # prepare coordinates
+        lats, lons, _, _ = self._init_lons_lats(lats_all, lons_all,
+                                                lat0, lon0, lat1, lon1)
+        # Init data array
+        vals = np.ones((len(lats), len(lons))) * np.nan
+        # loop over all coordinates and try access the elevation data
+        for i in range(len(lats)):
+            for j in range(len(lons)):
+                vals[i, j] = dat.get_elevation(lats[i], lons[j])
+
+        return TopoData(lats, lons, vals, data_id=self.topo_id)
```

### Comparing `geonum-1.4.5rc1/geonum/exceptions.py` & `geonum-1.5.0.dev9/geonum/exceptions.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-# -*- coding: utf-8 -*-
-#
 # Geonum is a Python library for geographical calculations in 3D
 # Copyright (C) 2017 Jonas Gliss (jonasgliss@gmail.com)
 #
 # This program is free software: you can redistribute it and/or
 # modify it under the terms of the GNU General Public License a
 # published by the Free Software Foundation, either version 3 of
 # the License, or (at your option) any later version.
@@ -12,16 +10,21 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
 # General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program. If not, see <http://www.gnu.org/licenses/>.
 
-"""Custom exceptions of geonum"""
-class SRTMNotCoveredError(ValueError):
+class InvalidTopoMode(IOError):
     pass
 
-class TopoAccessError(IOError):
+class IntersectNotFound(ValueError):
     pass
 
-class InvalidTopoMode(IOError):
+class OutOfDomain(ValueError):
+    pass
+
+class SRTMNotCoveredError(ValueError):
+    pass
+
+class TopoAccessError(IOError):
     pass
```

### Comparing `geonum-1.4.5rc1/geonum/geopoint.py` & `geonum-1.5.0.dev9/geonum/geopoint.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-# -*- coding: utf-8 -*-
-#
 # Geonum is a Python library for geographical calculations in 3D
 # Copyright (C) 2017 Jonas Gliss (jonasgliss@gmail.com)
 #
 # This program is free software: you can redistribute it and/or
 # modify it under the terms of the GNU General Public License a
 # published by the Free Software Foundation, either version 3 of
 # the License, or (at your option) any later version.
@@ -12,528 +10,629 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
 # General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program. If not, see <http://www.gnu.org/licenses/>.
 
-from LatLon23 import LatLon, GeoVector
-    
-from numpy import (radians, cos, sin, degrees, sqrt,tan, isnan, arctan2,
-                   asarray, nanmin, nanmax)
+import numpy as np
+from LatLon23 import LatLon
+
+from geonum.exceptions import OutOfDomain
+from geonum.topodata import TopoData
+from geonum.topodataaccess import TopoDataAccess
 
-from warnings import warn
 
 class GeoPoint(LatLon):
-    """The Geopoint object represents a location in the atmosphere 
-    
-    This object is in 3D and includes elevation information.
-    
+    """The Geopoint object represents a location in the atmosphere
+
+    This object is in 3D and includes altitude information.
+
     Attributes
     ----------
     altitude : float
         altitude in m
     altitude_err : float
         uncertainty in altitude
     local_topo_path : str
         directory that is used to search for local topography if topodata is
         requested. Irrelevant for default topo
+
     Parameters
     ----------
-    lat : float 
-        latitude of point (decimal degrees)
-    lon : float 
-        longitude of point (decimal degrees)
-    altitude : float
-        elevation of point in m
-    name : str
-        name (ID) of this point
-    topo_access_mode : str
-        string specifying the current access mode for topographic data (in v1, 
-        choose between srtm or etopo1)
-    topo_path : str
-        specify path where etopo1 data files are stored
-    topo_data : TopoData 
-        existing topographic dataset that can be assigned to this point (can 
+    latitude : float, optional
+        latitude of point (decimal degrees), defaults to 0.
+    longitude : float, optional
+        longitude of point (decimal degrees), defaults to 0.
+    altitude : float, optional
+        elevation of point in m, defaults to 0.
+    name : str, optional
+        name (ID) of this point, defaults to undefined
+    topo_access_mode : str, optional
+        string specifying the current access mode for topographic data (in v1,
+        choose between srtm or etopo1), defaults to None, in which case default
+        of :class:`TopoDataAccess` is used if topographic data is accessed via
+        this point (e.g. if `auto_topo_access` is True). As of v1.4.X, default
+        access mode is srtm, which uses SRTM database, which does not have
+        full global coverage!
+    topo_path : str, optional
+        local path where local topography data is stored (at the moment only
+        relevant for topo_mode etopo1), defaults to None.
+    topo_data : TopoData, optional
+        existing topographic dataset that can be assigned to this point (can
         save time, e.g. for altitude access)
+    auto_topo_access : bool
+        if True, try set :attr:`altitude`and :attr:`altitude_err` based on
+        local topography (note that defa)
     """
-    _ALTERR_DEFAULT = 99999999999.9
-    def __init__(self, lat=0.0, lon=0.0, altitude=None, name="n/d",
-                 topo_access_mode="srtm", topo_path=None, topo_data=None,
-                 auto_topo_access=True):
-        
-        LatLon.__init__(self, float(lat), float(lon), name)
-        self.altitude = altitude #altitude in m
-        self.altitude_err = 0.0
-        
+    _ALTERR_DEFAULT = 1e9
+
+    def __init__(self, latitude=0, longitude=0, altitude=None, name=None,
+                 topo_access_mode=None, topo_path=None, topo_data=None,
+                 auto_topo_access=False):
+        if name is None:
+            name = 'undefined'
+        LatLon.__init__(self, float(latitude), float(longitude), name)
+        if altitude is None:
+            altitude = 0
+        elif auto_topo_access:  # altitude is not None
+            raise ValueError(
+                'either provide altitude or deactivate auto_topo_access'
+            )
+        self.altitude = altitude  # altitude in m
+        self.altitude_err = self._ALTERR_DEFAULT
+
         self.topo_access_mode = topo_access_mode
         self.local_topo_path = topo_path
-        
-        self.topo_data = None 
-        
+
+        self.topo_data = None
+
         if topo_data is not None:
             self.set_topo_data(topo_data)
-        
-        if self.altitude is None or isnan(self.altitude):
-            if auto_topo_access:
-                self.get_altitude()
-            else:
-                self.altitude = 0.0
-                self.altitude_err = self._ALTERR_DEFAULT
-    
+
+        if auto_topo_access:
+            self.set_topo_altitude()
+
     @property
-    def longitude(self):
+    def longitude(self) -> float:
         """Longitude coordinate in decimal degrees"""
         return self.lon.decimal_degree
 
     @property
-    def latitude(self):
+    def latitude(self) -> float:
         """Latitude coordinate in decimal degrees"""
         return self.lat.decimal_degree
-    
-    def offset(self, azimuth, dist_hor, dist_vert=0.0, ellipse="WGS84", 
-               **kwargs):
+
+    @property
+    def _topo_access(self) -> TopoDataAccess:
+        """Topography data access class"""
+        return TopoDataAccess(mode=self.topo_access_mode,
+                              local_path=self.local_topo_path)
+
+    def offset(self, azimuth, dist_hor, dist_vert=0.0, ellipse=None,
+               **kwargs) -> 'GeoPoint':
         """Returns new GeoPoint at offset position
-        
+
         Parameters
         -----------
         azimuth : float
-            azimuth direction angle (in decimal degrees, e.g. 90 for E 
+            azimuth direction angle (in decimal degrees, e.g. 90 for E
             direction, -90 or 270 for west)
-        dist_hor : float 
-            horizontal offset to this point in km 
-        dist_vert : float 
-            vertical offset to this point in m (positive if point is higher, 
+        dist_hor : float
+            horizontal offset to this point in km
+        dist_vert : float
+            vertical offset to this point in m (positive if point is higher,
             negative, if it is lower)
-        ellipse : float 
-            geodetic system (ellipsoid), default is "WGS84", i.e. 
+        ellipse : float
+            geodetic system (ellipsoid), default is "WGS84", i.e.
             `World Geodetic System <https://confluence.qps.nl/pages/view page.
             action?pageId=29855173>`__
-        **kwargs : 
-            additional keyword arguments passed to init of new 
+        **kwargs :
+            additional keyword arguments passed to init of new
             :class:`GeoPoint` object
-        
+
         Returns
         -------
         GeoPoint
             new location at offset position
         """
+        if ellipse is None:
+            ellipse = "WGS84"
         p = LatLon(self.lat.decimal_degree, self.lon.decimal_degree)
         p1 = p.offset(azimuth, dist_hor, ellipse)
         return GeoPoint(p1.lat.decimal_degree, p1.lon.decimal_degree,
                         self.altitude + dist_vert, **kwargs)
-    
+
     def set_topo_data(self, topo_data):
         """Assign topographic data to this point
-        
-        If input is valid, the topographic data set will be stored in 
+
+        If input is valid, the topographic data set will be stored in
         class attribute topo_data.
-        
+
         Parameters
         ----------
         topo_data : TopoData
             topography dataset
         """
-        from geonum.topodata import TopoData
         if not isinstance(topo_data, TopoData):
-            return
+            raise ValueError('need instance of geonum.TopoData')
         elif not topo_data.includes_coordinate(self.latitude, self.longitude):
-            raise TypeError("Could not assign topodata to GeoPoint %s: "
-             "topodata does not cover the coordinates" %self.name)
+            raise OutOfDomain(
+                f'Cannot assign input TopoData {topo_data} to {self}. '
+                f'The location of {self} are outside the borders of TopoData'
+            )
         self.topo_data = topo_data
-    
-    def range_borders(self, *points):
+
+    def range_borders(self, *points, extend_fac=0.1):
         """Get geographical borders (lower left, top right) of this point
-        
+
         Additional points can be included as non keyword arguments. The
         range borders are then determined under consideration of all
         specified points. If no additional points are specified,
-        the range corners will be set corresponding to 1km diagonal 
+        the range corners will be set corresponding to 1km diagonal
         distance to this point.
-        
+
         Parameters
         ----------
-        *points 
+        *points
             additional :class:`GeoPoint` objects to be  considered
-        
+        extend_fac : float
+            domain extension factor wrt to lat / lon span covered by input
+            points, defaults to 0.1 (ca 10% extension)
+
         Returns
         -------
-        2-element tuple, containing:
-            
-            - :class:`GeoPoint`, lower left corner of regime
-            - :class:`GeoPoint`, top right corner of regime
-        
+        GeoPoint
+            lower left corner of regime
+        GeoPoint
+            top right corner of regime
+
         """
         lats, lons = [self.latitude], [self.longitude]
-        #retrieve all latitudes and longitudes
+        # retrieve all latitudes and longitudes
         for p in points:
             if isinstance(p, GeoPoint):
                 lats.append(p.latitude)
                 lons.append(p.longitude)
-        lats, lons = asarray(lats), asarray(lons)
-        if not len(lats) > 0:
-            #print "Borders could not be initiated, no objects found..."
-            return False
-        lat_ll, lon_ll, lat_tr , lon_tr = (nanmin(lats), nanmin(lons), 
-                                           nanmax(lats), nanmax(lons))
+        lats, lons = np.asarray(lats), np.asarray(lons)
+
+        (lat_ll, lon_ll,
+         lat_tr, lon_tr) = (np.nanmin(lats), np.nanmin(lons),
+                            np.nanmax(lats), np.nanmax(lons))
         pll, ptr = GeoPoint(lat_ll, lon_ll, 0.0), GeoPoint(lat_tr, lon_tr, 0.0)
-        extend_km = (pll - ptr).magnitude * 0.1
+        extend_km = (pll - ptr).magnitude * extend_fac
         if extend_km == 0:
             extend_km = 1
         ll = pll.offset(azimuth=-135, dist_hor=float(extend_km), name="ll")
         tr = ptr.offset(azimuth=45, dist_hor=float(extend_km), name="tr")
-        return  ll, tr        
-        
+        return (ll, tr)
+
     def get_topo_data(self, geo_point=None, azimuth=None, dist_hor=None,
                       lon1=None, lat1=None):
         """Retrieve topographic data grid spanned by this and another point
-        
-        The second coordinate can be specified in several different ways 
+
+        The second coordinate can be specified in several different ways
         dependent on which of the input arguments are used. First checks if the
-        currently loaded topo data (``self.topo_data``) covers the range 
-        spanned by the 2 points. If this is the case, the loaded data will be 
-        used and nothing reloaded. If not, data will attempted to be loaded 
-        from the current :class:`TopoDataAccess` object within the lon lat 
+        currently loaded topo data (``self.topo_data``) covers the range
+        spanned by the 2 points. If this is the case, the loaded data will be
+        used and nothing reloaded. If not, data will attempted to be loaded
+        from the current :class:`TopoDataAccess` object within the lon lat
         range covered by the 2 points (set using :func:`range_borders`)
-        
+
         Note
         ----
-        The following input combinations work (and are preferentially 
-        processed in the specified list order if multiple input is given):
-        
+        The following input combinations work (and are preferentially
+        processed in the specified order if multiple input is given):
+
             1. specify endpoint using geo_point
             #. specify endpoint using azimuth and dist_hor
             #. specify endpoint using lon1 and lat1
-        
+
         Parameters
         ----------
-        geo_point : GeoPoint 
-            another geo_point,topo data will be retrieved between this point 
+        geo_point : GeoPoint
+            another geo_point,topo data will be retrieved between this point
             and destination point
-        azimuth : float 
-            azimuth angle of heading in decimal degrees (to be used with 
+        azimuth : float
+            azimuth angle of heading in decimal degrees (to be used with
             dist_hor)
-        dist_hor : float 
+        dist_hor : float
             horizontal distance from this point in km (to be used with azimuth)
         lon1 : float
-            longitude of destination point, topo data will be retrieved between 
+            longitude of destination point, topo data will be retrieved between
             this point and destination point (to be used with lat1)
-        lat1 : float 
-            latitude of destination point, topo data will be retrieved between 
+        lat1 : float
+            latitude of destination point, topo data will be retrieved between
             this point and destination point (to be used with lon1)
-        
+
         Returns
         -------
-        2-element tuple, containing:
-            
-            - :class:`TopoData`, the topographic data
-            - :class:`GeoPoint`, the second coordinate
+        TopoData
+            topographic data object.
+        GeoPoint
+            the second coordinate which deterimes the domain wrt to this
+            location.
         """
         pf = self
         if isinstance(geo_point, GeoPoint):
             pf = geo_point
         elif all(isinstance(x, (int, float)) for x in [dist_hor, azimuth]):
             pf = self.offset(azimuth, dist_hor)
         elif all(isinstance(x, (int, float)) for x in [lon1, lat1]):
             pf = GeoPoint(lat1, lon1)
-        
+
         ll, tr = self.range_borders(self, pf)
         lat0, lon0 = ll.latitude, ll.longitude
         lat1, lon1 = tr.latitude, tr.longitude
         if not (self.check_topo(lat1, lon1) and self.check_topo(lat0, lon0)):
-            print(("Topo data not avaialable in geo point %s, loading topodata"
-                        %self.name))
             self._load_topo_data(lat0, lon0, lat1, lon1)
-        else:
-            print ("Topo data avaialable in geo point %s")
         return self.topo_data, pf
-    
+
     def check_topo(self, lat1=None, lon1=None):
         """Check if topography is available between this point and another
-        
-        :param float lat1: latitude of end point, if None, only the 
-            coordinates of this object will be considered
-        :param float lon1: longitude of end point, if None, only the 
-            coordinates of this object will be considered
-        :returns: - bool, True if topo data is loaded, False if not
+
+        Parameters
+        ----------
+        lat1 : float
+            latitude of end point, if None, only the coordinates of this
+            object will be considered
+        lon1 : float
+            longitude of end point, if None, only the coordinates of this
+            object will be considered
+
+        Returns
+        -------
+        bool
+            True if topo data is loaded, False if not
         """
         if any([x == None for x in [lat1, lon1]]):
             lat1, lon1 = self.latitude, self.longitude
         if self.topo_data is None:
             return False
-        if not (self.topo_data.includes_coordinate(self.latitude, 
-                                                   self.longitude) 
-            and self.topo_data.includes_coordinate(lat1, lon1)):
+        if not (self.topo_data.includes_coordinate(self.latitude,
+                                                   self.longitude)
+                and self.topo_data.includes_coordinate(lat1, lon1)):
             return False
         return True
-        
-    def get_elevation_profile(self, geo_point=None, azimuth=None, 
-                              dist_hor=None, lon1=None, lat1=None, 
+
+    def get_elevation_profile(self, geo_point=None, azimuth=None,
+                              dist_hor=None, lon1=None, lat1=None,
                               resolution=5., **mapping_opts):
-        """Estimates the elevation profile for a given viewing direction up
-        to a given distance from the coordinates of this point. For input 
-        possibilities see docs of :func:`get_topo_data`.
-        
-        :param GeoPoint geo_point: another geo_point,topo data will be 
-            retrieved between this point and destination point
-        :param float azimuth: azimuth angle of heading in decimal degrees 
-            (to be used with dist_hor)
-        :param float dist_hor: horizontal distance from this point in km 
-            (to be used with azimuth)
-        :param float lon1: longitude of destination point, topo data will 
-            be retrieved between this point and destination point (to be 
-            used with lat1)
-        :param float lat1: latitude of destination point, topo data will be 
-            retrieved between this point and destination point 
-            (to be used with lon1)
-        :param float resolution: desired topo grid resolution in m. 
-            1D interpolation of the elevation profile is performed is 
-            applicable.
-        :returns: 
-            - :class:`ElevationProfile`, the profile object
-          
+        """Estimates the elevation profile for a given viewing direction
+
+        The profile is retrieved up to a given distance from the coordinate of
+        this point. For input possibilities see docs of :func:`get_topo_data`.
+
+        Note
+        ----
         The following input combinations work (and are preferentially processed
         in the specified list order if multiple input is given):
-        
+
             1. specify endpoint using geo_point
             #. specify endpoint using azimuth and dist_hor
             #. specify endpoint using lon1 and lat1
-            
-        
+
+        Parameters
+        ----------
+        geo_point : GeoPoint
+            end location of elevation profile (if this is provided, the
+            following other input options to determine the end point will be
+            ignored).
+        azimuth : float
+            azimuth angle (direction) of elevation profile in decimal degrees
+            (to be used with input arg dist_hor)
+        dist_hor : float
+            horizontal distance from this point in km (to be used with azimuth)
+        lon1 : float
+            longitude of destination point, topo data will
+            be retrieved between this point and destination point (to be
+            used with lat1)
+        lat1 : float
+            latitude of destination point, topo data will be
+            retrieved between this point and destination point
+            (to be used with lon1)
+        resolution : float
+            desired topo grid resolution in m.
+            1D interpolation of the elevation profile is performed if
+            applicable.
+
+        Returns
+        -------
+        ElevationProfile
+            the profile object
         """
         from geonum.elevationprofile import ElevationProfile
-        data, pf = self.get_topo_data(geo_point, azimuth, dist_hor, lon1, 
-                                      lat1)
-        return ElevationProfile(data, self, pf, resolution=resolution,
+        topo, pf = self.get_topo_data(geo_point, azimuth, dist_hor, lon1, lat1)
+        if pf == self:
+            raise ValueError('please specify endpoint location')
+        return ElevationProfile(observer=self,
+                                endpoint=pf,
+                                topo_data=topo,
+                                calc_on_init=True,
+                                resolution=resolution,
                                 **mapping_opts)
-        
-    def get_altitude(self):
-        """Estimate the altitude (+/- uncertainty) of this point 
-        
-        The estimatation is done by retrieving a 2x2 grid of topography
-        data enclosing this point. The altitude value is estimated using the 
-        topo data tile closest to the coordinates of this point. The uncertainty
-        is estimated conservatively using min/max difference of data in the 2x2
-        grid.
-        
-        :returns: 
-            - altitude (0 if retrieval failed)
-            - altitude error (99999999999 if retrieval failes)
-        :rtype:
-            - int, float
-        
-        """
-#==============================================================================
-#         print ("Try retrieving altitude for point %s (lat, lon): %s, %s" 
-#                                 %(self.name, self.latitude, self.longitude))
-#==============================================================================
-        try:
-            #the data access class already catches access failure and in case,
-            #tries to  access etopo1 data
+
+    def set_topo_altitude(self):
+        """Set altitude using topographic terrain height at lat / lon position
+
+        The estimation is done by retrieving a 2x2 grid of topography
+        data enclosing this point. The altitude value is estimated using the
+        topo data tile closest to the coordinates of this point. The
+        uncertainty is estimated conservatively using min/max difference of
+        data in the 2x2 grid.
+
+        Returns
+        -------
+        float
+            altitude
+        float
+            uncertainty in altitude value
+        """
+        if not isinstance(self.topo_data, TopoData):
             data = self._topo_access.get_data(self.latitude,
                                               self.longitude)
-            z = data(self.latitude, self.longitude)# / 1000.
-            z_err = (data.data.max() - data.data.min()) #/ 1000.'
-#            print "Retrieved altitude: %s +/- %s m" %(z, z_err)
-        except Exception as e:
-            warn('Altitude of {} could not be retrieved...\n'
-                 'Setting altitude to 0.0 m\n'
-                 'Error: {}'.format(repr(self), repr(e)))
-            z, z_err = 0.0, self._ALTERR_DEFAULT
-    
+            # store for later usage
+            self.set_topo_data(data)
+        else:
+            data = self.topo_data
+        z = data(self.latitude, self.longitude)
+        z_err = (data.data.max() - data.data.min())
         self.altitude, self.altitude_err = z, z_err
-        
         return (z, z_err)
-    
-    """HELPERS, IO stuff, etc"""
-    def update_topo_access(self, mode, local_path=None):
-        """Update topo access mode
-        
-        :param str mode: valid access mode (e.g. "srtm", "etopo1")        
-        :param str local_path (None): path for etopo1 access (if None, uses 
-            the one which is currently set in ``self._topo_access``)
-        """
-        if local_path is not None:
-            self.local_topo_path = local_path
-        self.topo_access_mode = mode
-        
-        
-    """Plotting etc..."""
-    def plot_2d(self, map, add_name=False, dist_text=0.5, angle_text=-45, 
-                **kwargs):
+
+    def plot_2d(self, map, add_name=False, dist_text=0.5, angle_text=-45,
+                **kwargs):  # pragma: no cover
         """Plot this point into existing 2D basemap
-                
-        :param map basemap: Basemap object (drawn in an Axes3D object)
-        :param bool add_name: add the name of this GeoPoint in the map
-        :param float dist_text: distance of text annotation from point
-        :param float angle_text: angle of text displacement
-        :param kwargs: additional keyword arguments passed to matplotlib 
-            plot function
+
+        Parameters
+        ----------
+        map : basemap
+            Basemap object (drawn in an Axes3D object)
+        add_name : bool
+            add the name of this GeoPoint in the map
+        dist_text : float
+            distance of text annotation from point
+        angle_text : float
+            angle of text displacement
+        **kwargs
+            additional keyword arguments passed to matplotlib plot function
         """
         if not "marker" in kwargs:
             kwargs["marker"] = "^"
         if not any([x in kwargs for x in ["c", "color"]]):
             kwargs["c"] = "lime"
         map.draw_geo_point_2d(self, **kwargs)
         if add_name:
             map.write_point_name_2d(self, dist_text, angle_text)
-                                                    
-    def plot_3d(self, map, add_name=False, dz_text=0.0, **kwargs):
-        """Plot this point into existing 3D basemap
-                
-        :param map basemap: Basemap object (drawn in an Axes3D object)
-        :param bool add_name: add the name of this GeoPoint in the map
-        :param float dz_text: altitude offset of text(to point)
-        :param kwargs: additional keyword arguments passed to matplotlib 
-            plot function
+
+    def plot_3d(self, map, add_name=False, dz_text=0.0,
+                **kwargs):  # pragma: no cover
+        """
+        Plot this point into existing 3D basemap
+
+        map : basemap
+            Basemap object (drawn in an Axes3D object)
+        add_name : bool
+            add the name of this GeoPoint in the map
+        dz_text : float
+            altitude offset of text (to point location in map)
+        **kwargs
+            additional keyword arguments passed to matplotlib plot function.
         """
         if not "marker" in kwargs:
             kwargs["marker"] = "^"
         if not any([x in kwargs for x in ["c", "color"]]):
             kwargs["c"] = "lime"
         map.draw_geo_point_3d(self, **kwargs)
-        x0, y0 = list(map(self.lon.decimal_degree, self.lat.decimal_degree))
+        # x0, y0 = list(map(self.lon.decimal_degree, self.lat.decimal_degree))
         if add_name and self.name is not None:
             try:
                 fs = kwargs["fontSize"]
-            except:
+            except Exception:
                 fs = 12
-            #zt=self.altitude*1000. + dz_text
+
             zt = self.altitude + dz_text
             map.draw_text_3d(self.longitude, self.latitude, zt, self.name,
                              color="k", fontsize=fs)
-            
-    @property
-    def _topo_access(self):
-        """Topography data access class"""
-        from geonum.topodataaccess import TopoDataAccess
-        return TopoDataAccess(mode=self.topo_access_mode,
-                              local_path=self.local_topo_path)
-        
-    def _load_topo_data(self, lat0, lon0, lat1, lon1):
-        """Load and update topo data
-        
-        :param float lon0: start longitude
-        :param float lat0: start latitude
-        :param float lon1: stop longitude 
-        :param float lat1: stop latitude
-        :return:
-            - :class:`TopoData` object with loaded data (it is also stored in
-                ``self.topo_data``)
+
+    def _load_topo_data(self, lat0, lon0, lat1, lon1) -> TopoData:
+        """Load topo data
+
+        Parameters
+        ----------
+        lon0 : float
+            start longitude
+        lat0 : float
+            start latitude
+        lon1 : float
+            stop longitude
+        lat1 : float
+            stop latitude
+
+        Return
+        ------
+        TopoData
+            loaded topographic data
         """
-        print("Trying to load topography data for {}".format(self))
         self.topo_data = self._topo_access.get_data(lat0, lon0, lat1, lon1)
         return self.topo_data
-        
+
     def _sub_geo_vector_2d(self, other):
         """Subtract another geo vector
-        
+
         Called when subtracting a GeoVector object from self (adapted from
-        `LatLon` object,  only return type was changed from LatLon 
+        `LatLon` object,  only return type was changed from LatLon
         object to GeoPoint object)
-        
-        :param (GeoVector, GeoVector3D) other: vector to be subtracted
-        :return: :class:`GeoPoint` at difference position
+
+        Parameters
+        ----------
+        other : GeoVector
+            vector to be subtracted from this location
+
+        Returns
+        -------
+        GeoPoint
+            endpoint location
         """
         heading, distance = other()
-        heading = (heading + 180) % 360 # Flip heading
+        heading = (heading + 180) % 360  # Flip heading
         p = GeoPoint(self.lat, self.lon, self.altitude)
-        
+
         return p.offset(heading, distance)
-    
+
     def _add_geo_vector_2d(self, other):
-        """Subtract another geo vector
-        
-        Add a geo vector (adapted from `LatLon` object,  only return 
+        """Add another geo vector
+
+        Add a geo vector (adapted from `LatLon` object,  only return
         type was changed from LatLon object to GeoPoint object)
-        
-        :param GeoVector other: Geovector added to this 
-        
+
+        Parameters
+        ----------
+        other : GeoVector
+            vector to be added to this location
+
+        Returns
+        -------
+        GeoPoint
+            endpoint location
+
         """
         azimuth, dist_hor = other()
         p = GeoPoint(self.lat, self.lon, self.altitude)
         return p.offset(azimuth, dist_hor, 0.0)
-        
+
     def _sub_geo_vector_3d(self, other):
-        """Called when subtracting a GeoVector3D object from self"""
+        """Subtract a GeoVector3D object from self
+
+        Parameters
+        ----------
+        other : GeoVector3D
+            vector to be subtracted from this location
+
+        Returns
+        -------
+        GeoPoint
+            endpoint location
+        """
         azimuth, dist_hor, dz = other()
-        azimuth = (azimuth + 180) % 360 # Flip heading
-        p = GeoPoint(self.lat, self.lon, self.altitude) # Copy current position
-        return p.offset(azimuth, dist_hor, -dz) # Offset position by GeoVector
-    
+        azimuth = (azimuth + 180) % 360  # Flip heading
+        p = GeoPoint(self.lat, self.lon, self.altitude)  # Copy current position
+        return p.offset(azimuth, dist_hor, -dz)  # Offset position by GeoVector
+
     def _add_geo_vector_3d(self, other):
         """Add a 3d geo vector object
-        
-        :param GeoVector3D other: Geovector which is added to self
+
+        Parameters
+        ----------
+        other : GeoVector3D
+            vector to be added to this location
+
+        Returns
+        -------
+        GeoPoint
+            endpoint location
         """
         azimuth, dist_hor, dz = other()
         p = GeoPoint(self.lat, self.lon, self.altitude)
         return p.offset(azimuth, dist_hor, dz)
-        
+
     def _sub_latlon(self, other):
         """Called when subtracting a LatLon object from this point"""
         from geonum import GeoVector3D
         inv = self._pyproj_inv(other)
         heading = inv['heading_reverse']
         distance = inv['distance']
-        name=str(other.name + "->" + self.name)
+        on = other.name
+        if on is None:
+            on = 'undefined'
+        name = f'{on}->{self.name}'
         return GeoVector3D(dz=0.0, azimuth=heading, dist_hor=distance,
                            anchor=other, name=name)
-    
+
     def _sub_geo_point(self, other):
         """Called when subtracting a LatLon object from self"""
         from geonum import GeoVector3D
         inv = self._pyproj_inv(other)
         heading = inv['heading_reverse']
         distance = inv['distance']
         name = str(other.name + "->" + self.name)
         dz = self.altitude - other.altitude
         return GeoVector3D(dz=dz, azimuth=heading, dist_hor=distance,
                            anchor=other, name=name)
-        
+
     def __eq__(self, other):
         """Checks equality of this point with another
-        
-        :param other: another :class:`GeoPoint` object
+
+        Parameters
+        ----------
+        other : GeoPoint
+            other location
+
+        Returns
+        -------
+        bool
+            True if other is equal, else False
         """
-        if (self.lat == other.lat and self.lon == other.lon 
-            and self.altitude == other.altitude):
+        if (self.latitude == other.latitude and
+                self.longitude == other.longitude and
+                self.altitude == other.altitude):
             return True
         return False
-        
+
     def __add__(self, other):
-        """Add a geo vector to this point
-        
-        :param (GeoVector, GeoVector3D) other: a vector
-        """
-        object_operator = {'GeoVector'      :   self._add_geo_vector_2d,
-                           'GeoVector3D'    :   self._add_geo_vector_3d}
+        """Add a geo vector or geo point to this point"""
+        object_operator = {'GeoVector': self._add_geo_vector_2d,
+                           'GeoVector3D': self._add_geo_vector_3d}
+        try:
+            tp = other.type()
+            if not tp in object_operator.keys():
+                raise AttributeError
+        except AttributeError:
+            raise ValueError(f'invalid input type {type(other)}, choose from '
+                             f'{list(object_operator)}')
         return object_operator[other.type()](other)
 
     def __sub__(self, other):
         """Subtraction"""
-        object_operator = {'GeoVector'      :   self._sub_geo_vector_2d,
-                           'GeoVector3D'    :   self._sub_geo_vector_3d,
-                           'LatLon'         :   self._sub_latlon,
-                           'GeoPoint'       :   self._sub_geo_point}
+        object_operator = {'GeoVector': self._sub_geo_vector_2d,
+                           'GeoVector3D': self._sub_geo_vector_3d,
+                           'LatLon': self._sub_latlon,
+                           'GeoPoint': self._sub_geo_point}
+        try:
+            tp = other.type()
+            if not tp in object_operator.keys():
+                raise AttributeError
+        except AttributeError:
+            raise ValueError(f'invalid input type {type(other)}, choose from '
+                             f'{list(object_operator)}')
         return object_operator[other.type()](other)
-    
+
     def __str__(self):
         """String formatting"""
-        return ("GeoPoint %s\nLat: %s, Lon: %s, Alt: %s m\n" 
-                %(self.name, self.latitude, self.longitude, self.altitude))
-    
+        return (
+            f"GeoPoint {self.name}\nLat: {self.latitude},  Lon:"
+            f" {self.longitude}, Alt: {self.altitude} m\n")
+
     def __repr__(self):
         """Obj. representation"""
-        return ("%s, %s, Alt. %s m" 
-                %(self.lat.__repr__(), self.lon.__repr__(), self.altitude))
-    
-    def __complex__(self):
-        """Complex representation of lat and lon"""
-        return self.complex()
-    
+        return (
+            f"Lat: {self.latitude}, Lon: {self.longitude}, Alt:"
+            f" {self.altitude} m")
+
     def type(self):
         """Object type identifier
-        
-        :returns: str, the string identifier        
+
+        Returns
+        -------
+        str
+            value='GeoPoint'
         """
         return 'GeoPoint'
+
+    @staticmethod
+    def from_LatLon(coord):
+        if not isinstance(coord, LatLon):
+            raise ValueError('Need LatLon...')
+        return GeoPoint(latitude=coord.lon.decimal_degree,
+                        longitude=coord.lat.decimal_degree,
+                        altitude=0,
+                        auto_topo_access=False)
```

### Comparing `geonum-1.4.5rc1/geonum/geovector3d.py` & `geonum-1.5.0.dev9/geonum/geovector3d.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-# -*- coding: utf-8 -*-
-#
 # Geonum is a Python library for geographical calculations in 3D
 # Copyright (C) 2017 Jonas Gliss (jonasgliss@gmail.com)
 #
 # This program is free software: you can redistribute it and/or
 # modify it under the terms of the GNU General Public License a
 # published by the Free Software Foundation, either version 3 of
 # the License, or (at your option) any later version.
@@ -11,241 +9,323 @@
 # This program is distributed in the hope that it will be useful,
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
 # General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program. If not, see <http://www.gnu.org/licenses/>.
+import warnings
+
+from LatLon23 import GeoVector, LatLon
+from numpy import (radians, cos, sin, degrees, sqrt, tan, isnan, arctan2)
 
-from LatLon23 import GeoVector
 from geonum.geopoint import GeoPoint
-    
-from numpy import (radians, cos, sin, degrees, sqrt,tan, isnan, arctan2)
+
 
 class GeoVector3D(GeoVector):
-    """A 3 dimensional geo vector object 
-    
-    3D vector representation for geo numerical calculations, intuitive 
-    usage, i.e.::
-    
-        from geonum import GeoPoint, GeoVector3D
-        p = GeoPoint(10.0, 15.0, name = "random_point") #lat, lon
-        v = GeoVector3D(dx = 15, dy = 100, dz = 300) #dx, dy in km, dz in m
-        
-        new_point = p + v # GeoPoint object
-        
+    """A 3-dimensional geo vector object
     
+    3D vector representation for geodesic connections and arithmetics of
+    locations (:class:`geonum.GeoPoint`).
+
     Note
     ----
-    
-        This class inherits and makes use of the functionality of 
-        `GeoVector` objects of the `LatLon` library. Methods and 
-        attributes are partly the same and partly overwritten
-        (note that it is not initiated as :class:`GeoVector`)
- 
+    To create an instnace of :class:`GeoVector3D` use one of the following to
+    input combinations:
+
+        1. dx, dy, dz
+        #. dz, azimuth, dist_hor
+        #. azimuth, dist_hor, elevation
+
+    Multiple input combinations will be processed in the preferred order
+    as given in the list.
+
+
+    Note
+    ----
+    Horitontal displacement components dx (longitude) and dy (latitude) are
+    in units of km, while vertical displacement component dz (altitude) is
+    in units of m.
+
+    Attributes
+    ----------
+    dx : float
+        longitudinal component in units of km
+    dy : float
+        latitudinal component in units of km
+    dz : float
+        altitude component in units of m
+    name : str
+        name of vector
+
+
+    Parameters
+    ----------
+    dx : float, optional
+        longitudinal component in units of km
+    dy : float, optional
+        latitudinal component in units of km
+    dz : float, optional
+        altitude component in units of m
+    azimuth : float, optional
+        azimuth orientation angle in units of decimal degrees, relative to
+        North direction.
+    dist_hor : float, optional
+        horizontal displacement length in input `azimuth` direction.
+    elevation : float, optional
+        elevation angle in decimal degrees (0 corresponds to horizon,
+        90 to zenith)
+    anchor : GeoPoint, optional
+        anchor point of this vector.
+    name : str, optional
+        name of vector, defaults to "undefined".
+
+    Example
+    -------
+
+    >>> from geonum import GeoPoint, GeoVector3D
+    >>> p = GeoPoint(latitude=10.0, longitude=15.0, name="random_point")
+    >>> v = GeoVector3D(dx=15, dy=100, dz=300) #dx, dy in km, dz in m
+    >>> new_point = p + v # GeoPoint object
+    >>> print(new_point)
+    GeoPoint undefined
+    Lat: 10.904041412793307,  Lon: 15.137202747069097, Alt: 300 m
+
     """
-            
-    def __init__(self, dx=None, dy=None, dz=None, azimuth=None, dist_hor=None, 
-                 elevation=None, anchor=None, name="n/d"):
-        """Class initialisation
-        
-        :param float dx: longitudinal length in km
-        :param float dy: latitudinal length in km
-        :param float dz: altitude length in m
-        :param float azimuth: azimuth angle to North direction (corresponds to 
-            heading_initial variable in :class:`GeoVector` object)
-        :param float dist_hor: horizontal displacement of object in km
-        :param float elevation: elevation angle in decimal degrees 
-            (0 corresponds to horizon, 90, to zenith)
-        
-        For initiation use one of the following to input combinations:
-        
-            1. dx, dy, dz
-            #. dz, azimuth, dist_hor
-            #. azimuth, dist_hor, elevation
-            
-        Multiple input combinations will be processed in the preferred order
-        as given in the list
-        
-        """
+
+    def __init__(self, dx=None, dy=None, dz=None, azimuth=None, dist_hor=None,
+                 elevation=None, anchor=None, name=None):
+        if name is None:
+            name = 'undefined'
+
         self.name = name
-        if any(x == None for x in [dx, dy]): # If only initial_heading and distance are given
-            theta_rad = radians(self._angle_or_heading(azimuth))
-            self.dx = dist_hor * cos(theta_rad)
-            self.dy = dist_hor * sin(theta_rad)
-        elif azimuth == None and dist_hor == None: # If only dx and dy are given
-            self.dx = dx
-            self.dy = dy
-        else:
-            raise NameError
-        #Check input for altitude difference dz
+
+        self.dx = None
+        self.dy = None
+        self.dz = None
+
+        self._eval_input(dx,dy,dz,azimuth,dist_hor,elevation)
+
+        # dictionary with private attributes
+        self._priv_attr= {"anchor" : None}
+
+        # call setter for private attribute anchor (this ensures that input
+        # attr anchor is of right type
+        if anchor is not None:
+            try:
+                self.set_anchor(anchor)
+            except TypeError as e:
+                print(f'Failed to set anchor. Reason: {e}')
+
+
+    def _eval_input(self,dx,dy,dz,azimuth,dist_hor,elevation):
+        """
+        Retrieve dx, dy, dz based on input
+
+        See parameter description regarding allowed input combinations. Note that for the horizontal
+        component, inputs of `dx` and `dy` are preferred over `azimuth` and `elevation` (in case
+        both are wrongly provided).
+
+        Parameters
+        ----------
+        dx : float, optional
+            delta x in units of longitude degrees East.
+            To be combined with `dy`. If None, it is expected that
+            azimuth and dist_hor are provided.
+        dy : float, optional
+            delta y in units of latitude North, to be combined with `dx`.
+            If None, it is expected that azimuth and dist_hor are provided.
+        dz : float, optional
+            delta z in units of m. If None or NaN, it will either be inferred
+            from input `elevation` and `dx` & `dy` or if that's not
+            possible (`elevation` is None), then it will be set to 0 m.
+        azimuth : float, optional
+            horizontal direction of vector in units of radians or degrees
+            (relative to North, or 12 o'clock direction)
+        dist_hor : float, optional
+            magnitude of horizontal component of vector (dx, dy).
+        elevation : float, optional
+            vertical elevation angle in units of degrees. Allowed input range are values between
+            (and excluding) -90 and +90 (zenith).
+        """
+        if dx is None or dy is None:
+            if azimuth is not None and dist_hor is not None:
+                theta_rad = radians(self._angle_or_heading(azimuth))
+                dx = dist_hor * cos(theta_rad)
+                dy = dist_hor * sin(theta_rad)
+            else: # If only dx and dy are given
+                raise ValueError('Please specify either: 1. azimuth and dist_hor, or 2. dx and dy')
+
+        self.dx = dx
+        self.dy = dy
+        # Check input for altitude component dz
         if dz is None or isnan(dz): #invalid for dz directly
-            if elevation is not None and -90 <= elevation <= 90: #check if instead elevation is valid, then set dz
-                #tan elev = dz/dist_hor
+            if elevation is not None and -90 < elevation < 90: #check if instead elevation is valid, then set dz
                 dz = tan(radians(elevation))*sqrt(self.dx**2+self.dy**2)*1000
             else: #both dz input and elevation are invalid, set dz=0
                 dz = 0.0
         self.dz = dz
-        # dictionary with private attributes
-        self._priv_attr= {"anchor" : None}
-        # call setter for private attribute anchor (this ensures that input 
-        # attr anchor is of right type
-        try:
-            self.set_anchor(anchor)
-        except:
-            pass
-    
+
     @property
-    def azimuth(self):
-        """Azimuth angle in dec degrees 
-        
-        Horizontal orientation measured from N direction
+    def dz_km(self) -> float:
+        """:attr:`dz` converted to units of km
+
+        E.g. used for internal arithmetics.
         """
-        return self._geom_hor()[0]
+        return self.dz/1000
 
     @property
-    def elevation(self):
-        """Elevation angle in decimal degrees
-        
-        Measured from horizon (i.e. 0 -> horizon, 90 -> zenith)
-        """
-        return 90 - self.polar_angle    
+    def azimuth(self) -> float:
+        """Horizontal orientation angle relative to North direction"""
+        return degrees(arctan2(self.dx, self.dy))
+
+    @property
+    def elevation(self) -> float:
+        """Elevation angle in decimal degrees relative to horizon"""
+        return (90-self.polar_angle)
     
     @property
-    def polar_angle(self):
-        """Polar angle in decimal degrees
-        
-        Returns the polar angle in decimal degrees (measured from zenith), 
-        i.e.::
-        
-            90 - self.elevation
-            
-        """
-        return degrees(arctan2(self.dist_hor, self.dz / 1000.))
+    def polar_angle(self) -> float:
+        """Polar angle in decimal degrees relative to zenith"""
+        return degrees(arctan2(self.dist_hor, self.dz_km))
     
     @property    
-    def magnitude(self):
-        """Return magnitude of vector (length)"""
-        return sqrt(self.dist_hor**2 + (self.dz / 1000.)**2)
+    def magnitude(self) -> float:
+        """Magnitude of vector (length) in units of km"""
+        return sqrt(self.dist_hor**2 + self.dz_km**2)
 
     @property
-    def norm(self):
-        """Return magnitude of vector (length)"""
+    def norm(self) -> float:
+        """Norm of vector, wrapper for :meth:`magnitude`"""
         return self.magnitude
         
     @property
-    def dist_hor(self):
+    def dist_hor(self) -> float:
         """Horizontal distance spanned by this vector"""
-        return self._geom_hor()[1]
+        return sqrt(self.dx**2 + self.dy**2)
     
     @property
-    def anchor(self):
-        """Getter method for private attribute anchor"""
+    def anchor(self) -> GeoPoint:
+        """Anchor point of vector"""
         return self._priv_attr["anchor"]
         
     @anchor.setter
     def anchor(self, value):
-        """Setter method of private property anchor
-        
-        See :func:`set_anchor` for input / output specs
-        """     
         self.set_anchor(value)
     
     def set_anchor(self, geo_point):
         """Set anchor of this vector
-        
-        :param GeoPoint geo_point: anchor point of this vector
-        :raises TypeError: if input is not :class:`GeoPoint` object        
+
+        Parameters
+        ----------
+        geo_point : GeoPoint
+            anchor location.
+
+        Raises
+        ------
+        TypeError
+            if input point is not instance of :class:`GeoPoint`.
         """
         if not isinstance(geo_point, GeoPoint):
-            raise TypeError("Could not set anchor: Invalid input type")
+            if isinstance(geo_point, LatLon):
+                geo_point = GeoPoint.from_LatLon(geo_point)
+            else:
+                raise TypeError("Could not set anchor: Invalid input type")
         self._priv_attr["anchor"] = geo_point
            
-    def intersect_hor(self, other):
-        """Determine the horizontal intersection of this vector with other 
-        input vector
-        
-        :param GeoVector3D: other vector
-        
-        .. note::
-        
-            Only works if anchor is defined
+    def intersect_hor(self, other) -> 'GeoVector3D':
+        """Find horizontal intersection of this vector with another vector
+
+        Note
+        ----
+        Only works if anchor point (:attr:`anchor`) is set in both vectors.
+
+        Parameters
+        ----------
+        other : GeoVector3D
+            Other vector for which the intersection is to be determined.
+
+        Raises
+        ------
+        AttributeError
+            if :attr:`anchor` is not set in this vector or input vector
+
+        Returns
+        -------
+        GeoVector3D
+            New vector pointing in direction of this vector but with correct
+            horizontal magnitude to the intersection with the other vector.
+
         """
         if not all([isinstance(x,GeoPoint) for x in [self.anchor, other.anchor]]):
-            raise ValueError("Intersection can not be determined, anchor "
-                " of one of the vectors not set..")
+            raise AttributeError(
+                "Intersection can not be determined, anchor "
+                "of one of the vectors not set..")
         v = other.anchor - self.anchor
         v.dz = 0.0
         other_az = radians((other.azimuth + 360) % 360)
         self_az = radians((self.azimuth + 360) % 360)
         dy = (v.dx - tan(other_az) * v.dy) / (tan(self_az) - tan(other_az))
         dx = tan(self_az) * dy
         return GeoVector3D(dx, dy, dz=0.0)
-        
-    def _geom_hor(self):
-        """Returns horizontal heading and horizontal magnitude"""
-        return (degrees(arctan2(self.dx, self.dy)),
-                sqrt(self.dx**2 + self.dy**2))
-        
-    """Plotting etc..."""
-    def plot(self, map, add_anchor=False, **kwargs):
-        """Plot this vector into existing basemap
-        
-        :param Map map: map object
-        :param bool add_anchor: If true, the anchor point is plotted as well
-        :param kwargs: additional keyword arguments
-        
-        .. note::
-        
-            1. The basemap needs to be set up with Axes3D
-            #. ``self.anchor`` must be set with a :class:`Geopoint` instance
-            
-        """
+
+    def plot(self, map, add_anchor=False, **kwargs): # pragma: no cover
+        """Plot this vector into existing basemap"""
+        warnings.warn(DeprecationWarning(
+            'See https://github.com/jgliss/geonum/issues/4'))
         map.draw_geo_vector_3d(self, **kwargs)
         if add_anchor:
             self.anchor.plot(map, add_name=True, dz_text=self.dz*.1)
-        
-    """Redifining magic methods from base class :class:`GeoVector` object for
-    3D calcs
-    """
+
+
+    # ToDo: check if __call__ is really needed, a little confusing...
     def __call__(self):
         """Call function
-        
-        :returns:
-            - float azimuth angle
-            - float, horizontal length in km
-            - float, vertical length in m
+
+        Returns
+        -------
+        float
+            azimuth angle in units of decimal degrees wrt to N direction
+        float
+            horizontal length in km
+        float
+            vertical length in m
         """
-        azimuth, dist_hor = self._geom_hor()
-        return azimuth, dist_hor, self.dz
-    
-    
+        return (self.azimuth, self.dist_hor, self.dz)
         
     def __neg__(self):
         """Returns negative of this vector"""
         return GeoVector3D(-self.dx, -self.dy, -self.dz)
-    
+
+    def __truediv__(self, other):
+        if isinstance(other, GeoVector3D):
+            dx = self.dx / other.dx
+            dy = self.dy / other.dy
+            dz = self.dz / other.dz
+        else:
+            dx = self.dx / other
+            dy = self.dy / other
+            dz = self.dz / other
+        return GeoVector3D(dx,dy,dz)
+
+
     def __add__(self, other):
-        """Add another geo vector
-        
-        
-        :param GeoVector3D other: another geo vector  
-        """
+        """Add another geo vector"""
         return GeoVector3D(self.dx + other.dx, self.dy + other.dy,
                            self.dz + other.dz)
 
-    def __str__(self):
+    def __str__(self) -> str:
         """String representation"""
         return ('GeoVector3D {}\n'
                 'Azimuth: {:.2f}°, Elevation: {:.4f}°, Magnitude: {:.2f} km '
                 '(hor: {:.2f} km)'
                 .format(self.name, self.azimuth, self.elevation, 
                         self.magnitude, self.dist_hor))
             
     
-    def __repr__(self):
+    def __repr__(self) -> str:
         return ('Az %s, Elev %s, Mag. %s' 
                 %(self.azimuth, self.elevation, self.magnitude))
     
-    def type(self):
+    def type(self) -> str:
         """Returns object type"""
         return 'GeoVector3D'
```

### Comparing `geonum-1.4.5rc1/geonum/mapping.py` & `geonum-1.5.0.dev9/geonum/mapping.py`

 * *Files 10% similar despite different names*

```diff
@@ -13,165 +13,177 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
 # General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program. If not, see <http://www.gnu.org/licenses/>.
 try:
     from mpl_toolkits.basemap import Basemap
+    basemap_avail = True
 except:
-    print('Plotting of maps etc. is deactivated, please install Basemap')
-
-import numpy as np    
+    Basemap = object
+    basemap_avail = False
 
+import numpy as np
 from geonum.topodataaccess import TopoDataAccess
 from geonum.topodata import TopoData
 from geonum.exceptions import TopoAccessError
-from geonum.helpers import haversine_formula, shifted_color_map, exponent
+from geonum.helpers import haversine_formula, shifted_color_map, order_of_magnitude
 
 from geonum import CV2_AVAILABLE
+import warnings
+warnings.warn(DeprecationWarning('geonum.mapping module is deprecated '
+                                 'since it is based on the deprecated '
+                                 'basemap library. It is in the process of '
+                                 'being replaced using cartopy instead. See '
+                                 'geonum.helpers_plot and example scripts '
+                                 'for plot functionality.'))
 
 class Map(Basemap):
     """Basemap object for drawing and plotting (on) a map
-    
+
     This object is initiated as `Basemap <http://matplotlib.org/basemap/
-    users/examples.html>`_ and can therefore be used as such. 
+    users/examples.html>`_ and can therefore be used as such.
     Added functionality mainly includes:
-    
+
     1. Including topography data
     #. 2D and 3D plotting
     #. Handle of :class:`GeoVector3D` and :class:`GeoPoint` objects
     #. Some more high level functionality (i.e. draw text, points, polygons \
        or plot data onto map)
 
     Note
     ----
-    
-    The mapping functionality was initally developed for geographical 
-    setups on local scales (i.e. several 10 km grids) including 
-    handling of high resolution topography data and was not tested to 
+
+    The mapping functionality was initally developed for geographical
+    setups on local scales (i.e. several 10 km grids) including
+    handling of high resolution topography data and was not tested to
     create large maps on global scales. In principle, this should work,
     though.
-       
-    """ 
+
+    """
     def __init__(self, *args, **kwargs):
         """Initialisation of the map object
-        
-        :param *args: additional non-keyword parameters (passed to `basemap 
+
+        :param *args: additional non-keyword parameters (passed to `basemap
             <http://matplotlib.org/basemap/api/basemap_api.html#mpl
             _toolkits.basemap.Basemap>`_)
-        :param **kwargs: additional keyword parameters (passed to `basemap 
+        :param **kwargs: additional keyword parameters (passed to `basemap
             <http://matplotlib.org/basemap/api/basemap_api.html#mpl
             _toolkits.basemap.Basemap>`_)
-            
+
         .. note::
-        
-            Additional possible input in **kwargs wit to ``Basemap`` 
-            objects is "topo_data" which will be set in case it is a valid 
-            input (i.e. :class:`TopoData`) and will be used for plotting 
+
+            Additional possible input in **kwargs wit to ``Basemap``
+            objects is "topo_data" which will be set in case it is a valid
+            input (i.e. :class:`TopoData`) and will be used for plotting
             topography
         """
+        if not basemap_avail:
+            raise ModuleNotFoundError(
+                'Plotting of maps etc. is deactivated, please install Basemap'
+                )
         super(Map, self).__init__(*args, **kwargs)
 
         self.topo_data = None
         #IMPORTANT HANDLES
         self.contour_lines = None
         self.contour_filled = None
-        
+
         self.colorbars = {}
         self.points = {}
         self.lines = {}
         self.polygons = {}
         self.texts = {}
         self.plotted_data = {}
-        
+
         self.map_scale = None
         self.meridians = None
         self.parallels = None
-        
+
         self.default_colors = {"contour_lines"  :   "#708090",
                                "land"           :   "#FFE0B2",
                                "water"          :   "#e6e6fa"}
-                               
+
     @property
     def color_land(self):
         """Default color of land tiles"""
         return self.default_colors["land"]
 
     @property
     def color_water(self):
         """Default color of ocean / sea tiles"""
         return self.default_colors["water"]
-                
+
     def set_topo_data(self, topo):
         """Update topo data
-        
+
         :class TopoData topo: object containing topography data
         """
         if isinstance(topo, TopoData):
             self.topo_data = topo
-        
+
     def load_topo_data(self, mode="srtm", local_path=None):
         """Geonum wrapper for topography access"""
         ta = TopoDataAccess(mode, local_path)
         try:
             self.topo_data = ta.get_data(self.lat_ll, self.lon_ll,
                                          self.lat_tr, self.lon_tr)
             return self.topo_data
         except Exception as e:
             raise TopoAccessError(repr(e))
-            
+
     @property
     def lon_ll(self):
         """Lower left longitude of plotted range"""
         return self.llcrnrlon
     @property
     def lat_ll(self):
         """Lower left latitude of plotted range"""
         return self.llcrnrlat
     @property
     def lon_tr(self):
-        """Top right longitude of plotted range"""        
+        """Top right longitude of plotted range"""
         return self.urcrnrlon
     @property
     def lat_tr(self):
-        """Top right latitude of plotted range"""        
+        """Top right latitude of plotted range"""
         return self.urcrnrlat
-    
+
     @property
     def delta_lon(self):
         """Returns longitude range"""
         return abs(self.lon_tr - self.lon_ll)
-        
-    @property    
+
+    @property
     def delta_lat(self):
         """Returns latitude range"""
         return abs(self.lat_tr - self.lat_ll)
-        
+
     def fill_map(self):
         """Fill the map with default colors"""
         self.drawmapboundary(fill_color=self.color_water)
         self.fillcontinents(color=self.color_land, lake_color=self.color_water)
-    
+
     def _prep_topo_data(self, grid_points=100):
         """Prepare topography data for map
-        
+
         This function prepares high resolution topography for plotting, i.e.
         it reduces the resolution based on the map size
-        
+
         :param int grid_points: number of plotted grid points (default: 100)
-        
+
         """
-        
-            
+
+
         if not isinstance(self.topo_data, TopoData):
             try:
                 self.load_topo_data()
             except:
                 raise
-    
+
         topo = self.topo_data
         # determine the nu
         pyr_steps = int(np.ceil(np.log2(float(len(topo.lons)) / grid_points)))
         z_max = float(topo.max)
         z_min = float(topo.min)
         z_order = np.floor(np.log10(topo.alt_range))
         X,Y = np.meshgrid(topo.lons, topo.lats)
@@ -183,181 +195,181 @@
                           "opencv library is not available")
         else:
             from cv2 import pyrDown
             if pyr_steps > 0:
                 for k in range(pyr_steps):
                     x = pyrDown(x)
                     y = pyrDown(y)
-                    z = pyrDown(z)            
+                    z = pyrDown(z)
         return (x, y, z, z_min, z_max, z_order)
-            
+
     def draw_topo_contour(self, include_seabed=1, separation_levels=500):
         """Draw topography contour lines
-        
-         :param bool include_seabed: include seabed topography 
+
+         :param bool include_seabed: include seabed topography
              (default: True)
          :param int separation_levels: separation in m of contour lines
              (default: 500)
         """
 
         x, y, z, z_min, z_max, z_order = self._prep_topo_data()
         if z_min > 0:
             include_seabed=1
         min_c = int(round(z_min / 10**(z_order - 1)) * 10**(z_order - 1))
         max_c = int(round(z_max / 10**(z_order - 1)) * 10**(z_order - 1))
         if include_seabed:
             levels_contour = np.arange(min_c, max_c, separation_levels)
         else:
             levels_contour = np.arange(0, max_c, separation_levels)
-        
+
         CS1 = self.contour(x, y, z, levels_contour, linewidths=0.5,
                            colors=self.default_colors["contour_lines"])
         CS1.levels = [self._convert_float(val) for val in CS1.levels]
-             
+
         self.ax.clabel(CS1, CS1.levels, inline=True)
-        self.contour_lines = CS1   
-            
+        self.contour_lines = CS1
+
     def _convert_float(self, val):
         """Custom float to string conversion for topo contour plotting
-        
-        :param float val: the float value to be converted into string        
+
+        :param float val: the float value to be converted into string
         """
         s = "%.1f" %val
         if s[-1] == "0":
             return "%.0f" %val
         return "%.1f" %val
-    
+
     def _check_ax3d(self, ax):
         """Check if input is :class:`Axes3D`"""
 
         from mpl_toolkits import mplot3d
         if isinstance(ax, mplot3d.Axes3D):
             return True
         return False
-    
+
     def set_ticks_topo_colorbar(self, start, stop, step):
         """Update ticks of topo colorbar"""
         cb = self.colorbars["topo"]
         ticks = np.arange(start, stop, step)
         cb.set_ticks(ticks)
-        
+
     def draw_topo(self, insert_colorbar=False, include_seabed=True,
                     max_grid_points=500, cmap_div=None,
                     cmap_seq=None, alpha=0.5, ax=None):
         """Draw topography into map
-        
+
         :param bool insert_colorbar: draws a colorbar for altitude
             range (default: False)
-        :param bool include_seabed: include seabed topography 
+        :param bool include_seabed: include seabed topography
             (default: True)
-        :param int max_grid_points: resolution of displayed topo data 
+        :param int max_grid_points: resolution of displayed topo data
             points (makes it faster in interactive mode, default: 500)
-        :param str cmap_div: name of a diverging colormap (this one is 
-            used if :arg:`include_seabed` is True, and the cmap is shifted 
-            such , that white colors correspond to sea level altitude, 
+        :param str cmap_div: name of a diverging colormap (this one is
+            used if :arg:`include_seabed` is True, and the cmap is shifted
+            such , that white colors correspond to sea level altitude,
             default: "coolwarm")
-        :param str cmap_seq: name of a sequential colormap (this one is 
+        :param str cmap_seq: name of a sequential colormap (this one is
             used if :arg:`include_seabed` is False, default: "Oranges")
-        :param float alpha: Alpha value (transparency) of plotted 
+        :param float alpha: Alpha value (transparency) of plotted
             topography
         :param ax: matplotlib axes object
         """
         import matplotlib.cm as colormaps
         if cmap_div is None:
             cmap_div = colormaps.coolwarm
         if cmap_seq is None:
             cmap_seq = colormaps.Oranges
-        
-        try:  
+
+        try:
             if ax is None:
                 ax = self.ax
             if ax is None:
                 from matplotlib.pyplot import subplots
                 fig, ax = subplots(1, 1, figsize=(16,10))
                 self.ax = ax
-    
-            (x, y, z, z_min, z_max, 
+
+            (x, y, z, z_min, z_max,
              z_order) = self._prep_topo_data(grid_points=max_grid_points)
-                
-            
+
+
             delz = z_max - z_min #in m
-            exp = exponent(delz) - 1
+            exp = order_of_magnitude(delz) - 1
             start_alt = round((z_min - delz*0.1)*10**(-exp))*10**exp
             stop_alt = round((z_max + delz*0.1)*10**(-exp))*10**exp
             if z_min > 0:
                 include_seabed = 1
-                
+
             if not include_seabed:
                 start_alt = 0
-            
-            z_step = (stop_alt - start_alt) / 1000. 
+
+            z_step = (stop_alt - start_alt) / 1000.
             levels_filled = np.arange(start_alt, stop_alt, z_step)
-            
-            if levels_filled[0] < 0:          
+
+            if levels_filled[0] < 0:
                 shifted_cmap = shifted_color_map(z_min, z_max, cmap_div)
-                
+
                 cs2 = ax.contourf(x, y, z, levels_filled, cmap=shifted_cmap,
                                   extend="both", alpha=alpha)
-                                  
-            elif levels_filled[0] >= 0:        
+
+            elif levels_filled[0] >= 0:
                 cs2 = ax.contourf(x, y, z, levels_filled, cmap=cmap_seq,
                                   alpha=1.0, extend="min")
                 self.contour_filled = cs2
-                    
-            if insert_colorbar:              
+
+            if insert_colorbar:
                 self.insert_colorbar("topo", cs2, label="Altitude [m]")
-                exp = exponent(delz)
+                exp = order_of_magnitude(delz)
                 step = round(delz*10**(-exp))*10**(exp-1)
                 self.set_ticks_topo_colorbar(start_alt, stop_alt, step)
         except Exception as e:
             raise
             msg=("Could not draw topography in high res, using default "
                  "etopo() instead...")
             print(msg + repr(e))
             self.etopo()
-                 
+
     def draw_topo_3d(self, num_ticks=4, cmap="Oranges", alpha=0.5,
-                     contour_color="#708090", contour_antialiased=True, 
+                     contour_color="#708090", contour_antialiased=True,
                      contour_lw=0.2, ax=None, figsize=(16,8)):
         """Draw topography into 3D axis
-        
+
         Parameters
-        ----------        
-        num_ticks : int 
+        ----------
+        num_ticks : int
             number of lon / lat axis ticks (default: 4)
         cmap : str
             string ID of the colormap used (default: "Oranges")
         alpha : flaot
             Alpha value (transparency) of plotted topography (default: 0.5)
         contour_color : str
-            string specifying color of contour lines colors of contour lines 
+            string specifying color of contour lines colors of contour lines
             (default: "#708090")
         contour_antialiased : bool
             apply antialiasing to surface plot of topography, defaults to False
-        contour_lw : 
-            width of drawn contour lines, defaults to 0.5, use 0 if you do not 
+        contour_lw :
+            width of drawn contour lines, defaults to 0.5, use 0 if you do not
             want contour lines inserted
-            
-        ax : 
+
+        ax :
             axes object
         """
         if not self._check_ax3d(ax):
             if self._check_ax3d(self.ax):
                 ax = self.ax
             else:
                 from mpl_toolkits import mplot3d
                 from matplotlib.pyplot import figure
                 fig = figure(figsize=figsize)
                 ax = mplot3d.Axes3D(fig)
-    
+
         x, y, z, z_min, z_max, z_order = self._prep_topo_data()
-        tickformatter = "{:.2f}"    
-        ax.plot_surface(x, y, z, rstride=1, cstride=1, cmap=cmap, alpha=alpha, 
-                        linewidth=contour_lw, antialiased=contour_antialiased, 
-                        edgecolors=contour_color, vmin=z_min, vmax=z_max, 
+        tickformatter = "{:.2f}"
+        ax.plot_surface(x, y, z, rstride=1, cstride=1, cmap=cmap, alpha=alpha,
+                        linewidth=contour_lw, antialiased=contour_antialiased,
+                        edgecolors=contour_color, vmin=z_min, vmax=z_max,
                         zorder=1)
         #xlabels=ax.get_xticklabels()
         ax.set_xlabel("Lons")
         ax.set_ylabel("Lats")
         ax.set_zlabel("Altitude [m]")
         lon_step, lat_step = self.delta_lon * .33, self.delta_lat * .33
         lon_tick_array, lat_tick_array=[], []
@@ -367,39 +379,39 @@
         #lon_tick_array, lat_tick_array = self._prep_coord_ticks()
         lon_coords=[]
         lon_labels=[]
         for lon in lon_tick_array:
             x,_=self(lon,self.lat_ll)
             lon_coords.append(x)
             lon_labels.append(tickformatter.format(lon))
-        
+
         lat_coords=[]
         lat_labels=[]
         for lat in lat_tick_array:
             _, y = self(self.lon_ll, lat)
             lat_coords.append(y)
             lat_labels.append(tickformatter.format(lat))
-            
+
         ax.set_yticks(lat_coords)
         ax.set_yticklabels(lat_labels)
         ax.set_xticks(lon_coords)
         ax.set_xticklabels(lon_labels)
         self.ax = ax
-        
+
     def draw_mapscale_auto(self, **kwargs):
-        """Insert a map scale 
-        
-        Determines missing input parameters automatically and calls 
-        :func:`drawmapscale` 
-        
+        """Insert a map scale
+
+        Determines missing input parameters automatically and calls
+        :func:`drawmapscale`
+
         :param kwargs: key word arguments for :func:`drawmapscale` (missing
             ones will be set automatically)
         """
-        l = self._len_diag()  
-        exp = exponent(l)
+        l = self._len_diag()
+        exp = order_of_magnitude(l)
         l = round(l * 10**(-exp))*10**(exp)/5.0
         lat_center, lon_center = self.get_map_center()
         str_format = '%d'
         if not "length" in kwargs:
             kwargs["length"] = l
         if l < 40:
             str_format = '%.1f'
@@ -416,66 +428,66 @@
         if not "barstyle" in kwargs:
             kwargs["barstyle"] = "fancy"
         if not "units" in kwargs:
             kwargs["units"] = "km"
         if not "format" in kwargs:
             kwargs["format"] = str_format
         self.map_scale = self.drawmapscale(**kwargs)
-        
+
     def remove_map_scale(self):
         """Remove scale"""
         if self.map_scale is not None:
             for i in self.map_scale:
                 try:
                     i.remove()
                 except:
                     print(("Warning in remove_map_scale: item %s could not be "
                         "removed" %i))
         self.fig.canvas.draw()
-    
+
     def _prep_coord_ticks(self, lon_tick=None, lat_tick=None):
         """Prepare coordinate ticks for parallels and meridians
-        
+
         :param float lon_tick: longitude separation (in decimal degrees).
             Will be set automatically if unspecified
         :param float lat_tick: latitude separation (in decimal degrees)
             Will be set automatically if unspecified
         """
         if lon_tick is None:
             pot_lon = np.floor(np.log10(self.delta_lon))
             lon_tick = np.floor(self.delta_lon / 10**pot_lon) * 10**pot_lon / 4
         if lat_tick is None:
             pot_lat = np.floor(np.log10(self.delta_lat))
             lat_tick = np.floor(self.delta_lat / 10**pot_lat) * 10**pot_lat / 3
-            
-        lon_tick_array = np.arange(lon_tick * int((self.lon_ll - self.delta_lon 
-                                * 0.3) / lon_tick), lon_tick * int((self.lon_tr 
+
+        lon_tick_array = np.arange(lon_tick * int((self.lon_ll - self.delta_lon
+                                * 0.3) / lon_tick), lon_tick * int((self.lon_tr
                                 + self.delta_lon * 0.3) / lon_tick), lon_tick)
-                                
-        lat_tick_array = np.arange(lat_tick * int((self.lat_ll - self.delta_lat 
-                                * 0.3) / lat_tick), lat_tick * int((self.lat_tr 
+
+        lat_tick_array = np.arange(lat_tick * int((self.lat_ll - self.delta_lat
+                                * 0.3) / lat_tick), lat_tick * int((self.lat_tr
                                 + self.delta_lat * 0.3) / lat_tick), lat_tick)
-                                
+
         return lon_tick_array, lat_tick_array
-    
+
     def _len_diag(self):
         """Returns the lenght from LL point to TR point in km"""
         return self.haversine(self.lon_ll,self.lat_ll,self.lon_tr,self.lat_tr)
-    
-        
+
+
     def draw_coordinates(self, lat_tick=None, lon_tick=None,
-                         labelslon=[0,0,0,1], labelslat=[1,0,0,0], 
+                         labelslon=[0,0,0,1], labelslat=[1,0,0,0],
                          **kwargs):
-        """Draws meridians and parallels 
-        
+        """Draws meridians and parallels
+
         :param float lat_tick: latitude separation (in decimal degrees)
         :param float lon_tick: longitude separation (in decimal degrees)
         :param labelslon: see basemap docs (default: [0,0,0,1])
         :param labelslat: see basemap docs (default: [1,0,0,0])
-        :param **kwargs: additional keyword arguments (passed to 
+        :param **kwargs: additional keyword arguments (passed to
             :func:`drawmeridians` and :func:`drawparallels`)
         """
         if not "color" in kwargs:
             kwargs["color"] = "gray"
         if not "fmt" in kwargs:
             digs = '%d' %(4 - int(np.floor(np.log10(self._len_diag()))))
             kwargs["fmt"] = "%." + digs + "f"
@@ -485,198 +497,198 @@
                                        **kwargs)
         for m in meridians:
             try:
                 meridians[m][1][0].set_rotation(25)
             except:
                 pass
         self.meridians = meridians
-        self.parallels = ps =self.drawparallels(lat_tick_array, 
-                                                labels=labelslat, 
+        self.parallels = ps =self.drawparallels(lat_tick_array,
+                                                labels=labelslat,
                                                 **kwargs)
         for p in ps:
             try:
                 ps[p][1][0].set_rotation(25)
             except:
                 print("Could not rotate parallel...")
-            
+
     def remove_coordinates(self):
         """Remove drawn parallels and meridians"""
         if self.meridians is not None:
             for Dict in [self.meridians, self.parallels]:
                 for key in Dict:
                     for item in Dict[key]:
                         try:
                             item[0].remove()
                         except:
                             print("Object %s could not be removed" %item)
         self.fig.canvas.draw()
-    
+
     def legend(self, ax=None, **kwargs):
         """Insert a legend"""
         if ax is None:
             ax = self.ax
 # =============================================================================
 #         if not "fontsize" in kwargs:
 #             kwargs["fontsize"] = 10
 # =============================================================================
         ax.legend(loc="best", fancybox=True, framealpha=0.7, **kwargs)
-                                                                
+
     def draw_geo_point_2d(self, p, add_name=False, ax=None, **kwargs):
         """Draw a GeoPoint into 2D basemap
-        
-        :param GeoPoint p: the actual point        
+
+        :param GeoPoint p: the actual point
         :param **kwargs: passed to matplotlib plotting function
-            
+
         """
         if ax is None:
             ax = self.ax
         if not "marker" in kwargs:
             kwargs["marker"] = "^"
         if not "c" in kwargs:
             kwargs["c"]="lime"
         x, y = self(p.longitude, p.latitude) #maps the geo coordinates to figure coordinates
-                
-        handle = ax.plot(x, y, **kwargs) 
+
+        handle = ax.plot(x, y, **kwargs)
         self.points[p.name] = handle
         if add_name:
             self.write_point_name_2d(p)
         return handle
-    
+
     def draw_geo_vector_2d(self, vec, **kwargs):
         """Draw a :class:`GeoVector3D` into 2D map
-        
-        :param GeoVector3D vec: the vector 
-        
+
+        :param GeoVector3D vec: the vector
+
         .. note::
-        
-            Anchor must be set in the :class:`GeoVector3D` object  
+
+            Anchor must be set in the :class:`GeoVector3D` object
         """
         if not vec.type() == "GeoVector3D":
             raise AttributeError("Wrong input, need :class:`GeoVector3D` "
                                                                 "object")
         elif not vec.anchor.type() == "GeoPoint":
             raise AttributeError("Vector anchor not set or wrong type..")
 
         if not any([x in kwargs for x in["ls", "linestyle"]]):
             kwargs["ls"] = "--"
-            
+
         a = vec.anchor
         pf = a + vec
         x0, y0 = self(a.longitude, a.latitude)
         x1, y1 = self(pf.longitude, pf.latitude)
         return self.draw_line_2d(vec.name, a.latitude, a.longitude,
                                  pf.latitude, pf.longitude, **kwargs)
-    
-    def add_geo_points_3d(self, pts, distances=None, marker="x", color="b", 
+
+    def add_geo_points_3d(self, pts, distances=None, marker="x", color="b",
                           connect=True, connect_style="--", alt_offset_m=0):
         """Draws a list of :class:`GeoPoint` objects into the map
-        
+
         :param list pts: geopoint objects
         :param color: color of points (passed to plot function, default: "b")
         :param marker: marker of points (default: "x")
-        :param connect: if True, points the points are connected with each 
+        :param connect: if True, points the points are connected with each
             other
         :param str connect_style: line style of connection
         """
         xs, ys, zs = [], [], []
         for p in pts:
             try:
                 px, py= self(p.lon.decimal_degree,p.lat.decimal_degree)
                 xs.append(px), ys.append(py), zs.append(p.altitude)
-                self.draw_geo_point_3d(p, alt_offset_m=alt_offset_m, 
+                self.draw_geo_point_3d(p, alt_offset_m=alt_offset_m,
                                        marker=marker, s=20, c=color)
             except:
                 print("Failed to add %s to map" %p)
         if distances is not None and len(distances) == len(pts):
-            sc = self.ax.scatter(xs, ys, np.asarray(zs)+alt_offset_m, zdir='z', 
-                                 s=20, c=distances, cmap="Oranges", 
+            sc = self.ax.scatter(xs, ys, np.asarray(zs)+alt_offset_m, zdir='z',
+                                 s=20, c=distances, cmap="Oranges",
                                  zorder=100000)
             zlabel = "Distance [%km]"
             self.insert_colorbar("dists", sc, label=zlabel)
         elif connect:
-            self.ax.plot(xs, ys, np.asarray(zs)+alt_offset_m, 
-                         ls=connect_style, 
-                         c=color, lw=2, zorder=100000)   
-                                                
+            self.ax.plot(xs, ys, np.asarray(zs)+alt_offset_m,
+                         ls=connect_style,
+                         c=color, lw=2, zorder=100000)
+
     def draw_geo_point_3d(self, p, ax=None, alt_offset_m=0.0, **kwargs):
         """Draw a GeoPoint into 3D basemap
-        
-        :param GeoPoint p: the actual point        
+
+        :param GeoPoint p: the actual point
         :param ax: matplotlib axes object (3d axis)
         :param float alt_offset_m: plot point with altitude offset, default 0
         :param **kwargs: passed to matplotlib plotting function
-        
+
         .. note::
-        
+
             The basemap needs to be set up with Axes3d object
-            
+
         """
         if not self._check_ax3d(ax):
-            if not self._check_ax3d(self.ax):    
+            if not self._check_ax3d(self.ax):
                 raise TypeError("No 3D Axes object available...")
             ax=self.ax
         if not "marker" in kwargs:
             kwargs["marker"] = "^"
         if not any([x in kwargs for x in ["c", "color"]]):
             kwargs["c"] = "lime"
         from mpl_toolkits import mplot3d
         if not isinstance(self.ax, mplot3d.Axes3D):
             raise ValueError("Need :class:`Axes3D` object as input...")
         x0, y0 = self(p.longitude, p.latitude)
         z0 = p.altitude + alt_offset_m#*1000
         handle = ax.scatter(x0, y0, z0, zorder=100000, **kwargs)
         self.points[p.name] = handle
         return handle
-                                 
+
     def draw_geo_vector_3d(self, vec, ax=None,  **kwargs):
         """Draw a :class:`GeoVector3D` into 3D map
-        
-        :param GeoVector3D vec: the vector 
-        
+
+        :param GeoVector3D vec: the vector
+
         .. note::
-        
-            Anchor must be set in the :class:`GeoVector3D` object  
-            
-        """ 
+
+            Anchor must be set in the :class:`GeoVector3D` object
+
+        """
         if ax is None:
             ax = self.ax
         try:
             from mpl_toolkits import mplot3d
             if not isinstance(ax, mplot3d.Axes3D):
                 raise ValueError("Need :class:`Axes3D` object as input...")
             elif not vec.type() == "GeoVector3D":
                 raise AttributeError("Wrong input, need :class:`GeoVector3D` "
                                                                     "object")
             elif not vec.anchor.type() == "GeoPoint":
                 raise AttributeError("Vector anchor not set or wrong type..")
-    
+
             if not any([x in kwargs for x in["ls", "linestyle"]]):
                 kwargs["ls"] = "--"
-            
+
             a = vec.anchor
             pf = a + vec
             x0, y0 = self(a.longitude, a.latitude)
             z0 = a.altitude#*1000
             x1, y1 = self(pf.longitude, pf.latitude)
             z1 = pf.altitude#*1000
-    
+
             l = mplot3d.art3d.Line3D((x0,x1), (y0,y1), (z0,z1), **kwargs)
             handle = ax.add_line(l)
             self.lines[vec.name] = handle
             return pf
 
         except:
             print(vec.anchor.type())
             raise
-    
+
     def add_polygon_2d(self, points=[], poly_id="undefined", ax=None, **kwargs):
         """Add a polygon specified by list of input points
-        
+
         :param list points: list with :class:`GeoPoint` objects
-        :param str poly_id: string ID of this object (e.g. for 
+        :param str poly_id: string ID of this object (e.g. for
             deletion, default: "undefined")
         """
         if ax is None:
             ax = self.ax
         if not "label" in kwargs:
             kwargs["label"] = poly_id
         coords=[]
@@ -684,20 +696,20 @@
             try:
                 coords.append(self(p.longitude, p.latitude))
             except Exception as e:
                 print("Failed to add one point to poly: " + repr(e))
         from matplotlib.pyplot import Polygon
         polygon = Polygon(coords, **kwargs)
         ax.add_patch(polygon)
-        
+
     def add_polygon_3d(self, points=[], poly_id="undefined", ax=None, **kwargs):
-        """Add a polygon specified by list of input points 
-        
+        """Add a polygon specified by list of input points
+
         :param list points: list with :class:`GeoPoint` objects
-        :param str poly_id: string ID of this object (e.g. for 
+        :param str poly_id: string ID of this object (e.g. for
             deletion, default: "undefined")
         """
         from mpl_toolkits import mplot3d
         if ax is None:
             ax = self.ax
         if not "label" in kwargs:
             kwargs["label"] = poly_id
@@ -706,248 +718,243 @@
             x,y=self(p.longitude, p.latitude)
             xs.append(x)
             ys.append(y)
             zs.append(p.altitude)#*1000)
         coords = [list(zip(xs, ys, zs))]
         poly_coll = mplot3d.art3d.Poly3DCollection(coords, **kwargs)
         ax.add_collection3d(poly_coll)
-           
+
     def draw_line_2d(self,line_id, lat0, lon0, lat1, lon1, **kwargs):
         """Draw a line between 2 geo coordinates
-        
+
         :param str line_id: ID of the line artist (for deletion management)
-        :param float lon0: start longitude 
-        :param float lat0: start latitude 
-        :param float lon1: stop longitude 
+        :param float lon0: start longitude
+        :param float lat0: start latitude
+        :param float lon1: stop longitude
         :param float lat1: stop latitude
         :returns: line object
         """
-        line = self.drawgreatcircle(lon0, lat0, lon1, lat1, **kwargs)
-        self.lines[line_id] = line
-        return line
-    
+        from pyproj.exceptions import GeodError
+        try:
+            line = self.drawgreatcircle(lon0, lat0, lon1, lat1, **kwargs)
+            self.lines[line_id] = line
+            return line
+        except GeodError:
+            pass #if npoints ends up 0 in basemap.drawgreatcircle body
+
     def write_point_name_2d(self, p, dist=0, angle=0, ax=None, **kwargs):
         """Annotate name of point to point in map
-        
+
         :param GeoPoint p: the point
         :param float dist: distance of annotation in km (default: 0)
         :param float angle: angular direction of  diplacement (default: 0)
         :param ax: matplotlib axes instance
         """
         if dist == 0:
-            self.draw_text_2d(p.longitude, p.latitude, p.name, ax, **kwargs) 
+            self.draw_text_2d(p.longitude, p.latitude, p.name, ax, **kwargs)
         else:
             pt = p.offset(azimuth=angle, dist_hor=dist)
             self.annotate_text_2d(pt.longitude, pt.latitude, p.name,
                                   p.longitude, p.latitude, ax, **kwargs)
-    
+
     def annotate_text_2d(self, lon_text, lat_text, text, lon_point, lat_point,
                          ax=None, **kwargs):
         """Annotate text to a certain position in a 2D basemap
-        
+
         :param float lon_text: longitude coordinate of text position
         :param float lat_text: latitude coordinate of text position
         :param str text: the actual text
         :param float lon_point: longitude of text annotation
         :param float lat_point: latitude of text annotation
-        :param **kwargs: additional keyword arguments passed to 
+        :param **kwargs: additional keyword arguments passed to
             :func:`annotate`
         """
         if ax is None:
             ax = self.ax
-        x_text, y_text = self(lon_text, lat_text)  
+        x_text, y_text = self(lon_text, lat_text)
         x_point, y_point = self(lon_point, lat_point)
-        t = ax.annotate(text, xy=(x_point, y_point), xytext=(x_text, y_text), 
+        t = ax.annotate(text, xy=(x_point, y_point), xytext=(x_text, y_text),
                         arrowprops=dict(arrowstyle="->", connectionstyle=
-                        "arc,angleA=10,armA=20,rad=6", shrinkA=2.0, 
+                        "arc,angleA=10,armA=20,rad=6", shrinkA=2.0,
                         shrinkB=10), **kwargs)
-                        
+
         self.texts[text] = t
         return t
-            
+
     def draw_text_2d(self, lon, lat, text, ax=None, **kwargs):
         """Draw a text into a 2D map
-                
+
         :param float lon: longitude of text
         :param float lat: latitude of text
         :param str text: the actual text
-        :param **kwargs: draw parameters 
+        :param **kwargs: draw parameters
         """
         if ax is None:
             ax = self.ax
-        x, y = self(lon, lat)  
+        x, y = self(lon, lat)
         t = ax.text(x, y, text, **kwargs)
         self.texts[text] = t
         return t
-    
+
     def draw_text_3d(self, lon, lat, alt, text, ax=None, **kwargs):
         """Draw a text into a 3D map
-        
+
         :param float lon: longitude of text
         :param float lat: latitude of text
         :param float alt: altitude of text (in m)
         :param str text: the actual text
-        :param **kwargs: draw parameters 
+        :param **kwargs: draw parameters
         """
         if not self._check_ax3d(ax):
-            if not self._check_ax3d(self.ax):    
+            if not self._check_ax3d(self.ax):
                 raise TypeError("No 3D Axes object available...")
             ax = self.ax
-        x, y = self(lon, lat)  
+        x, y = self(lon, lat)
         t = ax.text(x, y, alt, text, zorder=1e6, **kwargs)
         self.texts[text] = t
         return t
-    
+
     def draw_data_scatter_2d(self, data=None, lons=None, lats=None,
                              unit=None, data_id="n/d", ax=None, **kwargs):
         """Draw data into map
-        
+
         If input is unspecified, a random test data set will be created and
         plotted onto the map.
-        
+
         :param float data: the actual data
         :param float lons: array with longitude coordinates
         :param float lats: array with latitude coordinates
         :param str unit: Unit of Data for labelling
         :param str data_id: string ID under which data will be stored
         :param ax: axes object
         :param **kwargs: keyword arguments passed to :func:`scatter`
-        
+
         """
         if ax is None:
             ax = self.ax
         if not "marker" in kwargs:
             kwargs["marker"] = "^"
         if not "s" in kwargs:
             kwargs["s"] = 30
         if not any([x in kwargs for x in ["edgecolor", "edgecolors"]]):
             kwargs["edgecolor"] = "none"
-        
+
         if data is None:
             print("No input data, create random data")
             lons, lats, data = self.make_random_data()
             data_id = "TestData"
             unit = 'n/d'
-    
+
         x, y = self(lons, lats)
         z = np.array(data)
         sc = ax.scatter(x, y, c=z, **kwargs)
         zlabel = "%s [%s]" %(data_id, unit)
         self.insert_colorbar(data_id, sc, label=zlabel)
         self.plotted_data[data_id] = sc
 
     def insert_colorbar(self, obj_id, obj, label=None, ax=None, **kwargs):
         """Insert a colorbar into the map
-        
+
         :param obj_id: save ID
         :param obj: the actual artist to which the colorbar belongs
         :param str label: colorbar label
-        :param **kwargs: further arguments for :func:`colorbar` call 
+        :param **kwargs: further arguments for :func:`colorbar` call
             (see matplotlib docs)
         """
         if ax is None:
             ax = self.ax
         cb = self.fig.colorbar(obj, shrink=0.9, ax=ax, **kwargs)
         if isinstance(label, str):
             cb.set_label(label, fontsize=16)
         self.colorbars[obj_id] = cb
         ax.figure.canvas.draw()
-        
+
     def remove_colorbar(self, cb_id):
         """Remove a drawn colorbar
-        
-        :param str cb_id: string ID of colorbar        
+
+        :param str cb_id: string ID of colorbar
         """
         if not cb_id in self.colorbars:
             raise KeyError("No colorbar found with ID: " + cb_id)
         cb = self.colorbars[cb_id]
         cb.remove()
         del self.colorbars[cb_id]
         self.fig.canvas.draw()
-    
+
     @property
     def set_ax(self):
         """Check current axes and write into ``self.ax``"""
         self.ax = self._check_ax()
-        return self.ax  
-        
+        return self.ax
+
     @property
     def fig(self):
         """The current figure canvas"""
         return self.set_ax.figure
-        
+
     def remove_all_colorbars(self):
         """Remove all colorbars from map"""
         cbs = self.colorbars
         for key, cb in cbs.items():
             cb.remove()
             del self.colorbars[key]
         self.colorbars = {}
         self.fig.canvas.draw()
-        
+
     """Calculations etc
-    """    
-    
+    """
+
     def haversine(self, lon0, lat0, lon1, lat1):
         """Haversine formula (Distance between two geo coordinates)
-        
-        Approximate horizontal distance between 2 points assuming a spherical 
+
+        Approximate horizontal distance between 2 points assuming a spherical
         earth
-        
+
         :param float lon0: longitude of first point in decimal degrees
         :param float lat0: latitude of first point in decimal degrees
         :param float lon1: longitude of second point in decimal degrees
         :param float lat1: latitude of second point in decimal degrees
         """
         return haversine_formula(lon0, lat0, lon1, lat1)
-            
+
     def get_map_center(self):
         """Returns center coordinates of map (lat, lon)"""
         lon_center = self.lon_ll + self.delta_lon / 2.0
         lat_center = self.lat_ll + self.delta_lat / 2.0
         return (lat_center, lon_center)
-        
+
     """Other stuff"""
     def make_random_data(self,total_number=200, value_range=[-100, 100, 1]):
         """Create random data in the current regime"""
         from random import randrange
         lons, lats = np.zeros(total_number), np.zeros(total_number)
         data = np.zeros(total_number)
         for k in range(total_number):
             lons[k] = 0.1 * randrange(self.lon_ll * 10, self.lon_tr * 10, 1)
             lats[k] = 0.1 * randrange(self.lat_ll * 10, self.lat_tr * 10, 1)
             data[k] = randrange(value_range[0], value_range[1], value_range[2])
-            
+
         return lons, lats, data
-    
+
     """I/O, printing, etc...
     """
     def print_map_info(self):
         """Print some basic info about this map"""
         lat_center,lon_center=self.get_map_center()
         print()
         print("-------------------------------")
         print("------- MAP INFORMATION -------")
         print("-------------------------------")
         print()
         print("(Lon|Lat) lower left: (%s|%s)" %(self.lon_ll, self.lat_ll))
         print("(Lon|Lat) top right: (%s|%s)" %(self.lon_tr, self.lat_tr))
         print("(Lon|Lat) center: (%s|%s)" %(lon_center, lat_center))
         print("Projection: %s" %self.projection)
-        
+
     def save_as(self, save_dir=None, save_name=None, ftype="png"):
         """Save current figure as image"""
         import os
         if save_dir is None:
             save_dir = os.getcwd()
         if save_name is None:
             save_name = "geonum_map"
         self.fig.savefig(os.path.join(save_dir, save_name + ftype))
-        
-if __name__ == "__main__":
-    from matplotlib.pyplot import close
-    from geonum import GeoSetup
-    close("all")
-    s = GeoSetup()
-    s.create_test_data()
-    s.plot_2d()
-
```

### Comparing `geonum-1.4.5rc1/geonum/processing.py` & `geonum-1.5.0.dev9/geonum/lineongrid.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-# -*- coding: utf-8 -*-
-#
 # Geonum is a Python library for geographical calculations in 3D
 # Copyright (C) 2017 Jonas Gliss (jonasgliss@gmail.com)
 #
 # This program is free software: you can redistribute it and/or
 # modify it under the terms of the GNU General Public License a
 # published by the Free Software Foundation, either version 3 of
 # the License, or (at your option) any later version.
@@ -11,184 +9,229 @@
 # This program is distributed in the hope that it will be useful,
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
 # General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program. If not, see <http://www.gnu.org/licenses/>.
-
-"""
-Processing module of geonum library
-"""
+import matplotlib.pyplot as plt
 import numpy as np
 from scipy.ndimage import map_coordinates
 
+
 class LineOnGrid(object):
-    """A class representing a line on a discrete grid"""
-    def __init__(self, x0, y0, x1, y1, id=""):
-        """Class initialisation
-        
-        :param int x0: start x coordinate
-        :param int y0: start y coordinate
-        :param int x1: stop x coordinate
-        :param int y1: stop y coordinate
-        :param str id: string for identification (optional)
-        """
-        self.id = id
-        self.start  = [x0,y0]
-        self.stop   = [x1,y1]
-        
-        self.profile_coords = None
-        
-        #self.check_coordinates()
+    """A class representing a line on a discrete grid
+
+    Attributes
+    ----------
+    start : list
+        start location [x0, y0]
+    stop : list
+        stop location [x1, y1]
+
+    Parameters
+    ----------
+    x0 : int
+        start x coordinate
+    y0 : int
+        start y coordinate
+    x1 : int
+        end x coordinate
+    y1 : int
+        end y coordinate
+    name : int
+        string for identification (optional)
+
+    Example
+    -------
+
+    >>> import numpy as np
+    >>> from geonum import LineOnGrid
+    >>> data = np.ones((10,15)) * np.arange(15)
+    >>> line = LineOnGrid(2,2,5,5)
+    >>> profile = line.get_line_profile(data)
+    >>> print(profile)
+    [2.         2.74392912 3.50304939 4.24920976 5.        ]
+
+    """
+    def __init__(self, x0, y0, x1, y1, name=None):
+        if name is None:
+            name = 'undefined'
+        self.name = name
+        self.start = [x0, y0]
+        self.stop = [x1, y1]
+
+        self._profile_coords = None
+
         self._det_normal_vec()
-        self.prepare_profile_coordinates()
-    
-    def check_coordinates(self):
-        """Check if coordinates are in the right order and swap, if not"""
-        if any([x < 0 for x in self.start]):
-            raise ValueError("Invalid value encountered, coords must not be"
-                " smaller than 0")
-        if any([x < 0 for x in self.stop]):
-            raise ValueError("Invalid value encountered, coords must not be"
-                " smaller than 0")
-        if self.start[0] > self.stop[0]:
-            print("X coordinate of Start point is larger than X of stop point")
-            print("Start and Stop will be exchanged")
-            self.start, self.stop = self.stop, self.start
-    
-    """Processing functionality"""
-    def prepare_profile_coordinates(self):
+
+    @property
+    def profile_coords(self) -> 'numpy.ndarray':
+        """(y,x) profile coordinates"""
+        if self._profile_coords is None:
+            self._profile_coords = self._prepare_profile_coordinates()
+        return self._profile_coords
+
+
+    def _prepare_profile_coordinates(self):
         """Prepare the evaluation coordinates as stack"""
         length = self.length
-        x0, y0 = self.start     
+        x0, y0 = self.start
         x1, y1 = self.stop
-        x = np.linspace(x0, x1, length+1)
-        y = np.linspace(y0, y1, length+1)
-        self.profile_coords = np.vstack((y,x))
-    
+        x = np.linspace(x0, x1, length + 1)
+        y = np.linspace(y0, y1, length + 1)
+        return np.vstack((y, x))
+
     @property
-    def normal_vector(self):
-        """Normal vector of line"""
+    def normal_vector(self) -> tuple:
+        """Normal vector of line (x, y)"""
         return self._det_normal_vec()
-        
+
     @property
-    def length(self):
-        """Determine the length in grid coordinates"""
+    def length(self) -> int:
+        """Determine the length in units of grid indices
+
+        Note
+        ----
+        The length is rounded to integer precision.
+        """
         del_x, del_y = self._delx_dely()
         return int(round(np.hypot(del_x, del_y)))
-    
+
     def get_line_profile(self, array, **kwargs):
         """Retrieve line profile of data on a 2D array
-        
-        Uses method :func:`scipy.ndimage.map_coordinates` 
-        
+
+        Uses method :func:`scipy.ndimage.map_coordinates`
+
         Note
         ----
-        The spline interpolation will fail if there are NaNs in the input data. 
+        The spline interpolation will fail if there are NaNs in the input data.
         In this case, try using order=1 as additional input argument or use
         prefilter=False. For details see `here <https://docs.scipy.org/doc/
         scipy-0.14.0/reference/generated/scipy.ndimage.interpolation.
         map_coordinates.html>`__
-        
+
         Parameters
         ----------
-        array : ndarray
+        array : numpy.ndarray
             2D data array
         **kwargs
             additional keyword args that are passed to
             :func:`scipy.ndimage.map_coordinates`
-            
+
         Returns
         -------
-        ndarray
+        numpy.ndarray
             1D array containing the values along the line profile coordinates
         """
-        # Extract the values along the line, using cubic interpolation
-        zi = map_coordinates(array, self.profile_coords, **kwargs)
-        return zi
-    
+        return map_coordinates(array, self.profile_coords, **kwargs)
+
     def plot_line_on_grid(self, array, ax=None, **kwargs):
         """Plot this line on an input array using imshow
-        
-        :param ndarray array: the data array
-        :param **kwargs: additional keyword arguments for imshow
-        
+
+        Parameters
+        ----------
+        array : numpy.ndarray
+            the data array to which this line is mapped
+        ax : matplotlib.axes.Axes, optional
+            axes object
+        **kwargs
+            additional keyword arguments for imshow
+
+        Returns
+        -------
+        matplotlib.axes.Axes
+            axes instance used for plotting
+
         """
-        import matplotlib.pyplot as plt
         if ax is None:
-            fig, ax = plt.subplots(1,1)
-        
-        im = ax.imshow(array, cmap="gray", interpolation='none', 
-                       origin="upper", **kwargs)
+            fig, ax = plt.subplots(1, 1)
+        else:
+            fig = ax.figure
+
+        imshow_args = dict(cmap="gray", interpolation='none', origin="upper")
+        imshow_args.update(kwargs)
+        im = ax.imshow(array, **imshow_args)
         fig.colorbar(im, ax=ax, shrink=0.9)
-        ax.plot([self.start[0], self.stop[0]], [self.start[1], self.stop[1]],
+        ax.plot([self.start[0], self.stop[0]],
+                [self.start[1], self.stop[1]],
                 'co-')
-            
+
         ax.set_xlim([0, array.shape[1] - 1])
         ax.set_ylim([array.shape[0] - 1, 0])
         return ax
-    
-    def plot_line_profile(self, array, ax=None, **kwargs):
-        """Plot the line profile 
-        
-        :param ndarray array: the data array
-        :param ax (None): axes object
-        :param **kwargs: additional keyword arguments for imshow
-        
+
+    def plot_line_profile(self, array, ax=None):
+        """Plot profile of line in input data array
+
+        Parameters
+        ----------
+        array : numpy.ndarray
+            the data array to which this line is mapped
+        ax : matplotlib.axes.Axes, optional
+            axes object
+
+        Returns
+        -------
+        matplotlib.axes.Axes
+            axes instance used for plotting
         """
         if ax is None:
-            import matplotlib.pyplot as plt
-            fig, ax = plt.subplots(1,1)
+            fig, ax = plt.subplots(1, 1)
         p = self.get_line_profile(array)
         ax.set_xlim([0, self.length])
         ax.grid()
         ax.plot(p)
         ax.set_title("Line profile")
         return ax
-    
-    def plot(self, array, fig_width=12):
+
+    def plot(self, array):
         """High level plot function, calls:
-        
+
             1. :func:`plot_line_on_grid`
-            #. :func:`plot_line_profile`
-            
+            2. :func:`plot_line_profile`
+
         and puts them next to each other in a subplot
-        
-        :param ndarray array: the data array
-        :param int fig_width: width of figure in inch
-        
-        """
-        import matplotlib.pyplot as plt
-
-        dx, dy = self._delx_dely()
-        if dx > dy:
-            r = float(dy) / dx
-            h = int(fig_width * r * 2.5)
-            fig, axes = plt.subplots(2,1, figsize=(fig_width, h))
-        else:
-            fig, axes = plt.subplots(1,2, figsize = (18, 6))
+
+        Parameters
+        ----------
+        array : numpy.ndarray
+            2D data array to which this line is mapped
+
+        Returns
+        -------
+        matplotlib.figure.Figure
+            figure instance containing the plots.
+        """
+        fig, axes = plt.subplots(2, 1)
+
         self.plot_line_on_grid(array, ax=axes[0])
         self.plot_line_profile(array, ax=axes[1])
         plt.tight_layout()
-    
-    """'Private' functions"""
+        return fig
+
     def _delx_dely(self):
         """Returns length of x and y range"""
         return (abs(self.stop[0] - self.start[0]),
                 abs(self.stop[1] - self.start[1]))
-                        
+
     def _det_normal_vec(self):
-        """Determines the normal vector of the line"""
+        """Determines the normal vector (orientation) of the line
+
+        Returns
+        -------
+        tuple
+            2-element tuple containing (x, y) elements of normal vector
+        """
         delx, dely = self._delx_dely()
         try:
             a = np.arctan(float(dely) / float(delx))
         except ZeroDivisionError:
             a = np.pi / 2
         return (np.sin(a), np.cos(a))
-        
-    """Magic methods"""
+
     def __str__(self):
         """String representation"""
-        s = ("LineOnGrid %s\nStart (x,y): %s\nStop (x,y): %s\n" 
-                                        %(self.id, self.start, self.stop))
-        return s
+        s = (
+            f"LineOnGrid {self.name}. Start (x,y): {self.start}. Stop (x,"
+            f"y): {self.stop}")
+        return s
```

### Comparing `geonum-1.4.5rc1/geonum/test/test_atmosphere.py` & `geonum-1.5.0.dev9/test/test_atmosphere.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-# -*- coding: utf-8 -*-
-#
 # Geonum is a Python library for geographical calculations in 3D
 # Copyright (C) 2017 Jonas Gliss (jonasgliss@gmail.com)
 #
 # This program is free software: you can redistribute it and/or
 # modify it under the terms of the GNU General Public License a
 # published by the Free Software Foundation, either version 3 of
 # the License, or (at your option) any later version.
@@ -16,14 +14,15 @@
 # You should have received a copy of the GNU General Public License
 # along with this program. If not, see <http://www.gnu.org/licenses/>.
 
 """
 Module for atmospheric calculations relevant for geonum
 """
 import pytest
+import numpy as np
 import numpy.testing as npt
 from geonum import atmosphere as atm
 
 def test_p0():
 #: Pressure at sea level [Pa]
     assert atm.p0 == 101325.0
 
@@ -75,14 +74,18 @@
 @pytest.mark.parametrize('lat,alt,should_be',[
     (0, 0, 9.780356),
     (45, 0, 9.80616), #45deg
     (90, 0, 9.83208), #90deg
     (0, 1000, 9.471702),
     (45, 1000, 9.497733), #45deg
     (90, 1000, 9.523879), #90deg
+
+    (np.array([45,90]),np.array([0,1000]),
+     np.array([[9.80616, 9.83207964],
+               [9.49773256, 9.5238791]]))
     ])
 def test_g(lat,alt,should_be):
     val = atm.g(lat,alt)
     npt.assert_allclose(val, should_be, rtol=1e-7)
 
 @pytest.mark.parametrize('lat,should_be',[
     (0, 9.780356),
@@ -212,18 +215,21 @@
     (0,None,atm.p0,atm.T0_STD,0,atm.L_STD_ATM,atm.M_AIR_AVG,45,2.5469602223632817e+25),
     (10000,None,atm.p0,atm.T0_STD,0,atm.L_STD_ATM,atm.M_AIR_AVG,45,8.581329e+24),
     ])
 def test_air_number_density(alt,temp,ref_p,ref_temp,ref_alt,lapse_rate,mol_mass,lat,should_be):
     val = atm.air_number_density(alt,temp,ref_p,ref_temp,ref_alt,lapse_rate,mol_mass,lat)
     npt.assert_allclose(val, should_be, rtol=1e-7)
 
-# ToDo: add more tests for the functions below (so far only default input is tested)
-def test_refr_idx_300ppm_co2():
-    val = atm.refr_idx_300ppm_co2()
-    should_be=1.000291554210872
+@pytest.mark.parametrize('lbda_mu,should_be', [
+    (0.3, 1.000291554210872),
+    (0.2, 1.000324)
+    ])
+def test_refr_idx_300ppm_co2(lbda_mu,should_be):
+    val = atm.refr_idx_300ppm_co2(lbda_mu)
+
     npt.assert_allclose(val, should_be, rtol=1e-7)
 
 def test_refr_idx():
     val = atm.refr_idx()
     should_be=1.000291554210872
     npt.assert_allclose(val, should_be, rtol=1e-7)
 
@@ -239,35 +245,32 @@
 
 def test_F_AIR():
     val = atm.F_AIR()
     should_be=1.056395
     npt.assert_allclose(val, should_be, rtol=1e-5)
 
 @pytest.mark.parametrize('lbda_mu,co2_ppm,should_be', [
-    (0.3, 400,2.443366e+19),
-    (0.5, 400,2.879508e+18),
-    (0.9, 400,2.651503e+17),
+    (0.3, 400,5.652217e-26),
+    (0.5, 400,6.661139e-27),
+    (0.9, 400,6.133698e-28),
 
-    (0.5, 500,2.879819e+18),
+    (0.5, 500,6.661859e-27),
 
-    (0.5, 100,2.878574e+18),
+    (0.5, 100,6.658979e-27),
     ])
 def test_sigma_rayleigh(lbda_mu,co2_ppm,should_be):
     val = atm.sigma_rayleigh(lbda_mu,co2_ppm)
     npt.assert_allclose(val, should_be, rtol=1e-5)
 
 @pytest.mark.parametrize('alt,lbda_mu,co2_ppm,should_be', [
-    (0,0.3,400,2.993132e+16),
-    (1000,0.3,400,2.716173e+16),
-    (10000,0.3,400,1.008459e+16),
+    (0,0.3,400,1.439597e-06),
+    (1000,0.3,400,1.306389e-06),
+    (10000,0.3,400,4.850354e-07),
 
-    (0,0.5,400,3.527406e+15),
-    (0,0.9,400,3.2481e+14),
+    (0,0.5,400,1.696566e-07),
+    (0,0.9,400,1.562228e-08),
 
-    (0,0.3,400,2.993132e+16),
+    (0,0.3,400,1.439597e-06),
     ])
 def test_rayleigh_vol_sc_coeff(alt,lbda_mu,co2_ppm,should_be):
     val = atm.rayleigh_vol_sc_coeff(alt,lbda_mu,co2_ppm)
-    npt.assert_allclose(val, should_be, rtol=1e-5)
-if __name__ == '__main__':
-    import sys
-    pytest.main(sys.argv)
+    npt.assert_allclose(val, should_be, rtol=1e-5)
```

### Comparing `geonum-1.4.5rc1/geonum/test/test_base_classes.py` & `geonum-1.5.0.dev9/test/test_base_classes.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,44 +1,52 @@
 # -*- coding: utf-8 -*-
 """Test environment for base.py module."""
-import pytest
 import numpy.testing as npt
+import pytest
+
 from geonum import GeoPoint, GeoVector3D
 
+
 def test_GeoPoint():
     """Test basic arithmetic operations on GeoPoints."""
-    p = GeoPoint(lat=0, lon=0, auto_topo_access=False)
+    p = GeoPoint(latitude=0, longitude=0,
+                 auto_topo_access=False)
     assert p.latitude == 0
     assert p.longitude == 0
 
+
 def test_GeoVector3D():
     """Test basic arithmetic operations on GeoVectors."""
     v = GeoVector3D(dx=1, dy=1, dz=100)
 
-    npt.assert_array_equal([v.dx, v.dy, v.dz], [1,1,100])
+    npt.assert_array_equal([v.dx, v.dy, v.dz], [1, 1, 100])
     npt.assert_array_almost_equal([v.elevation,
                                    v.magnitude,
                                    v.azimuth,
                                    v.dist_hor],
                                   [4.044691, 1.417745, 45., 1.414214])
+
+
 def test_diffvector():
-    p1 = GeoPoint(lat=37.751005, lon=14.993435, altitude=3264.0,
+    p1 = GeoPoint(latitude=37.751005, longitude=14.993435,
+                  altitude=3264.0,
                   auto_topo_access=False)
-    p2 = GeoPoint(37.765755,  15.016696, altitude=2820.0,
+    p2 = GeoPoint(37.765755, 15.016696, altitude=2820.0,
                   auto_topo_access=False)
     connection_vector = p2 - p1
 
     assert connection_vector.anchor is p1
 
     actual = [connection_vector.azimuth,
               connection_vector.elevation,
               connection_vector.magnitude]
 
-
     npt.assert_allclose(actual=actual,
                         desired=[51.378677249653983,
                                  -9.6064174085658465,
                                  2.6606074796318557], rtol=1e-7)
 
-if __name__ == '__main__':
+
+if __name__ == "__main__":
     import sys
-    pytest.main(sys.argv)
+
+    pytest.main(sys.argv)
```

### Comparing `geonum-1.4.5rc1/geonum/test/test_helpers.py` & `geonum-1.5.0.dev9/test/test_helpers.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,23 +1,20 @@
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
-"""
-Created on Mon Feb 22 15:11:33 2021
-
-@author: jonasg
-"""
-
 import pytest
 import os, shutil
 import numpy as np
 import numpy.testing as npt
 from geonum import LOCAL_TOPO_DIR, TOPO_INFO_FILE
-from geonum.conftest import does_not_raise_exception
 from geonum import helpers as h
 
+@pytest.mark.parametrize('num,result', [
+    (10, 1), (1000, 3), (1.2,0), (0.023, -2)
+])
+def test_order_of_magnitude(num,result):
+    assert h.order_of_magnitude(num) == result
+
 def test_all_topodata_search_dirs():
     all_dirs = h.all_topodata_search_dirs()
     assert isinstance(all_dirs, list)
     assert LOCAL_TOPO_DIR in all_dirs
     for dirloc in all_dirs:
         assert os.path.exists(dirloc)
 
@@ -60,18 +57,12 @@
     (-90,0,90,0,500,500 * np.pi), # half around the equator
     ])
 def test_haversine_formula(lon0,lat0,lon1,lat1,radius,value):
     val = h.haversine_formula(lon0, lat0, lon1, lat1, radius)
     npt.assert_allclose(val, value, rtol=1e-5)
 
 
-
-
-
-
-
-
-if __name__ == '__main__':
+if __name__ == "__main__":
     import sys
     pytest.main(sys.argv)
```

### Comparing `geonum-1.4.5rc1/geonum/test/test_srtmpy_lib.py` & `geonum-1.5.0.dev9/test/test_srtmpy_lib.py`

 * *Files 15% similar despite different names*

```diff
@@ -18,10 +18,10 @@
     assert not fh.exists('nonexistingfile.hgt')
     assert os.path.exists(fh.local_cache_dir)
 
 def test_get_data():
     acc = srtm.get_data()
     assert isinstance(acc, srtm.data.GeoElevationData)
 
-if __name__ == '__main__':
+if __name__ == "__main__":
     import sys
     pytest.main(sys.argv)
```

### Comparing `geonum-1.4.5rc1/geonum/topodata.py` & `geonum-1.5.0.dev9/geonum/topodata.py`

 * *Files 9% similar despite different names*

```diff
@@ -49,41 +49,71 @@
     lats : ndarray
         numpy array with latitude coordinates of the topographic dataset.
         Accessible via :attr:`latitude`.
     lons : ndarray
         numpy array with longitude coordinates of the topographic dataset.
         Accessible via :attr:`longitude`.
     data : ndarray
-        2D numpy array containing elevation values.
+        2D numpy array containing elevation values, first index denotes
+        latitude dimension, 2nd index denotes longitude dimension.
     data_id : str
         ID of this data set.
     repl_nan_minval : bool
-        coordinates containing NaN values are replaced with the minimum
-        altitude in the range.
+        if True, then coordinates containing NaN values are replaced with the
+        minimum altitude in `data`.
     """
-    def __init__(self, lats, lons, data, data_id="", repl_nan_minval=False):
-        self.data_id = data_id #: ID of topodata file
+    def __init__(self, lats, lons, data, data_id=None, repl_nan_minval=False):
+        if data_id is None:
+            data_id = 'undefined'
+        self.data_id = data_id
+
+        lats = np.asarray(lats)
+        lons = np.asarray(lons)
+        data = np.asarray(data)
+        if not data.shape == (len(lats), len(lons)):
+            raise ValueError(
+                'shape mismatch between input lats and lons and data...'
+                )
+
+        self.lats = lats
+        self.lons = lons
+        self.data = data
 
-        self.lats = lats #
-        self.lons = lons #asarray(lons)
 
         if repl_nan_minval:
             self.replace_nans()
 
-        self.data = data
+    def __str__(self):
+        return (
+            f'geonum.TopoData (data_id: {self.data_id})\n'
+            f'Dimensions: {self.dims}, shape: {self.shape}\n'
+            f'latitude range: {self.lat0} - {self.lat1}\n'
+            f'longitude range: {self.lon0} - {self.lon1}\n'
+            f'data: {type(self.data)}\n{self.data}'
+            )
+
+    def __repr__(self):
+        return (f'geonum.TopoData (data_id: {self.data_id}, shape: {self.shape})\n')
 
     @property
     def latitude(self):
         """Wrapper for :attr:`lats`"""
         return self.lats
 
     @property
     def longitude(self):
-        """Wrapper for :attr:`lats`"""
-        return self.lats
+        """Wrapper for :attr:`lons`"""
+        return self.lons
+
+    @property
+    def dims(self):
+        """
+        list: List of dimension names
+        """
+        return ['latitude', 'longitude']
 
     def replace_nans(self, fillval=None):
         """Replace NaNs in topographic data with a fill value
 
         Parameters
         ----------
         fillval : float
@@ -137,29 +167,31 @@
     def resolution(self):
         """Returns tuple (lat, lon) of the current grid resolution in km
 
         Note
         ----
         The resolution is determined at the center of this grid
         """
+        if not len(self.lons) > 1 or not len(self.lats) > 1:
+            raise ValueError('Need at least 2x2 sized topofield')
         x_lon, x_lat = int(len(self.lons) / 2), int(len(self.lats) / 2)
         p0 = LatLon(self.lats[x_lat], self.lons[x_lon])
-        r_lon = (p0 - LatLon(self.lats[x_lat], self.lons[x_lon + 1])).magnitude
-        r_lat = (p0 - LatLon(self.lats[x_lat + 1], self.lons[x_lon])).magnitude
+        r_lon = (p0 - LatLon(self.lats[x_lat], self.lons[x_lon-1])).magnitude
+        r_lat = (p0 - LatLon(self.lats[x_lat-1], self.lons[x_lon])).magnitude
         return (r_lat, r_lon)
 
     def mean(self):
         """Mean elevation (ignores NaNs in data)"""
         return np.nanmean(self.data)
 
     def std(self):
         """Standard deviation of topographic dataset"""
         return np.nanstd(self.data)
 
-    def increase_grid_resolution(self, res=0.2, polyorder=2):
+    def increase_grid_resolution(self, res=0.2, polyorder=2): # pragma: no cover
         """Gaussian pyramide based upscaling of topographic grid
 
         This function checks the current topographic resolution in the center
         of the grid. Based on this, an upsacling factor is determined and the
         :func:`cv2.pyrUp` is used to increase the resolution using
         interpolation. Note, that this does not increase the actual resolution
         of the topographic data grid.
@@ -228,16 +260,28 @@
 
     @property
     def center_coordinates(self):
         """Tuple (lat, lon) with center coordinates of data"""
         return (self.lats[0] + self.delta_lat / 2.,
                 self.lons[0] + self.delta_lon / 2.)
 
+    def init_mesh(self):
+        """
+        Init X,Y meshgrid from latitudes and longitudes for map plots
+
+        Returns
+        -------
+        list
+            meshgrid
+
+        """
+        return np.meshgrid(self.longitude, self.latitude)
+
     def plot(self, plot3d=True, draw_coastlines=False,
-             draw_mapscale=False, **kwargs):
+             draw_mapscale=False, **kwargs): # pragma: no cover
         from geonum.mapping import Map
         if not "projection" in kwargs:
             kwargs["projection"] = "lcc"
         if not "llcrnrlon" in kwargs:
             kwargs["llcrnrlat"] = self.lat0
             kwargs["llcrnrlon"] = self.lon0
             kwargs["urcrnrlat"] = self.lat1
@@ -261,28 +305,28 @@
             if draw_coastlines:
                 m.draw_coastlines()
             m.draw_coordinates()
             if draw_mapscale:
                 m.draw_mapscale_auto()
         return m
 
-    def plot_2d(self, ax=None):
+    def plot_2d(self, ax=None): # pragma: no cover
         """Plot 2D basemap of topodata"""
         from geonum.mapping import Map
         latc, lonc = self.center_coordinates
         m = Map(self.lon0, self.lat0, self.lon1, self.lat1,
                 projection="merc", lat_0=latc, lon_0=lonc, ax=ax)
         m.set_topo_data(self)
         m.draw_topo(insert_colorbar=True)
         m.draw_topo_contour()
         m.draw_coordinates()
         m.drawcoastlines()
         return m
 
-    def plot_3d(self, ax=None):
+    def plot_3d(self, ax=None): # pragma: no cover
         """Creates 3D surface plot of data
 
         Parameters
         ----------
         ax
             instance of matplotlib Axes3D object
 
@@ -305,28 +349,28 @@
         if not (self.lat0 <= lat <= self.lat1 and
                 self.lon0 <= lon <= self.lon1):
             print("Input coordinates out of topo data range...")
             return False
         return True
 
     def closest_index(self, lat, lon):
-        """Finds closest index to input coordinate
+        """Finds the closest index to input coordinate
 
         Parameters
         ----------
         lat : float
             latitude coordinate in decimal degrees
         lon : float
             longitude coordinate in decimal degrees
 
         Returns
         -------
         tuple
-            2-element tuple containing closest index of lat and lon arrays to
-            to input index
+            2-element tuple containing the closest index of lat and lon
+            arrays to input index
 
         Raises
         ------
         ValueError
             if input coordinate is not included in this dataset
         """
         if not self.includes_coordinate(lat, lon):
@@ -346,25 +390,17 @@
         lon : int or float
             longitude of coordinate
 
         Returns
         -------
         float
             altitude at input coordinate
-
-        Raises
-        ------
-        ValueError
-            if retrieved altitude value is NaN
         """
         idx_lat, idx_lon = self.closest_index(lat, lon)
-        dat = self.data[idx_lat, idx_lon]
-        if np.isnan(dat):
-            raise ValueError("Invalid value encountered in topodata...")
-        return dat
+        return self.data[idx_lat, idx_lon]
 
     def __call__(self, lat, lon):
         """Get altitude value at input position"""
         try:
             return self.get_altitude(lat, lon)
         except ValueError as e:
             raise e
```

### Comparing `geonum-1.4.5rc1/geonum/topodataaccess.py` & `geonum-1.5.0.dev9/geonum/topodataaccess.py`

 * *Files 5% similar despite different names*

```diff
@@ -23,115 +23,116 @@
 import os
 
 from geonum.exceptions import InvalidTopoMode, TopoAccessError
 from geonum.topoaccessbase import SRTMAccess, Etopo1Access
 
 class TopoDataAccess(object):
     """Factory class for accessing topographic data
-    
+
     This is a high-level factory class which handles the access of topography
-    data. Registered topographic datasets can be found in :attr:`REGISTERED` 
-    
-    Default access mode is SRTM (topographic dataset from NASA 
-    `Shuttle Radar Topography Mission <https://www2.jpl.nasa.gov/srtm/>`__). 
-    
+    data. Registered topographic datasets can be found in :attr:`REGISTERED`
+
+    Default access mode is SRTM (topographic dataset from NASA
+    `Shuttle Radar Topography Mission <https://www2.jpl.nasa.gov/srtm/>`__).
+
     Example
     -------
-    
+
     >>> acc = TopoDataAccess(mode='srtm')
     >>> topo_data = acc.get_data(lat0=5, lon0=30, lat1=15, lon1=40)
-        
+
     Note
     ----
-    
-    For developers: the registered access  classes (such as 
-    :class:`SRTMAccess`) should be based on (or follow the API of) template 
+
+    For developers: the registered access  classes (such as
+    :class:`SRTMAccess`) should be based on (or follow the API of) template
     base class :class:`TopoAccessBase`.
-    
-    
+
+
     Attributes
     ----------
     mode : str
         current access mode (string specifying which topographic dataset is
-        supposed to be used for access). 
+        supposed to be used for access).
     local_path : str
         local path to etopo data (only relevant for etopo1 mode)
-        
+
     Parameters
     ----------
     mode : str
         one of the supported data access types (cf. keys of :attr:`REGISTERED`)
     local_path : str
         local path to etopo data (only relevant for etopo1 mode)
     """
     #: supported access modes (topographic datasets)
     REGISTERED = dict(srtm      = SRTMAccess,
                       etopo1    = Etopo1Access)
-    
-    def __init__(self, mode="srtm", local_path=None):
+    DEFAULT_MODE = 'srtm'
+    def __init__(self, mode=None, local_path=None):
+        if mode is None:
+            mode = self.DEFAULT_MODE
         #mode and data access variables
         if not mode in self.REGISTERED:
             raise InvalidTopoMode(mode)
         self.mode = mode
-    
+
         self.local_path = local_path
-        
+
     @property
     def modes(self):
         """List of supported topographic datasets"""
         return list(self.REGISTERED.keys())
-    
+
     @property
     def supported(self):
         """List of supported datasets (wrapper for :attr:`modes`)"""
         return self.modes
-    
+
     def __deepcopy__(self, memo):
         return TopoDataAccess(self.mode, self.local_path)
-    
-    def get_data(self, lat0, lon0, lat1=None, lon1=None, 
-                 mode=None, local_path=None, check_allnan=True, 
+
+    def get_data(self, lat0, lon0, lat1=None, lon1=None,
+                 mode=None, local_path=None, check_allnan=True,
                  **access_opts):
         """Retrieve data from topography file
-        
+
         Parameters
         ----------
-        lat0 : float 
+        lat0 : float
             start longitude for data extraction
-        lon0 : float 
+        lon0 : float
             start latitude for data extraction
-        lat1 : float 
-            stop longitude for data extraction (default: None). If None only 
+        lat1 : float
+            stop longitude for data extraction (default: None). If None only
             data around lon0, lat0 will be extracted.
         lon1 : float
-            stop latitude for data extraction (default: None). 
+            stop latitude for data extraction (default: None).
             If None only data around lon0, lat0 will be extracted
         mode : str, optional
             mode specifying the topographic dataset that is supposed to be used
         local_path : str, optional
             local path where topography data is stored (can be dictionary or
-            filepath, is passed to corresponding access class and handled 
+            filepath, is passed to corresponding access class and handled
             as implemented there)
         check_allnan : bool
             if True and all retrieved values are NaN, then an error is thrown
         **access_opts
-            additional access options that may be specific for the mode 
+            additional access options that may be specific for the mode
             specified (e.g. search_database in case of etopo1)
-        
-        
+
         Returns
         -------
         TopoData
             object containing the data
-        
+
         Raises
         ------
         TopoAccessError
             if access fails
-        
+
         """
         if mode is not None:
             if not mode in self.REGISTERED:
                 raise InvalidTopoMode(mode)
             self.mode = mode
         if local_path is not None and os.path.exists(local_path):
             self.local_path=local_path
```

### Comparing `geonum-1.4.5rc1/geonum.egg-info/SOURCES.txt` & `geonum-1.5.0.dev9/geonum.egg-info/SOURCES.txt`

 * *Files 27% similar despite different names*

```diff
@@ -1,31 +1,40 @@
 LICENSE
 MANIFEST.in
 README.rst
-VERSION.rst
 setup.py
 geonum/__init__.py
+geonum/_init_helpers.py
 geonum/atmosphere.py
 geonum/conftest.py
 geonum/elevationprofile.py
 geonum/exceptions.py
 geonum/geopoint.py
 geonum/geosetup.py
 geonum/geovector3d.py
 geonum/helpers.py
+geonum/lineongrid.py
 geonum/mapping.py
-geonum/processing.py
+geonum/plot_helpers.py
 geonum/topoaccessbase.py
 geonum/topodata.py
 geonum/topodataaccess.py
+geonum/utils.py
 geonum.egg-info/PKG-INFO
 geonum.egg-info/SOURCES.txt
 geonum.egg-info/dependency_links.txt
 geonum.egg-info/top_level.txt
-geonum/test/__init__.py
-geonum/test/test_atmosphere.py
-geonum/test/test_base_classes.py
-geonum/test/test_elevationprofile.py
-geonum/test/test_helpers.py
-geonum/test/test_srtm_access.py
-geonum/test/test_srtmpy_lib.py
-geonum/test/test_topodata.py
+test/__init__.py
+test/test_atmosphere.py
+test/test_base_classes.py
+test/test_elevationprofile.py
+test/test_geopoint.py
+test/test_geosetup.py
+test/test_geovector3d.py
+test/test_helpers.py
+test/test_lineongrid.py
+test/test_plot_helpers.py
+test/test_srtmpy_lib.py
+test/test_topoaccessbase.py
+test/test_topodata.py
+test/test_topodataaccess.py
+test/test_utils.py
```

