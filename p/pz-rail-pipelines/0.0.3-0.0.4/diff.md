# Comparing `tmp/pz-rail-pipelines-0.0.3.tar.gz` & `tmp/pz-rail-pipelines-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pz-rail-pipelines-0.0.3.tar", last modified: Thu May  4 06:17:22 2023, max compression
+gzip compressed data, was "pz-rail-pipelines-0.0.4.tar", last modified: Fri May 12 22:15:04 2023, max compression
```

## Comparing `pz-rail-pipelines-0.0.3.tar` & `pz-rail-pipelines-0.0.4.tar`

### file list

```diff
@@ -1,36 +1,40 @@
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.959374 pz-rail-pipelines-0.0.3/
--rw-r--r--   0 runner    (1001) docker     (122)      123 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/.github/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (122)     2052 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/.github/workflows/main.yml
--rw-r--r--   0 runner    (1001) docker     (122)      548 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/.github/workflows/pypi.yaml
--rw-r--r--   0 runner    (1001) docker     (122)     1823 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/.gitignore
--rw-r--r--   0 runner    (1001) docker     (122)     1102 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (122)     1938 2023-05-04 06:17:22.959374 pz-rail-pipelines-0.0.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (122)       66 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/README.md
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/nb/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/nb/examples/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/nb/examples/goldenspike/
--rw-r--r--   0 runner    (1001) docker     (122)     2700 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/nb/examples/goldenspike/goldenspike.ipynb
--rw-r--r--   0 runner    (1001) docker     (122)     2932 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (122)       60 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (122)       38 2023-05-04 06:17:22.959374 pz-rail-pipelines-0.0.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (122)       71 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/src/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/src/pz_rail_pipelines.egg-info/
--rw-r--r--   0 runner    (1001) docker     (122)     1938 2023-05-04 06:17:22.000000 pz-rail-pipelines-0.0.3/src/pz_rail_pipelines.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (122)      580 2023-05-04 06:17:22.000000 pz-rail-pipelines-0.0.3/src/pz_rail_pipelines.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (122)        1 2023-05-04 06:17:22.000000 pz-rail-pipelines-0.0.3/src/pz_rail_pipelines.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (122)       69 2023-05-04 06:17:22.000000 pz-rail-pipelines-0.0.3/src/pz_rail_pipelines.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (122)        5 2023-05-04 06:17:22.000000 pz-rail-pipelines-0.0.3/src/pz_rail_pipelines.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/src/rail/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/src/rail/pipelines/
--rw-r--r--   0 runner    (1001) docker     (122)       35 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/src/rail/pipelines/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      160 2023-05-04 06:17:21.000000 pz-rail-pipelines-0.0.3/src/rail/pipelines/_version.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.955373 pz-rail-pipelines-0.0.3/src/rail/pipelines/examples/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.959374 pz-rail-pipelines-0.0.3/src/rail/pipelines/examples/goldenspike/
--rw-r--r--   0 runner    (1001) docker     (122)     7533 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/src/rail/pipelines/examples/goldenspike/goldenspike.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.959374 pz-rail-pipelines-0.0.3/src/rail/pipelines/utils/
--rw-r--r--   0 runner    (1001) docker     (122)     1136 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/src/rail/pipelines/utils/name_factory.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-04 06:17:22.959374 pz-rail-pipelines-0.0.3/tests/
--rw-r--r--   0 runner    (1001) docker     (122)      816 2023-05-04 06:17:03.000000 pz-rail-pipelines-0.0.3/tests/test_pipelines.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.867574 pz-rail-pipelines-0.0.4/
+-rw-r--r--   0 runner    (1001) docker     (122)      123 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.855574 pz-rail-pipelines-0.0.4/.github/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.859574 pz-rail-pipelines-0.0.4/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (122)     2057 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/.github/workflows/main.yml
+-rw-r--r--   0 runner    (1001) docker     (122)      548 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/.github/workflows/pypi.yaml
+-rw-r--r--   0 runner    (1001) docker     (122)     1823 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (122)     1102 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (122)     1959 2023-05-12 22:15:04.867574 pz-rail-pipelines-0.0.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (122)       66 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/README.md
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.855574 pz-rail-pipelines-0.0.4/nb/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.863574 pz-rail-pipelines-0.0.4/nb/estimation/
+-rw-r--r--   0 runner    (1001) docker     (122)     3654 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/nb/estimation/inform_all_hsc.ipynb
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.855574 pz-rail-pipelines-0.0.4/nb/examples/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.863574 pz-rail-pipelines-0.0.4/nb/examples/goldenspike/
+-rw-r--r--   0 runner    (1001) docker     (122)     2700 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/nb/examples/goldenspike/goldenspike.ipynb
+-rw-r--r--   0 runner    (1001) docker     (122)     3117 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (122)       60 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (122)       38 2023-05-12 22:15:04.867574 pz-rail-pipelines-0.0.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (122)       71 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.855574 pz-rail-pipelines-0.0.4/src/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.863574 pz-rail-pipelines-0.0.4/src/pz_rail_pipelines.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (122)     1959 2023-05-12 22:15:04.000000 pz-rail-pipelines-0.0.4/src/pz_rail_pipelines.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (122)      659 2023-05-12 22:15:04.000000 pz-rail-pipelines-0.0.4/src/pz_rail_pipelines.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        1 2023-05-12 22:15:04.000000 pz-rail-pipelines-0.0.4/src/pz_rail_pipelines.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (122)      208 2023-05-12 22:15:04.000000 pz-rail-pipelines-0.0.4/src/pz_rail_pipelines.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        5 2023-05-12 22:15:04.000000 pz-rail-pipelines-0.0.4/src/pz_rail_pipelines.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.855574 pz-rail-pipelines-0.0.4/src/rail/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.863574 pz-rail-pipelines-0.0.4/src/rail/pipelines/
+-rw-r--r--   0 runner    (1001) docker     (122)       35 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/src/rail/pipelines/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      160 2023-05-12 22:15:03.000000 pz-rail-pipelines-0.0.4/src/rail/pipelines/_version.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.863574 pz-rail-pipelines-0.0.4/src/rail/pipelines/estimation/
+-rw-r--r--   0 runner    (1001) docker     (122)     2972 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/src/rail/pipelines/estimation/inform_all.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.859574 pz-rail-pipelines-0.0.4/src/rail/pipelines/examples/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.863574 pz-rail-pipelines-0.0.4/src/rail/pipelines/examples/goldenspike/
+-rw-r--r--   0 runner    (1001) docker     (122)     7588 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/src/rail/pipelines/examples/goldenspike/goldenspike.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.863574 pz-rail-pipelines-0.0.4/src/rail/pipelines/utils/
+-rw-r--r--   0 runner    (1001) docker     (122)     1136 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/src/rail/pipelines/utils/name_factory.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-12 22:15:04.867574 pz-rail-pipelines-0.0.4/tests/
+-rw-r--r--   0 runner    (1001) docker     (122)      816 2023-05-12 22:14:54.000000 pz-rail-pipelines-0.0.4/tests/test_pipelines.py
```

### Comparing `pz-rail-pipelines-0.0.3/.github/workflows/main.yml` & `pz-rail-pipelines-0.0.4/.github/workflows/main.yml`

 * *Files 5% similar despite different names*

```diff
@@ -28,15 +28,15 @@
       uses: actions/setup-python@v2
       with:
         python-version: ${{ matrix.python-version }}
     - name: Install dependencies
       run: |
         python -m pip install --upgrade pip
         pip install wheel numpy
