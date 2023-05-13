# Comparing `tmp/efficiency-1.2.1.tar.gz` & `tmp/efficiency-1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "efficiency-1.2.1.tar", last modified: Fri Apr 28 16:20:32 2023, max compression
+gzip compressed data, was "efficiency-1.3.tar", last modified: Sat May 13 10:25:54 2023, max compression
```

## Comparing `efficiency-1.2.1.tar` & `efficiency-1.3.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxr-xr-x   0 zjin      (7600) is        (1040)        0 2023-04-28 16:20:32.797467 efficiency-1.2.1/
--rw-r--r--   0 zjin      (7600) is        (1040)     1079 2023-04-28 16:20:12.000000 efficiency-1.2.1/LICENSE.txt
--rw-r--r--   0 zjin      (7600) is        (1040)     1864 2023-04-28 16:20:32.797467 efficiency-1.2.1/PKG-INFO
--rw-r--r--   0 zjin      (7600) is        (1040)     1612 2023-04-28 16:20:12.000000 efficiency-1.2.1/README.md
-drwxr-xr-x   0 zjin      (7600) is        (1040)        0 2023-04-28 16:20:32.797467 efficiency-1.2.1/efficiency/
--rw-r--r--   0 zjin      (7600) is        (1040)      201 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/__init__.py
--rw-r--r--   0 zjin      (7600) is        (1040)     6788 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/bib.py
--rw-r--r--   0 zjin      (7600) is        (1040)     1011 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/file_manager.py
--rw-r--r--   0 zjin      (7600) is        (1040)     6584 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/function.py
--rw-r--r--   0 zjin      (7600) is        (1040)    12306 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/log.py
-drwxr-xr-x   0 zjin      (7600) is        (1040)        0 2023-04-28 16:20:32.797467 efficiency-1.2.1/efficiency/mt/
--rw-r--r--   0 zjin      (7600) is        (1040)       55 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/mt/__init__.py
--rw-r--r--   0 zjin      (7600) is        (1040)     5695 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/mt/loss_plot.py
--rw-r--r--   0 zjin      (7600) is        (1040)     5695 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/mt/tensorboard_logging.py
--rw-r--r--   0 zjin      (7600) is        (1040)     8364 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/nlp.py
--rw-r--r--   0 zjin      (7600) is        (1040)     9206 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/plotter.py
--rw-r--r--   0 zjin      (7600) is        (1040)      520 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/record.py
--rw-r--r--   0 zjin      (7600) is        (1040)    11694 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/text.py
--rw-r--r--   0 zjin      (7600) is        (1040)      573 2023-04-28 16:20:12.000000 efficiency-1.2.1/efficiency/web.py
-drwxr-xr-x   0 zjin      (7600) is        (1040)        0 2023-04-28 16:20:32.797467 efficiency-1.2.1/efficiency.egg-info/
--rw-r--r--   0 zjin      (7600) is        (1040)     1864 2023-04-28 16:20:32.000000 efficiency-1.2.1/efficiency.egg-info/PKG-INFO
--rw-r--r--   0 zjin      (7600) is        (1040)      506 2023-04-28 16:20:32.000000 efficiency-1.2.1/efficiency.egg-info/SOURCES.txt
--rw-r--r--   0 zjin      (7600) is        (1040)        1 2023-04-28 16:20:32.000000 efficiency-1.2.1/efficiency.egg-info/dependency_links.txt
--rw-r--r--   0 zjin      (7600) is        (1040)       24 2023-04-28 16:20:32.000000 efficiency-1.2.1/efficiency.egg-info/requires.txt
--rw-r--r--   0 zjin      (7600) is        (1040)       11 2023-04-28 16:20:32.000000 efficiency-1.2.1/efficiency.egg-info/top_level.txt
--rw-r--r--   0 zjin      (7600) is        (1040)       79 2023-04-28 16:20:32.797467 efficiency-1.2.1/setup.cfg
--rw-r--r--   0 zjin      (7600) is        (1040)      509 2023-04-28 16:20:12.000000 efficiency-1.2.1/setup.py
+drwxr-xr-x   0 zjin      (7600) is        (1040)        0 2023-05-13 10:25:54.817127 efficiency-1.3/
+-rw-r--r--   0 zjin      (7600) is        (1040)     1079 2023-05-13 10:23:38.000000 efficiency-1.3/LICENSE.txt
+-rw-r--r--   0 zjin      (7600) is        (1040)     1862 2023-05-13 10:25:54.817127 efficiency-1.3/PKG-INFO
+-rw-r--r--   0 zjin      (7600) is        (1040)     1612 2023-05-13 10:23:38.000000 efficiency-1.3/README.md
+drwxr-xr-x   0 zjin      (7600) is        (1040)        0 2023-05-13 10:25:54.817127 efficiency-1.3/efficiency/
+-rw-r--r--   0 zjin      (7600) is        (1040)      201 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/__init__.py
+-rw-r--r--   0 zjin      (7600) is        (1040)     6788 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/bib.py
+-rw-r--r--   0 zjin      (7600) is        (1040)     1011 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/file_manager.py
+-rw-r--r--   0 zjin      (7600) is        (1040)     7880 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/function.py
+-rw-r--r--   0 zjin      (7600) is        (1040)    13665 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/log.py
+drwxr-xr-x   0 zjin      (7600) is        (1040)        0 2023-05-13 10:25:54.817127 efficiency-1.3/efficiency/mt/
+-rw-r--r--   0 zjin      (7600) is        (1040)       55 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/mt/__init__.py
+-rw-r--r--   0 zjin      (7600) is        (1040)     5695 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/mt/loss_plot.py
+-rw-r--r--   0 zjin      (7600) is        (1040)     5695 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/mt/tensorboard_logging.py
+-rw-r--r--   0 zjin      (7600) is        (1040)    12536 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/nlp.py
+-rw-r--r--   0 zjin      (7600) is        (1040)     9206 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/plotter.py
+-rw-r--r--   0 zjin      (7600) is        (1040)      520 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/record.py
+-rw-r--r--   0 zjin      (7600) is        (1040)    11694 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/text.py
+-rw-r--r--   0 zjin      (7600) is        (1040)      573 2023-05-13 10:23:38.000000 efficiency-1.3/efficiency/web.py
+drwxr-xr-x   0 zjin      (7600) is        (1040)        0 2023-05-13 10:25:54.817127 efficiency-1.3/efficiency.egg-info/
+-rw-r--r--   0 zjin      (7600) is        (1040)     1862 2023-05-13 10:25:54.000000 efficiency-1.3/efficiency.egg-info/PKG-INFO
+-rw-r--r--   0 zjin      (7600) is        (1040)      506 2023-05-13 10:25:54.000000 efficiency-1.3/efficiency.egg-info/SOURCES.txt
+-rw-r--r--   0 zjin      (7600) is        (1040)        1 2023-05-13 10:25:54.000000 efficiency-1.3/efficiency.egg-info/dependency_links.txt
+-rw-r--r--   0 zjin      (7600) is        (1040)       13 2023-05-13 10:25:54.000000 efficiency-1.3/efficiency.egg-info/requires.txt
+-rw-r--r--   0 zjin      (7600) is        (1040)       11 2023-05-13 10:25:54.000000 efficiency-1.3/efficiency.egg-info/top_level.txt
+-rw-r--r--   0 zjin      (7600) is        (1040)       79 2023-05-13 10:25:54.821127 efficiency-1.3/setup.cfg
+-rw-r--r--   0 zjin      (7600) is        (1040)      490 2023-05-13 10:23:38.000000 efficiency-1.3/setup.py
```

### Comparing `efficiency-1.2.1/LICENSE.txt` & `efficiency-1.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/PKG-INFO` & `efficiency-1.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: efficiency
-Version: 1.2.1
+Version: 1.3
 Summary: A package for efficient programming
 Home-page: https://github.com/zhijing-jin/efficiency
 Author: Zhijing Jin
 License: MIT
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
```

### Comparing `efficiency-1.2.1/README.md` & `efficiency-1.3/README.md`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency/bib.py` & `efficiency-1.3/efficiency/bib.py`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency/file_manager.py` & `efficiency-1.3/efficiency/file_manager.py`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency/function.py` & `efficiency-1.3/efficiency/function.py`

 * *Files 17% similar despite different names*

