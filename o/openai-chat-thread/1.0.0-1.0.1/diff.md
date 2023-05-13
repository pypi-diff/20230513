# Comparing `tmp/openai-chat-thread-1.0.0.tar.gz` & `tmp/openai-chat-thread-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "openai-chat-thread-1.0.0.tar", last modified: Fri May 12 23:59:13 2023, max compression
+gzip compressed data, was "openai-chat-thread-1.0.1.tar", last modified: Sat May 13 00:23:04 2023, max compression
```

## Comparing `openai-chat-thread-1.0.0.tar` & `openai-chat-thread-1.0.1.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 23:59:13.299806 openai-chat-thread-1.0.0/
--rw-r--r--   0 chiubowen   (501) staff       (20)     2122 2023-05-12 23:59:13.299680 openai-chat-thread-1.0.0/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)     1946 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/README.md
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 23:59:13.299500 openai-chat-thread-1.0.0/openai_chat_thread.egg-info/
--rw-r--r--   0 chiubowen   (501) staff       (20)     2122 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/openai_chat_thread.egg-info/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)      294 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/openai_chat_thread.egg-info/SOURCES.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/openai_chat_thread.egg-info/dependency_links.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       64 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/openai_chat_thread.egg-info/entry_points.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       21 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/openai_chat_thread.egg-info/requires.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       19 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/openai_chat_thread.egg-info/top_level.txt
--rwxr-xr-x   0 chiubowen   (501) staff       (20)     1367 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/openai_chat_thread.py
--rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-12 23:59:13.299843 openai-chat-thread-1.0.0/setup.cfg
--rw-r--r--   0 chiubowen   (501) staff       (20)      536 2023-05-12 23:59:13.000000 openai-chat-thread-1.0.0/setup.py
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 00:23:04.524890 openai-chat-thread-1.0.1/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     2294 2023-05-13 00:23:04.524719 openai-chat-thread-1.0.1/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)     2118 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/README.md
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 00:23:04.524555 openai-chat-thread-1.0.1/openai_chat_thread.egg-info/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     2294 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/openai_chat_thread.egg-info/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)      294 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/openai_chat_thread.egg-info/SOURCES.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/openai_chat_thread.egg-info/dependency_links.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       64 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/openai_chat_thread.egg-info/entry_points.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       49 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/openai_chat_thread.egg-info/requires.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       19 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/openai_chat_thread.egg-info/top_level.txt
+-rwxr-xr-x   0 chiubowen   (501) staff       (20)     1712 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/openai_chat_thread.py
+-rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-13 00:23:04.524927 openai-chat-thread-1.0.1/setup.cfg
+-rw-r--r--   0 chiubowen   (501) staff       (20)      536 2023-05-13 00:23:04.000000 openai-chat-thread-1.0.1/setup.py
```

### Comparing `openai-chat-thread-1.0.0/PKG-INFO` & `openai-chat-thread-1.0.1/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: openai-chat-thread
-Version: 1.0.0
+Version: 1.0.1
 Summary: UNKNOWN
 Home-page: UNKNOWN
 License: UNKNOWN
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # GPT 聊天程式碼庫
@@ -44,23 +44,24 @@
 然後 GPT 將回應您的提示。
 
 ## 函式庫用法
 
 您也可以在 Python 程式中導入此庫並使用它。只需導入`openai_chat_thread`函數，並提供一個提示（prompt）：
 
 ```python
-from openai_chat_thread import openai_chat_thread
-
-q = openai_chat_thread("你好，GPT！")
-
-response = q.get()
-print(response)
+from openai_chat_thread import openai_chat_thread_taiwan, openai_chat_thread
+q = openai_chat_thread_taiwan('妳好') # 若改用 openai_chat_thread 就不會自動轉繁體中文 
+while True:
+    response = q.get()
+    if response is None:
+        break
+    print(response, end="", flush=True)
 ```
 
-`openai_chat_thread`函數將返回一個`queue.Queue`對象，您可以使用它來讀取 GPT 的回應。
+`openai_chat_thread_taiwan`函數將返回一個`queue.Queue`對象，您可以使用它來讀取 GPT 的回應。
 
 ## 運作原理
 
 該程式碼庫使用 OpenAI 提供的 GPT-4 模型。當您提供一個提示（prompt）時，該程序將向 GPT-4 模型發送請求，並將其回應返回給您。
 
 為了實現實時回應，我們在後台啟動一個新的執行緒，並在其中與 GPT 模型進行通信。這意味著您可以在等待 GPT 的回應時繼續執行其他任務。
```

### Comparing `openai-chat-thread-1.0.0/README.md` & `openai-chat-thread-1.0.1/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -35,23 +35,24 @@
 然後 GPT 將回應您的提示。
 
 ## 函式庫用法
 
 您也可以在 Python 程式中導入此庫並使用它。只需導入`openai_chat_thread`函數，並提供一個提示（prompt）：
 
 ```python
-from openai_chat_thread import openai_chat_thread
-
-q = openai_chat_thread("你好，GPT！")
-
-response = q.get()
-print(response)
+from openai_chat_thread import openai_chat_thread_taiwan, openai_chat_thread
+q = openai_chat_thread_taiwan('妳好') # 若改用 openai_chat_thread 就不會自動轉繁體中文 
+while True:
+    response = q.get()
+    if response is None:
+        break
+    print(response, end="", flush=True)
 ```
 
