# Comparing `tmp/flapgui-0.2.0.tar.gz` & `tmp/flapgui-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "flapgui-0.2.0.tar", last modified: Sat May 13 14:31:10 2023, max compression
+gzip compressed data, was "flapgui-0.2.1.tar", last modified: Sat May 13 14:32:50 2023, max compression
```

## Comparing `flapgui-0.2.0.tar` & `flapgui-0.2.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:31:10.158078 flapgui-0.2.0/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.2.0/LICENSE
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:31:10.157667 flapgui-0.2.0/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6181 2023-05-13 10:49:01.000000 flapgui-0.2.0/README.md
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 14:30:38.000000 flapgui-0.2.0/pyproject.toml
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 14:31:10.158194 flapgui-0.2.0/setup.cfg
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:31:10.095895 flapgui-0.2.0/src/
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:31:10.116697 flapgui-0.2.0/src/flapgui/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     7580 2023-05-13 14:26:22.000000 flapgui-0.2.0/src/flapgui/__init__.py
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:31:10.156700 flapgui-0.2.0/src/flapgui.egg-info/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:31:10.000000 flapgui-0.2.0/src/flapgui.egg-info/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 14:31:10.000000 flapgui-0.2.0/src/flapgui.egg-info/SOURCES.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 14:31:10.000000 flapgui-0.2.0/src/flapgui.egg-info/dependency_links.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 14:31:10.000000 flapgui-0.2.0/src/flapgui.egg-info/top_level.txt
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:32:50.012355 flapgui-0.2.1/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.2.1/LICENSE
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6733 2023-05-13 14:32:50.011967 flapgui-0.2.1/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6192 2023-05-13 14:32:32.000000 flapgui-0.2.1/README.md
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 14:32:15.000000 flapgui-0.2.1/pyproject.toml
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 14:32:50.012480 flapgui-0.2.1/setup.cfg
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:32:49.970456 flapgui-0.2.1/src/
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:32:49.973473 flapgui-0.2.1/src/flapgui/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     7580 2023-05-13 14:26:22.000000 flapgui-0.2.1/src/flapgui/__init__.py
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:32:50.010922 flapgui-0.2.1/src/flapgui.egg-info/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6733 2023-05-13 14:32:49.000000 flapgui-0.2.1/src/flapgui.egg-info/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 14:32:49.000000 flapgui-0.2.1/src/flapgui.egg-info/SOURCES.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 14:32:49.000000 flapgui-0.2.1/src/flapgui.egg-info/dependency_links.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 14:32:49.000000 flapgui-0.2.1/src/flapgui.egg-info/top_level.txt
```

### Comparing `flapgui-0.2.0/LICENSE` & `flapgui-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `flapgui-0.2.0/PKG-INFO` & `flapgui-0.2.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flapgui
-Version: 0.2.0
+Version: 0.2.1
 Summary: Easy-to-use and cross-platform GUI library for making functional GUI apps
 Author-email: WinFan3672 <winfan3672@gmail.com>
 Project-URL: Homepage, https://github.com/WinFan3672/Flap
 Project-URL: Bug Tracker, https://github.com/WinFan3672/Flap/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -17,15 +17,15 @@
 # Purpose
 FlapGUI is designed to make writing GUI applications as simple as possible, eliminating the learning curve for making functional programs. 
 
 Most GUI frameworks (tkinter, qt, gtk, etc.) have a steep learning curve, which FlapGUI intends to fix.
 
 **Flap is an Alpha framework and is not complete. It is subject to rapid and signigicant change at the moment.**
 
-# Tutorial
+# Tutorial (Outdated)
 This section explains how to make applications using FlapGUI.
 ## Installing
 To install it, simply run:  
 ```
 pip install flapgui
 ```
 ## Importing
```

### Comparing `flapgui-0.2.0/README.md` & `flapgui-0.2.1/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 # Purpose
 FlapGUI is designed to make writing GUI applications as simple as possible, eliminating the learning curve for making functional programs. 
 
 Most GUI frameworks (tkinter, qt, gtk, etc.) have a steep learning curve, which FlapGUI intends to fix.
 
 **Flap is an Alpha framework and is not complete. It is subject to rapid and signigicant change at the moment.**
 
-# Tutorial
+# Tutorial (Outdated)
 This section explains how to make applications using FlapGUI.
 ## Installing
 To install it, simply run:  
 ```
 pip install flapgui
 ```
 ## Importing
```

### Comparing `flapgui-0.2.0/pyproject.toml` & `flapgui-0.2.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "flapgui"
-version = "0.2.0"
+version = "0.2.1"
 authors = [
   { name="WinFan3672", email="winfan3672@gmail.com" },
 ]
 description = "Easy-to-use and cross-platform GUI library for making functional GUI apps"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `flapgui-0.2.0/src/flapgui/__init__.py` & `flapgui-0.2.1/src/flapgui/__init__.py`

 * *Files identical despite different names*

### Comparing `flapgui-0.2.0/src/flapgui.egg-info/PKG-INFO` & `flapgui-0.2.1/src/flapgui.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flapgui
-Version: 0.2.0
+Version: 0.2.1
 Summary: Easy-to-use and cross-platform GUI library for making functional GUI apps
 Author-email: WinFan3672 <winfan3672@gmail.com>
 Project-URL: Homepage, https://github.com/WinFan3672/Flap
 Project-URL: Bug Tracker, https://github.com/WinFan3672/Flap/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -17,15 +17,15 @@
 # Purpose
 FlapGUI is designed to make writing GUI applications as simple as possible, eliminating the learning curve for making functional programs. 
 
 Most GUI frameworks (tkinter, qt, gtk, etc.) have a steep learning curve, which FlapGUI intends to fix.
 
 **Flap is an Alpha framework and is not complete. It is subject to rapid and signigicant change at the moment.**
 
-# Tutorial
+# Tutorial (Outdated)
 This section explains how to make applications using FlapGUI.
 ## Installing
 To install it, simply run:  
 ```
 pip install flapgui
 ```
 ## Importing
```

