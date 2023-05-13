# Comparing `tmp/mawk-0.1.1.tar.gz` & `tmp/mawk-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mawk-0.1.1.tar", max compression
+gzip compressed data, was "mawk-0.1.2.tar", max compression
```

## Comparing `mawk-0.1.1.tar` & `mawk-0.1.2.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0    11357 2023-05-11 14:09:29.798425 mawk-0.1.1/LICENSE
--rw-r--r--   0        0        0     2266 2023-05-11 14:09:29.798425 mawk-0.1.1/README.md
--rw-r--r--   0        0        0     3171 2023-05-11 14:09:29.798425 mawk-0.1.1/mawk.py
--rw-r--r--   0        0        0      471 2023-05-11 14:09:29.802425 mawk-0.1.1/pyproject.toml
--rw-r--r--   0        0        0     2935 1970-01-01 00:00:00.000000 mawk-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-05-13 19:24:00.617990 mawk-0.1.2/LICENSE
+-rw-r--r--   0        0        0     2266 2023-05-13 19:24:00.617990 mawk-0.1.2/README.md
+-rw-r--r--   0        0        0     3349 2023-05-13 19:24:00.617990 mawk-0.1.2/mawk.py
+-rw-r--r--   0        0        0      543 2023-05-13 19:24:00.617990 mawk-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0     2935 1970-01-01 00:00:00.000000 mawk-0.1.2/PKG-INFO
```

### Comparing `mawk-0.1.1/LICENSE` & `mawk-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `mawk-0.1.1/README.md` & `mawk-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `mawk-0.1.1/mawk.py` & `mawk-0.1.2/mawk.py`

 * *Files 9% similar despite different names*

```diff
@@ -8,70 +8,76 @@
 
 
 """Global counter to sort filters by the order in which they appear
 in a class."""
 _filter_creation_order = 0
 
 
-def match_filter(expr: str, handler: Callable[[re.Match], Optional[list[str]]], inp: str) -> Optional[list[str]]:
+def match_filter(
+    expr: str, handler: Callable[[re.Match], Optional[list[str]]], inp: str
+) -> Optional[list[str]]:
     if m := re.match(expr, inp):
         return handler(m)
     return None
 
 
 def on_match(expr: str):
     """Decorator for doing search-and-replace based on a given regex.
-    
+
     The inner function should take as argument a `re.Match` object
     and return a list of strings. The resulting decorated function
     then becomes a function from string to list of strings.
-    
+
     If the input doesn't match the given regex, the original string
     is returned.
-    
+
     The inner function may still decide to do nothing by returning None.
-    
+
     To erase the matched input return the empty list.
 
     This decorator also works on class methods. It is then assumed that
     the method has signature `(self, m: re.Match)`.
     """
+
     def _decorator(f):
         global _filter_creation_order
-        method = len(f.__qualname__.split('.')) > 1
+        method = len(f.__qualname__.split(".")) > 1
         if method:
+
             @wraps(f)
             def _impl(self, inp):
                 return match_filter(expr, partial(f, self), inp)
+
             _impl._is_rule = _filter_creation_order  # add tag to method
             _filter_creation_order += 1
             return _impl
         else:
             return wraps(f)(partial(match_filter, expr, f))
+
     return _decorator
 
 
 def always(f):
     """Suppose you have a rule with `@on_match(r".*")`, then it is better
     not to run the regex machinery at all and just pass on the string.
     In that case it is better to use `@always`."""
     global _filter_creation_order
-    method = len(f.__qualname__.split('.')) > 1
+    method = len(f.__qualname__.split(".")) > 1
     if method:
         f._is_rule = _filter_creation_order  # add tag to method
         _filter_creation_order += 1
         return f
     else:
         return f
 
 
 Rule = Callable[[str], list[str]]
 
 
-def run(rules: list[Rule], inp: str, exclusive=True) -> str:
+def run(rules: list[Rule], inp: str, exclusive=True, on_eof=None) -> str:
     """Takes a list of rules, being function from `str` to `list[str]`.
     The input string is split into lines, after which each line is fed
     through the list of rules. All the results are colected into a list
     of strings and then joined by newline.
     """
     lines = inp.splitlines()
     result = []
@@ -80,21 +86,30 @@
             v = r(l)
             if v is not None:
                 result.extend(v)
                 if exclusive:
                     break
         else:
             result.append(l)
+
+    if on_eof:
+        result.extend(on_eof())
+
     return "\n".join(result)
 
 
 class RuleSet:
     """To be used as a base class for classes that contain `on_match`
     decorated methods."""
+
     def list_rules(self):
-        members = (getattr(self, m) for m in dir(self) if m[0] != '_')
-        rules = [m for m in members if hasattr(m, '_is_rule')]
+        members = (getattr(self, m) for m in dir(self) if m[0] != "_")
+        rules = [m for m in members if hasattr(m, "_is_rule")]
         return sorted(rules, key=lambda r: r._is_rule)
 
+    def on_eof(self):
+        """This method gets called at the end of a scan."""
+        return []
+
     def run(self, inp: str, exclusive=True) -> str:
         """Runs all rules in the class on input."""
-        return run(self.list_rules(), inp, exclusive)
+        return run(self.list_rules(), inp, exclusive, on_eof=self.on_eof)
```

### Comparing `mawk-0.1.1/PKG-INFO` & `mawk-0.1.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mawk
-Version: 0.1.1
+Version: 0.1.2
 Summary: A minimalist implementation of an Awk-like model in Python
 Home-page: https://github.com/jhidding/mawk
 License: Apache 2
 Author: Johan Hidding
 Author-email: j.hidding@esciencecenter.nl
 Requires-Python: >=3.8,<4.0
 Classifier: License :: Other/Proprietary License
```

