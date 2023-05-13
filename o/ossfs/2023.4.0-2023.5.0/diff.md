# Comparing `tmp/ossfs-2023.4.0.tar.gz` & `tmp/ossfs-2023.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ossfs-2023.4.0.tar", last modified: Sun Apr 23 06:18:12 2023, max compression
+gzip compressed data, was "ossfs-2023.5.0.tar", last modified: Sat May 13 03:30:14 2023, max compression
```

## Comparing `ossfs-2023.4.0.tar` & `ossfs-2023.5.0.tar`

### file list

```diff
@@ -1,56 +1,57 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.401256 ossfs-2023.4.0/
--rw-r--r--   0 runner    (1001) docker     (123)      750 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.cruft.json
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.gitattributes
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.393256 ossfs-2023.4.0/.github/
--rw-r--r--   0 runner    (1001) docker     (123)      737 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.github/dependabot.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.393256 ossfs-2023.4.0/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      632 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.github/workflows/docs.yml
--rw-r--r--   0 runner    (1001) docker     (123)      725 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.github/workflows/release.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1683 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.github/workflows/tests.yml
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.github/workflows/update-template.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2035 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1477 2023-04-23 06:17:45.000000 ossfs-2023.4.0/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     5399 2023-04-23 06:17:45.000000 ossfs-2023.4.0/CODE_OF_CONDUCT.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2715 2023-04-23 06:17:45.000000 ossfs-2023.4.0/CONTRIBUTING.rst
--rw-r--r--   0 runner    (1001) docker     (123)    11345 2023-04-23 06:17:45.000000 ossfs-2023.4.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       46 2023-04-23 06:17:45.000000 ossfs-2023.4.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     5671 2023-04-23 06:18:12.401256 ossfs-2023.4.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4989 2023-04-23 06:17:45.000000 ossfs-2023.4.0/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.393256 ossfs-2023.4.0/docs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.393256 ossfs-2023.4.0/docs/assets/
--rw-r--r--   0 runner    (1001) docker     (123)     1905 2023-04-23 06:17:45.000000 ossfs-2023.4.0/docs/assets/logo.svg
--rw-r--r--   0 runner    (1001) docker     (123)      759 2023-04-23 06:17:45.000000 ossfs-2023.4.0/docs/gen_ref_pages.py
--rw-r--r--   0 runner    (1001) docker     (123)       66 2023-04-23 06:17:45.000000 ossfs-2023.4.0/docs/index.md
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-04-23 06:17:45.000000 ossfs-2023.4.0/mkdocs.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1973 2023-04-23 06:17:45.000000 ossfs-2023.4.0/noxfile.py
--rw-r--r--   0 runner    (1001) docker     (123)     1635 2023-04-23 06:17:45.000000 ossfs-2023.4.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)     1360 2023-04-23 06:18:12.401256 ossfs-2023.4.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.389256 ossfs-2023.4.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.393256 ossfs-2023.4.0/src/ossfs/
--rw-r--r--   0 runner    (1001) docker     (123)      303 2023-04-23 06:17:45.000000 ossfs-2023.4.0/src/ossfs/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    23852 2023-04-23 06:17:45.000000 ossfs-2023.4.0/src/ossfs/async_oss.py
--rw-r--r--   0 runner    (1001) docker     (123)     9608 2023-04-23 06:17:45.000000 ossfs-2023.4.0/src/ossfs/base.py
--rw-r--r--   0 runner    (1001) docker     (123)    19735 2023-04-23 06:17:45.000000 ossfs-2023.4.0/src/ossfs/core.py
--rw-r--r--   0 runner    (1001) docker     (123)     1908 2023-04-23 06:17:45.000000 ossfs-2023.4.0/src/ossfs/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     1738 2023-04-23 06:17:45.000000 ossfs-2023.4.0/src/ossfs/file.py
--rw-r--r--   0 runner    (1001) docker     (123)     3573 2023-04-23 06:17:45.000000 ossfs-2023.4.0/src/ossfs/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.397256 ossfs-2023.4.0/src/ossfs.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5671 2023-04-23 06:18:12.000000 ossfs-2023.4.0/src/ossfs.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      955 2023-04-23 06:18:12.000000 ossfs-2023.4.0/src/ossfs.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-23 06:18:12.000000 ossfs-2023.4.0/src/ossfs.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-23 06:18:12.000000 ossfs-2023.4.0/src/ossfs.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      631 2023-04-23 06:18:12.000000 ossfs-2023.4.0/src/ossfs.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-04-23 06:18:12.000000 ossfs-2023.4.0/src/ossfs.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.401256 ossfs-2023.4.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.401256 ossfs-2023.4.0/tests/bench/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/bench/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2234 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/bench/test_put_get.py
--rw-r--r--   0 runner    (1001) docker     (123)     3412 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-23 06:18:12.401256 ossfs-2023.4.0/tests/func/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/func/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3398 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/func/test_bucket.py
--rw-r--r--   0 runner    (1001) docker     (123)    13170 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/func/test_file.py
--rw-r--r--   0 runner    (1001) docker     (123)     3129 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/func/test_login.py
--rw-r--r--   0 runner    (1001) docker     (123)    23431 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/func/test_object.py
--rw-r--r--   0 runner    (1001) docker     (123)     3799 2023-04-23 06:17:45.000000 ossfs-2023.4.0/tests/func/test_ossfs.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/
+-rw-r--r--   0 runner    (1001) docker     (123)      750 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.cruft.json
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.gitattributes
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.262926 ossfs-2023.5.0/.github/
+-rw-r--r--   0 runner    (1001) docker     (123)      737 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.github/dependabot.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      632 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.github/workflows/docs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      725 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.github/workflows/release.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1683 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.github/workflows/tests.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      298 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.github/workflows/update-template.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2035 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1477 2023-05-13 03:29:52.000000 ossfs-2023.5.0/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     5399 2023-05-13 03:29:52.000000 ossfs-2023.5.0/CODE_OF_CONDUCT.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2715 2023-05-13 03:29:52.000000 ossfs-2023.5.0/CONTRIBUTING.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    11345 2023-05-13 03:29:52.000000 ossfs-2023.5.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       46 2023-05-13 03:29:52.000000 ossfs-2023.5.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     5672 2023-05-13 03:30:14.266926 ossfs-2023.5.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4990 2023-05-13 03:29:52.000000 ossfs-2023.5.0/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/docs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/docs/assets/
+-rw-r--r--   0 runner    (1001) docker     (123)     1905 2023-05-13 03:29:52.000000 ossfs-2023.5.0/docs/assets/logo.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      759 2023-05-13 03:29:52.000000 ossfs-2023.5.0/docs/gen_ref_pages.py
+-rw-r--r--   0 runner    (1001) docker     (123)       66 2023-05-13 03:29:52.000000 ossfs-2023.5.0/docs/index.md
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 03:29:52.000000 ossfs-2023.5.0/mkdocs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1973 2023-05-13 03:29:52.000000 ossfs-2023.5.0/noxfile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1635 2023-05-13 03:29:52.000000 ossfs-2023.5.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)     1360 2023-05-13 03:30:14.270926 ossfs-2023.5.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.262926 ossfs-2023.5.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/src/ossfs/
+-rw-r--r--   0 runner    (1001) docker     (123)      303 2023-05-13 03:29:52.000000 ossfs-2023.5.0/src/ossfs/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23854 2023-05-13 03:29:52.000000 ossfs-2023.5.0/src/ossfs/async_oss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9608 2023-05-13 03:29:52.000000 ossfs-2023.5.0/src/ossfs/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19742 2023-05-13 03:29:52.000000 ossfs-2023.5.0/src/ossfs/core.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1908 2023-05-13 03:29:52.000000 ossfs-2023.5.0/src/ossfs/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1738 2023-05-13 03:29:52.000000 ossfs-2023.5.0/src/ossfs/file.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3573 2023-05-13 03:29:52.000000 ossfs-2023.5.0/src/ossfs/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/src/ossfs.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5672 2023-05-13 03:30:14.000000 ossfs-2023.5.0/src/ossfs.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      980 2023-05-13 03:30:14.000000 ossfs-2023.5.0/src/ossfs.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 03:30:14.000000 ossfs-2023.5.0/src/ossfs.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 03:30:14.000000 ossfs-2023.5.0/src/ossfs.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      631 2023-05-13 03:30:14.000000 ossfs-2023.5.0/src/ossfs.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-13 03:30:14.000000 ossfs-2023.5.0/src/ossfs.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/tests/bench/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/bench/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1758 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/bench/test_put_get.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3951 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:30:14.266926 ossfs-2023.5.0/tests/func/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/func/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3360 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/func/test_bucket.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1258 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/func/test_error.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12885 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/func/test_file.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3129 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/func/test_login.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20771 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/func/test_object.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3507 2023-05-13 03:29:52.000000 ossfs-2023.5.0/tests/func/test_ossfs.py
```

### Comparing `ossfs-2023.4.0/.cruft.json` & `ossfs-2023.5.0/.cruft.json`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/.github/dependabot.yml` & `ossfs-2023.5.0/.github/dependabot.yml`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/.github/workflows/docs.yml` & `ossfs-2023.5.0/.github/workflows/docs.yml`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/.github/workflows/release.yml` & `ossfs-2023.5.0/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/.github/workflows/tests.yml` & `ossfs-2023.5.0/.github/workflows/tests.yml`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/.gitignore` & `ossfs-2023.5.0/.gitignore`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/.pre-commit-config.yaml` & `ossfs-2023.5.0/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/CODE_OF_CONDUCT.rst` & `ossfs-2023.5.0/CODE_OF_CONDUCT.rst`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/CONTRIBUTING.rst` & `ossfs-2023.5.0/CONTRIBUTING.rst`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/LICENSE` & `ossfs-2023.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/PKG-INFO` & `ossfs-2023.5.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ossfs
-Version: 2023.4.0
+Version: 2023.5.0
 Summary: fsspec filesystem for OSS
 Home-page: https://github.com/fsspec/ossfs
 Download-URL: https://github.com/fsspec/ossfs
 Maintainer-email: gao@iterive.ai
 License: Apache-2.0
 Platform: any
 Classifier: Programming Language :: Python :: 3
@@ -70,15 +70,15 @@
 .. code:: console
 
    $ conda install -c conda-forge ossfs
 
 Quick Start
 ------------
 
-Here is a simple example of locating and reading a object in OSS.
+Here is a simple example of locating and reading an object in OSS.
 
 .. code:: python
 
    import ossfs
    fs = ossfs.OSSFileSystem(endpoint='http://oss-cn-hangzhou.aliyuncs.com')
    fs.ls('/dvc-test-anonymous/LICENSE')
    [{'name': '/dvc-test-anonymous/LICENSE',
```

