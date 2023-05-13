# Comparing `tmp/ucsd-cape-0.2.0.tar.gz` & `tmp/ucsd-cape-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ucsd-cape-0.2.0.tar", last modified: Wed May 10 01:13:35 2023, max compression
+gzip compressed data, was "ucsd-cape-0.3.0.tar", last modified: Sat May 13 02:13:00 2023, max compression
```

## Comparing `ucsd-cape-0.2.0.tar` & `ucsd-cape-0.3.0.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-05-10 01:13:35.565566 ucsd-cape-0.2.0/
--rw-rw-rw-   0        0        0     1087 2023-05-05 20:11:49.000000 ucsd-cape-0.2.0/LICENSE
--rw-rw-rw-   0        0        0     1903 2023-05-10 01:13:35.561224 ucsd-cape-0.2.0/PKG-INFO
--rw-rw-rw-   0        0        0       12 2023-05-05 20:10:21.000000 ucsd-cape-0.2.0/README.md
--rw-rw-rw-   0        0        0      810 2023-05-10 00:17:43.000000 ucsd-cape-0.2.0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-10 01:13:35.565566 ucsd-cape-0.2.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-05-10 01:13:35.506975 ucsd-cape-0.2.0/ucsd_cape.egg-info/
--rw-rw-rw-   0        0        0     1903 2023-05-10 01:13:35.000000 ucsd-cape-0.2.0/ucsd_cape.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      227 2023-05-10 01:13:35.000000 ucsd-cape-0.2.0/ucsd_cape.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-10 01:13:35.000000 ucsd-cape-0.2.0/ucsd_cape.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-05-10 01:13:35.000000 ucsd-cape-0.2.0/ucsd_cape.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-05-10 01:13:35.517196 ucsd-cape-0.2.0/ucsdcape/
--rw-rw-rw-   0        0        0        0 2023-05-09 18:41:47.000000 ucsd-cape-0.2.0/ucsdcape/__init__.py
--rw-rw-rw-   0        0        0        0 2023-05-09 18:41:47.000000 ucsd-cape-0.2.0/ucsdcape/__main__.py
--rw-rw-rw-   0        0        0      346 2023-05-10 00:42:39.000000 ucsd-cape-0.2.0/ucsdcape/capedata.py
+drwxrwxrwx   0        0        0        0 2023-05-13 02:13:00.138608 ucsd-cape-0.3.0/
+-rw-rw-rw-   0        0        0     1087 2023-05-05 20:11:49.000000 ucsd-cape-0.3.0/LICENSE
+-rw-rw-rw-   0        0        0     2302 2023-05-13 02:13:00.138608 ucsd-cape-0.3.0/PKG-INFO
+-rw-rw-rw-   0        0        0       12 2023-05-05 20:10:21.000000 ucsd-cape-0.3.0/README.md
+-rw-rw-rw-   0        0        0     1168 2023-05-13 02:11:50.000000 ucsd-cape-0.3.0/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 02:13:00.138608 ucsd-cape-0.3.0/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 02:13:00.138608 ucsd-cape-0.3.0/ucsd_cape.egg-info/
+-rw-rw-rw-   0        0        0     2302 2023-05-13 02:13:00.000000 ucsd-cape-0.3.0/ucsd_cape.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      227 2023-05-13 02:13:00.000000 ucsd-cape-0.3.0/ucsd_cape.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 02:13:00.000000 ucsd-cape-0.3.0/ucsd_cape.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 02:13:00.000000 ucsd-cape-0.3.0/ucsd_cape.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 02:13:00.138608 ucsd-cape-0.3.0/ucsdcape/
+-rw-rw-rw-   0        0        0        0 2023-05-11 19:14:07.000000 ucsd-cape-0.3.0/ucsdcape/__init__.py
+-rw-rw-rw-   0        0        0        0 2023-05-11 19:14:07.000000 ucsd-cape-0.3.0/ucsdcape/__main__.py
+-rw-rw-rw-   0        0        0     7975 2023-05-13 02:07:36.000000 ucsd-cape-0.3.0/ucsdcape/capedata.py
```

### Comparing `ucsd-cape-0.2.0/LICENSE` & `ucsd-cape-0.3.0/LICENSE`

 * *Files identical despite different names*

