# Comparing `tmp/logmaster-1.0.4.tar.gz` & `tmp/logmaster-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "logmaster-1.0.4.tar", last modified: Thu May 11 16:08:17 2023, max compression
+gzip compressed data, was "logmaster-1.0.5.tar", last modified: Sat May 13 19:46:36 2023, max compression
```

## Comparing `logmaster-1.0.4.tar` & `logmaster-1.0.5.tar`

### file list

```diff
@@ -1,12 +1,12 @@
-drwxrwxrwx   0        0        0        0 2023-05-11 16:08:17.927127 logmaster-1.0.4/
--rw-rw-rw-   0        0        0     1083 2023-05-08 22:14:25.000000 logmaster-1.0.4/LICENSE
--rw-rw-rw-   0        0        0     1511 2023-05-11 16:08:17.927127 logmaster-1.0.4/PKG-INFO
--rw-rw-rw-   0        0        0     1031 2023-05-11 15:57:31.000000 logmaster-1.0.4/README.md
-drwxrwxrwx   0        0        0        0 2023-05-11 16:08:17.879128 logmaster-1.0.4/logmaster/
-drwxrwxrwx   0        0        0        0 2023-05-11 16:08:17.927127 logmaster-1.0.4/logmaster/logmaster.egg-info/
--rw-rw-rw-   0        0        0     1511 2023-05-11 16:08:17.000000 logmaster-1.0.4/logmaster/logmaster.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      214 2023-05-11 16:08:17.000000 logmaster-1.0.4/logmaster/logmaster.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-11 16:08:17.000000 logmaster-1.0.4/logmaster/logmaster.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        1 2023-05-11 16:08:17.000000 logmaster-1.0.4/logmaster/logmaster.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      109 2023-05-09 16:02:47.000000 logmaster-1.0.4/pyproject.toml
--rw-rw-rw-   0        0        0      614 2023-05-11 16:08:17.935122 logmaster-1.0.4/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 19:46:36.017525 logmaster-1.0.5/
+-rw-rw-rw-   0        0        0     1083 2023-05-08 22:14:25.000000 logmaster-1.0.5/LICENSE
+-rw-rw-rw-   0        0        0     1511 2023-05-13 19:46:36.018525 logmaster-1.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0     1031 2023-05-11 15:57:31.000000 logmaster-1.0.5/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 19:46:35.959518 logmaster-1.0.5/logmaster/
+drwxrwxrwx   0        0        0        0 2023-05-13 19:46:36.009527 logmaster-1.0.5/logmaster/logmaster.egg-info/
+-rw-rw-rw-   0        0        0     1511 2023-05-13 19:46:35.000000 logmaster-1.0.5/logmaster/logmaster.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      214 2023-05-13 19:46:35.000000 logmaster-1.0.5/logmaster/logmaster.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 19:46:35.000000 logmaster-1.0.5/logmaster/logmaster.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 19:46:35.000000 logmaster-1.0.5/logmaster/logmaster.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      109 2023-05-09 16:02:47.000000 logmaster-1.0.5/pyproject.toml
+-rw-rw-rw-   0        0        0      614 2023-05-13 19:46:36.022519 logmaster-1.0.5/setup.cfg
```

### Comparing `logmaster-1.0.4/LICENSE` & `logmaster-1.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `logmaster-1.0.4/PKG-INFO` & `logmaster-1.0.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: logmaster
-Version: 1.0.4
+Version: 1.0.5
 Summary: A simple logging library for Python
 Home-page: https://github.com/W1L7dev/Logmaster
 Author: W1L7dev
 Author-email: w1l7dev@gmail.com
 Keywords: logmaster,logging,log,logger
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `logmaster-1.0.4/README.md` & `logmaster-1.0.5/README.md`

 * *Files identical despite different names*

### Comparing `logmaster-1.0.4/logmaster/logmaster.egg-info/PKG-INFO` & `logmaster-1.0.5/logmaster/logmaster.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: logmaster
-Version: 1.0.4
+Version: 1.0.5
 Summary: A simple logging library for Python
 Home-page: https://github.com/W1L7dev/Logmaster
 Author: W1L7dev
 Author-email: w1l7dev@gmail.com
 Keywords: logmaster,logging,log,logger
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `logmaster-1.0.4/setup.cfg` & `logmaster-1.0.5/setup.cfg`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 206c 6f67 6d61 7374 6572 0d0a 7665   = logmaster..ve
-00000020: 7273 696f 6e20 3d20 312e 302e 340d 0a61  rsion = 1.0.4..a
+00000020: 7273 696f 6e20 3d20 312e 302e 350d 0a61  rsion = 1.0.5..a
 00000030: 7574 686f 7220 3d20 5731 4c37 6465 760d  uthor = W1L7dev.
 00000040: 0a61 7574 686f 725f 656d 6169 6c20 3d20  .author_email = 
 00000050: 7731 6c37 6465 7640 676d 6169 6c2e 636f  w1l7dev@gmail.co
 00000060: 6d0d 0a64 6573 6372 6970 7469 6f6e 203d  m..description =
 00000070: 2041 2073 696d 706c 6520 6c6f 6767 696e   A simple loggin
 00000080: 6720 6c69 6272 6172 7920 666f 7220 5079  g library for Py
 00000090: 7468 6f6e 0d0a 6c6f 6e67 5f64 6573 6372  thon..long_descr
```

