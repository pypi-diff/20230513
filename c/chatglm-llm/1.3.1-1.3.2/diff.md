# Comparing `tmp/chatglm-llm-1.3.1.tar.gz` & `tmp/chatglm-llm-1.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chatglm-llm-1.3.1.tar", last modified: Wed May 10 13:52:13 2023, max compression
+gzip compressed data, was "chatglm-llm-1.3.2.tar", last modified: Sat May 13 02:18:11 2023, max compression
```

## Comparing `chatglm-llm-1.3.1.tar` & `chatglm-llm-1.3.2.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxr-xr-x   0 dr         (501) staff       (20)        0 2023-05-10 13:52:13.906891 chatglm-llm-1.3.1/
--rw-r--r--   0 dr         (501) staff       (20)       36 2023-05-09 13:18:22.000000 chatglm-llm-1.3.1/MANIFEST.in
--rw-r--r--   0 dr         (501) staff       (20)      184 2023-05-10 13:52:13.906559 chatglm-llm-1.3.1/PKG-INFO
--rw-r--r--   0 dr         (501) staff       (20)     1887 2023-05-03 14:04:42.000000 chatglm-llm-1.3.1/README.md
-drwxr-xr-x   0 dr         (501) staff       (20)        0 2023-05-10 13:52:13.903046 chatglm-llm-1.3.1/chatglm_llm.egg-info/
--rw-r--r--   0 dr         (501) staff       (20)      184 2023-05-10 13:52:13.000000 chatglm-llm-1.3.1/chatglm_llm.egg-info/PKG-INFO
--rw-r--r--   0 dr         (501) staff       (20)      480 2023-05-10 13:52:13.000000 chatglm-llm-1.3.1/chatglm_llm.egg-info/SOURCES.txt
--rw-r--r--   0 dr         (501) staff       (20)        1 2023-05-10 13:52:13.000000 chatglm-llm-1.3.1/chatglm_llm.egg-info/dependency_links.txt
--rw-r--r--   0 dr         (501) staff       (20)       53 2023-05-10 13:52:13.000000 chatglm-llm-1.3.1/chatglm_llm.egg-info/entry_points.txt
--rw-r--r--   0 dr         (501) staff       (20)        1 2023-05-09 12:57:36.000000 chatglm-llm-1.3.1/chatglm_llm.egg-info/not-zip-safe
--rw-r--r--   0 dr         (501) staff       (20)      226 2023-05-10 13:52:13.000000 chatglm-llm-1.3.1/chatglm_llm.egg-info/requires.txt
--rw-r--r--   0 dr         (501) staff       (20)       12 2023-05-10 13:52:13.000000 chatglm-llm-1.3.1/chatglm_llm.egg-info/top_level.txt
-drwxr-xr-x   0 dr         (501) staff       (20)        0 2023-05-10 13:52:13.904756 chatglm-llm-1.3.1/chatglm_src/
--rw-r--r--   0 dr         (501) staff       (20)      680 2023-05-10 13:38:04.000000 chatglm-llm-1.3.1/chatglm_src/__init__.py
--rw-r--r--   0 dr         (501) staff       (20)     3963 2023-05-09 12:56:40.000000 chatglm-llm-1.3.1/chatglm_src/callbacks.py
-drwxr-xr-x   0 dr         (501) staff       (20)        0 2023-05-10 13:52:13.905663 chatglm-llm-1.3.1/chatglm_src/chains/
--rw-r--r--   0 dr         (501) staff       (20)       69 2023-05-09 13:28:08.000000 chatglm-llm-1.3.1/chatglm_src/chains/__init__.py
--rw-r--r--   0 dr         (501) staff       (20)     4402 2023-05-10 13:43:12.000000 chatglm-llm-1.3.1/chatglm_src/chains/local_qa.py
--rw-r--r--   0 dr         (501) staff       (20)      443 2023-05-03 12:45:54.000000 chatglm-llm-1.3.1/chatglm_src/cmd.py
--rw-r--r--   0 dr         (501) staff       (20)     3058 2023-05-10 12:51:59.000000 chatglm-llm-1.3.1/chatglm_src/embeding.py
--rw-r--r--   0 dr         (501) staff       (20)    23800 2023-05-10 13:22:51.000000 chatglm-llm-1.3.1/chatglm_src/llm.py
-drwxr-xr-x   0 dr         (501) staff       (20)        0 2023-05-10 13:52:13.906095 chatglm-llm-1.3.1/chatglm_src/loader/
--rw-r--r--   0 dr         (501) staff       (20)     1403 2023-05-10 13:44:53.000000 chatglm-llm-1.3.1/chatglm_src/loader/__init__.py
--rw-r--r--   0 dr         (501) staff       (20)       38 2023-05-10 13:52:13.906993 chatglm-llm-1.3.1/setup.cfg
--rw-r--r--   0 dr         (501) staff       (20)      997 2023-05-10 13:50:50.000000 chatglm-llm-1.3.1/setup.py
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.633467 chatglm-llm-1.3.2/
+-rw-r--r--   0 mroy       (501) staff       (20)       36 2023-05-10 01:48:15.000000 chatglm-llm-1.3.2/MANIFEST.in
+-rw-r--r--   0 mroy       (501) staff       (20)      212 2023-05-13 02:18:11.633355 chatglm-llm-1.3.2/PKG-INFO
+-rw-r--r--   0 mroy       (501) staff       (20)     1887 2023-05-04 01:08:28.000000 chatglm-llm-1.3.2/README.md
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.631428 chatglm-llm-1.3.2/chatglm_llm.egg-info/
+-rw-r--r--   0 mroy       (501) staff       (20)      212 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/PKG-INFO
+-rw-r--r--   0 mroy       (501) staff       (20)      480 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/SOURCES.txt
+-rw-r--r--   0 mroy       (501) staff       (20)        1 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/dependency_links.txt
+-rw-r--r--   0 mroy       (501) staff       (20)       53 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/entry_points.txt
+-rw-r--r--   0 mroy       (501) staff       (20)        1 2023-05-04 01:12:10.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/not-zip-safe
+-rw-r--r--   0 mroy       (501) staff       (20)      226 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/requires.txt
+-rw-r--r--   0 mroy       (501) staff       (20)       12 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/top_level.txt
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.632366 chatglm-llm-1.3.2/chatglm_src/
+-rw-r--r--   0 mroy       (501) staff       (20)      680 2023-05-11 01:28:05.000000 chatglm-llm-1.3.2/chatglm_src/__init__.py
+-rw-r--r--   0 mroy       (501) staff       (20)     4079 2023-05-13 01:46:04.000000 chatglm-llm-1.3.2/chatglm_src/callbacks.py
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.632784 chatglm-llm-1.3.2/chatglm_src/chains/
+-rw-r--r--   0 mroy       (501) staff       (20)       69 2023-05-10 01:48:15.000000 chatglm-llm-1.3.2/chatglm_src/chains/__init__.py
+-rw-r--r--   0 mroy       (501) staff       (20)     4402 2023-05-11 09:17:21.000000 chatglm-llm-1.3.2/chatglm_src/chains/local_qa.py
+-rw-r--r--   0 mroy       (501) staff       (20)      443 2023-05-04 01:08:28.000000 chatglm-llm-1.3.2/chatglm_src/cmd.py
+-rw-r--r--   0 mroy       (501) staff       (20)     3052 2023-05-11 09:34:29.000000 chatglm-llm-1.3.2/chatglm_src/embeding.py
+-rw-r--r--   0 mroy       (501) staff       (20)    23753 2023-05-13 01:50:42.000000 chatglm-llm-1.3.2/chatglm_src/llm.py
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.633069 chatglm-llm-1.3.2/chatglm_src/loader/
+-rw-r--r--   0 mroy       (501) staff       (20)     1403 2023-05-11 01:28:05.000000 chatglm-llm-1.3.2/chatglm_src/loader/__init__.py
+-rw-r--r--   0 mroy       (501) staff       (20)       38 2023-05-13 02:18:11.633510 chatglm-llm-1.3.2/setup.cfg
+-rw-r--r--   0 mroy       (501) staff       (20)      997 2023-05-13 01:46:10.000000 chatglm-llm-1.3.2/setup.py
```

### Comparing `chatglm-llm-1.3.1/README.md` & `chatglm-llm-1.3.2/README.md`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.1/chatglm_src/__init__.py` & `chatglm-llm-1.3.2/chatglm_src/__init__.py`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.1/chatglm_src/callbacks.py` & `chatglm-llm-1.3.2/chatglm_src/callbacks.py`

 * *Files 5% similar despite different names*

```diff
@@ -2,16 +2,21 @@
 import re
 import langchain
 from langchain.callbacks.base import AsyncCallbackHandler, BaseCallbackHandler
 from langchain.llms.base import LLMResult
 from langchain.prompts import PromptTemplate
 from typing import Any, Coroutine, Dict, List
 from termcolor import colored
