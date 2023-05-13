# Comparing `tmp/jms-metabolite-services-0.5.6.tar.gz` & `tmp/jms-metabolite-services-0.5.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/Users/shuzhao/li.github/JMS/dist/.tmp-bo5q0smb/jms-metabolite-services-0.5.6.tar", last modified: Tue Apr 11 00:21:39 2023, max compression
+gzip compressed data, was "/Users/shuzhao/li.github/JMS/dist/.tmp-3nackh_x/jms-metabolite-services-0.5.7.tar", last modified: Sat May 13 20:48:43 2023, max compression
```

## Comparing `jms-metabolite-services-0.5.6.tar` & `jms-metabolite-services-0.5.7.tar`

### file list

```diff
@@ -1,39 +1,39 @@
-drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/
--rw-r--r--   0 shuzhao    (501) staff       (20)     1073 2020-05-11 14:03:57.000000 jms-metabolite-services-0.5.6/LICENSE
--rw-r--r--   0 shuzhao    (501) staff       (20)     5597 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/PKG-INFO
--rw-r--r--   0 shuzhao    (501) staff       (20)     4720 2023-01-09 23:02:36.000000 jms-metabolite-services-0.5.6/README.md
-drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms/
--rw-r--r--   0 shuzhao    (501) staff       (20)       22 2023-04-11 00:19:46.000000 jms-metabolite-services-0.5.6/jms/__init__.py
--rw-r--r--   0 shuzhao    (501) staff       (20)     4443 2023-04-11 00:19:46.000000 jms-metabolite-services-0.5.6/jms/coverage.py
-drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms/data/
--rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 02:27:53.000000 jms-metabolite-services-0.5.6/jms/data/__init__.py
--rw-r--r--   0 shuzhao    (501) staff       (20)   749330 2023-04-11 00:03:32.000000 jms-metabolite-services-0.5.6/jms/data/humangem_pathways.py
--rw-r--r--   0 shuzhao    (501) staff       (20)  3085036 2022-02-23 20:21:57.000000 jms-metabolite-services-0.5.6/jms/data/list_formula_mass.py
--rw-r--r--   0 shuzhao    (501) staff       (20)       84 2022-02-10 00:56:47.000000 jms-metabolite-services-0.5.6/jms/data/masters.py
--rw-r--r--   0 shuzhao    (501) staff       (20) 20170544 2023-04-11 00:13:02.000000 jms-metabolite-services-0.5.6/jms/data/smpdb_pathways.py
--rw-r--r--   0 shuzhao    (501) staff       (20)    37884 2023-04-09 02:06:42.000000 jms-metabolite-services-0.5.6/jms/dbStructures.py
--rw-r--r--   0 shuzhao    (501) staff       (20)     4898 2023-04-10 13:43:20.000000 jms-metabolite-services-0.5.6/jms/empiricalCpds.py
--rw-r--r--   0 shuzhao    (501) staff       (20)     2229 2023-04-10 18:43:40.000000 jms-metabolite-services-0.5.6/jms/formula.py
--rw-r--r--   0 shuzhao    (501) staff       (20)     4605 2023-04-06 21:06:32.000000 jms-metabolite-services-0.5.6/jms/io.py
--rw-r--r--   0 shuzhao    (501) staff       (20)     1801 2023-03-08 18:14:43.000000 jms-metabolite-services-0.5.6/jms/ions.py
--rw-r--r--   0 shuzhao    (501) staff       (20)    14660 2023-04-10 19:30:36.000000 jms-metabolite-services-0.5.6/jms/modelConvert.py
--rw-r--r--   0 shuzhao    (501) staff       (20)      461 2023-04-06 15:29:23.000000 jms-metabolite-services-0.5.6/jms/model_port.py
--rw-r--r--   0 shuzhao    (501) staff       (20)    11998 2023-03-08 17:59:27.000000 jms-metabolite-services-0.5.6/jms/search.py
--rw-r--r--   0 shuzhao    (501) staff       (20)      649 2023-01-01 22:01:32.000000 jms-metabolite-services-0.5.6/jms/test.py
--rw-r--r--   0 shuzhao    (501) staff       (20)       58 2022-02-10 00:39:06.000000 jms-metabolite-services-0.5.6/jms/updates.py
-drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms/utils/
--rw-r--r--   0 shuzhao    (501) staff       (20)     5832 2022-05-19 20:33:17.000000 jms-metabolite-services-0.5.6/jms/utils/Tabular2Json.py
--rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 02:28:13.000000 jms-metabolite-services-0.5.6/jms/utils/__init__.py
--rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 00:48:16.000000 jms-metabolite-services-0.5.6/jms/utils/chemebi.py
--rw-r--r--   0 shuzhao    (501) staff       (20)    10125 2023-04-06 15:29:23.000000 jms-metabolite-services-0.5.6/jms/utils/gems.py
--rw-r--r--   0 shuzhao    (501) staff       (20)    11707 2022-02-10 02:05:11.000000 jms-metabolite-services-0.5.6/jms/utils/hmdb.py
--rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 00:48:21.000000 jms-metabolite-services-0.5.6/jms/utils/pubchem.py
--rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 00:48:26.000000 jms-metabolite-services-0.5.6/jms/utils/refmet.py
-drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms_metabolite_services.egg-info/
--rw-r--r--   0 shuzhao    (501) staff       (20)     5597 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms_metabolite_services.egg-info/PKG-INFO
--rw-r--r--   0 shuzhao    (501) staff       (20)      723 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms_metabolite_services.egg-info/SOURCES.txt
--rw-r--r--   0 shuzhao    (501) staff       (20)        1 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms_metabolite_services.egg-info/dependency_links.txt
--rw-r--r--   0 shuzhao    (501) staff       (20)       10 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms_metabolite_services.egg-info/requires.txt
--rw-r--r--   0 shuzhao    (501) staff       (20)        4 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/jms_metabolite_services.egg-info/top_level.txt
--rw-r--r--   0 shuzhao    (501) staff       (20)       38 2023-04-11 00:21:39.000000 jms-metabolite-services-0.5.6/setup.cfg
--rw-r--r--   0 shuzhao    (501) staff       (20)     1300 2022-05-19 20:56:08.000000 jms-metabolite-services-0.5.6/setup.py
+drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/
+-rw-r--r--   0 shuzhao    (501) staff       (20)     1073 2020-05-11 14:03:57.000000 jms-metabolite-services-0.5.7/LICENSE
+-rw-r--r--   0 shuzhao    (501) staff       (20)     5597 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/PKG-INFO
+-rw-r--r--   0 shuzhao    (501) staff       (20)     4720 2023-01-09 23:02:36.000000 jms-metabolite-services-0.5.7/README.md
+drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms/
+-rw-r--r--   0 shuzhao    (501) staff       (20)       22 2023-05-13 20:46:32.000000 jms-metabolite-services-0.5.7/jms/__init__.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     4443 2023-04-11 00:19:46.000000 jms-metabolite-services-0.5.7/jms/coverage.py
+drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms/data/
+-rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 02:27:53.000000 jms-metabolite-services-0.5.7/jms/data/__init__.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)   749330 2023-04-11 00:03:32.000000 jms-metabolite-services-0.5.7/jms/data/humangem_pathways.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)  3085036 2022-02-23 20:21:57.000000 jms-metabolite-services-0.5.7/jms/data/list_formula_mass.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)       84 2022-02-10 00:56:47.000000 jms-metabolite-services-0.5.7/jms/data/masters.py
+-rw-r--r--   0 shuzhao    (501) staff       (20) 20170544 2023-04-11 00:13:02.000000 jms-metabolite-services-0.5.7/jms/data/smpdb_pathways.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)    38468 2023-05-13 20:47:33.000000 jms-metabolite-services-0.5.7/jms/dbStructures.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     4898 2023-04-10 13:43:20.000000 jms-metabolite-services-0.5.7/jms/empiricalCpds.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     2229 2023-04-10 18:43:40.000000 jms-metabolite-services-0.5.7/jms/formula.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     4788 2023-05-13 20:35:55.000000 jms-metabolite-services-0.5.7/jms/io.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     1801 2023-03-08 18:14:43.000000 jms-metabolite-services-0.5.7/jms/ions.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)    14660 2023-04-10 19:30:36.000000 jms-metabolite-services-0.5.7/jms/modelConvert.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)      461 2023-04-06 15:29:23.000000 jms-metabolite-services-0.5.7/jms/model_port.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)    11998 2023-03-08 17:59:27.000000 jms-metabolite-services-0.5.7/jms/search.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)      649 2023-01-01 22:01:32.000000 jms-metabolite-services-0.5.7/jms/test.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)       58 2022-02-10 00:39:06.000000 jms-metabolite-services-0.5.7/jms/updates.py
+drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms/utils/
+-rw-r--r--   0 shuzhao    (501) staff       (20)     5832 2022-05-19 20:33:17.000000 jms-metabolite-services-0.5.7/jms/utils/Tabular2Json.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 02:28:13.000000 jms-metabolite-services-0.5.7/jms/utils/__init__.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 00:48:16.000000 jms-metabolite-services-0.5.7/jms/utils/chemebi.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)    10125 2023-04-06 15:29:23.000000 jms-metabolite-services-0.5.7/jms/utils/gems.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)    11707 2022-02-10 02:05:11.000000 jms-metabolite-services-0.5.7/jms/utils/hmdb.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 00:48:21.000000 jms-metabolite-services-0.5.7/jms/utils/pubchem.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)        0 2022-02-10 00:48:26.000000 jms-metabolite-services-0.5.7/jms/utils/refmet.py
+drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms_metabolite_services.egg-info/
+-rw-r--r--   0 shuzhao    (501) staff       (20)     5597 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms_metabolite_services.egg-info/PKG-INFO
+-rw-r--r--   0 shuzhao    (501) staff       (20)      723 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms_metabolite_services.egg-info/SOURCES.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)        1 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms_metabolite_services.egg-info/dependency_links.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)       10 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms_metabolite_services.egg-info/requires.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)        4 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/jms_metabolite_services.egg-info/top_level.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)       38 2023-05-13 20:48:43.000000 jms-metabolite-services-0.5.7/setup.cfg
+-rw-r--r--   0 shuzhao    (501) staff       (20)     1300 2022-05-19 20:56:08.000000 jms-metabolite-services-0.5.7/setup.py
```

### Comparing `jms-metabolite-services-0.5.6/LICENSE` & `jms-metabolite-services-0.5.7/LICENSE`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/PKG-INFO` & `jms-metabolite-services-0.5.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jms-metabolite-services
-Version: 0.5.6
+Version: 0.5.7
 Summary: conversion, search of metabolic models and metabolomics data
 Home-page: https://github.com/shuzhao-li/JMS
 Author: Shuzhao Li, Minghao Gong
 Author-email: shuzhao.li@gmail.com
 License: Python
 Keywords: metabolomics,chemistry,bioinformatics,mass spectrometry
 Classifier: Development Status :: 4 - Beta
```

