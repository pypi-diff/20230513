# Comparing `tmp/t_python_markdown-1.3.1.tar.gz` & `tmp/t_python_markdown-1.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "t_python_markdown-1.3.1.tar", last modified: Sun Apr 23 16:05:36 2023, max compression
+gzip compressed data, was "t_python_markdown-1.3.2.tar", last modified: Sat May 13 14:02:40 2023, max compression
```

## Comparing `t_python_markdown-1.3.1.tar` & `t_python_markdown-1.3.2.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-23 16:05:36.193213 t_python_markdown-1.3.1/
--rw-rw-rw-   0 root         (0) root         (0)     1062 2023-04-23 16:05:13.000000 t_python_markdown-1.3.1/LICENSE
--rw-r--r--   0 root         (0) root         (0)     7525 2023-04-23 16:05:36.192213 t_python_markdown-1.3.1/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)     5652 2023-04-23 16:05:13.000000 t_python_markdown-1.3.1/README.md
--rw-rw-rw-   0 root         (0) root         (0)      875 2023-04-23 16:05:13.000000 t_python_markdown-1.3.1/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-04-23 16:05:36.193213 t_python_markdown-1.3.1/setup.cfg
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-23 16:05:36.191213 t_python_markdown-1.3.1/t_python_markdown/
--rw-rw-rw-   0 root         (0) root         (0)      789 2023-04-23 16:05:13.000000 t_python_markdown-1.3.1/t_python_markdown/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-23 16:05:36.192213 t_python_markdown-1.3.1/t_python_markdown/extensions/
--rw-rw-rw-   0 root         (0) root         (0)       47 2023-04-23 16:05:13.000000 t_python_markdown-1.3.1/t_python_markdown/extensions/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1666 2023-04-23 16:05:13.000000 t_python_markdown-1.3.1/t_python_markdown/extensions/mkdocs.py
--rw-rw-rw-   0 root         (0) root         (0)    10281 2023-04-23 16:05:13.000000 t_python_markdown-1.3.1/t_python_markdown/t_python_markdown.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-23 16:05:36.192213 t_python_markdown-1.3.1/t_python_markdown.egg-info/
--rw-r--r--   0 root         (0) root         (0)     7525 2023-04-23 16:05:36.000000 t_python_markdown-1.3.1/t_python_markdown.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      385 2023-04-23 16:05:36.000000 t_python_markdown-1.3.1/t_python_markdown.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-04-23 16:05:36.000000 t_python_markdown-1.3.1/t_python_markdown.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       32 2023-04-23 16:05:36.000000 t_python_markdown-1.3.1/t_python_markdown.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       23 2023-04-23 16:05:36.000000 t_python_markdown-1.3.1/t_python_markdown.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:02:40.993254 t_python_markdown-1.3.2/
+-rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/LICENSE
+-rw-r--r--   0 root         (0) root         (0)     7525 2023-05-13 14:02:40.993254 t_python_markdown-1.3.2/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)     5652 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/README.md
+-rw-rw-rw-   0 root         (0) root         (0)      875 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 14:02:40.993254 t_python_markdown-1.3.2/setup.cfg
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:02:40.991254 t_python_markdown-1.3.2/t_python_markdown/
+-rw-rw-rw-   0 root         (0) root         (0)      789 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/t_python_markdown/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:02:40.992254 t_python_markdown-1.3.2/t_python_markdown/extensions/
+-rw-rw-rw-   0 root         (0) root         (0)       47 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/t_python_markdown/extensions/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1666 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/t_python_markdown/extensions/mkdocs.py
+-rw-rw-rw-   0 root         (0) root         (0)    10307 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/t_python_markdown/t_python_markdown.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:02:40.992254 t_python_markdown-1.3.2/t_python_markdown.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     7525 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      385 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       32 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       23 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/top_level.txt
```

### Comparing `t_python_markdown-1.3.1/LICENSE` & `t_python_markdown-1.3.2/LICENSE`

 * *Files identical despite different names*

### Comparing `t_python_markdown-1.3.1/PKG-INFO` & `t_python_markdown-1.3.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: t_python_markdown
-Version: 1.3.1
+Version: 1.3.2
 Summary: A simple to use markdown generator for Python.
 Author-email: t-python-markdown <t-python-markdown@toyne.cix.co.uk>
 Maintainer-email: t-python-markdown <t-python-markdown@toyne.cix.co.uk>
 License: MIT License
         
         Copyright (c) 2023 Toyne
```

### Comparing `t_python_markdown-1.3.1/README.md` & `t_python_markdown-1.3.2/README.md`

 * *Files identical despite different names*

### Comparing `t_python_markdown-1.3.1/pyproject.toml` & `t_python_markdown-1.3.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "t_python_markdown"
 description = "A simple to use markdown generator for Python."
 readme = "README.md"
-version = "1.3.1"
+version = "1.3.2"
 license = {file = "LICENSE"}
 keywords = ["markdown"]
 authors = [
     { name="t-python-markdown", email="t-python-markdown@toyne.cix.co.uk" },
 ]
 maintainers = [
     { name="t-python-markdown", email="t-python-markdown@toyne.cix.co.uk" },
```

### Comparing `t_python_markdown-1.3.1/t_python_markdown/__init__.py` & `t_python_markdown-1.3.2/t_python_markdown/__init__.py`

 * *Files identical despite different names*

### Comparing `t_python_markdown-1.3.1/t_python_markdown/extensions/mkdocs.py` & `t_python_markdown-1.3.2/t_python_markdown/extensions/mkdocs.py`

 * *Files identical despite different names*

### Comparing `t_python_markdown-1.3.1/t_python_markdown/t_python_markdown.py` & `t_python_markdown-1.3.2/t_python_markdown/t_python_markdown.py`

 * *Files 1% similar despite different names*

```diff
@@ -283,15 +283,15 @@
       o = []
     super().__init__(o)
 
   def _render(self, _parent):
     _rv = super()._render(_parent)
     if isinstance(_parent, Table):
       if markdown:
-        return markdown.markdown(_rv).replace("\n", "")
+        return markdown.markdown(_rv, extensions=['attr_list']).replace("\n", "")
       raise BadFormatException(f"Cannot embed List in {_parent.__class__.__name__} without markdown package.")
     return _rv
 
   def _render_item(self, _parent, _child, _item):
     _pad = "".join(" " for _ in range(self.__check_indent(self) * 3))
     _rv = self._render_list_item(isinstance(_child, (List)), _pad, "".join(_item))
     return _rv
```

### Comparing `t_python_markdown-1.3.1/t_python_markdown.egg-info/PKG-INFO` & `t_python_markdown-1.3.2/t_python_markdown.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: t-python-markdown
-Version: 1.3.1
+Version: 1.3.2
 Summary: A simple to use markdown generator for Python.
 Author-email: t-python-markdown <t-python-markdown@toyne.cix.co.uk>
 Maintainer-email: t-python-markdown <t-python-markdown@toyne.cix.co.uk>
 License: MIT License
         
         Copyright (c) 2023 Toyne
```

