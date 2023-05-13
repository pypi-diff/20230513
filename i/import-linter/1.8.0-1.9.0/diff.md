# Comparing `tmp/import-linter-1.8.0.tar.gz` & `tmp/import-linter-1.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "import-linter-1.8.0.tar", last modified: Fri Mar  3 15:57:18 2023, max compression
+gzip compressed data, was "import-linter-1.9.0.tar", last modified: Sat May 13 17:13:06 2023, max compression
```

## Comparing `import-linter-1.8.0.tar` & `import-linter-1.9.0.tar`

### file list

```diff
@@ -1,63 +1,62 @@
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.283362 import-linter-1.8.0/
--rw-r--r--   0 david.seddon   (501) staff       (20)      555 2023-01-10 11:25:44.000000 import-linter-1.8.0/AUTHORS.rst
--rw-r--r--   0 david.seddon   (501) staff       (20)     1315 2022-02-17 08:16:10.000000 import-linter-1.8.0/LICENSE
--rw-r--r--   0 david.seddon   (501) staff       (20)     4334 2023-03-03 15:57:18.283460 import-linter-1.8.0/PKG-INFO
--rw-r--r--   0 david.seddon   (501) staff       (20)     3158 2022-12-02 13:44:09.000000 import-linter-1.8.0/README.rst
--rw-r--r--   0 david.seddon   (501) staff       (20)      209 2022-08-22 11:28:15.000000 import-linter-1.8.0/pyproject.toml
--rw-r--r--   0 david.seddon   (501) staff       (20)      217 2023-03-03 15:57:18.283822 import-linter-1.8.0/setup.cfg
--rwxr-xr-x   0 david.seddon   (501) staff       (20)     2158 2023-03-03 15:56:09.000000 import-linter-1.8.0/setup.py
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.271055 import-linter-1.8.0/src/
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.274380 import-linter-1.8.0/src/import_linter.egg-info/
--rw-r--r--   0 david.seddon   (501) staff       (20)     4334 2023-03-03 15:57:18.000000 import-linter-1.8.0/src/import_linter.egg-info/PKG-INFO
--rw-r--r--   0 david.seddon   (501) staff       (20)     1895 2023-03-03 15:57:18.000000 import-linter-1.8.0/src/import_linter.egg-info/SOURCES.txt
--rw-r--r--   0 david.seddon   (501) staff       (20)        1 2023-03-03 15:57:18.000000 import-linter-1.8.0/src/import_linter.egg-info/dependency_links.txt
--rw-r--r--   0 david.seddon   (501) staff       (20)       72 2023-03-03 15:57:18.000000 import-linter-1.8.0/src/import_linter.egg-info/entry_points.txt
--rw-r--r--   0 david.seddon   (501) staff       (20)        1 2022-02-17 08:16:33.000000 import-linter-1.8.0/src/import_linter.egg-info/not-zip-safe
--rw-r--r--   0 david.seddon   (501) staff       (20)       89 2023-03-03 15:57:18.000000 import-linter-1.8.0/src/import_linter.egg-info/requires.txt
--rw-r--r--   0 david.seddon   (501) staff       (20)       13 2023-03-03 15:57:18.000000 import-linter-1.8.0/src/import_linter.egg-info/top_level.txt
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.275529 import-linter-1.8.0/src/importlinter/
--rw-r--r--   0 david.seddon   (501) staff       (20)      300 2023-03-03 15:56:09.000000 import-linter-1.8.0/src/importlinter/__init__.py
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.276724 import-linter-1.8.0/src/importlinter/adapters/
--rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/adapters/__init__.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      643 2023-03-03 15:54:46.000000 import-linter-1.8.0/src/importlinter/adapters/building.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      547 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/adapters/filesystem.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      398 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/adapters/printing.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      170 2022-04-04 12:57:31.000000 import-linter-1.8.0/src/importlinter/adapters/timing.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     4024 2023-01-27 09:19:47.000000 import-linter-1.8.0/src/importlinter/adapters/user_options.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     1256 2022-08-18 07:37:36.000000 import-linter-1.8.0/src/importlinter/api.py
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.278618 import-linter-1.8.0/src/importlinter/application/
--rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/application/__init__.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      661 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/application/app_config.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     2487 2022-03-30 08:56:22.000000 import-linter-1.8.0/src/importlinter/application/contract_utils.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      755 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/application/file_finding.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     4216 2023-01-10 11:24:41.000000 import-linter-1.8.0/src/importlinter/application/output.py
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.280024 import-linter-1.8.0/src/importlinter/application/ports/
--rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/application/ports/__init__.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      364 2023-03-03 15:54:46.000000 import-linter-1.8.0/src/importlinter/application/ports/building.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      713 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/application/ports/filesystem.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      300 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/application/ports/printing.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     2010 2022-09-08 15:16:44.000000 import-linter-1.8.0/src/importlinter/application/ports/reporting.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     1215 2022-10-04 12:42:31.000000 import-linter-1.8.0/src/importlinter/application/ports/timing.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      264 2022-08-16 09:59:53.000000 import-linter-1.8.0/src/importlinter/application/ports/user_options.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     4079 2022-11-02 17:04:52.000000 import-linter-1.8.0/src/importlinter/application/rendering.py
--rw-r--r--   0 david.seddon   (501) staff       (20)       28 2023-03-03 15:54:46.000000 import-linter-1.8.0/src/importlinter/application/sentinels.py
--rw-r--r--   0 david.seddon   (501) staff       (20)    11185 2023-03-03 15:54:46.000000 import-linter-1.8.0/src/importlinter/application/use_cases.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      833 2023-03-03 11:24:24.000000 import-linter-1.8.0/src/importlinter/application/user_options.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     3514 2023-03-03 15:54:46.000000 import-linter-1.8.0/src/importlinter/cli.py
--rw-r--r--   0 david.seddon   (501) staff       (20)      680 2023-03-03 15:54:46.000000 import-linter-1.8.0/src/importlinter/configuration.py
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.281311 import-linter-1.8.0/src/importlinter/contracts/
--rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/contracts/__init__.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     6910 2023-01-27 08:53:23.000000 import-linter-1.8.0/src/importlinter/contracts/_common.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     8079 2023-01-27 08:53:23.000000 import-linter-1.8.0/src/importlinter/contracts/forbidden.py
--rw-r--r--   0 david.seddon   (501) staff       (20)    10818 2022-10-04 13:06:35.000000 import-linter-1.8.0/src/importlinter/contracts/independence.py
--rw-r--r--   0 david.seddon   (501) staff       (20)    17453 2023-01-27 08:53:23.000000 import-linter-1.8.0/src/importlinter/contracts/layers.py
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.282600 import-linter-1.8.0/src/importlinter/domain/
--rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/domain/__init__.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     3901 2022-12-05 16:03:56.000000 import-linter-1.8.0/src/importlinter/domain/contract.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     7177 2022-12-05 16:03:56.000000 import-linter-1.8.0/src/importlinter/domain/fields.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     7784 2023-01-27 08:53:23.000000 import-linter-1.8.0/src/importlinter/domain/helpers.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     3063 2022-08-22 11:28:15.000000 import-linter-1.8.0/src/importlinter/domain/imports.py
-drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-03-03 15:57:18.283127 import-linter-1.8.0/src/importlinter/domain/ports/
--rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.8.0/src/importlinter/domain/ports/__init__.py
--rw-r--r--   0 david.seddon   (501) staff       (20)     2672 2023-01-27 08:53:23.000000 import-linter-1.8.0/src/importlinter/domain/ports/graph.py
--rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-10-04 12:42:31.000000 import-linter-1.8.0/src/importlinter/py.typed
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.566094 import-linter-1.9.0/
+-rw-r--r--   0 david.seddon   (501) staff       (20)      555 2023-01-10 11:25:44.000000 import-linter-1.9.0/AUTHORS.rst
+-rw-r--r--   0 david.seddon   (501) staff       (20)     1315 2022-02-17 08:16:10.000000 import-linter-1.9.0/LICENSE
+-rw-r--r--   0 david.seddon   (501) staff       (20)     4289 2023-05-13 17:13:06.566225 import-linter-1.9.0/PKG-INFO
+-rw-r--r--   0 david.seddon   (501) staff       (20)     3158 2022-12-02 13:44:09.000000 import-linter-1.9.0/README.rst
+-rw-r--r--   0 david.seddon   (501) staff       (20)     1861 2023-05-13 17:11:47.000000 import-linter-1.9.0/pyproject.toml
+-rw-r--r--   0 david.seddon   (501) staff       (20)      137 2023-05-13 17:13:06.566612 import-linter-1.9.0/setup.cfg
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.549725 import-linter-1.9.0/src/
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.553275 import-linter-1.9.0/src/import_linter.egg-info/
+-rw-r--r--   0 david.seddon   (501) staff       (20)     4289 2023-05-13 17:13:06.000000 import-linter-1.9.0/src/import_linter.egg-info/PKG-INFO
+-rw-r--r--   0 david.seddon   (501) staff       (20)     1886 2023-05-13 17:13:06.000000 import-linter-1.9.0/src/import_linter.egg-info/SOURCES.txt
+-rw-r--r--   0 david.seddon   (501) staff       (20)        1 2023-05-13 17:13:06.000000 import-linter-1.9.0/src/import_linter.egg-info/dependency_links.txt
+-rw-r--r--   0 david.seddon   (501) staff       (20)       71 2023-05-13 17:13:06.000000 import-linter-1.9.0/src/import_linter.egg-info/entry_points.txt
+-rw-r--r--   0 david.seddon   (501) staff       (20)        1 2022-02-17 08:16:33.000000 import-linter-1.9.0/src/import_linter.egg-info/not-zip-safe
+-rw-r--r--   0 david.seddon   (501) staff       (20)       89 2023-05-13 17:13:06.000000 import-linter-1.9.0/src/import_linter.egg-info/requires.txt
+-rw-r--r--   0 david.seddon   (501) staff       (20)       13 2023-05-13 17:13:06.000000 import-linter-1.9.0/src/import_linter.egg-info/top_level.txt
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.554607 import-linter-1.9.0/src/importlinter/
+-rw-r--r--   0 david.seddon   (501) staff       (20)      300 2023-05-13 17:11:47.000000 import-linter-1.9.0/src/importlinter/__init__.py
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.556148 import-linter-1.9.0/src/importlinter/adapters/
+-rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/adapters/__init__.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      643 2023-03-03 15:54:46.000000 import-linter-1.9.0/src/importlinter/adapters/building.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      547 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/adapters/filesystem.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      398 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/adapters/printing.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      170 2022-04-04 12:57:31.000000 import-linter-1.9.0/src/importlinter/adapters/timing.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     4024 2023-01-27 09:19:47.000000 import-linter-1.9.0/src/importlinter/adapters/user_options.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     1256 2022-08-18 07:37:36.000000 import-linter-1.9.0/src/importlinter/api.py
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.558309 import-linter-1.9.0/src/importlinter/application/
+-rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/application/__init__.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      661 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/application/app_config.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     2471 2023-05-05 10:50:40.000000 import-linter-1.9.0/src/importlinter/application/contract_utils.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      755 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/application/file_finding.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     4216 2023-01-10 11:24:41.000000 import-linter-1.9.0/src/importlinter/application/output.py
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.559953 import-linter-1.9.0/src/importlinter/application/ports/
+-rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/application/ports/__init__.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      364 2023-03-03 15:54:46.000000 import-linter-1.9.0/src/importlinter/application/ports/building.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      713 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/application/ports/filesystem.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      300 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/application/ports/printing.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     2010 2022-09-08 15:16:44.000000 import-linter-1.9.0/src/importlinter/application/ports/reporting.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     1215 2022-10-04 12:42:31.000000 import-linter-1.9.0/src/importlinter/application/ports/timing.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      264 2022-08-16 09:59:53.000000 import-linter-1.9.0/src/importlinter/application/ports/user_options.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     4079 2022-11-02 17:04:52.000000 import-linter-1.9.0/src/importlinter/application/rendering.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)       28 2023-03-03 15:54:46.000000 import-linter-1.9.0/src/importlinter/application/sentinels.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)    11185 2023-03-03 15:54:46.000000 import-linter-1.9.0/src/importlinter/application/use_cases.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      833 2023-03-03 11:24:24.000000 import-linter-1.9.0/src/importlinter/application/user_options.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     3514 2023-05-13 16:25:02.000000 import-linter-1.9.0/src/importlinter/cli.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)      680 2023-03-03 15:54:46.000000 import-linter-1.9.0/src/importlinter/configuration.py
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.562999 import-linter-1.9.0/src/importlinter/contracts/
+-rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/contracts/__init__.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     6811 2023-05-13 16:03:45.000000 import-linter-1.9.0/src/importlinter/contracts/_common.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     8535 2023-05-13 17:10:28.000000 import-linter-1.9.0/src/importlinter/contracts/forbidden.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)    10742 2023-05-05 10:50:40.000000 import-linter-1.9.0/src/importlinter/contracts/independence.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)    17453 2023-01-27 08:53:23.000000 import-linter-1.9.0/src/importlinter/contracts/layers.py
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.565202 import-linter-1.9.0/src/importlinter/domain/
+-rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/domain/__init__.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     3901 2022-12-05 16:03:56.000000 import-linter-1.9.0/src/importlinter/domain/contract.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     7177 2022-12-05 16:03:56.000000 import-linter-1.9.0/src/importlinter/domain/fields.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     7734 2023-05-05 10:50:40.000000 import-linter-1.9.0/src/importlinter/domain/helpers.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     3063 2022-08-22 11:28:15.000000 import-linter-1.9.0/src/importlinter/domain/imports.py
+drwxr-xr-x   0 david.seddon   (501) staff       (20)        0 2023-05-13 17:13:06.565815 import-linter-1.9.0/src/importlinter/domain/ports/
+-rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-02-17 08:16:10.000000 import-linter-1.9.0/src/importlinter/domain/ports/__init__.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)     2672 2023-01-27 08:53:23.000000 import-linter-1.9.0/src/importlinter/domain/ports/graph.py
+-rw-r--r--   0 david.seddon   (501) staff       (20)        0 2022-10-04 12:42:31.000000 import-linter-1.9.0/src/importlinter/py.typed
```

### Comparing `import-linter-1.8.0/AUTHORS.rst` & `import-linter-1.9.0/AUTHORS.rst`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/LICENSE` & `import-linter-1.9.0/LICENSE`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/PKG-INFO` & `import-linter-1.9.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,15 @@
 Metadata-Version: 2.1
 Name: import-linter
