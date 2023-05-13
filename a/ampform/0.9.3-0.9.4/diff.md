# Comparing `tmp/ampform-0.9.3.tar.gz` & `tmp/ampform-0.9.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ampform-0.9.3.tar", last modified: Thu Jun 10 16:50:52 2021, max compression
+gzip compressed data, was "ampform-0.9.4.tar", last modified: Tue Jun 15 17:33:45 2021, max compression
```

## Comparing `ampform-0.9.3.tar` & `ampform-0.9.4.tar`

### file list

```diff
@@ -1,134 +1,134 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.498502 ampform-0.9.3/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.490501 ampform-0.9.3/.constraints/
--rw-r--r--   0 runner    (1001) docker     (121)     1942 2021-06-10 16:50:45.000000 ampform-0.9.3/.constraints/pin_requirements.py
--rw-r--r--   0 runner    (1001) docker     (121)     3778 2021-06-10 16:50:45.000000 ampform-0.9.3/.constraints/py3.6.txt
--rw-r--r--   0 runner    (1001) docker     (121)     3727 2021-06-10 16:50:45.000000 ampform-0.9.3/.constraints/py3.7.txt
--rw-r--r--   0 runner    (1001) docker     (121)     3700 2021-06-10 16:50:45.000000 ampform-0.9.3/.constraints/py3.8.txt
--rw-r--r--   0 runner    (1001) docker     (121)     3700 2021-06-10 16:50:45.000000 ampform-0.9.3/.constraints/py3.9.txt
--rw-r--r--   0 runner    (1001) docker     (121)     4446 2021-06-10 16:50:45.000000 ampform-0.9.3/.cspell.json
--rw-r--r--   0 runner    (1001) docker     (121)      378 2021-06-10 16:50:45.000000 ampform-0.9.3/.editorconfig
--rw-r--r--   0 runner    (1001) docker     (121)      888 2021-06-10 16:50:45.000000 ampform-0.9.3/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.490501 ampform-0.9.3/.github/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.490501 ampform-0.9.3/.github/ISSUE_TEMPLATE/
--rw-r--r--   0 runner    (1001) docker     (121)      678 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0 runner    (1001) docker     (121)      539 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/ISSUE_TEMPLATE/feature_request.md
--rw-r--r--   0 runner    (1001) docker     (121)      284 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/pull_request_template.md
--rw-r--r--   0 runner    (1001) docker     (121)      827 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/release-drafter.yml
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (121)     1186 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/cd.yml
--rw-r--r--   0 runner    (1001) docker     (121)      868 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/ci-docs.yml
--rw-r--r--   0 runner    (1001) docker     (121)      574 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/ci-style.yml
--rw-r--r--   0 runner    (1001) docker     (121)     2271 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/ci-tests.yml
--rw-r--r--   0 runner    (1001) docker     (121)      666 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/linkcheck.yml
--rw-r--r--   0 runner    (1001) docker     (121)      292 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/milestone.yml
--rw-r--r--   0 runner    (1001) docker     (121)      827 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/pr-linting.yml
--rw-r--r--   0 runner    (1001) docker     (121)      280 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/release-drafter.yml
--rw-r--r--   0 runner    (1001) docker     (121)     2571 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/requirements-cron.yml
--rw-r--r--   0 runner    (1001) docker     (121)     2734 2021-06-10 16:50:45.000000 ampform-0.9.3/.github/workflows/requirements-pr.yml
--rw-r--r--   0 runner    (1001) docker     (121)      566 2021-06-10 16:50:45.000000 ampform-0.9.3/.gitignore
--rw-r--r--   0 runner    (1001) docker     (121)      927 2021-06-10 16:50:45.000000 ampform-0.9.3/.gitpod.yml
--rw-r--r--   0 runner    (1001) docker     (121)      105 2021-06-10 16:50:45.000000 ampform-0.9.3/.markdownlint.json
--rw-r--r--   0 runner    (1001) docker     (121)      607 2021-06-10 16:50:45.000000 ampform-0.9.3/.mypy.ini
--rw-r--r--   0 runner    (1001) docker     (121)     3125 2021-06-10 16:50:45.000000 ampform-0.9.3/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (121)       13 2021-06-10 16:50:45.000000 ampform-0.9.3/.prettierignore
--rw-r--r--   0 runner    (1001) docker     (121)       48 2021-06-10 16:50:45.000000 ampform-0.9.3/.prettierrc
--rw-r--r--   0 runner    (1001) docker     (121)      344 2021-06-10 16:50:45.000000 ampform-0.9.3/.pydocstyle
--rw-r--r--   0 runner    (1001) docker     (121)      797 2021-06-10 16:50:45.000000 ampform-0.9.3/.pylintrc
--rw-r--r--   0 runner    (1001) docker     (121)      151 2021-06-10 16:50:45.000000 ampform-0.9.3/.readthedocs.yml
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/.vscode/
--rw-r--r--   0 runner    (1001) docker     (121)      770 2021-06-10 16:50:45.000000 ampform-0.9.3/.vscode/extensions.json
--rw-r--r--   0 runner    (1001) docker     (121)      415 2021-06-10 16:50:45.000000 ampform-0.9.3/.vscode/launch.json
--rw-r--r--   0 runner    (1001) docker     (121)     2268 2021-06-10 16:50:45.000000 ampform-0.9.3/.vscode/settings.json
--rw-r--r--   0 runner    (1001) docker     (121)      237 2021-06-10 16:50:45.000000 ampform-0.9.3/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (121)     4863 2021-06-10 16:50:52.498502 ampform-0.9.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     3002 2021-06-10 16:50:45.000000 ampform-0.9.3/README.md
--rw-r--r--   0 runner    (1001) docker     (121)      982 2021-06-10 16:50:45.000000 ampform-0.9.3/codecov.yml
--rw-r--r--   0 runner    (1001) docker     (121)      333 2021-06-10 16:50:45.000000 ampform-0.9.3/commitlint.config.js
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/docs/
--rw-r--r--   0 runner    (1001) docker     (121)       73 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/.gitignore
--rw-r--r--   0 runner    (1001) docker     (121)       75 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/.pydocstyle
--rw-r--r--   0 runner    (1001) docker     (121)      710 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (121)    15406 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/_static/favicon.ico
--rw-r--r--   0 runner    (1001) docker     (121)      158 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/_static/linebreaks-api.css
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/docs/_templates/
--rw-r--r--   0 runner    (1001) docker     (121)     1692 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/_templates/genindex.html
--rw-r--r--   0 runner    (1001) docker     (121)      201 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/_templates/layout.html
--rw-r--r--   0 runner    (1001) docker     (121)      253 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/_templates/module.rst_t
--rw-r--r--   0 runner    (1001) docker     (121)     1025 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/_templates/package.rst_t
--rw-r--r--   0 runner    (1001) docker     (121)      127 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/_templates/toc.rst_t
--rw-r--r--   0 runner    (1001) docker     (121)     2107 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/abbreviate_signature.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/docs/adr/
--rw-r--r--   0 runner    (1001) docker     (121)     2262 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/adr/template.md
--rw-r--r--   0 runner    (1001) docker     (121)    17160 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/bibliography.bib
--rw-r--r--   0 runner    (1001) docker     (121)    10077 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (121)     6624 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/extend_docstrings.py
--rw-r--r--   0 runner    (1001) docker     (121)     3441 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/index.md
--rw-r--r--   0 runner    (1001) docker     (121)     1860 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/install.md
--rw-r--r--   0 runner    (1001) docker     (121)      179 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/references.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/docs/usage/
--rw-r--r--   0 runner    (1001) docker     (121)        6 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage/.gitignore
--rw-r--r--   0 runner    (1001) docker     (121)    17405 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage/amplitude.ipynb
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/docs/usage/dynamics/
--rw-r--r--   0 runner    (1001) docker     (121)    10884 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage/dynamics/analytic-continuation.ipynb
--rw-r--r--   0 runner    (1001) docker     (121)     9052 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage/dynamics/custom.ipynb
--rw-r--r--   0 runner    (1001) docker     (121)    13551 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage/dynamics/k-matrix.ipynb
--rw-r--r--   0 runner    (1001) docker     (121)    17009 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage/dynamics.ipynb
--rw-r--r--   0 runner    (1001) docker     (121)    15604 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage/interactive.ipynb
--rw-r--r--   0 runner    (1001) docker     (121)     6487 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage/symplot.ipynb
--rw-r--r--   0 runner    (1001) docker     (121)      268 2021-06-10 16:50:45.000000 ampform-0.9.3/docs/usage.md
--rw-r--r--   0 runner    (1001) docker     (121)      174 2021-06-10 16:50:45.000000 ampform-0.9.3/environment.yml
--rw-r--r--   0 runner    (1001) docker     (121)      510 2021-06-10 16:50:45.000000 ampform-0.9.3/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)      293 2021-06-10 16:50:45.000000 ampform-0.9.3/pyrightconfig.json
--rw-r--r--   0 runner    (1001) docker     (121)      529 2021-06-10 16:50:45.000000 ampform-0.9.3/pytest.ini
--rw-r--r--   0 runner    (1001) docker     (121)     2660 2021-06-10 16:50:52.498502 ampform-0.9.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)      112 2021-06-10 16:50:45.000000 ampform-0.9.3/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.490501 ampform-0.9.3/src/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/src/ampform/
--rw-r--r--   0 runner    (1001) docker     (121)     1416 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     4833 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/_graph_info.py
--rw-r--r--   0 runner    (1001) docker     (121)    12132 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/data.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.498502 ampform-0.9.3/src/ampform/dynamics/
--rw-r--r--   0 runner    (1001) docker     (121)    11520 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/dynamics/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     5714 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/dynamics/builder.py
--rw-r--r--   0 runner    (1001) docker     (121)     4653 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/dynamics/decorator.py
--rw-r--r--   0 runner    (1001) docker     (121)     2255 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/dynamics/math.py
--rw-r--r--   0 runner    (1001) docker     (121)    26830 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/helicity.py
--rw-r--r--   0 runner    (1001) docker     (121)    12753 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/kinematics.py
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:45.000000 ampform-0.9.3/src/ampform/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.494501 ampform-0.9.3/src/ampform.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     4863 2021-06-10 16:50:52.000000 ampform-0.9.3/src/ampform.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2654 2021-06-10 16:50:52.000000 ampform-0.9.3/src/ampform.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2021-06-10 16:50:52.000000 ampform-0.9.3/src/ampform.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1777 2021-06-10 16:50:52.000000 ampform-0.9.3/src/ampform.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       16 2021-06-10 16:50:52.000000 ampform-0.9.3/src/ampform.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.498502 ampform-0.9.3/src/symplot/
--rw-r--r--   0 runner    (1001) docker     (121)     9381 2021-06-10 16:50:45.000000 ampform-0.9.3/src/symplot/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:45.000000 ampform-0.9.3/src/symplot/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.498502 ampform-0.9.3/tests/
--rw-r--r--   0 runner    (1001) docker     (121)       75 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/.pydocstyle
--rw-r--r--   0 runner    (1001) docker     (121)       57 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     5475 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.498502 ampform-0.9.3/tests/external/
--rw-r--r--   0 runner    (1001) docker     (121)       57 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/external/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1727 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/external/test_sympy.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.498502 ampform-0.9.3/tests/output/
--rw-r--r--   0 runner    (1001) docker     (121)       14 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/output/.gitignore
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.498502 ampform-0.9.3/tests/symplot/
--rw-r--r--   0 runner    (1001) docker     (121)       57 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/symplot/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      650 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/symplot/test_ipywidgets.py
--rw-r--r--   0 runner    (1001) docker     (121)     7471 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/symplot/test_symplot.py
--rw-r--r--   0 runner    (1001) docker     (121)     7566 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/test_angular_distributions.py
--rw-r--r--   0 runner    (1001) docker     (121)     1691 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/test_angular_momentum.py
--rw-r--r--   0 runner    (1001) docker     (121)     2400 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/test_data.py
--rw-r--r--   0 runner    (1001) docker     (121)     4739 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/test_dynamics.py
--rw-r--r--   0 runner    (1001) docker     (121)      940 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/test_graph_info.py
--rw-r--r--   0 runner    (1001) docker     (121)     1554 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/test_helicity.py
--rw-r--r--   0 runner    (1001) docker     (121)     3781 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/test_kinematics.py
--rw-r--r--   0 runner    (1001) docker     (121)     1466 2021-06-10 16:50:45.000000 ampform-0.9.3/tests/test_parity_prefactor.py
--rw-r--r--   0 runner    (1001) docker     (121)     2485 2021-06-10 16:50:45.000000 ampform-0.9.3/tox.ini
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:52.498502 ampform-0.9.3/typings/
--rw-r--r--   0 runner    (1001) docker     (121)       10 2021-06-10 16:50:45.000000 ampform-0.9.3/typings/.gitignore
--rw-r--r--   0 runner    (1001) docker     (121)       75 2021-06-10 16:50:45.000000 ampform-0.9.3/typings/.pydocstyle
--rw-r--r--   0 runner    (1001) docker     (121)      517 2021-06-10 16:50:45.000000 ampform-0.9.3/typings/README.md
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-06-10 16:50:45.000000 ampform-0.9.3/typings/__init__.pyi
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.188816 ampform-0.9.4/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.180816 ampform-0.9.4/.constraints/
+-rw-r--r--   0 runner    (1001) docker     (121)     1942 2021-06-15 17:33:36.000000 ampform-0.9.4/.constraints/pin_requirements.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3789 2021-06-15 17:33:36.000000 ampform-0.9.4/.constraints/py3.6.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     3738 2021-06-15 17:33:36.000000 ampform-0.9.4/.constraints/py3.7.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     3694 2021-06-15 17:33:36.000000 ampform-0.9.4/.constraints/py3.8.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     3694 2021-06-15 17:33:36.000000 ampform-0.9.4/.constraints/py3.9.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     4446 2021-06-15 17:33:36.000000 ampform-0.9.4/.cspell.json
+-rw-r--r--   0 runner    (1001) docker     (121)      378 2021-06-15 17:33:36.000000 ampform-0.9.4/.editorconfig
+-rw-r--r--   0 runner    (1001) docker     (121)      888 2021-06-15 17:33:36.000000 ampform-0.9.4/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.180816 ampform-0.9.4/.github/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.180816 ampform-0.9.4/.github/ISSUE_TEMPLATE/
+-rw-r--r--   0 runner    (1001) docker     (121)      678 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0 runner    (1001) docker     (121)      539 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/ISSUE_TEMPLATE/feature_request.md
+-rw-r--r--   0 runner    (1001) docker     (121)      284 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/pull_request_template.md
+-rw-r--r--   0 runner    (1001) docker     (121)      827 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/release-drafter.yml
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.180816 ampform-0.9.4/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (121)     1186 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/cd.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      868 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/ci-docs.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      589 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/ci-style.yml
+-rw-r--r--   0 runner    (1001) docker     (121)     2271 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/ci-tests.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      666 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/linkcheck.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      292 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/milestone.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      827 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/pr-linting.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      280 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/release-drafter.yml
+-rw-r--r--   0 runner    (1001) docker     (121)     2571 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/requirements-cron.yml
+-rw-r--r--   0 runner    (1001) docker     (121)     2734 2021-06-15 17:33:36.000000 ampform-0.9.4/.github/workflows/requirements-pr.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      566 2021-06-15 17:33:36.000000 ampform-0.9.4/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (121)      927 2021-06-15 17:33:36.000000 ampform-0.9.4/.gitpod.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      105 2021-06-15 17:33:36.000000 ampform-0.9.4/.markdownlint.json
+-rw-r--r--   0 runner    (1001) docker     (121)      607 2021-06-15 17:33:36.000000 ampform-0.9.4/.mypy.ini
+-rw-r--r--   0 runner    (1001) docker     (121)     3125 2021-06-15 17:33:36.000000 ampform-0.9.4/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (121)       13 2021-06-15 17:33:36.000000 ampform-0.9.4/.prettierignore
+-rw-r--r--   0 runner    (1001) docker     (121)       48 2021-06-15 17:33:36.000000 ampform-0.9.4/.prettierrc
+-rw-r--r--   0 runner    (1001) docker     (121)      344 2021-06-15 17:33:36.000000 ampform-0.9.4/.pydocstyle
+-rw-r--r--   0 runner    (1001) docker     (121)      797 2021-06-15 17:33:36.000000 ampform-0.9.4/.pylintrc
+-rw-r--r--   0 runner    (1001) docker     (121)      151 2021-06-15 17:33:36.000000 ampform-0.9.4/.readthedocs.yml
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.180816 ampform-0.9.4/.vscode/
+-rw-r--r--   0 runner    (1001) docker     (121)      770 2021-06-15 17:33:36.000000 ampform-0.9.4/.vscode/extensions.json
+-rw-r--r--   0 runner    (1001) docker     (121)      415 2021-06-15 17:33:36.000000 ampform-0.9.4/.vscode/launch.json
+-rw-r--r--   0 runner    (1001) docker     (121)     2268 2021-06-15 17:33:36.000000 ampform-0.9.4/.vscode/settings.json
+-rw-r--r--   0 runner    (1001) docker     (121)      237 2021-06-15 17:33:36.000000 ampform-0.9.4/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (121)     4863 2021-06-15 17:33:45.188816 ampform-0.9.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     3002 2021-06-15 17:33:36.000000 ampform-0.9.4/README.md
+-rw-r--r--   0 runner    (1001) docker     (121)      982 2021-06-15 17:33:36.000000 ampform-0.9.4/codecov.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      333 2021-06-15 17:33:36.000000 ampform-0.9.4/commitlint.config.js
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/docs/
+-rw-r--r--   0 runner    (1001) docker     (121)       73 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (121)       75 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/.pydocstyle
+-rw-r--r--   0 runner    (1001) docker     (121)      710 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (121)    15406 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/_static/favicon.ico
+-rw-r--r--   0 runner    (1001) docker     (121)      158 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/_static/linebreaks-api.css
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/docs/_templates/
+-rw-r--r--   0 runner    (1001) docker     (121)     1692 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/_templates/genindex.html
+-rw-r--r--   0 runner    (1001) docker     (121)      201 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/_templates/layout.html
+-rw-r--r--   0 runner    (1001) docker     (121)      253 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/_templates/module.rst_t
+-rw-r--r--   0 runner    (1001) docker     (121)     1025 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/_templates/package.rst_t
+-rw-r--r--   0 runner    (1001) docker     (121)      127 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/_templates/toc.rst_t
+-rw-r--r--   0 runner    (1001) docker     (121)     2107 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/abbreviate_signature.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/docs/adr/
+-rw-r--r--   0 runner    (1001) docker     (121)     2262 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/adr/template.md
+-rw-r--r--   0 runner    (1001) docker     (121)    17160 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/bibliography.bib
+-rw-r--r--   0 runner    (1001) docker     (121)    10077 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7370 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/extend_docstrings.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3441 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/index.md
+-rw-r--r--   0 runner    (1001) docker     (121)     1860 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/install.md
+-rw-r--r--   0 runner    (1001) docker     (121)      179 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/references.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/docs/usage/
+-rw-r--r--   0 runner    (1001) docker     (121)        6 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (121)    17405 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage/amplitude.ipynb
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/docs/usage/dynamics/
+-rw-r--r--   0 runner    (1001) docker     (121)    11735 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage/dynamics/analytic-continuation.ipynb
+-rw-r--r--   0 runner    (1001) docker     (121)     9052 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage/dynamics/custom.ipynb
+-rw-r--r--   0 runner    (1001) docker     (121)    13551 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage/dynamics/k-matrix.ipynb
+-rw-r--r--   0 runner    (1001) docker     (121)    18290 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage/dynamics.ipynb
+-rw-r--r--   0 runner    (1001) docker     (121)    15604 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage/interactive.ipynb
+-rw-r--r--   0 runner    (1001) docker     (121)     6487 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage/symplot.ipynb
+-rw-r--r--   0 runner    (1001) docker     (121)      268 2021-06-15 17:33:36.000000 ampform-0.9.4/docs/usage.md
+-rw-r--r--   0 runner    (1001) docker     (121)      174 2021-06-15 17:33:36.000000 ampform-0.9.4/environment.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      510 2021-06-15 17:33:36.000000 ampform-0.9.4/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (121)      293 2021-06-15 17:33:36.000000 ampform-0.9.4/pyrightconfig.json
+-rw-r--r--   0 runner    (1001) docker     (121)      529 2021-06-15 17:33:36.000000 ampform-0.9.4/pytest.ini
+-rw-r--r--   0 runner    (1001) docker     (121)     2676 2021-06-15 17:33:45.188816 ampform-0.9.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)      112 2021-06-15 17:33:36.000000 ampform-0.9.4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.172816 ampform-0.9.4/src/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/src/ampform/
+-rw-r--r--   0 runner    (1001) docker     (121)     1416 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4833 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/_graph_info.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12132 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/data.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/src/ampform/dynamics/
+-rw-r--r--   0 runner    (1001) docker     (121)    12241 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/dynamics/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5726 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/dynamics/builder.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4653 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/dynamics/decorator.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2255 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/dynamics/math.py
+-rw-r--r--   0 runner    (1001) docker     (121)    26830 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/helicity.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12753 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/kinematics.py
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:36.000000 ampform-0.9.4/src/ampform/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/src/ampform.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     4863 2021-06-15 17:33:44.000000 ampform-0.9.4/src/ampform.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     2654 2021-06-15 17:33:45.000000 ampform-0.9.4/src/ampform.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2021-06-15 17:33:44.000000 ampform-0.9.4/src/ampform.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     1807 2021-06-15 17:33:44.000000 ampform-0.9.4/src/ampform.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       16 2021-06-15 17:33:44.000000 ampform-0.9.4/src/ampform.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.184816 ampform-0.9.4/src/symplot/
+-rw-r--r--   0 runner    (1001) docker     (121)     9381 2021-06-15 17:33:36.000000 ampform-0.9.4/src/symplot/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:36.000000 ampform-0.9.4/src/symplot/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.188816 ampform-0.9.4/tests/
+-rw-r--r--   0 runner    (1001) docker     (121)       75 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/.pydocstyle
+-rw-r--r--   0 runner    (1001) docker     (121)       57 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5475 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.188816 ampform-0.9.4/tests/external/
+-rw-r--r--   0 runner    (1001) docker     (121)       57 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/external/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1727 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/external/test_sympy.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.188816 ampform-0.9.4/tests/output/
+-rw-r--r--   0 runner    (1001) docker     (121)       14 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/output/.gitignore
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.188816 ampform-0.9.4/tests/symplot/
+-rw-r--r--   0 runner    (1001) docker     (121)       57 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/symplot/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      650 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/symplot/test_ipywidgets.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7471 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/symplot/test_symplot.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7566 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/test_angular_distributions.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1691 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/test_angular_momentum.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2400 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/test_data.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4645 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/test_dynamics.py
+-rw-r--r--   0 runner    (1001) docker     (121)      940 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/test_graph_info.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1554 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/test_helicity.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3781 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/test_kinematics.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1466 2021-06-15 17:33:36.000000 ampform-0.9.4/tests/test_parity_prefactor.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2485 2021-06-15 17:33:36.000000 ampform-0.9.4/tox.ini
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:45.188816 ampform-0.9.4/typings/
+-rw-r--r--   0 runner    (1001) docker     (121)       10 2021-06-15 17:33:36.000000 ampform-0.9.4/typings/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (121)       75 2021-06-15 17:33:36.000000 ampform-0.9.4/typings/.pydocstyle
+-rw-r--r--   0 runner    (1001) docker     (121)      517 2021-06-15 17:33:36.000000 ampform-0.9.4/typings/README.md
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-06-15 17:33:36.000000 ampform-0.9.4/typings/__init__.pyi
```

### Comparing `ampform-0.9.3/.constraints/pin_requirements.py` & `ampform-0.9.4/.constraints/pin_requirements.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.constraints/py3.6.txt` & `ampform-0.9.4/.constraints/py3.6.txt`

 * *Files 2% similar despite different names*

```diff
@@ -2,25 +2,24 @@
 # This file is autogenerated by pip-compile
 # To update, run:
 #
 #    pip-compile --extra=dev --no-annotate --output-file=.constraints/py3.6.txt
 #
 alabaster==0.7.12
 anyio==3.1.0
