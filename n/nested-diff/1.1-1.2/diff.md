# Comparing `tmp/nested_diff-1.1.tar.gz` & `tmp/nested_diff-1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nested_diff-1.1.tar", last modified: Sun Nov 27 18:09:14 2022, max compression
+gzip compressed data, was "nested_diff-1.2.tar", last modified: Fri May 12 22:11:02 2023, max compression
```

## Comparing `nested_diff-1.1.tar` & `nested_diff-1.2.tar`

### file list

```diff
@@ -1,21 +1,30 @@
-drwxrwxr-x   0 mixas     (1000) mixas     (1000)        0 2022-11-27 18:09:14.345785 nested_diff-1.1/
--rw-rw-r--   0 mixas     (1000) mixas     (1000)    11357 2022-11-27 18:08:35.000000 nested_diff-1.1/LICENSE
--rw-rw-r--   0 mixas     (1000) mixas     (1000)     5666 2022-11-27 18:09:14.345785 nested_diff-1.1/PKG-INFO
--rw-rw-r--   0 mixas     (1000) mixas     (1000)     4250 2022-11-27 18:08:35.000000 nested_diff-1.1/README.md
-drwxrwxr-x   0 mixas     (1000) mixas     (1000)        0 2022-11-27 18:09:14.341785 nested_diff-1.1/nested_diff/
--rw-rw-r--   0 mixas     (1000) mixas     (1000)    10697 2022-11-27 18:08:35.000000 nested_diff-1.1/nested_diff/__init__.py
--rw-rw-r--   0 mixas     (1000) mixas     (1000)    12900 2022-11-27 18:08:35.000000 nested_diff-1.1/nested_diff/cli.py
--rw-rw-r--   0 mixas     (1000) mixas     (1000)     9263 2022-11-27 18:08:35.000000 nested_diff-1.1/nested_diff/diff_tool.py
--rw-rw-r--   0 mixas     (1000) mixas     (1000)    12687 2022-11-27 18:08:35.000000 nested_diff-1.1/nested_diff/formatters.py
--rw-rw-r--   0 mixas     (1000) mixas     (1000)    19709 2022-11-27 18:08:35.000000 nested_diff-1.1/nested_diff/handlers.py
--rw-rw-r--   0 mixas     (1000) mixas     (1000)     2423 2022-11-27 18:08:35.000000 nested_diff-1.1/nested_diff/patch_tool.py
-drwxrwxr-x   0 mixas     (1000) mixas     (1000)        0 2022-11-27 18:09:14.345785 nested_diff-1.1/nested_diff.egg-info/
--rw-rw-r--   0 mixas     (1000) mixas     (1000)     5666 2022-11-27 18:09:14.000000 nested_diff-1.1/nested_diff.egg-info/PKG-INFO
--rw-rw-r--   0 mixas     (1000) mixas     (1000)      416 2022-11-27 18:09:14.000000 nested_diff-1.1/nested_diff.egg-info/SOURCES.txt
--rw-rw-r--   0 mixas     (1000) mixas     (1000)        1 2022-11-27 18:09:14.000000 nested_diff-1.1/nested_diff.egg-info/dependency_links.txt
--rw-rw-r--   0 mixas     (1000) mixas     (1000)      100 2022-11-27 18:09:14.000000 nested_diff-1.1/nested_diff.egg-info/entry_points.txt
--rw-rw-r--   0 mixas     (1000) mixas     (1000)        1 2022-11-27 18:09:14.000000 nested_diff-1.1/nested_diff.egg-info/not-zip-safe
--rw-rw-r--   0 mixas     (1000) mixas     (1000)       19 2022-11-27 18:09:14.000000 nested_diff-1.1/nested_diff.egg-info/requires.txt
--rw-rw-r--   0 mixas     (1000) mixas     (1000)       12 2022-11-27 18:09:14.000000 nested_diff-1.1/nested_diff.egg-info/top_level.txt
--rw-rw-r--   0 mixas     (1000) mixas     (1000)       38 2022-11-27 18:09:14.345785 nested_diff-1.1/setup.cfg
--rw-rw-r--   0 mixas     (1000) mixas     (1000)     1946 2022-11-27 18:08:35.000000 nested_diff-1.1/setup.py
+drwxrwxr-x   0 mixas     (1000) mixas     (1000)        0 2023-05-12 22:11:02.506249 nested_diff-1.2/
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)    11357 2023-05-12 22:09:24.000000 nested_diff-1.2/LICENSE
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     6088 2023-05-12 22:11:02.506249 nested_diff-1.2/PKG-INFO
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     4672 2023-05-12 22:09:24.000000 nested_diff-1.2/README.md
+drwxrwxr-x   0 mixas     (1000) mixas     (1000)        0 2023-05-12 22:11:02.506249 nested_diff-1.2/nested_diff/
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)    10776 2023-05-12 22:09:24.000000 nested_diff-1.2/nested_diff/__init__.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)    12900 2023-05-12 22:09:24.000000 nested_diff-1.2/nested_diff/cli.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     9263 2023-05-12 22:09:24.000000 nested_diff-1.2/nested_diff/diff_tool.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)    12734 2023-05-12 22:09:24.000000 nested_diff-1.2/nested_diff/formatters.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)    20316 2023-05-12 22:09:24.000000 nested_diff-1.2/nested_diff/handlers.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     2433 2023-05-12 22:09:24.000000 nested_diff-1.2/nested_diff/patch_tool.py
+drwxrwxr-x   0 mixas     (1000) mixas     (1000)        0 2023-05-12 22:11:02.506249 nested_diff-1.2/nested_diff.egg-info/
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     6088 2023-05-12 22:11:02.000000 nested_diff-1.2/nested_diff.egg-info/PKG-INFO
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)      602 2023-05-12 22:11:02.000000 nested_diff-1.2/nested_diff.egg-info/SOURCES.txt
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)        1 2023-05-12 22:11:02.000000 nested_diff-1.2/nested_diff.egg-info/dependency_links.txt
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)      100 2023-05-12 22:11:02.000000 nested_diff-1.2/nested_diff.egg-info/entry_points.txt
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)        1 2023-05-12 22:11:02.000000 nested_diff-1.2/nested_diff.egg-info/not-zip-safe
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)       19 2023-05-12 22:11:02.000000 nested_diff-1.2/nested_diff.egg-info/requires.txt
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)       12 2023-05-12 22:11:02.000000 nested_diff-1.2/nested_diff.egg-info/top_level.txt
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)       38 2023-05-12 22:11:02.506249 nested_diff-1.2/setup.cfg
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     1946 2023-05-12 22:09:24.000000 nested_diff-1.2/setup.py
+drwxrwxr-x   0 mixas     (1000) mixas     (1000)        0 2023-05-12 22:11:02.506249 nested_diff-1.2/tests/
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     1710 2023-05-12 22:09:24.000000 nested_diff-1.2/tests/test_custom_containers.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     3018 2023-05-12 22:09:24.000000 nested_diff-1.2/tests/test_diff.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)      629 2023-05-12 22:09:24.000000 nested_diff-1.2/tests/test_fmt_html.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)      629 2023-05-12 22:09:24.000000 nested_diff-1.2/tests/test_fmt_term.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)      629 2023-05-12 22:09:24.000000 nested_diff-1.2/tests/test_fmt_text.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     1280 2023-05-12 22:09:24.000000 nested_diff-1.2/tests/test_handlers.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     3157 2023-05-12 22:09:24.000000 nested_diff-1.2/tests/test_iterator.py
+-rw-rw-r--   0 mixas     (1000) mixas     (1000)     2216 2023-05-12 22:09:24.000000 nested_diff-1.2/tests/test_patch.py
```

### Comparing `nested_diff-1.1/LICENSE` & `nested_diff-1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `nested_diff-1.1/PKG-INFO` & `nested_diff-1.2/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nested_diff
-Version: 1.1
+Version: 1.2
 Summary: Recursive diff for nested structures
 Home-page: https://github.com/mr-mixas/Nested-Diff.py
 Author: Michael Samoglyadov
 Author-email: mixas.sr@gmail.com
 License: Apache License 2.0
 Keywords: diff nested-diff recursive-diff nested-data data-structures
 Classifier: Development Status :: 4 - Beta
@@ -28,42 +28,54 @@
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Description-Content-Type: text/markdown
 Provides-Extra: cli
 License-File: LICENSE
 
 # Nested-Diff.py
 
-Recursive diff and patch for nested structures. **[Live Demo](https://nesteddiff.pythonanywhere.com/)**
+Recursive diff and patch for nested structures.
 
 [![Tests Status](https://github.com/mr-mixas/Nested-Diff.py/actions/workflows/tests.yml/badge.svg)](https://github.com/mr-mixas/Nested-Diff.py/actions?query=branch%3Amaster)
 [![Coverage Status](https://coveralls.io/repos/github/mr-mixas/Nested-Diff.py/badge.svg)](https://coveralls.io/github/mr-mixas/Nested-Diff.py)
 [![Supported Python versions](https://img.shields.io/pypi/pyversions/nested_diff.svg)](https://pypi.org/project/nested_diff/)
 [![License](https://img.shields.io/pypi/l/nested_diff.svg)](https://pypi.org/project/nested_diff/)
 
+## Main features
+
+* Mashine-readable diff structure.
+* Human-friendly diff visualization, collapsible html diffs.
+* All operation tags are optional and may be disabled.
+* Extensibility.
+
+**[See Live Demo!](https://nesteddiff.pythonanywhere.com/)**
+
 ## Install
 
 `pip install nested_diff`
 
 For extra formats support (YAML, TOML) in cli tools, use
 
 `pip install nested_diff[cli]`
 
 ## Command line tools
 
 ```
