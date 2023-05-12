# Comparing `tmp/honeybee-ies-0.6.2.tar.gz` & `tmp/honeybee-ies-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/honeybee-ies-0.6.2.tar", last modified: Mon Feb  6 19:32:47 2023, max compression
+gzip compressed data, was "dist/honeybee-ies-0.7.0.tar", last modified: Fri May 12 22:37:07 2023, max compression
```

## Comparing `honeybee-ies-0.6.2.tar` & `honeybee-ies-0.7.0.tar`

### file list

```diff
@@ -1,66 +1,67 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     2807 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/.github/workflows/ci.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1001 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/.github/workflows/dependency-release.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      167 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      294 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/.releaserc.json
--rw-r--r--   0 runner    (1001) docker     (123)      279 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/CODE_OF_CONDUCT.md
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (123)    34523 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1674 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      165 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/deploy.sh
--rw-r--r--   0 runner    (1001) docker     (123)      276 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/dev-requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      360 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/docs/_build/
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/_build/.nojekyll
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/_build/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/docs/_build/docs/
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/_build/docs/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (123)      899 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/_static/custom.css
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/docs/_templates/
--rw-r--r--   0 runner    (1001) docker     (123)     3668 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/_templates/layout.html
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/docs/cli/
--rw-r--r--   0 runner    (1001) docker     (123)      126 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/cli/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)    21471 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      387 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)       78 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/docs/modules.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies/
--rw-r--r--   0 runner    (1001) docker     (123)       97 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/honeybee_ies/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       72 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/honeybee_ies/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)      191 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/honeybee_ies/_extend_honeybee.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies/cli/
--rw-r--r--   0 runner    (1001) docker     (123)      389 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/honeybee_ies/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2768 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/honeybee_ies/cli/translate.py
--rw-r--r--   0 runner    (1001) docker     (123)     8201 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/honeybee_ies/reader.py
--rw-r--r--   0 runner    (1001) docker     (123)      994 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/honeybee_ies/templates.py
--rw-r--r--   0 runner    (1001) docker     (123)    10208 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/honeybee_ies/writer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1265 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/honeybee_ies.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1040 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/tests/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/tests/assets/
--rw-r--r--   0 runner    (1001) docker     (123)  2630219 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/assets/lab_building.hbjson
--rw-r--r--   0 runner    (1001) docker     (123)   134559 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/assets/multiline_name_test.hbjson
--rw-r--r--   0 runner    (1001) docker     (123)   274009 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/assets/revit_sample_model.hbjson
--rw-r--r--   0 runner    (1001) docker     (123)     1171 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/assets/room_underground.gem
--rw-r--r--   0 runner    (1001) docker     (123)    47646 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/assets/room_with_air_boundary.hbjson
--rw-r--r--   0 runner    (1001) docker     (123)    46729 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/assets/sample_model_45.hbjson
--rw-r--r--   0 runner    (1001) docker     (123)    42885 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/assets/shade_with_holes.hbjson
--rw-r--r--   0 runner    (1001) docker     (123)    46189 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/assets/single_face_shade.hbjson
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-06 19:32:47.000000 honeybee-ies-0.6.2/tests/cli/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      547 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/cli/translate_cli_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      361 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/extend_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      250 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/reader_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     3186 2023-02-06 19:31:25.000000 honeybee-ies-0.6.2/tests/writer_test.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     2807 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/.github/workflows/ci.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1001 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/.github/workflows/dependency-release.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      294 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/.releaserc.json
+-rw-r--r--   0 runner    (1001) docker     (123)      279 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/CODE_OF_CONDUCT.md
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)    34523 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1674 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      165 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/deploy.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      276 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/dev-requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      360 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/docs/_build/
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/_build/.nojekyll
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/_build/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/docs/_build/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/_build/docs/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)      899 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/_static/custom.css
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/docs/_templates/
+-rw-r--r--   0 runner    (1001) docker     (123)     3668 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/_templates/layout.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/docs/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)      126 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/cli/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    21471 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      387 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       78 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/docs/modules.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/honeybee_ies/
+-rw-r--r--   0 runner    (1001) docker     (123)       97 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/honeybee_ies/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       72 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/honeybee_ies/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      191 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/honeybee_ies/_extend_honeybee.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/honeybee_ies/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)      389 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/honeybee_ies/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2765 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/honeybee_ies/cli/translate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8201 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/honeybee_ies/reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)      994 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/honeybee_ies/templates.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12240 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/honeybee_ies/writer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/honeybee_ies.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-05-12 22:37:06.000000 honeybee-ies-0.7.0/honeybee_ies.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1302 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/honeybee_ies.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:37:06.000000 honeybee-ies-0.7.0/honeybee_ies.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-12 22:37:06.000000 honeybee-ies-0.7.0/honeybee_ies.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-12 22:37:06.000000 honeybee-ies-0.7.0/honeybee_ies.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-12 22:37:06.000000 honeybee-ies-0.7.0/honeybee_ies.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1040 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/tests/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/tests/assets/
+-rw-r--r--   0 runner    (1001) docker     (123)  2630219 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/lab_building.hbjson
+-rw-r--r--   0 runner    (1001) docker     (123)    55839 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/model_with_holes.hbjson
+-rw-r--r--   0 runner    (1001) docker     (123)   134559 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/multiline_name_test.hbjson
+-rw-r--r--   0 runner    (1001) docker     (123)   274009 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/revit_sample_model.hbjson
+-rw-r--r--   0 runner    (1001) docker     (123)     1171 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/room_underground.gem
+-rw-r--r--   0 runner    (1001) docker     (123)    47646 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/room_with_air_boundary.hbjson
+-rw-r--r--   0 runner    (1001) docker     (123)    46729 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/sample_model_45.hbjson
+-rw-r--r--   0 runner    (1001) docker     (123)    42885 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/shade_with_holes.hbjson
+-rw-r--r--   0 runner    (1001) docker     (123)    46189 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/assets/single_face_shade.hbjson
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:37:07.000000 honeybee-ies-0.7.0/tests/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/cli/translate_cli_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      361 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/extend_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      250 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/reader_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3601 2023-05-12 22:35:48.000000 honeybee-ies-0.7.0/tests/writer_test.py
```

### Comparing `honeybee-ies-0.6.2/.github/workflows/ci.yaml` & `honeybee-ies-0.7.0/.github/workflows/ci.yaml`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/.github/workflows/dependency-release.yaml` & `honeybee-ies-0.7.0/.github/workflows/dependency-release.yaml`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/LICENSE` & `honeybee-ies-0.7.0/LICENSE`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/PKG-INFO` & `honeybee-ies-0.7.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: honeybee-ies
-Version: 0.6.2
+Version: 0.7.0
 Summary: Honeybee extension for import and export to/from IES-VE
 Home-page: https://github.com/ladybug-tools/honeybee-ies
 Author: Ladybug Tools
 Author-email: info@ladybug.tools
 License: AGPL-3.0
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `honeybee-ies-0.6.2/README.md` & `honeybee-ies-0.7.0/README.md`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/docs/_static/custom.css` & `honeybee-ies-0.7.0/docs/_static/custom.css`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/docs/_templates/layout.html` & `honeybee-ies-0.7.0/docs/_templates/layout.html`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/docs/conf.py` & `honeybee-ies-0.7.0/docs/conf.py`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/honeybee_ies/cli/translate.py` & `honeybee-ies-0.7.0/honeybee_ies/cli/translate.py`

 * *Files 8% similar despite different names*

```diff
@@ -27,15 +27,15 @@
                     dir_okay=True), default='.', show_default=True
 )
 @click.option(
     '--shade-thickness', '-st', help='Optional value for shade thickness in meters. '
     'This value will be used to extrude shades with no group id. IES doesn\'t consider '
     'the effect of shades with no thickness in SunCalc. This function extrudes the '
     'geometry to create a closed volume for the shade.',
-    type=click.FLOAT, default=0.01, show_default=True
+    type=click.FLOAT, default=0, show_default=True
 )
 def model_to_gem(model_json, name, folder, shade_thickness):
     """Translate a Model JSON file to an IES GEM file.
     \b
 
     Args:
         model_json: Full path to a Model JSON file (HBJSON) or a Model pkl (HBpkl) file.
```

### Comparing `honeybee-ies-0.6.2/honeybee_ies/reader.py` & `honeybee-ies-0.7.0/honeybee_ies/reader.py`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/honeybee_ies/templates.py` & `honeybee-ies-0.7.0/honeybee_ies/templates.py`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/honeybee_ies/writer.py` & `honeybee-ies-0.7.0/honeybee_ies/writer.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import pathlib
-from typing import List
+from typing import List, Union
 
 from ladybug_geometry.geometry3d import Face3D, Polyface3D, Point3D
-from honeybee.model import Model, Shade, Room, AirBoundary
+from honeybee.model import Model, Shade, Room, AirBoundary, RoofCeiling, Floor
 
 from .templates import SPACE_TEMPLATE, SHADE_TEMPLATE, ADJ_BLDG_TEMPLATE
 from .reader import Z_AXIS, ROOF_ANGLE_TOLERANCE
 
 
 def _opening_to_ies(
         parent_geo: Face3D, opening_geos: List[Face3D], opening_type: int = 0) -> str:
@@ -43,39 +43,64 @@
     vertices = '\n'.join(
         '   {:.6f}    {:.6f}    {:.6f}'.format(v.x, v.y, v.z)
         for v in vertices
     )
     return vertices
 
 
-def _shade_geometry_to_ies(geometry: Polyface3D, name: str, is_detached=True):
+def _shade_geometry_to_ies(
+    geometry: Union[Face3D, Polyface3D], name: str, is_detached=True
+        ):
+
     open_count = 0
-    unique_vertices = geometry.vertices
-    vertices = _vertices_to_ies(unique_vertices)
     faces = []
 
-    for face_i, face in zip(geometry.face_indices, geometry.faces):
-        index = [str(v + 1) for v in face_i[0]]
+    if isinstance(geometry, Polyface3D):
+        unique_vertices = geometry.vertices
+        vertices = _vertices_to_ies(unique_vertices)
+        for face_i, face in zip(geometry.face_indices, geometry.faces):
+            index = [str(v + 1) for v in face_i[0]]
+            face_str = '%d %s \n' % (len(index), ' '.join(index))
+            open_count, openings = 0, []
+            if face.has_holes:
+                sub_faces = [Face3D(hole, face.plane) for hole in face.holes]
+                openings.append(_opening_to_ies(face, sub_faces, 2))
+                open_count += len(sub_faces)
+
+            open_str = '\n' + '\n'.join(openings) if len(openings) != 0 else ''
+            faces.append('%s%d%s' % (face_str, open_count, open_str))
+        face_count = len(geometry.faces)
+    else:
+        # Face 3D
+        unique_vertices = geometry.lower_left_counter_clockwise_vertices
+        vertices = _vertices_to_ies(unique_vertices)
+        index = [str(v + 1) for v in range(len(unique_vertices))]
         face_str = '%d %s \n' % (len(index), ' '.join(index))
         open_count, openings = 0, []
-        if face.has_holes:
+        if geometry.has_holes:
             sub_faces = [Face3D(hole, face.plane) for hole in face.holes]
             openings.append(_opening_to_ies(face, sub_faces, 2))
             open_count += len(sub_faces)
-
         open_str = '\n' + '\n'.join(openings) if len(openings) != 0 else ''
         faces.append('%s%d%s' % (face_str, open_count, open_str))
+        face_count = 1
 
     template = ADJ_BLDG_TEMPLATE if is_detached else SHADE_TEMPLATE
+
+    if len(unique_vertices) < 3:
+        # a check for line-like mesh faces
+        print('Invalid line-like shade object found and removed.')
+        return ''
+
     return template.format(
         name=name,
         vertices_count=len(unique_vertices),
         vertices=vertices,
         faces='\n'.join(faces),
-        face_count=len(geometry.faces)
+        face_count=face_count
     )
 
 
 def _shade_group_to_ies(shades: List[Shade]) -> str:
     """Convert a group of shades into a GEM string.
 
     The files in the shade group should create a closed volume. The translator uses
