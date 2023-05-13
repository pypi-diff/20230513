# Comparing `tmp/zyncify-0.1.1-py2.py3-none-any.whl.zip` & `tmp/zyncify-0.1.2-py2.py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,13 +1,13 @@
-Zip file size: 15891 bytes, number of entries: 11
+Zip file size: 16331 bytes, number of entries: 11
 -rw-r--r--  2.0 unx      180 b- defN 23-May-13 15:40 zync/__init__.py
 -rw-r--r--  2.0 unx      480 b- defN 23-May-13 13:21 zync/logging.py
--rw-r--r--  2.0 unx     1470 b- defN 23-May-13 16:32 zync/main.py
+-rw-r--r--  2.0 unx     1470 b- defN 23-May-13 16:44 zync/main.py
 -rw-r--r--  2.0 unx      838 b- defN 23-May-13 13:15 zync/slugify.py
 -rw-r--r--  2.0 unx      966 b- defN 23-May-13 14:31 zync/zync.py
--rw-r--r--  2.0 unx    35149 b- defN 23-May-13 16:32 zyncify-0.1.1.dist-info/LICENSE
--rw-r--r--  2.0 unx      257 b- defN 23-May-13 16:32 zyncify-0.1.1.dist-info/METADATA
--rw-r--r--  2.0 unx      110 b- defN 23-May-13 16:32 zyncify-0.1.1.dist-info/WHEEL
--rw-r--r--  2.0 unx       40 b- defN 23-May-13 16:32 zyncify-0.1.1.dist-info/entry_points.txt
--rw-r--r--  2.0 unx        5 b- defN 23-May-13 16:32 zyncify-0.1.1.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      832 b- defN 23-May-13 16:32 zyncify-0.1.1.dist-info/RECORD
-11 files, 40327 bytes uncompressed, 14495 bytes compressed:  64.1%
+-rw-r--r--  2.0 unx    35149 b- defN 23-May-13 16:44 zyncify-0.1.2.dist-info/LICENSE
+-rw-r--r--  2.0 unx     1647 b- defN 23-May-13 16:44 zyncify-0.1.2.dist-info/METADATA
+-rw-r--r--  2.0 unx      110 b- defN 23-May-13 16:44 zyncify-0.1.2.dist-info/WHEEL
+-rw-r--r--  2.0 unx       40 b- defN 23-May-13 16:44 zyncify-0.1.2.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx        5 b- defN 23-May-13 16:44 zyncify-0.1.2.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      833 b- defN 23-May-13 16:44 zyncify-0.1.2.dist-info/RECORD
+11 files, 41718 bytes uncompressed, 14935 bytes compressed:  64.2%
```

## zipnote {}

```diff
@@ -9,26 +9,26 @@
 
 Filename: zync/slugify.py
 Comment: 
 
 Filename: zync/zync.py
 Comment: 
 
-Filename: zyncify-0.1.1.dist-info/LICENSE
+Filename: zyncify-0.1.2.dist-info/LICENSE
 Comment: 
 
-Filename: zyncify-0.1.1.dist-info/METADATA
+Filename: zyncify-0.1.2.dist-info/METADATA
 Comment: 
 
-Filename: zyncify-0.1.1.dist-info/WHEEL
+Filename: zyncify-0.1.2.dist-info/WHEEL
 Comment: 
 
-Filename: zyncify-0.1.1.dist-info/entry_points.txt
+Filename: zyncify-0.1.2.dist-info/entry_points.txt
 Comment: 
 
-Filename: zyncify-0.1.1.dist-info/top_level.txt
+Filename: zyncify-0.1.2.dist-info/top_level.txt
 Comment: 
 
-Filename: zyncify-0.1.1.dist-info/RECORD
+Filename: zyncify-0.1.2.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## zync/main.py

```diff
@@ -5,15 +5,15 @@
 import argparse
 from .__init__ import __all__ as methods
 
 NAME = "zyncify"
 DISPLAY_NAME = "zync"
 DESCRIPTION = "zync is a utility tool for python operations"
 URL = "https://github.com/tjbredemeyer/zync"
-VERSION = "0.1.1"
+VERSION = "0.1.2"
 AUTHOR = "TJ Bredemeyer"
 AUTHOR_EMAIL = "tj@teicor.com"
 LICENSE = "GNU Public License v3"
 
 info_string = (
     "\n"
     f"name: {DISPLAY_NAME}\n"
```

## Comparing `zyncify-0.1.1.dist-info/LICENSE` & `zyncify-0.1.2.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `zyncify-0.1.1.dist-info/RECORD` & `zyncify-0.1.2.dist-info/RECORD`

 * *Files 21% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 zync/__init__.py,sha256=_1Ddgq-jZ-TwHdJ2lVcMHMApIN9T5t_-eYm83gulqsg,180
 zync/logging.py,sha256=m5_OZAfXkLTDfUD-rTyPJMt9H64VQKnZELGUeRExvdA,480
-zync/main.py,sha256=McIioAcguF3FVnDK9P208AZOv0E3NXanuMJyCAuoAeI,1470
+zync/main.py,sha256=ezRqKu8j964LyUMb4WjnPdds1uNYS5uSdM4hUYwjAzg,1470
 zync/slugify.py,sha256=7Q0h1h1vl30lOnX_ivNNjaihTOhE1W049f8_2GJQUCQ,838
 zync/zync.py,sha256=8v_UuFXkqXBWJoWMVPXrYaTjm44A-ebqma6aWz7C08o,966
-zyncify-0.1.1.dist-info/LICENSE,sha256=OXLcl0T2SZ8Pmy2_dmlvKuetivmyPd5m1q-Gyd-zaYY,35149
-zyncify-0.1.1.dist-info/METADATA,sha256=p64N-E42a3OqIBBqjisDC9GJCUqrgh3cVCcWFRbDjLQ,257
-zyncify-0.1.1.dist-info/WHEEL,sha256=a-zpFRIJzOq5QfuhBzbhiA1eHTzNCJn8OdRvhdNX0Rk,110
-zyncify-0.1.1.dist-info/entry_points.txt,sha256=0QVFF5WXT78tlcVIjqC1XaJQCoKLt3Ift4yf5XKvang,40
-zyncify-0.1.1.dist-info/top_level.txt,sha256=mlXSVhjVoe_juOKGaECAEy2FR1Bt94xpiQhAcXNu5w0,5
-zyncify-0.1.1.dist-info/RECORD,,
+zyncify-0.1.2.dist-info/LICENSE,sha256=OXLcl0T2SZ8Pmy2_dmlvKuetivmyPd5m1q-Gyd-zaYY,35149
+zyncify-0.1.2.dist-info/METADATA,sha256=860Lt1a9NhocEKXLI0AGlV8B1HVPS3rSN30L6edjGLw,1647
+zyncify-0.1.2.dist-info/WHEEL,sha256=a-zpFRIJzOq5QfuhBzbhiA1eHTzNCJn8OdRvhdNX0Rk,110
+zyncify-0.1.2.dist-info/entry_points.txt,sha256=0QVFF5WXT78tlcVIjqC1XaJQCoKLt3Ift4yf5XKvang,40
+zyncify-0.1.2.dist-info/top_level.txt,sha256=mlXSVhjVoe_juOKGaECAEy2FR1Bt94xpiQhAcXNu5w0,5
+zyncify-0.1.2.dist-info/RECORD,,
```

