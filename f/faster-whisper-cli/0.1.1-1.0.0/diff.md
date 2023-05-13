# Comparing `tmp/faster_whisper_cli-0.1.1.tar.gz` & `tmp/faster_whisper_cli-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "faster_whisper_cli-0.1.1.tar", max compression
+gzip compressed data, was "faster_whisper_cli-1.0.0.tar", max compression
```

## Comparing `faster_whisper_cli-0.1.1.tar` & `faster_whisper_cli-1.0.0.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0        0 2023-05-13 05:37:21.049722 faster_whisper_cli-0.1.1/faster_whisper_cli/__init__.py
--rw-r--r--   0        0        0     1353 2023-05-13 05:26:04.350409 faster_whisper_cli-0.1.1/faster_whisper_cli/cli.py
--rw-r--r--   0        0        0      456 2023-05-13 06:18:35.662372 faster_whisper_cli-0.1.1/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-13 05:37:21.051346 faster_whisper_cli-0.1.1/README.md
--rw-r--r--   0        0        0      450 1970-01-01 00:00:00.000000 faster_whisper_cli-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-05-13 05:37:21.049722 faster_whisper_cli-1.0.0/faster_whisper_cli/__init__.py
+-rw-r--r--   0        0        0     8774 2023-05-13 09:16:33.081448 faster_whisper_cli-1.0.0/faster_whisper_cli/cli.py
+-rw-r--r--   0        0        0      456 2023-05-13 09:18:15.263791 faster_whisper_cli-1.0.0/pyproject.toml
+-rw-r--r--   0        0        0     2318 2023-05-13 09:03:58.379166 faster_whisper_cli-1.0.0/README.md
+-rw-r--r--   0        0        0     2719 1970-01-01 00:00:00.000000 faster_whisper_cli-1.0.0/PKG-INFO
```

