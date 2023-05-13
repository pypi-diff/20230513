# Comparing `tmp/txl_notebook-0.1.5.tar.gz` & `tmp/txl_notebook-0.1.7.tar.gz`

## Comparing `txl_notebook-0.1.5.tar` & `txl_notebook-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_notebook-0.1.5/txl_notebook/__init__.py
--rw-r--r--   0        0        0      658 2020-02-02 00:00:00.000000 txl_notebook-0.1.5/txl_notebook/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_notebook-0.1.5/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_notebook-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 txl_notebook-0.1.5/README.md
--rw-r--r--   0        0        0     1037 2020-02-02 00:00:00.000000 txl_notebook-0.1.5/pyproject.toml
--rw-r--r--   0        0        0      902 2020-02-02 00:00:00.000000 txl_notebook-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_notebook-0.1.7/txl_notebook/__init__.py
+-rw-r--r--   0        0        0      705 2020-02-02 00:00:00.000000 txl_notebook-0.1.7/txl_notebook/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_notebook-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_notebook-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 txl_notebook-0.1.7/README.md
+-rw-r--r--   0        0        0     1037 2020-02-02 00:00:00.000000 txl_notebook-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      902 2020-02-02 00:00:00.000000 txl_notebook-0.1.7/PKG-INFO
```

### Comparing `txl_notebook-0.1.5/LICENSE.txt` & `txl_notebook-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_notebook-0.1.5/pyproject.toml` & `txl_notebook-0.1.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
   "Programming Language :: Python :: 3.10",
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "txl",
-  "jupyter_ydoc >=0.3.0a1"
+  "jupyter_ydoc >=0.3.0a4"
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/plugins/notebook"
 
 [project.entry-points.txl_component]
```

### Comparing `txl_notebook-0.1.5/PKG-INFO` & `txl_notebook-0.1.7/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: txl_notebook
-Version: 0.1.5
+Version: 0.1.7
 Summary: TXL plugin for a notebook
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/notebook
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
@@ -12,12 +12,12 @@
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Requires-Python: >=3.7
-Requires-Dist: jupyter-ydoc>=0.3.0a1
+Requires-Dist: jupyter-ydoc>=0.3.0a4
 Requires-Dist: txl
 Description-Content-Type: text/markdown
 
 # TXL plugin for a notebook
```

