# Comparing `tmp/django-formtools-2.4.tar.gz` & `tmp/django-formtools-2.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-formtools-2.4.tar", last modified: Wed Sep 28 18:33:18 2022, max compression
+gzip compressed data, was "django-formtools-2.4.1.tar", last modified: Sat May 13 12:49:58 2023, max compression
```

## Comparing `django-formtools-2.4.tar` & `django-formtools-2.4.1.tar`

### file list

```diff
@@ -1,385 +1,385 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.600195 django-formtools-2.4/
--rw-r--r--   0 runner    (1001) docker     (121)       71 2022-09-28 18:33:04.000000 django-formtools-2.4/.coveragerc
--rw-r--r--   0 runner    (1001) docker     (121)      202 2022-09-28 18:33:04.000000 django-formtools-2.4/.editorconfig
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.540192 django-formtools-2.4/.github/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.568193 django-formtools-2.4/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (121)     1004 2022-09-28 18:33:04.000000 django-formtools-2.4/.github/workflows/release.yml
--rw-r--r--   0 runner    (1001) docker     (121)      764 2022-09-28 18:33:04.000000 django-formtools-2.4/.github/workflows/test.yml
--rw-r--r--   0 runner    (1001) docker     (121)       92 2022-09-28 18:33:04.000000 django-formtools-2.4/.gitignore
--rw-r--r--   0 runner    (1001) docker     (121)       10 2022-09-28 18:33:04.000000 django-formtools-2.4/.pre-commit-config.yaml
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.568193 django-formtools-2.4/.tx/
--rw-r--r--   0 runner    (1001) docker     (121)      256 2022-09-28 18:33:04.000000 django-formtools-2.4/.tx/config
--rw-r--r--   0 runner    (1001) docker     (121)      819 2022-09-28 18:33:04.000000 django-formtools-2.4/AUTHORS.rst
--rw-r--r--   0 runner    (1001) docker     (121)     2375 2022-09-28 18:33:04.000000 django-formtools-2.4/CODE_OF_CONDUCT.md
--rw-r--r--   0 runner    (1001) docker     (121)      338 2022-09-28 18:33:04.000000 django-formtools-2.4/CONTRIBUTING.rst
--rw-r--r--   0 runner    (1001) docker     (121)     1562 2022-09-28 18:33:04.000000 django-formtools-2.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)      257 2022-09-28 18:33:04.000000 django-formtools-2.4/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)      665 2022-09-28 18:33:04.000000 django-formtools-2.4/Makefile
--rw-r--r--   0 runner    (1001) docker     (121)     3882 2022-09-28 18:33:18.600195 django-formtools-2.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2594 2022-09-28 18:33:04.000000 django-formtools-2.4/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.568193 django-formtools-2.4/django_formtools.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     3882 2022-09-28 18:33:18.000000 django-formtools-2.4/django_formtools.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     8071 2022-09-28 18:33:18.000000 django-formtools-2.4/django_formtools.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-09-28 18:33:18.000000 django-formtools-2.4/django_formtools.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-09-28 18:33:18.000000 django-formtools-2.4/django_formtools.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (121)       12 2022-09-28 18:33:18.000000 django-formtools-2.4/django_formtools.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       10 2022-09-28 18:33:18.000000 django-formtools-2.4/django_formtools.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.568193 django-formtools-2.4/docs/
--rw-r--r--   0 runner    (1001) docker     (121)     6802 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (121)     2369 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/changelog.rst
--rw-r--r--   0 runner    (1001) docker     (121)    10698 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/conf.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.568193 django-formtools-2.4/docs/extensions/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/extensions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      153 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/extensions/settings.py
--rw-r--r--   0 runner    (1001) docker     (121)     2838 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (121)     6721 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (121)     4460 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/preview.rst
--rw-r--r--   0 runner    (1001) docker     (121)        7 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)    28845 2022-09-28 18:33:04.000000 django-formtools-2.4/docs/wizard.rst
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.568193 django-formtools-2.4/formtools/
--rw-r--r--   0 runner    (1001) docker     (121)      319 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      183 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/apps.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.544192 django-formtools-2.4/formtools/locale/af/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.568193 django-formtools-2.4/formtools/locale/af/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1126 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/af/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1769 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/af/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.544192 django-formtools-2.4/formtools/locale/ar/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.568193 django-formtools-2.4/formtools/locale/ar/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1277 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ar/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1962 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ar/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.544192 django-formtools-2.4/formtools/locale/ast/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/ast/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      578 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ast/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1573 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ast/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.544192 django-formtools-2.4/formtools/locale/az/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/az/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1174 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/az/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1814 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/az/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.544192 django-formtools-2.4/formtools/locale/be/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/be/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      710 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/be/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1644 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/be/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.544192 django-formtools-2.4/formtools/locale/bg/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/bg/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1118 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/bg/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1967 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/bg/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.544192 django-formtools-2.4/formtools/locale/br/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/br/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1415 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/br/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2102 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/br/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.548192 django-formtools-2.4/formtools/locale/ca/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/ca/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1179 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ca/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1876 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ca/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.548192 django-formtools-2.4/formtools/locale/cs/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/cs/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1215 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/cs/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1860 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/cs/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.548192 django-formtools-2.4/formtools/locale/cy/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/cy/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      853 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/cy/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1717 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/cy/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.548192 django-formtools-2.4/formtools/locale/da/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/da/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1130 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/da/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1864 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/da/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.548192 django-formtools-2.4/formtools/locale/de/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/de/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1173 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/de/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1829 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/de/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.548192 django-formtools-2.4/formtools/locale/el/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/el/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1321 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/el/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2054 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/el/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.548192 django-formtools-2.4/formtools/locale/en/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/en/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      356 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/en/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1352 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/en/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.548192 django-formtools-2.4/formtools/locale/en_GB/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/en_GB/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      623 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/en_GB/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1642 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/en_GB/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.552193 django-formtools-2.4/formtools/locale/eo/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/eo/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      779 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/eo/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1752 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/eo/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.552193 django-formtools-2.4/formtools/locale/es/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/es/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1145 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/es/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1925 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/es/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.552193 django-formtools-2.4/formtools/locale/es_AR/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.572193 django-formtools-2.4/formtools/locale/es_AR/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1193 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/es_AR/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1859 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/es_AR/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.552193 django-formtools-2.4/formtools/locale/es_MX/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/es_MX/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1149 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/es_MX/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1778 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/es_MX/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.552193 django-formtools-2.4/formtools/locale/et/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/et/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1119 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/et/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1889 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/et/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.552193 django-formtools-2.4/formtools/locale/eu/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/eu/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1142 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/eu/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1794 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/eu/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.552193 django-formtools-2.4/formtools/locale/fa/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/fa/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1216 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/fa/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1963 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/fa/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/fi/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/fi/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1136 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/fi/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1868 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/fi/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/fr/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/fr/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1250 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/fr/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1949 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/fr/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/ga/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/ga/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      658 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ga/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1682 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ga/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/gd/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/gd/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1210 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/gd/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1828 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/gd/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/gl/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/gl/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      608 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/gl/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1612 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/gl/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/he/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/he/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1237 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/he/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1927 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/he/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/hi/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/hi/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      655 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/hi/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1688 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/hi/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/hr/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/hr/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      681 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/hr/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1754 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/hr/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/hu/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.576194 django-formtools-2.4/formtools/locale/hu/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1120 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/hu/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1822 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/hu/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/ia/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/ia/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      611 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ia/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1589 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ia/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.556193 django-formtools-2.4/formtools/locale/id/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/id/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1109 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/id/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1834 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/id/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/io/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/io/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      597 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/io/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1584 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/io/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/is/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/is/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      948 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/is/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1814 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/is/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/it/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/it/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1172 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/it/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1987 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/it/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ja/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/ja/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1195 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ja/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1873 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ja/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ka/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/ka/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      658 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ka/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1673 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ka/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ko/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/ko/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1125 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ko/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1895 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ko/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ky/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/ky/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1341 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ky/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1998 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ky/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/lt/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/lt/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1261 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/lt/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1902 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/lt/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/lv/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.580194 django-formtools-2.4/formtools/locale/lv/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1195 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/lv/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1841 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/lv/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/mk/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/mk/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1121 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/mk/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1988 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/mk/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ml/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/ml/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1715 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ml/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2445 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ml/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/mn/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/mn/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1337 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/mn/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2033 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/mn/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ms/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/ms/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1096 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ms/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1717 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ms/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/nb/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/nb/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1165 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/nb/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1872 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/nb/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ne/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/ne/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      665 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ne/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1650 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ne/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/nl/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/nl/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1144 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/nl/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2007 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/nl/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/nn/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/nn/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      612 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/nn/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1625 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/nn/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/os/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/os/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      646 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/os/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1621 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/os/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/pa/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/pa/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      647 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/pa/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1619 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/pa/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/pl/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/pl/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1289 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/pl/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2134 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/pl/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/pt/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.584194 django-formtools-2.4/formtools/locale/pt/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      827 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/pt/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1716 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/pt/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/pt_BR/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/pt_BR/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1243 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/pt_BR/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2044 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/pt_BR/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ro/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/ro/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1187 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ro/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1952 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ro/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/ru/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/ru/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1511 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ru/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2210 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/ru/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/sk/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/sk/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      640 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sk/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1698 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sk/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.560193 django-formtools-2.4/formtools/locale/sl/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/sl/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      661 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sl/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1677 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sl/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/sq/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/sq/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1211 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sq/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1814 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sq/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/sr/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/sr/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1358 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sr/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2090 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sr/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/sr_Latn/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/sr_Latn/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      701 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sr_Latn/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1719 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sr_Latn/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/sv/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/sv/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1166 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sv/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1885 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sv/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/sw/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/sw/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1173 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sw/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1768 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/sw/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/th/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.588194 django-formtools-2.4/formtools/locale/th/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      707 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/th/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1790 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/th/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/tr/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/locale/tr/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1175 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/tr/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1863 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/tr/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/uk/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/locale/uk/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1544 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/uk/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     2307 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/uk/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/vi/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/locale/vi/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1133 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/vi/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1771 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/vi/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/zh_CN/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/locale/zh_CN/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)     1078 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/zh_CN/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1841 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/zh_CN/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/zh_Hans/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/locale/zh_Hans/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      637 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/zh_Hans/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1695 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/zh_Hans/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/zh_Hant/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/locale/zh_Hant/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      587 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/zh_Hant/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1622 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/zh_Hant/LC_MESSAGES/django.po
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/locale/zh_TW/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/locale/zh_TW/LC_MESSAGES/
--rw-r--r--   0 runner    (1001) docker     (121)      607 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/zh_TW/LC_MESSAGES/django.mo
--rw-r--r--   0 runner    (1001) docker     (121)     1609 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/locale/zh_TW/LC_MESSAGES/django.po
--rw-r--r--   0 runner    (1001) docker     (121)      103 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/models.py
--rw-r--r--   0 runner    (1001) docker     (121)     6251 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/preview.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.564193 django-formtools-2.4/formtools/templates/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/templates/formtools/
--rw-r--r--   0 runner    (1001) docker     (121)      422 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/templates/formtools/form.html
--rw-r--r--   0 runner    (1001) docker     (121)      882 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/templates/formtools/preview.html
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/templates/formtools/wizard/
--rw-r--r--   0 runner    (1001) docker     (121)      672 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/templates/formtools/wizard/wizard_form.html
--rw-r--r--   0 runner    (1001) docker     (121)      922 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.592194 django-formtools-2.4/formtools/wizard/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/wizard/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      299 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/wizard/forms.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.596195 django-formtools-2.4/formtools/wizard/storage/
--rw-r--r--   0 runner    (1001) docker     (121)      471 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/wizard/storage/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     4998 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/wizard/storage/base.py
--rw-r--r--   0 runner    (1001) docker     (121)      806 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/wizard/storage/cookie.py
--rw-r--r--   0 runner    (1001) docker     (121)      175 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/wizard/storage/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (121)      523 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/wizard/storage/session.py
--rw-r--r--   0 runner    (1001) docker     (121)    28897 2022-09-28 18:33:04.000000 django-formtools-2.4/formtools/wizard/views.py
--rw-r--r--   0 runner    (1001) docker     (121)      268 2022-09-28 18:33:18.600195 django-formtools-2.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1847 2022-09-28 18:33:04.000000 django-formtools-2.4/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.596195 django-formtools-2.4/tests/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      544 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/forms.py
--rw-r--r--   0 runner    (1001) docker     (121)       29 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)      912 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/settings.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.596195 django-formtools-2.4/tests/templates/
--rw-r--r--   0 runner    (1001) docker     (121)       11 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/templates/404.html
--rw-r--r--   0 runner    (1001) docker     (121)       35 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/templates/base.html
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.596195 django-formtools-2.4/tests/templates/forms/
--rw-r--r--   0 runner    (1001) docker     (121)      307 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/templates/forms/wizard.html
--rw-r--r--   0 runner    (1001) docker     (121)     8648 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/tests.py
--rw-r--r--   0 runner    (1001) docker     (121)      250 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/urls.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.596195 django-formtools-2.4/tests/wizard/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.600195 django-formtools-2.4/tests/wizard/namedwizardtests/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/namedwizardtests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1715 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/namedwizardtests/forms.py
--rw-r--r--   0 runner    (1001) docker     (121)    16243 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/namedwizardtests/tests.py
--rw-r--r--   0 runner    (1001) docker     (121)      978 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/namedwizardtests/urls.py
--rw-r--r--   0 runner    (1001) docker     (121)     3660 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/storage.py
--rw-r--r--   0 runner    (1001) docker     (121)      577 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/test_basestorage.py
--rw-r--r--   0 runner    (1001) docker     (121)     1640 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/test_cookiestorage.py
--rw-r--r--   0 runner    (1001) docker     (121)    11070 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/test_forms.py
--rw-r--r--   0 runner    (1001) docker     (121)      678 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/test_loadstorage.py
--rw-r--r--   0 runner    (1001) docker     (121)      236 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/test_sessionstorage.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.600195 django-formtools-2.4/tests/wizard/wizardtests/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/wizardtests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     2102 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/wizardtests/forms.py
--rw-r--r--   0 runner    (1001) docker     (121)      430 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/wizardtests/models.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-28 18:33:18.600195 django-formtools-2.4/tests/wizard/wizardtests/templates/
--rw-r--r--   0 runner    (1001) docker     (121)       50 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/wizardtests/templates/other_wizard_form.html
--rw-r--r--   0 runner    (1001) docker     (121)    19183 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/wizardtests/tests.py
--rw-r--r--   0 runner    (1001) docker     (121)      697 2022-09-28 18:33:04.000000 django-formtools-2.4/tests/wizard/wizardtests/urls.py
--rw-r--r--   0 runner    (1001) docker     (121)      633 2022-09-28 18:33:04.000000 django-formtools-2.4/tox.ini
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.502792 django-formtools-2.4.1/
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-13 12:49:41.000000 django-formtools-2.4.1/.coveragerc
+-rw-r--r--   0 runner    (1001) docker     (123)      203 2023-05-13 12:49:41.000000 django-formtools-2.4.1/.editorconfig
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.474792 django-formtools-2.4.1/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 12:49:41.000000 django-formtools-2.4.1/.github/workflows/release.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      765 2023-05-13 12:49:41.000000 django-formtools-2.4.1/.github/workflows/test.yml
+-rw-r--r--   0 runner    (1001) docker     (123)       92 2023-05-13 12:49:41.000000 django-formtools-2.4.1/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 12:49:41.000000 django-formtools-2.4.1/.pre-commit-config.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.474792 django-formtools-2.4.1/.tx/
+-rw-r--r--   0 runner    (1001) docker     (123)      256 2023-05-13 12:49:41.000000 django-formtools-2.4.1/.tx/config
+-rw-r--r--   0 runner    (1001) docker     (123)      819 2023-05-13 12:49:41.000000 django-formtools-2.4.1/AUTHORS.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2375 2023-05-13 12:49:41.000000 django-formtools-2.4.1/CODE_OF_CONDUCT.md
+-rw-r--r--   0 runner    (1001) docker     (123)      338 2023-05-13 12:49:41.000000 django-formtools-2.4.1/CONTRIBUTING.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1562 2023-05-13 12:49:41.000000 django-formtools-2.4.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-13 12:49:41.000000 django-formtools-2.4.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)      665 2023-05-13 12:49:41.000000 django-formtools-2.4.1/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)     3884 2023-05-13 12:49:58.502792 django-formtools-2.4.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2593 2023-05-13 12:49:41.000000 django-formtools-2.4.1/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.474792 django-formtools-2.4.1/django_formtools.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3884 2023-05-13 12:49:58.000000 django-formtools-2.4.1/django_formtools.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8071 2023-05-13 12:49:58.000000 django-formtools-2.4.1/django_formtools.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:49:58.000000 django-formtools-2.4.1/django_formtools.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:49:58.000000 django-formtools-2.4.1/django_formtools.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-13 12:49:58.000000 django-formtools-2.4.1/django_formtools.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 12:49:58.000000 django-formtools-2.4.1/django_formtools.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.474792 django-formtools-2.4.1/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)     6803 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)     2663 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/changelog.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    10698 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/conf.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.474792 django-formtools-2.4.1/docs/extensions/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/extensions/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      153 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/extensions/settings.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2838 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6721 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)     4460 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/preview.rst
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    28857 2023-05-13 12:49:41.000000 django-formtools-2.4.1/docs/wizard.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/
+-rw-r--r--   0 runner    (1001) docker     (123)      319 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      183 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/apps.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/af/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/af/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1126 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/af/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1769 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/af/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/ar/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/ar/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1277 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ar/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1962 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ar/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/ast/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/ast/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      578 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ast/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1573 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ast/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/az/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/az/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1174 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/az/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1814 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/az/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/be/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/be/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      710 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/be/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1644 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/be/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/bg/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/bg/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1118 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/bg/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1967 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/bg/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/br/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/br/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1415 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/br/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2102 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/br/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/ca/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/ca/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1179 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ca/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1876 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ca/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/cs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/cs/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1215 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/cs/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1860 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/cs/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/cy/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/cy/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      853 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/cy/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1717 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/cy/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.458792 django-formtools-2.4.1/formtools/locale/da/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/da/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1130 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/da/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1864 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/da/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/de/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.478792 django-formtools-2.4.1/formtools/locale/de/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/de/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1829 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/de/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/el/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/el/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1321 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/el/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2054 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/el/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/en/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/en/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      356 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/en/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1352 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/en/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/en_GB/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/en_GB/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      623 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/en_GB/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1642 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/en_GB/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/eo/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/eo/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      779 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/eo/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1752 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/eo/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/es/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/es/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1145 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/es/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1925 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/es/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/es_AR/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/es_AR/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1193 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/es_AR/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1859 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/es_AR/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/es_MX/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/es_MX/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/es_MX/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1778 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/es_MX/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/et/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/et/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1119 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/et/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1889 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/et/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/eu/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/eu/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1142 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/eu/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1794 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/eu/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/fa/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/fa/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1216 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/fa/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1963 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/fa/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/fi/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/fi/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1136 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/fi/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1868 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/fi/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/fr/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/fr/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1250 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/fr/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1949 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/fr/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/ga/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/ga/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      658 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ga/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ga/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/gd/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/gd/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1210 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/gd/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/gd/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/gl/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.482792 django-formtools-2.4.1/formtools/locale/gl/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      608 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/gl/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1612 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/gl/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/he/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/he/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1237 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/he/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1927 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/he/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/hi/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/hi/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      655 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/hi/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1688 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/hi/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/hr/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/hr/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      681 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/hr/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1754 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/hr/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/hu/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/hu/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1120 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/hu/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1822 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/hu/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/ia/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/ia/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      611 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ia/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1589 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ia/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/id/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/id/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/id/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1834 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/id/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.462792 django-formtools-2.4.1/formtools/locale/io/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/io/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      597 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/io/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1584 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/io/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/is/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/is/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      948 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/is/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1814 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/is/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/it/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/it/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1172 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/it/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/it/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ja/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/ja/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1195 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ja/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1873 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ja/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ka/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/ka/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      658 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ka/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1673 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ka/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ko/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/ko/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1125 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ko/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1895 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ko/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ky/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/ky/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1341 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ky/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1998 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ky/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/lt/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/lt/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1261 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/lt/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1902 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/lt/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/lv/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/lv/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1195 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/lv/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1841 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/lv/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/mk/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.486792 django-formtools-2.4.1/formtools/locale/mk/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1121 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/mk/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1988 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/mk/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ml/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/ml/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1715 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ml/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2445 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ml/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/mn/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/mn/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1337 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/mn/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2033 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/mn/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ms/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/ms/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1096 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ms/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1717 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ms/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/nb/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/nb/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1165 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/nb/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/nb/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ne/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/ne/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      665 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ne/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1650 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ne/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/nl/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/nl/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1144 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/nl/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2007 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/nl/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/nn/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/nn/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/nn/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1625 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/nn/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/os/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/os/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      646 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/os/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1621 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/os/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/pa/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/pa/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      647 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/pa/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1619 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/pa/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/pl/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/pl/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1289 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/pl/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2134 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/pl/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/pt/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/pt/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      827 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/pt/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1716 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/pt/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/pt_BR/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/pt_BR/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1243 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/pt_BR/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2044 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/pt_BR/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ro/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/ro/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1187 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ro/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1952 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ro/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/ru/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/ru/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1511 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ru/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2210 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/ru/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.466792 django-formtools-2.4.1/formtools/locale/sk/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.490792 django-formtools-2.4.1/formtools/locale/sk/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sk/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1698 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sk/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/sl/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/sl/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      661 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sl/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1677 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sl/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/sq/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/sq/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sq/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1814 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sq/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/sr/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/sr/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1358 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sr/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2090 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sr/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/sr_Latn/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/sr_Latn/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      701 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sr_Latn/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1719 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sr_Latn/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/sv/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/sv/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1166 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sv/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1885 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sv/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/sw/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/sw/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sw/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1768 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/sw/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/th/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/th/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      707 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/th/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1790 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/th/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/tr/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/tr/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1175 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/tr/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1863 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/tr/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/uk/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/uk/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1544 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/uk/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     2307 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/uk/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/vi/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/vi/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/vi/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1771 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/vi/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/zh_CN/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/zh_CN/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)     1078 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/zh_CN/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1841 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/zh_CN/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/zh_Hans/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/zh_Hans/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      637 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/zh_Hans/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1695 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/zh_Hans/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/zh_Hant/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/zh_Hant/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      587 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/zh_Hant/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1622 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/zh_Hant/LC_MESSAGES/django.po
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/locale/zh_TW/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/locale/zh_TW/LC_MESSAGES/
+-rw-r--r--   0 runner    (1001) docker     (123)      607 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/zh_TW/LC_MESSAGES/django.mo
+-rw-r--r--   0 runner    (1001) docker     (123)     1609 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/locale/zh_TW/LC_MESSAGES/django.po
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6251 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/preview.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.470792 django-formtools-2.4.1/formtools/templates/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.494792 django-formtools-2.4.1/formtools/templates/formtools/
+-rw-r--r--   0 runner    (1001) docker     (123)      435 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/templates/formtools/form.html
+-rw-r--r--   0 runner    (1001) docker     (123)      906 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/templates/formtools/preview.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.498792 django-formtools-2.4.1/formtools/templates/formtools/wizard/
+-rw-r--r--   0 runner    (1001) docker     (123)      684 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/templates/formtools/wizard/wizard_form.html
+-rw-r--r--   0 runner    (1001) docker     (123)      922 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.498792 django-formtools-2.4.1/formtools/wizard/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/wizard/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      299 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/wizard/forms.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.498792 django-formtools-2.4.1/formtools/wizard/storage/
+-rw-r--r--   0 runner    (1001) docker     (123)      471 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/wizard/storage/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4998 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/wizard/storage/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      806 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/wizard/storage/cookie.py
+-rw-r--r--   0 runner    (1001) docker     (123)      175 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/wizard/storage/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      523 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/wizard/storage/session.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29202 2023-05-13 12:49:41.000000 django-formtools-2.4.1/formtools/wizard/views.py
+-rw-r--r--   0 runner    (1001) docker     (123)      268 2023-05-13 12:49:58.502792 django-formtools-2.4.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-13 12:49:41.000000 django-formtools-2.4.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.498792 django-formtools-2.4.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      544 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/forms.py
+-rw-r--r--   0 runner    (1001) docker     (123)       42 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      912 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/settings.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.498792 django-formtools-2.4.1/tests/templates/
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/templates/404.html
+-rw-r--r--   0 runner    (1001) docker     (123)       35 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/templates/base.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.498792 django-formtools-2.4.1/tests/templates/forms/
+-rw-r--r--   0 runner    (1001) docker     (123)      307 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/templates/forms/wizard.html
+-rw-r--r--   0 runner    (1001) docker     (123)     8648 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/tests.py
+-rw-r--r--   0 runner    (1001) docker     (123)      250 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/urls.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.498792 django-formtools-2.4.1/tests/wizard/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.498792 django-formtools-2.4.1/tests/wizard/namedwizardtests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/namedwizardtests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1715 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/namedwizardtests/forms.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16243 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/namedwizardtests/tests.py
+-rw-r--r--   0 runner    (1001) docker     (123)      978 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/namedwizardtests/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3660 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/storage.py
+-rw-r--r--   0 runner    (1001) docker     (123)      577 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/test_basestorage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1640 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/test_cookiestorage.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11856 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/test_forms.py
+-rw-r--r--   0 runner    (1001) docker     (123)      678 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/test_loadstorage.py
+-rw-r--r--   0 runner    (1001) docker     (123)      236 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/test_sessionstorage.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.502792 django-formtools-2.4.1/tests/wizard/wizardtests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/wizardtests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2102 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/wizardtests/forms.py
+-rw-r--r--   0 runner    (1001) docker     (123)      430 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/wizardtests/models.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:49:58.502792 django-formtools-2.4.1/tests/wizard/wizardtests/templates/
+-rw-r--r--   0 runner    (1001) docker     (123)       50 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/wizardtests/templates/other_wizard_form.html
+-rw-r--r--   0 runner    (1001) docker     (123)    19183 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/wizardtests/tests.py
+-rw-r--r--   0 runner    (1001) docker     (123)      697 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tests/wizard/wizardtests/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)      644 2023-05-13 12:49:41.000000 django-formtools-2.4.1/tox.ini
```

### Comparing `django-formtools-2.4/.github/workflows/release.yml` & `django-formtools-2.4.1/.github/workflows/release.yml`

 * *Files 2% similar despite different names*

```diff
@@ -7,20 +7,20 @@
 
 jobs:
   build:
     if: github.repository == 'jazzband/django-formtools'
     runs-on: ubuntu-latest
 
     steps:
-      - uses: actions/checkout@v2
+      - uses: actions/checkout@v3
         with:
           fetch-depth: 0
 
       - name: Set up Python
-        uses: actions/setup-python@v2
+        uses: actions/setup-python@v3
         with:
           python-version: 3.8
 
       - name: Install dependencies
         run: |
           python -m pip install -U pip
           python -m pip install -U setuptools twine wheel
```

### Comparing `django-formtools-2.4/.github/workflows/test.yml` & `django-formtools-2.4.1/.github/workflows/test.yml`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 jobs:
   build:
     runs-on: ubuntu-latest
     strategy:
       fail-fast: false
       max-parallel: 5
       matrix:
-        python-version: ['3.6', '3.7', '3.8', '3.9', '3.10']
+        python-version: ['3.7', '3.8', '3.9', '3.10', '3.11']
 
     steps:
     - uses: actions/checkout@v3
 
     - name: Set up Python ${{ matrix.python-version }}
       uses: actions/setup-python@v4
       with:
```

### Comparing `django-formtools-2.4/AUTHORS.rst` & `django-formtools-2.4.1/AUTHORS.rst`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/CODE_OF_CONDUCT.md` & `django-formtools-2.4.1/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/LICENSE` & `django-formtools-2.4.1/LICENSE`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/Makefile` & `django-formtools-2.4.1/Makefile`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/PKG-INFO` & `django-formtools-2.4.1/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,36 +1,36 @@
 Metadata-Version: 2.1
 Name: django-formtools
