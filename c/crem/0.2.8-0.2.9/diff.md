# Comparing `tmp/crem-0.2.8.tar.gz` & `tmp/crem-0.2.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/crem-0.2.8.tar", last modified: Fri Feb  4 12:53:58 2022, max compression
+gzip compressed data, was "dist/crem-0.2.9.tar", last modified: Fri Feb  4 13:57:38 2022, max compression
```

## Comparing `crem-0.2.8.tar` & `crem-0.2.9.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxr-x   0 pavel     (1000) pavel     (1000)        0 2022-02-04 12:53:58.000000 crem-0.2.8/
--rw-rw-r--   0 pavel     (1000) pavel     (1000)    10629 2022-02-04 12:53:58.000000 crem-0.2.8/PKG-INFO
-drwxrwxr-x   0 pavel     (1000) pavel     (1000)        0 2022-02-04 12:53:58.000000 crem-0.2.8/crem.egg-info/
--rw-rw-r--   0 pavel     (1000) pavel     (1000)    10629 2022-02-04 12:53:58.000000 crem-0.2.8/crem.egg-info/PKG-INFO
--rw-rw-r--   0 pavel     (1000) pavel     (1000)      448 2022-02-04 12:53:58.000000 crem-0.2.8/crem.egg-info/SOURCES.txt
--rw-rw-r--   0 pavel     (1000) pavel     (1000)      210 2022-02-04 12:53:58.000000 crem-0.2.8/crem.egg-info/entry_points.txt
--rw-rw-r--   0 pavel     (1000) pavel     (1000)        5 2022-02-04 12:53:58.000000 crem-0.2.8/crem.egg-info/top_level.txt
--rw-rw-r--   0 pavel     (1000) pavel     (1000)       24 2022-02-04 12:53:58.000000 crem-0.2.8/crem.egg-info/requires.txt
--rw-rw-r--   0 pavel     (1000) pavel     (1000)        1 2022-02-04 12:53:58.000000 crem-0.2.8/crem.egg-info/dependency_links.txt
--rw-rw-r--   0 pavel     (1000) pavel     (1000)       79 2022-02-04 12:53:58.000000 crem-0.2.8/setup.cfg
-drwxrwxr-x   0 pavel     (1000) pavel     (1000)        0 2022-02-04 12:53:58.000000 crem-0.2.8/crem/
--rw-rw-r--   0 pavel     (1000) pavel     (1000)    42588 2022-02-04 12:46:43.000000 crem-0.2.8/crem/crem.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)     1396 2019-11-25 13:17:56.000000 crem-0.2.8/crem/functions.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)     3214 2021-12-12 19:22:13.000000 crem-0.2.8/crem/fragmentation.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)     6389 2020-04-04 13:19:20.000000 crem-0.2.8/crem/frag_to_env_mp.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)     9235 2021-11-11 15:15:55.000000 crem-0.2.8/crem/utils.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)    11778 2021-02-20 14:08:59.000000 crem-0.2.8/crem/mol_context.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)     5590 2020-09-01 18:23:43.000000 crem-0.2.8/crem/import_env_to_db.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)    12411 2020-04-05 17:50:03.000000 crem-0.2.8/crem/guacamol_crem_test.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)      379 2022-02-04 12:50:11.000000 crem-0.2.8/crem/__init__.py
-drwxrwxr-x   0 pavel     (1000) pavel     (1000)        0 2022-02-04 12:53:58.000000 crem-0.2.8/crem/scripts/
--rwxr-xr-x   0 pavel     (1000) pavel     (1000)     1012 2020-03-06 18:29:49.000000 crem-0.2.8/crem/scripts/crem_create_frag_db.sh
--rw-rw-r--   0 pavel     (1000) pavel     (1000)     4868 2020-03-13 07:00:24.000000 crem-0.2.8/crem/guacamol_distribution_test.py
--rw-rw-r--   0 pavel     (1000) pavel     (1000)     8210 2021-12-02 14:16:44.000000 crem-0.2.8/README.md
--rw-rw-r--   0 pavel     (1000) pavel     (1000)     1342 2020-08-18 18:47:01.000000 crem-0.2.8/setup.py
+drwxrwxr-x   0 pavel     (1000) pavel     (1000)        0 2022-02-04 13:57:38.000000 crem-0.2.9/
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)    10629 2022-02-04 13:57:38.000000 crem-0.2.9/PKG-INFO
+drwxrwxr-x   0 pavel     (1000) pavel     (1000)        0 2022-02-04 13:57:38.000000 crem-0.2.9/crem.egg-info/
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)    10629 2022-02-04 13:57:38.000000 crem-0.2.9/crem.egg-info/PKG-INFO
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)      448 2022-02-04 13:57:38.000000 crem-0.2.9/crem.egg-info/SOURCES.txt
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)      210 2022-02-04 13:57:38.000000 crem-0.2.9/crem.egg-info/entry_points.txt
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)        5 2022-02-04 13:57:38.000000 crem-0.2.9/crem.egg-info/top_level.txt
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)       24 2022-02-04 13:57:38.000000 crem-0.2.9/crem.egg-info/requires.txt
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)        1 2022-02-04 13:57:38.000000 crem-0.2.9/crem.egg-info/dependency_links.txt
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)       79 2022-02-04 13:57:38.000000 crem-0.2.9/setup.cfg
+drwxrwxr-x   0 pavel     (1000) pavel     (1000)        0 2022-02-04 13:57:38.000000 crem-0.2.9/crem/
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)    42632 2022-02-04 13:53:42.000000 crem-0.2.9/crem/crem.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)     1396 2019-11-25 13:17:56.000000 crem-0.2.9/crem/functions.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)     3214 2021-12-12 19:22:13.000000 crem-0.2.9/crem/fragmentation.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)     6389 2020-04-04 13:19:20.000000 crem-0.2.9/crem/frag_to_env_mp.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)     9235 2021-11-11 15:15:55.000000 crem-0.2.9/crem/utils.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)    11778 2021-02-20 14:08:59.000000 crem-0.2.9/crem/mol_context.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)     5590 2020-09-01 18:23:43.000000 crem-0.2.9/crem/import_env_to_db.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)    12411 2020-04-05 17:50:03.000000 crem-0.2.9/crem/guacamol_crem_test.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)      379 2022-02-04 13:56:19.000000 crem-0.2.9/crem/__init__.py
+drwxrwxr-x   0 pavel     (1000) pavel     (1000)        0 2022-02-04 13:57:38.000000 crem-0.2.9/crem/scripts/
+-rwxr-xr-x   0 pavel     (1000) pavel     (1000)     1012 2020-03-06 18:29:49.000000 crem-0.2.9/crem/scripts/crem_create_frag_db.sh
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)     4868 2020-03-13 07:00:24.000000 crem-0.2.9/crem/guacamol_distribution_test.py
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)     8210 2021-12-02 14:16:44.000000 crem-0.2.9/README.md
+-rw-rw-r--   0 pavel     (1000) pavel     (1000)     1342 2020-08-18 18:47:01.000000 crem-0.2.9/setup.py
```

### Comparing `crem-0.2.8/PKG-INFO` & `crem-0.2.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: crem
-Version: 0.2.8
+Version: 0.2.9
 Summary: CReM: chemically reasonable mutations framework
 Home-page: https://github.com/DrrDom/crem
 Author: Pavel Polishchuk
 Author-email: pavel_polishchuk@ukr.net
 License: UNKNOWN
 Description: # CReM - chemically reasonable mutations
