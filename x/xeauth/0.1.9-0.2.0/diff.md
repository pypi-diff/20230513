# Comparing `tmp/xeauth-0.1.9.tar.gz` & `tmp/xeauth-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "xeauth-0.1.9.tar", last modified: Fri Sep  3 05:03:53 2021, max compression
+gzip compressed data, was "xeauth-0.2.0.tar", max compression
```

## Comparing `xeauth-0.1.9.tar` & `xeauth-0.2.0.tar`

### file list

```diff
@@ -1,17 +1,14 @@
--rw-r--r--   0        0        0     1073 2020-12-17 17:27:26.780407 xeauth-0.1.9/LICENSE
--rw-r--r--   0        0        0      877 2020-12-17 17:27:26.757073 xeauth-0.1.9/README.rst
--rw-r--r--   0        0        0     1490 2021-09-03 05:03:15.560351 xeauth-0.1.9/pyproject.toml
--rw-r--r--   0        0        0       36 2020-12-17 17:27:26.787073 xeauth-0.1.9/tests/__init__.py
--rw-r--r--   0        0        0     1002 2020-12-17 17:27:26.797073 xeauth-0.1.9/tests/test_xeauth.py
--rw-r--r--   0        0        0      157 2021-09-03 05:03:15.563685 xeauth-0.1.9/xeauth/__init__.py
--rw-r--r--   0        0        0     1958 2021-02-17 18:34:52.524942 xeauth-0.1.9/xeauth/certificates.py
--rw-r--r--   0        0        0      454 2021-02-06 16:13:18.417046 xeauth-0.1.9/xeauth/cli.py
--rw-r--r--   0        0        0       35 2021-02-24 19:20:56.535121 xeauth-0.1.9/xeauth/integrations/__init__.py
--rw-r--r--   0        0        0     1226 2021-08-31 10:53:48.073644 xeauth-0.1.9/xeauth/integrations/eve_panel.py
--rw-r--r--   0        0        0     2952 2021-08-31 16:56:33.558239 xeauth-0.1.9/xeauth/integrations/panel_server.py
--rw-r--r--   0        0        0    14364 2021-08-31 10:54:41.337655 xeauth-0.1.9/xeauth/oauth.py
--rw-r--r--   0        0        0     2189 2021-08-31 20:13:05.269524 xeauth-0.1.9/xeauth/settings.py
--rw-r--r--   0        0        0      203 2021-02-26 23:50:05.585234 xeauth-0.1.9/xeauth/utils.py
--rw-r--r--   0        0        0     1745 2021-03-04 13:52:48.197508 xeauth-0.1.9/xeauth/xeauth.py
--rw-r--r--   0        0        0     1941 2021-09-03 05:03:53.558083 xeauth-0.1.9/setup.py
--rw-r--r--   0        0        0     1717 2021-09-03 05:03:53.558615 xeauth-0.1.9/PKG-INFO
+-rw-r--r--   0        0        0     1073 2020-12-17 17:27:26.780407 xeauth-0.2.0/LICENSE
+-rw-r--r--   0        0        0      877 2020-12-17 17:27:26.757073 xeauth-0.2.0/README.rst
+-rw-r--r--   0        0        0     1432 2023-05-13 20:35:24.214007 xeauth-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0       36 2020-12-17 17:27:26.787073 xeauth-0.2.0/tests/__init__.py
+-rw-r--r--   0        0        0     1002 2023-01-19 13:38:16.595387 xeauth-0.2.0/tests/test_xeauth.py
+-rw-r--r--   0        0        0      262 2023-05-13 20:35:24.214007 xeauth-0.2.0/xeauth/__init__.py
+-rw-r--r--   0        0        0     2266 2023-01-19 15:33:09.669806 xeauth-0.2.0/xeauth/admin.py
+-rw-r--r--   0        0        0     3925 2023-01-19 15:32:52.905554 xeauth-0.2.0/xeauth/cli.py
+-rw-r--r--   0        0        0     6097 2023-05-13 20:33:32.315405 xeauth-0.2.0/xeauth/github.py
+-rw-r--r--   0        0        0     2123 2023-05-13 20:33:32.315405 xeauth-0.2.0/xeauth/settings.py
+-rw-r--r--   0        0        0     2463 2023-05-13 20:33:32.315405 xeauth-0.2.0/xeauth/user.py
+-rw-r--r--   0        0        0     1162 2023-01-19 13:38:16.922057 xeauth-0.2.0/xeauth/utils.py
+-rw-r--r--   0        0        0     1939 1970-01-01 00:00:00.000000 xeauth-0.2.0/setup.py
+-rw-r--r--   0        0        0     1900 1970-01-01 00:00:00.000000 xeauth-0.2.0/PKG-INFO
```

### Comparing `xeauth-0.1.9/LICENSE` & `xeauth-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `xeauth-0.1.9/README.rst` & `xeauth-0.2.0/README.rst`

 * *Files identical despite different names*

