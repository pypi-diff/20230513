# Comparing `tmp/crelm-0.0.33a0.tar.gz` & `tmp/crelm-0.0.33a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "crelm-0.0.33a0.tar", max compression
+gzip compressed data, was "crelm-0.0.33a1.tar", max compression
```

## Comparing `crelm-0.0.33a0.tar` & `crelm-0.0.33a1.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1108 2023-05-03 17:25:38.782803 crelm-0.0.33a0/LICENSE
--rw-r--r--   0        0        0      600 2023-05-03 17:25:38.782803 crelm-0.0.33a0/README.md
--rw-r--r--   0        0        0      187 2023-05-03 17:25:38.782803 crelm-0.0.33a0/crelm/__init__.py
--rw-r--r--   0        0        0     3071 2023-05-03 17:25:38.782803 crelm-0.0.33a0/crelm/factory.py
--rw-r--r--   0        0        0      391 2023-05-03 17:25:38.782803 crelm-0.0.33a0/crelm/libcrelm.py
--rw-r--r--   0        0        0   107326 2023-05-03 17:25:38.784803 crelm-0.0.33a0/crelm/makeheaders.c
--rw-r--r--   0        0        0     1987 2023-05-03 17:25:38.784803 crelm-0.0.33a0/crelm/makeheaders_crelm.c
--rw-r--r--   0        0        0    13764 2023-05-08 00:36:28.945262 crelm-0.0.33a0/crelm/tube.py
--rw-r--r--   0        0        0      778 2023-05-08 00:51:03.997888 crelm-0.0.33a0/pyproject.toml
--rw-r--r--   0        0        0     1469 1970-01-01 00:00:00.000000 crelm-0.0.33a0/PKG-INFO
+-rw-r--r--   0        0        0     1108 2023-05-03 17:25:38.782803 crelm-0.0.33a1/LICENSE
+-rw-r--r--   0        0        0      600 2023-05-03 17:25:38.782803 crelm-0.0.33a1/README.md
+-rw-r--r--   0        0        0      187 2023-05-03 17:25:38.782803 crelm-0.0.33a1/crelm/__init__.py
+-rw-r--r--   0        0        0     3071 2023-05-03 17:25:38.782803 crelm-0.0.33a1/crelm/factory.py
+-rw-r--r--   0        0        0      388 2023-05-13 18:12:40.800567 crelm-0.0.33a1/crelm/libcrelm.py
+-rw-r--r--   0        0        0   107326 2023-05-03 17:25:38.784803 crelm-0.0.33a1/crelm/makeheaders.c
+-rw-r--r--   0        0        0     1987 2023-05-03 17:25:38.784803 crelm-0.0.33a1/crelm/makeheaders_crelm.c
+-rw-r--r--   0        0        0    14462 2023-05-13 14:41:12.722203 crelm-0.0.33a1/crelm/tube.py
+-rw-r--r--   0        0        0      778 2023-05-13 18:05:17.136000 crelm-0.0.33a1/pyproject.toml
+-rw-r--r--   0        0        0     1469 1970-01-01 00:00:00.000000 crelm-0.0.33a1/PKG-INFO
```

### Comparing `crelm-0.0.33a0/LICENSE` & `crelm-0.0.33a1/LICENSE`

 * *Files identical despite different names*

### Comparing `crelm-0.0.33a0/README.md` & `crelm-0.0.33a1/README.md`

 * *Files identical despite different names*

### Comparing `crelm-0.0.33a0/crelm/factory.py` & `crelm-0.0.33a1/crelm/factory.py`

 * *Files identical despite different names*

### Comparing `crelm-0.0.33a0/crelm/makeheaders.c` & `crelm-0.0.33a1/crelm/makeheaders.c`

 * *Files identical despite different names*

### Comparing `crelm-0.0.33a0/crelm/makeheaders_crelm.c` & `crelm-0.0.33a1/crelm/makeheaders_crelm.c`

 * *Files identical despite different names*

### Comparing `crelm-0.0.33a0/crelm/tube.py` & `crelm-0.0.33a1/crelm/tube.py`

 * *Files 1% similar despite different names*

```diff
@@ -178,15 +178,15 @@
                             self._header_text + '\n')
 
         self._header_filenames += [
             self._make_gen_filename(self._generated_header_filename)]
 
         self._cdef = self._preprocess_headers()
 
