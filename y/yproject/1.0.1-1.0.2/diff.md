# Comparing `tmp/yproject-1.0.1.tar.gz` & `tmp/yproject-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "yproject-1.0.1.tar", last modified: Sat May 13 09:03:58 2023, max compression
+gzip compressed data, was "yproject-1.0.2.tar", last modified: Sat May 13 09:18:27 2023, max compression
```

## Comparing `yproject-1.0.1.tar` & `yproject-1.0.2.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:03:58.001396 yproject-1.0.1/
--rw-r--r--   0 ben       (1000) ben       (1000)     1065 2023-05-13 07:21:44.000000 yproject-1.0.1/LICENSE
--rw-r--r--   0 ben       (1000) ben       (1000)     1247 2023-05-13 09:03:58.001396 yproject-1.0.1/PKG-INFO
--rw-r--r--   0 ben       (1000) ben       (1000)      813 2023-05-13 08:53:11.000000 yproject-1.0.1/README.md
--rw-r--r--   0 ben       (1000) ben       (1000)      624 2023-05-13 08:54:28.000000 yproject-1.0.1/pyproject.toml
--rw-r--r--   0 ben       (1000) ben       (1000)       38 2023-05-13 09:03:58.001396 yproject-1.0.1/setup.cfg
-drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:03:57.998062 yproject-1.0.1/src/
-drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:03:58.001396 yproject-1.0.1/src/y/
--rw-r--r--   0 ben       (1000) ben       (1000)       17 2023-05-13 08:37:34.000000 yproject-1.0.1/src/y/__init__.py
--rw-r--r--   0 ben       (1000) ben       (1000)     1080 2023-05-13 07:31:27.000000 yproject-1.0.1/src/y/y.py
-drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:03:58.001396 yproject-1.0.1/src/yproject.egg-info/
--rw-r--r--   0 ben       (1000) ben       (1000)     1247 2023-05-13 09:03:57.000000 yproject-1.0.1/src/yproject.egg-info/PKG-INFO
--rw-r--r--   0 ben       (1000) ben       (1000)      219 2023-05-13 09:03:57.000000 yproject-1.0.1/src/yproject.egg-info/SOURCES.txt
--rw-r--r--   0 ben       (1000) ben       (1000)        1 2023-05-13 09:03:57.000000 yproject-1.0.1/src/yproject.egg-info/dependency_links.txt
--rw-r--r--   0 ben       (1000) ben       (1000)        2 2023-05-13 09:03:57.000000 yproject-1.0.1/src/yproject.egg-info/top_level.txt
-drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:03:58.001396 yproject-1.0.1/tests/
--rw-r--r--   0 ben       (1000) ben       (1000)      458 2023-05-13 08:45:54.000000 yproject-1.0.1/tests/test.py
+drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:18:27.279093 yproject-1.0.2/
+-rw-r--r--   0 ben       (1000) ben       (1000)     1065 2023-05-13 07:21:44.000000 yproject-1.0.2/LICENSE
+-rw-r--r--   0 ben       (1000) ben       (1000)     1247 2023-05-13 09:18:27.279093 yproject-1.0.2/PKG-INFO
+-rw-r--r--   0 ben       (1000) ben       (1000)      813 2023-05-13 09:11:45.000000 yproject-1.0.2/README.md
+-rw-r--r--   0 ben       (1000) ben       (1000)      624 2023-05-13 09:12:36.000000 yproject-1.0.2/pyproject.toml
+-rw-r--r--   0 ben       (1000) ben       (1000)       38 2023-05-13 09:18:27.279093 yproject-1.0.2/setup.cfg
+drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:18:27.275760 yproject-1.0.2/src/
+drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:18:27.279093 yproject-1.0.2/src/yproject/
+-rw-r--r--   0 ben       (1000) ben       (1000)       17 2023-05-13 08:37:34.000000 yproject-1.0.2/src/yproject/__init__.py
+-rw-r--r--   0 ben       (1000) ben       (1000)     1080 2023-05-13 07:31:27.000000 yproject-1.0.2/src/yproject/y.py
+drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:18:27.279093 yproject-1.0.2/src/yproject.egg-info/
+-rw-r--r--   0 ben       (1000) ben       (1000)     1247 2023-05-13 09:18:27.000000 yproject-1.0.2/src/yproject.egg-info/PKG-INFO
+-rw-r--r--   0 ben       (1000) ben       (1000)      233 2023-05-13 09:18:27.000000 yproject-1.0.2/src/yproject.egg-info/SOURCES.txt
+-rw-r--r--   0 ben       (1000) ben       (1000)        1 2023-05-13 09:18:27.000000 yproject-1.0.2/src/yproject.egg-info/dependency_links.txt
+-rw-r--r--   0 ben       (1000) ben       (1000)        9 2023-05-13 09:18:27.000000 yproject-1.0.2/src/yproject.egg-info/top_level.txt
+drwxr-xr-x   0 ben       (1000) ben       (1000)        0 2023-05-13 09:18:27.279093 yproject-1.0.2/tests/
+-rw-r--r--   0 ben       (1000) ben       (1000)      458 2023-05-13 09:11:39.000000 yproject-1.0.2/tests/test.py
```

### Comparing `yproject-1.0.1/LICENSE` & `yproject-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `yproject-1.0.1/PKG-INFO` & `yproject-1.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yproject
-Version: 1.0.1
+Version: 1.0.2
 Summary: Pipes for humans.
 Author-email: Ben Karcher <s6bkarc@uni-bonn.de>, wbrandon@csail.mit.edu, bdrisc@cs.stanford.edu, fydai@berkeley.edu, Lukas Sabatschus <lus@wallpen.com>, Ethan Smith <ethan@python.org>
 Project-URL: Homepage, https://y-project.dev
 Project-URL: Issues, https://github.com/the-y-project/y/issues
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `yproject-1.0.1/README.md` & `yproject-1.0.2/README.md`

 * *Files identical despite different names*

### Comparing `yproject-1.0.1/pyproject.toml` & `yproject-1.0.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "yproject"
-version = "1.0.1"
+version = "1.0.2"
 description = "Pipes for humans."
 readme = "README.md"
 authors = [
     {name = "Ben Karcher", email = "s6bkarc@uni-bonn.de"},
     {name = "", email = "wbrandon@csail.mit.edu"},
     {name = "", email = "bdrisc@cs.stanford.edu"},
     {name = "", email = "fydai@berkeley.edu"},
```

### Comparing `yproject-1.0.1/src/y/y.py` & `yproject-1.0.2/src/yproject/y.py`

 * *Files identical despite different names*

### Comparing `yproject-1.0.1/src/yproject.egg-info/PKG-INFO` & `yproject-1.0.2/src/yproject.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yproject
-Version: 1.0.1
+Version: 1.0.2
 Summary: Pipes for humans.
 Author-email: Ben Karcher <s6bkarc@uni-bonn.de>, wbrandon@csail.mit.edu, bdrisc@cs.stanford.edu, fydai@berkeley.edu, Lukas Sabatschus <lus@wallpen.com>, Ethan Smith <ethan@python.org>
 Project-URL: Homepage, https://y-project.dev
 Project-URL: Issues, https://github.com/the-y-project/y/issues
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