### Comparing `jms-metabolite-services-0.5.6/README.md` & `jms-metabolite-services-0.5.7/README.md`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/coverage.py` & `jms-metabolite-services-0.5.7/jms/coverage.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/data/humangem_pathways.py` & `jms-metabolite-services-0.5.7/jms/data/humangem_pathways.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/data/list_formula_mass.py` & `jms-metabolite-services-0.5.7/jms/data/list_formula_mass.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/data/smpdb_pathways.py` & `jms-metabolite-services-0.5.7/jms/data/smpdb_pathways.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/dbStructures.py` & `jms-metabolite-services-0.5.7/jms/dbStructures.py`

 * *Files 4% similar despite different names*

```diff
@@ -324,24 +324,38 @@
         '''
         self.adduct_patterns = adduct_search_patterns
         if self.mode == 'neg':
             self.adduct_patterns = adduct_search_patterns_neg
         self.isotope_search_patterns = isotope_search_patterns
         self.extended_adducts = extended_adducts
 
-    def build_from_list_peaks(self, list_peaks):
+    def build_from_list_peaks(self, 
+                              list_peaks, 
+                              charges=[1, 2, 3],
+                              has_parent_masstrack=True,
+                              ):
         '''
         Wrapper of khipu epdsConstructor, to construct empirical compounds (empCpds).
         Updates self.dict_empCpds and does self.index_empCpds().
 
         list_peaks : [{'parent_masstrace_id': 1670, 'mz': 133.09702315984987, 'rtime': 654, 
                 'height': 14388.0, 'id_number': 555}, ...]
         isotope/adduct patterns, mz_tolerance_ppm and rt_tolerance are from self,
         as they are parameters to this class.
 
+        charges : multiple charged ions to consider.
+        has_parent_masstrack : True if from asari. 
+            Used to determine the need of setting parent_masstrack.
+
+        Updates
+        -------
+        self.list_peaks
+        self.dict_empCpds
+        self.indexed_peaks, self.formula_tree, self.indexed_empCpds
+
         Future updates can include enforcing overlap in scans not just rtime tolerance.
         '''
         # check if intensity value is provided
         if 'representative_intensity' not in list_peaks[0]:
             if 'peak_area' in list_peaks[0]:
                 for p in list_peaks:
                     p['representative_intensity'] = p['peak_area']
@@ -357,14 +371,16 @@
         ECCON = epdsConstructor(list_peaks, mode=self.mode)
         self.dict_empCpds = ECCON.peaks_to_epdDict(
                         self.isotope_search_patterns,
                         self.adduct_patterns,
                         self.extended_adducts,
                         self.mz_tolerance_ppm,
                         self.rt_tolerance,
+                        charges,
+                        has_parent_masstrack,
         ) 
         self.index_empCpds()
 
     def build_from_list_empCpds(self, list_empCpds):
         for E in list_empCpds:
             self.dict_empCpds[E['interim_id']] = E
         self.index_empCpds()
@@ -623,23 +639,23 @@
             for jj in range(1, len(PP)):
                 _P = self.dict_peaks[PP[jj][0]]
                 if is_coeluted(tmp[-1], _P, rt_tolerance=self.rt_tolerance):
                     tmp.append(_P)
                 else:
                     # not coeluted, new empCpd
                     new_id_start += 1
-                    self.dict_empCpds[new_id_start] = {'interim_id': new_id_start,
+                    self.dict_empCpds[new_id_start] = {'interim_id': str(new_id_start),
                             'neutral_formula_mass': neutral_formula_mass, 'neutral_formula': formula,
                             'MS1_pseudo_Spectra': self.__extend_peakList__(
                                 formula, neutral_formula_mass, tmp, peakTree, self.mz_tolerance_ppm),
                     }
                     tmp = [_P, ]
 
             new_id_start += 1
-            self.dict_empCpds[new_id_start] = {'interim_id': new_id_start,
+            self.dict_empCpds[new_id_start] = {'interim_id': str(new_id_start),
                     'neutral_formula_mass': neutral_formula_mass, 'neutral_formula': formula,
                     'MS1_pseudo_Spectra': self.__extend_peakList__(
                                 formula, neutral_formula_mass, tmp, peakTree, self.mz_tolerance_ppm),
             }
 
 
     def __extend_peakList__(self, neutral_formula, neutral_formula_mass, epd_peaks, peakTree,
```

