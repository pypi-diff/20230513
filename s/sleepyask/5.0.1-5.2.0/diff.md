# Comparing `tmp/sleepyask-5.0.1.tar.gz` & `tmp/sleepyask-5.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sleepyask-5.0.1.tar", last modified: Thu Apr 13 19:53:21 2023, max compression
+gzip compressed data, was "sleepyask-5.2.0.tar", last modified: Sat May 13 02:43:52 2023, max compression
```

## Comparing `sleepyask-5.0.1.tar` & `sleepyask-5.2.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-13 19:53:21.095219 sleepyask-5.0.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-04-13 19:53:11.000000 sleepyask-5.0.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5463 2023-04-13 19:53:21.095219 sleepyask-5.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5071 2023-04-13 19:53:11.000000 sleepyask-5.0.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      543 2023-04-13 19:53:11.000000 sleepyask-5.0.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-13 19:53:21.095219 sleepyask-5.0.1/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-13 19:53:21.091219 sleepyask-5.0.1/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-13 19:53:21.091219 sleepyask-5.0.1/src/sleepyask/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-13 19:53:21.095219 sleepyask-5.0.1/src/sleepyask/openai/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-13 19:53:11.000000 sleepyask-5.0.1/src/sleepyask/openai/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      994 2023-04-13 19:53:11.000000 sleepyask-5.0.1/src/sleepyask/openai/chat.py
--rw-r--r--   0 runner    (1001) docker     (123)     4643 2023-04-13 19:53:11.000000 sleepyask-5.0.1/src/sleepyask/openai/chatgpt.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-13 19:53:21.095219 sleepyask-5.0.1/src/sleepyask.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5463 2023-04-13 19:53:21.000000 sleepyask-5.0.1/src/sleepyask.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      310 2023-04-13 19:53:21.000000 sleepyask-5.0.1/src/sleepyask.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-13 19:53:21.000000 sleepyask-5.0.1/src/sleepyask.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       31 2023-04-13 19:53:21.000000 sleepyask-5.0.1/src/sleepyask.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-04-13 19:53:21.000000 sleepyask-5.0.1/src/sleepyask.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:43:52.804676 sleepyask-5.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-05-13 02:43:35.000000 sleepyask-5.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5471 2023-05-13 02:43:52.804676 sleepyask-5.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5079 2023-05-13 02:43:35.000000 sleepyask-5.2.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      543 2023-05-13 02:43:35.000000 sleepyask-5.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 02:43:52.804676 sleepyask-5.2.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:43:52.800676 sleepyask-5.2.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:43:52.800676 sleepyask-5.2.0/src/sleepyask/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:43:52.804676 sleepyask-5.2.0/src/sleepyask/openai/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:43:35.000000 sleepyask-5.2.0/src/sleepyask/openai/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      888 2023-05-13 02:43:35.000000 sleepyask-5.2.0/src/sleepyask/openai/chat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4098 2023-05-13 02:43:35.000000 sleepyask-5.2.0/src/sleepyask/openai/chatgpt.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:43:52.800676 sleepyask-5.2.0/src/sleepyask.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5471 2023-05-13 02:43:52.000000 sleepyask-5.2.0/src/sleepyask.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      310 2023-05-13 02:43:52.000000 sleepyask-5.2.0/src/sleepyask.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:43:52.000000 sleepyask-5.2.0/src/sleepyask.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-05-13 02:43:52.000000 sleepyask-5.2.0/src/sleepyask.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 02:43:52.000000 sleepyask-5.2.0/src/sleepyask.egg-info/top_level.txt
```

### Comparing `sleepyask-5.0.1/LICENSE` & `sleepyask-5.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `sleepyask-5.0.1/PKG-INFO` & `sleepyask-5.2.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sleepyask
-Version: 5.0.1
+Version: 5.2.0
 Summary: A small tool for automating collecting data from ChatGPT
 Author-email: hwelsters <redacted@redacted.redacted>
 Project-URL: Homepage, https://github.com/hwelsters/sleepyask
 Project-URL: Bug Tracker, https://github.com/hwelsters/sleepyask/issues
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -63,14 +63,15 @@
 > Create new secret key.  
 ```
 - `count` - This specifies the number of workers to create for asking questions. You can have multiple workers asking questions in parallel.  
 	
 ### Sample code
 It is recommended that you do not store your user credentials directly in your code. Instead, use something like `python-dotenv` to store your credentials in another file.
 ```python
+import os
 from dotenv import load_dotenv
 from sleepyask.openai import chat
 
 load_dotenv()  # take environment variables from .env.
 
 # Your ChatGPT authentication configs
 config = {
@@ -86,15 +87,15 @@
 question_list = ['What is 1 + 1?', 'What is 1 + 2?', 'What is 1 + 3?']
 
 # The filename in which you would like your responses to be stored.
 # sleepyask will create this file for you. If you create it yourself, there might be some problems.
 output_file_path = 'draw.json'  
 
 # Run sleepy_ask
-chat.ask(configs=configs,
+chat.ask(config=config,
            questions=question_list,
            output_file_path=output_file_path,
            verbose=True)
 ```
 
 <p align="center">
   <img src="https://user-images.githubusercontent.com/84760072/227817860-f4aef84b-9992-4ddd-a99d-019566cce0c5.png" width="900" />
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: sleepyask Version: 5.0.1 Summary: A small tool for
+Metadata-Version: 2.1 Name: sleepyask Version: 5.2.0 Summary: A small tool for
 automating collecting data from ChatGPT Author-email: hwelsters
 redacted.redacted> Project-URL: Homepage, https://github.com/hwelsters/
 sleepyask Project-URL: Bug Tracker, https://github.com/hwelsters/sleepyask/
 issues Requires-Python: >=3.7 Description-Content-Type: text/markdown License-
 File: LICENSE
  [https://user-images.githubusercontent.com/84760072/227817729-098182f3-6916-
                           48d8-b17a-4e4126ddd245.png]