+try:
+    from langchain.callbacks.base import AsyncCallbackManager
+except:
+    from langchain.callbacks.manager import AsyncCallbackManager
 
-class AsyncWebSocksetCallbackManager(langchain.callbacks.base.AsyncCallbackManager):
+
+class AsyncWebSocksetCallbackManager(AsyncCallbackManager):
     online_histories = {}
     user_id_websocket = {}
     async def on_llm_start(self, prompt: str,prompts: List[str], **kwargs: Any) -> Any:
         await super().on_llm_start(prompt, prompts, **kwargs)
         if "(history_id:" in prompt:
             
             history_id = self.extract_history_id_from_prompt(prompt)
```

### Comparing `chatglm-llm-1.3.1/chatglm_src/chains/local_qa.py` & `chatglm-llm-1.3.2/chatglm_src/chains/local_qa.py`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.1/chatglm_src/embeding.py` & `chatglm-llm-1.3.2/chatglm_src/embeding.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,16 +21,16 @@
         if remote_host is None:
             self._emb = HuggingFaceEmbeddings(model_name=model_path)
         else:
             self.remote_host = remote_host
 
     def send_and_recv(self, data, ws):
         try:
-            for i in tqdm.tqdm(range(0, len(data), 1024*1024*2), desc="sending data"):
-                ws.send(data[i:i+1024*1024*2])
+            for i in tqdm.tqdm(range(0, len(data), 1024*102), desc="sending data"):
+                ws.send(data[i:i+1024*102])
             ws.send("[STOP]")
             message = ""
             total = int(ws.recv())
             bar = tqdm.tqdm(desc="receiving data", total=total)
             while 1:
                 res = ws.recv()
                 message += res
```

