# Comparing `tmp/checkify-0.3.tar.gz` & `tmp/checkify-0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "checkify-0.3.tar", last modified: Sat May 13 14:10:54 2023, max compression
+gzip compressed data, was "checkify-0.4.tar", last modified: Sat May 13 14:31:07 2023, max compression
```

## Comparing `checkify-0.3.tar` & `checkify-0.4.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:10:54.029281 checkify-0.3/
--rw-rw-rw-   0        0        0     1101 2023-05-13 13:47:43.000000 checkify-0.3/LICENSE
--rw-rw-rw-   0        0        0      746 2023-05-13 14:10:54.027770 checkify-0.3/PKG-INFO
--rw-rw-rw-   0        0        0      497 2023-05-13 14:06:02.000000 checkify-0.3/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 14:10:53.990737 checkify-0.3/checkify/
--rw-rw-rw-   0        0        0        0 2023-05-13 13:57:56.000000 checkify-0.3/checkify/__init__.py
--rw-rw-rw-   0        0        0      798 2023-05-13 14:10:02.000000 checkify-0.3/checkify/code_checker.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:10:54.026811 checkify-0.3/checkify.egg-info/
--rw-rw-rw-   0        0        0      746 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      231 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        7 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-05-13 14:10:53.000000 checkify-0.3/checkify.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 14:10:54.030291 checkify-0.3/setup.cfg
--rw-rw-rw-   0        0        0      501 2023-05-13 14:10:42.000000 checkify-0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:31:07.478750 checkify-0.4/
+-rw-rw-rw-   0        0        0     1101 2023-05-13 13:47:43.000000 checkify-0.4/LICENSE
+-rw-rw-rw-   0        0        0     1143 2023-05-13 14:31:07.476752 checkify-0.4/PKG-INFO
+-rw-rw-rw-   0        0        0      587 2023-05-13 14:30:49.000000 checkify-0.4/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 14:31:07.430730 checkify-0.4/checkify/
+-rw-rw-rw-   0        0        0        0 2023-05-13 13:57:56.000000 checkify-0.4/checkify/__init__.py
+-rw-rw-rw-   0        0        0      798 2023-05-13 14:10:02.000000 checkify-0.4/checkify/code_checker.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:31:07.473764 checkify-0.4/checkify.egg-info/
+-rw-rw-rw-   0        0        0     1143 2023-05-13 14:31:06.000000 checkify-0.4/checkify.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      231 2023-05-13 14:31:07.000000 checkify-0.4/checkify.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:31:06.000000 checkify-0.4/checkify.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 14:31:06.000000 checkify-0.4/checkify.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 14:31:06.000000 checkify-0.4/checkify.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:31:07.478750 checkify-0.4/setup.cfg
+-rw-rw-rw-   0        0        0     1053 2023-05-13 14:30:58.000000 checkify-0.4/setup.py
```

### Comparing `checkify-0.3/LICENSE` & `checkify-0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `checkify-0.3/checkify/code_checker.py` & `checkify-0.4/checkify/code_checker.py`

 * *Files identical despite different names*

