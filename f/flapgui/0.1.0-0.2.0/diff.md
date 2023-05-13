# Comparing `tmp/flapgui-0.1.0.tar.gz` & `tmp/flapgui-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "flapgui-0.1.0.tar", last modified: Sat May 13 14:19:27 2023, max compression
+gzip compressed data, was "flapgui-0.2.0.tar", last modified: Sat May 13 14:31:10 2023, max compression
```

## Comparing `flapgui-0.1.0.tar` & `flapgui-0.2.0.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:19:27.880889 flapgui-0.1.0/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.1.0/LICENSE
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:19:27.880420 flapgui-0.1.0/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6181 2023-05-13 10:49:01.000000 flapgui-0.1.0/README.md
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 14:19:04.000000 flapgui-0.1.0/pyproject.toml
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 14:19:27.881013 flapgui-0.1.0/setup.cfg
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:19:27.839173 flapgui-0.1.0/src/
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:19:27.875650 flapgui-0.1.0/src/flapgui/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     7579 2023-05-13 14:19:12.000000 flapgui-0.1.0/src/flapgui/__init__.py
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:19:27.879210 flapgui-0.1.0/src/flapgui.egg-info/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:19:27.000000 flapgui-0.1.0/src/flapgui.egg-info/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 14:19:27.000000 flapgui-0.1.0/src/flapgui.egg-info/SOURCES.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 14:19:27.000000 flapgui-0.1.0/src/flapgui.egg-info/dependency_links.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 14:19:27.000000 flapgui-0.1.0/src/flapgui.egg-info/top_level.txt
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:31:10.158078 flapgui-0.2.0/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.2.0/LICENSE
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:31:10.157667 flapgui-0.2.0/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6181 2023-05-13 10:49:01.000000 flapgui-0.2.0/README.md
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 14:30:38.000000 flapgui-0.2.0/pyproject.toml
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 14:31:10.158194 flapgui-0.2.0/setup.cfg
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:31:10.095895 flapgui-0.2.0/src/
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:31:10.116697 flapgui-0.2.0/src/flapgui/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     7580 2023-05-13 14:26:22.000000 flapgui-0.2.0/src/flapgui/__init__.py
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:31:10.156700 flapgui-0.2.0/src/flapgui.egg-info/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6722 2023-05-13 14:31:10.000000 flapgui-0.2.0/src/flapgui.egg-info/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 14:31:10.000000 flapgui-0.2.0/src/flapgui.egg-info/SOURCES.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 14:31:10.000000 flapgui-0.2.0/src/flapgui.egg-info/dependency_links.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 14:31:10.000000 flapgui-0.2.0/src/flapgui.egg-info/top_level.txt
```

### Comparing `flapgui-0.1.0/LICENSE` & `flapgui-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `flapgui-0.1.0/PKG-INFO` & `flapgui-0.2.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flapgui
-Version: 0.1.0
+Version: 0.2.0
 Summary: Easy-to-use and cross-platform GUI library for making functional GUI apps
 Author-email: WinFan3672 <winfan3672@gmail.com>
 Project-URL: Homepage, https://github.com/WinFan3672/Flap
 Project-URL: Bug Tracker, https://github.com/WinFan3672/Flap/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `flapgui-0.1.0/README.md` & `flapgui-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `flapgui-0.1.0/pyproject.toml` & `flapgui-0.2.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "flapgui"
-version = "0.1.0"
+version = "0.2.0"
 authors = [
   { name="WinFan3672", email="winfan3672@gmail.com" },
 ]
 description = "Easy-to-use and cross-platform GUI library for making functional GUI apps"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `flapgui-0.1.0/src/flapgui/__init__.py` & `flapgui-0.2.0/src/flapgui/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 import tkinter as tk
 from tkinter import filedialog
 from tkinter import messagebox
+from tkinter import ttk
 import tkinter.colorchooser
 
+
 global app_version
-app_version = [0,1,0]
+app_version = [0,2,0]
 global verbose
 verbose = True
 
 def window(title="flapWindow", width=250, height=250):
     """
 Creates a window.
     """
@@ -37,19 +39,17 @@
     scaleResolution(window,width,height)
 def scaleResolution(window, width, height):
     if verbose:
         print(f"Flap: Scaled Resolution to {width}x{height}")
     window.geometry(f"{width}x{height}")
 def maximiseWindow(window):
     window.attributes('-zoomed', True)
-def pack(text):
-    if verbose:
-        print("Flap: Added Text",text)
-    l = label(text)
-    l.pack()
+def addText(root, text):
+    label = tk.Label(root, text=text)
+    label.pack()
 def textEntry(width, height,fg=None,bg=None):
     if verbose:
         print(f"Flap: Made new text entry: bg {bg} fg {fg}")
     text_box = tk.Text(width=width, height=height,fg=fg,bg=bg,insertbackground=fg)
     return text_box
 def framedTextEntry(window, width=40, bg="#FFFFFF", fg="#000000"):
     if verbose:
```

### Comparing `flapgui-0.1.0/src/flapgui.egg-info/PKG-INFO` & `flapgui-0.2.0/src/flapgui.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flapgui
-Version: 0.1.0
+Version: 0.2.0
 Summary: Easy-to-use and cross-platform GUI library for making functional GUI apps
 Author-email: WinFan3672 <winfan3672@gmail.com>
 Project-URL: Homepage, https://github.com/WinFan3672/Flap
 Project-URL: Bug Tracker, https://github.com/WinFan3672/Flap/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

