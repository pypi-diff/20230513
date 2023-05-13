# Comparing `tmp/gandai-1.1.4.tar.gz` & `tmp/gandai-1.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gandai-1.1.4.tar", last modified: Fri May 12 20:54:13 2023, max compression
+gzip compressed data, was "gandai-1.1.5.tar", last modified: Sat May 13 20:22:51 2023, max compression
```

## Comparing `gandai-1.1.4.tar` & `gandai-1.1.5.tar`

### file list

```diff
@@ -1,47 +1,37 @@
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-12 20:54:13.354554 gandai-1.1.4/
--rw-r--r--   0 parker     (501) staff       (20)       26 2023-05-09 22:04:17.000000 gandai-1.1.4/MANIFEST.in
--rw-r--r--   0 parker     (501) staff       (20)      215 2023-05-12 20:54:13.354427 gandai-1.1.4/PKG-INFO
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-12 20:54:13.348103 gandai-1.1.4/gandai/
--rw-r--r--   0 parker     (501) staff       (20)        0 2023-05-11 12:03:39.000000 gandai-1.1.4/gandai/__init__.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-12 20:54:13.351535 gandai-1.1.4/gandai/__pycache__/
--rw-r--r--   0 parker     (501) staff       (20)      179 2023-05-11 12:17:29.000000 gandai-1.1.4/gandai/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     7464 2023-05-09 01:55:35.000000 gandai-1.1.4/gandai/__pycache__/adapters.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     4191 2023-05-02 14:03:52.000000 gandai-1.1.4/gandai/__pycache__/auth.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     4152 2023-04-12 13:11:27.000000 gandai-1.1.4/gandai/__pycache__/datastore.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     1981 2023-05-11 12:17:30.000000 gandai-1.1.4/gandai/__pycache__/db.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     5979 2023-05-05 21:52:33.000000 gandai-1.1.4/gandai/__pycache__/grata.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     5068 2023-05-12 19:30:40.000000 gandai-1.1.4/gandai/__pycache__/main.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     6064 2023-05-12 19:41:17.000000 gandai-1.1.4/gandai/__pycache__/models.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)    15927 2023-05-11 13:39:01.000000 gandai-1.1.4/gandai/__pycache__/query.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     3403 2023-05-01 00:06:24.000000 gandai-1.1.4/gandai/__pycache__/services.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     7849 2023-05-12 19:25:42.000000 gandai-1.1.4/gandai/__pycache__/sources.cpython-311.pyc
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-12 20:54:13.352512 gandai-1.1.4/gandai/adapters/
--rw-r--r--   0 parker     (501) staff       (20)        0 2023-03-03 12:29:00.000000 gandai-1.1.4/gandai/adapters/__init__.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-12 20:54:13.353583 gandai-1.1.4/gandai/adapters/__pycache__/
--rw-r--r--   0 parker     (501) staff       (20)      188 2023-04-07 16:05:45.000000 gandai-1.1.4/gandai/adapters/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     1875 2023-04-10 12:31:26.000000 gandai-1.1.4/gandai/adapters/__pycache__/dealcloud.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)      924 2023-04-07 16:06:33.000000 gandai-1.1.4/gandai/adapters/__pycache__/filters.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)    14686 2023-04-14 19:20:28.000000 gandai-1.1.4/gandai/adapters/__pycache__/grata.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     1299 2023-05-11 12:41:01.000000 gandai-1.1.4/gandai/adapters/dealcloud.py
--rw-r--r--   0 parker     (501) staff       (20)     1824 2023-03-18 19:53:14.000000 gandai-1.1.4/gandai/adapters/filters.py
--rw-r--r--   0 parker     (501) staff       (20)    10624 2023-05-11 12:52:58.000000 gandai-1.1.4/gandai/adapters/grata.py
--rw-r--r--   0 parker     (501) staff       (20)     1742 2023-05-12 20:52:41.000000 gandai-1.1.4/gandai/auth.py
--rw-r--r--   0 parker     (501) staff       (20)     1578 2023-04-12 13:11:26.000000 gandai-1.1.4/gandai/datastore.py
--rw-r--r--   0 parker     (501) staff       (20)     2382 2023-05-11 11:58:58.000000 gandai-1.1.4/gandai/db.py
--rw-r--r--   0 parker     (501) staff       (20)     3286 2023-05-12 19:30:37.000000 gandai-1.1.4/gandai/main.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-12 20:54:13.354152 gandai-1.1.4/gandai/migrations/
--rw-r--r--   0 parker     (501) staff       (20)        0 2023-04-10 12:18:33.000000 gandai-1.1.4/gandai/migrations/__init__.py
--rw-r--r--   0 parker     (501) staff       (20)     3653 2023-05-12 19:32:11.000000 gandai-1.1.4/gandai/migrations/db_create.py
--rw-r--r--   0 parker     (501) staff       (20)     2072 2023-05-12 19:25:46.000000 gandai-1.1.4/gandai/migrations/db_seed.py
--rw-r--r--   0 parker     (501) staff       (20)     1868 2023-05-11 12:41:47.000000 gandai-1.1.4/gandai/migrations/dealcloud_to_gandai.py
--rw-r--r--   0 parker     (501) staff       (20)     2592 2023-05-12 19:41:16.000000 gandai-1.1.4/gandai/models.py
--rw-r--r--   0 parker     (501) staff       (20)     8401 2023-05-11 13:39:00.000000 gandai-1.1.4/gandai/query.py
--rw-r--r--   0 parker     (501) staff       (20)     5418 2023-05-12 19:25:41.000000 gandai-1.1.4/gandai/sources.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-12 20:54:13.348643 gandai-1.1.4/gandai.egg-info/
--rw-r--r--   0 parker     (501) staff       (20)      215 2023-05-12 20:54:13.000000 gandai-1.1.4/gandai.egg-info/PKG-INFO
--rw-r--r--   0 parker     (501) staff       (20)     1199 2023-05-12 20:54:13.000000 gandai-1.1.4/gandai.egg-info/SOURCES.txt
--rw-r--r--   0 parker     (501) staff       (20)        1 2023-05-12 20:54:13.000000 gandai-1.1.4/gandai.egg-info/dependency_links.txt
--rw-r--r--   0 parker     (501) staff       (20)        7 2023-05-12 20:54:13.000000 gandai-1.1.4/gandai.egg-info/top_level.txt
--rw-r--r--   0 parker     (501) staff       (20)      370 2023-05-12 20:54:00.000000 gandai-1.1.4/pyproject.toml
--rw-r--r--   0 parker     (501) staff       (20)       38 2023-05-12 20:54:13.354585 gandai-1.1.4/setup.cfg
--rw-r--r--   0 parker     (501) staff       (20)      159 2023-03-06 14:38:11.000000 gandai-1.1.4/setup.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-13 20:22:51.218492 gandai-1.1.5/
+-rw-r--r--   0 parker     (501) staff       (20)       26 2023-05-09 22:04:17.000000 gandai-1.1.5/MANIFEST.in
+-rw-r--r--   0 parker     (501) staff       (20)      215 2023-05-13 20:22:51.218361 gandai-1.1.5/PKG-INFO
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-13 20:22:51.213620 gandai-1.1.5/gandai/
+-rw-r--r--   0 parker     (501) staff       (20)       45 2023-05-13 19:24:50.000000 gandai-1.1.5/gandai/__init__.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-13 20:22:51.217116 gandai-1.1.5/gandai/__pycache__/
+-rw-r--r--   0 parker     (501) staff       (20)      264 2023-05-13 19:25:52.000000 gandai-1.1.5/gandai/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     7464 2023-05-09 01:55:35.000000 gandai-1.1.5/gandai/__pycache__/adapters.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     4191 2023-05-02 14:03:52.000000 gandai-1.1.5/gandai/__pycache__/auth.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     4152 2023-04-12 13:11:27.000000 gandai-1.1.5/gandai/__pycache__/datastore.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     2075 2023-05-13 19:36:23.000000 gandai-1.1.5/gandai/__pycache__/db.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     5979 2023-05-05 21:52:33.000000 gandai-1.1.5/gandai/__pycache__/grata.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     5068 2023-05-12 19:30:40.000000 gandai-1.1.5/gandai/__pycache__/main.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     6064 2023-05-12 19:41:17.000000 gandai-1.1.5/gandai/__pycache__/models.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)    15927 2023-05-13 19:31:21.000000 gandai-1.1.5/gandai/__pycache__/query.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     3403 2023-05-01 00:06:24.000000 gandai-1.1.5/gandai/__pycache__/services.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     7849 2023-05-12 19:25:42.000000 gandai-1.1.5/gandai/__pycache__/sources.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     1699 2023-05-13 19:58:43.000000 gandai-1.1.5/gandai/auth.py
+-rw-r--r--   0 parker     (501) staff       (20)     2451 2023-05-13 19:35:44.000000 gandai-1.1.5/gandai/db.py
+-rw-r--r--   0 parker     (501) staff       (20)     3286 2023-05-12 19:30:37.000000 gandai-1.1.5/gandai/main.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-13 20:22:51.217662 gandai-1.1.5/gandai/migrations/
+-rw-r--r--   0 parker     (501) staff       (20)        0 2023-04-10 12:18:33.000000 gandai-1.1.5/gandai/migrations/__init__.py
+-rw-r--r--   0 parker     (501) staff       (20)      409 2023-05-13 19:26:13.000000 gandai-1.1.5/gandai/migrations/db_create.py
+-rw-r--r--   0 parker     (501) staff       (20)     1565 2023-05-13 19:29:54.000000 gandai-1.1.5/gandai/migrations/db_seed.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-13 20:22:51.217915 gandai-1.1.5/gandai/migrations/sql/
+-rw-r--r--   0 parker     (501) staff       (20)     2815 2023-05-13 19:15:16.000000 gandai-1.1.5/gandai/migrations/sql/schema.sql
+-rw-r--r--   0 parker     (501) staff       (20)     2592 2023-05-12 19:41:16.000000 gandai-1.1.5/gandai/models.py
+-rw-r--r--   0 parker     (501) staff       (20)     8401 2023-05-13 19:31:13.000000 gandai-1.1.5/gandai/query.py
+-rw-r--r--   0 parker     (501) staff       (20)     5418 2023-05-12 19:25:41.000000 gandai-1.1.5/gandai/sources.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-05-13 20:22:51.214314 gandai-1.1.5/gandai.egg-info/
+-rw-r--r--   0 parker     (501) staff       (20)      215 2023-05-13 20:22:51.000000 gandai-1.1.5/gandai.egg-info/PKG-INFO
+-rw-r--r--   0 parker     (501) staff       (20)      853 2023-05-13 20:22:51.000000 gandai-1.1.5/gandai.egg-info/SOURCES.txt
+-rw-r--r--   0 parker     (501) staff       (20)        1 2023-05-13 20:22:51.000000 gandai-1.1.5/gandai.egg-info/dependency_links.txt
+-rw-r--r--   0 parker     (501) staff       (20)        7 2023-05-13 20:22:51.000000 gandai-1.1.5/gandai.egg-info/top_level.txt
+-rw-r--r--   0 parker     (501) staff       (20)      370 2023-05-13 20:22:42.000000 gandai-1.1.5/pyproject.toml
+-rw-r--r--   0 parker     (501) staff       (20)       38 2023-05-13 20:22:51.218530 gandai-1.1.5/setup.cfg
+-rw-r--r--   0 parker     (501) staff       (20)      159 2023-03-06 14:38:11.000000 gandai-1.1.5/setup.py
```

### Comparing `gandai-1.1.4/gandai/__pycache__/adapters.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/adapters.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/__pycache__/auth.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/auth.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/__pycache__/datastore.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/datastore.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/__pycache__/db.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/db.cpython-311.pyc`

 * *Files 14% similar despite different names*

#### Python bytecode

```diff
@@ -1,10 +1,10 @@
 magic:    0xa70d0d0a
