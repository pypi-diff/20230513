# Comparing `tmp/survey-4.0.0a0.tar.gz` & `tmp/survey-4.1.0a0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "survey-4.0.0a0.tar", last modified: Sat Apr 22 16:24:32 2023, max compression
+gzip compressed data, was "survey-4.1.0a0.tar", last modified: Fri May 12 18:24:59 2023, max compression
```

## Comparing `survey-4.0.0a0.tar` & `survey-4.1.0a0.tar`

### file list

```diff
@@ -1,46 +1,46 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 16:24:32.496133 survey-4.0.0a0/
--rw-r--r--   0 runner    (1001) docker     (123)     1077 2023-04-22 16:24:17.000000 survey-4.0.0a0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1098 2023-04-22 16:24:32.496133 survey-4.0.0a0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      847 2023-04-22 16:24:17.000000 survey-4.0.0a0/README.rst
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-22 16:24:32.496133 survey-4.0.0a0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      673 2023-04-22 16:24:17.000000 survey-4.0.0a0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 16:24:32.492133 survey-4.0.0a0/survey/
--rw-r--r--   0 runner    (1001) docker     (123)      562 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5088 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_colors.py
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     2609 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_controls.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 16:24:32.496133 survey-4.0.0a0/survey/_core/
--rw-r--r--   0 runner    (1001) docker     (123)      669 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4964 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_ansi.py
--rw-r--r--   0 runner    (1001) docker     (123)     1954 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_console.py
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     7099 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_cursor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1054 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_handle.py
--rw-r--r--   0 runner    (1001) docker     (123)     1504 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_helpers.py
--rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_io.py
--rw-r--r--   0 runner    (1001) docker     (123)     1967 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_io_os.py
--rw-r--r--   0 runner    (1001) docker     (123)     2361 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_io_os_nt.py
--rw-r--r--   0 runner    (1001) docker     (123)      686 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_io_os_posix.py
--rw-r--r--   0 runner    (1001) docker     (123)     6051 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_render.py
--rw-r--r--   0 runner    (1001) docker     (123)     1900 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_screen.py
--rw-r--r--   0 runner    (1001) docker     (123)     3571 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_core/_source.py
--rw-r--r--   0 runner    (1001) docker     (123)    30907 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_funnels.py
--rw-r--r--   0 runner    (1001) docker     (123)    12548 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_graphics.py
--rw-r--r--   0 runner    (1001) docker     (123)     2482 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_handle.py
--rw-r--r--   0 runner    (1001) docker     (123)    10173 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_helpers.py
--rw-r--r--   0 runner    (1001) docker     (123)    18288 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_mutates.py
--rw-r--r--   0 runner    (1001) docker     (123)     3578 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_printers.py
--rw-r--r--   0 runner    (1001) docker     (123)    16758 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)      806 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_searches.py
--rw-r--r--   0 runner    (1001) docker     (123)     6084 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_stage.py
--rw-r--r--   0 runner    (1001) docker     (123)      489 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_system.py
--rw-r--r--   0 runner    (1001) docker     (123)     1538 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_theme.py
--rw-r--r--   0 runner    (1001) docker     (123)      543 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    10424 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_visuals.py
--rw-r--r--   0 runner    (1001) docker     (123)    58488 2023-04-22 16:24:17.000000 survey-4.0.0a0/survey/_widgets.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-22 16:24:32.492133 survey-4.0.0a0/survey.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1098 2023-04-22 16:24:32.000000 survey-4.0.0a0/survey.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      858 2023-04-22 16:24:32.000000 survey-4.0.0a0/survey.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-22 16:24:32.000000 survey-4.0.0a0/survey.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       75 2023-04-22 16:24:32.000000 survey-4.0.0a0/survey.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-04-22 16:24:32.000000 survey-4.0.0a0/survey.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:24:59.912244 survey-4.1.0a0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1077 2023-05-12 18:24:50.000000 survey-4.1.0a0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1106 2023-05-12 18:24:59.912244 survey-4.1.0a0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      855 2023-05-12 18:24:50.000000 survey-4.1.0a0/README.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 18:24:59.912244 survey-4.1.0a0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      673 2023-05-12 18:24:50.000000 survey-4.1.0a0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:24:59.908244 survey-4.1.0a0/survey/
+-rw-r--r--   0 runner    (1001) docker     (123)      562 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5088 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_colors.py
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2609 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_controls.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:24:59.912244 survey-4.1.0a0/survey/_core/
+-rw-r--r--   0 runner    (1001) docker     (123)      669 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4964 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_ansi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1954 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_console.py
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7099 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_cursor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1054 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_handle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1504 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1363 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_io.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1968 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_io_os.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2361 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_io_os_nt.py
+-rw-r--r--   0 runner    (1001) docker     (123)      686 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_io_os_posix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6051 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_render.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1900 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_screen.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3571 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_core/_source.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30907 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_funnels.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12548 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_graphics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2482 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_handle.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10173 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18288 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_mutates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3578 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_printers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16711 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)      806 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_searches.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6084 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_stage.py
+-rw-r--r--   0 runner    (1001) docker     (123)      489 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_system.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1538 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_theme.py
+-rw-r--r--   0 runner    (1001) docker     (123)      543 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10424 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_visuals.py
+-rw-r--r--   0 runner    (1001) docker     (123)    58488 2023-05-12 18:24:50.000000 survey-4.1.0a0/survey/_widgets.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 18:24:59.908244 survey-4.1.0a0/survey.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1106 2023-05-12 18:24:59.000000 survey-4.1.0a0/survey.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      858 2023-05-12 18:24:59.000000 survey-4.1.0a0/survey.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 18:24:59.000000 survey-4.1.0a0/survey.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       75 2023-05-12 18:24:59.000000 survey-4.1.0a0/survey.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-12 18:24:59.000000 survey-4.1.0a0/survey.egg-info/top_level.txt
```

### Comparing `survey-4.0.0a0/LICENSE` & `survey-4.1.0a0/LICENSE`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/PKG-INFO` & `survey-4.1.0a0/README.rst`

 * *Files 9% similar despite different names*

