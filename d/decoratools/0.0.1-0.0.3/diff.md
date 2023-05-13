# Comparing `tmp/decoratools-0.0.1.tar.gz` & `tmp/decoratools-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "decoratools-0.0.1.tar", last modified: Sat May 13 11:58:44 2023, max compression
+gzip compressed data, was "decoratools-0.0.3.tar", last modified: Sat May 13 15:03:41 2023, max compression
```

## Comparing `decoratools-0.0.1.tar` & `decoratools-0.0.3.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.837163 decoratools-0.0.1/
--rw-rw-rw-   0 root         (0) root         (0)       94 2023-05-13 11:58:27.000000 decoratools-0.0.1/.gitignore
--rw-rw-rw-   0 root         (0) root         (0)     4303 2023-05-13 11:58:27.000000 decoratools-0.0.1/.gitlab-ci.yml
--rw-rw-rw-   0 root         (0) root         (0)      717 2023-05-13 11:58:27.000000 decoratools-0.0.1/.pre-commit-config.yaml
--rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 11:58:27.000000 decoratools-0.0.1/LICENSE
--rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 11:58:44.836163 decoratools-0.0.1/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)      306 2023-05-13 11:58:27.000000 decoratools-0.0.1/Pipfile
--rw-rw-rw-   0 root         (0) root         (0)    43703 2023-05-13 11:58:27.000000 decoratools-0.0.1/Pipfile.lock
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.830163 decoratools-0.0.1/decoratools/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.835163 decoratools-0.0.1/decoratools/capi/
--rw-rw-rw-   0 root         (0) root         (0)     4084 2023-05-13 11:58:27.000000 decoratools-0.0.1/decoratools/capi/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.835163 decoratools-0.0.1/decoratools.egg-info/
--rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 11:58:44.000000 decoratools-0.0.1/decoratools.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      327 2023-05-13 11:58:44.000000 decoratools-0.0.1/decoratools.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 11:58:44.000000 decoratools-0.0.1/decoratools.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       12 2023-05-13 11:58:44.000000 decoratools-0.0.1/decoratools.egg-info/top_level.txt
--rw-rw-rw-   0 root         (0) root         (0)     1368 2023-05-13 11:58:27.000000 decoratools-0.0.1/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 11:58:44.837163 decoratools-0.0.1/setup.cfg
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.835163 decoratools-0.0.1/tests/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 11:58:27.000000 decoratools-0.0.1/tests/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 11:58:44.836163 decoratools-0.0.1/tests/unit/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 11:58:27.000000 decoratools-0.0.1/tests/unit/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     8919 2023-05-13 11:58:27.000000 decoratools-0.0.1/tests/unit/test_capi.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:03:41.307646 decoratools-0.0.3/
+-rw-rw-rw-   0 root         (0) root         (0)       94 2023-05-13 15:03:24.000000 decoratools-0.0.3/.gitignore
+-rw-rw-rw-   0 root         (0) root         (0)     4303 2023-05-13 15:03:24.000000 decoratools-0.0.3/.gitlab-ci.yml
+-rw-rw-rw-   0 root         (0) root         (0)      717 2023-05-13 15:03:24.000000 decoratools-0.0.3/.pre-commit-config.yaml
+-rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 15:03:24.000000 decoratools-0.0.3/LICENSE
+-rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 15:03:41.307646 decoratools-0.0.3/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)      306 2023-05-13 15:03:24.000000 decoratools-0.0.3/Pipfile
+-rw-rw-rw-   0 root         (0) root         (0)    43703 2023-05-13 15:03:24.000000 decoratools-0.0.3/Pipfile.lock
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:03:41.300645 decoratools-0.0.3/decoratools/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:03:41.305645 decoratools-0.0.3/decoratools/capi/
+-rw-rw-rw-   0 root         (0) root         (0)     4301 2023-05-13 15:03:24.000000 decoratools-0.0.3/decoratools/capi/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:03:41.305645 decoratools-0.0.3/decoratools.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      738 2023-05-13 15:03:41.000000 decoratools-0.0.3/decoratools.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      327 2023-05-13 15:03:41.000000 decoratools-0.0.3/decoratools.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 15:03:41.000000 decoratools-0.0.3/decoratools.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       12 2023-05-13 15:03:41.000000 decoratools-0.0.3/decoratools.egg-info/top_level.txt
+-rw-rw-rw-   0 root         (0) root         (0)     1368 2023-05-13 15:03:24.000000 decoratools-0.0.3/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 15:03:41.307646 decoratools-0.0.3/setup.cfg
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:03:41.306645 decoratools-0.0.3/tests/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 15:03:24.000000 decoratools-0.0.3/tests/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 15:03:41.306645 decoratools-0.0.3/tests/unit/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 15:03:24.000000 decoratools-0.0.3/tests/unit/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    10281 2023-05-13 15:03:24.000000 decoratools-0.0.3/tests/unit/test_capi.py
```

### Comparing `decoratools-0.0.1/.gitlab-ci.yml` & `decoratools-0.0.3/.gitlab-ci.yml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.1/.pre-commit-config.yaml` & `decoratools-0.0.3/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.1/LICENSE` & `decoratools-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.1/PKG-INFO` & `decoratools-0.0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: decoratools
-Version: 0.0.1
+Version: 0.0.3
 Summary: Collection of useful decorators
 Author-email: Quentin Bouget <ypsah@devyard.org>
 License: MIT
 Project-URL: homepage, https://gitlab.com/ypsah/decoratools
 Project-URL: repository, https://gitlab.com/ypsah/decoratools
 Keywords: decorator,utility,library
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `decoratools-0.0.1/Pipfile.lock` & `decoratools-0.0.3/Pipfile.lock`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.1/decoratools/capi/__init__.py` & `decoratools-0.0.3/decoratools/capi/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -3,27 +3,35 @@
 from dataclasses import dataclass
 from functools import wraps
 from inspect import currentframe, get_annotations
 from types import GenericAlias
 from typing import Any, dataclass_transform, get_args, get_origin, get_type_hints
 
 
