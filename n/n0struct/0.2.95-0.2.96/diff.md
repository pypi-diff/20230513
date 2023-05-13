# Comparing `tmp/n0struct-0.2.95.tar.gz` & `tmp/n0struct-0.2.96.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\n0struct-0.2.95.tar", last modified: Sat May 13 11:14:33 2023, max compression
+gzip compressed data, was "dist\n0struct-0.2.96.tar", last modified: Sat May 13 12:24:15 2023, max compression
```

## Comparing `n0struct-0.2.95.tar` & `n0struct-0.2.96.tar`

### file list

```diff
@@ -1,42 +1,42 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 11:14:33.412640 n0struct-0.2.95/
--rw-rw-rw-   0        0        0    11558 2022-09-04 19:16:09.000000 n0struct-0.2.95/LICENSE
--rw-rw-rw-   0        0        0     1060 2023-05-13 11:14:33.413622 n0struct-0.2.95/PKG-INFO
--rw-rw-rw-   0        0        0      590 2022-09-04 19:16:09.000000 n0struct-0.2.95/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 11:14:33.364735 n0struct-0.2.95/n0struct/
--rw-rw-rw-   0        0        0      988 2023-05-13 11:12:54.000000 n0struct-0.2.95/n0struct/__init__.py
--rw-rw-rw-   0        0        0     3671 2023-05-12 12:43:36.000000 n0struct-0.2.95/n0struct/n0struct_arrays.py
--rw-rw-rw-   0        0        0     2647 2023-05-12 12:38:36.000000 n0struct-0.2.95/n0struct/n0struct_comprehensions.py
--rw-rw-rw-   0        0        0    13176 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_date.py
--rw-rw-rw-   0        0        0     3389 2023-05-13 05:52:52.000000 n0struct-0.2.95/n0struct/n0struct_files.py
--rw-rw-rw-   0        0        0    29825 2023-05-13 09:51:04.000000 n0struct-0.2.95/n0struct/n0struct_files_csv.py
--rw-rw-rw-   0        0        0     7180 2023-05-12 12:45:32.000000 n0struct-0.2.95/n0struct/n0struct_files_fwf.py
--rw-rw-rw-   0        0        0    15647 2023-05-12 12:40:01.000000 n0struct-0.2.95/n0struct/n0struct_findall.py
--rw-rw-rw-   0        0        0     4070 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_git.py
--rw-rw-rw-   0        0        0    20938 2023-05-12 12:47:23.000000 n0struct-0.2.95/n0struct/n0struct_logging.py
--rw-rw-rw-   0        0        0     2287 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_mask.py
--rw-rw-rw-   0        0        0    12168 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_n0dict_.py
--rw-rw-rw-   0        0        0    17325 2023-05-12 12:47:58.000000 n0struct-0.2.95/n0struct/n0struct_n0dict__.py
--rw-rw-rw-   0        0        0     7517 2023-05-12 12:41:09.000000 n0struct-0.2.95/n0struct/n0struct_n0list_.py
--rw-rw-rw-   0        0        0    75633 2023-05-13 05:34:23.000000 n0struct-0.2.95/n0struct/n0struct_n0list_n0dict.py
--rw-rw-rw-   0        0        0      917 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_random.py
--rw-rw-rw-   0        0        0     3852 2023-04-25 08:08:57.000000 n0struct-0.2.95/n0struct/n0struct_references.py
--rw-rw-rw-   0        0        0     3235 2023-05-12 12:49:17.000000 n0struct-0.2.95/n0struct/n0struct_transform_structure.py
--rw-rw-rw-   0        0        0    18057 2023-05-12 12:49:39.000000 n0struct-0.2.95/n0struct/n0struct_utils.py
--rw-rw-rw-   0        0        0     6659 2023-05-12 12:42:29.000000 n0struct-0.2.95/n0struct/n0struct_utils_compare.py
--rw-rw-rw-   0        0        0     4120 2023-05-12 12:42:54.000000 n0struct-0.2.95/n0struct/n0struct_utils_find.py
-drwxrwxrwx   0        0        0        0 2023-05-13 11:14:33.412640 n0struct-0.2.95/n0struct/test/
--rw-rw-rw-   0        0        0        0 2022-09-04 19:16:09.000000 n0struct-0.2.95/n0struct/test/__init__.py
--rw-rw-rw-   0        0        0      136 2022-09-04 19:16:09.000000 n0struct-0.2.95/n0struct/test/__main__.py
--rw-rw-rw-   0        0        0    33263 2023-04-23 13:25:25.000000 n0struct-0.2.95/n0struct/test/test_n0struct.py
--rw-rw-rw-   0        0        0     2572 2023-03-06 04:48:48.000000 n0struct-0.2.95/n0struct/test/test_n0struct2.py
--rw-rw-rw-   0        0        0     1177 2023-03-23 03:01:29.000000 n0struct-0.2.95/n0struct/test/test_n0struct3.py
--rw-rw-rw-   0        0        0     1849 2023-04-23 14:00:38.000000 n0struct-0.2.95/n0struct/test/test_n0struct4.py
-drwxrwxrwx   0        0        0        0 2023-05-13 11:14:33.397647 n0struct-0.2.95/n0struct.egg-info/
--rw-rw-rw-   0        0        0     1060 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1032 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       55 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-05-13 11:14:33.000000 n0struct-0.2.95/n0struct.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 11:14:33.414602 n0struct-0.2.95/setup.cfg
--rw-rw-rw-   0        0        0     2476 2023-04-02 07:28:40.000000 n0struct-0.2.95/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:24:15.367426 n0struct-0.2.96/
+-rw-rw-rw-   0        0        0    11558 2022-09-04 19:16:09.000000 n0struct-0.2.96/LICENSE
+-rw-rw-rw-   0        0        0     1060 2023-05-13 12:24:15.368456 n0struct-0.2.96/PKG-INFO
+-rw-rw-rw-   0        0        0      590 2022-09-04 19:16:09.000000 n0struct-0.2.96/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 12:24:15.335914 n0struct-0.2.96/n0struct/
+-rw-rw-rw-   0        0        0      988 2023-05-13 11:12:54.000000 n0struct-0.2.96/n0struct/__init__.py
+-rw-rw-rw-   0        0        0     3671 2023-05-12 12:43:36.000000 n0struct-0.2.96/n0struct/n0struct_arrays.py
+-rw-rw-rw-   0        0        0     2104 2023-05-13 11:27:25.000000 n0struct-0.2.96/n0struct/n0struct_comprehensions.py
+-rw-rw-rw-   0        0        0    13176 2023-04-25 08:08:57.000000 n0struct-0.2.96/n0struct/n0struct_date.py
+-rw-rw-rw-   0        0        0     3389 2023-05-13 05:52:52.000000 n0struct-0.2.96/n0struct/n0struct_files.py
+-rw-rw-rw-   0        0        0    29362 2023-05-13 11:55:07.000000 n0struct-0.2.96/n0struct/n0struct_files_csv.py
+-rw-rw-rw-   0        0        0     7117 2023-05-13 11:56:28.000000 n0struct-0.2.96/n0struct/n0struct_files_fwf.py
+-rw-rw-rw-   0        0        0    15648 2023-05-13 11:36:31.000000 n0struct-0.2.96/n0struct/n0struct_findall.py
+-rw-rw-rw-   0        0        0     4070 2023-04-25 08:08:57.000000 n0struct-0.2.96/n0struct/n0struct_git.py
+-rw-rw-rw-   0        0        0    20873 2023-05-13 12:00:24.000000 n0struct-0.2.96/n0struct/n0struct_logging.py
+-rw-rw-rw-   0        0        0     2287 2023-04-25 08:08:57.000000 n0struct-0.2.96/n0struct/n0struct_mask.py
+-rw-rw-rw-   0        0        0    12168 2023-04-25 08:08:57.000000 n0struct-0.2.96/n0struct/n0struct_n0dict_.py
+-rw-rw-rw-   0        0        0    17116 2023-05-13 12:19:09.000000 n0struct-0.2.96/n0struct/n0struct_n0dict__.py
+-rw-rw-rw-   0        0        0     7519 2023-05-13 11:50:12.000000 n0struct-0.2.96/n0struct/n0struct_n0list_.py
+-rw-rw-rw-   0        0        0    75645 2023-05-13 12:22:04.000000 n0struct-0.2.96/n0struct/n0struct_n0list_n0dict.py
+-rw-rw-rw-   0        0        0      917 2023-04-25 08:08:57.000000 n0struct-0.2.96/n0struct/n0struct_random.py
+-rw-rw-rw-   0        0        0     3852 2023-04-25 08:08:57.000000 n0struct-0.2.96/n0struct/n0struct_references.py
+-rw-rw-rw-   0        0        0     3235 2023-05-12 12:49:17.000000 n0struct-0.2.96/n0struct/n0struct_transform_structure.py
+-rw-rw-rw-   0        0        0    18067 2023-05-13 12:20:41.000000 n0struct-0.2.96/n0struct/n0struct_utils.py
+-rw-rw-rw-   0        0        0     6659 2023-05-12 12:42:29.000000 n0struct-0.2.96/n0struct/n0struct_utils_compare.py
+-rw-rw-rw-   0        0        0     4120 2023-05-12 12:42:54.000000 n0struct-0.2.96/n0struct/n0struct_utils_find.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:24:15.367426 n0struct-0.2.96/n0struct/test/
+-rw-rw-rw-   0        0        0        0 2022-09-04 19:16:09.000000 n0struct-0.2.96/n0struct/test/__init__.py
+-rw-rw-rw-   0        0        0      136 2022-09-04 19:16:09.000000 n0struct-0.2.96/n0struct/test/__main__.py
+-rw-rw-rw-   0        0        0    33051 2023-05-13 12:06:10.000000 n0struct-0.2.96/n0struct/test/test_n0struct.py
+-rw-rw-rw-   0        0        0     2572 2023-03-06 04:48:48.000000 n0struct-0.2.96/n0struct/test/test_n0struct2.py
+-rw-rw-rw-   0        0        0      890 2023-05-13 12:07:38.000000 n0struct-0.2.96/n0struct/test/test_n0struct3.py
+-rw-rw-rw-   0        0        0     1490 2023-05-13 12:23:25.000000 n0struct-0.2.96/n0struct/test/test_n0struct4.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:24:15.360401 n0struct-0.2.96/n0struct.egg-info/
+-rw-rw-rw-   0        0        0     1060 2023-05-13 12:24:15.000000 n0struct-0.2.96/n0struct.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1032 2023-05-13 12:24:15.000000 n0struct-0.2.96/n0struct.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 12:24:15.000000 n0struct-0.2.96/n0struct.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-05-13 12:24:15.000000 n0struct-0.2.96/n0struct.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       55 2023-05-13 12:24:15.000000 n0struct-0.2.96/n0struct.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 12:24:15.000000 n0struct-0.2.96/n0struct.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 12:24:15.378396 n0struct-0.2.96/setup.cfg
+-rw-rw-rw-   0        0        0     2476 2023-04-02 07:28:40.000000 n0struct-0.2.96/setup.py
```

### Comparing `n0struct-0.2.95/LICENSE` & `n0struct-0.2.96/LICENSE`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/PKG-INFO` & `n0struct-0.2.96/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: n0struct
-Version: 0.2.95
+Version: 0.2.96
 Summary: list/dict extensions allow to load/save/serialize/deserialize xml/json/csv/dsv/fwf files into python/from structures, compare them and work with them using xpath approach
 Home-page: https://github.com/pythonist552/n0struct/
 Author: pythonist552
 Author-email: pythonist552@gmail.com
 License: ASL
 Platform: any
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `n0struct-0.2.95/README.md` & `n0struct-0.2.96/README.md`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/__init__.py` & `n0struct-0.2.96/n0struct/__init__.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_arrays.py` & `n0struct-0.2.96/n0struct/n0struct_arrays.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_comprehensions.py` & `n0struct-0.2.96/n0struct/n0struct_comprehensions.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,32 +1,35 @@
 # Python 3.8+ is required. := (walrus operator) is used in comprehension inside load_ini(...)
 import typing
 from .n0struct_utils import isnumber
 from .n0struct_files import load_lines
 # ******************************************************************************
+def default_parse_value(key_value, default_value):
+    stripped_value = key_value[1].strip()
+    if isnumber(stripped_value):
+        if '.' in stripped_value:
+            return round(float(stripped_value), 7)
+        else:
+            return int(stripped_value)
+    else:
+        if len(stripped_value) >=2 and (
+                    ( stripped_value.startswith('"') and stripped_value.endswith('"') )
+                 or ( stripped_value.startswith("'") and stripped_value.endswith("'") )
+        ):
+            return stripped_value[1:-1]
+        else:
+            return stripped_value
+
 def load_ini(
                 file_path: str,
                 default_value = None,
                 equal_tag: str = '=',
                 comment_tags: typing.Union[tuple, list] = ("#", "//"),
                 parse_key: typing.Callable = lambda key_value, default_key: key_value[0].strip().upper(),
-                parse_value: typing.Callable = lambda key_value, default_value:
-                                                        (
-                                                            round(float(stripped_value), 7)
-                                                            if '.' in stripped_value
-                                                            else int(stripped_value)
-                                                        )
-                                                        if isnumber(stripped_value:=key_value[1].strip())
-                                                        else (
-                                                            stripped_value[1:-1]
-                                                            if len(stripped_value) >=2 and (
-                                                                (stripped_value.startswith('"') and stripped_value.endswith('"'))
-                                                                or (stripped_value.startswith("'") and stripped_value.endswith("'"))
-                                                            ) else stripped_value
-                                                        ),
+                parse_value: typing.Callable = default_parse_value,
 ) -> dict:
     """
         load ini file as:
             // Ini file
             KEY1 =VALUE1
             # KEY2=VALUE2
             KEY3= VALUE3
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_date.py` & `n0struct-0.2.96/n0struct/n0struct_date.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_files.py` & `n0struct-0.2.96/n0struct/n0struct_files.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_files_csv.py` & `n0struct-0.2.96/n0struct/n0struct_files_csv.py`

 * *Files 1% similar despite different names*

