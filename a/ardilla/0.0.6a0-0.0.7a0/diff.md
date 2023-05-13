# Comparing `tmp/ardilla-0.0.6a0.tar.gz` & `tmp/ardilla-0.0.7a0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ardilla-0.0.6a0.tar", last modified: Sat May 13 04:31:48 2023, max compression
+gzip compressed data, was "ardilla-0.0.7a0.tar", last modified: Sat May 13 17:33:54 2023, max compression
```

## Comparing `ardilla-0.0.6a0.tar` & `ardilla-0.0.7a0.tar`

### file list

```diff
@@ -1,29 +1,30 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.122576 ardilla-0.0.6a0/
--rw-rw-rw-   0        0        0     1084 2023-05-08 03:28:44.000000 ardilla-0.0.6a0/LICENCE
--rw-rw-rw-   0        0        0     3988 2023-05-13 04:31:48.121578 ardilla-0.0.6a0/PKG-INFO
--rw-rw-rw-   0        0        0     3297 2023-05-12 03:38:21.000000 ardilla-0.0.6a0/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.055435 ardilla-0.0.6a0/ardilla/
--rw-rw-rw-   0        0        0      106 2023-05-08 02:18:14.000000 ardilla-0.0.6a0/ardilla/__init__.py
--rw-rw-rw-   0        0        0     3240 2023-05-13 04:14:16.000000 ardilla-0.0.6a0/ardilla/abc.py
-drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.105001 ardilla-0.0.6a0/ardilla/asyncio/
--rw-rw-rw-   0        0        0       78 2023-05-08 16:29:21.000000 ardilla-0.0.6a0/ardilla/asyncio/__init__.py
--rw-rw-rw-   0        0        0      468 2023-05-13 04:14:11.000000 ardilla-0.0.6a0/ardilla/asyncio/abc.py
--rw-rw-rw-   0        0        0     6194 2023-05-12 13:48:41.000000 ardilla-0.0.6a0/ardilla/asyncio/crud.py
--rw-rw-rw-   0        0        0      974 2023-05-13 04:12:28.000000 ardilla-0.0.6a0/ardilla/asyncio/engine.py
--rw-rw-rw-   0        0        0     6753 2023-05-13 04:30:42.000000 ardilla-0.0.6a0/ardilla/crud.py
--rw-rw-rw-   0        0        0     1250 2023-05-13 04:12:04.000000 ardilla-0.0.6a0/ardilla/engine.py
--rw-rw-rw-   0        0        0      216 2023-05-11 02:46:57.000000 ardilla-0.0.6a0/ardilla/errors.py
--rw-rw-rw-   0        0        0     1475 2023-05-12 03:30:34.000000 ardilla-0.0.6a0/ardilla/models.py
--rw-rw-rw-   0        0        0     2151 2023-05-13 04:07:51.000000 ardilla-0.0.6a0/ardilla/schemas.py
-drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.085724 ardilla-0.0.6a0/ardilla.egg-info/
--rw-rw-rw-   0        0        0     3988 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      471 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      144 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-13 04:31:47.000000 ardilla-0.0.6a0/ardilla.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      916 2023-05-13 04:25:38.000000 ardilla-0.0.6a0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-13 04:31:48.123576 ardilla-0.0.6a0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-05-13 04:31:48.116559 ardilla-0.0.6a0/tests/
--rw-rw-rw-   0        0        0     5291 2023-05-12 03:30:55.000000 ardilla-0.0.6a0/tests/test_async.py
--rw-rw-rw-   0        0        0      567 2023-05-12 03:32:46.000000 ardilla-0.0.6a0/tests/test_models.py
--rw-rw-rw-   0        0        0     4964 2023-05-12 03:31:02.000000 ardilla-0.0.6a0/tests/test_sync.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:33:54.541981 ardilla-0.0.7a0/
+-rw-rw-rw-   0        0        0     1084 2023-05-08 03:28:44.000000 ardilla-0.0.7a0/LICENCE
+-rw-rw-rw-   0        0        0     3988 2023-05-13 17:33:54.536979 ardilla-0.0.7a0/PKG-INFO
+-rw-rw-rw-   0        0        0     3297 2023-05-12 03:38:21.000000 ardilla-0.0.7a0/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 17:33:54.458981 ardilla-0.0.7a0/ardilla/
+-rw-rw-rw-   0        0        0      136 2023-05-13 16:32:48.000000 ardilla-0.0.7a0/ardilla/__init__.py
+-rw-rw-rw-   0        0        0     3240 2023-05-13 04:14:16.000000 ardilla-0.0.7a0/ardilla/abc.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:33:54.515978 ardilla-0.0.7a0/ardilla/asyncio/
+-rw-rw-rw-   0        0        0       78 2023-05-08 16:29:21.000000 ardilla-0.0.7a0/ardilla/asyncio/__init__.py
+-rw-rw-rw-   0        0        0      468 2023-05-13 04:14:11.000000 ardilla-0.0.7a0/ardilla/asyncio/abc.py
+-rw-rw-rw-   0        0        0     6364 2023-05-13 16:27:36.000000 ardilla-0.0.7a0/ardilla/asyncio/crud.py
+-rw-rw-rw-   0        0        0     1292 2023-05-13 16:09:59.000000 ardilla-0.0.7a0/ardilla/asyncio/engine.py
+-rw-rw-rw-   0        0        0     6753 2023-05-13 04:30:42.000000 ardilla-0.0.7a0/ardilla/crud.py
+-rw-rw-rw-   0        0        0     1661 2023-05-13 16:03:58.000000 ardilla-0.0.7a0/ardilla/engine.py
+-rw-rw-rw-   0        0        0      216 2023-05-11 02:46:57.000000 ardilla-0.0.7a0/ardilla/errors.py
+-rw-rw-rw-   0        0        0      217 2023-05-13 16:26:28.000000 ardilla-0.0.7a0/ardilla/logging.py
+-rw-rw-rw-   0        0        0     1475 2023-05-12 03:30:34.000000 ardilla-0.0.7a0/ardilla/models.py
+-rw-rw-rw-   0        0        0     2151 2023-05-13 04:07:51.000000 ardilla-0.0.7a0/ardilla/schemas.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:33:54.499980 ardilla-0.0.7a0/ardilla.egg-info/
+-rw-rw-rw-   0        0        0     3988 2023-05-13 17:33:54.000000 ardilla-0.0.7a0/ardilla.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      490 2023-05-13 17:33:54.000000 ardilla-0.0.7a0/ardilla.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 17:33:54.000000 ardilla-0.0.7a0/ardilla.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      144 2023-05-13 17:33:54.000000 ardilla-0.0.7a0/ardilla.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-13 17:33:54.000000 ardilla-0.0.7a0/ardilla.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      916 2023-05-13 17:32:31.000000 ardilla-0.0.7a0/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 17:33:54.542976 ardilla-0.0.7a0/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 17:33:54.531976 ardilla-0.0.7a0/tests/
+-rw-rw-rw-   0        0        0     5291 2023-05-12 03:30:55.000000 ardilla-0.0.7a0/tests/test_async.py
+-rw-rw-rw-   0        0        0      567 2023-05-12 03:32:46.000000 ardilla-0.0.7a0/tests/test_models.py
+-rw-rw-rw-   0        0        0     4964 2023-05-12 03:31:02.000000 ardilla-0.0.7a0/tests/test_sync.py
```

### Comparing `ardilla-0.0.6a0/LICENCE` & `ardilla-0.0.7a0/LICENCE`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.6a0/PKG-INFO` & `ardilla-0.0.7a0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ardilla
-Version: 0.0.6a0
+Version: 0.0.7a0
 Summary: A small package for performing basic CRUD operations with sqlite via aiosqlite and pydantic
 Author-email: ChrisDewa <chrisdewa@duck.com>
 Project-URL: Homepage, https://github.com/chrisdewa/ardilla
 Project-URL: Bug Tracker, https://github.com/chrisdewa/ardilla/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `ardilla-0.0.6a0/README.md` & `ardilla-0.0.7a0/README.md`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.6a0/ardilla/abc.py` & `ardilla-0.0.7a0/ardilla/abc.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.6a0/ardilla/asyncio/crud.py` & `ardilla-0.0.7a0/ardilla/asyncio/crud.py`

 * *Files 13% similar despite different names*

