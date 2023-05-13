# Comparing `tmp/fastapi-listing-0.0.7.tar.gz` & `tmp/fastapi-listing-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fastapi-listing-0.0.7.tar", last modified: Sun May  7 19:25:13 2023, max compression
+gzip compressed data, was "fastapi-listing-0.0.8.tar", last modified: Sat May 13 08:12:49 2023, max compression
```

## Comparing `fastapi-listing-0.0.7.tar` & `fastapi-listing-0.0.8.tar`

### file list

```diff
@@ -1,61 +1,62 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.415625 fastapi-listing-0.0.7/
--rw-r--r--   0 runner    (1001) docker     (123)    21413 2023-05-07 19:25:13.415625 fastapi-listing-0.0.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    20636 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.411625 fastapi-listing-0.0.7/fastapi_listing/
--rw-r--r--   0 runner    (1001) docker     (123)      769 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.411625 fastapi-listing-0.0.7/fastapi_listing/abstracts/
--rw-r--r--   0 runner    (1001) docker     (123)      401 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/abstracts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      366 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/abstracts/base_query.py
--rw-r--r--   0 runner    (1001) docker     (123)      722 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/abstracts/dao.py
--rw-r--r--   0 runner    (1001) docker     (123)      244 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/abstracts/filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/abstracts/listing.py
--rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/abstracts/paginator.py
--rw-r--r--   0 runner    (1001) docker     (123)      321 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/abstracts/sorter.py
--rw-r--r--   0 runner    (1001) docker     (123)      203 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/constants.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.411625 fastapi-listing-0.0.7/fastapi_listing/dao/
--rw-r--r--   0 runner    (1001) docker     (123)       35 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/dao/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4049 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/dao/generic_dao.py
--rw-r--r--   0 runner    (1001) docker     (123)      423 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/errors.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.411625 fastapi-listing-0.0.7/fastapi_listing/factory/
--rw-r--r--   0 runner    (1001) docker     (123)      120 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/factory/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      942 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/factory/_generic_factory.py
--rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/factory/filter.py
--rw-r--r--   0 runner    (1001) docker     (123)      760 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/factory/strategy.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.411625 fastapi-listing-0.0.7/fastapi_listing/filters/
--rw-r--r--   0 runner    (1001) docker     (123)      519 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/filters/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5274 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/filters/generic_filters.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.411625 fastapi-listing-0.0.7/fastapi_listing/interface/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/interface/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1286 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/interface/listing_meta_info.py
--rw-r--r--   0 runner    (1001) docker     (123)      677 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/loader.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.411625 fastapi-listing-0.0.7/fastapi_listing/mechanics/
--rw-r--r--   0 runner    (1001) docker     (123)      182 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/mechanics/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1920 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/mechanics/iterative_filter_mechanics.py
--rw-r--r--   0 runner    (1001) docker     (123)     1405 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/mechanics/singleton_sorter_mechanics.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.415625 fastapi-listing-0.0.7/fastapi_listing/paginator/
--rw-r--r--   0 runner    (1001) docker     (123)       80 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/paginator/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/paginator/naive_page_builder.py
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.415625 fastapi-listing-0.0.7/fastapi_listing/service/
--rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/service/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    14811 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/service/listing_main.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.415625 fastapi-listing-0.0.7/fastapi_listing/sorter/
--rw-r--r--   0 runner    (1001) docker     (123)       74 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/sorter/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1803 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/sorter/naive_page_sorter.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.415625 fastapi-listing-0.0.7/fastapi_listing/strategies/
--rw-r--r--   0 runner    (1001) docker     (123)      579 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/strategies/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1288 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/strategies/query_strategy.py
--rw-r--r--   0 runner    (1001) docker     (123)     1024 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/typing.py
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/fastapi_listing/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.411625 fastapi-listing-0.0.7/fastapi_listing.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    21413 2023-05-07 19:25:13.000000 fastapi-listing-0.0.7/fastapi_listing.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1577 2023-05-07 19:25:13.000000 fastapi-listing-0.0.7/fastapi_listing.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-07 19:25:13.000000 fastapi-listing-0.0.7/fastapi_listing.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      226 2023-05-07 19:25:13.000000 fastapi-listing-0.0.7/fastapi_listing.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-07 19:25:13.000000 fastapi-listing-0.0.7/fastapi_listing.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-07 19:25:13.415625 fastapi-listing-0.0.7/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2014 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:13.415625 fastapi-listing-0.0.7/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6983 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/tests/fake_listing_setup.py
--rw-r--r--   0 runner    (1001) docker     (123)     5095 2023-05-07 19:25:04.000000 fastapi-listing-0.0.7/tests/test_main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    21709 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    20760 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.477732 fastapi-listing-0.0.8/fastapi_listing/
+-rw-r--r--   0 runner    (1001) docker     (123)      769 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.477732 fastapi-listing-0.0.8/fastapi_listing/abstracts/
+-rw-r--r--   0 runner    (1001) docker     (123)      401 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/abstracts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      366 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/abstracts/base_query.py
+-rw-r--r--   0 runner    (1001) docker     (123)      722 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/abstracts/dao.py
+-rw-r--r--   0 runner    (1001) docker     (123)      244 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/abstracts/filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/abstracts/listing.py
+-rw-r--r--   0 runner    (1001) docker     (123)      362 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/abstracts/paginator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      321 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/abstracts/sorter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      203 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/constants.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.477732 fastapi-listing-0.0.8/fastapi_listing/dao/
+-rw-r--r--   0 runner    (1001) docker     (123)       35 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/dao/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4049 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/dao/generic_dao.py
+-rw-r--r--   0 runner    (1001) docker     (123)      423 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/errors.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.477732 fastapi-listing-0.0.8/fastapi_listing/factory/
+-rw-r--r--   0 runner    (1001) docker     (123)      120 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/factory/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      942 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/factory/_generic_factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/factory/filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      760 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/factory/strategy.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.477732 fastapi-listing-0.0.8/fastapi_listing/filters/
+-rw-r--r--   0 runner    (1001) docker     (123)      519 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/filters/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5274 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/filters/generic_filters.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/fastapi_listing/interface/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/interface/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1286 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/interface/listing_meta_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)      677 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/loader.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/fastapi_listing/mechanics/
+-rw-r--r--   0 runner    (1001) docker     (123)      182 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/mechanics/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1920 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/mechanics/iterative_filter_mechanics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1405 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/mechanics/singleton_sorter_mechanics.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/fastapi_listing/paginator/
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/paginator/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/paginator/naive_page_builder.py
+-rw-r--r--   0 runner    (1001) docker     (123)       25 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/fastapi_listing/service/
+-rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/service/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14811 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/service/listing_main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/fastapi_listing/sorter/
+-rw-r--r--   0 runner    (1001) docker     (123)       74 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/sorter/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1803 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/sorter/naive_page_sorter.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/fastapi_listing/strategies/
+-rw-r--r--   0 runner    (1001) docker     (123)      579 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/strategies/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1288 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/strategies/query_strategy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1024 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/typing.py
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/fastapi_listing/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.477732 fastapi-listing-0.0.8/fastapi_listing.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    21709 2023-05-13 08:12:49.000000 fastapi-listing-0.0.8/fastapi_listing.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-05-13 08:12:49.000000 fastapi-listing-0.0.8/fastapi_listing.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:12:49.000000 fastapi-listing-0.0.8/fastapi_listing.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      226 2023-05-13 08:12:49.000000 fastapi-listing-0.0.8/fastapi_listing.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 08:12:49.000000 fastapi-listing-0.0.8/fastapi_listing.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2164 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:49.481732 fastapi-listing-0.0.8/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9180 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/tests/fake_listing_setup.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5774 2023-05-13 08:12:39.000000 fastapi-listing-0.0.8/tests/test_main.py
```

### Comparing `fastapi-listing-0.0.7/PKG-INFO` & `fastapi-listing-0.0.8/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,34 +1,38 @@
 Metadata-Version: 2.1
 Name: fastapi-listing