```diff
@@ -135,22 +135,20 @@
         ## LEGACY
         if header_is_mandatory is None:
             header_is_mandatory = contains_header
         elif isinstance(header_is_mandatory, bool):
             if header_is_mandatory != contains_header:
                 raise SyntaxError(f"{contains_header=} must be equal {header_is_mandatory=} if it's bool")
         contains_header = column_names
-    elif isinstance(contains_header, str):
-        pass
     elif isinstance(contains_header, (list, tuple)):
         if len(contains_header) != len(set(contains_header)):
             raise SyntaxError(f"Column names {contains_header} contains not unique names of columns")
     elif contains_header is None:
         contains_header = column_names
-    else:
+    elif not isinstance(contains_header, str):
         raise SyntaxError(f"Not expectable type of {type(contains_header)} {contains_header=}."
                          " Should be str (first column name) or list/tuple (mandatory column names) or bool (LEGACY) or None"
         )
 
 
     ## process_field
     if not callable(process_field):
@@ -179,17 +177,14 @@
             if not line:
                 raise EOFError("Empty file or file only with spaces")
             header_line = process_line(line.rstrip(EOL))
             if header_line:
                 break
 
         possible_column_names = parse_csv_line(header_line, delimiter, process_field)
-        # n0debug("possible_column_names")
-        # n0debug("contains_header")
-        # n0debug("header_is_mandatory")
 
         first_line_is_header = False
         if contains_header:
             if isinstance(contains_header, str):
                 if possible_column_names[0] != contains_header:
                     if header_is_mandatory:
                         raise ReferenceError(f"First line is not header {possible_column_names}. Expected first column '{contains_header}'")
@@ -201,54 +196,47 @@
                         raise ReferenceError(f"First line is not header {possible_column_names}. Expected {contains_header}")
                 else:
                     first_line_is_header = True
         else:
             if header_is_mandatory and not column_names:
                 first_line_is_header = True
 
-        # n0debug("first_line_is_header")
         if not first_line_is_header:
             in_file.seek(file_offset) # first line is NOT header, re-read first line as data line
             if column_names:
                 possible_column_names = column_names
             else:
                 column_names = possible_column_names = [i for i in range(len(possible_column_names))]
         else:
             if header_is_mandatory and len(possible_column_names) != len(set(possible_column_names)):
                 raise KeyError(f"Read header {possible_column_names} contains not unique names of columns")
             if not column_names:
                 column_names = possible_column_names
         len_possible_column_names = len(possible_column_names)
-        # n0debug("column_names")
-        # n0debug("possible_column_names")
 
         while True:
             line = in_file.readline()  # removed walrus operator for compatibility with 3.7
             if not line:
                 return None  # EOF
             stripped_line = process_line(line.rstrip(EOL))
             if skip_empty_lines and not stripped_line:
                 continue
 
             # removed walrus operator for compatibility with 3.7
             list_field_values = parse_csv_line(stripped_line, delimiter, process_field, EOL)
             dict_field_values = n0dict( zip(
                                     possible_column_names,
                                     list_field_values
-                                    + [None for i in range(len_possible_column_names - len(list_field_values))]
+                                    + ([None] * (len_possible_column_names - len(list_field_values)))
             ))
             if column_names != possible_column_names:
-                # n0debug("column_names")
-                # n0debug("possible_column_names")
                 dict_field_values = n0dict({
                     key: dict_field_values[key]
                     for key in column_names
                 })
-            # n0debug("dict_field_values")
-            # n0debug("return_original_line")
             if return_original_line:
                 yield dict_field_values, stripped_line
             else:
                 yield dict_field_values
 # ******************************************************************************
 load_complex_csv = load_csv  # Synonym
 # ******************************************************************************
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_files_fwf.py` & `n0struct-0.2.96/n0struct/n0struct_files_fwf.py`

 * *Files 2% similar despite different names*

