# Comparing `tmp/scikit-llm-0.1.0a1.tar.gz` & `tmp/scikit-llm-0.1.0b1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "scikit-llm-0.1.0a1.tar", last modified: Fri May 12 18:50:51 2023, max compression
+gzip compressed data, was "scikit-llm-0.1.0b1.tar", last modified: Sat May 13 17:57:54 2023, max compression
```

## Comparing `scikit-llm-0.1.0a1.tar` & `scikit-llm-0.1.0b1.tar`

### file list

```diff
@@ -1,20 +1,24 @@
-drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-12 18:50:51.654248 scikit-llm-0.1.0a1/
--rw-r--r--   0 kostrominoleg   (501) staff       (20)     1077 2023-05-12 18:41:11.000000 scikit-llm-0.1.0a1/LICENSE
--rw-r--r--   0 kostrominoleg   (501) staff       (20)      545 2023-05-12 18:50:51.653942 scikit-llm-0.1.0a1/PKG-INFO
--rw-r--r--   0 kostrominoleg   (501) staff       (20)       12 2023-05-12 18:41:11.000000 scikit-llm-0.1.0a1/README.md
--rw-r--r--   0 kostrominoleg   (501) staff       (20)      764 2023-05-12 18:50:32.000000 scikit-llm-0.1.0a1/pyproject.toml
-drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-12 18:50:51.651933 scikit-llm-0.1.0a1/scikit_llm.egg-info/
--rw-r--r--   0 kostrominoleg   (501) staff       (20)      545 2023-05-12 18:50:51.000000 scikit-llm-0.1.0a1/scikit_llm.egg-info/PKG-INFO
--rw-r--r--   0 kostrominoleg   (501) staff       (20)      317 2023-05-12 18:50:51.000000 scikit-llm-0.1.0a1/scikit_llm.egg-info/SOURCES.txt
--rw-r--r--   0 kostrominoleg   (501) staff       (20)        1 2023-05-12 18:50:51.000000 scikit-llm-0.1.0a1/scikit_llm.egg-info/dependency_links.txt
--rw-r--r--   0 kostrominoleg   (501) staff       (20)       49 2023-05-12 18:50:51.000000 scikit-llm-0.1.0a1/scikit_llm.egg-info/requires.txt
--rw-r--r--   0 kostrominoleg   (501) staff       (20)        6 2023-05-12 18:50:51.000000 scikit-llm-0.1.0a1/scikit_llm.egg-info/top_level.txt
--rw-r--r--   0 kostrominoleg   (501) staff       (20)       38 2023-05-12 18:50:51.654345 scikit-llm-0.1.0a1/setup.cfg
-drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-12 18:50:51.652495 scikit-llm-0.1.0a1/skllm/
--rw-r--r--   0 kostrominoleg   (501) staff       (20)       97 2023-05-12 18:41:11.000000 scikit-llm-0.1.0a1/skllm/__init__.py
--rw-r--r--   0 kostrominoleg   (501) staff       (20)      324 2023-05-12 18:41:11.000000 scikit-llm-0.1.0a1/skllm/config.py
-drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-12 18:50:51.652963 scikit-llm-0.1.0a1/skllm/models/
--rw-r--r--   0 kostrominoleg   (501) staff       (20)     4437 2023-05-12 18:41:11.000000 scikit-llm-0.1.0a1/skllm/models/gpt_zero_shot_clf.py
-drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-12 18:50:51.653576 scikit-llm-0.1.0a1/skllm/openai/
--rw-r--r--   0 kostrominoleg   (501) staff       (20)      732 2023-05-12 18:41:11.000000 scikit-llm-0.1.0a1/skllm/openai/chatgpt.py
--rw-r--r--   0 kostrominoleg   (501) staff       (20)     2186 2023-05-12 18:41:11.000000 scikit-llm-0.1.0a1/skllm/openai/prompts.py
+drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-13 17:57:54.379731 scikit-llm-0.1.0b1/
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)     1077 2023-05-12 18:41:11.000000 scikit-llm-0.1.0b1/LICENSE
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)     4193 2023-05-13 17:57:54.379400 scikit-llm-0.1.0b1/PKG-INFO
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)     3660 2023-05-13 17:42:08.000000 scikit-llm-0.1.0b1/README.md
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)      780 2023-05-13 17:57:13.000000 scikit-llm-0.1.0b1/pyproject.toml
+drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-13 17:57:54.376910 scikit-llm-0.1.0b1/scikit_llm.egg-info/
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)     4193 2023-05-13 17:57:54.000000 scikit-llm-0.1.0b1/scikit_llm.egg-info/PKG-INFO
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)      404 2023-05-13 17:57:54.000000 scikit-llm-0.1.0b1/scikit_llm.egg-info/SOURCES.txt
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)        1 2023-05-13 17:57:54.000000 scikit-llm-0.1.0b1/scikit_llm.egg-info/dependency_links.txt
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)       62 2023-05-13 17:57:54.000000 scikit-llm-0.1.0b1/scikit_llm.egg-info/requires.txt
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)        6 2023-05-13 17:57:54.000000 scikit-llm-0.1.0b1/scikit_llm.egg-info/top_level.txt
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)       38 2023-05-13 17:57:54.379810 scikit-llm-0.1.0b1/setup.cfg
+drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-13 17:57:54.377463 scikit-llm-0.1.0b1/skllm/
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)       97 2023-05-12 18:41:11.000000 scikit-llm-0.1.0b1/skllm/__init__.py
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)      592 2023-05-13 17:42:03.000000 scikit-llm-0.1.0b1/skllm/config.py
+drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-13 17:57:54.378269 scikit-llm-0.1.0b1/skllm/datasets/
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)      142 2023-05-13 15:03:57.000000 scikit-llm-0.1.0b1/skllm/datasets/__init__.py
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)     5870 2023-05-13 15:02:46.000000 scikit-llm-0.1.0b1/skllm/datasets/multi_class.py
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)     1438 2023-05-13 15:03:34.000000 scikit-llm-0.1.0b1/skllm/datasets/multi_label.py
+drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-13 17:57:54.378536 scikit-llm-0.1.0b1/skllm/models/
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)     5517 2023-05-13 17:55:02.000000 scikit-llm-0.1.0b1/skllm/models/gpt_zero_shot_clf.py
+drwxr-xr-x   0 kostrominoleg   (501) staff       (20)        0 2023-05-13 17:57:54.379002 scikit-llm-0.1.0b1/skllm/openai/
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)      873 2023-05-13 17:37:39.000000 scikit-llm-0.1.0b1/skllm/openai/chatgpt.py
+-rw-r--r--   0 kostrominoleg   (501) staff       (20)     2186 2023-05-12 18:41:11.000000 scikit-llm-0.1.0b1/skllm/openai/prompts.py
```

### Comparing `scikit-llm-0.1.0a1/LICENSE` & `scikit-llm-0.1.0b1/LICENSE`

 * *Files identical despite different names*

### Comparing `scikit-llm-0.1.0a1/skllm/models/gpt_zero_shot_clf.py` & `scikit-llm-0.1.0b1/skllm/models/gpt_zero_shot_clf.py`

 * *Files 26% similar despite different names*

```diff
@@ -3,15 +3,20 @@
 import pandas as pd
 from collections import Counter
 import random
 from tqdm import tqdm
 from abc import ABC, abstractmethod
 from sklearn.base import BaseEstimator, ClassifierMixin
 from skllm.openai.prompts import get_zero_shot_prompt_slc, get_zero_shot_prompt_mlc
