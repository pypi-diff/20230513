# Comparing `tmp/nepattern-0.5.6.tar.gz` & `tmp/nepattern-0.5.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nepattern-0.5.6.tar", last modified: Wed May  3 12:22:38 2023, max compression
+gzip compressed data, was "nepattern-0.5.7.tar", last modified: Sat May 13 07:29:42 2023, max compression
```

## Comparing `nepattern-0.5.6.tar` & `nepattern-0.5.7.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0     1091 2022-01-24 11:14:57.524000 nepattern-0.5.6/LICENSE
--rw-r--r--   0        0        0      703 2023-04-17 06:05:25.529605 nepattern-0.5.6/nepattern/__init__.py
--rw-r--r--   0        0        0     8946 2023-05-03 08:23:13.426003 nepattern-0.5.6/nepattern/base.py
--rw-r--r--   0        0        0     4010 2023-03-31 19:06:53.737926 nepattern-0.5.6/nepattern/context.py
--rw-r--r--   0        0        0     1419 2023-04-17 06:19:02.570290 nepattern-0.5.6/nepattern/context.pyi
--rw-r--r--   0        0        0    15857 2023-05-03 08:15:17.438046 nepattern-0.5.6/nepattern/core.py
--rw-r--r--   0        0        0       63 2022-08-22 03:10:58.502097 nepattern-0.5.6/nepattern/exception.py
--rw-r--r--   0        0        0       26 2023-04-17 06:05:25.556543 nepattern-0.5.6/nepattern/i18n/.config.json
--rw-r--r--   0        0        0      381 2023-04-17 06:05:25.502608 nepattern-0.5.6/nepattern/i18n/en-US.json
--rw-r--r--   0        0        0      353 2023-04-17 06:05:25.567509 nepattern-0.5.6/nepattern/i18n/zh-CN.json
--rw-r--r--   0        0        0    10277 2023-05-03 08:25:00.521491 nepattern-0.5.6/nepattern/main.py
--rw-r--r--   0        0        0      695 2023-04-17 06:21:36.032925 nepattern-0.5.6/nepattern/util.py
--rw-r--r--   0        0        0     1738 2023-05-03 08:26:17.522535 nepattern-0.5.6/pyproject.toml
--rw-r--r--   0        0        0      943 2023-02-25 11:05:27.501329 nepattern-0.5.6/README.md
--rw-r--r--   0        0        0     1625 1970-01-01 00:00:00.000000 nepattern-0.5.6/PKG-INFO
+-rw-r--r--   0        0        0     1091 2022-01-24 11:14:57.524000 nepattern-0.5.7/LICENSE
+-rw-r--r--   0        0        0      703 2023-04-17 06:05:25.529605 nepattern-0.5.7/nepattern/__init__.py
+-rw-r--r--   0        0        0     8966 2023-05-13 07:03:55.942573 nepattern-0.5.7/nepattern/base.py
+-rw-r--r--   0        0        0     4010 2023-03-31 19:06:53.737926 nepattern-0.5.7/nepattern/context.py
+-rw-r--r--   0        0        0     1419 2023-04-17 06:19:02.570290 nepattern-0.5.7/nepattern/context.pyi
+-rw-r--r--   0        0        0    15857 2023-05-03 08:15:17.438046 nepattern-0.5.7/nepattern/core.py
+-rw-r--r--   0        0        0       63 2022-08-22 03:10:58.502097 nepattern-0.5.7/nepattern/exception.py
+-rw-r--r--   0        0        0       26 2023-04-17 06:05:25.556543 nepattern-0.5.7/nepattern/i18n/.config.json
+-rw-r--r--   0        0        0      381 2023-04-17 06:05:25.502608 nepattern-0.5.7/nepattern/i18n/en-US.json
+-rw-r--r--   0        0        0      353 2023-04-17 06:05:25.567509 nepattern-0.5.7/nepattern/i18n/zh-CN.json
+-rw-r--r--   0        0        0    10277 2023-05-03 08:25:00.521491 nepattern-0.5.7/nepattern/main.py
+-rw-r--r--   0        0        0      695 2023-04-17 06:21:36.032925 nepattern-0.5.7/nepattern/util.py
+-rw-r--r--   0        0        0     1738 2023-05-13 07:29:18.513282 nepattern-0.5.7/pyproject.toml
+-rw-r--r--   0        0        0      943 2023-02-25 11:05:27.501329 nepattern-0.5.7/README.md
+-rw-r--r--   0        0        0     1625 1970-01-01 00:00:00.000000 nepattern-0.5.7/PKG-INFO
```

### Comparing `nepattern-0.5.6/LICENSE` & `nepattern-0.5.7/LICENSE`

 * *Files identical despite different names*

### Comparing `nepattern-0.5.6/nepattern/__init__.py` & `nepattern-0.5.7/nepattern/__init__.py`

 * *Files identical despite different names*

### Comparing `nepattern-0.5.6/nepattern/base.py` & `nepattern-0.5.7/nepattern/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -63,15 +63,15 @@
                 if (res := pat.validate(text)).success:
                     return res.value
             raise MatchFailed(
                 lang.require("nepattern", "content_error").format(target=text)
             )
         return text
 
