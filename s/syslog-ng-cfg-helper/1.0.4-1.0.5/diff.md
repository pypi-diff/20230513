# Comparing `tmp/syslog_ng_cfg_helper-1.0.4.tar.gz` & `tmp/syslog_ng_cfg_helper-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "syslog_ng_cfg_helper-1.0.4.tar", max compression
+gzip compressed data, was "syslog_ng_cfg_helper-1.0.5.tar", max compression
```

## Comparing `syslog_ng_cfg_helper-1.0.4.tar` & `syslog_ng_cfg_helper-1.0.5.tar`

### file list

```diff
@@ -1,29 +1,29 @@
--rw-r--r--   0        0        0    35148 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/LICENSE
--rw-r--r--   0        0        0     2869 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/README.md
--rw-r--r--   0        0        0     1147 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/__init__.py
--rw-r--r--   0        0        0      941 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/build_db.py
--rw-r--r--   0        0        0     2486 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/console.py
--rw-r--r--   0        0        0      244 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__init__.py
--rw-r--r--   0        0        0      535 2023-05-13 20:59:06.978325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0     8160 2023-05-13 20:59:06.986325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc
--rw-r--r--   0        0        0     4579 2023-05-13 20:59:06.982325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc
--rw-r--r--   0        0        0     5314 2023-05-13 20:59:06.982325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc
--rw-r--r--   0        0        0      439 2023-05-13 20:59:06.982325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/exceptions.cpython-311.pyc
--rw-r--r--   0        0        0     5440 2023-05-13 20:59:06.986325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc
--rw-r--r--   0        0        0     1331 2023-05-13 20:59:06.986325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc
--rw-r--r--   0        0        0     3783 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/block.py
--rw-r--r--   0        0        0     1769 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/driver.py
--rw-r--r--   0        0        0     2263 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/driver_db.py
--rw-r--r--   0        0        0       42 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/exceptions.py
--rw-r--r--   0        0        0     2249 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/option.py
--rw-r--r--   0        0        0      479 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/utils.py
--rw-r--r--   0        0        0      893 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/globals.py
--rw-r--r--   0        0        0       75 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__init__.py
--rw-r--r--   0        0        0      281 2023-05-13 20:59:06.518324 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0    11313 2023-05-13 20:59:06.522324 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc
--rw-r--r--   0        0        0     7404 2023-05-13 20:59:06.986325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc
--rw-r--r--   0        0        0     6094 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/load_modules.py
--rw-r--r--   0        0        0     4225 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/parse_sentence.py
--rw-r--r--   0        0        0   215603 2023-05-13 20:59:17.870350 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db
--rw-r--r--   0        0        0     3811 1970-01-01 00:00:00.000000 syslog_ng_cfg_helper-1.0.4/PKG-INFO
+-rw-r--r--   0        0        0    35148 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/LICENSE
+-rw-r--r--   0        0        0     2869 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/README.md
+-rw-r--r--   0        0        0     1147 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/__init__.py
+-rw-r--r--   0        0        0      941 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/build_db.py
+-rw-r--r--   0        0        0     2486 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/console.py
+-rw-r--r--   0        0        0      244 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__init__.py
+-rw-r--r--   0        0        0      535 2023-05-13 21:14:11.276717 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0     8160 2023-05-13 21:14:11.280717 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc
+-rw-r--r--   0        0        0     4579 2023-05-13 21:14:11.280717 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc
+-rw-r--r--   0        0        0     5314 2023-05-13 21:14:11.276717 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc
+-rw-r--r--   0        0        0      439 2023-05-13 21:14:11.280717 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/exceptions.cpython-311.pyc
+-rw-r--r--   0        0        0     5440 2023-05-13 21:14:11.284717 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc
+-rw-r--r--   0        0        0     1331 2023-05-13 21:14:11.284717 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc
+-rw-r--r--   0        0        0     3783 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/block.py
+-rw-r--r--   0        0        0     1769 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/driver.py
+-rw-r--r--   0        0        0     2263 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/driver_db.py
+-rw-r--r--   0        0        0       42 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/exceptions.py
+-rw-r--r--   0        0        0     2249 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/option.py
+-rw-r--r--   0        0        0      479 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/utils.py
+-rw-r--r--   0        0        0      893 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/globals.py
+-rw-r--r--   0        0        0       75 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/__init__.py
+-rw-r--r--   0        0        0      281 2023-05-13 21:14:10.712711 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0    11313 2023-05-13 21:14:10.716711 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc
+-rw-r--r--   0        0        0     7404 2023-05-13 21:14:11.284717 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc
+-rw-r--r--   0        0        0     6094 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/load_modules.py
+-rw-r--r--   0        0        0     4225 2023-05-13 21:12:48.335766 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/parse_sentence.py
+-rw-r--r--   0        0        0   215603 2023-05-13 21:14:25.952865 syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db
+-rw-r--r--   0        0        0     3811 1970-01-01 00:00:00.000000 syslog_ng_cfg_helper-1.0.5/PKG-INFO
```

### Comparing `syslog_ng_cfg_helper-1.0.4/LICENSE` & `syslog_ng_cfg_helper-1.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/README.md` & `syslog_ng_cfg_helper-1.0.5/README.md`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/pyproject.toml` & `syslog_ng_cfg_helper-1.0.5/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "syslog-ng-cfg-helper"
-version = "1.0.4"
+version = "1.0.5"
 description = "Configuration helper for syslog-ng."
 authors = ["Attila Szakacs <szakacs.attila96@gmail.com>"]
 readme = "README.md"
 license = "GPL-3.0-only"
 homepage = "https://github.com/alltilla/syslog-ng-cfg-helper"
 repository = "https://github.com/alltilla/syslog-ng-cfg-helper"
 keywords = ["syslog-ng", "configuration", "cfg"]
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/build_db.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/build_db.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/console.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/console.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc`

 * *Files 20% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