-Version: 0.0.7
+Version: 0.0.8
 Summary: Advaned Data Listing Library for FastAPI
 Home-page: https://github.com/danielhasan1/fastapi-listing
 Author: Danish Hasan
 Author-email: dh813030@gmail.com
 Keywords: starlette,fastapi,pydantic,sqlalchemy
 Classifier: Development Status :: 4 - Beta
 Classifier: Environment :: Web Environment
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 Provides-Extra: test
+License-File: LICENSE
 
 # fastapi-listing
 
 An Advanced Data Listing Library for fastapi
 
 [![.github/workflows/deploy.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/deploy.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/deploy.yml)
-![PyPI - Downloads](https://img.shields.io/pypi/dw/fastapi-listing)[![.github/workflows/tests.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml)
+[![.github/workflows/tests.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml) ![PyPI - Downloads](https://img.shields.io/pypi/dw/fastapi-listing?color=%2334D058) ![PyPI - Programming Language](https://img.shields.io/pypi/pyversions/fastapi-listing.svg?color=%2334D058)
 
 The FastAPI Listing Library is a Python library for building fast, flexible, and customizable listing views in FastAPI web applications. It allows you to easily define listing views for your data models and customize the behavior of those views with minimal code.
 ## Features
 
  - Easy-to-use API for listing and formatting data
  - Customizable behavior with minimal code
  - Customizable formatting options, including sorting and filtering
```

### Comparing `fastapi-listing-0.0.7/README.md` & `fastapi-listing-0.0.8/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 # fastapi-listing
 
 An Advanced Data Listing Library for fastapi
 
 [![.github/workflows/deploy.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/deploy.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/deploy.yml)
-![PyPI - Downloads](https://img.shields.io/pypi/dw/fastapi-listing)[![.github/workflows/tests.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml)
+[![.github/workflows/tests.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml) ![PyPI - Downloads](https://img.shields.io/pypi/dw/fastapi-listing?color=%2334D058) ![PyPI - Programming Language](https://img.shields.io/pypi/pyversions/fastapi-listing.svg?color=%2334D058)
 
 The FastAPI Listing Library is a Python library for building fast, flexible, and customizable listing views in FastAPI web applications. It allows you to easily define listing views for your data models and customize the behavior of those views with minimal code.
 ## Features
 
  - Easy-to-use API for listing and formatting data
  - Customizable behavior with minimal code
  - Customizable formatting options, including sorting and filtering
```

### Comparing `fastapi-listing-0.0.7/fastapi_listing/__init__.py` & `fastapi-listing-0.0.8/fastapi_listing/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from fastapi_listing.factory import strategy_factory
 from fastapi_listing.strategies import NaiveQueryStrategy, NaivePaginationStrategy, SortingOrderStrategy
 from fastapi_listing.service.listing_main import ListingService, FastapiListing
 from fastapi_listing.mechanics import IterativeFilterMechanics, SingletonSorterMechanics
 
 
-__version__ = "0.0.7"
+__version__ = "0.0.8"
 
 strategy_factory.register_strategy("naive_paginator", NaivePaginationStrategy)
 strategy_factory.register_strategy("naive_sorter", SortingOrderStrategy)
 strategy_factory.register_strategy("naive_query", NaiveQueryStrategy)
 strategy_factory.register_strategy("iterative_filter_mechanics", IterativeFilterMechanics)
 strategy_factory.register_strategy("singleton_sorter_mechanics", SingletonSorterMechanics)
```

### Comparing `fastapi-listing-0.0.7/fastapi_listing/abstracts/dao.py` & `fastapi-listing-0.0.8/fastapi_listing/abstracts/dao.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/abstracts/listing.py` & `fastapi-listing-0.0.8/fastapi_listing/abstracts/listing.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/dao/generic_dao.py` & `fastapi-listing-0.0.8/fastapi_listing/dao/generic_dao.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/factory/_generic_factory.py` & `fastapi-listing-0.0.8/fastapi_listing/factory/_generic_factory.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/factory/filter.py` & `fastapi-listing-0.0.8/fastapi_listing/factory/filter.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/factory/strategy.py` & `fastapi-listing-0.0.8/fastapi_listing/factory/strategy.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/filters/__init__.py` & `fastapi-listing-0.0.8/fastapi_listing/filters/__init__.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/filters/generic_filters.py` & `fastapi-listing-0.0.8/fastapi_listing/filters/generic_filters.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/interface/listing_meta_info.py` & `fastapi-listing-0.0.8/fastapi_listing/interface/listing_meta_info.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/loader.py` & `fastapi-listing-0.0.8/fastapi_listing/loader.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/mechanics/iterative_filter_mechanics.py` & `fastapi-listing-0.0.8/fastapi_listing/mechanics/iterative_filter_mechanics.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/mechanics/singleton_sorter_mechanics.py` & `fastapi-listing-0.0.8/fastapi_listing/mechanics/singleton_sorter_mechanics.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/paginator/naive_page_builder.py` & `fastapi-listing-0.0.8/fastapi_listing/paginator/naive_page_builder.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/service/listing_main.py` & `fastapi-listing-0.0.8/fastapi_listing/service/listing_main.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/sorter/naive_page_sorter.py` & `fastapi-listing-0.0.8/fastapi_listing/sorter/naive_page_sorter.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/strategies/__init__.py` & `fastapi-listing-0.0.8/fastapi_listing/strategies/__init__.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing/strategies/query_strategy.py` & `fastapi-listing-0.0.8/fastapi_listing/strategies/query_strategy.py`

 * *Files 11% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
         if custom_fields:
             # ("BYPASS CUSTOM PYDANTIC FIELDS ALLOWED.")
             # when serializer contains fields that get filled via validators or at runtime
             # or fields that get generated from model fields.
             for field in field_list:
                 try:
-                    inst_fields.append(getattr(field, dao.model))
+                    inst_fields.append(getattr(dao.model, field))
                 except AttributeError:
                     pass
         else:
             inst_fields = [getattr(dao.model, field) for field in field_list]
         return inst_fields
 
     def get_query(self, *, request: FastapiRequest = None, dao: GenericDao = None,
```

### Comparing `fastapi-listing-0.0.7/fastapi_listing/typing.py` & `fastapi-listing-0.0.8/fastapi_listing/typing.py`

 * *Files identical despite different names*

### Comparing `fastapi-listing-0.0.7/fastapi_listing.egg-info/PKG-INFO` & `fastapi-listing-0.0.8/fastapi_listing.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,34 +1,38 @@
 Metadata-Version: 2.1
 Name: fastapi-listing
-Version: 0.0.7
+Version: 0.0.8
 Summary: Advaned Data Listing Library for FastAPI
 Home-page: https://github.com/danielhasan1/fastapi-listing
 Author: Danish Hasan
 Author-email: dh813030@gmail.com
 Keywords: starlette,fastapi,pydantic,sqlalchemy
 Classifier: Development Status :: 4 - Beta
 Classifier: Environment :: Web Environment
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 Provides-Extra: test
+License-File: LICENSE
 
 # fastapi-listing
 
 An Advanced Data Listing Library for fastapi
 
 [![.github/workflows/deploy.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/deploy.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/deploy.yml)
-![PyPI - Downloads](https://img.shields.io/pypi/dw/fastapi-listing)[![.github/workflows/tests.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml)
+[![.github/workflows/tests.yml](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml/badge.svg)](https://github.com/danielhasan1/fastapi-listing/actions/workflows/tests.yml) ![PyPI - Downloads](https://img.shields.io/pypi/dw/fastapi-listing?color=%2334D058) ![PyPI - Programming Language](https://img.shields.io/pypi/pyversions/fastapi-listing.svg?color=%2334D058)
 
 The FastAPI Listing Library is a Python library for building fast, flexible, and customizable listing views in FastAPI web applications. It allows you to easily define listing views for your data models and customize the behavior of those views with minimal code.
 ## Features
 
  - Easy-to-use API for listing and formatting data
  - Customizable behavior with minimal code
  - Customizable formatting options, including sorting and filtering
```

### Comparing `fastapi-listing-0.0.7/fastapi_listing.egg-info/SOURCES.txt` & `fastapi-listing-0.0.8/fastapi_listing.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+LICENSE
 README.md
 setup.py
 fastapi_listing/__init__.py
 fastapi_listing/constants.py
 fastapi_listing/errors.py
 fastapi_listing/loader.py
 fastapi_listing/py.typed
```

### Comparing `fastapi-listing-0.0.7/setup.py` & `fastapi-listing-0.0.8/setup.py`

 * *Files 22% similar despite different names*

```diff
@@ -33,14 +33,17 @@
         "Development Status :: 4 - Beta",
         "Environment :: Web Environment",
         "Intended Audience :: Developers",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
         "Programming Language :: Python",
         "Programming Language :: Python :: 3",
+        "Programming Language :: Python :: 3.7",
+        "Programming Language :: Python :: 3.8",
+        "Programming Language :: Python :: 3.9",
         "Programming Language :: Python :: 3.10",
         "Programming Language :: Python :: 3.11",
     ],
     python_requires=">=3.7",
     keywords=["starlette", "fastapi", "pydantic", "sqlalchemy"],
     extras_require={
         "test": [
```

### Comparing `fastapi-listing-0.0.7/tests/fake_listing_setup.py` & `fastapi-listing-0.0.8/tests/fake_listing_setup.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,13 +1,14 @@
+from typing import Optional
 from fastapi_listing import FastapiListing, ListingService
 from fastapi_listing.strategies import NaiveQueryStrategy, NaivePaginationStrategy, SortingOrderStrategy
 from fastapi_listing.factory import strategy_factory, filter_factory
 from fastapi_listing.filters import generic_filters
 from fastapi_listing.dao import GenericDao
-from pydantic import BaseModel, Field
+from pydantic import BaseModel, Field, root_validator
 from fastapi_listing import utils
 from sqlalchemy.orm import declarative_base
 from sqlalchemy import Column, String, Integer
 from sqlalchemy.dialects.mysql import BIT
 from typing import List, Dict
 
 Base = declarative_base()
@@ -34,14 +35,29 @@
     {
         "id": 2,
         "pn": "Hyundai Centro",
         "ia": 0
     }
 ]
 
+fake_custom_column_resp_aliased = [
+    {
+        "id": 1,
+        "pn": "Hyundai Verna",
+        "ia": 1,
+        "cd": "1-HV"
+    },
+    {
+        "id": 2,
+        "pn": "Hyundai Centro",
+        "ia": 0,
+        "cd": "2-HC"
+    }
+]
+
 fake_resp_aliased_size_1 = [
     {
         "id": 1,
         "pn": "Hyundai Verna",
         "ia": 1
     },
 ]
@@ -51,14 +67,22 @@
     "data": fake_resp_aliased,
     "totalCount": len(fake_db),
     "currentPageSize": 10,
     "currentPageNumber": 0,
     "hasNext": False
 }
 
+fake_db_response_with_custom_column = {
+    "data": fake_custom_column_resp_aliased,
+    "totalCount": len(fake_db),
+    "currentPageSize": 10,
+    "currentPageNumber": 0,
+    "hasNext": False
+}
+
 fake_db_response_page_size_1 = {
     "data": fake_resp_aliased_size_1,
     "totalCount": len(fake_resp_aliased_size_1),
     "currentPageSize": 1,
     "currentPageNumber": 0,
     "hasNext": False
 }
@@ -81,14 +105,46 @@
     totalCount: int
 
     class Config:
         orm_mode = True
         allow_population_by_field_name = True
 
 
+class ProductDetailWithCustomFields(BaseModel):
+    id: int
+    product_name: str = Field(alias="pn")
+    is_active: bool = Field(alias="ia")
+    code: Optional[str] = Field(alias="cd")
+
+    @root_validator
+    def generate_product_code(cls, values):
+        pnm = values["product_name"]
+        pnm = pnm.split()
+        cd = []
+        for nm in pnm:
+            cd.append(nm[:1])
+        values["code"] = f"{values['id']}-{''.join(cd)}"
+        return values
+
+    class Config:
+        allow_population_by_field_name = True
+
+
+class ProductPageWithCustomColumns(BaseModel):
+    data: List[ProductDetailWithCustomFields] = []
+    currentPageSize: int
+    currentPageNumber: int
+    hasNext: bool
+    totalCount: int
+
+    class Config:
+        orm_mode = True
+        allow_population_by_field_name = True
+
+
 class Product(Base):
     __tablename__ = 'fake_product'
     id = Column(Integer, primary_key=True)
     product_name = Column(String(500, 'utf8mb4_unicode_520_ci'), index=True)
     is_active = Column(BIT(1), nullable=False, index=True)
 
 
@@ -96,18 +152,24 @@
     model = Product
 
 
 class FakeQueryStrategyV1(NaiveQueryStrategy):
 
     def get_query(self, *, request=None, dao=None,
                   extra_context: dict = None):
-        assert extra_context.get("field_list") == list(ProductDetail.__fields__.keys())
-        assert extra_context.get("custom_fields") == False
+
         assert dao.model == Product
         assert isinstance(dao, FakeProductDao) == True
+        if not extra_context.get("custom_fields"):
+            assert extra_context.get("field_list") == list(ProductDetail.__fields__.keys())
+            assert [Product.id, Product.product_name, Product.is_active] == \
+                   self.get_inst_attr_to_read(custom_fields=False, field_list=extra_context.get("field_list"), dao=dao)
+        else:
+            assert [Product.id, Product.product_name, Product.is_active] == \
+                   self.get_inst_attr_to_read(custom_fields=True, field_list=extra_context.get("field_list"), dao=dao)
         return fake_db_query1
 
 
 class FakeSortingStrategy(SortingOrderStrategy):
 
     def sort(self, *, query=None, value: Dict[str, str] = None,
              extra_context: dict = None):
@@ -143,14 +205,25 @@
     SORTING_STRATEGY = "fake_sorting_strategy"
     PAGINATE_STRATEGY = "fake_paginator_strategy"
 
     def get_listing(self):
         return FastapiListing(self.request, self.dao, ProductDetail).get_response(self.MetaInfo(self))
 
 
+class TestListingServiceDefaultFlowWithCustomColumns(ListingService):
+    DEFAULT_SRT_ON = "id"
+    dao_kls = FakeProductDao
+    QUERY_STRATEGY = "fake_query_strategy"
+    SORTING_STRATEGY = "fake_sorting_strategy"
+    PAGINATE_STRATEGY = "fake_paginator_strategy"
+
+    def get_listing(self):
+        return FastapiListing(self.request, self.dao, ProductDetailWithCustomFields, custom_fields=True).get_response(self.MetaInfo(self))
+
+
 class FakePaginationStrategyV2(NaivePaginationStrategy):
 
     def paginate(self, query, request, extra_context: dict):
         pagination_params = utils.jsonify_query_params(request.query_params.get("pagination"))
         assert pagination_params == {"pageSize": 1, "page": 0}
         assert query == fake_db_query1
         return {
@@ -161,15 +234,15 @@
             "hasNext": False
         }
 
 
 strategy_factory.register_strategy("fake_paginator_strategy_v2", FakePaginationStrategyV2)
 
 
-class TestListinghServiceVariablePageFlow(ListingService):
+class TestListingServiceVariablePageFlow(ListingService):
     DEFAULT_SRT_ON = "id"
     dao_kls = FakeProductDao
     QUERY_STRATEGY = "fake_query_strategy"
     SORTING_STRATEGY = "fake_sorting_strategy"
     PAGINATE_STRATEGY = "fake_paginator_strategy_v2"
 
     def get_listing(self):
```

### Comparing `fastapi-listing-0.0.7/tests/test_main.py` & `fastapi-listing-0.0.8/tests/test_main.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,28 +1,34 @@
 from fastapi import Request
 from fastapi import FastAPI
 import pytest
 from fastapi.testclient import TestClient
 from .fake_listing_setup import ProductPage, TestListingServiceDefaultFlow, fake_db_response, \
-    fake_db_response_page_size_1, TestListinghServiceVariablePageFlow, TestListingServiceSortFlow, \
-    spawn_valueerror_for_strategy_registry, spawn_valueerror_for_filter_factory, invalid_type_factory_keys
+    fake_db_response_page_size_1, TestListingServiceVariablePageFlow, TestListingServiceSortFlow, \
+    spawn_valueerror_for_strategy_registry, spawn_valueerror_for_filter_factory, invalid_type_factory_keys, ProductPageWithCustomColumns, TestListingServiceDefaultFlowWithCustomColumns, fake_db_response_with_custom_column
 from fastapi_listing.errors import ListingFilterError
 
 app = FastAPI()
 
 
 @app.get("/", response_model=ProductPage)
 def read_main(request: Request):
     resp = TestListingServiceDefaultFlow(request, read_db="read_db_session", write_db="write_db_session").get_listing()
     return resp
 
 
+@app.get("/custom-columns", response_model=ProductPageWithCustomColumns)
+def read_main_with_custom_fields(request: Request):
+    resp = TestListingServiceDefaultFlowWithCustomColumns(request, read_db="read_db_session", write_db="write_db_session").get_listing()
+    return resp
+
+
 @app.get("/var-page", response_model=ProductPage)
 def read_limit_1_page(request: Request):
-    resp = TestListinghServiceVariablePageFlow(request, read_db="read_db_session",
+    resp = TestListingServiceVariablePageFlow(request, read_db="read_db_session",
                                                write_db="write_db_session").get_listing()
     return resp
 
 
 @app.get("/sort", response_model=ProductPage)
 def sort_test(reqeust: Request):
     resp = TestListingServiceSortFlow(reqeust).get_listing()
@@ -34,14 +40,20 @@
 
 def test_call_default():
     response = client.get("/", params={"pagination": "%7B%22pageSize%22%3A10%2C%20%22page%22%3A0%7D"})
     assert response.status_code == 200
     assert response.json() == fake_db_response
 
 
+def test_call_default_flow_with_custom_columns():
+    response = client.get("/custom-columns", params={"pagination": "%7B%22pageSize%22%3A10%2C%20%22page%22%3A0%7D"})
+    assert response.status_code == 200
+    assert response.json() == fake_db_response_with_custom_column
+
+
 def test_call_variable_page():
     response = client.get("/var-page", params={"pagination": "%7B%22pageSize%22%3A1%2C%20%22page%22%3A0%7D"})
     assert response.status_code == 200
     assert response.json() == fake_db_response_page_size_1
 
 
 def test_call_filter_not_registered():
```

