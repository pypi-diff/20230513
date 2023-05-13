# Comparing `tmp/n0struct-0.2.94.tar.gz` & `tmp/n0struct-0.2.95.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\n0struct-0.2.94.tar", last modified: Sun Apr 23 14:01:16 2023, max compression
+gzip compressed data, was "dist\n0struct-0.2.95.tar", last modified: Sat May 13 11:14:33 2023, max compression
```

## Comparing `n0struct-0.2.94.tar` & `n0struct-0.2.95.tar`

### file list

```diff
@@ -1,42 +1,42 @@
-drwxrwxrwx   0        0        0        0 2023-04-23 14:01:16.077435 n0struct-0.2.94/
--rw-rw-rw-   0        0        0    11558 2022-09-04 19:16:09.000000 n0struct-0.2.94/LICENSE
--rw-rw-rw-   0        0        0     1060 2023-04-23 14:01:16.078465 n0struct-0.2.94/PKG-INFO
--rw-rw-rw-   0        0        0      590 2022-09-04 19:16:09.000000 n0struct-0.2.94/README.md
-drwxrwxrwx   0        0        0        0 2023-04-23 14:01:16.047055 n0struct-0.2.94/n0struct/
--rw-rw-rw-   0        0        0    13230 2023-04-02 07:25:19.000000 n0struct-0.2.94/n0struct/__init__.py
--rw-rw-rw-   0        0        0     3665 2023-04-02 13:22:27.000000 n0struct-0.2.94/n0struct/n0struct_arrays.py
--rw-rw-rw-   0        0        0     2646 2023-04-02 07:35:55.000000 n0struct-0.2.94/n0struct/n0struct_comprehensions.py
--rw-rw-rw-   0        0        0    13176 2023-04-23 10:14:47.000000 n0struct-0.2.94/n0struct/n0struct_date.py
--rw-rw-rw-   0        0        0     2847 2023-04-17 17:27:53.000000 n0struct-0.2.94/n0struct/n0struct_files.py
--rw-rw-rw-   0        0        0    22639 2023-04-02 12:49:20.000000 n0struct-0.2.94/n0struct/n0struct_files_csv.py
--rw-rw-rw-   0        0        0     7171 2023-04-02 12:54:45.000000 n0struct-0.2.94/n0struct/n0struct_files_fwf.py
--rw-rw-rw-   0        0        0    15645 2023-04-18 03:40:30.000000 n0struct-0.2.94/n0struct/n0struct_findall.py
--rw-rw-rw-   0        0        0     4070 2023-04-18 03:45:21.000000 n0struct-0.2.94/n0struct/n0struct_git.py
--rw-rw-rw-   0        0        0    20911 2023-04-18 03:47:04.000000 n0struct-0.2.94/n0struct/n0struct_logging.py
--rw-rw-rw-   0        0        0     2287 2023-03-10 04:00:32.000000 n0struct-0.2.94/n0struct/n0struct_mask.py
--rw-rw-rw-   0        0        0    12168 2023-04-23 10:15:27.000000 n0struct-0.2.94/n0struct/n0struct_n0dict_.py
--rw-rw-rw-   0        0        0    17317 2023-04-18 04:08:26.000000 n0struct-0.2.94/n0struct/n0struct_n0dict__.py
--rw-rw-rw-   0        0        0     7515 2023-04-23 06:00:38.000000 n0struct-0.2.94/n0struct/n0struct_n0list_.py
--rw-rw-rw-   0        0        0    75711 2023-04-23 13:24:17.000000 n0struct-0.2.94/n0struct/n0struct_n0list_n0dict.py
--rw-rw-rw-   0        0        0      917 2023-02-26 06:04:26.000000 n0struct-0.2.94/n0struct/n0struct_random.py
--rw-rw-rw-   0        0        0     3852 2023-04-18 04:31:43.000000 n0struct-0.2.94/n0struct/n0struct_references.py
--rw-rw-rw-   0        0        0     3233 2023-04-02 06:21:50.000000 n0struct-0.2.94/n0struct/n0struct_transform_structure.py
--rw-rw-rw-   0        0        0    17303 2023-04-02 06:34:23.000000 n0struct-0.2.94/n0struct/n0struct_utils.py
--rw-rw-rw-   0        0        0     6658 2023-04-18 04:28:52.000000 n0struct-0.2.94/n0struct/n0struct_utils_compare.py
--rw-rw-rw-   0        0        0     4117 2023-04-18 04:29:28.000000 n0struct-0.2.94/n0struct/n0struct_utils_find.py
-drwxrwxrwx   0        0        0        0 2023-04-23 14:01:16.077435 n0struct-0.2.94/n0struct/test/
--rw-rw-rw-   0        0        0        0 2022-09-04 19:16:09.000000 n0struct-0.2.94/n0struct/test/__init__.py
--rw-rw-rw-   0        0        0      136 2022-09-04 19:16:09.000000 n0struct-0.2.94/n0struct/test/__main__.py
--rw-rw-rw-   0        0        0    33263 2023-04-23 13:25:25.000000 n0struct-0.2.94/n0struct/test/test_n0struct.py
--rw-rw-rw-   0        0        0     2572 2023-03-06 04:48:48.000000 n0struct-0.2.94/n0struct/test/test_n0struct2.py
--rw-rw-rw-   0        0        0     1177 2023-03-23 03:01:29.000000 n0struct-0.2.94/n0struct/test/test_n0struct3.py
--rw-rw-rw-   0        0        0     1849 2023-04-23 14:00:38.000000 n0struct-0.2.94/n0struct/test/test_n0struct4.py
-drwxrwxrwx   0        0        0        0 2023-04-23 14:01:16.069993 n0struct-0.2.94/n0struct.egg-info/
--rw-rw-rw-   0        0        0     1060 2023-04-23 14:01:15.000000 n0struct-0.2.94/n0struct.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1032 2023-04-23 14:01:15.000000 n0struct-0.2.94/n0struct.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-23 14:01:15.000000 n0struct-0.2.94/n0struct.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-04-23 14:01:15.000000 n0struct-0.2.94/n0struct.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       55 2023-04-23 14:01:15.000000 n0struct-0.2.94/n0struct.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-04-23 14:01:15.000000 n0struct-0.2.94/n0struct.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-04-23 14:01:16.079455 n0struct-0.2.94/setup.cfg
--rw-rw-rw-   0        0        0     2476 2023-04-02 07:28:40.000000 n0struct-0.2.94/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:14:33.412640 n0struct-0.2.95/
+-rw-rw-rw-   0        0        0    11558 2022-09-04 19:16:09.000000 n0struct-0.2.95/LICENSE
+-rw-rw-rw-   0        0        0     1060 2023-05-13 11:14:33.413622 n0struct-0.2.95/PKG-INFO
+-rw-rw-rw-   0        0        0      590 2022-09-04 19:16:09.000000 n0struct-0.2.95/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 11:14:33.364735 n0struct-0.2.95/n0struct/
+-rw-rw-rw-   0        0        0      988 2023-05-13 11:12:54.000000 n0struct-0.2.95/n0struct/__init__.py
+-rw-rw-rw-   0        0        0     3671 2023-05-12 12:43:36.000000 n0struct-0.2.95/n0struct/n0struct_arrays.py
+-rw-rw-rw-   0        0        0     2647 2023-05-12 12:38:36.000000 n0struct-0.2.95/n0struct/n0struct_comprehensions.py
+-rw-rw-rw-   0        0        0    13176 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_date.py
+-rw-rw-rw-   0        0        0     3389 2023-05-13 05:52:52.000000 n0struct-0.2.95/n0struct/n0struct_files.py
+-rw-rw-rw-   0        0        0    29825 2023-05-13 09:51:04.000000 n0struct-0.2.95/n0struct/n0struct_files_csv.py
+-rw-rw-rw-   0        0        0     7180 2023-05-12 12:45:32.000000 n0struct-0.2.95/n0struct/n0struct_files_fwf.py
+-rw-rw-rw-   0        0        0    15647 2023-05-12 12:40:01.000000 n0struct-0.2.95/n0struct/n0struct_findall.py
+-rw-rw-rw-   0        0        0     4070 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_git.py
+-rw-rw-rw-   0        0        0    20938 2023-05-12 12:47:23.000000 n0struct-0.2.95/n0struct/n0struct_logging.py
+-rw-rw-rw-   0        0        0     2287 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_mask.py
+-rw-rw-rw-   0        0        0    12168 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_n0dict_.py
+-rw-rw-rw-   0        0        0    17325 2023-05-12 12:47:58.000000 n0struct-0.2.95/n0struct/n0struct_n0dict__.py
+-rw-rw-rw-   0        0        0     7517 2023-05-12 12:41:09.000000 n0struct-0.2.95/n0struct/n0struct_n0list_.py
+-rw-rw-rw-   0        0        0    75633 2023-05-13 05:34:23.000000 n0struct-0.2.95/n0struct/n0struct_n0list_n0dict.py
+-rw-rw-rw-   0        0        0      917 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_random.py
+-rw-rw-rw-   0        0        0     3852 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_references.py
+-rw-rw-rw-   0        0        0     3235 2023-05-12 12:49:17.000000 n0struct-0.2.95/n0struct/n0struct_transform_structure.py
+-rw-rw-rw-   0        0        0    18057 2023-05-12 12:49:39.000000 n0struct-0.2.95/n0struct/n0struct_utils.py
+-rw-rw-rw-   0        0        0     6659 2023-05-12 12:42:29.000000 n0struct-0.2.95/n0struct/n0struct_utils_compare.py
+-rw-rw-rw-   0        0        0     4120 2023-05-12 12:42:54.000000 n0struct-0.2.95/n0struct/n0struct_utils_find.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:14:33.412640 n0struct-0.2.95/n0struct/test/
+-rw-rw-rw-   0        0        0        0 2022-09-04 19:16:09.000000 n0struct-0.2.95/n0struct/test/__init__.py
+-rw-rw-rw-   0        0        0      136 2022-09-04 19:16:09.000000 n0struct-0.2.95/n0struct/test/__main__.py
+-rw-rw-rw-   0        0        0    33263 2023-04-23 13:25:25.000000 n0struct-0.2.95/n0struct/test/test_n0struct.py
+-rw-rw-rw-   0        0        0     2572 2023-03-06 04:48:48.000000 n0struct-0.2.95/n0struct/test/test_n0struct2.py
+-rw-rw-rw-   0        0        0     1177 2023-03-23 03:01:29.000000 n0struct-0.2.95/n0struct/test/test_n0struct3.py
+-rw-rw-rw-   0        0        0     1849 2023-04-23 14:00:38.000000 n0struct-0.2.95/n0struct/test/test_n0struct4.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:14:33.397647 n0struct-0.2.95/n0struct.egg-info/
+-rw-rw-rw-   0        0        0     1060 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1032 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       55 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 11:14:33.414602 n0struct-0.2.95/setup.cfg
+-rw-rw-rw-   0        0        0     2476 2023-04-02 07:28:40.000000 n0struct-0.2.95/setup.py
```

### Comparing `n0struct-0.2.94/LICENSE` & `n0struct-0.2.95/LICENSE`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/PKG-INFO` & `n0struct-0.2.95/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: n0struct
-Version: 0.2.94
+Version: 0.2.95
 Summary: list/dict extensions allow to load/save/serialize/deserialize xml/json/csv/dsv/fwf files into python/from structures, compare them and work with them using xpath approach
 Home-page: https://github.com/pythonist552/n0struct/
 Author: pythonist552
 Author-email: pythonist552@gmail.com
 License: ASL
 Platform: any
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `n0struct-0.2.94/README.md` & `n0struct-0.2.95/README.md`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/n0struct_arrays.py` & `n0struct-0.2.95/n0struct/n0struct_arrays.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 import typing
 # ******************************************************************************
 # ******************************************************************************
 def split_pair(
                 in_str: str,
                 delimiter: str,
-                transform_left: callable = lambda x:x,
-                transform_right: callable = lambda x:x,
+                transform_left: callable = lambda x: x,
+                transform_right: callable = lambda x: x,
                 default_element: int = 1,
                 default_left: typing.Any = None,
                 default_right: typing.Any = None,
 ) -> tuple:
     """
-    split_pair(in_str: str, delimiter: str, transform_left: callable = lambda x:x, transform_right: callable = lambda x:x, default_element: int = 1) -> tuple:
+    split_pair(in_str: str, delimiter: str, transform_left: callable = lambda x: x, transform_right: callable = lambda x: x, default_element: int = 1) -> tuple:
 
     split string into 2 sub strings in any cases:
         '' by '://'                                     => (default_left, default_right)
         'www.aaa.com' by '://'                          => (default_left, 'www.aaa.com')
         'https://www.aaa.com' by '://'                  => ('http', 'www.aaa.com')
         'www.aaa.com',default_element = 0 by '/'        => ('www.aaa.com')
         'www.aaa.com/path',default_element = 0 by '/'   => ('www.aaa.com', 'path')
@@ -31,15 +31,15 @@
         else:
             # first (left) element is default
             return transform_left(str_parts[0]), transform_right(default_right)
     return transform_left(str_parts[0]), transform_right(str_parts[1])
 # ******************************************************************************
 def join_triplets(
                     in_list: typing.Union[None, str, tuple, list],
-                    level:int = 0
+                    level: int = 0
 ) -> str:
     """
     join_triplets(in_list: typing.Union[None, str, tuple, list], level = 0) -> str:
 
     join elements with middle sepataror:
         [elem1, delimiter, elem2]   => elem1, delimiter, elem2
         [elem1, delimiter, None]    => elem1
@@ -58,15 +58,15 @@
         for item in in_list:
             out_list.append(join_triplets(item, level+1))
 
         if len(in_list) == 3:
             if isinstance(in_list[1], str):
                 result = out_list[0] +  (out_list[1] if out_list[0] and out_list[2] else "") + out_list[2]
             else:
-                if not isinstance(in_list[1], (tuple, list)) or len(in_list[1]) not in (1,2):
+                if not isinstance(in_list[1], (tuple, list)) or len(in_list[1]) not in (1, 2):
                     raise TypeError(f"{type(in_list[1])} '{in_list[1]}' is not correct delimiter")
                 if len(in_list[1]) == 2 and not in_list[1][0]:
                     result = out_list[0] +  (out_list[1] if out_list[2] else "") + out_list[2]
                 else:
                     result = out_list[0] +  (out_list[1] if out_list[0] else "") + out_list[2]
         else:
             result = "".join(out_list)
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_comprehensions.py` & `n0struct-0.2.95/n0struct/n0struct_comprehensions.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
                 file_path: str,
                 default_value = None,
                 equal_tag: str = '=',
                 comment_tags: typing.Union[tuple, list] = ("#", "//"),
                 parse_key: typing.Callable = lambda key_value, default_key: key_value[0].strip().upper(),
                 parse_value: typing.Callable = lambda key_value, default_value:
                                                         (
-                                                            round(float(stripped_value),7)
+                                                            round(float(stripped_value), 7)
                                                             if '.' in stripped_value
                                                             else int(stripped_value)
                                                         )
                                                         if isnumber(stripped_value:=key_value[1].strip())
                                                         else (
                                                             stripped_value[1:-1]
                                                             if len(stripped_value) >=2 and (
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_date.py` & `n0struct-0.2.95/n0struct/n0struct_date.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/n0struct_files.py` & `n0struct-0.2.95/n0struct/n0struct_files.py`

 * *Files 11% similar despite different names*

