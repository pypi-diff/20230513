# Comparing `tmp/rad-tools-0.6.0.tar.gz` & `tmp/rad-tools-0.6.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rad-tools-0.6.0.tar", last modified: Tue May  9 00:29:06 2023, max compression
+gzip compressed data, was "rad-tools-0.6.1.tar", last modified: Sat May 13 01:38:04 2023, max compression
```

## Comparing `rad-tools-0.6.0.tar` & `rad-tools-0.6.1.tar`

### file list

```diff
@@ -1,48 +1,48 @@
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:06.049432 rad-tools-0.6.0/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     1071 2022-10-03 15:21:14.000000 rad-tools-0.6.0/LICENSE.txt
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     2840 2023-05-09 00:29:06.048835 rad-tools-0.6.0/PKG-INFO
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     2123 2023-05-09 00:12:40.000000 rad-tools-0.6.0/README.rst
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:05.959755 rad-tools-0.6.0/rad_tools/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      613 2023-05-09 00:15:00.000000 rad-tools-0.6.0/rad_tools/__init__.py
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:05.974783 rad-tools-0.6.0/rad_tools/dos/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      183 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/dos/__init__.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)    21740 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/dos/dos.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)    22059 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/dos/pdos.py
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:05.980888 rad-tools-0.6.0/rad_tools/exchange/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      253 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/exchange/__init__.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     7428 2023-05-07 21:38:27.000000 rad-tools-0.6.0/rad_tools/exchange/bond.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)    27641 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/exchange/model.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     1196 2023-03-30 12:48:24.000000 rad-tools-0.6.0/rad_tools/exchange/template.py
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:05.985855 rad-tools-0.6.0/rad_tools/io/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      549 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/io/__init__.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     1956 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/io/internal.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     4042 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/io/tb2j.py
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:05.988981 rad-tools-0.6.0/rad_tools/kpoints/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      616 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/kpoints/__init__.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)    30577 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/kpoints/high_symmetry_point.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     3626 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/kpoints/kpoints.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     1284 2023-03-30 12:48:24.000000 rad-tools-0.6.0/rad_tools/map.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     6315 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/routines.py
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:05.996356 rad-tools-0.6.0/rad_tools/score/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     1584 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/score/__init__.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     4511 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/score/extract_tb2j.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     4054 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/score/identify_wannier_centres.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     4758 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/score/make_template.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)    13305 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/score/plot_dos.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     9921 2023-05-09 00:12:40.000000 rad-tools-0.6.0/rad_tools/score/plot_tb2j.py
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:05.971291 rad-tools-0.6.0/rad_tools.egg-info/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     2840 2023-05-09 00:29:05.000000 rad-tools-0.6.0/rad_tools.egg-info/PKG-INFO
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     1008 2023-05-09 00:29:05.000000 rad-tools-0.6.0/rad_tools.egg-info/SOURCES.txt
--rw-r--r--   0 rybakov.ad   (501) staff       (20)        1 2023-05-09 00:29:05.000000 rad-tools-0.6.0/rad_tools.egg-info/dependency_links.txt
--rw-r--r--   0 rybakov.ad   (501) staff       (20)       22 2023-05-09 00:29:05.000000 rad-tools-0.6.0/rad_tools.egg-info/requires.txt
--rw-r--r--   0 rybakov.ad   (501) staff       (20)       10 2023-05-09 00:29:05.000000 rad-tools-0.6.0/rad_tools.egg-info/top_level.txt
-drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-09 00:29:06.039860 rad-tools-0.6.0/scripts/
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     3225 2023-03-30 12:48:24.000000 rad-tools-0.6.0/scripts/compute-energies.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     2933 2023-03-30 12:48:24.000000 rad-tools-0.6.0/scripts/phonopy-plotter.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      292 2023-05-09 00:12:40.000000 rad-tools-0.6.0/scripts/rad-extract-tb2j.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      304 2023-05-09 00:12:40.000000 rad-tools-0.6.0/scripts/rad-identify-wannier-centres.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      293 2023-05-09 00:12:40.000000 rad-tools-0.6.0/scripts/rad-make-template.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      288 2023-05-09 00:12:40.000000 rad-tools-0.6.0/scripts/rad-plot-dos.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)      289 2023-05-09 00:12:40.000000 rad-tools-0.6.0/scripts/rad-plot-tb2j.py
--rw-r--r--   0 rybakov.ad   (501) staff       (20)       38 2023-05-09 00:29:06.049565 rad-tools-0.6.0/setup.cfg
--rw-r--r--   0 rybakov.ad   (501) staff       (20)     1400 2023-05-09 00:12:40.000000 rad-tools-0.6.0/setup.py
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.090298 rad-tools-0.6.1/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     1071 2022-10-03 15:21:14.000000 rad-tools-0.6.1/LICENSE.txt
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     2859 2023-05-13 01:38:04.089830 rad-tools-0.6.1/PKG-INFO
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     2142 2023-05-12 23:13:20.000000 rad-tools-0.6.1/README.rst
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.064351 rad-tools-0.6.1/rad_tools/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      561 2023-05-13 01:32:49.000000 rad-tools-0.6.1/rad_tools/__init__.py
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.070122 rad-tools-0.6.1/rad_tools/dos/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      183 2023-05-13 01:31:59.000000 rad-tools-0.6.1/rad_tools/dos/__init__.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)    21722 2023-05-13 01:08:44.000000 rad-tools-0.6.1/rad_tools/dos/dos.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)    22436 2023-05-13 01:11:24.000000 rad-tools-0.6.1/rad_tools/dos/pdos.py
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.074891 rad-tools-0.6.1/rad_tools/exchange/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      253 2023-05-09 00:12:40.000000 rad-tools-0.6.1/rad_tools/exchange/__init__.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     7700 2023-05-13 01:07:33.000000 rad-tools-0.6.1/rad_tools/exchange/bond.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)    28094 2023-05-13 01:21:46.000000 rad-tools-0.6.1/rad_tools/exchange/model.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     1198 2023-05-13 01:12:42.000000 rad-tools-0.6.1/rad_tools/exchange/template.py
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.077418 rad-tools-0.6.1/rad_tools/io/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      547 2023-05-13 01:31:59.000000 rad-tools-0.6.1/rad_tools/io/__init__.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     1930 2023-05-13 01:23:59.000000 rad-tools-0.6.1/rad_tools/io/internal.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     4054 2023-05-13 01:24:34.000000 rad-tools-0.6.1/rad_tools/io/tb2j.py
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.081169 rad-tools-0.6.1/rad_tools/kpoints/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      616 2023-05-09 00:12:40.000000 rad-tools-0.6.1/rad_tools/kpoints/__init__.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)    30577 2023-05-12 23:13:20.000000 rad-tools-0.6.1/rad_tools/kpoints/high_symmetry_point.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     3626 2023-05-09 00:12:40.000000 rad-tools-0.6.1/rad_tools/kpoints/kpoints.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     1284 2023-03-30 12:48:24.000000 rad-tools-0.6.1/rad_tools/map.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     3372 2023-05-13 01:31:59.000000 rad-tools-0.6.1/rad_tools/routines.py
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.084943 rad-tools-0.6.1/rad_tools/score/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     1539 2023-05-13 01:31:59.000000 rad-tools-0.6.1/rad_tools/score/__init__.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     4512 2023-05-13 00:20:50.000000 rad-tools-0.6.1/rad_tools/score/extract_tb2j.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     3715 2023-05-13 00:12:08.000000 rad-tools-0.6.1/rad_tools/score/identify_wannier_centres.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     4705 2023-05-13 00:23:29.000000 rad-tools-0.6.1/rad_tools/score/make_template.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)    13248 2023-05-13 01:31:59.000000 rad-tools-0.6.1/rad_tools/score/plot_dos.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     9938 2023-05-13 01:31:55.000000 rad-tools-0.6.1/rad_tools/score/plot_tb2j.py
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.067139 rad-tools-0.6.1/rad_tools.egg-info/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     2859 2023-05-13 01:38:03.000000 rad-tools-0.6.1/rad_tools.egg-info/PKG-INFO
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     1008 2023-05-13 01:38:04.000000 rad-tools-0.6.1/rad_tools.egg-info/SOURCES.txt
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)        1 2023-05-13 01:38:03.000000 rad-tools-0.6.1/rad_tools.egg-info/dependency_links.txt
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)       32 2023-05-13 01:38:03.000000 rad-tools-0.6.1/rad_tools.egg-info/requires.txt
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)       10 2023-05-13 01:38:03.000000 rad-tools-0.6.1/rad_tools.egg-info/top_level.txt
+drwxr-xr-x   0 rybakov.ad   (501) staff       (20)        0 2023-05-13 01:38:04.089275 rad-tools-0.6.1/scripts/
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     3225 2023-03-30 12:48:24.000000 rad-tools-0.6.1/scripts/compute-energies.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     2933 2023-03-30 12:48:24.000000 rad-tools-0.6.1/scripts/phonopy-plotter.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      293 2023-05-13 01:31:59.000000 rad-tools-0.6.1/scripts/rad-extract-tb2j.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      305 2023-05-13 01:31:59.000000 rad-tools-0.6.1/scripts/rad-identify-wannier-centres.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      294 2023-05-13 01:31:59.000000 rad-tools-0.6.1/scripts/rad-make-template.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      289 2023-05-13 01:31:59.000000 rad-tools-0.6.1/scripts/rad-plot-dos.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)      290 2023-05-13 01:31:59.000000 rad-tools-0.6.1/scripts/rad-plot-tb2j.py
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)       38 2023-05-13 01:38:04.090456 rad-tools-0.6.1/setup.cfg
+-rw-r--r--   0 rybakov.ad   (501) staff       (20)     1413 2023-05-12 23:45:26.000000 rad-tools-0.6.1/setup.py
```

### Comparing `rad-tools-0.6.0/LICENSE.txt` & `rad-tools-0.6.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `rad-tools-0.6.0/PKG-INFO` & `rad-tools-0.6.1/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rad-tools
-Version: 0.6.0
+Version: 0.6.1
 Summary: Scripts for condense matter calculations and post-processing.
 Home-page: https://rad-tools.adrybakov.com/en/stable/
 Download-URL: https://github.com/adrybakov/rad-tools.git
 Author: Andrey Rybakov
 Author-email: rybakov.ad@icloud.com
 License: MIT license
 Classifier: Development Status :: 3 - Alpha
@@ -45,16 +45,16 @@
 
 It is expected to be used in two ways:
 
 * As Python library
 
 * Via scripts (i.e. usage from command line)
 
-Documentations is available 
-`here. <https://rad-tools.adrybakov.com>`_
+For the detailed descriprion check
+`documentation. <https://rad-tools.adrybakov.com>`_
 
 Installation
 ============
 
 Requirement for RAD-tools installation are:
 
 * Python itself (>=3.6)
