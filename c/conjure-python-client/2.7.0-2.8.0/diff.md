# Comparing `tmp/conjure-python-client-2.7.0.tar.gz` & `tmp/conjure-python-client-2.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "conjure-python-client-2.7.0.tar", last modified: Thu Mar 16 01:26:02 2023, max compression
+gzip compressed data, was "conjure-python-client-2.8.0.tar", last modified: Sat May 13 13:12:52 2023, max compression
```

## Comparing `conjure-python-client-2.7.0.tar` & `conjure-python-client-2.8.0.tar`

### file list

```diff
@@ -1,32 +1,32 @@
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-03-16 01:26:02.954839 conjure-python-client-2.7.0/
--rw-r--r--   0 circleci  (3434) circleci  (3434)    11358 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/LICENSE
--rw-r--r--   0 circleci  (3434) circleci  (3434)      535 2023-03-16 01:26:02.954839 conjure-python-client-2.7.0/PKG-INFO
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1041 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/README.md
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-03-16 01:26:02.950839 conjure-python-client-2.7.0/conjure_python_client/
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1098 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/__init__.py
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-03-16 01:26:02.950839 conjure-python-client-2.7.0/conjure_python_client/_http/
--rw-r--r--   0 circleci  (3434) circleci  (3434)      881 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_http/__init__.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1052 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_http/configuration.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     9318 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_http/requests_client.py
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-03-16 01:26:02.950839 conjure-python-client-2.7.0/conjure_python_client/_lib/
--rw-r--r--   0 circleci  (3434) circleci  (3434)      889 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_lib/__init__.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)      778 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_lib/case.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1379 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_lib/sanitize.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     4358 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_lib/types.py
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-03-16 01:26:02.950839 conjure-python-client-2.7.0/conjure_python_client/_serde/
--rw-r--r--   0 circleci  (3434) circleci  (3434)      748 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_serde/__init__.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)    11006 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_serde/decoder.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     3060 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/_serde/encoder.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)       22 2023-03-16 01:26:02.000000 conjure-python-client-2.7.0/conjure_python_client/_version.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)        0 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/conjure_python_client/py.typed
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-03-16 01:26:02.950839 conjure-python-client-2.7.0/conjure_python_client.egg-info/
--rw-r--r--   0 circleci  (3434) circleci  (3434)      535 2023-03-16 01:26:02.000000 conjure-python-client-2.7.0/conjure_python_client.egg-info/PKG-INFO
--rw-r--r--   0 circleci  (3434) circleci  (3434)      790 2023-03-16 01:26:02.000000 conjure-python-client-2.7.0/conjure_python_client.egg-info/SOURCES.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)        1 2023-03-16 01:26:02.000000 conjure-python-client-2.7.0/conjure_python_client.egg-info/dependency_links.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)        9 2023-03-16 01:26:02.000000 conjure-python-client-2.7.0/conjure_python_client.egg-info/requires.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)       22 2023-03-16 01:26:02.000000 conjure-python-client-2.7.0/conjure_python_client.egg-info/top_level.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)       38 2023-03-16 01:26:02.954839 conjure-python-client-2.7.0/setup.cfg
--rw-r--r--   0 circleci  (3434) circleci  (3434)     3446 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/setup.py
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-03-16 01:26:02.950839 conjure-python-client-2.7.0/test/
--rw-r--r--   0 circleci  (3434) circleci  (3434)     6219 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/test/test_http.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)      774 2023-03-16 01:25:56.000000 conjure-python-client-2.7.0/test/test_version.py
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-05-13 13:12:52.243853 conjure-python-client-2.8.0/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)    11358 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/LICENSE
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      535 2023-05-13 13:12:52.243853 conjure-python-client-2.8.0/PKG-INFO
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     1041 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/README.md
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-05-13 13:12:52.239853 conjure-python-client-2.8.0/conjure_python_client/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     1098 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/__init__.py
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-05-13 13:12:52.243853 conjure-python-client-2.8.0/conjure_python_client/_http/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      881 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_http/__init__.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     1052 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_http/configuration.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     9646 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_http/requests_client.py
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-05-13 13:12:52.243853 conjure-python-client-2.8.0/conjure_python_client/_lib/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      889 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_lib/__init__.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      778 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_lib/case.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     1379 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_lib/sanitize.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     4358 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_lib/types.py
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-05-13 13:12:52.243853 conjure-python-client-2.8.0/conjure_python_client/_serde/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      748 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_serde/__init__.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)    14273 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_serde/decoder.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     3060 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/_serde/encoder.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)       22 2023-05-13 13:12:52.000000 conjure-python-client-2.8.0/conjure_python_client/_version.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)        0 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/conjure_python_client/py.typed
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-05-13 13:12:52.239853 conjure-python-client-2.8.0/conjure_python_client.egg-info/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      535 2023-05-13 13:12:52.000000 conjure-python-client-2.8.0/conjure_python_client.egg-info/PKG-INFO
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      790 2023-05-13 13:12:52.000000 conjure-python-client-2.8.0/conjure_python_client.egg-info/SOURCES.txt
+-rw-r--r--   0 circleci  (3434) circleci  (3434)        1 2023-05-13 13:12:52.000000 conjure-python-client-2.8.0/conjure_python_client.egg-info/dependency_links.txt
+-rw-r--r--   0 circleci  (3434) circleci  (3434)        9 2023-05-13 13:12:52.000000 conjure-python-client-2.8.0/conjure_python_client.egg-info/requires.txt
+-rw-r--r--   0 circleci  (3434) circleci  (3434)       22 2023-05-13 13:12:52.000000 conjure-python-client-2.8.0/conjure_python_client.egg-info/top_level.txt
+-rw-r--r--   0 circleci  (3434) circleci  (3434)       38 2023-05-13 13:12:52.243853 conjure-python-client-2.8.0/setup.cfg
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     3446 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/setup.py
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2023-05-13 13:12:52.243853 conjure-python-client-2.8.0/test/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     6219 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/test/test_http.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      774 2023-05-13 13:12:45.000000 conjure-python-client-2.8.0/test/test_version.py
```

### Comparing `conjure-python-client-2.7.0/LICENSE` & `conjure-python-client-2.8.0/LICENSE`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/PKG-INFO` & `conjure-python-client-2.8.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.2
 Name: conjure-python-client
-Version: 2.7.0
+Version: 2.8.0
 Summary: Conjure Python Library
 Home-page: https://github.com/palantir/conjure-python-client
 Author: Palantir Technologies, Inc.
 License: UNKNOWN
 Description: UNKNOWN
 Platform: UNKNOWN
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `conjure-python-client-2.7.0/README.md` & `conjure-python-client-2.8.0/README.md`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/__init__.py` & `conjure-python-client-2.8.0/conjure_python_client/__init__.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_http/__init__.py` & `conjure-python-client-2.8.0/conjure_python_client/_http/__init__.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_http/configuration.py` & `conjure-python-client-2.8.0/conjure_python_client/_http/configuration.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_http/requests_client.py` & `conjure-python-client-2.8.0/conjure_python_client/_http/requests_client.py`

 * *Files 4% similar despite different names*

