# Comparing `tmp/magicsoup-0.3.8.tar.gz` & `tmp/magicsoup-0.3.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "magicsoup-0.3.8.tar", last modified: Mon May  1 19:54:06 2023, max compression
+gzip compressed data, was "magicsoup-0.3.9.tar", last modified: Tue May  2 11:49:54 2023, max compression
```

## Comparing `magicsoup-0.3.8.tar` & `magicsoup-0.3.9.tar`

### file list

```diff
@@ -1,32 +1,33 @@
-drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-01 19:54:06.189160 magicsoup-0.3.8/
--rw-rw-r--   0 marc      (1000) marc      (1003)    34888 2023-01-23 15:27:37.000000 magicsoup-0.3.8/LICENSE
--rw-rw-r--   0 marc      (1000) marc      (1003)     5297 2023-05-01 19:54:06.189160 magicsoup-0.3.8/PKG-INFO
--rw-rw-r--   0 marc      (1000) marc      (1003)     4360 2023-04-07 09:06:36.000000 magicsoup-0.3.8/README.md
--rw-rw-r--   0 marc      (1000) marc      (1003)     1092 2023-01-26 15:22:43.000000 magicsoup-0.3.8/pyproject.toml
--rw-rw-r--   0 marc      (1000) marc      (1003)       38 2023-05-01 19:54:06.189160 magicsoup-0.3.8/setup.cfg
-drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-01 19:54:06.189160 magicsoup-0.3.8/src/
-drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-01 19:54:06.189160 magicsoup-0.3.8/src/magicsoup/
--rw-rw-r--   0 marc      (1000) marc      (1003)      119 2023-05-01 19:53:50.000000 magicsoup-0.3.8/src/magicsoup/__init__.py
--rw-rw-r--   0 marc      (1000) marc      (1003)     1109 2023-04-27 20:14:44.000000 magicsoup-0.3.8/src/magicsoup/constants.py
--rw-rw-r--   0 marc      (1000) marc      (1003)    23599 2023-04-27 20:14:11.000000 magicsoup-0.3.8/src/magicsoup/containers.py
-drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-01 19:54:06.189160 magicsoup-0.3.8/src/magicsoup/examples/
--rw-rw-r--   0 marc      (1000) marc      (1003)        0 2023-01-23 15:27:37.000000 magicsoup-0.3.8/src/magicsoup/examples/__init__.py
--rw-rw-r--   0 marc      (1000) marc      (1003)      833 2023-01-23 15:27:37.000000 magicsoup-0.3.8/src/magicsoup/examples/n2_fixing.py
--rw-rw-r--   0 marc      (1000) marc      (1003)     1473 2023-01-23 15:27:37.000000 magicsoup-0.3.8/src/magicsoup/examples/reverse_krebs.py
--rw-rw-r--   0 marc      (1000) marc      (1003)     1930 2023-02-16 21:19:27.000000 magicsoup-0.3.8/src/magicsoup/examples/wood_ljungdahl.py
--rw-rw-r--   0 marc      (1000) marc      (1003)    12180 2023-04-27 20:14:54.000000 magicsoup-0.3.8/src/magicsoup/genetics.py
--rw-rw-r--   0 marc      (1000) marc      (1003)    30687 2023-04-27 20:15:08.000000 magicsoup-0.3.8/src/magicsoup/kinetics.py
--rw-rw-r--   0 marc      (1000) marc      (1003)     4143 2023-04-27 20:15:25.000000 magicsoup-0.3.8/src/magicsoup/mutations.py
--rw-rw-r--   0 marc      (1000) marc      (1003)     5288 2023-04-07 13:25:00.000000 magicsoup-0.3.8/src/magicsoup/util.py
--rw-rw-r--   0 marc      (1000) marc      (1003)    42942 2023-05-01 19:50:00.000000 magicsoup-0.3.8/src/magicsoup/world.py
-drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-01 19:54:06.189160 magicsoup-0.3.8/src/magicsoup.egg-info/
--rw-rw-r--   0 marc      (1000) marc      (1003)     5297 2023-05-01 19:54:06.000000 magicsoup-0.3.8/src/magicsoup.egg-info/PKG-INFO
--rw-rw-r--   0 marc      (1000) marc      (1003)      647 2023-05-01 19:54:06.000000 magicsoup-0.3.8/src/magicsoup.egg-info/SOURCES.txt
--rw-rw-r--   0 marc      (1000) marc      (1003)        1 2023-05-01 19:54:06.000000 magicsoup-0.3.8/src/magicsoup.egg-info/dependency_links.txt
--rw-rw-r--   0 marc      (1000) marc      (1003)       10 2023-05-01 19:54:06.000000 magicsoup-0.3.8/src/magicsoup.egg-info/top_level.txt
-drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-01 19:54:06.189160 magicsoup-0.3.8/tests/
--rw-rw-r--   0 marc      (1000) marc      (1003)      710 2023-02-09 10:42:28.000000 magicsoup-0.3.8/tests/test_containers.py
--rw-rw-r--   0 marc      (1000) marc      (1003)     6012 2023-04-06 09:44:07.000000 magicsoup-0.3.8/tests/test_genetics.py
--rw-rw-r--   0 marc      (1000) marc      (1003)    46871 2023-04-27 20:17:09.000000 magicsoup-0.3.8/tests/test_kinetics.py
--rw-rw-r--   0 marc      (1000) marc      (1003)     1433 2023-04-03 15:10:20.000000 magicsoup-0.3.8/tests/test_util.py
--rw-rw-r--   0 marc      (1000) marc      (1003)    19437 2023-05-01 19:52:39.000000 magicsoup-0.3.8/tests/test_world.py
+drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-02 11:49:54.675226 magicsoup-0.3.9/
+-rw-rw-r--   0 marc      (1000) marc      (1003)    34888 2023-01-23 15:27:37.000000 magicsoup-0.3.9/LICENSE
+-rw-rw-r--   0 marc      (1000) marc      (1003)     5297 2023-05-02 11:49:54.675226 magicsoup-0.3.9/PKG-INFO
+-rw-rw-r--   0 marc      (1000) marc      (1003)     4360 2023-04-07 09:06:36.000000 magicsoup-0.3.9/README.md
+-rw-rw-r--   0 marc      (1000) marc      (1003)     1092 2023-01-26 15:22:43.000000 magicsoup-0.3.9/pyproject.toml
+-rw-rw-r--   0 marc      (1000) marc      (1003)       38 2023-05-02 11:49:54.675226 magicsoup-0.3.9/setup.cfg
+drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-02 11:49:54.675226 magicsoup-0.3.9/src/
+drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-02 11:49:54.675226 magicsoup-0.3.9/src/magicsoup/
+-rw-rw-r--   0 marc      (1000) marc      (1003)      119 2023-05-02 11:49:42.000000 magicsoup-0.3.9/src/magicsoup/__init__.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)     1109 2023-04-27 20:14:44.000000 magicsoup-0.3.9/src/magicsoup/constants.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)    23599 2023-04-27 20:14:11.000000 magicsoup-0.3.9/src/magicsoup/containers.py
+drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-02 11:49:54.675226 magicsoup-0.3.9/src/magicsoup/examples/
+-rw-rw-r--   0 marc      (1000) marc      (1003)        0 2023-01-23 15:27:37.000000 magicsoup-0.3.9/src/magicsoup/examples/__init__.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)      833 2023-01-23 15:27:37.000000 magicsoup-0.3.9/src/magicsoup/examples/n2_fixing.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)     1473 2023-01-23 15:27:37.000000 magicsoup-0.3.9/src/magicsoup/examples/reverse_krebs.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)     1930 2023-02-16 21:19:27.000000 magicsoup-0.3.9/src/magicsoup/examples/wood_ljungdahl.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)    12180 2023-04-27 20:14:54.000000 magicsoup-0.3.9/src/magicsoup/genetics.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)    30687 2023-04-27 20:15:08.000000 magicsoup-0.3.9/src/magicsoup/kinetics.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)     4143 2023-05-01 20:15:52.000000 magicsoup-0.3.9/src/magicsoup/mutations.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)     5288 2023-04-07 13:25:00.000000 magicsoup-0.3.9/src/magicsoup/util.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)    42969 2023-05-02 11:48:17.000000 magicsoup-0.3.9/src/magicsoup/world.py
+drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-02 11:49:54.675226 magicsoup-0.3.9/src/magicsoup.egg-info/
+-rw-rw-r--   0 marc      (1000) marc      (1003)     5297 2023-05-02 11:49:54.000000 magicsoup-0.3.9/src/magicsoup.egg-info/PKG-INFO
+-rw-rw-r--   0 marc      (1000) marc      (1003)      671 2023-05-02 11:49:54.000000 magicsoup-0.3.9/src/magicsoup.egg-info/SOURCES.txt
+-rw-rw-r--   0 marc      (1000) marc      (1003)        1 2023-05-02 11:49:54.000000 magicsoup-0.3.9/src/magicsoup.egg-info/dependency_links.txt
+-rw-rw-r--   0 marc      (1000) marc      (1003)       10 2023-05-02 11:49:54.000000 magicsoup-0.3.9/src/magicsoup.egg-info/top_level.txt
+drwxrwxr-x   0 marc      (1000) marc      (1003)        0 2023-05-02 11:49:54.675226 magicsoup-0.3.9/tests/
+-rw-rw-r--   0 marc      (1000) marc      (1003)      710 2023-02-09 10:42:28.000000 magicsoup-0.3.9/tests/test_containers.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)     6012 2023-04-06 09:44:07.000000 magicsoup-0.3.9/tests/test_genetics.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)    46871 2023-04-27 20:17:09.000000 magicsoup-0.3.9/tests/test_kinetics.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)     1041 2023-05-01 20:29:24.000000 magicsoup-0.3.9/tests/test_mutations.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)     1433 2023-04-03 15:10:20.000000 magicsoup-0.3.9/tests/test_util.py
+-rw-rw-r--   0 marc      (1000) marc      (1003)    19437 2023-05-01 19:52:39.000000 magicsoup-0.3.9/tests/test_world.py
```

### Comparing `magicsoup-0.3.8/LICENSE` & `magicsoup-0.3.9/LICENSE`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/PKG-INFO` & `magicsoup-0.3.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: magicsoup
-Version: 0.3.8
+Version: 0.3.9
 Summary: Simulation for cell metabolic and transduction pathway evolution
 Author-email: Marc <schweringmarc01@gmail.com>
 Project-URL: Documentation, https://magic-soup.readthedocs.io/
 Project-URL: Homepage, https://github.com/mRcSchwering/magic-soup
 Project-URL: Bug Tracker, https://github.com/mRcSchwering/magic-soup/issues
 Classifier: Environment :: Console
 Classifier: Environment :: GPU
```

