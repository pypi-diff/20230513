# Comparing `tmp/rmmbr-0.0.5.tar.gz` & `tmp/rmmbr-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rmmbr-0.0.5.tar", last modified: Fri May 12 11:53:26 2023, max compression
+gzip compressed data, was "rmmbr-0.0.6.tar", last modified: Sat May 13 10:06:32 2023, max compression
```

## Comparing `rmmbr-0.0.5.tar` & `rmmbr-0.0.6.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:53:26.492429 rmmbr-0.0.5/
--rw-r--r--   0 runner    (1001) docker     (123)     1998 2023-05-12 11:53:26.492429 rmmbr-0.0.5/PKG-INFO
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:53:26.492429 rmmbr-0.0.5/rmmbr/
--rw-r--r--   0 runner    (1001) docker     (123)      109 2023-05-12 11:53:17.000000 rmmbr-0.0.5/rmmbr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      562 2023-05-12 11:53:17.000000 rmmbr-0.0.5/rmmbr/crypto.py
--rw-r--r--   0 runner    (1001) docker     (123)     5071 2023-05-12 11:53:17.000000 rmmbr-0.0.5/rmmbr/main.py
--rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-05-12 11:53:17.000000 rmmbr-0.0.5/rmmbr/main_test.py
--rw-r--r--   0 runner    (1001) docker     (123)      497 2023-05-12 11:53:17.000000 rmmbr-0.0.5/rmmbr/serialization.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 11:53:26.492429 rmmbr-0.0.5/rmmbr.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1998 2023-05-12 11:53:26.000000 rmmbr-0.0.5/rmmbr.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      274 2023-05-12 11:53:26.000000 rmmbr-0.0.5/rmmbr.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 11:53:26.000000 rmmbr-0.0.5/rmmbr.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-05-12 11:53:26.000000 rmmbr-0.0.5/rmmbr.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       93 2023-05-12 11:53:26.000000 rmmbr-0.0.5/rmmbr.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-12 11:53:26.000000 rmmbr-0.0.5/rmmbr.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 11:53:26.492429 rmmbr-0.0.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      858 2023-05-12 11:53:17.000000 rmmbr-0.0.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 10:06:32.616151 rmmbr-0.0.6/
+-rw-r--r--   0 runner    (1001) docker     (123)     2132 2023-05-13 10:06:32.616151 rmmbr-0.0.6/PKG-INFO
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 10:06:32.616151 rmmbr-0.0.6/rmmbr/
+-rw-r--r--   0 runner    (1001) docker     (123)      109 2023-05-13 10:06:18.000000 rmmbr-0.0.6/rmmbr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      562 2023-05-13 10:06:18.000000 rmmbr-0.0.6/rmmbr/crypto.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5071 2023-05-13 10:06:18.000000 rmmbr-0.0.6/rmmbr/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-05-13 10:06:18.000000 rmmbr-0.0.6/rmmbr/main_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)      443 2023-05-13 10:06:18.000000 rmmbr-0.0.6/rmmbr/serialization.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 10:06:32.616151 rmmbr-0.0.6/rmmbr.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2132 2023-05-13 10:06:32.000000 rmmbr-0.0.6/rmmbr.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      274 2023-05-13 10:06:32.000000 rmmbr-0.0.6/rmmbr.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 10:06:32.000000 rmmbr-0.0.6/rmmbr.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-05-13 10:06:32.000000 rmmbr-0.0.6/rmmbr.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-05-13 10:06:32.000000 rmmbr-0.0.6/rmmbr.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-13 10:06:32.000000 rmmbr-0.0.6/rmmbr.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 10:06:32.616151 rmmbr-0.0.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      858 2023-05-13 10:06:18.000000 rmmbr-0.0.6/setup.py
```

### Comparing `rmmbr-0.0.5/PKG-INFO` & `rmmbr-0.0.6/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,20 +1,24 @@
 Metadata-Version: 2.1
 Name: rmmbr
-Version: 0.0.5
+Version: 0.0.6
 Summary: Simple persistent caching.
 Home-page: https://github.com/uriva/rmmbr
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
 
