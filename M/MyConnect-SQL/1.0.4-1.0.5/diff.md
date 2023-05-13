# Comparing `tmp/MyConnect - SQL-1.0.4.tar.gz` & `tmp/MyConnect - SQL-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MyConnect - SQL-1.0.4.tar", last modified: Sat May 13 21:13:00 2023, max compression
+gzip compressed data, was "MyConnect - SQL-1.0.5.tar", last modified: Sat May 13 21:25:24 2023, max compression
```

## Comparing `MyConnect - SQL-1.0.4.tar` & `MyConnect - SQL-1.0.5.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 21:13:00.005901 MyConnect - SQL-1.0.4/
-drwxrwxrwx   0        0        0        0 2023-05-13 21:12:59.948255 MyConnect - SQL-1.0.4/MyConnect/
--rw-rw-rw-   0        0        0     6439 2023-05-13 21:12:37.000000 MyConnect - SQL-1.0.4/MyConnect/AuthLogin.py
--rw-rw-rw-   0        0        0      544 2023-05-13 21:11:26.000000 MyConnect - SQL-1.0.4/MyConnect/moduleTest.py
--rw-rw-rw-   0        0        0        0 2023-05-13 21:09:51.000000 MyConnect - SQL-1.0.4/MyConnect/user.py
-drwxrwxrwx   0        0        0        0 2023-05-13 21:12:59.907056 MyConnect - SQL-1.0.4/MyConnect/venv/
-drwxrwxrwx   0        0        0        0 2023-05-13 21:12:59.950257 MyConnect - SQL-1.0.4/MyConnect/venv/Scripts/
--rw-rw-rw-   0        0        0     1169 2023-05-13 19:48:27.000000 MyConnect - SQL-1.0.4/MyConnect/venv/Scripts/activate_this.py
-drwxrwxrwx   0        0        0        0 2023-05-13 21:12:59.996903 MyConnect - SQL-1.0.4/MyConnect_SQL.egg-info/
--rw-rw-rw-   0        0        0      590 2023-05-13 21:12:59.000000 MyConnect - SQL-1.0.4/MyConnect_SQL.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      271 2023-05-13 21:12:59.000000 MyConnect - SQL-1.0.4/MyConnect_SQL.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 21:12:59.000000 MyConnect - SQL-1.0.4/MyConnect_SQL.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       10 2023-05-13 21:12:59.000000 MyConnect - SQL-1.0.4/MyConnect_SQL.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      592 2023-05-13 21:12:59.999884 MyConnect - SQL-1.0.4/PKG-INFO
--rw-rw-rw-   0        0        0      896 2023-05-13 16:40:01.000000 MyConnect - SQL-1.0.4/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 21:13:00.005901 MyConnect - SQL-1.0.4/setup.cfg
--rw-rw-rw-   0        0        0      687 2023-05-13 21:09:24.000000 MyConnect - SQL-1.0.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:25:24.185203 MyConnect - SQL-1.0.5/
+drwxrwxrwx   0        0        0        0 2023-05-13 21:25:24.098176 MyConnect - SQL-1.0.5/MyConnect/
+-rw-rw-rw-   0        0        0     6427 2023-05-13 21:25:13.000000 MyConnect - SQL-1.0.5/MyConnect/AuthLogin.py
+-rw-rw-rw-   0        0        0      544 2023-05-13 21:11:26.000000 MyConnect - SQL-1.0.5/MyConnect/moduleTest.py
+-rw-rw-rw-   0        0        0        0 2023-05-13 21:09:51.000000 MyConnect - SQL-1.0.5/MyConnect/user.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:25:24.063658 MyConnect - SQL-1.0.5/MyConnect/venv/
+drwxrwxrwx   0        0        0        0 2023-05-13 21:25:24.103189 MyConnect - SQL-1.0.5/MyConnect/venv/Scripts/
+-rw-rw-rw-   0        0        0     1169 2023-05-13 19:48:27.000000 MyConnect - SQL-1.0.5/MyConnect/venv/Scripts/activate_this.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:25:24.178677 MyConnect - SQL-1.0.5/MyConnect_SQL.egg-info/
+-rw-rw-rw-   0        0        0      590 2023-05-13 21:25:24.000000 MyConnect - SQL-1.0.5/MyConnect_SQL.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      271 2023-05-13 21:25:24.000000 MyConnect - SQL-1.0.5/MyConnect_SQL.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 21:25:24.000000 MyConnect - SQL-1.0.5/MyConnect_SQL.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 21:25:24.000000 MyConnect - SQL-1.0.5/MyConnect_SQL.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      592 2023-05-13 21:25:24.183205 MyConnect - SQL-1.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0      896 2023-05-13 16:40:01.000000 MyConnect - SQL-1.0.5/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 21:25:24.186203 MyConnect - SQL-1.0.5/setup.cfg
+-rw-rw-rw-   0        0        0      687 2023-05-13 21:24:42.000000 MyConnect - SQL-1.0.5/setup.py
```

### Comparing `MyConnect - SQL-1.0.4/MyConnect/AuthLogin.py` & `MyConnect - SQL-1.0.5/MyConnect/AuthLogin.py`

 * *Files 5% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from tkinter import *
 from tkinter import messagebox
 import mysql.connector as MC 
 from mysql.connector import errorcode
 
 # Var
 
-u1 = open("user.py", "r")
+u1 = open("user.txt", "r")
 
 global lg
 global LoginFrame
 lg = Tk()
 LoginFrame = Frame(lg, width=350, height=350, bg="white")
 
 # Def
@@ -137,16 +137,16 @@
                         query='select * from '+Table+' where '+TableUser+'=%s and '+TablePassword+'=%s'
                         cursor.execute(query ,(username ,password))
                         row = cursor.fetchone()
                         if row == None:
                             messagebox.showerror('Login', 'Invalid username or/and password')
                         else:
                             messagebox.showinfo('Succes', 'Login is sucessful')
-                            u1 = open("user.py", "w+")
-                            u1.write("username = "+username)
+                            u1 = open("user.txt", "w+")
+                            u1.write(username)
                             u1.close()
                             print("Welcome "+username)
                     except MC.Error as err:
                         messagebox.showerror("MySQL Error", err)
```

