# Comparing `tmp/cliconfig-0.5.0.tar.gz` & `tmp/cliconfig-0.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cliconfig-0.5.0.tar", last modified: Fri May 12 17:49:21 2023, max compression
+gzip compressed data, was "cliconfig-0.5.1.tar", last modified: Sat May 13 00:48:37 2023, max compression
```

## Comparing `cliconfig-0.5.0.tar` & `cliconfig-0.5.1.tar`

### file list

```diff
@@ -1,106 +1,107 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.297199 cliconfig-0.5.0/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.coveragerc
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.265199 cliconfig-0.5.0/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.277199 cliconfig-0.5.0/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.github/workflows/flake.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.github/workflows/mypy.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.github/workflows/pipy_deployment.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.github/workflows/pydocstyle.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.github/workflows/pylint.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.github/workflows/ruff.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.github/workflows/tests.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.markdownlint.json
--rw-r--r--   0 runner    (1001) docker     (123)    20457 2023-05-12 17:49:05.000000 cliconfig-0.5.0/.pylintrc
--rw-r--r--   0 runner    (1001) docker     (123)     4847 2023-05-12 17:49:05.000000 cliconfig-0.5.0/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-12 17:49:05.000000 cliconfig-0.5.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     6778 2023-05-12 17:49:21.297199 cliconfig-0.5.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    10441 2023-05-12 17:49:05.000000 cliconfig-0.5.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     6343 2023-05-12 17:49:05.000000 cliconfig-0.5.0/README_pypi.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.277199 cliconfig-0.5.0/cliconfig/
--rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-12 17:49:21.000000 cliconfig-0.5.0/cliconfig/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/cli_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     7616 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/config_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)    14751 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/dict_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     8079 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/process_routines.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.281199 cliconfig-0.5.0/cliconfig/processing/
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/processing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3118 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/processing/_type_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1703 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/processing/base.py
--rw-r--r--   0 runner    (1001) docker     (123)    16117 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/processing/builtin.py
--rw-r--r--   0 runner    (1001) docker     (123)     4786 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/processing/create.py
--rw-r--r--   0 runner    (1001) docker     (123)     2017 2023-05-12 17:49:05.000000 cliconfig-0.5.0/cliconfig/tag_routines.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.281199 cliconfig-0.5.0/cliconfig.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6778 2023-05-12 17:49:21.000000 cliconfig-0.5.0/cliconfig.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2336 2023-05-12 17:49:21.000000 cliconfig-0.5.0/cliconfig.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 17:49:21.000000 cliconfig-0.5.0/cliconfig.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-12 17:49:21.000000 cliconfig-0.5.0/cliconfig.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-12 17:49:21.000000 cliconfig-0.5.0/cliconfig.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.285199 cliconfig-0.5.0/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.285199 cliconfig-0.5.0/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (123)     5501 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/_static/logo.png
--rw-r--r--   0 runner    (1001) docker     (123)     6203 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/_static/logo_extend.png
--rw-r--r--   0 runner    (1001) docker     (123)      507 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/cliconfig.processing.rst
--rw-r--r--   0 runner    (1001) docker     (123)      818 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/cliconfig_api.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/contribute.md
--rw-r--r--   0 runner    (1001) docker     (123)      965 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/edge_cases.md
--rw-r--r--   0 runner    (1001) docker     (123)     4827 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/installation.md
--rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/license.md
--rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)    12546 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/processing.md
--rw-r--r--   0 runner    (1001) docker     (123)     5006 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/quickstart.md
--rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-12 17:49:05.000000 cliconfig-0.5.0/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.289199 cliconfig-0.5.0/github_actions_utils/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-12 17:49:05.000000 cliconfig-0.5.0/github_actions_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-12 17:49:05.000000 cliconfig-0.5.0/github_actions_utils/color.py
--rw-r--r--   0 runner    (1001) docker     (123)      754 2023-05-12 17:49:05.000000 cliconfig-0.5.0/github_actions_utils/pydocstyle_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-12 17:49:05.000000 cliconfig-0.5.0/github_actions_utils/pylint_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-12 17:49:05.000000 cliconfig-0.5.0/github_actions_utils/pytest_manager.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.289199 cliconfig-0.5.0/licenses_tier/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-12 17:49:05.000000 cliconfig-0.5.0/licenses_tier/FLATTEN_DICT_LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1252 2023-05-12 17:49:05.000000 cliconfig-0.5.0/pre-commit-checks.sh
--rw-r--r--   0 runner    (1001) docker     (123)     2579 2023-05-12 17:49:05.000000 cliconfig-0.5.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-12 17:49:05.000000 cliconfig-0.5.0/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-12 17:49:05.000000 cliconfig-0.5.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 17:49:21.297199 cliconfig-0.5.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-12 17:49:05.000000 cliconfig-0.5.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.289199 cliconfig-0.5.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.293199 cliconfig-0.5.0/tests/configs/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/config1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/config2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/configtag1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/configtag2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/default1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/default2.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.293199 cliconfig-0.5.0/tests/configs/integration/
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/integration/main.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/integration/sub1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       31 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/integration/sub2.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.297199 cliconfig-0.5.0/tests/configs/merge/
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/merge/additional1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/merge/additional2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/merge/additional3.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/merge/default1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/merge/default2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/configs/merge/default3.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2517 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.297199 cliconfig-0.5.0/tests/integration/
--rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/integration/test_inte_multiple_tags.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.297199 cliconfig-0.5.0/tests/unit/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:49:21.297199 cliconfig-0.5.0/tests/unit/processing/
--rw-r--r--   0 runner    (1001) docker     (123)      932 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/processing/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     8301 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/processing/test_builtin.py
--rw-r--r--   0 runner    (1001) docker     (123)     2207 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/processing/test_create.py
--rw-r--r--   0 runner    (1001) docker     (123)     1294 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/processing/test_type_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/test_cli_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/test_config_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     5808 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/test_dict_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/test_process_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     1523 2023-05-12 17:49:05.000000 cliconfig-0.5.0/tests/unit/test_tag_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.coveragerc
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.219479 cliconfig-0.5.1/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.223479 cliconfig-0.5.1/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/flake.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/mypy.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/pipy_deployment.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/pydocstyle.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/pylint.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/ruff.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/tests.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.markdownlint.json
+-rw-r--r--   0 runner    (1001) docker     (123)    20457 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.pylintrc
+-rw-r--r--   0 runner    (1001) docker     (123)     4847 2023-05-13 00:48:19.000000 cliconfig-0.5.1/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 00:48:19.000000 cliconfig-0.5.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     6788 2023-05-13 00:48:37.231479 cliconfig-0.5.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    10451 2023-05-13 00:48:19.000000 cliconfig-0.5.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     6353 2023-05-13 00:48:19.000000 cliconfig-0.5.1/README_pypi.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/cliconfig/
+-rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/cli_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7339 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/config_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14751 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/dict_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8079 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/process_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/cliconfig/processing/
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3118 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/_type_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1703 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16885 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/builtin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9833 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/create.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3032 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/tag_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/cliconfig.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6788 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2363 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)     5501 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/_static/logo.png
+-rw-r--r--   0 runner    (1001) docker     (123)     6203 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/_static/logo_extend.png
+-rw-r--r--   0 runner    (1001) docker     (123)      507 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/cliconfig.processing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      818 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/cliconfig_api.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/contribute.md
+-rw-r--r--   0 runner    (1001) docker     (123)      965 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/edge_cases.md
+-rw-r--r--   0 runner    (1001) docker     (123)     4827 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/installation.md
+-rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/license.md
+-rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/processing.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5006 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/quickstart.md
+-rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/github_actions_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/color.py
+-rw-r--r--   0 runner    (1001) docker     (123)      754 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/pydocstyle_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/pylint_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/pytest_manager.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/licenses_tier/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 00:48:19.000000 cliconfig-0.5.1/licenses_tier/FLATTEN_DICT_LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1252 2023-05-13 00:48:19.000000 cliconfig-0.5.1/pre-commit-checks.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     2579 2023-05-13 00:48:19.000000 cliconfig-0.5.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 00:48:19.000000 cliconfig-0.5.1/requirements-dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 00:48:19.000000 cliconfig-0.5.1/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 00:48:37.231479 cliconfig-0.5.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 00:48:19.000000 cliconfig-0.5.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/configs/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/config1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/config2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/configtag1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/configtag2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/default1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/default2.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/configs/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/integration/main.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/integration/sub1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/integration/sub2.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/configs/merge/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/additional1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/additional2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/additional3.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/default1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/default2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/default3.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/integration/test_inte_multiple_tags.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/unit/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/unit/processing/
+-rw-r--r--   0 runner    (1001) docker     (123)      932 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/processing/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8624 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/processing/test_builtin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/processing/test_create.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1294 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/processing/test_type_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_cli_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_config_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5808 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_dict_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4779 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_ex_docs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_process_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2181 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_tag_routines.py
```

### Comparing `cliconfig-0.5.0/.github/workflows/pipy_deployment.yaml` & `cliconfig-0.5.1/.github/workflows/pipy_deployment.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/.github/workflows/pydocstyle.yaml` & `cliconfig-0.5.1/.github/workflows/pydocstyle.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/.github/workflows/pylint.yaml` & `cliconfig-0.5.1/.github/workflows/pylint.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/.github/workflows/tests.yaml` & `cliconfig-0.5.1/.github/workflows/tests.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/.pylintrc` & `cliconfig-0.5.1/.pylintrc`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/CONTRIBUTING.md` & `cliconfig-0.5.1/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/LICENSE` & `cliconfig-0.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/PKG-INFO` & `cliconfig-0.5.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cliconfig
-Version: 0.5.0
+Version: 0.5.1
 Summary: Merge your config files and set parameters from the command line in a simple way.
 Author-email: Valentin Goldite <valentin.goldite@gmail.com>
 Project-URL: Source, https://github.com/valentingol/cliconfig
 Keywords: logging,machine,learning
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
@@ -135,21 +135,21 @@
 * [x] allow passing new arguments by CLI (with warning and no actual merge)
 * [ ] add a routine to check if a tag is in a key and robust to all other
   possible tags
 * [ ] add an integration test with all built-in processing (and more)
 
 Secondary:
 
-* [ ] add `make_processing_keep_status` to make a processing that keep the
-  status of a parameter across merged configs. The status is any python object
+* [ ] add `make_processing_keep_property` to make a processing that keep the
+  property of a parameter across merged configs. The property is any python object
   returned by a function that takes the parameter as input
 * [ ] add `ProcessSelect` (with tag "@select") to select a subconfig (or parameter)
   and delete the others configs at the same level (to cure the resulting config)
 * [ ] allow nested types in `ProcessTyping`
-* [ ] add DefaultProcessing that add default processing to list of processing
+* [x] add DefaultProcessings that stores default processing as list of processing
 
 ## License
 
 Copyright (C) 2023  Valentin Goldité
 
 This program is free software: you can redistribute it and/or modify it under the
 terms of the [MIT License](LICENSE). This program is distributed in the hope that
```

