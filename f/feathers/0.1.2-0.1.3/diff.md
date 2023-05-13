# Comparing `tmp/feathers-0.1.2.tar.gz` & `tmp/feathers-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "feathers-0.1.2.tar", max compression
+gzip compressed data, was "feathers-0.1.3.tar", max compression
```

## Comparing `feathers-0.1.2.tar` & `feathers-0.1.3.tar`

### file list

```diff
@@ -1,19 +1,25 @@
--rw-r--r--   0        0        0       29 2023-05-11 13:14:26.704562 feathers-0.1.2/README.md
--rw-r--r--   0        0        0        0 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/__init__.py
--rw-r--r--   0        0        0       53 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/__main__.py
--rw-r--r--   0        0        0     5955 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/cache.py
--rw-r--r--   0        0        0      161 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/demo.py
--rw-r--r--   0        0        0       64 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/utils/__init__.py
--rw-r--r--   0        0        0      763 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/utils/_errors.py
--rw-r--r--   0        0        0      202 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/__init__.py
--rw-r--r--   0        0        0     5737 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/_cached_view.py
--rw-r--r--   0        0        0     9016 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/_nav_view.py
--rw-r--r--   0        0        0      118 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/help/__init__.py
--rw-r--r--   0        0        0     1125 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/help/_base.py
--rw-r--r--   0        0        0     3684 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/help/_help.py
--rw-r--r--   0        0        0     5784 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/help/_long_help.py
--rw-r--r--   0        0        0      714 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/help/_models.py
--rw-r--r--   0        0        0     3999 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/help/_short_help.py
--rw-r--r--   0        0        0     1307 2023-05-11 13:14:26.704562 feathers-0.1.2/feathers/widgets/help/_utils.py
--rw-r--r--   0        0        0      907 2023-05-11 13:14:26.708562 feathers-0.1.2/pyproject.toml
--rw-r--r--   0        0        0      816 1970-01-01 00:00:00.000000 feathers-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0       29 2023-05-13 06:59:34.277125 feathers-0.1.3/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/__init__.py
+-rw-r--r--   0        0        0       53 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/__main__.py
+-rw-r--r--   0        0        0     5996 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/cache.py
+-rw-r--r--   0        0        0      161 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/demo.py
+-rw-r--r--   0        0        0       71 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/renderables/__init__.py
+-rw-r--r--   0        0        0     3187 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/renderables/_divider.py
+-rw-r--r--   0        0        0       64 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/utils/__init__.py
+-rw-r--r--   0        0        0      763 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/utils/_errors.py
+-rw-r--r--   0        0        0      202 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/widgets/__init__.py
+-rw-r--r--   0        0        0     5932 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/widgets/_cached_view.py
+-rw-r--r--   0        0        0     9016 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/widgets/_nav_view.py
+-rw-r--r--   0        0        0      146 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/widgets/chat/__init__.py
+-rw-r--r--   0        0        0     2445 2023-05-13 06:59:34.277125 feathers-0.1.3/feathers/widgets/chat/_chat.py
+-rw-r--r--   0        0        0     1113 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/chat/_models.py
+-rw-r--r--   0        0        0     2193 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/chat/_renderers.py
+-rw-r--r--   0        0        0      118 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/help/__init__.py
+-rw-r--r--   0        0        0     1125 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/help/_base.py
+-rw-r--r--   0        0        0     3684 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/help/_help.py
+-rw-r--r--   0        0        0     5784 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/help/_long_help.py
+-rw-r--r--   0        0        0      714 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/help/_models.py
+-rw-r--r--   0        0        0     3999 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/help/_short_help.py
+-rw-r--r--   0        0        0     1307 2023-05-13 06:59:34.281126 feathers-0.1.3/feathers/widgets/help/_utils.py
+-rw-r--r--   0        0        0      907 2023-05-13 06:59:34.281126 feathers-0.1.3/pyproject.toml
+-rw-r--r--   0        0        0      816 1970-01-01 00:00:00.000000 feathers-0.1.3/PKG-INFO
```

### Comparing `feathers-0.1.2/feathers/cache.py` & `feathers-0.1.3/feathers/cache.py`

 * *Files 3% similar despite different names*

```diff
@@ -121,14 +121,15 @@
         # By iterating over the list in reverse order, we can safely remove items without changing
         # the indices of the remaining items in the list. This approach can be more memory-efficient
         # than making a copy of the list to iterate over, especially for large lists, since we only need
         # to keep track of the current index and don't need to create a copy of the list.
         for i in range(len(self._cache) - 1, -1, -1):
             if id in self._cache[i]:
                 self._cache.pop(i)
