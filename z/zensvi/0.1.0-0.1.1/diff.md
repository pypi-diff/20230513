# Comparing `tmp/zensvi-0.1.0.tar.gz` & `tmp/zensvi-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zensvi-0.1.0.tar", max compression
+gzip compressed data, was "zensvi-0.1.1.tar", max compression
```

## Comparing `zensvi-0.1.0.tar` & `zensvi-0.1.1.tar`

### file list

```diff
@@ -1,19 +1,19 @@
--rwxr-xr-x   0        0        0     1072 2023-05-10 07:40:35.070000 zensvi-0.1.0/LICENSE
--rwxr-xr-x   0        0        0      669 2023-05-10 08:45:06.029273 zensvi-0.1.0/README.md
--rwxr-xr-x   0        0        0      678 2023-05-12 09:44:23.434823 zensvi-0.1.0/pyproject.toml
--rwxr-xr-x   0        0        0      131 2023-05-10 08:45:06.034573 zensvi-0.1.0/src/zensvi/__init__.py
--rwxr-xr-x   0        0        0       27 2023-05-10 08:45:06.034772 zensvi-0.1.0/src/zensvi/cv/__init__.py
--rwxr-xr-x   0        0        0       27 2023-05-10 08:45:06.034938 zensvi-0.1.0/src/zensvi/cv/segmentation/__init__.py
--rwxr-xr-x   0        0        0    38123 2023-05-10 08:45:06.035269 zensvi-0.1.0/src/zensvi/cv/segmentation/segmentation.py
--rwxr-xr-x   0        0        0       55 2023-05-10 08:45:06.035499 zensvi-0.1.0/src/zensvi/download/__init__.py
--rwxr-xr-x   0        0        0    12210 2023-05-12 09:26:45.990826 zensvi-0.1.0/src/zensvi/download/streetview_downloader.py
--rwxr-xr-x   0        0        0   316244 2023-05-10 08:45:06.037620 zensvi-0.1.0/src/zensvi/download/utils/UserAgent.csv
--rwxr-xr-x   0        0        0        0 2023-05-10 08:45:06.037726 zensvi-0.1.0/src/zensvi/download/utils/__init__.py
--rwxr-xr-x   0        0        0     7705 2023-05-12 09:26:45.991456 zensvi-0.1.0/src/zensvi/download/utils/geoprocess.py
--rwxr-xr-x   0        0        0     1730 2023-05-10 08:45:06.038142 zensvi-0.1.0/src/zensvi/download/utils/get_pids.py
--rwxr-xr-x   0        0        0      956 2023-05-10 08:45:06.038300 zensvi-0.1.0/src/zensvi/download/utils/helpers.py
--rwxr-xr-x   0        0        0     7161 2023-05-11 09:20:45.913523 zensvi-0.1.0/src/zensvi/download/utils/imtool.py
--rwxr-xr-x   0        0        0       30 2023-05-10 08:45:06.038720 zensvi-0.1.0/src/zensvi/transform/__init__.py
--rwxr-xr-x   0        0        0     6500 2023-05-10 08:45:06.038914 zensvi-0.1.0/src/zensvi/transform/transform_image.py
--rwxr-xr-x   0        0        0        0 2023-05-10 08:45:06.038961 zensvi-0.1.0/src/zensvi/zensvi.py
--rw-r--r--   0        0        0     1753 1970-01-01 00:00:00.000000 zensvi-0.1.0/PKG-INFO
+-rwxr-xr-x   0        0        0     1072 2023-05-10 07:40:35.070000 zensvi-0.1.1/LICENSE
+-rwxr-xr-x   0        0        0      669 2023-05-10 08:45:06.029273 zensvi-0.1.1/README.md
+-rwxr-xr-x   0        0        0      678 2023-05-13 01:40:21.877470 zensvi-0.1.1/pyproject.toml
+-rwxr-xr-x   0        0        0      131 2023-05-10 08:45:06.034573 zensvi-0.1.1/src/zensvi/__init__.py
+-rwxr-xr-x   0        0        0       27 2023-05-10 08:45:06.034772 zensvi-0.1.1/src/zensvi/cv/__init__.py
+-rwxr-xr-x   0        0        0       27 2023-05-10 08:45:06.034938 zensvi-0.1.1/src/zensvi/cv/segmentation/__init__.py
+-rwxr-xr-x   0        0        0    38123 2023-05-10 08:45:06.035269 zensvi-0.1.1/src/zensvi/cv/segmentation/segmentation.py
+-rwxr-xr-x   0        0        0       55 2023-05-10 08:45:06.035499 zensvi-0.1.1/src/zensvi/download/__init__.py
+-rwxr-xr-x   0        0        0    12110 2023-05-12 09:55:42.348324 zensvi-0.1.1/src/zensvi/download/streetview_downloader.py
+-rwxr-xr-x   0        0        0   316244 2023-05-10 08:45:06.037620 zensvi-0.1.1/src/zensvi/download/utils/UserAgent.csv
+-rwxr-xr-x   0        0        0        0 2023-05-10 08:45:06.037726 zensvi-0.1.1/src/zensvi/download/utils/__init__.py
+-rwxr-xr-x   0        0        0     8366 2023-05-13 01:37:08.893361 zensvi-0.1.1/src/zensvi/download/utils/geoprocess.py
+-rwxr-xr-x   0        0        0     1730 2023-05-10 08:45:06.038142 zensvi-0.1.1/src/zensvi/download/utils/get_pids.py
+-rwxr-xr-x   0        0        0      956 2023-05-10 08:45:06.038300 zensvi-0.1.1/src/zensvi/download/utils/helpers.py
+-rwxr-xr-x   0        0        0     7161 2023-05-11 09:20:45.913523 zensvi-0.1.1/src/zensvi/download/utils/imtool.py
+-rwxr-xr-x   0        0        0       30 2023-05-10 08:45:06.038720 zensvi-0.1.1/src/zensvi/transform/__init__.py
+-rwxr-xr-x   0        0        0     6500 2023-05-10 08:45:06.038914 zensvi-0.1.1/src/zensvi/transform/transform_image.py
+-rwxr-xr-x   0        0        0        0 2023-05-10 08:45:06.038961 zensvi-0.1.1/src/zensvi/zensvi.py
+-rw-r--r--   0        0        0     1753 1970-01-01 00:00:00.000000 zensvi-0.1.1/PKG-INFO
```

### Comparing `zensvi-0.1.0/LICENSE` & `zensvi-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `zensvi-0.1.0/README.md` & `zensvi-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `zensvi-0.1.0/pyproject.toml` & `zensvi-0.1.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "zensvi"
-version = "0.1.0"
+version = "0.1.1"
 description = "This package handles downloading, cleaning, analyzing street view imagery in one-stop and zen manner."
 authors = ["koito19960406"]
 license = "MIT"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.9"