```diff
@@ -116,16 +116,14 @@
     if list_of_items:
         if mapping_dict is None:
             if isinstance(list_of_items[0], list):
                 header = [str(i) for i in range(0, len(list_of_items[0]))]
             elif isinstance(list_of_items[0], dict):
                 header = list(list_of_items[0].keys())
             mapping_dict = {column_name: column_name for column_name in header}
-        else:
-            header = list(mapping_dict.keys())
 
         for found_item in list_of_items:  # found_item == row in case of CSV list or item node in case of XML structure
             if isinstance(found_item, dict):
                 found_item = n0dict(found_item) # to have ability to use .first(xpath)
             elif isinstance(found_item, list):
                 found_item = n0list(found_item) # to have ability to use .first(xpath)
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_findall.py` & `n0struct-0.2.96/n0struct/n0struct_findall.py`

 * *Files 0% similar despite different names*

```diff
@@ -125,15 +125,15 @@
                     equal_condition = False
                     condition_delimiter = '!='
                 elif after_text.startswith('<>'):
                     equal_condition = False
                     condition_delimiter = '<>'
                 else:
                     raise TypeError(f"Unknown logic condition [{child_index}] in '{str(seeked_xpath_list[0])}'")
-                before_condition, after_condition = child_index.split(condition_delimiter, 1)
+                _before_condition, after_condition = child_index.split(condition_delimiter, 1)
                 value_for_condition = after_condition.strip()
                 if len(value_for_condition) > 1 and \
                    (
                        (value_for_condition.startswith('"') and value_for_condition.endswith('"'))
                        or
                        (value_for_condition.startswith("'") and value_for_condition.endswith("'"))
                    ):
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_git.py` & `n0struct-0.2.96/n0struct/n0struct_git.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_logging.py` & `n0struct-0.2.96/n0struct/n0struct_logging.py`

 * *Files 1% similar despite different names*

