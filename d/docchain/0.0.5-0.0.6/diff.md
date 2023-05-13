# Comparing `tmp/docchain-0.0.5.tar.gz` & `tmp/docchain-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "docchain-0.0.5.tar", max compression
+gzip compressed data, was "docchain-0.0.6.tar", max compression
```

## Comparing `docchain-0.0.5.tar` & `docchain-0.0.6.tar`

### file list

```diff
@@ -1,25 +1,25 @@
--rw-r--r--   0        0        0     1139 2023-05-12 01:15:32.853173 docchain-0.0.5/README.md
--rw-r--r--   0        0        0        0 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/__init__.py
--rw-r--r--   0        0        0      284 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/blocks/__init__.py
--rw-r--r--   0        0        0     1724 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/blocks/base.py
--rw-r--r--   0        0        0      867 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/blocks/json_schema.py
--rw-r--r--   0        0        0      953 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/blocks/pydantic.py
--rw-r--r--   0        0        0      746 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/blocks/text.py
--rw-r--r--   0        0        0      855 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/blocks/ui_schema.py
--rw-r--r--   0        0        0     1023 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/documents.py
--rw-r--r--   0        0        0       51 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/exceptions.py
--rw-r--r--   0        0        0     4141 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/generator.py
--rw-r--r--   0        0        0      817 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/middleware/__init__.py
--rw-r--r--   0        0        0      588 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/middleware/base.py
--rw-r--r--   0        0        0      963 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/middleware/collect_openai_stats.py
--rw-r--r--   0        0        0      423 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/middleware/save_document.py
--rw-r--r--   0        0        0        0 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/models/__init__.py
--rw-r--r--   0        0        0      155 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/models/gpt.py
--rw-r--r--   0        0        0      154 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/output_parsers/__init__.py
--rw-r--r--   0        0        0     1706 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/output_parsers/json_schema.py
--rw-r--r--   0        0        0      879 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/output_parsers/ui_schema.py
--rw-r--r--   0        0        0     1508 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/settings.py
--rw-r--r--   0        0        0      592 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/specs.py
--rw-r--r--   0        0        0      288 2023-05-12 01:15:32.853173 docchain-0.0.5/docchain/utils.py
--rw-r--r--   0        0        0      647 2023-05-12 01:15:32.857173 docchain-0.0.5/pyproject.toml
--rw-r--r--   0        0        0     1698 1970-01-01 00:00:00.000000 docchain-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0     1139 2023-05-13 03:26:26.948617 docchain-0.0.6/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/__init__.py
+-rw-r--r--   0        0        0      284 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/__init__.py
+-rw-r--r--   0        0        0     1796 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/base.py
+-rw-r--r--   0        0        0      867 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/json_schema.py
+-rw-r--r--   0        0        0      953 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/pydantic.py
+-rw-r--r--   0        0        0      746 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/text.py
+-rw-r--r--   0        0        0      855 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/ui_schema.py
+-rw-r--r--   0        0        0     1023 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/documents.py
+-rw-r--r--   0        0        0       51 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/exceptions.py
+-rw-r--r--   0        0        0     4141 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/generator.py
+-rw-r--r--   0        0        0      817 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/middleware/__init__.py
+-rw-r--r--   0        0        0      588 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/middleware/base.py
+-rw-r--r--   0        0        0      963 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/middleware/collect_openai_stats.py
+-rw-r--r--   0        0        0      423 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/middleware/save_document.py
+-rw-r--r--   0        0        0        0 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/models/__init__.py
+-rw-r--r--   0        0        0      155 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/models/gpt.py
+-rw-r--r--   0        0        0      154 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/output_parsers/__init__.py
+-rw-r--r--   0        0        0     1706 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/output_parsers/json_schema.py
+-rw-r--r--   0        0        0      879 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/output_parsers/ui_schema.py
+-rw-r--r--   0        0        0     1508 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/settings.py
+-rw-r--r--   0        0        0      592 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/specs.py
+-rw-r--r--   0        0        0      288 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/utils.py
+-rw-r--r--   0        0        0      628 2023-05-13 03:26:26.952617 docchain-0.0.6/pyproject.toml
+-rw-r--r--   0        0        0     1737 1970-01-01 00:00:00.000000 docchain-0.0.6/PKG-INFO
```

### Comparing `docchain-0.0.5/README.md` & `docchain-0.0.6/README.md`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/blocks/base.py` & `docchain-0.0.6/docchain/blocks/base.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+from jinja2 import Template
 from langchain.chains import LLMChain
 from langchain.llms.base import BaseLLM
 from langchain.prompts import BasePromptTemplate
 from pydantic import BaseModel
 
 from ..documents import Document
 
@@ -35,15 +36,16 @@
     def get_params(self, document: Document) -> dict:
         """
         Renders params for the given document. Could be overridden in the subclass.
         """
         res = {}
         for key, value in self.config.dict().items():
             if isinstance(value, str):
-                value = value.format(**document.context)
+                template = Template(value)
+                value = template.render(document.context)
 
             res[key] = value
 
         return res
 
     def transform_result(self, result: str) -> any:
         """
```

