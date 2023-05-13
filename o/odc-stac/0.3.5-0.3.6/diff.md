# Comparing `tmp/odc-stac-0.3.5.tar.gz` & `tmp/odc-stac-0.3.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "odc-stac-0.3.5.tar", last modified: Tue Jan 17 22:47:20 2023, max compression
+gzip compressed data, was "odc-stac-0.3.6.tar", last modified: Sat May 13 04:03:05 2023, max compression
```

## Comparing `odc-stac-0.3.5.tar` & `odc-stac-0.3.6.tar`

### file list

```diff
@@ -1,41 +1,51 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-17 22:47:20.633120 odc-stac-0.3.5/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-01-17 22:47:08.000000 odc-stac-0.3.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-01-17 22:47:20.633120 odc-stac-0.3.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3188 2023-01-17 22:47:08.000000 odc-stac-0.3.5/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-17 22:47:20.625120 odc-stac-0.3.5/odc/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-17 22:47:20.629120 odc-stac-0.3.5/odc/stac/
--rw-r--r--   0 runner    (1001) docker     (123)      936 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5834 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_aws.py
--rw-r--r--   0 runner    (1001) docker     (123)     1221 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_dask.py
--rw-r--r--   0 runner    (1001) docker     (123)    26856 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_load.py
--rw-r--r--   0 runner    (1001) docker     (123)    28219 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_mdtools.py
--rw-r--r--   0 runner    (1001) docker     (123)    17411 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     7018 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     7735 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_rio.py
--rw-r--r--   0 runner    (1001) docker     (123)     1048 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)       54 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/_version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-17 22:47:20.629120 odc-stac-0.3.5/odc/stac/bench/
--rw-r--r--   0 runner    (1001) docker     (123)      452 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/bench/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/bench/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6812 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/bench/_cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     2624 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/bench/_prepare.py
--rw-r--r--   0 runner    (1001) docker     (123)     1191 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/bench/_report.py
--rw-r--r--   0 runner    (1001) docker     (123)    15861 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/bench/_run.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-17 22:47:20.629120 odc-stac-0.3.5/odc/stac/eo3/
--rw-r--r--   0 runner    (1001) docker     (123)      200 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/eo3/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10928 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/eo3/_eo3converter.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-17 22:47:20.629120 odc-stac-0.3.5/odc/stac/testing/
--rw-r--r--   0 runner    (1001) docker     (123)       33 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/testing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2018 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/testing/fixtures.py
--rw-r--r--   0 runner    (1001) docker     (123)     4685 2023-01-17 22:47:08.000000 odc-stac-0.3.5/odc/stac/testing/stac.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-17 22:47:20.633120 odc-stac-0.3.5/odc_stac.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-01-17 22:47:20.000000 odc-stac-0.3.5/odc_stac.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      742 2023-01-17 22:47:20.000000 odc-stac-0.3.5/odc_stac.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-01-17 22:47:20.000000 odc-stac-0.3.5/odc_stac.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-01-17 22:47:20.000000 odc-stac-0.3.5/odc_stac.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-01-17 22:47:20.000000 odc-stac-0.3.5/odc_stac.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-01-17 22:47:20.000000 odc-stac-0.3.5/odc_stac.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      454 2023-01-17 22:47:08.000000 odc-stac-0.3.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)     1383 2023-01-17 22:47:20.633120 odc-stac-0.3.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-01-17 22:47:08.000000 odc-stac-0.3.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:03:05.841025 odc-stac-0.3.6/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-05-13 04:02:50.000000 odc-stac-0.3.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-05-13 04:03:05.841025 odc-stac-0.3.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3188 2023-05-13 04:02:50.000000 odc-stac-0.3.6/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:03:05.833025 odc-stac-0.3.6/odc/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:03:05.837026 odc-stac-0.3.6/odc/stac/
+-rw-r--r--   0 runner    (1001) docker     (123)      936 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5834 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_aws.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1221 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_dask.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26856 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_load.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28761 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_mdtools.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17497 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7018 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7735 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_rio.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1048 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)       54 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/_version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:03:05.837026 odc-stac-0.3.6/odc/stac/bench/
+-rw-r--r--   0 runner    (1001) docker     (123)      452 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/bench/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/bench/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6812 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/bench/_cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2624 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/bench/_prepare.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1191 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/bench/_report.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15861 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/bench/_run.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:03:05.837026 odc-stac-0.3.6/odc/stac/eo3/
+-rw-r--r--   0 runner    (1001) docker     (123)      200 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/eo3/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10899 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/eo3/_eo3converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:03:05.837026 odc-stac-0.3.6/odc/stac/testing/
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/testing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2018 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/testing/fixtures.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4683 2023-05-13 04:02:50.000000 odc-stac-0.3.6/odc/stac/testing/stac.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:03:05.837026 odc-stac-0.3.6/odc_stac.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-05-13 04:03:05.000000 odc-stac-0.3.6/odc_stac.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      934 2023-05-13 04:03:05.000000 odc-stac-0.3.6/odc_stac.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 04:03:05.000000 odc-stac-0.3.6/odc_stac.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 04:03:05.000000 odc-stac-0.3.6/odc_stac.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 04:03:05.000000 odc-stac-0.3.6/odc_stac.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-05-13 04:03:05.000000 odc-stac-0.3.6/odc_stac.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      455 2023-05-13 04:02:50.000000 odc-stac-0.3.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)     1383 2023-05-13 04:03:05.841025 odc-stac-0.3.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 04:02:50.000000 odc-stac-0.3.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 04:03:05.841025 odc-stac-0.3.6/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     6850 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_bench.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1229 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_dask.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7665 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_eo3converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7232 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_load.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18107 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_mdtools.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6816 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7538 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)      355 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4623 2023-05-13 04:02:50.000000 odc-stac-0.3.6/tests/test_utils_aws.py
```

### Comparing `odc-stac-0.3.5/LICENSE` & `odc-stac-0.3.6/LICENSE`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/PKG-INFO` & `odc-stac-0.3.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: odc-stac
-Version: 0.3.5
+Version: 0.3.6
 Summary: Tooling for converting STAC metadata to ODC data model
 Home-page: https://github.com/opendatacube/odc-stac/
 Author: Open Data Cube
 Author-email: 
 Maintainer: Open Data Cube
 Maintainer-email: 
 License: Apache License 2.0
```

