# Comparing `tmp/chatsnack-0.1.4.tar.gz` & `tmp/chatsnack-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chatsnack-0.1.4.tar", max compression
+gzip compressed data, was "chatsnack-0.1.5.tar", max compression
```

## Comparing `chatsnack-0.1.4.tar` & `chatsnack-0.1.5.tar`

### file list

```diff
@@ -1,26 +1,26 @@
--rw-r--r--   0        0        0     3795 2023-04-15 22:05:43.794976 chatsnack-0.1.4/chatsnack/__init__.py
--rw-r--r--   0        0        0     5793 2023-04-23 19:18:42.180282 chatsnack-0.1.4/chatsnack/aiwrapper.py
--rw-r--r--   0        0        0     1498 2023-04-09 18:26:53.563580 chatsnack-0.1.4/chatsnack/asynchelpers.py
--rw-r--r--   0        0        0     4486 2023-04-29 02:58:40.680324 chatsnack-0.1.4/chatsnack/chat/__init__.py
--rw-r--r--   0        0        0     6844 2023-04-29 03:01:10.662761 chatsnack-0.1.4/chatsnack/chat/mixin_messages.py
--rw-r--r--   0        0        0     4959 2023-05-07 23:04:09.343669 chatsnack-0.1.4/chatsnack/chat/mixin_params.py
--rw-r--r--   0        0        0     6966 2023-04-29 03:01:48.045271 chatsnack-0.1.4/chatsnack/chat/mixin_query.py
--rw-r--r--   0        0        0     3345 2023-04-23 15:02:14.751611 chatsnack-0.1.4/chatsnack/chat/mixin_serialization.py
--rw-r--r--   0        0        0      929 2023-04-09 15:02:47.382274 chatsnack-0.1.4/chatsnack/defaults.py
--rw-r--r--   0        0        0     1306 2023-04-09 15:11:16.782131 chatsnack-0.1.4/chatsnack/fillings.py
--rw-r--r--   0        0        0       25 2023-04-09 16:04:20.190406 chatsnack-0.1.4/chatsnack/packs/__init__.py
--rw-r--r--   0        0        0    19461 2023-04-14 02:01:22.528095 chatsnack-0.1.4/chatsnack/packs/default_packs/ChatsnackHelper.yml
--rw-r--r--   0        0        0      762 2023-04-14 02:00:30.545934 chatsnack-0.1.4/chatsnack/packs/default_packs/Chester.yml
--rw-r--r--   0        0        0      811 2023-04-14 01:57:06.309659 chatsnack-0.1.4/chatsnack/packs/default_packs/Confectioner.yml
--rw-r--r--   0        0        0      889 2023-04-14 01:57:06.272212 chatsnack-0.1.4/chatsnack/packs/default_packs/Data.yml
--rw-r--r--   0        0        0      736 2023-04-14 01:57:06.293264 chatsnack-0.1.4/chatsnack/packs/default_packs/Jane.yml
--rw-r--r--   0        0        0      905 2023-04-14 01:57:06.327853 chatsnack-0.1.4/chatsnack/packs/default_packs/Jolly.yml
--rw-r--r--   0        0        0     1244 2023-04-23 18:55:56.684760 chatsnack-0.1.4/chatsnack/packs/default_packs/Summarizer.yml
--rw-r--r--   0        0        0     2877 2023-05-03 23:27:38.108990 chatsnack-0.1.4/chatsnack/packs/module_help_vendor.py
--rw-r--r--   0        0        0     4028 2023-04-20 15:50:28.683064 chatsnack-0.1.4/chatsnack/packs/snackpacks.py
--rw-r--r--   0        0        0     1229 2023-04-06 15:39:54.021402 chatsnack-0.1.4/chatsnack/txtformat.py
--rw-r--r--   0        0        0     3976 2023-04-20 00:41:01.746999 chatsnack-0.1.4/chatsnack/yamlformat.py
--rw-r--r--   0        0        0     1091 2023-04-14 18:33:08.190283 chatsnack-0.1.4/LICENSE
--rw-r--r--   0        0        0     1005 2023-05-07 23:05:00.479706 chatsnack-0.1.4/pyproject.toml
--rw-r--r--   0        0        0     9186 2023-04-29 00:10:57.640242 chatsnack-0.1.4/README.md
--rw-r--r--   0        0        0    10107 1970-01-01 00:00:00.000000 chatsnack-0.1.4/PKG-INFO
+-rw-r--r--   0        0        0     3795 2023-04-15 22:05:43.794976 chatsnack-0.1.5/chatsnack/__init__.py
+-rw-r--r--   0        0        0     8609 2023-05-13 02:00:34.040960 chatsnack-0.1.5/chatsnack/aiwrapper.py
+-rw-r--r--   0        0        0     1498 2023-04-09 18:26:53.563580 chatsnack-0.1.5/chatsnack/asynchelpers.py
+-rw-r--r--   0        0        0     4542 2023-05-12 21:47:45.298231 chatsnack-0.1.5/chatsnack/chat/__init__.py
+-rw-r--r--   0        0        0     6844 2023-04-29 03:01:10.662761 chatsnack-0.1.5/chatsnack/chat/mixin_messages.py
+-rw-r--r--   0        0        0     5326 2023-05-12 15:23:39.491102 chatsnack-0.1.5/chatsnack/chat/mixin_params.py
+-rw-r--r--   0        0        0    11266 2023-05-12 23:17:34.321113 chatsnack-0.1.5/chatsnack/chat/mixin_query.py
+-rw-r--r--   0        0        0     3345 2023-04-23 15:02:14.751611 chatsnack-0.1.5/chatsnack/chat/mixin_serialization.py
+-rw-r--r--   0        0        0      929 2023-04-09 15:02:47.382274 chatsnack-0.1.5/chatsnack/defaults.py
+-rw-r--r--   0        0        0     1306 2023-04-09 15:11:16.782131 chatsnack-0.1.5/chatsnack/fillings.py
+-rw-r--r--   0        0        0       25 2023-04-09 16:04:20.190406 chatsnack-0.1.5/chatsnack/packs/__init__.py
+-rw-r--r--   0        0        0    19461 2023-04-14 02:01:22.528095 chatsnack-0.1.5/chatsnack/packs/default_packs/ChatsnackHelper.yml
+-rw-r--r--   0        0        0      762 2023-04-14 02:00:30.545934 chatsnack-0.1.5/chatsnack/packs/default_packs/Chester.yml
+-rw-r--r--   0        0        0      811 2023-04-14 01:57:06.309659 chatsnack-0.1.5/chatsnack/packs/default_packs/Confectioner.yml
+-rw-r--r--   0        0        0      889 2023-04-14 01:57:06.272212 chatsnack-0.1.5/chatsnack/packs/default_packs/Data.yml
+-rw-r--r--   0        0        0      736 2023-04-14 01:57:06.293264 chatsnack-0.1.5/chatsnack/packs/default_packs/Jane.yml
+-rw-r--r--   0        0        0      905 2023-04-14 01:57:06.327853 chatsnack-0.1.5/chatsnack/packs/default_packs/Jolly.yml
+-rw-r--r--   0        0        0     1244 2023-04-23 18:55:56.684760 chatsnack-0.1.5/chatsnack/packs/default_packs/Summarizer.yml
+-rw-r--r--   0        0        0     2877 2023-05-03 23:27:38.108990 chatsnack-0.1.5/chatsnack/packs/module_help_vendor.py
+-rw-r--r--   0        0        0     4028 2023-04-20 15:50:28.683064 chatsnack-0.1.5/chatsnack/packs/snackpacks.py
+-rw-r--r--   0        0        0     1229 2023-04-06 15:39:54.021402 chatsnack-0.1.5/chatsnack/txtformat.py
+-rw-r--r--   0        0        0     3976 2023-04-20 00:41:01.746999 chatsnack-0.1.5/chatsnack/yamlformat.py
+-rw-r--r--   0        0        0     1091 2023-04-14 18:33:08.190283 chatsnack-0.1.5/LICENSE
+-rw-r--r--   0        0        0     1030 2023-05-13 02:02:04.638312 chatsnack-0.1.5/pyproject.toml
+-rw-r--r--   0        0        0     9186 2023-04-29 00:10:57.640242 chatsnack-0.1.5/README.md
+-rw-r--r--   0        0        0    10107 1970-01-01 00:00:00.000000 chatsnack-0.1.5/PKG-INFO
```

### Comparing `chatsnack-0.1.4/chatsnack/__init__.py` & `chatsnack-0.1.5/chatsnack/__init__.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/aiwrapper.py` & `chatsnack-0.1.5/chatsnack/aiwrapper.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,21 +1,22 @@
 import asyncio
 import openai
 import os
 import json
