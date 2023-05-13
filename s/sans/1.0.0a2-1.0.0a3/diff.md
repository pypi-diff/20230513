# Comparing `tmp/sans-1.0.0a2.tar.gz` & `tmp/sans-1.0.0a3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sans-1.0.0a2.tar", last modified: Tue May  9 04:44:04 2023, max compression
+gzip compressed data, was "sans-1.0.0a3.tar", last modified: Sat May 13 02:22:57 2023, max compression
```

## Comparing `sans-1.0.0a2.tar` & `sans-1.0.0a3.tar`

### file list

```diff
@@ -1,46 +1,49 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 04:44:04.554112 sans-1.0.0a2/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 04:44:04.550111 sans-1.0.0a2/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 04:44:04.550111 sans-1.0.0a2/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-05-09 04:43:52.000000 sans-1.0.0a2/.github/workflows/codeql-analysis.yml
--rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-09 04:43:52.000000 sans-1.0.0a2/.github/workflows/pythonpublish.yml
--rw-r--r--   0 runner    (1001) docker     (123)     3101 2023-05-09 04:43:52.000000 sans-1.0.0a2/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1126 2023-05-09 04:43:52.000000 sans-1.0.0a2/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-09 04:43:52.000000 sans-1.0.0a2/.readthedocs.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-09 04:43:52.000000 sans-1.0.0a2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5253 2023-05-09 04:44:04.554112 sans-1.0.0a2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2751 2023-05-09 04:43:52.000000 sans-1.0.0a2/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 04:44:04.550111 sans-1.0.0a2/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      581 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/__init__.rst
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/api.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6097 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/errors.rst
--rw-r--r--   0 runner    (1001) docker     (123)      209 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/objects.rst
--rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-09 04:43:52.000000 sans-1.0.0a2/docs/utils.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2326 2023-05-09 04:43:52.000000 sans-1.0.0a2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      190 2023-05-09 04:43:52.000000 sans-1.0.0a2/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 04:44:04.554112 sans-1.0.0a2/sans/
--rw-r--r--   0 runner    (1001) docker     (123)     1953 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3437 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)      785 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/_state.py
--rw-r--r--   0 runner    (1001) docker     (123)     1544 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/client.py
--rw-r--r--   0 runner    (1001) docker     (123)    23030 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/client.pyi
--rw-r--r--   0 runner    (1001) docker     (123)     3145 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/decoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     2278 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/errors.py
--rw-r--r--   0 runner    (1001) docker     (123)     2117 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/limiter.py
--rw-r--r--   0 runner    (1001) docker     (123)     5646 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/lock.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)     2410 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3114 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2552 2023-05-09 04:43:52.000000 sans-1.0.0a2/sans/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 04:44:04.554112 sans-1.0.0a2/sans.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5253 2023-05-09 04:44:04.000000 sans-1.0.0a2/sans.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      691 2023-05-09 04:44:04.000000 sans-1.0.0a2/sans.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-09 04:44:04.000000 sans-1.0.0a2/sans.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-09 04:44:04.000000 sans-1.0.0a2/sans.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      153 2023-05-09 04:44:04.000000 sans-1.0.0a2/sans.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-09 04:44:04.000000 sans-1.0.0a2/sans.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-09 04:44:04.554112 sans-1.0.0a2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-09 04:43:52.000000 sans-1.0.0a2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.493552 sans-1.0.0a3/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.489552 sans-1.0.0a3/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.489552 sans-1.0.0a3/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-05-13 02:22:45.000000 sans-1.0.0a3/.github/workflows/codeql-analysis.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-13 02:22:45.000000 sans-1.0.0a3/.github/workflows/pythonpublish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     3101 2023-05-13 02:22:45.000000 sans-1.0.0a3/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1263 2023-05-13 02:22:45.000000 sans-1.0.0a3/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 02:22:45.000000 sans-1.0.0a3/.readthedocs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-13 02:22:45.000000 sans-1.0.0a3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5831 2023-05-13 02:22:57.493552 sans-1.0.0a3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3329 2023-05-13 02:22:45.000000 sans-1.0.0a3/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.489552 sans-1.0.0a3/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      581 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/auth.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6127 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      100 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/errors.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      237 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      115 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/limiter.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       94 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/lock.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)      106 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/response.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/url.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-05-13 02:22:45.000000 sans-1.0.0a3/docs/utils.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2236 2023-05-13 02:22:45.000000 sans-1.0.0a3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      239 2023-05-13 02:22:45.000000 sans-1.0.0a3/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.493552 sans-1.0.0a3/sans/
+-rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      803 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/_state.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/auth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1310 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29355 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/client.pyi
+-rw-r--r--   0 runner    (1001) docker     (123)     4276 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/decoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6689 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/limiter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5056 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/lock.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     4163 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2310 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/url.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3213 2023-05-13 02:22:45.000000 sans-1.0.0a3/sans/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:22:57.493552 sans-1.0.0a3/sans.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5831 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      728 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      135 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 02:22:57.000000 sans-1.0.0a3/sans.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 02:22:57.493552 sans-1.0.0a3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 02:22:45.000000 sans-1.0.0a3/setup.py
```

### Comparing `sans-1.0.0a2/.github/workflows/codeql-analysis.yml` & `sans-1.0.0a3/.github/workflows/codeql-analysis.yml`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a2/.github/workflows/pythonpublish.yml` & `sans-1.0.0a3/.github/workflows/pythonpublish.yml`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a2/.gitignore` & `sans-1.0.0a3/.gitignore`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a2/.pre-commit-config.yaml` & `sans-1.0.0a3/.pre-commit-config.yaml`

 * *Files 26% similar despite different names*

```diff
@@ -11,18 +11,14 @@
     -   id: check-yaml
     -   id: check-added-large-files
 -   repo: https://github.com/charliermarsh/ruff-pre-commit
     rev: v0.0.265
     hooks:
     -   id: ruff
         args: [ --fix, --exit-non-zero-on-fix ]
--   repo: https://github.com/PyCQA/isort
-    rev: 5.11.5
-    hooks:
-    -   id: isort
 -   repo: https://github.com/psf/black
     rev: 23.3.0
     hooks:
     -   id: black
 -   repo: https://github.com/RobertCraigie/pyright-python
     rev: v1.1.306
     hooks:
@@ -31,11 +27,18 @@
             # required dependencies
         -   httpx ~= 0.21.1
         -   importlib_metadata >= 1.4.0; python_version < "3.8"
 
             # optional dependencies
             # [lxml]
         -   lxml ~= 4.9.2
-        -   lxml-stubs ~= 0.4.0
 
             # [json]
         -   xmltodict ~= 0.13.0
+
+            # typing
+        -   typing_extensions
+        -   lxml-stubs @ https://github.com/lxml/lxml-stubs/archive/master.zip#egg=lxml-stubs
+ci:
+    skip:
+    # CI doesn't like pip scripts calling their own node, so skip this for now
+    -   pyright
```

### Comparing `sans-1.0.0a2/LICENSE` & `sans-1.0.0a3/LICENSE`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a2/PKG-INFO` & `sans-1.0.0a3/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sans
-Version: 1.0.0a2
+Version: 1.0.0a3
 Summary: Synchronous / Asynchronous HTTPX extension for NationStates
 Author: Zephyrkul
 License: MIT License
         
         Copyright (c) 2018 - 2023
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -66,108 +66,122 @@
 it is highly recommended to use Dolph's pynationstates
 (`GitHub <https://github.com/DolphDev/pynationstates>`_
 | `PyPI <https://pypi.org/project/nationstates/>`_) for simpler scripts.
 
 Installing
 ----------
 
-::
+.. code::
 
    python3 -m pip install -U sans
 
 Development version:
 
-::
+.. code::
 
    python3 -m pip install -U https://github.com/zephyrkul/sans/archive/master.zip#egg=sans
 
 Examples
 --------
 
