# Comparing `tmp/simple_connect-1.0.5.tar.gz` & `tmp/simple_connect-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simple_connect-1.0.5.tar", last modified: Wed May 10 18:38:25 2023, max compression
+gzip compressed data, was "simple_connect-1.1.0.tar", last modified: Sat May 13 09:43:35 2023, max compression
```

## Comparing `simple_connect-1.0.5.tar` & `simple_connect-1.1.0.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 saeedabdulrahim   (501) staff       (20)        0 2023-05-10 18:38:25.916870 simple_connect-1.0.5/
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)     1073 2023-05-10 18:26:35.000000 simple_connect-1.0.5/LICENSE
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)     3085 2023-05-10 18:38:25.916307 simple_connect-1.0.5/PKG-INFO
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)     2455 2023-05-10 18:26:35.000000 simple_connect-1.0.5/README.md
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)      626 2023-05-10 18:37:23.000000 simple_connect-1.0.5/pyproject.toml
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)       38 2023-05-10 18:38:25.917010 simple_connect-1.0.5/setup.cfg
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)      745 2023-05-10 18:29:50.000000 simple_connect-1.0.5/setup.py
-drwxr-xr-x   0 saeedabdulrahim   (501) staff       (20)        0 2023-05-10 18:38:25.913264 simple_connect-1.0.5/simple_connect/
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)       21 2023-05-10 18:26:35.000000 simple_connect-1.0.5/simple_connect/__init__.py
--rw-rw-r--   0 saeedabdulrahim   (501) staff       (20)    14358 2023-05-04 09:22:57.000000 simple_connect-1.0.5/simple_connect/connect.py
-drwxr-xr-x   0 saeedabdulrahim   (501) staff       (20)        0 2023-05-10 18:38:25.915744 simple_connect-1.0.5/simple_connect.egg-info/
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)     3085 2023-05-10 18:38:25.000000 simple_connect-1.0.5/simple_connect.egg-info/PKG-INFO
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)      283 2023-05-10 18:38:25.000000 simple_connect-1.0.5/simple_connect.egg-info/SOURCES.txt
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)        1 2023-05-10 18:38:25.000000 simple_connect-1.0.5/simple_connect.egg-info/dependency_links.txt
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)      103 2023-05-10 18:38:25.000000 simple_connect-1.0.5/simple_connect.egg-info/requires.txt
--rw-r--r--   0 saeedabdulrahim   (501) staff       (20)       15 2023-05-10 18:38:25.000000 simple_connect-1.0.5/simple_connect.egg-info/top_level.txt
+drwxr-xr-x   0 saeedabdulrahim   (501) staff       (20)        0 2023-05-13 09:43:35.791074 simple_connect-1.1.0/
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)     1073 2023-05-10 18:26:35.000000 simple_connect-1.1.0/LICENSE
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)     3085 2023-05-13 09:43:35.790686 simple_connect-1.1.0/PKG-INFO
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)     2455 2023-05-10 18:26:35.000000 simple_connect-1.1.0/README.md
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)      626 2023-05-13 09:42:43.000000 simple_connect-1.1.0/pyproject.toml
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)       38 2023-05-13 09:43:35.791169 simple_connect-1.1.0/setup.cfg
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)      745 2023-05-13 09:42:21.000000 simple_connect-1.1.0/setup.py
+drwxr-xr-x   0 saeedabdulrahim   (501) staff       (20)        0 2023-05-13 09:43:35.788335 simple_connect-1.1.0/simple_connect/
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)       21 2023-05-10 18:26:35.000000 simple_connect-1.1.0/simple_connect/__init__.py
+-rw-rw-r--   0 saeedabdulrahim   (501) staff       (20)    13976 2023-05-13 09:41:36.000000 simple_connect-1.1.0/simple_connect/connect.py
+drwxr-xr-x   0 saeedabdulrahim   (501) staff       (20)        0 2023-05-13 09:43:35.790277 simple_connect-1.1.0/simple_connect.egg-info/
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)     3085 2023-05-13 09:43:35.000000 simple_connect-1.1.0/simple_connect.egg-info/PKG-INFO
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)      283 2023-05-13 09:43:35.000000 simple_connect-1.1.0/simple_connect.egg-info/SOURCES.txt
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)        1 2023-05-13 09:43:35.000000 simple_connect-1.1.0/simple_connect.egg-info/dependency_links.txt
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)      103 2023-05-13 09:43:35.000000 simple_connect-1.1.0/simple_connect.egg-info/requires.txt
+-rw-r--r--   0 saeedabdulrahim   (501) staff       (20)       15 2023-05-13 09:43:35.000000 simple_connect-1.1.0/simple_connect.egg-info/top_level.txt
```

### Comparing `simple_connect-1.0.5/LICENSE` & `simple_connect-1.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `simple_connect-1.0.5/PKG-INFO` & `simple_connect-1.1.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple_connect
-Version: 1.0.5
+Version: 1.1.0
 Summary: Simplify SQL Connection for data analysis
 Home-page: https://github.com/saeed-abdul-rahim/simple_connect
 Author: Saeed
 Author-email: Saeed Abdul Rahim <sae.ar2@gmail.com>
 Project-URL: Homepage, https://github.com/saeed-abdul-rahim/simple_connect
 Project-URL: Bug Tracker, https://github.com/saeed-abdul-rahim/simple_connect/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `simple_connect-1.0.5/README.md` & `simple_connect-1.1.0/README.md`

 * *Files identical despite different names*

### Comparing `simple_connect-1.0.5/pyproject.toml` & `simple_connect-1.1.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "simple_connect"
-version = "1.0.5"
+version = "1.1.0"
 authors = [
   { name="Saeed Abdul Rahim", email="sae.ar2@gmail.com" },
 ]
 description = "Simplify SQL Connection for data analysis"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `simple_connect-1.0.5/setup.py` & `simple_connect-1.1.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="simple_connect",
-    version="1.0.5",
+    version="1.1.0",
     author="Saeed",
     author_email="sae.ar2@gmail.com",
     description="Simplify Connection",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url='https://github.com/saeed-abdul-rahim/simple_connect',
     packages=setuptools.find_packages(),
```