### Comparing `jms-metabolite-services-0.5.6/jms/empiricalCpds.py` & `jms-metabolite-services-0.5.7/jms/empiricalCpds.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/formula.py` & `jms-metabolite-services-0.5.7/jms/formula.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/io.py` & `jms-metabolite-services-0.5.7/jms/io.py`

 * *Files 13% similar despite different names*

```diff
@@ -29,16 +29,16 @@
     'm/z': 'mz',
     'mz': 'mz',
     'apex': 'rtime',
     # ...,
 }
 
 def read_table_to_peaks(infile, 
-                        has_header=True, mz_col=1, rtime_col=2, feature_id=None,
-                        full_extract=False,
+                        has_header=True, mz_col=1, rtime_col=2, intensity=(11,21), feature_id=None,
+                        full_extract=True, max_col=21,
                         delimiter='\t'):
     '''
     Read a text feature table, and 
     return list of peaks, e.g. [ {
         'id_number': 555,
         'mz': 133.0970, 
         'apex': 654, 
@@ -50,39 +50,38 @@
     '''
     def _make_id(ii, mz, rt):
         return 'F' + str(ii) + '_' + str(round(mz, 6)) + '@' + str(round(rt, 2))
 
     list_peaks = []
     w = open(infile).readlines()
     if has_header:
-        header = w[0].rstrip().split(delimiter)
+        header = w[0].rstrip().split(delimiter)[:max_col]
         w = w[1:]
     ii = 0
     for line in w:
-        a = line.split(delimiter)   # not rstrip, so trailing EOL will be carried forward
+        a = line.split(delimiter)[:max_col]   # not rstrip, so trailing EOL will be carried forward
         mz, rt = float(a[mz_col]), float(a[rtime_col])
+        intensities = [float(x) for x in a[intensity[0]: intensity[1]]]
         if feature_id != None:
             fid = a[feature_id].strip()
         else:
             ii += 1
             fid = _make_id(ii, mz, rt)
-        peak = {'id_number': fid, 'mz': mz, 'rtime': rt, 'apex': rt}
+        peak = {'id_number': fid, 'mz': mz, 'rtime': rt, 'apex': rt, 'representative_intensity': sum(intensities) / len(intensities)}
         if has_header and full_extract:
             # will remove redundant fields
             peak2 = dict(zip(header, a))
             peak2.update(peak)
             peak = peak2
 
         list_peaks.append( peak )
 
     return list_peaks
 
 
-# 
-
 def read_tsv_hmdb_to_empCpds(infile, delimiter='\t'):
     '''
     Previously parsed HMDB4 in short tsv format.
     Ref:
     https://github.com/shuzhao-li/JMS/wiki/Scripting-to-create-a-dictionary-from-HMDB-data
     https://github.com/shuzhao-li/JMS/blob/main/jms/utils/hmdb.py
     A copy of HMDB4_compounds.tsv is under
```