-        extern_python = '\n'.join([f'extern "Python" {x}' for x in self._externs])
+        extern_python = '\n'.join(self._externs)
         self._cdef += '\n' + extern_python
 
         if self._verbose:
             print(f'cdef: {self._cdef}')
 
         return True
 
@@ -227,14 +227,15 @@
         args = self._build_compiler_args()
 
         if self._verbose:
             print(f'module: {self._module_name}')
             print(f'cdef: {self._cdef}')
             print(f'headers: {headers}')
             print(f'sources: {source_filenames}')
+            print(f'externs: {self._externs}')
             print(f'args: {args}')
             print(f'verbose: {self._verbose}')
             print(f'gen folder: {self._gen_foldername}')
 
         ffibuilder = FFI()
 
         try:
@@ -345,15 +346,15 @@
 
     def add_macro_if(self, predicate: bool, macro: str) -> TSelf:
         if predicate:
             self._macros.append(macro)
         return self
 
     def add_extern(self, extern: str) -> TSelf:
-        self._externs.append(extern)
+        self._externs.append(f'extern "Python" {extern}')
         return self
 
     def add_externs(self, externs: List[str]) -> TSelf:
         for extern in externs:
             self.add_extern(extern)
 
         return self
@@ -380,24 +381,41 @@
                 return self._tube._ffi.new(f"char[]", v.encode('utf-8'))
 
             if isinstance(v, int):
                 return self._tube._ffi.new(f"char[{v}]")
 
             return None
 
-        def string(self, var) -> str:
-            return self._tube._ffi.string(var).decode('utf-8')
-        
         def str(self, cstr) -> str:
-            return self.string(cstr)
+            return self._tube._ffi.string(cstr).decode('utf-8')
 
         @property
         def null_pointer(self):
             return self._tube._ffi.NULL
 
+        @property
+        def typedef_names(self):
+            return self._tube._ffi.list_types()[0]
+
+        @property
+        def struct_names(self):
+            return self._tube._ffi.list_types()[1]
+
+        @property
+        def union_names(self):
+            return self._tube._ffi.list_types()[2]
+
+        def typedef_decl(self, type_name: str, instance_name: str = ''):
+            return self._tube._ffi.getctype(type_name, instance_name)
+
+        def function_decl(self, type_name: str, instance_name: str = ''):
+            return self.typedef_decl(type_name).replace('(*)', f' {instance_name}')
+
+        def struct_decl(self, type_name: str, instance_name: str = ''):
+            return self.typedef_decl(type_name)
 
     def squeeze(self, build: bool = True) -> TSelf:
         if build:
             try:
                 if not self._build():
                     print(f'{self._name}: build failed')
                     return None
```

### Comparing `crelm-0.0.33a0/pyproject.toml` & `crelm-0.0.33a1/pyproject.toml`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "crelm"
-version = "0.0.33a0"
+version = "0.0.33a1"
 description = "Utility that automates turning simple C classes into Python objects"
 authors = [
   "WideOpenTech <foss@wideopentech.co.uk>",
 ]
 readme = "README.md"
 classifiers = [
     "Programming Language :: Python :: 3",
```

### Comparing `crelm-0.0.33a0/PKG-INFO` & `crelm-0.0.33a1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: crelm
-Version: 0.0.33a0
+Version: 0.0.33a1
 Summary: Utility that automates turning simple C classes into Python objects
 Home-page: https://github.com/wideopensource/crelm
 Author: WideOpenTech
 Author-email: foss@wideopentech.co.uk
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