### Comparing `magicsoup-0.3.8/README.md` & `magicsoup-0.3.9/README.md`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/pyproject.toml` & `magicsoup-0.3.9/pyproject.toml`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/constants.py` & `magicsoup-0.3.9/src/magicsoup/constants.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/containers.py` & `magicsoup-0.3.9/src/magicsoup/containers.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/examples/n2_fixing.py` & `magicsoup-0.3.9/src/magicsoup/examples/n2_fixing.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/examples/reverse_krebs.py` & `magicsoup-0.3.9/src/magicsoup/examples/reverse_krebs.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/examples/wood_ljungdahl.py` & `magicsoup-0.3.9/src/magicsoup/examples/wood_ljungdahl.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/genetics.py` & `magicsoup-0.3.9/src/magicsoup/genetics.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/kinetics.py` & `magicsoup-0.3.9/src/magicsoup/kinetics.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/mutations.py` & `magicsoup-0.3.9/src/magicsoup/mutations.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/util.py` & `magicsoup-0.3.9/src/magicsoup/util.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/src/magicsoup/world.py` & `magicsoup-0.3.9/src/magicsoup/world.py`

 * *Files 0% similar despite different names*

```diff
@@ -814,19 +814,20 @@
             statedir / "cell_divisions.pt", map_location=self.device
         ).int()
 
         with open(statedir / "cells.fasta", "r", encoding="utf-8") as fh:
             text: str = fh.read()
             entries = [d.strip() for d in text.split(">") if len(d.strip()) > 0]
 
+        self.labels = []
+        self.genomes = []
         genome_idx_pairs: list[tuple[str, int]] = []
-        for entry in entries:
+        for idx, entry in enumerate(entries):
             descr, seq = entry.split("\n")
             names = descr.split()
-            idx = int(names[0].strip())
             label = names[1].strip() if len(names) > 1 else ""
             self.genomes.append(seq)
             self.labels.append(label)
             genome_idx_pairs.append((seq, idx))
 
         self.n_cells = len(genome_idx_pairs)
```

