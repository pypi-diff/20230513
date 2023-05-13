# Comparing `tmp/LordPath-2023.5.4.tar.gz` & `tmp/LordPath-2023.5.6.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "LordPath-2023.5.4.tar", last modified: Thu May  4 14:22:19 2023, max compression
+gzip compressed data, was "LordPath-2023.5.6.4.tar", last modified: Sat May  6 13:47:15 2023, max compression
```

## Comparing `LordPath-2023.5.4.tar` & `LordPath-2023.5.6.4.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-05-04 14:22:19.190334 LordPath-2023.5.4/
-drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-05-04 14:22:19.186067 LordPath-2023.5.4/LordPath/
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     3203 2023-03-17 16:10:53.000000 LordPath-2023.5.4/LordPath/__init__.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      617 2022-12-09 23:13:08.000000 LordPath-2023.5.4/LordPath/dataset.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      583 2023-03-21 08:46:08.000000 LordPath-2023.5.4/LordPath/descriptors.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     6385 2023-03-17 16:32:55.000000 LordPath-2023.5.4/LordPath/filefolderclass.py
-drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-05-04 14:22:19.189660 LordPath-2023.5.4/LordPath/opener/
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1051 2023-05-04 14:21:50.000000 LordPath-2023.5.4/LordPath/opener/__init__.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      328 2023-03-17 16:42:56.000000 LordPath-2023.5.4/LordPath/opener/base.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      868 2023-03-17 16:42:56.000000 LordPath-2023.5.4/LordPath/opener/json.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      864 2023-03-17 16:42:56.000000 LordPath-2023.5.4/LordPath/opener/pickle.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      490 2023-03-17 16:42:56.000000 LordPath-2023.5.4/LordPath/opener/toml.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1019 2023-03-16 23:58:05.000000 LordPath-2023.5.4/LordPath/opener/yaml.py
-drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-05-04 14:22:19.187396 LordPath-2023.5.4/LordPath.egg-info/
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      463 2023-05-04 14:22:19.000000 LordPath-2023.5.4/LordPath.egg-info/PKG-INFO
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      427 2023-05-04 14:22:19.000000 LordPath-2023.5.4/LordPath.egg-info/SOURCES.txt
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)        1 2023-05-04 14:22:19.000000 LordPath-2023.5.4/LordPath.egg-info/dependency_links.txt
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)       23 2023-05-04 14:22:19.000000 LordPath-2023.5.4/LordPath.egg-info/requires.txt
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)        9 2023-05-04 14:22:19.000000 LordPath-2023.5.4/LordPath.egg-info/top_level.txt
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      463 2023-05-04 14:22:19.190153 LordPath-2023.5.4/PKG-INFO
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)       58 2023-03-19 09:41:22.000000 LordPath-2023.5.4/README.rst
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      516 2023-05-04 14:22:14.000000 LordPath-2023.5.4/pyproject.toml
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)       38 2023-05-04 14:22:19.190380 LordPath-2023.5.4/setup.cfg
+drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-05-06 13:47:15.489013 LordPath-2023.5.6.4/
+drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-05-06 13:47:15.484317 LordPath-2023.5.6.4/LordPath/
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     3483 2023-05-06 13:46:10.000000 LordPath-2023.5.6.4/LordPath/__init__.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      617 2022-12-09 23:13:08.000000 LordPath-2023.5.6.4/LordPath/dataset.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      583 2023-03-21 08:46:08.000000 LordPath-2023.5.6.4/LordPath/descriptors.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     6385 2023-03-17 16:32:55.000000 LordPath-2023.5.6.4/LordPath/filefolderclass.py
+drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-05-06 13:47:15.488299 LordPath-2023.5.6.4/LordPath/opener/
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1051 2023-05-04 14:21:50.000000 LordPath-2023.5.6.4/LordPath/opener/__init__.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      328 2023-03-17 16:42:56.000000 LordPath-2023.5.6.4/LordPath/opener/base.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      868 2023-03-17 16:42:56.000000 LordPath-2023.5.6.4/LordPath/opener/json.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      864 2023-03-17 16:42:56.000000 LordPath-2023.5.6.4/LordPath/opener/pickle.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      490 2023-03-17 16:42:56.000000 LordPath-2023.5.6.4/LordPath/opener/toml.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1019 2023-03-16 23:58:05.000000 LordPath-2023.5.6.4/LordPath/opener/yaml.py
+drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-05-06 13:47:15.485556 LordPath-2023.5.6.4/LordPath.egg-info/
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      465 2023-05-06 13:47:15.000000 LordPath-2023.5.6.4/LordPath.egg-info/PKG-INFO
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      427 2023-05-06 13:47:15.000000 LordPath-2023.5.6.4/LordPath.egg-info/SOURCES.txt
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)        1 2023-05-06 13:47:15.000000 LordPath-2023.5.6.4/LordPath.egg-info/dependency_links.txt
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)       23 2023-05-06 13:47:15.000000 LordPath-2023.5.6.4/LordPath.egg-info/requires.txt
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)        9 2023-05-06 13:47:15.000000 LordPath-2023.5.6.4/LordPath.egg-info/top_level.txt
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      465 2023-05-06 13:47:15.488837 LordPath-2023.5.6.4/PKG-INFO
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)       58 2023-03-19 09:41:22.000000 LordPath-2023.5.6.4/README.rst
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      518 2023-05-06 13:47:11.000000 LordPath-2023.5.6.4/pyproject.toml
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)       38 2023-05-06 13:47:15.489053 LordPath-2023.5.6.4/setup.cfg
```

### Comparing `LordPath-2023.5.4/LordPath/__init__.py` & `LordPath-2023.5.6.4/LordPath/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 import regex as re
 from typing import Union
 
 # File Path
 patternFileName = re.compile(r'[\/\\\?\<\>\|\:\'\"\*,]')  # / \ ? < > | : ' " * ,
 
 # configs
