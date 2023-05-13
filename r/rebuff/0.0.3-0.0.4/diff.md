# Comparing `tmp/rebuff-0.0.3.tar.gz` & `tmp/rebuff-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rebuff-0.0.3.tar", last modified: Sat May 13 21:14:53 2023, max compression
+gzip compressed data, was "rebuff-0.0.4.tar", last modified: Sat May 13 21:21:12 2023, max compression
```

## Comparing `rebuff-0.0.3.tar` & `rebuff-0.0.4.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:14:53.031864 rebuff-0.0.3/
--rw-r--r--   0 willempienaar   (501) staff       (20)       70 2023-05-13 21:14:53.031933 rebuff-0.0.3/PKG-INFO
--rw-r--r--   0 willempienaar   (501) staff       (20)      344 2023-04-29 19:39:35.000000 rebuff-0.0.3/pyproject.toml
-drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:14:53.030219 rebuff-0.0.3/rebuff/
--rw-r--r--   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:14:27.000000 rebuff-0.0.3/rebuff/__init__.py
--rw-r--r--   0 willempienaar   (501) staff       (20)     6508 2023-05-13 20:59:59.000000 rebuff-0.0.3/rebuff/rebuff.py
-drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:14:53.031165 rebuff-0.0.3/rebuff.egg-info/
--rw-r--r--   0 willempienaar   (501) staff       (20)       70 2023-05-13 21:14:52.000000 rebuff-0.0.3/rebuff.egg-info/PKG-INFO
--rw-r--r--   0 willempienaar   (501) staff       (20)      268 2023-05-13 21:14:53.000000 rebuff-0.0.3/rebuff.egg-info/SOURCES.txt
--rw-r--r--   0 willempienaar   (501) staff       (20)        1 2023-05-13 21:14:52.000000 rebuff-0.0.3/rebuff.egg-info/dependency_links.txt
--rw-r--r--   0 willempienaar   (501) staff       (20)      133 2023-05-13 21:14:52.000000 rebuff-0.0.3/rebuff.egg-info/requires.txt
--rw-r--r--   0 willempienaar   (501) staff       (20)        7 2023-05-13 21:14:52.000000 rebuff-0.0.3/rebuff.egg-info/top_level.txt
--rw-r--r--   0 willempienaar   (501) staff       (20)      451 2023-05-13 21:14:53.032271 rebuff-0.0.3/setup.cfg
--rw-r--r--   0 willempienaar   (501) staff       (20)      463 2023-05-13 21:14:47.000000 rebuff-0.0.3/setup.py
-drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:14:53.031632 rebuff-0.0.3/tests/
--rw-r--r--   0 willempienaar   (501) staff       (20)     3431 2023-05-13 20:59:34.000000 rebuff-0.0.3/tests/test_integration.py
--rw-r--r--   0 willempienaar   (501) staff       (20)     2741 2023-05-13 20:59:59.000000 rebuff-0.0.3/tests/test_langchain.py
+drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:21:12.690230 rebuff-0.0.4/
+-rw-r--r--   0 willempienaar   (501) staff       (20)       70 2023-05-13 21:21:12.690292 rebuff-0.0.4/PKG-INFO
+-rw-r--r--   0 willempienaar   (501) staff       (20)      344 2023-04-29 19:39:35.000000 rebuff-0.0.4/pyproject.toml
+drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:21:12.688811 rebuff-0.0.4/rebuff/
+-rw-r--r--   0 willempienaar   (501) staff       (20)      223 2023-05-13 21:20:25.000000 rebuff-0.0.4/rebuff/__init__.py
+-rw-r--r--   0 willempienaar   (501) staff       (20)     6508 2023-05-13 20:59:59.000000 rebuff-0.0.4/rebuff/rebuff.py
+drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:21:12.689622 rebuff-0.0.4/rebuff.egg-info/
+-rw-r--r--   0 willempienaar   (501) staff       (20)       70 2023-05-13 21:21:12.000000 rebuff-0.0.4/rebuff.egg-info/PKG-INFO
+-rw-r--r--   0 willempienaar   (501) staff       (20)      268 2023-05-13 21:21:12.000000 rebuff-0.0.4/rebuff.egg-info/SOURCES.txt
+-rw-r--r--   0 willempienaar   (501) staff       (20)        1 2023-05-13 21:21:12.000000 rebuff-0.0.4/rebuff.egg-info/dependency_links.txt
+-rw-r--r--   0 willempienaar   (501) staff       (20)      133 2023-05-13 21:21:12.000000 rebuff-0.0.4/rebuff.egg-info/requires.txt
+-rw-r--r--   0 willempienaar   (501) staff       (20)        7 2023-05-13 21:21:12.000000 rebuff-0.0.4/rebuff.egg-info/top_level.txt
+-rw-r--r--   0 willempienaar   (501) staff       (20)      451 2023-05-13 21:21:12.690611 rebuff-0.0.4/setup.cfg
+-rw-r--r--   0 willempienaar   (501) staff       (20)      463 2023-05-13 21:21:11.000000 rebuff-0.0.4/setup.py
+drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 21:21:12.690033 rebuff-0.0.4/tests/
+-rw-r--r--   0 willempienaar   (501) staff       (20)     3431 2023-05-13 20:59:34.000000 rebuff-0.0.4/tests/test_integration.py
+-rw-r--r--   0 willempienaar   (501) staff       (20)     2741 2023-05-13 20:59:59.000000 rebuff-0.0.4/tests/test_langchain.py
```

### Comparing `rebuff-0.0.3/rebuff/rebuff.py` & `rebuff-0.0.4/rebuff/rebuff.py`

 * *Files identical despite different names*

### Comparing `rebuff-0.0.3/tests/test_integration.py` & `rebuff-0.0.4/tests/test_integration.py`

 * *Files identical despite different names*

### Comparing `rebuff-0.0.3/tests/test_langchain.py` & `rebuff-0.0.4/tests/test_langchain.py`

 * *Files identical despite different names*