-    def __repr__(self):
+    def __calc_repr__(self):
         return ("!" if self.anti else "") + (
             "|".join(repr(a) for a in (*self.for_validate, *self.for_equal))
         )
 
     def prefixed(self) -> UnionPattern:
         from .main import type_parser
 
@@ -149,15 +149,15 @@
             raise fail[0][1]
         if self._mode == "pre" and fail:
             return self.origin(i[1] for i in success if i[0] < fail[0][0])
         if self._mode == "suf" and fail:
             return self.origin(i[1] for i in success if i[0] > fail[-1][0])
         return self.origin(i[1] for i in success)
 
-    def __repr__(self):
+    def __calc_repr__(self):
         return f"{self.origin.__name__}[{self.base}]"
 
     def prefixed(self) -> SequencePattern:
         self._mode = "pre"
         return super(SequencePattern, self).prefixed()
 
     def suffixed(self) -> SequencePattern:
@@ -222,15 +222,15 @@
             raise fail[0][1]
         if self._mode == "pre" and fail:
             return {i[1]: i[2] for i in success if i[0] < fail[0][0]}
         if self._mode == "suf" and fail:
             return {i[1]: i[2] for i in success if i[0] > fail[-1][0]}
         return {i[1]: i[2] for i in success}
 
-    def __repr__(self):
+    def __calc_repr__(self):
         return f"dict[{self.key.origin.__name__}, {self.value}]"
 
     def prefixed(self) -> MappingPattern:
         self._mode = "pre"
         return super(MappingPattern, self).prefixed()
 
     def suffixed(self) -> MappingPattern:
@@ -244,15 +244,15 @@
 class SwitchPattern(BasePattern[_TCase]):
     switch: dict[Any, _TCase]
 
     def __init__(self, data: dict[Any | ellipsis, _TCase]):
         self.switch = data
         super().__init__("", MatchMode.TYPE_CONVERT, type(list(data.values())[0]))
 
-    def __repr__(self):
+    def __calc_repr__(self):
         return "|".join(f"{k}" for k in self.switch if k != Ellipsis)
 
     def match(self, input_: Any) -> _TCase:
         try:
             return self.switch[input_]
         except KeyError as e:
             if Ellipsis in self.switch:
```

### Comparing `nepattern-0.5.6/nepattern/context.py` & `nepattern-0.5.7/nepattern/context.py`

 * *Files identical despite different names*

### Comparing `nepattern-0.5.6/nepattern/context.pyi` & `nepattern-0.5.7/nepattern/context.pyi`

 * *Files identical despite different names*

### Comparing `nepattern-0.5.6/nepattern/core.py` & `nepattern-0.5.7/nepattern/core.py`

 * *Files identical despite different names*

### Comparing `nepattern-0.5.6/nepattern/main.py` & `nepattern-0.5.7/nepattern/main.py`

 * *Files identical despite different names*

### Comparing `nepattern-0.5.6/nepattern/util.py` & `nepattern-0.5.7/nepattern/util.py`

 * *Files identical despite different names*

### Comparing `nepattern-0.5.6/pyproject.toml` & `nepattern-0.5.7/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "nepattern"
-version = "0.5.6"
+version = "0.5.7"
 description = "a complex pattern, support typing"
 authors = [
     { name = "RF-Tar-Railt", email = "rf_tar_railt@qq.com" },
 ]
 dependencies = [
     "typing-extensions>=4.5.0",
     "tarina>=0.3.3",
```

### Comparing `nepattern-0.5.6/README.md` & `nepattern-0.5.7/README.md`

 * *Files identical despite different names*

### Comparing `nepattern-0.5.6/PKG-INFO` & `nepattern-0.5.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nepattern
-Version: 0.5.6
+Version: 0.5.7
 Summary: a complex pattern, support typing
 License: MIT
 Keywords: typing,pattern,converter,validator
 Author-email: RF-Tar-Railt <rf_tar_railt@qq.com>
 Requires-Python: >=3.8
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: MIT License
```

