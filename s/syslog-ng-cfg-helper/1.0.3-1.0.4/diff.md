# Comparing `tmp/syslog_ng_cfg_helper-1.0.3.tar.gz` & `tmp/syslog_ng_cfg_helper-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "syslog_ng_cfg_helper-1.0.3.tar", max compression
+gzip compressed data, was "syslog_ng_cfg_helper-1.0.4.tar", max compression
```

## Comparing `syslog_ng_cfg_helper-1.0.3.tar` & `syslog_ng_cfg_helper-1.0.4.tar`

### file list

```diff
@@ -1,29 +1,29 @@
--rw-r--r--   0        0        0    35148 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/LICENSE
--rw-r--r--   0        0        0     2869 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/README.md
--rw-r--r--   0        0        0     1147 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/__init__.py
--rw-r--r--   0        0        0      941 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/build_db.py
--rw-r--r--   0        0        0     2486 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/console.py
--rw-r--r--   0        0        0      244 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__init__.py
--rw-r--r--   0        0        0      535 2023-05-13 20:54:49.110200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0     8160 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc
--rw-r--r--   0        0        0     4579 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc
--rw-r--r--   0        0        0     5314 2023-05-13 20:54:49.110200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc
--rw-r--r--   0        0        0      439 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/exceptions.cpython-311.pyc
--rw-r--r--   0        0        0     5440 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc
--rw-r--r--   0        0        0     1331 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc
--rw-r--r--   0        0        0     3783 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/block.py
--rw-r--r--   0        0        0     1769 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/driver.py
--rw-r--r--   0        0        0     2263 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/driver_db.py
--rw-r--r--   0        0        0       42 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/exceptions.py
--rw-r--r--   0        0        0     2249 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/option.py
--rw-r--r--   0        0        0      479 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/utils.py
--rw-r--r--   0        0        0      893 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/globals.py
--rw-r--r--   0        0        0       75 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__init__.py
--rw-r--r--   0        0        0      281 2023-05-13 20:54:48.670191 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0    11313 2023-05-13 20:54:48.674191 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc
--rw-r--r--   0        0        0     7404 2023-05-13 20:54:49.118200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc
--rw-r--r--   0        0        0     6094 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/load_modules.py
--rw-r--r--   0        0        0     4225 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/parse_sentence.py
--rw-r--r--   0        0        0   215603 2023-05-13 20:55:01.706456 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db
--rw-r--r--   0        0        0     3811 1970-01-01 00:00:00.000000 syslog_ng_cfg_helper-1.0.3/PKG-INFO
+-rw-r--r--   0        0        0    35148 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/LICENSE
+-rw-r--r--   0        0        0     2869 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/README.md
+-rw-r--r--   0        0        0     1147 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/__init__.py
+-rw-r--r--   0        0        0      941 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/build_db.py
+-rw-r--r--   0        0        0     2486 2023-05-13 20:58:07.254169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/console.py
+-rw-r--r--   0        0        0      244 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__init__.py
+-rw-r--r--   0        0        0      535 2023-05-13 20:59:06.978325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0     8160 2023-05-13 20:59:06.986325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc
+-rw-r--r--   0        0        0     4579 2023-05-13 20:59:06.982325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc
+-rw-r--r--   0        0        0     5314 2023-05-13 20:59:06.982325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc
+-rw-r--r--   0        0        0      439 2023-05-13 20:59:06.982325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/exceptions.cpython-311.pyc
+-rw-r--r--   0        0        0     5440 2023-05-13 20:59:06.986325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc
+-rw-r--r--   0        0        0     1331 2023-05-13 20:59:06.986325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc
+-rw-r--r--   0        0        0     3783 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/block.py
+-rw-r--r--   0        0        0     1769 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/driver.py
+-rw-r--r--   0        0        0     2263 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/driver_db.py
+-rw-r--r--   0        0        0       42 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/exceptions.py
+-rw-r--r--   0        0        0     2249 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/option.py
+-rw-r--r--   0        0        0      479 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/utils.py
+-rw-r--r--   0        0        0      893 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/globals.py
+-rw-r--r--   0        0        0       75 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__init__.py
+-rw-r--r--   0        0        0      281 2023-05-13 20:59:06.518324 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0    11313 2023-05-13 20:59:06.522324 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc
+-rw-r--r--   0        0        0     7404 2023-05-13 20:59:06.986325 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc
+-rw-r--r--   0        0        0     6094 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/load_modules.py
+-rw-r--r--   0        0        0     4225 2023-05-13 20:58:07.258169 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/parse_sentence.py
+-rw-r--r--   0        0        0   215603 2023-05-13 20:59:17.870350 syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db
+-rw-r--r--   0        0        0     3811 1970-01-01 00:00:00.000000 syslog_ng_cfg_helper-1.0.4/PKG-INFO
```

### Comparing `syslog_ng_cfg_helper-1.0.3/LICENSE` & `syslog_ng_cfg_helper-1.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/README.md` & `syslog_ng_cfg_helper-1.0.4/README.md`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/pyproject.toml` & `syslog_ng_cfg_helper-1.0.4/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "syslog-ng-cfg-helper"
-version = "1.0.3"
+version = "1.0.4"
 description = "Configuration helper for syslog-ng."
 authors = ["Attila Szakacs <szakacs.attila96@gmail.com>"]
 readme = "README.md"
 license = "GPL-3.0-only"
 homepage = "https://github.com/alltilla/syslog-ng-cfg-helper"
 repository = "https://github.com/alltilla/syslog-ng-cfg-helper"
 keywords = ["syslog-ng", "configuration", "cfg"]
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/build_db.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/build_db.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/console.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/console.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc`

 * *Files 2% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
+moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
 files sz: 244
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 2
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
+moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
 files sz: 3783
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
+moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
 files sz: 1769
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 5
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
+moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
 files sz: 2263
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
+moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
 files sz: 2249
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc`

 * *Files 8% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
+moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
 files sz: 479
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/block.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/block.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/driver.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/driver.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/driver_db.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/driver_db.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/option.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/driver_db/option.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/globals.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/globals.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
+moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
 files sz: 6094
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 8
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
+moddate:  0xdff95f64 (Sat May 13 20:58:07 2023 UTC)
 files sz: 4225
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 8
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/load_modules.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/load_modules.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/parse_sentence.py` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/module_loader/parse_sentence.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db` & `syslog_ng_cfg_helper-1.0.4/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db`

 * *Files 1% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9999134318775429%*

 * *Differences: {"'contexts'": "{'parser': {'regexp-parser': {'options': {'flags': {'params': {insert: [(1, "*

 * *               "['<string>'])], delete: [0]}}}}, 'metrics-probe': {'options': {'labels': "*

 * *               "{'params': {insert: [(1, ['<empty>'])], delete: [0]}}}}, 'syslog-parser': "*

 * *               "{'options': {'flags': {'params': {insert: [(1, ['<string>'])], delete: [0]}}, "*

 * *               "'default-facility': {'params': {insert: [(1, ['<string>'])], delete: [0]}}}}, "*

 * *               "'python': {'blocks': {'opti […]*

```diff
@@ -71,18 +71,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -247,18 +247,18 @@
                                 },
                                 "name": "key",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ],
                                             [
-                                                "<string-list>"
+                                                "<string>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
@@ -360,19 +360,19 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
@@ -710,18 +710,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -893,18 +893,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -1083,18 +1083,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -1308,18 +1308,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -1506,18 +1506,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -1842,18 +1842,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -1915,43 +1915,43 @@
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<number>"
+                                                "[",
+                                                "<string-list>",
+                                                "]"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<string>"
+                                                "<float>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<string>",
+                                                "=>",
+                                                "<number>"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
                                                 "<python-yesno>"
                                             ],
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<float>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>",
-                                                "=>",
-                                                "[",
-                                                "<string-list>",
-                                                "]"
+                                                "<empty>"
                                             ]
                                         ]
                                     },
                                     "LogTemplate": {
                                         "name": "LogTemplate",
                                         "params": [
                                             [
@@ -1996,18 +1996,18 @@
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
@@ -2324,30 +2324,30 @@
                     },
                     "response-action": {
                         "name": "response-action",
                         "params": [
                             [
                                 "<positive-integer>",
                                 "=>",
-                                "success"
+                                "retry"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
-                                "retry"
+                                "disconnect"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
                                 "drop"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
-                                "disconnect"
+                                "success"
                             ],
                             [
                                 "<empty>"
                             ]
                         ]
                     },
                     "retries": {
@@ -2526,18 +2526,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -2653,37 +2653,37 @@
                             ]
                         ]
                     },
                     "option": {
                         "name": "option",
                         "params": [
                             [
+                                "<empty>"
+                            ],
+                            [
                                 "<string>",
                                 "=>",
                                 "<string-or-number>"
                             ],
                             [
                                 "<string>",
                                 "<string-or-number>"
-                            ],
-                            [
-                                "<empty>"
                             ]
                         ]
                     },
                     "options": {
                         "name": "options",
                         "params": [
                             [
                                 "<string>",
-                                "=>",
                                 "<string-or-number>"
                             ],
                             [
                                 "<string>",
+                                "=>",
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
-                                        "=>",
                                         "<string-or-number>"
                                     ],
                                     [
                                         "<string>",
+                                        "=>",
                                         "<string-or-number>"
                                     ],
                                     [
                                         "<empty>"
                                     ]
                                 ]
                             },