+Synchronous
+~~~~~~~~~~~
+
+.. code:: python
+
+   import sans
+   from xml.etree import ElementTree as ET
+
+   def main():
+      sans.set_agent("Darcania")
+      request = sans.Nation(
+         "darcania",
+         "fullname population flag census",
+         mode="score",
+         scale="65 66",
+      )
+      root = sans.get(request)
+      sans.indent(root)
+      print(ET.tostring(root, encoding="unicode"))
+
+      with sans.stream("GET", sans.RegionsDump()) as response:
+         for region in response.iter_xml():
+            sans.indent(region)
+            print(ET.tostring(region, encoding="unicode"))
+
+   if __name__ == "__main__":
+      main()
+
 Asynchronous
 ~~~~~~~~~~~~
 
-.. code:: py
+.. code:: python
 
    import asyncio
    import sans
-   from sans.api import Api, Dumps
-   from sans.utils import pretty_string
+   from xml.etree import ElementTree as ET
 
    async def main():
-       Api.agent = "Darcania"
-       request = Api(
-           "fullname population flag census",
-           nation="darcania",
-           mode="score",
-           scale="65 66",
-       )
-       root = await request
-       pretty = pretty_string(root)
-       print(pretty)
-
-       request = Dumps.REGIONS
-       async for region in request:
-           pretty = pretty_string(region)
-           print(pretty)
-
+      sans.set_agent("Darcania")
+      async with sans.AsyncClient() as client:
+         request = sans.Nation(
+            "darcania",
+            "fullname population flag census",
+            mode="score",
+            scale="65 66",
+         )
+         root = (await client.send(request)).xml
+         sans.indent(root)
+         print(ET.tostring(root, encoding="unicode"))
+
+         async with client.stream("GET", sans.RegionsDump()) as response:
+            async for region in response.aiter_xml():
+               sans.indent(region)
+               print(ET.tostring(region, encoding="unicode"))
 
-   asyncio.run(main())  # Python 3.7+ only
+   if __name__ == "__main__":
+      asyncio.run(main())
 
-Synchronous
-~~~~~~~~~~~
+Command Line
+------------
 
-.. code:: py
+.. code::
 
-   import sans
-   from sans.api import Api, Dumps
+   $ sans --nation darcania census --scale "65 66" --mode score --agent Darcania
 
-   def main():
-       sans.run_in_thread()
-       Api.agent = "Darcania"
-       request = Api(
-           "fullname population flag census",
-           nation="darcania",
-           mode="score",
-           scale="65 66",
-       )
-       root = request.threadsafe()
-       pretty = pretty_string(root)
-       print(pretty)
-
-       request = Dumps.REGIONS
-       for region in request.threadsafe:
-           pretty = pretty_string(region)
-           print(pretty)
+   <CENSUS>
+      <SCALE id="65">
+         <SCORE>4949.00</SCORE>
+      </SCALE>
+      <SCALE id="66">
+         <SCORE>130.00</SCORE>
+      </SCALE>
+   </CENSUS>
 
+   $ sans --nation testlandia fullname
 
-   main()
+   <FULLNAME>The Hive Mind of Testlandia</FULLNAME>
 
-Command Line
-------------
+   sans --region "the north pacific" numnations lastupdate
 
-::
+   <LASTUPDATE>1683650325</LASTUPDATE>
+   <NUMNATIONS>10503</NUMNATIONS>
 
-   python3 -m sans --nation darcania census --scale "65 66" --mode score --agent Darcania
-   <NATION>...</NATION>
-   sans --nation testlandia fullname
-   <NATION>...</NATION>
-   sans --region "the north pacific" numnations lastupdate
-   <REGION>...</REGION>
-   sans --quit
-   Exiting...
+   $ sans --quit
+   No query provided. Exiting...
 
 Requirements
 ------------
 
--  Python 3.6+
--  aiohttp
--  lxml
+-  Python 3.7+
+-  httpx
 
 .. |pypi| image:: https://img.shields.io/pypi/v/sans.svg
    :target: https://pypi.python.org/pypi/sans
+   :alt: pypi version
 .. |Code style: black| image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/ambv/black
-.. |Build Status| image:: https://github.com/zephyrkul/sans/workflows/build/badge.svg
-   :target: https://github.com/zephyrkul/sans/actions?workflow=build
+.. |Build Status| image:: https://results.pre-commit.ci/badge/github/Zephyrkul/sans/master.svg
+   :target: https://results.pre-commit.ci/latest/github/Zephyrkul/sans/master
+   :alt: pre-commit.ci status
 .. |Documentation Status| image:: https://readthedocs.org/projects/sans/badge/?version=latest
    :target: http://sans.readthedocs.org/en/latest/?badge=latest
```

### Comparing `sans-1.0.0a2/README.rst` & `sans-1.0.0a3/README.rst`

 * *Files 21% similar despite different names*

```diff
@@ -12,108 +12,122 @@
 it is highly recommended to use Dolph's pynationstates
 (`GitHub <https://github.com/DolphDev/pynationstates>`_
 | `PyPI <https://pypi.org/project/nationstates/>`_) for simpler scripts.
 
 Installing
 ----------
 
-::
+.. code::
 
    python3 -m pip install -U sans
 
 Development version:
 
-::
+.. code::
 
    python3 -m pip install -U https://github.com/zephyrkul/sans/archive/master.zip#egg=sans
 
 Examples
 --------
 
+Synchronous
+~~~~~~~~~~~
+
+.. code:: python
+
+   import sans
+   from xml.etree import ElementTree as ET
+
+   def main():
+      sans.set_agent("Darcania")
+      request = sans.Nation(
+         "darcania",
+         "fullname population flag census",
+         mode="score",
+         scale="65 66",
+      )
+      root = sans.get(request)
+      sans.indent(root)
+      print(ET.tostring(root, encoding="unicode"))
+
+      with sans.stream("GET", sans.RegionsDump()) as response:
+         for region in response.iter_xml():
+            sans.indent(region)
+            print(ET.tostring(region, encoding="unicode"))
+
+   if __name__ == "__main__":
+      main()
+
 Asynchronous
 ~~~~~~~~~~~~
 
-.. code:: py
+.. code:: python
 
    import asyncio
    import sans
-   from sans.api import Api, Dumps
-   from sans.utils import pretty_string
+   from xml.etree import ElementTree as ET
 
    async def main():
-       Api.agent = "Darcania"
-       request = Api(
-           "fullname population flag census",
-           nation="darcania",
-           mode="score",
-           scale="65 66",
-       )
-       root = await request
-       pretty = pretty_string(root)
-       print(pretty)
-
-       request = Dumps.REGIONS
-       async for region in request:
-           pretty = pretty_string(region)
-           print(pretty)
-
+      sans.set_agent("Darcania")
+      async with sans.AsyncClient() as client:
+         request = sans.Nation(
+            "darcania",
+            "fullname population flag census",
+            mode="score",
+            scale="65 66",
+         )
+         root = (await client.send(request)).xml
+         sans.indent(root)
+         print(ET.tostring(root, encoding="unicode"))
+
+         async with client.stream("GET", sans.RegionsDump()) as response:
+            async for region in response.aiter_xml():
+               sans.indent(region)
+               print(ET.tostring(region, encoding="unicode"))
 
-   asyncio.run(main())  # Python 3.7+ only
+   if __name__ == "__main__":
+      asyncio.run(main())
 
-Synchronous
-~~~~~~~~~~~
+Command Line
+------------
 
-.. code:: py
+.. code::
 
-   import sans
-   from sans.api import Api, Dumps
+   $ sans --nation darcania census --scale "65 66" --mode score --agent Darcania
 
-   def main():
-       sans.run_in_thread()
-       Api.agent = "Darcania"
-       request = Api(
-           "fullname population flag census",
-           nation="darcania",
-           mode="score",
-           scale="65 66",
-       )
-       root = request.threadsafe()
-       pretty = pretty_string(root)
-       print(pretty)
-
-       request = Dumps.REGIONS
-       for region in request.threadsafe:
-           pretty = pretty_string(region)
-           print(pretty)
+   <CENSUS>
+      <SCALE id="65">
+         <SCORE>4949.00</SCORE>
+      </SCALE>
+      <SCALE id="66">
+         <SCORE>130.00</SCORE>
+      </SCALE>
+   </CENSUS>
 