### Comparing `cliconfig-0.5.0/README.md` & `cliconfig-0.5.1/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -226,27 +226,27 @@
 Please see our [contributing guidelines](CONTRIBUTING.md) for more information 🤗
 
 ## Todo
 
 Priority:
 
 * [x] allow passing new arguments by CLI (with warning and no actual merge)
-* [ ] add a routine to check if a tag is in a key and robust to all other
+* [x] add a routine to check if a tag is in a key and robust to all other
   possible tags
 * [ ] add an integration test with all built-in processing (and more)
 
 Secondary:
 
-* [ ] add `make_processing_keep_status` to make a processing that keep the
-  status of a parameter across merged configs. The status is any python object
+* [x] add `make_processing_keep_property` to make a processing that keep the
+  property of a parameter across merged configs. The property is any python object
   returned by a function that takes the parameter as input
 * [ ] add `ProcessSelect` (with tag "@select") to select a subconfig (or parameter)
   and delete the others configs at the same level (to cure the resulting config)
 * [ ] allow nested types in `ProcessTyping`
-* [ ] add DefaultProcessing that add default processing to list of processing
+* [x] add DefaultProcessings that stores default processing as list of processing
 
 ## License
 
 Copyright (C) 2023  Valentin Goldité
 
 This program is free software: you can redistribute it and/or modify it under the
 terms of the [MIT License](LICENSE). This program is distributed in the hope that