### Comparing `docchain-0.0.5/docchain/blocks/json_schema.py` & `docchain-0.0.6/docchain/blocks/json_schema.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/blocks/pydantic.py` & `docchain-0.0.6/docchain/blocks/pydantic.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/blocks/text.py` & `docchain-0.0.6/docchain/blocks/text.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/blocks/ui_schema.py` & `docchain-0.0.6/docchain/blocks/ui_schema.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/documents.py` & `docchain-0.0.6/docchain/documents.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/generator.py` & `docchain-0.0.6/docchain/generator.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/middleware/__init__.py` & `docchain-0.0.6/docchain/middleware/__init__.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/middleware/base.py` & `docchain-0.0.6/docchain/middleware/base.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/middleware/collect_openai_stats.py` & `docchain-0.0.6/docchain/middleware/collect_openai_stats.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/output_parsers/json_schema.py` & `docchain-0.0.6/docchain/output_parsers/json_schema.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/output_parsers/ui_schema.py` & `docchain-0.0.6/docchain/output_parsers/ui_schema.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/settings.py` & `docchain-0.0.6/docchain/settings.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/docchain/specs.py` & `docchain-0.0.6/docchain/specs.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.5/pyproject.toml` & `docchain-0.0.6/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,31 +1,31 @@
 [tool.poetry]
 name = "docchain"
-version = "0.0.5"
+version = "0.0.6"
 description = ""
 authors = ["Artem Kolesnikov <tyomo4ka@gmail.com>"]
 readme = "README.md"
 packages = [{include = "docchain"}]
 
 [tool.poetry.dependencies]
 python = "^3.10"
-langchain = "^0.0.158"
+langchain = "^0.0.167"
 openai = "^0.27.6"
 jsonschema = "^4.17.3"
-fsspec = "^2023.4.0"
+fsspec = "^2023.5.0"
 pydantic = "^1.10.7"
+jinja2 = "^3.1.2"
 
 
 [tool.poetry.group.test.dependencies]
 pytest = "^7.3.1"
 pytest-dotenv = "^0.5.2"
 
 [tool.poetry.group.dev.dependencies]
-pre-commit = "^3.2.2"
-datamodel-code-generator = "^0.18.0"
+pre-commit = "^3.3.1"
 bump2version = "^1.0.1"
 
 [tool.ruff]
 line-length = 99
 
 [build-system]
 requires = ["poetry-core"]
```

### Comparing `docchain-0.0.5/PKG-INFO` & `docchain-0.0.6/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,20 +1,21 @@
 Metadata-Version: 2.1
 Name: docchain
-Version: 0.0.5
+Version: 0.0.6
 Summary: 
 Author: Artem Kolesnikov
 Author-email: tyomo4ka@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: fsspec (>=2023.4.0,<2024.0.0)
+Requires-Dist: fsspec (>=2023.5.0,<2024.0.0)
+Requires-Dist: jinja2 (>=3.1.2,<4.0.0)
 Requires-Dist: jsonschema (>=4.17.3,<5.0.0)
-Requires-Dist: langchain (>=0.0.158,<0.0.159)
+Requires-Dist: langchain (>=0.0.167,<0.0.168)
 Requires-Dist: openai (>=0.27.6,<0.28.0)
 Requires-Dist: pydantic (>=1.10.7,<2.0.0)
 Description-Content-Type: text/markdown
 
 # DocChain
 
 This package can be used to generate complex structured documents from Specs using LLMm models.
```

