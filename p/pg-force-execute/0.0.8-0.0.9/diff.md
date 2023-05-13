# Comparing `tmp/pg_force_execute-0.0.8.tar.gz` & `tmp/pg_force_execute-0.0.9.tar.gz`

## Comparing `pg_force_execute-0.0.8.tar` & `pg_force_execute-0.0.9.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0     2835 2020-02-02 00:00:00.000000 pg_force_execute-0.0.8/pg_force_execute.py
--rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 pg_force_execute-0.0.8/.gitignore
--rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 pg_force_execute-0.0.8/LICENSE
--rw-r--r--   0        0        0     2276 2020-02-02 00:00:00.000000 pg_force_execute-0.0.8/README.md
--rw-r--r--   0        0        0      813 2020-02-02 00:00:00.000000 pg_force_execute-0.0.8/pyproject.toml
--rw-r--r--   0        0        0     2976 2020-02-02 00:00:00.000000 pg_force_execute-0.0.8/PKG-INFO
+-rw-r--r--   0        0        0     2835 2020-02-02 00:00:00.000000 pg_force_execute-0.0.9/pg_force_execute.py
+-rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 pg_force_execute-0.0.9/.gitignore
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 pg_force_execute-0.0.9/LICENSE
+-rw-r--r--   0        0        0     2534 2020-02-02 00:00:00.000000 pg_force_execute-0.0.9/README.md
+-rw-r--r--   0        0        0     1092 2020-02-02 00:00:00.000000 pg_force_execute-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0     3864 2020-02-02 00:00:00.000000 pg_force_execute-0.0.9/PKG-INFO
```

### Comparing `pg_force_execute-0.0.8/pg_force_execute.py` & `pg_force_execute-0.0.9/pg_force_execute.py`

 * *Files identical despite different names*

### Comparing `pg_force_execute-0.0.8/.gitignore` & `pg_force_execute-0.0.9/.gitignore`

 * *Files identical despite different names*

### Comparing `pg_force_execute-0.0.8/LICENSE` & `pg_force_execute-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `pg_force_execute-0.0.8/README.md` & `pg_force_execute-0.0.9/README.md`

 * *Files 16% similar despite different names*

```diff
@@ -33,14 +33,22 @@
         ):
 
     results = conn.execute(sa.text(query))
     print(results.fetchall())
 ```
 
 
+## Compatibility
+
+- Python >= 3.7.1 (tested on 3.7.1, 3.8.0, 3.9.0, 3.10.0, and 3.11.0)
+- psycopg2 >= 2.9.2 or Psycopg 3 >= 3.1.4
+- SQLAlchemy >= 1.4.0 (tested on 1.4.0 and 2.0.0)
+- PostgreSQL >= 9.6 (tested on 9.6, 10.0, 11.0, 12.0, 13.0, 14.0, and 15.0)
+
+
 ## API
 
 The API a single context manager `pg_force_execute`.
 
 `pg_force_execute`(conn, engine, delay=datetime.timedelta(minutes=5), check_interval=datetime.timedelta(seconds=1), termination_thread_timeout=datetime.timedelta(seconds=10), logger=logging.getLogger("pg_force_execute"))
 
 - `conn` - A [SQLAlchemy connection](https://docs.sqlalchemy.org/en/20/core/connections.html#sqlalchemy.engine.Connection) that will be unblocked
```

### Comparing `pg_force_execute-0.0.8/pyproject.toml` & `pg_force_execute-0.0.9/pyproject.toml`

 * *Files 26% similar despite different names*

```diff
@@ -1,34 +1,50 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "pg-force-execute"
-version = "0.0.8"
+version = "0.0.9"
 authors = [
   { name="Department for International Trade", email="sre@digital.trade.gov.uk" },
 ]
 description = "Context manager to run PostgreSQL queries with SQLAlchemy, terminating any other clients that block them"
 readme = "README.md"
-requires-python = ">=3.7"
+requires-python = ">=3.7.1"
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 dependencies = [
-    "sqlalchemy>=1.4.40",
+    "sqlalchemy>=1.4.0",
 ]
 
 [project.optional-dependencies]
 dev = [
-    "psycopg[binary]>=3.1.9",
+    "psycopg>=3.1.4",
+    "psycopg2>=2.9.2",
     "pytest>=7.2.1",
 ]
+ci = [
+    "pytest==7.2.1",
+]
+ci-psycopg2-sqlalchemy1 = [
+    "psycopg2==2.9.2",
+    "sqlalchemy==1.4.0",
+]
+ci-psycopg2-sqlalchemy2 = [
+    "psycopg2==2.9.2",
+    "sqlalchemy==2.0.0",
+]
+ci-psycopg3-sqlalchemy2 = [
+    "psycopg==3.1.4",
+    "sqlalchemy==2.0.0",
+]
 
 [project.urls]
 "Source" = "https://github.com/uktrade/pg-force-execute"
 
 [tool.hatch.build]
 include = [
   "pg_force_execute.py"
```