```

### Comparing `cliconfig-0.5.0/README_pypi.md` & `cliconfig-0.5.1/README_pypi.md`

 * *Files 2% similar despite different names*

```diff
@@ -123,21 +123,21 @@
 * [x] allow passing new arguments by CLI (with warning and no actual merge)
 * [ ] add a routine to check if a tag is in a key and robust to all other
   possible tags
 * [ ] add an integration test with all built-in processing (and more)
 
 Secondary:
 
-* [ ] add `make_processing_keep_status` to make a processing that keep the
-  status of a parameter across merged configs. The status is any python object
+* [ ] add `make_processing_keep_property` to make a processing that keep the
+  property of a parameter across merged configs. The property is any python object
   returned by a function that takes the parameter as input
 * [ ] add `ProcessSelect` (with tag "@select") to select a subconfig (or parameter)
   and delete the others configs at the same level (to cure the resulting config)
 * [ ] allow nested types in `ProcessTyping`
-* [ ] add DefaultProcessing that add default processing to list of processing
+* [x] add DefaultProcessings that stores default processing as list of processing
 
 ## License
 
 Copyright (C) 2023  Valentin Goldité
 
 This program is free software: you can redistribute it and/or modify it under the
 terms of the [MIT License](LICENSE). This program is distributed in the hope that
```

### Comparing `cliconfig-0.5.0/cliconfig/cli_parser.py` & `cliconfig-0.5.1/cliconfig/cli_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/cliconfig/config_routines.py` & `cliconfig-0.5.1/cliconfig/config_routines.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,20 +8,15 @@
 from cliconfig.process_routines import (
     load_processing,
     merge_flat_paths_processing,
     merge_flat_processing,
     save_processing,
 )
 from cliconfig.processing.base import Processing