```diff
@@ -59,28 +59,33 @@
 
 class Service(object):
     _requests_session: requests.Session
     _uris: List[str]
     _connect_timeout: float
     _read_timeout: float
     _verify: str
+    _return_none_for_unknown_union_types: bool
 
     def __init__(
         self,
         requests_session: requests.Session,
         uris: List[str],
         _connect_timeout: float,
         _read_timeout: float,
         _verify: str,
+        _return_none_for_unknown_union_types: bool = False,
     ) -> None:
         self._requests_session = requests_session
         self._uris = uris
         self._connect_timeout = _connect_timeout
         self._read_timeout = _read_timeout
         self._verify = _verify
+        self._return_none_for_unknown_union_types = (
+            _return_none_for_unknown_union_types
+        )
 
     @property
     def _uri(self) -> str:
         """returns a random uri"""
         return random.SystemRandom().choice(self._uris)
 
     def _request(self, *args, **kwargs) -> Response:
@@ -154,14 +159,15 @@
 class RequestsClient(object):
     @classmethod
     def create(
         cls,
         service_class: Type[T],
         user_agent: str,
         service_config: ServiceConfiguration,
+        return_none_for_unknown_union_types: bool = False,
     ) -> T:
         # setup retry to match java remoting
         # https://github.com/palantir/http-remoting/tree/3.12.0#quality-of-service-retry-failover-throttling
         retry = RetryWithJitter(
             total=service_config.max_num_retries,
             read=0,  # do not retry read errors
             status_forcelist=[308, 429, 503],
@@ -179,14 +185,15 @@
             session.mount(uri, transport_adapter)
         return service_class(  # type: ignore
             session,
             service_config.uris,
             service_config.connect_timeout,
             service_config.read_timeout,
             verify,
+            return_none_for_unknown_union_types,
         )
 
 
 class TransportAdapter(HTTPAdapter):
     """Transport adapter that allows customising ssl things"""
 
     def init_poolmanager(
```

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_lib/__init__.py` & `conjure-python-client-2.8.0/conjure_python_client/_lib/__init__.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_lib/case.py` & `conjure-python-client-2.8.0/conjure_python_client/_lib/case.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_lib/sanitize.py` & `conjure-python-client-2.8.0/conjure_python_client/_lib/sanitize.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_lib/types.py` & `conjure-python-client-2.8.0/conjure_python_client/_lib/types.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_serde/__init__.py` & `conjure-python-client-2.8.0/conjure_python_client/_serde/__init__.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_serde/decoder.py` & `conjure-python-client-2.8.0/conjure_python_client/_serde/decoder.py`

 * *Files 25% similar despite different names*

```diff
@@ -31,22 +31,27 @@
 NoneType = type(None)
 
 
 class ConjureDecoder(object):
     """Decodes json into a conjure object"""
 
     @classmethod