@@ -78,21 +78,21 @@
 
 * Clone the project to your local computer:
 
 .. code-block:: python
 
    git clone git@github.com:adrybakov/rad-tools.git
 
-Change the directory:
+* Change the directory:
 
 .. code-block:: python
 
    cd rad-tools
 
-To install RAD-tools, run (you may need to use ``pip3``):
+* To install RAD-tools, run (you may need to use ``pip3``):
 
 .. code-block:: console
 
    pip install rad-tools
 
 Additionally you may run the unit tests, 
 which requires pytest (requires Python 3.7+) to be installed:
```

### Comparing `rad-tools-0.6.0/README.rst` & `rad-tools-0.6.1/README.rst`

 * *Files 11% similar despite different names*

```diff
@@ -26,16 +26,16 @@
 
 It is expected to be used in two ways:
 
 * As Python library
 
 * Via scripts (i.e. usage from command line)
 
-Documentations is available 
-`here. <https://rad-tools.adrybakov.com>`_
+For the detailed descriprion check
+`documentation. <https://rad-tools.adrybakov.com>`_
 
 Installation
 ============
 
 Requirement for RAD-tools installation are:
 
 * Python itself (>=3.6)
@@ -59,21 +59,21 @@
 
 * Clone the project to your local computer:
 
 .. code-block:: python
 
    git clone git@github.com:adrybakov/rad-tools.git
 
-Change the directory:
+* Change the directory:
 
 .. code-block:: python
 
    cd rad-tools
 
-To install RAD-tools, run (you may need to use ``pip3``):
+* To install RAD-tools, run (you may need to use ``pip3``):
 
 .. code-block:: console
 
    pip install rad-tools
 
 Additionally you may run the unit tests, 
 which requires pytest (requires Python 3.7+) to be installed:
```

### Comparing `rad-tools-0.6.0/rad_tools/__init__.py` & `rad-tools-0.6.1/rad_tools/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,28 +1,24 @@
 r"""
 All tools from the package.
 
 
 |version|
 """
 
-__version__ = "0.6.0"
+__version__ = "0.6.1"
 
 
-from . import score
-from .score import *
-from . import io
-from .io import *
-from . import exchange
+from . import dos, exchange, io, kpoints, score
+from .dos import *
 from .exchange import *
-from . import kpoints
+from .io import *
 from .kpoints import *
-from . import dos
-from .dos import *
 from .routines import *
+from .score import *
 
 __all__ = []
 __all__.extend(score.__all__)
 __all__.extend(io.__all__)
 __all__.extend(exchange.__all__)
 __all__.extend(kpoints.__all__)
 __all__.extend(dos.__all__)
```

### Comparing `rad-tools-0.6.0/rad_tools/dos/dos.py` & `rad-tools-0.6.1/rad_tools/dos/dos.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,43 +1,43 @@
 r"""
 DOS
 """
 import re
 from os import walk
-from os.path import abspath, join
+from os.path import join
 
 import matplotlib.pyplot as plt
 import numpy as np
 
 from rad_tools.dos.pdos import PDOSQE
 
 
 class DOSQE:
     r"""
-    Analyse the folder with the Quantum Espresso results and store all information.
+    Analyse the folder with the |QE|_ results and store all information.
 
     Parameters
     ----------
     seedname : str
-        Seedname for the Quantum Espresso output files.
+        Seedname for the |QE|_ output files.
     input_folder : str
-        Path to the folder with Quantum Espresso output files.
+        Path to the folder with |QE|_ output files.
     energy_window : tuple, default None
         Energy limits, necessary for correct plotting.
 
     Attributes
     ----------
     seedname : str
-        Seedname for the Quantum Espresso output files.
+        Seedname for the |QE|_ output files.
     energy : array
         Energy values of the DOS/PDOS.
     k_resolved : bool
     case : int
     casename : str
-        Human readable name of the case base on ``case``.
+        Human readable name of the case base on :py:attr:`.case`.
     nkpoints : int
         Number of k points for k resolved DOS. 1 if DOS is not k resolved.
     nepoints : int
         Number of energy points.
     filenames : list
     atoms : list
     """
@@ -207,16 +207,16 @@
 
         return self._filenames
 
     def _decompose_filenames(self):
         r"""
         Decompose filenames and extract information about atoms and projectors.
 
-        Note
-        ----
+        Notes
+        -----
         atoms : dist
             Dictionary with the atom labels and their numbers.
 
             .. code-block:: python
 
                 atoms = {atom1: [n_1, n_2, n_3, ...]}
         wfcs : dict
@@ -271,15 +271,15 @@
         Parameters
         ----------
         squeeze : bool, default False
             Whether to sum over k points. Ignored if DOS is not k resolved.
 
         Returns
         -------
-        total_dos : array
+        total_dos : :numpy:`ndarray`
             Shape :math:`(2, n_e)` if DOS is collinear, spin-polarized;
             :math:`(n_e)` otherwise.
         """
 
         dos = np.loadtxt(
             join(self._input_path, f"{self.seedname}.pdos_tot"), skiprows=1
         ).T