### Comparing `xeauth-0.1.9/pyproject.toml` & `xeauth-0.2.0/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,38 +1,38 @@
 [tool]
 [tool.poetry]
 name = "xeauth"
-version = "0.1.9"
+version = "0.2.0"
 homepage = "https://github.com/jmosbacher/xeauth"
 description = "Top-level package for xeauth."
 authors = ["Yossi Mosbacher <joe.mosbacher@gmail.com>"]
 readme = "README.rst"
 license =  "MIT"
 classifiers=[
     'Development Status :: 2 - Pre-Alpha',
     'Intended Audience :: Developers',
     'License :: OSI Approved :: MIT License',
     'Natural Language :: English',
 
-    'Programming Language :: Python :: 3.6',
-    'Programming Language :: Python :: 3.7',
+
     'Programming Language :: Python :: 3.8',
 ]
 packages = [
     { include = "xeauth" },
     { include = "tests", format = "sdist" },
 ]
     
 [tool.poetry.dependencies]
-python = ">=3.7.1"
+python = ">=3.7,<4"
 click = "*"
-Authlib = "^0.15.3"
-panel = "^0.12.1"
-httpx = "^0.16.1"
+httpx = ">=0.19,<0.23"
 appdirs = "^1.4.4"
+param = "^1.12.0"
+gnupg = "^2.3.1"
+rich = "^13.1.0"
 
 [tool.poetry.dev-dependencies]
 bumpversion = "*"
 coverage = "*"
 flake8 = "*"
 invoke = "*"
 isort = "*"
@@ -50,14 +50,14 @@
 [tool.poetry.plugins."panel.auth"]
 "xeauth" = "xeauth.integrations.panel_server:XenonPanelAuth"
 
 [tool.poetry.scripts]
 xeauth = 'xeauth.cli:main'
 
 [build-system]
-requires = ["poetry>=0.12", "setuptools"]
-build-backend = "poetry.masonry.api"
+requires = ["poetry-core>=1.0.8", "setuptools"]
+build-backend = "poetry.core.masonry.api"
 
 [tool.dephell.main]
 versioning = "semver"
 from = {format = "poetry", path = "pyproject.toml"}
 to = {format = "setuppy", path = "setup.py"}
```

### Comparing `xeauth-0.1.9/tests/test_xeauth.py` & `xeauth-0.2.0/tests/test_xeauth.py`

 * *Files 23% similar despite different names*

```diff
@@ -26,11 +26,11 @@
 
 
 def test_command_line_interface():
     """Test the CLI."""
     runner = CliRunner()
     result = runner.invoke(cli.main)
     assert result.exit_code == 0
-    assert 'xeauth.cli.main' in result.output
-    help_result = runner.invoke(cli.main, ['--help'])
+    assert "xeauth.cli.main" in result.output
+    help_result = runner.invoke(cli.main, ["--help"])
     assert help_result.exit_code == 0
-    assert '--help  Show this message and exit.' in help_result.output
+    assert "--help  Show this message and exit." in help_result.output
```

### Comparing `xeauth-0.1.9/setup.py` & `xeauth-0.2.0/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,40 +1,41 @@
 # -*- coding: utf-8 -*-
 from setuptools import setup
 
 packages = \
