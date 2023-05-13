# Comparing `tmp/jac_misc-1.4.0.8.tar.gz` & `tmp/jac_misc-1.4.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jac_misc-1.4.0.8.tar", last modified: Wed Feb  8 14:13:29 2023, max compression
+gzip compressed data, was "jac_misc-1.4.0.9.tar", last modified: Tue Feb 14 17:26:20 2023, max compression
```

## Comparing `jac_misc-1.4.0.8.tar` & `jac_misc-1.4.0.9.tar`

### file list

```diff
@@ -1,55 +1,55 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.207405 jac_misc-1.4.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)      290 2023-02-08 14:13:29.207405 jac_misc-1.4.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.203405 jac_misc-1.4.0.8/jac_misc/
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/VERSION
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.203405 jac_misc-1.4.0.8/jac_misc/cluster/
--rw-r--r--   0 runner    (1001) docker     (123)       31 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/cluster/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4428 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/cluster/cluster.py
--rw-r--r--   0 runner    (1001) docker     (123)       33 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/cluster/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.203405 jac_misc-1.4.0.8/jac_misc/cluster/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/cluster/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1212 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/cluster/tests/test_cluster.py
--rw-r--r--   0 runner    (1001) docker     (123)      380 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.203405 jac_misc-1.4.0.8/jac_misc/example_module/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/example_module/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      300 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/example_module/example_module.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/example_module/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.203405 jac_misc-1.4.0.8/jac_misc/pdf_ext/
--rw-r--r--   0 runner    (1001) docker     (123)       31 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/pdf_ext/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3152 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/pdf_ext/pdf_ext.py
--rw-r--r--   0 runner    (1001) docker     (123)       21 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/pdf_ext/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.207405 jac_misc-1.4.0.8/jac_misc/pdf_ext/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/pdf_ext/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1018 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/pdf_ext/tests/test_pdf_ext.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.207405 jac_misc-1.4.0.8/jac_misc/ph/
--rw-r--r--   0 runner    (1001) docker     (123)      133 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1273 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     6983 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/inference.py
--rw-r--r--   0 runner    (1001) docker     (123)     4404 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/ph.py
--rw-r--r--   0 runner    (1001) docker     (123)       61 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     3816 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/train.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.207405 jac_misc-1.4.0.8/jac_misc/ph/utils/
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9698 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1559 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/dataloader.py
--rw-r--r--   0 runner    (1001) docker     (123)     4191 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     1384 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/loss.py
--rw-r--r--   0 runner    (1001) docker     (123)      978 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/metric.py
--rw-r--r--   0 runner    (1001) docker     (123)     2950 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/model.py
--rw-r--r--   0 runner    (1001) docker     (123)     1484 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/process.py
--rw-r--r--   0 runner    (1001) docker     (123)     4609 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/trainer.py
--rw-r--r--   0 runner    (1001) docker     (123)     2783 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/ph/utils/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.207405 jac_misc-1.4.0.8/jac_misc/translator/
--rw-r--r--   0 runner    (1001) docker     (123)       34 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/translator/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       79 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/translator/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     2061 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/jac_misc/translator/translator.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:29.203405 jac_misc-1.4.0.8/jac_misc.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      290 2023-02-08 14:13:29.000000 jac_misc-1.4.0.8/jac_misc.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1208 2023-02-08 14:13:29.000000 jac_misc-1.4.0.8/jac_misc.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-08 14:13:29.000000 jac_misc-1.4.0.8/jac_misc.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      467 2023-02-08 14:13:29.000000 jac_misc-1.4.0.8/jac_misc.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-02-08 14:13:29.000000 jac_misc-1.4.0.8/jac_misc.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-08 14:13:29.207405 jac_misc-1.4.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-02-08 14:13:11.000000 jac_misc-1.4.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.977539 jac_misc-1.4.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)      290 2023-02-14 17:26:20.977539 jac_misc-1.4.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.969539 jac_misc-1.4.0.9/jac_misc/
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/VERSION
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.973539 jac_misc-1.4.0.9/jac_misc/cluster/
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/cluster/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4428 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/cluster/cluster.py
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/cluster/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.973539 jac_misc-1.4.0.9/jac_misc/cluster/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/cluster/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1212 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/cluster/tests/test_cluster.py
+-rw-r--r--   0 runner    (1001) docker     (123)      380 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.973539 jac_misc-1.4.0.9/jac_misc/example_module/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/example_module/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      300 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/example_module/example_module.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/example_module/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.973539 jac_misc-1.4.0.9/jac_misc/pdf_ext/
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/pdf_ext/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3152 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/pdf_ext/pdf_ext.py
+-rw-r--r--   0 runner    (1001) docker     (123)       21 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/pdf_ext/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.973539 jac_misc-1.4.0.9/jac_misc/pdf_ext/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/pdf_ext/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1018 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/pdf_ext/tests/test_pdf_ext.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.977539 jac_misc-1.4.0.9/jac_misc/ph/
+-rw-r--r--   0 runner    (1001) docker     (123)      133 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1273 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     7026 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/inference.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4749 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/ph.py
+-rw-r--r--   0 runner    (1001) docker     (123)       61 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     3816 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/train.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.977539 jac_misc-1.4.0.9/jac_misc/ph/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12555 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1559 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/dataloader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4191 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1384 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)      978 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/metric.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2950 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1484 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/process.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4609 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/trainer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2783 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/ph/utils/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.977539 jac_misc-1.4.0.9/jac_misc/translator/
+-rw-r--r--   0 runner    (1001) docker     (123)       34 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/translator/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       79 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/translator/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2061 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/jac_misc/translator/translator.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:20.973539 jac_misc-1.4.0.9/jac_misc.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      290 2023-02-14 17:26:20.000000 jac_misc-1.4.0.9/jac_misc.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1208 2023-02-14 17:26:20.000000 jac_misc-1.4.0.9/jac_misc.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-14 17:26:20.000000 jac_misc-1.4.0.9/jac_misc.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      467 2023-02-14 17:26:20.000000 jac_misc-1.4.0.9/jac_misc.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-02-14 17:26:20.000000 jac_misc-1.4.0.9/jac_misc.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-14 17:26:20.977539 jac_misc-1.4.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-02-14 17:25:58.000000 jac_misc-1.4.0.9/setup.py
```

### Comparing `jac_misc-1.4.0.8/README.md` & `jac_misc-1.4.0.9/README.md`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/cluster/cluster.py` & `jac_misc-1.4.0.9/jac_misc/cluster/cluster.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/cluster/tests/test_cluster.py` & `jac_misc-1.4.0.9/jac_misc/cluster/tests/test_cluster.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/pdf_ext/pdf_ext.py` & `jac_misc-1.4.0.9/jac_misc/pdf_ext/pdf_ext.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/pdf_ext/tests/test_pdf_ext.py` & `jac_misc-1.4.0.9/jac_misc/pdf_ext/tests/test_pdf_ext.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/config.yaml` & `jac_misc-1.4.0.9/jac_misc/ph/config.yaml`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/ph.py` & `jac_misc-1.4.0.9/jac_misc/ph/ph.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from http.client import ImproperConnectionState
 from typing import Any, Dict
 import warnings
 import os
 import traceback
 from fastapi import HTTPException
