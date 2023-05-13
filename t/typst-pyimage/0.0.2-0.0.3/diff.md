# Comparing `tmp/typst_pyimage-0.0.2.tar.gz` & `tmp/typst_pyimage-0.0.3.tar.gz`

## Comparing `typst_pyimage-0.0.2.tar` & `typst_pyimage-0.0.3.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0      139 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/typst_pyimage/__init__.py
--rw-r--r--   0        0        0      350 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/typst_pyimage/__main__.py
--rw-r--r--   0        0        0      220 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/typst_pyimage/pyimage.typ
--rw-r--r--   0        0        0     4542 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/typst_pyimage/run.py
--rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/.gitignore
--rw-r--r--   0        0        0    11357 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/LICENSE
--rw-r--r--   0        0        0     3653 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/README.md
--rw-r--r--   0        0        0     1118 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/pyproject.toml
--rw-r--r--   0        0        0    17333 2020-02-02 00:00:00.000000 typst_pyimage-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0      139 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/typst_pyimage/__init__.py
+-rw-r--r--   0        0        0      350 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/typst_pyimage/__main__.py
+-rw-r--r--   0        0        0      393 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/typst_pyimage/pyimage.typ
+-rw-r--r--   0        0        0     5866 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/typst_pyimage/run.py
+-rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/.gitignore
+-rw-r--r--   0        0        0    11357 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/LICENSE
+-rw-r--r--   0        0        0     4012 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/README.md
+-rw-r--r--   0        0        0     1118 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0    17692 2020-02-02 00:00:00.000000 typst_pyimage-0.0.3/PKG-INFO
```

### Comparing `typst_pyimage-0.0.2/LICENSE` & `typst_pyimage-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `typst_pyimage-0.0.2/README.md` & `typst_pyimage-0.0.3/README.md`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 <h1 align="center">typst_pyimage</h1>
 
-<p align="center">Wraps <a href="https://github.com/typst/typst">Typst</a> to support inline Python code for generating figures.</p>
+<p align="center">Wraps <a href="https://github.com/typst/typst">Typst</a> to support inline Python code for generating content and figures.</p>
 
 ## Example
 
 <img align="right" width="45%" src="https://raw.githubusercontent.com/patrick-kidger/typst_pyimage/main/imgs/lotka_volterra.png">
 
 ```typst
 #import ".typst_pyimage/pyimage.typ": pyimage
@@ -53,52 +53,58 @@
 pip install typst_pyimage
 ```
 
 This requires that you're using Typst locally -- it won't work with the web app.
 
 ## Usage
 
-1. Import `pyimage.typ`. At the start of your `.typ` file, add the line `#import ".typst_pyimage/pyimage.typ": pyimage`.
+1. Import `pyimage.typ`. At the start of your `.typ` file, add the line `#import ".typst_pyimage/pyimage.typ": pyimage, pycontent, pyinit`.
 
-2. Use the `pyimage` function. This has syntax `pyimage(string, ..arguments) -> content`. The positional string should be a Python program that creates a single matplotlib figure. Any named arguments are forwarded on to Typst's built-in `image` function. You can use it just like the normal `image` function, e.g. `#align(center, pyimage("..."))`.
+2. Use these functions.
+
+    a. `pyimage(string, ..arguments) -> content`. The positional string should be a Python program that creates a single matplotlib figure. Any named arguments are forwarded on to Typst's built-in `image` function. You can use it just like the normal `image` function, e.g. `#align(center, pyimage("..."))`.
+
+    b. `pycontent(string)`. The positional string should be a Python program that produces a string on its final line. This will be treated as Typst code.
+
+    c. `pyinit(string)`. The positional string should be a Python program. This will be evaluated before all `pyimage` or `pycontent` calls, e.g. to do import or perform setup.
 
 3. Compile or watch. Run either of the following two commands:
     ```
     python -m typst_pyimage compile your_file.typ
     python -m typst_pyimage watch your_file.typ
     ```
     This will extract and run all your Python code. In addition it will call either `typst compile your_file.typ` or `typst watch your_file.typ`.
 
     The resulting images are saved in the `.typst_pyimage` folder.
 
 ## Notes
 