+   $ sans --nation testlandia fullname
 
-   main()
+   <FULLNAME>The Hive Mind of Testlandia</FULLNAME>
 
-Command Line
-------------
+   sans --region "the north pacific" numnations lastupdate
 
-::
+   <LASTUPDATE>1683650325</LASTUPDATE>
+   <NUMNATIONS>10503</NUMNATIONS>
 
-   python3 -m sans --nation darcania census --scale "65 66" --mode score --agent Darcania
-   <NATION>...</NATION>
-   sans --nation testlandia fullname
-   <NATION>...</NATION>
-   sans --region "the north pacific" numnations lastupdate
-   <REGION>...</REGION>
-   sans --quit
-   Exiting...
+   $ sans --quit
+   No query provided. Exiting...
 
 Requirements
 ------------
 
--  Python 3.6+
--  aiohttp
--  lxml
+-  Python 3.7+
+-  httpx
 
 .. |pypi| image:: https://img.shields.io/pypi/v/sans.svg
    :target: https://pypi.python.org/pypi/sans
+   :alt: pypi version
 .. |Code style: black| image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/ambv/black
-.. |Build Status| image:: https://github.com/zephyrkul/sans/workflows/build/badge.svg
-   :target: https://github.com/zephyrkul/sans/actions?workflow=build
+.. |Build Status| image:: https://results.pre-commit.ci/badge/github/Zephyrkul/sans/master.svg
+   :target: https://results.pre-commit.ci/latest/github/Zephyrkul/sans/master
+   :alt: pre-commit.ci status
 .. |Documentation Status| image:: https://readthedocs.org/projects/sans/badge/?version=latest
    :target: http://sans.readthedocs.org/en/latest/?badge=latest
```

### Comparing `sans-1.0.0a2/docs/Makefile` & `sans-1.0.0a3/docs/Makefile`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a2/docs/conf.py` & `sans-1.0.0a3/docs/conf.py`

 * *Files 4% similar despite different names*

```diff
@@ -18,21 +18,21 @@
 sys.path.insert(0, os.path.abspath(".."))
 # autodoc_mock_imports = ["lxml"]
 
 
 # -- Project information -----------------------------------------------------
 
 if sys.version_info < (3, 8):
-    from importlib_metadata import metadata as _metadata
+    from importlib_metadata import metadata as _metadata  # type: ignore
 else:
     from importlib.metadata import metadata as _metadata
 
 project = "sans"
 meta = _metadata(project)
-copyright = meta["Copyright"]
+copyright = "Copyright 2019-2023 Zephyrkul"
 author = meta["Version"]
 
 # The full version, including alpha/beta/rc tags
 release = meta["Version"]
 # The short X.Y version
 version = ".".join(release.split(".")[:2])
 
@@ -72,15 +72,15 @@
 master_doc = "index"
 
 # The language for content autogenerated by Sphinx. Refer to documentation
 # for a list of supported languages.
 #
 # This is also used if you do content translation via gettext catalogs.
 # Usually you set "language" from the command line for these cases.
-language = None
+language = "en"
 
 # List of patterns, relative to source directory, that match files and
 # directories to ignore when looking for source files.
 # This pattern also affects html_static_path and html_extra_path.
 exclude_patterns = ["_build", "Thumbs.db", ".DS_Store"]
 
 # The name of the Pygments (syntax highlighting) style to use.
```

### Comparing `sans-1.0.0a2/docs/make.bat` & `sans-1.0.0a3/docs/make.bat`

 * *Files identical despite different names*

### Comparing `sans-1.0.0a2/pyproject.toml` & `sans-1.0.0a3/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -52,39 +52,36 @@
 sans = 'sans.__main__:main'
 
 [project.optional-dependencies]
 docs = [
     'Sphinx ~= 5.3.0'
 ]
 lxml = [
-    'lxml ~= 4.9.2',
-    'lxml-stubs ~= 0.4.0'
+    'lxml ~= 4.9.2'
 ]
 json = [
     'xmltodict ~= 0.13.0'
 ]
 
 [tool.setuptools_scm]
 
-[tool.isort]
-    profile = 'black'
-    combine_as_imports = true
-    extra_standard_library = ['typing_extensions']
-    treat_comments_as_code = ['# type: ignore']
-
 [tool.black]
     target-version = ['py37']
     include = '\.pyi?$'
 
 [tool.pyright]
     pythonVersion = '3.7'
     reportUnnecessaryTypeIgnoreComment = 'warning'
     #   typeCheckingMode = 'strict'
 
 [tool.ruff]
     target-version = 'py37'
-    select = ['E', 'F', 'B', 'Q']
+    select = ['E', 'F', 'B', 'Q', 'I', 'W']
     ignore = ['E501']
 
+[tool.ruff.isort]
+combine-as-imports = true
+extra-standard-library = ['typing_extensions']
+
 [tool.ruff.per-file-ignores]
     "**/__init__.py" = ['F403']
     "**/*.pyi" = ['F403', 'F405']
```

### Comparing `sans-1.0.0a2/sans/__init__.py` & `sans-1.0.0a3/sans/__init__.py`

 * *Files 13% similar despite different names*

```diff
@@ -18,35 +18,26 @@
 # AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 # LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 # OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 # SOFTWARE.
 
 import sys as _sys
 
-try:
-    import httpx as _httpx
-except ImportError:
-    pass
-else:
-    # submodules that require httpx
-    from ._state import set_agent as set_agent
-    from .client import *
-    from .errors import *
-    from .limiter import *
-    from .request import *
-    from .response import *
-    from .utils import *
-
-    del _httpx
-
-# submodules that do not require httpx
+from ._state import set_agent as set_agent
+from .auth import *
+from .client import *
+from .errors import *
+from .limiter import *
 from .lock import *
+from .response import *
+from .url import *
+from .utils import *
 
 if _sys.version_info < (3, 8):
-    from importlib_metadata import metadata as _metadata
+    from importlib_metadata import metadata as _metadata  # type: ignore
 else:
     from importlib.metadata import metadata as _metadata
 
 __copyright__ = "Copyright 2019-2023 Zephyrkul"
 
 _meta = _metadata(__name__)
 __title__ = _meta["Name"]
```

### Comparing `sans-1.0.0a2/sans/client.pyi` & `sans-1.0.0a3/sans/client.pyi`

 * *Files 16% similar despite different names*

```diff
@@ -1,18 +1,39 @@
-from contextlib import asynccontextmanager, contextmanager
-from typing import Any, AsyncIterator, Iterator, Mapping, overload
+from __future__ import annotations
 
