# Comparing `tmp/revpimodio2-2.6.0rc4.tar.gz` & `tmp/revpimodio2-2.6.0rc5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "revpimodio2-2.6.0rc4.tar", last modified: Tue Feb  7 09:07:48 2023, max compression
+gzip compressed data, was "revpimodio2-2.6.0rc5.tar", last modified: Sat May 13 09:58:53 2023, max compression
```

## Comparing `revpimodio2-2.6.0rc4.tar` & `revpimodio2-2.6.0rc5.tar`

### file list

```diff
@@ -1,33 +1,34 @@
-drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-02-07 09:07:48.021524 revpimodio2-2.6.0rc4/
--rw-r--r--   0 svensager   (501) staff       (20)    18092 2023-02-03 11:02:00.000000 revpimodio2-2.6.0rc4/LICENSE.txt
--rw-r--r--   0 svensager   (501) staff       (20)      174 2023-01-22 17:26:50.000000 revpimodio2-2.6.0rc4/MANIFEST.in
--rw-r--r--   0 svensager   (501) staff       (20)      813 2023-02-03 11:06:16.000000 revpimodio2-2.6.0rc4/Makefile
--rw-r--r--   0 svensager   (501) staff       (20)     4569 2023-02-07 09:07:48.021396 revpimodio2-2.6.0rc4/PKG-INFO
--rw-r--r--   0 svensager   (501) staff       (20)     3646 2023-02-03 11:02:00.000000 revpimodio2-2.6.0rc4/README.md
-drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-02-07 09:07:48.017339 revpimodio2-2.6.0rc4/docs/
--rw-r--r--   0 svensager   (501) staff       (20)      667 2023-01-22 17:08:01.000000 revpimodio2-2.6.0rc4/docs/Makefile
--rw-r--r--   0 svensager   (501) staff       (20)      837 2023-02-07 08:37:44.000000 revpimodio2-2.6.0rc4/docs/conf.py
--rw-r--r--   0 svensager   (501) staff       (20)      447 2023-02-07 08:37:44.000000 revpimodio2-2.6.0rc4/docs/index.rst
--rw-r--r--   0 svensager   (501) staff       (20)       54 2023-01-22 16:50:05.000000 revpimodio2-2.6.0rc4/docs/modules.rst
--rw-r--r--   0 svensager   (501) staff       (20)     1445 2023-01-22 16:50:05.000000 revpimodio2-2.6.0rc4/docs/revpimodio2.rst
--rw-r--r--   0 svensager   (501) staff       (20)       25 2023-01-20 16:11:10.000000 revpimodio2-2.6.0rc4/requirements.txt
--rw-r--r--   0 svensager   (501) staff       (20)       38 2023-02-07 09:07:48.021576 revpimodio2-2.6.0rc4/setup.cfg
--rw-r--r--   0 svensager   (501) staff       (20)     1545 2023-02-03 11:02:00.000000 revpimodio2-2.6.0rc4/setup.py
-drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-02-07 09:07:48.015157 revpimodio2-2.6.0rc4/src/
-drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-02-07 09:07:48.020344 revpimodio2-2.6.0rc4/src/revpimodio2/
--rw-r--r--   0 svensager   (501) staff       (20)     1390 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/__init__.py
--rw-r--r--   0 svensager   (501) staff       (20)     1660 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/_internal.py
--rw-r--r--   0 svensager   (501) staff       (20)     1104 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/app.py
--rw-r--r--   0 svensager   (501) staff       (20)    50983 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/device.py
--rw-r--r--   0 svensager   (501) staff       (20)      256 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/errors.py
--rw-r--r--   0 svensager   (501) staff       (20)    23236 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/helper.py
--rw-r--r--   0 svensager   (501) staff       (20)    53076 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/io.py
--rw-r--r--   0 svensager   (501) staff       (20)    53697 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/modio.py
--rw-r--r--   0 svensager   (501) staff       (20)    36670 2023-02-06 16:43:23.000000 revpimodio2-2.6.0rc4/src/revpimodio2/netio.py
--rw-r--r--   0 svensager   (501) staff       (20)     5307 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/pictory.py
--rw-r--r--   0 svensager   (501) staff       (20)      551 2023-02-03 11:04:53.000000 revpimodio2-2.6.0rc4/src/revpimodio2/summary.py
-drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-02-07 09:07:48.021163 revpimodio2-2.6.0rc4/src/revpimodio2.egg-info/
--rw-r--r--   0 svensager   (501) staff       (20)     4569 2023-02-07 09:07:48.000000 revpimodio2-2.6.0rc4/src/revpimodio2.egg-info/PKG-INFO
--rw-r--r--   0 svensager   (501) staff       (20)      588 2023-02-07 09:07:48.000000 revpimodio2-2.6.0rc4/src/revpimodio2.egg-info/SOURCES.txt
--rw-r--r--   0 svensager   (501) staff       (20)        1 2023-02-07 09:07:48.000000 revpimodio2-2.6.0rc4/src/revpimodio2.egg-info/dependency_links.txt
--rw-r--r--   0 svensager   (501) staff       (20)       12 2023-02-07 09:07:48.000000 revpimodio2-2.6.0rc4/src/revpimodio2.egg-info/top_level.txt
+drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-05-13 09:58:53.303374 revpimodio2-2.6.0rc5/
+-rw-r--r--   0 svensager   (501) staff       (20)    18092 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/LICENSE.txt
+-rw-r--r--   0 svensager   (501) staff       (20)      174 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/MANIFEST.in
+-rw-r--r--   0 svensager   (501) staff       (20)      813 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/Makefile
+-rw-r--r--   0 svensager   (501) staff       (20)     4568 2023-05-13 09:58:53.303239 revpimodio2-2.6.0rc5/PKG-INFO
+-rw-r--r--   0 svensager   (501) staff       (20)     3646 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/README.md
+drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-05-13 09:58:53.299818 revpimodio2-2.6.0rc5/docs/
+-rw-r--r--   0 svensager   (501) staff       (20)      667 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/docs/Makefile
+-rw-r--r--   0 svensager   (501) staff       (20)      837 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/docs/conf.py
+-rw-r--r--   0 svensager   (501) staff       (20)      447 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/docs/index.rst
+-rw-r--r--   0 svensager   (501) staff       (20)       54 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/docs/modules.rst
+-rw-r--r--   0 svensager   (501) staff       (20)     1445 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/docs/revpimodio2.rst
+-rw-r--r--   0 svensager   (501) staff       (20)       25 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/requirements.txt
+-rw-r--r--   0 svensager   (501) staff       (20)       38 2023-05-13 09:58:53.303417 revpimodio2-2.6.0rc5/setup.cfg
+-rw-r--r--   0 svensager   (501) staff       (20)     1598 2023-05-13 09:48:25.000000 revpimodio2-2.6.0rc5/setup.py
+drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-05-13 09:58:53.297109 revpimodio2-2.6.0rc5/src/
+drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-05-13 09:58:53.302479 revpimodio2-2.6.0rc5/src/revpimodio2/
+-rw-r--r--   0 svensager   (501) staff       (20)      196 2023-05-13 08:22:50.000000 revpimodio2-2.6.0rc5/src/revpimodio2/__about__.py
+-rw-r--r--   0 svensager   (501) staff       (20)     1372 2023-05-13 09:56:10.000000 revpimodio2-2.6.0rc5/src/revpimodio2/__init__.py
+-rw-r--r--   0 svensager   (501) staff       (20)     1660 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/_internal.py
+-rw-r--r--   0 svensager   (501) staff       (20)     1104 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/app.py
+-rw-r--r--   0 svensager   (501) staff       (20)    50983 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/device.py
+-rw-r--r--   0 svensager   (501) staff       (20)      256 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/errors.py
+-rw-r--r--   0 svensager   (501) staff       (20)    23236 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/helper.py
+-rw-r--r--   0 svensager   (501) staff       (20)    53076 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/io.py
+-rw-r--r--   0 svensager   (501) staff       (20)    53697 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/modio.py
+-rw-r--r--   0 svensager   (501) staff       (20)    36670 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/netio.py
+-rw-r--r--   0 svensager   (501) staff       (20)     5307 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/pictory.py
+-rw-r--r--   0 svensager   (501) staff       (20)      551 2023-02-07 09:16:12.000000 revpimodio2-2.6.0rc5/src/revpimodio2/summary.py
+drwxr-xr-x   0 svensager   (501) staff       (20)        0 2023-05-13 09:58:53.303034 revpimodio2-2.6.0rc5/src/revpimodio2.egg-info/
+-rw-r--r--   0 svensager   (501) staff       (20)     4568 2023-05-13 09:58:53.000000 revpimodio2-2.6.0rc5/src/revpimodio2.egg-info/PKG-INFO
+-rw-r--r--   0 svensager   (501) staff       (20)      617 2023-05-13 09:58:53.000000 revpimodio2-2.6.0rc5/src/revpimodio2.egg-info/SOURCES.txt
+-rw-r--r--   0 svensager   (501) staff       (20)        1 2023-05-13 09:58:53.000000 revpimodio2-2.6.0rc5/src/revpimodio2.egg-info/dependency_links.txt
+-rw-r--r--   0 svensager   (501) staff       (20)       12 2023-05-13 09:58:53.000000 revpimodio2-2.6.0rc5/src/revpimodio2.egg-info/top_level.txt
```

### Comparing `revpimodio2-2.6.0rc4/LICENSE.txt` & `revpimodio2-2.6.0rc5/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/Makefile` & `revpimodio2-2.6.0rc5/Makefile`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/PKG-INFO` & `revpimodio2-2.6.0rc5/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: revpimodio2
-Version: 2.6.0rc4
+Version: 2.6.0rc5
 Summary: Python3 programming for RevolutionPi of KUNBUS GmbH
 Home-page: https://revpimodio.org/
 Author: Sven Sager
 Author-email: akira@narux.de
 Maintainer: Sven Sager
 Maintainer-email: akira@revpimodio.org
 License: LGPLv2
@@ -15,15 +15,15 @@
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: GNU Lesser General Public License v2 (LGPLv2)
 Classifier: Operating System :: MacOS :: MacOS X
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Requires-Python: ~=3.2
+Requires-Python: >= 3.2
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
 # RevPiModIO
 
 ### Python3 programming for RevolutionPi of KUNBUS GmbH.
 
@@ -114,9 +114,7 @@
 communication with the process image is optimally performed inside the module.
 Changes to the inputs and outputs are also evaluated along with the additional
 functions of the module give the developer many tools along the way.
 
 More examples: (https://revpimodio.org/en/blogs/examples/)
 
 Provided under the [LGPLv2](LICENSE.txt) license
-
-
```