@@ -24,25 +24,25 @@
 https://platform.openai.com/account/org-settings - `api_key` - You OpenAI API
 Key. To get it: ```bash > Go to https://platform.openai.com/account/api-keys >
 Login (if it is required) > Click on your profile picture on the top-right >
 View API Keys > Create new secret key. ``` - `count` - This specifies the
 number of workers to create for asking questions. You can have multiple workers
 asking questions in parallel. ### Sample code It is recommended that you do not
 store your user credentials directly in your code. Instead, use something like
-`python-dotenv` to store your credentials in another file. ```python from
-dotenv import load_dotenv from sleepyask.openai import chat load_dotenv() #
-take environment variables from .env. # Your ChatGPT authentication configs
+`python-dotenv` to store your credentials in another file. ```python import os
+from dotenv import load_dotenv from sleepyask.openai import chat load_dotenv()
+# take environment variables from .env. # Your ChatGPT authentication configs
 config = { "organization": os.getenv('OPENAI_ORGANIZATION_1'), "api_key":
 os.getenv('OPENAI_API_KEY_1'), "count": 1 } # List of authentication configs
 configs = [config] # List of questions you would like to ask ChatGPT
 question_list = ['What is 1 + 1?', 'What is 1 + 2?', 'What is 1 + 3?'] # The
 filename in which you would like your responses to be stored. # sleepyask will
 create this file for you. If you create it yourself, there might be some
 problems. output_file_path = 'draw.json' # Run sleepy_ask chat.ask
