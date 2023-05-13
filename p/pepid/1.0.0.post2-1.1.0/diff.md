# Comparing `tmp/pepid-1.0.0.post2.tar.gz` & `tmp/pepid-1.1.0.tar.gz`

## Comparing `pepid-1.0.0.post2.tar` & `pepid-1.1.0.tar`

### file list

```diff
@@ -1,38 +1,45 @@
--rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/__init__.py
--rw-r--r--   0        0        0     9069 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/blackboard.py
--rw-r--r--   0        0        0    12843 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/db.py
--rw-r--r--   0        0        0     1615 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/db_node.py
--rw-r--r--   0        0        0    17716 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/gen_fdr_report.py
--rw-r--r--   0        0        0     2794 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/main.py
--rw-r--r--   0        0        0      430 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/my_script.py
--rw-r--r--   0        0        0     2832 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/node.py
--rw-r--r--   0        0        0     1183 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/output_node.py
--rw-r--r--   0        0        0      917 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_compare.py
--rw-r--r--   0        0        0     2885 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_files.py
--rw-r--r--   0        0        0     4864 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_io.py
--rw-r--r--   0        0        0     7321 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_mp.py
--rw-r--r--   0        0        0    11017 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_percolator.py
--rw-r--r--   0        0        0     4545 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_randomforest.py
--rw-r--r--   0        0        0      984 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_rescore.py
--rw-r--r--   0        0        0    10625 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_search.py
--rw-r--r--   0        0        0     4359 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pepid_utils.py
--rw-r--r--   0        0        0     1201 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/pin_node.py
--rw-r--r--   0        0        0     5062 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/queries.py
--rw-r--r--   0        0        0     1585 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/queries_node.py
--rw-r--r--   0        0        0    24611 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/search.py
--rw-r--r--   0        0        0     1152 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/search_node.py
--rw-r--r--   0        0        0     7985 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/data/default.cfg
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/__init__.py
--rw-r--r--   0        0        0     3538 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/psmatcher_v2.py
--rw-r--r--   0        0        0     3612 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/spectrum_generator_multi_sparse.py
--rw-r--r--   0        0        0     3457 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/spectrum_generator_sparse.py
--rw-r--r--   0        0        0     3570 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/test_model_multi_sparse.py
--rw-r--r--   0        0        0     3440 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/test_model_sparse.py
--rw-r--r--   0        0        0     9336 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/train_model_multi_sparse.py
--rw-r--r--   0        0        0     7405 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/train_model_sparse.py
--rw-r--r--   0        0        0     8093 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pepid/ml/train_psmatcher.py
--rw-r--r--   0        0        0       82 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/.gitignore
--rw-r--r--   0        0        0     1090 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/LICENSE.md
--rw-r--r--   0        0        0     7970 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/README.md
--rw-r--r--   0        0        0     1557 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/pyproject.toml
--rw-r--r--   0        0        0     8748 2020-02-02 00:00:00.000000 pepid-1.0.0.post2/PKG-INFO
+-rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/__init__.py
+-rw-r--r--   0        0        0       50 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/__main__.py
+-rw-r--r--   0        0        0     9453 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/blackboard.py
+-rw-r--r--   0        0        0    12846 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/db.py
+-rw-r--r--   0        0        0     1615 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/db_node.py
+-rw-r--r--   0        0        0     2614 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/drop_columns.py
+-rw-r--r--   0        0        0     1785 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/drop_node.py
+-rw-r--r--   0        0        0     6879 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/example_proteometools.cfg
+-rw-r--r--   0        0        0     7470 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/example_proteometools_ml.cfg
+-rw-r--r--   0        0        0     6788 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/example_yeast.cfg
+-rw-r--r--   0        0        0     8198 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/extensions.py
+-rw-r--r--   0        0        0     9943 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/finetune_rf_rescorer.py
+-rw-r--r--   0        0        0    20150 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/gen_fdp_report.py
+-rw-r--r--   0        0        0     6253 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/gen_fdp_report_debug.py
+-rw-r--r--   0        0        0    18182 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/gen_fdr_report.py
+-rw-r--r--   0        0        0     3960 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/main.py
+-rw-r--r--   0        0        0     2832 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/node.py
+-rw-r--r--   0        0        0     1183 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/output_node.py
+-rw-r--r--   0        0        0     1012 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_compare.py
+-rw-r--r--   0        0        0     2885 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_files.py
+-rw-r--r--   0        0        0     5131 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_io.py
+-rw-r--r--   0        0        0     2934 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_mgf_meta.py
+-rw-r--r--   0        0        0     7321 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_mp.py
+-rw-r--r--   0        0        0     5455 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_percolator.py
+-rw-r--r--   0        0        0     1587 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_postprocess.py
+-rw-r--r--   0        0        0     4545 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_randomforest.py
+-rw-r--r--   0        0        0      966 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_rescore.py
+-rw-r--r--   0        0        0     9536 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_search.py
+-rw-r--r--   0        0        0     8549 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pepid_utils.py
+-rw-r--r--   0        0        0     2422 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/pin_node.py
+-rw-r--r--   0        0        0     1443 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/post_node.py
+-rw-r--r--   0        0        0     4963 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/queries.py
+-rw-r--r--   0        0        0     1585 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/queries_node.py
+-rw-r--r--   0        0        0    24915 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/search.py
+-rw-r--r--   0        0        0     1152 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/search_node.py
+-rw-r--r--   0        0        0     5326 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/test_model.py
+-rw-r--r--   0        0        0     9829 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/train_rf_rescorer.py
+-rw-r--r--   0        0        0     8211 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/data/default.cfg
+-rw-r--r--   0        0        0     8142 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/ml/best_lgt_model.py
+-rw-r--r--   0        0        0     7109 2020-02-02 00:00:00.000000 pepid-1.1.0/pepid/ml/train_best_lgt_model.py
+-rw-r--r--   0        0        0       82 2020-02-02 00:00:00.000000 pepid-1.1.0/.gitignore
+-rw-r--r--   0        0        0     1090 2020-02-02 00:00:00.000000 pepid-1.1.0/LICENSE.md
+-rw-r--r--   0        0        0     9108 2020-02-02 00:00:00.000000 pepid-1.1.0/README.md
+-rw-r--r--   0        0        0     1582 2020-02-02 00:00:00.000000 pepid-1.1.0/pyproject.toml
+-rw-r--r--   0        0        0     9880 2020-02-02 00:00:00.000000 pepid-1.1.0/PKG-INFO
```

### Comparing `pepid-1.0.0.post2/pepid/blackboard.py` & `pepid-1.1.0/pepid/blackboard.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,26 +1,32 @@
 import configparser
 import os
 import sqlite3
 import time
 import uuid
+import msgpack
 import pickle
 import sys
 import fcntl
 
 import logging
 
 import subprocess as sp
 
 LOG = None
 CONN = None
 RES_CONN = None
 META_CONN = None
 LOCK = None
 
+def pin_template():
+    return ["PSMId", "Label", "ScanNr" ,"expMass", "calcMass", "FEATURES", "Peptide", "Proteins"]
+
+FEATS_BLACKLIST = set(["seq", "modseq", "title", "desc", "decoy", "file"]) # Set of keys generated by our default scoring functions to ignore during pin generation XXX needs cleanup/generalization
+
 config = configparser.ConfigParser(inline_comment_prefixes="#")
 
 DB_TYPES = None
 RES_TYPES = None
 META_TYPES = None
 QUERY_TYPES = None
 DB_COLS = None
@@ -153,28 +159,28 @@
     global TMP_PATH
 
     global LOG
 
     RES_COLS = ["title", "desc", "seq", "modseq", "score", "query_charge", "query_mass", "cand_mass", "candrow", "qrow", "file", "rrow"]
     RES_TYPES = ["TEXT", "TEXT", "TEXT", "BLOB", "REAL", "INTEGER", "REAL", "REAL", "INTEGER", "INTEGER", "TEXT", "INTEGER"]
 
-    META_COLS = ["qrow", "candrow", "data", "score", "rrow"] # score is used to mirror insertion exclusion via CHECK(score > 0) from the 'data' db
-    META_TYPES = ["INTEGER", "INTEGER", "TEXT", "REAL", "INTEGER"]
+    META_COLS = ["qrow", "candrow", "data", "extra", "score", "rrow"] # score is used to mirror insertion exclusion via CHECK(score > 0) from the 'data' db
+    META_TYPES = ["INTEGER", "INTEGER", "BLOB", "BLOB", "REAL", "INTEGER"]
 
     DB_COLS = ["desc", "decoy", "rt", "length", "mass", "seq", "mods", "spec", "meta"]
     DB_TYPES = ["TEXT", "INTEGER", "REAL", "INTEGER", "REAL", "TEXT", "AUTOBLOB", "SPECTRUM", "META"]
 
     QUERY_COLS = ["title", "rt", "charge", "mass", "spec", "min_mass", "max_mass", "meta"]
     QUERY_TYPES = ["TEXT", "REAL", "INTEGER", "REAL", "SPECTRUM", "REAL", "REAL", "META"]
 
     sqlite3.register_adapter(Spectrum, lambda x: pickle.dumps(x.data))
-    sqlite3.register_adapter(Meta, lambda x: pickle.dumps(x.data))
+    sqlite3.register_adapter(Meta, lambda x: msgpack.dumps(x.data))
     sqlite3.register_converter("spectrum", lambda x: Spectrum(pickle.loads(x)))
-    sqlite3.register_converter("meta", lambda x: Meta(pickle.loads(x)))
-    sqlite3.register_converter("autoblob", lambda x: pickle.loads(x))
+    sqlite3.register_converter("meta", lambda x: Meta(msgpack.loads(x)))
+    sqlite3.register_converter("autoblob", lambda x: msgpack.loads(x))
 
     DB_FNAME = list(filter(lambda x: len(x) > 0, config['data']['database'].split('/')))[-1].rsplit('.', 1)[0]
     RES_DB_FNAME = DB_FNAME + ".sqlite"
     META_DB_FNAME = DB_FNAME + "_meta.sqlite"
 
     workdir = config['data']['workdir']
     try:
@@ -187,17 +193,18 @@
 
     DB_PATH = os.path.join(TMP_PATH, DB_FNAME)
     RES_DB_PATH = DB_PATH + ".sqlite"
     META_DB_PATH = DB_PATH + "_meta.sqlite"
 
     handler = logging.StreamHandler()
     handler.setFormatter(logging.Formatter("[%(asctime)s] %(levelname)s: %(message)s"))
-    LOG = logging.getLogger("pepid")
-    LOG.setLevel(config['logging']['level'].upper())
-    LOG.addHandler(handler)
+    if LOG is None:
+        LOG = logging.getLogger("pepid")
+        LOG.setLevel(config['logging']['level'].upper())
+        LOG.addHandler(handler)
 
 def prepare_connection():
     global CONN
     global RES_CONN
     CONN = None
     _CONN = None
     while CONN is None:
```

### Comparing `pepid-1.0.0.post2/pepid/db.py` & `pepid-1.1.0/pepid/db.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import re
 from os import path
 import math
 import time
 import os
 import random
 import copy
-import pickle
+import msgpack
 
 if __package__ is None or __package__ == '':
     import blackboard
     import pepid_utils
 else:
     from . import blackboard
     from . import pepid_utils
@@ -167,15 +167,15 @@
     
     for i in range(len(data)):
         data[i]['spec'] = specs[i]
         data[i]['rt'] = rts[i]
     ret = user_fn(data)
     #rowids = list(range(start+1, end+1))
     for r in ret:
-        r['mods'] = pickle.dumps(r['mods'])
+        r['mods'] = msgpack.dumps(r['mods'])
 
     #blackboard.executemany(cur, "UPDATE candidates SET rt = ?, spec = ? WHERE rowid = ?;", list(zip(rts, specs, rowids)))
     blackboard.executemany(cur, "REPLACE INTO candidates ({}) VALUES ({});".format(",".join(blackboard.DB_COLS), ",".join(list(map(lambda x: ":" + x, blackboard.DB_COLS)))), ret)
     blackboard.commit()
 
 def process_entry(description, buff, settings):
     return process_entry_core(description, buff, settings, 'normal')
@@ -253,15 +253,15 @@
                                 if aa == mod and m == 0:
                                     var_list.append((curr_nmods+1, curr_mods[:iaa] + [sum(settings.var_mods[mod])] + curr_mods[iaa+1:]))
                   
             var_set = set(map(lambda x: tuple(x[1]), var_list)) # can't use lists in sets......
             for var in var_set:
                 mass = pepid_utils.theoretical_mass(peps[j], var, settings.nterm, settings.cterm)
                 if settings.min_mass <= mass <= settings.max_mass:
-                    data.append({"desc": description.split(" ", 1)[0], "decoy": seq_type == "decoy", "seq": peps[j], "mods": pickle.dumps(var), "rt": 0.0, "length": len(peps[j]), "mass": mass, "spec": blackboard.Spectrum(None), 'meta': blackboard.Meta(None)})
+                    data.append({"desc": description.split(" ", 1)[0], "decoy": seq_type == "decoy", "seq": peps[j], "mods": msgpack.dumps(var), "rt": 0.0, "length": len(peps[j]), "mass": mass, "spec": blackboard.Spectrum(None), 'meta': blackboard.Meta(None)})
     return data
 
 def fill_db(start, end, seq_type):
     """
     Processes database entries, performing digestion and generating variable mods as needed.
     Also applies config-specified mass and length filtering.
     Data is inserted in the temporary database.
```

### Comparing `pepid-1.0.0.post2/pepid/db_node.py` & `pepid-1.1.0/pepid/db_node.py`

 * *Files identical despite different names*

### Comparing `pepid-1.0.0.post2/pepid/gen_fdr_report.py` & `pepid-1.1.0/pepid/gen_fdr_report.py`

 * *Files 16% similar despite different names*

```diff
@@ -2,16 +2,18 @@
 import sys
 import os
 import tqdm
 import math
 
 if __package__ is None or __package__ == '':
     import blackboard
+    import pepid_utils
 else:
     from . import blackboard
+    from . import pepid_utils
 
 def tda_fdr(rescored=False):
     fname, fext = blackboard.config['data']['output'].rsplit(".", 1)
     full_fname = (fname + "." + fext) if not rescored else (fname + blackboard.config['rescoring']['suffix'] + "." + fext)
     decoy_prefix = blackboard.config['processing.db']['decoy prefix']
     topN = blackboard.config['report'].getint('max scores')
 
@@ -19,41 +21,63 @@
 
     try:
         f = open(full_fname, 'r')
     except:
         import sys
         sys.stderr.write("FATAL: File specified in {} ({}) could not be read\n".format(sys.argv[1], full_fname))
         sys.exit(-1)
+
+    staged = []
+    prev_title = None
     for li, l in enumerate(f):
         if li == 0:
             header = l.strip().split("\t")
-        if li > 0:
+        else:
             try:
                 fields = l.strip().split("\t")
             except:
                 import sys
                 blackboard.LOG.error("During report: ERR: {}\n".format(l))
                 sys.exit(-1)
             score = float(fields[header.index('score')])
             title = fields[header.index('title')]
             desc = fields[header.index('desc')]
             qrow = fields[header.index('qrow')]
             candrow = fields[header.index('candrow')]
             charge = int(fields[header.index('query_charge')])
             mass = float(fields[header.index('query_mass')])
             seq = fields[header.index('seq')]
+            modseq = fields[header.index('modseq')]
+            if title != prev_title:
+                prev_title = title
+                if len(staged) > 0:
+                    idxs = numpy.argsort([s[2] for s in staged])[::-1]
+                    for n, idx in enumerate(idxs):
+                        if n >= topN:
+                            break
+                        data.append(staged[idx])
+                    del idxs
+                    del staged
+                    staged = []
             if not math.isinf(score):
-                data.append((title, score, desc.startswith(decoy_prefix), qrow, candrow, len(seq), charge, mass))
+                staged.append((title, seq, score, desc.startswith(decoy_prefix), qrow, candrow, len(seq), charge, mass))
+
+    idxs = numpy.argsort([s[2] for s in staged])[::-1]
+    for n, idx in enumerate(idxs):
+        if n >= topN:
+            break
+        data.append(staged[idx])
+    del staged
 
     if len(data) == 0:
         import sys # despite top-level import, this is required... wtf???
         blackboard.LOG.error("FATAL: No entries in {}!\n".format(full_fname))
         sys.exit(-1)
 
-    dtype = [('title', object), ('score', numpy.float64), ('decoy', bool), ('qrow', numpy.int64), ('candrow', numpy.int64), ('lgt', numpy.int32), ('charge', numpy.int32), ('mass', numpy.float32)]
+    dtype = [('title', object), ('seq', object), ('score', numpy.float64), ('decoy', bool), ('qrow', numpy.int64), ('candrow', numpy.int64), ('lgt', numpy.int32), ('charge', numpy.int32), ('mass', numpy.float32)]
     ndata = numpy.array(data, dtype=dtype)
     ndata.sort(order=['score'])
     ndata = ndata[::-1]
     keys = numpy.unique([d[0] for d in data])
     grouped_data = {k: [] for k in keys}
     for d in ndata:
         if len(grouped_data[d['title']]) >= topN:
@@ -63,62 +87,51 @@
 
     fdr = data['decoy'].sum() / numpy.logical_not(data['decoy']).sum()
 
     # resort the collated subdata before further processing
     data.sort(order=['score'])
     data = data[::-1]
 
-    fdr_index = numpy.cumsum(numpy.logical_not(data['decoy']))
-    fdr_levels = numpy.cumsum(data['decoy'].astype('float32')) / numpy.maximum(1, fdr_index)
-    sort_idx = numpy.argsort(fdr_levels)
-    fdr_index = fdr_index[sort_idx]
-    fdr_levels = fdr_levels[sort_idx]
-    lgts = data['lgt'][sort_idx]
-    charges = data['charge'][sort_idx]
-    masses = data['mass'][sort_idx]
-    scores = data['score'][sort_idx]
-    fmax = fdr_index[0]
-    for i in range(len(fdr_index)):
-        fmax = max(fmax, fdr_index[i])
-        fdr_index[i] = fmax
+    fdrs = numpy.asarray(pepid_utils.calc_qval(data['score'], numpy.logical_not(data['decoy'])))
 
-    if len(fdr_levels) == 0:
+    if len(fdrs) == 0:
         blackboard.LOG.warning("Empty fdr levels in fdr report")
-        fdr_levels = numpy.array([0])
-        fdr_index = numpy.array([0])
+        fdrs = numpy.array([0])
 
-    best_fdr_idx = -1
     fdr_limit = float(blackboard.config['report']['fdr threshold'])
-    for i, fv in enumerate(fdr_levels):
-        if fv <= fdr_limit:
-            best_fdr_idx = i
-        else:
-            break
+    aw = numpy.argwhere(fdrs <= fdr_limit)
+    idx = min(len(data)-1, aw.reshape((-1,))[-1]+1) if len(aw) > 0 else -1
+
+    blackboard.LOG.info("Overall FDR: {}; FDR range: {}-{}; PSM@{}%: {}".format(fdr, fdrs[0], fdrs[-1], int(fdr_limit * 100.), (data['score'] > data['score'][idx]).sum() if idx >= 0 else 0))
+    blackboard.LOG.info("Unique peps@{}%: {}".format(int(fdr_limit * 100.), len(numpy.unique(data[(data['score'] > data['score'][idx])]['seq'])) if idx >= 0 else 0))
 
-    blackboard.LOG.info("Overall FDR: {}; FDR range: {}-{}; Peptide count over FDR range: {}-{}; PSM@{}%: {}".format(fdr, fdr_levels.min(), fdr_levels.max(), fdr_index.min(), fdr_index.max(), int(fdr_limit * 100.), best_fdr_idx+1))
+    ufdrs = numpy.unique(fdrs)
+    levels = []
+    for u in ufdrs:
+        levels.append((fdrs <= u).sum())
 
     return {
             'n_data': len(grouped_data),
             'fdr': fdr,
-            'level': best_fdr_idx,
-            'curve': numpy.array(list(zip(fdr_levels, fdr_index))),
+            'level': idx,
+            'curve': numpy.array(list(zip(ufdrs, levels))),
             'decoy scores': data['score'][data['decoy']],
             'target scores': data['score'][numpy.logical_not(data['decoy'])],
             'spectra': data['qrow'],
             'peptides': data['candrow'],
-            'lgts': lgts,
+            'lgts': data['lgt'],
             'target lgts': data['lgt'][numpy.logical_not(data['decoy'])],
             'decoy lgts': data['lgt'][data['decoy']],
-            'charges': charges,
+            'charges': data['charge'],
             'target charges': data['charge'][numpy.logical_not(data['decoy'])],
             'decoy charges': data['charge'][data['decoy']],
-            'masses': masses,
+            'masses': data['mass'],
             'target masses': data['mass'][numpy.logical_not(data['decoy'])],
             'decoy masses': data['mass'][data['decoy']],
-            'scores': scores,
+            'scores': data['score'],
             }
 
 def plot_report(stats, fdr_limit, index=0, fig_axs=None):
     import matplotlib
     matplotlib.use("Agg")
     from matplotlib import pyplot as plt
 
@@ -185,15 +198,15 @@
     for i in range(10):
         start = int(i * 0.1 * len(stats['curve']))
         end = int((i+1) * 0.1 * len(stats['curve']))
         dec_stats[i] = inv_curve[start:end].mean()
 
     axs['C'].bar(list(range(10)), dec_stats, alpha=0.7, color=color_all)
 
-    n_unique = len(numpy.unique(stats['peptides'][stats['curve'][:,0] <= fdr_limit]))
+    n_unique = len(numpy.unique(stats['peptides'][:stats['level']]))
     n_all = len(numpy.unique(stats['peptides']))
 
     # Unique peptides, identified spectra
     axs['D'].set_title("Unique Peptides ID'd at {}% FDR\nIDs: {} All: {}".format(int(fdr_limit * 100), n_unique, n_all))
     axs['D'].set_xlabel("Count")
     axs['D'].set_yticks(list(range(2)))
     axs['D'].set_yticklabels(["Unique Peptide IDs", "Unique Peptides"])
@@ -208,15 +221,15 @@
     axs['E'].set_title("Hit Count by Type at {}% FDR\nTargets: {} Decoys: {}".format(int(fdr_limit * 100), n_targets, n_decoys))
     axs['E'].set_yticks(list(range(2)))
     axs['E'].set_yticklabels(["Targets", "Decoys"])
     axs['E'].tick_params(axis='x', rotation=90)
     axs['E'].barh([0, 1], [n_targets, n_decoys], alpha=0.7, color=[color_targets, color_decoys])
 
     # Identified spectra
-    n_spectra_ids = len(numpy.unique(stats['spectra'][stats['curve'][:,0] <= fdr_limit]))
+    n_spectra_ids = len(numpy.unique(stats['spectra'][:stats['level']]))
     n_spectra_no_ids = len(numpy.unique(stats['spectra'])) - n_spectra_ids
 
     axs['F'].set_title("Identified Spectra at {}% FDR\nID: {} No ID: {}".format(int(fdr_limit * 100), n_spectra_ids, n_spectra_no_ids))
     axs['F'].set_yticks(list(range(2)))
     axs['F'].set_yticklabels(["Spectra With IDs", "Spectra Without IDs"])
     axs['F'].tick_params(axis='x', rotation=90)
     axs['F'].barh([0, 1], [n_spectra_ids, n_spectra_no_ids], alpha=0.7, color=color_all)
```

### Comparing `pepid-1.0.0.post2/pepid/main.py` & `pepid-1.1.0/pepid/main.py`

 * *Files 15% similar despite different names*

```diff
@@ -6,88 +6,112 @@
     import blackboard
     from blackboard import here
 else:
     from . import blackboard
     from .blackboard import here
 
 def run(cfg):
-    blackboard.config.read(blackboard.here("data/default.cfg"))
-    blackboard.config.read(cfg)
+    ret = 0
 
-    log_level = blackboard.config['logging']['level'].lower()
+    try:
+        blackboard.config.read(blackboard.here("data/default.cfg"))
+        blackboard.config.read(cfg)
+        blackboard.setup_constants()
+
+        log_level = blackboard.config['logging']['level'].lower()
+
+        if blackboard.config['pipeline'].getboolean('search'):
+            proc = blackboard.subprocess([here("pepid_search.py"), cfg])
+            while True:
+                ret = proc.poll()
+                if ret is not None:
+                    break
+                time.sleep(1) 
+
+            if ret < 0:
+                if log_level == 'debug':
+                    sys.stderr.write("Terminated with error {}\n".format(ret))
+                raise Exception(ret)
+
+        if blackboard.config['pipeline'].getboolean('postsearch'):
+            proc = blackboard.subprocess([here("pepid_postprocess.py"), cfg])
+            while True:
+                ret = proc.poll()
+                if ret is not None:
+                    break
+                time.sleep(1)
+
+            if ret < 0:
+                if log_level == 'debug':
+                    sys.stderr.write("Terminated with error {}\n".format(ret))
+                raise Exception(ret)
+
+        if blackboard.config['pipeline'].getboolean('output'):
+            proc = blackboard.subprocess([here("pepid_io.py"), cfg])
+            while True:
+                ret = proc.poll()
+                if ret is not None:
+                    break
+                time.sleep(1) 
+
+            if ret < 0:
+                if log_level == 'debug':
+                    sys.stderr.write("Terminated with error {}\n".format(ret))
+                raise Exception(ret)
+
+        if blackboard.config['pipeline'].getboolean('report'):
+            report_name = "gen_fdr_report.py"
+            proc = blackboard.subprocess([here(report_name), cfg, "output"])
+            while True:
+                ret = proc.poll()
+                if ret is not None:
+                    break
+                time.sleep(1) 
+
+            if ret < 0:
+                if log_level == 'debug':
+                    sys.stderr.write("Terminated with error {}\n".format(ret))
+                raise Exception(ret)
+
+        if blackboard.config['pipeline'].getboolean('rescoring'):
+            rescorer = blackboard.config['rescoring']['function']
+            proc = blackboard.subprocess([here("pepid_rescore.py"), cfg])
+            while True:
+                ret = proc.poll()
+                if ret is not None:
+                    break
+                time.sleep(1) 
+
+            if ret < 0:
+                if log_level == 'debug':
+                    sys.stderr.write("Terminated with error {}\n".format(ret))
+                raise Exception(ret)
+
+        if blackboard.config['pipeline'].getboolean('rescoring report'):
+            report_name = "gen_fdr_report.py"
+            proc = blackboard.subprocess([here(report_name), cfg, "rescored"])
+            while True:
+                ret = proc.poll()
+                if ret is not None:
+                    break
+                time.sleep(1) 
+
+            if ret < 0:
+                if log_level == 'debug':
+                    sys.stderr.write("Terminated with error {}\n".format(ret))
+                raise Exception(ret)
+
+    finally:
+        if log_level in ['debug', 'info']:
+            sys.stderr.write("Cleaning up...\n")
+        import os
+        os.system("rm -rf {}".format(os.path.join(blackboard.config['data']['tmpdir'], "pepid_socket*")))
+        os.system("rm -rf {}".format(os.path.join(blackboard.config['data']['workdir'], ".lock")))
 
-    if blackboard.config['pipeline'].getboolean('search'):
-        proc = blackboard.subprocess([here("pepid_search.py"), cfg])
-        while True:
-            ret = proc.poll()
-            if ret is not None:
-                break
-            time.sleep(1) 
-
-        if ret < 0:
-            if log_level == 'debug':
-                sys.stderr.write("Terminated with error {}\n".format(ret))
-            sys.exit(ret)
-
-    if blackboard.config['pipeline'].getboolean('output'):
-        proc = blackboard.subprocess([here("pepid_io.py"), cfg])
-        while True:
-            ret = proc.poll()
-            if ret is not None:
-                break
-            time.sleep(1) 
-
-        if ret < 0:
-            if log_level == 'debug':
-                sys.stderr.write("Terminated with error {}\n".format(ret))
-            sys.exit(ret)
-
-
-
-    if blackboard.config['pipeline'].getboolean('report'):
-        report_name = "gen_fdr_report.py"
-        proc = blackboard.subprocess([here(report_name), cfg, "output"])
-        while True:
-            ret = proc.poll()
-            if ret is not None:
-                break
-            time.sleep(1) 
-
-        if ret < 0:
-            if log_level == 'debug':
-                sys.stderr.write("Terminated with error {}\n".format(ret))
-            sys.exit(ret)
-
-    if blackboard.config['pipeline'].getboolean('rescoring'):
-        rescorer = blackboard.config['rescoring']['function']
-        proc = blackboard.subprocess([here("pepid_rescore.py"), cfg])
-        while True:
-            ret = proc.poll()
-            if ret is not None:
-                break
-            time.sleep(1) 
-
-        if ret < 0:
-            if log_level == 'debug':
-                sys.stderr.write("Terminated with error {}\n".format(ret))
-            sys.exit(ret)
-
-    if blackboard.config['pipeline'].getboolean('rescoring report'):
-        report_name = "gen_fdr_report.py"
-        proc = blackboard.subprocess([here(report_name), cfg, "rescored"])
-        while True:
-            ret = proc.poll()
-            if ret is not None:
-                break
-            time.sleep(1) 
-
-        if ret < 0:
-            if log_level == 'debug':
-                sys.stderr.write("Terminated with error {}\n".format(ret))
-            sys.exit(ret)
+        sys.exit(ret)
 
 if __name__ == '__main__':
     if len(sys.argv) != 2:
         print("USAGE: {} config.cfg".format(sys.argv[0]))
         sys.exit(-1)
 
     run(sys.argv[1])
```

### Comparing `pepid-1.0.0.post2/pepid/node.py` & `pepid-1.1.0/pepid/node.py`

 * *Files identical despite different names*

### Comparing `pepid-1.0.0.post2/pepid/output_node.py` & `pepid-1.1.0/pepid/output_node.py`

 * *Files identical despite different names*

### Comparing `pepid-1.0.0.post2/pepid/pepid_compare.py` & `pepid-1.1.0/pepid/pepid_compare.py`

 * *Files 24% similar despite different names*

```diff
@@ -8,14 +8,17 @@
 blackboard.config.read(sys.argv[1])
 blackboard.setup_constants()
 fdr_limit = float(blackboard.config['report']['fdr threshold'])
 
 f1 = pickle.load(open(sys.argv[2], 'rb'))
 f2 = pickle.load(open(sys.argv[3], 'rb'))
 
+import numpy
+f1['curve'] = numpy.asarray(f1['curve'])
+f2['curve'] = numpy.asarray(f2['curve'])
 fig, axs, leg1 = gen_fdr_report.plot_report(f1, fdr_limit, index=0)
 fig, axs, leg2 = gen_fdr_report.plot_report(f2, fdr_limit, index=1, fig_axs=(fig, axs))
 fig.legend(handles=leg1+leg2, loc='lower center', ncols=6, bbox_to_anchor=(0.5, -0.025))
 fig.tight_layout()
 
 base = blackboard.config['data']['output'].rsplit(".", 1)[0]
 fname1 = sys.argv[2].rsplit("/", 1)[-1].rsplit(".", 1)[0]
```

### Comparing `pepid-1.0.0.post2/pepid/pepid_files.py` & `pepid-1.1.0/pepid/pepid_files.py`

 * *Files identical despite different names*

### Comparing `pepid-1.0.0.post2/pepid/pepid_io.py` & `pepid-1.1.0/pepid/pepid_io.py`

 * *Files 10% similar despite different names*

```diff
@@ -50,37 +50,50 @@
             except:
                 time.sleep(1)
                 continue
 
         blackboard.execute(cur, "SELECT results.rowid, {} FROM results JOIN (SELECT qrow, IFNULL((SELECT score FROM results WHERE qrow = qrows.qrow ORDER BY score DESC LIMIT 1 OFFSET ?), -1) AS cutoff_score FROM (SELECT DISTINCT qrow FROM results) AS qrows) AS cutoffs ON results.qrow = cutoffs.qrow AND results.score >= cutoffs.cutoff_score ORDER BY results.qrow ASC, results.score DESC;".format(",".join(map(lambda x: "results." + x, header))), (max_cands-1,))
         fetch_batch_size = 62000 # The maximum batch size supported by the default sqlite engine is a bit more than 62000
 
+        prev_key = None
+        payloads = []
+
         while True:
             results = cur.fetchmany(fetch_batch_size)
             if len(results) == 0:
+                if prev_key is None or len(payloads) == 0:
+                    break
+
+                blackboard.lock()
+                outf = open(out_fname, 'a')
+
+                for datum in payloads[:max_cands]:
+                    fields = []
+                    for k in header:
+                        fields.append(str(datum[k]).replace("\t", "    "))
+                    outf.write("\t".join(fields) + "\n")
+
+                outf.close()
+                blackboard.unlock()
                 break
 
             blackboard.lock()
             outf = open(out_fname, 'a')
 
             for idata, data in enumerate(results):
                 data = dict(data)
-                # Need this second counter because if we have more than X results with the same score
-                # we end up grabbing it all anyway. Example:
-                # scores 1 1 1 1 1 1 1 1 1 1 1 0.9 0.9 0.9 with top 10:
-                #   We end up selecting (>=) 11 1's instead of the max 10.
-                if counts[data['qrow']] >= max_cands:
-                    continue
-                else:
-                    fields = []
-                    for k in header:
-                        fields.append(str(data[k]).replace("\t", "    "))
-                    #fields.append(str(data['rowid']))
-                    outf.write("\t".join(fields) + "\n")
-                    counts[data['qrow']] += 1
+                if prev_key is None or data['qrow'] != prev_key:
+                    for datum in payloads[:max_cands]:
+                        fields = []
+                        for k in header:
+                            fields.append(str(datum[k]).replace("\t", "    "))
+                        outf.write("\t".join(fields) + "\n")
+                    prev_key = data['qrow']
+                    payloads = []
+                payloads.append(data)
 
             outf.close()
             blackboard.unlock()
 
         del cur
         del conn
```

### Comparing `pepid-1.0.0.post2/pepid/pepid_mp.py` & `pepid-1.1.0/pepid/pepid_mp.py`

 * *Files identical despite different names*

### Comparing `pepid-1.0.0.post2/pepid/pepid_randomforest.py` & `pepid-1.1.0/pepid/pepid_randomforest.py`

 * *Files identical despite different names*

### Comparing `pepid-1.0.0.post2/pepid/pepid_rescore.py` & `pepid-1.1.0/pepid/pepid_rescore.py`

 * *Files 17% similar despite different names*

```diff
@@ -18,16 +18,15 @@
     if rescore_fn is not None:
         f = open(blackboard.config['data']['output'], 'r')
         fname, ext = blackboard.config['data']['output'].rsplit('.', 1)
         outf = open(fname + blackboard.config['rescoring']['suffix'] + "." + ext, 'w')
 
         header = next(f)
         outf.write(header)
-        f.seek(0)
+        f.close()
 
         for data in rescore_fn(sys.argv[1]):
             outf.write("\t".join(list(map(str, data))) + "\n")
 
-        f.close()
         outf.close()
     else:
         blackboard.LOG.warning("No rescoring function specified, not rescoring")
```

### Comparing `pepid-1.0.0.post2/pepid/pepid_search.py` & `pepid-1.1.0/pepid/pepid_search.py`

 * *Files 14% similar despite different names*

```diff
@@ -27,155 +27,144 @@
         import db
         import search
     else:
         from . import queries
         from . import db
         from . import search
 
-    try:
-        log.info("Search phases to run: | " + ("Query Processing | " if blackboard.config['processing.query'].getboolean('enabled') else "") +
-                                    ("DB Processing | " if blackboard.config['processing.db'].getboolean('enabled') else "") +
-                                    ("Postprocessing | " if blackboard.config['postprocessing'].getboolean('enabled') else "") +
-                                    ("Score | " if blackboard.config['scoring'].getboolean('enabled') else ""))
-        log.info("Preparing Input Databases...")
-        db_paths = []
-        if blackboard.config['processing.query'].getboolean('enabled'):
-            db_paths.append(blackboard.DB_PATH + "_q.sqlite")
-        if blackboard.config['processing.db'].getboolean('enabled'):
-            db_paths.append(blackboard.DB_PATH + "_cands.sqlite")
-        if blackboard.config['scoring'].getboolean('enabled'):
-            db_paths.append(blackboard.DB_PATH + ".sqlite")
-        for p in db_paths:
-            if os.path.exists(p):
-                os.remove(p)
-        blackboard.prepare_connection()
-        if blackboard.config['processing.query'].getboolean('enabled'):
-            queries.prepare_db()
-        if blackboard.config['processing.db'].getboolean('enabled'):
-            db.prepare_db()
-        blackboard.init_results_db()
-
-        if blackboard.config['scoring'].getboolean('enabled'):
-            log.info("Preparing Input Processing Nodes...")
-            
-            qnodes = blackboard.config['processing.query'].getint('workers')
-            dbnodes = blackboard.config['processing.db'].getint('workers')
-            snodes = blackboard.config['scoring'].getint('workers')
-
-            if qnodes < 0 or dbnodes < 0 or snodes < 0:
-                log.fatal("Node settings are query={}, db={}, search={}, but only values 0 or above allowed.".format(qnodes, dbnodes, snodes))
-                sys.exit(-2)
-
-            base_path = blackboard.TMP_PATH
-
-            proc_spec = []
-
-            if blackboard.config['processing.db'].getboolean('enabled'):
-                batch_size = blackboard.config['processing.db'].getint('batch size')
-                n_db = db.count_db()
-                n_db_batches = math.ceil(n_db / batch_size)
-
-                dbspecs = []
-
-                # Have to use 2 separate steps to ensure that if there are overlaps, the decoys are dropped
-                # The protein-reverse approach generates quite a few overlaps...
-                dbspec = [(blackboard.here("db_node.py"), dbnodes, n_db_batches,
-                                            [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(dbnodes)],
-                                            [struct.pack("!cQQI6sc", bytes([0x01]), b * batch_size, min((b+1) * batch_size, n_db), 6, "normal".encode('utf-8'), "$".encode("utf-8")) for b in range(n_db_batches)],
-                                            [struct.pack("!cc", bytes([0x7f]), "$".encode('utf-8')) for _ in range(dbnodes)])]
-                dbspecs.append(dbspec)
-
-                if blackboard.config['processing.db'].getboolean('generate decoys'):
-                    dbdecoy_spec = [(blackboard.here("db_node.py"), dbnodes, n_db_batches,
-                                                [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(dbnodes)],
-                                                [struct.pack("!cQQI5sc", bytes([0x01]), b * batch_size, min((b+1) * batch_size, n_db), 5, "decoy".encode('utf-8'), "$".encode("utf-8")) for b in range(n_db_batches)],
-                                                [struct.pack("!cc", bytes([0x7f]), "$".encode('utf-8')) for _ in range(dbnodes)])]
-                    dbspecs.append(dbdecoy_spec)
-
-                proc_spec = proc_spec
-                for spec in dbspecs:
-                    proc_spec = proc_spec + spec
+    log.info("Search phases to run: | " + ("Query Processing | " if blackboard.config['processing.query'].getboolean('enabled') else "") +
+                                ("DB Processing | " if blackboard.config['processing.db'].getboolean('enabled') else "") +
+                                ("Postprocessing | " if blackboard.config['postprocessing'].getboolean('enabled') else "") +
+                                ("Score | " if blackboard.config['scoring'].getboolean('enabled') else ""))
+    log.info("Preparing Input Databases...")
+    db_paths = []
+    if blackboard.config['processing.query'].getboolean('enabled'):
+        db_paths.append(blackboard.DB_PATH + "_q.sqlite")
+    if blackboard.config['processing.db'].getboolean('enabled'):
+        db_paths.append(blackboard.DB_PATH + "_cands.sqlite")
+    if blackboard.config['scoring'].getboolean('enabled'):
+        db_paths.append(blackboard.DB_PATH + ".sqlite")
+    for p in db_paths:
+        if os.path.exists(p):
+            os.remove(p)
+    blackboard.prepare_connection()
+    if blackboard.config['processing.query'].getboolean('enabled'):
+        queries.prepare_db()
+    if blackboard.config['processing.db'].getboolean('enabled'):
+        db.prepare_db()
+    blackboard.init_results_db()
+
+    n_queries = -1
+    base_path = blackboard.TMP_PATH
+    log.info("Preparing Input Processing Nodes...")
+    
+    qnodes = blackboard.config['processing.query'].getint('workers')
+    dbnodes = blackboard.config['processing.db'].getint('workers')
+    snodes = blackboard.config['scoring'].getint('workers')
+
+    if qnodes < 0 or dbnodes < 0 or snodes < 0:
+        log.fatal("Node settings are query={}, db={}, search={}, but only values 0 or above allowed.".format(qnodes, dbnodes, snodes))
+        sys.exit(-2)
+
+    proc_spec = []
+
+    if blackboard.config['processing.db'].getboolean('enabled'):
+        batch_size = blackboard.config['processing.db'].getint('batch size')
+        n_db = db.count_db()
+        n_db_batches = math.ceil(n_db / batch_size)
+
+        dbspecs = []
+
+        # Have to use 2 separate steps to ensure that if there are overlaps, the decoys are dropped
+        # The protein-reverse approach generates quite a few overlaps...
+        dbspec = [(blackboard.here("db_node.py"), dbnodes, n_db_batches,
+                                    [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(dbnodes)],
+                                    [struct.pack("!cQQI6sc", bytes([0x01]), b * batch_size, min((b+1) * batch_size, n_db), 6, "normal".encode('utf-8'), "$".encode("utf-8")) for b in range(n_db_batches)],
+                                    [struct.pack("!cc", bytes([0x7f]), "$".encode('utf-8')) for _ in range(dbnodes)])]
+        dbspecs.append(dbspec)
+
+        if blackboard.config['processing.db'].getboolean('generate decoys'):
+            dbdecoy_spec = [(blackboard.here("db_node.py"), dbnodes, n_db_batches,
+                                        [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(dbnodes)],
+                                        [struct.pack("!cQQI5sc", bytes([0x01]), b * batch_size, min((b+1) * batch_size, n_db), 5, "decoy".encode('utf-8'), "$".encode("utf-8")) for b in range(n_db_batches)],
+                                        [struct.pack("!cc", bytes([0x7f]), "$".encode('utf-8')) for _ in range(dbnodes)])]
+            dbspecs.append(dbdecoy_spec)
+
+        proc_spec = proc_spec
+        for spec in dbspecs:
+            proc_spec = proc_spec + spec
+
+    if (blackboard.config['processing.query'].getboolean('enabled') or blackboard.config['postprocessing'].getboolean('queries')) or blackboard.config['scoring'].getboolean('enabled'):
+        n_queries = queries.count_queries()
+
+    if blackboard.config['processing.query'].getboolean('enabled'):
+        batch_size = blackboard.config['processing.query'].getint('batch size')
+        n_query_batches = math.ceil(n_queries / batch_size)
+
+        qspec = [(blackboard.here("queries_node.py"), qnodes, n_query_batches,
+                        [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(qnodes)],
+                        [struct.pack("!cQQc", bytes([0x01]), b * batch_size, min((b+1) * batch_size, n_queries), "$".encode("utf-8")) for b in range(n_query_batches)],
+                        [struct.pack("!cc", bytes([0x7f]), "$".encode("utf-8")) for _ in range(qnodes)])] 
+
+        proc_spec = proc_spec + qspec
+
+    if len(proc_spec) != 0:
+        pepid_mp.handle_nodes("Input Processing", proc_spec, cfg_file=cfg_file, tqdm_silence=tqdm_silence)
+
+    if blackboard.config['postprocessing'].getboolean('enabled'):
+        idx = 0
+
+        qnodes = blackboard.config['processing.query'].getint('postprocessing workers')
+        dbnodes = blackboard.config['processing.db'].getint('postprocessing workers')
+
+        if qnodes < 0 or dbnodes < 0:
+            log.fatal("Post-processing node settings are query={}, db={}, but only values 0 or above allowed.".format(qnodes, dbnodes))
+            sys.exit(-2)
+
+        specs = []
+
+        if blackboard.config['postprocessing'].getboolean('db'):
+            db_batch_size = blackboard.config['processing.db'].getint('batch size')
+            n_db = db.count_peps()
+            n_db_batches = math.ceil(n_db / db_batch_size)
+
+            dbspec = [(blackboard.here("db_node.py"), dbnodes, n_db_batches,
+                            [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(dbnodes)],
+                            [struct.pack("!cQQc", bytes([0x02]), b * db_batch_size, min((b+1) * db_batch_size, n_db), "$".encode('utf-8')) for b in range(n_db_batches)],
+                            [struct.pack("!cc", bytes([0x7f]), "$".encode("utf-8")) for _ in range(dbnodes)])]
+            specs.extend(dbspec)
 
-            if (blackboard.config['processing.query'].getboolean('enabled') and blackboard.config['postprocessing'].getboolean('queries')) or blackboard.config['scoring'].getboolean('enabled'):
+        if blackboard.config['postprocessing'].getboolean('queries'):
+            if n_queries < 0:
                 n_queries = queries.count_queries()
+            q_batch_size = blackboard.config['processing.query'].getint('batch size')
+            n_query_batches = math.ceil(n_queries / q_batch_size)
+            qspec = [(blackboard.here("queries_node.py"), qnodes, n_query_batches,
+                            [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(qnodes)],
+                            [struct.pack("!cQQc", bytes([0x02]), b * q_batch_size, min((b+1) * q_batch_size, n_queries), "$".encode("utf-8")) for b in range(n_query_batches)],
+                            [struct.pack("!cc", bytes([0x7f]), "$".encode("utf-8")) for _ in range(qnodes)])]
+            specs.extend(qspec)
+
+        if len(specs) != 0:
+            pepid_mp.handle_nodes("Input Postprocessing", specs, cfg_file=cfg_file, tqdm_silence=tqdm_silence)
+
+    cur = blackboard.CONN.cursor()
+    blackboard.execute(cur, "CREATE INDEX IF NOT EXISTS c.cand_mass_idx ON candidates (mass ASC);")
+    blackboard.execute(cur, "CREATE INDEX IF NOT EXISTS q.query_mass_idx ON queries (mass ASC);")
+    del cur
+
+    if blackboard.config['scoring'].getboolean('enabled'):
+        batch_size = blackboard.config['scoring'].getint('batch size')
+        n_search_batches = math.ceil(n_queries / batch_size)
+        sspec = [(blackboard.here("search_node.py"), snodes, n_search_batches,
+                        [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(snodes)],
+                        [struct.pack("!cQQc", bytes([0x01]), b * batch_size, min((b+1) * batch_size, n_queries), "$".encode("utf-8")) for b in range(n_search_batches)],
+                        [struct.pack("!cc", bytes([0x7f]), "$".encode("utf-8")) for _ in range(snodes)])]
 
-            if blackboard.config['processing.query'].getboolean('enabled'):
-                batch_size = blackboard.config['processing.query'].getint('batch size')
-                n_query_batches = math.ceil(n_queries / batch_size)
-        
-                qspec = [(blackboard.here("queries_node.py"), qnodes, n_query_batches,
-                                [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(qnodes)],
-                                [struct.pack("!cQQc", bytes([0x01]), b * batch_size, min((b+1) * batch_size, n_queries), "$".encode("utf-8")) for b in range(n_query_batches)],
-                                [struct.pack("!cc", bytes([0x7f]), "$".encode("utf-8")) for _ in range(qnodes)])] 
-
-                proc_spec = proc_spec + qspec
-
-            if len(proc_spec) != 0:
-                pepid_mp.handle_nodes("Input Processing", proc_spec, cfg_file=cfg_file, tqdm_silence=tqdm_silence)
-
-        if blackboard.config['postprocessing'].getboolean('enabled'):
-            idx = 0
-
-            qnodes = blackboard.config['processing.query'].getint('postprocessing workers')
-            dbnodes = blackboard.config['processing.db'].getint('postprocessing workers')
-
-            if qnodes < 0 or dbnodes < 0:
-                log.fatal("Post-processing node settings are query={}, db={}, but only values 0 or above allowed.".format(qnodes, dbnodes))
-                sys.exit(-2)
-
-            specs = []
-
-            if blackboard.config['postprocessing'].getboolean('db'):
-                db_batch_size = blackboard.config['processing.db'].getint('batch size')
-                n_db = db.count_peps()
-                n_db_batches = math.ceil(n_db / db_batch_size)
-
-                dbspec = [(blackboard.here("db_node.py"), dbnodes, n_db_batches,
-                                [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(dbnodes)],
-                                [struct.pack("!cQQc", bytes([0x02]), b * db_batch_size, min((b+1) * db_batch_size, n_db), "$".encode('utf-8')) for b in range(n_db_batches)],
-                                [struct.pack("!cc", bytes([0x7f]), "$".encode("utf-8")) for _ in range(dbnodes)])]
-                specs.extend(dbspec)
-
-            if blackboard.config['postprocessing'].getboolean('queries'):
-                q_batch_size = blackboard.config['processing.query'].getint('batch size')
-                n_query_batches = math.ceil(n_queries / q_batch_size)
-                qspec = [(blackboard.here("queries_node.py"), qnodes, n_query_batches,
-                                [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(qnodes)],
-                                [struct.pack("!cQQc", bytes([0x02]), b * q_batch_size, min((b+1) * q_batch_size, n_queries), "$".encode("utf-8")) for b in range(n_query_batches)],
-                                [struct.pack("!cc", bytes([0x7f]), "$".encode("utf-8")) for _ in range(qnodes)])]
-                specs.extend(qspec)
-
-            if len(specs) != 0:
-                pepid_mp.handle_nodes("Input Postprocessing", specs, cfg_file=cfg_file, tqdm_silence=tqdm_silence)
-
-        cur = blackboard.CONN.cursor()
-        blackboard.execute(cur, "CREATE INDEX IF NOT EXISTS c.cand_mass_idx ON candidates (mass ASC);")
-        blackboard.execute(cur, "CREATE INDEX IF NOT EXISTS q.query_mass_idx ON queries (mass ASC);")
-        del cur
-
-        if blackboard.config['scoring'].getboolean('enabled'):
-            batch_size = blackboard.config['scoring'].getint('batch size')
-            n_search_batches = math.ceil(n_queries / batch_size)
-            sspec = [(blackboard.here("search_node.py"), snodes, n_search_batches,
-                            [struct.pack("!cI{}sc".format(len(base_path)), bytes([0x00]), len(base_path), base_path.encode("utf-8"), "$".encode("utf-8")) for _ in range(snodes)],
-                            [struct.pack("!cQQc", bytes([0x01]), b * batch_size, min((b+1) * batch_size, n_queries), "$".encode("utf-8")) for b in range(n_search_batches)],
-                            [struct.pack("!cc", bytes([0x7f]), "$".encode("utf-8")) for _ in range(snodes)])]
-
-            pepid_mp.handle_nodes("Search", sspec, cfg_file=cfg_file, tqdm_silence=tqdm_silence)
-
-    finally:
-        log.info("Cleaning up...")
-        if len(blackboard.TMP_PATH) > 0:
-            os.system("rm -rf {}".format(os.path.join(blackboard.config['data']['tmpdir'], "pepid_socket*")))
-            #os.system("rm -rf {}".format(os.path.join(blackboard.TMP_PATH, "pepidtmp*")))
-            # Note: final db not removed for future reuse
-
-            if blackboard.LOCK is not None:
-                blackboard.LOCK.close()
-                os.system("rm -rf {}".format(os.path.join(blackboard.TMP_PATH, ".lock")))
+        pepid_mp.handle_nodes("Search", sspec, cfg_file=cfg_file, tqdm_silence=tqdm_silence)
 
 if __name__ == "__main__":
     if(len(sys.argv) != 2):
         print("USAGE: {} config.cfg".format(sys.argv[0]))
         sys.exit(-1)
 
     global cfg_file
```

### Comparing `pepid-1.0.0.post2/pepid/pin_node.py` & `pepid-1.1.0/pepid/search_node.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,41 +1,41 @@
 import struct
 import os
 import time
 import sys
 
 if __package__ is None or __package__ == '':
-    import node
     import blackboard
+    import node
 else:
-    from . import node
     from . import blackboard
+    from . import node
+
 
-class PINNode(node.Node):
+class SearchNode(node.Node):
     def __init__(self, unix_sock):
         super().__init__(unix_sock)
         self.path = None
-        self.file = None
         self.messages[0x00] = [None, self.prepare]
         self.messages[0x01] = ["!QQc", self.do]
 
     def do(self, start, end, _):
         if __package__ is None or __package__ == '':
-            import pepid_percolator
+            import search
         else:
-            from . import pepid_percolator
+            from . import search
 
         if not self.path:
             raise ValueError("'do' message received before 'prepare' message, aborting.")
 
-        pepid_percolator.generate_pin(start, end)
+        search.search_core(start, end)
 
     def prepare(self, msg):
         lgt = struct.unpack("!I", msg[:4])[0]
         blackboard.TMP_PATH = struct.unpack("!{}sc".format(lgt), msg[4:])[0].decode('utf-8')
         self.path = blackboard.TMP_PATH
         blackboard.setup_constants()
         blackboard.LOCK = open(os.path.join(blackboard.TMP_PATH, ".lock"), "wb")
         blackboard.prepare_connection()
 
 if __name__ == '__main__':
-    node.init(PINNode)
+    node.init(SearchNode)
```

### Comparing `pepid-1.0.0.post2/pepid/queries.py` & `pepid-1.1.0/pepid/queries.py`

 * *Files 8% similar despite different names*

```diff
@@ -46,46 +46,47 @@
             entry_idx += 1
             title = ""
             charge = 0
             precmass = 0.0
             rt = 0.0
             mz_arr = []
             intens_arr = []
+            continue
+
         if entry_idx < start:
             continue
         elif entry_idx >= end:
             break
-        else:
-            if l[:len("TITLE=")] == "TITLE=":
-                title = l[len("TITLE="):].strip()
-            elif l[:len("RTINSECONDS=")] == "RTINSECONDS=":
-                rt = float(l[len("RTINSECONDS="):].strip())
-            elif l[:len("CHARGE=")] == "CHARGE=":
-                charge = int(l[len("CHARGE="):].strip().replace("+", ""))
-            elif l[:len("PEPMASS=")] == "PEPMASS=":
-                precmass = float(l[len("PEPMASS="):].split(maxsplit=1)[0])
-            elif l[:len("END IONS")] == "END IONS":
-                precmass = (precmass * charge) - (charge-1)*pepid_utils.MASS_PROT - pepid_utils.MASS_PROT
-                if (min_mass <= precmass <= max_mass) and (min_charge <= charge <= max_charge):
-                    data.append({k:None for k in blackboard.QUERY_COLS})
-                    delta_l = tol_l if not is_ppm else pepid_utils.calc_rev_ppm(precmass, tol_l)
-                    delta_r = tol_r if not is_ppm else pepid_utils.calc_rev_ppm(precmass, tol_r)
-                    data[-1]['title'] = title
-                    data[-1]['rt'] = rt
-                    data[-1]['charge'] = charge
-                    data[-1]['mass'] = precmass
-                    data[-1]['spec'] = blackboard.Spectrum(list(zip(mz_arr, intens_arr)))
-                    data[-1]['min_mass'] = precmass + delta_l
-                    data[-1]['max_mass'] = precmass + delta_r
-                    data[-1]['meta'] = blackboard.Meta(None)
-                    
-            elif '0' <= l[0] <= '9':
-                mz, intens = l.split(maxsplit=1)
-                mz_arr.append(float(mz))
-                intens_arr.append(float(intens))
+
+        if l[:len("TITLE=")] == "TITLE=":
+            title = l[len("TITLE="):].strip()
+        elif l[:len("RTINSECONDS=")] == "RTINSECONDS=":
+            rt = float(l[len("RTINSECONDS="):].strip())
+        elif l[:len("CHARGE=")] == "CHARGE=":
+            charge = int(l[len("CHARGE="):].strip().replace("+", ""))
+        elif l[:len("PEPMASS=")] == "PEPMASS=":
+            precmass = float(l[len("PEPMASS="):].split(maxsplit=1)[0])
+        elif l[:len("END IONS")] == "END IONS":
+            precmass = (precmass * charge) - (charge-1)*pepid_utils.MASS_PROT - pepid_utils.MASS_PROT
+            if (min_mass <= precmass <= max_mass) and (min_charge <= charge <= max_charge):
+                data.append({k:None for k in blackboard.QUERY_COLS})
+                delta_l = tol_l if not is_ppm else pepid_utils.calc_rev_ppm(precmass, tol_l)
+                delta_r = tol_r if not is_ppm else pepid_utils.calc_rev_ppm(precmass, tol_r)
+                data[-1]['title'] = title
+                data[-1]['rt'] = rt
+                data[-1]['charge'] = charge
+                data[-1]['mass'] = precmass
+                data[-1]['spec'] = blackboard.Spectrum(list(zip(mz_arr, intens_arr)))
+                data[-1]['min_mass'] = precmass + delta_l
+                data[-1]['max_mass'] = precmass + delta_r
+                data[-1]['meta'] = blackboard.Meta(None)
+        elif '0' <= l[0] <= '9':
+            mz, intens = l.split(maxsplit=1)
+            mz_arr.append(float(mz))
+            intens_arr.append(float(intens))
     cur = blackboard.CONN.cursor()
     blackboard.executemany(cur, blackboard.insert_dict_str("queries", blackboard.QUERY_COLS), data)
     cur.close()
     blackboard.commit()
 
 def user_processing(start, end):
     """
