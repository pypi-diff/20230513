# Comparing `tmp/cliconfig-0.5.4.tar.gz` & `tmp/cliconfig-0.5.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cliconfig-0.5.4.tar", last modified: Sat May 13 16:17:45 2023, max compression
+gzip compressed data, was "cliconfig-0.5.5.tar", last modified: Sat May 13 16:24:28 2023, max compression
```

## Comparing `cliconfig-0.5.4.tar` & `cliconfig-0.5.5.tar`

### file list

```diff
@@ -1,107 +1,107 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.975058 cliconfig-0.5.4/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.coveragerc
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.959058 cliconfig-0.5.4/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.963058 cliconfig-0.5.4/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.github/workflows/flake.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.github/workflows/mypy.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.github/workflows/pipy_deployment.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.github/workflows/pydocstyle.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.github/workflows/pylint.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.github/workflows/ruff.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.github/workflows/tests.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.markdownlint.json
--rw-r--r--   0 runner    (1001) docker     (123)    20457 2023-05-13 16:17:26.000000 cliconfig-0.5.4/.pylintrc
--rw-r--r--   0 runner    (1001) docker     (123)     4847 2023-05-13 16:17:26.000000 cliconfig-0.5.4/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 16:17:26.000000 cliconfig-0.5.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     6933 2023-05-13 16:17:45.975058 cliconfig-0.5.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    10878 2023-05-13 16:17:26.000000 cliconfig-0.5.4/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     6498 2023-05-13 16:17:26.000000 cliconfig-0.5.4/README_pypi.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.967058 cliconfig-0.5.4/cliconfig/
--rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 16:17:45.000000 cliconfig-0.5.4/cliconfig/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/cli_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     7339 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/config_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)    14751 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/dict_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     8079 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/process_routines.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.967058 cliconfig-0.5.4/cliconfig/processing/
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/processing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5350 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/processing/_type_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1703 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/processing/base.py
--rw-r--r--   0 runner    (1001) docker     (123)    22217 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/processing/builtin.py
--rw-r--r--   0 runner    (1001) docker     (123)     9833 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/processing/create.py
--rw-r--r--   0 runner    (1001) docker     (123)     3074 2023-05-13 16:17:26.000000 cliconfig-0.5.4/cliconfig/tag_routines.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.967058 cliconfig-0.5.4/cliconfig.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6933 2023-05-13 16:17:45.000000 cliconfig-0.5.4/cliconfig.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2363 2023-05-13 16:17:45.000000 cliconfig-0.5.4/cliconfig.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 16:17:45.000000 cliconfig-0.5.4/cliconfig.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 16:17:45.000000 cliconfig-0.5.4/cliconfig.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 16:17:45.000000 cliconfig-0.5.4/cliconfig.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.971058 cliconfig-0.5.4/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.971058 cliconfig-0.5.4/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (123)     5501 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/_static/logo.png
--rw-r--r--   0 runner    (1001) docker     (123)     6203 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/_static/logo_extend.png
--rw-r--r--   0 runner    (1001) docker     (123)      507 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/cliconfig.processing.rst
--rw-r--r--   0 runner    (1001) docker     (123)      818 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/cliconfig_api.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/contribute.md
--rw-r--r--   0 runner    (1001) docker     (123)     1110 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/edge_cases.md
--rw-r--r--   0 runner    (1001) docker     (123)     4998 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/installation.md
--rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/license.md
--rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/processing.md
--rw-r--r--   0 runner    (1001) docker     (123)     5380 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/quickstart.md
--rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 16:17:26.000000 cliconfig-0.5.4/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.971058 cliconfig-0.5.4/github_actions_utils/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 16:17:26.000000 cliconfig-0.5.4/github_actions_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-13 16:17:26.000000 cliconfig-0.5.4/github_actions_utils/color.py
--rw-r--r--   0 runner    (1001) docker     (123)      754 2023-05-13 16:17:26.000000 cliconfig-0.5.4/github_actions_utils/pydocstyle_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-13 16:17:26.000000 cliconfig-0.5.4/github_actions_utils/pylint_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 16:17:26.000000 cliconfig-0.5.4/github_actions_utils/pytest_manager.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.971058 cliconfig-0.5.4/licenses_tier/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 16:17:26.000000 cliconfig-0.5.4/licenses_tier/FLATTEN_DICT_LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1252 2023-05-13 16:17:26.000000 cliconfig-0.5.4/pre-commit-checks.sh
--rw-r--r--   0 runner    (1001) docker     (123)     2579 2023-05-13 16:17:26.000000 cliconfig-0.5.4/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 16:17:26.000000 cliconfig-0.5.4/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 16:17:26.000000 cliconfig-0.5.4/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 16:17:45.975058 cliconfig-0.5.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 16:17:26.000000 cliconfig-0.5.4/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.971058 cliconfig-0.5.4/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.971058 cliconfig-0.5.4/tests/configs/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/config1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/config2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/configtag1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/configtag2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/default1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/default2.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.975058 cliconfig-0.5.4/tests/configs/integration/
--rw-r--r--   0 runner    (1001) docker     (123)      152 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/integration/main.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/integration/sub1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/integration/sub2.yaml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.975058 cliconfig-0.5.4/tests/configs/merge/
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/merge/additional1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/merge/additional2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/merge/additional3.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/merge/default1.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/merge/default2.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/configs/merge/default3.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.975058 cliconfig-0.5.4/tests/integration/
--rw-r--r--   0 runner    (1001) docker     (123)     1156 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/integration/test_inte_multiple_tags.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.975058 cliconfig-0.5.4/tests/unit/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:17:45.975058 cliconfig-0.5.4/tests/unit/processing/
--rw-r--r--   0 runner    (1001) docker     (123)      932 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/processing/test_base.py
--rw-r--r--   0 runner    (1001) docker     (123)    10858 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/processing/test_builtin.py
--rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/processing/test_create.py
--rw-r--r--   0 runner    (1001) docker     (123)     3969 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/processing/test_type_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/test_cli_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/test_config_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     5808 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/test_dict_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     4779 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/test_ex_docs.py
--rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/test_process_routines.py
--rw-r--r--   0 runner    (1001) docker     (123)     2181 2023-05-13 16:17:26.000000 cliconfig-0.5.4/tests/unit/test_tag_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.coveragerc
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.124336 cliconfig-0.5.5/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.128336 cliconfig-0.5.5/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      398 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/flake.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/mypy.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/pipy_deployment.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/pydocstyle.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/pylint.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/ruff.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.github/workflows/tests.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      258 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.markdownlint.json
+-rw-r--r--   0 runner    (1001) docker     (123)    20457 2023-05-13 16:24:02.000000 cliconfig-0.5.5/.pylintrc
+-rw-r--r--   0 runner    (1001) docker     (123)     4847 2023-05-13 16:24:02.000000 cliconfig-0.5.5/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 16:24:02.000000 cliconfig-0.5.5/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     7003 2023-05-13 16:24:28.136336 cliconfig-0.5.5/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    11023 2023-05-13 16:24:02.000000 cliconfig-0.5.5/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     6568 2023-05-13 16:24:02.000000 cliconfig-0.5.5/README_pypi.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.128336 cliconfig-0.5.5/cliconfig/
+-rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/cli_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7339 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/config_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14751 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/dict_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8079 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/process_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/cliconfig/processing/
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5350 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/_type_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1703 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22217 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/builtin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9833 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/processing/create.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3074 2023-05-13 16:24:02.000000 cliconfig-0.5.5/cliconfig/tag_routines.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.128336 cliconfig-0.5.5/cliconfig.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     7003 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2363 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 16:24:28.000000 cliconfig-0.5.5/cliconfig.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      640 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)     5501 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/_static/logo.png
+-rw-r--r--   0 runner    (1001) docker     (123)     6203 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/_static/logo_extend.png
+-rw-r--r--   0 runner    (1001) docker     (123)      507 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/cliconfig.processing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      818 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/cliconfig_api.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      383 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/contribute.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1110 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/edge_cases.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5068 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      232 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/installation.md
+-rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/license.md
+-rw-r--r--   0 runner    (1001) docker     (123)      766 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/processing.md
+-rw-r--r--   0 runner    (1001) docker     (123)     5380 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/quickstart.md
+-rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 16:24:02.000000 cliconfig-0.5.5/docs/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/github_actions_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/color.py
+-rw-r--r--   0 runner    (1001) docker     (123)      754 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/pydocstyle_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/pylint_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 16:24:02.000000 cliconfig-0.5.5/github_actions_utils/pytest_manager.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/licenses_tier/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-05-13 16:24:02.000000 cliconfig-0.5.5/licenses_tier/FLATTEN_DICT_LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1252 2023-05-13 16:24:02.000000 cliconfig-0.5.5/pre-commit-checks.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     2579 2023-05-13 16:24:02.000000 cliconfig-0.5.5/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-13 16:24:02.000000 cliconfig-0.5.5/requirements-dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-05-13 16:24:02.000000 cliconfig-0.5.5/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 16:24:28.136336 cliconfig-0.5.5/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 16:24:02.000000 cliconfig-0.5.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/tests/configs/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/config1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/config2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/configtag1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/configtag2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/default1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/default2.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.132336 cliconfig-0.5.5/tests/configs/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)      152 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/integration/main.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/integration/sub1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/integration/sub2.yaml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/tests/configs/merge/
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/additional1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       64 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/additional2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/additional3.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/default1.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/default2.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/configs/merge/default3.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/tests/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)     1156 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/integration/test_inte_multiple_tags.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/tests/unit/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 16:24:28.136336 cliconfig-0.5.5/tests/unit/processing/
+-rw-r--r--   0 runner    (1001) docker     (123)      932 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/processing/test_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10858 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/processing/test_builtin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/processing/test_create.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3969 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/processing/test_type_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_cli_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_config_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5808 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_dict_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4779 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_ex_docs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_process_routines.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2181 2023-05-13 16:24:02.000000 cliconfig-0.5.5/tests/unit/test_tag_routines.py
```

### Comparing `cliconfig-0.5.4/.github/workflows/pipy_deployment.yaml` & `cliconfig-0.5.5/.github/workflows/pipy_deployment.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/.github/workflows/pydocstyle.yaml` & `cliconfig-0.5.5/.github/workflows/pydocstyle.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/.github/workflows/pylint.yaml` & `cliconfig-0.5.5/.github/workflows/pylint.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/.github/workflows/tests.yaml` & `cliconfig-0.5.5/.github/workflows/tests.yaml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/.pylintrc` & `cliconfig-0.5.5/.pylintrc`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/CONTRIBUTING.md` & `cliconfig-0.5.5/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/LICENSE` & `cliconfig-0.5.5/LICENSE`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/PKG-INFO` & `cliconfig-0.5.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cliconfig
-Version: 0.5.4
+Version: 0.5.5
 Summary: Merge your config files and set parameters from the command line in a simple way.
 Author-email: Valentin Goldite <valentin.goldite@gmail.com>
 Project-URL: Source, https://github.com/valentingol/cliconfig
 Keywords: logging,machine,learning
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
@@ -61,30 +61,33 @@
 from cliconfig import make_config
 
 config = make_config('default1.yaml', 'default2.yaml')
 config_dict = config.dict  # native python dict
 ```
 
 Then launch your script with additional config(s) file(s) and parameters by command line.
-**By default, these additional configs cannot add new parameters to the default config
-(for security and retro-compatibility reasons).** For instance:
+The additional configs are merge on the default ones then the parameters are set.
 
 ```bash
 python main.py --config first.yaml,second.yaml --param2=-2 --letters.letter2='B'
 ```
 
+**By default, these additional configs cannot add new parameters to the default config
+(for security and retro-compatibility reasons).**
+
 See [*Quick Start*](https://cliconfig.readthedocs.io/en/stable/quick_start.html) section
 of the documentation for more details.
 
 ## With processing
 
 The library provide powerfull tools to modify the configuration called "processings".
 One of the possibility they add is to merge multiple configurations,
 copy a parameter on another, enforce type and more. To do so, simply adding the
 corresponding tags to your parameter names (on config files or CLI parameters).
+
 For instance with these config files:
 
 ```yaml
 ---  # main.yaml
 path_1@merge_add: sub1.yaml
 path_2@merge_add: sub2.yaml
 config3.select@select: "config3.param1"
