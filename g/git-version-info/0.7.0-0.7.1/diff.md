# Comparing `tmp/git_version_info-0.7.0.tar.gz` & `tmp/git_version_info-0.7.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "git_version_info-0.7.0.tar", last modified: Sat May 13 14:21:56 2023, max compression
+gzip compressed data, was "git_version_info-0.7.1.tar", last modified: Sat May 13 14:34:04 2023, max compression
```

## Comparing `git_version_info-0.7.0.tar` & `git_version_info-0.7.1.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:21:56.708723 git_version_info-0.7.0/
--rw-rw-rw-   0 root         (0) root         (0)     1072 2023-05-13 14:21:45.000000 git_version_info-0.7.0/LICENSE
--rw-rw-rw-   0 root         (0) root         (0)      107 2023-05-13 14:21:45.000000 git_version_info-0.7.0/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)      963 2023-05-13 14:21:56.708723 git_version_info-0.7.0/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)      390 2023-05-13 14:21:45.000000 git_version_info-0.7.0/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:21:56.707723 git_version_info-0.7.0/git_version_info.egg-info/
--rw-r--r--   0 root         (0) root         (0)      963 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      387 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       57 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       13 2023-05-13 14:21:56.000000 git_version_info-0.7.0/git_version_info.egg-info/top_level.txt
--rw-rw-rw-   0 root         (0) root         (0)       42 2023-05-13 14:21:45.000000 git_version_info-0.7.0/requirements.in
--rw-rw-rw-   0 root         (0) root         (0)       50 2023-05-13 14:21:45.000000 git_version_info-0.7.0/requirementsDev.in
--rw-rw-rw-   0 root         (0) root         (0)      712 2023-05-13 14:21:56.709723 git_version_info-0.7.0/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)      545 2023-05-13 14:21:45.000000 git_version_info-0.7.0/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:21:56.707723 git_version_info-0.7.0/test/
--rw-rw-rw-   0 root         (0) root         (0)      442 2023-05-13 14:21:45.000000 git_version_info-0.7.0/test/test_basics.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:21:56.709723 git_version_info-0.7.0/version_info/
--rw-rw-rw-   0 root         (0) root         (0)      207 2023-05-13 14:21:45.000000 git_version_info-0.7.0/version_info/__init__.py
--rw-r--r--   0 root         (0) root         (0)      498 2023-05-13 14:21:56.709723 git_version_info-0.7.0/version_info/_version.py
--rw-rw-rw-   0 root         (0) root         (0)     3323 2023-05-13 14:21:45.000000 git_version_info-0.7.0/version_info/main.py
--rw-rw-rw-   0 root         (0) root         (0)    68749 2023-05-13 14:21:45.000000 git_version_info-0.7.0/versioneer.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:34:04.399485 git_version_info-0.7.1/
+-rw-rw-rw-   0 root         (0) root         (0)     1072 2023-05-13 14:33:53.000000 git_version_info-0.7.1/LICENSE
+-rw-rw-rw-   0 root         (0) root         (0)      107 2023-05-13 14:33:53.000000 git_version_info-0.7.1/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)      963 2023-05-13 14:34:04.399485 git_version_info-0.7.1/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)      390 2023-05-13 14:33:53.000000 git_version_info-0.7.1/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:34:04.397485 git_version_info-0.7.1/git_version_info.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      963 2023-05-13 14:34:04.000000 git_version_info-0.7.1/git_version_info.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      387 2023-05-13 14:34:04.000000 git_version_info-0.7.1/git_version_info.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 14:34:04.000000 git_version_info-0.7.1/git_version_info.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       57 2023-05-13 14:34:04.000000 git_version_info-0.7.1/git_version_info.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       13 2023-05-13 14:34:04.000000 git_version_info-0.7.1/git_version_info.egg-info/top_level.txt
+-rw-rw-rw-   0 root         (0) root         (0)       42 2023-05-13 14:33:53.000000 git_version_info-0.7.1/requirements.in
+-rw-rw-rw-   0 root         (0) root         (0)       50 2023-05-13 14:33:53.000000 git_version_info-0.7.1/requirementsDev.in
+-rw-rw-rw-   0 root         (0) root         (0)      712 2023-05-13 14:34:04.399485 git_version_info-0.7.1/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)      545 2023-05-13 14:33:53.000000 git_version_info-0.7.1/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:34:04.397485 git_version_info-0.7.1/test/
+-rw-rw-rw-   0 root         (0) root         (0)      442 2023-05-13 14:33:53.000000 git_version_info-0.7.1/test/test_basics.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 14:34:04.400485 git_version_info-0.7.1/version_info/
+-rw-rw-rw-   0 root         (0) root         (0)      207 2023-05-13 14:33:53.000000 git_version_info-0.7.1/version_info/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      498 2023-05-13 14:34:04.400485 git_version_info-0.7.1/version_info/_version.py
+-rw-rw-rw-   0 root         (0) root         (0)     3356 2023-05-13 14:33:53.000000 git_version_info-0.7.1/version_info/main.py
+-rw-rw-rw-   0 root         (0) root         (0)    68749 2023-05-13 14:33:53.000000 git_version_info-0.7.1/versioneer.py
```

### Comparing `git_version_info-0.7.0/LICENSE` & `git_version_info-0.7.1/LICENSE`

 * *Files identical despite different names*

### Comparing `git_version_info-0.7.0/PKG-INFO` & `git_version_info-0.7.1/git_version_info.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: git_version_info
-Version: 0.7.0
+Name: git-version-info
+Version: 0.7.1
 Summary: Basic version tagging for python scripts and plots
 Home-page: https://gitlab.com/charlesbaynham/version_info
 Author: Charles Baynham
 License: UNKNOWN
 Project-URL: Bug Tracker, https://gitlab.com/charlesbaynham/version_info/-/issues
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `git_version_info-0.7.0/git_version_info.egg-info/PKG-INFO` & `git_version_info-0.7.1/PKG-INFO`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: git-version-info
-Version: 0.7.0
+Name: git_version_info
+Version: 0.7.1
 Summary: Basic version tagging for python scripts and plots
 Home-page: https://gitlab.com/charlesbaynham/version_info
 Author: Charles Baynham
 License: UNKNOWN
 Project-URL: Bug Tracker, https://gitlab.com/charlesbaynham/version_info/-/issues
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `git_version_info-0.7.0/setup.cfg` & `git_version_info-0.7.1/setup.cfg`

 * *Files identical despite different names*

### Comparing `git_version_info-0.7.0/setup.py` & `git_version_info-0.7.1/setup.py`

 * *Files identical despite different names*

### Comparing `git_version_info-0.7.0/version_info/main.py` & `git_version_info-0.7.1/version_info/main.py`

 * *Files 2% similar despite different names*

```diff
@@ -60,15 +60,15 @@
                 dirty_str = ""
 
             return fmt.format(
                 tag=tag, commitcount=count, gitsha=sha.lstrip("g"), dirty=dirty_str
             )
         except AssertionError:
             return version
-    except FileNotFoundError:
+    except (FileNotFoundError, subprocess.CalledProcessError):
         # Git is not installed
         return "unknown-version"
 
 
 def tag_plot(ax=None, small=False, tag_text=None) -> str:
     """
     Tags the passed Axes object with the project's current version.
```

### Comparing `git_version_info-0.7.0/versioneer.py` & `git_version_info-0.7.1/versioneer.py`

 * *Files identical despite different names*

