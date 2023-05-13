# Comparing `tmp/users_db-0.0.8.tar.gz` & `tmp/users_db-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "users_db-0.0.8.tar", max compression
+gzip compressed data, was "users_db-0.0.9.tar", max compression
```

## Comparing `users_db-0.0.8.tar` & `users_db-0.0.9.tar`

### file list

```diff
@@ -1,18 +1,19 @@
--rw-r--r--   0        0        0       10 2023-03-03 20:07:13.436325 users_db-0.0.8/README.md
--rw-r--r--   0        0        0      741 2023-03-27 23:09:58.548699 users_db-0.0.8/pyproject.toml
--rw-r--r--   0        0        0        0 2023-03-03 09:35:50.245218 users_db-0.0.8/users_db/__init__.py
--rw-r--r--   0        0        0     3090 2023-03-04 23:18:42.458330 users_db-0.0.8/users_db/alembic.ini
--rw-r--r--   0        0        0     1680 2023-03-27 20:42:36.222846 users_db-0.0.8/users_db/commands.py
--rw-r--r--   0        0        0      464 2023-03-15 22:26:17.885908 users_db-0.0.8/users_db/config.py
--rw-r--r--   0        0        0     1404 2023-03-07 20:58:40.204599 users_db-0.0.8/users_db/db.py
--rw-r--r--   0        0        0       38 2023-02-26 19:47:51.265164 users_db-0.0.8/users_db/migrations/README
--rw-r--r--   0        0        0     1268 2023-03-27 21:30:14.297708 users_db-0.0.8/users_db/migrations/README.md
--rw-r--r--   0        0        0      585 2023-03-27 23:07:36.548958 users_db-0.0.8/users_db/migrations/__init__.py
--rw-r--r--   0        0        0     2027 2023-02-28 12:47:13.470860 users_db-0.0.8/users_db/migrations/env.py
--rw-r--r--   0        0        0      510 2023-02-26 19:47:51.261835 users_db-0.0.8/users_db/migrations/script.py.mako
--rw-r--r--   0        0        0     1509 2023-03-27 23:07:27.649806 users_db-0.0.8/users_db/migrations/versions/7e479e30b57f_add_roles_enum_and_role_permission_table.py
--rw-r--r--   0        0        0     1375 2023-03-27 23:01:16.229381 users_db-0.0.8/users_db/migrations/versions/f102a531f12e_.py
--rw-r--r--   0        0        0      905 2023-03-27 22:45:13.595732 users_db-0.0.8/users_db/migrations/versions/f46112e923d8_.py
--rw-r--r--   0        0        0      738 2023-03-27 22:58:28.051263 users_db-0.0.8/users_db/schema.py
--rw-r--r--   0        0        0     1580 2023-03-20 15:21:05.620890 users_db-0.0.8/users_db/users.py
--rw-r--r--   0        0        0      662 1970-01-01 00:00:00.000000 users_db-0.0.8/PKG-INFO
+-rw-r--r--   0        0        0       10 2023-03-03 20:07:13.436325 users_db-0.0.9/README.md
+-rw-r--r--   0        0        0      763 2023-03-28 16:51:12.478237 users_db-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-03-03 09:35:50.245218 users_db-0.0.9/users_db/__init__.py
+-rw-r--r--   0        0        0     3090 2023-03-04 23:18:42.458330 users_db-0.0.9/users_db/alembic.ini
+-rw-r--r--   0        0        0     1680 2023-03-27 20:42:36.222846 users_db-0.0.9/users_db/commands.py
+-rw-r--r--   0        0        0      464 2023-03-15 22:26:17.885908 users_db-0.0.9/users_db/config.py
+-rw-r--r--   0        0        0     2290 2023-03-28 16:41:48.172046 users_db-0.0.9/users_db/db.py
+-rw-r--r--   0        0        0       38 2023-02-26 19:47:51.265164 users_db-0.0.9/users_db/migrations/README
+-rw-r--r--   0        0        0     1276 2023-03-28 15:03:04.177790 users_db-0.0.9/users_db/migrations/README.md
+-rw-r--r--   0        0        0      585 2023-03-27 23:07:36.548958 users_db-0.0.9/users_db/migrations/__init__.py
+-rw-r--r--   0        0        0     2027 2023-02-28 12:47:13.470860 users_db-0.0.9/users_db/migrations/env.py
+-rw-r--r--   0        0        0      510 2023-02-26 19:47:51.261835 users_db-0.0.9/users_db/migrations/script.py.mako
+-rw-r--r--   0        0        0      946 2023-03-28 15:02:52.518068 users_db-0.0.9/users_db/migrations/versions/3eb311d1aec7_add_password_and_email_columns_to_users_.py
+-rw-r--r--   0        0        0     1509 2023-03-27 23:07:27.649806 users_db-0.0.9/users_db/migrations/versions/7e479e30b57f_add_roles_enum_and_role_permission_table.py
+-rw-r--r--   0        0        0     1375 2023-03-27 23:01:16.229381 users_db-0.0.9/users_db/migrations/versions/f102a531f12e_.py
+-rw-r--r--   0        0        0      905 2023-03-27 22:45:13.595732 users_db-0.0.9/users_db/migrations/versions/f46112e923d8_.py
+-rw-r--r--   0        0        0      853 2023-03-28 15:00:57.976503 users_db-0.0.9/users_db/schema.py
+-rw-r--r--   0        0        0     1871 2023-03-28 16:21:19.916306 users_db-0.0.9/users_db/users.py
+-rw-r--r--   0        0        0      705 1970-01-01 00:00:00.000000 users_db-0.0.9/PKG-INFO
```

### Comparing `users_db-0.0.8/pyproject.toml` & `users_db-0.0.9/pyproject.toml`

 * *Files 21% similar despite different names*

```diff
@@ -1,24 +1,25 @@
 [tool.poetry]
 name = "users-db"
