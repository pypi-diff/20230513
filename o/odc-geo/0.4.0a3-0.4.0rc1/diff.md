# Comparing `tmp/odc-geo-0.4.0a3.tar.gz` & `tmp/odc-geo-0.4.0rc1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "odc-geo-0.4.0a3.tar", last modified: Sat May  6 06:29:29 2023, max compression
+gzip compressed data, was "odc-geo-0.4.0rc1.tar", last modified: Sat May 13 02:27:02 2023, max compression
```

## Comparing `odc-geo-0.4.0a3.tar` & `odc-geo-0.4.0rc1.tar`

### file list

```diff
@@ -1,69 +1,69 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 06:29:29.980272 odc-geo-0.4.0a3/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       63 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     3900 2023-05-06 06:29:29.980272 odc-geo-0.4.0a3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2898 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 06:29:29.972272 odc-geo-0.4.0a3/odc/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 06:29:29.976272 odc-geo-0.4.0a3/odc/geo/
--rw-r--r--   0 runner    (1001) docker     (123)     1151 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5358 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_blocks.py
--rw-r--r--   0 runner    (1001) docker     (123)    15515 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_cog.py
--rw-r--r--   0 runner    (1001) docker     (123)     2775 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_compress.py
--rw-r--r--   0 runner    (1001) docker     (123)     4169 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_dask.py
--rw-r--r--   0 runner    (1001) docker     (123)     1465 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_interop.py
--rw-r--r--   0 runner    (1001) docker     (123)     4241 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_map.py
--rw-r--r--   0 runner    (1001) docker     (123)     8424 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_rgba.py
--rw-r--r--   0 runner    (1001) docker     (123)       56 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)    27222 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/_xr_interop.py
--rw-r--r--   0 runner    (1001) docker     (123)     2647 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/converters.py
--rw-r--r--   0 runner    (1001) docker     (123)    14454 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/crs.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 06:29:29.976272 odc-geo-0.4.0a3/odc/geo/data/
--rw-r--r--   0 runner    (1001) docker     (123)     1593 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/data/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      553 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/data/gbox.css
--rw-r--r--   0 runner    (1001) docker     (123)    23424 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/data/ocean.geojson.xz
--rw-r--r--   0 runner    (1001) docker     (123)     9959 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/gcp.py
--rw-r--r--   0 runner    (1001) docker     (123)    42911 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/geobox.py
--rw-r--r--   0 runner    (1001) docker     (123)    42282 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/geom.py
--rw-r--r--   0 runner    (1001) docker     (123)    10864 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/gridspec.py
--rw-r--r--   0 runner    (1001) docker     (123)    20248 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/math.py
--rw-r--r--   0 runner    (1001) docker     (123)    18443 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/overlap.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)    21996 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/roi.py
--rw-r--r--   0 runner    (1001) docker     (123)     6579 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/testutils.py
--rw-r--r--   0 runner    (1001) docker     (123)    11734 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/types.py
--rw-r--r--   0 runner    (1001) docker     (123)    10508 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/ui.py
--rw-r--r--   0 runner    (1001) docker     (123)     6735 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/warp.py
--rw-r--r--   0 runner    (1001) docker     (123)     1309 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/odc/geo/xr.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 06:29:29.976272 odc-geo-0.4.0a3/odc_geo.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3900 2023-05-06 06:29:29.000000 odc-geo-0.4.0a3/odc_geo.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1296 2023-05-06 06:29:29.000000 odc-geo-0.4.0a3/odc_geo.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-06 06:29:29.000000 odc-geo-0.4.0a3/odc_geo.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-06 06:29:29.000000 odc-geo-0.4.0a3/odc_geo.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      126 2023-05-06 06:29:29.000000 odc-geo-0.4.0a3/odc_geo.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-06 06:29:29.000000 odc-geo-0.4.0a3/odc_geo.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      646 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)     1309 2023-05-06 06:29:29.980272 odc-geo-0.4.0a3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 06:29:29.980272 odc-geo-0.4.0a3/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     4373 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_bbox.py
--rw-r--r--   0 runner    (1001) docker     (123)     3631 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_blocks.py
--rw-r--r--   0 runner    (1001) docker     (123)     1102 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_cog.py
--rw-r--r--   0 runner    (1001) docker     (123)     2707 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_converters.py
--rw-r--r--   0 runner    (1001) docker     (123)     9445 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_crs.py
--rw-r--r--   0 runner    (1001) docker     (123)     1855 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_dask_interop.py
--rw-r--r--   0 runner    (1001) docker     (123)      723 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_datasets.py
--rw-r--r--   0 runner    (1001) docker     (123)     4162 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_gbox_ops.py
--rw-r--r--   0 runner    (1001) docker     (123)     6638 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_gcp.py
--rw-r--r--   0 runner    (1001) docker     (123)    19992 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_geobox.py
--rw-r--r--   0 runner    (1001) docker     (123)     4158 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_geoboxtiles.py
--rw-r--r--   0 runner    (1001) docker     (123)    31468 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_geom.py
--rw-r--r--   0 runner    (1001) docker     (123)     3831 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_gridspec.py
--rw-r--r--   0 runner    (1001) docker     (123)     1842 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_map.py
--rw-r--r--   0 runner    (1001) docker     (123)     9934 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_math.py
--rw-r--r--   0 runner    (1001) docker     (123)    15659 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_overlap.py
--rw-r--r--   0 runner    (1001) docker     (123)     4569 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_rgba.py
--rw-r--r--   0 runner    (1001) docker     (123)      894 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_rioxarray_interop.py
--rw-r--r--   0 runner    (1001) docker     (123)    10069 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_roi.py
--rw-r--r--   0 runner    (1001) docker     (123)     3547 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_types.py
--rw-r--r--   0 runner    (1001) docker     (123)      839 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_ui.py
--rw-r--r--   0 runner    (1001) docker     (123)    18437 2023-05-06 06:29:17.000000 odc-geo-0.4.0a3/tests/test_xr_interop.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:27:02.470234 odc-geo-0.4.0rc1/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       63 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     3901 2023-05-13 02:27:02.470234 odc-geo-0.4.0rc1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2898 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:27:02.462233 odc-geo-0.4.0rc1/odc/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:27:02.466234 odc-geo-0.4.0rc1/odc/geo/
+-rw-r--r--   0 runner    (1001) docker     (123)     1151 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5358 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_blocks.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15515 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_cog.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2775 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_compress.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4169 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_dask.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1465 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_interop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4241 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_map.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8424 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_rgba.py
+-rw-r--r--   0 runner    (1001) docker     (123)       57 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27368 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/_xr_interop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2647 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/converters.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14454 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/crs.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:27:02.466234 odc-geo-0.4.0rc1/odc/geo/data/
+-rw-r--r--   0 runner    (1001) docker     (123)     1593 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/data/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      553 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/data/gbox.css
+-rw-r--r--   0 runner    (1001) docker     (123)    23424 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/data/ocean.geojson.xz
+-rw-r--r--   0 runner    (1001) docker     (123)     9959 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/gcp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42911 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/geobox.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42282 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/geom.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10864 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/gridspec.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20248 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/math.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18767 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/overlap.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)    21996 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/roi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6579 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/testutils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11734 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10508 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/ui.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6735 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/warp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1309 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/odc/geo/xr.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:27:02.466234 odc-geo-0.4.0rc1/odc_geo.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3901 2023-05-13 02:27:02.000000 odc-geo-0.4.0rc1/odc_geo.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1296 2023-05-13 02:27:02.000000 odc-geo-0.4.0rc1/odc_geo.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:27:02.000000 odc-geo-0.4.0rc1/odc_geo.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 02:27:02.000000 odc-geo-0.4.0rc1/odc_geo.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      126 2023-05-13 02:27:02.000000 odc-geo-0.4.0rc1/odc_geo.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-13 02:27:02.000000 odc-geo-0.4.0rc1/odc_geo.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      646 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)     1309 2023-05-13 02:27:02.470234 odc-geo-0.4.0rc1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 02:27:02.470234 odc-geo-0.4.0rc1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     4373 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_bbox.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3631 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_blocks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1102 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_cog.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2707 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_converters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9445 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_crs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1855 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_dask_interop.py
+-rw-r--r--   0 runner    (1001) docker     (123)      723 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_datasets.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4162 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_gbox_ops.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6638 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_gcp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19992 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_geobox.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4158 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_geoboxtiles.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31468 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_geom.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3831 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_gridspec.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1842 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_map.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9934 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_math.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16129 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_overlap.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4569 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_rgba.py
+-rw-r--r--   0 runner    (1001) docker     (123)      894 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_rioxarray_interop.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10069 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_roi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3547 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)      839 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_ui.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18437 2023-05-13 02:26:44.000000 odc-geo-0.4.0rc1/tests/test_xr_interop.py
```

### Comparing `odc-geo-0.4.0a3/LICENSE` & `odc-geo-0.4.0rc1/LICENSE`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/PKG-INFO` & `odc-geo-0.4.0rc1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: odc-geo
-Version: 0.4.0a3
+Version: 0.4.0rc1
 Summary: Geometry Classes and Operations (opendatacube)
 Home-page: https://github.com/opendatacube/odc-geo/
 Author: Open Data Cube
 Author-email: 
 Maintainer: Open Data Cube
 Maintainer-email: 
 License: Apache License 2.0
```

