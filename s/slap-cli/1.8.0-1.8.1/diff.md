# Comparing `tmp/slap_cli-1.8.0.tar.gz` & `tmp/slap_cli-1.8.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "slap_cli-1.8.0.tar", max compression
+gzip compressed data, was "slap_cli-1.8.1.tar", max compression
```

## Comparing `slap_cli-1.8.0.tar` & `slap_cli-1.8.1.tar`

### file list

```diff
@@ -1,62 +1,61 @@
--rw-r--r--   0        0        0     1002 2023-05-13 10:33:37.160056 slap_cli-1.8.0/LICENSE
--rw-r--r--   0        0        0     4682 2023-05-13 17:03:04.948662 slap_cli-1.8.0/pyproject.toml
--rw-r--r--   0        0        0     6005 2023-05-13 10:33:37.164056 slap_cli-1.8.0/readme.md
--rw-r--r--   0        0        0       98 2023-05-13 17:03:04.960662 slap_cli-1.8.0/src/slap/__init__.py
--rw-r--r--   0        0        0       82 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/__main__.py
--rw-r--r--   0        0        0    10314 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/application.py
--rw-r--r--   0        0        0     9163 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/changelog.py
--rw-r--r--   0        0        0     3353 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/check.py
--rw-r--r--   0        0        0     2520 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/configuration.py
--rw-r--r--   0        0        0     5337 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/add.py
--rw-r--r--   0        0        0    27292 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/changelog.py
--rw-r--r--   0        0        0     6202 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/check.py
--rw-r--r--   0        0        0     3049 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/info.py
--rw-r--r--   0        0        0     4793 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/ext/application/init.py
--rw-r--r--   0        0        0    14043 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/install.py
--rw-r--r--   0        0        0     5930 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/link.py
--rw-r--r--   0        0        0     4102 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/publish.py
--rw-r--r--   0        0        0    21301 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/release.py
--rw-r--r--   0        0        0     3344 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/report.py
--rw-r--r--   0        0        0     3521 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/run.py
--rw-r--r--   0        0        0     7789 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/test.py
--rw-r--r--   0        0        0    19021 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/application/venv.py
--rw-r--r--   0        0        0     2075 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/checks/changelog.py
--rw-r--r--   0        0        0     2215 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/checks/general.py
--rw-r--r--   0        0        0     6060 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/checks/poetry.py
--rw-r--r--   0        0        0     2812 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/checks/release.py
--rw-r--r--   0        0        0     8491 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/project_handlers/base.py
--rw-r--r--   0        0        0     3799 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/project_handlers/flit.py
--rw-r--r--   0        0        0     6462 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/project_handlers/poetry.py
--rw-r--r--   0        0        0     5751 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/project_handlers/setuptools.py
--rw-r--r--   0        0        0     1208 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/release/changelog.py
--rw-r--r--   0        0        0     2046 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/release/source_code_version.py
--rw-r--r--   0        0        0    16205 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/ext/repository_ci/github_actions.py
--rw-r--r--   0        0        0     4065 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/repository_handlers/default.py
--rw-r--r--   0        0        0     4479 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/repository_hosts/github.py
--rw-r--r--   0        0        0     1357 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/version_incrementing_rule.py
--rw-r--r--   0        0        0    10869 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/install/installer.py
--rw-r--r--   0        0        0     8244 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/plugins.py
--rw-r--r--   0        0        0     7835 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/project.py
--rw-r--r--   0        0        0        0 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/py.typed
--rw-r--r--   0        0        0    14700 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/python/dependency.py
--rw-r--r--   0        0        0     9711 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/python/environment.py
--rw-r--r--   0        0        0     6833 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/python/pep508.py
--rw-r--r--   0        0        0     2535 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/release.py
--rw-r--r--   0        0        0     5092 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/repository.py
--rw-r--r--   0        0        0     1105 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/github-actions/.github/workflows/changelog.yaml
--rw-r--r--   0        0        0      955 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/github-actions/.github/workflows/python.yaml
--rw-r--r--   0        0        0      208 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/.flake8
--rw-r--r--   0        0        0       78 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/.gitignore
--rw-r--r--   0        0        0        0 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/LICENSE
--rw-r--r--   0        0        0        9 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/README.md
--rw-r--r--   0        0        0     1451 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/pyproject.toml
--rw-r--r--   0        0        0       22 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/src/{path}/__init__.py
--rw-r--r--   0        0        0        0 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/src/{path}/py.typed
--rw-r--r--   0        0        0       67 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/tests/test_import.py
--rw-r--r--   0        0        0     1847 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/cleo.py
--rw-r--r--   0        0        0     4309 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/external/licenses.py
--rw-r--r--   0        0        0     2172 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/external/pypi_classifiers.py
--rw-r--r--   0        0        0      418 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/pygments.py
--rw-r--r--   0        0        0     2113 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/toml_file.py
--rw-r--r--   0        0        0     7363 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/vcs.py
--rw-r--r--   0        0        0     7548 1970-01-01 00:00:00.000000 slap_cli-1.8.0/PKG-INFO
+-rw-r--r--   0        0        0     1002 2023-05-13 10:33:37.160056 slap_cli-1.8.1/LICENSE
+-rw-r--r--   0        0        0     4974 2023-05-13 19:14:08.329715 slap_cli-1.8.1/pyproject.toml
+-rw-r--r--   0        0        0       98 2023-05-13 19:14:08.333715 slap_cli-1.8.1/src/slap/__init__.py
+-rw-r--r--   0        0        0       82 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/__main__.py
+-rw-r--r--   0        0        0    10314 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/application.py
+-rw-r--r--   0        0        0     9163 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/changelog.py
+-rw-r--r--   0        0        0     3353 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/check.py
+-rw-r--r--   0        0        0     2520 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/configuration.py
+-rw-r--r--   0        0        0     5337 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/add.py
+-rw-r--r--   0        0        0    27292 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/changelog.py
+-rw-r--r--   0        0        0     6202 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/check.py
+-rw-r--r--   0        0        0     3049 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/info.py
+-rw-r--r--   0        0        0     4783 2023-05-13 18:51:06.372905 slap_cli-1.8.1/src/slap/ext/application/init.py
+-rw-r--r--   0        0        0    14043 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/install.py
+-rw-r--r--   0        0        0     5930 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/link.py
+-rw-r--r--   0        0        0     4102 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/publish.py
+-rw-r--r--   0        0        0    21301 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/release.py
+-rw-r--r--   0        0        0     3344 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/report.py
+-rw-r--r--   0        0        0     3521 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/run.py
+-rw-r--r--   0        0        0     7789 2023-05-13 10:33:37.164056 slap_cli-1.8.1/src/slap/ext/application/test.py
+-rw-r--r--   0        0        0    19021 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/application/venv.py
+-rw-r--r--   0        0        0     2075 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/checks/changelog.py
+-rw-r--r--   0        0        0     2215 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/checks/general.py
+-rw-r--r--   0        0        0     6060 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/checks/poetry.py
+-rw-r--r--   0        0        0     2812 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/checks/release.py
+-rw-r--r--   0        0        0     8491 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/project_handlers/base.py
+-rw-r--r--   0        0        0     3799 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/project_handlers/flit.py
+-rw-r--r--   0        0        0     6462 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/project_handlers/poetry.py
+-rw-r--r--   0        0        0     5751 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/project_handlers/setuptools.py
+-rw-r--r--   0        0        0     1208 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/release/changelog.py
+-rw-r--r--   0        0        0     2046 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/release/source_code_version.py
+-rw-r--r--   0        0        0    16205 2023-05-13 17:02:56.460903 slap_cli-1.8.1/src/slap/ext/repository_ci/github_actions.py
+-rw-r--r--   0        0        0     4065 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/repository_handlers/default.py
+-rw-r--r--   0        0        0     4479 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/repository_hosts/github.py
+-rw-r--r--   0        0        0     1357 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/ext/version_incrementing_rule.py
+-rw-r--r--   0        0        0    10869 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/install/installer.py
+-rw-r--r--   0        0        0     8244 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/plugins.py
+-rw-r--r--   0        0        0     7835 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/project.py
+-rw-r--r--   0        0        0        0 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/py.typed
+-rw-r--r--   0        0        0    14965 2023-05-13 18:23:43.419460 slap_cli-1.8.1/src/slap/python/dependency.py
+-rw-r--r--   0        0        0     9711 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/python/environment.py
+-rw-r--r--   0        0        0     6833 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/python/pep508.py
+-rw-r--r--   0        0        0     2535 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/release.py
+-rw-r--r--   0        0        0     5092 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/repository.py
+-rw-r--r--   0        0        0     1091 2023-05-13 18:54:04.063864 slap_cli-1.8.1/src/slap/templates/github/.github/workflows/changelog.yaml
+-rw-r--r--   0        0        0      972 2023-05-13 18:53:05.709519 slap_cli-1.8.1/src/slap/templates/github/.github/workflows/python.yaml
+-rw-r--r--   0        0        0      246 2023-05-13 18:23:57.759054 slap_cli-1.8.1/src/slap/templates/poetry/.flake8
+-rw-r--r--   0        0        0       78 2023-05-13 17:02:56.460903 slap_cli-1.8.1/src/slap/templates/poetry/.gitignore
+-rw-r--r--   0        0        0        0 2023-05-13 17:02:56.460903 slap_cli-1.8.1/src/slap/templates/poetry/LICENSE
+-rw-r--r--   0        0        0        9 2023-05-13 17:02:56.460903 slap_cli-1.8.1/src/slap/templates/poetry/README.md
+-rw-r--r--   0        0        0     1451 2023-05-13 17:02:56.460903 slap_cli-1.8.1/src/slap/templates/poetry/pyproject.toml
+-rw-r--r--   0        0        0       22 2023-05-13 17:02:56.460903 slap_cli-1.8.1/src/slap/templates/poetry/src/{path}/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 17:02:56.460903 slap_cli-1.8.1/src/slap/templates/poetry/src/{path}/py.typed
+-rw-r--r--   0        0        0       67 2023-05-13 17:02:56.460903 slap_cli-1.8.1/src/slap/templates/poetry/tests/test_import.py
+-rw-r--r--   0        0        0     1847 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/util/cleo.py
+-rw-r--r--   0        0        0     4309 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/util/external/licenses.py
+-rw-r--r--   0        0        0     2172 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/util/external/pypi_classifiers.py
+-rw-r--r--   0        0        0      418 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/util/pygments.py
+-rw-r--r--   0        0        0     2113 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/util/toml_file.py
+-rw-r--r--   0        0        0     7363 2023-05-13 10:33:37.168056 slap_cli-1.8.1/src/slap/util/vcs.py
+-rw-r--r--   0        0        0     1501 1970-01-01 00:00:00.000000 slap_cli-1.8.1/PKG-INFO
```

### Comparing `slap_cli-1.8.0/LICENSE` & `slap_cli-1.8.1/LICENSE`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/pyproject.toml` & `slap_cli-1.8.1/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "slap-cli"
-version = "1.8.0"
+version = "1.8.1"
 description = "Slap is a command-line utility for developing Python applications."
 authors = ["Niklas Rosenstein <rosensteinniklas@gmail.com>"]
 license = "MIT"
-readme = "readme.md"
 packages = [{ include = "slap", from = "src" }]
 classifiers = [
   "Development Status :: 3 - Alpha",
   "Environment :: Console",
   "Programming Language :: Python :: 3.10",
 ]
 
@@ -56,15 +55,15 @@
 
 [tool.poetry.group.docs]
 optional = true
 
 [tool.poetry.group.docs.dependencies]
 mkdocs = "*"
 mkdocs-material = "*"
-novella = "0.2.3"
+novella = "0.2.5"
 pydoc-markdown = "4.6.0"
 
 [tool.poetry.scripts]
 slap = "slap.__main__:main"
 
 [tool.poetry.plugins."slap.plugins.application"]
 add = "slap.ext.application.add:AddCommandPlugin"
@@ -114,25 +113,26 @@
 [tool.poetry.plugins."slap.plugins.repository_host"]
 github = "slap.ext.repository_hosts.github:GithubRepositoryHost"
 
 [tool.slap]
 typed = true
 
 [tool.slap.test]
-mypy = "dmypy run src -- --namespace-packages --exclude src/slap/templates"
+mypy   = "dmypy run src -- --namespace-packages --exclude src/slap/templates"
 pytest = "pytest tests/ -vv"
-check = "slap check"
-isort = "isort src/ tests/ --check-only"
-black = "black src/ tests/ --check"
+check  = "slap check"
+isort  = "isort src/ tests/ --check-only"
+black  = "black src/ tests/ --check"
 flake8 = "flake8 src/ tests/"
 
 [tool.slap.run]
-"docs:build" = "cd docs && novella --base-url slap-cli/"
-"docs:dev" = "cd docs && novella --serve"
-fmt = "isort src/ tests/ && black src/ tests"
+"docs:install" = "slap venv -c docs --python python3.10 && slap install --use-venv docs --only-extras docs"
+"docs:build"   = "slap run --use-venv docs -- bash -c 'export PATH=\"$(slap venv -p)/bin:${PATH}\" && cd docs && novella --base-url slap/'"
+"docs:dev"     = "slap run --use-venv docs -- bash -c 'export PATH=\"$(slap venv -p)/bin:${PATH}\" && cd docs && novella --base-url slap/ --serve'"
+fmt            = "isort src/ tests/ && black src/ tests"
 
 [tool.mypy]
 pretty = true
 warn_redundant_casts = true
 #warn_unused_ignores = true
 warn_no_return = true
 warn_unreachable = true
```

