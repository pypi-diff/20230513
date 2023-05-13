# Comparing `tmp/pandasgwas-0.99.9.tar.gz` & `tmp/pandasgwas-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\pandasgwas-0.99.9.tar", last modified: Tue Jul 19 13:44:10 2022, max compression
+gzip compressed data, was "pandasgwas-1.0.0.tar", last modified: Sat May 13 06:25:03 2023, max compression
```

## Comparing `pandasgwas-0.99.9.tar` & `pandasgwas-1.0.0.tar`

### file list

```diff
@@ -1,27 +1,30 @@
-drwxrwxrwx   0        0        0        0 2022-07-19 13:44:10.912633 pandasgwas-0.99.9/
--rw-rw-rw-   0        0        0     1118 2022-06-28 05:00:31.000000 pandasgwas-0.99.9/LICENSE
--rw-rw-rw-   0        0        0     4281 2022-07-19 13:44:10.912633 pandasgwas-0.99.9/PKG-INFO
--rw-rw-rw-   0        0        0     3580 2022-07-19 13:34:05.000000 pandasgwas-0.99.9/README.md
-drwxrwxrwx   0        0        0        0 2022-07-19 13:44:10.865762 pandasgwas-0.99.9/pandasgwas/
--rw-rw-rw-   0        0        0     8634 2022-06-22 01:52:14.000000 pandasgwas-0.99.9/pandasgwas/Association.py
--rw-rw-rw-   0        0        0     1362 2022-06-05 12:18:01.000000 pandasgwas-0.99.9/pandasgwas/Browser.py
--rw-rw-rw-   0        0        0     6538 2022-06-21 08:07:17.000000 pandasgwas-0.99.9/pandasgwas/SingleNucleotidePolymorphism.py
--rw-rw-rw-   0        0        0     7950 2022-06-21 08:07:16.000000 pandasgwas-0.99.9/pandasgwas/Study.py
--rw-rw-rw-   0        0        0     3833 2022-06-21 08:05:22.000000 pandasgwas-0.99.9/pandasgwas/Trait.py
--rw-rw-rw-   0        0        0      228 2022-06-22 01:52:14.000000 pandasgwas-0.99.9/pandasgwas/__init__.py
--rw-rw-rw-   0        0        0     8427 2022-06-05 12:18:01.000000 pandasgwas-0.99.9/pandasgwas/client.py
--rw-rw-rw-   0        0        0    78270 2022-06-06 13:16:18.000000 pandasgwas-0.99.9/pandasgwas/cytogenetic_bands.csv
--rw-rw-rw-   0        0        0     8267 2022-06-30 00:45:07.000000 pandasgwas-0.99.9/pandasgwas/get_SNPs.py
--rw-rw-rw-   0        0        0     4871 2022-06-05 12:18:01.000000 pandasgwas-0.99.9/pandasgwas/get_associations.py
--rw-rw-rw-   0        0        0     6828 2022-06-30 01:58:25.000000 pandasgwas-0.99.9/pandasgwas/get_studies.py
--rw-rw-rw-   0        0        0     4369 2022-06-05 12:18:01.000000 pandasgwas-0.99.9/pandasgwas/get_traits.py
--rw-rw-rw-   0        0        0     1695 2022-06-21 07:58:27.000000 pandasgwas-0.99.9/pandasgwas/set_operation.py
-drwxrwxrwx   0        0        0        0 2022-07-19 13:44:10.912633 pandasgwas-0.99.9/pandasgwas.egg-info/
--rw-rw-rw-   0        0        0     4281 2022-07-19 13:44:09.000000 pandasgwas-0.99.9/pandasgwas.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      551 2022-07-19 13:44:10.000000 pandasgwas-0.99.9/pandasgwas.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-07-19 13:44:09.000000 pandasgwas-0.99.9/pandasgwas.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       59 2022-07-19 13:44:09.000000 pandasgwas-0.99.9/pandasgwas.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2022-07-19 13:44:09.000000 pandasgwas-0.99.9/pandasgwas.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       86 2022-06-07 12:29:56.000000 pandasgwas-0.99.9/pyproject.toml
--rw-rw-rw-   0        0        0       42 2022-07-19 13:44:10.912633 pandasgwas-0.99.9/setup.cfg
--rw-rw-rw-   0        0        0     1162 2022-07-19 13:31:55.000000 pandasgwas-0.99.9/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:25:03.575496 pandasgwas-1.0.0/
+-rw-rw-rw-   0        0        0     1118 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/LICENSE
+-rw-rw-rw-   0        0        0     6564 2023-05-13 06:25:03.575496 pandasgwas-1.0.0/PKG-INFO
+-rw-rw-rw-   0        0        0     5851 2023-05-13 06:22:54.000000 pandasgwas-1.0.0/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 06:25:03.513002 pandasgwas-1.0.0/pandasgwas/
+-rw-rw-rw-   0        0        0     8596 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/Association.py
+-rw-rw-rw-   0        0        0     1362 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/Browser.py
+-rw-rw-rw-   0        0        0     8198 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/Study.py
+-rw-rw-rw-   0        0        0     3795 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/Trait.py
+-rw-rw-rw-   0        0        0     6284 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/Variant.py
+-rw-rw-rw-   0        0        0     1862 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/__init__.py
+-rw-rw-rw-   0        0        0    10818 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/client.py
+-rw-rw-rw-   0        0        0    78270 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/cytogenetic_bands.csv
+-rw-rw-rw-   0        0        0     4871 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/get_associations.py
+-rw-rw-rw-   0        0        0     6828 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/get_studies.py
+-rw-rw-rw-   0        0        0     4369 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/get_traits.py
+-rw-rw-rw-   0        0        0     7700 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/get_variants.py
+-rw-rw-rw-   0        0        0  2771641 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/harmonised_list.txt
+-rw-rw-rw-   0        0        0     1296 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/set_operation.py
+-rw-rw-rw-   0        0        0     5348 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/summary_statistics.py
+-rw-rw-rw-   0        0        0      826 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pandasgwas/utility.py
+drwxrwxrwx   0        0        0        0 2023-05-13 06:25:03.575496 pandasgwas-1.0.0/pandasgwas.egg-info/
+-rw-rw-rw-   0        0        0     6564 2023-05-13 06:25:02.000000 pandasgwas-1.0.0/pandasgwas.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      620 2023-05-13 06:25:03.000000 pandasgwas-1.0.0/pandasgwas.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 06:25:02.000000 pandasgwas-1.0.0/pandasgwas.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       51 2023-05-13 06:25:02.000000 pandasgwas-1.0.0/pandasgwas.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 06:25:02.000000 pandasgwas-1.0.0/pandasgwas.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       86 2023-04-18 02:33:30.000000 pandasgwas-1.0.0/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 06:25:03.575496 pandasgwas-1.0.0/setup.cfg
+-rw-rw-rw-   0        0        0     1173 2023-05-13 06:15:24.000000 pandasgwas-1.0.0/setup.py
```

### Comparing `pandasgwas-0.99.9/LICENSE` & `pandasgwas-1.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pandasgwas-0.99.9/pandasgwas/Association.py` & `pandasgwas-1.0.0/pandasgwas/Association.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 from pandas import DataFrame, Series, json_normalize, set_option
 import numpy
 import warnings
 
