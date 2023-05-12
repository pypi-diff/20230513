# Comparing `tmp/lazi-1.2.0.15.tar.gz` & `tmp/lazi-1.4.0.32.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lazi-1.2.0.15.tar", max compression
+gzip compressed data, was "lazi-1.4.0.32.tar", max compression
```

## Comparing `lazi-1.2.0.15.tar` & `lazi-1.4.0.32.tar`

### file list

```diff
@@ -1,13 +1,21 @@
--rw-r--r--   0        0        0    34523 2023-05-10 08:04:21.503726 lazi-1.2.0.15/LICENSE
--rw-r--r--   0        0        0     1386 2023-05-11 11:12:42.598828 lazi-1.2.0.15/README.md
--rw-r--r--   0        0        0      104 2023-05-11 08:57:20.841058 lazi-1.2.0.15/lazi/auto.py
--rw-r--r--   0        0        0       37 2023-05-11 10:10:32.878224 lazi-1.2.0.15/lazi/conf/all.py
--rw-r--r--   0        0        0      863 2023-05-11 10:10:32.874224 lazi-1.2.0.15/lazi/conf/base.py
--rw-r--r--   0        0        0      720 2023-05-11 10:24:25.485088 lazi-1.2.0.15/lazi/conf/conf.py
--rw-r--r--   0        0        0      593 2023-05-11 11:10:16.320921 lazi-1.2.0.15/lazi/core/__init__.py
--rw-r--r--   0        0        0     3173 2023-05-11 10:24:25.477088 lazi-1.2.0.15/lazi/core/finder.py
--rw-r--r--   0        0        0     2609 2023-05-11 09:48:59.517349 lazi-1.2.0.15/lazi/core/loader.py
--rw-r--r--   0        0        0     4953 2023-05-11 10:24:25.461088 lazi-1.2.0.15/lazi/core/record.py
--rw-r--r--   0        0        0      815 2023-05-11 10:00:09.202100 lazi-1.2.0.15/lazi/core/util.py
--rw-r--r--   0        0        0     1166 2023-05-11 11:16:15.941606 lazi-1.2.0.15/pyproject.toml
--rw-r--r--   0        0        0     2532 1970-01-01 00:00:00.000000 lazi-1.2.0.15/PKG-INFO
+-rw-r--r--   0        0        0    34523 2023-05-10 08:04:21.503726 lazi-1.4.0.32/LICENSE
+-rw-r--r--   0        0        0     2159 2023-05-12 22:56:51.654129 lazi-1.4.0.32/README.md
+-rw-r--r--   0        0        0      104 2023-05-11 08:57:20.841058 lazi-1.4.0.32/lazi/auto.py
+-rw-r--r--   0        0        0      284 2023-05-12 07:30:19.063612 lazi-1.4.0.32/lazi/conf/auto.py
+-rw-r--r--   0        0        0     2161 2023-05-12 21:13:16.032559 lazi-1.4.0.32/lazi/conf/base.py
+-rw-r--r--   0        0        0     4933 2023-05-12 07:30:19.043612 lazi-1.4.0.32/lazi/conf/conf.py
+-rw-r--r--   0        0        0       69 2023-05-12 21:13:16.044560 lazi-1.4.0.32/lazi/conf/test.py
+-rw-r--r--   0        0        0      663 2023-05-12 23:20:14.516521 lazi-1.4.0.32/lazi/core/__init__.py
+-rw-r--r--   0        0        0     4488 2023-05-12 22:47:20.382630 lazi-1.4.0.32/lazi/core/finder.py
+-rw-r--r--   0        0        0     3468 2023-05-12 22:52:20.018565 lazi-1.4.0.32/lazi/core/loader.py
+-rw-r--r--   0        0        0     6167 2023-05-12 23:18:02.702794 lazi-1.4.0.32/lazi/core/record.py
+-rw-r--r--   0        0        0       46 2023-05-12 00:02:04.162155 lazi-1.4.0.32/lazi/util/__init__.py
+-rw-r--r--   0        0        0      248 2023-05-11 20:06:44.097623 lazi-1.4.0.32/lazi/util/debug.py
+-rw-r--r--   0        0        0     2056 2023-05-12 23:17:59.374750 lazi-1.4.0.32/lazi/util/functional.py
+-rw-r--r--   0        0        0      618 2023-05-11 20:06:44.097623 lazi-1.4.0.32/lazi/util/util.py
+-rw-r--r--   0        0        0     1213 2023-05-12 23:27:36.566323 lazi-1.4.0.32/pyproject.toml
+-rw-r--r--   0        0        0      918 2023-05-12 22:06:26.710396 lazi-1.4.0.32/tests/test_django.py
+-rw-r--r--   0        0        0     1233 2023-05-12 07:00:36.171542 lazi-1.4.0.32/tests/test_importlib.py
+-rw-r--r--   0        0        0      120 2023-05-12 06:05:10.203013 lazi-1.4.0.32/tests/test_pandas.py
+-rw-r--r--   0        0        0      192 2023-05-12 23:21:17.805350 lazi-1.4.0.32/tests/test_record.py
+-rw-r--r--   0        0        0     3302 1970-01-01 00:00:00.000000 lazi-1.4.0.32/PKG-INFO
```

### Comparing `lazi-1.2.0.15/LICENSE` & `lazi-1.4.0.32/LICENSE`

 * *Files identical despite different names*

### Comparing `lazi-1.2.0.15/lazi/core/loader.py` & `lazi-1.4.0.32/lazi/core/loader.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,82 +1,106 @@
+import sys
 from types import ModuleType
 from importlib.util import LazyLoader
 # noinspection PyUnresolvedReferences,PyProtectedMember
 from importlib.util import _LazyModule  # type: type[ModuleType]
 
 from lazi.conf import conf
