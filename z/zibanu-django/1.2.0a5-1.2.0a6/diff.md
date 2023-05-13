# Comparing `tmp/zibanu-django-1.2.0a5.tar.gz` & `tmp/zibanu-django-1.2.0a6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zibanu-django-1.2.0a5.tar", last modified: Tue Apr 11 22:56:50 2023, max compression
+gzip compressed data, was "zibanu-django-1.2.0a6.tar", last modified: Sat May 13 14:29:57 2023, max compression
```

## Comparing `zibanu-django-1.2.0a5.tar` & `zibanu-django-1.2.0a6.tar`

### file list

```diff
@@ -1,139 +1,147 @@
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.692224 zibanu-django-1.2.0a5/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)    35148 2022-05-01 19:35:15.000000 zibanu-django-1.2.0a5/LICENSE
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      207 2023-03-31 15:51:33.000000 zibanu-django-1.2.0a5/MANIFEST.in
--rw-r--r--   0 macercha  (1000) macercha  (1000)    41365 2023-04-11 22:56:50.692224 zibanu-django-1.2.0a5/PKG-INFO
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      158 2023-01-18 12:15:22.000000 zibanu-django-1.2.0a5/README.md
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      849 2023-04-11 22:55:00.000000 zibanu-django-1.2.0a5/pyproject.toml
--rw-r--r--   0 macercha  (1000) macercha  (1000)       38 2023-04-11 22:56:50.692224 zibanu-django-1.2.0a5/setup.cfg
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.674224 zibanu-django-1.2.0a5/zibanu/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      623 2022-12-10 15:21:05.000000 zibanu-django-1.2.0a5/zibanu/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.675224 zibanu-django-1.2.0a5/zibanu/django/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      508 2022-12-11 23:08:20.000000 zibanu-django-1.2.0a5/zibanu/django/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      895 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/apps.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.675224 zibanu-django-1.2.0a5/zibanu/django/auth/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      311 2023-04-08 12:20:31.000000 zibanu-django-1.2.0a5/zibanu/django/auth/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.676224 zibanu-django-1.2.0a5/zibanu/django/auth/api/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      311 2023-04-08 12:25:30.000000 zibanu-django-1.2.0a5/zibanu/django/auth/api/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     3848 2023-04-11 22:46:44.000000 zibanu-django-1.2.0a5/zibanu/django/auth/api/serializers.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      915 2023-04-10 18:51:33.000000 zibanu-django-1.2.0a5/zibanu/django/auth/apps.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.676224 zibanu-django-1.2.0a5/zibanu/django/auth/lib/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      313 2023-04-10 19:32:01.000000 zibanu-django-1.2.0a5/zibanu/django/auth/lib/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.676224 zibanu-django-1.2.0a5/zibanu/django/auth/lib/choices/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      313 2023-04-10 19:48:01.000000 zibanu-django-1.2.0a5/zibanu/django/auth/lib/choices/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.677224 zibanu-django-1.2.0a5/zibanu/django/auth/migrations/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)    24474 2023-04-11 22:39:55.000000 zibanu-django-1.2.0a5/zibanu/django/auth/migrations/0001_initial.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      313 2023-04-10 19:31:28.000000 zibanu-django-1.2.0a5/zibanu/django/auth/migrations/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1605 2023-04-11 22:39:53.000000 zibanu-django-1.2.0a5/zibanu/django/auth/models.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      637 2023-04-08 12:38:36.000000 zibanu-django-1.2.0a5/zibanu/django/auth/urls.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.677224 zibanu-django-1.2.0a5/zibanu/django/db/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      508 2022-12-13 18:13:01.000000 zibanu-django-1.2.0a5/zibanu/django/db/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.677224 zibanu-django-1.2.0a5/zibanu/django/db/backends/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-07 01:34:17.000000 zibanu-django-1.2.0a5/zibanu/django/db/backends/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.678224 zibanu-django-1.2.0a5/zibanu/django/db/backends/oracle/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-07 01:34:17.000000 zibanu-django-1.2.0a5/zibanu/django/db/backends/oracle/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1158 2023-02-07 01:58:51.000000 zibanu-django-1.2.0a5/zibanu/django/db/backends/oracle/base.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.678224 zibanu-django-1.2.0a5/zibanu/django/db/models/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      766 2023-01-17 11:51:34.000000 zibanu-django-1.2.0a5/zibanu/django/db/models/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      931 2023-03-01 18:58:00.000000 zibanu-django-1.2.0a5/zibanu/django/db/models/dated_model.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1458 2023-03-03 23:10:34.000000 zibanu-django-1.2.0a5/zibanu/django/db/models/manager.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      738 2022-12-20 14:58:49.000000 zibanu-django-1.2.0a5/zibanu/django/db/models/model.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.671224 zibanu-django-1.2.0a5/zibanu/django/locale/
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.671224 zibanu-django-1.2.0a5/zibanu/django/locale/es/
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.679224 zibanu-django-1.2.0a5/zibanu/django/locale/es/LC_MESSAGES/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     2274 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/locale/es/LC_MESSAGES/django.mo
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     3609 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/locale/es/LC_MESSAGES/django.po
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.679224 zibanu-django-1.2.0a5/zibanu/django/logging/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-03-16 14:08:34.000000 zibanu-django-1.2.0a5/zibanu/django/logging/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      919 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/apps.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.680224 zibanu-django-1.2.0a5/zibanu/django/logging/lib/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-03-15 20:39:57.000000 zibanu-django-1.2.0a5/zibanu/django/logging/lib/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.680224 zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      702 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1018 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/on_change_password.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1243 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/on_login.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      975 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/on_send_mail.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.680224 zibanu-django-1.2.0a5/zibanu/django/logging/lib/managers/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-03-15 21:05:35.000000 zibanu-django-1.2.0a5/zibanu/django/logging/lib/managers/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      453 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/lib/signals.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.672224 zibanu-django-1.2.0a5/zibanu/django/logging/locale/
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.672224 zibanu-django-1.2.0a5/zibanu/django/logging/locale/es/
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.681224 zibanu-django-1.2.0a5/zibanu/django/logging/locale/es/LC_MESSAGES/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      702 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/locale/es/LC_MESSAGES/django.mo
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1185 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/locale/es/LC_MESSAGES/django.po
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.682224 zibanu-django-1.2.0a5/zibanu/django/logging/migrations/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1501 2023-03-15 21:32:53.000000 zibanu-django-1.2.0a5/zibanu/django/logging/migrations/0001_initial.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1143 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/migrations/0002_maillog.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-03-15 21:33:26.000000 zibanu-django-1.2.0a5/zibanu/django/logging/migrations/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1946 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/logging/models.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.682224 zibanu-django-1.2.0a5/zibanu/django/repository/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-03 02:16:47.000000 zibanu-django-1.2.0a5/zibanu/django/repository/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.682224 zibanu-django-1.2.0a5/zibanu/django/repository/api/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-04 20:42:37.000000 zibanu-django-1.2.0a5/zibanu/django/repository/api/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      958 2023-02-03 02:43:10.000000 zibanu-django-1.2.0a5/zibanu/django/repository/apps.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.683224 zibanu-django-1.2.0a5/zibanu/django/repository/lib/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-04 20:45:36.000000 zibanu-django-1.2.0a5/zibanu/django/repository/lib/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.683224 zibanu-django-1.2.0a5/zibanu/django/repository/lib/managers/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      566 2023-02-04 20:47:18.000000 zibanu-django-1.2.0a5/zibanu/django/repository/lib/managers/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      740 2023-02-04 21:36:16.000000 zibanu-django-1.2.0a5/zibanu/django/repository/lib/managers/document.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.683224 zibanu-django-1.2.0a5/zibanu/django/repository/lib/utils/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      593 2023-02-04 20:45:36.000000 zibanu-django-1.2.0a5/zibanu/django/repository/lib/utils/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     6973 2023-04-11 22:50:39.000000 zibanu-django-1.2.0a5/zibanu/django/repository/lib/utils/document_generator.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.672224 zibanu-django-1.2.0a5/zibanu/django/repository/locale/
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.672224 zibanu-django-1.2.0a5/zibanu/django/repository/locale/es/
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.684224 zibanu-django-1.2.0a5/zibanu/django/repository/locale/es/LC_MESSAGES/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1605 2023-02-09 14:40:51.000000 zibanu-django-1.2.0a5/zibanu/django/repository/locale/es/LC_MESSAGES/django.mo
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     2664 2023-04-11 22:52:31.000000 zibanu-django-1.2.0a5/zibanu/django/repository/locale/es/LC_MESSAGES/django.po
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.684224 zibanu-django-1.2.0a5/zibanu/django/repository/migrations/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1372 2023-02-03 02:43:34.000000 zibanu-django-1.2.0a5/zibanu/django/repository/migrations/0001_initial.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      427 2023-02-08 14:23:11.000000 zibanu-django-1.2.0a5/zibanu/django/repository/migrations/0002_document_description.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)        0 2023-02-03 02:23:41.000000 zibanu-django-1.2.0a5/zibanu/django/repository/migrations/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1575 2023-02-08 14:23:06.000000 zibanu-django-1.2.0a5/zibanu/django/repository/models.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.685224 zibanu-django-1.2.0a5/zibanu/django/rest_framework/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      508 2022-12-13 12:39:27.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/__init__.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.685224 zibanu-django-1.2.0a5/zibanu/django/rest_framework/exceptions/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      973 2022-12-20 02:49:47.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/exceptions/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1967 2022-12-14 09:17:28.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/exceptions/api_exception.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.685224 zibanu-django-1.2.0a5/zibanu/django/rest_framework/fields/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      651 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/fields/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1142 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/fields/current_user_default.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.686224 zibanu-django-1.2.0a5/zibanu/django/rest_framework/serializers/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1560 2022-12-20 10:51:58.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/serializers/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      651 2023-02-27 20:11:57.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/serializers/fields.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      867 2022-12-14 09:18:30.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/serializers/model_serializer.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.687224 zibanu-django-1.2.0a5/zibanu/django/rest_framework/viewsets/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      784 2023-02-13 14:05:54.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/viewsets/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)    10439 2023-03-31 16:50:03.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/viewsets/model_viewset.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1332 2023-02-13 14:05:54.000000 zibanu-django-1.2.0a5/zibanu/django/rest_framework/viewsets/viewset.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.687224 zibanu-django-1.2.0a5/zibanu/django/template/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-01-28 17:50:45.000000 zibanu-django-1.2.0a5/zibanu/django/template/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      663 2023-01-28 20:32:11.000000 zibanu-django-1.2.0a5/zibanu/django/template/apps.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.688224 zibanu-django-1.2.0a5/zibanu/django/template/context_processors/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      624 2023-01-29 02:00:01.000000 zibanu-django-1.2.0a5/zibanu/django/template/context_processors/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      784 2023-01-29 02:00:01.000000 zibanu-django-1.2.0a5/zibanu/django/template/context_processors/full_static_uri.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      742 2023-01-28 20:37:34.000000 zibanu-django-1.2.0a5/zibanu/django/template/context_processors/site.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.673225 zibanu-django-1.2.0a5/zibanu/django/template/locale/
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.673225 zibanu-django-1.2.0a5/zibanu/django/template/locale/es/
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.688224 zibanu-django-1.2.0a5/zibanu/django/template/locale/es/LC_MESSAGES/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      519 2023-02-09 14:42:38.000000 zibanu-django-1.2.0a5/zibanu/django/template/locale/es/LC_MESSAGES/django.mo
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1022 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/template/locale/es/LC_MESSAGES/django.po
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.689224 zibanu-django-1.2.0a5/zibanu/django/template/templatetags/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-02-07 23:57:31.000000 zibanu-django-1.2.0a5/zibanu/django/template/templatetags/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1539 2023-01-29 02:38:53.000000 zibanu-django-1.2.0a5/zibanu/django/template/templatetags/static_uri.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      666 2023-02-08 00:00:29.000000 zibanu-django-1.2.0a5/zibanu/django/template/templatetags/string_concat.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     2009 2023-02-16 14:53:50.000000 zibanu-django-1.2.0a5/zibanu/django/template/templatetags/subtotal_dict.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1216 2023-02-08 15:25:53.000000 zibanu-django-1.2.0a5/zibanu/django/template/templatetags/sum_dict.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.690224 zibanu-django-1.2.0a5/zibanu/django/utils/
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      863 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/utils/__init__.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     3059 2023-03-14 20:09:11.000000 zibanu-django-1.2.0a5/zibanu/django/utils/code_generator.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1895 2023-02-26 20:02:32.000000 zibanu-django-1.2.0a5/zibanu/django/utils/date_time.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1163 2023-03-03 13:27:43.000000 zibanu-django-1.2.0a5/zibanu/django/utils/error_messages.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     4325 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/utils/mail.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      562 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a5/zibanu/django/utils/request_utils.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)     1251 2022-12-14 09:24:38.000000 zibanu-django-1.2.0a5/zibanu/django/utils/user.py
--rw-rw-r--   0 macercha  (1000) macercha  (1000)      699 2023-03-03 13:27:43.000000 zibanu-django-1.2.0a5/zibanu/django/utils/validate_cache_code.py
-drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-04-11 22:56:50.691224 zibanu-django-1.2.0a5/zibanu_django.egg-info/
--rw-r--r--   0 macercha  (1000) macercha  (1000)    41365 2023-04-11 22:56:50.000000 zibanu-django-1.2.0a5/zibanu_django.egg-info/PKG-INFO
--rw-r--r--   0 macercha  (1000) macercha  (1000)     3816 2023-04-11 22:56:50.000000 zibanu-django-1.2.0a5/zibanu_django.egg-info/SOURCES.txt
--rw-r--r--   0 macercha  (1000) macercha  (1000)        1 2023-04-11 22:56:50.000000 zibanu-django-1.2.0a5/zibanu_django.egg-info/dependency_links.txt
--rw-r--r--   0 macercha  (1000) macercha  (1000)       32 2023-04-11 22:56:50.000000 zibanu-django-1.2.0a5/zibanu_django.egg-info/requires.txt
--rw-r--r--   0 macercha  (1000) macercha  (1000)        7 2023-04-11 22:56:50.000000 zibanu-django-1.2.0a5/zibanu_django.egg-info/top_level.txt
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.589411 zibanu-django-1.2.0a6/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)    35148 2022-05-01 19:35:15.000000 zibanu-django-1.2.0a6/LICENSE
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      207 2023-03-31 15:51:33.000000 zibanu-django-1.2.0a6/MANIFEST.in
+-rw-r--r--   0 macercha  (1000) macercha  (1000)    41365 2023-05-13 14:29:57.588411 zibanu-django-1.2.0a6/PKG-INFO
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      158 2023-01-18 12:15:22.000000 zibanu-django-1.2.0a6/README.md
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      849 2023-05-13 14:27:36.000000 zibanu-django-1.2.0a6/pyproject.toml
+-rw-r--r--   0 macercha  (1000) macercha  (1000)       38 2023-05-13 14:29:57.589411 zibanu-django-1.2.0a6/setup.cfg
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.557412 zibanu-django-1.2.0a6/zibanu/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      623 2022-12-10 15:21:05.000000 zibanu-django-1.2.0a6/zibanu/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.558412 zibanu-django-1.2.0a6/zibanu/django/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      508 2022-12-11 23:08:20.000000 zibanu-django-1.2.0a6/zibanu/django/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      895 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/apps.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.558412 zibanu-django-1.2.0a6/zibanu/django/auth/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      311 2023-04-08 12:20:31.000000 zibanu-django-1.2.0a6/zibanu/django/auth/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.559412 zibanu-django-1.2.0a6/zibanu/django/auth/api/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      311 2023-04-08 12:25:30.000000 zibanu-django-1.2.0a6/zibanu/django/auth/api/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.559412 zibanu-django-1.2.0a6/zibanu/django/auth/api/serializers/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      648 2023-04-27 14:40:31.000000 zibanu-django-1.2.0a6/zibanu/django/auth/api/serializers/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      749 2023-04-27 12:00:18.000000 zibanu-django-1.2.0a6/zibanu/django/auth/api/serializers/profile.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     3051 2023-04-27 12:17:39.000000 zibanu-django-1.2.0a6/zibanu/django/auth/api/serializers/token.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     3944 2023-05-13 14:19:35.000000 zibanu-django-1.2.0a6/zibanu/django/auth/api/serializers/user.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.560412 zibanu-django-1.2.0a6/zibanu/django/auth/api/services/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      376 2023-04-27 14:42:35.000000 zibanu-django-1.2.0a6/zibanu/django/auth/api/services/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     3165 2023-05-13 14:20:35.000000 zibanu-django-1.2.0a6/zibanu/django/auth/api/services/user.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      915 2023-04-10 18:51:33.000000 zibanu-django-1.2.0a6/zibanu/django/auth/apps.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.560412 zibanu-django-1.2.0a6/zibanu/django/auth/lib/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      313 2023-04-10 19:32:01.000000 zibanu-django-1.2.0a6/zibanu/django/auth/lib/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.560412 zibanu-django-1.2.0a6/zibanu/django/auth/lib/choices/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      313 2023-04-10 19:48:01.000000 zibanu-django-1.2.0a6/zibanu/django/auth/lib/choices/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.560412 zibanu-django-1.2.0a6/zibanu/django/auth/migrations/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)    24474 2023-04-11 22:39:55.000000 zibanu-django-1.2.0a6/zibanu/django/auth/migrations/0001_initial.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      313 2023-04-10 19:31:28.000000 zibanu-django-1.2.0a6/zibanu/django/auth/migrations/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1605 2023-04-11 22:39:53.000000 zibanu-django-1.2.0a6/zibanu/django/auth/models.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      856 2023-04-28 00:32:16.000000 zibanu-django-1.2.0a6/zibanu/django/auth/urls.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.561412 zibanu-django-1.2.0a6/zibanu/django/db/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      508 2022-12-13 18:13:01.000000 zibanu-django-1.2.0a6/zibanu/django/db/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.561412 zibanu-django-1.2.0a6/zibanu/django/db/backends/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-07 01:34:17.000000 zibanu-django-1.2.0a6/zibanu/django/db/backends/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.561412 zibanu-django-1.2.0a6/zibanu/django/db/backends/oracle/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-07 01:34:17.000000 zibanu-django-1.2.0a6/zibanu/django/db/backends/oracle/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1158 2023-02-07 01:58:51.000000 zibanu-django-1.2.0a6/zibanu/django/db/backends/oracle/base.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.562412 zibanu-django-1.2.0a6/zibanu/django/db/models/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      766 2023-01-17 11:51:34.000000 zibanu-django-1.2.0a6/zibanu/django/db/models/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      931 2023-03-01 18:58:00.000000 zibanu-django-1.2.0a6/zibanu/django/db/models/dated_model.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1458 2023-03-03 23:10:34.000000 zibanu-django-1.2.0a6/zibanu/django/db/models/manager.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      738 2022-12-20 14:58:49.000000 zibanu-django-1.2.0a6/zibanu/django/db/models/model.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.553412 zibanu-django-1.2.0a6/zibanu/django/locale/
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.553412 zibanu-django-1.2.0a6/zibanu/django/locale/es/
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.562412 zibanu-django-1.2.0a6/zibanu/django/locale/es/LC_MESSAGES/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     2274 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/locale/es/LC_MESSAGES/django.mo
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     3598 2023-04-27 15:33:39.000000 zibanu-django-1.2.0a6/zibanu/django/locale/es/LC_MESSAGES/django.po
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.562412 zibanu-django-1.2.0a6/zibanu/django/logging/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-03-16 14:08:34.000000 zibanu-django-1.2.0a6/zibanu/django/logging/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      919 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/apps.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.563412 zibanu-django-1.2.0a6/zibanu/django/logging/lib/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-03-15 20:39:57.000000 zibanu-django-1.2.0a6/zibanu/django/logging/lib/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.564412 zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      702 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1018 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/on_change_password.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1243 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/on_login.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      975 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/on_send_mail.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.564412 zibanu-django-1.2.0a6/zibanu/django/logging/lib/managers/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-03-15 21:05:35.000000 zibanu-django-1.2.0a6/zibanu/django/logging/lib/managers/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      453 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/lib/signals.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.554412 zibanu-django-1.2.0a6/zibanu/django/logging/locale/
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.554412 zibanu-django-1.2.0a6/zibanu/django/logging/locale/es/
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.564412 zibanu-django-1.2.0a6/zibanu/django/logging/locale/es/LC_MESSAGES/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      702 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/locale/es/LC_MESSAGES/django.mo
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1185 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/locale/es/LC_MESSAGES/django.po
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.565412 zibanu-django-1.2.0a6/zibanu/django/logging/migrations/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1501 2023-03-15 21:32:53.000000 zibanu-django-1.2.0a6/zibanu/django/logging/migrations/0001_initial.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1143 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/migrations/0002_maillog.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-03-15 21:33:26.000000 zibanu-django-1.2.0a6/zibanu/django/logging/migrations/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1946 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/logging/models.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.565412 zibanu-django-1.2.0a6/zibanu/django/repository/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-03 02:16:47.000000 zibanu-django-1.2.0a6/zibanu/django/repository/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.565412 zibanu-django-1.2.0a6/zibanu/django/repository/api/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-04 20:42:37.000000 zibanu-django-1.2.0a6/zibanu/django/repository/api/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      958 2023-02-03 02:43:10.000000 zibanu-django-1.2.0a6/zibanu/django/repository/apps.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.565412 zibanu-django-1.2.0a6/zibanu/django/repository/lib/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      505 2023-02-04 20:45:36.000000 zibanu-django-1.2.0a6/zibanu/django/repository/lib/__init__.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.566412 zibanu-django-1.2.0a6/zibanu/django/repository/lib/managers/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      566 2023-02-04 20:47:18.000000 zibanu-django-1.2.0a6/zibanu/django/repository/lib/managers/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      740 2023-02-04 21:36:16.000000 zibanu-django-1.2.0a6/zibanu/django/repository/lib/managers/document.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.566412 zibanu-django-1.2.0a6/zibanu/django/repository/lib/utils/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      593 2023-02-04 20:45:36.000000 zibanu-django-1.2.0a6/zibanu/django/repository/lib/utils/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     6973 2023-04-11 22:50:39.000000 zibanu-django-1.2.0a6/zibanu/django/repository/lib/utils/document_generator.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.555412 zibanu-django-1.2.0a6/zibanu/django/repository/locale/
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.555412 zibanu-django-1.2.0a6/zibanu/django/repository/locale/es/
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.566412 zibanu-django-1.2.0a6/zibanu/django/repository/locale/es/LC_MESSAGES/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1605 2023-02-09 14:40:51.000000 zibanu-django-1.2.0a6/zibanu/django/repository/locale/es/LC_MESSAGES/django.mo
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     2664 2023-04-11 22:52:31.000000 zibanu-django-1.2.0a6/zibanu/django/repository/locale/es/LC_MESSAGES/django.po
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.567412 zibanu-django-1.2.0a6/zibanu/django/repository/migrations/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1372 2023-02-03 02:43:34.000000 zibanu-django-1.2.0a6/zibanu/django/repository/migrations/0001_initial.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      427 2023-02-08 14:23:11.000000 zibanu-django-1.2.0a6/zibanu/django/repository/migrations/0002_document_description.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)        0 2023-02-03 02:23:41.000000 zibanu-django-1.2.0a6/zibanu/django/repository/migrations/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1575 2023-02-08 14:23:06.000000 zibanu-django-1.2.0a6/zibanu/django/repository/models.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.567412 zibanu-django-1.2.0a6/zibanu/django/rest_framework/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      508 2022-12-13 12:39:27.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1650 2023-04-28 00:41:44.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/decorators.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.567412 zibanu-django-1.2.0a6/zibanu/django/rest_framework/exceptions/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      973 2022-12-20 02:49:47.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/exceptions/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     2039 2023-04-27 15:30:28.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/exceptions/api_exception.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.568412 zibanu-django-1.2.0a6/zibanu/django/rest_framework/fields/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      651 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/fields/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1142 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/fields/current_user_default.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.568412 zibanu-django-1.2.0a6/zibanu/django/rest_framework/serializers/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1560 2022-12-20 10:51:58.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/serializers/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      651 2023-02-27 20:11:57.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/serializers/fields.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      867 2022-12-14 09:18:30.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/serializers/model_serializer.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.569412 zibanu-django-1.2.0a6/zibanu/django/rest_framework/viewsets/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      784 2023-02-13 14:05:54.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/viewsets/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)    10487 2023-04-28 00:47:56.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/viewsets/model_viewset.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1332 2023-02-13 14:05:54.000000 zibanu-django-1.2.0a6/zibanu/django/rest_framework/viewsets/viewset.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.569412 zibanu-django-1.2.0a6/zibanu/django/template/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-01-28 17:50:45.000000 zibanu-django-1.2.0a6/zibanu/django/template/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      663 2023-01-28 20:32:11.000000 zibanu-django-1.2.0a6/zibanu/django/template/apps.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.570412 zibanu-django-1.2.0a6/zibanu/django/template/context_processors/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      624 2023-01-29 02:00:01.000000 zibanu-django-1.2.0a6/zibanu/django/template/context_processors/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      784 2023-01-29 02:00:01.000000 zibanu-django-1.2.0a6/zibanu/django/template/context_processors/full_static_uri.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      742 2023-01-28 20:37:34.000000 zibanu-django-1.2.0a6/zibanu/django/template/context_processors/site.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.556412 zibanu-django-1.2.0a6/zibanu/django/template/locale/
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.556412 zibanu-django-1.2.0a6/zibanu/django/template/locale/es/
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.570412 zibanu-django-1.2.0a6/zibanu/django/template/locale/es/LC_MESSAGES/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      519 2023-02-09 14:42:38.000000 zibanu-django-1.2.0a6/zibanu/django/template/locale/es/LC_MESSAGES/django.mo
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1022 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/template/locale/es/LC_MESSAGES/django.po
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.571412 zibanu-django-1.2.0a6/zibanu/django/template/templatetags/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      506 2023-02-07 23:57:31.000000 zibanu-django-1.2.0a6/zibanu/django/template/templatetags/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1539 2023-01-29 02:38:53.000000 zibanu-django-1.2.0a6/zibanu/django/template/templatetags/static_uri.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      666 2023-02-08 00:00:29.000000 zibanu-django-1.2.0a6/zibanu/django/template/templatetags/string_concat.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     2009 2023-02-16 14:53:50.000000 zibanu-django-1.2.0a6/zibanu/django/template/templatetags/subtotal_dict.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1216 2023-02-08 15:25:53.000000 zibanu-django-1.2.0a6/zibanu/django/template/templatetags/sum_dict.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.572412 zibanu-django-1.2.0a6/zibanu/django/utils/
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      863 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/utils/__init__.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     3332 2023-04-28 21:35:15.000000 zibanu-django-1.2.0a6/zibanu/django/utils/code_generator.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1895 2023-02-26 20:02:32.000000 zibanu-django-1.2.0a6/zibanu/django/utils/date_time.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1163 2023-03-03 13:27:43.000000 zibanu-django-1.2.0a6/zibanu/django/utils/error_messages.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     4325 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/utils/mail.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      562 2023-03-31 15:46:10.000000 zibanu-django-1.2.0a6/zibanu/django/utils/request_utils.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)     1251 2022-12-14 09:24:38.000000 zibanu-django-1.2.0a6/zibanu/django/utils/user.py
+-rw-rw-r--   0 macercha  (1000) macercha  (1000)      699 2023-03-03 13:27:43.000000 zibanu-django-1.2.0a6/zibanu/django/utils/validate_cache_code.py
+drwxr-xr-x   0 macercha  (1000) macercha  (1000)        0 2023-05-13 14:29:57.588411 zibanu-django-1.2.0a6/zibanu_django.egg-info/
+-rw-r--r--   0 macercha  (1000) macercha  (1000)    41365 2023-05-13 14:29:57.000000 zibanu-django-1.2.0a6/zibanu_django.egg-info/PKG-INFO
+-rw-r--r--   0 macercha  (1000) macercha  (1000)     4085 2023-05-13 14:29:57.000000 zibanu-django-1.2.0a6/zibanu_django.egg-info/SOURCES.txt
+-rw-r--r--   0 macercha  (1000) macercha  (1000)        1 2023-05-13 14:29:57.000000 zibanu-django-1.2.0a6/zibanu_django.egg-info/dependency_links.txt
+-rw-r--r--   0 macercha  (1000) macercha  (1000)       32 2023-05-13 14:29:57.000000 zibanu-django-1.2.0a6/zibanu_django.egg-info/requires.txt
+-rw-r--r--   0 macercha  (1000) macercha  (1000)        7 2023-05-13 14:29:57.000000 zibanu-django-1.2.0a6/zibanu_django.egg-info/top_level.txt
```

### Comparing `zibanu-django-1.2.0a5/LICENSE` & `zibanu-django-1.2.0a6/LICENSE`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/PKG-INFO` & `zibanu-django-1.2.0a6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zibanu-django
-Version: 1.2.0a5
+Version: 1.2.0a6
 Summary: Zibanu library for django projects
 Author-email: Mario Cerón <mario.ceron@cqinversiones.co>
 License:                     GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
```

