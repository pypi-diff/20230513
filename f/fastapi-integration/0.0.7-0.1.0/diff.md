# Comparing `tmp/fastapi-integration-0.0.7.tar.gz` & `tmp/fastapi-integration-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fastapi-integration-0.0.7.tar", last modified: Thu Apr  6 12:20:41 2023, max compression
+gzip compressed data, was "fastapi-integration-0.1.0.tar", last modified: Fri May 12 17:36:28 2023, max compression
```

## Comparing `fastapi-integration-0.0.7.tar` & `fastapi-integration-0.1.0.tar`

### file list

```diff
@@ -1,46 +1,54 @@
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.485032 fastapi-integration-0.0.7/
--rw-rw-rw-   0        0        0      301 2023-04-06 12:20:41.485032 fastapi-integration-0.0.7/PKG-INFO
--rw-rw-rw-   0        0        0     7054 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/README.md
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.472029 fastapi-integration-0.0.7/fastapi_integration/
--rw-rw-rw-   0        0        0     3968 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/__init__.py
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.476029 fastapi-integration-0.0.7/fastapi_integration/admin/
--rw-rw-rw-   0        0        0        0 2023-04-01 15:15:54.000000 fastapi-integration-0.0.7/fastapi_integration/admin/__init__.py
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.478030 fastapi-integration-0.0.7/fastapi_integration/auth/
--rw-rw-rw-   0        0        0        0 2023-04-01 15:15:52.000000 fastapi-integration-0.0.7/fastapi_integration/auth/__init__.py
--rw-rw-rw-   0        0        0     2428 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/auth/routers.py
--rw-rw-rw-   0        0        0      188 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/auth/schemas.py
--rw-rw-rw-   0        0        0      117 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/auth/security.py
--rw-rw-rw-   0        0        0     3794 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/auth/utils.py
--rw-rw-rw-   0        0        0       97 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/common.py
--rw-rw-rw-   0        0        0     1415 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/config.py
--rw-rw-rw-   0        0        0     2897 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/db.py
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.479030 fastapi-integration-0.0.7/fastapi_integration/generic/
--rw-rw-rw-   0        0        0        0 2023-04-01 15:15:50.000000 fastapi-integration-0.0.7/fastapi_integration/generic/__init__.py
--rw-rw-rw-   0        0        0     6684 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/generic/crud.py
--rw-rw-rw-   0        0        0        0 2023-04-01 12:17:01.000000 fastapi-integration-0.0.7/fastapi_integration/generic/views.py
--rw-rw-rw-   0        0        0     1285 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/models.py
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.482029 fastapi-integration-0.0.7/fastapi_integration/orm/
--rw-rw-rw-   0        0        0        0 2023-04-01 15:15:48.000000 fastapi-integration-0.0.7/fastapi_integration/orm/__init__.py
--rw-rw-rw-   0        0        0     9460 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/orm/base.py
--rw-rw-rw-   0        0        0      334 2023-04-04 22:18:10.000000 fastapi-integration-0.0.7/fastapi_integration/orm/models.py
--rw-rw-rw-   0        0        0    13317 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/orm/queries.py
--rw-rw-rw-   0        0        0     1308 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/orm/signals.py
--rw-rw-rw-   0        0        0        0 2023-04-04 13:39:29.000000 fastapi-integration-0.0.7/fastapi_integration/orm/transaction.py
--rw-rw-rw-   0        0        0      981 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/fastapi_integration/orm/utils.py
--rw-rw-rw-   0        0        0        0 2023-04-01 12:23:41.000000 fastapi-integration-0.0.7/fastapi_integration/schema.py
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.483029 fastapi-integration-0.0.7/fastapi_integration/utils/
--rw-rw-rw-   0        0        0        0 2023-04-01 15:15:47.000000 fastapi-integration-0.0.7/fastapi_integration/utils/__init__.py
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.475029 fastapi-integration-0.0.7/fastapi_integration.egg-info/
--rw-rw-rw-   0        0        0      301 2023-04-06 12:20:41.000000 fastapi-integration-0.0.7/fastapi_integration.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1116 2023-04-06 12:20:41.000000 fastapi-integration-0.0.7/fastapi_integration.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-06 12:20:41.000000 fastapi-integration-0.0.7/fastapi_integration.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       33 2023-04-06 12:20:41.000000 fastapi-integration-0.0.7/fastapi_integration.egg-info/requires.txt
--rw-rw-rw-   0        0        0       26 2023-04-06 12:20:41.000000 fastapi-integration-0.0.7/fastapi_integration.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-04-06 12:20:41.485032 fastapi-integration-0.0.7/setup.cfg
--rw-rw-rw-   0        0        0      477 2023-04-06 12:19:57.000000 fastapi-integration-0.0.7/setup.py
-drwxrwxrwx   0        0        0        0 2023-04-06 12:20:41.484029 fastapi-integration-0.0.7/tests/
--rw-rw-rw-   0        0        0        0 2023-04-06 11:11:49.000000 fastapi-integration-0.0.7/tests/__init__.py
--rw-rw-rw-   0        0        0    10833 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/tests/complex_query.py
--rw-rw-rw-   0        0        0     7021 2023-04-06 12:07:46.000000 fastapi-integration-0.0.7/tests/query.py
--rw-rw-rw-   0        0        0      162 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/tests/resolve_path.py
--rw-rw-rw-   0        0        0      979 2023-04-06 12:07:44.000000 fastapi-integration-0.0.7/tests/start.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.352298 fastapi-integration-0.1.0/
+-rw-rw-rw-   0        0        0      301 2023-05-12 17:36:28.351297 fastapi-integration-0.1.0/PKG-INFO
+-rw-rw-rw-   0        0        0     7114 2023-05-12 15:02:24.000000 fastapi-integration-0.1.0/README.md
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.322255 fastapi-integration-0.1.0/examples/
+-rw-rw-rw-   0        0        0        0 2023-05-10 12:42:06.000000 fastapi-integration-0.1.0/examples/__init__.py
+-rw-rw-rw-   0        0        0      157 2023-05-12 14:59:56.000000 fastapi-integration-0.1.0/examples/admin.py
+-rw-rw-rw-   0        0        0      374 2023-05-12 14:08:35.000000 fastapi-integration-0.1.0/examples/base.py
+-rw-rw-rw-   0        0        0     1306 2023-05-12 15:00:08.000000 fastapi-integration-0.1.0/examples/main.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.326255 fastapi-integration-0.1.0/fastapi_integration/
+-rw-rw-rw-   0        0        0     6607 2023-05-12 16:14:47.000000 fastapi-integration-0.1.0/fastapi_integration/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.342271 fastapi-integration-0.1.0/fastapi_integration/admin/
+-rw-rw-rw-   0        0        0     1078 2023-05-12 15:09:09.000000 fastapi-integration-0.1.0/fastapi_integration/admin/__init__.py
+-rw-rw-rw-   0        0        0     1090 2023-05-12 16:12:12.000000 fastapi-integration-0.1.0/fastapi_integration/admin/generator.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.344272 fastapi-integration-0.1.0/fastapi_integration/auth/
+-rw-rw-rw-   0        0        0     1694 2023-05-12 15:09:42.000000 fastapi-integration-0.1.0/fastapi_integration/auth/__init__.py
+-rw-rw-rw-   0        0        0     4188 2023-05-12 16:02:33.000000 fastapi-integration-0.1.0/fastapi_integration/auth/routers.py
+-rw-rw-rw-   0        0        0     1236 2023-05-12 16:02:47.000000 fastapi-integration-0.1.0/fastapi_integration/auth/schemas.py
+-rw-rw-rw-   0        0        0     3360 2023-05-12 15:14:15.000000 fastapi-integration-0.1.0/fastapi_integration/auth/utils.py
+-rw-rw-rw-   0        0        0      286 2023-05-12 16:09:08.000000 fastapi-integration-0.1.0/fastapi_integration/common.py
+-rw-rw-rw-   0        0        0     3505 2023-05-12 15:38:17.000000 fastapi-integration-0.1.0/fastapi_integration/config.py
+-rw-rw-rw-   0        0        0     5227 2023-05-12 16:43:57.000000 fastapi-integration-0.1.0/fastapi_integration/db.py
+-rw-rw-rw-   0        0        0      909 2023-05-12 16:11:09.000000 fastapi-integration-0.1.0/fastapi_integration/dependencies.py
+-rw-rw-rw-   0        0        0     1018 2023-05-12 16:07:33.000000 fastapi-integration-0.1.0/fastapi_integration/exceptions.py
+-rw-rw-rw-   0        0        0      603 2023-05-12 16:07:52.000000 fastapi-integration-0.1.0/fastapi_integration/features.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.345272 fastapi-integration-0.1.0/fastapi_integration/generic/
+-rw-rw-rw-   0        0        0        0 2023-04-01 15:15:50.000000 fastapi-integration-0.1.0/fastapi_integration/generic/__init__.py
+-rw-rw-rw-   0        0        0     8968 2023-05-12 15:17:57.000000 fastapi-integration-0.1.0/fastapi_integration/generic/crud.py
+-rw-rw-rw-   0        0        0        0 2023-04-01 12:17:01.000000 fastapi-integration-0.1.0/fastapi_integration/generic/views.py
+-rw-rw-rw-   0        0        0     2635 2023-05-12 16:08:42.000000 fastapi-integration-0.1.0/fastapi_integration/models.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.348271 fastapi-integration-0.1.0/fastapi_integration/orm/
+-rw-rw-rw-   0        0        0        0 2023-04-01 15:15:48.000000 fastapi-integration-0.1.0/fastapi_integration/orm/__init__.py
+-rw-rw-rw-   0        0        0    10300 2023-05-10 14:45:33.000000 fastapi-integration-0.1.0/fastapi_integration/orm/base.py
+-rw-rw-rw-   0        0        0      242 2023-05-12 16:45:11.000000 fastapi-integration-0.1.0/fastapi_integration/orm/models.py
+-rw-rw-rw-   0        0        0    13436 2023-05-10 13:51:16.000000 fastapi-integration-0.1.0/fastapi_integration/orm/queries.py
+-rw-rw-rw-   0        0        0     1251 2023-05-08 17:22:39.000000 fastapi-integration-0.1.0/fastapi_integration/orm/signals.py
+-rw-rw-rw-   0        0        0        0 2023-04-04 13:39:29.000000 fastapi-integration-0.1.0/fastapi_integration/orm/transaction.py
+-rw-rw-rw-   0        0        0      985 2023-05-07 14:59:54.000000 fastapi-integration-0.1.0/fastapi_integration/orm/utils.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.349272 fastapi-integration-0.1.0/fastapi_integration/utils/
+-rw-rw-rw-   0        0        0        0 2023-04-01 15:15:47.000000 fastapi-integration-0.1.0/fastapi_integration/utils/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.341271 fastapi-integration-0.1.0/fastapi_integration.egg-info/
+-rw-rw-rw-   0        0        0      301 2023-05-12 17:36:28.000000 fastapi-integration-0.1.0/fastapi_integration.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1281 2023-05-12 17:36:28.000000 fastapi-integration-0.1.0/fastapi_integration.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-12 17:36:28.000000 fastapi-integration-0.1.0/fastapi_integration.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       94 2023-05-12 17:36:28.000000 fastapi-integration-0.1.0/fastapi_integration.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       35 2023-05-12 17:36:28.000000 fastapi-integration-0.1.0/fastapi_integration.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-12 17:36:28.352298 fastapi-integration-0.1.0/setup.cfg
+-rw-rw-rw-   0        0        0      612 2023-05-12 17:36:25.000000 fastapi-integration-0.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.349272 fastapi-integration-0.1.0/tests/
+-rw-rw-rw-   0        0        0        0 2023-05-10 12:42:06.000000 fastapi-integration-0.1.0/tests/__init__.py
+-rw-rw-rw-   0        0        0      374 2023-05-12 15:00:58.000000 fastapi-integration-0.1.0/tests/base.py
+drwxrwxrwx   0        0        0        0 2023-05-12 17:36:28.351297 fastapi-integration-0.1.0/tests/query/
+-rw-rw-rw-   0        0        0        0 2023-04-06 11:11:49.000000 fastapi-integration-0.1.0/tests/query/__init__.py
+-rw-rw-rw-   0        0        0    10030 2023-05-09 16:06:29.000000 fastapi-integration-0.1.0/tests/query/test_complex.py
+-rw-rw-rw-   0        0        0     7270 2023-05-09 16:07:05.000000 fastapi-integration-0.1.0/tests/query/test_simple.py
```

### Comparing `fastapi-integration-0.0.7/fastapi_integration/models.py` & `fastapi-integration-0.1.0/fastapi_integration/models.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,13 +1,32 @@
-from .orm.models import AbstractModel
-from sqlalchemy import Column, Integer, String, DateTime, Boolean
 from datetime import datetime
 