-set_option('display.max_rows', None)
 set_option('display.max_columns', None)
 set_option('display.width', 1000)
 set_option('display.colheader_justify', 'center')
 set_option('display.precision', 3)
 
 
 class Association:
```

### Comparing `pandasgwas-0.99.9/pandasgwas/Browser.py` & `pandasgwas-1.0.0/pandasgwas/Browser.py`

 * *Files identical despite different names*

### Comparing `pandasgwas-0.99.9/pandasgwas/SingleNucleotidePolymorphism.py` & `pandasgwas-1.0.0/pandasgwas/Variant.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,41 +1,40 @@
 from pandas import DataFrame, Series, json_normalize, set_option
 import numpy
 import warnings
 
-set_option('display.max_rows', None)
 set_option('display.max_columns', None)
 set_option('display.width', 1000)
 set_option('display.colheader_justify', 'center')
 set_option('display.precision', 3)
 
 
-class SingleNucleotidePolymorphism:
+class Variant:
     def __init__(self, data: list = None):
         if data is None:
             data = []
         self.parse(data)
 
     def parse(self, data: list = None):
         if data is None:
             warnings.warn("Data is None, DataFrame will be empty")
         self.raw_data = data
         if data is None or len(data) == 0:
-            self.single_nucleotide_polymorphisms = DataFrame(
+            self.variants = DataFrame(
                 columns=['rsId', 'merged', 'functionalClass', 'lastUpdateDate', 'locations', 'genomicContexts'])
             self.locations = DataFrame(columns=['chromosomeName', 'chromosomePosition', 'region.name', 'rsId'])
             self.genomic_contexts = DataFrame(
                 columns=['isIntergenic', 'isUpstream', 'isDownstream', 'distance', 'source', 'mappingMethod',
                          'isClosestGene', 'gene.geneName', 'gene.entrezGeneIds', 'gene.ensemblGeneIds',
                          'location.chromosomeName', 'location.chromosomePosition', 'location.region.name', 'rsId',
                          'genomicContextId'])
             self.ensembl_gene_ids = DataFrame(columns=['rsId', 'genomicContextId', 'ensemblGeneId'])
             self.entrez_gene_ids = DataFrame(columns=['rsId', 'genomicContextId', 'entrezGeneId'])
             return
-        self.single_nucleotide_polymorphisms: DataFrame = json_normalize(data, max_level=2)
+        self.variants: DataFrame = json_normalize(data, max_level=2)
         self.locations: DataFrame = json_normalize(data, record_path=['locations'], meta=['rsId'])
         genomic_contexts = json_normalize(data, record_path=['genomicContexts'], meta=['rsId'])
         genomic_contexts['genomicContextId'] = Series(data=range(0, len(genomic_contexts)))
         self.genomic_contexts: DataFrame = genomic_contexts
         ensembl_gene_ids = genomic_contexts[['gene.ensemblGeneIds', 'rsId', 'genomicContextId']].copy()
         ensembl_gene_ids['gene.ensemblGeneIds'] = ensembl_gene_ids['gene.ensemblGeneIds'].apply(
             lambda x: x if len(x) > 0 else numpy.nan)
@@ -52,15 +51,15 @@
         entrez_gene_ids = entrez_gene_ids.explode('gene.entrezGeneIds')
         entrez_gene_ids['entrezGeneId'] = entrez_gene_ids['gene.entrezGeneIds'].apply(
             lambda x: x['entrezGeneId'])
         entrez_gene_ids = entrez_gene_ids.drop(columns=['gene.entrezGeneIds'])
         self.entrez_gene_ids: DataFrame = entrez_gene_ids.reset_index(drop=True)
 
     def __len__(self):
-        return len(self.single_nucleotide_polymorphisms)
+        return len(self.variants)
 
     def __getitem__(self, item):
         if isinstance(item, str) or isinstance(item, int):
             arr = [item]
         elif isinstance(item, list) or isinstance(item, tuple) or isinstance(item, range):
             arr = item
         elif isinstance(item, slice):
@@ -76,57 +75,57 @@
         for i in arr:
             if isinstance(i, str) :
                 sub_set.append(raw_data_dict[i])
             elif isinstance(i, int):
                 sub_set.append(raw_data[i])
             else:
                 raise TypeError('Invalid item type: {}'.format(type(i)))
-        return SingleNucleotidePolymorphism(sub_set)
+        return Variant(sub_set)
 
     def __add__(self, other):
-        return SingleNucleotidePolymorphism(self.raw_data + other.raw_data)
+        return Variant(self.raw_data + other.raw_data)
 
     def __sub__(self, other):
         self_key_set = set()
         self_dict = {}
         other_key_set = set()
         for i in self.raw_data:
             self_key_set.add(i['rsId'])
             self_dict[i['rsId']] = i
         for j in other.raw_data:
             other_key_set.add(j['rsId'])
         sub_key = self_key_set - other_key_set
         data = []
         for k in sub_key:
             data.append(self_dict[k])
-        return SingleNucleotidePolymorphism(data)
+        return Variant(data)
 
     def __and__(self, other):
         self_key_set = set()
         self_dict = {}
         other_key_set = set()
         for i in self.raw_data:
             self_key_set.add(i['rsId'])
             self_dict[i['rsId']] = i
         for j in other.raw_data:
             other_key_set.add(j['rsId'])
         sub_key = self_key_set & other_key_set
         data = []
         for k in sub_key:
             data.append(self_dict[k])
-        return SingleNucleotidePolymorphism(data)
+        return Variant(data)
 
     def __or__(self, other):
         and_dict = {}
         for i in self.raw_data:
             and_dict[i['rsId']] = i
         for j in other.raw_data:
             and_dict[j['rsId']] = j
         data = list(and_dict.values())
-        return SingleNucleotidePolymorphism(data)
+        return Variant(data)
 
     def __xor__(self, other):
         self_key_set = set()
         and_dict = {}
         other_key_set = set()
         for i in self.raw_data:
             self_key_set.add(i['rsId'])
@@ -134,13 +133,13 @@
         for j in other.raw_data:
             other_key_set.add(j['rsId'])
             and_dict[j['rsId']] = j
         sub_key = self_key_set ^ other_key_set
         data = []
         for k in sub_key:
             data.append(and_dict[k])
-        return SingleNucleotidePolymorphism(data)
+        return Variant(data)
 
     def __eq__(self, other):
         if self is None or other is None:
             return self is None and other is None
         return self.raw_data == other.raw_data
```

### Comparing `pandasgwas-0.99.9/pandasgwas/Study.py` & `pandasgwas-1.0.0/pandasgwas/Study.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 from pandas import DataFrame, Series, json_normalize, set_option
 import numpy
 import warnings
 
-set_option('display.max_rows', None)
 set_option('display.max_columns', None)
 set_option('display.width', 1000)
 set_option('display.colheader_justify', 'center')
 set_option('display.precision', 3)
 
 
 class Study:
@@ -54,25 +53,31 @@
         ancestral_groups = ancestral_groups.drop(columns=['ancestralGroups'])
         self.ancestral_groups: DataFrame = ancestral_groups.reset_index(drop=True)
         country_of_origin = ancestries[['countryOfOrigin', 'accessionId', 'ancestryId']].copy()
         country_of_origin['countryOfOrigin'] = country_of_origin['countryOfOrigin'].apply(
             lambda x: x if len(x) > 0 else numpy.nan)
         country_of_origin = country_of_origin.dropna()
         country_of_origin = country_of_origin.explode('countryOfOrigin')
-        country_of_origin[['majorArea', 'region', 'countryName']] = country_of_origin['countryOfOrigin'].apply(
-            lambda x: Series(data=[x['majorArea'], x['region'], x['countryName']]))
+        if len(country_of_origin)>0:
+            country_of_origin[['majorArea', 'region', 'countryName']] = country_of_origin['countryOfOrigin'].apply(
+                lambda x: Series(data=[x['majorArea'], x['region'], x['countryName']]))
+        else:
+            country_of_origin.assign(majorArea=[],region=[],countryName=[])
         country_of_origin = country_of_origin.drop(columns=['countryOfOrigin'])
         self.country_of_origin: DataFrame = country_of_origin.reset_index(drop=True)
         country_of_recruitment = ancestries[['countryOfRecruitment', 'accessionId', 'ancestryId']].copy()
         country_of_recruitment['countryOfRecruitment'] = country_of_recruitment['countryOfRecruitment'].apply(
             lambda x: x if len(x) > 0 else numpy.nan)
         country_of_recruitment = country_of_recruitment.dropna()
         country_of_recruitment = country_of_recruitment.explode('countryOfRecruitment')
-        country_of_recruitment[['majorArea', 'region', 'countryName']] = country_of_recruitment[
-            'countryOfRecruitment'].apply(lambda x: Series([x['majorArea'], x['region'], x['countryName']]))
+        if len(country_of_recruitment)>0:
+            country_of_recruitment[['majorArea', 'region', 'countryName']] = country_of_recruitment[
+                'countryOfRecruitment'].apply(lambda x: Series([x['majorArea'], x['region'], x['countryName']]))
+        else:
+            country_of_recruitment.assign(majorArea=[],region=[],countryName=[])
         country_of_recruitment = country_of_recruitment.drop(columns=['countryOfRecruitment'])
         self.country_of_recruitment: DataFrame = country_of_recruitment.reset_index(drop=True)
 
     def __len__(self):
         return len(self.studies)
 
     def __getitem__(self, item):
```

### Comparing `pandasgwas-0.99.9/pandasgwas/Trait.py` & `pandasgwas-1.0.0/pandasgwas/Trait.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 from pandas import DataFrame, json_normalize, set_option
 import warnings
 
-set_option('display.max_rows', None)
 set_option('display.max_columns', None)
 set_option('display.width', 1000)
 set_option('display.colheader_justify', 'center')
 set_option('display.precision', 3)
 
 
 class Trait:
```

### Comparing `pandasgwas-0.99.9/pandasgwas/client.py` & `pandasgwas-1.0.0/pandasgwas/client.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,151 +1,163 @@
+import functools
+
 import requests
 import json
 import progressbar
 from typing import List, Dict
 import re
 
 from requests.adapters import HTTPAdapter
 s = requests.Session()
 s.mount('https://', HTTPAdapter(max_retries=5))
 
 
+@functools.lru_cache(maxsize=None)
+def cache_get(url):
+    return s.get(url)
+
+
 def get_studies(url: str, interactive: bool = True) -> List[Dict]:
-    r = s.get(url)
+    r = cache_get(url)
     if r.status_code == 200:
         parsed_data = json.loads(r.text, object_hook=remove_links)
         if parsed_data.get('_embedded') is not None:
             study_list = parsed_data.get('_embedded').get("studies")
-            if parsed_data.get('page') is not None:
+            if parsed_data.get('page') is not None and parsed_data.get('page').get('totalPages') > 1:
                 if parsed_data.get('page').get('totalPages') > 100 and interactive:
                     answer = ask_yes_no_question(
                         "You are about to download to many data from the GWAS Catalog.\r\nThis might take several "
                         "minutes.\r\nDo you still want to proceed? (Yes or No)")
                     if answer == "NO":
                         return []
-                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages')-1)
+                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages')-1).start()
                 for i in range(1, parsed_data.get('page').get('totalPages')):
                     format_url = '%s?page=%d&size=20' % (url, i)
                     if '?' in url:
                         format_url = '%s&page=%d&size=20' % (url, i)
                     # print('http req:'+format_url)
+
                     bar.update(i)
-                    r = s.get(format_url)
+                    r = cache_get(format_url)
                     if r.status_code == 200:
                         study_list.extend(
                             json.loads(r.text, object_hook=remove_links).get('_embedded').get("studies"))
                     else:
                         raise Exception('The request for %s failed: response code was %d' % (url, r.status_code))
+                bar.finish()
             return study_list
         else:
             return [parsed_data]
     elif r.status_code == 404:
         return []
     else:
         print('The request for %s failed: response code was %d' % (url, r.status_code))
 
 
 def get_SNPs(url: str, interactive: bool = True) -> List[Dict]:
-    r = s.get(url)
+    r = cache_get(url)
     if r.status_code == 200:
         parsed_data = json.loads(r.text, object_hook=remove_links)
         if parsed_data.get('_embedded') is not None:
             variant_list = parsed_data.get('_embedded').get("singleNucleotidePolymorphisms")
-            if parsed_data.get('page') is not None:
+            if parsed_data.get('page') is not None and parsed_data.get('page').get('totalPages') > 1:
                 if parsed_data.get('page').get('totalPages') > 100 and interactive:
                     answer = ask_yes_no_question(
                         "You are about to download to many data from the GWAS Catalog.\r\nThis might take several "
                         "minutes.\r\nDo you still want to proceed? (Yes or No)")
                     if answer == "NO":
                         return []
-                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages')-1)
+                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages')-1).start()
                 for i in range(1, parsed_data.get('page').get('totalPages')):
                     format_url = '%s?page=%d&size=20' % (url, i)
                     if '?' in url:
                         format_url = '%s&page=%d&size=20' % (url, i)
                     # print('http req:'+format_url)
                     bar.update(i)
-                    r = s.get(format_url)
+                    r = cache_get(format_url)
                     if r.status_code == 200:
                         variant_list.extend(
                             json.loads(r.text, object_hook=remove_links).get('_embedded').get(
                                 "singleNucleotidePolymorphisms"))
                     else:
                         raise Exception('The request for %s failed: response code was %d' % (url, r.status_code))
+                bar.finish()
             return variant_list
         else:
             return [parsed_data]
     elif r.status_code == 404:
         return []
     else:
         print('The request for %s failed: response code was %d' % (url, r.status_code))
 
 
 def get_traits(url: str, interactive: bool = True) -> List[Dict]:
-    r = s.get(url)
+    r = cache_get(url)
     if r.status_code == 200:
         parsed_data = json.loads(r.text, object_hook=remove_links)
         if parsed_data.get('_embedded') is not None:
             trait_list = parsed_data.get('_embedded').get("efoTraits")
-            if parsed_data.get('page') is not None:
+            if parsed_data.get('page') is not None and parsed_data.get('page').get('totalPages') > 1:
                 if parsed_data.get('page').get('totalPages') > 100 and interactive:
                     answer = ask_yes_no_question(
                         "You are about to download to many data from the GWAS Catalog.\r\nThis might take several "
                         "minutes.\r\nDo you still want to proceed? (Yes or No)")
                     if answer == "NO":
                         return []
-                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages')-1)
+                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages')-1).start()
                 for i in range(1, parsed_data.get('page').get('totalPages')):
                     format_url = '%s?page=%d&size=20' % (url, i)
                     if '?' in url:
                         format_url = '%s&page=%d&size=20' % (url, i)
                     # print('http req:'+format_url)
                     bar.update(i)
-                    r = s.get(format_url)
+                    r = cache_get(format_url)
                     if r.status_code == 200:
                         trait_list.extend(
                             json.loads(r.text, object_hook=remove_links).get('_embedded').get("efoTraits"))
                     else:
                         raise Exception('The request for %s failed: response code was %d' % (url, r.status_code))
+                bar.finish()
             return trait_list
         else:
             return [parsed_data]
     elif r.status_code == 404:
         return []
     else:
         print('The request for %s failed: response code was %d' % (url, r.status_code))
 
 
 def get_associations(url: str, interactive: bool = True) -> List[Dict]:
-    r = s.get(url)
+    r = cache_get(url)
     if r.status_code == 200:
         parsed_data = json.loads(r.text, object_hook=remove_links_get_id)
         if parsed_data.get('_embedded') is not None:
             association_list = parsed_data.get('_embedded').get("associations")
-            if parsed_data.get('page') is not None:
+            if parsed_data.get('page') is not None and parsed_data.get('page').get('totalPages') > 1:
                 if parsed_data.get('page').get('totalPages') > 100 and interactive:
                     answer = ask_yes_no_question(
                         "You are about to download to many data from the GWAS Catalog.\r\nThis might take several "
                         "minutes.\r\nDo you still want to proceed? (Yes or No)")
                     if answer == "NO":
                         return []
-                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages')-1)
+                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages')-1).start()
                 for i in range(1, parsed_data.get('page').get('totalPages')):
                     format_url = '%s?page=%d&size=20' % (url, i)
                     if '?' in url:
                         format_url = '%s&page=%d&size=20' % (url, i)
                     # print('http req:'+format_url)
                     bar.update(i)
-                    r = s.get(format_url)
+                    r = cache_get(format_url)
                     if r.status_code == 200:
                         association_list.extend(
                             json.loads(r.text, object_hook=remove_links_get_id).get('_embedded').get(
                                 "associations"))
                     else:
                         raise Exception('The request for %s failed: response code was %d' % (url, r.status_code))
+                bar.finish()
             return association_list
         else:
             return [parsed_data]
     elif r.status_code == 404:
         return []
     else:
         print('The request for %s failed: response code was %d' % (url, r.status_code))
@@ -170,7 +182,44 @@
     temp = {}
     for a in d.keys():
         if a != '_links':
             temp[a] = d[a]
         elif 'self' in d['_links'] and not (re.match('.*associations/(.*)', d['_links']['self']['href']) is None):
             temp['associationId'] = re.match('.*associations/(.*)', d['_links']['self']['href']).group(1)
     return temp
+
+
+def get_child_efo(url: str, interactive: bool = True) -> List[Dict]:
+    r = cache_get(url)
+    if r.status_code == 200:
+        parsed_data = json.loads(r.text, object_hook=remove_links)
+        if parsed_data.get('_embedded') is not None:
+            terms = parsed_data.get('_embedded').get("terms")
+            if parsed_data.get('page') is not None and parsed_data.get('page').get('totalPages') > 1:
+                if parsed_data.get('page').get('totalPages') > 100 and interactive:
+                    answer = ask_yes_no_question(
+                        "You are about to download to many data from the GWAS Catalog.\r\nThis might take several "
+                        "minutes.\r\nDo you still want to proceed? (Yes or No)")
+                    if answer == "NO":
+                        return []
+                bar = progressbar.ProgressBar(max_value=parsed_data.get('page').get('totalPages') - 1).start()
+                for i in range(1, parsed_data.get('page').get('totalPages')):
+                    format_url = '%s?page=%d&size=20' % (url, i)
+                    if '?' in url:
+                        format_url = '%s&page=%d&size=20' % (url, i)
+                    # print('http req:'+format_url)
+
+                    bar.update(i)
+                    r = cache_get(format_url)
+                    if r.status_code == 200:
+                        terms.extend(
+                            json.loads(r.text, object_hook=remove_links).get('_embedded').get("terms"))
+                    else:
+                        raise Exception('The request for %s failed: response code was %d' % (url, r.status_code))
+                bar.finish()
+            return terms
+        else:
+            return []
+    elif r.status_code == 404:
+        return []
+    else:
+        print('The request for %s failed: response code was %d' % (url, r.status_code))
```

### Comparing `pandasgwas-0.99.9/pandasgwas/cytogenetic_bands.csv` & `pandasgwas-1.0.0/pandasgwas/cytogenetic_bands.csv`

 * *Files identical despite different names*

### Comparing `pandasgwas-0.99.9/pandasgwas/get_SNPs.py` & `pandasgwas-1.0.0/pandasgwas/get_variants.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,101 +1,101 @@
 from typing import List
 
-from pandasgwas.SingleNucleotidePolymorphism import SingleNucleotidePolymorphism
+from pandasgwas.Variant import Variant
 from pandasgwas import client
 from functools import reduce
 from pandas import read_csv
 import os
 
 
-def get_variants_by_study_id(study_id: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+def get_variants_by_study_id(study_id: str, interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs('https://www.ebi.ac.uk/gwas/rest/api/studies/%s/snps' % study_id, interactive=interactive))
 
 
-def get_variants_by_association_id(association_id: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+def get_variants_by_association_id(association_id: str, interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs('https://www.ebi.ac.uk/gwas/rest/api/associations/%s/snps' % association_id,
                         interactive=interactive))
 
 
-def get_variants_by_variant_id(variant_id: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+def get_variants_by_variant_id(variant_id: str, interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs('https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms/%s' % variant_id,
                         interactive=interactive))
 
 
-def get_variants_by_efo_id(efo_id: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
+def get_variants_by_efo_id(efo_id: str, interactive: bool = True) -> Variant:
     trait = client.get_traits('https://www.ebi.ac.uk/gwas/rest/api/efoTraits/%s' % efo_id)[0].get('trait')
     return get_variants_by_efo_trait(trait, interactive)
 
 
-def get_variants_by_pubmed_id(pubmed_id: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+def get_variants_by_pubmed_id(pubmed_id: str, interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs(
             'https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms/search/findByPubmedId?pubmedId=%s' % pubmed_id,
             interactive=interactive))
 
 
 def get_variants_by_genomic_range(chromosome: str, start: int, end: int,
-                                  interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+                                  interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs(
             'https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms/search/findByChromBpLocationRange'
             '?chrom=%s&bpStart=%d&bpEnd=%d' % (chromosome,
                                                start, end), interactive=interactive))
 
 
-def get_variants_by_cytogenetic_band(cytogenetic_band: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
+def get_variants_by_cytogenetic_band(cytogenetic_band: str, interactive: bool = True) -> Variant:
     project_dir = os.path.split(os.path.realpath(__file__))[0]
     df = read_csv(project_dir + os.sep + 'cytogenetic_bands.csv', index_col='index', infer_datetime_format=True,
                   parse_dates=['last_download_date'])
     query_df = df[df['cytogenetic_band'] == cytogenetic_band]
     if query_df.size == 0:
-        return SingleNucleotidePolymorphism()
+        return Variant()
     else:
         chromosome = query_df.loc[:, 'chromosome'].values[0]
         start = query_df.loc[:, 'start'].values[0]
         end = query_df.loc[:, 'end'].values[0]
     return get_variants_by_genomic_range(chromosome, start, end, interactive=interactive)
 
 
-def get_variants_by_gene_name(gene_name: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+def get_variants_by_gene_name(gene_name: str, interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs(
             'https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms/search/findByGene?geneName=%s' % gene_name,
             interactive=interactive))
 
 
-def get_variants_by_efo_trait(efo_trait: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+def get_variants_by_efo_trait(efo_trait: str, interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs(
             'https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms/search/findByEfoTrait?efoTrait=%s' % efo_trait,
             interactive=interactive))
 
 
-def get_variants_by_reported_trait(reported_trait: str, interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+def get_variants_by_reported_trait(reported_trait: str, interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs(
             'https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms/search/findByDiseaseTrait?diseaseTrait=%s' % reported_trait,
             interactive=interactive))
 
 
-def get_variants_all(interactive: bool = True) -> SingleNucleotidePolymorphism:
-    return SingleNucleotidePolymorphism(
+def get_variants_all(interactive: bool = True) -> Variant:
+    return Variant(
         client.get_SNPs('https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms', interactive=interactive))
 
 
 def get_variants(study_id: str = None, association_id: str = None, variant_id: str = None, efo_id: str = None,
                  pubmed_id: str = None, genomic_range: List[int] = None,
                  gene_name: str = None, efo_trait: str = None, reported_trait: str = None,
                  set_operation: str = 'bind',
-                 interactive: bool = True) -> SingleNucleotidePolymorphism:
+                 interactive: bool = True) -> Variant:
     if study_id is None and association_id is None and variant_id is None and efo_id is None and pubmed_id is None and genomic_range is None and gene_name is None and efo_trait is None and reported_trait is None:
-        return SingleNucleotidePolymorphism(
+        return Variant(
             client.get_SNPs('https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms',
                             interactive=interactive))
     variants = {}
     if study_id is not None:
         variants['study_id'] = client.get_SNPs('https://www.ebi.ac.uk/gwas/rest/api/studies/%s/snps' % study_id,
                                                interactive=interactive)
 
@@ -140,22 +140,22 @@
         variants['reported_trait'] = client.get_SNPs(
             'https://www.ebi.ac.uk/gwas/rest/api/singleNucleotidePolymorphisms/search/findByDiseaseTrait?diseaseTrait=%s' % reported_trait,
             interactive=interactive)
     if set_operation == 'bind':
         all_data = []
         for singe_get in variants.values():
             all_data.extend(singe_get)
-        return SingleNucleotidePolymorphism(all_data)
+        return Variant(all_data)
     else:
         rsId_dict = {}
         rsId_sets = []
         for singe_get in variants.values():
             temp_set = set()
             for i in singe_get:
                 rsId_dict[i.get('rsId')] = i
                 temp_set.add(i.get('rsId'))
             rsId_sets.append(temp_set)
         intersection_rsId = reduce(lambda x, y: x.intersection(y), rsId_sets)
         intersection_result = []
         for k in intersection_rsId:
             intersection_result.append(rsId_dict.get(k))
-        return SingleNucleotidePolymorphism(intersection_result)
+        return Variant(intersection_result)
```

### Comparing `pandasgwas-0.99.9/pandasgwas/get_associations.py` & `pandasgwas-1.0.0/pandasgwas/get_associations.py`

 * *Files identical despite different names*

### Comparing `pandasgwas-0.99.9/pandasgwas/get_studies.py` & `pandasgwas-1.0.0/pandasgwas/get_studies.py`

 * *Files identical despite different names*

### Comparing `pandasgwas-0.99.9/pandasgwas/get_traits.py` & `pandasgwas-1.0.0/pandasgwas/get_traits.py`

 * *Files identical despite different names*

### Comparing `pandasgwas-0.99.9/pandasgwas.egg-info/SOURCES.txt` & `pandasgwas-1.0.0/pandasgwas.egg-info/SOURCES.txt`

 * *Files 9% similar despite different names*

```diff
@@ -1,22 +1,25 @@
 LICENSE
 README.md
 pyproject.toml
 setup.py
 pandasgwas/Association.py
 pandasgwas/Browser.py
-pandasgwas/SingleNucleotidePolymorphism.py
 pandasgwas/Study.py
 pandasgwas/Trait.py
+pandasgwas/Variant.py
 pandasgwas/__init__.py
 pandasgwas/client.py
 pandasgwas/cytogenetic_bands.csv
-pandasgwas/get_SNPs.py
 pandasgwas/get_associations.py
 pandasgwas/get_studies.py
 pandasgwas/get_traits.py
+pandasgwas/get_variants.py
+pandasgwas/harmonised_list.txt
 pandasgwas/set_operation.py
+pandasgwas/summary_statistics.py
+pandasgwas/utility.py
 pandasgwas.egg-info/PKG-INFO
 pandasgwas.egg-info/SOURCES.txt
 pandasgwas.egg-info/dependency_links.txt
 pandasgwas.egg-info/requires.txt
 pandasgwas.egg-info/top_level.txt
```

### Comparing `pandasgwas-0.99.9/setup.py` & `pandasgwas-1.0.0/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,34 +1,34 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="pandasgwas",
-    version="0.99.9",
+    version="1.0.0",
     author="Cao Tianze",
     author_email="hnrcao@qq.com",
-    description="A Python package for easy retrieval of GWAS catalog data",
+    description="A Python package for easy retrieval of GWAS Catalog data",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/caotianze/pandasgwas",
     project_urls={
         "Bug Tracker": "https://github.com/caotianze/pandasgwas/issues",
     },
     classifiers=[
-        "Development Status :: 4 - Beta",
+        "Development Status :: 5 - Production/Stable",
         "Programming Language :: Python :: 3",
         "Programming Language :: Python :: 3.8",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
     ],
     # package_dir={"": "pandasgwas"},
     packages=['pandasgwas'],
     python_requires=">=3.8",
-    install_requires=['pandas>=1.1.3, <=1.2.5', 'requests>=2.28.1', 'progressbar2>=4.0.0'],
+    install_requires=['pandas>=1.4.3', 'requests>=2.28.1', 'progressbar2>=4.0.0'],
     license="MIT",
     keywords=['gwas', 'genomics', 'snp', 'bioinformatics','pandas'],
     package_data={
-        "": ["*.csv"]
+        "": ["*.csv","*.txt"]
     }
 )
```

