# Comparing `tmp/wiretap_sqlserver-2.1.0-py3-none-any.whl.zip` & `tmp/wiretap_sqlserver-4.2.0-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 2918 bytes, number of entries: 7
+Zip file size: 2985 bytes, number of entries: 7
 -rw-rw-rw-  2.0 fat        0 b- defN 23-Jan-27 19:36 __init__.py
 -rw-rw-rw-  2.0 fat       96 b- defN 23-Jan-27 19:49 wiretap_sqlserver/__init__.py
--rw-rw-rw-  2.0 fat     3159 b- defN 23-Feb-15 17:33 wiretap_sqlserver/sqlserverhandler.py
--rw-rw-rw-  2.0 fat      189 b- defN 23-Feb-16 11:12 wiretap_sqlserver-2.1.0.dist-info/METADATA
--rw-rw-rw-  2.0 fat       92 b- defN 23-Feb-16 11:12 wiretap_sqlserver-2.1.0.dist-info/WHEEL
--rw-rw-rw-  2.0 fat       27 b- defN 23-Feb-16 11:12 wiretap_sqlserver-2.1.0.dist-info/top_level.txt
-?rw-rw-r--  2.0 fat      580 b- defN 23-Feb-16 11:12 wiretap_sqlserver-2.1.0.dist-info/RECORD
-7 files, 4143 bytes uncompressed, 1874 bytes compressed:  54.8%
+-rw-rw-rw-  2.0 fat     3446 b- defN 23-May-13 16:15 wiretap_sqlserver/sqlserverhandler.py
+-rw-rw-rw-  2.0 fat      189 b- defN 23-May-13 16:16 wiretap_sqlserver-4.2.0.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 23-May-13 16:16 wiretap_sqlserver-4.2.0.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat       27 b- defN 23-May-13 16:16 wiretap_sqlserver-4.2.0.dist-info/top_level.txt
+-rw-rw-r--  2.0 fat      580 b- defN 23-May-13 16:16 wiretap_sqlserver-4.2.0.dist-info/RECORD
+7 files, 4430 bytes uncompressed, 1941 bytes compressed:  56.2%
```

## zipnote {}

```diff
@@ -3,20 +3,20 @@
 
 Filename: wiretap_sqlserver/__init__.py
 Comment: 
 
 Filename: wiretap_sqlserver/sqlserverhandler.py
 Comment: 
 
-Filename: wiretap_sqlserver-2.1.0.dist-info/METADATA
+Filename: wiretap_sqlserver-4.2.0.dist-info/METADATA
 Comment: 
 
-Filename: wiretap_sqlserver-2.1.0.dist-info/WHEEL
+Filename: wiretap_sqlserver-4.2.0.dist-info/WHEEL
 Comment: 
 
-Filename: wiretap_sqlserver-2.1.0.dist-info/top_level.txt
+Filename: wiretap_sqlserver-4.2.0.dist-info/top_level.txt
 Comment: 
 
-Filename: wiretap_sqlserver-2.1.0.dist-info/RECORD
+Filename: wiretap_sqlserver-4.2.0.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## wiretap_sqlserver/sqlserverhandler.py

