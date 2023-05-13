# Comparing `tmp/itzma-lint-0.1.1.tar.gz` & `tmp/itzma-lint-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "itzma-lint-0.1.1.tar", last modified: Fri May 12 01:27:17 2023, max compression
+gzip compressed data, was "itzma-lint-0.1.2.tar", last modified: Sat May 13 01:22:39 2023, max compression
```

## Comparing `itzma-lint-0.1.1.tar` & `itzma-lint-0.1.2.tar`

### file list

```diff
@@ -1,41 +1,105 @@
-drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-12 01:27:17.044339 itzma-lint-0.1.1/
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      288 2023-05-12 01:18:38.000000 itzma-lint-0.1.1/.bumpversion.cfg
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      112 2023-05-11 19:14:59.000000 itzma-lint-0.1.1/.flake8
-drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-12 01:27:17.041325 itzma-lint-0.1.1/.github/
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      117 2023-05-11 21:36:04.000000 itzma-lint-0.1.1/.github/dependabot.yml
-drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-12 01:27:17.041529 itzma-lint-0.1.1/.github/workflows/
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      787 2023-05-11 21:36:04.000000 itzma-lint-0.1.1/.github/workflows/test.yml
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     1814 2023-05-11 19:14:59.000000 itzma-lint-0.1.1/.gitignore
--rw-r--r--   0 tchitrakorn   (501) staff       (20)    21108 2023-05-11 21:36:04.000000 itzma-lint-0.1.1/.pylintrc
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     2130 2023-05-12 01:18:38.000000 itzma-lint-0.1.1/CONTRIBUTING.md
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     1074 2023-04-08 18:39:48.000000 itzma-lint-0.1.1/LICENSE
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      204 2023-05-11 21:36:04.000000 itzma-lint-0.1.1/MANIFEST.in
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     2164 2023-05-11 21:36:04.000000 itzma-lint-0.1.1/Makefile
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     3941 2023-05-12 01:27:17.044203 itzma-lint-0.1.1/PKG-INFO
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     2017 2023-05-12 01:18:38.000000 itzma-lint-0.1.1/README.md
--rw-r--r--   0 tchitrakorn   (501) staff       (20)        0 2023-05-11 19:14:59.000000 itzma-lint-0.1.1/__init__.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     1709 2023-05-12 01:18:38.000000 itzma-lint-0.1.1/pyproject.toml
--rw-r--r--   0 tchitrakorn   (501) staff       (20)       36 2023-05-11 21:36:04.000000 itzma-lint-0.1.1/requirements.txt
--rw-r--r--   0 tchitrakorn   (501) staff       (20)       38 2023-05-12 01:27:17.044379 itzma-lint-0.1.1/setup.cfg
--rw-r--r--   0 tchitrakorn   (501) staff       (20)       38 2023-05-11 21:36:04.000000 itzma-lint-0.1.1/setup.py
-drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-12 01:27:17.042346 itzma-lint-0.1.1/src/
--rw-r--r--   0 tchitrakorn   (501) staff       (20)       21 2023-05-12 01:18:38.000000 itzma-lint-0.1.1/src/_version.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     4150 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/checks.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     1092 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/flake8_itzma.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      134 2023-05-11 18:25:01.000000 itzma-lint-0.1.1/src/helpers.py
-drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-12 01:27:17.043019 itzma-lint-0.1.1/src/itzma_lint.egg-info/
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     3941 2023-05-12 01:27:17.000000 itzma-lint-0.1.1/src/itzma_lint.egg-info/PKG-INFO
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      685 2023-05-12 01:27:17.000000 itzma-lint-0.1.1/src/itzma_lint.egg-info/SOURCES.txt
--rw-r--r--   0 tchitrakorn   (501) staff       (20)        1 2023-05-12 01:27:17.000000 itzma-lint-0.1.1/src/itzma_lint.egg-info/dependency_links.txt
--rw-r--r--   0 tchitrakorn   (501) staff       (20)       96 2023-05-12 01:27:17.000000 itzma-lint-0.1.1/src/itzma_lint.egg-info/requires.txt
--rw-r--r--   0 tchitrakorn   (501) staff       (20)       58 2023-05-12 01:27:17.000000 itzma-lint-0.1.1/src/itzma_lint.egg-info/top_level.txt
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     2480 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/testing_checks.py
-drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-12 01:27:17.043240 itzma-lint-0.1.1/src/tests/
--rw-r--r--   0 tchitrakorn   (501) staff       (20)        0 2023-05-11 21:36:04.000000 itzma-lint-0.1.1/src/tests/__init__.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)     4101 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/tests/test_itzma.py
-drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-12 01:27:17.043948 itzma-lint-0.1.1/src/tests/test_samples/
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      145 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/tests/test_samples/test1.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      426 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/tests/test_samples/test2.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      136 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/tests/test_samples/test3.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      165 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/tests/test_samples/test4.py
--rw-r--r--   0 tchitrakorn   (501) staff       (20)      127 2023-05-11 19:15:00.000000 itzma-lint-0.1.1/src/tests/test_samples/test5.py
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.979713 itzma-lint-0.1.2/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      288 2023-05-13 01:16:40.000000 itzma-lint-0.1.2/.bumpversion.cfg
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      132 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/.flake8
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.950232 itzma-lint-0.1.2/.github/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      117 2023-05-11 21:36:04.000000 itzma-lint-0.1.2/.github/dependabot.yml
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.950481 itzma-lint-0.1.2/.github/workflows/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      787 2023-05-11 21:36:04.000000 itzma-lint-0.1.2/.github/workflows/test.yml
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     1814 2023-05-11 19:14:59.000000 itzma-lint-0.1.2/.gitignore
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    21106 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/.pylintrc
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     2130 2023-05-12 01:18:38.000000 itzma-lint-0.1.2/CONTRIBUTING.md
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     1074 2023-04-08 18:39:48.000000 itzma-lint-0.1.2/LICENSE
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      245 2023-05-13 00:54:40.000000 itzma-lint-0.1.2/MANIFEST.in
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     2164 2023-05-11 21:36:04.000000 itzma-lint-0.1.2/Makefile
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     4129 2023-05-13 01:22:39.979565 itzma-lint-0.1.2/PKG-INFO
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     2205 2023-05-13 00:54:40.000000 itzma-lint-0.1.2/README.md
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)        0 2023-05-11 19:14:59.000000 itzma-lint-0.1.2/__init__.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     1736 2023-05-13 00:54:40.000000 itzma-lint-0.1.2/coverage.json
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.950635 itzma-lint-0.1.2/docs/
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.946575 itzma-lint-0.1.2/docs/build/
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.951196 itzma-lint-0.1.2/docs/build/doctrees/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    18705 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/doctrees/environment.pickle
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    76589 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/doctrees/index.doctree
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.952909 itzma-lint-0.1.2/docs/build/html/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      230 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/.buildinfo
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.953067 itzma-lint-0.1.2/docs/build/html/_sources/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     1204 2023-05-13 00:37:54.000000 itzma-lint-0.1.2/docs/build/html/_sources/index.rst.txt
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.958107 itzma-lint-0.1.2/docs/build/html/_static/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     4418 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/_sphinx_javascript_frameworks_compat.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    11185 2023-05-12 03:35:11.000000 itzma-lint-0.1.2/docs/build/html/_static/alabaster.css
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    15228 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/_static/basic.css
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.958553 itzma-lint-0.1.2/docs/build/html/_static/css/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     3229 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/badge_only.css
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.974326 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    87624 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/Roboto-Slab-Bold.woff
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    67312 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/Roboto-Slab-Bold.woff2
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    86288 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/Roboto-Slab-Regular.woff
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    66444 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/Roboto-Slab-Regular.woff2
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   165742 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/fontawesome-webfont.eot
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   444379 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/fontawesome-webfont.svg
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   165548 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/fontawesome-webfont.ttf
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    98024 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/fontawesome-webfont.woff
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    77160 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/fontawesome-webfont.woff2
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   323344 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/lato-bold-italic.woff
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   193308 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/lato-bold-italic.woff2
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   309728 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/lato-bold.woff
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   184912 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/lato-bold.woff2
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   328412 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/lato-normal-italic.woff
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   195704 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/lato-normal-italic.woff2
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   309192 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/lato-normal.woff
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   182708 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/fonts/lato-normal.woff2
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   135235 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/css/theme.css
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       42 2021-01-29 11:59:09.000000 itzma-lint-0.1.2/docs/build/html/_static/custom.css
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     8171 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/doctools.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      421 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/_static/documentation_options.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      286 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/file.png
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)   288580 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/jquery-3.6.0.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    89501 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/jquery.js
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.975761 itzma-lint-0.1.2/docs/build/html/_static/js/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      934 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/js/badge_only.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     4370 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/js/html5shiv-printshiv.min.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     2734 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/js/html5shiv.min.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     5023 2023-05-12 03:39:49.000000 itzma-lint-0.1.2/docs/build/html/_static/js/theme.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     4758 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/_static/language_data.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       90 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/minus.png
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       90 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/plus.png
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     4819 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/_static/pygments.css
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    17088 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/searchtools.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    68420 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/underscore-1.13.1.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    19530 2022-07-14 07:38:21.000000 itzma-lint-0.1.2/docs/build/html/_static/underscore.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     6874 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/genindex.html
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    21939 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/index.html
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      446 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/objects.inv
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     3803 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/py-modindex.html
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     3664 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/search.html
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     4079 2023-05-13 01:03:10.000000 itzma-lint-0.1.2/docs/build/html/searchindex.js
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)    25480 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/docs/index.html
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.976263 itzma-lint-0.1.2/docs/source/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     2525 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/docs/source/conf.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     1204 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/docs/source/index.rst
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     1709 2023-05-13 01:16:40.000000 itzma-lint-0.1.2/pyproject.toml
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       36 2023-05-11 21:36:04.000000 itzma-lint-0.1.2/requirements.txt
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       38 2023-05-13 01:22:39.979755 itzma-lint-0.1.2/setup.cfg
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       38 2023-05-11 21:36:04.000000 itzma-lint-0.1.2/setup.py
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.977389 itzma-lint-0.1.2/src/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 00:54:40.000000 itzma-lint-0.1.2/src/__init__.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       22 2023-05-13 01:19:43.000000 itzma-lint-0.1.2/src/_version.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     7659 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/src/checks.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     1687 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/src/flake8_itzma.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     1115 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/src/helpers.py
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.978046 itzma-lint-0.1.2/src/itzma_lint.egg-info/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     4129 2023-05-13 01:22:39.000000 itzma-lint-0.1.2/src/itzma_lint.egg-info/PKG-INFO
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     2932 2023-05-13 01:22:39.000000 itzma-lint-0.1.2/src/itzma_lint.egg-info/SOURCES.txt
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)        1 2023-05-13 01:22:39.000000 itzma-lint-0.1.2/src/itzma_lint.egg-info/dependency_links.txt
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       96 2023-05-13 01:22:39.000000 itzma-lint-0.1.2/src/itzma_lint.egg-info/requires.txt
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)       67 2023-05-13 01:22:39.000000 itzma-lint-0.1.2/src/itzma_lint.egg-info/top_level.txt
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     2286 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/src/testing_checks.py
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.978273 itzma-lint-0.1.2/src/tests/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)        0 2023-05-11 21:36:04.000000 itzma-lint-0.1.2/src/tests/__init__.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)     4041 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/src/tests/test_itzma.py
+drwxr-xr-x   0 tchitrakorn   (501) staff       (20)        0 2023-05-13 01:22:39.979347 itzma-lint-0.1.2/src/tests/test_samples/
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      144 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/src/tests/test_samples/test1.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      426 2023-05-11 19:15:00.000000 itzma-lint-0.1.2/src/tests/test_samples/test2.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      136 2023-05-11 19:15:00.000000 itzma-lint-0.1.2/src/tests/test_samples/test3.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      270 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/src/tests/test_samples/test4.py
+-rw-r--r--   0 tchitrakorn   (501) staff       (20)      161 2023-05-13 01:19:14.000000 itzma-lint-0.1.2/src/tests/test_samples/test5.py
```

### Comparing `itzma-lint-0.1.1/.github/workflows/test.yml` & `itzma-lint-0.1.2/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `itzma-lint-0.1.1/.gitignore` & `itzma-lint-0.1.2/.gitignore`

 * *Files identical despite different names*