```diff
@@ -5,44 +5,52 @@
 from .n0struct_utils import n0eval
 from .n0struct_utils import isnumber
 # ******************************************************************************
 # ******************************************************************************
 def load_file(
                 file_path: str,
                 mode: str = 't',
-                encoding: str = "utf-8",
+                encoding: typing.Union[str, bytes] = "utf-8-sig",  # with possible UTF-8 BOM (Byte Order Mark)
 ) -> str:
     if mode == 'b':
         encoding = None
     with open(file_path, 'r'+mode, encoding=encoding) as in_filehandler:
         return in_filehandler.read()
 # ******************************************************************************
 def load_lines(
                 file_path: str,
                 mode: str = 't',
-                encoding: str = "utf-8",
+                encoding: str = "utf-8-sig",  # with possible UTF-8 BOM (Byte Order Mark)
                 EOL: str = '\n',
 ) -> typing.Generator:
     if mode == 'b':
         # Impossible to mix return and yield under single function
-        for line in load_file(file_path, mode=mode).split(bytes(EOL, encoding=encoding)):
+        if isinstance(EOL, str):
+            EOL = bytes(EOL, encoding="utf-8")
+        elif not isinstance(EOL, bytes):
+            raise TypeError(f"{EOL=} could be str or bytes for {mode=}")
+        for line in load_file(file_path, mode=mode, encoding=encoding).split(EOL):
             yield line
     else:
+        if isinstance(EOL, bytes):
+            EOL = EOL.decode("utf-8-sig")
+        elif not isinstance(EOL, str):
+            raise TypeError(f"{EOL=} could be str or bytes for {mode=}")
         with open(file_path, 'rt', encoding=encoding) as in_filehandler:
             while True:
                 line = in_filehandler.readline()
                 if not line:
                     break
                 yield line.rstrip(EOL)
 # ******************************************************************************
 def save_file(
                 file_path: str,
                 lines: typing.Union[tuple, list, dict, str, bytes, bytearray],
                 mode: str = 't',
-                encoding: str = "utf-8",
+                encoding: str = "utf-8",  # without UTF-8 BOM (Byte Order Mark)
                 EOL: str = '\n',
                 equal_tag: str = "=",
 ):
     Path(file_path).parent.mkdir(parents=True, exist_ok=True)
 
     if isinstance(lines, (list, tuple)):
         output_buffer = EOL.join(lines)
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_files_csv.py` & `n0struct-0.2.95/n0struct/n0struct_files_csv.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 import typing
 from pathlib import Path
 from .n0struct_n0list_n0dict import n0dict
 from .n0struct_n0list_n0dict import n0list
+from n0struct import * # required to use external functions in validate_csv_row()
 # ******************************************************************************
 # ******************************************************************************
 def parse_complex_csv_line(
-    line:str,
-    delimiter:str = ',',
-    process_field:callable = lambda field_value: field_value,  # possible to field_value.strip()
-    EOL:str = '\n',
+    line: str,
+    delimiter: str = ',',
+    process_field: callable = lambda field_value: field_value,  # possible to field_value.strip()
+    EOL: str = '\n',
 ) -> list:
     fields_in_the_row = []
     flag_quotes_in_the_begining = flag_expect_delimiter_or_quotes = False
     field_value = ""
-    for offset,ch in enumerate(line.strip(EOL)):
+    for offset, ch in enumerate(line.strip(EOL)):
         if ch == delimiter and (flag_quotes_in_the_begining == False or flag_expect_delimiter_or_quotes == True):
             # The next field is started
             fields_in_the_row.append(process_field(field_value))
             flag_quotes_in_the_begining = flag_expect_delimiter_or_quotes = False
             field_value = ""
             continue  # skip delimiter
         elif ch == '"':
@@ -35,142 +36,267 @@
             raise ValueError(f"Expected delimiter '{delimiter}' or second '\"', but received '{ch}' in offset {offset} of '{line}'")
         field_value += ch
     fields_in_the_row.append(process_field(field_value)) # Save the last field
     return fields_in_the_row
 # ******************************************************************************
 def load_csv(
     file_name: str,
-    column_names: list = None,
+    column_names: typing.Union[list, tuple, None] = None,
     delimiter: str = ',',
     process_field: typing.Union[callable, None] = None,
+    # process_field == None
+    #   strip_field == False                    lambda field_value: field_value
+    #   strip_field == True                     lambda field_value: field_value.strip()
     EOL: str = '\n',
-    contains_header: typing.Union[bool,str] = False,
-    process_line: typing.Union[callable, None] = None,
+    contains_header: typing.Union[bool, str, list, tuple, None] = None,
+    # contains_header == True || False          ***LEGACY***
+    #   header_is_mandatory == None             Copy value from contains_header into header_is_mandatory
+    #   header_is_mandatory != contains_header  Exception
+    #
+    # contains_header == "???"
+    #   contains_header == row[0]
+    #       column_names == []                  First row is header: column_names as is
+    #       column_names == None                First row is header: column_names = row
+    #   contains_header != row[0]
+    #       header_is_mandatory == False        First row is data
+    #       header_is_mandatory == True         Exception
+    #
+    # contains_header == []
+    #   all(contains_header[i] in row)
+    #       column_names == []                  First row is header: column_names as is
+    #       column_names == None                First row is header: column_names = row
+    #   any(contains_header[i] not in row)
+    #       header_is_mandatory == False        First row is data
+    #       header_is_mandatory == True         Exception
+    #
+    # contains_header == None
+    #   column_names == []
+    #       all(column_names[i] in row)         First row is header: column_names as is
+    #       any(column_names[i] not in row)
+    #           header_is_mandatory == True     Exception
+    #           header_is_mandatory == False    First row is data
+    #   column_names == None
+    #       header_is_mandatory == True         First row is header: column_names = row
+    #       header_is_mandatory == False        First row is data
+    process_line: typing.Union[callable, bool, None] = None,
+    # process_line == None
+    #   strip_line == False                 line_value: line_value.strip()
+    #   strip_line == True                  line_value: line_value
     skip_empty_lines: bool = True,
-    strip_line: typing.Union[bool,callable] = False,
-    strip_field: typing.Union[bool,callable] = False,
-    return_always_list: bool = False,
+    strip_line: typing.Union[bool, callable] = False,
+    strip_field: typing.Union[bool, callable] = False,
     return_original_line: bool = False,
+    # return_original_line == False         Return list/dict of fields
+    # return_original_line == True          Return tuple(list/dict of fields, read line)
     parse_csv_line: callable = parse_complex_csv_line,
-    encoding: str = "utf-8",
-) -> typing.Generator:  # list, typing.Tuple[list, str], dict, typing.Tuple[dict, str]
+    encoding: typing.Union[str, None] = "utf-8-sig",  # with possible UTF-8 BOM (Byte Order Mark)
+    read_mode: str = "t",
+    header_is_mandatory: typing.Union[bool, None] = None,
+    # header_is_mandatory == None
+    #   contains_header == True || False    Copy value from contains_header in header_is_mandatory
+    #   contains_header == None             header_is_mandatory = False
+    # header_is_mandatory == False          The first row is header or data row, depends of contains_header/column_names
+    # header_is_mandatory == True
+    #   contains_header == None
+    #       column_names == None            Exception
+    #       column_names == []              All column names from column_names are mandatory
+    #   contains_header == []               All column names from contains_header are mandatory
+    #       column_names == None            The first row is header, column_names = first row
+    #       column_names == []              The first row is header
+) -> typing.Generator:
+    # dict                                  dict of fields got from current read line
+    # typing.Tuple[dict, str]               dict of fields got from current read line, current read line
+
+    ## header_is_mandatory
+    if header_is_mandatory is None:
+        header_is_mandatory = False
+    elif not isinstance(header_is_mandatory, bool):
+        raise SyntaxError(f"Not expectable value in {header_is_mandatory=}. Should be bool or None")
+
+    ## column_names
+    if isinstance(column_names, (list, tuple)):
+        if not column_names:
+            column_names = None
+        else:
+            if len(column_names) != len(set(column_names)):
+                raise SyntaxError(f"Column names {column_names} contains not unique names of columns")
+            elif contains_header:
+                if isinstance(contains_header, str) and column_names[0] != contains_header:
+                    raise SyntaxError(f"Column names {column_names} contains not unique names of columns")
+                elif isinstance(contains_header, (list, tuple)) \
+                     and any(mandatory_column_name not in column_names for mandatory_column_name in contains_header):
+                    raise SyntaxError(f"Mandatory column names {contains_header} are not in expected column names {column_names}")
+    elif column_names is not None:
+        raise SyntaxError(f"Not expectable value in {column_names=}. Should be list/tuple/None")
+
+    ## contains_header
+    if isinstance(contains_header, (str, list, tuple)) and not contains_header:
+        contains_header = None
+    if isinstance(contains_header, bool):
+        ## LEGACY
+        if header_is_mandatory is None:
+            header_is_mandatory = contains_header
+        elif isinstance(header_is_mandatory, bool):
+            if header_is_mandatory != contains_header:
+                raise SyntaxError(f"{contains_header=} must be equal {header_is_mandatory=} if it's bool")
+        contains_header = column_names
+    elif isinstance(contains_header, str):
+        pass
+    elif isinstance(contains_header, (list, tuple)):
+        if len(contains_header) != len(set(contains_header)):
+            raise SyntaxError(f"Column names {contains_header} contains not unique names of columns")
+    elif contains_header is None:
+        contains_header = column_names
+    else:
+        raise SyntaxError(f"Not expectable type of {type(contains_header)} {contains_header=}."
+                         " Should be str (first column name) or list/tuple (mandatory column names) or bool (LEGACY) or None"
+        )
 
-    if column_names and len(column_names) != len(set(column_names)):
-        raise KeyError(f"Column names {column_names} contains not unique names of columns")
 
+    ## process_field
     if not callable(process_field):
         if isinstance(strip_field, bool) and strip_field == True:
             process_field = lambda field_value: field_value.strip()
         elif callable(strip_field):
             process_field = strip_field
         else:
             process_field = lambda field_value: field_value
 
+    ## process_line
     if not callable(process_line):
         if isinstance(strip_line, bool) and strip_line == True:
-            process_line = lambda field_value: field_value.strip()
+            process_line = lambda line_value: line_value.strip()
         elif callable(strip_line):
             process_line = strip_line
         else:
-            process_line = lambda line: line
+            process_line = lambda line_value: line_value
 
-    if not isinstance(contains_header, (str, bool)):
-        raise ValueError(f"Not expectable value in {contains_header=}. Should be bool or str")
 
-    if not process_line:
-        process_line = lambda line_value: line_value
-    elif isinstance(process_line, bool) and process_line == True:
-        process_line = lambda line_value: line_value.strip()
+    with open(file_name, mode='r'+read_mode, encoding=encoding) as in_file:
+        # skip empty lines at the begining of the file
+        while True:
+            file_offset = in_file.tell()
+            line = in_file.readline()  # removed walrus operator for compatibility with 3.7
+            if not line:
+                raise EOFError("Empty file or file only with spaces")
+            header_line = process_line(line.rstrip(EOL))
+            if header_line:
+                break
+
+        possible_column_names = parse_csv_line(header_line, delimiter, process_field)
+        # n0debug("possible_column_names")
+        # n0debug("contains_header")
+        # n0debug("header_is_mandatory")
 
-    with open(file_name, 'rt', encoding=encoding) as in_file:
+        first_line_is_header = False
         if contains_header:
-            while True:  # skip empty lines at the begining of the file
-                file_offset = in_file.tell()
-                line = in_file.readline()  # removed walrus operator for compatibility with 3.7
-                if not line:
-                    return [] # Empty file or file only with spaces
-                header_line = process_line(line.rstrip(EOL))
-                if header_line:
-                    break
-            possible_column_names = parse_csv_line(header_line, delimiter, process_field)
             if isinstance(contains_header, str):
-                # if contains_header is not boolean, then first line could be header or not
-                # to check if the first line is header, check value of first column
-                # if it's like expected, then the first line is header
                 if possible_column_names[0] != contains_header:
-                    in_file.seek(file_offset) # first line is NOT header, re-read first line as data line
-                    possible_column_names = None
-            else:
-                if column_names:
-                    if isinstance(contains_header, bool):
-                        if set(possible_column_names) != set(column_names):
-                            raise KeyError(f"Expected column names {column_names}, but read {possible_column_names}")
+                    if header_is_mandatory:
+                        raise ReferenceError(f"First line is not header {possible_column_names}. Expected first column '{contains_header}'")
                 else:
-                    if possible_column_names:
-                        # Only in case of
-                        #   contains_header = "first column name",
-                        #   first line contains the header
-                        #   column_names = None
-                        column_names = possible_column_names
+                    first_line_is_header = True
+            elif isinstance(contains_header, (list, tuple)):
+                if any(mandatory_column_name not in possible_column_names for mandatory_column_name in contains_header):
+                    if header_is_mandatory:
+                        raise ReferenceError(f"First line is not header {possible_column_names}. Expected {contains_header}")
+                else:
+                    first_line_is_header = True
+        else:
+            if header_is_mandatory and not column_names:
+                first_line_is_header = True
+
+        # n0debug("first_line_is_header")
+        if not first_line_is_header:
+            in_file.seek(file_offset) # first line is NOT header, re-read first line as data line
+            if column_names:
+                possible_column_names = column_names
+            else:
+                column_names = possible_column_names = [i for i in range(len(possible_column_names))]
+        else:
+            if header_is_mandatory and len(possible_column_names) != len(set(possible_column_names)):
+                raise KeyError(f"Read header {possible_column_names} contains not unique names of columns")
+            if not column_names:
+                column_names = possible_column_names
+        len_possible_column_names = len(possible_column_names)
+        # n0debug("column_names")
+        # n0debug("possible_column_names")
 
         while True:
             line = in_file.readline()  # removed walrus operator for compatibility with 3.7
             if not line:
                 return None  # EOF
             stripped_line = process_line(line.rstrip(EOL))
             if skip_empty_lines and not stripped_line:
                 continue
-            field_values = parse_csv_line(stripped_line, delimiter, process_field, EOL)
-            if not column_names or return_always_list:
-                if return_original_line:
-                    yield field_values, stripped_line
-                else:
-                    yield field_values
+
+            # removed walrus operator for compatibility with 3.7
+            list_field_values = parse_csv_line(stripped_line, delimiter, process_field, EOL)
+            dict_field_values = n0dict( zip(
+                                    possible_column_names,
+                                    list_field_values
+                                    + [None for i in range(len_possible_column_names - len(list_field_values))]
+            ))
+            if column_names != possible_column_names:
+                # n0debug("column_names")
+                # n0debug("possible_column_names")
+                dict_field_values = n0dict({
+                    key: dict_field_values[key]
+                    for key in column_names
+                })
+            # n0debug("dict_field_values")
+            # n0debug("return_original_line")
+            if return_original_line:
+                yield dict_field_values, stripped_line
             else:
-                if return_original_line:
-                    yield n0dict(zip(column_names, field_values)), stripped_line
-                else:
-                    yield n0dict(zip(column_names, field_values))
+                yield dict_field_values
 # ******************************************************************************
 load_complex_csv = load_csv  # Synonym
 # ******************************************************************************
 def load_simple_csv(
     file_name: str,
-    column_names: list = None,
+    column_names: typing.Union[list, tuple, None] = None,
     delimiter: str = ',',
     process_field: typing.Union[callable, None] = None,
     EOL: str = '\n',
-    contains_header: typing.Union[bool,str] = False,
-    process_line: typing.Union[callable, None] = None,
+    contains_header: typing.Union[bool, str, list, tuple, None] = None,
+    process_line: typing.Union[callable, bool, None] = None,
     skip_empty_lines: bool = True,
-    strip_line: typing.Union[bool,callable] = False,
-    strip_field: typing.Union[bool,callable] = False,
-    return_always_list: bool = False,
+    strip_line: typing.Union[bool, callable] = False,
+    strip_field: typing.Union[bool, callable] = False,
     return_original_line: bool = False,
-) -> typing.Generator:  # list, typing.Tuple[list, str], dict, typing.Tuple[dict, str]
+    parse_csv_line: callable = lambda line, delimiter, process_field: [process_field(field_value) for field_value in line.split(delimiter)],
+    encoding: typing.Union[str, None] = "utf-8-sig",  # with possible UTF-8 BOM (Byte Order Mark)
+    read_mode: str = "t",
+    header_is_mandatory: typing.Union[bool, None] = None,
+) -> typing.Generator:
+    # dict                                  dict of fields got from current read line
+    # typing.Tuple[dict, str]               dict of fields got from current read line, current read line
     return load_csv(
-        file_name               = file_name,
-        column_names            = column_names,
-        delimiter               = delimiter,
-        process_field           = process_field,
-        EOL                     = EOL,
-        contains_header         = contains_header,
-        process_line            = process_line,
-        skip_empty_lines        = skip_empty_lines,
-        strip_line              = strip_line,
-        strip_field             = strip_field,
-        return_always_list      = return_always_list,
-        return_original_line    = return_original_line,
-        parse_csv_line          = lambda line, delimiter, process_field: [process_field(field_value) for field_value in line.split(delimiter)],
+        file_name            = file_name,
+        column_names         = column_names,
+        delimiter            = delimiter,
+        process_field        = process_field,
+        EOL                  = EOL,
+        contains_header      = contains_header,
+        process_line         = process_line,
+        skip_empty_lines     = skip_empty_lines,
+        strip_line           = strip_line,
+        strip_field          = strip_field,
+        return_original_line = return_original_line,
+        parse_csv_line       = parse_csv_line,
+        encoding             = encoding,
+        read_mode            = read_mode,
+        header_is_mandatory  = header_is_mandatory,
     )
 # ******************************************************************************
 def generate_comlex_csv_row(
-    row:list,
-    delimiter:str = ',',
-    EOL:str = '\n',
+    row: list,
+    delimiter: str = ',',
+    EOL: str = '\n',
 ) -> str:
     generated_csv_row = ""
     for field_value in row:
         if field_value is None:
             field_value = ""
         elif not isinstance(field_value, str):
             field_value = str(field_value)
@@ -178,20 +304,20 @@
             if '"' in field_value:
                 field_value = field_value.replace('"', '""')
             field_value = '"' + field_value + '"'
         generated_csv_row += field_value + delimiter
     return generated_csv_row[:-len(delimiter)] + EOL
 # ******************************************************************************
 def generate_csv(
-    root_node:dict,
-    list_xpath:str,
-    mapping_dict:dict = None,
-    save_to:str = None,
-    delimiter:str = ',',
-    show_header:bool = True
+    root_node: dict,
+    list_xpath: str,
+    mapping_dict: dict = None,
+    save_to: str = None,
+    delimiter: str = ',',
+    show_header: bool = True
 ) -> list:
     '''
     Samples:
         response_json = n0dict({
             "records" : [
                 {
                     "node" : {
@@ -249,15 +375,15 @@
     if save_to:
         out_filehandler = open(save_to, 'wt')
 
     csv_table = []
     if list_of_items:
         if mapping_dict is None:
             if isinstance(list_of_items[0], list):
-                header = [str(i) for i in range(0,len(list_of_items[0]))]
+                header = [str(i) for i in range(0, len(list_of_items[0]))]
             elif isinstance(list_of_items[0], dict):
                 header = list(list_of_items[0].keys())
             mapping_dict = {column_name: column_name for column_name in header}
         else:
             header = list(mapping_dict.keys())
 
         if save_to and show_header:
@@ -291,15 +417,15 @@
 # ******************************************************************************
 def remove_colums_in_csv(
     columns_to_remove: list,
     csv_rows: list = None,
     csv_schema: dict = None,
     are_required: bool = False
 ):
-    if all([isinstance(column_to_remove,int) for column_to_remove in columns_to_remove]) \
+    if all([isinstance(column_to_remove, int) for column_to_remove in columns_to_remove]) \
        and len(csv_rows) and isinstance(csv_rows[0], list):
         columns_to_remove.sort(reverse=True) # delete firstly last elements in the list
 
 
     for row_index, row in enumerate(csv_rows):
         # Remove columns in structure
         if isinstance(csv_rows[row_index], (dict, list)):
@@ -355,14 +481,16 @@
         return csv_rows
 # ******************************************************************************
 def validate_csv_row(
     row: typing.Union[list, dict],
     csv_schema: dict,
     external_variables = {},
     interrupt_after_first_fail: bool = False,
+    row_i: int = None,
+    rows_count: int = 0,
 ):
     '''
     row:
         list: [field_value[0], field_value[1], ... field_value[i]]
         dict: {column_name[0]: field_value[0], column_name[1]: field_value[1], ... column_name[i]: field_value[i]}
     csv_schema: dict
         //items[0..i]/id                     = column_name[i]
@@ -398,62 +526,68 @@
     columns_count = len(row)
     min_items = int(csv_schema.get("minItems", -1))     # removed walrus operator for compatibility with 3.7
     if columns_count < min_items:
         failed_validations[the_whole_row_related_validations].append(f"Mimimum {min_items} columns expected, but got {columns_count}")
     max_items = int(csv_schema.get("maxItems", 9999))   # removed walrus operator for compatibility with 3.7
     if columns_count > max_items:
         failed_validations[the_whole_row_related_validations].append(f"Maximum {max_items} columns expected, but got {columns_count}")
-        
+
     required_columns = csv_schema.get("required")       # removed walrus operator for compatibility with 3.7
     if required_columns and isinstance(required_columns, (list, tuple)):
         for required_column in required_columns:
             if required_column not in row:
                 failed_validations[the_whole_row_related_validations].append(f"Required column '{required_column}' doesn't exist in row")
     if not failed_validations[the_whole_row_related_validations]:
         del failed_validations[the_whole_row_related_validations]
     elif interrupt_after_first_fail:
         return failed_validations
 
     mapped_values = {**external_variables, **{f'value_{column_name}': row[column_name] for column_name in row}}
 
+    row_last = rows_count - 1
     for column_name in row:
         field_value = row[column_name]
         column_schema = csv_schema.first(f"items/[id={column_name}]")
-        mapped_values.update({
+        mapped_values.update({  # Used in validation_lambda/validation_msg
             'column_name': column_name,
             'column_value': field_value,  # Legacy
             'field_value': field_value,
             'column_schema': column_schema,
+            'row_i': row_i,
+            'rows_count': rows_count,
+            'row_last': row_last,
         })
 
         if column_schema.get('mandatory', False) and not field_value:
             failed_validations.update({column_name: f"mandatory column '{column_name}' is empty"})
             continue
 
         for validation in column_schema.get('validations', ()):
             validation_msg = None
-            if isinstance(validation, (list,tuple)):
+            if isinstance(validation, (list, tuple)):
                 validation_lambda = validation[0]
                 if len(validation) >= 2:
                     validation_msg = validation[1]
             else:
                 validation_lambda = validation
 
             is_valid = False
             try:
-                lambda_function_for_validation = eval("lambda field_value, row: " + validation_lambda.format(**mapped_values))
+                lambda_function_for_validation = eval(
+                    "lambda column_name, field_value, row, row_i, row_last: " + validation_lambda.format(**mapped_values)
+                )
             except Exception as ex1:
                 validation_msg = f"Not passed validation #1 for '{column_name}': " + str(ex1)
             else:
                 try:
-                    is_valid = lambda_function_for_validation(field_value, row)
+                    is_valid = lambda_function_for_validation(column_name, field_value, row, row_i, row_last)
                 except Exception as ex2:
                     validation_msg = f"Not passed validation #2 for '{column_name}': " + str(ex2)
-                    
-            if is_valid == False:
+
+            if not is_valid:
                 if column_name not in failed_validations:
                     failed_validations.update({column_name: []})
 
                 try:
                     failed_validation_message = validation_msg.format(**mapped_values)
                 except Exception as ex3:
                     failed_validation_message = f"Not passed validation #3 for '{column_name}': " + str(ex3)
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_files_fwf.py` & `n0struct-0.2.95/n0struct/n0struct_files_fwf.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 )
 # ******************************************************************************
 # ******************************************************************************
 def load_fwf_format(file_path: str):
     # fwf_format file is csv file, contains columns:
     #   #,name,offset,size,till
     loaded_format = load_csv(file_path)
-    for i,column in enumerate(loaded_format):
+    for i, column in enumerate(loaded_format):
         loaded_format[i]['offset'] = to_int(column['offset'], default_value = None)
         loaded_format[i]['till']   = to_int(column['till'], default_value = None)
         loaded_format[i]['size']   = to_int(column['size'], default_value = None)
     return loaded_format
 # ******************************************************************************
 def parse_fwf_line(incoming_row: str, fwf_format: dict, validate: bool = True):
     if not fwf_format:
@@ -46,15 +46,15 @@
                 if not lambda_function_for_validation(column_value, parsed_line):
                     error_messages.append(format_column['error_message'])
         if error_messages:
             return incoming_row, ";".join(error_messages)
             
     return parsed_line
 # ******************************************************************************
-def load_fwf(file_path:str, header_format: dict, body_format: dict = None, tail_format: dict = None, validate: bool = True):
+def load_fwf(file_path: str, header_format: dict, body_format: dict = None, tail_format: dict = None, validate: bool = True):
     success_parsed_lines = []
     failed_lines = []
     if not header_format:
         raise SyntaxError("header_format is mandatory parameter")
     if not body_format:
         body_format = header_format
     if not tail_format:
@@ -74,15 +74,15 @@
             parsed_line = parse_fwf_line(previous_line, tail_format, validate)
             if isinstance(parsed_line, dict):
                 success_parsed_lines.append(parsed_line)
             else:
                 failed_lines.append(parsed_line)
     return success_parsed_lines, failed_lines
 # ******************************************************************************
-def generate_fwf_row(struct_to_save: dict, fwf_format: dict, filler:str = ' '):
+def generate_fwf_row(struct_to_save: dict, fwf_format: dict, filler: str = ' '):
     if not fwf_format:
         raise SyntaxError("fwf_format is mandatory parameter")
 
     line_len = max([column['till'] for column in fwf_format])
     rendered_line = filler*line_len
 
     for format_column in fwf_format:
@@ -99,28 +99,28 @@
             column_value = str(column_value).zfill(format_column_size)[:format_column_size]
         else:
             column_value = str(column_value).ljust(format_column_size)[:format_column_size]
         rendered_line = rendered_line[:format_column['offset']] +  column_value + rendered_line[format_column['till']:]
 
     return rendered_line
 # ******************************************************************************
-def generate_fwf(root_node:dict, list_xpath:str, mapping_dict:dict, fwf_format: dict, save_to:str = None, filler:str = ' ') -> list:
+def generate_fwf(root_node: dict, list_xpath: str, mapping_dict: dict, fwf_format: dict, save_to: str = None, filler: str = ' ') -> list:
     if isinstance(root_node, (list, tuple)):
         list_of_items = root_node
     else:
         list_of_items = root_node.get(list_xpath, tuple())
         
     if save_to:
         out_filehandler = open(save_to, 'wt')
 
     fwf_table = []
     if list_of_items:
         if mapping_dict is None:
             if isinstance(list_of_items[0], list):
-                header = [str(i) for i in range(0,len(list_of_items[0]))]
+                header = [str(i) for i in range(0, len(list_of_items[0]))]
             elif isinstance(list_of_items[0], dict):
                 header = list(list_of_items[0].keys())
             mapping_dict = {column_name: column_name for column_name in header}
         else:
             header = list(mapping_dict.keys())
 
         for found_item in list_of_items:  # found_item == row in case of CSV list or item node in case of XML structure
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_findall.py` & `n0struct-0.2.95/n0struct/n0struct_findall.py`

 * *Files 1% similar despite different names*

