# Comparing `tmp/v4xyz-0.0.1.tar.gz` & `tmp/v4xyz-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "v4xyz-0.0.1.tar", last modified: Fri May 12 18:56:05 2023, max compression
+gzip compressed data, was "v4xyz-0.0.2.tar", last modified: Sat May 13 11:21:02 2023, max compression
```

## Comparing `v4xyz-0.0.1.tar` & `v4xyz-0.0.2.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 john      (1000) john      (1000)        0 2023-05-12 18:56:05.280767 v4xyz-0.0.1/
--rw-r--r--   0 john      (1000) john      (1000)     1801 2023-05-12 18:56:05.280767 v4xyz-0.0.1/PKG-INFO
--rw-r--r--   0 john      (1000) john      (1000)      781 2023-05-12 18:34:43.000000 v4xyz-0.0.1/README.md
--rw-r--r--   0 john      (1000) john      (1000)       38 2023-05-12 18:56:05.280767 v4xyz-0.0.1/setup.cfg
--rw-r--r--   0 john      (1000) john      (1000)     1358 2023-05-12 18:54:46.000000 v4xyz-0.0.1/setup.py
--rw-r--r--   0 john      (1000) john      (1000)     4465 2023-05-12 18:43:27.000000 v4xyz-0.0.1/v4.py
-drwxr-xr-x   0 john      (1000) john      (1000)        0 2023-05-12 18:56:05.280767 v4xyz-0.0.1/v4xyz.egg-info/
--rw-r--r--   0 john      (1000) john      (1000)     1801 2023-05-12 18:56:05.000000 v4xyz-0.0.1/v4xyz.egg-info/PKG-INFO
--rw-r--r--   0 john      (1000) john      (1000)      200 2023-05-12 18:56:05.000000 v4xyz-0.0.1/v4xyz.egg-info/SOURCES.txt
--rw-r--r--   0 john      (1000) john      (1000)        1 2023-05-12 18:56:05.000000 v4xyz-0.0.1/v4xyz.egg-info/dependency_links.txt
--rw-r--r--   0 john      (1000) john      (1000)       32 2023-05-12 18:56:05.000000 v4xyz-0.0.1/v4xyz.egg-info/entry_points.txt
--rw-r--r--   0 john      (1000) john      (1000)       41 2023-05-12 18:56:05.000000 v4xyz-0.0.1/v4xyz.egg-info/requires.txt
--rw-r--r--   0 john      (1000) john      (1000)        3 2023-05-12 18:56:05.000000 v4xyz-0.0.1/v4xyz.egg-info/top_level.txt
+drwxr-xr-x   0 john      (1000) john      (1000)        0 2023-05-13 11:21:02.041088 v4xyz-0.0.2/
+-rw-r--r--   0 john      (1000) john      (1000)     2305 2023-05-13 11:21:02.041088 v4xyz-0.0.2/PKG-INFO
+-rw-r--r--   0 john      (1000) john      (1000)     1236 2023-05-13 11:01:36.000000 v4xyz-0.0.2/README.md
+-rw-r--r--   0 john      (1000) john      (1000)       38 2023-05-13 11:21:02.041088 v4xyz-0.0.2/setup.cfg
+-rw-r--r--   0 john      (1000) john      (1000)     1358 2023-05-13 11:20:46.000000 v4xyz-0.0.2/setup.py
+-rw-r--r--   0 john      (1000) john      (1000)     4952 2023-05-13 11:19:45.000000 v4xyz-0.0.2/v4.py
+drwxr-xr-x   0 john      (1000) john      (1000)        0 2023-05-13 11:21:02.041088 v4xyz-0.0.2/v4xyz.egg-info/
+-rw-r--r--   0 john      (1000) john      (1000)     2305 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/PKG-INFO
+-rw-r--r--   0 john      (1000) john      (1000)      200 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/SOURCES.txt
+-rw-r--r--   0 john      (1000) john      (1000)        1 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/dependency_links.txt
+-rw-r--r--   0 john      (1000) john      (1000)       32 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/entry_points.txt
+-rw-r--r--   0 john      (1000) john      (1000)       41 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/requires.txt
+-rw-r--r--   0 john      (1000) john      (1000)        3 2023-05-13 11:21:02.000000 v4xyz-0.0.2/v4xyz.egg-info/top_level.txt
```

### Comparing `v4xyz-0.0.1/setup.py` & `v4xyz-0.0.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import os
 from setuptools import setup
 