### Comparing `ossfs-2023.4.0/README.rst` & `ossfs-2023.5.0/README.rst`

 * *Files 0% similar despite different names*

```diff
@@ -48,15 +48,15 @@
 .. code:: console
 
    $ conda install -c conda-forge ossfs
 
 Quick Start
 ------------
 
-Here is a simple example of locating and reading a object in OSS.
+Here is a simple example of locating and reading an object in OSS.
 
 .. code:: python
 
    import ossfs
    fs = ossfs.OSSFileSystem(endpoint='http://oss-cn-hangzhou.aliyuncs.com')
    fs.ls('/dvc-test-anonymous/LICENSE')
    [{'name': '/dvc-test-anonymous/LICENSE',
```

### Comparing `ossfs-2023.4.0/docs/assets/logo.svg` & `ossfs-2023.5.0/docs/assets/logo.svg`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/docs/gen_ref_pages.py` & `ossfs-2023.5.0/docs/gen_ref_pages.py`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/mkdocs.yml` & `ossfs-2023.5.0/mkdocs.yml`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/noxfile.py` & `ossfs-2023.5.0/noxfile.py`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/pyproject.toml` & `ossfs-2023.5.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/setup.cfg` & `ossfs-2023.5.0/setup.cfg`

 * *Files 8% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 [options]
 python_requires = >=3.8
 zip_safe = False
 package_dir = 
 	=src
 packages = find:
 install_requires = 
-	fsspec==2023.4.0
+	fsspec==2023.5.0
 	oss2==2.17.0
 	aiooss2==0.2.5
 
 [options.extras_require]
 docs = 
 	mkdocs==1.3.1
 	mkdocs-gen-files==0.3.5
@@ -40,15 +40,15 @@
 	pytest==7.2.0
 	pytest-sugar==0.9.5
 	pytest-cov==3.0.0
 	pytest-mock==3.8.2
 	pylint==2.15.0
 	pylint-pytest==1.1.2
 	mypy==0.971
-	requests==2.28.2
+	requests==2.30.0
 	aliyun-python-sdk-sts==3.1.1
 dev = 
 	%(tests)s
 	%(docs)s
 
 [options.packages.find]
 exclude =
```

### Comparing `ossfs-2023.4.0/src/ossfs/async_oss.py` & `ossfs-2023.5.0/src/ossfs/async_oss.py`

 * *Files 0% similar despite different names*

```diff
@@ -96,15 +96,15 @@
                 endpoint=self._endpoint,
                 bucket_name=bucket_name,
                 connect_timeout=connect_timeout,
                 session=self._session,
                 app_name="ossfs",
             )
         except ClientError as err:
-            raise ValueError(bucket_name) from err
+            raise FileNotFoundError(bucket_name) from err
 
     async def set_session(self, refresh: bool = False):
         """Establish a connection session object.
         Returns
         -------
         Session to be closed later with await .close()
         """
@@ -333,15 +333,15 @@
             for bucket_info in await self._ls_buckets():
                 if bucket_info["name"] == norm_path.rstrip("/"):
                     return {
                         "size": 0,
                         "name": path,
                         "type": "directory",
                     }
-        raise FileNotFoundError(norm_path)
+        raise FileNotFoundError(path)
 
     def _cache_result_analysis(self, norm_path: str, parent: str) -> bool:
         if norm_path in self.dircache:
             for file_info in self.dircache[norm_path]:
                 # For files the dircache can contain itself.
                 # If it contains anything other than itself it is a directory.
                 if file_info["name"] != norm_path:
```

### Comparing `ossfs-2023.4.0/src/ossfs/base.py` & `ossfs-2023.5.0/src/ossfs/base.py`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/src/ossfs/core.py` & `ossfs-2023.5.0/src/ossfs/core.py`

 * *Files 0% similar despite different names*