-        pip install .
+        pip install .[dev]
         pip install flake8 pytest pytest-cov mockmpi pytest-timeout
         if [ -f requirements.txt ]; then pip install -r requirements.txt; fi			
     - name: Test with pytest
       run: |
         python -m pytest --cov=rail.pipelines --cov-report=xml
     - name: Upload coverage to Codecov
       uses: codecov/codecov-action@v1
```

### Comparing `pz-rail-pipelines-0.0.3/.github/workflows/pypi.yaml` & `pz-rail-pipelines-0.0.4/.github/workflows/pypi.yaml`

 * *Files identical despite different names*

### Comparing `pz-rail-pipelines-0.0.3/.gitignore` & `pz-rail-pipelines-0.0.4/.gitignore`

 * *Files identical despite different names*

### Comparing `pz-rail-pipelines-0.0.3/LICENSE` & `pz-rail-pipelines-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `pz-rail-pipelines-0.0.3/PKG-INFO` & `pz-rail-pipelines-0.0.4/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pz-rail-pipelines
-Version: 0.0.3
+Version: 0.0.4
 Summary: RAIL pipelines
 Author-email: The LSST DESC PZ WG <echarles@slac.stanford.edu>
 License: MIT License
         
         Copyright (c) 2022 LSST Dark Energy Science Collaboration (DESC)
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -32,9 +32,10 @@
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Natural Language :: English
 Classifier: Operating System :: POSIX
 Requires-Python: >=3.8
 Description-Content-Type: text/x-rst
+Provides-Extra: full
 Provides-Extra: dev
 License-File: LICENSE
```