+import time
 from loguru import logger
 from functools import wraps
 
 openai.api_key = os.getenv("OPENAI_API_KEY")
 
 async def set_api_key(api_key):
     openai.api_key = api_key
 
 # decorator to retry API calls
-def retryAPI(exception, tries=4, delay=3, backoff=2):
+def retryAPI_a(exception, tries=4, delay=3, backoff=2):
     """Retry calling the decorated function using an exponential backoff.
     :param Exception exception: the exception to check. may be a tuple of
         exceptions to check
     :param int tries: number of times to try (not retry) before giving up
     :param int delay: initial delay between retries in seconds
     :param int backoff: backoff multiplier e.g. value of 2 will double the
         delay each retry
@@ -34,15 +35,43 @@
                     await asyncio.sleep(mdelay)
                     mtries -= 1
                     mdelay *= backoff
             return await f(*args, **kwargs)
         return f_retry  # true decorator
     return deco_retry
 
+def retryAPI(exception, tries=4, delay=3, backoff=2):
+    """Retry calling the decorated function using an exponential backoff.
+    :param Exception exception: the exception to check. may be a tuple of
+        exceptions to check
+    :param int tries: number of times to try (not retry) before giving up
+    :param int delay: initial delay between retries in seconds
+    :param int backoff: backoff multiplier e.g. value of 2 will double the
+        delay each retry
+    :raises Exception: the last exception raised
+    """
+    def deco_retry(f):
+        @wraps(f)
+        def f_retry(*args, **kwargs):
+            mtries, mdelay = tries, delay
+            while mtries > 1:
+                try:
+                    return f(*args, **kwargs)
+                except exception as e:
+                    msg = "%s, Retrying in %d seconds..." % (str(e), mdelay)
+                    logger.debug(msg)
+                    time.sleep(mdelay)
+                    mtries -= 1
+                    mdelay *= backoff
+            return f(*args, **kwargs)
+        return f_retry  # true decorator
+    return deco_retry
+
 # openai
+@retryAPI_a(openai.error.RateLimitError, tries=3, delay=2, backoff=2)
 async def _chatcompletion(prompt, engine="gpt-3.5-turbo", max_tokens=None, temperature=0.7, top_p=1, stop=None, presence_penalty=0, frequency_penalty=0, n=1, stream=False, user=None):
     if user is None:
         user = "_not_set"
     # prompt will be in JSON format, let us translate it to a python list
     # if the prompt is a list already, we will just use it as is
     if isinstance(prompt, list):
         messages = prompt
@@ -62,26 +91,53 @@
                                             stop=stop,
                                             n=n,
                                             stream=stream,
                                             user=user)
     logger.trace("OpenAI Completion Result: {0}".format(response))
     return response
 
+@retryAPI(openai.error.RateLimitError, tries=3, delay=2, backoff=2)
+def _chatcompletion_s(prompt, engine="gpt-3.5-turbo", max_tokens=None, temperature=0.7, top_p=1, stop=None, presence_penalty=0, frequency_penalty=0, n=1, stream=False, user=None):
+    if user is None:
+        user = "_not_set"
+    # prompt will be in JSON format, let us translate it to a python list
+    # if the prompt is a list already, we will just use it as is
+    if isinstance(prompt, list):
+        messages = prompt
+    else:
+        messages = json.loads(prompt)
+    logger.trace("""Chat Query:
+    Prompt: {0}
+    Model: {2}, Max Tokens: {3}, Stop: {5}, Temperature: {1}, Top-P: {4}, Presence Penalty {6}, Frequency Penalty: {7}, N: {8}, Stream: {9}, User: {10}
+    """,prompt, temperature, engine, max_tokens, top_p, stop, presence_penalty, frequency_penalty, n, stream, user)
+    response = openai.ChatCompletion.create(model=engine,
+                                            messages=messages,
+                                            max_tokens=max_tokens,
+                                            temperature=temperature,
+                                            top_p=top_p,
+                                            presence_penalty=presence_penalty,
+                                            frequency_penalty=frequency_penalty,
+                                            stop=stop,
+                                            n=n,
+                                            stream=stream,
+                                            user=user)
+    logger.trace("OpenAI Completion Result: {0}".format(response))
+    return response
+
 def _trimmed_fetch_chat_response(resp, n):
     if n == 1:
         return resp.choices[0].message.content.strip()
     else:
         logger.trace('_trimmed_fetch_response :: returning {0} responses from ChatGPT'.format(n))
         texts = []
         for idx in range(0, n):
             texts.append(resp.choices[idx].message.content.strip())
         return texts
 
 # ChatGPT
-@retryAPI(openai.error.RateLimitError, tries=3, delay=2, backoff=2)
 async def cleaned_chat_completion(prompt, engine="gpt-3.5-turbo", max_tokens=None, temperature=0.7, top_p=1, stop=None, presence_penalty=0, frequency_penalty=0, n=1, stream=False, user=None, **ignored):
     '''
     Wrapper for OpenAI API chat completion. Returns whitespace trimmed result from ChatGPT.
     '''
     resp = await _chatcompletion(prompt,
                             engine=engine,
                             max_tokens=max_tokens,
```

### Comparing `chatsnack-0.1.4/chatsnack/asynchelpers.py` & `chatsnack-0.1.5/chatsnack/asynchelpers.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/chat/__init__.py` & `chatsnack-0.1.5/chatsnack/chat/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -82,16 +82,18 @@
                 # if we get two args, the first is the name and the second is the system message
                 self.system_message = args[1]
         
         self._initial_name = self.name
         self._initial_params = copy.copy(self.params)
         self._initial_messages = copy.copy(self.messages)
         self._initial_system_message = self.system_message
+        self._ready = True
    
     def reset(self) -> object:
         """ Resets the chat prompt to its initial state, returns itself """
         self.name = self._initial_name
         self.params = self._initial_params
         self.messages = self._initial_messages
         if self._initial_system_message is not None:
             self.system_message = self._initial_system_message
+        self._ready = True
         return self
```

### Comparing `chatsnack-0.1.4/chatsnack/chat/mixin_messages.py` & `chatsnack-0.1.5/chatsnack/chat/mixin_messages.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/chat/mixin_params.py` & `chatsnack-0.1.5/chatsnack/chat/mixin_params.py`

 * *Files 3% similar despite different names*

```diff
@@ -65,14 +65,26 @@
             return None
         return self.params.response_pattern
     @pattern.setter
     def pattern(self, value):
         if self.params is None:
             self.params = ChatParams()
         self.params.response_pattern = value
+    # same thing for streaming
+    @property
+    def stream(self):
+        if self.params is None:
+            return False # default to False
+        else:
+            return self.params.stream
+    @stream.setter
+    def stream(self, value: bool):
+        if self.params is None:
+            self.params = ChatParams()
+        self.params.stream = value
     def set_response_filter(self, prefix: Optional[str] = None, suffix: Optional[str] = None, pattern: Optional[str] = None):
         """ Filters the response given prefix and suffix or pattern. If suffix is None, it is set to the same as prefix. 
          Note that this overwrites any existing regex pattern. ⭐ """
         # if pattern is set then fail if they provided prefix or suffix
         if pattern:
             if prefix or suffix:
                 raise ValueError("Cannot set both pattern and prefix/suffix")
```

### Comparing `chatsnack-0.1.4/chatsnack/chat/mixin_serialization.py` & `chatsnack-0.1.5/chatsnack/chat/mixin_serialization.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/defaults.py` & `chatsnack-0.1.5/chatsnack/defaults.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/fillings.py` & `chatsnack-0.1.5/chatsnack/fillings.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/default_packs/ChatsnackHelper.yml` & `chatsnack-0.1.5/chatsnack/packs/default_packs/ChatsnackHelper.yml`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/default_packs/Chester.yml` & `chatsnack-0.1.5/chatsnack/packs/default_packs/Chester.yml`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/default_packs/Confectioner.yml` & `chatsnack-0.1.5/chatsnack/packs/default_packs/Confectioner.yml`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/default_packs/Data.yml` & `chatsnack-0.1.5/chatsnack/packs/default_packs/Data.yml`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/default_packs/Jane.yml` & `chatsnack-0.1.5/chatsnack/packs/default_packs/Jane.yml`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/default_packs/Jolly.yml` & `chatsnack-0.1.5/chatsnack/packs/default_packs/Jolly.yml`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/default_packs/Summarizer.yml` & `chatsnack-0.1.5/chatsnack/packs/default_packs/Summarizer.yml`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/module_help_vendor.py` & `chatsnack-0.1.5/chatsnack/packs/module_help_vendor.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/packs/snackpacks.py` & `chatsnack-0.1.5/chatsnack/packs/snackpacks.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/txtformat.py` & `chatsnack-0.1.5/chatsnack/txtformat.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/chatsnack/yamlformat.py` & `chatsnack-0.1.5/chatsnack/yamlformat.py`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/LICENSE` & `chatsnack-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/pyproject.toml` & `chatsnack-0.1.5/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "chatsnack"
-version = "0.1.4"
+version = "0.1.5"
 description = "chatsnack is the easiest Python library for rapid development with OpenAI's ChatGPT API. It provides an intuitive interface for creating and managing chat-based prompts and responses, making it convenient to build complex, interactive conversations with AI."
 authors = ["Mattie Casper"]
 license = "MIT"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.10"
@@ -16,14 +16,15 @@
 Flask = {version = "^2.1", optional = true}
 questionary = {version = "^1.10.0", optional = true}
 rich = {version = "^13.3.2", optional = true}
 
 [tool.poetry.dev-dependencies]
 pytest = "^7.2"
 pytest-asyncio = "^0.21.0"
+pytest-mock = "^3.10.0"
 
 [tool.poetry.extras]
 flask = ["Flask"]
 questionary = ["questionary"]
 rich = ["rich"]
 examples = ["questionary", "rich", "Flask"]
```

### Comparing `chatsnack-0.1.4/README.md` & `chatsnack-0.1.5/README.md`

 * *Files identical despite different names*

### Comparing `chatsnack-0.1.4/PKG-INFO` & `chatsnack-0.1.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chatsnack
-Version: 0.1.4
+Version: 0.1.5
 Summary: chatsnack is the easiest Python library for rapid development with OpenAI's ChatGPT API. It provides an intuitive interface for creating and managing chat-based prompts and responses, making it convenient to build complex, interactive conversations with AI.
 License: MIT
 Author: Mattie Casper
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
```

