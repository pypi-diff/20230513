# Comparing `tmp/prr-0.2.1.tar.gz` & `tmp/prr-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "prr-0.2.1.tar", max compression
+gzip compressed data, was "prr-0.2.2.tar", max compression
```

## Comparing `prr-0.2.1.tar` & `prr-0.2.2.tar`

### file list

```diff
@@ -1,20 +1,20 @@
--rw-r--r--   0        0        0     1074 2023-05-07 19:46:47.449469 prr-0.2.1/LICENSE
--rw-r--r--   0        0        0    18072 2023-05-11 16:48:22.364108 prr-0.2.1/README.md
--rwxr-xr-x   0        0        0     2621 2023-05-11 16:48:22.364465 prr-0.2.1/prr/__init__.py
--rw-r--r--   0        0        0      143 2023-05-11 16:48:22.364670 prr-0.2.1/prr/config.py
--rw-r--r--   0        0        0      931 2023-05-11 16:48:21.982369 prr-0.2.1/prr/options.py
--rw-r--r--   0        0        0     7489 2023-05-11 16:48:21.982538 prr-0.2.1/prr/prompt.py
--rw-r--r--   0        0        0      644 2023-05-11 16:48:21.982660 prr-0.2.1/prr/prompt_run.py
--rw-r--r--   0        0        0      954 2023-05-11 16:48:21.982771 prr-0.2.1/prr/prompt_run_result.py
--rw-r--r--   0        0        0      886 2023-05-11 16:48:21.982881 prr-0.2.1/prr/request.py
--rw-r--r--   0        0        0      810 2023-05-11 16:48:21.982989 prr-0.2.1/prr/response.py
--rw-r--r--   0        0        0     1086 2023-05-11 16:48:21.983099 prr-0.2.1/prr/runner.py
--rw-r--r--   0        0        0     2797 2023-05-11 16:48:21.983230 prr-0.2.1/prr/saver.py
--rw-r--r--   0        0        0      486 2023-05-11 16:48:21.983364 prr-0.2.1/prr/service_config.py
--rw-r--r--   0        0        0      634 2023-05-11 16:48:21.983486 prr-0.2.1/prr/service_registry.py
--rw-r--r--   0        0        0     2343 2023-05-11 16:48:22.365057 prr-0.2.1/prr/services/providers/anthropic/complete.py
--rw-r--r--   0        0        0     1684 2023-05-11 16:48:22.365446 prr-0.2.1/prr/services/providers/openai/chat.py
--rwxr-xr-x   0        0        0     4293 2023-05-11 16:48:22.365824 prr-0.2.1/prr/utils/run.py
--rwxr-xr-x   0        0        0     2333 2023-05-11 16:48:22.366102 prr-0.2.1/prr/utils/watch.py
--rw-r--r--   0        0        0      807 2023-05-11 16:48:22.366351 prr-0.2.1/pyproject.toml
--rw-r--r--   0        0        0    18807 1970-01-01 00:00:00.000000 prr-0.2.1/PKG-INFO
+-rw-r--r--   0        0        0     1074 2023-05-07 19:46:47.449469 prr-0.2.2/LICENSE
+-rw-r--r--   0        0        0    18186 2023-05-12 09:06:58.754836 prr-0.2.2/README.md
+-rwxr-xr-x   0        0        0     2621 2023-05-12 09:06:58.755131 prr-0.2.2/prr/__init__.py
+-rw-r--r--   0        0        0      143 2023-05-12 09:06:58.755478 prr-0.2.2/prr/config.py
+-rw-r--r--   0        0        0      931 2023-05-12 09:06:58.755747 prr-0.2.2/prr/options.py
+-rw-r--r--   0        0        0     7489 2023-05-12 09:06:58.755911 prr-0.2.2/prr/prompt.py
+-rw-r--r--   0        0        0      644 2023-05-12 09:06:58.756020 prr-0.2.2/prr/prompt_run.py
+-rw-r--r--   0        0        0      954 2023-05-12 09:06:58.756155 prr-0.2.2/prr/prompt_run_result.py
+-rw-r--r--   0        0        0      886 2023-05-12 09:06:58.756267 prr-0.2.2/prr/request.py
+-rw-r--r--   0        0        0      810 2023-05-12 09:06:58.756379 prr-0.2.2/prr/response.py
+-rw-r--r--   0        0        0     1086 2023-05-12 09:06:58.756486 prr-0.2.2/prr/runner.py
+-rw-r--r--   0        0        0     2797 2023-05-12 09:06:58.756591 prr-0.2.2/prr/saver.py
+-rw-r--r--   0        0        0      486 2023-05-12 09:06:58.756697 prr-0.2.2/prr/service_config.py
+-rw-r--r--   0        0        0      634 2023-05-12 09:06:58.757233 prr-0.2.2/prr/service_registry.py
+-rw-r--r--   0        0        0     2343 2023-05-12 09:06:58.757749 prr-0.2.2/prr/services/providers/anthropic/complete.py
+-rw-r--r--   0        0        0     1726 2023-05-13 08:10:45.786625 prr-0.2.2/prr/services/providers/openai/chat.py
+-rwxr-xr-x   0        0        0     4293 2023-05-12 09:06:58.758300 prr-0.2.2/prr/utils/run.py
+-rwxr-xr-x   0        0        0     2333 2023-05-12 09:06:58.758555 prr-0.2.2/prr/utils/watch.py
+-rw-r--r--   0        0        0      807 2023-05-13 08:10:12.716396 prr-0.2.2/pyproject.toml
+-rw-r--r--   0        0        0    18921 1970-01-01 00:00:00.000000 prr-0.2.2/PKG-INFO
```

### Comparing `prr-0.2.1/LICENSE` & `prr-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/README.md` & `prr-0.2.2/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -48,77 +48,42 @@
 - [ ] Support evaluating prompt outputs for quality by LLMs themselves
 - [ ] Support for streaming responses
 - [ ] Support for running prompts in parallel
 - [ ] Support for calculating pricing for prompts based on defined pricelist
 - [ ] Allow for specifying how many times to run each service to ensure statistically relevant-ish performance results
 - [ ] Prompt fine-tuning tooling
 - [ ] Support multiple completions