+from sqlalchemy import Column, Integer, String, DateTime, Boolean
+
+from fastapi_integration.orm.models import AbstractModel
+from fastapi_integration.dependencies import SQLAlchemy
+
 
-class AbstractBaseUser(AbstractModel):
+class AbstractBaseUser(SQLAlchemy, AbstractModel):
+    """
+    Represents the abstract base user model.
+
+    This class uses the SQLAlchemy dependency and the AbstractModel class.
+
+    Attributes:
+        id: The primary key of the user.
+        email: The email of the user.
+        username: The username of the user.
+        password: The password of the user.
+        created_at: The timestamp of when the user was created.
+        updated_at: The timestamp of when the user was last updated.
+        is_active: Indicates whether the user is active.
+        is_admin: Indicates whether the user is an administrator.
+        last_login: The timestamp of the user's last login.
+    """
     __abstract__ = True
 
     id = Column(Integer, primary_key=True, index=True)
     email = Column(String(50), unique=True, index=True)
     username = Column(String(50), unique=True, index=True, nullable=True)
     password = Column(String(200))
     created_at = Column(DateTime, default=datetime.utcnow)
@@ -17,15 +36,29 @@
         onupdate=datetime.utcnow
     )
     is_active = Column(Boolean, default=True)
     is_admin = Column(Boolean, default=False)
     last_login = Column(DateTime, nullable=True, default=None)
 
 
