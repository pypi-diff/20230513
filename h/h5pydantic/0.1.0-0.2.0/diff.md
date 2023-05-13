# Comparing `tmp/h5pydantic-0.1.0.tar.gz` & `tmp/h5pydantic-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "h5pydantic-0.1.0.tar", max compression
+gzip compressed data, was "h5pydantic-0.2.0.tar", max compression
```

## Comparing `h5pydantic-0.1.0.tar` & `h5pydantic-0.2.0.tar`

### file list

```diff
@@ -1,4 +1,4 @@
--rw-r--r--   0        0        0     6207 2023-05-10 01:43:39.954330 h5pydantic-0.1.0/README.md
--rw-r--r--   0        0        0      482 2023-05-10 02:03:28.669613 h5pydantic-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     3246 2023-05-10 01:45:24.603947 h5pydantic-0.1.0/src/h5pydantic/__init__.py
--rw-r--r--   0        0        0     6687 1970-01-01 00:00:00.000000 h5pydantic-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0      340 2023-05-13 03:54:48.206900 h5pydantic-0.2.0/README.md
+-rw-r--r--   0        0        0      997 2023-05-13 04:30:16.241603 h5pydantic-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0     4730 2023-05-13 01:47:30.188229 h5pydantic-0.2.0/src/h5pydantic/__init__.py
+-rw-r--r--   0        0        0     1254 1970-01-01 00:00:00.000000 h5pydantic-0.2.0/PKG-INFO
```