+class ARRAY:
+    def __class_getitem__(cls, *args):
+        return GenericAlias(cls, *args)
+
+
 @wraps(ctypes.POINTER, updated=())
 class POINTER(Callable):
     def __new__(cls, *args, **kwargs):
         return ctypes.POINTER(*args, **kwargs)
 
     def __class_getitem__(cls, *args):
         return GenericAlias(cls, *args)
 
 
 def _fields(cls: type, globals: dict[str, Any], locals: dict[str, Any]) -> Iterator[tuple[str, type]]:
     for key, value in get_type_hints(cls, globalns=globals, localns=locals).items():
         if get_origin(value) is POINTER:
             yield key, ctypes.POINTER(*get_args(value))
+        elif get_origin(value) is ARRAY:
+            ctype, length = get_args(value)
+            yield key, ctype * length
         else:
             yield key, value
 
 
 def bind(
     cls: type[ctypes.Structure] | type[ctypes.Union],
     *,
```

### Comparing `decoratools-0.0.1/decoratools.egg-info/PKG-INFO` & `decoratools-0.0.3/decoratools.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: decoratools
-Version: 0.0.1
+Version: 0.0.3
 Summary: Collection of useful decorators
 Author-email: Quentin Bouget <ypsah@devyard.org>
 License: MIT
 Project-URL: homepage, https://gitlab.com/ypsah/decoratools
 Project-URL: repository, https://gitlab.com/ypsah/decoratools
 Keywords: decorator,utility,library
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `decoratools-0.0.1/pyproject.toml` & `decoratools-0.0.3/pyproject.toml`

 * *Files identical despite different names*

### Comparing `decoratools-0.0.1/tests/unit/test_capi.py` & `decoratools-0.0.3/tests/unit/test_capi.py`

 * *Files 12% similar despite different names*

```diff
@@ -3,30 +3,35 @@
 import ctypes
 from dataclasses import is_dataclass
 from types import GenericAlias
 from typing import Annotated
 
 import pytest
 
-from decoratools.capi import POINTER, bind, structure, union
+from decoratools.capi import ARRAY, POINTER, bind, structure, union
 
 
 def test_pointer_type_annotation():
     assert isinstance(POINTER[ctypes.c_int], GenericAlias)
 
 
 def test_pointer_wrapper():
     assert POINTER(ctypes.c_int) == ctypes.POINTER(ctypes.c_int)
 
 
+def test_array_type_annotation():
+    assert isinstance(ARRAY[ctypes.c_int, 10], GenericAlias)
+
+
 def test_structure_retains_name_docstring_and_annotations():
     class Point:
         """
         A 2D point
         """
+
         x: ctypes.c_int
         y: ctypes.c_int
 
     StructPoint = structure(Point)
 
     for attribute in ("__name__", "__doc__", "__annotations__"):
         assert getattr(StructPoint, attribute) == getattr(Point, attribute)
@@ -47,14 +52,30 @@
     class Point:
         x: ctypes.c_int
         y: ctypes.c_int
 
     assert is_dataclass(Point)
 
 
+def test_structure_array_field():
+    @structure
+    class Point:
+        coordinates: ARRAY[ctypes.c_int, 2]
+
+    assert Point._fields_ == [("coordinates", ctypes.c_int * 2)]
+
+
+def test_structure_pointer_field():
+    @structure
+    class CharBox:
+        char: POINTER[ctypes.c_char]
+
+    assert CharBox._fields_ == [("char", POINTER(ctypes.c_char))]
+
+
 def test_structure_anonymous_fields():
     @structure
     class XCoordinate:
         x: ctypes.c_int
 
     @structure
     class YCoordinate:
@@ -156,15 +177,15 @@
 
 @pytest.mark.parametrize(
     ("endianness", "expected"),
     [
         pytest.param("native", ctypes.Structure, id="native"),
         pytest.param("little", ctypes.LittleEndianStructure, id="little-endian"),
         pytest.param("big", ctypes.BigEndianStructure, id="big-endian"),
-    ]
+    ],
 )
 def test_structure_endianness(
     endianness: str,
     expected: type[ctypes.Structure | ctypes.LittleEndianStructure | ctypes.BigEndianStructure],
 ):
     @structure(endianness=endianness)
     class Point:
@@ -189,14 +210,29 @@
     ],
 )
 def test_structure_illegal_dataclass_kwargs(illegal_dataclass_kwarg: str):
     with pytest.raises(TypeError, match=illegal_dataclass_kwarg):
         structure(**{illegal_dataclass_kwarg: None})
 
 
+def test_union_retains_name_docstring_and_annotations():
+    class Data:
+        """
+        Some data
+        """
+
+        char: ctypes.c_char
+        integer: ctypes.c_int
+
+    UnionData = union(Data)
+
+    for attribute in ("__name__", "__doc__", "__annotations__"):
+        assert getattr(UnionData, attribute) == getattr(Data, attribute)
+
+
 def test_union_ctypes():
     @structure(autobind=False)
     class BinaryBranch:
         left: POINTER[BinaryNode]
         right: POINTER[BinaryNode]
 
     @structure
@@ -230,14 +266,34 @@
         leaf: POINTER[Leaf]
 
     bind(BinaryBranch)
 
     assert is_dataclass(BinaryNode)
 
 
+def test_union_array_field():
+    @union
+    class Data:
+        char: ctypes.c_char
+        integer: ctypes.c_int
+        five_char_word: ARRAY[ctypes.c_char, 5]
+
+    assert Data._fields_ == [("char", ctypes.c_char), ("integer", ctypes.c_int), ("five_char_word", ctypes.c_char * 5)]
+
+
+def test_union_pointer_field():
+    @union
+    class Data:
+        char: ctypes.c_char
+        integer: ctypes.c_int
+        string: POINTER[ctypes.c_char]
+
+    assert Data._fields_ == [("char", ctypes.c_char), ("integer", ctypes.c_int), ("string", POINTER(ctypes.c_char))]
+
+
 def test_union_anonymous_fields():
     @structure
     class XCoordinate:
         x: ctypes.c_int
 
     @structure
     class YCoordinate:
@@ -252,25 +308,26 @@
         "x",
         "y",
     )
 
 
 def test_union_some_bindings_must_be_delayed():
     with pytest.raises(NameError, match="TBD"):
+
         @union
         class _:
             backward: TBD  # noqa: F821
-            forward: TBD   # noqa: F821
+            forward: TBD  # noqa: F821
 
 
 def test_union_delayed_bindings():
     @union(autobind=False)
     class Direction:
         backward: TBD  # noqa: F821
-        forward: TBD   # noqa: F821
+        forward: TBD  # noqa: F821
 
     bind(Direction, locals={"TBD": POINTER[Direction]})
 
 
 def test_union_delayed_binding_with_custom_global_type_resolution():
     @structure
     class Point:
@@ -281,15 +338,15 @@
     class _Point:
         x: ctypes.c_int
         y: ctypes.c_int
         _id: ctypes.c_int
 
     def cursor():
         @union(autobind=False)
-        class Cursor():
+        class Cursor:
             point: Point
             location: Point
 
         bind(Cursor, globals={"Point": _Point})
 
         return Cursor
 
@@ -305,15 +362,15 @@
     @structure
     class _Point:
         x: ctypes.c_int
         y: ctypes.c_int
         _id: ctypes.c_int
 
     @union(autobind=False)
-    class Cursor():
+    class Cursor:
         point: Point
         location: Point
 
     bind(Cursor, locals={"Point": _Point})
 
     assert Cursor._fields_ == [("point", _Point), ("location", _Point)]
 
@@ -337,15 +394,15 @@
 
 @pytest.mark.parametrize(
     ("endianness", "expected"),
     [
         pytest.param("native", ctypes.Union, id="native"),
         pytest.param("little", ctypes.LittleEndianUnion, id="little-endian"),
         pytest.param("big", ctypes.BigEndianUnion, id="big-endian"),
-    ]
+    ],
 )
 def test_union_endianness(
     endianness: str,
     expected: type[ctypes.Union | ctypes.LittleEndianUnion | ctypes.BigEndianUnion],
 ):
     @union(endianness=endianness)
     class Point:
```