@@ -318,15 +318,15 @@
         Parameters
         ----------
         squeeze : bool, default False
             Whether to sum over k points. Ignored if DOS is not k resolved.
 
         Returns
         -------
-        total_pdos : array
+        total_pdos : :numpy:`ndarray`
             Shape :math:`(2, n_e)` if PDOS is collinear, spin-polarized;
             :math:`(n_e)` otherwise.
         """
 
         dos = np.loadtxt(
             join(f"{self._input_path}", f"{self.seedname}.pdos_tot"), skiprows=1
         ).T
@@ -525,15 +525,15 @@
         Plot total DOS vs total PDOS.
 
         Parameters
         ----------
         output_name : str
             Name of the output file.
         interactive : bool, default False
-            Whether to plot in interactive matplotlib window.
+            Whether to plot in interactive |matplotlib|_ window.
         efermi : float, default 0
             Fermi energy. Zero of energy scale is shifted to it.
         xlim : tuple, default None
             Limits for energy scale.
         ylim : tuple, default None
             Limits for dos scale.
         save_pickle : bool, default False
```

### Comparing `rad-tools-0.6.0/rad_tools/dos/pdos.py` & `rad-tools-0.6.1/rad_tools/dos/pdos.py`

 * *Files 4% similar despite different names*

```diff
@@ -12,44 +12,44 @@
 class PDOS:
     r"""
     Partial density of states, projected on arbitrary projections.
 
     Supports k-resolved density of states.
     Support spin-polarised and spin-unpolarised cases.
 
-    PDOS class is iterable (over ``projectors``) and
+    PDOS class is iterable (over :py:attr:`.projectors`) and
     supports item call (return PDOS for ``key`` projector).
 
-    Operations of addition and substruction are defined.
+    Operations of addition and subtraction are defined.
 
     Parameters
     ----------
-    energy : array
+    energy : |array_like|_
         Values of energy for the PDOS. Shape :math:`n_e` is assumed.
-    pdos : array
+    pdos : |array_like|_
         Array with the values of PDOS. Shape is assumed to be:
 
         * Spin-polarized, k-resolved: :math:`(n, 2, n_k, n_e)`
         * Spin-unpolarized, k-resolved: :math:`(n, n_k, n_e)`
         * Spin-polarized, non k-resolved: :math:`(n, 2, n_e)`
         * Spin-unpolarized, non k-resolved: :math:`(n, n_e)`
 
         where :math:`n` is the number of projections,
         :math:`n_k` is the number of k-points,
         :math:`n_e` is the number of energy points.
     projectors_group : str
         Name of the projectors group.
     projectors : list
         Names of the projectors.
-        If ``projectors_group`` has the form "l" or "l_j",
+        If :py:attr:`projectors_group` has the form "l" or "l_j",
         where l is "s", "p", "d", "f" and j is the total angular momentum,
         the projectors are assigned automatically,
         otherwise it is necessary to provide :math:`n` projectors manually.
         The names of projectors are directly used in the plots.
-    ldos : array, default None
+    ldos : |array_like|_, default None
         Local density of states. Sum of partial density of states over all projectors.
         Computed based on ``pdos`` if not provided.
         Shape is assumed to be:
 
         * Spin-polarized, k-resolved: :math:`(2, n_k, n_e)`
         * Spin-unpolarized, k-resolved: :math:`(n_k, n_e)`
         * Spin-polarized, non k-resolved: :math:`(2, n_e)`
@@ -58,18 +58,18 @@
         where :math:`n_k` is the number of k-points,
         :math:`n_e` is the number of energy points.
     spin_pol : bool, default False
         Whether PDOS is spin-polarized or not.
 
     Attributes
     ----------
-    energy : array
+    energy : :numpy:`ndarray`
         Values of energy for the PDOS. Has the shape :math:`n_e`.
-    ldos : array
-    pdos : array
+    ldos : :numpy:`ndarray`
+    pdos : :numpy:`ndarray`
     projectors_group : str
         Name of the projectors group.
     projectors : list
         Names of the projectors.
     spin_pol : bool, default False
         Whether PDOS is spin-polarized or not.
     k_resolved : bool, default False
@@ -80,15 +80,15 @@
         energy,
         pdos,
         projectors_group: str,
         projectors,
         ldos=None,
         spin_pol=False,
     ):
-        self.energy = energy
+        self.energy = np.array(energy)
         self._pdos = None
         self._ldos = None
         self.projectors_group = projectors_group
         self.projectors = projectors
         self.spin_pol = spin_pol
 
         self.pdos = pdos
