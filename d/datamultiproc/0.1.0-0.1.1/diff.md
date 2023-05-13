# Comparing `tmp/datamultiproc-0.1.0.tar.gz` & `tmp/datamultiproc-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datamultiproc-0.1.0.tar", max compression
+gzip compressed data, was "datamultiproc-0.1.1.tar", max compression
```

## Comparing `datamultiproc-0.1.0.tar` & `datamultiproc-0.1.1.tar`

### file list

```diff
@@ -1,4 +1,6 @@
--rw-r--r--   0        0        0        0 2023-05-13 13:48:50.442174 datamultiproc-0.1.0/datamultiproc/__init__.py
--rw-r--r--   0        0        0      285 2023-05-13 13:48:35.654208 datamultiproc-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      491 2023-05-13 13:49:04.292452 datamultiproc-0.1.0/setup.py
--rw-r--r--   0        0        0      331 2023-05-13 13:49:04.292560 datamultiproc-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1065 2023-05-13 13:52:01.191826 datamultiproc-0.1.1/LICENSE
+-rw-r--r--   0        0        0      174 2023-05-13 13:53:41.866068 datamultiproc-0.1.1/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 13:52:01.219306 datamultiproc-0.1.1/datamultiproc/__init__.py
+-rw-r--r--   0        0        0      361 2023-05-13 13:56:35.293482 datamultiproc-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0      706 2023-05-13 13:57:24.164876 datamultiproc-0.1.1/setup.py
+-rw-r--r--   0        0        0      600 2023-05-13 13:57:24.164992 datamultiproc-0.1.1/PKG-INFO
```

