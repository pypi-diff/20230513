# Comparing `tmp/khipu-metabolomics-0.6.0.tar.gz` & `tmp/khipu-metabolomics-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "khipu-metabolomics-0.6.0.tar", last modified: Sat Apr  1 20:33:17 2023, max compression
+gzip compressed data, was "/Users/shuzhao/li.github/khipu/dist/.tmp-1ubjmb2p/khipu-metabolomics-0.7.0.tar", last modified: Sat May 13 20:35:01 2023, max compression
```

## Comparing `khipu-metabolomics-0.6.0.tar` & `khipu-metabolomics-0.7.0.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 lish       (501) staff       (20)        0 2023-04-01 20:33:17.599201 khipu-metabolomics-0.6.0/
--rw-r--r--   0 lish       (501) staff       (20)      360 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/LICENSE
--rw-r--r--   0 lish       (501) staff       (20)     8280 2023-04-01 20:33:17.598871 khipu-metabolomics-0.6.0/PKG-INFO
--rw-r--r--   0 lish       (501) staff       (20)     7438 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/README.md
-drwxr-xr-x   0 lish       (501) staff       (20)        0 2023-04-01 20:33:17.596776 khipu-metabolomics-0.6.0/khipu/
--rw-r--r--   0 lish       (501) staff       (20)       22 2023-04-01 20:28:45.000000 khipu-metabolomics-0.6.0/khipu/__init__.py
--rw-r--r--   0 lish       (501) staff       (20)       24 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/khipu/command_line.py
--rw-r--r--   0 lish       (501) staff       (20)     4073 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/khipu/epdsConstructor.py
--rw-r--r--   0 lish       (501) staff       (20)    12942 2023-04-01 20:20:10.000000 khipu-metabolomics-0.6.0/khipu/extended.py
--rw-r--r--   0 lish       (501) staff       (20)     1474 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/khipu/main.py
--rw-r--r--   0 lish       (501) staff       (20)    29762 2023-04-01 20:27:26.000000 khipu-metabolomics-0.6.0/khipu/model.py
--rw-r--r--   0 lish       (501) staff       (20)     1471 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/khipu/plot.py
--rw-r--r--   0 lish       (501) staff       (20)     4269 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/khipu/test.py
--rw-r--r--   0 lish       (501) staff       (20)    21323 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/khipu/utils.py
-drwxr-xr-x   0 lish       (501) staff       (20)        0 2023-04-01 20:33:17.598463 khipu-metabolomics-0.6.0/khipu_metabolomics.egg-info/
--rw-r--r--   0 lish       (501) staff       (20)     8280 2023-04-01 20:33:17.000000 khipu-metabolomics-0.6.0/khipu_metabolomics.egg-info/PKG-INFO
--rw-r--r--   0 lish       (501) staff       (20)      435 2023-04-01 20:33:17.000000 khipu-metabolomics-0.6.0/khipu_metabolomics.egg-info/SOURCES.txt
--rw-r--r--   0 lish       (501) staff       (20)        1 2023-04-01 20:33:17.000000 khipu-metabolomics-0.6.0/khipu_metabolomics.egg-info/dependency_links.txt
--rw-r--r--   0 lish       (501) staff       (20)       50 2023-04-01 20:33:17.000000 khipu-metabolomics-0.6.0/khipu_metabolomics.egg-info/entry_points.txt
--rw-r--r--   0 lish       (501) staff       (20)       27 2023-04-01 20:33:17.000000 khipu-metabolomics-0.6.0/khipu_metabolomics.egg-info/requires.txt
--rw-r--r--   0 lish       (501) staff       (20)        6 2023-04-01 20:33:17.000000 khipu-metabolomics-0.6.0/khipu_metabolomics.egg-info/top_level.txt
--rw-r--r--   0 lish       (501) staff       (20)       38 2023-04-01 20:33:17.599282 khipu-metabolomics-0.6.0/setup.cfg
--rw-r--r--   0 lish       (501) staff       (20)     1412 2023-04-01 19:09:23.000000 khipu-metabolomics-0.6.0/setup.py
+drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/
+-rw-r--r--   0 shuzhao    (501) staff       (20)      360 2020-08-10 13:09:16.000000 khipu-metabolomics-0.7.0/LICENSE
+-rw-r--r--   0 shuzhao    (501) staff       (20)     8564 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/PKG-INFO
+-rw-r--r--   0 shuzhao    (501) staff       (20)     7722 2023-05-12 13:43:10.000000 khipu-metabolomics-0.7.0/README.md
+drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/khipu/
+-rw-r--r--   0 shuzhao    (501) staff       (20)       22 2023-05-13 16:09:34.000000 khipu-metabolomics-0.7.0/khipu/__init__.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)       24 2022-11-14 16:24:11.000000 khipu-metabolomics-0.7.0/khipu/command_line.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     3913 2023-05-13 17:49:54.000000 khipu-metabolomics-0.7.0/khipu/epdsConstructor.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)    13705 2023-05-13 17:49:54.000000 khipu-metabolomics-0.7.0/khipu/extended.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     1474 2022-12-26 02:11:23.000000 khipu-metabolomics-0.7.0/khipu/main.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)    30719 2023-05-13 17:02:39.000000 khipu-metabolomics-0.7.0/khipu/model.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     1471 2023-02-14 14:42:35.000000 khipu-metabolomics-0.7.0/khipu/plot.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)     4360 2023-05-13 20:30:26.000000 khipu-metabolomics-0.7.0/khipu/test.py
+-rw-r--r--   0 shuzhao    (501) staff       (20)    22536 2023-05-13 17:02:39.000000 khipu-metabolomics-0.7.0/khipu/utils.py
+drwxr-xr-x   0 shuzhao    (501) staff       (20)        0 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/khipu_metabolomics.egg-info/
+-rw-r--r--   0 shuzhao    (501) staff       (20)     8564 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/khipu_metabolomics.egg-info/PKG-INFO
+-rw-r--r--   0 shuzhao    (501) staff       (20)      435 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/khipu_metabolomics.egg-info/SOURCES.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)        1 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/khipu_metabolomics.egg-info/dependency_links.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)       50 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/khipu_metabolomics.egg-info/entry_points.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)       27 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/khipu_metabolomics.egg-info/requires.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)        6 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/khipu_metabolomics.egg-info/top_level.txt
+-rw-r--r--   0 shuzhao    (501) staff       (20)       38 2023-05-13 20:35:01.000000 khipu-metabolomics-0.7.0/setup.cfg
+-rw-r--r--   0 shuzhao    (501) staff       (20)     1412 2023-02-19 21:01:51.000000 khipu-metabolomics-0.7.0/setup.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive
+POSIX tar archive (GNU)
```

### Comparing `khipu-metabolomics-0.6.0/PKG-INFO` & `khipu-metabolomics-0.7.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: khipu-metabolomics
-Version: 0.6.0
+Version: 0.7.0
 Summary: Common utilities for interpreting mass spectrometry data
 Home-page: https://github.com/shuzhao-li/khipu
 Author: Shuzhao Li
 Author-email: shuzhao.li@gmail.com
 License: BSD
 Keywords: chemistry,bioinformatics,mass spectrometry
 Classifier: Development Status :: 4 - Beta
@@ -18,14 +18,18 @@
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # khipu: generalized tree structure to annotate untargeted metabolomics and stable isotope tracing data
 
