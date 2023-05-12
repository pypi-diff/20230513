# Comparing `tmp/stogui-0.1.8.tar.gz` & `tmp/stogui-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stogui-0.1.8.tar", last modified: Thu Apr 27 04:22:02 2023, max compression
+gzip compressed data, was "stogui-0.1.9.tar", last modified: Wed May  3 21:12:08 2023, max compression
```

## Comparing `stogui-0.1.8.tar` & `stogui-0.1.9.tar`

### file list

```diff
@@ -1,70 +1,85 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.914566 stogui-0.1.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-04-27 04:21:08.000000 stogui-0.1.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       80 2023-04-27 04:21:08.000000 stogui-0.1.8/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)      230 2023-04-27 04:22:02.914566 stogui-0.1.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-04-27 04:21:08.000000 stogui-0.1.8/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      453 2023-04-27 04:22:02.914566 stogui-0.1.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-04-27 04:21:08.000000 stogui-0.1.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui/
--rw-r--r--   0 runner    (1001) docker     (123)      135 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui/pipeline_maker/
--rw-r--r--   0 runner    (1001) docker     (123)     1778 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui/pipeline_maker/frontend/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.890566 stogui-0.1.8/stogui/pipeline_maker/frontend/build/
--rw-r--r--   0 runner    (1001) docker     (123)      859 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/asset-manifest.json
--rw-r--r--   0 runner    (1001) docker     (123)   197459 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/bootstrap.min.css
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/index.html
--rw-r--r--   0 runner    (1001) docker     (123)      564 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/precache-manifest.0a876a512cd852ca08256154cd9ec9e5.js
--rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/service-worker.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.898566 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/
--rw-r--r--   0 runner    (1001) docker     (123)  1718475 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js
--rw-r--r--   0 runner    (1001) docker     (123)     6206 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js.LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)  6244744 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js.map
--rw-r--r--   0 runner    (1001) docker     (123)     7998 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/main.8b135fc4.chunk.js
--rw-r--r--   0 runner    (1001) docker     (123)    19537 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/main.8b135fc4.chunk.js.map
--rw-r--r--   0 runner    (1001) docker     (123)     1598 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/runtime-main.44d30fc2.js
--rw-r--r--   0 runner    (1001) docker     (123)     8317 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/runtime-main.44d30fc2.js.map
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.898566 stogui-0.1.8/stogui/session_table/
--rw-r--r--   0 runner    (1001) docker     (123)      951 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui/session_table/frontend/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.898566 stogui-0.1.8/stogui/session_table/frontend/build/
--rw-r--r--   0 runner    (1001) docker     (123)     1322 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/asset-manifest.json
--rw-r--r--   0 runner    (1001) docker     (123)   197459 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/bootstrap.min.css
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/index.html
--rw-r--r--   0 runner    (1001) docker     (123)     1168 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/precache-manifest.c54c351d49044c01549cdc85c1442590.js
--rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/service-worker.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui/session_table/frontend/build/static/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.906566 stogui-0.1.8/stogui/session_table/frontend/build/static/js/
--rw-r--r--   0 runner    (1001) docker     (123)  1555139 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js
--rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js.LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)  5532059 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js.map
--rw-r--r--   0 runner    (1001) docker     (123)    26632 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/static/js/main.7b870594.chunk.js
--rw-r--r--   0 runner    (1001) docker     (123)    68447 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/static/js/main.7b870594.chunk.js.map
--rw-r--r--   0 runner    (1001) docker     (123)     1598 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/static/js/runtime-main.44d30fc2.js
--rw-r--r--   0 runner    (1001) docker     (123)     8317 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/session_table/frontend/build/static/js/runtime-main.44d30fc2.js.map
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.906566 stogui-0.1.8/stogui/test_results_table/
--rw-r--r--   0 runner    (1001) docker     (123)      966 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui/test_results_table/frontend/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.906566 stogui-0.1.8/stogui/test_results_table/frontend/build/
--rw-r--r--   0 runner    (1001) docker     (123)     1322 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/asset-manifest.json
--rw-r--r--   0 runner    (1001) docker     (123)   197459 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/bootstrap.min.css
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/index.html
--rw-r--r--   0 runner    (1001) docker     (123)     1168 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/precache-manifest.5d02d48087dbf73d69c390198230a4ff.js
--rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/service-worker.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui/test_results_table/frontend/build/static/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.914566 stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/
--rw-r--r--   0 runner    (1001) docker     (123)  1557976 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js
--rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js.LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)  5588155 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js.map
--rw-r--r--   0 runner    (1001) docker     (123)    27308 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/main.ad6bea04.chunk.js
--rw-r--r--   0 runner    (1001) docker     (123)    71287 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/main.ad6bea04.chunk.js.map
--rw-r--r--   0 runner    (1001) docker     (123)     1598 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/runtime-main.44d30fc2.js
--rw-r--r--   0 runner    (1001) docker     (123)     8317 2023-04-27 04:21:08.000000 stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/runtime-main.44d30fc2.js.map
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-27 04:22:02.886566 stogui-0.1.8/stogui.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      230 2023-04-27 04:22:02.000000 stogui-0.1.8/stogui.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2831 2023-04-27 04:22:02.000000 stogui-0.1.8/stogui.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-27 04:22:02.000000 stogui-0.1.8/stogui.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-27 04:22:02.000000 stogui-0.1.8/stogui.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-04-27 04:22:02.000000 stogui-0.1.8/stogui.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-04-27 04:22:02.000000 stogui-0.1.8/stogui.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.187061 stogui-0.1.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-03 21:11:10.000000 stogui-0.1.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-05-03 21:11:10.000000 stogui-0.1.9/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)      230 2023-05-03 21:12:08.187061 stogui-0.1.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-03 21:11:10.000000 stogui-0.1.9/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      453 2023-05-03 21:12:08.187061 stogui-0.1.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-03 21:11:10.000000 stogui-0.1.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.143060 stogui-0.1.9/stogui/
+-rw-r--r--   0 runner    (1001) docker     (123)      168 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.147060 stogui-0.1.9/stogui/dpp_table/
+-rw-r--r--   0 runner    (1001) docker     (123)      880 2023-05-03 21:12:05.000000 stogui-0.1.9/stogui/dpp_table/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.139060 stogui-0.1.9/stogui/dpp_table/frontend/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.147060 stogui-0.1.9/stogui/dpp_table/frontend/build/
+-rw-r--r--   0 runner    (1001) docker     (123)     1322 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/asset-manifest.json
+-rw-r--r--   0 runner    (1001) docker     (123)   197459 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/bootstrap.min.css
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/service-worker.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.143060 stogui-0.1.9/stogui/dpp_table/frontend/build/static/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.155061 stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/
+-rw-r--r--   0 runner    (1001) docker     (123)  1557976 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/2.41898aa7.chunk.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/2.41898aa7.chunk.js.LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)  5588155 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/2.41898aa7.chunk.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)     1598 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/runtime-main.44d30fc2.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8317 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/runtime-main.44d30fc2.js.map
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.155061 stogui-0.1.9/stogui/pipeline_maker/
+-rw-r--r--   0 runner    (1001) docker     (123)     1778 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.143060 stogui-0.1.9/stogui/pipeline_maker/frontend/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.155061 stogui-0.1.9/stogui/pipeline_maker/frontend/build/
+-rw-r--r--   0 runner    (1001) docker     (123)      859 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/asset-manifest.json
+-rw-r--r--   0 runner    (1001) docker     (123)   197459 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/bootstrap.min.css
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)      564 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/precache-manifest.0a876a512cd852ca08256154cd9ec9e5.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/service-worker.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.143060 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.167061 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/
+-rw-r--r--   0 runner    (1001) docker     (123)  1718475 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js
+-rw-r--r--   0 runner    (1001) docker     (123)     6206 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js.LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)  6244744 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)     7998 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/main.8b135fc4.chunk.js
+-rw-r--r--   0 runner    (1001) docker     (123)    19537 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/main.8b135fc4.chunk.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)     1598 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/runtime-main.44d30fc2.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8317 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/runtime-main.44d30fc2.js.map
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.167061 stogui-0.1.9/stogui/session_table/
+-rw-r--r--   0 runner    (1001) docker     (123)      951 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.143060 stogui-0.1.9/stogui/session_table/frontend/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.167061 stogui-0.1.9/stogui/session_table/frontend/build/
+-rw-r--r--   0 runner    (1001) docker     (123)     1322 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/asset-manifest.json
+-rw-r--r--   0 runner    (1001) docker     (123)   197459 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/bootstrap.min.css
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)     1168 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/precache-manifest.c54c351d49044c01549cdc85c1442590.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/service-worker.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.143060 stogui-0.1.9/stogui/session_table/frontend/build/static/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.175061 stogui-0.1.9/stogui/session_table/frontend/build/static/js/
+-rw-r--r--   0 runner    (1001) docker     (123)  1555139 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js.LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)  5532059 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)    26632 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/static/js/main.7b870594.chunk.js
+-rw-r--r--   0 runner    (1001) docker     (123)    68447 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/static/js/main.7b870594.chunk.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)     1598 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/static/js/runtime-main.44d30fc2.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8317 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/session_table/frontend/build/static/js/runtime-main.44d30fc2.js.map
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.175061 stogui-0.1.9/stogui/test_results_table/
+-rw-r--r--   0 runner    (1001) docker     (123)      966 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.143060 stogui-0.1.9/stogui/test_results_table/frontend/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.179061 stogui-0.1.9/stogui/test_results_table/frontend/build/
+-rw-r--r--   0 runner    (1001) docker     (123)     1322 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/asset-manifest.json
+-rw-r--r--   0 runner    (1001) docker     (123)   197459 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/bootstrap.min.css
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)     1168 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/precache-manifest.5d02d48087dbf73d69c390198230a4ff.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1183 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/service-worker.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.143060 stogui-0.1.9/stogui/test_results_table/frontend/build/static/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.187061 stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/
+-rw-r--r--   0 runner    (1001) docker     (123)  1557976 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js.LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)  5588155 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)    27308 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/main.ad6bea04.chunk.js
+-rw-r--r--   0 runner    (1001) docker     (123)    71287 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/main.ad6bea04.chunk.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)     1598 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/runtime-main.44d30fc2.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8317 2023-05-03 21:11:10.000000 stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/runtime-main.44d30fc2.js.map
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-03 21:12:08.147060 stogui-0.1.9/stogui.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      230 2023-05-03 21:12:07.000000 stogui-0.1.9/stogui.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3395 2023-05-03 21:12:08.000000 stogui-0.1.9/stogui.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-03 21:12:07.000000 stogui-0.1.9/stogui.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-03 21:12:07.000000 stogui-0.1.9/stogui.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-03 21:12:07.000000 stogui-0.1.9/stogui.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-03 21:12:07.000000 stogui-0.1.9/stogui.egg-info/top_level.txt
```

### Comparing `stogui-0.1.8/LICENSE` & `stogui-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/__init__.py` & `stogui-0.1.9/stogui/pipeline_maker/__init__.py`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/asset-manifest.json` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/asset-manifest.json`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/bootstrap.min.css` & `stogui-0.1.9/stogui/dpp_table/frontend/build/bootstrap.min.css`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/index.html` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/index.html`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/precache-manifest.0a876a512cd852ca08256154cd9ec9e5.js` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/precache-manifest.0a876a512cd852ca08256154cd9ec9e5.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/service-worker.js` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/service-worker.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js.LICENSE.txt` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js.LICENSE.txt`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js.map` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/main.8b135fc4.chunk.js` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/main.8b135fc4.chunk.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/main.8b135fc4.chunk.js.map` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/main.8b135fc4.chunk.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/runtime-main.44d30fc2.js` & `stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/runtime-main.44d30fc2.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/pipeline_maker/frontend/build/static/js/runtime-main.44d30fc2.js.map` & `stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/runtime-main.44d30fc2.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/__init__.py` & `stogui-0.1.9/stogui/session_table/__init__.py`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/asset-manifest.json` & `stogui-0.1.9/stogui/session_table/frontend/build/asset-manifest.json`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/bootstrap.min.css` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/bootstrap.min.css`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/index.html` & `stogui-0.1.9/stogui/session_table/frontend/build/index.html`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/precache-manifest.c54c351d49044c01549cdc85c1442590.js` & `stogui-0.1.9/stogui/session_table/frontend/build/precache-manifest.c54c351d49044c01549cdc85c1442590.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/service-worker.js` & `stogui-0.1.9/stogui/session_table/frontend/build/service-worker.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js` & `stogui-0.1.9/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js.LICENSE.txt` & `stogui-0.1.9/stogui/dpp_table/frontend/build/static/js/2.41898aa7.chunk.js.LICENSE.txt`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js.map` & `stogui-0.1.9/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/static/js/main.7b870594.chunk.js` & `stogui-0.1.9/stogui/session_table/frontend/build/static/js/main.7b870594.chunk.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/static/js/main.7b870594.chunk.js.map` & `stogui-0.1.9/stogui/session_table/frontend/build/static/js/main.7b870594.chunk.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/static/js/runtime-main.44d30fc2.js` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/runtime-main.44d30fc2.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/session_table/frontend/build/static/js/runtime-main.44d30fc2.js.map` & `stogui-0.1.9/stogui/pipeline_maker/frontend/build/static/js/runtime-main.44d30fc2.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/__init__.py` & `stogui-0.1.9/stogui/test_results_table/__init__.py`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/asset-manifest.json` & `stogui-0.1.9/stogui/test_results_table/frontend/build/asset-manifest.json`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/bootstrap.min.css` & `stogui-0.1.9/stogui/session_table/frontend/build/bootstrap.min.css`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/index.html` & `stogui-0.1.9/stogui/test_results_table/frontend/build/index.html`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/precache-manifest.5d02d48087dbf73d69c390198230a4ff.js` & `stogui-0.1.9/stogui/test_results_table/frontend/build/precache-manifest.5d02d48087dbf73d69c390198230a4ff.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/service-worker.js` & `stogui-0.1.9/stogui/test_results_table/frontend/build/service-worker.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js` & `stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js.LICENSE.txt` & `stogui-0.1.9/stogui/session_table/frontend/build/static/js/2.268fd857.chunk.js.LICENSE.txt`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js.map` & `stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/2.6d15c91c.chunk.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/main.ad6bea04.chunk.js` & `stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/main.ad6bea04.chunk.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/main.ad6bea04.chunk.js.map` & `stogui-0.1.9/stogui/test_results_table/frontend/build/static/js/main.ad6bea04.chunk.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/runtime-main.44d30fc2.js` & `stogui-0.1.9/stogui/session_table/frontend/build/static/js/runtime-main.44d30fc2.js`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui/test_results_table/frontend/build/static/js/runtime-main.44d30fc2.js.map` & `stogui-0.1.9/stogui/session_table/frontend/build/static/js/runtime-main.44d30fc2.js.map`

 * *Files identical despite different names*

### Comparing `stogui-0.1.8/stogui.egg-info/SOURCES.txt` & `stogui-0.1.9/stogui.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -6,14 +6,24 @@
 stogui/__init__.py
 stogui.egg-info/PKG-INFO
 stogui.egg-info/SOURCES.txt
 stogui.egg-info/dependency_links.txt
 stogui.egg-info/not-zip-safe
 stogui.egg-info/requires.txt
 stogui.egg-info/top_level.txt
