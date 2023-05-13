# Comparing `tmp/bettersleepy-0.1.1-py3.11.egg` & `tmp/bettersleepy-0.1.2-py3.11.egg`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 1820 bytes, number of entries: 7
--rw-r--r--  2.0 unx      684 b- defN 23-May-13 07:58 EGG-INFO/PKG-INFO
--rw-r--r--  2.0 unx      198 b- defN 23-May-13 07:58 EGG-INFO/SOURCES.txt
--rw-r--r--  2.0 unx        1 b- defN 23-May-13 07:58 EGG-INFO/dependency_links.txt
--rw-r--r--  2.0 unx       13 b- defN 23-May-13 07:58 EGG-INFO/top_level.txt
--rw-r--r--  2.0 unx        1 b- defN 23-May-13 07:58 EGG-INFO/zip-safe
+Zip file size: 1821 bytes, number of entries: 7
+-rw-r--r--  2.0 unx      697 b- defN 23-May-13 08:05 EGG-INFO/PKG-INFO
+-rw-r--r--  2.0 unx      198 b- defN 23-May-13 08:05 EGG-INFO/SOURCES.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-May-13 08:05 EGG-INFO/dependency_links.txt
+-rw-r--r--  2.0 unx       13 b- defN 23-May-13 08:05 EGG-INFO/top_level.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-May-13 08:05 EGG-INFO/zip-safe
 -rw-r--r--  2.0 unx      132 b- defN 23-May-12 22:03 bettersleepy/__init__.py
--rw-r--r--  2.0 unx      751 b- defN 23-May-13 07:58 bettersleepy/__pycache__/__init__.cpython-311.pyc
-7 files, 1780 bytes uncompressed, 910 bytes compressed:  48.9%
+-rw-r--r--  2.0 unx      751 b- defN 23-May-13 08:05 bettersleepy/__pycache__/__init__.cpython-311.pyc
+7 files, 1793 bytes uncompressed, 911 bytes compressed:  49.2%
```

## EGG-INFO/PKG-INFO

```diff
@@ -1,28 +1,33 @@
 Metadata-Version: 2.1
 Name: bettersleepy
-Version: 0.1.1
+Version: 0.1.2
 Summary: Makes the Python sleep module easier a bit.
 Home-page: https://github.com/octopus1348/bettersleepy
 Author: Czira Zsombor
 Author-email: czirazsombor313@icloud.com
 
 BetterSleePy
 ============
 
-Makes the Python sleep module easier a bit. # Installation
+Makes the Python sleep module easier a bit.
+
+Installation
+============
 
 ::
 
    pip3 install bettersleepy
 
 Usage
 =====
 
-I recommend importing it as wait to make it shorter. Seconds:
+I recommend importing it as wait to make it shorter.
+
+Seconds:
 
 ::
 
    import bettersleepy as wait
 
    wait.sec(1)
    print("Waited 1 second.")
```

