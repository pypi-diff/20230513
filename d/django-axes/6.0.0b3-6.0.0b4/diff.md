# Comparing `tmp/django-axes-6.0.0b3.tar.gz` & `tmp/django-axes-6.0.0b4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-axes-6.0.0b3.tar", last modified: Mon May  1 18:32:38 2023, max compression
+gzip compressed data, was "django-axes-6.0.0b4.tar", last modified: Sat May 13 11:11:13 2023, max compression
```

## Comparing `django-axes-6.0.0b3.tar` & `django-axes-6.0.0b4.tar`

### file list

```diff
@@ -1,132 +1,132 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.910358 django-axes-6.0.0b3/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.878357 django-axes-6.0.0b3/.github/
--rw-r--r--   0 runner    (1001) docker     (123)      285 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/.github/dependabot.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.882357 django-axes-6.0.0b3/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1425 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/.github/workflows/codeql.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1025 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/.github/workflows/release.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2360 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/.github/workflows/test.yml
--rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/.prospector.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    31599 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/CHANGES.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2375 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/CODE_OF_CONDUCT.md
--rw-r--r--   0 runner    (1001) docker     (123)     2328 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/CONTRIBUTING.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1184 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    35865 2023-05-01 18:32:38.910358 django-axes-6.0.0b3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2495 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.886357 django-axes-6.0.0b3/axes/
--rw-r--r--   0 runner    (1001) docker     (123)      273 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2974 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/admin.py
--rw-r--r--   0 runner    (1001) docker     (123)     1519 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/apps.py
--rw-r--r--   0 runner    (1001) docker     (123)     3194 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/attempts.py
--rw-r--r--   0 runner    (1001) docker     (123)     3855 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/backends.py
--rw-r--r--   0 runner    (1001) docker     (123)     4856 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/checks.py
--rw-r--r--   0 runner    (1001) docker     (123)     6584 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      628 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/decorators.py
--rw-r--r--   0 runner    (1001) docker     (123)      380 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/exceptions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.886357 django-axes-6.0.0b3/axes/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7852 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/handlers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     6511 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/handlers/cache.py
--rw-r--r--   0 runner    (1001) docker     (123)    12894 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/handlers/database.py
--rw-r--r--   0 runner    (1001) docker     (123)      725 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/handlers/dummy.py
--rw-r--r--   0 runner    (1001) docker     (123)     5150 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/handlers/proxy.py
--rw-r--r--   0 runner    (1001) docker     (123)      687 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/handlers/test.py
--rw-r--r--   0 runner    (1001) docker     (123)    20418 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/helpers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.870357 django-axes-6.0.0b3/axes/locale/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.870357 django-axes-6.0.0b3/axes/locale/ar/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.890357 django-axes-6.0.0b3/axes/locale/ar/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (123)     2018 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/ar/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (123)     2566 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/ar/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.870357 django-axes-6.0.0b3/axes/locale/de/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.890357 django-axes-6.0.0b3/axes/locale/de/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (123)     1711 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/de/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (123)     2496 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/de/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.870357 django-axes-6.0.0b3/axes/locale/pl/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.890357 django-axes-6.0.0b3/axes/locale/pl/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (123)     1526 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/pl/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (123)     2266 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/pl/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.870357 django-axes-6.0.0b3/axes/locale/ru/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.890357 django-axes-6.0.0b3/axes/locale/ru/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (123)     1910 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/ru/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (123)     2495 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/ru/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.870357 django-axes-6.0.0b3/axes/locale/tr/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.890357 django-axes-6.0.0b3/axes/locale/tr/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (123)     1412 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/tr/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (123)     2075 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/locale/tr/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.890357 django-axes-6.0.0b3/axes/management/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/management/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.894358 django-axes-6.0.0b3/axes/management/commands/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/management/commands/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      369 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/management/commands/axes_list_attempts.py
--rw-r--r--   0 runner    (1001) docker     (123)      374 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/management/commands/axes_reset.py
--rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/management/commands/axes_reset_failure_logs.py
--rw-r--r--   0 runner    (1001) docker     (123)      552 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/management/commands/axes_reset_ip.py
--rw-r--r--   0 runner    (1001) docker     (123)      643 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/management/commands/axes_reset_logs.py
--rw-r--r--   0 runner    (1001) docker     (123)      579 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/management/commands/axes_reset_username.py
--rw-r--r--   0 runner    (1001) docker     (123)     1670 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/middleware.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.898357 django-axes-6.0.0b3/axes/migrations/
--rw-r--r--   0 runner    (1001) docker     (123)     2830 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/0001_initial.py
--rw-r--r--   0 runner    (1001) docker     (123)     1722 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/0002_auto_20151217_2044.py
--rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/0003_auto_20160322_0929.py
--rw-r--r--   0 runner    (1001) docker     (123)     2196 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/0004_auto_20181024_1538.py
--rw-r--r--   0 runner    (1001) docker     (123)      218 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/0005_remove_accessattempt_trusted.py
--rw-r--r--   0 runner    (1001) docker     (123)      273 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/0006_remove_accesslog_trusted.py
--rw-r--r--   0 runner    (1001) docker     (123)     1216 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/0007_alter_accessattempt_unique_together.py
--rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/0008_accessfailurelog.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/migrations/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1940 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/models.py
--rw-r--r--   0 runner    (1001) docker     (123)     1782 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/signals.py
--rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/axes/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      212 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/codecov.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.898357 django-axes-6.0.0b3/django_axes.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    35865 2023-05-01 18:32:38.000000 django-axes-6.0.0b3/django_axes.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2728 2023-05-01 18:32:38.000000 django-axes-6.0.0b3/django_axes.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-01 18:32:38.000000 django-axes-6.0.0b3/django_axes.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-01 18:32:38.000000 django-axes-6.0.0b3/django_axes.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       50 2023-05-01 18:32:38.000000 django-axes-6.0.0b3/django_axes.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-01 18:32:38.000000 django-axes-6.0.0b3/django_axes.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.902358 django-axes-6.0.0b3/docs/
--rw-r--r--   0 runner    (1001) docker     (123)       43 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/10_changelog.rst
--rw-r--r--   0 runner    (1001) docker     (123)      657 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/1_requirements.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6103 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/2_installation.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4307 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/3_usage.rst
--rw-r--r--   0 runner    (1001) docker     (123)    63233 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/4_configuration.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6274 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/5_customization.rst
--rw-r--r--   0 runner    (1001) docker     (123)     9401 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/6_integration.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3597 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/7_architecture.rst
--rw-r--r--   0 runner    (1001) docker     (123)      406 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/8_reference.rst
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/9_contributing.rst
--rw-r--r--   0 runner    (1001) docker     (123)     7426 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)     4044 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/conf.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.902358 django-axes-6.0.0b3/docs/images/
--rw-r--r--   0 runner    (1001) docker     (123)   133029 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/images/flow.png
--rw-r--r--   0 runner    (1001) docker     (123)      356 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      249 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/manage.py
--rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/mypy.ini
--rw-r--r--   0 runner    (1001) docker     (123)     1345 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       77 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/requirements-qa.txt
--rw-r--r--   0 runner    (1001) docker     (123)      115 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/requirements-test.txt
--rw-r--r--   0 runner    (1001) docker     (123)       88 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-01 18:32:38.910358 django-axes-6.0.0b3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2457 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:38.910358 django-axes-6.0.0b3/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6048 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2239 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/settings.py
--rw-r--r--   0 runner    (1001) docker     (123)     1192 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_admin.py
--rw-r--r--   0 runner    (1001) docker     (123)     5846 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_attempts.py
--rw-r--r--   0 runner    (1001) docker     (123)      747 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_backends.py
--rw-r--r--   0 runner    (1001) docker     (123)     3629 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_checks.py
--rw-r--r--   0 runner    (1001) docker     (123)     1939 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_decorators.py
--rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_failures.py
--rw-r--r--   0 runner    (1001) docker     (123)    21076 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_handlers.py
--rw-r--r--   0 runner    (1001) docker     (123)    31936 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_helpers.py
--rw-r--r--   0 runner    (1001) docker     (123)     4610 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_logging.py
--rw-r--r--   0 runner    (1001) docker     (123)    29839 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_login.py
--rw-r--r--   0 runner    (1001) docker     (123)     3760 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_management.py
--rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_middleware.py
--rw-r--r--   0 runner    (1001) docker     (123)     1321 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_models.py
--rw-r--r--   0 runner    (1001) docker     (123)      489 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/test_signals.py
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-01 18:32:19.000000 django-axes-6.0.0b3/tests/urls_empty.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.171756 django-axes-6.0.0b4/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.163756 django-axes-6.0.0b4/.github/
+-rw-r--r--   0 runner    (1001) docker     (123)      285 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/.github/dependabot.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.163756 django-axes-6.0.0b4/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1425 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/.github/workflows/codeql.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1025 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/.github/workflows/release.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2360 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/.github/workflows/test.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/.prospector.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    32031 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/CHANGES.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2375 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/CODE_OF_CONDUCT.md
+-rw-r--r--   0 runner    (1001) docker     (123)     2328 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/CONTRIBUTING.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1184 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    36297 2023-05-13 11:11:13.171756 django-axes-6.0.0b4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2495 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.163756 django-axes-6.0.0b4/axes/
+-rw-r--r--   0 runner    (1001) docker     (123)      273 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2974 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/admin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1698 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/apps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3216 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/attempts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3855 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/backends.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5175 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/checks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7082 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      628 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/decorators.py
+-rw-r--r--   0 runner    (1001) docker     (123)      380 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/exceptions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.163756 django-axes-6.0.0b4/axes/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7852 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/handlers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6623 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/handlers/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13006 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/handlers/database.py
+-rw-r--r--   0 runner    (1001) docker     (123)      725 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/handlers/dummy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5150 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/handlers/proxy.py
+-rw-r--r--   0 runner    (1001) docker     (123)      687 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/handlers/test.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21297 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/helpers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.159756 django-axes-6.0.0b4/axes/locale/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.159756 django-axes-6.0.0b4/axes/locale/ar/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.163756 django-axes-6.0.0b4/axes/locale/ar/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     2018 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/ar/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2566 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/ar/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.159756 django-axes-6.0.0b4/axes/locale/de/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.163756 django-axes-6.0.0b4/axes/locale/de/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1711 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/de/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2496 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/de/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.159756 django-axes-6.0.0b4/axes/locale/pl/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.163756 django-axes-6.0.0b4/axes/locale/pl/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1526 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/pl/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2266 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/pl/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.159756 django-axes-6.0.0b4/axes/locale/ru/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.167756 django-axes-6.0.0b4/axes/locale/ru/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     2081 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/ru/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2753 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/ru/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.159756 django-axes-6.0.0b4/axes/locale/tr/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.167756 django-axes-6.0.0b4/axes/locale/tr/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1412 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/tr/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2075 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/locale/tr/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.167756 django-axes-6.0.0b4/axes/management/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/management/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.167756 django-axes-6.0.0b4/axes/management/commands/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/management/commands/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      369 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/management/commands/axes_list_attempts.py
+-rw-r--r--   0 runner    (1001) docker     (123)      374 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/management/commands/axes_reset.py
+-rw-r--r--   0 runner    (1001) docker     (123)      659 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/management/commands/axes_reset_failure_logs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      552 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/management/commands/axes_reset_ip.py
+-rw-r--r--   0 runner    (1001) docker     (123)      643 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/management/commands/axes_reset_logs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      579 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/management/commands/axes_reset_username.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1670 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/middleware.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.167756 django-axes-6.0.0b4/axes/migrations/
+-rw-r--r--   0 runner    (1001) docker     (123)     2830 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/0001_initial.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1722 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/0002_auto_20151217_2044.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/0003_auto_20160322_0929.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2196 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/0004_auto_20181024_1538.py
+-rw-r--r--   0 runner    (1001) docker     (123)      218 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/0005_remove_accessattempt_trusted.py
+-rw-r--r--   0 runner    (1001) docker     (123)      273 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/0006_remove_accesslog_trusted.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1216 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/0007_alter_accessattempt_unique_together.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/0008_accessfailurelog.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/migrations/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1940 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1782 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/signals.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2197 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/axes/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      212 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/codecov.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.167756 django-axes-6.0.0b4/django_axes.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    36297 2023-05-13 11:11:13.000000 django-axes-6.0.0b4/django_axes.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2728 2023-05-13 11:11:13.000000 django-axes-6.0.0b4/django_axes.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:11:13.000000 django-axes-6.0.0b4/django_axes.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:11:13.000000 django-axes-6.0.0b4/django_axes.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       50 2023-05-13 11:11:13.000000 django-axes-6.0.0b4/django_axes.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 11:11:13.000000 django-axes-6.0.0b4/django_axes.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.171756 django-axes-6.0.0b4/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)       43 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/10_changelog.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      657 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/1_requirements.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6103 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/2_installation.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4307 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/3_usage.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    64873 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/4_configuration.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     7802 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/5_customization.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     9401 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/6_integration.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3597 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/7_architecture.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      406 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/8_reference.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/9_contributing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     7426 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)     4044 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/conf.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.171756 django-axes-6.0.0b4/docs/images/
+-rw-r--r--   0 runner    (1001) docker     (123)   133029 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/images/flow.png
+-rw-r--r--   0 runner    (1001) docker     (123)      356 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      249 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/manage.py
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/mypy.ini
+-rw-r--r--   0 runner    (1001) docker     (123)     1345 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       78 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/requirements-qa.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      115 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/requirements-test.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       88 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 11:11:13.171756 django-axes-6.0.0b4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2457 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:13.171756 django-axes-6.0.0b4/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6048 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2239 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/settings.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1192 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_admin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5990 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_attempts.py
+-rw-r--r--   0 runner    (1001) docker     (123)      747 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_backends.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3629 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_checks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1939 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_decorators.py
+-rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_failures.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21483 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_handlers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39363 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4625 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)    37892 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_login.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3760 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_management.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_middleware.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1321 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_models.py
+-rw-r--r--   0 runner    (1001) docker     (123)      489 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/test_signals.py
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 11:11:00.000000 django-axes-6.0.0b4/tests/urls_empty.py
```

### Comparing `django-axes-6.0.0b3/.github/workflows/codeql.yml` & `django-axes-6.0.0b4/.github/workflows/codeql.yml`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/.github/workflows/release.yml` & `django-axes-6.0.0b4/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/.github/workflows/test.yml` & `django-axes-6.0.0b4/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/CHANGES.rst` & `django-axes-6.0.0b4/CHANGES.rst`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,21 @@
 
 Changes
 =======
 
 
