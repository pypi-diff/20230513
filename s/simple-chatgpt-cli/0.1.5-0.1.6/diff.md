# Comparing `tmp/simple_chatgpt_cli-0.1.5.tar.gz` & `tmp/simple_chatgpt_cli-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simple_chatgpt_cli-0.1.5.tar", max compression
+gzip compressed data, was "simple_chatgpt_cli-0.1.6.tar", max compression
```

## Comparing `simple_chatgpt_cli-0.1.5.tar` & `simple_chatgpt_cli-0.1.6.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0     1321 2023-05-12 21:16:48.898764 simple_chatgpt_cli-0.1.5/README.md
--rw-r--r--   0        0        0        0 2023-05-12 12:32:57.857467 simple_chatgpt_cli-0.1.5/chatgpt_cli/__init__.py
--rw-r--r--   0        0        0     6444 2023-05-12 21:01:15.393834 simple_chatgpt_cli-0.1.5/chatgpt_cli/main.py
--rw-r--r--   0        0        0      701 2023-05-12 21:17:17.303436 simple_chatgpt_cli-0.1.5/pyproject.toml
--rw-r--r--   0        0        0     1767 1970-01-01 00:00:00.000000 simple_chatgpt_cli-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0     1429 2023-05-12 22:45:32.387874 simple_chatgpt_cli-0.1.6/README.md
+-rw-r--r--   0        0        0        0 2023-05-12 12:32:57.857467 simple_chatgpt_cli-0.1.6/chatgpt_cli/__init__.py
+-rw-r--r--   0        0        0     6697 2023-05-12 22:21:56.432298 simple_chatgpt_cli-0.1.6/chatgpt_cli/main.py
+-rw-r--r--   0        0        0      701 2023-05-12 22:45:47.139114 simple_chatgpt_cli-0.1.6/pyproject.toml
+-rw-r--r--   0        0        0     1875 1970-01-01 00:00:00.000000 simple_chatgpt_cli-0.1.6/PKG-INFO
```

### Comparing `simple_chatgpt_cli-0.1.5/README.md` & `simple_chatgpt_cli-0.1.6/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -20,14 +20,16 @@
 
 You must either set/save the key following the CLI prompts (recommended) or set an environment variable `OPENAI_API_KEY`.
 
 ![screenshot](screenshot.png)
 
 ## Tips
 
+Use `#multiline` to enter multiline mode. This is useful when you want to enter messages with line breaks.
+
 Use `#startover` to start a new conversation whenever you switch to a new topic and the bot doesn't need previous context anymore. This helps reduce your OpenAI bill.
 
 The program will remind you this if you come back to an idle conversation after more than 5 minutes.
 
 ## Development
 
 This project was initialized by my [Python project boilerplate](https://github.com/tailaiw/python-boilerplate). So you will need all the prerequisites of that project.
```

### Comparing `simple_chatgpt_cli-0.1.5/chatgpt_cli/main.py` & `simple_chatgpt_cli-0.1.6/chatgpt_cli/main.py`

 * *Files 3% similar despite different names*

```diff
@@ -97,14 +97,23 @@
             f"{WARNING_PREFIX} A new conversation will lose all previous context. Do you really want to start a new conversation?",
             default=True,
         )
         if startover_confirm:
             return ChatExitReason.START_OVER.value
         return request_user_input()
 
+    if user_input == "#multiline":
+        print("Multiline mode enabled. Press CTRL+D to finish.")
+        try:
+            user_input = ""
+            while True:
+                user_input += input() + "\n"
+        except EOFError:
+            pass
+
     return user_input
 
 
 def chat(
     model: str, has_previous_chat: bool, roller_message: Message | None = None
 ) -> tuple[ChatExitReason, Message | None]:
     # welcome console message
```

### Comparing `simple_chatgpt_cli-0.1.5/pyproject.toml` & `simple_chatgpt_cli-0.1.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 wrap-descriptions = 88
 
 [tool.poetry.scripts]
 chatgpt = 'chatgpt_cli.main:run'
 
 [tool.poetry]
 name = "simple-chatgpt-cli"
-version = "0.1.5"
+version = "0.1.6"
 description = ""
 authors = ["tailaiw <29800495+tailaiw@users.noreply.github.com>"]
 readme = "README.md"
 packages = [{ include = "chatgpt_cli" }]
 
 [tool.poetry.dependencies]
 python = ">=3.10,<3.12"
```

### Comparing `simple_chatgpt_cli-0.1.5/PKG-INFO` & `simple_chatgpt_cli-0.1.6/PKG-INFO`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-chatgpt-cli
-Version: 0.1.5
+Version: 0.1.6
 Summary: 
 Author: tailaiw
 Author-email: 29800495+tailaiw@users.noreply.github.com
 Requires-Python: >=3.10,<3.12
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
@@ -34,14 +34,16 @@
 
 You must either set/save the key following the CLI prompts (recommended) or set an environment variable `OPENAI_API_KEY`.
 
 ![screenshot](screenshot.png)
 
 ## Tips
 
+Use `#multiline` to enter multiline mode. This is useful when you want to enter messages with line breaks.
+
 Use `#startover` to start a new conversation whenever you switch to a new topic and the bot doesn't need previous context anymore. This helps reduce your OpenAI bill.
 
 The program will remind you this if you come back to an idle conversation after more than 5 minutes.
 
 ## Development
 
 This project was initialized by my [Python project boilerplate](https://github.com/tailaiw/python-boilerplate). So you will need all the prerequisites of that project.
```