-Version: 1.8.0
+Version: 1.9.0
 Summary: Enforces rules for the imports within and between Python packages.
-Home-page: UNKNOWN
-Author: David Seddon
-Author-email: david@seddonym.me
+Author-email: David Seddon <david@seddonym.me>
 License: BSD 2-Clause License
 Project-URL: Documentation, https://import-linter.readthedocs.io/
-Project-URL: Source code, https://github.com/seddonym/import-linter/
-Platform: UNKNOWN
+Project-URL: Source-code, https://github.com/seddonym/import-linter/
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: Unix
 Classifier: Operating System :: POSIX
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Programming Language :: Python
@@ -127,9 +124,7 @@
     -----------------------------
 
     myproject.foo is not allowed to import myproject.bar:
 
     -   myproject.foo.blue -> myproject.utils.red (l.16)
         myproject.utils.red -> myproject.utils.green (l.1)
         myproject.utils.green -> myproject.bar.yellow (l.3)
-
-
```

### Comparing `import-linter-1.8.0/README.rst` & `import-linter-1.9.0/README.rst`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/setup.py` & `import-linter-1.9.0/pyproject.toml`

 * *Files 21% similar despite different names*

```diff
@@ -1,63 +1,74 @@
-#!/usr/bin/env python
-# -*- encoding: utf-8 -*-
-import io
-from glob import glob
-from os.path import basename, dirname, join, splitext
-
-from setuptools import find_packages, setup
-
-
-def read(*names, **kwargs):
-    with io.open(
-        join(dirname(__file__), *names), encoding=kwargs.get("encoding", "utf8")
-    ) as fh:
-        return fh.read()
-
-
-setup(
-    name="import-linter",
-    version="1.8.0",
-    license="BSD 2-Clause License",
-    description="Enforces rules for the imports within and between Python packages.",
-    long_description=read("README.rst"),
-    long_description_content_type="text/x-rst",
-    author="David Seddon",
-    author_email="david@seddonym.me",
-    project_urls={
-        "Documentation": "https://import-linter.readthedocs.io/",
-        "Source code": "https://github.com/seddonym/import-linter/",
-    },
-    packages=find_packages("src"),
-    package_data={"importlinter": ["py.typed"]},
-    package_dir={"": "src"},
-    py_modules=[splitext(basename(path))[0] for path in glob("src/*.py")],
-    include_package_data=True,
-    zip_safe=False,
-    classifiers=[
-        # complete classifier list: http://pypi.python.org/pypi?%3Aaction=list_classifiers
-        "Development Status :: 5 - Production/Stable",
-        "Intended Audience :: Developers",
-        "License :: OSI Approved :: BSD License",
-        "Operating System :: Unix",
-        "Operating System :: POSIX",
-        "Operating System :: Microsoft :: Windows",
-        "Programming Language :: Python",
-        "Programming Language :: Python :: 3.7",
-        "Programming Language :: Python :: 3.8",
-        "Programming Language :: Python :: 3.9",
-        "Programming Language :: Python :: 3.10",
-        "Programming Language :: Python :: 3.11",
-        "Programming Language :: Python :: Implementation :: CPython",
-        "Topic :: Utilities",
-    ],
-    python_requires=">=3.7",
-    install_requires=[
-        "click>=6",
-        "grimp>=2.3",
-        "tomli>=1.2.1; python_version < '3.11'",
-        "typing-extensions>=3.10.0.0",
-    ],
-    entry_points={
-        "console_scripts": ["lint-imports = importlinter.cli:lint_imports_command"]
-    },
-)
+[build-system]
+requires = ["setuptools>=61.2"]
+build-backend = "setuptools.build_meta"
+
+[project]
+name = "import-linter"
+version = "1.9.0"
+license = {text = "BSD 2-Clause License"}
+description = "Enforces rules for the imports within and between Python packages."
+authors = [
+    {name = "David Seddon", email = "david@seddonym.me"},
+]
+requires-python = ">=3.7"
+dependencies = [
+    "click>=6",
+    "grimp>=2.4",
+    "tomli>=1.2.1; python_version < '3.11'",
+    "typing-extensions>=3.10.0.0",
+]
+classifiers = [
+    "Development Status :: 5 - Production/Stable",
+    "Intended Audience :: Developers",
+    "License :: OSI Approved :: BSD License",
+    "Operating System :: Unix",
+    "Operating System :: POSIX",
+    "Operating System :: Microsoft :: Windows",
+    "Programming Language :: Python",
+    "Programming Language :: Python :: 3.7",
+    "Programming Language :: Python :: 3.8",
+    "Programming Language :: Python :: 3.9",
+    "Programming Language :: Python :: 3.10",
+    "Programming Language :: Python :: 3.11",
+    "Programming Language :: Python :: Implementation :: CPython",
+    "Topic :: Utilities",
+]
+dynamic = ["readme"]
+
+[project.urls]
+Documentation = "https://import-linter.readthedocs.io/"
+Source-code = "https://github.com/seddonym/import-linter/"
+
+[project.scripts]
+lint-imports = "importlinter.cli:lint_imports_command"
+
+[tool.setuptools]
+include-package-data = true
+zip-safe = false
+
+[tool.setuptools.dynamic]
+readme = {file = "README.rst"}
+
+[tool.setuptools.package-data]
+importlinter = ["py.typed"]
+
+[tool.setuptools.packages.find]
+where = ["src"]
+namespaces = false
+
+[tool.black]
+line-length = 99
+
+[tool.isort]
+multi_line_output = 3
+include_trailing_comma = "True"
+force_grid_wrap = 0
+use_parentheses = "True"
+line_length = 99
+
+[tool.mypy]
+exclude = [
+    '^tests/assets/',
+]
+warn_unused_ignores = true
+warn_redundant_casts = true
```