+6.0.0b4 (2023-05-13)
+--------------------
+
+- Add ``AXES_LOCKOUT_PARAMETERS`` configuration flag that will supersede ``AXES_ONLY_USER_FAILURES``, ``AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP``, ``AXES_LOCK_OUT_BY_USER_OR_IP``, and ``AXES_USE_USER_AGENT`` configurations. Add deprecation warnings for old flags. See project documentation on RTD for update instructions.
+  [hirotasoshu]
+- Improve translations.
+  [hirotasoshu]
+
+
 6.0.0b3 (2023-05-01)
 --------------------
 
 - Use Django ``cache.incr`` API for atomic cached failure counting
   [hirotasoshu, aleksihakli]
 
 
@@ -117,15 +126,15 @@
 - Add support for float or partial hours for ``AXES_COOLOFF_TIME``.
   [hramezani]
 
 
 5.32.0 (2022-04-08)
 -------------------
 
-- Add support for persistent logging
+- Add support for persistent failure logging
   where failed login attempts are persisted in the database
   until a specific threshold is reached.
   [p1-gdd]
 - Add support for not resetting login times when users
   try to login during the lockout cooloff period.
   [antoine-42]
```

### Comparing `django-axes-6.0.0b3/CODE_OF_CONDUCT.md` & `django-axes-6.0.0b4/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/CONTRIBUTING.rst` & `django-axes-6.0.0b4/CONTRIBUTING.rst`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/LICENSE` & `django-axes-6.0.0b4/LICENSE`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/PKG-INFO` & `django-axes-6.0.0b4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-axes
-Version: 6.0.0b3
+Version: 6.0.0b4
 Summary: Keep track of failed login attempts in Django-powered sites.
 Home-page: https://github.com/jazzband/django-axes
 Author: Josh VanderLinden, Philip Neustrom, Michael Blume, Alex Clark, Camilo Nova, Aleksi Hakli
 Author-email: security@jazzband.co
 Maintainer: Jazzband
 Maintainer-email: security@jazzband.co
 License: MIT
@@ -13,16 +13,16 @@
 Project-URL: Tracker, https://github.com/jazzband/django-axes/issues
 Keywords: authentication django pci security
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Web Environment
 Classifier: Environment :: Plugins
 Classifier: Framework :: Django
 Classifier: Framework :: Django :: 3.2
-Classifier: Framework :: Django :: 4.0
 Classifier: Framework :: Django :: 4.1
+Classifier: Framework :: Django :: 4.2
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: System Administrators
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
@@ -124,14 +124,23 @@
 See `CONTRIBUTING <CONTRIBUTING.rst>`__.
 
 
 Changes
 =======
 
 
+6.0.0b4 (2023-05-13)
+--------------------
+
+- Add ``AXES_LOCKOUT_PARAMETERS`` configuration flag that will supersede ``AXES_ONLY_USER_FAILURES``, ``AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP``, ``AXES_LOCK_OUT_BY_USER_OR_IP``, and ``AXES_USE_USER_AGENT`` configurations. Add deprecation warnings for old flags. See project documentation on RTD for update instructions.
+  [hirotasoshu]
+- Improve translations.
+  [hirotasoshu]
+
+
 6.0.0b3 (2023-05-01)
 --------------------
 
 - Use Django ``cache.incr`` API for atomic cached failure counting
   [hirotasoshu, aleksihakli]
 
 
@@ -242,15 +251,15 @@
 - Add support for float or partial hours for ``AXES_COOLOFF_TIME``.
   [hramezani]
 
 
 5.32.0 (2022-04-08)
 -------------------
 
-- Add support for persistent logging
+- Add support for persistent failure logging
   where failed login attempts are persisted in the database
   until a specific threshold is reached.
   [p1-gdd]
 - Add support for not resetting login times when users
   try to login during the lockout cooloff period.
   [antoine-42]
```

### Comparing `django-axes-6.0.0b3/README.rst` & `django-axes-6.0.0b4/README.rst`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/admin.py` & `django-axes-6.0.0b4/axes/admin.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/attempts.py` & `django-axes-6.0.0b4/axes/attempts.py`

 * *Files 2% similar despite different names*

```diff
@@ -34,15 +34,15 @@
     """
     Return a list querysets of AccessAttempts that match the given request and credentials.
     """
 
     username = get_client_username(request, credentials)
 
     filter_kwargs_list = get_client_parameters(
-        username, request.axes_ip_address, request.axes_user_agent
+        username, request.axes_ip_address, request.axes_user_agent, request, credentials
     )
     attempts_list = [
         AccessAttempt.objects.filter(**filter_kwargs)
         for filter_kwargs in filter_kwargs_list
     ]
     return attempts_list
```

### Comparing `django-axes-6.0.0b3/axes/backends.py` & `django-axes-6.0.0b4/axes/backends.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/checks.py` & `django-axes-6.0.0b4/axes/checks.py`

 * *Files 4% similar despite different names*

```diff
@@ -124,14 +124,21 @@
         "AXES_LOGGER",
         # AXES_PROXY_ and AXES_META_ parameters were updated to more explicit
         # AXES_IPWARE_PROXY_ and AXES_IPWARE_META_ prefixes in version 6.x
         "AXES_PROXY_ORDER",
         "AXES_PROXY_COUNT",
         "AXES_PROXY_TRUSTED_IPS",
         "AXES_META_PRECEDENCE_ORDER",
+        # AXES_ONLY_USER_FAILURES, AXES_USE_USER_AGENT and
+        # AXES_LOCK_OUT parameters were replaced with AXES_LOCKOUT_PARAMETERS
+        # in version 6.x
+        "AXES_ONLY_USER_FAILURES",
+        "AXES_LOCK_OUT_BY_USER_OR_IP",
+        "AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP",
+        "AXES_USE_USER_AGENT",
     ]
 
     for deprecated_setting in deprecated_settings:
         try:
             getattr(settings, deprecated_setting)
             warnings.append(
                 Warning(
```

### Comparing `django-axes-6.0.0b3/axes/conf.py` & `django-axes-6.0.0b4/axes/conf.py`

 * *Files 12% similar despite different names*

```diff
@@ -6,36 +6,45 @@
 
 # see if the user has overridden the failure limit
 settings.AXES_FAILURE_LIMIT = getattr(settings, "AXES_FAILURE_LIMIT", 3)
 
 # see if the user has set axes to lock out logins after failure limit
 settings.AXES_LOCK_OUT_AT_FAILURE = getattr(settings, "AXES_LOCK_OUT_AT_FAILURE", True)
 
-# lock out with the combination of username and IP address
-settings.AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP = getattr(
-    settings, "AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP", False
-)
-
-# lock out with the username or IP address
-settings.AXES_LOCK_OUT_BY_USER_OR_IP = getattr(
-    settings, "AXES_LOCK_OUT_BY_USER_OR_IP", False
-)
-
-# lock out with username and never the IP or user agent
-settings.AXES_ONLY_USER_FAILURES = getattr(settings, "AXES_ONLY_USER_FAILURES", False)
+# lockout parameters
+# default value will be ["ip_address"] after removing AXES_LOCK_OUT params support
+settings.AXES_LOCKOUT_PARAMETERS = getattr(settings, "AXES_LOCKOUT_PARAMETERS", None)
+
+# TODO: remove it in future versions
+if settings.AXES_LOCKOUT_PARAMETERS is None:
+    if getattr(settings, "AXES_ONLY_USER_FAILURES", False):
+        settings.AXES_LOCKOUT_PARAMETERS = ["username"]
+    else:
+        if getattr(settings, "AXES_LOCK_OUT_BY_USER_OR_IP", False):
+            settings.AXES_LOCKOUT_PARAMETERS = ["username", "ip_address"]
+        elif getattr(settings, "AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP", False):
+            settings.AXES_LOCKOUT_PARAMETERS = [["username", "ip_address"]]
+        else:
+            settings.AXES_LOCKOUT_PARAMETERS = ["ip_address"]
+
+    if getattr(settings, "AXES_USE_USER_AGENT", False):
+        if isinstance(settings.AXES_LOCKOUT_PARAMETERS[0], str):
+            settings.AXES_LOCKOUT_PARAMETERS[0] = [
+                settings.AXES_LOCKOUT_PARAMETERS[0],
+                "user_agent",
+            ]
+        else:
+            settings.AXES_LOCKOUT_PARAMETERS[0].append("user_agent")
 
 # lock out just for admin site
 settings.AXES_ONLY_ADMIN_SITE = getattr(settings, "AXES_ONLY_ADMIN_SITE", False)
 
 # show Axes logs in admin
 settings.AXES_ENABLE_ADMIN = getattr(settings, "AXES_ENABLE_ADMIN", True)
 
-# lock out with the user agent, has no effect when ONLY_USER_FAILURES is set
-settings.AXES_USE_USER_AGENT = getattr(settings, "AXES_USE_USER_AGENT", False)
-
 # use a specific username field to retrieve from login POST data
 settings.AXES_USERNAME_FORM_FIELD = getattr(
     settings, "AXES_USERNAME_FORM_FIELD", "username"
 )
 
 # use a specific password field to retrieve from login POST data
 settings.AXES_PASSWORD_FORM_FIELD = getattr(
```

