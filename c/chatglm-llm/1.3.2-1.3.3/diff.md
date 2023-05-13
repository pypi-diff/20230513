# Comparing `tmp/chatglm-llm-1.3.2.tar.gz` & `tmp/chatglm-llm-1.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chatglm-llm-1.3.2.tar", last modified: Sat May 13 02:18:11 2023, max compression
+gzip compressed data, was "chatglm-llm-1.3.3.tar", last modified: Sat May 13 03:02:37 2023, max compression
```

## Comparing `chatglm-llm-1.3.2.tar` & `chatglm-llm-1.3.3.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.633467 chatglm-llm-1.3.2/
--rw-r--r--   0 mroy       (501) staff       (20)       36 2023-05-10 01:48:15.000000 chatglm-llm-1.3.2/MANIFEST.in
--rw-r--r--   0 mroy       (501) staff       (20)      212 2023-05-13 02:18:11.633355 chatglm-llm-1.3.2/PKG-INFO
--rw-r--r--   0 mroy       (501) staff       (20)     1887 2023-05-04 01:08:28.000000 chatglm-llm-1.3.2/README.md
-drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.631428 chatglm-llm-1.3.2/chatglm_llm.egg-info/
--rw-r--r--   0 mroy       (501) staff       (20)      212 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/PKG-INFO
--rw-r--r--   0 mroy       (501) staff       (20)      480 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/SOURCES.txt
--rw-r--r--   0 mroy       (501) staff       (20)        1 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/dependency_links.txt
--rw-r--r--   0 mroy       (501) staff       (20)       53 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/entry_points.txt
--rw-r--r--   0 mroy       (501) staff       (20)        1 2023-05-04 01:12:10.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/not-zip-safe
--rw-r--r--   0 mroy       (501) staff       (20)      226 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/requires.txt
--rw-r--r--   0 mroy       (501) staff       (20)       12 2023-05-13 02:18:11.000000 chatglm-llm-1.3.2/chatglm_llm.egg-info/top_level.txt
-drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.632366 chatglm-llm-1.3.2/chatglm_src/
--rw-r--r--   0 mroy       (501) staff       (20)      680 2023-05-11 01:28:05.000000 chatglm-llm-1.3.2/chatglm_src/__init__.py
--rw-r--r--   0 mroy       (501) staff       (20)     4079 2023-05-13 01:46:04.000000 chatglm-llm-1.3.2/chatglm_src/callbacks.py
-drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.632784 chatglm-llm-1.3.2/chatglm_src/chains/
--rw-r--r--   0 mroy       (501) staff       (20)       69 2023-05-10 01:48:15.000000 chatglm-llm-1.3.2/chatglm_src/chains/__init__.py
--rw-r--r--   0 mroy       (501) staff       (20)     4402 2023-05-11 09:17:21.000000 chatglm-llm-1.3.2/chatglm_src/chains/local_qa.py
--rw-r--r--   0 mroy       (501) staff       (20)      443 2023-05-04 01:08:28.000000 chatglm-llm-1.3.2/chatglm_src/cmd.py
--rw-r--r--   0 mroy       (501) staff       (20)     3052 2023-05-11 09:34:29.000000 chatglm-llm-1.3.2/chatglm_src/embeding.py
--rw-r--r--   0 mroy       (501) staff       (20)    23753 2023-05-13 01:50:42.000000 chatglm-llm-1.3.2/chatglm_src/llm.py
-drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 02:18:11.633069 chatglm-llm-1.3.2/chatglm_src/loader/
--rw-r--r--   0 mroy       (501) staff       (20)     1403 2023-05-11 01:28:05.000000 chatglm-llm-1.3.2/chatglm_src/loader/__init__.py
--rw-r--r--   0 mroy       (501) staff       (20)       38 2023-05-13 02:18:11.633510 chatglm-llm-1.3.2/setup.cfg
--rw-r--r--   0 mroy       (501) staff       (20)      997 2023-05-13 01:46:10.000000 chatglm-llm-1.3.2/setup.py
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 03:02:37.077184 chatglm-llm-1.3.3/
+-rw-r--r--   0 mroy       (501) staff       (20)       36 2023-05-10 01:48:15.000000 chatglm-llm-1.3.3/MANIFEST.in
+-rw-r--r--   0 mroy       (501) staff       (20)      212 2023-05-13 03:02:37.077062 chatglm-llm-1.3.3/PKG-INFO
+-rw-r--r--   0 mroy       (501) staff       (20)     1887 2023-05-04 01:08:28.000000 chatglm-llm-1.3.3/README.md
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 03:02:37.075524 chatglm-llm-1.3.3/chatglm_llm.egg-info/
+-rw-r--r--   0 mroy       (501) staff       (20)      212 2023-05-13 03:02:36.000000 chatglm-llm-1.3.3/chatglm_llm.egg-info/PKG-INFO
+-rw-r--r--   0 mroy       (501) staff       (20)      480 2023-05-13 03:02:37.000000 chatglm-llm-1.3.3/chatglm_llm.egg-info/SOURCES.txt
+-rw-r--r--   0 mroy       (501) staff       (20)        1 2023-05-13 03:02:36.000000 chatglm-llm-1.3.3/chatglm_llm.egg-info/dependency_links.txt
+-rw-r--r--   0 mroy       (501) staff       (20)       53 2023-05-13 03:02:36.000000 chatglm-llm-1.3.3/chatglm_llm.egg-info/entry_points.txt
+-rw-r--r--   0 mroy       (501) staff       (20)        1 2023-05-04 01:12:10.000000 chatglm-llm-1.3.3/chatglm_llm.egg-info/not-zip-safe
+-rw-r--r--   0 mroy       (501) staff       (20)      226 2023-05-13 03:02:36.000000 chatglm-llm-1.3.3/chatglm_llm.egg-info/requires.txt
+-rw-r--r--   0 mroy       (501) staff       (20)       12 2023-05-13 03:02:37.000000 chatglm-llm-1.3.3/chatglm_llm.egg-info/top_level.txt
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 03:02:37.076190 chatglm-llm-1.3.3/chatglm_src/
+-rw-r--r--   0 mroy       (501) staff       (20)      680 2023-05-11 01:28:05.000000 chatglm-llm-1.3.3/chatglm_src/__init__.py
+-rw-r--r--   0 mroy       (501) staff       (20)     4201 2023-05-13 02:36:58.000000 chatglm-llm-1.3.3/chatglm_src/callbacks.py
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 03:02:37.076759 chatglm-llm-1.3.3/chatglm_src/chains/
+-rw-r--r--   0 mroy       (501) staff       (20)       69 2023-05-10 01:48:15.000000 chatglm-llm-1.3.3/chatglm_src/chains/__init__.py
+-rw-r--r--   0 mroy       (501) staff       (20)     4402 2023-05-11 09:17:21.000000 chatglm-llm-1.3.3/chatglm_src/chains/local_qa.py
+-rw-r--r--   0 mroy       (501) staff       (20)      443 2023-05-04 01:08:28.000000 chatglm-llm-1.3.3/chatglm_src/cmd.py
+-rw-r--r--   0 mroy       (501) staff       (20)     3052 2023-05-11 09:34:29.000000 chatglm-llm-1.3.3/chatglm_src/embeding.py
+-rw-r--r--   0 mroy       (501) staff       (20)    24310 2023-05-13 03:01:32.000000 chatglm-llm-1.3.3/chatglm_src/llm.py
+drwxr-xr-x   0 mroy       (501) staff       (20)        0 2023-05-13 03:02:37.076890 chatglm-llm-1.3.3/chatglm_src/loader/
+-rw-r--r--   0 mroy       (501) staff       (20)     1403 2023-05-11 01:28:05.000000 chatglm-llm-1.3.3/chatglm_src/loader/__init__.py
+-rw-r--r--   0 mroy       (501) staff       (20)       38 2023-05-13 03:02:37.077224 chatglm-llm-1.3.3/setup.cfg
+-rw-r--r--   0 mroy       (501) staff       (20)      997 2023-05-13 03:02:29.000000 chatglm-llm-1.3.3/setup.py
```

### Comparing `chatglm-llm-1.3.2/README.md` & `chatglm-llm-1.3.3/README.md`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.2/chatglm_src/__init__.py` & `chatglm-llm-1.3.3/chatglm_src/__init__.py`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.2/chatglm_src/callbacks.py` & `chatglm-llm-1.3.3/chatglm_src/callbacks.py`

 * *Files 11% similar despite different names*

```diff
@@ -4,16 +4,18 @@
 from langchain.callbacks.base import AsyncCallbackHandler, BaseCallbackHandler
 from langchain.llms.base import LLMResult
 from langchain.prompts import PromptTemplate
 from typing import Any, Coroutine, Dict, List
 from termcolor import colored
 try:
     from langchain.callbacks.base import AsyncCallbackManager
