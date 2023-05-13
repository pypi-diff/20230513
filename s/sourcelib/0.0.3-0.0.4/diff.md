# Comparing `tmp/sourcelib-0.0.3.tar.gz` & `tmp/sourcelib-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sourcelib-0.0.3.tar", last modified: Fri Jan 27 12:36:25 2023, max compression
+gzip compressed data, was "sourcelib-0.0.4.tar", last modified: Sat May 13 12:55:30 2023, max compression
```

## Comparing `sourcelib-0.0.3.tar` & `sourcelib-0.0.4.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-27 12:36:25.666499 sourcelib-0.0.3/
--rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-01-27 12:36:07.000000 sourcelib-0.0.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2807 2023-01-27 12:36:25.666499 sourcelib-0.0.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      836 2023-01-27 12:36:07.000000 sourcelib-0.0.3/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     1169 2023-01-27 12:36:07.000000 sourcelib-0.0.3/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-01-27 12:36:25.666499 sourcelib-0.0.3/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-27 12:36:25.662495 sourcelib-0.0.3/sourcelib/
--rw-r--r--   0 runner    (1001) docker     (123)       33 2023-01-27 12:36:07.000000 sourcelib-0.0.3/sourcelib/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       21 2023-01-27 12:36:07.000000 sourcelib-0.0.3/sourcelib/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)     3200 2023-01-27 12:36:07.000000 sourcelib-0.0.3/sourcelib/associations.py
--rw-r--r--   0 runner    (1001) docker     (123)     3316 2023-01-27 12:36:07.000000 sourcelib-0.0.3/sourcelib/collect.py
--rw-r--r--   0 runner    (1001) docker     (123)     1056 2023-01-27 12:36:07.000000 sourcelib-0.0.3/sourcelib/copy.py
--rw-r--r--   0 runner    (1001) docker     (123)      540 2023-01-27 12:36:07.000000 sourcelib-0.0.3/sourcelib/extension.py
--rw-r--r--   0 runner    (1001) docker     (123)     1451 2023-01-27 12:36:07.000000 sourcelib-0.0.3/sourcelib/file.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-27 12:36:25.666499 sourcelib-0.0.3/sourcelib.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2807 2023-01-27 12:36:25.000000 sourcelib-0.0.3/sourcelib.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      346 2023-01-27 12:36:25.000000 sourcelib-0.0.3/sourcelib.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-01-27 12:36:25.000000 sourcelib-0.0.3/sourcelib.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-01-27 12:36:25.000000 sourcelib-0.0.3/sourcelib.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-01-27 12:36:25.000000 sourcelib-0.0.3/sourcelib.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:30.950467 sourcelib-0.0.4/
+-rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-05-13 12:55:06.000000 sourcelib-0.0.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2807 2023-05-13 12:55:30.950467 sourcelib-0.0.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      836 2023-05-13 12:55:06.000000 sourcelib-0.0.4/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1169 2023-05-13 12:55:06.000000 sourcelib-0.0.4/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:55:30.950467 sourcelib-0.0.4/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:30.946467 sourcelib-0.0.4/sourcelib/
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 12:55:06.000000 sourcelib-0.0.4/sourcelib/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       21 2023-05-13 12:55:06.000000 sourcelib-0.0.4/sourcelib/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3292 2023-05-13 12:55:06.000000 sourcelib-0.0.4/sourcelib/associations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4316 2023-05-13 12:55:06.000000 sourcelib-0.0.4/sourcelib/collect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1056 2023-05-13 12:55:06.000000 sourcelib-0.0.4/sourcelib/copy.py
+-rw-r--r--   0 runner    (1001) docker     (123)      540 2023-05-13 12:55:06.000000 sourcelib-0.0.4/sourcelib/extension.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1451 2023-05-13 12:55:06.000000 sourcelib-0.0.4/sourcelib/file.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:30.950467 sourcelib-0.0.4/sourcelib.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2807 2023-05-13 12:55:30.000000 sourcelib-0.0.4/sourcelib.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 12:55:30.000000 sourcelib-0.0.4/sourcelib.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:55:30.000000 sourcelib-0.0.4/sourcelib.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-13 12:55:30.000000 sourcelib-0.0.4/sourcelib.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 12:55:30.000000 sourcelib-0.0.4/sourcelib.egg-info/top_level.txt
```

### Comparing `sourcelib-0.0.3/LICENSE` & `sourcelib-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `sourcelib-0.0.3/PKG-INFO` & `sourcelib-0.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sourcelib
-Version: 0.0.3
+Version: 0.0.4
 Author-email: Mart van Rijthoven <mart.vanrijthoven@gmail.com>
 License: MIT License
         
         Copyright (c) 2022 martvanrijthoven
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
         of this software and associated documentation files (the "Software"), to deal
```

### Comparing `sourcelib-0.0.3/README.md` & `sourcelib-0.0.4/README.md`

 * *Files identical despite different names*

### Comparing `sourcelib-0.0.3/pyproject.toml` & `sourcelib-0.0.4/pyproject.toml`

 * *Files identical despite different names*

### Comparing `sourcelib-0.0.3/sourcelib/associations.py` & `sourcelib-0.0.4/sourcelib/associations.py`

 * *Files 2% similar despite different names*

