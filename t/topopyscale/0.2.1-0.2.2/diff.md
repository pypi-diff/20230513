# Comparing `tmp/topopyscale-0.2.1.tar.gz` & `tmp/topopyscale-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "topopyscale-0.2.1.tar", last modified: Tue Mar  7 11:18:00 2023, max compression
+gzip compressed data, was "topopyscale-0.2.2.tar", last modified: Sat May 13 17:28:09 2023, max compression
```

## Comparing `topopyscale-0.2.1.tar` & `topopyscale-0.2.2.tar`

### file list

```diff
@@ -1,42 +1,44 @@
-drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-03-07 11:18:00.676581 topopyscale-0.2.1/
-drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-03-07 11:18:00.668581 topopyscale-0.2.1/.github/
-drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-03-07 11:18:00.668581 topopyscale-0.2.1/.github/workflows/
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      668 2022-11-15 14:35:18.000000 topopyscale-0.2.1/.github/workflows/draft-pdf.yml
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     1082 2022-11-11 15:15:36.000000 topopyscale-0.2.1/.github/workflows/python-publish.yml
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     1866 2021-11-05 08:58:50.000000 topopyscale-0.2.1/.gitignore
-drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-03-07 11:18:00.668581 topopyscale-0.2.1/JOSS/
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)   110899 2022-12-14 14:07:56.000000 topopyscale-0.2.1/JOSS/figure2.png
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    17303 2022-12-16 08:48:45.000000 topopyscale-0.2.1/JOSS/paper.bib
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     8357 2022-12-23 10:22:53.000000 topopyscale-0.2.1/JOSS/paper.md
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)  3156813 2022-12-14 14:07:56.000000 topopyscale-0.2.1/JOSS/temperature_comparison_crop_scaled.jpg
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     1101 2022-11-08 15:22:59.000000 topopyscale-0.2.1/LICENSE
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)       18 2021-08-25 13:16:00.000000 topopyscale-0.2.1/MANIFEST.in
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     7605 2023-03-07 11:18:00.676581 topopyscale-0.2.1/PKG-INFO
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     6507 2023-03-06 16:08:00.000000 topopyscale-0.2.1/README.md
-drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-03-07 11:18:00.676581 topopyscale-0.2.1/TopoPyScale/
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)        0 2021-09-27 15:27:21.000000 topopyscale-0.2.1/TopoPyScale/__init__.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     6428 2022-03-16 13:31:57.000000 topopyscale-0.2.1/TopoPyScale/fetch_dem.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     7016 2022-11-11 15:00:20.000000 topopyscale-0.2.1/TopoPyScale/fetch_era5.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     6150 2023-01-09 17:39:35.000000 topopyscale-0.2.1/TopoPyScale/meteo_util.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      846 2022-02-17 15:07:15.000000 topopyscale-0.2.1/TopoPyScale/precip_orographic.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     3755 2023-02-15 14:57:15.000000 topopyscale-0.2.1/TopoPyScale/solar_geom.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     7786 2023-01-11 18:09:18.000000 topopyscale-0.2.1/TopoPyScale/topo_compare.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    39132 2022-03-17 08:36:58.000000 topopyscale-0.2.1/TopoPyScale/topo_da.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    28681 2023-03-06 16:08:00.000000 topopyscale-0.2.1/TopoPyScale/topo_export.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     8560 2023-01-11 11:16:20.000000 topopyscale-0.2.1/TopoPyScale/topo_obs.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     9784 2022-11-14 12:34:22.000000 topopyscale-0.2.1/TopoPyScale/topo_param.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     3385 2023-01-24 22:23:04.000000 topopyscale-0.2.1/TopoPyScale/topo_plot.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    22691 2023-03-07 11:14:30.000000 topopyscale-0.2.1/TopoPyScale/topo_scale.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    15015 2022-06-24 12:12:44.000000 topopyscale-0.2.1/TopoPyScale/topo_sim.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    12429 2023-02-06 12:58:13.000000 topopyscale-0.2.1/TopoPyScale/topo_sub.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     6658 2023-02-16 14:27:22.000000 topopyscale-0.2.1/TopoPyScale/topo_utils.py
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    34454 2023-03-06 16:08:00.000000 topopyscale-0.2.1/TopoPyScale/topoclass.py
--rw-r--r--   0 simonfi  (264780) simonfi  (231366)    18619 2022-11-10 16:25:16.000000 topopyscale-0.2.1/logo.svg
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      131 2023-03-07 11:18:00.676581 topopyscale-0.2.1/setup.cfg
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     2624 2023-03-07 11:16:27.000000 topopyscale-0.2.1/setup.py
-drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-03-07 11:18:00.676581 topopyscale-0.2.1/topopyscale.egg-info/
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     7605 2023-03-07 11:18:00.000000 topopyscale-0.2.1/topopyscale.egg-info/PKG-INFO
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      839 2023-03-07 11:18:00.000000 topopyscale-0.2.1/topopyscale.egg-info/SOURCES.txt
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)        1 2023-03-07 11:18:00.000000 topopyscale-0.2.1/topopyscale.egg-info/dependency_links.txt
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      130 2023-03-07 11:18:00.000000 topopyscale-0.2.1/topopyscale.egg-info/requires.txt
--rw-rw-r--   0 simonfi  (264780) simonfi  (231366)       12 2023-03-07 11:18:00.000000 topopyscale-0.2.1/topopyscale.egg-info/top_level.txt
+drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-05-13 17:28:09.409811 topopyscale-0.2.2/
+drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-05-13 17:28:09.401811 topopyscale-0.2.2/.github/
+drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-05-13 17:28:09.405811 topopyscale-0.2.2/.github/workflows/
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      737 2023-05-12 08:59:46.000000 topopyscale-0.2.2/.github/workflows/draft-pdf.yml
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     1082 2022-11-11 15:15:36.000000 topopyscale-0.2.2/.github/workflows/python-publish.yml
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     1435 2023-05-12 14:15:58.000000 topopyscale-0.2.2/.github/workflows/test_topopyscale.yml
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     1866 2021-11-05 08:58:50.000000 topopyscale-0.2.2/.gitignore
+drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-05-13 17:28:09.405811 topopyscale-0.2.2/JOSS/
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)   110899 2022-12-14 14:07:56.000000 topopyscale-0.2.2/JOSS/figure2.png
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    17303 2022-12-16 08:48:45.000000 topopyscale-0.2.2/JOSS/paper.bib
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     8357 2022-12-23 10:22:53.000000 topopyscale-0.2.2/JOSS/paper.md
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)  3156813 2022-12-14 14:07:56.000000 topopyscale-0.2.2/JOSS/temperature_comparison_crop_scaled.jpg
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     1101 2022-11-08 15:22:59.000000 topopyscale-0.2.2/LICENSE
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)       18 2021-08-25 13:16:00.000000 topopyscale-0.2.2/MANIFEST.in
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     8175 2023-05-13 17:28:09.409811 topopyscale-0.2.2/PKG-INFO
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     7077 2023-05-12 08:59:46.000000 topopyscale-0.2.2/README.md
+drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-05-13 17:28:09.409811 topopyscale-0.2.2/TopoPyScale/
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)        0 2021-09-27 15:27:21.000000 topopyscale-0.2.2/TopoPyScale/__init__.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     6428 2022-03-16 13:31:57.000000 topopyscale-0.2.2/TopoPyScale/fetch_dem.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    11239 2023-03-20 11:33:37.000000 topopyscale-0.2.2/TopoPyScale/fetch_era5.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     6256 2023-05-05 07:46:03.000000 topopyscale-0.2.2/TopoPyScale/meteo_util.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      846 2022-02-17 15:07:15.000000 topopyscale-0.2.2/TopoPyScale/precip_orographic.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     3761 2023-05-11 09:47:51.000000 topopyscale-0.2.2/TopoPyScale/solar_geom.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     7786 2023-01-11 18:09:18.000000 topopyscale-0.2.2/TopoPyScale/topo_compare.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    39212 2023-05-11 15:47:15.000000 topopyscale-0.2.2/TopoPyScale/topo_da.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    28688 2023-05-11 15:52:16.000000 topopyscale-0.2.2/TopoPyScale/topo_export.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     8560 2023-01-11 11:16:20.000000 topopyscale-0.2.2/TopoPyScale/topo_obs.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     9814 2023-05-11 09:47:51.000000 topopyscale-0.2.2/TopoPyScale/topo_param.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     3733 2023-05-13 17:13:41.000000 topopyscale-0.2.2/TopoPyScale/topo_plot.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    24323 2023-05-12 14:43:18.000000 topopyscale-0.2.2/TopoPyScale/topo_scale.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    24569 2023-05-12 12:48:57.000000 topopyscale-0.2.2/TopoPyScale/topo_sim.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    12429 2023-02-06 12:58:13.000000 topopyscale-0.2.2/TopoPyScale/topo_sub.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     6756 2023-05-11 16:13:13.000000 topopyscale-0.2.2/TopoPyScale/topo_utils.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)    35685 2023-05-13 15:51:40.000000 topopyscale-0.2.2/TopoPyScale/topoclass.py
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     6102 2023-05-11 15:58:03.000000 topopyscale-0.2.2/environment.yml
+-rw-r--r--   0 simonfi  (264780) simonfi  (231366)    18619 2022-11-10 16:25:16.000000 topopyscale-0.2.2/logo.svg
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      131 2023-05-13 17:28:09.409811 topopyscale-0.2.2/setup.cfg
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     2624 2023-05-13 17:17:38.000000 topopyscale-0.2.2/setup.py
+drwxrwxr-x   0 simonfi  (264780) simonfi  (231366)        0 2023-05-13 17:28:09.409811 topopyscale-0.2.2/topopyscale.egg-info/
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)     8175 2023-05-13 17:28:09.000000 topopyscale-0.2.2/topopyscale.egg-info/PKG-INFO
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      894 2023-05-13 17:28:09.000000 topopyscale-0.2.2/topopyscale.egg-info/SOURCES.txt
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)        1 2023-05-13 17:28:09.000000 topopyscale-0.2.2/topopyscale.egg-info/dependency_links.txt
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)      130 2023-05-13 17:28:09.000000 topopyscale-0.2.2/topopyscale.egg-info/requires.txt
+-rw-rw-r--   0 simonfi  (264780) simonfi  (231366)       12 2023-05-13 17:28:09.000000 topopyscale-0.2.2/topopyscale.egg-info/top_level.txt
```

### Comparing `topopyscale-0.2.1/.github/workflows/python-publish.yml` & `topopyscale-0.2.2/.github/workflows/python-publish.yml`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/.gitignore` & `topopyscale-0.2.2/.gitignore`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/JOSS/figure2.png` & `topopyscale-0.2.2/JOSS/figure2.png`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/JOSS/paper.bib` & `topopyscale-0.2.2/JOSS/paper.bib`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/JOSS/paper.md` & `topopyscale-0.2.2/JOSS/paper.md`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/JOSS/temperature_comparison_crop_scaled.jpg` & `topopyscale-0.2.2/JOSS/temperature_comparison_crop_scaled.jpg`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/LICENSE` & `topopyscale-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/PKG-INFO` & `topopyscale-0.2.2/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: topopyscale
-Version: 0.2.1
+Version: 0.2.2
 Summary: A Python package to perform climate downscaling at the hillslope scale
 Home-page: https://github.com/ArcticSnow/TopoPyScale
 Download-URL: https://github.com/ArcticSnow/TopoPyScale/releases/latest
 Author: ['Simon Filhol', 'Joel Fiddes', 'Kristoffer Aalstad']
 Author-email: simon.filhol@geo.uio.no
 License: MIT
 Project-URL: Documentation, https://topopyscale.readthedocs.io/en/latest/