```diff
@@ -1,17 +1,7 @@
-Metadata-Version: 2.1
-Name: survey
-Version: 4.0.0a0
-Summary: A simple library for creating beautiful interactive prompts.
-Home-page: https://github.com/Exahilosys/survey
-License: MIT
-Requires-Python: >=3.11
-Provides-Extra: docs
-License-File: LICENSE
-
 ✨ A simple library for creating beautiful interactive prompts.
 
 .. image:: https://github.com/Exahilosys/survey/blob/main/docs/_static/images/showcase-1.gif?raw=true
 
 Features
 --------
 
@@ -22,15 +12,15 @@
 - **Complete**: Supports Windows 10 (Anniversary Update and up).
 
 Installing
 ----------
 
 .. code-block::
 
-    pip3 install survey
+    pip install survey==4.0.0a0
 
 Links
 -----
 
 - Check out the `Quickstart <https://survey.readthedocs.io/reference.html>`_ guide for more.
 - Greatly inspired by `AlecAivazis's GoLang <https://github.com/AlecAivazis/survey>`_ library.
```

### Comparing `survey-4.0.0a0/setup.py` & `survey-4.1.0a0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open('README.rst') as file:
     readme = file.read()
 
 author = 'Exahilosys'
 project = 'survey'
-version = '4.0.0-alpha'
+version = '4.1.0-alpha'
 
 url = 'https://github.com/{0}/{1}'.format(author, project)
 
 setuptools.setup(
     name = project,
     python_requires = '>=3.11',
     version = version,
```

### Comparing `survey-4.0.0a0/survey/__init__.py` & `survey-4.1.0a0/survey/__init__.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_colors.py` & `survey-4.1.0a0/survey/_colors.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_controls.py` & `survey-4.1.0a0/survey/_controls.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/__init__.py` & `survey-4.1.0a0/survey/_core/__init__.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_ansi.py` & `survey-4.1.0a0/survey/_core/_ansi.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_console.py` & `survey-4.1.0a0/survey/_core/_console.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_cursor.py` & `survey-4.1.0a0/survey/_core/_cursor.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_handle.py` & `survey-4.1.0a0/survey/_core/_handle.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_helpers.py` & `survey-4.1.0a0/survey/_core/_helpers.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_io.py` & `survey-4.1.0a0/survey/_core/_io.py`

 * *Files 18% similar despite different names*

```diff
@@ -52,26 +52,25 @@
 
         super().__init__(i.buffer, o.buffer, *args, **kwargs)
 
     def _encode(self, text):
 
         return text.encode(self._o_encoding)
 
-    def _send(self, 
-              text: str):
+    def _send(self, text):
 
         text_raw = self._encode(text)
 
         super()._send(text_raw)
 
     def _decode(self, text):
 
         return text.decode(self._i_encoding)
 
-    def _recv(self) -> str:
+    def _recv(self):
 
         text_raw = super()._recv()
 
         text = self._decode(text_raw)
 
         return text
```

### Comparing `survey-4.0.0a0/survey/_core/_io_os.py` & `survey-4.1.0a0/survey/_core/_io_os.py`

 * *Files 0% similar despite different names*

```diff
@@ -112,15 +112,15 @@
     def _send(self, value):
 
         self._o.write(value)
         self._o.flush()
 
     def _recv(self):
 
-        text = self._i.read1()
+        text = self._i.read1(1)
 
         return text
 
     def __iter__(self):
 
         while not self._i.closed:
             yield self._recv()
```

### Comparing `survey-4.0.0a0/survey/_core/_io_os_nt.py` & `survey-4.1.0a0/survey/_core/_io_os_nt.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_io_os_posix.py` & `survey-4.1.0a0/survey/_core/_io_os_posix.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_render.py` & `survey-4.1.0a0/survey/_core/_render.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_screen.py` & `survey-4.1.0a0/survey/_core/_screen.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_core/_source.py` & `survey-4.1.0a0/survey/_core/_source.py`

 * *Files 1% similar despite different names*

```diff
@@ -77,24 +77,24 @@
         self._callback = callback
         self._io = io
 
         self._lock = threading.RLock()
 
     def _get(self):
 
-        text = self._io.recv()
+        rune = self._io.recv()
 
-        if not text:
+        if not rune:
             raise _EmptyRead()
 
         if self._wait:
             self._wait = False
             self._io.wait(False)
 
-        return text
+        return rune
     
     _empty = _ansi.Escape('')
 
     def _next(self):
 
         try:
             code = _ansi.parse(self._get)
```

### Comparing `survey-4.0.0a0/survey/_funnels.py` & `survey-4.1.0a0/survey/_funnels.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_graphics.py` & `survey-4.1.0a0/survey/_graphics.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_handle.py` & `survey-4.1.0a0/survey/_handle.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_helpers.py` & `survey-4.1.0a0/survey/_helpers.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_mutates.py` & `survey-4.1.0a0/survey/_mutates.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_printers.py` & `survey-4.1.0a0/survey/_printers.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_routines.py` & `survey-4.1.0a0/survey/_routines.py`

 * *Files 1% similar despite different names*

```diff
@@ -242,16 +242,14 @@
     widget_kwargs_names = _helpers.get_function_args_names(_widgets.Inquire)
     widget_kwargs = _helpers.yank_dict(kwargs, widget_kwargs_names)
     
     options = _helpers.get_function_arg_safe(_widgets.Inquire, 'options', widget_kwargs)
     default_value = _helpers.get_function_arg_safe(_widgets.Inquire, 'default', widget_kwargs)
     default_option = next((option for (option, value) in options.items() if value == default_value), default_value)
 
-    widget_kwargs['default'] = default_option
-
     widget = _widgets.Inquire(**widget_kwargs)
 
     if not 'hint' in kwargs:
         hint_transform = lambda value: _helpers.paint_text(default_color, value.title())
         hint_segments = (hint_transform(option) if option == default_option else option for option in options)
         hint = kwargs['hint'] = '(' + '/'.join(hint_segments) + ')' + ' '
```

### Comparing `survey-4.0.0a0/survey/_searches.py` & `survey-4.1.0a0/survey/_searches.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_stage.py` & `survey-4.1.0a0/survey/_stage.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_theme.py` & `survey-4.1.0a0/survey/_theme.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_utils.py` & `survey-4.1.0a0/survey/_utils.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_visuals.py` & `survey-4.1.0a0/survey/_visuals.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey/_widgets.py` & `survey-4.1.0a0/survey/_widgets.py`

 * *Files identical despite different names*

### Comparing `survey-4.0.0a0/survey.egg-info/PKG-INFO` & `survey-4.1.0a0/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: survey
-Version: 4.0.0a0
+Version: 4.1.0a0
 Summary: A simple library for creating beautiful interactive prompts.
 Home-page: https://github.com/Exahilosys/survey
 License: MIT
 Requires-Python: >=3.11
 Provides-Extra: docs
 License-File: LICENSE
 
@@ -22,15 +22,15 @@
 - **Complete**: Supports Windows 10 (Anniversary Update and up).
 
 Installing
 ----------
 
 .. code-block::
 
-    pip3 install survey
+    pip install survey==4.0.0a0
 
 Links
 -----
 
 - Check out the `Quickstart <https://survey.readthedocs.io/reference.html>`_ guide for more.
 - Greatly inspired by `AlecAivazis's GoLang <https://github.com/AlecAivazis/survey>`_ library.
```

### Comparing `survey-4.0.0a0/survey.egg-info/SOURCES.txt` & `survey-4.1.0a0/survey.egg-info/SOURCES.txt`

 * *Files identical despite different names*