### Comparing `MyConnect - SQL-1.0.4/MyConnect/moduleTest.py` & `MyConnect - SQL-1.0.5/MyConnect/moduleTest.py`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.4/MyConnect/venv/Scripts/activate_this.py` & `MyConnect - SQL-1.0.5/MyConnect/venv/Scripts/activate_this.py`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.4/MyConnect_SQL.egg-info/PKG-INFO` & `MyConnect - SQL-1.0.5/MyConnect_SQL.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyConnect-SQL
-Version: 1.0.4
+Version: 1.0.5
 Summary: Auth Login simplifies the creation of login page and account creation.
 Home-page: https://github.com/Rayanis55/AuthLogin
 Author: Venorix - Rayanis55
 License: MIT
 Requires-Python: >=3.0
 
 Auth Login simplifies the creation of login page and account creation.         AuthLogin is a module that facilitates the creation of login and registration pages     The module is rather a simplification because if we can say that it compresses     the tkinter variables (That's why you have to put a login.loop() at the end).
```

### Comparing `MyConnect - SQL-1.0.4/PKG-INFO` & `MyConnect - SQL-1.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyConnect - SQL
-Version: 1.0.4
+Version: 1.0.5
 Summary: Auth Login simplifies the creation of login page and account creation.
 Home-page: https://github.com/Rayanis55/AuthLogin
 Author: Venorix - Rayanis55
 License: MIT
 Requires-Python: >=3.0
 
 Auth Login simplifies the creation of login page and account creation.         AuthLogin is a module that facilitates the creation of login and registration pages     The module is rather a simplification because if we can say that it compresses     the tkinter variables (That's why you have to put a login.loop() at the end).
```

### Comparing `MyConnect - SQL-1.0.4/README.md` & `MyConnect - SQL-1.0.5/README.md`

 * *Files identical despite different names*

### Comparing `MyConnect - SQL-1.0.4/setup.py` & `MyConnect - SQL-1.0.5/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
   name = "MyConnect - SQL",
-  version = "1.0.4",
+  version = "1.0.5",
   author="Venorix - Rayanis55",
   license='MIT',
   description='Auth Login simplifies the creation of login page and account creation.',
   long_description="Auth Login simplifies the creation of login page and account creation. \
     \
     AuthLogin is a module that facilitates the creation of login and registration pages \
     The module is rather a simplification because if we can say that it compresses \
```