-from skllm.openai.chatgpt import construct_message, get_chat_completion, extract_json_key
+from skllm.openai.chatgpt import (
+    construct_message,
+    get_chat_completion,
+    extract_json_key,
+)
+from skllm.config import SKLLMConfig as _Config
 
 
 class _BaseZeroShotGPTClassifier(ABC, BaseEstimator, ClassifierMixin):
     def __init__(
         self,
         openai_key: Optional[str] = None,
         openai_org: Optional[str] = None,
@@ -19,28 +24,45 @@
     ):
         self.openai_key = openai_key
         self.openai_org = openai_org
         self.openai_model = openai_model
 
     def fit(
         self,
-        X: Union[np.ndarray, pd.Series, List[str]],
+        X: Optional[Union[np.ndarray, pd.Series, List[str]]],
         y: Union[np.ndarray, pd.Series, List[str], List[List[str]]],
     ):
+        if isinstance(X, np.ndarray):
+            X = np.squeeze(X)
         self.classes_, self.probabilities_ = self._get_unique_targets(y)
         return self
 
-    def predict(self, X):
+    def predict(self, X: Union[np.ndarray, pd.Series, List[str]]):
+        if isinstance(X, np.ndarray):
+            X = np.squeeze(X)
         predictions = []
         for i in tqdm(range(len(X))):
             predictions.append(self._predict_single(X[i]))
         return predictions
 