### Comparing `django-axes-6.0.0b3/axes/decorators.py` & `django-axes-6.0.0b4/axes/decorators.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/handlers/base.py` & `django-axes-6.0.0b4/axes/handlers/base.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/handlers/cache.py` & `django-axes-6.0.0b4/axes/handlers/cache.py`

 * *Files 4% similar despite different names*

```diff
@@ -7,14 +7,15 @@
     get_cache,
     get_cache_timeout,
     get_client_cache_keys,
     get_client_str,
     get_client_username,
     get_credentials,
     get_failure_limit,
+    get_lockout_parameters,
 )
 from axes.models import AccessAttempt
 from axes.signals import user_locked_out
 
 log = getLogger(__name__)
 
 
@@ -74,17 +75,18 @@
         if request is None:
             log.error(
                 "AXES: AxesCacheHandler.user_login_failed does not function without a request."
             )
             return
 
         username = get_client_username(request, credentials)
-        if settings.AXES_ONLY_USER_FAILURES and username is None:
+        lockout_parameters = get_lockout_parameters(request, credentials)
+        if lockout_parameters == ["username"] and username is None:
             log.warning(
-                "AXES: Username is None and AXES_ONLY_USER_FAILURES is enabled, new record will NOT be created."
+                "AXES: Username is None and username is the only one lockout parameter, new record will NOT be created."
             )
             return
 
         # If axes denied access, don't record the failed attempt as that would reset the lockout time.
         if (
             not settings.AXES_RESET_COOL_OFF_ON_FAILURE_DURING_LOCKOUT
             and request.axes_locked_out
```

### Comparing `django-axes-6.0.0b3/axes/handlers/database.py` & `django-axes-6.0.0b4/axes/handlers/database.py`

 * *Files 3% similar despite different names*

```diff
@@ -14,14 +14,15 @@
 from axes.conf import settings
 from axes.handlers.base import AxesBaseHandler, AbstractAxesHandler
 from axes.helpers import (
     get_client_str,
     get_client_username,
     get_credentials,
     get_failure_limit,
+    get_lockout_parameters,
     get_query_str,
 )
 from axes.models import AccessLog, AccessAttempt, AccessFailureLog
 from axes.signals import user_locked_out
 
 log = getLogger(__name__)
 
@@ -160,17 +161,18 @@
         post_data = get_query_str(request.POST).replace("\0", "0x00")
 
         if self.is_whitelisted(request, credentials):
             log.info("AXES: Login failed from whitelisted client %s.", client_str)
             return
 
         # 2. database query: Get or create access record with the new failure data
-        if settings.AXES_ONLY_USER_FAILURES and username is None:
+        lockout_parameters = get_lockout_parameters(request, credentials)
+        if lockout_parameters == ["username"] and username is None:
             log.warning(
-                "AXES: Username is None and AXES_ONLY_USER_FAILURES is enabled, new record will NOT be created."
+                "AXES: Username is None and username is the only one lockout parameter, new record will NOT be created."
             )
         else:
             with transaction.atomic():
                 (
                     attempt,
                     created,
                 ) = AccessAttempt.objects.select_for_update().get_or_create(
```

### Comparing `django-axes-6.0.0b3/axes/handlers/dummy.py` & `django-axes-6.0.0b4/axes/handlers/dummy.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/handlers/proxy.py` & `django-axes-6.0.0b4/axes/handlers/proxy.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/handlers/test.py` & `django-axes-6.0.0b4/axes/handlers/test.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/helpers.py` & `django-axes-6.0.0b4/axes/helpers.py`

 * *Files 11% similar despite different names*

```diff
@@ -213,43 +213,79 @@
     return request.META.get("PATH_INFO", "<unknown>")[:255]
 
 
 def get_client_http_accept(request: HttpRequest) -> str:
     return request.META.get("HTTP_ACCEPT", "<unknown>")[:1025]
 
 
-def get_client_parameters(username: str, ip_address: str, user_agent: str) -> list:
+def get_lockout_parameters(
+    request_or_attempt: Union[HttpRequest, AccessBase],
+    credentials: Optional[dict] = None,
+) -> List[Union[str, List[str]]]:
+    if callable(settings.AXES_LOCKOUT_PARAMETERS):
+        return settings.AXES_LOCKOUT_PARAMETERS(request_or_attempt, credentials)
+
+    if isinstance(settings.AXES_LOCKOUT_PARAMETERS, str):
+        return import_string(settings.AXES_LOCKOUT_PARAMETERS)(
+            request_or_attempt, credentials
+        )
+
+    if isinstance(settings.AXES_LOCKOUT_PARAMETERS, list):
+        return settings.AXES_LOCKOUT_PARAMETERS
+
+    raise TypeError(
+        "settings.AXES_LOCKOUT_PARAMETERS needs to be a callable or iterable"
+    )
+
+
+def get_client_parameters(
+    username: str,
+    ip_address: str,
+    user_agent: str,
+    request_or_attempt: Union[HttpRequest, AccessBase],
+    credentials: Optional[dict] = None,
+) -> List[dict]:
     """
     Get query parameters for filtering AccessAttempt queryset.
 
     This method returns a dict that guarantees iteration order for keys and values,
     and can so be used in e.g. the generation of hash keys or other deterministic functions.
 
     Returns list of dict, every item of list are separate parameters
     """
+    lockout_parameters = get_lockout_parameters(request_or_attempt, credentials)
 
-    if settings.AXES_ONLY_USER_FAILURES:
-        # 1. Only individual usernames can be tracked with parametrization
-        filter_query = [{"username": username}]
-    else:
-        if settings.AXES_LOCK_OUT_BY_USER_OR_IP:
-            # One of `username` or `IP address` is used
-            filter_query = [{"username": username}, {"ip_address": ip_address}]
-        elif settings.AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP:
-            # 2. A combination of username and IP address can be used as well
-            filter_query = [{"username": username, "ip_address": ip_address}]
-        else:
-            # 3. Default case is to track the IP address only, which is the most secure option
-            filter_query = [{"ip_address": ip_address}]
-
-        if settings.AXES_USE_USER_AGENT:
-            # 4. The HTTP User-Agent can be used to track e.g. one browser
-            filter_query[0]["user_agent"] = user_agent
+    parameters_dict = {
+        "username": username,
+        "ip_address": ip_address,
+        "user_agent": user_agent,
+    }
+
+    filter_kwargs = []
+
+    for parameter in lockout_parameters:
+        try:
+            if isinstance(parameter, str):
+                filter_kwarg = {parameter: parameters_dict[parameter]}
+            else:
+                filter_kwarg = {
+                    combined_parameter: parameters_dict[combined_parameter]
+                    for combined_parameter in parameter
+                }
+            filter_kwargs.append(filter_kwarg)
+
+        except KeyError as e:
+            error_msg = (
+                f"{e} lockout parameter is not allowed. "
+                f"Allowed parameters: {', '.join(parameters_dict.keys())}"
+            )
+            log.exception(error_msg)
+            raise ValueError(error_msg) from e
 
-    return filter_query
+    return filter_kwargs
 
 
 def make_cache_key_list(filter_kwargs_list: List[dict]) -> List[str]:
     cache_keys = []
     for filter_kwargs in filter_kwargs_list:
         cache_key_components = "".join(
             value for value in filter_kwargs.values() if value
@@ -276,15 +312,17 @@
         ip_address = request_or_attempt.ip_address
         user_agent = request_or_attempt.user_agent
     else:
         username = get_client_username(request_or_attempt, credentials)
         ip_address = get_client_ip_address(request_or_attempt)
         user_agent = get_client_user_agent(request_or_attempt)
 
-    filter_kwargs_list = get_client_parameters(username, ip_address, user_agent)
+    filter_kwargs_list = get_client_parameters(
+        username, ip_address, user_agent, request_or_attempt, credentials
+    )
 
     return make_cache_key_list(filter_kwargs_list)
 
 
 def get_client_str(
     username: str,
     ip_address: str,
@@ -319,15 +357,15 @@
     if settings.AXES_VERBOSE:
         # Verbose mode logs every attribute that is available
         client_dict["username"] = username
         client_dict["ip_address"] = ip_address
         client_dict["user_agent"] = user_agent
     else:
         # Other modes initialize the attributes that are used for the actual lockouts
-        client_list = get_client_parameters(username, ip_address, user_agent)
+        client_list = get_client_parameters(username, ip_address, user_agent, request)
         client_dict = {}
         for client in client_list:
             client_dict.update(client)
     client_dict = cleanse_parameters(client_dict.copy())
     # Path info is always included as last component in the client string for traceability purposes
     if path_info and isinstance(path_info, (tuple, list)):
         path_info = path_info[0]
```

### Comparing `django-axes-6.0.0b3/axes/locale/ar/LC_MESSAGES/django.mo` & `django-axes-6.0.0b4/axes/locale/ar/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/locale/ar/LC_MESSAGES/django.po` & `django-axes-6.0.0b4/axes/locale/ar/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/locale/de/LC_MESSAGES/django.mo` & `django-axes-6.0.0b4/axes/locale/de/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/locale/de/LC_MESSAGES/django.po` & `django-axes-6.0.0b4/axes/locale/de/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/locale/pl/LC_MESSAGES/django.mo` & `django-axes-6.0.0b4/axes/locale/pl/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/locale/pl/LC_MESSAGES/django.po` & `django-axes-6.0.0b4/axes/locale/pl/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/locale/ru/LC_MESSAGES/django.mo` & `django-axes-6.0.0b4/axes/locale/ru/LC_MESSAGES/django.mo`

 * *Files 16% similar despite different names*

#### msgunfmt {}