@@ -166,56 +191,78 @@
             used to extrude shades with no group id. IES doesn't consider the effect of
             shades with no thickness in SunCalc. This function extrudes the geometry to
             create a closed volume for the shade. Default: 0.01
     Returns:
         A formatted string that represents this room in GEM format.
 
     """
+
+    def _find_index(vertex: Point3D, vertices: List[Point3D], tolerance=0.01):
+        for c, v in enumerate(vertices):
+            if v.distance_to_point(vertex) <= tolerance:
+                return str(c + 1)
+        else:
+            raise ValueError(f'Failed to find {vertex} in the vertices.')
+
     unique_vertices = room.geometry.vertices
     vertices = _vertices_to_ies(unique_vertices)
-
+    face_count = len(room.faces)
     faces = []
     air_boundary_count = 0
     _key = '__ies_import__'
     for face_i, face in zip(room.geometry.face_indices, room.faces):
         if isinstance(face.type, AirBoundary) and face.user_data \
                 and _key in face.user_data:
             # This air boundary was created during the process of importing holes
             # from an IES GEM file. We don't write these air boundaries back to GEM.
             air_boundary_count += 1
             continue
+        if isinstance(face.type, (RoofCeiling, Floor)) and face.geometry.has_holes:
+            # IES doesn't like rooms with holes in them. We need to break the face
+            # into smaller faces
+            fgs = face.geometry.split_through_holes()
+            face_count += len(fgs) - 1
+            indexes = [
+                [
+                    _find_index(v, unique_vertices)
+                    for v in fg.lower_left_counter_clockwise_vertices
+                ] for fg in fgs
+            ]
+        else:
+            fgs = [face.geometry]
+            indexes = [[str(v + 1) for v in face_i[0]]]
 
-        index = [str(v + 1) for v in face_i[0]]
-        face_str = '%d %s \n' % (len(index), ' '.join(index))
-        open_count, openings, fg = 0, [], face.geometry
-        if isinstance(face.type, AirBoundary):
-            # add the face itself as the hole
-            sub_faces = [Face3D(fg.vertices, fg.plane)]
-            openings.append(_opening_to_ies(fg, sub_faces, 2))
-            open_count += 1
-        elif fg.has_holes:
-            sub_faces = [Face3D(hole, fg.plane) for hole in fg.holes]
-            openings.append(_opening_to_ies(fg, sub_faces, 2))
-            open_count += len(sub_faces)
-        if len(face.apertures) != 0:
-            sub_faces = [ap.geometry for ap in face.apertures]
-            openings.append(_opening_to_ies(fg, sub_faces, 0))
-            open_count += len(sub_faces)
-        if len(face.doors) != 0:
-            sub_faces = [dr.geometry for dr in face.doors]
-            openings.append(_opening_to_ies(fg, sub_faces, 1))
-            open_count += len(sub_faces)
-        open_str = '\n' + '\n'.join(openings) if len(openings) != 0 else ''
-        faces.append('%s%d%s' % (face_str, open_count, open_str))
+        for index, fg in zip(indexes, fgs):
+            face_str = '%d %s \n' % (len(index), ' '.join(index))
+            open_count, openings = 0, []
+            if isinstance(face.type, AirBoundary):
+                # add the face itself as the hole
+                sub_faces = [Face3D(fg.vertices, fg.plane)]
+                openings.append(_opening_to_ies(fg, sub_faces, 2))
+                open_count += 1
+            elif fg.has_holes:
+                sub_faces = [Face3D(hole, fg.plane) for hole in fg.holes]
+                openings.append(_opening_to_ies(fg, sub_faces, 2))
+                open_count += len(sub_faces)
+            if len(face.apertures) != 0:
+                sub_faces = [ap.geometry for ap in face.apertures]
+                openings.append(_opening_to_ies(fg, sub_faces, 0))
+                open_count += len(sub_faces)
+            if len(face.doors) != 0:
+                sub_faces = [dr.geometry for dr in face.doors]
+                openings.append(_opening_to_ies(fg, sub_faces, 1))
+                open_count += len(sub_faces)
+            open_str = '\n' + '\n'.join(openings) if len(openings) != 0 else ''
+            faces.append('%s%d%s' % (face_str, open_count, open_str))
 
     # remove new lines from the name
     room_name = ' '.join(room.display_name.split())
     space = SPACE_TEMPLATE.format(
         space_name=room_name, vertices_count=len(unique_vertices),
-        face_count=len(room.faces) - air_boundary_count,
+        face_count=face_count - air_boundary_count,
         vertices=vertices, faces='\n'.join(faces)
     )
 
     # collect all the shades from room
     shades = [shade for shade in room.shades]
     for face in room.faces:
         for aperture in face.apertures:
```

### Comparing `honeybee-ies-0.6.2/honeybee_ies.egg-info/PKG-INFO` & `honeybee-ies-0.7.0/honeybee_ies.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: honeybee-ies
-Version: 0.6.2
+Version: 0.7.0
 Summary: Honeybee extension for import and export to/from IES-VE
 Home-page: https://github.com/ladybug-tools/honeybee-ies
 Author: Ladybug Tools
 Author-email: info@ladybug.tools
 License: AGPL-3.0
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `honeybee-ies-0.6.2/honeybee_ies.egg-info/SOURCES.txt` & `honeybee-ies-0.7.0/honeybee_ies.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -35,14 +35,15 @@
 honeybee_ies.egg-info/top_level.txt
 honeybee_ies/cli/__init__.py
 honeybee_ies/cli/translate.py
 tests/extend_test.py
 tests/reader_test.py
 tests/writer_test.py
 tests/assets/lab_building.hbjson
+tests/assets/model_with_holes.hbjson
 tests/assets/multiline_name_test.hbjson
 tests/assets/revit_sample_model.hbjson
 tests/assets/room_underground.gem
 tests/assets/room_with_air_boundary.hbjson
 tests/assets/sample_model_45.hbjson
 tests/assets/shade_with_holes.hbjson
 tests/assets/single_face_shade.hbjson
```

### Comparing `honeybee-ies-0.6.2/setup.py` & `honeybee-ies-0.7.0/setup.py`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/assets/lab_building.hbjson` & `honeybee-ies-0.7.0/tests/assets/lab_building.hbjson`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/assets/multiline_name_test.hbjson` & `honeybee-ies-0.7.0/tests/assets/multiline_name_test.hbjson`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/assets/revit_sample_model.hbjson` & `honeybee-ies-0.7.0/tests/assets/revit_sample_model.hbjson`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/assets/room_underground.gem` & `honeybee-ies-0.7.0/tests/assets/room_underground.gem`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/assets/room_with_air_boundary.hbjson` & `honeybee-ies-0.7.0/tests/assets/room_with_air_boundary.hbjson`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/assets/sample_model_45.hbjson` & `honeybee-ies-0.7.0/tests/assets/sample_model_45.hbjson`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/assets/shade_with_holes.hbjson` & `honeybee-ies-0.7.0/tests/assets/shade_with_holes.hbjson`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/assets/single_face_shade.hbjson` & `honeybee-ies-0.7.0/tests/assets/single_face_shade.hbjson`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/cli/translate_cli_test.py` & `honeybee-ies-0.7.0/tests/cli/translate_cli_test.py`

 * *Files identical despite different names*

### Comparing `honeybee-ies-0.6.2/tests/writer_test.py` & `honeybee-ies-0.7.0/tests/writer_test.py`

 * *Files 7% similar despite different names*

```diff
@@ -87,7 +87,20 @@
         '4 2\n' \
         '   9.000000    7.000000\n' \
         '   9.000000    9.000000\n' \
         '   7.000000    9.000000\n' \
         '   7.000000    7.000000\n'
 
     assert hole_str in outf.read_text()
+
+
+def test_model_with_holes():
+    in_file = './tests/assets/model_with_holes.hbjson'
+    out_folder = pathlib.Path('./tests/assets/temp')
+    out_folder.mkdir(parents=True, exist_ok=True)
+    model = Model.from_hbjson(in_file)
+    outf = model_to_ies(model, out_folder.as_posix(), name='model_with_holes')
+    assert outf.exists()
+
+    room_str = 'IES Room w holes\n28 18'
+
+    assert room_str in outf.read_text()
```

