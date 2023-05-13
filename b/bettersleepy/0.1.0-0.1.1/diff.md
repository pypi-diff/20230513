# Comparing `tmp/bettersleepy-0.1.0-py3.11.egg` & `tmp/bettersleepy-0.1.1-py3.11.egg`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 1662 bytes, number of entries: 7
--rw-r--r--  2.0 unx      227 b- defN 23-May-12 22:02 EGG-INFO/PKG-INFO
--rw-r--r--  2.0 unx      187 b- defN 23-May-12 22:02 EGG-INFO/SOURCES.txt
--rw-r--r--  2.0 unx        1 b- defN 23-May-12 22:02 EGG-INFO/dependency_links.txt
--rw-r--r--  2.0 unx       13 b- defN 23-May-12 22:02 EGG-INFO/top_level.txt
--rw-r--r--  2.0 unx        1 b- defN 23-May-12 22:02 EGG-INFO/zip-safe
--rw-r--r--  2.0 unx      132 b- defN 23-May-12 22:00 bettersleepy/__init__.py
--rw-r--r--  2.0 unx      751 b- defN 23-May-12 22:02 bettersleepy/__pycache__/__init__.cpython-311.pyc
-7 files, 1312 bytes uncompressed, 752 bytes compressed:  42.7%
+Zip file size: 1820 bytes, number of entries: 7
+-rw-r--r--  2.0 unx      684 b- defN 23-May-13 07:58 EGG-INFO/PKG-INFO
+-rw-r--r--  2.0 unx      198 b- defN 23-May-13 07:58 EGG-INFO/SOURCES.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-May-13 07:58 EGG-INFO/dependency_links.txt
+-rw-r--r--  2.0 unx       13 b- defN 23-May-13 07:58 EGG-INFO/top_level.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-May-13 07:58 EGG-INFO/zip-safe
+-rw-r--r--  2.0 unx      132 b- defN 23-May-12 22:03 bettersleepy/__init__.py
+-rw-r--r--  2.0 unx      751 b- defN 23-May-13 07:58 bettersleepy/__pycache__/__init__.cpython-311.pyc
+7 files, 1780 bytes uncompressed, 910 bytes compressed:  48.9%
```

## EGG-INFO/PKG-INFO

```diff
@@ -1,7 +1,46 @@
 Metadata-Version: 2.1
 Name: bettersleepy
-Version: 0.1.0
+Version: 0.1.1
 Summary: Makes the Python sleep module easier a bit.
 Home-page: https://github.com/octopus1348/bettersleepy
 Author: Czira Zsombor
 Author-email: czirazsombor313@icloud.com
+
+BetterSleePy
+============
+
+Makes the Python sleep module easier a bit. # Installation
+
+::
+
+   pip3 install bettersleepy
+
+Usage
+=====
+
+I recommend importing it as wait to make it shorter. Seconds:
+
+::
+
+   import bettersleepy as wait
+
+   wait.sec(1)
+   print("Waited 1 second.")
+
+Minutes:
+
+::
+
+   import bettersleepy as wait
+
+   wait.min(1)
+   print("Waited 1 minute.")
+
+Hours:
+
+::
+
+   import bettersleepy as wait
+
+   wait.hour(1)
+   print("Waited 1 hour.")
```

## EGG-INFO/SOURCES.txt

```diff
@@ -1,7 +1,8 @@
 README.md
+README.rst
 setup.py
 bettersleepy/__init__.py
 bettersleepy.egg-info/PKG-INFO
 bettersleepy.egg-info/SOURCES.txt
 bettersleepy.egg-info/dependency_links.txt
 bettersleepy.egg-info/top_level.txt
```

## bettersleepy/__pycache__/__init__.cpython-311.pyc

### Python bytecode

```diff
@@ -1,9 +1,9 @@
 magic:    0xa70d0d0a
-moddate:  0xc99a5e64 (Fri May 12 20:00:09 2023 UTC)
+moddate:  0x829b5e64 (Fri May 12 20:03:14 2023 UTC)
 files sz: 132
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 2
    flags     : 0
    code
```