### Comparing `slap_cli-1.8.0/src/slap/application.py` & `slap_cli-1.8.1/src/slap/application.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/changelog.py` & `slap_cli-1.8.1/src/slap/changelog.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/check.py` & `slap_cli-1.8.1/src/slap/check.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/configuration.py` & `slap_cli-1.8.1/src/slap/configuration.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/add.py` & `slap_cli-1.8.1/src/slap/ext/application/add.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/changelog.py` & `slap_cli-1.8.1/src/slap/ext/application/changelog.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/check.py` & `slap_cli-1.8.1/src/slap/ext/application/check.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/info.py` & `slap_cli-1.8.1/src/slap/ext/application/info.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/init.py` & `slap_cli-1.8.1/src/slap/ext/application/init.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 from typing import Iterable
 
 from slap.application import Application, Command, argument, option
 from slap.plugins import ApplicationPlugin
 from slap.util.external.licenses import get_spdx_license_details, wrap_license_text
 from slap.util.vcs import get_git_author
 
-TEMPLATES = ["poetry", "github-workflows"]
+TEMPLATES = ["poetry", "github"]
 
 
 def load_template(name: str) -> Iterable[tuple[str, str]]:
     """
     Loads a template, iterating over all its files.
     """
```

### Comparing `slap_cli-1.8.0/src/slap/ext/application/install.py` & `slap_cli-1.8.1/src/slap/ext/application/install.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/link.py` & `slap_cli-1.8.1/src/slap/ext/application/link.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/publish.py` & `slap_cli-1.8.1/src/slap/ext/application/publish.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/release.py` & `slap_cli-1.8.1/src/slap/ext/application/release.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/report.py` & `slap_cli-1.8.1/src/slap/ext/application/report.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/run.py` & `slap_cli-1.8.1/src/slap/ext/application/run.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/test.py` & `slap_cli-1.8.1/src/slap/ext/application/test.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/application/venv.py` & `slap_cli-1.8.1/src/slap/ext/application/venv.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/checks/changelog.py` & `slap_cli-1.8.1/src/slap/ext/checks/changelog.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/checks/general.py` & `slap_cli-1.8.1/src/slap/ext/checks/general.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/checks/poetry.py` & `slap_cli-1.8.1/src/slap/ext/checks/poetry.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/checks/release.py` & `slap_cli-1.8.1/src/slap/ext/checks/release.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/project_handlers/base.py` & `slap_cli-1.8.1/src/slap/ext/project_handlers/base.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/project_handlers/flit.py` & `slap_cli-1.8.1/src/slap/ext/project_handlers/flit.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/project_handlers/poetry.py` & `slap_cli-1.8.1/src/slap/ext/project_handlers/poetry.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/project_handlers/setuptools.py` & `slap_cli-1.8.1/src/slap/ext/project_handlers/setuptools.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/release/changelog.py` & `slap_cli-1.8.1/src/slap/ext/release/changelog.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/release/source_code_version.py` & `slap_cli-1.8.1/src/slap/ext/release/source_code_version.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/repository_ci/github_actions.py` & `slap_cli-1.8.1/src/slap/ext/repository_ci/github_actions.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/repository_handlers/default.py` & `slap_cli-1.8.1/src/slap/ext/repository_handlers/default.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/repository_hosts/github.py` & `slap_cli-1.8.1/src/slap/ext/repository_hosts/github.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/ext/version_incrementing_rule.py` & `slap_cli-1.8.1/src/slap/ext/version_incrementing_rule.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/install/installer.py` & `slap_cli-1.8.1/src/slap/install/installer.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/plugins.py` & `slap_cli-1.8.1/src/slap/plugins.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/project.py` & `slap_cli-1.8.1/src/slap/project.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/python/dependency.py` & `slap_cli-1.8.1/src/slap/python/dependency.py`

 * *Files 3% similar despite different names*

```diff
@@ -162,15 +162,20 @@
         """Parses a package name and its version spec from a string."""
 
         value, markers = value.partition(";")[::2]
 
         match = re.match(r"\s*[^<>=!~\^\(\)\*]+", value)
         if match:
             name = match.group(0)
