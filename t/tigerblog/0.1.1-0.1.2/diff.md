# Comparing `tmp/tigerblog-0.1.1.tar.gz` & `tmp/tigerblog-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tigerblog-0.1.1.tar", last modified: Sat May 13 20:35:44 2023, max compression
+gzip compressed data, was "tigerblog-0.1.2.tar", last modified: Sat May 13 20:43:26 2023, max compression
```

## Comparing `tigerblog-0.1.1.tar` & `tigerblog-0.1.2.tar`

### file list

```diff
@@ -1,17 +1,19 @@
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:35:44.849872 tigerblog-0.1.1/
--rw-r--r--   0 user      (1000) user      (1000)    11358 2023-05-13 19:28:39.000000 tigerblog-0.1.1/LICENSE.txt
--rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:35:44.849872 tigerblog-0.1.1/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1000)      358 2023-05-13 19:37:09.000000 tigerblog-0.1.1/README.md
--rw-r--r--   0 user      (1000) user      (1000)      344 2023-05-13 20:35:44.850873 tigerblog-0.1.1/setup.cfg
--rw-r--r--   0 user      (1000) user      (1000)      955 2023-05-13 20:35:35.000000 tigerblog-0.1.1/setup.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:35:44.848873 tigerblog-0.1.1/tigerblog/
--rw-r--r--   0 user      (1000) user      (1000)      163 2023-05-13 19:36:22.000000 tigerblog-0.1.1/tigerblog/config.json
--rwxr-xr-x   0 user      (1000) user      (1000)    11914 2023-05-13 20:35:17.000000 tigerblog-0.1.1/tigerblog/tigerblog.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:35:44.849872 tigerblog-0.1.1/tigerblog.egg-info/
--rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1000)      313 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1000)       54 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/entry_points.txt
--rw-r--r--   0 user      (1000) user      (1000)      108 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1000)       10 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:05:19.000000 tigerblog-0.1.1/tigerblog.egg-info/zip-safe
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:43:26.974154 tigerblog-0.1.2/
+-rw-r--r--   0 user      (1000) user      (1000)    11358 2023-05-13 19:28:39.000000 tigerblog-0.1.2/LICENSE.txt
+-rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:43:26.974154 tigerblog-0.1.2/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1000)      358 2023-05-13 19:37:09.000000 tigerblog-0.1.2/README.md
+-rw-r--r--   0 user      (1000) user      (1000)      344 2023-05-13 20:43:26.975154 tigerblog-0.1.2/setup.cfg
+-rw-r--r--   0 user      (1000) user      (1000)      981 2023-05-13 20:43:20.000000 tigerblog-0.1.2/setup.py
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:43:26.964154 tigerblog-0.1.2/tigerblog/
+-rw-r--r--   0 user      (1000) user      (1000)      163 2023-05-13 19:36:22.000000 tigerblog-0.1.2/tigerblog/config.json
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:43:26.974154 tigerblog-0.1.2/tigerblog/themes/
+-rw-r--r--   0 user      (1000) user      (1000)      163 2023-05-13 19:46:59.000000 tigerblog-0.1.2/tigerblog/themes/config.json
+-rwxr-xr-x   0 user      (1000) user      (1000)    11633 2023-05-13 20:41:31.000000 tigerblog-0.1.2/tigerblog/tigerblog.py
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:43:26.974154 tigerblog-0.1.2/tigerblog.egg-info/
+-rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1000)      342 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/SOURCES.txt
+-rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/dependency_links.txt
+-rw-r--r--   0 user      (1000) user      (1000)       54 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/entry_points.txt
+-rw-r--r--   0 user      (1000) user      (1000)      108 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/requires.txt
+-rw-r--r--   0 user      (1000) user      (1000)       10 2023-05-13 20:43:26.000000 tigerblog-0.1.2/tigerblog.egg-info/top_level.txt
+-rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:05:19.000000 tigerblog-0.1.2/tigerblog.egg-info/zip-safe
```

### Comparing `tigerblog-0.1.1/LICENSE.txt` & `tigerblog-0.1.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `tigerblog-0.1.1/PKG-INFO` & `tigerblog-0.1.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tigerblog
-Version: 0.1.1
+Version: 0.1.2
 Summary: Simplest Blog Engine for Developers
 Home-page: https://github.com/tigerteamx/tigerblog
 Author: Martin F
 Author-email: pypi.org@tigerteamx.com
 Keywords: blog,productivity,bottlepy,peewee
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `tigerblog-0.1.1/setup.py` & `tigerblog-0.1.2/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,18 +3,19 @@
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 
 setuptools.setup(
     name="tigerblog",
     packages=["tigerblog"],
+    # package_dir=["themes/"],
     package_data={
-        'tigerblog': ['config.json', "themes/*.html"]
+        'tigerblog': ['config.json', "themes/*"]
     },
-    version="0.1.1",
+    version="0.1.2",
     author="Martin F",
     author_email="pypi.org@tigerteamx.com",
     description="Simplest Blog Engine for Developers",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/tigerteamx/tigerblog",
     install_requires=[],  # Used for dependencies
```

### Comparing `tigerblog-0.1.1/tigerblog/tigerblog.py` & `tigerblog-0.1.2/tigerblog/tigerblog.py`

 * *Files 2% similar despite different names*

```diff
@@ -113,39 +113,30 @@
             'markdown.extensions.toc',
         ],
     )
 
 
 class Blog:
     def __init__(self, config, markdown=markdown):
-        # Sane Defaults
-        self.config = dict(
-            content_path='content',
-            tmp='tmp',
-            output='dist/blog',
-            host='http://localhost:8000/blog',
-            theme=f'beautiful-tiger',
-        )
+        self.config = config
         self.markdown = markdown
-        # Update our defaults with config
-        self.config.update(config)
         if not Path(self.config['theme']).is_dir() and not Path(f"{LIB_DIR}/{self.config['theme']}"):
             raise Exception("Could not find theme directory")
         elif Path(self.config['theme']).is_dir():
             # Precedence to local folder
             pass
         elif Path(f"{LIB_DIR}/{self.config['theme']}"):
             self.config['theme'] = f"{LIB_DIR}/{self.config['theme']}"
 
         self.sidebar = ""
         self.intro = ""
 
         self.tags = []
         self.env = Environment(
-            loader=FileSystemLoader(["templates/", config['theme']]),
+            loader=FileSystemLoader(["templates/", self.config['theme']]),
             autoescape=select_autoescape(),
         )
 
         self.files = [
             os.path.join(dp, f)
             for dp, dn, filenames in os.walk(self.config['content_path'])
             for f in filenames]
```

### Comparing `tigerblog-0.1.1/tigerblog.egg-info/PKG-INFO` & `tigerblog-0.1.2/tigerblog.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tigerblog
-Version: 0.1.1
+Version: 0.1.2
 Summary: Simplest Blog Engine for Developers
 Home-page: https://github.com/tigerteamx/tigerblog
 Author: Martin F
 Author-email: pypi.org@tigerteamx.com
 Keywords: blog,productivity,bottlepy,peewee
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