-It's common to have an initial block of code that is in common to all `#pyimage("...")` calls (such as import statements, defining helpers etc). These can be placed in a `#pyimageinit("...")` directive.
+It's common to have an initial block of code that is in common to all `#pyimage("...")` and `#pycontent("...")` calls (such as import statements, defining helpers etc). These can be placed in a `#pyinit("...")` directive.
 
 Each `#pyimage("...")` block is executed as a fresh module (i.e. as if each was a separate Python file), but with the same Python interpreter.
 
 Overall, this is essentially equivalent to the following Python code:
 ```
 # main.py
-import pyimageinit
+import pyinit
 import pyimage1
 import pyimage2
 
-# pyimageinit.py
-...  # your #pyimageinit("...") code
+# pyinit.py
+...  # your #pyinit("...") code
 
 # pyimage1.py
-from pyimageinit import *
+from pyinit import *
 ...  # your first #pyimage("...") code
 
 # pyimage2.py
-from pyimageinit import *
+from pyinit import *
 ...  # your second #pyimage("...") code
 ```
 This means that e.g. any global caches will be shared across all `#pyimage("...")` calls. (Useful when using a library like JAX, which has a JIT compilation cache.)
 
 ## Limitations
 
-1. The watcher just extracts all the `pyimage("...")` blocks via regex, and runs them in the order that they appear in the file. This means that (a) the `"` character may not appear anywhere in the Python code (even if escaped), and (b) trying to call `pyimage` dynamically (i.e. not with a literal string at the top level of your program) will not work.
-2. Only `pyimage("...")` calls inside the single watched file are tracked.
+1. The watcher just extracts all the `pyimage("...")` etc. blocks via regex, and runs them in the order that they appear in the file. This means that (a) the `"` character may not appear anywhere in the Python code (even if escaped), and (b) trying to call `pyimage` etc. dynamically (i.e. not with a literal string at the top level of your program) will not work.
+2. Only `pyimage("...")` etc. calls inside the single watched file are tracked.
 
 We could probably lift 1a and 2 with a bit of effort. PRs welcome.
```

### Comparing `typst_pyimage-0.0.2/pyproject.toml` & `typst_pyimage-0.0.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "typst_pyimage"
-version = "0.0.2"
+version = "0.0.3"
 description = "Typst extension, adding support for generating figures using inline Python code"
 readme = "README.md"
 requires-python = "~=3.8"
 license = {file = "LICENSE"}
 authors = [
   {name = "Patrick Kidger", email = "contact@kidger.site"},
 ]
```

### Comparing `typst_pyimage-0.0.2/PKG-INFO` & `typst_pyimage-0.0.3/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: typst_pyimage
-Version: 0.0.2
+Version: 0.0.3
 Summary: Typst extension, adding support for generating figures using inline Python code
 Project-URL: repository, https://github.com/patrick-kidger/typst_pyimage
 Author-email: Patrick Kidger <contact@kidger.site>
 License:                                  Apache License
                                    Version 2.0, January 2004
                                 http://www.apache.org/licenses/
         
@@ -215,15 +215,15 @@
 Classifier: Programming Language :: Python :: 3
 Requires-Python: ~=3.8
 Requires-Dist: matplotlib>=3.7.1
 Description-Content-Type: text/markdown
 
 <h1 align="center">typst_pyimage</h1>
 
-<p align="center">Wraps <a href="https://github.com/typst/typst">Typst</a> to support inline Python code for generating figures.</p>
+<p align="center">Wraps <a href="https://github.com/typst/typst">Typst</a> to support inline Python code for generating content and figures.</p>
 
 ## Example
 
 <img align="right" width="45%" src="https://raw.githubusercontent.com/patrick-kidger/typst_pyimage/main/imgs/lotka_volterra.png">
 
 ```typst
 #import ".typst_pyimage/pyimage.typ": pyimage
@@ -272,52 +272,58 @@
 pip install typst_pyimage
 ```
 
 This requires that you're using Typst locally -- it won't work with the web app.
 
 ## Usage
 