+[![Documentation Status](https://readthedocs.org/projects/khipu/badge/?version=latest)](https://khipu.readthedocs.io/en/latest/?badge=latest)
+[![DOI](https://img.shields.io/badge/DOI-doi%2F10.1021%2Facs.analchem.2c05810-blue)](https://pubs.acs.org/doi/10.1021/acs.analchem.2c05810)
+
+
 Pre-annotation tool to annotate degenerate ions in relationships to the original compound and infer neutral mass. 
 
 This applies to regular LC-MS data, but also enables easy analysis of isotope tracing and chemical labeling data.
 
 ![khipugram](doc/khipugram.png)
 
 ## Implementation overview
```

### Comparing `khipu-metabolomics-0.6.0/README.md` & `khipu-metabolomics-0.7.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -1,9 +1,13 @@
 # khipu: generalized tree structure to annotate untargeted metabolomics and stable isotope tracing data
 
+[![Documentation Status](https://readthedocs.org/projects/khipu/badge/?version=latest)](https://khipu.readthedocs.io/en/latest/?badge=latest)
+[![DOI](https://img.shields.io/badge/DOI-doi%2F10.1021%2Facs.analchem.2c05810-blue)](https://pubs.acs.org/doi/10.1021/acs.analchem.2c05810)
+
+
 Pre-annotation tool to annotate degenerate ions in relationships to the original compound and infer neutral mass. 
 
 This applies to regular LC-MS data, but also enables easy analysis of isotope tracing and chemical labeling data.
 
 ![khipugram](doc/khipugram.png)
 
 ## Implementation overview
```

### Comparing `khipu-metabolomics-0.6.0/khipu/epdsConstructor.py` & `khipu-metabolomics-0.7.0/khipu/epdsConstructor.py`

 * *Files 9% similar despite different names*

```diff
@@ -16,31 +16,35 @@
 
 class epdsConstructor:
     '''Wrapper class to organize a list of peaks/features into a list of empirical compounds.
 
     To-dos:
         add support of user input formats where rtime isn't precise or unavailable.
         add options of coelution_function (see mass2chem.epdsConstructor )
+        Future consideration: explicitly model resolved and unresolved mass values (e.g. 34S vs 37Cl).
     '''
     def __init__(self, peak_list, mode='pos'):
         '''
         Parameters
         ----------
-        peak_list : [{'parent_masstrace_id': 1670, 'mz': 133.09702315984987, 'rtime': 654, 'height': 14388.0, 'id': 555}, ...]
-        mz_tolerance_ppm: ppm tolerance in examining m/z patterns.
+        peak_list : [{'parent_masstrace_id': 1670, 'mz': 133.09702315984987, 
+            'rtime': 654, 'height': 14388.0, 'id': 555}, ...]
+        mz_tolerance_ppm : ppm tolerance in examining m/z patterns.
         '''
         self.mode = mode
         self.peak_list = peak_list
 
     def peaks_to_epdDict(self, 
                         isotope_search_patterns,
                         adduct_search_patterns,
                         extended_adducts,
                         mz_tolerance_ppm,
                         rt_tolerance=2,
+                        charges=[1, 2, 3],
+                        has_parent_masstrack=True,
         ):
         '''
         Parameters
         ----------
         isotope_search_patterns : exact list used to retrieve the subnetworks. E.g. 
             [ (1.003355, '13C/12C', (0, 0.8)),
             (2.00671, '13C/12C*2', (0, 0.8)),
@@ -62,35 +66,24 @@
                 Default intended as 2 seconds.
 
         Returns
         -------
         epdDict : A dictionary of empCpds (empirical compounds) indexed by IDs ('interim_id').
                 Not including singletons.
         '''
-        subnetworks, peak_dict, _ = peaks_to_networks(self.peak_list,
-                    isotope_search_patterns,
-                    adduct_search_patterns,
-                    mz_tolerance_ppm,
-                    rt_tolerance
-        )
-        WV = Weavor(peak_dict, isotope_search_patterns=isotope_search_patterns, 
-                    adduct_search_patterns=adduct_search_patterns, 
-                    mz_tolerance_ppm=mz_tolerance_ppm, mode=self.mode)
-        print("\n")
-        print("Initial khipu search grid: ")
-        print(WV.mzgrid)
-        print("\n")
-
-        khipu_list = graphs_to_khipu_list(
-            subnetworks, WV, mz_tolerance_ppm=mz_tolerance_ppm,
-            )
-        khipu_list, all_assigned_peaks = extend_khipu_list(khipu_list, peak_dict, 
-                        extended_adducts, mz_tolerance_ppm=mz_tolerance_ppm,
-                        rt_tolerance=rt_tolerance)
-
+        khipu_list, all_assigned_peaks = peaklist_to_khipu_list(self.peak_list, 
+                    isotope_search_patterns=isotope_search_patterns, 
+                    adduct_search_patterns=adduct_search_patterns,
+                    extended_adducts=extended_adducts,
+                    mz_tolerance_ppm=mz_tolerance_ppm,
+                    rt_tolerance=rt_tolerance,
+                    mode=self.mode,
+                    charges=charges,
+                    has_parent_masstrack=has_parent_masstrack,
+                    )
         print("\n\n ~~~~~~ Got %d khipus, with %d features ~~~~~~~ \n\n" 
                     %(len(khipu_list), len(all_assigned_peaks)))
         empCpds = export_empCpd_khipu_list(khipu_list)
         epdDict = {}
         for E in empCpds:
             epdDict[E['interim_id']] = E
         return epdDict
```

### Comparing `khipu-metabolomics-0.6.0/khipu/extended.py` & `khipu-metabolomics-0.7.0/khipu/extended.py`

 * *Files 6% similar despite different names*

```diff
@@ -12,21 +12,23 @@
         '''Show what nodes are removed from input_network. After running self.build_khipu.
         '''
         print("nodes_to_use: ", self.nodes_to_use)
         print("redundant_nodes: ", self.redundant_nodes)
 
     def build_diagnostic_tree(self, input_network, depth_limit = 10):
         '''Build diagnostic tree using input nodes.
-
+        
         Updates
         -------
         self.diagnostic_tree as an instance of treelib.Tree.
 
-        Examples (tree here is diagnostic_tree)
+        Examples 
         --------
+        (tree here is diagnostic_tree)
+
         >>> KP = model.khipu()
         >>> KP.build_tree(big[0], peak_dict, edge_dict)
         >>> 
         >>> KP.tree.show()
         116.0707@138.3
         └── 117.0741@138.5
             ├── 120.084@136.8
@@ -46,17 +48,16 @@
                 ├── 122.0876@109.7
                 │   ├── 120.0808@109.9
                 │   └── 120.0808@110.6
                 ├── 122.0876@110.4
                 ├── 124.0943@110.8
                 └── 125.0976@110.6
 
-        Notes
-        -----
-        A minimum_spanning_tree will have all necessary patterns to cover full khipu, but not unique pattern.
+        Note:
+            A minimum_spanning_tree will have all necessary patterns to cover full khipu, but not unique pattern.
         '''
         T = nx.minimum_spanning_tree(input_network)
         peak_dict = self.feature_dict
         tree = treelib.Tree()
         root_node = self.root
         tree.create_node(make_peak_tag(peak_dict[root_node]), root_node, data=peak_dict[root_node])
 
@@ -129,120 +130,131 @@
             ii = np.argmin(abs(expected - x[0]))
             khipu_grid.iloc[np.unravel_index(ii, expected.shape)] = x[1]
         return khipu_grid
 
 
 # -----------------------------------------------------------------------------
 
-def local_read_file(infile, 
-                    start_col=3,
-                    end_col=6,
-                    isotope_search_patterns=isotope_search_patterns, 
-                    adduct_search_patterns=adduct_search_patterns,
-                    mz_tolerance_ppm=5,
-                    rt_tolerance=2, ):
+def local_read_file(infile, start_col=3, end_col=6):
     '''The input feature table must be a tab delimited file, with the first four columns as:
     ID, m/z, retention_time, intensity.
     Example data at '../testdata/full_Feature_table.tsv'.
+    Returns peaklist
     '''
     print("Working on file ", infile)
-    flist = read_features_from_text(open(infile).read(),
+    peaklist = read_features_from_text(open(infile).read(),
                     id_col=0, mz_col=1, rtime_col=2, intensity_cols=(start_col, end_col), delimiter="\t"
     )
-    subnetworks, peak_dict, edge_dict = peaks_to_networks(flist,
-                    isotope_search_patterns,
-                    adduct_search_patterns,
-                    mz_tolerance_ppm,
-                    rt_tolerance
-    )
-    return subnetworks, peak_dict, edge_dict
+    return peaklist
 
 def khipu_annotate(args):
     '''Automated pre-annotation using Khipu on a feature table.
     args as from parser.parse_args().
 
     One can follow the steps here to construct a custom workflow,
     using scripting or notebooks.
+
+    See also:
+        epdsConstructor.epdsConstructor for similar but embedded workflow.
     '''
     adduct_patterns = adduct_search_patterns
+    singleton_ion = 'M+H+'
     delta_mz = PROTON
     if args.mode == 'neg':
         adduct_patterns = adduct_search_patterns_neg
         delta_mz = -PROTON
+        singleton_ion = 'M-H-'
 
-    subnetworks, peak_dict, edge_dict = local_read_file(infile=args.input,
-                    start_col=args.start,
-                    end_col=args.end,
+    peaklist = local_read_file(infile=args.input, start_col=args.start, end_col=args.end)
+    peak_dict = make_peak_dict(peaklist)
+    khipu_list, all_assigned_peaks = peaklist_to_khipu_list(peaklist, 
                     isotope_search_patterns=isotope_search_patterns, 
                     adduct_search_patterns=adduct_patterns,
+                    extended_adducts=extended_adducts,
                     mz_tolerance_ppm=args.ppm,
                     rt_tolerance=args.rtol,
-    )
-    WV = Weavor(peak_dict, isotope_search_patterns=isotope_search_patterns, 
-                adduct_search_patterns=adduct_patterns, 
-                mz_tolerance_ppm=args.ppm, mode=args.mode)
-    print("\n")
-    print("Initial khipu search grid: ")
-    print(WV.mzgrid)
-    print("\n")
-
-    khipu_list = graphs_to_khipu_list(
-        subnetworks, WV, mz_tolerance_ppm=args.ppm,
-        )
-    khipu_list, all_assigned_peaks = extend_khipu_list(khipu_list, peak_dict, 
-                    extended_adducts, mz_tolerance_ppm=args.ppm,
-                    rt_tolerance=args.rtol)
+                    mode=args.mode,
+                    charges=[1, 2, 3],
+                    )
 
-    print("\n\n ~~~~~~ Got %d khipus, with %d features ~~~~~~~ \n\n" 
+    print("\n ~~~~~~ Got %d khipus, with %d features ~~~~~~~ \n\n" 
                 %(len(khipu_list), len(all_assigned_peaks)))
     empCpds = export_empCpd_khipu_list(khipu_list)
 
     outfile = 'khipu_test_empricalCompounds.json'
     if args.output:
         outfile = args.output + '.json'
     with open(outfile, 'w', encoding='utf-8') as f:
         json.dump(empCpds, f, ensure_ascii=False, indent=2)
 
-    singleton_ion = list(WV.mzgrid.columns)[0]
     export_khipu_table(outfile.replace(".json", ".tsv"), peak_dict, empCpds, singleton_ion, delta_mz)
 
 def peaklist_to_khipu_list(peaklist, 
                     isotope_search_patterns=isotope_search_patterns, 
                     adduct_search_patterns=adduct_search_patterns,
-
+                    extended_adducts=extended_adducts,
                     mz_tolerance_ppm=5,
                     rt_tolerance=2, 
-                    mode='pos'):
+                    mode='pos',
+                    charges=[1, 2, 3],
+                    has_parent_masstrack=False,
+                    ):
     '''A wrapper function easier for local data analysis.
     peaklist : list of input peaks/features in JSON notion as defined in Khipu or MetDataModel.
+    charges : multiple-charged ions considered.
     return khipu_list, all_assigned_peaks
     '''
-    subnetworks, peak_dict, edge_dict = peaks_to_networks(peaklist,
-                    isotope_search_patterns,
-                    adduct_search_patterns,
-                    mz_tolerance_ppm,
-                    rt_tolerance
-    )
-    WV = Weavor(peak_dict, isotope_search_patterns=isotope_search_patterns, 
-                adduct_search_patterns=adduct_search_patterns, 
-                mz_tolerance_ppm=mz_tolerance_ppm, 
-                mode=mode)
     print("\n")
-    print("Initial khipu search grid: ")
-    print(WV.mzgrid)
+    print("Multiple charges considered: " + str(charges))
     print("\n")
-    khipu_list = graphs_to_khipu_list(
-        subnetworks, WV, mz_tolerance_ppm=mz_tolerance_ppm,
+    khipu_list, assigned_peaks = [], []
+
+    for ch in charges:
+        iso_patterns = compute_multichaged_patterns(isotope_search_patterns, ch)
+        adduct_patterns = compute_multichaged_patterns(adduct_search_patterns, ch)
+        peaklist = [p for p in peaklist if p['id'] not in assigned_peaks]
+        subnetworks, peak_dict, edge_dict = peaks_to_networks(peaklist,
+                        iso_patterns,
+                        adduct_patterns,
+                        mz_tolerance_ppm,
+                        rt_tolerance
         )
-    khipu_list, all_assigned_peaks = extend_khipu_list(khipu_list, peak_dict, 
-                    extended_adducts, mz_tolerance_ppm=mz_tolerance_ppm,
-                    rt_tolerance=rt_tolerance)
+        WV = Weavor(peak_dict, isotope_search_patterns=iso_patterns, 
+                    adduct_search_patterns=adduct_patterns, 
+                    mz_tolerance_ppm=mz_tolerance_ppm, 
+                    mode=mode,
+                    charge=ch,
+                    parent_masstrack = has_parent_masstrack,
+                    )
+        print("Khipu search grid: ")
+        print(WV.mzgrid)
+        kps = graphs_to_khipu_list(
+            subnetworks, WV, mz_tolerance_ppm=mz_tolerance_ppm, id_start=len(khipu_list),
+            )
+        print(f"Constructed {len(kps)} khipus in this round.")
+        print("\n")
+        for KP in kps:
+            assigned_peaks += KP.nodes_to_use
+        khipu_list += kps
+    
+    dict_extended_adducts = {}
+    for ch in charges:
+        dict_extended_adducts[ch] = compute_multichaged_patterns(extended_adducts, ch)
+
+    khipu_list, all_assigned_peaks = extend_khipu_list(
+                    khipu_list, 
+                    peaklist, 
+                    dict_extended_adducts, 
+                    mz_tolerance_ppm=mz_tolerance_ppm,
+                    rt_tolerance=rt_tolerance
+                    )
+    
     return khipu_list, all_assigned_peaks
 
-def graphs_to_khipu_list(subnetworks, WeavorInstance, mz_tolerance_ppm):
+def graphs_to_khipu_list(subnetworks, WeavorInstance, mz_tolerance_ppm, id_start=0):
     '''Generate full khipu_list from subnetworks, 
     including iterative khipus based on features pruned out of initial subnetwork.
     '''
     khipu_list, khipu_list_valid = [], []
     for g in subnetworks:
         if g.number_of_edges() > 0:
             KP = Khipu(g)
@@ -254,37 +266,47 @@
                                         for c in nx.connected_components(KP.pruned_network)]
                 for _G in more_subnets:
                     KP = Khipu(_G)
                     KP.build_khipu(WeavorInstance, mz_tolerance_ppm)
                     khipu_list.append(KP)
 
     # assign IDs
-    ii = 0
+    ii = id_start
     for KP in khipu_list:
         if KP.valid:
             base_mz = str(round(KP.neutral_mass, 4))
             ii += 1
             KP.id = 'kp' + str(ii) + "_" + str(base_mz)
             khipu_list_valid.append(KP)
 
     return khipu_list_valid
 
-def extend_khipu_list(khipu_list, peak_dict, adduct_search_patterns_extended, 
-                      mz_tolerance_ppm=5, rt_tolerance=2):
+def extend_khipu_list(khipu_list, 
+                      peaklist, 
+                      dict_extended_adducts,
+                      mz_tolerance_ppm=5, 
+                      rt_tolerance=2
+                      ):
     '''Update khipus by extended adduct search.
     Returns updated khipu_list and list_assigned_peaks.
+    New in version 0.7: multiple charges are accommodated via dict_extended_adducts.
     '''
     list_assigned_peaks = []
     for KP in khipu_list:
         list_assigned_peaks += KP.nodes_to_use
-    unassigned_peaks = [v for x,v in peak_dict.items() if x not in list_assigned_peaks]
+    # unassigned_peaks = [v for x,v in peak_dict.items() if x not in list_assigned_peaks]
+    unassigned_peaks = [p for p in peaklist if p['id'] not in list_assigned_peaks]
     mztree = build_centurion_tree(unassigned_peaks)
     for KP in khipu_list:
-        added_peaks = KP.extended_search(mztree, 
-                            adduct_search_patterns_extended,  mz_tolerance_ppm, rt_tolerance)
+        added_peaks = KP.extended_search(
+                            mztree, 
+                            dict_extended_adducts[KP.charge],  
+                            mz_tolerance_ppm, 
+                            rt_tolerance
+                            )
         list_assigned_peaks += added_peaks
 
     return khipu_list, set(list_assigned_peaks)
 
 def export_json_khipu_list(khipu_list):
     J = []
     for KP in khipu_list:
@@ -312,15 +334,15 @@
     for J in json_khipu_list:
         for F in J["MS1_pseudo_Spectra"]:
             in_khipu_list.append(F['id'])
             s += '\t'.join([
                 F['id'], str(F['mz']), str(F['rtime']), J['interim_id'], str(J['neutral_formula_mass']), 
                 F.get('isotope', ''), F.get('modification', ''), F['ion_relation']
             ]) + '\n'
-    # other peaks
+    # singleton peaks
     for k,F in peak_dict.items(): 
         if k not in in_khipu_list:
             s += '\t'.join([
                 F['id'], str(F['mz']), str(F['rtime']), 'singleton', str(round(F['mz']-delta_mz,4)), 
                 'M0', singleton_ion, ''
             ]) + '\n'
```

### Comparing `khipu-metabolomics-0.6.0/khipu/main.py` & `khipu-metabolomics-0.7.0/khipu/main.py`

 * *Files identical despite different names*

### Comparing `khipu-metabolomics-0.6.0/khipu/model.py` & `khipu-metabolomics-0.7.0/khipu/model.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,33 +2,35 @@
 Comprehensive construction of empCpds via generic tree structures (khipu).
 Each khipu = empCpd["MS1_pseudo_Spectra"].
 This module contains two classes:
 Weavor is constructed once and provides the main algorithms and functions;
 Khipu is mainlty the data structures and built as one instance per emprical compound.
 So from one experiment/feature table, one may get 10**3 khipus.
 '''
-
+import logging
 import numpy as np
 import pandas as pd
 import treelib
 from scipy.optimize import curve_fit
 from .plot import plot_khipugram
 from .utils import *
 
 
 class Weavor:
     '''For each experiment, this class sets up a grid of isotopes and adducts,
     and provide function solve to produce matched features and inferred neutral mass.
     '''
     def __init__(self, peak_dict, 
                 isotope_search_patterns, adduct_search_patterns, 
-                mz_tolerance_ppm=5, mode='pos'):
+                mz_tolerance_ppm=5, mode='pos', charge=1, parent_masstrack=False):
         '''Initiate mzgrid and indices.        
         '''
         self.mode = mode
+        self.charge = charge
+        self.parent_masstrack = parent_masstrack                          # parent_masstrack from asari 
         self.mz_tolerance_ppm = mz_tolerance_ppm
         self.peak_dict = peak_dict
         self.isotope_search_patterns  = sorted(isotope_search_patterns)   # m/z sort search patterns
         self.adduct_search_patterns = sorted(adduct_search_patterns)
         self.make_grid()
 
     def make_grid(self):
@@ -47,15 +49,16 @@
         self.mzgrid : pd.DataFrame with isotopes as rows and adducts as cols
         '''
         _d, self.adduct_dict, self.isotope_dict = {}, {}, {}
         self.isotope_index = ['M0'] + [x[1] for x in self.isotope_search_patterns]
         for x in self.isotope_search_patterns:
             self.isotope_dict[x[1]] = x[0]
 
-        self.adduct_pattern = make_expected_adduct_index(self.mode, self.adduct_search_patterns)
+        self.adduct_pattern = make_expected_adduct_index(
+            self.mode, self.adduct_search_patterns, self.charge)
         # [(PRONTON, M+H+), ..., (42.0338, ACN), ...]
         self.adduct_index = [A[1] for A in self.adduct_pattern]
         for A in self.adduct_pattern:
             _d[A[1]] = [A[0]] + [A[0]+x[0] for x in self.isotope_search_patterns]
             self.adduct_dict[A[1]] = A[0]
 
         self._M, self._N = len(self.isotope_index), len(self.adduct_index)
@@ -126,23 +129,23 @@
         neutral_mass = self.regress_neutral_mass(feature_map)
 
         return neutral_mass, grid, feature_map
 
     def regress_neutral_mass(self, feature_map):
         '''Get neutral mass by regression on mapped features.
         feature_map : {feature_id: (isotope_index, adduct_index)}
-        return 
+        Returns inferred neutral mass.
         '''
         def _func(x, neu):
             return x + neu
         fixed_feature_list = list(feature_map.keys())
         Y = [self.peak_dict[f]['mz'] for f in fixed_feature_list]
         X = [self.mzgrid.at[feature_map[f][0], feature_map[f][1]] for f in fixed_feature_list]
         popt, _ = curve_fit(_func, X, Y)
-        neutral_mass = popt[0]
+        neutral_mass = popt[0] * self.charge
         return neutral_mass
 
     def trunk_solver(self, adduct_edges, branch_dict={}):
         '''Find best solution to fit a set of edges on the trunk. 
         This uses score_graph_on_trunk to score matched graph, which can be 
         abstracted_adduct_edges or regular adduct edges.
 
@@ -195,40 +198,44 @@
 
         score = len(feature_map)
 
         return score, feature_map
 
     def build_full_grid(self, abstracted_adduct_edges, branch_dict, nodes_to_use):
         '''Build a khipu grid, after the input network is cleaned to isotopic_edges and adduct_edges.
-        1) Get isotopic branches first, and treat them each branch as a node. This converts (U, V) to (U, B).
-            Done in Khipu.branch_abstraction().
+        
+        1) Get isotopic branches first, and treat them each branch as a node. This converts (U, V) to (U, B). Done in Khipu.branch_abstraction().
         2) Get optimal order of abstracted adduct_edges. Done in Weavor.trunk_solver(), by topology not involving m/z. 
         3) Generate grids starting from the smallest m/z in each branch. Get the grid of best feature map.
         4) Use the optimal feature map to set grids.
 
         Parameters
         ----------
-        abstracted_adduct_edges : list of nonredundant directed edges with data tag.
-            A node here can be a feature or a branch, which is a list of isotopes.
-        branch_dict : dictionary, branch ID to member features/nodes.
+            abstracted_adduct_edges
+                list of nonredundant directed edges with data tag.
+                A node here can be a feature or a branch, which is a list of isotopes.
+            branch_dict
+                dictionary, branch ID to member features/nodes.
 
         Returns
         -------
-        neutral_mass : inferred neutral mass by linear regression
-        grid : dataframe of features, coordinates as adduct/isotope
-        best_feature_map : optimal feature map as dict, {feature_id: (isotope_index, adduct_index), ...}
-
-        Notes
-        -----
-        We don't know the real root to start with, and can't assume the lowest m/z is M+H+ or M-H-.
-        The root should be inferred from best overall pattern match.
-        A pseudo-root is not necessarily M0, which may not be detected in perfect labeling experiments.
+            neutral_mass
+                inferred neutral mass by linear regression
+            grid
+                dataframe of features, coordinates as adduct/isotope
+            best_feature_map
+                optimal feature map as dict, {feature_id: (isotope_index, adduct_index), ...}
+
+        Note:
+            We don't know the real root to start with, and can't assume the lowest m/z is M+H+ or M-H-.
+            The root should be inferred from best overall pattern match.
+            A pseudo-root is not necessarily M0, which may not be detected in perfect labeling experiments.
 
-        Enforce unique node per grid, by best rtime with future option of a fitness function (Khipu.clean()). 
-        Extra nodes go to a new khipu.
+            Enforce unique node per grid, by best rtime with future option of a fitness function (Khipu.clean()). 
+            Extra nodes go to a new khipu.
         '''
         mz_features = [(self.peak_dict[f]['mz'], f) for f in nodes_to_use]
         root, edges = self.trunk_solver(abstracted_adduct_edges, branch_dict)
         abstracted_adducts = [root, ]
         abstracted_adduct_tags = [self.adduct_index[0], ]
         for e in edges:
             abstracted_adducts.append(e[1])
@@ -331,25 +338,29 @@
     def build_khipu(self, WeavorInstance, mz_tolerance_ppm=5, check_fitness=False):
         '''Convert a network of two types of edges, isotopic and adduct, to khipu instances of unique nodes.
         Use the grid to enforce unique ion in each position, as the initial network can contain 
         erroneously redundant leaves/nodes.
 
         WeavorInstance : Weavor instance to solve the grid.
         check_fitness : if True, chech if replacing with any redundant nodes improves fitness. 
-            This is a placeholder as a good fitness function is not easy to implement and it slows down computing.
-            Future use can be if check_fitness: self.select_by_fitness()
+        This is a placeholder as a good fitness function is not easy to implement and it slows down computing.
+        Future use can be if check_fitness: self.select_by_fitness()
 
         Updates
         -------
         self.khipu_grid : pd.DataFrame
         self.neutral_mass : inferred neutral mass for the khipu compound
         '''
         self._size_limit_ = WeavorInstance._size    # Set max limit of feature number based on grid size
+        self.charge = WeavorInstance.charge
         self.feature_dict, self.mzstr_dict = self.get_feature_dict(
-                                        WeavorInstance.peak_dict, mz_tolerance_ppm)
+                                        WeavorInstance.peak_dict, 
+                                        mz_tolerance_ppm,
+                                        WeavorInstance.parent_masstrack
+                                        )
         if self.input_network.number_of_edges() == 1:
             edge = list(self.input_network.edges(data=True))[0]
             self.neutral_mass, self.khipu_grid, self.feature_map =\
                         WeavorInstance.build_simple_pair_grid(edge)
             self.clean_network = self.input_network
             self.nodes_to_use = list(self.clean_network.nodes())
 
@@ -375,23 +386,28 @@
                 self.neutral_mass, self.khipu_grid, self.feature_map = \
                     WeavorInstance.build_branch_only_grid(self.sorted_mz_peak_ids)
             elif adduct_edges:          # trunk only, no isotopes
                 self.neutral_mass, self.khipu_grid, self.feature_map = \
                     WeavorInstance.build_trunk_only_grid(adduct_edges)
             else:
                 self.valid = False
-                print("Empty network - ", self.nodes_to_use, isotopic_edges, adduct_edges, 
-                                        self.input_network.edges(data=True))
+                logging.info(
+                    '\t'.join([str(x) for x in [
+                        "Empty network - ", self.nodes_to_use, isotopic_edges, adduct_edges, 
+                                        self.input_network.edges(data=True)
+                    ]])
+                )
             
         if self.feature_map:
             self.get_pruned_network()
 
 
     def get_pruned_network(self):
         '''Get extra features and edges that are not fit in this khipu.
+        
         Updates
         -------
         self.redundant_nodes
         self.pruned_network
         self.nodes_to_use
         '''
         _used_nodes = set(self.feature_map.keys())
@@ -410,23 +426,26 @@
         self.mzstr_dict
         self.median_rtime
         self.nodes_to_use
         self.redundant_nodes 
         self.sorted_mz_peak_ids
         self.root       # temporary
 
-        Notes
-        -----
-        Note: mzstr_dict can be problematic in data that were not processed well, 
-        because minor potential shift can confuse ion relations.
-        This clean() may cut some initial edges.
+        
+        Note: 
+            mzstr_dict can be problematic in data that were not processed well, 
+            because minor potential shift can confuse ion relations.
+            This clean() may cut some initial edges.
         '''
         if self.input_network.number_of_nodes() > self._size_limit_:
             self.input_network = self.down_size()
-        self.feature_dict, self.mzstr_dict = self.get_feature_dict(WeavorInstance.peak_dict, mz_tolerance_ppm)
+        self.feature_dict, self.mzstr_dict = self.get_feature_dict(WeavorInstance.peak_dict, 
+                                                                   mz_tolerance_ppm,
+                                                                   WeavorInstance.parent_masstrack
+                                                                   )
         self.median_rtime = np.median([self.feature_dict[n]['rtime'] for n in self.input_network])
         for k,v in self.mzstr_dict.items():
             # v as list of node IDs
             if len(v) == 1:
                 self.nodes_to_use.append(v[0])
             else:
                 sorted_by_rtime_match = sorted(
@@ -447,15 +466,15 @@
         ]
         _N = len(use_nodes)
         use_nodes = sorted(use_nodes, reverse=True)[:self._size_limit_]
         print("Downsized input network with %d features, highest peak at %s " %(_N, use_nodes[0][1]))
         new_network = self.input_network.subgraph([x[1] for x in use_nodes])
         return new_network
 
-    def get_feature_dict(self, peak_dict, mz_tolerance_ppm):
+    def get_feature_dict(self, peak_dict, mz_tolerance_ppm, has_parent_masstrack):
         '''Index all input features; establish str identifier for features of same/close m/z values.
         Base on asari mass track IDs; keep unique m/z only.
         It's more efficient to use, since feature_dict is much smaller than peak_dict.
 
         Parameters
         ----------
         peak_dict : dict of peaks/features indexed by IDs. Must have fields 
@@ -466,15 +485,16 @@
         -------
         feature_dict : feature_dict with 'parent_masstrack_id'.
         mzstr_dict : dict indexed by parent_masstrack_id, e.g. {'trackx': [f1, f2], ...}
         '''
         feature_dict, mzstr_dict = {}, {}
         for n in self.input_network.nodes():
             feature_dict[n] = peak_dict[n]
-        if 'parent_masstrack_id' not in feature_dict[n]:
+
+        if not has_parent_masstrack:
             feature_dict = assign_masstrack_ids_in_khipu(feature_dict, mz_tolerance_ppm)
 
         for n,v in feature_dict.items():
             parent_masstrack_id = v['parent_masstrack_id']
             if parent_masstrack_id in mzstr_dict:
                 mzstr_dict[parent_masstrack_id].append(n)
             else:
@@ -489,22 +509,23 @@
         
     def branch_abstraction(self, isotopic_edges, adduct_edges):
         '''Abstract a group of connecgted isotopic featrures into a branch.
         Reduce the input network to a set of abstracted_adduct_edges (hence new tree) of B-nodes.
         
         Returns
         -------
-        abstracted_adduct_edges : list of nonredundant directed edges with data tag
-        branch_dict : dictionary, branch ID to member features/nodes.
-
-        Notes
-        -----
-        Membership of B-nodes is returned as branch_dict, which is needed to realign to khipu grid.
-        Without branch constraint, the grid realignment is error prone.
-        Not checking if abstracted_adduct_edges are fully connected.
+            abstracted_adduct_edges
+                list of nonredundant directed edges with data tag
+            branch_dict
+                dictionary, branch ID to member features/nodes.
+
+        Note:
+            Membership of B-nodes is returned as branch_dict, which is needed to realign to khipu grid.
+            Without branch constraint, the grid realignment is error prone.
+            Not checking if abstracted_adduct_edges are fully connected.
         '''
         G = nx.Graph(isotopic_edges)
         subnetworks = [G.subgraph(c).copy() for c in nx.connected_components(G)]
         _dict_branch, branch_dict = {}, {}
         _ii = 0
         for g in subnetworks:
             nodes = list(g.nodes())
@@ -540,19 +561,19 @@
         Updates
         -------
         self.feature_map
         self.khipu_grid
 
         Returns
         -------
-        added_peaks
+        added_peaks : list of peak ids
 
-        Notes
-        -----
-        annotation_dict may have fewer nodes than nodes_to_use, but is preferred here for cleaner results.
+        
+        Note:
+            annotation_dict may have fewer nodes than nodes_to_use, but is preferred here for cleaner results.
         '''
         matched, _new_anno_dict = [], {}
         for n, v in self.feature_map.items():
             _iso, _ad = v
             P1 = self.feature_dict[n]
             for _pair in adduct_search_patterns_extended:
                 (mass_difference, relation) = _pair[:2]
```

### Comparing `khipu-metabolomics-0.6.0/khipu/plot.py` & `khipu-metabolomics-0.7.0/khipu/plot.py`

 * *Files identical despite different names*

### Comparing `khipu-metabolomics-0.6.0/khipu/test.py` & `khipu-metabolomics-0.7.0/khipu/test.py`

 * *Files 1% similar despite different names*

```diff
@@ -92,15 +92,15 @@
     print("\n\n")
     print("Build and export JSON file of full list of khipus: ")
     print("================================================== \n")
 
     khipu_list = graphs_to_khipu_list(
         subnetworks, WV, mz_tolerance_ppm=5)
     
-    # khipu_list = extend_khipu_list(khipu_list, peak_dict, adduct_search_patterns_extended)
+    # khipu_list = extend_khipu_list(khipu_list, peaks, adduct_search_patterns_extended)
     print("\n\n ~~~~~~ Got %d khipus ~~~~~~~ \n\n" %len(khipu_list))
     empCpds = export_empCpd_khipu_list(khipu_list)
 
     outfile = 'khipu_test_empricalCompounds.json'
     with open(outfile, 'w', encoding='utf-8') as f:
         json.dump(empCpds, f, ensure_ascii=False, indent=2)
 
@@ -120,15 +120,17 @@
 
     ECCON = epdsConstructor(list_peaks, mode=mode)
     dict_empCpds = ECCON.peaks_to_epdDict(
                         isotope_search_patterns,
                         adduct_patterns,
                         extended_adducts,
                         mz_tolerance_ppm,
-                        # rt_tolerance,
+                        rt_tolerance=2,
+                        charges=[1, 2, 3],
+                        has_parent_masstrack=False,
         ) 
     outfile = 'khipu_test2.json'
     with open(outfile, 'w', encoding='utf-8') as f:
         json.dump(dict_empCpds, f, ensure_ascii=False, indent=2)
 
 
 #
```

### Comparing `khipu-metabolomics-0.6.0/khipu/utils.py` & `khipu-metabolomics-0.7.0/khipu/utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,22 +3,26 @@
 Adduct rules can be still better learned in the future.
 '''
 import json
 import numpy as np
 import networkx as nx
 from mass2chem.search import build_centurion_tree, find_all_matches_centurion_indexed_list
 
+import logging
+logging.basicConfig(filename='khipu.log', level=logging.INFO)   #  encoding='utf-8',
 
 #
 # m/z differences corresponding to adducts and isotopes
 # Not using charge in tables, because all m/z diff is relative to other charged ions
 #
 PROTON = 1.00727646677
 electron = 0.000549
 
+# These are single-charged values. 
+# Double and Tripple charged ions are computed after the initial round, on the fly
 # avoid confusing adducts in initial search, e.g. H, H2O
 adduct_search_patterns = [  # initial patterns are relative to M+H+
                             (21.9820, 'Na/H'),
                             (41.026549, 'ACN'),     # Acetonitrile
                             (35.9767, 'HCl'),
                             (37.955882, 'K/H'),
                             ]
@@ -42,25 +46,28 @@
                             (10.03355, '13C/12C*10', (0, 0.8)),
                             (11.036905, '13C/12C*11', (0, 0.8)),
                             (12.04026, '13C/12C*12', (0, 0.8)),
                             ]
 
 extended_adducts = [(1.0078, 'H'),
                             (-1.0078, '-H'),
-                            (10.991, 'Na/H, double charged'),
-                            (0.5017, '13C/12C, double charged'),
-                            (117.02655, '-NH3'),
+                            (1.9972, '37/35Cl'),
+                            (-17.02655, '-NH3'),
                             (17.02655, 'NH3'),
                             (-18.0106, '-H2O'),
                             (18.0106, 'H2O'),      # easy to confuse with bio reactions
                             (18.033823, 'NH4'),
                             (27.01089904, 'HCN'),
-                            (37.94694, 'Ca/H2'),
+                            (27.99492, 'CO'),
                             (32.026215, 'MeOH'),
+                            (-35.037114, '-NH3-H2O'),
+                            (37.94694, 'Ca/H2'),
                             (43.96389, 'Na2/H2'),
+                            (46.00548, 'CO2H2'),
+                            (-46.00548, '-CO2H2'),
                             (67.987424, 'NaCOOH'),
                             (83.961361, 'KCOOH'),
                             (97.96737927, 'H2SO4'),
                             (97.97689507, 'H3PO4'),
 ]
 
 relabel_dict = {
@@ -68,54 +75,79 @@
     'M+H+,HCl': 'M+HCl+H+',
     'M+H+,K/H': 'M+K+',
     'M+H+,ACN': 'M+ACN+H+',
     'M+H+,NH3': 'M+NH4+',
     'M+H+,M+H+,Na2/H2': 'M-H+Na+Na+',
 }
 
+def compute_multichaged_patterns(pattern=[(21.9820, 'Na/H'), (41.026549, 'ACN')], charge=2):
+    '''
+    Compute and return mass difference patterns for multiple charged ions.
+    '''
+    new = [list(x) for x in pattern]
+    note = ''
+    if charge > 1:
+        note = f", {charge}x charged"
+    for x in new:
+        x[0] = x[0] / charge
+        x[1] = x[1] + note
+    return new
+
 def make_expected_adduct_index(mode='pos', 
-                               pattern=[(21.9820, 'Na/H'), (41.026549, 'ACN')]):
+                               pattern=[(21.9820, 'Na/H'), (41.026549, 'ACN')],
+                               charge=1,
+                               ):
     '''Construct the adduct list for a core list of adduct m/z diff patterns. 
     Use neutral mass as 0 offset, so that later regression will compute neutral mass.
     Not modify adduct tag, so that the edges can be later mapped correctly.
     '''
     if mode == 'pos':
         # pos base ion as M+H+
-        return [(PROTON, 'M+H+'), ] + [(x[0] + PROTON, x[1]) for x in pattern] 
+        A0 = compute_multichaged_patterns([(PROTON, 'M+H+')], charge)
+        return A0 + [(x[0] + PROTON, x[1]) for x in pattern] 
     else:
         # neg base ion as M-H[-]
-        return [(-PROTON, 'M-H-')] + [(x[0] - PROTON, x[1]) for x in pattern]
+        A0 = compute_multichaged_patterns([(-PROTON, 'M-H-')], charge)
+        return A0 + [(x[0] - PROTON, x[1]) for x in pattern]
 
 
 def read_features_from_text(text_table, 
                         id_col=0, mz_col=1, rtime_col=2, 
                         intensity_cols=(3, 6), delimiter="\t"):
     '''
     Read a text feature table into a list of features.
+    
     Input
     -----
-    text_table: Tab delimited feature table read as text. First line as header.
-                    Recommended col 0 for ID, col 1 for m/z, col 2 for rtime.
-    id_col: column for id. If feature ID is not given, row_number is used as ID.
-    mz_col: column for m/z.
-    rtime_col: column for retention time.
-    intensity_cols: range of columns for intensity values. E.g. (3,5) includes only col 3 and 4.
+    text_table:
+        Tab delimited feature table read as text. First line as header.
+        Recommended col 0 for ID, col 1 for m/z, col 2 for rtime.
+    id_col: 
+        column for id. If feature ID is not given, row_number is used as ID.
+    mz_col: 
+        column for m/z.
+    rtime_col: 
+        column for retention time.
+    intensity_cols: 
+        range of columns for intensity values. E.g. (3,5) includes only col 3 and 4.
+    
     Return
     ------
-    List of features: [{'id': '', 'mz': 0, 'rtime': 0, 
-                        intensities: [], 'representative_intensity': 0, ...}, 
-                        ...], 
-                        where representative_intensity is mean value.
+    List of features: 
+        [{'id': '', 'mz': 0, 'rtime': 0, 
+        intensities: [], 'representative_intensity': 0, ...}, 
+        ...], 
+        where representative_intensity is mean value.
     '''
     # featureLines = open(feature_table).read().splitlines()
     featureLines = text_table.splitlines()
     header = featureLines[0].split(delimiter)
     num_features = len(featureLines)-1
     # sanity check
-    print("table header looks like: ", header[:intensity_cols[1]])
+    print("table header looks like: \n  ", header[:intensity_cols[1]])
     print("Read %d feature lines" %num_features)
     L = []
     for ii in range(1, num_features+1):
         if featureLines[ii].strip():
             a = featureLines[ii].split(delimiter)
             if isinstance(id_col, int):         # feature id specified
                 iid = a[id_col]
@@ -171,30 +203,32 @@
 
 def assign_masstrack_ids_in_khipu(feature_dict, mz_tolerance_ppm=5):
     '''Assign mass track ids if they are not included in peak dict.
     They should be if features were processed by asari.
 
     Parameters
     ----------
-    feature_dict : feature dictionary indexed by feature ids, based on input network to khipu, 
+    feature_dict : 
+        feature dictionary indexed by feature ids, based on input network to khipu, 
         thus very limited size.
-    mz_tolerance_ppm : ppm tolerance in examining m/z groups.
+    mz_tolerance_ppm : 
+        ppm tolerance in examining m/z groups.
 
     Returns
     -------
     Updated feature_dict with 'parent_masstrack_id'.
 
-    Notes
-    -----
-    Sort by m/z; separate by mz_tolerance_ppm.
-    m/z has to be check by ppm because 1) minor variation may exist btw peaks; and 
-    2) float numbers are bad for dictionary keys.
-    This method can be occasionally problematic in data that were not processed well,
-    by accidently merging m/z regions, therefore causing problems in downstream determination of ion relations.
-    (Why mass track is good in asari.)
+    
+    Note:
+        Sort by m/z; separate by mz_tolerance_ppm.
+        m/z has to be check by ppm because 1) minor variation may exist btw peaks; and 
+        2) float numbers are bad for dictionary keys.
+        This method can be occasionally problematic in data that were not processed well,
+        by accidently merging m/z regions, therefore causing problems in downstream determination of ion relations.
+        (Why mass track is good in asari.)
     '''
     features = sorted([(feature_dict[n]['mz'], n) for n in feature_dict])
     _N = len(features)
     current_mz = features[0][0]
     str_mz = str(current_mz)
     feature_dict[features[0][1]]['parent_masstrack_id'] = str_mz
     for x in features[1:]:
@@ -216,29 +250,34 @@
     '''
     To find all isotope pairs. 
     Similar to search.get_seed_empCpd_signatures, but return unidirectional pairs only.
     If input peaks have overlaps/duplicates, result will contain the redundant overlap peaks.
 
     Input
     =====
-    list_peaks: [{'parent_masstrace_id': 1670, 'mz': 133.09702315984987, 'rtime': 654, 'height': 14388.0, 'id': 555}, ...]
-    mztree: indexed list_peaks
-    mz_tolerance_ppm: ppm tolerance in examining m/z patterns.
-    search_patterns: a list in the format of [(mz difference, notion, (ratio low limit, ratio high limit)), ..]
-            This can be obtained through search.isotopic_patterns. The ratios are optional, because 
-            1) naturally occuring constrains are based on chemical formula;
-            2) rules are different when isotope tracers are introduced to the experiments.
-            But it's important to have a comprehensive list here for isotope tracing experiments.
-    rt_tolerance: tolerance threshold for deviation in retetion time, arbitrary unit depending on input data.
-            Default intended as 2 seconds.
+    list_peaks: 
+        [{'parent_masstrace_id': 1670, 'mz': 133.09702315984987, 'rtime': 654, 'height': 14388.0, 'id': 555}, ...]
+    mztree: 
+        indexed list_peaks
+    mz_tolerance_ppm: 
+        ppm tolerance in examining m/z patterns.
+    search_patterns: 
+        a list in the format of [(mz difference, notion, (ratio low limit, ratio high limit)), ..]
+        This can be obtained through search.isotopic_patterns. The ratios are optional, because 
+        1) naturally occuring constrains are based on chemical formula;
+        2) rules are different when isotope tracers are introduced to the experiments.
+        But it's important to have a comprehensive list here for isotope tracing experiments.
+    rt_tolerance: 
+        tolerance threshold for deviation in retetion time, arbitrary unit depending on input data.
+        Default intended as 2 seconds.
 
     Return
     ======
-    list of lists of peak pairs that match search_patterns patterns, e.g.
-    [ (195, 206, '13C/12C'), ...]. 
+        list of lists of peak pairs that match search_patterns patterns, 
+        e.g.[ (195, 206, '13C/12C'), ...]. 
     '''
     signatures = []
     for P1 in list_peaks:
         matched = [  ] 
         for _pair in search_patterns:
             (mass_difference, relation) = _pair[:2]
             tmp = find_all_matches_centurion_indexed_list(P1['mz'] + mass_difference, mztree, mz_tolerance_ppm)
@@ -259,25 +298,30 @@
                     mz_tolerance_ppm=5, rt_tolerance=2,
                     ):
     '''
     To find all pairs of adducts (fragments and neutral loss can be accommodated using negative mz difference). 
 
     Input
     =====
-    list_peaks: [{'parent_masstrace_id': 1670, 'mz': 133.09702315984987, 'rtime': 654, 'height': 14388.0, 'id': 555}, ...]
-    mztree: indexed list_peaks
-    mz_tolerance_ppm: ppm tolerance in examining m/z patterns.
-    search_patterns: a list in the format of [(mz difference, notion), ...] 
-    rt_tolerance: tolerance threshold for deviation in retetion time, arbitrary unit depending on input data.
-            Default intended as 2 seconds.
+    list_peaks: 
+        [{'parent_masstrace_id': 1670, 'mz': 133.09702315984987, 'rtime': 654, 'height': 14388.0, 'id': 555}, ...]
+    mztree: 
+        indexed list_peaks
+    mz_tolerance_ppm: 
+        ppm tolerance in examining m/z patterns.
+    search_patterns: 
+        a list in the format of [(mz difference, notion), ...] 
+    rt_tolerance: 
+        tolerance threshold for deviation in retetion time, arbitrary unit depending on input data.
+        Default intended as 2 seconds.
 
     Return
     ======
-    list of lists of peak pairs that match search_patterns patterns, e.g.
-    [ (195, 206, 'H/Na'), ...]. 
+        list of lists of peak pairs that match search_patterns patterns, e.g.
+        [ (195, 206, 'H/Na'), ...]. 
     '''
     signatures = []
     for P1 in list_peaks:
         matched = [  ] 
         for _pair in search_patterns:
             (mass_difference, relation) = _pair[:2]
             tmp = find_all_matches_centurion_indexed_list(P1['mz'] + mass_difference, mztree, mz_tolerance_ppm)
@@ -301,54 +345,61 @@
                     mz_tolerance_ppm=5, 
                     rt_tolerance=2, 
                     ):
     '''Search peak_list for patterns of isotopes and adducts, form a network and get connected subnetworks.
     
     Parameters
     ----------
-    list_peaks : [{'mz': 133.09702315984987, 'rtime': 654, 'id': 555}, ...]
+    list_peaks : 
+        [{'mz': 133.09702315984987, 'rtime': 654, 'id': 555}, ...]
 
-    isotope_search_patterns : exact list used to retrieve the subnetworks. E.g. 
+    isotope_search_patterns : 
+        exact list used to retrieve the subnetworks. E.g. 
         [ (1.003355, '13C/12C', (0, 0.8)),
         (2.00671, '13C/12C*2', (0, 0.8)),
         (3.010065, '13C/12C*3', (0, 0.8)),
         (4.01342, '13C/12C*4', (0, 0.8)),
         (5.016775, '13C/12C*5', (0, 0.8)),
         (6.02013, '13C/12C*6', (0, 0.8)),]
 
-    adduct_search_patterns : exact list used to retrieve the subnetworks. 
+    adduct_search_patterns : 
+        exact list used to retrieve the subnetworks. 
         It's not recommended to have a long list here, as it's better to search additional 
         in-source modifications after empCpds are seeded. Example adduct_search_patterns list: 
         [ (1.0078, 'H'), 
         (21.9820, 'Na/H'), 
         (41.026549, 'Acetonitrile')]
 
-    mz_tolerance_ppm : ppm tolerance in examining m/z patterns.
-    rt_tolerance: tolerance threshold for deviation in retetion time, arbitrary unit depending on input data.
-            Default intended as 2 seconds.
+    mz_tolerance_ppm : 
+        ppm tolerance in examining m/z patterns.
+    rt_tolerance: 
+        tolerance threshold for deviation in retetion time, arbitrary unit depending on input data.
+        Default intended as 2 seconds.
 
     Returns
     -------
-    subnetwork : undirected graph. Example edges:
+    subnetwork : 
+        undirected graph. Example edges:
         [('F1606', 'F20', {'type': 'modification', 'tag': 'H'}), 
         ('F3533', 'F20', {'type': 'modification', 'tag': 'Na/H'}), 
         ('F195', 'F20', {'type': 'modification', 'tag': 'Acetonitrile'}), 
         ('F20', 'F807', {'type': 'modification', 'tag': 'Acetonitrile'}), 
         ('F20', 'F53', {'type': 'isotope', 'tag': '13C/12C'}), 
         ('F874', 'F808', {'type': 'isotope', 'tag': '13C/12C'})]
+    peak_dict : 
+        JSON peaks indexed by ID
+    edge_dict :     
+        edge_tag is str sorted, but the dict values preserve the direction, which is missed in nx.subnetwork.
 
-    peak_dict : JSON peaks indexed by ID
-    edge_dict : edge_tag is str sorted, but the dict values preserve the direction, which is missed in nx.subnetwork.
-
-    Notes
-    -----
-    Features of low abundance may not have detectable isotopes, but can have multiple adducts.
-    Do not include too many adducts in the intial search. 
-    Do not include neutral loss and fragments in initial search.
-    They are better done after a list of khipus are constructed.
+        
+    Note:
+        Features of low abundance may not have detectable isotopes, but can have multiple adducts.
+        Do not include too many adducts in the intial search. 
+        Do not include neutral loss and fragments in initial search.
+        They are better done after a list of khipus are constructed.
     '''
     mztree = build_centurion_tree(peak_list)
     peak_dict = make_peak_dict(peak_list)
     iso_edges = get_isotopic_edge_pairs(peak_list, mztree, 
                                         search_patterns=isotope_search_patterns,
                                         mz_tolerance_ppm=mz_tolerance_ppm,
                                         isotope_rt_tolerance=rt_tolerance,
@@ -382,43 +433,47 @@
     '''To snap isotopic branch. Assume lowest m/z as M0, and re-align other features against M0.
         Because edges in input_network can be relationship between any pairs. 
         Re-alignment will get them consistent on grid.
         No redundant features are allowed here, whihc are handled in khipu.clean().
 
     Parameters
     ----------
-    sorted_mz_peak_ids : [(mz, peak_id), ...]; must be unique per m/z. khipu.khipu.clean() takes care of that.
-    isotope_search_patterns : [ (1.003355, '13C/12C', (0, 0.8)), (3.010065, '13C/12C*3', (0, 0.8)),..]
+    sorted_mz_peak_ids : 
+        [(mz, peak_id), ...]; must be unique per m/z. khipu.khipu.clean() takes care of that.
+    isotope_search_patterns : 
+        [ (1.003355, '13C/12C', (0, 0.8)), (3.010065, '13C/12C*3', (0, 0.8)),..]
 
     Returns
     -------
     A dictionary of {'M0': F1, '13C/12C*2': F11, ...}
     '''
     M0 = sorted_mz_peak_ids[0]
     _d = {'M0': M0[1]}
     for p in sorted_mz_peak_ids[1:]:
         match = get_isotope_pattern_name(p[0] - M0[0], isotope_search_patterns, mz_tolerance)
         if match == 'Unknown':
             # _d["? " + p[1]] = p[1]
-            print("Unknown isotope match ~ ", p)
+            logging.info("Unknown isotope match ~ " + str(p))
         else:
             _d[match] = p[1]
 
     return _d
 
 def realign_isotopes_reverse(sorted_mz_peak_ids, isotope_search_patterns, mz_tolerance=0.01):
     '''To snap isotopic branch. Assume lowest m/z as M0, and re-align other features against M0.
         Because edges in g can be relationship between any pairs. 
         Re-alignment will get them consistent on grid.
         No redundant features are allowed here, whihc are handled in khipu.clean().
 
     Parameters
     ----------
-    sorted_mz_peak_ids : [(mz, peak_id), ...]; unique per m/z not required, different from realign_isotopes.
-    isotope_search_patterns : [ (1.003355, '13C/12C', (0, 0.8)), (3.010065, '13C/12C*3', (0, 0.8)),..]
+    sorted_mz_peak_ids : 
+        [(mz, peak_id), ...]; unique per m/z not required, different from realign_isotopes.
+    isotope_search_patterns : 
+        [ (1.003355, '13C/12C', (0, 0.8)), (3.010065, '13C/12C*3', (0, 0.8)),..]
 
     Returns
     -------
     A dictionary of {F0: 'M0', F1, '13C/12C*2', ...}
     '''
     M0 = sorted_mz_peak_ids[0]
     _d = {'M0': M0[1]}
@@ -428,21 +483,22 @@
 
 def get_isotope_pattern_name(mz, isotope_search_patterns, mz_tolerance=0.01):
     '''Get the isotope with closest m/z match. 
     If error > mz_tolerance, return Unknown, 
     which can happen if the isotope_search_patterns does not cover all possible labled atoms.
     The mz_tolerance needs not to be too precise, as input value was from isotopic_edges.
     Used by realign_isotopes.
+   
     Returns
     -------
     A name in isotope_search_patterns or 'Unknown'.
     '''
     L = sorted([(abs(mz-x[0]), x[1]) for x in isotope_search_patterns])
     if L[0][0] > mz_tolerance:
-        print("Warning no match in isotope_pattern: ", mz)
+        logging.info("Warning no match in isotope_pattern: " + str(mz))
         return 'Unknown'
     else:
         return L[0][1]
 
 
 def add_data_to_tag(trees, len_limit=20):
     '''
@@ -503,19 +559,23 @@
     if x[1][-1] == '-':     # charged
         return x[0]
     else:
         return x[0]-PROTON
 
 def __mass_pair_mapping(list1, list2):
     '''Placeholder. Find best matched value_index in list2 for each value in list1.
+    
     Parameters
     ----------
-    list1, list2 : each a list of m/z values
+    list1, list2 :  
+        each a list of m/z values
+    
     Returns
     -------
-    list1_matched : list of index position of best match in list2 for each value in list1
-    Notes
-    -----
-    ref: asari.mass_functions.complete_mass_paired_mapping
-    Given the small size of matrices in khipu, np.argmin() is a better solution.
+    list1_matched : 
+        list of index position of best match in list2 for each value in list1
+    
+    Note:
+        ref: asari.mass_functions.complete_mass_paired_mapping
+        Given the small size of matrices in khipu, np.argmin() is a better solution.
     '''
     pass
```

### Comparing `khipu-metabolomics-0.6.0/khipu_metabolomics.egg-info/PKG-INFO` & `khipu-metabolomics-0.7.0/khipu_metabolomics.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: khipu-metabolomics
-Version: 0.6.0
+Version: 0.7.0
 Summary: Common utilities for interpreting mass spectrometry data
 Home-page: https://github.com/shuzhao-li/khipu
 Author: Shuzhao Li
 Author-email: shuzhao.li@gmail.com
 License: BSD
 Keywords: chemistry,bioinformatics,mass spectrometry
 Classifier: Development Status :: 4 - Beta
@@ -18,14 +18,18 @@
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # khipu: generalized tree structure to annotate untargeted metabolomics and stable isotope tracing data
 
+[![Documentation Status](https://readthedocs.org/projects/khipu/badge/?version=latest)](https://khipu.readthedocs.io/en/latest/?badge=latest)
+[![DOI](https://img.shields.io/badge/DOI-doi%2F10.1021%2Facs.analchem.2c05810-blue)](https://pubs.acs.org/doi/10.1021/acs.analchem.2c05810)
+
+
 Pre-annotation tool to annotate degenerate ions in relationships to the original compound and infer neutral mass. 
 
 This applies to regular LC-MS data, but also enables easy analysis of isotope tracing and chemical labeling data.
 
 ![khipugram](doc/khipugram.png)
 
 ## Implementation overview
```

### Comparing `khipu-metabolomics-0.6.0/setup.py` & `khipu-metabolomics-0.7.0/setup.py`

 * *Files identical despite different names*