-from cliconfig.processing.builtin import (
-    ProcessCheckTags,
-    ProcessCopy,
-    ProcessMerge,
-    ProcessTyping,
-)
+from cliconfig.processing.builtin import DefaultProcessings
 from cliconfig.tag_routines import clean_all_tags
 
 
 def make_config(
     *default_config_paths: str,
     process_list: Optional[List[Processing]] = None,
     add_default_processing: bool = True,
@@ -71,28 +66,23 @@
             --architecture.layers.hidden_dim=64
 
     """
     # Create the processing list
     if process_list is None:
         process_list_: List[Processing] = []
     if add_default_processing:
-        process_list_.extend([
-            ProcessCheckTags(),
-            ProcessTyping(),
-            ProcessCopy(),
-            ProcessMerge(),
-        ])
+        process_list_ += DefaultProcessings().list
 
     config = Config({}, process_list_)
 
     # Merge default configs and additional configs
     additional_config_paths, cli_params_dict = parse_cli(sys.argv)
     for i, paths in enumerate([default_config_paths, additional_config_paths]):
         # Allow new keys for default configs only
-        allow_new_keys = (i == 0)
+        allow_new_keys = i == 0
         for path in paths:
             config = merge_flat_paths_processing(
                 config,
                 path,
                 allow_new_keys=allow_new_keys,
                 preprocess_first=False,  # Already processed
             )
@@ -165,20 +155,15 @@
         list (config.process_list), which can be used to apply further processing
         routines.
     """
     # Crate process_list
     if process_list is None:
         process_list_ = []
     if add_default_processing:
-        process_list_.extend([
-            ProcessTyping(),
-            ProcessCheckTags(),
-            ProcessCopy(),
-            ProcessMerge(),
-        ])
+        process_list_ += DefaultProcessings().list
 
     config = Config({}, process_list_)
     if default_config_paths:
         for config_path in default_config_paths:
             config = merge_flat_paths_processing(
                 config,
                 config_path,
```

### Comparing `cliconfig-0.5.0/cliconfig/dict_routines.py` & `cliconfig-0.5.1/cliconfig/dict_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/cliconfig/process_routines.py` & `cliconfig-0.5.1/cliconfig/process_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/cliconfig/processing/_type_parser.py` & `cliconfig-0.5.1/cliconfig/processing/_type_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/cliconfig/processing/base.py` & `cliconfig-0.5.1/cliconfig/processing/base.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/cliconfig/processing/builtin.py` & `cliconfig-0.5.1/cliconfig/processing/builtin.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 """Built-in processing classes.
 
 Classes to apply pre-merge, post-merge, pre-save and post-load modifications
 to dict with processing routines (found in cliconfig.process_routines).
 """
 # pylint: disable=unused-argument
-from typing import Any, Dict
+from typing import Any, Dict, List
 
 from cliconfig.base import Config
 from cliconfig.process_routines import (
     merge_flat_paths_processing,
     merge_flat_processing,
 )
 from cliconfig.processing._type_parser import _parse_type
 from cliconfig.processing.base import Processing
-from cliconfig.tag_routines import clean_all_tags, clean_tag, dict_clean_tags
+from cliconfig.tag_routines import clean_all_tags, clean_tag, dict_clean_tags, is_tag_in
 
 
 class ProcessMerge(Processing):
     """Merge dicts just in time with '@merge_after/_before/_add' tags.
 
     Tag your key with '@merge_after', '@merge_before' or @merge_add to load
     the dict corresponding to the value (path) and merge it just before or after
@@ -70,16 +70,15 @@
         super().__init__()
         self.premerge_order = -20.0
 
     def premerge(self, flat_config: Config) -> Config:
         """Pre-merge processing."""
         items = list(flat_config.dict.items())
         for flat_key, val in items:
-            end_key = flat_key.split('.')[-1]
-            if "@merge_after" in end_key:
+            if is_tag_in(flat_key, "merge_after"):
                 if not isinstance(val, str) or not val.endswith('.yaml'):
                     raise ValueError(
                         "Key with '@merge_after' tag must be associated "
                         "to a string corresponding to a *yaml* file."
                         f"The problem occurs at key: {flat_key}"
                     )
                 # Remove the tag in the dict
@@ -93,15 +92,15 @@
                     flat_config,
                     val,
                     allow_new_keys=True,
                     preprocess_first=False,  # Already processed
                     postprocess=False,
                 )
 
-            elif "@merge_before" in end_key:
+            elif is_tag_in(flat_key, "merge_before"):
                 if not isinstance(val, str) or not val.endswith('.yaml'):
                     raise ValueError(
                         "Key with '@merge_before' tag must be associated "
                         "to a string corresponding to a *yaml* file."
                         f"The problem occurs at key: {flat_key}"
                     )
                 # Remove the tag in the dict
@@ -112,15 +111,15 @@
                     val,
                     flat_config,
                     allow_new_keys=True,
                     preprocess_second=False,  # Already processed
                     postprocess=False,
                 )
 
-            elif "@merge_add" in end_key:
+            elif is_tag_in(flat_key, "merge_add"):
                 if not isinstance(val, str) or not val.endswith('.yaml'):
                     raise ValueError(
                         "Key with '@merge_add' tag must be associated "
                         "to a string corresponding to a *yaml* file."
                         f"The problem occurs at key: {flat_key}"
                     )
                 # Remove the tag in the dict
@@ -200,16 +199,15 @@
         self.keys_to_copy: Dict[str, str] = {}
         self.current_value: Dict[str, Any] = {}
 
     def premerge(self, flat_config: Config) -> Config:
         """Pre-merge processing."""
         items = list(flat_config.dict.items())
         for flat_key, val in items:
-            key = flat_key.split(".")[-1]
-            if "@copy" in key:
+            if is_tag_in(flat_key, "copy"):
                 if not isinstance(val, str):
                     raise ValueError(
                         "Key with '@copy' tag must be associated "
                         "to a string corresponding to a flat key. "
                         f"The problem occurs at key: {flat_key} with value: {val}"
                     )
                 clean_key = clean_all_tags(flat_key)
@@ -370,7 +368,32 @@
                 "- a missing processing in process_list\n"
                 "- the use of an 'at' ('@') in a parameter name\n"
                 "- the use of a custom processing that does not remove a tag\n\n"
                 "The tagged keys encountered (5 first if more than 5) are:\n"
                 f"{keys_message}"
             )
         return flat_config
+
+
+class DefaultProcessings():
+    """Default list of built-in processings.
+
+    To add these processings to a Config instance, use:
+
+    config.process_list += DefaultProcessings().list
+
+    The current default processing list contains:
+     * ProcessCheckTags: protect against '@' in keys at the end of pre-merge)
+     * ProcessMerge (@merge_all, @merge_before, @merge_after): merge multiple
+       files into one.
+     * ProcessCopy (@copy): persistently copy a value from one key to an other
+       and protect it
+     * ProcessTyping (@type:X): force the type of parameter to any type X.
+    """
+
+    def __init__(self) -> None:
+        self.list: List[Processing] = [
+            ProcessCheckTags(),
+            ProcessMerge(),
+            ProcessCopy(),
+            ProcessTyping(),
+        ]
```

### Comparing `cliconfig-0.5.0/cliconfig/tag_routines.py` & `cliconfig-0.5.1/cliconfig/tag_routines.py`

 * *Files 14% similar despite different names*

```diff
@@ -69,7 +69,39 @@
     tagged_keys = []
     for key, value in items:
         if '@' in key:
             del clean_dict[key]
             clean_dict[clean_all_tags(key)] = value
             tagged_keys.append(key)
     return clean_dict, tagged_keys
+
+
+def is_tag_in(flat_key: str, tag_name: str, *, full_key: bool = False) -> bool:
+    """Check if a tag is in a flat key.
+
+    The tag name must be the exact name. For instance the tag "@tag" is not
+    found if the key is only tagged with "@tag_2".
+
+    Parameters
+    ----------
+    flat_key : str
+        The flat key to check.
+    tag_name : str
+        The name of the tag to check, with or without the '@' prefix.
+    full_key : bool, optional
+        If True, check for the full key. If False, check for the last part of
+        the flat key (after the last dot) that correspond to the parameter name.
+        By default, False.
+
+    Returns
+    -------
+    bool
+        True if the tag is in the flat key, False otherwise.
+    """
+    if tag_name[0] == "@":
+        tag_name = tag_name[1:]
+    if not full_key:
+        flat_key = flat_key.split('.')[-1]
+    is_in = (flat_key.endswith(f"@{tag_name}")
+             or f"@{tag_name}@" in flat_key
+             or f"@{tag_name}." in flat_key)
+    return is_in
```

### Comparing `cliconfig-0.5.0/cliconfig.egg-info/PKG-INFO` & `cliconfig-0.5.1/cliconfig.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cliconfig
-Version: 0.5.0
+Version: 0.5.1
 Summary: Merge your config files and set parameters from the command line in a simple way.
 Author-email: Valentin Goldite <valentin.goldite@gmail.com>
 Project-URL: Source, https://github.com/valentingol/cliconfig
 Keywords: logging,machine,learning
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
@@ -135,21 +135,21 @@
 * [x] allow passing new arguments by CLI (with warning and no actual merge)
 * [ ] add a routine to check if a tag is in a key and robust to all other
   possible tags
 * [ ] add an integration test with all built-in processing (and more)
 
 Secondary:
 
-* [ ] add `make_processing_keep_status` to make a processing that keep the
-  status of a parameter across merged configs. The status is any python object
+* [ ] add `make_processing_keep_property` to make a processing that keep the
+  property of a parameter across merged configs. The property is any python object
   returned by a function that takes the parameter as input
 * [ ] add `ProcessSelect` (with tag "@select") to select a subconfig (or parameter)
   and delete the others configs at the same level (to cure the resulting config)
 * [ ] allow nested types in `ProcessTyping`
-* [ ] add DefaultProcessing that add default processing to list of processing
+* [x] add DefaultProcessings that stores default processing as list of processing
 
 ## License
 
 Copyright (C) 2023  Valentin Goldité
 
 This program is free software: you can redistribute it and/or modify it under the
 terms of the [MIT License](LICENSE). This program is distributed in the hope that
```

### Comparing `cliconfig-0.5.0/cliconfig.egg-info/SOURCES.txt` & `cliconfig-0.5.1/cliconfig.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -75,13 +75,14 @@
 tests/configs/merge/default1.yaml
 tests/configs/merge/default2.yaml
 tests/configs/merge/default3.yaml
 tests/integration/test_inte_multiple_tags.py
 tests/unit/test_cli_parser.py
 tests/unit/test_config_routines.py
 tests/unit/test_dict_routines.py
+tests/unit/test_ex_docs.py
 tests/unit/test_process_routines.py
 tests/unit/test_tag_routines.py
 tests/unit/processing/test_base.py
 tests/unit/processing/test_builtin.py
 tests/unit/processing/test_create.py
 tests/unit/processing/test_type_parser.py
```

### Comparing `cliconfig-0.5.0/docs/Makefile` & `cliconfig-0.5.1/docs/Makefile`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/_static/logo.png` & `cliconfig-0.5.1/docs/_static/logo.png`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/_static/logo_extend.png` & `cliconfig-0.5.1/docs/_static/logo_extend.png`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/cliconfig_api.rst` & `cliconfig-0.5.1/docs/cliconfig_api.rst`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/conf.py` & `cliconfig-0.5.1/docs/conf.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/edge_cases.md` & `cliconfig-0.5.1/docs/edge_cases.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/index.rst` & `cliconfig-0.5.1/docs/index.rst`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/license.md` & `cliconfig-0.5.1/docs/license.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/make.bat` & `cliconfig-0.5.1/docs/make.bat`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/docs/processing.md` & `cliconfig-0.5.1/docs/processing.md`

 * *Files 12% similar despite different names*

```diff
@@ -78,26 +78,26 @@
 Fortunately, the post-merge orders are set as follows: `20.0` for the type processing
 and `10.0` for the copy processing. As a result, the copy processing triggers first.
 Therefore, it is crucial to carefully manage the order when creating your own
 processings!
 
 ## Create basic processing
 
-### Pre-merge processing dealing with a single value at a time
+### Pre-merge processing that modify a single value
 
 The pre-merge processing is particularly useful as it allows you to modify the input
 config provided by the user and create the resulting Python dictionary that stores the
 configuration for your experiment. It serves as the interface between the user config
 and the final config.
 
-In a lot of cases, you may need to get parameters which names match a certain
+In some cases, you may need to get parameters which names match a certain
 patterns (e.g a prefix or a suffix) or contain a specific tag and modify their values
 depending on their current ones.
 
-To simplify this process, we provide the `cliconfig.create_processing_value` function.
+To simplify the creation of such a process, we provide the `cliconfig.create_processing_value` function.
 This function allows you to quickly create a processing that matches a regular
 expression or a specific tag name (in which case the tag is removed after pre-merging).
 You specify the function to be applied on the value to modify it, and optionally,
 the order of the processing. Additionally, there is a `persistent` argument, which is
 a boolean value indicating whether encountering the tag (if a tag is used) once in
 a parameter name will continue to trigger the processing for this parameter
 even after the tag is removed.
@@ -113,78 +113,121 @@
 be converted to `{"subconfig.param": "1"}`. Moreover, the keys `subconfig.param`
 will be permanently converted to strings before every merge.
 
 It's worth noting that you can also use functions that have side effects without
 necessarily changing the value itself. For example, you can use a function to
 check if a certain condition is met by the value.
 
+### Pre-merge/post-merge processing that protect a property from being modified
+
+An other useful kind of processing is a processing that ensure to keep a certain
+property on the value. For this kind of processing, you can use
+`cliconfig.create_processing_keep_property`. It takes a function that returns
+the property from the value, the regex or the tag name like the previous function,
+and the order of the pre-merge and the post-merge.
+
+The pre-merge processing looks for keys that match the tag or the regex, apply
+the function on the value and store the result (= the "property").
+The post-merge processing will check that the property is the same as the one
+stored during pre-merge. If not, it will raise an error.
+
+Examples:
+
+A processing that enforce the types of all the parameters to be constant
+(equal to the type of the first value encountered):
+
+```python
+create_processing_keep_property(type, regex=".*", premerge_order=15.0,
+                                postmerge_order=15.0)
+```
+
+A processing that protect parameters tagged with @protect from being changed:
+
+```python
+create_processing_keep_property(lambda x: x, tag_name="protect",
+                                premerge_order=15.0, postmerge_order=15.0)
+```
+
+Each time you choose the order `15.0` because it is a good values for processing that
+made checks on the values. Indeed processings that change the values such as
+`ProcessCopy` have an order that is generally <= 10.0.
+
 ## Create your processing classes (Advanced)
 
 To create your own processing classes and unlock more possibilities, you simply
 need to overload the methods of the Processing class to modify the config at the
 desired timings. To do so, you often need to manipulate tags.
 
 ### Manipulate the tags
 
 Tags are useful for triggering a processing, as we have seen. However, we need
 to be cautious because tagging a key modifies its name and can lead to conflicts
 when using processing. To address this issue, we provide tag routines in
 `cliconfig.tag_routines`. These routines include:
 
+* `is_tag_in`: Checks if a tag is in a key. It look for the exact tag name.
+  If `full_key` is True, it looks for all the fkat key, including sub-configs
+  (default: False)
 * `clean_tag`: Removes a specific tag (based on its exact name) from a key.
   It is helpful to remove the tag after pre-merging.
 * `clean_all_tags`: Removes all tags from a key. This is helpful each time you
   need the true parameter name.
 * `clean_dict_tags`: Removes all tags from a dictionary and returns the cleaned
   dict along with a list of keys that contained tags. This is helpful to get all
   the parameter names of a full dict with tags.
 
-With these tools, we can write a processing, for example, that searches for the
-tag `"@protect"` and restores the value of a parameter after every merge.
-In other words, the value is protected from being changed by the user.
+With these tools, we can write a processing, for example, that searches for all
+parameters with a tag @look ant that prints their sorted values at the end of
+the post-merging.
 
 ```python
-class ProcessProtect(Processing):
-    """Prevent a value from being changed after merging."""
+class ProcessPrintSorted(Processing):
+    """Print the parameters tagged with "@look", sorted by value on post-merge."""
 
     def __init__(self) -> None:
         super().__init__()
-        self.protected_params: Dict[str, Any] = {}
+        self.looked_keys: Set[str] = set()
+        # Pre-merge just look for the tag so order is not important
+        self.premerge_order = 0.0
+        # Post-merge should be after the copy processing if we want the final values
+        # on post-merge
+        self.postmerge_order = 15.0
 
-    # NOTE: process_list will not be used here
     def premerge(self, flat_config: Config) -> Config:
         """Pre-merge processing."""
-        # Browse a freeze version of the dict
+        # Browse a freeze version of the dict (because we will modify it to remove tags)
         items = list(flat_config.dict.items())
         for flat_key, value in items:
-            end_key = flat_key.split(".")[-1]  # parameter name
-            if "@protect" in end_key:
+            if is_tag_in(flat_key, "look"):  # Check if the key contains the tag
                 # Remove the tag and update the dict
-                new_key = clean_tag(flat_key, "protect")
-                del flat_config.dict[flat_key]
+                new_key = clean_tag(flat_key, "look")
                 flat_config.dict[new_key] = value
-                # Store the value
+                del flat_config.dict[flat_key]
+                # Store the key
                 clean_key = clean_all_tags(key)  # remove all tags = true parameter name
-                self.protected_params[clean_key] = value
+                self.looked_keys.add(clean_key)
         return flat_config
 
     def postmerge(self, flat_config: Config) -> Config:
         """Post-merge processing."""
-        # Restore the values and print a warning if they were modified
-        for key, value in self.protected_params.items():
-            # (`if key in flat_dict:` is important: the dicts seen by the processing
-            # not necessarily contains all the same keys)
+        values = []
+        for key in self.looked_keys:
+            # IMPORTANT
+            # ("if key in flat_config.dict:" is important in case of some keys were
+            # removed or if multiple dicts with different parameters are seen by
+            # the processing)
             if key in flat_config.dict:
-                if flat_config.dict[key] != value:
-                    print(f"WARNING: protected key {key} was modified by the merge")
-                flat_config.dict[key] = value
-        return flat_config
+                values.append(flat_config.dict[key])
+        print("The sorted looked values are: ", sorted(values))
+        # If we don't want to keep the looked keys for further print:
+        self.looked_keys = set()
 
+        return flat_config
 
-# Use it:
+# And to use it:
 config = make_config("main.yaml", process_list=[ProcessProtect()])
 ```
 
 **Important note**: After all pre-merge processings, the config should no longer contains
 tags as they should be removed by pre-merge processings. Otherwise, a security
 processing raises an error. It is then not necessary to take care on tags on post-merge,
 and pre-save.
@@ -242,36 +285,63 @@
 instance to choose a particular configuration among several ones by setting the path
 as value of the tagged key (as long as this config is on the default configs).
 
 ### Change processing list in processing (Still more advanced)
 
 Note that the processing functions receive the list of processing objects as an
 input and update as an attribute of the processing object. This means that it
-is possible to manually modify this list in processing functions to change internal
-variables, add or remove processing.
+is possible to manually modify this list in processing functions.
 
-One simple example is creating a processing that triggers only once and adds a
-list of processing to the processing list. This avoids the need to pass the entire
-list in the make_config function.
+**Disclaimer**: The processing list to apply during pre/post-merge, pre-save and
+post-load are determined before the first processing is applied. Therefore, you can't
+add or remove processing and expect it to be effective during the current merge/save/load.
+However, if you modify their internal variables it will be effective immediately.
+
+Here an example of a processing that remove the type check of a parameter in
+`ProcessTyping` processing. It is then possible for instance to force an other
+type (it is not possible otherwise).
 
 ```python
-class AddProcessList(Processing):
-    def __init__(self):
+from cliconfig.processing.builtin import ProcessTyping
+
+class ProcessBypassTyping(Processing):
+    """Bypass type check of ProcessTyping for parameters tagged with "@bypass_typing".
+
+    In pre-merge it looks for a parameter with the tag "@bypass_typing",
+    removes it and change the internal ProcessTyping variables to avoid
+    checking the type of the parameter with ProcessTyping.
+    """
+
+    def __init__(self) -> None:
         super().__init__()
-        self.process_list = [Process1(), Process2(), ...]
-        self.already_added = False
-        # Ensure that the processing trigger before all processing of the list:
-        self.premerge_order = -100.0
+        self.bypassed_forced_types: Dict[str, tuple] = {}
+        # Before ProcessTyping pre-merge to let it change the type
+        self.premerge_order = 1.0
 
     def premerge(self, flat_config: Config) -> Config:
-        if not self.already_added:
-            self.already_added = True
-            # NOTE: the order of the process list has no importance
-            flat_config.process_list += self.process_list
+        """Pre-merge processing."""
+        items = list(flat_config.dict.items())
+        for flat_key, value in items:
+            if is_tag_in(flat_key, "bypass_typing"):
+                new_key = clean_tag(flat_key, "bypass_typing")
+                flat_config.dict[new_key] = value
+                del flat_config.dict[flat_key]
+                clean_key = clean_all_tags(flat_key)
+                for processing in flat_config.process_list:
+                    if (isinstance(processing, ProcessTyping)
+                            and clean_key in processing.forced_types):
+                        forced_type = processing.forced_types.pop(clean_key)
+                        self.bypassed_forced_types[clean_key] = forced_type
         return flat_config
 
-config = make_config("main.yaml", process_list=[AddProcessList()])
+# Without bypass:
+config1 = Config({"a@type:int": 0}, [ProcessBypassTyping(), ProcessTyping()])
+config2 = Config({"a@bypass_typing@type:str": "a"}, [])
+config = merge_flat_processing(config1, config2)
+# Error: try to change the forced type of "a" from int to str
+
+# With bypass:
+config1 = Config({"a@type:int": 0}, [ProcessBypassTyping(), ProcessTyping()])
+config2 = Config({"a@bypass_typing@type:str": "a"}, [])
+config = merge_flat_processing(config1, config2)
+# No error
 ```
-
-This way you can then even create named spaces of processing to organize them.
-The processing list is dynamic, use it as you want for more advanced use cases as
-long as you know what you are doing!
```

### Comparing `cliconfig-0.5.0/docs/quickstart.md` & `cliconfig-0.5.1/docs/quickstart.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/github_actions_utils/pydocstyle_manager.py` & `cliconfig-0.5.1/github_actions_utils/pydocstyle_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/github_actions_utils/pylint_manager.py` & `cliconfig-0.5.1/github_actions_utils/pylint_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/github_actions_utils/pytest_manager.py` & `cliconfig-0.5.1/github_actions_utils/pytest_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/licenses_tier/FLATTEN_DICT_LICENSE` & `cliconfig-0.5.1/licenses_tier/FLATTEN_DICT_LICENSE`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/pre-commit-checks.sh` & `cliconfig-0.5.1/pre-commit-checks.sh`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/pyproject.toml` & `cliconfig-0.5.1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/tests/conftest.py` & `cliconfig-0.5.1/tests/conftest.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,27 +1,26 @@
 """Shared pytest fixtures."""
 from typing import Any, Dict
 
 import pytest
 
 from cliconfig.base import Config
 from cliconfig.processing.base import Processing
-from cliconfig.tag_routines import clean_all_tags, clean_tag
+from cliconfig.tag_routines import clean_all_tags, clean_tag, is_tag_in
 
 
 class ProcessAdd1(Processing):
     """Add 1 to values with tag "@add1"."""
 
     # pylint: disable=unused-argument
     def premerge(self, flat_config: Config) -> Config:
         """Pre-merge processing."""
         items = list(flat_config.dict.items())
         for flat_key, value in items:
-            end_key = flat_key.split(".")[-1]
-            if "@add1" in end_key:
+            if is_tag_in(flat_key, "add1"):
                 flat_config.dict[clean_tag(flat_key, "add1")] = value + 1
                 del flat_config.dict[flat_key]
         return flat_config
 
     def presave(self, flat_config: Config) -> Config:
         """Pre-save processing."""
         return self.premerge(flat_config)
@@ -35,16 +34,15 @@
         self.keep_vals: Dict[str, Any] = {}
 
     # pylint: disable=unused-argument
     def premerge(self, flat_config: Config) -> Config:
         """Pre-merge processing."""
         items = list(flat_config.dict.items())
         for flat_key, value in items:
-            end_key = flat_key.split(".")[-1]
-            if "@keep" in end_key:
+            if is_tag_in(flat_key, "keep"):
                 new_key = clean_tag(flat_key, "keep")
                 flat_config.dict[new_key] = value
                 del flat_config.dict[flat_key]
                 self.keep_vals[clean_all_tags(flat_key)] = value
         return flat_config
 
     # pylint: disable=unused-argument
```

### Comparing `cliconfig-0.5.0/tests/integration/test_inte_multiple_tags.py` & `cliconfig-0.5.1/tests/integration/test_inte_multiple_tags.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/tests/unit/processing/test_base.py` & `cliconfig-0.5.1/tests/unit/processing/test_base.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/tests/unit/processing/test_builtin.py` & `cliconfig-0.5.1/tests/unit/processing/test_builtin.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 
 import pytest
 import pytest_check as check
 
 from cliconfig.base import Config
 from cliconfig.dict_routines import flatten
 from cliconfig.processing.builtin import (
+    DefaultProcessings,
     ProcessCheckTags,
     ProcessCopy,
     ProcessMerge,
     ProcessTyping,
 )
 
 
@@ -240,7 +241,19 @@
             ValueError,
             match=(
                 "Keys with tags are encountered at the end of "
                 "the pre-merge process.*"
             )
         ):
             processing.premerge(Config(flat_dict, [processing]))
+
+
+def test_default_processings() -> None:
+    """Test DefaultProcessings."""
+    config = Config({}, DefaultProcessings().list)
+    for proc in [
+        ProcessCheckTags(),
+        ProcessMerge(),
+        ProcessCopy(),
+        ProcessTyping()
+    ]:
+        check.is_in(proc, config.process_list)
```

### Comparing `cliconfig-0.5.0/tests/unit/processing/test_type_parser.py` & `cliconfig-0.5.1/tests/unit/processing/test_type_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/tests/unit/test_cli_parser.py` & `cliconfig-0.5.1/tests/unit/test_cli_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/tests/unit/test_config_routines.py` & `cliconfig-0.5.1/tests/unit/test_config_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/tests/unit/test_dict_routines.py` & `cliconfig-0.5.1/tests/unit/test_dict_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/tests/unit/test_process_routines.py` & `cliconfig-0.5.1/tests/unit/test_process_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.0/tests/unit/test_tag_routines.py` & `cliconfig-0.5.1/tests/unit/test_tag_routines.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 """Test the tag routines."""
 
 import pytest
 import pytest_check as check
 
-from cliconfig.tag_routines import clean_all_tags, clean_tag, dict_clean_tags
+from cliconfig.tag_routines import clean_all_tags, clean_tag, dict_clean_tags, is_tag_in
 
 
 @pytest.fixture()
 def key1() -> str:
     """Return a key with many tags."""
     return "abc@tag.def@tag_2.ghi@tag"
 
@@ -57,7 +57,19 @@
         key1: 1,
         key2: 2,
     }
     out_dict, tagged_keys = dict_clean_tags(in_dict)
     check.equal(out_dict, {"abc.def.pqr": 0, "abc.def.ghi": 1, "abc.def.jkl.mno": 2})
     check.is_true(key1 in tagged_keys)
     check.is_true(key1 in tagged_keys)
+
+
+def test_is_tag_in() -> None:
+    """Test is_tag_in."""
+    check.is_true(is_tag_in("config.config2.config3@tag", "tag"))
+    check.is_false(is_tag_in("config.config2.config3@tag", "tog"))
+    check.is_false(is_tag_in("config.config2.config3@tag_2", "tag"))
+    check.is_false(is_tag_in("config.config2.config3@tag_2@tog", "tag"))
+    check.is_true(is_tag_in("config.config2.config3@tag@tog", "@tag"))
+    check.is_true(is_tag_in("config.config2.config3@tag@tog", "@tog"))
+    check.is_true(is_tag_in("config.config2@tag.config3@tog", "tag", full_key=True))
+    check.is_false(is_tag_in("config.config2@tag.config3@tog", "tag", full_key=False))
```

