# Comparing `tmp/t_python_markdown-1.3.2.tar.gz` & `tmp/t_python_markdown-1.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "t_python_markdown-1.3.2.tar", last modified: Sat May 13 14:02:40 2023, max compression
+gzip compressed data, was "t_python_markdown-1.4.0.tar", last modified: Sat May 13 19:29:16 2023, max compression
```

## Comparing `t_python_markdown-1.3.2.tar` & `t_python_markdown-1.4.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:02:40.993254 t_python_markdown-1.3.2/
--rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/LICENSE
--rw-r--r--   0 root         (0) root         (0)     7525 2023-05-13 14:02:40.993254 t_python_markdown-1.3.2/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)     5652 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/README.md
--rw-rw-rw-   0 root         (0) root         (0)      875 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 14:02:40.993254 t_python_markdown-1.3.2/setup.cfg
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:02:40.991254 t_python_markdown-1.3.2/t_python_markdown/
--rw-rw-rw-   0 root         (0) root         (0)      789 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/t_python_markdown/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:02:40.992254 t_python_markdown-1.3.2/t_python_markdown/extensions/
--rw-rw-rw-   0 root         (0) root         (0)       47 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/t_python_markdown/extensions/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1666 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/t_python_markdown/extensions/mkdocs.py
--rw-rw-rw-   0 root         (0) root         (0)    10307 2023-05-13 14:02:20.000000 t_python_markdown-1.3.2/t_python_markdown/t_python_markdown.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:02:40.992254 t_python_markdown-1.3.2/t_python_markdown.egg-info/
--rw-r--r--   0 root         (0) root         (0)     7525 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      385 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       32 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       23 2023-05-13 14:02:40.000000 t_python_markdown-1.3.2/t_python_markdown.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:29:16.875731 t_python_markdown-1.4.0/
+-rw-rw-rw-   0 root         (0) root         (0)     1062 2023-05-13 19:28:57.000000 t_python_markdown-1.4.0/LICENSE
+-rw-r--r--   0 root         (0) root         (0)     4225 2023-05-13 19:29:16.875731 t_python_markdown-1.4.0/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)     2351 2023-05-13 19:28:57.000000 t_python_markdown-1.4.0/README.md
+-rw-rw-rw-   0 root         (0) root         (0)      875 2023-05-13 19:28:57.000000 t_python_markdown-1.4.0/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 19:29:16.875731 t_python_markdown-1.4.0/setup.cfg
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:29:16.873731 t_python_markdown-1.4.0/t_python_markdown/
+-rw-rw-rw-   0 root         (0) root         (0)      789 2023-05-13 19:28:57.000000 t_python_markdown-1.4.0/t_python_markdown/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:29:16.875731 t_python_markdown-1.4.0/t_python_markdown/extensions/
+-rw-rw-rw-   0 root         (0) root         (0)       47 2023-05-13 19:28:57.000000 t_python_markdown-1.4.0/t_python_markdown/extensions/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1666 2023-05-13 19:28:57.000000 t_python_markdown-1.4.0/t_python_markdown/extensions/mkdocs.py
+-rw-rw-rw-   0 root         (0) root         (0)    11048 2023-05-13 19:28:57.000000 t_python_markdown-1.4.0/t_python_markdown/t_python_markdown.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 19:29:16.874731 t_python_markdown-1.4.0/t_python_markdown.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     4225 2023-05-13 19:29:16.000000 t_python_markdown-1.4.0/t_python_markdown.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      385 2023-05-13 19:29:16.000000 t_python_markdown-1.4.0/t_python_markdown.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 19:29:16.000000 t_python_markdown-1.4.0/t_python_markdown.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       32 2023-05-13 19:29:16.000000 t_python_markdown-1.4.0/t_python_markdown.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       23 2023-05-13 19:29:16.000000 t_python_markdown-1.4.0/t_python_markdown.egg-info/top_level.txt
```

### Comparing `t_python_markdown-1.3.2/LICENSE` & `t_python_markdown-1.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `t_python_markdown-1.3.2/pyproject.toml` & `t_python_markdown-1.4.0/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "t_python_markdown"
 description = "A simple to use markdown generator for Python."
 readme = "README.md"
-version = "1.3.2"
+version = "1.4.0"
 license = {file = "LICENSE"}
 keywords = ["markdown"]
 authors = [
     { name="t-python-markdown", email="t-python-markdown@toyne.cix.co.uk" },
 ]
 maintainers = [
     { name="t-python-markdown", email="t-python-markdown@toyne.cix.co.uk" },
```

