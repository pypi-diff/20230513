# Comparing `tmp/sans-1.0.0b1.tar.gz` & `tmp/sans-1.0.0b2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sans-1.0.0b1.tar", last modified: Sat May 13 06:36:22 2023, max compression
+gzip compressed data, was "sans-1.0.0b2.tar", last modified: Sat May 13 18:51:25 2023, max compression
```

## Comparing `sans-1.0.0b1.tar` & `sans-1.0.0b2.tar`

### file list

```diff
@@ -1,49 +1,49 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.314650 sans-1.0.0b1/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.306650 sans-1.0.0b1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.310650 sans-1.0.0b1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-05-13 06:36:10.000000 sans-1.0.0b1/.github/workflows/codeql-analysis.yml
--rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-13 06:36:10.000000 sans-1.0.0b1/.github/workflows/pythonpublish.yml
--rw-r--r--   0 runner    (1001) docker     (123)     3101 2023-05-13 06:36:10.000000 sans-1.0.0b1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1236 2023-05-13 06:36:10.000000 sans-1.0.0b1/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 06:36:10.000000 sans-1.0.0b1/.readthedocs.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-13 06:36:10.000000 sans-1.0.0b1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5675 2023-05-13 06:36:22.314650 sans-1.0.0b1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3174 2023-05-13 06:36:10.000000 sans-1.0.0b1/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.310650 sans-1.0.0b1/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      581 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/auth.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6127 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/errors.rst
--rw-r--r--   0 runner    (1001) docker     (123)      237 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      115 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/limiter.rst
--rw-r--r--   0 runner    (1001) docker     (123)       94 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/lock.rst
--rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)      106 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/response.rst
--rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/url.rst
--rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 06:36:10.000000 sans-1.0.0b1/docs/utils.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2233 2023-05-13 06:36:10.000000 sans-1.0.0b1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      237 2023-05-13 06:36:10.000000 sans-1.0.0b1/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.310650 sans-1.0.0b1/sans/
--rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)      803 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/_state.py
--rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/auth.py
--rw-r--r--   0 runner    (1001) docker     (123)     1310 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/client.py
--rw-r--r--   0 runner    (1001) docker     (123)    29256 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/client.pyi
--rw-r--r--   0 runner    (1001) docker     (123)     4276 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/decoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/errors.py
--rw-r--r--   0 runner    (1001) docker     (123)     6689 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/limiter.py
--rw-r--r--   0 runner    (1001) docker     (123)     5056 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/lock.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)     4163 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2310 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/url.py
--rw-r--r--   0 runner    (1001) docker     (123)     3279 2023-05-13 06:36:10.000000 sans-1.0.0b1/sans/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:36:22.314650 sans-1.0.0b1/sans.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5675 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      133 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 06:36:22.000000 sans-1.0.0b1/sans.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 06:36:22.314650 sans-1.0.0b1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 06:36:10.000000 sans-1.0.0b1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:25.288592 sans-1.0.0b2/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:25.276591 sans-1.0.0b2/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:25.280592 sans-1.0.0b2/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-05-13 18:51:11.000000 sans-1.0.0b2/.github/workflows/codeql-analysis.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-13 18:51:11.000000 sans-1.0.0b2/.github/workflows/pythonpublish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     3101 2023-05-13 18:51:11.000000 sans-1.0.0b2/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1232 2023-05-13 18:51:11.000000 sans-1.0.0b2/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 18:51:11.000000 sans-1.0.0b2/.readthedocs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-13 18:51:11.000000 sans-1.0.0b2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5675 2023-05-13 18:51:25.288592 sans-1.0.0b2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3174 2023-05-13 18:51:11.000000 sans-1.0.0b2/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:25.280592 sans-1.0.0b2/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      581 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/auth.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6127 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/errors.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      237 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      115 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/limiter.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       94 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/lock.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)      106 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/response.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/url.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 18:51:11.000000 sans-1.0.0b2/docs/utils.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2227 2023-05-13 18:51:11.000000 sans-1.0.0b2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      233 2023-05-13 18:51:11.000000 sans-1.0.0b2/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:25.284592 sans-1.0.0b2/sans/
+-rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      803 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/_state.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/auth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1310 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29256 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/client.pyi
+-rw-r--r--   0 runner    (1001) docker     (123)     2777 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/decoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6689 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/limiter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5056 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/lock.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     3246 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2310 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/url.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3279 2023-05-13 18:51:11.000000 sans-1.0.0b2/sans/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 18:51:25.288592 sans-1.0.0b2/sans.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5675 2023-05-13 18:51:25.000000 sans-1.0.0b2/sans.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-13 18:51:25.000000 sans-1.0.0b2/sans.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 18:51:25.000000 sans-1.0.0b2/sans.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 18:51:25.000000 sans-1.0.0b2/sans.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      127 2023-05-13 18:51:25.000000 sans-1.0.0b2/sans.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 18:51:25.000000 sans-1.0.0b2/sans.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 18:51:25.288592 sans-1.0.0b2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 18:51:11.000000 sans-1.0.0b2/setup.py
```

### Comparing `sans-1.0.0b1/.github/workflows/codeql-analysis.yml` & `sans-1.0.0b2/.github/workflows/codeql-analysis.yml`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/.github/workflows/pythonpublish.yml` & `sans-1.0.0b2/.github/workflows/pythonpublish.yml`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/.gitignore` & `sans-1.0.0b2/.gitignore`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/.pre-commit-config.yaml` & `sans-1.0.0b2/.pre-commit-config.yaml`

 * *Files 9% similar despite different names*