### Comparing `revpimodio2-2.6.0rc4/README.md` & `revpimodio2-2.6.0rc5/README.md`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/docs/Makefile` & `revpimodio2-2.6.0rc5/docs/Makefile`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/docs/conf.py` & `revpimodio2-2.6.0rc5/docs/conf.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/docs/revpimodio2.rst` & `revpimodio2-2.6.0rc5/docs/revpimodio2.rst`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/setup.py` & `revpimodio2-2.6.0rc5/setup.py`

 * *Files 13% similar despite different names*

```diff
@@ -3,27 +3,29 @@
 """Setup-script for revpimodio2."""
 __author__ = "Sven Sager"
 __copyright__ = "Copyright (C) 2023 Sven Sager"
 __license__ = "LGPLv2"
 
 from setuptools import setup, find_namespace_packages
 
+from src.revpimodio2.__about__ import __version__
+
 with open("README.md") as fh:
     # Load long description from readme file
     long_description = fh.read()
 
 setup(
     name="revpimodio2",
-    version="2.6.0rc4",
+    version=__version__,
 
     packages=find_namespace_packages("src"),
     package_dir={'': 'src'},
     include_package_data=True,
 
-    python_requires="~=3.2",
+    python_requires=">= 3.2",
     install_requires=[],
     entry_points={},
 
     platforms=["all"],
 
     url="https://revpimodio.org/",
     license="LGPLv2",
```

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/__init__.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -18,16 +18,15 @@
     "RevPiNetIO", "RevPiNetIODriver", "RevPiNetIOSelected", "run_net_plc",
     "Cycletools", "EventCallback",
     "ProductType", "AIO", "COMPACT", "DI", "DO", "DIO", "FLAT", "MIO",
 ]
 __author__ = "Sven Sager <akira@revpimodio.org>"
 __copyright__ = "Copyright (C) 2023 Sven Sager"
 __license__ = "LGPLv2"
