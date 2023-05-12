# Comparing `tmp/throne-0.5.1.tar.gz` & `tmp/throne-0.6.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "throne-0.5.1.tar", last modified: Wed Mar  8 19:36:51 2023, max compression
+gzip compressed data, was "throne-0.6.1.tar", last modified: Fri May 12 23:23:41 2023, max compression
```

## Comparing `throne-0.5.1.tar` & `throne-0.6.1.tar`

### file list

```diff
@@ -1,29 +1,27 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-08 19:36:51.814396 throne-0.5.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-03-08 19:36:38.000000 throne-0.5.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2449 2023-03-08 19:36:51.814396 throne-0.5.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2142 2023-03-08 19:36:38.000000 throne-0.5.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-08 19:36:51.810396 throne-0.5.1/bin/
--rw-r--r--   0 runner    (1001) docker     (123)      968 2023-03-08 19:36:38.000000 throne-0.5.1/bin/throne.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-03-08 19:36:51.814396 throne-0.5.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      743 2023-03-08 19:36:38.000000 throne-0.5.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-08 19:36:51.814396 throne-0.5.1/src/
--rw-r--r--   0 runner    (1001) docker     (123)     3244 2023-03-08 19:36:38.000000 throne-0.5.1/src/api.py
--rw-r--r--   0 runner    (1001) docker     (123)     7477 2023-03-08 19:36:38.000000 throne-0.5.1/src/bgp.py
--rw-r--r--   0 runner    (1001) docker     (123)      866 2023-03-08 19:36:38.000000 throne-0.5.1/src/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     7118 2023-03-08 19:36:38.000000 throne-0.5.1/src/ip.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-08 19:36:51.814396 throne-0.5.1/src/parsers/
--rw-r--r--   0 runner    (1001) docker     (123)     1193 2023-03-08 19:36:38.000000 throne-0.5.1/src/parsers/json_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     8089 2023-03-08 19:36:38.000000 throne-0.5.1/src/parsers/lg_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)    10703 2023-03-08 19:36:38.000000 throne-0.5.1/src/parsers/rdap_asn_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)    13161 2023-03-08 19:36:38.000000 throne-0.5.1/src/parsers/rdap_ip_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     9124 2023-03-08 19:36:38.000000 throne-0.5.1/src/parsers/shodan_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     5871 2023-03-08 19:36:38.000000 throne-0.5.1/src/peeringdb.py
--rw-r--r--   0 runner    (1001) docker     (123)    17525 2023-03-08 19:36:38.000000 throne-0.5.1/src/shodan.py
--rw-r--r--   0 runner    (1001) docker     (123)     7767 2023-03-08 19:36:38.000000 throne-0.5.1/src/whois.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-08 19:36:51.814396 throne-0.5.1/throne.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2449 2023-03-08 19:36:51.000000 throne-0.5.1/throne.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      459 2023-03-08 19:36:51.000000 throne-0.5.1/throne.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-08 19:36:51.000000 throne-0.5.1/throne.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       42 2023-03-08 19:36:51.000000 throne-0.5.1/throne.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       31 2023-03-08 19:36:51.000000 throne-0.5.1/throne.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-03-08 19:36:51.000000 throne-0.5.1/throne.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:23:41.427134 throne-0.6.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-05-12 23:23:31.000000 throne-0.6.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2449 2023-05-12 23:23:41.427134 throne-0.6.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2142 2023-05-12 23:23:31.000000 throne-0.6.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:23:41.423134 throne-0.6.1/bin/
+-rw-r--r--   0 runner    (1001) docker     (123)      968 2023-05-12 23:23:31.000000 throne-0.6.1/bin/throne.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 23:23:41.427134 throne-0.6.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      743 2023-05-12 23:23:31.000000 throne-0.6.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:23:41.423134 throne-0.6.1/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     3244 2023-05-12 23:23:31.000000 throne-0.6.1/src/api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7477 2023-05-12 23:23:31.000000 throne-0.6.1/src/bgp.py
+-rw-r--r--   0 runner    (1001) docker     (123)      866 2023-05-12 23:23:31.000000 throne-0.6.1/src/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5704 2023-05-12 23:23:31.000000 throne-0.6.1/src/ip.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:23:41.423134 throne-0.6.1/src/parsers/
+-rw-r--r--   0 runner    (1001) docker     (123)     1193 2023-05-12 23:23:31.000000 throne-0.6.1/src/parsers/json_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8089 2023-05-12 23:23:31.000000 throne-0.6.1/src/parsers/lg_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9124 2023-05-12 23:23:31.000000 throne-0.6.1/src/parsers/shodan_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5871 2023-05-12 23:23:31.000000 throne-0.6.1/src/peeringdb.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17525 2023-05-12 23:23:31.000000 throne-0.6.1/src/shodan.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7767 2023-05-12 23:23:31.000000 throne-0.6.1/src/whois.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 23:23:41.427134 throne-0.6.1/throne.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2449 2023-05-12 23:23:41.000000 throne-0.6.1/throne.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-12 23:23:41.000000 throne-0.6.1/throne.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 23:23:41.000000 throne-0.6.1/throne.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       42 2023-05-12 23:23:41.000000 throne-0.6.1/throne.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-05-12 23:23:41.000000 throne-0.6.1/throne.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-12 23:23:41.000000 throne-0.6.1/throne.egg-info/top_level.txt
```

### Comparing `throne-0.5.1/LICENSE` & `throne-0.6.1/LICENSE`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 The Clear BSD License
 
-Copyright (c) 2021 Throne, LLC
+Copyright (c) 2023 Throne, LLC
 All rights reserved.
 
 Redistribution and use in source and binary forms, with or without
 modification, are permitted (subject to the limitations in the disclaimer
 below) provided that the following conditions are met:
 
      * Redistributions of source code must retain the above copyright notice,
```

