# Comparing `tmp/griseo-0.8.0.tar.gz` & `tmp/griseo-0.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "griseo-0.8.0.tar", max compression
+gzip compressed data, was "griseo-0.9.0.tar", max compression
```

## Comparing `griseo-0.8.0.tar` & `griseo-0.9.0.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0    11357 2023-04-24 14:34:40.416451 griseo-0.8.0/LICENSE
--rw-r--r--   0        0        0      280 2023-04-24 14:34:40.416451 griseo-0.8.0/README.md
--rw-r--r--   0        0        0     3403 2023-04-24 14:34:40.416451 griseo-0.8.0/griseo/__init__.py
--rw-r--r--   0        0        0      653 2023-04-24 14:34:40.416451 griseo-0.8.0/griseo/__main__.py
--rw-r--r--   0        0        0     1193 2023-04-24 14:34:40.416451 griseo-0.8.0/pyproject.toml
--rw-r--r--   0        0        0     1115 1970-01-01 00:00:00.000000 griseo-0.8.0/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-04-25 03:10:55.574123 griseo-0.9.0/LICENSE
+-rw-r--r--   0        0        0      280 2023-04-25 03:10:55.574123 griseo-0.9.0/README.md
+-rw-r--r--   0        0        0     4086 2023-04-25 03:10:55.574123 griseo-0.9.0/griseo/__init__.py
+-rw-r--r--   0        0        0      653 2023-04-25 03:10:55.574123 griseo-0.9.0/griseo/__main__.py
+-rw-r--r--   0        0        0     1213 2023-04-25 03:10:55.574123 griseo-0.9.0/pyproject.toml
+-rw-r--r--   0        0        0     1156 1970-01-01 00:00:00.000000 griseo-0.9.0/PKG-INFO
```

### Comparing `griseo-0.8.0/LICENSE` & `griseo-0.9.0/LICENSE`

 * *Files identical despite different names*

### Comparing `griseo-0.8.0/griseo/__init__.py` & `griseo-0.9.0/griseo/__init__.py`

 * *Files 20% similar despite different names*

```diff
@@ -14,14 +14,20 @@
 
 import sys
 import textwrap
 from argparse import ArgumentParser, ArgumentDefaultsHelpFormatter, REMAINDER
 from importlib import metadata
 
 import openai
+from tenacity import (
+    retry,
+    stop_after_attempt,
+    wait_random_exponential,
+    retry_if_exception_type,
+)  # for exponential backoff
 
 __version__ = metadata.version(__package__)
 del metadata  # avoids polluting the results of dir(__package__)
 
 
 def spin(response, print_role) -> (str, str):
     role, content = '', ''
@@ -33,37 +39,47 @@
         if delta.get('content'):
             content += delta['content']
             print(delta['content'], end='', flush=True)
     print()
     return role, content
 
 
+@retry(
+    wait=wait_random_exponential(min=1, max=60),
+    stop=stop_after_attempt(3),
+    retry=retry_if_exception_type(openai.error.RateLimitError),
+    reraise=True)
+def completions_with_backoff(**kwargs):
+    return openai.ChatCompletion.create(**kwargs)
+
+
 def oneshot(words):
     content = ' '.join(words)
-    response = openai.ChatCompletion.create(
+    response = completions_with_backoff(
         model="gpt-3.5-turbo",
         messages=[{"role": "user", "content": content}],
         stream=True)
     spin(response, print_role=False)
 
 
 def chat():
     class Context:
         def __init__(self):
             self._messages = [
                 {"role": "system", "content": "You are a helpful assistant."}
             ]
 
         def tell(self, msg):
-            self._messages.append({"role": "user", "content": msg})
-            response = openai.ChatCompletion.create(
+            messages = self._messages + [{"role": "user", "content": msg}]
+            response = completions_with_backoff(
                 model="gpt-3.5-turbo",
-                messages=self._messages,
+                messages=messages,
                 stream=True)
             role, content = spin(response, print_role=True)
+            self._messages.append({"role": "user", "content": msg})
             self._messages.append({"role": role, "content": content})
 
         def clear(self):
             self._messages = []
 
     ctx = Context()
 
@@ -78,21 +94,29 @@
     Welcome to chat with Griseo!
 
     type :c or :clear to clear context
     type :q or :quit  to exit
     """))
 
     while True:
-        req = input('user << ').strip()
+        try:
+            req = input('user << ').strip()
+        except (EOFError, KeyboardInterrupt):
+            print()
+            break
+
         if req.startswith(':'):
             commands[req[1:]]()
             continue
 
         if len(req) > 0:  # skip empty input
-            ctx.tell(req)
+            try:
+                ctx.tell(req)
+            except openai.error.RateLimitError as e:
+                print(e.user_message)
 
 
 def main():
     import dotenv
     import os
 
     dotenv.load_dotenv()
```

### Comparing `griseo-0.8.0/griseo/__main__.py` & `griseo-0.9.0/griseo/__main__.py`

 * *Files identical despite different names*

### Comparing `griseo-0.8.0/pyproject.toml` & `griseo-0.9.0/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -10,28 +10,29 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 [tool.poetry]
 name = "griseo"
-version = "0.8.0"
+version = "0.9.0"
 description = "Chat with OpenAI in the Hacker way."
 authors = ["tison <wander4096@gmail.com>"]
 license = "Apache-2.0"
 readme = "README.md"
 homepage = "https://github.com/korandoru/griseo"
 repository = "https://github.com/korandoru/griseo"
 documentation = "https://github.com/korandoru/griseo"
 keywords = ["chatgpt", "cli", "openai"]
 
 [tool.poetry.dependencies]
 python = "^3.8"
 openai = "^0.27.4"
 python-dotenv = "^1.0.0"
+tenacity = "^8.2.2"
 
 [tool.poetry.scripts]
 griseo = "griseo:main"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `griseo-0.8.0/PKG-INFO` & `griseo-0.9.0/PKG-INFO`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: griseo
-Version: 0.8.0
+Version: 0.9.0
 Summary: Chat with OpenAI in the Hacker way.
 Home-page: https://github.com/korandoru/griseo
 License: Apache-2.0
 Keywords: chatgpt,cli,openai
 Author: tison
 Author-email: wander4096@gmail.com
 Requires-Python: >=3.8,<4.0
@@ -12,14 +12,15 @@
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: openai (>=0.27.4,<0.28.0)
 Requires-Dist: python-dotenv (>=1.0.0,<2.0.0)
+Requires-Dist: tenacity (>=8.2.2,<9.0.0)
 Project-URL: Documentation, https://github.com/korandoru/griseo
 Project-URL: Repository, https://github.com/korandoru/griseo
 Description-Content-Type: text/markdown
 
 # Griseo
 
 Chat with OpenAI in the Hacker way.
```

