# Comparing `tmp/docchain-0.0.6.tar.gz` & `tmp/docchain-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "docchain-0.0.6.tar", max compression
+gzip compressed data, was "docchain-0.0.7.tar", max compression
```

## Comparing `docchain-0.0.6.tar` & `docchain-0.0.7.tar`

### file list

```diff
@@ -1,25 +1,25 @@
--rw-r--r--   0        0        0     1139 2023-05-13 03:26:26.948617 docchain-0.0.6/README.md
--rw-r--r--   0        0        0        0 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/__init__.py
--rw-r--r--   0        0        0      284 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/__init__.py
--rw-r--r--   0        0        0     1796 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/base.py
--rw-r--r--   0        0        0      867 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/json_schema.py
--rw-r--r--   0        0        0      953 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/pydantic.py
--rw-r--r--   0        0        0      746 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/text.py
--rw-r--r--   0        0        0      855 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/blocks/ui_schema.py
--rw-r--r--   0        0        0     1023 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/documents.py
--rw-r--r--   0        0        0       51 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/exceptions.py
--rw-r--r--   0        0        0     4141 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/generator.py
--rw-r--r--   0        0        0      817 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/middleware/__init__.py
--rw-r--r--   0        0        0      588 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/middleware/base.py
--rw-r--r--   0        0        0      963 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/middleware/collect_openai_stats.py
--rw-r--r--   0        0        0      423 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/middleware/save_document.py
--rw-r--r--   0        0        0        0 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/models/__init__.py
--rw-r--r--   0        0        0      155 2023-05-13 03:26:26.948617 docchain-0.0.6/docchain/models/gpt.py
--rw-r--r--   0        0        0      154 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/output_parsers/__init__.py
--rw-r--r--   0        0        0     1706 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/output_parsers/json_schema.py
--rw-r--r--   0        0        0      879 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/output_parsers/ui_schema.py
--rw-r--r--   0        0        0     1508 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/settings.py
--rw-r--r--   0        0        0      592 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/specs.py
--rw-r--r--   0        0        0      288 2023-05-13 03:26:26.952617 docchain-0.0.6/docchain/utils.py
--rw-r--r--   0        0        0      628 2023-05-13 03:26:26.952617 docchain-0.0.6/pyproject.toml
--rw-r--r--   0        0        0     1737 1970-01-01 00:00:00.000000 docchain-0.0.6/PKG-INFO
+-rw-r--r--   0        0        0     1139 2023-05-13 03:33:25.965853 docchain-0.0.7/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/__init__.py
+-rw-r--r--   0        0        0      284 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/blocks/__init__.py
+-rw-r--r--   0        0        0     1796 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/blocks/base.py
+-rw-r--r--   0        0        0      867 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/blocks/json_schema.py
+-rw-r--r--   0        0        0      953 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/blocks/pydantic.py
+-rw-r--r--   0        0        0      746 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/blocks/text.py
+-rw-r--r--   0        0        0      855 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/blocks/ui_schema.py
+-rw-r--r--   0        0        0     1023 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/documents.py
+-rw-r--r--   0        0        0       51 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/exceptions.py
+-rw-r--r--   0        0        0     4141 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/generator.py
+-rw-r--r--   0        0        0      817 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/middleware/__init__.py
+-rw-r--r--   0        0        0      588 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/middleware/base.py
+-rw-r--r--   0        0        0      963 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/middleware/collect_openai_stats.py
+-rw-r--r--   0        0        0      423 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/middleware/save_document.py
+-rw-r--r--   0        0        0        0 2023-05-13 03:33:25.965853 docchain-0.0.7/docchain/models/__init__.py
+-rw-r--r--   0        0        0      155 2023-05-13 03:33:25.969853 docchain-0.0.7/docchain/models/gpt.py
+-rw-r--r--   0        0        0      154 2023-05-13 03:33:25.969853 docchain-0.0.7/docchain/output_parsers/__init__.py
+-rw-r--r--   0        0        0     1706 2023-05-13 03:33:25.969853 docchain-0.0.7/docchain/output_parsers/json_schema.py
+-rw-r--r--   0        0        0      879 2023-05-13 03:33:25.969853 docchain-0.0.7/docchain/output_parsers/ui_schema.py
+-rw-r--r--   0        0        0     1541 2023-05-13 03:33:25.969853 docchain-0.0.7/docchain/settings.py
+-rw-r--r--   0        0        0      592 2023-05-13 03:33:25.969853 docchain-0.0.7/docchain/specs.py
+-rw-r--r--   0        0        0      288 2023-05-13 03:33:25.969853 docchain-0.0.7/docchain/utils.py
+-rw-r--r--   0        0        0      628 2023-05-13 03:33:25.969853 docchain-0.0.7/pyproject.toml
+-rw-r--r--   0        0        0     1737 1970-01-01 00:00:00.000000 docchain-0.0.7/PKG-INFO
```

### Comparing `docchain-0.0.6/README.md` & `docchain-0.0.7/README.md`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/blocks/base.py` & `docchain-0.0.7/docchain/blocks/base.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/blocks/json_schema.py` & `docchain-0.0.7/docchain/blocks/json_schema.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/blocks/pydantic.py` & `docchain-0.0.7/docchain/blocks/pydantic.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/blocks/text.py` & `docchain-0.0.7/docchain/blocks/text.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/blocks/ui_schema.py` & `docchain-0.0.7/docchain/blocks/ui_schema.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/documents.py` & `docchain-0.0.7/docchain/documents.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/generator.py` & `docchain-0.0.7/docchain/generator.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/middleware/__init__.py` & `docchain-0.0.7/docchain/middleware/__init__.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/middleware/base.py` & `docchain-0.0.7/docchain/middleware/base.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/middleware/collect_openai_stats.py` & `docchain-0.0.7/docchain/middleware/collect_openai_stats.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/output_parsers/json_schema.py` & `docchain-0.0.7/docchain/output_parsers/json_schema.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/output_parsers/ui_schema.py` & `docchain-0.0.7/docchain/output_parsers/ui_schema.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/docchain/settings.py` & `docchain-0.0.7/docchain/settings.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from fsspec import AbstractFileSystem, get_filesystem_class
 from pydantic import BaseSettings, DirectoryPath, Field, PyObject
 
 
 class Settings(BaseSettings):
     class Config:
+        env_prefix = "DOCCHAIN_"
         env_file = ".env"
         env_file_encoding = "utf-8"
 
     debug: str = Field(default=False)
     openai_api_key: str = Field(default="--none--")
     max_tokens: int = Field(
         default=2048, description="Max number of tokens to use in the model."
```

### Comparing `docchain-0.0.6/docchain/specs.py` & `docchain-0.0.7/docchain/specs.py`

 * *Files identical despite different names*

### Comparing `docchain-0.0.6/pyproject.toml` & `docchain-0.0.7/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "docchain"
-version = "0.0.6"
+version = "0.0.7"
 description = ""
 authors = ["Artem Kolesnikov <tyomo4ka@gmail.com>"]
 readme = "README.md"
 packages = [{include = "docchain"}]
 
 [tool.poetry.dependencies]
 python = "^3.10"
```

### Comparing `docchain-0.0.6/PKG-INFO` & `docchain-0.0.7/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: docchain
-Version: 0.0.6
+Version: 0.0.7
 Summary: 
 Author: Artem Kolesnikov
 Author-email: tyomo4ka@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
```

