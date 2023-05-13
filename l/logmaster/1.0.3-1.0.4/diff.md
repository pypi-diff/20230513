# Comparing `tmp/logmaster-1.0.3.tar.gz` & `tmp/logmaster-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "logmaster-1.0.3.tar", last modified: Thu May 11 00:54:58 2023, max compression
+gzip compressed data, was "logmaster-1.0.4.tar", last modified: Thu May 11 16:08:17 2023, max compression
```

## Comparing `logmaster-1.0.3.tar` & `logmaster-1.0.4.tar`

### file list

```diff
@@ -1,12 +1,12 @@
-drwxrwxrwx   0        0        0        0 2023-05-11 00:54:58.441204 logmaster-1.0.3/
--rw-rw-rw-   0        0        0     1083 2023-05-08 22:14:25.000000 logmaster-1.0.3/LICENSE
--rw-rw-rw-   0        0        0     1514 2023-05-11 00:54:58.442203 logmaster-1.0.3/PKG-INFO
--rw-rw-rw-   0        0        0     1034 2023-05-08 22:25:07.000000 logmaster-1.0.3/README.md
-drwxrwxrwx   0        0        0        0 2023-05-11 00:54:58.395197 logmaster-1.0.3/logmaster/
-drwxrwxrwx   0        0        0        0 2023-05-11 00:54:58.438199 logmaster-1.0.3/logmaster/logmaster.egg-info/
--rw-rw-rw-   0        0        0     1514 2023-05-11 00:54:58.000000 logmaster-1.0.3/logmaster/logmaster.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      214 2023-05-11 00:54:58.000000 logmaster-1.0.3/logmaster/logmaster.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-11 00:54:58.000000 logmaster-1.0.3/logmaster/logmaster.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        1 2023-05-11 00:54:58.000000 logmaster-1.0.3/logmaster/logmaster.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      109 2023-05-09 16:02:47.000000 logmaster-1.0.3/pyproject.toml
--rw-rw-rw-   0        0        0      644 2023-05-11 00:54:58.446198 logmaster-1.0.3/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-11 16:08:17.927127 logmaster-1.0.4/
+-rw-rw-rw-   0        0        0     1083 2023-05-08 22:14:25.000000 logmaster-1.0.4/LICENSE
+-rw-rw-rw-   0        0        0     1511 2023-05-11 16:08:17.927127 logmaster-1.0.4/PKG-INFO
+-rw-rw-rw-   0        0        0     1031 2023-05-11 15:57:31.000000 logmaster-1.0.4/README.md
+drwxrwxrwx   0        0        0        0 2023-05-11 16:08:17.879128 logmaster-1.0.4/logmaster/
+drwxrwxrwx   0        0        0        0 2023-05-11 16:08:17.927127 logmaster-1.0.4/logmaster/logmaster.egg-info/
+-rw-rw-rw-   0        0        0     1511 2023-05-11 16:08:17.000000 logmaster-1.0.4/logmaster/logmaster.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      214 2023-05-11 16:08:17.000000 logmaster-1.0.4/logmaster/logmaster.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-11 16:08:17.000000 logmaster-1.0.4/logmaster/logmaster.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        1 2023-05-11 16:08:17.000000 logmaster-1.0.4/logmaster/logmaster.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      109 2023-05-09 16:02:47.000000 logmaster-1.0.4/pyproject.toml
+-rw-rw-rw-   0        0        0      614 2023-05-11 16:08:17.935122 logmaster-1.0.4/setup.cfg
```

### Comparing `logmaster-1.0.3/LICENSE` & `logmaster-1.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `logmaster-1.0.3/PKG-INFO` & `logmaster-1.0.4/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,24 +1,26 @@
 Metadata-Version: 2.1
 Name: logmaster
-Version: 1.0.3
+Version: 1.0.4
 Summary: A simple logging library for Python
 Home-page: https://github.com/W1L7dev/Logmaster
 Author: W1L7dev
 Author-email: w1l7dev@gmail.com
 Keywords: logmaster,logging,log,logger
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Logmaster
-## A simple logging package for Python
+## A simple logging package for
+
+
 ---
 
 ### Installation
 ```bash
 pip install logmaster
 ```
 > note: this package is not yet on PyPI, so you will have to install it from source.
```

### Comparing `logmaster-1.0.3/README.md` & `logmaster-1.0.4/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -1,9 +1,11 @@
 # Logmaster
-## A simple logging package for Python
+## A simple logging package for
+
+
 ---
 
 ### Installation
 ```bash
 pip install logmaster
 ```
 > note: this package is not yet on PyPI, so you will have to install it from source.
