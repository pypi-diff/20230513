# Comparing `tmp/slap_cli-1.7.6.tar.gz` & `tmp/slap_cli-1.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "slap_cli-1.7.6.tar", max compression
+gzip compressed data, was "slap_cli-1.8.0.tar", max compression
```

## Comparing `slap_cli-1.7.6.tar` & `slap_cli-1.8.0.tar`

### file list

```diff
@@ -1,52 +1,62 @@
--rw-r--r--   0        0        0     1002 2023-03-16 13:53:48.750935 slap_cli-1.7.6/LICENSE
--rw-r--r--   0        0        0     4631 2023-03-16 14:01:57.785358 slap_cli-1.7.6/pyproject.toml
--rw-r--r--   0        0        0     6005 2023-03-16 13:53:48.757221 slap_cli-1.7.6/readme.md
--rw-r--r--   0        0        0       98 2023-03-16 14:01:57.785545 slap_cli-1.7.6/src/slap/__init__.py
--rw-r--r--   0        0        0       82 2023-03-16 13:53:48.757788 slap_cli-1.7.6/src/slap/__main__.py
--rw-r--r--   0        0        0    10314 2023-03-16 13:53:48.758025 slap_cli-1.7.6/src/slap/application.py
--rw-r--r--   0        0        0     9163 2023-03-16 13:53:48.758241 slap_cli-1.7.6/src/slap/changelog.py
--rw-r--r--   0        0        0     3353 2023-03-16 13:53:48.758403 slap_cli-1.7.6/src/slap/check.py
--rw-r--r--   0        0        0     2520 2023-03-16 13:53:48.758561 slap_cli-1.7.6/src/slap/configuration.py
--rw-r--r--   0        0        0     5337 2023-03-16 13:53:48.759121 slap_cli-1.7.6/src/slap/ext/application/add.py
--rw-r--r--   0        0        0    27292 2023-03-16 13:53:48.759434 slap_cli-1.7.6/src/slap/ext/application/changelog.py
--rw-r--r--   0        0        0     6202 2023-03-16 13:53:48.759670 slap_cli-1.7.6/src/slap/ext/application/check.py
--rw-r--r--   0        0        0     3049 2023-03-16 13:53:48.759880 slap_cli-1.7.6/src/slap/ext/application/info.py
--rw-r--r--   0        0        0     8359 2023-03-16 13:53:48.760100 slap_cli-1.7.6/src/slap/ext/application/init.py
--rw-r--r--   0        0        0    14043 2023-03-16 13:53:48.760324 slap_cli-1.7.6/src/slap/ext/application/install.py
--rw-r--r--   0        0        0     5930 2023-03-16 13:53:48.760522 slap_cli-1.7.6/src/slap/ext/application/link.py
--rw-r--r--   0        0        0     4102 2023-03-16 13:53:48.760689 slap_cli-1.7.6/src/slap/ext/application/publish.py
--rw-r--r--   0        0        0    21301 2023-03-16 13:53:48.760929 slap_cli-1.7.6/src/slap/ext/application/release.py
--rw-r--r--   0        0        0     3344 2023-03-16 13:53:48.761128 slap_cli-1.7.6/src/slap/ext/application/report.py
--rw-r--r--   0        0        0     3521 2023-03-16 13:53:48.761286 slap_cli-1.7.6/src/slap/ext/application/run.py
--rw-r--r--   0        0        0     7789 2023-03-16 13:53:48.761460 slap_cli-1.7.6/src/slap/ext/application/test.py
--rw-r--r--   0        0        0    19021 2023-03-16 13:53:48.761711 slap_cli-1.7.6/src/slap/ext/application/venv.py
--rw-r--r--   0        0        0     2075 2023-03-16 13:53:48.762069 slap_cli-1.7.6/src/slap/ext/checks/changelog.py
--rw-r--r--   0        0        0     2215 2023-03-16 13:53:48.762277 slap_cli-1.7.6/src/slap/ext/checks/general.py
--rw-r--r--   0        0        0     6060 2023-03-16 13:53:48.762519 slap_cli-1.7.6/src/slap/ext/checks/poetry.py
--rw-r--r--   0        0        0     2812 2023-03-16 13:53:48.762725 slap_cli-1.7.6/src/slap/ext/checks/release.py
--rw-r--r--   0        0        0     8491 2023-03-16 13:53:48.763078 slap_cli-1.7.6/src/slap/ext/project_handlers/base.py
--rw-r--r--   0        0        0     3799 2023-03-16 13:53:48.763415 slap_cli-1.7.6/src/slap/ext/project_handlers/flit.py
--rw-r--r--   0        0        0     6462 2023-03-16 13:53:48.763934 slap_cli-1.7.6/src/slap/ext/project_handlers/poetry.py
--rw-r--r--   0        0        0     5751 2023-03-16 13:53:48.764174 slap_cli-1.7.6/src/slap/ext/project_handlers/setuptools.py
--rw-r--r--   0        0        0     1208 2023-03-16 13:53:48.764609 slap_cli-1.7.6/src/slap/ext/release/changelog.py
--rw-r--r--   0        0        0     2046 2023-03-16 13:53:48.764824 slap_cli-1.7.6/src/slap/ext/release/source_code_version.py
--rw-r--r--   0        0        0     2505 2023-03-16 13:53:48.765144 slap_cli-1.7.6/src/slap/ext/repository_ci/github_actions.py
--rw-r--r--   0        0        0     4065 2023-03-16 13:53:48.765548 slap_cli-1.7.6/src/slap/ext/repository_handlers/default.py
--rw-r--r--   0        0        0     4479 2023-03-16 13:53:48.765944 slap_cli-1.7.6/src/slap/ext/repository_hosts/github.py
--rw-r--r--   0        0        0     1357 2023-03-16 13:53:48.766160 slap_cli-1.7.6/src/slap/ext/version_incrementing_rule.py
--rw-r--r--   0        0        0    10869 2023-03-16 13:53:48.766537 slap_cli-1.7.6/src/slap/install/installer.py
--rw-r--r--   0        0        0     8244 2023-03-16 13:53:48.766731 slap_cli-1.7.6/src/slap/plugins.py
--rw-r--r--   0        0        0     7835 2023-03-16 13:53:48.766923 slap_cli-1.7.6/src/slap/project.py
--rw-r--r--   0        0        0        0 2023-03-16 13:53:48.767014 slap_cli-1.7.6/src/slap/py.typed
--rw-r--r--   0        0        0    14700 2023-03-16 13:59:28.383374 slap_cli-1.7.6/src/slap/python/dependency.py
--rw-r--r--   0        0        0     9711 2023-03-16 13:53:48.767555 slap_cli-1.7.6/src/slap/python/environment.py
--rw-r--r--   0        0        0     6833 2023-03-16 13:53:48.767767 slap_cli-1.7.6/src/slap/python/pep508.py
--rw-r--r--   0        0        0     2535 2023-03-16 13:53:48.768052 slap_cli-1.7.6/src/slap/release.py
--rw-r--r--   0        0        0     5092 2023-03-16 13:53:48.768251 slap_cli-1.7.6/src/slap/repository.py
--rw-r--r--   0        0        0     1847 2023-03-16 13:53:48.768554 slap_cli-1.7.6/src/slap/util/cleo.py
--rw-r--r--   0        0        0     4309 2023-03-16 13:53:48.768898 slap_cli-1.7.6/src/slap/util/external/licenses.py
--rw-r--r--   0        0        0     2172 2023-03-16 13:53:48.769131 slap_cli-1.7.6/src/slap/util/external/pypi_classifiers.py
--rw-r--r--   0        0        0      418 2023-03-16 13:53:48.769315 slap_cli-1.7.6/src/slap/util/pygments.py
--rw-r--r--   0        0        0     2113 2023-03-16 13:53:48.769497 slap_cli-1.7.6/src/slap/util/toml_file.py
--rw-r--r--   0        0        0     7363 2023-03-16 13:53:48.769721 slap_cli-1.7.6/src/slap/util/vcs.py
--rw-r--r--   0        0        0     7505 1970-01-01 00:00:00.000000 slap_cli-1.7.6/PKG-INFO
+-rw-r--r--   0        0        0     1002 2023-05-13 10:33:37.160056 slap_cli-1.8.0/LICENSE
+-rw-r--r--   0        0        0     4682 2023-05-13 17:03:04.948662 slap_cli-1.8.0/pyproject.toml
+-rw-r--r--   0        0        0     6005 2023-05-13 10:33:37.164056 slap_cli-1.8.0/readme.md
+-rw-r--r--   0        0        0       98 2023-05-13 17:03:04.960662 slap_cli-1.8.0/src/slap/__init__.py
+-rw-r--r--   0        0        0       82 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/__main__.py
+-rw-r--r--   0        0        0    10314 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/application.py
+-rw-r--r--   0        0        0     9163 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/changelog.py
+-rw-r--r--   0        0        0     3353 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/check.py
+-rw-r--r--   0        0        0     2520 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/configuration.py
+-rw-r--r--   0        0        0     5337 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/add.py
+-rw-r--r--   0        0        0    27292 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/changelog.py
+-rw-r--r--   0        0        0     6202 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/check.py
+-rw-r--r--   0        0        0     3049 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/info.py
+-rw-r--r--   0        0        0     4793 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/ext/application/init.py
+-rw-r--r--   0        0        0    14043 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/install.py
+-rw-r--r--   0        0        0     5930 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/link.py
+-rw-r--r--   0        0        0     4102 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/publish.py
+-rw-r--r--   0        0        0    21301 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/release.py
+-rw-r--r--   0        0        0     3344 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/report.py
+-rw-r--r--   0        0        0     3521 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/run.py
+-rw-r--r--   0        0        0     7789 2023-05-13 10:33:37.164056 slap_cli-1.8.0/src/slap/ext/application/test.py
+-rw-r--r--   0        0        0    19021 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/application/venv.py
+-rw-r--r--   0        0        0     2075 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/checks/changelog.py
+-rw-r--r--   0        0        0     2215 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/checks/general.py
+-rw-r--r--   0        0        0     6060 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/checks/poetry.py
+-rw-r--r--   0        0        0     2812 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/checks/release.py
+-rw-r--r--   0        0        0     8491 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/project_handlers/base.py
+-rw-r--r--   0        0        0     3799 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/project_handlers/flit.py
+-rw-r--r--   0        0        0     6462 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/project_handlers/poetry.py
+-rw-r--r--   0        0        0     5751 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/project_handlers/setuptools.py
+-rw-r--r--   0        0        0     1208 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/release/changelog.py
+-rw-r--r--   0        0        0     2046 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/release/source_code_version.py
+-rw-r--r--   0        0        0    16205 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/ext/repository_ci/github_actions.py
+-rw-r--r--   0        0        0     4065 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/repository_handlers/default.py
+-rw-r--r--   0        0        0     4479 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/repository_hosts/github.py
+-rw-r--r--   0        0        0     1357 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/ext/version_incrementing_rule.py
+-rw-r--r--   0        0        0    10869 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/install/installer.py
+-rw-r--r--   0        0        0     8244 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/plugins.py
+-rw-r--r--   0        0        0     7835 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/project.py
+-rw-r--r--   0        0        0        0 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/py.typed
+-rw-r--r--   0        0        0    14700 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/python/dependency.py
+-rw-r--r--   0        0        0     9711 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/python/environment.py
+-rw-r--r--   0        0        0     6833 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/python/pep508.py
+-rw-r--r--   0        0        0     2535 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/release.py
+-rw-r--r--   0        0        0     5092 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/repository.py
+-rw-r--r--   0        0        0     1105 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/github-actions/.github/workflows/changelog.yaml
+-rw-r--r--   0        0        0      955 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/github-actions/.github/workflows/python.yaml
+-rw-r--r--   0        0        0      208 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/.flake8
+-rw-r--r--   0        0        0       78 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/.gitignore
+-rw-r--r--   0        0        0        0 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/LICENSE
+-rw-r--r--   0        0        0        9 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/README.md
+-rw-r--r--   0        0        0     1451 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/pyproject.toml
+-rw-r--r--   0        0        0       22 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/src/{path}/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/src/{path}/py.typed
+-rw-r--r--   0        0        0       67 2023-05-13 17:02:56.460903 slap_cli-1.8.0/src/slap/templates/poetry/tests/test_import.py
+-rw-r--r--   0        0        0     1847 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/cleo.py
+-rw-r--r--   0        0        0     4309 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/external/licenses.py
+-rw-r--r--   0        0        0     2172 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/external/pypi_classifiers.py
+-rw-r--r--   0        0        0      418 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/pygments.py
+-rw-r--r--   0        0        0     2113 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/toml_file.py
+-rw-r--r--   0        0        0     7363 2023-05-13 10:33:37.168056 slap_cli-1.8.0/src/slap/util/vcs.py
+-rw-r--r--   0        0        0     7548 1970-01-01 00:00:00.000000 slap_cli-1.8.0/PKG-INFO
```

### Comparing `slap_cli-1.7.6/LICENSE` & `slap_cli-1.8.0/LICENSE`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/pyproject.toml` & `slap_cli-1.8.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "slap-cli"
-version = "1.7.6"
+version = "1.8.0"
 description = "Slap is a command-line utility for developing Python applications."
 authors = ["Niklas Rosenstein <rosensteinniklas@gmail.com>"]
 license = "MIT"
 readme = "readme.md"
 packages = [{ include = "slap", from = "src" }]
 classifiers = [
   "Development Status :: 3 - Alpha",
@@ -36,14 +36,15 @@
 setuptools = ">=39.1.0"  # Needed for pkg_resources
 tomli = "^2.0.0"
 tomlkit = "^0.10.1"
 twine = "^3.7.0"
 tqdm = "^4.64.0"
 build = "^0.8.0"
 "nr.python.environment" = "^0.1.4"
+gitpython = "^3.1.31"
 
 [tool.poetry.dev-dependencies]
 black = "^22.3.0"
 flake8 = "^4.0.1"
 isort = "^5.10.1"
 mypy = "^0.931"
 pytest = "^7.1.1"
@@ -113,15 +114,15 @@
 [tool.poetry.plugins."slap.plugins.repository_host"]
 github = "slap.ext.repository_hosts.github:GithubRepositoryHost"
 
 [tool.slap]
 typed = true
 
 [tool.slap.test]
-mypy = "dmypy run src -- --namespace-packages"
+mypy = "dmypy run src -- --namespace-packages --exclude src/slap/templates"
 pytest = "pytest tests/ -vv"
 check = "slap check"
 isort = "isort src/ tests/ --check-only"
 black = "black src/ tests/ --check"
 flake8 = "flake8 src/ tests/"
 
 [tool.slap.run]
```

