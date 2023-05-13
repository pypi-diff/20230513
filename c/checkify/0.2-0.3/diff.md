# Comparing `tmp/checkify-0.2.tar.gz` & `tmp/checkify-0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "checkify-0.2.tar", last modified: Sat May 13 14:06:21 2023, max compression
+gzip compressed data, was "checkify-0.3.tar", last modified: Sat May 13 14:10:54 2023, max compression
```

## Comparing `checkify-0.2.tar` & `checkify-0.3.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:06:21.328421 checkify-0.2/
--rw-rw-rw-   0        0        0     1101 2023-05-13 13:47:43.000000 checkify-0.2/LICENSE
--rw-rw-rw-   0        0        0      746 2023-05-13 14:06:21.326460 checkify-0.2/PKG-INFO
--rw-rw-rw-   0        0        0      497 2023-05-13 14:06:02.000000 checkify-0.2/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 14:06:21.291417 checkify-0.2/checkify/
--rw-rw-rw-   0        0        0        0 2023-05-13 13:57:56.000000 checkify-0.2/checkify/__init__.py
--rw-rw-rw-   0        0        0      641 2023-05-13 14:01:42.000000 checkify-0.2/checkify/code_checker.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:06:21.324426 checkify-0.2/checkify.egg-info/
--rw-rw-rw-   0        0        0      746 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      231 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        7 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 14:06:21.328421 checkify-0.2/setup.cfg
--rw-rw-rw-   0        0        0      501 2023-05-13 14:06:16.000000 checkify-0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:10:54.029281 checkify-0.3/
+-rw-rw-rw-   0        0        0     1101 2023-05-13 13:47:43.000000 checkify-0.3/LICENSE
+-rw-rw-rw-   0        0        0      746 2023-05-13 14:10:54.027770 checkify-0.3/PKG-INFO
+-rw-rw-rw-   0        0        0      497 2023-05-13 14:06:02.000000 checkify-0.3/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 14:10:53.990737 checkify-0.3/checkify/
+-rw-rw-rw-   0        0        0        0 2023-05-13 13:57:56.000000 checkify-0.3/checkify/__init__.py
+-rw-rw-rw-   0        0        0      798 2023-05-13 14:10:02.000000 checkify-0.3/checkify/code_checker.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:10:54.026811 checkify-0.3/checkify.egg-info/
+-rw-rw-rw-   0        0        0      746 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      231 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:10:54.030291 checkify-0.3/setup.cfg
+-rw-rw-rw-   0        0        0      501 2023-05-13 14:10:42.000000 checkify-0.3/setup.py
```

### Comparing `checkify-0.2/LICENSE` & `checkify-0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `checkify-0.2/PKG-INFO` & `checkify-0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: checkify
-Version: 0.2
+Version: 0.3
 Home-page: https://github.com/aditya0072001/checkify
 Project-URL: Download Statistics, https://pepy.tech/project/checkify/month
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # checkify
```

### Comparing `checkify-0.2/checkify.egg-info/PKG-INFO` & `checkify-0.3/checkify.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: checkify
-Version: 0.2
+Version: 0.3
 Home-page: https://github.com/aditya0072001/checkify
 Project-URL: Download Statistics, https://pepy.tech/project/checkify/month
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # checkify
```

