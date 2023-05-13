# Comparing `tmp/cdk-codeartifact-1.0.3.tar.gz` & `tmp/cdk-codeartifact-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cdk-codeartifact-1.0.3.tar", last modified: Sat May 13 04:21:27 2023, max compression
+gzip compressed data, was "cdk-codeartifact-1.0.4.tar", last modified: Sat May 13 04:30:29 2023, max compression
```

## Comparing `cdk-codeartifact-1.0.3.tar` & `cdk-codeartifact-1.0.4.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:21:27.337562 cdk-codeartifact-1.0.3/
--rw-r--r--   0 runner    (1001) docker     (123)    11358 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     4190 2023-05-13 04:21:27.337562 cdk-codeartifact-1.0.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3180 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      236 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 04:21:27.337562 cdk-codeartifact-1.0.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1829 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:21:27.333562 cdk-codeartifact-1.0.3/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:21:27.333562 cdk-codeartifact-1.0.3/src/cdk_artifact/
--rw-r--r--   0 runner    (1001) docker     (123)    23356 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/src/cdk_artifact/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:21:27.333562 cdk-codeartifact-1.0.3/src/cdk_artifact/_jsii/
--rw-r--r--   0 runner    (1001) docker     (123)      399 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/src/cdk_artifact/_jsii/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    34119 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/src/cdk_artifact/_jsii/cdk-codeartifact@1.0.3.jsii.tgz
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 04:21:09.000000 cdk-codeartifact-1.0.3/src/cdk_artifact/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:21:27.337562 cdk-codeartifact-1.0.3/src/cdk_codeartifact.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4190 2023-05-13 04:21:26.000000 cdk-codeartifact-1.0.3/src/cdk_codeartifact.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      417 2023-05-13 04:21:27.000000 cdk-codeartifact-1.0.3/src/cdk_codeartifact.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 04:21:26.000000 cdk-codeartifact-1.0.3/src/cdk_codeartifact.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 04:21:27.000000 cdk-codeartifact-1.0.3/src/cdk_codeartifact.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 04:21:27.000000 cdk-codeartifact-1.0.3/src/cdk_codeartifact.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:30:29.483663 cdk-codeartifact-1.0.4/
+-rw-r--r--   0 runner    (1001) docker     (123)    11358 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     4190 2023-05-13 04:30:29.479663 cdk-codeartifact-1.0.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3180 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      236 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 04:30:29.483663 cdk-codeartifact-1.0.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1829 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:30:29.479663 cdk-codeartifact-1.0.4/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:30:29.479663 cdk-codeartifact-1.0.4/src/cdk_artifact/
+-rw-r--r--   0 runner    (1001) docker     (123)    23356 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/src/cdk_artifact/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:30:29.479663 cdk-codeartifact-1.0.4/src/cdk_artifact/_jsii/
+-rw-r--r--   0 runner    (1001) docker     (123)      399 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/src/cdk_artifact/_jsii/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    34118 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/src/cdk_artifact/_jsii/cdk-codeartifact@1.0.4.jsii.tgz
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 04:30:16.000000 cdk-codeartifact-1.0.4/src/cdk_artifact/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:30:29.479663 cdk-codeartifact-1.0.4/src/cdk_codeartifact.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4190 2023-05-13 04:30:28.000000 cdk-codeartifact-1.0.4/src/cdk_codeartifact.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      417 2023-05-13 04:30:29.000000 cdk-codeartifact-1.0.4/src/cdk_codeartifact.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 04:30:29.000000 cdk-codeartifact-1.0.4/src/cdk_codeartifact.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 04:30:29.000000 cdk-codeartifact-1.0.4/src/cdk_codeartifact.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 04:30:29.000000 cdk-codeartifact-1.0.4/src/cdk_codeartifact.egg-info/top_level.txt
```

### Comparing `cdk-codeartifact-1.0.3/LICENSE` & `cdk-codeartifact-1.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `cdk-codeartifact-1.0.3/PKG-INFO` & `cdk-codeartifact-1.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cdk-codeartifact
-Version: 1.0.3
+Version: 1.0.4
 Summary: This is an AWS CDK Construct to create a new AWS Codeartifact Domain and one or more Repositories
 Home-page: https://github.com/walmsles/cdk-codeartifact
 Author: Michael Walmsley (@walmsles)<2704782+walmsles@users.noreply.github.com>
 License: Apache-2.0
 Project-URL: Source, https://github.com/walmsles/cdk-codeartifact
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
```

### Comparing `cdk-codeartifact-1.0.3/README.md` & `cdk-codeartifact-1.0.4/README.md`

 * *Files identical despite different names*

### Comparing `cdk-codeartifact-1.0.3/setup.py` & `cdk-codeartifact-1.0.4/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import json
 import setuptools
 
 kwargs = json.loads(
     """
 {
     "name": "cdk-codeartifact",
-    "version": "1.0.3",
+    "version": "1.0.4",
     "description": "This is an AWS CDK Construct to create a new AWS Codeartifact Domain and one or more Repositories",
     "license": "Apache-2.0",
     "url": "https://github.com/walmsles/cdk-codeartifact",
     "long_description_content_type": "text/markdown",
     "author": "Michael Walmsley (@walmsles)<2704782+walmsles@users.noreply.github.com>",
     "bdist_wheel": {
         "universal": true
@@ -22,15 +22,15 @@
     },
     "packages": [
         "cdk_artifact",
         "cdk_artifact._jsii"
     ],
     "package_data": {
         "cdk_artifact._jsii": [
-            "cdk-codeartifact@1.0.3.jsii.tgz"
+            "cdk-codeartifact@1.0.4.jsii.tgz"
         ],
         "cdk_artifact": [
             "py.typed"
         ]
     },
     "python_requires": "~=3.7",
     "install_requires": [
```

### Comparing `cdk-codeartifact-1.0.3/src/cdk_artifact/__init__.py` & `cdk-codeartifact-1.0.4/src/cdk_artifact/__init__.py`

 * *Files identical despite different names*

### Comparing `cdk-codeartifact-1.0.3/src/cdk_codeartifact.egg-info/PKG-INFO` & `cdk-codeartifact-1.0.4/src/cdk_codeartifact.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cdk-codeartifact
-Version: 1.0.3
+Version: 1.0.4
 Summary: This is an AWS CDK Construct to create a new AWS Codeartifact Domain and one or more Repositories
 Home-page: https://github.com/walmsles/cdk-codeartifact
 Author: Michael Walmsley (@walmsles)<2704782+walmsles@users.noreply.github.com>
 License: Apache-2.0
 Project-URL: Source, https://github.com/walmsles/cdk-codeartifact
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
```