-apipkg==1.5
 appdirs==1.4.4
 aquirdturtle-collapsible-headings==3.1.0
 argon2-cffi==20.1.0
 astroid==2.5.6
 async-generator==1.10
 attrs==20.3.0
 babel==2.9.1
 backcall==0.2.0
 beautifulsoup4==4.9.3
-black==21.5b2
+black==21.6b0
 bleach==3.3.0
 certifi==2021.5.30
 cffi==1.14.5
 cfgv==3.3.0
 chardet==4.0.0
 click==8.0.1
 colorama==0.4.4
@@ -29,15 +28,15 @@
 cycler==0.10.0
 dataclasses==0.8 ; python_version < "3.7"
 decorator==5.0.9
 defusedxml==0.7.1
 distlib==0.3.2
 docutils==0.16
 entrypoints==0.3
-execnet==1.8.1
+execnet==1.9.0
 filelock==3.0.12
 flake8-blind-except==0.2.0
 flake8-bugbear==21.4.3
 flake8-builtins==1.5.3
 flake8-comprehensions==3.5.0
 flake8-plugin-utils==1.3.2
 flake8-polyfill==1.0.2
@@ -47,15 +46,15 @@
 flake8==3.9.2
 future==0.18.2
 gitdb==4.0.7
 gitpython==3.1.17
 gprof2dot==2021.2.21
 graphviz==0.16
 hepunits==2.1.1
