# Comparing `tmp/flapgui-0.2.1.tar.gz` & `tmp/flapgui-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "flapgui-0.2.1.tar", last modified: Sat May 13 14:32:50 2023, max compression
+gzip compressed data, was "flapgui-0.3.0.tar", last modified: Sat May 13 17:29:25 2023, max compression
```

## Comparing `flapgui-0.2.1.tar` & `flapgui-0.3.0.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:32:50.012355 flapgui-0.2.1/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.2.1/LICENSE
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6733 2023-05-13 14:32:50.011967 flapgui-0.2.1/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6192 2023-05-13 14:32:32.000000 flapgui-0.2.1/README.md
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 14:32:15.000000 flapgui-0.2.1/pyproject.toml
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 14:32:50.012480 flapgui-0.2.1/setup.cfg
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:32:49.970456 flapgui-0.2.1/src/
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:32:49.973473 flapgui-0.2.1/src/flapgui/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     7580 2023-05-13 14:26:22.000000 flapgui-0.2.1/src/flapgui/__init__.py
-drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 14:32:50.010922 flapgui-0.2.1/src/flapgui.egg-info/
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6733 2023-05-13 14:32:49.000000 flapgui-0.2.1/src/flapgui.egg-info/PKG-INFO
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 14:32:49.000000 flapgui-0.2.1/src/flapgui.egg-info/SOURCES.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 14:32:49.000000 flapgui-0.2.1/src/flapgui.egg-info/dependency_links.txt
--rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 14:32:49.000000 flapgui-0.2.1/src/flapgui.egg-info/top_level.txt
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 17:29:25.847316 flapgui-0.3.0/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     1073 2023-05-12 20:35:47.000000 flapgui-0.3.0/LICENSE
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6747 2023-05-13 17:29:25.846739 flapgui-0.3.0/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6206 2023-05-13 17:28:24.000000 flapgui-0.3.0/README.md
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      614 2023-05-13 17:25:37.000000 flapgui-0.3.0/pyproject.toml
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)       38 2023-05-13 17:29:25.847452 flapgui-0.3.0/setup.cfg
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 17:29:25.832838 flapgui-0.3.0/src/
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 17:29:25.838279 flapgui-0.3.0/src/flapgui/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     8608 2023-05-13 17:22:41.000000 flapgui-0.3.0/src/flapgui/__init__.py
+drwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        0 2023-05-13 17:29:25.845368 flapgui-0.3.0/src/flapgui.egg-info/
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)     6747 2023-05-13 17:29:25.000000 flapgui-0.3.0/src/flapgui.egg-info/PKG-INFO
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)      196 2023-05-13 17:29:25.000000 flapgui-0.3.0/src/flapgui.egg-info/SOURCES.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        1 2023-05-13 17:29:25.000000 flapgui-0.3.0/src/flapgui.egg-info/dependency_links.txt
+-rwxrwxrwx   0 winfan3672  (1000) winfan3672  (1000)        8 2023-05-13 17:29:25.000000 flapgui-0.3.0/src/flapgui.egg-info/top_level.txt
```

### Comparing `flapgui-0.2.1/LICENSE` & `flapgui-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `flapgui-0.2.1/PKG-INFO` & `flapgui-0.3.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flapgui
-Version: 0.2.1
+Version: 0.3.0
 Summary: Easy-to-use and cross-platform GUI library for making functional GUI apps
 Author-email: WinFan3672 <winfan3672@gmail.com>
 Project-URL: Homepage, https://github.com/WinFan3672/Flap
 Project-URL: Bug Tracker, https://github.com/WinFan3672/Flap/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -42,56 +42,56 @@
 ### Example
 ```
 import flapgui as fl
 root = fl.window("Tutorial Window")
 ```
 This will create a blank window with the title "Tutorial Window".
 ## Adding text to a window
-To add some text, you use the fl.pack() function:  
+To add some text, you use the fl.addText() function:  
 ```
 import flapgui as fl
 root = fl.window("Tutorial Window")