### Comparing `zibanu-django-1.2.0a5/pyproject.toml` & `zibanu-django-1.2.0a6/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
     "setuptools>=42",
     "wheel",
 ]
 build-backend="setuptools.build_meta"
 
 [project]
 name = "zibanu-django"
-version = "1.2.0-alpha.5"
+version = "1.2.0-alpha.6"
 authors = [
     {name="Mario Cerón", email="mario.ceron@cqinversiones.co"}
 ]
 description = "Zibanu library for django projects"
 readme = "README.md"
 license = {file="LICENSE"}
 requires-python = ">=3.9"
```

### Comparing `zibanu-django-1.2.0a5/zibanu/__init__.py` & `zibanu-django-1.2.0a6/zibanu/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/apps.py` & `zibanu-django-1.2.0a6/zibanu/django/apps.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/auth/api/serializers.py` & `zibanu-django-1.2.0a6/zibanu/django/auth/api/serializers/user.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,106 +1,107 @@
 # -*- coding: utf-8 -*-
 
 # ****************************************************************
 # IDE:          PyCharm
 # Developed by: macercha
-# Date:         8/04/23 9:58
-# Project:      Django Plugins
-# Module Name:  serializers
+# Date:         27/04/23 6:57
+# Project:      Zibanu - Django
+# Module Name:  user
 # Description:
 # ****************************************************************