```diff
@@ -29,15 +29,15 @@
 # ******************************************************************************
 def findfirst(current_node: typing.Union[dict, list], seeked_xpath_str: str, raise_exception = True) -> tuple:
     found = findall(current_node, seeked_xpath_str, False)
     if not found:
         if raise_exception:
             raise IndexError(f"Not found item {seeked_xpath_str}")
         else:
-            return None,None
+            return None, None
     elif len(found) > 1 and raise_exception:
         raise IndexError(f"Found more that single item {seeked_xpath_str}")  # In case of more than 1 found
             
     found_key = list(found.keys())[0]  # Return first pair in any cases: key, value
     return found_key, found[found_key]
 # ******************************************************************************
 def _findall(
@@ -125,15 +125,15 @@
                     equal_condition = False
                     condition_delimiter = '!='
                 elif after_text.startswith('<>'):
                     equal_condition = False
                     condition_delimiter = '<>'
                 else:
                     raise TypeError(f"Unknown logic condition [{child_index}] in '{str(seeked_xpath_list[0])}'")
-                before_condition,after_condition = child_index.split(condition_delimiter, 1)
+                before_condition, after_condition = child_index.split(condition_delimiter, 1)
                 value_for_condition = after_condition.strip()
                 if len(value_for_condition) > 1 and \
                    (
                        (value_for_condition.startswith('"') and value_for_condition.endswith('"'))
                        or
                        (value_for_condition.startswith("'") and value_for_condition.endswith("'"))
                    ):
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_git.py` & `n0struct-0.2.95/n0struct/n0struct_git.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/n0struct_logging.py` & `n0struct-0.2.95/n0struct/n0struct_logging.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,27 +6,27 @@
 import typing
 from .n0struct_date import date_timestamp
 # ******************************************************************************
 # ******************************************************************************
 # __prev_end = "\n"
 
 __debug_show_object_type = True
-def set_debug_show_object_type(debug_show_object_type:bool):
+def set_debug_show_object_type(debug_show_object_type: bool):
     global __debug_show_object_type
     __debug_show_object_type = debug_show_object_type
 
 
 __debug_show_object_id = True
-def set_debug_show_object_id(debug_show_object_id:bool):
+def set_debug_show_object_id(debug_show_object_id: bool):
     global __debug_show_object_id
     __debug_show_object_id = debug_show_object_id
 
 
 __debug_show_item_count = True
-def set_debug_show_item_count(debug_show_item_count:bool):
+def set_debug_show_item_count(debug_show_item_count: bool):
     global __debug_show_item_count
     __debug_show_item_count = debug_show_item_count
 
 
 __main_log_filename = None
 def init_logger(
         debug_level: str = "TRACE",
@@ -91,23 +91,23 @@
 # ******************************************************************************
 def n0error(text: str, internal_call: int = 0):
     n0print(text, level = "ERROR", internal_call = internal_call + 1)
 # ******************************************************************************
 def n0pretty(
             item: typing.Any,
             indent_: int = 0,
-            show_type:bool = None,
+            show_type: bool = None,
             __indent_size: int = 4,
-            __quotes:str = '"',
-            pairs_in_one_line:bool = True,
-            json_convention:bool = False,
-            skip_empty_arrays:bool = False,
-            skip_simple_types:bool = True,
-            auto_quotes:bool = True,
-            show_item_count:bool = None,
+            __quotes: str = '"',
+            pairs_in_one_line: bool = True,
+            json_convention: bool = False,
+            skip_empty_arrays: bool = False,
+            skip_simple_types: bool = True,
+            auto_quotes: bool = True,
+            show_item_count: bool = None,
 ):
     """
     :param item:
     :param indent_:
     :return:
     """
     # ######################################################################
@@ -292,15 +292,15 @@
         and (not skip_simple_types or not isinstance(item, (str, int, float))):
             # removed walrus operator for compatibility with 3.7
             result_type = str(type(item)).replace("<class '", "<").replace("'>", " ")
             if result_type:
                 class_type_parts = result_type.split('.')
                 if len(class_type_parts) > 2:
                     # leave just only first and last class names
-                    result_type = ".".join((class_type_parts[0],class_type_parts[-1]))
+                    result_type = ".".join((class_type_parts[0], class_type_parts[-1]))
 
             if isinstance(item, (str, bytes, bytearray, list, tuple, set, frozenset, dict)):
                 result_type += f" {len(item)}"
             result_type += "> "
 
         if result or skip_empty_arrays == False:
             if "\n" in result:
@@ -336,21 +336,21 @@
 
         if isinstance(item, bool) and json_convention:
             result = result.lower()
 
     return result
 # ******************************************************************************
 def n0debug_calc(var_object, var_name: str = "", level: str = "DEBUG", internal_call: int = 0,
-            show_type:bool = None,
-            pairs_in_one_line:bool = True,
-            json_convention:bool = False,
-            skip_empty_arrays:bool = False,
-            skip_simple_types:bool = True,
-            auto_quotes:bool = True,
-            show_item_count:bool = None,
+            show_type: bool = None,
+            pairs_in_one_line: bool = True,
+            json_convention: bool = False,
+            skip_empty_arrays: bool = False,
+            skip_simple_types: bool = True,
+            auto_quotes: bool = True,
+            show_item_count: bool = None,
 ):
     """
     Print  calculated value (for example returned by function),
     depends of value in global variable __debug_level.
 
     :param var_object:
     :param var_name:
@@ -385,31 +385,31 @@
         ,
         level = level,
         internal_call = internal_call + 1,
     )
 # ******************************************************************************
 def n0debug(var_name: str, level: str = "DEBUG",
 
-            show_type:bool = None,
-            pairs_in_one_line:bool = True,
-            json_convention:bool = False,
-            skip_empty_arrays:bool = False,
-            skip_simple_types:bool = True,
-            auto_quotes:bool = True,
-            show_item_count:bool = None,
+            show_type: bool = None,
+            pairs_in_one_line: bool = True,
+            json_convention: bool = False,
+            skip_empty_arrays: bool = False,
+            skip_simple_types: bool = True,
+            auto_quotes: bool = True,
+            show_item_count: bool = None,
 ):
     """
     Print value of the variable with name {var_name},
     depends of value in global variable {__debug_level}.
 
     :param var_name:
     :param level:
     :return:
     """
-    if not isinstance(var_name,str):
+    if not isinstance(var_name, str):
         raise TypeError("incorrect call of n0debug(..): argument MUST BE string")
 
     __f_locals = inspect.currentframe().f_back.f_locals
     if var_name not in __f_locals:
         raise NameError(f"impossible to find object '{var_name}'")
     var_object = __f_locals.get(var_name)
     n0debug_calc(
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_mask.py` & `n0struct-0.2.95/n0struct/n0struct_mask.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/n0struct_n0dict_.py` & `n0struct-0.2.95/n0struct/n0struct_n0dict_.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/n0struct_n0dict__.py` & `n0struct-0.2.95/n0struct/n0struct_n0dict__.py`

 * *Files 1% similar despite different names*