-__package__ = "revpimodio2"
-__version__ = "2.6.0rc4"
 
+from .__about__ import __version__
 from ._internal import *
 from .helper import Cycletools, EventCallback
 from .io import IOEvent
 from .modio import RevPiModIO, RevPiModIODriver, RevPiModIOSelected, run_plc
 from .netio import RevPiNetIO, RevPiNetIODriver, RevPiNetIOSelected, run_net_plc
 from .pictory import ProductType, AIO, COMPACT, DI, DO, DIO, FLAT, MIO
```

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/_internal.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/_internal.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/app.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/app.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/device.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/device.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/helper.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/helper.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/io.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/io.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/modio.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/modio.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/netio.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/netio.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/pictory.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/pictory.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2/summary.py` & `revpimodio2-2.6.0rc5/src/revpimodio2/summary.py`

 * *Files identical despite different names*

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2.egg-info/PKG-INFO` & `revpimodio2-2.6.0rc5/src/revpimodio2.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: revpimodio2
-Version: 2.6.0rc4
+Version: 2.6.0rc5
 Summary: Python3 programming for RevolutionPi of KUNBUS GmbH
 Home-page: https://revpimodio.org/
 Author: Sven Sager
 Author-email: akira@narux.de
 Maintainer: Sven Sager
 Maintainer-email: akira@revpimodio.org
 License: LGPLv2