@@ -106,16 +107,17 @@
 
     if metadata_fn is None:
         return
 
     cur = blackboard.CONN.cursor()
     blackboard.execute(cur, blackboard.select_str("queries", blackboard.QUERY_COLS + ["rowid"], "WHERE rowid BETWEEN ? AND ?"), (start+1, end))
     data = cur.fetchall()
-    meta = metadata_fn(data[:end-start])
-    blackboard.executemany(cur, "UPDATE queries SET meta = ? WHERE rowid = ?;", zip(map(blackboard.Meta, meta), map(lambda x: x['rowid'], data)))
+    meta = metadata_fn(data)
+    if meta is not None:
+        blackboard.executemany(cur, "UPDATE queries SET meta = ? WHERE rowid = ?;", zip(map(blackboard.Meta, meta), map(lambda x: x['rowid'], data)))
     cur.close()
 
 def prepare_db():
     """
     Creates the required tables in the temporary database for queries processing
     """
```

### Comparing `pepid-1.0.0.post2/pepid/queries_node.py` & `pepid-1.1.0/pepid/queries_node.py`

 * *Files identical despite different names*

### Comparing `pepid-1.0.0.post2/pepid/search.py` & `pepid-1.1.0/pepid/search.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 import numpy
 import numpy.linalg
 import re
 import numba
 import numba.typed
 import sys
