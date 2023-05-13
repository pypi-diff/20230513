# Comparing `tmp/wwsimulator-1.0.1.tar.gz` & `tmp/wwsimulator-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "wwsimulator-1.0.1.tar", last modified: Sat May 13 14:37:51 2023, max compression
+gzip compressed data, was "wwsimulator-1.0.2.tar", last modified: Sat May 13 15:03:44 2023, max compression
```

## Comparing `wwsimulator-1.0.1.tar` & `wwsimulator-1.0.2.tar`

### file list

```diff
@@ -1,10 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:37:51.658549 wwsimulator-1.0.1/
--rw-rw-rw-   0        0        0       73 2023-05-13 14:37:51.654549 wwsimulator-1.0.1/PKG-INFO
--rw-rw-rw-   0        0        0       11 2023-05-13 13:41:59.000000 wwsimulator-1.0.1/README.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 14:37:51.658549 wwsimulator-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0      349 2023-05-13 14:37:09.000000 wwsimulator-1.0.1/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:37:51.654549 wwsimulator-1.0.1/wwsimulator.egg-info/
--rw-rw-rw-   0        0        0       73 2023-05-13 14:37:51.000000 wwsimulator-1.0.1/wwsimulator.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      212 2023-05-13 14:37:51.000000 wwsimulator-1.0.1/wwsimulator.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:37:51.000000 wwsimulator-1.0.1/wwsimulator.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       38 2023-05-13 14:37:51.000000 wwsimulator-1.0.1/wwsimulator.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 15:03:44.288474 wwsimulator-1.0.2/
+-rw-rw-rw-   0        0        0       73 2023-05-13 15:03:44.288474 wwsimulator-1.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0       11 2023-05-13 13:41:59.000000 wwsimulator-1.0.2/README.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 15:03:44.288474 wwsimulator-1.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      323 2023-05-13 15:03:39.000000 wwsimulator-1.0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:03:44.272474 wwsimulator-1.0.2/wwsimulator/
+-rw-rw-rw-   0        0        0        0 2023-05-13 14:58:55.000000 wwsimulator-1.0.2/wwsimulator/__init__.py
+-rw-rw-rw-   0        0        0    24914 2023-05-13 12:06:06.000000 wwsimulator-1.0.2/wwsimulator/wwsimulator.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:03:44.288474 wwsimulator-1.0.2/wwsimulator.egg-info/
+-rw-rw-rw-   0        0        0       73 2023-05-13 15:03:44.000000 wwsimulator-1.0.2/wwsimulator.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      210 2023-05-13 15:03:44.000000 wwsimulator-1.0.2/wwsimulator.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 15:03:44.000000 wwsimulator-1.0.2/wwsimulator.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       12 2023-05-13 15:03:44.000000 wwsimulator-1.0.2/wwsimulator.egg-info/top_level.txt
```