-moddate:  0x82d85c64 (Thu May 11 11:58:58 2023 UTC)
-files sz: 2382
+moddate:  0x90e65f64 (Sat May 13 19:35:44 2023 UTC)
+files sz: 2451
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 2
    flags     : 0
    code
       0x9700640064016c005a00640064026c016d025a026d035a030100640064
@@ -59,23 +59,25 @@
          flags     : 3
          code
             0x87028703870487058706870797007400000000000000000000006a0100
             000000000000006401190000000000000000008a06740000000000000000
             0000006a0100000000000000006402190000000000000000008a05740000
             0000000000000000006a0100000000000000006403190000000000000000
             008a047400000000000000000000006a0100000000000000006404190000
-            000000000000008a037400000000000000000000006a0100000000000000
-            00a00200000000000000000000000000000000000000006405a6010000ab
-            010000000000000000720c7406000000000000000000006a040000000000
-            0000006e0b7406000000000000000000006a0500000000000000008a0774
-            0d00000000000000000000a6000000ab0000000000000000008a02640674
-            0e000000000000000000006a0800000000000000006a0900000000000000
-            00660288028803880488058806880766066407840c7d0074150000000000
-            00000000006a0b000000000000000064087c006409640a640b640cac0da6
-            060000ab0600000000000000007d017c015300
+            000000000000008a03740500000000000000000000890689058904640564
+            068502190000000000000000008903a6040000ab04000000000000000001
+            007400000000000000000000006a010000000000000000a0030000000000
+            0000000000000000000000000000006407a6010000ab0100000000000000
+            00720c7408000000000000000000006a0500000000000000006e0b740800
+            0000000000000000006a0600000000000000008a07740f00000000000000
+            000000a6000000ab0000000000000000008a026408741000000000000000
+            0000006a0900000000000000006a0a000000000000000066028802880388
+            0488058806880766066409840c7d007417000000000000000000006a0c00
+            00000000000000640a7c00640b640c640d640eac0fa6060000ab06000000
+            00000000007d017c015300
                        0 MAKE_CELL                2 (connector)
                        2 MAKE_CELL                3 (db_name)
                        4 MAKE_CELL                4 (db_pass)
                        6 MAKE_CELL                5 (db_user)
                        8 MAKE_CELL                6 (instance_connection_name)
                       10 MAKE_CELL                7 (ip_type)
          
