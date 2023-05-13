# Comparing `tmp/noise2read-0.0.75.tar.gz` & `tmp/noise2read-0.0.76.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "noise2read-0.0.75.tar", last modified: Mon May  1 13:43:48 2023, max compression
+gzip compressed data, was "noise2read-0.0.76.tar", last modified: Sat May 13 12:25:23 2023, max compression
```

## Comparing `noise2read-0.0.75.tar` & `noise2read-0.0.76.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-01 13:43:48.084283 noise2read-0.0.75/
--rw-r--r--   0 pping    (55472) Research  (5010)     1068 2023-04-20 03:30:20.000000 noise2read-0.0.75/LICENSE
--rw-r--r--   0 pping    (55472) Research  (5010)     1627 2023-05-01 13:43:48.088562 noise2read-0.0.75/PKG-INFO
--rw-r--r--   0 pping    (55472) Research  (5010)     1208 2023-05-01 13:35:09.000000 noise2read-0.0.75/README.rst
--rw-r--r--   0 pping    (55472) Research  (5010)       90 2023-04-20 03:30:20.000000 noise2read-0.0.75/pyproject.toml
--rw-r--r--   0 pping    (55472) Research  (5010)     1000 2023-05-01 13:43:48.097016 noise2read-0.0.75/setup.cfg
-drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-01 13:43:47.704235 noise2read-0.0.75/src/
-drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-01 13:43:47.925626 noise2read-0.0.75/src/noise2read/
--rw-r--r--   0 pping    (55472) Research  (5010)      182 2023-04-23 01:19:38.000000 noise2read-0.0.75/src/noise2read/__init__.py
--rw-r--r--   0 pping    (55472) Research  (5010)    12784 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/classifier.py
--rw-r--r--   0 pping    (55472) Research  (5010)    16050 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/config.py
--rw-r--r--   0 pping    (55472) Research  (5010)     2701 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/coverage.py
--rw-r--r--   0 pping    (55472) Research  (5010)    70175 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/data_analysis.py
--rw-r--r--   0 pping    (55472) Research  (5010)    45141 2023-04-23 06:01:09.000000 noise2read-0.0.75/src/noise2read/data_generation.py
--rw-r--r--   0 pping    (55472) Research  (5010)    11181 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/data_preprocessing.py
--rw-r--r--   0 pping    (55472) Research  (5010)    29580 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/encoding.py
--rw-r--r--   0 pping    (55472) Research  (5010)    30699 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/error_orrection.py
--rw-r--r--   0 pping    (55472) Research  (5010)    16773 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/isolates_correction.py
--rw-r--r--   0 pping    (55472) Research  (5010)    26366 2023-04-25 08:21:29.000000 noise2read-0.0.75/src/noise2read/noise2read.py
--rw-r--r--   0 pping    (55472) Research  (5010)    34369 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/reads2vectors.py
--rw-r--r--   0 pping    (55472) Research  (5010)    12273 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/simulation.py
--rw-r--r--   0 pping    (55472) Research  (5010)     3475 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/umitest.py
--rw-r--r--   0 pping    (55472) Research  (5010)    15905 2023-04-20 03:30:20.000000 noise2read-0.0.75/src/noise2read/utils.py
-drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-01 13:43:48.038058 noise2read-0.0.75/src/noise2read.egg-info/
--rw-r--r--   0 pping    (55472) Research  (5010)     1627 2023-05-01 13:43:47.000000 noise2read-0.0.75/src/noise2read.egg-info/PKG-INFO
--rw-r--r--   0 pping    (55472) Research  (5010)      837 2023-05-01 13:43:47.000000 noise2read-0.0.75/src/noise2read.egg-info/SOURCES.txt
--rw-r--r--   0 pping    (55472) Research  (5010)        1 2023-05-01 13:43:47.000000 noise2read-0.0.75/src/noise2read.egg-info/dependency_links.txt
--rw-r--r--   0 pping    (55472) Research  (5010)       58 2023-05-01 13:43:47.000000 noise2read-0.0.75/src/noise2read.egg-info/entry_points.txt
--rw-r--r--   0 pping    (55472) Research  (5010)        1 2023-04-20 03:31:42.000000 noise2read-0.0.75/src/noise2read.egg-info/not-zip-safe
--rw-r--r--   0 pping    (55472) Research  (5010)      218 2023-05-01 13:43:47.000000 noise2read-0.0.75/src/noise2read.egg-info/requires.txt
--rw-r--r--   0 pping    (55472) Research  (5010)       11 2023-05-01 13:43:47.000000 noise2read-0.0.75/src/noise2read.egg-info/top_level.txt
-drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-01 13:43:48.071005 noise2read-0.0.75/tests/
--rw-r--r--   0 pping    (55472) Research  (5010)     3641 2023-04-20 03:30:20.000000 noise2read-0.0.75/tests/test_data_generation.py
--rw-r--r--   0 pping    (55472) Research  (5010)      985 2023-04-20 03:30:20.000000 noise2read-0.0.75/tests/test_reads2vector.py
--rw-r--r--   0 pping    (55472) Research  (5010)     4216 2023-04-20 03:30:20.000000 noise2read-0.0.75/tests/test_utils.py
+drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-13 12:25:23.722598 noise2read-0.0.76/
+-rw-r--r--   0 pping    (55472) Research  (5010)     1068 2023-04-20 03:30:20.000000 noise2read-0.0.76/LICENSE
+-rw-r--r--   0 pping    (55472) Research  (5010)     5951 2023-05-13 12:25:23.724444 noise2read-0.0.76/PKG-INFO
+-rw-r--r--   0 pping    (55472) Research  (5010)     5531 2023-05-13 12:21:26.000000 noise2read-0.0.76/README.rst
+-rw-r--r--   0 pping    (55472) Research  (5010)       90 2023-04-20 03:30:20.000000 noise2read-0.0.76/pyproject.toml
+-rw-r--r--   0 pping    (55472) Research  (5010)     1000 2023-05-13 12:25:23.727464 noise2read-0.0.76/setup.cfg
+drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-13 12:25:23.572083 noise2read-0.0.76/src/
+drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-13 12:25:23.668244 noise2read-0.0.76/src/noise2read/
+-rw-r--r--   0 pping    (55472) Research  (5010)      182 2023-05-13 06:56:03.000000 noise2read-0.0.76/src/noise2read/__init__.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    12784 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/classifier.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    15992 2023-05-03 12:02:17.000000 noise2read-0.0.76/src/noise2read/config.py
+-rw-r--r--   0 pping    (55472) Research  (5010)     2701 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/coverage.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    70175 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/data_analysis.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    45703 2023-05-13 12:24:51.000000 noise2read-0.0.76/src/noise2read/data_generation.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    11181 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/data_preprocessing.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    29580 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/encoding.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    30699 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/error_orrection.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    16773 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/isolates_correction.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    26366 2023-04-25 08:21:29.000000 noise2read-0.0.76/src/noise2read/noise2read.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    34369 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/reads2vectors.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    12273 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/simulation.py
+-rw-r--r--   0 pping    (55472) Research  (5010)     3475 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/umitest.py
+-rw-r--r--   0 pping    (55472) Research  (5010)    15905 2023-04-20 03:30:20.000000 noise2read-0.0.76/src/noise2read/utils.py
+drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-13 12:25:23.703091 noise2read-0.0.76/src/noise2read.egg-info/
+-rw-r--r--   0 pping    (55472) Research  (5010)     5951 2023-05-13 12:25:23.000000 noise2read-0.0.76/src/noise2read.egg-info/PKG-INFO
+-rw-r--r--   0 pping    (55472) Research  (5010)      837 2023-05-13 12:25:23.000000 noise2read-0.0.76/src/noise2read.egg-info/SOURCES.txt
+-rw-r--r--   0 pping    (55472) Research  (5010)        1 2023-05-13 12:25:23.000000 noise2read-0.0.76/src/noise2read.egg-info/dependency_links.txt
+-rw-r--r--   0 pping    (55472) Research  (5010)       58 2023-05-13 12:25:23.000000 noise2read-0.0.76/src/noise2read.egg-info/entry_points.txt
+-rw-r--r--   0 pping    (55472) Research  (5010)        1 2023-04-20 03:31:42.000000 noise2read-0.0.76/src/noise2read.egg-info/not-zip-safe
+-rw-r--r--   0 pping    (55472) Research  (5010)      218 2023-05-13 12:25:23.000000 noise2read-0.0.76/src/noise2read.egg-info/requires.txt
+-rw-r--r--   0 pping    (55472) Research  (5010)       11 2023-05-13 12:25:23.000000 noise2read-0.0.76/src/noise2read.egg-info/top_level.txt
+drwxr-xr-x   0 pping    (55472) Research  (5010)        0 2023-05-13 12:25:23.717768 noise2read-0.0.76/tests/
+-rw-r--r--   0 pping    (55472) Research  (5010)     3641 2023-04-20 03:30:20.000000 noise2read-0.0.76/tests/test_data_generation.py
+-rw-r--r--   0 pping    (55472) Research  (5010)      985 2023-04-20 03:30:20.000000 noise2read-0.0.76/tests/test_reads2vector.py
+-rw-r--r--   0 pping    (55472) Research  (5010)     4216 2023-04-20 03:30:20.000000 noise2read-0.0.76/tests/test_utils.py
```

### Comparing `noise2read-0.0.75/LICENSE` & `noise2read-0.0.76/LICENSE`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/setup.cfg` & `noise2read-0.0.76/setup.cfg`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/classifier.py` & `noise2read-0.0.76/src/noise2read/classifier.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/config.py` & `noise2read-0.0.76/src/noise2read/config.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # -*- coding: utf-8 -*-
 # @Author: Pengyao Ping
 # @Date:   2023-01-19 10:56:38
 # @Last Modified by:   Pengyao Ping