-class AbstractOAuth2User(AbstractModel):
+class AbstractOAuth2User(SQLAlchemy, AbstractModel):
+    """
+    Represents the abstract OAuth2 user model.
+
+    This class extends the SQLAlchemy dependency and the AbstractModel class.
+
+    Attributes:
+        id: The primary key of the OAuth2 user.
+        oauth_name: The name of the OAuth provider.
+        access_token: The access token for the OAuth user.
+        expires_at: The timestamp of when the access token expires.
+        refresh_token: The refresh token for the OAuth user.
+        account_id: The account ID associated with the OAuth user.
+        account_email: The email associated with the OAuth user.
+    """
     __abstract__ = True
 
     id = Column(Integer, primary_key=True, index=True)
     oauth_name = Column(String(100), unique=True, index=True)
     access_token = Column(String(200), unique=True, index=True)
     expires_at = Column(DateTime, nullable=True, default=None)
     refresh_token = Column(String(200), unique=True, index=True)
```

### Comparing `fastapi-integration-0.0.7/fastapi_integration/orm/base.py` & `fastapi-integration-0.1.0/fastapi_integration/orm/base.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,25 +1,28 @@
+from typing import (Union, Sequence, Tuple)
+
 from sqlalchemy import func
 from sqlalchemy import (
     select,
     and_,
 )
 from sqlalchemy.ext.asyncio import AsyncSession
 from sqlalchemy.orm import RelationshipProperty
-from .utils import get_association_id_column
 from sqlalchemy.sql.selectable import Select
-from typing import (Union, Sequence, Tuple)
+
+from fastapi_integration.dependencies import SQLAlchemy
+from .utils import get_association_id_column
 
 
-class BaseQuery:
+class BaseQuery(SQLAlchemy):
     needs_scalar: bool = True
     _instance = None
     _prefetch_related_joins = []
-    _joint: list = list()
-    _smtm: Select = None
+    _joint: list = []
+    _query: Select = None
     condition_map = {
         'exact': lambda column, value: column == value,
         'contains': lambda column, value: column.contains(value),
         'in': lambda column, value: column.in_(value),
         'gt': lambda column, value: column > value,
         'gte': lambda column, value: column >= value,
         'lt': lambda column, value: column < value,
@@ -31,79 +34,94 @@
         'year': lambda column, value: func.extract('year', column) == value,
         'month': lambda column, value: func.extract('month', column) == value,
         'day': lambda column, value: func.extract('day', column) == value,
         'iexact': lambda column, value: column.ilike(value),
         'icontains': lambda column, value: column.ilike(f"%{value}%"),
         'istartswith': lambda column, value: column.ilike(f"{value}%"),
         'iendswith': lambda column, value: column.ilike(f"%{value}"),
+        "week": lambda f, v: func.extract("week", f) == v,
+        "week_day": lambda f, v: func.extract("dow", f) == v,
+        "iso_week_day": lambda f, v: func.extract("isodow", f) == v,
+        "iso_year": lambda f, v: func.extract("isoyear", f) == v,
+        "quarter": lambda f, v: func.extract("quarter", f) == v,
+        "time": lambda f, v: func.time(f) == v,
+        "hour": lambda f, v: func.extract("hour", f) == v,
+        "minute": lambda f, v: func.extract("minute", f) == v,
+        "second": lambda f, v: func.extract("second", f) == v,
+        "isnull": lambda f, v: f.is_(None) if v else f.isnot(None),
+        "regex": lambda f, v: f.op("~")(v),
+        "iregex": lambda f, v: f.op("~*")(v),
     }
 
     def __init__(self, cls):
         self.cls = cls
 
     def __iter__(self):
-        return self.execute().__iter__()
+        return self.execute(db_session=None).__iter__()
 
