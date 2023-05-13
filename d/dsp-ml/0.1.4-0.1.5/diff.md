# Comparing `tmp/dsp-ml-0.1.4.tar.gz` & `tmp/dsp-ml-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/dsp-ml-0.1.4.tar", last modified: Mon Feb 13 20:10:06 2023, max compression
+gzip compressed data, was "dsp-ml-0.1.5.tar", last modified: Sat May 13 09:10:26 2023, max compression
```

## Comparing `dsp-ml-0.1.4.tar` & `dsp-ml-0.1.5.tar`

### file list

```diff
@@ -1,39 +1,49 @@
-drwxrwxr-x   0 okhattab  (1000) okhattab  (1000)        0 2023-02-13 20:10:06.861175 dsp-ml-0.1.4/
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      612 2023-02-13 20:10:06.861175 dsp-ml-0.1.4/PKG-INFO
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     1236 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/README.md
-drwxrwxr-x   0 okhattab  (1000) okhattab  (1000)        0 2023-02-13 20:10:06.857175 dsp-ml-0.1.4/dsp/
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      101 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/__init__.py
-drwxrwxr-x   0 okhattab  (1000) okhattab  (1000)        0 2023-02-13 20:10:06.857175 dsp-ml-0.1.4/dsp/evaluation/
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)        1 2023-02-11 12:04:42.000000 dsp-ml-0.1.4/dsp/evaluation/__init__.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     2496 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/evaluation/utils.py
-drwxrwxr-x   0 okhattab  (1000) okhattab  (1000)        0 2023-02-13 20:10:06.857175 dsp-ml-0.1.4/dsp/modules/
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)       71 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/modules/__init__.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      804 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/modules/cache_utils.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     1892 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/modules/colbertv2.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     4023 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/modules/gpt3.py
-drwxrwxr-x   0 okhattab  (1000) okhattab  (1000)        0 2023-02-13 20:10:06.857175 dsp-ml-0.1.4/dsp/primitives/
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      121 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/primitives/__init__.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     5171 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/primitives/compiler.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     3008 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/primitives/demonstrate.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     5949 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/primitives/predict.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     1450 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/primitives/primitives.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      733 2023-02-11 12:03:06.000000 dsp-ml-0.1.4/dsp/primitives/search.py
-drwxrwxr-x   0 okhattab  (1000) okhattab  (1000)        0 2023-02-13 20:10:06.857175 dsp-ml-0.1.4/dsp/templates/
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      173 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/templates/__init__.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     7718 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/templates/template_v2.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     1237 2023-02-11 12:09:38.000000 dsp-ml-0.1.4/dsp/templates/template_v3.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      275 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/templates/utils.py
-drwxrwxr-x   0 okhattab  (1000) okhattab  (1000)        0 2023-02-13 20:10:06.861175 dsp-ml-0.1.4/dsp/utils/
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      122 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/utils/__init__.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     7071 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/utils/dpr.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     5933 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/utils/metrics.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     1456 2023-02-13 19:59:04.000000 dsp-ml-0.1.4/dsp/utils/settings.py
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)     4712 2023-02-11 11:46:54.000000 dsp-ml-0.1.4/dsp/utils/utils.py
-drwxrwxr-x   0 okhattab  (1000) okhattab  (1000)        0 2023-02-13 20:10:06.861175 dsp-ml-0.1.4/dsp_ml.egg-info/
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      612 2023-02-13 20:10:06.000000 dsp-ml-0.1.4/dsp_ml.egg-info/PKG-INFO
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      702 2023-02-13 20:10:06.000000 dsp-ml-0.1.4/dsp_ml.egg-info/SOURCES.txt
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)        1 2023-02-13 20:10:06.000000 dsp-ml-0.1.4/dsp_ml.egg-info/dependency_links.txt
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)       69 2023-02-13 20:10:06.000000 dsp-ml-0.1.4/dsp_ml.egg-info/requires.txt
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)        4 2023-02-13 20:10:06.000000 dsp-ml-0.1.4/dsp_ml.egg-info/top_level.txt
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)       38 2023-02-13 20:10:06.861175 dsp-ml-0.1.4/setup.cfg
--rw-rw-r--   0 okhattab  (1000) okhattab  (1000)      895 2023-02-13 20:09:22.000000 dsp-ml-0.1.4/setup.py
+drwxr-xr-x   0 sri        (501) staff       (20)        0 2023-05-13 09:10:26.420172 dsp-ml-0.1.5/
+-rw-r--r--   0 sri        (501) staff       (20)     1085 2023-02-08 07:26:37.000000 dsp-ml-0.1.5/LICENSE
+-rw-r--r--   0 sri        (501) staff       (20)      595 2023-05-13 09:10:26.420024 dsp-ml-0.1.5/PKG-INFO
+-rw-r--r--   0 sri        (501) staff       (20)     5224 2023-04-08 05:34:57.000000 dsp-ml-0.1.5/README.md
+drwxr-xr-x   0 sri        (501) staff       (20)        0 2023-05-13 09:10:26.412074 dsp-ml-0.1.5/dsp/
+-rw-r--r--   0 sri        (501) staff       (20)      101 2023-02-08 07:26:37.000000 dsp-ml-0.1.5/dsp/__init__.py
+drwxr-xr-x   0 sri        (501) staff       (20)        0 2023-05-13 09:10:26.412725 dsp-ml-0.1.5/dsp/evaluation/
+-rw-r--r--   0 sri        (501) staff       (20)        1 2023-02-08 07:26:37.000000 dsp-ml-0.1.5/dsp/evaluation/__init__.py
+-rw-r--r--   0 sri        (501) staff       (20)     2496 2023-05-06 19:22:54.000000 dsp-ml-0.1.5/dsp/evaluation/utils.py
+drwxr-xr-x   0 sri        (501) staff       (20)        0 2023-05-13 09:10:26.415716 dsp-ml-0.1.5/dsp/modules/
+-rw-r--r--   0 sri        (501) staff       (20)      181 2023-05-13 09:08:14.000000 dsp-ml-0.1.5/dsp/modules/__init__.py
+-rw-r--r--   0 sri        (501) staff       (20)      804 2023-05-01 21:06:09.000000 dsp-ml-0.1.5/dsp/modules/cache_utils.py
+-rw-r--r--   0 sri        (501) staff       (20)     4311 2023-04-24 17:06:17.000000 dsp-ml-0.1.5/dsp/modules/cohere.py
+-rw-r--r--   0 sri        (501) staff       (20)     2191 2023-03-27 05:01:30.000000 dsp-ml-0.1.5/dsp/modules/colbertv2.py
+-rw-r--r--   0 sri        (501) staff       (20)     6894 2023-05-11 20:41:39.000000 dsp-ml-0.1.5/dsp/modules/gpt3.py
+-rw-r--r--   0 sri        (501) staff       (20)     4201 2023-04-24 17:06:17.000000 dsp-ml-0.1.5/dsp/modules/hf.py
+-rw-r--r--   0 sri        (501) staff       (20)      682 2023-04-24 17:06:17.000000 dsp-ml-0.1.5/dsp/modules/hf_client.py
+-rw-r--r--   0 sri        (501) staff       (20)     1973 2023-05-13 09:08:14.000000 dsp-ml-0.1.5/dsp/modules/hf_server.py
+-rw-r--r--   0 sri        (501) staff       (20)     2299 2023-04-26 16:56:03.000000 dsp-ml-0.1.5/dsp/modules/lm.py
+-rw-r--r--   0 sri        (501) staff       (20)      691 2023-05-13 09:08:14.000000 dsp-ml-0.1.5/dsp/modules/sbert.py
+-rw-r--r--   0 sri        (501) staff       (20)     5981 2023-03-02 18:50:40.000000 dsp-ml-0.1.5/dsp/modules/sentence_vectorizer.py
+drwxr-xr-x   0 sri        (501) staff       (20)        0 2023-05-13 09:10:26.417380 dsp-ml-0.1.5/dsp/primitives/
+-rw-r--r--   0 sri        (501) staff       (20)      145 2023-03-27 05:01:30.000000 dsp-ml-0.1.5/dsp/primitives/__init__.py
+-rw-r--r--   0 sri        (501) staff       (20)     5171 2023-03-02 18:50:40.000000 dsp-ml-0.1.5/dsp/primitives/compiler.py
+-rw-r--r--   0 sri        (501) staff       (20)     5767 2023-05-11 20:41:39.000000 dsp-ml-0.1.5/dsp/primitives/demonstrate.py
+-rw-r--r--   0 sri        (501) staff       (20)     2513 2023-03-27 05:01:30.000000 dsp-ml-0.1.5/dsp/primitives/inspect.py
+-rw-r--r--   0 sri        (501) staff       (20)     7959 2023-04-25 10:15:30.000000 dsp-ml-0.1.5/dsp/primitives/predict.py
+-rw-r--r--   0 sri        (501) staff       (20)     1449 2023-03-27 05:01:30.000000 dsp-ml-0.1.5/dsp/primitives/primitives.py
+-rw-r--r--   0 sri        (501) staff       (20)     2358 2023-05-13 09:08:14.000000 dsp-ml-0.1.5/dsp/primitives/search.py
+drwxr-xr-x   0 sri        (501) staff       (20)        0 2023-05-13 09:10:26.418146 dsp-ml-0.1.5/dsp/templates/
+-rw-r--r--   0 sri        (501) staff       (20)      173 2023-02-08 07:26:37.000000 dsp-ml-0.1.5/dsp/templates/__init__.py
+-rw-r--r--   0 sri        (501) staff       (20)     8070 2023-04-08 05:34:53.000000 dsp-ml-0.1.5/dsp/templates/template_v2.py
+-rw-r--r--   0 sri        (501) staff       (20)     1648 2023-04-08 05:34:53.000000 dsp-ml-0.1.5/dsp/templates/template_v3.py
+-rw-r--r--   0 sri        (501) staff       (20)     1156 2023-03-27 05:01:30.000000 dsp-ml-0.1.5/dsp/templates/utils.py
+drwxr-xr-x   0 sri        (501) staff       (20)        0 2023-05-13 09:10:26.419141 dsp-ml-0.1.5/dsp/utils/
+-rw-r--r--   0 sri        (501) staff       (20)      123 2023-03-02 18:50:40.000000 dsp-ml-0.1.5/dsp/utils/__init__.py
+-rw-r--r--   0 sri        (501) staff       (20)     4903 2023-04-24 17:06:17.000000 dsp-ml-0.1.5/dsp/utils/ann_utils.py
+-rw-r--r--   0 sri        (501) staff       (20)     7071 2023-02-08 07:26:37.000000 dsp-ml-0.1.5/dsp/utils/dpr.py
+-rw-r--r--   0 sri        (501) staff       (20)     5933 2023-02-08 07:26:37.000000 dsp-ml-0.1.5/dsp/utils/metrics.py
+-rw-r--r--   0 sri        (501) staff       (20)     2183 2023-05-13 09:08:14.000000 dsp-ml-0.1.5/dsp/utils/settings.py
+-rw-r--r--   0 sri        (501) staff       (20)     4769 2023-03-27 05:01:30.000000 dsp-ml-0.1.5/dsp/utils/utils.py
+drwxr-xr-x   0 sri        (501) staff       (20)        0 2023-05-13 09:10:26.419844 dsp-ml-0.1.5/dsp_ml.egg-info/
+-rw-r--r--   0 sri        (501) staff       (20)      595 2023-05-13 09:10:26.000000 dsp-ml-0.1.5/dsp_ml.egg-info/PKG-INFO
+-rw-r--r--   0 sri        (501) staff       (20)      923 2023-05-13 09:10:26.000000 dsp-ml-0.1.5/dsp_ml.egg-info/SOURCES.txt
+-rw-r--r--   0 sri        (501) staff       (20)        1 2023-05-13 09:10:26.000000 dsp-ml-0.1.5/dsp_ml.egg-info/dependency_links.txt
+-rw-r--r--   0 sri        (501) staff       (20)       69 2023-05-13 09:10:26.000000 dsp-ml-0.1.5/dsp_ml.egg-info/requires.txt
+-rw-r--r--   0 sri        (501) staff       (20)        4 2023-05-13 09:10:26.000000 dsp-ml-0.1.5/dsp_ml.egg-info/top_level.txt
+-rw-r--r--   0 sri        (501) staff       (20)       38 2023-05-13 09:10:26.420220 dsp-ml-0.1.5/setup.cfg
+-rw-r--r--   0 sri        (501) staff       (20)      895 2023-05-13 09:09:51.000000 dsp-ml-0.1.5/setup.py
```

### Comparing `dsp-ml-0.1.4/PKG-INFO` & `dsp-ml-0.1.5/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,18 +1,17 @@
-Metadata-Version: 1.2
+Metadata-Version: 2.1
 Name: dsp-ml
