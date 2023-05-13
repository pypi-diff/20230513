# Comparing `tmp/sampleproject-dhchenx-0.0.1a0.tar.gz` & `tmp/sampleproject-dhchenx-0.0.1a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sampleproject-dhchenx-0.0.1a0.tar", last modified: Sat May 13 17:05:18 2023, max compression
+gzip compressed data, was "sampleproject-dhchenx-0.0.1a1.tar", last modified: Sat May 13 17:19:11 2023, max compression
```

## Comparing `sampleproject-dhchenx-0.0.1a0.tar` & `sampleproject-dhchenx-0.0.1a1.tar`

### file list

```diff
@@ -1,20 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 17:05:18.441205 sampleproject-dhchenx-0.0.1a0/
--rw-rw-rw-   0        0        0     1081 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a0/LICENSE.txt
--rw-rw-rw-   0        0        0     4285 2023-05-13 17:05:18.438206 sampleproject-dhchenx-0.0.1a0/PKG-INFO
--rw-rw-rw-   0        0        0     1804 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a0/README.md
--rw-rw-rw-   0        0        0     6210 2023-05-13 17:03:49.000000 sampleproject-dhchenx-0.0.1a0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-13 17:05:18.441205 sampleproject-dhchenx-0.0.1a0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-05-13 17:05:18.392192 sampleproject-dhchenx-0.0.1a0/src/
-drwxrwxrwx   0        0        0        0 2023-05-13 17:05:18.401713 sampleproject-dhchenx-0.0.1a0/src/sample/
--rw-rw-rw-   0        0        0      111 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a0/src/sample/__init__.py
--rw-rw-rw-   0        0        0        9 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a0/src/sample/package_data.dat
--rw-rw-rw-   0        0        0       43 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a0/src/sample/simple.py
-drwxrwxrwx   0        0        0        0 2023-05-13 17:05:18.432684 sampleproject-dhchenx-0.0.1a0/src/sampleproject_dhchenx.egg-info/
--rw-rw-rw-   0        0        0     4285 2023-05-13 17:05:18.000000 sampleproject-dhchenx-0.0.1a0/src/sampleproject_dhchenx.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      425 2023-05-13 17:05:18.000000 sampleproject-dhchenx-0.0.1a0/src/sampleproject_dhchenx.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 17:05:18.000000 sampleproject-dhchenx-0.0.1a0/src/sampleproject_dhchenx.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       39 2023-05-13 17:05:18.000000 sampleproject-dhchenx-0.0.1a0/src/sampleproject_dhchenx.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       50 2023-05-13 17:05:18.000000 sampleproject-dhchenx-0.0.1a0/src/sampleproject_dhchenx.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-05-13 17:05:18.000000 sampleproject-dhchenx-0.0.1a0/src/sampleproject_dhchenx.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-05-13 17:05:18.434682 sampleproject-dhchenx-0.0.1a0/tests/
--rw-rw-rw-   0        0        0      417 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a0/tests/test_simple.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:19:11.731908 sampleproject-dhchenx-0.0.1a1/
+-rw-rw-rw-   0        0        0     1088 2023-05-13 17:18:32.000000 sampleproject-dhchenx-0.0.1a1/LICENSE.txt
+-rw-rw-rw-   0        0        0     2671 2023-05-13 17:19:11.731398 sampleproject-dhchenx-0.0.1a1/PKG-INFO
+-rw-rw-rw-   0        0        0      241 2023-05-13 17:18:32.000000 sampleproject-dhchenx-0.0.1a1/README.md
+-rw-rw-rw-   0        0        0     6210 2023-05-13 17:18:32.000000 sampleproject-dhchenx-0.0.1a1/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 17:19:11.731908 sampleproject-dhchenx-0.0.1a1/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 17:19:11.697255 sampleproject-dhchenx-0.0.1a1/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 17:19:11.712829 sampleproject-dhchenx-0.0.1a1/src/sample/
+-rw-rw-rw-   0        0        0      111 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a1/src/sample/__init__.py
+-rw-rw-rw-   0        0        0        9 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a1/src/sample/package_data.dat
+-rw-rw-rw-   0        0        0       43 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a1/src/sample/simple.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:19:11.728400 sampleproject-dhchenx-0.0.1a1/src/sampleproject_dhchenx.egg-info/
+-rw-rw-rw-   0        0        0     2671 2023-05-13 17:19:11.000000 sampleproject-dhchenx-0.0.1a1/src/sampleproject_dhchenx.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      373 2023-05-13 17:19:11.000000 sampleproject-dhchenx-0.0.1a1/src/sampleproject_dhchenx.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 17:19:11.000000 sampleproject-dhchenx-0.0.1a1/src/sampleproject_dhchenx.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-13 17:19:11.000000 sampleproject-dhchenx-0.0.1a1/src/sampleproject_dhchenx.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 17:19:11.000000 sampleproject-dhchenx-0.0.1a1/src/sampleproject_dhchenx.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 17:19:11.729395 sampleproject-dhchenx-0.0.1a1/tests/
+-rw-rw-rw-   0        0        0      417 2023-04-26 19:25:03.000000 sampleproject-dhchenx-0.0.1a1/tests/test_simple.py
```

### Comparing `sampleproject-dhchenx-0.0.1a0/LICENSE.txt` & `sampleproject-dhchenx-0.0.1a1/LICENSE.txt`

 * *Files 19% similar despite different names*

```diff
@@ -1,19 +1,22 @@
-Copyright (c) 2016 The Python Packaging Authority (PyPA)
+MIT License
 