-identify==2.2.9
+identify==2.2.10
 idna==2.10
 imagesize==1.2.0
 immutables==0.15
 importlib-metadata==4.5.0
 importlib-resources==3.0.0
 iniconfig==1.1.1
 ipykernel==5.5.5
@@ -88,15 +87,15 @@
 matplotlib==3.3.4
 mccabe==0.6.1
 mdit-py-plugins==0.2.6
 mistune==0.8.4
 mpl-interactions==0.17.12
 mpmath==1.2.1
 mypy-extensions==0.4.3
-mypy==0.812
+mypy==0.902
 myst-nb==0.12.3
 myst-parser==0.13.7
 nbclassic==0.3.1
 nbclient==0.5.3
 nbconvert==5.6.1
 nbdime==3.1.0
 nbformat==5.1.3
@@ -140,55 +139,56 @@
 pytest==6.2.4
 python-constraint==1.4.0
 python-dateutil==2.8.1
 pytz==2021.1
 pyyaml==5.4.1
 pyzmq==22.1.0
 qrules==0.8.2
-radon==4.5.2
+radon==5.0.1
 regex==2021.4.4
 requests==2.25.1
 restructuredtext-lint==1.3.2
 send2trash==1.5.0
 six==1.16.0
 smmap==4.0.0
 sniffio==1.2.0
 snowballstemmer==2.1.0
 soupsieve==2.2.1
 sphinx-autobuild==2021.3.14
 sphinx-book-theme==0.1.0
-sphinx-copybutton==0.3.1
+sphinx-copybutton==0.3.3
 sphinx-panels==0.6.0
 sphinx-thebe==0.0.8
 sphinx-togglebutton==0.2.3
 sphinx==3.5.4
 sphinxcontrib-applehelp==1.0.2
 sphinxcontrib-bibtex==2.3.0
 sphinxcontrib-devhelp==1.0.2
 sphinxcontrib-hep-pdgref==0.1.3
 sphinxcontrib-htmlhelp==2.0.0
 sphinxcontrib-jsmath==1.0.1
 sphinxcontrib-qthelp==1.0.3
 sphinxcontrib-serializinghtml==1.1.5
 sqlalchemy==1.3.24
 sympy==1.8
-terminado==0.10.0
+terminado==0.10.1
 testpath==0.5.0
 toml==0.10.2
 tornado==6.1
 tox==3.23.1
-tqdm==4.61.0
+tqdm==4.61.1
 traitlets==4.3.3
 typed-ast==1.4.3
+types-docutils==0.1.6
 typing-extensions==3.10.0.0 ; python_version < "3.8.0"
 urllib3==1.26.5
 virtualenv==20.4.7
 wcwidth==0.2.5
 webencodings==0.5.1
-websocket-client==1.0.1
+websocket-client==1.1.0
 wheel==0.36.2
 widgetsnbextension==3.5.1
 wrapt==1.12.1
 zipp==3.4.1
 
 # The following packages are considered to be unsafe in a requirements file:
 # pip
```

### Comparing `ampform-0.9.3/.constraints/py3.7.txt` & `ampform-0.9.4/.constraints/py3.7.txt`

 * *Files 3% similar despite different names*

```diff
@@ -2,40 +2,39 @@
 # This file is autogenerated by pip-compile
 # To update, run:
 #
 #    pip-compile --extra=dev --no-annotate --output-file=.constraints/py3.7.txt
 #
 alabaster==0.7.12
 anyio==3.1.0
-apipkg==1.5
 appdirs==1.4.4
 aquirdturtle-collapsible-headings==3.1.0
 argon2-cffi==20.1.0
 astroid==2.5.6
 async-generator==1.10
 attrs==20.3.0
 babel==2.9.1
 backcall==0.2.0
 beautifulsoup4==4.9.3
-black==21.5b2
+black==21.6b0
 bleach==3.3.0
 certifi==2021.5.30
 cffi==1.14.5
 cfgv==3.3.0
 chardet==4.0.0
 click==8.0.1
 colorama==0.4.4
 coverage==5.5
 cycler==0.10.0
 decorator==5.0.9
 defusedxml==0.7.1
 distlib==0.3.2
 docutils==0.16
 entrypoints==0.3
-execnet==1.8.1
+execnet==1.9.0
 filelock==3.0.12
 flake8-blind-except==0.2.0
 flake8-bugbear==21.4.3
 flake8-builtins==1.5.3
 flake8-comprehensions==3.5.0
 flake8-plugin-utils==1.3.2
 flake8-polyfill==1.0.2
@@ -45,15 +44,15 @@
 flake8==3.9.2
 future==0.18.2
 gitdb==4.0.7
 gitpython==3.1.17
 gprof2dot==2021.2.21
 graphviz==0.16
 hepunits==2.1.1
-identify==2.2.9
+identify==2.2.10
 idna==2.10
 imagesize==1.2.0
 importlib-metadata==4.5.0
 importlib-resources==5.1.4
 iniconfig==1.1.1
 ipykernel==5.5.5
 ipympl==0.7.0
@@ -86,15 +85,15 @@
 matplotlib==3.4.2
 mccabe==0.6.1
 mdit-py-plugins==0.2.6
 mistune==0.8.4
 mpl-interactions==0.17.12
 mpmath==1.2.1
 mypy-extensions==0.4.3
-mypy==0.812
+mypy==0.902
 myst-nb==0.12.3
 myst-parser==0.13.7
 nbclassic==0.3.1
 nbclient==0.5.3
 nbconvert==5.6.1
 nbdime==3.1.0
 nbformat==5.1.3
@@ -138,55 +137,56 @@
 pytest==6.2.4
 python-constraint==1.4.0
 python-dateutil==2.8.1
 pytz==2021.1
 pyyaml==5.4.1
 pyzmq==22.1.0
 qrules==0.8.2
-radon==4.5.2
+radon==5.0.1
 regex==2021.4.4
 requests==2.25.1
 restructuredtext-lint==1.3.2
 send2trash==1.5.0
 six==1.16.0
 smmap==4.0.0
 sniffio==1.2.0
 snowballstemmer==2.1.0
 soupsieve==2.2.1
 sphinx-autobuild==2021.3.14
 sphinx-book-theme==0.1.0
-sphinx-copybutton==0.3.1
+sphinx-copybutton==0.3.3
 sphinx-panels==0.6.0
 sphinx-thebe==0.0.8
 sphinx-togglebutton==0.2.3
 sphinx==3.5.4
 sphinxcontrib-applehelp==1.0.2
 sphinxcontrib-bibtex==2.3.0
 sphinxcontrib-devhelp==1.0.2
 sphinxcontrib-hep-pdgref==0.1.3
 sphinxcontrib-htmlhelp==2.0.0
 sphinxcontrib-jsmath==1.0.1
 sphinxcontrib-qthelp==1.0.3
 sphinxcontrib-serializinghtml==1.1.5
 sqlalchemy==1.3.24
 sympy==1.8
-terminado==0.10.0
+terminado==0.10.1
 testpath==0.5.0
 toml==0.10.2
 tornado==6.1
 tox==3.23.1
-tqdm==4.61.0
+tqdm==4.61.1
 traitlets==5.0.5
 typed-ast==1.4.3
+types-docutils==0.1.6
 typing-extensions==3.10.0.0 ; python_version < "3.8.0"
 urllib3==1.26.5
 virtualenv==20.4.7
 wcwidth==0.2.5
 webencodings==0.5.1
-websocket-client==1.0.1
+websocket-client==1.1.0
 wheel==0.36.2
 widgetsnbextension==3.5.1
 wrapt==1.12.1
 zipp==3.4.1
 
 # The following packages are considered to be unsafe in a requirements file:
 # pip
```

### Comparing `ampform-0.9.3/.constraints/py3.8.txt` & `ampform-0.9.4/.constraints/py3.9.txt`

 * *Files 3% similar despite different names*

```diff
@@ -1,41 +1,40 @@
 #
 # This file is autogenerated by pip-compile
 # To update, run:
 #
-#    pip-compile --extra=dev --no-annotate --output-file=.constraints/py3.8.txt
+#    pip-compile --extra=dev --no-annotate --output-file=.constraints/py3.9.txt
 #
 alabaster==0.7.12
 anyio==3.1.0
-apipkg==1.5
 appdirs==1.4.4
 aquirdturtle-collapsible-headings==3.1.0
 argon2-cffi==20.1.0
 astroid==2.5.6
 async-generator==1.10
 attrs==20.3.0
 babel==2.9.1
 backcall==0.2.0
 beautifulsoup4==4.9.3
