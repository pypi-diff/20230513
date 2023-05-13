# Comparing `tmp/ardilla-0.0.5a0.tar.gz` & `tmp/ardilla-0.0.6a0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ardilla-0.0.5a0.tar", last modified: Fri May 12 13:52:41 2023, max compression
+gzip compressed data, was "ardilla-0.0.6a0.tar", last modified: Sat May 13 04:31:48 2023, max compression
```

## Comparing `ardilla-0.0.5a0.tar` & `ardilla-0.0.6a0.tar`

### file list

```diff
@@ -1,29 +1,29 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 13:52:41.547533 ardilla-0.0.5a0/
--rw-rw-rw-   0        0        0     1084 2023-05-08 03:28:44.000000 ardilla-0.0.5a0/LICENCE
--rw-rw-rw-   0        0        0     3988 2023-05-12 13:52:41.546546 ardilla-0.0.5a0/PKG-INFO
--rw-rw-rw-   0        0        0     3297 2023-05-12 03:38:21.000000 ardilla-0.0.5a0/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 13:52:41.473536 ardilla-0.0.5a0/ardilla/
--rw-rw-rw-   0        0        0      106 2023-05-08 02:18:14.000000 ardilla-0.0.5a0/ardilla/__init__.py
--rw-rw-rw-   0        0        0     3189 2023-05-12 13:46:56.000000 ardilla-0.0.5a0/ardilla/abc.py
-drwxrwxrwx   0        0        0        0 2023-05-12 13:52:41.533535 ardilla-0.0.5a0/ardilla/asyncio/
--rw-rw-rw-   0        0        0       78 2023-05-08 16:29:21.000000 ardilla-0.0.5a0/ardilla/asyncio/__init__.py
--rw-rw-rw-   0        0        0      443 2023-05-12 13:48:16.000000 ardilla-0.0.5a0/ardilla/asyncio/abc.py
--rw-rw-rw-   0        0        0     6194 2023-05-12 13:48:41.000000 ardilla-0.0.5a0/ardilla/asyncio/crud.py
--rw-rw-rw-   0        0        0      922 2023-05-12 13:50:34.000000 ardilla-0.0.5a0/ardilla/asyncio/engine.py
--rw-rw-rw-   0        0        0     6312 2023-05-12 13:46:27.000000 ardilla-0.0.5a0/ardilla/crud.py
--rw-rw-rw-   0        0        0     1172 2023-05-12 13:46:42.000000 ardilla-0.0.5a0/ardilla/engine.py
--rw-rw-rw-   0        0        0      216 2023-05-11 02:46:57.000000 ardilla-0.0.5a0/ardilla/errors.py
--rw-rw-rw-   0        0        0     1475 2023-05-12 03:30:34.000000 ardilla-0.0.5a0/ardilla/models.py
--rw-rw-rw-   0        0        0     2126 2023-05-12 03:30:39.000000 ardilla-0.0.5a0/ardilla/schemas.py
-drwxrwxrwx   0        0        0        0 2023-05-12 13:52:41.520532 ardilla-0.0.5a0/ardilla.egg-info/
--rw-rw-rw-   0        0        0     3988 2023-05-12 13:52:41.000000 ardilla-0.0.5a0/ardilla.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      471 2023-05-12 13:52:41.000000 ardilla-0.0.5a0/ardilla.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 13:52:41.000000 ardilla-0.0.5a0/ardilla.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      144 2023-05-12 13:52:41.000000 ardilla-0.0.5a0/ardilla.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-12 13:52:41.000000 ardilla-0.0.5a0/ardilla.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      916 2023-05-12 03:39:21.000000 ardilla-0.0.5a0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-12 13:52:41.548537 ardilla-0.0.5a0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-05-12 13:52:41.543534 ardilla-0.0.5a0/tests/
--rw-rw-rw-   0        0        0     5291 2023-05-12 03:30:55.000000 ardilla-0.0.5a0/tests/test_async.py
--rw-rw-rw-   0        0        0      567 2023-05-12 03:32:46.000000 ardilla-0.0.5a0/tests/test_models.py
--rw-rw-rw-   0        0        0     4964 2023-05-12 03:31:02.000000 ardilla-0.0.5a0/tests/test_sync.py
+drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.122576 ardilla-0.0.6a0/
+-rw-rw-rw-   0        0        0     1084 2023-05-08 03:28:44.000000 ardilla-0.0.6a0/LICENCE
+-rw-rw-rw-   0        0        0     3988 2023-05-13 04:31:48.121578 ardilla-0.0.6a0/PKG-INFO
+-rw-rw-rw-   0        0        0     3297 2023-05-12 03:38:21.000000 ardilla-0.0.6a0/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.055435 ardilla-0.0.6a0/ardilla/
+-rw-rw-rw-   0        0        0      106 2023-05-08 02:18:14.000000 ardilla-0.0.6a0/ardilla/__init__.py
+-rw-rw-rw-   0        0        0     3240 2023-05-13 04:14:16.000000 ardilla-0.0.6a0/ardilla/abc.py
+drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.105001 ardilla-0.0.6a0/ardilla/asyncio/
+-rw-rw-rw-   0        0        0       78 2023-05-08 16:29:21.000000 ardilla-0.0.6a0/ardilla/asyncio/__init__.py
+-rw-rw-rw-   0        0        0      468 2023-05-13 04:14:11.000000 ardilla-0.0.6a0/ardilla/asyncio/abc.py
+-rw-rw-rw-   0        0        0     6194 2023-05-12 13:48:41.000000 ardilla-0.0.6a0/ardilla/asyncio/crud.py
+-rw-rw-rw-   0        0        0      974 2023-05-13 04:12:28.000000 ardilla-0.0.6a0/ardilla/asyncio/engine.py
+-rw-rw-rw-   0        0        0     6753 2023-05-13 04:30:42.000000 ardilla-0.0.6a0/ardilla/crud.py
+-rw-rw-rw-   0        0        0     1250 2023-05-13 04:12:04.000000 ardilla-0.0.6a0/ardilla/engine.py
+-rw-rw-rw-   0        0        0      216 2023-05-11 02:46:57.000000 ardilla-0.0.6a0/ardilla/errors.py
+-rw-rw-rw-   0        0        0     1475 2023-05-12 03:30:34.000000 ardilla-0.0.6a0/ardilla/models.py
+-rw-rw-rw-   0        0        0     2151 2023-05-13 04:07:51.000000 ardilla-0.0.6a0/ardilla/schemas.py
+drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.085724 ardilla-0.0.6a0/ardilla.egg-info/
+-rw-rw-rw-   0        0        0     3988 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      471 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      144 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      916 2023-05-13 04:25:38.000000 ardilla-0.0.6a0/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 04:31:48.123576 ardilla-0.0.6a0/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.116559 ardilla-0.0.6a0/tests/
+-rw-rw-rw-   0        0        0     5291 2023-05-12 03:30:55.000000 ardilla-0.0.6a0/tests/test_async.py
+-rw-rw-rw-   0        0        0      567 2023-05-12 03:32:46.000000 ardilla-0.0.6a0/tests/test_models.py
+-rw-rw-rw-   0        0        0     4964 2023-05-12 03:31:02.000000 ardilla-0.0.6a0/tests/test_sync.py
```

### Comparing `ardilla-0.0.5a0/LICENCE` & `ardilla-0.0.6a0/LICENCE`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.5a0/PKG-INFO` & `ardilla-0.0.6a0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ardilla
-Version: 0.0.5a0
+Version: 0.0.6a0
 Summary: A small package for performing basic CRUD operations with sqlite via aiosqlite and pydantic
 Author-email: ChrisDewa <chrisdewa@duck.com>
 Project-URL: Homepage, https://github.com/chrisdewa/ardilla
 Project-URL: Bug Tracker, https://github.com/chrisdewa/ardilla/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `ardilla-0.0.5a0/README.md` & `ardilla-0.0.6a0/README.md`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.5a0/ardilla/abc.py` & `ardilla-0.0.6a0/ardilla/abc.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,23 +7,25 @@
 from .models import M, Model as BaseModel
 
 E = TypeVar("E")  # Engine Type
 
 
 class AbstractEngine(ABC):
     """This just provides autocompletition across the library"""
+    schemas: set[str]
     @abstractmethod
     def __enter__(self) -> sqlite3.Connection:
         ...
     abstractmethod
     def cursor(self, con: sqlite3.Connection) -> sqlite3.Cursor:
         ...
 
 
 class CrudABC(ABC):
+    engine: AbstractEngine
     def __init__(self, Model: type[M], engine: E | None = None) -> None:
         if engine:
             self.engine = engine
 
         self.Model = Model
         if Model.__schema__:
             self.engine.schemas.add(Model.__schema__)
```