+import msgpack
 
 if __package__ is None or __package__ == '':
     import blackboard
     import pepid_utils
 else:
     from . import blackboard
     from . import pepid_utils
@@ -116,28 +117,28 @@
                 score = sumis.sum()
                 for m in mults:
                     score *= m
             score = float(min(score, float_lim))
 
             logsumI = numpy.log10(sumI) # note: x!tandem uses a factor 4 to multiply this by default
 
-            ret[-1].append({"dM": (c['mass'] - q['mass']) / c['mass'],
-                        "absdM": abs((c['mass'] - q['mass']) / c['mass']),
+            ret[-1].append({"dM": float((c['mass'] - q['mass']) / c['mass']),
+                        "absdM": float(abs((c['mass'] - q['mass']) / c['mass'])),
                         "peplen": len(c['seq']),
-                        "ionFrac": total_matched / (theoretical.shape[0] * theoretical.shape[1]),
+                        "ionFrac": float(total_matched / (theoretical.shape[0] * theoretical.shape[1])),
                         #'relIntTotMatch': sumI / norm,
                         'charge': int(q['charge']),
                         'z2': int(q['charge'] == 2),
                         'z3': int(q['charge'] == 3),
                         'z4': int(q['charge'] == 4),
-                        'rawscore': score,
+                        'rawscore': float(score),
                         #'xcorr': xcorr,
-                        'expMass': q['mass'],
-                        'calcMass': c['mass'],
-                'score': score, 'sumI': logsumI, 'total_matched': total_matched, 'title': q['title'], 'desc': c['desc'], 'seq': c['seq'], 'modseq': "".join([s if m == 0 else s + "[{}]".format(m) for s, m in zip(c['seq'], c['mods'])])})
+                        'expMass': float(q['mass']),
+                        'calcMass': float(c['mass']),
+                'score': float(score), 'sumI': float(logsumI), 'total_matched': int(total_matched), 'title': q['title'], 'desc': c['desc'], 'seq': c['seq'], 'modseq': "".join([s if m == 0 else s + "[{}]".format(m) for s, m in zip(c['seq'], c['mods'])])})
     return ret
 
 @numba.njit(locals={'spectrum': numba.float32[:,::1], 'theoretical': numba.float32[:,:,::1], 'acc': numba.float32, 'delta': numba.float32, 'series_count': numba.int32, 'norm': numba.float32, 'spec_idx': numba.int32})
 def hyperscore_score(spectrum, theoretical, norm, acc=10, acc_ppm=True, cutoff=0.01, match_mult=100.0, type_charge=False, type_series=False, type_both=True, series_count=2, ignore_weights=False, match_all=False):
     mz_array = spectrum[:,0]
     intens = spectrum[:,1]
 