@@ -169,30 +169,30 @@
 
         Parameters
         ----------
         key : str or int
             Projector`s name or index.
         Returns
         -------
-        pdos : array
+        pdos : :numpy:`ndarray`
             Partial density of states.
         """
         if isinstance(key, str):
             key = self.projectors.index(key)
 
         return self.pdos[key]
 
     @property
     def ldos(self) -> np.ndarray:
         r"""
         Local density of states.
 
         Returns
         -------
-        ldos : array
+        ldos : :numpy:`ndarray`
             Summed density of states along all projectors.
             Has the following shapes:
 
             * Spin-polarized, k-resolved: :math:`(2, n_k, n_e)`
             * Spin-unpolarized, k-resolved: :math:`(n_k, n_e)`
             * Spin-polarized, non k-resolved: :math:`(2, n_e)`
             * Spin-unpolarized, non k-resolved: :math:`(n_e)`
@@ -229,15 +229,15 @@
     @property
     def pdos(self) -> np.ndarray:
         r"""
         Partial density of states.
 
         Returns
         -------
-        pdos : array
+        pdos : :numpy:`ndarray`
             Has the following shapes:
 
             * Spin-polarized, k-resolved: :math:`(n, 2, n_k, n_e)`
             * Spin-unpolarized, k-resolved: :math:`(n, n_k, n_e)`
             * Spin-polarized, non k-resolved: :math:`(n, 2, n_e)`
             * Spin-unpolarized, non k-resolved: :math:`(n, n_e)`
 
@@ -269,48 +269,55 @@
                 f"PDOS does not match with projectors: "
                 + f"{len(self.projectors)} projectors, {self.pdos.shape[0]} PDOS"
             )
 
     @property
     def k_resolved(self):
         r"""
-        Check if pdos is k-resolved based on shape of ``self.pdos``.
+        Check if pdos is k-resolved based on shape of :py:attr:`.pdos`.
         """
 
         return (
             self.spin_pol
             and len(self.pdos.shape) == 4
             or not self.spin_pol
             and len(self.pdos.shape) == 3
         )
 
     def squeeze(self):
         r"""
         Squeeze k-resolved PDOS.
 
+        See Also
+        --------
+        squeezed : Returns new object.
+
         Notes
         -----
         It modifies the instance on which called.
-        See also :py:func:`.PDOS.squeezed`
         """
 
         if self.k_resolved:
             self._pdos = np.sum(self._pdos, axis=1 + int(self.spin_pol))
             self._ldos = np.sum(self._ldos, axis=int(self.spin_pol))
 
     def squeezed(self):
         r"""
         Return new instance with squeezed PDOS.
 
-        Calls :py:func:`PDOS.squeeze`.
+        Calls :py:func:`.PDOS.squeeze`.
 
         Returns
         -------
-        pdos_squeezed : :py:class:`PDOS`
+        pdos_squeezed : :py:class:`.PDOS`
             Squeezed PDOS.
+
+        See Also
+        --------
+        squeeze : Modifies current object.
         """
 
         squeezed_pdos = deepcopy(self)
         squeezed_pdos.squeeze()
         return squeezed_pdos
 
     def normalize(self):
@@ -323,18 +330,22 @@
         .. math::
             x_i(E, k) \rightarrow \dfrac{x_i(E, k)}{\sum_{j=0}^{n} x_j(E, k)}
 
         where :math:`n` is the total number of projectors.
         Those sums are computed individually for spin-up and
         spin-down in the spin-polarized case.
 
+        See Also
+        --------
+        normalized : Returns new object.
+
         Notes
         -----
         It modifies the instance on which called.
-        See also :py:func:`PDOS.normalized`
+
         """
 
         for i in range(0, self.pdos.shape[0]):
             self._pdos[i] = np.where(self.ldos > 10e-8, self._pdos[i] / self.ldos, None)
         self._ldos = np.where(self.ldos > 10e-8, self._ldos / self.ldos, 0)
 
     def normalized(self):
@@ -343,14 +354,18 @@
 
         Calls :py:func:`PDOS.normalize`.
 
         Returns
         -------
         normalized_pdos : :py:class:`PDOS`
             Normalized PDOS.
+
+        See Also
+        --------
+        normalize : Modifies current object.
         """
 
         normalized_pdos = deepcopy(self)
         normalized_pdos.normalize()
         return normalized_pdos
 
     def dump_txt(self, ouptut_name):
@@ -433,28 +448,27 @@
 class PDOSQE(PDOS):
     r"""
     PDOS wrapper for |QE|_ pdos.
 
     Supports the order of projectors of |projwfc|_ (s,p,d,f) and
     the case of projection in the spin-orbit calculations.
     In the custom cases it is necessary to specify projectors manually.
-    If ``projectors_group`` has the form "l" or "l_j",
+    If :py:attr:`.projectors_group` has the form "l" or "l_j",
     where l is "s", "p", "d", "f" and j is the total angular momentum,
     the projectors are assigned automatically,
     otherwise it is necessary to provide :math:`n` projectors manually.
     The names of projectors are directly used in the plots.
-    If ``projectors_group`` is one of "s", "p", "d", "f", then the projectors are:
+    If :py:attr:`.projectors_group` is one of "s", "p", "d", "f", then the projectors are:
 
     * s : :math:`s`
     * p : :math:`p_z`, :math:`p_y`, :math:`p_x`
     * d : :math:`d_{z^2}`, :math:`d_{zx}`, :math:`d_{zy}`, :math:`d_{x^2 - y^2}`, :math:`d_{xy}`
     * f : :math:`f_{z^3}`, :math:`f_{yz^2}`, :math:`f_{xz^2}`, :math:`f_{z(x^2 - y^2)}`, :math:`f_{xyz}`, :math:`f_{y(3x^2 - y^2)}`, :math:`f_{x(x^2 - 3y^2)}`
 
-    If ``projectors_group`` has the form "l_j", then the projectors are :math:`(1, ..., 2j+1)`
-
+    If :py:attr:`.projectors_group` has the form "l_j", then the projectors are :math:`(1, ..., 2j+1)`
     """
 
     _pattern = "[spdf]_j[0-9.]*"
     _projectors = {
         "s": ["s"],
         "p": ["$p_z$", "$p_y$", "$p_x$"],
         "d": ["$d_{z^2}$", "$d_{zx}$", "$d_{zy}$", "$d_{x^2 - y^2}$", "$d_{xy}$"],
@@ -508,15 +522,15 @@
     save_pickle=False,
 ):
     r"""
     Plot PDOS.
 
     Parameters
     ----------
-    pdos : PDOS
+    pdos : :py:class:`.PDOS`
         PDOS for the plot.
     efermi : float, default 0
         Fermi energy.
     output_name : str, default "pdos"
         output_name for the plot file. Extension ".png" is added at the end.
     title : str, default None
         Title of the plot. Passed to the ``ax.set_title()``.
```

### Comparing `rad-tools-0.6.0/rad_tools/exchange/bond.py` & `rad-tools-0.6.1/rad_tools/exchange/bond.py`

 * *Files 13% similar despite different names*