### Comparing `import-linter-1.8.0/src/import_linter.egg-info/PKG-INFO` & `import-linter-1.9.0/src/import_linter.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,15 @@
 Metadata-Version: 2.1
 Name: import-linter
-Version: 1.8.0
+Version: 1.9.0
 Summary: Enforces rules for the imports within and between Python packages.
-Home-page: UNKNOWN
-Author: David Seddon
-Author-email: david@seddonym.me
+Author-email: David Seddon <david@seddonym.me>
 License: BSD 2-Clause License
 Project-URL: Documentation, https://import-linter.readthedocs.io/
-Project-URL: Source code, https://github.com/seddonym/import-linter/
-Platform: UNKNOWN
+Project-URL: Source-code, https://github.com/seddonym/import-linter/
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: Unix
 Classifier: Operating System :: POSIX
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Programming Language :: Python
@@ -127,9 +124,7 @@
     -----------------------------
 
     myproject.foo is not allowed to import myproject.bar:
 
     -   myproject.foo.blue -> myproject.utils.red (l.16)
         myproject.utils.red -> myproject.utils.green (l.1)
         myproject.utils.green -> myproject.bar.yellow (l.3)
-
-
```

### Comparing `import-linter-1.8.0/src/import_linter.egg-info/SOURCES.txt` & `import-linter-1.9.0/src/import_linter.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,12 @@
 AUTHORS.rst
 LICENSE
 README.rst
 pyproject.toml
 setup.cfg
