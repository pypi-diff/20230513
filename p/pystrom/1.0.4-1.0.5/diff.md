# Comparing `tmp/pystrom-1.0.4.tar.gz` & `tmp/pystrom-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pystrom-1.0.4.tar", last modified: Thu Feb  4 11:59:21 2021, max compression
+gzip compressed data, was "pystrom-1.0.5.tar", last modified: Sat May 13 20:26:10 2023, max compression
```

## Comparing `pystrom-1.0.4.tar` & `pystrom-1.0.5.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (116)        0 2021-02-04 11:59:21.097100 pystrom-1.0.4/
--rw-r--r--   0 runner    (1001) docker     (116)     1055 2021-02-04 11:58:59.000000 pystrom-1.0.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (116)       62 2021-02-04 11:58:59.000000 pystrom-1.0.4/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (116)     1784 2021-02-04 11:59:21.097100 pystrom-1.0.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (116)      802 2021-02-04 11:58:59.000000 pystrom-1.0.4/README.md
-drwxr-xr-x   0 runner    (1001) docker     (116)        0 2021-02-04 11:59:21.097100 pystrom-1.0.4/pystrom/
--rw-r--r--   0 runner    (1001) docker     (116)        0 2021-02-04 11:58:59.000000 pystrom-1.0.4/pystrom/__init__.py
--rw-r--r--   0 runner    (1001) docker     (116)      176 2021-02-04 11:58:59.000000 pystrom-1.0.4/pystrom/__main__.py
--rw-r--r--   0 runner    (1001) docker     (116)     1394 2021-02-04 11:58:59.000000 pystrom-1.0.4/pystrom/console.py
--rw-r--r--   0 runner    (1001) docker     (116)     2454 2021-02-04 11:58:59.000000 pystrom-1.0.4/pystrom/device.py
--rw-r--r--   0 runner    (1001) docker     (116)     1610 2021-02-04 11:58:59.000000 pystrom-1.0.4/pystrom/search.py
--rw-r--r--   0 runner    (1001) docker     (116)      262 2021-02-04 11:58:59.000000 pystrom-1.0.4/pystrom/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (116)        0 2021-02-04 11:59:21.097100 pystrom-1.0.4/pystrom.egg-info/
--rw-r--r--   0 runner    (1001) docker     (116)     1784 2021-02-04 11:59:19.000000 pystrom-1.0.4/pystrom.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (116)      314 2021-02-04 11:59:20.000000 pystrom-1.0.4/pystrom.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (116)        1 2021-02-04 11:59:19.000000 pystrom-1.0.4/pystrom.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (116)       46 2021-02-04 11:59:19.000000 pystrom-1.0.4/pystrom.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (116)        8 2021-02-04 11:59:19.000000 pystrom-1.0.4/pystrom.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (116)     1039 2021-02-04 11:59:21.097100 pystrom-1.0.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (116)       38 2021-02-04 11:58:59.000000 pystrom-1.0.4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:26:10.347730 pystrom-1.0.5/
+-rw-r--r--   0 runner    (1001) docker     (123)     1055 2023-05-13 20:26:00.000000 pystrom-1.0.5/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       62 2023-05-13 20:26:00.000000 pystrom-1.0.5/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1607 2023-05-13 20:26:10.347730 pystrom-1.0.5/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      802 2023-05-13 20:26:00.000000 pystrom-1.0.5/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:26:10.347730 pystrom-1.0.5/pystrom/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 20:26:00.000000 pystrom-1.0.5/pystrom/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      176 2023-05-13 20:26:00.000000 pystrom-1.0.5/pystrom/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1394 2023-05-13 20:26:00.000000 pystrom-1.0.5/pystrom/console.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2458 2023-05-13 20:26:00.000000 pystrom-1.0.5/pystrom/device.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1610 2023-05-13 20:26:00.000000 pystrom-1.0.5/pystrom/search.py
+-rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-13 20:26:00.000000 pystrom-1.0.5/pystrom/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:26:10.347730 pystrom-1.0.5/pystrom.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1607 2023-05-13 20:26:10.000000 pystrom-1.0.5/pystrom.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      314 2023-05-13 20:26:10.000000 pystrom-1.0.5/pystrom.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 20:26:10.000000 pystrom-1.0.5/pystrom.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       46 2023-05-13 20:26:10.000000 pystrom-1.0.5/pystrom.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 20:26:10.000000 pystrom-1.0.5/pystrom.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1039 2023-05-13 20:26:10.347730 pystrom-1.0.5/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 20:26:00.000000 pystrom-1.0.5/setup.py
```

### Comparing `pystrom-1.0.4/LICENSE` & `pystrom-1.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `pystrom-1.0.4/PKG-INFO` & `pystrom-1.0.5/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,43 +1,43 @@
 Metadata-Version: 2.1
 Name: pystrom
-Version: 1.0.4
+Version: 1.0.5
 Summary: Unoffizielle MyStrom-Steuerung
 Home-page: https://github.com/rafaelurben/python-mystrom
 Author: Rafael Urben
 Author-email: github@rafaelurben.ch
 Maintainer: Rafael Urben
 Maintainer-email: github@rafaelurben.ch
 License: MIT
 Project-URL: GitHub, https://github.com/rafaelurben/python-mystrom
 Project-URL: Issues, https://github.com/rafaelurben/python-mystrom/issues
-Description: # python-mystrom aka. pystrom
-        
-        Dies ist eine unoffizielle Python-Integration für die Steuerung von lokalen MyStrom-Geräten.
-        
-        Dieses Projekt ist noch sehr neu und hat deshalb noch nicht sehr viele Features.
-        
-        HINWEIS: Dieses Projekt wird nicht von [MyStrom](https://mystrom.ch) entwickelt und steht auch nicht damit in Verbindung.
-        
-        ## Installation
-        
-        Die Installation benötigt [Python](https://www.python.org/downloads/) sowie [Pip](https://pip.pypa.io/en/stable/installing/#installing-with-get-pip-py).
-        
-        `python -m pip install -U pip pystrom`
-        
-        ## Features
-        
-        ### Konsolen-Befehle
-        
-        | Befehl                     | Funktion                                 |
-        | -------------------------- | ---------------------------------------- |
-        | `python -m pystrom search` | Suche MyStrom-Geräte im lokalen Netzwerk |
-        
-Platform: UNKNOWN
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
+License-File: LICENSE
+
+# python-mystrom aka. pystrom
+
+Dies ist eine unoffizielle Python-Integration für die Steuerung von lokalen MyStrom-Geräten.
+
+Dieses Projekt ist noch sehr neu und hat deshalb noch nicht sehr viele Features.
+
+HINWEIS: Dieses Projekt wird nicht von [MyStrom](https://mystrom.ch) entwickelt und steht auch nicht damit in Verbindung.
+
+## Installation
+
+Die Installation benötigt [Python](https://www.python.org/downloads/) sowie [Pip](https://pip.pypa.io/en/stable/installing/#installing-with-get-pip-py).
+
+`python -m pip install -U pip pystrom`
+
+## Features
+
+### Konsolen-Befehle
+
+| Befehl                     | Funktion                                 |
+| -------------------------- | ---------------------------------------- |
+| `python -m pystrom search` | Suche MyStrom-Geräte im lokalen Netzwerk |
```

