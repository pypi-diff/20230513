# Comparing `tmp/pydantic_db_backend-0.1.0.tar.gz` & `tmp/pydantic_db_backend-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pydantic_db_backend-0.1.0.tar", max compression
+gzip compressed data, was "pydantic_db_backend-0.2.0.tar", max compression
```

## Comparing `pydantic_db_backend-0.1.0.tar` & `pydantic_db_backend-0.2.0.tar`

### file list

```diff
@@ -1,7 +1,9 @@
--rw-r--r--   0        0        0        0 2023-05-11 08:45:05.171805 pydantic_db_backend-0.1.0/README.md
--rw-r--r--   0        0        0        0 2023-05-11 08:45:17.171212 pydantic_db_backend-0.1.0/pydantic_db_backend/__init__.py
--rw-r--r--   0        0        0     2954 2023-05-11 08:54:38.634782 pydantic_db_backend-0.1.0/pydantic_db_backend/backend.py
--rw-r--r--   0        0        0     2875 2023-05-11 08:54:38.630782 pydantic_db_backend-0.1.0/pydantic_db_backend/couchdb_backend.py
--rw-r--r--   0        0        0       92 2023-05-11 09:09:54.582757 pydantic_db_backend-0.1.0/pydantic_db_backend/json_files_backend.py
--rw-r--r--   0        0        0      651 2023-05-11 08:54:48.750504 pydantic_db_backend-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      467 1970-01-01 00:00:00.000000 pydantic_db_backend-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-05-11 08:45:05.171805 pydantic_db_backend-0.2.0/README.md
+-rw-r--r--   0        0        0        0 2023-05-11 08:45:17.171212 pydantic_db_backend-0.2.0/pydantic_db_backend/__init__.py
+-rw-r--r--   0        0        0     2550 2023-05-13 10:51:56.578404 pydantic_db_backend-0.2.0/pydantic_db_backend/backend.py
+-rw-r--r--   0        0        0        0 2023-05-13 10:06:57.338481 pydantic_db_backend-0.2.0/pydantic_db_backend/backends/__init__.py
+-rw-r--r--   0        0        0     2943 2023-05-13 10:05:18.402714 pydantic_db_backend-0.2.0/pydantic_db_backend/backends/couchdb.py
+-rw-r--r--   0        0        0       92 2023-05-11 09:09:54.582757 pydantic_db_backend-0.2.0/pydantic_db_backend/backends/json_files.py
+-rw-r--r--   0        0        0      566 2023-05-13 10:05:53.046645 pydantic_db_backend-0.2.0/pydantic_db_backend/utils.py
+-rw-r--r--   0        0        0      724 2023-05-13 10:55:06.803914 pydantic_db_backend-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0      548 1970-01-01 00:00:00.000000 pydantic_db_backend-0.2.0/PKG-INFO
```

### Comparing `pydantic_db_backend-0.1.0/pydantic_db_backend/backend.py` & `pydantic_db_backend-0.2.0/pydantic_db_backend/backend.py`

 * *Files 18% similar despite different names*

```diff
@@ -2,46 +2,28 @@
 
 import contextlib
 import datetime
 import json
 import re
 from contextvars import ContextVar
 from typing import Type, Dict
-from uuid import uuid4
 
 from dotenv import load_dotenv
 import logging
 
-from iso8601 import iso8601, ParseError
 from pydantic import BaseModel, Field
 
+from pydantic_db_backend.utils import uid, utcnow, str_to_datetime_if_parseable
+
 log = logging.getLogger(__name__)
 
 backend_context_var = ContextVar('backend_context_var')
 backend_alias_context_var = ContextVar('backend_alias_context_var', default='default')
 
 
-def uid():
-    return str(uuid4()).replace("-", "")
-
-
-def utcnow():
-    return datetime.datetime.utcnow().replace(tzinfo=datetime.timezone.utc)
-
-
-def str_to_datetime_if_parseable(value: str) -> datetime.datetime | str:
-    if len(value) < 8 or value.count('-') != 2:
-        return value
-    try:
-        ret = iso8601.parse_date(value)
-    except (ParseError, ValueError, TypeError):
-        ret = value
-    return ret
-
-
 class BackendModel(BaseModel):
     uid: str | None = Field(default_factory=uid)
     created_time: datetime.datetime | None = Field(default_factory=utcnow)
     updated_time: datetime.datetime | None = Field(default_factory=utcnow)
 
     class Config:
         json_encoders = {
```

### Comparing `pydantic_db_backend-0.1.0/pydantic_db_backend/couchdb_backend.py` & `pydantic_db_backend-0.2.0/pydantic_db_backend/backends/couchdb.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,14 +3,16 @@
 import os
 import sys
 from typing import Dict, Type
 
 import pydash
 from pip._internal.metadata import Backend
 
+import pydantic_db_backend.utils
+
 
 class CouchDbBackend(Backend):
     _collections: Dict[Type[BaseModel], str] = {}
     _connections: Dict[str, CouchDbConnectionModel] = {}
 
     @classmethod
     def startup(cls, alias: str | None = "default", uri: str | None = None):
@@ -67,16 +69,16 @@
     def post_instance(cls, instance: BackendModel) -> BackendModel:
         document = cls.to_db(instance)
         return cls.post_document(instance.__class__, document)
 
     @classmethod
     def put_instance(cls, instance: BackendModel) -> BackendModel:
         db = cls.get_db(db_name=cls.collection_name(instance.__class__))
-        if instance.uid in db:
-            record = db[instance.uid]
+        if pydantic_db_backend.utils.uid in db:
+            record = db[pydantic_db_backend.utils.uid]
             record.update(cls.to_db(instance))
             db.save(record)
         else:
             return cls.post_instance(instance)
 
 
 class CouchDbConnectionModel(BaseModel):
```

### Comparing `pydantic_db_backend-0.1.0/pyproject.toml` & `pydantic_db_backend-0.2.0/pyproject.toml`

 * *Files 26% similar despite different names*

```diff
@@ -1,26 +1,29 @@
 [tool.poetry]
 name = "pydantic-db-backend"
-version = "0.1.0"
+version = "0.2.0"
 description = ""
 authors = ["Marco Bartel <bsimpson888@gmail.com>"]
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.11"
 python-dotenv = "^1.0.0"
-# couchdb = "^1.2"
+couchdb = { version = "^1.2", optional = true }
 pydash = "^7.0.3"
 iso8601 = "^1.1.0"
 pydantic = "^1.10.7"
 
 
 [tool.poetry.group.dev.dependencies]
 pytest = "^7.3.1"
 
+[tool.poetry.extras]
+couchdb = ["couchdb"]
+
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.pytest.ini_options]
 minversion = "6.0"
 addopts = "-ra -q -s -v"
```