```diff
@@ -7,66 +7,75 @@
 "Language-Team: LANGUAGE <LL@li.org>\n"
 "Language: \n"
 "MIME-Version: 1.0\n"
 "Content-Type: text/plain; charset=UTF-8\n"
 "Content-Transfer-Encoding: 8bit\n"
 "Plural-Forms: nplurals=2; plural=(n != 1);\n"
 
+msgid "Access lock out"
+msgstr "Доступ запрещен"
+
 msgid ""
 "Account locked: too many login attempts. Contact an admin to unlock your "
 "account."
 msgstr ""
-"Учетная запись заблокирована: слишком много попыток входа. Обратитесь к "
-"администратору для разблокирования учетной записи."
+"Учетная запись заблокирована: слишком много попыток входа. Свяжитесь с "
+"администратором, чтобы разблокировать учетную запись."
 
 msgid "Account locked: too many login attempts. Please try again later."
 msgstr ""
 "Учетная запись заблокирована: слишком много попыток входа. Повторите попытку "
 "позже."
 
 msgid "Attempt Time"
-msgstr "Время входа"
+msgstr "Время попытки входа"
 
 msgid "Failed Logins"
 msgstr "Ошибочные попытки"
 
 msgid "Form Data"
 msgstr "Данные формы"
 
 msgid "GET Data"
 msgstr "Данные GET-запроса"
 
 msgid "HTTP Accept"
-msgstr "Запрос HTTP"
+msgstr "HTTP Accept"
 
 msgid "IP Address"
-msgstr "Адрес IP"
+msgstr "IP Адрес"
 
 msgid "Logout Time"
 msgstr "Время выхода"
 
 msgid "Meta Data"
 msgstr "Метаданные"
 
 msgid "POST Data"
 msgstr "Данные POST-запроса"
 
 msgid "Path"
 msgstr "Путь"
 
 msgid "User Agent"
-msgstr "Браузер пользователя"
+msgstr "User Agent"
 
 msgid "Username"
-msgstr "Пользователь"
+msgstr "Имя пользователя"
 
 msgid "access attempt"
 msgstr "Запись о попытке доступа"
 
 msgid "access attempts"
 msgstr "Попытки доступа"
 
+msgid "access failure"
+msgstr "Ошибка доступа"
+
+msgid "access failures"
+msgstr "Ошибки доступа"
+
 msgid "access log"
 msgstr "Запись о доступе"
 
 msgid "access logs"
 msgstr "Логи доступа"
```

### Comparing `django-axes-6.0.0b3/axes/locale/ru/LC_MESSAGES/django.po` & `django-axes-6.0.0b4/axes/locale/ru/LC_MESSAGES/django.po`

 * *Files 13% similar despite different names*

```diff
@@ -4,94 +4,106 @@
 # FIRST AUTHOR <EMAIL@ADDRESS>, YEAR.
 #
 #, fuzzy
 msgid ""
 msgstr ""
 "Project-Id-Version: PACKAGE VERSION\n"
 "Report-Msgid-Bugs-To: \n"
-"POT-Creation-Date: 2019-01-11 12:20+0300\n"
+"POT-Creation-Date: 2023-05-13 12:36+0500\n"
 "PO-Revision-Date: YEAR-MO-DA HO:MI+ZONE\n"
 "Last-Translator: FULL NAME <EMAIL@ADDRESS>\n"
 "Language-Team: LANGUAGE <LL@li.org>\n"
 "Language: \n"
 "MIME-Version: 1.0\n"
 "Content-Type: text/plain; charset=UTF-8\n"
 "Content-Transfer-Encoding: 8bit\n"
 "Plural-Forms: nplurals=2; plural=(n != 1);\n"
 
-#: axes/admin.py:38
+#: axes/admin.py:27
 msgid "Form Data"
 msgstr "Данные формы"
 
-#: axes/admin.py:41 axes/admin.py:95
+#: axes/admin.py:28 axes/admin.py:65 axes/admin.py:100
 msgid "Meta Data"
 msgstr "Метаданные"
 
-#: axes/conf.py:58
+#: axes/conf.py:99
 msgid "Account locked: too many login attempts. Please try again later."
 msgstr ""
-"Учетная запись заблокирована: слишком много попыток входа. "
-"Повторите попытку позже."
+"Учетная запись заблокирована: слишком много попыток входа. Повторите попытку "
+"позже."
 
-#: axes/conf.py:61
+#: axes/conf.py:107
 msgid ""
 "Account locked: too many login attempts. Contact an admin to unlock your "
 "account."
 msgstr ""
-"Учетная запись заблокирована: слишком много попыток входа. "
-"Обратитесь к администратору для разблокирования учетной записи."
+"Учетная запись заблокирована: слишком много попыток входа. Свяжитесь с "
+"администратором, чтобы разблокировать учетную запись."
 
-#: axes/models.py:9
+#: axes/models.py:6
 msgid "User Agent"
-msgstr "Браузер пользователя"
+msgstr "User Agent"
 
-#: axes/models.py:15
+#: axes/models.py:8
 msgid "IP Address"
-msgstr "Адрес IP"
+msgstr "IP Адрес"
 
-#: axes/models.py:21
+#: axes/models.py:10
 msgid "Username"
-msgstr "Пользователь"
+msgstr "Имя пользователя"
 
-#: axes/models.py:35
+#: axes/models.py:12
 msgid "HTTP Accept"
-msgstr "Запрос HTTP"
+msgstr "HTTP Accept"
 
-#: axes/models.py:40
+#: axes/models.py:14
 msgid "Path"
 msgstr "Путь"
 
-#: axes/models.py:45
+#: axes/models.py:16
 msgid "Attempt Time"
-msgstr "Время входа"
+msgstr "Время попытки входа"
+
+#: axes/models.py:26
+msgid "Access lock out"
+msgstr "Доступ запрещен"
+
+#: axes/models.py:34
+msgid "access failure"
+msgstr "Ошибка доступа"
+
+#: axes/models.py:35
+msgid "access failures"
+msgstr "Ошибки доступа"
 
-#: axes/models.py:57
+#: axes/models.py:39
 msgid "GET Data"
 msgstr "Данные GET-запроса"
 
-#: axes/models.py:61
+#: axes/models.py:41
 msgid "POST Data"
 msgstr "Данные POST-запроса"
 
-#: axes/models.py:65
+#: axes/models.py:43
 msgid "Failed Logins"
 msgstr "Ошибочные попытки"
 
-#: axes/models.py:76
+#: axes/models.py:49
 msgid "access attempt"
 msgstr "Запись о попытке доступа"
 
-#: axes/models.py:77
+#: axes/models.py:50
 msgid "access attempts"
 msgstr "Попытки доступа"
 
-#: axes/models.py:81
+#: axes/models.py:55
 msgid "Logout Time"
 msgstr "Время выхода"
 
-#: axes/models.py:90
+#: axes/models.py:61
 msgid "access log"
 msgstr "Запись о доступе"
 
-#: axes/models.py:91
+#: axes/models.py:62
 msgid "access logs"
 msgstr "Логи доступа"
```

### Comparing `django-axes-6.0.0b3/axes/locale/tr/LC_MESSAGES/django.mo` & `django-axes-6.0.0b4/axes/locale/tr/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/locale/tr/LC_MESSAGES/django.po` & `django-axes-6.0.0b4/axes/locale/tr/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/management/commands/axes_reset_failure_logs.py` & `django-axes-6.0.0b4/axes/management/commands/axes_reset_failure_logs.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/management/commands/axes_reset_ip.py` & `django-axes-6.0.0b4/axes/management/commands/axes_reset_ip.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/management/commands/axes_reset_logs.py` & `django-axes-6.0.0b4/axes/management/commands/axes_reset_logs.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/management/commands/axes_reset_username.py` & `django-axes-6.0.0b4/axes/management/commands/axes_reset_username.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/middleware.py` & `django-axes-6.0.0b4/axes/middleware.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/migrations/0001_initial.py` & `django-axes-6.0.0b4/axes/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/migrations/0002_auto_20151217_2044.py` & `django-axes-6.0.0b4/axes/migrations/0002_auto_20151217_2044.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/migrations/0003_auto_20160322_0929.py` & `django-axes-6.0.0b4/axes/migrations/0003_auto_20160322_0929.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/migrations/0004_auto_20181024_1538.py` & `django-axes-6.0.0b4/axes/migrations/0004_auto_20181024_1538.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/migrations/0007_alter_accessattempt_unique_together.py` & `django-axes-6.0.0b4/axes/migrations/0007_alter_accessattempt_unique_together.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/migrations/0008_accessfailurelog.py` & `django-axes-6.0.0b4/axes/migrations/0008_accessfailurelog.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/models.py` & `django-axes-6.0.0b4/axes/models.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/signals.py` & `django-axes-6.0.0b4/axes/signals.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/axes/utils.py` & `django-axes-6.0.0b4/axes/utils.py`

 * *Files 21% similar despite different names*

```diff
@@ -6,17 +6,16 @@
 """
 
 from logging import getLogger
 from typing import Optional
 
 from django.http import HttpRequest
 
-from axes.conf import settings
 from axes.handlers.proxy import AxesProxyHandler
-from axes.helpers import get_client_ip_address
+from axes.helpers import get_client_ip_address, get_lockout_parameters
 
 log = getLogger(__name__)
 
 
 def reset(
     ip: Optional[str] = None, username: Optional[str] = None, ip_or_username=False
 ) -> int:
@@ -33,27 +32,42 @@
 
 def reset_request(request: HttpRequest) -> int:
     """
     Reset records that match IP or username, and return the count of removed attempts.
 
     This utility method is meant to be used from the CLI or via Python API.
     """
+    lockout_paramaters = get_lockout_parameters(request)
 
     ip: Optional[str] = get_client_ip_address(request)
     username = request.GET.get("username", None)
 
-    ip_or_username = settings.AXES_LOCK_OUT_BY_USER_OR_IP
-    if settings.AXES_ONLY_USER_FAILURES:
+    ip_required = False
+    username_required = False
+    ip_and_username = False
+
+    for param in lockout_paramaters:
+        # hack: in works with all iterables, including strings
+        # so this checks works with separate parameters
+        # and with parameters combinations
+        if "username" in param and "ip_address" in param:
+            ip_and_username = True
+            ip_required = True
+            username_required = True
+            break
+        if "username" in param:
+            username_required = True
+        elif "ip_address" in param:
+            ip_required = True
+
+    ip_or_username = not ip_and_username and ip_required and username_required
+    if not ip_required:
         ip = None
-    elif not (
-        settings.AXES_LOCK_OUT_BY_USER_OR_IP
-        or settings.AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP
-    ):
+    if not username_required:
         username = None
 
     if not ip and not username:
         return 0
         # We don't want to reset everything, if there is some wrong request parameter
 
-    # if settings.AXES_USE_USER_AGENT:
     # TODO: reset based on user_agent?
     return reset(ip, username, ip_or_username)
```

### Comparing `django-axes-6.0.0b3/django_axes.egg-info/PKG-INFO` & `django-axes-6.0.0b4/django_axes.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-axes
-Version: 6.0.0b3
+Version: 6.0.0b4
 Summary: Keep track of failed login attempts in Django-powered sites.
 Home-page: https://github.com/jazzband/django-axes
 Author: Josh VanderLinden, Philip Neustrom, Michael Blume, Alex Clark, Camilo Nova, Aleksi Hakli
 Author-email: security@jazzband.co
 Maintainer: Jazzband
 Maintainer-email: security@jazzband.co
 License: MIT
@@ -13,16 +13,16 @@
 Project-URL: Tracker, https://github.com/jazzband/django-axes/issues
 Keywords: authentication django pci security
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Web Environment
 Classifier: Environment :: Plugins
 Classifier: Framework :: Django
 Classifier: Framework :: Django :: 3.2
-Classifier: Framework :: Django :: 4.0
 Classifier: Framework :: Django :: 4.1
+Classifier: Framework :: Django :: 4.2
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: System Administrators
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
@@ -124,14 +124,23 @@
 See `CONTRIBUTING <CONTRIBUTING.rst>`__.
 
 
 Changes
 =======
 
 