### Comparing `odc-geo-0.4.0a3/README.rst` & `odc-geo-0.4.0rc1/README.rst`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/__init__.py` & `odc-geo-0.4.0rc1/odc/geo/__init__.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/_blocks.py` & `odc-geo-0.4.0rc1/odc/geo/_blocks.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/_cog.py` & `odc-geo-0.4.0rc1/odc/geo/_cog.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/_compress.py` & `odc-geo-0.4.0rc1/odc/geo/_compress.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/_dask.py` & `odc-geo-0.4.0rc1/odc/geo/_dask.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/_interop.py` & `odc-geo-0.4.0rc1/odc/geo/_interop.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/_map.py` & `odc-geo-0.4.0rc1/odc/geo/_map.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/_rgba.py` & `odc-geo-0.4.0rc1/odc/geo/_rgba.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/_xr_interop.py` & `odc-geo-0.4.0rc1/odc/geo/_xr_interop.py`

 * *Files 2% similar despite different names*

```diff
@@ -28,15 +28,15 @@
 
 from ._interop import have, is_dask_collection
 from ._rgba import colorize, to_rgba
 from .crs import CRS, CRSError, SomeCRS, norm_crs_or_error
 from .gcp import GCPGeoBox, GCPMapping
 from .geobox import Coordinate, GeoBox
 from .geom import Geometry
-from .math import affine_from_axis, resolution_from_affine
+from .math import affine_from_axis, maybe_int, resolution_from_affine
 from .overlap import compute_output_geobox
 from .types import Resolution, xy_
 
 # pylint: disable=import-outside-toplevel
 if have.rasterio:
     from ._cog import to_cog, write_cog
     from ._compress import compress
@@ -545,18 +545,21 @@
 
     assert isinstance(src.odc, ODCExtensionDa)  # for mypy sake
     src_gbox = src.odc.geobox
 
     if src_gbox is None or src_gbox.crs is None:
         raise ValueError("Can not reproject non-georegistered array.")
 
+    resolution = kw.pop("resolution", "auto")
+    tight = kw.pop("tight", False)
+
     if isinstance(how, GeoBox):
         dst_geobox = how
     else:
-        dst_geobox = src.odc.output_geobox(how)
+        dst_geobox = src.odc.output_geobox(how, resolution=resolution, tight=tight)
 
     # compute destination shape by replacing spatial dimensions shape
     ydim = src.odc.ydim
     assert ydim + 1 == src.odc.xdim
     dst_shape = (*src.shape[:ydim], *dst_geobox.shape, *src.shape[ydim + 2 :])
 
     src_nodata = kw.pop("src_nodata", None)
@@ -594,15 +597,15 @@
         )
 
     attrs = {k: v for k, v in src.attrs.items() if k not in SPATIAL_ATTRIBUTES}
     if dst_nodata is None:
         attrs.pop("nodata", None)
         attrs.pop("_FillValue", None)
     else:
-        attrs.update(nodata=dst_nodata)
+        attrs.update(nodata=maybe_int(dst_nodata, 1e-6))
 
     # new set of coords (replace x,y dims)
     sdims = src.odc.spatial_dims
     assert sdims is not None
     coords = dict((k, v) for k, v in src.coords.items() if k not in sdims)
     coords.update(xr_coords(dst_geobox))
```

