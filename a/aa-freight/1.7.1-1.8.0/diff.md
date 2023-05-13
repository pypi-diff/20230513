# Comparing `tmp/aa-freight-1.7.1.tar.gz` & `tmp/aa_freight-1.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aa-freight-1.7.1.tar", last modified: Wed Sep  7 21:06:11 2022, max compression
+gzip compressed data, last modified: Sun Feb  2 00:00:00 2020, max compression
```

## Comparing `aa-freight-1.7.1.tar` & `aa_freight-1.8.0.tar`

### file list

```diff
@@ -1,62 +1,71 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.773525 aa-freight-1.7.1/
--rw-rw-rw-   0 root         (0) root         (0)     1070 2020-10-24 18:25:45.000000 aa-freight-1.7.1/LICENSE
--rw-rw-rw-   0 root         (0) root         (0)      323 2021-02-27 11:50:00.000000 aa-freight-1.7.1/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)    16685 2022-09-07 21:06:11.773525 aa-freight-1.7.1/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)    15772 2022-02-08 12:59:56.000000 aa-freight-1.7.1/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.761525 aa-freight-1.7.1/aa_freight.egg-info/
--rw-r--r--   0 root         (0) root         (0)    16685 2022-09-07 21:06:11.000000 aa-freight-1.7.1/aa_freight.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     1474 2022-09-07 21:06:11.000000 aa-freight-1.7.1/aa_freight.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2022-09-07 21:06:11.000000 aa-freight-1.7.1/aa_freight.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       86 2022-09-07 21:06:11.000000 aa-freight-1.7.1/aa_freight.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       17 2022-09-07 21:06:11.000000 aa-freight-1.7.1/aa_freight.egg-info/top_level.txt
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.765525 aa-freight-1.7.1/freight/
--rw-rw-rw-   0 root         (0) root         (0)       95 2022-09-07 20:42:24.000000 aa-freight-1.7.1/freight/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     6708 2022-09-07 12:59:10.000000 aa-freight-1.7.1/freight/admin.py
--rw-rw-rw-   0 root         (0) root         (0)     2961 2022-02-03 21:44:03.000000 aa-freight-1.7.1/freight/app_settings.py
--rw-rw-rw-   0 root         (0) root         (0)      183 2022-09-07 12:59:10.000000 aa-freight-1.7.1/freight/apps.py
--rw-rw-rw-   0 root         (0) root         (0)     1113 2021-05-06 18:28:15.000000 aa-freight-1.7.1/freight/auth_hooks.py
--rw-rw-rw-   0 root         (0) root         (0)      105 2022-09-07 12:59:10.000000 aa-freight-1.7.1/freight/constants.py
--rw-rw-rw-   0 root         (0) root         (0)     2636 2022-09-07 12:59:10.000000 aa-freight-1.7.1/freight/forms.py
--rw-rw-rw-   0 root         (0) root         (0)     1369 2022-09-07 18:47:36.000000 aa-freight-1.7.1/freight/helpers.py
--rw-rw-rw-   0 root         (0) root         (0)    18034 2022-09-07 18:47:36.000000 aa-freight-1.7.1/freight/managers.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.765525 aa-freight-1.7.1/freight/migrations/
--rw-rw-rw-   0 root         (0) root         (0)    22961 2022-09-07 12:59:10.000000 aa-freight-1.7.1/freight/migrations/0001_squashed.py
--rw-rw-rw-   0 root         (0) root         (0)      980 2022-09-07 12:59:10.000000 aa-freight-1.7.1/freight/migrations/0002_alter_contracthandler_last_error.py
--rw-rw-rw-   0 root         (0) root         (0)        0 2020-10-24 18:25:45.000000 aa-freight-1.7.1/freight/migrations/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    48444 2022-09-07 18:47:36.000000 aa-freight-1.7.1/freight/models.py
--rw-rw-rw-   0 root         (0) root         (0)      236 2022-06-16 21:17:57.000000 aa-freight-1.7.1/freight/providers.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.757525 aa-freight-1.7.1/freight/static/
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.757525 aa-freight-1.7.1/freight/static/freight/
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.765525 aa-freight-1.7.1/freight/static/freight/css/
--rw-rw-rw-   0 root         (0) root         (0)       91 2021-05-06 18:28:15.000000 aa-freight-1.7.1/freight/static/freight/css/calculator.css
--rw-rw-rw-   0 root         (0) root         (0)      396 2021-02-27 11:50:00.000000 aa-freight-1.7.1/freight/static/freight/css/contracts.css
--rw-rw-rw-   0 root         (0) root         (0)     1362 2021-05-06 19:15:24.000000 aa-freight-1.7.1/freight/static/freight/css/kalkoken.css
--rw-rw-rw-   0 root         (0) root         (0)     1148 2021-02-27 11:50:00.000000 aa-freight-1.7.1/freight/static/freight/css/statistics.css
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.769525 aa-freight-1.7.1/freight/static/freight/js/
--rw-rw-rw-   0 root         (0) root         (0)     2568 2022-02-05 16:06:24.000000 aa-freight-1.7.1/freight/static/freight/js/contracts.js
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.757525 aa-freight-1.7.1/freight/static/freight/vendor/
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.769525 aa-freight-1.7.1/freight/static/freight/vendor/datatables/
--rw-rw-rw-   0 root         (0) root         (0)     3250 2020-11-19 23:19:41.000000 aa-freight-1.7.1/freight/static/freight/vendor/datatables/datetime.js
--rw-rw-rw-   0 root         (0) root         (0)   887006 2022-06-16 21:17:57.000000 aa-freight-1.7.1/freight/swagger.json
--rw-rw-rw-   0 root         (0) root         (0)     2364 2022-09-07 18:47:36.000000 aa-freight-1.7.1/freight/tasks.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.757525 aa-freight-1.7.1/freight/templates/
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.769525 aa-freight-1.7.1/freight/templates/freight/
--rw-rw-rw-   0 root         (0) root         (0)      480 2021-02-27 11:50:00.000000 aa-freight-1.7.1/freight/templates/freight/add_location.html
--rw-rw-rw-   0 root         (0) root         (0)      269 2021-05-06 18:28:15.000000 aa-freight-1.7.1/freight/templates/freight/base.html
--rw-rw-rw-   0 root         (0) root         (0)    11837 2022-09-07 12:59:10.000000 aa-freight-1.7.1/freight/templates/freight/calculator.html
--rw-rw-rw-   0 root         (0) root         (0)     1991 2021-05-06 18:28:15.000000 aa-freight-1.7.1/freight/templates/freight/contracts_all.html
--rw-rw-rw-   0 root         (0) root         (0)     1577 2021-05-06 18:28:15.000000 aa-freight-1.7.1/freight/templates/freight/contracts_user.html
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.769525 aa-freight-1.7.1/freight/templates/freight/partials/
--rw-rw-rw-   0 root         (0) root         (0)      718 2021-05-06 18:28:15.000000 aa-freight-1.7.1/freight/templates/freight/partials/contract_table.html
--rw-rw-rw-   0 root         (0) root         (0)      366 2022-07-19 15:47:41.000000 aa-freight-1.7.1/freight/templates/freight/partials/contracts_js_includes.html
--rw-rw-rw-   0 root         (0) root         (0)      762 2021-05-06 18:28:15.000000 aa-freight-1.7.1/freight/templates/freight/partials/contracts_legend.html
--rw-rw-rw-   0 root         (0) root         (0)     2567 2021-05-06 18:28:15.000000 aa-freight-1.7.1/freight/templates/freight/partials/global_js.html
--rw-rw-rw-   0 root         (0) root         (0)     3019 2021-05-06 19:15:24.000000 aa-freight-1.7.1/freight/templates/freight/partials/menu.html
--rw-rw-rw-   0 root         (0) root         (0)    12595 2022-02-05 16:06:24.000000 aa-freight-1.7.1/freight/templates/freight/statistics.html
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-09-07 21:06:11.773525 aa-freight-1.7.1/freight/templatetags/
--rw-rw-rw-   0 root         (0) root         (0)        0 2020-10-24 18:25:45.000000 aa-freight-1.7.1/freight/templatetags/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      504 2020-10-24 18:25:45.000000 aa-freight-1.7.1/freight/templatetags/freight_filters.py
--rw-rw-rw-   0 root         (0) root         (0)     1452 2022-02-07 20:14:52.000000 aa-freight-1.7.1/freight/urls.py
--rw-rw-rw-   0 root         (0) root         (0)    20060 2022-09-07 18:47:36.000000 aa-freight-1.7.1/freight/views.py
--rw-r--r--   0 root         (0) root         (0)       38 2022-09-07 21:06:11.773525 aa-freight-1.7.1/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)     1611 2022-07-19 15:54:47.000000 aa-freight-1.7.1/setup.py
+-rw-r--r--   0        0        0       95 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/__init__.py
+-rw-r--r--   0        0        0     6954 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/admin.py
+-rw-r--r--   0        0        0     2961 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/app_settings.py
+-rw-r--r--   0        0        0      183 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/apps.py
+-rw-r--r--   0        0        0     1113 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/auth_hooks.py
+-rw-r--r--   0        0        0      105 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/constants.py
+-rw-r--r--   0        0        0     2636 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/forms.py
+-rw-r--r--   0        0        0     1369 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/helpers.py
+-rw-r--r--   0        0        0    18034 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/managers.py
+-rw-r--r--   0        0        0    48444 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/models.py
+-rw-r--r--   0        0        0      236 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/providers.py
+-rw-r--r--   0        0        0   887006 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/swagger.json
+-rw-r--r--   0        0        0     2364 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tasks.py
+-rw-r--r--   0        0        0     1452 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/urls.py
+-rw-r--r--   0        0        0    20324 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/views.py
+-rw-r--r--   0        0        0     8026 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/django.pot
+-rw-r--r--   0        0        0     8073 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/de/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8073 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/en/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8073 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/es/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8026 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/fr_FR/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8026 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/it_IT/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8066 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/ja/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8026 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/ko_KR/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8217 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/ru/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8304 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/uk/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0     8066 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/locale/zh_Hans/LC_MESSAGES/django.po
+-rw-r--r--   0        0        0    22960 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/migrations/0001_squashed.py
+-rw-r--r--   0        0        0      979 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/migrations/0002_alter_contracthandler_last_error.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/migrations/__init__.py
+-rw-r--r--   0        0        0       91 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/static/freight/css/calculator.css
+-rw-r--r--   0        0        0      396 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/static/freight/css/contracts.css
+-rw-r--r--   0        0        0     1362 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/static/freight/css/kalkoken.css
+-rw-r--r--   0        0        0     1148 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/static/freight/css/statistics.css
+-rw-r--r--   0        0        0     2568 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/static/freight/js/contracts.js
+-rw-r--r--   0        0        0     3250 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/static/freight/vendor/datatables/datetime.js
+-rw-r--r--   0        0        0      568 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/add_location.html
+-rw-r--r--   0        0        0      269 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/base.html
+-rw-r--r--   0        0        0    13875 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/calculator.html
+-rw-r--r--   0        0        0     2131 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/contracts_all.html
+-rw-r--r--   0        0        0     1577 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/contracts_user.html
+-rw-r--r--   0        0        0    14434 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/statistics.html
+-rw-r--r--   0        0        0      718 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/partials/contract_table.html
+-rw-r--r--   0        0        0      366 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/partials/contracts_js_includes.html
+-rw-r--r--   0        0        0      762 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/partials/contracts_legend.html
+-rw-r--r--   0        0        0     2567 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/partials/global_js.html
+-rw-r--r--   0        0        0     3019 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templates/freight/partials/menu.html
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templatetags/__init__.py
+-rw-r--r--   0        0        0      504 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/templatetags/freight_filters.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/__init__.py
+-rw-r--r--   0        0        0     3138 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/test_admin.py
+-rw-r--r--   0        0        0     1876 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/test_helpers.py
+-rw-r--r--   0        0        0     5514 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/test_integration.py
+-rw-r--r--   0        0        0    35000 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/test_managers.py
+-rw-r--r--   0        0        0    60667 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/test_models.py
+-rw-r--r--   0        0        0     4428 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/test_tasks.py
+-rw-r--r--   0        0        0      993 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/test_templatetags.py
+-rw-r--r--   0        0        0    20751 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/test_views.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/__init__.py
+-rw-r--r--   0        0        0     1555 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/characters.json
+-rw-r--r--   0        0        0    13440 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/contracts.json
+-rw-r--r--   0        0        0     1670 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/factories.py
+-rw-r--r--   0        0        0     2903 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/factories_2.py
+-rw-r--r--   0        0        0     3213 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/generate_contracts.py
+-rw-r--r--   0        0        0     2437 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/generate_contracts_2.py
+-rw-r--r--   0        0        0     6658 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/helpers.py
+-rw-r--r--   0        0        0      722 2020-02-02 00:00:00.000000 aa_freight-1.8.0/freight/tests/testdata/universe_structures.json
+-rw-r--r--   0        0        0      187 2020-02-02 00:00:00.000000 aa_freight-1.8.0/.gitignore
+-rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 aa_freight-1.8.0/LICENSE
+-rw-r--r--   0        0        0    15772 2020-02-02 00:00:00.000000 aa_freight-1.8.0/README.md
+-rw-r--r--   0        0        0     1774 2020-02-02 00:00:00.000000 aa_freight-1.8.0/pyproject.toml
+-rw-r--r--   0        0        0    16881 2020-02-02 00:00:00.000000 aa_freight-1.8.0/PKG-INFO
```

### Comparing `aa-freight-1.7.1/LICENSE` & `aa_freight-1.8.0/LICENSE`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/PKG-INFO` & `aa_freight-1.8.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,31 +1,34 @@
 Metadata-Version: 2.1
 Name: aa-freight
-Version: 1.7.1
+Version: 1.8.0
 Summary: Freight is an Alliance Auth app for running a freight service
-Home-page: https://gitlab.com/ErikKalkoken/aa-freight
-Author: Erik Kalkoken
-Author-email: kaloken87@gmail.com
-License: MIT
-Platform: UNKNOWN
+Project-URL: Homepage, https://gitlab.com/ErikKalkoken/aa-freight
+Author-email: Erik Kalkoken <kaloken87@gmail.com>
+License-Expression: MIT
+License-File: LICENSE
 Classifier: Environment :: Web Environment
 Classifier: Framework :: Django
-Classifier: Framework :: Django :: 3.2
+Classifier: Framework :: Django :: 4.0
 Classifier: Intended Audience :: End Users/Desktop
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Internet :: WWW/HTTP
 Classifier: Topic :: Internet :: WWW/HTTP :: Dynamic Content
-Requires-Python: ~=3.7
+Requires-Python: >=3.8
+Requires-Dist: allianceauth-app-utils>=1.18.0
+Requires-Dist: allianceauth>=3.0.0
+Requires-Dist: dhooks-lite>=0.6.1
+Requires-Dist: django-navhelper
 Description-Content-Type: text/markdown
-License-File: LICENSE
 
 # Freight for Alliance Auth
 
 Freight is an [Alliance Auth](https://gitlab.com/allianceauth/allianceauth) (AA) app for running a freight service.
 
 [![release](https://img.shields.io/pypi/v/aa-freight?label=release)](https://pypi.org/project/aa-freight/)
 [![python](https://img.shields.io/pypi/pyversions/aa-freight)](https://pypi.org/project/aa-freight/)
@@ -287,9 +290,7 @@
 The following parameters will be checked (if they have been defined):
 
 - reward in contract >= calculated reward
 - volume min <= volume in contract <= volume max
 - collateral min <= collateral in contract <= collateral max
 
 Deviations on "Days to expire" and "Days to complete" are currently not part of the contract check and only used to show the recommended contract parameters in the calculator.
-
-
```