+6.0.0b4 (2023-05-13)
+--------------------
+
+- Add ``AXES_LOCKOUT_PARAMETERS`` configuration flag that will supersede ``AXES_ONLY_USER_FAILURES``, ``AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP``, ``AXES_LOCK_OUT_BY_USER_OR_IP``, and ``AXES_USE_USER_AGENT`` configurations. Add deprecation warnings for old flags. See project documentation on RTD for update instructions.
+  [hirotasoshu]
+- Improve translations.
+  [hirotasoshu]
+
+
 6.0.0b3 (2023-05-01)
 --------------------
 
 - Use Django ``cache.incr`` API for atomic cached failure counting
   [hirotasoshu, aleksihakli]
 
 
@@ -242,15 +251,15 @@
 - Add support for float or partial hours for ``AXES_COOLOFF_TIME``.
   [hramezani]
 
 
 5.32.0 (2022-04-08)
 -------------------
 
-- Add support for persistent logging
+- Add support for persistent failure logging
   where failed login attempts are persisted in the database
   until a specific threshold is reached.
   [p1-gdd]
 - Add support for not resetting login times when users
   try to login during the lockout cooloff period.
   [antoine-42]
```

### Comparing `django-axes-6.0.0b3/django_axes.egg-info/SOURCES.txt` & `django-axes-6.0.0b4/django_axes.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/docs/1_requirements.rst` & `django-axes-6.0.0b4/docs/1_requirements.rst`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/docs/2_installation.rst` & `django-axes-6.0.0b4/docs/2_installation.rst`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/docs/3_usage.rst` & `django-axes-6.0.0b4/docs/3_usage.rst`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/docs/4_configuration.rst` & `django-axes-6.0.0b4/docs/4_configuration.rst`

 * *Files 7% similar despite different names*

```diff
@@ -23,23 +23,23 @@
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_LOCK_OUT_AT_FAILURE                             | True                                         | After the number of allowed login attempts are exceeded, should we lock out this IP (and optional user agent)?                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_COOLOFF_TIME                                    | None                                         | If set, defines a period of inactivity after which  old failed login attempts will be cleared.  Can be set to a Python timedelta object, an integer, a float, a callable, or a string path to a callable which takes no arguments.  If an integer or float, will be interpreted as a number of hours:  ``AXES_COOLOFF_TIME = 2`` 2 hours,   ``AXES_COOLOFF_TIME = 2.0`` 2 hours, 120 minutes,  ``AXES_COOLOFF_TIME = 1.7`` 1.7 hours, 102 minutes, 6120 seconds                                                                                                                                                                                                                                                                           |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_ONLY_ADMIN_SITE                                 | False                                        | If ``True``, lock is only enabled for admin site. Admin site is determined by checking request path against the path of ``"admin:index"`` view. If admin urls are not registered in current urlconf, all requests will not be locked.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
-| AXES_ONLY_USER_FAILURES                              | False                                        | If ``True``, only lock based on username, and never lock based on IP if attempts exceed the limit. Otherwise utilize the existing IP and user locking logic.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
+| AXES_ONLY_USER_FAILURES                              | False                                        | DEPRECATED: USE ``AXES_LOCKOUT_PARAMETERS ISNTEAD``. If ``True``, only lock based on username, and never lock based on IP if attempts exceed the limit. Otherwise utilize the existing IP and user locking logic.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_ENABLE_ADMIN                                    | True                                         | If ``True``, admin views for access attempts and logins are shown in Django admin interface.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
-| AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP             | False                                        | If ``True``, prevent login from IP under a particular username if the attempt limit has been exceeded, otherwise lock out based on IP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
+| AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP             | False                                        | DEPRECATED: USE ``AXES_LOCKOUT_PARAMETERS`` INSTEAD. If ``True``, prevent login from IP under a particular username if the attempt limit has been exceeded, otherwise lock out based on IP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
-| AXES_LOCK_OUT_BY_USER_OR_IP                          | False                                        |  If ``True``, prevent login from if the attempt limit has been exceeded for IP or username.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
+| AXES_LOCK_OUT_BY_USER_OR_IP                          | False                                        | DEPRECATED: USE ``AXES_LOCKOUT_PARAMETERS`` INSTEAD. If ``True``, prevent login from if the attempt limit has been exceeded for IP or username.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
-| AXES_USE_USER_AGENT                                  | False                                        | If ``True``, lock out and log based on the IP address and the user agent.  This means requests from different user agents but from the same IP are treated differently. This settings has no effect if the ``AXES_ONLY_USER_FAILURES`` setting is active.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
+| AXES_USE_USER_AGENT                                  | False                                        | DEPRECATED: USE ``AXES_LOCKOUT_PARAMETERS`` INSTEAD. If ``True``, lock out and log based on the IP address and the user agent.  This means requests from different user agents but from the same IP are treated differently. This settings has no effect if the ``AXES_ONLY_USER_FAILURES`` setting is active.                                                                                                                                                                                                                                                                                                                                                                                                                            |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_HANDLER                                         | 'axes.handlers.database.AxesDatabaseHandler' | The path to the handler class to use. If set, overrides the default signal handler backend. Default: ``'axes.handlers.database.AxesDatabaseHandler'``                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_CACHE                                           | 'default'                                    | The name of the cache for Axes to use.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_LOCKOUT_TEMPLATE                                | None                                         |  If set, specifies a template to render when a user is locked out. Template receives ``cooloff_timedelta``, ``cooloff_time``, ``username`` and ``failure_limit`` as context variables.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
@@ -79,14 +79,16 @@
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_ALLOWED_CORS_ORIGINS                            | "*"                                          | Configures lockout response CORS headers for XHR requests.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_HTTP_RESPONSE_CODE                              | 429                                          | Sets the http response code returned when ``AXES_FAILURE_LIMIT`` is reached. For example: ``AXES_HTTP_RESPONSE_CODE = 403``                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 | AXES_RESET_COOL_OFF_ON_FAILURE_DURING_LOCKOUT        | True                                         |  If ``True``, a failed login attempt during lockout will reset the cool off period.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
 +------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
+| AXES_LOCKOUT_PARAMETERS                              | ["ip_address"]                               |  A list of parameters that Axes uses to lock out users. It can also be callable, which takes an http request or AccesAttempt object and credentials and returns a list of parameters. Each parameter can be a string (a single parameter) or a list of strings (a combined parameter). For example, if you configure ``AXES_LOCKOUT_PARAMETERS = ["ip_address", ["username", "user_agent"]]``, axes will block clients by ip and/or username and user agent combination. See :ref:`customizing-lockout-parameters` for more details.                                                                                                                                                                                                      |
++------------------------------------------------------+----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
 
 The configuration option precedences for the access attempt monitoring are:
 
 1. Default: only use IP address.
 2. ``AXES_ONLY_USER_FAILURES``: only user username (``AXES_USE_USER_AGENT`` has no effect).
 3. ``AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP``: use username and IP address.
```

### Comparing `django-axes-6.0.0b3/docs/5_customization.rst` & `django-axes-6.0.0b4/docs/5_customization.rst`

 * *Files 16% similar despite different names*

```diff
@@ -151,15 +151,14 @@
 
 .. note::
    You still have to make these modifications yourself before calling
    authenticate. If you want to re-use the same function for consistency, that's
    fine, but Axes does not inject these changes into the authentication flow
    for you.
 
-
 Customizing lockout responses
 -----------------------------
 
 Axes can be configured with ``AXES_LOCKOUT_CALLABLE`` to return a custom lockout response when using the plugin with e.g. DRF (Django REST Framework) or other third party libraries which require specialized formats such as JSON or XML response formats or customized response status codes.
 
 An example of usage could be e.g. a custom view for processing lockouts.
 
@@ -170,17 +169,58 @@
     def lockout(request, credentials, *args, **kwargs):
         return JsonResponse({"status": "Locked out due to too many login failures"}, status=403)
 
 ``settings.py``::
 
     AXES_LOCKOUT_CALLABLE = "example.views.lockout"
 
+.. _customizing-lockout-parameters:
+
+Customizing lockout parameters
+------------------------------
+
+Axes can be configured with ``AXES_LOCKOUT_PARAMETERS`` to lock out users not only by IP address.
+
+``AXES_LOCKOUT_PARAMETERS`` can be a list of strings (which represents a separate lockout parameter) or nested lists of strings (which represents lockout parameters used in combination) or a callable which accepts HttpRequest or AccessAttempt and credentials and returns a list of the same form as described earlier.
+
+Example ``AXES_LOCKOUT_PARAMETERS`` configuration:
+
+``settings.py``::
+
+    AXES_LOCKOUT_PARAMETERS = ["ip_address", ["username", "user_agent"]]
+
+This way, axes will lock out users using ip_address and/or combination of username and user agent
+
+Example of callable ``AXES_LOCKOUT_PARAMETERS``:
+
+``example/utils.py``::
+
+    from django.http import HttpRequest
+
+    def get_lockout_parameters(request_or_attempt, credentials):
+
+        if isinstance(request_or_attempt, HttpRequest):
+           is_localhost = request.META.get("REMOTE_ADDR") == "127.0.0.1"
+
+        else:
+           is_localhost = request_or_attempt.ip_address == "127.0.0.1"
+        
+        if is_localhost:
+           return ["username"] 
+        
+        return ["ip_address", "username"]
+
+``settings.py``::
+
+    AXES_LOCKOUT_CALLABLE = "example.utils.get_lockout_parameters"
+
+This way, if client ip_address is localhost, axes will lockout client only by username. In other case, axes will lockout client by username and/or ip_address.
 
 Customizing client ip address lookups
------------------------------
+-------------------------------------
 
 Axes can be configured with ``AXES_CLIENT_IP_CALLABLE`` to use custom client ip address lookup logic.
 
 ``example/utils.py``::
 
     def get_client_ip(request):
         return request.META.get("REMOTE_ADDR")
```

### Comparing `django-axes-6.0.0b3/docs/6_integration.rst` & `django-axes-6.0.0b4/docs/6_integration.rst`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/docs/7_architecture.rst` & `django-axes-6.0.0b4/docs/7_architecture.rst`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/docs/Makefile` & `django-axes-6.0.0b4/docs/Makefile`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/docs/conf.py` & `django-axes-6.0.0b4/docs/conf.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/docs/images/flow.png` & `django-axes-6.0.0b4/docs/images/flow.png`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/pyproject.toml` & `django-axes-6.0.0b4/pyproject.toml`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/setup.py` & `django-axes-6.0.0b4/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -44,16 +44,16 @@
     packages=find_packages(exclude=["tests"]),
     classifiers=[
         "Development Status :: 5 - Production/Stable",
         "Environment :: Web Environment",
         "Environment :: Plugins",
         "Framework :: Django",
         "Framework :: Django :: 3.2",
-        "Framework :: Django :: 4.0",
         "Framework :: Django :: 4.1",
+        "Framework :: Django :: 4.2",
         "Intended Audience :: Developers",
         "Intended Audience :: System Administrators",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
         "Programming Language :: Python",
         "Programming Language :: Python :: 3",
         "Programming Language :: Python :: 3.7",
```

### Comparing `django-axes-6.0.0b3/tests/base.py` & `django-axes-6.0.0b4/tests/base.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/settings.py` & `django-axes-6.0.0b4/tests/settings.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/test_admin.py` & `django-axes-6.0.0b4/tests/test_admin.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/test_attempts.py` & `django-axes-6.0.0b4/tests/test_attempts.py`

 * *Files 8% similar despite different names*

```diff
@@ -78,78 +78,78 @@
 
     def test_reset_ip_username(self):
         self.request.GET["username"] = self.USERNAME_1
         self.request.META["REMOTE_ADDR"] = self.IP_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 3)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_reset_user_failures(self):
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 5)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_reset_ip_user_failures(self):
         self.request.META["REMOTE_ADDR"] = self.IP_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 5)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_reset_username_user_failures(self):
         self.request.GET["username"] = self.USERNAME_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 3)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_reset_ip_username_user_failures(self):
         self.request.GET["username"] = self.USERNAME_1
         self.request.META["REMOTE_ADDR"] = self.IP_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 3)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_reset_user_or_ip(self):
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 5)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_reset_ip_user_or_ip(self):
         self.request.META["REMOTE_ADDR"] = self.IP_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 3)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_reset_username_user_or_ip(self):
         self.request.GET["username"] = self.USERNAME_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 3)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_reset_ip_username_user_or_ip(self):
         self.request.GET["username"] = self.USERNAME_1
         self.request.META["REMOTE_ADDR"] = self.IP_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 2)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_reset_user_and_ip(self):
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 5)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_reset_ip_user_and_ip(self):
         self.request.META["REMOTE_ADDR"] = self.IP_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 3)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_reset_username_user_and_ip(self):
         self.request.GET["username"] = self.USERNAME_1
         reset_request(self.request)
         self.assertEqual(AccessAttempt.objects.count(), 3)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_AND=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_reset_ip_username_user_and_ip(self):
         self.request.GET["username"] = self.USERNAME_1
         self.request.META["REMOTE_ADDR"] = self.IP_1
         reset_request(self.request)