### Comparing `t_python_markdown-1.3.2/t_python_markdown/__init__.py` & `t_python_markdown-1.4.0/t_python_markdown/__init__.py`

 * *Files identical despite different names*

### Comparing `t_python_markdown-1.3.2/t_python_markdown/extensions/mkdocs.py` & `t_python_markdown-1.4.0/t_python_markdown/extensions/mkdocs.py`

 * *Files identical despite different names*

### Comparing `t_python_markdown-1.3.2/t_python_markdown/t_python_markdown.py` & `t_python_markdown-1.4.0/t_python_markdown/t_python_markdown.py`

 * *Files 3% similar despite different names*

```diff
@@ -35,14 +35,22 @@
   @property
   def root(self):
     """Returns root element"""
     if self._parent:
       return self._parent.root
     return self
 
+  def _is_parent_class(self, _class):
+    """Returns if parent class is of type"""
+    if self._parent:
+      if isinstance(self._parent, _class):
+        return True
+      return self._parent._is_parent_class(_class)  # pylint: disable=W0212
+    return False
+
   @property
   def output(self):
     """Returns rendered markdown document"""
     _rv = self._render(None).split("\n")
     _rv = [_ for _lc, _ in enumerate(_rv) if not _lc or len(_) or (len(_rv[_lc - 1]) != len(_))]
     return "\n".join(_rv)
 
@@ -63,14 +71,22 @@
     self.__add_child(_p2)
 
   def __add_child(self, _child):
     if isinstance(_child, MarkdownElement):
       if _child._parent:  # pylint: disable=W0212
         raise Exception(f"Already has parent: {_child} -> {_child._render(_child._parent)}")  # pylint: disable=W0212,W0719
       _child._parent = self  # pylint: disable=W0212
+
+    elif isinstance(_child, list):
+      for _c in _child:
+        if isinstance(_c, MarkdownElement):
+          if _c._parent:  # pylint: disable=W0212
+            raise Exception(f"Already has parent: {_c} -> {_c._render(_c._parent)}")  # pylint: disable=W0212,W0719
+          _c._parent = self  # pylint: disable=W0212
+
     self.__children.append(_child)
 
   def _render(self, _parent):
     _rv = []
     if isinstance(self, ChildlessMarkdownElement):
       _rv.append(self._render_item(_parent, None, None))
     else:
@@ -281,15 +297,15 @@
   def __init__(self, o=None):
     if o is None:
       o = []
     super().__init__(o)
 
   def _render(self, _parent):
     _rv = super()._render(_parent)
-    if isinstance(_parent, Table):
+    if isinstance(_parent, Table) or (_parent and _parent._is_parent_class(Table)):  # pylint: disable=W0212
       if markdown:
         return markdown.markdown(_rv, extensions=['attr_list']).replace("\n", "")
       raise BadFormatException(f"Cannot embed List in {_parent.__class__.__name__} without markdown package.")
     return _rv
 
   def _render_item(self, _parent, _child, _item):
     _pad = "".join(" " for _ in range(self.__check_indent(self) * 3))
@@ -350,15 +366,15 @@
     self.__alignment = alignment[0:_lh]
     self.__alignment.extend([next(reversed(alignment), ":-:") for _ in range(_lh - len(alignment))])
 
   def _render(self, _parent):
     _rv = super()._render(_parent)
     header = "|" + "|".join(list(self.__format_header(x) for x in self.__heading)) + "|"
     alignment = "|" + "|".join(list(f" {_} " for _ in self.__alignment)) + "|"
-    if isinstance(_parent, (Table, List)):
+    if isinstance(_parent, (Table, List)) or (_parent and _parent._is_parent_class((Table, List))):  # pylint: disable=W0212
       if markdown:
         return markdown.markdown(f"{header}\n{alignment}\n{_rv}", extensions=['tables', 'attr_list']).replace("\n", "")
       raise BadFormatException(f"Cannot embed Table in {_parent.__class__.__name__} without markdown package.")
     return f"\n\n{header}\n{alignment}\n{_rv}\n"
 
   def __format_header(self, _o):
     if _o:
```

