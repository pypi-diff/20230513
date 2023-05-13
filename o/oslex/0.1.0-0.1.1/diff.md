# Comparing `tmp/oslex-0.1.0.tar.gz` & `tmp/oslex-0.1.1.tar.gz`

## Comparing `oslex-0.1.0.tar` & `oslex-0.1.1.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0      110 2020-02-02 00:00:00.000000 oslex-0.1.0/.editorconfig
--rw-r--r--   0        0        0     2465 2020-02-02 00:00:00.000000 oslex-0.1.0/oslex.py
--rw-r--r--   0        0        0     3238 2020-02-02 00:00:00.000000 oslex-0.1.0/.gitignore
--rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 oslex-0.1.0/LICENSE
--rw-r--r--   0        0        0      834 2020-02-02 00:00:00.000000 oslex-0.1.0/README.md
--rw-r--r--   0        0        0     1016 2020-02-02 00:00:00.000000 oslex-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     1777 2020-02-02 00:00:00.000000 oslex-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0      110 2020-02-02 00:00:00.000000 oslex-0.1.1/.editorconfig
+-rw-r--r--   0        0        0     2589 2020-02-02 00:00:00.000000 oslex-0.1.1/oslex.py
+-rw-r--r--   0        0        0     3238 2020-02-02 00:00:00.000000 oslex-0.1.1/.gitignore
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 oslex-0.1.1/LICENSE
+-rw-r--r--   0        0        0      834 2020-02-02 00:00:00.000000 oslex-0.1.1/README.md
+-rw-r--r--   0        0        0     1119 2020-02-02 00:00:00.000000 oslex-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     1727 2020-02-02 00:00:00.000000 oslex-0.1.1/PKG-INFO
```

### Comparing `oslex-0.1.0/oslex.py` & `oslex-0.1.1/oslex.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 import sys
 
 
 def is_posix() -> bool:
     """
     Returns whether the system running Python is POSIX compatible.
-    This is the condition for oslex.underyling being shlex.
+    This is the condition for oslex.underlying being shlex.
     This is also the condition for os.path being posixpath.
     """
     return 'posix' in sys.builtin_module_names
 
 
 def is_windows() -> bool:
     """
     Returns whether the system running Python is Windows based.
-    This is the condition for oslex.underyling being mslex.
+    This is the condition for oslex.underlying being mslex.
     This is also the condition for os.path being ntpath.
     """
 
     if is_posix():
         # This early return is likely redundant, but we want to be 100% equivalent to the if-elseif structure found in os.py
         # See https://github.com/python/cpython/blob/3.7/Lib/os.py
         return False
@@ -27,15 +27,15 @@
 
 # Import OS-specific module
 
 if is_posix():
     import shlex as underlying
 elif is_windows():
     # mslex has no type annotations -> we have to ignore the "import" error
-    # also, mypy does not understand conditioanl importing, so it thinks we are redefining the name -> we have to ignore the "no-redef" error
+    # also, mypy does not understand conditional importing, so it thinks we are redefining the name "underlying" -> we have to ignore the "no-redef" error
     import mslex as underlying  # type: ignore[import, no-redef]
 else:
     raise ImportError('no os specific module found')
 
 # Define functions
 
 
@@ -57,11 +57,12 @@
 
 def join(split_command: list[str]) -> str:
     """
     Concatenate the tokens of the list split_command and return a string. This function is the inverse of split().
     The returned value is shell-escaped to protect against injection vulnerabilities (see quote()).
     This function is safe to use both for POSIX-compatible shells and for Windows's cmd.
     """
-    # shlex only has join() since python 3.8
+    # shlex only has join() since Python 3.8
     # mslex doesn't have it at all
-    # it's easier to just implement it without trying to import the functionality
+    # It's easier to just implement it without trying to import the functionality
+    # Implementation is the same as shlex.join(), see https://github.com/python/cpython/blob/3.8/Lib/shlex.py
     return ' '.join(quote(arg) for arg in split_command)
```

### Comparing `oslex-0.1.0/.gitignore` & `oslex-0.1.1/.gitignore`

 * *Files identical despite different names*

### Comparing `oslex-0.1.0/LICENSE` & `oslex-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `oslex-0.1.0/README.md` & `oslex-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `oslex-0.1.0/PKG-INFO` & `oslex-0.1.1/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,28 +1,27 @@
 Metadata-Version: 2.1
 Name: oslex
-Version: 0.1.0
+Version: 0.1.1
 Summary: OS-independent wrapper for shlex and mslex
 Project-URL: Homepage, https://github.com/petamas/oslex
 Project-URL: Bug Tracker, https://github.com/petamas/oslex/issues
 Author-email: Tamás PEREGI <petamas@gmail.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: MacOS
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Python: >=3.5
+Requires-Python: >=3.6
 Requires-Dist: mslex
 Description-Content-Type: text/markdown
 
 # oslex
 
 `oslex` is an OS-independent wrapper for [`shlex`](https://docs.python.org/3/library/shlex.html) and [`mslex`](https://pypi.org/project/mslex/).
```