-fl.pack("This is some text")
-fl.pack("This is some more")
+fl.addText(root, "This is some text")
+fl.addText(root, "This is some more")
 ```
 ## Adding a button
 You can also add a button that performs an action when it is pressed.
 
 You do this with the create_button() function.
 
 ```
-create_button(window, text, command=None)
+createButton(root, text, command=None)
 ```
 
 Window is the window you specified, text is the text that will appear on it, and command is the function that is called when you press it.
 ```
 import flapgui as fl
 root=fl.window("Tutorial #2: Buttons")
-fl.pack("The below button will print stuff to the terminal")
-b = fl.create_button(root, "Press Me",lambda: print("hello world"))
+fl.addText(root, "The below button will print stuff to the terminal")
+b = fl.createButton(root, "Press Me",lambda: print("hello world"))
 ```
 As you can see, in the above example, I used an anonymous function. 
 ## Menu Bars
 Creating a menu bar allows you to add menus to the top of the program, and can let you add more functionality to it easily.
 
 First, you add a menu bar:  
 
 ```
 root=fl.window()
-menu = fl.create_menu_bar(root)
+menu = fl.menuBar(root)
 ```
 Then, you add cascades to the menu:
 ```
-fileMenu = fl.add_cascade(menu,"File")
-editMenu = fl.add_cascade(menu,"Edit")
-helpMenu = fl.add_cascade(menu,"Help")
+fileMenu = fl.addCascade(menu,"File")
+editMenu = fl.addCascade(menu,"Edit")
+helpMenu = fl.addCascade(menu,"Help")
 ```
 Once you've done that, you add commands to those cascades:
 ```
-fl.add_command(fileMenu,"Exit",exit_application,"Ctrl+Q")
+fl.addCommand(fileMenu,"Exit",exit_application,"Ctrl+Q")
 ```
 The above command calls exit_application() and shows "Ctrl+Q" as an accelerator.
 ### Final Application
 ```
 # Final application
 root = fl.window("Tutorial #3: Menu Bar")
 menu = fl.create_menu(root)
```

### Comparing `flapgui-0.2.1/README.md` & `flapgui-0.3.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -28,56 +28,56 @@
 ### Example
 ```
 import flapgui as fl
 root = fl.window("Tutorial Window")
 ```
 This will create a blank window with the title "Tutorial Window".
 ## Adding text to a window
-To add some text, you use the fl.pack() function:  
+To add some text, you use the fl.addText() function:  
 ```
 import flapgui as fl
 root = fl.window("Tutorial Window")
-fl.pack("This is some text")
-fl.pack("This is some more")
+fl.addText(root, "This is some text")
+fl.addText(root, "This is some more")
 ```
 ## Adding a button
 You can also add a button that performs an action when it is pressed.
 
 You do this with the create_button() function.
 
 ```
-create_button(window, text, command=None)
+createButton(root, text, command=None)
 ```
 
 Window is the window you specified, text is the text that will appear on it, and command is the function that is called when you press it.
 ```
 import flapgui as fl
 root=fl.window("Tutorial #2: Buttons")
-fl.pack("The below button will print stuff to the terminal")
-b = fl.create_button(root, "Press Me",lambda: print("hello world"))
+fl.addText(root, "The below button will print stuff to the terminal")
+b = fl.createButton(root, "Press Me",lambda: print("hello world"))
 ```
 As you can see, in the above example, I used an anonymous function. 
 ## Menu Bars
 Creating a menu bar allows you to add menus to the top of the program, and can let you add more functionality to it easily.
 
 First, you add a menu bar:  
 
 ```
 root=fl.window()
-menu = fl.create_menu_bar(root)
+menu = fl.menuBar(root)
 ```
 Then, you add cascades to the menu:
 ```
-fileMenu = fl.add_cascade(menu,"File")
-editMenu = fl.add_cascade(menu,"Edit")
-helpMenu = fl.add_cascade(menu,"Help")
+fileMenu = fl.addCascade(menu,"File")
+editMenu = fl.addCascade(menu,"Edit")
+helpMenu = fl.addCascade(menu,"Help")
 ```
 Once you've done that, you add commands to those cascades:
 ```
-fl.add_command(fileMenu,"Exit",exit_application,"Ctrl+Q")
+fl.addCommand(fileMenu,"Exit",exit_application,"Ctrl+Q")
 ```
 The above command calls exit_application() and shows "Ctrl+Q" as an accelerator.
 ### Final Application
 ```
 # Final application
 root = fl.window("Tutorial #3: Menu Bar")
 menu = fl.create_menu(root)
```