+    from langchain.callbacks.base import BaseCallbackManager
 except:
     from langchain.callbacks.manager import AsyncCallbackManager
+    from langchain.callbacks.base import BaseCallbackManager
 
 
 class AsyncWebSocksetCallbackManager(AsyncCallbackManager):
     online_histories = {}
     user_id_websocket = {}
     async def on_llm_start(self, prompt: str,prompts: List[str], **kwargs: Any) -> Any:
         await super().on_llm_start(prompt, prompts, **kwargs)
```

### Comparing `chatglm-llm-1.3.2/chatglm_src/chains/local_qa.py` & `chatglm-llm-1.3.3/chatglm_src/chains/local_qa.py`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.2/chatglm_src/embeding.py` & `chatglm-llm-1.3.3/chatglm_src/embeding.py`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.2/chatglm_src/llm.py` & `chatglm-llm-1.3.3/chatglm_src/llm.py`

 * *Files 2% similar despite different names*

```diff
@@ -22,14 +22,15 @@
     from langchain.embeddings import HuggingFaceEmbeddings
     from accelerate import load_checkpoint_and_dispatch
     import torch, gc
     import gptcache
     from gptcache.processor.pre import get_prompt
     from gptcache.manager.factory import get_data_manager
     from langchain.cache import GPTCache