```diff
@@ -63,15 +63,15 @@
                 self._endpoint,
                 bucket_name,
                 session=self._session,
                 connect_timeout=connect_timeout,
                 app_name="ossfs",
             )
         except oss2.exceptions.ClientError as err:
-            raise ValueError(bucket_name) from err
+            raise FileNotFoundError(bucket_name) from err
 
     def _call_oss(
         self,
         method_name: str,
         *args,
         bucket: Optional[str] = None,
         timeout: Optional[int] = None,
```

### Comparing `ossfs-2023.4.0/src/ossfs/exceptions.py` & `ossfs-2023.5.0/src/ossfs/exceptions.py`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/src/ossfs/file.py` & `ossfs-2023.5.0/src/ossfs/file.py`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/src/ossfs/utils.py` & `ossfs-2023.5.0/src/ossfs/utils.py`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/src/ossfs.egg-info/PKG-INFO` & `ossfs-2023.5.0/src/ossfs.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ossfs
-Version: 2023.4.0
+Version: 2023.5.0
 Summary: fsspec filesystem for OSS
 Home-page: https://github.com/fsspec/ossfs
 Download-URL: https://github.com/fsspec/ossfs
 Maintainer-email: gao@iterive.ai
 License: Apache-2.0
 Platform: any
 Classifier: Programming Language :: Python :: 3
@@ -70,15 +70,15 @@
 .. code:: console
 
    $ conda install -c conda-forge ossfs
 
 Quick Start
 ------------
 