```diff
@@ -353,26 +353,25 @@
     depends of value in global variable __debug_level.
 
     :param var_object:
     :param var_name:
     :param level:
     :return:
     """
-    ## prefix = (
-    ##             (str(type(var_object)) or "").replace("<class '", "<").replace("'>", ">")
-    ##             if __debug_show_object_type
-    ##             else ""
-    ##          ) + (
-    ##             f" id={id(var_object)}" 
-    ##             if __debug_show_object_id 
-    ##             else ""
-    ##          )
-    ## if prefix:
-    ##     prefix += " "
-    prefix = ""
+    prefix = (
+                (str(type(var_object)) or "").replace("<class '", "<").replace("'>", ">")
+                if __debug_show_object_type
+                else ""
+             ) + (
+                f" id={id(var_object)}"
+                if __debug_show_object_id
+                else ""
+             )
+    if prefix:
+        prefix += " "
 
     n0print(
         f"{prefix}{var_name}{' == ' if prefix or var_name else ''}" +
             n0pretty(
                 var_object,
                 show_type = show_type,
                 pairs_in_one_line = pairs_in_one_line,
@@ -427,21 +426,23 @@
 # ******************************************************************************
 def n0debug_object(object_name: str, level: str = "DEBUG"):
     class_object = inspect.currentframe().f_back.f_locals[object_name]
     class_attribs_methods = set(dir(class_object)) - set(dir(object))
     class_attribs = set()
     class_methods = set()
 
-    prefix = str(type(class_object)) \
-             if __debug_show_object_type \
-             else (
-                 f" id={id(class_object)}"
-                 if __debug_show_object_id
-                 else ""
-             )
+    prefix = (
+        str(type(class_object))
+        if __debug_show_object_type
+        else (
+             f" id={id(class_object)}"
+             if __debug_show_object_id
+             else ""
+        )
+    )
     if prefix:
         prefix = "(" + prefix + ")"
     to_print = f"{prefix}{object_name} == \n"
 
     for attrib_name in class_attribs_methods:
         attrib = getattr(class_object, attrib_name)
         if callable(attrib):
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_mask.py` & `n0struct-0.2.96/n0struct/n0struct_mask.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_n0dict_.py` & `n0struct-0.2.96/n0struct/n0struct_n0dict_.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_n0dict__.py` & `n0struct-0.2.96/n0struct/n0struct_n0dict__.py`

 * *Files 3% similar despite different names*