-mixas:~/$ cat a.json b.json
+$ cat a.json b.json
 [0, [1],    3]
 [0, [1, 2], 3]
-mixas:~/$ nested_diff a.json b.json
+```
+```
+$ nested_diff a.json b.json
   [1]
 +   [1]
 +     2
-mixas:~/$
-mixas:~/$ nested_diff a.json b.json --ofmt json > patch.json
-mixas:~/$ nested_patch a.json patch.json
+```
+```
+$ nested_diff a.json b.json --ofmt json > patch.json
+$ nested_patch a.json patch.json
 ```
 
 ## Library usage
 
 ```
 >>> from nested_diff import diff, patch
 >>>
@@ -84,36 +96,38 @@
 >>> assert c == d
 >>>
 ```
 
 ### Formatting diffs
 
 ```
->>> from nested_diff import diff
+>>> from nested_diff import diff, handlers
 >>> from nested_diff.formatters import TextFormatter
 >>>
 >>> a = {'one': 1, 'two': 'some\ntext\ninside'}
 >>> b = {'one': 0, 'two': 'some\ntext'}
 >>>
->>> d = diff(a, b, U=False, text_diff_ctx=3)
+>>> d = diff(a, b, U=False, extra_handlers=[handlers.TextHandler(context=3)])
 >>> print(TextFormatter().format(d))
   {'one'}
 -   1
 +   0
   {'two'}
 #   <str>
     @@ -1,3 +1,2 @@
     some
     text
 -   inside
 <BLANKLINE>
 >>>
 ```
 
-See more examples in [HOWTO](./HOWTO.md) and [tests](./tests/).
+For more examples see [Live Demo](https://nesteddiff.pythonanywhere.com/),
+[HOWTO](https://github.com/mr-mixas/Nested-Diff.py/blob/master/HOWTO.md) and
+[tests](https://github.com/mr-mixas/Nested-Diff.py/tree/master/tests).
 
 ## Diff structure
 
 Diff is a dict and may contain status keys:
 
 * `A` stands for 'added', it's value - added item.
 * `D` means 'different' and contains subdiff.
@@ -165,13 +179,13 @@
 
 ## License
 
 Licensed under the terms of the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).
 
 ## See Also
 
-[HOWTO](./HOWTO.md)
+[HOWTO](https://github.com/mr-mixas/Nested-Diff.py/blob/master/HOWTO.md)
 
 [deepdiff](https://pypi.org/project/deepdiff/),
 [jsondiff](https://pypi.org/project/jsondiff/),
 [jsonpatch](https://pypi.org/project/jsonpatch/),
 [json-delta](https://pypi.org/project/json-delta/)
```