+from lazi.util import debug
 from .record import SpecRecord
-from .util import trace
 
 __all__ = "Loader",
 
 
 class Loader(LazyLoader):
     spec_record: SpecRecord
 
     def __init__(self, spec_record: SpecRecord):
         self.spec_record = spec_record
         super().__init__(spec_record.spec.loader)
 
     @property
-    def loaded(self) -> bool:
+    def used(self) -> bool:
         return self.spec_record.used
 
     def hook(self):
         assert self.spec_record.hook is True
         self.spec_record.spec.loader = self
 
     def pre_load(self):
-        return self.spec_record.pre_load()
+        self.spec_record.pre_load()
 
     def on_load(self):
-        assert self.loaded is False
+        self.spec_record.on_load()
 
-        if conf.LOADER_AUTO_DEPS:
-            for dep in (dep for dep in self.spec_record.deps if dep.spec is not None):
-                # New discovery from this: dep.spec.loader gets changed between its on_create() and here.
+    def on_load_exc(self, attr, exc):
+        return self.spec_record.on_load_exc(attr, exc)
 
-                trace("dep_load", self.spec_record.name, "->", dep.spec, dep.loader, dep.spec.loader)
+    def on_exec(self, module: ModuleType):
+        return self.spec_record.on_exec(module)
 
-                getattr(dep.module, "__path__", None)  # Force the module to load.
+    def post_exec(self, module: ModuleType) -> bool:
+        return self.spec_record.post_exec(module)
 
-        return self.spec_record.on_load()
+    def exec_module(self, module: ModuleType):
+        # TODO(?): Detect recursion issues.
 
-    def on_create(self, module: ModuleType):
-        return self.spec_record.on_create(module)
+        assert self.spec_record.spec is not None
+        assert not self.used
+
+        mdic = object.__getattribute__(module, "__dict__")
+
+        self.on_exec(module)
 
-    def exec_module(self, module: ModuleType):
-        self.on_create(module)
         super().exec_module(module)
 
+        loader_orig = self.spec_record.spec.loader
+        self.spec_record.spec.loader = self
+        mdic["__loader__"] = self
+
         # noinspection PyMethodParameters
         class LazyModule(_LazyModule):
-            def __getattribute__(self_, attr):
-                trace("getattribute", self.spec_record.name, attr)
+            def __setattr__(_, key, value):
+                debug.trace("setattribute", self.spec_record.name, key)
+                return super().__setattr__(key, value)
+
+            def __getattribute__(_, attr):
+                if attr == "__class__" or attr in conf.LOADER_FAKE_ATTR:
+                    if attr in mdic:
+                        debug.trace("geyattribute", self.spec_record.name, attr)
+                        return mdic[attr]
 
-                assert self.loaded is False
-
-                if attr in conf.LOADER_FAKE_ATTR:
-                    match attr:
-                        case "__spec__":
-                            return self.spec_record.spec
-                        case "__loader__":
-                            return self
-                        case "__name__":
-                            return self.spec_record.name
+                    debug.trace("geeattribute", self.spec_record.name, attr)
+                    raise AttributeError(attr)
 
                 self.pre_load()
 
+                self.spec_record.spec.loader = loader_orig
+                mdic["__loader__"] = loader_orig
+
                 try:
-                    trace("getattribute", self.spec_record.name, attr, "load")
-                    return _LazyModule.__getattribute__(self_, attr)  # Errors here are from the import two lines above (in trace)
+                    debug.trace("getattribute", self.spec_record.name, attr, "<load>")
+                    valu = _LazyModule.__getattribute__(_, attr)
 
