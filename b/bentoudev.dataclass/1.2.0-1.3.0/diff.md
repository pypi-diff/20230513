# Comparing `tmp/bentoudev.dataclass-1.2.0.tar.gz` & `tmp/bentoudev.dataclass-1.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bentoudev.dataclass-1.2.0.tar", last modified: Sun Nov 13 16:52:47 2022, max compression
+gzip compressed data, was "bentoudev.dataclass-1.3.0.tar", last modified: Sat May 13 21:41:45 2023, max compression
```

## Comparing `bentoudev.dataclass-1.2.0.tar` & `bentoudev.dataclass-1.3.0.tar`

### file list

```diff
@@ -1,18 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 16:52:47.352142 bentoudev.dataclass-1.2.0/
--rw-r--r--   0 runner    (1001) docker     (121)     4833 2022-11-13 16:52:47.352142 bentoudev.dataclass-1.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     4396 2022-11-13 16:52:30.000000 bentoudev.dataclass-1.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 16:52:47.352142 bentoudev.dataclass-1.2.0/bentoudev/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 16:52:47.352142 bentoudev.dataclass-1.2.0/bentoudev/dataclass/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-11-13 16:52:30.000000 bentoudev.dataclass-1.2.0/bentoudev/dataclass/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)       46 2022-11-13 16:52:30.000000 bentoudev.dataclass-1.2.0/bentoudev/dataclass/_version.py
--rw-r--r--   0 runner    (1001) docker     (121)    11741 2022-11-13 16:52:30.000000 bentoudev.dataclass-1.2.0/bentoudev/dataclass/base.py
--rw-r--r--   0 runner    (1001) docker     (121)    18135 2022-11-13 16:52:30.000000 bentoudev.dataclass-1.2.0/bentoudev/dataclass/yaml_loader.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-13 16:52:47.352142 bentoudev.dataclass-1.2.0/bentoudev.dataclass.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     4833 2022-11-13 16:52:47.000000 bentoudev.dataclass-1.2.0/bentoudev.dataclass.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      374 2022-11-13 16:52:47.000000 bentoudev.dataclass-1.2.0/bentoudev.dataclass.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-11-13 16:52:47.000000 bentoudev.dataclass-1.2.0/bentoudev.dataclass.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)      151 2022-11-13 16:52:47.000000 bentoudev.dataclass-1.2.0/bentoudev.dataclass.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       10 2022-11-13 16:52:47.000000 bentoudev.dataclass-1.2.0/bentoudev.dataclass.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1248 2022-11-13 16:52:30.000000 bentoudev.dataclass-1.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-11-13 16:52:47.352142 bentoudev.dataclass-1.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)       37 2022-11-13 16:52:30.000000 bentoudev.dataclass-1.2.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:41:45.395786 bentoudev.dataclass-1.3.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     4833 2023-05-13 21:41:45.395786 bentoudev.dataclass-1.3.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4396 2023-05-13 21:41:31.000000 bentoudev.dataclass-1.3.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:41:45.395786 bentoudev.dataclass-1.3.0/bentoudev/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:41:45.395786 bentoudev.dataclass-1.3.0/bentoudev/dataclass/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 21:41:31.000000 bentoudev.dataclass-1.3.0/bentoudev/dataclass/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       46 2023-05-13 21:41:31.000000 bentoudev.dataclass-1.3.0/bentoudev/dataclass/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12136 2023-05-13 21:41:31.000000 bentoudev.dataclass-1.3.0/bentoudev/dataclass/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17742 2023-05-13 21:41:31.000000 bentoudev.dataclass-1.3.0/bentoudev/dataclass/yaml_loader.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:41:45.395786 bentoudev.dataclass-1.3.0/bentoudev.dataclass.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4833 2023-05-13 21:41:45.000000 bentoudev.dataclass-1.3.0/bentoudev.dataclass.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 21:41:45.000000 bentoudev.dataclass-1.3.0/bentoudev.dataclass.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 21:41:45.000000 bentoudev.dataclass-1.3.0/bentoudev.dataclass.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      151 2023-05-13 21:41:45.000000 bentoudev.dataclass-1.3.0/bentoudev.dataclass.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 21:41:45.000000 bentoudev.dataclass-1.3.0/bentoudev.dataclass.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1248 2023-05-13 21:41:31.000000 bentoudev.dataclass-1.3.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 21:41:45.395786 bentoudev.dataclass-1.3.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       37 2023-05-13 21:41:31.000000 bentoudev.dataclass-1.3.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:41:45.395786 bentoudev.dataclass-1.3.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)    11982 2023-05-13 21:41:31.000000 bentoudev.dataclass-1.3.0/tests/test_load_dataclass.py
```

### Comparing `bentoudev.dataclass-1.2.0/PKG-INFO` & `bentoudev.dataclass-1.3.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bentoudev.dataclass
-Version: 1.2.0
+Version: 1.3.0
 Summary: Yaml to dataclass loader
 Author: BentouDev
 Project-URL: Homepage, https://github.com/BentouDev/zetsubou.dataclass
 Keywords: yaml,dataclass
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
```

### Comparing `bentoudev.dataclass-1.2.0/README.md` & `bentoudev.dataclass-1.3.0/README.md`

 * *Files identical despite different names*

### Comparing `bentoudev.dataclass-1.2.0/bentoudev/dataclass/base.py` & `bentoudev.dataclass-1.3.0/bentoudev/dataclass/base.py`

 * *Files 3% similar despite different names*

```diff
@@ -129,15 +129,15 @@
         first_line = ''
         if len(label) != 0:
             first_line = f'{label}: {message}'
         else:
             first_line = f'{message}'
 
         return (
-            f'{first_line}'
+            f'{first_line}\n'
             f'in "{self.file_name}", line {self.line_number}, column {self.column_number}:'
         )
 
 
 @dataclasses.dataclass
 class DataclassErrorMessage:
     source: Source