```

### Comparing `crem-0.2.8/crem.egg-info/PKG-INFO` & `crem-0.2.9/crem.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: crem
-Version: 0.2.8
+Version: 0.2.9
 Summary: CReM: chemically reasonable mutations framework
 Home-page: https://github.com/DrrDom/crem
 Author: Pavel Polishchuk
 Author-email: pavel_polishchuk@ukr.net
 License: UNKNOWN
 Description: # CReM - chemically reasonable mutations
```

### Comparing `crem-0.2.8/crem/crem.py` & `crem-0.2.9/crem/crem.py`

 * *Files 2% similar despite different names*

```diff
@@ -490,15 +490,15 @@
                                                                 min_inc=min_inc, max_inc=max_inc,
                                                                 max_replacements=max_replacements,
                                                                 replace_cycles=replace_cycles,
                                                                 protected_ids_1=protected_ids, protected_ids_2=None,
                                                                 min_freq=min_freq, symmetry_fixes=symmetry_fixes,
                                                                 **kwargs):
             for smi, m, rxn in __frag_replace(mol, None, frag_sma, core_sma, radius, ids, None):
-                if max_replacements is None or (max_replacements is not None and len(products) < max_replacements):
+                if max_replacements is None or len(products) < (max_replacements + 1):  # +1 because we added source mol to output smiles
                     if smi not in products:
                         products.add(smi)
                         res = [smi]
                         if return_rxn:
                             res.append(rxn)
                             if return_rxn_freq:
                                 res.append(freq)
@@ -513,15 +513,15 @@
         p = Pool(min(ncores, cpu_count()))
         for items in p.imap(__frag_replace_mp, __get_data(mol, db_name, radius, min_size, max_size, min_rel_size,
                                                           max_rel_size, min_inc, max_inc, replace_cycles,
                                                           protected_ids, min_freq, max_replacements, symmetry_fixes,
                                                           **kwargs),
                             chunksize=100):
             for smi, m, rxn, freq in items:
-                if max_replacements is None or (max_replacements is not None and len(products) < max_replacements):
+                if max_replacements is None or len(products) < (max_replacements + 1):  # +1 because we added source mol to output smiles
                     if smi not in products:
                         products.add(smi)
                         res = [smi]
                         if return_rxn:
                             res.append(rxn)
                             if return_rxn_freq:
                                 res.append(freq)
```

### Comparing `crem-0.2.8/crem/functions.py` & `crem-0.2.9/crem/functions.py`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/crem/fragmentation.py` & `crem-0.2.9/crem/fragmentation.py`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/crem/frag_to_env_mp.py` & `crem-0.2.9/crem/frag_to_env_mp.py`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/crem/utils.py` & `crem-0.2.9/crem/utils.py`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/crem/mol_context.py` & `crem-0.2.9/crem/mol_context.py`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/crem/import_env_to_db.py` & `crem-0.2.9/crem/import_env_to_db.py`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/crem/guacamol_crem_test.py` & `crem-0.2.9/crem/guacamol_crem_test.py`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/crem/scripts/crem_create_frag_db.sh` & `crem-0.2.9/crem/scripts/crem_create_frag_db.sh`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/crem/guacamol_distribution_test.py` & `crem-0.2.9/crem/guacamol_distribution_test.py`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/README.md` & `crem-0.2.9/README.md`

 * *Files identical despite different names*

### Comparing `crem-0.2.8/setup.py` & `crem-0.2.9/setup.py`

 * *Files identical despite different names*

