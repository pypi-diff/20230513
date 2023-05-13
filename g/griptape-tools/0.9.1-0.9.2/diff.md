# Comparing `tmp/griptape_tools-0.9.1.tar.gz` & `tmp/griptape_tools-0.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "griptape_tools-0.9.1.tar", max compression
+gzip compressed data, was "griptape_tools-0.9.2.tar", max compression
```

## Comparing `griptape_tools-0.9.1.tar` & `griptape_tools-0.9.2.tar`

### file list

```diff
@@ -1,30 +1,30 @@
--rw-r--r--   0        0        0    11339 2023-04-06 19:20:02.762584 griptape_tools-0.9.1/LICENSE
--rw-r--r--   0        0        0     1151 2023-04-24 20:05:55.932841 griptape_tools-0.9.1/README.md
--rw-r--r--   0        0        0       65 2023-04-07 15:46:22.422848 griptape_tools-0.9.1/griptape/__init__.py
--rw-r--r--   0        0        0      352 2023-04-13 16:07:18.435628 griptape_tools-0.9.1/griptape/tools/__init__.py
--rw-r--r--   0        0        0        0 2023-04-06 19:20:02.783032 griptape_tools-0.9.1/griptape/tools/aws_cli/__init__.py
--rw-r--r--   0        0        0      159 2023-04-13 16:14:30.544316 griptape_tools-0.9.1/griptape/tools/aws_cli/manifest.yml
--rw-r--r--   0        0        0       73 2023-05-03 17:35:47.045678 griptape_tools-0.9.1/griptape/tools/aws_cli/requirements.txt
--rw-r--r--   0        0        0     1780 2023-05-03 17:18:05.788226 griptape_tools-0.9.1/griptape/tools/aws_cli/tool.py
--rw-r--r--   0        0        0        0 2023-04-06 19:20:02.783032 griptape_tools-0.9.1/griptape/tools/calculator/__init__.py
--rw-r--r--   0        0        0      169 2023-04-06 19:20:02.784946 griptape_tools-0.9.1/griptape/tools/calculator/manifest.yml
--rw-r--r--   0        0        0       16 2023-05-03 17:35:47.047062 griptape_tools-0.9.1/griptape/tools/calculator/requirements.txt
--rw-r--r--   0        0        0      816 2023-04-30 19:49:57.299564 griptape_tools-0.9.1/griptape/tools/calculator/tool.py
--rw-r--r--   0        0        0        0 2023-04-06 19:20:02.783032 griptape_tools-0.9.1/griptape/tools/email_client/__init__.py
--rw-r--r--   0        0        0      153 2023-04-12 21:25:06.766972 griptape_tools-0.9.1/griptape/tools/email_client/manifest.yml
--rw-r--r--   0        0        0       16 2023-05-03 17:35:47.048425 griptape_tools-0.9.1/griptape/tools/email_client/requirements.txt
--rw-r--r--   0        0        0     6041 2023-04-30 19:49:57.293290 griptape_tools-0.9.1/griptape/tools/email_client/tool.py
--rw-r--r--   0        0        0        0 2023-04-06 19:20:02.783032 griptape_tools-0.9.1/griptape/tools/sql_client/__init__.py
--rw-r--r--   0        0        0      154 2023-04-12 19:53:04.579660 griptape_tools-0.9.1/griptape/tools/sql_client/manifest.yml
--rw-r--r--   0        0        0       28 2023-05-03 17:35:47.036400 griptape_tools-0.9.1/griptape/tools/sql_client/requirements.txt
--rw-r--r--   0        0        0     1413 2023-04-30 19:49:57.297074 griptape_tools-0.9.1/griptape/tools/sql_client/tool.py
--rw-r--r--   0        0        0        0 2023-04-06 19:20:02.786470 griptape_tools-0.9.1/griptape/tools/web_scraper/__init__.py
--rw-r--r--   0        0        0      195 2023-04-11 21:24:23.634297 griptape_tools-0.9.1/griptape/tools/web_scraper/manifest.yml
--rw-r--r--   0        0        0       28 2023-05-03 17:35:47.038379 griptape_tools-0.9.1/griptape/tools/web_scraper/requirements.txt
--rw-r--r--   0        0        0     2890 2023-04-30 19:49:57.304804 griptape_tools-0.9.1/griptape/tools/web_scraper/tool.py
--rw-r--r--   0        0        0        0 2023-04-06 19:20:02.786470 griptape_tools-0.9.1/griptape/tools/web_search/__init__.py
--rw-r--r--   0        0        0      172 2023-04-08 22:17:19.115836 griptape_tools-0.9.1/griptape/tools/web_search/manifest.yml
--rw-r--r--   0        0        0       24 2023-05-03 17:35:47.049925 griptape_tools-0.9.1/griptape/tools/web_search/requirements.txt
--rw-r--r--   0        0        0     2323 2023-04-30 19:49:57.307290 griptape_tools-0.9.1/griptape/tools/web_search/tool.py
--rw-r--r--   0        0        0      520 2023-05-03 17:37:10.633859 griptape_tools-0.9.1/pyproject.toml
--rw-r--r--   0        0        0     1805 1970-01-01 00:00:00.000000 griptape_tools-0.9.1/PKG-INFO
+-rw-r--r--   0        0        0    11339 2023-04-06 19:20:02.762584 griptape_tools-0.9.2/LICENSE
+-rw-r--r--   0        0        0     1151 2023-04-24 20:05:55.932841 griptape_tools-0.9.2/README.md
+-rw-r--r--   0        0        0       65 2023-04-07 15:46:22.422848 griptape_tools-0.9.2/griptape/__init__.py
+-rw-r--r--   0        0        0      352 2023-04-13 16:07:18.435628 griptape_tools-0.9.2/griptape/tools/__init__.py
+-rw-r--r--   0        0        0        0 2023-04-06 19:20:02.783032 griptape_tools-0.9.2/griptape/tools/aws_cli/__init__.py
+-rw-r--r--   0        0        0      159 2023-04-13 16:14:30.544316 griptape_tools-0.9.2/griptape/tools/aws_cli/manifest.yml
+-rw-r--r--   0        0        0       73 2023-05-03 17:50:42.760907 griptape_tools-0.9.2/griptape/tools/aws_cli/requirements.txt
+-rw-r--r--   0        0        0     1780 2023-05-03 17:18:05.788226 griptape_tools-0.9.2/griptape/tools/aws_cli/tool.py
+-rw-r--r--   0        0        0        0 2023-04-06 19:20:02.783032 griptape_tools-0.9.2/griptape/tools/calculator/__init__.py
+-rw-r--r--   0        0        0      169 2023-04-06 19:20:02.784946 griptape_tools-0.9.2/griptape/tools/calculator/manifest.yml
+-rw-r--r--   0        0        0       16 2023-05-03 17:50:42.762103 griptape_tools-0.9.2/griptape/tools/calculator/requirements.txt
+-rw-r--r--   0        0        0      816 2023-04-30 19:49:57.299564 griptape_tools-0.9.2/griptape/tools/calculator/tool.py
+-rw-r--r--   0        0        0        0 2023-04-06 19:20:02.783032 griptape_tools-0.9.2/griptape/tools/email_client/__init__.py
+-rw-r--r--   0        0        0      153 2023-04-12 21:25:06.766972 griptape_tools-0.9.2/griptape/tools/email_client/manifest.yml
+-rw-r--r--   0        0        0       16 2023-05-03 17:50:42.766100 griptape_tools-0.9.2/griptape/tools/email_client/requirements.txt
+-rw-r--r--   0        0        0     6041 2023-04-30 19:49:57.293290 griptape_tools-0.9.2/griptape/tools/email_client/tool.py
+-rw-r--r--   0        0        0        0 2023-04-06 19:20:02.783032 griptape_tools-0.9.2/griptape/tools/sql_client/__init__.py
+-rw-r--r--   0        0        0      154 2023-04-12 19:53:04.579660 griptape_tools-0.9.2/griptape/tools/sql_client/manifest.yml
+-rw-r--r--   0        0        0       28 2023-05-03 17:50:42.763411 griptape_tools-0.9.2/griptape/tools/sql_client/requirements.txt
+-rw-r--r--   0        0        0     1413 2023-04-30 19:49:57.297074 griptape_tools-0.9.2/griptape/tools/sql_client/tool.py
+-rw-r--r--   0        0        0        0 2023-04-06 19:20:02.786470 griptape_tools-0.9.2/griptape/tools/web_scraper/__init__.py
+-rw-r--r--   0        0        0      195 2023-04-11 21:24:23.634297 griptape_tools-0.9.2/griptape/tools/web_scraper/manifest.yml
+-rw-r--r--   0        0        0       28 2023-05-03 17:50:42.764941 griptape_tools-0.9.2/griptape/tools/web_scraper/requirements.txt
+-rw-r--r--   0        0        0     2890 2023-04-30 19:49:57.304804 griptape_tools-0.9.2/griptape/tools/web_scraper/tool.py
+-rw-r--r--   0        0        0        0 2023-04-06 19:20:02.786470 griptape_tools-0.9.2/griptape/tools/web_search/__init__.py
+-rw-r--r--   0        0        0      172 2023-04-08 22:17:19.115836 griptape_tools-0.9.2/griptape/tools/web_search/manifest.yml
+-rw-r--r--   0        0        0       24 2023-05-03 17:50:42.759298 griptape_tools-0.9.2/griptape/tools/web_search/requirements.txt
+-rw-r--r--   0        0        0     2323 2023-04-30 19:49:57.307290 griptape_tools-0.9.2/griptape/tools/web_search/tool.py
+-rw-r--r--   0        0        0      520 2023-05-03 17:52:50.669749 griptape_tools-0.9.2/pyproject.toml
+-rw-r--r--   0        0        0     1805 1970-01-01 00:00:00.000000 griptape_tools-0.9.2/PKG-INFO
```

### Comparing `griptape_tools-0.9.1/LICENSE` & `griptape_tools-0.9.2/LICENSE`

 * *Files identical despite different names*

### Comparing `griptape_tools-0.9.1/README.md` & `griptape_tools-0.9.2/README.md`

 * *Files identical despite different names*

### Comparing `griptape_tools-0.9.1/griptape/tools/aws_cli/tool.py` & `griptape_tools-0.9.2/griptape/tools/aws_cli/tool.py`

 * *Files identical despite different names*

### Comparing `griptape_tools-0.9.1/griptape/tools/calculator/tool.py` & `griptape_tools-0.9.2/griptape/tools/calculator/tool.py`

 * *Files identical despite different names*

### Comparing `griptape_tools-0.9.1/griptape/tools/email_client/tool.py` & `griptape_tools-0.9.2/griptape/tools/email_client/tool.py`

 * *Files identical despite different names*

### Comparing `griptape_tools-0.9.1/griptape/tools/sql_client/tool.py` & `griptape_tools-0.9.2/griptape/tools/sql_client/tool.py`

 * *Files identical despite different names*

### Comparing `griptape_tools-0.9.1/griptape/tools/web_scraper/tool.py` & `griptape_tools-0.9.2/griptape/tools/web_scraper/tool.py`

 * *Files identical despite different names*

### Comparing `griptape_tools-0.9.1/griptape/tools/web_search/tool.py` & `griptape_tools-0.9.2/griptape/tools/web_search/tool.py`

 * *Files identical despite different names*

### Comparing `griptape_tools-0.9.1/pyproject.toml` & `griptape_tools-0.9.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 [tool.poetry]
 name = "griptape-tools"