@@ -149,15 +149,15 @@
 class DataclassLoadError(Exception):
     LABEL:ClassVar[str] = 'error'
     error_msg: DataclassErrorMessage
     msg:str = ''
     source:Source = None
     format:EErrorFormat = EErrorFormat.Pretty
 
-    errors: List[Union[Exception,DataclassErrorMessage]] = dataclasses.field(default_factory=list)
+    errors: List[Union[Exception,DataclassErrorMessage]] = []
 
     def is_compound(self):
         return len(self.errors) > 0
 
     def has_data_errors(self):
         return any(isinstance(e, DataclassErrorMessage) for e in self.errors)
 
@@ -206,24 +206,34 @@
         result.format = format
         return result
 
     def __init__(self):
         pass
 
     def __str__(self):
+        def print_err(err):
+            if isinstance(err, DataclassErrorMessage):
+                if hasattr(err, 'errors'):
+                    mid_buff = []
+                    for sub_err in err.errors:
+                        mid_buff.append(print_err(sub_err))
+                    return '\n'.join(mid_buff)
+                elif err.source is not None:
+                    return err.source.format(err.label, err.message, self.format)
+                else:
+                    return f"{err.label}: {err.message}"
+            else:
+                return str(err)
+
         if self.is_compound():
             buffer = [ f"{self.LABEL} : {self.msg}" ] if self.msg != '' and self.msg != None else []
+            buffer.append('')
             for err in self.errors:
-                if isinstance(err, DataclassErrorMessage):
-                    buffer.append(err.source.format(err.label, err.message, self.format))
-                else:
-                    buffer.append(str(err))
-
+                buffer.append(print_err(err))
             return '\n'.join(buffer)
-
         else:
             return self.source.format(self.LABEL, self.msg, self.format)
 
 
 class UnhandledType(Exception):
     pass
```

### Comparing `bentoudev.dataclass-1.2.0/bentoudev/dataclass/yaml_loader.py` & `bentoudev.dataclass-1.3.0/bentoudev/dataclass/yaml_loader.py`

 * *Files 2% similar despite different names*

```diff
@@ -181,14 +181,24 @@
 
 def is_obj_tracked(obj):
     if is_obj_dict(type(obj)):
         return '__yaml_location__' in obj and '__yaml_field_location__' in obj
     return (hasattr(obj, '__yaml_location__') and hasattr(obj, '__yaml_field_location__'))
 
 
