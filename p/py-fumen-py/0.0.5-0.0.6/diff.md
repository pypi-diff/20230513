# Comparing `tmp/py_fumen_py-0.0.5.tar.gz` & `tmp/py_fumen_py-0.0.6.tar.gz`

## Comparing `py_fumen_py-0.0.5.tar` & `py_fumen_py-0.0.6.tar`

### file list

```diff
@@ -1,16 +1,16 @@
--rw-r--r--   0        0        0      241 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/__init__.py
--rw-r--r--   0        0        0     4063 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/action.py
--rw-r--r--   0        0        0     1046 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/comment.py
--rw-r--r--   0        0        0      798 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/constant.py
--rw-r--r--   0        0        0    10786 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/field.py
--rw-r--r--   0        0        0     8437 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/fumen_buffer.py
--rw-r--r--   0        0        0     3531 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/fumen_codec.py
--rw-r--r--   0        0        0     1265 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/js_escape.py
--rw-r--r--   0        0        0     6723 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/operation.py
--rw-r--r--   0        0        0     1380 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/page.py
--rw-r--r--   0        0        0     4104 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/src/py_fumen_py/quiz.py
--rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/.gitignore
--rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/LICENSE
--rw-r--r--   0        0        0     2254 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/README.md
--rw-r--r--   0        0        0      524 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/pyproject.toml
--rw-r--r--   0        0        0     2696 2020-02-02 00:00:00.000000 py_fumen_py-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0      241 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/__init__.py
+-rw-r--r--   0        0        0     4063 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/action.py
+-rw-r--r--   0        0        0     1046 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/comment.py
+-rw-r--r--   0        0        0      798 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/constant.py
+-rw-r--r--   0        0        0    10823 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/field.py
+-rw-r--r--   0        0        0     8437 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/fumen_buffer.py
+-rw-r--r--   0        0        0     3531 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/fumen_codec.py
+-rw-r--r--   0        0        0     1265 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/js_escape.py
+-rw-r--r--   0        0        0     6723 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/operation.py
+-rw-r--r--   0        0        0     1380 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/page.py
+-rw-r--r--   0        0        0     4104 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/src/py_fumen_py/quiz.py
+-rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/.gitignore
+-rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/LICENSE
+-rw-r--r--   0        0        0     2273 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/README.md
+-rw-r--r--   0        0        0      524 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/pyproject.toml
+-rw-r--r--   0        0        0     2715 2020-02-02 00:00:00.000000 py_fumen_py-0.0.6/PKG-INFO
```

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/action.py` & `py_fumen_py-0.0.6/src/py_fumen_py/action.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/comment.py` & `py_fumen_py-0.0.6/src/py_fumen_py/comment.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/constant.py` & `py_fumen_py-0.0.6/src/py_fumen_py/constant.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/field.py` & `py_fumen_py-0.0.6/src/py_fumen_py/field.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,16 @@
 from .constant import FieldConstants as Consts
 from .operation import Mino, Rotation, Operation
 
 class Field:
     """Keep data of a Tetris playing field."""
     @staticmethod
     def _empty_lines(height):