### Comparing `chatglm-llm-1.3.1/chatglm_src/llm.py` & `chatglm-llm-1.3.2/chatglm_src/llm.py`

 * *Files 1% similar despite different names*

```diff
@@ -159,26 +159,26 @@
 
     """
     max_token: int = 10000
     temperature: float = 0.01
     top_p = 0.9
     history = []
     history_id = "default"
-    tokenizer: object = None
-    model: object = None
+    tokenizer: Any = None
+    model: Any = None
     history_len: int = 10
-    model: object = None
-    tokenizer: object = None
+    model: Any = None
+    tokenizer: Any = None
     model_path: str = pathlib.Path.home() / ".cache" / "chatglm"
     cpu: bool = False
     streaming: bool = False
     verbose: bool = False
-    callbacks  = [StreamingStdOutCallbackHandler(), AsyncWebsocketHandler()]
-    callback_manager: langchain.callbacks.base.BaseCallbackManager = None
-    remote_host: str = None
+    callbacks :Any  = [StreamingStdOutCallbackHandler(), AsyncWebsocketHandler()]
+    callback_manager:  Any = None
+    remote_host: Any = None
 
 
     @classmethod
     def load(cls, *args, model_path: str = None, **kargs):
         """
         Load a model from local or remote
         if want to use stream mode:
```

### Comparing `chatglm-llm-1.3.1/chatglm_src/loader/__init__.py` & `chatglm-llm-1.3.2/chatglm_src/loader/__init__.py`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.1/setup.py` & `chatglm-llm-1.3.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 
 from setuptools import setup, find_packages
 
 
 setup(name='chatglm-llm',
-    version='1.3.1',
+    version='1.3.2',
     description='chatglm llm',
     url='https://github.com/xxx',
     author='auth',
     author_email='xxx@gmail.com',
     license='MIT',
     include_package_data=True,
     zip_safe=False,
```