+stogui/dpp_table/__init__.py
+stogui/dpp_table/frontend/build/asset-manifest.json
+stogui/dpp_table/frontend/build/bootstrap.min.css
+stogui/dpp_table/frontend/build/index.html
+stogui/dpp_table/frontend/build/service-worker.js
+stogui/dpp_table/frontend/build/static/js/2.41898aa7.chunk.js
+stogui/dpp_table/frontend/build/static/js/2.41898aa7.chunk.js.LICENSE.txt
+stogui/dpp_table/frontend/build/static/js/2.41898aa7.chunk.js.map
+stogui/dpp_table/frontend/build/static/js/runtime-main.44d30fc2.js
+stogui/dpp_table/frontend/build/static/js/runtime-main.44d30fc2.js.map
 stogui/pipeline_maker/__init__.py
 stogui/pipeline_maker/frontend/build/asset-manifest.json
 stogui/pipeline_maker/frontend/build/bootstrap.min.css
 stogui/pipeline_maker/frontend/build/index.html
 stogui/pipeline_maker/frontend/build/precache-manifest.0a876a512cd852ca08256154cd9ec9e5.js
 stogui/pipeline_maker/frontend/build/service-worker.js
 stogui/pipeline_maker/frontend/build/static/js/2.395bb2b5.chunk.js
```

