# Comparing `tmp/cliconfig-0.5.1.tar.gz` & `tmp/cliconfig-0.5.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cliconfig-0.5.1.tar", last modified: Sat May 13 00:48:37 2023, max compression
+gzip compressed data, was "cliconfig-0.5.3.tar", last modified: Sat May 13 14:13:53 2023, max compression
```

## Comparing `cliconfig-0.5.1.tar` & `cliconfig-0.5.3.tar`

### file list

```diff
@@ -1,107 +1,107 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.coveragerc
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.219479 cliconfig-0.5.1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.223479 cliconfig-0.5.1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/flake.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/mypy.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/pipy_deployment.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/pydocstyle.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/pylint.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/ruff.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.github/workflows/tests.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.markdownlint.json
--rw-r--r--   0 runner    (1001) docker     (123)    20457 2023-05-13 00:48:19.000000 cliconfig-0.5.1/.pylintrc
--rw-r--r--   0 runner    (1001) docker     (123)     4847 2023-05-13 00:48:19.000000 cliconfig-0.5.1/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 00:48:19.000000 cliconfig-0.5.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     6788 2023-05-13 00:48:37.231479 cliconfig-0.5.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    10451 2023-05-13 00:48:19.000000 cliconfig-0.5.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     6353 2023-05-13 00:48:19.000000 cliconfig-0.5.1/README_pypi.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/cliconfig/
--rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/cli_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     7339 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/config_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)    14751 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/dict_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     8079 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/process_routines.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/cliconfig/processing/
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3118 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/_type_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1703 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/base.py
--rw-r--r--   0 runner    (1001) docker     (123)    16885 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/builtin.py
--rw-r--r--   0 runner    (1001) docker     (123)     9833 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/processing/create.py
--rw-r--r--   0 runner    (1001) docker     (123)     3032 2023-05-13 00:48:19.000000 cliconfig-0.5.1/cliconfig/tag_routines.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/cliconfig.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6788 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2363 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 00:48:37.000000 cliconfig-0.5.1/cliconfig.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.227479 cliconfig-0.5.1/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (123)     5501 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/_static/logo.png
--rw-r--r--   0 runner    (1001) docker     (123)     6203 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/_static/logo_extend.png
--rw-r--r--   0 runner    (1001) docker     (123)      507 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/cliconfig.processing.rst
--rw-r--r--   0 runner    (1001) docker     (123)      818 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/cliconfig_api.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/contribute.md
--rw-r--r--   0 runner    (1001) docker     (123)      965 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/edge_cases.md
--rw-r--r--   0 runner    (1001) docker     (123)     4827 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/installation.md
--rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/license.md
--rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/processing.md
--rw-r--r--   0 runner    (1001) docker     (123)     5006 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/quickstart.md
--rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 00:48:19.000000 cliconfig-0.5.1/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/github_actions_utils/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/color.py
--rw-r--r--   0 runner    (1001) docker     (123)      754 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/pydocstyle_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/pylint_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 00:48:19.000000 cliconfig-0.5.1/github_actions_utils/pytest_manager.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/licenses_tier/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 00:48:19.000000 cliconfig-0.5.1/licenses_tier/FLATTEN_DICT_LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1252 2023-05-13 00:48:19.000000 cliconfig-0.5.1/pre-commit-checks.sh
--rw-r--r--   0 runner    (1001) docker     (123)     2579 2023-05-13 00:48:19.000000 cliconfig-0.5.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 00:48:19.000000 cliconfig-0.5.1/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 00:48:19.000000 cliconfig-0.5.1/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 00:48:37.231479 cliconfig-0.5.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 00:48:19.000000 cliconfig-0.5.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/configs/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/config1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/config2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/configtag1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/configtag2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/default1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/default2.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/configs/integration/
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/integration/main.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/integration/sub1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       31 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/integration/sub2.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/configs/merge/
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/additional1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/additional2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/additional3.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/default1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/default2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/configs/merge/default3.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/integration/
--rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/integration/test_inte_multiple_tags.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/unit/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 00:48:37.231479 cliconfig-0.5.1/tests/unit/processing/
--rw-r--r--   0 runner    (1001) docker     (123)      932 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/processing/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     8624 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/processing/test_builtin.py
--rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/processing/test_create.py
--rw-r--r--   0 runner    (1001) docker     (123)     1294 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/processing/test_type_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_cli_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_config_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     5808 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_dict_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     4779 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_ex_docs.py
--rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_process_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     2181 2023-05-13 00:48:19.000000 cliconfig-0.5.1/tests/unit/test_tag_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.813057 cliconfig-0.5.3/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.coveragerc
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.777057 cliconfig-0.5.3/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.789057 cliconfig-0.5.3/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.github/workflows/flake.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.github/workflows/mypy.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.github/workflows/pipy_deployment.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.github/workflows/pydocstyle.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.github/workflows/pylint.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.github/workflows/ruff.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.github/workflows/tests.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.markdownlint.json
+-rw-r--r--   0 runner    (1001) docker     (123)    20457 2023-05-13 14:13:24.000000 cliconfig-0.5.3/.pylintrc
+-rw-r--r--   0 runner    (1001) docker     (123)     4847 2023-05-13 14:13:24.000000 cliconfig-0.5.3/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 14:13:24.000000 cliconfig-0.5.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     6788 2023-05-13 14:13:53.813057 cliconfig-0.5.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    10509 2023-05-13 14:13:24.000000 cliconfig-0.5.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     6353 2023-05-13 14:13:24.000000 cliconfig-0.5.3/README_pypi.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.793057 cliconfig-0.5.3/cliconfig/
+-rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 14:13:53.000000 cliconfig-0.5.3/cliconfig/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/cli_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7339 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/config_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14751 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/dict_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8079 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/process_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.797057 cliconfig-0.5.3/cliconfig/processing/
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/processing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5367 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/processing/_type_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1703 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/processing/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16899 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/processing/builtin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9833 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/processing/create.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3032 2023-05-13 14:13:24.000000 cliconfig-0.5.3/cliconfig/tag_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.793057 cliconfig-0.5.3/cliconfig.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6788 2023-05-13 14:13:53.000000 cliconfig-0.5.3/cliconfig.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2363 2023-05-13 14:13:53.000000 cliconfig-0.5.3/cliconfig.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:13:53.000000 cliconfig-0.5.3/cliconfig.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 14:13:53.000000 cliconfig-0.5.3/cliconfig.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 14:13:53.000000 cliconfig-0.5.3/cliconfig.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.801057 cliconfig-0.5.3/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.801057 cliconfig-0.5.3/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)     5501 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/_static/logo.png
+-rw-r--r--   0 runner    (1001) docker     (123)     6203 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/_static/logo_extend.png
+-rw-r--r--   0 runner    (1001) docker     (123)      507 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/cliconfig.processing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      818 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/cliconfig_api.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/contribute.md
+-rw-r--r--   0 runner    (1001) docker     (123)      965 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/edge_cases.md
+-rw-r--r--   0 runner    (1001) docker     (123)     4827 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/installation.md
+-rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/license.md
+-rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/processing.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5064 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/quickstart.md
+-rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 14:13:24.000000 cliconfig-0.5.3/docs/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.805057 cliconfig-0.5.3/github_actions_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 14:13:24.000000 cliconfig-0.5.3/github_actions_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-13 14:13:24.000000 cliconfig-0.5.3/github_actions_utils/color.py
+-rw-r--r--   0 runner    (1001) docker     (123)      754 2023-05-13 14:13:24.000000 cliconfig-0.5.3/github_actions_utils/pydocstyle_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-13 14:13:24.000000 cliconfig-0.5.3/github_actions_utils/pylint_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 14:13:24.000000 cliconfig-0.5.3/github_actions_utils/pytest_manager.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.805057 cliconfig-0.5.3/licenses_tier/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 14:13:24.000000 cliconfig-0.5.3/licenses_tier/FLATTEN_DICT_LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1252 2023-05-13 14:13:24.000000 cliconfig-0.5.3/pre-commit-checks.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     2579 2023-05-13 14:13:24.000000 cliconfig-0.5.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 14:13:24.000000 cliconfig-0.5.3/requirements-dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 14:13:24.000000 cliconfig-0.5.3/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:13:53.813057 cliconfig-0.5.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 14:13:24.000000 cliconfig-0.5.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.805057 cliconfig-0.5.3/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.805057 cliconfig-0.5.3/tests/configs/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/config1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/config2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/configtag1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/configtag2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/default1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/default2.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.809057 cliconfig-0.5.3/tests/configs/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/integration/main.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/integration/sub1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/integration/sub2.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.809057 cliconfig-0.5.3/tests/configs/merge/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/merge/additional1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/merge/additional2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/merge/additional3.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/merge/default1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/merge/default2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/configs/merge/default3.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.809057 cliconfig-0.5.3/tests/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/integration/test_inte_multiple_tags.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.813057 cliconfig-0.5.3/tests/unit/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:13:53.813057 cliconfig-0.5.3/tests/unit/processing/
+-rw-r--r--   0 runner    (1001) docker     (123)      932 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/processing/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8818 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/processing/test_builtin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/processing/test_create.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3969 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/processing/test_type_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/test_cli_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/test_config_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5808 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/test_dict_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4779 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/test_ex_docs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/test_process_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2181 2023-05-13 14:13:24.000000 cliconfig-0.5.3/tests/unit/test_tag_routines.py
```

### Comparing `cliconfig-0.5.1/.github/workflows/pipy_deployment.yaml` & `cliconfig-0.5.3/.github/workflows/pipy_deployment.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/.github/workflows/pydocstyle.yaml` & `cliconfig-0.5.3/.github/workflows/pydocstyle.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/.github/workflows/pylint.yaml` & `cliconfig-0.5.3/.github/workflows/pylint.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/.github/workflows/tests.yaml` & `cliconfig-0.5.3/.github/workflows/tests.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/.pylintrc` & `cliconfig-0.5.3/.pylintrc`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/CONTRIBUTING.md` & `cliconfig-0.5.3/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/LICENSE` & `cliconfig-0.5.3/LICENSE`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/PKG-INFO` & `cliconfig-0.5.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cliconfig
-Version: 0.5.1
+Version: 0.5.3
 Summary: Merge your config files and set parameters from the command line in a simple way.
 Author-email: Valentin Goldite <valentin.goldite@gmail.com>
 Project-URL: Source, https://github.com/valentingol/cliconfig
 Keywords: logging,machine,learning
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
```

### Comparing `cliconfig-0.5.1/README.md` & `cliconfig-0.5.3/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -138,15 +138,16 @@
   is not guaranteed as it depends on the order of the tags in the configuration file.
 * `@copy`: This tag copies a parameter from another key. The value should be a string
   that represents the flattened key. The copied value is then protected from further
   updates but will be updated if the copied key change during a merge.
 * `@type:<my type>`: This tag checks if the key matches the specified type `<my type>`
    after each update, even if the tag is no longer present. It supports basic types
    (except for tuples and sets, which are not handled by YAML) as well as unions
