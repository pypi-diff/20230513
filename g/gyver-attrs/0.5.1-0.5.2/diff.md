# Comparing `tmp/gyver_attrs-0.5.1.tar.gz` & `tmp/gyver_attrs-0.5.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gyver_attrs-0.5.1.tar", max compression
+gzip compressed data, was "gyver_attrs-0.5.2.tar", max compression
```

## Comparing `gyver_attrs-0.5.1.tar` & `gyver_attrs-0.5.2.tar`

### file list

```diff
@@ -1,22 +1,22 @@
--rw-r--r--   0        0        0    11352 2023-04-26 20:21:33.954424 gyver_attrs-0.5.1/LICENSE
--rw-r--r--   0        0        0     5279 2023-04-26 20:21:33.954424 gyver_attrs-0.5.1/README.md
--rw-r--r--   0        0        0       80 2023-04-26 20:21:33.954424 gyver_attrs-0.5.1/gyver/__init__.py
--rw-r--r--   0        0        0      543 2023-04-26 20:34:05.470429 gyver_attrs-0.5.1/gyver/attrs/__init__.py
--rw-r--r--   0        0        0     3132 2023-04-26 20:27:13.432336 gyver_attrs-0.5.1/gyver/attrs/camel.py
--rw-r--r--   0        0        0      146 2023-04-26 20:21:33.954424 gyver_attrs-0.5.1/gyver/attrs/converters/__init__.py
--rw-r--r--   0        0        0      751 2023-04-26 20:21:33.954424 gyver_attrs-0.5.1/gyver/attrs/converters/json.py
--rw-r--r--   0        0        0     1516 2023-04-26 20:21:33.954424 gyver_attrs-0.5.1/gyver/attrs/converters/utils.py
--rw-r--r--   0        0        0     5493 2023-04-26 20:27:12.428348 gyver_attrs-0.5.1/gyver/attrs/field.py
--rw-r--r--   0        0        0     1046 2023-04-26 20:27:13.436336 gyver_attrs-0.5.1/gyver/attrs/helpers.py
--rw-r--r--   0        0        0    24627 2023-04-26 20:27:13.447335 gyver_attrs-0.5.1/gyver/attrs/main.py
--rw-r--r--   0        0        0     4793 2023-04-26 20:27:12.441348 gyver_attrs-0.5.1/gyver/attrs/methods.py
--rw-r--r--   0        0        0        0 2023-04-26 20:21:33.955424 gyver_attrs-0.5.1/gyver/attrs/py.typed
--rw-r--r--   0        0        0     3872 2023-04-26 20:27:13.451335 gyver_attrs-0.5.1/gyver/attrs/resolver.py
--rw-r--r--   0        0        0     4048 2023-04-26 20:27:13.454335 gyver_attrs-0.5.1/gyver/attrs/schema.py
--rw-r--r--   0        0        0     4376 2023-04-26 20:27:13.455335 gyver_attrs-0.5.1/gyver/attrs/shortcuts.py
--rw-r--r--   0        0        0        0 2023-04-26 20:21:33.955424 gyver_attrs-0.5.1/gyver/attrs/utils/__init__.py
--rw-r--r--   0        0        0      604 2023-04-26 20:21:33.955424 gyver_attrs-0.5.1/gyver/attrs/utils/factory.py
--rw-r--r--   0        0        0     1441 2023-04-26 20:27:12.347349 gyver_attrs-0.5.1/gyver/attrs/utils/functions.py
--rw-r--r--   0        0        0      298 2023-04-26 20:21:33.955424 gyver_attrs-0.5.1/gyver/attrs/utils/typedef.py
--rw-r--r--   0        0        0      655 2023-04-26 20:34:05.469429 gyver_attrs-0.5.1/pyproject.toml
--rw-r--r--   0        0        0     5824 1970-01-01 00:00:00.000000 gyver_attrs-0.5.1/PKG-INFO
+-rw-r--r--   0        0        0    11352 2023-04-26 20:21:33.954424 gyver_attrs-0.5.2/LICENSE
+-rw-r--r--   0        0        0     5279 2023-04-26 20:21:33.954424 gyver_attrs-0.5.2/README.md
+-rw-r--r--   0        0        0       80 2023-04-26 20:21:33.954424 gyver_attrs-0.5.2/gyver/__init__.py
+-rw-r--r--   0        0        0      543 2023-05-13 16:46:32.485325 gyver_attrs-0.5.2/gyver/attrs/__init__.py
+-rw-r--r--   0        0        0     3132 2023-04-26 20:27:13.432336 gyver_attrs-0.5.2/gyver/attrs/camel.py
+-rw-r--r--   0        0        0      146 2023-04-26 20:21:33.954424 gyver_attrs-0.5.2/gyver/attrs/converters/__init__.py
+-rw-r--r--   0        0        0      751 2023-04-26 20:21:33.954424 gyver_attrs-0.5.2/gyver/attrs/converters/json.py
+-rw-r--r--   0        0        0     1516 2023-04-26 20:21:33.954424 gyver_attrs-0.5.2/gyver/attrs/converters/utils.py
+-rw-r--r--   0        0        0     5493 2023-04-26 20:27:12.428348 gyver_attrs-0.5.2/gyver/attrs/field.py
+-rw-r--r--   0        0        0     1046 2023-04-26 20:27:13.436336 gyver_attrs-0.5.2/gyver/attrs/helpers.py
+-rw-r--r--   0        0        0    24627 2023-04-26 20:27:13.447335 gyver_attrs-0.5.2/gyver/attrs/main.py
+-rw-r--r--   0        0        0     4793 2023-04-26 20:27:12.441348 gyver_attrs-0.5.2/gyver/attrs/methods.py
+-rw-r--r--   0        0        0        0 2023-04-26 20:21:33.955424 gyver_attrs-0.5.2/gyver/attrs/py.typed
+-rw-r--r--   0        0        0     3872 2023-04-26 20:27:13.451335 gyver_attrs-0.5.2/gyver/attrs/resolver.py
+-rw-r--r--   0        0        0     4048 2023-04-26 20:27:13.454335 gyver_attrs-0.5.2/gyver/attrs/schema.py
+-rw-r--r--   0        0        0     4391 2023-05-13 16:44:54.697409 gyver_attrs-0.5.2/gyver/attrs/shortcuts.py
+-rw-r--r--   0        0        0        0 2023-04-26 20:21:33.955424 gyver_attrs-0.5.2/gyver/attrs/utils/__init__.py
+-rw-r--r--   0        0        0      604 2023-04-26 20:21:33.955424 gyver_attrs-0.5.2/gyver/attrs/utils/factory.py
+-rw-r--r--   0        0        0     1441 2023-04-26 20:27:12.347349 gyver_attrs-0.5.2/gyver/attrs/utils/functions.py
+-rw-r--r--   0        0        0      298 2023-04-26 20:21:33.955424 gyver_attrs-0.5.2/gyver/attrs/utils/typedef.py
+-rw-r--r--   0        0        0      655 2023-05-13 16:46:32.483325 gyver_attrs-0.5.2/pyproject.toml
+-rw-r--r--   0        0        0     5824 1970-01-01 00:00:00.000000 gyver_attrs-0.5.2/PKG-INFO
```

### Comparing `gyver_attrs-0.5.1/LICENSE` & `gyver_attrs-0.5.2/LICENSE`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/README.md` & `gyver_attrs-0.5.2/README.md`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/__init__.py` & `gyver_attrs-0.5.2/gyver/attrs/__init__.py`

 * *Files 21% similar despite different names*

```diff
@@ -17,9 +17,9 @@
     "fromjson",
     "fields",
     "call_init",
     "mutable",
     "kw_only",
 ]
 