@@ -15,15 +15,15 @@
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: GNU Lesser General Public License v2 (LGPLv2)
 Classifier: Operating System :: MacOS :: MacOS X
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Requires-Python: ~=3.2
+Requires-Python: >= 3.2
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
 # RevPiModIO
 
 ### Python3 programming for RevolutionPi of KUNBUS GmbH.
 
@@ -114,9 +114,7 @@
 communication with the process image is optimally performed inside the module.
 Changes to the inputs and outputs are also evaluated along with the additional
 functions of the module give the developer many tools along the way.
 
 More examples: (https://revpimodio.org/en/blogs/examples/)
 
 Provided under the [LGPLv2](LICENSE.txt) license
-
-
```

### Comparing `revpimodio2-2.6.0rc4/src/revpimodio2.egg-info/SOURCES.txt` & `revpimodio2-2.6.0rc5/src/revpimodio2.egg-info/SOURCES.txt`

 * *Files 16% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 requirements.txt
 setup.py
 docs/Makefile
 docs/conf.py
 docs/index.rst
 docs/modules.rst
 docs/revpimodio2.rst
+src/revpimodio2/__about__.py
 src/revpimodio2/__init__.py
 src/revpimodio2/_internal.py
 src/revpimodio2/app.py
 src/revpimodio2/device.py
 src/revpimodio2/errors.py
 src/revpimodio2/helper.py
 src/revpimodio2/io.py
```

