# Comparing `tmp/txl_launcher-0.1.5.tar.gz` & `tmp/txl_launcher-0.1.7.tar.gz`

## Comparing `txl_launcher-0.1.5.tar` & `txl_launcher-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_launcher-0.1.5/txl_launcher/__init__.py
--rw-r--r--   0        0        0     1319 2020-02-02 00:00:00.000000 txl_launcher-0.1.5/txl_launcher/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_launcher-0.1.5/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_launcher-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 txl_launcher-0.1.5/README.md
--rw-r--r--   0        0        0     1009 2020-02-02 00:00:00.000000 txl_launcher-0.1.5/pyproject.toml
--rw-r--r--   0        0        0      865 2020-02-02 00:00:00.000000 txl_launcher-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_launcher-0.1.7/txl_launcher/__init__.py
+-rw-r--r--   0        0        0     1320 2020-02-02 00:00:00.000000 txl_launcher-0.1.7/txl_launcher/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_launcher-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_launcher-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 txl_launcher-0.1.7/README.md
+-rw-r--r--   0        0        0     1009 2020-02-02 00:00:00.000000 txl_launcher-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      865 2020-02-02 00:00:00.000000 txl_launcher-0.1.7/PKG-INFO
```

### Comparing `txl_launcher-0.1.5/txl_launcher/components.py` & `txl_launcher-0.1.7/txl_launcher/components.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from asphalt.core import Component, Context
 from textual.widget import Widget
 from textual.widgets import Button
+
 from txl.base import Launcher, MainArea
 from txl.hooks import register_component
 
 
 class LauncherMeta(type(Launcher), type(Widget)):
     pass
```

### Comparing `txl_launcher-0.1.5/LICENSE.txt` & `txl_launcher-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_launcher-0.1.5/pyproject.toml` & `txl_launcher-0.1.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `txl_launcher-0.1.5/PKG-INFO` & `txl_launcher-0.1.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: txl_launcher
-Version: 0.1.5
+Version: 0.1.7
 Summary: TXL plugin for a launcher
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/launcher
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
```