```diff
@@ -25,15 +25,15 @@
         if not xpath:
             raise IndexError(f"xpath '{xpath}' is not valid")
         if xpath.startswith('?'):
             xpath = xpath[1:]
             raise_exception = False
             if_not_found = ''
         if any(char in xpath for char in "/["):
-            parent_node, node_name_index, cur_value, xpath_found_str, not_found_xpath_list = self._find(xpath, self, return_lists)
+            _parent_node, _node_name_index, cur_value, xpath_found_str, not_found_xpath_list = self._find(xpath, self, return_lists)
             if not not_found_xpath_list:
                 return cur_value
             else:
                 if raise_exception:
                     raise IndexError(f"not found '{'/'.join(not_found_xpath_list)}' in '{xpath_found_str}'")
                 else:
                     return if_not_found
@@ -117,39 +117,38 @@
         """
         if xpath.startswith('?'):
             if new_value is None or (isinstance(new_value, str) and new_value == ""):
                 return None
             xpath = xpath[1:]
 
         if any(char in xpath for char in "/["):
-            parent_node, node_name_index, cur_value, xpath_found_str, not_found_xpath_list = self._find(xpath, self, return_lists = True)
+            parent_node, node_name_index, _cur_value, _xpath_found_str, not_found_xpath_list = self._find(xpath, self, return_lists = True)
             if not_found_xpath_list:
                 parent_node, node_name_index = self._add(parent_node, node_name_index, not_found_xpath_list)
 
             node_name, node_index = split_name_index(node_name_index)
             if isinstance(parent_node, dict):
                 if node_index:
                     raise IndexError(f"How is it possible: index '{node_index}' for dictionary ({type(parent_node)})'{parent_node}'?")
                 parent_node.update({node_name_index: new_value})
             elif isinstance(parent_node, (list, tuple)):
                 if node_name:
                     raise IndexError(f"How is it possible: key '{node_name}' for list ({type(parent_node)})'{parent_node}'?")
-                eval_node_index = n0eval(node_index)
                 parent_node[n0eval(node_index)] = new_value
             else:
                 raise TypeError(f"How is it possible: unknown type of parent node ({type(parent_node)}) of '{parent_node}'")
         else:
             super(n0dict__, self).__setitem__(xpath, new_value)
 
         return new_value  # For speed
     # **************************************************************************
     def delete(self, xpath: str, recursively: bool = False) -> n0dict__:
         xpath_list = xpath.split('/')
         for i, last_xpath_index in enumerate(range(len(xpath_list), 0, -1)):
-            parent_node, node_name_index, cur_value, xpath_found_str, not_found_xpath_list = \
+            parent_node, node_name_index, cur_value, _xpath_found_str, _not_found_xpath_list = \
                 self._find(xpath_list[0:last_xpath_index], self, return_lists=True)
             if i == 0 or (
                 recursively and
                 isinstance(cur_value, n0dict__) and not len(cur_value)
             ):
                 if isinstance(parent_node, list) and not isinstance(node_name_index, int):
                     if not isinstance(node_name_index, str) or not node_name_index.startswith('[') or not node_name_index.endswith(']'):
@@ -212,15 +211,15 @@
             node_value = self.get(node_xpath)
             if callable(validate):
                 validate_result = validate(node_value)
             elif isinstance(validate, (list, tuple)):
                 validate_result = node_value in validate
             else:
                 validate_result = node_value == validate
-        except:
+        except Exception:
             validate_result = False
 
         if validate_result == expected_result_for_error:
             if msg is None:
                 return False
             else:
                 return msg.format(node_xpath, str(node_value))
@@ -270,37 +269,28 @@
             "self_unique":  [],
             "other_unique": [],
         })
         if get__flag_compare_check_different_types():
             validation_results.update({"difftypes": []})
 
         # TO DO: redo with 'in'
-        try:
+        with contextlib.suppress(Exception):
             if self[xpath]:
                 return validation_results
-        except:
-            pass
+
         validation_results["differences"].append(f"[{xpath}] doesn't exist")
         validation_results["other_unique"].append((xpath, None))
         return validation_results
     # **************************************************************************
     # **************************************************************************
     def is_exist(self, xpath: str) -> bool:
         """
         Public function: return True, if self[xpath] exists
         """
         # TO DO: redo with 'in'
-        '''
-        try:
-            if self[xpath]:
-                return True
-        except:
-            pass
-        return False
-        '''
         with contextlib.suppress(Exception):
             if self[xpath]:
                 return True
         return False
     # **************************************************************************
     # **************************************************************************
     def has_all(self, tupple_of_keys: typing.Union[tuple, list]) -> bool:
@@ -320,39 +310,39 @@
     def isEqual(self, xpath, value):
         """
         Public function: return empty lists in dict, if self[xpath] == value
         """
         validation_results = self.isExist(xpath)
         if notemptyitems(validation_results):
             return validation_results
-        try:
+
+        with contextlib.suppress(Exception):
             if self[xpath] == value:
                 return []
-        except:
-            pass
+
         validation_results["differences"].append(f"[{xpath}]=='{self[xpath]}' != '{value}'")
         validation_results["not_equal"].append((xpath, (self[xpath], value)))
         return validation_results
     # **************************************************************************
     # **************************************************************************
     def isTheSame(self, xpath, other_n0dict, other_xpath=None, transformation=lambda x: x):
         """
         Public function: return empty lists in dict, if transformation(self[xpath]) == transformation(other_n0dict[other_xpath])
         """
         if not other_xpath:
             other_xpath = xpath
         validation_results = self.isExist(xpath).update_extend(other_n0dict.isExist(other_xpath))
         if notemptyitems(validation_results):
             return validation_results
-        try:
+
+        with contextlib.suppress(Exception):
             if transformation(self[xpath]) == transformation(other_n0dict[other_xpath]):
                 return validation_results
-        except:
-            # n0print("EXCEPTION in 'if transformation(self[xpath]) == transformation(other_n0dict[other_xpath]):'")
-            pass
+        ## n0print("EXCEPTION in 'if transformation(self[xpath]) == (other_n0dict[other_xpath]):'")
+
         validation_results["differences"].append(
             f"[{xpath}]=='{transformation(self[xpath])}' != [{other_xpath}]=='{transformation(other_n0dict[other_xpath])}'"
         )
         validation_results["not_equal"].append((xpath, (self[xpath], other_n0dict[other_xpath])))
         return validation_results
 # ******************************************************************************
 # ******************************************************************************
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_n0list_.py` & `n0struct-0.2.96/n0struct/n0struct_n0list_.py`

 * *Files 1% similar despite different names*