@@ -101,142 +103,157 @@
          
           23         122 LOAD_GLOBAL              0 (os)
                      134 LOAD_ATTR                1 (environ)
                      144 LOAD_CONST               4 ('DB_NAME')
                      146 BINARY_SUBSCR
                      156 STORE_DEREF              3 (db_name)
          
-          25         158 LOAD_GLOBAL              0 (os)
-                     170 LOAD_ATTR                1 (environ)
-                     180 LOAD_METHOD              2 (get)
-                     202 LOAD_CONST               5 ('PRIVATE_IP')
-                     204 PRECALL                  1
-                     208 CALL                     1
-                     218 POP_JUMP_FORWARD_IF_FALSE    12 (to 244)
-                     220 LOAD_GLOBAL              6 (IPTypes)
-                     232 LOAD_ATTR                4 (PRIVATE)
-                     242 JUMP_FORWARD            11 (to 266)
-                 >>  244 LOAD_GLOBAL              6 (IPTypes)
-                     256 LOAD_ATTR                5 (PUBLIC)
-                 >>  266 STORE_DEREF              7 (ip_type)
-         
-          28         268 LOAD_GLOBAL             13 (NULL + Connector)
-                     280 PRECALL                  0
-                     284 CALL                     0
-                     294 STORE_DEREF              2 (connector)
-         
-          30         296 LOAD_CONST               6 ('return')
-                     298 LOAD_GLOBAL             14 (pg8000)
-                     310 LOAD_ATTR                8 (dbapi)
-                     320 LOAD_ATTR                9 (Connection)
-                     330 BUILD_TUPLE              2
-                     332 LOAD_CLOSURE             2 (connector)
-                     334 LOAD_CLOSURE             3 (db_name)
-                     336 LOAD_CLOSURE             4 (db_pass)
-                     338 LOAD_CLOSURE             5 (db_user)
-                     340 LOAD_CLOSURE             6 (instance_connection_name)
-                     342 LOAD_CLOSURE             7 (ip_type)
-                     344 BUILD_TUPLE              6
-                     346 LOAD_CONST               7 (<code object getconn, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py", line 30>)
-                     348 MAKE_FUNCTION           12 (annotations, closure)
-                     350 STORE_FAST               0 (getconn)
-         
-          43         352 LOAD_GLOBAL             21 (NULL + sqlalchemy)
-                     364 LOAD_ATTR               11 (create_engine)
-         
-          44         374 LOAD_CONST               8 ('postgresql+pg8000://')
-         
-          45         376 LOAD_FAST                0 (getconn)
-         
-          48         378 LOAD_CONST               9 (5)
-         
-          51         380 LOAD_CONST              10 (2)
-         
-          59         382 LOAD_CONST              11 (30)
-         
-          64         384 LOAD_CONST              12 (1800)
-         
-          43         386 KW_NAMES                13
-                     388 PRECALL                  6
-                     392 CALL                     6
-                     402 STORE_FAST               1 (pool)
+          24         158 LOAD_GLOBAL              5 (NULL + print)
+                     170 LOAD_DEREF               6 (instance_connection_name)
+                     172 LOAD_DEREF               5 (db_user)
+                     174 LOAD_DEREF               4 (db_pass)
+                     176 LOAD_CONST               5 (-5)
+                     178 LOAD_CONST               6 (None)
+                     180 BUILD_SLICE              2
+                     182 BINARY_SUBSCR
+                     192 LOAD_DEREF               3 (db_name)
+                     194 PRECALL                  4
+                     198 CALL                     4
+                     208 POP_TOP
+         
+          26         210 LOAD_GLOBAL              0 (os)
+                     222 LOAD_ATTR                1 (environ)
+                     232 LOAD_METHOD              3 (get)
+                     254 LOAD_CONST               7 ('PRIVATE_IP')
+                     256 PRECALL                  1
+                     260 CALL                     1
+                     270 POP_JUMP_FORWARD_IF_FALSE    12 (to 296)
+                     272 LOAD_GLOBAL              8 (IPTypes)
+                     284 LOAD_ATTR                5 (PRIVATE)
+                     294 JUMP_FORWARD            11 (to 318)
+                 >>  296 LOAD_GLOBAL              8 (IPTypes)
+                     308 LOAD_ATTR                6 (PUBLIC)
+                 >>  318 STORE_DEREF              7 (ip_type)
+         
+          29         320 LOAD_GLOBAL             15 (NULL + Connector)
+                     332 PRECALL                  0
+                     336 CALL                     0
+                     346 STORE_DEREF              2 (connector)
+         
+          31         348 LOAD_CONST               8 ('return')
+                     350 LOAD_GLOBAL             16 (pg8000)
+                     362 LOAD_ATTR                9 (dbapi)
+                     372 LOAD_ATTR               10 (Connection)
+                     382 BUILD_TUPLE              2
+                     384 LOAD_CLOSURE             2 (connector)
+                     386 LOAD_CLOSURE             3 (db_name)
+                     388 LOAD_CLOSURE             4 (db_pass)
+                     390 LOAD_CLOSURE             5 (db_user)
+                     392 LOAD_CLOSURE             6 (instance_connection_name)
+                     394 LOAD_CLOSURE             7 (ip_type)
+                     396 BUILD_TUPLE              6
+                     398 LOAD_CONST               9 (<code object getconn, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py", line 31>)
+                     400 MAKE_FUNCTION           12 (annotations, closure)
+                     402 STORE_FAST               0 (getconn)
+         
+          44         404 LOAD_GLOBAL             23 (NULL + sqlalchemy)
+                     416 LOAD_ATTR               12 (create_engine)
+         
+          45         426 LOAD_CONST              10 ('postgresql+pg8000://')
+         
+          46         428 LOAD_FAST                0 (getconn)
+         
+          49         430 LOAD_CONST              11 (5)
+         
+          52         432 LOAD_CONST              12 (2)
+         
+          60         434 LOAD_CONST              13 (30)
+         
+          65         436 LOAD_CONST              14 (1800)
+         
+          44         438 KW_NAMES                15
+                     440 PRECALL                  6
+                     444 CALL                     6
+                     454 STORE_FAST               1 (pool)
          
-          67         404 LOAD_FAST                1 (pool)
-                     406 RETURN_VALUE
+          68         456 LOAD_FAST                1 (pool)
+                     458 RETURN_VALUE
          consts
             '\n    Initializes a connection pool for a Cloud SQL instance of Postgres.\n\n    Uses the Cloud SQL Python Connector package.\n    '
             'INSTANCE_CONNECTION_NAME'
             'DB_USER'
             'DB_PASS'
             'DB_NAME'
+            -5
+            None
             'PRIVATE_IP'
             'return'
             code
                argcount  : 0
                nlocals   : 1
                stacksize : 8
                flags     : 19
                code
                   0x950697008901a000000000000000000000000000000000000000000089
                   0564018904890389028906ac02a6060000ab0600000000000000007d007c
                   005300
                              0 COPY_FREE_VARS           6
                
-                30           2 RESUME                   0
+                31           2 RESUME                   0
                
-                31           4 LOAD_DEREF               1 (connector)
+                32           4 LOAD_DEREF               1 (connector)
                              6 LOAD_METHOD              0 (connect)
                
-                32          28 LOAD_DEREF               5 (instance_connection_name)
+                33          28 LOAD_DEREF               5 (instance_connection_name)
                
-                33          30 LOAD_CONST               1 ('pg8000')
+                34          30 LOAD_CONST               1 ('pg8000')
                
-                34          32 LOAD_DEREF               4 (db_user)
+                35          32 LOAD_DEREF               4 (db_user)
                
-                35          34 LOAD_DEREF               3 (db_pass)
+                36          34 LOAD_DEREF               3 (db_pass)
                
-                36          36 LOAD_DEREF               2 (db_name)
+                37          36 LOAD_DEREF               2 (db_name)
                
-                37          38 LOAD_DEREF               6 (ip_type)
+                38          38 LOAD_DEREF               6 (ip_type)
                
-                31          40 KW_NAMES                 2
+                32          40 KW_NAMES                 2
                             42 PRECALL                  6
                             46 CALL                     6
                             56 STORE_FAST               0 (conn)
                
-                39          58 LOAD_FAST                0 (conn)
+                40          58 LOAD_FAST                0 (conn)
                             60 RETURN_VALUE
                consts
                   None
                   'pg8000'
                   ('user', 'password', 'db', 'ip_type')
                names      ('connect',)
                varnames   ('conn',)
                freevars   ('connector', 'db_name', 'db_pass', 'db_user', 'instance_connection_name', 'ip_type')
                cellvars   ()
                filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py'
                name       'getconn'
-               firstlineno 30
+               firstlineno 31
                lnotab 0x040118010201020102010201020102fa1208
             'postgresql+pg8000://'
             5
             2
             30
             1800
             ('creator', 'pool_size', 'max_overflow', 'pool_timeout', 'pool_recycle')
-         names      ('os', 'environ', 'get', 'IPTypes', 'PRIVATE', 'PUBLIC', 'Connector', 'pg8000', 'dbapi', 'Connection', 'sqlalchemy', 'create_engine')
+         names      ('os', 'environ', 'print', 'get', 'IPTypes', 'PRIVATE', 'PUBLIC', 'Connector', 'pg8000', 'dbapi', 'Connection', 'sqlalchemy', 'create_engine')
          varnames   ('getconn', 'pool')
          freevars   ()
          cellvars   ('connector', 'db_name', 'db_pass', 'db_user', 'instance_connection_name', 'ip_type')
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py'
          name       'connect_with_connector'
          firstlineno 9
          lnotab
-            0x0e0b24012401240124026e031c02380d16010201020302030208020502
-            eb1218
+            0x0e0b240124012401240134026e031c02380d1601020102030203020802
+            0502eb1218
    names      ('os', 'google.cloud.sql.connector', 'Connector', 'IPTypes', 'pg8000', 'sqlalchemy', 'engine', 'base', 'Engine', 'connect_with_connector')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py'
    name       '<module>'
    firstlineno 1
```

### Comparing `gandai-1.1.4/gandai/__pycache__/grata.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/grata.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/__pycache__/main.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/main.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/__pycache__/models.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/models.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/__pycache__/query.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/query.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xf4ef5c64 (Thu May 11 13:39:00 2023 UTC)
+moddate:  0x81e55f64 (Sat May 13 19:31:13 2023 UTC)
 files sz: 8401
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 5
    flags     : 0
    code
```

### Comparing `gandai-1.1.4/gandai/__pycache__/services.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/services.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/__pycache__/sources.cpython-311.pyc` & `gandai-1.1.5/gandai/__pycache__/sources.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/auth.py` & `gandai-1.1.5/gandai/auth.py`

 * *Files 7% similar despite different names*

```diff
@@ -2,16 +2,14 @@
 import random
 from dataclasses import asdict, dataclass, field
 from hashlib import md5
 from time import time
 import os
 from twilio.rest import Client
 
-# from gandai.datastore import Cloudstore
-
 # from gandai.models.User import user_exists # create_user
 
 # ds = Cloudstore()
 twilio_client = Client(os.getenv("TWILIO_APP"), os.getenv("TWILIO_TOKEN"))
 
 
 @dataclass
```

### Comparing `gandai-1.1.4/gandai/db.py` & `gandai-1.1.5/gandai/db.py`

 * *Files 6% similar despite different names*

```diff
@@ -17,14 +17,15 @@
     # Cloud Secret Manager (https://cloud.google.com/secret-manager) to help
     # keep secrets safe.
 
     instance_connection_name = os.environ["INSTANCE_CONNECTION_NAME"]  # e.g. 'project:region:instance'
     db_user = os.environ["DB_USER"]  # e.g. 'my-db-user'
     db_pass = os.environ["DB_PASS"]  # e.g. 'my-db-password'
     db_name = os.environ["DB_NAME"]  # e.g. 'my-database'
+    print(instance_connection_name, db_user, db_pass[-5::], db_name)
 
     ip_type = IPTypes.PRIVATE if os.environ.get("PRIVATE_IP") else IPTypes.PUBLIC
 
     # initialize Cloud SQL Python Connector object
     connector = Connector()
 
     def getconn() -> pg8000.dbapi.Connection:
```

### Comparing `gandai-1.1.4/gandai/main.py` & `gandai-1.1.5/gandai/main.py`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/migrations/db_create.py` & `gandai-1.1.5/gandai/migrations/sql/schema.sql`

 * *Files 26% similar despite different names*

```diff
@@ -1,114 +1,94 @@
-import sqlalchemy
-from gandai.db import connect_with_connector
-from dotenv import load_dotenv
-
-load_dotenv()
-
-
-def create_db():
-    db = connect_with_connector()
-
-    statement = sqlalchemy.text(
-        """
-            CREATE TABLE IF NOT EXISTS search  (
-            id SERIAL PRIMARY KEY,
-            uid INTEGER UNIQUE NOT NULL,
-            meta JSONB,
-            label VARCHAR(255) UNIQUE,
-            client_domain VARCHAR(255),
-            inclusion JSONB DEFAULT '{}'::jsonb,
-            exclusion JSONB DEFAULT '{}'::jsonb,
-            sort JSONB DEFAULT '{}'::jsonb,
-            created TIMESTAMP NOT NULL DEFAULT NOW(),
-            updated TIMESTAMP NOT NULL DEFAULT NOW()
-        );
-
-        CREATE TABLE IF NOT EXISTS company (
-            id SERIAL PRIMARY KEY,
-            domain VARCHAR(255) UNIQUE NOT NULL,
-            name VARCHAR(255),
-            description TEXT,
-            meta JSONB DEFAULT '{}'::jsonb, 
-            created TIMESTAMP NOT NULL DEFAULT NOW(),
-            updated TIMESTAMP NOT NULL DEFAULT NOW()
-
-        );
-
-        CREATE TABLE IF NOT EXISTS actor (
-            id SERIAL PRIMARY KEY,
-            key VARCHAR(255) UNIQUE NOT NULL,
-            type VARCHAR(255) NOT NULL,
-            name VARCHAR(255),
-            created TIMESTAMP NOT NULL DEFAULT NOW(),
-            updated TIMESTAMP NOT NULL DEFAULT NOW()
-        );
-
-
-        CREATE TABLE IF NOT EXISTS event (
-            id SERIAL PRIMARY KEY,
-            search_uid INTEGER NOT NULL REFERENCES search(uid),
-            domain VARCHAR(255) REFERENCES company(domain),
-            actor_key VARCHAR(255) NOT NULL REFERENCES actor(key),
-            type VARCHAR(255) NOT NULL,
-            data JSONB DEFAULT '{}'::jsonb,
-            created TIMESTAMP NOT NULL DEFAULT NOW()
-        );
-
-        --ALTER TABLE event ADD CONSTRAINT unique_event_type_domain_search_uid UNIQUE (type, domain, search_uid);
-
-
-        CREATE TABLE IF NOT EXISTS checkpoint (
-            id SERIAL PRIMARY KEY,
-            event_id INTEGER NOT NULL REFERENCES event(id),
-            created TIMESTAMP NOT NULL DEFAULT NOW()
-        );
-
-        CREATE MATERIALIZED VIEW IF NOT EXISTS target AS
-        SELECT 
-            e.id, 
-            e.search_uid, 
-            e.domain, 
-            e.data, 
-            e.type AS last_event_type, 
-            e.created AS last_event_dt,
-            c.name as name,
-            c.description as description,
-            c.meta as meta,
-            (c.meta->>'employees')::int AS employees,
-            (c.meta->>'ownership_status') AS ownership_status,
-            (c.meta->>'social_linkedin') AS linkedin,    
-            (r.data->>'rating')::int AS rating
-        FROM (
-            SELECT 
-                domain, 
-                MAX(created) AS max_created
-            FROM 
-                event
-            WHERE 
-                type NOT IN ('comment','rating','generate','criteria')
-            GROUP BY 
-                domain
-        ) AS max_event
-        JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created
-        JOIN company c ON c.domain = e.domain
-        LEFT JOIN (
-            SELECT 
-                domain, 
-                MAX(created) AS max_created
-            FROM 
-                event
-            WHERE 
-                type = 'rating'
-            GROUP BY 
-                domain
-        ) AS max_rating ON e.domain = max_rating.domain
-        LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;
-    """
-    )
-    with db.connect() as conn:
-        conn.execute(statement)
-        conn.commit()
+CREATE TABLE IF NOT EXISTS search  (
+    id SERIAL PRIMARY KEY,
+	uid INTEGER UNIQUE NOT NULL,
+    meta JSONB,
+    label VARCHAR(255) UNIQUE,
+    client_domain VARCHAR(255),
+    inclusion JSONB DEFAULT '{}'::jsonb,
+    exclusion JSONB DEFAULT '{}'::jsonb,
+    sort JSONB DEFAULT '{}'::jsonb,
+    created BIGINT NOT NULL DEFAULT FLOOR(EXTRACT(EPOCH FROM NOW())),
+    updated BIGINT NOT NULL DEFAULT FLOOR(EXTRACT(EPOCH FROM NOW()))
+);
+
+CREATE TABLE IF NOT EXISTS company (
+    id SERIAL PRIMARY KEY,
+    domain VARCHAR(255) UNIQUE NOT NULL,
+    name VARCHAR(255),
+    description TEXT,
+    meta JSONB DEFAULT '{}'::jsonb, 
+    created BIGINT NOT NULL DEFAULT FLOOR(EXTRACT(EPOCH FROM NOW())),
+    updated BIGINT NOT NULL DEFAULT FLOOR(EXTRACT(EPOCH FROM NOW()))
+
+);
+
+CREATE TABLE IF NOT EXISTS actor (
+    id SERIAL PRIMARY KEY,
+    key VARCHAR(255) UNIQUE NOT NULL,
+    type VARCHAR(255) NOT NULL,
+    name VARCHAR(255),
+    created BIGINT NOT NULL DEFAULT FLOOR(EXTRACT(EPOCH FROM NOW())),
+    updated BIGINT NOT NULL DEFAULT FLOOR(EXTRACT(EPOCH FROM NOW()))
+);
+
+
+CREATE TABLE IF NOT EXISTS event (
+    id SERIAL PRIMARY KEY,
+    search_uid INTEGER NOT NULL REFERENCES search(uid),
+    domain VARCHAR(255) REFERENCES company(domain),
+    actor_key VARCHAR(255) NOT NULL REFERENCES actor(key),
+    type VARCHAR(255) NOT NULL,
+    data JSONB DEFAULT '{}'::jsonb,
+    created BIGINT NOT NULL DEFAULT FLOOR(EXTRACT(EPOCH FROM NOW()))
+);
+
+--ALTER TABLE event ADD CONSTRAINT unique_event_type_domain_search_uid UNIQUE (type, domain, search_uid);
+
+
+CREATE TABLE IF NOT EXISTS checkpoint (
+    id SERIAL PRIMARY KEY,
+    event_id INTEGER NOT NULL REFERENCES event(id),
+    created BIGINT NOT NULL DEFAULT FLOOR(EXTRACT(EPOCH FROM NOW()))
+);
+
+CREATE MATERIALIZED VIEW IF NOT EXISTS target AS
+SELECT 
+    e.id, 
+    e.search_uid, 
+    e.domain, 
+    e.data, 
+    e.type AS last_event_type, 
+    e.created AS last_event_dt,
+    c.name as name,
+    c.description as description,
+    c.meta as meta,
+    (c.meta->>'employees')::int AS employees,
+    (c.meta->>'ownership_status') AS ownership_status,
+    (c.meta->>'social_linkedin') AS linkedin,    
+    (r.data->>'rating')::int AS rating
+FROM (
+    SELECT 
+        domain, 
+        MAX(created) AS max_created
+    FROM 
+        event
+    WHERE 
+        type NOT IN ('comment','rating','generate','criteria')
+    GROUP BY 
+        domain
+) AS max_event
+JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created
+JOIN company c ON c.domain = e.domain
+LEFT JOIN (
+    SELECT 
+        domain, 
+        MAX(created) AS max_created
+    FROM 
+        event
+    WHERE 
+        type = 'rating'
+    GROUP BY 
+        domain
+) AS max_rating ON e.domain = max_rating.domain
+LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;
 
-
-if __name__ == "__main__":
-    create_db()
```

### Comparing `gandai-1.1.4/gandai/migrations/db_seed.py` & `gandai-1.1.5/gandai/migrations/db_seed.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,14 +1,29 @@
 from gandai import query
 from gandai.models import Company, Actor, Search, Event
-from dotenv import load_dotenv
 
-load_dotenv()
+def seed_actors():
+    actors = {
+        "7138248581": "Parker",
+        "6508620943": "Gabe",
+        "9413500954": "Skye",
+        "3102835279": "Chris",
+        "5126571681": "Brandon",
+        "5125659474": "Jack",
+        "4805706789": "Eli",
+        "grata": "Grata Bot",
+        "dealcloud": "DealCloud Bot",
+        "chatgpt": "ChatGPT",
+    }
 
-def seed_db():
+    for key, name in actors.items():
+        actor = query.insert_actor(Actor(key=key, type="research", name=name))
+        print(f"Added: {actor}")
+
+def seed_hello_world():
     search = query.insert_search(
         Search(
             uid=1,
             client_domain="parkerholcomb.com",
             label="Hello World",
             meta={"research": "Parker", "status": "In Progress"},
             inclusion={
@@ -17,47 +32,14 @@
                 "country": ["USA"],
             },
             exclusion={"keywords": [], "state": []},
             sort={"field": "domain", "order": "desc"},
         )
     )
 
-
-    search = query.insert_search(
-        Search(
-            uid=13728594,
-            client_domain="comvest.com",
-            label="Comvest - Renovation Brands Add-On",
-            meta={"research": "Chris", "status": "In Progress"},
-            inclusion={
-                "keywords": ["renovation", "home improvement", "home renovation"],
-                "employees_range": [0, 100],
-                "country": ["USA"],
-            },
-            exclusion={"keywords": ["farms"], "state": ["CA"]},
-            sort={"field": "domain", "order": "desc"},
-        )
-    )
-
-    actors = {
-        "7138248581": "Parker",
-        "6508620943": "Gabe",
-        "9413500954": "Skye",
-        "3102835279": "Chris",
-        "5126571681": "Brandon",
-        "5125659474": "Jack",
-        "4805706789": "Eli",
-        "grata": "Grata Bot",
-        "dealcloud": "DealCloud Bot",
-        "chatgpt": "ChatGPT",
-    }
-
-    for key, name in actors.items():
-        actor = query.insert_actor(Actor(key=key, type="research", name=name))
-
     company = query.insert_company(
         Company(
             domain="grata.com",
             name="Grata",
             description="Grata is a thing.",
         )
     )
@@ -67,10 +49,14 @@
             search_uid=search.uid,
             domain=company.domain,
             actor_key="7138248581",
             type="create",
         )
     )
 
+def main():
+    seed_actors()
+    seed_hello_world()
+    
 
 if __name__ == "__main__":
-    seed_db()
+    main()
```

### Comparing `gandai-1.1.4/gandai/models.py` & `gandai-1.1.5/gandai/models.py`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/query.py` & `gandai-1.1.5/gandai/query.py`

 * *Files identical despite different names*

### Comparing `gandai-1.1.4/gandai/sources.py` & `gandai-1.1.5/gandai/sources.py`

 * *Files identical despite different names*