```diff
@@ -140,15 +140,15 @@
         else:
             super(n0dict__, self).__setitem__(xpath, new_value)
 
         return new_value  # For speed
     # **************************************************************************
     def delete(self, xpath: str, recursively: bool = False) -> n0dict__:
         xpath_list = xpath.split('/')
-        for i,last_xpath_index in enumerate(range(len(xpath_list), 0, -1)):
+        for i, last_xpath_index in enumerate(range(len(xpath_list), 0, -1)):
             parent_node, node_name_index, cur_value, xpath_found_str, not_found_xpath_list = \
                 self._find(xpath_list[0:last_xpath_index], self, return_lists=True)
             if i == 0 or (
                 recursively and
                 isinstance(cur_value, n0dict__) and not len(cur_value)
             ):
                 if isinstance(parent_node, list) and not isinstance(node_name_index, int):
@@ -178,38 +178,38 @@
     # **************************************************************************
     def all_valid(self, validate):
         return not self._consists_of(validate, False)
     # **************************************************************************
     def all_not_valid(self, validate):
         return not self._consists_of(validate, True)
     # **************************************************************************
-    def valid(self, node_xpath:str, validate, expected_result_for_error: bool = False, msg:str = None):
+    def valid(self, node_xpath: str, validate, expected_result_for_error: bool = False, msg: str = None):
         """
         :param node_xpath:
             xpath to the node inside self
         :param validate:
             list/scalar/function = validation
         :param expected_result_for_error:
             By default expected that if result of validation is True, then self[node_xpath] is not valid (return False)
         :param msg:
             if None => return result as bool True(validation)/False
         :return:
 
         Examples:
-            xml.valid('node/subnode', ["",None], True, "ERROR")
+            xml.valid('node/subnode', ["", None], True, "ERROR")
                 If xml['node/subnode'] is equal "" or None (result of comparising is True), then return ERROR, else ""
-            xml.valid('node/subnode', ["",None], True)
+            xml.valid('node/subnode', ["", None], True)
                 If xml['node/subnode'] is equal "" or None (result of comparising is True), then return False (not valid), else True
             xml.valid('node/subnode', "", True)
                 If xml['node/subnode'] is equal "" (result of comparising is True), then return False (not valid), else True
-            xml.valid('node/subnode', [1,2], False, "ERROR")
+            xml.valid('node/subnode', [1, 2], False, "ERROR")
                 If xml['node/subnode'] is not equal 1 or 2 (result of comparising is False), then return ERROR, else ""
-            xml.valid('node/subnode', [1,2], False)
+            xml.valid('node/subnode', [1, 2], False)
                 If xml['node/subnode'] is not equal 1 or 2 (result of comparising is False), then return False (not valid), else True
-            xml.valid('node/subnode', [1,2])
+            xml.valid('node/subnode', [1, 2])
                 If xml['node/subnode'] is not equal 1 or 2 (result of comparising is False), then return False (not valid), else True
         """
         try:
             node_value = self.get(node_xpath)
             if callable(validate):
                 validate_result = validate(node_value)
             elif isinstance(validate, (list, tuple)):
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_n0list_.py` & `n0struct-0.2.95/n0struct/n0struct_n0list_.py`

 * *Files 1% similar despite different names*