```diff
@@ -25,18 +25,18 @@
         additional_dependencies:
             # required dependencies
         -   httpx ~= 0.23
         -   importlib_metadata >= 1.4.0; python_version < "3.8"
 
             # optional dependencies
             # [lxml]
-        -   lxml ~= 4.9.2
+        -   lxml ~= 4.9
 
             # [json]
-        -   xmltodict ~= 0.13.0
+        -   xmltodict ~= 0.13
 
             # typing
         -   typing_extensions
         -   lxml-stubs @ https://github.com/lxml/lxml-stubs/archive/master.zip#egg=lxml-stubs
 ci:
     skip:
     # CI doesn't like pip scripts calling their own node, so skip this for now
```

### Comparing `sans-1.0.0b1/LICENSE` & `sans-1.0.0b2/LICENSE`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/PKG-INFO` & `sans-1.0.0b2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sans
-Version: 1.0.0b1
+Version: 1.0.0b2
 Summary: Synchronous / Asynchronous HTTPX extension for NationStates
 Author: Zephyrkul
 License: MIT License
         
         Copyright (c) 2018 - 2023
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `sans-1.0.0b1/README.rst` & `sans-1.0.0b2/README.rst`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/docs/Makefile` & `sans-1.0.0b2/docs/Makefile`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/docs/conf.py` & `sans-1.0.0b2/docs/conf.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/docs/make.bat` & `sans-1.0.0b2/docs/make.bat`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/pyproject.toml` & `sans-1.0.0b2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -49,21 +49,21 @@
 repository = 'https://github.com/Zephyrkul/sans.git'
 
 [project.scripts]
 sans = 'sans.__main__:main'
 
 [project.optional-dependencies]
 docs = [
-    'Sphinx ~= 5.3.0'
+    'Sphinx ~= 5.3'
 ]
 lxml = [
-    'lxml ~= 4.9.2'
+    'lxml ~= 4.9'
 ]
 json = [
-    'xmltodict ~= 0.13.0'
+    'xmltodict ~= 0.13'
 ]
 
 [tool.setuptools_scm]
 
 [tool.black]
     target-version = ['py37']
     include = '\.pyi?$'