```

### Comparing `cliconfig-0.5.4/README.md` & `cliconfig-0.5.5/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -206,14 +206,17 @@
 
 **Please note that YAML does not support tuples and sets**, and therefore they
 cannot be used in YAML files. If possible, consider using lists instead.
 
 Moreover, YAML does not recognize "None" as a None object, but interprets it as a
 string. If you wish to set a None object, you can use "null" or "Null" instead.
 
+"@" is a special character used by the package to identify tags. You can't use it
+in your parameters names (but you can use it in your values).
+
 In the context of this package, dictionaries are treated as sub-configurations,
 which means that modifying or adding keys directly in the additional configs may
 not be possible (because only the merge of default configuration allow adding new keys).
 If you need to modify or add keys within a dictionary, consider enclosing it in a list.
 
 For instance:
```

### Comparing `cliconfig-0.5.4/README_pypi.md` & `cliconfig-0.5.5/README_pypi.md`

 * *Files 2% similar despite different names*

```diff
@@ -49,30 +49,33 @@
 from cliconfig import make_config
 
 config = make_config('default1.yaml', 'default2.yaml')
 config_dict = config.dict  # native python dict
 ```
 
 Then launch your script with additional config(s) file(s) and parameters by command line.
-**By default, these additional configs cannot add new parameters to the default config
-(for security and retro-compatibility reasons).** For instance:
+The additional configs are merge on the default ones then the parameters are set.
 
 ```bash
 python main.py --config first.yaml,second.yaml --param2=-2 --letters.letter2='B'
 ```
 
+**By default, these additional configs cannot add new parameters to the default config
+(for security and retro-compatibility reasons).**
+
 See [*Quick Start*](https://cliconfig.readthedocs.io/en/stable/quick_start.html) section
 of the documentation for more details.
 
 ## With processing
 
 The library provide powerfull tools to modify the configuration called "processings".
 One of the possibility they add is to merge multiple configurations,
 copy a parameter on another, enforce type and more. To do so, simply adding the
 corresponding tags to your parameter names (on config files or CLI parameters).
+
 For instance with these config files:
 
 ```yaml
 ---  # main.yaml
 path_1@merge_add: sub1.yaml
 path_2@merge_add: sub2.yaml
 config3.select@select: "config3.param1"