### Comparing `slap_cli-1.7.6/readme.md` & `slap_cli-1.8.0/readme.md`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/application.py` & `slap_cli-1.8.0/src/slap/application.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/changelog.py` & `slap_cli-1.8.0/src/slap/changelog.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/check.py` & `slap_cli-1.8.0/src/slap/check.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/configuration.py` & `slap_cli-1.8.0/src/slap/configuration.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/add.py` & `slap_cli-1.8.0/src/slap/ext/application/add.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/changelog.py` & `slap_cli-1.8.0/src/slap/ext/application/changelog.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/check.py` & `slap_cli-1.8.0/src/slap/ext/application/check.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/info.py` & `slap_cli-1.8.0/src/slap/ext/application/info.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/install.py` & `slap_cli-1.8.0/src/slap/ext/application/install.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/link.py` & `slap_cli-1.8.0/src/slap/ext/application/link.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/publish.py` & `slap_cli-1.8.0/src/slap/ext/application/publish.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/release.py` & `slap_cli-1.8.0/src/slap/ext/application/release.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/report.py` & `slap_cli-1.8.0/src/slap/ext/application/report.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/run.py` & `slap_cli-1.8.0/src/slap/ext/application/run.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/test.py` & `slap_cli-1.8.0/src/slap/ext/application/test.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/application/venv.py` & `slap_cli-1.8.0/src/slap/ext/application/venv.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/checks/changelog.py` & `slap_cli-1.8.0/src/slap/ext/checks/changelog.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/checks/general.py` & `slap_cli-1.8.0/src/slap/ext/checks/general.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/checks/poetry.py` & `slap_cli-1.8.0/src/slap/ext/checks/poetry.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/checks/release.py` & `slap_cli-1.8.0/src/slap/ext/checks/release.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/project_handlers/base.py` & `slap_cli-1.8.0/src/slap/ext/project_handlers/base.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/project_handlers/flit.py` & `slap_cli-1.8.0/src/slap/ext/project_handlers/flit.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/project_handlers/poetry.py` & `slap_cli-1.8.0/src/slap/ext/project_handlers/poetry.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/project_handlers/setuptools.py` & `slap_cli-1.8.0/src/slap/ext/project_handlers/setuptools.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/release/changelog.py` & `slap_cli-1.8.0/src/slap/ext/release/changelog.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/release/source_code_version.py` & `slap_cli-1.8.0/src/slap/ext/release/source_code_version.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/repository_handlers/default.py` & `slap_cli-1.8.0/src/slap/ext/repository_handlers/default.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/repository_hosts/github.py` & `slap_cli-1.8.0/src/slap/ext/repository_hosts/github.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/ext/version_incrementing_rule.py` & `slap_cli-1.8.0/src/slap/ext/version_incrementing_rule.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/install/installer.py` & `slap_cli-1.8.0/src/slap/install/installer.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/plugins.py` & `slap_cli-1.8.0/src/slap/plugins.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/project.py` & `slap_cli-1.8.0/src/slap/project.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/python/dependency.py` & `slap_cli-1.8.0/src/slap/python/dependency.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/python/environment.py` & `slap_cli-1.8.0/src/slap/python/environment.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/python/pep508.py` & `slap_cli-1.8.0/src/slap/python/pep508.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/release.py` & `slap_cli-1.8.0/src/slap/release.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/repository.py` & `slap_cli-1.8.0/src/slap/repository.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/util/cleo.py` & `slap_cli-1.8.0/src/slap/util/cleo.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/util/external/licenses.py` & `slap_cli-1.8.0/src/slap/util/external/licenses.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/util/external/pypi_classifiers.py` & `slap_cli-1.8.0/src/slap/util/external/pypi_classifiers.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/util/toml_file.py` & `slap_cli-1.8.0/src/slap/util/toml_file.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/src/slap/util/vcs.py` & `slap_cli-1.8.0/src/slap/util/vcs.py`

 * *Files identical despite different names*