-   (using "Union" or "|"), optional values, lists, and dictionaries.
+   (using "Union" or "|"), optional values, nested list, and nested dict.
+   For instance: `@type:List[Dict[str, int|float]]`.
 
 The tags are applied in the following order: `@merge`, `@copy`, and then `@type`.
 
 Please note that the tags serve as triggers for internal processing and will be
 automatically removed from the key after processing.
 
 It is also possible to combine multiple tags. For example:
@@ -237,15 +238,15 @@
 Secondary:
 
 * [x] add `make_processing_keep_property` to make a processing that keep the
   property of a parameter across merged configs. The property is any python object
   returned by a function that takes the parameter as input
 * [ ] add `ProcessSelect` (with tag "@select") to select a subconfig (or parameter)
   and delete the others configs at the same level (to cure the resulting config)
-* [ ] allow nested types in `ProcessTyping`
+* [x] allow nested types in `ProcessTyping`
 * [x] add DefaultProcessings that stores default processing as list of processing
 
 ## License
 
 Copyright (C) 2023  Valentin Goldité
 
 This program is free software: you can redistribute it and/or modify it under the
```

### Comparing `cliconfig-0.5.1/README_pypi.md` & `cliconfig-0.5.3/README_pypi.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig/__init__.py` & `cliconfig-0.5.3/cliconfig/__init__.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig/cli_parser.py` & `cliconfig-0.5.3/cliconfig/cli_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig/config_routines.py` & `cliconfig-0.5.3/cliconfig/config_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig/dict_routines.py` & `cliconfig-0.5.3/cliconfig/dict_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig/process_routines.py` & `cliconfig-0.5.3/cliconfig/process_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig/processing/base.py` & `cliconfig-0.5.3/cliconfig/processing/base.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig/processing/builtin.py` & `cliconfig-0.5.3/cliconfig/processing/builtin.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 from typing import Any, Dict, List
 
 from cliconfig.base import Config
 from cliconfig.process_routines import (
     merge_flat_paths_processing,
     merge_flat_processing,
 )
