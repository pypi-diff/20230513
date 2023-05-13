# Comparing `tmp/IMDbTraktSyncer-1.1.0.tar.gz` & `tmp/IMDbTraktSyncer-1.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "IMDbTraktSyncer-1.1.0.tar", last modified: Sat May 13 08:17:30 2023, max compression
+gzip compressed data, was "IMDbTraktSyncer-1.1.1.tar", last modified: Sat May 13 08:57:09 2023, max compression
```

## Comparing `IMDbTraktSyncer-1.1.0.tar` & `IMDbTraktSyncer-1.1.1.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 08:17:30.402412 IMDbTraktSyncer-1.1.0/
-drwxrwxrwx   0        0        0        0 2023-05-13 08:17:30.366967 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/
--rw-rw-rw-   0        0        0    10477 2023-05-13 08:14:40.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/IMDbTraktSyncer.py
--rw-rw-rw-   0        0        0        0 2023-04-29 22:05:24.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/__init__.py
--rw-rw-rw-   0        0        0     1805 2023-05-07 03:12:27.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/authTrakt.py
--rw-rw-rw-   0        0        0      642 2023-05-07 03:12:27.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/checkChromedriver.py
--rw-rw-rw-   0        0        0     2038 2023-05-13 08:07:22.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/imdbRatings.py
--rw-rw-rw-   0        0        0     1408 2023-05-13 08:07:19.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/traktRatings.py
--rw-rw-rw-   0        0        0     2516 2023-05-07 03:12:27.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/verifyCredentials.py
-drwxrwxrwx   0        0        0        0 2023-05-13 08:17:30.399414 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/
--rw-rw-rw-   0        0        0     6624 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      491 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       73 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       29 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/requires.txt
--rw-rw-rw-   0        0        0       16 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1079 2023-04-26 18:19:27.000000 IMDbTraktSyncer-1.1.0/LICENSE
--rw-rw-rw-   0        0        0     6624 2023-05-13 08:17:30.401414 IMDbTraktSyncer-1.1.0/PKG-INFO
--rw-rw-rw-   0        0        0     6004 2023-05-13 08:16:25.000000 IMDbTraktSyncer-1.1.0/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 08:17:30.402412 IMDbTraktSyncer-1.1.0/setup.cfg
--rw-rw-rw-   0        0        0     1287 2023-05-13 08:17:03.000000 IMDbTraktSyncer-1.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 08:57:09.302025 IMDbTraktSyncer-1.1.1/
+drwxrwxrwx   0        0        0        0 2023-05-13 08:57:09.279555 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/
+-rw-rw-rw-   0        0        0    10477 2023-05-13 08:29:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/IMDbTraktSyncer.py
+-rw-rw-rw-   0        0        0        0 2023-04-29 22:05:24.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/__init__.py
+-rw-rw-rw-   0        0        0     1805 2023-05-13 08:29:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/authTrakt.py
+-rw-rw-rw-   0        0        0      642 2023-05-13 08:29:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/checkChromedriver.py
+-rw-rw-rw-   0        0        0     2060 2023-05-13 08:50:24.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/imdbRatings.py
+-rw-rw-rw-   0        0        0     1408 2023-05-13 08:29:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/traktRatings.py
+-rw-rw-rw-   0        0        0     2516 2023-05-13 08:29:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/verifyCredentials.py
+drwxrwxrwx   0        0        0        0 2023-05-13 08:57:09.299528 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer.egg-info/
+-rw-rw-rw-   0        0        0     6624 2023-05-13 08:57:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      491 2023-05-13 08:57:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 08:57:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       73 2023-05-13 08:57:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       29 2023-05-13 08:57:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       16 2023-05-13 08:57:09.000000 IMDbTraktSyncer-1.1.1/IMDbTraktSyncer.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1079 2023-04-26 18:19:27.000000 IMDbTraktSyncer-1.1.1/LICENSE
+-rw-rw-rw-   0        0        0     6624 2023-05-13 08:57:09.301529 IMDbTraktSyncer-1.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0     6004 2023-05-13 08:16:25.000000 IMDbTraktSyncer-1.1.1/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 08:57:09.302524 IMDbTraktSyncer-1.1.1/setup.cfg
+-rw-rw-rw-   0        0        0     1287 2023-05-13 08:56:51.000000 IMDbTraktSyncer-1.1.1/setup.py
```

### Comparing `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/IMDbTraktSyncer.py` & `IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/IMDbTraktSyncer.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/authTrakt.py` & `IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/authTrakt.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/checkChromedriver.py` & `IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/checkChromedriver.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/imdbRatings.py` & `IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/imdbRatings.py`

 * *Files 1% similar despite different names*

```diff
@@ -45,15 +45,15 @@
                     type = "movie"
                 imdb_ratings.append({'Title': title, 'Year': year, 'Rating': rating, 'ID': imdb_id, 'Type': type})
     except FileNotFoundError:
         print('Ratings file not found')
         
     # Delete csv files
     for file in os.listdir(directory):
-        if file.endswith('.csv'):
+        if file.endswith('.csv') and 'ratings' in file:
             os.remove(os.path.join(directory, file))
 
     print('Getting IMDB Ratings Complete')
     
     return imdb_ratings
```

### Comparing `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/traktRatings.py` & `IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/traktRatings.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/verifyCredentials.py` & `IMDbTraktSyncer-1.1.1/IMDbTraktSyncer/verifyCredentials.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/PKG-INFO` & `IMDbTraktSyncer-1.1.1/IMDbTraktSyncer.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IMDbTraktSyncer
-Version: 1.1.0
+Version: 1.1.1
 Summary: This python script will sync user ratings for Movies and TV Shows both ways between Trakt and IMDb.
 Home-page: https://github.com/RileyXX/IMDb-Trakt-Syncer
 Keywords: python,video,trakt,imdb,ratings,sync,movies,tv shows
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: End Users/Desktop
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
```

### Comparing `IMDbTraktSyncer-1.1.0/LICENSE` & `IMDbTraktSyncer-1.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.1.0/PKG-INFO` & `IMDbTraktSyncer-1.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IMDbTraktSyncer
-Version: 1.1.0
+Version: 1.1.1
 Summary: This python script will sync user ratings for Movies and TV Shows both ways between Trakt and IMDb.
 Home-page: https://github.com/RileyXX/IMDb-Trakt-Syncer
 Keywords: python,video,trakt,imdb,ratings,sync,movies,tv shows
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: End Users/Desktop
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
```

### Comparing `IMDbTraktSyncer-1.1.0/README.md` & `IMDbTraktSyncer-1.1.1/README.md`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.1.0/setup.py` & `IMDbTraktSyncer-1.1.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 #To upload package: twine upload dist/*
 
 here = os.path.abspath(os.path.dirname(__file__))
 
 with codecs.open(os.path.join(here, "README.md"), encoding="utf-8") as fh:
     long_description = "\n" + fh.read()
 
-VERSION = '1.1.0'
+VERSION = '1.1.1'
 DESCRIPTION = 'This python script will sync user ratings for Movies and TV Shows both ways between Trakt and IMDb.'
 
 # Setting up
 setup(
     name="IMDbTraktSyncer",
     version=VERSION,
     description=DESCRIPTION,
```