-    def execute(self) -> Sequence:
-        if self._smtm is not None:
-            return
-        else:
-            raise ValueError("Query is not built")
+    async def execute(
+            self, db_session: AsyncSession
+    ) -> Sequence:
+        if self.query is not None:
+            result = await db_session.execute(self.query)
+            if self.needs_scalar:
+                return result.scalars().all()
+            return result.all()
+        raise ValueError("Query is not built")
 
     @property
-    def smtm(self) -> Select:
-        return self._smtm
+    def query(self) -> Select:
+        return self._query
 
-    @smtm.setter
-    def smtm(self, value):
-        self._smtm = value
+    @query.setter
+    def query(self, value):
+        self._query = value
 
     @property
     def instance(self):
         return self._instance
 
     @instance.setter
     def instance(self, value):
         self._instance = value
 
-    async def _build_query(
+    def _build_query(
         self,
-        db_session: AsyncSession,
-        joins: set = set(),
+        joins: set,
         order_by=None,
         skip: int = None,
         limit: int = None,
         distinct_fields=None,
         where=None,
         select_models=None,
         **kwargs
     ) -> Select:
         """
         Build a basic query for the current model.
-        :param db_session: The async database session.
         :return: A query object.
         """
+        joins = joins or set()
         joint = []
         if select_models is not None:
-            stmt = select(*select_models, self.cls).select_from(self.cls)
+            query = select(*select_models, self.cls).select_from(self.cls)
             self.needs_scalar = False
         else:
-            stmt = select(self.cls)
+            query = select(self.cls)
             self.needs_scalar = True
 
         if where is not None:
-            stmt = stmt.where(*where)
+            query = query.where(*where)
 
         for join_condition in joins:
             related_model = (
                 join_condition.left.table
                 if join_condition.left.table != self.cls.__table__
                 else join_condition.right.table
             )
-            stmt = stmt.join(related_model, join_condition)
+            query = query.join(related_model, join_condition)
             joint.append(related_model)
 
         conditions = []
         for key, value in kwargs.items():
             filter_parts = key.split('__')
             column_name = filter_parts[0]
             filter_type = filter_parts[-1] if len(filter_parts) > 1 else None
@@ -114,157 +132,159 @@
                         self.cls, column_name
                     ).property), RelationshipProperty
                 ):
                     parent_cls = getattr(
                         self.cls, column_name
                     ).property.mapper.class_
                     if parent_cls not in joint:
-                        stmt = stmt.join(parent_cls)
+                        query = query.join(parent_cls)
                         joint.append(parent_cls)
                 else:
                     parent_cls = self.cls
 
                 filter_field = next(
                     (obj for obj in filter_parts if hasattr(parent_cls, obj)),
                     None
                 )
                 if filter_field is None:
                     raise ValueError("This Column does not exist")
                 column = getattr(parent_cls, filter_field)