+def clear_tracked_obj(obj):
+    if is_obj_tracked(obj):
+        if is_obj_dict(type(obj)):
+            obj.pop('__yaml_field_location__', None)
+            obj.pop('__yaml_location__', None)
+        else:
+            delattr(obj, '__yaml_field_location__')
+            delattr(obj, '__yaml_location__')
+    return obj
+
 
 class YamlSourceTracker(SourceTracker):
 
     @staticmethod
     def yaml_to_src(yaml_loc: YamlSourceLocation, context: DataclassVisitorContext) -> Source:
         start_line: int = yaml_loc.line
         buff = context.get_yaml_line(start_line - 1)
@@ -226,14 +236,17 @@
         return False
 
     def __ne__(self, other):
         return not(self == other)
 
 
 def YamlToScalar(clazz: type, yaml_obj: Any, context: DataclassVisitorContext):
+    if clazz == Any:
+        return clear_tracked_obj(yaml_obj)
+
     if inspect.isclass(clazz) and issubclass(clazz, enum.Enum):
         value_t = type(yaml_obj)
         if value_t is not str:
             loc_src = context.get_location_source()
             raise DataclassLoadError.from_source(f"Got '{value_t.__name__}' when expecting enum '{clazz.__name__}'", loc_src, context.error_format)
 
         allowed_values = list(map(lambda i: i[0], clazz.__members__.items()))
@@ -282,53 +295,35 @@
                 preffered_type = type(yaml_obj)
                 union_types = typing_inspect.get_args(clazz)
 
                 if len(union_types) == 2 and type(None) in union_types:
                     subtype = clazz.__args__[0]
                     return YamlToObject(subtype, yaml_obj, context)
 
-                # Check the type of the value, it may fit just fine
-                # if preffered_type in union_types:
-                #     try:
-                #         result = YamlToObject(preffered_type, yaml_obj, context)
-                #     except UnhandledType as err:
-                #         pass
-                #     else:
-                #         return result
-
-                # else:
                 failed_attempts = []
                 for possible_dict_t in union_types:
                     try:
                         result = YamlToObject(possible_dict_t, yaml_obj, context)
                     except DataclassLoadError as err:
                         failed_attempts.append(err)
                     except Exception as err:
                         failed_attempts.append(err)
                     else:
                         return result
 
-                allowed_types = ', '.join([t.__name__ for t in union_types] )
+                allowed_types = ', '.join([str(t) for t in union_types] )
                 loc_src = context.get_location_source()
 
                 raise DataclassLoadError.from_exception_list(
                     msg=f"Got '{type(yaml_obj)}' when expecting 'Union [{allowed_types}]'. Failed to substitute all Union types.",
                     src=loc_src,
                     excs=failed_attempts,
                     format=context.error_format
                 )
 
-                # allowed_types = ', '.join([t.__name__ for t in union_types] )
-                # loc_src = context.get_location_source()
-                # raise DataclassLoadError.from_source(f"Got '{type(yaml_obj)}' when expecting 'Union [{allowed_types}]'", loc_src, format=context.error_format)
-
-            # elif typing_inspect.is_optional_type(clazz):
-            #     subtype = clazz.__args__[0]
-            #     return YamlToObject(subtype, yaml_obj, context)
-
             elif is_obj_dict(clazz):
                 key_type, value_type = typing_inspect.get_args(clazz)
 
                 if not is_obj_dict(type(yaml_obj)):
                     loc_src = context.get_location_source()
                     raise DataclassLoadError.from_source(f"Got '{type(yaml_obj)}', when expecting 'Dict [{key_type.__name__},{value_type.__name__}]'", loc_src, context.error_format)
 
@@ -399,24 +394,40 @@
                 loc_src = context.get_location_source(entry)
                 errors.append(DataclassErrorMessage(
                     loc_src, DataclassLoadError.LABEL, f"Unknown field '{entry}' for class '{clazz.__name__}'", context.error_format
                 ))
 
         if has_missing_fields:
             errors.append(DataclassErrorMessage(
-                root_src, DataclassLoadError.LABEL, f"Missing required field(s) of class '{clazz.__name__}': { ','.join(missing_fields) }", context.error_format
+                root_src, DataclassLoadError.LABEL, f"Missing required field(s) of class '{clazz.__name__}': { ', '.join(missing_fields) }", context.error_format
             ))
 
         raise DataclassLoadError.from_error_list(root_src, errors, context.error_format)
 
 
 def DictToDataclass(clazz: type, yaml_obj: Any, context: DataclassVisitorContext):
     if not dataclasses.is_dataclass(clazz):
         raise ValueError(f'Class \'{clazz}\' passed to YAMLToDataclass must be a dataclass!')
 