-    def _get_openai_keys(self):
-        return self.openai_key, self.openai_org
+    def _get_openai_key(self):
+        key = self.openai_key
+        if key is None:
+            key = _Config.get_openai_key()
+        if key is None:
+            raise RuntimeError("OpenAI key was not found")
+        return key
+
+    def _get_openai_org(self):
+        key = self.openai_org
+        if key is None:
+            key = _Config.get_openai_org()
+        if key is None:
+            raise RuntimeError("OpenAI organization was not found")
+        return key
 
     @abstractmethod
     def _extract_labels(self, y: Any) -> List[str]:
         pass
 
     def _get_unique_targets(self, y):
         labels = self._extract_labels(y)
@@ -52,21 +74,21 @@
         classes, probs = [], []
         for l, c in counts.items():
             classes.append(l)
             probs.append(c / total)
 
         return classes, probs
 
-    def _get_completion(self, x):
+    def _get_chat_completion(self, x):
         prompt = self._get_prompt(x)
         msgs = []
         msgs.append(construct_message("system", "You are a text classification model."))
         msgs.append(construct_message("user", prompt))
         completion = get_chat_completion(
-            msgs, self.openai_key, self.openai_org, self.openai_model
+            msgs, self._get_openai_key(), self._get_openai_org(), self.openai_model
         )
         return completion
 
 
 class ZeroShotGPTClassifier(_BaseZeroShotGPTClassifier):
     def __init__(
         self,
@@ -83,26 +105,35 @@
             labels = y
         return labels
 
     def _get_prompt(self, x) -> str:
         return get_zero_shot_prompt_slc(x, self.classes_)
 
     def _predict_single(self, x):
-        completion = self._get_completion(x)
+        completion = self._get_chat_completion(x)
         try:
             label = str(
                 extract_json_key(completion.choices[0].message["content"], "label")
             )
         except Exception as e:
             label = ""
 
         if label not in self.classes_:
             label = random.choices(self.classes_, self.probabilities_)[0]
         return label
 
+    def fit(
+        self,
+        X: Optional[Union[np.ndarray, pd.Series, List[str]]],
+        y: Union[np.ndarray, pd.Series, List[str]],
+    ):
+        if isinstance(y, np.ndarray):
+            y = np.squeeze(y)
+        return super().fit(X, y)
+
 
 class MultiLabelZeroShotGPTClassifier(_BaseZeroShotGPTClassifier):
     def __init__(
         self,
         openai_key: Optional[str] = None,
         openai_org: Optional[str] = None,
         openai_model: str = "gpt-3.5-turbo",
@@ -121,22 +152,29 @@
 
         return labels
 
     def _get_prompt(self, x) -> str:
         return get_zero_shot_prompt_mlc(x, self.classes_, self.max_labels)
 
     def _predict_single(self, x):
-        completion = self._get_completion(x)
+        completion = self._get_chat_completion(x)
         try:
             labels = extract_json_key(completion.choices[0].message["content"], "label")
             if not isinstance(labels, list):
                 raise RuntimeError("Invalid labels type, expected list")
         except Exception as e:
             labels = []
 
         labels = list(filter(lambda l: l in self.classes_, labels))
 
         if len(labels) > self.max_labels:
             labels = labels[: self.max_labels - 1]
         elif len(labels) < 1:
             labels = [random.choices(self.classes_, self.probabilities_)[0]]
-        return labels
+        return labels
+
+    def fit(
+        self,
+        X: Optional[Union[np.ndarray, pd.Series, List[str]]],
+        y: List[List[str]],
+    ):
+        return super().fit(X, y)
```

### Comparing `scikit-llm-0.1.0a1/skllm/openai/chatgpt.py` & `scikit-llm-0.1.0b1/skllm/openai/chatgpt.py`

 * *Files 13% similar despite different names*

```diff
@@ -2,22 +2,25 @@
 import json
 
 def construct_message(role, content):
     if role not in ("system", "user", "assistant"):
         raise ValueError("Invalid role")
     return {"role": role, "content": content}
 
-def get_chat_completion(messages, key, org, model="gpt-3.5-turbo"):
+def get_chat_completion(messages, key, org, model="gpt-3.5-turbo", max_retries = 3):
     openai.api_key = key
     openai.organization = org
-    completion = openai.ChatCompletion.create(
-        model=model, temperature=0., messages=messages
-    )
-
-    return completion
+    for _ in range(max_retries):
+        try:
+            completion = openai.ChatCompletion.create(
+                model=model, temperature=0., messages=messages
+            )
+            return completion
+        except Exception:
+            continue
 
 def extract_json_key(json_, key):
     try: 
         as_json = json.loads(json_.replace('\n', '')) 
         if key not in as_json.keys():
             raise KeyError("The required key was not found")
         return as_json[key]
```

### Comparing `scikit-llm-0.1.0a1/skllm/openai/prompts.py` & `scikit-llm-0.1.0b1/skllm/openai/prompts.py`

 * *Files identical despite different names*