```diff
@@ -16,41 +16,33 @@
     then it is derived from ``iso``, ``aniso`` and ``dmi``.
     If nothing is provided exchange matrix is set to zero matrix.
 
     Parameters
     ----------
     iso : int or float, default None
         Value of isotropic exchange parameter.
-    aniso : 3 x 3 array, None
+    aniso : (3, 3) |array_like|_, default None
         3 x 3 matrix of symmetric anisotropic exchange.
-    dmi : 1 x 3 array, None
+    dmi : (3,) |array_like|_, default None
         Dzyaroshinsky-Moria interaction vector :math:`(D_x, D_y, D_z)`.
-    matrix : 3 x 3 array, None
+    matrix : (3, 3) |array_like|_, default None
         Exchange matrix.
 
     Attributes
     ----------
-    matrix : 3 x 3 array of floats
-        Exchange matrix.
-
-        .. code-block:: python
-
-            [[J_xx, J_xy, J_xz],
-             [J_yx, J_yy, J_yz],
-             [J_zx, J_zy, J_zz]]
-
-    symm_matrix : 3 x 3 array of floats
-    asymm_matrix : 3 x 3 array of floats
+    matrix : 3 x 3 :numpy:`ndarray`
+    symm_matrix : (3, 3) :numpy:`ndarray`
+    asymm_matrix : (3, 3) :numpy:`ndarray`
     iso : float
-    iso_matrix : 3 x 3 array of floats
-    aniso : 3 x 3 array of floats
-    aniso_diagonal : 1 x 3 array of floats
-    aniso_diagonal_matrix : 3 x 3 array of floats
-    dmi : 1 x 3 array of floats
-    dmi_matrix : 3 x 3 array of floats
+    iso_matrix : (3, 3) :numpy:`ndarray`
+    aniso : (3, 3) :numpy:`ndarray`
+    aniso_diagonal : (3,) :numpy:`ndarray`
+    aniso_diagonal_matrix : (3, 3) :numpy:`ndarray`
+    dmi : (3,) :numpy:`ndarray`
+    dmi_matrix : (3, 3) :numpy:`ndarray`
     dmi_module : float
     """
 
     def __init__(self, matrix=None, iso=None, aniso=None, dmi=None) -> None:
         self._matrix = np.zeros((3, 3), dtype=float)
         self._iso = 0.0
         self._aniso = np.zeros((3, 3), dtype=float)
@@ -60,53 +52,63 @@
             self.iso = iso
             self.dmi = dmi
             self.aniso = aniso
         else:
             self.matrix = matrix
 
     @property
-    def matrix(self):
+    def matrix(self) -> np.ndarray:
+        r"""
+        Full exchange matrix.
+
+        .. code-block:: python
+
+            [[J_xx, J_xy, J_xz],
+             [J_yx, J_yy, J_yz],
+             [J_zx, J_zy, J_zz]]
+        """
+
         return self._matrix
 
     @matrix.setter
     def matrix(self, new_matrix):
         if new_matrix is not None:
             new_matrix = np.array(new_matrix, dtype=float)
             if new_matrix.shape != (3, 3):
                 raise ValueError("Matrix shape has to be equal to (3, 3)")
         else:
             new_matrix = np.zeros((3, 3), dtype=float)
         self._matrix = new_matrix
 
     @property
-    def symm_matrix(self):
+    def symm_matrix(self) -> np.ndarray:
         r"""
-        Symmetric part of exchange matrix.
+        Symmetric part of exchange :py:attr:`matrix`.
 
         .. math::
 
             J_{symm} = \dfrac{J + J^T}{2}
         """
 
         return (self.matrix + self.matrix.T) / 2
 
     @property
-    def asymm_matrix(self):
+    def asymm_matrix(self) -> np.ndarray:
         """
-        Asymmetric part of exchange matrix.
+        Asymmetric part of exchange :py:attr:`matrix`.
 
         .. math::
 
             J_{asymm} = \dfrac{J - J^T}{2}
         """
 
         return (self.matrix - self.matrix.T) / 2
 
     @property
-    def iso(self):
+    def iso(self) -> float:
         r"""
         Value of isotropic exchange parameter.
 
         Derived from the exchange matrix (:math:`\mathbf{J}`) as
 
         .. math::
             J_{iso} = \dfrac{1}{3}Tr(\mathbf{J})
@@ -120,31 +122,31 @@
             # correction is correct (see matrix update)
             new_iso = new_iso - self.iso
         else:
             new_iso = -self.iso
         self.matrix = self.matrix + (new_iso) * np.identity(3, dtype=float)
 
     @property
-    def iso_matrix(self):
+    def iso_matrix(self) -> np.ndarray:
         r"""
-        Isotropic part of the exchange matrix.
+        Isotropic part of the exchange :py:attr:`matrix`.
 
         Matrix form:
 
         .. code-block:: python
 
             [[J, 0, 0],
              [0, J, 0],
              [0, 0, J]]
         """
 
         return self.iso * np.identity(3, dtype=float)
 
     @property
-    def aniso(self):
+    def aniso(self) -> np.ndarray:
         r"""
         3 x 3 matrix of symmetric anisotropic exchange.
 
         .. code-block:: python
 
             [[J_xx, J_xy, J_xz],
              [J_xy, J_yy, J_yz],
@@ -170,41 +172,41 @@
             # correction is correct (see matrix update)
             new_aniso = new_aniso - self.aniso
         else:
             new_aniso = -self.aniso
         self.matrix = self.matrix + new_aniso
 
     @property
-    def aniso_diagonal(self):
+    def aniso_diagonal(self) -> np.ndarray:
         r"""
         Diagonal part of the symmetric anisotropic exchange.
 
         .. code-block:: python
 
             [J_xx, J_yy, J_zz]
         """
 
         return np.diag(self.aniso)
 
     @property
-    def aniso_diagonal_matrix(self):
+    def aniso_diagonal_matrix(self) -> np.ndarray:
         r"""
-        Diagonal part of the symmetric anisotropic exchange matrix.
+        Diagonal part of the symmetric anisotropic exchange.
 
         .. code-block:: python
 
             [[J_xx, 0, 0],
              [0, J_yy, 0],
              [0, 0, J_zz]]
         """
 
         return np.diag(np.diag(self.aniso))
 
     @property
-    def dmi(self):
+    def dmi(self) -> np.ndarray:
         r"""
         Dzyaroshinsky-Moria interaction vector (Dx, Dy, Dz).
 
         .. code-block:: python
 
             [D_x, D_y, D_z]
         """
@@ -230,42 +232,42 @@
                 [new_dmi[1], -new_dmi[0], 0],
             ],
             dtype=float,
         )
         self.matrix = self.matrix + dmi_matrix
 
     @property
-    def dmi_matrix(self):
+    def dmi_matrix(self) -> np.ndarray:
         r"""
-        Asymmetric part of the exchange matrix.
+        Asymmetric part of the exchange :py:attr:`matrix`.
 
         .. code-block:: python
 
             [[0, D_z, -D_y],
              [-D_z, 0, D_x],
              [D_y, -D_x, 0]]
         """
 
         return self.asymm_matrix
 
     @property
-    def dmi_module(self):
+    def dmi_module(self) -> float:
         r"""
         Length of the DMI vector in the units of exchange interaction.
         """
 
         return sqrt(np.sum(self.dmi**2))
 
     def round(self, decimals=4):
         r"""Round exchange values.
 
         Parameters
         ----------
-        accuracy : int, default 4
-            number of decimals after the point.
+        decimals : int, default 4
+            Number of decimals after the coma.
         """
 
         self.matrix = np.round(self.matrix, decimals=decimals)
 
     def __add__(self, other):
         if isinstance(other, Bond):
             matrix = self.matrix + other.matrix
```

### Comparing `rad-tools-0.6.0/rad_tools/exchange/model.py` & `rad-tools-0.6.1/rad_tools/exchange/model.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 r"""
 Exchange model.
 
-Write a tutorial with docstrings here.
+Write a tutorial with docstring here.
 """
 
 from copy import deepcopy
 from math import cos, pi, sin, sqrt
 
 import numpy as np
 
@@ -27,25 +27,25 @@
             {(Atom_1, Atom_2, R): bond, ...}
     magnetic_atoms : dict
         Dictionary with keys : str - marks of atoms and value : 1 x 3 array
         - coordinate of the atom in Angstroms.
     nonmagnetic_atoms : dist
         Dictionary with keys : str - marks of atoms and value : 1 x 3 array
         - coordinate of the atom in Angstroms. Only non-magnetic atoms.
-    cell : 3 x 3 array of floats
-    a : 3 x 1 array
-    b : 3 x 1 array
-    c : 3 x 1 array
+    cell : (3, 3) :numpy:`ndarray`
+    a : (3,) :numpy:`ndarray`
+    b : (3,) :numpy:`ndarray`
+    c : (3,) :numpy:`ndarray`
     len_a : float
     len_b : float
     len_c : float
     unit_cell_volume : float
-    b1 : 3 x 1 array
-    b2 : 3 x 1 array
-    b3 : 3 x 1 array
+    b1 : (3,) :numpy:`ndarray`
+    b2 : (3,) :numpy:`ndarray`
+    b3 : (3,) :numpy:`ndarray`
     cell_list : list
     number_spins_in_unit_cell : int
 
     space_dimensions : tuple of floats
     """
 
     def __init__(self) -> None:
@@ -221,15 +221,15 @@
         List of cells from the model.
 
         Return the list of R for all cell that are present in the model.
         Not ordered.
 
         Returns
         -------
-        cells : n x 3 array
+        cells : (n, 3) :numpy:`ndarray`
             Array of n unit cells.
         """
 
         cells = set()
         for atom1, atom2, R in self:
             cells.add(R)
         return np.array(list(cells))
@@ -296,15 +296,15 @@
 
     def add_bond(self, bond: Bond, atom1, atom2, R):
         r"""
         Add one bond to the model.
 
         Parameters
         ----------
-        bond : :py:class:`Bond`
+        bond : :py:class:`.Bond`
             An instance of :py:class:`Bond` class with the information about
             exchange parameters.
         atom1 : str
             Name of atom1 in (0, 0, 0) unit cell.
         atom2 : str
             Name of atom2 in R unit cell.
         R : tuple of ints
@@ -352,15 +352,15 @@
 
         self.magnetic_atoms[name] = np.array([a, b, c])
 
     def remove_atom(self, name):
         r"""
         Remove magnetic atom from the model.
 
-        Note: this method will remove atom from ``magnetic_atoms`` and all the
+        Note: this method will remove atom from :py:attr:`magnetic_atoms` and all the
         bonds, which starts or ends in this atom.
 
         Parameters
         ----------
         name : str
             Mark for the atom.
         """
@@ -379,15 +379,15 @@
         r"""
         Getter for the atom coordinates.
 
         Parameters
         ----------
         atom : str
             Name of atom1 in R unit cell.
-        R : 1 x 3 array, default (0, 0, 0)
+        R : (3,) |array_like|_, default (0, 0, 0)
             Radius vector of the unit cell for atom2.
 
         Returns
         -------
         coordinates : 1 x 3 array
             Coordinates of atom in the cell R in real space.
         """
@@ -404,20 +404,20 @@
 
         Parameters
         ----------
         atom1 : str
             Name of atom1 in (0, 0, 0) unit cell.
         atom2 : str
             Name of atom2 in R unit cell.
-        R : tuple of ints, default (0, 0, 0)
+        R : (3,) |array_like|_, default (0, 0, 0)
             Radius vector of the unit cell for atom2.
 
         Returns
         -------
