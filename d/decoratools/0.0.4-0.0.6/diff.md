# Comparing `tmp/decoratools-0.0.4.tar.gz` & `tmp/decoratools-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "decoratools-0.0.4.tar", last modified: Sat May 13 15:21:38 2023, max compression
+gzip compressed data, was "decoratools-0.0.6.tar", last modified: Sat May 13 16:24:24 2023, max compression
```

## Comparing `decoratools-0.0.4.tar` & `decoratools-0.0.6.tar`

### file list

```diff
@@ -1,23 +1,24 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:21:38.399351 decoratools-0.0.4/
--rw-rw-rw-   0 root         (0) root         (0)       94 2023-05-13 15:21:20.000000 decoratools-0.0.4/.gitignore
--rw-rw-rw-   0 root         (0) root         (0)     4303 2023-05-13 15:21:20.000000 decoratools-0.0.4/.gitlab-ci.yml
--rw-rw-rw-   0 root         (0) root         (0)      717 2023-05-13 15:21:20.000000 decoratools-0.0.4/.pre-commit-config.yaml
--rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 15:21:20.000000 decoratools-0.0.4/LICENSE
--rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 15:21:38.399351 decoratools-0.0.4/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)      306 2023-05-13 15:21:20.000000 decoratools-0.0.4/Pipfile
--rw-rw-rw-   0 root         (0) root         (0)    43703 2023-05-13 15:21:20.000000 decoratools-0.0.4/Pipfile.lock
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:21:38.393351 decoratools-0.0.4/decoratools/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:21:38.398351 decoratools-0.0.4/decoratools/capi/
--rw-rw-rw-   0 root         (0) root         (0)     3918 2023-05-13 15:21:20.000000 decoratools-0.0.4/decoratools/capi/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:21:38.398351 decoratools-0.0.4/decoratools.egg-info/
--rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 15:21:38.000000 decoratools-0.0.4/decoratools.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      327 2023-05-13 15:21:38.000000 decoratools-0.0.4/decoratools.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 15:21:38.000000 decoratools-0.0.4/decoratools.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       12 2023-05-13 15:21:38.000000 decoratools-0.0.4/decoratools.egg-info/top_level.txt
--rw-rw-rw-   0 root         (0) root         (0)     1368 2023-05-13 15:21:20.000000 decoratools-0.0.4/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 15:21:38.400351 decoratools-0.0.4/setup.cfg
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:21:38.398351 decoratools-0.0.4/tests/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 15:21:20.000000 decoratools-0.0.4/tests/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:21:38.399351 decoratools-0.0.4/tests/unit/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 15:21:20.000000 decoratools-0.0.4/tests/unit/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     8514 2023-05-13 15:21:20.000000 decoratools-0.0.4/tests/unit/test_capi.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 16:24:24.852457 decoratools-0.0.6/
+-rw-rw-rw-   0 root         (0) root         (0)       94 2023-05-13 16:24:07.000000 decoratools-0.0.6/.gitignore
+-rw-rw-rw-   0 root         (0) root         (0)     4303 2023-05-13 16:24:07.000000 decoratools-0.0.6/.gitlab-ci.yml
+-rw-rw-rw-   0 root         (0) root         (0)      717 2023-05-13 16:24:07.000000 decoratools-0.0.6/.pre-commit-config.yaml
+-rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 16:24:07.000000 decoratools-0.0.6/LICENSE
+-rw-r--r--   0 root         (0) root         (0)     3276 2023-05-13 16:24:24.852457 decoratools-0.0.6/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)      306 2023-05-13 16:24:07.000000 decoratools-0.0.6/Pipfile
+-rw-rw-rw-   0 root         (0) root         (0)    43703 2023-05-13 16:24:07.000000 decoratools-0.0.6/Pipfile.lock
+-rw-rw-rw-   0 root         (0) root         (0)     2537 2023-05-13 16:24:07.000000 decoratools-0.0.6/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 16:24:24.845456 decoratools-0.0.6/decoratools/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 16:24:24.850457 decoratools-0.0.6/decoratools/capi/
+-rw-rw-rw-   0 root         (0) root         (0)     4234 2023-05-13 16:24:07.000000 decoratools-0.0.6/decoratools/capi/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 16:24:24.850457 decoratools-0.0.6/decoratools.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     3276 2023-05-13 16:24:24.000000 decoratools-0.0.6/decoratools.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      337 2023-05-13 16:24:24.000000 decoratools-0.0.6/decoratools.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 16:24:24.000000 decoratools-0.0.6/decoratools.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       12 2023-05-13 16:24:24.000000 decoratools-0.0.6/decoratools.egg-info/top_level.txt
+-rw-rw-rw-   0 root         (0) root         (0)     1368 2023-05-13 16:24:07.000000 decoratools-0.0.6/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 16:24:24.852457 decoratools-0.0.6/setup.cfg
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 16:24:24.851457 decoratools-0.0.6/tests/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 16:24:07.000000 decoratools-0.0.6/tests/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 16:24:24.851457 decoratools-0.0.6/tests/unit/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 16:24:07.000000 decoratools-0.0.6/tests/unit/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    10281 2023-05-13 16:24:07.000000 decoratools-0.0.6/tests/unit/test_capi.py
```

### Comparing `decoratools-0.0.4/.gitlab-ci.yml` & `decoratools-0.0.6/.gitlab-ci.yml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.4/.pre-commit-config.yaml` & `decoratools-0.0.6/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.4/LICENSE` & `decoratools-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.4/Pipfile.lock` & `decoratools-0.0.6/Pipfile.lock`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.4/decoratools/capi/__init__.py` & `decoratools-0.0.6/decoratools/capi/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import ctypes
 from collections.abc import Callable, Iterator
+from dataclasses import dataclass
 from functools import wraps
 from inspect import currentframe, get_annotations
 from types import GenericAlias
 from typing import Any, get_args, get_origin, get_type_hints
 
 
 class ARRAY:
@@ -55,29 +56,33 @@
 
 def structure(
     cls: type | None = None,
     *,
     autobind: bool = True,
     pack: int | None = None,
     endianness: str = "native",
+    **kwargs,
 ) -> type | Callable[[type], type]:
     context = currentframe().f_back
+    _dataclass = dataclass(init=False, frozen=False, slots=False, weakref_slot=False, **kwargs)
     match endianness:
         case "native":
             structure = ctypes.Structure
         case "little":
             structure = ctypes.LittleEndianStructure
         case "big":
             structure = ctypes.BigEndianStructure
         case _:
             raise ValueError(
                 f"expected 'endianness' to be one of: 'native', 'little', or 'big', but got '{endianness}'"
             )
 
     def wrapper(cls: type) -> type:
+        cls = _dataclass(cls)
+
         @wraps(cls, updated=())
         class Wrap(cls, structure):
             if autobind:
                 _anonymous_ = tuple(_anonymous(cls, globals=context.f_globals, locals=context.f_locals))
                 _fields_ = list(_fields(cls, globals=context.f_globals, locals=context.f_locals))
             if pack is not None:
                 _pack_ = pack
@@ -92,29 +97,33 @@
 
 def union(
     cls: type | None = None,
     *,
     autobind: bool = True,
     pack: int | None = None,
     endianness: str = "native",
+    **kwargs,
 ) -> type | Callable[[type], type]:
     context = currentframe().f_back
+    _dataclass = dataclass(init=False, frozen=False, slots=False, weakref_slot=False, **kwargs)
     match endianness:
         case "native":
             union = ctypes.Union
         case "little":
             union = ctypes.LittleEndianUnion
         case "big":
             union = ctypes.BigEndianUnion
         case _:
             raise ValueError(
                 f"expected 'endianness' to be one of: 'native', 'little', or 'big', but got '{endianness}'"
             )
 
     def wrapper(cls: type) -> type:
+        cls = _dataclass(cls)
+
         @wraps(cls, updated=())
         class Wrap(cls, union):
             if autobind:
                 _anonymous_ = tuple(_anonymous(cls, globals=context.f_globals, locals=context.f_locals))
                 _fields_ = list(_fields(cls, globals=context.f_globals, locals=context.f_locals))
             if pack is not None:
                 _pack_ = pack
```