### Comparing `pz-rail-pipelines-0.0.3/nb/examples/goldenspike/goldenspike.ipynb` & `pz-rail-pipelines-0.0.4/nb/examples/goldenspike/goldenspike.ipynb`

 * *Files identical despite different names*

### Comparing `pz-rail-pipelines-0.0.3/pyproject.toml` & `pz-rail-pipelines-0.0.4/pyproject.toml`

 * *Files 13% similar despite different names*

```diff
@@ -16,19 +16,28 @@
     "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3.10",
     "Natural Language :: English",
     "Operating System :: POSIX"
 ]
 dynamic = ["version"]
 dependencies = [
-    "pz-rail-hub>=0.0.4",
+    "pz-rail>=0.98.5",
 ]
 
 [project.optional-dependencies]
+full = [
+    "pz-rail-bpz>=0.0.9",
+    "pz-rail-flexzboost>=0.0.9",
+    "pz-rail-gpz-v1>=0.1.1",
+]
+
 dev = [
+    "pz-rail-bpz>=0.0.9",
+    "pz-rail-flexzboost>=0.0.9",
+    "pz-rail-gpz-v1>=0.1.1",
     "coverage",
     "pylint",
     "pytest",
     "pytest-cov",
     "yamllint",
 ]
```

### Comparing `pz-rail-pipelines-0.0.3/src/pz_rail_pipelines.egg-info/PKG-INFO` & `pz-rail-pipelines-0.0.4/src/pz_rail_pipelines.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pz-rail-pipelines
-Version: 0.0.3
+Version: 0.0.4
 Summary: RAIL pipelines
 Author-email: The LSST DESC PZ WG <echarles@slac.stanford.edu>
 License: MIT License
         
         Copyright (c) 2022 LSST Dark Energy Science Collaboration (DESC)
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -32,9 +32,10 @@
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Natural Language :: English
 Classifier: Operating System :: POSIX
 Requires-Python: >=3.8
 Description-Content-Type: text/x-rst
+Provides-Extra: full
 Provides-Extra: dev
 License-File: LICENSE
```

### Comparing `pz-rail-pipelines-0.0.3/src/pz_rail_pipelines.egg-info/SOURCES.txt` & `pz-rail-pipelines-0.0.4/src/pz_rail_pipelines.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -3,18 +3,20 @@
 LICENSE
 README.md
 pyproject.toml
 requirements.txt
 setup.py
 .github/workflows/main.yml
 .github/workflows/pypi.yaml
+nb/estimation/inform_all_hsc.ipynb
 nb/examples/goldenspike/goldenspike.ipynb
 src/pz_rail_pipelines.egg-info/PKG-INFO
 src/pz_rail_pipelines.egg-info/SOURCES.txt
 src/pz_rail_pipelines.egg-info/dependency_links.txt
 src/pz_rail_pipelines.egg-info/requires.txt
 src/pz_rail_pipelines.egg-info/top_level.txt
 src/rail/pipelines/__init__.py
 src/rail/pipelines/_version.py
+src/rail/pipelines/estimation/inform_all.py
 src/rail/pipelines/examples/goldenspike/goldenspike.py
 src/rail/pipelines/utils/name_factory.py
 tests/test_pipelines.py
```

### Comparing `pz-rail-pipelines-0.0.3/src/rail/pipelines/examples/goldenspike/goldenspike.py` & `pz-rail-pipelines-0.0.4/src/rail/pipelines/examples/goldenspike/goldenspike.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,14 +2,16 @@
 # coding: utf-8
 
 # Prerquisites, os, and numpy
 import os
 import numpy as np
 
 # Various rail modules
+import rail.stages
+rail.stages.import_and_attach_all()
 from rail.stages import *
 
 from rail.pipelines.utils.name_factory import NameFactory, DataType, CatalogType, ModelType, PdfType
 from rail.core.stage import RailStage, RailPipeline
 
 import ceci
```

### Comparing `pz-rail-pipelines-0.0.3/src/rail/pipelines/utils/name_factory.py` & `pz-rail-pipelines-0.0.4/src/rail/pipelines/utils/name_factory.py`

 * *Files identical despite different names*

### Comparing `pz-rail-pipelines-0.0.3/tests/test_pipelines.py` & `pz-rail-pipelines-0.0.4/tests/test_pipelines.py`

 * *Files identical despite different names*

