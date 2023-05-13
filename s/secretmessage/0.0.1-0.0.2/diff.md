# Comparing `tmp/secretmessage-0.0.1.tar.gz` & `tmp/secretmessage-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "secretmessage-0.0.1.tar", last modified: Sat May 13 10:13:45 2023, max compression
+gzip compressed data, was "secretmessage-0.0.2.tar", last modified: Sat May 13 08:00:44 2023, max compression
```

## Comparing `secretmessage-0.0.1.tar` & `secretmessage-0.0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 10:13:45.006343 secretmessage-0.0.1/
--rw-rw----   0 root         (0) everybody  (9997)     1061 2023-05-12 17:08:36.000000 secretmessage-0.0.1/LICENSE
--rw-rw----   0 root         (0) everybody  (9997)       54 2023-05-12 17:10:16.000000 secretmessage-0.0.1/MANIFEST.in
--rw-rw----   0 root         (0) everybody  (9997)     2573 2023-05-13 10:13:45.006343 secretmessage-0.0.1/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)     2140 2023-05-12 19:51:42.000000 secretmessage-0.0.1/README.md
--rw-rw----   0 root         (0) everybody  (9997)      103 2023-05-12 19:37:43.000000 secretmessage-0.0.1/pyproject.toml
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 10:13:44.946343 secretmessage-0.0.1/secretmessage/
--rw-rw----   0 root         (0) everybody  (9997)     1762 2023-05-12 17:57:05.000000 secretmessage-0.0.1/secretmessage/__init__.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 10:13:45.006343 secretmessage-0.0.1/secretmessage.egg-info/
--rw-rw----   0 root         (0) everybody  (9997)     2573 2023-05-13 10:13:44.000000 secretmessage-0.0.1/secretmessage.egg-info/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)      228 2023-05-13 10:13:44.000000 secretmessage-0.0.1/secretmessage.egg-info/SOURCES.txt
--rw-rw----   0 root         (0) everybody  (9997)        1 2023-05-13 10:13:44.000000 secretmessage-0.0.1/secretmessage.egg-info/dependency_links.txt
--rw-rw----   0 root         (0) everybody  (9997)       14 2023-05-13 10:13:44.000000 secretmessage-0.0.1/secretmessage.egg-info/top_level.txt
--rw-rw----   0 root         (0) everybody  (9997)      521 2023-05-13 10:13:45.016343 secretmessage-0.0.1/setup.cfg
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 08:00:44.667859 secretmessage-0.0.2/
+-rw-rw----   0 root         (0) everybody  (9997)     1061 2023-05-12 17:08:36.000000 secretmessage-0.0.2/LICENSE
+-rw-rw----   0 root         (0) everybody  (9997)       54 2023-05-12 17:10:16.000000 secretmessage-0.0.2/MANIFEST.in
+-rw-rw----   0 root         (0) everybody  (9997)     2573 2023-05-13 08:00:44.667859 secretmessage-0.0.2/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)     2140 2023-05-12 19:51:42.000000 secretmessage-0.0.2/README.md
+-rw-rw----   0 root         (0) everybody  (9997)      103 2023-05-12 19:37:43.000000 secretmessage-0.0.2/pyproject.toml
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 08:00:44.597859 secretmessage-0.0.2/secretmessage/
+-rw-rw----   0 root         (0) everybody  (9997)     1762 2023-05-12 17:57:05.000000 secretmessage-0.0.2/secretmessage/__init__.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-05-13 08:00:44.657859 secretmessage-0.0.2/secretmessage.egg-info/
+-rw-rw----   0 root         (0) everybody  (9997)     2573 2023-05-13 08:00:44.000000 secretmessage-0.0.2/secretmessage.egg-info/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)      228 2023-05-13 08:00:44.000000 secretmessage-0.0.2/secretmessage.egg-info/SOURCES.txt
+-rw-rw----   0 root         (0) everybody  (9997)        1 2023-05-13 08:00:44.000000 secretmessage-0.0.2/secretmessage.egg-info/dependency_links.txt
+-rw-rw----   0 root         (0) everybody  (9997)       14 2023-05-13 08:00:44.000000 secretmessage-0.0.2/secretmessage.egg-info/top_level.txt
+-rw-rw----   0 root         (0) everybody  (9997)      521 2023-05-13 08:00:44.667859 secretmessage-0.0.2/setup.cfg
```

### Comparing `secretmessage-0.0.1/LICENSE` & `secretmessage-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `secretmessage-0.0.1/PKG-INFO` & `secretmessage-0.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: secretmessage
-Version: 0.0.1
+Version: 0.0.2
 Summary: For generating Messages Secretly.
 Home-page: https://github.com/PurpleBird7613/secretmessage
 Author: E Lusifa Taehyung
 Author-email: purplebird7613@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `secretmessage-0.0.1/README.md` & `secretmessage-0.0.2/README.md`

 * *Files identical despite different names*

### Comparing `secretmessage-0.0.1/secretmessage/__init__.py` & `secretmessage-0.0.2/secretmessage/__init__.py`

 * *Files identical despite different names*

### Comparing `secretmessage-0.0.1/secretmessage.egg-info/PKG-INFO` & `secretmessage-0.0.2/secretmessage.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: secretmessage
-Version: 0.0.1
+Version: 0.0.2
 Summary: For generating Messages Secretly.
 Home-page: https://github.com/PurpleBird7613/secretmessage
 Author: E Lusifa Taehyung
 Author-email: purplebird7613@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `secretmessage-0.0.1/setup.cfg` & `secretmessage-0.0.2/setup.cfg`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = secretmessage
-version = 0.0.1
+version = 0.0.2
 author = E Lusifa Taehyung
 author_email = purplebird7613@gmail.com
 description = For generating Messages Secretly.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/PurpleBird7613/secretmessage
 classifiers =
```