-['tests', 'xeauth', 'xeauth.integrations']
+['tests', 'xeauth']
 
 package_data = \
 {'': ['*']}
 
 install_requires = \
-['Authlib>=0.15.3,<0.16.0',
- 'appdirs>=1.4.4,<2.0.0',
+['appdirs>=1.4.4,<2.0.0',
  'click',
- 'httpx>=0.16.1,<0.17.0',
- 'panel>=0.12.1,<0.13.0']
+ 'gnupg>=2.3.1,<3.0.0',
+ 'httpx>=0.19,<0.23',
+ 'param>=1.12.0,<2.0.0',
+ 'rich>=13.1.0,<14.0.0']
 
 entry_points = \
 {'console_scripts': ['xeauth = xeauth.cli:main'],
  'eve_panel.auth': ['XenonAuth = xeauth.integrations.eve_panel:XenonEveAuth'],
  'panel.auth': ['xeauth = xeauth.integrations.panel_server:XenonPanelAuth']}
 
 setup_kwargs = {
     'name': 'xeauth',
-    'version': '0.1.9',
+    'version': '0.2.0',
     'description': 'Top-level package for xeauth.',
     'long_description': '======\nxeauth\n======\n\n\n.. image:: https://img.shields.io/pypi/v/xeauth.svg\n        :target: https://pypi.python.org/pypi/xeauth\n\n.. image:: https://img.shields.io/travis/jmosbacher/xeauth.svg\n        :target: https://travis-ci.com/jmosbacher/xeauth\n\n.. image:: https://readthedocs.org/projects/xeauth/badge/?version=latest\n        :target: https://xeauth.readthedocs.io/en/latest/?badge=latest\n        :alt: Documentation Status\n\n\n\n\nAuthentication client for the Xenon edark matter experiment.\n\n\n* Free software: MIT\n* Documentation: https://xeauth.readthedocs.io.\n\n\nFeatures\n--------\n\n* TODO\n\nCredits\n-------\n\nThis package was created with Cookiecutter_ and the `briggySmalls/cookiecutter-pypackage`_ project template.\n\n.. _Cookiecutter: https://github.com/audreyr/cookiecutter\n.. _`briggySmalls/cookiecutter-pypackage`: https://github.com/briggySmalls/cookiecutter-pypackage\n',
     'author': 'Yossi Mosbacher',
     'author_email': 'joe.mosbacher@gmail.com',
-    'maintainer': None,
-    'maintainer_email': None,
+    'maintainer': 'None',
+    'maintainer_email': 'None',
     'url': 'https://github.com/jmosbacher/xeauth',
     'packages': packages,
     'package_data': package_data,
     'install_requires': install_requires,
     'entry_points': entry_points,
-    'python_requires': '>=3.7.1',
+    'python_requires': '>=3.7,<4',
 }
 
 
 setup(**setup_kwargs)
```

### Comparing `xeauth-0.1.9/PKG-INFO` & `xeauth-0.2.0/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,29 +1,33 @@
 Metadata-Version: 2.1
 Name: xeauth
-Version: 0.1.9
+Version: 0.2.0
 Summary: Top-level package for xeauth.
 Home-page: https://github.com/jmosbacher/xeauth
 License: MIT
 Author: Yossi Mosbacher
 Author-email: joe.mosbacher@gmail.com
-Requires-Python: >=3.7.1
+Requires-Python: >=3.7,<4
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
-Requires-Dist: Authlib (>=0.15.3,<0.16.0)
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Classifier: Programming Language :: Python :: 3.8
 Requires-Dist: appdirs (>=1.4.4,<2.0.0)
 Requires-Dist: click
-Requires-Dist: httpx (>=0.16.1,<0.17.0)
-Requires-Dist: panel (>=0.12.1,<0.13.0)
+Requires-Dist: gnupg (>=2.3.1,<3.0.0)
+Requires-Dist: httpx (>=0.19,<0.23)
+Requires-Dist: param (>=1.12.0,<2.0.0)
+Requires-Dist: rich (>=13.1.0,<14.0.0)
 Description-Content-Type: text/x-rst
 
 ======
 xeauth
 ======
```