### Comparing `slap_cli-1.7.6/PKG-INFO` & `slap_cli-1.8.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: slap-cli
-Version: 1.7.6
+Version: 1.8.0
 Summary: Slap is a command-line utility for developing Python applications.
 License: MIT
 Author: Niklas Rosenstein
 Author-email: rosensteinniklas@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Environment :: Console
@@ -15,14 +15,15 @@
 Classifier: Programming Language :: Python :: 3.10
 Requires-Dist: PyYAML (>=4.0)
 Requires-Dist: beautifulsoup4 (>=4.10.0,<5.0.0)
 Requires-Dist: build (>=0.8.0,<0.9.0)
 Requires-Dist: cleo (>=1.0.0a4)
 Requires-Dist: databind (>=2.0.0,<3.0.0)
 Requires-Dist: flit (>=3.6.0,<4.0.0)
+Requires-Dist: gitpython (>=3.1.31,<4.0.0)
 Requires-Dist: nr.python.environment (>=0.1.4,<0.2.0)
 Requires-Dist: nr.util (>=0.8.12,<1.0.0)
 Requires-Dist: poetry-core (>=1.1.0a6,<2.0.0)
 Requires-Dist: ptyprocess (>=0.7.0,<0.8.0)
 Requires-Dist: pygments (>=2.11.2,<3.0.0)
 Requires-Dist: requests (>=2.27.1,<3.0.0)
 Requires-Dist: setuptools (>=39.1.0)
```