-    def decode_conjure_bean_type(cls, obj, conjure_type):
+    def decode_conjure_bean_type(
+        cls, obj, conjure_type, return_none_for_unknown_union_types=False
+    ):
         """Decodes json into a conjure bean type (a plain bean, not enum
         or union).
 
         Args:
             obj: the json object to decode
             conjure_type: a class object which is the bean type
                 we're decoding into
+            return_none_for_unknown_union_types: if set to True, returns None
+                instead of raising an exception when an unknown union type is
+                encountered
         Returns:
             A instance of a bean of type conjure_type.
         """
         deserialized: Dict[str, Any] = {}
         for (
             python_arg_name,
             field_definition,
@@ -57,15 +62,15 @@
                 cls.check_null_field(
                     obj, deserialized, python_arg_name, field_definition
                 )
             else:
                 value = obj[field_identifier]
                 field_type = field_definition.field_type
                 deserialized[python_arg_name] = cls.do_decode(
-                    value, field_type
+                    value, field_type, return_none_for_unknown_union_types
                 )
         return conjure_type(**deserialized)
 
     @classmethod
     def check_null_field(
         cls, obj, deserialized, python_arg_name, field_definition
     ):
@@ -86,46 +91,56 @@
             raise Exception(
                 "field {} not found in object {}".format(
                     field_definition.identifier, obj
                 )
             )
 
     @classmethod
-    def decode_conjure_union_type(cls, obj, conjure_type):
+    def decode_conjure_union_type(
+        cls, obj, conjure_type, return_none_for_unknown_union_types=False
+    ):
         """Decodes json into a conjure union type.
 
         Args:
             obj: the json object to decode
             conjure_type: a class object which is the union type
                 we're decoding into
+            return_none_for_unknown_union_types: if set to True, returns None
+                instead of raising an exception when an unknown union type is
+                encountered
         Returns:
             An instance of type conjure_type.
         """
         type_of_union: str = obj["type"]
         for attr, conjure_field in conjure_type._options().items():
             if conjure_field.identifier == type_of_union:
                 attribute = attr
                 conjure_field_definition = conjure_field
                 break
         else:
-            raise ValueError(
-                "unknown union type {0} for {1}".format(
-                    type_of_union, conjure_type
+            if return_none_for_unknown_union_types:
+                return None
+            else:
+                raise ValueError(
+                    "unknown union type {0} for {1}".format(
+                        type_of_union, conjure_type
+                    )
                 )
-            )
 
         deserialized: Dict[str, Any] = {}
         if type_of_union not in obj or obj[type_of_union] is None:
             cls.check_null_field(
                 obj, deserialized, attribute, conjure_field_definition
             )
         else:
             value = obj[type_of_union]
             field_type = conjure_field_definition.field_type
-            deserialized[attribute] = cls.do_decode(value, field_type)
+            deserialized[attribute] = cls.do_decode(
+                value, field_type, return_none_for_unknown_union_types
+            )
 
         # for backwards compatibility with conjure-python,
         # only pass in arg type_of_union if it is expected
         param_dict = inspect.signature(conjure_type.__init__).parameters
         if 'type_of_union' in param_dict:
             deserialized['type_of_union'] = type_of_union
         return conjure_type(**deserialized)
@@ -156,24 +171,28 @@
 
     @classmethod
     def decode_dict(
         cls,
         obj: Dict[Any, Any],
         key_type: Type[DecodableType],
         item_type: Type[DecodableType],
+        return_none_for_unknown_union_types: bool = False,
     ) -> Dict[Any, Any]:
         """Decodes json into a dictionary, handling conversion of the
         keys/values (the keys/values may themselves require conversion).
 
         Args:
             obj: the json object to decode
             key_type: a class object which is the conjure type
                 of the keys in this dict
             item_type: a class object which is the conjure type
                 of the values in this dict
+            return_none_for_unknown_union_types: if set to True, returns None
+                instead of raising an exception when an unknown union type is
+                encountered
         Returns:
             A python dictionary, where the keys are instances of type key_type
             and the values are of type value_type.
         """
         if not isinstance(obj, dict):
             raise Exception("expected a python dict")
         if (
@@ -184,68 +203,101 @@
                 inspect.isclass(key_type)
                 and issubclass(key_type, ConjureEnumType)
             )
         ):
             return dict(
                 (
                     (
-                        cls.do_decode(x[0], key_type),
-                        cls.do_decode(x[1], item_type),
+                        cls.do_decode(
+                            x[0], key_type, return_none_for_unknown_union_types
+                        ),
+                        cls.do_decode(
+                            x[1],
+                            item_type,
+                            return_none_for_unknown_union_types,
+                        ),
                     )
                     for x in obj.items()
                 )
             )
 
         return dict(
             (
                 (
-                    cls.do_decode(json.loads(x[0]), key_type),
-                    cls.do_decode(x[1], item_type),
+                    cls.do_decode(
+                        json.loads(x[0]),
+                        key_type,
+                        return_none_for_unknown_union_types,
+                    ),
+                    cls.do_decode(
+                        x[1], item_type, return_none_for_unknown_union_types
+                    ),
                 )
                 for x in obj.items()
             )
         )
 
     @classmethod
     def decode_list(
-        cls, obj: List[Any], element_type: Type[DecodableType]
+        cls,
+        obj: List[Any],
+        element_type: Type[DecodableType],
+        return_none_for_unknown_union_types: bool = False,
     ) -> List[Any]:
         """Decodes json into a list, handling conversion of the elements.
 
         Args:
             obj: the json object to decode
             element_type: a class object which is the conjure type of
                 the elements in this list.
+            return_none_for_unknown_union_types: if set to True, returns None
+                instead of raising an exception when an unknown union type is
+                encountered
         Returns:
             A python list where the elements are instances of type
                 element_type.
         """
         if not isinstance(obj, list):
             raise Exception("expected a python list")
 
-        return list(map(lambda x: cls.do_decode(x, element_type), obj))
+        return list(
+            map(
+                lambda x: cls.do_decode(
+                    x, element_type, return_none_for_unknown_union_types
+                ),
+                obj,
+            )
+        )
 
     @classmethod
     def decode_optional(
-        cls, obj: Optional[Any], object_type: Type[DecodableType]
+        cls,
+        obj: Optional[Any],
+        object_type: Type[DecodableType],
+        return_none_for_unknown_union_types: bool = False,
     ) -> Optional[Any]:
         """Decodes json into an element, returning None if the provided object
         is None.
 
         Args:
             obj: the json object to decode
             object_type: a class object which is the conjure type of
                 the object if present.
+            return_none_for_unknown_union_types: if set to True, returns None
+                instead of raising an exception when an unknown union type is
+                encountered
         Returns:
             The decoded obj or None if no obj is provided.
         """
         if obj is None:
             return None
 
-        return cls.do_decode(obj, object_type)
+        return cls.do_decode(
+            obj, object_type, return_none_for_unknown_union_types
+        )
 
     @classmethod
     def decode_primitive(cls, obj, object_type):
         def raise_mismatch():
             raise Exception(
                 "Expected to find {} type but found {} instead".format(
                     object_type, type(obj)
@@ -266,60 +318,99 @@
                 raise_mismatch()
         elif not isinstance(obj, object_type):
             raise_mismatch()
 
         return obj
 
     @classmethod
-    def do_decode(cls, obj: Any, obj_type: Type[DecodableType]) -> Any:
+    def do_decode(
+        cls,
+        obj: Any,
+        obj_type: Type[DecodableType],
+        return_none_for_unknown_union_types: bool = False,
+    ) -> Any:
         """Decodes json into the specified type
 
         Args:
             obj: the json object to decode
             obj_type: a class object which is the type we're decoding into.
+            return_none_for_unknown_union_types: if set to True, returns None
+                instead of raising an exception when an unknown union type is
+                encountered
         """
 
         type_origin = get_origin(obj_type)
         type_args = get_args(obj_type)
 
         if inspect.isclass(obj_type) and issubclass(obj_type, ConjureBeanType):
-            return cls.decode_conjure_bean_type(obj, obj_type)
+            return cls.decode_conjure_bean_type(
+                obj, obj_type, return_none_for_unknown_union_types
+            )
 
         elif inspect.isclass(obj_type) and issubclass(
             obj_type, ConjureUnionType
         ):
-            return cls.decode_conjure_union_type(obj, obj_type)
+            return cls.decode_conjure_union_type(
+                obj, obj_type, return_none_for_unknown_union_types
+            )
 
         elif inspect.isclass(obj_type) and issubclass(
             obj_type, ConjureEnumType
         ):
             return cls.decode_conjure_enum_type(obj, obj_type)
 
         elif isinstance(obj_type, DictType):
-            return cls.decode_dict(obj, obj_type.key_type, obj_type.value_type)
+            return cls.decode_dict(
+                obj,
+                obj_type.key_type,
+                obj_type.value_type,
+                return_none_for_unknown_union_types,
+            )
 
         elif isinstance(obj_type, ListType):
-            return cls.decode_list(obj, obj_type.item_type)
+            return cls.decode_list(
+                obj, obj_type.item_type, return_none_for_unknown_union_types
+            )
 
         elif isinstance(obj_type, OptionalType):
-            return cls.decode_optional(obj, obj_type.item_type)
+            return cls.decode_optional(
+                obj, obj_type.item_type, return_none_for_unknown_union_types
+            )
 
         elif type_origin is OptionalTypeWrapper:
-            return cls.decode_optional(obj, type_args[0])
+            return cls.decode_optional(
+                obj, type_args[0], return_none_for_unknown_union_types
+            )
 
         elif type_origin is dict:
             (key_type, value_type) = type_args
-            return cls.decode_dict(obj, key_type, value_type)
+            return cls.decode_dict(
+                obj, key_type, value_type, return_none_for_unknown_union_types
+            )
 
         elif type_origin is list:
-            return cls.decode_list(obj, type_args[0])
+            return cls.decode_list(
+                obj, type_args[0], return_none_for_unknown_union_types
+            )
 
         return cls.decode_primitive(obj, obj_type)
 
-    def decode(self, obj: Any, obj_type: Type[DecodableType]) -> Any:
-        return self.do_decode(obj, obj_type)
+    def decode(
+        self,
+        obj: Any,
+        obj_type: Type[DecodableType],
+        return_none_for_unknown_union_types: bool = False,
+    ) -> Any:
+        return self.do_decode(
+            obj, obj_type, return_none_for_unknown_union_types
+        )
 
     def read_from_string(
-        self, string_value: str, obj_type: Type[DecodableType]
+        self,
+        string_value: str,
+        obj_type: Type[DecodableType],
+        return_none_for_unknown_union_types: bool = False,
     ) -> Any:
         deserialized = json.loads(string_value)
-        return self.decode(deserialized, obj_type)
+        return self.decode(
+            deserialized, obj_type, return_none_for_unknown_union_types
+        )
```

### Comparing `conjure-python-client-2.7.0/conjure_python_client/_serde/encoder.py` & `conjure-python-client-2.8.0/conjure_python_client/_serde/encoder.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/conjure_python_client.egg-info/PKG-INFO` & `conjure-python-client-2.8.0/conjure_python_client.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.2
 Name: conjure-python-client
-Version: 2.7.0
+Version: 2.8.0
 Summary: Conjure Python Library
 Home-page: https://github.com/palantir/conjure-python-client
 Author: Palantir Technologies, Inc.
 License: UNKNOWN
 Description: UNKNOWN
 Platform: UNKNOWN
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `conjure-python-client-2.7.0/conjure_python_client.egg-info/SOURCES.txt` & `conjure-python-client-2.8.0/conjure_python_client.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/setup.py` & `conjure-python-client-2.8.0/setup.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/test/test_http.py` & `conjure-python-client-2.8.0/test/test_http.py`

 * *Files identical despite different names*

### Comparing `conjure-python-client-2.7.0/test/test_version.py` & `conjure-python-client-2.8.0/test/test_version.py`

 * *Files identical despite different names*