```

### Comparing `cliconfig-0.5.4/cliconfig/__init__.py` & `cliconfig-0.5.5/cliconfig/__init__.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/cli_parser.py` & `cliconfig-0.5.5/cliconfig/cli_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/config_routines.py` & `cliconfig-0.5.5/cliconfig/config_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/dict_routines.py` & `cliconfig-0.5.5/cliconfig/dict_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/process_routines.py` & `cliconfig-0.5.5/cliconfig/process_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/processing/_type_parser.py` & `cliconfig-0.5.5/cliconfig/processing/_type_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/processing/base.py` & `cliconfig-0.5.5/cliconfig/processing/base.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/processing/builtin.py` & `cliconfig-0.5.5/cliconfig/processing/builtin.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/processing/create.py` & `cliconfig-0.5.5/cliconfig/processing/create.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig/tag_routines.py` & `cliconfig-0.5.5/cliconfig/tag_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/cliconfig.egg-info/PKG-INFO` & `cliconfig-0.5.5/cliconfig.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cliconfig
-Version: 0.5.4
+Version: 0.5.5
 Summary: Merge your config files and set parameters from the command line in a simple way.
 Author-email: Valentin Goldite <valentin.goldite@gmail.com>
 Project-URL: Source, https://github.com/valentingol/cliconfig
 Keywords: logging,machine,learning
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
@@ -61,30 +61,33 @@
 from cliconfig import make_config
 
 config = make_config('default1.yaml', 'default2.yaml')
 config_dict = config.dict  # native python dict
 ```
 
 Then launch your script with additional config(s) file(s) and parameters by command line.
-**By default, these additional configs cannot add new parameters to the default config
-(for security and retro-compatibility reasons).** For instance:
+The additional configs are merge on the default ones then the parameters are set.
 
 ```bash
 python main.py --config first.yaml,second.yaml --param2=-2 --letters.letter2='B'
 ```
 
+**By default, these additional configs cannot add new parameters to the default config
+(for security and retro-compatibility reasons).**
+
 See [*Quick Start*](https://cliconfig.readthedocs.io/en/stable/quick_start.html) section
 of the documentation for more details.
 
 ## With processing
 
 The library provide powerfull tools to modify the configuration called "processings".
 One of the possibility they add is to merge multiple configurations,
 copy a parameter on another, enforce type and more. To do so, simply adding the
 corresponding tags to your parameter names (on config files or CLI parameters).
+
 For instance with these config files:
 
 ```yaml
 ---  # main.yaml
 path_1@merge_add: sub1.yaml
 path_2@merge_add: sub2.yaml
 config3.select@select: "config3.param1"