### Comparing `flapgui-0.2.1/pyproject.toml` & `flapgui-0.3.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "flapgui"
-version = "0.2.1"
+version = "0.3.0"
 authors = [
   { name="WinFan3672", email="winfan3672@gmail.com" },
 ]
 description = "Easy-to-use and cross-platform GUI library for making functional GUI apps"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `flapgui-0.2.1/src/flapgui/__init__.py` & `flapgui-0.3.0/src/flapgui/__init__.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 import tkinter as tk
 from tkinter import filedialog
 from tkinter import messagebox
 from tkinter import ttk
 import tkinter.colorchooser
-
+import webbrowser
 
 global app_version
-app_version = [0,2,0]
+app_version = [0,3,0]
 global verbose
 verbose = True
 
 def window(title="flapWindow", width=250, height=250):
     """
 Creates a window.
     """
@@ -28,14 +28,24 @@
     
     if close_parent:
         child_window.protocol("WM_DELETE_WINDOW", child_window.destroy)
     else:
         child_window.protocol("WM_DELETE_WINDOW", root.destroy)
     
     return child_window
+def createFrame(root):
+    frame = tk.Frame(root)
+    frame.pack()
+    return frame
+def createHyperlinkText(root, label_text, url):
+    label = tk.Label(root, text=label_text, fg='blue', cursor='hand2')
+    label.pack()
+    label.bind('<Button-1>', lambda e: webbrowser.open(url))
+def changeTitle(root, new_title):
+    root.title(new_title)
 def autoScaleResolution(window):
     window.update_idletasks()  # Update window to ensure accurate widget sizes
     width = window.winfo_reqwidth()
     height = window.winfo_reqheight()
     scaleResolution(window,width,height)
 def scaleResolution(window, width, height):
     if verbose:
@@ -90,34 +100,55 @@
     root.protocol("WM_DELETE_WINDOW", disable_close_button)
 def makeReclosable(root):
     root.protocol("WM_DELETE_WINDOW", root.destroy)
 def menuBar(root):
     if verbose:
         print(f"Flap: Added Menu Bar")
     # create the menu bar widget
-    menu_bar = tk.Menu(parent)
-    parent.config(menu=menu_bar)
+    menu_bar = tk.Menu(root)
+    root.config(menu=menu_bar)
     return menu_bar
 def addCascade(menuBar,label):
     if verbose:
         print(f"Flap: New Cascade \"{label}\"")
     # create a new menu
-    cascade_menu = tk.Menu(menu_bar, tearoff=0)
+    cascade_menu = tk.Menu(menuBar, tearoff=0)
     # add the cascade menu to the menu bar
     menuBar.add_cascade(label=label, menu=cascade_menu)
     return cascade_menu
 def addCommand(cascade, label, command=None, accelerator=None):
     if verbose:
         print(f"Flap: Added Command To Cascade: {label}")
         cascade.add_command(label=label, command=command,accelerator=accelerator)
     
 def keyBind(root,binding,command=None):
     if verbose:
         print(f"Flap: Added Binding: {binding}")
     root.bind(binding,command)
+def addText(root, label_text):
+    label = tk.Label(root, text=label_text)
+    label.pack()
+def addFrameScrollbar(frame):
+    scrollbar = tk.Scrollbar(frame)
+    scrollbar.pack(side=tk.RIGHT, fill=tk.Y)
+
+    canvas = tk.Canvas(frame, yscrollcommand=scrollbar.set)
+    canvas.pack(side=tk.LEFT, fill=tk.BOTH, expand=True)
+
+    scrollbar.config(command=canvas.yview)
+
+    content_frame = tk.Frame(canvas)
+    canvas.create_window((0, 0), window=content_frame, anchor="nw")
+
+    def configure_scrollbar(event):
+        canvas.configure(scrollregion=canvas.bbox("all"), width=200, height=200)
+
+    content_frame.bind("<Configure>", configure_scrollbar)
+
+    return content_frame
 def messageBox(title,message):
     msg=message.replace("\n","\\n")
     print(f"Flap: Message Box: {title} :: \"{msg}\"")
     root = tk.Tk()
     root.withdraw() # hide the main window
 
     messagebox.showinfo(title, message)
```