-# @Last Modified time: 2023-02-16 11:10:21
+# @Last Modified time: 2023-05-03 22:02:17
 
 import configparser
 import os
 
 class Config(object):
     def __init__(self, config_file, logger):
         conf = configparser.ConfigParser()
@@ -31,15 +31,15 @@
             if conf.has_option("SourceInputData", "correct_data"):
                 self.correct_data = conf.get("SourceInputData", "correct_data")
 
             # setting model parameters
             if conf.has_option("General", "num_workers"):
                 self.num_workers = conf.getint("General", "num_workers")
             else:
-                self.num_workers = -1 # this set will use total cpu cores - 2  
+                self.num_workers = -1   
             if conf.has_option("General", "verbose"):
                 self.verbose = conf.getboolean("General", "verbose")
             else:
                 self.verbose = False
             if conf.has_option("General", "min_iters"):
                 self.min_iters = conf.getint("General", "min_iters")
             else:
@@ -260,27 +260,27 @@
                 self.error_rate = conf.getfloat("Simulation", "error_rate")
             else:
                 self.error_rate = 0.001 # default
             if conf.has_option("Simulation", "min_read_count"):
                 self.min_read_count = conf.getint("Simulation", "min_read_count")
             else:
                 self.min_read_count = 30 # default
-            # Evaluation
-            if conf.has_option("Evaluation", "delta"):
-                self.delta = conf.getint("Evaluation", "delta")
-            else:
-                self.delta = 10 # default
+            # # Evaluation
+            # if conf.has_option("Evaluation", "delta"):
+            #     self.delta = conf.getint("Evaluation", "delta")
+            # else:
+            #     self.delta = 10 # default
 
         if config_file == None:
             # path
             self.result_dir = os.path.join(base_path, 'result/')
             # input
             self.ground_truth_data = None  
             # general
