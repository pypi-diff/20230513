# Comparing `tmp/evoluzo-0.0.1.tar.gz` & `tmp/evoluzo-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "evoluzo-0.0.1.tar", last modified: Thu Apr 27 23:52:36 2023, max compression
+gzip compressed data, was "evoluzo-0.0.2.tar", last modified: Sat May 13 18:49:06 2023, max compression
```

## Comparing `evoluzo-0.0.1.tar` & `evoluzo-0.0.2.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxr-x   0 pedro     (1000) pedro     (1000)        0 2023-04-27 23:52:36.586323 evoluzo-0.0.1/
--rw-rw-r--   0 pedro     (1000) pedro     (1000)      412 2023-04-27 23:52:36.586323 evoluzo-0.0.1/PKG-INFO
--rw-rw-r--   0 pedro     (1000) pedro     (1000)        8 2023-04-23 14:04:20.000000 evoluzo-0.0.1/README.md
--rw-rw-r--   0 pedro     (1000) pedro     (1000)      104 2023-04-27 23:46:26.000000 evoluzo-0.0.1/pyproject.toml
--rw-rw-r--   0 pedro     (1000) pedro     (1000)       38 2023-04-27 23:52:36.586323 evoluzo-0.0.1/setup.cfg
--rw-rw-r--   0 pedro     (1000) pedro     (1000)      721 2023-04-27 23:44:26.000000 evoluzo-0.0.1/setup.py
-drwxrwxr-x   0 pedro     (1000) pedro     (1000)        0 2023-04-27 23:52:36.582325 evoluzo-0.0.1/src/
-drwxrwxr-x   0 pedro     (1000) pedro     (1000)        0 2023-04-27 23:52:36.586323 evoluzo-0.0.1/src/evoluzo/
--rw-rw-r--   0 pedro     (1000) pedro     (1000)       40 2023-04-23 14:04:20.000000 evoluzo-0.0.1/src/evoluzo/__init__.py
--rw-rw-r--   0 pedro     (1000) pedro     (1000)      543 2023-04-27 23:34:01.000000 evoluzo-0.0.1/src/evoluzo/dna.py
--rw-rw-r--   0 pedro     (1000) pedro     (1000)     1511 2023-04-27 23:40:48.000000 evoluzo-0.0.1/src/evoluzo/population.py
-drwxrwxr-x   0 pedro     (1000) pedro     (1000)        0 2023-04-27 23:52:36.586323 evoluzo-0.0.1/src/evoluzo.egg-info/
--rw-rw-r--   0 pedro     (1000) pedro     (1000)      412 2023-04-27 23:52:36.000000 evoluzo-0.0.1/src/evoluzo.egg-info/PKG-INFO
--rw-rw-r--   0 pedro     (1000) pedro     (1000)      242 2023-04-27 23:52:36.000000 evoluzo-0.0.1/src/evoluzo.egg-info/SOURCES.txt
--rw-rw-r--   0 pedro     (1000) pedro     (1000)        1 2023-04-27 23:52:36.000000 evoluzo-0.0.1/src/evoluzo.egg-info/dependency_links.txt
--rw-rw-r--   0 pedro     (1000) pedro     (1000)        8 2023-04-27 23:52:36.000000 evoluzo-0.0.1/src/evoluzo.egg-info/top_level.txt
+drwxr-xr-x   0 pedro      (501) staff       (20)        0 2023-05-13 18:49:06.701557 evoluzo-0.0.2/
+-rw-r--r--   0 pedro      (501) staff       (20)      412 2023-05-13 18:49:06.701352 evoluzo-0.0.2/PKG-INFO
+-rw-r--r--   0 pedro      (501) staff       (20)        8 2023-05-13 18:43:37.000000 evoluzo-0.0.2/README.md
+-rw-r--r--   0 pedro      (501) staff       (20)      104 2023-05-13 18:43:37.000000 evoluzo-0.0.2/pyproject.toml
+-rw-r--r--   0 pedro      (501) staff       (20)       38 2023-05-13 18:49:06.701594 evoluzo-0.0.2/setup.cfg
+-rw-r--r--   0 pedro      (501) staff       (20)      721 2023-05-13 18:48:39.000000 evoluzo-0.0.2/setup.py
+drwxr-xr-x   0 pedro      (501) staff       (20)        0 2023-05-13 18:49:06.699048 evoluzo-0.0.2/src/
+drwxr-xr-x   0 pedro      (501) staff       (20)        0 2023-05-13 18:49:06.700064 evoluzo-0.0.2/src/evoluzo/
+-rw-r--r--   0 pedro      (501) staff       (20)       40 2023-05-13 18:43:37.000000 evoluzo-0.0.2/src/evoluzo/__init__.py
+-rw-r--r--   0 pedro      (501) staff       (20)      543 2023-05-13 18:43:37.000000 evoluzo-0.0.2/src/evoluzo/dna.py
+-rw-r--r--   0 pedro      (501) staff       (20)     1511 2023-05-13 18:43:37.000000 evoluzo-0.0.2/src/evoluzo/population.py
+drwxr-xr-x   0 pedro      (501) staff       (20)        0 2023-05-13 18:49:06.701120 evoluzo-0.0.2/src/evoluzo.egg-info/
+-rw-r--r--   0 pedro      (501) staff       (20)      412 2023-05-13 18:49:06.000000 evoluzo-0.0.2/src/evoluzo.egg-info/PKG-INFO
+-rw-r--r--   0 pedro      (501) staff       (20)      242 2023-05-13 18:49:06.000000 evoluzo-0.0.2/src/evoluzo.egg-info/SOURCES.txt
+-rw-r--r--   0 pedro      (501) staff       (20)        1 2023-05-13 18:49:06.000000 evoluzo-0.0.2/src/evoluzo.egg-info/dependency_links.txt
+-rw-r--r--   0 pedro      (501) staff       (20)        8 2023-05-13 18:49:06.000000 evoluzo-0.0.2/src/evoluzo.egg-info/top_level.txt
```

### Comparing `evoluzo-0.0.1/setup.py` & `evoluzo-0.0.2/setup.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="evoluzo",
-    version="0.0.1",
+    version="0.0.2",
     author="Zmee",
     author_email="mail.of.zmee@gmail.com",
     description="A genetic algorithm implementation",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/pypa/sampleproject",
     project_urls={},
```

### Comparing `evoluzo-0.0.1/src/evoluzo/dna.py` & `evoluzo-0.0.2/src/evoluzo/dna.py`

 * *Files identical despite different names*

### Comparing `evoluzo-0.0.1/src/evoluzo/population.py` & `evoluzo-0.0.2/src/evoluzo/population.py`

 * *Files identical despite different names*