-Version: 0.1.4
+Version: 0.1.5
 Summary: Demonstrate-Search-Predict
 Home-page: https://github.com/stanfordnlp/dsp
 Author: Omar Khattab
 Author-email: okhattab@stanford.edu
 License: MIT License
-Description: UNKNOWN
-Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: POSIX :: Linux
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
-Requires-Python: >=3.8
+Requires-Python: >=3.9
+License-File: LICENSE
```

### Comparing `dsp-ml-0.1.4/dsp/evaluation/utils.py` & `dsp-ml-0.1.5/dsp/evaluation/utils.py`

 * *Files identical despite different names*

### Comparing `dsp-ml-0.1.4/dsp/modules/cache_utils.py` & `dsp-ml-0.1.5/dsp/modules/cache_utils.py`

 * *Files identical despite different names*

### Comparing `dsp-ml-0.1.4/dsp/modules/colbertv2.py` & `dsp-ml-0.1.5/dsp/modules/colbertv2.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,46 +1,55 @@
 import functools
+from typing import Optional, Union, Any
 import requests
 
 from dsp.modules.cache_utils import CacheMemory, NotebookCacheMemory
 from dsp.utils import dotdict
 
 
 # TODO: Ideally, this takes the name of the index and looks up its port.
 
 
 class ColBERTv2:
-    def __init__(self, url='http://0.0.0.0', port=None, post_requests=False):
+    """Wrapper for the ColBERTv2 Retrieval."""
+
+    def __init__(
+        self,
+        url: str = "http://0.0.0.0",
+        port: Optional[Union[str, int]] = None,
+        post_requests: bool = False,
+    ):
         self.post_requests = post_requests
-        self.url = f'{url}:{port}' if port else url
+        self.url = f"{url}:{port}" if port else url
 
-    def __call__(self, query: str, k=10, simplify=False):
+    def __call__(
+        self, query: str, k: int = 10, simplify: bool = False
+    ) -> Union[list[str], list[dotdict]]:
         if self.post_requests:
-            topk = colbertv2_post_request(self.url, query, k)
+            topk: list[dict[str, Any]] = colbertv2_post_request(self.url, query, k)
         else:
-            topk = colbertv2_get_request(self.url, query, k)
-
-        topk = [dotdict(psg) for psg in topk]
+            topk: list[dict[str, Any]] = colbertv2_get_request(self.url, query, k)
 
         if simplify:
-            topk = [psg.long_text for psg in topk]
+            return [psg["long_text"] for psg in topk]
 
-        return topk
+        return [dotdict(psg) for psg in topk]
 
 
 @CacheMemory.cache
 def colbertv2_get_request_v2(url: str, query: str, k: int):