-                conditions = await self.apply_filter_type(
+                conditions = self.apply_filter_type(
                     filter_type, conditions, column, value
                 )
 
         if conditions:
-            stmt = stmt.where(and_(*conditions))
+            query = query.where(and_(*conditions))
 
         if order_by:
-            stmt = self._apply_ordering(stmt, order_by)
-            stmt = self._apply_distinct(
-                stmt, distinct_fields
+            query = self._apply_ordering(query, order_by)
+            query = self._apply_distinct(
+                query, distinct_fields
             )
         elif distinct_fields:
             raise ValueError(
                 "You must specify order_by when using distinct_fields"
             )
 
         if skip:
-            stmt = stmt.offset(skip)
+            query = query.offset(skip)
 
         if limit:
-            stmt = stmt.limit(limit)
+            query = query.limit(limit)
 
         self._joint.extend(joint)
-        return stmt
+        return query
 
-    async def build_handler(
+    def build_handler(
         self,
-        db_session: AsyncSession,
-        joins=set(),
+        joins=None,
         order_by=None,
         skip: int = 0,
         limit: int = 20,
         distinct_fields=None,
         where=None,
         select_models=None,
         **kwargs
     ) -> Select:
         """
         Build a query handler with the given filters.
-        :param db_session: The async database session.
         :param kwargs: Filters for the query.
         :return: A query handler.
         """
-        cached_query = await self._build_query(
-            db_session, joins, skip=skip, limit=limit, order_by=order_by,
+        joins = joins or set()
+        cached_query = self._build_query(
+            joins, skip=skip, limit=limit, order_by=order_by,
             distinct_fields=distinct_fields, where=where,
             select_models=select_models, **kwargs
         )
         return cached_query
 
-    def is_relationship_field(self, model, field_name):
+    @staticmethod
+    def is_relationship_field(model, field_name):
         field = getattr(model, field_name)
         return isinstance(field.property, RelationshipProperty)
 
-    def is_m2m_relationship(self, model, field_name):
+    @staticmethod
+    def is_m2m_relationship(model, field_name):
         field = getattr(model, field_name)
         return (
             isinstance(field.property, RelationshipProperty)
             and field.property.secondary is not None
         )
 
-    def _apply_prefetch_related(self, db_session=None, stmt: Select = None):
+    def _apply_prefetch_related(self, query):
         for prefetch_joins in self._prefetch_related_joins:
             if len(prefetch_joins) == 2:
                 related_model, association_table = prefetch_joins
                 related_model_id, association_related_id = (
                     get_association_id_column(association_table, related_model)
                 )
                 self_model_id_column, association_self_id = (
                         get_association_id_column(association_table, self.cls)
                     )
 
                 if association_table not in self._joint:
-                    stmt = stmt.join(
+                    query = query.join(
                         association_table,
                         self_model_id_column == association_self_id
                     )
                     self._joint.append(association_table)
 
                 if related_model not in self._joint:
-                    stmt = stmt.join(
+                    query = query.join(
                         related_model,
                         related_model_id == association_related_id
                     )
                     self._joint.append(related_model)
 
             elif len(prefetch_joins) == 1:
-                stmt = stmt.join(prefetch_joins)
-        return stmt
+                query = query.join(prefetch_joins)
+        return query
 
-    async def apply_filter_type(
+    def apply_filter_type(
         self,
         filter_type: str,
         conditions: list,
         column,
         value,
     ) -> Select:
         conditions.append(self.condition_map.get(
             filter_type, lambda column, value: column == value)(column, value)
         )
         return conditions
 
-    def _apply_ordering(self, stmt, order_by: Union[str, Tuple[str]]) -> None:
+    def _apply_ordering(self, query, order_by: Union[str, Tuple[str]]) -> None:
         """
         Apply ordering to the SQL statement based on the given order_by parm.
 
-        :param stmt: The SQL statement to modify.
         :param order_by: A string or tuple of strings indicating orderby col.
         :return: None
         """
+        if order_by == "?":
+            return query.order_by(func.random())
+
         order_by = (order_by,) if isinstance(order_by, str) else order_by
         cols = [
             getattr(self.cls, col.lstrip("-")).desc() if col.startswith("-")
             else getattr(self.cls, col).asc() for col in order_by
         ]
-        stmt = stmt.order_by(*cols)
-        return stmt
+        query = query.order_by(*cols)
+        return query
 
-    def _apply_distinct(self, stmt, distinct_fields=None):
+    def _apply_distinct(self, query, distinct_fields=None):
         """
         Apply a DISTINCT clause to the SQL statement.
 
-        :param stmt: The SQL statement to modify.
         :return: None
         """
 
         if distinct_fields is not None:
             if isinstance(distinct_fields, (list, tuple)):
                 columns = [
                     getattr(self.cls, field) for field in distinct_fields
                 ]
-                stmt = stmt.distinct(*columns)
+                query = query.distinct(*columns)
             else:
                 raise ValueError(
                     "distinct_fields should be a list or tuple of field names."
                 )
-        return stmt
+        return query
```

### Comparing `fastapi-integration-0.0.7/fastapi_integration/orm/queries.py` & `fastapi-integration-0.1.0/fastapi_integration/orm/queries.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,73 +1,78 @@
+from typing import Type, Union, Tuple, Any, List
+
+
 from sqlalchemy import (
     select,
     delete as sqla_delete,
     update as sqla_update,
 )
 from sqlalchemy.ext.asyncio import AsyncSession
-from typing import Type, Union, Tuple, Any, List
 from sqlalchemy import func
 from sqlalchemy.orm import RelationshipProperty
+
+
 from .signals import SignalMixin
 from .base import BaseQuery
 
 
 class QueryMixin(BaseQuery, SignalMixin):
 
     async def get(
         self,
         db_session: AsyncSession,
-        joins=set(),
+        joins: set = None,
         order_by=None,
         **kwargs
     ) -> Union[Type[Any], Type["QueryMixin"]]:
-        stmt = await self.build_handler(
-            db_session,
+        self.query = self.build_handler(
             joins=joins,
             order_by=order_by,
             **kwargs
         )
-        result = await db_session.execute(stmt)
+        result = await db_session.execute(self.query)
         self.instance = result.scalars().first()
         return self.instance
 
-    async def filter(
+    def filter(
         self,
-        db_session: AsyncSession,
-        joins=set(),
+        joins: set = None,
         order_by=None,
         skip: int = 0,
-        values_fields: list = [],
+        values_fields: list = None,
         where=None,
+        select_models=None,
+        distinct_fields=None,
         **kwargs
     ) -> Union[Type[Any], Type["QueryMixin"]]:
-        stmt = await self.build_handler(
-            db_session, joins=joins, order_by=order_by, skip=skip, where=where,
+        self.query = self.build_handler(
+            joins=joins, order_by=order_by, skip=skip, where=where,
+            distinct_fields=distinct_fields, select_models=select_models,
             **kwargs
         )
+
         if values_fields:
-            stmt = stmt.with_only_columns(
+            self.query = self.query.with_only_columns(
                 *[getattr(self.cls, field) for field in values_fields]
             )
         if hasattr(self, "_prefetch_related_joins"):
-            stmt = self._apply_prefetch_related(db_session, stmt)
-        result = await db_session.execute(stmt)
-        if self.needs_scalar:
-            self.instance = result.scalars().all()
-        else:
-            self.instance = result.all()
-        return self.instance
+            self.query = self._apply_prefetch_related(self.query)
+        return self
 
-    async def count(self, db_session: AsyncSession, stmt) -> int:
-        stmt = stmt.with_only_columns(func.count(self.cls.id))
-        result = await db_session.execute(stmt)
+    async def count(self, db_session: AsyncSession) -> int:
+        modified_query = self.query.limit(None).offset(None)
+        subquery = modified_query.subquery()
+        count_stmt = select(func.count()).select_from(subquery)
+        result = await db_session.execute(count_stmt)
         return result.scalar()
 
     async def create(
-        self, db_session: AsyncSession, **kwargs
+        self,
+        db_session: AsyncSession,
+        **kwargs
     ) -> Union[Type[Any], Type["QueryMixin"]]:
         self.instance = self.cls()
         for key, value in kwargs.items():
             attr = getattr(self.cls, key, None)
 
             if attr is None:
                 raise ValueError(
@@ -78,90 +83,88 @@
                 attr.property, RelationshipProperty
             ):
                 related_instance = value
                 setattr(self.instance, key, related_instance)
             else:
                 setattr(self.instance, key, value)
 
-        # instance = await self._pre_save(db_session, instance, **kwargs)
+        # self.instance = await self._pre_save(db_session, instance, **kwargs)
         try:
             db_session.add(self.instance)
             await db_session.flush()
             await db_session.commit()
-        except Exception as e:
+        except Exception as error:
             await db_session.rollback()
-            raise e
+            raise error
         return self.instance
 
-    async def all(
+    def all(
         self,
-        db_session: AsyncSession,
-        joins=set(),
+        joins: set = None,
         order_by: str = None,
-        skip: int = 0,
     ) -> Union[Type[Any], Type["QueryMixin"]]:
-        return await self.filter(db_session, joins, order_by=order_by, skip=0)
+        self.filter(joins, order_by=order_by, skip=0)
+        return self
 
     async def delete(
         self,
         db_session: AsyncSession,
-        joins=set(),
+        joins: set = None,
         **kwargs
     ) -> int:
         """
         Delete instances matching the given filters.
         :param db_session: The async database session.
         :param kwargs: Filters for the instances to delete.
         :return: None
         """
-        stmt = await self.build_handler(
-            db_session=db_session, joins=joins, **kwargs
+        self.query = self.build_handler(
+            joins=joins, **kwargs
         )
-        stmt = await self._pre_delete(db_session, stmt, **kwargs)
-        delete_stmt = sqla_delete(self.cls).where(stmt.whereclause)
+        self.query = await self._pre_delete(db_session, self.query, **kwargs)
+        delete_stmt = sqla_delete(self.cls).where(self.query.whereclause)
         result = await db_session.execute(delete_stmt)
         await db_session.commit()
         return result.rowcount
 
     async def update(
         self,
         db_session: AsyncSession,
         data: dict,
-        joins=set(),
+        joins: set = None,
         **kwargs
     ) -> int:
         """
         Update instances matching the given filters with the given data.
 
         :param db_session: The async database session.
         :param update_data: A dictionary containing the data to update.
         :param kwargs: Filters for the instances to update.
         :return: None
         """
-        stmt = await self.build_handler(
-            db_session=db_session, joins=joins, **kwargs
-        )
-        stmt = await self._pre_update(db_session, stmt, **kwargs)
-        update_stmt = sqla_update(self.cls).where(stmt.whereclause).values(
-            data
+        self.query = self.build_handler(
+            joins=joins, **kwargs
         )
-        result = await db_session.execute(update_stmt)
+        self.query = await self._pre_update(db_session, self.query, **kwargs)
+        self.query = sqla_update(self.cls).where(
+            self.query.whereclause
+        ).values(data)
+        result = await db_session.execute(self.query)
         await db_session.commit()
         if result.rowcount == 1:
             updated_instance = await self.get(db_session, **kwargs)
             return updated_instance
-        else:
-            return result.rowcount or None
+        return result.rowcount
 
     async def aggregate(
         self,
         db_session: AsyncSession,
         field: str,
         agg_func: str = "sum",
-        joins=set(),
+        joins: set = None,
         **kwargs
     ) -> Union[int, float, None]:
         """
         Perform an aggregation on a column.
 
         :param db_session: The async database session.
         :param aggregation_fn: The aggregation function to use.
@@ -179,24 +182,26 @@
         if agg_func.lower() not in supported_agg_funcs:
             raise NotImplementedError(
                 f"Unsupported aggregation function '{agg_func}'"
             )
         aggregation = supported_agg_funcs[agg_func.lower()](
             getattr(self.cls, field)
         )
-        stmt = select(aggregation)
-        stmt = await self.build_handler(db_session, joins=joins, **kwargs)
-        stmt = stmt.select_from(self.cls).with_only_columns(aggregation)
-        result = await db_session.execute(stmt)
+        self.query = select(aggregation)
+        self.query = self.build_handler(joins=joins, **kwargs)
+        self.query = self.query.select_from(self.cls).with_only_columns(
+            aggregation
+        )
+        result = await db_session.execute(self.query)
         return result.scalar()
 
     async def exclude(
         self,
         db_session: AsyncSession,
-        joins=set(),
+        joins: set = None,
         order_by=None,
         skip: int = 0,
         **kwargs
     ) -> Union[Type[Any], Type["QueryMixin"]]:
         """
         Retrieve instances that do not match the given filters.
 
@@ -206,47 +211,50 @@
             to order by.
         :param skip: The number of instances to skip.
         :param get_count: If True, also return the count of instances.
         :param kwargs: Additional filters for the query.
         :return: A list of instances or a tuple containing the list of
             instances and the count.
         """
-        all_stmt = await self.build_handler(
+        all_stmt = self.build_handler(
             db_session=db_session, joins=joins, order_by=order_by, skip=skip
         )
         all_result = await db_session.execute(all_stmt)
         all_instances = all_result.scalars().all()
-        exclude_stmt = await self.build_handler(
+        exclude_stmt = self.build_handler(
             db_session=db_session, joins=joins, order_by=order_by, skip=skip,
             **kwargs
         )
         exclude_result = await db_session.execute(exclude_stmt)
         exclude_instances = exclude_result.scalars().all()
         self.instance = list(set(all_instances) - set(exclude_instances))
         return self.instance
 
-    async def add_m2m(self, db_session: AsyncSession, other_model) -> None:
+    async def add_m2m(
+            self, db_session: AsyncSession, other_models: list
+    ) -> None:
         """
         Add a many-to-many relationship between two entities.d
         :param db_session: The async database session.
-        :param other_model: The entity in the relationship.
+        :param other_models: The entity in the relationship as list.
         :return: None
         """
         if self.instance is None:
             raise ValueError("Perform a query before using add_m2m method")
-        for attr, value in self.instance.__class__.__dict__.items():
-            if isinstance(
-                value, RelationshipProperty
-            ) and value.argument == other_model.__class__.__name__:
-                getattr(self.instance, attr).append(other_model)
-        for attr, value in other_model.__class__.__dict__.items():
-            if isinstance(
-                value, RelationshipProperty
-            ) and value.argument == self.instance.__class__.__name__:
-                getattr(other_model, attr).append(self.instance)
+        for other_model in other_models:
+            for attr, value in self.instance.__class__.__dict__.items():
+                if isinstance(
+                    value, RelationshipProperty
+                ) and value.argument == other_model.__class__.__name__:
+                    getattr(self.instance, attr).append(other_model)
+            for attr, value in other_model.__class__.__dict__.items():
+                if isinstance(
+                    value, RelationshipProperty
+                ) and value.argument == self.instance.__class__.__name__:
+                    getattr(other_model, attr).append(self.instance)
 
         await db_session.commit()
 
     async def get_or_create(
         self, db_session: AsyncSession, create_data: dict, **kwargs
     ) -> Tuple[Union[Type[Any], Type["QueryMixin"]], bool]:
         """
@@ -277,17 +285,17 @@
         """
         instances = [self.cls(**data) for data in instances_data]
 
         try:
             db_session.add_all(instances)
             await db_session.flush()
             await db_session.commit()
-        except Exception as e:
+        except Exception as error:
             await db_session.rollback()
-            raise e
+            raise error
         return len(instances)
 
     async def select_related(self, session, *related_models):
         raise NotImplementedError("Not Implemented Yet")
 
     def prefetch_related(self, related_model: 'QueryMixin') -> 'QueryMixin':
         model_fields = [
@@ -325,34 +333,33 @@
         db_sesssion: AsyncSession,
         update_data: List[Tuple[dict, dict]]
     ) -> int:
         raise NotImplementedError("""
         sqlalchemy.exc.InvalidRequestError
         WHERE clause with bulk ORM UPDATE not supported right now
         """)
-        """
-        Perform a bulk update of instances based on given filters and update.
-
-        :param db_session: The async database session.
-        :param update_data: A list of tuples, where each tuple contains a
-            dictionary of filters and a dictionary of update data.
-        :return: The number of updated instances.
-        """
+        # """
+        # Perform a bulk update of instances based on given filters and update.
+        # :param db_session: The async database session.
+        # :param update_data: A list of tuples, where each tuple contains a
+        #     dictionary of filters and a dictionary of update data.
+        # :return: The number of updated instances.
+        # """
         # num_updated = 0
         # update_params = []
         # for idx, (filter_conditions, data) in enumerate(update_data):
         #     update_params.append(
         #         {
         #             **filter_conditions,
         #             **{f"{key}_{idx}": value for key, value in data.items()}
         #         }
         #     )
         # update_stmt = sqla_update(self.cls)
         # for idx, (filter_conditions, data) in enumerate(update_data):
-        #     condition_query = await self.build_handler(
+        #     condition_query = self.build_handler(
         #         db_session, **filter_conditions
         #     )
         #     update_stmt = update_stmt.where(condition_query)
         #     for key in data.keys():
         #         update_stmt = update_stmt.values(
         #             {getattr(self.cls, key): bindparam(f"{key}_{idx}")}
         #         )
```

### Comparing `fastapi-integration-0.0.7/fastapi_integration/orm/signals.py` & `fastapi-integration-0.1.0/fastapi_integration/orm/signals.py`

 * *Files 4% similar despite different names*

```diff
@@ -10,34 +10,31 @@
         self, db_session: AsyncSession, instance=None, **kwargs
     ):
         _instance = await self.pre_save(
             db_session, instance=instance, **kwargs
         )
         if _instance is not None:
             return _instance
-        else:
-            return instance
+        return instance
 
     async def _pre_update(
             self, db_session: AsyncSession, stmt=None, **kwargs
     ) -> TypedReturnsRows:
         _stmt = await self.pre_update(db_session, stmt=stmt, **kwargs)
         if _stmt is not None:
             return _stmt
-        else:
-            return stmt
+        return stmt
 
     async def _pre_delete(
             self, db_session: AsyncSession, stmt=None, **kwargs
     ) -> TypedReturnsRows:
         _stmt = await self.pre_delete(db_session, stmt=stmt, **kwargs)
         if _stmt is not None:
             return _stmt
-        else:
-            return stmt
+        return stmt
 
     async def pre_save(self, db_session: AsyncSession, **kwargs):
         pass
 
     async def pre_update(self, db_session: AsyncSession, stmt=None, **kwargs):
         pass
```

### Comparing `fastapi-integration-0.0.7/fastapi_integration/orm/utils.py` & `fastapi-integration-0.1.0/fastapi_integration/orm/utils.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,8 +1,10 @@
 from typing import Tuple
+
+
 from sqlalchemy import Column, ForeignKey
 
 
 def get_foreign_key(column: Column, model) -> ForeignKey:
     return next((
         fk for fk in column.foreign_keys if fk.column.table == model.__table__
     ), None)
```

### Comparing `fastapi-integration-0.0.7/fastapi_integration.egg-info/SOURCES.txt` & `fastapi-integration-0.1.0/fastapi_integration.egg-info/SOURCES.txt`

 * *Files 16% similar despite different names*

```diff
@@ -1,35 +1,41 @@
 README.md
 setup.py
+examples/__init__.py
+examples/admin.py
+examples/base.py
+examples/main.py
 fastapi_integration/__init__.py
 fastapi_integration/common.py
 fastapi_integration/config.py
 fastapi_integration/db.py
+fastapi_integration/dependencies.py
+fastapi_integration/exceptions.py
+fastapi_integration/features.py
 fastapi_integration/models.py
-fastapi_integration/schema.py
 fastapi_integration.egg-info/PKG-INFO
 fastapi_integration.egg-info/SOURCES.txt
 fastapi_integration.egg-info/dependency_links.txt
 fastapi_integration.egg-info/requires.txt
 fastapi_integration.egg-info/top_level.txt
 fastapi_integration/admin/__init__.py
+fastapi_integration/admin/generator.py
 fastapi_integration/auth/__init__.py
 fastapi_integration/auth/routers.py
 fastapi_integration/auth/schemas.py
-fastapi_integration/auth/security.py
 fastapi_integration/auth/utils.py
 fastapi_integration/generic/__init__.py
 fastapi_integration/generic/crud.py
 fastapi_integration/generic/views.py
 fastapi_integration/orm/__init__.py
 fastapi_integration/orm/base.py
 fastapi_integration/orm/models.py
 fastapi_integration/orm/queries.py
 fastapi_integration/orm/signals.py
 fastapi_integration/orm/transaction.py
 fastapi_integration/orm/utils.py
 fastapi_integration/utils/__init__.py
 tests/__init__.py
-tests/complex_query.py
-tests/query.py
-tests/resolve_path.py
-tests/start.py
+tests/base.py
+tests/query/__init__.py
+tests/query/test_complex.py
+tests/query/test_simple.py
```

### Comparing `fastapi-integration-0.0.7/tests/query.py` & `fastapi-integration-0.1.0/tests/query/test_simple.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,15 +1,18 @@
-import resolve_path
 import random
 import string
 import unittest
+
+
 from sqlalchemy.orm import declarative_base
-from fastapi_integration.db import Engine
+
+
+from tests.base import MyConfig
+from fastapi_integration.db import SqlEngine
 from fastapi_integration.models import AbstractBaseUser
-from tests.start import MyConfig
 
 
 def get_random_info():
     username = ''.join(random.choices(string.ascii_lowercase, k=8))
     domain = ''.join(random.choices(string.ascii_lowercase, k=8))
     email = username + "@" + domain + ".com"
     icontain_email = username[:-3] + "@" + domain + ".com"
@@ -24,16 +27,24 @@
 
     async def asyncTearDown(self):
         await db_engine.drop_database(Base)
         async with db_engine.engine.connect() as conn:
             await conn.close()
             await db_engine.engine.dispose()
 
+    async def test_lazy_obj(self):
+        obj1 = User.objects
+        obj2 = User.objects
+        obj1.id = "lazy"
+        obj2.id = "lazy2"
+        self.assertEqual(obj1.id, "lazy")
+        self.assertEqual(obj2.id, "lazy2")
+
     async def test_filter_update_delete_all(self):
-        async with db_engine.get_pg_db_with_async() as session:
+        async with db_engine.connection_context_manager() as session:
             await User.objects.create(
                 email=self.random_info[1],
                 username=self.random_info[0],
                 password="testpassword",
                 db_session=session
             )
             await User.objects.create(
@@ -44,25 +55,27 @@
             )
             await User.objects.update(
                 session,
                 email=self.random_info[1],
                 data={"username": "NewUser"}
             )
             res = await User.objects.get(session, username="NewUser")
-            self.all_query = await User.objects.all(db_session=session)
+            self.all_query = await User.objects.all().execute(
+                db_session=session
+            )
             self.delete = await User.objects.delete(
                 email=self.random_info[1], db_session=session
             )
 
         self.assertEqual(res.username, "NewUser")
         self.assertEqual(self.delete, 1)
         self.assertGreater(len(self.all_query), 1)
 
     async def test_user_field_looksup(self):
-        async with db_engine.get_pg_db_with_async() as session:
+        async with db_engine.connection_context_manager() as session:
             new_email = str(self.random_info[1]).join(random.choices(
                 string.ascii_lowercase, k=2)
             )
             new_username = str(self.random_info[2]).join(random.choices(
                 string.ascii_lowercase, k=2)
             )
             await User.objects.create(
@@ -70,40 +83,37 @@
                 password="testpassword", db_session=session
             )
             await User.objects.create(
                 email=new_email, username=new_username,
                 password="testpassword", db_session=session
             )
             self.filter_gte = await User.objects.filter(
-                id__gte=1, db_session=session
-            )
+                id__gte=1
+            ).execute(db_session=session, )
             self.filter_lte = await User.objects.filter(
-                id__lte=0, db_session=session
-            )
+                id__lte=0
+            ).execute(db_session=session, )
             self.filter_icontain = await User.objects.filter(
-                email__icontains=self.random_info[2][:2],
-                db_session=session
-            )
+                email__icontains=self.random_info[2][:2]
+            ).execute(db_session=session)
             self.startswith = await User.objects.filter(
-                username__startswith=self.random_info[1][:3],
-                db_session=session
-            )
+                username__startswith=self.random_info[1][:3]
+            ).execute(db_session=session)
             self.istartswith = await User.objects.filter(
                 username__istartswith=self.random_info[1][:3].upper(),
-                db_session=session
-            )
+            ).execute(db_session=session)
 
         self.assertEqual(len(self.filter_icontain), 2)
         self.assertGreater(len(self.filter_gte), 0)
         self.assertEqual(len(self.filter_lte), 0)
         self.assertEqual(len(self.startswith), 1)
         self.assertEqual(len(self.istartswith), 1)
 
     async def test_user_exclude(self):
-        async with db_engine.get_pg_db_with_async() as session:
+        async with db_engine.connection_context_manager() as session:
             await User.objects.create(
                 email=self.random_info[1],
                 username=self.random_info[0],
                 password="testpassword",
                 db_session=session
             )
             await User.objects.create(
@@ -121,15 +131,15 @@
                 email="",
                 db_session=session
             )
         self.assertGreater(len(self.multiple_exclude_lte), 0)
         self.assertEqual(len(self.exclude_lte), 0)
 
     async def test_query_order_limit(self):
-        async with db_engine.get_pg_db_with_async() as session:
+        async with db_engine.connection_context_manager() as session:
             new_email = str(self.random_info[1]).join(
                 random.choices(string.ascii_lowercase, k=2)
             )
             new_username = str(self.random_info[2]).join(
                 random.choices(string.ascii_lowercase, k=2)
             )
             await User.objects.create(
@@ -141,45 +151,41 @@
             await User.objects.create(
                 email=new_email,
                 username=new_username,
                 password="testpassword",
                 db_session=session
             )
             limit_query = await User.objects.filter(
-                db_session=session,
                 order_by="-id",
                 limit=1
-            )
+            ).execute(db_session=session)
             order_query = await User.objects.filter(
-                db_session=session,
                 order_by="-id",
                 limit=2
-            )
+            ).execute(db_session=session)
 
         self.assertEqual(len(limit_query), 1)
         self.assertGreater(order_query[0].id, order_query[1].id)
 
     async def test_values(self):
-        async with db_engine.get_pg_db_with_async() as session:
+        async with db_engine.connection_context_manager() as session:
             await User.objects.create(
                 email=self.random_info[1],
                 username=self.random_info[0],
                 password="testpassword",
                 db_session=session
             )
             value_query = await User.objects.filter(
                 email=self.random_info[1],
-                db_session=session,
                 values_fields=["username", "id"]
-            )
+            ).execute(db_session=session)
         self.assertEqual(hasattr(value_query[0], 'password'), False)
 
 
 if __name__ == "__main__":
-    resolve_path
     Base = declarative_base()
 
     class User(AbstractBaseUser, Base):
         __tablename__ = "users"
 
-    db_engine = Engine(MyConfig())
+    db_engine = SqlEngine(MyConfig())
     unittest.main()
```