+moddate:  0x50fd5f64 (Sat May 13 21:12:48 2023 UTC)
 files sz: 244
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 2
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
+moddate:  0x50fd5f64 (Sat May 13 21:12:48 2023 UTC)
 files sz: 3783
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
+moddate:  0x50fd5f64 (Sat May 13 21:12:48 2023 UTC)
 files sz: 1769
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 5
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
+moddate:  0x50fd5f64 (Sat May 13 21:12:48 2023 UTC)
 files sz: 2263
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
+moddate:  0x50fd5f64 (Sat May 13 21:12:48 2023 UTC)
 files sz: 2249
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
+moddate:  0x50fd5f64 (Sat May 13 21:12:48 2023 UTC)
 files sz: 479
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/block.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/block.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/driver.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/driver.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/driver_db.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/driver_db.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/option.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/driver_db/option.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/globals.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/globals.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
+moddate:  0x50fd5f64 (Sat May 13 21:12:48 2023 UTC)
 files sz: 6094
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 8
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
+moddate:  0x50fd5f64 (Sat May 13 21:12:48 2023 UTC)
 files sz: 4225
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 8
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/load_modules.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/load_modules.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/parse_sentence.py` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/module_loader/parse_sentence.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db` & `syslog_ng_cfg_helper-1.0.5/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db`

 * *Files 1% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9999642426568853%*

 * *Differences: {"'contexts'": "{'parser': {'csv-parser': {'blocks': {'delimiters': {'options': {'': {'params': "*

 * *               "{insert: [(1, ['<string>'])], delete: [0]}}}}}, 'options': {'flags': {'params': "*

 * *               "{insert: [(2, ['<string>'])], delete: [0]}}}}, 'syslog-parser': {'options': "*

 * *               "{'flags': {'params': {insert: [(0, ['check-hostname'])], delete: [2]}}, "*

 * *               "'default-facility': {'params': {insert: [(1, ['KW_SYSLOG'])], delete: [0]}}}}, "*

 * *               "'python': {'blocks' […]*

```diff
@@ -360,31 +360,31 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ],
                                     [
-                                        "<empty>"
+                                        "<string>"
                                     ]
                                 ]
                             }
                         }
                     }
                 },
                 "context": "destination",
@@ -964,51 +964,51 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -1032,18 +1032,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -1102,18 +1102,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pad-size": {
                         "name": "pad-size",
                         "params": [
                             [
@@ -1121,18 +1121,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -1379,51 +1379,51 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -1455,18 +1455,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -1541,18 +1541,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pad-size": {
                         "name": "pad-size",
                         "params": [
                             [
@@ -1560,18 +1560,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -1745,18 +1745,18 @@
                         "blocks": {},
                         "name": "cipher-suite",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ],
                                     [
-                                        "<empty>"
+                                        "<string>"
                                     ]
                                 ]
                             },
                             "tls12-and-older": {
                                 "name": "tls12-and-older",
                                 "params": [
                                     [
@@ -1915,43 +1915,43 @@
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "[",
-                                                "<string-list>",
-                                                "]"
+                                                "<python-yesno>"
+                                            ],
+                                            [
+                                                "<empty>"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<float>"
+                                                "[",
+                                                "<string-list>",
+                                                "]"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<number>"
+                                                "<float>"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<python-yesno>"
+                                                "<string>"
                                             ],
                                             [
                                                 "<string>"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<string>"
-                                            ],
-                                            [
-                                                "<empty>"
+                                                "<number>"
                                             ]
                                         ]
                                     },
                                     "LogTemplate": {
                                         "name": "LogTemplate",
                                         "params": [
                                             [
@@ -2322,35 +2322,35 @@
                             ]
                         ]
                     },
                     "response-action": {
                         "name": "response-action",
                         "params": [
                             [
-                                "<positive-integer>",
-                                "=>",
-                                "retry"
+                                "<empty>"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
                                 "disconnect"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
                                 "drop"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
-                                "success"
+                                "retry"
                             ],
                             [
-                                "<empty>"
+                                "<positive-integer>",
+                                "=>",
+                                "success"
                             ]
                         ]
                     },
                     "retries": {
                         "name": "retries",
                         "params": [
                             [
@@ -2653,37 +2653,37 @@
                             ]
                         ]
                     },
                     "option": {
                         "name": "option",
                         "params": [
                             [
-                                "<empty>"
-                            ],
-                            [
                                 "<string>",
                                 "=>",
                                 "<string-or-number>"
                             ],
                             [
                                 "<string>",
                                 "<string-or-number>"
+                            ],
+                            [
+                                "<empty>"
                             ]
                         ]
                     },
                     "options": {
                         "name": "options",
                         "params": [
                             [
                                 "<string>",
+                                "=>",
                                 "<string-or-number>"
                             ],
                             [
                                 "<string>",
-                                "=>",
                                 "<string-or-number>"
                             ],
                             [
                                 "<empty>"
                             ]
                         ]
                     },
@@ -2760,19 +2760,19 @@
                         "name": "config",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
                                         "<string>",
+                                        "=>",
                                         "<string-or-number>"
                                     ],
                                     [
                                         "<string>",
-                                        "=>",
                                         "<string-or-number>"
                                     ],
                                     [
                                         "<empty>"
                                     ]
                                 ]
                             },
@@ -3416,31 +3416,31 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ],
                                     [
-                                        "<empty>"
+                                        "<string>"
                                     ]
                                 ]
                             }
                         }
                     }
                 },
                 "context": "destination",
@@ -4752,21 +4752,21 @@
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
                                 "udp"
                             ],
                             [
-                                "tcp"
+                                "<string>"
                             ],
                             [
-                                "tls"
+                                "tcp"
                             ],
                             [
-                                "<string>"
+                                "tls"
                             ]
                         ]
                     },
                     "truncate-size": {
                         "name": "truncate-size",
                         "params": [
                             [
@@ -4925,51 +4925,51 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -4993,18 +4993,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -5063,18 +5063,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pad-size": {
                         "name": "pad-size",
                         "params": [
                             [
@@ -5082,18 +5082,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -5332,18 +5332,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -5906,43 +5906,43 @@
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
                                         "<string>",
                                         "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<python-yesno>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<float>"
+                                        "[",
+                                        "<string-list>",
+                                        "]"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<string>"
                                     ],
                                     [
                                         "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
+                                        "<number>"
                                     ]
                                 ]
                             },
                             "LogTemplate": {
                                 "name": "LogTemplate",
                                 "params": [
                                     [
@@ -6144,31 +6144,31 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ],
                                     [
-                                        "<empty>"
+                                        "<string>"
                                     ]
                                 ]
                             }
                         }
                     }
                 },
                 "context": "destination",
@@ -6805,31 +6805,31 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ],
                                     [
-                                        "<empty>"
+                                        "<string>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "disk-buffer": {
                         "blocks": {},
@@ -7102,23 +7102,23 @@
                             ]
                         ]
                     },
                     "event-time": {
                         "name": "event-time",
                         "params": [
                             [
-                                "<template-content>"
+                                "<template-content>",
+                                "microseconds"
                             ],
                             [
                                 "<template-content>",
                                 "seconds"
                             ],
                             [
-                                "<template-content>",
-                                "microseconds"
+                                "<template-content>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -7421,18 +7421,18 @@
                 "context": "destination",
                 "name": "smtp",
                 "options": {
                     "bcc": {
                         "name": "bcc",
                         "params": [
                             [
+                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
-                                "<template-content>",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "body": {
                         "name": "body",
                         "params": [
@@ -7441,18 +7441,18 @@
                             ]
                         ]
                     },
                     "cc": {
                         "name": "cc",
                         "params": [
                             [
+                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
-                                "<template-content>",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "frac-digits": {
                         "name": "frac-digits",
                         "params": [
@@ -7461,18 +7461,18 @@
                             ]
                         ]
                     },
                     "from": {
                         "name": "from",
                         "params": [
                             [
+                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
-                                "<template-content>",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "header": {
                         "name": "header",
                         "params": [
@@ -7538,18 +7538,18 @@
                             ]
                         ]
                     },
                     "reply-to": {
                         "name": "reply-to",
                         "params": [
                             [
+                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
-                                "<template-content>",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "retries": {
                         "name": "retries",
                         "params": [
@@ -7566,18 +7566,18 @@
                             ]
                         ]
                     },
                     "sender": {
                         "name": "sender",
                         "params": [
                             [
+                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
-                                "<template-content>",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "subject": {
                         "name": "subject",
                         "params": [
@@ -7610,18 +7610,18 @@
                             ]
                         ]
                     },
                     "to": {
                         "name": "to",
                         "params": [
                             [
+                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
-                                "<template-content>",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "ts-format": {
                         "name": "ts-format",
                         "params": [
@@ -8085,18 +8085,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -8296,21 +8296,21 @@
                             ]
                         ]
                     },
                     "values": {
                         "name": "values",
                         "params": [
                             [
-                                "default"
+                                "<empty>"
                             ],
                             [
-                                "<template-content>"
+                                "default"
                             ],
                             [
-                                "<empty>"
+                                "<template-content>"
                             ]
                         ]
                     }
                 }
             },
             "stomp": {
                 "blocks": {
@@ -8625,19 +8625,19 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
@@ -8989,18 +8989,18 @@
                                 "blocks": {},
                                 "name": "cipher-suite",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<empty>"
                                             ],
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ]
                                         ]
                                     },
                                     "tls12-and-older": {
                                         "name": "tls12-and-older",
                                         "params": [
                                             [
@@ -9249,18 +9249,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -9602,21 +9602,21 @@
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
                                 "udp"
                             ],
                             [
-                                "tls"
+                                "<string>"
                             ],
                             [
                                 "tcp"
                             ],
                             [
-                                "<string>"
+                                "tls"
                             ]
                         ]
                     },
                     "truncate-size": {
                         "name": "truncate-size",
                         "params": [
                             [
@@ -10066,18 +10066,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -12451,18 +12451,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -13351,18 +13351,18 @@
                         "blocks": {},
                         "name": "delimiters",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ],
                                     [
-                                        "<empty>"
+                                        "<string>"
                                     ]
                                 ]
                             },
                             "chars": {
                                 "name": "chars",
                                 "params": [
                                     [
@@ -13408,21 +13408,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "drop-invalid"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -13477,18 +13477,18 @@
                 "context": "parser",
                 "name": "date-parser",
                 "options": {
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -14274,19 +14274,19 @@
                         ]
                     },
                     "pair": {
                         "name": "pair",
                         "params": [
                             [
                                 "<string>",
-                                ":",
                                 "<template-content>"
                             ],
                             [
                                 "<string>",
+                                ":",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "scope": {
                         "name": "scope",
                         "params": [
@@ -14416,43 +14416,43 @@
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
                                         "<string>",
                                         "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<python-yesno>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<float>"
+                                        "[",
+                                        "<string-list>",
+                                        "]"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<string>"
                                     ],
                                     [
                                         "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
+                                        "<number>"
                                     ]
                                 ]
                             },
                             "LogTemplate": {
                                 "name": "LogTemplate",
                                 "params": [
                                     [
@@ -14641,18 +14641,18 @@
                 "context": "parser",
                 "name": "syslog-parser",
                 "options": {
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -14684,21 +14684,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "check-hostname"
+                                "<string>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -14987,18 +14987,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -15049,18 +15049,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -15188,18 +15188,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -15428,18 +15428,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -15558,18 +15558,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -15601,18 +15601,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -15620,18 +15620,18 @@
                             ]
                         ]
                     },
                     "freq": {
                         "name": "freq",
                         "params": [
                             [
-                                "<positive-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<positive-integer>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
                         "params": [
                             [
@@ -15751,18 +15751,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -15884,18 +15884,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -15919,40 +15919,40 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -15968,21 +15968,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -15990,18 +15990,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
                         "params": [
                             [
@@ -16121,18 +16121,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pad-size": {
                         "name": "pad-size",
                         "params": [
                             [
@@ -16140,18 +16140,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -16207,18 +16207,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -16332,18 +16332,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -16367,40 +16367,40 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -16416,18 +16416,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
                                 "<string>"
                             ]
                         ]
                     },
                     "follow-freq": {
@@ -16457,18 +16457,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
                         "params": [
                             [
@@ -16588,18 +16588,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pad-size": {
                         "name": "pad-size",
                         "params": [
                             [
@@ -16607,18 +16607,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -16682,18 +16682,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -16911,18 +16911,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -17125,18 +17125,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -17236,18 +17236,18 @@
                                 "blocks": {},
                                 "name": "cipher-suite",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<empty>"
                                             ],
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ]
                                         ]
                                     },
                                     "tls12-and-older": {
                                         "name": "tls12-and-older",
                                         "params": [
                                             [
@@ -17450,18 +17450,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -17528,21 +17528,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "check-hostname"
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -17857,21 +17857,21 @@
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
                                 "udp"
                             ],
                             [
-                                "tcp"
+                                "<string>"
                             ],
                             [
-                                "tls"
+                                "tcp"
                             ],
                             [
-                                "<string>"
+                                "tls"
                             ]
                         ]
                     },
                     "trim-large-messages": {
                         "name": "trim-large-messages",
                         "params": [
                             [
@@ -17879,18 +17879,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -18102,18 +18102,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -18137,40 +18137,40 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -18186,21 +18186,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -18208,18 +18208,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
                         "params": [
                             [
@@ -18339,18 +18339,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pad-size": {
                         "name": "pad-size",
                         "params": [
                             [
@@ -18358,18 +18358,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -18425,18 +18425,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -18550,18 +18550,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -18601,21 +18601,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -18767,18 +18767,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -18870,43 +18870,43 @@
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
                                         "<string>",
                                         "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<python-yesno>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<float>"
+                                        "[",
+                                        "<string-list>",
+                                        "]"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<string>"
                                     ],
                                     [
                                         "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
+                                        "<number>"
                                     ]
                                 ]
                             },
                             "LogTemplate": {
                                 "name": "LogTemplate",
                                 "params": [
                                     [
@@ -18936,18 +18936,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -19118,18 +19118,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -19221,43 +19221,43 @@
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
                                         "<string>",
                                         "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<python-yesno>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<float>"
+                                        "[",
+                                        "<string-list>",
+                                        "]"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<string>"
                                     ],
                                     [
                                         "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
+                                        "<number>"
                                     ]
                                 ]
                             },
                             "LogTemplate": {
                                 "name": "LogTemplate",
                                 "params": [
                                     [
@@ -19287,18 +19287,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -19488,18 +19488,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -19605,18 +19605,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -19640,40 +19640,40 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -19689,21 +19689,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "follow-freq": {
                         "name": "follow-freq",
                         "params": [
                             [
@@ -19730,18 +19730,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
                         "params": [
                             [
@@ -19861,18 +19861,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pad-size": {
                         "name": "pad-size",
                         "params": [
                             [
@@ -19880,18 +19880,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -19955,18 +19955,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -20484,18 +20484,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -20562,21 +20562,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -20891,21 +20891,21 @@
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
                                 "udp"
                             ],
                             [
-                                "tcp"
+                                "<string>"
                             ],
                             [
-                                "tls"
+                                "tcp"
                             ],
                             [
-                                "<string>"
+                                "tls"
                             ]
                         ]
                     },
                     "trim-large-messages": {
                         "name": "trim-large-messages",
                         "params": [
                             [
@@ -20913,18 +20913,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -21022,18 +21022,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -21222,18 +21222,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -21339,18 +21339,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -21390,21 +21390,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "check-hostname"
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -21604,18 +21604,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -21707,18 +21707,18 @@
                                 "blocks": {},
                                 "name": "cipher-suite",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<empty>"
                                             ],
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ]
                                         ]
                                     },
                                     "tls12-and-older": {
                                         "name": "tls12-and-older",
                                         "params": [
                                             [
@@ -21921,18 +21921,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -21999,21 +21999,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -22325,18 +22325,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -22428,18 +22428,18 @@
                                 "blocks": {},
                                 "name": "cipher-suite",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<empty>"
                                             ],
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ]
                                         ]
                                     },
                                     "tls12-and-older": {
                                         "name": "tls12-and-older",
                                         "params": [
                                             [
@@ -22642,18 +22642,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -22720,21 +22720,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "check-hostname"
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -23046,18 +23046,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -23163,18 +23163,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -23214,18 +23214,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
                                 "<string>"
                             ]
                         ]
                     },
                     "format": {
@@ -23516,18 +23516,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -23633,18 +23633,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -23684,21 +23684,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ],
                             [
-                                "check-hostname"
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -23986,18 +23986,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -24119,18 +24119,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -24154,40 +24154,40 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -24230,21 +24230,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -24252,18 +24252,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
                         "params": [
                             [
@@ -24383,18 +24383,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pass-unix-credentials": {
                         "name": "pass-unix-credentials",
                         "params": [
                             [
@@ -24402,18 +24402,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -24533,18 +24533,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -24666,18 +24666,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "syslog"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "syslog"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -24701,40 +24701,40 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -24777,21 +24777,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -24799,18 +24799,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
                         "params": [
                             [
@@ -24930,18 +24930,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pass-unix-credentials": {
                         "name": "pass-unix-credentials",
                         "params": [
                             [
@@ -24949,18 +24949,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -25080,18 +25080,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -25205,18 +25205,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -25240,40 +25240,40 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -25297,21 +25297,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "check-hostname"
                             ],
                             [
                                 "<empty>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "follow-freq": {
                         "name": "follow-freq",
                         "params": [
                             [
@@ -25330,18 +25330,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
                         "params": [
                             [
@@ -25477,18 +25477,18 @@
                             ]
                         ]
                     },
                     "owner": {
                         "name": "owner",
                         "params": [
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ]
                         ]
                     },
                     "pad-size": {
                         "name": "pad-size",
                         "params": [
                             [
@@ -25496,18 +25496,18 @@
                             ]
                         ]
                     },
                     "perm": {
                         "name": "perm",
                         "params": [
                             [
-                                "<number>"
+                                "<empty>"
                             ],
                             [
-                                "<empty>"
+                                "<number>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -25571,18 +25571,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "persist-only"
+                                "<yesno>"
                             ],
                             [
-                                "<yesno>"
+                                "persist-only"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
```

### Comparing `syslog_ng_cfg_helper-1.0.4/PKG-INFO` & `syslog_ng_cfg_helper-1.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: syslog-ng-cfg-helper
-Version: 1.0.4
+Version: 1.0.5
 Summary: Configuration helper for syslog-ng.
 Home-page: https://github.com/alltilla/syslog-ng-cfg-helper
 License: GPL-3.0-only
 Keywords: syslog-ng,configuration,cfg
 Author: Attila Szakacs
 Author-email: szakacs.attila96@gmail.com
 Requires-Python: >=3.8,<4.0
```