+from .profile import ProfileSerializer
 from django.conf import settings
-from django.contrib.auth import authenticate
 from django.contrib.auth import get_user_model
-from django.contrib.auth.models import update_last_login
-from rest_framework.exceptions import AuthenticationFailed
+from django.utils.translation import gettext_lazy as _
 from rest_framework import serializers
-from rest_framework_simplejwt.serializers import TokenObtainSerializer, TokenRefreshSerializer
-from rest_framework_simplejwt.settings import api_settings
-from rest_framework_simplejwt.tokens import SlidingToken
-from typing import Dict, Any
+from rest_framework.exceptions import ValidationError
 from zibanu.django.auth.models import UserProfile
 
-class ProfileSerializer(serializers.ModelSerializer):
-
-    class Meta:
-        model = UserProfile
-        fields = ("timezone", "theme", "lang", "avatar", "messages_timeout", "keep_logged_in", "app_profile")
 
 class UserSerializer(serializers.ModelSerializer):
+    """
+    Serializer class for Django user entity, including user profile, permissions and roles (groups).
+    """
     full_name = serializers.SerializerMethodField(default="Guest")
     profile = ProfileSerializer(required=True, read_only=False)
     roles = serializers.SerializerMethodField(default=[])
-    user_permissions = serializers.SerializerMethodField(default=[])
-
-    class Meta:
-        model = get_user_model()
-        fields = ("id", "email", "full_name", "is_staff", "is_superuser", "last_login", "profile", "roles", "user_permissions")
+    permissions = serializers.SerializerMethodField(default=[])
 