### Comparing `throne-0.5.1/PKG-INFO` & `throne-0.6.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: throne
-Version: 0.5.1
+Version: 0.6.1
 Summary: Watch the internet from up on your throne.
 Home-page: https://github.com/throne/throne-cli/
 Author: throne:shrunbr
 Author-email: shrunbr@throne.dev
 License: BSD 3-Clause Clear License
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `throne-0.5.1/README.md` & `throne-0.6.1/README.md`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/bin/throne.py` & `throne-0.6.1/bin/throne.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/setup.py` & `throne-0.6.1/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from setuptools import setup
 
 parent_dir = pathlib.Path(__file__).parent
 README = (parent_dir / "README.md").read_text()
 
 setup(
     name='throne',
-    version='0.5.1',
+    version='0.6.1',
     author='throne:shrunbr',
     author_email='shrunbr@throne.dev',
     url='https://github.com/throne/throne-cli/',
     description='Watch the internet from up on your throne.',
     long_description=README,
     long_description_content_type="text/markdown",
     license="BSD 3-Clause Clear License",
```

### Comparing `throne-0.5.1/src/api.py` & `throne-0.6.1/src/api.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/src/bgp.py` & `throne-0.6.1/src/bgp.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/src/exceptions.py` & `throne-0.6.1/src/exceptions.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/src/parsers/json_request.py` & `throne-0.6.1/src/parsers/json_request.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/src/parsers/lg_parser.py` & `throne-0.6.1/src/parsers/lg_parser.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/src/parsers/shodan_parser.py` & `throne-0.6.1/src/parsers/shodan_parser.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/src/peeringdb.py` & `throne-0.6.1/src/peeringdb.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/src/shodan.py` & `throne-0.6.1/src/shodan.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/src/whois.py` & `throne-0.6.1/src/whois.py`

 * *Files identical despite different names*

### Comparing `throne-0.5.1/throne.egg-info/PKG-INFO` & `throne-0.6.1/throne.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: throne
-Version: 0.5.1
+Version: 0.6.1
 Summary: Watch the internet from up on your throne.
 Home-page: https://github.com/throne/throne-cli/
 Author: throne:shrunbr
 Author-email: shrunbr@throne.dev
 License: BSD 3-Clause Clear License
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

