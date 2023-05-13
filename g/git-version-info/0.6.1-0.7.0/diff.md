# Comparing `tmp/git_version_info-0.6.1.tar.gz` & `tmp/git_version_info-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "git_version_info-0.6.1.tar", last modified: Sun Apr 23 19:03:58 2023, max compression
+gzip compressed data, was "git_version_info-0.7.0.tar", last modified: Sat May 13 14:21:56 2023, max compression
```

## Comparing `git_version_info-0.6.1.tar` & `git_version_info-0.7.0.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-23 19:03:58.466489 git_version_info-0.6.1/
--rw-rw-rw-   0 root         (0) root         (0)     1072 2023-04-23 19:03:46.000000 git_version_info-0.6.1/LICENSE
--rw-rw-rw-   0 root         (0) root         (0)      107 2023-04-23 19:03:46.000000 git_version_info-0.6.1/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)      963 2023-04-23 19:03:58.466489 git_version_info-0.6.1/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)      390 2023-04-23 19:03:46.000000 git_version_info-0.6.1/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-23 19:03:58.464489 git_version_info-0.6.1/git_version_info.egg-info/
--rw-r--r--   0 root         (0) root         (0)      963 2023-04-23 19:03:58.000000 git_version_info-0.6.1/git_version_info.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      387 2023-04-23 19:03:58.000000 git_version_info-0.6.1/git_version_info.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-04-23 19:03:58.000000 git_version_info-0.6.1/git_version_info.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       57 2023-04-23 19:03:58.000000 git_version_info-0.6.1/git_version_info.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       13 2023-04-23 19:03:58.000000 git_version_info-0.6.1/git_version_info.egg-info/top_level.txt
--rw-rw-rw-   0 root         (0) root         (0)       42 2023-04-23 19:03:46.000000 git_version_info-0.6.1/requirements.in
--rw-rw-rw-   0 root         (0) root         (0)       50 2023-04-23 19:03:46.000000 git_version_info-0.6.1/requirementsDev.in
--rw-rw-rw-   0 root         (0) root         (0)      712 2023-04-23 19:03:58.467489 git_version_info-0.6.1/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)      545 2023-04-23 19:03:46.000000 git_version_info-0.6.1/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-23 19:03:58.465489 git_version_info-0.6.1/test/
--rw-rw-rw-   0 root         (0) root         (0)      242 2023-04-23 19:03:46.000000 git_version_info-0.6.1/test/test_basics.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-04-23 19:03:58.468489 git_version_info-0.6.1/version_info/
--rw-rw-rw-   0 root         (0) root         (0)      207 2023-04-23 19:03:46.000000 git_version_info-0.6.1/version_info/__init__.py
--rw-r--r--   0 root         (0) root         (0)      498 2023-04-23 19:03:58.468489 git_version_info-0.6.1/version_info/_version.py
--rw-rw-rw-   0 root         (0) root         (0)     3106 2023-04-23 19:03:46.000000 git_version_info-0.6.1/version_info/main.py
--rw-rw-rw-   0 root         (0) root         (0)    68749 2023-04-23 19:03:46.000000 git_version_info-0.6.1/versioneer.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:21:56.708723 git_version_info-0.7.0/
+-rw-rw-rw-   0 root         (0) root         (0)     1072 2023-05-13 14:21:45.000000 git_version_info-0.7.0/LICENSE
+-rw-rw-rw-   0 root         (0) root         (0)      107 2023-05-13 14:21:45.000000 git_version_info-0.7.0/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)      963 2023-05-13 14:21:56.708723 git_version_info-0.7.0/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)      390 2023-05-13 14:21:45.000000 git_version_info-0.7.0/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:21:56.707723 git_version_info-0.7.0/git_version_info.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      963 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      387 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       57 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       13 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/top_level.txt
+-rw-rw-rw-   0 root         (0) root         (0)       42 2023-05-13 14:21:45.000000 git_version_info-0.7.0/requirements.in
+-rw-rw-rw-   0 root         (0) root         (0)       50 2023-05-13 14:21:45.000000 git_version_info-0.7.0/requirementsDev.in
+-rw-rw-rw-   0 root         (0) root         (0)      712 2023-05-13 14:21:56.709723 git_version_info-0.7.0/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)      545 2023-05-13 14:21:45.000000 git_version_info-0.7.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:21:56.707723 git_version_info-0.7.0/test/
+-rw-rw-rw-   0 root         (0) root         (0)      442 2023-05-13 14:21:45.000000 git_version_info-0.7.0/test/test_basics.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:21:56.709723 git_version_info-0.7.0/version_info/
+-rw-rw-rw-   0 root         (0) root         (0)      207 2023-05-13 14:21:45.000000 git_version_info-0.7.0/version_info/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      498 2023-05-13 14:21:56.709723 git_version_info-0.7.0/version_info/_version.py
+-rw-rw-rw-   0 root         (0) root         (0)     3323 2023-05-13 14:21:45.000000 git_version_info-0.7.0/version_info/main.py
+-rw-rw-rw-   0 root         (0) root         (0)    68749 2023-05-13 14:21:45.000000 git_version_info-0.7.0/versioneer.py
```

### Comparing `git_version_info-0.6.1/LICENSE` & `git_version_info-0.7.0/LICENSE`

 * *Files identical despite different names*

### Comparing `git_version_info-0.6.1/PKG-INFO` & `git_version_info-0.7.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: git_version_info
-Version: 0.6.1
+Version: 0.7.0
 Summary: Basic version tagging for python scripts and plots
 Home-page: https://gitlab.com/charlesbaynham/version_info
 Author: Charles Baynham
 License: UNKNOWN
 Project-URL: Bug Tracker, https://gitlab.com/charlesbaynham/version_info/-/issues
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `git_version_info-0.6.1/git_version_info.egg-info/PKG-INFO` & `git_version_info-0.7.0/git_version_info.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: git-version-info
-Version: 0.6.1
+Version: 0.7.0
 Summary: Basic version tagging for python scripts and plots
 Home-page: https://gitlab.com/charlesbaynham/version_info
 Author: Charles Baynham
 License: UNKNOWN
 Project-URL: Bug Tracker, https://gitlab.com/charlesbaynham/version_info/-/issues
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `git_version_info-0.6.1/setup.cfg` & `git_version_info-0.7.0/setup.cfg`

 * *Files identical despite different names*

### Comparing `git_version_info-0.6.1/setup.py` & `git_version_info-0.7.0/setup.py`

 * *Files identical despite different names*

### Comparing `git_version_info-0.6.1/version_info/main.py` & `git_version_info-0.7.0/version_info/main.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 """ version_info.py
 
 This module defines a function, `version_info`, which returns a string
 describing the current git version of the highest project in the calling tree.
 """
 import importlib
