# Comparing `tmp/garatool-0.1683684558.0.tar.gz` & `tmp/garatool-0.1683950588.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "garatool-0.1683684558.0.tar", last modified: Wed May 10 02:09:20 2023, max compression
+gzip compressed data, was "garatool-0.1683950588.0.tar", last modified: Sat May 13 04:03:09 2023, max compression
```

## Comparing `garatool-0.1683684558.0.tar` & `garatool-0.1683950588.0.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 curlyz     (501) staff       (20)        0 2023-05-10 02:09:20.267911 garatool-0.1683684558.0/
--rw-r--r--   0 curlyz     (501) staff       (20)      286 2023-05-10 02:09:20.267367 garatool-0.1683684558.0/PKG-INFO
--rw-r--r--   0 curlyz     (501) staff       (20)        0 2023-05-09 14:06:02.000000 garatool-0.1683684558.0/README.md
-drwxr-xr-x   0 curlyz     (501) staff       (20)        0 2023-05-10 02:09:20.245966 garatool-0.1683684558.0/garatool/
--rw-r--r--   0 curlyz     (501) staff       (20)     6418 2023-05-10 02:09:06.000000 garatool-0.1683684558.0/garatool/__init__.py
--rw-r--r--   0 curlyz     (501) staff       (20)       64 2023-05-09 16:48:25.000000 garatool-0.1683684558.0/garatool/__main__.py
-drwxr-xr-x   0 curlyz     (501) staff       (20)        0 2023-05-10 02:09:20.262399 garatool-0.1683684558.0/garatool.egg-info/
--rw-r--r--   0 curlyz     (501) staff       (20)      286 2023-05-10 02:09:19.000000 garatool-0.1683684558.0/garatool.egg-info/PKG-INFO
--rw-r--r--   0 curlyz     (501) staff       (20)      219 2023-05-10 02:09:20.000000 garatool-0.1683684558.0/garatool.egg-info/SOURCES.txt
--rw-r--r--   0 curlyz     (501) staff       (20)        1 2023-05-10 02:09:19.000000 garatool-0.1683684558.0/garatool.egg-info/dependency_links.txt
--rw-r--r--   0 curlyz     (501) staff       (20)       51 2023-05-10 02:09:19.000000 garatool-0.1683684558.0/garatool.egg-info/requires.txt
--rw-r--r--   0 curlyz     (501) staff       (20)        9 2023-05-10 02:09:19.000000 garatool-0.1683684558.0/garatool.egg-info/top_level.txt
--rw-r--r--   0 curlyz     (501) staff       (20)       38 2023-05-10 02:09:20.269381 garatool-0.1683684558.0/setup.cfg
--rw-r--r--   0 curlyz     (501) staff       (20)     1102 2023-05-09 16:41:54.000000 garatool-0.1683684558.0/setup.py
+drwxr-xr-x   0 curlyz     (501) staff       (20)        0 2023-05-13 04:03:09.151366 garatool-0.1683950588.0/
+-rw-r--r--   0 curlyz     (501) staff       (20)      286 2023-05-13 04:03:09.150713 garatool-0.1683950588.0/PKG-INFO
+-rw-r--r--   0 curlyz     (501) staff       (20)        0 2023-05-09 14:06:02.000000 garatool-0.1683950588.0/README.md
+drwxr-xr-x   0 curlyz     (501) staff       (20)        0 2023-05-13 04:03:09.145933 garatool-0.1683950588.0/garatool/
+-rw-r--r--   0 curlyz     (501) staff       (20)     6595 2023-05-13 04:02:57.000000 garatool-0.1683950588.0/garatool/__init__.py
+-rw-r--r--   0 curlyz     (501) staff       (20)       64 2023-05-09 16:48:25.000000 garatool-0.1683950588.0/garatool/__main__.py
+drwxr-xr-x   0 curlyz     (501) staff       (20)        0 2023-05-13 04:03:09.149324 garatool-0.1683950588.0/garatool.egg-info/
+-rw-r--r--   0 curlyz     (501) staff       (20)      286 2023-05-13 04:03:08.000000 garatool-0.1683950588.0/garatool.egg-info/PKG-INFO
+-rw-r--r--   0 curlyz     (501) staff       (20)      219 2023-05-13 04:03:09.000000 garatool-0.1683950588.0/garatool.egg-info/SOURCES.txt
+-rw-r--r--   0 curlyz     (501) staff       (20)        1 2023-05-13 04:03:08.000000 garatool-0.1683950588.0/garatool.egg-info/dependency_links.txt
+-rw-r--r--   0 curlyz     (501) staff       (20)       51 2023-05-13 04:03:08.000000 garatool-0.1683950588.0/garatool.egg-info/requires.txt
+-rw-r--r--   0 curlyz     (501) staff       (20)        9 2023-05-13 04:03:08.000000 garatool-0.1683950588.0/garatool.egg-info/top_level.txt
+-rw-r--r--   0 curlyz     (501) staff       (20)       38 2023-05-13 04:03:09.151481 garatool-0.1683950588.0/setup.cfg
+-rw-r--r--   0 curlyz     (501) staff       (20)     1102 2023-05-09 16:41:54.000000 garatool-0.1683950588.0/setup.py
```

### Comparing `garatool-0.1683684558.0/setup.py` & `garatool-0.1683950588.0/setup.py`

 * *Files identical despite different names*

