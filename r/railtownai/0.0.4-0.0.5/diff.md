# Comparing `tmp/railtownai-0.0.4.tar.gz` & `tmp/railtownai-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "railtownai-0.0.4.tar", last modified: Fri May 12 22:17:43 2023, max compression
+gzip compressed data, was "railtownai-0.0.5.tar", last modified: Fri May 12 22:20:02 2023, max compression
```

## Comparing `railtownai-0.0.4.tar` & `railtownai-0.0.5.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0       33 2023-05-12 20:33:38.491589 railtownai-0.0.4/.gitignore
--rw-r--r--   0        0        0     1099 2023-05-12 16:09:43.096706 railtownai-0.0.4/LICENSE
--rw-r--r--   0        0        0     1083 2023-05-12 21:19:09.774851 railtownai-0.0.4/README.md
--rw-r--r--   0        0        0     1797 2023-05-12 21:19:18.884853 railtownai-0.0.4/pyproject.toml
--rw-r--r--   0        0        0     4059 2023-05-12 21:10:52.697137 railtownai-0.0.4/src/railtownai/__init__.py
--rw-r--r--   0        0        0     1009 2023-05-12 21:15:53.138497 railtownai-0.0.4/tests/conftest.py
--rw-r--r--   0        0        0      982 2023-05-12 21:03:10.112978 railtownai-0.0.4/tests/test_methods.py
--rw-r--r--   0        0        0     1371 1970-01-01 00:00:00.000000 railtownai-0.0.4/PKG-INFO
+-rw-r--r--   0        0        0       33 2023-05-12 20:33:38.491589 railtownai-0.0.5/.gitignore
+-rw-r--r--   0        0        0     1099 2023-05-12 16:09:43.096706 railtownai-0.0.5/LICENSE
+-rw-r--r--   0        0        0      358 2023-05-12 22:18:39.166314 railtownai-0.0.5/README.md
+-rw-r--r--   0        0        0     1797 2023-05-12 21:19:18.884853 railtownai-0.0.5/pyproject.toml
+-rw-r--r--   0        0        0     4059 2023-05-12 22:19:22.356109 railtownai-0.0.5/src/railtownai/__init__.py
+-rw-r--r--   0        0        0     1009 2023-05-12 21:15:53.138497 railtownai-0.0.5/tests/conftest.py
+-rw-r--r--   0        0        0      982 2023-05-12 21:03:10.112978 railtownai-0.0.5/tests/test_methods.py
+-rw-r--r--   0        0        0      664 1970-01-01 00:00:00.000000 railtownai-0.0.5/PKG-INFO
```

### Comparing `railtownai-0.0.4/LICENSE` & `railtownai-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `railtownai-0.0.4/pyproject.toml` & `railtownai-0.0.5/pyproject.toml`

 * *Files identical despite different names*

### Comparing `railtownai-0.0.4/src/railtownai/__init__.py` & `railtownai-0.0.5/src/railtownai/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -113,8 +113,8 @@
     trc = "Traceback (most recent call last):\n"
     stackstr = trc + "".join(traceback.format_list(stack))
     if exc is not None:
         stackstr += "  " + traceback.format_exc().lstrip(trc)
     return stackstr
 
 
-__version__ = "0.0.4"
+__version__ = "0.0.5"
```

### Comparing `railtownai-0.0.4/tests/conftest.py` & `railtownai-0.0.5/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `railtownai-0.0.4/tests/test_methods.py` & `railtownai-0.0.5/tests/test_methods.py`

 * *Files identical despite different names*

