# Comparing `tmp/flapgui-0.0.4.tar.gz` & `tmp/flapgui-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "flapgui-0.0.4.tar", last modified: Sat May 13 14:17:34 2023, max compression
+gzip compressed data, was "flapgui-0.1.0.tar", last modified: Sat May 13 14:19:27 2023, max compression
```

## Comparing `flapgui-0.0.4.tar` & `flapgui-0.1.0.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:17:34.761965 flapgui-0.0.4/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.0.4/LICENSE
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:17:34.761525 flapgui-0.0.4/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6181 2023-05-13 10:49:01.000000 flapgui-0.0.4/README.md
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 12:10:31.000000 flapgui-0.0.4/pyproject.toml
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 14:17:34.762091 flapgui-0.0.4/setup.cfg
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:17:34.710956 flapgui-0.0.4/src/
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:17:34.755103 flapgui-0.0.4/src/flapgui/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     7579 2023-05-13 13:47:33.000000 flapgui-0.0.4/src/flapgui/__init__.py
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:17:34.760451 flapgui-0.0.4/src/flapgui.egg-info/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:17:34.000000 flapgui-0.0.4/src/flapgui.egg-info/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 14:17:34.000000 flapgui-0.0.4/src/flapgui.egg-info/SOURCES.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 14:17:34.000000 flapgui-0.0.4/src/flapgui.egg-info/dependency_links.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 14:17:34.000000 flapgui-0.0.4/src/flapgui.egg-info/top_level.txt
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:19:27.880889 flapgui-0.1.0/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.1.0/LICENSE
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:19:27.880420 flapgui-0.1.0/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6181 2023-05-13 10:49:01.000000 flapgui-0.1.0/README.md
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 14:19:04.000000 flapgui-0.1.0/pyproject.toml
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 14:19:27.881013 flapgui-0.1.0/setup.cfg
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:19:27.839173 flapgui-0.1.0/src/
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:19:27.875650 flapgui-0.1.0/src/flapgui/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     7579 2023-05-13 14:19:12.000000 flapgui-0.1.0/src/flapgui/__init__.py
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:19:27.879210 flapgui-0.1.0/src/flapgui.egg-info/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:19:27.000000 flapgui-0.1.0/src/flapgui.egg-info/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 14:19:27.000000 flapgui-0.1.0/src/flapgui.egg-info/SOURCES.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 14:19:27.000000 flapgui-0.1.0/src/flapgui.egg-info/dependency_links.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 14:19:27.000000 flapgui-0.1.0/src/flapgui.egg-info/top_level.txt
```

### Comparing `flapgui-0.0.4/LICENSE` & `flapgui-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `flapgui-0.0.4/PKG-INFO` & `flapgui-0.1.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flapgui
-Version: 0.0.4
+Version: 0.1.0
 Summary: Easy-to-use and cross-platform GUI library for making functional GUI apps
 Author-email: WinFan3672 <winfan3672@gmail.com>
 Project-URL: Homepage, https://github.com/WinFan3672/Flap
 Project-URL: Bug Tracker, https://github.com/WinFan3672/Flap/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `flapgui-0.0.4/README.md` & `flapgui-0.1.0/README.md`

 * *Files identical despite different names*

### Comparing `flapgui-0.0.4/pyproject.toml` & `flapgui-0.1.0/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "flapgui"
-version = "0.0.4"
+version = "0.1.0"
 authors = [
   { name="WinFan3672", email="winfan3672@gmail.com" },
 ]
 description = "Easy-to-use and cross-platform GUI library for making functional GUI apps"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `flapgui-0.0.4/src/flapgui/__init__.py` & `flapgui-0.1.0/src/flapgui/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import tkinter as tk
 from tkinter import filedialog
 from tkinter import messagebox
 import tkinter.colorchooser
 
 global app_version
-app_version = [0,0,4]
+app_version = [0,1,0]
 global verbose
 verbose = True
 
 def window(title="flapWindow", width=250, height=250):
     """
 Creates a window.
     """
```

### Comparing `flapgui-0.0.4/src/flapgui.egg-info/PKG-INFO` & `flapgui-0.1.0/src/flapgui.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flapgui
-Version: 0.0.4
+Version: 0.1.0
 Summary: Easy-to-use and cross-platform GUI library for making functional GUI apps
 Author-email: WinFan3672 <winfan3672@gmail.com>
 Project-URL: Homepage, https://github.com/WinFan3672/Flap
 Project-URL: Bug Tracker, https://github.com/WinFan3672/Flap/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