-from httpx import (
-    AsyncClient as _XAsyncClient,
-    BaseTransport,
-    Client as _XClient,
-    Limits,
-    Response as _Response,
+from typing import (
+    TYPE_CHECKING,
+    Any,
+    AsyncContextManager,
+    Callable,
+    Collection,
+    ContextManager,
+    Mapping,
+    overload,
 )
-from httpx._types import *
+
+import httpx
+
+if TYPE_CHECKING:
+    from typing_extensions import TypedDict
+
+    from httpx._types import (
+        AuthTypes,
+        CertTypes,
+        CookieTypes,
+        HeaderTypes,
+        ProxiesTypes,
+        QueryParamTypes,
+        RequestContent,
+        RequestData,
+        RequestFiles,
+        TimeoutTypes,
+        URLTypes,
+        VerifyTypes,
+    )
 
 from .limiter import RateLimiter
 from .response import Response
 
 __all__ = [
     "Client",
     "AsyncClient",
@@ -23,21 +44,33 @@
     "patch",
     "post",
     "put",
     "request",
     "stream",
 ]
 
+class _EventHooks(TypedDict):
+    request: list[Callable[[httpx.Request], None]]
+    response: list[Callable[[httpx.Response], None]]
+
+class _EventHooksParam(TypedDict):
+    request: Collection[Callable[[httpx.Request], None]]
+    response: Collection[Callable[[httpx.Response], None]]
+
 class _ClientMixin:
     @property
     def auth(self) -> RateLimiter: ...
     @auth.setter
     def auth(self, auth: RateLimiter) -> None: ...
+    @property
+    def event_hooks(self) -> _EventHooks: ...
+    @event_hooks.setter
+    def event_hooks(self, value: _EventHooksParam) -> None: ...
 
-class ClientType(_ClientMixin, _XClient):
+class ClientType(_ClientMixin, httpx.Client):
     @overload
     def request(
         self,
         method: str,
         url: URLTypes,
         *,
         content: RequestContent = ...,
@@ -47,15 +80,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def request(
         self,
         method: str,
         url: URLTypes,
         *,
         content: RequestContent = ...,
@@ -69,24 +102,24 @@
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
     ) -> Response: ...
     @overload
     def send(
         self,
-        request: Request,
+        request: httpx.Request,
         *,
         stream: bool = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def send(
         self,
-        request: Request,
+        request: httpx.Request,
         *,
         stream: bool = ...,
         auth: RateLimiter = ...,
         follow_redirects: bool = ...,
     ) -> Response: ...
     @overload
     def get(
@@ -96,15 +129,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def get(
         self,
         url: URLTypes,
         *,
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
@@ -122,15 +155,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def options(
         self,
         url: URLTypes,
         *,
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
@@ -148,15 +181,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def head(
         self,
         url: URLTypes,
         *,
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
@@ -178,15 +211,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def post(
         self,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -212,15 +245,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def put(
         self,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -246,15 +279,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def patch(
         self,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -276,30 +309,29 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     def delete(
         self,
         url: URLTypes,
         *,
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: RateLimiter = ...,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
     ) -> Response: ...
     @overload
-    @contextmanager
     def stream(
         self,
         method: str,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -308,17 +340,16 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> Iterator[_Response]: ...
+    ) -> ContextManager[httpx.Response]: ...
     @overload
-    @contextmanager
     def stream(
         self,
         method: str,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -327,17 +358,17 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: RateLimiter = ...,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> Iterator[Response]: ...
+    ) -> ContextManager[Response]: ...
 
-class AsyncClientType(_ClientMixin, _XAsyncClient):
+class AsyncClientType(_ClientMixin, httpx.AsyncClient):
     @overload
     async def request(
         self,
         method: str,
         url: URLTypes,
         *,
         content: RequestContent = ...,
@@ -347,15 +378,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def request(
         self,
         method: str,
         url: URLTypes,
         *,
         content: RequestContent = ...,
@@ -369,24 +400,24 @@
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
     ) -> Response: ...
     @overload
     async def send(
         self,
-        request: Request,
+        request: httpx.Request,
         *,
         stream: bool = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def send(
         self,
-        request: Request,
+        request: httpx.Request,
         *,
         stream: bool = ...,
         auth: RateLimiter = ...,
         follow_redirects: bool = ...,
     ) -> Response: ...
     @overload
     async def get(
@@ -396,15 +427,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def get(
         self,
         url: URLTypes,
         *,
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
@@ -422,15 +453,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def options(
         self,
         url: URLTypes,
         *,
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
@@ -448,15 +479,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def head(
         self,
         url: URLTypes,
         *,
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
@@ -478,15 +509,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def post(
         self,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -512,15 +543,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def put(
         self,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -546,15 +577,15 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def patch(
         self,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -576,30 +607,29 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> _Response: ...
+    ) -> httpx.Response: ...
     @overload
     async def delete(
         self,
         url: URLTypes,
         *,
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: RateLimiter = ...,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
     ) -> Response: ...
     @overload
-    @asynccontextmanager
     def stream(
         self,
         method: str,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -608,17 +638,16 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: AuthTypes,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> AsyncIterator[_Response]: ...
+    ) -> AsyncContextManager[httpx.Response]: ...
     @overload
-    @asynccontextmanager
     def stream(
         self,
         method: str,
         url: URLTypes,
         *,
         content: RequestContent = ...,
         data: RequestData[Any, Any] = ...,
@@ -627,60 +656,129 @@
         params: QueryParamTypes = ...,
         headers: HeaderTypes = ...,
         cookies: CookieTypes = ...,
         auth: RateLimiter = ...,
         follow_redirects: bool = ...,
         timeout: TimeoutTypes = ...,
         extensions: dict[Any, Any] = ...,
-    ) -> AsyncIterator[Response]: ...
+    ) -> AsyncContextManager[Response]: ...
 
+@overload
+def Client(
+    *,
+    auth: AuthTypes,
+    params: QueryParamTypes = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    verify: VerifyTypes = ...,
+    cert: CertTypes = ...,
+    http1: bool = ...,
+    http2: bool = ...,
+    proxies: ProxiesTypes = ...,
+    mounts: Mapping[str, httpx.BaseTransport] = ...,
+    timeout: TimeoutTypes = ...,
+    follow_redirects: bool = ...,
+    limits: httpx.Limits = ...,
+    max_redirects: int = ...,
+    event_hooks: Mapping[str, list[Callable[..., Any]]] = ...,
+    base_url: URLTypes = ...,
+    transport: httpx.BaseTransport = ...,
+    app: Callable[..., Any] = ...,
+    trust_env: bool = ...,
+) -> httpx.Client: ...
+@overload
 def Client(
     *,
     auth: RateLimiter = ...,
     params: QueryParamTypes = ...,
     headers: HeaderTypes = ...,
     cookies: CookieTypes = ...,
     verify: VerifyTypes = ...,
     cert: CertTypes = ...,
     http1: bool = ...,
     http2: bool = ...,
     proxies: ProxiesTypes = ...,
-    mounts: Mapping[str, BaseTransport] = ...,
+    mounts: Mapping[str, httpx.BaseTransport] = ...,
     timeout: TimeoutTypes = ...,
     follow_redirects: bool = ...,
-    limits: Limits = ...,
+    limits: httpx.Limits = ...,
     max_redirects: int = ...,
-    event_hooks: Mapping[str, List[Callable[..., Any]]] = ...,
+    event_hooks: _EventHooksParam = ...,
     base_url: URLTypes = ...,
-    transport: BaseTransport = ...,
+    transport: httpx.BaseTransport = ...,
     app: Callable[..., Any] = ...,
     trust_env: bool = ...,
 ) -> ClientType: ...
+@overload
+def AsyncClient(
+    *,
+    auth: AuthTypes,
+    params: QueryParamTypes = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    verify: VerifyTypes = ...,
+    cert: CertTypes = ...,
+    http1: bool = ...,
+    http2: bool = ...,
+    proxies: ProxiesTypes = ...,
+    mounts: Mapping[str, httpx.BaseTransport] = ...,
+    timeout: TimeoutTypes = ...,
+    follow_redirects: bool = ...,
+    limits: httpx.Limits = ...,
+    max_redirects: int = ...,
+    event_hooks: _EventHooksParam = ...,
+    base_url: URLTypes = ...,
+    transport: httpx.BaseTransport = ...,
+    app: Callable[..., Any] = ...,
+    trust_env: bool = ...,
+) -> httpx.AsyncClient: ...
+@overload
 def AsyncClient(
     *,
     auth: RateLimiter = ...,
     params: QueryParamTypes = ...,
     headers: HeaderTypes = ...,
     cookies: CookieTypes = ...,
     verify: VerifyTypes = ...,
     cert: CertTypes = ...,
     http1: bool = ...,
     http2: bool = ...,
     proxies: ProxiesTypes = ...,
-    mounts: Mapping[str, BaseTransport] = ...,
+    mounts: Mapping[str, httpx.BaseTransport] = ...,
     timeout: TimeoutTypes = ...,
     follow_redirects: bool = ...,
-    limits: Limits = ...,
+    limits: httpx.Limits = ...,
     max_redirects: int = ...,
-    event_hooks: Mapping[str, List[Callable[..., Any]]] = ...,
+    event_hooks: Mapping[str, Collection[Callable[..., Any]]] = ...,
     base_url: URLTypes = ...,
-    transport: BaseTransport = ...,
+    transport: httpx.BaseTransport = ...,
     app: Callable[..., Any] = ...,
     trust_env: bool = ...,
 ) -> AsyncClientType: ...
+@overload
+def request(
+    method: str,
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    content: RequestContent = ...,
+    data: RequestData[Any, Any] = ...,
+    files: RequestFiles = ...,
+    json: Any = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    timeout: TimeoutTypes = ...,
+    follow_redirects: bool = ...,
+    verify: VerifyTypes = ...,
+    cert: CertTypes = ...,
+    trust_env: bool = ...,
+) -> httpx.Response: ...
+@overload
 def request(
     method: str,
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     content: RequestContent = ...,
     data: RequestData[Any, Any] = ...,
@@ -692,15 +790,35 @@
     proxies: ProxiesTypes = ...,
     timeout: TimeoutTypes = ...,
     follow_redirects: bool = ...,
     verify: VerifyTypes = ...,
     cert: CertTypes = ...,
     trust_env: bool = ...,
 ) -> Response: ...
-@contextmanager
+@overload
+def stream(
+    method: str,
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    content: RequestContent = ...,
+    data: RequestData[Any, Any] = ...,
+    files: RequestFiles = ...,
+    json: Any = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    timeout: TimeoutTypes = ...,
+    follow_redirects: bool = ...,
+    verify: VerifyTypes = ...,
+    cert: CertTypes = ...,
+    trust_env: bool = ...,
+) -> ContextManager[httpx.Response]: ...
+@overload
 def stream(
     method: str,
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     content: RequestContent = ...,
     data: RequestData[Any, Any] = ...,
@@ -711,57 +829,125 @@
     auth: RateLimiter = ...,
     proxies: ProxiesTypes = ...,
     timeout: TimeoutTypes = ...,
     follow_redirects: bool = ...,
     verify: VerifyTypes = ...,
     cert: CertTypes = ...,
     trust_env: bool = ...,
-) -> Iterator[Response]: ...
+) -> ContextManager[Response]: ...
+@overload
+def get(
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    follow_redirects: bool = ...,
+    cert: CertTypes = ...,
+    verify: VerifyTypes = ...,
+    timeout: TimeoutTypes = ...,
+    trust_env: bool = ...,
+) -> httpx.Response: ...
+@overload
 def get(
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     headers: HeaderTypes = ...,
     cookies: CookieTypes = ...,
     auth: RateLimiter = ...,
     proxies: ProxiesTypes = ...,
     follow_redirects: bool = ...,
     cert: CertTypes = ...,
     verify: VerifyTypes = ...,
     timeout: TimeoutTypes = ...,
     trust_env: bool = ...,
 ) -> Response: ...
+@overload
+def options(
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    follow_redirects: bool = ...,
+    cert: CertTypes = ...,
+    verify: VerifyTypes = ...,
+    timeout: TimeoutTypes = ...,
+    trust_env: bool = ...,
+) -> httpx.Response: ...
+@overload
 def options(
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     headers: HeaderTypes = ...,
     cookies: CookieTypes = ...,
     auth: RateLimiter = ...,
     proxies: ProxiesTypes = ...,
     follow_redirects: bool = ...,
     cert: CertTypes = ...,
     verify: VerifyTypes = ...,
     timeout: TimeoutTypes = ...,
     trust_env: bool = ...,
 ) -> Response: ...
+@overload
+def head(
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    follow_redirects: bool = ...,
+    cert: CertTypes = ...,
+    verify: VerifyTypes = ...,
+    timeout: TimeoutTypes = ...,
+    trust_env: bool = ...,
+) -> httpx.Response: ...
+@overload
 def head(
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     headers: HeaderTypes = ...,
     cookies: CookieTypes = ...,
     auth: RateLimiter = ...,
     proxies: ProxiesTypes = ...,
     follow_redirects: bool = ...,
     cert: CertTypes = ...,
     verify: VerifyTypes = ...,
     timeout: TimeoutTypes = ...,
     trust_env: bool = ...,
 ) -> Response: ...
+@overload
+def post(
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    content: RequestContent = ...,
+    data: RequestData[Any, Any] = ...,
+    files: RequestFiles = ...,
+    json: Any = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    timeout: TimeoutTypes = ...,
+    follow_redirects: bool = ...,
+    verify: VerifyTypes = ...,
+    cert: CertTypes = ...,
+    trust_env: bool = ...,
+) -> httpx.Response: ...
+@overload
 def post(
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     content: RequestContent = ...,
     data: RequestData[Any, Any] = ...,
     files: RequestFiles = ...,
@@ -772,14 +958,34 @@
     proxies: ProxiesTypes = ...,
     timeout: TimeoutTypes = ...,
     follow_redirects: bool = ...,
     verify: VerifyTypes = ...,
     cert: CertTypes = ...,
     trust_env: bool = ...,
 ) -> Response: ...
+@overload
+def put(
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    content: RequestContent = ...,
+    data: RequestData[Any, Any] = ...,
+    files: RequestFiles = ...,
+    json: Any = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    timeout: TimeoutTypes = ...,
+    follow_redirects: bool = ...,
+    verify: VerifyTypes = ...,
+    cert: CertTypes = ...,
+    trust_env: bool = ...,
+) -> httpx.Response: ...
+@overload
 def put(
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     content: RequestContent = ...,
     data: RequestData[Any, Any] = ...,
     files: RequestFiles = ...,
@@ -790,14 +996,34 @@
     proxies: ProxiesTypes = ...,
     timeout: TimeoutTypes = ...,
     follow_redirects: bool = ...,
     verify: VerifyTypes = ...,
     cert: CertTypes = ...,
     trust_env: bool = ...,
 ) -> Response: ...
+@overload
+def patch(
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    content: RequestContent = ...,
+    data: RequestData[Any, Any] = ...,
+    files: RequestFiles = ...,
+    json: Any = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    timeout: TimeoutTypes = ...,
+    follow_redirects: bool = ...,
+    verify: VerifyTypes = ...,
+    cert: CertTypes = ...,
+    trust_env: bool = ...,
+) -> httpx.Response: ...
+@overload
 def patch(
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     content: RequestContent = ...,
     data: RequestData[Any, Any] = ...,
     files: RequestFiles = ...,
@@ -808,14 +1034,30 @@
     proxies: ProxiesTypes = ...,
     timeout: TimeoutTypes = ...,
     follow_redirects: bool = ...,
     verify: VerifyTypes = ...,
     cert: CertTypes = ...,
     trust_env: bool = ...,
 ) -> Response: ...
+@overload
+def delete(
+    url: URLTypes,
+    *,
+    params: QueryParamTypes = ...,
+    headers: HeaderTypes = ...,
+    cookies: CookieTypes = ...,
+    auth: AuthTypes,
+    proxies: ProxiesTypes = ...,
+    follow_redirects: bool = ...,
+    cert: CertTypes = ...,
+    verify: VerifyTypes = ...,
+    timeout: TimeoutTypes = ...,
+    trust_env: bool = ...,
+) -> httpx.Response: ...
+@overload
 def delete(
     url: URLTypes,
     *,
     params: QueryParamTypes = ...,
     headers: HeaderTypes = ...,
     cookies: CookieTypes = ...,
     auth: RateLimiter = ...,
```

### Comparing `sans-1.0.0a2/sans/decoder.py` & `sans-1.0.0a3/sans/decoder.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,88 +1,127 @@
 from __future__ import annotations
 
 import codecs
-from operator import attrgetter, itemgetter
+import zlib
+from operator import itemgetter
 from typing import TYPE_CHECKING, Iterable
-from xml.etree.ElementTree import Element, XMLPullParser
+from xml.etree.ElementTree import Element, XMLParser, XMLPullParser
 
 if TYPE_CHECKING:
     from typing_extensions import Literal
 
 
+class GZipDecoder:
+    def __init__(self) -> None:
+        self._decompressobj = zlib.decompressobj(zlib.MAX_WBITS | 16)
+
+    def decode(self, data: bytes) -> bytes:
+        return self._decompressobj.decompress(data)
+
+    def flush(self) -> bytes:
+        return self._decompressobj.flush()
+
+
 class XMLDecoder:
-    _events = ["end"]
-    _read_events = property(attrgetter("_pull_parser.read_events"))
+    def __init__(self, encoding: str | None = None) -> None:
+        self._parser = XMLParser(encoding=encoding)
+
+    def decode(self, data: bytes) -> None:
+        self._parser.feed(data)
+
+    def flush(self) -> Element:
+        return self._parser.close()
 
-    def __init__(self, encoding: str = "utf-8") -> None:
-        self._decoder = codecs.getincrementaldecoder(encoding)("xmlcharrefreplace")
-        self._pull_parser = XMLPullParser(self._events)
 
-    def feed(self, data: bytes) -> Iterable[Element]:
-        self._pull_parser.feed(self._decoder.decode(data, False))
+class XMLChunker:
+    def __init__(self, *, encoding: str | None = None) -> None:
+        self._decoder_chain: list[codecs.IncrementalDecoder] = []
+        if encoding:
+            self._decoder_chain.append(
+                codecs.getincrementaldecoder(encoding)("replace")
+            )
+        self._pull_parser = XMLPullParser(["start", "end"])
+        self._root: Element | None = None
+
+    def decode(self, data: bytes) -> Iterable[Element]:
+        for chain in self._decoder_chain:
+            data = chain.decode(data, False)  # type: ignore
+        self._pull_parser.feed(data)
         return map(itemgetter(1), self._read_events())
 
-    def flush(self) -> Iterable[Element]:
-        self._pull_parser.feed(self._decoder.decode(b"", True))
+    def flush(self, data: bytes = b"") -> Iterable[Element]:
+        for chain in self._decoder_chain:
+            data = chain.decode(data, True)  # type: ignore
+        self._pull_parser.feed(data)
         self._pull_parser.close()
         return map(itemgetter(1), self._read_events())
 
-
-class XMLChunker(XMLDecoder):
-    _events = ["start", "end"]
-    _root: Element | None = None
-
     def _read_events(self) -> Iterable[tuple[Literal["end"], Element]]:
         depth = 0
+        element: Element
         for event, element in self._pull_parser.read_events():
             if not self._root:
                 self._root = element
             if event == "start":
                 depth += 1
             elif event == "end":
                 depth -= 1
                 if depth == 1:
                     yield event, element
                     self._root.clear()
 
 
 try:
-    from lxml.etree import XMLPullParser as LXMLPullParser, _Element as LElement
+    from lxml.etree import (
+        XMLParser as LXMLParser,
+        XMLPullParser as LXMLPullParser,
+        _Element as LElement,  # type: ignore
+    )
 except ImportError:
     pass
 else:
 
     class LXMLDecoder:
-        _events = ["end"]
-        _read_events = property(attrgetter("_pull_parser.read_events"))
+        def __init__(self, encoding: str | None = None) -> None:
+            self._parser = LXMLParser(encoding=encoding)
+
+        def decode(self, data: bytes) -> None:
+            self._parser.feed(data)
 
-        def __init__(self, encoding: str = "utf-8") -> None:
-            self._decoder = codecs.getincrementaldecoder(encoding)("xmlcharrefreplace")
-            # the typehint below is close enough due to missing stubs
-            self._pull_parser: XMLPullParser = LXMLPullParser(self._events)
+        def flush(self) -> LElement:
+            return self._parser.close()
 
-        def feed(self, data: bytes) -> Iterable[LElement]:
-            self._pull_parser.feed(self._decoder.decode(data, False))
+    class LXMLChunker:
+        def __init__(self, *, encoding: str | None = None) -> None:
+            self._decoder_chain: list[codecs.IncrementalDecoder] = []
+            if encoding:
+                self._decoder_chain.append(
+                    codecs.getincrementaldecoder(encoding)("replace")
+                )
+            self._pull_parser = LXMLPullParser(["start", "end"])
+
+        def decode(self, data: bytes) -> Iterable[LElement]:
+            for chain in self._decoder_chain:
+                data = chain.decode(data, False)  # type: ignore
+            self._pull_parser.feed(data)
             return map(itemgetter(1), self._read_events())
 
-        def flush(self) -> Iterable[LElement]:
-            self._pull_parser.feed(self._decoder.decode(b"", True))
+        def flush(self, data: bytes = b"") -> Iterable[LElement]:
+            for chain in self._decoder_chain:
+                data = chain.decode(data, True)  # type: ignore
+            self._pull_parser.feed(data)
             self._pull_parser.close()
             return map(itemgetter(1), self._read_events())
 
-    class LXMLChunker(LXMLDecoder):
-        _events = ["start", "end"]
-
         def _read_events(self) -> Iterable[tuple[Literal["end"], LElement]]:
-            element: LElement
             depth = 0
-            for event, element in self._pull_parser.read_events():
+            element: LElement
+            for event, element in self._pull_parser.read_events():  # type: ignore
+                if not self._root:
+                    self._root = element
                 if event == "start":
                     depth += 1
-                else:
-                    assert event == "end"
+                elif event == "end":
                     depth -= 1
                     if depth == 1:
                         yield event, element
-                        element.clear(keep_tail=True)  # type: ignore
-                        while element.getprevious() is not None:
-                            del element.getparent()[0]  # type: ignore
+                        self._root.clear()
```

### Comparing `sans-1.0.0a2/sans/errors.py` & `sans-1.0.0a3/sans/errors.py`

 * *Files 5% similar despite different names*

```diff
@@ -12,26 +12,31 @@
         _codes: ClassVar[Collection[int]]
 
 else:
     _HTTPStatusError = HTTPStatusError
 
 
 __all__ = [
+    "AgentNotSetError",
     "HTTPStatusError",  # re-export
     "ClientError",
     "BadRequest",
     "Forbidden",
     "NotFound",
     "Conflict",
     "Teapot",
     "TooManyRequests",
     "ServerError",
 ]
 
 
+class AgentNotSetError(RuntimeError):
+    pass
+
+
 def narrow(original: HTTPStatusError) -> HTTPStatusError:
     code = original.response.status_code
     match = (sys.maxsize, HTTPStatusError)
     for exc in globals().values():
         if not issubclass(exc, _HTTPStatusError):
             continue
         if exc is HTTPStatusError:
```

### Comparing `sans-1.0.0a2/sans/lock.py` & `sans-1.0.0a3/sans/lock.py`

 * *Files 11% similar despite different names*

```diff
@@ -4,18 +4,17 @@
 import threading
 from collections import deque
 from contextvars import Context, copy_context
 from functools import partial
 from operator import add
 from time import monotonic
 from typing import TYPE_CHECKING, Any, Callable, Mapping, TypeVar
-from urllib.parse import urlparse
 
 if TYPE_CHECKING:
-    from typing_extensions import Literal, Self
+    from typing_extensions import Literal
 
 __all__ = ["ResetLock"]
 
 
 _KT = TypeVar("_KT")
 
 
@@ -33,28 +32,14 @@
 
     def run(self) -> None:
         # freeze .when() at the current time
         self.when = partial(add, monotonic(), self.interval)
         return super().run()
 
 
-class _NullContext:
-    def __enter__(self):
-        pass
-
-    def __exit__(self, *_):
-        pass
-
-    async def __aenter__(self):
-        pass
-
-    async def __aexit__(self, *_):
-        pass
-
-
 # I would love to make this utilize a semaphore instead
 # However, since multiple clients can exist on one machine,
 # locking and checking the headers sequentially is a requirement
 class ResetLock:
     """
     Combination :class:`asyncio.Lock` and :class:`threading.Lock`
     for ratelimiting purposes.
@@ -62,15 +47,15 @@
     Usage::
 
         lock = ResetLock()
         [async] with lock.maybe_lock(url):
             response = ...
             lock.maybe_defer(response.headers)
 
-    Note that, when using :module:`httpx`,
+    Note that, when using :mod:`httpx`,
     using :class:`RateLimiter` will manage a global lock for you.
     """
 
     def __init__(self):
         self.__deferred: asyncio.TimerHandle | _Timer | None = None
         self._lock = threading.Lock()
         self._waiters: deque[asyncio.Future[Literal[True]]] = deque()
@@ -168,23 +153,14 @@
             return
         xrlr = _get_as_int(response_headers, "RateLimit-Remaining", 1)
         if xrlr:
             return
         xrlr = _get_as_int(response_headers, "RateLimit-Reset", 0)
         self._deferred = call_later(xrlr, self._release)
 
-    def maybe_lock(self, hostname: str, path: str | None = None) -> Self | _NullContext:
-        if not path:
-            url = urlparse(hostname)
-            hostname = url.hostname or ""
-            path = url.path
-        if hostname == "www.nationstates.net" and path == "/cgi-bin/api.cgi":
-            return self
-        return _NullContext()
-
     def locked(self):
         return self._lock.locked()
 
     def release(self):
         if self.deferred is not None:
             return
         self._wake_up_next()
```

### Comparing `sans-1.0.0a2/sans/request.py` & `sans-1.0.0a3/sans/url.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,83 +1,78 @@
 from __future__ import annotations
 
-from datetime import date
+from datetime import date as _date
 from typing import TYPE_CHECKING, Mapping
 
-from httpx import URL, Request as RequestType
+import httpx
 
 if TYPE_CHECKING:
     from typing_extensions import Literal
-API_URL = URL("https://www.nationstates.net/cgi-bin/api.cgi")
+API_URL = httpx.URL("https://www.nationstates.net/cgi-bin/api.cgi")
 
 __all__ = [
     "API_URL",
-    "Request",
     "Nation",
     "Region",
     "World",
     "WA",
     "Shard",
     "NationsDump",
     "RegionsDump",
     "CardsDump",
 ]
 
 
-def Request(*shards: str | Mapping[str, str], **parameters: str) -> RequestType:
+def Nation(nation: str, *shards: str, **parameters: str) -> httpx.URL:
+    return World(*shards, nation=nation, **parameters)
+
+
+def Region(region: str, *shards: str, **parameters: str) -> httpx.URL:
+    return World(*shards, region=region, **parameters)
+
+
+def World(*shards: str | Mapping[str, str], **parameters: str) -> httpx.URL:
     q: list[str | None] = [parameters.pop("q", None)]
     query: dict[str, str] = {}
     for shard in shards:
         try:
             shard = dict(shard)  # type: ignore
-        except TypeError:
+        except (TypeError, ValueError):
             q.append(str(shard))
         else:
             q.append(shard.pop("q", None))  # type: ignore
             query.update(shard)  # type: ignore
     query.update(parameters, q="+".join(map(str, filter(None, q))))
     if query.get("a", "").lower() == "sendtg":
         raise RuntimeError("sans does not currently support the telegram API.")
-    return RequestType("GET", API_URL, params=query)
-
-
-def Nation(nation: str, *shards: str, **parameters: str) -> RequestType:
-    return Request(*shards, nation=nation, **parameters)
-
-
-def Region(region: str, *shards: str, **parameters: str) -> RequestType:
-    return Request(*shards, region=region, **parameters)
-
-
-World = Request
+    return API_URL.copy_with(params=query)
 
 
-def WA(wa: Literal[1, "1", 2, "2"], *shards: str, **parameters: str) -> RequestType:
-    return Request(*shards, wa=str(wa), **parameters)
+def WA(wa: Literal[1, "1", 2, "2"], *shards: str, **parameters: str) -> httpx.URL:
+    return World(*shards, wa=str(wa), **parameters)
 
 
 def Shard(q: str, **parameters: str) -> dict[str, str]:
     parameters["q"] = q
     return parameters
 
 
 # https://www.nationstates.net/archive/nations/2018-09-30-nations-xml.gz
-def NationsDump(date: date | None = None) -> RequestType:
+def NationsDump(date: _date | None = None) -> httpx.URL:
     if date:
         path = date.strftime("/archive/nations/%Y-%m-%d-nations-xml.gz")
     else:
         path = "/pages/nations.xml.gz"
-    return RequestType("GET", API_URL.join(path))
+    return API_URL.join(path)
 
 
 # https://www.nationstates.net/archive/nations/2018-09-30-regions-xml.gz
-def RegionsDump(date: date | None = None) -> RequestType:
+def RegionsDump(date: _date | None = None) -> httpx.URL:
     if date:
         path = date.strftime("/archive/nations/%Y-%m-%d-regions-xml.gz")
     else:
         path = "/pages/regions.xml.gz"
-    return RequestType("GET", API_URL.join(path))
+    return API_URL.join(path)
 
 
-def CardsDump(season: int):
-    path = f"/pages/cardlist_S{season}.xml.gz"
-    return RequestType("GET", API_URL.join(path))
+def CardsDump(season: Literal[1, "1", 2, "2", 3, "3"]) -> httpx.URL:
+    return API_URL.join(f"/pages/cardlist_S{season}.xml.gz")
```

### Comparing `sans-1.0.0a2/sans/utils.py` & `sans-1.0.0a3/sans/utils.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from __future__ import annotations
 
 import sys
 from typing import Any, Coroutine, Mapping, overload
 from xml.etree import ElementTree as etree
 
 from .client import AsyncClientType, ClientType
-from .request import Request
 from .response import Response
+from .url import World
 
 __all__ = ["prepare_and_execute", "indent"]
 
 
 @overload
 def prepare_and_execute(
     client: ClientType, *shards: str | Mapping[str, str], **parameters: str
@@ -28,50 +28,65 @@
 def prepare_and_execute(
     client: ClientType | AsyncClientType,
     *shards: str | Mapping[str, str],
     **parameters: str,
 ) -> Response | Coroutine[Any, Any, Response]:
     if isinstance(client, AsyncClientType):
         return _prepare_async(client, *shards, **parameters)
-    request = Request(*shards, **parameters, mode="prepare")
-    response = client.send(request)
-    token: str = response.xml.find("TOKEN").text  # type: ignore
-    request = Request(*shards, **parameters, mode="execute", token=token)
-    return client.send(request)
+    request = World(*shards, **parameters, mode="prepare")
+    response = client.get(request)
+    token: str = response.xml.find("SUCCESS").text  # type: ignore
+    request = World(*shards, **parameters, mode="execute", token=token)
+    return client.get(request)
 
 
 async def _prepare_async(
     client: AsyncClientType, *shards: str | Mapping[str, str], **parameters: str
 ) -> Response:
-    request = Request(*shards, **parameters, mode="prepare")
-    response = await client.send(request)
-    token: str = response.xml.find("TOKEN").text  # type: ignore
-    request = Request(*shards, **parameters, mode="execute", token=token)
-    return await client.send(request)
+    request = World(*shards, **parameters, mode="prepare")
+    response = await client.get(request)
+    token: str = response.xml.find("SUCCESS").text  # type: ignore
+    request = World(*shards, **parameters, mode="execute", token=token)
+    return await client.get(request)
 
 
 if sys.version_info < (3, 9):
-    # from: https://stackoverflow.com/a/4590052
+    # from: https://github.com/python/cpython/blob/3.11/Lib/xml/etree/ElementTree.py#L1154
     def indent(
-        tree: etree.Element | etree.ElementTree,
-        space: str = "  ",
-        level: int = 0,
-        *,
-        _parent: etree.Element | None = None,
-        _index: int = -1,
-    ) -> None:
-        """Backport of ElementTree.indent"""
-        if not _parent and isinstance(tree, etree.ElementTree):
+        tree: etree.Element | etree.ElementTree, space: str = "  ", level: int = 0
+    ):
+        if isinstance(tree, etree.ElementTree):
             tree = tree.getroot()
-        assert isinstance(tree, etree.Element)
-        for i, node in enumerate(tree):
-            indent(node, space, level + 1, _parent=tree, _index=i)
-        if _parent is not None:
-            if _index == 0:
-                _parent.text = "\n" + (space * level)
-            else:
-                _parent[_index - 1].tail = "\n" + (space * level)
-            if _index == len(_parent) - 1:
-                tree.tail = "\n" + (space * (level - 1))
+        if level < 0:
+            raise ValueError(f"Initial indentation level must be >= 0, got {level}")
+        if not len(tree):
+            return
+
+        # Reduce the memory consumption by reusing indentation strings.
+        indentations = ["\n" + level * space]
+
+        def _indent_children(elem: etree.Element, level: int):
+            # Start a new indentation level for the first child.
+            child_level = level + 1
+            try:
+                child_indentation = indentations[child_level]
+            except IndexError:
+                child_indentation = indentations[level] + space
+                indentations.append(child_indentation)
+
+            if not elem.text or not elem.text.strip():
+                elem.text = child_indentation
+
+            for child in elem:
+                if len(child):
+                    _indent_children(child, child_level)
+                if not child.tail or not child.tail.strip():
+                    child.tail = child_indentation
+
+            # Dedent after the last child by overwriting the previous indentation.
+            if not child.tail.strip():  # type: ignore
+                child.tail = indentations[level]  # type: ignore
+
+        _indent_children(tree, 0)
 
 else:
     from xml.etree.ElementTree import indent
```

### Comparing `sans-1.0.0a2/sans.egg-info/PKG-INFO` & `sans-1.0.0a3/sans.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sans
-Version: 1.0.0a2
+Version: 1.0.0a3
 Summary: Synchronous / Asynchronous HTTPX extension for NationStates
 Author: Zephyrkul
 License: MIT License
         
         Copyright (c) 2018 - 2023
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -66,108 +66,122 @@
 it is highly recommended to use Dolph's pynationstates
 (`GitHub <https://github.com/DolphDev/pynationstates>`_
 | `PyPI <https://pypi.org/project/nationstates/>`_) for simpler scripts.
 
 Installing
 ----------
 
-::
+.. code::
 
    python3 -m pip install -U sans
 
 Development version:
 
-::
+.. code::
 
    python3 -m pip install -U https://github.com/zephyrkul/sans/archive/master.zip#egg=sans
 
 Examples
 --------
 
+Synchronous
+~~~~~~~~~~~
+
+.. code:: python
+
+   import sans
+   from xml.etree import ElementTree as ET
+
+   def main():
+      sans.set_agent("Darcania")
+      request = sans.Nation(
+         "darcania",
+         "fullname population flag census",
+         mode="score",
+         scale="65 66",
+      )
+      root = sans.get(request)
+      sans.indent(root)
+      print(ET.tostring(root, encoding="unicode"))
+
+      with sans.stream("GET", sans.RegionsDump()) as response:
+         for region in response.iter_xml():
+            sans.indent(region)
+            print(ET.tostring(region, encoding="unicode"))
+
+   if __name__ == "__main__":
+      main()
+
 Asynchronous
 ~~~~~~~~~~~~
 
-.. code:: py
+.. code:: python
 
    import asyncio
    import sans
-   from sans.api import Api, Dumps
-   from sans.utils import pretty_string
+   from xml.etree import ElementTree as ET
 
    async def main():
-       Api.agent = "Darcania"
-       request = Api(
-           "fullname population flag census",
-           nation="darcania",
-           mode="score",
-           scale="65 66",
-       )
-       root = await request
-       pretty = pretty_string(root)
-       print(pretty)
-
-       request = Dumps.REGIONS
-       async for region in request:
-           pretty = pretty_string(region)
-           print(pretty)
-
+      sans.set_agent("Darcania")
+      async with sans.AsyncClient() as client:
+         request = sans.Nation(
+            "darcania",
+            "fullname population flag census",
+            mode="score",
+            scale="65 66",
+         )
+         root = (await client.send(request)).xml
+         sans.indent(root)
+         print(ET.tostring(root, encoding="unicode"))
+
+         async with client.stream("GET", sans.RegionsDump()) as response:
+            async for region in response.aiter_xml():
+               sans.indent(region)
+               print(ET.tostring(region, encoding="unicode"))
 
-   asyncio.run(main())  # Python 3.7+ only
+   if __name__ == "__main__":
+      asyncio.run(main())
 
-Synchronous
-~~~~~~~~~~~
+Command Line
+------------
 
-.. code:: py
+.. code::
 
-   import sans
-   from sans.api import Api, Dumps
+   $ sans --nation darcania census --scale "65 66" --mode score --agent Darcania
 
-   def main():
-       sans.run_in_thread()
-       Api.agent = "Darcania"
-       request = Api(
-           "fullname population flag census",
-           nation="darcania",
-           mode="score",
-           scale="65 66",
-       )
-       root = request.threadsafe()
-       pretty = pretty_string(root)
-       print(pretty)
-
-       request = Dumps.REGIONS
-       for region in request.threadsafe:
-           pretty = pretty_string(region)
-           print(pretty)
+   <CENSUS>
+      <SCALE id="65">
+         <SCORE>4949.00</SCORE>
+      </SCALE>
+      <SCALE id="66">
+         <SCORE>130.00</SCORE>
+      </SCALE>
+   </CENSUS>
 
+   $ sans --nation testlandia fullname
 
-   main()
+   <FULLNAME>The Hive Mind of Testlandia</FULLNAME>
 
-Command Line
-------------
+   sans --region "the north pacific" numnations lastupdate
 
-::
+   <LASTUPDATE>1683650325</LASTUPDATE>
+   <NUMNATIONS>10503</NUMNATIONS>
 
-   python3 -m sans --nation darcania census --scale "65 66" --mode score --agent Darcania
-   <NATION>...</NATION>
-   sans --nation testlandia fullname
-   <NATION>...</NATION>
-   sans --region "the north pacific" numnations lastupdate
-   <REGION>...</REGION>
-   sans --quit
-   Exiting...
+   $ sans --quit
+   No query provided. Exiting...
 
 Requirements
 ------------
 
--  Python 3.6+
--  aiohttp
--  lxml
+-  Python 3.7+
+-  httpx
 
 .. |pypi| image:: https://img.shields.io/pypi/v/sans.svg
    :target: https://pypi.python.org/pypi/sans
+   :alt: pypi version
 .. |Code style: black| image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/ambv/black
-.. |Build Status| image:: https://github.com/zephyrkul/sans/workflows/build/badge.svg
-   :target: https://github.com/zephyrkul/sans/actions?workflow=build
+.. |Build Status| image:: https://results.pre-commit.ci/badge/github/Zephyrkul/sans/master.svg
+   :target: https://results.pre-commit.ci/latest/github/Zephyrkul/sans/master
+   :alt: pre-commit.ci status
 .. |Documentation Status| image:: https://readthedocs.org/projects/sans/badge/?version=latest
    :target: http://sans.readthedocs.org/en/latest/?badge=latest
```

### Comparing `sans-1.0.0a2/sans.egg-info/SOURCES.txt` & `sans-1.0.0a3/sans.egg-info/SOURCES.txt`

 * *Files 24% similar despite different names*

```diff
@@ -5,34 +5,37 @@
 README.rst
 pyproject.toml
 requirements.txt
 setup.py
 .github/workflows/codeql-analysis.yml
 .github/workflows/pythonpublish.yml
 docs/Makefile
-docs/__init__.rst
-docs/api.rst
+docs/auth.rst
 docs/conf.py
 docs/errors.rst
 docs/index.rst
+docs/limiter.rst
+docs/lock.rst
 docs/make.bat
-docs/objects.rst
+docs/response.rst
+docs/url.rst
 docs/utils.rst
 sans/__init__.py
 sans/__main__.py
 sans/_state.py
+sans/auth.py
 sans/client.py
 sans/client.pyi
 sans/decoder.py
 sans/errors.py
 sans/limiter.py
 sans/lock.py
 sans/py.typed
-sans/request.py
 sans/response.py
+sans/url.py
 sans/utils.py
 sans.egg-info/PKG-INFO
 sans.egg-info/SOURCES.txt
 sans.egg-info/dependency_links.txt
 sans.egg-info/entry_points.txt
 sans.egg-info/requires.txt
 sans.egg-info/top_level.txt
```