+import logging
 
 from jaseci.actions.live_actions import jaseci_action
 
 from .utils.util import read_yaml, deep_update, save_custom_python
 from .inference import InferenceList
 
 warnings.filterwarnings("ignore")
@@ -17,15 +18,20 @@
 HEAD_LIST_NOT_FOUND = "No Active head list found. Use create_head_list first."
 
 
 def setup():
     global il, list_config
     dirname = os.path.dirname(__file__)
     list_config = read_yaml(os.path.join(dirname, "config.yaml"))
-    il = None
+    if os.path.exists("heads/config.yaml") and os.path.exists("heads/custom.py"):
+        logging.warning("Found a heads list in the current directory. Loading it ...")
+        il = InferenceList(config=read_yaml("heads/config.yaml"))
+    else:
+        logging.info("No heads list found. Run create_head_list to create one.")
+        il = None
 
 
 setup()
 
 ### Start of PersonalizedHead Actions ###
```

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/train.py` & `jac_misc-1.4.0.9/jac_misc/ph/train.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/base.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/base.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,20 +1,24 @@
+from typing import Any, Dict
 import torch.nn as nn
 import numpy as np
 from abc import abstractmethod
 from numpy import inf
 import torch
 from pathlib import Path
 from datetime import datetime
 from torch.utils.data import DataLoader
 from torch.utils.data.dataloader import default_collate
 from torch.utils.data.sampler import SubsetRandomSampler
 from collections import OrderedDict
+import os
+import shutil
 
 from .logger import TensorboardWriter, get_logger
+from . import model as model_module
 
 
 class BaseModel(nn.Module):
     """
     Base class for all models
     """
 
@@ -284,7 +288,82 @@
         return train_sampler, valid_sampler
 
     def split_validation(self):
         if self.valid_sampler is None:
             return None
         else:
             return DataLoader(sampler=self.valid_sampler, **self.init_kwargs)
+
+
+class BaseInference:
+    def __init__(self, config: Dict, logger, uuid: str = None) -> None:
+        self.config = config
+        model_config = self.config["Model"]
+        self.infer_config = self.config["Inference"]
+
+        self.model = getattr(model_module, model_config["type"])(
+            **model_config.get("args", {})
+        )
+
+        # loading pretrained weights
+        if self.infer_config["weights"]:
+            if not os.path.exists(f"heads/{uuid}/current.pth"):
+                shutil.copyfile(
+                    self.infer_config["weights"], f"heads/{self.id}/current.pth"
+                )
+                self.logger.info(
+                    "Loading default checkpoint: {} ...".format(
+                        self.infer_config["weights"]
+                    )
+                )
+
+            checkpoint = torch.load(f"heads/{self.id}/current.pth")
+            state_dict = checkpoint.get("state_dict", checkpoint)
+            model_keys = list(self.model.state_dict().keys())
+            if model_keys[0].startswith("model."):
+                new_state_dict = OrderedDict()
+                for k, v in state_dict.items():
+                    name = "model." + k
+                    new_state_dict[name] = v
+                state_dict = new_state_dict
+            self.model.load_state_dict(state_dict)
+            logger.info("Checkpoint loaded.")
+
+        # Setting the device
+        self.device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
+        self.model = self.model.to(self.device)
+        self.model.eval()
+
+        # Get Intermediate Activations
+        self.out_activation_layer = self.infer_config.get("out_activation_layer", None)
+        if self.out_activation_layer:
+            self.activation = {}
+            getattr(self.model, self.out_activation_layer).register_forward_hook(
+                self.get_activation(self.out_activation_layer)
+            )
+
+    @torch.no_grad()
+    def predict(self, data: Any) -> Any:
+        data = self.preprocess(data)
+        data = data.to(self.device)
+        output = self.model(data)
+        if self.out_activation_layer:
+            output = self.activation[self.out_activation_layer]
+        output = self.postprocess(output)
+        return output
+
+    def preprocess(self, data: Any) -> Any:
+        raise NotImplementedError
+
+    def postprocess(self, data: Any) -> Any:
+        raise NotImplementedError
+
+    def load_weights(self, weights: str) -> None:
+        checkpoint = torch.load(weights)
+        state_dict = checkpoint.get("state_dict", checkpoint)
+        self.model.load_state_dict(state_dict)
+
+    def get_activation(self, name):
+        def hook(model, input, output):
+            self.activation[name] = output.detach()
+
+        return hook
```

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/dataloader.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/dataloader.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/logger.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/logger.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/loss.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/loss.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/metric.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/metric.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/model.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/model.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/process.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/process.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/trainer.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/trainer.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/ph/utils/util.py` & `jac_misc-1.4.0.9/jac_misc/ph/utils/util.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc/translator/translator.py` & `jac_misc-1.4.0.9/jac_misc/translator/translator.py`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/jac_misc.egg-info/SOURCES.txt` & `jac_misc-1.4.0.9/jac_misc.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `jac_misc-1.4.0.8/setup.py` & `jac_misc-1.4.0.9/setup.py`

 * *Files identical despite different names*