-__version__ = "0.5.1"
+__version__ = "0.5.2"
 __version_info__ = tuple(map(int, __version__.split(".")))
```

### Comparing `gyver_attrs-0.5.1/gyver/attrs/camel.py` & `gyver_attrs-0.5.2/gyver/attrs/camel.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/converters/json.py` & `gyver_attrs-0.5.2/gyver/attrs/converters/json.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/converters/utils.py` & `gyver_attrs-0.5.2/gyver/attrs/converters/utils.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/field.py` & `gyver_attrs-0.5.2/gyver/attrs/field.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/helpers.py` & `gyver_attrs-0.5.2/gyver/attrs/helpers.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/main.py` & `gyver_attrs-0.5.2/gyver/attrs/main.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/methods.py` & `gyver_attrs-0.5.2/gyver/attrs/methods.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/resolver.py` & `gyver_attrs-0.5.2/gyver/attrs/resolver.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/schema.py` & `gyver_attrs-0.5.2/gyver/attrs/schema.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/shortcuts.py` & `gyver_attrs-0.5.2/gyver/attrs/shortcuts.py`

 * *Files 3% similar despite different names*

```diff
@@ -18,16 +18,16 @@
     *,
     kw_only: bool = False,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    pydantic: bool = True,
-    dataclass_fields: bool = True,
+    pydantic: bool = False,
+    dataclass_fields: bool = False,
 ) -> typing.Callable[[type[T]], type[T]]:
     ...
 
 
 @typing.overload
 def mutable(
     maybe_cls: type[T],
@@ -35,16 +35,16 @@
     *,
     kw_only: bool = False,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    pydantic: bool = True,
-    dataclass_fields: bool = True,
+    pydantic: bool = False,
+    dataclass_fields: bool = False,
 ) -> type[T]:
     ...
 
 
 @typing_extensions.dataclass_transform(
     order_default=True,
     frozen_default=False,
@@ -57,16 +57,16 @@
     *,
     kw_only: bool = False,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    pydantic: bool = True,
-    dataclass_fields: bool = True,
+    pydantic: bool = False,
+    dataclass_fields: bool = False,
 ) -> ReturnT[T]:
     return define(
         maybe_cls,
         frozen=False,
         kw_only=kw_only,
         slots=slots,
         repr=repr,
@@ -85,16 +85,16 @@
     *,
     frozen: bool = False,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    pydantic: bool = True,
-    dataclass_fields: bool = True,
+    pydantic: bool = False,
+    dataclass_fields: bool = False,
 ) -> typing.Callable[[type[T]], type[T]]:
     ...
 
 
 @typing.overload
 def kw_only(
     maybe_cls: type[T],
@@ -102,16 +102,16 @@
     *,
     frozen: bool = False,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    pydantic: bool = True,
-    dataclass_fields: bool = True,
+    pydantic: bool = False,
+    dataclass_fields: bool = False,
 ) -> type[T]:
     ...
 
 
 @typing_extensions.dataclass_transform(
     order_default=True,
     frozen_default=True,
@@ -124,16 +124,16 @@
     *,
     frozen: bool = True,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    pydantic: bool = True,
-    dataclass_fields: bool = True,
+    pydantic: bool = False,
+    dataclass_fields: bool = False,
 ) -> ReturnT[T]:
     return define(
         maybe_cls,
         frozen=frozen,
         kw_only=True,
         slots=slots,
         repr=repr,
@@ -153,15 +153,15 @@
     frozen: bool = False,
     kw_only: bool = False,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    dataclass_fields: bool = True,
+    dataclass_fields: bool = False,
 ) -> typing.Callable[[type[T]], type[T]]:
     ...
 
 
 @typing.overload
 def schema_class(
     maybe_cls: type[T],
@@ -170,15 +170,15 @@
     frozen: bool = False,
     kw_only: bool = False,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    dataclass_fields: bool = True,
+    dataclass_fields: bool = False,
 ) -> type[T]:
     ...
 
 
 @typing_extensions.dataclass_transform(
     order_default=True,
     frozen_default=True,
@@ -192,15 +192,15 @@
     frozen: bool = True,
     kw_only: bool = False,
     slots: bool = True,
     repr: bool = True,
     eq: bool = True,
     order: bool = True,
     hash: typing.Optional[bool] = None,
-    dataclass_fields: bool = True,
+    dataclass_fields: bool = False,
 ) -> ReturnT[T]:
     return define(
         maybe_cls,
         frozen=frozen,
         kw_only=kw_only,
         slots=slots,
         repr=repr,
```

### Comparing `gyver_attrs-0.5.1/gyver/attrs/utils/factory.py` & `gyver_attrs-0.5.2/gyver/attrs/utils/factory.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/gyver/attrs/utils/functions.py` & `gyver_attrs-0.5.2/gyver/attrs/utils/functions.py`

 * *Files identical despite different names*

### Comparing `gyver_attrs-0.5.1/pyproject.toml` & `gyver_attrs-0.5.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "gyver-attrs"
-version = "0.5.1"
+version = "0.5.2"
 description = ""
 authors = ["Gustavo Cardoso <self.gustavocorrea@gmail.com>"]
 readme = "README.md"
 packages = [{ include = "gyver" }]
 
 [tool.poetry.dependencies]
 python = "^3.9"
```

### Comparing `gyver_attrs-0.5.1/PKG-INFO` & `gyver_attrs-0.5.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gyver-attrs
-Version: 0.5.1
+Version: 0.5.2
 Summary: 
 Author: Gustavo Cardoso
 Author-email: self.gustavocorrea@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