-(configs=configs, questions=question_list, output_file_path=output_file_path,
+(config=config, questions=question_list, output_file_path=output_file_path,
 verbose=True) ```
  [https://user-images.githubusercontent.com/84760072/227817860-f4aef84b-9992-
                           4ddd-a99d-019566cce0c5.png]
 ### Parameters `sleepyask.openai.ask` has the following parameters: ####
 Required - `configs` :: **(required)** - should be a list of dicts containing
 `organization` (your OpenAI organization ID), `api key` (your OpenAI api key)
 and the `count` (the number of instances to spin up for asking questions) -
```

### Comparing `sleepyask-5.0.1/README.md` & `sleepyask-5.2.0/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -52,14 +52,15 @@
 > Create new secret key.  
 ```
 - `count` - This specifies the number of workers to create for asking questions. You can have multiple workers asking questions in parallel.  
 	
 ### Sample code
 It is recommended that you do not store your user credentials directly in your code. Instead, use something like `python-dotenv` to store your credentials in another file.
 ```python
+import os
 from dotenv import load_dotenv
 from sleepyask.openai import chat
 
 load_dotenv()  # take environment variables from .env.
 
 # Your ChatGPT authentication configs
 config = {
@@ -75,15 +76,15 @@
 question_list = ['What is 1 + 1?', 'What is 1 + 2?', 'What is 1 + 3?']
 
 # The filename in which you would like your responses to be stored.
 # sleepyask will create this file for you. If you create it yourself, there might be some problems.
 output_file_path = 'draw.json'  
 
 # Run sleepy_ask
-chat.ask(configs=configs,
+chat.ask(config=config,
            questions=question_list,
            output_file_path=output_file_path,
            verbose=True)
 ```
 
 <p align="center">
   <img src="https://user-images.githubusercontent.com/84760072/227817860-f4aef84b-9992-4ddd-a99d-019566cce0c5.png" width="900" />
```

#### html2text {}

```diff
@@ -18,25 +18,25 @@
 https://platform.openai.com/account/org-settings - `api_key` - You OpenAI API
 Key. To get it: ```bash > Go to https://platform.openai.com/account/api-keys >
 Login (if it is required) > Click on your profile picture on the top-right >
 View API Keys > Create new secret key. ``` - `count` - This specifies the
 number of workers to create for asking questions. You can have multiple workers
 asking questions in parallel. ### Sample code It is recommended that you do not
 store your user credentials directly in your code. Instead, use something like
-`python-dotenv` to store your credentials in another file. ```python from
-dotenv import load_dotenv from sleepyask.openai import chat load_dotenv() #
-take environment variables from .env. # Your ChatGPT authentication configs
+`python-dotenv` to store your credentials in another file. ```python import os
+from dotenv import load_dotenv from sleepyask.openai import chat load_dotenv()
+# take environment variables from .env. # Your ChatGPT authentication configs
 config = { "organization": os.getenv('OPENAI_ORGANIZATION_1'), "api_key":
 os.getenv('OPENAI_API_KEY_1'), "count": 1 } # List of authentication configs
 configs = [config] # List of questions you would like to ask ChatGPT
 question_list = ['What is 1 + 1?', 'What is 1 + 2?', 'What is 1 + 3?'] # The
 filename in which you would like your responses to be stored. # sleepyask will
 create this file for you. If you create it yourself, there might be some
 problems. output_file_path = 'draw.json' # Run sleepy_ask chat.ask
-(configs=configs, questions=question_list, output_file_path=output_file_path,
+(config=config, questions=question_list, output_file_path=output_file_path,
 verbose=True) ```
  [https://user-images.githubusercontent.com/84760072/227817860-f4aef84b-9992-
                           4ddd-a99d-019566cce0c5.png]
 ### Parameters `sleepyask.openai.ask` has the following parameters: ####
 Required - `configs` :: **(required)** - should be a list of dicts containing
 `organization` (your OpenAI organization ID), `api key` (your OpenAI api key)
 and the `count` (the number of instances to spin up for asking questions) -
```

### Comparing `sleepyask-5.0.1/pyproject.toml` & `sleepyask-5.2.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "sleepyask"
-version = "5.0.1"
+version = "5.2.0"
 authors = [
   { name="hwelsters", email="redacted@redacted.redacted" },
 ]
 description = "A small tool for automating collecting data from ChatGPT"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = []
```

### Comparing `sleepyask-5.0.1/src/sleepyask/openai/chat.py` & `sleepyask-5.2.0/src/sleepyask/openai/chat.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,17 +1,21 @@
 from sleepyask.openai.chatgpt import ask_questions
 import traceback
 import logging
+import time
 
-def ask(config, questions : list, output_file_path : str, verbose: bool = False, model : str = "gpt-3.5-turbo", system_text : str | None = None, temperature : float | None = 1, max_tokens : int | None = 2048):
+def ask(configs : list, questions : list, output_file_path : str, verbose: bool = False, model : str = "gpt-3.5-turbo"):
     '''
     `config` should be a list containing your ChatGPT access tokens / email and password\n
     `questions` should contain a list of questions you would like ChatGPT to answer.\n
     `output_file_path` should be the file path where you would like your responses to be saved.\n
     '''
     redo = True
     while redo:
         if not isinstance(questions, list): raise ValueError("[questions] should be a list")
 
-        try: ask_questions(config=config, questions=questions, output_file_path=output_file_path, verbose=verbose, model=model, system_text=system_text, temperature=temperature, max_tokens=max_tokens)
+        try: ask_questions(configs=configs, questions=questions, output_file_path=output_file_path, verbose=verbose, model=model)
         except Exception as e: 
-            logging.error(traceback.format_exc())
+            logging.error(traceback.format_exc())
+        
+        time.sleep(60)
+
```

### Comparing `sleepyask-5.0.1/src/sleepyask/openai/chatgpt.py` & `sleepyask-5.2.0/src/sleepyask/openai/chatgpt.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,33 +1,34 @@
 import json
 from pathlib import Path
 from datetime import datetime
 import threading
 import queue
-import logging
+import logging 
 import traceback
-import time
-import openai
 
-def __append_to_file(output_file_path: str, data):
-    with open(output_file_path, 'a') as outfile:
-        outfile.write(json.dumps(data))
-        outfile.write("\n")
-        outfile.close()
+
 
 
 def __clean_str_for_json(text: str):
-    return text
+    return text.replace("\"", "\'")
+
 
-def ask_questions(config, questions : list, output_file_path : str, verbose: bool = False, model : str = "gpt-3.5-turbo", system_text : str | None = None, temperature : float | None = 1, max_tokens : int | None = 2048) -> None:
+def ask_questions(configs, questions: list, output_file_path: str, verbose: bool, model) -> None:
     question_queue = queue.Queue()
     save_queue = queue.Queue()
 
-    openai.organization = config["organization"]
-    openai.api_key = config["api_key"]
+    def actually_append(output_file_path: str, data):
+        with open(output_file_path, 'a') as outfile:
+            outfile.write(json.dumps(data))
+            outfile.write("\n")
+            outfile.close()
+
+    def __append_to_file(output_file_path: str, data):
+        save_queue.put(data)
 
     def loader_worker():
         if verbose:
             print(f"[sleepyask] Loading questions into queue")
         # Check for failed questions
         check_set = set()
         if Path(output_file_path).is_file():
@@ -49,85 +50,73 @@
         for index in range(0, len(questions)):
             if not index in check_set:
                 question_queue.put(
                     {"question": questions[index], "question_number": index})
 
         if question_queue.empty():
             print("[sleepyask] All questions exhausted")
-            print("\n***     DONE ASKING ALL QUESTIONS       ***")
-
-    def saver_worker():
-        while True:
-            if save_queue.empty(): continue
-            to_add = save_queue.get()
-            __append_to_file(output_file_path, to_add)
-            save_queue.task_done()
+            print("""
+***     DONE ASKING ALL QUESTIONS       ***""")
 
-    def asker_worker(index):
+    def asker_worker(index, config):
+        import openai
+        openai.organization = config["organization"]
+        openai.api_key = config["api_key"]
 
         succeed = True
         while succeed:
-            if question_queue.empty(): succeed = False
             question = question_queue.get()
             message = ''
             if verbose:
                 print(f"[sleepyask {index}] Asking:", question["question"])
+            # logging.disable(logging.ERROR)
             try:
-                messages = [
-                    {"role": "user", "content": question["question"]},
-                ]
-
-                if (system_text != None):
-                    messages.insert(
-                        0, {"role": "system", "content": system_text})
-
                 message = openai.ChatCompletion.create(
-                    temperature=temperature,
-                    max_tokens=max_tokens,
                     model=model,
-                    messages=messages
+                    messages=[
+                        {"role": "user", "content": question["question"]},
+                    ]
                 )
-
                 actual_model = message["model"]
                 usage = message["usage"]
                 message = message["choices"][0]["message"]["content"]
 
                 if verbose:
                     print(f"[sleepyask {index}] Received:", message)
 
                 dt_string = datetime.now().strftime("%d/%m/%Y %H:%M:%S")
-                row_to_append = {"model": actual_model, "temperature": temperature, "max_tokens": max_tokens, "date_time": dt_string, "question_number":
-                                 question["question_number"], "question": question["question"], "system_text": str(system_text), "response": __clean_str_for_json(message), **usage}
-                save_queue.put(row_to_append)
+                row_to_append = {"model": actual_model, "date_time": dt_string, "question_number":
+                                 question["question_number"], "question": question["question"], "response": __clean_str_for_json(message), **usage}
+                __append_to_file(output_file_path, row_to_append)
 
-            except KeyboardInterrupt:
-                succeed = False
-                break
-            except openai.error.AuthenticationError:
-                logging.error(traceback.format_exc())
-                question_queue.put(question)
-                time.sleep(120)
             except:
+                logging.error(traceback.format_exc())
+                
                 question_queue.put(question)
-                time.sleep(120)
+                succeed = False
 
             question_queue.task_done()
 
+    def saver_worker():
+        while True:
+            to_append = save_queue.get()
+            actually_append(output_file_path, to_append)
+
     thread_refs = []
-    for num in range(config["count"]):
-        t = threading.Thread(target=asker_worker, daemon=True, kwargs={'index': num})
-        thread_refs.append(t)
-        t.start()
-
-    loader = threading.Thread(target=loader_worker, daemon=True)
-    saver = threading.Thread(target=saver_worker, daemon=True)
-    thread_refs.append(loader)
-    thread_refs.append(saver)
-    
-    loader.start()
-    saver.start()
+    for index, config in enumerate(configs):
+        for num in range(config["count"]):
+            t = threading.Thread(target=asker_worker, daemon=True, kwargs={
+                'index': index * config["count"] + num, 'config': config})
+            thread_refs.append(t)
+            t.start()
+
+    t = threading.Thread(target=loader_worker, daemon=True)
+    thread_refs.append(t)
+    b = threading.Thread(target=saver_worker, daemon=True)
+    thread_refs.append(b)
+    t.start()
+    b.start()
 
     question_queue.join()
-    save_queue.join()
 
     for t in thread_refs:
         t.join()
```

### Comparing `sleepyask-5.0.1/src/sleepyask.egg-info/PKG-INFO` & `sleepyask-5.2.0/src/sleepyask.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sleepyask
-Version: 5.0.1
+Version: 5.2.0
 Summary: A small tool for automating collecting data from ChatGPT
 Author-email: hwelsters <redacted@redacted.redacted>
 Project-URL: Homepage, https://github.com/hwelsters/sleepyask
 Project-URL: Bug Tracker, https://github.com/hwelsters/sleepyask/issues
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -63,14 +63,15 @@
 > Create new secret key.  
 ```
 - `count` - This specifies the number of workers to create for asking questions. You can have multiple workers asking questions in parallel.  
 	
 ### Sample code
 It is recommended that you do not store your user credentials directly in your code. Instead, use something like `python-dotenv` to store your credentials in another file.
 ```python
+import os
 from dotenv import load_dotenv
 from sleepyask.openai import chat
 
 load_dotenv()  # take environment variables from .env.
 
 # Your ChatGPT authentication configs
 config = {
@@ -86,15 +87,15 @@
 question_list = ['What is 1 + 1?', 'What is 1 + 2?', 'What is 1 + 3?']
 
 # The filename in which you would like your responses to be stored.
 # sleepyask will create this file for you. If you create it yourself, there might be some problems.
 output_file_path = 'draw.json'  
 
 # Run sleepy_ask
-chat.ask(configs=configs,
+chat.ask(config=config,
            questions=question_list,
            output_file_path=output_file_path,
            verbose=True)
 ```
 
 <p align="center">
   <img src="https://user-images.githubusercontent.com/84760072/227817860-f4aef84b-9992-4ddd-a99d-019566cce0c5.png" width="900" />
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: sleepyask Version: 5.0.1 Summary: A small tool for
+Metadata-Version: 2.1 Name: sleepyask Version: 5.2.0 Summary: A small tool for
 automating collecting data from ChatGPT Author-email: hwelsters
 redacted.redacted> Project-URL: Homepage, https://github.com/hwelsters/
 sleepyask Project-URL: Bug Tracker, https://github.com/hwelsters/sleepyask/
 issues Requires-Python: >=3.7 Description-Content-Type: text/markdown License-
 File: LICENSE
  [https://user-images.githubusercontent.com/84760072/227817729-098182f3-6916-
                           48d8-b17a-4e4126ddd245.png]
@@ -24,25 +24,25 @@
 https://platform.openai.com/account/org-settings - `api_key` - You OpenAI API
 Key. To get it: ```bash > Go to https://platform.openai.com/account/api-keys >
 Login (if it is required) > Click on your profile picture on the top-right >
 View API Keys > Create new secret key. ``` - `count` - This specifies the
 number of workers to create for asking questions. You can have multiple workers
 asking questions in parallel. ### Sample code It is recommended that you do not
 store your user credentials directly in your code. Instead, use something like
-`python-dotenv` to store your credentials in another file. ```python from
-dotenv import load_dotenv from sleepyask.openai import chat load_dotenv() #
-take environment variables from .env. # Your ChatGPT authentication configs
+`python-dotenv` to store your credentials in another file. ```python import os
+from dotenv import load_dotenv from sleepyask.openai import chat load_dotenv()
+# take environment variables from .env. # Your ChatGPT authentication configs
 config = { "organization": os.getenv('OPENAI_ORGANIZATION_1'), "api_key":
 os.getenv('OPENAI_API_KEY_1'), "count": 1 } # List of authentication configs
 configs = [config] # List of questions you would like to ask ChatGPT
 question_list = ['What is 1 + 1?', 'What is 1 + 2?', 'What is 1 + 3?'] # The
 filename in which you would like your responses to be stored. # sleepyask will
 create this file for you. If you create it yourself, there might be some
 problems. output_file_path = 'draw.json' # Run sleepy_ask chat.ask
-(configs=configs, questions=question_list, output_file_path=output_file_path,
+(config=config, questions=question_list, output_file_path=output_file_path,
 verbose=True) ```
  [https://user-images.githubusercontent.com/84760072/227817860-f4aef84b-9992-
                           4ddd-a99d-019566cce0c5.png]
 ### Parameters `sleepyask.openai.ask` has the following parameters: ####
 Required - `configs` :: **(required)** - should be a list of dicts containing
 `organization` (your OpenAI organization ID), `api key` (your OpenAI api key)
 and the `count` (the number of instances to spin up for asking questions) -
```