```diff
@@ -20,15 +20,14 @@
         print("[stdout]", subp_stdout, "[end]")
     if stderr and subp_stderr:
         print("[stderr]", subp_stderr, "[end]")
 
     return subp_stdout, subp_stderr
 
 
-
 def mproc(func, input_list, avail_cpu=multiprocessing.cpu_count() - 4):
     '''
     This is a multiprocess function where you execute the function with 
     every input in the input_list simutaneously.
     @ return output_list: the list of outputs w.r.t. input_list
     '''
     from multiprocessing import Pool
@@ -74,17 +73,35 @@
     return list(chain.from_iterable(nested_list))
 
 
 def flatten_dict(dict_list):
     from collections import ChainMap
     return dict(ChainMap(*dict_list))
 
+
 def nested_list2tuple(t):
     return tuple(map(nested_list2tuple, t)) if isinstance(t, (tuple, list)) else t
 
+
+def search_nested_dict(nested_dict, target_key):
+    queue = [(nested_dict, key) for key in nested_dict]
+
+    while queue:
+        current_dict, key = queue.pop(0)
+
+        if key == target_key:
+            return current_dict[key]
+
+        if isinstance(current_dict[key], dict):
+            for sub_key in current_dict[key]:
+                queue.append((current_dict[key], sub_key))
+
+    return None
+
+
 def lstrip_word(word, pref):
     if word.startswith(pref):
         return word[len(pref):]
     return word
 
 
 def rstrip_word(word, suf):
@@ -115,14 +132,42 @@
         torch.manual_seed(seed)
         torch.cuda.manual_seed_all(seed)
         torch.backends.cudnn.deterministic = True
         torch.backends.cudnn.benchmark = False
     except ImportError:
         pass
 
+
+def get_set_f1(ground_truth_set, predicted_set, report_percentage=True):
+    true_positives = len(ground_truth_set.intersection(predicted_set))
+    false_positives = len(predicted_set.difference(ground_truth_set))
+    false_negatives = len(ground_truth_set.difference(predicted_set))
+
+    if true_positives == 0:
+        return 0
+    precision = true_positives / (true_positives + false_positives)
+    recall = true_positives / (true_positives + false_negatives)
+
+    f1 = 2 * (precision * recall) / (precision + recall)
+    if report_percentage:
+        f1 *= 100
+    return f1
+
+def get_set_edit_distance(set1, set2):
+    try:
+        import Levenshtein
+    except:
+        import os
+        os.system('pip install python-Levenshtein')
+        import Levenshtein
+
+    list1 = sorted(list(set1))
+    list2 = sorted(list(set2))
+    return Levenshtein.distance(str(list1), str(list2))
+
 def dict_diff(dict0, dict1, note=''):
     if isinstance(dict0, dict) and isinstance(dict1, dict):
         for [key0, val0], [key1, val1] in zip(sorted(dict0.items()),
                                               sorted(dict1.items())):
             if key0 != key1:
                 yield (key0, key1, note + ', key_is_diff')
             else:
@@ -134,26 +179,27 @@
                         (isinstance(val1, list) or isinstance(val1, tuple)):
                     for i in dict_diff(val0, val1, note + ', ' + key0):
                         for b in i:
                             yield b
                 else:
                     if val0 != val1:
                         yield (
-                        val0, val1, note + ', {}, val_is_diff'.format(key0))
+                            val0, val1, note + ', {}, val_is_diff'.format(key0))
 
     elif (isinstance(dict0, list) or isinstance(dict0, tuple)) and \
             (isinstance(dict1, list) or isinstance(dict1, tuple)):
         for ls_ix, (item0, item1) in enumerate(zip(dict0, dict1)):
             for i in dict_diff(item0, item1, note + ', {}'.format(ls_ix)):
                 for b in i:
                     yield b
     else:
         if dict0 != dict1:
             yield (dict0, dict1, note)
 
+
 def reorder(_x, order):
     x = list(range(len(_x)))
     for i, a in zip(order, _x):
         x[i] = a
     return x
```