### Comparing `decoratools-0.0.4/pyproject.toml` & `decoratools-0.0.6/pyproject.toml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.4/tests/unit/test_capi.py` & `decoratools-0.0.6/tests/unit/test_capi.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from __future__ import annotations
 
 import ctypes
+from dataclasses import is_dataclass
 from types import GenericAlias
 from typing import Annotated
 
 import pytest
 
 from decoratools.capi import ARRAY, POINTER, bind, structure, union
 
@@ -42,14 +43,23 @@
         x: ctypes.c_int
         y: ctypes.c_int
 
     assert issubclass(Point, ctypes.Structure)
     assert Point._fields_ == [("x", ctypes.c_int), ("y", ctypes.c_int)]
 
 
+def test_structure_dataclass():
+    @structure
+    class Point:
+        x: ctypes.c_int
+        y: ctypes.c_int
+
+    assert is_dataclass(Point)
+
+
 def test_structure_array_field():
     @structure
     class Point:
         coordinates: ARRAY[ctypes.c_int, 2]
 
     assert Point._fields_ == [("coordinates", ctypes.c_int * 2)]
 
@@ -186,14 +196,28 @@
 
 
 def test_structure_invalid_endianness():
     with pytest.raises(ValueError, match="invalid"):
         structure(endianness="invalid")
 
 