```diff
@@ -2,18 +2,18 @@
 
 import aiosqlite
 from aiosqlite import Row
 
 from ..errors import QueryExecutionError
 from ..models import M
 from ..abc import CrudABC
+from ..logging import log, log_query
 
 from .abc import AbstractAsyncEngine
 
-
 class AsyncCrud(CrudABC, Generic[M]):
     """Abstracts CRUD actions for model associated tables"""
 
     engine: AbstractAsyncEngine
 
     async def _get_or_none_any(self, many: bool, **kws) -> list[M] | M | None:
         """
@@ -21,15 +21,15 @@
         if param "many" is true it will return a list of matches else will return only one record
         """
         keys, vals = zip(*kws.items())
         to_match = f" AND ".join(f"{k} = ?" for k in keys)
 
         limit = "LIMIT 1;" if not many else ";"
         q = f"SELECT rowid, * FROM {self.tablename} WHERE ({to_match}) {limit}"
-
+        log_query(q, vals)
         async with self.engine as con:
             async with con.execute(q, vals) as cur:
                 if many:
                     rows: list[Row] = await cur.fetchall()
                     return [self._row2obj(row) for row in rows]
 
                 else:
@@ -46,15 +46,15 @@
         keys, vals = zip(*kws.items())
         placeholders = ", ".join("?" * len(keys))
         cols = ", ".join(keys)
 
         q = "INSERT OR IGNORE " if ignore else "INSERT "
         q += f"INTO {self.tablename} ({cols}) VALUES ({placeholders})"
         q += " RETURNING *;" if returning else ";"
-
+        log_query(q, vals)
         async with self.engine as con:
             con = await self.engine.connect()
             cur = None
             try:
                 cur = await con.execute(q, vals)
             except aiosqlite.IntegrityError as e:
                 raise QueryExecutionError(str(e))
@@ -102,28 +102,29 @@
         return await self._get_or_none_any(many=True, **kws)
 
     async def save_one(self, obj: M) -> Literal[True]:
         """Saves one object to the database"""
         cols, vals = zip(*obj.dict().items())
         placeholders = ", ".join("?" * len(cols))
 
-        upsert_query = f"""
+        q = f"""
         INSERT OR REPLACE INTO {self.tablename} ({', '.join(cols)}) VALUES ({placeholders});
         """
-
+        log_query(q, vals)
         async with self.engine as con:
-            await con.execute(upsert_query, vals)
+            await con.execute(q, vals)
             await con.commit()
         return True
 
     async def save_many(self, *objs: M) -> Literal[True]:
         """Saves all the given objects to the database"""
         placeholders = ", ".join("?" * len(self.columns))
         q = f'INSERT OR REPLACE INTO {self.tablename} ({", ".join(self.columns)}) VALUES ({placeholders});'
         vals = [tuple(obj.dict().values()) for obj in objs]
+        log_query(q, vals)
         async with self.engine as con:
             await con.executemany(q, vals)
             await con.commit()
 
         return True
 
     async def delete_one(self, obj: M) -> Literal[True]:
@@ -132,14 +133,15 @@
         queries only by the Model id fields (fields suffixed with 'id')
         """
         obj_dict = obj.dict()
         id_cols = tuple([k for k in obj_dict if "id" in k])
         placeholders = ", ".join(f"{k} = ?" for k in id_cols)
         vals = tuple([obj_dict[k] for k in id_cols])
         q = f"DELETE FROM {self.tablename} WHERE ({placeholders});"
+        log_query(q, vals)
         async with self.engine as con:
             await con.execute(q, vals)
             await con.commit()
         return True
 
     async def delete_many(self, *objs: M) -> Literal[True]:
         if not objs:
@@ -151,12 +153,13 @@
             f"({', '.join(f'{k} = ?' for k in id_cols)})" for _ in objs
         )
         vals = tuple(
             [val for obj in objs for key, val in obj.dict().items() if key in id_cols]
         )
 
         q = f"DELETE FROM {self.tablename} WHERE {placeholders};"
+        log_query(q, vals)
         async with self.engine as con:
             await con.execute(q, vals)
             await con.commit()
 
-        return True
+        return
```