-    def get_user_permissions(self, instance) -> list:
-        user_permissions = []
+    def get_permissions(self, instance) -> list:
+        """
+        Obtain permissions list from User object
+        :param instance: user instance
+        :return: list with user permissions
+        """
+        permissions = []
         if self.context.get("load_permissions", settings.ZB_AUTH_INCLUDE_PERMISSIONS):
-            for user_permission in instance.user_permissions.all():
-                user_permissions.append(user_permission.code)
-        return user_permissions
+            permissions = list(instance.get_all_permissions())
+        return permissions
 
     def get_roles(self, instance) -> list:
+        """
+        Obtain django group list from User object
+        :param instance: user instance
+        :return: list of roles
+        """
         roles = []
         if self.context.get("load_roles", settings.ZB_AUTH_INCLUDE_GROUPS):
             for group in instance.user_permissions.all():
                 roles.append(group.name)
         return roles
 
     def get_full_name(self, instance) -> str:
+        """
+        Return a full name from get_full_name method on User object
+        :param instance: user instance
+        :return: user full name
+        """
         return instance.get_full_name()
 
+    def create(self, validated_data):
+        """
+        Create user with its profile
+        :param validated_data: data validated from serializer
+        :return: user object
+        """
+        email = validated_data.pop("email")
+        user_object = self.Meta.model.objects.filter(email__exact=email).first()
+
+        if user_object is None:
+            if "password" not in validated_data.keys():
+                raise ValidationError(_("The password is required."), "create_user")
+
+            password = validated_data.pop("password")
+            username = validated_data.pop("username")
+            profile_data = validated_data.pop("profile")
+            user_object = self.Meta.model.objects.create_user(username=username, email=email, password=password, **validated_data)
+            # Create profile
+            user_profile = UserProfile(user=user_object, **profile_data)
+            user_profile.save()
+        else:
+            raise ValidationError(_("Email is already registered in our database."))
+        return user_object
 
