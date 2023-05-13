# Comparing `tmp/markpickle-1.1.0.tar.gz` & `tmp/markpickle-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "markpickle-1.1.0.tar", max compression
+gzip compressed data, was "markpickle-1.2.0.tar", max compression
```

## Comparing `markpickle-1.1.0.tar` & `markpickle-1.2.0.tar`

### file list

```diff
@@ -1,14 +1,19 @@
--rw-r--r--   0        0        0     1071 2023-03-13 16:01:29.095278 markpickle-1.1.0/LICENSE
--rw-r--r--   0        0        0      363 2023-03-19 02:37:17.804275 markpickle-1.1.0/markpickle/__init__.py
--rw-r--r--   0        0        0     1046 2023-03-19 15:42:10.146065 markpickle-1.1.0/markpickle/config_class.py
--rw-r--r--   0        0        0     6176 2023-03-19 15:40:41.821112 markpickle-1.1.0/markpickle/deserialize.py
--rw-r--r--   0        0        0      568 2023-03-19 01:38:27.019163 markpickle-1.1.0/markpickle/mypy_types.py
--rw-r--r--   0        0        0       80 2023-01-30 03:12:57.741220 markpickle-1.1.0/markpickle/py.typed
--rw-r--r--   0        0        0     4817 2023-03-19 15:40:41.780446 markpickle-1.1.0/markpickle/python_to_tables.py
--rw-r--r--   0        0        0     8864 2023-03-19 15:40:41.871916 markpickle-1.1.0/markpickle/serialize.py
--rw-r--r--   0        0        0      737 2023-03-19 15:41:53.757488 markpickle-1.1.0/markpickle/simplify_types.py
--rw-r--r--   0        0        0     1252 2023-03-19 15:02:17.487053 markpickle-1.1.0/markpickle/third_party_tables.py
--rw-r--r--   0        0        0     3579 2023-03-19 16:33:12.905914 markpickle-1.1.0/pyproject.toml
--rw-r--r--   0        0        0     3909 2023-03-19 16:27:35.142051 markpickle-1.1.0/README.md
--rw-r--r--   0        0        0     4654 1970-01-01 00:00:00.000000 markpickle-1.1.0/setup.py
--rw-r--r--   0        0        0     5452 1970-01-01 00:00:00.000000 markpickle-1.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-03-13 16:01:29.095278 markpickle-1.2.0/LICENSE
+-rw-r--r--   0        0        0      520 2023-03-25 02:59:54.639724 markpickle-1.2.0/markpickle/__init__.py
+-rw-r--r--   0        0        0     1543 2023-05-13 21:17:46.471801 markpickle-1.2.0/markpickle/binary_streams.py
+-rw-r--r--   0        0        0     2298 2023-05-13 21:17:46.474842 markpickle-1.2.0/markpickle/config_class.py
+-rw-r--r--   0        0        0    11510 2023-05-13 21:06:47.467612 markpickle-1.2.0/markpickle/deserialize.py
+-rw-r--r--   0        0        0      890 2023-05-13 21:06:43.777843 markpickle-1.2.0/markpickle/import_string.py
+-rw-r--r--   0        0        0      359 2023-03-25 02:20:40.183215 markpickle-1.2.0/markpickle/meta.py
+-rw-r--r--   0        0        0      568 2023-03-19 01:38:27.019163 markpickle-1.2.0/markpickle/mypy_types.py
+-rw-r--r--   0        0        0       80 2023-01-30 03:12:57.741220 markpickle-1.2.0/markpickle/py.typed
+-rw-r--r--   0        0        0     4817 2023-03-19 15:40:41.780446 markpickle-1.2.0/markpickle/python_to_tables.py
+-rw-r--r--   0        0        0    14695 2023-05-13 21:17:51.391118 markpickle-1.2.0/markpickle/serialize.py
+-rw-r--r--   0        0        0      737 2023-03-19 15:41:53.757488 markpickle-1.2.0/markpickle/simplify_types.py
+-rw-r--r--   0        0        0     1032 2023-03-20 03:05:14.208164 markpickle-1.2.0/markpickle/split_file_code.py
+-rw-r--r--   0        0        0     1252 2023-03-19 15:02:17.487053 markpickle-1.2.0/markpickle/third_party_tables.py
+-rw-r--r--   0        0        0     1741 2023-05-13 21:06:36.820923 markpickle-1.2.0/markpickle/tool.py
+-rw-r--r--   0        0        0     3624 2023-05-13 21:21:21.556492 markpickle-1.2.0/pyproject.toml
+-rw-r--r--   0        0        0     5015 2023-05-13 21:21:08.812592 markpickle-1.2.0/README.md
+-rw-r--r--   0        0        0     5790 1970-01-01 00:00:00.000000 markpickle-1.2.0/setup.py
+-rw-r--r--   0        0        0     6580 1970-01-01 00:00:00.000000 markpickle-1.2.0/PKG-INFO
```

### Comparing `markpickle-1.1.0/LICENSE` & `markpickle-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `markpickle-1.1.0/markpickle/mypy_types.py` & `markpickle-1.2.0/markpickle/mypy_types.py`

 * *Files identical despite different names*