-Version: 2.4
+Version: 2.4.1
 Summary: A set of high-level abstractions for Django forms
 Home-page: https://django-formtools.readthedocs.io/en/latest/
 Author: Django Software Foundation
 Author-email: foundation@djangoproject.com
 License: BSD
 Project-URL: Source, https://github.com/jazzband/django-formtools
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Web Environment
 Classifier: Framework :: Django
-Classifier: Framework :: Django :: 2.2
 Classifier: Framework :: Django :: 3.2
 Classifier: Framework :: Django :: 4.0
 Classifier: Framework :: Django :: 4.1
+Classifier: Framework :: Django :: 4.2
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Internet :: WWW/HTTP
-Requires-Python: >=3.6
+Requires-Python: >=3.7
 Description-Content-Type: text/x-rst
 License-File: LICENSE
 
 ================
 django-formtools
 ================
 
@@ -93,23 +93,23 @@
 
 The previous command will run the tests in different combinations of Python
 (if available) and Django versions. To see the full list of combinations use
 the ``-l`` option::
 
     $ tox -l
     ...
-    py38-django-AB
-    py38-django-master
+    py310-djangoAB
+    py310-djangomain
 
 You can run each environment with the ``-e`` option::
 
-    $ tox -e py38-django-AB  # runs the tests only on Python 3.5 and Django A.B.x
+    $ tox -e py310-djangoAB  # runs the tests only on Python 3.10 and Django A.B.x
 
 Optionally you can also specify a country whose tests you want to run::
 
     $ COUNTRY=us tox
 
 And combine both options::
 