+import os
 import subprocess
 
 try:
     import matplotlib.pyplot as plt
     from matplotlib.axes import Axes
 
     matplotlib_present = True
@@ -20,21 +21,26 @@
 fmt = "{tag}_{commitcount}+{gitsha}{dirty}"
 
 
 def get_version() -> str:
     """
     Returns a string describing the git version of the given project.
 
+    Calls git to request current version unless the environmental variable `GIT_DESCRIBE` is set.
+
     :param ax: Axes object for the chart whose name will be updated. Unused if alter_plot is false, set to
     `matplotlib.pyplot.gca()` by default
     :return: A string describing the project's version
     """
 
     try:
-        version = subprocess.check_output(command, universal_newlines=True).strip()
+        if "GIT_DESCRIBE" in os.environ:
+            version = os.environ["GIT_DESCRIBE"]
+        else:
+            version = subprocess.check_output(command, universal_newlines=True).strip()
 
         # Thanks to pyfidelity/setuptools-git-version
         try:
             parts = version.split("-")
             assert len(parts) in (3, 4)
             dirty = len(parts) == 4
             tag, count, sha = parts[:3]
```

### Comparing `git_version_info-0.6.1/versioneer.py` & `git_version_info-0.7.0/versioneer.py`

 * *Files identical despite different names*

