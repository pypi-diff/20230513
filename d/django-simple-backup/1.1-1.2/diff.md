# Comparing `tmp/django-simple-backup-1.1.tar.gz` & `tmp/django-simple-backup-1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/django-simple-backup-1.1.tar", last modified: Sat May 13 18:20:38 2023, max compression
+gzip compressed data, was "dist/django-simple-backup-1.2.tar", last modified: Sat May 13 18:25:37 2023, max compression
```

## Comparing `django-simple-backup-1.1.tar` & `django-simple-backup-1.2.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/
--rw-r--r--   0 evgeny     (501) staff       (20)      261 2023-05-13 18:20:38.000000 django-simple-backup-1.1/PKG-INFO
--rw-r--r--   0 evgeny     (501) staff       (20)       89 2023-05-13 16:03:45.000000 django-simple-backup-1.1/MANIFEST.in
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/docs/
--rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.1/docs/Makefile
--rw-r--r--   0 evgeny     (501) staff       (20)      435 2023-05-13 18:20:00.000000 django-simple-backup-1.1/setup.py
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/
--rw-r--r--   0 evgeny     (501) staff       (20)      261 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/PKG-INFO
--rw-r--r--   0 evgeny     (501) staff       (20)      399 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/SOURCES.txt
--rw-r--r--   0 evgeny     (501) staff       (20)       14 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/top_level.txt
--rw-r--r--   0 evgeny     (501) staff       (20)        1 2023-05-13 18:20:38.000000 django-simple-backup-1.1/django_simple_backup.egg-info/dependency_links.txt
--rw-r--r--   0 evgeny     (501) staff       (20)       38 2023-05-13 18:20:38.000000 django-simple-backup-1.1/setup.cfg
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/simple_backup/
--rw-r--r--   0 evgeny     (501) staff       (20)       88 2023-05-13 16:03:45.000000 django-simple-backup-1.1/simple_backup/signals.py
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/simple_backup/management/
--rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.1/simple_backup/management/__init__.py
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:20:38.000000 django-simple-backup-1.1/simple_backup/management/commands/
--rw-r--r--   0 evgeny     (501) staff       (20)     7761 2023-05-13 16:07:11.000000 django-simple-backup-1.1/simple_backup/management/commands/backup.py
--rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.1/simple_backup/management/commands/__init__.py
--rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.1/simple_backup/__init__.py
--rw-r--r--   0 evgeny     (501) staff       (20)     1527 2023-05-13 16:03:45.000000 django-simple-backup-1.1/README.rst
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/
+-rw-r--r--   0 evgeny     (501) staff       (20)     2093 2023-05-13 18:25:37.000000 django-simple-backup-1.2/PKG-INFO
+-rw-r--r--   0 evgeny     (501) staff       (20)       89 2023-05-13 16:03:45.000000 django-simple-backup-1.2/MANIFEST.in
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/docs/
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.2/docs/Makefile
+-rw-r--r--   0 evgeny     (501) staff       (20)      542 2023-05-13 18:24:56.000000 django-simple-backup-1.2/setup.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/
+-rw-r--r--   0 evgeny     (501) staff       (20)     2093 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/PKG-INFO
+-rw-r--r--   0 evgeny     (501) staff       (20)      399 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/SOURCES.txt
+-rw-r--r--   0 evgeny     (501) staff       (20)       14 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/top_level.txt
+-rw-r--r--   0 evgeny     (501) staff       (20)        1 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/dependency_links.txt
+-rw-r--r--   0 evgeny     (501) staff       (20)       38 2023-05-13 18:25:37.000000 django-simple-backup-1.2/setup.cfg
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/simple_backup/
+-rw-r--r--   0 evgeny     (501) staff       (20)       88 2023-05-13 16:03:45.000000 django-simple-backup-1.2/simple_backup/signals.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/simple_backup/management/
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.2/simple_backup/management/__init__.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/simple_backup/management/commands/
+-rw-r--r--   0 evgeny     (501) staff       (20)     7761 2023-05-13 16:07:11.000000 django-simple-backup-1.2/simple_backup/management/commands/backup.py
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.2/simple_backup/management/commands/__init__.py
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.2/simple_backup/__init__.py
+-rw-r--r--   0 evgeny     (501) staff       (20)     1527 2023-05-13 16:03:45.000000 django-simple-backup-1.2/README.rst
```

### Comparing `django-simple-backup-1.1/simple_backup/management/commands/backup.py` & `django-simple-backup-1.2/simple_backup/management/commands/backup.py`

 * *Files identical despite different names*

### Comparing `django-simple-backup-1.1/README.rst` & `django-simple-backup-1.2/README.rst`

 * *Files identical despite different names*