@@ -274,28 +275,28 @@
             n_series = frag.shape[0] // series_count
             total_lgt = frag.shape[1] * frag.shape[0]
 
             if score <= 0:
                 ret[-1].append({'score': 0})
                 continue
             else:
-                ret[-1].append({"dM": (c['mass'] - q['mass']) / c['mass'],
+                ret[-1].append({"dM": float((c['mass'] - q['mass']) / c['mass']),
                             "absdM": abs((c['mass'] - q['mass']) / c['mass']),
                             "peplen": len(c['seq']),
-                            "ionFrac": n_matches / total_lgt,
+                            "ionFrac": float(n_matches / total_lgt),
                             #'relIntTotMatch': sumI / norm,
                             'charge': int(q['charge']),
                             'z2': int(q['charge'] == 2),
                             'z3': int(q['charge'] == 3),
                             'z4': int(q['charge'] == 4),
-                            'rawscore': score,
+                            'rawscore': float(score),
                             #'xcorr': xcorr,
-                            'expMass': q['mass'],
-                            'calcMass': c['mass'],
-                            'score': score, 'sumI': sumI, 'total_matched': n_matches, 'title': q['title'], 'desc': c['desc'], 'seq': c['seq'], 'modseq': "".join([s if m == 0 else s + "[{}]".format(m) for s, m in zip(c['seq'], c['mods'])])})
+                            'expMass': float(q['mass']),
+                            'calcMass': float(c['mass']),
+                            'score': float(score), 'sumI': float(sumI), 'total_matched': int(n_matches), 'title': q['title'], 'desc': c['desc'], 'seq': c['seq'], 'modseq': "".join([s if m == 0 else s + "[{}]".format(m) for s, m in zip(c['seq'], c['mods'])])})
     return ret
 
 @numba.njit(locals={'scale': numba.int32, 'i': numba.int32, 'bins': numba.float32[::1]})
 def get_bin_index(mass, bins):
     if len(bins) == 0:
         return len(bins)
     if mass < bins[0]:
@@ -419,45 +420,47 @@
 
     ret_xcorr = xcorr(qcands, qs)
     ret_hscore = hyperscore(qcands, qs)
 
     ret = [[{**rh, **rx, 'xcorr': rx['score'], 'hyperscore': rh['score']} for rx, rh in zip(retx, reth)] for retx, reth in zip(ret_xcorr, ret_hscore)]
     for re in ret:
         for r in re:
-            r['score'] = max(0, r['xcorr'], numpy.sqrt(numpy.log10(r['hyperscore'] + 1)), r['xcorr'] * numpy.sqrt(numpy.log10(r['hyperscore'] + 1)))
+            r['score'] = float(max(0, r['xcorr'], numpy.sqrt(numpy.log10(r['hyperscore'] + 1)), r['xcorr'] * numpy.sqrt(numpy.log10(r['hyperscore'] + 1))))
 
     return ret
 
+def stub_filter(cands, q):
+    return cands
+
 def search_core(start, end):
     """
     Core search algorithm: collects and finalizes the data, then
     parses and applies the user scoring function from the config.
     The function should take two arguments: a list of candidates, and a query.
 
     Candidates and queries are rows as saved in the DB, whose description can be found
     in `blackboard.py`.
     """
 
     blackboard.init_results_db(generate=True, base_dir=blackboard.TMP_PATH)
     shard_level = blackboard.config['scoring'].getint('sharding threshold')
 
     scoring_fn = pepid_utils.import_or(blackboard.config['scoring']['function'], xcorr)
+    select_fn = pepid_utils.import_or(blackboard.config['scoring']['candidate filtering function'], stub_filter)
 
     batch_size = blackboard.config['scoring'].getint('batch size')
 
     cur = blackboard.CONN.cursor()
     res_cur = blackboard.RES_CONN.cursor()
     m_cur = blackboard.META_CONN.cursor()
 
     blackboard.execute(cur, blackboard.select_str("queries", ["rowid"] + blackboard.QUERY_COLS, "WHERE rowid BETWEEN ? AND ?"), (start+1, end))
     queries = cur.fetchall()
 
-    blackboard.execute(res_cur, "SELECT MAX(rrow) FROM results;")
-    prev_rrow = res_cur.fetchone()[0]
-    rrow = 1 if prev_rrow is None else prev_rrow + 1
+    rrow = 1
 
     fname_prefix = blackboard.RES_DB_FNAME.rsplit(".", 1)[0]
 
     n_cands = 0
     cands = []
     quers = []
 
@@ -471,15 +474,15 @@
         this_res = []
         metar = []
         for ii, (r, c) in enumerate(zip(res, cands)):
             if r['score'] <= 0:
                 continue
             else:
                 this_res.append({'qrow': q['rowid'], 'matches': r['total_matched'], 'logSumI': r['sumI'], 'candrow': c['rowid'], 'score': r['score'], 'title': r['title'], 'desc': r['desc'], 'modseq': r['modseq'], 'seq': r['seq'], 'query_charge': q['charge'], 'query_mass': q['mass'], 'cand_mass': c['mass'], 'rrow': rrow, 'file': fname_prefix})
-                metar.append({'score': r['score'], 'qrow': q['rowid'], 'candrow': c['rowid'], 'data': str(r), "rrow": rrow})
+                metar.append({'score': r['score'], 'qrow': q['rowid'], 'candrow': c['rowid'], 'data': msgpack.dumps(r), 'extra': msgpack.dumps(None), "rrow": rrow})
                 rrow += 1
         if len(this_res) > 0:
             blackboard.executemany(res_cur, blackboard.maybe_insert_dict_str("results", blackboard.RES_COLS), this_res)
             blackboard.executemany(m_cur, blackboard.maybe_insert_dict_str("meta", blackboard.META_COLS), metar)
             if rrow > shard_level:
                 rrow = 1
                 blackboard.RES_CONN.commit()
@@ -501,32 +504,34 @@
 
     for iq, q in enumerate(queries):
         quers.append(q)
         cands.append([])
         blackboard.execute(cur, blackboard.select_str("candidates", ["rowid"] + blackboard.DB_COLS, "WHERE mass BETWEEN ? AND ?"), (q['min_mass'], q['max_mass']))
         
         while True:
-            cand_set = cur.fetchmany(batch_size)
+            raw_set = cur.fetchmany(batch_size)
+            if len(raw_set) == 0:
+                break
+            cand_set = select_fn([dict(o) for o in raw_set], q)
+            if len(cand_set) == 0:
+                continue
             cands[-1].extend(cand_set)
             n_cands += len(cand_set)
 
             if n_cands >= batch_size:
                 n_cands = 0
                 res = scoring_fn(cands, quers)
                 for oq, ocands, ores in zip(quers, cands, res):
                     rrow = insert(ores, ocands, oq, rrow)
                 cands = [[]]
                 quers = [quers[-1]]
-
-            if len(cand_set) == 0:
-                if len(cands[0]) > 0:
-                    res = scoring_fn(cands, quers)
-                    for oq, ocands, ores in zip(quers, cands, res):
-                        rrow = insert(ores, ocands, oq, rrow)
-                break
+        if iq == len(queries) and len(cands[-1]) > 0:
+            res = scoring_fn(cands, quers)
+            for oq, ocands, ores in zip(quers, cands, res):
+                rrow = insert(ores, ocands, oq, rrow)
 
     blackboard.RES_CONN.commit()
     blackboard.META_CONN.commit()
     blackboard.execute(res_cur, "CREATE INDEX IF NOT EXISTS res_qrow_idx ON results (qrow ASC, score DESC);")
     blackboard.execute(res_cur, "CREATE INDEX IF NOT EXISTS res_rrow_idx ON results (rrow ASC);")
     blackboard.execute(m_cur, "CREATE INDEX IF NOT EXISTS m_rrow_idx ON meta (rrow ASC);")
     blackboard.RES_CONN.commit()
```

### Comparing `pepid-1.0.0.post2/pepid/search_node.py` & `pepid-1.1.0/pepid/post_node.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,41 +1,45 @@
 import struct
 import os
 import time
-import sys
 
 if __package__ is None or __package__ == '':
     import blackboard
     import node
+    import pepid_utils
 else:
     from . import blackboard
     from . import node
+    from . import pepid_utils
 
-
-class SearchNode(node.Node):
+class PostNode(node.Node):
     def __init__(self, unix_sock):
         super().__init__(unix_sock)
         self.path = None
         self.messages[0x00] = [None, self.prepare]
-        self.messages[0x01] = ["!QQc", self.do]
+        self.messages[0x01] = [None, self.do]
 
-    def do(self, start, end, _):
-        if __package__ is None or __package__ == '':
-            import search
-        else:
-            from . import search
+    def do(self, msg):
+        start, end = struct.unpack("!QQ", msg[:16])
+
+        post_fn = pepid_utils.import_or(blackboard.config['postsearch']['function'], None)
 
         if not self.path:
             raise ValueError("'do' message received before 'prepare' message, aborting.")
 
-        search.search_core(start, end)
+        if post_fn is not None:
+            post_fn(start, end)
+            blackboard.CONN.commit()
+        else:
+            blackboard.LOG.warning("Could not find postprocessing function '{}', not applying postprocessing".format(blackboard.config['postsearch']['function']))
+            return
 
     def prepare(self, msg):
         lgt = struct.unpack("!I", msg[:4])[0]
-        blackboard.TMP_PATH = struct.unpack("!{}sc".format(lgt), msg[4:])[0].decode('utf-8')
-        self.path = blackboard.TMP_PATH
+        self.path = struct.unpack("!{}sc".format(lgt), msg[4:])[0].decode('utf-8')
+        blackboard.TMP_PATH = self.path
         blackboard.setup_constants()
         blackboard.LOCK = open(os.path.join(blackboard.TMP_PATH, ".lock"), "wb")
         blackboard.prepare_connection()
 
 if __name__ == '__main__':
-    node.init(SearchNode)
+    node.init(PostNode)
```

### Comparing `pepid-1.0.0.post2/pepid/data/default.cfg` & `pepid-1.1.0/pepid/data/default.cfg`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 # Basic workflow:
 # - simultaneous processing (db, query)
 # - simultaneous postprocessing (db, query)
 # - search
+# - postsearch
 # - output (tsv, then report, then rescoring, then final report)
 
 # Format for functions is: importable.module:function_name
 # See below for examples
 
 [performance]
 python = python # path to python/pypy/etc. executable
@@ -20,15 +21,15 @@
 database = database.fasta # input database
 workdir = false # this should be the path to the generated work files' directory if using, else 'false'
 tmpdir = /tmp/ # where to put temporary files
 
 [processing.query]
 enabled = true
 workers = 32
-postprocessing function = my_script.predict_length
+postprocessing function = extensions.stub
 postprocessing workers = 32
 batch size = 1180 # batch size for parallel processing
 max peaks = 9999 # Discard spectra with more than this many peaks
 min peaks = 0 # Discard spectra with fewer than this many peaks
 min mass = 250 # Queries with precursor masses below this level are omitted
 max mass = 6000 # Queries with precursor mass above this level are omitted
 max charge = 4 # Max charge for spectra
@@ -87,14 +88,15 @@
 enabled = true
 workers = 64
 batch size = 23000
 sharding threshold = 1000000 # create a new shard after X (default: 1m) results stored in this shard
 candidate filtering tolerance = -100,100 # left and right side tolerance for candidate filtering previous to search
 filtering unit = ppm
 function = search.xcorr_hyperscore
+candidate filtering function = search.stub_filter
 
 [scoring.xcorr]
 bin resolution = 20 # mass error tolerance for matching peaks
 bin matching unit = ppm # ppm or abs (any non-ppm value assumed to be abs)
 correlation window size = 75 # window size for averaging step in correlation
 norm window count = 10 # how many windows to use for intensity normalization
 intensity cutoff = 0.05 # ignore peaks with intensity less than this times max intensity
@@ -146,27 +148,39 @@
 batch size = 16
 
 [report]
 max scores = 1 # How many scores to retain per spectrum for reporting
 fdr threshold = 0.01 # FDR threshold at which to report passing PSM count
 out = report # output directory for report artifacts
 
+[postsearch]
+# Postprocessing step operating over the search results
+workers = 13
+batch size = 45
+function = extensions.stub
+
 [rescoring]
 function = pepid_percolator.rescore
 suffix = _final # Suffix to use to generate the rescored results filename. Cannot be empty.
-max scores = 10 # Keep only top `max scores` PSMs for each spectrum before training, rescoring and outputting.
 batch size = 1180 # Batch size for rescoring, in spectra
 
 [rescoring.percolator]
 percolator = percolator # point to the percolator executable
-generate pin = true # Whether to reuse existing pin or generate a new one (should be true if max scores in [rescoring] changes for instance)
 pin batch size = 100000
 pin workers = 64
 options = -Y --trainFDR 0.01 --testFDR 0.01 -i 10 # Extra command-line options for percolator binary
 cleanup = false # whether to delete the percolator .pin and .pout output at the end
 
+[misc.tsv_to_pin]
+enabled = true
+use extra = true # Whether to insert the 'extra' metadata (inserted by postprocessors)
+user function = None # Function used to generate extra feature based on the input tsv lines
+max scores = 10 # Keep only top `max scores` PSMs in pin output
+
+
 [pipeline]
 search = true
+postsearch = true
 output = true
 report = true
 rescoring = true
 rescoring report = true
```