-`openai_chat_thread`函數將返回一個`queue.Queue`對象，您可以使用它來讀取 GPT 的回應。
+`openai_chat_thread_taiwan`函數將返回一個`queue.Queue`對象，您可以使用它來讀取 GPT 的回應。
 
 ## 運作原理
 
 該程式碼庫使用 OpenAI 提供的 GPT-4 模型。當您提供一個提示（prompt）時，該程序將向 GPT-4 模型發送請求，並將其回應返回給您。
 
 為了實現實時回應，我們在後台啟動一個新的執行緒，並在其中與 GPT 模型進行通信。這意味著您可以在等待 GPT 的回應時繼續執行其他任務。
```

### Comparing `openai-chat-thread-1.0.0/openai_chat_thread.egg-info/PKG-INFO` & `openai-chat-thread-1.0.1/openai_chat_thread.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: openai-chat-thread
-Version: 1.0.0
+Version: 1.0.1
 Summary: UNKNOWN
 Home-page: UNKNOWN
 License: UNKNOWN
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # GPT 聊天程式碼庫
@@ -44,23 +44,24 @@
 然後 GPT 將回應您的提示。
 
 ## 函式庫用法
 
 您也可以在 Python 程式中導入此庫並使用它。只需導入`openai_chat_thread`函數，並提供一個提示（prompt）：
 
 ```python
-from openai_chat_thread import openai_chat_thread
-
-q = openai_chat_thread("你好，GPT！")
-
-response = q.get()
-print(response)
+from openai_chat_thread import openai_chat_thread_taiwan, openai_chat_thread
+q = openai_chat_thread_taiwan('妳好') # 若改用 openai_chat_thread 就不會自動轉繁體中文 
+while True:
+    response = q.get()
+    if response is None:
+        break
+    print(response, end="", flush=True)
 ```
 
-`openai_chat_thread`函數將返回一個`queue.Queue`對象，您可以使用它來讀取 GPT 的回應。
+`openai_chat_thread_taiwan`函數將返回一個`queue.Queue`對象，您可以使用它來讀取 GPT 的回應。
 
 ## 運作原理
 
 該程式碼庫使用 OpenAI 提供的 GPT-4 模型。當您提供一個提示（prompt）時，該程序將向 GPT-4 模型發送請求，並將其回應返回給您。
 
 為了實現實時回應，我們在後台啟動一個新的執行緒，並在其中與 GPT 模型進行通信。這意味著您可以在等待 GPT 的回應時繼續執行其他任務。
```

### Comparing `openai-chat-thread-1.0.0/openai_chat_thread.py` & `openai-chat-thread-1.0.1/openai_chat_thread.py`

 * *Files 15% similar despite different names*

```diff
@@ -2,49 +2,58 @@
 import argparse
 import os
 import queue
 import threading
 
 import openai
 from dotenv import load_dotenv
+from opencc import OpenCC
+
+cc = OpenCC('s2t')
 
 load_dotenv()
 openai.api_key = os.getenv("OPENAI_API_KEY")
 
 
-def openai_chat_thread(prompt=None):
-    def process_gpt(prompt: str, q: queue.Queue):
-        dic = {}
+def openai_chat_thread(prompt=None, convert_to_taiwan=False):
+    def process_gpt(prompt: str, q: queue.Queue, convert_to_traditional: bool):
         response = openai.ChatCompletion.create(
             model="gpt-4",
             messages=[{"role": "system", "content": prompt}],
             temperature=0.5,
             stream=True,
             max_tokens=2048
         )
         for chunk in response:
             delta = chunk["choices"][0]["delta"]
             if "finish_reason" in chunk["choices"][0] and chunk["choices"][0]["finish_reason"] == "stop":
                 break
             if "content" in delta:
-                q.put(delta["content"])
+                content = delta["content"]
+                if convert_to_traditional:
+                    content = cc.convert(content)
+                q.put(content)
         q.put(None)
 
     q = queue.Queue()
-    new_thread = threading.Thread(target=process_gpt, args=(prompt, q))
+    new_thread = threading.Thread(target=process_gpt, args=(prompt, q, convert_to_taiwan))
     new_thread.start()
     return q
 
 
+def openai_chat_thread_taiwan(prompt=None):
+    return openai_chat_thread(prompt, convert_to_taiwan=True)
+
+
 def main():
     parser = argparse.ArgumentParser(description="Chat with GPT.")
     parser.add_argument("prompt", type=str, help="The prompt for GPT to respond to")
     args = parser.parse_args()
 
-    q = openai_chat_thread(args.prompt)
+    q = openai_chat_thread_taiwan(args.prompt)
 
     while True:
         response = q.get()
         if response is None:
             break
         print(response, end="", flush=True)
```

### Comparing `openai-chat-thread-1.0.0/setup.py` & `openai-chat-thread-1.0.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from setuptools import setup, find_packages
 
 with open('requirements.txt') as f:
     requirements = [line.strip() for line in f.readlines()]
 
 setup(
     name="openai-chat-thread",
-    version="1.0.0",
+    version="1.0.1",
     packages=find_packages(),
     py_modules=['openai_chat_thread'],
     install_requires=requirements,
     entry_points={
         'console_scripts': [
             'openai_chat_thread = openai_chat_thread:main',
         ],
```