### Comparing `odc-geo-0.4.0a3/odc/geo/converters.py` & `odc-geo-0.4.0rc1/odc/geo/converters.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/crs.py` & `odc-geo-0.4.0rc1/odc/geo/crs.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/data/__init__.py` & `odc-geo-0.4.0rc1/odc/geo/data/__init__.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/data/gbox.css` & `odc-geo-0.4.0rc1/odc/geo/data/gbox.css`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/data/ocean.geojson.xz` & `odc-geo-0.4.0rc1/odc/geo/data/ocean.geojson.xz`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/gcp.py` & `odc-geo-0.4.0rc1/odc/geo/gcp.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/geobox.py` & `odc-geo-0.4.0rc1/odc/geo/geobox.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/geom.py` & `odc-geo-0.4.0rc1/odc/geo/geom.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/gridspec.py` & `odc-geo-0.4.0rc1/odc/geo/gridspec.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/math.py` & `odc-geo-0.4.0rc1/odc/geo/math.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/overlap.py` & `odc-geo-0.4.0rc1/odc/geo/overlap.py`

 * *Files 2% similar despite different names*

```diff
@@ -27,15 +27,15 @@
     NormalizedSlice,
     roi_boundary,
     roi_center,
     roi_from_points,
     roi_is_empty,
     scaled_up_roi,
 )
-from .types import XY, SomeShape, res_, shape_, xy_
+from .types import XY, SomeResolution, SomeShape, res_, shape_, xy_
 
 
 class PointTransform(Protocol):
     """
     Invertible point transform.
     """
 
@@ -552,15 +552,15 @@
     )
 
 
 def compute_output_geobox(
     gbox: Union[GeoBox, GCPGeoBox],
     crs: SomeCRS,
     *,
-    resolution: Literal["auto", "fit", "same"] = "auto",
+    resolution: Union[SomeResolution, Literal["auto", "fit", "same"]] = "auto",
     tight: bool = False,
 ) -> GeoBox:
     """
     Compute output ``GeoBox``.
 
     Find best fitting, axis aligned GeoBox in a different coordinate reference given source
     ``GeoBox`` on input.
@@ -573,14 +573,15 @@
 
     :param resolution:
 
        * "same" use exactly the same resolution as src
        * "fit" use center pixel to determine scale change between the two
        * | "auto" is to use the same resolution on the output if CRS units are the same
          |  between the source and destination and otherwise use "fit"
+       * Else resolution in the units of the output crs
 
     :param tight:
       By default output pixel grid is adjusted to align pixel edges to X/Y axis, suppling
       ``tight=True`` produces unaligned geobox on the output.
 
     :return:
        Similar resolution, axis aligned geobox that fully encloses source one but in a different
@@ -589,14 +590,22 @@
     # pylint: disable=too-many-locals
     src_crs = gbox.crs
     assert src_crs is not None
 
     bbox = gbox.footprint(crs, buffer=0.9, npoints=100).boundingbox
     dst_crs = bbox.crs
     assert dst_crs is not None
+
+    if (
+        dst_crs == src_crs
+        and resolution in ("auto", "same")
+        and isinstance(gbox, GeoBox)
+    ):
+        return gbox
+
     same_units = src_crs.units == dst_crs.units
 
     if resolution == "same":
         res = gbox.resolution
     elif resolution == "auto" and same_units:
         res = gbox.resolution
     elif resolution in ("fit", "auto"):
@@ -613,12 +622,15 @@
         # .. but we want square pixels, so pick average between x and y
         sx, sy = get_scale_at_point(xy_(0.5, 0.5), native_pix_transform(dst_, cp)).xy
 
         # always produces square pixels on output with inverted Y axis
         avg_res = (abs(dst_.resolution.x / sx) + abs(dst_.resolution.y / sy)) / 2
         res = res_(avg_res)
     else:
-        raise ValueError(
-            f"Resolution ought to be one of: same,auto,fit, not '{resolution}'"
-        )
+        if isinstance(resolution, str):
+            raise ValueError(
+                f"Resolution ought to be one of: same,auto,fit, not '{resolution}'"
+            )
+
+        res = res_(resolution)
 
     return GeoBox.from_bbox(bbox, dst_crs, resolution=res, tight=tight)
```

