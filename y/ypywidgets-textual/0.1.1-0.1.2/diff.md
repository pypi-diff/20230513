# Comparing `tmp/ypywidgets_textual-0.1.1.tar.gz` & `tmp/ypywidgets_textual-0.1.2.tar.gz`

## Comparing `ypywidgets_textual-0.1.1.tar` & `ypywidgets_textual-0.1.2.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.1/ypywidgets_textual/__init__.py
--rw-r--r--   0        0        0      675 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.1/ypywidgets_textual/switch.py
--rw-r--r--   0        0        0      488 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.1/ypywidgets_textual/txl/switch.py
--rw-r--r--   0        0        0       53 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.1/README.md
--rw-r--r--   0        0        0      815 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.1/pyproject.toml
--rw-r--r--   0        0        0      474 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.2/ypywidgets_textual/__init__.py
+-rw-r--r--   0        0        0      539 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.2/ypywidgets_textual/switch.py
+-rw-r--r--   0        0        0      558 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.2/ypywidgets_textual/txl/switch.py
+-rw-r--r--   0        0        0       53 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.2/README.md
+-rw-r--r--   0        0        0      817 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0      476 2020-02-02 00:00:00.000000 ypywidgets_textual-0.1.2/PKG-INFO
```

### Comparing `ypywidgets_textual-0.1.1/ypywidgets_textual/switch.py` & `ypywidgets_textual-0.1.2/ypywidgets_textual/switch.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,27 +1,21 @@
-from ypywidgets import Widget
+from ypywidgets import Widget, reactive
 
 
 class Switch(Widget):
 
-    def __init__(self, value: bool = False, open_comm: bool = True) -> None:
-        super().__init__(name="switch", open_comm=open_comm)
-        self.yvalue = self.ydoc.get_map("value")
-        self._set(value)
-
-    def _set(self, value: bool) -> None:
-        with self.ydoc.begin_transaction() as t:
-            self.yvalue.set(t, "value",  value)
-
-    @property
-    def value(self) -> bool:
-        return self.yvalue["value"]
-
-    @value.setter
-    def value(self, value: bool):
-        if value == self.value:
-            return
+    value = reactive(False)
 
-        self._set(value)
+    def __init__(self, value: bool = False, primary: bool = True) -> None:
+        super().__init__(primary=primary)
+        self.value_change_callbacks = []
+        self.value = value
 
     def toggle(self):
         self.value = not self.value
+
+    def on_value_change(self, cb):
+        self.value_change_callbacks.append(cb)
+
+    def watch_value(self, value: bool) -> None:
+        for cb in self.value_change_callbacks:
+            cb(value)
```

### Comparing `ypywidgets_textual-0.1.1/pyproject.toml` & `ypywidgets_textual-0.1.2/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -15,25 +15,25 @@
 keywords = [
     "widgets",
     "jupyter",
     "ypy",
     "textual",
 ]
 dependencies = [
-    "ypywidgets >=0.2.0",
-    "textual >=0.11",
+    "ypywidgets >=0.4.0",
+    "textual >=0.24.1",
 ]
 
 [project.urls]
 Homepage = "https://github.com/davidbrochart/ypywidgets-textual"
 
 [tool.hatch.version]
 path = "ypywidgets_textual/__init__.py"
 
 [tool.hatch.build.targets.sdist]
 include = [
     "/ypywidgets_textual",
 ]
 
 [project.entry-points.ypywidgets]
-switch = "ypywidgets_textual.switch:Switch"
-txl_switch = "ypywidgets_textual.txl.switch:Switch"
+Switch = "ypywidgets_textual.switch:Switch"
+txl_Switch = "ypywidgets_textual.txl.switch:Switch"
```