-        return [[Mino._] * Consts.WIDTH for y in range(height)]
+        empty_lines = [[Mino._] * Consts.WIDTH for y in range(height)]
+        return empty_lines[:]
 
     @staticmethod
     def _to_field_range(slice_=slice(None, None, None)):
         # Convert a normal slice to a suitable range in the field
         return range(
             -Consts.GARBAGE_HEIGHT if slice_.start is None else slice_.start,
             Consts.HEIGHT if slice_.stop is None else slice_.stop,
@@ -61,15 +62,15 @@
     def __setitem__(self, key, value):
         """Modify specified line(s) in the field
         The key can be an int (for one line) or a slice (for a set of lines)
         Negative values in slices are deemed as indexing of garbage lines,
         instead of counting from the end of the field.
         """
         if isinstance(key, slice):
-            range_ = self._to_field_range(slice)
+            range_ = self._to_field_range(key)
             if range_.step == 1:
                 if range_.start >= 0 and range_.stop >= 0:
                     self._field[range_.start:range_.stop] = value
                 elif range_.start < 0 and range_.stop < 0:
                     self._garbage[-range_.start-1:
                                   -range_.stop-1] = reversed(value)
                 elif range_.start < 0 and range_.stop >= 0:
@@ -174,28 +175,28 @@
         mirror_color: if the L-J and Z-S color swap should happen. (default:
             False)
         """
         for line in self:
             line[:] = [mino.mirrored() if mirror_color else mino
                        for mino in reversed(line)]
 
-    def shfit_up(self, amount=1):
+    def shift_up(self, amount=1):
         """Shift the playing field upwards.
         Keyword arguments:
         amount: (default: 1)
         """
         self[amount:] = self[0:Consts.HEIGHT-amount]
-        self[:amount] = self._empty_lines(amount)
+        self[0:amount] = self._empty_lines(amount)
 
     def shift_down(self, amount=1):
         """Shift the playing field downwards.
         Keyword arguments:
         amount: (default: 1)
         """
-        self[:Consts.HEIGHT-amount] = self[amount:]
+        self[0:Consts.HEIGHT-amount] = self[amount:]
         self[Consts.HEIGHT-amount:] = self._empty_lines(amount)
 
     def shift_left(self, amount=1, warp=False):
         """Shift or warp the playing field to the left.
         Keyword arguments:
         amount: (default: 1)
         warp: if the left-most columns should be warpped to the right.
```

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/fumen_buffer.py` & `py_fumen_py-0.0.6/src/py_fumen_py/fumen_buffer.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/fumen_codec.py` & `py_fumen_py-0.0.6/src/py_fumen_py/fumen_codec.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/js_escape.py` & `py_fumen_py-0.0.6/src/py_fumen_py/js_escape.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/operation.py` & `py_fumen_py-0.0.6/src/py_fumen_py/operation.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/page.py` & `py_fumen_py-0.0.6/src/py_fumen_py/page.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/src/py_fumen_py/quiz.py` & `py_fumen_py-0.0.6/src/py_fumen_py/quiz.py`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/.gitignore` & `py_fumen_py-0.0.6/.gitignore`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/LICENSE` & `py_fumen_py-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `py_fumen_py-0.0.5/README.md` & `py_fumen_py-0.0.6/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 ## Usage
 ```python
 from py_fumen_py import *
 ```
 
 ### Module
 
-> **`bold names`** are automatically imported with `from py_fumen_py import *`
+* **`bold names`** are automatically imported with `from py_fumen_py import *`
 
 |Name|Description|Importable Names|
 |:-|:-|:-|
 |`action`|Codec for action in a fumen string|`Action`, `ActionCodec`|
 |`comment`|Codec for comment in a fumen string |`CommentCodec`|
 |`constant`|Constants used in the project|**`FieldConstants`**, `FieldConstants110`, **`FumenStringConstants`**|
 |`field`|Playing field object|**`Field`**|
@@ -67,8 +67,8 @@
 - Action encoding and decoding are moved to `action`
 - Comment encoding and decoding are moved to `comment`
 - Added `FieldConstants110` to `constant` to accomodate for Fumen version `110`
 - `decoder` and `encoder` are combined into one `fumen-codec` module
 - `field` and `inner_field` are combined into one `field` module
 - Action, comment and field reading/writing are moved to `fumen_buffer`
 - Placement tetrimino `enum` objects are moved to `operation`
-- `quiz` works completely differently (based on [](fumen.zui.jp) instead of `tetris-fumen`)
+- `quiz` works completely differently (based on [this editor](https://fumen.zui.jp) instead of `tetris-fumen`)
```

### Comparing `py_fumen_py-0.0.5/pyproject.toml` & `py_fumen_py-0.0.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "py_fumen_py"
-version = "0.0.5"
+version = "0.0.6"
 authors = [
 	{ name="Octupus Tea" },
 ]
 description = "Python implementation of the JavaScript package 'tetris-fumen'"
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
```

### Comparing `py_fumen_py-0.0.5/PKG-INFO` & `py_fumen_py-0.0.6/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py_fumen_py
-Version: 0.0.5
+Version: 0.0.6
 Summary: Python implementation of the JavaScript package 'tetris-fumen'
 Project-URL: Source, https://github.com/OctupusTea/py-fumen-py
 Author: Octupus Tea
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
@@ -20,15 +20,15 @@
 ## Usage
 ```python
 from py_fumen_py import *
 ```
 
 ### Module
 
-> **`bold names`** are automatically imported with `from py_fumen_py import *`
+* **`bold names`** are automatically imported with `from py_fumen_py import *`
 
 |Name|Description|Importable Names|
 |:-|:-|:-|
 |`action`|Codec for action in a fumen string|`Action`, `ActionCodec`|
 |`comment`|Codec for comment in a fumen string |`CommentCodec`|
 |`constant`|Constants used in the project|**`FieldConstants`**, `FieldConstants110`, **`FumenStringConstants`**|
 |`field`|Playing field object|**`Field`**|
@@ -80,8 +80,8 @@
 - Action encoding and decoding are moved to `action`
 - Comment encoding and decoding are moved to `comment`
 - Added `FieldConstants110` to `constant` to accomodate for Fumen version `110`
 - `decoder` and `encoder` are combined into one `fumen-codec` module
 - `field` and `inner_field` are combined into one `field` module
 - Action, comment and field reading/writing are moved to `fumen_buffer`
 - Placement tetrimino `enum` objects are moved to `operation`
-- `quiz` works completely differently (based on [](fumen.zui.jp) instead of `tetris-fumen`)
+- `quiz` works completely differently (based on [this editor](https://fumen.zui.jp) instead of `tetris-fumen`)
```