### Comparing `pystrom-1.0.4/README.md` & `pystrom-1.0.5/README.md`

 * *Files identical despite different names*

### Comparing `pystrom-1.0.4/pystrom/console.py` & `pystrom-1.0.5/pystrom/console.py`

 * *Files identical despite different names*

### Comparing `pystrom-1.0.4/pystrom/device.py` & `pystrom-1.0.5/pystrom/device.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,15 +38,15 @@
             return cls.all_devices[mac]
 
     @property
     def type_name(self):
         if self.device_type in self.DEVICE_TYPES:
             return self.DEVICE_TYPES[self.device_type]
         else:
-            return "Non-MyStrom-Device ("+self.device_type+")"
+            return f"Non-MyStrom-Device ({str(self.device_type)})"
 
 
     def __str__(self):
         return f"<MyStromDevice '{self.type_name}' {self.mac} @ {self.ip}>"
 
     # API General
```

### Comparing `pystrom-1.0.4/pystrom/search.py` & `pystrom-1.0.5/pystrom/search.py`

 * *Files identical despite different names*

### Comparing `pystrom-1.0.4/pystrom.egg-info/PKG-INFO` & `pystrom-1.0.5/pystrom.egg-info/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,43 +1,43 @@
 Metadata-Version: 2.1
 Name: pystrom
-Version: 1.0.4
+Version: 1.0.5
 Summary: Unoffizielle MyStrom-Steuerung
 Home-page: https://github.com/rafaelurben/python-mystrom
 Author: Rafael Urben
 Author-email: github@rafaelurben.ch
 Maintainer: Rafael Urben
 Maintainer-email: github@rafaelurben.ch
 License: MIT
 Project-URL: GitHub, https://github.com/rafaelurben/python-mystrom
 Project-URL: Issues, https://github.com/rafaelurben/python-mystrom/issues
-Description: # python-mystrom aka. pystrom
-        
-        Dies ist eine unoffizielle Python-Integration für die Steuerung von lokalen MyStrom-Geräten.
-        
-        Dieses Projekt ist noch sehr neu und hat deshalb noch nicht sehr viele Features.
-        
-        HINWEIS: Dieses Projekt wird nicht von [MyStrom](https://mystrom.ch) entwickelt und steht auch nicht damit in Verbindung.
-        
-        ## Installation
-        
-        Die Installation benötigt [Python](https://www.python.org/downloads/) sowie [Pip](https://pip.pypa.io/en/stable/installing/#installing-with-get-pip-py).
-        
-        `python -m pip install -U pip pystrom`
-        
-        ## Features
-        
-        ### Konsolen-Befehle
-        
-        | Befehl                     | Funktion                                 |
-        | -------------------------- | ---------------------------------------- |
-        | `python -m pystrom search` | Suche MyStrom-Geräte im lokalen Netzwerk |
-        
-Platform: UNKNOWN
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
+License-File: LICENSE
+
+# python-mystrom aka. pystrom
+
+Dies ist eine unoffizielle Python-Integration für die Steuerung von lokalen MyStrom-Geräten.
+
+Dieses Projekt ist noch sehr neu und hat deshalb noch nicht sehr viele Features.
+
+HINWEIS: Dieses Projekt wird nicht von [MyStrom](https://mystrom.ch) entwickelt und steht auch nicht damit in Verbindung.
+
+## Installation
+
+Die Installation benötigt [Python](https://www.python.org/downloads/) sowie [Pip](https://pip.pypa.io/en/stable/installing/#installing-with-get-pip-py).
+
+`python -m pip install -U pip pystrom`
+
+## Features
+
+### Konsolen-Befehle
+
+| Befehl                     | Funktion                                 |
+| -------------------------- | ---------------------------------------- |
+| `python -m pystrom search` | Suche MyStrom-Geräte im lokalen Netzwerk |
```

### Comparing `pystrom-1.0.4/setup.cfg` & `pystrom-1.0.5/setup.cfg`

 * *Files identical despite different names*