-            version_spec = VersionSpec(value[match.end() :].strip() or "*")  # noqa: E203
+            constraint = value[match.end() :].strip() or "*"
+            if constraint.startswith("("):
+                if not constraint.endswith(")"):
+                    raise ValueError(f"invalid version constraint {constraint!r}")
+                constraint = constraint[1:-1].strip()
+            version_spec = VersionSpec(constraint)  # noqa: E203
         else:
             name = value
             version_spec = VersionSpec("")
 
         name, extras = split_package_name_with_extras(name)
         return PypiDependency(name=name, version=version_spec, extras=extras, markers=markers.strip() or None)
```

### Comparing `slap_cli-1.8.0/src/slap/python/environment.py` & `slap_cli-1.8.1/src/slap/python/environment.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/python/pep508.py` & `slap_cli-1.8.1/src/slap/python/pep508.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/release.py` & `slap_cli-1.8.1/src/slap/release.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/repository.py` & `slap_cli-1.8.1/src/slap/repository.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/templates/github-actions/.github/workflows/changelog.yaml` & `slap_cli-1.8.1/src/slap/templates/github/.github/workflows/changelog.yaml`

 * *Files 11% similar despite different names*

```diff
@@ -2,27 +2,27 @@
 #
 # - Insert the Pull Request URL into new changelog entries.
 # - Assert that a new changelog entry has been added in the PR unless a "no changelog" label is added to the PR.
 
 name: "Changelog"
 
 on:
-  pull_request_target: { branches: [ "develop" ] }
+  pull_request_target: {{ branches: [ "develop" ] }}
 
 jobs:
   changelog-update:
     name: "Insert Pull Request URL into new changelog entries"
     runs-on: ubuntu-latest
     if: github.event_name == 'pull_request_target'
     steps:
       - uses: actions/checkout@v2
       - uses: NiklasRosenstein/slap@gha/changelog/update/v2
-        with: { version: '*', pr-id: '${{ github.event.pull_request.number }}' }
+        with: {{ pr-id: '${{{{ github.event.pull_request.number }}}}' }}
 
   assert-new-changelog-entries:
     name: "At least one new changelog entry must be added"
     runs-on: ubuntu-latest
     if: github.base_ref != '' && !contains(github.event.pull_request.labels.*.name, 'no changelog')
     steps:
       - uses: actions/checkout@v2
       - uses: NiklasRosenstein/slap@gha/changelog/assert-added/v2
-        with: { version: '*', pr-id: '${{ github.event.pull_request.number }}' }
+        with: {{ pr-id: '${{{{ github.event.pull_request.number }}}}' }}
```

### Comparing `slap_cli-1.8.0/src/slap/templates/github-actions/.github/workflows/python.yaml` & `slap_cli-1.8.1/src/slap/templates/github/.github/workflows/python.yaml`

 * *Files 10% similar despite different names*

```diff
@@ -1,31 +1,31 @@
 name: "Python"
 
 on:
-  push: { branches: [ "develop" ], tags: [ "*" ] }
-  pull_request: { branches: [ "develop" ] }
+  push: {{ branches: [ "develop" ], tags: [ "*" ] }}
+  pull_request: {{ branches: [ "develop" ] }}
 
 jobs:
   test:
     runs-on: ubuntu-latest
     strategy:
       matrix:
         python-version: ["3.8", "3.9", "3.10", "3.11", "3.x"]
     steps:
     - uses: actions/checkout@v2
     - uses: NiklasRosenstein/slap@gha/install/v1
     - uses: actions/setup-python@v2
-      with: { python-version: "${{ matrix.python-version }}" }
+      with: {{ python-version: "${{{{ matrix.python-version }}}}" }}
     - run: slap install --link --no-venv-check
     - run: slap test
 
   documentation:
     runs-on: ubuntu-latest
     needs: test
     steps:
     - uses: actions/checkout@v2
     - uses: NiklasRosenstein/slap@gha/install/v1
     - run: slap install --no-venv-check --only-extras docs
     - run: slap run --no-venv-check docs:build
     - uses: JamesIves/github-pages-deploy-action@4.1.4
       if: github.ref == 'refs/heads/develop'
-      with: { branch: gh-pages, folder: docs/site, ssh-key: "${{ secrets.DEPLOY_KEY }}" }
+      with: {{ branch: gh-pages, folder: docs/_site, ssh-key: "${{{{ secrets.DEPLOY_KEY }}}}" }}
```

### Comparing `slap_cli-1.8.0/src/slap/templates/poetry/pyproject.toml` & `slap_cli-1.8.1/src/slap/templates/poetry/pyproject.toml`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/util/cleo.py` & `slap_cli-1.8.1/src/slap/util/cleo.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/util/external/licenses.py` & `slap_cli-1.8.1/src/slap/util/external/licenses.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/util/external/pypi_classifiers.py` & `slap_cli-1.8.1/src/slap/util/external/pypi_classifiers.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/util/toml_file.py` & `slap_cli-1.8.1/src/slap/util/toml_file.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.8.0/src/slap/util/vcs.py` & `slap_cli-1.8.1/src/slap/util/vcs.py`

 * *Files identical despite different names*

