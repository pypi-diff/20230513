# Comparing `tmp/pyllms-0.2.1.tar.gz` & `tmp/pyllms-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyllms-0.2.1.tar", last modified: Sun May  7 04:01:34 2023, max compression
+gzip compressed data, was "pyllms-0.2.2.tar", last modified: Sat May 13 02:07:11 2023, max compression
```

## Comparing `pyllms-0.2.1.tar` & `pyllms-0.2.2.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 prelovac   (502) staff       (20)        0 2023-05-07 04:01:34.472844 pyllms-0.2.1/
--rw-r--r--   0 prelovac   (502) staff       (20)     1068 2023-04-10 01:29:26.000000 pyllms-0.2.1/LICENSE
--rw-r--r--   0 prelovac   (502) staff       (20)    16541 2023-05-07 04:01:34.472571 pyllms-0.2.1/PKG-INFO
--rw-r--r--   0 prelovac   (502) staff       (20)    15228 2023-04-29 05:43:17.000000 pyllms-0.2.1/README.md
-drwxr-xr-x   0 prelovac   (502) staff       (20)        0 2023-05-07 04:01:34.468803 pyllms-0.2.1/llms/
--rw-r--r--   0 prelovac   (502) staff       (20)      295 2023-04-13 02:24:28.000000 pyllms-0.2.1/llms/__init__.py
--rw-r--r--   0 prelovac   (502) staff       (20)    18384 2023-05-07 04:00:58.000000 pyllms-0.2.1/llms/llms.py
-drwxr-xr-x   0 prelovac   (502) staff       (20)        0 2023-05-07 04:01:34.470981 pyllms-0.2.1/llms/providers/
--rw-r--r--   0 prelovac   (502) staff       (20)      228 2023-04-23 02:39:46.000000 pyllms-0.2.1/llms/providers/__init__.py
--rw-r--r--   0 prelovac   (502) staff       (20)     2159 2023-05-07 04:00:58.000000 pyllms-0.2.1/llms/providers/ai21.py
--rw-r--r--   0 prelovac   (502) staff       (20)     3769 2023-05-07 04:00:58.000000 pyllms-0.2.1/llms/providers/aleph.py
--rw-r--r--   0 prelovac   (502) staff       (20)     9105 2023-05-07 04:00:58.000000 pyllms-0.2.1/llms/providers/anthropic.py
--rw-r--r--   0 prelovac   (502) staff       (20)     1565 2023-05-07 04:00:58.000000 pyllms-0.2.1/llms/providers/base_provider.py
--rw-r--r--   0 prelovac   (502) staff       (20)     4701 2023-05-07 04:00:58.000000 pyllms-0.2.1/llms/providers/cohere.py
--rw-r--r--   0 prelovac   (502) staff       (20)     2989 2023-05-07 04:00:58.000000 pyllms-0.2.1/llms/providers/huggingface.py
--rw-r--r--   0 prelovac   (502) staff       (20)     7943 2023-05-07 04:00:58.000000 pyllms-0.2.1/llms/providers/openai.py
-drwxr-xr-x   0 prelovac   (502) staff       (20)        0 2023-05-07 04:01:34.472242 pyllms-0.2.1/pyllms.egg-info/
--rw-r--r--   0 prelovac   (502) staff       (20)    16541 2023-05-07 04:01:34.000000 pyllms-0.2.1/pyllms.egg-info/PKG-INFO
--rw-r--r--   0 prelovac   (502) staff       (20)      419 2023-05-07 04:01:34.000000 pyllms-0.2.1/pyllms.egg-info/SOURCES.txt
--rw-r--r--   0 prelovac   (502) staff       (20)        1 2023-05-07 04:01:34.000000 pyllms-0.2.1/pyllms.egg-info/dependency_links.txt
--rw-r--r--   0 prelovac   (502) staff       (20)       85 2023-05-07 04:01:34.000000 pyllms-0.2.1/pyllms.egg-info/requires.txt
--rw-r--r--   0 prelovac   (502) staff       (20)        5 2023-05-07 04:01:34.000000 pyllms-0.2.1/pyllms.egg-info/top_level.txt
--rw-r--r--   0 prelovac   (502) staff       (20)       38 2023-05-07 04:01:34.472913 pyllms-0.2.1/setup.cfg
--rw-r--r--   0 prelovac   (502) staff       (20)     1882 2023-05-07 04:01:09.000000 pyllms-0.2.1/setup.py
+drwxr-xr-x   0 prelovac   (502) staff       (20)        0 2023-05-13 02:07:11.011228 pyllms-0.2.2/
+-rw-r--r--   0 prelovac   (502) staff       (20)     1068 2023-04-10 01:29:26.000000 pyllms-0.2.2/LICENSE
+-rw-r--r--   0 prelovac   (502) staff       (20)    16541 2023-05-13 02:07:11.010860 pyllms-0.2.2/PKG-INFO
+-rw-r--r--   0 prelovac   (502) staff       (20)    15228 2023-04-29 05:43:17.000000 pyllms-0.2.2/README.md
+drwxr-xr-x   0 prelovac   (502) staff       (20)        0 2023-05-13 02:07:11.006742 pyllms-0.2.2/llms/
+-rw-r--r--   0 prelovac   (502) staff       (20)      295 2023-04-13 02:24:28.000000 pyllms-0.2.2/llms/__init__.py
+-rw-r--r--   0 prelovac   (502) staff       (20)    18384 2023-05-07 04:00:58.000000 pyllms-0.2.2/llms/llms.py
+drwxr-xr-x   0 prelovac   (502) staff       (20)        0 2023-05-13 02:07:11.009199 pyllms-0.2.2/llms/providers/
+-rw-r--r--   0 prelovac   (502) staff       (20)      228 2023-04-23 02:39:46.000000 pyllms-0.2.2/llms/providers/__init__.py
+-rw-r--r--   0 prelovac   (502) staff       (20)     2159 2023-05-07 04:00:58.000000 pyllms-0.2.2/llms/providers/ai21.py
+-rw-r--r--   0 prelovac   (502) staff       (20)     3769 2023-05-07 04:00:58.000000 pyllms-0.2.2/llms/providers/aleph.py
+-rw-r--r--   0 prelovac   (502) staff       (20)     9195 2023-05-13 01:46:47.000000 pyllms-0.2.2/llms/providers/anthropic.py
+-rw-r--r--   0 prelovac   (502) staff       (20)     1565 2023-05-07 04:00:58.000000 pyllms-0.2.2/llms/providers/base_provider.py
+-rw-r--r--   0 prelovac   (502) staff       (20)     4701 2023-05-07 04:00:58.000000 pyllms-0.2.2/llms/providers/cohere.py
+-rw-r--r--   0 prelovac   (502) staff       (20)     3517 2023-05-13 02:04:37.000000 pyllms-0.2.2/llms/providers/huggingface.py
+-rw-r--r--   0 prelovac   (502) staff       (20)     7943 2023-05-07 04:00:58.000000 pyllms-0.2.2/llms/providers/openai.py
+drwxr-xr-x   0 prelovac   (502) staff       (20)        0 2023-05-13 02:07:11.010495 pyllms-0.2.2/pyllms.egg-info/
+-rw-r--r--   0 prelovac   (502) staff       (20)    16541 2023-05-13 02:07:10.000000 pyllms-0.2.2/pyllms.egg-info/PKG-INFO
+-rw-r--r--   0 prelovac   (502) staff       (20)      419 2023-05-13 02:07:11.000000 pyllms-0.2.2/pyllms.egg-info/SOURCES.txt
+-rw-r--r--   0 prelovac   (502) staff       (20)        1 2023-05-13 02:07:10.000000 pyllms-0.2.2/pyllms.egg-info/dependency_links.txt
+-rw-r--r--   0 prelovac   (502) staff       (20)      109 2023-05-13 02:07:10.000000 pyllms-0.2.2/pyllms.egg-info/requires.txt
+-rw-r--r--   0 prelovac   (502) staff       (20)        5 2023-05-13 02:07:10.000000 pyllms-0.2.2/pyllms.egg-info/top_level.txt
+-rw-r--r--   0 prelovac   (502) staff       (20)       38 2023-05-13 02:07:11.011315 pyllms-0.2.2/setup.cfg
+-rw-r--r--   0 prelovac   (502) staff       (20)     1917 2023-05-13 02:06:48.000000 pyllms-0.2.2/setup.py
```

### Comparing `pyllms-0.2.1/LICENSE` & `pyllms-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `pyllms-0.2.1/PKG-INFO` & `pyllms-0.2.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyllms
-Version: 0.2.1
+Version: 0.2.2
 Summary: Minimal Python library to connect to LLMs (OpenAI, Anthropic, AI21, Cohere, Aleph-Alpha, HuggingfaceHub), with a built-in model performance benchmark.
 Author: Vladimir Prelovac
 Author-email: vlad@kagi.com
 Project-URL: Documentation, https://github.com/kagisearch/pyllms
 Project-URL: Source Code, https://github.com/kagisearch/pyllms
 Project-URL: Issue Tracker, https://github.com/kagisearch/pyllms/issues
 Keywords: llm,llms,large language model,AI,NLP,natural language processing,gpt,chatgpt,openai,anthropic,ai21,cohere,aleph alpha,huggingface hub
```