+    class Meta:
+        """
+        Metaclass for UserSerializer
+        """
+        model = get_user_model()
+        fields = ("email", "full_name", "last_login", "is_staff", "is_superuser", "is_active", "profile", "roles",
+                  "first_name", "last_name", "permissions", "username", "password")
 
 
+class UserListSerializer(serializers.ModelSerializer):
+    """
+    User list serializer class for list basic data
+    """
+    full_name = serializers.SerializerMethodField(default="Guest")
 
-class EmailTokenObtainSerializer(TokenObtainSerializer):
-    username_field = get_user_model().EMAIL_FIELD
+    class Meta:
+        """
+        Metaclass for UserListSerializer
+        """
+        fields = ("full_name", "email", "last_login", "username", "is_staff", "is_superuser")
+        model = get_user_model()
 
-    def __init__(self, *args, **kwargs):
-        super().__init__(*args, **kwargs)
-        self.user = None
-
-    @classmethod
-    def get_token(cls, user):
-        token = super().get_token(user)
-
-        # Include user data
-        user_serializer = UserSerializer(instance=user)
-        token["user"] = user_serializer.data
-
-        return token
-
-    def validate(self, attrs: Dict[str, Any]) -> Dict[Any, Any]:
-        user = get_user_model().objects.filter(email__iexact=attrs.get(self.username_field)).first()
-
-        if user is None:
-            raise AuthenticationFailed(self.error_messages["no_active_account"], "no_active_account")
-
-        authenticate_kwargs = {
-            get_user_model().USERNAME_FIELD: user.get_username(),
-            "password": attrs.get("password")
-        }
-        self.user = authenticate(**authenticate_kwargs)
-        if not api_settings.USER_AUTHENTICATION_RULE(self.user):
-            raise AuthenticationFailed(
-                self.error_messages["no_active_account"],
-                "no_active_account",
-            )
-        return {}
-
-
-class TokenObtainSlidingSerializer(EmailTokenObtainSerializer):
-    token_class = SlidingToken
-
-    def validate(self, attrs: Dict[str, Any]) -> Dict[Any, Any]:
-        data = super().validate(attrs)
-        token = self.get_token(self.user)
-        data["token"] = str(token)
-
-        if api_settings.UPDATE_LAST_LOGIN:
-            update_last_login(None, self.user)
-        return data
+    def get_full_name(self, instance):
+        return instance.get_full_name()
```

### Comparing `zibanu-django-1.2.0a5/zibanu/django/auth/apps.py` & `zibanu-django-1.2.0a6/zibanu/django/auth/apps.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/auth/migrations/0001_initial.py` & `zibanu-django-1.2.0a6/zibanu/django/auth/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/auth/models.py` & `zibanu-django-1.2.0a6/zibanu/django/auth/models.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/db/backends/oracle/base.py` & `zibanu-django-1.2.0a6/zibanu/django/db/backends/oracle/base.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/db/models/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/db/models/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/db/models/dated_model.py` & `zibanu-django-1.2.0a6/zibanu/django/db/models/dated_model.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/db/models/manager.py` & `zibanu-django-1.2.0a6/zibanu/django/db/models/manager.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/db/models/model.py` & `zibanu-django-1.2.0a6/zibanu/django/db/models/model.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/locale/es/LC_MESSAGES/django.mo` & `zibanu-django-1.2.0a6/zibanu/django/locale/es/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/locale/es/LC_MESSAGES/django.po` & `zibanu-django-1.2.0a6/zibanu/django/locale/es/LC_MESSAGES/django.po`

 * *Files 24% similar despite different names*

```diff
@@ -4,114 +4,118 @@
 # FIRST AUTHOR <EMAIL@ADDRESS>, YEAR.
 #
 #, fuzzy
 msgid ""
 msgstr ""
 "Project-Id-Version: PACKAGE VERSION\n"
 "Report-Msgid-Bugs-To: \n"