```diff
@@ -44,14 +44,17 @@
 class Associations(UserDict):
     def __init__(self):
         super().__init__({})
 
     def add_file_key(self, file_key: str, mode):
         self.setdefault(file_key, AssociatedFiles(file_key, mode))
 
+    def add_file_with_key(self, file_key, file):
+        self[file_key].add_file(file)
+
     def add_file(
         self, file: Path, associater: Callable, exact_match: bool, required: bool
     ):
         file_key = self._associate(file, associater, exact_match)
         if file_key is None and not required:
             return
         self[file_key].add_file(file)
@@ -72,15 +75,15 @@
 def associate_files(
     files1: List[File],
     files2: List[File],
     associations: Optional[Associations] = None,
     associator: Callable = stem_file_associater,
     exact_match=False,
 ) -> Associations:
-
+    
     if associations is None:
         associations = Associations()
 
     for file1 in files1:
         file_key = associator(file1)
         associations.add_file_key(file_key=file_key, mode=file1.mode)
         associations.add_file(
```

### Comparing `sourcelib-0.0.3/sourcelib/collect.py` & `sourcelib-0.0.4/sourcelib/collect.py`

 * *Files 23% similar despite different names*

```diff
@@ -2,24 +2,39 @@
 from enum import Enum
 from pathlib import Path
 from typing import List, Mapping, Tuple, Union
 import re
 import yaml
 
 from sourcelib.file import File, FileMode
+from sourcelib.associations import Associations
 
 
 class NoSourceFilesInFolderError(Exception):
     ...
 
 
 class NonExistentModeInYamlSource(Exception):
     ...
 
 
+def _get_data(source, mode):
+    if isinstance(source, Mapping):
+        data = deepcopy(source)
+    if isinstance(source, (str, Path)):
+        with open(source, encoding="utf-8") as file:
+            data = yaml.safe_load(file)
+
+    if mode.name not in data:
+        raise NonExistentModeInYamlSource(
+            f"mode '{mode.name}' not in data {data.keys()} in: {source}"
+        )
+    return data
+
+
 def get_files_from_paths(
     file_cls: Union[str, type],
     mode: Enum,
     paths: List[str],
     filters: List[str],
     excludes: List[str],
     regex=None,
@@ -52,15 +67,14 @@
     mode: Enum = FileMode.default,
     filters: List[str] = (),
     excludes: List[str] = (),
     regex=None,
     recursive=False,
     **kwargs,
 ):
-
     all_sources = []
     folder = Path(folder)
     for extension in file_cls.EXTENSIONS:
         paths = (
             folder.rglob("*" + extension) if recursive else folder.glob("*" + extension)
         )
         sources = get_files_from_paths(
@@ -81,35 +95,49 @@
     file_cls: File,
     mode: Enum = FileMode.default,
     filters=(),
     excludes=(),
     regex=None,
     **kwargs,
 ):
-
-    data = {}
-    if isinstance(yaml_source, Mapping):
-        data = deepcopy(yaml_source)
-    elif isinstance(yaml_source, (str, Path)):
-        with open(yaml_source, encoding="utf-8") as file:
-            data = yaml.safe_load(file)
+    data = _get_data(yaml_source, mode)
+    file_identifier = file_cls.IDENTIFIER
 
     paths = []
-    if mode.name not in data:
-        raise NonExistentModeInYamlSource(
-            f"mode '{mode.name}' not in data {data.keys()} in: {yaml_source}"
-        )
-
-    file_identifier = file_cls.IDENTIFIER
     for item in data[mode.name]:
         if file_identifier in item:
             paths.append(item[file_identifier].pop("path"))
             kwargs.update(item[file_identifier])
 
-    return get_files_from_paths(file_cls, mode, paths, filters, excludes, regex, **kwargs)
+    return get_files_from_paths(
+        file_cls, mode, paths, filters, excludes, regex, **kwargs
+    )
+
+
+def get_associations_from_yaml(
+    yaml_source: Union[str, dict],
+    file_classes: List[File],
+    mode: Enum = FileMode.default,
+):
+    data = _get_data(yaml_source, mode)
+
+    associations = Associations()
+    for file_key, item in enumerate(data[mode.name]):
+        file_key = str(file_key)
+        associations.add_file_key(file_key=file_key, mode=mode)
+        for _, file_data in file_classes.items():
+            file_cls = file_data["class"]
+            kwargs = file_data["kwargs"] if "kwargs" in file_data else {}
+            file_identifier = file_cls.IDENTIFIER
+            if file_identifier in item:
+                path = item[file_identifier].pop("path")
+                kwargs.update(item[file_identifier])
+                file = file_cls(mode=mode, path=path, **kwargs)
+                associations.add_file_with_key(file_key=file_key, file=file)
+    return associations
 
 
 def copy_from_yml(
     yaml_source: Union[Path, dict],
     file_cls: File,
     copy_path: Path,
     modes: Tuple[Enum] = (FileMode.default,),
```

### Comparing `sourcelib-0.0.3/sourcelib/copy.py` & `sourcelib-0.0.4/sourcelib/copy.py`

 * *Files identical despite different names*

### Comparing `sourcelib-0.0.3/sourcelib/extension.py` & `sourcelib-0.0.4/sourcelib/extension.py`

 * *Files identical despite different names*

### Comparing `sourcelib-0.0.3/sourcelib/file.py` & `sourcelib-0.0.4/sourcelib/file.py`

 * *Files identical despite different names*

### Comparing `sourcelib-0.0.3/sourcelib.egg-info/PKG-INFO` & `sourcelib-0.0.4/sourcelib.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sourcelib
-Version: 0.0.3
+Version: 0.0.4
 Author-email: Mart van Rijthoven <mart.vanrijthoven@gmail.com>
 License: MIT License
         
         Copyright (c) 2022 martvanrijthoven
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
         of this software and associated documentation files (the "Software"), to deal
```

