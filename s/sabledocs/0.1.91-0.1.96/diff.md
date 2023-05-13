# Comparing `tmp/sabledocs-0.1.91.tar.gz` & `tmp/sabledocs-0.1.96.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sabledocs-0.1.91.tar", last modified: Sun Apr 16 21:33:52 2023, max compression
+gzip compressed data, was "sabledocs-0.1.96.tar", last modified: Sun Apr 16 21:35:38 2023, max compression
```

## Comparing `sabledocs-0.1.91.tar` & `sabledocs-0.1.96.tar`

### file list

```diff
@@ -1,31 +1,31 @@
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:33:52.289291 sabledocs-0.1.91/
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1078 2023-04-16 21:33:41.000000 sabledocs-0.1.91/LICENSE
--rw-r--r--   0 circleci  (1001) circleci  (1002)       44 2023-04-16 21:33:41.000000 sabledocs-0.1.91/MANIFEST.in
--rw-r--r--   0 circleci  (1001) circleci  (1002)     3857 2023-04-16 21:33:52.289291 sabledocs-0.1.91/PKG-INFO
--rw-r--r--   0 circleci  (1001) circleci  (1002)     3321 2023-04-16 21:33:41.000000 sabledocs-0.1.91/README.md
--rw-r--r--   0 circleci  (1001) circleci  (1002)      776 2023-04-16 21:33:41.000000 sabledocs-0.1.91/pyproject.toml
--rw-r--r--   0 circleci  (1001) circleci  (1002)       73 2023-04-16 21:33:52.289291 sabledocs-0.1.91/setup.cfg
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:33:52.285292 sabledocs-0.1.91/src/
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:33:52.289291 sabledocs-0.1.91/src/sabledocs/
--rw-r--r--   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/__init__.py
--rw-r--r--   0 circleci  (1001) circleci  (1002)     2227 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/__main__.py
--rw-r--r--   0 circleci  (1001) circleci  (1002)    13639 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/proto_descriptor_parser.py
--rw-r--r--   0 circleci  (1001) circleci  (1002)     2719 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/proto_model.py
--rw-r--r--   0 circleci  (1001) circleci  (1002)     2269 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/sable_config.py
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:33:52.285292 sabledocs-0.1.91/src/sabledocs/templates/
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:33:52.289291 sabledocs-0.1.91/src/sabledocs/templates/_default/
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1850 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/templates/_default/base.html
--rw-r--r--   0 circleci  (1001) circleci  (1002)      826 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/templates/_default/enum.html
--rw-r--r--   0 circleci  (1001) circleci  (1002)      528 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/templates/_default/index.html
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1399 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/templates/_default/message.html
--rw-r--r--   0 circleci  (1001) circleci  (1002)     1889 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/templates/_default/package.html
--rw-r--r--   0 circleci  (1001) circleci  (1002)      815 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/templates/_default/service.html
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:33:52.289291 sabledocs-0.1.91/src/sabledocs/templates/_default/static/
--rw-r--r--   0 circleci  (1001) circleci  (1002)   257737 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/templates/_default/static/mystyles.css
--rw-r--r--   0 circleci  (1001) circleci  (1002)      560 2023-04-16 21:33:41.000000 sabledocs-0.1.91/src/sabledocs/templates/_default/type_name.html
-drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:33:52.289291 sabledocs-0.1.91/src/sabledocs.egg-info/
--rw-r--r--   0 circleci  (1001) circleci  (1002)     3857 2023-04-16 21:33:52.000000 sabledocs-0.1.91/src/sabledocs.egg-info/PKG-INFO
--rw-r--r--   0 circleci  (1001) circleci  (1002)      763 2023-04-16 21:33:52.000000 sabledocs-0.1.91/src/sabledocs.egg-info/SOURCES.txt
--rw-r--r--   0 circleci  (1001) circleci  (1002)        1 2023-04-16 21:33:52.000000 sabledocs-0.1.91/src/sabledocs.egg-info/dependency_links.txt
--rw-r--r--   0 circleci  (1001) circleci  (1002)       53 2023-04-16 21:33:52.000000 sabledocs-0.1.91/src/sabledocs.egg-info/entry_points.txt
--rw-r--r--   0 circleci  (1001) circleci  (1002)       10 2023-04-16 21:33:52.000000 sabledocs-0.1.91/src/sabledocs.egg-info/top_level.txt
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:35:38.872708 sabledocs-0.1.96/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1078 2023-04-16 21:35:27.000000 sabledocs-0.1.96/LICENSE
+-rw-r--r--   0 circleci  (1001) circleci  (1002)       44 2023-04-16 21:35:27.000000 sabledocs-0.1.96/MANIFEST.in
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     3968 2023-04-16 21:35:38.872708 sabledocs-0.1.96/PKG-INFO
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     3432 2023-04-16 21:35:27.000000 sabledocs-0.1.96/README.md
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      776 2023-04-16 21:35:27.000000 sabledocs-0.1.96/pyproject.toml
+-rw-r--r--   0 circleci  (1001) circleci  (1002)       73 2023-04-16 21:35:38.872708 sabledocs-0.1.96/setup.cfg
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:35:38.868708 sabledocs-0.1.96/src/
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:35:38.872708 sabledocs-0.1.96/src/sabledocs/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/__init__.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     2227 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/__main__.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)    13639 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/proto_descriptor_parser.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     2719 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/proto_model.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     2269 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/sable_config.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:35:38.868708 sabledocs-0.1.96/src/sabledocs/templates/
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:35:38.872708 sabledocs-0.1.96/src/sabledocs/templates/_default/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1850 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/templates/_default/base.html
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      826 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/templates/_default/enum.html
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      528 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/templates/_default/index.html
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1399 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/templates/_default/message.html
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1889 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/templates/_default/package.html
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      815 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/templates/_default/service.html
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:35:38.872708 sabledocs-0.1.96/src/sabledocs/templates/_default/static/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)   257737 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/templates/_default/static/mystyles.css
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      560 2023-04-16 21:35:27.000000 sabledocs-0.1.96/src/sabledocs/templates/_default/type_name.html
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2023-04-16 21:35:38.872708 sabledocs-0.1.96/src/sabledocs.egg-info/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     3968 2023-04-16 21:35:38.000000 sabledocs-0.1.96/src/sabledocs.egg-info/PKG-INFO
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      763 2023-04-16 21:35:38.000000 sabledocs-0.1.96/src/sabledocs.egg-info/SOURCES.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)        1 2023-04-16 21:35:38.000000 sabledocs-0.1.96/src/sabledocs.egg-info/dependency_links.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)       53 2023-04-16 21:35:38.000000 sabledocs-0.1.96/src/sabledocs.egg-info/entry_points.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)       10 2023-04-16 21:35:38.000000 sabledocs-0.1.96/src/sabledocs.egg-info/top_level.txt
```

### Comparing `sabledocs-0.1.91/LICENSE` & `sabledocs-0.1.96/LICENSE`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/PKG-INFO` & `sabledocs-0.1.96/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,25 +1,26 @@
 Metadata-Version: 2.1
 Name: sabledocs
-Version: 0.1.91
+Version: 0.1.96
 Summary: Static documentation generator for Protobuf and gRPC
 Author-email: Mark Vincze <mrk.vincze@gmail.com>
 Project-URL: Homepage, https://github.com/markvincze/sabledocs
 Project-URL: Bug Tracker, https://github.com/markvincze/sabledocs/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.11.0
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-[# Sabledocs](https://markvincze.github.io/sabledocs/)
+# [Sabledocs](https://markvincze.github.io/sabledocs/)
 
 [![CircleCI](https://dl.circleci.com/status-badge/img/gh/markvincze/sabledocs/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/markvincze/sabledocs/tree/main)
 [![PyPi](https://img.shields.io/pypi/v/sabledocs.svg)](https://pypi.org/project/sabledocs/)
+[![Python versions](https://img.shields.io/pypi/pyversions/Markdown.svg)](https://pypi.org/project/sabledocs/)
 
 A simple static documentation generator for Protobuf and gRPC contracts.
 
 **Demo**: You can check out this [demo](https://markvincze.github.io/sabledocs/demo/) showing the generated documentation for the [Google Cloud Pub/Sub contracts](https://github.com/googleapis/googleapis/tree/master/google/pubsub/v1).
 
 ## How to use
```

