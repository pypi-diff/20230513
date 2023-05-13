# Comparing `tmp/elasticityproject-0.1.1.1.tar.gz` & `tmp/elasticityproject-0.1.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "elasticityproject-0.1.1.1.tar", max compression
+gzip compressed data, was "elasticityproject-0.1.1.3.tar", max compression
```

## Comparing `elasticityproject-0.1.1.1.tar` & `elasticityproject-0.1.1.3.tar`

### file list

```diff
@@ -1,7 +1,8 @@
--rwxr-xr-x   0        0        0    35106 2023-04-30 22:15:20.832855 elasticityproject-0.1.1.1/LICENSE
--rw-r--r--   0        0        0      687 2023-05-10 16:05:49.138095 elasticityproject-0.1.1.1/pyproject.toml
--rw-r--r--   0        0        0      120 2023-05-10 15:55:03.674155 elasticityproject-0.1.1.1/src/elasticityproject/__init__.py
--rw-r--r--   0        0        0    21274 2023-05-10 15:29:26.293436 elasticityproject-0.1.1.1/src/elasticityproject/elasticity.py
--rw-r--r--   0        0        0     2891 2023-05-10 15:32:22.882648 elasticityproject-0.1.1.1/src/elasticityproject/plots3d.py
--rw-r--r--   0        0        0      827 2023-05-10 16:05:52.881065 elasticityproject-0.1.1.1/setup.py
--rw-r--r--   0        0        0      608 2023-05-10 16:05:52.881386 elasticityproject-0.1.1.1/PKG-INFO
+-rwxr-xr-x   0        0        0    35100 2023-05-13 19:37:36.869380 elasticityproject-0.1.1.3/LICENSE
+-rw-r--r--   0        0        0      793 2023-05-13 19:37:37.816241 elasticityproject-0.1.1.3/README.md
+-rw-r--r--   0        0        0      637 2023-05-13 21:01:28.766573 elasticityproject-0.1.1.3/pyproject.toml
+-rw-r--r--   0        0        0      119 2023-05-13 19:37:42.637839 elasticityproject-0.1.1.3/src/elasticityproject/__init__.py
+-rw-r--r--   0        0        0    21274 2023-05-13 19:57:02.043623 elasticityproject-0.1.1.3/src/elasticityproject/elasticityproject.py
+-rw-r--r--   0        0        0     2891 2023-05-13 19:57:56.680020 elasticityproject-0.1.1.3/src/elasticityproject/plots3d.py
+-rw-r--r--   0        0        0     1637 2023-05-13 21:01:33.478831 elasticityproject-0.1.1.3/setup.py
+-rw-r--r--   0        0        0     1437 2023-05-13 21:01:33.479140 elasticityproject-0.1.1.3/PKG-INFO
```

### Comparing `elasticityproject-0.1.1.1/LICENSE` & `elasticityproject-0.1.1.3/LICENSE`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 GNU GENERAL PUBLIC LICENSE
                        Version 3, 29 June 2007
 
- Copyright (C) 2023, EEL-USP-Elasticity Group
+ Copyright (C) 2023, EELElasticityGroup
  Everyone is permitted to copy and distribute verbatim copies
  of this license document, but changing it is not allowed.
 
                             Preamble
 
   The GNU General Public License is a free, copyleft license for
 software and other kinds of works.
```

### Comparing `elasticityproject-0.1.1.1/src/elasticityproject/elasticity.py` & `elasticityproject-0.1.1.3/src/elasticityproject/elasticityproject.py`

 * *Files identical despite different names*

### Comparing `elasticityproject-0.1.1.1/src/elasticityproject/plots3d.py` & `elasticityproject-0.1.1.3/src/elasticityproject/plots3d.py`

 * *Files identical despite different names*

