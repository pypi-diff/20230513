# Comparing `tmp/cv2geojson-0.0.5.tar.gz` & `tmp/cv2geojson-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cv2geojson-0.0.5.tar", last modified: Tue Apr  4 18:12:29 2023, max compression
+gzip compressed data, was "cv2geojson-0.0.6.tar", last modified: Sat May 13 12:37:23 2023, max compression
```

## Comparing `cv2geojson-0.0.5.tar` & `cv2geojson-0.0.6.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-04-04 18:12:29.021809 cv2geojson-0.0.5/
--rw-rw-rw-   0        0        0     1090 2023-04-04 10:50:06.000000 cv2geojson-0.0.5/LICENSE
--rw-rw-rw-   0        0        0     1970 2023-04-04 18:12:29.021809 cv2geojson-0.0.5/PKG-INFO
--rw-rw-rw-   0        0        0     1286 2023-04-04 17:47:03.000000 cv2geojson-0.0.5/README.md
-drwxrwxrwx   0        0        0        0 2023-04-04 18:12:29.013809 cv2geojson-0.0.5/cv2geojson/
--rw-rw-rw-   0        0        0       37 2023-04-04 12:24:11.000000 cv2geojson-0.0.5/cv2geojson/__init__.py
--rw-rw-rw-   0        0        0     4642 2023-04-04 11:27:57.000000 cv2geojson-0.0.5/cv2geojson/geocontour.py
-drwxrwxrwx   0        0        0        0 2023-04-04 18:12:29.020809 cv2geojson-0.0.5/cv2geojson.egg-info/
--rw-rw-rw-   0        0        0     1970 2023-04-04 18:12:28.000000 cv2geojson-0.0.5/cv2geojson.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      249 2023-04-04 18:12:29.000000 cv2geojson-0.0.5/cv2geojson.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-04 18:12:28.000000 cv2geojson-0.0.5/cv2geojson.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       28 2023-04-04 18:12:28.000000 cv2geojson-0.0.5/cv2geojson.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-04-04 18:12:28.000000 cv2geojson-0.0.5/cv2geojson.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      729 2023-04-04 18:12:10.000000 cv2geojson-0.0.5/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-04-04 18:12:29.021809 cv2geojson-0.0.5/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 12:37:23.597352 cv2geojson-0.0.6/
+-rw-rw-rw-   0        0        0     1090 2023-04-04 10:50:06.000000 cv2geojson-0.0.6/LICENSE
+-rw-rw-rw-   0        0        0     2902 2023-05-13 12:37:23.597352 cv2geojson-0.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0     2165 2023-05-13 12:26:09.000000 cv2geojson-0.0.6/README.md
+-rw-rw-rw-   0        0        0      774 2023-05-13 12:37:02.000000 cv2geojson-0.0.6/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 12:37:23.597352 cv2geojson-0.0.6/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 12:37:23.581721 cv2geojson-0.0.6/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 12:37:23.581721 cv2geojson-0.0.6/src/cv2geojson/
+-rw-rw-rw-   0        0        0    12518 2023-05-13 11:18:59.000000 cv2geojson-0.0.6/src/cv2geojson/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:37:23.597352 cv2geojson-0.0.6/src/cv2geojson.egg-info/
+-rw-rw-rw-   0        0        0     2902 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      248 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       28 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 12:37:23.000000 cv2geojson-0.0.6/src/cv2geojson.egg-info/top_level.txt
```

### Comparing `cv2geojson-0.0.5/LICENSE` & `cv2geojson-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `cv2geojson-0.0.5/pyproject.toml` & `cv2geojson-0.0.6/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 [project]
 name = "cv2geojson"
-version = "0.0.5"
+version = "0.0.6"
 authors = [
   { name="Mohsen Farzi", email="mhnfarzi@gmail.com" },
 ]
 description = "Export contour annotations as geojson formatted data"
 readme = "README.md"
 requires-python = ">=3.7"
 dependencies=['opencv-python', 'numpy', 'geojson']
 keywords=['python', 'geojson', 'opencv', 'contours', 'polygons']
 classifiers = [
     "Development Status :: 1 - Planning",
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
     "Intended Audience :: Developers",
+    "Intended Audience :: Science/Research"
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/mfarzi/cv2geojson"
 "Bug Tracker" = "https://github.com/mfarzi/cv2geojson/issues"
```