```

### Comparing `logmaster-1.0.3/logmaster/logmaster.egg-info/PKG-INFO` & `logmaster-1.0.4/logmaster/logmaster.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,24 +1,26 @@
 Metadata-Version: 2.1
 Name: logmaster
-Version: 1.0.3
+Version: 1.0.4
 Summary: A simple logging library for Python
 Home-page: https://github.com/W1L7dev/Logmaster
 Author: W1L7dev
 Author-email: w1l7dev@gmail.com
 Keywords: logmaster,logging,log,logger
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Logmaster
-## A simple logging package for Python
+## A simple logging package for
+
+
 ---
 
 ### Installation
 ```bash
 pip install logmaster
 ```
 > note: this package is not yet on PyPI, so you will have to install it from source.
```

### Comparing `logmaster-1.0.3/setup.cfg` & `logmaster-1.0.4/setup.cfg`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 206c 6f67 6d61 7374 6572 0d0a 7665   = logmaster..ve
-00000020: 7273 696f 6e20 3d20 312e 302e 330d 0a61  rsion = 1.0.3..a
+00000020: 7273 696f 6e20 3d20 312e 302e 340d 0a61  rsion = 1.0.4..a
 00000030: 7574 686f 7220 3d20 5731 4c37 6465 760d  uthor = W1L7dev.
 00000040: 0a61 7574 686f 725f 656d 6169 6c20 3d20  .author_email = 
 00000050: 7731 6c37 6465 7640 676d 6169 6c2e 636f  w1l7dev@gmail.co
 00000060: 6d0d 0a64 6573 6372 6970 7469 6f6e 203d  m..description =
 00000070: 2041 2073 696d 706c 6520 6c6f 6767 696e   A simple loggin
 00000080: 6720 6c69 6272 6172 7920 666f 7220 5079  g library for Py
 00000090: 7468 6f6e 0d0a 6c6f 6e67 5f64 6573 6372  thon..long_descr
@@ -24,18 +24,16 @@
 00000170: 6775 6167 6520 3a3a 2050 7974 686f 6e20  guage :: Python 
 00000180: 3a3a 2033 0d0a 094c 6963 656e 7365 203a  :: 3...License :
 00000190: 3a20 4f53 4920 4170 7072 6f76 6564 203a  : OSI Approved :
 000001a0: 3a20 4d49 5420 4c69 6365 6e73 650d 0a09  : MIT License...
 000001b0: 4f70 6572 6174 696e 6720 5379 7374 656d  Operating System
 000001c0: 203a 3a20 4f53 2049 6e64 6570 656e 6465   :: OS Independe
 000001d0: 6e74 0d0a 0d0a 5b6f 7074 696f 6e73 5d0d  nt....[options].
-000001e0: 0a70 6163 6b61 6765 5f64 6972 203d 200d  .package_dir = .
-000001f0: 0a09 3d20 6c6f 676d 6173 7465 720d 0a70  ..= logmaster..p
-00000200: 6163 6b61 6765 7320 3d20 6669 6e64 3a0d  ackages = find:.
-00000210: 0a70 7974 686f 6e5f 7265 7175 6972 6573  .python_requires
-00000220: 203d 203e 3d33 2e37 0d0a 0d0a 5b6f 7074   = >=3.7....[opt
-00000230: 696f 6e73 2e70 6163 6b61 6765 732e 6669  ions.packages.fi
-00000240: 6e64 5d0d 0a77 6865 7265 203d 206c 6f67  nd]..where = log
-00000250: 6d61 7374 6572 0d0a 0d0a 5b65 6767 5f69  master....[egg_i
-00000260: 6e66 6f5d 0d0a 7461 675f 6275 696c 6420  nfo]..tag_build 
-00000270: 3d20 0d0a 7461 675f 6461 7465 203d 2030  = ..tag_date = 0
-00000280: 0d0a 0d0a                                ....
+000001e0: 0a70 6163 6b61 6765 7320 3d20 6669 6e64  .packages = find
+000001f0: 3a0d 0a70 7974 686f 6e5f 7265 7175 6972  :..python_requir
+00000200: 6573 203d 203e 3d33 2e37 0d0a 0d0a 5b6f  es = >=3.7....[o
+00000210: 7074 696f 6e73 2e70 6163 6b61 6765 732e  ptions.packages.
+00000220: 6669 6e64 5d0d 0a77 6865 7265 203d 206c  find]..where = l
+00000230: 6f67 6d61 7374 6572 0d0a 0d0a 5b65 6767  ogmaster....[egg
+00000240: 5f69 6e66 6f5d 0d0a 7461 675f 6275 696c  _info]..tag_buil
+00000250: 6420 3d20 0d0a 7461 675f 6461 7465 203d  d = ..tag_date =
+00000260: 2030 0d0a 0d0a                            0....
```