### Comparing `odc-geo-0.4.0a3/odc/geo/roi.py` & `odc-geo-0.4.0rc1/odc/geo/roi.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/testutils.py` & `odc-geo-0.4.0rc1/odc/geo/testutils.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/types.py` & `odc-geo-0.4.0rc1/odc/geo/types.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/ui.py` & `odc-geo-0.4.0rc1/odc/geo/ui.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/warp.py` & `odc-geo-0.4.0rc1/odc/geo/warp.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc/geo/xr.py` & `odc-geo-0.4.0rc1/odc/geo/xr.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/odc_geo.egg-info/PKG-INFO` & `odc-geo-0.4.0rc1/odc_geo.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: odc-geo
-Version: 0.4.0a3
+Version: 0.4.0rc1
 Summary: Geometry Classes and Operations (opendatacube)
 Home-page: https://github.com/opendatacube/odc-geo/
 Author: Open Data Cube
 Author-email: 
 Maintainer: Open Data Cube
 Maintainer-email: 
 License: Apache License 2.0
```

### Comparing `odc-geo-0.4.0a3/odc_geo.egg-info/SOURCES.txt` & `odc-geo-0.4.0rc1/odc_geo.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/pyproject.toml` & `odc-geo-0.4.0rc1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/setup.cfg` & `odc-geo-0.4.0rc1/setup.cfg`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_bbox.py` & `odc-geo-0.4.0rc1/tests/test_bbox.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_blocks.py` & `odc-geo-0.4.0rc1/tests/test_blocks.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_cog.py` & `odc-geo-0.4.0rc1/tests/test_cog.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_converters.py` & `odc-geo-0.4.0rc1/tests/test_converters.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_crs.py` & `odc-geo-0.4.0rc1/tests/test_crs.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_dask_interop.py` & `odc-geo-0.4.0rc1/tests/test_dask_interop.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_datasets.py` & `odc-geo-0.4.0rc1/tests/test_datasets.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_gbox_ops.py` & `odc-geo-0.4.0rc1/tests/test_gbox_ops.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_gcp.py` & `odc-geo-0.4.0rc1/tests/test_gcp.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_geobox.py` & `odc-geo-0.4.0rc1/tests/test_geobox.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_geoboxtiles.py` & `odc-geo-0.4.0rc1/tests/test_geoboxtiles.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_geom.py` & `odc-geo-0.4.0rc1/tests/test_geom.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_gridspec.py` & `odc-geo-0.4.0rc1/tests/test_gridspec.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_map.py` & `odc-geo-0.4.0rc1/tests/test_map.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_math.py` & `odc-geo-0.4.0rc1/tests/test_math.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_overlap.py` & `odc-geo-0.4.0rc1/tests/test_overlap.py`

 * *Files 5% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 import math
 from random import uniform
 
 import numpy as np
 import pytest
 from affine import Affine
 