-from cliconfig.processing._type_parser import _parse_type
+from cliconfig.processing._type_parser import _isinstance, _parse_type
 from cliconfig.processing.base import Processing
 from cliconfig.tag_routines import clean_all_tags, clean_tag, dict_clean_tags, is_tag_in
 
 
 class ProcessMerge(Processing):
     """Merge dicts just in time with '@merge_after/_before/_add' tags.
 
@@ -315,15 +315,15 @@
                 self.type_desc[clean_key] = type_desc
         return flat_config
 
     def postmerge(self, flat_config: Config) -> Config:
         """Post-merge processing."""
         for key, expected_type in self.forced_types.items():
             if (key in flat_config.dict
-                    and not isinstance(flat_config.dict[key], expected_type)):
+                    and not _isinstance(flat_config.dict[key], expected_type)):
                 type_desc = self.type_desc[key]
                 raise ValueError(
                     f"Key previously tagged with '@type:{type_desc}' must be "
                     f"associated to a value of type {type_desc}. Find the "
                     f"value: {flat_config.dict[key]} of type "
                     f"{type(flat_config.dict[key])} at key: {key}"
                 )
```

### Comparing `cliconfig-0.5.1/cliconfig/processing/create.py` & `cliconfig-0.5.3/cliconfig/processing/create.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig/tag_routines.py` & `cliconfig-0.5.3/cliconfig/tag_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/cliconfig.egg-info/PKG-INFO` & `cliconfig-0.5.3/cliconfig.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cliconfig
-Version: 0.5.1
+Version: 0.5.3
 Summary: Merge your config files and set parameters from the command line in a simple way.
 Author-email: Valentin Goldite <valentin.goldite@gmail.com>
 Project-URL: Source, https://github.com/valentingol/cliconfig
 Keywords: logging,machine,learning
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
```

### Comparing `cliconfig-0.5.1/cliconfig.egg-info/SOURCES.txt` & `cliconfig-0.5.3/cliconfig.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/Makefile` & `cliconfig-0.5.3/docs/Makefile`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/_static/logo.png` & `cliconfig-0.5.3/docs/_static/logo.png`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/_static/logo_extend.png` & `cliconfig-0.5.3/docs/_static/logo_extend.png`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/cliconfig_api.rst` & `cliconfig-0.5.3/docs/cliconfig_api.rst`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/conf.py` & `cliconfig-0.5.3/docs/conf.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/edge_cases.md` & `cliconfig-0.5.3/docs/edge_cases.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/index.rst` & `cliconfig-0.5.3/docs/index.rst`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/license.md` & `cliconfig-0.5.3/docs/license.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/make.bat` & `cliconfig-0.5.3/docs/make.bat`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/processing.md` & `cliconfig-0.5.3/docs/processing.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/docs/quickstart.md` & `cliconfig-0.5.3/docs/quickstart.md`

 * *Files 9% similar despite different names*

```diff
@@ -97,15 +97,16 @@
   is not guaranteed as it depends on the order of the tags in the configuration file.
 * `@copy`: This tag copies a parameter from another key. The value should be a string
   that represents the flattened key. The copied value is then protected from further
   updates but will be updated if the copied key change during a merge.
 * `@type:<my type>`: This tag checks if the key matches the specified type `<my type>`
    after each update, even if the tag is no longer present. It supports basic types
    (except for tuples and sets, which are not handled by YAML) as well as unions
-   (using "Union" or "|"), optional values, lists, and dictionaries.
+   (using "Union" or "|"), optional values, nested list, and nested dict.
+   For instance: `@type:List[Dict[str, int|float]]`.
 
 The tags are applied in the following order: `@merge`, `@copy`, and then `@type`.
 
 Please note that the tags serve as triggers for internal processing and will be
 automatically removed from the key after processing.
 
 It is also possible to combine multiple tags. For example:
```

### Comparing `cliconfig-0.5.1/github_actions_utils/pydocstyle_manager.py` & `cliconfig-0.5.3/github_actions_utils/pydocstyle_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/github_actions_utils/pylint_manager.py` & `cliconfig-0.5.3/github_actions_utils/pylint_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/github_actions_utils/pytest_manager.py` & `cliconfig-0.5.3/github_actions_utils/pytest_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/licenses_tier/FLATTEN_DICT_LICENSE` & `cliconfig-0.5.3/licenses_tier/FLATTEN_DICT_LICENSE`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/pre-commit-checks.sh` & `cliconfig-0.5.3/pre-commit-checks.sh`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/pyproject.toml` & `cliconfig-0.5.3/pyproject.toml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/conftest.py` & `cliconfig-0.5.3/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/integration/test_inte_multiple_tags.py` & `cliconfig-0.5.3/tests/integration/test_inte_multiple_tags.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/unit/processing/test_base.py` & `cliconfig-0.5.3/tests/unit/processing/test_base.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/unit/processing/test_builtin.py` & `cliconfig-0.5.3/tests/unit/processing/test_builtin.py`

 * *Files 3% similar despite different names*

```diff
@@ -167,35 +167,41 @@
 
 
 def test_process_typing() -> None:
     """Test ProcessTyping."""
     processing = ProcessTyping()
     flat_dict = {
         "param1@type:int": 1,
-        "param2@type:List|Dict": [0.0],
+        "param2@type:List[Optional[Dict[str, int|float]]]": [{'a': [0.0]}],
     }
     flat_config = Config(flat_dict, [processing])
     flat_config = processing.premerge(flat_config)
     flat_config.dict['param1'] = 3
-    flat_config.dict['param2'] = {'a': None, 'b': 1}
+    flat_config.dict['param2'] = {'a': None, 'b': [{'c': 1}]}
     flat_config.dict = flatten(flat_config.dict)
     flat_config = processing.postmerge(flat_config)
-    check.equal(flat_config.dict, {"param1": 3, "param2.a": None, "param2.b": 1})
+    check.equal(
+        flat_config.dict,
+        {"param1": 3, "param2.a": None, "param2.b": [{'c': 1}]}
+    )
     check.equal(
         flat_config.process_list[0].forced_types,  # type: ignore
-        {"param1": (int, ), "param2": (list, dict)}
+        {
+            "param1": (int, ),
+            "param2": (('list', ((type(None), ('dict', (str,), (int, float))),)),)
+        }
     )
     check.equal(
         flat_config.process_list[0].type_desc,  # type: ignore
-        {"param1": "int", "param2": "List|Dict"}
+        {"param1": "int", "param2": "List[Optional[Dict[str, int|float]]]"}
     )
     flat_config = processing.presave(flat_config)
     check.equal(
         flat_config.dict,
-        {"param1@type:int": 3, "param2.a": None, "param2.b": 1}
+        {"param1@type:int": 3, "param2.a": None, "param2.b": [{'c': 1}]}
     )
     processing.forced_types = {}  # Reset forced types
     processing.type_desc = {}  # Reset type description
 
     # Case of different type on pre-merge: do not raise error!
     processing.premerge(Config({"param@type:int": "str"}, [processing]))
```

### Comparing `cliconfig-0.5.1/tests/unit/processing/test_create.py` & `cliconfig-0.5.3/tests/unit/processing/test_create.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/unit/test_cli_parser.py` & `cliconfig-0.5.3/tests/unit/test_cli_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/unit/test_config_routines.py` & `cliconfig-0.5.3/tests/unit/test_config_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/unit/test_dict_routines.py` & `cliconfig-0.5.3/tests/unit/test_dict_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/unit/test_ex_docs.py` & `cliconfig-0.5.3/tests/unit/test_ex_docs.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/unit/test_process_routines.py` & `cliconfig-0.5.3/tests/unit/test_process_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.1/tests/unit/test_tag_routines.py` & `cliconfig-0.5.3/tests/unit/test_tag_routines.py`

 * *Files identical despite different names*

