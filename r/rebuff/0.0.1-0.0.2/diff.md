# Comparing `tmp/rebuff-0.0.1.tar.gz` & `tmp/rebuff-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rebuff-0.0.1.tar", last modified: Tue Apr 25 17:42:02 2023, max compression
+gzip compressed data, was "rebuff-0.0.2.tar", last modified: Sat May 13 20:50:01 2023, max compression
```

## Comparing `rebuff-0.0.1.tar` & `rebuff-0.0.2.tar`

### file list

```diff
@@ -1,11 +1,14 @@
-drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-04-25 17:42:02.101033 rebuff-0.0.1/
--rw-r--r--   0 willempienaar   (501) staff       (20)      180 2023-04-25 17:42:02.100916 rebuff-0.0.1/PKG-INFO
--rw-r--r--   0 willempienaar   (501) staff       (20)       52 2023-04-25 17:42:01.000000 rebuff-0.0.1/README.md
-drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-04-25 17:42:02.100785 rebuff-0.0.1/rebuff.egg-info/
--rw-r--r--   0 willempienaar   (501) staff       (20)      180 2023-04-25 17:42:02.000000 rebuff-0.0.1/rebuff.egg-info/PKG-INFO
--rw-r--r--   0 willempienaar   (501) staff       (20)      148 2023-04-25 17:42:02.000000 rebuff-0.0.1/rebuff.egg-info/SOURCES.txt
--rw-r--r--   0 willempienaar   (501) staff       (20)        1 2023-04-25 17:42:02.000000 rebuff-0.0.1/rebuff.egg-info/dependency_links.txt
--rw-r--r--   0 willempienaar   (501) staff       (20)        7 2023-04-25 17:42:02.000000 rebuff-0.0.1/rebuff.egg-info/top_level.txt
--rw-r--r--   0 willempienaar   (501) staff       (20)       26 2023-04-25 17:42:01.000000 rebuff-0.0.1/rebuff.py
--rw-r--r--   0 willempienaar   (501) staff       (20)       38 2023-04-25 17:42:02.101068 rebuff-0.0.1/setup.cfg
--rw-r--r--   0 willempienaar   (501) staff       (20)      225 2023-04-25 17:42:01.000000 rebuff-0.0.1/setup.py
+drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 20:50:01.986329 rebuff-0.0.2/
+-rw-r--r--   0 willempienaar   (501) staff       (20)       70 2023-05-13 20:50:01.986404 rebuff-0.0.2/PKG-INFO
+-rw-r--r--   0 willempienaar   (501) staff       (20)      344 2023-04-29 19:39:35.000000 rebuff-0.0.2/pyproject.toml
+drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 20:50:01.985571 rebuff-0.0.2/rebuff.egg-info/
+-rw-r--r--   0 willempienaar   (501) staff       (20)       70 2023-05-13 20:50:01.000000 rebuff-0.0.2/rebuff.egg-info/PKG-INFO
+-rw-r--r--   0 willempienaar   (501) staff       (20)      232 2023-05-13 20:50:01.000000 rebuff-0.0.2/rebuff.egg-info/SOURCES.txt
+-rw-r--r--   0 willempienaar   (501) staff       (20)        1 2023-05-13 20:50:01.000000 rebuff-0.0.2/rebuff.egg-info/dependency_links.txt
+-rw-r--r--   0 willempienaar   (501) staff       (20)      133 2023-05-13 20:50:01.000000 rebuff-0.0.2/rebuff.egg-info/requires.txt
+-rw-r--r--   0 willempienaar   (501) staff       (20)        1 2023-05-13 20:50:01.000000 rebuff-0.0.2/rebuff.egg-info/top_level.txt
+-rw-r--r--   0 willempienaar   (501) staff       (20)      451 2023-05-13 20:50:01.986735 rebuff-0.0.2/setup.cfg
+-rw-r--r--   0 willempienaar   (501) staff       (20)      463 2023-05-13 14:57:54.000000 rebuff-0.0.2/setup.py
+drwxr-xr-x   0 willempienaar   (501) staff       (20)        0 2023-05-13 20:50:01.986045 rebuff-0.0.2/tests/
+-rw-r--r--   0 willempienaar   (501) staff       (20)     3430 2023-05-13 15:06:09.000000 rebuff-0.0.2/tests/test_integration.py
+-rw-r--r--   0 willempienaar   (501) staff       (20)     2723 2023-05-13 15:05:01.000000 rebuff-0.0.2/tests/test_langchain.py
```