-        self.assertEqual(AccessAttempt.objects.count(), 3)
+        self.assertEqual(AccessAttempt.objects.count(), 4)
```

### Comparing `django-axes-6.0.0b3/tests/test_backends.py` & `django-axes-6.0.0b4/tests/test_backends.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/test_checks.py` & `django-axes-6.0.0b4/tests/test_checks.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/test_decorators.py` & `django-axes-6.0.0b4/tests/test_decorators.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/test_failures.py` & `django-axes-6.0.0b4/tests/test_failures.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/test_handlers.py` & `django-axes-6.0.0b4/tests/test_handlers.py`

 * *Files 3% similar despite different names*

```diff
@@ -257,15 +257,18 @@
         self.assertEqual(1, AxesProxyHandler.reset_failure_logs(age_days=42))
         self.assertEqual(AccessFailureLog.objects.count(), 1)
 
     def test_handler_remove_out_of_limit_failure_logs(self):
         _more = 10
         for i in range(settings.AXES_ACCESS_FAILURE_LOG_PER_USER_LIMIT + _more):
             self.create_failure_log()
-        self.assertEqual(_more, AxesProxyHandler.remove_out_of_limit_failure_logs(username=self.username))
+        self.assertEqual(
+            _more,
+            AxesProxyHandler.remove_out_of_limit_failure_logs(username=self.username),
+        )
 
     @override_settings(AXES_RESET_ON_SUCCESS=True)
     def test_handler(self):
         self.check_handler()
 
     @override_settings(AXES_RESET_ON_SUCCESS=False)
     def test_handler_without_reset(self):
@@ -292,52 +295,67 @@
     def test_empty_request(self, log):
         self.check_empty_request(log, "AxesDatabaseHandler")
 
     @patch("axes.handlers.database.log")
     def test_whitelist(self, log):
         self.check_whitelist(log)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     @patch("axes.handlers.database.log")
     def test_user_login_failed_only_user_failures_with_none_username(self, log):
         credentials = {"username": None, "password": "test"}
         sender = MagicMock()
         AxesProxyHandler.user_login_failed(sender, credentials, self.request)
         attempt = AccessAttempt.objects.all()
         self.assertEqual(0, AccessAttempt.objects.count())
         log.warning.assert_called_with(
-            "AXES: Username is None and AXES_ONLY_USER_FAILURES is enabled, new record will NOT be created."
+            "AXES: Username is None and username is the only one lockout parameter, new record will NOT be created."
         )
 
     def test_user_login_failed_with_none_username(self):
         credentials = {"username": None, "password": "test"}
         sender = MagicMock()
         AxesProxyHandler.user_login_failed(sender, credentials, self.request)
         attempt = AccessAttempt.objects.all()
         self.assertEqual(1, AccessAttempt.objects.filter(username__isnull=True).count())
 
     def test_user_login_failed_multiple_username(self):
         configurations = (
             (2, 1, {}, ["admin", "admin1"]),
-            (2, 1, {"AXES_USE_USER_AGENT": True}, ["admin", "admin1"]),
-            (2, 1, {"AXES_ONLY_USER_FAILURES": True}, ["admin", "admin1"]),
             (
                 2,
                 1,
-                {"AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP": True},
+                {"AXES_LOCKOUT_PARAMETERS": [["ip_address", "user_agent"]]},
+                ["admin", "admin1"],
+            ),
+            (2, 1, {"AXES_LOCKOUT_PARAMETERS": ["username"]}, ["admin", "admin1"]),
+            (
+                2,
+                1,
+                {"AXES_LOCKOUT_PARAMETERS": [["username", "ip_address"]]},
                 ["admin", "admin1"],
             ),
             (
                 1,
                 2,
-                {"AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP": True},
+                {"AXES_LOCKOUT_PARAMETERS": [["username", "ip_address"]]},
                 ["admin", "admin"],
             ),
-            (1, 2, {"AXES_LOCK_OUT_BY_USER_OR_IP": True}, ["admin", "admin"]),
-            (2, 1, {"AXES_LOCK_OUT_BY_USER_OR_IP": True}, ["admin", "admin1"]),
+            (
+                1,
+                2,
+                {"AXES_LOCKOUT_PARAMETERS": ["username", "ip_address"]},
+                ["admin", "admin"],
+            ),
+            (
+                2,
+                1,
+                {"AXES_LOCKOUT_PARAMETERS": ["username", "ip_address"]},
+                ["admin", "admin1"],
+            ),
         )
 
         for (
             total_attempts_count,
             failures_since_start,
             overrides,
             usernames,
@@ -396,15 +414,15 @@
         finally:
             self.request.META["REMOTE_ADDR"] = prev_ip
 
     def test_handler_reset_attempts(self):
         with self.assertRaises(NotImplementedError):
             AxesProxyHandler.reset_attempts()
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_handler_reset_attempts_username(self):
         self.set_up_login_attempts()
         self.assertEqual(
             2,
             AxesProxyHandler.get_failures(
                 self.request, credentials={"username": self.USERNAME_1}
             ),
@@ -432,15 +450,15 @@
     def test_handler_reset_attempts_ip(self):
         self.set_up_login_attempts()
         self.check_failures(2, ip_address=self.IP_1)
         self.assertEqual(1, AxesProxyHandler.reset_attempts(ip_address=self.IP_1))
         self.check_failures(0, ip_address=self.IP_1)
         self.check_failures(2, ip_address=self.IP_2)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_handler_reset_attempts_ip_and_username(self):
         self.set_up_login_attempts()
         self.check_failures(1, username=self.USERNAME_1, ip_address=self.IP_1)
         self.check_failures(1, username=self.USERNAME_2, ip_address=self.IP_1)
         self.check_failures(1, username=self.USERNAME_1, ip_address=self.IP_2)
         self.assertEqual(
             1,
@@ -478,26 +496,26 @@
     def test_empty_request(self, log):
         self.check_empty_request(log, "AxesCacheHandler")
 
     @patch("axes.handlers.cache.log")
     def test_whitelist(self, log):
         self.check_whitelist(log)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     @patch.object(cache, "set")
     @patch("axes.handlers.cache.log")
     def test_user_login_failed_only_user_failures_with_none_username(
         self, log, cache_set
     ):
         credentials = {"username": None, "password": "test"}
         sender = MagicMock()
         AxesProxyHandler.user_login_failed(sender, credentials, self.request)
         self.assertFalse(cache_set.called)
         log.warning.assert_called_with(
-            "AXES: Username is None and AXES_ONLY_USER_FAILURES is enabled, new record will NOT be created."
+            "AXES: Username is None and username is the only one lockout parameter, new record will NOT be created."
         )
 
     @patch.object(cache, "add")
     def test_user_login_failed_with_none_username(self, cache_add):
         credentials = {"username": None, "password": "test"}
         sender = MagicMock()
         AxesProxyHandler.user_login_failed(sender, credentials, self.request)
```

### Comparing `django-axes-6.0.0b3/tests/test_helpers.py` & `django-axes-6.0.0b4/tests/test_helpers.py`

 * *Files 17% similar despite different names*

```diff
@@ -146,15 +146,15 @@
         expected = '{ip_address: "127.0.0.1", path_info: "/admin/"}'
         actual = get_client_str(
             username, ip_address, user_agent, path_info, self.request
         )
 
         self.assertEqual(expected, actual)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     @override_settings(AXES_VERBOSE=True)
     def test_verbose_user_only_client_details(self):
         username = "test@example.com"
         ip_address = "127.0.0.1"
         user_agent = "Googlebot/2.1 (+http://www.googlebot.com/bot.html)"
         path_info = "/admin/"
 
@@ -163,30 +163,30 @@
         )
         actual = get_client_str(
             username, ip_address, user_agent, path_info, self.request
         )
 
         self.assertEqual(expected, actual)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     @override_settings(AXES_VERBOSE=False)
     def test_non_verbose_user_only_client_details(self):
         username = "test@example.com"
         ip_address = "127.0.0.1"
         user_agent = "Googlebot/2.1 (+http://www.googlebot.com/bot.html)"
         path_info = "/admin/"
 
         expected = '{username: "test@example.com", path_info: "/admin/"}'
         actual = get_client_str(
             username, ip_address, user_agent, path_info, self.request
         )
 
         self.assertEqual(expected, actual)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     @override_settings(AXES_VERBOSE=True)
     def test_verbose_user_ip_combo_client_details(self):
         username = "test@example.com"
         ip_address = "127.0.0.1"
         user_agent = "Googlebot/2.1 (+http://www.googlebot.com/bot.html)"
         path_info = "/admin/"
 
@@ -195,30 +195,30 @@
         )
         actual = get_client_str(
             username, ip_address, user_agent, path_info, self.request
         )
 
         self.assertEqual(expected, actual)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     @override_settings(AXES_VERBOSE=False)
     def test_non_verbose_user_ip_combo_client_details(self):
         username = "test@example.com"
         ip_address = "127.0.0.1"
         user_agent = "Googlebot/2.1 (+http://www.googlebot.com/bot.html)"
         path_info = "/admin/"
 
         expected = '{username: "test@example.com", ip_address: "127.0.0.1", path_info: "/admin/"}'
         actual = get_client_str(
             username, ip_address, user_agent, path_info, self.request
         )
 
         self.assertEqual(expected, actual)
 
-    @override_settings(AXES_USE_USER_AGENT=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["ip_address", "user_agent"]])
     @override_settings(AXES_VERBOSE=True)
     def test_verbose_user_agent_client_details(self):
         username = "test@example.com"
         ip_address = "127.0.0.1"
         user_agent = "Googlebot/2.1 (+http://www.googlebot.com/bot.html)"
         path_info = "/admin/"
 
@@ -227,15 +227,15 @@
         )
         actual = get_client_str(
             username, ip_address, user_agent, path_info, self.request
         )
 
         self.assertEqual(expected, actual)
 
