# Comparing `tmp/a_pandas_ex_read_sql-0.10.tar.gz` & `tmp/a_pandas_ex_read_sql-0.11.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "a_pandas_ex_read_sql-0.10.tar", last modified: Thu Nov 17 02:53:20 2022, max compression
+gzip compressed data, was "a_pandas_ex_read_sql-0.11.tar", last modified: Sat May 13 18:14:14 2023, max compression
```

## Comparing `a_pandas_ex_read_sql-0.10.tar` & `a_pandas_ex_read_sql-0.11.tar`

### file list

```diff
@@ -1,19 +1,18 @@
-drwxrwxrwx   0        0        0        0 2022-11-17 02:53:20.776024 a_pandas_ex_read_sql-0.10/
--rw-rw-rw-   0        0        0     1148 2022-11-17 02:53:13.000000 a_pandas_ex_read_sql-0.10/LICENSE.rst
--rw-rw-rw-   0        0        0      169 2022-11-17 02:53:13.000000 a_pandas_ex_read_sql-0.10/MANIFEST.in
--rw-rw-rw-   0        0        0     1179 2022-11-17 02:53:20.776024 a_pandas_ex_read_sql-0.10/PKG-INFO
--rw-rw-rw-   0        0        0      247 2022-11-17 02:50:29.000000 a_pandas_ex_read_sql-0.10/README.md
-drwxrwxrwx   0        0        0        0 2022-11-17 02:53:20.770029 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql/
--rw-rw-rw-   0        0        0     1069 2022-10-02 04:27:48.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql/LICENSE
--rw-rw-rw-   0        0        0      247 2022-11-17 02:50:29.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql/README.MD
--rw-rw-rw-   0        0        0     1010 2022-11-17 02:49:13.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql/__init__.py
--rw-rw-rw-   0        0        0        6 2022-11-17 02:53:19.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql/requirements.txt
--rw-rw-rw-   0        0        0        2 2022-11-17 02:53:19.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql/thirdparty.json
-drwxrwxrwx   0        0        0        0 2022-11-17 02:53:20.776024 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql.egg-info/
--rw-rw-rw-   0        0        0     1179 2022-11-17 02:53:20.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      439 2022-11-17 02:53:20.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-11-17 02:53:20.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        7 2022-11-17 02:53:20.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql.egg-info/requires.txt
--rw-rw-rw-   0        0        0       21 2022-11-17 02:53:20.000000 a_pandas_ex_read_sql-0.10/a_pandas_ex_read_sql.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      115 2022-11-17 02:53:20.776024 a_pandas_ex_read_sql-0.10/setup.cfg
--rw-rw-rw-   0        0        0     1419 2022-11-17 02:53:19.000000 a_pandas_ex_read_sql-0.10/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 18:14:14.442620 a_pandas_ex_read_sql-0.11/
+-rw-rw-rw-   0        0        0     1148 2023-05-13 18:14:07.000000 a_pandas_ex_read_sql-0.11/LICENSE.rst
+-rw-rw-rw-   0        0        0      131 2023-05-13 18:14:06.000000 a_pandas_ex_read_sql-0.11/MANIFEST.in
+-rw-rw-rw-   0        0        0     2738 2023-05-13 18:14:14.442620 a_pandas_ex_read_sql-0.11/PKG-INFO
+-rw-rw-rw-   0        0        0     2084 2023-05-13 18:09:38.000000 a_pandas_ex_read_sql-0.11/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 18:14:14.439628 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql/
+-rw-rw-rw-   0        0        0     2084 2023-05-13 18:09:38.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql/README.MD
+-rw-rw-rw-   0        0        0     6496 2023-05-13 18:01:27.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql/__init__.py
+-rw-rw-rw-   0        0        0      103 2023-05-13 18:14:13.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql/requirements.txt
+-rw-rw-rw-   0        0        0     7182 2023-05-13 18:14:13.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql/thirdparty.json
+drwxrwxrwx   0        0        0        0 2023-05-13 18:14:14.442620 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql.egg-info/
+-rw-rw-rw-   0        0        0     2738 2023-05-13 18:14:14.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      410 2023-05-13 18:14:14.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 18:14:14.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      100 2023-05-13 18:14:14.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       21 2023-05-13 18:14:14.000000 a_pandas_ex_read_sql-0.11/a_pandas_ex_read_sql.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       85 2023-05-13 18:14:14.443617 a_pandas_ex_read_sql-0.11/setup.cfg
+-rw-rw-rw-   0        0        0     1545 2023-05-13 18:14:13.000000 a_pandas_ex_read_sql-0.11/setup.py
```

### Comparing `a_pandas_ex_read_sql-0.10/LICENSE.rst` & `a_pandas_ex_read_sql-0.11/LICENSE.rst`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 
  The MIT License (MIT)
- Copyright (c) 2022 Johannes Fischer
+ Copyright (c) 2023 Johannes Fischer
  
  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:
```

