# Comparing `tmp/wwsimulator-1.0.0.tar.gz` & `tmp/wwsimulator-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "wwsimulator-1.0.0.tar", last modified: Sat May 13 13:49:52 2023, max compression
+gzip compressed data, was "wwsimulator-1.0.1.tar", last modified: Sat May 13 14:37:51 2023, max compression
```

## Comparing `wwsimulator-1.0.0.tar` & `wwsimulator-1.0.1.tar`

### file list

```diff
@@ -1,10 +1,10 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 13:49:52.642361 wwsimulator-1.0.0/
--rw-rw-rw-   0        0        0       58 2023-05-13 13:49:52.641362 wwsimulator-1.0.0/PKG-INFO
--rw-rw-rw-   0        0        0       11 2023-05-13 13:41:59.000000 wwsimulator-1.0.0/README.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 13:49:52.642361 wwsimulator-1.0.0/setup.cfg
--rw-rw-rw-   0        0        0      263 2023-05-13 13:46:58.000000 wwsimulator-1.0.0/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 13:49:52.640381 wwsimulator-1.0.0/wwsimulator.egg-info/
--rw-rw-rw-   0        0        0       58 2023-05-13 13:49:52.000000 wwsimulator-1.0.0/wwsimulator.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      206 2023-05-13 13:49:52.000000 wwsimulator-1.0.0/wwsimulator.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 13:49:52.000000 wwsimulator-1.0.0/wwsimulator.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       32 2023-05-13 13:49:52.000000 wwsimulator-1.0.0/wwsimulator.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 14:37:51.658549 wwsimulator-1.0.1/
+-rw-rw-rw-   0        0        0       73 2023-05-13 14:37:51.654549 wwsimulator-1.0.1/PKG-INFO
+-rw-rw-rw-   0        0        0       11 2023-05-13 13:41:59.000000 wwsimulator-1.0.1/README.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:37:51.658549 wwsimulator-1.0.1/setup.cfg
+-rw-rw-rw-   0        0        0      349 2023-05-13 14:37:09.000000 wwsimulator-1.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:37:51.654549 wwsimulator-1.0.1/wwsimulator.egg-info/
+-rw-rw-rw-   0        0        0       73 2023-05-13 14:37:51.000000 wwsimulator-1.0.1/wwsimulator.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      212 2023-05-13 14:37:51.000000 wwsimulator-1.0.1/wwsimulator.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:37:51.000000 wwsimulator-1.0.1/wwsimulator.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       38 2023-05-13 14:37:51.000000 wwsimulator-1.0.1/wwsimulator.egg-info/top_level.txt
```

