# Comparing `tmp/checkify-0.1.tar.gz` & `tmp/checkify-0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "checkify-0.1.tar", last modified: Sat May 13 14:01:46 2023, max compression
+gzip compressed data, was "checkify-0.2.tar", last modified: Sat May 13 14:06:21 2023, max compression
```

## Comparing `checkify-0.1.tar` & `checkify-0.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:01:46.108399 checkify-0.1/
--rw-rw-rw-   0        0        0     1101 2023-05-13 13:47:43.000000 checkify-0.1/LICENSE
--rw-rw-rw-   0        0        0       76 2023-05-13 14:01:46.106397 checkify-0.1/PKG-INFO
--rw-rw-rw-   0        0        0      104 2023-05-13 13:47:43.000000 checkify-0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 14:01:46.081398 checkify-0.1/checkify/
--rw-rw-rw-   0        0        0        0 2023-05-13 13:57:56.000000 checkify-0.1/checkify/__init__.py
--rw-rw-rw-   0        0        0      641 2023-05-13 14:01:42.000000 checkify-0.1/checkify/code_checker.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:01:46.104395 checkify-0.1/checkify.egg-info/
--rw-rw-rw-   0        0        0       76 2023-05-13 14:01:45.000000 checkify-0.1/checkify.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      231 2023-05-13 14:01:45.000000 checkify-0.1/checkify.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:01:45.000000 checkify-0.1/checkify.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        7 2023-05-13 14:01:45.000000 checkify-0.1/checkify.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-05-13 14:01:45.000000 checkify-0.1/checkify.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 14:01:46.108399 checkify-0.1/setup.cfg
--rw-rw-rw-   0        0        0      163 2023-05-13 14:00:52.000000 checkify-0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:06:21.328421 checkify-0.2/
+-rw-rw-rw-   0        0        0     1101 2023-05-13 13:47:43.000000 checkify-0.2/LICENSE
+-rw-rw-rw-   0        0        0      746 2023-05-13 14:06:21.326460 checkify-0.2/PKG-INFO
+-rw-rw-rw-   0        0        0      497 2023-05-13 14:06:02.000000 checkify-0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 14:06:21.291417 checkify-0.2/checkify/
+-rw-rw-rw-   0        0        0        0 2023-05-13 13:57:56.000000 checkify-0.2/checkify/__init__.py
+-rw-rw-rw-   0        0        0      641 2023-05-13 14:01:42.000000 checkify-0.2/checkify/code_checker.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:06:21.324426 checkify-0.2/checkify.egg-info/
+-rw-rw-rw-   0        0        0      746 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      231 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 14:06:21.000000 checkify-0.2/checkify.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:06:21.328421 checkify-0.2/setup.cfg
+-rw-rw-rw-   0        0        0      501 2023-05-13 14:06:16.000000 checkify-0.2/setup.py
```

### Comparing `checkify-0.1/LICENSE` & `checkify-0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `checkify-0.1/checkify/code_checker.py` & `checkify-0.2/checkify/code_checker.py`

 * *Files identical despite different names*