-black==21.5b2
+black==21.6b0
 bleach==3.3.0
 certifi==2021.5.30
 cffi==1.14.5
 cfgv==3.3.0
 chardet==4.0.0
 click==8.0.1
 colorama==0.4.4
 coverage==5.5
 cycler==0.10.0
 decorator==5.0.9
 defusedxml==0.7.1
 distlib==0.3.2
 docutils==0.16
 entrypoints==0.3
-execnet==1.8.1
+execnet==1.9.0
 filelock==3.0.12
 flake8-blind-except==0.2.0
 flake8-bugbear==21.4.3
 flake8-builtins==1.5.3
 flake8-comprehensions==3.5.0
 flake8-plugin-utils==1.3.2
 flake8-polyfill==1.0.2
@@ -45,15 +44,15 @@
 flake8==3.9.2
 future==0.18.2
 gitdb==4.0.7
 gitpython==3.1.17
 gprof2dot==2021.2.21
 graphviz==0.16
 hepunits==2.1.1
-identify==2.2.9
+identify==2.2.10
 idna==2.10
 imagesize==1.2.0
 importlib-metadata==4.5.0
 importlib-resources==5.1.4
 iniconfig==1.1.1
 ipykernel==5.5.5
 ipympl==0.7.0
@@ -86,15 +85,15 @@
 matplotlib==3.4.2
 mccabe==0.6.1
 mdit-py-plugins==0.2.6
 mistune==0.8.4
 mpl-interactions==0.17.12
 mpmath==1.2.1
 mypy-extensions==0.4.3
-mypy==0.812
+mypy==0.902
 myst-nb==0.12.3
 myst-parser==0.13.7
 nbclassic==0.3.1
 nbclient==0.5.3
 nbconvert==5.6.1
 nbdime==3.1.0
 nbformat==5.1.3
@@ -138,55 +137,55 @@
 pytest==6.2.4
 python-constraint==1.4.0
 python-dateutil==2.8.1
 pytz==2021.1
 pyyaml==5.4.1
 pyzmq==22.1.0
 qrules==0.8.2
-radon==4.5.2
+radon==5.0.1
 regex==2021.4.4
 requests==2.25.1
 restructuredtext-lint==1.3.2
 send2trash==1.5.0
 six==1.16.0
 smmap==4.0.0
 sniffio==1.2.0
 snowballstemmer==2.1.0
 soupsieve==2.2.1
 sphinx-autobuild==2021.3.14
 sphinx-book-theme==0.1.0
-sphinx-copybutton==0.3.1
+sphinx-copybutton==0.3.3
 sphinx-panels==0.6.0
 sphinx-thebe==0.0.8
 sphinx-togglebutton==0.2.3
 sphinx==3.5.4
 sphinxcontrib-applehelp==1.0.2
 sphinxcontrib-bibtex==2.3.0
 sphinxcontrib-devhelp==1.0.2
 sphinxcontrib-hep-pdgref==0.1.3
 sphinxcontrib-htmlhelp==2.0.0
 sphinxcontrib-jsmath==1.0.1
 sphinxcontrib-qthelp==1.0.3
 sphinxcontrib-serializinghtml==1.1.5
 sqlalchemy==1.3.24
 sympy==1.8
-terminado==0.10.0
+terminado==0.10.1
 testpath==0.5.0
 toml==0.10.2
 tornado==6.1
 tox==3.23.1
-tqdm==4.61.0
+tqdm==4.61.1
 traitlets==5.0.5
-typed-ast==1.4.3
+types-docutils==0.1.6
 typing-extensions==3.10.0.0
 urllib3==1.26.5
 virtualenv==20.4.7
 wcwidth==0.2.5
 webencodings==0.5.1
-websocket-client==1.0.1
+websocket-client==1.1.0
 wheel==0.36.2
 widgetsnbextension==3.5.1
 wrapt==1.12.1
 zipp==3.4.1
 
 # The following packages are considered to be unsafe in a requirements file:
 # pip
```

### Comparing `ampform-0.9.3/.constraints/py3.9.txt` & `ampform-0.9.4/.constraints/py3.8.txt`

 * *Files 2% similar despite different names*

```diff
@@ -1,41 +1,40 @@
 #
 # This file is autogenerated by pip-compile
 # To update, run:
 #
-#    pip-compile --extra=dev --no-annotate --output-file=.constraints/py3.9.txt
+#    pip-compile --extra=dev --no-annotate --output-file=.constraints/py3.8.txt
 #
 alabaster==0.7.12
 anyio==3.1.0
-apipkg==1.5
 appdirs==1.4.4
 aquirdturtle-collapsible-headings==3.1.0
 argon2-cffi==20.1.0
 astroid==2.5.6
 async-generator==1.10
 attrs==20.3.0
 babel==2.9.1
 backcall==0.2.0
 beautifulsoup4==4.9.3
-black==21.5b2
+black==21.6b0
 bleach==3.3.0
 certifi==2021.5.30
 cffi==1.14.5
 cfgv==3.3.0
 chardet==4.0.0
 click==8.0.1
 colorama==0.4.4
 coverage==5.5
 cycler==0.10.0
 decorator==5.0.9
 defusedxml==0.7.1
 distlib==0.3.2
 docutils==0.16
 entrypoints==0.3
-execnet==1.8.1
+execnet==1.9.0
 filelock==3.0.12
 flake8-blind-except==0.2.0
 flake8-bugbear==21.4.3
 flake8-builtins==1.5.3
 flake8-comprehensions==3.5.0
 flake8-plugin-utils==1.3.2
 flake8-polyfill==1.0.2
@@ -45,15 +44,15 @@
 flake8==3.9.2
 future==0.18.2
 gitdb==4.0.7
 gitpython==3.1.17
 gprof2dot==2021.2.21
 graphviz==0.16
 hepunits==2.1.1
-identify==2.2.9
+identify==2.2.10
 idna==2.10
 imagesize==1.2.0
 importlib-metadata==4.5.0
 importlib-resources==5.1.4
 iniconfig==1.1.1
 ipykernel==5.5.5
 ipympl==0.7.0
@@ -86,15 +85,15 @@
 matplotlib==3.4.2
 mccabe==0.6.1
 mdit-py-plugins==0.2.6
 mistune==0.8.4
 mpl-interactions==0.17.12
 mpmath==1.2.1
 mypy-extensions==0.4.3
-mypy==0.812
+mypy==0.902
 myst-nb==0.12.3
 myst-parser==0.13.7
 nbclassic==0.3.1
 nbclient==0.5.3
 nbconvert==5.6.1
 nbdime==3.1.0
 nbformat==5.1.3
@@ -138,55 +137,55 @@
 pytest==6.2.4
 python-constraint==1.4.0
 python-dateutil==2.8.1
 pytz==2021.1
 pyyaml==5.4.1
 pyzmq==22.1.0
 qrules==0.8.2
-radon==4.5.2
+radon==5.0.1
 regex==2021.4.4
 requests==2.25.1
 restructuredtext-lint==1.3.2
 send2trash==1.5.0
 six==1.16.0
 smmap==4.0.0
 sniffio==1.2.0
 snowballstemmer==2.1.0
 soupsieve==2.2.1
 sphinx-autobuild==2021.3.14
 sphinx-book-theme==0.1.0
-sphinx-copybutton==0.3.1
+sphinx-copybutton==0.3.3
 sphinx-panels==0.6.0
 sphinx-thebe==0.0.8
 sphinx-togglebutton==0.2.3
 sphinx==3.5.4
 sphinxcontrib-applehelp==1.0.2
 sphinxcontrib-bibtex==2.3.0
 sphinxcontrib-devhelp==1.0.2
 sphinxcontrib-hep-pdgref==0.1.3
 sphinxcontrib-htmlhelp==2.0.0
 sphinxcontrib-jsmath==1.0.1
 sphinxcontrib-qthelp==1.0.3
 sphinxcontrib-serializinghtml==1.1.5
 sqlalchemy==1.3.24
 sympy==1.8
-terminado==0.10.0
+terminado==0.10.1
 testpath==0.5.0
 toml==0.10.2
 tornado==6.1
 tox==3.23.1
-tqdm==4.61.0
+tqdm==4.61.1
 traitlets==5.0.5
-typed-ast==1.4.3
+types-docutils==0.1.6
 typing-extensions==3.10.0.0
 urllib3==1.26.5
 virtualenv==20.4.7
 wcwidth==0.2.5
 webencodings==0.5.1
-websocket-client==1.0.1
+websocket-client==1.1.0
 wheel==0.36.2
 widgetsnbextension==3.5.1
 wrapt==1.12.1
 zipp==3.4.1
 
 # The following packages are considered to be unsafe in a requirements file:
 # pip
```

### Comparing `ampform-0.9.3/.cspell.json` & `ampform-0.9.4/.cspell.json`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.flake8` & `ampform-0.9.4/.flake8`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/ISSUE_TEMPLATE/bug_report.md` & `ampform-0.9.4/.github/ISSUE_TEMPLATE/bug_report.md`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/ISSUE_TEMPLATE/feature_request.md` & `ampform-0.9.4/.github/ISSUE_TEMPLATE/feature_request.md`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/release-drafter.yml` & `ampform-0.9.4/.github/release-drafter.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/workflows/cd.yml` & `ampform-0.9.4/.github/workflows/cd.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/workflows/ci-docs.yml` & `ampform-0.9.4/.github/workflows/ci-docs.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/workflows/ci-style.yml` & `ampform-0.9.4/.github/workflows/ci-style.yml`

 * *Files 24% similar despite different names*

```diff
@@ -21,8 +21,8 @@
         with:
           python-version: 3.7
       - name: Install dependencies
         run: |
           python -m pip install --upgrade pip
           pip install -c .constraints/py3.7.txt -e .[sty]
       - name: Perform style checks
-        run: pre-commit run -a
+        run: pre-commit run -a --color always
```

### Comparing `ampform-0.9.3/.github/workflows/ci-tests.yml` & `ampform-0.9.4/.github/workflows/ci-tests.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/workflows/linkcheck.yml` & `ampform-0.9.4/.github/workflows/linkcheck.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/workflows/pr-linting.yml` & `ampform-0.9.4/.github/workflows/pr-linting.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/workflows/requirements-cron.yml` & `ampform-0.9.4/.github/workflows/requirements-cron.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.github/workflows/requirements-pr.yml` & `ampform-0.9.4/.github/workflows/requirements-pr.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.gitignore` & `ampform-0.9.4/.gitignore`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.gitpod.yml` & `ampform-0.9.4/.gitpod.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.mypy.ini` & `ampform-0.9.4/.mypy.ini`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.pre-commit-config.yaml` & `ampform-0.9.4/.pre-commit-config.yaml`

 * *Files 0% similar despite different names*

```diff
@@ -43,15 +43,15 @@
 
   - repo: https://github.com/asottile/blacken-docs
     rev: v1.10.0
     hooks:
       - id: blacken-docs
 
   - repo: https://github.com/ComPWA/mirrors-cspell
-    rev: v5.6.0
+    rev: v5.6.3
     hooks:
       - id: cspell
 
   - repo: https://github.com/editorconfig-checker/editorconfig-checker.python
     rev: 2.3.5
     hooks:
       - id: editorconfig-checker
@@ -62,15 +62,15 @@
 
   - repo: https://github.com/igorshubovych/markdownlint-cli
     rev: v0.27.1
     hooks:
       - id: markdownlint
 
   - repo: https://github.com/nbQA-dev/nbQA