-encodes = ["utf-8-sig", "utf-8", "utf-16", "cp1252", "iso8859-1"]
+encodes = ["utf-8-sig", "utf-8", "utf-16", "cp1252", "iso8859-1", "cp437"]
 list_dir_filter = ['.DS_Store', '.git']
 
 
 def _path_convert(path: str | Path) -> Path:
     if isinstance(path, str):
         return Path(path)
     else:
@@ -103,19 +103,26 @@
             if _text:
                 return _text
 
     file = Path(file)
     if not file.exists():
         return default
 
+    with file.open("br") as f:
+        read_binary = f.read()
+
     for enc in encodes:
         try:
-            with file.open("r", encoding=enc) as f:
-                return f.read()
-        except:
+            d = read_binary.decode(enc)
+            if 'Û' in d:
+                char_position = d.index('Û')
+                if read_binary[char_position] == 219:  # 219 (=/xdb) welcher bei 1252 ein falsches zeichen ist
+                    continue
+            return d
+        except UnicodeDecodeError:
             pass
 
     return default
 
 
 def typical_readable_file_type(filename):
     path = Path(filename)
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `LordPath-2023.5.4/LordPath/dataset.py` & `LordPath-2023.5.6.4/LordPath/dataset.py`

 * *Files identical despite different names*

### Comparing `LordPath-2023.5.4/LordPath/descriptors.py` & `LordPath-2023.5.6.4/LordPath/descriptors.py`

 * *Files identical despite different names*

### Comparing `LordPath-2023.5.4/LordPath/filefolderclass.py` & `LordPath-2023.5.6.4/LordPath/filefolderclass.py`

 * *Files identical despite different names*

### Comparing `LordPath-2023.5.4/LordPath/opener/__init__.py` & `LordPath-2023.5.6.4/LordPath/opener/__init__.py`

 * *Files identical despite different names*

### Comparing `LordPath-2023.5.4/LordPath/opener/json.py` & `LordPath-2023.5.6.4/LordPath/opener/json.py`

 * *Files identical despite different names*

### Comparing `LordPath-2023.5.4/LordPath/opener/pickle.py` & `LordPath-2023.5.6.4/LordPath/opener/pickle.py`

 * *Files identical despite different names*

### Comparing `LordPath-2023.5.4/LordPath/opener/yaml.py` & `LordPath-2023.5.6.4/LordPath/opener/yaml.py`

 * *Files identical despite different names*

### Comparing `LordPath-2023.5.4/pyproject.toml` & `LordPath-2023.5.6.4/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "LordPath"
-version = "2023.5.4"
+version = "2023.5.6.4"
 description = "File Manager Helping Module base on Pathlib"
 readme = "README.rst"
 requires-python = ">=3.10"
 keywords = []
 classifiers = []
 dependencies = [ "regex", "pyyaml", "LordUtils",]
 [[project.authors]]
```

