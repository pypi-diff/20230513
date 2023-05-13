# Comparing `tmp/localcider-0.1.9.post3.tar.gz` & `tmp/localcider-0.1.9.post4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/localcider-0.1.9.post3.tar", last modified: Tue Oct 11 23:57:07 2016, max compression
+gzip compressed data, was "dist/localcider-0.1.9.post4.tar", last modified: Tue Oct 11 23:58:17 2016, max compression
```

## Comparing `localcider-0.1.9.post3.tar` & `localcider-0.1.9.post4.tar`

### file list

```diff
@@ -1,46 +1,46 @@
-drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/
-drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/docs/
--rw-r--r--   0 alex       (501) staff       (20)       73 2014-08-11 18:19:14.000000 localcider-0.1.9.post3/docs/doc.txt
--rw-r--r--   0 alex       (501) staff       (20)    18109 2014-08-08 20:42:32.000000 localcider-0.1.9.post3/LICENSE.txt
-drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider/
--rwxr-xr-x   0 alex       (501) staff       (20)     4036 2016-08-20 17:13:15.000000 localcider-0.1.9.post3/localcider/__init__.py
-drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider/backend/
--rw-r--r--   0 alex       (501) staff       (20)     3522 2016-08-20 17:15:30.000000 localcider-0.1.9.post3/localcider/backend/__init__.py
--rw-r--r--   0 alex       (501) staff       (20)     6089 2016-08-20 17:15:24.000000 localcider-0.1.9.post3/localcider/backend/backendtools.py
--rw-r--r--   0 alex       (501) staff       (20)     3449 2016-09-30 23:30:25.000000 localcider-0.1.9.post3/localcider/backend/config.py
-drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider/backend/data/
--rw-r--r--   0 alex       (501) staff       (20)     3282 2016-08-20 17:16:32.000000 localcider-0.1.9.post3/localcider/backend/data/__init__.py
--rw-r--r--   0 alex       (501) staff       (20)    12390 2016-08-20 17:16:23.000000 localcider-0.1.9.post3/localcider/backend/data/aminoacids.py
--rw-r--r--   0 alex       (501) staff       (20)     6747 2016-08-20 17:16:18.000000 localcider-0.1.9.post3/localcider/backend/data/buildHighComplexitySequences.py
--rw-r--r--   0 alex       (501) staff       (20)    15361 2016-08-20 17:16:11.000000 localcider-0.1.9.post3/localcider/backend/data/highComplexitySequences.py
--rw-r--r--   0 alex       (501) staff       (20)    15941 2016-08-20 17:15:05.000000 localcider-0.1.9.post3/localcider/backend/keyfile.py
--rw-r--r--   0 alex       (501) staff       (20)     4717 2016-08-20 17:14:58.000000 localcider-0.1.9.post3/localcider/backend/localciderExceptions.py
--rw-r--r--   0 alex       (501) staff       (20)    35403 2016-10-01 10:41:54.000000 localcider-0.1.9.post3/localcider/backend/plotting.py
--rw-r--r--   0 alex       (501) staff       (20)     3897 2016-08-20 17:14:41.000000 localcider-0.1.9.post3/localcider/backend/residue.py
--rw-r--r--   0 alex       (501) staff       (20)     5981 2016-08-20 17:14:35.000000 localcider-0.1.9.post3/localcider/backend/restable.py
--rw-r--r--   0 alex       (501) staff       (20)     7437 2016-08-20 17:14:27.000000 localcider-0.1.9.post3/localcider/backend/seqfileparser.py
--rw-r--r--   0 alex       (501) staff       (20)    61942 2016-10-06 15:15:54.000000 localcider-0.1.9.post3/localcider/backend/sequence.py
--rw-r--r--   0 alex       (501) staff       (20)    24348 2016-08-20 17:14:08.000000 localcider-0.1.9.post3/localcider/backend/sequenceComplexity.py
--rw-r--r--   0 alex       (501) staff       (20)    59134 2016-08-20 17:13:52.000000 localcider-0.1.9.post3/localcider/backend/wang_landau.py
--rw-r--r--   0 alex       (501) staff       (20)    24305 2016-08-20 17:13:04.000000 localcider-0.1.9.post3/localcider/plots.py
--rw-r--r--   0 alex       (501) staff       (20)    68915 2016-10-01 16:10:39.000000 localcider-0.1.9.post3/localcider/sequenceParameters.py
--rw-r--r--   0 alex       (501) staff       (20)     4934 2016-08-20 17:12:54.000000 localcider-0.1.9.post3/localcider/sequencePermutants.py
-drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider/tests/
--rw-r--r--   0 alex       (501) staff       (20)     3502 2016-09-30 23:18:03.000000 localcider-0.1.9.post3/localcider/tests/__init__.py
--rw-r--r--   0 alex       (501) staff       (20)     4552 2016-09-30 23:17:51.000000 localcider-0.1.9.post3/localcider/tests/runtests.py
--rw-r--r--   0 alex       (501) staff       (20)     4769 2016-09-30 23:17:44.000000 localcider-0.1.9.post3/localcider/tests/runtests_py3.py
--rw-r--r--   0 alex       (501) staff       (20)    10743 2016-09-30 23:17:28.000000 localcider-0.1.9.post3/localcider/tests/test_complexity.py
--rw-r--r--   0 alex       (501) staff       (20)    18739 2016-09-30 23:21:26.000000 localcider-0.1.9.post3/localcider/tests/test_plots.py
--rw-r--r--   0 alex       (501) staff       (20)     6220 2016-09-30 23:17:11.000000 localcider-0.1.9.post3/localcider/tests/test_sequence.py
--rw-r--r--   0 alex       (501) staff       (20)    28772 2016-09-30 23:17:00.000000 localcider-0.1.9.post3/localcider/tests/test_sequenceParameters.py
--rw-r--r--   0 alex       (501) staff       (20)     3807 2016-09-30 23:17:35.000000 localcider-0.1.9.post3/localcider/tests/testTools.py
-drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider.egg-info/
--rw-r--r--   0 alex       (501) staff       (20)        1 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider.egg-info/dependency_links.txt
--rw-r--r--   0 alex       (501) staff       (20)     3791 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider.egg-info/PKG-INFO
--rw-r--r--   0 alex       (501) staff       (20)       23 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider.egg-info/requires.txt
--rw-r--r--   0 alex       (501) staff       (20)     1171 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider.egg-info/SOURCES.txt
--rw-r--r--   0 alex       (501) staff       (20)       11 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/localcider.egg-info/top_level.txt
--rw-r--r--   0 alex       (501) staff       (20)     3791 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/PKG-INFO
--rw-r--r--   0 alex       (501) staff       (20)     3023 2016-10-11 23:52:02.000000 localcider-0.1.9.post3/README.txt
--rw-r--r--   0 alex       (501) staff       (20)       59 2016-10-11 23:57:07.000000 localcider-0.1.9.post3/setup.cfg
--rw-r--r--   0 alex       (501) staff       (20)      729 2016-10-11 23:50:51.000000 localcider-0.1.9.post3/setup.py
+drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/
+drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/docs/
+-rw-r--r--   0 alex       (501) staff       (20)       73 2014-08-11 18:19:14.000000 localcider-0.1.9.post4/docs/doc.txt
+-rw-r--r--   0 alex       (501) staff       (20)    18109 2014-08-08 20:42:32.000000 localcider-0.1.9.post4/LICENSE.txt
+drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/localcider/
+-rwxr-xr-x   0 alex       (501) staff       (20)     4036 2016-08-20 17:13:15.000000 localcider-0.1.9.post4/localcider/__init__.py
+drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/localcider/backend/
+-rw-r--r--   0 alex       (501) staff       (20)     3522 2016-08-20 17:15:30.000000 localcider-0.1.9.post4/localcider/backend/__init__.py
+-rw-r--r--   0 alex       (501) staff       (20)     6089 2016-08-20 17:15:24.000000 localcider-0.1.9.post4/localcider/backend/backendtools.py
+-rw-r--r--   0 alex       (501) staff       (20)     3449 2016-09-30 23:30:25.000000 localcider-0.1.9.post4/localcider/backend/config.py
+drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/localcider/backend/data/
+-rw-r--r--   0 alex       (501) staff       (20)     3282 2016-08-20 17:16:32.000000 localcider-0.1.9.post4/localcider/backend/data/__init__.py
+-rw-r--r--   0 alex       (501) staff       (20)    12390 2016-08-20 17:16:23.000000 localcider-0.1.9.post4/localcider/backend/data/aminoacids.py
+-rw-r--r--   0 alex       (501) staff       (20)     6747 2016-08-20 17:16:18.000000 localcider-0.1.9.post4/localcider/backend/data/buildHighComplexitySequences.py
+-rw-r--r--   0 alex       (501) staff       (20)    15361 2016-08-20 17:16:11.000000 localcider-0.1.9.post4/localcider/backend/data/highComplexitySequences.py
+-rw-r--r--   0 alex       (501) staff       (20)    15941 2016-08-20 17:15:05.000000 localcider-0.1.9.post4/localcider/backend/keyfile.py
+-rw-r--r--   0 alex       (501) staff       (20)     4717 2016-08-20 17:14:58.000000 localcider-0.1.9.post4/localcider/backend/localciderExceptions.py
+-rw-r--r--   0 alex       (501) staff       (20)    35403 2016-10-01 10:41:54.000000 localcider-0.1.9.post4/localcider/backend/plotting.py
+-rw-r--r--   0 alex       (501) staff       (20)     3897 2016-08-20 17:14:41.000000 localcider-0.1.9.post4/localcider/backend/residue.py
+-rw-r--r--   0 alex       (501) staff       (20)     5981 2016-08-20 17:14:35.000000 localcider-0.1.9.post4/localcider/backend/restable.py
+-rw-r--r--   0 alex       (501) staff       (20)     7437 2016-08-20 17:14:27.000000 localcider-0.1.9.post4/localcider/backend/seqfileparser.py
+-rw-r--r--   0 alex       (501) staff       (20)    61942 2016-10-06 15:15:54.000000 localcider-0.1.9.post4/localcider/backend/sequence.py
+-rw-r--r--   0 alex       (501) staff       (20)    24348 2016-08-20 17:14:08.000000 localcider-0.1.9.post4/localcider/backend/sequenceComplexity.py
+-rw-r--r--   0 alex       (501) staff       (20)    59134 2016-08-20 17:13:52.000000 localcider-0.1.9.post4/localcider/backend/wang_landau.py
+-rw-r--r--   0 alex       (501) staff       (20)    24305 2016-08-20 17:13:04.000000 localcider-0.1.9.post4/localcider/plots.py
+-rw-r--r--   0 alex       (501) staff       (20)    68915 2016-10-01 16:10:39.000000 localcider-0.1.9.post4/localcider/sequenceParameters.py
+-rw-r--r--   0 alex       (501) staff       (20)     4934 2016-08-20 17:12:54.000000 localcider-0.1.9.post4/localcider/sequencePermutants.py
+drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/localcider/tests/
+-rw-r--r--   0 alex       (501) staff       (20)     3502 2016-09-30 23:18:03.000000 localcider-0.1.9.post4/localcider/tests/__init__.py
+-rw-r--r--   0 alex       (501) staff       (20)     4552 2016-09-30 23:17:51.000000 localcider-0.1.9.post4/localcider/tests/runtests.py
+-rw-r--r--   0 alex       (501) staff       (20)     4769 2016-09-30 23:17:44.000000 localcider-0.1.9.post4/localcider/tests/runtests_py3.py
+-rw-r--r--   0 alex       (501) staff       (20)    10743 2016-09-30 23:17:28.000000 localcider-0.1.9.post4/localcider/tests/test_complexity.py
+-rw-r--r--   0 alex       (501) staff       (20)    18739 2016-09-30 23:21:26.000000 localcider-0.1.9.post4/localcider/tests/test_plots.py
+-rw-r--r--   0 alex       (501) staff       (20)     6220 2016-09-30 23:17:11.000000 localcider-0.1.9.post4/localcider/tests/test_sequence.py
+-rw-r--r--   0 alex       (501) staff       (20)    28772 2016-09-30 23:17:00.000000 localcider-0.1.9.post4/localcider/tests/test_sequenceParameters.py
+-rw-r--r--   0 alex       (501) staff       (20)     3807 2016-09-30 23:17:35.000000 localcider-0.1.9.post4/localcider/tests/testTools.py
+drwxr-xr-x   0 alex       (501) staff       (20)        0 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/localcider.egg-info/
+-rw-r--r--   0 alex       (501) staff       (20)        1 2016-10-11 23:58:16.000000 localcider-0.1.9.post4/localcider.egg-info/dependency_links.txt
+-rw-r--r--   0 alex       (501) staff       (20)     3788 2016-10-11 23:58:16.000000 localcider-0.1.9.post4/localcider.egg-info/PKG-INFO
+-rw-r--r--   0 alex       (501) staff       (20)       23 2016-10-11 23:58:16.000000 localcider-0.1.9.post4/localcider.egg-info/requires.txt
+-rw-r--r--   0 alex       (501) staff       (20)     1171 2016-10-11 23:58:16.000000 localcider-0.1.9.post4/localcider.egg-info/SOURCES.txt
+-rw-r--r--   0 alex       (501) staff       (20)       11 2016-10-11 23:58:16.000000 localcider-0.1.9.post4/localcider.egg-info/top_level.txt
+-rw-r--r--   0 alex       (501) staff       (20)     3788 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/PKG-INFO
+-rw-r--r--   0 alex       (501) staff       (20)     3023 2016-10-11 23:52:02.000000 localcider-0.1.9.post4/README.txt
+-rw-r--r--   0 alex       (501) staff       (20)       59 2016-10-11 23:58:17.000000 localcider-0.1.9.post4/setup.cfg
+-rw-r--r--   0 alex       (501) staff       (20)      726 2016-10-11 23:58:07.000000 localcider-0.1.9.post4/setup.py
```

### Comparing `localcider-0.1.9.post3/LICENSE.txt` & `localcider-0.1.9.post4/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/__init__.py` & `localcider-0.1.9.post4/localcider/__init__.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/__init__.py` & `localcider-0.1.9.post4/localcider/backend/__init__.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/backendtools.py` & `localcider-0.1.9.post4/localcider/backend/backendtools.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/config.py` & `localcider-0.1.9.post4/localcider/backend/config.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/data/__init__.py` & `localcider-0.1.9.post4/localcider/backend/data/__init__.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/data/aminoacids.py` & `localcider-0.1.9.post4/localcider/backend/data/aminoacids.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/data/buildHighComplexitySequences.py` & `localcider-0.1.9.post4/localcider/backend/data/buildHighComplexitySequences.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/data/highComplexitySequences.py` & `localcider-0.1.9.post4/localcider/backend/data/highComplexitySequences.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/keyfile.py` & `localcider-0.1.9.post4/localcider/backend/keyfile.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/localciderExceptions.py` & `localcider-0.1.9.post4/localcider/backend/localciderExceptions.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/plotting.py` & `localcider-0.1.9.post4/localcider/backend/plotting.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/residue.py` & `localcider-0.1.9.post4/localcider/backend/residue.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/restable.py` & `localcider-0.1.9.post4/localcider/backend/restable.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/seqfileparser.py` & `localcider-0.1.9.post4/localcider/backend/seqfileparser.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/sequence.py` & `localcider-0.1.9.post4/localcider/backend/sequence.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/sequenceComplexity.py` & `localcider-0.1.9.post4/localcider/backend/sequenceComplexity.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/backend/wang_landau.py` & `localcider-0.1.9.post4/localcider/backend/wang_landau.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/plots.py` & `localcider-0.1.9.post4/localcider/plots.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/sequenceParameters.py` & `localcider-0.1.9.post4/localcider/sequenceParameters.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/sequencePermutants.py` & `localcider-0.1.9.post4/localcider/sequencePermutants.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/tests/__init__.py` & `localcider-0.1.9.post4/localcider/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/tests/runtests.py` & `localcider-0.1.9.post4/localcider/tests/runtests.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/tests/runtests_py3.py` & `localcider-0.1.9.post4/localcider/tests/runtests_py3.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/tests/test_complexity.py` & `localcider-0.1.9.post4/localcider/tests/test_complexity.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/tests/test_plots.py` & `localcider-0.1.9.post4/localcider/tests/test_plots.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/tests/test_sequence.py` & `localcider-0.1.9.post4/localcider/tests/test_sequence.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/tests/test_sequenceParameters.py` & `localcider-0.1.9.post4/localcider/tests/test_sequenceParameters.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider/tests/testTools.py` & `localcider-0.1.9.post4/localcider/tests/testTools.py`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/localcider.egg-info/PKG-INFO` & `localcider-0.1.9.post4/localcider.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 1.0
 Name: localcider
-Version: 0.1.9.post3
-Summary: Tools for calculating sequence properties of disordered proteins [from the Pappu Lab in at Washington University in St. Louis]
+Version: 0.1.9.post4
+Summary: Tools for calculating sequence properties of disordered proteins [from the Pappu Lab at Washington University in St. Louis]
 Home-page: http://pappulab.github.io/localCIDER/
 Author: Alex Holehouse
 Author-email: alex.holehouse@wustl.edu
 License: LICENSE.txt
 Description: ==========
         localCIDER
         ==========
```