-        coordinates : 1 x 3 array
+        coordinates : (3,) :numpy:`ndarray`
             Coordinates of the middle of a bond in real space.
         """
 
         atom1 = self.get_atom_coordinates(atom1)
         atom2 = self.get_atom_coordinates(atom2, R)
 
         return (atom1 + atom2) / 2
@@ -428,20 +428,20 @@
 
         Parameters
         ----------
         atom1 : str
             Name of atom1 in (0, 0, 0) unit cell.
         atom2 : str
             Name of atom2 in R unit cell.
-        R : tuple of ints, default (0, 0, 0)
+        R : (3,) |array_like|_, default (0, 0, 0)
             Radius vector of the unit cell for atom2.
 
         Returns
         -------
-        v : 1 x 3 array
+        v : (3,) :numpy:`ndarray`
             Vector from atom1 to atom2 of the bond.
         """
 
         atom1 = self.get_atom_coordinates(atom1)
         atom2 = self.get_atom_coordinates(atom2, R)
 
         return atom2 - atom1
@@ -452,15 +452,15 @@
 
         Parameters
         ----------
         atom1 : str
             Name of atom1 in (0, 0, 0) unit cell.
         atom2 : str
             Name of atom2 in R unit cell.
-        R : tuple of ints, default (0, 0, 0)
+        R : (3,) |array_like|_, default (0, 0, 0)
             Radius vector of the unit cell for atom2.
 
         Returns
         -------
         distance : floats
             Distance between atom1 and atom2.
         """
@@ -473,31 +473,36 @@
         r"""
         Filter the exchange entries based on the given conditions.
 
         The result will be defined by logical conjugate of the conditions.
         Saying so the filtering will be performed for each given condition
         one by one.
 
-        .. note::
-            This method modifies the instance at which it is called.
-
         Parameters
         ----------
         max_distance : float or int, optional
             Distance for sorting, the condition is <<less or equal>>.
         min_distance : float or int, optional
             Distance for sorting, the condition is <<more or equal>>.
         template : list or :py:class:`.ExchangeTemplate`.
             List of pairs, which will remain in the model. ::
 
                 [(atom1, atom2, R), ...]
 
         R_vector : tuple of ints or list of tuples of ints
             Tuple of 3 integers or list of tuples, specifying the R vectors,
             which will be kept after filtering.
+
+        See Also
+        --------
+        filtered : Returns new object.
+
+        Notes
+        -----
+        This method modifies the instance at which it is called.
         """
 
         if isinstance(template, ExchangeTemplate):
             template = template.get_list()
         if template is not None:
             template = set(template)
         if R_vector is not None:
@@ -527,23 +532,24 @@
             self.remove_bond(atom1, atom2, R)
 
     def remove(self, template):
         r"""
         Remove bonds from the exchange model, based on the template.
 
 
-        .. note::
-            This method modifies the instance at which it is called.
-
         Parameters
         ----------
         template : list or :py:class:`.ExchangeTemplate`.
             List of pairs, which will remain in the model. ::
 
                 [(atom1, atom2, R), ...]