### Comparing `pepid-1.0.0.post2/pepid/ml/train_model_sparse.py` & `pepid-1.1.0/pepid/ml/train_best_lgt_model.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,96 +1,37 @@
-import pepid_utils
-
 import torch
 import torch.nn as nn
 from torch.utils.data import Dataset, DataLoader
-from torch.autograd import Variable
 
 import numpy
 import tables
-import pickle as cPickle
-
-import tqdm
+import time
+import json
+import pickle
 
 import os
 import sys
+import itertools
 
-CUDA = True
-
-BATCH_SIZE = 500
-MAX_SIZE = 5000000
-
-INIT_PATIENCE = 999
-
-raw_data = tables.open_file("data/pt_pf_round.h5", 'r')
-
-class MsDataset(Dataset):
-    def __init__(self, data, idxs, max_charge=7, epoch_len=None, theoretical=True, generated=False, shuffle=False):
-        self.data = data
-        self.idxs = idxs
-        numpy.random.shuffle(self.idxs)
-        self.theoretical = theoretical or generated
-        self.generated = generated
-        self.shuffle = shuffle
-        self.len = epoch_len if epoch_len is not None else len(idxs)
-        self.max_charge = max_charge
-
-    def __len__(self):
-        return self.len
-
-    def __getitem__(self, idx):
-        seq = None
-        while seq is None or (len(seq) >= PROT_STR_LEN):
-            idx = numpy.random.choice(len(self.idxs))
-            seq = self.data.root.meta[self.idxs[idx]]['seq'].decode('utf-8')
-            mods = numpy.zeros((len(seq),))
-            mods[seq == '1'] = pepid_utils.MASS_O
-            mods[seq == 'C'] = pepid_utils.MASS_CAM
-            seq = seq.replace('1', 'M')
-        spec = self.data.root.spectrum[self.idxs[idx]]
-        charge = self.data.root.meta[self.idxs[idx]]['charge']
-        mass = self.data.root.meta[self.idxs[idx]]['mass']
-        
-        enc_seq = embed({"pep": seq, "mods": mods, "charge": charge, 'mass': mass})
-          
-        out_set = []
-        out_set.append(torch.FloatTensor(enc_seq))
-        out_set.append(torch.LongTensor([charge-1])) # 0-index the charge...
-        out_set.append(torch.FloatTensor(spec))
-        #out_set[-1] = torch.sqrt(out_set[-1])
-        return tuple(out_set)
-
-def import_all(mod):
-    imp = __import__(mod, fromlist=["Model", "embed", "PROT_BLIT_LEN", "PROT_STR_LEN"])
-    global Model
-    global embed
-    global PROT_BLIT_LEN
-    global PROT_STR_LEN
-    global SEQ_SIZE
-    embed = getattr(imp, "embed")
-    PROT_BLIT_LEN = getattr(imp, "PROT_BLIT_LEN")
-    PROT_STR_LEN = getattr(imp, "PROT_STR_LEN")
-    SEQ_SIZE = getattr(imp, "SEQ_SIZE")
-    Model = getattr(imp, "Model")
-
-def make_run(mod):
-    import_all(mod)
-    model = Model()
-
-    if CUDA:
-        torch.backends.cudnn.enabled = True
-        model.cuda()
+import time
 
-    print(model)
-    #model.load_state_dict(torch.load("ml/{}.pkl".format(mod)))
+from best_lgt_model import *
+import tqdm
 
+MAX_EPOCHS = 10000
+def make_run(data, outdir, args):
     numpy.random.seed(0)
 
-    all_idxs = numpy.arange(len(raw_data.root.meta))
-    unique_peps = numpy.unique(list(map(lambda x: x.decode("utf-8").replace("_", "").replace("M(ox)", "1"), raw_data.root.meta[all_idxs]['seq'])))
+    raw_data = tables.open_file("../data/massive.h5", 'r')
+    #print(raw_data.root.meta[:]['mass'].max())
+
+    #all_idxs = raw_data.root.meta.get_where_list("(score > {}) & (exists > 0.5)".format(SCORE_CUTOFF))
+    #all_idxs = raw_data.root.meta.get_where_list("(exists > 0.5)")
+    all_idxs = numpy.arange(raw_data.root.meta.shape[0])
+    unique_peps = numpy.unique(list(map(lambda x: x.decode('utf-8').replace("_", "").replace("M(ox)", "1"), raw_data.root.meta[all_idxs]['seq'])))
     n_data = unique_peps.shape[0]
     all_pep_idxs = numpy.arange(n_data)
     numpy.random.shuffle(all_pep_idxs)
 
     train_peptides = all_pep_idxs[:int(0.8*len(all_pep_idxs))]
     test_peptides = all_pep_idxs[int(0.8*len(all_pep_idxs)):int(0.9*len(all_pep_idxs))]
     valid_peptides = all_pep_idxs[int(0.9*len(all_pep_idxs)):]
@@ -110,86 +51,100 @@
     valid_idxs = numpy.argwhere(numpy.isin(raw_data_seqs, unique_peps[valid_peptides]))[:,0]
     numpy.random.shuffle(valid_idxs)
     valid_idxs = valid_idxs[:int(all_n * 0.1)]
 
     pep_lengths_tr = list(map(lambda x: len(x.decode('utf-8').replace("_", "").replace("M(ox)", "1")), raw_data.root.meta[idxs]['seq']))
     pep_lengths_va = list(map(lambda x: len(x.decode('utf-8').replace("_", "").replace("M(ox)", "1")), raw_data.root.meta[valid_idxs]['seq']))
     pep_lengths_te = list(map(lambda x: len(x.decode('utf-8').replace("_", "").replace("M(ox)", "1")), raw_data.root.meta[test_idxs]['seq']))
-
     print("Train set size: {}; Valid set size: {}; Test set size: {}".format(len(idxs), len(valid_idxs), len(test_idxs)))
     print("Train lengths: min {} max {}".format(numpy.min(pep_lengths_tr), numpy.max(pep_lengths_tr)))
     print("Valid lengths: min {} max {}".format(numpy.min(pep_lengths_va), numpy.max(pep_lengths_va)))
     print("Test lengths: min {} max {}".format(numpy.min(pep_lengths_te), numpy.max(pep_lengths_te)))
 
-    dataset = MsDataset(raw_data, idxs, epoch_len=None)
-    dataset_test = MsDataset(raw_data, test_idxs, epoch_len=20000)
-    dl = DataLoader(dataset, batch_size=BATCH_SIZE, shuffle=True, num_workers=0, drop_last=True)
-    dl_test = DataLoader(dataset_test, batch_size=BATCH_SIZE, shuffle=True, num_workers=0, drop_last=True)
-
-    loss_fn = torch.nn.CosineSimilarity(dim=-1).cuda()
-    optimizer = torch.optim.Adam(model.parameters(), lr=3e-4)
-
-    patience = INIT_PATIENCE
-    best_loss = float('inf')
-    last_epoch = 200
-    epoch_idx = 0
-
-    prev_sim = 0
-
-    while epoch_idx < last_epoch and patience > 0:
-        loss_value = {'train': 0, 'test': 0}
-        cos_sim = {'train': 0, 'test': 0}
-        sparsity = {'train': 0, 'test': 0}
-
-        for this_dl in (dl, dl_test):
-            phase = 'train' if this_dl is dl else 'test'
-            if this_dl is dl:
-                model.train()
-            else:
-                model.eval()
-            n = 0
-            bar = tqdm.tqdm(enumerate(this_dl), total=len(this_dl))
+    dataset = MsDataset(raw_data, idxs, epoch_len=50000, class_balance=False)
+    dataset_test = MsDataset(raw_data, test_idxs, epoch_len=5000)
+    dl = DataLoader(dataset, batch_size=BATCH_SIZE, shuffle=True, num_workers=1, drop_last=True)
+    dl_test = DataLoader(dataset_test, batch_size=BATCH_SIZE, shuffle=True, num_workers=1, drop_last=True)
+
+    model = Model().cuda()
+    #model.load_state_dict(torch.load("best_nice_chop3.pkl"))
+
+    i = 1
+
+    lgt_prior = numpy.zeros(GT_MAX_LGT - GT_MIN_LGT+1)
+    n_batches = 0
+    eye = numpy.eye(GT_MAX_LGT - GT_MIN_LGT+1)
+    n_classes = (GT_MAX_LGT - GT_MIN_LGT + 1)
+    for batch in dl:
+        lgt_prior += eye[batch[-1].detach().cpu().numpy().reshape((-1,)).astype('int32') - GT_MIN_LGT].mean(axis=0)
+        n_batches += 1
+    lgt_prior /= n_batches
+    lgt_weight = numpy.copy(lgt_prior)
+    lgt_weight[lgt_weight > 0] = 1.0 / (n_classes * lgt_weight[lgt_weight > 0])
+    print(lgt_prior)
+    lgt_prior = torch.FloatTensor(numpy.log(numpy.maximum(1e-10, lgt_prior))).view(1, -1).repeat(BATCH_SIZE, 1).cuda()
+
+    #loss_fn = torch.nn.NLLLoss().cuda()
+    #loss_fn = torch.nn.BCEWithLogitsLoss().cuda()
+    loss_fn = torch.nn.NLLLoss().cuda()
+    weighted_loss_fn = torch.nn.NLLLoss(weight=torch.FloatTensor(lgt_weight)).cuda()
+    #mse_loss = torch.nn.MSELoss().cuda()
+    optimizer = torch.optim.Adam(model.parameters(), lr=1e-3)
+    best = float('inf')
+
+    lgt_cnt = numpy.array([0]*34)
+
+    while i < MAX_EPOCHS:
+        acc = {'train': 0, 'test': 0}
+        acc_rank = {'train': 0, 'test': 0}
+        conv = {'train': 0, 'test': 0}
+        lin = {'train': 0, 'test': 0}
+        meta = {'train': 0, 'test': 0}
+        loss = {'train': 0, 'test': 0}
+        n = {'train': 0, 'test': 0}
+
+        for this_dl, phase in zip([dl, dl_test], ['train', 'test']):
+            bar = tqdm.tqdm(enumerate(this_dl), total=len(this_dl), desc=phase)
+            start_time = time.strftime("%I:%M:%S %p", time.localtime())
             for it, batch in bar:
-                if this_dl is dl:
+                spec, precmass, lgts = batch
+                spec = spec.cuda()
+                lgts = lgts.cuda()
+                precmass = precmass.cuda()
+
+                #lgt_cnt[lgts.cpu().detach().numpy().astype('int32') - OFFSET] += 1
+
+                if phase == 'train':
                     optimizer.zero_grad()
-                seq, charge, spec = batch
-                seq = seq.cuda()
-                spec = spec[:,:PROT_BLIT_LEN].cuda()
-                charge = charge.view(-1).cuda()
-
-                spec = spec.view(-1, spec.shape[-1])
-                pred = model(seq).view(spec.shape[0], -1)
-
-                l_expr = -loss_fn(pred, spec).mean() - loss_fn(pred * (pred >= 1e-3), spec).mean()
-
-                loss_value[phase] += l_expr.data.cpu().numpy()
-                spec_post = spec / torch.norm(spec, p=2, dim=-1, keepdim=True)
-                pred_post = pred / torch.norm(pred, p=2, dim=-1, keepdim=True)
-                cos_sim[phase] += (spec_post * pred_post).sum(dim=-1).mean().detach().cpu().numpy()
 
-                if this_dl is dl:
-                    l_expr.backward(retain_graph=False)
-                    optimizer.step()
+                ret = model(spec.view(-1, PROT_TGT_LEN), precmass)
+                lgts = lgts - OFFSET
 
