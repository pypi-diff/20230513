# Comparing `tmp/prr-0.2.2.tar.gz` & `tmp/prr-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "prr-0.2.2.tar", max compression
+gzip compressed data, was "prr-0.2.3.tar", max compression
```

## Comparing `prr-0.2.2.tar` & `prr-0.2.3.tar`

### file list

```diff
@@ -1,20 +1,21 @@
--rw-r--r--   0        0        0     1074 2023-05-07 19:46:47.449469 prr-0.2.2/LICENSE
--rw-r--r--   0        0        0    18186 2023-05-12 09:06:58.754836 prr-0.2.2/README.md
--rwxr-xr-x   0        0        0     2621 2023-05-12 09:06:58.755131 prr-0.2.2/prr/__init__.py
--rw-r--r--   0        0        0      143 2023-05-12 09:06:58.755478 prr-0.2.2/prr/config.py
--rw-r--r--   0        0        0      931 2023-05-12 09:06:58.755747 prr-0.2.2/prr/options.py
--rw-r--r--   0        0        0     7489 2023-05-12 09:06:58.755911 prr-0.2.2/prr/prompt.py
--rw-r--r--   0        0        0      644 2023-05-12 09:06:58.756020 prr-0.2.2/prr/prompt_run.py
--rw-r--r--   0        0        0      954 2023-05-12 09:06:58.756155 prr-0.2.2/prr/prompt_run_result.py
--rw-r--r--   0        0        0      886 2023-05-12 09:06:58.756267 prr-0.2.2/prr/request.py
--rw-r--r--   0        0        0      810 2023-05-12 09:06:58.756379 prr-0.2.2/prr/response.py
--rw-r--r--   0        0        0     1086 2023-05-12 09:06:58.756486 prr-0.2.2/prr/runner.py
--rw-r--r--   0        0        0     2797 2023-05-12 09:06:58.756591 prr-0.2.2/prr/saver.py
--rw-r--r--   0        0        0      486 2023-05-12 09:06:58.756697 prr-0.2.2/prr/service_config.py
--rw-r--r--   0        0        0      634 2023-05-12 09:06:58.757233 prr-0.2.2/prr/service_registry.py
--rw-r--r--   0        0        0     2343 2023-05-12 09:06:58.757749 prr-0.2.2/prr/services/providers/anthropic/complete.py
--rw-r--r--   0        0        0     1726 2023-05-13 08:10:45.786625 prr-0.2.2/prr/services/providers/openai/chat.py
--rwxr-xr-x   0        0        0     4293 2023-05-12 09:06:58.758300 prr-0.2.2/prr/utils/run.py
--rwxr-xr-x   0        0        0     2333 2023-05-12 09:06:58.758555 prr-0.2.2/prr/utils/watch.py
--rw-r--r--   0        0        0      807 2023-05-13 08:10:12.716396 prr-0.2.2/pyproject.toml
--rw-r--r--   0        0        0    18921 1970-01-01 00:00:00.000000 prr-0.2.2/PKG-INFO
+-rw-r--r--   0        0        0     1074 2023-05-07 19:46:47.449469 prr-0.2.3/LICENSE
+-rw-r--r--   0        0        0    18287 2023-05-13 08:41:24.219498 prr-0.2.3/README.md
+-rwxr-xr-x   0        0        0        0 2023-05-13 08:35:38.815655 prr-0.2.3/prr/__init__.py
+-rwxr-xr-x   0        0        0     2556 2023-05-13 08:37:47.287713 prr-0.2.3/prr/__main__.py
+-rw-r--r--   0        0        0      143 2023-05-12 09:06:58.755478 prr-0.2.3/prr/config.py
+-rw-r--r--   0        0        0      931 2023-05-12 09:06:58.755747 prr-0.2.3/prr/options.py
+-rw-r--r--   0        0        0     7489 2023-05-12 09:06:58.755911 prr-0.2.3/prr/prompt.py
+-rw-r--r--   0        0        0      644 2023-05-12 09:06:58.756020 prr-0.2.3/prr/prompt_run.py
+-rw-r--r--   0        0        0      954 2023-05-12 09:06:58.756155 prr-0.2.3/prr/prompt_run_result.py
+-rw-r--r--   0        0        0      886 2023-05-12 09:06:58.756267 prr-0.2.3/prr/request.py
+-rw-r--r--   0        0        0      810 2023-05-12 09:06:58.756379 prr-0.2.3/prr/response.py
+-rw-r--r--   0        0        0     1086 2023-05-12 09:06:58.756486 prr-0.2.3/prr/runner.py
+-rw-r--r--   0        0        0     2797 2023-05-12 09:06:58.756591 prr-0.2.3/prr/saver.py
+-rw-r--r--   0        0        0      486 2023-05-12 09:06:58.756697 prr-0.2.3/prr/service_config.py
+-rw-r--r--   0        0        0      634 2023-05-12 09:06:58.757233 prr-0.2.3/prr/service_registry.py
+-rw-r--r--   0        0        0     2343 2023-05-12 09:06:58.757749 prr-0.2.3/prr/services/providers/anthropic/complete.py
+-rw-r--r--   0        0        0     1726 2023-05-13 08:10:45.786625 prr-0.2.3/prr/services/providers/openai/chat.py
+-rwxr-xr-x   0        0        0     4293 2023-05-12 09:06:58.758300 prr-0.2.3/prr/utils/run.py
+-rwxr-xr-x   0        0        0     2333 2023-05-12 09:06:58.758555 prr-0.2.3/prr/utils/watch.py
+-rw-r--r--   0        0        0      816 2023-05-13 08:40:07.365411 prr-0.2.3/pyproject.toml
+-rw-r--r--   0        0        0    19022 1970-01-01 00:00:00.000000 prr-0.2.3/PKG-INFO
```

### Comparing `prr-0.2.2/LICENSE` & `prr-0.2.3/LICENSE`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/README.md` & `prr-0.2.3/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -408,14 +408,16 @@
 ANTHROPIC_API_KEY="sk-ant-..."
 
 DEFAULT_SERVICE="openai/chat/gpt-3.5-turbo"
 ```
 
 You can also use DEFAULT_SERVICE to specify the model you want to use by default, but otherwise you're good to go!
 