-    $ COUNTRY=us tox -e py38-django-AB
+    $ COUNTRY=us tox -e py310-djangoAB
 
 __ https://tox.readthedocs.io/en/latest/install.html
```

### Comparing `django-formtools-2.4/README.rst` & `django-formtools-2.4.1/README.rst`

 * *Files 4% similar despite different names*

```diff
@@ -61,23 +61,23 @@
 
 The previous command will run the tests in different combinations of Python
 (if available) and Django versions. To see the full list of combinations use
 the ``-l`` option::
 
     $ tox -l
     ...
-    py38-django-AB
-    py38-django-master
+    py310-djangoAB
+    py310-djangomain
 
 You can run each environment with the ``-e`` option::
 
-    $ tox -e py38-django-AB  # runs the tests only on Python 3.5 and Django A.B.x
+    $ tox -e py310-djangoAB  # runs the tests only on Python 3.10 and Django A.B.x
 
 Optionally you can also specify a country whose tests you want to run::
 
     $ COUNTRY=us tox
 
 And combine both options::
 
-    $ COUNTRY=us tox -e py38-django-AB
+    $ COUNTRY=us tox -e py310-djangoAB
 
 __ https://tox.readthedocs.io/en/latest/install.html
```

### Comparing `django-formtools-2.4/django_formtools.egg-info/PKG-INFO` & `django-formtools-2.4.1/django_formtools.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,36 +1,36 @@
 Metadata-Version: 2.1
 Name: django-formtools
