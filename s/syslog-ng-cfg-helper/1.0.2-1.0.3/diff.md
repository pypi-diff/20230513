# Comparing `tmp/syslog_ng_cfg_helper-1.0.2.tar.gz` & `tmp/syslog_ng_cfg_helper-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "syslog_ng_cfg_helper-1.0.2.tar", max compression
+gzip compressed data, was "syslog_ng_cfg_helper-1.0.3.tar", max compression
```

## Comparing `syslog_ng_cfg_helper-1.0.2.tar` & `syslog_ng_cfg_helper-1.0.3.tar`

### file list

```diff
@@ -1,29 +1,29 @@
--rw-r--r--   0        0        0    35148 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/LICENSE
--rw-r--r--   0        0        0     2868 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/README.md
--rw-r--r--   0        0        0     1147 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/__init__.py
--rw-r--r--   0        0        0      941 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/build_db.py
--rw-r--r--   0        0        0     2486 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/console.py
--rw-r--r--   0        0        0      244 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__init__.py
--rw-r--r--   0        0        0      535 2023-05-13 20:34:10.780076 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0     8160 2023-05-13 20:34:10.784076 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc
--rw-r--r--   0        0        0     4579 2023-05-13 20:34:10.784076 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc
--rw-r--r--   0        0        0     5314 2023-05-13 20:34:10.780076 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc
--rw-r--r--   0        0        0      439 2023-05-13 20:34:10.784076 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/exceptions.cpython-311.pyc
--rw-r--r--   0        0        0     5440 2023-05-13 20:34:10.784076 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc
--rw-r--r--   0        0        0     1331 2023-05-13 20:34:10.784076 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc
--rw-r--r--   0        0        0     3783 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/block.py
--rw-r--r--   0        0        0     1769 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/driver.py
--rw-r--r--   0        0        0     2263 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/driver_db.py
--rw-r--r--   0        0        0       42 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/exceptions.py
--rw-r--r--   0        0        0     2249 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/option.py
--rw-r--r--   0        0        0      479 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/utils.py
--rw-r--r--   0        0        0      893 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/globals.py
--rw-r--r--   0        0        0       75 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/__init__.py
--rw-r--r--   0        0        0      281 2023-05-13 20:34:10.340069 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0    11313 2023-05-13 20:34:10.344070 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc
--rw-r--r--   0        0        0     7404 2023-05-13 20:34:10.788076 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc
--rw-r--r--   0        0        0     6094 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/load_modules.py
--rw-r--r--   0        0        0     4225 2023-05-13 20:33:12.579251 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/parse_sentence.py
--rw-r--r--   0        0        0   215603 2023-05-13 20:34:23.300254 syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db
--rw-r--r--   0        0        0     3810 1970-01-01 00:00:00.000000 syslog_ng_cfg_helper-1.0.2/PKG-INFO
+-rw-r--r--   0        0        0    35148 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/LICENSE
+-rw-r--r--   0        0        0     2869 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/README.md
+-rw-r--r--   0        0        0     1147 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/__init__.py
+-rw-r--r--   0        0        0      941 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/build_db.py
+-rw-r--r--   0        0        0     2486 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/console.py
+-rw-r--r--   0        0        0      244 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__init__.py
+-rw-r--r--   0        0        0      535 2023-05-13 20:54:49.110200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0     8160 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc
+-rw-r--r--   0        0        0     4579 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc
+-rw-r--r--   0        0        0     5314 2023-05-13 20:54:49.110200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc
+-rw-r--r--   0        0        0      439 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/exceptions.cpython-311.pyc
+-rw-r--r--   0        0        0     5440 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc
+-rw-r--r--   0        0        0     1331 2023-05-13 20:54:49.114200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc
+-rw-r--r--   0        0        0     3783 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/block.py
+-rw-r--r--   0        0        0     1769 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/driver.py
+-rw-r--r--   0        0        0     2263 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/driver_db.py
+-rw-r--r--   0        0        0       42 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/exceptions.py
+-rw-r--r--   0        0        0     2249 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/option.py
+-rw-r--r--   0        0        0      479 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/utils.py
+-rw-r--r--   0        0        0      893 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/globals.py
+-rw-r--r--   0        0        0       75 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__init__.py
+-rw-r--r--   0        0        0      281 2023-05-13 20:54:48.670191 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0    11313 2023-05-13 20:54:48.674191 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc
+-rw-r--r--   0        0        0     7404 2023-05-13 20:54:49.118200 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc
+-rw-r--r--   0        0        0     6094 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/load_modules.py
+-rw-r--r--   0        0        0     4225 2023-05-13 20:53:48.160937 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/parse_sentence.py
+-rw-r--r--   0        0        0   215603 2023-05-13 20:55:01.706456 syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db
+-rw-r--r--   0        0        0     3811 1970-01-01 00:00:00.000000 syslog_ng_cfg_helper-1.0.3/PKG-INFO
```

### Comparing `syslog_ng_cfg_helper-1.0.2/LICENSE` & `syslog_ng_cfg_helper-1.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/README.md` & `syslog_ng_cfg_helper-1.0.3/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -86,14 +86,14 @@
 
 The [Makefile](https://github.com/alltilla/syslog-ng-cfg-helper/blob/master/Makefile) consists of some useful commands:
   * `make venv` prepares the venv.
   * `make bison` downloads bison 3.7.6, builds it and installs it under `/usr/local`.
     * You can change the install path with `make bison BISON_INSTALL_PATH=...`
   * `make check` runs the unit tests, style-checkers and linters.
   * `make format` formats the code.
-  * `make db` download the syslog-ng release tarball and generates the option database.
+  * `make db` downloads the syslog-ng release tarball and generates the option database.
   * `make package` creates the pip package.
 
 ## Community
 You can reach out to the syslog-ng community on Discord:
 
 [![Axoflow Discord Server](https://discordapp.com/api/guilds/1082023686028148877/widget.png?style=banner2)](https://discord.gg/E65kP9aZGm)
```

### Comparing `syslog_ng_cfg_helper-1.0.2/pyproject.toml` & `syslog_ng_cfg_helper-1.0.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "syslog-ng-cfg-helper"
-version = "1.0.2"
+version = "1.0.3"
 description = "Configuration helper for syslog-ng."
 authors = ["Attila Szakacs <szakacs.attila96@gmail.com>"]
 readme = "README.md"
 license = "GPL-3.0-only"
 homepage = "https://github.com/alltilla/syslog-ng-cfg-helper"
 repository = "https://github.com/alltilla/syslog-ng-cfg-helper"
 keywords = ["syslog-ng", "configuration", "cfg"]
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/build_db.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/build_db.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/console.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/console.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/__init__.cpython-311.pyc`

 * *Files 21% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0x08f45f64 (Sat May 13 20:33:12 2023 UTC)
+moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
 files sz: 244
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 2
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/block.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0x08f45f64 (Sat May 13 20:33:12 2023 UTC)
+moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
 files sz: 3783
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/driver.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0x08f45f64 (Sat May 13 20:33:12 2023 UTC)
+moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
 files sz: 1769
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 5
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/driver_db.cpython-311.pyc`

 * *Files 2% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0x08f45f64 (Sat May 13 20:33:12 2023 UTC)
+moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
 files sz: 2263
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/option.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0x08f45f64 (Sat May 13 20:33:12 2023 UTC)
+moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
 files sz: 2249
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 16777216
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/__pycache__/utils.cpython-311.pyc`

 * *Files 9% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0x08f45f64 (Sat May 13 20:33:12 2023 UTC)
+moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
 files sz: 479
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/block.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/block.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/driver.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/driver.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/driver_db.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/driver_db.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/driver_db/option.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/driver_db/option.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/globals.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/globals.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/load_modules.cpython-311.pyc`

 * *Files 1% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0x08f45f64 (Sat May 13 20:33:12 2023 UTC)
+moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
 files sz: 6094
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 8
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/__pycache__/parse_sentence.cpython-311.pyc`

 * *Files 0% similar despite different names*

#### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0x08f45f64 (Sat May 13 20:33:12 2023 UTC)
+moddate:  0xdcf85f64 (Sat May 13 20:53:48 2023 UTC)
 files sz: 4225
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 8
    flags     : 0
    code
```

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/load_modules.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/load_modules.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/module_loader/parse_sentence.py` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/module_loader/parse_sentence.py`

 * *Files identical despite different names*

### Comparing `syslog_ng_cfg_helper-1.0.2/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db` & `syslog_ng_cfg_helper-1.0.3/syslog_ng_cfg_helper/syslog-ng-cfg-helper.db`

 * *Files 1% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9998960928035681%*

 * *Differences: {"'contexts'": "{'parser': {'csv-parser': {'blocks': {'delimiters': {'options': {'': {'params': "*

 * *               "{insert: [(1, ['<empty>'])], delete: [0]}}}}}, 'options': {'flags': {'params': "*

 * *               "{insert: [(1, ['drop-invalid']), (2, ['<empty>'])], delete: [1, 0]}}}}, "*

 * *               "'regexp-parser': {'options': {'flags': {'params': {insert: [(1, ['<empty>'])], "*

 * *               "delete: [0]}}}}, 'metrics-probe': {'options': {'labels': {'params': {insert: [(1, "*

 * *               "['<string>', ' […]*

```diff
@@ -71,18 +71,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                                "<string-list>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
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
-                                        "<empty>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ]
                                 ]
                             }
                         }
                     }
                 },
                 "context": "destination",
@@ -710,18 +710,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -964,51 +964,51 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -1083,18 +1083,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -1379,51 +1379,51 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -1506,18 +1506,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
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
-                                        "<empty>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "tls12-and-older": {
                                 "name": "tls12-and-older",
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -1913,45 +1913,45 @@
                                 "blocks": {},
                                 "name": "options",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<empty>"
-                                            ],
-                                            [
                                                 "<string>",
                                                 "=>",
-                                                "<python-yesno>"
+                                                "<number>"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "[",
-                                                "<string-list>",
-                                                "]"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>",
-                                                "=>",
                                                 "<string>"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<float>"
+                                                "<python-yesno>"
+                                            ],
+                                            [
+                                                "<empty>"
                                             ],
                                             [
                                                 "<string>",
                                                 "=>",
-                                                "<number>"
+                                                "<float>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<string>",
+                                                "=>",
+                                                "[",
+                                                "<string-list>",
+                                                "]"
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
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
                                             ]
                                         ]
                                     },
                                     "tls12-and-older": {
                                         "name": "tls12-and-older",
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
-                                "<empty>"
-                            ],
-                            [
                                 "<positive-integer>",
                                 "=>",
-                                "drop"
+                                "success"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
                                 "retry"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
-                                "success"
+                                "drop"
                             ],
                             [
                                 "<positive-integer>",
                                 "=>",
                                 "disconnect"
+                            ],
+                            [
+                                "<empty>"
                             ]
                         ]
                     },
                     "retries": {
                         "name": "retries",
                         "params": [
                             [
@@ -2526,18 +2526,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -2653,41 +2653,41 @@
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
                     "persist-name": {
                         "name": "persist-name",
                         "params": [
                             [
@@ -2759,24 +2759,24 @@
                         "blocks": {},
                         "name": "config",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
                                         "<string-or-number>"
                                     ],
                                     [
                                         "<string>",
                                         "<string-or-number>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ]
                                 ]
                             },
                             "<string>": {
                                 "name": "<string>",
                                 "params": [
                                     [
@@ -2854,18 +2854,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                                "<string-list>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
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
-                                        "<empty>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ]
                                 ]
                             }
                         }
                     }
                 },
                 "context": "destination",
@@ -3638,18 +3638,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
                                             ]
                                         ]
                                     },
                                     "tls12-and-older": {
                                         "name": "tls12-and-older",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -4752,21 +4752,21 @@
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
                                 "<string>"
                             ],
                             [
-                                "udp"
+                                "tcp"
                             ],
                             [
                                 "tls"
                             ],
                             [
-                                "tcp"
+                                "udp"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -4925,51 +4925,51 @@
                             ]
                         ]
                     },
                     "dir-group": {
                         "name": "dir-group",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "internal": {
                         "name": "internal",
                         "params": [
                             [
@@ -5044,18 +5044,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -5332,18 +5332,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -5423,18 +5423,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -5904,45 +5904,45 @@
                         "blocks": {},
                         "name": "options",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<number>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
                                         "<string>"
                                     ],
                                     [
-                                        "<string>",
-                                        "=>",
-                                        "<float>"
+                                        "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "<python-yesno>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
+                                    ],
+                                    [
+                                        "<string>",
+                                        "=>",
+                                        "[",
+                                        "<string-list>",
+                                        "]"
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
-                                                "<string-list>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
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
-                                        "<empty>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ]
                                 ]
                             }
                         }
                     }
                 },
                 "context": "destination",
@@ -6382,18 +6382,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                "<string>",
-                                "<template-content>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<string>",
+                                "<template-content>"
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
-                                                "<string-list>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<string-list>"
                                             ]
                                         ]
                                     }
                                 }
                             },
                             "rekey": {
                                 "blocks": {},
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
-                                        "<empty>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "disk-buffer": {
                         "blocks": {},
@@ -6899,18 +6899,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -7366,18 +7366,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -7702,18 +7702,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -8073,30 +8073,30 @@
                         ]
                     },
                     "dbd-option": {
                         "name": "dbd-option",
                         "params": [
                             [
                                 "<string>",
-                                "<number>"
+                                "<string>"
                             ],
                             [
                                 "<string>",
-                                "<string>"
+                                "<number>"
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -8296,18 +8296,18 @@
                             ]
                         ]
                     },
                     "values": {
                         "name": "values",
                         "params": [
                             [
-                                "<empty>"
+                                "default"
                             ],
                             [
-                                "default"
+                                "<empty>"
                             ],
                             [
                                 "<template-content>"
                             ]
                         ]
                     }
                 }
@@ -8382,18 +8382,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                                "<string-list>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<string-list>"
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
-                                        "<empty>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "failover": {
                         "blocks": {
@@ -8989,18 +8989,18 @@
                                 "blocks": {},
                                 "name": "cipher-suite",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
                                             ]
                                         ]
                                     },
                                     "tls12-and-older": {
                                         "name": "tls12-and-older",
                                         "params": [
                                             [
@@ -9125,31 +9125,31 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
+                                        "<empty>"
+                                    ],
+                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
                                 "params": [
                                     [
-                                        "<yesno>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<yesno>"
                                     ]
                                 ]
                             },
                             "pkcs12-file": {
                                 "name": "pkcs12-file",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
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
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
                             ]
                         ]
                     },
                     "on-error": {
                         "name": "on-error",
                         "params": [
                             [
@@ -9602,21 +9602,21 @@
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
                                 "tls"
                             ],
                             [
-                                "udp"
+                                "tcp"
                             ],
                             [
-                                "<string>"
+                                "udp"
                             ],
                             [
-                                "tcp"
+                                "<string>"
                             ]
                         ]
                     },
                     "truncate-size": {
                         "name": "truncate-size",
                         "params": [
                             [
@@ -9704,18 +9704,18 @@
                                     ]
                                 ]
                             },
                             "truncate-size-ratio": {
                                 "name": "truncate-size-ratio",
                                 "params": [
                                     [
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
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
+                                        "<empty>"
+                                    ],
+                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
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
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
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
+                                        "<empty>"
+                                    ],
+                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
                                     ]
                                 ]
                             }
                         }
                     },
                     "hook-commands": {
                         "blocks": {},
@@ -12451,18 +12451,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "flush-lines": {
                         "name": "flush-lines",
                         "params": [
                             [
@@ -12534,18 +12534,18 @@
                             ]
                         ]
                     },
                     "mark-mode": {
                         "name": "mark-mode",
                         "params": [
                             [
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                        "<float>"
+                                        "<nonnegative-integer>"
                                     ],
                                     [
-                                        "<nonnegative-integer>"
+                                        "<float>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     }
                 }
             },
             "jvm-options": {
                 "blocks": {},
@@ -13351,18 +13351,18 @@
                         "blocks": {},
                         "name": "delimiters",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<empty>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
                                 "drop-invalid"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -13559,18 +13559,18 @@
                             ]
                         ]
                     },
                     "inject-mode": {
                         "name": "inject-mode",
                         "params": [
                             [
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                "internal"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "internal"
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
-                                        "<string-list>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<string-list>"
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
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
+                                "<empty>"
+                            ],
+                            [
                                 "<string>",
                                 "=>",
                                 "<template-content>"
-                            ],
-                            [
-                                "<empty>"
                             ]
                         ]
                     },
                     "level": {
                         "name": "level",
                         "params": [
                             [
@@ -14414,45 +14414,45 @@
                         "blocks": {},
                         "name": "options",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<number>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
                                         "<string>"
                                     ],
                                     [
-                                        "<string>",
-                                        "=>",
-                                        "<float>"
+                                        "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "<python-yesno>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
+                                    ],
+                                    [
+                                        "<string>",
+                                        "=>",
+                                        "[",
+                                        "<string-list>",
+                                        "]"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
@@ -15030,18 +15030,18 @@
                             ]
                         ]
                     },
                     "fetch-no-data-delay": {
                         "name": "fetch-no-data-delay",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "file": {
                         "name": "file",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "host-override": {
                         "name": "host-override",
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
+                                "<empty>"
+                            ],
+                            [
                                 "<string>",
                                 "=>",
                                 "<template-content>"
-                            ],
-                            [
-                                "<empty>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
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
-                                "<float>"
+                                "<positive-integer>"
                             ],
                             [
-                                "<positive-integer>"
+                                "<float>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
                             ]
                         ]
                     },
                     "follow-freq": {
                         "name": "follow-freq",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "force-directory-polling": {
                         "name": "force-directory-polling",
                         "params": [
                             [
@@ -16457,18 +16457,18 @@
                             ]
                         ]
                     },
                     "group": {
                         "name": "group",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
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
@@ -16785,18 +16785,18 @@
                                 "blocks": {},
                                 "name": "cipher-suite",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
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
@@ -16954,18 +16954,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
@@ -17236,18 +17236,18 @@
                                 "blocks": {},
                                 "name": "cipher-suite",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
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
@@ -17509,18 +17509,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
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
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -17854,24 +17854,24 @@
                             ]
                         ]
                     },
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
-                                "udp"
+                                "<string>"
                             ],
                             [
-                                "tls"
+                                "tcp"
                             ],
                             [
-                                "tcp"
+                                "udp"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
@@ -18868,45 +18868,45 @@
                         "blocks": {},
                         "name": "options",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<float>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<number>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
                                         "<string>"
                                     ],
                                     [
-                                        "<string>",
-                                        "=>",
-                                        "<float>"
+                                        "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "<python-yesno>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<empty>"
+                                    ],
+                                    [
+                                        "<string>",
+                                        "=>",
+                                        "[",
+                                        "<string-list>",
+                                        "]"
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
@@ -18979,18 +18979,18 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
@@ -19219,45 +19219,45 @@
                         "blocks": {},
                         "name": "options",
                         "options": {
                             "": {
                                 "name": null,
                                 "params": [
                                     [
-                                        "<empty>"
-                                    ],
-                                    [
                                         "<string>",
                                         "=>",
-                                        "<python-yesno>"
+                                        "<number>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "[",
-                                        "<string-list>",
-                                        "]"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>",
-                                        "=>",
                                         "<string>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<float>"
+                                        "<python-yesno>"
+                                    ],
+                                    [
+                                        "<empty>"
                                     ],
                                     [
                                         "<string>",
                                         "=>",
-                                        "<number>"
+                                        "<float>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<string>",
+                                        "=>",
+                                        "[",
+                                        "<string-list>",
+                                        "]"
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
@@ -19330,29 +19330,29 @@
                             ]
                         ]
                     },
                     "fetch-no-data-delay": {
                         "name": "fetch-no-data-delay",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "<string>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -19689,32 +19689,32 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
                             ]
                         ]
                     },
                     "follow-freq": {
                         "name": "follow-freq",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "force-directory-polling": {
                         "name": "force-directory-polling",
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
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
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
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
+                                        "<empty>"
+                                    ],
+                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
                                     ]
                                 ]
                             },
                             "peer-verify": {
                                 "name": "peer-verify",
                                 "params": [
                                     [
-                                        "<yesno>"
+                                        "<string>"
                                     ],
                                     [
-                                        "<string>"
+                                        "<yesno>"
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
@@ -20543,18 +20543,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -20888,23 +20888,23 @@
                             ]
                         ]
                     },
                     "transport": {
                         "name": "transport",
                         "params": [
                             [
-                                "udp"
-                            ],
-                            [
                                 "tls"
                             ],
                             [
                                 "tcp"
                             ],
                             [
+                                "udp"
+                            ],
+                            [
                                 "<string>"
                             ]
                         ]
                     },
                     "trim-large-messages": {
                         "name": "trim-large-messages",
                         "params": [
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
@@ -21137,20 +21137,20 @@
                             ]
                         ]
                     },
                     "matches": {
                         "name": "matches",
                         "params": [
                             [
+                                "<empty>"
+                            ],
+                            [
                                 "<string>",
                                 "=>",
                                 "<string>"
-                            ],
-                            [
-                                "<empty>"
                             ]
                         ]
                     },
                     "max-field-size": {
                         "name": "max-field-size",
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
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
@@ -21707,18 +21707,18 @@
                                 "blocks": {},
                                 "name": "cipher-suite",
                                 "options": {
                                     "": {
                                         "name": null,
                                         "params": [
                                             [
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
                                             ]
                                         ]
                                     },
                                     "tls12-and-older": {
                                         "name": "tls12-and-older",
                                         "params": [
                                             [
@@ -21835,20 +21835,20 @@
                                     ]
                                 ]
                             },
                             "openssl-conf-cmds": {
                                 "name": "openssl-conf-cmds",
                                 "params": [
                                     [
+                                        "<empty>"
+                                    ],
+                                    [
                                         "<string>",
                                         "=>",
                                         "<string>"
-                                    ],
-                                    [
-                                        "<empty>"
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
@@ -21980,18 +21980,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
-                                                "<empty>"
+                                                "<string>"
                                             ],
                                             [
-                                                "<string>"
+                                                "<empty>"
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
@@ -22701,18 +22701,18 @@
                             ]
                         ]
                     },
                     "dynamic-window-stats-freq": {
                         "name": "dynamic-window-stats-freq",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
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
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
@@ -23214,21 +23214,21 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
                         "params": [
                             [
@@ -23516,18 +23516,18 @@
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
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
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
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "persist-name": {
                         "name": "persist-name",
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
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
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "encoding": {
                         "name": "encoding",
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
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-owner": {
                         "name": "dir-owner",
                         "params": [
                             [
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dir-perm": {
                         "name": "dir-perm",
                         "params": [
                             [
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
                             ]
                         ]
                     },
                     "dns-cache": {
                         "name": "dns-cache",
                         "params": [
                             [
@@ -25297,32 +25297,32 @@
                             ]
                         ]
                     },
                     "flags": {
                         "name": "flags",
                         "params": [
                             [
-                                "<empty>"
+                                "<string>"
                             ],
                             [
-                                "check-hostname"
+                                "<empty>"
                             ],
                             [
-                                "<string>"
+                                "check-hostname"
                             ]
                         ]
                     },
                     "follow-freq": {
                         "name": "follow-freq",
                         "params": [
                             [
-                                "<float>"
+                                "<nonnegative-integer>"
                             ],
                             [
-                                "<nonnegative-integer>"
+                                "<float>"
                             ]
                         ]
                     },
                     "format": {
                         "name": "format",
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<string-or-number>"
                             ],
                             [
-                                "<string-or-number>"
+                                "<empty>"
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
-                                "<empty>"
+                                "<number>"
                             ],
                             [
-                                "<number>"
+                                "<empty>"
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
```

### Comparing `syslog_ng_cfg_helper-1.0.2/PKG-INFO` & `syslog_ng_cfg_helper-1.0.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: syslog-ng-cfg-helper
-Version: 1.0.2
+Version: 1.0.3
 Summary: Configuration helper for syslog-ng.
 Home-page: https://github.com/alltilla/syslog-ng-cfg-helper
 License: GPL-3.0-only
 Keywords: syslog-ng,configuration,cfg
 Author: Attila Szakacs
 Author-email: szakacs.attila96@gmail.com
 Requires-Python: >=3.8,<4.0
@@ -109,15 +109,15 @@
 
 The [Makefile](https://github.com/alltilla/syslog-ng-cfg-helper/blob/master/Makefile) consists of some useful commands:
   * `make venv` prepares the venv.
   * `make bison` downloads bison 3.7.6, builds it and installs it under `/usr/local`.
     * You can change the install path with `make bison BISON_INSTALL_PATH=...`
   * `make check` runs the unit tests, style-checkers and linters.
   * `make format` formats the code.
-  * `make db` download the syslog-ng release tarball and generates the option database.
+  * `make db` downloads the syslog-ng release tarball and generates the option database.
   * `make package` creates the pip package.
 
 ## Community
 You can reach out to the syslog-ng community on Discord:
 
 [![Axoflow Discord Server](https://discordapp.com/api/guilds/1082023686028148877/widget.png?style=banner2)](https://discord.gg/E65kP9aZGm)
```

