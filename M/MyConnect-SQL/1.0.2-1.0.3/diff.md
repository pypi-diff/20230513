# Comparing `tmp/MyConnect - SQL-1.0.2.tar.gz` & `tmp/MyConnect - SQL-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MyConnect - SQL-1.0.2.tar", last modified: Sat May 13 21:01:13 2023, max compression
+gzip compressed data, was "MyConnect - SQL-1.0.3.tar", last modified: Sat May 13 21:06:37 2023, max compression
```

## Comparing `MyConnect - SQL-1.0.2.tar` & `MyConnect - SQL-1.0.3.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.262003 MyConnect - SQL-1.0.2/
-drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.213605 MyConnect - SQL-1.0.2/MyConnect/
--rw-rw-rw-   0        0        0     6427 2023-05-13 20:59:14.000000 MyConnect - SQL-1.0.2/MyConnect/AuthLogin.py
--rw-rw-rw-   0        0        0      559 2023-05-13 20:49:55.000000 MyConnect - SQL-1.0.2/MyConnect/moduleTest.py
-drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.183522 MyConnect - SQL-1.0.2/MyConnect/venv/
-drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.218605 MyConnect - SQL-1.0.2/MyConnect/venv/Scripts/
--rw-rw-rw-   0        0        0     1169 2023-05-13 19:48:27.000000 MyConnect - SQL-1.0.2/MyConnect/venv/Scripts/activate_this.py
-drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.250438 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/
--rw-rw-rw-   0        0        0      590 2023-05-13 21:01:13.000000 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      253 2023-05-13 21:01:13.000000 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 21:01:13.000000 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 21:01:13.000000 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      592 2023-05-13 21:01:13.259458 MyConnect - SQL-1.0.2/PKG-INFO
--rw-rw-rw-   0        0        0      896 2023-05-13 16:40:01.000000 MyConnect - SQL-1.0.2/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 21:01:13.263005 MyConnect - SQL-1.0.2/setup.cfg
--rw-rw-rw-   0        0        0      687 2023-05-13 21:00:31.000000 MyConnect - SQL-1.0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.208956 MyConnect - SQL-1.0.3/
+drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.144616 MyConnect - SQL-1.0.3/MyConnect/
+-rw-rw-rw-   0        0        0     6427 2023-05-13 21:05:42.000000 MyConnect - SQL-1.0.3/MyConnect/AuthLogin.py
+-rw-rw-rw-   0        0        0      559 2023-05-13 20:49:55.000000 MyConnect - SQL-1.0.3/MyConnect/moduleTest.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.117541 MyConnect - SQL-1.0.3/MyConnect/venv/
+drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.150137 MyConnect - SQL-1.0.3/MyConnect/venv/Scripts/
+-rw-rw-rw-   0        0        0     1169 2023-05-13 19:48:27.000000 MyConnect - SQL-1.0.3/MyConnect/venv/Scripts/activate_this.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.196957 MyConnect - SQL-1.0.3/MyConnect_SQL.egg-info/
+-rw-rw-rw-   0        0        0      590 2023-05-13 21:06:37.000000 MyConnect - SQL-1.0.3/MyConnect_SQL.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      253 2023-05-13 21:06:37.000000 MyConnect - SQL-1.0.3/MyConnect_SQL.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 21:06:37.000000 MyConnect - SQL-1.0.3/MyConnect_SQL.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 21:06:37.000000 MyConnect - SQL-1.0.3/MyConnect_SQL.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      592 2023-05-13 21:06:37.201949 MyConnect - SQL-1.0.3/PKG-INFO
+-rw-rw-rw-   0        0        0      896 2023-05-13 16:40:01.000000 MyConnect - SQL-1.0.3/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 21:06:37.208956 MyConnect - SQL-1.0.3/setup.cfg
+-rw-rw-rw-   0        0        0      687 2023-05-13 21:06:33.000000 MyConnect - SQL-1.0.3/setup.py
```

### Comparing `MyConnect - SQL-1.0.2/MyConnect/AuthLogin.py` & `MyConnect - SQL-1.0.3/MyConnect/AuthLogin.py`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.2/MyConnect/moduleTest.py` & `MyConnect - SQL-1.0.3/MyConnect/moduleTest.py`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.2/MyConnect/venv/Scripts/activate_this.py` & `MyConnect - SQL-1.0.3/MyConnect/venv/Scripts/activate_this.py`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/PKG-INFO` & `MyConnect - SQL-1.0.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: MyConnect-SQL
-Version: 1.0.2
+Name: MyConnect - SQL
+Version: 1.0.3
 Summary: Auth Login simplifies the creation of login page and account creation.
 Home-page: https://github.com/Rayanis55/AuthLogin
 Author: Venorix - Rayanis55
 License: MIT
 Requires-Python: >=3.0
 
 Auth Login simplifies the creation of login page and account creation.         AuthLogin is a module that facilitates the creation of login and registration pages     The module is rather a simplification because if we can say that it compresses     the tkinter variables (That's why you have to put a login.loop() at the end).
```

### Comparing `MyConnect - SQL-1.0.2/PKG-INFO` & `MyConnect - SQL-1.0.3/MyConnect_SQL.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: MyConnect - SQL
-Version: 1.0.2
+Name: MyConnect-SQL
+Version: 1.0.3
 Summary: Auth Login simplifies the creation of login page and account creation.
 Home-page: https://github.com/Rayanis55/AuthLogin
 Author: Venorix - Rayanis55
 License: MIT
 Requires-Python: >=3.0
 
 Auth Login simplifies the creation of login page and account creation.         AuthLogin is a module that facilitates the creation of login and registration pages     The module is rather a simplification because if we can say that it compresses     the tkinter variables (That's why you have to put a login.loop() at the end).
```

### Comparing `MyConnect - SQL-1.0.2/README.md` & `MyConnect - SQL-1.0.3/README.md`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.2/setup.py` & `MyConnect - SQL-1.0.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
   name = "MyConnect - SQL",
-  version = "1.0.2",
+  version = "1.0.3",
   author="Venorix - Rayanis55",
   license='MIT',
   description='Auth Login simplifies the creation of login page and account creation.',
   long_description="Auth Login simplifies the creation of login page and account creation. \
     \
     AuthLogin is a module that facilitates the creation of login and registration pages \
     The module is rather a simplification because if we can say that it compresses \
```

