# Comparing `tmp/garlandtools_async-0.1.1.tar.gz` & `tmp/garlandtools_async-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "garlandtools_async-0.1.1.tar", max compression
+gzip compressed data, was "garlandtools_async-0.1.2.tar", max compression
```

## Comparing `garlandtools_async-0.1.1.tar` & `garlandtools_async-0.1.2.tar`

### file list

```diff
@@ -1,12 +1,15 @@
--rw-r--r--   0        0        0     1069 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/LICENSE
--rw-r--r--   0        0        0      571 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/README.md
--rw-r--r--   0        0        0       62 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/garlandtools/__init__.py
--rw-r--r--   0        0        0     1722 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/garlandtools/client.py
--rw-r--r--   0        0        0      112 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/garlandtools/models/__init__.py
--rw-r--r--   0        0        0      152 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/garlandtools/models/lang.py
--rw-r--r--   0        0        0       66 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/garlandtools/models/partials/__init__.py
--rw-r--r--   0        0        0      588 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/garlandtools/models/partials/item_partial.py
--rw-r--r--   0        0        0      309 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/garlandtools/models/partials/partial.py
--rw-r--r--   0        0        0      328 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/garlandtools/models/type.py
--rw-r--r--   0        0        0      593 2023-05-11 22:05:50.630530 garlandtools_async-0.1.1/pyproject.toml
--rw-r--r--   0        0        0     1084 1970-01-01 00:00:00.000000 garlandtools_async-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/LICENSE
+-rw-r--r--   0        0        0      571 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/__init__.py
+-rw-r--r--   0        0        0     2398 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/client.py
+-rw-r--r--   0        0        0        0 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/__init__.py
+-rw-r--r--   0        0        0      152 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/lang.py
+-rw-r--r--   0        0        0        0 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/partials/__init__.py
+-rw-r--r--   0        0        0      588 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/partials/item_partial.py
+-rw-r--r--   0        0        0      308 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/partials/partial.py
+-rw-r--r--   0        0        0     2175 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/records/base_record.py
+-rw-r--r--   0        0        0     1253 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/records/factory.py
+-rw-r--r--   0        0        0     2782 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/records/item.py
+-rw-r--r--   0        0        0      328 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/garlandtools/models/type.py
+-rw-r--r--   0        0        0      593 2023-05-13 16:28:23.700816 garlandtools_async-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0     1084 1970-01-01 00:00:00.000000 garlandtools_async-0.1.2/PKG-INFO
```

### Comparing `garlandtools_async-0.1.1/LICENSE` & `garlandtools_async-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `garlandtools_async-0.1.1/README.md` & `garlandtools_async-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `garlandtools_async-0.1.1/garlandtools/client.py` & `garlandtools_async-0.1.2/garlandtools/client.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,29 +1,37 @@
-from typing import Any, Dict, List, Optional
+from typing import Any
 
 from aiohttp import ClientSession
 
-from garlandtools.models import Lang, Type
+from garlandtools.models.lang import Lang
+from garlandtools.models.records.base_record import BaseRecord
+from garlandtools.models.records.factory import partial_factory, record_factory
+from garlandtools.models.type import Type
 
 
 class Client:
     base_url = "https://garlandtools.org/api/"
 
-    def __init__(self, session: Optional[ClientSession] = None):
+    def __init__(
+        self,
+        session: ClientSession | None = None,
+        lang: Lang = Lang.EN,
+    ):
         self._session = session
+        self.lang = lang
 
     @property
     def session(self) -> ClientSession:
         if self._session is None or self._session.closed:
             self._session = ClientSession()
         return self._session
 
     async def search(
-        self, query: str, type: Optional[Type], exact: Optional[bool] = False
-    ) -> List[Dict]:
+        self, query: str, type: Type | None = None, exact: bool = False
+    ) -> list[BaseRecord]:
         """Search Garland Tools for the given query.
 
         Filters are not yet implemented.
 
         :param query: The query to search for.
         :param type: The record type you want to search for.
         :param exact: If the query should be an exact match.
@@ -31,24 +39,35 @@
         params = {"text": query}
         if type is not None:
             params["type"] = type.value
         if exact:
             params["exact"] = "true"
         result = await self._get("search.php", params=params)
 
-        return result
+        return [partial_factory(r, client=self) for r in result]
 
-    def get_by_id(self, id: int, type: Type, lang: Lang):
+    async def _get_by_id(self, id: int, type: Type):
+        params = {
+            "id": id,
+            "type": type.value,
+            "lang": self.lang.value,
+            "version": 3 if type == type.LEVE or type == type.ITEM else 2,
+        }
+        return await self._get("get.php", params=params)
+
+    async def get_by_id(self, id: int, type: Type):
         """Get a record by its ID.
 
         :param id: The ID of the record.
         :param type: The type of the record.
         :param lang: The language of the record.
         """
+        result = await self._get_by_id(id, type)
+        return record_factory(type, result, self)
 
-    async def _get(self, path: str, params: Optional[dict] = None) -> Any:
+    async def _get(self, path: str, params: dict | None = None) -> Any:
         url = self.base_url + path
         async with self.session.get(url, params=params) as response:
             if response.status == 200:
                 return await response.json()
             else:
                 raise Exception(f"Received status code {response.status} from {url}")
```

### Comparing `garlandtools_async-0.1.1/garlandtools/models/partials/item_partial.py` & `garlandtools_async-0.1.2/garlandtools/models/partials/item_partial.py`

 * *Files identical despite different names*

### Comparing `garlandtools_async-0.1.1/pyproject.toml` & `garlandtools_async-0.1.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "garlandtools-async"
-version = "0.1.1"
+version = "0.1.2"
 description = "A async python wrapper for the https://garlandtools.org/ API"
 authors = ["Abigail Howe <abby@abigailhowe.org>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "garlandtools"}]
 
 [tool.poetry.dependencies]
```

### Comparing `garlandtools_async-0.1.1/PKG-INFO` & `garlandtools_async-0.1.2/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: garlandtools-async
-Version: 0.1.1
+Version: 0.1.2
 Summary: A async python wrapper for the https://garlandtools.org/ API
 License: MIT
 Author: Abigail Howe
 Author-email: abby@abigailhowe.org
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