### Comparing `ardilla-0.0.5a0/ardilla/asyncio/crud.py` & `ardilla-0.0.6a0/ardilla/asyncio/crud.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.5a0/ardilla/asyncio/engine.py` & `ardilla-0.0.6a0/ardilla/asyncio/engine.py`

 * *Files 17% similar despite different names*

```diff
@@ -25,8 +25,9 @@
         async with self as con:
             await con.execute("PRAGMA foreign_keys = ON;")
             for table in self.schemas:
                 await con.execute(table)
             await con.commit()
 
     def crud(self, Model: type[M]) -> AsyncCrud[M]:
-        return AsyncCrud(Model, self)
+        crud = self._cruds.setdefault(Model, AsyncCrud(Model, self))
+        return crud
```

### Comparing `ardilla-0.0.5a0/ardilla/crud.py` & `ardilla-0.0.6a0/ardilla/crud.py`

 * *Files 3% similar despite different names*

```diff
@@ -131,23 +131,33 @@
             con.commit()
 
         return True
 
     def delete_one(self, obj: M) -> Literal[True]:
         """
         Deletes the object from the database (won't delete the actual object)
-        queries only by the Model id fields (fields suffixed with 'id')
-        """
-        obj_dict = obj.dict()
-        id_cols = tuple([k for k in obj_dict if "id" in k])
-        placeholders = ", ".join(f"{k} = ?" for k in id_cols)
-        vals = tuple([obj_dict[k] for k in id_cols])
-        q = f"""
-        DELETE FROM {self.tablename} WHERE ({placeholders});
+        If the object has a PK field or the rowid setup, those will be 
+        used to locate the obj and delete it. 
+        If not, this function will delete any object like this one.
         """
+        
+        if obj.__pk__:
+            q = f'DELETE FROM {self.tablename} WHERE {obj.__pk__} = ?'
+            vals = getattr(obj, obj.__pk__),
+        elif obj.__rowid__:
+            q = f'DELETE FROM {self.tablename} WHERE rowid = ?'
+            vals = obj.__rowid__,
+        else:
+            obj_dict = obj.dict()
+            id_cols = tuple([k for k in obj_dict if "id" in k])
+            placeholders = ", ".join(f"{k} = ?" for k in id_cols)
+            vals = tuple([obj_dict[k] for k in id_cols])
+            q = f"""
+            DELETE FROM {self.tablename} WHERE ({placeholders});
+            """
         with self.engine as con:
             con.execute(q, vals)
             con.commit()
 
         return True
 
     def delete_many(self, *objs: M) -> Literal[True]:
```