+If you'd like to run this code during developmnent, you can use `python -m prr` to load the module.
+
 
 ## Contributing
 
 We'd love your help in making Prr even better! To contribute, please follow these steps:
 
 1. Fork the repo
 2. Create a new branch
```

### Comparing `prr-0.2.2/prr/__init__.py` & `prr-0.2.3/prr/__main__.py`

 * *Files 5% similar despite different names*

```diff
@@ -5,17 +5,14 @@
 import sys
 
 from prr.config import load_config
 
 from .utils.run import RunPromptCommand
 from .utils.watch import WatchPromptCommand
 
-# sys.path.append(".")
-
-
 config = load_config()
 
 
 def main():
     parser = argparse.ArgumentParser(
         description="Run a prompt against configured models.",
         prog="prr",
@@ -84,11 +81,7 @@
     if parsed_args["command"] == "run":
         command = RunPromptCommand(parsed_args)
         command.run_prompt()
 
     if parsed_args["command"] == "watch":
         command = WatchPromptCommand(parsed_args)
         command.watch_prompt()
-
-
-if __name__ == "__main__":
-    main()
```

### Comparing `prr-0.2.2/prr/options.py` & `prr-0.2.3/prr/options.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/prompt.py` & `prr-0.2.3/prr/prompt.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/prompt_run.py` & `prr-0.2.3/prr/prompt_run.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/prompt_run_result.py` & `prr-0.2.3/prr/prompt_run_result.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/request.py` & `prr-0.2.3/prr/request.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/response.py` & `prr-0.2.3/prr/response.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/runner.py` & `prr-0.2.3/prr/runner.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/saver.py` & `prr-0.2.3/prr/saver.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/service_registry.py` & `prr-0.2.3/prr/service_registry.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/services/providers/anthropic/complete.py` & `prr-0.2.3/prr/services/providers/anthropic/complete.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/services/providers/openai/chat.py` & `prr-0.2.3/prr/services/providers/openai/chat.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/utils/run.py` & `prr-0.2.3/prr/utils/run.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/prr/utils/watch.py` & `prr-0.2.3/prr/utils/watch.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.2/pyproject.toml` & `prr-0.2.3/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "prr"
-version = "0.2.2"
+version = "0.2.3"
 description = "prr - command-line LLM prompt runner"
 authors = [ "Zbigniew Sobiecki <zbigniew@fwdoperators.com>" , "Mateusz Kozak <mateusz@fwdoperators.com>" ]
 license = "MIT"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.9"
@@ -17,15 +17,15 @@
 
 [tool.poetry.dev-dependencies]
 pre-commit = "^2.12.0"
 black = "^23.3.0"
 isort = "^5.12.0"
 
 [tool.poetry.scripts]
-prr = { callable = "prr:main" }
+prr = { callable = "prr:__main__.main" }
 
 [tool.isort]
 # https://pycqa.github.io/isort/docs/configuration/black_compatibility/
 profile = "black"
 
 [project.urls]
 Homepage = "https://github.com/Forward-Operators/prr"
```

### Comparing `prr-0.2.2/PKG-INFO` & `prr-0.2.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: prr
-Version: 0.2.2
+Version: 0.2.3
 Summary: prr - command-line LLM prompt runner
 License: MIT
 Author: Zbigniew Sobiecki
 Author-email: zbigniew@fwdoperators.com
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -429,14 +429,16 @@
 ANTHROPIC_API_KEY="sk-ant-..."
 
 DEFAULT_SERVICE="openai/chat/gpt-3.5-turbo"
 ```
 
 You can also use DEFAULT_SERVICE to specify the model you want to use by default, but otherwise you're good to go!
 
+If you'd like to run this code during developmnent, you can use `python -m prr` to load the module.
+
 
 ## Contributing
 
 We'd love your help in making Prr even better! To contribute, please follow these steps:
 
 1. Fork the repo
 2. Create a new branch
```

