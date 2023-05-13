# Comparing `tmp/rebasin-0.0.8.tar.gz` & `tmp/rebasin-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rebasin-0.0.8.tar", last modified: Mon Apr  3 14:00:17 2023, max compression
+gzip compressed data, was "rebasin-0.0.9.tar", last modified: Mon Apr  3 14:14:02 2023, max compression
```

## Comparing `rebasin-0.0.8.tar` & `rebasin-0.0.9.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 sebastianmuller   (501) staff       (20)        0 2023-04-03 14:00:17.400639 rebasin-0.0.8/
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     1074 2023-02-23 11:53:52.000000 rebasin-0.0.8/LICENSE
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     1750 2023-04-03 14:00:17.400831 rebasin-0.0.8/PKG-INFO
--rw-r--r--   0 sebastianmuller   (501) staff       (20)      897 2023-04-01 08:57:23.000000 rebasin-0.0.8/README.md
-drwxr-xr-x   0 sebastianmuller   (501) staff       (20)        0 2023-04-03 14:00:17.392018 rebasin-0.0.8/rebasin/
--rw-r--r--   0 sebastianmuller   (501) staff       (20)      101 2023-04-03 13:59:02.000000 rebasin-0.0.8/rebasin/__init__.py
--rw-r--r--   0 sebastianmuller   (501) staff       (20)    15950 2023-04-03 13:58:53.000000 rebasin-0.0.8/rebasin/_wm_init_perms.py
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     9211 2023-04-01 09:25:31.000000 rebasin-0.0.8/rebasin/interpolation.py
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     6932 2023-04-03 13:58:53.000000 rebasin-0.0.8/rebasin/permutation_coordinate_descent.py
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     1654 2023-03-31 13:37:55.000000 rebasin-0.0.8/rebasin/structs.py
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     3651 2023-04-01 08:57:23.000000 rebasin-0.0.8/rebasin/util.py
-drwxr-xr-x   0 sebastianmuller   (501) staff       (20)        0 2023-04-03 14:00:17.395142 rebasin-0.0.8/rebasin.egg-info/
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     1750 2023-04-03 14:00:17.000000 rebasin-0.0.8/rebasin.egg-info/PKG-INFO
--rw-r--r--   0 sebastianmuller   (501) staff       (20)      425 2023-04-03 14:00:17.000000 rebasin-0.0.8/rebasin.egg-info/SOURCES.txt
--rw-r--r--   0 sebastianmuller   (501) staff       (20)        1 2023-04-03 14:00:17.000000 rebasin-0.0.8/rebasin.egg-info/dependency_links.txt
--rw-r--r--   0 sebastianmuller   (501) staff       (20)        8 2023-04-03 14:00:17.000000 rebasin-0.0.8/rebasin.egg-info/top_level.txt
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     1046 2023-04-03 14:00:17.401695 rebasin-0.0.8/setup.cfg
--rw-r--r--   0 sebastianmuller   (501) staff       (20)       38 2023-02-06 22:40:16.000000 rebasin-0.0.8/setup.py
-drwxr-xr-x   0 sebastianmuller   (501) staff       (20)        0 2023-04-03 14:00:17.399741 rebasin-0.0.8/tests/
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     4351 2023-04-03 13:58:53.000000 rebasin-0.0.8/tests/test_init_perms.py
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     7889 2023-04-01 10:00:26.000000 rebasin-0.0.8/tests/test_interpolation.py
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     3890 2023-04-03 13:58:53.000000 rebasin-0.0.8/tests/test_permutation_coordinate_descent.py
--rw-r--r--   0 sebastianmuller   (501) staff       (20)     3109 2023-04-03 13:52:03.000000 rebasin-0.0.8/tests/test_util.py
+drwxr-xr-x   0 sebastianmuller   (501) staff       (20)        0 2023-04-03 14:14:02.902750 rebasin-0.0.9/
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     1074 2023-02-23 11:53:52.000000 rebasin-0.0.9/LICENSE
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     1750 2023-04-03 14:14:02.903055 rebasin-0.0.9/PKG-INFO
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)      897 2023-04-01 08:57:23.000000 rebasin-0.0.9/README.md
+drwxr-xr-x   0 sebastianmuller   (501) staff       (20)        0 2023-04-03 14:14:02.892958 rebasin-0.0.9/rebasin/
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)      101 2023-04-03 13:59:02.000000 rebasin-0.0.9/rebasin/__init__.py
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)    15970 2023-04-03 14:13:06.000000 rebasin-0.0.9/rebasin/_init_perms_weight_matching.py
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     9211 2023-04-01 09:25:31.000000 rebasin-0.0.9/rebasin/interpolation.py
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     6945 2023-04-03 14:02:05.000000 rebasin-0.0.9/rebasin/permutation_coordinate_descent.py
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     1654 2023-03-31 13:37:55.000000 rebasin-0.0.9/rebasin/structs.py
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     3651 2023-04-01 08:57:23.000000 rebasin-0.0.9/rebasin/util.py
+drwxr-xr-x   0 sebastianmuller   (501) staff       (20)        0 2023-04-03 14:14:02.896216 rebasin-0.0.9/rebasin.egg-info/
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     1750 2023-04-03 14:14:02.000000 rebasin-0.0.9/rebasin.egg-info/PKG-INFO
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)      438 2023-04-03 14:14:02.000000 rebasin-0.0.9/rebasin.egg-info/SOURCES.txt
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)        1 2023-04-03 14:14:02.000000 rebasin-0.0.9/rebasin.egg-info/dependency_links.txt
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)        8 2023-04-03 14:14:02.000000 rebasin-0.0.9/rebasin.egg-info/top_level.txt
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     1046 2023-04-03 14:14:02.904387 rebasin-0.0.9/setup.cfg
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)       38 2023-02-06 22:40:16.000000 rebasin-0.0.9/setup.py
+drwxr-xr-x   0 sebastianmuller   (501) staff       (20)        0 2023-04-03 14:14:02.901627 rebasin-0.0.9/tests/
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     4364 2023-04-03 14:02:05.000000 rebasin-0.0.9/tests/test_init_perms.py
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     7889 2023-04-01 10:00:26.000000 rebasin-0.0.9/tests/test_interpolation.py
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     3890 2023-04-03 13:58:53.000000 rebasin-0.0.9/tests/test_permutation_coordinate_descent.py
+-rw-r--r--   0 sebastianmuller   (501) staff       (20)     3109 2023-04-03 13:52:03.000000 rebasin-0.0.9/tests/test_util.py
```

### Comparing `rebasin-0.0.8/LICENSE` & `rebasin-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `rebasin-0.0.8/PKG-INFO` & `rebasin-0.0.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rebasin
-Version: 0.0.8
+Version: 0.0.9
 Summary: An implementation of methods described in Git Re-basin-paper by Ainsworth et al.
 Home-page: https://github.com/snimu/rebasin
 Author: Sebastian Müller @snimu
 Author-email: sebastian.nicolas.mueller@gmail.com
 License: MIT
 Keywords: torch git-rebasin rebasin interpolate interpolation model deep-learning
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `rebasin-0.0.8/README.md` & `rebasin-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `rebasin-0.0.8/rebasin/_wm_init_perms.py` & `rebasin-0.0.9/rebasin/_init_perms_weight_matching.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 from __future__ import annotations
 
-from typing import Any
+from typing import Any, Union
 
 import torch
 from torch import nn
 from torchview import FunctionNode, ModuleNode, TensorNode, draw_graph
 
 from rebasin import util
 from rebasin.structs import (
     AxisType,
     ParameterInfo,
     Permutation,
 )
 
-NODE_TYPES = FunctionNode | ModuleNode | TensorNode
+NODE_TYPES = Union[FunctionNode, ModuleNode, TensorNode]  # noqa
 
 
 class PermutationInitializer:
     def __init__(self, model_a: nn.Module, model_b: nn.Module, input_data: Any) -> None:
         self.model_a = model_a
         self.model_b = model_b
         self.input_data = input_data
```