@@ -2854,18 +2854,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -3173,18 +3173,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -3303,18 +3303,18 @@
                                 },
                                 "name": "key",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ],
                                             [
-                                                "<string-list>"
+                                                "<string>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
@@ -3416,19 +3416,19 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
@@ -3638,18 +3638,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -3695,18 +3695,18 @@
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
@@ -4037,18 +4037,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "failover": {
                         "blocks": {
@@ -4139,18 +4139,18 @@
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
@@ -4275,20 +4275,20 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
                                 "params": [
                                     [
@@ -4399,18 +4399,18 @@
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
@@ -4538,18 +4538,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -4749,24 +4749,24 @@
                             ]
                         ]
                     },
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
-                                "<string>"
+                                "udp"
                             ],
                             [
                                 "tcp"
                             ],
                             [
                                 "tls"
                             ],
                             [
-                                "udp"
+                                "<string>"
                             ]
                         ]
                     },
                     "truncate-size": {
                         "name": "truncate-size",
                         "params": [
                             [
@@ -4854,18 +4854,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -5044,18 +5044,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -5269,18 +5269,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -5423,18 +5423,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -5618,18 +5618,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -5849,18 +5849,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -5906,43 +5906,43 @@
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
                                         "<string>",
                                         "=>",
+                                        "[",
+                                        "<string-list>",
+                                        "]"
+                                    ],
+                                    [
+                                        "<string>",
+                                        "=>",
                                         "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
                                         "<number>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<string>"
+                                        "<python-yesno>"
                                     ],
                                     [
                                         "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<string>"
                                     ],
                                     [
                                         "<empty>"
-                                    ],
-                                    [
-                                        "<string>",
-                                        "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
                                     ]
                                 ]
                             },
                             "LogTemplate": {
                                 "name": "LogTemplate",
                                 "params": [
                                     [
@@ -6031,18 +6031,18 @@
                                 },
                                 "name": "key",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ],
                                             [
-                                                "<string-list>"
+                                                "<string>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
@@ -6144,19 +6144,19 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
@@ -6382,18 +6382,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -6461,19 +6461,19 @@
                             ]
                         ]
                     },
                     "command": {
                         "name": "command",
                         "params": [
                             [
-                                "<string>"
-                            ],
-                            [
                                 "<string>",
                                 "<template-content>"
+                            ],
+                            [
+                                "<string>"
                             ]
                         ]
                     },
                     "frac-digits": {
                         "name": "frac-digits",
                         "params": [
                             [
@@ -6684,18 +6684,18 @@
                                 },
                                 "name": "key",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ],
                                             [
-                                                "<string-list>"
+                                                "<string>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
@@ -6805,19 +6805,19 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
-                                        ":",
                                         "<template-content>"
                                     ]
                                 ]
                             },
                             "scope": {
                                 "name": "scope",
                                 "params": [
@@ -6899,18 +6899,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -7102,23 +7102,23 @@
                             ]
                         ]
                     },
                     "event-time": {
                         "name": "event-time",
                         "params": [
                             [
+                                "<template-content>"
+                            ],
+                            [
                                 "<template-content>",
                                 "seconds"
                             ],
                             [
                                 "<template-content>",
                                 "microseconds"
-                            ],
-                            [
-                                "<template-content>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -7366,18 +7366,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -7421,18 +7421,18 @@
                 "context": "destination",
                 "name": "smtp",
                 "options": {
                     "bcc": {
                         "name": "bcc",
                         "params": [
                             [
-                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
+                                "<template-content>",
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
-                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
+                                "<template-content>",
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
-                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
+                                "<template-content>",
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
-                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
+                                "<template-content>",
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
-                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
+                                "<template-content>",
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
-                                "<template-content>",
                                 "<template-content>"
                             ],
                             [
+                                "<template-content>",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "ts-format": {
                         "name": "ts-format",
                         "params": [
@@ -7702,18 +7702,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -7977,18 +7977,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -8299,18 +8299,18 @@
                     "values": {
                         "name": "values",
                         "params": [
                             [
                                 "default"
                             ],
                             [
-                                "<empty>"
+                                "<template-content>"
                             ],
                             [
-                                "<template-content>"
+                                "<empty>"
                             ]
                         ]
                     }
                 }
             },
             "stomp": {
                 "blocks": {
@@ -8382,18 +8382,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -8512,18 +8512,18 @@
                                 },
                                 "name": "key",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ],
                                             [
-                                                "<string-list>"
+                                                "<string>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
@@ -8625,31 +8625,31 @@
                                 ]
                             },
                             "pair": {
                                 "name": "pair",
                                 "params": [
                                     [
                                         "<string>",
+                                        ":",
                                         "<template-content>"
                                     ],
                                     [
                                         "<string>",
-                                        ":",
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
@@ -8887,18 +8887,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "failover": {
                         "blocks": {
@@ -9125,31 +9125,31 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<yesno>"
                                     ],
                                     [
-                                        "<yesno>"
+                                        "<string>"
                                     ]
                                 ]
                             },
                             "pkcs12-file": {
                                 "name": "pkcs12-file",
                                 "params": [
                                     [
@@ -9388,18 +9388,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -9599,21 +9599,21 @@
                             ]
                         ]
                     },
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
-                                "tls"
+                                "udp"
                             ],
                             [
-                                "tcp"
+                                "tls"
                             ],
                             [
-                                "udp"
+                                "tcp"
                             ],
                             [
                                 "<string>"
                             ]
                         ]
                     },
                     "truncate-size": {
@@ -9704,18 +9704,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "failover": {
                         "blocks": {
@@ -9806,18 +9806,18 @@
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
@@ -9942,20 +9942,20 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
                                 "params": [
                                     [
@@ -10197,18 +10197,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -10480,18 +10480,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "failover": {
                         "blocks": {
@@ -10582,18 +10582,18 @@
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
@@ -10718,20 +10718,20 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
                                 "params": [
                                     [
@@ -10842,18 +10842,18 @@
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
@@ -10973,18 +10973,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -11256,18 +11256,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "failover": {
                         "blocks": {
@@ -11388,18 +11388,18 @@
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
@@ -11519,18 +11519,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -11818,18 +11818,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "failover": {
                         "blocks": {
@@ -11950,18 +11950,18 @@
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
@@ -12081,18 +12081,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -12380,18 +12380,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -12534,18 +12534,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -12785,18 +12785,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -12856,18 +12856,18 @@
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
@@ -12939,18 +12939,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -13229,18 +13229,18 @@
                             ]
                         ]
                     },
                     "truncate-size-ratio": {
                         "name": "truncate-size-ratio",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     }
                 }
             },
             "jvm-options": {
                 "blocks": {},
@@ -13559,18 +13559,18 @@
                             ]
                         ]
                     },
                     "inject-mode": {
                         "name": "inject-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -13815,18 +13815,18 @@
                             ]
                         ]
                     },
                     "inject-mode": {
                         "name": "inject-mode",
                         "params": [
                             [
-                                "<string>"
+                                "internal"
                             ],
                             [
-                                "internal"
+                                "<string>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -14168,18 +14168,18 @@
                         },
                         "name": "key",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<string-list>"
                                     ],
                                     [
-                                        "<string-list>"
+                                        "<string>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "rekey": {
                         "blocks": {},
@@ -14274,31 +14274,31 @@
                         ]
                     },
                     "pair": {
                         "name": "pair",
                         "params": [
                             [
                                 "<string>",
+                                ":",
                                 "<template-content>"
                             ],
                             [
                                 "<string>",
-                                ":",
                                 "<template-content>"
                             ]
                         ]
                     },
                     "scope": {
                         "name": "scope",
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
                     }
                 }
             },
             "metrics-probe": {
                 "blocks": {},
@@ -14337,20 +14337,20 @@
                             ]
                         ]
                     },
                     "labels": {
                         "name": "labels",
                         "params": [
                             [
-                                "<empty>"
-                            ],
-                            [
                                 "<string>",
                                 "=>",
                                 "<template-content>"
+                            ],
+                            [
+                                "<empty>"
                             ]
                         ]
                     },
                     "level": {
                         "name": "level",
                         "params": [
                             [
@@ -14416,43 +14416,43 @@
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
                                         "<string>",
                                         "=>",
+                                        "[",
+                                        "<string-list>",
+                                        "]"
+                                    ],
+                                    [
+                                        "<string>",
+                                        "=>",
                                         "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
                                         "<number>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<string>"
+                                        "<python-yesno>"
                                     ],
                                     [
                                         "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<string>"
                                     ],
                                     [
                                         "<empty>"
-                                    ],
-                                    [
-                                        "<string>",
-                                        "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
                                     ]
                                 ]
                             },
                             "LogTemplate": {
                                 "name": "LogTemplate",
                                 "params": [
                                     [
@@ -14513,18 +14513,18 @@
                 "context": "parser",
                 "name": "regexp-parser",
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
                     "internal": {
                         "name": "internal",
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -14684,18 +14684,18 @@
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
                             ],
                             [
                                 "check-hostname"
                             ]
                         ]
                     },
                     "internal": {
@@ -14987,18 +14987,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -15030,18 +15030,18 @@
                             ]
                         ]
                     },
                     "fetch-no-data-delay": {
                         "name": "fetch-no-data-delay",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "file": {
                         "name": "file",
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
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -15305,18 +15305,18 @@
                             ]
                         ]
                     },
                     "freq": {
                         "name": "freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
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
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -15455,20 +15455,20 @@
                             ]
                         ]
                     },
                     "values": {
                         "name": "values",
                         "params": [
                             [
-                                "<empty>"
-                            ],
-                            [
                                 "<string>",
                                 "=>",
                                 "<template-content>"
+                            ],
+                            [
+                                "<empty>"
                             ]
                         ]
                     }
                 }
             },
             "example-random-generator": {
                 "blocks": {
@@ -15558,18 +15558,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -15971,18 +15971,18 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -16416,32 +16416,32 @@
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
                                 "<empty>"
                             ],
                             [
                                 "check-hostname"
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
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "force-directory-polling": {
                         "name": "force-directory-polling",
                         "params": [
                             [
@@ -16785,18 +16785,18 @@
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
@@ -16911,18 +16911,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -16954,18 +16954,18 @@
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
@@ -17364,20 +17364,20 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
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
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -17509,18 +17509,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
                         "params": [
                             [
@@ -17528,18 +17528,18 @@
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
                             ],
                             [
                                 "check-hostname"
                             ]
                         ]
                     },
                     "format": {
@@ -17854,24 +17854,24 @@
                             ]
                         ]
                     },
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
-                                "<string>"
+                                "udp"
                             ],
                             [
                                 "tcp"
                             ],
                             [
-                                "udp"
+                                "tls"
                             ],
                             [
-                                "tls"
+                                "<string>"
                             ]
                         ]
                     },
                     "trim-large-messages": {
                         "name": "trim-large-messages",
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -18189,18 +18189,18 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -18604,18 +18604,18 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
+                                        "[",
+                                        "<string-list>",
+                                        "]"
+                                    ],
+                                    [
+                                        "<string>",
+                                        "=>",
                                         "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
                                         "<number>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<string>"
+                                        "<python-yesno>"
                                     ],
                                     [
                                         "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<string>"
                                     ],
                                     [
                                         "<empty>"
-                                    ],
-                                    [
-                                        "<string>",
-                                        "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -18979,18 +18979,18 @@
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
@@ -19221,43 +19221,43 @@
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "[",
+                                        "<string-list>",
+                                        "]"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<string>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<string>",
+                                        "=>",
+                                        "<number>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
                                         "<python-yesno>"
                                     ],
                                     [
-                                        "<empty>"
+                                        "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<float>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>",
-                                        "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<empty>"
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -19330,29 +19330,29 @@
                             ]
                         ]
                     },
                     "fetch-no-data-delay": {
                         "name": "fetch-no-data-delay",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
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
@@ -19488,18 +19488,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -19692,29 +19692,29 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ]
                         ]
                     },
                     "follow-freq": {
                         "name": "follow-freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "force-directory-polling": {
                         "name": "force-directory-polling",
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
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -20270,18 +20270,18 @@
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
@@ -20398,31 +20398,31 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
                                 "params": [
                                     [
-                                        "<string>"
+                                        "<yesno>"
                                     ],
                                     [
-                                        "<yesno>"
+                                        "<string>"
                                     ]
                                 ]
                             },
                             "pkcs12-file": {
                                 "name": "pkcs12-file",
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
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -20543,18 +20543,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
                         "params": [
                             [
@@ -20565,18 +20565,18 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -20888,21 +20888,21 @@
                             ]
                         ]
                     },
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
-                                "tls"
+                                "udp"
                             ],
                             [
                                 "tcp"
                             ],
                             [
-                                "udp"
+                                "tls"
                             ],
                             [
                                 "<string>"
                             ]
                         ]
                     },
                     "trim-large-messages": {
@@ -20913,18 +20913,18 @@
                             ]
                         ]
                     },
                     "use-dns": {
                         "name": "use-dns",
                         "params": [
                             [
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -21137,20 +21137,20 @@
                             ]
                         ]
                     },
                     "matches": {
                         "name": "matches",
                         "params": [
                             [
-                                "<empty>"
-                            ],
-                            [
                                 "<string>",
                                 "=>",
                                 "<string>"
+                            ],
+                            [
+                                "<empty>"
                             ]
                         ]
                     },
                     "max-field-size": {
                         "name": "max-field-size",
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
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
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
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -21390,18 +21390,18 @@
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
                             ],
                             [
                                 "check-hostname"
                             ]
                         ]
                     },
                     "format": {
@@ -21835,20 +21835,20 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
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
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -21980,18 +21980,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
                         "params": [
                             [
@@ -22002,18 +22002,18 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
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
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
                             ]
                         ]
                     },
                     "use-fqdn": {
                         "name": "use-fqdn",
                         "params": [
                             [
@@ -22556,20 +22556,20 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
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
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -22701,18 +22701,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
                         "params": [
                             [
@@ -22720,18 +22720,18 @@
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
                             ],
                             [
                                 "check-hostname"
                             ]
                         ]
                     },
                     "format": {
@@ -23163,18 +23163,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -23214,21 +23214,21 @@
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
                                 "<empty>"
                             ],
                             [
                                 "check-hostname"
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
@@ -23633,18 +23633,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -23684,18 +23684,18 @@
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
                             ],
                             [
                                 "check-hostname"
                             ]
                         ]
                     },
                     "format": {
@@ -24119,18 +24119,18 @@
                             ]
                         ]
                     },
                     "default-facility": {
                         "name": "default-facility",
                         "params": [
                             [
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -24211,18 +24211,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
                         "params": [
                             [
@@ -24233,18 +24233,18 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
-                                "<yesno>"
+                                "persist-only"
                             ],
                             [
-                                "persist-only"
+                                "<yesno>"
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
-                                "<string>"
+                                "syslog"
                             ],
                             [
-                                "syslog"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -24758,18 +24758,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
                         "params": [
                             [
@@ -24780,18 +24780,18 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
-                                "<string>"
+                                "KW_SYSLOG"
                             ],
                             [
-                                "KW_SYSLOG"
+                                "<string>"
                             ]
                         ]
                     },
                     "default-level": {
                         "name": "default-level",
                         "params": [
                             [
@@ -25300,29 +25300,29 @@
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "<empty>"
+                                "check-hostname"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ]
                         ]
                     },
                     "follow-freq": {
                         "name": "follow-freq",
                         "params": [
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ],
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
```

### Comparing `syslog_ng_cfg_helper-1.0.3/PKG-INFO` & `syslog_ng_cfg_helper-1.0.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: syslog-ng-cfg-helper
-Version: 1.0.3
+Version: 1.0.4
 Summary: Configuration helper for syslog-ng.
 Home-page: https://github.com/alltilla/syslog-ng-cfg-helper
 License: GPL-3.0-only
 Keywords: syslog-ng,configuration,cfg
 Author: Attila Szakacs
 Author-email: szakacs.attila96@gmail.com
 Requires-Python: >=3.8,<4.0
```