+@pytest.mark.parametrize(
+    ("illegal_dataclass_kwarg",),
+    [
+        pytest.param("init", id="init, to not override Structure's"),
+        pytest.param("frozen", id="frozen, to be compatible with Structure's descriptors"),
+        pytest.param("slots", id="slots, to be compatible with Structure's descriptors"),
+        pytest.param("wearkref_slots", id="weakref_slots, out of consistency wrt slots"),
+    ],
+)
+def test_structure_illegal_dataclass_kwargs(illegal_dataclass_kwarg: str):
+    with pytest.raises(TypeError, match=illegal_dataclass_kwarg):
+        structure(**{illegal_dataclass_kwarg: None})
+
+
 def test_union_retains_name_docstring_and_annotations():
     class Data:
         """
         Some data
         """
 
         char: ctypes.c_char
@@ -222,14 +246,34 @@
 
     bind(BinaryBranch)
 
     assert issubclass(BinaryNode, ctypes.Union)
     assert BinaryNode._fields_ == [("branch", POINTER(BinaryBranch)), ("leaf", POINTER(Leaf))]
 
 
+def test_union_dataclass():
+    @structure(autobind=False)
+    class BinaryBranch:
+        left: POINTER[BinaryNode]
+        right: POINTER[BinaryNode]
+
+    @structure
+    class Leaf:
+        value: ctypes.c_void_p
+
+    @union
+    class BinaryNode:
+        branch: POINTER[BinaryBranch]
+        leaf: POINTER[Leaf]
+
+    bind(BinaryBranch)
+
+    assert is_dataclass(BinaryNode)
+
+
 def test_union_array_field():
     @union
     class Data:
         char: ctypes.c_char
         integer: ctypes.c_int
         five_char_word: ARRAY[ctypes.c_char, 5]
 
@@ -367,7 +411,21 @@
 
     assert issubclass(Point, expected)
 
 
 def test_union_invalid_endianness():
     with pytest.raises(ValueError, match="invalid"):
         union(endianness="invalid")
+
+
+@pytest.mark.parametrize(
+    ("illegal_dataclass_kwarg",),
+    [
+        pytest.param("init", id="init, to not override Union's"),
+        pytest.param("frozen", id="frozen, to be compatible with Union's descriptors"),
+        pytest.param("slots", id="slots, to be compatible with Union's descriptors"),
+        pytest.param("wearkref_slots", id="weakref_slots, out of consistency wrt slots"),
+    ],
+)
+def test_union_illegal_dataclass_kwargs(illegal_dataclass_kwarg: str):
+    with pytest.raises(TypeError, match=illegal_dataclass_kwarg):
+        union(**{illegal_dataclass_kwarg: None})
```