```diff
@@ -31,15 +31,15 @@
             return if_not_found
 
         if xpath.startswith('?'):
             xpath = xpath[1:]
             raise_exception = False
             if_not_found = ''
         if any(char in xpath for char in "/["):
-            parent_node, node_name_index, cur_value, xpath_found_str, not_found_xpath_list = self._find(xpath, self, return_lists)
+            _parent_node, _node_name_index, cur_value, xpath_found_str, not_found_xpath_list = self._find(xpath, self, return_lists)
             if not not_found_xpath_list:
                 return cur_value
             else:
                 if raise_exception:
                     raise IndexError(f"not found '{'/'.join(not_found_xpath_list)}' in '{xpath_found_str}'")
                 else:
                     return if_not_found
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_n0list_n0dict.py` & `n0struct-0.2.96/n0struct/n0struct_n0list_n0dict.py`

 * *Files 0% similar despite different names*

```diff
@@ -142,15 +142,15 @@
                 if fst_found_xpath_str:
                     return fst_parent_node, fst_node_name_index, cur_values, fst_found_xpath_str,   None
                 else:
                     return parent_node,     None,                None,       xpath_found_str,        xpath_list
             else:
                 try:
                     node_index_int = n0eval(node_index_str)
-                except:
+                except Exception:
                     raise IndexError(f"Unknown index '{xpath_found_str}[{node_index_str}]'")
 
                 if isinstance(parent_node, (list, tuple)):
                     len__parent_node = len(parent_node)
                 else:
                     len__parent_node = 1
                     parent_node = [parent_node]
@@ -1098,15 +1098,15 @@
         # ##########################################################################################
         else:
             #--------------------------------
             # NOT FOUND: new element in n0list
             #--------------------------------
             if node_index == "new()":
                 parent_node, node_name_index, cur_value, xpath_found_str, \
-                    not_found_xpath_list = self._find(xpath_found_str, self, return_lists)
+                    _not_found_xpath_list = self._find(xpath_found_str, self, return_lists)
                 if not isinstance(parent_node[node_name_index], (list, tuple)):
                     parent_node[node_name_index] = n0list([parent_node[node_name_index]])
                 return parent_node[node_name_index], None, None, xpath_found_str, ["[new()]"] + xpath_list[1:]
             # ..................................................................
             # Try to check all [*] items in the loop
             # ..................................................................
             elif node_index == "*":
@@ -1275,15 +1275,15 @@
                 next_node_name_index = "[last()]"
         else:
             ####################################################################
             # Parent is LIST or should be a list
             ####################################################################
             # Original code
             if cur_node_index == "new()":
-            # FIXME
+            # FIX ME
             # or (isinstance(parent_node, (list, tuple)) and n0eval(cur_node_index) == len(parent_node)) \
             # or (isinstance(parent_node[cur_node_name], (list, tuple)) and n0eval(cur_node_index) == len(parent_node)[cur_node_name]):
                 if cur_node_name and not isinstance(parent_node[cur_node_name], (list, tuple, n0list)):
                     ####################################################################
                     # Convert not LIST into the list
                     ####################################################################
                     if len(parent_node[cur_node_name]):
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_random.py` & `n0struct-0.2.96/n0struct/n0struct_random.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_references.py` & `n0struct-0.2.96/n0struct/n0struct_references.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_transform_structure.py` & `n0struct-0.2.96/n0struct/n0struct_transform_structure.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_utils.py` & `n0struct-0.2.96/n0struct/n0struct_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -396,11 +396,11 @@
         result:typing.Any => if defined, return {result} in case of no exception
     """
     try:
         result = func()
         if "result" in kw:
             result = kw.get("result")
         return result
-    except:
+    except Exception:
         return result_in_case_of_exception
 # ******************************************************************************
 # ******************************************************************************
```

