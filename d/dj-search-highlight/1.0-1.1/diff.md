# Comparing `tmp/dj_search_highlight-1.0.tar.gz` & `tmp/dj_search_highlight-1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dj_search_highlight-1.0.tar", last modified: Sat May 13 09:58:36 2023, max compression
+gzip compressed data, was "dj_search_highlight-1.1.tar", last modified: Sat May 13 11:06:33 2023, max compression
```

## Comparing `dj_search_highlight-1.0.tar` & `dj_search_highlight-1.1.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 09:58:36.005643 dj_search_highlight-1.0/
--rw-rw-rw-   0        0        0       12 2023-05-13 09:52:29.000000 dj_search_highlight-1.0/LICENSE
--rw-rw-rw-   0        0        0       35 2023-05-13 09:52:29.000000 dj_search_highlight-1.0/MANIFEST.in
--rw-rw-rw-   0        0        0      999 2023-05-13 09:58:36.005643 dj_search_highlight-1.0/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 09:58:36.005643 dj_search_highlight-1.0/dj_search_highlight.egg-info/
--rw-rw-rw-   0        0        0      999 2023-05-13 09:58:35.000000 dj_search_highlight-1.0/dj_search_highlight.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      469 2023-05-13 09:58:35.000000 dj_search_highlight-1.0/dj_search_highlight.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 09:58:35.000000 dj_search_highlight-1.0/dj_search_highlight.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       12 2023-05-13 09:58:35.000000 dj_search_highlight-1.0/dj_search_highlight.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-05-13 09:58:36.005643 dj_search_highlight-1.0/highlighter/
--rw-rw-rw-   0        0        0        0 2023-05-13 09:31:06.000000 dj_search_highlight-1.0/highlighter/__init__.py
--rw-rw-rw-   0        0        0       66 2023-05-13 09:31:06.000000 dj_search_highlight-1.0/highlighter/admin.py
--rw-rw-rw-   0        0        0      180 2023-05-13 09:42:01.000000 dj_search_highlight-1.0/highlighter/apps.py
-drwxrwxrwx   0        0        0        0 2023-05-13 09:58:36.005643 dj_search_highlight-1.0/highlighter/migrations/
--rw-rw-rw-   0        0        0        0 2023-05-13 09:31:06.000000 dj_search_highlight-1.0/highlighter/migrations/__init__.py
--rw-rw-rw-   0        0        0       60 2023-05-13 09:31:06.000000 dj_search_highlight-1.0/highlighter/models.py
-drwxrwxrwx   0        0        0        0 2023-05-13 09:58:36.005643 dj_search_highlight-1.0/highlighter/templatetags/
--rw-rw-rw-   0        0        0        0 2023-05-13 09:27:19.000000 dj_search_highlight-1.0/highlighter/templatetags/__init__.py
--rw-rw-rw-   0        0        0      445 2023-05-13 09:30:46.000000 dj_search_highlight-1.0/highlighter/templatetags/search_highlighter.py
--rw-rw-rw-   0        0        0       63 2023-05-13 09:31:06.000000 dj_search_highlight-1.0/highlighter/tests.py
--rw-rw-rw-   0        0        0       66 2023-05-13 09:31:06.000000 dj_search_highlight-1.0/highlighter/views.py
--rw-rw-rw-   0        0        0       71 2023-05-13 09:42:01.000000 dj_search_highlight-1.0/readme.rst
--rw-rw-rw-   0        0        0      946 2023-05-13 09:58:36.005643 dj_search_highlight-1.0/setup.cfg
--rw-rw-rw-   0        0        0       41 2023-05-13 09:52:29.000000 dj_search_highlight-1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:06:33.810221 dj_search_highlight-1.1/
+-rw-rw-rw-   0        0        0       12 2023-05-13 09:52:29.000000 dj_search_highlight-1.1/LICENSE
+-rw-rw-rw-   0        0        0       35 2023-05-13 09:52:29.000000 dj_search_highlight-1.1/MANIFEST.in
+-rw-rw-rw-   0        0        0      999 2023-05-13 11:06:33.811210 dj_search_highlight-1.1/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 11:06:33.801010 dj_search_highlight-1.1/dj_search_highlight.egg-info/
+-rw-rw-rw-   0        0        0      999 2023-05-13 11:06:33.000000 dj_search_highlight-1.1/dj_search_highlight.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      469 2023-05-13 11:06:33.000000 dj_search_highlight-1.1/dj_search_highlight.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 11:06:33.000000 dj_search_highlight-1.1/dj_search_highlight.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       12 2023-05-13 11:06:33.000000 dj_search_highlight-1.1/dj_search_highlight.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 11:06:33.807211 dj_search_highlight-1.1/highlighter/
+-rw-rw-rw-   0        0        0        0 2023-05-13 09:31:06.000000 dj_search_highlight-1.1/highlighter/__init__.py
+-rw-rw-rw-   0        0        0       66 2023-05-13 09:31:06.000000 dj_search_highlight-1.1/highlighter/admin.py
+-rw-rw-rw-   0        0        0      160 2023-05-13 11:02:12.000000 dj_search_highlight-1.1/highlighter/apps.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:06:33.808210 dj_search_highlight-1.1/highlighter/migrations/
+-rw-rw-rw-   0        0        0        0 2023-05-13 09:31:06.000000 dj_search_highlight-1.1/highlighter/migrations/__init__.py
+-rw-rw-rw-   0        0        0       60 2023-05-13 09:31:06.000000 dj_search_highlight-1.1/highlighter/models.py
+drwxrwxrwx   0        0        0        0 2023-05-13 11:06:33.809235 dj_search_highlight-1.1/highlighter/templatetags/
+-rw-rw-rw-   0        0        0        0 2023-05-13 09:27:19.000000 dj_search_highlight-1.1/highlighter/templatetags/__init__.py
+-rw-rw-rw-   0        0        0      445 2023-05-13 09:30:46.000000 dj_search_highlight-1.1/highlighter/templatetags/search_highlighter.py
+-rw-rw-rw-   0        0        0       63 2023-05-13 09:31:06.000000 dj_search_highlight-1.1/highlighter/tests.py
+-rw-rw-rw-   0        0        0       66 2023-05-13 09:31:06.000000 dj_search_highlight-1.1/highlighter/views.py
+-rw-rw-rw-   0        0        0       71 2023-05-13 09:42:01.000000 dj_search_highlight-1.1/readme.rst
+-rw-rw-rw-   0        0        0      946 2023-05-13 11:06:33.813215 dj_search_highlight-1.1/setup.cfg
+-rw-rw-rw-   0        0        0       41 2023-05-13 09:52:29.000000 dj_search_highlight-1.1/setup.py
```

### Comparing `dj_search_highlight-1.0/PKG-INFO` & `dj_search_highlight-1.1/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dj_search_highlight
-Version: 1.0
+Version: 1.1
 Summary: Highlight string in the text.
 Home-page: https://medium.com/@sevdimali
 Author: Sevdimali Isayev
 Author-email: sevdimaliisa@gmail.com
 License: MIT
 Keywords: django highlight
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `dj_search_highlight-1.0/dj_search_highlight.egg-info/PKG-INFO` & `dj_search_highlight-1.1/dj_search_highlight.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dj-search-highlight
-Version: 1.0
+Version: 1.1
 Summary: Highlight string in the text.
 Home-page: https://medium.com/@sevdimali
 Author: Sevdimali Isayev
 Author-email: sevdimaliisa@gmail.com
 License: MIT
 Keywords: django highlight
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `dj_search_highlight-1.0/setup.cfg` & `dj_search_highlight-1.1/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2064 6a5f 7365 6172 6368 5f68 6967   = dj_search_hig
 00000020: 686c 6967 6874 0d0a 7665 7273 696f 6e20  hlight..version 
-00000030: 3d20 312e 300d 0a61 7574 686f 7220 3d20  = 1.0..author = 
+00000030: 3d20 312e 310d 0a61 7574 686f 7220 3d20  = 1.1..author = 
 00000040: 5365 7664 696d 616c 6920 4973 6179 6576  Sevdimali Isayev
 00000050: 0d0a 6175 7468 6f72 5f65 6d61 696c 203d  ..author_email =
 00000060: 2073 6576 6469 6d61 6c69 6973 6140 676d   sevdimaliisa@gm
 00000070: 6169 6c2e 636f 6d0d 0a64 6573 6372 6970  ail.com..descrip
 00000080: 7469 6f6e 203d 2048 6967 686c 6967 6874  tion = Highlight
 00000090: 2073 7472 696e 6720 696e 2074 6865 2074   string in the t
 000000a0: 6578 742e 0d0a 6c6f 6e67 5f64 6573 6372  ext...long_descr
```