```

### Comparing `cliconfig-0.5.4/cliconfig.egg-info/SOURCES.txt` & `cliconfig-0.5.5/cliconfig.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/Makefile` & `cliconfig-0.5.5/docs/Makefile`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/_static/logo.png` & `cliconfig-0.5.5/docs/_static/logo.png`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/_static/logo_extend.png` & `cliconfig-0.5.5/docs/_static/logo_extend.png`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/cliconfig_api.rst` & `cliconfig-0.5.5/docs/cliconfig_api.rst`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/conf.py` & `cliconfig-0.5.5/docs/conf.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/edge_cases.md` & `cliconfig-0.5.5/docs/edge_cases.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/index.rst` & `cliconfig-0.5.5/docs/index.rst`

 * *Files 2% similar despite different names*

```diff
@@ -31,28 +31,31 @@
    # main.py
    from cliconfig import make_config
 
    config = make_config('default1.yaml', 'default2.yaml')
    config_dict = config.dict  # native python dict
 
 Then launch your script with additional config(s) file(s) and parameters by command line.
-**By default, these additional configs cannot add new parameters to the default config
-(for security and retro-compatibility reasons).** For instance:
+The additional configs are merge on the default ones then the parameters are set.
 
 .. code:: bash
 
    python main.py --config first.yaml,second.yaml --param1=1 --subconfig.param2='foo'
 