-    rev: 0.10.0
+    rev: 0.12.0
     hooks:
       - id: nbqa-black
         args: [--nbqa-mutate]
       - id: nbqa-flake8
         args: ["--extend-ignore=E402,F821"]
       - id: nbqa-isort
         args: [--nbqa-mutate]
@@ -83,15 +83,15 @@
   - repo: https://github.com/pre-commit/mirrors-prettier
     rev: v2.3.1
     hooks:
       - id: prettier
         language_version: 12.18.2 # prettier does not specify node correctly
 
   - repo: https://github.com/ComPWA/mirrors-pyright
-    rev: v1.1.147
+    rev: v1.1.148
     hooks:
       - id: pyright
 
   # The following tools have to be install locally, because they can also be
   # used by code editors (e.g. linting and format-on-save).
 
   - repo: local
```

### Comparing `ampform-0.9.3/.pylintrc` & `ampform-0.9.4/.pylintrc`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.vscode/extensions.json` & `ampform-0.9.4/.vscode/extensions.json`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/.vscode/settings.json` & `ampform-0.9.4/.vscode/settings.json`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/PKG-INFO` & `ampform-0.9.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ampform
-Version: 0.9.3
+Version: 0.9.4
 Summary: UNKNOWN
 Home-page: UNKNOWN
 Author: Common Partial Wave Analysis
 Author-email: compwa-admin@ep1.rub.de
 Maintainer-email: compwa-admin@ep1.rub.de
 License: GPLv3 or later
 Project-URL: Tracker, https://github.com/ComPWA/ampform/issues
```

### Comparing `ampform-0.9.3/README.md` & `ampform-0.9.4/README.md`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/codecov.yml` & `ampform-0.9.4/codecov.yml`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/Makefile` & `ampform-0.9.4/docs/Makefile`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/_static/favicon.ico` & `ampform-0.9.4/docs/_static/favicon.ico`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/_templates/genindex.html` & `ampform-0.9.4/docs/_templates/genindex.html`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/_templates/package.rst_t` & `ampform-0.9.4/docs/_templates/package.rst_t`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/abbreviate_signature.py` & `ampform-0.9.4/docs/abbreviate_signature.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/adr/template.md` & `ampform-0.9.4/docs/adr/template.md`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/bibliography.bib` & `ampform-0.9.4/docs/bibliography.bib`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/conf.py` & `ampform-0.9.4/docs/conf.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/extend_docstrings.py` & `ampform-0.9.4/docs/extend_docstrings.py`

 * *Files 6% similar despite different names*

```diff
@@ -10,19 +10,20 @@
 from typing import Callable, Type, Union
 
 import sympy as sp
 
 from ampform.dynamics import (
     BlattWeisskopfSquared,
     _analytic_continuation,
-    _phase_space_factor_hat,
     breakup_momentum_squared,
     coupled_width,
     phase_space_factor,
-    phase_space_factor_ac,
+    phase_space_factor_abs,
+    phase_space_factor_analytic,
+    phase_space_factor_complex,
     relativistic_breit_wigner,
     relativistic_breit_wigner_with_ff,
 )
 from ampform.dynamics.math import ComplexSqrt
 
 
 def update_docstring(
@@ -123,35 +124,61 @@
         :label: phase_space_factor
 
     with :math:`q^2(s)` defined as :eq:`breakup_momentum_squared`.
     """,
     )
 
 
-def render_phase_space_factor_ac() -> None:
-    s, m_a, m_b, rho_hat_symbol, q_squared_symbol = sp.symbols(
-        R"s, m_a, m_b, \hat{\rho}, q^{2}(s)"
+def render_phase_space_factor_abs() -> None:
+    s, m_a, m_b = sp.symbols("s, m_a, m_b")
+    rho_hat = phase_space_factor_abs(s, m_a, m_b)
+    q_squared = breakup_momentum_squared(s, m_a, m_b)
+    rho_hat = rho_hat.subs({4 * q_squared: 4 * sp.Symbol("q^{2}(s)")})
+    update_docstring(
+        phase_space_factor_abs,
+        fR"""
+
+    .. math:: \hat{{\rho}} = {sp.latex(rho_hat)}
+        :label: phase_space_factor_abs
+
+    with :math:`q^2(s)` defined as :eq:`breakup_momentum_squared`.
+    """,
     )
+
+
+def render_phase_space_factor_analytic() -> None:
+    s, m_a, m_b, rho_hat_symbol = sp.symbols(R"s, m_a, m_b, \hat{\rho}")
     rho_analytic = _analytic_continuation(
         rho_hat_symbol, s, s_threshold=(m_a + m_b) ** 2
     )
-    q_squared = breakup_momentum_squared(s, m_a, m_b)
-    rho_hat = _phase_space_factor_hat(s, m_a, m_b)
-    rho_hat_subs = rho_hat.subs(4 * q_squared, 4 * q_squared_symbol)
     update_docstring(
-        phase_space_factor_ac,
+        phase_space_factor_analytic,
         fR"""
     .. math:: {sp.latex(rho_analytic)}
-        :label: phase_space_factor_ac
+        :label: phase_space_factor_analytic
+
+    with :math:`\hat{{\rho}}` defined by :func:`.phase_space_factor_abs`
+    :eq:`phase_space_factor_abs`.
+    """,
+    )
 
-    with :math:`\hat{{\rho}}` a slightly adapted :func:`phase_space_factor`
-    that takes the absolute value of :func:`.breakup_momentum_squared`:
 
-    .. math:: {sp.latex(rho_hat_subs)}
-        :label: rho_hat
+def render_phase_space_factor_complex() -> None:
+    s, m_a, m_b = sp.symbols("s, m_a, m_b")
+    rho = phase_space_factor_complex(s, m_a, m_b)
+    q_squared = breakup_momentum_squared(s, m_a, m_b)
+    rho = rho.subs({4 * q_squared: 4 * sp.Symbol("q^{2}(s)")})
+    update_docstring(
+        phase_space_factor_complex,
+        fR"""
+
+    .. math:: \hat{{\rho}} = {sp.latex(rho)}
+        :label: phase_space_factor_complex
+
+    with :math:`q^2(s)` defined as :eq:`breakup_momentum_squared`.
     """,
     )
 
 
 def render_relativistic_breit_wigner() -> None:
     s, m0, w0 = sp.symbols("s m0 Gamma0")
     rel_bw = relativistic_breit_wigner(s, m0, w0)
```