### Comparing `pyllms-0.2.1/README.md` & `pyllms-0.2.2/README.md`

 * *Files identical despite different names*

### Comparing `pyllms-0.2.1/llms/llms.py` & `pyllms-0.2.2/llms/llms.py`

 * *Files identical despite different names*

### Comparing `pyllms-0.2.1/llms/providers/ai21.py` & `pyllms-0.2.2/llms/providers/ai21.py`

 * *Files identical despite different names*

### Comparing `pyllms-0.2.1/llms/providers/aleph.py` & `pyllms-0.2.2/llms/providers/aleph.py`

 * *Files identical despite different names*

### Comparing `pyllms-0.2.1/llms/providers/anthropic.py` & `pyllms-0.2.2/llms/providers/anthropic.py`

 * *Files 1% similar despite different names*

```diff
@@ -57,14 +57,15 @@
             "/v1/complete",
             **kwargs
         )
 
 
 class AnthropicProvider(BaseProvider):
     MODEL_INFO = {
+        "claude-instant-v1.1": {"prompt": 1.63, "completion": 5.51, "token_limit": 9000},
         "claude-instant-v1": {"prompt": 1.63, "completion": 5.51, "token_limit": 9000},
         "claude-v1": {"prompt": 11.02, "completion": 32.68, "token_limit": 9000},
     }
 
     def __init__(self, api_key=None, model=None):
         if model is None:
             model = list(self.MODEL_INFO.keys())[0]
```