-Version: 2.4
+Version: 2.4.1
 Summary: A set of high-level abstractions for Django forms
 Home-page: https://django-formtools.readthedocs.io/en/latest/
 Author: Django Software Foundation
 Author-email: foundation@djangoproject.com
 License: BSD
 Project-URL: Source, https://github.com/jazzband/django-formtools
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Web Environment
 Classifier: Framework :: Django
-Classifier: Framework :: Django :: 2.2
 Classifier: Framework :: Django :: 3.2
 Classifier: Framework :: Django :: 4.0
 Classifier: Framework :: Django :: 4.1
+Classifier: Framework :: Django :: 4.2
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Internet :: WWW/HTTP
-Requires-Python: >=3.6
+Requires-Python: >=3.7
 Description-Content-Type: text/x-rst
 License-File: LICENSE
 
 ================
 django-formtools
 ================
 
@@ -93,23 +93,23 @@
 
 The previous command will run the tests in different combinations of Python
 (if available) and Django versions. To see the full list of combinations use
 the ``-l`` option::
 
     $ tox -l
     ...
-    py38-django-AB
-    py38-django-master
+    py310-djangoAB
+    py310-djangomain
 
 You can run each environment with the ``-e`` option::
 
-    $ tox -e py38-django-AB  # runs the tests only on Python 3.5 and Django A.B.x
+    $ tox -e py310-djangoAB  # runs the tests only on Python 3.10 and Django A.B.x
 
 Optionally you can also specify a country whose tests you want to run::
 
     $ COUNTRY=us tox
 
 And combine both options::
 