-setup.py
 src/import_linter.egg-info/PKG-INFO
 src/import_linter.egg-info/SOURCES.txt
 src/import_linter.egg-info/dependency_links.txt
 src/import_linter.egg-info/entry_points.txt
 src/import_linter.egg-info/not-zip-safe
 src/import_linter.egg-info/requires.txt
 src/import_linter.egg-info/top_level.txt
```

### Comparing `import-linter-1.8.0/src/importlinter/adapters/building.py` & `import-linter-1.9.0/src/importlinter/adapters/building.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/adapters/filesystem.py` & `import-linter-1.9.0/src/importlinter/adapters/filesystem.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/adapters/user_options.py` & `import-linter-1.9.0/src/importlinter/adapters/user_options.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/api.py` & `import-linter-1.9.0/src/importlinter/api.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/app_config.py` & `import-linter-1.9.0/src/importlinter/application/app_config.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/contract_utils.py` & `import-linter-1.9.0/src/importlinter/application/contract_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -34,15 +34,15 @@
     """
     imports, unresolved_expressions = helpers.resolve_import_expressions(
         graph=graph, expressions=ignore_imports if ignore_imports else []
     )
 
     warnings = _handle_unresolved_import_expressions(
         unresolved_expressions,
-        unmatched_alerting,  # type: ignore
+        unmatched_alerting,
     )
 
     helpers.pop_imports(graph, imports)
 
     return warnings
```

### Comparing `import-linter-1.8.0/src/importlinter/application/file_finding.py` & `import-linter-1.9.0/src/importlinter/application/file_finding.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/output.py` & `import-linter-1.9.0/src/importlinter/application/output.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/ports/filesystem.py` & `import-linter-1.9.0/src/importlinter/application/ports/filesystem.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/ports/reporting.py` & `import-linter-1.9.0/src/importlinter/application/ports/reporting.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/ports/timing.py` & `import-linter-1.9.0/src/importlinter/application/ports/timing.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/rendering.py` & `import-linter-1.9.0/src/importlinter/application/rendering.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/use_cases.py` & `import-linter-1.9.0/src/importlinter/application/use_cases.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/application/user_options.py` & `import-linter-1.9.0/src/importlinter/application/user_options.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/cli.py` & `import-linter-1.9.0/src/importlinter/cli.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/configuration.py` & `import-linter-1.9.0/src/importlinter/configuration.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/contracts/_common.py` & `import-linter-1.9.0/src/importlinter/contracts/_common.py`

 * *Files 3% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 Helper functions used by more than one contract type.
 
 Code in here should not be relied upon as a public API; if you're
 relying on it for a custom contract type, be aware things may change
 without warning.
 """
 