```diff
@@ -93,21 +93,21 @@
         """
         if isinstance(xpath, str):
             return self._get(xpath, raise_exception = True)
         else:
             return super(n0list_, self).__getitem__(xpath)
     # # **************************************************************************
     # # def append(self, sigle_item):
-    # # if isinstance(sigle_item, (list,n0list_)):
+    # # if isinstance(sigle_item, (list, n0list_)):
     # # raise (TypeError, f"({type(sigle_item)}){sigle_item} must be scalar")
     # # super(n0list_, self).append(sigle_item)  #append the item to itself (the list)
     # # return self
     # # **************************************************************************
     # # def extend(self, other_list):
-    # # if not isinstance(other_list, (list,n0list_)):
+    # # if not isinstance(other_list, (list, n0list_)):
     # # raise (TypeError, f"({type(sigle_item)}){sigle_item} must be list")
     # # super(n0list_, self).extend(other_list)
     # # return self
     # # **************************************************************************
     def _in(self, other_list, in_is_expected: bool):
         if not isinstance(other_list, (list, tuple)):
             other_list = [other_list]
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_n0list_n0dict.py` & `n0struct-0.2.95/n0struct/n0struct_n0list_n0dict.py`

 * *Files 0% similar despite different names*

```diff
@@ -117,15 +117,15 @@
 
             # ..................................................................
             # Try to check all [*] items in the loop
             # ..................................................................
             if node_index_str == "*":
                 cur_values = n0list()
                 fst_parent_node = fst_node_name_index = fst_value = fst_found_xpath_str = None
-                for i,next_parent_node in enumerate(parent_node):
+                for i, next_parent_node in enumerate(parent_node):
                     if isinstance(next_parent_node, dict):
                         cur_parent_node, cur_node_name_index, cur_value, cur_found_xpath_str, \
                             cur_not_found_xpath_list = n0dict._find(next_parent_node, xpath_list[1:], next_parent_node, return_lists,  xpath_found_str + f"[{i}]")
                     elif isinstance(next_parent_node, (list, tuple)):
                         cur_parent_node, cur_node_name_index, cur_value, cur_found_xpath_str, \
                             cur_not_found_xpath_list = self._find(xpath_list[1:], next_parent_node, return_lists, xpath_found_str + f"[{i}]")
                     else:
@@ -649,19 +649,17 @@
 
             file=f"{file_path}" =>  load XML-text/JSON-text from {file_path}
         """
         len__args = len(args)
         if not len__args:
             _file = kw.pop("file", None)
             if _file:
-                with open(_file, "rb") as in_filehandler:
-                    buffer_bytes = in_filehandler.read()
-                    if buffer_bytes[:3] == b'\xEF\xBB\xBF': # UTF-8 BOM (Byte Order Mark)
-                        buffer_bytes = buffer_bytes[3:]
-                    self.__init__(buffer_bytes.decode('utf-8').strip(), **kw)
+                _encoding = kw.pop("encoding", "utf-8-sig") # with possible UTF-8 BOM (Byte Order Mark)
+                with open(_file, "rt", encoding=_encoding) as in_filehandler:
+                    self.__init__(in_filehandler.read().strip(), **kw)
             else:
                 super(n0dict, self).__init__(*args, **kw)
         elif len__args == 1:
             # Not kw.pop()! Because of in case of .get "recursively" will be provided deeper into _constructor(..)
             _recursively = kw.get("recursively", False)
             if isinstance(args[0], str):
                 if _recursively:
@@ -691,22 +689,22 @@
                             value = n0dict(value, recursively = _recursively)
                         elif isinstance(value, (list, tuple)):
                             value = n0list(value, recursively = _recursively)
                     self.update({key: value})
             elif isinstance(args[0], (list, tuple)):
                 # [key1, value1, key2, value2, ..., keyN, valueN]
                 if (len(args[0]) % 2) == 0 and all(isinstance(itm, str) for itm in args[0][0::2]):
-                    for key, value in zip(args[0][0::2],args[0][1::2]):
+                    for key, value in zip(args[0][0::2], args[0][1::2]):
                         self.update({key: value})
                 # [(key1, value1), (key2, value2), ..., (keyN, valueN)]
-                elif all(isinstance(itm, (tuple,list)) and len(itm) == 2 and isinstance(itm[0], str) for itm in args[0]):
+                elif all(isinstance(itm, (tuple, list)) and len(itm) == 2 and isinstance(itm[0], str) for itm in args[0]):
                     for pair in args[0]:
                         self.update({pair[0]: pair[1]})
                 else:
-                    raise TypeError(f"Expected even strings in the list [k1,v1,k2,v2] or list of pairs [[k1,v1],[k2,v2]] as argument for n0dict.__init__({args})")
+                    raise TypeError(f"Expected even strings in the list [k1, v1, k2, v2] or list of pairs [[k1, v1],[k2, v2]] as argument for n0dict.__init__({args})")
             elif isinstance(args[0], zip):
                 for key, value in args[0]:
                     self.update({key: value})
             else:
                 raise TypeError(f"Expected str/dict/list/tuple/zip, but received {type(args[0])} as first argument for n0dict.__init__({args})")
         else:
             raise TypeError("n0dict.__init__(..) takes exactly one notnamed argument (string (XML or JSON) or dict/zip or paired tuple/list)")
@@ -1113,15 +1111,15 @@
             # ..................................................................
             elif node_index == "*":
                 if not isinstance(parent_node, (list, tuple)):
                     # Hidden list. Convert single item into list
                     parent_node = [parent_node]
                 cur_values = n0list()
                 fst_parent_node = fst_node_name_index = fst_value = fst_found_xpath_str = None
-                for i,cur_node in enumerate(parent_node):
+                for i, cur_node in enumerate(parent_node):
                     cur_parent_node, cur_node_name_index, cur_value, cur_found_xpath_str, \
                         cur_not_found_xpath_list = self._find([f"[{i}]"] + xpath_list[1:], parent_node, return_lists, xpath_found_str)
                     if not cur_not_found_xpath_list:
                         cur_values.append(cur_value)
                         if not fst_found_xpath_str:
                             fst_parent_node, fst_node_name_index, fst_value, fst_found_xpath_str = \
                                 cur_parent_node, cur_node_name_index, cur_value, cur_found_xpath_str
@@ -1361,12 +1359,12 @@
         # **********************************************************************
         if isinstance(xpath, dict) and new_value is None:
             for item_key in xpath:
                 multi_define(item_key, xpath[item_key])
         elif isinstance(xpath, str) and new_value is not None:
             multi_define(xpath, new_value)
         else:
-            raise TypeError(f"Received (type(xpath),{type(new_value)}) as argument, but expected (key,value) or (dict).")
+            raise TypeError(f"Received (type(xpath),{type(new_value)}) as argument, but expected (key, value) or (dict).")
         return self
 # ******************************************************************************
 # ******************************************************************************
 # ******************************************************************************
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_random.py` & `n0struct-0.2.95/n0struct/n0struct_random.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/n0struct_references.py` & `n0struct-0.2.95/n0struct/n0struct_references.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/n0struct_transform_structure.py` & `n0struct-0.2.95/n0struct/n0struct_transform_structure.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 from .n0struct_utils import isnumber
 # ******************************************************************************
 # ******************************************************************************
-strip_ns = lambda key: key.split(':',1)[1] if ':' in key else key
+strip_ns = lambda key: key.split(':', 1)[1] if ':' in key else key
 # ******************************************************************************
 '''
 # Sample
 currency_converter = {"682": "SAR"}
 keys_for_currency_convertion = {
     "currency":         lambda value: currency_converter[value] if value in currency_converter else value,
     "source_currency":  lambda value: currency_converter[value] if value in currency_converter else value,
 }
 sample: def convert_to_native_format(value, key = None, exception = None, transform_depends_of_key = keys_for_currency_convertion):
 '''
 # ******************************************************************************
-def convert_to_native_format(value, key = None, exception: set = None, transform_depends_of_key:dict = None):
+def convert_to_native_format(value, key = None, exception: set = None, transform_depends_of_key: dict = None):
     if key is not None:
         if exception and key in exception:
             return value
         if transform_depends_of_key and key in transform_depends_of_key:
             return transform_depends_of_key[key](value)
     if isinstance(value, str):
         value = value.strip()
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_utils.py` & `n0struct-0.2.95/n0struct/n0struct_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -89,30 +89,30 @@
         deserialize_list_of_lists(buffer_str) == ["ITEM1", "ITEM2", "ITEM3"]
     '''
     if not isinstance(buffer_str, str):
         return default_list_result or []
 
     separated_items = buffer_str.split(delimiter)
     deserialized_list = []
-    for item_index,item in enumerate(separated_items):
+    for item_index, item in enumerate(separated_items):
         if item or parse_empty:
             parsed_item = parse_item(item, item_index = item_index, separated_items = separated_items, previous_items = deserialized_list)
             deserialized_list.append(parsed_item)
     return deserialized_list
 # ******************************************************************************
 def deserialize_key_value(
                         buffer_str: str,
                         equal_tag: str = "=",
                         parse_key: typing.Callable = lambda key_value, default_key: key_value[0],
 # Sample of calling:
 #   default_key(key_value, parsed_value)
 # Sample of definition:
 #   lambda key_value, parsed_value: parsed_value.get('SQL_FILE') if isinstance(parsed_value, dict) else key_value
                         default_key: typing.Union[typing.Callable, typing.Any, None] = None,
-                        
+
                         parse_value: typing.Callable = lambda key_value, default_value: key_value[1],
 # Sample of calling:
 #   default_value(key_value, parsed_key)
 # Sample of definition:
 #   lambda key_value, parsed_key: key_value
                         default_value: typing.Union[typing.Callable, typing.Any, None] = None,
                         default_tuple_result = None,
@@ -125,15 +125,15 @@
         buffer_str = "VALUE1"
         deserialize_key_value(buffer_str, default_key = "TAG1") == ("TAG1", "VALUE1")
     '''
     if not isinstance(buffer_str, str):
         return default_tuple_result or tuple()
 
     key_value = buffer_str.split(equal_tag, 1)
-    
+
     parsed_key = None
     parsed_value = None
     if len(key_value) < 2:
         if default_key:
             # key_value == (single_item) -> {default_key: single_item}
             key_value = (
                             default_key((key_value[0], None), key_value[0]) if callable(default_key) else default_key,       # parsed_key
@@ -147,15 +147,15 @@
                             key_value[0],
                             default_value((None, key_value[0]), key_value[0]) if callable(default_value) else default_value  # parsed_value
             )
             # Skip more one manipulation with the value, because of it's already default
             parse_value = lambda key_value, default_value: key_value[1]
     parsed_key = parse_key(key_value, (default_key(key_value, key_value[1]) if callable(default_key) else default_key) )
     parsed_value = parse_value(key_value, default_value(key_value, parsed_key) if callable(default_value) else default_value)
-    
+
     return parsed_key, parsed_value
 # ******************************************************************************
 def deserialize_dict(
                         buffer_str: str,
                         delimiter: str = ";",
 # Sample of definition:
 #   parse_item = lambda item, item_index, separated_items, previous_items: item
@@ -174,15 +174,15 @@
         buffer_str = "TAG1=VALUE1;TAG2=VALUE2"
         deserialize_dict(buffer_str) == {"TAG1": "VALUE1", "TAG2": "VALUE2"}
     '''
     deserialized_list = deserialize_list(
                             buffer_str,
                             delimiter,
                             parse_item = parse_item or (
-                                            lambda item, item_index, separated_items, previous_items: 
+                                            lambda item, item_index, separated_items, previous_items:
                                                 deserialize_key_value(
                                                     item,
                                                     equal_tag = equal_tag,
                                                     parse_key = parse_key,
                                                     default_key = default_key,
                                                     parse_value = parse_value,
                                                     default_value = default_value,
@@ -377,8 +377,30 @@
         return return_if_wrong_input
     if value in possible_values_the_last_is_default:
         return value
     if isinstance(raise_if_not_found, Exception):
         raise raise_if_not_found
     return possible_values_the_last_is_default[-1]
 # ******************************************************************************
+def raise_exception(ex: Exception):
+    raise ex
+# ******************************************************************************
+def catch_exception(func: callable, result_in_case_of_exception: typing.Any = None, **kw):
+    """
+    args == tuple, kw == mapping(dictionary)
+
+    * == convert from tuple into list of arguments
+    ** == convert from mapping into list of named arguments
+
+    :param args:
+    :param kw:
+        result:typing.Any => if defined, return {result} in case of no exception
+    """
+    try:
+        result = func()
+        if "result" in kw:
+            result = kw.get("result")
+        return result
+    except:
+        return result_in_case_of_exception
+# ******************************************************************************
 # ******************************************************************************
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_utils_compare.py` & `n0struct-0.2.95/n0struct/n0struct_utils_compare.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,15 +15,15 @@
     global __flag_compare_check_different_types
     return __flag_compare_check_different_types
 # ******************************************************************************
 __flag_compare_return_difference_of_values = False
 def set__flag_compare_return_difference_of_values(value: bool):
     """
     if __flag_compare_return_difference_of_values == True, then
-    if values of attributes are different and are int,float,
+    if values of attributes are different and are int, float,
     return additional element in result["not_equal"] with difference
     """
     global __flag_compare_return_difference_of_values
     __flag_compare_return_difference_of_values = value
 def get__flag_compare_return_difference_of_values() -> bool:
     global __flag_compare_return_difference_of_values
     return __flag_compare_return_difference_of_values
```

