# Comparing `tmp/fastapi_async_langchain-0.5.2.tar.gz` & `tmp/fastapi_async_langchain-0.5.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fastapi_async_langchain-0.5.2.tar", max compression
+gzip compressed data, was "fastapi_async_langchain-0.5.3.tar", max compression
```

## Comparing `fastapi_async_langchain-0.5.2.tar` & `fastapi_async_langchain-0.5.3.tar`

### file list

```diff
@@ -1,19 +1,19 @@
--rw-r--r--   0        0        0     1073 2023-05-11 07:44:57.359675 fastapi_async_langchain-0.5.2/LICENSE
--rw-r--r--   0        0        0     2938 2023-05-11 07:44:57.359675 fastapi_async_langchain-0.5.2/README.md
--rw-r--r--   0        0        0        0 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/__init__.py
--rw-r--r--   0        0        0     2326 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/__init__.py
--rw-r--r--   0        0        0      956 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/base.py
--rw-r--r--   0        0        0     1389 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/llm.py
--rw-r--r--   0        0        0     2704 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/qa_with_sources.py
--rw-r--r--   0        0        0     2882 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/retrieval_qa.py
--rw-r--r--   0        0        0     1332 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/register.py
--rw-r--r--   0        0        0       74 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/responses/__init__.py
--rw-r--r--   0        0        0     2787 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/responses/streaming.py
--rw-r--r--   0        0        0      536 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/schemas.py
--rw-r--r--   0        0        0       69 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/testing/__init__.py
--rw-r--r--   0        0        0     2496 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/testing/gradio.py
--rw-r--r--   0        0        0      391 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/testing/settings.py
--rw-r--r--   0        0        0       73 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/websockets/__init__.py
--rw-r--r--   0        0        0     3661 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/fastapi_async_langchain/websockets/base.py
--rw-r--r--   0        0        0      705 2023-05-11 07:44:57.543677 fastapi_async_langchain-0.5.2/pyproject.toml
--rw-r--r--   0        0        0     3787 1970-01-01 00:00:00.000000 fastapi_async_langchain-0.5.2/PKG-INFO
+-rw-r--r--   0        0        0     1073 2023-05-12 15:29:38.403779 fastapi_async_langchain-0.5.3/LICENSE
+-rw-r--r--   0        0        0     2938 2023-05-12 15:29:38.403779 fastapi_async_langchain-0.5.3/README.md
+-rw-r--r--   0        0        0        0 2023-05-12 15:29:38.607778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/__init__.py
+-rw-r--r--   0        0        0     2326 2023-05-12 15:29:38.607778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/__init__.py
+-rw-r--r--   0        0        0      956 2023-05-12 15:29:38.607778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/base.py
+-rw-r--r--   0        0        0     1389 2023-05-12 15:29:38.607778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/llm.py
+-rw-r--r--   0        0        0     2704 2023-05-12 15:29:38.607778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/qa_with_sources.py
+-rw-r--r--   0        0        0     2882 2023-05-12 15:29:38.607778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/retrieval_qa.py
+-rw-r--r--   0        0        0     1332 2023-05-12 15:29:38.607778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/register.py
+-rw-r--r--   0        0        0       74 2023-05-12 15:29:38.607778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/responses/__init__.py
+-rw-r--r--   0        0        0     2787 2023-05-12 15:29:38.611778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/responses/streaming.py
+-rw-r--r--   0        0        0      536 2023-05-12 15:29:38.611778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/schemas.py
+-rw-r--r--   0        0        0       69 2023-05-12 15:29:38.611778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/testing/__init__.py
+-rw-r--r--   0        0        0     2496 2023-05-12 15:29:38.611778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/testing/gradio.py
+-rw-r--r--   0        0        0      391 2023-05-12 15:29:38.611778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/testing/settings.py
+-rw-r--r--   0        0        0       73 2023-05-12 15:29:38.611778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/websockets/__init__.py
+-rw-r--r--   0        0        0     3661 2023-05-12 15:29:38.611778 fastapi_async_langchain-0.5.3/fastapi_async_langchain/websockets/base.py
+-rw-r--r--   0        0        0      706 2023-05-12 15:29:38.611778 fastapi_async_langchain-0.5.3/pyproject.toml
+-rw-r--r--   0        0        0     3778 1970-01-01 00:00:00.000000 fastapi_async_langchain-0.5.3/PKG-INFO
```

### Comparing `fastapi_async_langchain-0.5.2/LICENSE` & `fastapi_async_langchain-0.5.3/LICENSE`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/README.md` & `fastapi_async_langchain-0.5.3/README.md`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/__init__.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/__init__.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/base.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/base.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/llm.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/llm.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/qa_with_sources.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/qa_with_sources.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/callbacks/retrieval_qa.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/callbacks/retrieval_qa.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/register.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/register.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/responses/streaming.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/responses/streaming.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/schemas.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/schemas.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/testing/gradio.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/testing/gradio.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/fastapi_async_langchain/websockets/base.py` & `fastapi_async_langchain-0.5.3/fastapi_async_langchain/websockets/base.py`

 * *Files identical despite different names*

### Comparing `fastapi_async_langchain-0.5.2/pyproject.toml` & `fastapi_async_langchain-0.5.3/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [tool.poetry]
 name = "fastapi-async-langchain"
-version = "0.5.2"
+version = "0.5.3"
 description = "Ship production-ready LangChain projects with FastAPI"
 authors = ["Ajinkya Indulkar <26824103+ajndkr@users.noreply.github.com>"]
 readme = "README.md"
 homepage = "https://github.com/ajndkr/fastapi-async-langchain"
 repository = "https://github.com/ajndkr/fastapi-async-langchain"
 license = "MIT"
 packages = [{include = "fastapi_async_langchain"}]
 
 [tool.poetry.dependencies]
 python = "^3.9"
 fastapi = "^0.95.1"
-langchain = "^0.0.164"
+langchain = ">=0.0.166"
 urllib3 = "<=1.26.15"  # added due to poetry errors
 python-dotenv = "^1.0.0"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `fastapi_async_langchain-0.5.2/PKG-INFO` & `fastapi_async_langchain-0.5.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 Metadata-Version: 2.1
 Name: fastapi-async-langchain
-Version: 0.5.2
+Version: 0.5.3
 Summary: Ship production-ready LangChain projects with FastAPI
 Home-page: https://github.com/ajndkr/fastapi-async-langchain
 License: MIT
 Author: Ajinkya Indulkar
 Author-email: 26824103+ajndkr@users.noreply.github.com
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: fastapi (>=0.95.1,<0.96.0)
-Requires-Dist: langchain (>=0.0.164,<0.0.165)
+Requires-Dist: langchain (>=0.0.166)
 Requires-Dist: python-dotenv (>=1.0.0,<2.0.0)
 Requires-Dist: urllib3 (<=1.26.15)
 Project-URL: Repository, https://github.com/ajndkr/fastapi-async-langchain
 Description-Content-Type: text/markdown
 
 # fastapi-async-langchain
```