-            self.num_workers = -1 # this set will use totalcpu - 2 
+            self.num_workers = -1 
             self.min_iters = 1000
             self.verbose = False 
             self.iso_change_detail = False     
             self.top_n = 100      
             # self.over_sampling = True 
             self.negative_sample_num = 500000
             self.min_read_len = 30
@@ -341,15 +341,15 @@
 
             # simulation
             self.min_read_count = 30
             self.substations = True
             self.indels = False
             self.error_rate = 0.001
 
-            # Evaluation
-            self.delta = 1
+            # # Evaluation
+            # self.delta = 1
 
             # # coverage
             # self.library_layout = 'PE'
             # self.Alignment = '--local' # '--end-to-end'
```

### Comparing `noise2read-0.0.75/src/noise2read/coverage.py` & `noise2read-0.0.76/src/noise2read/coverage.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/data_analysis.py` & `noise2read-0.0.76/src/noise2read/data_analysis.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/data_generation.py` & `noise2read-0.0.76/src/noise2read/data_generation.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # -*- coding: utf-8 -*-
 # @Author: Pengyao Ping
 # @Date:   2023-01-16 15:52:44
 # @Last Modified by:   Pengyao Ping
-# @Last Modified time: 2023-04-23 16:01:09
+# @Last Modified time: 2023-05-13 22:24:36
 
 import editdistance
 import networkx as nx
 import os
 import csv
 from tqdm import tqdm
 from noise2read.utils import *
@@ -28,15 +28,15 @@
         Args:
             logger (class): customized logging
             config (class): parameters below setting using configparser
                 parameters:
                 config.num_workers (int): the number of subprocesses to use.
                 config.input_file (str): The filename including path to be corrected.
                 config.result_dir (str): Full pathname where the results will be saved.