```

### Comparing `sans-1.0.0b1/sans/__init__.py` & `sans-1.0.0b2/sans/__init__.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/__main__.py` & `sans-1.0.0b2/sans/__main__.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/_state.py` & `sans-1.0.0b2/sans/_state.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/auth.py` & `sans-1.0.0b2/sans/auth.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/client.py` & `sans-1.0.0b2/sans/client.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/client.pyi` & `sans-1.0.0b2/sans/client.pyi`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/decoder.py` & `sans-1.0.0b2/sans/decoder.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,19 +1,27 @@
 from __future__ import annotations
 
 import codecs
 import zlib
+from functools import reduce
 from operator import itemgetter
 from typing import TYPE_CHECKING, Iterable
 from xml.etree.ElementTree import Element, XMLParser, XMLPullParser
 
 if TYPE_CHECKING:
     from typing_extensions import Literal
 
 
+def _reducer(final: bool):
+    def inner(data: bytes, decoder: codecs.IncrementalDecoder) -> bytes:
+        return decoder.decode(data, final)  # type: ignore
+
+    return inner
+
+
 class GZipDecoder:
     def __init__(self) -> None:
         self._decompressobj = zlib.decompressobj(zlib.MAX_WBITS | 16)
 
     def decode(self, data: bytes) -> bytes:
         return self._decompressobj.decompress(data)
 
@@ -36,48 +44,43 @@
     def __init__(self, *, encoding: str | None = None) -> None:
         self._decoder_chain: list[codecs.IncrementalDecoder] = []
         if encoding:
             self._decoder_chain.append(
                 codecs.getincrementaldecoder(encoding)("replace")
             )
         self._pull_parser = XMLPullParser(["start", "end"])
-        self._root: Element | None = None
+        self._path: list[Element] = []
 
     def decode(self, data: bytes) -> Iterable[Element]:
-        for chain in self._decoder_chain:
-            data = chain.decode(data, False)  # type: ignore
+        data = reduce(_reducer(False), self._decoder_chain, data)
         self._pull_parser.feed(data)
         return map(itemgetter(1), self._read_events())
 
-    def flush(self, data: bytes = b"") -> Iterable[Element]:
-        for chain in self._decoder_chain:
-            data = chain.decode(data, True)  # type: ignore
+    def flush(self) -> Iterable[Element]:
+        data = reduce(_reducer(True), self._decoder_chain, b"")
         self._pull_parser.feed(data)
         self._pull_parser.close()
         return map(itemgetter(1), self._read_events())
 
     def _read_events(self) -> Iterable[tuple[Literal["end"], Element]]:
-        depth = 0
         element: Element
+        path = self._path
         for event, element in self._pull_parser.read_events():
-            if not self._root:
-                self._root = element
             if event == "start":
-                depth += 1
+                path.append(element)
             elif event == "end":
-                depth -= 1
-                if depth == 1:
+                path.pop()
+                if len(path) == 1:
                     yield event, element
-                    self._root.clear()
+                    path[0].clear()
 
 
 try:
     from lxml.etree import (
         XMLParser as LXMLParser,
-        XMLPullParser as LXMLPullParser,
         _Element as LElement,  # type: ignore
     )
 except ImportError:
     pass
 else:
 
     class LXMLDecoder:
@@ -85,43 +88,7 @@
             self._parser = LXMLParser(encoding=encoding)
 
         def decode(self, data: bytes) -> None:
             self._parser.feed(data)
 
         def flush(self) -> LElement:
             return self._parser.close()
-
-    class LXMLChunker:
-        def __init__(self, *, encoding: str | None = None) -> None:
-            self._decoder_chain: list[codecs.IncrementalDecoder] = []
-            if encoding:
-                self._decoder_chain.append(
-                    codecs.getincrementaldecoder(encoding)("replace")
-                )
-            self._pull_parser = LXMLPullParser(["start", "end"])
-
-        def decode(self, data: bytes) -> Iterable[LElement]:
-            for chain in self._decoder_chain:
-                data = chain.decode(data, False)  # type: ignore
-            self._pull_parser.feed(data)
-            return map(itemgetter(1), self._read_events())
-
-        def flush(self, data: bytes = b"") -> Iterable[LElement]:
-            for chain in self._decoder_chain:
-                data = chain.decode(data, True)  # type: ignore
-            self._pull_parser.feed(data)
-            self._pull_parser.close()
-            return map(itemgetter(1), self._read_events())
-
-        def _read_events(self) -> Iterable[tuple[Literal["end"], LElement]]:
-            depth = 0
-            element: LElement
-            for event, element in self._pull_parser.read_events():  # type: ignore
-                if not self._root:
-                    self._root = element
-                if event == "start":
-                    depth += 1
-                elif event == "end":
-                    depth -= 1
-                    if depth == 1:
-                        yield event, element
-                        self._root.clear()
```