@@ -13,25 +13,30 @@
 Keywords: climate,downscaling,meteorology,xarray
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Science/Research
 Classifier: Topic :: Scientific/Engineering :: Visualization
 Classifier: Topic :: Scientific/Engineering :: Hydrology
 Classifier: Topic :: Scientific/Engineering :: Atmospheric Science
 Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 
 
 [![DOI](https://zenodo.org/badge/411249045.svg)](https://zenodo.org/badge/latestdoi/411249045)
 [![GitHub license](https://img.shields.io/github/license/ArcticSnow/TopoPyScale)](https://github.com/ArcticSnow/TopoPyScale/blob/main/LICENSE)
 ![GitHub release (latest by date)](https://img.shields.io/github/v/release/ArcticSnow/TopoPyScale)
 <a href="https://joss.theoj.org/papers/91621581b2d0c097495fdd1e58179e87"><img src="https://joss.theoj.org/papers/91621581b2d0c097495fdd1e58179e87/status.svg"></a>
+[![][docs-dev-img]][docs-dev-url]
+![Test](https://github.com/ArcticSnow/TopoPyScale/actions/workflows/test_topopyscale.yml/badge.svg)
+
+[docs-dev-img]: https://img.shields.io/badge/docs-latest-blue.svg
+[docs-dev-url]: https://topopyscale.readthedocs.io
 
 # TopoPyScale
 Python version of Toposcale packaged as a Pypi library. Toposcale is an original idea of Joel Fiddes to perform topography-based downscaling of climate data to the hillslope scale.
 
 Documentation avalaible: https://topopyscale.readthedocs.io
 
 ![](https://github.com/ArcticSnow/TopoPyScale/blob/main/JOSS/temperature_comparison_crop_scaled.jpg)
@@ -41,33 +46,29 @@
 - Fiddes, J. and Gruber, S.: TopoSUB: a tool for efficient large area numerical modelling in complex topography at sub-grid scales, Geosci. Model Dev., 5, 1245–1257, https://doi.org/10.5194/gmd-5-1245-2012, 2012. 
 
 Kristoffer Aalstad has a Matlab implementation: https://github.com/krisaalstad/TopoLAB
 
 ## Contribution Workflow
 **Please follow these simple rules:**
 1. a bug -> fix it! 
-2. an idea or a bug you cannot fix? -> create a new [issue](https://github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one exist, then add material to tit.
-3. wanna develop a new feature/idea? -> create a new branch. Do the development. Merge with main branch when accomplished.
-4. Create release version when significant improvements and bug fixes have been done. Coordinate with others
+2. an idea or a bug you cannot fix? -> create a new [issue](https://github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one exist, then add material to it.
+3. wanna develop a new feature/idea? -> create a new branch. Go wild. Merge with main branch when accomplished.
+4. Create release version when significant improvements and bug fixes have been done. Coordinate with others on [Discussions](https://github.com/ArcticSnow/TopoPyScale/discussions)
 
 **Create a new release:**
 Follow procedure and conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY
 
-And check out our Slack: tscaleworkspace.slack.com
+Our forum is now on [Github Discussions](https://github.com/ArcticSnow/TopoPyScale/discussions). Come visit!
 
-Contributors to the current version (2021) are:
-- Simon Filhol
-- Joel Fiddes
-- Kristoffer Aalstad
 
 ## Design
 
 1. Inputs
     - Climate data from reanalysis (ERA5, etc)
-    - Climate data from future projections (CORDEX) (not avail.)
+    - Climate data from future projections (CORDEX) (TBD)
     - DEM from local source, or fetch from public repository: SRTM, ArcticDEM, ASTER
 2. Run TopoScale
     - compute derived values (from DEM)
     - toposcale (k-mean clustering)
     - interpolation (bilinear, inverse square dist.)
 3. Output
     - Cryogrid format
@@ -76,27 +77,37 @@
     - Snowmodel format
     - basic netcfd
     - For each method, have the choice to output either the abstract cluster points, or the gridded product after interpolation
 4. Validation toolset
     - validation to local observation timeseries
     - plotting
 5. Gap filling algorithm
-    - random forest temporal gap filling
+    - random forest temporal gap filling (TBD)
 
 Validation (4) and Gap filling (4) are future implementation.
 
 ## Installation
 
+We have now added an environments.yml file to handle versions of depencencies that are tested with the current codebase, to use this run:
+
+`conda env create -f environment.yml`
+
+Alternatively you can follow this method for dependencies (to be deprecated):
+
 ```bash
-conda create -n downscaling python=3.8 ipython
+conda create -n downscaling python=3.9 ipython
 conda activate downscaling
 
 # Recomended way to install dependencies:
-conda install -c conda-forge xarray matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask
+conda install -c conda-forge xarray matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask rioxarray
+```
+
+Then install the code:
 
+```
 # OPTION 1 (Pypi release):
 pip install TopoPyScale
 
 # OPTION 2 (development):
 cd github  # navigate to where you want to clone TopoPyScale
 git clone git@github.com:ArcticSnow/TopoPyScale.git
 pip install -e TopoPyScale    #install a development version
```

#### html2text {}

```diff
@@ -1,85 +1,93 @@
-Metadata-Version: 2.1 Name: topopyscale Version: 0.2.1 Summary: A Python
+Metadata-Version: 2.1 Name: topopyscale Version: 0.2.2 Summary: A Python
 package to perform climate downscaling at the hillslope scale Home-page: https:
 //github.com/ArcticSnow/TopoPyScale Download-URL: https://github.com/
 ArcticSnow/TopoPyScale/releases/latest Author: ['Simon Filhol', 'Joel Fiddes',
 'Kristoffer Aalstad'] Author-email: simon.filhol@geo.uio.no License: MIT
 Project-URL: Documentation, https://topopyscale.readthedocs.io/en/latest/
 Project-URL: Source, https://github.com/ArcticSnow/TopoPyScale Project-URL:
 Examples, https://github.com/ArcticSnow/TopoPyScale_examples Keywords:
 climate,downscaling,meteorology,xarray Classifier: Development Status :: 4 -
 Beta Classifier: Intended Audience :: Science/Research Classifier: Topic ::
 Scientific/Engineering :: Visualization Classifier: Topic :: Scientific/
 Engineering :: Hydrology Classifier: Topic :: Scientific/Engineering ::
 Atmospheric Science Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.8 Requires-Python: >=3.8
+Classifier: Programming Language :: Python :: 3.9 Requires-Python: >=3.8
 Description-Content-Type: text/markdown License-File: LICENSE [![DOI](https://
 zenodo.org/badge/411249045.svg)](https://zenodo.org/badge/latestdoi/411249045)
 [![GitHub license](https://img.shields.io/github/license/ArcticSnow/
 TopoPyScale)](https://github.com/ArcticSnow/TopoPyScale/blob/main/LICENSE) !
 [GitHub release (latest by date)](https://img.shields.io/github/v/release/
 ArcticSnow/TopoPyScale) [https://joss.theoj.org/papers/
-91621581b2d0c097495fdd1e58179e87/status.svg] # TopoPyScale Python version of
-Toposcale packaged as a Pypi library. Toposcale is an original idea of Joel
-Fiddes to perform topography-based downscaling of climate data to the hillslope
-scale. Documentation avalaible: https://topopyscale.readthedocs.io ![](https://
-github.com/ArcticSnow/TopoPyScale/blob/main/JOSS/
-temperature_comparison_crop_scaled.jpg) **References:** - Fiddes, J. and
-Gruber, S.: TopoSCALE v.1.0: downscaling gridded climate data in complex
+91621581b2d0c097495fdd1e58179e87/status.svg] [![][docs-dev-img]][docs-dev-url]
+![Test](https://github.com/ArcticSnow/TopoPyScale/actions/workflows/
+test_topopyscale.yml/badge.svg) [docs-dev-img]: https://img.shields.io/badge/
+docs-latest-blue.svg [docs-dev-url]: https://topopyscale.readthedocs.io #
+TopoPyScale Python version of Toposcale packaged as a Pypi library. Toposcale
+is an original idea of Joel Fiddes to perform topography-based downscaling of
+climate data to the hillslope scale. Documentation avalaible: https://
+topopyscale.readthedocs.io ![](https://github.com/ArcticSnow/TopoPyScale/blob/
+main/JOSS/temperature_comparison_crop_scaled.jpg) **References:** - Fiddes, J.
+and Gruber, S.: TopoSCALE v.1.0: downscaling gridded climate data in complex
 terrain, Geosci. Model Dev., 7, 387â405, https://doi.org/10.5194/gmd-7-387-
 2014, 2014. - Fiddes, J. and Gruber, S.: TopoSUB: a tool for efficient large
 area numerical modelling in complex topography at sub-grid scales, Geosci.
 Model Dev., 5, 1245â1257, https://doi.org/10.5194/gmd-5-1245-2012, 2012.
 Kristoffer Aalstad has a Matlab implementation: https://github.com/krisaalstad/
 TopoLAB ## Contribution Workflow **Please follow these simple rules:** 1. a bug
 -> fix it! 2. an idea or a bug you cannot fix? -> create a new [issue](https://
 github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one
-exist, then add material to tit. 3. wanna develop a new feature/idea? -> create
-a new branch. Do the development. Merge with main branch when accomplished. 4.
-Create release version when significant improvements and bug fixes have been
-done. Coordinate with others **Create a new release:** Follow procedure and
-conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY And check
-out our Slack: tscaleworkspace.slack.com Contributors to the current version
-(2021) are: - Simon Filhol - Joel Fiddes - Kristoffer Aalstad ## Design 1.
-Inputs - Climate data from reanalysis (ERA5, etc) - Climate data from future
-projections (CORDEX) (not avail.) - DEM from local source, or fetch from public
-repository: SRTM, ArcticDEM, ASTER 2. Run TopoScale - compute derived values
-(from DEM) - toposcale (k-mean clustering) - interpolation (bilinear, inverse
-square dist.) 3. Output - Cryogrid format - FSM format - CROCUS format -
-Snowmodel format - basic netcfd - For each method, have the choice to output
-either the abstract cluster points, or the gridded product after interpolation
-4. Validation toolset - validation to local observation timeseries - plotting
-5. Gap filling algorithm - random forest temporal gap filling Validation (4)
-and Gap filling (4) are future implementation. ## Installation ```bash conda
-create -n downscaling python=3.8 ipython conda activate downscaling #
-Recomended way to install dependencies: conda install -c conda-forge xarray
-matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask #
-OPTION 1 (Pypi release): pip install TopoPyScale # OPTION 2 (development): cd
-github # navigate to where you want to clone TopoPyScale git clone
-git@github.com:ArcticSnow/TopoPyScale.git pip install -e TopoPyScale #install a
-development version #---------------------------------------------------------
-- # OPTIONAL: if using jupyter lab # add this new Python kernel to your jupyter
-lab PATH python -m ipykernel install --user --name downscaling # Tool for
-generating documentation from code docstring pip install lazydocs ``` Then you
-need to setup your `cdsapi` with the Copernicus API key system. Follow [this
-tutorial](https://cds.climate.copernicus.eu/api-how-to#install-the-cds-api-key)
-after creating an account with [Copernicus](https://cds.climate.copernicus.eu/
-). On Linux, create a file `nano ~/.cdsapirc` with inside: ``` url: https://
-cds.climate.copernicus.eu/api/v2 key: {uid}:{api-key} ``` ## Basic usage 1.
-Setup your Python environment 2. Create your project directory 3. Configure the
-file `config.ini` to fit your problem (see [`config.yml`](https://github.com/
-ArcticSnow/TopoPyScale_examples/blob/main/ex1_norway_finse/config_spatial.yml)
-for an example) 4. Run TopoPyScale ```python import pandas as pd from
-TopoPyScale import topoclass as tc from matplotlib import pyplot as plt #
-========= STEP 1 ========== # Load Configuration config_file = './config.yml'
-mp = tc.Topoclass(config_file) # Compute parameters of the DEM (slope, aspect,
-sky view factor) mp.compute_dem_param() # ========== STEP 2 =========== #
-Extract DEM parameters for points of interest (centroids or physical points)
-mp.extract_topo_param() # ----- Option 1: # Compute clustering of the input DEM
-and extract cluster centroids #mp.extract_dem_cluster_param() # plot clusters
+exist, then add material to it. 3. wanna develop a new feature/idea? -> create
+a new branch. Go wild. Merge with main branch when accomplished. 4. Create
+release version when significant improvements and bug fixes have been done.
+Coordinate with others on [Discussions](https://github.com/ArcticSnow/
+TopoPyScale/discussions) **Create a new release:** Follow procedure and
+conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY Our forum
+is now on [Github Discussions](https://github.com/ArcticSnow/TopoPyScale/
+discussions). Come visit! ## Design 1. Inputs - Climate data from reanalysis
+(ERA5, etc) - Climate data from future projections (CORDEX) (TBD) - DEM from
+local source, or fetch from public repository: SRTM, ArcticDEM, ASTER 2. Run
+TopoScale - compute derived values (from DEM) - toposcale (k-mean clustering) -
+interpolation (bilinear, inverse square dist.) 3. Output - Cryogrid format -
+FSM format - CROCUS format - Snowmodel format - basic netcfd - For each method,
+have the choice to output either the abstract cluster points, or the gridded
+product after interpolation 4. Validation toolset - validation to local
+observation timeseries - plotting 5. Gap filling algorithm - random forest
+temporal gap filling (TBD) Validation (4) and Gap filling (4) are future
+implementation. ## Installation We have now added an environments.yml file to
+handle versions of depencencies that are tested with the current codebase, to
+use this run: `conda env create -f environment.yml` Alternatively you can
+follow this method for dependencies (to be deprecated): ```bash conda create -
+n downscaling python=3.9 ipython conda activate downscaling # Recomended way to
+install dependencies: conda install -c conda-forge xarray matplotlib scikit-
+learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask rioxarray ``` Then
+install the code: ``` # OPTION 1 (Pypi release): pip install TopoPyScale #
+OPTION 2 (development): cd github # navigate to where you want to clone
+TopoPyScale git clone git@github.com:ArcticSnow/TopoPyScale.git pip install -
+e TopoPyScale #install a development version #---------------------------------
+------------------------- # OPTIONAL: if using jupyter lab # add this new
+Python kernel to your jupyter lab PATH python -m ipykernel install --user --
+name downscaling # Tool for generating documentation from code docstring pip
+install lazydocs ``` Then you need to setup your `cdsapi` with the Copernicus
+API key system. Follow [this tutorial](https://cds.climate.copernicus.eu/api-
+how-to#install-the-cds-api-key) after creating an account with [Copernicus]
+(https://cds.climate.copernicus.eu/). On Linux, create a file `nano
+~/.cdsapirc` with inside: ``` url: https://cds.climate.copernicus.eu/api/v2
+key: {uid}:{api-key} ``` ## Basic usage 1. Setup your Python environment 2.
+Create your project directory 3. Configure the file `config.ini` to fit your
+problem (see [`config.yml`](https://github.com/ArcticSnow/TopoPyScale_examples/
+blob/main/ex1_norway_finse/config_spatial.yml) for an example) 4. Run
+TopoPyScale ```python import pandas as pd from TopoPyScale import topoclass as
+tc from matplotlib import pyplot as plt # ========= STEP 1 ========== # Load
+Configuration config_file = './config.yml' mp = tc.Topoclass(config_file) #
+Compute parameters of the DEM (slope, aspect, sky view factor)
+mp.compute_dem_param() # ========== STEP 2 =========== # Extract DEM parameters
+for points of interest (centroids or physical points) mp.extract_topo_param() #
+----- Option 1: # Compute clustering of the input DEM and extract cluster
+centroids #mp.extract_dem_cluster_param() # plot clusters
 #mp.toposub.plot_clusters_map() # plot sky view factor
 #mp.toposub.plot_clusters_map(var='svf', cmap=plt.cm.viridis) # ------ Option
 2: # inidicate in the config file the .csv file containing a list of point
 coordinates (!!! must same coordinate system as DEM !!!) #mp.extract_pts_param
 (method='linear',index_col=0) # ========= STEP 3 ========== # compute solar
 geometry and horizon angles mp.compute_solar_geometry() mp.compute_horizon() #
 ========= STEP 4 ========== # Perform the downscaling mp.downscale_climate() #
```

### Comparing `topopyscale-0.2.1/README.md` & `topopyscale-0.2.2/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -1,13 +1,18 @@
 
 
 [![DOI](https://zenodo.org/badge/411249045.svg)](https://zenodo.org/badge/latestdoi/411249045)
 [![GitHub license](https://img.shields.io/github/license/ArcticSnow/TopoPyScale)](https://github.com/ArcticSnow/TopoPyScale/blob/main/LICENSE)
 ![GitHub release (latest by date)](https://img.shields.io/github/v/release/ArcticSnow/TopoPyScale)
 <a href="https://joss.theoj.org/papers/91621581b2d0c097495fdd1e58179e87"><img src="https://joss.theoj.org/papers/91621581b2d0c097495fdd1e58179e87/status.svg"></a>
+[![][docs-dev-img]][docs-dev-url]
+![Test](https://github.com/ArcticSnow/TopoPyScale/actions/workflows/test_topopyscale.yml/badge.svg)
+
+[docs-dev-img]: https://img.shields.io/badge/docs-latest-blue.svg
+[docs-dev-url]: https://topopyscale.readthedocs.io
 
 # TopoPyScale
 Python version of Toposcale packaged as a Pypi library. Toposcale is an original idea of Joel Fiddes to perform topography-based downscaling of climate data to the hillslope scale.
 
 Documentation avalaible: https://topopyscale.readthedocs.io
 
 ![](https://github.com/ArcticSnow/TopoPyScale/blob/main/JOSS/temperature_comparison_crop_scaled.jpg)
@@ -17,33 +22,29 @@
 - Fiddes, J. and Gruber, S.: TopoSUB: a tool for efficient large area numerical modelling in complex topography at sub-grid scales, Geosci. Model Dev., 5, 1245–1257, https://doi.org/10.5194/gmd-5-1245-2012, 2012. 
 
 Kristoffer Aalstad has a Matlab implementation: https://github.com/krisaalstad/TopoLAB
 
 ## Contribution Workflow
 **Please follow these simple rules:**
 1. a bug -> fix it! 
-2. an idea or a bug you cannot fix? -> create a new [issue](https://github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one exist, then add material to tit.
-3. wanna develop a new feature/idea? -> create a new branch. Do the development. Merge with main branch when accomplished.
-4. Create release version when significant improvements and bug fixes have been done. Coordinate with others
+2. an idea or a bug you cannot fix? -> create a new [issue](https://github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one exist, then add material to it.
+3. wanna develop a new feature/idea? -> create a new branch. Go wild. Merge with main branch when accomplished.
+4. Create release version when significant improvements and bug fixes have been done. Coordinate with others on [Discussions](https://github.com/ArcticSnow/TopoPyScale/discussions)
 
 **Create a new release:**
 Follow procedure and conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY
 
-And check out our Slack: tscaleworkspace.slack.com
+Our forum is now on [Github Discussions](https://github.com/ArcticSnow/TopoPyScale/discussions). Come visit!
 
-Contributors to the current version (2021) are:
-- Simon Filhol
-- Joel Fiddes
-- Kristoffer Aalstad
 
 ## Design
 
 1. Inputs
     - Climate data from reanalysis (ERA5, etc)
-    - Climate data from future projections (CORDEX) (not avail.)
+    - Climate data from future projections (CORDEX) (TBD)
     - DEM from local source, or fetch from public repository: SRTM, ArcticDEM, ASTER
 2. Run TopoScale
     - compute derived values (from DEM)
     - toposcale (k-mean clustering)
     - interpolation (bilinear, inverse square dist.)
 3. Output
     - Cryogrid format
@@ -52,27 +53,37 @@
     - Snowmodel format
     - basic netcfd
     - For each method, have the choice to output either the abstract cluster points, or the gridded product after interpolation
 4. Validation toolset
     - validation to local observation timeseries
     - plotting
 5. Gap filling algorithm
-    - random forest temporal gap filling
+    - random forest temporal gap filling (TBD)
 
 Validation (4) and Gap filling (4) are future implementation.
 
 ## Installation
 
+We have now added an environments.yml file to handle versions of depencencies that are tested with the current codebase, to use this run:
+
+`conda env create -f environment.yml`
+
+Alternatively you can follow this method for dependencies (to be deprecated):
+
 ```bash
-conda create -n downscaling python=3.8 ipython
+conda create -n downscaling python=3.9 ipython
 conda activate downscaling
 
 # Recomended way to install dependencies:
-conda install -c conda-forge xarray matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask
+conda install -c conda-forge xarray matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask rioxarray
+```
+
+Then install the code:
 
+```
 # OPTION 1 (Pypi release):
 pip install TopoPyScale
 
 # OPTION 2 (development):
 cd github  # navigate to where you want to clone TopoPyScale
 git clone git@github.com:ArcticSnow/TopoPyScale.git
 pip install -e TopoPyScale    #install a development version
```

#### html2text {}

```diff
@@ -1,70 +1,78 @@
  [![DOI](https://zenodo.org/badge/411249045.svg)](https://zenodo.org/badge/
 latestdoi/411249045) [![GitHub license](https://img.shields.io/github/license/
 ArcticSnow/TopoPyScale)](https://github.com/ArcticSnow/TopoPyScale/blob/main/
 LICENSE) ![GitHub release (latest by date)](https://img.shields.io/github/v/
 release/ArcticSnow/TopoPyScale) [https://joss.theoj.org/papers/
-91621581b2d0c097495fdd1e58179e87/status.svg] # TopoPyScale Python version of
-Toposcale packaged as a Pypi library. Toposcale is an original idea of Joel
-Fiddes to perform topography-based downscaling of climate data to the hillslope
-scale. Documentation avalaible: https://topopyscale.readthedocs.io ![](https://
-github.com/ArcticSnow/TopoPyScale/blob/main/JOSS/
-temperature_comparison_crop_scaled.jpg) **References:** - Fiddes, J. and
-Gruber, S.: TopoSCALE v.1.0: downscaling gridded climate data in complex
+91621581b2d0c097495fdd1e58179e87/status.svg] [![][docs-dev-img]][docs-dev-url]
+![Test](https://github.com/ArcticSnow/TopoPyScale/actions/workflows/
+test_topopyscale.yml/badge.svg) [docs-dev-img]: https://img.shields.io/badge/
+docs-latest-blue.svg [docs-dev-url]: https://topopyscale.readthedocs.io #
+TopoPyScale Python version of Toposcale packaged as a Pypi library. Toposcale
+is an original idea of Joel Fiddes to perform topography-based downscaling of
+climate data to the hillslope scale. Documentation avalaible: https://
+topopyscale.readthedocs.io ![](https://github.com/ArcticSnow/TopoPyScale/blob/
+main/JOSS/temperature_comparison_crop_scaled.jpg) **References:** - Fiddes, J.
+and Gruber, S.: TopoSCALE v.1.0: downscaling gridded climate data in complex
 terrain, Geosci. Model Dev., 7, 387â405, https://doi.org/10.5194/gmd-7-387-
 2014, 2014. - Fiddes, J. and Gruber, S.: TopoSUB: a tool for efficient large
 area numerical modelling in complex topography at sub-grid scales, Geosci.
 Model Dev., 5, 1245â1257, https://doi.org/10.5194/gmd-5-1245-2012, 2012.
 Kristoffer Aalstad has a Matlab implementation: https://github.com/krisaalstad/
 TopoLAB ## Contribution Workflow **Please follow these simple rules:** 1. a bug
 -> fix it! 2. an idea or a bug you cannot fix? -> create a new [issue](https://
 github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one
-exist, then add material to tit. 3. wanna develop a new feature/idea? -> create
-a new branch. Do the development. Merge with main branch when accomplished. 4.
-Create release version when significant improvements and bug fixes have been
-done. Coordinate with others **Create a new release:** Follow procedure and
-conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY And check
-out our Slack: tscaleworkspace.slack.com Contributors to the current version
-(2021) are: - Simon Filhol - Joel Fiddes - Kristoffer Aalstad ## Design 1.
-Inputs - Climate data from reanalysis (ERA5, etc) - Climate data from future
-projections (CORDEX) (not avail.) - DEM from local source, or fetch from public
-repository: SRTM, ArcticDEM, ASTER 2. Run TopoScale - compute derived values
-(from DEM) - toposcale (k-mean clustering) - interpolation (bilinear, inverse
-square dist.) 3. Output - Cryogrid format - FSM format - CROCUS format -
-Snowmodel format - basic netcfd - For each method, have the choice to output
-either the abstract cluster points, or the gridded product after interpolation
-4. Validation toolset - validation to local observation timeseries - plotting
-5. Gap filling algorithm - random forest temporal gap filling Validation (4)
-and Gap filling (4) are future implementation. ## Installation ```bash conda
-create -n downscaling python=3.8 ipython conda activate downscaling #
-Recomended way to install dependencies: conda install -c conda-forge xarray
-matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask #
-OPTION 1 (Pypi release): pip install TopoPyScale # OPTION 2 (development): cd
-github # navigate to where you want to clone TopoPyScale git clone
-git@github.com:ArcticSnow/TopoPyScale.git pip install -e TopoPyScale #install a
-development version #---------------------------------------------------------
-- # OPTIONAL: if using jupyter lab # add this new Python kernel to your jupyter
-lab PATH python -m ipykernel install --user --name downscaling # Tool for
-generating documentation from code docstring pip install lazydocs ``` Then you
-need to setup your `cdsapi` with the Copernicus API key system. Follow [this
-tutorial](https://cds.climate.copernicus.eu/api-how-to#install-the-cds-api-key)
-after creating an account with [Copernicus](https://cds.climate.copernicus.eu/
-). On Linux, create a file `nano ~/.cdsapirc` with inside: ``` url: https://
-cds.climate.copernicus.eu/api/v2 key: {uid}:{api-key} ``` ## Basic usage 1.
-Setup your Python environment 2. Create your project directory 3. Configure the
-file `config.ini` to fit your problem (see [`config.yml`](https://github.com/
-ArcticSnow/TopoPyScale_examples/blob/main/ex1_norway_finse/config_spatial.yml)
-for an example) 4. Run TopoPyScale ```python import pandas as pd from
-TopoPyScale import topoclass as tc from matplotlib import pyplot as plt #
-========= STEP 1 ========== # Load Configuration config_file = './config.yml'
-mp = tc.Topoclass(config_file) # Compute parameters of the DEM (slope, aspect,
-sky view factor) mp.compute_dem_param() # ========== STEP 2 =========== #
-Extract DEM parameters for points of interest (centroids or physical points)
-mp.extract_topo_param() # ----- Option 1: # Compute clustering of the input DEM
-and extract cluster centroids #mp.extract_dem_cluster_param() # plot clusters
+exist, then add material to it. 3. wanna develop a new feature/idea? -> create
+a new branch. Go wild. Merge with main branch when accomplished. 4. Create
+release version when significant improvements and bug fixes have been done.
+Coordinate with others on [Discussions](https://github.com/ArcticSnow/
+TopoPyScale/discussions) **Create a new release:** Follow procedure and
+conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY Our forum
+is now on [Github Discussions](https://github.com/ArcticSnow/TopoPyScale/
+discussions). Come visit! ## Design 1. Inputs - Climate data from reanalysis
+(ERA5, etc) - Climate data from future projections (CORDEX) (TBD) - DEM from
+local source, or fetch from public repository: SRTM, ArcticDEM, ASTER 2. Run
+TopoScale - compute derived values (from DEM) - toposcale (k-mean clustering) -
+interpolation (bilinear, inverse square dist.) 3. Output - Cryogrid format -
+FSM format - CROCUS format - Snowmodel format - basic netcfd - For each method,
+have the choice to output either the abstract cluster points, or the gridded
+product after interpolation 4. Validation toolset - validation to local
+observation timeseries - plotting 5. Gap filling algorithm - random forest
+temporal gap filling (TBD) Validation (4) and Gap filling (4) are future
+implementation. ## Installation We have now added an environments.yml file to
+handle versions of depencencies that are tested with the current codebase, to
+use this run: `conda env create -f environment.yml` Alternatively you can
+follow this method for dependencies (to be deprecated): ```bash conda create -
+n downscaling python=3.9 ipython conda activate downscaling # Recomended way to
+install dependencies: conda install -c conda-forge xarray matplotlib scikit-
+learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask rioxarray ``` Then
+install the code: ``` # OPTION 1 (Pypi release): pip install TopoPyScale #
+OPTION 2 (development): cd github # navigate to where you want to clone
+TopoPyScale git clone git@github.com:ArcticSnow/TopoPyScale.git pip install -
+e TopoPyScale #install a development version #---------------------------------
+------------------------- # OPTIONAL: if using jupyter lab # add this new
+Python kernel to your jupyter lab PATH python -m ipykernel install --user --
+name downscaling # Tool for generating documentation from code docstring pip
+install lazydocs ``` Then you need to setup your `cdsapi` with the Copernicus
+API key system. Follow [this tutorial](https://cds.climate.copernicus.eu/api-
+how-to#install-the-cds-api-key) after creating an account with [Copernicus]
+(https://cds.climate.copernicus.eu/). On Linux, create a file `nano
+~/.cdsapirc` with inside: ``` url: https://cds.climate.copernicus.eu/api/v2
+key: {uid}:{api-key} ``` ## Basic usage 1. Setup your Python environment 2.
+Create your project directory 3. Configure the file `config.ini` to fit your
+problem (see [`config.yml`](https://github.com/ArcticSnow/TopoPyScale_examples/
+blob/main/ex1_norway_finse/config_spatial.yml) for an example) 4. Run
+TopoPyScale ```python import pandas as pd from TopoPyScale import topoclass as
+tc from matplotlib import pyplot as plt # ========= STEP 1 ========== # Load
+Configuration config_file = './config.yml' mp = tc.Topoclass(config_file) #
+Compute parameters of the DEM (slope, aspect, sky view factor)
+mp.compute_dem_param() # ========== STEP 2 =========== # Extract DEM parameters
+for points of interest (centroids or physical points) mp.extract_topo_param() #
+----- Option 1: # Compute clustering of the input DEM and extract cluster
+centroids #mp.extract_dem_cluster_param() # plot clusters
 #mp.toposub.plot_clusters_map() # plot sky view factor
 #mp.toposub.plot_clusters_map(var='svf', cmap=plt.cm.viridis) # ------ Option
 2: # inidicate in the config file the .csv file containing a list of point
 coordinates (!!! must same coordinate system as DEM !!!) #mp.extract_pts_param
 (method='linear',index_col=0) # ========= STEP 3 ========== # compute solar
 geometry and horizon angles mp.compute_solar_geometry() mp.compute_horizon() #
 ========= STEP 4 ========== # Perform the downscaling mp.downscale_climate() #
```

### Comparing `topopyscale-0.2.1/TopoPyScale/fetch_dem.py` & `topopyscale-0.2.2/TopoPyScale/fetch_dem.py`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/TopoPyScale/meteo_util.py` & `topopyscale-0.2.2/TopoPyScale/meteo_util.py`

 * *Files 2% similar despite different names*

```diff
@@ -166,8 +166,9 @@
         ds (dataset): dataset with pressure and mix_ratio variables
         var (dict): variable name correspondance 
     Returns:
         dataset: input dataset with new `vp` columns
     """
     eps0 = 0.622  # Ratio of molecular weight of water and dry air [-]
     ds['vp'] = 0.5 * ds[var['pressure']] * (-1 + np.sqrt(1 + 4 * ds[var['mix_ratio']] / eps0))
-    return ds
+    ds.vp.attrs = {'units': '???????', 'long_name': 'Vapor pressure', 'standard_name': 'vapor_pressure'}
+    return ds
```

### Comparing `topopyscale-0.2.1/TopoPyScale/precip_orographic.py` & `topopyscale-0.2.2/TopoPyScale/precip_orographic.py`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/TopoPyScale/solar_geom.py` & `topopyscale-0.2.2/TopoPyScale/solar_geom.py`

 * *Files 2% similar despite different names*

```diff
@@ -36,15 +36,15 @@
     """
     print('\n---> Computing solar geometry')
     if (int(sr_epsg) != "4326") or ('longitude' not in df_position.columns):
         trans = Transformer.from_crs("epsg:" + sr_epsg, "epsg:4326", always_xy=True)
         df_position['longitude'], df_position['latitude'] = trans.transform(df_position.x.values, df_position.y.values)
     # tstep_dict = {'1H': 1, '3H': 3, '6H': 6}
 
-    times = pd.date_range(start_date, pd.to_datetime(end_date)+pd.to_timedelta('1D'), freq=tstep, tz='UTC', closed='left')
+    times = pd.date_range(start_date, pd.to_datetime(end_date)+pd.to_timedelta('1D'), freq=tstep, tz='UTC', inclusive='left')
 
 
     df_pool = pd.DataFrame()
     df_pool[['latitude', 'longitude', 'elevation']] = df_position[['latitude', 'longitude', 'elevation']]
     df_pool['times'] = df_pool.latitude.apply(lambda x: times)
 
     def compute_solar_geom(time_step, latitude, longitude, elevation):
@@ -71,15 +71,15 @@
         {
             "zenith": (["point_id", "time"], np.deg2rad(arr_val[:, 0, :])),
             "azimuth": (["point_id", "time"], np.deg2rad(arr_val[:,1,:] - 180)),
             "elevation": (["point_id", "time"], np.deg2rad(arr_val[:, 2, :])),
         },
         coords={
             "point_id": df_position.index,
-            "time": pd.date_range(start_date, pd.to_datetime(end_date)+pd.to_timedelta('1D'), freq=tstep, closed='left'),
+            "time": pd.date_range(start_date, pd.to_datetime(end_date)+pd.to_timedelta('1D'), freq=tstep, inclusive='left'),
             "reference_time": pd.Timestamp(start_date),
         },
     )
 
     ds['mu0'] = np.cos(ds.zenith) * (np.cos(ds.zenith)>0)
     S0 = 1370 # Solar constat (total TOA solar irradiance) [Wm^-2] used in ECMWF's IFS
     ds['SWtoa'] = S0 * ds.mu0
```

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_compare.py` & `topopyscale-0.2.2/TopoPyScale/topo_compare.py`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_da.py` & `topopyscale-0.2.2/TopoPyScale/topo_da.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,19 +11,20 @@
 import re
 import pandas as pd
 import numpy as np
 from matplotlib import pyplot as plt
 import copy
 import rasterio as rio
 from osgeo import gdal
-import osr
+from osgeo import osr 
 from scipy.interpolate import interp1d
 from TopoPyScale import topo_sim as sim
 from datetime import datetime
 import xarray as xr
+import rioxarray
 
 
 # import gdal
 
 
 def lognormDraws_kris(n, med, s):
     """
@@ -305,15 +306,15 @@
     os.makedirs(MODPATH, exist_ok=True)
     os.makedirs(RAWPATH, exist_ok=True)
     os.makedirs(MODPATH + "/transformed/", exist_ok=True)
 
     hreg = ("h" + f"{horiz:02d}")  # re.compile("h2[4]")
     vreg = ("v" + f"{vert:02d}")  # re.compile("v0[5]")
     TILE = hreg + vreg
-    print("Downloading " + product + " from " + STARTDATE + " to " + ENDDATE)
+    print("Downloading " + PRODUCT + " from " + STARTDATE + " to " + ENDDATE)
     os.system("modis_download.py -U " +
               USER +
               " -P " + PWD +
               " -u " + HOST +
               " -p mail@pymodis.com "
               " -s " + FOLDER +
               " -p " + PRODUCT +
@@ -393,33 +394,36 @@
 
     Returns:
         df_sort: dataframe of julian dates and fSCA values
     """
 
     files = glob.glob(wdir + "/modis/transformed/*.tif")
     data = []
+    doy = []
     juldates = []
     for file in files:
         with rio.open(file) as src:
             # Read as numpy array
             array = src.read()
             profile = src.profile
 
             mymean = np.mean(array)
             juldate = file.split(".")[1].split("A")[1]
+            mydoy = juldate[4:7]   
 
         data.append(mymean)
         juldates.append(juldate)
+        doy.append(mydoy)
 
     # convert to fSCA
     fsca = (-0.01 + (1.45 * np.array(data)))
     fsca[fsca <= 0] = 0
     fsca[fsca > 100] = 100
 
-    d = {'dates': juldates, 'fSCA': fsca}
+    d = {'dates': juldates, 'fSCA': fsca, 'DOY': doy}
     df = pd.DataFrame(data=d)
     df_sort = df.sort_values("dates")
     # add datetime object
     df_sort["mydates"] = [pd.to_datetime(e[:4]) + pd.to_timedelta(int(e[4:]) - 1, unit='D') for e in df_sort.dates]
 
     df_sort_reindex = df_sort.reset_index(drop=True)
     if plot:
@@ -869,15 +873,15 @@
 
     nclust = len(df_mean)
     lookup = np.arange(nclust, dtype=np.uint16)
 
     for i in range(0, nclust):
         lookup[i] = df_mean[i]
 
-    with rasterio.open('landform.tif') as src:
+    with rio.open('landform.tif') as src:
         # Read as numpy array
         array = src.read()
         profile = src.profile
 
         # Reclassify in a single operation using broadcasting
         array = lookup[array]
         # binary map
@@ -886,15 +890,15 @@
 
 
     # rasterio.plot.show(array, cmap='viridis')
     # plt.show()
 
     with rio.open('output_raster.tif', 'w', **profile) as dst:
         # Write to disk
-        dst.write(array.astype(rasterio.int16))
+        dst.write(array.astype(rio.int16))
 
     src1 = rio.open("output_raster.tif")
     rio.plot.show(src1, ax=axhist)
     cbar2 = plt.imshow(src1.read(1), cmap='viridis')
     fig.colorbar(cbar2, ax=axhist)
     plt.show()
 
@@ -995,32 +999,32 @@
     # compute and plot open loop
     nclust = len(df_mean_open)
     lookup = np.arange(nclust, dtype=np.uint16)
 
     for i in range(0, nclust):
         lookup[i] = df_mean_open[i]
 
-    with rasterio.open('landform.tif') as src:
+    with rio.open('landform.tif') as src:
         # Read as numpy array
         array = src.read()
         profile = src.profile
 
         # Reclassify in a single operation using broadcasting
         array = lookup[array]
         # binary map
         #array[array <= 0] = 0
         #array[array > 0] = 1
 
 
-    # rasterio.plot.show(array, cmap='viridis')
+    # rio.plot.show(array, cmap='viridis')
     # plt.show()
 
     with rio.open('output_raster.tif', 'w', **profile) as dst:
         # Write to disk
-        dst.write(array.astype(rasterio.int16))
+        dst.write(array.astype(rio.int16))
 
     src1 = rio.open("output_raster.tif")
     rio.plot.show(src1, ax=axopen)
     cbar2 = plt.imshow(src1.read(1), cmap='viridis')
     fig.colorbar(cbar2, ax=axopen)
 
     # plot modis again
@@ -1032,32 +1036,32 @@
     # compute and plot DA
     nclust = len(df_mean_da)
     lookup = np.arange(nclust, dtype=np.uint16)
 
     for i in range(0, nclust):
         lookup[i] = df_mean_da[i]
 
-    with rasterio.open('landform.tif') as src:
+    with rio.open('landform.tif') as src:
         # Read as numpy array
         array = src.read()
         profile = src.profile
 
         # Reclassify in a single operation using broadcasting
         array = lookup[array]
         # binary map
         #array[array <= 0] = 0
         #array[array > 0] = 1
 
 
-    # rasterio.plot.show(array, cmap='viridis')
+    # rio.plot.show(array, cmap='viridis')
     # plt.show()
 
     with rio.open('output_raster.tif', 'w', **profile) as dst:
         # Write to disk
-        dst.write(array.astype(rasterio.int16))
+        dst.write(array.astype(rio.int16))
 
     src1 = rio.open("output_raster.tif")
     rio.plot.show(src1, ax=axda)
     cbar2 = plt.imshow(src1.read(1), cmap='viridis')
     fig.colorbar(cbar2, ax=axda)
     plt.show()
 
@@ -1070,15 +1074,15 @@
         return sorted(l, key=alphanum_key)
     geotiff_list = natural_sort(geotiff_list_unsorted)
 
     # Create variable used for time axis
     mydates = [lname.split('.A')[1].split(".h")[0] for lname in geotiff_list]
     time_var = xr.Variable('time', mydates)
     # Load in and concatenate all individual GeoTIFFs
-    geotiffs_da = xr.concat([xr.open_rasterio(i) for i in geotiff_list], dim=time_var)
+    geotiffs_da = xr.concat([rioxarray.open_rasterio(i) for i in geotiff_list], dim=time_var)
     # Covert our xarray.DataArray into a xarray.Dataset
     geotiffs_ds = geotiffs_da.to_dataset('band')
     # Rename the variable to a more useful name
     ds = geotiffs_ds.rename({1: 'fSCA'})
     arr = ds.to_array()
 
     # tuples of coordinates
@@ -1120,14 +1124,15 @@
     xmax = float(centreX + xres/2)
     xmin = float(centreX - xres/2)
     ymax = float(centreY + yres/2)
     ymin = float(centreY - yres/2)
     bbox = [xmax,xmin, ymax, ymin]
     return bbox
 
+'''
 def getSamples_inModisPixel(map_path):
     """
     Identify samples that exist within a single bbox and proportianal cover. This can be used to construct a modelled fSCA in a MODIS pixel
 
     Args:
         map_path: path to landform.tif
 
@@ -1137,16 +1142,16 @@
     """
 
     # # define proj
     # proj = pyproj.Transformer.from_crs(int(epsg_in), int(epsg_out), always_xy=True)
     # # project
     # x2, y2 = proj.transform(x_coord, y_coord)
     # open map
-    dataset = rasterio.open(map_path)
+    dataset = rio.open(map_path)
     # get pixel x+y of the coordinate
     py, px = dataset.index(x2, y2)
     # create 1x1px window of the pixel
-    window = rasterio.windows.Window(px - 1 // 2, py - 1 // 2, 1, 1)
+    window = rio.windows.Window(px - 1 // 2, py - 1 // 2, 1, 1)
     # read rgb values of the window
     clip = dataset.read(window=window)
     return (int(clip))
-
+'''
```

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_export.py` & `topopyscale-0.2.2/TopoPyScale/topo_export.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 S. Filhol, December 2021
 
 TODO;
 - SPHY forcing (grids)
 """
 import pdb
-import sys
+import sys, csv
 import numpy as np
 import pandas as pd
 import datetime as dt
 import xarray as xr
 from scipy import io
 from TopoPyScale import meteo_util as mu
 from multiprocessing.dummy import Pool as ThreadPool
@@ -103,16 +103,16 @@
     fo = fo.drop_vars(['q', 'tp'])
     fo = fo[['tair', 'rh', 'p', 'lw', 'sw', 'ws', 'precip']].expand_dims({'dummy': 1}, axis=2)
 
     fo.tair.attrs = {'units':'C', 'standard_name':'tair', 'long_name':'Near Surface Air Temperature', '_FillValue': -9999999.0}
     fo.rh.attrs = {'units':'kg/kg', 'standard_name':'rh', 'long_name':'Near Surface Relative Humidity', '_FillValue': -9999999.0}
     fo.ws.attrs = {'units':'m/s', 'standard_name':'ws', 'long_name':'Wind Speed', '_FillValue': -9999999.0}
     fo.precip.attrs = {'units':'mm/s', 'standard_name':'precip', 'long_name':'Precipitation', '_FillValue': -9999999.0}
-    fo.sw.attrs = {'units':'W/m2', 'standard_name':'sw', 'long_name':'Surface Incident Direct Shortwave Radiation', '_FillValue': -9999999.0}
-    fo.lw.attrs = {'units':'W/m2', 'standard_name':'lw', 'long_name':'Surface Incident Longtwave Radiation', '_FillValue': -9999999.0}
+    fo.sw.attrs = {'units':'W/m^2', 'standard_name':'sw', 'long_name':'Surface Incident Direct Shortwave Radiation', '_FillValue': -9999999.0}
+    fo.lw.attrs = {'units':'W/m^2', 'standard_name':'lw', 'long_name':'Surface Incident Longtwave Radiation', '_FillValue': -9999999.0}
     fo.p.attrs = {'units':'Pa', 'standard_name':'p', 'long_name':'Surface Pressure', '_FillValue': -9999999.0}
 
     fo.attrs = {'title':'Forcing for MuSa assimilation scheme',
                 'source': 'Data from {} downscaled with TopoPyScale'.format(climate_dataset_name),
                 'creator_name':'Dataset created by {}'.format(project_authors),
                 'date_created':dt.datetime.now().strftime('%Y/%m/%d %H:%M:%S')}
     encod_dict = {}
@@ -179,21 +179,21 @@
         fo['Sin'] = ('time', ds_pt.SW.values)
         fo['Lin'] = ('time', ds_pt.LW.values)
         fo['p'] = ('time', ds_pt.p.values)
         rh = mu.q_2_rh(ds_pt.t.values, ds_pt.p.values, ds_pt.q.values)
         rain, snow = mu.partition_snow(ds_pt.tp.values, ds_pt.t.values, rh, ds_pt.p.values, method=snow_partition_method)
         fo['rainfall'], fo['snowfall'] = ('time', rain * 24), ('time', snow * 24)  # convert from mm/hr to mm/day
 
-        fo.Tair.attrs = {'units':'C', 'standard_name':'Tair', 'long_name':'Near Surface Air Temperature', '_FillValue': -9999999.0}
+        fo.Tair.attrs = {'units':'°C', 'standard_name':'Tair', 'long_name':'Near Surface Air Temperature', '_FillValue': -9999999.0}
         fo.q.attrs = {'units':'kg/kg', 'standard_name':'q', 'long_name':'Near Surface Specific Humidity', '_FillValue': -9999999.0}
         fo.wind.attrs = {'units':'m/s', 'standard_name':'wind', 'long_name':'Wind Speed', '_FillValue': -9999999.0}
-        fo.rainfall.attrs = {'units':'mm/day', 'standard_name':'rainfall', 'long_name':'Rainfall Rate', '_FillValue': -9999999.0}
-        fo.snowfall.attrs = {'units':'mm/day', 'standard_name':'snowfall', 'long_name':'Snowfall Rate', '_FillValue': -9999999.0}
-        fo.Sin.attrs = {'units':'W/m2', 'standard_name':'Sin', 'long_name':'Surface Incident Direct Shortwave Radiation', '_FillValue': -9999999.0}
-        fo.Lin.attrs = {'units':'W/m2', 'standard_name':'Lin', 'long_name':'Surface Incident Longtwave Radiation', '_FillValue': -9999999.0}
+        fo.rainfall.attrs = {'units':'mm/d', 'standard_name':'rainfall', 'long_name':'Rainfall Rate', '_FillValue': -9999999.0}
+        fo.snowfall.attrs = {'units':'mm/d', 'standard_name':'snowfall', 'long_name':'Snowfall Rate', '_FillValue': -9999999.0}
+        fo.Sin.attrs = {'units':'W/m^2', 'standard_name':'Sin', 'long_name':'Surface Incident Direct Shortwave Radiation', '_FillValue': -9999999.0}
+        fo.Lin.attrs = {'units':'W/m^2', 'standard_name':'Lin', 'long_name':'Surface Incident Longtwave Radiation', '_FillValue': -9999999.0}
         fo.p.attrs = {'units':'Pa', 'standard_name':'p', 'long_name':'Surface Pressure', '_FillValue': -9999999.0}
 
         fo.attrs = {'title':'Forcing for Cryogrid Community model',
                     'source': 'Data from {} downscaled with TopoPyScale'.format(climate_dataset_name),
                     'creator_name':'Dataset created by {}'.format(project_author),
                     'date_created':dt.datetime.now().strftime('%Y/%m/%d %H:%M:%S')}
         encod_dict = {}
@@ -234,15 +234,15 @@
     - Check unit DONE jf
     - Check format is compatible with compiled model DONE jf
     - ensure ds.point_id.values always
     """
 
     #n_digits = len(str(ds.point_id.values.max()))
     # always set this as 3  simplifies parsing files later on
-    n_digits = 3
+    n_digits = 2
 
     for pt in ds.point_id.values:
         foutput = fname_format.split('*')[0] + str(pt).zfill(n_digits) + fname_format.split('*')[1]
         ds_pt = ds.sel(point_id=pt).copy()
         df = pd.DataFrame()
         df['year'] = pd.to_datetime(ds_pt.time.values).year
         df['month']  = pd.to_datetime(ds_pt.time.values).month
```

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_obs.py` & `topopyscale-0.2.2/TopoPyScale/topo_obs.py`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_param.py` & `topopyscale-0.2.2/TopoPyScale/topo_param.py`

 * *Files 3% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 from topocalc import viewf
 from topocalc import horizon
 import time
 from multiprocessing.dummy import Pool as ThreadPool
 import multiprocessing as mproc
 import os
 from TopoPyScale import topo_export as te
-
+import rioxarray
 
 def convert_epsg_pts(xs,ys, epsg_src=4326, epsg_tgt=3844):
     """
     Simple function to convert a list fo poitn from one projection to another oen using PyProj
 
     Args:
         xs (array): 1D array with X-coordinate expressed in the source EPSG
@@ -134,15 +134,15 @@
         dem_file (str): path to raster file (geotif). Raster must be in local cartesian coordinate system (e.g. UTM)
 
     Returns:  
         dataset: x, y, elev, slope, aspect, svf
 
     """
     print('\n---> Extracting DEM parameters (slope, aspect, svf)')
-    ds = xr.open_rasterio(dem_file).to_dataset('band')
+    ds = rioxarray.open_rasterio(dem_file).to_dataset('band')
     ds = ds.rename({1: 'elevation'})
     dx = ds.x.diff('x').median().values
     dy = ds.y.diff('y').median().values
     dem_arr = ds.elevation.values
     print('Computing slope and aspect ...')
     slope, aspect = gradient.gradient_d8(dem_arr, dx, dy)
     print('Computing svf ...')
@@ -178,15 +178,15 @@
         num_threads (int): number of threads to parallize on
 
     Returns: 
         dataarray: all horizon angles for x,y,azimuth coordinates
          
     """
     print('\n---> Computing horizons with {} degree increments'.format(azimuth_inc))
-    ds = xr.open_rasterio(dem_file).to_dataset('band')
+    ds = rioxarray.open_rasterio(dem_file).to_dataset('band')
     ds = ds.rename({1: 'elevation'})
     dx = ds.x.diff('x').median().values
 
     azimuth = np.arange(-180 + azimuth_inc / 2, 180, azimuth_inc) # center the azimuth in middle of the bin
     arr_val = np.empty((azimuth.shape[0], ds.elevation.shape[0], ds.elevation.shape[1]))
 
     if num_threads is None:
```

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_plot.py` & `topopyscale-0.2.2/TopoPyScale/topo_plot.py`

 * *Files 15% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 S. Filhol, December 2021
 
 """
 
 import matplotlib.pyplot as plt
 from matplotlib.colors import LightSource
 import numpy as np
+import xarray as xr
 
 def map_terrain(ds_param,
                 var='elevation',
                 hillshade=True,
                 cmap=plt.cm.viridis,
                 **kwargs):
     '''
@@ -44,42 +45,48 @@
                alpha=alpha, **kwargs)
     plt.colorbar(label=var)
     plt.show()
 
 
 def map_variable(ds_down,
                  ds_param,
-                 time_step=1,
+                 time_step=None,
                  time=None,
-                 var='t',
+                 var=None,
                  ax=None,
                  cmap=plt.cm.RdBu_r,
                  hillshade=True,
                  **kwargs):
     """
     Function to plot unclustered downscaled points given that each point corresponds to a cluster label
 
     Args:
-        ds_down (dataset): TopoPyScale downscaled point object with coordinates (time, point_id)
+        ds_down (dataset): TopoPyScale downscaled point object with coordinates (time, point_id). Can be single variable or multiple
         ds_param (dataset): TopoPyScale toposub dataset with coordinates (x,y)
         time_step (int): (optional) time step to plot.
         time (str): (optional) time slice to plot. time overule time_step
-        var (str): variable from ds_down to plot. e.g. 't' for temperature
+        var (str): variable from ds_down to plot. e.g. 't' for temperature if ds_down has more than one variable
         cmap (obj): pyplot colormap object
         hillshade (bool): add terrain hillshade in background
         **kwargs: kwargs to pass to imshow() in dict format.
 
     TODO:
     - if temperature, divergent colorscale around 0degC
     """
     if ax is None:
         fig, ax = plt.subplots(1,1)
 
-    if time is None:
-        time = ds_down.time.isel(time=time_step).data
+    if time is None and time_step is not None:
+        ds = ds_down.isel(time=time_step)
+    elif time is not None and time_step is None:
+        ds = ds_down.sel(time=time)
+    elif type(ds_down) is xr.DataArray:
+        ds = ds_down.to_dataset()
+    else:
+        ds = ds_down
 
     if var=='t':
         print('Suggestion: use divergent colormap plt.cm.RdBl_r centered around 0C')
 
     alpha=1
     if hillshade:
         ls = LightSource(azdeg=315, altdeg=45)
@@ -88,15 +95,18 @@
                              dy=ds_param.y.diff('y')[0].values,
                              fraction=1.0)
         ax.imshow(shade,
                    extent=[ds_param.x.min(), ds_param.x.max(), ds_param.y.min(), ds_param.y.max()],
                    cmap=plt.cm.gray)
         alpha=0.5
 
-    ds_down[var].sel(point_id=ds_param.cluster_labels).sel(time=time).plot.imshow(alpha=alpha, cmap=cmap, **kwargs)
+    if len(list(ds.keys()))==1:
+        var = list(ds.keys())[0]
+    ds[var].sel(point_id=ds_param.cluster_labels).plot.imshow(alpha=alpha, cmap=cmap, **kwargs)
+
 
     return ax
 
 def map_clusters(ds_down,
                  ds_param,
                  df_centroids=None,
                  **kwargs):
```

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_scale.py` & `topopyscale-0.2.2/TopoPyScale/topo_scale.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,9 @@
 """
 Toposcale functionalities
-
 S. Filhol, Oct 2021
 
 ======= Organization of input data to Toposcale ======
 dem_description (nb_points)
     X
     Y,
     elev,
@@ -16,37 +15,28 @@
     elev_ERA,
 
 horizon_angles (nb_points * bins)
 solar_geom (nb_points * time * 2)
 surface_climate_data (spatial + time + var)
 plevels_climate_data (spatial + time + var + plevel)
 
-
 ======= Dataset naming convention:  =========
 ds_surf => dataset direct from ERA5 single level surface
 ds_plev => dataset direct from ERA5 pressure levels
 
 ds_surf_pt => 3*3 grid ERA5 single surface level around a given point (lat,lon)
 ds_plev_pt => 3*3 grid ERA5 pressure level around a given point (lat,lon)
 
 plev_interp => horizontal interpolation of the 3*3 grid at the point (lat,lon) for the pressure levels
 surf_interp => horizontal interpolation of the 3*3 grid at the point (lat,lon) for the single surface level
 
 top => closest pressure level above the point (lat,lon,elev) for each timesep
 bot => closest pressure level below the point (lat,lon,elev) for each timesep
 
 down_pt => downscaled data time series (t, u, v, q, LW, SW, tp)
-
-TODO:
-- check that transformation from r,t to q for plevels is working fine
-- add metadata to all newly created variables in datasets ds_psurf, ds_plevel, down_pt
-- upscale method for all points in df_centroids:
-    - method (1) simply using a for loop over each row
-    - method (2) concatenate 3*3 grid along an additional dimension to process all points in one go.
-
 """
 import pdb
 
 import pandas as pd
 import xarray as xr
 from pyproj import Transformer
 import numpy as np
@@ -68,14 +58,22 @@
         fun (obj): function to distribute
         fun_param zip(list): zip list of functino arguments
         n_core (int): number o cores
     '''
     if n_cores is None:
         n_cores = mproc.cpu_count() - 2
         print(f'WARNING: number of cores to use not provided. By default {n_cores} cores will be used')
+    elif n_cores > mproc.cpu_count():
+        n_cores = mproc.cpu_count() - 2
+        print(f'WARNING: Only {mproc.cpu_count()} cores available on this machine, reducing n_cores to {n_cores} ')
+
+    # make sure it will run on one core at least
+    if n_cores == 0:
+        n_cores = 1
+
 
     pool = Pool(n_cores)
     pool.starmap(fun, fun_param)
     pool.close()
     pool.join()
     pool = None
 
@@ -140,67 +138,70 @@
     clear_files(f'{project_directory}outputs/tmp')
 
     start_time = time.time()
     tstep_dict = {'1H': 1, '3H': 3, '6H': 6}
     n_digits = len(str(df_centroids.index.max()))
 
     # =========== Open dataset with Dask =================
-    tvec = pd.date_range(start_date, pd.to_datetime(end_date) + pd.to_timedelta('1D'), freq=tstep, closed='left')
+    tvec = pd.date_range(start_date, pd.to_datetime(end_date) + pd.to_timedelta('1D'), freq=tstep, inclusive='left')
 
-    flist_PLEV = glob.glob('inputs/climate/PLEV*.nc')
-    flist_SURF = glob.glob('inputs/climate/SURF*.nc')
+    flist_PLEV = (f'{project_directory}inputs/climate/PLEV*.nc')
+    flist_SURF = (f'{project_directory}inputs/climate/SURF*.nc')
 
-    flist_PLEV.sort()
-    flist_SURF.sort()
 
     def _open_dataset_climate(flist):
+    
+
+        ds_ = xr.open_mfdataset(flist, parallel=True)
+
 
-        ds__list = []
-        for file in flist:
-            ds__list.append(xr.open_dataset(file))
 
-        ds_ = xr.concat(ds__list, dim='time')
         # this block handles the expver dimension that is in downloaded ERA5 data if data is ERA5/ERA5T mix. If only ERA5 or
         # only ERA5T it is not present. ERA5T data can be present in the timewindow T-5days to T -3months, where T is today.
         # https://code.mpimet.mpg.de/boards/1/topics/8961
         # https://confluence.ecmwf.int/display/CUSF/ERA5+CDS+requests+which+return+a+mixture+of+ERA5+and+ERA5T+data
         try:
             # in case of there being an expver dimension and it has two or more values, select first value
             expverN = ds_["expver"].values[0]
             # create new datset when this dimoension only has a single value
             ds_ = ds_.sel(expver=expverN)
             # finally this drops the coordinate
             ds_ = ds_.drop("expver")
         except:
             print("No ERA5T  PRESSURE data present with additional dimension <expver>")
 
-        trans = Transformer.from_crs("epsg:4326", "epsg:" + str(target_EPSG), always_xy=True)
-        nxv,  nyv = np.meshgrid(ds_.longitude.values, ds_.latitude.values)
-        nlons, nlats = trans.transform(nxv, nyv)
-        ds_ = ds_.assign_coords({"latitude": nlats[:, 0], "longitude": nlons[0, :]})
         return ds_
 
     def _subset_climate_dataset(ds_, row, type='plev', pt_id=0):
         print('Preparing {} for point {}'.format(type, row.name))
         # =========== Extract the 3*3 cells centered on a given point ============
-        ind_lat = np.abs(ds_.latitude - row.y).argmin()
-        ind_lon = np.abs(ds_.longitude - row.x).argmin()
+        ind_lat = np.abs(ds_.latitude - row.lat).argmin()
+        ind_lon = np.abs(ds_.longitude - row.lon).argmin()
         #from remote_pdb import set_trace
         #set_trace()
         ds_tmp = ds_.isel(latitude=[ind_lat-1, ind_lat, ind_lat+1], longitude=[ind_lon-1, ind_lon, ind_lon+1]).copy()
         # convert geopotential height to elevation (in m), normalizing by g
         ds_tmp['z'] = ds_tmp.z/g
 
         comp = dict(zlib=True, complevel=5)
         encoding = {var: comp for var in ds_tmp.data_vars}
-        ds_tmp.to_netcdf(f'outputs/tmp/ds_{type}_pt_{pt_id}.nc', engine='h5netcdf', encoding=encoding)
+        ds_tmp.to_netcdf(f'{project_directory}outputs/tmp/ds_{type}_pt_{pt_id}.nc', engine='h5netcdf', encoding=encoding)
         ds_ = None
         ds_tmp = None
 
     ds_plev = _open_dataset_climate(flist_PLEV).sel(time=tvec.values)
+    # Check tvec is within time period of ds_plev.time or return error
+    if ds_plev.time.min() > tvec.min():
+        print(f'ERROR: start date {tvec[0].strftime(format="%Y-%m-%d")} not covered in climate forcing.')
+        return
+    elif ds_plev.time.max() < tvec.max():
+        print(f'ERROR: end date {tvec[-1].strftime(format="%Y-%m-%d")} not covered in climate forcing.')
+        return
+    else:
+        ds_plev = ds_plev.sel(time=tvec.values)
 
     row_list = []
     ds_list = []
     for _, row in df_centroids.iterrows():
         row_list.append(row)
         ds_list.append(ds_plev)
 
@@ -222,34 +223,40 @@
     surf_pt_list = []
     plev_pt_list = []
     ds_solar_list = []
     horizon_da_list = []
     row_list = []
     meta_list = []
     for i, row in df_centroids.iterrows():
-        surf_pt_list.append(xr.open_dataset(f'outputs/tmp/ds_surf_pt_{i}.nc', engine='h5netcdf'))
-        plev_pt_list.append(xr.open_dataset(f'outputs/tmp/ds_plev_pt_{i}.nc', engine='h5netcdf'))
+        surf_pt_list.append(xr.open_dataset(f'{project_directory}outputs/tmp/ds_surf_pt_{i}.nc', engine='h5netcdf'))
+        plev_pt_list.append(xr.open_dataset(f'{project_directory}outputs/tmp/ds_plev_pt_{i}.nc', engine='h5netcdf'))
         ds_solar_list.append(ds_solar.sel(point_id=row.name))
         horizon_da_list.append(horizon_da)
         row_list.append(row)
         meta_list.append({'interp_method':interp_method,
-                         'lw_terrain_flag':lw_terrain_flag,
-                         'tstep':tstep_dict.get(tstep),
+                          'lw_terrain_flag':lw_terrain_flag,
+                          'tstep':tstep_dict.get(tstep),
                           'n_digits':n_digits,
                           'file_pattern':file_pattern})
 
     def pt_downscale_interp(row, ds_plev_pt, ds_surf_pt, meta):
-        pt_id = np.int(row.point_id)
+        pt_id = np.int32(row.point_id)
         print(f'Downscaling t,q,p,tp,ws,wd for point: {pt_id+1}')
 
         # ====== Horizontal interpolation ====================
         interp_method = meta.get('interp_method')
         n_digits = meta.get('n_digits')
 
-        Xs, Ys = np.meshgrid(ds_plev_pt.longitude.values, ds_plev_pt.latitude.values)
+        # convert gridcells coordinates from WGS84 to DEM projection
+        lons, lats = np.meshgrid(ds_plev_pt.longitude.values, ds_plev_pt.latitude.values)
+        trans = Transformer.from_crs("epsg:4326", "epsg:" + str(target_EPSG), always_xy=True)
+        Xs, Ys = trans.transform(lons.flatten(), lats.flatten())
+        Xs = Xs.reshape(lons.shape)
+        Ys = Ys.reshape(lons.shape)
+
         dist = np.sqrt((row.x - Xs)**2 + (row.y - Ys)**2)
         if interp_method == 'idw':
             idw = 1/(dist**2)
             weights = idw / np.sum(idw)  # normalize idw to sum(idw) = 1
         elif interp_method == 'linear':
             weights = dist / np.sum(dist)
         else:
@@ -344,14 +351,25 @@
         down_pt['theta_neg'] = (down_pt.theta < 0) * (down_pt.theta + 2 * np.pi)
         down_pt['theta_pos'] = (down_pt.theta >= 0) * down_pt.theta
         down_pt = down_pt.drop('theta')
         down_pt['wd'] = (down_pt.theta_pos + down_pt.theta_neg)  # direction in Rad
         down_pt['ws'] = np.sqrt(down_pt.u ** 2 + down_pt.v**2)
         down_pt = down_pt.drop(['theta_pos', 'theta_neg', 'month'])
 
+        down_pt.t.attrs = {'units': 'K', 'long_name': 'Temperature', 'standard_name': 'air_temperature'}
+        down_pt.q.attrs = {'units': 'kg kg**-1', 'long_name': 'Specific humidity', 'standard_name': 'specific_humidity'}
+        down_pt.u.attrs = {'units': 'm s**-1', 'long_name': 'U component of wind', 'standard_name': 'eastward_wind'}
+        down_pt.v.attrs = {'units': 'm s**-1', 'long_name': 'V component of wind', 'standard_name': 'northward wind'}
+        down_pt.p.attrs = {'units': 'bar', 'long_name': 'Pression atmospheric', 'standard_name': 'pression_atmospheric'}
+
+        down_pt.ws.attrs = {'units': 'm s**-1', 'long_name': 'Wind speed', 'standard_name': 'wind_speed'}
+        down_pt.wd.attrs = {'units': 'deg', 'long_name': 'Wind direction', 'standard_name': 'wind_direction'}
+        down_pt.tp.attrs = {'units': 'mm hr**-1', 'long_name': 'Precipitation', 'standard_name': 'precipitation'}
+        down_pt.precip_lapse_rate.attrs = {'units': 'mm hr**-1', 'long_name': 'Precipitation after lapse-rate correction', 'standard_name': 'precipitation_after_lapse-rate_correction'}
+
         print(f'---> Storing point {pt_id} to outputs/tmp/')
 
         comp = dict(zlib=True, complevel=5)
         encoding = {var: comp for var in down_pt.data_vars}
         down_pt.to_netcdf(project_directory + 'outputs/tmp/down_pt_{}.nc'.format(str(pt_id).zfill(n_digits)), engine='h5netcdf', encoding=encoding)
 
         comp = dict(zlib=True, complevel=5)
@@ -367,21 +385,21 @@
     plev_pt_list = None
     surf_pt_list = None
 
 
     def pt_downscale_radiations(row, ds_solar, horizon_da, meta):
         # insrt here downscaling routine for sw and lw
         # save file final file
-        pt_id = np.int(row.point_id)
+        pt_id = np.int32(row.point_id)
         n_digits = meta.get('n_digits')
         file_pattern = meta.get('file_pattern')
         print(f'Downscaling LW, SW for point: {pt_id+1}')
 
-        down_pt = xr.open_dataset('outputs/tmp/down_pt_{}.nc'.format(str(pt_id).zfill(n_digits)), engine='h5netcdf')
-        surf_interp = xr.open_dataset('outputs/tmp/surf_interp_{}.nc'.format(str(pt_id).zfill(n_digits)), engine='h5netcdf')
+        down_pt = xr.open_dataset('{}outputs/tmp/down_pt_{}.nc'.format(project_directory, str(pt_id).zfill(n_digits)), engine='h5netcdf')
+        surf_interp = xr.open_dataset('{}outputs/tmp/surf_interp_{}.nc'.format(project_directory, str(pt_id).zfill(n_digits)), engine='h5netcdf')
 
 
         # ======== Longwave downward radiation ===============
         x1, x2 = 0.43, 5.7
         sbc = 5.67e-8
 
         down_pt = mu.mixing_ratio(down_pt, mu.var_era_plevel)
@@ -441,19 +459,19 @@
         down_pt['SW'] = down_pt.SW_diffuse + down_pt.SW_direct
 
         # currently drop azimuth and level as they are coords. Could be passed to variables instead.
         # round(5) required to sufficiently represent specific humidty, q (eg typical value 0.00078)
         down_pt = down_pt.drop(['level']).round(5)
 
         # adding metadata
-        down_pt.LW.attrs = {'units': 'W/m**2', 'standard_name': 'Longwave radiations downward'}
+        down_pt.LW.attrs = {'units': 'W m**-2', 'long_name': 'Surface longwave radiation downwards','standard_name': 'longwave_radiation_downward'}
         down_pt.cse.attrs = {'units': 'xxx', 'standard_name': 'Clear sky emissivity'}
         down_pt = down_pt.drop(['SW_direct_tmp'])
-        down_pt.SW.attrs = {'units': 'W/m**2', 'standard_name': 'Shortwave radiations downward'}
-        down_pt.SW_diffuse.attrs = {'units': 'W/m**2', 'standard_name': 'Shortwave diffuse radiations downward'}
+        down_pt.SW.attrs = {'units': 'W m**-2', 'long_name': 'Surface solar radiation downwards', 'standard_name': 'shortwave_radiation_downward'}
+        down_pt.SW_diffuse.attrs = {'units': 'W m**-2', 'long_name': 'Surface solar diffuse radiation downwards', 'standard_name': 'shortwave_diffuse_radiation_downward'}
 
         num = str(pt_id).zfill(n_digits)
         comp = dict(zlib=True, complevel=5)
         encoding = {var: comp for var in down_pt.data_vars}
         down_pt.to_netcdf(f'{project_directory}outputs/downscaled/{file_pattern.split("*")[0]}{num}{file_pattern.split("*")[1]}', engine='h5netcdf', encoding=encoding, mode='a')
 
         # Clear memory
```

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_sub.py` & `topopyscale-0.2.2/TopoPyScale/topo_sub.py`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/TopoPyScale/topo_utils.py` & `topopyscale-0.2.2/TopoPyScale/topo_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -16,15 +16,16 @@
                      header=None, index_col='datetime',
                      parse_dates={'datetime': [0, 1, 2, 3]},
                      date_parser=lambda x: pd.datetime.strptime(x, '%Y %m %d %H'))
 
     df.columns = ['ISWR', 'ILWR', 'Sf', 'Rf', 'TA', 'RH', 'VW', 'P']
 
     if resample == "TRUE":
-        df = df.resample(freq).apply(resample_func)
+        print('ERROR: line 24 to be fixed!')
+        #df = df.resample(freq).apply(resample_func)
 
     return (df)
 
 
 def FsmSnowParser(file, freq="1H", resample=False):
     '''
     parses FSM output fuiles
@@ -32,23 +33,24 @@
 
     df = pd.read_csv(file, delim_whitespace=True, parse_dates=[[0, 1, 2]], header=None)
     df.set_index(df.iloc[:, 0], inplace=True)
     df.drop(df.columns[[0]], axis=1, inplace=True)
     df.columns = ['albedo', 'Rof', 'HS', 'SWE', 'TS10', 'TS50']
 
     if resample == "TRUE":
-        df = df.resample(freq).apply(resample_func)
+        print('ERROR: line 39 to be fixed!')
+        #df = df.resample(freq).apply(resample_func)
 
     return (df)
 
 
-def FsmPlot(df):
-    df.plot(subplots=True)
-    plt.title("Sample=" + str(sampleN) + " Elev=" + str(np.round(lp.elevation[sampleN])))
-    plt.show()
+#def FsmPlot(df):
+#    df.plot(subplots=True)
+#    plt.title("Sample=" + str(sampleN) + " Elev=" + str(np.round(lp.elevation[sampleN])))
+#    plt.show()
 
 def FsmPlot_ensemble(wdir, simvar, sampleN):
     """
     Function to plot ensemble results for a given variable and point.
 
     Args:
         wdir: full path to sim directory
@@ -211,16 +213,16 @@
     plt.xlabel("Modelled")
     plt.ylabel("Measured")
     plot_xyline(ax)
     plt.show()
 
     myfile = "/home/joel/sim/topoPyscale_davos/outputs/FSM_pt_00.txt"
     df = FsmMetParser(myfile)
-    FsmPlot(df)
+    #FsmPlot(df)
 
     myfile = "/home/joel/sim/topoPyscale_davos/fsm_sims/sim_ENS1_FSM_pt_00.txt"
     df = FsmSnowParser(myfile)
-    FsmPlot(df)
+    #FsmPlot(df)
```

### Comparing `topopyscale-0.2.1/TopoPyScale/topoclass.py` & `topopyscale-0.2.2/TopoPyScale/topoclass.py`

 * *Files 1% similar despite different names*

```diff
@@ -39,16 +39,21 @@
     """
 
     def __init__(self, config_file):
 
         try:
             with open(config_file, 'r') as f:
                 self.config = DefaultMunch.fromYAML(f)
+
+
+            if self.config.project.directory is None:
+                self.config.project.directory = os.getcwd() + '/'
+
         except IOError:
-            print('ERROR: config file does not exist. Check path.')
+            print(f'ERROR: config file does not exist. \n\t Current file path: {config_file}\n\t Current working directory: {os.getcwd()}')
 
         if self.config.outputs.file.clean_outputs:
             # remove outputs directory because if results already exist this causes concat of netcdf files
             try:
                 shutil.rmtree(self.config.project.directory + '/outputs/')
                 print('---> Output directory cleaned')
             except:
@@ -252,14 +257,15 @@
         """
         self.toposub.df_centroids = pd.read_csv(
             self.config.project.directory + 'inputs/dem/' + self.config.sampling.points.csv_file, **kwargs)
         self.toposub.df_centroids['point_id'] = self.toposub.df_centroids.index.astype(int)
         self.toposub.df_centroids = tp.extract_pts_param(self.toposub.df_centroids, self.toposub.ds_param,
                                                          method=method)
 
+
     def extract_topo_cluster_param(self):
         """
         Function to segment a DEM in clusters and retain only the centroids of each cluster.
 
         :return:
 
         TODO:
@@ -323,14 +329,20 @@
 
                 # implement the case one wann run both toposub and a list of points
                 print('ERROR: method not yet implemented')
 
             else:
                 print('ERROR: Extraction method not available')
 
+
+            self.toposub.df_centroids['lon'], self.toposub.df_centroids['lat'] = tp.convert_epsg_pts(self.toposub.df_centroids.x,
+                                                                                              self.toposub.df_centroids.y,
+                                                                                              self.config.dem.epsg,
+                                                                                              4326)
+
             # Store dataframe to pickle
             self.toposub.df_centroids.to_pickle(
                 self.config.project.directory + 'outputs/' + self.config.outputs.file.df_centroids)
             print(f'---> Centroids file {self.config.outputs.file.df_centroids} saved')
 
     class TimeSplitter():
         def __init__(self, start, end, period, ds_solar_fname, downscale_fname):
@@ -507,36 +519,47 @@
         - merge monthly data into one file (cdo?)- this creates massive slow down!
         """
         lonW = self.config.project.extent.get('lonW') - 0.4
         lonE = self.config.project.extent.get('lonE') + 0.4
         latN = self.config.project.extent.get('latN') + 0.4
         latS = self.config.project.extent.get('latS') - 0.4
 
+        # if keyword exists in config set realtime to value (True/False)
+        if self.config.climate[self.config.project.climate].realtime:
+            realtime=self.config.climate[self.config.project.climate].realtime
+        # else set realtime to False
+        else:
+            realtime=False
+
+
+
         # retreive ERA5 surface data
         fe.retrieve_era5(
             self.config.climate[self.config.project.climate].product,
             self.config.project.start,
             self.config.project.end,
             self.config.climate.path,
             latN, latS, lonE, lonW,
             self.config.climate[self.config.project.climate].timestep,
             self.config.climate[self.config.project.climate].download_threads,
-            surf_plev='surf'
+            surf_plev='surf',
+            realtime=realtime
         )
         # retrieve era5 plevels
         fe.retrieve_era5(
             self.config.climate[self.config.project.climate].product,
             self.config.project.start,
             self.config.project.end,
             self.config.climate.path,
             latN, latS, lonE, lonW,
             self.config.climate[self.config.project.climate].timestep,
             self.config.climate[self.config.project.climate].download_threads,
             surf_plev='plev',
             plevels=self.config.climate[self.config.project.climate].plevels,
+            realtime=realtime
         )
 
     def get_WMO_observations(self):
         """
         Function to download and parse in-situ data from WMO database
         """
         lonW = self.config.project.extent.get('lonW') - 0.4
@@ -547,15 +570,15 @@
         df = pd.DataFrame()
         df['dates'] = pd.date_range(self.config.project.start,
                                     self.config.project.end, freq='M')
         df['month'] = df.dates.dt.month
         df['year'] = df.dates.dt.year
 
         bbox = [latS, lonW, latN, lonE]
-        for year in years:
+        for year in df.year.unique():
             # API only accept one year request
             tpo.fetch_WMO_insitu_observations(years=year,
                                               months=list(df.month.unique().astype(str)),
                                               bbox=bbox)
         tpo.parse_WMO_insitu_observations()
 
     def to_cryogrid(self, fname_format='Cryogrid_pt_*.nc', precip_partition='continuous'):
@@ -621,15 +644,18 @@
         function to export toposcale output to one single generic netcdf format, compressed
 
         Args:
             file_out (str): name of export file
             variables (list str): list of variable to export. Default exports all variables
         """
         if variables is None:
-            variables = list(self.downscaled_pts.keys())
+            if (type(self.config.outputs.variables) is not list) or (self.config.outputs.variables is None):
+                variables = list(self.downscaled_pts.keys())
+            else:
+                variables = self.config.outputs.variables
 
         te.to_netcdf(self.downscaled_pts[variables], f'{self.config.project.directory}outputs/' + file_out, variables)
         print('---> File {} saved'.format(file_out))
 
     def to_snowpack(self, fname_format='smet_pt_*.smet'):
         """
         function to export toposcale output to FSM format
```

### Comparing `topopyscale-0.2.1/logo.svg` & `topopyscale-0.2.2/logo.svg`

 * *Files identical despite different names*

### Comparing `topopyscale-0.2.1/setup.py` & `topopyscale-0.2.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 
 this_directory = path.abspath(path.dirname(__file__))
 with open(path.join(this_directory, 'README.md')) as f:
     long_description = f.read()
 
 setup(
     name='topopyscale',
-    version='0.2.1',
+    version='0.2.2',
     description='A Python package to perform climate downscaling at the hillslope scale',
     long_description=long_description,
 
     # The project's main homepage.
     url='https://github.com/ArcticSnow/TopoPyScale',
     download_url = 'https://github.com/ArcticSnow/TopoPyScale/releases/latest',
     project_urls={
@@ -43,15 +43,15 @@
         'Topic :: Scientific/Engineering :: Atmospheric Science',
 
         # Pick your license as you wish (should match "license" above)
         'License :: OSI Approved :: MIT License',
 
         # Specify the Python versions you support here. In particular, ensure
         # that you indicate whether you support Python 2, Python 3 or both.
-        'Programming Language :: Python :: 3.8',
+        'Programming Language :: Python :: 3.9',
     ],
 
     # What does your project relate to?
     keywords=['climate', 'downscaling', 'meteorology', 'xarray'],
     packages=find_packages(),
     python_requires='>=3.8',
     install_requires=['xarray[complete]',
```

### Comparing `topopyscale-0.2.1/topopyscale.egg-info/PKG-INFO` & `topopyscale-0.2.2/topopyscale.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: topopyscale
-Version: 0.2.1
+Version: 0.2.2
 Summary: A Python package to perform climate downscaling at the hillslope scale
 Home-page: https://github.com/ArcticSnow/TopoPyScale
 Download-URL: https://github.com/ArcticSnow/TopoPyScale/releases/latest
 Author: ['Simon Filhol', 'Joel Fiddes', 'Kristoffer Aalstad']
 Author-email: simon.filhol@geo.uio.no
 License: MIT
 Project-URL: Documentation, https://topopyscale.readthedocs.io/en/latest/
@@ -13,25 +13,30 @@
 Keywords: climate,downscaling,meteorology,xarray
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Science/Research
 Classifier: Topic :: Scientific/Engineering :: Visualization
 Classifier: Topic :: Scientific/Engineering :: Hydrology
 Classifier: Topic :: Scientific/Engineering :: Atmospheric Science
 Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 
 
 [![DOI](https://zenodo.org/badge/411249045.svg)](https://zenodo.org/badge/latestdoi/411249045)
 [![GitHub license](https://img.shields.io/github/license/ArcticSnow/TopoPyScale)](https://github.com/ArcticSnow/TopoPyScale/blob/main/LICENSE)
 ![GitHub release (latest by date)](https://img.shields.io/github/v/release/ArcticSnow/TopoPyScale)
 <a href="https://joss.theoj.org/papers/91621581b2d0c097495fdd1e58179e87"><img src="https://joss.theoj.org/papers/91621581b2d0c097495fdd1e58179e87/status.svg"></a>
+[![][docs-dev-img]][docs-dev-url]
+![Test](https://github.com/ArcticSnow/TopoPyScale/actions/workflows/test_topopyscale.yml/badge.svg)
+
+[docs-dev-img]: https://img.shields.io/badge/docs-latest-blue.svg
+[docs-dev-url]: https://topopyscale.readthedocs.io
 
 # TopoPyScale
 Python version of Toposcale packaged as a Pypi library. Toposcale is an original idea of Joel Fiddes to perform topography-based downscaling of climate data to the hillslope scale.
 
 Documentation avalaible: https://topopyscale.readthedocs.io
 
 ![](https://github.com/ArcticSnow/TopoPyScale/blob/main/JOSS/temperature_comparison_crop_scaled.jpg)
@@ -41,33 +46,29 @@
 - Fiddes, J. and Gruber, S.: TopoSUB: a tool for efficient large area numerical modelling in complex topography at sub-grid scales, Geosci. Model Dev., 5, 1245–1257, https://doi.org/10.5194/gmd-5-1245-2012, 2012. 
 
 Kristoffer Aalstad has a Matlab implementation: https://github.com/krisaalstad/TopoLAB
 
 ## Contribution Workflow
 **Please follow these simple rules:**
 1. a bug -> fix it! 
-2. an idea or a bug you cannot fix? -> create a new [issue](https://github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one exist, then add material to tit.
-3. wanna develop a new feature/idea? -> create a new branch. Do the development. Merge with main branch when accomplished.
-4. Create release version when significant improvements and bug fixes have been done. Coordinate with others
+2. an idea or a bug you cannot fix? -> create a new [issue](https://github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one exist, then add material to it.
+3. wanna develop a new feature/idea? -> create a new branch. Go wild. Merge with main branch when accomplished.
+4. Create release version when significant improvements and bug fixes have been done. Coordinate with others on [Discussions](https://github.com/ArcticSnow/TopoPyScale/discussions)
 
 **Create a new release:**
 Follow procedure and conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY
 
-And check out our Slack: tscaleworkspace.slack.com
+Our forum is now on [Github Discussions](https://github.com/ArcticSnow/TopoPyScale/discussions). Come visit!
 
-Contributors to the current version (2021) are:
-- Simon Filhol
-- Joel Fiddes
-- Kristoffer Aalstad
 
 ## Design
 
 1. Inputs
     - Climate data from reanalysis (ERA5, etc)
-    - Climate data from future projections (CORDEX) (not avail.)
+    - Climate data from future projections (CORDEX) (TBD)
     - DEM from local source, or fetch from public repository: SRTM, ArcticDEM, ASTER
 2. Run TopoScale
     - compute derived values (from DEM)
     - toposcale (k-mean clustering)
     - interpolation (bilinear, inverse square dist.)
 3. Output
     - Cryogrid format
@@ -76,27 +77,37 @@
     - Snowmodel format
     - basic netcfd
     - For each method, have the choice to output either the abstract cluster points, or the gridded product after interpolation
 4. Validation toolset
     - validation to local observation timeseries
     - plotting
 5. Gap filling algorithm
-    - random forest temporal gap filling
+    - random forest temporal gap filling (TBD)
 
 Validation (4) and Gap filling (4) are future implementation.
 
 ## Installation
 
+We have now added an environments.yml file to handle versions of depencencies that are tested with the current codebase, to use this run:
+
+`conda env create -f environment.yml`
+
+Alternatively you can follow this method for dependencies (to be deprecated):
+
 ```bash
-conda create -n downscaling python=3.8 ipython
+conda create -n downscaling python=3.9 ipython
 conda activate downscaling
 
 # Recomended way to install dependencies:
-conda install -c conda-forge xarray matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask
+conda install -c conda-forge xarray matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask rioxarray
+```
+
+Then install the code:
 
+```
 # OPTION 1 (Pypi release):
 pip install TopoPyScale
 
 # OPTION 2 (development):
 cd github  # navigate to where you want to clone TopoPyScale
 git clone git@github.com:ArcticSnow/TopoPyScale.git
 pip install -e TopoPyScale    #install a development version
```

#### html2text {}

```diff
@@ -1,85 +1,93 @@
-Metadata-Version: 2.1 Name: topopyscale Version: 0.2.1 Summary: A Python
+Metadata-Version: 2.1 Name: topopyscale Version: 0.2.2 Summary: A Python
 package to perform climate downscaling at the hillslope scale Home-page: https:
 //github.com/ArcticSnow/TopoPyScale Download-URL: https://github.com/
 ArcticSnow/TopoPyScale/releases/latest Author: ['Simon Filhol', 'Joel Fiddes',
 'Kristoffer Aalstad'] Author-email: simon.filhol@geo.uio.no License: MIT
 Project-URL: Documentation, https://topopyscale.readthedocs.io/en/latest/
 Project-URL: Source, https://github.com/ArcticSnow/TopoPyScale Project-URL:
 Examples, https://github.com/ArcticSnow/TopoPyScale_examples Keywords:
 climate,downscaling,meteorology,xarray Classifier: Development Status :: 4 -
 Beta Classifier: Intended Audience :: Science/Research Classifier: Topic ::
 Scientific/Engineering :: Visualization Classifier: Topic :: Scientific/
 Engineering :: Hydrology Classifier: Topic :: Scientific/Engineering ::
 Atmospheric Science Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.8 Requires-Python: >=3.8
+Classifier: Programming Language :: Python :: 3.9 Requires-Python: >=3.8
 Description-Content-Type: text/markdown License-File: LICENSE [![DOI](https://
 zenodo.org/badge/411249045.svg)](https://zenodo.org/badge/latestdoi/411249045)
 [![GitHub license](https://img.shields.io/github/license/ArcticSnow/
 TopoPyScale)](https://github.com/ArcticSnow/TopoPyScale/blob/main/LICENSE) !
 [GitHub release (latest by date)](https://img.shields.io/github/v/release/
 ArcticSnow/TopoPyScale) [https://joss.theoj.org/papers/
-91621581b2d0c097495fdd1e58179e87/status.svg] # TopoPyScale Python version of
-Toposcale packaged as a Pypi library. Toposcale is an original idea of Joel
-Fiddes to perform topography-based downscaling of climate data to the hillslope
-scale. Documentation avalaible: https://topopyscale.readthedocs.io ![](https://
-github.com/ArcticSnow/TopoPyScale/blob/main/JOSS/
-temperature_comparison_crop_scaled.jpg) **References:** - Fiddes, J. and
-Gruber, S.: TopoSCALE v.1.0: downscaling gridded climate data in complex
+91621581b2d0c097495fdd1e58179e87/status.svg] [![][docs-dev-img]][docs-dev-url]
+![Test](https://github.com/ArcticSnow/TopoPyScale/actions/workflows/
+test_topopyscale.yml/badge.svg) [docs-dev-img]: https://img.shields.io/badge/
+docs-latest-blue.svg [docs-dev-url]: https://topopyscale.readthedocs.io #
+TopoPyScale Python version of Toposcale packaged as a Pypi library. Toposcale
+is an original idea of Joel Fiddes to perform topography-based downscaling of
+climate data to the hillslope scale. Documentation avalaible: https://
+topopyscale.readthedocs.io ![](https://github.com/ArcticSnow/TopoPyScale/blob/
+main/JOSS/temperature_comparison_crop_scaled.jpg) **References:** - Fiddes, J.
+and Gruber, S.: TopoSCALE v.1.0: downscaling gridded climate data in complex
 terrain, Geosci. Model Dev., 7, 387â405, https://doi.org/10.5194/gmd-7-387-
 2014, 2014. - Fiddes, J. and Gruber, S.: TopoSUB: a tool for efficient large
 area numerical modelling in complex topography at sub-grid scales, Geosci.
 Model Dev., 5, 1245â1257, https://doi.org/10.5194/gmd-5-1245-2012, 2012.
 Kristoffer Aalstad has a Matlab implementation: https://github.com/krisaalstad/
 TopoLAB ## Contribution Workflow **Please follow these simple rules:** 1. a bug
 -> fix it! 2. an idea or a bug you cannot fix? -> create a new [issue](https://
 github.com/ArcticSnow/TopoPyScale/issues) if none doesn't already exist. If one
-exist, then add material to tit. 3. wanna develop a new feature/idea? -> create
-a new branch. Do the development. Merge with main branch when accomplished. 4.
-Create release version when significant improvements and bug fixes have been
-done. Coordinate with others **Create a new release:** Follow procedure and
-conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY And check
-out our Slack: tscaleworkspace.slack.com Contributors to the current version
-(2021) are: - Simon Filhol - Joel Fiddes - Kristoffer Aalstad ## Design 1.
-Inputs - Climate data from reanalysis (ERA5, etc) - Climate data from future
-projections (CORDEX) (not avail.) - DEM from local source, or fetch from public
-repository: SRTM, ArcticDEM, ASTER 2. Run TopoScale - compute derived values
-(from DEM) - toposcale (k-mean clustering) - interpolation (bilinear, inverse
-square dist.) 3. Output - Cryogrid format - FSM format - CROCUS format -
-Snowmodel format - basic netcfd - For each method, have the choice to output
-either the abstract cluster points, or the gridded product after interpolation
-4. Validation toolset - validation to local observation timeseries - plotting
-5. Gap filling algorithm - random forest temporal gap filling Validation (4)
-and Gap filling (4) are future implementation. ## Installation ```bash conda
-create -n downscaling python=3.8 ipython conda activate downscaling #
-Recomended way to install dependencies: conda install -c conda-forge xarray
-matplotlib scikit-learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask #
-OPTION 1 (Pypi release): pip install TopoPyScale # OPTION 2 (development): cd
-github # navigate to where you want to clone TopoPyScale git clone
-git@github.com:ArcticSnow/TopoPyScale.git pip install -e TopoPyScale #install a
-development version #---------------------------------------------------------
-- # OPTIONAL: if using jupyter lab # add this new Python kernel to your jupyter
-lab PATH python -m ipykernel install --user --name downscaling # Tool for
-generating documentation from code docstring pip install lazydocs ``` Then you
-need to setup your `cdsapi` with the Copernicus API key system. Follow [this
-tutorial](https://cds.climate.copernicus.eu/api-how-to#install-the-cds-api-key)
-after creating an account with [Copernicus](https://cds.climate.copernicus.eu/
-). On Linux, create a file `nano ~/.cdsapirc` with inside: ``` url: https://
-cds.climate.copernicus.eu/api/v2 key: {uid}:{api-key} ``` ## Basic usage 1.
-Setup your Python environment 2. Create your project directory 3. Configure the
-file `config.ini` to fit your problem (see [`config.yml`](https://github.com/
-ArcticSnow/TopoPyScale_examples/blob/main/ex1_norway_finse/config_spatial.yml)
-for an example) 4. Run TopoPyScale ```python import pandas as pd from
-TopoPyScale import topoclass as tc from matplotlib import pyplot as plt #
-========= STEP 1 ========== # Load Configuration config_file = './config.yml'
-mp = tc.Topoclass(config_file) # Compute parameters of the DEM (slope, aspect,
-sky view factor) mp.compute_dem_param() # ========== STEP 2 =========== #
-Extract DEM parameters for points of interest (centroids or physical points)
-mp.extract_topo_param() # ----- Option 1: # Compute clustering of the input DEM
-and extract cluster centroids #mp.extract_dem_cluster_param() # plot clusters
+exist, then add material to it. 3. wanna develop a new feature/idea? -> create
+a new branch. Go wild. Merge with main branch when accomplished. 4. Create
+release version when significant improvements and bug fixes have been done.
+Coordinate with others on [Discussions](https://github.com/ArcticSnow/
+TopoPyScale/discussions) **Create a new release:** Follow procedure and
+conventions described in: https://www.youtube.com/watch?v=Ob9llA_QhQY Our forum
+is now on [Github Discussions](https://github.com/ArcticSnow/TopoPyScale/
+discussions). Come visit! ## Design 1. Inputs - Climate data from reanalysis
+(ERA5, etc) - Climate data from future projections (CORDEX) (TBD) - DEM from
+local source, or fetch from public repository: SRTM, ArcticDEM, ASTER 2. Run
+TopoScale - compute derived values (from DEM) - toposcale (k-mean clustering) -
+interpolation (bilinear, inverse square dist.) 3. Output - Cryogrid format -
+FSM format - CROCUS format - Snowmodel format - basic netcfd - For each method,
+have the choice to output either the abstract cluster points, or the gridded
+product after interpolation 4. Validation toolset - validation to local
+observation timeseries - plotting 5. Gap filling algorithm - random forest
+temporal gap filling (TBD) Validation (4) and Gap filling (4) are future
+implementation. ## Installation We have now added an environments.yml file to
+handle versions of depencencies that are tested with the current codebase, to
+use this run: `conda env create -f environment.yml` Alternatively you can
+follow this method for dependencies (to be deprecated): ```bash conda create -
+n downscaling python=3.9 ipython conda activate downscaling # Recomended way to
+install dependencies: conda install -c conda-forge xarray matplotlib scikit-
+learn pandas numpy netcdf4 h5netcdf rasterio pyproj dask rioxarray ``` Then
+install the code: ``` # OPTION 1 (Pypi release): pip install TopoPyScale #
+OPTION 2 (development): cd github # navigate to where you want to clone
+TopoPyScale git clone git@github.com:ArcticSnow/TopoPyScale.git pip install -
+e TopoPyScale #install a development version #---------------------------------
+------------------------- # OPTIONAL: if using jupyter lab # add this new
+Python kernel to your jupyter lab PATH python -m ipykernel install --user --
+name downscaling # Tool for generating documentation from code docstring pip
+install lazydocs ``` Then you need to setup your `cdsapi` with the Copernicus
+API key system. Follow [this tutorial](https://cds.climate.copernicus.eu/api-
+how-to#install-the-cds-api-key) after creating an account with [Copernicus]
+(https://cds.climate.copernicus.eu/). On Linux, create a file `nano
+~/.cdsapirc` with inside: ``` url: https://cds.climate.copernicus.eu/api/v2
+key: {uid}:{api-key} ``` ## Basic usage 1. Setup your Python environment 2.
+Create your project directory 3. Configure the file `config.ini` to fit your
+problem (see [`config.yml`](https://github.com/ArcticSnow/TopoPyScale_examples/
+blob/main/ex1_norway_finse/config_spatial.yml) for an example) 4. Run
+TopoPyScale ```python import pandas as pd from TopoPyScale import topoclass as
+tc from matplotlib import pyplot as plt # ========= STEP 1 ========== # Load
+Configuration config_file = './config.yml' mp = tc.Topoclass(config_file) #
+Compute parameters of the DEM (slope, aspect, sky view factor)
+mp.compute_dem_param() # ========== STEP 2 =========== # Extract DEM parameters
+for points of interest (centroids or physical points) mp.extract_topo_param() #
+----- Option 1: # Compute clustering of the input DEM and extract cluster
+centroids #mp.extract_dem_cluster_param() # plot clusters
 #mp.toposub.plot_clusters_map() # plot sky view factor
 #mp.toposub.plot_clusters_map(var='svf', cmap=plt.cm.viridis) # ------ Option
 2: # inidicate in the config file the .csv file containing a list of point
 coordinates (!!! must same coordinate system as DEM !!!) #mp.extract_pts_param
 (method='linear',index_col=0) # ========= STEP 3 ========== # compute solar
 geometry and horizon angles mp.compute_solar_geometry() mp.compute_horizon() #
 ========= STEP 4 ========== # Perform the downscaling mp.downscale_climate() #
```

### Comparing `topopyscale-0.2.1/topopyscale.egg-info/SOURCES.txt` & `topopyscale-0.2.2/topopyscale.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -1,16 +1,18 @@
 .gitignore
 LICENSE
 MANIFEST.in
 README.md
+environment.yml
 logo.svg
 setup.cfg
 setup.py
 .github/workflows/draft-pdf.yml
 .github/workflows/python-publish.yml
+.github/workflows/test_topopyscale.yml
 JOSS/figure2.png
 JOSS/paper.bib
 JOSS/paper.md
 JOSS/temperature_comparison_crop_scaled.jpg
 TopoPyScale/__init__.py
 TopoPyScale/fetch_dem.py
 TopoPyScale/fetch_era5.py
```

