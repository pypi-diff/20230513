# Comparing `tmp/text_chunker-0.2.1.tar.gz` & `tmp/text_chunker-0.2.2.tar.gz`

## Comparing `text_chunker-0.2.1.tar` & `text_chunker-0.2.2.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0       92 2020-02-02 00:00:00.000000 text_chunker-0.2.1/setup.sh
--rw-r--r--   0        0        0       61 2020-02-02 00:00:00.000000 text_chunker-0.2.1/src/text_chunker/__init__.py
--rw-r--r--   0        0        0     2548 2020-02-02 00:00:00.000000 text_chunker-0.2.1/src/text_chunker/text_chunker.py
--rw-r--r--   0        0        0      296 2020-02-02 00:00:00.000000 text_chunker-0.2.1/tests/test.py
--rw-r--r--   0        0        0      154 2020-02-02 00:00:00.000000 text_chunker-0.2.1/tests/test_paragraphs.py
--rw-r--r--   0        0        0      152 2020-02-02 00:00:00.000000 text_chunker-0.2.1/tests/test_sentences.py
--rw-r--r--   0        0        0    15841 2020-02-02 00:00:00.000000 text_chunker-0.2.1/tests/test_text.txt
--rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 text_chunker-0.2.1/LICENSE
--rw-r--r--   0        0        0     1532 2020-02-02 00:00:00.000000 text_chunker-0.2.1/README.md
--rw-r--r--   0        0        0      658 2020-02-02 00:00:00.000000 text_chunker-0.2.1/pyproject.toml
--rw-r--r--   0        0        0     2122 2020-02-02 00:00:00.000000 text_chunker-0.2.1/PKG-INFO
+-rw-r--r--   0        0        0       92 2020-02-02 00:00:00.000000 text_chunker-0.2.2/setup.sh
+-rw-r--r--   0        0        0       61 2020-02-02 00:00:00.000000 text_chunker-0.2.2/src/text_chunker/__init__.py
+-rw-r--r--   0        0        0     3531 2020-02-02 00:00:00.000000 text_chunker-0.2.2/src/text_chunker/text_chunker.py
+-rw-r--r--   0        0        0      296 2020-02-02 00:00:00.000000 text_chunker-0.2.2/tests/test.py
+-rw-r--r--   0        0        0      154 2020-02-02 00:00:00.000000 text_chunker-0.2.2/tests/test_paragraphs.py
+-rw-r--r--   0        0        0      152 2020-02-02 00:00:00.000000 text_chunker-0.2.2/tests/test_sentences.py
+-rw-r--r--   0        0        0    15841 2020-02-02 00:00:00.000000 text_chunker-0.2.2/tests/test_text.txt
+-rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 text_chunker-0.2.2/LICENSE
+-rw-r--r--   0        0        0     1546 2020-02-02 00:00:00.000000 text_chunker-0.2.2/README.md
+-rw-r--r--   0        0        0      658 2020-02-02 00:00:00.000000 text_chunker-0.2.2/pyproject.toml
+-rw-r--r--   0        0        0     2136 2020-02-02 00:00:00.000000 text_chunker-0.2.2/PKG-INFO
```

### Comparing `text_chunker-0.2.1/tests/test_text.txt` & `text_chunker-0.2.2/tests/test_text.txt`

 * *Files identical despite different names*

### Comparing `text_chunker-0.2.1/LICENSE` & `text_chunker-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `text_chunker-0.2.1/README.md` & `text_chunker-0.2.2/README.md`

 * *Files 7% similar despite different names*

```diff
@@ -23,21 +23,21 @@
     print(chunk)
 ```
 
 The `chunk` method attempts to split paragraphs first while keeping chunk length below `maxlen`. If a paragraph is longer than `maxlen`, the method attempts to split the paragraph into sentences. If a sentence is longer than `maxlen`, it is split into smaller chunks no longer than `maxlen`.
 
 There are also functions called `paragraphs` and `sentences` that divide the text into paragraphs and sentences, respectively.
 
-```
+``` python
 from text_chunker import paragraphs
 
 for p in paragraphs(text):
     print(p)
 ```
-```
+``` python
 from text_chunker import sentences
 
 for s in sentences(text):
     print(s)
 ```
 
 The `sentences` function utilizes a tokenizer from the [`nltk`](https://pypi.org/project/nltk/) library.
```

### Comparing `text_chunker-0.2.1/pyproject.toml` & `text_chunker-0.2.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling","nltk"]
 build-backend = "hatchling.build"
 
 [project]
 name = "text_chunker"
-version = "0.2.1"
+version = "0.2.2"
 authors = [
   { name="rpawk", email="rpawizardk@gmail.com" },
 ]
 description = "A Python class that takes in long text as input and divides it into shorter chunks no longer than a specified length."
 readme = "README.md"
 requires-python = ">=3.5"
 classifiers = [
```

### Comparing `text_chunker-0.2.1/PKG-INFO` & `text_chunker-0.2.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: text_chunker
-Version: 0.2.1
+Version: 0.2.2
 Summary: A Python class that takes in long text as input and divides it into shorter chunks no longer than a specified length.
 Project-URL: Homepage, https://github.com/rpawk/text_chunker
 Project-URL: Bug Tracker, https://github.com/rpawk/text_chunker/issues
 Author-email: rpawk <rpawizardk@gmail.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -37,21 +37,21 @@
     print(chunk)
 ```
 
 The `chunk` method attempts to split paragraphs first while keeping chunk length below `maxlen`. If a paragraph is longer than `maxlen`, the method attempts to split the paragraph into sentences. If a sentence is longer than `maxlen`, it is split into smaller chunks no longer than `maxlen`.
 
 There are also functions called `paragraphs` and `sentences` that divide the text into paragraphs and sentences, respectively.
 
-```
+``` python
 from text_chunker import paragraphs
 
 for p in paragraphs(text):
     print(p)
 ```
-```
+``` python
 from text_chunker import sentences
 
 for s in sentences(text):
     print(s)
 ```
 
 The `sentences` function utilizes a tokenizer from the [`nltk`](https://pypi.org/project/nltk/) library.
```

