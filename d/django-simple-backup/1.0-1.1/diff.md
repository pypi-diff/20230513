# Comparing `tmp/django-simple-backup-1.0.tar.gz` & `tmp/django-simple-backup-1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/django-simple-backup-1.0.tar", last modified: Sat Nov  1 22:36:40 2014, max compression
+gzip compressed data, was "dist/django-simple-backup-1.1.tar", last modified: Sat May 13 18:20:38 2023, max compression
```

## Comparing `django-simple-backup-1.0.tar` & `django-simple-backup-1.1.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 22:36:40.000000 django-simple-backup-1.0/
-drwxr-xr-x   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 22:36:40.000000 django-simple-backup-1.0/django_simple_backup.egg-info/
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)        1 2014-11-01 22:36:40.000000 django-simple-backup-1.0/django_simple_backup.egg-info/dependency_links.txt
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)      241 2014-11-01 22:36:40.000000 django-simple-backup-1.0/django_simple_backup.egg-info/PKG-INFO
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)      399 2014-11-01 22:36:40.000000 django-simple-backup-1.0/django_simple_backup.egg-info/SOURCES.txt
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)       14 2014-11-01 22:36:40.000000 django-simple-backup-1.0/django_simple_backup.egg-info/top_level.txt
-drwxr-xr-x   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 22:36:40.000000 django-simple-backup-1.0/docs/
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 18:14:45.000000 django-simple-backup-1.0/docs/Makefile
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)       89 2014-11-01 22:35:06.000000 django-simple-backup-1.0/MANIFEST.in
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)      241 2014-11-01 22:36:40.000000 django-simple-backup-1.0/PKG-INFO
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)     1527 2014-11-01 21:59:48.000000 django-simple-backup-1.0/README.rst
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)       59 2014-11-01 22:36:40.000000 django-simple-backup-1.0/setup.cfg
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)      409 2014-11-01 21:15:39.000000 django-simple-backup-1.0/setup.py
-drwxr-xr-x   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 22:36:40.000000 django-simple-backup-1.0/simple_backup/
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 18:14:45.000000 django-simple-backup-1.0/simple_backup/__init__.py
-drwxr-xr-x   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 22:36:40.000000 django-simple-backup-1.0/simple_backup/management/
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 18:14:45.000000 django-simple-backup-1.0/simple_backup/management/__init__.py
-drwxr-xr-x   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 22:36:40.000000 django-simple-backup-1.0/simple_backup/management/commands/
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)        0 2014-11-01 18:14:45.000000 django-simple-backup-1.0/simple_backup/management/commands/__init__.py
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)     7761 2014-11-01 22:22:22.000000 django-simple-backup-1.0/simple_backup/management/commands/backup.py
--rw-r--r--   0 evgenyfadeev   (501) staff       (20)       88 2014-11-01 22:05:20.000000 django-simple-backup-1.0/simple_backup/signals.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/
+-rw-r--r--   0 evgeny     (501) staff       (20)      261 2023-05-13 18:20:38.000000 django-simple-backup-1.1/PKG-INFO
+-rw-r--r--   0 evgeny     (501) staff       (20)       89 2023-05-13 16:03:45.000000 django-simple-backup-1.1/MANIFEST.in
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/docs/
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.1/docs/Makefile
+-rw-r--r--   0 evgeny     (501) staff       (20)      435 2023-05-13 18:20:00.000000 django-simple-backup-1.1/setup.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/
+-rw-r--r--   0 evgeny     (501) staff       (20)      261 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/PKG-INFO
+-rw-r--r--   0 evgeny     (501) staff       (20)      399 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/SOURCES.txt
+-rw-r--r--   0 evgeny     (501) staff       (20)       14 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/top_level.txt
+-rw-r--r--   0 evgeny     (501) staff       (20)        1 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/dependency_links.txt
+-rw-r--r--   0 evgeny     (501) staff       (20)       38 2023-05-13 18:20:38.000000 django-simple-backup-1.1/setup.cfg
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/simple_backup/
+-rw-r--r--   0 evgeny     (501) staff       (20)       88 2023-05-13 16:03:45.000000 django-simple-backup-1.1/simple_backup/signals.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/simple_backup/management/
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.1/simple_backup/management/__init__.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/simple_backup/management/commands/
+-rw-r--r--   0 evgeny     (501) staff       (20)     7761 2023-05-13 16:07:11.000000 django-simple-backup-1.1/simple_backup/management/commands/backup.py
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.1/simple_backup/management/commands/__init__.py
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.1/simple_backup/__init__.py
+-rw-r--r--   0 evgeny     (501) staff       (20)     1527 2023-05-13 16:03:45.000000 django-simple-backup-1.1/README.rst
```

### Comparing `django-simple-backup-1.0/README.rst` & `django-simple-backup-1.1/README.rst`

 * *Files identical despite different names*

### Comparing `django-simple-backup-1.0/simple_backup/management/commands/backup.py` & `django-simple-backup-1.1/simple_backup/management/commands/backup.py`

 * *Files identical despite different names*

