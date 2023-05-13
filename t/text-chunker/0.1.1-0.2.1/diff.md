# Comparing `tmp/text_chunker-0.1.1.tar.gz` & `tmp/text_chunker-0.2.1.tar.gz`

## Comparing `text_chunker-0.1.1.tar` & `text_chunker-0.2.1.tar`

### file list

```diff
@@ -1,9 +1,11 @@
--rw-r--r--   0        0        0       92 2020-02-02 00:00:00.000000 text_chunker-0.1.1/setup.sh
--rw-r--r--   0        0        0      296 2020-02-02 00:00:00.000000 text_chunker-0.1.1/examples/test.py
--rw-r--r--   0        0        0    15841 2020-02-02 00:00:00.000000 text_chunker-0.1.1/examples/test_text.txt
--rw-r--r--   0        0        0       38 2020-02-02 00:00:00.000000 text_chunker-0.1.1/src/text_chunker/__init__.py
--rw-r--r--   0        0        0     2323 2020-02-02 00:00:00.000000 text_chunker-0.1.1/src/text_chunker/text_chunker.py
--rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 text_chunker-0.1.1/LICENSE
--rw-r--r--   0        0        0     1128 2020-02-02 00:00:00.000000 text_chunker-0.1.1/README.md
--rw-r--r--   0        0        0      654 2020-02-02 00:00:00.000000 text_chunker-0.1.1/pyproject.toml
--rw-r--r--   0        0        0     1721 2020-02-02 00:00:00.000000 text_chunker-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0       92 2020-02-02 00:00:00.000000 text_chunker-0.2.1/setup.sh
+-rw-r--r--   0        0        0       61 2020-02-02 00:00:00.000000 text_chunker-0.2.1/src/text_chunker/__init__.py
+-rw-r--r--   0        0        0     2548 2020-02-02 00:00:00.000000 text_chunker-0.2.1/src/text_chunker/text_chunker.py
+-rw-r--r--   0        0        0      296 2020-02-02 00:00:00.000000 text_chunker-0.2.1/tests/test.py
+-rw-r--r--   0        0        0      154 2020-02-02 00:00:00.000000 text_chunker-0.2.1/tests/test_paragraphs.py
+-rw-r--r--   0        0        0      152 2020-02-02 00:00:00.000000 text_chunker-0.2.1/tests/test_sentences.py
+-rw-r--r--   0        0        0    15841 2020-02-02 00:00:00.000000 text_chunker-0.2.1/tests/test_text.txt
+-rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 text_chunker-0.2.1/LICENSE
+-rw-r--r--   0        0        0     1532 2020-02-02 00:00:00.000000 text_chunker-0.2.1/README.md
+-rw-r--r--   0        0        0      658 2020-02-02 00:00:00.000000 text_chunker-0.2.1/pyproject.toml
+-rw-r--r--   0        0        0     2122 2020-02-02 00:00:00.000000 text_chunker-0.2.1/PKG-INFO
```

### Comparing `text_chunker-0.1.1/examples/test_text.txt` & `text_chunker-0.2.1/tests/test_text.txt`

 * *Files identical despite different names*

### Comparing `text_chunker-0.1.1/src/text_chunker/text_chunker.py` & `text_chunker-0.2.1/src/text_chunker/text_chunker.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,7 +1,12 @@
+from nltk import tokenize
+
+PUNCTUATION_MARKS = ('. ','? ','! ')
+
+
 class TextChunker():
     """
     A class for chunking long text into smaller chunks.
 
     Parameters
     ----------
     maxlen : int
@@ -17,15 +22,14 @@
     >>> chunker = TextChunker(maxlen=1000)
     >>> for chunk in chunker.chunk(text):
     ...     print(chunk)
     """
 
     def __init__(self, maxlen):
         self.maxlen = maxlen
-        self.punctuation_marks = ('. ','? ','! ')
 
     def chunk(self, text):
         """
         Divide the input text into smaller chunks no longer than `maxlen`. If a chunk is longer than `maxlen`, it is split into smaller chunks separated by a newline character or punctuation marks.
 
         Parameters
         ----------
@@ -46,27 +50,39 @@
 
         end=0
         while len(text) > self.maxlen and end != -1:
             # split paragraphs
             end = text[:self.maxlen].rfind('\n')
             # if a paragraph is longer than maxlen: split sentences
             if end == -1:
-                end = max([text[:self.maxlen].rfind(m) for m in self.punctuation_marks])
+                end = max([text[:self.maxlen].rfind(m) for m in PUNCTUATION_MARKS])
                 # if a sentence is longer than maxlen: split words
                 if end == -1:
                     end = text[:self.maxlen].rfind(' ')
                     # if a word is longer than maxlen: force split
                     if end == -1:
                         end = self.maxlen-1
 
             yield text[:end+1]
             text = text[end+1:]
         yield text
 
 
+def paragraphs(text):
+    for paragraph in text.splitlines():
+        if paragraph:
+            yield paragraph
+
+
+def sentences(text):
+    for s in tokenize.sent_tokenize(text):
+        if s:
+            yield s
+
+
 if __name__ == '__main__':
     with open('test_text.txt','r') as ft:
         text = ft.read()
 
     chunk = TextChunker(1500)
     cum=0
     for i, line in enumerate(chunk.chunk(text)):
```

### Comparing `text_chunker-0.1.1/LICENSE` & `text_chunker-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `text_chunker-0.1.1/pyproject.toml` & `text_chunker-0.2.1/pyproject.toml`

 * *Files 25% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 [build-system]
-requires = ["hatchling"]
+requires = ["hatchling","nltk"]
 build-backend = "hatchling.build"
 
 [project]
 name = "text_chunker"
-version = "0.1.1"
+version = "0.2.1"
 authors = [
-  { name="RPAW Kim", email="rpawizardk@gmail.com" },
+  { name="rpawk", email="rpawizardk@gmail.com" },
 ]
 description = "A Python class that takes in long text as input and divides it into shorter chunks no longer than a specified length."
 readme = "README.md"
 requires-python = ">=3.5"
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
```

### Comparing `text_chunker-0.1.1/PKG-INFO` & `text_chunker-0.2.1/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 2.1
 Name: text_chunker
-Version: 0.1.1
+Version: 0.2.1
 Summary: A Python class that takes in long text as input and divides it into shorter chunks no longer than a specified length.
 Project-URL: Homepage, https://github.com/rpawk/text_chunker
 Project-URL: Bug Tracker, https://github.com/rpawk/text_chunker/issues
-Author-email: RPAW Kim <rpawizardk@gmail.com>
+Author-email: rpawk <rpawizardk@gmail.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.5
 Description-Content-Type: text/markdown
 
@@ -35,10 +35,28 @@
 text = "This is a long text string..."
 for chunk in chunker.chunk(text):
     print(chunk)
 ```
 
 The `chunk` method attempts to split paragraphs first while keeping chunk length below `maxlen`. If a paragraph is longer than `maxlen`, the method attempts to split the paragraph into sentences. If a sentence is longer than `maxlen`, it is split into smaller chunks no longer than `maxlen`.
 
+There are also functions called `paragraphs` and `sentences` that divide the text into paragraphs and sentences, respectively.
+
+```
+from text_chunker import paragraphs
+
+for p in paragraphs(text):
+    print(p)
+```
+```
+from text_chunker import sentences
+
+for s in sentences(text):
+    print(s)
+```
+
+The `sentences` function utilizes a tokenizer from the [`nltk`](https://pypi.org/project/nltk/) library.
+
+
 ## License
 
 This project is distributed under the MIT license. See the LICENSE file for details.
```

