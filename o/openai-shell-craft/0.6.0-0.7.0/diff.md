# Comparing `tmp/openai_shell_craft-0.6.0.tar.gz` & `tmp/openai_shell_craft-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "openai_shell_craft-0.6.0.tar", last modified: Thu Apr 27 16:14:28 2023, max compression
+gzip compressed data, was "openai_shell_craft-0.7.0.tar", last modified: Sat May 13 16:55:44 2023, max compression
```

## Comparing `openai_shell_craft-0.6.0.tar` & `openai_shell_craft-0.7.0.tar`

### file list

```diff
@@ -1,38 +1,39 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 16:14:28.674135 openai_shell_craft-0.6.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1078 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     8048 2023-04-27 16:14:28.674135 openai_shell_craft-0.6.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     7463 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 16:14:28.670135 openai_shell_craft-0.6.0/openai_shell_craft.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     8048 2023-04-27 16:14:28.000000 openai_shell_craft-0.6.0/openai_shell_craft.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      834 2023-04-27 16:14:28.000000 openai_shell_craft-0.6.0/openai_shell_craft.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-27 16:14:28.000000 openai_shell_craft-0.6.0/openai_shell_craft.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-04-27 16:14:28.000000 openai_shell_craft-0.6.0/openai_shell_craft.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-04-27 16:14:28.000000 openai_shell_craft-0.6.0/openai_shell_craft.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-04-27 16:14:28.000000 openai_shell_craft-0.6.0/openai_shell_craft.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      762 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-27 16:14:28.674135 openai_shell_craft-0.6.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 16:14:28.670135 openai_shell_craft-0.6.0/shell_craft/
--rw-r--r--   0 runner    (1001) docker     (123)     1151 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1188 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/__main__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 16:14:28.674135 openai_shell_craft-0.6.0/shell_craft/cli/
--rw-r--r--   0 runner    (1001) docker     (123)     1159 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1543 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/help.py
--rw-r--r--   0 runner    (1001) docker     (123)     3389 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/key.py
--rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/language.py
--rw-r--r--   0 runner    (1001) docker     (123)     2090 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/main.py
--rw-r--r--   0 runner    (1001) docker     (123)     1769 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/models.py
--rw-r--r--   0 runner    (1001) docker     (123)     7220 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     2650 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/prompt.py
--rw-r--r--   0 runner    (1001) docker     (123)     1593 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2248 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/cli/results.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 16:14:28.674135 openai_shell_craft-0.6.0/shell_craft/factories/
--rw-r--r--   0 runner    (1001) docker     (123)     1179 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/factories/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1951 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/factories/prompt.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 16:14:28.674135 openai_shell_craft-0.6.0/shell_craft/prompts/
--rw-r--r--   0 runner    (1001) docker     (123)     1643 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/prompts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3545 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/prompts/languages.py
--rw-r--r--   0 runner    (1001) docker     (123)     2435 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/prompts/prompt.py
--rw-r--r--   0 runner    (1001) docker     (123)     2277 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/prompts/templates.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     3388 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/shell_craft/service.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 16:14:28.674135 openai_shell_craft-0.6.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1656 2023-04-27 16:14:17.000000 openai_shell_craft-0.6.0/tests/test_factories.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:55:44.777291 openai_shell_craft-0.7.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1078 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     8201 2023-05-13 16:55:44.777291 openai_shell_craft-0.7.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     7616 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:55:44.773290 openai_shell_craft-0.7.0/openai_shell_craft.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     8201 2023-05-13 16:55:44.000000 openai_shell_craft-0.7.0/openai_shell_craft.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      852 2023-05-13 16:55:44.000000 openai_shell_craft-0.7.0/openai_shell_craft.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 16:55:44.000000 openai_shell_craft-0.7.0/openai_shell_craft.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-05-13 16:55:44.000000 openai_shell_craft-0.7.0/openai_shell_craft.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-13 16:55:44.000000 openai_shell_craft-0.7.0/openai_shell_craft.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-13 16:55:44.000000 openai_shell_craft-0.7.0/openai_shell_craft.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      762 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 16:55:44.777291 openai_shell_craft-0.7.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:55:44.773290 openai_shell_craft-0.7.0/shell_craft/
+-rw-r--r--   0 runner    (1001) docker     (123)     1151 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1188 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/__main__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:55:44.773290 openai_shell_craft-0.7.0/shell_craft/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)     1159 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1543 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/help.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3389 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/language.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2397 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1962 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6993 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2650 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/prompt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1593 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2248 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/cli/results.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:55:44.773290 openai_shell_craft-0.7.0/shell_craft/factories/
+-rw-r--r--   0 runner    (1001) docker     (123)     1179 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/factories/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1951 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/factories/prompt.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:55:44.773290 openai_shell_craft-0.7.0/shell_craft/prompts/
+-rw-r--r--   0 runner    (1001) docker     (123)     1643 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/prompts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3545 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/prompts/languages.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2435 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/prompts/prompt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2277 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/prompts/templates.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     3388 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/shell_craft/service.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:55:44.777291 openai_shell_craft-0.7.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1582 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/tests/test_cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1656 2023-05-13 16:55:35.000000 openai_shell_craft-0.7.0/tests/test_factories.py
```

### Comparing `openai_shell_craft-0.6.0/LICENSE` & `openai_shell_craft-0.7.0/LICENSE`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/PKG-INFO` & `openai_shell_craft-0.7.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 Metadata-Version: 2.1
 Name: openai_shell_craft
-Version: 0.6.0
+Version: 0.7.0
 Summary: Generating shell commands and code using natural language models (OpenAI ChatGPT).
 Author-email: Johnathan Irvin <irvinjohnathan@gmail.com>
 Project-URL: Homepage, https://github.com/JohnnyIrvin/shell-craft
 Project-URL: Bug Tracker, https://github.com/JohnnyIrvin/shell-craft/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Shell Craft
 
-[![PyPI version](https://img.shields.io/pypi/v/openai-shell-craft?color=green&label=PyPI)](https://pypi.org/project/openai-shell-craft/)
+[![PyPI version](https://img.shields.io/pypi/v/openai-shell-craft?color=green&label=PyPI)](https://pypi.org/project/openai-shell-craft/) [![codecov](https://codecov.io/gh/JohnnyIrvin/shell-craft/branch/trunk/graph/badge.svg?token=MKYZOJR8SQ)](https://codecov.io/gh/JohnnyIrvin/shell-craft)
 
 Generating shell commands and code using natural language models (OpenAI ChatGPT).
 
 ## Install using Pip
 
 ```sh
 pip install openai-shell-craft
