# Comparing `tmp/txl_terminal-0.1.5.tar.gz` & `tmp/txl_terminal-0.1.7.tar.gz`

## Comparing `txl_terminal-0.1.5.tar` & `txl_terminal-0.1.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_terminal-0.1.5/txl_terminal/__init__.py
--rw-r--r--   0        0        0     2824 2020-02-02 00:00:00.000000 txl_terminal-0.1.5/txl_terminal/components.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_terminal-0.1.5/.gitignore
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_terminal-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 txl_terminal-0.1.5/README.md
--rw-r--r--   0        0        0     1034 2020-02-02 00:00:00.000000 txl_terminal-0.1.5/pyproject.toml
--rw-r--r--   0        0        0      906 2020-02-02 00:00:00.000000 txl_terminal-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 txl_terminal-0.1.7/txl_terminal/__init__.py
+-rw-r--r--   0        0        0     2824 2020-02-02 00:00:00.000000 txl_terminal-0.1.7/txl_terminal/components.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 txl_terminal-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 txl_terminal-0.1.7/LICENSE.txt
+-rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 txl_terminal-0.1.7/README.md
+-rw-r--r--   0        0        0     1034 2020-02-02 00:00:00.000000 txl_terminal-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0      906 2020-02-02 00:00:00.000000 txl_terminal-0.1.7/PKG-INFO
```

### Comparing `txl_terminal-0.1.5/txl_terminal/components.py` & `txl_terminal-0.1.7/txl_terminal/components.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,17 +2,17 @@
 
 import pyte
 from asphalt.core import Component, Context
 from rich.console import RenderableType
 from rich.text import Text
 from textual import events
 from textual.widget import Widget
-from txl.base import TerminalFactory, Terminal
-from txl.hooks import register_component
 
+from txl.base import Terminal, TerminalFactory
+from txl.hooks import register_component
 
 CTRL_KEYS = {
     "left": "\u001b[D",
     "right": "\u001b[C",
     "up": "\u001b[A",
     "down": "\u001b[B",
 }
```

### Comparing `txl_terminal-0.1.5/LICENSE.txt` & `txl_terminal-0.1.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `txl_terminal-0.1.5/pyproject.toml` & `txl_terminal-0.1.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `txl_terminal-0.1.5/PKG-INFO` & `txl_terminal-0.1.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: txl_terminal
-Version: 0.1.5
+Version: 0.1.7
 Summary: TXL plugin for a terminal widget
 Project-URL: Source, https://github.com/davidbrochart/jpterm/plugins/terminal
 Author-email: David Brochart <david.brochart@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
```