```

### Comparing `zensvi-0.1.0/src/zensvi/cv/segmentation/segmentation.py` & `zensvi-0.1.1/src/zensvi/cv/segmentation/segmentation.py`

 * *Files identical despite different names*

### Comparing `zensvi-0.1.0/src/zensvi/download/streetview_downloader.py` & `zensvi-0.1.1/src/zensvi/download/streetview_downloader.py`

 * *Files 2% similar despite different names*

```diff
@@ -277,21 +277,19 @@
         # cropped = False
         # full = True
         # create a folder within self.dir_output
         panorama_output = os.path.join(self.dir_output, "panorama")
         os.makedirs(panorama_output, exist_ok=True)
         
         panoids = self._read_pids(path_pid)
-        panoids_rest = self._check_already(panoids)
 
-        panoids = self._read_pids(path_pid)
-        if len(panoids_rest) > 0:
-            panoids_rest = self._check_already(panoids)
-        else:
+        if len(panoids) == 0:
             print("There is no panorama ID to download.")
             return
+        else:
+            panoids_rest = self._check_already(panoids)
 
         if len(panoids_rest) > 0:
             UAs = random.choices(self.user_agent, k = len(panoids_rest))
             ImageTool.dwl_multiple(panoids_rest, zoom, v_tiles, h_tiles, panorama_output, UAs, cropped, full, log_path=self.log_path)
         else:
             print("All images have been downloaded.")