-from typing import List, Optional, Sequence, Tuple, Union, cast
+from typing import List, Optional, Sequence, Tuple, Union
 
 from typing_extensions import TypedDict
 
 from importlinter.application import output
 from importlinter.domain.imports import Module
 from importlinter.domain.ports.graph import ImportGraph
 
@@ -58,15 +58,15 @@
         segment: List[Link] = []
         for importer_in_chain, imported_in_chain in [
             (chain[i], chain[i + 1]) for i in range(len(chain) - 1)
         ]:
             import_details = reference_graph.get_import_details(
                 importer=importer_in_chain, imported=imported_in_chain
             )
-            line_numbers = tuple(sorted(set(cast(int, j["line_number"]) for j in import_details)))
+            line_numbers = tuple(sorted(set(j["line_number"] for j in import_details)))
             segment.append(
                 {
                     "importer": importer_in_chain,
                     "imported": imported_in_chain,
                     "line_numbers": line_numbers,
                 }
             )
@@ -86,17 +86,15 @@
             m
             for m in candidate_modules
             if Module(m) == importer or Module(m).is_descendant_of(importer)
         ]:
             import_details_list = graph.get_import_details(
                 importer=module, imported=imported_module
             )
-            line_numbers = tuple(
-                sorted(set(cast(int, j["line_number"]) for j in import_details_list))
-            )
+            line_numbers = tuple(sorted(set(j["line_number"] for j in import_details_list)))
             head_imports.append(
                 {"importer": module, "imported": imported_module, "line_numbers": line_numbers}
             )
 
         tail_imports: List[Link] = []
         importer_module = segment[-1]["importer"]
         candidate_modules = sorted(graph.find_modules_directly_imported_by(importer_module))