### Comparing `localcider-0.1.9.post3/localcider.egg-info/SOURCES.txt` & `localcider-0.1.9.post4/localcider.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/PKG-INFO` & `localcider-0.1.9.post4/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 1.0
 Name: localcider
-Version: 0.1.9.post3
-Summary: Tools for calculating sequence properties of disordered proteins [from the Pappu Lab in at Washington University in St. Louis]
+Version: 0.1.9.post4
+Summary: Tools for calculating sequence properties of disordered proteins [from the Pappu Lab at Washington University in St. Louis]
 Home-page: http://pappulab.github.io/localCIDER/
 Author: Alex Holehouse
 Author-email: alex.holehouse@wustl.edu
 License: LICENSE.txt
 Description: ==========
         localCIDER
         ==========
```

### Comparing `localcider-0.1.9.post3/README.txt` & `localcider-0.1.9.post4/README.txt`

 * *Files identical despite different names*

### Comparing `localcider-0.1.9.post3/setup.py` & `localcider-0.1.9.post4/setup.py`

 * *Files 15% similar despite different names*

```diff
@@ -5,20 +5,20 @@
 if sys.version_info >= (3, 0):
     extras.update(
             use_2to3=True,
     )
 
 setup(
     name='localcider',
-    version='0.1.9.post3',
+    version='0.1.9.post4',
     author='Alex Holehouse',
     author_email='alex.holehouse@wustl.edu',
     packages=['localcider', 'localcider.tests', 'localcider.backend', 'localcider.backend.data'],
     scripts=[],
     url='http://pappulab.github.io/localCIDER/',
     license='LICENSE.txt',
-    description='Tools for calculating sequence properties of disordered proteins [from the Pappu Lab in at Washington University in St. Louis]',
+    description='Tools for calculating sequence properties of disordered proteins [from the Pappu Lab at Washington University in St. Louis]',
     long_description=open('README.txt').read(),
     install_requires=[
         "numpy","matplotlib","scipy"],
     **extras
 )
```

