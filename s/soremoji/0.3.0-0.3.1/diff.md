# Comparing `tmp/soremoji-0.3.0.tar.gz` & `tmp/soremoji-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "soremoji-0.3.0.tar", max compression
+gzip compressed data, was "soremoji-0.3.1.tar", max compression
```

## Comparing `soremoji-0.3.0.tar` & `soremoji-0.3.1.tar`

### file list

```diff
@@ -1,10 +1,9 @@
--rw-r--r--   0        0        0     1061 2023-05-01 06:45:31.890052 soremoji-0.3.0/LICENSE
--rw-r--r--   0        0        0     5411 2023-05-01 06:45:31.890052 soremoji-0.3.0/README.md
--rw-r--r--   0        0        0      369 2023-05-01 06:45:31.890052 soremoji-0.3.0/pyproject.toml
--rw-r--r--   0        0        0      114 2023-05-01 06:45:31.890052 soremoji-0.3.0/soremoji/__init__.py
--rw-r--r--   0        0        0       61 2023-05-01 06:45:31.890052 soremoji-0.3.0/soremoji/__main__.py
--rw-r--r--   0        0        0     1441 2023-05-01 06:45:31.890052 soremoji-0.3.0/soremoji/cli.py
--rw-r--r--   0        0        0     1575 2023-05-01 06:45:31.890052 soremoji-0.3.0/soremoji/command.py
--rw-r--r--   0        0        0     7195 2023-05-01 06:45:31.890052 soremoji-0.3.0/soremoji/emoji.py
--rw-r--r--   0        0        0     1824 2023-05-01 06:45:31.890052 soremoji-0.3.0/soremoji/feature.py
--rw-r--r--   0        0        0     5932 1970-01-01 00:00:00.000000 soremoji-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0     1061 2023-05-13 11:46:17.757243 soremoji-0.3.1/LICENSE
+-rw-r--r--   0        0        0     5411 2023-05-13 11:46:17.757243 soremoji-0.3.1/README.md
+-rw-r--r--   0        0        0      369 2023-05-13 11:46:17.757243 soremoji-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0      114 2023-05-13 11:46:17.757243 soremoji-0.3.1/soremoji/__init__.py
+-rw-r--r--   0        0        0     1441 2023-05-13 11:46:17.757243 soremoji-0.3.1/soremoji/cli.py
+-rw-r--r--   0        0        0     1575 2023-05-13 11:46:17.757243 soremoji-0.3.1/soremoji/command.py
+-rw-r--r--   0        0        0     7195 2023-05-13 11:46:17.757243 soremoji-0.3.1/soremoji/emoji.py
+-rw-r--r--   0        0        0     1824 2023-05-13 11:46:17.757243 soremoji-0.3.1/soremoji/feature.py
+-rw-r--r--   0        0        0     5932 1970-01-01 00:00:00.000000 soremoji-0.3.1/PKG-INFO
```

### Comparing `soremoji-0.3.0/LICENSE` & `soremoji-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `soremoji-0.3.0/README.md` & `soremoji-0.3.1/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -23,15 +23,15 @@
   - repo: https://github.com/psf/black
     rev: 22.6.0
     hooks:
       - id: black
         stages: [commit]
 
   - repo: https://github.com/netsora/soremoji
-    rev: 0.3.0
+    rev: 0.3.1
     hooks:
       - id: soremoji
         stages: [pre-commit-msg]
 ```
 
 ## 使用
```

### Comparing `soremoji-0.3.0/soremoji/cli.py` & `soremoji-0.3.1/soremoji/cli.py`

 * *Files identical despite different names*

### Comparing `soremoji-0.3.0/soremoji/command.py` & `soremoji-0.3.1/soremoji/command.py`

 * *Files identical despite different names*

### Comparing `soremoji-0.3.0/soremoji/emoji.py` & `soremoji-0.3.1/soremoji/emoji.py`

 * *Files identical despite different names*

### Comparing `soremoji-0.3.0/soremoji/feature.py` & `soremoji-0.3.1/soremoji/feature.py`

 * *Files identical despite different names*

### Comparing `soremoji-0.3.0/PKG-INFO` & `soremoji-0.3.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: soremoji
-Version: 0.3.0
+Version: 0.3.1
 Summary: 自维护的 gitmoji-cli，做了部分更改
 License: MIT
 Author: mute.
 Author-email: mute231010@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -39,15 +39,15 @@
   - repo: https://github.com/psf/black
     rev: 22.6.0
     hooks:
       - id: black
         stages: [commit]
 
   - repo: https://github.com/netsora/soremoji
-    rev: 0.3.0
+    rev: 0.3.1
     hooks:
       - id: soremoji
         stages: [pre-commit-msg]
 ```
 
 ## 使用
```