### Comparing `ardilla-0.0.5a0/ardilla/engine.py` & `ardilla-0.0.6a0/ardilla/engine.py`

 * *Files 6% similar despite different names*

```diff
@@ -17,14 +17,15 @@
         self.cur.close()
 
 
 class Engine(AbstractEngine):
     def __init__(self, path: str):
         self.path = path
         self.schemas: set[str] = set()
+        self._cruds = {}
 
     def __enter__(self) -> sqlite3.Connection:
         con = sqlite3.connect(self.path)
         con.row_factory = sqlite3.Row
         self.con = con
         return con
 
@@ -38,8 +39,9 @@
         with self as con:
             con.execute("PRAGMA foreign_keys = ON;")
             for table in self.schemas:
                 con.execute(table)
             con.commit()
     
     def crud(self, Model: type[M]) -> Crud[M]:
-        return Crud(Model, self)
+        crud = self._cruds.setdefault(Model, Crud(Model, self))
+        return crud
```

### Comparing `ardilla-0.0.5a0/ardilla/models.py` & `ardilla-0.0.6a0/ardilla/models.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.5a0/ardilla/schemas.py` & `ardilla-0.0.6a0/ardilla/schemas.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,24 +1,25 @@
 import re
 from datetime import datetime, date
-from pydantic import BaseModel
+from pydantic import BaseModel, Json
 from .errors import ModelIntegrityError
 
 
 SCHEMA_TEMPLATE = "CREATE TABLE IF NOT EXISTS {tablename} (\n{fields}\n);"
 
 
 FIELD_MAPPING = {
     int: "INTEGER",
     float: "REAL",
     str: "TEXT",
     bytes: "BLOB",
     bool: "INTEGER",
     date: "DATE",
     datetime: "TIMESTAMP",
+    Json: "TEXT",
 }
 
 
 def get_tablename(model: type[BaseModel]) -> str:
     return getattr(model, "__tablename__", model.__name__.lower())
```

### Comparing `ardilla-0.0.5a0/ardilla.egg-info/PKG-INFO` & `ardilla-0.0.6a0/ardilla.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ardilla
-Version: 0.0.5a0
+Version: 0.0.6a0
 Summary: A small package for performing basic CRUD operations with sqlite via aiosqlite and pydantic
 Author-email: ChrisDewa <chrisdewa@duck.com>
 Project-URL: Homepage, https://github.com/chrisdewa/ardilla
 Project-URL: Bug Tracker, https://github.com/chrisdewa/ardilla/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `ardilla-0.0.5a0/pyproject.toml` & `ardilla-0.0.6a0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "ardilla"
-version = "0.0.5-alpha"
+version = "0.0.6-alpha"
 authors = [
   { name="ChrisDewa", email="chrisdewa@duck.com" },
 ]
 description = "A small package for performing basic CRUD operations with sqlite via aiosqlite and pydantic"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
```

### Comparing `ardilla-0.0.5a0/tests/test_async.py` & `ardilla-0.0.6a0/tests/test_async.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.5a0/tests/test_models.py` & `ardilla-0.0.6a0/tests/test_models.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.5a0/tests/test_sync.py` & `ardilla-0.0.6a0/tests/test_sync.py`

 * *Files identical despite different names*