### Comparing `flapgui-0.2.1/src/flapgui.egg-info/PKG-INFO` & `flapgui-0.3.0/src/flapgui.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flapgui
-Version: 0.2.1
+Version: 0.3.0
 Summary: Easy-to-use and cross-platform GUI library for making functional GUI apps
 Author-email: WinFan3672 <winfan3672@gmail.com>
 Project-URL: Homepage, https://github.com/WinFan3672/Flap
 Project-URL: Bug Tracker, https://github.com/WinFan3672/Flap/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -42,56 +42,56 @@
 ### Example
 ```
 import flapgui as fl
 root = fl.window("Tutorial Window")
 ```
 This will create a blank window with the title "Tutorial Window".
 ## Adding text to a window
-To add some text, you use the fl.pack() function:  
+To add some text, you use the fl.addText() function:  
 ```
 import flapgui as fl
 root = fl.window("Tutorial Window")
-fl.pack("This is some text")
-fl.pack("This is some more")
+fl.addText(root, "This is some text")
+fl.addText(root, "This is some more")
 ```
 ## Adding a button
 You can also add a button that performs an action when it is pressed.
 
 You do this with the create_button() function.
 
 ```
-create_button(window, text, command=None)
+createButton(root, text, command=None)
 ```
 
 Window is the window you specified, text is the text that will appear on it, and command is the function that is called when you press it.
 ```
 import flapgui as fl
 root=fl.window("Tutorial #2: Buttons")
-fl.pack("The below button will print stuff to the terminal")
-b = fl.create_button(root, "Press Me",lambda: print("hello world"))
+fl.addText(root, "The below button will print stuff to the terminal")
+b = fl.createButton(root, "Press Me",lambda: print("hello world"))
 ```
 As you can see, in the above example, I used an anonymous function. 
 ## Menu Bars
 Creating a menu bar allows you to add menus to the top of the program, and can let you add more functionality to it easily.
 
 First, you add a menu bar:  
 
 ```
 root=fl.window()
-menu = fl.create_menu_bar(root)
+menu = fl.menuBar(root)
 ```
 Then, you add cascades to the menu:
 ```
-fileMenu = fl.add_cascade(menu,"File")
-editMenu = fl.add_cascade(menu,"Edit")
-helpMenu = fl.add_cascade(menu,"Help")
+fileMenu = fl.addCascade(menu,"File")
+editMenu = fl.addCascade(menu,"Edit")
+helpMenu = fl.addCascade(menu,"Help")
 ```
 Once you've done that, you add commands to those cascades:
 ```
-fl.add_command(fileMenu,"Exit",exit_application,"Ctrl+Q")
+fl.addCommand(fileMenu,"Exit",exit_application,"Ctrl+Q")
 ```
 The above command calls exit_application() and shows "Ctrl+Q" as an accelerator.
 ### Final Application
 ```
 # Final application
 root = fl.window("Tutorial #3: Menu Bar")
 menu = fl.create_menu(root)
```