### Comparing `sans-1.0.0b1/sans/errors.py` & `sans-1.0.0b2/sans/errors.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/limiter.py` & `sans-1.0.0b2/sans/limiter.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/lock.py` & `sans-1.0.0b2/sans/lock.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/response.py` & `sans-1.0.0b2/sans/response.py`

 * *Files 11% similar despite different names*

```diff
@@ -20,15 +20,15 @@
 try:
     from lxml.etree import _Element  # type: ignore
 
     HAS_LXML = True
 except ImportError:
     HAS_LXML = False  # type: ignore
 else:
-    from .decoder import LXMLChunker, LXMLDecoder
+    from .decoder import LXMLDecoder
 
 __all__ = ["Response"]
 
 
 class Response(httpx.Response):
     @property
     def content_type(self) -> str:
@@ -97,35 +97,12 @@
             if not hasattr(self, "_lxml"):
                 content = self.content
                 decoder = LXMLDecoder(self.encoding)
                 decoder.decode(content)
                 self._lxml = decoder.flush()
             return self._lxml
 
-        def iter_lxml(self) -> Iterator[_Element]:
-            decoder = LXMLChunker(encoding=self.encoding)
-            chunker = (
-                self.iter_gzip()
-                if self.content_type.endswith(("/x-gzip", "/gzip"))
-                else self.iter_bytes()
-            )
-            yield from chain.from_iterable(map(decoder.decode, chunker))
-            yield from decoder.flush()
-
-        async def aiter_lxml(self) -> AsyncIterator[_Element]:
-            decoder = LXMLChunker(encoding=self.encoding)
-            chunker = (
-                self.aiter_gzip()
-                if self.content_type.endswith(("/x-gzip", "/gzip"))
-                else self.aiter_bytes()
-            )
-            async for chunk in chunker:
-                for element in decoder.decode(chunk):
-                    yield element
-            for element in decoder.flush():
-                yield element
-
     def raise_for_status(self) -> None:
         try:
             return super().raise_for_status()
         except httpx.HTTPStatusError as exc:
             raise narrow(exc) from None
```

### Comparing `sans-1.0.0b1/sans/url.py` & `sans-1.0.0b2/sans/url.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans/utils.py` & `sans-1.0.0b2/sans/utils.py`

 * *Files identical despite different names*

### Comparing `sans-1.0.0b1/sans.egg-info/PKG-INFO` & `sans-1.0.0b2/sans.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sans
-Version: 1.0.0b1
+Version: 1.0.0b2
 Summary: Synchronous / Asynchronous HTTPX extension for NationStates
 Author: Zephyrkul
 License: MIT License
         
         Copyright (c) 2018 - 2023
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `sans-1.0.0b1/sans.egg-info/SOURCES.txt` & `sans-1.0.0b2/sans.egg-info/SOURCES.txt`

 * *Files identical despite different names*