### Comparing `n0struct-0.2.95/n0struct/n0struct_utils_compare.py` & `n0struct-0.2.96/n0struct/n0struct_utils_compare.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/n0struct_utils_find.py` & `n0struct-0.2.96/n0struct/n0struct_utils_find.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/test/test_n0struct.py` & `n0struct-0.2.96/n0struct/test/test_n0struct.py`

 * *Files 1% similar despite different names*

```diff
@@ -78,16 +78,14 @@
     assert notemptyitems(differences1_direct_compare["difftypes"])          == 0
     assert notemptyitems(differences1_direct_compare["other_unique"])       == 0
     assert notemptyitems(differences1_direct_compare["self_unique"])        == 0
 
     n0print("="*80)
     n0debug("differences2_wise_compare")
     assert differences1_direct_compare["differences"]  == differences2_wise_compare["differences"]
-    # n0debug_calc(differences1_direct_compare["not_equal"],  'differences1_direct_compare["not_equal"]')
-    # n0debug_calc(differences2_wise_compare["not_equal"],    'differences2_wise_compare["not_equal"]')
     assert differences1_direct_compare["not_equal"]    == differences2_wise_compare["not_equal"]
     assert differences1_direct_compare["difftypes"]    == differences2_wise_compare["difftypes"]
     assert differences1_direct_compare["other_unique"] == differences2_wise_compare["other_unique"]
     assert differences1_direct_compare["self_unique"]  == differences2_wise_compare["self_unique"]
 # ******************************************************************************
 def test_unsorted_lists():
     n0print("*"*80 + " 3 = Unsorted list in dictionary = direct_compare")
```

