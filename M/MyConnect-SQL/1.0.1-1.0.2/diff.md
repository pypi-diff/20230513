# Comparing `tmp/MyConnect - SQL-1.0.1.tar.gz` & `tmp/MyConnect - SQL-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MyConnect - SQL-1.0.1.tar", last modified: Sat May 13 19:59:25 2023, max compression
+gzip compressed data, was "MyConnect - SQL-1.0.2.tar", last modified: Sat May 13 21:01:13 2023, max compression
```

## Comparing `MyConnect - SQL-1.0.1.tar` & `MyConnect - SQL-1.0.2.tar`

### file list

```diff
@@ -1,17 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 19:59:25.968793 MyConnect - SQL-1.0.1/
-drwxrwxrwx   0        0        0        0 2023-05-13 19:59:25.700210 MyConnect - SQL-1.0.1/MyConnect/
--rw-rw-rw-   0        0        0     6355 2023-05-13 19:48:26.000000 MyConnect - SQL-1.0.1/MyConnect/AuthLogin.py
--rw-rw-rw-   0        0        0      471 2023-05-13 19:48:26.000000 MyConnect - SQL-1.0.1/MyConnect/moduleTest.py
--rw-rw-rw-   0        0        0      130 2023-05-13 19:48:27.000000 MyConnect - SQL-1.0.1/MyConnect/root.py
-drwxrwxrwx   0        0        0        0 2023-05-13 19:59:25.585554 MyConnect - SQL-1.0.1/MyConnect/venv/
-drwxrwxrwx   0        0        0        0 2023-05-13 19:59:25.710726 MyConnect - SQL-1.0.1/MyConnect/venv/Scripts/
--rw-rw-rw-   0        0        0     1169 2023-05-13 19:48:27.000000 MyConnect - SQL-1.0.1/MyConnect/venv/Scripts/activate_this.py
-drwxrwxrwx   0        0        0        0 2023-05-13 19:59:25.962799 MyConnect - SQL-1.0.1/MyConnect_SQL.egg-info/
--rw-rw-rw-   0        0        0      590 2023-05-13 19:59:25.000000 MyConnect - SQL-1.0.1/MyConnect_SQL.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      271 2023-05-13 19:59:25.000000 MyConnect - SQL-1.0.1/MyConnect_SQL.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 19:59:25.000000 MyConnect - SQL-1.0.1/MyConnect_SQL.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 19:59:25.000000 MyConnect - SQL-1.0.1/MyConnect_SQL.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      592 2023-05-13 19:59:25.966790 MyConnect - SQL-1.0.1/PKG-INFO
--rw-rw-rw-   0        0        0      896 2023-05-13 16:40:01.000000 MyConnect - SQL-1.0.1/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 19:59:25.969789 MyConnect - SQL-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0      687 2023-05-13 19:59:12.000000 MyConnect - SQL-1.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.262003 MyConnect - SQL-1.0.2/
+drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.213605 MyConnect - SQL-1.0.2/MyConnect/
+-rw-rw-rw-   0        0        0     6427 2023-05-13 20:59:14.000000 MyConnect - SQL-1.0.2/MyConnect/AuthLogin.py
+-rw-rw-rw-   0        0        0      559 2023-05-13 20:49:55.000000 MyConnect - SQL-1.0.2/MyConnect/moduleTest.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.183522 MyConnect - SQL-1.0.2/MyConnect/venv/
+drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.218605 MyConnect - SQL-1.0.2/MyConnect/venv/Scripts/
+-rw-rw-rw-   0        0        0     1169 2023-05-13 19:48:27.000000 MyConnect - SQL-1.0.2/MyConnect/venv/Scripts/activate_this.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:01:13.250438 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/
+-rw-rw-rw-   0        0        0      590 2023-05-13 21:01:13.000000 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      253 2023-05-13 21:01:13.000000 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 21:01:13.000000 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 21:01:13.000000 MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      592 2023-05-13 21:01:13.259458 MyConnect - SQL-1.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0      896 2023-05-13 16:40:01.000000 MyConnect - SQL-1.0.2/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 21:01:13.263005 MyConnect - SQL-1.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      687 2023-05-13 21:00:31.000000 MyConnect - SQL-1.0.2/setup.py
```

### Comparing `MyConnect - SQL-1.0.1/MyConnect/AuthLogin.py` & `MyConnect - SQL-1.0.2/MyConnect/AuthLogin.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,19 +1,23 @@
 # Importation
 
 from tkinter import *
 from tkinter import messagebox
-from AuthLogin.root import *
 import mysql.connector as MC 
 from mysql.connector import errorcode
 
 # Var
 
 u1 = open("user.txt", "r")
 
+global lg
+global LoginFrame
+lg = Tk()
+LoginFrame = Frame(lg, width=350, height=350, bg="white")
+
 # Def
 
 class login():
     # Windows
 
     def setTitle(title):
         lg.title(title)
```

### Comparing `MyConnect - SQL-1.0.1/MyConnect/venv/Scripts/activate_this.py` & `MyConnect - SQL-1.0.2/MyConnect/venv/Scripts/activate_this.py`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.1/MyConnect_SQL.egg-info/PKG-INFO` & `MyConnect - SQL-1.0.2/MyConnect_SQL.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyConnect-SQL
-Version: 1.0.1
+Version: 1.0.2
 Summary: Auth Login simplifies the creation of login page and account creation.
 Home-page: https://github.com/Rayanis55/AuthLogin
 Author: Venorix - Rayanis55
 License: MIT
 Requires-Python: >=3.0
 
 Auth Login simplifies the creation of login page and account creation.         AuthLogin is a module that facilitates the creation of login and registration pages     The module is rather a simplification because if we can say that it compresses     the tkinter variables (That's why you have to put a login.loop() at the end).
```

### Comparing `MyConnect - SQL-1.0.1/PKG-INFO` & `MyConnect - SQL-1.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyConnect - SQL
-Version: 1.0.1
+Version: 1.0.2
 Summary: Auth Login simplifies the creation of login page and account creation.
 Home-page: https://github.com/Rayanis55/AuthLogin
 Author: Venorix - Rayanis55
 License: MIT
 Requires-Python: >=3.0
 
 Auth Login simplifies the creation of login page and account creation.         AuthLogin is a module that facilitates the creation of login and registration pages     The module is rather a simplification because if we can say that it compresses     the tkinter variables (That's why you have to put a login.loop() at the end).
```

### Comparing `MyConnect - SQL-1.0.1/README.md` & `MyConnect - SQL-1.0.2/README.md`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.1/setup.py` & `MyConnect - SQL-1.0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
   name = "MyConnect - SQL",
-  version = "1.0.1",
+  version = "1.0.2",
   author="Venorix - Rayanis55",
   license='MIT',
   description='Auth Login simplifies the creation of login page and account creation.',
   long_description="Auth Login simplifies the creation of login page and account creation. \
     \
     AuthLogin is a module that facilitates the creation of login and registration pages \
     The module is rather a simplification because if we can say that it compresses \
```

