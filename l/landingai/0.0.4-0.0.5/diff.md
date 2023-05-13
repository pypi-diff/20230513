# Comparing `tmp/landingai-0.0.4.tar.gz` & `tmp/landingai-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "landingai-0.0.4.tar", max compression
+gzip compressed data, was "landingai-0.0.5.tar", max compression
```

## Comparing `landingai-0.0.4.tar` & `landingai-0.0.5.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0     3994 2023-05-12 06:20:53.826686 landingai-0.0.4/README.md
--rw-r--r--   0        0        0       40 2023-05-11 23:35:20.932651 landingai-0.0.4/landingai/__init__.py
--rw-r--r--   0        0        0     1953 2023-05-12 06:05:01.363124 landingai-0.0.4/landingai/common.py
--rw-r--r--   0        0        0     7308 2023-05-11 23:35:20.933105 landingai-0.0.4/landingai/predict.py
--rw-r--r--   0        0        0     1901 2023-05-12 05:26:12.539615 landingai-0.0.4/landingai/visualize.py
--rw-r--r--   0        0        0      843 2023-05-12 06:23:10.006279 landingai-0.0.4/pyproject.toml
--rw-r--r--   0        0        0     4896 1970-01-01 00:00:00.000000 landingai-0.0.4/PKG-INFO
+-rw-r--r--   0        0        0     3994 2023-05-12 21:15:52.967298 landingai-0.0.5/README.md
+-rw-r--r--   0        0        0       40 2023-05-11 23:35:20.932651 landingai-0.0.5/landingai/__init__.py
+-rw-r--r--   0        0        0     2377 2023-05-12 06:50:21.023938 landingai-0.0.5/landingai/common.py
+-rw-r--r--   0        0        0     7308 2023-05-11 23:35:20.933105 landingai-0.0.5/landingai/predict.py
+-rw-r--r--   0        0        0     2101 2023-05-12 16:17:00.941369 landingai-0.0.5/landingai/visualize.py
+-rw-r--r--   0        0        0      843 2023-05-12 21:17:24.044850 landingai-0.0.5/pyproject.toml
+-rw-r--r--   0        0        0     4896 1970-01-01 00:00:00.000000 landingai-0.0.5/PKG-INFO
```

### Comparing `landingai-0.0.4/README.md` & `landingai-0.0.5/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -25,17 +25,17 @@
 - Install the library with the above command.
 - Create a `Predictor` with your inference endpoint id, landing API key and secret.
 - Call `predict()` with an image (in numpy array format).
 
 ```python
 from landingai.predict import Predictor
 # Find your API key and secrets
-endpoint_id = "FILL YOUR INFERENCE ENDPOINT ID"
-api_key = "FILL YOUR API KEY"
-api_secret = "FILL YOUR API SECRET"
+endpoint_id = "FILL_YOUR_INFERENCE_ENDPOINT_ID"
+api_key = "FILL_YOUR_API_KEY"
+api_secret = "FILL_YOUR_API_SECRET"
 # Load your image
 image = ...
 # Run inference
 predictor = Predictor(endpoint_id, api_key, api_secret)
 predictions = predictor.predict(image)
 ```
```

### Comparing `landingai-0.0.4/landingai/common.py` & `landingai-0.0.5/landingai/common.py`

 * *Files 20% similar despite different names*

```diff
@@ -3,35 +3,40 @@
 from typing import Dict, List, Tuple
 
 import numpy as np
 from pydantic import BaseModel, BaseSettings
 
 
 class Credential(BaseSettings):
-    # TODO: support env vars
+    """Landing AI API credential of a particular user."""
     api_key: str
     api_secret: str
 
 
 class Prediction(BaseModel):
-    # TODO: add docs
+    """The base/parent prediction class that stores the common shared properties of a prediction.
+    E.g, the confidence score, the predicted label.
+    """
     id: str
     score: float
     label_name: str
     label_index: int
 
 
 class ObjectDetectionPrediction(Prediction):
-    # TODO: add docs
-    # xmin, ymin, xmax, ymax
+    """A single bounding box prediction for an image.
+    It includes a predicted bounding box (xmin, ymin, xmax, ymax), confidence score and the predicted label.
+    """
     bboxes: Tuple[int, int, int, int]
 
 
 class SegmentationPrediction(Prediction):