-version = "0.9.1"
+version = "0.9.2"
 description = "Tools for the griptape-core package."
 authors = ["Griptape <hello@griptape.ai>"]
 license = "Apache 2.0"
 readme = "README.md"
 repository = "https://github.com/griptape-ai/griptape-tools"
 
 packages = [
     {include = "griptape"}
 ]
 
 [tool.poetry.dependencies]
 python = "^3.9"
-griptape = ">=0.7.2"
+griptape = ">=0.7.3"
 
 [tool.poetry.group.test.dependencies]
 pytest = "*"
 pytest-mock = "*"
 
 [build-system]
 requires = ["poetry-core"]
```

### Comparing `griptape_tools-0.9.1/PKG-INFO` & `griptape_tools-0.9.2/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 Metadata-Version: 2.1
 Name: griptape-tools
-Version: 0.9.1
+Version: 0.9.2
 Summary: Tools for the griptape-core package.
 Home-page: https://github.com/griptape-ai/griptape-tools
 License: Apache 2.0
 Author: Griptape
 Author-email: hello@griptape.ai
 Requires-Python: >=3.9,<4.0
 Classifier: License :: Other/Proprietary License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: griptape (>=0.7.2)
+Requires-Dist: griptape (>=0.7.3)
 Project-URL: Repository, https://github.com/griptape-ai/griptape-tools
 Description-Content-Type: text/markdown
 
 # griptape-tools
 
 [![PyPI Version](https://img.shields.io/pypi/v/griptape-tools.svg)](https://pypi.python.org/pypi/griptape-tools)
 [![Tests](https://github.com/griptape-ai/griptape-tools/actions/workflows/tests.yml/badge.svg)](https://github.com/griptape-ai/griptape-tools/actions/workflows/tests.yml)
```