-1. Import `pyimage.typ`. At the start of your `.typ` file, add the line `#import ".typst_pyimage/pyimage.typ": pyimage`.
+1. Import `pyimage.typ`. At the start of your `.typ` file, add the line `#import ".typst_pyimage/pyimage.typ": pyimage, pycontent, pyinit`.
 
-2. Use the `pyimage` function. This has syntax `pyimage(string, ..arguments) -> content`. The positional string should be a Python program that creates a single matplotlib figure. Any named arguments are forwarded on to Typst's built-in `image` function. You can use it just like the normal `image` function, e.g. `#align(center, pyimage("..."))`.
+2. Use these functions.
+
+    a. `pyimage(string, ..arguments) -> content`. The positional string should be a Python program that creates a single matplotlib figure. Any named arguments are forwarded on to Typst's built-in `image` function. You can use it just like the normal `image` function, e.g. `#align(center, pyimage("..."))`.
+
+    b. `pycontent(string)`. The positional string should be a Python program that produces a string on its final line. This will be treated as Typst code.
+
+    c. `pyinit(string)`. The positional string should be a Python program. This will be evaluated before all `pyimage` or `pycontent` calls, e.g. to do import or perform setup.
 
 3. Compile or watch. Run either of the following two commands:
     ```
     python -m typst_pyimage compile your_file.typ
     python -m typst_pyimage watch your_file.typ
     ```
     This will extract and run all your Python code. In addition it will call either `typst compile your_file.typ` or `typst watch your_file.typ`.
 
     The resulting images are saved in the `.typst_pyimage` folder.
 
 ## Notes
 
-It's common to have an initial block of code that is in common to all `#pyimage("...")` calls (such as import statements, defining helpers etc). These can be placed in a `#pyimageinit("...")` directive.
+It's common to have an initial block of code that is in common to all `#pyimage("...")` and `#pycontent("...")` calls (such as import statements, defining helpers etc). These can be placed in a `#pyinit("...")` directive.
 
 Each `#pyimage("...")` block is executed as a fresh module (i.e. as if each was a separate Python file), but with the same Python interpreter.
 
 Overall, this is essentially equivalent to the following Python code:
 ```
 # main.py
-import pyimageinit
+import pyinit
 import pyimage1
 import pyimage2
 
-# pyimageinit.py
-...  # your #pyimageinit("...") code
+# pyinit.py
+...  # your #pyinit("...") code
 
 # pyimage1.py
-from pyimageinit import *
+from pyinit import *
 ...  # your first #pyimage("...") code
 
 # pyimage2.py
-from pyimageinit import *
+from pyinit import *
 ...  # your second #pyimage("...") code
 ```
 This means that e.g. any global caches will be shared across all `#pyimage("...")` calls. (Useful when using a library like JAX, which has a JIT compilation cache.)
 
 ## Limitations
 
-1. The watcher just extracts all the `pyimage("...")` blocks via regex, and runs them in the order that they appear in the file. This means that (a) the `"` character may not appear anywhere in the Python code (even if escaped), and (b) trying to call `pyimage` dynamically (i.e. not with a literal string at the top level of your program) will not work.
-2. Only `pyimage("...")` calls inside the single watched file are tracked.
+1. The watcher just extracts all the `pyimage("...")` etc. blocks via regex, and runs them in the order that they appear in the file. This means that (a) the `"` character may not appear anywhere in the Python code (even if escaped), and (b) trying to call `pyimage` etc. dynamically (i.e. not with a literal string at the top level of your program) will not work.
+2. Only `pyimage("...")` etc. calls inside the single watched file are tracked.
 
 We could probably lift 1a and 2 with a bit of effort. PRs welcome.
```