### Comparing `jms-metabolite-services-0.5.6/jms/ions.py` & `jms-metabolite-services-0.5.7/jms/ions.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/modelConvert.py` & `jms-metabolite-services-0.5.7/jms/modelConvert.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/search.py` & `jms-metabolite-services-0.5.7/jms/search.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/test.py` & `jms-metabolite-services-0.5.7/jms/test.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/utils/Tabular2Json.py` & `jms-metabolite-services-0.5.7/jms/utils/Tabular2Json.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/utils/gems.py` & `jms-metabolite-services-0.5.7/jms/utils/gems.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms/utils/hmdb.py` & `jms-metabolite-services-0.5.7/jms/utils/hmdb.py`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/jms_metabolite_services.egg-info/PKG-INFO` & `jms-metabolite-services-0.5.7/jms_metabolite_services.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jms-metabolite-services
-Version: 0.5.6
+Version: 0.5.7
 Summary: conversion, search of metabolic models and metabolomics data
 Home-page: https://github.com/shuzhao-li/JMS
 Author: Shuzhao Li, Minghao Gong
 Author-email: shuzhao.li@gmail.com
 License: Python
 Keywords: metabolomics,chemistry,bioinformatics,mass spectrometry
 Classifier: Development Status :: 4 - Beta
```

### Comparing `jms-metabolite-services-0.5.6/jms_metabolite_services.egg-info/SOURCES.txt` & `jms-metabolite-services-0.5.7/jms_metabolite_services.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `jms-metabolite-services-0.5.6/setup.py` & `jms-metabolite-services-0.5.7/setup.py`

 * *Files identical despite different names*