### Comparing `nested_diff-1.1/README.md` & `nested_diff-1.2/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -1,37 +1,49 @@
 # Nested-Diff.py
 
-Recursive diff and patch for nested structures. **[Live Demo](https://nesteddiff.pythonanywhere.com/)**
+Recursive diff and patch for nested structures.
 
 [![Tests Status](https://github.com/mr-mixas/Nested-Diff.py/actions/workflows/tests.yml/badge.svg)](https://github.com/mr-mixas/Nested-Diff.py/actions?query=branch%3Amaster)
 [![Coverage Status](https://coveralls.io/repos/github/mr-mixas/Nested-Diff.py/badge.svg)](https://coveralls.io/github/mr-mixas/Nested-Diff.py)
 [![Supported Python versions](https://img.shields.io/pypi/pyversions/nested_diff.svg)](https://pypi.org/project/nested_diff/)
 [![License](https://img.shields.io/pypi/l/nested_diff.svg)](https://pypi.org/project/nested_diff/)
 
+## Main features
+
+* Mashine-readable diff structure.
+* Human-friendly diff visualization, collapsible html diffs.
+* All operation tags are optional and may be disabled.
+* Extensibility.
+
+**[See Live Demo!](https://nesteddiff.pythonanywhere.com/)**
+
 ## Install
 
 `pip install nested_diff`
 
 For extra formats support (YAML, TOML) in cli tools, use
 
 `pip install nested_diff[cli]`
 
 ## Command line tools
 
 ```
-mixas:~/$ cat a.json b.json
+$ cat a.json b.json
 [0, [1],    3]
 [0, [1, 2], 3]
-mixas:~/$ nested_diff a.json b.json
+```
+```
+$ nested_diff a.json b.json
   [1]
 +   [1]
 +     2
-mixas:~/$
-mixas:~/$ nested_diff a.json b.json --ofmt json > patch.json
-mixas:~/$ nested_patch a.json patch.json
+```
+```
+$ nested_diff a.json b.json --ofmt json > patch.json
+$ nested_patch a.json patch.json
 ```
 
 ## Library usage
 
 ```
 >>> from nested_diff import diff, patch
 >>>
@@ -52,36 +64,38 @@
 >>> assert c == d
 >>>
 ```
 
 ### Formatting diffs
 
 ```
->>> from nested_diff import diff
+>>> from nested_diff import diff, handlers
 >>> from nested_diff.formatters import TextFormatter
 >>>
 >>> a = {'one': 1, 'two': 'some\ntext\ninside'}
 >>> b = {'one': 0, 'two': 'some\ntext'}
 >>>
->>> d = diff(a, b, U=False, text_diff_ctx=3)
+>>> d = diff(a, b, U=False, extra_handlers=[handlers.TextHandler(context=3)])
 >>> print(TextFormatter().format(d))
   {'one'}
 -   1
 +   0
   {'two'}
 #   <str>
     @@ -1,3 +1,2 @@
     some
     text
 -   inside
 <BLANKLINE>
 >>>
 ```
 
-See more examples in [HOWTO](./HOWTO.md) and [tests](./tests/).
+For more examples see [Live Demo](https://nesteddiff.pythonanywhere.com/),
+[HOWTO](https://github.com/mr-mixas/Nested-Diff.py/blob/master/HOWTO.md) and
+[tests](https://github.com/mr-mixas/Nested-Diff.py/tree/master/tests).
 
 ## Diff structure
 
 Diff is a dict and may contain status keys:
 
 * `A` stands for 'added', it's value - added item.
 * `D` means 'different' and contains subdiff.
@@ -133,13 +147,13 @@
 
 ## License
 
 Licensed under the terms of the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).
 
 ## See Also
 
-[HOWTO](./HOWTO.md)
+[HOWTO](https://github.com/mr-mixas/Nested-Diff.py/blob/master/HOWTO.md)
 
 [deepdiff](https://pypi.org/project/deepdiff/),
 [jsondiff](https://pypi.org/project/jsondiff/),
 [jsonpatch](https://pypi.org/project/jsonpatch/),
 [json-delta](https://pypi.org/project/json-delta/)
```

### Comparing `nested_diff-1.1/nested_diff/__init__.py` & `nested_diff-1.2/nested_diff/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # -*- coding: utf-8 -*-
 #
-# Copyright 2018-2022 Michael Samoglyadov
+# Copyright 2018-2023 Michael Samoglyadov
 #
 # Licensed under the Apache License, Version 2.0 (the "License");
 # you may not use this file except in compliance with the License.
 # You may obtain a copy of the License at
 #
 #     http://www.apache.org/licenses/LICENSE-2.0
 #
@@ -18,15 +18,15 @@
 
 from warnings import warn
 
 import nested_diff.handlers
 
 __all__ = ['Differ', 'Iterator', 'Patcher', 'diff', 'patch']
 
-__version__ = '1.1'
+__version__ = '1.2'
 __author__ = 'Michael Samoglyadov'
 __license__ = 'Apache License, Version 2.0'
 __website__ = 'https://github.com/mr-mixas/Nested-Diff.py'
 
 DEFAULT_HANDLER = nested_diff.handlers.TypeHandler()
 
 TYPE_HANDLERS = (
@@ -309,32 +309,36 @@
         """
         self._iters_by_cls[handler.handled_type] = handler.iterate_diff
 
         if handler.extension_id is not None:
             self._iters_by_ext[handler.extension_id] = handler.iterate_diff
 
 
-def diff(a, b, text_diff_ctx=-1, **kwargs):
+def diff(a, b, extra_handlers=(), text_diff_ctx=-1, **kwargs):
     """Calculate diff for two objects.
 
     Args:
         a: First object to diff.
         b: Second object to diff.
+        extra_handlers: List of additional type handlers.
         text_diff_ctx: Amount of context lines for text (multiline strings)
             diffs. Disabled entirely when value is negative. This opt is
             deprecated and should be avoided.
         kwargs: Passed to Differ's constructor as is.
 
     Returns:
-        Tuple: equality flag and nested diff.
+        Tuple: nested diff.
 
     """
     differ = Differ(**kwargs)
 
-    if text_diff_ctx >= 0 and kwargs.get('N', True) and kwargs.get('O', True):
+    for handler in extra_handlers:
+        differ.set_handler(handler)
+
+    if text_diff_ctx >= 0:
         warn('`text_diff_ctx` opt is deprecated and will be removed soon',
              DeprecationWarning, stacklevel=2)
 
         differ.set_handler(nested_diff.handlers.TextHandler(
             context=text_diff_ctx))
 
     return differ.diff(a, b)[1]
```

### Comparing `nested_diff-1.1/nested_diff/cli.py` & `nested_diff-1.2/nested_diff/cli.py`

 * *Files identical despite different names*

### Comparing `nested_diff-1.1/nested_diff/diff_tool.py` & `nested_diff-1.2/nested_diff/diff_tool.py`

 * *Files identical despite different names*

### Comparing `nested_diff-1.1/nested_diff/formatters.py` & `nested_diff-1.2/nested_diff/formatters.py`

 * *Files 1% similar despite different names*

```diff
@@ -160,15 +160,16 @@
         try:
             comment = diff['C']
         except KeyError:
             if extension_id is not None and self.type_hints:
                 yield from self.generate_string(
                     self._type_by_ext[extension_id].__name__, 'E', depth)
         else:
-            yield from self.generate_string(comment, 'C', depth)
+            for line in comment.splitlines():
+                yield from self.generate_string(line, 'C', depth)
 
         yield from generator(self, diff, depth)
 
         yield self.diff_suffix
 
     def generate_key(self, key, tag, diff_type, depth):
         """Generate key line."""
```

### Comparing `nested_diff-1.1/nested_diff/handlers.py` & `nested_diff-1.2/nested_diff/handlers.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # -*- coding: utf-8 -*-
 #
-# Copyright 2022 Michael Samoglyadov
+# Copyright 2022-2023 Michael Samoglyadov
 #
 # Licensed under the Apache License, Version 2.0 (the "License");
 # you may not use this file except in compliance with the License.
 # You may obtain a copy of the License at
 #
 #     http://www.apache.org/licenses/LICENSE-2.0
 #
@@ -13,14 +13,15 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 """Type handlers for nedted diff."""
 
 from difflib import SequenceMatcher
+from math import isnan
 from pickle import dumps
 
 
 class TypeHandler():
     """Base class for type handlers.
 
     Handlers provide diff, patch, generate_formatted_diff and iterate_diff
@@ -146,14 +147,37 @@
 
 
 class FloatHandler(ScalarHandler):
     """float handler."""
 
     handled_type = float
 
+    def __init__(self, nans_equal=False):
+        """Initialize handler.
+
+        Args:
+            nans_equal: When True treat NaN (not a number) as equal to NaN.
+
+        """
+        super().__init__()
+
+        if nans_equal:
+            orig_diff_method = self.diff
+
+            def _diff_nan_wrapper(differ, a, b):
+                if isnan(a) and isnan(b):
+                    if differ.op_u:
+                        return True, {'U': a}
+
+                    return True, {}
+
+                return orig_diff_method(differ, a, b)
+
+            self.diff = _diff_nan_wrapper
+
 
 class StrHandler(ScalarHandler):
     """str handler."""
 
     handled_type = str
```

### Comparing `nested_diff-1.1/nested_diff/patch_tool.py` & `nested_diff-1.2/nested_diff/patch_tool.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # -*- coding: utf-8 -*-
 #
-# Copyright 2019-2022 Michael Samoglyadov
+# Copyright 2019-2023 Michael Samoglyadov
 #
 # Licensed under the Apache License, Version 2.0 (the "License");
 # you may not use this file except in compliance with the License.
 # You may obtain a copy of the License at
 #
 #     http://www.apache.org/licenses/LICENSE-2.0
 #
@@ -68,15 +68,15 @@
             target: Object to patch.
             diff: Nested diff.
 
         Returns:
             Patched object.
 
         """
-        return nested_diff.patch(target, diff)
+        return nested_diff.Patcher().patch(target, diff)
 
     def run(self):
         """Patch app object entry point."""
         patched = self.patch(
             self.load(self.args.target_file),
             self.load(self.args.patch_file),
         )
```

### Comparing `nested_diff-1.1/nested_diff.egg-info/PKG-INFO` & `nested_diff-1.2/nested_diff.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nested-diff
-Version: 1.1
+Version: 1.2
 Summary: Recursive diff for nested structures
 Home-page: https://github.com/mr-mixas/Nested-Diff.py
 Author: Michael Samoglyadov
 Author-email: mixas.sr@gmail.com
 License: Apache License 2.0
 Keywords: diff nested-diff recursive-diff nested-data data-structures
 Classifier: Development Status :: 4 - Beta
@@ -28,42 +28,54 @@
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Description-Content-Type: text/markdown
 Provides-Extra: cli
 License-File: LICENSE
 
 # Nested-Diff.py
 
-Recursive diff and patch for nested structures. **[Live Demo](https://nesteddiff.pythonanywhere.com/)**
+Recursive diff and patch for nested structures.
 
 [![Tests Status](https://github.com/mr-mixas/Nested-Diff.py/actions/workflows/tests.yml/badge.svg)](https://github.com/mr-mixas/Nested-Diff.py/actions?query=branch%3Amaster)
 [![Coverage Status](https://coveralls.io/repos/github/mr-mixas/Nested-Diff.py/badge.svg)](https://coveralls.io/github/mr-mixas/Nested-Diff.py)
 [![Supported Python versions](https://img.shields.io/pypi/pyversions/nested_diff.svg)](https://pypi.org/project/nested_diff/)
 [![License](https://img.shields.io/pypi/l/nested_diff.svg)](https://pypi.org/project/nested_diff/)
 
+## Main features
+
+* Mashine-readable diff structure.
+* Human-friendly diff visualization, collapsible html diffs.
+* All operation tags are optional and may be disabled.
+* Extensibility.
+
+**[See Live Demo!](https://nesteddiff.pythonanywhere.com/)**
+
 ## Install
 
 `pip install nested_diff`
 
 For extra formats support (YAML, TOML) in cli tools, use
 
 `pip install nested_diff[cli]`
 
 ## Command line tools
 
 ```
-mixas:~/$ cat a.json b.json
+$ cat a.json b.json
 [0, [1],    3]
 [0, [1, 2], 3]
-mixas:~/$ nested_diff a.json b.json
+```
+```
+$ nested_diff a.json b.json
   [1]
 +   [1]
 +     2
-mixas:~/$
-mixas:~/$ nested_diff a.json b.json --ofmt json > patch.json
-mixas:~/$ nested_patch a.json patch.json
+```
+```
+$ nested_diff a.json b.json --ofmt json > patch.json
+$ nested_patch a.json patch.json
 ```
 
 ## Library usage
 
 ```
 >>> from nested_diff import diff, patch
 >>>
@@ -84,36 +96,38 @@
 >>> assert c == d
 >>>
 ```
 
 ### Formatting diffs
 
 ```
->>> from nested_diff import diff
+>>> from nested_diff import diff, handlers
 >>> from nested_diff.formatters import TextFormatter
 >>>
 >>> a = {'one': 1, 'two': 'some\ntext\ninside'}
 >>> b = {'one': 0, 'two': 'some\ntext'}
 >>>
->>> d = diff(a, b, U=False, text_diff_ctx=3)
+>>> d = diff(a, b, U=False, extra_handlers=[handlers.TextHandler(context=3)])
 >>> print(TextFormatter().format(d))
   {'one'}
 -   1
 +   0
   {'two'}
 #   <str>
     @@ -1,3 +1,2 @@
     some
     text
 -   inside
 <BLANKLINE>
 >>>
 ```
 
-See more examples in [HOWTO](./HOWTO.md) and [tests](./tests/).
+For more examples see [Live Demo](https://nesteddiff.pythonanywhere.com/),
+[HOWTO](https://github.com/mr-mixas/Nested-Diff.py/blob/master/HOWTO.md) and
+[tests](https://github.com/mr-mixas/Nested-Diff.py/tree/master/tests).
 
 ## Diff structure
 
 Diff is a dict and may contain status keys:
 
 * `A` stands for 'added', it's value - added item.
 * `D` means 'different' and contains subdiff.
@@ -165,13 +179,13 @@
 
 ## License
 
 Licensed under the terms of the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).
 
 ## See Also
 
-[HOWTO](./HOWTO.md)
+[HOWTO](https://github.com/mr-mixas/Nested-Diff.py/blob/master/HOWTO.md)
 
 [deepdiff](https://pypi.org/project/deepdiff/),
 [jsondiff](https://pypi.org/project/jsondiff/),
 [jsonpatch](https://pypi.org/project/jsonpatch/),
 [json-delta](https://pypi.org/project/json-delta/)
```

### Comparing `nested_diff-1.1/setup.py` & `nested_diff-1.2/setup.py`

 * *Files identical despite different names*