### Comparing `n0struct-0.2.95/n0struct/test/test_n0struct2.py` & `n0struct-0.2.96/n0struct/test/test_n0struct2.py`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/n0struct/test/test_n0struct4.py` & `n0struct-0.2.96/n0struct/test/test_n0struct4.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,30 +1,18 @@
 import os
 import sys
 mydir = os.path.dirname(os.path.realpath(__file__))
 sys.path.insert(0, mydir)
 sys.path.insert(0, mydir+"/../")
 sys.path.insert(0, mydir+"/../../")
-from n0struct import *
-# from n0struct import (
-    # n0print,
-    # n0debug,
-    # # n0debug_calc,
-    # # set__flag_compare_check_different_types,
-    # # set__flag_compare_return_difference_of_values,
-    # # init_logger,
-    
-    # # deserialize_list,
-    # # deserialize_fixed_list,
-    # # deserialize_dict,
-    # # get_value_by_tag,
-    # # deserialize_list_of_lists,
-    # load_ini,
-    # save_file,
-# )
+from n0struct import (
+    n0dict,
+    n0print,
+    n0debug,
+)
 
 # ******************************************************************************
 dict1 = n0dict({
     "C": [
         {"a": 1, "b": 2, "c": 3, "value1": 1, "value2": 4},
         {"a": 4, "b": 5, "c": 6, "value1": 2, "value2": 5},
         {"a": 7, "b": 8, "c": 9, "value1": 3, "value2": 6},
```

### Comparing `n0struct-0.2.95/n0struct.egg-info/PKG-INFO` & `n0struct-0.2.96/n0struct.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: n0struct
-Version: 0.2.95
+Version: 0.2.96
 Summary: list/dict extensions allow to load/save/serialize/deserialize xml/json/csv/dsv/fwf files into python/from structures, compare them and work with them using xpath approach
 Home-page: https://github.com/pythonist552/n0struct/
 Author: pythonist552
 Author-email: pythonist552@gmail.com
 License: ASL
 Platform: any
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `n0struct-0.2.95/n0struct.egg-info/SOURCES.txt` & `n0struct-0.2.96/n0struct.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `n0struct-0.2.95/setup.py` & `n0struct-0.2.96/setup.py`

 * *Files identical despite different names*