-    @override_settings(AXES_USE_USER_AGENT=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["ip_address", "user_agent"]])
     @override_settings(AXES_VERBOSE=False)
     def test_non_verbose_user_agent_client_details(self):
         username = "test@example.com"
         ip_address = "127.0.0.1"
         user_agent = "Googlebot/2.1 (+http://www.googlebot.com/bot.html)"
         path_info = "/admin/"
 
@@ -296,84 +296,270 @@
 
 def get_dummy_client_str_using_request(
     username, ip_address, user_agent, path_info, request
 ):
     return f"{request.user.email}"
 
 
+def get_dummy_lockout_parameters(request, credentials=None):
+    return ["ip_address", ["username", "user_agent"]]
+
+
 class ClientParametersTestCase(AxesTestCase):
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_get_filter_kwargs_user(self):
         self.assertEqual(
-            get_client_parameters(self.username, self.ip_address, self.user_agent),
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
             [{"username": self.username}],
         )
 
-    @override_settings(
-        AXES_ONLY_USER_FAILURES=False,
-        AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=False,
-        AXES_USE_USER_AGENT=False,
-    )
     def test_get_filter_kwargs_ip(self):
         self.assertEqual(
-            get_client_parameters(self.username, self.ip_address, self.user_agent),
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
             [{"ip_address": self.ip_address}],
         )
 
-    @override_settings(
-        AXES_ONLY_USER_FAILURES=False,
-        AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True,
-        AXES_USE_USER_AGENT=False,
-    )
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_get_filter_kwargs_user_and_ip(self):
         self.assertEqual(
-            get_client_parameters(self.username, self.ip_address, self.user_agent),
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
             [{"username": self.username, "ip_address": self.ip_address}],
         )
 
-    @override_settings(
-        AXES_ONLY_USER_FAILURES=False,
-        AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=False,
-        AXES_LOCK_OUT_BY_USER_OR_IP=True,
-        AXES_USE_USER_AGENT=False,
-    )
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "user_agent"]])
+    def test_get_filter_kwargs_user_and_user_agent(self):
+        self.assertEqual(
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
+            [{"username": self.username, "user_agent": self.user_agent}],
+        )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["ip_address", ["username", "user_agent"]])
+    def test_get_filter_kwargs_ip_or_user_and_user_agent(self):
+        self.assertEqual(
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
+            [{"ip_address": self.ip_address}, {"username": self.username, "user_agent": self.user_agent}],
+        )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["ip_address", "user_agent"], ["username", "user_agent"]])
+    def test_get_filter_kwargs_ip_and_user_agent_or_user_and_user_agent(self):
+        self.assertEqual(
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
+            [{"ip_address": self.ip_address, "user_agent": self.user_agent}, {"username": self.username, "user_agent": self.user_agent}],
+        )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_get_filter_kwargs_user_or_ip(self):
         self.assertEqual(
-            get_client_parameters(self.username, self.ip_address, self.user_agent),
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
             [{"username": self.username}, {"ip_address": self.ip_address}],
         )
 
-    @override_settings(
-        AXES_ONLY_USER_FAILURES=False,
-        AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=False,
-        AXES_USE_USER_AGENT=True,
-    )
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address", "user_agent"])
+    def test_get_filter_kwargs_user_or_ip_or_user_agent(self):
+        self.assertEqual(
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
+            [{"username": self.username}, {"ip_address": self.ip_address}, {"user_agent": self.user_agent}],
+        )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["ip_address", "user_agent"]])
     def test_get_filter_kwargs_ip_and_agent(self):
         self.assertEqual(
-            get_client_parameters(self.username, self.ip_address, self.user_agent),
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
             [{"ip_address": self.ip_address, "user_agent": self.user_agent}],
         )
 
     @override_settings(
-        AXES_ONLY_USER_FAILURES=False,
-        AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True,
-        AXES_USE_USER_AGENT=True,
+        AXES_LOCKOUT_PARAMETERS=[["username", "ip_address", "user_agent"]]
     )
     def test_get_filter_kwargs_user_ip_agent(self):
         self.assertEqual(
-            get_client_parameters(self.username, self.ip_address, self.user_agent),
+            get_client_parameters(self.username, self.ip_address, self.user_agent, self.request, self.credentials),
             [
                 {
                     "username": self.username,
                     "ip_address": self.ip_address,
                     "user_agent": self.user_agent,
                 },
             ],
         )
 
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["wrong_param"])
+    @patch("axes.helpers.log")
+    def test_get_filter_kwargs_invalid_parameter(self, log):
+        with self.assertRaises(ValueError):
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            )
+            log.exception.assert_called_with(
+                (
+                    "wrong_param lockout parameter is not allowed. "
+                    "Allowed lockout parameters: username, ip_address, user_agent"
+                )
+            )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["ip_address", "wrong_param"]])
+    @patch("axes.helpers.log")
+    def test_get_filter_kwargs_invalid_combined_parameter(self, log):
+        with self.assertRaises(ValueError):
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            )
+            log.exception.assert_called_with(
+                (
+                    "wrong_param lockout parameter is not allowed. "
+                    "Allowed lockout parameters: username, ip_address, user_agent"
+                )
+            )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=get_dummy_lockout_parameters)
+    def test_get_filter_kwargs_callable_lockout_parameters(self):
+        self.assertEqual(
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            ),
+            [
+                {
+                    "ip_address": self.ip_address,
+                },
+                {
+                    "username": self.username,
+                    "user_agent": self.user_agent,
+                },
+            ],
+        )
+
+    @override_settings(
+        AXES_LOCKOUT_PARAMETERS="tests.test_helpers.get_dummy_lockout_parameters"
+    )
+    def test_get_filter_kwargs_callable_str_lockout_parameters(self):
+        self.assertEqual(
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            ),
+            [
+                {
+                    "ip_address": self.ip_address,
+                },
+                {
+                    "username": self.username,
+                    "user_agent": self.user_agent,
+                },
+            ],
+        )
+
+    @override_settings(
+        AXES_LOCKOUT_PARAMETERS=lambda request, credentials: ["username"]
+    )
+    def test_get_filter_kwargs_callable_lambda_lockout_parameters(self):
+        self.assertEqual(
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            ),
+            [
+                {
+                    "username": self.username,
+                },
+            ],
+        )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=True)
+    def test_get_filter_kwargs_not_list_or_callable(self):
+        with self.assertRaises(TypeError):
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=lambda: None)
+    def test_get_filter_kwargs_invalid_callable_too_few_arguments(self):
+        with self.assertRaises(TypeError):
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            )
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=lambda request, credentials, extra: None)
+    def test_get_filter_kwargs_invalid_callable_too_many_arguments(self):
+        with self.assertRaises(TypeError):
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            )
+
+    @override_settings(
+        AXES_LOCKOUT_PARAMETERS=lambda request, credentials: ["wrong_param"]
+    )
+    @patch("axes.helpers.log")
+    def test_get_filter_kwargs_callable_invalid_lockout_param(self, log):
+        with self.assertRaises(ValueError):
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            )
+            log.exception.assert_called_with(
+                (
+                    "wrong_param lockout parameter is not allowed. "
+                    "Allowed lockout parameters: username, ip_address, user_agent"
+                )
+            )
+
+    @override_settings(
+        AXES_LOCKOUT_PARAMETERS=lambda request, credentials: [
+            ["ip_address", "wrong_param"]
+        ]
+    )
+    @patch("axes.helpers.log")
+    def test_get_filter_kwargs_callable_invalid_combined_lockout_param(self, log):
+        with self.assertRaises(ValueError):
+            get_client_parameters(
+                self.username,
+                self.ip_address,
+                self.user_agent,
+                self.request,
+                self.credentials,
+            )
+            log.exception.assert_called_with(
+                (
+                    "wrong_param lockout parameter is not allowed. "
+                    "Allowed lockout parameters: username, ip_address, user_agent"
+                )
+            )
+
 
 class ClientCacheKeyTestCase(AxesTestCase):
     def test_get_cache_keys(self):
         """
         Test the cache key format.
         """
```

### Comparing `django-axes-6.0.0b3/tests/test_logging.py` & `django-axes-6.0.0b4/tests/test_logging.py`

 * *Files 6% similar despite different names*

```diff
@@ -30,33 +30,34 @@
         )
 
     @override_settings(AXES_VERBOSE=False)
     def test_axes_config_log_not_verbose(self, log):
         AppConfig.initialize()
         self.assertFalse(log.info.called)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_axes_config_log_user_only(self, log):
         AppConfig.initialize()
-        log.info.assert_called_with(_BEGIN, _VERSION, "blocking by username only")
+        log.info.assert_called_with(_BEGIN, _VERSION, "blocking by username")
 
-    @override_settings(AXES_ONLY_USER_FAILURES=False)
     def test_axes_config_log_ip_only(self, log):
         AppConfig.initialize()
-        log.info.assert_called_with(_BEGIN, _VERSION, "blocking by IP only")
+        log.info.assert_called_with(_BEGIN, _VERSION, "blocking by ip_address")
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_axes_config_log_user_ip(self, log):
         AppConfig.initialize()
-        log.info.assert_called_with(_BEGIN, _VERSION, "blocking by combination of username and IP")
+        log.info.assert_called_with(
+            _BEGIN, _VERSION, "blocking by combination of username and ip_address"
+        )
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_axes_config_log_user_or_ip(self, log):
         AppConfig.initialize()
-        log.info.assert_called_with(_BEGIN, _VERSION, "blocking by username or IP")
+        log.info.assert_called_with(_BEGIN, _VERSION, "blocking by username or ip_address")
 
 
 class AccessLogTestCase(AxesTestCase):
     def test_access_log_on_logout(self):
         """
         Test a valid logout and make sure the logout_time is updated.
         """
```

### Comparing `django-axes-6.0.0b3/tests/test_login.py` & `django-axes-6.0.0b4/tests/test_login.py`

 * *Files 23% similar despite different names*

```diff
@@ -178,35 +178,36 @@
         self.login(is_valid_username=True, is_valid_password=True)
         self.assertFalse(self.attempt_count())
 
         response = self.lockout()
         self.assertContains(response, self.LOCKED_MESSAGE, status_code=self.BLOCKED)
         self.assertTrue(self.attempt_count())
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_combination_user_and_ip(self):
         """
-        Test login failure when AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP is True.
+        Test login failure when lockout parameters is combination
+        of username and ip_address.
         """
 
         # test until one try before the limit
         for _ in range(1, settings.AXES_FAILURE_LIMIT):
             response = self.login(is_valid_username=True, is_valid_password=False)
             # Check if we are in the same login page
             self.assertContains(response, self.LOGIN_FORM_KEY, html=True)
 
         # So, we shouldn't have gotten a lock-out yet.
         # But we should get one now
         response = self.login(is_valid_username=True, is_valid_password=False)
         self.assertContains(response, self.LOCKED_MESSAGE, status_code=429)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_only_user_failures(self):
         """
-        Test login failure when AXES_ONLY_USER_FAILURES is True.
+        Test login failure when lockout parameter is username.
         """
 
         # test until one try before the limit
         for _ in range(1, settings.AXES_FAILURE_LIMIT):
             response = self._login(self.username, self.WRONG_PASSWORD)
 
             # Check if we are in the same login page