-    assert k <= 100, f'Only k <= 100 is supported for the hosted ColBERTv2 server at the moment.'
+    assert (
+        k <= 100
+    ), "Only k <= 100 is supported for the hosted ColBERTv2 server at the moment."
 
     payload = {"query": query, "k": k}
-    res = requests.get(url, params=payload)
-
-    topk = res.json()['topk'][:k]
-    topk = [{**d, 'long_text': d['text']} for d in topk]
+    res = requests.get(url, params=payload, timeout=10)
 
+    topk = res.json()["topk"][:k]
+    topk = [{**d, "long_text": d["text"]} for d in topk]
     return topk[:k]
 
 
 @functools.lru_cache(maxsize=None)
 @NotebookCacheMemory.cache
 def colbertv2_get_request_v2_wrapped(*args, **kwargs):
     return colbertv2_get_request_v2(*args, **kwargs)
@@ -49,17 +58,17 @@
 colbertv2_get_request = colbertv2_get_request_v2_wrapped
 
 
 @CacheMemory.cache
 def colbertv2_post_request_v2(url: str, query: str, k: int):
     headers = {"Content-Type": "application/json; charset=utf-8"}
     payload = {"query": query, "k": k}
-    res = requests.post(url, json=payload, headers=headers)
+    res = requests.post(url, json=payload, headers=headers, timeout=10)
 
-    return res.json()['topk'][:k]
+    return res.json()["topk"][:k]
 
 
 @functools.lru_cache(maxsize=None)
 @NotebookCacheMemory.cache
 def colbertv2_post_request_v2_wrapped(*args, **kwargs):
     return colbertv2_post_request_v2(*args, **kwargs)
```

### Comparing `dsp-ml-0.1.4/dsp/primitives/compiler.py` & `dsp-ml-0.1.5/dsp/primitives/compiler.py`

 * *Files identical despite different names*

### Comparing `dsp-ml-0.1.4/dsp/primitives/primitives.py` & `dsp-ml-0.1.5/dsp/primitives/primitives.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,9 @@
 import dsp
 import copy
-
 from functools import wraps
 
 # applied right to left (innermost first, like function calls)
 def compose_decorators(*decorators):
     def decorator(func):
         for decorator in decorators[::-1]:
             func = decorator(func)
```

### Comparing `dsp-ml-0.1.4/dsp/templates/template_v2.py` & `dsp-ml-0.1.5/dsp/templates/template_v2.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,49 +1,36 @@
 from collections import namedtuple
 import re
-
+from typing import Union, Any
 import dsp
+from dsp.primitives.demonstrate import Example
+from .utils import passages2text, format_answers
 
 Field = namedtuple("Field", "name separator input_variable output_variable description")
 
 # TODO: de-duplicate with dsp/templates/template.py
 
 
-def passages2text(passages):
-    if type(passages) is str:
-        return passages
-
-    assert type(passages) in [list, tuple]
-
-    if len(passages) == 1:
-        return f"«{passages[0]}»"
-
-    return "\n".join([f"[{idx+1}] «{txt}»" for idx, txt in enumerate(passages)])
-
-
-def format_answers(answers):
-    if isinstance(answers, list):
-        if len(answers) >= 1:
-            return str(answers[0]).strip()
-        elif len(answers) == 0:
-            raise ValueError(f"No answers found")
-    elif isinstance(answers, str):
-        return answers
-    else:
-        raise ValueError(f"Unable to parse answers of type {type(answers)}")
-
-
 class TemplateV2:
-    def __init__(self, template, format_handlers={"passages": passages2text, "context": passages2text, "answer": format_answers, "answers": format_answers}):
+    def __init__(
+        self,
+        template,
+        format_handlers={
+            "passages": passages2text,
+            "context": passages2text,
+            "answer": format_answers,
+            "answers": format_answers,
+        },
+    ):
         self.format_handlers = format_handlers
 
         template = template.strip()
 
         self.instructions = re.search("(.*)\n", template).group(1)
-        template = template[len(self.instructions):].strip()
+        template = template[len(self.instructions) :].strip()
 
         self.fields = []
         while len(template) > 0:
             match = re.search("(.*)(\s){(.*)}\s(.*\${.*})", template)
             if match is not None:
                 name = match.group(1)
                 separator = match.group(2)
@@ -73,18 +60,19 @@
                     separator=separator,
                     input_variable=input_variable,
                     output_variable=output_variable,
                     description=description,
                 )
             )
 
-            template = template[len(match.group(0)):].strip()
+            template = template[len(match.group(0)) :].strip()
 
-    def query(self, example, is_demo=False):
-        result = []
+    def query(self, example: Example, is_demo: bool = False) -> str:
+        """Retrieves the input variables from the example and formats them into a query string."""
+        result: list[str] = []
 
         if not is_demo:
             has_value = [
                 field.input_variable in example
                 and example[field.input_variable] is not None
                 and example[field.input_variable] != ""
                 for field in self.fields
@@ -92,121 +80,157 @@
 
             for i in range(1, len(has_value)):
                 if has_value[i - 1] and not any(has_value[i:]):
                     example[self.fields[i].input_variable] = ""
                     break
 
         for field in self.fields:
-            if (field.input_variable in example and example[field.input_variable] is not None):
+            if (
+                field.input_variable in example
+                and example[field.input_variable] is not None
+            ):
                 if field.input_variable in self.format_handlers:
                     format_handler = self.format_handlers[field.input_variable]
                 else:
-                    def format_handler(x): return ' '.join(x.split())
-                
-                result.append(f"{field.name}{field.separator}{format_handler(example[field.input_variable])}")
 
-        if self._has_augmented_guidelines() and ("augmented" in example and example.augmented):
+                    def format_handler(x):
+                        return " ".join(x.split())
+
+                result.append(
+                    f"{field.name}{field.separator}{format_handler(example[field.input_variable])}"
+                )
+
+        if self._has_augmented_guidelines() and (
+            "augmented" in example and example.augmented
+        ):
             return "\n\n".join(result)
-        else:
-            return "\n".join(result)
+        return "\n".join(result)
 
-    def guidelines(self, show_guidelines=True):
-        if (not show_guidelines) or (hasattr(dsp.settings, 'show_guidelines') and not dsp.settings.show_guidelines):
-            return ''
+    def guidelines(self, show_guidelines=True) -> str:
+        """Returns the task guidelines as described in the lm prompt"""
+        if (not show_guidelines) or (
+            hasattr(dsp.settings, "show_guidelines")
+            and not dsp.settings.show_guidelines
+        ):
+            return ""
 
         result = "Follow the following format.\n\n"
 
         example = dsp.Example()
         for field in self.fields:
             example[field.input_variable] = field.description
         example.augmented = self._has_augmented_guidelines()
 
         result += self.query(example)
         return result
 
     def _has_augmented_guidelines(self):
-        return len(self.fields) > 3 or any(field.separator == "\n" for field in self.fields)
-
-    def extract(self, example, raw_pred):
+        return len(self.fields) > 3 or any(
+            field.separator == "\n" for field in self.fields
+        )
+
+    def extract(
+        self, example: Union[Example, dict[str, Any]], raw_pred: str
+    ) -> Example:
+        """Extracts the answer from the LM raw prediction using the template structure
+
+        Args:
+            example (Union[Example, dict[str, Any]]): Contains the input variables that raw_pred was completed on.
+            raw_pred (str): LM generated string
+
+        Returns:
+            Example: The example with the output variables filled in
+        """
         example = dsp.Example(example)
 
         raw_pred = raw_pred.strip()
 
         idx = 0
         while idx < len(self.fields):
-            if (self.fields[idx].input_variable not in example or example[self.fields[idx].input_variable] is None):
+            if (
+                self.fields[idx].input_variable not in example
+                or example[self.fields[idx].input_variable] is None
+            ):
                 break
             idx += 1
-        
-        idx = min(idx, len(self.fields) - 1)
 
+        idx = min(idx, len(self.fields) - 1)
         while raw_pred != "" and idx < len(self.fields):
-            # print("HERE,", idx)
             if idx < len(self.fields) - 1:
-                next_field_name = '\n' + self.fields[idx + 1].name
+                next_field_name = "\n" + self.fields[idx + 1].name
                 offset = raw_pred.find(next_field_name)
-                # print(f"Looking for ```{next_field_name}```. Found it at {offset}")
 
                 if offset >= 0:
-                    example[self.fields[idx].output_variable] = raw_pred[:offset].strip()
-                    raw_pred = raw_pred[offset + len(next_field_name):].strip()
+                    example[self.fields[idx].output_variable] = raw_pred[
+                        :offset
+                    ].strip()
+                    raw_pred = raw_pred[offset + len(next_field_name) :].strip()
                     idx += 1
                 else:
                     example[self.fields[idx].output_variable] = raw_pred.strip()
                     raw_pred = ""
                     idx += 1
-                    # print("Exiting")
                     break
 
-            else: #if idx == len(self.fields) - 1:
+            else:
                 assert idx == len(self.fields) - 1, (idx, len(self.fields))
                 example[self.fields[idx].output_variable] = raw_pred.strip()
                 break
-                # offset = raw_pred.find(self.fields[idx].name)
-                # if offset < 0:
-                # else:
-                #     raw_pred = raw_pred[offset + len(self.fields[idx].name):].strip()
-                #     example[self.fields[idx].output_variable] = raw_pred
 
         return example
 
-    def __call__(self, example, show_guidelines=True):
+    def __call__(self, example, show_guidelines=True) -> str:
         example = dsp.Example(example)
 
+        # The training data should not contain the output variable
         if self.fields[-1].input_variable in example:
             del example[self.fields[-1].input_variable]
 
         rdemos = [
             self.query(demo, is_demo=True)
             for demo in example.demos
             if (
                 ("augmented" not in demo or not demo.augmented)
-                and (
+                and (  # validate that the training example has the same primitive input var as the template
                     self.fields[-1].input_variable in demo
                     and demo[self.fields[-1].input_variable] is not None
                 )
             )
         ]
+
         ademos = [
             self.query(demo, is_demo=True)
             for demo in example.demos
             if "augmented" in demo and demo.augmented
         ]
 
         long_query = self._has_augmented_guidelines()
         if long_query:
             example["augmented"] = True
         query = self.query(example)
-
         rdemos = "\n\n".join(rdemos)
         if len(rdemos) >= 1 and len(ademos) == 0 and not long_query:
             rdemos_and_query = "\n\n".join([rdemos, query])
-            parts = [self.instructions, self.guidelines(show_guidelines), rdemos_and_query]
+            parts = [
+                self.instructions,
+                self.guidelines(show_guidelines),
+                rdemos_and_query,
+            ]
         elif len(rdemos) == 0:
-            parts = [self.instructions, self.guidelines(show_guidelines), *ademos, query]
+            parts = [
+                self.instructions,
+                self.guidelines(show_guidelines),
+                *ademos,
+                query,
+            ]
         else:
-            parts = [self.instructions, rdemos,
-                     self.guidelines(show_guidelines), *ademos, query]
+            parts = [
+                self.instructions,
+                rdemos,
+                self.guidelines(show_guidelines),
+                *ademos,
+                query,
+            ]
 
         prompt = "\n\n---\n\n".join([p.strip() for p in parts if p])
 
         return prompt.strip()
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `dsp-ml-0.1.4/dsp/templates/template_v3.py` & `dsp-ml-0.1.5/dsp/templates/template_v3.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,32 +1,51 @@
+from typing import Callable
 from dsp.templates import TemplateV2, passages2text, format_answers, Field
 
+
 class Type:
-    def __init__(self, prefix, desc, format=None, aliases=[]) -> None:
+    """A primitive datatype that defines and represents a prompt label."""
+
+    def __init__(self, prefix: str, desc: str, format=None, aliases=[]) -> None:
         self.prefix = prefix
         self.desc = desc
         self.format = format
         self.aliases = aliases
 
-        assert aliases == [], "TODO: If aliases is used, handling of input_variable in V2 needs to be richer."
-    
+        assert (
+            aliases == []
+        ), "TODO: If aliases is used, handling of input_variable in V2 needs to be richer."
+
     def __call__(self, **kwargs):
         kwargs = {**self.__dict__, **kwargs}
         return Type(**kwargs)
 
+
 class Template(TemplateV2):
-    def __init__(self, instructions, **kwargs):
+    """A template datatype that represents the structure of communicate with the LM."""
+
+    def __init__(self, instructions: str, **kwargs):
         self.instructions = instructions
 
-        self.fields = []
-        self.format_handlers = {"context": passages2text, "answers": format_answers}
+        self.fields: list[Field] = []
+        self.format_handlers: dict[str, Callable] = {
+            "context": passages2text,
+            "answers": format_answers,
+        }
 
         for key, value in kwargs.items():
-            prefix = value.prefix
-            separator = ' ' if prefix.rstrip() == prefix else prefix[len(prefix.rstrip()):]
-            field = Field(name=prefix.strip(), description=value.desc,
-                          input_variable=key, output_variable=key, separator=separator)
+            prefix: str = value.prefix
+            separator: str = (
+                " " if prefix.rstrip() == prefix else prefix[len(prefix.rstrip()) :]
+            )
+            field = Field(
+                name=prefix.strip(),
+                description=value.desc,
+                input_variable=key,
+                output_variable=key,
+                separator=separator,
+            )
             self.fields.append(field)
 
             if value.format:
                 for name in [key, *value.aliases]:
                     self.format_handlers[name] = value.format
```

### Comparing `dsp-ml-0.1.4/dsp/utils/dpr.py` & `dsp-ml-0.1.5/dsp/utils/dpr.py`

 * *Files identical despite different names*

### Comparing `dsp-ml-0.1.4/dsp/utils/metrics.py` & `dsp-ml-0.1.5/dsp/utils/metrics.py`

 * *Files identical despite different names*

### Comparing `dsp-ml-0.1.4/dsp/utils/utils.py` & `dsp-ml-0.1.5/dsp/utils/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,75 +3,77 @@
 import datetime
 import itertools
 
 from collections import defaultdict
 
 
 def print_message(*s, condition=True, pad=False, sep=None):
-    s = ' '.join([str(x) for x in s])
+    s = " ".join([str(x) for x in s])
     msg = "[{}] {}".format(datetime.datetime.now().strftime("%b %d, %H:%M:%S"), s)
 
     if condition:
-        msg = msg if not pad else f'\n{msg}\n'
+        msg = msg if not pad else f"\n{msg}\n"
         print(msg, flush=True, sep=sep)
 
-
     return msg
 
 
 def timestamp(daydir=False):
     format_str = f"%Y-%m{'/' if daydir else '-'}%d{'/' if daydir else '_'}%H.%M.%S"
     result = datetime.datetime.now().strftime(format_str)
     return result
 
 
 def file_tqdm(file):
     print(f"#> Reading {file.name}")
 
-    with tqdm.tqdm(total=os.path.getsize(file.name) / 1024.0 / 1024.0, unit="MiB") as pbar:
+    with tqdm.tqdm(
+        total=os.path.getsize(file.name) / 1024.0 / 1024.0, unit="MiB"
+    ) as pbar:
         for line in file:
             yield line
             pbar.update(len(line) / 1024.0 / 1024.0)
 
         pbar.close()
 
 
 def create_directory(path):
     if os.path.exists(path):
-        print('\n')
-        print_message("#> Note: Output directory", path, 'already exists\n\n')
+        print("\n")
+        print_message("#> Note: Output directory", path, "already exists\n\n")
     else:
-        print('\n')
-        print_message("#> Creating directory", path, '\n\n')
+        print("\n")
+        print_message("#> Creating directory", path, "\n\n")
         os.makedirs(path)
 
 
-def deduplicate(seq):
+def deduplicate(seq: list[str]) -> list[str]:
     """
     Source: https://stackoverflow.com/a/480227/1493011
     """
 
     seen = set()
     return [x for x in seq if not (x in seen or seen.add(x))]
 
 
 def batch(group, bsize, provide_offset=False):
     offset = 0
     while offset < len(group):
-        L = group[offset: offset + bsize]
+        L = group[offset : offset + bsize]
         yield ((offset, L) if provide_offset else L)
         offset += len(L)
     return
 
 
 class dotdict(dict):
     """
     dot.notation access to dictionary attributes
     Credit: derek73 @ https://stackoverflow.com/questions/2352181
     """
+
     __getattr__ = dict.__getitem__
     __setattr__ = dict.__setitem__
     __delattr__ = dict.__delitem__
 
 
 class dotdict_lax(dict):
     __getattr__ = dict.get
@@ -115,17 +117,17 @@
 
     assert length in [None, len(L3)], "zip_first() failure: length differs!"
 
     return L3
 
 
 def int_or_float(val):
-    if '.' in val:
+    if "." in val:
         return float(val)
-        
+
     return int(val)
 
 
 def groupby_first_item(lst):
     groups = defaultdict(list)
 
     for first, *rest in lst:
@@ -133,28 +135,30 @@
         groups[first].append(rest)
 
     return groups
 
 
 def process_grouped_by_first_item(lst):
     """
-        Requires items in list to already be grouped by first item.
+    Requires items in list to already be grouped by first item.
     """
 
     groups = defaultdict(list)
 
     started = False
     last_group = None
 
     for first, *rest in lst:
         rest = rest[0] if len(rest) == 1 else rest
 
         if started and first != last_group:
             yield (last_group, groups[last_group])
-            assert first not in groups, f"{first} seen earlier --- violates precondition."
+            assert (
+                first not in groups
+            ), f"{first} seen earlier --- violates precondition."
 
         groups[first].append(rest)
 
         last_group = first
         started = True
 
     return groups
@@ -181,16 +185,18 @@
     return
 
 
 # see https://stackoverflow.com/a/45187287
 class NullContextManager(object):
     def __init__(self, dummy_resource=None):
         self.dummy_resource = dummy_resource
+
     def __enter__(self):
         return self.dummy_resource
+
     def __exit__(self, *args):
         pass
 
 
 def load_batch_backgrounds(args, qids):
     if args.qid2backgrounds is None:
         return None
@@ -199,13 +205,13 @@
 
     for qid in qids:
         back = args.qid2backgrounds[qid]
 
         if len(back) and type(back[0]) == int:
             x = [args.collection[pid] for pid in back]
         else:
-            x = [args.collectionX.get(pid, '') for pid in back]
+            x = [args.collectionX.get(pid, "") for pid in back]
 
-        x = ' [SEP] '.join(x)
+        x = " [SEP] ".join(x)
         qbackgrounds.append(x)
-    
+
     return qbackgrounds
```

### Comparing `dsp-ml-0.1.4/dsp_ml.egg-info/PKG-INFO` & `dsp-ml-0.1.5/dsp_ml.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,18 +1,17 @@
-Metadata-Version: 1.2
+Metadata-Version: 2.1
 Name: dsp-ml
-Version: 0.1.4
+Version: 0.1.5
 Summary: Demonstrate-Search-Predict
 Home-page: https://github.com/stanfordnlp/dsp
 Author: Omar Khattab
 Author-email: okhattab@stanford.edu
 License: MIT License
-Description: UNKNOWN
-Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: POSIX :: Linux
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
-Requires-Python: >=3.8
+Requires-Python: >=3.9
+License-File: LICENSE
```

### Comparing `dsp-ml-0.1.4/dsp_ml.egg-info/SOURCES.txt` & `dsp-ml-0.1.5/dsp_ml.egg-info/SOURCES.txt`

 * *Files 18% similar despite different names*

```diff
@@ -1,27 +1,37 @@
+LICENSE
 README.md
 setup.py
 dsp/__init__.py
 dsp/evaluation/__init__.py
 dsp/evaluation/utils.py
 dsp/modules/__init__.py
 dsp/modules/cache_utils.py
+dsp/modules/cohere.py
 dsp/modules/colbertv2.py
 dsp/modules/gpt3.py
+dsp/modules/hf.py
+dsp/modules/hf_client.py
+dsp/modules/hf_server.py
+dsp/modules/lm.py
+dsp/modules/sbert.py
+dsp/modules/sentence_vectorizer.py
 dsp/primitives/__init__.py
 dsp/primitives/compiler.py
 dsp/primitives/demonstrate.py
+dsp/primitives/inspect.py
 dsp/primitives/predict.py
 dsp/primitives/primitives.py
 dsp/primitives/search.py
 dsp/templates/__init__.py
 dsp/templates/template_v2.py
 dsp/templates/template_v3.py
 dsp/templates/utils.py
 dsp/utils/__init__.py
+dsp/utils/ann_utils.py
 dsp/utils/dpr.py
 dsp/utils/metrics.py
 dsp/utils/settings.py
 dsp/utils/utils.py
 dsp_ml.egg-info/PKG-INFO
 dsp_ml.egg-info/SOURCES.txt
 dsp_ml.egg-info/dependency_links.txt
```

### Comparing `dsp-ml-0.1.4/setup.py` & `dsp-ml-0.1.5/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 from setuptools import setup, find_packages
 
 setup(
     name="dsp-ml",
-    version="0.1.4",
+    version="0.1.5",
     description="Demonstrate-Search-Predict",
     url="https://github.com/stanfordnlp/dsp",
     author="Omar Khattab",
     author_email="okhattab@stanford.edu",
     license="MIT License",
     packages=find_packages(),
-    python_requires='>=3.8',
+    python_requires='>=3.9',
     install_requires=[
         "backoff",
         "joblib",
         "jupyter",
         "openai",
         "pandas",
         "spacy",
```