+**By default, these additional configs cannot add new parameters to the default config
+(for security and retro-compatibility reasons).**
+
 With processing
 ---------------
 
 The library provide powerfull tools to modify the configuration called "processings".
 One of the possibility they add is to merge multiple configurations,
 copy a parameter on another, enforce type and more. To do so, simply adding the
 corresponding tags to your parameter names (on config files or CLI parameters).
+
 For instance with these config files:
 
 .. code:: yaml
 
     ---  # main.yaml
     path_1@merge_add: sub1.yaml
     path_2@merge_add: sub2.yaml
```

### Comparing `cliconfig-0.5.4/docs/license.md` & `cliconfig-0.5.5/docs/license.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/make.bat` & `cliconfig-0.5.5/docs/make.bat`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/processing.md` & `cliconfig-0.5.5/docs/processing.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/docs/quickstart.md` & `cliconfig-0.5.5/docs/quickstart.md`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/github_actions_utils/pydocstyle_manager.py` & `cliconfig-0.5.5/github_actions_utils/pydocstyle_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/github_actions_utils/pylint_manager.py` & `cliconfig-0.5.5/github_actions_utils/pylint_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/github_actions_utils/pytest_manager.py` & `cliconfig-0.5.5/github_actions_utils/pytest_manager.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/licenses_tier/FLATTEN_DICT_LICENSE` & `cliconfig-0.5.5/licenses_tier/FLATTEN_DICT_LICENSE`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/pre-commit-checks.sh` & `cliconfig-0.5.5/pre-commit-checks.sh`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/pyproject.toml` & `cliconfig-0.5.5/pyproject.toml`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/conftest.py` & `cliconfig-0.5.5/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/integration/test_inte_multiple_tags.py` & `cliconfig-0.5.5/tests/integration/test_inte_multiple_tags.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/processing/test_base.py` & `cliconfig-0.5.5/tests/unit/processing/test_base.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/processing/test_builtin.py` & `cliconfig-0.5.5/tests/unit/processing/test_builtin.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/processing/test_create.py` & `cliconfig-0.5.5/tests/unit/processing/test_create.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/processing/test_type_parser.py` & `cliconfig-0.5.5/tests/unit/processing/test_type_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/test_cli_parser.py` & `cliconfig-0.5.5/tests/unit/test_cli_parser.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/test_config_routines.py` & `cliconfig-0.5.5/tests/unit/test_config_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/test_dict_routines.py` & `cliconfig-0.5.5/tests/unit/test_dict_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/test_ex_docs.py` & `cliconfig-0.5.5/tests/unit/test_ex_docs.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/test_process_routines.py` & `cliconfig-0.5.5/tests/unit/test_process_routines.py`

 * *Files identical despite different names*

### Comparing `cliconfig-0.5.4/tests/unit/test_tag_routines.py` & `cliconfig-0.5.5/tests/unit/test_tag_routines.py`

 * *Files identical despite different names*