-    $ COUNTRY=us tox -e py38-django-AB
+    $ COUNTRY=us tox -e py310-djangoAB
 
 __ https://tox.readthedocs.io/en/latest/install.html
```

### Comparing `django-formtools-2.4/django_formtools.egg-info/SOURCES.txt` & `django-formtools-2.4.1/django_formtools.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/docs/Makefile` & `django-formtools-2.4.1/docs/Makefile`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 SPHINXOPTS    =
 SPHINXBUILD   = sphinx-build
 PAPER         =
 BUILDDIR      = _build
 
 # User-friendly check for sphinx-build
 ifeq ($(shell which $(SPHINXBUILD) >/dev/null 2>&1; echo $$?), 1)
-$(error The '$(SPHINXBUILD)' command was not found. Make sure you have Sphinx installed, then set the SPHINXBUILD environment variable to point to the full path of the '$(SPHINXBUILD)' executable. Alternatively you can add the directory with the executable to your PATH. If you don't have Sphinx installed, grab it from http://sphinx-doc.org/)
+$(error The '$(SPHINXBUILD)' command was not found. Make sure you have Sphinx installed, then set the SPHINXBUILD environment variable to point to the full path of the '$(SPHINXBUILD)' executable. Alternatively you can add the directory with the executable to your PATH. If you don't have Sphinx installed, grab it from https://sphinx-doc.org/)
 endif
 
 # Internal variables.
 PAPEROPT_a4     = -D latex_paper_size=a4
 PAPEROPT_letter = -D latex_paper_size=letter
 ALLSPHINXOPTS   = -d $(BUILDDIR)/doctrees $(PAPEROPT_$(PAPER)) $(SPHINXOPTS) .
 # the i18n builder cannot share the environment and doctrees with the others
```

### Comparing `django-formtools-2.4/docs/changelog.rst` & `django-formtools-2.4.1/docs/changelog.rst`

 * *Files 7% similar despite different names*

```diff
@@ -1,12 +1,22 @@
 Changelog
 =========
 
 This page details the changes in the various ``django-formtools`` releases.
 
+2.4.1 (2023-05-13)
+------------------
+
+- Fixed a regression causing a recursion error when getting ``get_form_list()``
+  from a form condition (#220).
+
+- Removed Python 3.6 support and added Python 3.11 to test matrix.
+
+- Dropped testing for Django < 3.2 and confirmed support for Django 4.2.
+
 2.4 (2022-09-28)
 ----------------
 
 - Updated translations from Transifex.
 
 - Any kwarg passed to ``render_goto_step()`` is passed over to ``render``.
```

### Comparing `django-formtools-2.4/docs/conf.py` & `django-formtools-2.4.1/docs/conf.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/docs/index.rst` & `django-formtools-2.4.1/docs/index.rst`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/docs/make.bat` & `django-formtools-2.4.1/docs/make.bat`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/docs/preview.rst` & `django-formtools-2.4.1/docs/preview.rst`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/docs/wizard.rst` & `django-formtools-2.4.1/docs/wizard.rst`

 * *Files 0% similar despite different names*

```diff
@@ -222,18 +222,18 @@
             {{ form.as_table }}
         {% endfor %}
     {% else %}
         {{ wizard.form }}
     {% endif %}
     </table>
     {% if wizard.steps.prev %}
-    <button name="wizard_goto_step" type="submit" value="{{ wizard.steps.first }}">{% trans "first step" %}</button>
-    <button name="wizard_goto_step" type="submit" value="{{ wizard.steps.prev }}">{% trans "prev step" %}</button>
+    <button name="wizard_goto_step" type="submit" value="{{ wizard.steps.first }}">{% translate "first step" %}</button>
+    <button name="wizard_goto_step" type="submit" value="{{ wizard.steps.prev }}">{% translate "prev step" %}</button>
     {% endif %}
-    <input type="submit" value="{% trans "submit" %}"/>
+    <input type="submit" value="{% translate "submit" %}"/>
     </form>
     {% endblock %}
 
 .. note::
 
     Note that ``{{ wizard.management_form }}`` **must be used** for
     the wizard to work properly.
```