-"POT-Creation-Date: 2023-03-17 14:57-0500\n"
+"POT-Creation-Date: 2023-04-27 10:33-0500\n"
 "PO-Revision-Date: YEAR-MO-DA HO:MI+ZONE\n"
 "Last-Translator: FULL NAME <EMAIL@ADDRESS>\n"
 "Language-Team: LANGUAGE <LL@li.org>\n"
 "Language: \n"
 "MIME-Version: 1.0\n"
 "Content-Type: text/plain; charset=UTF-8\n"
 "Content-Transfer-Encoding: 8bit\n"
 "Plural-Forms: nplurals=2; plural=(n != 1);\n"
 
-#: django/db/models/dated_model.py:20
+#: db/models/dated_model.py:20
 msgid "Created at"
 msgstr "Creado el"
 
-#: django/db/models/dated_model.py:21
+#: db/models/dated_model.py:21
 msgid "Modified at"
 msgstr "Modificado el"
 
-#: django/db/models/manager.py:42
-#| msgid "Object does not exists."
+#: db/models/manager.py:42
 msgid "OASIS Error. The object does not exists."
 msgstr "El objeto no existe."
 
-#: django/rest_framework/exceptions/api_exception.py:24
+#: rest_framework/decorators.py:42
+#: rest_framework/exceptions/api_exception.py:27
+msgid "You do not have permission to perform this action."
+msgstr "No posee permisos para ejecutar esta acción."
+
+#: rest_framework/exceptions/api_exception.py:24
 msgid "Object has not been created."
 msgstr "El objeto no ha sido creado."
 
-#: django/rest_framework/exceptions/api_exception.py:25
-#: django/rest_framework/exceptions/api_exception.py:43
-#: django/rest_framework/exceptions/api_exception.py:44
+#: rest_framework/exceptions/api_exception.py:25
+#: rest_framework/exceptions/api_exception.py:44
+#: rest_framework/exceptions/api_exception.py:45
 msgid "Generic error."
 msgstr "Error genérico."
 
