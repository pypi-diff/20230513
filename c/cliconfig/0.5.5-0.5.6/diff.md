# Comparing `tmp/cliconfig-0.5.5.tar.gz` & `tmp/cliconfig-0.5.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cliconfig-0.5.5.tar", last modified: Sat May 13 16:24:28 2023, max compression
+gzip compressed data, was "cliconfig-0.5.6.tar", last modified: Sat May 13 17:09:52 2023, max compression
```

## Comparing `cliconfig-0.5.5.tar` & `cliconfig-0.5.6.tar`

### file list

```diff
@@ -1,107 +1,107 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.coveragerc
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.124336 cliconfig-0.5.5/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.128336 cliconfig-0.5.5/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/flake.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/mypy.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/pipy_deployment.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/pydocstyle.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/pylint.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/ruff.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/tests.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.markdownlint.json
--rw-r--r--   0 runner    (1001) docker     (123)    20457 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.pylintrc
--rw-r--r--   0 runner    (1001) docker     (123)     4847 2023-05-13 16:24:02.000000 cliconfig-0.5.5/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 16:24:02.000000 cliconfig-0.5.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     7003 2023-05-13 16:24:28.136336 cliconfig-0.5.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    11023 2023-05-13 16:24:02.000000 cliconfig-0.5.5/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     6568 2023-05-13 16:24:02.000000 cliconfig-0.5.5/README_pypi.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.128336 cliconfig-0.5.5/cliconfig/
--rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/cli_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     7339 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/config_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)    14751 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/dict_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     8079 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/process_routines.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/cliconfig/processing/
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5350 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/_type_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1703 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/base.py
--rw-r--r--   0 runner    (1001) docker     (123)    22217 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/builtin.py
--rw-r--r--   0 runner    (1001) docker     (123)     9833 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/create.py
--rw-r--r--   0 runner    (1001) docker     (123)     3074 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/tag_routines.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.128336 cliconfig-0.5.5/cliconfig.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     7003 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2363 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (123)     5501 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/_static/logo.png
--rw-r--r--   0 runner    (1001) docker     (123)     6203 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/_static/logo_extend.png
--rw-r--r--   0 runner    (1001) docker     (123)      507 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/cliconfig.processing.rst
--rw-r--r--   0 runner    (1001) docker     (123)      818 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/cliconfig_api.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/contribute.md
--rw-r--r--   0 runner    (1001) docker     (123)     1110 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/edge_cases.md
--rw-r--r--   0 runner    (1001) docker     (123)     5068 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/installation.md
--rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/license.md
--rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/processing.md
--rw-r--r--   0 runner    (1001) docker     (123)     5380 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/quickstart.md
--rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/github_actions_utils/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/color.py
--rw-r--r--   0 runner    (1001) docker     (123)      754 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/pydocstyle_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/pylint_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/pytest_manager.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/licenses_tier/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 16:24:02.000000 cliconfig-0.5.5/licenses_tier/FLATTEN_DICT_LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1252 2023-05-13 16:24:02.000000 cliconfig-0.5.5/pre-commit-checks.sh
--rw-r--r--   0 runner    (1001) docker     (123)     2579 2023-05-13 16:24:02.000000 cliconfig-0.5.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 16:24:02.000000 cliconfig-0.5.5/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 16:24:02.000000 cliconfig-0.5.5/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 16:24:28.136336 cliconfig-0.5.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 16:24:02.000000 cliconfig-0.5.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/tests/configs/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/config1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/config2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/configtag1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/configtag2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/default1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/default2.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/tests/configs/integration/
--rw-r--r--   0 runner    (1001) docker     (123)      152 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/integration/main.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/integration/sub1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/integration/sub2.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/tests/configs/merge/
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/additional1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/additional2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/additional3.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/default1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/default2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/default3.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/tests/integration/
--rw-r--r--   0 runner    (1001) docker     (123)     1156 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/integration/test_inte_multiple_tags.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/tests/unit/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/tests/unit/processing/
--rw-r--r--   0 runner    (1001) docker     (123)      932 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/processing/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)    10858 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/processing/test_builtin.py
--rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/processing/test_create.py
--rw-r--r--   0 runner    (1001) docker     (123)     3969 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/processing/test_type_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_cli_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_config_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     5808 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_dict_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     4779 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_ex_docs.py
--rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_process_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     2181 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_tag_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.914167 cliconfig-0.5.6/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.coveragerc
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.902167 cliconfig-0.5.6/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.906167 cliconfig-0.5.6/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.github/workflows/flake.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.github/workflows/mypy.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.github/workflows/pipy_deployment.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.github/workflows/pydocstyle.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.github/workflows/pylint.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.github/workflows/ruff.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.github/workflows/tests.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.markdownlint.json
+-rw-r--r--   0 runner    (1001) docker     (123)    20457 2023-05-13 17:09:36.000000 cliconfig-0.5.6/.pylintrc
+-rw-r--r--   0 runner    (1001) docker     (123)     4847 2023-05-13 17:09:36.000000 cliconfig-0.5.6/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 17:09:36.000000 cliconfig-0.5.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     7058 2023-05-13 17:09:52.914167 cliconfig-0.5.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    11078 2023-05-13 17:09:36.000000 cliconfig-0.5.6/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     6623 2023-05-13 17:09:36.000000 cliconfig-0.5.6/README_pypi.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.906167 cliconfig-0.5.6/cliconfig/
+-rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 17:09:52.000000 cliconfig-0.5.6/cliconfig/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/cli_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7339 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/config_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14751 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/dict_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8079 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/process_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.906167 cliconfig-0.5.6/cliconfig/processing/
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/processing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5350 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/processing/_type_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1703 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/processing/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22217 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/processing/builtin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9833 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/processing/create.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3074 2023-05-13 17:09:36.000000 cliconfig-0.5.6/cliconfig/tag_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.906167 cliconfig-0.5.6/cliconfig.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     7058 2023-05-13 17:09:52.000000 cliconfig-0.5.6/cliconfig.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2363 2023-05-13 17:09:52.000000 cliconfig-0.5.6/cliconfig.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:09:52.000000 cliconfig-0.5.6/cliconfig.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 17:09:52.000000 cliconfig-0.5.6/cliconfig.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 17:09:52.000000 cliconfig-0.5.6/cliconfig.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)     5501 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/_static/logo.png
+-rw-r--r--   0 runner    (1001) docker     (123)     6203 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/_static/logo_extend.png
+-rw-r--r--   0 runner    (1001) docker     (123)      507 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/cliconfig.processing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      818 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/cliconfig_api.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/contribute.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1110 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/edge_cases.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5128 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/installation.md
+-rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/license.md
+-rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/processing.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5435 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/quickstart.md
+-rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 17:09:36.000000 cliconfig-0.5.6/docs/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/github_actions_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 17:09:36.000000 cliconfig-0.5.6/github_actions_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-13 17:09:36.000000 cliconfig-0.5.6/github_actions_utils/color.py
+-rw-r--r--   0 runner    (1001) docker     (123)      754 2023-05-13 17:09:36.000000 cliconfig-0.5.6/github_actions_utils/pydocstyle_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-13 17:09:36.000000 cliconfig-0.5.6/github_actions_utils/pylint_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 17:09:36.000000 cliconfig-0.5.6/github_actions_utils/pytest_manager.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/licenses_tier/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 17:09:36.000000 cliconfig-0.5.6/licenses_tier/FLATTEN_DICT_LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1252 2023-05-13 17:09:36.000000 cliconfig-0.5.6/pre-commit-checks.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     2579 2023-05-13 17:09:36.000000 cliconfig-0.5.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 17:09:36.000000 cliconfig-0.5.6/requirements-dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 17:09:36.000000 cliconfig-0.5.6/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 17:09:52.914167 cliconfig-0.5.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 17:09:36.000000 cliconfig-0.5.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/tests/configs/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/config1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/config2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/configtag1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/configtag2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/default1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/default2.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/tests/configs/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)      152 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/integration/main.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/integration/sub1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/integration/sub2.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/tests/configs/merge/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/merge/additional1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/merge/additional2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/merge/additional3.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/merge/default1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/merge/default2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/configs/merge/default3.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/tests/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)     1156 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/integration/test_inte_multiple_tags.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.910167 cliconfig-0.5.6/tests/unit/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:09:52.914167 cliconfig-0.5.6/tests/unit/processing/
+-rw-r--r--   0 runner    (1001) docker     (123)      932 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/processing/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10901 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/processing/test_builtin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/processing/test_create.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3969 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/processing/test_type_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/test_cli_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/test_config_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5808 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/test_dict_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4779 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/test_ex_docs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/test_process_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2181 2023-05-13 17:09:36.000000 cliconfig-0.5.6/tests/unit/test_tag_routines.py
```

### Comparing `cliconfig-0.5.5/.github/workflows/pipy_deployment.yaml` & `cliconfig-0.5.6/.github/workflows/pipy_deployment.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/.github/workflows/pydocstyle.yaml` & `cliconfig-0.5.6/.github/workflows/pydocstyle.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/.github/workflows/pylint.yaml` & `cliconfig-0.5.6/.github/workflows/pylint.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/.github/workflows/tests.yaml` & `cliconfig-0.5.6/.github/workflows/tests.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/.pylintrc` & `cliconfig-0.5.6/.pylintrc`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/CONTRIBUTING.md` & `cliconfig-0.5.6/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/LICENSE` & `cliconfig-0.5.6/LICENSE`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/PKG-INFO` & `cliconfig-0.5.6/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cliconfig
-Version: 0.5.5
+Version: 0.5.6
 Summary: Merge your config files and set parameters from the command line in a simple way.
 Author-email: Valentin Goldite <valentin.goldite@gmail.com>
 Project-URL: Source, https://github.com/valentingol/cliconfig
 Keywords: logging,machine,learning
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
@@ -90,15 +90,15 @@
 ---  # main.yaml
 path_1@merge_add: sub1.yaml
 path_2@merge_add: sub2.yaml
 config3.select@select: "config3.param1"
 
 --- # sub1.yaml
 config1:
-  param@copy@type:int: config2.param2
+  param@copy@type:int: config2.param
   param2@type:int: 1
 
 --- # sub2.yaml
 config2.param@type:None|int: 2
 config3:
   param1: 0
   param2: 1
@@ -106,25 +106,26 @@
 
 Here `main.yaml` is interpreted like:
 
 ```yaml
 path_1: sub1.yaml
 path_2: sub2.yaml
 config1:
-  param: 2  # the value of config2.param2
+  param: 2  # the value of config2.param
   param2: 1
 config2:
   param: 2
 config3:
   select: "config3.param1"
   param1: 0
+  # param2 is deleted because it is not in the selection
 ```
 
 Then, all the parameters in `config1` and `config2` have enforced types
-(`config1.param` can also be None) and changing `config2.param` will also update
+(`config2.param` can also be None) and changing `config2.param` will also update
 `config1.param` accordingly (which is protected by direct update).
 
 See [*Processing*](https://cliconfig.readthedocs.io/en/stable/processing.html) section
 of the documentation for details on processing and how to create your own.
 
 ## How to contribute
```

### Comparing `cliconfig-0.5.5/README.md` & `cliconfig-0.5.6/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -159,15 +159,15 @@
 ---  # main.yaml
 path_1@merge_add: sub1.yaml
 path_2@merge_add: sub2.yaml
 config3.select@select: "config3.param1"
 
 --- # sub1.yaml
 config1:
-  param@copy@type:int: config2.param2
+  param@copy@type:int: config2.param
   param2@type:int: 1
 
 --- # sub2.yaml
 config2.param@type:None|int: 2
 config3:
   param1: 0
   param2: 1
@@ -175,25 +175,26 @@
 
 Here `main.yaml` is interpreted like:
 
 ```yaml
 path_1: sub1.yaml
 path_2: sub2.yaml
 config1:
-  param: 2  # the value of config2.param2
+  param: 2  # the value of config2.param
   param2: 1
 config2:
   param: 2
 config3:
   select: "config3.param1"
   param1: 0
+  # param2 is deleted because it is not in the selection
 ```
 
 Then, all the parameters in `config1` and `config2` have enforced types
-(`config1.param` can also be None) and changing `config2.param` will also update
+(`config2.param` can also be None) and changing `config2.param` will also update
 `config1.param` accordingly (which is protected by direct update).
 
 These side effects are not visible in the config but stored on processing classes.
 They are objects that find the tags, remove them from config and apply a modification.
 These processing are powerful tools that can be used to highly customize the
 configuration process.
```

### Comparing `cliconfig-0.5.5/README_pypi.md` & `cliconfig-0.5.6/README_pypi.md`

 * *Files 4% similar despite different names*

```diff
@@ -78,15 +78,15 @@
 ---  # main.yaml
 path_1@merge_add: sub1.yaml
 path_2@merge_add: sub2.yaml
 config3.select@select: "config3.param1"
 
 --- # sub1.yaml
 config1:
-  param@copy@type:int: config2.param2
+  param@copy@type:int: config2.param
   param2@type:int: 1
 
 --- # sub2.yaml
 config2.param@type:None|int: 2
 config3:
   param1: 0
   param2: 1
@@ -94,25 +94,26 @@
 
 Here `main.yaml` is interpreted like:
 
 ```yaml
 path_1: sub1.yaml
 path_2: sub2.yaml
 config1:
-  param: 2  # the value of config2.param2
+  param: 2  # the value of config2.param
   param2: 1
 config2:
   param: 2
 config3:
   select: "config3.param1"
   param1: 0
+  # param2 is deleted because it is not in the selection
 ```
 
 Then, all the parameters in `config1` and `config2` have enforced types
-(`config1.param` can also be None) and changing `config2.param` will also update
+(`config2.param` can also be None) and changing `config2.param` will also update
 `config1.param` accordingly (which is protected by direct update).
 
 See [*Processing*](https://cliconfig.readthedocs.io/en/stable/processing.html) section
 of the documentation for details on processing and how to create your own.
 
 ## How to contribute
```

### Comparing `cliconfig-0.5.5/cliconfig/__init__.py` & `cliconfig-0.5.6/cliconfig/__init__.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/cli_parser.py` & `cliconfig-0.5.6/cliconfig/cli_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/config_routines.py` & `cliconfig-0.5.6/cliconfig/config_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/dict_routines.py` & `cliconfig-0.5.6/cliconfig/dict_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/process_routines.py` & `cliconfig-0.5.6/cliconfig/process_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/processing/_type_parser.py` & `cliconfig-0.5.6/cliconfig/processing/_type_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/processing/base.py` & `cliconfig-0.5.6/cliconfig/processing/base.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/processing/builtin.py` & `cliconfig-0.5.6/cliconfig/processing/builtin.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/processing/create.py` & `cliconfig-0.5.6/cliconfig/processing/create.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig/tag_routines.py` & `cliconfig-0.5.6/cliconfig/tag_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/cliconfig.egg-info/PKG-INFO` & `cliconfig-0.5.6/cliconfig.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cliconfig
-Version: 0.5.5
+Version: 0.5.6
 Summary: Merge your config files and set parameters from the command line in a simple way.
 Author-email: Valentin Goldite <valentin.goldite@gmail.com>
 Project-URL: Source, https://github.com/valentingol/cliconfig
 Keywords: logging,machine,learning
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
@@ -90,15 +90,15 @@
 ---  # main.yaml
 path_1@merge_add: sub1.yaml
 path_2@merge_add: sub2.yaml
 config3.select@select: "config3.param1"
 
 --- # sub1.yaml
 config1:
-  param@copy@type:int: config2.param2
+  param@copy@type:int: config2.param
   param2@type:int: 1
 
 --- # sub2.yaml
 config2.param@type:None|int: 2
 config3:
   param1: 0
   param2: 1
@@ -106,25 +106,26 @@
 
 Here `main.yaml` is interpreted like:
 
 ```yaml
 path_1: sub1.yaml
 path_2: sub2.yaml
 config1:
-  param: 2  # the value of config2.param2
+  param: 2  # the value of config2.param
   param2: 1
 config2:
   param: 2
 config3:
   select: "config3.param1"
   param1: 0
+  # param2 is deleted because it is not in the selection
 ```
 
 Then, all the parameters in `config1` and `config2` have enforced types
-(`config1.param` can also be None) and changing `config2.param` will also update
+(`config2.param` can also be None) and changing `config2.param` will also update
 `config1.param` accordingly (which is protected by direct update).
 
 See [*Processing*](https://cliconfig.readthedocs.io/en/stable/processing.html) section
 of the documentation for details on processing and how to create your own.
 
 ## How to contribute
```

### Comparing `cliconfig-0.5.5/cliconfig.egg-info/SOURCES.txt` & `cliconfig-0.5.6/cliconfig.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/Makefile` & `cliconfig-0.5.6/docs/Makefile`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/_static/logo.png` & `cliconfig-0.5.6/docs/_static/logo.png`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/_static/logo_extend.png` & `cliconfig-0.5.6/docs/_static/logo_extend.png`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/cliconfig_api.rst` & `cliconfig-0.5.6/docs/cliconfig_api.rst`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/conf.py` & `cliconfig-0.5.6/docs/conf.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/edge_cases.md` & `cliconfig-0.5.6/docs/edge_cases.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/index.rst` & `cliconfig-0.5.6/docs/index.rst`

 * *Files 3% similar despite different names*

```diff
@@ -75,24 +75,25 @@
 Here `main.yaml` will be interpreted like:
 
 .. code:: yaml
 
     path_1: sub1.yaml
     path_2: sub2.yaml
     config1:
-      param: 2  # the value of config2.param2
+      param: 2  # the value of config2.param
       param2: 1
     config2:
       param: 2
     config3:
       select: "config3.param1"
       param1: 0
+      # param2 is deleted because it is not in the selection
 
 Then, all the parameters in `config1` and `config2` have enforced types
-(`config1.param` can also be None) and changing `config2.param` will also update
+(`config2.param` can also be None) and changing `config2.param` will also update
 `config1.param` accordingly (which is protected by direct update).
 
 See *Quickstart* section for more details and *Processing* section for advanced usage.
 
 .. |PyPI version| image:: https://img.shields.io/github/v/tag/valentingol/cliconfig?label=Pypi&logo=pypi&logoColor=yellow
    :target: https://pypi.org/project/cliconfig/
 .. |PythonVersion| image:: https://img.shields.io/badge/Python-3.7%20%7E%203.11-informational
```

### Comparing `cliconfig-0.5.5/docs/license.md` & `cliconfig-0.5.6/docs/license.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/make.bat` & `cliconfig-0.5.6/docs/make.bat`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/processing.md` & `cliconfig-0.5.6/docs/processing.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/docs/quickstart.md` & `cliconfig-0.5.6/docs/quickstart.md`

 * *Files 2% similar despite different names*

```diff
@@ -118,15 +118,15 @@
 ---  # main.yaml
 path_1@merge_add: sub1.yaml
 path_2@merge_add: sub2.yaml
 config3.select@select: "config3.param1"
 
 --- # sub1.yaml
 config1:
-  param@copy@type:int: config2.param2
+  param@copy@type:int: config2.param
   param2@type:int: 1
 
 --- # sub2.yaml
 config2.param@type:None|int: 2
 config3:
   param1: 0
   param2: 1
@@ -134,21 +134,22 @@
 
 Here `main.yaml` is interpreted like:
 
 ```yaml
 path_1: sub1.yaml
 path_2: sub2.yaml
 config1:
-  param: 2  # the value of config2.param2
+  param: 2  # the value of config2.param
   param2: 1
 config2:
   param: 2
 config3:
   select: "config3.param1"
   param1: 0
+  # param2 is deleted because it is not in the selection
 ```
 
 Then, all the parameters in `config1` and `config2` have enforced types
 (`config1.param` can also be None) and changing `config2.param` will also update
 `config1.param` accordingly (which is protected by direct update).
 
 These side effects are not visible in the config but stored on processing classes.
```

### Comparing `cliconfig-0.5.5/github_actions_utils/pydocstyle_manager.py` & `cliconfig-0.5.6/github_actions_utils/pydocstyle_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/github_actions_utils/pylint_manager.py` & `cliconfig-0.5.6/github_actions_utils/pylint_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/github_actions_utils/pytest_manager.py` & `cliconfig-0.5.6/github_actions_utils/pytest_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/licenses_tier/FLATTEN_DICT_LICENSE` & `cliconfig-0.5.6/licenses_tier/FLATTEN_DICT_LICENSE`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/pre-commit-checks.sh` & `cliconfig-0.5.6/pre-commit-checks.sh`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/pyproject.toml` & `cliconfig-0.5.6/pyproject.toml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/conftest.py` & `cliconfig-0.5.6/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/integration/test_inte_multiple_tags.py` & `cliconfig-0.5.6/tests/integration/test_inte_multiple_tags.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/processing/test_base.py` & `cliconfig-0.5.6/tests/unit/processing/test_base.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/processing/test_builtin.py` & `cliconfig-0.5.6/tests/unit/processing/test_builtin.py`

 * *Files 2% similar despite different names*

```diff
@@ -107,21 +107,22 @@
     }
     flat_config = Config(flat_dict, [processing])
     flat_config = processing.premerge(flat_config)
     check.equal(
         flat_config.dict,
         {"config1.param1": 1, "config2.param2": 'config1.param1'}
     )
+    flat_config.dict["config1.param1"] = 2
     flat_config = processing.postmerge(flat_config)
-    check.equal(flat_config.dict, {"config1.param1": 1, "config2.param2": 1})
+    check.equal(flat_config.dict, {"config1.param1": 2, "config2.param2": 2})
     flat_config = processing.presave(flat_config)
-    check.equal(processing.current_value, {"config2.param2": 1})
+    check.equal(processing.current_value, {"config2.param2": 2})
     check.equal(
         flat_config.dict,
-        {"config1.param1": 1, "config2.param2@copy": 'config1.param1'}
+        {"config1.param1": 2, "config2.param2@copy": 'config1.param1'}
     )
     check.equal(processing.keys_to_copy, {"config2.param2": "config1.param1"})
     check.equal(flat_config.process_list, [processing])
     # Reset copy processing
     processing.keys_to_copy = {}
     # Case of wrong key
     with pytest.raises(
```

### Comparing `cliconfig-0.5.5/tests/unit/processing/test_create.py` & `cliconfig-0.5.6/tests/unit/processing/test_create.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/processing/test_type_parser.py` & `cliconfig-0.5.6/tests/unit/processing/test_type_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/test_cli_parser.py` & `cliconfig-0.5.6/tests/unit/test_cli_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/test_config_routines.py` & `cliconfig-0.5.6/tests/unit/test_config_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/test_dict_routines.py` & `cliconfig-0.5.6/tests/unit/test_dict_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/test_ex_docs.py` & `cliconfig-0.5.6/tests/unit/test_ex_docs.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/test_process_routines.py` & `cliconfig-0.5.6/tests/unit/test_process_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.5/tests/unit/test_tag_routines.py` & `cliconfig-0.5.6/tests/unit/test_tag_routines.py`

 * *Files identical despite different names*