-from odc.geo import CRS, geom, resyx_, wh_, xy_
+from odc.geo import CRS, geom, res_, resyx_, wh_, xy_
 from odc.geo.geobox import GeoBox, scaled_down_geobox
 from odc.geo.gridspec import GridSpec
 from odc.geo.math import affine_from_pts, decompose_rws, is_affine_st, stack_xy
 from odc.geo.overlap import (
     LinearPointTransform,
     ReprojectInfo,
     _can_paste,
@@ -461,14 +461,25 @@
     # force estimation of new resolution
     dst = compute_output_geobox(src, "epsg:6933", resolution="fit")
     assert dst.crs == "epsg:6933"
     assert dst.resolution != src.resolution
     assert dst.resolution.x == -dst.resolution.y
     assert dst.geographic_extent.contains(src.geographic_extent)
 
+    # force specific resolution
+    dst = compute_output_geobox(src, "epsg:6933", resolution=101)
+    assert dst.crs == "epsg:6933"
+    assert dst.resolution == res_(101)
+    assert dst.geographic_extent.contains(src.geographic_extent)
+
+    # check identity case
+    assert src is compute_output_geobox(src, src.crs)
+    assert src is compute_output_geobox(src, src.crs, resolution="same")
+    assert src is compute_output_geobox(src, src.crs, resolution="auto")
+
     # check conversion to lon/lat
     dst = compute_output_geobox(src, "epsg:4326")
     assert dst.crs == "epsg:4326"
     assert dst.resolution != src.resolution
     assert dst.resolution.x == -dst.resolution.y
     assert dst.geographic_extent.contains(src.geographic_extent)
     npix_change = (src.shape[0] * src.shape[1]) / (dst.shape[0] * dst.shape[1])
```

### Comparing `odc-geo-0.4.0a3/tests/test_rgba.py` & `odc-geo-0.4.0rc1/tests/test_rgba.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_rioxarray_interop.py` & `odc-geo-0.4.0rc1/tests/test_rioxarray_interop.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_roi.py` & `odc-geo-0.4.0rc1/tests/test_roi.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_types.py` & `odc-geo-0.4.0rc1/tests/test_types.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_ui.py` & `odc-geo-0.4.0rc1/tests/test_ui.py`

 * *Files identical despite different names*

### Comparing `odc-geo-0.4.0a3/tests/test_xr_interop.py` & `odc-geo-0.4.0rc1/tests/test_xr_interop.py`

 * *Files identical despite different names*