### Comparing `itzma-lint-0.1.1/.pylintrc` & `itzma-lint-0.1.2/.pylintrc`

 * *Files 0% similar despite different names*

```diff
@@ -35,15 +35,15 @@
 
 # Return non-zero exit code if any of these messages/categories are detected,
 # even if score is above --fail-under value. Syntax same as enable. Messages
 # specified are enabled, while categories only check already-enabled messages.
 fail-on=
 
 # Specify a score threshold under which the program will exit with error.
-fail-under=9.5
+fail-under=8
 
 # Interpret the stdin as a python script, whose filename needs to be passed as
 # the module_or_package argument.
 #from-stdin=
 
 # Files or directories to be skipped. They should be base names, not paths.
 ignore=CVS
```

### Comparing `itzma-lint-0.1.1/CONTRIBUTING.md` & `itzma-lint-0.1.2/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `itzma-lint-0.1.1/LICENSE` & `itzma-lint-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `itzma-lint-0.1.1/Makefile` & `itzma-lint-0.1.2/Makefile`

 * *Files identical despite different names*

### Comparing `itzma-lint-0.1.1/PKG-INFO` & `itzma-lint-0.1.2/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: itzma-lint
-Version: 0.1.1
+Version: 0.1.2
 Summary: A customized linter for personal use
 Author-email: Tattie Chitrakorn <tc3117@columbia.edu>
 License: MIT License
         
         Copyright (c) 2023 Tattie Chitrakorn
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -41,14 +41,16 @@
 
 <p align="center"> "Your Lint, Your Rules" </p>
 
 ![GitHub](https://img.shields.io/github/license/tchitrakorn/itzma-lint)
 ![GitHub issues](https://img.shields.io/github/issues/tchitrakorn/itzma-lint)
 [![Itzma workflow](https://github.com/tchitrakorn/itzma-lint/actions/workflows/test.yml/badge.svg)](https://github.com/tchitrakorn/itzma-lint/actions/workflows/test.yml)
 [![codecov](https://codecov.io/gh/tchitrakorn/itzma-lint/branch/main/graph/badge.svg?token=46KL4N7H8P)](https://codecov.io/gh/tchitrakorn/itzma-lint)
+[![PyPI](https://img.shields.io/pypi/v/itzma-lint)](https://pypi.org/project/itzma-lint/)
+[![Docs](https://img.shields.io/badge/docs-link-blue)](https://tchitrakorn.github.io/itzma-lint/)
 
 <h2>Overview</h1>
 
 Do you love using a linter but want even more personalized rules? Building off a traditional lint, ITZMA offers additional features such as:
 
 *  Enforcing all functions that change the state of the programs to begin with verbs
 *  Enforcing all functions that return values to be nouns
```

### Comparing `itzma-lint-0.1.1/README.md` & `itzma-lint-0.1.2/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -2,14 +2,16 @@
 
 <p align="center"> "Your Lint, Your Rules" </p>
 
 ![GitHub](https://img.shields.io/github/license/tchitrakorn/itzma-lint)
 ![GitHub issues](https://img.shields.io/github/issues/tchitrakorn/itzma-lint)
 [![Itzma workflow](https://github.com/tchitrakorn/itzma-lint/actions/workflows/test.yml/badge.svg)](https://github.com/tchitrakorn/itzma-lint/actions/workflows/test.yml)
 [![codecov](https://codecov.io/gh/tchitrakorn/itzma-lint/branch/main/graph/badge.svg?token=46KL4N7H8P)](https://codecov.io/gh/tchitrakorn/itzma-lint)
+[![PyPI](https://img.shields.io/pypi/v/itzma-lint)](https://pypi.org/project/itzma-lint/)
+[![Docs](https://img.shields.io/badge/docs-link-blue)](https://tchitrakorn.github.io/itzma-lint/)
 
 <h2>Overview</h1>
 
 Do you love using a linter but want even more personalized rules? Building off a traditional lint, ITZMA offers additional features such as:
 
 *  Enforcing all functions that change the state of the programs to begin with verbs
 *  Enforcing all functions that return values to be nouns
```

### Comparing `itzma-lint-0.1.1/pyproject.toml` & `itzma-lint-0.1.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 build-backend="setuptools.build_meta"
 
 [project]
 name = "itzma-lint"
 authors = [{name = "Tattie Chitrakorn", email = "tc3117@columbia.edu"}]
 description="A customized linter for personal use"
 readme = "README.md"
-version="0.1.1"
+version="0.1.2"
 requires-python = ">=3.9"
 
 dependencies = ["flake8", "nltk", "inflection"]
 
 classifiers = [
     "Development Status :: 2 - Pre-Alpha",
     "Programming Language :: Python :: Implementation :: CPython",
```

### Comparing `itzma-lint-0.1.1/src/itzma_lint.egg-info/PKG-INFO` & `itzma-lint-0.1.2/src/itzma_lint.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: itzma-lint
-Version: 0.1.1
+Version: 0.1.2
 Summary: A customized linter for personal use
 Author-email: Tattie Chitrakorn <tc3117@columbia.edu>
 License: MIT License
         
         Copyright (c) 2023 Tattie Chitrakorn
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -41,14 +41,16 @@
 
 <p align="center"> "Your Lint, Your Rules" </p>
 
 ![GitHub](https://img.shields.io/github/license/tchitrakorn/itzma-lint)
 ![GitHub issues](https://img.shields.io/github/issues/tchitrakorn/itzma-lint)
 [![Itzma workflow](https://github.com/tchitrakorn/itzma-lint/actions/workflows/test.yml/badge.svg)](https://github.com/tchitrakorn/itzma-lint/actions/workflows/test.yml)
 [![codecov](https://codecov.io/gh/tchitrakorn/itzma-lint/branch/main/graph/badge.svg?token=46KL4N7H8P)](https://codecov.io/gh/tchitrakorn/itzma-lint)
+[![PyPI](https://img.shields.io/pypi/v/itzma-lint)](https://pypi.org/project/itzma-lint/)
+[![Docs](https://img.shields.io/badge/docs-link-blue)](https://tchitrakorn.github.io/itzma-lint/)
 
 <h2>Overview</h1>
 
 Do you love using a linter but want even more personalized rules? Building off a traditional lint, ITZMA offers additional features such as:
 
 *  Enforcing all functions that change the state of the programs to begin with verbs
 *  Enforcing all functions that return values to be nouns
```

### Comparing `itzma-lint-0.1.1/src/testing_checks.py` & `itzma-lint-0.1.2/src/testing_checks.py`

 * *Files 6% similar despite different names*

```diff
@@ -28,43 +28,35 @@
     @classmethod
     def check(cls, node, errors):
         for child in ast.walk(node):
             if isinstance(child, ast.FunctionDef):
                 func_name = child.name
                 # camelcase check:
                 if not camelize(func_name, uppercase_first_letter=False) == func_name:
-                    err = Flake8ASTErrorInfo(
-                        child.lineno, child.col_offset, cls.msg1, cls
-                    )
+                    err = Flake8ASTErrorInfo(child.lineno, child.col_offset, cls.msg1, cls)
                     errors.append(err)
 
 
 class UnconventionalClassNamesNotAllowed:
     msg = "IM class names must be camel case with uppercase first letter"
 
     @classmethod
     def check(cls, node, errors):
         for child in ast.walk(node):
             if isinstance(child, ast.ClassDef):
                 class_name = child.name
                 if not camelize(class_name, uppercase_first_letter=True) == class_name:
-                    err = Flake8ASTErrorInfo(
-                        child.lineno, child.col_offset, cls.msg, cls
-                    )
+                    err = Flake8ASTErrorInfo(child.lineno, child.col_offset, cls.msg, cls)
                     errors.append(err)
 
 
 class UnconventionalVariableNamesNotAllowed:
     msg = "IM variable names must be plural if they are assigned to a list"
 
     @classmethod
     def check(cls, node, errors):
         for child in ast.walk(node):
             if isinstance(child, ast.Assign):  # check assignment
                 if isinstance(child.value, ast.List):  # if the value is a list
-                    if (
-                        pluralize(child.targets[0].id) == child.targets[0].id
-                    ):  # and the name is not plural
-                        err = Flake8ASTErrorInfo(
-                            child.lineno, child.col_offset, cls.msg, cls
-                        )
+                    if pluralize(child.targets[0].id) == child.targets[0].id:  # and the name is not plural
+                        err = Flake8ASTErrorInfo(child.lineno, child.col_offset, cls.msg, cls)
                         errors.append(err)
```

### Comparing `itzma-lint-0.1.1/src/tests/test_itzma.py` & `itzma-lint-0.1.2/src/tests/test_itzma.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,20 +4,15 @@
 import ast
 
 
 class UnitTests(unittest.TestCase):
     def test_error_definition(self):  # unit test 0
         line_number, offset, msg, cls = 10, 2, "Testing Message", str
         error = helpers.Flake8ASTErrorInfo(line_number, offset, msg, cls)
-        assert (
-            error.line_number == 10
-            and error.offset == 2
-            and error.msg == "Testing Message"
-            and error.cls == str
-        )
+        assert error.line_number == 10 and error.offset == 2 and error.msg == "Testing Message" and error.cls == str
 
     def test_local_imports_not_allowed(self):  # unit test 1
         expected = {
             "line_number": 7,
             "offset": 4,
             "msg": "IM local imports are not allowed inside a function",
         }
@@ -87,15 +82,15 @@
             and result.msg == expected["msg"]
         )
 
 
 class IntegrationTests(unittest.TestCase):
     def test_all_checks(self):  # integration test 1
         expected = {
-            "line_number": 5,
+            "line_number": 8,
             "offset": 0,
             "msg": "IM function names must be camel case with lowercase first letter",
         }
         errors = []
         with open("src/tests/test_samples/test5.py") as f:
             code = f.read()
         node = ast.parse(code)
```