+        self._refresh_virtual_size()
 
     def _extract_lines(
         self,
         renderable: RenderableWithOptions,
     ) -> list[Strip] | None:
         renderableType, width, expand, shrink, wrap = (
             renderable.renderableType,
@@ -156,20 +157,19 @@
         if not lines:
             return None
 
         strips = Strip.from_lines(lines)
         for strip in strips:
             strip.adjust_cell_length(render_width)
 
-        max_width = max(sum([segment.cell_length for segment in strip]) for strip in strips)
+        max_width = max(strip.cell_length for strip in strips)
         new_width = max(self._virtual_size.width, max_width)
         new_height = self._virtual_size.height + len(strips)
         self._virtual_size = Size(new_width, new_height)
-
-        # self.max_width = max(
-        #     self.max_width,
-        #     sum([segment.cell_length for segment in strip]),
-        # )
         return strips
 
+    def _refresh_virtual_size(self):
+        max_width = max(strip[1].cell_length for strip in self._cache)
+        self._virtual_size = Size(max_width, len(self._cache))
+
     def __len__(self) -> int:
         return len(self._cache)
```

### Comparing `feathers-0.1.2/feathers/utils/_errors.py` & `feathers-0.1.3/feathers/utils/_errors.py`

 * *Files identical despite different names*

### Comparing `feathers-0.1.2/feathers/widgets/_cached_view.py` & `feathers-0.1.3/feathers/widgets/_cached_view.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,22 +21,24 @@
     # shows up for few characters on first call to `on_resize`
     DEFAULT_CSS = """
     CachedView{
         scrollbar-gutter: stable;
     }
     """
 
+    max_width: int | None = None
     wrap: bool = False
     highlight: bool = False
     markup: bool = False
     auto_scroll: bool = True
 
     def __init__(
         self,
         *,
+        max_width: int | None = None,
         wrap: bool = False,
         highlight: bool = False,
         markup: bool = False,
         auto_scroll: bool = True,
         enable_cursor: bool = False,
         name: str | None = None,
         id: str | None = None,
@@ -53,14 +55,16 @@
             enable_cursor: Enable cursor which name this view navigable. This also make this view focusable.
             name: The name of the text log.
             id: The ID of the text log in the DOM.
             classes: The CSS classes of the text log.
             disabled: Whether the text log is disabled or not.
         """
         super().__init__(disable_cursor=not enable_cursor, name=name, id=id, classes=classes, disabled=disabled)
+        self.max_width = max_width
+        """Enforce max width of all the content"""
         self.wrap = wrap
         """Enable word wrapping."""
         self.highlight = highlight
         """Automatically highlight content."""
         self.markup = markup
         """Apply Rich console markup."""
         self.auto_scroll = auto_scroll
@@ -87,15 +91,15 @@
                 if self.highlighter is not None:
                     renderable = self.highlighter(renderable)
             else:
                 renderable = cast(RenderableType, content)
 
         return RenderableWithOptions(renderable, width, expand, shrink, self.wrap)
 
-    def write(
+    def add(
         self,
         content: RenderableType | object,
         width: int | None = None,
         expand: bool = False,
         shrink: bool = True,
         scroll_end: bool | None = None,
     ) -> CachedView:
@@ -109,14 +113,15 @@
             shrink: Enable shrinking of content to fit width.
             scroll_end: Enable automatic scroll to end, or `None` to use `self.auto_scroll`.
 
         Returns:
             The `TextLog` instance.
         """
 
+        width = width or self.max_width
         renderable = self._extract_renderable(content, width, expand, shrink)
         self._renderables_cache.add(renderable)
 
         auto_scroll = self.auto_scroll if scroll_end is None else scroll_end
         if auto_scroll:
             self.scroll_end(animate=False)
```

### Comparing `feathers-0.1.2/feathers/widgets/_nav_view.py` & `feathers-0.1.3/feathers/widgets/_nav_view.py`

 * *Files identical despite different names*

### Comparing `feathers-0.1.2/feathers/widgets/help/_base.py` & `feathers-0.1.3/feathers/widgets/help/_base.py`

 * *Files identical despite different names*

### Comparing `feathers-0.1.2/feathers/widgets/help/_help.py` & `feathers-0.1.3/feathers/widgets/help/_help.py`

 * *Files identical despite different names*

### Comparing `feathers-0.1.2/feathers/widgets/help/_long_help.py` & `feathers-0.1.3/feathers/widgets/help/_long_help.py`

 * *Files identical despite different names*

### Comparing `feathers-0.1.2/feathers/widgets/help/_models.py` & `feathers-0.1.3/feathers/widgets/help/_models.py`

 * *Files identical despite different names*

### Comparing `feathers-0.1.2/feathers/widgets/help/_short_help.py` & `feathers-0.1.3/feathers/widgets/help/_short_help.py`

 * *Files identical despite different names*

### Comparing `feathers-0.1.2/feathers/widgets/help/_utils.py` & `feathers-0.1.3/feathers/widgets/help/_utils.py`

 * *Files identical despite different names*

### Comparing `feathers-0.1.2/pyproject.toml` & `feathers-0.1.3/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "feathers"
-version = "0.1.2"
+version = "0.1.3"
 description = "Beautiful TUI components written on top of Textual"
 authors = ["Shashank Tomar <shashank004@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "feathers"}]
 repository = "https://github.com/shashanktomar/feathers"
 keywords = ["textual", "terminal", "TUI"]
```

### Comparing `feathers-0.1.2/PKG-INFO` & `feathers-0.1.3/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: feathers
-Version: 0.1.2
+Version: 0.1.3
 Summary: Beautiful TUI components written on top of Textual
 Home-page: https://github.com/shashanktomar/feathers
 License: MIT
 Keywords: textual,terminal,TUI
 Author: Shashank Tomar
 Author-email: shashank004@gmail.com
 Requires-Python: >=3.8,<4.0
```

