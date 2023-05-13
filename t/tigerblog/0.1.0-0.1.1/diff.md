# Comparing `tmp/tigerblog-0.1.0.tar.gz` & `tmp/tigerblog-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tigerblog-0.1.0.tar", last modified: Sat May 13 20:05:19 2023, max compression
+gzip compressed data, was "tigerblog-0.1.1.tar", last modified: Sat May 13 20:35:44 2023, max compression
```

## Comparing `tigerblog-0.1.0.tar` & `tigerblog-0.1.1.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:05:19.235781 tigerblog-0.1.0/
--rw-r--r--   0 user      (1000) user      (1000)    11358 2023-05-13 19:28:39.000000 tigerblog-0.1.0/LICENSE.txt
--rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:05:19.235781 tigerblog-0.1.0/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1000)      358 2023-05-13 19:37:09.000000 tigerblog-0.1.0/README.md
--rw-r--r--   0 user      (1000) user      (1000)      344 2023-05-13 20:05:19.235781 tigerblog-0.1.0/setup.cfg
--rw-r--r--   0 user      (1000) user      (1000)      955 2023-05-13 20:04:43.000000 tigerblog-0.1.0/setup.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:05:19.234781 tigerblog-0.1.0/tigerblog/
--rw-r--r--   0 user      (1000) user      (1000)      163 2023-05-13 19:36:22.000000 tigerblog-0.1.0/tigerblog/config.json
--rwxr-xr-x   0 user      (1000) user      (1000)    11488 2023-05-13 19:46:03.000000 tigerblog-0.1.0/tigerblog/tigerblog.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:05:19.235781 tigerblog-0.1.0/tigerblog.egg-info/
--rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:05:19.000000 tigerblog-0.1.0/tigerblog.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1000)      313 2023-05-13 20:05:19.000000 tigerblog-0.1.0/tigerblog.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:05:19.000000 tigerblog-0.1.0/tigerblog.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1000)       54 2023-05-13 20:05:19.000000 tigerblog-0.1.0/tigerblog.egg-info/entry_points.txt
--rw-r--r--   0 user      (1000) user      (1000)      108 2023-05-13 20:05:19.000000 tigerblog-0.1.0/tigerblog.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1000)       10 2023-05-13 20:05:19.000000 tigerblog-0.1.0/tigerblog.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:05:19.000000 tigerblog-0.1.0/tigerblog.egg-info/zip-safe
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:35:44.849872 tigerblog-0.1.1/
+-rw-r--r--   0 user      (1000) user      (1000)    11358 2023-05-13 19:28:39.000000 tigerblog-0.1.1/LICENSE.txt
+-rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:35:44.849872 tigerblog-0.1.1/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1000)      358 2023-05-13 19:37:09.000000 tigerblog-0.1.1/README.md
+-rw-r--r--   0 user      (1000) user      (1000)      344 2023-05-13 20:35:44.850873 tigerblog-0.1.1/setup.cfg
+-rw-r--r--   0 user      (1000) user      (1000)      955 2023-05-13 20:35:35.000000 tigerblog-0.1.1/setup.py
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:35:44.848873 tigerblog-0.1.1/tigerblog/
+-rw-r--r--   0 user      (1000) user      (1000)      163 2023-05-13 19:36:22.000000 tigerblog-0.1.1/tigerblog/config.json
+-rwxr-xr-x   0 user      (1000) user      (1000)    11914 2023-05-13 20:35:17.000000 tigerblog-0.1.1/tigerblog/tigerblog.py
+drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 20:35:44.849872 tigerblog-0.1.1/tigerblog.egg-info/
+-rw-r--r--   0 user      (1000) user      (1000)      842 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1000)      313 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/SOURCES.txt
+-rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/dependency_links.txt
+-rw-r--r--   0 user      (1000) user      (1000)       54 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/entry_points.txt
+-rw-r--r--   0 user      (1000) user      (1000)      108 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/requires.txt
+-rw-r--r--   0 user      (1000) user      (1000)       10 2023-05-13 20:35:44.000000 tigerblog-0.1.1/tigerblog.egg-info/top_level.txt
+-rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 20:05:19.000000 tigerblog-0.1.1/tigerblog.egg-info/zip-safe
```

### Comparing `tigerblog-0.1.0/LICENSE.txt` & `tigerblog-0.1.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `tigerblog-0.1.0/PKG-INFO` & `tigerblog-0.1.1/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tigerblog
-Version: 0.1.0
+Version: 0.1.1
 Summary: Simplest Blog Engine for Developers
 Home-page: https://github.com/tigerteamx/tigerblog
 Author: Martin F
 Author-email: pypi.org@tigerteamx.com
 Keywords: blog,productivity,bottlepy,peewee
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `tigerblog-0.1.0/setup.py` & `tigerblog-0.1.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 
 setuptools.setup(
     name="tigerblog",
     packages=["tigerblog"],
     package_data={
         'tigerblog': ['config.json', "themes/*.html"]
     },
-    version="0.1.0",
+    version="0.1.1",
     author="Martin F",
     author_email="pypi.org@tigerteamx.com",
     description="Simplest Blog Engine for Developers",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/tigerteamx/tigerblog",
     install_requires=[],  # Used for dependencies
```

### Comparing `tigerblog-0.1.0/tigerblog/tigerblog.py` & `tigerblog-0.1.1/tigerblog/tigerblog.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python3
 
 from pprint import pprint
 from datetime import date, datetime
 from os import system
-import pathlib
+from pathlib import Path
 import shutil
 import json
 from typing import List, Optional
 import os
 from dataclasses import dataclass
 from traceback import format_exc
 from typing_extensions import Self
@@ -16,14 +16,17 @@
 from frontmatter import load
 from markdown import markdown as _markdown
 from slugify import slugify
 from jinja2 import Environment, FileSystemLoader, select_autoescape, BaseLoader
 from docopt import docopt
 
 
+LIB_DIR = os.path.split(__file__)[0]
+
+
 @dataclass
 class Tag:
     title: str
     slug: str
     url: str
 
     def __hash__(self):
@@ -47,19 +50,19 @@
     related: List[Self]
 
     def __hash__(self):
         return hash((self.title, self.dst, self.url))
 
 
 def mkdir(path):
-    return pathlib.Path(path).mkdir(parents=True, exist_ok=True)
+    return Path(path).mkdir(parents=True, exist_ok=True)
 
 
 def mkdir_parent(path):
-    return pathlib.Path(path).parent.mkdir(parents=True, exist_ok=True)
+    return Path(path).parent.mkdir(parents=True, exist_ok=True)
 
 
 def read(path):
     with open(path, 'r') as f:
         return f.read()
 
 
@@ -72,15 +75,14 @@
     defaults = dict(
         title="",
         description="",
         date="2023-02-23",
         draft=False,
         tags=[],
         body="",
-        theme="themes/beautiful-tiger",
     )
     data = load(path)
     if data.content:
         data['body'] = data.content
     defaults.update(data)
     defaults['date'] = datetime.strptime(defaults['date'], "%Y-%m-%d")
     return defaults
@@ -117,18 +119,27 @@
     def __init__(self, config, markdown=markdown):
         # Sane Defaults
         self.config = dict(
             content_path='content',
             tmp='tmp',
             output='dist/blog',
             host='http://localhost:8000/blog',
+            theme=f'beautiful-tiger',
         )
         self.markdown = markdown
         # Update our defaults with config
         self.config.update(config)
+        if not Path(self.config['theme']).is_dir() and not Path(f"{LIB_DIR}/{self.config['theme']}"):
+            raise Exception("Could not find theme directory")
+        elif Path(self.config['theme']).is_dir():
+            # Precedence to local folder
+            pass
+        elif Path(f"{LIB_DIR}/{self.config['theme']}"):
+            self.config['theme'] = f"{LIB_DIR}/{self.config['theme']}"
+
         self.sidebar = ""
         self.intro = ""
 
         self.tags = []
         self.env = Environment(
             loader=FileSystemLoader(["templates/", config['theme']]),
             autoescape=select_autoescape(),
@@ -318,32 +329,32 @@
             f"{blog.config['tmp']}/{tag.slug}/index.html",
             blog.get_pages_with_tag(tag),
             tag,
             f'{blog.config["host"]}/{tag.slug}/',
         )
     blog.copy_files()
 
-    if pathlib.Path(f'{blog.config["theme"]}/static').is_dir():
+    if Path(f'{blog.config["theme"]}/static').is_dir():
         shutil.copytree(f'{blog.config["theme"]}/static', f"{blog.config['tmp']}/static")
 
-    if pathlib.Path('static').is_dir():
+    if Path('static').is_dir():
         merge_two_folders('static', f"{blog.config['tmp']}/static")
 
     shutil.rmtree(blog.config['output'], ignore_errors=True, onerror=None)
     shutil.copytree(blog.config['tmp'] + "/", blog.config['output'])
 
 
 def build(config):
     try:
         # This is the default way of calling the blog engine
         # but you can make your own custom way
         if config:
             c = json.loads(read(config))
         else:
-            c = json.loads(read("config.json"))
+            c = json.loads(read(f"{LIB_DIR}/config.json"))
 
         main(c)
 
         print("Ok")
     except: # noqa
         print("Error happened when compiling")
         print(format_exc())
```

### Comparing `tigerblog-0.1.0/tigerblog.egg-info/PKG-INFO` & `tigerblog-0.1.1/tigerblog.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tigerblog
-Version: 0.1.0
+Version: 0.1.1
 Summary: Simplest Blog Engine for Developers
 Home-page: https://github.com/tigerteamx/tigerblog
 Author: Martin F
 Author-email: pypi.org@tigerteamx.com
 Keywords: blog,productivity,bottlepy,peewee
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