### Comparing `ardilla-0.0.6a0/ardilla/crud.py` & `ardilla-0.0.7a0/ardilla/crud.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.6a0/ardilla/models.py` & `ardilla-0.0.7a0/ardilla/models.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.6a0/ardilla/schemas.py` & `ardilla-0.0.7a0/ardilla/schemas.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.6a0/ardilla.egg-info/PKG-INFO` & `ardilla-0.0.7a0/ardilla.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ardilla
-Version: 0.0.6a0
+Version: 0.0.7a0
 Summary: A small package for performing basic CRUD operations with sqlite via aiosqlite and pydantic
 Author-email: ChrisDewa <chrisdewa@duck.com>
 Project-URL: Homepage, https://github.com/chrisdewa/ardilla
 Project-URL: Bug Tracker, https://github.com/chrisdewa/ardilla/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `ardilla-0.0.6a0/pyproject.toml` & `ardilla-0.0.7a0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "ardilla"
-version = "0.0.6-alpha"
+version = "0.0.7-alpha"
 authors = [
   { name="ChrisDewa", email="chrisdewa@duck.com" },
 ]
 description = "A small package for performing basic CRUD operations with sqlite via aiosqlite and pydantic"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
```

### Comparing `ardilla-0.0.6a0/tests/test_async.py` & `ardilla-0.0.7a0/tests/test_async.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.6a0/tests/test_models.py` & `ardilla-0.0.7a0/tests/test_models.py`

 * *Files identical despite different names*

### Comparing `ardilla-0.0.6a0/tests/test_sync.py` & `ardilla-0.0.7a0/tests/test_sync.py`

 * *Files identical despite different names*

