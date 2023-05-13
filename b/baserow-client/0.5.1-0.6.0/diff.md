# Comparing `tmp/baserow-client-0.5.1.tar.gz` & `tmp/baserow_client-0.6.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "baserow-client-0.5.1.tar", max compression
+gzip compressed data, was "baserow_client-0.6.0.tar", max compression
```

## Comparing `baserow-client-0.5.1.tar` & `baserow_client-0.6.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
--rw-r--r--   0        0        0     1001 2022-03-23 21:48:21.758805 baserow-client-0.5.1/LICENSE
--rw-r--r--   0        0        0     1358 2022-03-23 23:35:01.408813 baserow-client-0.5.1/pyproject.toml
--rw-r--r--   0        0        0      254 2022-03-23 21:53:15.808805 baserow-client-0.5.1/readme.md
--rw-r--r--   0        0        0       85 2022-03-23 23:35:01.408813 baserow-client-0.5.1/src/baserow/__init__.py
--rw-r--r--   0        0        0    10420 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/client.py
--rw-r--r--   0        0        0     1292 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/field_types.py
--rw-r--r--   0        0        0     3977 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/filter.py
--rw-r--r--   0        0        0      357 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/orm/__init__.py
--rw-r--r--   0        0        0     2044 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/orm/__main__.py
--rw-r--r--   0        0        0     5449 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/orm/column.py
--rw-r--r--   0        0        0     6065 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/orm/database.py
--rw-r--r--   0        0        0      227 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/orm/exc.py
--rw-r--r--   0        0        0     3551 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/orm/mapping.py
--rw-r--r--   0        0        0     2301 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/orm/model.py
--rw-r--r--   0        0        0        0 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/py.typed
--rw-r--r--   0        0        0     1078 2022-03-23 21:48:21.758805 baserow-client-0.5.1/src/baserow/types.py
--rw-r--r--   0        0        0     1071 1970-01-01 00:00:00.000000 baserow-client-0.5.1/setup.py
--rw-r--r--   0        0        0     1031 1970-01-01 00:00:00.000000 baserow-client-0.5.1/PKG-INFO
+-rw-r--r--   0        0        0     1001 2023-05-13 10:06:26.838322 baserow_client-0.6.0/LICENSE
+-rw-r--r--   0        0        0     1476 2023-05-13 17:22:44.275165 baserow_client-0.6.0/pyproject.toml
+-rw-r--r--   0        0        0      254 2023-05-13 10:06:26.838322 baserow_client-0.6.0/readme.md
+-rw-r--r--   0        0        0       85 2023-05-13 17:22:44.275165 baserow_client-0.6.0/src/baserow/__init__.py
+-rw-r--r--   0        0        0    10424 2023-05-13 17:05:32.520472 baserow_client-0.6.0/src/baserow/client.py
+-rw-r--r--   0        0        0     1297 2023-05-13 17:22:33.719465 baserow_client-0.6.0/src/baserow/field_types.py
+-rw-r--r--   0        0        0     1022 2023-05-13 17:22:33.719465 baserow_client-0.6.0/src/baserow/field_types_test.py
+-rw-r--r--   0        0        0     3977 2023-05-13 10:06:26.838322 baserow_client-0.6.0/src/baserow/filter.py
+-rw-r--r--   0        0        0      357 2023-05-13 10:06:26.838322 baserow_client-0.6.0/src/baserow/orm/__init__.py
+-rw-r--r--   0        0        0     2052 2023-05-13 17:05:32.520472 baserow_client-0.6.0/src/baserow/orm/__main__.py
+-rw-r--r--   0        0        0     5449 2023-05-13 10:06:26.842322 baserow_client-0.6.0/src/baserow/orm/column.py
+-rw-r--r--   0        0        0     6065 2023-05-13 10:06:26.842322 baserow_client-0.6.0/src/baserow/orm/database.py
+-rw-r--r--   0        0        0      227 2023-05-13 10:06:26.842322 baserow_client-0.6.0/src/baserow/orm/exc.py
+-rw-r--r--   0        0        0     3551 2023-05-13 10:06:26.842322 baserow_client-0.6.0/src/baserow/orm/mapping.py
+-rw-r--r--   0        0        0     2301 2023-05-13 10:06:26.842322 baserow_client-0.6.0/src/baserow/orm/model.py
+-rw-r--r--   0        0        0        0 2023-05-13 10:06:26.842322 baserow_client-0.6.0/src/baserow/py.typed
+-rw-r--r--   0        0        0     1153 2023-05-13 17:22:33.719465 baserow_client-0.6.0/src/baserow/types.py
+-rw-r--r--   0        0        0     1061 1970-01-01 00:00:00.000000 baserow_client-0.6.0/PKG-INFO
```

### Comparing `baserow-client-0.5.1/LICENSE` & `baserow_client-0.6.0/LICENSE`

 * *Files identical despite different names*

### Comparing `baserow-client-0.5.1/pyproject.toml` & `baserow_client-0.6.0/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "baserow-client"
-version = "0.5.1"
+version = "0.6.0"
 description = "Client for the baserow.io API."
 authors = ["Niklas Rosenstein <rosensteinniklas@gmail.com>"]
 license = "MIT"
 readme = "readme.md"
 packages = [{ include = "baserow", from = "src" }]
 classifiers = []
 keywords = []