-                except Exception:
-                    raise
+                except Exception as exc:
+                    self.on_load_exc(attr, exc)
+                    raise AttributeError(attr) from exc
 
-                finally:
+                else:
                     self.on_load()
+                    return valu
 
-            def __delattr__(self_, attr):
-                return _LazyModule.__delattr__(self_,  attr)
+                finally:
+                    if mdic.get("__class__", LazyModule) is LazyModule:
+                        self.spec_record.spec.loader = self
+                        mdic["__loader__"] = self
+
+            def __delattr__(_, attr):
+                return _LazyModule.__delattr__(_,  attr)
 
         module.__class__ = LazyModule
+
+        if self.post_exec(module) and conf.LOADER_AUTO_DEPS:
+            # Bypass lazy loading in recursive situations (called here indirectly between pre_load and on_load).
+            debug.trace("exec_module", self.spec_record.name, "<force>")
+            # return self.spec_record.loader.exec_module(module)
+            getattr(module, "__dict__", None)  # Force the module to load.
```

### Comparing `lazi-1.2.0.15/pyproject.toml` & `lazi-1.4.0.32/pyproject.toml`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "lazi"
-version = "1.2.0.15"
+version = "1.4.0.32"
 description = "A lightweight and extensible way to implement lazy imports globally."
 authors = ["Phillip Sitbon <phillip.sitbon@gmail.com>"]
 readme = "README.md"
 license = "AGPLv3"
 repository = "https://github.com/sitbon/lazi"
 classifiers= [
     "Environment :: Web Environment",
@@ -18,28 +18,31 @@
     "Programming Language :: Python :: 3.11",
     "Programming Language :: Python :: 3 :: Only",
     "Topic :: Software Development :: Libraries",
 ]
 
 packages = [
     { include = "lazi" },
+    { include = "tests", format = "sdist" }
 ]
 
 
 [tool.poetry.group.dev]
 optional = true
 
 [tool.poetry.group.dev.dependencies]
-django = "^4.2.1"
-requests = "^2.30.0"
-toolz = "^0.12.0"
-rich = "^13.3.5"
-setuptools = "^67.7.2"
+django = "^4"
+requests = "^2"
+toolz = "^0"
+rich = "^13"
+setuptools = "^67"
+pandas = "^2"
+pytest = "^7"
 
 
 [tool.poetry.dependencies]
-python = ">=3.10,<4"
+python = ">=3.10"
 
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `lazi-1.2.0.15/PKG-INFO` & `lazi-1.4.0.32/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: lazi
-Version: 1.2.0.15
+Version: 1.4.0.32
 Summary: A lightweight and extensible way to implement lazy imports globally.
 Home-page: https://github.com/sitbon/lazi
 License: AGPLv3
 Author: Phillip Sitbon
 Author-email: phillip.sitbon@gmail.com
-Requires-Python: >=3.10,<4
+Requires-Python: >=3.10
 Classifier: Environment :: Web Environment
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3 or later (AGPLv3+)
 Classifier: License :: Other/Proprietary License
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
@@ -48,15 +48,15 @@
 ```
 
 ```shell
 python example.py
 ```
 
 ```python
-5
+0
 211
 ```
 
 ```python
 """Manual lazy loading example.
 """
 import lazi.core                        # Import Lazi.
@@ -64,18 +64,43 @@
 django_test = lazi.lazy("django.test")  # Import more stuff.
 print(lazi.used_count())                # Count loaded modules.
 TestCase = django_test.TestCase         # Trigger lazy loading.
 print(lazi.used_count())                # Module was lazy loaded.
 ```
 
 ```python
-1
+0
 2
 ```
 
+## Configuration
+
+The `lazi.conf` namespace package contains configuration modules
+that get autoloaded (in import order) by `lazi.conf.conf`.
+It is fully decoupled from the rest of the codebase.
+
+As a result, it's possible configure Lazi by creating `lazi.conf`
+modules in your project (within the `lazi.conf` namespace package),
+and use conf modules provided by other packages.
+
+Configuration is not yet controllable via environment variables,
+but this is planned for the future.
+
+It's also possible to manually change the configuration at runtime,
+with the caveat that some variables may have already been used by
+`lazi.core`. To avoid this, configure Lazi before importing it:
+
+```python
+from lazi.conf import conf
+conf.DEBUG_TRACING = True
+import lazi.auto
+# ...
+```
+
+
 ## Metadata
 
 Reference for developers: The json dict below contains Python versioning parameters:
 - Soft `min` (ignore rev) & hard `max` compatible versions.
 - Recommended `use` & creator's environment `dev` versions.
 
 ```json
```