@@ -104,17 +102,15 @@
             m
             for m in candidate_modules
             if Module(m) == imported or Module(m).is_descendant_of(imported)
         ]:
             import_details_list = graph.get_import_details(
                 importer=importer_module, imported=module
             )
-            line_numbers = tuple(
-                sorted(set(cast(int, j["line_number"]) for j in import_details_list))
-            )
+            line_numbers = tuple(sorted(set(j["line_number"] for j in import_details_list)))
             tail_imports.append(
                 {"importer": importer_module, "imported": module, "line_numbers": line_numbers}
             )
 
         collapsed_chains.append(
             {
                 "chain": [head_imports[0]] + segment[1:-1] + [tail_imports[0]],
```

### Comparing `import-linter-1.8.0/src/importlinter/contracts/forbidden.py` & `import-linter-1.9.0/src/importlinter/contracts/forbidden.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,8 +1,9 @@
-from typing import Tuple, cast
+from __future__ import annotations
+from typing import List, Tuple, cast
 
 from importlinter.application import contract_utils, output
 from importlinter.application.contract_utils import AlertLevel
 from importlinter.configuration import settings
 from importlinter.domain import fields
 from importlinter.domain.contract import Contract, ContractCheck
 from importlinter.domain.imports import Module
@@ -43,15 +44,15 @@
         warnings = contract_utils.remove_ignored_imports(
             graph=graph,
             ignore_imports=self.ignore_imports,  # type: ignore
             unmatched_alerting=self.unmatched_ignore_imports_alerting,  # type: ignore
         )
 
         self._check_all_modules_exist_in_graph(graph)
-        self._check_external_forbidden_modules(graph)
+        self._check_external_forbidden_modules()
 
         # We only need to check for illegal imports for forbidden modules that are in the graph.
         forbidden_modules_in_graph = [
             m for m in self.forbidden_modules if m.name in graph.modules  # type: ignore
         ]
 
         for source_module in self.source_modules:  # type: ignore
@@ -139,26 +140,35 @@
             output.new_line()
 
     def _check_all_modules_exist_in_graph(self, graph: ImportGraph) -> None:
         for module in self.source_modules:  # type: ignore
             if module.name not in graph.modules:
                 raise ValueError(f"Module '{module.name}' does not exist.")
 
-    def _check_external_forbidden_modules(self, graph: ImportGraph) -> None:
-        if (
-            self._contains_external_forbidden_modules(graph)
-            and not self._graph_was_built_with_externals()
-        ):
-            raise ValueError(
-                "The top level configuration must have include_external_packages=True "
-                "when there are external forbidden modules."
-            )
+    def _check_external_forbidden_modules(self) -> None:
+        external_forbidden_modules = self._get_external_forbidden_modules()
+        if external_forbidden_modules:
+            if self._graph_was_built_with_externals():
+                for module in external_forbidden_modules:
+                    if module.root_package_name != module.name:
+                        raise ValueError(
+                            f"Invalid forbidden module {module}: "
+                            "subpackages of external packages are not valid."
+                        )
+            else:
+                raise ValueError(
+                    "The top level configuration must have include_external_packages=True "
+                    "when there are external forbidden modules."
+                )
 
-    def _contains_external_forbidden_modules(self, graph: ImportGraph) -> bool:
+    def _get_external_forbidden_modules(self) -> set[Module]:
         root_packages = [Module(name) for name in self.session_options["root_packages"]]
-        return not all(
-            any(forbidden_module.is_in_package(root_package) for root_package in root_packages)
-            for forbidden_module in self.forbidden_modules  # type: ignore
-        )
+        return {
+            forbidden_module
+            for forbidden_module in cast(List[Module], self.forbidden_modules)
+            if not any(
+                forbidden_module.is_in_package(root_package) for root_package in root_packages
+            )
+        }
 
     def _graph_was_built_with_externals(self) -> bool:
         return str(self.session_options.get("include_external_packages")).lower() == "true"
```

### Comparing `import-linter-1.8.0/src/importlinter/contracts/independence.py` & `import-linter-1.9.0/src/importlinter/contracts/independence.py`

 * *Files 2% similar despite different names*

```diff
@@ -61,15 +61,15 @@
             unmatched_alerting=self.unmatched_ignore_imports_alerting,  # type: ignore
         )
 
         self._check_all_modules_exist_in_graph(graph)
 
         temp_graph = copy.deepcopy(graph)
         # First pass: direct imports.
-        for subpackage_1, subpackage_2 in permutations(modules, r=2):  # type: ignore
+        for subpackage_1, subpackage_2 in permutations(modules, r=2):
             output.verbose_print(
                 verbose,
                 "Searching for direct imports from " f"{subpackage_1} to {subpackage_2}...",
             )
             with settings.TIMER as timer:
                 direct_chains = self._pop_direct_imports(
                     importer_package=subpackage_1,
@@ -90,15 +90,15 @@
                 output.print(
                     f"Found {chain_count} illegal chain{pluralized} "
                     f"in {timer.duration_in_s}s.",
                 )
 
         # Second pass: indirect imports.
         self._squash_modules(graph=temp_graph, modules_to_squash=modules)
-        for subpackage_1, subpackage_2 in permutations(modules, r=2):  # type: ignore
+        for subpackage_1, subpackage_2 in permutations(modules, r=2):
             output.verbose_print(
                 verbose,
                 "Searching for indirect imports from " f"{subpackage_1} to {subpackage_2}...",
             )
             with settings.TIMER as timer:
                 other_independent_packages = [
                     m for m in modules if m not in (subpackage_1, subpackage_2)
@@ -206,21 +206,21 @@
 
         for importer_module in importer_modules:
             for imported_module in imported_modules:
                 import_details = graph.get_import_details(
                     importer=importer_module, imported=imported_module
                 )
                 if import_details:
-                    line_numbers = tuple(cast(int, i["line_number"]) for i in import_details)
+                    line_numbers = tuple(i["line_number"] for i in import_details)
                     direct_imports.append(
                         {
                             "chain": [
                                 {
-                                    "importer": cast(str, import_details[0]["importer"]),
-                                    "imported": cast(str, import_details[0]["imported"]),
+                                    "importer": import_details[0]["importer"],
+                                    "imported": import_details[0]["imported"],
                                     "line_numbers": line_numbers,
                                 }
                             ],
                             "extra_firsts": [],
                             "extra_lasts": [],
                         }
                     )
@@ -246,15 +246,15 @@
         if chains:
             for chain in chains:
                 chain_data: List[Link] = []
                 for importer, imported in [
                     (chain[i], chain[i + 1]) for i in range(len(chain) - 1)
                 ]:
                     import_details = graph.get_import_details(importer=importer, imported=imported)
-                    line_numbers = tuple(cast(int, j["line_number"]) for j in import_details)
+                    line_numbers = tuple(j["line_number"] for j in import_details)
                     chain_data.append(
                         {
                             "importer": importer,
                             "imported": imported,
                             "line_numbers": line_numbers,
                         }
                     )
```

### Comparing `import-linter-1.8.0/src/importlinter/contracts/layers.py` & `import-linter-1.9.0/src/importlinter/contracts/layers.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/domain/contract.py` & `import-linter-1.9.0/src/importlinter/domain/contract.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/domain/fields.py` & `import-linter-1.9.0/src/importlinter/domain/fields.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/domain/helpers.py` & `import-linter-1.9.0/src/importlinter/domain/helpers.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import itertools
 import re
-from typing import Iterable, List, Pattern, Set, Tuple, cast
+from typing import Iterable, List, Pattern, Set, Tuple
 
 from grimp import DetailedImport
 
 from importlinter.domain.imports import DirectImport, ImportExpression, Module
 from importlinter.domain.ports.graph import ImportGraph
 
 
@@ -58,18 +58,18 @@
     for (importer, imported) in _expression_to_modules(expression, graph):
         import_details = graph.get_import_details(importer=importer.name, imported=imported.name)
 
         if import_details:
             for individual_import_details in import_details:
                 imports.add(
                     DirectImport(
-                        importer=Module(cast(str, individual_import_details["importer"])),
-                        imported=Module(cast(str, individual_import_details["imported"])),
-                        line_number=cast(int, individual_import_details["line_number"]),
-                        line_contents=cast(str, individual_import_details["line_contents"]),
+                        importer=Module(individual_import_details["importer"]),
+                        imported=Module(individual_import_details["imported"]),
+                        line_number=individual_import_details["line_number"],
+                        line_contents=individual_import_details["line_contents"],
                     )
                 )
             matched = True
 
     if not matched:
         raise MissingImport(
             f"Ignored import expression {expression} didn't match anything in the graph."
```

### Comparing `import-linter-1.8.0/src/importlinter/domain/imports.py` & `import-linter-1.9.0/src/importlinter/domain/imports.py`

 * *Files identical despite different names*

### Comparing `import-linter-1.8.0/src/importlinter/domain/ports/graph.py` & `import-linter-1.9.0/src/importlinter/domain/ports/graph.py`

 * *Files identical despite different names*