-Here is a simple example of locating and reading a object in OSS.
+Here is a simple example of locating and reading an object in OSS.
 
 .. code:: python
 
    import ossfs
    fs = ossfs.OSSFileSystem(endpoint='http://oss-cn-hangzhou.aliyuncs.com')
    fs.ls('/dvc-test-anonymous/LICENSE')
    [{'name': '/dvc-test-anonymous/LICENSE',
```

### Comparing `ossfs-2023.4.0/src/ossfs.egg-info/SOURCES.txt` & `ossfs-2023.5.0/src/ossfs.egg-info/SOURCES.txt`

 * *Files 8% similar despite different names*

```diff
@@ -34,11 +34,12 @@
 src/ossfs.egg-info/top_level.txt
 tests/__init__.py
 tests/conftest.py
 tests/bench/__init__.py
 tests/bench/test_put_get.py
 tests/func/__init__.py
 tests/func/test_bucket.py
+tests/func/test_error.py
 tests/func/test_file.py
 tests/func/test_login.py
 tests/func/test_object.py
 tests/func/test_ossfs.py
```

### Comparing `ossfs-2023.4.0/src/ossfs.egg-info/requires.txt` & `ossfs-2023.5.0/src/ossfs.egg-info/requires.txt`

 * *Files 2% similar despite different names*

```diff
@@ -1,20 +1,20 @@
-fsspec==2023.4.0
+fsspec==2023.5.0
 oss2==2.17.0
 aiooss2==0.2.5
 
 [dev]
 pytest==7.2.0
 pytest-sugar==0.9.5
 pytest-cov==3.0.0
 pytest-mock==3.8.2
 pylint==2.15.0
 pylint-pytest==1.1.2
 mypy==0.971
-requests==2.28.2
+requests==2.30.0
 aliyun-python-sdk-sts==3.1.1
 mkdocs==1.3.1
 mkdocs-gen-files==0.3.5
 mkdocs-material==8.4.1
 mkdocs-section-index==0.3.4
 mkdocstrings-python==0.7.1
 
@@ -29,9 +29,9 @@
 pytest==7.2.0
 pytest-sugar==0.9.5
 pytest-cov==3.0.0
 pytest-mock==3.8.2
 pylint==2.15.0
 pylint-pytest==1.1.2
 mypy==0.971
-requests==2.28.2
+requests==2.30.0
 aliyun-python-sdk-sts==3.1.1
```

### Comparing `ossfs-2023.4.0/tests/conftest.py` & `ossfs-2023.5.0/tests/conftest.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 """
 Pytest setup
 """
 # pylint: disable=missing-function-docstring
 # pylint: disable=redefined-outer-name
+import inspect
 import os
 import pathlib
 import subprocess
 import uuid
-from typing import Dict, Union
+from typing import Dict, Optional, Union
 
 import oss2
 import pytest
 import requests
 from oss2 import Auth
 
 from ossfs import AioOSSFileSystem, OSSFileSystem
@@ -26,14 +27,22 @@
 test_id = uuid.uuid4()
 
 
 def bucket_relative_path(path: str) -> str:
     return path.split("/", 2)[2]
 
 
+def function_name(ossfs: Optional[Union["OSSFileSystem", "AioOSSFileSystem"]] = None):
+    file_name = inspect.stack()[1].filename.rsplit(os.sep, maxsplit=1)[-1][:-3]
+    function_name = inspect.stack()[1][0].f_code.co_name
+    if ossfs:
+        function_name += f"_{ossfs.__class__.__name__}"
+    return f"{file_name}/{function_name}"
+
+
 @pytest.fixture(scope="session")
 def emulator_endpoint() -> str:
     return f"http://127.0.0.1:{PORT}/"
 
 
 @pytest.fixture(scope="session")
 def endpoint() -> str:
@@ -45,14 +54,19 @@
 @pytest.fixture(scope="session")
 def test_bucket_name() -> str:
     test_bucket_name = os.environ.get("OSS_TEST_BUCKET_NAME")
     assert test_bucket_name
     return test_bucket_name
 
 
+@pytest.fixture(scope="session", name="test_path")
+def file_level_path(test_bucket_name: str, test_directory: str) -> str:
+    return f"/{test_bucket_name}/{test_directory}"
+
+
 @pytest.fixture(scope="session")
 def anonymous_bucket_name() -> str:
     anonymous_bucket_name = os.environ.get("OSS_TEST_ANONYMOUS_BUCKET_NAME")
     assert anonymous_bucket_name
     return anonymous_bucket_name
```

### Comparing `ossfs-2023.4.0/tests/func/test_bucket.py` & `ossfs-2023.5.0/tests/func/test_bucket.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 """tests for bucket level operations"""
-# pylint:disable = too-many-arguments
 # pylint:disable=missing-function-docstring
 from typing import TYPE_CHECKING, Union
 
 import pytest
 from oss2.auth import AnonymousAuth
 
 if TYPE_CHECKING:
```

### Comparing `ossfs-2023.4.0/tests/func/test_file.py` & `ossfs-2023.5.0/tests/func/test_file.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,106 +1,93 @@
 """
 Test all OSSFile related methods
 """
-import inspect
-
-# pylint:disable=invalid-name
 # pylint:disable=missing-function-docstring
-# pylint:disable=protected-access
 import io
 import os
 from typing import TYPE_CHECKING, Union
 
 import pytest
 
-from ..conftest import LICENSE_PATH, NUMBERS, bucket_relative_path
+from ..conftest import LICENSE_PATH, NUMBERS, bucket_relative_path, function_name
 
 if TYPE_CHECKING:
     from oss2 import Bucket
 
     from ossfs import AioOSSFileSystem, OSSFileSystem
 
 
-@pytest.fixture(scope="module", name="test_path")
-def file_level_path(test_bucket_name: str, test_directory: str):
-    current_file_name = __file__.rsplit(os.sep, maxsplit=1)[-1]
-    return f"/{test_bucket_name}/{test_directory}/{current_file_name}"
-
-
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_simple_read(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    object_name = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/"
+    object_name = f"{test_path}/{function_name(ossfs)}"
     data = os.urandom(10 * 2**20)
     bucket.put_object(bucket_relative_path(object_name), data)
 
-    with ossfs.open(object_name, "rb") as f:
-        out = f.read(len(data))
+    with ossfs.open(object_name, "rb") as f_rb:
+        out = f_rb.read(len(data))
     assert len(data) == len(out)
     assert out == data
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_simple_write(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    object_name = f"{test_path}/{function_name}"
+    object_name = f"{test_path}/{function_name(ossfs)}"
     data = os.urandom(10 * 2**20)
 
-    with ossfs.open(object_name, "wb") as f:
-        f.write(data)
+    with ossfs.open(object_name, "wb") as f_wb:
+        f_wb.write(data)
 
     out = bucket.get_object(bucket_relative_path(object_name)).read()
     assert out == data
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_seek(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    object_name = f"{test_path}/{function_name}"
+    object_name = f"{test_path}/{function_name(ossfs)}"
     bucket.put_object(bucket_relative_path(object_name), b"123")
 
-    with ossfs.open(object_name) as f:
-        f.seek(1000)
+    with ossfs.open(object_name) as f_seek:
+        f_seek.seek(1000)
         with pytest.raises(ValueError):
-            f.seek(-1)
+            f_seek.seek(-1)
         with pytest.raises(ValueError):
-            f.seek(-5, 2)
+            f_seek.seek(-5, 2)
         with pytest.raises(ValueError):
-            f.seek(0, 10)
-        f.seek(0)
-        assert f.read(1) == b"1"
-        f.seek(0)
-        assert f.read(1) == b"1"
-        f.seek(3)
-        assert f.read(1) == b""
-        f.seek(-1, 2)
-        assert f.read(1) == b"3"
-        f.seek(-1, 1)
-        f.seek(-1, 1)
-        assert f.read(1) == b"2"
+            f_seek.seek(0, 10)
+        f_seek.seek(0)
+        assert f_seek.read(1) == b"1"
+        f_seek.seek(0)
+        assert f_seek.read(1) == b"1"
+        f_seek.seek(3)
+        assert f_seek.read(1) == b""
+        f_seek.seek(-1, 2)
+        assert f_seek.read(1) == b"3"
+        f_seek.seek(-1, 1)
+        f_seek.seek(-1, 1)
+        assert f_seek.read(1) == b"2"
         for i in range(4):
-            assert f.seek(i) == i
+            assert f_seek.seek(i) == i
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_read_small(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     number_file: str,
     bucket: "Bucket",
 ):
-    with ossfs.open(number_file, "rb", block_size=3) as f:
+    with ossfs.open(number_file, "rb", block_size=3) as f_rb:
         out = []
         while True:
-            data = f.read(2)
+            data = f_rb.read(2)
             if data == b"":
                 break
             out.append(data)
         assert bucket.get_object(bucket_relative_path(number_file)).read() == b"".join(
             out
         )
 
@@ -135,263 +122,260 @@
 @pytest.mark.parametrize("size", [2**10, 2**20, 10 * 2**20])
 def test_write(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     test_path: str,
     size: int,
     bucket: "Bucket",
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    object_name = f"{test_path}/{function_name}"
+    object_name = f"{test_path}/{function_name(ossfs)}"
     data = os.urandom(size)
-    with ossfs.open(object_name, "wb") as f:
-        f.write(data)
+    with ossfs.open(object_name, "wb") as f_wb:
+        f_wb.write(data)
     out = bucket.get_object(bucket_relative_path(object_name)).read()
     assert data == out
     assert ossfs.info(object_name)["Size"] == len(data)
     ossfs.open(object_name, "wb").close()
     assert ossfs.info(object_name)["Size"] == 0
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_write_fails(ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    object_name = f"{test_path}/{function_name}"
+    object_name = f"{test_path}/{function_name(ossfs)}"
     ossfs.touch(object_name)
     with pytest.raises(ValueError):
         ossfs.open(object_name, "rb").write(b"hello")
-    f = ossfs.open(object_name, "wb")
-    f.close()
+    f_wb = ossfs.open(object_name, "wb")
+    f_wb.close()
     with pytest.raises(ValueError):
-        f.write(b"hello")
+        f_wb.write(b"hello")
     with pytest.raises(FileNotFoundError):
         ossfs.open("nonexistentbucket/temp", "wb").close()
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_write_blocks(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    object_name = f"{test_path}/{function_name}"
-    with ossfs.open(object_name, "wb") as f:
-        f.write(os.urandom(2 * 2**20))
-        assert f.buffer.tell() == 2 * 2**20
-        f.flush()
-        assert f.buffer.tell() == 2 * 2**20
-        f.write(os.urandom(2 * 2**20))
-        f.write(os.urandom(2 * 2**20))
+    object_name = f"{test_path}/{function_name(ossfs)}"
+    with ossfs.open(object_name, "wb") as f_wb:
+        f_wb.write(os.urandom(2 * 2**20))
+        assert f_wb.buffer.tell() == 2 * 2**20
+        f_wb.flush()
+        assert f_wb.buffer.tell() == 2 * 2**20
+        f_wb.write(os.urandom(2 * 2**20))
+        f_wb.write(os.urandom(2 * 2**20))
     out = bucket.get_object(bucket_relative_path(object_name)).read()
     assert len(out) == 6 * 2**20
-    with ossfs.open(object_name, "wb", block_size=10 * 2**20) as f:
-        f.write(os.urandom(15 * 2**20))
-        assert f.buffer.tell() == 0
+    with ossfs.open(object_name, "wb", block_size=10 * 2**20) as f_wb:
+        f_wb.write(os.urandom(15 * 2**20))
+        assert f_wb.buffer.tell() == 0
     out = bucket.get_object(bucket_relative_path(object_name)).read()
     assert len(out) == 15 * 2**20
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_readline(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     number_file: str,
     license_file: str,
 ):
-    with ossfs.open("/".join([number_file]), "rb") as f_r:
-        result = f_r.readline()
+    with ossfs.open("/".join([number_file]), "rb") as f_rb:
+        result = f_rb.readline()
         expected = NUMBERS
         assert result == expected
 
-    with ossfs.open("/".join([license_file]), "rb") as f_r, open(
+    with ossfs.open("/".join([license_file]), "rb") as f_rb, open(
         LICENSE_PATH, "rb"
     ) as f_l:
-        result = f_r.readline()
+        result = f_rb.readline()
         expected = f_l.readline()
         assert result == expected
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_readline_empty(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str
 ):
-    file = test_path + "/test_readline_empty/empty"
+    file = f"{test_path}/{function_name(ossfs)}/empty"
     data = b""
-    with ossfs.open(file, "wb") as f:
-        f.write(data)
-    with ossfs.open(file, "rb") as f:
-        result = f.readline()
+    with ossfs.open(file, "wb") as f_wb:
+        f_wb.write(data)
+    with ossfs.open(file, "rb") as f_rb:
+        result = f_rb.readline()
         assert result == data
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_readline_blocksize(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str
 ):
-    test_file_a = test_path + "/test_readline_blocksize/a"
+    test_file_a = f"{test_path}/{function_name(ossfs)}/a"
     data = b"ab\n" + b"a" * (10 * 2**20) + b"\nab"
-    with ossfs.open(test_file_a, "wb") as f:
-        f.write(data)
-    with ossfs.open(test_file_a, "rb") as f:
-        result = f.readline()
+    with ossfs.open(test_file_a, "wb") as f_wb:
+        f_wb.write(data)
+    with ossfs.open(test_file_a, "rb") as f_rb:
+        result = f_rb.readline()
         expected = b"ab\n"
         assert result == expected
 
-        result = f.readline()
+        result = f_rb.readline()
         expected = b"a" * (10 * 2**20) + b"\n"
         assert result == expected
 
-        result = f.readline()
+        result = f_rb.readline()
         expected = b"ab"
         assert result == expected
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_next(ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], license_file: str):
-    with open(LICENSE_PATH, "rb") as f_l, ossfs.open(license_file) as f_r:
-        expected = f_l.readline()
+    with open(LICENSE_PATH, "rb") as f_rb, ossfs.open(license_file) as f_r:
+        expected = f_rb.readline()
         result = next(f_r)
         assert result == expected
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_iterable(ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str):
-    file = test_path + "/test_iterable/file"
+    file = f"{test_path}/{function_name(ossfs)}/file"
     data = b"abc\n123"
-    with ossfs.open(file, "wb") as f:
-        f.write(data)
-    with ossfs.open(file) as f, io.BytesIO(data) as g:
-        for fromossfs, fromio in zip(f, g):
+    with ossfs.open(file, "wb") as f_wb:
+        f_wb.write(data)
+    with ossfs.open(file) as f_r, io.BytesIO(data) as bytes_io:
+        for fromossfs, fromio in zip(f_r, bytes_io):
             assert fromossfs == fromio
-        f.seek(0)
-        assert f.readline() == b"abc\n"
-        assert f.readline() == b"123"
-        f.seek(1)
-        assert f.readline() == b"bc\n"
-
-    with ossfs.open(file) as f:
-        out = list(f)
-    with ossfs.open(file) as f:
-        out2 = f.readlines()
+        f_r.seek(0)
+        assert f_r.readline() == b"abc\n"
+        assert f_r.readline() == b"123"
+        f_r.seek(1)
+        assert f_r.readline() == b"bc\n"
+
+    with ossfs.open(file) as f_r:
+        out = list(f_r)
+    with ossfs.open(file) as f_r:
+        out2 = f_r.readlines()
     assert out == out2
     assert b"".join(out) == data
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_file_status(ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str):
-    file = test_path + "/test_file_status/file"
-    with ossfs.open(file, "wb") as f:
-        assert not f.readable()
-        assert not f.seekable()
-        assert f.writable()
-
-    with ossfs.open(file, "rb") as f:
-        assert f.readable()
-        assert f.seekable()
-        assert not f.writable()
+    file = f"{test_path}/{function_name(ossfs)}/file"
+    with ossfs.open(file, "wb") as f_wb:
+        assert not f_wb.readable()
+        assert not f_wb.seekable()
+        assert f_wb.writable()
+
+    with ossfs.open(file, "rb") as f_rb:
+        assert f_rb.readable()
+        assert f_rb.seekable()
+        assert not f_rb.writable()
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 @pytest.mark.parametrize("data_size", [0, 20, 10 * 2**20])
 @pytest.mark.parametrize("append_size", [0, 20, 10 * 2**20])
 def test_append(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     test_path: str,
     data_size: int,
     append_size: int,
 ):
-    file = test_path + f"/test_append/file_{data_size}_{append_size}"
+    file = f"{test_path}/{function_name(ossfs)}/file_{data_size}_{append_size}"
     data = os.urandom(data_size)
     extra = os.urandom(append_size)
-    with ossfs.open(file, "wb") as f:
-        f.write(data)
+    with ossfs.open(file, "wb") as f_wb:
+        f_wb.write(data)
     assert ossfs.cat(file) == data
-    with ossfs.open(file, "ab") as f:
-        f.write(extra)  # append, write, small file
+    with ossfs.open(file, "ab") as f_ab:
+        f_ab.write(extra)  # append, write, small file
     assert ossfs.cat(file) == data + extra
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_bigger_than_block_read(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], number_file: str
 ):
-    with ossfs.open(number_file, "rb", block_size=3) as f:
+    with ossfs.open(number_file, "rb", block_size=3) as f_rb:
         out = []
         while True:
-            data = f.read(4)
+            data = f_rb.read(4)
             out.append(data)
             if len(data) == 0:
                 break
     assert b"".join(out) == NUMBERS
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_text_io__stream_wrapper_works(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str
 ):
     """Ensure using TextIOWrapper works."""
-    file = test_path + "/test_text_io__stream_wrapper_works/file"
-    with ossfs.open(file, "wb") as fd:
-        fd.write("\u00af\\_(\u30c4)_/\u00af".encode("utf-16-le"))
+    file = f"{test_path}/{function_name(ossfs)}/file"
+    with ossfs.open(file, "wb") as f_wb:
+        f_wb.write("\u00af\\_(\u30c4)_/\u00af".encode("utf-16-le"))
 
-    with ossfs.open(file, "rb") as fd:
-        with io.TextIOWrapper(fd, "utf-16-le") as stream:
+    with ossfs.open(file, "rb") as f_rb:
+        with io.TextIOWrapper(f_rb, "utf-16-le") as stream:
             assert stream.readline() == "\u00af\\_(\u30c4)_/\u00af"
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_text_io__basic(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str
 ):
     """Text mode is now allowed."""
-    file = test_path + "/test_text_io__basic/file"
-    with ossfs.open(file, "w", encoding="utf-8") as fd:
-        fd.write("\u00af\\_(\u30c4)_/\u00af")
+    file = f"{test_path}/{function_name(ossfs)}/file"
+    with ossfs.open(file, "w", encoding="utf-8") as f_w:
+        f_w.write("\u00af\\_(\u30c4)_/\u00af")
 
-    with ossfs.open(file, "r", encoding="utf-8") as fd:
-        assert fd.read() == "\u00af\\_(\u30c4)_/\u00af"
+    with ossfs.open(file, "r", encoding="utf-8") as f_r:
+        assert f_r.read() == "\u00af\\_(\u30c4)_/\u00af"
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_text_io__override_encoding(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str
 ):
     """Allow overriding the default text encoding."""
-    file = test_path + "/test_text_io__override_encoding/file"
+    file = f"{test_path}/{function_name(ossfs)}/file"
 
-    with ossfs.open(file, "w", encoding="ibm500") as fd:
-        fd.write("Hello, World!")
+    with ossfs.open(file, "w", encoding="ibm500") as f_w:
+        f_w.write("Hello, World!")
 
-    with ossfs.open(file, "r", encoding="ibm500") as fd:
-        assert fd.read() == "Hello, World!"
+    with ossfs.open(file, "r", encoding="ibm500") as f_r:
+        assert f_r.read() == "Hello, World!"
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_readinto(ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str):
-    file = test_path + "/test_readinto/file"
+    file = f"{test_path}/{function_name(ossfs)}/file"
 
-    with ossfs.open(file, "wb") as fd:
-        fd.write(b"Hello, World!")
+    with ossfs.open(file, "wb") as f_wb:
+        f_wb.write(b"Hello, World!")
 
     contents = bytearray(15)
 
-    with ossfs.open(file, "rb") as fd:
-        assert fd.readinto(contents) == 13
+    with ossfs.open(file, "rb") as f_wb:
+        assert f_wb.readinto(contents) == 13
 
     assert contents.startswith(b"Hello, World!")
 
 
 @pytest.mark.parametrize("ossfs", ["async", "sync"], indirect=True)
 def test_seek_reads(ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str):
-    file = test_path + "/test_seek_reads/file"
-    with ossfs.open(file, "wb") as f:
-        f.write(os.urandom(5627146))
-    with ossfs.open(file, "rb", blocksize=100) as f:
-        f.seek(5561610)
-        f.read(65536)
+    file = f"{test_path}/{function_name(ossfs)}/file"
+    with ossfs.open(file, "wb") as f_wb:
+        f_wb.write(os.urandom(5627146))
+    with ossfs.open(file, "rb", blocksize=100) as f_rb:
+        f_rb.seek(5561610)
+        f_rb.read(65536)
 
-        f.seek(4)
+        f_rb.seek(4)
         size = 562198
-        d2 = f.read(size)
-        assert len(d2) == size
+        data_2 = f_rb.read(size)
+        assert len(data_2) == size
 
-        f.seek(562288)
+        f_rb.seek(562288)
         size = 562187
-        d3 = f.read(size)
-        assert len(d3) == size
+        data_3 = f_rb.read(size)
+        assert len(data_3) == size
```

### Comparing `ossfs-2023.4.0/tests/func/test_login.py` & `ossfs-2023.5.0/tests/func/test_login.py`

 * *Files identical despite different names*

### Comparing `ossfs-2023.4.0/tests/func/test_object.py` & `ossfs-2023.5.0/tests/func/test_object.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,54 +1,43 @@
 """
 Test all oss object related methods
 """
-import inspect
 
-# pylint:disable=invalid-name
 # pylint:disable=missing-function-docstring
-# pylint:disable=protected-access
-# pylint:disable=consider-using-with
 import os
 import time
 from typing import TYPE_CHECKING, Union
 
 import fsspec
 import pytest
 
-from ..conftest import NUMBERS, bucket_relative_path
+from ..conftest import NUMBERS, bucket_relative_path, function_name
 
 if TYPE_CHECKING:
     from oss2 import Bucket
 
     from ossfs import AioOSSFileSystem, OSSFileSystem
 
 
-@pytest.fixture(scope="module", name="test_path")
-def file_name_path(test_bucket_name: str, test_directory: str):
-    current_file = __file__.rsplit(os.sep, maxsplit=1)[-1]
-    return f"/{test_bucket_name}/{test_directory}/{current_file}"
-
-
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_info(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
     # test file info
-    function_name = inspect.stack()[0][0].f_code.co_name
-    object_name_foo = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/foo"
+    object_name_foo = f"{test_path}/{function_name(ossfs)}/foo"
     bucket.put_object(bucket_relative_path(object_name_foo), "foo")
     info = ossfs.info(object_name_foo)
     linfo = ossfs.ls(object_name_foo, detail=True)[0]
 
     assert abs(info.pop("LastModified") - linfo.pop("LastModified")) <= 1
     assert info["size"] == 3
     assert info == linfo
 
     # test not exist dir
-    file_path = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/"
+    file_path = f"{test_path}/{function_name(ossfs)}/"
     object_name_bar = file_path + "bar"
     with pytest.raises(FileNotFoundError):
         ossfs.info(object_name_bar)
     ossfs.invalidate_cache(file_path)
 
     # add a new file then we can info this new dir.
     bucket.put_object(bucket_relative_path(object_name_bar), "bar")
@@ -56,16 +45,15 @@
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_checksum(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
     # don't make local "directory"
-    function_name = inspect.stack()[0][0].f_code.co_name
-    object_name = f"{test_path}/{function_name}"
+    object_name = f"{test_path}/{function_name(ossfs)}"
 
     # change one file, using cache
     bucket.put_object(bucket_relative_path(object_name), "foo")
     checksum = ossfs.checksum(object_name)
 
     # Test changed contents
     bucket.put_object(bucket_relative_path(object_name), "bar")
@@ -87,41 +75,38 @@
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_ls_object(
     # don't make local "directory"
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     test_path: str,
     bucket: "Bucket",
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     assert ossfs.ls(path + "nonexistent") == []
     ossfs.invalidate_cache(path)
     filename = path + "accounts.1.json"
     bucket.put_object(bucket_relative_path(filename), "")
     assert filename in ossfs.ls(path, detail=False)
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_ls_dir(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file = path + "file"
     bucket.put_object(bucket_relative_path(file), "")
     assert file in ossfs.ls(path, detail=False)
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_ls_and_touch(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
     # don't make local "directory"
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file_a = path + "a"
     file_b = path + "b"
     assert not bucket.object_exists(bucket_relative_path(path))
     ossfs.touch(file_a)
     ossfs.touch(file_b)
     ls_result = ossfs.ls(path, detail=True)
     assert {result["Key"] for result in ls_result} == {file_a, file_b}
@@ -133,16 +118,15 @@
 def test_isfile(
     # don't make local "directory"
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     test_path: str,
     bucket: "Bucket",
 ):
     "test isfile in ossfs"
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file_foo = path + "foo"
     assert not ossfs.isfile("")
     assert not ossfs.isfile("/")
     assert not ossfs.isfile(path)
 
     assert not ossfs.isfile(file_foo)
     ossfs.invalidate_cache()
@@ -151,30 +135,28 @@
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_isdir(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
     "test isdir in ossfs"
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file_foo = path + "foo"
     bucket.put_object(bucket_relative_path(file_foo), "foo")
     assert not ossfs.isdir(file_foo)
     assert ossfs.isdir(test_path)
     assert ossfs.isdir(path)
     assert ossfs.isdir(path.rstrip("/"))
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_rm(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file_foo = path + "foo"
     nest_file = path + "nested/nested2/file1"
     bucket.put_object(bucket_relative_path(file_foo), "foo")
     assert bucket.object_exists(bucket_relative_path(file_foo))
     ossfs.rm(file_foo)
     assert not bucket.object_exists(bucket_relative_path(file_foo))
     with pytest.raises(FileNotFoundError):
@@ -184,16 +166,15 @@
     assert not bucket.object_exists(bucket_relative_path(nest_file))
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_bulk_delete(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     nest_file1 = path + "nested/file1"
     nest_file2 = path + "nested/file2"
     bucket.put_object(bucket_relative_path(nest_file1), "foo")
     bucket.put_object(bucket_relative_path(nest_file2), "bar")
     filelist = ossfs.find(path + "nested/")
     assert set(filelist) == {nest_file1, nest_file2}
     ossfs.rm(filelist)
@@ -212,63 +193,59 @@
     assert ossfs.info(number_file)["Size"] == len(NUMBERS)
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_du(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file1 = path + "file1"
     file2 = path + "dir/file2"
     file3 = path + "dir/file3"
     bucket.put_object(bucket_relative_path(file1), b"1234567890")
     bucket.put_object(bucket_relative_path(file2), b"12345")
     bucket.put_object(bucket_relative_path(file3), b"1234567890" * 2)
 
-    d = ossfs.du(path, total=False)
-    assert all(isinstance(v, int) and v >= 0 for v in d.values())
-    assert d[file1] == 10
-    assert d[file2] == 5
-    assert d[file3] == 20
+    du_result = ossfs.du(path, total=False)
+    assert all(isinstance(v, int) and v >= 0 for v in du_result.values())
+    assert du_result[file1] == 10
+    assert du_result[file2] == 5
+    assert du_result[file3] == 20
     assert ossfs.du(path, total=True) == 35
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_ossfs_ls(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     filename = path + "nested/file1"
     bucket.put_object(bucket_relative_path(filename), "foo")
     assert filename not in ossfs.ls(path, detail=False)
     assert filename in ossfs.ls(path + "nested/", detail=False)
     assert filename in ossfs.ls(path + "nested", detail=False)
-    L = ossfs.ls(path + "nested", detail=True)
-    assert all(isinstance(item, dict) for item in L)
+    ls_result = ossfs.ls(path + "nested", detail=True)
+    assert all(isinstance(item, dict) for item in ls_result)
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_ossfs_big_ls(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     for num in range(120):
         bucket.put_object(bucket_relative_path(f"{path}{num}.part"), "foo")
     assert len(ossfs.ls(path, detail=False, connect_timeout=600)) == 120
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_ossfs_glob(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file1 = path + "nested/file.dat"
     file2 = path + "nested/filedat"
     bucket.put_object(bucket_relative_path(file1), "foo")
     bucket.put_object(bucket_relative_path(file2), "bar")
     assert file1 not in ossfs.glob(path + "")
     assert file1 not in ossfs.glob(path + "*")
     assert file1 not in ossfs.glob(path + "nested")
@@ -289,30 +266,28 @@
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_copy(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     number_file: str,
     test_path: str,
     bucket: "Bucket",
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     new_file = path + "file"
     ossfs.copy(number_file, new_file)
     assert bucket.get_object(bucket_relative_path(new_file)).read() == NUMBERS
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_move(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     number_file: str,
     test_path: str,
     bucket: "Bucket",
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     from_file = path + "from"
     to_file = path + "to"
     ossfs.copy(number_file, from_file)
     assert bucket.object_exists(bucket_relative_path(from_file))
     assert not bucket.object_exists(bucket_relative_path(to_file))
     ossfs.mv(from_file, to_file)
     assert bucket.get_object(bucket_relative_path(to_file)).read() == NUMBERS
@@ -324,84 +299,48 @@
 def test_get_put(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     tmpdir,
     test_path: str,
     size: int,
     bucket: "Bucket",
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
 
     local_file = str(tmpdir.join("number"))
     data = os.urandom(size)
-    open(local_file, "wb").write(data)
+    open(local_file, "wb").write(data)  # pylint:disable=consider-using-with
 
     remote_file = path + "file"
     ossfs.put(local_file, remote_file)
     assert bucket.object_exists(bucket_relative_path(remote_file))
     assert bucket.get_object(bucket_relative_path(remote_file)).read() == data
 
     get_file = str(tmpdir.join("get"))
     ossfs.get(remote_file, get_file)
-    assert open(get_file, "rb").read() == data
+    assert open(get_file, "rb").read() == data  # pylint:disable=consider-using-with
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 @pytest.mark.parametrize("size", [2**10, 20 * 2**20])
 def test_pipe_cat_big(
     ossfs: "OSSFileSystem", size: int, test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     bigfile = path + "bigfile"
     data = os.urandom(size)
     ossfs.pipe(bigfile, data)
     assert bucket.get_object(bucket_relative_path(bigfile)).read() == data
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
-def test_errors(
-    ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
-):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
-
-    with pytest.raises(FileNotFoundError):
-        ossfs.open(path + "none", "rb")
-
-    with pytest.raises(FileNotFoundError):
-        ossfs.mv(path + "x", path + "y")
-
-    with pytest.raises(ValueError):
-        ossfs.open("x", "rb")
-
-    with pytest.raises(FileNotFoundError):
-        ossfs.open("xxxx", "rb")
-
-    with pytest.raises(PermissionError):
-        ossfs.rm("/non-exist-bucket")
-
-    with pytest.raises(ValueError):
-        with ossfs.open(path + "temp", "wb") as f:
-            f.read()
-
-    bucket.put_object(path.split("/", 2)[-1] + "temp", "foobar")
-    with pytest.raises(ValueError):
-        f = ossfs.open(path + "temp", "rb")
-        f.close()
-        f.read()
-
-
-@pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_touch(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
     # create
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/{ossfs.__class__.__name__}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     filename = path + "file"
     assert not bucket.object_exists(bucket_relative_path(filename))
     ossfs.touch(filename)
     assert bucket.object_exists(bucket_relative_path(filename))
     assert bucket.get_object(bucket_relative_path(filename)).read() == b""
 
     bucket.put_object(bucket_relative_path(filename), b"data")
@@ -410,16 +349,15 @@
     assert bucket.get_object(bucket_relative_path(filename)).read() == b"data"
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_cat_missing(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file1 = path + "file0"
     file2 = path + "file1"
     ossfs.touch(file1)
     bucket.put_object(bucket_relative_path(file1), b"foo")
     with pytest.raises(FileNotFoundError):
         ossfs.cat([file1, file2], on_error="raise")
     out = ossfs.cat([file1, file2], on_error="omit")
@@ -432,35 +370,33 @@
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_get_directories(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     tmpdir,
     test_path: str,
     bucket: "Bucket",
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     bucket.put_object(bucket_relative_path(path + "dir/dirkey/key0"), "")
     bucket.put_object(bucket_relative_path(path + "dir/dirkey/key1"), "")
     bucket.put_object(bucket_relative_path(path + "dir/dir/key"), "")
-    d = str(tmpdir)
-    ossfs.get(path + "dir/", d, recursive=True)
-    assert {"dirkey", "dir"} == set(os.listdir(d))
-    assert ["key"] == os.listdir(os.path.join(d, "dir"))
-    assert {"key0", "key1"} == set(os.listdir(os.path.join(d, "dirkey")))
+    tmpdir_str = str(tmpdir)
+    ossfs.get(path + "dir/", tmpdir_str, recursive=True)
+    assert {"dirkey", "dir"} == set(os.listdir(tmpdir_str))
+    assert ["key"] == os.listdir(os.path.join(tmpdir_str, "dir"))
+    assert {"key0", "key1"} == set(os.listdir(os.path.join(tmpdir_str, "dirkey")))
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_modified(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"],
     test_path: str,
     test_bucket_name: str,
     bucket: "Bucket",
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file_path = path + "file"
     notexist_path = path + "notexist"
 
     # Test file
     bucket.put_object(bucket_relative_path(file_path), "")
     modified = ossfs.modified(path=file_path)
     assert isinstance(modified, int)
@@ -478,16 +414,15 @@
         ossfs.modified(path=test_bucket_name)
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_find_file_info_with_selector(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     file_a = path + "test_file_a"
     file_b = path + "test_file_b"
     dir_a = path + "test_dir_a"
     file_c = path + "test_dir_a/test_file_c"
 
     bucket.put_object(bucket_relative_path(file_a), "")
     bucket.put_object(bucket_relative_path(file_b), "")
@@ -509,16 +444,15 @@
             raise ValueError(f"unexpected path {info['name']}")
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_exists(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/{ossfs.__class__.__name__}"
+    path = f"{test_path}/{function_name(ossfs)}/"
     bucket.put_object(bucket_relative_path(path + "very/similar/prefix1"), "")
     bucket.put_object(bucket_relative_path(path + "very/similar/prefix2"), "")
     bucket.put_object(bucket_relative_path(path + "very/similar/prefix3/something"), "")
 
     assert not ossfs.exists(path + "very/similar/prefix")
     assert not ossfs.exists(path + "very/similar/prefi")
     assert not ossfs.exists(path + "very/similar/pref")
@@ -543,29 +477,27 @@
     assert not ossfs.exists(path + "starting/very/similar/prefix/")
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_leading_forward_slash(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     bucket.put_object(bucket_relative_path(path + "some/file"), "")
     assert ossfs.ls(path + "some/")
     path = path.lstrip("/")
     assert ossfs.exists(path + "some/file")
     assert ossfs.exists("/" + path + "some/file")
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_find_with_prefix(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str, bucket: "Bucket"
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     if not ossfs.exists(path):
         for cursor in range(100):
             bucket.put_object(
                 bucket_relative_path(path + f"prefixes/test_{cursor}"), ""
             )
         bucket.put_object(bucket_relative_path(path + "prefixes2"), "")
 
@@ -583,24 +515,23 @@
     test_1s = ossfs.find(path + "prefixes/", prefix="test_1")
     assert len(test_1s) == 11
     assert test_1s == [path + "prefixes/test_1"] + [
         path + f"prefixes/test_{cursor}" for cursor in range(10, 20)
     ]
 
 
-WRITE_BLOCK_SIZE = 2**13  # 8KB blocks
+WRITE_BLOCK_SIZE = 2**14  # 16KB blocks
 READ_BLOCK_SIZE = 2**14  # 16KB blocks
 
 
 @pytest.mark.parametrize("ossfs", ["sync"], indirect=True)
 def test_get_put_file(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], tmpdir, test_path: str
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     src_file = str(tmpdir / "source")
     src2_file = str(tmpdir / "source_2")
     dest_file = path + "get_put_file/dest"
 
     data = b"test" * 2**20
 
     # pylint: disable=missing-class-docstring
```

### Comparing `ossfs-2023.4.0/tests/func/test_ossfs.py` & `ossfs-2023.5.0/tests/func/test_ossfs.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,74 +1,64 @@
 """
 Test class level functionality.
 """
-import inspect
 
-# pylint:disable=protected-access
 # pylint:disable=missing-function-docstring
-# pylint:disable=invalid-name
-import os
 import pickle
 import time
 from multiprocessing.pool import ThreadPool
 from typing import Dict, Union
 
 import fsspec.core
 import pytest
 
 from ossfs import AioOSSFileSystem, OSSFileSystem
 from ossfs.base import BaseOSSFileSystem
 
-
-@pytest.fixture(scope="module", name="test_path")
-def file_level_path(test_bucket_name: str, test_directory: str):
-    file_name = __file__.rsplit(os.sep, maxsplit=1)[-1]
-    return f"/{test_bucket_name}/{test_directory}/{file_name}"
+from ..conftest import function_name
 
 
 @pytest.mark.parametrize("aio", [False, True])
 @pytest.mark.parametrize("default_cache_type", ["none", "bytes", "readahead"])
 def test_default_cache_type(
     init_config: Dict, default_cache_type: str, test_path: str, aio: bool
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name()}/"
     data = b"a" * (10 * 2**20)
     file = path + "/test_default_cache_type/file"
     init_config["default_cache_type"] = default_cache_type
     if aio:
         ossfs = AioOSSFileSystem(**init_config)
     else:
         ossfs = OSSFileSystem(**init_config)
-    with ossfs.open(file, "wb") as f:
-        f.write(data)
+    with ossfs.open(file, "wb") as f_wb:
+        f_wb.write(data)
 
-    with ossfs.open(file, "rb") as f:
-        assert isinstance(f.cache, fsspec.core.caches[default_cache_type])
-        out = f.read(len(data))
+    with ossfs.open(file, "rb") as f_rb:
+        assert isinstance(f_rb.cache, fsspec.core.caches[default_cache_type])
+        out = f_rb.read(len(data))
         assert len(data) == len(out)
         assert out == data
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 @pytest.mark.parametrize("cache_type", ["none", "bytes", "readahead"])
 def test_cache_type(
     ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], cache_type: str, test_path: str
 ):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     data = b"a" * (10 * 2**20)
     file = path + "/test_cache_type/file"
 
-    with ossfs.open(file, "wb") as f:
-        f.write(data)
+    with ossfs.open(file, "wb") as f_wb:
+        f_wb.write(data)
 
-    with ossfs.open(file, "rb", cache_type=cache_type) as f:
-        assert isinstance(f.cache, fsspec.core.caches[cache_type])
-        out = f.read(len(data))
+    with ossfs.open(file, "rb", cache_type=cache_type) as f_rb:
+        assert isinstance(f_rb.cache, fsspec.core.caches[cache_type])
+        out = f_rb.read(len(data))
         assert len(data) == len(out)
         assert out == data
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_current(ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], init_config: Dict):
     ossfs._cache.clear()  # pylint: disable=protected-access
@@ -90,26 +80,31 @@
     assert all(out)
     pool.close()
     pool.join()
 
 
 @pytest.mark.parametrize("ossfs", ["sync", "async"], indirect=True)
 def test_pickle(ossfs: Union["OSSFileSystem", "AioOSSFileSystem"], test_path: str):
-    function_name = inspect.stack()[0][0].f_code.co_name
-    path = f"{test_path}/{function_name}/"
+    path = f"{test_path}/{function_name(ossfs)}/"
     for number in range(10):
         ossfs.touch(path + "file" + str(number))
 
     ossfs1 = pickle.loads(pickle.dumps(ossfs))
     assert ossfs.ls(path) == ossfs1.ls(path)
     ossfs2 = pickle.loads(pickle.dumps(ossfs1))
     assert ossfs.ls(path) == ossfs2.ls(path)
 
 
 def test_strip_protocol():
     """
     Test protocols
     """
     address = "http://oss-cn-hangzhou.aliyuncs.com/mybucket/myobject"
-    assert BaseOSSFileSystem._strip_protocol(address) == "/mybucket/myobject"
+    assert (
+        BaseOSSFileSystem._strip_protocol(address)  # pylint: disable=protected-access
+        == "/mybucket/myobject"
+    )
     address = "oss://mybucket/myobject"
-    assert BaseOSSFileSystem._strip_protocol(address) == "/mybucket/myobject"
+    assert (
+        BaseOSSFileSystem._strip_protocol(address)  # pylint: disable=protected-access
+        == "/mybucket/myobject"
+    )
```