### Comparing `django-formtools-2.4/formtools/locale/af/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/af/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/af/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/af/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ar/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ar/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ar/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ar/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ast/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ast/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ast/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ast/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/az/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/az/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/az/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/az/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/be/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/be/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/be/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/be/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/bg/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/bg/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/bg/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/bg/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/br/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/br/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/br/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/br/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ca/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ca/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ca/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ca/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/cs/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/cs/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/cs/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/cs/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/cy/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/cy/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/cy/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/cy/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/da/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/da/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/da/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/da/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/de/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/de/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/de/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/de/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/el/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/el/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/el/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/el/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/en/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/en/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/en_GB/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/en_GB/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/en_GB/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/en_GB/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/eo/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/eo/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/eo/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/eo/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/es/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/es/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/es/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/es/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/es_AR/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/es_AR/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/es_AR/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/es_AR/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/es_MX/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/es_MX/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/es_MX/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/es_MX/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/et/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/et/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/et/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/et/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/eu/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/eu/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/eu/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/eu/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/fa/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/fa/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/fa/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/fa/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/fi/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/fi/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/fi/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/fi/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/fr/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/fr/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/fr/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/fr/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ga/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ga/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ga/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ga/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/gd/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/gd/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/gd/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/gd/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/gl/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/gl/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/gl/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/gl/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/he/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/he/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/he/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/he/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/hi/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/hi/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/hi/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/hi/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/hr/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/hr/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/hr/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/hr/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/hu/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/hu/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/hu/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/hu/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ia/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ia/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ia/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ia/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/id/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/id/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/id/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/id/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/io/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/io/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/io/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/io/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/is/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/is/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/is/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/is/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/it/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/it/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/it/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/it/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ja/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ja/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ja/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ja/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ka/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ka/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ka/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ka/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ko/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ko/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ko/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ko/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ky/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ky/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ky/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ky/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/lt/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/lt/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/lt/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/lt/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/lv/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/lv/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/lv/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/lv/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/mk/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/mk/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/mk/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/mk/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ml/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ml/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ml/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ml/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/mn/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/mn/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/mn/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/mn/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ms/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ms/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ms/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ms/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/nb/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/nb/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/nb/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/nb/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ne/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ne/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ne/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ne/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/nl/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/nl/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/nl/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/nl/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/nn/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/nn/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/nn/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/nn/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/os/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/os/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/os/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/os/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/pa/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/pa/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/pa/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/pa/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/pl/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/pl/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/pl/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/pl/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/pt/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/pt/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/pt/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/pt/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/pt_BR/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/pt_BR/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/pt_BR/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/pt_BR/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ro/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ro/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ro/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ro/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ru/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/ru/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/ru/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/ru/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sk/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/sk/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sk/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/sk/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sl/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/sl/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sl/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/sl/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sq/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/sq/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sq/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/sq/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sr/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/sr/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sr/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/sr/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sr_Latn/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/sr_Latn/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sr_Latn/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/sr_Latn/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sv/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/sv/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sv/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/sv/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sw/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/sw/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/sw/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/sw/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/th/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/th/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/th/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/th/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/tr/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/tr/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/tr/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/tr/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/uk/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/uk/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/uk/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/uk/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/vi/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/vi/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/vi/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/vi/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/zh_CN/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/zh_CN/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/zh_CN/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/zh_CN/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/zh_Hans/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/zh_Hans/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/zh_Hans/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/zh_Hans/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/zh_Hant/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/zh_Hant/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/zh_Hant/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/zh_Hant/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/zh_TW/LC_MESSAGES/django.mo` & `django-formtools-2.4.1/formtools/locale/zh_TW/LC_MESSAGES/django.mo`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/locale/zh_TW/LC_MESSAGES/django.po` & `django-formtools-2.4.1/formtools/locale/zh_TW/LC_MESSAGES/django.po`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/preview.py` & `django-formtools-2.4.1/formtools/preview.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/templates/formtools/preview.html` & `django-formtools-2.4.1/formtools/templates/formtools/preview.html`

 * *Files 22% similar despite different names*

```diff
@@ -1,37 +1,37 @@
 {% extends "base.html" %}
 {% load i18n %}
 
 {% block content %}
 
-<h1>{% trans "Preview your submission" %}</h1>
+<h1>{% translate "Preview your submission" %}</h1>
 
 <table>
 {% for field in form %}
 <tr>
 <th>{{ field.label }}:</th>
 <td>{{ field.data }}</td>
 </tr>
 {% endfor %}
 </table>
 
-<p>{% blocktrans %}Security hash: {{ hash_value }}{% endblocktrans %}</p>
+<p>{% blocktranslate %}Security hash: {{ hash_value }}{% endblocktranslate %}</p>
 
 <form action="" method="post">{% csrf_token %}
 {% for field in form %}{{ field.as_hidden }}
 {% endfor %}
 <input type="hidden" name="{{ stage_field }}" value="2" />
 <input type="hidden" name="{{ hash_field }}" value="{{ hash_value }}" />
-<p><input type="submit" value="{% trans "Submit" %}" /></p>
+<p><input type="submit" value="{% translate "Submit" %}" /></p>
 </form>
 
-<h1>{% trans "Or edit it again" %}</h1>
+<h1>{% translate "Or edit it again" %}</h1>
 
 <form action="" method="post">{% csrf_token %}
 <table>
 {{ form.as_table }}
 </table>
 <input type="hidden" name="{{ stage_field }}" value="1" />
-<p><input type="submit" value="{% trans "Preview" %}" /></p>
+<p><input type="submit" value="{% translate "Preview" %}" /></p>
 </form>
 
 {% endblock %}
```

#### html2text {}

```diff
@@ -1,10 +1,10 @@
 {% extends "base.html" %} {% load i18n %} {% block content %}
-****** {% trans "Preview your submission" %} ******
+****** {% translate "Preview your submission" %} ******
 {{ field.label }}: {{ field.data }}
-{% blocktrans %}Security hash: {{ hash_value }}{% endblocktrans %}
+{% blocktranslate %}Security hash: {{ hash_value }}{% endblocktranslate %}
 {% csrf_token %} {% for field in form %}{{ field.as_hidden }} {% endfor %}
  %}" />
-****** {% trans "Or edit it again" %} ******
+****** {% translate "Or edit it again" %} ******
 {% csrf_token %}
  %}" />
 {% endblock %}
```

### Comparing `django-formtools-2.4/formtools/utils.py` & `django-formtools-2.4.1/formtools/utils.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/wizard/storage/base.py` & `django-formtools-2.4.1/formtools/wizard/storage/base.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/wizard/storage/cookie.py` & `django-formtools-2.4.1/formtools/wizard/storage/cookie.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/wizard/storage/session.py` & `django-formtools-2.4.1/formtools/wizard/storage/session.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/formtools/wizard/views.py` & `django-formtools-2.4.1/formtools/wizard/views.py`

 * *Files 2% similar despite different names*