-                config.high_freq_thre (int, optional): The threshold of the high frequency. Defaults to 5.
+                config.high_freq_thre (int, optional): The threshold of the high frequency. Defaults to 4.
                 config.max_error_freq (int, optional): The highest frequency of error sequences. Defaults to 3.
                 config.save_graph (bool, optional): If true, noise2read will save the construted graph to file. Defaults to False. 
                 config.graph_visualization (bool, optional): If true, noise2read will draw the connected subgraphs of the construted  graph. Defaults to False.
                 config.drawing_graph_num (int, optional): The number of subgraphs will be drawing. Defaults to 50.
                 config.high_ambiguous (bool, optional): If true, noise2read will predict high ambiguous errors. Defaults to False.
                 config.min_iters (int, optional): Minimum progress display update interval in iterations for the module tqdm. Defaults to 100.
                 config.verbose (bool, optional): If true, noise2read will save the genuine, ambiguous errors and negative reads to csv.
@@ -227,15 +227,15 @@
                             tt = nei_degree * 0.5 + nei_count * 0.5
                             nei_degree_count.append((nei, tt, nei_count))
                         # nei2count.sort(key=lambda x:x[1], reverse=True)
                         nei_degree_count.sort(key=lambda x:x[1], reverse=True)
                         # first_nei, first_nei_count = nei2count[0]
                         first_nei, tt, first_nei_count = nei_degree_count[0]
                         first_nei_degree = sub_graph.degree[first_nei]
-                        if first_nei_count >= self.config.high_freq_thre:
+                        if first_nei_count > self.config.high_freq_thre:
                             line = [first_nei, first_nei_count, first_nei_degree, node, node_count, node_degree]
                             newline = self.err_type_classification(line)
                             genuine_df.loc[len(genuine_df)] = newline
                             sub_graph.nodes[node]['flag'] = True
                     else:
                         continue   
         if self.config.verbose:
@@ -348,54 +348,59 @@
                 node_degree = sub_graph.degree[node]
                 if node_count <= self.config.max_error_freq and not sub_graph.nodes[node]['flag']:
                     node_neis = [n for n in sub_graph.neighbors(node)]
                     if node_degree == 1:
                         nei = node_neis[0]
                         nei_count = sub_graph.nodes[nei]['count']
                         nei_degree = sub_graph.degree[nei]
-                        if nei_count >= self.config.high_freq_thre:
+                        # if nei_count >= self.config.high_freq_thre:
+                        if nei_count > self.config.high_freq_thre:
                             line = [nei, nei_count, nei_degree, node, node_count, node_degree]
                             if edit_dis == 1:
                                 newline = self.err_type_classification(line)
                                 # gen_df.loc[len(gen_df)] = newline
                                 gen_lst.append(newline)
                                 del line, newline 
                             else:
                                 # gen_df.loc[len(gen_df)] = line 
                                 gen_lst.append(line)
                                 del line                                   
-                    elif node_degree <= self.config.ambiguous_error_node_degree:
+                    # elif node_degree <= self.config.ambiguous_error_node_degree: # comment this line on 13 May 2023
+                    else:
                         high_num = 0
                         nei2count = []
                         for nei in node_neis:
                             nei_count = sub_graph.nodes[nei]['count']
                             nei_degree = sub_graph.degree[nei]
-                            if nei_count >= self.config.high_freq_thre:
+                            # if nei_count >= self.config.high_freq_thre:
+                            if nei_count > self.config.high_freq_thre:
                                 high_num += 1
                                 nei2count.append((nei, nei_count))
                         if high_num == 1:             
                             nei2count.sort(key=lambda x:x[1], reverse=True)
                             first_nei, first_nei_count = nei2count[0]
                             first_nei_degree = sub_graph.degree[first_nei]
-                            if first_nei_count >= self.config.high_freq_thre:
+                            # if first_nei_count >= self.config.high_freq_thre:
+                            if first_nei_count > self.config.high_freq_thre:
                                 line = [first_nei, first_nei_count, first_nei_degree, node, node_count, node_degree]
                                 if edit_dis == 1:
                                     newline = self.err_type_classification(line)
                                     # gen_df.loc[len(gen_df)] = newline
                                     gen_lst.append(newline)
                                     del line, newline  
                                 else:
                                     # gen_df.loc[len(gen_df)] = line 
                                     gen_lst.append(line)
                                     del line
                         else:
                             # ambiguous errors
                             tmp_lst = []
                             for cre_nei, cur_nei_count in nei2count:
-                                if cur_nei_count >= self.config.high_freq_thre:
+                                # if cur_nei_count >= self.config.high_freq_thre:
+                                if cur_nei_count > self.config.high_freq_thre:
                                     cur_nei_degree = sub_graph.degree[nei]
                                     line = [cre_nei, cur_nei_count, cur_nei_degree, node, node_count, node_degree]
                                     if edit_dis == 1:
                                         newline = self.err_type_classification(line)
                                     else:
                                         newline = line
                                     # newline.insert(0, idx)
@@ -464,15 +469,15 @@
         if edit_dis == 1:
             negative_csv = self.config.result_dir + "negative1.csv"
         elif edit_dis == 2:   
             negative_csv = self.config.result_dir + "negative2.csv"  
         negative_df = pd.DataFrame(columns=["StartRead","StartReadCount", "StartDegree"])
         for k in isolates:
             k_count = graph.nodes[k]['count']
-            if k_count >= self.config.high_freq_thre:
+            if k_count > self.config.high_freq_thre:
                 k_degree = graph.degree[k]
                 line = [k, k_count, k_degree]
                 negative_df.loc[len(negative_df)] = line  
         if self.config.verbose:
             negative_df.to_csv(negative_csv, index=False) 
         self.logger.info("Done!")
         return negative_df
@@ -559,15 +564,16 @@
         read_count = Counter(total_seqs)
         high_freq = []
         low_freq = []
 
         for read, frequency in tqdm(read_count.items(), desc=self.logger.info("Adding nodes to " + str(edit_dis) + "nt-edit-distance read graph..."), miniters=int(len(read_count)/self.config.min_iters)):
             if not graph.has_node(read):
                 graph.add_node(read, count = frequency, flag=False)  
-            if frequency >= self.config.high_freq_thre:
+            # if frequency >= self.config.high_freq_thre:
+            if frequency > self.config.high_freq_thre:
                 high_freq.append(read)
             else:
                 low_freq.append(read)
         if len(high_freq) == 0:
             self.logger.error("Error Correction Failed as no high-frequency reads detected.")
             sys.exit(1)
         self.logger.debug(len(read_count))
@@ -778,15 +784,16 @@
             edges_lst = [e for e in s.edges()]
             if len(edges_lst) > 0:
                 for (a, b) in edges_lst:
                     a_count = s.nodes[a]['count']
                     b_count = s.nodes[b]['count']
                     a_degree = s.degree[a]
                     b_degree = s.degree[b]
-                    if a_count > self.config.high_freq_thre and b_count > self.config.high_freq_thre:
+                    if a_count > self.config.high_freq_thre and b_count > self.config.high_freq_thre: 
+                    # if a_count >= self.config.high_freq_thre and b_count >= self.config.high_freq_thre: # comment this line on 13 May 2023
                         a2b = [a, a_count, a_degree, b, b_count, b_degree]
                         new_a2b = self.err_type_classification(a2b) 
                         new_a2b.insert(0, idx)     
                         high_ambiguous_df.loc[len(high_ambiguous_df)] = new_a2b 
                         b2a = [b, b_count, b_degree, a, a_count, a_degree]
                         new_b2a = self.err_type_classification(b2a)
                         new_b2a.insert(0, idx)
```

### Comparing `noise2read-0.0.75/src/noise2read/data_preprocessing.py` & `noise2read-0.0.76/src/noise2read/data_preprocessing.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/encoding.py` & `noise2read-0.0.76/src/noise2read/encoding.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/error_orrection.py` & `noise2read-0.0.76/src/noise2read/error_orrection.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/isolates_correction.py` & `noise2read-0.0.76/src/noise2read/isolates_correction.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/noise2read.py` & `noise2read-0.0.76/src/noise2read/noise2read.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/reads2vectors.py` & `noise2read-0.0.76/src/noise2read/reads2vectors.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/simulation.py` & `noise2read-0.0.76/src/noise2read/simulation.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/umitest.py` & `noise2read-0.0.76/src/noise2read/umitest.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read/utils.py` & `noise2read-0.0.76/src/noise2read/utils.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/src/noise2read.egg-info/SOURCES.txt` & `noise2read-0.0.76/src/noise2read.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/tests/test_data_generation.py` & `noise2read-0.0.76/tests/test_data_generation.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/tests/test_reads2vector.py` & `noise2read-0.0.76/tests/test_reads2vector.py`

 * *Files identical despite different names*

### Comparing `noise2read-0.0.75/tests/test_utils.py` & `noise2read-0.0.76/tests/test_utils.py`

 * *Files identical despite different names*