+- [ ] Support `.env` file for configuration from current directory (or any other as `--config` option)
 
 
 ## Getting started
 
 Here's a quick run through on what you need to know to use `prr` effectively.
 
 ### Installation & configuration
 Install it via `pip` 
 ```sh
 $ pip install prr
 ```
 
-Copy `.env.example` - and save it as `.env`. Fill in your API keys for OpenAI, Anthropic and others:
+Check `.env.example` - and save it as `~/.prr_rc`. Fill in your API keys for OpenAI, Anthropic and others:
 
 ```bash
 # https://platform.openai.com/account/api-keys
 OPENAI_API_KEY="sk-..."
 
 # https://console.anthropic.com/account/keys
 ANTHROPIC_API_KEY="sk-ant-..."
 
 DEFAULT_SERVICE="openai/chat/gpt-3.5-turbo"
 ```
 
 You can also use DEFAULT_SERVICE to specify the model you want to use by default, but otherwise you're good to go!
 
 
-## Development
-
-
-1. Clone the repo
-
-```sh
-$ git clone https://github.com/Forward-Operators/prr.git
-```
-
-2. Make sure you have Python 3.9 or 3.10 installed. If you need to have multiple Python versions in your system, consider using [asdf](https://github.com/asdf-vm/asdf).
-
-3. Install the required packages:
-This project uses Poetry. See [how to install](https://python-poetry.org/docs/#installation) it. 
-
-```sh
-poetry shell
-poetry install
-```
-It will install `prr` executable file in your active python environment.
-
-4. Setup your API keys
-
-Copy `.env.example` - and save it as `.env`. Fill in your API keys for OpenAI, Anthropic and others:
-
-```bash
-# https://platform.openai.com/account/api-keys
-OPENAI_API_KEY="sk-..."
-
-# https://console.anthropic.com/account/keys
-ANTHROPIC_API_KEY="sk-ant-..."
-
-DEFAULT_SERVICE="openai/chat/gpt-3.5-turbo"
-```
-
-You can also use DEFAULT_SERVICE to specify the model you want to use by default, but otherwise you're good to go!
-
 ### Run a prompt from a simple text file containing just a prompt
 
 Let's create a simple text file and call it `dingo` with the following content:
 
 ```text
 What are key traits of a Dingo dog?
 ```
@@ -408,14 +373,50 @@
 ## Available models
 
 ### Current integrations
 
 * OpenAI/chat - https://platform.openai.com/docs/guides/chat
 * Anthropic/complete - https://console.anthropic.com/docs/api
 
+## Development
+
+1. Clone the repo
+
+```sh
+$ git clone https://github.com/Forward-Operators/prr.git
+```
+
+2. Make sure you have Python 3.9 or 3.10 installed. If you need to have multiple Python versions in your system, consider using [asdf](https://github.com/asdf-vm/asdf).
+
+3. Install the required packages:
+This project uses Poetry. See [how to install](https://python-poetry.org/docs/#installation) it. 
+
+```sh
+poetry shell
+poetry install
+```
+It will install `prr` executable file in your active python environment.
+
+4. Setup your API keys
+
+Copy `.env.example` - and save it as `~/.prr_rc`. Fill in your API keys for OpenAI, Anthropic and others:
+
+```bash
+# https://platform.openai.com/account/api-keys
+OPENAI_API_KEY="sk-..."
+
+# https://console.anthropic.com/account/keys
+ANTHROPIC_API_KEY="sk-ant-..."
+
+DEFAULT_SERVICE="openai/chat/gpt-3.5-turbo"
+```
+
+You can also use DEFAULT_SERVICE to specify the model you want to use by default, but otherwise you're good to go!
+
+
 ## Contributing
 
 We'd love your help in making Prr even better! To contribute, please follow these steps:
 
 1. Fork the repo
 2. Create a new branch
 3. Install pre-commit - `pre-commit install`
```

### Comparing `prr-0.2.1/prr/__init__.py` & `prr-0.2.2/prr/__init__.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/options.py` & `prr-0.2.2/prr/options.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/prompt.py` & `prr-0.2.2/prr/prompt.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/prompt_run.py` & `prr-0.2.2/prr/prompt_run.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/prompt_run_result.py` & `prr-0.2.2/prr/prompt_run_result.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/request.py` & `prr-0.2.2/prr/request.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/response.py` & `prr-0.2.2/prr/response.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/runner.py` & `prr-0.2.2/prr/runner.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/saver.py` & `prr-0.2.2/prr/saver.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/service_registry.py` & `prr-0.2.2/prr/service_registry.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/services/providers/anthropic/complete.py` & `prr-0.2.2/prr/services/providers/anthropic/complete.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/services/providers/openai/chat.py` & `prr-0.2.2/prr/services/providers/openai/chat.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 import openai
 
 from prr.config import load_config
 from prr.request import ServiceRequest
 from prr.response import ServiceResponse
 
 config = load_config()
+openai.api_key = config["OPENAI_API_KEY"]
 
 
 # OpenAI model provider class
 class ServiceOpenAIChat:
     provider = "openai"
     service = "chat"
```

### Comparing `prr-0.2.1/prr/utils/run.py` & `prr-0.2.2/prr/utils/run.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/prr/utils/watch.py` & `prr-0.2.2/prr/utils/watch.py`

 * *Files identical despite different names*

### Comparing `prr-0.2.1/pyproject.toml` & `prr-0.2.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "prr"
-version = "0.2.1"
+version = "0.2.2"
 description = "prr - command-line LLM prompt runner"
 authors = [ "Zbigniew Sobiecki <zbigniew@fwdoperators.com>" , "Mateusz Kozak <mateusz@fwdoperators.com>" ]
 license = "MIT"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.9"
```

### Comparing `prr-0.2.1/PKG-INFO` & `prr-0.2.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: prr
-Version: 0.2.1
+Version: 0.2.2
 Summary: prr - command-line LLM prompt runner
 License: MIT
 Author: Zbigniew Sobiecki
 Author-email: zbigniew@fwdoperators.com
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -69,77 +69,42 @@
 - [ ] Support evaluating prompt outputs for quality by LLMs themselves
 - [ ] Support for streaming responses
 - [ ] Support for running prompts in parallel
 - [ ] Support for calculating pricing for prompts based on defined pricelist
 - [ ] Allow for specifying how many times to run each service to ensure statistically relevant-ish performance results
 - [ ] Prompt fine-tuning tooling
 - [ ] Support multiple completions
+- [ ] Support `.env` file for configuration from current directory (or any other as `--config` option)
 
 
 ## Getting started
 
 Here's a quick run through on what you need to know to use `prr` effectively.
 
 ### Installation & configuration
 Install it via `pip` 
 ```sh
 $ pip install prr
 ```
 
-Copy `.env.example` - and save it as `.env`. Fill in your API keys for OpenAI, Anthropic and others:
+Check `.env.example` - and save it as `~/.prr_rc`. Fill in your API keys for OpenAI, Anthropic and others:
 
 ```bash
 # https://platform.openai.com/account/api-keys
 OPENAI_API_KEY="sk-..."
 
 # https://console.anthropic.com/account/keys
 ANTHROPIC_API_KEY="sk-ant-..."
 
 DEFAULT_SERVICE="openai/chat/gpt-3.5-turbo"
 ```
 
 You can also use DEFAULT_SERVICE to specify the model you want to use by default, but otherwise you're good to go!
 
 
-## Development
-
-
-1. Clone the repo
-
-```sh
-$ git clone https://github.com/Forward-Operators/prr.git
-```
-
-2. Make sure you have Python 3.9 or 3.10 installed. If you need to have multiple Python versions in your system, consider using [asdf](https://github.com/asdf-vm/asdf).
-
-3. Install the required packages:
-This project uses Poetry. See [how to install](https://python-poetry.org/docs/#installation) it. 
-
-```sh
-poetry shell
-poetry install
-```
-It will install `prr` executable file in your active python environment.
-
-4. Setup your API keys
-
-Copy `.env.example` - and save it as `.env`. Fill in your API keys for OpenAI, Anthropic and others:
-
-```bash
-# https://platform.openai.com/account/api-keys
-OPENAI_API_KEY="sk-..."
-
-# https://console.anthropic.com/account/keys
-ANTHROPIC_API_KEY="sk-ant-..."
-
-DEFAULT_SERVICE="openai/chat/gpt-3.5-turbo"
-```
-
-You can also use DEFAULT_SERVICE to specify the model you want to use by default, but otherwise you're good to go!
-
 ### Run a prompt from a simple text file containing just a prompt
 
 Let's create a simple text file and call it `dingo` with the following content:
 
 ```text
 What are key traits of a Dingo dog?
 ```
@@ -429,14 +394,50 @@
 ## Available models
 
 ### Current integrations
 
 * OpenAI/chat - https://platform.openai.com/docs/guides/chat
 * Anthropic/complete - https://console.anthropic.com/docs/api
 
+## Development
+
+1. Clone the repo
+
+```sh
+$ git clone https://github.com/Forward-Operators/prr.git
+```
+
+2. Make sure you have Python 3.9 or 3.10 installed. If you need to have multiple Python versions in your system, consider using [asdf](https://github.com/asdf-vm/asdf).
+
+3. Install the required packages:
+This project uses Poetry. See [how to install](https://python-poetry.org/docs/#installation) it. 
+
+```sh
+poetry shell
+poetry install
+```
+It will install `prr` executable file in your active python environment.
+
+4. Setup your API keys
+
+Copy `.env.example` - and save it as `~/.prr_rc`. Fill in your API keys for OpenAI, Anthropic and others:
+
+```bash
+# https://platform.openai.com/account/api-keys
+OPENAI_API_KEY="sk-..."
+
+# https://console.anthropic.com/account/keys
+ANTHROPIC_API_KEY="sk-ant-..."
+
+DEFAULT_SERVICE="openai/chat/gpt-3.5-turbo"
+```
+
+You can also use DEFAULT_SERVICE to specify the model you want to use by default, but otherwise you're good to go!
+
+
 ## Contributing
 
 We'd love your help in making Prr even better! To contribute, please follow these steps:
 
 1. Fork the repo
 2. Create a new branch
 3. Install pre-commit - `pre-commit install`
```