-version = "0.0.1"
+version = "0.0.2"
 description = "A command line tool to chat with GPT4 and render markdown response."
 with open("README.md") as fp:
     long_description = fp.read()
 url = "https://github.com/imhuwq/v4xyz"
 author = "imhuwq"
 author_email = "imhuwq@gmail.com"
 classifiers = [
```

### Comparing `v4xyz-0.0.1/v4.py` & `v4xyz-0.0.2/v4.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,27 +1,36 @@
-import os
 import json
+import os
 from datetime import datetime
 
 import click
 import openai
+from art import text2art
+from rich import print
 from rich.live import Live
 from rich.markdown import Markdown
 
 HOME_DIR = os.path.expanduser("~")
 CONFIG_PATH = os.path.join(HOME_DIR, ".v4xyz", "config.json")
 CONFIG_TEMPLATE = """
 {
   "openai_secret": "",
   "http_proxy": "",
   "https_proxy": ""
 }
 """.strip()
 OPENAI_SECRET = None
-HISTORY_PATH = os.path.join(HOME_DIR, ".v4", "chat_history.txt")
+HISTORY_PATH = os.path.join(HOME_DIR, ".v4xyz", "chat_history.txt")
+
+
+class Cmd(click.Command):
+    def format_help(self, ctx, formatter):
+        art = text2art("This is the Way", "Small Slant")
+        click.echo(art)
+        super().format_help(ctx, formatter)
 
 
 def edit_config():
     if not os.path.exists(CONFIG_PATH):
         os.makedirs(os.path.dirname(CONFIG_PATH), exist_ok=True)
         with open(CONFIG_PATH, "w") as fp:
             fp.write(CONFIG_TEMPLATE)
@@ -49,14 +58,16 @@
 
 def count_token(content: str):
     return len(content) // 4
 
 
 def load_history(max_token: int = 4096):
     histories = []
+    if not os.path.exists(HISTORY_PATH):
+        return [], 0, 0
 
     with open(HISTORY_PATH, "r") as fp:
         block_data = ""
         block_role = None
         for line in fp:
             beg_q = line.startswith("Question\t")
             beg_a = line.startswith("Answer\t")
@@ -90,24 +101,28 @@
     return histories, total_token, num_dropped
 
 
 def ask_gpt4(inputs: str):
     histories, histories_token, num_dropped = load_history()
 
     system_prompt = "You are a helpful assistant always replay in markdown format."
+    system_prompt += "You should answer as brief as possible."
+
     sys_prompt_token = count_token(system_prompt)
     input_token = count_token(inputs)
     total_token = histories_token + sys_prompt_token + input_token
 
     messages = [{"role": "system", "content": system_prompt}, ]
     messages.extend(histories)
     messages.append({"role": "user", "content": inputs})
 
-    print(f">> Question : {inputs}")
-    print(f">> Meta     : [histories: {len(histories)}]\t[dropped: {num_dropped}]\t[tokens: {total_token}]\n")
+    print(f"[bold red   ]Question: {inputs}[/]")
+    print(f"[bold yellow]Context : {len(histories)} histories, {num_dropped} dropped, {total_token} tokens[/]")
+    print("-" * 10)
+    print("")
 
     rsp = openai.ChatCompletion.create(model="gpt-4", messages=messages, stream=True)
     answer = ""
     md = Markdown(answer)
     with Live(md, refresh_per_second=10) as live:
         for chunk in rsp:
             delta = chunk["choices"][0]["delta"]
@@ -117,20 +132,22 @@
 
     with open(HISTORY_PATH, "a") as fp:
         fp.write(f"Question\t{datetime.now()}\n{inputs}\n")
 
     with open(HISTORY_PATH, "a") as fp:
         fp.write(f"Answer\t{datetime.now()}\n{answer}\n")
 
-    print(f">> Meta     : [tokens: {count_token(answer)}]\n")
+    print("")
+    print("-" * 10)
+    print(f"[bold yellow]Received: {count_token(answer)} tokens[/]")
 
 
-@click.command()
+@click.command(cls=Cmd)
 @click.option("-e", "--edit", is_flag=True, help="Edit the config file")
-@click.argument("inputs", nargs=1, required=False)
+@click.argument("inputs", nargs=1, required=True)
 def v4(edit, inputs):
     if edit is True:
         return edit_config()
     else:
         load_config()
 
     inputs = inputs.strip()
```