-version = "0.0.8"
+version = "0.0.9"
 description = "user_db is a database package for user CRUD operations"
 authors = ["Bohdan Stratila <bogdanstratila@icloud.com>"]
 readme = "README.md"
 packages = [{include = "users_db"}]
 
 [tool.poetry.dependencies]
 python = "^3.10"
 sqlalchemy = "^2.0.4"
 alembic = "1.9.4"
 pytest = "7.2.1"
 black = "23.1.0"
 flake8 = "6.0.0"
 psycopg2-binary = "2.9.5"
 click = "^8.1.3"
+pytest-cov = "^4.0.0"
 
 [tool.poetry.scripts]
 alembic_upgrade = 'users_db.commands:db_upgrade_cmd'
 alembic_downgrade = 'users_db.commands:db_downgrade_cmd'
 alembic_current= 'users_db.commands:db_current_cmd'
 alembic_revision = 'users_db.commands:db_revision_cmd'
```

### Comparing `users_db-0.0.8/users_db/alembic.ini` & `users_db-0.0.9/users_db/alembic.ini`

 * *Files identical despite different names*

### Comparing `users_db-0.0.8/users_db/commands.py` & `users_db-0.0.9/users_db/commands.py`

 * *Files identical despite different names*

### Comparing `users_db-0.0.8/users_db/migrations/README.md` & `users_db-0.0.9/users_db/migrations/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -2,13 +2,13 @@
 
 1. We wrap alembic commands into functions in `migrations/__init__.py`. This functions are imported by the `commands.py` file in the users_db module. 
 
 2. This `commands.py` file wraps the functions defined in the `alembic/__init__.py` file, providing command   line interface to this functions using Click library. Also, these commands always knows where the working directory with `alembic.ini` file is. We install this commands as Poetry scripts, so we can run them from the command line and don't worry about `alembic.ini` file location.
 
 3. If `commands.py` doesn't have the command you need, you'll have to add it in `migrations/__init__.py`, then define click command in `commands.py` and finally install it as a Poetry script
 