### Comparing `rebasin-0.0.8/rebasin/interpolation.py` & `rebasin-0.0.9/rebasin/interpolation.py`

 * *Files identical despite different names*

### Comparing `rebasin-0.0.8/rebasin/permutation_coordinate_descent.py` & `rebasin-0.0.9/rebasin/permutation_coordinate_descent.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 from typing import Any
 
 import torch
 from scipy.optimize import linear_sum_assignment  # type: ignore[import]
 from torch import nn
 
-from rebasin._wm_init_perms import PermutationInitializer
+from rebasin._init_perms_weight_matching import PermutationInitializer
 
 
 def calculate_progress(
         cost_mat: torch.Tensor, perm_old: torch.Tensor, perm_new: torch.Tensor
 ) -> bool:
     """
     Compute the progress of the permutation.
```

### Comparing `rebasin-0.0.8/rebasin/structs.py` & `rebasin-0.0.9/rebasin/structs.py`

 * *Files identical despite different names*

### Comparing `rebasin-0.0.8/rebasin/util.py` & `rebasin-0.0.9/rebasin/util.py`

 * *Files identical despite different names*

### Comparing `rebasin-0.0.8/rebasin.egg-info/PKG-INFO` & `rebasin-0.0.9/rebasin.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rebasin
-Version: 0.0.8
+Version: 0.0.9
 Summary: An implementation of methods described in Git Re-basin-paper by Ainsworth et al.
 Home-page: https://github.com/snimu/rebasin
 Author: Sebastian Müller @snimu
 Author-email: sebastian.nicolas.mueller@gmail.com
 License: MIT
 Keywords: torch git-rebasin rebasin interpolate interpolation model deep-learning
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `rebasin-0.0.8/setup.cfg` & `rebasin-0.0.9/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = rebasin
-version = 0.0.8
+version = 0.0.9
 description = An implementation of methods described in Git Re-basin-paper by Ainsworth et al.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/snimu/rebasin
 author = Sebastian Müller @snimu
 author_email = sebastian.nicolas.mueller@gmail.com
 license = MIT
```

### Comparing `rebasin-0.0.8/tests/test_init_perms.py` & `rebasin-0.0.9/tests/test_init_perms.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from __future__ import annotations
 
 import torch
 from torch import nn
 from torchvision.models import resnet18  # type: ignore[import]
 
 from rebasin import util
-from rebasin._wm_init_perms import PermutationInitializer
+from rebasin._init_perms_weight_matching import PermutationInitializer
 from rebasin.structs import AxisType
 
 from .fixtures.models import MLP, ModuleWithWeirdWeightAndBiasNames
 
 
 def test_init_permutations_weird_weight_bias_names() -> None:
     model_a = ModuleWithWeirdWeightAndBiasNames()
```

### Comparing `rebasin-0.0.8/tests/test_interpolation.py` & `rebasin-0.0.9/tests/test_interpolation.py`

 * *Files identical despite different names*

### Comparing `rebasin-0.0.8/tests/test_permutation_coordinate_descent.py` & `rebasin-0.0.9/tests/test_permutation_coordinate_descent.py`

 * *Files identical despite different names*

### Comparing `rebasin-0.0.8/tests/test_util.py` & `rebasin-0.0.9/tests/test_util.py`

 * *Files identical despite different names*