### Comparing `n0struct-0.2.94/n0struct/n0struct_utils_find.py` & `n0struct-0.2.95/n0struct/n0struct_utils_find.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,22 +15,22 @@
     node_index_tuple = None
     if '[' in node_name and node_name.endswith(']'):
         node_name, node_index_str = node_name[:-1].split('[', 1)
         node_name = node_name.strip()
         node_index_str = node_index_str.strip()
         if node_index_str:
             if node_index_str.lower().startswith('contains') and node_index_str.endswith(')'):
-                node_index_part1, node_index_part2 = node_index_str[8:-1].strip().split('(',1)[1].split(',',1)
+                node_index_part1, node_index_part2 = node_index_str[8:-1].strip().split('(', 1)[1].split(',', 1)
                 if node_index_part1.lower().startswith('text'):
                     node_index_str = "text()~~" + node_index_part2
             if '=' in node_index_str or '~' in node_index_str:
                 delimiters = ("==","!=","~~","!~","~","=")
                 for delimiter in delimiters:
                     if delimiter in node_index_str:
-                        expected_node_name, expected_value = node_index_str.split(delimiter,1)
+                        expected_node_name, expected_value = node_index_str.split(delimiter, 1)
                         expected_node_name = expected_node_name.strip()
                         expected_value = expected_value.strip()
                         if delimiter == '=':
                             delimiter = '=='
                         if delimiter == '~':
                             delimiter = '~~'
                         break
```

### Comparing `n0struct-0.2.94/n0struct/test/test_n0struct.py` & `n0struct-0.2.95/n0struct/test/test_n0struct.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/test/test_n0struct2.py` & `n0struct-0.2.95/n0struct/test/test_n0struct2.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/test/test_n0struct3.py` & `n0struct-0.2.95/n0struct/test/test_n0struct3.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct/test/test_n0struct4.py` & `n0struct-0.2.95/n0struct/test/test_n0struct4.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/n0struct.egg-info/PKG-INFO` & `n0struct-0.2.95/n0struct.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: n0struct
-Version: 0.2.94
+Version: 0.2.95
 Summary: list/dict extensions allow to load/save/serialize/deserialize xml/json/csv/dsv/fwf files into python/from structures, compare them and work with them using xpath approach
 Home-page: https://github.com/pythonist552/n0struct/
 Author: pythonist552
 Author-email: pythonist552@gmail.com
 License: ASL
 Platform: any
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `n0struct-0.2.94/n0struct.egg-info/SOURCES.txt` & `n0struct-0.2.95/n0struct.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.94/setup.py` & `n0struct-0.2.95/setup.py`

 * *Files identical despite different names*