### Comparing `magicsoup-0.3.8/src/magicsoup.egg-info/PKG-INFO` & `magicsoup-0.3.9/src/magicsoup.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: magicsoup
-Version: 0.3.8
+Version: 0.3.9
 Summary: Simulation for cell metabolic and transduction pathway evolution
 Author-email: Marc <schweringmarc01@gmail.com>
 Project-URL: Documentation, https://magic-soup.readthedocs.io/
 Project-URL: Homepage, https://github.com/mRcSchwering/magic-soup
 Project-URL: Bug Tracker, https://github.com/mRcSchwering/magic-soup/issues
 Classifier: Environment :: Console
 Classifier: Environment :: GPU
```

### Comparing `magicsoup-0.3.8/src/magicsoup.egg-info/SOURCES.txt` & `magicsoup-0.3.9/src/magicsoup.egg-info/SOURCES.txt`

 * *Files 3% similar despite different names*

```diff
@@ -16,9 +16,10 @@
 src/magicsoup/examples/__init__.py
 src/magicsoup/examples/n2_fixing.py
 src/magicsoup/examples/reverse_krebs.py
 src/magicsoup/examples/wood_ljungdahl.py
 tests/test_containers.py
 tests/test_genetics.py
 tests/test_kinetics.py
+tests/test_mutations.py
 tests/test_util.py
 tests/test_world.py
```

### Comparing `magicsoup-0.3.8/tests/test_containers.py` & `magicsoup-0.3.9/tests/test_containers.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/tests/test_genetics.py` & `magicsoup-0.3.9/tests/test_genetics.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/tests/test_kinetics.py` & `magicsoup-0.3.9/tests/test_kinetics.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/tests/test_util.py` & `magicsoup-0.3.9/tests/test_util.py`

 * *Files identical despite different names*

### Comparing `magicsoup-0.3.8/tests/test_world.py` & `magicsoup-0.3.9/tests/test_world.py`

 * *Files identical despite different names*