```

### Comparing `openai_shell_craft-0.6.0/README.md` & `openai_shell_craft-0.7.0/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # Shell Craft
 
-[![PyPI version](https://img.shields.io/pypi/v/openai-shell-craft?color=green&label=PyPI)](https://pypi.org/project/openai-shell-craft/)
+[![PyPI version](https://img.shields.io/pypi/v/openai-shell-craft?color=green&label=PyPI)](https://pypi.org/project/openai-shell-craft/) [![codecov](https://codecov.io/gh/JohnnyIrvin/shell-craft/branch/trunk/graph/badge.svg?token=MKYZOJR8SQ)](https://codecov.io/gh/JohnnyIrvin/shell-craft)
 
 Generating shell commands and code using natural language models (OpenAI ChatGPT).
 
 ## Install using Pip
 
 ```sh
 pip install openai-shell-craft
```

### Comparing `openai_shell_craft-0.6.0/openai_shell_craft.egg-info/PKG-INFO` & `openai_shell_craft-0.7.0/openai_shell_craft.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 Metadata-Version: 2.1
 Name: openai-shell-craft
-Version: 0.6.0
+Version: 0.7.0
 Summary: Generating shell commands and code using natural language models (OpenAI ChatGPT).
 Author-email: Johnathan Irvin <irvinjohnathan@gmail.com>
 Project-URL: Homepage, https://github.com/JohnnyIrvin/shell-craft
 Project-URL: Bug Tracker, https://github.com/JohnnyIrvin/shell-craft/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Shell Craft
 
-[![PyPI version](https://img.shields.io/pypi/v/openai-shell-craft?color=green&label=PyPI)](https://pypi.org/project/openai-shell-craft/)
+[![PyPI version](https://img.shields.io/pypi/v/openai-shell-craft?color=green&label=PyPI)](https://pypi.org/project/openai-shell-craft/) [![codecov](https://codecov.io/gh/JohnnyIrvin/shell-craft/branch/trunk/graph/badge.svg?token=MKYZOJR8SQ)](https://codecov.io/gh/JohnnyIrvin/shell-craft)
 
 Generating shell commands and code using natural language models (OpenAI ChatGPT).
 
 ## Install using Pip
 
 ```sh
 pip install openai-shell-craft
```

### Comparing `openai_shell_craft-0.6.0/openai_shell_craft.egg-info/SOURCES.txt` & `openai_shell_craft-0.7.0/openai_shell_craft.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -22,8 +22,9 @@
 shell_craft/cli/results.py
 shell_craft/factories/__init__.py
 shell_craft/factories/prompt.py
 shell_craft/prompts/__init__.py
 shell_craft/prompts/languages.py
 shell_craft/prompts/prompt.py
 shell_craft/prompts/templates.py
+tests/test_cli.py
 tests/test_factories.py
```

### Comparing `openai_shell_craft-0.6.0/pyproject.toml` & `openai_shell_craft-0.7.0/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "openai_shell_craft"
-version = "0.6.0"
+version = "0.7.0"
 authors = [
   { name="Johnathan Irvin", email="irvinjohnathan@gmail.com" },
 ]
 description = "Generating shell commands and code using natural language models (OpenAI ChatGPT)."
 readme = "README.md"
 requires-python = ">=3.9"
 classifiers = [
```

### Comparing `openai_shell_craft-0.6.0/shell_craft/__init__.py` & `openai_shell_craft-0.7.0/shell_craft/__init__.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/__main__.py` & `openai_shell_craft-0.7.0/shell_craft/__main__.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/__init__.py` & `openai_shell_craft-0.7.0/shell_craft/cli/__init__.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/help.py` & `openai_shell_craft-0.7.0/shell_craft/cli/help.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/key.py` & `openai_shell_craft-0.7.0/shell_craft/cli/key.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/language.py` & `openai_shell_craft-0.7.0/shell_craft/cli/language.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/main.py` & `openai_shell_craft-0.7.0/shell_craft/cli/main.py`

 * *Files 14% similar despite different names*

```diff
@@ -14,26 +14,36 @@
 # THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
 # EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
 # MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
 # NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
 # LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
 # OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
 # WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
+from argparse import ArgumentParser
+
 from shell_craft import Service
 from shell_craft.factories import PromptFactory
 
-from .parser import PARSER, get_arguments
+from .parser import get_arguments, initialize_parser
 
 
 def main():
     """
     Main function that processes the command-line arguments and queries the
     OpenAI API using shell_craft.
     """
-    args = get_arguments(PARSER)
+    args = get_arguments(
+        initialize_parser(
+            ArgumentParser(
+                prog="shell-craft",
+                description="Generating shell commands and code using natural language models (OpenAI ChatGPT).",
+                add_help=False
+            )
+        )
+    )
     prompt = PromptFactory.get_prompt(args.prompt)
 
     if getattr(args, "refactor", False):
         prompt = prompt.refactoring
     elif getattr(args, "document", False):
         prompt = prompt.documentation
     elif getattr(args, "test", False):
```

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/models.py` & `openai_shell_craft-0.7.0/shell_craft/cli/request.py`

 * *Files 12% similar despite different names*

```diff
@@ -19,22 +19,19 @@
 # OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
 # WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
 from argparse import ArgumentParser
 
 
 def add_arguments(parser: ArgumentParser):
     """
-    Adds '--model' argument to the parser. This argument is used to specify
-    openai's model to use. The default is 'gpt-3.5-turbo'. This argument is
-    optional. The models are provided by the OpenAI API but not all models
-    are available to all users. Nor are all models implemented in the
-    shell_craft library.
+    Adds 'request' argument to the parser. This argument is used to
+    specify the input to prompt the API with. This argument is required,
+    however, it can be piped in from another command or from a file.
 
     Args:
         parser (ArgumentParser): The parser to add the argument to.
     """    
     parser.add_argument(
-        "--model",
+        "request",
         type=str,
-        default="gpt-3.5-turbo",
-        help="The input to prompt the API with.",
+        nargs="*",
     )
```

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/parser.py` & `openai_shell_craft-0.7.0/shell_craft/cli/parser.py`

 * *Files 3% similar despite different names*

```diff
@@ -170,20 +170,11 @@
 
     if not stdin.isatty():
         stdin.flush()
         arguments += stdin.readlines()
 
     return parser.parse_args(arguments)
 
-PARSER = initialize_parser(
-    ArgumentParser(
-        prog="shell-craft",
-        description="Generating shell commands and code using natural language models (OpenAI ChatGPT).",
-        add_help=False
-    )
-)
-
 __all__ = [
     "get_arguments",
-    "PARSER"
 ]
```

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/prompt.py` & `openai_shell_craft-0.7.0/shell_craft/cli/prompt.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/request.py` & `openai_shell_craft-0.7.0/shell_craft/cli/results.py`

 * *Files 20% similar despite different names*

```diff
@@ -14,24 +14,48 @@
 # THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
 # EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
 # MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
 # NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
 # LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
 # OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
 # WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
-from argparse import ArgumentParser
+from argparse import ArgumentParser, ArgumentTypeError
+
+def limited_float(min: float, max: float):
+    def _ret_func(arg: str):
+        if not str(arg).isdecimal:
+            raise ArgumentTypeError(f"{arg} is not a decimal")
+        
+        f = float(arg)
+        if f < min or f > max:
+            raise ArgumentTypeError(f"{arg} is not between {min} and {max}")
+        
+        return f
+    
+    return _ret_func
 
 
 def add_arguments(parser: ArgumentParser):
     """
-    Adds 'request' argument to the parser. This argument is used to
-    specify the input to prompt the API with. This argument is required,
-    however, it can be piped in from another command or from a file.
+    Adds arguments that effect the results of the openai api call.
+
+    '--count (-c)' is used to specify the number of results to return.
+    '--temperature (-t)' is used to specify the sampling temperature to use.
 
     Args:
-        parser (ArgumentParser): The parser to add the argument to.
+        parser (ArgumentParser): The parser to add the arguments to.
     """    
     parser.add_argument(
-        "request",
-        type=str,
-        nargs="*",
+        "-c",
+        "--count",
+        type=int,
+        default=1,
+        help="The number of results to return.",
     )
+
+    parser.add_argument(
+        "-t",
+        "--temperature",
+        type=limited_float(0.0, 2.0),
+        default=1.0,
+        help="The sampling temperature to use. Must be between 0 and 2.",
+    )
```

### Comparing `openai_shell_craft-0.6.0/shell_craft/cli/results.py` & `openai_shell_craft-0.7.0/shell_craft/cli/models.py`

 * *Files 22% similar despite different names*

```diff
@@ -14,48 +14,35 @@
 # THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
 # EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
 # MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
 # NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
 # LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
 # OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
 # WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
-from argparse import ArgumentParser, ArgumentTypeError
-
-def limited_float(min: float, max: float):
-    def _ret_func(arg: str):
-        if not str(arg).isdecimal:
-            raise ArgumentTypeError(f"{arg} is not a decimal")
-        
-        f = float(arg)
-        if f < min or f > max:
-            raise ArgumentTypeError(f"{arg} is not between {min} and {max}")
-        
-        return f
-    
-    return _ret_func
+from argparse import ArgumentParser
 
 
 def add_arguments(parser: ArgumentParser):
     """
-    Adds arguments that effect the results of the openai api call.
-
-    '--count (-c)' is used to specify the number of results to return.
-    '--temperature (-t)' is used to specify the sampling temperature to use.
+    Adds '--model' argument to the parser. This argument is used to specify
+    openai's model to use. The default is 'gpt-3.5-turbo'. This argument is
+    optional. The models are provided by the OpenAI API but not all models
+    are available to all users. Nor are all models implemented in the
+    shell_craft library.
 
     Args:
-        parser (ArgumentParser): The parser to add the arguments to.
+        parser (ArgumentParser): The parser to add the argument to.
     """    
     parser.add_argument(
-        "-c",
-        "--count",
-        type=int,
-        default=1,
-        help="The number of results to return.",
+        "--model",
+        type=str,
+        default="gpt-3.5-turbo",
+        help="The input to prompt the API with.",
+        choices=[
+            "gpt-4",
+            "gpt-4-0314",
+            "gpt-4-32k",
+            "gpt-4-32k-0314",
+            "gpt-3.5-turbo",
+            "gpt-3.5-turbo-0301",
+        ]
     )
-
-    parser.add_argument(
-        "-t",
-        "--temperature",
-        type=limited_float(0.0, 2.0),
-        default=1.0,
-        help="The sampling temperature to use. Must be between 0 and 2.",
-    )
```

### Comparing `openai_shell_craft-0.6.0/shell_craft/factories/__init__.py` & `openai_shell_craft-0.7.0/shell_craft/factories/__init__.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/factories/prompt.py` & `openai_shell_craft-0.7.0/shell_craft/factories/prompt.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/prompts/__init__.py` & `openai_shell_craft-0.7.0/shell_craft/prompts/__init__.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/prompts/languages.py` & `openai_shell_craft-0.7.0/shell_craft/prompts/languages.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/prompts/prompt.py` & `openai_shell_craft-0.7.0/shell_craft/prompts/prompt.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/prompts/templates.py` & `openai_shell_craft-0.7.0/shell_craft/prompts/templates.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/shell_craft/service.py` & `openai_shell_craft-0.7.0/shell_craft/service.py`

 * *Files identical despite different names*

### Comparing `openai_shell_craft-0.6.0/tests/test_factories.py` & `openai_shell_craft-0.7.0/tests/test_factories.py`

 * *Files identical despite different names*