### Comparing `ampform-0.9.3/docs/index.md` & `ampform-0.9.4/docs/index.md`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/install.md` & `ampform-0.9.4/docs/install.md`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/usage/amplitude.ipynb` & `ampform-0.9.4/docs/usage/amplitude.ipynb`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/usage/dynamics/analytic-continuation.ipynb` & `ampform-0.9.4/docs/usage/dynamics/analytic-continuation.ipynb`

 * *Files 9% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9679368764877371%*

 * *Differences: {"'cells'": "{8: {'source': ['The {func}`~sympy.functions.elementary.miscellaneous.sqrt` or "*

 * *            "{class}`.ComplexSqrt` of {func}`.breakup_momentum_squared`:']}, 12: {'source': "*

 * *            '["The \'normal\' {func}`.phase_space_factor` (the denominator makes the difference to '*

 * *            '{eq}`coupled_width`!):"]}, 14: {\'source\': {insert: [(1, \'Math(fR"\\\\rho(s) = '*

 * *            '{sp.latex(rho_subs)}")\')], delete: [1]}}, 16: {\'source\': [\'A '*

 * *            "{func}`.phase_space_factor_complex […]*

```diff
@@ -104,15 +104,22 @@
                 "from IPython.display import Math"
             ]
         },
         {
             "cell_type": "markdown",
             "metadata": {},
             "source": [
-                "1. The {func}`~sympy.functions.elementary.miscellaneous.sqrt` or `.ComplexSqrt` of {func}`.breakup_momentum_squared`:"
+                "### 1) Break-up momentum"
+            ]
+        },
+        {
+            "cell_type": "markdown",
+            "metadata": {},
+            "source": [
+                "The {func}`~sympy.functions.elementary.miscellaneous.sqrt` or {class}`.ComplexSqrt` of {func}`.breakup_momentum_squared`:"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
                 "tags": []
@@ -142,15 +149,22 @@
                 "Math(f\"{sp.latex(q_squared_symbol)} = {sp.latex(q_squared)}\")"
             ]
         },
         {
             "cell_type": "markdown",
             "metadata": {},
             "source": [
-                "2. The 'normal' {func}`.phase_space_factor` (the denominator makes the difference to {eq}`coupled_width`!):"
+                "### 2) 'Normal' phase space factor"
+            ]
+        },
+        {
+            "cell_type": "markdown",
+            "metadata": {},
+            "source": [
+                "The 'normal' {func}`.phase_space_factor` (the denominator makes the difference to {eq}`coupled_width`!):"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {},
             "outputs": [],
@@ -170,35 +184,82 @@
                 "tags": [
                     "hide-input"
                 ]
             },
             "outputs": [],
             "source": [
                 "rho_subs = rho.subs(4 * q_squared, 4 * q_squared_symbol)\n",
-                "Math(fR\"\\hat{{\\rho}}(s) = {sp.latex(rho_subs)}\")"
+                "Math(fR\"\\rho(s) = {sp.latex(rho_subs)}\")"
+            ]
+        },
+        {
+            "cell_type": "markdown",
+            "metadata": {},
+            "source": [
+                "### 3) 'Complex' phase space factor"
+            ]
+        },
+        {
+            "cell_type": "markdown",
+            "metadata": {},
+            "source": [
+                "A {func}`.phase_space_factor_complex` that uses {class}`.ComplexSqrt`:"
+            ]
+        },
+        {
+            "cell_type": "code",
+            "execution_count": null,
+            "metadata": {},
+            "outputs": [],
+            "source": [
+                "from ampform.dynamics import phase_space_factor_complex\n",
+                "\n",
+                "rho_complex = phase_space_factor_complex(s, m_a, m_b)"
+            ]
+        },
+        {
+            "cell_type": "code",
+            "execution_count": null,
+            "metadata": {
+                "jupyter": {
+                    "source_hidden": true
+                },
+                "tags": []
+            },
+            "outputs": [],
+            "source": [
+                "rho_complex_subs = rho_complex.subs(4 * q_squared, 4 * q_squared_symbol)\n",
+                "Math(fR\"\\rho_c(s) = {sp.latex(rho_complex_subs)}\")"
+            ]
+        },
+        {
+            "cell_type": "markdown",
+            "metadata": {},
+            "source": [
+                "### 4) 'Analytic continuation' of the phase space factor"
             ]
         },
         {
             "cell_type": "markdown",
             "metadata": {},
             "source": [
-                "3. The following 'case-by-case' **analytic continuation**, {func}`.phase_space_factor_ac`:"
+                "The following 'case-by-case' **analytic continuation**, {func}`.phase_space_factor_analytic`:"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
-                "from ampform.dynamics import phase_space_factor_ac\n",
+                "from ampform.dynamics import phase_space_factor_analytic\n",
                 "\n",
-                "rho_analytic = phase_space_factor_ac(s, m_a, m_b)"
+                "rho_analytic = phase_space_factor_analytic(s, m_a, m_b)"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
                 "jupyter": {
@@ -220,46 +281,42 @@
             "cell_type": "markdown",
             "metadata": {},
             "source": [
                 "with"
             ]
         },
         {
-            "cell_type": "markdown",
-            "metadata": {},
-            "source": [
-                ":::{margin}\n",
-                "\n",
-                "Mind the absolute value!\n",
-                "\n",
-                ":::"
-            ]
-        },
-        {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
                 "jupyter": {
                     "source_hidden": true
                 },
                 "tags": [
                     "remove-input"
                 ]
             },
             "outputs": [],
             "source": [
-                "from ampform.dynamics import _phase_space_factor_hat\n",
+                "from ampform.dynamics import phase_space_factor_abs\n",
                 "\n",
-                "rho_hat = _phase_space_factor_hat(s, m_a, m_b)\n",
+                "rho_hat = phase_space_factor_abs(s, m_a, m_b)\n",
                 "rho_hat_subs = rho_hat.subs(4 * q_squared, 4 * q_squared_symbol)\n",
                 "Math(f\"{sp.latex(rho_hat_symbol)} = {sp.latex(rho_hat_subs)}\")"
             ]
         },
         {
             "cell_type": "markdown",
+            "metadata": {},
+            "source": [
+                "(Mind the absolute value.)"
+            ]
+        },
+        {
+            "cell_type": "markdown",
             "metadata": {
                 "tags": []
             },
             "source": [
                 "## Visualization"
             ]
         },
@@ -284,40 +341,48 @@
                 "import symplot"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
+                "jupyter": {
+                    "source_hidden": true
+                },
                 "tags": []
             },
             "outputs": [],
             "source": [
+                "from ampform.dynamics import ComplexSqrt\n",
+                "\n",
                 "m = sp.Symbol(\"m\", real=True)\n",
-                "rho = phase_space_factor(m ** 2, m_a, m_b)\n",
-                "rho_ac = phase_space_factor_ac(m ** 2, m_a, m_b)\n",
-                "np_rho, sliders = symplot.prepare_sliders(plot_symbol=m, expression=rho)\n",
-                "np_rho_ac = sp.lambdify((m, m_a, m_b), rho_ac, \"numpy\")"
+                "rho_c = phase_space_factor_complex(m ** 2, m_a, m_b)\n",
+                "rho_ac = phase_space_factor_analytic(m ** 2, m_a, m_b)\n",
+                "np_rho_c, sliders = symplot.prepare_sliders(plot_symbol=m, expression=rho_c)\n",
+                "np_rho_ac = sp.lambdify((m, m_a, m_b), rho_ac, \"numpy\")\n",
+                "np_breakup_momentum = sp.lambdify(\n",
+                "    (m, m_a, m_b), ComplexSqrt(q_squared.subs(s, m ** 2)), \"numpy\"\n",
+                ")"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
-                "plot_domain = np.linspace(0, 3, 1_000)\n",
+                "plot_domain = np.linspace(0, 3, 500)\n",
                 "sliders.set_ranges(\n",
                 "    m_a=(0, 2, 200),\n",
                 "    m_b=(0, 2, 200),\n",
                 ")\n",
                 "sliders.set_values(\n",
-                "    m_a=0.8,\n",
+                "    m_a=0.6,\n",
                 "    m_b=1.25,\n",
                 ")"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
@@ -328,32 +393,14 @@
                 "tags": [
                     "remove-output",
                     "hide-input"
                 ]
             },
             "outputs": [],
             "source": [
-                "from ampform.dynamics import ComplexSqrt\n",
-                "\n",
-                "np_rho, sliders = symplot.prepare_sliders(plot_symbol=m, expression=rho)\n",
-                "np_rho_ac = sp.lambdify((m, m_a, m_b), rho_ac, \"numpy\")\n",
-                "np_breakup_momentum = sp.lambdify(\n",
-                "    (m, m_a, m_b), ComplexSqrt(q_squared.subs(s, m ** 2)), \"numpy\"\n",
-                ")\n",
-                "\n",
-                "plot_domain = np.linspace(0, 3, 500)\n",
-                "sliders.set_ranges(\n",
-                "    m_a=(0, 2, 200),\n",
-                "    m_b=(0, 2, 200),\n",
-                ")\n",
-                "sliders.set_values(\n",
-                "    m_a=0.6,\n",
-                "    m_b=1.25,\n",
-                ")\n",
-                "\n",
                 "fig, axes = plt.subplots(1, 3, figsize=[10, 4], tight_layout=True)\n",
                 "fig.canvas.toolbar_visible = False\n",
                 "\n",
                 "ax_q, ax_rho, ax_rho_ac = axes\n",
                 "for ax in axes:\n",
                 "    ax.set_xlabel(\"$m$\")\n",
                 "\n",
@@ -386,27 +433,27 @@
                 "    label=\"imaginary\",\n",
                 "    controls=controls,\n",
                 "    ylim=ylim_q,\n",
                 "    ax=ax_q,\n",
                 "    alpha=0.7,\n",
                 ")\n",
                 "\n",
-                "ax_rho.set_title(f\"${sp.latex(rho_subs)}$\")\n",
+                "ax_rho.set_title(f\"${sp.latex(rho_complex_subs)}$\")\n",
                 "iplt.plot(\n",
                 "    plot_domain,\n",
-                "    func_real(np_rho),\n",
+                "    func_real(np_rho_c),\n",
                 "    label=\"real\",\n",
                 "    controls=controls,\n",
                 "    ylim=ylim_rho,\n",
                 "    ax=ax_rho,\n",
                 "    alpha=0.7,\n",
                 ")\n",
                 "iplt.plot(\n",
                 "    plot_domain,\n",
-                "    func_imag(np_rho),\n",
+                "    func_imag(np_rho_c),\n",
                 "    label=\"imaginary\",\n",
                 "    controls=controls,\n",
                 "    ylim=ylim_rho,\n",
                 "    ax=ax_rho,\n",
                 "    alpha=0.7,\n",
                 ")\n",
                 "\n",
```

### Comparing `ampform-0.9.3/docs/usage/dynamics/custom.ipynb` & `ampform-0.9.4/docs/usage/dynamics/custom.ipynb`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/usage/dynamics/k-matrix.ipynb` & `ampform-0.9.4/docs/usage/dynamics/k-matrix.ipynb`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/usage/dynamics.ipynb` & `ampform-0.9.4/docs/usage/dynamics.ipynb`

 * *Files 7% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9929118981697618%*

 * *Differences: {"'cells'": "{24: {'source': {insert: [(1, '    phase_space_factor_analytic,\\n'), (13, '    "*

 * *            "phsp_factor=phase_space_factor_analytic,\\n')], delete: [13, 1]}}, 25: {'source': "*

 * *            "{insert: [(5, '    s, m0, w0, m_a, m_b, L, d, "*

 * *            "phsp_factor=phase_space_factor_analytic\\n')], delete: [5]}}, 27: {'source': {insert: "*

 * *            "[(13, '    phsp_factor=phase_space_factor_analytic,\\n')], delete: [13]}}, 28: "*

 * *            "{'source': {insert: [(3, 'rho = phase_space_factor_ […]*

```diff
@@ -377,27 +377,27 @@
             "execution_count": null,
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
                 "from ampform.dynamics import (\n",
-                "    phase_space_factor_ac,\n",
+                "    phase_space_factor_analytic,\n",
                 "    relativistic_breit_wigner_with_ff,\n",
                 ")\n",
                 "\n",
                 "rel_bw_with_ff = relativistic_breit_wigner_with_ff(\n",
                 "    s=s,\n",
                 "    mass0=m0,\n",
                 "    gamma0=w0,\n",
                 "    m_a=m_a,\n",
                 "    m_b=m_b,\n",
                 "    angular_momentum=L,\n",
                 "    meson_radius=d,\n",
-                "    phsp_factor=phase_space_factor_ac,\n",
+                "    phsp_factor=phase_space_factor_analytic,\n",
                 ")"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
@@ -411,15 +411,15 @@
             "outputs": [],
             "source": [
                 "from ampform.dynamics import coupled_width\n",
                 "\n",
                 "q_squared = breakup_momentum_squared(s, m_a, m_b)\n",
                 "ff_sq = BlattWeisskopfSquared(L, z=q_squared * d ** 2)\n",
                 "mass_dependent_width = coupled_width(\n",
-                "    s, m0, w0, m_a, m_b, L, d, phsp_factor=phase_space_factor_ac\n",
+                "    s, m0, w0, m_a, m_b, L, d, phsp_factor=phase_space_factor_analytic\n",
                 ")\n",
                 "rel_bw_with_ff.subs(\n",
                 "    {\n",
                 "        2 * q_squared: 2 * sp.Symbol(\"q^{2}(m)\"),\n",
                 "        ff_sq: sp.Symbol(R\"B_{L}^{2}\\left(q\\right)\"),\n",
                 "        mass_dependent_width: sp.Symbol(R\"\\Gamma(m)\"),\n",
                 "    }\n",
@@ -450,15 +450,15 @@
                 "    s=s,\n",
                 "    mass0=m0,\n",
                 "    gamma0=w0,\n",
                 "    m_a=m_a,\n",
                 "    m_b=m_b,\n",
                 "    angular_momentum=L,\n",
                 "    meson_radius=d,\n",
-                "    phsp_factor=phase_space_factor_ac,\n",
+                "    phsp_factor=phase_space_factor_analytic,\n",
                 ")"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
@@ -470,16 +470,16 @@
                 ]
             },
             "outputs": [],
             "source": [
                 "q0_squared = breakup_momentum_squared(m0 ** 2, m_a, m_b)\n",
                 "ff = BlattWeisskopfSquared(L, z=q_squared * d ** 2)\n",
                 "ff0_sq = BlattWeisskopfSquared(L, z=q0_squared * d ** 2)\n",
-                "rho = phase_space_factor_ac(s, m_a, m_b)\n",
-                "rho0 = phase_space_factor_ac(m0 ** 2, m_a, m_b)\n",
+                "rho = phase_space_factor_analytic(s, m_a, m_b)\n",
+                "rho0 = phase_space_factor_analytic(m0 ** 2, m_a, m_b)\n",
                 "running_width = running_width.subs(\n",
                 "    {\n",
                 "        rho / rho0: sp.Symbol(R\"\\rho(m)\") / sp.Symbol(R\"\\rho(m_{0})\"),\n",
                 "        ff: sp.Symbol(\"B_{L}(q)\"),\n",
                 "        ff0_sq: sp.Symbol(\"B_{L}(q_{0})\"),\n",
                 "    },\n",
                 ")\n",
@@ -495,156 +495,185 @@
         },
         {
             "cell_type": "markdown",
             "metadata": {
                 "tags": []
             },
             "source": [
-                "### Comparison"
+                "### Analytic continuation"
+            ]
+        },
+        {
+            "cell_type": "markdown",
+            "metadata": {},
+            "source": [
+                "The following shows the effect of {doc}`/usage/dynamics/analytic-continuation` a on relativistic Breit-Wigner:"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": null,
             "metadata": {
                 "jupyter": {
                     "source_hidden": true
                 },
                 "tags": [
-                    "remove-cell"
+                    "hide-cell",
+                    "remove-output"
                 ]
             },
             "outputs": [],
             "source": [
+                "from ampform.dynamics import phase_space_factor_complex\n",
+                "\n",
+                "# Two types of relativistic Breit-Wigners\n",
+                "rel_bw_with_ff = relativistic_breit_wigner_with_ff(\n",
+                "    s=s,\n",
+                "    mass0=m0,\n",
+                "    gamma0=w0,\n",
+                "    m_a=m_a,\n",
+                "    m_b=m_b,\n",
+                "    angular_momentum=L,\n",
+                "    meson_radius=d,\n",
+                "    phsp_factor=phase_space_factor_complex,\n",
+                ")\n",
+                "rel_bw_with_ff_ac = relativistic_breit_wigner_with_ff(\n",
+                "    s=s,\n",
+                "    mass0=m0,\n",
+                "    gamma0=w0,\n",
+                "    m_a=m_a,\n",
+                "    m_b=m_b,\n",
+                "    angular_momentum=L,\n",
+                "    meson_radius=d,\n",
+                "    phsp_factor=phase_space_factor_analytic,\n",
+                ")\n",
+                "\n",
+                "# Lambdify\n",
                 "np_rel_bw_with_ff, sliders = symplot.prepare_sliders(\n",
                 "    plot_symbol=m,\n",
                 "    expression=rel_bw_with_ff.doit(),\n",
                 ")\n",
-                "np_rel_bw = sp.lambdify((m, w0, L, d, m0, m_a, m_b), rel_bw.doit())"
-            ]
-        },
-        {
-            "cell_type": "code",
-            "execution_count": null,
-            "metadata": {
-                "tags": [
-                    "remove-cell"
-                ]
-            },
-            "outputs": [],
-            "source": [
-                "plot_domain = np.linspace(\n",
-                "    start=0,\n",
-                "    stop=4,\n",
-                "    num=500,\n",
+                "np_rel_bw_with_ff_ac = sp.lambdify(\n",
+                "    args=(m, w0, L, d, m0, m_a, m_b),\n",
+                "    expr=rel_bw_with_ff_ac.doit(),\n",
+                ")\n",
+                "np_rel_bw = sp.lambdify(\n",
+                "    args=(m, w0, L, d, m0, m_a, m_b),\n",
+                "    expr=rel_bw.doit(),\n",
                 ")\n",
+                "\n",
+                "# Set sliders\n",
+                "plot_domain = np.linspace(start=0, stop=4, num=500)\n",
                 "sliders.set_ranges(\n",
-                "    m0=(0, 5, 500),\n",
+                "    m0=(0, 4, 200),\n",
                 "    Gamma0=(0, 1, 100),\n",
                 "    L=(0, 8),\n",
                 "    m_a=(0, 2, 200),\n",
                 "    m_b=(0, 2, 200),\n",
                 "    d=(0, 5),\n",
                 ")\n",
                 "sliders.set_values(\n",
                 "    m0=1.8,\n",
                 "    Gamma0=0.6,\n",
                 "    L=1,\n",
                 "    m_a=0.7,\n",
                 "    m_b=0.5,\n",
                 "    d=1,\n",
-                ")"
-            ]
-        },
-        {
-            "cell_type": "code",
-            "execution_count": null,
-            "metadata": {
-                "jupyter": {
-                    "source_hidden": true
-                },
-                "tags": [
-                    "hide-input",
-                    "remove-output"
-                ]
-            },
-            "outputs": [],
-            "source": [
-                "fig, axes = plt.subplots(2, 1, figsize=(8, 6), sharex=True)\n",
-                "ax_real, ax_imag = axes\n",
-                "ax_imag.set_xlabel(\"$m$\")\n",
-                "ax_real.set_ylabel(R\"$\\left|A\\right|^2$\")\n",
-                "ax_imag.set_ylabel(R\"Im$\\left(A\\right)$\")\n",
+                ")\n",
+                "\n",
+                "fig, axes = plt.subplots(\n",
+                "    nrows=2,\n",
+                "    figsize=(8, 6),\n",
+                "    sharex=True,\n",
+                "    #     gridspec_kw={\"height_ratios\": [1, 1.8]},\n",
+                ")\n",
+                "ax_ff, ax_ac = axes\n",
+                "ax_ac.set_xlabel(\"$m$\")\n",
+                "for ax in axes:\n",
+                "    ax.axhline(0, c=\"gray\", linewidth=0.5)\n",
+                "\n",
+                "rho_c = phase_space_factor_complex(m, m_a, m_b)\n",
+                "q_squared = breakup_momentum_squared(m, m_a, m_b)\n",
+                "rho_c_math = rho_c.subs(q_squared, sp.Symbol(\"q^{2}(m)\"))\n",
+                "ax_ff.set_title(f\"'Complex' phase space factor: ${sp.latex(rho_c_math)}$\")\n",
+                "ax_ac.set_title(\"Analytic continuation of the phase space factor\")\n",
                 "\n",
-                "# Real\n",
-                "ylim = (0, 1.1)\n",
+                "ylim = \"auto\"  # (-0.6, 1.2)\n",
                 "controls = iplt.plot(\n",
                 "    plot_domain,\n",
-                "    lambda *args, **kwargs: np.abs(np_rel_bw_with_ff(*args, **kwargs)) ** 2,\n",
-                "    label=\"analytic continuation\",\n",
+                "    lambda *args, **kwargs: np_rel_bw_with_ff(*args, **kwargs).real,\n",
+                "    label=\"real\",\n",
                 "    **sliders,\n",
                 "    ylim=ylim,\n",
-                "    ax=ax_real,\n",
-                "    linestyle=\"dotted\",\n",
-                "    c=\"C0\",\n",
+                "    ax=ax_ff,\n",
                 ")\n",
                 "iplt.plot(\n",
                 "    plot_domain.real,\n",
-                "    lambda *args, **kwargs: np.abs(np_rel_bw_with_ff(*args, **kwargs)) ** 2,\n",
-                "    label=\"$with$ form factor\",\n",
+                "    lambda *args, **kwargs: np_rel_bw_with_ff(*args, **kwargs).imag,\n",
+                "    label=\"imaginary\",\n",
                 "    controls=controls,\n",
                 "    ylim=ylim,\n",
-                "    ax=ax_real,\n",
+                "    ax=ax_ff,\n",
                 ")\n",
                 "iplt.plot(\n",
                 "    plot_domain.real,\n",
-                "    lambda *args, **kwargs: np.abs(np_rel_bw(*args, **kwargs)) ** 2,\n",
-                "    label=\"non-relativistic Breit-Wigner\",\n",
+                "    lambda *args, **kwargs: np.abs(np_rel_bw_with_ff(*args, **kwargs)) ** 2,\n",
+                "    label=\"absolute\",\n",
                 "    controls=controls,\n",
                 "    ylim=ylim,\n",
-                "    ax=ax_real,\n",
+                "    ax=ax_ff,\n",
+                "    c=\"black\",\n",
+                "    linestyle=\"dotted\",\n",
                 ")\n",
-                "iplt.axvline(controls[\"m0\"], c=\"gray\", linestyle=\"dotted\")\n",
                 "\n",
-                "# Imaginary\n",
+                "\n",
                 "iplt.plot(\n",
-                "    plot_domain,\n",
-                "    lambda *args, **kwargs: np_rel_bw_with_ff(*args, **kwargs).imag,\n",
-                "    label=\"analytic continuation\",\n",
+                "    plot_domain.real,\n",
+                "    lambda *args, **kwargs: np_rel_bw_with_ff_ac(*args, **kwargs).real,\n",
+                "    label=\"real\",\n",
                 "    controls=controls,\n",
                 "    ylim=ylim,\n",
-                "    ax=ax_imag,\n",
-                "    alpha=0.5,\n",
-                "    linestyle=\"dotted\",\n",
-                "    c=\"C0\",\n",
+                "    ax=ax_ac,\n",
                 ")\n",
                 "iplt.plot(\n",
                 "    plot_domain.real,\n",
-                "    lambda *args, **kwargs: np_rel_bw_with_ff(*args, **kwargs).imag,\n",
-                "    label=\"$with$ form factor\",\n",
+                "    lambda *args, **kwargs: np_rel_bw_with_ff_ac(*args, **kwargs).imag,\n",
+                "    label=\"imaginary\",\n",
                 "    controls=controls,\n",
                 "    ylim=ylim,\n",
-                "    ax=ax_imag,\n",
+                "    ax=ax_ac,\n",
                 ")\n",
                 "iplt.plot(\n",
                 "    plot_domain.real,\n",
-                "    lambda *args, **kwargs: np_rel_bw(*args, **kwargs).imag,\n",
-                "    label=\"non-relativistic Breit-Wigner\",\n",
+                "    lambda *args, **kwargs: np.abs(np_rel_bw_with_ff_ac(*args, **kwargs)) ** 2,\n",
+                "    label=\"absolute\",\n",
                 "    controls=controls,\n",
                 "    ylim=ylim,\n",
-                "    ax=ax_imag,\n",
+                "    ax=ax_ac,\n",
+                "    c=\"black\",\n",
+                "    linestyle=\"dotted\",\n",
                 ")\n",
-                "iplt.axvline(controls[\"m0\"], c=\"gray\", linestyle=\"dotted\")\n",
                 "\n",
-                "ax_real.legend(loc=\"upper right\")\n",
-                "iplt.title(\n",
-                "    R\"$m_0={m0:.1f} \\qquad \\Gamma_0={Gamma0:.1f} \\qquad L={L} \\qquad m_a={m_a:.1f} \\qquad m_b={m_b:.1f}$\",\n",
-                "    controls=controls,\n",
-                "    ax=ax_real,\n",
-                ")\n",
+                "for ax in axes:\n",
+                "    iplt.axvline(\n",
+                "        controls[\"m0\"],\n",
+                "        ax=ax,\n",
+                "        c=\"red\",\n",
+                "        label=f\"${sp.latex(m0)}$\",\n",
+                "        alpha=0.3,\n",
+                "    )\n",
+                "    iplt.axvline(\n",
+                "        lambda m_a, m_b, **kwargs: m_a + m_b,\n",
+                "        controls=controls,\n",
+                "        ax=ax,\n",
+                "        c=\"black\",\n",
+                "        alpha=0.3,\n",
+                "        label=f\"${sp.latex(m_a)} + {sp.latex(m_b)}$\",\n",
+                "    )\n",
+                "ax_ac.legend(loc=\"upper right\")\n",
                 "fig.tight_layout()\n",
                 "plt.show()"
             ]
         },
         {
             "cell_type": "markdown",
             "metadata": {},
```

### Comparing `ampform-0.9.3/docs/usage/interactive.ipynb` & `ampform-0.9.4/docs/usage/interactive.ipynb`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/docs/usage/symplot.ipynb` & `ampform-0.9.4/docs/usage/symplot.ipynb`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/pytest.ini` & `ampform-0.9.4/pytest.ini`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/setup.cfg` & `ampform-0.9.4/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -96,14 +96,15 @@
 	pylint >= 2.5  # good-names-rgxs
 	radon
 sty = 
 	%(format)s
 	%(lint)s
 	%(test)s  # for pytest type hints
 	pre-commit >= 1.4.0
+	types-docutils
 dev = 
 	%(all)s
 	%(doc)s
 	%(sty)s
 	%(test)s
 	aquirdturtle_collapsible_headings
 	jupyterlab
```

### Comparing `ampform-0.9.3/src/ampform/__init__.py` & `ampform-0.9.4/src/ampform/__init__.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/src/ampform/_graph_info.py` & `ampform-0.9.4/src/ampform/_graph_info.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/src/ampform/data.py` & `ampform-0.9.4/src/ampform/data.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/src/ampform/dynamics/__init__.py` & `ampform-0.9.4/src/ampform/dynamics/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -176,67 +176,71 @@
 
 
 class PhaseSpaceFactor(Protocol):
     """Protocol that is used by :func:`.coupled_width`.
 
     Use this `~typing.Protocol` when defining other implementations of a phase
     space factor. Compare for instance :func:`.phase_space_factor` and
-    :func:`.phase_space_factor_ac`.
+    :func:`.phase_space_factor_analytic`.
     """
 
     def __call__(
         self, s: sp.Symbol, m_a: sp.Symbol, m_b: sp.Symbol
     ) -> sp.Expr:
         """Expected `~inspect.signature`."""
         ...
 
 
 def phase_space_factor(
     s: sp.Symbol, m_a: sp.Symbol, m_b: sp.Symbol
 ) -> sp.Expr:
     """Standard phase-space factor, using :func:`breakup_momentum_squared`.
 
-    See :pdg-review:`2020; Resonances; p.4`, Equation (49.8), with a slight
-    adaptation: instead of a normal square root, this phase space factor make
-    use of :eq:`ComplexSqrt` (`.ComplexSqrt`).
+    See :pdg-review:`2020; Resonances; p.4`, Equation (49.8).
     """
     q_squared = breakup_momentum_squared(s, m_a, m_b)
     denominator = _phase_space_factor_denominator(s)
-    return ComplexSqrt(q_squared) / denominator
+    return sp.sqrt(q_squared) / denominator
 
 
-def phase_space_factor_ac(
+def phase_space_factor_abs(
+    s: sp.Symbol, m_a: sp.Symbol, m_b: sp.Symbol
+) -> sp.Expr:
+    r"""Phase space factor square root over the absolute value.
+
+    As opposed to :func:`.phase_space_factor`, this takes the
+    `~sympy.functions.elementary.complexes.Abs` value of
+    :func:`.breakup_momentum_squared`, then the
+    :func:`~sympy.functions.elementary.miscellaneous.sqrt`.
+
+    This version of the phase space factor is often denoted as
+    :math:`\hat{\rho}` and is used in analytic continuation
+    (:func:`.phase_space_factor_analytic`).
+    """
+    q_squared = breakup_momentum_squared(s, m_a, m_b)
+    denominator = _phase_space_factor_denominator(s)
+    return sp.sqrt(sp.Abs(q_squared)) / denominator
+
+
+def phase_space_factor_analytic(
     s: sp.Symbol, m_a: sp.Symbol, m_b: sp.Symbol
 ) -> sp.Expr:
     """Analytic continuation for the :func:`phase_space_factor`.
 
     See :pdg-review:`2014; Resonances; p.8` and
     :doc:`/usage/dynamics/analytic-continuation`.
 
     **Warning**: The PDG specifically derives this formula for a two-body decay
     *with equal masses*.
     """
-    rho_hat = _phase_space_factor_hat(s, m_a, m_b)
+    rho_hat = phase_space_factor_abs(s, m_a, m_b)
     s_threshold = (m_a + m_b) ** 2
     return _analytic_continuation(rho_hat, s, s_threshold)
 
 
-def _phase_space_factor_hat(
-    s: sp.Symbol, m_a: sp.Symbol, m_b: sp.Symbol
-) -> sp.Expr:
-    """Phase space factor used in the analytic continuation."""
-    q_squared = breakup_momentum_squared(s, m_a, m_b)
-    denominator = _phase_space_factor_denominator(s)
-    return sp.sqrt(sp.Abs(q_squared)) / denominator
-
-
-def _phase_space_factor_denominator(s: sp.Symbol) -> sp.Expr:
-    return 8 * sp.pi * sp.sqrt(s)
-
-
 def _analytic_continuation(
     rho: sp.Symbol, s: sp.Symbol, s_threshold: sp.Symbol
 ) -> sp.Expr:
     return sp.Piecewise(
         (
             sp.I * rho / sp.pi * sp.log(sp.Abs((1 + rho) / (1 - rho))),
             s < 0,
@@ -248,14 +252,31 @@
         (
             2 * sp.I * rho / sp.pi * sp.atan(1 / rho),
             True,
         ),
     )
 
 
+def phase_space_factor_complex(
+    s: sp.Symbol, m_a: sp.Symbol, m_b: sp.Symbol
+) -> sp.Expr:
+    """Phase-space factor with `.ComplexSqrt`.
+
+    Same as :func:`phase_space_factor`, but using a `.ComplexSqrt` that does
+    have defined behavior for defined for negative input values.
+    """
+    q_squared = breakup_momentum_squared(s, m_a, m_b)
+    denominator = _phase_space_factor_denominator(s)
+    return ComplexSqrt(q_squared) / denominator
+
+
+def _phase_space_factor_denominator(s: sp.Symbol) -> sp.Expr:
+    return 8 * sp.pi * sp.sqrt(s)
+
+
 def coupled_width(  # pylint: disable=too-many-arguments
     s: sp.Symbol,
     mass0: sp.Symbol,
     gamma0: sp.Symbol,
     m_a: sp.Symbol,
     m_b: sp.Symbol,
     angular_momentum: sp.Symbol,
```

### Comparing `ampform-0.9.3/src/ampform/dynamics/builder.py` & `ampform-0.9.4/src/ampform/dynamics/builder.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 from qrules.particle import Particle
 
 from . import (
     BlattWeisskopfSquared,
     PhaseSpaceFactor,
     breakup_momentum_squared,
     phase_space_factor,
-    phase_space_factor_ac,
+    phase_space_factor_analytic,
     relativistic_breit_wigner,
     relativistic_breit_wigner_with_ff,
 )
 
 # pyright: reportUnusedImport=false
 from .decorator import verify_signature  # noqa: F401
 
@@ -163,14 +163,14 @@
 
 
 create_relativistic_breit_wigner_with_ff = _make_relativistic_breit_wigner_with_ff(
     phsp_factor=phase_space_factor,
     docstring="Create a `.relativistic_breit_wigner_with_ff` for a two-body decay.",
 )
 create_analytic_breit_wigner = _make_relativistic_breit_wigner_with_ff(
-    phsp_factor=phase_space_factor_ac,
+    phsp_factor=phase_space_factor_analytic,
     docstring="""
 Create a `.relativistic_breit_wigner_with_ff` with analytic continuation.
 
 .. seealso:: :doc:`/usage/dynamics/analytic-continuation`.
 """,
 )
```

### Comparing `ampform-0.9.3/src/ampform/dynamics/decorator.py` & `ampform-0.9.4/src/ampform/dynamics/decorator.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/src/ampform/dynamics/math.py` & `ampform-0.9.4/src/ampform/dynamics/math.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/src/ampform/helicity.py` & `ampform-0.9.4/src/ampform/helicity.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/src/ampform/kinematics.py` & `ampform-0.9.4/src/ampform/kinematics.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/src/ampform.egg-info/PKG-INFO` & `ampform-0.9.4/src/ampform.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ampform
-Version: 0.9.3
+Version: 0.9.4
 Summary: UNKNOWN
 Home-page: UNKNOWN
 Author: Common Partial Wave Analysis
 Author-email: compwa-admin@ep1.rub.de
 Maintainer-email: compwa-admin@ep1.rub.de
 License: GPLv3 or later
 Project-URL: Tracker, https://github.com/ComPWA/ampform/issues
```

### Comparing `ampform-0.9.3/src/ampform.egg-info/SOURCES.txt` & `ampform-0.9.4/src/ampform.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/src/ampform.egg-info/requires.txt` & `ampform-0.9.4/src/ampform.egg-info/requires.txt`

 * *Files 6% similar despite different names*

```diff
@@ -43,14 +43,15 @@
 ipywidgets
 pytest
 pytest-cov
 pytest-notebook
 pytest-profiling
 pytest-xdist
 pre-commit>=1.4.0
+types-docutils
 ipywidgets
 pytest
 pytest-cov
 pytest-notebook
 pytest-profiling
 pytest-xdist
 aquirdturtle_collapsible_headings
@@ -120,14 +121,15 @@
 ipywidgets
 pytest
 pytest-cov
 pytest-notebook
 pytest-profiling
 pytest-xdist
 pre-commit>=1.4.0
+types-docutils
 
 [test]
 ipywidgets
 pytest
 pytest-cov
 pytest-notebook
 pytest-profiling
```

### Comparing `ampform-0.9.3/src/symplot/__init__.py` & `ampform-0.9.4/src/symplot/__init__.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/conftest.py` & `ampform-0.9.4/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/external/test_sympy.py` & `ampform-0.9.4/tests/external/test_sympy.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/symplot/test_ipywidgets.py` & `ampform-0.9.4/tests/symplot/test_ipywidgets.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/symplot/test_symplot.py` & `ampform-0.9.4/tests/symplot/test_symplot.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/test_angular_distributions.py` & `ampform-0.9.4/tests/test_angular_distributions.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/test_angular_momentum.py` & `ampform-0.9.4/tests/test_angular_momentum.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/test_data.py` & `ampform-0.9.4/tests/test_data.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/test_dynamics.py` & `ampform-0.9.4/tests/test_dynamics.py`

 * *Files 5% similar despite different names*

```diff
@@ -76,22 +76,20 @@
 
     expression = round_nested(expression, n_decimals=2)
     expression = round_nested(expression, n_decimals=2)
 
     expression = sp.piecewise_fold(expression)
     assert isinstance(expression, sp.Add)
     a1, a2 = tuple(map(str, expression.args))
-    a1 = a1.replace("ComplexSqrt", "sqrt")
-    a2 = a2.replace("ComplexSqrt", "sqrt")
     if formalism == "canonical":
-        assert a1 == "0.08/(-m**2 + 0.98 - 0.12*I*sqrt(m**2/4 - 0.02)/Abs(m))"
-        assert a2 == "0.23/(-m**2 + 2.27 - 0.34*I*sqrt(m**2/4 - 0.02)/Abs(m))"
+        assert a1 == "0.08/(-m**2 - 0.06*I*sqrt(m**2 - 0.07)/Abs(m) + 0.98)"
+        assert a2 == "0.23/(-m**2 - 0.17*I*sqrt(m**2 - 0.07)/Abs(m) + 2.27)"
     elif formalism == "helicity":
-        assert a1 == "0.17/(-m**2 + 2.27 - 0.34*I*sqrt(m**2/4 - 0.02)/Abs(m))"
-        assert a2 == "0.06/(-m**2 + 0.98 - 0.12*I*sqrt(m**2/4 - 0.02)/Abs(m))"
+        assert a1 == "0.17/(-m**2 - 0.17*I*sqrt(m**2 - 0.07)/Abs(m) + 2.27)"
+        assert a2 == "0.06/(-m**2 - 0.06*I*sqrt(m**2 - 0.07)/Abs(m) + 0.98)"
     else:
         raise NotImplementedError
 
 
 def round_nested(expression: sp.Expr, n_decimals: int) -> sp.Expr:
     for node in preorder_traversal(expression):
         if node.free_symbols:
```

### Comparing `ampform-0.9.3/tests/test_graph_info.py` & `ampform-0.9.4/tests/test_graph_info.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/test_helicity.py` & `ampform-0.9.4/tests/test_helicity.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/test_kinematics.py` & `ampform-0.9.4/tests/test_kinematics.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tests/test_parity_prefactor.py` & `ampform-0.9.4/tests/test_parity_prefactor.py`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/tox.ini` & `ampform-0.9.4/tox.ini`

 * *Files identical despite different names*

### Comparing `ampform-0.9.3/typings/README.md` & `ampform-0.9.4/typings/README.md`

 * *Files identical despite different names*

