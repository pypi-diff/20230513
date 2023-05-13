# Comparing `tmp/typeapi-1.4.2.tar.gz` & `tmp/typeapi-1.4.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "typeapi-1.4.2.tar", max compression
+gzip compressed data, was "typeapi-1.4.3.tar", max compression
```

## Comparing `typeapi-1.4.2.tar` & `typeapi-1.4.3.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0      991 2023-03-01 15:02:00.051150 typeapi-1.4.2/LICENSE
--rw-r--r--   0        0        0     2215 2023-04-12 22:39:01.286876 typeapi-1.4.2/pyproject.toml
--rw-r--r--   0        0        0     4481 2023-03-23 10:30:24.377082 typeapi-1.4.2/readme.md
--rw-r--r--   0        0        0      595 2023-04-12 22:39:01.286876 typeapi-1.4.2/src/typeapi/__init__.py
--rw-r--r--   0        0        0     4883 2023-03-02 10:19:24.777783 typeapi-1.4.2/src/typeapi/backport/inspect.py
--rw-r--r--   0        0        0     5505 2023-04-12 22:28:15.607915 typeapi-1.4.2/src/typeapi/future/astrewrite.py
--rw-r--r--   0        0        0     2342 2023-04-12 22:36:27.277248 typeapi-1.4.2/src/typeapi/future/fake.py
--rw-r--r--   0        0        0     1570 2023-03-01 15:02:00.051150 typeapi-1.4.2/src/typeapi/future/fake_test.py
--rw-r--r--   0        0        0        0 2023-03-01 15:02:00.051150 typeapi-1.4.2/src/typeapi/py.typed
--rw-r--r--   0        0        0    15204 2023-04-12 22:18:08.512957 typeapi-1.4.2/src/typeapi/typehint.py
--rw-r--r--   0        0        0    14932 2023-04-12 22:20:39.278551 typeapi-1.4.2/src/typeapi/typehint_test.py
--rw-r--r--   0        0        0    13473 2023-04-12 22:18:08.516957 typeapi-1.4.2/src/typeapi/utils.py
--rw-r--r--   0        0        0    16298 2023-04-12 22:29:54.749041 typeapi-1.4.2/src/typeapi/utils_test.py
--rw-r--r--   0        0        0     5322 1970-01-01 00:00:00.000000 typeapi-1.4.2/setup.py
--rw-r--r--   0        0        0     5297 1970-01-01 00:00:00.000000 typeapi-1.4.2/PKG-INFO
+-rw-r--r--   0        0        0      991 2022-11-06 01:30:42.966331 typeapi-1.4.3/LICENSE
+-rw-r--r--   0        0        0     2215 2023-05-13 00:14:29.393800 typeapi-1.4.3/pyproject.toml
+-rw-r--r--   0        0        0     4481 2023-05-13 00:07:03.090520 typeapi-1.4.3/readme.md
+-rw-r--r--   0        0        0      595 2023-05-13 00:14:29.393800 typeapi-1.4.3/src/typeapi/__init__.py
+-rw-r--r--   0        0        0     4883 2023-03-23 10:16:27.335509 typeapi-1.4.3/src/typeapi/backport/inspect.py
+-rw-r--r--   0        0        0     5505 2023-05-13 00:07:03.090520 typeapi-1.4.3/src/typeapi/future/astrewrite.py
+-rw-r--r--   0        0        0     2342 2023-03-23 10:16:27.335509 typeapi-1.4.3/src/typeapi/future/fake.py
+-rw-r--r--   0        0        0     1570 2023-03-23 10:16:27.335509 typeapi-1.4.3/src/typeapi/future/fake_test.py
+-rw-r--r--   0        0        0        0 2022-11-06 01:30:42.966331 typeapi-1.4.3/src/typeapi/py.typed
+-rw-r--r--   0        0        0    15268 2023-05-13 00:08:05.916727 typeapi-1.4.3/src/typeapi/typehint.py
+-rw-r--r--   0        0        0    14932 2023-05-13 00:07:03.090520 typeapi-1.4.3/src/typeapi/typehint_test.py
+-rw-r--r--   0        0        0    13473 2023-05-13 00:07:03.090520 typeapi-1.4.3/src/typeapi/utils.py
+-rw-r--r--   0        0        0    16298 2023-05-13 00:07:03.090520 typeapi-1.4.3/src/typeapi/utils_test.py
+-rw-r--r--   0        0        0     5322 1970-01-01 00:00:00.000000 typeapi-1.4.3/setup.py
+-rw-r--r--   0        0        0     5297 1970-01-01 00:00:00.000000 typeapi-1.4.3/PKG-INFO
```

### Comparing `typeapi-1.4.2/LICENSE` & `typeapi-1.4.3/LICENSE`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/pyproject.toml` & `typeapi-1.4.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 # NOTE(NiklasRosenstein): We pin this version so we can keep using the old way that Slap supports installing
 #                         the "docs" extra without Poetry complaining about invalid format of the requirements.
 requires = ["poetry-core==1.1.0a6"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "typeapi"
-version = "1.4.2"
+version = "1.4.3"
 description = ""
 authors = ["Niklas Rosenstein <rosensteinniklas@gmail.com>"]
 license = "MIT"
 readme = "readme.md"
 packages = [{ include = "typeapi", from = "src" }]
 classifiers = []
 keywords = []
```