### Comparing `sabledocs-0.1.91/README.md` & `sabledocs-0.1.96/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,12 @@
-[# Sabledocs](https://markvincze.github.io/sabledocs/)
+# [Sabledocs](https://markvincze.github.io/sabledocs/)
 
 [![CircleCI](https://dl.circleci.com/status-badge/img/gh/markvincze/sabledocs/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/markvincze/sabledocs/tree/main)
 [![PyPi](https://img.shields.io/pypi/v/sabledocs.svg)](https://pypi.org/project/sabledocs/)
+[![Python versions](https://img.shields.io/pypi/pyversions/Markdown.svg)](https://pypi.org/project/sabledocs/)
 
 A simple static documentation generator for Protobuf and gRPC contracts.
 
 **Demo**: You can check out this [demo](https://markvincze.github.io/sabledocs/demo/) showing the generated documentation for the [Google Cloud Pub/Sub contracts](https://github.com/googleapis/googleapis/tree/master/google/pubsub/v1).
 
 ## How to use
```

### Comparing `sabledocs-0.1.91/pyproject.toml` & `sabledocs-0.1.96/pyproject.toml`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/__main__.py` & `sabledocs-0.1.96/src/sabledocs/__main__.py`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/proto_descriptor_parser.py` & `sabledocs-0.1.96/src/sabledocs/proto_descriptor_parser.py`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/proto_model.py` & `sabledocs-0.1.96/src/sabledocs/proto_model.py`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/sable_config.py` & `sabledocs-0.1.96/src/sabledocs/sable_config.py`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/templates/_default/base.html` & `sabledocs-0.1.96/src/sabledocs/templates/_default/base.html`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/templates/_default/enum.html` & `sabledocs-0.1.96/src/sabledocs/templates/_default/enum.html`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/templates/_default/index.html` & `sabledocs-0.1.96/src/sabledocs/templates/_default/index.html`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/templates/_default/message.html` & `sabledocs-0.1.96/src/sabledocs/templates/_default/message.html`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/templates/_default/package.html` & `sabledocs-0.1.96/src/sabledocs/templates/_default/package.html`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/templates/_default/service.html` & `sabledocs-0.1.96/src/sabledocs/templates/_default/service.html`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/templates/_default/static/mystyles.css` & `sabledocs-0.1.96/src/sabledocs/templates/_default/static/mystyles.css`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs/templates/_default/type_name.html` & `sabledocs-0.1.96/src/sabledocs/templates/_default/type_name.html`

 * *Files identical despite different names*

### Comparing `sabledocs-0.1.91/src/sabledocs.egg-info/PKG-INFO` & `sabledocs-0.1.96/src/sabledocs.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,25 +1,26 @@
 Metadata-Version: 2.1
 Name: sabledocs
-Version: 0.1.91
+Version: 0.1.96
 Summary: Static documentation generator for Protobuf and gRPC
 Author-email: Mark Vincze <mrk.vincze@gmail.com>
 Project-URL: Homepage, https://github.com/markvincze/sabledocs
 Project-URL: Bug Tracker, https://github.com/markvincze/sabledocs/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.11.0
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-[# Sabledocs](https://markvincze.github.io/sabledocs/)
+# [Sabledocs](https://markvincze.github.io/sabledocs/)
 
 [![CircleCI](https://dl.circleci.com/status-badge/img/gh/markvincze/sabledocs/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/markvincze/sabledocs/tree/main)
 [![PyPi](https://img.shields.io/pypi/v/sabledocs.svg)](https://pypi.org/project/sabledocs/)
+[![Python versions](https://img.shields.io/pypi/pyversions/Markdown.svg)](https://pypi.org/project/sabledocs/)
 
 A simple static documentation generator for Protobuf and gRPC contracts.
 
 **Demo**: You can check out this [demo](https://markvincze.github.io/sabledocs/demo/) showing the generated documentation for the [Google Cloud Pub/Sub contracts](https://github.com/googleapis/googleapis/tree/master/google/pubsub/v1).
 
 ## How to use
```

### Comparing `sabledocs-0.1.91/src/sabledocs.egg-info/SOURCES.txt` & `sabledocs-0.1.96/src/sabledocs.egg-info/SOURCES.txt`

 * *Files identical despite different names*

