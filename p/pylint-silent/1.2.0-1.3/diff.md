# Comparing `tmp/pylint-silent-1.2.0.tar.gz` & `tmp/pylint-silent-1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pylint-silent-1.2.0.tar", last modified: Fri Dec 23 21:13:33 2022, max compression
+gzip compressed data, was "pylint-silent-1.3.tar", last modified: Fri May 12 22:43:32 2023, max compression
```

## Comparing `pylint-silent-1.2.0.tar` & `pylint-silent-1.3.tar`

### file list

```diff
@@ -1,14 +1,16 @@
-drwxrwxr-x   0 udi       (1000) udi       (1000)        0 2022-12-23 21:13:33.883117 pylint-silent-1.2.0/
--rw-rw-r--   0 udi       (1000) udi       (1000)     5064 2022-12-23 21:13:33.879117 pylint-silent-1.2.0/PKG-INFO
--rw-rw-r--   0 udi       (1000) udi       (1000)     4043 2022-12-23 21:13:09.000000 pylint-silent-1.2.0/README.md
-drwxrwxr-x   0 udi       (1000) udi       (1000)        0 2022-12-23 21:13:33.879117 pylint-silent-1.2.0/pylint_silent/
--rw-rw-r--   0 udi       (1000) udi       (1000)     6865 2022-12-23 21:13:09.000000 pylint-silent-1.2.0/pylint_silent/__init__.py
--rw-rw-r--   0 udi       (1000) udi       (1000)      807 2022-11-30 23:00:20.000000 pylint-silent-1.2.0/pylint_silent/__main__.py
-drwxrwxr-x   0 udi       (1000) udi       (1000)        0 2022-12-23 21:13:33.879117 pylint-silent-1.2.0/pylint_silent.egg-info/
--rw-rw-r--   0 udi       (1000) udi       (1000)     5064 2022-12-23 21:13:33.000000 pylint-silent-1.2.0/pylint_silent.egg-info/PKG-INFO
--rw-rw-r--   0 udi       (1000) udi       (1000)      264 2022-12-23 21:13:33.000000 pylint-silent-1.2.0/pylint_silent.egg-info/SOURCES.txt
--rw-rw-r--   0 udi       (1000) udi       (1000)        1 2022-12-23 21:13:33.000000 pylint-silent-1.2.0/pylint_silent.egg-info/dependency_links.txt
--rw-rw-r--   0 udi       (1000) udi       (1000)       62 2022-12-23 21:13:33.000000 pylint-silent-1.2.0/pylint_silent.egg-info/entry_points.txt
--rw-rw-r--   0 udi       (1000) udi       (1000)       14 2022-12-23 21:13:33.000000 pylint-silent-1.2.0/pylint_silent.egg-info/top_level.txt
--rw-rw-r--   0 udi       (1000) udi       (1000)     1292 2022-12-01 01:24:20.000000 pylint-silent-1.2.0/pyproject.toml
--rw-rw-r--   0 udi       (1000) udi       (1000)       38 2022-12-23 21:13:33.883117 pylint-silent-1.2.0/setup.cfg
+drwxrwxr-x   0 udi       (1000) udi       (1000)        0 2023-05-12 22:43:32.604986 pylint-silent-1.3/
+-rw-rw-r--   0 udi       (1000) udi       (1000)     6849 2023-05-12 22:43:32.604986 pylint-silent-1.3/PKG-INFO
+-rw-rw-r--   0 udi       (1000) udi       (1000)     5829 2023-05-12 22:26:16.000000 pylint-silent-1.3/README.md
+drwxrwxr-x   0 udi       (1000) udi       (1000)        0 2023-05-12 22:43:32.604986 pylint-silent-1.3/pylint_silent/
+-rw-rw-r--   0 udi       (1000) udi       (1000)    10530 2023-05-12 22:26:49.000000 pylint-silent-1.3/pylint_silent/__init__.py
+-rw-rw-r--   0 udi       (1000) udi       (1000)     1798 2023-05-12 22:36:46.000000 pylint-silent-1.3/pylint_silent/__main__.py
+drwxrwxr-x   0 udi       (1000) udi       (1000)        0 2023-05-12 22:43:32.604986 pylint-silent-1.3/pylint_silent.egg-info/
+-rw-rw-r--   0 udi       (1000) udi       (1000)     6849 2023-05-12 22:43:32.000000 pylint-silent-1.3/pylint_silent.egg-info/PKG-INFO
+-rw-rw-r--   0 udi       (1000) udi       (1000)      286 2023-05-12 22:43:32.000000 pylint-silent-1.3/pylint_silent.egg-info/SOURCES.txt
+-rw-rw-r--   0 udi       (1000) udi       (1000)        1 2023-05-12 22:43:32.000000 pylint-silent-1.3/pylint_silent.egg-info/dependency_links.txt
+-rw-rw-r--   0 udi       (1000) udi       (1000)       62 2023-05-12 22:43:32.000000 pylint-silent-1.3/pylint_silent.egg-info/entry_points.txt
+-rw-rw-r--   0 udi       (1000) udi       (1000)       14 2023-05-12 22:43:32.000000 pylint-silent-1.3/pylint_silent.egg-info/top_level.txt
+-rw-rw-r--   0 udi       (1000) udi       (1000)     1292 2022-12-01 01:24:20.000000 pylint-silent-1.3/pyproject.toml
+-rw-rw-r--   0 udi       (1000) udi       (1000)       38 2023-05-12 22:43:32.604986 pylint-silent-1.3/setup.cfg
+drwxrwxr-x   0 udi       (1000) udi       (1000)        0 2023-05-12 22:43:32.604986 pylint-silent-1.3/tests/
+-rw-rw-r--   0 udi       (1000) udi       (1000)     8556 2023-05-12 21:13:29.000000 pylint-silent-1.3/tests/test_samples.py
```

### Comparing `pylint-silent-1.2.0/PKG-INFO` & `pylint-silent-1.3/README.md`

 * *Files 18% similar despite different names*

```diff
@@ -1,31 +1,7 @@
-Metadata-Version: 2.1
-Name: pylint-silent
-Version: 1.2.0
-Summary: Automatically add code comments to silence the output of pylint
-Author-email: Udi Fuchs <udifuchs@gmail.com>
-License: GPL-2.0-or-later
-Project-URL: Homepage, http://github.com/udifuchs/pylint-silent
-Keywords: pylint
-Classifier: Topic :: Software Development :: Quality Assurance
-Classifier: Development Status :: 5 - Production/Stable
-Classifier: Environment :: Console
-Classifier: License :: OSI Approved :: GNU General Public License v2 or later (GPLv2+)
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Classifier: Operating System :: OS Independent
-Classifier: Intended Audience :: Developers
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-
 # pylint-silent
 **Automatically add code comments to silence the output of [pylint](https://github.com/PyCQA/pylint).**
 
 `pylint` can be very useful in finding software bugs in python code. A good article demonstrating this is [Why Pylint is both useful and unusable, and how you can actually use it](https://pythonspeed.com/articles/pylint/). In short, when running `pylint` on existing code, it tends to output tons of messages.
 
 `pylint-silent` is suppose to make `pylint` usable. The idea is to automatically add code comments of the form `# pylint: disable` to silent every `pylint` message. This will allow you to deploy `pylint` in a Continuous Integration (CI) setup. If a code commit introduces **new** `pylint` messages, these will be visible immediately.
 
@@ -52,19 +28,36 @@
 ```
 
 `pylint-silent` would add this comment:
 ```
 def func(name):  # pylint: disable=unused-argument
 ```
 
-For subsequent runs, you probably want to clear the old comments first:
+If adding the comment would make the line too long, `pylint-silent` would instead add:
+```
+# pylint-next: disable=unused-argument
+def very-long-function-name-with-some-arguments(first_argument, second_argument):
+```
+`--max-line-length` specfies the maximum line length.
+This feature is disabled by default for compatibility with previous versions.
+It is disabled by having a default maximum line length of 999.
+In the future the default should change to 88.
+
+Another option is to run `pylint-silent --signature` to add a signature to each generated comment:
+```
+def func(name):  # pylint: disable=unused-argument; silent
 ```
-pylint-silent reset my_package/*.py  # List all python files here
+This way you can easily identify which comments were generated by `pylint-silent`.
+
+For subsequent runs, you probably want to clear the old comments first.
+Assuming you are using signatures:
+```
+pylint-silent reset --signature my_package/*.py  # List all python files here
 pylint my_package > pylint.log
-pylint-silent apply pylint.log
+pylint-silent apply --signature pylint.log
 ```
 
 There are two reasons to clear old comments:
 
 1. Remove stale comments to code that was already fixed.
 2. `pylint-silent` does not know how to handle lines that already have a `# pylint` comment in them.
 
@@ -112,7 +105,45 @@
 Whichever option you choose, I recommend reading their documentation about how `pylint` should be used.
 
 ### Summary
 `pylint`'s motto is: **It's not just a linter that annoys you!**
 
 `pylint-silent` helps `pylint` live up to its motto.
 
+### Changelog
+
+#### 1.3 (2023-05-12)
+
+* Mark every pylint-silent comment with a signature. Fixes #4. PR #5.
+* Add a --max-line-length option. Fixes #3.
+* Fix tests for pylint 2.16. Require pylint >= 2.16 for the tests.
+
+#### 1.2 (2022-12-23)
+
+* Preserve comments meant for other non-pylint tools. PR #2.
+
+#### 1.1.2 (2022-11-30)
+
+* Use pyproject.toml instead of setup.py.
+* Update compatible python versions to currently supported python 3.7 through 3.11.
+* Fix bug in `pylint-silent stats` that got confused with `=` symbols in code.
+* Document in README.md how to reset or get statistics on all files in folder.
+
+#### 1.1.1 (2021-04-13)
+
+* Preserve file permissions in generated code. Fixes #1.
+
+#### 1.1 (2021-03-04)
+
+* Ignore disable/enable blocks.
+* Add reference to pylint-ignore in the README.
+* Add testing based on pytest and tox.
+* Handle missing-module-docstring correctly.
+
+#### 1.0.1 (2020-07-22)
+
+* Fix link from pypi.org to github.
+* Fix markdown in README.md.
+
+#### 1.0 (2020-07-20)
+
+* Initial release.
```

### Comparing `pylint-silent-1.2.0/pylint_silent.egg-info/PKG-INFO` & `pylint-silent-1.3/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pylint-silent
-Version: 1.2.0
+Version: 1.3
 Summary: Automatically add code comments to silence the output of pylint
 Author-email: Udi Fuchs <udifuchs@gmail.com>
 License: GPL-2.0-or-later
 Project-URL: Homepage, http://github.com/udifuchs/pylint-silent
 Keywords: pylint
 Classifier: Topic :: Software Development :: Quality Assurance
 Classifier: Development Status :: 5 - Production/Stable
@@ -52,19 +52,36 @@
 ```
 
 `pylint-silent` would add this comment:
 ```
 def func(name):  # pylint: disable=unused-argument
 ```
 
-For subsequent runs, you probably want to clear the old comments first:
+If adding the comment would make the line too long, `pylint-silent` would instead add:
 ```
-pylint-silent reset my_package/*.py  # List all python files here
+# pylint-next: disable=unused-argument
+def very-long-function-name-with-some-arguments(first_argument, second_argument):
+```
+`--max-line-length` specfies the maximum line length.
+This feature is disabled by default for compatibility with previous versions.
+It is disabled by having a default maximum line length of 999.
+In the future the default should change to 88.
+
+Another option is to run `pylint-silent --signature` to add a signature to each generated comment:
+```
+def func(name):  # pylint: disable=unused-argument; silent
+```
+This way you can easily identify which comments were generated by `pylint-silent`.
+
+For subsequent runs, you probably want to clear the old comments first.
+Assuming you are using signatures:
+```
+pylint-silent reset --signature my_package/*.py  # List all python files here
 pylint my_package > pylint.log
-pylint-silent apply pylint.log
+pylint-silent apply --signature pylint.log
 ```
 
 There are two reasons to clear old comments:
 
 1. Remove stale comments to code that was already fixed.
 2. `pylint-silent` does not know how to handle lines that already have a `# pylint` comment in them.
 
@@ -112,7 +129,45 @@
 Whichever option you choose, I recommend reading their documentation about how `pylint` should be used.
 
 ### Summary
 `pylint`'s motto is: **It's not just a linter that annoys you!**
 
 `pylint-silent` helps `pylint` live up to its motto.
 
+### Changelog
+
+#### 1.3 (2023-05-12)
+
+* Mark every pylint-silent comment with a signature. Fixes #4. PR #5.
+* Add a --max-line-length option. Fixes #3.
+* Fix tests for pylint 2.16. Require pylint >= 2.16 for the tests.
+
+#### 1.2 (2022-12-23)
+
+* Preserve comments meant for other non-pylint tools. PR #2.
+
+#### 1.1.2 (2022-11-30)
+
+* Use pyproject.toml instead of setup.py.
+* Update compatible python versions to currently supported python 3.7 through 3.11.
+* Fix bug in `pylint-silent stats` that got confused with `=` symbols in code.
+* Document in README.md how to reset or get statistics on all files in folder.
+
+#### 1.1.1 (2021-04-13)
+
+* Preserve file permissions in generated code. Fixes #1.
+
+#### 1.1 (2021-03-04)
+
+* Ignore disable/enable blocks.
+* Add reference to pylint-ignore in the README.
+* Add testing based on pytest and tox.
+* Handle missing-module-docstring correctly.
+
+#### 1.0.1 (2020-07-22)
+
+* Fix link from pypi.org to github.
+* Fix markdown in README.md.
+
+#### 1.0 (2020-07-20)
+
+* Initial release.
```

### Comparing `pylint-silent-1.2.0/pyproject.toml` & `pylint-silent-1.3/pyproject.toml`

 * *Files identical despite different names*