### Comparing `markpickle-1.1.0/markpickle/python_to_tables.py` & `markpickle-1.2.0/markpickle/python_to_tables.py`

 * *Files identical despite different names*

### Comparing `markpickle-1.1.0/markpickle/simplify_types.py` & `markpickle-1.2.0/markpickle/simplify_types.py`

 * *Files identical despite different names*

### Comparing `markpickle-1.1.0/markpickle/third_party_tables.py` & `markpickle-1.2.0/markpickle/third_party_tables.py`

 * *Files identical despite different names*

### Comparing `markpickle-1.1.0/pyproject.toml` & `markpickle-1.2.0/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "markpickle"
-version = "1.1.0"
+version = "1.2.0"
 description = "Lossy python to markdown serializer"
 authors = ["Matthew Martin <matthewdeanmartin@gmail.com>"]
 keywords = ["serializer", "deserializer", "markdown",]
 classifiers = [
     "Development Status :: 3 - Alpha",
     "Intended Audience :: Developers",
     "License :: OSI Approved :: MIT License",
@@ -34,15 +34,16 @@
 [tool.poetry.dependencies]
 # DOM parser
 mistune = "*"
 # alternate formatter
 mdformat = "*"
 # support more types to table
 tabulate = "*"
-
+# image/binary support
+pillow = "*"
 
 [tool.poetry.dev-dependencies]
 #marko = "*"
 #mistletoe = "*"
 pytest = "*"
 vermin = "*"
 hypothesis = {extras = ["cli"], version = "*"}
@@ -144,14 +145,14 @@
 format = "md"
 version = "literal: pyproject.toml: project.version"
 
 [tool.hatch.version]
 path = "markpickle/__init__.py"
 output_file = "CHANGELOG.${config:format}"
 
-[tool.setuptools]
-find = {}
-py-modules = ["markpickle",
-    "markpickle.deserialize",
-    "markpickle.python_to_tables",
-    "markpickle.serialize",
-]
+#[tool.setuptools]
+## find = {}
+#py-modules = ["markpickle",
+#    "markpickle.deserialize",
+#    "markpickle.python_to_tables",
+#    "markpickle.serialize",
+#]
```

### Comparing `markpickle-1.1.0/README.md` & `markpickle-1.2.0/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -1,85 +1,106 @@
 # markpickle
 
-Lossy serialization of markdown to simple python data types and back. It will create predictable markdown from a python object, but can't turn all markdown files into sensible python objects (for that use a markdown library that creates an AST). I created this because I wanted a way to turn json into Markdown.
+Markpickle is a Python library for lossy serialization of markdown to simple python data types and back. It will create predictable markdown from a python object, but can't turn all markdown files into sensible python objects (for that use a markdown library that creates an AST). I created this because I wanted a way to turn json into Markdown.
 
 For example this
 
 ```markdown
 - 1
 - 2
 ```
 
 becomes the python list `[1, 2]`
 
 Almost all markdown libraries use it as intended, as a way to generate HTML fragments from untrusted sources for insertion into some other HTML template. We are using it to represent data.
 
 ![Libraries.io dependency status for latest release](https://img.shields.io/librariesio/release/pypi/markpickle) [![Downloads](https://pepy.tech/badge/markpickle/month)](https://pepy.tech/project/markpickle/month)
 
+______________________________________________________________________
+
 ## Installation
 
 ```shell
 pip install markpickle
 ```
 
 ## Capabilities
+
 This is a lossy serialization. Markdown is missing too many concepts to make a high fidelity representation of a python data structure. If you want an object model that faithfully represents each object in a Markdown document, use the AST of mistune or one of the other markdown parsers.
 
-Supported types
+______________________________________________________________________
+
+### Supported Types
 
 - Scalar values
 - Lists of scalar values
 - Dictionaries with scalar values
 - Lists of dictionaries of scalar values
 - Dictionaries with list values
 - Partial support for blanks/string with leading/trailing whitespace
 
-Not supported
+See [examples](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/examples.md).
+
+### Not Supported
 
 - Things not ordinarily serializable
 - Markdown that uses more than headers, lists, tables
 - Blanks, falsy values, empty iterables don't round trip
 - Scalar type inference doesn't round trip. After a scalar is converted to a markdown string, there is no indication if the original was a string or not.
 
-# Serializing
-Results can be formatted at cost of speed.
+______________________________________________________________________
+
+## Serializing and Deserializing
+
+______________________________________________________________________
 
-Dictionaries can be represented as tables or header text pairs.
+### Serializing
 
-# Deserializing
+Results can be formatted at the cost of speed. Dictionaries can be represented as tables or header-text pairs.
 
-Markdown is deserialized by parsing the document to an abstract syntax tree. This is done by `mistune`. If the markdown file has the same structure that markpickle uses, then it will create a sensible object. Deserializing a random README.md file is not expected to always work. For that you should use mistune's AST.
+### Deserializing
 
-# Round Tripping
+Markdown is deserialized by parsing the document to an abstract syntax tree (AST). This is done by `mistune`. If the markdown file has the same structure that markpickle uses, then it will create a sensible object. Deserializing a random README.md file is not expected to always work. For that, you should use mistune's AST.
+
+### Round Tripping
 
 Some but not all data structures will be round-trippable. The goal is that the sort of dicts you get from loading JSON will be round-trippable, provided everything is a string.
 
+### Splitting Files
+
+## If typical serialization scenarios, many json files might be written to a single file, or in the case of yaml, you can put multiple documents into one file separated by `---`. markpickle can treat the horizontal rule as a document spliter if you use `split_file`. It works like [splitstream](https://github.com/rickardp/splitstream), but less efficiently.
 
 ## Prior Art
 
-People normally want to convert json to markdown. Json looks like python dict, so if you can do that you can probably do both.
+## People normally want to convert json to markdown. Json looks like python dict, so if you can do that you can probably do both.
 
 ### Serializing to Markdown
+
 [json2md](https://github.com/IonicaBizau/json2md), a node package, will turn json that looks like the HTML document object model into markdown, e.g.
+
 ```python
 {"h1": "Some Header",
  "p": "Some Text"}
 ```
 
 [tomark](https://pypi.org/project/tomark/) will turn dict into a markdown table. Unmaintained.
 
 [pytablewriter](https://pytablewriter.readthedocs.io/en/latest/pages/reference/writers/text/markup/md.html) also, dict to table, but supports many tabular formats.
 
-### Deserializing to Python 
+### Deserializing to Python
 
 I don't know of any libraries that turn markdown into basic python types. At the moment, they all turn markdown into document object model.
 
-[mistune](https://pypi.org/project/mistune/) will turn markdown into an Abstract Syntax Tree. The AST is faithful representation of the Markdown, including concepts that have no semantic equivalent to python datatypes. 
+[mistune](https://pypi.org/project/mistune/) will turn markdown into an Abstract Syntax Tree. The AST is faithful representation of the Markdown, including concepts that have no semantic equivalent to python datatypes.
 
-[beautifulsoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) will let you navigate the HTML DOM. So you can turn the markdown into HTML, then parse with Beautiful Soup. 
+## [beautifulsoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) will let you navigate the HTML DOM. So you can turn the markdown into HTML, then parse with Beautiful Soup.
 
-# Documentation
+## Documentation
 
 - [Examples](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/examples.md)
 - [TODO](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/TODO.md)
 - [People solving similar problems on StackOverflow](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/stackoverflow.md)
 
+
+## Change Log
+- 1.1.0 - Basic functionality. See [examples](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/examples.md) for what is supported.
+- 1.2.0 - Add support for binary data, which is serialized as images with data URLs.
```

### Comparing `markpickle-1.1.0/PKG-INFO` & `markpickle-1.2.0/PKG-INFO`

 * *Files 26% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: markpickle
-Version: 1.1.0
+Version: 1.2.0
 Summary: Lossy python to markdown serializer
 Home-page: https://github.com/matthewdeanmartin/markpickle
 License: MIT
 Keywords: serializer,deserializer,markdown
 Author: Matthew Martin
 Author-email: matthewdeanmartin@gmail.com
 Classifier: Development Status :: 3 - Alpha
@@ -22,100 +22,121 @@
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.6
 Requires-Dist: mdformat
 Requires-Dist: mistune
+Requires-Dist: pillow
 Requires-Dist: tabulate
 Project-URL: Bug Tracker, https://github.com/matthewdeanmartin/markpickle/issues
 Project-URL: Change Log, https://github.com/matthewdeanmartin/markpickle/blob/main/CHANGES.md
 Project-URL: Documentation, https://github.com/matthewdeanmartin/markpickle
 Project-URL: Repository, https://github.com/matthewdeanmartin/markpickle
 Description-Content-Type: text/markdown
 
 # markpickle
 
-Lossy serialization of markdown to simple python data types and back. It will create predictable markdown from a python object, but can't turn all markdown files into sensible python objects (for that use a markdown library that creates an AST). I created this because I wanted a way to turn json into Markdown.
+Markpickle is a Python library for lossy serialization of markdown to simple python data types and back. It will create predictable markdown from a python object, but can't turn all markdown files into sensible python objects (for that use a markdown library that creates an AST). I created this because I wanted a way to turn json into Markdown.
 
 For example this
 
 ```markdown
 - 1
 - 2
 ```
 
 becomes the python list `[1, 2]`
 
 Almost all markdown libraries use it as intended, as a way to generate HTML fragments from untrusted sources for insertion into some other HTML template. We are using it to represent data.
 
 ![Libraries.io dependency status for latest release](https://img.shields.io/librariesio/release/pypi/markpickle) [![Downloads](https://pepy.tech/badge/markpickle/month)](https://pepy.tech/project/markpickle/month)
 
+______________________________________________________________________
+
 ## Installation
 
 ```shell
 pip install markpickle
 ```
 
 ## Capabilities
+
 This is a lossy serialization. Markdown is missing too many concepts to make a high fidelity representation of a python data structure. If you want an object model that faithfully represents each object in a Markdown document, use the AST of mistune or one of the other markdown parsers.
 
-Supported types
+______________________________________________________________________
+
+### Supported Types
 
 - Scalar values
 - Lists of scalar values
 - Dictionaries with scalar values
 - Lists of dictionaries of scalar values
 - Dictionaries with list values
 - Partial support for blanks/string with leading/trailing whitespace
 
-Not supported
+See [examples](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/examples.md).
+
+### Not Supported
 
 - Things not ordinarily serializable
 - Markdown that uses more than headers, lists, tables
 - Blanks, falsy values, empty iterables don't round trip
 - Scalar type inference doesn't round trip. After a scalar is converted to a markdown string, there is no indication if the original was a string or not.
 
-# Serializing
-Results can be formatted at cost of speed.
+______________________________________________________________________
+
+## Serializing and Deserializing
 
-Dictionaries can be represented as tables or header text pairs.
+______________________________________________________________________
 
-# Deserializing
+### Serializing
 
-Markdown is deserialized by parsing the document to an abstract syntax tree. This is done by `mistune`. If the markdown file has the same structure that markpickle uses, then it will create a sensible object. Deserializing a random README.md file is not expected to always work. For that you should use mistune's AST.
+Results can be formatted at the cost of speed. Dictionaries can be represented as tables or header-text pairs.
 
-# Round Tripping
+### Deserializing
+
+Markdown is deserialized by parsing the document to an abstract syntax tree (AST). This is done by `mistune`. If the markdown file has the same structure that markpickle uses, then it will create a sensible object. Deserializing a random README.md file is not expected to always work. For that, you should use mistune's AST.
+
+### Round Tripping
 
 Some but not all data structures will be round-trippable. The goal is that the sort of dicts you get from loading JSON will be round-trippable, provided everything is a string.
 
+### Splitting Files
+
+## If typical serialization scenarios, many json files might be written to a single file, or in the case of yaml, you can put multiple documents into one file separated by `---`. markpickle can treat the horizontal rule as a document spliter if you use `split_file`. It works like [splitstream](https://github.com/rickardp/splitstream), but less efficiently.
 
 ## Prior Art
 
-People normally want to convert json to markdown. Json looks like python dict, so if you can do that you can probably do both.
+## People normally want to convert json to markdown. Json looks like python dict, so if you can do that you can probably do both.
 
 ### Serializing to Markdown
+
 [json2md](https://github.com/IonicaBizau/json2md), a node package, will turn json that looks like the HTML document object model into markdown, e.g.
+
 ```python
 {"h1": "Some Header",
  "p": "Some Text"}
 ```
 
 [tomark](https://pypi.org/project/tomark/) will turn dict into a markdown table. Unmaintained.
 
 [pytablewriter](https://pytablewriter.readthedocs.io/en/latest/pages/reference/writers/text/markup/md.html) also, dict to table, but supports many tabular formats.
 
-### Deserializing to Python 
+### Deserializing to Python
 
 I don't know of any libraries that turn markdown into basic python types. At the moment, they all turn markdown into document object model.
 
-[mistune](https://pypi.org/project/mistune/) will turn markdown into an Abstract Syntax Tree. The AST is faithful representation of the Markdown, including concepts that have no semantic equivalent to python datatypes. 
+[mistune](https://pypi.org/project/mistune/) will turn markdown into an Abstract Syntax Tree. The AST is faithful representation of the Markdown, including concepts that have no semantic equivalent to python datatypes.
 
-[beautifulsoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) will let you navigate the HTML DOM. So you can turn the markdown into HTML, then parse with Beautiful Soup. 
+## [beautifulsoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) will let you navigate the HTML DOM. So you can turn the markdown into HTML, then parse with Beautiful Soup.
 
-# Documentation
+## Documentation
 
 - [Examples](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/examples.md)
 - [TODO](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/TODO.md)
 - [People solving similar problems on StackOverflow](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/stackoverflow.md)
 
 
+## Change Log
+- 1.1.0 - Basic functionality. See [examples](https://github.com/matthewdeanmartin/markpickle/blob/main/docs/examples.md) for what is supported.
+- 1.2.0 - Add support for binary data, which is serialized as images with data URLs.
```