-4. In oder to create the migration, first you need to start containers `docker compose up -d`, make changes in the schema.py by defining the new models or changing the existing ones, and then run `docker compose exec alembic_revision --autogenerate -m "migration message"`.
+4. In oder to create the migration, first you need to start containers `docker compose up -d`, make changes in the schema.py by defining the new models or changing the existing ones, and then run `docker compose exec db alembic_revision --autogenerate=True -m "migration message"`.
 
 5. After that, you need to run `docker compose exec alembic_upgrade head` to apply the migration to the database.
 
 
 TODO add the example of the migration for Enum, because alembic doesn't support the autogeneration for Enum
```

### Comparing `users_db-0.0.8/users_db/migrations/__init__.py` & `users_db-0.0.9/users_db/migrations/__init__.py`

 * *Files identical despite different names*

### Comparing `users_db-0.0.8/users_db/migrations/env.py` & `users_db-0.0.9/users_db/migrations/env.py`

 * *Files identical despite different names*

### Comparing `users_db-0.0.8/users_db/migrations/versions/7e479e30b57f_add_roles_enum_and_role_permission_table.py` & `users_db-0.0.9/users_db/migrations/versions/7e479e30b57f_add_roles_enum_and_role_permission_table.py`

 * *Files identical despite different names*

### Comparing `users_db-0.0.8/users_db/migrations/versions/f102a531f12e_.py` & `users_db-0.0.9/users_db/migrations/versions/f102a531f12e_.py`

 * *Files identical despite different names*

### Comparing `users_db-0.0.8/users_db/migrations/versions/f46112e923d8_.py` & `users_db-0.0.9/users_db/migrations/versions/f46112e923d8_.py`

 * *Files identical despite different names*

### Comparing `users_db-0.0.8/users_db/schema.py` & `users_db-0.0.9/users_db/schema.py`

 * *Files 8% similar despite different names*

```diff
@@ -22,9 +22,11 @@
 users = Table(
     "users",
     Base.metadata,
     Column("id", Integer, primary_key=True),
     Column("first_name", String(64), nullable=False),
     Column("middle_name", String(64), nullable=True),
     Column("last_name", String(64), nullable=False),
+    Column("email", String(64), nullable=False, unique=True),
+    Column("password", String(256), nullable=False),
     Column("role", Enum(Role), nullable=False),
 )
```

### Comparing `users_db-0.0.8/users_db/users.py` & `users_db-0.0.9/users_db/users.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,17 +1,26 @@
 from sqlalchemy import insert, select, update, delete
 
 from users_db.db import db_connection
-from users_db.schema import users
+from users_db.schema import Role, users
+
+ROLE_SUPER_ADMIN = Role.SUPER_ADMIN.name
+ROLE_ADMIN = Role.ADMIN.name
+ROLE_USER = Role.USER.name
 
 
 @db_connection
-def create_user(first_name, middle_name, last_name, db_conn):
+def create_user(first_name, middle_name, last_name, email, password, role, db_conn):
     return insert(users).values(
-        first_name=first_name, middle_name=middle_name, last_name=last_name
+        first_name=first_name,
+        middle_name=middle_name,
+        last_name=last_name,
+        email=email,
+        password=password,
+        role=role,
     )
 
 
 @db_connection
 def get_user(user_id, db_conn=None):
     stmt = select(users).where(users.c.id == user_id)
     rows = db_conn.execute(stmt)
@@ -22,28 +31,31 @@
 @db_connection
 def get_users(
     user_id=None,
     user_ids=None,
     first_name=None,
     middle_name=None,
     last_name=None,
+    email=None,
     db_conn=None,
 ):
     stmt = select(users)
 
     if user_id:
         stmt = stmt.where(users.c.id == user_id)
     if user_ids:
         stmt = stmt.where(users.c.id.in_(user_ids))
     if first_name:
         stmt = stmt.where(users.c.first_name == first_name)
     if middle_name:
         stmt = stmt.where(users.c.middle_name == middle_name)
     if last_name:
         stmt = stmt.where(users.c.last_name == last_name)
+    if email:
+        stmt = stmt.where(users.c.email == email)
 
     rows = db_conn.execute(stmt)
     rows = [dict(row) for row in rows.mappings().all()]
     return rows
 
 
 @db_connection
```