-    # TODO: add docs
+    """A single segmentation mask prediction for an image.
+    It includes a predicted segmentation mask, confidence score and the predicted label.
+    """
     encoded_mask: str
     encoding_map: Dict[str, int]
     mask_shape: Tuple[int, int]
 
     @cached_property
     def decoded_boolean_mask(self) -> np.ndarray:
         # NOTE: 1 and 0, not True and False
@@ -48,18 +53,20 @@
     class Config:
         keep_untouched=(cached_property, )
 
 
 def decode_bitmap_rle(bitmap: str, encoding_map: Dict[str, int]) -> List[int]:
     """
     Decode bitmap string to numpy array
-    -----
-    bitmap: str
+
+    Parameters
+    ----------
+    bitmap:
         Single run-length encoded bitmap string. e.g. "5Z3N2Z"
-    encoding_map: Dict[str, int]
+    encoding_map:
         Dictionary with the enconding used to generate the bitmap. e.g. {'Z':0, 'N':1}
 
     Return
     -----
     A flattened segmentation mask (with 0s and 1s) for a single class.
     """
     flat_mask = []
```

### Comparing `landingai-0.0.4/landingai/predict.py` & `landingai-0.0.5/landingai/predict.py`

 * *Files identical despite different names*

### Comparing `landingai-0.0.4/landingai/visualize.py` & `landingai-0.0.5/landingai/visualize.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,27 +1,32 @@
+import logging
 from typing import List
 
 import cv2
 import numpy as np
 from PIL import Image
 from segmentation_mask_overlay import overlay_masks
 
 from landingai.common import (
     ObjectDetectionPrediction,
     Prediction,
     SegmentationPrediction,
 )
 
 SPACING_PIXELS = -5
+_LOGGER = logging.getLogger(__name__)
 
 
 def overlay_predictions(
     predictions: List[Prediction], image: np.ndarray
 ) -> Image.Image:
     """Overlay the prediction results on the input image and return the image with overlaid."""
+    if len(predictions) == 0:
+        _LOGGER.warning("No predictions to overlay, returning original image")
+        return Image.fromarray(image)
     types = {type(pred) for pred in predictions}
     assert len(types) == 1, f"Expecting only one type of prediction, got {types}"
     overlay_func = _OVERLAY_FUNC_MAP[types.pop()]
     return overlay_func(predictions, image)
 
 
 def overlay_bboxes(predictions: List[ObjectDetectionPrediction], image: np.ndarray) -> Image.Image:
```

### Comparing `landingai-0.0.4/pyproject.toml` & `landingai-0.0.5/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "landingai"
-version = "0.0.4"
+version = "0.0.5"
 description = "Helper library for interacting with Landing AI LandingLens"
 authors = ["Landing AI <dev@landing.ai>"]
 readme = "README.md"
 packages = [{include = "landingai"}]
 
 [tool.poetry.urls]
 "Homepage" = "https://landing.ai"
```

### Comparing `landingai-0.0.4/PKG-INFO` & `landingai-0.0.5/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: landingai
-Version: 0.0.4
+Version: 0.0.5
 Summary: Helper library for interacting with Landing AI LandingLens
 Author: Landing AI
 Author-email: dev@landing.ai
 Requires-Python: >=3.8
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -48,17 +48,17 @@
 - Install the library with the above command.
 - Create a `Predictor` with your inference endpoint id, landing API key and secret.
 - Call `predict()` with an image (in numpy array format).
 
 ```python
 from landingai.predict import Predictor
 # Find your API key and secrets
-endpoint_id = "FILL YOUR INFERENCE ENDPOINT ID"
-api_key = "FILL YOUR API KEY"
-api_secret = "FILL YOUR API SECRET"
+endpoint_id = "FILL_YOUR_INFERENCE_ENDPOINT_ID"
+api_key = "FILL_YOUR_API_KEY"
+api_secret = "FILL_YOUR_API_SECRET"
 # Load your image
 image = ...
 # Run inference
 predictor = Predictor(endpoint_id, api_key, api_secret)
 predictions = predictor.predict(image)
 ```
```

