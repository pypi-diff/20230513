# Comparing `tmp/simple_chatgpt_cli-0.1.6.tar.gz` & `tmp/simple_chatgpt_cli-0.1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simple_chatgpt_cli-0.1.6.tar", max compression
+gzip compressed data, was "simple_chatgpt_cli-0.1.7.tar", max compression
```

## Comparing `simple_chatgpt_cli-0.1.6.tar` & `simple_chatgpt_cli-0.1.7.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0     1429 2023-05-12 22:45:32.387874 simple_chatgpt_cli-0.1.6/README.md
--rw-r--r--   0        0        0        0 2023-05-12 12:32:57.857467 simple_chatgpt_cli-0.1.6/chatgpt_cli/__init__.py
--rw-r--r--   0        0        0     6697 2023-05-12 22:21:56.432298 simple_chatgpt_cli-0.1.6/chatgpt_cli/main.py
--rw-r--r--   0        0        0      701 2023-05-12 22:45:47.139114 simple_chatgpt_cli-0.1.6/pyproject.toml
--rw-r--r--   0        0        0     1875 1970-01-01 00:00:00.000000 simple_chatgpt_cli-0.1.6/PKG-INFO
+-rw-r--r--   0        0        0     1429 2023-05-12 22:45:32.387874 simple_chatgpt_cli-0.1.7/README.md
+-rw-r--r--   0        0        0        0 2023-05-12 12:32:57.857467 simple_chatgpt_cli-0.1.7/chatgpt_cli/__init__.py
+-rw-r--r--   0        0        0     6758 2023-05-12 22:48:55.832214 simple_chatgpt_cli-0.1.7/chatgpt_cli/main.py
+-rw-r--r--   0        0        0      701 2023-05-12 22:52:08.737344 simple_chatgpt_cli-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0     1875 1970-01-01 00:00:00.000000 simple_chatgpt_cli-0.1.7/PKG-INFO
```

### Comparing `simple_chatgpt_cli-0.1.6/README.md` & `simple_chatgpt_cli-0.1.7/README.md`

 * *Files identical despite different names*

### Comparing `simple_chatgpt_cli-0.1.6/chatgpt_cli/main.py` & `simple_chatgpt_cli-0.1.7/chatgpt_cli/main.py`

 * *Files 2% similar despite different names*

```diff
@@ -115,17 +115,18 @@
 
 def chat(
     model: str, has_previous_chat: bool, roller_message: Message | None = None
 ) -> tuple[ChatExitReason, Message | None]:
     # welcome console message
     if not has_previous_chat:
         print(
-            f"{INFO_PREFIX} You can now start chatting with the bot. "
+            f"{INFO_PREFIX} You can now start chatting with the bot. \n"
             f"Type '{ChatExitReason.EXIT.value}' to exit. "
-            f"Type '{ChatExitReason.START_OVER.value}' to start a new conversation (a new conversation will lose all previous context)."
+            f"Type '{ChatExitReason.START_OVER.value}' to start a new conversation (a new conversation will lose all previous context). "
+            f"Type '#multiline' to enter multiline mode."
         )
     else:
         print(
             f"{INFO_PREFIX} A new conversation started. The bot forgot all previous context."
         )
 
     if roller_message is None:
```

### Comparing `simple_chatgpt_cli-0.1.6/pyproject.toml` & `simple_chatgpt_cli-0.1.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 wrap-descriptions = 88
 
 [tool.poetry.scripts]
 chatgpt = 'chatgpt_cli.main:run'
 
 [tool.poetry]
 name = "simple-chatgpt-cli"
-version = "0.1.6"
+version = "0.1.7"
 description = ""
 authors = ["tailaiw <29800495+tailaiw@users.noreply.github.com>"]
 readme = "README.md"
 packages = [{ include = "chatgpt_cli" }]
 
 [tool.poetry.dependencies]
 python = ">=3.10,<3.12"
```

### Comparing `simple_chatgpt_cli-0.1.6/PKG-INFO` & `simple_chatgpt_cli-0.1.7/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-chatgpt-cli
-Version: 0.1.6
+Version: 0.1.7
 Summary: 
 Author: tailaiw
 Author-email: 29800495+tailaiw@users.noreply.github.com
 Requires-Python: >=3.10,<3.12
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
```