-Permission is hereby granted, free of charge, to any person obtaining a copy of
-this software and associated documentation files (the "Software"), to deal in
-the Software without restriction, including without limitation the rights to
-use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
-of the Software, and to permit persons to whom the Software is furnished to do
-so, subject to the following conditions:
+Copyright (c) 2023 The Python Packaging Authority
+
+Permission is hereby granted, free of charge, to any person obtaining a copy
+of this software and associated documentation files (the "Software"), to deal
+in the Software without restriction, including without limitation the rights
+to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+copies of the Software, and to permit persons to whom the Software is
+furnished to do so, subject to the following conditions:
 
 The above copyright notice and this permission notice shall be included in all
 copies or substantial portions of the Software.
 
 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
 IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
 FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 SOFTWARE.
+
```

### Comparing `sampleproject-dhchenx-0.0.1a0/pyproject.toml` & `sampleproject-dhchenx-0.0.1a1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 name = "sampleproject-dhchenx"  # Required
 
 # Versions should comply with PEP 440:
 # https://www.python.org/dev/peps/pep-0440/
 #
 # For a discussion on single-sourcing the version, see
 # https://packaging.python.org/guides/single-sourcing-package-version/
-version = "0.0.1a0"  # Required
+version = "0.0.1a1"  # Required
 
 # This is a one-line description or tagline of what your project does. This
 # corresponds to the "Summary" metadata field:
 # https://packaging.python.org/specifications/core-metadata/#summary
 description = "A sample Python project developed by Donghua Chen"  # Optional
 
 # This is an optional longer description of your project that represents
@@ -59,27 +59,27 @@
 authors = [
   {name = "Donghua Chen", email = "douglaschan@126.com" } # Optional
 ]
 
 # This should be your name or the names of the organization who currently
 # maintains the project, and a valid email address corresponding to the name
 # listed.
-maintainers = [
-  {name = "Donghua Chen", email = "douglaschan@126.com" } # Optional
-]
+# maintainers = [
+#  {name = "Donghua Chen", email = "douglaschan@126.com" } # Optional
+#]
 
 # Classifiers help users find your project by categorizing it.
 #
 # For a list of valid classifiers, see https://pypi.org/classifiers/
 classifiers = [  # Optional
   # How mature is this project? Common values are
   #   3 - Alpha
   #   4 - Beta
   #   5 - Production/Stable
-  "Development Status :: 3 - Alpha",
+  "Development Status :: 4 - Beta",
 
   # Indicate who your project is intended for
   "Intended Audience :: Developers",
   "Topic :: Software Development :: Build Tools",
 
   # Pick your license as you wish
   "License :: OSI Approved :: MIT License",
@@ -99,15 +99,15 @@
 # This field lists other packages that your project depends on to run.
 # Any package you put here will be installed by pip when your project is
 # installed, so they must be valid existing projects.
 #
 # For an analysis of this field vs pip's requirements files see:
 # https://packaging.python.org/discussions/install-requires-vs-requirements/
 dependencies = [ # Optional
-  "peppercorn"
+  "numpy"
 ]
 
 # List additional groups of dependencies here (e.g. development
 # dependencies). Users will be able to install these using the "extras"
 # syntax, for example:
 #
 #   $ pip install sampleproject[dev]
@@ -134,15 +134,15 @@
 # "Funding" = "https://donate.pypi.org"
 # "Say Thanks!" = "http://saythanks.io/to/example"
 "Source" = "https://github.com/dhchenx/sampleproject/"
 
 # The following would provide a command line executable called `sample`
 # which executes the function `main` from this package when invoked.
 [project.scripts]  # Optional
-sample = "sample:main"
+# sample = "sample:main"
 
 # This is configuration specific to the `setuptools` build backend.
 # If you are using a different build backend, you will need to change this.
 [tool.setuptools]
 # If there are data files included in your packages that need to be
 # installed, specify them here.
 package-data = {"sample" = ["*.dat"]}
```