-                sparsity[phase] += (1.0 - (torch.count_nonzero(pred * (pred >= 1e-3), dim=-1).float() / pred.shape[-1]).mean()).detach().cpu().numpy()
+                loss_expr = weighted_loss_fn(ret['pred'].view(-1, PROT_STR_LEN - OFFSET + 1), lgts.view(-1).long())
+                pre_loss_expr = loss_fn(ret['conv'].view(-1, PROT_STR_LEN - OFFSET + 1), lgts.view(-1).long())
+                wloss_expr = weighted_loss_fn(ret['fc'].view(-1, PROT_STR_LEN - OFFSET + 1), lgts.view(-1).long())
+                mloss_expr = loss_fn(ret['mass'].view(-1, PROT_STR_LEN - OFFSET + 1), lgts.view(-1).long())
+                loss[phase] += loss_expr.data.cpu().numpy()
+                acc[phase] += (ret['pred'].argmax(dim=-1).view(-1) == lgts.view(-1)).float().mean().detach().cpu().numpy()
+                conv[phase] += (ret['conv'].argmax(dim=-1).view(-1) == lgts.view(-1)).float().mean().detach().cpu().numpy()
+                lin[phase] += (ret['fc'].argmax(dim=-1).view(-1) == lgts.view(-1)).float().mean().detach().cpu().numpy()
+                meta[phase] += (ret['mass'].argmax(dim=-1).view(-1) == lgts.view(-1)).float().mean().detach().cpu().numpy()
+                #adhoc[phase] += (out.argmax(dim=-1).view(-1) - lgts.view(-1)).abs().float().mean().detach().cpu().numpy()
+                n[phase] += 1
+
+                if phase == 'train':
+                    (pre_loss_expr + loss_expr + wloss_expr + mloss_expr).backward()
+                    #pre_loss_expr.backward()
+                    optimizer.step()
 
-                n += 1
+                bar.set_description("[{}] Epoch {} ({}): ".format(start_time, i, phase) + \
+                                "loss: {:.3f} (acc: {:.3f}; conv: {:.3f}, lin: {:.3f}, meta: {:.3f})".format(loss[phase] / max(1, n[phase]), acc[phase] / max(1, n[phase]), conv[phase] / max(1, n[phase]), lin[phase] / max(1, n[phase]), meta[phase] / max(1, n[phase])))
 
-                bar.set_description("[{}] {}: {:.3f} -> L:{:.3f} S:{:.3f}".format(epoch_idx, "T{}ing".format(phase[1:]), cos_sim[phase] / max(n, 1), loss_value[phase] / max(n, 1), sparsity[phase] / max(n, 1)))
+        if loss['test'] / n['test'] < best:
+            best = loss['test'] / n['test']
+            model.save("best_lgt_model.pkl")
+        model.save("latest_lgt_model.pkl")
 
-            loss_value[phase] /= n
-            cos_sim[phase] /= n
-            sparsity[phase] /= n
-
-        prev_sim = cos_sim['test']
-
-        if loss_value['test'] < best_loss:
-            best_loss = loss_value['test']
-            model.save("ml/{}.pkl".format(mod))
-            patience = INIT_PATIENCE
-        else:
-            patience -= 1
- 
-        epoch_idx += 1
+        i += 1
 
 if __name__ == '__main__':
-    make_run(sys.argv[1])
+    make_run(None, None, None)
```

### Comparing `pepid-1.0.0.post2/LICENSE.md` & `pepid-1.1.0/LICENSE.md`

 * *Files identical despite different names*

### Comparing `pepid-1.0.0.post2/README.md` & `pepid-1.1.0/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -1,25 +1,31 @@
 # Pepid: Research-Oriented, Highly Configurable Peptide Search Engine
 
 ## Quickstart
 
-An example config is provided in data/default.cfg: it should be copied somewhere and modified to suit user preferences (keys not filled in the user file are taken from the default config).
+An example config is provided in data/default.cfg: it should be copied somewhere and modified to suit user preferences (keys not filled in the user file are taken from the default config). Example templates suited for ProteomeTools and the One Hour Yeast Proteome are provided in the main distribution (`example_{proteometools,yeast}.cfg`). An example pipeline using all the custom deep learning primitives in Pepid is also provided for evaluation (`example_proteometools_ml.cfg`).
 
 ```
-python pepid.py <config.cfg>
+python main.py <config.cfg>
 ```
 
-Will run pepid. There are no command line arguments, all configuration is done through the configuration script. This makes tracking experimental details much easier. Pepid can also be run programmatically as follows:
+Will run pepid if executed in the pepid source directory. There are no command line arguments except the configuration filename, all configuration is done through the configuration script. This makes tracking experimental details much easier. Pepid can also be run programmatically as follows:
 
 ```
 import pepid
 pepid.run(<config.cfg>)
 ```
 
-In addition to its default search capabilities, pepid provides two utility scripts: `pepid_files.py <config.cfg> filetype` will output the paths to files matching a certain pepid artifact type (`report` will give the path to all normal report artifacts). `pepid_compare.py <config.cfg> <analysis1.pkl> <analysis2.pkl>` will plot two analyses on the same graph for easier comparative analysis. It can be used to compare results before/after rescoring, or to compare between two scoring methods, etc.
+Or as a module:
+
+```
+python -mpepid <config.cfg>
+```
+
+In addition to its default search capabilities, pepid provides some utility scripts: `pepid_files.py <config.cfg> filetype` will output the paths to files matching a certain pepid artifact type (`report` will give the path to all normal report artifacts). `pepid_compare.py <config.cfg> <analysis1.pkl> <analysis2.pkl>` will plot two analyses on the same graph for easier comparative analysis. It can be used to compare results before/after rescoring, or to compare between two scoring methods, etc. `pepid_mgf_meta.py <config.cfg> key` will insert the text of the key in the input MGF file into the query database's metadata field. This can be used for downstream analysis or external evaluation, such as adding the ground truth peptide in a dataset that has such data for FDP evaluation.
 
 IMPORTANT:
 
 - Pepid relies on numpy for some operations, which in turn relies on a platform BLAS implementation for efficiency. This may result, if running pepid in parallel, in exhausting resource limits (e.g. RLIMIT\_NPROC on linux). This can be avoided by setting the right environment variables, at the likely cost of performance (for example: OMP\_NUM\_THREADS=1), or by reducing the amount of processes running in parallel.
 - The pypi package does not contain the pretrained deep learning models, those have to be obtained separately (either trained locally or downloaded from the github repository at https://github.com/lemieux-lab/pepid)
 
 ## Why Pepid?
@@ -68,9 +74,12 @@
 Pepid also outputs a graphical report that can be used to quickly ascertain the quality of the search results, and helps identify potential sources of bias (such as the well-known peptide length bias in the Xcorr and Hyperscore functions). In addition, pepid offers a utility called `pepid_compare.py` which can be used to plot two different analyses on the same graph for comparison. The output of `pepid_compare.py` to examine rescoring by Percolator is shown below.
 
 ![Pepid with Xcorr on the 1h yeast proteome data (batched runs), comparing before and after rescoring by percolator](https://raw.githubusercontent.com/lemieux-lab/pepid/master/images/plot_compare_output_rescored.svg)
 
 ## State of the Art Features
 
 Experimental deep learning-based features are available for experimentation. Future releases will include better supported use of those features.
+Pepid includes a peptide length prediction module that can be enabled by adding extensions.predict\_length in preprocessing and extensions.postprocess\_for\_length in postprocessing, a rescoring algorithm based on a pretrained ground truth separation paradigm trained on Massive-KB along with a finetuning phase for experimental condition correction, and a whole-spectrum prediction algorithm similar to PredFull.
+
+## Citing
 
 See upcoming paper for more details.
```

### Comparing `pepid-1.0.0.post2/pyproject.toml` & `pepid-1.1.0/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -15,27 +15,28 @@
     "pepid/ml/train_model_ci.py",
     "pepid/ml/train_model_out.py",
 
     #"pepid/ml/spectrum_generator.pkl",
     #"pepid/ml/spectrum_generator_ci.pkl",
     #"pepid/ml/spectrum_generator_out.pkl",
     "pepid/ml/*.pkl",
+    "pepid/ml_old/*",
 
     "pepid/old_search.py",
-    "pepid/gen_fdp*",
 ]
 include = [
     "pepid/*.py",
+    "pepid/example_*.cfg",
 
     "pepid/data/default.cfg",
     "pepid/ml/*",
 ]
 
 [project]
-version = "1.0.0-2"
+version = "1.1.0"
 name = "pepid"
 authors = [
     { name="Jeremie Zumer", email="jeremie.zumer@umontreal.ca" },
 ]
 description = "Pepid: a Highly Modifiable, Bioinformatics-Oriented Peptide Search Engine"
 readme = "README.md"
 requires-python = ">=3.7"
```

### Comparing `pepid-1.0.0.post2/PKG-INFO` & `pepid-1.1.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pepid
-Version: 1.0.0.post2
+Version: 1.1.0
 Summary: Pepid: a Highly Modifiable, Bioinformatics-Oriented Peptide Search Engine
 Project-URL: Homepage, https://github.com/lemieux-lab/pepid
 Project-URL: Bug Tracker, https://github.com/lemieux-lab/pepid/issues
 Author-email: Jeremie Zumer <jeremie.zumer@umontreal.ca>
 License-File: LICENSE.md
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
@@ -16,28 +16,34 @@
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 
 # Pepid: Research-Oriented, Highly Configurable Peptide Search Engine
 
 ## Quickstart
 
-An example config is provided in data/default.cfg: it should be copied somewhere and modified to suit user preferences (keys not filled in the user file are taken from the default config).
+An example config is provided in data/default.cfg: it should be copied somewhere and modified to suit user preferences (keys not filled in the user file are taken from the default config). Example templates suited for ProteomeTools and the One Hour Yeast Proteome are provided in the main distribution (`example_{proteometools,yeast}.cfg`). An example pipeline using all the custom deep learning primitives in Pepid is also provided for evaluation (`example_proteometools_ml.cfg`).
 
 ```
-python pepid.py <config.cfg>
+python main.py <config.cfg>
 ```
 
-Will run pepid. There are no command line arguments, all configuration is done through the configuration script. This makes tracking experimental details much easier. Pepid can also be run programmatically as follows:
+Will run pepid if executed in the pepid source directory. There are no command line arguments except the configuration filename, all configuration is done through the configuration script. This makes tracking experimental details much easier. Pepid can also be run programmatically as follows:
 
 ```
 import pepid
 pepid.run(<config.cfg>)
 ```
 
-In addition to its default search capabilities, pepid provides two utility scripts: `pepid_files.py <config.cfg> filetype` will output the paths to files matching a certain pepid artifact type (`report` will give the path to all normal report artifacts). `pepid_compare.py <config.cfg> <analysis1.pkl> <analysis2.pkl>` will plot two analyses on the same graph for easier comparative analysis. It can be used to compare results before/after rescoring, or to compare between two scoring methods, etc.
+Or as a module:
+
+```
+python -mpepid <config.cfg>
+```
+
+In addition to its default search capabilities, pepid provides some utility scripts: `pepid_files.py <config.cfg> filetype` will output the paths to files matching a certain pepid artifact type (`report` will give the path to all normal report artifacts). `pepid_compare.py <config.cfg> <analysis1.pkl> <analysis2.pkl>` will plot two analyses on the same graph for easier comparative analysis. It can be used to compare results before/after rescoring, or to compare between two scoring methods, etc. `pepid_mgf_meta.py <config.cfg> key` will insert the text of the key in the input MGF file into the query database's metadata field. This can be used for downstream analysis or external evaluation, such as adding the ground truth peptide in a dataset that has such data for FDP evaluation.
 
 IMPORTANT:
 
 - Pepid relies on numpy for some operations, which in turn relies on a platform BLAS implementation for efficiency. This may result, if running pepid in parallel, in exhausting resource limits (e.g. RLIMIT\_NPROC on linux). This can be avoided by setting the right environment variables, at the likely cost of performance (for example: OMP\_NUM\_THREADS=1), or by reducing the amount of processes running in parallel.
 - The pypi package does not contain the pretrained deep learning models, those have to be obtained separately (either trained locally or downloaded from the github repository at https://github.com/lemieux-lab/pepid)
 
 ## Why Pepid?
@@ -86,9 +92,12 @@
 Pepid also outputs a graphical report that can be used to quickly ascertain the quality of the search results, and helps identify potential sources of bias (such as the well-known peptide length bias in the Xcorr and Hyperscore functions). In addition, pepid offers a utility called `pepid_compare.py` which can be used to plot two different analyses on the same graph for comparison. The output of `pepid_compare.py` to examine rescoring by Percolator is shown below.
 
 ![Pepid with Xcorr on the 1h yeast proteome data (batched runs), comparing before and after rescoring by percolator](https://raw.githubusercontent.com/lemieux-lab/pepid/master/images/plot_compare_output_rescored.svg)
 
 ## State of the Art Features
 
 Experimental deep learning-based features are available for experimentation. Future releases will include better supported use of those features.
+Pepid includes a peptide length prediction module that can be enabled by adding extensions.predict\_length in preprocessing and extensions.postprocess\_for\_length in postprocessing, a rescoring algorithm based on a pretrained ground truth separation paradigm trained on Massive-KB along with a finetuning phase for experimental condition correction, and a whole-spectrum prediction algorithm similar to PredFull.
+
+## Citing
 
 See upcoming paper for more details.
```