@@ -18,33 +18,41 @@
 # Documentation = ""
 Homepage = "https://github.com/NiklasRosenstein/python-baserow-client"
 # Repository = ""
 
 [tool.poetry.dependencies]
 python = "^3.8"
 requests = "^2.26.0"
-"databind.core" = "^1.2.1"
-"databind.json" = "^1.2.1"
+"databind.core" = "^4.2.5"
+"databind.json" = "^4.2.5"
 typing-extensions = ">=3.0.0"
 
 [tool.poetry.dev-dependencies]
 mypy = "*"
 pytest = "*"
+pycln = "^2.1.3"
 types-requests = "^2.25.6"
 
-[tool.poetry.extras]
-docs = ["novella==0.1.14", "pydoc-markdown==0.4.6", "mkdocs", "mkdocs-material"]
+[tool.poetry.group.docs]
+optional = true
+
+[tool.poetry.group.docs.dependencies]
+novella = "^0.1.14"
+pydoc-markdown = "^4.6.0"
+mkdocs = "*"
+mkdocs-material = "*"
 
 [tool.slap]
 typed = true
 
 [tool.slap.test]
 check = "slap check"
 mypy = "MYPYPATH=src mypy src/ --namespace-packages --explicit-package-bases"
-pytest = "pytest test/ -vv"
+pytest = "pytest src/ test/ -vv"
+pycln  = "pycln src/ tests/ --check"
 
 [tool.slap.run]
 "docs:build" = "cd docs && novella --base-url python-baserow-client/"
 "docs:dev" = "cd docs && novella --serve"
 
 [tool.mypy]
 pretty = true
```

### Comparing `baserow-client-0.5.1/src/baserow/client.py` & `baserow_client-0.6.0/src/baserow/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -128,27 +128,27 @@
     return databind.json.load(response, PermissionedOrderedGroup)
 
   def list_all_applications(self) -> t.List[Application]:
     response = self._request('GET', '/api/applications/').json()
     return databind.json.load(response, t.List[Application])
 
   def get_database_table(self, table_id: int) -> Table:
-    response = self._request('GET', f'/api/database/tables/{table_id}').json()
+    response = self._request('GET', f'/api/database/tables/{table_id}/').json()
     return databind.json.load(response, Table)
 
   def update_database_table(self, table_id: int, name: str) -> Table:
-    response = self._request('PATCH', f'/api/database/tables/{table_id}', json={'name': name}).json()
+    response = self._request('PATCH', f'/api/database/tables/{table_id}/', json={'name': name}).json()
     return databind.json.load(response, Table)
 
   def list_database_tables(self, database_id: int) -> t.List[Table]:
-    response = self._request('GET', f'/api/database/tables/database/{database_id}').json()
+    response = self._request('GET', f'/api/database/tables/database/{database_id}/').json()
     return databind.json.load(response, t.List[Table])
 
   def list_database_table_fields(self, table_id: int) -> t.List[TableField]:
-    response = self._request('GET', f'/api/database/fields/table/{table_id}').json()
+    response = self._request('GET', f'/api/database/fields/table/{table_id}/').json()
     return databind.json.load(response, t.List[TableField])
 
   def list_database_table_rows(
     self,
     table_id: int,
     exclude: t.Optional[t.List[str]] = None,
     filter: t.Optional[t.List[Filter]] = None,
```

### Comparing `baserow-client-0.5.1/src/baserow/field_types.py` & `baserow_client-0.6.0/src/baserow/field_types.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 
 import dataclasses
 import enum
 import typing as t
 
-from databind.core.annotations import union
+from databind.core.settings import Union
 
 from .types import TableField
 
 
 class NumberType(enum.Enum):
   INTEGER = enum.auto()
   DECIMAL = enum.auto()
@@ -16,53 +16,53 @@
 @dataclasses.dataclass
 class SelectOption:
   id: int
   value: str
   color: str
 
 
-@union.subtype(TableField, 'text')
+@Union.register(TableField, 'text')
 @dataclasses.dataclass
 class TextTableField(TableField):
   text_default: str
 
 
-@union.subtype(TableField, 'long_text')
+@Union.register(TableField, 'long_text')
 @dataclasses.dataclass
 class LongTextTableField(TableField): pass
 
 
-@union.subtype(TableField, 'number')
+@Union.register(TableField, 'number')
 @dataclasses.dataclass
 class NumberTableField(TableField):
   number_decimal_places: int
   number_negative: bool
   number_type: NumberType
 
 
-@union.subtype(TableField, 'single_select')
+@Union.register(TableField, 'single_select')
 @dataclasses.dataclass
 class SingleSelectTableField(TableField):
   select_options: t.List[SelectOption]
 
 
-@union.subtype(TableField, 'url')
+@Union.register(TableField, 'url')
 @dataclasses.dataclass
 class UrlTableField(TableField):
   pass
 
 
-@union.subtype(TableField, 'link_row')
+@Union.register(TableField, 'link_row')
 @dataclasses.dataclass
 class LinkRowTableField(TableField):
   link_row_table: int
   link_row_related_field: int
 
 
-@union.subtype(TableField, 'boolean')
+@Union.register(TableField, 'boolean')
 @dataclasses.dataclass
 class BooleanTableField(TableField): pass
 
 
-@union.subtype(TableField, 'file')
+@Union.register(TableField, 'file')
 @dataclasses.dataclass
 class FileTableField(TableField): pass
```

### Comparing `baserow-client-0.5.1/src/baserow/filter.py` & `baserow_client-0.6.0/src/baserow/filter.py`

 * *Files identical despite different names*

### Comparing `baserow-client-0.5.1/src/baserow/orm/__main__.py` & `baserow_client-0.6.0/src/baserow/orm/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 parser.add_argument('--url', required=True, help='The URL to your Baserow instance.')
 parser.add_argument('--user', help='The username to authenticate with.')
 parser.add_argument('--password', help='The password for the given --user. If omitted, the password will be asked.')
 parser.add_argument('--jwt', help='A JWT to use instead of generating a new one with --user and --password.')
 parser.add_argument('--write-to', help='The path to write the generated mappings to. If not specified, will be stdout.')
 
 
-def main():
+def main() -> None:
   args = parser.parse_args()
   client = BaserowClient(args.url)
 
   if args.user:
     if not args.password:
       args.password = getpass.getpass(f'Password for {args.user}: ')
     client.login(args.user, args.password)
```

### Comparing `baserow-client-0.5.1/src/baserow/orm/column.py` & `baserow_client-0.6.0/src/baserow/orm/column.py`

 * *Files identical despite different names*

### Comparing `baserow-client-0.5.1/src/baserow/orm/database.py` & `baserow_client-0.6.0/src/baserow/orm/database.py`

 * *Files identical despite different names*

### Comparing `baserow-client-0.5.1/src/baserow/orm/mapping.py` & `baserow_client-0.6.0/src/baserow/orm/mapping.py`

 * *Files identical despite different names*

### Comparing `baserow-client-0.5.1/src/baserow/orm/model.py` & `baserow_client-0.6.0/src/baserow/orm/model.py`

 * *Files identical despite different names*

### Comparing `baserow-client-0.5.1/src/baserow/types.py` & `baserow_client-0.6.0/src/baserow/types.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 
 import dataclasses
 import enum
 import typing as t
 
-from databind.core.annotations import union
+from databind.core.settings import Union
 
 T = t.TypeVar('T')
 
 
 class Permissions(enum.Enum):
   MEMBER = enum.auto()
   ADMIN = enum.auto()
@@ -23,14 +23,18 @@
 
 
 @dataclasses.dataclass
 class Group:
   id: int
   name: str
 
+@dataclasses.dataclass
+class Workspace:
+  id: int
+  name: str
 
 @dataclasses.dataclass
 class OrderedGroup(Group):
   order: int
 
 
 @dataclasses.dataclass
@@ -42,15 +46,15 @@
 class Table:
   id: int
   name: str
   order: int
   database_id: int
 
 
-@union(style=union.Style.flat, constructible=True)
+@Union(style=Union.FLAT)
 @dataclasses.dataclass
 class TableField:
   id: int
   table_id: int
   name: str
   order: int
   primary: bool
@@ -58,16 +62,17 @@
 
 @dataclasses.dataclass
 class Application:
   id: int
   name: str
   order: int
   type: str
-  group: Group
+  workspace: Workspace
   tables: t.List[Table]
+  group: t.Optional[Group] = None
 
 
 @dataclasses.dataclass
 class Page(t.Generic[T]):
   count: int
   previous: t.Optional[int]
   next: t.Optional[int]
```