### Comparing `typeapi-1.4.2/readme.md` & `typeapi-1.4.3/readme.md`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/src/typeapi/__init__.py` & `typeapi-1.4.3/src/typeapi/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-__version__ = "1.4.2"
+__version__ = "1.4.3"
 
 from .typehint import (
     AnnotatedTypeHint,
     ClassTypeHint,
     ForwardRefTypeHint,
     LiteralTypeHint,
     TupleTypeHint,
```

### Comparing `typeapi-1.4.2/src/typeapi/backport/inspect.py` & `typeapi-1.4.3/src/typeapi/backport/inspect.py`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/src/typeapi/future/astrewrite.py` & `typeapi-1.4.3/src/typeapi/future/astrewrite.py`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/src/typeapi/future/fake.py` & `typeapi-1.4.3/src/typeapi/future/fake.py`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/src/typeapi/future/fake_test.py` & `typeapi-1.4.3/src/typeapi/future/fake_test.py`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/src/typeapi/typehint.py` & `typeapi-1.4.3/src/typeapi/typehint.py`

 * *Files 1% similar despite different names*

```diff
@@ -437,13 +437,17 @@
 
     def _copy_with_args(self, args: "Tuple[Any, ...]") -> "TypeHint":
         if self._repeated:
             args = args + (...,)
         return super()._copy_with_args(args)
 
     @property
+    def type(self) -> type:
+        return tuple
+
+    @property
     def repeated(self) -> bool:
         """
         Returns `True` if the Tuple is of arbitrary length, but only of one type.
         """
 
         return self._repeated
```

### Comparing `typeapi-1.4.2/src/typeapi/typehint_test.py` & `typeapi-1.4.3/src/typeapi/typehint_test.py`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/src/typeapi/utils.py` & `typeapi-1.4.3/src/typeapi/utils.py`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/src/typeapi/utils_test.py` & `typeapi-1.4.3/src/typeapi/utils_test.py`

 * *Files identical despite different names*

### Comparing `typeapi-1.4.2/setup.py` & `typeapi-1.4.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 {'': ['*']}
 
 install_requires = \
 ['typing-extensions>=3.0.0']
 
 setup_kwargs = {
     'name': 'typeapi',
-    'version': '1.4.2',
+    'version': '1.4.3',
     'description': '',
     'long_description': '# typeapi\n\n[![Python](https://github.com/NiklasRosenstein/python-typeapi/actions/workflows/python.yml/badge.svg)](https://github.com/NiklasRosenstein/python-typeapi/actions/workflows/python.yml)\n\n  [PEP484]: https://peps.python.org/pep-0484/\n  [PEP585]: https://peps.python.org/pep-0585/\n  [PEP604]: https://peps.python.org/pep-0604/\n\n__Compatibility__: Python 3.6.3+\n\nThe `typeapi` package provides an object-oriented interface for introspecting [PEP484][] type hints at runtime,\nincluding forward references that make use of the more recent [PEP585][] and [PEP604][] type hint features in\nPython versions that don\'t natively support them.\n\nThe main API of this module is comprised of:\n\n* `typeapi.TypeHint()` &ndash; A class to parse low-level type hints and present them in a consistent, object-oriented API.\n* `typeapi.get_annotations()` &ndash; Retrieve an object\'s `__annotations__` with support for evaluating future type hints ([PEP585][], [PEP604][]).\n\nThe following kinds of type hints are currently supported:\n\n| Concrete type | Description | Added in |\n| ------------- | ----------- | -------- |\n| `ClassTypeHint` | For any normal or generic type as well as `typing.Any`. Provides access to the underlying type, the type arguments and parameters, if any. | 1.0.0 |\n| `UnionTypeHint` | Represents `Union` type hint and gives access to the union members. | 1.0.0 |\n| `LiteralTypeHint` | Represents a `Literal` type hint and gives access to the literal values. | 1.0.0 |\n| `AnnotatedTypeHint` | Represents an `Annotated` type hint and gives access to the annotated type as well as the metadata. | 1.0.0 |\n| `TypeVarTypeHint` | Represents a `TypeVar` type hint and gives an interface to access the variable\'s metadata (such as constarints, variance, ...). | 1.0.0 |\n| `ForwardRefTypeHint` | Represents a forward reference. Can be evaluated in Python 3.6+ even if it contains [PEP585][] and [PEP604][] expressions. <sup>1)</sup> | 1.0.0, future support in 1.3.0 |\n| `TupleTypeHint` | Reperesents a `Tuple` type hint, allowing you to differentiate between repeated and explicitly sized tuples. | 1.2.0 |\n\n<sup>1)</sup> New-style type union evaluation will continue to return a `typing.Union`, even if the same syntax\nevaluated natively by Python 3.10+ results in a `types.UnionType`.\n\n## Examples\n\nInspect a `List[int]` type hint:\n\n```py\n# cat <<EOF | python -\nfrom typeapi import ClassTypeHint, TypeHint\nfrom typing import List\n\nhint = TypeHint(List[int])\nassert isinstance(hint, ClassTypeHint)\nassert hint.type is list\n\nitem_hint = hint[0]\nassert isinstance(item_hint, ClassTypeHint)\nassert item_hint.type is int\n```\n\nRetrieve the metadata from an `Annotated[...]` type hint:\n\n```py\n# cat <<EOF | python -\nfrom typeapi import AnnotatedTypeHint, ClassTypeHint, TypeHint\nfrom typing_extensions import Annotated\n\nhint = TypeHint(Annotated[int, 42])\nassert isinstance(hint, AnnotatedTypeHint)\nassert hint.type is int\nassert hint.metadata == (42,)\n\nsub_hint = hint[0]\nassert isinstance(sub_hint, ClassTypeHint)\nassert sub_hint.type is int\n```\n\nParameterize one type hint with the parameterization of a generic alias:\n\n```py\n# cat <<EOF | python -\nfrom dataclasses import dataclass\nfrom typeapi import ClassTypeHint, TypeHint\nfrom typing import Generic, TypeVar\nfrom typing_extensions import Annotated\n\nT = TypeVar("T")\n\n@dataclass\nclass MyGeneric(Generic[T]):\n  value: T\n\nhint = TypeHint(MyGeneric[int])\nassert isinstance(hint, ClassTypeHint)\nassert hint.get_parameter_map() == {T: int}\n\nmember_hint = TypeHint(T).parameterize(hint.get_parameter_map())\nassert isinstance(member_hint, ClassTypeHint)\nassert member_hint.type is int\n```\n\nEvaluate forward references with `get_annotations()`:\n\n```py\n# cat <<EOF | python -\nfrom typeapi import get_annotations\nfrom typing import Optional\nfrom sys import version_info\n\nclass MyType:\n  a: "str | None"\n\nannotations = get_annotations(MyType)\n\nif version_info[:2] < (3, 10):\n  assert annotations == {"a": Optional[str]}\nelse:\n  assert annotations == {"a": str | None}\n```\n\nEvaluating forward references with the `TypeHint` API:\n\n```py\n# cat <<EOF | python -\nfrom typeapi import ClassTypeHint, ForwardRefTypeHint, TypeHint\n\nMyVector = "list[MyType]"\n\nclass MyType:\n  pass\n\nhint = TypeHint(MyVector).evaluate(globals())\nprint(hint)  # TypeHint(typing.List[__main__.MyType])\nassert isinstance(hint, ClassTypeHint)\nassert hint.type is list\n\nitem_hint = hint[0]\nassert isinstance(item_hint, ClassTypeHint)\nassert item_hint.type is MyType\n```\n',
     'author': 'Niklas Rosenstein',
     'author_email': 'rosensteinniklas@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

### Comparing `typeapi-1.4.2/PKG-INFO` & `typeapi-1.4.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: typeapi
-Version: 1.4.2
+Version: 1.4.3
 Summary: 
 License: MIT
 Author: Niklas Rosenstein
 Author-email: rosensteinniklas@gmail.com
 Requires-Python: >=3.6.3,<4.0.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