-#: django/rest_framework/exceptions/api_exception.py:26
+#: rest_framework/exceptions/api_exception.py:26
 msgid "You are not authorized for this resource."
 msgstr "No está autorizado para utilizar este recurso."
 
-#: django/rest_framework/exceptions/api_exception.py:27
+#: rest_framework/exceptions/api_exception.py:28
 msgid "Object does not exists."
 msgstr "El objeto no existe."
 
-#: django/rest_framework/exceptions/api_exception.py:28
+#: rest_framework/exceptions/api_exception.py:29
 msgid "Data validation error."
 msgstr "Error en validación de datos."
 
-#: django/rest_framework/exceptions/api_exception.py:29
+#: rest_framework/exceptions/api_exception.py:30
 msgid "Data required not found."
 msgstr "El dato requerido no existe."
 
-#: django/rest_framework/exceptions/api_exception.py:30
+#: rest_framework/exceptions/api_exception.py:31
 msgid "Not controlled exception error."
 msgstr "Error de excepción no controlada."
 
-#: django/utils/code_generator.py:99
+#: utils/code_generator.py:99
 msgid "The generated values are invalid."
 msgstr "El valor generado es inválido."
 
-#: django/utils/error_messages.py:21
+#: utils/error_messages.py:21
 msgid "Error! The field is required."
 msgstr "Error! El campo es requerido."
 
-#: django/utils/error_messages.py:22
+#: utils/error_messages.py:22
 msgid "Error! Record has not been created."
 msgstr "Error! El registro no ha sido creado."
 
-#: django/utils/error_messages.py:23
+#: utils/error_messages.py:23
 msgid "Error! Record has not been updated."
 msgstr "Error! El registro no ha sido actualizado."
 
-#: django/utils/error_messages.py:24
+#: utils/error_messages.py:24
 msgid "Error! There is not record matching."
 msgstr "Error! No existen registros que coincidan."
 
-#: django/utils/error_messages.py:25
+#: utils/error_messages.py:25
 msgid "Error! Record can not be deleted."
 msgstr "Error! El registro no ha sido eliminado."
 
-#: django/utils/error_messages.py:26
+#: utils/error_messages.py:26
 msgid "Error! The data required not found."
 msgstr "Error! Los datos requeridos no se encuentran."
 
-#: django/utils/error_messages.py:27
+#: utils/error_messages.py:27
 msgid "Error at database."
 msgstr "Error genérico en la base de datos."
 
-#: django/utils/error_messages.py:28
+#: utils/error_messages.py:28
 msgid "Data required at request not found."
 msgstr "El dato requerido no existe."
 
-#: django/utils/error_messages.py:29
+#: utils/error_messages.py:29
 msgid "Error! Exception not controlled."
 msgstr "Excepción no controlada"
 
-#: django/utils/mail.py:73
+#: utils/mail.py:73
 msgid "Syntax error loading template '{}'"
 msgstr "Error de sintaxis cargando la plantilla '{}'"
 
-#: django/utils/mail.py:75
+#: utils/mail.py:75
 msgid "Template '{}' does not exist."
 msgstr "La plantilla '{}' no existe."
 
-#: django/utils/mail.py:100
+#: utils/mail.py:100
 msgid "Error sending email."
 msgstr "Error enviando el correo."
 
 #~ msgid "Data request not found."
 #~ msgstr "El dato requerido no existe."
```

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/apps.py` & `zibanu-django-1.2.0a6/zibanu/django/logging/apps.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/on_change_password.py` & `zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/on_change_password.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/on_login.py` & `zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/on_login.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/lib/events/on_send_mail.py` & `zibanu-django-1.2.0a6/zibanu/django/logging/lib/events/on_send_mail.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/locale/es/LC_MESSAGES/django.mo` & `zibanu-django-1.2.0a6/zibanu/django/logging/locale/es/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/locale/es/LC_MESSAGES/django.po` & `zibanu-django-1.2.0a6/zibanu/django/logging/locale/es/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/migrations/0001_initial.py` & `zibanu-django-1.2.0a6/zibanu/django/logging/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/migrations/0002_maillog.py` & `zibanu-django-1.2.0a6/zibanu/django/logging/migrations/0002_maillog.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/logging/models.py` & `zibanu-django-1.2.0a6/zibanu/django/logging/models.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/apps.py` & `zibanu-django-1.2.0a6/zibanu/django/repository/apps.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/lib/managers/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/repository/lib/managers/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/lib/managers/document.py` & `zibanu-django-1.2.0a6/zibanu/django/repository/lib/managers/document.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/lib/utils/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/repository/lib/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/lib/utils/document_generator.py` & `zibanu-django-1.2.0a6/zibanu/django/repository/lib/utils/document_generator.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/locale/es/LC_MESSAGES/django.mo` & `zibanu-django-1.2.0a6/zibanu/django/repository/locale/es/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/locale/es/LC_MESSAGES/django.po` & `zibanu-django-1.2.0a6/zibanu/django/repository/locale/es/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/migrations/0001_initial.py` & `zibanu-django-1.2.0a6/zibanu/django/repository/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/repository/models.py` & `zibanu-django-1.2.0a6/zibanu/django/repository/models.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/exceptions/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/exceptions/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/exceptions/api_exception.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/exceptions/api_exception.py`

 * *Files 6% similar despite different names*

```diff
@@ -20,14 +20,15 @@
     """
     Override class from APIException
     """
     __default_messages = {
         "304": _("Object has not been created."),
         "400": _("Generic error."),
         "401": _("You are not authorized for this resource."),
+        "403": _("You do not have permission to perform this action."),
         "404": _("Object does not exists."),
         "406": _("Data validation error."),
         "412": _("Data required not found."),
         "500": _("Not controlled exception error."),
     }
 
     def __init__(self, msg: str = None, error: str = None, http_status: int = status.HTTP_400_BAD_REQUEST) -> None:
```

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/fields/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/fields/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/fields/current_user_default.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/fields/current_user_default.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/serializers/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/serializers/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/serializers/fields.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/serializers/fields.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/serializers/model_serializer.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/serializers/model_serializer.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/viewsets/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/viewsets/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/viewsets/model_viewset.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/viewsets/model_viewset.py`

 * *Files 1% similar despite different names*

```diff
@@ -150,26 +150,26 @@
         try:
             data_return = []
             status_return = status.HTTP_400_BAD_REQUEST
             request_data = request.data
             if len(request_data) > 0:
                 serializer = self.get_serializer(data=request_data)
                 if serializer.is_valid(raise_exception=True):
-                    created = serializer.create(validated_data=serializer.validated_data)
-                    if created is not None:
-                        data_return = self.get_serializer(created).data
+                    created_record = serializer.create(validated_data=serializer.validated_data)
+                    if created_record is not None:
+                        data_return = self.get_serializer(created_record).data
                         status_return = status.HTTP_201_CREATED
                     else:
-                        raise ValidationError(ErrorMessages.CREATE_ERROR, "create")
+                        raise ValidationError(ErrorMessages.CREATE_ERROR, "create_object")
             else:
-                raise APIException(ErrorMessages.DATA_REQUIRED)
+                raise APIException(ErrorMessages.DATA_REQUIRED, "data_required")
         except DatabaseError as exc:
             raise APIException(ErrorMessages.DATABASE_ERROR, str(exc)) from exc
         except ValidationError as exc:
-            raise APIException(error=str(exc.detail), http_status=status.HTTP_406_NOT_ACCEPTABLE) from exc
+            raise APIException(error=str(exc.detail[0]), http_status=status.HTTP_406_NOT_ACCEPTABLE) from exc
         except APIException as exc:
             raise APIException(exc.detail.get("message"), exc.detail.get("detail"), exc.status_code) from exc
         except Exception as exc:
             raise APIException(error=str(exc), http_status=status.HTTP_500_INTERNAL_SERVER_ERROR)
         else:
             return Response(status=status_return, data=data_return)
```

### Comparing `zibanu-django-1.2.0a5/zibanu/django/rest_framework/viewsets/viewset.py` & `zibanu-django-1.2.0a6/zibanu/django/rest_framework/viewsets/viewset.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/apps.py` & `zibanu-django-1.2.0a6/zibanu/django/template/apps.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/context_processors/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/template/context_processors/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/context_processors/full_static_uri.py` & `zibanu-django-1.2.0a6/zibanu/django/template/context_processors/full_static_uri.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/context_processors/site.py` & `zibanu-django-1.2.0a6/zibanu/django/template/context_processors/site.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/locale/es/LC_MESSAGES/django.mo` & `zibanu-django-1.2.0a6/zibanu/django/template/locale/es/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/locale/es/LC_MESSAGES/django.po` & `zibanu-django-1.2.0a6/zibanu/django/template/locale/es/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/templatetags/static_uri.py` & `zibanu-django-1.2.0a6/zibanu/django/template/templatetags/static_uri.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/templatetags/string_concat.py` & `zibanu-django-1.2.0a6/zibanu/django/template/templatetags/string_concat.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/templatetags/subtotal_dict.py` & `zibanu-django-1.2.0a6/zibanu/django/template/templatetags/subtotal_dict.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/template/templatetags/sum_dict.py` & `zibanu-django-1.2.0a6/zibanu/django/template/templatetags/sum_dict.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/utils/__init__.py` & `zibanu-django-1.2.0a6/zibanu/django/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/utils/code_generator.py` & `zibanu-django-1.2.0a6/zibanu/django/utils/code_generator.py`

 * *Files 21% similar despite different names*

```diff
@@ -15,15 +15,24 @@
 import string
 import secrets
 from django.utils.translation import gettext_lazy as _
 from uuid import SafeUUID, UUID
 
 
 class CodeGenerator:
+    """
+    Class to generate random different types of codes
+    """
     def __init__(self, action: str, is_safe: SafeUUID = SafeUUID.safe, code_length: int = 6):
+        """
+        Constructor Method
+        :param action: action code to reference it
+        :param is_safe: flag to enable SafeUUID
+        :param code_length: length of generated code
+        """
         self._action = action
         self._is_safe = is_safe
         self._code_length = code_length
         self._code = None
         self._token = None
         self._uuid = None
```

### Comparing `zibanu-django-1.2.0a5/zibanu/django/utils/date_time.py` & `zibanu-django-1.2.0a6/zibanu/django/utils/date_time.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/utils/error_messages.py` & `zibanu-django-1.2.0a6/zibanu/django/utils/error_messages.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/utils/mail.py` & `zibanu-django-1.2.0a6/zibanu/django/utils/mail.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/utils/request_utils.py` & `zibanu-django-1.2.0a6/zibanu/django/utils/request_utils.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/utils/user.py` & `zibanu-django-1.2.0a6/zibanu/django/utils/user.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu/django/utils/validate_cache_code.py` & `zibanu-django-1.2.0a6/zibanu/django/utils/validate_cache_code.py`

 * *Files identical despite different names*

### Comparing `zibanu-django-1.2.0a5/zibanu_django.egg-info/PKG-INFO` & `zibanu-django-1.2.0a6/zibanu_django.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zibanu-django
-Version: 1.2.0a5
+Version: 1.2.0a6
 Summary: Zibanu library for django projects
 Author-email: Mario Cerón <mario.ceron@cqinversiones.co>
 License:                     GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
```

### Comparing `zibanu-django-1.2.0a5/zibanu_django.egg-info/SOURCES.txt` & `zibanu-django-1.2.0a6/zibanu_django.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -6,15 +6,20 @@
 zibanu/django/__init__.py
 zibanu/django/apps.py
 zibanu/django/auth/__init__.py
 zibanu/django/auth/apps.py
 zibanu/django/auth/models.py
 zibanu/django/auth/urls.py
 zibanu/django/auth/api/__init__.py
-zibanu/django/auth/api/serializers.py
+zibanu/django/auth/api/serializers/__init__.py
+zibanu/django/auth/api/serializers/profile.py
+zibanu/django/auth/api/serializers/token.py
+zibanu/django/auth/api/serializers/user.py
+zibanu/django/auth/api/services/__init__.py
+zibanu/django/auth/api/services/user.py
 zibanu/django/auth/lib/__init__.py
 zibanu/django/auth/lib/choices/__init__.py
 zibanu/django/auth/migrations/0001_initial.py
 zibanu/django/auth/migrations/__init__.py
 zibanu/django/db/__init__.py
 zibanu/django/db/backends/__init__.py
 zibanu/django/db/backends/oracle/__init__.py
@@ -51,14 +56,15 @@
 zibanu/django/repository/lib/utils/document_generator.py
 zibanu/django/repository/locale/es/LC_MESSAGES/django.mo
 zibanu/django/repository/locale/es/LC_MESSAGES/django.po
 zibanu/django/repository/migrations/0001_initial.py
 zibanu/django/repository/migrations/0002_document_description.py
 zibanu/django/repository/migrations/__init__.py
 zibanu/django/rest_framework/__init__.py
+zibanu/django/rest_framework/decorators.py
 zibanu/django/rest_framework/exceptions/__init__.py
 zibanu/django/rest_framework/exceptions/api_exception.py
 zibanu/django/rest_framework/fields/__init__.py
 zibanu/django/rest_framework/fields/current_user_default.py
 zibanu/django/rest_framework/serializers/__init__.py
 zibanu/django/rest_framework/serializers/fields.py
 zibanu/django/rest_framework/serializers/model_serializer.py
```