```diff
@@ -1,98 +1,106 @@
+import atexit
 import logging
 import sys
 import uuid
-import os
-import pyodbc
-import json
-import atexit
-from datetime import datetime, date, timezone
+from datetime import datetime, timezone
 from logging import Handler
-from typing import Callable, Any, List, Optional, Dict, Protocol, runtime_checkable
+from typing import Any, Dict, Protocol, runtime_checkable, cast
+
+import sqlalchemy  # type: ignore
 
 DEFAULT_INSERT = """
 INSERT INTO wiretap_log(
-    [instance],
     [parent], 
     [node], 
     [timestamp], 
     [scope], 
     [status], 
     [level], 
     [elapsed], 
+    [message],
     [details],
     [attachment]
-) VALUES (?, ?, ?, ?, ?, ?, ?, ?, ?, ?)
+) VALUES (
+    :parent, 
+    :node, 
+    :timestamp, 
+    :scope, 
+    :status, 
+    :level, 
+    :elapsed, 
+    :message,
+    :details, 
+    :attachment
+)
 """
 
 
 @runtime_checkable
-class _WiretapRecord(Protocol):
-    exc_text: str | None
-    created: float
-    module: str
-    funcName: str
-    values: List[Any]
+class _LogRecordExt(Protocol):
     parent: uuid.UUID | None
     node: uuid.UUID
-    levelname: str
     status: str
     elapsed: float
     details: str | None
     attachment: str | None
 
 
 class SqlServerHandler(Handler):
 
-    def __init__(self, connection_string: str, insert: str):
+    def __init__(self, connection_string: str, insert: str = DEFAULT_INSERT):
         super().__init__()
-        self.connection_string = connection_string
-        self.insert = insert
-        self.db: Optional[pyodbc.Cursor] = None
+        connection_url = sqlalchemy.engine.URL.create("mssql+pyodbc", query={"odbc_connect": connection_string})
+        self.engine = sqlalchemy.create_engine(connection_url)
+        self.insert = sqlalchemy.sql.text(insert)
+
         atexit.register(self._cleanup)
 
-    def emit(self, record: _WiretapRecord):
-        # There's no 'status' or other fields when using the default interface.
-        if not hasattr(record, "status"):
-            return
-
-        self.formatter.format(record)
-
-        args = [
-            record.parent.__str__() if record.parent else None,  # parent
-            record.node.__str__(),  # node
-            # record.instance,  # instance
-            datetime.fromtimestamp(record.created, tz=timezone.utc),  # timestamp
-            ".".join(n for n in [record.module, record.funcName] if n is not None),  # scope
-            record.status.lower(),  # status
-            record.levelname,  # level
-            record.elapsed,  # elapsed
-            record.details,  # details
-            record.exc_text or record.attachment  # attachment
-        ]
+    def emit(self, record: logging.LogRecord):
+        is_ext = hasattr(record, "status")
 
-        args = record.values + args
+        params = {
+            "timestamp": datetime.fromtimestamp(record.created, tz=timezone.utc),
+            "scope": ".".join(n for n in [record.module, record.funcName] if n is not None),
+            "level": record.levelname,
+            "message": record.message if hasattr(record, "message") and record.message != str(None) else None,
+        }
+
+        recext = cast(_LogRecordExt, record)
+        params = params | (self.formatter.values or {} if hasattr(self.formatter, "values") else {})
+
+        if is_ext:
+            params = params | {
+                "parent": recext.parent.__str__() if recext.parent else None,
+                "node": recext.node.__str__(),
+                "status": recext.status.lower(),
+                "elapsed": recext.elapsed,
+                "details": recext.details,
+                "attachment": recext.attachment
+            }
+        else:
+            params = params | {
+                "parent": None,
+                "node": None,
+                "status": None,
+                "elapsed": None,
+                "details": None,
+                "attachment": None
+            }
 
         try:
-            self._connect()
-            self.db.execute(self.insert, *args)
-            self.db.commit()
-        except:
+            with self.engine.connect() as c:
+                c.execute(self.insert, **params)
+        except:  # noqa
             # Disable this handler if an error occurs.
             self.setLevel(sys.maxsize)
             logging.exception(msg=f"Handler '{self.name}' could not log and has been disabled.", exc_info=True)
 
-    def _connect(self):
-        if not self.db:
-            connection = pyodbc.connect(self.connection_string)
-            self.db = connection.cursor()
-
     def _cleanup(self):
-        if self.db:
-            self.db.connection.close()
+        self.engine.dispose(close=True)
 
 
 class SqlServerOdbcConnectionString:
 
     @staticmethod
     def standard(server: str, database: str, username: str, password: str, driver_version: str = "17") -> str:
         return f"DRIVER={{ODBC Driver {driver_version} for SQL Server}};SERVER={server};DATABASE={database};UID={username};PWD={password}"
```

## Comparing `wiretap_sqlserver-2.1.0.dist-info/RECORD` & `wiretap_sqlserver-4.2.0.dist-info/RECORD`

 * *Files 16% similar despite different names*

```diff
@@ -1,7 +1,7 @@
 __init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 wiretap_sqlserver/__init__.py,sha256=nqZUltBgZ_SflgaKeWApt-luGYUdKWlcrpvPtVwIzP4,96
-wiretap_sqlserver/sqlserverhandler.py,sha256=vCxOPSf7BWbvVXhzNPk_HktoPUGw2LiFkGLKqb27pAA,3159
-wiretap_sqlserver-2.1.0.dist-info/METADATA,sha256=TbkkK0l_1UhUHAOSBuJNXQHYjfvmmcpreYaBWwdl6iI,189
-wiretap_sqlserver-2.1.0.dist-info/WHEEL,sha256=2wepM1nk4DS4eFpYrW1TTqPcoGNfHhhO_i5m4cOimbo,92
-wiretap_sqlserver-2.1.0.dist-info/top_level.txt,sha256=ulA0TtAkY_FcwFu1cRdD0O4EblYR4uY30Y7sTpw7cVI,27
-wiretap_sqlserver-2.1.0.dist-info/RECORD,,
+wiretap_sqlserver/sqlserverhandler.py,sha256=m1qRwyrEiaUHBkRZQqHCB1ZrMS9bjEZ_4_rIeB1niYA,3446
+wiretap_sqlserver-4.2.0.dist-info/METADATA,sha256=WupoCUc0tRMLd-SRPaYQ0-5GUjQMuBZ9rholtqJ97s0,189
+wiretap_sqlserver-4.2.0.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
+wiretap_sqlserver-4.2.0.dist-info/top_level.txt,sha256=ulA0TtAkY_FcwFu1cRdD0O4EblYR4uY30Y7sTpw7cVI,27
+wiretap_sqlserver-4.2.0.dist-info/RECORD,,
```