+
+        Notes
+        -----
+        This method modifies the instance at which it is called.
         """
 
         if isinstance(template, ExchangeTemplate):
             template = template.get_list()
         template = set(template)
 
         for atom1, atom2, R in template:
@@ -558,19 +564,14 @@
         The result will be defined by logical conjugate of the conditions.
         Saying so the filtering will be performed for each given condition
         one by one.
         Note: this method is not modifying the instance at which it is called.
         It will create a new instance with sorted :py:attr:`bonds` and all
         the other attributes will be copied (through :py:func:`deepcopy`).
 
-        .. note::
-            This method is not modifying the instance at which it is called.
-            It will create a new instance with merged ``bonds`` and all the
-            other attributes will be copied (through deepcopy).
-
         Parameters
         ----------
         max_distance : float or int, optional
             Distance for sorting, the condition is <<less or equal>>.
         min_distance : float or int, optional
             Distance for sorting, the condition is <<more or equal>>.
         template : list or :py:class:`.ExchangeTemplate`
@@ -582,14 +583,24 @@
             Tuple of 3 integers or list of tuples, specifying the R vectors,
             which will be kept after filtering.
 
         Returns
         -------
         filtered_model : :py:class:`.ExchangeModel`
             Exchange model after filtering.
+
+        See Also
+        --------
+        filter : Modifies current object.
+
+        Notes
+        -----
+        This method is not modifying the instance at which it is called.
+        It creates a new instance with merged :py:attr:`.bonds` and all the
+        other attributes will be copied (through deepcopy).
         """
 
         filtered_model = deepcopy(self)
         filtered_model.filter(
             max_distance=max_distance,
             min_distance=min_distance,
             template=template,
@@ -607,14 +618,18 @@
 
         This method modifies an instance on which it was called.
 
         Parameters
         ----------
         template : :py:class:`.ExchangeTemplate`
             Template.
+
+        See Also
+        --------
+        forced_symmetry : Returns new object.
         """
 
         if not isinstance(template, ExchangeTemplate):
             raise TypeError
 
         self.filter(template=template)
 
@@ -650,14 +665,18 @@
         template : :py:class:`.ExchangeTemplate`
             Template.
 
         Returns
         -------
         new_model : :py:class:`.ExchangeModel`
             Exchange model with forced symmetry.
+
+        See Also
+        --------
+        force_symmetry: Modifies current object.
         """
 
         new_model = deepcopy(self)
         new_model.force_symmetry(template=template)
         return new_model
 
     def summary_as_txt(
```

### Comparing `rad-tools-0.6.0/rad_tools/exchange/template.py` & `rad-tools-0.6.1/rad_tools/exchange/template.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 r"""
 Exchange template.
 
-Write a tutorial with docstrings here.
+Write a tutorial with docstring here.
 """
 
 
 class ExchangeTemplate:
     r"""
-    Store a template for sorting the exchange from TB2J file.
+    Store a template for sorting the exchange from |TB2J|_ file.
 
     In addition stores the technical details for plotting,
     orbital decomposition, etc.
 
     Attributes
     ----------
     names : dict
```

### Comparing `rad-tools-0.6.0/rad_tools/io/__init__.py` & `rad-tools-0.6.1/rad_tools/io/__init__.py`

 * *Files 21% similar despite different names*

```diff
@@ -5,13 +5,11 @@
 data structures from the input data of the external programs, 
 as well as from the internal-specified formats.
 """
 
 from rad_tools.io.internal import read_template
 from rad_tools.io.tb2j import read_exchange_model as read_tb2j_model
 
-
 from .internal import read_template
 from .tb2j import read_exchange_model
 
-
 __all__ = ["read_template", "read_exchange_model"]
```

### Comparing `rad-tools-0.6.0/rad_tools/io/internal.py` & `rad-tools-0.6.1/rad_tools/io/internal.py`

 * *Files 5% similar despite different names*

```diff
@@ -18,17 +18,16 @@
     Returns
     -------
     template : :py:class:`.ExchangeTemplate`
         Exchange template.
 
     Notes
     -----
-    See also :ref:`Template specification <api>`
+    See also :ref:`Template specification <api>`.
     """
-    # TODO change the link
 
     # Constants
     major_sep = "=" * 20
     minor_sep = "-" * 20
     neighbors_flag = "Neighbors template:"
 
     template = ExchangeTemplate()
```

### Comparing `rad-tools-0.6.0/rad_tools/io/tb2j.py` & `rad-tools-0.6.1/rad_tools/io/tb2j.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,32 +1,32 @@
 r"""
-Input-output from TB2J.
+Input-output from |TB2J|_.
 """
 
 import numpy as np
 
 from rad_tools.exchange.model import Bond, ExchangeModel
 from rad_tools.routines import absolute_to_relative
 
 
 def read_exchange_model(filename, quiet=False) -> ExchangeModel:
     r"""
-    Read exchange model from TB2J output file.
+    Read exchange model from |TB2J|_ output file.
 
     Parameters
     ----------
     filename : str
-        Path to the TB2J output file.
+        Path to the |TB2J|_ output file.
     quiet : bool, default True
         Whether to suppress output.
 
     Returns
     -------
     model : :py:class:`.ExchangeModel`
-        Exchange model build from TB2J file.
+        Exchange model build from |TB2J|_ file.
     """
 
     major_sep = "=" * 90
     minor_sep = "-" * 88
     garbage = str.maketrans(
         {"(": None, ")": None, "[": None, "]": None, ",": None, "'": None}
     )
```

### Comparing `rad-tools-0.6.0/rad_tools/kpoints/__init__.py` & `rad-tools-0.6.1/rad_tools/kpoints/__init__.py`

 * *Files identical despite different names*

### Comparing `rad-tools-0.6.0/rad_tools/kpoints/high_symmetry_point.py` & `rad-tools-0.6.1/rad_tools/kpoints/high_symmetry_point.py`

 * *Files identical despite different names*

### Comparing `rad-tools-0.6.0/rad_tools/kpoints/kpoints.py` & `rad-tools-0.6.1/rad_tools/kpoints/kpoints.py`

 * *Files identical despite different names*

### Comparing `rad-tools-0.6.0/rad_tools/map.py` & `rad-tools-0.6.1/rad_tools/map.py`

 * *Files identical despite different names*

### Comparing `rad-tools-0.6.0/rad_tools/score/__init__.py` & `rad-tools-0.6.1/rad_tools/score/__init__.py`

 * *Files 13% similar despite different names*

```diff
@@ -31,29 +31,19 @@
         from rad_tools import make_template
         
         make_template(output_name="template",
             input_filename="exchange.out",
             max_distance=5)
 """
 
-from .identify_wannier_centres import (
-    manager as identify_wannier_centres,
-)
-from .plot_tb2j import (
-    manager as plot_tb2j,
-)
-from .extract_tb2j import (
-    manager as extract_tb2j,
-)
-from .plot_dos import (
-    manager as plot_dos,
-)
-from .make_template import (
-    manager as make_template,
-)
+from .extract_tb2j import manager as extract_tb2j
+from .identify_wannier_centres import manager as identify_wannier_centres
+from .make_template import manager as make_template
+from .plot_dos import manager as plot_dos
+from .plot_tb2j import manager as plot_tb2j
 
 __all__ = [
     "identify_wannier_centres",
     "plot_tb2j",
     "extract_tb2j",
     "plot_dos",
     "make_template",
```

### Comparing `rad-tools-0.6.0/rad_tools/score/extract_tb2j.py` & `rad-tools-0.6.1/rad_tools/score/extract_tb2j.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 from argparse import ArgumentParser
 from calendar import month_name
 from datetime import datetime
 from os import makedirs
 from os.path import abspath, join
 
+from termcolor import cprint
+
 from rad_tools import __version__ as version
 from rad_tools.io import read_tb2j_model
 from rad_tools.io.internal import read_template
-from rad_tools.routines import OK, RESET
 
 
 def manager(
     input_filename,
     template_file,
     output_path=".",
     output_name=None,
@@ -62,17 +63,18 @@
         with open(join(output_path, output_name + ".txt"), "w") as out_file:
             out_file.write(
                 f"Exchange values are extracted from: {input_filename}\n"
                 + f"on {cd.day} {month_name[cd.month]} {cd.year}"
                 + f" at {cd.hour}:{cd.minute}:{cd.second} by rad-tools {version}\n\n"
             )
             out_file.write(summary_txt)
-        print(
-            f"{OK}Extracted exchange info is in "
-            + f"{abspath(join(output_path, output_name + '.txt'))}{RESET}"
+        cprint(
+            f"Extracted exchange info is in "
+            + f"{abspath(join(output_path, output_name + '.txt'))}",
+            "green",
         )
     else:
         print(f"{summary_txt}")
 
 
 def create_parser():
     parser = ArgumentParser(
```

### Comparing `rad-tools-0.6.0/rad_tools/score/identify_wannier_centres.py` & `rad-tools-0.6.1/rad_tools/score/identify_wannier_centres.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 #! /usr/local/bin/python3
 
 from argparse import ArgumentParser
 from os.path import join, split
 
 import numpy as np
+from termcolor import cprint
 
-from rad_tools.routines import cprint
 
-
-def manager(filename, span, output_path, output_name, no_colour=False):
+def manager(filename, span, output_path, output_name):
     r"""
     ``rad-identify-wannier-centres.py`` script.
 
     Full documentation on the behaviour is available in the
     :ref:`User Guide <rad-identify-wannier-centres>`.
     Parameters of the function directly
     correspond to the arguments of the script.
@@ -53,21 +52,18 @@
         min_span = 10000
         name = "None"
         for atom, a_coord in atoms:
             if np.linalg.norm((centre[1] - a_coord)) < min_span:
                 min_span = np.linalg.norm((centre[1] - a_coord))
                 name = atom
         if min_span - span > separation_tolerance:
-            if no_colour:
-                print(f"Centre {centre} unidentified, " + "try to increase span")
-            else:
-                cprint(
-                    f"Centre {centre} unidentified, " + "try to increase span",
-                    colour="yellow",
-                )
+            cprint(
+                f"Centre {centre} unidentified, " + "try to increase span",
+                "yellow",
+            )
             print(
                 f"    span limit = {span}\n"
                 + f"    minimum distance to the atom ({name}) = {min_span:.8f}\n"
             )
             centre[0] = f"None, closest: {name} ({min_span:.8f})"
         else:
             centre[0] = name
@@ -118,15 +114,8 @@
     parser.add_argument(
         "-on",
         "--output-name",
         type=str,
         default=None,
         help="Seedname for the output files.",
     )
-    parser.add_argument(
-        "-nc",
-        "--no-colour",
-        action="store_true",
-        default=False,
-        help="Turn off coloured output.",
-    )
     return parser
```

### Comparing `rad-tools-0.6.0/rad_tools/score/make_template.py` & `rad-tools-0.6.1/rad_tools/score/make_template.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 from argparse import ArgumentParser
 from calendar import month_name
 from datetime import datetime
 from os import makedirs
 from os.path import abspath, split
 
 import numpy as np
+from termcolor import cprint
 
 from rad_tools import __version__ as version
 from rad_tools.io.tb2j import read_exchange_model
-from rad_tools.routines import OK, RESET, YELLOW
 
 
 def manager(
     output_name="template",
     input_filename=None,
     R_vector=None,
     max_distance=None,
@@ -98,19 +98,16 @@
                 + "\n"
             )
             for atom1, atom2, R in model.bonds:
                 file.write(
                     f"{atom1:4} {atom2:4} " + f"{R[0]:3.0f} {R[1]:3.0f} {R[2]:3.0f}\n"
                 )
             file.write("=" * 20 + "\n")
-    print(f"{OK}Template draft is in " + f"{abspath(output_name)}.txt{RESET}")
-    print(
-        f"{YELLOW}Do not forget to correct the template draft "
-        + f"to your needs!{RESET}"
-    )
+    cprint(f"Template draft is in " + f"{abspath(output_name)}.txt", "green")
+    cprint(f"Do not forget to correct the template draft to your needs!", "yellow")
 
 
 def create_parser():
     parser = ArgumentParser(
         description="Script for the creation of template`s template"
     )
```

### Comparing `rad-tools-0.6.0/rad_tools/score/plot_dos.py` & `rad-tools-0.6.1/rad_tools/score/plot_dos.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 # TODO Fix background total + non-colinear-nonspin-orbit
 
 import re
 from argparse import ArgumentParser
 from os import makedirs, walk
 from os.path import abspath, join
 
+from termcolor import cprint
 from tqdm import tqdm
 
-from rad_tools.dos import DOSQE, plot_projected, PDOS
-from rad_tools.routines import cprint
+from rad_tools.dos import DOSQE, PDOS, plot_projected
 
 
 def detect_seednames(input_path):
     r"""
     Analyze input folder, detects seednames for the dos output files.
 
     Parameters
@@ -82,48 +82,48 @@
         suffix += "-vstotal"
 
     # Detect seednames if not provided.
     if seedname is None:
         seednames = detect_seednames(input_path)
         print(f"Following DOS seednames (filpdos) are detected:")
         for item in seednames:
-            cprint(f"   * {item}", colour="yellow")
+            cprint(f"   * {item}", "green")
     else:
         seednames = [seedname]
 
     # Work with each seedname.
     for s_i, seedname in enumerate(seednames):
         cprint(
             f"({s_i + 1}/{len(seednames)}) Start to work with {seedname} seedname",
-            colour="yellow",
+            "green",
         )
         # Preparations
         output_root = join(output_path, f"{seedname}{suffix}")
         makedirs(output_root, exist_ok=True)
 
         # Load DOS data.
         dos = DOSQE(seedname, input_path, energy_window=energy_window, efermi=efermi)
         print(f"{dos.casename} case detected.")
         for atom in dos.atoms:
             print(f"    {len(dos.atom_numbers(atom))} of {atom} detected")
 
         # Plot PDOS vs DOS
-        cprint("Total DOS vs total PDOS", colour="yellow")
+        cprint("Total DOS vs total PDOS", "green")
         dos.plot_pdos_tot(
             output_name=join(output_root, "pdos-vs-dos"),
             interactive=interactive,
             efermi=efermi,
             xlim=energy_window,
             ylim=dos_window,
             save_pickle=save_pickle,
         )
         print(f"  Result is in {join(output_root, 'pdos-vs-dos')}")
 
         # Plot PDOS for each atom/wfc
-        cprint("Orbital-resolved PDOS:", colour="yellow")
+        cprint("Orbital-resolved PDOS:", "green")
         local_output = join(output_root, "orbital-resolved")
         makedirs(local_output, exist_ok=True)
         data = {}
         for atom, atom_number, wfc, wfc_number in dos:
             if atom not in data:
                 data[atom] = []
             data[atom].append((wfc, wfc_number))
@@ -178,15 +178,15 @@
                         normalize=normalize,
                         interactive=interactive,
                         save_pickle=save_pickle,
                     )
         print(f"  Results are in {abspath(local_output)}")
 
         # Plot wfc contribution into each atom
-        cprint("Orbital's contribution for each atom.", colour="yellow")
+        cprint("Orbital's contribution for each atom.", "green")
         local_output = join(output_root, "atom-resolved")
         makedirs(local_output, exist_ok=True)
 
         for atom in dos.atoms:
             if separate:
                 atom_numbers = dos.atom_numbers(atom)
             else:
@@ -237,15 +237,15 @@
                     normalize=normalize,
                     interactive=interactive,
                     save_pickle=save_pickle,
                 )
         print(f"  Results are in {abspath(local_output)}")
 
         # Plot atom contributions into total PDOS
-        cprint("Atom's contributions into total PDOS:", colour="yellow")
+        cprint("Atom's contributions into total PDOS:", "green")
         projectors = []
         pdos = []
         for atom in dos.atoms:
             if separate:
                 atom_numbers = dos.atom_numbers(atom)
             else:
                 atom_numbers = [None]
```

### Comparing `rad-tools-0.6.0/rad_tools/score/plot_tb2j.py` & `rad-tools-0.6.1/rad_tools/score/plot_tb2j.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,19 @@
 from argparse import ArgumentParser
 from math import sqrt
 from os import makedirs
 from os.path import abspath, join
 
 import numpy as np
 from matplotlib import pyplot as plt
+from termcolor import cprint
 
 from rad_tools.io.internal import read_template
 from rad_tools.io.tb2j import read_exchange_model
-from rad_tools.routines import OK, RESET, atom_mark_to_latex, rot_angle
+from rad_tools.routines import atom_mark_to_latex, rot_angle
 
 
 def manager(
     input_filename,
     output_path=".",
     output_name="exchange",
     what_to_plot="iso",
@@ -204,15 +205,15 @@
         ax.set_ylim(*ylims)
 
         if title is not None:
             ax.set_title(title, fontsize=1.5 * fontsize)
 
         png_path = join(output_path, f"{output_name}.{wtp}.png")
         plt.savefig(png_path, dpi=400, bbox_inches="tight")
-        print(f"{OK}2D plot with {wtp} is in {abspath(png_path)}{RESET}")
+        cprint(f"2D plot with {wtp} is in {abspath(png_path)}", "green")
 
 
 def create_parser():
     parser = ArgumentParser(description="Script for visualization of TB2J results")
 
     parser.add_argument(
         "-if",
```

### Comparing `rad-tools-0.6.0/rad_tools.egg-info/PKG-INFO` & `rad-tools-0.6.1/rad_tools.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rad-tools
-Version: 0.6.0
+Version: 0.6.1
 Summary: Scripts for condense matter calculations and post-processing.
 Home-page: https://rad-tools.adrybakov.com/en/stable/
 Download-URL: https://github.com/adrybakov/rad-tools.git
 Author: Andrey Rybakov
 Author-email: rybakov.ad@icloud.com
 License: MIT license
 Classifier: Development Status :: 3 - Alpha
@@ -45,16 +45,16 @@
 
 It is expected to be used in two ways:
 
 * As Python library
 
 * Via scripts (i.e. usage from command line)
 
-Documentations is available 
-`here. <https://rad-tools.adrybakov.com>`_
+For the detailed descriprion check
+`documentation. <https://rad-tools.adrybakov.com>`_
 
 Installation
 ============
 
 Requirement for RAD-tools installation are:
 
 * Python itself (>=3.6)
@@ -78,21 +78,21 @@
 
 * Clone the project to your local computer:
 
 .. code-block:: python
 
    git clone git@github.com:adrybakov/rad-tools.git
 
-Change the directory:
+* Change the directory:
 
 .. code-block:: python
 
    cd rad-tools
 
-To install RAD-tools, run (you may need to use ``pip3``):
+* To install RAD-tools, run (you may need to use ``pip3``):
 
 .. code-block:: console
 
    pip install rad-tools
 
 Additionally you may run the unit tests, 
 which requires pytest (requires Python 3.7+) to be installed:
```

### Comparing `rad-tools-0.6.0/rad_tools.egg-info/SOURCES.txt` & `rad-tools-0.6.1/rad_tools.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `rad-tools-0.6.0/scripts/compute-energies.py` & `rad-tools-0.6.1/scripts/compute-energies.py`

 * *Files identical despite different names*

### Comparing `rad-tools-0.6.0/scripts/phonopy-plotter.py` & `rad-tools-0.6.1/scripts/phonopy-plotter.py`

 * *Files identical despite different names*

### Comparing `rad-tools-0.6.0/setup.py` & `rad-tools-0.6.1/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -25,15 +25,15 @@
         "scripts/phonopy-plotter.py",
         "scripts/rad-extract-tb2j.py",
         "scripts/rad-make-template.py",
         "scripts/rad-plot-dos.py",
         "scripts/rad-identify-wannier-centres.py",
         "scripts/compute-energies.py",
     ],
-    install_requires=["numpy", "matplotlib", "tqdm"],
+    install_requires=["numpy", "matplotlib", "tqdm", "termcolor"],
     classifiers=[
         "Development Status :: 3 - Alpha",
         "Programming Language :: Python :: 3",
         "Operating System :: OS Independent",
         "Intended Audience :: Science/Research",
         "Topic :: Scientific/Engineering :: Chemistry",
         "Topic :: Scientific/Engineering :: Physics",
```

