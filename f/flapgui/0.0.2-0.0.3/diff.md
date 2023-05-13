# Comparing `tmp/flapgui-0.0.2.tar.gz` & `tmp/flapgui-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "flapgui-0.0.2.tar", last modified: Sat May 13 09:56:52 2023, max compression
+gzip compressed data, was "flapgui-0.0.3.tar", last modified: Sat May 13 10:57:49 2023, max compression
```

## Comparing `flapgui-0.0.2.tar` & `flapgui-0.0.3.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 09:56:52.314107 flapgui-0.0.2/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.0.2/LICENSE
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      586 2023-05-13 09:56:52.313652 flapgui-0.0.2/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       83 2023-05-12 20:35:39.000000 flapgui-0.0.2/README.md
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      576 2023-05-13 09:56:37.000000 flapgui-0.0.2/pyproject.toml
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 09:56:52.314222 flapgui-0.0.2/setup.cfg
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 09:56:52.300613 flapgui-0.0.2/src/
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 09:56:52.306845 flapgui-0.0.2/src/flap/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6341 2023-05-12 18:09:41.000000 flapgui-0.0.2/src/flap/__init__.py
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 09:56:52.312346 flapgui-0.0.2/src/flapgui.egg-info/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      586 2023-05-13 09:56:52.000000 flapgui-0.0.2/src/flapgui.egg-info/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      193 2023-05-13 09:56:52.000000 flapgui-0.0.2/src/flapgui.egg-info/SOURCES.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 09:56:52.000000 flapgui-0.0.2/src/flapgui.egg-info/dependency_links.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        5 2023-05-13 09:56:52.000000 flapgui-0.0.2/src/flapgui.egg-info/top_level.txt
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 10:57:49.361693 flapgui-0.0.3/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.0.3/LICENSE
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 10:57:49.348126 flapgui-0.0.3/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6181 2023-05-13 10:49:01.000000 flapgui-0.0.3/README.md
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 10:10:23.000000 flapgui-0.0.3/pyproject.toml
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 10:57:49.362444 flapgui-0.0.3/setup.cfg
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 10:57:49.234268 flapgui-0.0.3/src/
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 10:57:49.266434 flapgui-0.0.3/src/flapgui/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6295 2023-05-13 10:40:32.000000 flapgui-0.0.3/src/flapgui/__init__.py
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 10:57:49.304997 flapgui-0.0.3/src/flapgui.egg-info/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 10:57:49.000000 flapgui-0.0.3/src/flapgui.egg-info/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 10:57:49.000000 flapgui-0.0.3/src/flapgui.egg-info/SOURCES.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 10:57:49.000000 flapgui-0.0.3/src/flapgui.egg-info/dependency_links.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 10:57:49.000000 flapgui-0.0.3/src/flapgui.egg-info/top_level.txt
```

### Comparing `flapgui-0.0.2/LICENSE` & `flapgui-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `flapgui-0.0.2/pyproject.toml` & `flapgui-0.0.3/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "flapgui"
-version = "0.0.2"
+version = "0.0.3"
 authors = [
   { name="WinFan3672", email="winfan3672@gmail.com" },
 ]
-description = "Easy-to-use GUI library for Tkinter"
+description = "Easy-to-use and cross-platform GUI library for making functional GUI apps"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/WinFan3672/Flap"
-"Bug Tracker" = "https://github.com/WinFan3672/flap/issues"
+"Bug Tracker" = "https://github.com/WinFan3672/Flap/issues"
```

### Comparing `flapgui-0.0.2/src/flap/__init__.py` & `flapgui-0.0.3/src/flapgui/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import tkinter as tk
 from tkinter import filedialog
 from tkinter import messagebox
 import tkinter.colorchooser
 
 global app_version
-app_version = [0,0,2]
+app_version = [0,0,3]
 
 global verbose
 verbose = True
 
 def window(title="flapWindow", width=250, height=250):
     if verbose:
         print(f"Flap: Created window \"{title}\" with resolution {width}x{height}")
@@ -186,14 +186,13 @@
         return f"#{r:02x}{g:02x}{b:02x}"
     else:
         return None
 def createGrid(window):
     grid = tk.Frame(window)
     grid.pack()
     return grid
-def addGridButton(grid, label, function, x, y, buttonDimensionX=1, buttonDimensionY=1):
+def addGridButton(grid, label, function, x, y, buttonDimensionX=2, buttonDimensionY=1):
     button = tk.Button(grid, text=label, command=function)
     button.config(width=buttonDimensionX, height=buttonDimensionY)
     button.grid(row=x, column=y)
 if verbose:
-    print(f"Flap: Initialised v{app_version[0]}.{app_version[1]}.{app_version[2]}")
-    print(f"(c) 2023 WinFan3672, some rights reserved.")
+    print(f"Flap: Initialised Framework ({app_version[0]}.{app_version[1]}.{app_version[2]})")
```