### Comparing `aa-freight-1.7.1/README.md` & `aa_freight-1.8.0/README.md`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/admin.py` & `aa_freight-1.8.0/freight/admin.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 from django.conf import settings
 from django.contrib import admin
+from django.utils.translation import gettext_lazy as _
 
 from . import tasks
 from .models import (
     Contract,
     ContractCustomerNotification,
     ContractHandler,
     EveEntity,
@@ -31,26 +32,29 @@
 
     def has_add_permission(self, *args, **kwargs):
         return False
 
     def has_change_permission(self, *args, **kwargs):
         return False
 
-    @admin.display(description="Update selected locations from ESI")
+    @admin.display(description=_("Update selected locations from ESI"))
     def update_location(self, request, queryset):
         location_ids = list()
         for obj in queryset:
             location_ids.append(obj.pk)
 
         update_locations.delay(location_ids)
         self.message_user(
             request,
             (
-                f"Started updating {len(location_ids)} locations. "
-                "This can take a short while to complete."
+                _(
+                    "Started updating %d locations. "
+                    "This can take a short while to complete."
+                )
+                % len(location_ids)
             ),
         )
 
 
 @admin.register(Pricing)
 class PricingAdmin(admin.ModelAdmin):
     list_display = (
@@ -101,32 +105,35 @@
         "last_error",
     )
 
     @admin.display(boolean=True, description="sync ok")
     def _is_sync_ok(self, obj):
         return obj.is_sync_ok
 
-    @admin.display(description="Fetch contracts from Eve Online server")
+    @admin.display(description=_("Fetch contracts from Eve Online server"))
     def start_sync(self, request, queryset):
         for obj in queryset:
             tasks.run_contracts_sync.delay(force_sync=True, user_pk=request.user.pk)
             text = (
-                f"Started syncing contracts for: {obj} "
-                "You will receive a report once it is completed."
+                _(
+                    "Started syncing contracts for: %s "
+                    "You will receive a report once it is completed."
+                )
+                % obj
             )
             self.message_user(request, text)
 
-    @admin.display(description="Send notifications for outstanding contracts")
+    @admin.display(description=_("Send notifications for outstanding contracts"))
     def send_notifications(self, request, queryset):
         for obj in queryset:
             tasks.send_contract_notifications.delay(force_sent=True)
-            text = f"Started sending notifications for: {obj} "
+            text = _("Started sending notifications for: %s ") % obj
             self.message_user(request, text)
 
-    @admin.display(description="Update pricing info for all contracts")
+    @admin.display(description=_("Update pricing info for all contracts"))
     def update_pricing(self, request, queryset):
         del queryset
         tasks.update_contracts_pricing.delay()
         self.message_user(
             request, "Started updating pricing relations for all contracts"
         )
 
@@ -174,33 +181,35 @@
             return "?"
         notifications = [x.status for x in contract.customer_notifications.all()]
         if not notifications:
             return None
         return ", ".join(sorted(notifications, reverse=True))
 
     @admin.display(
-        description="Sent pilots notification for selected contracts to Discord"
+        description=_("Sent pilots notification for selected contracts to Discord")
     )
     def send_pilots_notification(self, request, queryset):
         for obj in queryset:
             obj.send_pilot_notification()
             self.message_user(
                 request,
-                f"Sent pilots notification for contract {obj.contract_id} to Discord",
+                _("Sent pilots notification for contract %d to Discord")
+                % obj.contract_id,
             )
 
     @admin.display(
-        description="Sent customer notification for selected contracts to Discord"
+        description=_("Sent customer notification for selected contracts to Discord")
     )
     def send_customer_notification(self, request, queryset):
         for obj in queryset:
             obj.send_customer_notification(force_sent=True)
             self.message_user(
                 request,
-                f"Sent customer notification for contract {obj.contract_id} to Discord",
+                _("Sent customer notification for contract %d to Discord")
+                % obj.contract_id,
             )
 
     def has_add_permission(self, *args, **kwargs):
         return False
 
     def has_change_permission(self, *args, **kwargs):
         return False
```

### Comparing `aa-freight-1.7.1/freight/app_settings.py` & `aa_freight-1.8.0/freight/app_settings.py`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/auth_hooks.py` & `aa_freight-1.8.0/freight/auth_hooks.py`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/forms.py` & `aa_freight-1.8.0/freight/forms.py`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/helpers.py` & `aa_freight-1.8.0/freight/helpers.py`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/managers.py` & `aa_freight-1.8.0/freight/managers.py`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/migrations/0001_squashed.py` & `aa_freight-1.8.0/freight/migrations/0001_squashed.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,14 @@
 
 import django.core.validators
 import django.db.models.deletion
 from django.db import migrations, models
 
 
 class Migration(migrations.Migration):
-
     # replaces = [
     #     ("freight", "0001_initial_new"),
     #     ("freight", "0002_auto_20191015_1229"),
     #     ("freight", "0003_auto_20191028_1023"),
     #     ("freight", "0004_remove_contract_price"),
     #     ("freight", "0005_auto_20191028_2155"),
     #     ("freight", "0006_auto_20191028_2204"),
```

### Comparing `aa-freight-1.7.1/freight/migrations/0002_alter_contracthandler_last_error.py` & `aa_freight-1.8.0/freight/migrations/0002_alter_contracthandler_last_error.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 # Generated by Django 4.0.7 on 2022-09-07 11:15
 
 from django.db import migrations, models
 
 
 class Migration(migrations.Migration):
-
     dependencies = [
         ("freight", "0001_squashed"),
     ]
 
     operations = [
         migrations.AlterField(
             model_name="contracthandler",
```

### Comparing `aa-freight-1.7.1/freight/models.py` & `aa_freight-1.8.0/freight/models.py`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/static/freight/css/kalkoken.css` & `aa_freight-1.8.0/freight/static/freight/css/kalkoken.css`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/static/freight/css/statistics.css` & `aa_freight-1.8.0/freight/static/freight/css/statistics.css`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/static/freight/js/contracts.js` & `aa_freight-1.8.0/freight/static/freight/js/contracts.js`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/static/freight/vendor/datatables/datetime.js` & `aa_freight-1.8.0/freight/static/freight/vendor/datatables/datetime.js`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/swagger.json` & `aa_freight-1.8.0/freight/swagger.json`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/tasks.py` & `aa_freight-1.8.0/freight/tasks.py`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/templates/freight/calculator.html` & `aa_freight-1.8.0/freight/templates/freight/calculator.html`

 * *Files 22% similar despite different names*

```diff
@@ -8,199 +8,229 @@
 {% block details %}
     <form id="form_calculator" class="form" action="{% url 'freight:calculator' %}" method="POST">
         {% csrf_token %}
         <div class="row">
             <div class="col-md-6">
                 <div class="panel panel-default">
                     <div class="panel-heading">
-                        <h3 class="panel-title">Calculator</h3>
+                        <h3 class="panel-title">{% translate "Calculator" %}</h3>
                     </div>
                     <div class="panel-body">
                         {% if has_pricing %}
                             {{ form|bootstrap }}
                             <br>
-                            <p><strong>Reward</strong></p>
+                            <p><strong>{% translate "Reward" %}</strong></p>
                             <h2 id="text_price">
-                                <span id="text_price_2">{{ price|formatnumber:"0"|default_if_none:"-" }} ISK</span>
+                                <span id="text_price_2">{{ price|formatnumber:"0"|default_if_none:"-" }}
+                                    &nbsp;{% translate "ISK" %}
+                                </span>
                                 <span class="copy_to_clipboard" data-text="{{ price }}">
                                     &nbsp;&nbsp;<i class="far fa-copy"></i></span>
                                 </span>
                             </h2>
-                                <button class="btn btn-success btn-lg" type="submit">Click To Calculate Reward!</button>
+                                <button class="btn btn-success btn-lg" type="submit">
+                                    {% translate "Click To Calculate Reward!" %}
+                                </button>
                         {% else %}
-                            <p class="text-warning">Please define a pricing/route!</p>
+                            <p class="text-warning">
+                                {% translate "Please define a pricing/route!" %}
+                            </p>
                         {% endif %}
                     </div>
                 </div>
             </div>
 
             <div class="col-md-6">
 
                 <div class="panel panel-default">
                     <div class="panel-heading">
-                        <h3 class="panel-title">Pricing details</h3>
+                        <h3 class="panel-title">{% translate "Pricing details" %}</h3>
                     </div>
 
                     <div class="panel-body" style="min-height: 100px;">
 
                         {% if pricing %}
                             <dl class="dl-horizontal">
                                 {% if pricing.is_bidirectional %}
-                                    <dt>From / To:</dt>
+                                    <dt>{% translate "From / To:" %}</dt>
                                 {% else %}
-                                    <dt>From:</dt>
+                                    <dt>{% translate "From:" %}</dt>
                                 {% endif %}
 
                                 <dd>{{ pricing.start_location }}</dd>
 
                                 {% if pricing.is_bidirectional %}
-                                    <dt>From / To:</dt>
+                                    <dt>{% translate "From / To:" %}</dt>
                                 {% else %}
-                                    <dt>To:</dt>
+                                    <dt>{% translate "To:" %}</dt>
                                 {% endif %}
                                 <dd>{{ pricing.end_location }}</dd>
 
-                                <dt>Both directions:</dt>
+                                <dt><dt>{% translate "Both directions:" %}</dt></dt>
                                 <dd>{{ pricing.is_bidirectional|yesno }}</dd>
                                 <br>
 
                                 {% if pricing.price_min != None %}
-                                    <dt>Minimum price:</dt>
-                                    <dd>{{ pricing.price_min|formatnumber:"0" }} ISK</dd>
+                                    <dt>{% translate "Minimum price:" %}</dt>
+                                    <dd>
+                                        {{ pricing.price_min|formatnumber:"0" }}&nbsp;{% translate "ISK" %}
+                                    </dd>
                                 {% endif %}
 
                                 {% if pricing.price_base != None %}
                                     {% if pricing.is_fix_price %}
-                                        <dt>Fix price:</dt>
+                                        <dt>{% translate "Fix price:" %}</dt>
                                     {% else %}
-                                        <dt>Base price:</dt>
+                                        <dt>{% translate "Base price:" %}</dt>
                                     {% endif %}
-                                    <dd>{{ pricing.price_base|formatnumber:"0" }} ISK</dd>
+                                    <dd>{{ pricing.price_base|formatnumber:"0" }}
+                                        &nbsp;{% translate "ISK" %}
+                                    </dd>
                                 {% endif %}
 
                                 {% if pricing_price_per_volume_eff != None %}
-                                    <dt>Price add-on per m3:</dt>
-                                    <dd>{{ pricing_price_per_volume_eff|formatnumber:"0" }} ISK</dd>
+                                    <dt>{% translate "Price add-on per m3:" %}</dt>
+                                    <dd>
+                                        {{ pricing_price_per_volume_eff|formatnumber:"0" }}
+                                        &nbsp;{% translate "ISK" %}
+                                    </dd>
                                 {% endif %}
 
                                 {% if pricing.price_per_collateral_percent != None %}
-                                    <dt>Price add-on collateral:</dt>
+                                    <dt>{% translate "Price add-on collateral:" %}</dt>
                                     <dd>{{ pricing.price_per_collateral_percent }} %</dd>
                                 {% endif %}
 
                                 <br>
                                 {% if pricing.volume_min != None %}
-                                    <dt>Min Volume:</dt>
-                                    <dd>{{ pricing.volume_min|formatnumber:"0"|default_if_none:"-" }} m3</dd>
+                                    <dt>{% translate "Min Volume:" %}</dt>
+                                    <dd>
+                                        {{ pricing.volume_min|formatnumber:"0"|default_if_none:"-" }}
+                                        &nbsp;{% translate "m3" %}
+                                    </dd>
                                 {% endif %}
 
                                 {% if pricing.volume_max != None %}
-                                    <dt>Max Volume:</dt>
-                                    <dd>{{ pricing.volume_max|formatnumber:"0"|default_if_none:"-" }} m3</dd>
+                                    <dt>{% translate "Max Volume:" %}</dt>
+                                    <dd>
+                                        {{ pricing.volume_max|formatnumber:"0"|default_if_none:"-" }}
+                                        &nbsp;{% translate "m3" %}
+                                    </dd>
                                 {% endif %}
 
                                 {% if pricing.collateral_min != None %}
-                                    <dt>Min. Collateral:</dt>
-                                    <dd>{{ pricing.collateral_min|formatnumber:"0" }} ISK</dd>
+                                    <dt>{% translate "Min. Collateral:" %}</dt>
+                                    <dd>
+                                        {{ pricing.collateral_min|formatnumber:"0" }}
+                                        &nbsp;{% translate "ISK" %}
+                                    </dd>
                                 {% endif %}
 
                                 {% if pricing.collateral_max != None %}
-                                    <dt>Max. Collateral:</dt>
-                                    <dd>{{ pricing.collateral_max|formatnumber:"0" }} ISK</dd>
+                                    <dt>{% translate "Max. Collateral:" %}</dt>
+                                    <dd>
+                                        {{ pricing.collateral_max|formatnumber:"0" }}
+                                        &nbsp;{% translate "ISK" %}
+                                    </dd>
                                 {% endif %}
 
                                 <br>
 
                                 {% if pricing.details %}
-                                    <dt>Additional Instructions:</dt>
+                                    <dt>{% translate "Additional Instructions:" %}</dt>
                                     <dd>{{ pricing.details|linebreaks }}</dd>
                                 {% endif %}
 
                             </dl>
 
                         {% else %}
-                            <p class="text-warning">Please define a pricing/route!</p>
+                            <p class="text-warning">{% translate "Please define a pricing/route!" %}</p>
                         {% endif %}
 
                     </div>
                 </div>
 
                 <div class="panel panel-default">
                     <div class="panel-heading">
-                        <h3 class="panel-title">Your contract</h3>
+                        <h3 class="panel-title">{% translate "Your contract" %}</h3>
                     </div>
                     <div class="panel-body" style="min-height: 100px;">
                         {% if price != None %}
                             <dl class="dl-horizontal">
-                                <dt>Contract Type:</dt>
-                                <dd>Courier</dd>
+                                <dt>{% translate "Contract Type:" %}</dt>
+                                <dd>{% translate "Courier" %}</dd>
 
-                                <dt>Availability:</dt>
+                                <dt>{% translate "Availability:" %}</dt>
                                 <dd>{{ availability }}</dd>
 
-                                <dt>Location:</dt>
+                                <dt>{% translate "Location:" %}</dt>
                                 <dd>
                                     {{ pricing.start_location }}
                                     <span class="copy_to_clipboard" data-text="{{ pricing.start_location }}">
                                         &nbsp;&nbsp;<i class="far fa-copy"></i></span>
                                     </span>
                                 </dd>
 
                                 <hr>
 
-                                <dt>Ship To:</dt>
+                                <dt>{% translate "Ship To:" %}</dt>
                                 <dd>
                                     {{ pricing.end_location }}
                                     <span class="copy_to_clipboard" data-text="{{ pricing.end_location }}">
                                         &nbsp;&nbsp;<i class="far fa-copy"></i></span>
                                     </span>
                                 </dd>
 
-                                <dt>Reward:</dt>
+                                <dt>{% translate "Reward:" %}</dt>
                                 <dd>
-                                    {{ price|formatnumber:"0"|default_if_none:"???" }} ISK
+                                    {{ price|formatnumber:"0"|default_if_none:"???" }}
+                                    &nbsp;{% translate "ISK" %}
                                     <span class="copy_to_clipboard" data-text="{{ price }}">
                                         &nbsp;&nbsp;<i class="far fa-copy"></i></span>
                                     </span>
                                 </dd>
 
-                                <dt>Collateral:</dt>
+                                <dt>{% translate "Collateral:" %}</dt>
                                 <dd>
-                                    {{ collateral|formatnumber:"0"|default_if_none:"???" }} ISK
+                                    {{ collateral|formatnumber:"0"|default_if_none:"???" }}
+                                    &nbsp;{% translate "ISK" %}
                                     <span class="copy_to_clipboard" data-text="{{ collateral }}">
                                         &nbsp;&nbsp;<i class="far fa-copy"></i></span>
                                     </span>
                                 </dd>
 
                                 {% if pricing.days_to_expire %}
-                                    <dt>Expiration:</dt>
-                                    <dd>{{ pricing.days_to_expire }} days ({{ expires_on|date:'Y-m-d' }})</dd>
+                                    <dt>{% translate "Expiration:" %}</dt>
+                                    <dd>{{ pricing.days_to_expire }} {% translate "days" %} ({{ expires_on|date:'Y-m-d' }})</dd>
                                 {% endif %}
 
                                 {% if pricing.days_to_complete %}
-                                    <dt>Days to complete:</dt>
+                                    <dt>{% translate "Days to complete:" %}</dt>
                                     <dd>
                                         {{ pricing.days_to_complete|default_if_none:"-" }}
                                         <span class="copy_to_clipboard" data-text="{{ pricing.days_to_complete }}">
                                             &nbsp;&nbsp;<i class="far fa-copy"></i></span>
                                         </span>
                                     </dd>
                                 {% endif %}
 
                                 {% if pricing.requires_volume %}
-                                    <dt>Volume:</dt>
-                                    <dd>{{ volume|formatnumber:"0"|default_if_none:"???" }} m3</dd>
+                                    <dt>{% translate "Volume:" %}</dt>
+                                    <dd>
+                                        {{ volume|formatnumber:"0"|default_if_none:"???" }}
+                                        &nbsp;{% translate "m3" %}
+                                    </dd>
                                 {% endif %}
 
                                 <hr>
-                                Note that this route is bidirectional, so Location and Destination can be switched.
+                                {% translate "Note that this route is bidirectional, so Location and Destination can be switched." %}
                             </dl>
 
                         {% else %}
-                            <p class="text-muted">No price calculated yet</p>
+                            <p class="text-muted">{% translate "No price calculated yet" %}</p>
                         {% endif %}
                     </div>
                 </div>
 
             </div>
         </div>
```

### Comparing `aa-freight-1.7.1/freight/templates/freight/contracts_all.html` & `aa_freight-1.8.0/freight/templates/freight/contracts_all.html`

 * *Files 7% similar despite different names*

```diff
@@ -3,16 +3,24 @@
 {% load humanize %}
 {% load static %}
 
 {% block details %}
 
     <!-- Nav tabs -->
     <ul class="nav nav-tabs" role="tablist">
-        <li role="presentation" class="active"><a href="#active_contracts" aria-controls="active_contracts" role="tab" data-toggle="tab">Active</a></li>
-        <li role="presentation"><a href="#all_contracts" aria-controls="all_contracts" role="tab" data-toggle="tab">All</a></li>
+        <li role="presentation" class="active">
+            <a href="#active_contracts" aria-controls="active_contracts" role="tab" data-toggle="tab">
+                {% translate "Active" %}
+            </a>
+        </li>
+        <li role="presentation">
+            <a href="#all_contracts" aria-controls="all_contracts" role="tab" data-toggle="tab">
+                {% translate "All" %}
+            </a>
+        </li>
     </ul>
 
     <div class="panel panel-default panel-tab">
         <div class="panel-body">
             <div class="tab-content">
                 <div role="tabpanel" class="tab-pane active" id="active_contracts">
                     {% include "freight/partials/contract_table.html" with tab_name="tab_active_contracts" %}
```

### Comparing `aa-freight-1.7.1/freight/templates/freight/contracts_user.html` & `aa_freight-1.8.0/freight/templates/freight/contracts_user.html`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/templates/freight/partials/contract_table.html` & `aa_freight-1.8.0/freight/templates/freight/partials/contract_table.html`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/templates/freight/partials/contracts_legend.html` & `aa_freight-1.8.0/freight/templates/freight/partials/contracts_legend.html`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/templates/freight/partials/global_js.html` & `aa_freight-1.8.0/freight/templates/freight/partials/global_js.html`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/templates/freight/partials/menu.html` & `aa_freight-1.8.0/freight/templates/freight/partials/menu.html`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/urls.py` & `aa_freight-1.8.0/freight/urls.py`

 * *Files identical despite different names*

### Comparing `aa-freight-1.7.1/freight/views.py` & `aa_freight-1.8.0/freight/views.py`

 * *Files 2% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 from django.contrib.auth.decorators import login_required, permission_required
 from django.db.models import Count, Q, Sum
 from django.forms import HiddenInput
 from django.http import JsonResponse
 from django.shortcuts import get_object_or_404, redirect, render
 from django.utils.html import format_html
 from django.utils.timezone import now
+from django.utils.translation import gettext_lazy as _
 from esi.decorators import token_required
 from esi.models import Token
 
 from allianceauth.authentication.models import CharacterOwnership
 from allianceauth.eveonline.models import EveCharacter, EveCorporationInfo
 from allianceauth.services.hooks import get_extension_logger
 from app_utils.logging import LoggerAddTag
@@ -48,15 +49,15 @@
         **context,
     }
     return new_context
 
 
 @login_required
 @permission_required("freight.basic_access")
-def index(_):
+def index(request):
     return redirect("freight:calculator")
 
 
 @login_required
 @permission_required("freight.use_calculator")
 def contract_list_user(request):
     try:
@@ -257,75 +258,82 @@
     token_char = get_object_or_404(EveCharacter, character_id=token.character_id)
     if (
         Freight.category_for_operation_mode(FREIGHT_OPERATION_MODE)
         == EveEntity.CATEGORY_ALLIANCE
     ) and token_char.alliance_id is None:
         messages.error(
             request,
-            "Can not setup contract handler, "
-            "because {} is not a member of any alliance".format(token_char),
+            _(
+                "Can not setup contract handler, "
+                "because %s is not a member of any alliance"
+            )
+            % token_char,
         )
         success = False
 
     owned_char = None
     if success:
         try:
             owned_char = CharacterOwnership.objects.get(
                 user=request.user, character=token_char
             )
         except CharacterOwnership.DoesNotExist:
             messages.error(
                 request,
-                format_html(
+                _(
                     "You can only use your main or alt characters to setup "
-                    " the contract handler. "
-                    "However, character <strong>{}</strong> is neither. ",
-                    token_char.character_name,
-                ),
+                    "the contract handler. "
+                    "However, character %s is neither. ",
+                )
+                % token_char.character_name,
             )
             success = False
 
     if success:
         handler = ContractHandler.objects.first()
         if handler and handler.operation_mode != FREIGHT_OPERATION_MODE:
             messages.error(
                 request,
-                "There already is a contract handler installed for a "
-                "different operation mode. You need to first delete the "
-                "existing contract handler in the admin section "
-                "before you can set up this app for a different operation mode.",
+                _(
+                    "There already is a contract handler installed for a "
+                    "different operation mode. You need to first delete the "
+                    "existing contract handler in the admin section "
+                    "before you can set up this app for a different operation mode."
+                ),
             )
             success = False
 
     if success:
-        organization, _ = update_or_create_eve_entity_from_evecharacter(
+        organization = update_or_create_eve_entity_from_evecharacter(
             token_char, Freight.category_for_operation_mode(FREIGHT_OPERATION_MODE)
-        )
+        )[0]
 
-        handler, _ = ContractHandler.objects.update_or_create(
+        handler = ContractHandler.objects.update_or_create(
             organization=organization,
             defaults={
                 "character": owned_char,
                 "operation_mode": FREIGHT_OPERATION_MODE,
             },
-        )
+        )[0]
         tasks.run_contracts_sync.delay(force_sync=True, user_pk=request.user.pk)
         messages.success(
             request,
-            format_html(
+            _(
                 "Contract Handler setup started for "
-                "<strong>{}</strong> organization "
-                "with <strong>{}</strong> as sync character. "
-                "Operation mode: <strong>{}</strong>. "
+                "%(organization)s organization "
+                "with %(character)s as sync character. "
+                "Operation mode: %(operation_mode)s. "
                 "Started syncing of courier contracts. "
-                "You will receive a report once it is completed.",
-                organization.name,
-                handler.character.character.character_name,
-                handler.operation_mode_friendly,
-            ),
+                "You will receive a report once it is completed."
+            )
+            % {
+                "organization": organization.name,
+                "character": handler.character.character.character_name,
+                "operation_mode": handler.operation_mode_friendly,
+            },
         )
     return redirect("freight:index")
 
 
 @login_required
 @token_required(scopes=Location.get_esi_scopes())
 @permission_required("freight.add_location")
@@ -352,25 +360,27 @@
             try:
                 location, created = Location.objects.update_or_create_esi(
                     token=token, location_id=location_id, add_unknown=False
                 )
             except OSError as ex:
                 messages.error(
                     request,
-                    "Failed to add location with token from {} "
-                    "for location ID {}: {}".format(
-                        token.character_name, location_id, type(ex).__name__
-                    ),
+                    _(
+                        "Failed to add location with token from %(character)s "
+                        "for location ID %(id)s: %(error)s"
+                    )
+                    % {
+                        "character": token.character_name,
+                        "id": location_id,
+                        "error": type(ex).__name__,
+                    },
                 )
             else:
-                action_txt = "Added:" if created else "Updated:"
-                messages.success(
-                    request,
-                    format_html("{} <strong>{}</strong>", action_txt, location.name),
-                )
+                action_txt = _("Added:") if created else _("Updated:")
+                messages.success(request, f"{action_txt} {location.name}")
                 return redirect("freight:add_location_2")
     context = {
         "page_title": "Add / Update Location",
         "form": form,
         "token_char_name": token.character_name,
     }
     return render(
```