### Comparing `odc-stac-0.3.5/README.rst` & `odc-stac-0.3.6/README.rst`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/__init__.py` & `odc-stac-0.3.6/odc/stac/__init__.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/_aws.py` & `odc-stac-0.3.6/odc/stac/_aws.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/_dask.py` & `odc-stac-0.3.6/odc/stac/_dask.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/_load.py` & `odc-stac-0.3.6/odc/stac/_load.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/_mdtools.py` & `odc-stac-0.3.6/odc/stac/_mdtools.py`

 * *Files 2% similar despite different names*

```diff
@@ -63,15 +63,35 @@
 
 EPSG4326 = CRS("EPSG:4326")
 
 # Assets with these roles are ignored unless manually requested
 ROLES_THUMBNAIL = {"thumbnail", "overview"}
 
 # Used to detect image assets when media_type is missing
-RASTER_FILE_EXTENSIONS = {"tif", "tiff", "jpeg", "jpg", "jp2", "img"}
+RASTER_FILE_EXTENSIONS = {
+    "tif",
+    "tiff",
+    "jpeg",
+    "jpg",
+    "jp2",
+    "img",
+    "hdf",
+    "nc",
+    "zarr",
+}
+
+# image/* and these media-type are considered to be raster
+NON_IMAGE_RASTER_MEDIA_TYPES = {
+    "application/x-hdf",
+    "application/hdf",
+    "application/x-netcdf",
+    "application/netcdf",
+    "application/x-zarr",
+    "application/zarr",
+}
 
 
 def with_default(v: Optional[T], default_value: T) -> T:
     """
     Replace ``None`` with default value.
 
     :param v: Value that might be None
@@ -203,27 +223,34 @@
     if media_type is None:
         # Type undefined
         #   Look if it has data role
         if "data" in roles:
             return True
         if "metadata" in roles:
             return False
-    elif "image/" in media_type:
+
+        ext = asset.href.split(".")[-1].lower()
+        return ext in RASTER_FILE_EXTENSIONS
+
+    media_type, *_ = media_type.split(";")
+    media_type = media_type.lower()
+
+    if media_type.startswith("image/"):
         # Image:
         #    False -- when thumbnail
         #    True  -- otherwise
         if any(r in roles for r in ROLES_THUMBNAIL):
             return False
         return True
-    else:
-        # Some type that is not `image/*`
-        return False
 
-    ext = asset.href.split(".")[-1].lower()
-    return ext in RASTER_FILE_EXTENSIONS
+    if media_type in NON_IMAGE_RASTER_MEDIA_TYPES:
+        return True
+
+    # some unsupported mime type
+    return False
 
 
 def mk_1x1_geobox(g: Geometry) -> GeoBox:
     """
     Construct 1x1 pixels GeoBox tightly enclosing supplied geometry.
 
     :param geom: Geometry in whatever projection
@@ -300,14 +327,15 @@
     return _group_geoboxes(geoboxes)
 
 
 def _group_geoboxes(
     geoboxes: Dict[str, GeoBox]
 ) -> Tuple[Dict[str, GeoBox], Dict[str, str]]:
     # pylint: disable=too-many-locals
+    assert len(geoboxes) > 0
 
     def gbox_name(geobox: GeoBox) -> str:
         gsd = geobox_gsd(geobox)
         return f"g{gsd:g}"
 
     # GeoBox to list of bands that share same footprint
     grids: Dict[GeoBox, List[str]] = {}
@@ -339,14 +367,17 @@
         for band in bands:
             band2grid[band] = grid_name
 
     return named_grids, band2grid
 
 
 def band2grid_from_gsd(assets: Dict[str, pystac.asset.Asset]) -> Dict[str, str]:
+    if not assets:
+        return {}
+
     grids: Dict[float, List[str]] = {}
     for name, asset in assets.items():
         gsd = asset.common_metadata.gsd
         gsd = 0 if gsd is None else gsd
         gsd_normed = float(f"{gsd:g}")
         grids.setdefault(gsd_normed, []).append(name)
 
@@ -634,29 +665,29 @@
         if grid is not None:
             return grid
         grid = asset_geobox(asset)
         _grids[grid_name] = grid
         return grid
 
     for bk, meta in template.bands.items():
-        asset_name, _ = bk
+        asset_name, band_idx = bk
         asset = _assets.get(asset_name)
         if asset is None:
             continue
 
         grid_name = band2grid.get(asset_name, "default")
         geobox: Optional[GeoBox] = _get_grid(grid_name, asset) if has_proj else None
 
         uri = asset.get_absolute_href()
         if uri is None:
             raise ValueError(
                 f"Can not determine absolute path for band: {asset_name}"
             )  # pragma: no cover (https://github.com/stac-utils/pystac/issues/754)
 
-        bands[bk] = RasterSource(uri=uri, geobox=geobox, meta=meta)
+        bands[bk] = RasterSource(uri=uri, band=band_idx, geobox=geobox, meta=meta)
 
     md = item.common_metadata
     return ParsedItem(
         item.id,
         template,
         bands,
         geometry,
```

### Comparing `odc-stac-0.3.5/odc/stac/_model.py` & `odc-stac-0.3.6/odc/stac/_model.py`

 * *Files 0% similar despite different names*

```diff
@@ -121,15 +121,17 @@
 
             for cn in canon_names:
                 out.setdefault(cn, []).append(alias)
         return out
 
     def _norm_key(self, k: BandKey) -> str:
         asset, idx = k
-        if idx == 1:
+
+        # if single band asset it's just asset name
+        if idx == 1 and (asset, 2) not in self.bands:
             return asset
 
         # if any alias references this key as first choice return that
         for alias, (_k, *_) in self.aliases.items():
             if _k == k:
                 return alias
```

### Comparing `odc-stac-0.3.5/odc/stac/_reader.py` & `odc-stac-0.3.6/odc/stac/_reader.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/_rio.py` & `odc-stac-0.3.6/odc/stac/_rio.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/_utils.py` & `odc-stac-0.3.6/odc/stac/_utils.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/bench/_cli.py` & `odc-stac-0.3.6/odc/stac/bench/_cli.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/bench/_prepare.py` & `odc-stac-0.3.6/odc/stac/bench/_prepare.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/bench/_report.py` & `odc-stac-0.3.6/odc/stac/bench/_report.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/bench/_run.py` & `odc-stac-0.3.6/odc/stac/bench/_run.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/eo3/_eo3converter.py` & `odc-stac-0.3.6/odc/stac/eo3/_eo3converter.py`

 * *Files 2% similar despite different names*

```diff
@@ -76,16 +76,16 @@
             "name": name,
             "dtype": band.data_type,
             "nodata": band.nodata,
             "units": band.unit,
         }
         if aliases is not None:
             doc["aliases"] = aliases
-        if idx > 0:
-            doc["band"] = idx + 1  # one based in datacube
+        if idx > 1:
+            doc["band"] = idx
         return doc
 
     # drop ambigous aliases
     band_aliases = md.band_aliases(unique=True)
     doc = {
         "name": md.name,
         "metadata_type": "eo3",
```

### Comparing `odc-stac-0.3.5/odc/stac/testing/fixtures.py` & `odc-stac-0.3.6/odc/stac/testing/fixtures.py`

 * *Files identical despite different names*

### Comparing `odc-stac-0.3.5/odc/stac/testing/stac.py` & `odc-stac-0.3.6/odc/stac/testing/stac.py`

 * *Files 1% similar despite different names*

```diff
@@ -154,15 +154,15 @@
         assert meta is not None
         return RasterBand.create(
             data_type=meta.data_type,  # type: ignore
             nodata=meta.nodata,
             unit=meta.unit,
         )
 
-    for (asset_name, bands) in item.assets().items():
+    for asset_name, bands in item.assets().items():
         b = bands[0]  # all bands shoudl share same uri
         xx.add_asset(
             asset_name,
             pystac.asset.Asset(b.uri, media_type="image/tiff", roles=["data"]),
         )
         RasterExtension(xx.assets[asset_name]).apply(list(map(_to_raster_band, bands)))
```

### Comparing `odc-stac-0.3.5/odc_stac.egg-info/PKG-INFO` & `odc-stac-0.3.6/odc_stac.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: odc-stac
-Version: 0.3.5
+Version: 0.3.6
 Summary: Tooling for converting STAC metadata to ODC data model
 Home-page: https://github.com/opendatacube/odc-stac/
 Author: Open Data Cube
 Author-email: 
 Maintainer: Open Data Cube
 Maintainer-email: 
 License: Apache License 2.0
```

### Comparing `odc-stac-0.3.5/odc_stac.egg-info/SOURCES.txt` & `odc-stac-0.3.6/odc_stac.egg-info/SOURCES.txt`

 * *Files 25% similar despite different names*

```diff
@@ -26,8 +26,17 @@
 odc/stac/testing/fixtures.py
 odc/stac/testing/stac.py
 odc_stac.egg-info/PKG-INFO
 odc_stac.egg-info/SOURCES.txt
 odc_stac.egg-info/dependency_links.txt
 odc_stac.egg-info/not-zip-safe
 odc_stac.egg-info/requires.txt
-odc_stac.egg-info/top_level.txt
+odc_stac.egg-info/top_level.txt
+tests/test_bench.py
+tests/test_dask.py
+tests/test_eo3converter.py
+tests/test_load.py
+tests/test_mdtools.py
+tests/test_model.py
+tests/test_reader.py
+tests/test_utils.py
+tests/test_utils_aws.py
```

### Comparing `odc-stac-0.3.5/setup.cfg` & `odc-stac-0.3.6/setup.cfg`

 * *Files identical despite different names*

