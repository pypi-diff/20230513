# Comparing `tmp/hashedcolls-1.1.0-py3-none-any.whl.zip` & `tmp/hashedcolls-1.1.1-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,8 +1,8 @@
-Zip file size: 2623 bytes, number of entries: 6
--rw-r--r--  2.0 unx      733 b- defN 23-Jan-04 23:23 hashedcolls/__init__.py
+Zip file size: 2610 bytes, number of entries: 6
+-rw-r--r--  2.0 unx      727 b- defN 23-May-13 20:51 hashedcolls/__init__.py
 -rw-r--r--  2.0 unx     1138 b- defN 22-May-29 11:56 hashedcolls/hashedcolls.py
--rw-r--r--  2.0 unx     1235 b- defN 23-Jan-04 23:28 hashedcolls-1.1.0.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jan-04 23:28 hashedcolls-1.1.0.dist-info/WHEEL
--rw-r--r--  2.0 unx       12 b- defN 23-Jan-04 23:28 hashedcolls-1.1.0.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx      476 b- defN 23-Jan-04 23:28 hashedcolls-1.1.0.dist-info/RECORD
-6 files, 3686 bytes uncompressed, 1759 bytes compressed:  52.3%
+-rw-r--r--  2.0 unx     1228 b- defN 23-May-13 20:52 hashedcolls-1.1.1.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-May-13 20:52 hashedcolls-1.1.1.dist-info/WHEEL
+-rw-r--r--  2.0 unx       12 b- defN 23-May-13 20:52 hashedcolls-1.1.1.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      476 b- defN 23-May-13 20:52 hashedcolls-1.1.1.dist-info/RECORD
+6 files, 3673 bytes uncompressed, 1746 bytes compressed:  52.5%
```

## zipnote {}

```diff
@@ -1,19 +1,19 @@
 Filename: hashedcolls/__init__.py
 Comment: 
 
 Filename: hashedcolls/hashedcolls.py
 Comment: 
 
-Filename: hashedcolls-1.1.0.dist-info/METADATA
+Filename: hashedcolls-1.1.1.dist-info/METADATA
 Comment: 
 
-Filename: hashedcolls-1.1.0.dist-info/WHEEL
+Filename: hashedcolls-1.1.1.dist-info/WHEEL
 Comment: 
 
-Filename: hashedcolls-1.1.0.dist-info/top_level.txt
+Filename: hashedcolls-1.1.1.dist-info/top_level.txt
 Comment: 
 
-Filename: hashedcolls-1.1.0.dist-info/RECORD
+Filename: hashedcolls-1.1.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## hashedcolls/__init__.py

```diff
@@ -10,13 +10,13 @@
 __pkg_desc__ = 'Hashed dict/list collections'
 __project_license__ = 'WTFPL'
 __author__ = '@jedi2light'
 __author_email__ = 'jedi2light@jedi2light.moe'
 __maintainer__ = __author__
 __maintainer_email__ = __author_email__
 __major_version__ = 1
-__minor_version__ = 0
-__patch_version__ = 2
+__minor_version__ = 1
+__patch_version__ = 1
 __version_tuple__ = (__major_version__,
                      __minor_version__,
                      __patch_version__)
-__version_string__ = '.'.join(list(map(str, __version_tuple__)))
+__version_string__ = '.'.join(map(str, __version_tuple__))
```

## Comparing `hashedcolls-1.1.0.dist-info/METADATA` & `hashedcolls-1.1.1.dist-info/METADATA`

 * *Files 13% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 Metadata-Version: 2.1
 Name: hashedcolls
-Version: 1.1.0
+Version: 1.1.1
 Summary: Hashed dict/list collections
 Author: @jedi2light
 Author-email: jedi2light@jedi2light.moe
 Maintainer: @jedi2light
 Maintainer-email: jedi2light@jedi2light.moe
 License: WTFPL
-Project-URL: Documentation, https://gitlab.com/jedi2light/hashedcolls.git
+Project-URL: Source, https://gitlab.com/jedi2light/hashedcolls.git
 Project-URL: Bug Tracker, https://gitlab.com/jedi2light/hashedcolls/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 
 # HashedColls - hashed dict/list collections
```