```diff
@@ -209,23 +209,29 @@
         and respect the result. (True means add the form, False means ignore
         the form)
 
         The form_list is always generated on the fly because condition methods
         could use data from other (maybe previous forms).
         """
         form_list = OrderedDict()
+        if getattr(self, '_check_cond_started', False):
+            # Guard against infinite recursion, in the case a get_form_list is
+            # called in the context of a condition() call.
+            return self.form_list
+        self._check_cond_started = True
         for form_key, form_class in self.form_list.items():
             # try to fetch the value from condition list, by default, the form
             # gets passed to the new list.
             condition = self.condition_dict.get(form_key, True)
             if callable(condition):
                 # call the value if needed, passes the current instance.
                 condition = condition(self)
             if condition:
                 form_list[form_key] = form_class
+        del self._check_cond_started
         return form_list
 
     def dispatch(self, request, *args, **kwargs):
         """
         This method gets called by the routing engine. The first argument is
         `request` which contains a `HttpRequest` instance.
         The request is stored in `self.request` for later use. The storage
```

### Comparing `django-formtools-2.4/setup.py` & `django-formtools-2.4.1/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -20,32 +20,32 @@
     description="A set of high-level abstractions for Django forms",
     long_description=read("README.rst"),
     long_description_content_type="text/x-rst",
     author="Django Software Foundation",
     author_email="foundation@djangoproject.com",
     packages=find_packages(exclude=["tests", "tests.*"]),
     include_package_data=True,
-    install_requires=["Django>=2.2"],
-    python_requires=">=3.6",
+    install_requires=["Django>=3.2"],
+    python_requires=">=3.7",
     classifiers=[
         "Development Status :: 5 - Production/Stable",
         "Environment :: Web Environment",
         "Framework :: Django",
-        "Framework :: Django :: 2.2",
         "Framework :: Django :: 3.2",
         "Framework :: Django :: 4.0",
         "Framework :: Django :: 4.1",
+        "Framework :: Django :: 4.2",
         "Intended Audience :: Developers",
         "License :: OSI Approved :: BSD License",
         "Operating System :: OS Independent",
         "Programming Language :: Python",
         "Programming Language :: Python :: 3",
         "Programming Language :: Python :: 3 :: Only",
-        "Programming Language :: Python :: 3.6",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
         "Programming Language :: Python :: 3.9",
         "Programming Language :: Python :: 3.10",
+        "Programming Language :: Python :: 3.11",
         "Topic :: Internet :: WWW/HTTP",
     ],
     zip_safe=False,
 )
```

### Comparing `django-formtools-2.4/tests/forms.py` & `django-formtools-2.4.1/tests/forms.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/settings.py` & `django-formtools-2.4.1/tests/settings.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/tests.py` & `django-formtools-2.4.1/tests/tests.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/namedwizardtests/forms.py` & `django-formtools-2.4.1/tests/wizard/namedwizardtests/forms.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/namedwizardtests/tests.py` & `django-formtools-2.4.1/tests/wizard/namedwizardtests/tests.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/namedwizardtests/urls.py` & `django-formtools-2.4.1/tests/wizard/namedwizardtests/urls.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/storage.py` & `django-formtools-2.4.1/tests/wizard/storage.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/test_basestorage.py` & `django-formtools-2.4.1/tests/wizard/test_basestorage.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/test_cookiestorage.py` & `django-formtools-2.4.1/tests/wizard/test_cookiestorage.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/test_forms.py` & `django-formtools-2.4.1/tests/wizard/test_forms.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+import sys
 from importlib import import_module
 
 from django import forms, http
 from django.conf import settings
 from django.contrib.auth.models import User
 from django.db import models
 from django.template.response import TemplateResponse
@@ -154,14 +155,34 @@
 
         testform = TestWizardWithInitAttrs.as_view(
             [('start', Step1), ('step2', Step2), ('step3', Step3)]
         )
         response, instance = testform(request)
         self.assertEqual(instance.get_next_step(), 'step2')
 
+    def test_form_condition_avoid_recursion(self):
+        def subsequent_step_check(wizard):
+            data = wizard.get_cleaned_data_for_step('step3') or {}
+            return data.get('foo')
+
+        testform = TestWizard.as_view(
+            [('start', Step1), ('step2', Step2), ('step3', Step3)],
+            condition_dict={'step3': subsequent_step_check}
+        )
+        request = get_request()
+        old_limit = sys.getrecursionlimit()
+        sys.setrecursionlimit(80)
+        try:
+            response, instance = testform(request)
+            self.assertEqual(instance.get_next_step(), 'step2')
+        except RecursionError:
+            self.fail("RecursionError happened during wizard test.")
+        finally:
+            sys.setrecursionlimit(old_limit)
+
     def test_form_condition_unstable(self):
         request = get_request()
         testform = TestWizard.as_view(
             [('start', Step1), ('step2', Step2), ('step3', Step3)],
             condition_dict={'step2': True}
         )
         response, instance = testform(request)
```

### Comparing `django-formtools-2.4/tests/wizard/test_loadstorage.py` & `django-formtools-2.4.1/tests/wizard/test_loadstorage.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/wizardtests/forms.py` & `django-formtools-2.4.1/tests/wizard/wizardtests/forms.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/wizardtests/tests.py` & `django-formtools-2.4.1/tests/wizard/wizardtests/tests.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tests/wizard/wizardtests/urls.py` & `django-formtools-2.4.1/tests/wizard/wizardtests/urls.py`

 * *Files identical despite different names*

### Comparing `django-formtools-2.4/tox.ini` & `django-formtools-2.4.1/tox.ini`

 * *Files 24% similar despite different names*

```diff
@@ -1,31 +1,31 @@
 [tox]
 args_are_paths = false
 envlist =
-    py{36,37,38,39}-django22
-    py{36,37,38,39,310}-django32
-    py{38,39,310}-django{40,41,main}
+    py{37,38,39,310,311}-django32
+    py{38,39,310,311}-django{40,41,42}
+    py{310,311}-djangomain
 
 [testenv]
 usedevelop = true
 allowlist_externals = make
 commands = make test
 pip_pre = true
 deps =
-    django22: Django>=2.2,<3.0
     django32: Django>=3.2,<4.0
     django40: Django>=4.0,<4.1
     django41: Django>=4.1,<4.2
+    django42: Django>=4.2,<5.0
     djangomain: https://github.com/django/django/archive/main.tar.gz
     -r{toxinidir}/tests/requirements.txt
 ignore_outcome =
-    djmain: True
+    djangomain: True
 ignore_errors =
-    djmain: True
+    djangomain: True
 
 [gh-actions]
 python =
-    3.6: py36
     3.7: py37
     3.8: py38
     3.9: py39
     3.10: py310
+    3.11: py311
```