@@ -234,14 +235,147 @@
 
         # Check if we can still log in with valid user
         response = self._login(self.username, self.password)
         self.assertNotContains(
             response, self.LOGIN_FORM_KEY, status_code=self.ALLOWED, html=True
         )
 
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["user_agent"])
+    def test_lockout_by_user_agent_only(self):
+        """
+        Test login failure when lockout parameter is only user_agent
+        """
+        # User is locked out with "test-browser" user agent.
+        self._lockout_user_from_ip(username="username", ip_addr=self.IP_1, user_agent="test-browser")
+
+        # Test he is locked:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked with another username:
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked with another ip:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test with another user agent:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser-2")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["ip_address", "username", "user_agent"])
+    def test_lockout_by_all_parameters(self):
+        # User is locked out with "test-browser" user agent.
+        self._lockout_user_from_ip(username="username", ip_addr=self.IP_1, user_agent="test-browser")
+
+        # Test he is locked:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked by username:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked by ip:
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked by user_agent:
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+       
+        # Test he is allowed to login with different username, ip and user_agent
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["ip_address", "username", "user_agent"]])
+    def test_lockout_by_combination_of_all_parameters(self):
+        # User is locked out with "test-browser" user agent.
+        self._lockout_user_from_ip(username="username", ip_addr=self.IP_1, user_agent="test-browser")
+
+        # Test he is locked:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is allowed to login with different username:
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+        # Test he is allowed to login with different IP:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+        # Test he is allowed to login with different user_agent:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+       
+        # Test he is allowed to login with different username, ip and user_agent
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["ip_address", ["username", "user_agent"]])
+    def test_lockout_by_ip_or_username_and_user_agent(self):
+        # User is locked out with "test-browser" user agent.
+        self._lockout_user_from_ip(username="username", ip_addr=self.IP_1, user_agent="test-browser")
+
+        # Test he is locked:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked by ip:
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked by username and user_agent:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is allowed to login with different username and ip
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+        # Test he is allowed to login with different user_agent and ip
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+        # Test he is allowed to login with different username, ip and user_agent
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["ip_address", "user_agent"], ["username", "user_agent"]])
+    def test_lockout_by_ip_and_user_agent_or_username_and_user_agent(self):
+        # User is locked out with "test-browser" user agent.
+        self._lockout_user_from_ip(username="username", ip_addr=self.IP_1, user_agent="test-browser")
+
+        # Test he is locked:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked by ip and user_agent:
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is locked by username and user_agent:
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.BLOCKED)
+
+        # Test he is allowed to login with different username and ip
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+        # Test he is allowed to login with different user_agent
+        response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+        # Test he is allowed to login with different username, ip and user_agent
+        response = self._login("username2", self.VALID_PASSWORD, ip_addr=self.IP_2, user_agent="test-browser2")
+        self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
+
+
     # Test for true and false positives when blocking by IP *OR* user (default)
     # Cache disabled. Default settings.
     def test_lockout_by_ip_blocks_when_same_user_same_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is still blocked from IP 1.
@@ -270,109 +404,109 @@
 
         # User 2 can still login from IP 2.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
     # Test for true and false positives when blocking by user only.
     # Cache disabled. When AXES_ONLY_USER_FAILURES = True
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_blocks_when_same_user_same_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is still blocked from IP 1.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_blocks_when_same_user_diff_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is also locked out from IP 2.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_allows_when_diff_user_same_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 1.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_allows_when_diff_user_diff_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 2.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_with_empty_username_allows_other_users_without_cache(self):
         # User with empty username is locked out from IP 1.
         self._lockout_user_from_ip(username="", ip_addr=self.IP_1)
 
         # Still possible to access the login page
         response = self.client.get(reverse("admin:login"), REMOTE_ADDR=self.IP_1)
         self.assertContains(response, self.LOGIN_FORM_KEY, status_code=200, html=True)
 
     # Test for true and false positives when blocking by user and IP together.
     # Cache disabled. When LOCK_OUT_BY_COMBINATION_USER_AND_IP = True
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_blocks_when_same_user_same_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is still blocked from IP 1.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_allows_when_same_user_diff_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 can still login from IP 2.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_allows_when_diff_user_same_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 1.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_allows_when_diff_user_diff_ip_without_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 2.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_with_empty_username_allows_other_users_without_cache(
         self,
     ):
         # User with empty username is locked out from IP 1.
         self._lockout_user_from_ip(username="", ip_addr=self.IP_1)
 
         # Still possible to access the login page
         response = self.client.get(reverse("admin:login"), REMOTE_ADDR=self.IP_1)
         self.assertContains(response, self.LOGIN_FORM_KEY, status_code=200, html=True)
 
-    @override_settings(AXES_USE_USER_AGENT=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["ip_address", "user_agent"]])
     def test_lockout_by_user_still_allows_login_with_differnet_user_agent(self):
         # User with empty username is locked out with "test-browser" user agent.
         self._lockout_user_from_ip(username="username", ip_addr=self.IP_1, user_agent="test-browser")
 
         # Test he is locked:
         response = self._login("username", self.VALID_PASSWORD, ip_addr=self.IP_1, user_agent="test-browser")
         self.assertEqual(response.status_code, self.BLOCKED)
@@ -411,101 +545,101 @@
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 2.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_with_empty_username_allows_other_users_using_cache(self):
         # User with empty username is locked out from IP 1.
         self._lockout_user_from_ip(username="", ip_addr=self.IP_1)
 
         # Still possible to access the login page
         response = self.client.get(reverse("admin:login"), REMOTE_ADDR=self.IP_1)
         self.assertContains(response, self.LOGIN_FORM_KEY, status_code=200, html=True)
 
     # Test for true and false positives when blocking by user only.
     # With cache enabled. When AXES_ONLY_USER_FAILURES = True
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_blocks_when_same_user_same_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is still blocked from IP 1.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_blocks_when_same_user_diff_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is also locked out from IP 2.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_allows_when_diff_user_same_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 1.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_ONLY_USER_FAILURES=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username"])
     def test_lockout_by_user_allows_when_diff_user_diff_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 2.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
     # Test for true and false positives when blocking by user and IP together.
     # With cache enabled. When LOCK_OUT_BY_COMBINATION_USER_AND_IP = True
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_blocks_when_same_user_same_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is still blocked from IP 1.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_allows_when_same_user_diff_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 can still login from IP 2.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_allows_when_diff_user_same_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 1.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_allows_when_diff_user_diff_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 2.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
     @override_settings(
-        AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True, AXES_FAILURE_LIMIT=2
+        AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]], AXES_FAILURE_LIMIT=2
     )
     def test_lockout_by_user_and_ip_allows_when_diff_user_same_ip_using_cache_multiple_attempts(
         self,
     ):
         # User 1 is locked out from IP 1.
         response = self._login(self.USER_1, self.WRONG_PASSWORD, self.IP_1)
         self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
@@ -526,55 +660,57 @@
         response = self._login(self.USER_1, self.WRONG_PASSWORD, ip_addr=self.IP_2)
         self.assertContains(response, self.LOCKED_MESSAGE, status_code=self.BLOCKED)
 
         # User 2 can still login from IP 2, only he has 1 attempt left
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_LOCK_OUT_BY_COMBINATION_USER_AND_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=[["username", "ip_address"]])
     def test_lockout_by_user_and_ip_with_empty_username_allows_other_users_using_cache(
         self,
     ):
         # User with empty username is locked out from IP 1.
         self._lockout_user_from_ip(username="", ip_addr=self.IP_1)
 
         # Still possible to access the login page
         response = self.client.get(reverse("admin:login"), REMOTE_ADDR=self.IP_1)
         self.assertContains(response, self.LOGIN_FORM_KEY, status_code=200, html=True)
 
     # Test for true and false positives when blocking by user or IP together.
     # With cache enabled. When AXES_LOCK_OUT_BY_USER_OR_IP = True
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_lockout_by_user_or_ip_blocks_when_same_user_same_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is still blocked from IP 1.
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_lockout_by_user_or_ip_allows_when_same_user_diff_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 1 is blocked out from IP 1
         response = self._login(self.USER_1, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_lockout_by_user_or_ip_allows_when_diff_user_same_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 1.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_1)
         self.assertEqual(response.status_code, self.BLOCKED)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True, AXES_FAILURE_LIMIT=3)
+    @override_settings(
+        AXES_LOCKOUT_PARAMETERS=["username", "ip_address"], AXES_FAILURE_LIMIT=3
+    )
     def test_lockout_by_user_or_ip_allows_when_diff_user_same_ip_using_cache_multiple_attempts(
         self,
     ):
         # User 1 is locked out from IP 1.
         response = self._login(self.USER_1, self.WRONG_PASSWORD, self.IP_1)
         self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
 
@@ -596,15 +732,17 @@
         response = self._login(self.USER_1, self.WRONG_PASSWORD, ip_addr=self.IP_1)
         self.assertContains(response, self.LOCKED_MESSAGE, status_code=self.BLOCKED)
         response = self._login(self.USER_2, self.WRONG_PASSWORD, ip_addr=self.IP_1)
         self.assertContains(response, self.LOCKED_MESSAGE, status_code=self.BLOCKED)
         response = self._login(self.USER_3, self.WRONG_PASSWORD, ip_addr=self.IP_1)
         self.assertContains(response, self.LOCKED_MESSAGE, status_code=self.BLOCKED)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True, AXES_FAILURE_LIMIT=3)
+    @override_settings(
+        AXES_LOCKOUT_PARAMETERS=["username", "ip_address"], AXES_FAILURE_LIMIT=3
+    )
     def test_lockout_by_user_or_ip_allows_when_diff_user_same_ip_using_cache_multiple_failed_attempts(
         self,
     ):
         """Test, if the failed attempts make also impact on the attempt count"""
         # User 1 is locked out from IP 1.
         response = self._login(self.USER_1, self.WRONG_PASSWORD, self.IP_1)
         self.assertEqual(response.status_code, self.ATTEMPT_NOT_BLOCKED)
@@ -621,24 +759,24 @@
         response = self._login(self.USER_1, self.WRONG_PASSWORD, ip_addr=self.IP_2)
         self.assertContains(response, self.LOCKED_MESSAGE, status_code=self.BLOCKED)
 
         # On IP 2 it is only 2. attempt, for user 2 it is also 2. attempt -> allow log in
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_lockout_by_user_or_ip_allows_when_diff_user_diff_ip_using_cache(self):
         # User 1 is locked out from IP 1.
         self._lockout_user1_from_ip1()
 
         # User 2 can still login from IP 2.
         response = self._login(self.USER_2, self.VALID_PASSWORD, ip_addr=self.IP_2)
         self.assertEqual(response.status_code, self.ALLOWED)
 
-    @override_settings(AXES_LOCK_OUT_BY_USER_OR_IP=True)
+    @override_settings(AXES_LOCKOUT_PARAMETERS=["username", "ip_address"])
     def test_lockout_by_user_or_ip_with_empty_username_allows_other_users_using_cache(
         self,
     ):
         # User with empty username is locked out from IP 1.
         self._lockout_user_from_ip(username="", ip_addr=self.IP_1)
 
         # Still possible to access the login page
```

### Comparing `django-axes-6.0.0b3/tests/test_management.py` & `django-axes-6.0.0b4/tests/test_management.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/test_middleware.py` & `django-axes-6.0.0b4/tests/test_middleware.py`

 * *Files identical despite different names*

### Comparing `django-axes-6.0.0b3/tests/test_models.py` & `django-axes-6.0.0b4/tests/test_models.py`

 * *Files identical despite different names*