### Comparing `pyllms-0.2.1/llms/providers/base_provider.py` & `pyllms-0.2.2/llms/providers/base_provider.py`

 * *Files identical despite different names*

### Comparing `pyllms-0.2.1/llms/providers/cohere.py` & `pyllms-0.2.2/llms/providers/cohere.py`

 * *Files identical despite different names*

### Comparing `pyllms-0.2.1/llms/providers/huggingface.py` & `pyllms-0.2.2/llms/providers/huggingface.py`

 * *Files 17% similar despite different names*

```diff
@@ -11,14 +11,33 @@
     MODEL_INFO = {
         "hf_pythia": {
             "full": "OpenAssistant/oasst-sft-4-pythia-12b-epoch-3.5",
             "prompt": 0,
             "completion": 0,
             "token_limit": 2048,
         },
+        "hf_mptinstruct": {
+            "full": "mosaicml/mpt-7b-instruct",
+            "prompt": 0,
+            "completion": 0,
+            "token_limit": 2048,
+        },
+        "hf_mptchat": {
+            "full": "mosaicml/mpt-7b-chat",
+            "prompt": 0,
+            "completion": 0,
+            "token_limit": 2048,
+        },
+        "hf_llava": {
+            "full": "liuhaotian/LLaVA-Lightning-MPT-7B-preview",
+            "prompt": 0,
+            "completion": 0,
+            "token_limit": 2048,
+        },
+
         "hf_dolly": {
             "full": "databricks/dolly-v2-12b",
             "prompt": 0,
             "completion": 0,
             "token_limit": -1,
         },
     }
@@ -63,15 +82,15 @@
     ):
         prompt, params = self._prepare_model_input(
             prompt=prompt,
             temperature=temperature,
             max_tokens=max_tokens,
             **kwargs,
         )
-        with self.track_latency as latency:
+        with self.track_latency() as latency:
             response = self.client(inputs=prompt, params=params)
 
         if "error" in response:
             print("Error: ", response["error"])
             return {}
 
         completion = response[0]["generated_text"][len(prompt) :]
```

### Comparing `pyllms-0.2.1/llms/providers/openai.py` & `pyllms-0.2.2/llms/providers/openai.py`

 * *Files identical despite different names*

### Comparing `pyllms-0.2.1/pyllms.egg-info/PKG-INFO` & `pyllms-0.2.2/pyllms.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyllms
-Version: 0.2.1
+Version: 0.2.2
 Summary: Minimal Python library to connect to LLMs (OpenAI, Anthropic, AI21, Cohere, Aleph-Alpha, HuggingfaceHub), with a built-in model performance benchmark.
 Author: Vladimir Prelovac
 Author-email: vlad@kagi.com
 Project-URL: Documentation, https://github.com/kagisearch/pyllms
 Project-URL: Source Code, https://github.com/kagisearch/pyllms
 Project-URL: Issue Tracker, https://github.com/kagisearch/pyllms/issues
 Keywords: llm,llms,large language model,AI,NLP,natural language processing,gpt,chatgpt,openai,anthropic,ai21,cohere,aleph alpha,huggingface hub
```

### Comparing `pyllms-0.2.1/setup.py` & `pyllms-0.2.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -5,29 +5,30 @@
 here = pathlib.Path(__file__).parent.resolve()
 long_description = (here / "README.md").read_text(encoding="utf-8")
 
 _project_homepage = "https://github.com/kagisearch/pyllms"
 
 setup(
     name="pyllms",
-    version="0.2.1",
+    version="0.2.2",
     description="Minimal Python library to connect to LLMs (OpenAI, Anthropic, AI21, Cohere, Aleph-Alpha, HuggingfaceHub), with a built-in model performance benchmark.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     author="Vladimir Prelovac",
     author_email="vlad@kagi.com",
     packages=find_packages(),
     install_requires=[
         "openai",
         "tiktoken",
         "anthropic",
         "ai21",
         "cohere",
         "aleph-alpha-client",
         "huggingface_hub",
+        "google-cloud-aiplatform",
         "prettytable",
     ],
     classifiers=[
         "Development Status :: 3 - Alpha",
         "Intended Audience :: Developers",
         "License :: OSI Approved :: MIT License",
         "Programming Language :: Python :: 3",
```

