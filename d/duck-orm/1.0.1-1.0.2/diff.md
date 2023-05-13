# Comparing `tmp/duck-orm-1.0.1.tar.gz` & `tmp/duck_orm-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "duck-orm-1.0.1.tar", last modified: Sun Nov  7 22:56:57 2021, max compression
+gzip compressed data, was "duck_orm-1.0.2.tar", max compression
```

## Comparing `duck-orm-1.0.1.tar` & `duck_orm-1.0.2.tar`

### file list

```diff
@@ -1,32 +1,18 @@
-drwxrwxrwx   0        0        0        0 2021-11-07 22:56:57.344633 duck-orm-1.0.1/
--rw-rw-rw-   0        0        0     1103 2021-10-31 20:36:58.000000 duck-orm-1.0.1/LICENSE
--rw-rw-rw-   0        0        0     2848 2021-11-07 22:56:57.344633 duck-orm-1.0.1/PKG-INFO
--rw-rw-rw-   0        0        0     1759 2021-10-31 20:36:58.000000 duck-orm-1.0.1/README.md
-drwxrwxrwx   0        0        0        0 2021-11-07 22:56:57.302636 duck-orm-1.0.1/duck_orm/
--rw-rw-rw-   0        0        0       23 2021-11-07 22:53:13.000000 duck-orm-1.0.1/duck_orm/__init__.py
--rw-rw-rw-   0        0        0      441 2021-10-31 20:36:58.000000 duck-orm-1.0.1/duck_orm/exceptions.py
--rw-rw-rw-   0        0        0    13910 2021-11-07 22:53:13.000000 duck-orm-1.0.1/duck_orm/model.py
--rw-rw-rw-   0        0        0     1317 2021-11-07 22:53:13.000000 duck-orm-1.0.1/duck_orm/model_manager.py
-drwxrwxrwx   0        0        0        0 2021-11-07 22:56:57.332635 duck-orm-1.0.1/duck_orm/sql/
--rw-rw-rw-   0        0        0        0 2021-10-31 20:36:58.000000 duck-orm-1.0.1/duck_orm/sql/__init__.py
--rw-rw-rw-   0        0        0     1340 2021-10-31 20:36:58.000000 duck-orm-1.0.1/duck_orm/sql/condition.py
--rw-rw-rw-   0        0        0     4580 2021-10-31 20:36:58.000000 duck-orm-1.0.1/duck_orm/sql/fields.py
--rw-rw-rw-   0        0        0      723 2021-10-31 20:36:58.000000 duck-orm-1.0.1/duck_orm/sql/operator.py
-drwxrwxrwx   0        0        0        0 2021-11-07 22:56:57.335633 duck-orm-1.0.1/duck_orm/sql/postgres/
--rw-rw-rw-   0        0        0      603 2021-10-31 20:36:58.000000 duck-orm-1.0.1/duck_orm/sql/postgres/__init__.py
--rw-rw-rw-   0        0        0     7866 2021-11-07 22:53:13.000000 duck-orm-1.0.1/duck_orm/sql/relationship.py
--rw-rw-rw-   0        0        0     5717 2021-11-07 22:53:13.000000 duck-orm-1.0.1/duck_orm/sql/sql.py
-drwxrwxrwx   0        0        0        0 2021-11-07 22:56:57.337635 duck-orm-1.0.1/duck_orm/sql/sqlite/
--rw-rw-rw-   0        0        0     1804 2021-11-07 22:53:13.000000 duck-orm-1.0.1/duck_orm/sql/sqlite/__init__.py
-drwxrwxrwx   0        0        0        0 2021-11-07 22:56:57.342635 duck-orm-1.0.1/duck_orm/utils/
--rw-rw-rw-   0        0        0        0 2021-10-31 20:36:58.000000 duck-orm-1.0.1/duck_orm/utils/__init__.py
--rw-rw-rw-   0        0        0      385 2021-10-31 20:36:58.000000 duck-orm-1.0.1/duck_orm/utils/functions.py
-drwxrwxrwx   0        0        0        0 2021-11-07 22:56:57.315637 duck-orm-1.0.1/duck_orm.egg-info/
--rw-rw-rw-   0        0        0     2848 2021-11-07 22:56:57.000000 duck-orm-1.0.1/duck_orm.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      567 2021-11-07 22:56:57.000000 duck-orm-1.0.1/duck_orm.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2021-11-07 22:56:57.000000 duck-orm-1.0.1/duck_orm.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      104 2021-11-07 22:56:57.000000 duck-orm-1.0.1/duck_orm.egg-info/requires.txt
--rw-rw-rw-   0        0        0       79 2021-11-07 22:56:57.000000 duck-orm-1.0.1/duck_orm.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      482 2021-11-05 17:19:26.000000 duck-orm-1.0.1/pyproject.toml
--rw-rw-rw-   0        0        0      110 2021-11-07 22:56:57.346635 duck-orm-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1643 2021-10-31 20:36:58.000000 duck-orm-1.0.1/setup.py
+-rw-r--r--   0        0        0     1083 2023-05-13 18:37:31.617547 duck_orm-1.0.2/LICENSE
+-rw-r--r--   0        0        0     1815 2023-05-13 18:37:31.617547 duck_orm-1.0.2/README.md
+-rw-r--r--   0        0        0        1 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/__init__.py
+-rw-r--r--   0        0        0      428 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/exceptions.py
+-rw-r--r--   0        0        0    14321 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/model.py
+-rw-r--r--   0        0        0     3886 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/model_manager.py
+-rw-r--r--   0        0        0        0 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/sql/__init__.py
+-rw-r--r--   0        0        0     1282 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/sql/condition.py
+-rw-r--r--   0        0        0     4328 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/sql/fields.py
+-rw-r--r--   0        0        0      699 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/sql/operator.py
+-rw-r--r--   0        0        0      531 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/sql/postgres/__init__.py
+-rw-r--r--   0        0        0     8134 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/sql/relationship.py
+-rw-r--r--   0        0        0     5098 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/sql/sql.py
+-rw-r--r--   0        0        0     1665 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/sql/sqlite/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/utils/__init__.py
+-rw-r--r--   0        0        0      626 2023-05-13 18:37:31.617547 duck_orm-1.0.2/duck_orm/utils/functions.py
+-rw-r--r--   0        0        0     1968 2023-05-13 18:37:31.617547 duck_orm-1.0.2/pyproject.toml
+-rw-r--r--   0        0        0     3756 1970-01-01 00:00:00.000000 duck_orm-1.0.2/PKG-INFO
```

### Comparing `duck-orm-1.0.1/LICENSE` & `duck_orm-1.0.2/LICENSE`

 * *Ordering differences only*

 * *Files 18% similar despite different names*

```diff
@@ -1,21 +1,21 @@
-MIT License
-
-Copyright (c) 2021 Rich Elton Carvalho Ramalho
-
-Permission is hereby granted, free of charge, to any person obtaining a copy
-of this software and associated documentation files (the "Software"), to deal
-in the Software without restriction, including without limitation the rights
-to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
-copies of the Software, and to permit persons to whom the Software is
-furnished to do so, subject to the following conditions:
-
-The above copyright notice and this permission notice shall be included in all
-copies or substantial portions of the Software.
-
-THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
-IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
-FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
-AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
-LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
-OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+MIT License
+
+Copyright (c) 2021 Rich Elton Carvalho Ramalho
+
+Permission is hereby granted, free of charge, to any person obtaining a copy
+of this software and associated documentation files (the "Software"), to deal
+in the Software without restriction, including without limitation the rights
+to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+copies of the Software, and to permit persons to whom the Software is
+furnished to do so, subject to the following conditions:
+
+The above copyright notice and this permission notice shall be included in all
+copies or substantial portions of the Software.
+
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 SOFTWARE.
```

### Comparing `duck-orm-1.0.1/README.md` & `duck_orm-1.0.2/README.md`

 * *Files 27% similar despite different names*

```diff
@@ -1,66 +1,70 @@
-# [DuckORM](https://pypi.org/project/duck-orm/)
-
-The `Duck-ORM` package is an asynchronous ORM for Python, with support for **Postgres** and **SQLite**. ORM is built with:
-
-- [databases](https://github.com/encode/databases)
-
-**Requirements**: Python 3.8+
-
-**Duck-ORM is still under development**.
-
-## Installation
-
-```bash
-$ pip install duck-orm
-```
-
-!!! note
-    Don't forget to install `databases` before installing `duck-orm`. 
-
-## Quickstart
-
-For this example we will create a connection to the SQLite database and create a model.
-
-```bash
-$ pip install databases[sqlite]
-$ pip install ipython
-```
-
-Note that we want to use `ipython` here, because it supports using await expressions directly from the console.
-
-### Creating the connection to the SQLite database:
-
-```Python
-from databases import Database
-from duck_orm.model import Model
-
-db = Database('sqlite:///example.db')
-await db.connect()
-```
-
-### Defining a model:
-
-```Python
-from duck_orm.sql import fields as Field
-
-class Person(Model):
-    __tablename__ = 'persons'
-    __db__ = db
-
-    id: int = Field.Integer(primary_key=True, auto_increment=True)
-    first_name: str = Field.String(unique=True)
-    last_name: str = Field.String(not_null=True)
-    age: int = Field.BigInteger(min_value=18)
-
-# Table creation in the database.
-await Person.create()
-```
-
-- The `__tablename__` attribute is used to define the table's name in the database.
-- The `__db__` attribute is the instance of the database connection.
-- And then the definition of the fields, their types and restrictions.
-- And finally, the table creation in the database.
-
-## License
-
-`DuckORM` is built as an open-source tool and remains completely free(MIT license).
+# [DuckORM](https://pypi.org/project/duck-orm/)
+
+The `Duck-ORM` package is an asynchronous ORM for Python, with support for **Postgres** and **SQLite**. ORM is built with:
+
+- [databases](https://github.com/encode/databases)
+
+**Requirements**: Python 3.8+
+
+**Duck-ORM is still under development**.
+
+## Installation
+
+```bash
+$ pip install duck-orm
+```
+
+!!! note
+    Don't forget to install `databases` before installing `duck-orm`. 
+
+## Quickstart
+
+For this example we will create a connection to the SQLite database and create a model.
+
+```bash
+$ pip install databases[sqlite]
+$ pip install ipython
+```
+
+Note that we want to use `ipython` here, because it supports using await expressions directly from the console.
+
+### Creating the connection to the SQLite database:
+
+```Python
+from databases import Database
+from duck_orm.model import Model
+
+db = Database('sqlite:///example.db')
+await db.connect()
+```
+
+### Defining a model:
+
+```Python
+from duck_orm.sql import fields as Field
+
+class Person(Model):
+    __tablename__ = 'persons'
+    __db__ = db
+
+    id: int = Field.Integer(primary_key=True, auto_increment=True)
+    first_name: str = Field.String(unique=True)
+    last_name: str = Field.String(not_null=True)
+    age: int = Field.BigInteger(min_value=18)
+
+# Table creation in the database.
+await Person.create()
+```
+
+- The `__tablename__` attribute is used to define the table's name in the database.
+- The `__db__` attribute is the instance of the database connection.
+- And then the definition of the fields, their types and restrictions.
+- And finally, the table creation in the database.
+
+## Author
+
+- Rich Ramalho - [@richecr](https://github.com/richecr) - [@richzinho_ecr](https://twitter.com/richzinho_ecr)
+
+## License
+
+`DuckORM` is built as an open-source tool and remains completely free(MIT license).
```

### Comparing `duck-orm-1.0.1/duck_orm/sql/fields.py` & `duck_orm-1.0.2/duck_orm/sql/fields.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,138 +1,134 @@
-from typing import Dict
-from enum import Enum
-from datetime import datetime
-
-from duck_orm.sql.sqlite import TYPES_SQL as TYPES_SQL_LITE
-from duck_orm.sql.postgres import TYPES_SQL as TYPES_SQL_POSTGRES
-
-
-class ActionsEnum(Enum):
-    NO_ACTION = "NO ACTION"
-    RESTRICT = "RESTRICT"
-    CASCADE = "CASCADE"
-    SET_DEFAULT = "SET DEFAULT"
-    SET_NULL = "SET NULL"
-
-    @classmethod
-    def has_value(cls, value):
-        return value in cls._value2member_map_
-
-
-class Column:
-    def __init__(self, type_column: str, unique: bool = False,
-                 primary_key: bool = False, not_null: bool = False,
-                 auto_increment: bool = False, default_value=None):
-        self.unique = unique
-        self.primary_key = primary_key
-        self.not_null = not_null
-        self.type = type_column
-        self.auto_increment = auto_increment
-        self.default_value = default_value
-
-    def type_sql(self, dialect: str) -> str:
-        column_sql = self.get_dialect(dialect)[self.type]
-        return column_sql
-
-    def column_sql(self, dialect: str) -> str:
-        column_sql = self.get_dialect(dialect)[self.type]
-
-        if (self.auto_increment and dialect == 'postgresql'):
-            column_sql = "SERIAL"
-        if (self.primary_key):
-            column_sql += " PRIMARY KEY"
-        if (self.auto_increment and dialect != 'postgresql'):
-            column_sql += " AUTOINCREMENT"
-        if (self.not_null):
-            column_sql += " NOT NULL"
-        if (self.unique):
-            column_sql += " UNIQUE"
-        if (self.default_value):
-            column_sql += f" DEFAULT '{self.default_value}'"
-
-        return column_sql
-
-    def get_dialect(self, dialect: str) -> Dict[str, str]:
-        if dialect == 'postgresql':
-            return TYPES_SQL_POSTGRES
-        elif dialect == 'sqlite':
-            return TYPES_SQL_LITE
-        else:
-            return TYPES_SQL_LITE
-
-    def validate_action(self, on_delete: str, on_update: str):
-        if not ActionsEnum.has_value(on_delete):
-            message = "ON DELETE with action {on_delete} is invalid"
-            raise Exception(message.format(on_delete=on_delete))
-
-        if not ActionsEnum.has_value(on_update):
-            message = "ON UPDATE with action {on_update} is invalid"
-            raise Exception(message.format(on_update=on_update))
-
-
-class String(Column, str):
-    def __new__(cls, **kwargs):
-        return super().__new__(cls)
-
-    def __init__(self, unique: bool = False,
-                 primary_key: bool = False, not_null: bool = False,
-                 default_value=None):
-        super().__init__(
-            'str', unique, primary_key, not_null, default_value=default_value)
-
-
-class Integer(Column, int):
-    def __new__(cls, **kwargs):
-        return super().__new__(cls)
-
-    def __init__(
-        self, min_value: int = None, unique: bool = False,
-        primary_key: bool = False, auto_increment: bool = False,
-        not_null: bool = False, default_value=None
-    ):
-        self.min_value = min_value
-        super().__init__(
-            'int', unique, primary_key, auto_increment=auto_increment,
-            not_null=not_null, default_value=default_value
-        )
-
-
-class BigInteger(Column, int):
-    def __new__(cls, **kwargs):
-        return super().__new__(cls)
-
-    def __init__(self, unique: bool = False, primary_key: bool = False,
-                 default_value=None):
-        super().__init__(
-            'bigint', unique, primary_key, default_value=default_value)
-
-
-class Varchar(Column, str):
-    def __new__(cls, **kwargs):
-        return super().__new__(cls, kwargs)
-
-    def __init__(self, length: int, unique: bool = False,
-                 primary_key: bool = False, default_value=None):
-        self.length = length
-        super().__init__(
-            'varchar', unique, primary_key, default_value=default_value)
-
-    def column_sql(self, dialect: str):
-        column_sql = super().column_sql(dialect)
-        return column_sql.format(length=self.length)
-
-
-class Boolean(Column):
-    def __new__(cls, **kwargs):
-        return super().__new__(cls)
-
-    def __init__(self, not_null: bool = False, default_value=None):
-        super().__init__(
-            'boolean', not_null=not_null, default_value=default_value)
-
-
-class Timestamp(Column, datetime):
-    def __new__(cls, **kwargs):
-        return super().__new__(cls, 2021, 1, 1)
-
-    def __init__(self):
-        super().__init__('timestamp')
+from typing import Dict
+from enum import Enum
+from datetime import datetime
+
+from duck_orm.sql.sqlite import TYPES_SQL as TYPES_SQL_LITE
+from duck_orm.sql.postgres import TYPES_SQL as TYPES_SQL_POSTGRES
+
+
+class ActionsEnum(Enum):
+    NO_ACTION = 'NO ACTION'
+    RESTRICT = 'RESTRICT'
+    CASCADE = 'CASCADE'
+    SET_DEFAULT = 'SET DEFAULT'
+    SET_NULL = 'SET NULL'
+
+    @classmethod
+    def has_value(cls, value):
+        return value in cls._value2member_map_
+
+
+class Column:
+    def __init__(self, type_column: str, unique: bool = False,
+                 primary_key: bool = False, not_null: bool = False,
+                 auto_increment: bool = False, default_value=None):
+        self.unique = unique
+        self.primary_key = primary_key
+        self.not_null = not_null
+        self.type = type_column
+        self.auto_increment = auto_increment
+        self.default_value = default_value
+
+    def type_sql(self, dialect: str) -> str:
+        column_sql = self.get_dialect(dialect)[self.type]
+        return column_sql
+
+    def column_sql(self, dialect: str) -> str:
+        column_sql = self.get_dialect(dialect)[self.type]
+
+        if (self.auto_increment and dialect == 'postgresql'):
+            column_sql = 'SERIAL'
+        if (self.primary_key):
+            column_sql += ' PRIMARY KEY'
+        if (self.auto_increment and dialect != 'postgresql'):
+            column_sql += ' AUTOINCREMENT'
+        if (self.not_null):
+            column_sql += ' NOT NULL'
+        if (self.unique):
+            column_sql += ' UNIQUE'
+        if (self.default_value):
+            column_sql += f" DEFAULT '{self.default_value}'"
+
+        return column_sql
+
+    def get_dialect(self, dialect: str) -> Dict[str, str]:
+        if dialect == 'postgresql':
+            return TYPES_SQL_POSTGRES
+        elif dialect == 'sqlite':
+            return TYPES_SQL_LITE
+        else:
+            return TYPES_SQL_LITE
+
+    def validate_action(self, on_delete: str, on_update: str):
+        if not ActionsEnum.has_value(on_delete):
+            raise Exception('ON DELETE with action {on_delete} is invalid'.format(on_delete=on_delete))
+
+        if not ActionsEnum.has_value(on_update):
+            raise Exception('ON UPDATE with action {on_update} is invalid'.format(on_update=on_update))
+
+
+class String(Column, str):
+    def __new__(cls, **kwargs):
+        return super().__new__(cls)
+
+    def __init__(
+            self,
+            unique: bool = False,
+            primary_key: bool = False,
+            not_null: bool = False,
+            default_value=None
+    ):
+        super().__init__('str', unique, primary_key, not_null, default_value=default_value)
+
+
+class Integer(Column, int):
+    def __new__(cls, **kwargs):
+        return super().__new__(cls)
+
+    def __init__(
+        self, min_value: int = None, unique: bool = False,
+        primary_key: bool = False, auto_increment: bool = False,
+        not_null: bool = False, default_value=None
+    ):
+        self.min_value = min_value
+        super().__init__(
+            'int', unique, primary_key, auto_increment=auto_increment,
+            not_null=not_null, default_value=default_value
+        )
+
+
+class BigInteger(Column, int):
+    def __new__(cls, **kwargs):
+        return super().__new__(cls)
+
+    def __init__(self, unique: bool = False, primary_key: bool = False, default_value=None):
+        super().__init__('bigint', unique, primary_key, default_value=default_value)
+
+
+class Varchar(Column, str):
+    def __new__(cls, **kwargs):
+        return super().__new__(cls, kwargs)
+
+    def __init__(self, length: int, unique: bool = False, primary_key: bool = False, default_value=None):
+        self.length = length
+        super().__init__('varchar', unique, primary_key, default_value=default_value)
+
+    def column_sql(self, dialect: str):
+        column_sql = super().column_sql(dialect)
+        return column_sql.format(length=self.length)
+
+
+class Boolean(Column):
+    def __new__(cls, **kwargs):
+        return super().__new__(cls)
+
+    def __init__(self, not_null: bool = False, default_value=None):
+        super().__init__('boolean', not_null=not_null, default_value=default_value)
+
+
+class Timestamp(Column, datetime):
+    def __new__(cls, **kwargs):
+        return super().__new__(cls, 2021, 1, 1)
+
+    def __init__(self):
+        super().__init__('timestamp')
```

### Comparing `duck-orm-1.0.1/duck_orm/sql/sql.py` & `duck_orm-1.0.2/duck_orm/sql/sql.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,176 +1,136 @@
-from typing import List, Mapping
-
-SELECT_TABLES_SQL = "SELECT name FROM sqlite_master where type = 'table';"
-SELECT_TABLE_SQL = "SELECT {fields} FROM {table}"
-LIMIT_SQL = " LIMIT {limit}"
-ORDER_BY_SQL = " ORDER BY {name_id} DESC"
-SELECT_TABLE_WHERE_SQL = SELECT_TABLE_SQL + " WHERE {conditions}"
-SELECT_LAST_ID_ORDER_BY_SQL = "SELECT {name_id} FROM {table} " +\
-    ORDER_BY_SQL + " LIMIT 1;"
-
-INSERT_INTO_SQL = "INSERT INTO {table}({fields_name}) VALUES({placeholders});"
-CREATE_SQL = "CREATE TABLE IF NOT EXISTS {name} ({fields});"
-UPDATE_SQL = "UPDATE {table} SET {fields_values} WHERE {conditions};"
-DELETE_SQL = "DELETE FROM {table} WHERE {conditions};"
-DROP_TABLE_SQL = "DROP TABLE IF EXISTS {name}"
-
-ADD_COLUMN_SQL = "ALTER TABLE {table_name} " + \
-    "ADD COLUMN {field_name} {field_type} "
-
-ADD_FK_SQL = "REFERENCES {table_relation} ({field}) " + \
-    "ON DELETE {on_delete} ON UPDATE {on_update}"
-
-ADD_FK_COLUMN_SQL = "FOREIGN KEY ({name}) " + ADD_FK_SQL
-
-ADD_FK_WITH_CONSTRAINT_WITHOUT_ALTER_SQL = "CONSTRAINT {name_constraint} " + \
-    ADD_FK_COLUMN_SQL
-
-ADD_FK_WITH_CONSTRAINT_SQL = "CONSTRAINT {name_constraint} " + ADD_FK_SQL
-
-ADD_COLUMN_FK_WITH_CONSTRAINT_SQL = ADD_COLUMN_SQL + ADD_FK_WITH_CONSTRAINT_SQL
-ADD_COLUMN_FK_SQL = ADD_COLUMN_SQL + ADD_FK_SQL
-
-
-class QueryExecutor:
-    @classmethod
-    def create_sql(cls, name_table: str, fields: List[str]):
-        return CREATE_SQL.format(name=name_table, fields=", ".join(fields))
-
-    @classmethod
-    def insert_sql(
-            cls,
-            name_table: str,
-            fields_name: List[str],
-            placeholders: List[str]
-    ):
-        return INSERT_INTO_SQL.format(table=name_table,
-                                      fields_name=", ".join(fields_name),
-                                      placeholders=", ".join(placeholders))
-
-    @classmethod
-    def update_sql(
-            cls,
-            name_table: str,
-            fields_values: List[str],
-            conditions: List[str]
-    ):
-        return UPDATE_SQL.format(table=name_table,
-                                 fields_values=", ".join(fields_values),
-                                 conditions=", ".join(conditions))
-
-    @classmethod
-    def select_sql(
-            cls,
-            name_table: str,
-            fields: List[str],
-            conditions: str,
-            limit: int = None
-    ) -> str:
-        sql = SELECT_TABLE_WHERE_SQL
-        if (limit is not None):
-            sql += LIMIT_SQL
-
-        return sql.format(
-            table=name_table,
-            fields=", ".join(fields),
-            conditions=conditions,
-            limit=limit
-        )
-
-    @classmethod
-    def select_last_id(cls, name_id: str, table: str):
-        return SELECT_LAST_ID_ORDER_BY_SQL.format(name_id=name_id, table=table)
-
-    @classmethod
-    def delete_sql(cls, name_table: str, conditions: str):
-        return DELETE_SQL.format(table=name_table, conditions=conditions)
-
-    @classmethod
-    def drop_table(cls, name_table: str, cascade: bool = False):
-        sql = DROP_TABLE_SQL.format(name=name_table)
-        if cascade:
-            sql += " CASCADE;"
-
-        return sql
-
-    @classmethod
-    def alter_table_add_column_with_constraint(
-        cls,
-        table_name: str,
-        field_name: str,
-        table_relation: str,
-        field: str,
-        field_type: str,
-        on_delete: str,
-        on_update: str,
-        name_constraint: str = ''
-    ) -> str:
-        args = {
-            "table_name": table_name,
-            "field_name": field_name,
-            "table_relation": table_relation,
-            "field": field,
-            "field_type": field_type,
-            "on_delete": on_delete,
-            "on_update": on_update
-        }
-        if name_constraint != "":
-            return ADD_COLUMN_FK_WITH_CONSTRAINT_SQL.format(
-                **args, name_constraint=name_constraint)
-
-        return ADD_COLUMN_FK_SQL.format(**args)
-
-    @classmethod
-    def add_foreing_key_column(
-        cls,
-        name: str,
-        table_name: str,
-        field: str,
-        on_delete: str,
-        on_update: str,
-        name_constraint: str = ""
-    ) -> str:
-        args = {
-            "name": name,
-            "table_relation": table_name,
-            "field": field,
-            "on_delete": on_delete,
-            "on_update": on_update
-        }
-        if name_constraint != "":
-            return ADD_FK_WITH_CONSTRAINT_WITHOUT_ALTER_SQL.format(
-                **args, name_constraint=name_constraint)
-
-        return ADD_FK_COLUMN_SQL.format(**args)
-
-    @classmethod
-    def select_tables_sql(cls, name_table: str):
-        return SELECT_TABLES_SQL
-
-    @classmethod
-    def parser(
-            cls,
-            row: Mapping,
-            fields: List[str] = [],
-            fields_foreign_key: dict = {}
-    ) -> dict:
-        entity = {}
-        if (fields != []):
-            for field in fields:
-                if isinstance(field, tuple):
-                    field = field[0]
-
-                if (row.__contains__(field)):
-                    if fields_foreign_key.__contains__(field):
-                        entity[field] = fields_foreign_key.get(field)
-                    else:
-                        entity[field] = row.get(field)
-                elif fields_foreign_key.__contains__(field):
-                    entity[field] = fields_foreign_key[field]
-                else:
-                    entity[field] = None
-        else:
-            for key, value in row.items():
-                entity[key] = value
-
-        return entity
+from typing import List, Mapping
+
+SELECT_TABLES_SQL = "SELECT name FROM sqlite_master where type = 'table';"
+SELECT_TABLE_SQL = "SELECT {fields} FROM {table}"
+LIMIT_SQL = " LIMIT {limit}"
+ORDER_BY_SQL = " ORDER BY {name_id} DESC"
+SELECT_TABLE_WHERE_SQL = SELECT_TABLE_SQL + " WHERE {conditions}"
+SELECT_LAST_ID_ORDER_BY_SQL = "SELECT {name_id} FROM {table} " + ORDER_BY_SQL + " LIMIT 1;"
+INSERT_INTO_SQL = "INSERT INTO {table}({fields_name}) VALUES({placeholders});"
+CREATE_SQL = "CREATE TABLE IF NOT EXISTS {name} ({fields});"
+UPDATE_SQL = "UPDATE {table} SET {fields_values} WHERE {conditions};"
+DELETE_SQL = "DELETE FROM {table} WHERE {conditions};"
+DROP_TABLE_SQL = "DROP TABLE IF EXISTS {name}"
+ADD_COLUMN_SQL = "ALTER TABLE {table_name} ADD COLUMN {field_name} {field_type} "
+ADD_FK_SQL = "REFERENCES {table_relation} ({field}) ON DELETE {on_delete} ON UPDATE {on_update}"
+ADD_FK_COLUMN_SQL = "FOREIGN KEY ({name}) " + ADD_FK_SQL
+ADD_FK_WITH_CONSTRAINT_WITHOUT_ALTER_SQL = "CONSTRAINT {name_constraint} " + ADD_FK_COLUMN_SQL
+ADD_FK_WITH_CONSTRAINT_SQL = "CONSTRAINT {name_constraint} " + ADD_FK_SQL
+ADD_COLUMN_FK_WITH_CONSTRAINT_SQL = ADD_COLUMN_SQL + ADD_FK_WITH_CONSTRAINT_SQL
+ADD_COLUMN_FK_SQL = ADD_COLUMN_SQL + ADD_FK_SQL
+
+
+class QueryExecutor:
+    @classmethod
+    def create_sql(cls, name_table: str, fields: List[str]):
+        return CREATE_SQL.format(name=name_table, fields=", ".join(fields))
+
+    @classmethod
+    def insert_sql(cls, name_table: str, fields_name: List[str], placeholders: List[str]):
+        return INSERT_INTO_SQL.format(
+            table=name_table, fields_name=", ".join(fields_name), placeholders=", ".join(placeholders))
+
+    @classmethod
+    def update_sql(cls, name_table: str, fields_values: List[str], conditions: List[str]):
+        return UPDATE_SQL.format(
+            table=name_table, fields_values=", ".join(fields_values), conditions=", ".join(conditions))
+
+    @classmethod
+    def select_sql(cls, name_table: str, fields: List[str], conditions: str, limit: int = None) -> str:
+        sql = SELECT_TABLE_WHERE_SQL
+        if (limit is not None):
+            sql += LIMIT_SQL
+
+        return sql.format(table=name_table, fields=", ".join(fields), conditions=conditions, limit=limit)
+
+    @classmethod
+    def select_last_id(cls, name_id: str, table: str):
+        return SELECT_LAST_ID_ORDER_BY_SQL.format(name_id=name_id, table=table)
+
+    @classmethod
+    def delete_sql(cls, name_table: str, conditions: str):
+        return DELETE_SQL.format(table=name_table, conditions=conditions)
+
+    @classmethod
+    def drop_table(cls, name_table: str, cascade: bool = False):
+        sql = DROP_TABLE_SQL.format(name=name_table)
+        if cascade:
+            sql += " CASCADE;"
+        return sql
+
+    @classmethod
+    def alter_table_add_column_with_constraint(
+        cls,
+        table_name: str,
+        field_name: str,
+        table_relation: str,
+        field: str,
+        field_type: str,
+        on_delete: str,
+        on_update: str,
+        name_constraint: str = ''
+    ) -> str:
+        args = {
+            "table_name": table_name,
+            "field_name": field_name,
+            "table_relation": table_relation,
+            "field": field,
+            "field_type": field_type,
+            "on_delete": on_delete,
+            "on_update": on_update
+        }
+        if name_constraint != "":
+            return ADD_COLUMN_FK_WITH_CONSTRAINT_SQL.format(**args, name_constraint=name_constraint)
+        return ADD_COLUMN_FK_SQL.format(**args)
+
+    @classmethod
+    def add_foreing_key_column(
+        cls,
+        name: str,
+        table_name: str,
+        field: str,
+        on_delete: str,
+        on_update: str,
+        name_constraint: str = ""
+    ) -> str:
+        args = {
+            "name": name,
+            "table_relation": table_name,
+            "field": field,
+            "on_delete": on_delete,
+            "on_update": on_update
+        }
+        if name_constraint != "":
+            return ADD_FK_WITH_CONSTRAINT_WITHOUT_ALTER_SQL.format(**args, name_constraint=name_constraint)
+        return ADD_FK_COLUMN_SQL.format(**args)
+
+    @classmethod
+    def select_tables_sql(cls):
+        return SELECT_TABLES_SQL
+
+    @classmethod
+    def parser(
+            cls,
+            row: Mapping,
+            fields: List[str] = [],
+            fields_foreign_key: dict = {}
+    ) -> dict:
+        entity = {}
+        if (fields != []):
+            for field in fields:
+                if isinstance(field, tuple):
+                    field = field[0]
+
+                if (row.__contains__(field)):
+                    if fields_foreign_key.__contains__(field):
+                        entity[field] = fields_foreign_key.get(field)
+                    else:
+                        entity[field] = row.get(field)
+                elif fields_foreign_key.__contains__(field):
+                    entity[field] = fields_foreign_key[field]
+                else:
+                    entity[field] = None
+        else:
+            for key, value in row.items():
+                entity[key] = value
+        return entity
```