### Comparing `efficiency-1.2.1/efficiency/log.py` & `efficiency-1.3/efficiency/log.py`

 * *Files 9% similar despite different names*

```diff
@@ -219,21 +219,21 @@
             print('[Info] Writing {} lines into {}'.format(length, path))
 
     with open(path, mode) as f:
         f.write(new_doc)
 
 
 def fread(path, if_strip=False, delete_empty=False, csv2list_or_dict='dict', encoding='utf-8', return_df=False,
-          verbose=True, if_empty_return=[]):
+          verbose=True, if_empty_return=[], calc_time=False):
     from efficiency.log import show_time
 
-    if verbose:
+    if calc_time:
         show_time('[Info] Starting to read file: ' + path)
     if not os.path.isfile(path):
-        print('[Warn] This file does not exist: ' + path)
+        if verbose: print('[Warn] This file does not exist: ' + path)
         return if_empty_return
 
     if path.endswith('.jsonl'):
         if verbose: print('[Info] Reading the file in jsonl format')
         import json
         with open(path) as f:
             data = []
@@ -250,15 +250,18 @@
     elif path.endswith('.json'):
         import json
         with open(path) as f:
             data = json.load(f)
 
     elif path.endswith('.csv'):
         import pandas as pd
-        data = pd.read_csv(path).to_dict(orient="records")
+        try:
+            data = pd.read_csv(path).to_dict(orient="records")
+        except:
+            return if_empty_return
 
         if False:
             # encoding="utf-8-sig" to ignore the \ufeff character
             import csv
             with open(path, encoding=encoding) as f:  # python 3: 'r',newline=""
                 dialect = csv.Sniffer().sniff(f.read(32), delimiters=";,")
                 f.seek(0)
@@ -304,36 +307,37 @@
     import csv
 
     if not len(data): return
 
     fieldnames = data[0].keys()
     lines = fread(file, verbose=False)
     existing = len(lines) >= 2
-    if existing:
-        fieldnames_existing = lines[0].keys()
-        if set(fieldnames) - set(fieldnames_existing):
-            print(f'[Warn] The existing csv columns ({fieldnames_existing}) are not compatible with the new csv '
-                  f'columns ({fieldnames}).')
-            import pdb;
-            pdb.set_trace()
-        fieldnames = fieldnames_existing
+    if mode == 'a':
+        if existing:
+            fieldnames_existing = lines[0].keys()
+            if set(fieldnames) - set(fieldnames_existing):
+                print(f'[Warn] The existing csv columns ({fieldnames_existing}) are not compatible with the new csv '
+                      f'columns ({fieldnames}).')
+                import pdb;
+                pdb.set_trace()
+            fieldnames = fieldnames_existing
     with open(file, mode=mode) as csv_file:
         writer = csv.DictWriter(csv_file, fieldnames=fieldnames)
-        if not existing: writer.writeheader()
+        if (mode == 'w') or (not existing): writer.writeheader()
         writer.writerows(data)
     '''
     df = pd.DataFrame(data_to_save)
     df.to_csv(output_file, index=False)
     '''
 
 
 def show_time(what_happens='', cat_server=False, printout=True):
     import datetime
 
-    disp = '⏰ Time: ' + \
+    disp = '🕙 Time: ' + \
            datetime.datetime.now().strftime('%m%d%H%M-%S')
     disp = disp + '\t' + what_happens if what_happens else disp
     if printout:
         try:
             print(disp)
         except:
             pass
@@ -365,20 +369,56 @@
         import git
 
     repo = git.Repo(search_parent_directories=True)
     sha = repo.head.object.hexsha
     return sha
 
 
+def verbalize_list_of_options(choices, connective=['and', 'or'][-1], add_comma_if_len=[2,3][-1],
+                              wrap_choices=['', '"'][-1]):
+
+    choices = [f'{wrap_choices}{i}{wrap_choices}' for i in choices]
+    if len(choices) > 1:
+        choices[-1] = f'{connective} ' + choices[-1]
+    if len(choices) < add_comma_if_len:
+        choices = ' '.join(choices)
+    else:
+        choices = ', '.join(choices)
+    return choices
+
+
 def del_quote(string):
     cleaned = string.replace("'", "")
     cleaned = cleaned.replace("\"", "")
     return cleaned
 
 
+def print_df_value_count(df, columns=None):
+    if columns is None: columns = df.columns
+    for column in columns:
+        print(f"Column {column}:")
+        print(df[column].value_counts(normalize=True) * 100)
+        print()
+
+
+def pivot_df(df, rows='query_type', columns='model_version'):
+    import pdb;pdb.set_trace()
+    pivot_df = df.pivot_table(index=rows, columns=columns, values='score', aggfunc='first')
+
+    pivot_df.reset_index(inplace=True)
+    pivot_df.fillna('---', inplace=True)
+    pivot_df.columns.name = None
+
+    desired_order = sorted(df[differ_by].unique().tolist())
+    pivot_df.set_index(rows, inplace=True)
+    pivot_df = pivot_df.reindex(desired_order)
+    pivot_df.reset_index(inplace=True)
+    return pivot_df
+
+
 def gpu_mem(gpu_id=0):
     from efficiency.function import shell
 
     line = 9 + gpu_id * 3
     cmd = "nvidia-smi | head -n {} | tail -n 1 | awk '{{print $9}}' | sed 's/MiB//' ".format(
         line)
```

### Comparing `efficiency-1.2.1/efficiency/mt/loss_plot.py` & `efficiency-1.3/efficiency/mt/loss_plot.py`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency/mt/tensorboard_logging.py` & `efficiency-1.3/efficiency/mt/tensorboard_logging.py`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency/plotter.py` & `efficiency-1.3/efficiency/plotter.py`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency/record.py` & `efficiency-1.3/efficiency/record.py`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency/text.py` & `efficiency-1.3/efficiency/text.py`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency/web.py` & `efficiency-1.3/efficiency/web.py`

 * *Files identical despite different names*

### Comparing `efficiency-1.2.1/efficiency.egg-info/PKG-INFO` & `efficiency-1.3/efficiency.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: efficiency
-Version: 1.2.1
+Version: 1.3
 Summary: A package for efficient programming
 Home-page: https://github.com/zhijing-jin/efficiency
 Author: Zhijing Jin
 License: MIT
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
```