+    from langchain.callbacks.manager import BaseCallbackManager, CallbackManagerForLLMRun
     DEFAULT_CACHE_MAP_PATH = str(pathlib.Path.home() / ".cache" / "local_qa_cache_map")
     i = 0
 
     def init_gptcache_map(cache_obj: gptcache.Cache):
         global i
         cache_path = f'{DEFAULT_CACHE_MAP_PATH}_{i}.txt'
         cache_obj.init(
@@ -169,15 +170,15 @@
     model: Any = None
     tokenizer: Any = None
     model_path: str = pathlib.Path.home() / ".cache" / "chatglm"
     cpu: bool = False
     streaming: bool = False
     verbose: bool = False
     callbacks :Any  = [StreamingStdOutCallbackHandler(), AsyncWebsocketHandler()]
-    callback_manager:  Any = None
+    # callback_manager:  Any = BaseCallbackManager
     remote_host: Any = None
 
 
     @classmethod
     def load(cls, *args, model_path: str = None, **kargs):
         """
         Load a model from local or remote
@@ -276,15 +277,15 @@
                 },
                 verbose=self.verbose
             )
             return current_completion
         elif self.remote_host is not None :
             uri = f"ws://{self.remote_host}:15000"
             result = ''
-            # self.callback_manager =  langchain.callbacks.base.BaseCallbackManager(self.callbacks)
+            self.callback_manager =  BaseCallbackManager(self.callbacks)
             self.callback_manager.set_handlers(self.callbacks)
             async with AioWebSocket(uri) as aws:
                 converse = aws.manipulator
                 
                 user_id = md5(time.asctime().encode()).hexdigest()
                 await converse.send(json.dumps({"user_id":user_id, "password":PASSWORD}).encode())
                 res = await converse.receive()
@@ -337,15 +338,15 @@
         """
         every chunk of data is 2M
         """
         for i in range(0, len(data), 1024*1024*2):
             await ws.send(data[i:i+1024*1024*2])
         await ws.send("[STOP]")
     
-    def _call(self, prompt: str, stop: List[str]  = None) -> str:
+    def _call(self, prompt: str, stop: List[str]  = None,run_manager: Optional[CallbackManagerForLLMRun] = None) -> str:
         if self.streaming:
             current_completion = ""
             if self.verbose:
                 print("streaming")
             
             for response, history in self.model.stream_chat(self.tokenizer, prompt, self.history, max_length=self.max_token, top_p=self.top_p,
                                                temperature=self.temperature):
@@ -358,46 +359,58 @@
                     delta, verbose=self.verbose, **data
                 )
             auto_gc()
             self.history = self.history+[[prompt, current_completion]]
             return current_completion
         elif self.remote_host is not None :
             ws = create_connection(f"ws://{self.remote_host}:15000")
-            # self.callback_manager =  langchain.callbacks.base.BaseCallbackManager(self.callbacks)
-            self.callback_manager.set_handlers(self.callbacks)
             user_id = md5(time.asctime().encode()).hexdigest()
+            # self.callback_manager =  langchain.callbacks.base.BaseCallbackManager(self.callbacks)
+            
+            # self.callback_manager =  BaseCallbackManager(self.callbacks)
+            # self.callback_manager.set_handlers(self.callbacks)
             ws.send(json.dumps({"user_id":user_id, "password":PASSWORD}))
             # time.sleep(0.5)
             res = ws.recv()
             if res != "ok":
                 print(colored("[info]:","yellow") ,res)
                 raise Exception("password error")
             result = ''
             data = json.dumps({"prompt":prompt, "history":self.history})
             self.send_to_remote(data, ws)
-            self.callback_manager.on_llm_start(
-                prompt,
-                None,
-                verbose=self.verbose
-            )
+            
+            for callback in self.callbacks:
+                callback.on_llm_start(
+                    None,
+                    prompt,
+                    run_id=user_id,
+                    verbose=self.verbose
+                )
             while 1:
                 res = ws.recv()
                 msg = json.loads(res)
                 # { "new":delta,"response": response, "history": history,"query": prompt}
                 if "stop" in msg:
                     break
                 new_token = msg["new"]
                 response = msg["response"]
                 history = msg["history"]
                 msg["verbose"] = self.verbose
                 # self.remote_callback(new_token, history, response)
                 
-                self.callback_manager.on_llm_new_token(new_token, **msg)
+                # self.callback_manager.on_llm_new_token(new_token, **msg)
+                for callback in self.callbacks:
+                    callback.on_llm_new_token(
+                        new_token,
+                        **msg
+                    )
                 result = response
-            self.callback_manager.on_llm_end(result, verbose=self.verbose)
+            for callback in self.callbacks:
+                callback.on_llm_end(result, verbose=self.verbose)
+            
             self.history = self.history+[[prompt, result]]
             return result
         else:
             response, _ = self.model.chat(
                 self.tokenizer,
                 prompt,
                 history=self.history[-self.history_len:] if self.history_len>0 else [],
```

### Comparing `chatglm-llm-1.3.2/chatglm_src/loader/__init__.py` & `chatglm-llm-1.3.3/chatglm_src/loader/__init__.py`

 * *Files identical despite different names*

### Comparing `chatglm-llm-1.3.2/setup.py` & `chatglm-llm-1.3.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 
 from setuptools import setup, find_packages
 
 
 setup(name='chatglm-llm',
-    version='1.3.2',
+    version='1.3.3',
     description='chatglm llm',
     url='https://github.com/xxx',
     author='auth',
     author_email='xxx@gmail.com',
     license='MIT',
     include_package_data=True,
     zip_safe=False,
```

