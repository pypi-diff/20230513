# Comparing `tmp/cipherLV-0.1.0.tar.gz` & `tmp/cipherLV-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cipherLV-0.1.0.tar", last modified: Sat May 13 18:23:26 2023, max compression
+gzip compressed data, was "cipherLV-0.1.1.tar", last modified: Sat May 13 18:32:55 2023, max compression
```

## Comparing `cipherLV-0.1.0.tar` & `cipherLV-0.1.1.tar`

### file list

```diff
@@ -1,10 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 18:23:26.167552 cipherLV-0.1.0/
--rw-rw-rw-   0        0        0      780 2023-05-13 18:23:26.165437 cipherLV-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0       98 2023-05-13 18:16:31.000000 cipherLV-0.1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 18:23:26.159843 cipherLV-0.1.0/cipherLV.egg-info/
--rw-rw-rw-   0        0        0      780 2023-05-13 18:23:25.000000 cipherLV-0.1.0/cipherLV.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      146 2023-05-13 18:23:26.000000 cipherLV-0.1.0/cipherLV.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 18:23:25.000000 cipherLV-0.1.0/cipherLV.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 18:23:25.000000 cipherLV-0.1.0/cipherLV.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 18:23:26.168550 cipherLV-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0     1181 2023-05-13 18:23:04.000000 cipherLV-0.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 18:32:55.607060 cipherLV-0.1.1/
+-rw-rw-rw-   0        0        0      780 2023-05-13 18:32:55.605390 cipherLV-0.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0       98 2023-05-13 18:16:31.000000 cipherLV-0.1.1/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 18:32:55.577932 cipherLV-0.1.1/cipherLV/
+-rw-rw-rw-   0        0        0      107 2023-05-13 18:32:07.000000 cipherLV-0.1.1/cipherLV/__init__.py
+-rw-rw-rw-   0        0        0     1222 2023-05-13 16:55:55.000000 cipherLV-0.1.1/cipherLV/cipherLV.py
+drwxrwxrwx   0        0        0        0 2023-05-13 18:32:55.598961 cipherLV-0.1.1/cipherLV.egg-info/
+-rw-rw-rw-   0        0        0      780 2023-05-13 18:32:55.000000 cipherLV-0.1.1/cipherLV.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      188 2023-05-13 18:32:55.000000 cipherLV-0.1.1/cipherLV.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 18:32:55.000000 cipherLV-0.1.1/cipherLV.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 18:32:55.000000 cipherLV-0.1.1/cipherLV.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 18:32:55.608056 cipherLV-0.1.1/setup.cfg
+-rw-rw-rw-   0        0        0     1181 2023-05-13 18:31:51.000000 cipherLV-0.1.1/setup.py
```

### Comparing `cipherLV-0.1.0/PKG-INFO` & `cipherLV-0.1.1/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cipherLV
-Version: 0.1.0
+Version: 0.1.1
 Summary: Description: LV cipher is used for encrypting and decrypting with symmetric key
 Home-page: UNKNOWN
 Author: sarath babu
 Author-email: babusarath05@gmail.com
 License: UNKNOWN
 Description: 
         <h1> LV cipher </h1>
```

### Comparing `cipherLV-0.1.0/cipherLV.egg-info/PKG-INFO` & `cipherLV-0.1.1/cipherLV.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cipherLV
-Version: 0.1.0
+Version: 0.1.1
 Summary: Description: LV cipher is used for encrypting and decrypting with symmetric key
 Home-page: UNKNOWN
 Author: sarath babu
 Author-email: babusarath05@gmail.com
 License: UNKNOWN
 Description: 
         <h1> LV cipher </h1>
```

### Comparing `cipherLV-0.1.0/setup.py` & `cipherLV-0.1.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import os
 
 here = os.path.abspath(os.path.dirname(__file__))
 
 with codecs.open(os.path.join(here, "README.md"), encoding="utf-8") as fh:
     long_description = "\n" + fh.read()
 
-VERSION = '0.1.0'
+VERSION = '0.1.1'
 DESCRIPTION = 'Description: LV cipher is used for encrypting and decrypting with symmetric key'
 #LONG_DESCRIPTION = 'Long Description: LV Cipher is used for encrypting and decrypting with symmetric key'
 
 # Setting up
 setup(
     name="cipherLV",
     version=VERSION,
```