+    def handle_source_tracked(result):
+        if is_source_tracked(clazz) and hasattr(result, 'set_source_tracker'):
+            stack_len = len(context.clazz_stack)
+            if stack_len > 0:
+                st = context.clazz_stack[stack_len - 1]
+                result.set_source_tracker(YamlSourceTracker.from_inline(st, context))
+            else:
+                raise ValueError(f"Unable to set source tracker for {clazz}")
+
+    if is_inline_loaded(clazz):
+        loader = get_inline_load_type(clazz)
+        loaded_val = YamlToObject(loader.inline_type, yaml_obj, context)
+        result = loader.loader(loaded_val)
+        handle_source_tracked(result)
+        return result
+
     if is_obj_dict(type(yaml_obj)):
 
         if context.always_track_source:
             clazz = track_source(clazz)
 
         st = None
         if is_source_tracked(clazz):
@@ -439,29 +450,16 @@
         if st is not None:
             result.set_source_tracker(st)
             context.clazz_stack.remove(st)
 
         return result
 
     else:
-        if is_inline_loaded(clazz):
-            loader = get_inline_load_type(clazz)
-            loaded_val = YamlToScalar(loader.inline_type, yaml_obj, context)
-            result = loader.loader(loaded_val)
-        else:
-            result = yaml_obj
-
-        if is_source_tracked(clazz) and hasattr(result, 'set_source_tracker'):
-            stack_len = len(context.clazz_stack)
-            if stack_len > 0:
-                st = context.clazz_stack[stack_len - 1]
-                result.set_source_tracker(YamlSourceTracker.from_inline(st, context))
-            else:
-                raise ValueError(f"Unable to set source tracker for {clazz}")
-
+        result = yaml_obj
+        handle_source_tracked(result)
         return result
 
 
 def load_yaml_dataclass(clazz:type, label:str, yaml_content:str, *, type_cache:dict=default_type_loaders(), ext_types:list=[],
         error_format:EErrorFormat=EErrorFormat.Pretty, always_track_source:bool=False, error_code_snippet_lines:int=4):
     try:
         context = DataclassVisitorContext()
```

### Comparing `bentoudev.dataclass-1.2.0/bentoudev.dataclass.egg-info/PKG-INFO` & `bentoudev.dataclass-1.3.0/bentoudev.dataclass.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bentoudev.dataclass
-Version: 1.2.0
+Version: 1.3.0
 Summary: Yaml to dataclass loader
 Author: BentouDev
 Project-URL: Homepage, https://github.com/BentouDev/zetsubou.dataclass
 Keywords: yaml,dataclass
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
```

### Comparing `bentoudev.dataclass-1.2.0/pyproject.toml` & `bentoudev.dataclass-1.3.0/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 build-backend = "setuptools.build_meta"
 
 [tool.setuptools]
 packages = [ 'bentoudev.dataclass' ]
 
 [project]
 name = "bentoudev.dataclass"
-version = "1.2.0"
+version = "1.3.0"
 description = "Yaml to dataclass loader"
 readme = "README.md"
 authors = [{ name = "BentouDev" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
@@ -31,15 +31,15 @@
 [project.optional-dependencies]
 dev = ["pyinstaller>=5.0", "bumpver", "pip-tools", "pytest", "build", "twine"]
 
 [project.urls]
 Homepage = "https://github.com/BentouDev/zetsubou.dataclass"
 
 [tool.bumpver]
-current_version = "1.2.0"
+current_version = "1.3.0"
 version_pattern = "MAJOR.MINOR.PATCH"
 commit_message = "[bot] Bump version {old_version} -> {new_version}"
 commit = false
 tag = false
 push = false
 
 [tool.bumpver.file_patterns]
```