+# rmmbr
+
+![rmmbr](https://media.tenor.com/NcnMXggTODAAAAAC/yeah-i-member-memberberries.gif)
+
 `rmmbr` is the simplest way to cache your async functions, locally or in the cloud.
 
-Usage:
+## Usage
 
 ```sh
 npm i rmmbr
 ```
 
 ```js
 import { cloudCache, localCache } from "rmmbr";
@@ -32,38 +36,42 @@
 // nCalled is 1 here
 ```
 
 The local cache stores data in a text file under a `.rmmbr` directory.
 
 There is also a `memCache`, if you are feeling nostalgic 😉 and just want to store stuff in memory.
 
+## Cross device caching
+
 To persist the cache across devices, we offer a use cloud service, which is free to use up to a quota.
 
 To use it, you can install the CLI tool:
 
 `source <(curl -s https://raw.githubusercontent.com/uriva/rmmbr/main/cli/install.sh)`
 
 Then
 
 ```sh
 rmmbr login
 rmmbr api-token
 ```
 
-You can then use your token with the API as follows:
+Use your token with the API as follows:
 
 ```js
 const cacher = cloudCache({
   token: "service-token",
   cacheId: "some name for the cache",
   url: "https://uriva-rmmbr.deno.dev",
   ttl: 60 * 60 * 24, // Values will expire after one day, omission of this field implies max.
 });
 ```
 
+### End to end encryption
+
 If your data is sensitive, you can e2e encrypt it by adding an `encryptionKey` parameter.
 
 To produce an encryption key:
 
 ```sh
 rmmbr secret
 ```
```

### Comparing `rmmbr-0.0.5/rmmbr/crypto.py` & `rmmbr-0.0.6/rmmbr/crypto.py`

 * *Files identical despite different names*

### Comparing `rmmbr-0.0.5/rmmbr/main.py` & `rmmbr-0.0.6/rmmbr/main.py`

 * *Files identical despite different names*

### Comparing `rmmbr-0.0.5/rmmbr/main_test.py` & `rmmbr-0.0.6/rmmbr/main_test.py`

 * *Files identical despite different names*

### Comparing `rmmbr-0.0.5/rmmbr.egg-info/PKG-INFO` & `rmmbr-0.0.6/rmmbr.egg-info/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,20 +1,24 @@
 Metadata-Version: 2.1
 Name: rmmbr
-Version: 0.0.5
+Version: 0.0.6
 Summary: Simple persistent caching.
 Home-page: https://github.com/uriva/rmmbr
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
 
+# rmmbr
+
+![rmmbr](https://media.tenor.com/NcnMXggTODAAAAAC/yeah-i-member-memberberries.gif)
+
 `rmmbr` is the simplest way to cache your async functions, locally or in the cloud.
 
-Usage:
+## Usage
 
 ```sh
 npm i rmmbr
 ```
 
 ```js
 import { cloudCache, localCache } from "rmmbr";
@@ -32,38 +36,42 @@
 // nCalled is 1 here
 ```
 
 The local cache stores data in a text file under a `.rmmbr` directory.
 
 There is also a `memCache`, if you are feeling nostalgic 😉 and just want to store stuff in memory.
 
+## Cross device caching
+
 To persist the cache across devices, we offer a use cloud service, which is free to use up to a quota.
 
 To use it, you can install the CLI tool:
 
 `source <(curl -s https://raw.githubusercontent.com/uriva/rmmbr/main/cli/install.sh)`
 
 Then
 
 ```sh
 rmmbr login
 rmmbr api-token
 ```
 
-You can then use your token with the API as follows:
+Use your token with the API as follows:
 
 ```js
 const cacher = cloudCache({
   token: "service-token",
   cacheId: "some name for the cache",
   url: "https://uriva-rmmbr.deno.dev",
   ttl: 60 * 60 * 24, // Values will expire after one day, omission of this field implies max.
 });
 ```
 
+### End to end encryption
+
 If your data is sensitive, you can e2e encrypt it by adding an `encryptionKey` parameter.
 
 To produce an encryption key:
 
 ```sh
 rmmbr secret
 ```
```

### Comparing `rmmbr-0.0.5/setup.py` & `rmmbr-0.0.6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 from setuptools import find_packages, setup
 
 _repo_dir = os.environ.get("GITHUB_WORKSPACE")
 assert _repo_dir
 setup(
     name="rmmbr",
-    version="0.0.5",
+    version="0.0.6",
     description="Simple persistent caching.",
     long_description=(pathlib.Path(_repo_dir) / "README.md").read_text(),
     long_description_content_type="text/markdown",
     url="https://github.com/uriva/rmmbr",
     packages=find_packages(),
     install_requires=[
         "redis>=3.5.3",
```