### Comparing `simple_connect-1.0.5/simple_connect/connect.py` & `simple_connect-1.1.0/simple_connect/connect.py`

 * *Files 8% similar despite different names*

```diff
@@ -20,160 +20,164 @@
 from email.mime.text import MIMEText
 from email.mime.application import MIMEApplication
 import pandas as pd
 import pymysql as db
 from sqlalchemy import create_engine
 from sqlalchemy.sql import text
 from sshtunnel import SSHTunnelForwarder
+import paramiko
 from googleapiclient.discovery import build
 from googleapiclient import errors, discovery
 from googleapiclient.http import MediaIoBaseDownload
 from httplib2 import Http
 import io
 import boto3
 from tqdm import tqdm
 
 class Common(object):
-    
-    def __init__(self,sql_serverhost,sql_user,sql_password,database):
-        self.sql_serverhost = sql_serverhost
-        self.sql_user=sql_user
-        self.sql_password=sql_password
-        self.database=database
+
+    def __init__(self, credentials, database):
+        self.__set_credentials(credentials)
+        self.database = database
     
     def create_sq_string(col_set, sep):
         cols=""
         for i, col in enumerate(col_set):
             cols = cols+ col + " = :"+col
             if not i==(len(col_set)-1):
                 cols = cols+" "+sep+" "
         return cols
     
-    def update_main(self,df,conn,table_name,set_cols,where_cols):
+    def update_main(self, df, conn, table_name, set_cols, where_cols):
         dict_data = df.to_dict('records')
         dict_data=tuple(dict_data)
         set_columns=Common.create_sq_string(set_cols, ",")
         where_columns=Common.create_sq_string(where_cols, "AND")
         stmt="UPDATE "+table_name+" SET "+set_columns+" WHERE "+where_columns
         stmt=text(stmt)
         for line in tqdm(dict_data):
               conn.execute(stmt, **line)  
         return self 
     
-    def delete_main(self,df,conn,table_name,where_cols):
+    def delete_main(self, df, conn, table_name, where_cols):
         dict_data = df.to_dict('records')
         dict_data=tuple(dict_data)
         where_columns=Common.create_sq_string(where_cols, "AND")
         stmt="DELETE FROM "+table_name+" WHERE "+where_columns
         stmt=text(stmt)
         for line in tqdm(dict_data):
               conn.execute(stmt, **line)
         return self
     
     def _execute(self, conn, stmt):
         conn.execute(text(stmt))
         return self
 
-class Connect(Common):
-    
-    def __init__(self,credentials,database):
-        cred_dir=os.path.join(os.path.expanduser('~'),'.credentials')
-        cred_file=os.path.join(cred_dir,credentials)
+    def __set_credentials(self, credentials):
+
+        self._cred_dir = os.path.join(os.path.expanduser('~'), '.credentials')
+        cred_file = os.path.join(self._cred_dir, credentials)
         with open(cred_file) as f:
             cred=json.load(f)
-        sql_serverhost=cred['SQL_HOST']
-        sql_user=cred['SQL_USER']
-        sql_password=cred['SQL_PASSWORD']
-        self.common=Common(sql_serverhost,sql_user,sql_password,database)
-        self.mydb=create_engine('mysql+pymysql://' + sql_user + ':' + sql_password + '@' + sql_serverhost + ':' + str(3306) + '/' + database , echo=False)
+        
+        self.localhost = '127.0.0.1'
+        self.sql_host = cred['SQL_HOST']
+        self.sql_user = cred['SQL_USER']
+        self.sql_password = cred['SQL_PASSWORD']
+
+        if 'BASTION_HOST' in cred:
+            self.bastion_host = cred['BASTION_HOST']
+            self.ssh_username = cred['SSH_USERNAME']
+            self.ssh_password = cred['SSH_PASSWORD']
+
+
+class Connect(Common):
+    
+    def __init__(self, credentials, database):
+        super().__init__(credentials, database)
+        self.db_engine = create_engine(f"mysql+pymysql://{self.sql_user}:{self.sql_password}@{self.sql_host}:3306/{self.database}", echo=False)
     
     def to_db(self,data,table):
-        data.to_sql(name=table, con=self.mydb, if_exists = 'append', index=False, chunksize=5000)
+        data.to_sql(name=table, con=self.db_engine, if_exists = 'append', index=False, chunksize=5000)
         
     def query(self,q):
-        return pd.read_sql_query(q, self.mydb)
+        return pd.read_sql_query(q, self.db_engine)
     
     def update_table(self,df,table_name,set_cols,where_cols):
-        self.common.update_main(df,self.mydb,table_name,set_cols,where_cols)
+        self.update_main(df,self.db_engine,table_name,set_cols,where_cols)
         
     def delete_row(self,df,table_name,where_cols):
-        self.common.delete_main(df,self.mydb,table_name,where_cols)
+        self.delete_main(df,self.db_engine,table_name,where_cols)
         
     def execute(self, stmt):
-        self.common._execute(self.mydb, stmt)
+        self._execute(self.db_engine, stmt)
     
 class BastionConnect(Common):
         
-    def __init__(self, credentials, database, pem_path=None):
-        cred_dir=os.path.join(os.path.expanduser('~'),'.credentials')
-        cred_file=os.path.join(cred_dir,credentials)
-        with open(cred_file) as f:
-            cred=json.load(f)        
-        ssh_username=cred['SSH_USERNAME']
-        ssh_password=cred['SSH_PASSWORD']
-        sql_serverhost=cred['SQL_HOST']
-        sql_user=cred['SQL_USER']
-        sql_password=cred['SQL_PASSWORD']
-        self.bastion_host = cred['BASTION_HOST']
-        self.localhost = '127.0.0.1'
-        self.ssh_username = ssh_username
-        self.ssh_password=ssh_password
-        self.common=Common(sql_serverhost,sql_user,sql_password,database)
-        if pem_path:
+    def __init__(self, credentials, database, pem=None):
+        super().__init__(credentials, database)
+
+        if pem:
+            pem_path=os.path.join(self._cred_dir, pem)
+            pem_file = paramiko.RSAKey.from_private_key_file(pem_path)
             self.server = SSHTunnelForwarder(
-                        (self.bastion_host, 22),
-                          ssh_username=self.ssh_username,
-                          ssh_private_key=pem_path,
-                          remote_bind_address=(self.common.sql_serverhost, 3306))
+                (self.bastion_host, 22),
+                ssh_username=self.ssh_username,
+                ssh_private_key=pem_file,
+                remote_bind_address=(self.sql_host, 3306)
+            )
         else:
             self.server = SSHTunnelForwarder(
-                        (self.bastion_host, 22),
-                          ssh_username=self.ssh_username,
-                          ssh_password=self.ssh_password,
-                          remote_bind_address=(self.common.sql_serverhost, 3306))
+                (self.bastion_host, 22),
+                ssh_username=self.ssh_username,
+                ssh_password=self.ssh_password,
+                remote_bind_address=(self.sql_host, 3306)
+            )
         self.conn=None
-        self.mydb=None
+        self.db_engine=None
     
     def start_conn(self):
-        self.conn = db.connect(host=self.localhost,
-                      port=self.server.local_bind_port,
-                      user=self.common.sql_user,
-                      passwd=self.common.sql_password,
-                      db=self.common.database)
-        self.mydb=create_engine('mysql+pymysql://' + self.common.sql_user + ':' + self.common.sql_password + '@' + self.localhost + ':' + str(self.server.local_bind_port) + '/' + self.common.database , echo=False)
+        self.conn = db.connect(
+            host=self.localhost,
+            port=self.server.local_bind_port,
+            user=self.sql_user,
+            passwd=self.sql_password,
+            db=self.database
+        )
+        self.db_engine = create_engine(f"mysql+pymysql://{self.sql_user}:{self.sql_password}@{self.localhost}:{str(self.server.local_bind_port)}/{self.database}", echo=False)
         
     def query(self,q):
         self.server.start()
         self.start_conn()
         df=pd.read_sql_query(q, self.conn)
         self.server.stop()
         return df   
 
     def to_db(self,df,table):
         self.server.start()
         self.start_conn()
-        df.to_sql(name=table, con=self.mydb, if_exists = 'append', index=False, chunksize=5000)
+        df.to_sql(name=table, con=self.db_engine, if_exists = 'append', index=False, chunksize=5000)
         self.server.stop()
         
-    def update_table(self,df,table_name,set_cols,where_cols):
+    def update_table(self, df, table_name, set_cols, where_cols):
         self.server.start()
         self.start_conn()
-        self.common.update_main(df,self.mydb,table_name,set_cols,where_cols)  
+        self.update_main(df, self.db_engine, table_name, set_cols, where_cols)  
         self.server.stop()
         
-    def delete_row(self,df,table_name,where_cols):
+    def delete_row(self, df, table_name, where_cols):
         self.server.start()
         self.start_conn()
-        self.common.delete_main(df,self.mydb,table_name,where_cols)  
+        self.delete_main(df, self.db_engine, table_name, where_cols)  
         self.server.stop()
     
     def execute(self, stmt):
         self.server.start()
         self.start_conn()
-        self.common._execute(self.mydb, stmt)
+        self._execute(self.db_engine, stmt)
         self.server.stop()
 
 
 class Gdrive:
     
     SCOPES = 'https://www.googleapis.com/auth/drive'
```

### Comparing `simple_connect-1.0.5/simple_connect.egg-info/PKG-INFO` & `simple_connect-1.1.0/simple_connect.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-connect
-Version: 1.0.5
+Version: 1.1.0
 Summary: Simplify SQL Connection for data analysis
 Home-page: https://github.com/saeed-abdul-rahim/simple_connect
 Author: Saeed
 Author-email: Saeed Abdul Rahim <sae.ar2@gmail.com>
 Project-URL: Homepage, https://github.com/saeed-abdul-rahim/simple_connect
 Project-URL: Bug Tracker, https://github.com/saeed-abdul-rahim/simple_connect/issues
 Classifier: Programming Language :: Python :: 3
```