```

### Comparing `zensvi-0.1.0/src/zensvi/download/utils/UserAgent.csv` & `zensvi-0.1.1/src/zensvi/download/utils/UserAgent.csv`

 * *Files identical despite different names*

### Comparing `zensvi-0.1.0/src/zensvi/download/utils/geoprocess.py` & `zensvi-0.1.1/src/zensvi/download/utils/geoprocess.py`

 * *Files 19% similar despite different names*

```diff
@@ -133,35 +133,49 @@
                 if self.grid == False:
                     future = executor.submit(self.get_street_points, geom)
                 else:
                     future = executor.submit(self.create_point_grid, geom, self.grid_size)
                 future_to_geom[future] = geom
 
             results = []
+            failed_geoms = []
             for future in tqdm(as_completed(future_to_geom.keys()), total=len(gdf), desc="Processing Polygons"):
                 # Retrieve the corresponding geom for each future
                 geom = future_to_geom[future]
                 try:
                     result = future.result()
                     results.append(result)
                 except (ValueError, networkx.exception.NetworkXPointlessConcept):
-                    tqdm.write("Found no graph nodes within the polygon or connectivity is undefined for the null graph, switching to grid creation.")
+                    tqdm.write("Found no graph nodes within the polygon or connectivity is undefined for the null graph. Store the polygon as a failed geom and retry later")
+                    failed_geoms.append(geom)
+                    
+            if len(failed_geoms) > 0:
+                print("Retrying failed geoms")
+                # resubmitting failed geoms
+                future_to_geom_retry = {}
+                for geom in tqdm(failed_geoms, desc="Preparing Failed Geoms"):
                     future = executor.submit(self.create_point_grid, geom, self.grid_size)
+                    future_to_geom_retry[future] = geom
+
+                for future in tqdm(as_completed(future_to_geom_retry.keys()), total=len(failed_geoms), desc="Processing Failed Geoms"):
+                    # No need to catch exceptions here because we're already in the retry block
                     result = future.result()
                     results.append(result)
 
             gdf['street_points'] = [result[0] for result in results]
             self.utm_crs = results[0][1]
 
         gdf = gdf.explode('street_points').reset_index(drop=True)
 
         # Convert the UTM points to latitude and longitude
         gdf['longitude'], gdf['latitude'] = zip(*self.utm_to_lat_lon(gdf['street_points'].tolist(), self.utm_crs))
 
         return gdf[self.id_columns + ['longitude', 'latitude']]
 
+
+
     def process_multipolygon(self, gdf):
         # Explode the multipolygon into individual polygons
         gdf = gdf.explode('geometry').reset_index(drop=True)
 
         # Call process_polygon on the exploded GeoDataFrame
         return self.process_polygon(gdf)
```

### Comparing `zensvi-0.1.0/src/zensvi/download/utils/get_pids.py` & `zensvi-0.1.1/src/zensvi/download/utils/get_pids.py`

 * *Files identical despite different names*

### Comparing `zensvi-0.1.0/src/zensvi/download/utils/helpers.py` & `zensvi-0.1.1/src/zensvi/download/utils/helpers.py`

 * *Files identical despite different names*

### Comparing `zensvi-0.1.0/src/zensvi/download/utils/imtool.py` & `zensvi-0.1.1/src/zensvi/download/utils/imtool.py`

 * *Files identical despite different names*

### Comparing `zensvi-0.1.0/src/zensvi/transform/transform_image.py` & `zensvi-0.1.1/src/zensvi/transform/transform_image.py`

 * *Files identical despite different names*

### Comparing `zensvi-0.1.0/PKG-INFO` & `zensvi-0.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zensvi
-Version: 0.1.0
+Version: 0.1.1
 Summary: This package handles downloading, cleaning, analyzing street view imagery in one-stop and zen manner.
 License: MIT
 Author: koito19960406
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
```

