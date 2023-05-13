# Comparing `tmp/pii-transform-0.5.0.tar.gz` & `tmp/pii-transform-0.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pii-transform-0.5.0.tar", last modified: Wed May 10 18:10:32 2023, max compression
+gzip compressed data, was "pii-transform-0.5.1.tar", last modified: Fri May 12 20:59:06 2023, max compression
```

## Comparing `pii-transform-0.5.0.tar` & `pii-transform-0.5.1.tar`

### file list

```diff
@@ -1,44 +1,44 @@
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.893382 pii-transform-0.5.0/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)    11357 2021-11-20 15:10:50.000000 pii-transform-0.5.0/LICENSE
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       79 2023-01-22 18:11:59.000000 pii-transform-0.5.0/MANIFEST.in
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2114 2023-05-10 18:10:32.893382 pii-transform-0.5.0/PKG-INFO
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1938 2023-05-10 18:08:53.000000 pii-transform-0.5.0/README.md
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       61 2023-05-10 18:08:53.000000 pii-transform-0.5.0/requirements.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-05-10 18:10:32.893382 pii-transform-0.5.0/setup.cfg
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2765 2023-05-10 18:08:53.000000 pii-transform-0.5.0/setup.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.889382 pii-transform-0.5.0/src/
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.889382 pii-transform-0.5.0/src/pii_transform/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       18 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.893382 pii-transform-0.5.0/src/pii_transform/api/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-01-22 18:11:59.000000 pii-transform-0.5.0/src/pii_transform/api/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.893382 pii-transform-0.5.0/src/pii_transform/api/e2e/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      243 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/api/e2e/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       90 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/api/e2e/defs.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4792 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/api/e2e/document.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     6076 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/api/e2e/multilang.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3480 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/api/e2e/textchunk.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3314 2023-03-30 21:45:31.000000 pii-transform-0.5.0/src/pii_transform/api/transform.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.893382 pii-transform-0.5.0/src/pii_transform/app/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-22 18:11:59.000000 pii-transform-0.5.0/src/pii_transform/app/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      526 2023-05-10 07:37:04.000000 pii-transform-0.5.0/src/pii_transform/app/chunk.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4569 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/app/multi.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3116 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/app/process.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2859 2023-01-22 18:11:59.000000 pii-transform-0.5.0/src/pii_transform/app/transform.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      128 2023-03-17 20:33:13.000000 pii-transform-0.5.0/src/pii_transform/defs.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.893382 pii-transform-0.5.0/src/pii_transform/helper/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       47 2023-01-22 18:11:59.000000 pii-transform-0.5.0/src/pii_transform/helper/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1810 2023-01-23 19:30:15.000000 pii-transform-0.5.0/src/pii_transform/helper/logger.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1018 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/helper/misc.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     3965 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/helper/placeholder.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     5655 2023-05-10 18:08:53.000000 pii-transform-0.5.0/src/pii_transform/helper/substitution.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     5078 2023-04-22 10:24:37.000000 pii-transform-0.5.0/src/pii_transform/helper/synthetic.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.893382 pii-transform-0.5.0/src/pii_transform/resources/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1412 2023-03-17 20:33:13.000000 pii-transform-0.5.0/src/pii_transform/resources/placeholder.json
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       73 2023-03-05 21:06:11.000000 pii-transform-0.5.0/src/pii_transform/resources/transform.json
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:32.893382 pii-transform-0.5.0/src/pii_transform.egg-info/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2114 2023-05-10 18:10:32.000000 pii-transform-0.5.0/src/pii_transform.egg-info/PKG-INFO
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1092 2023-05-10 18:10:32.000000 pii-transform-0.5.0/src/pii_transform.egg-info/SOURCES.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-05-10 18:10:32.000000 pii-transform-0.5.0/src/pii_transform.egg-info/dependency_links.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      161 2023-05-10 18:10:32.000000 pii-transform-0.5.0/src/pii_transform.egg-info/entry_points.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       82 2023-05-10 18:10:32.000000 pii-transform-0.5.0/src/pii_transform.egg-info/requires.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       14 2023-05-10 18:10:32.000000 pii-transform-0.5.0/src/pii_transform.egg-info/top_level.txt
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.169272 pii-transform-0.5.1/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)    11357 2021-11-20 15:10:50.000000 pii-transform-0.5.1/LICENSE
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       79 2023-01-22 18:11:59.000000 pii-transform-0.5.1/MANIFEST.in
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2114 2023-05-12 20:59:06.169272 pii-transform-0.5.1/PKG-INFO
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1938 2023-05-10 18:08:53.000000 pii-transform-0.5.1/README.md
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       61 2023-05-10 18:08:53.000000 pii-transform-0.5.1/requirements.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-05-12 20:59:06.169272 pii-transform-0.5.1/setup.cfg
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2765 2023-05-10 18:08:53.000000 pii-transform-0.5.1/setup.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.165272 pii-transform-0.5.1/src/
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.165272 pii-transform-0.5.1/src/pii_transform/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       18 2023-05-12 20:55:50.000000 pii-transform-0.5.1/src/pii_transform/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.165272 pii-transform-0.5.1/src/pii_transform/api/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-01-22 18:11:59.000000 pii-transform-0.5.1/src/pii_transform/api/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.165272 pii-transform-0.5.1/src/pii_transform/api/e2e/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      243 2023-05-10 18:08:53.000000 pii-transform-0.5.1/src/pii_transform/api/e2e/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       90 2023-05-12 20:55:50.000000 pii-transform-0.5.1/src/pii_transform/api/e2e/defs.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     4808 2023-05-12 20:55:50.000000 pii-transform-0.5.1/src/pii_transform/api/e2e/document.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     6092 2023-05-12 20:55:50.000000 pii-transform-0.5.1/src/pii_transform/api/e2e/multilang.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3496 2023-05-12 20:55:50.000000 pii-transform-0.5.1/src/pii_transform/api/e2e/textchunk.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3314 2023-03-30 21:45:31.000000 pii-transform-0.5.1/src/pii_transform/api/transform.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.165272 pii-transform-0.5.1/src/pii_transform/app/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-22 18:11:59.000000 pii-transform-0.5.1/src/pii_transform/app/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      526 2023-05-10 07:37:04.000000 pii-transform-0.5.1/src/pii_transform/app/chunk.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     4563 2023-05-12 20:55:50.000000 pii-transform-0.5.1/src/pii_transform/app/multi.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3116 2023-05-10 18:08:53.000000 pii-transform-0.5.1/src/pii_transform/app/process.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2859 2023-01-22 18:11:59.000000 pii-transform-0.5.1/src/pii_transform/app/transform.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      128 2023-03-17 20:33:13.000000 pii-transform-0.5.1/src/pii_transform/defs.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.169272 pii-transform-0.5.1/src/pii_transform/helper/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       47 2023-01-22 18:11:59.000000 pii-transform-0.5.1/src/pii_transform/helper/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1810 2023-01-23 19:30:15.000000 pii-transform-0.5.1/src/pii_transform/helper/logger.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1018 2023-05-10 18:08:53.000000 pii-transform-0.5.1/src/pii_transform/helper/misc.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     3965 2023-05-10 18:08:53.000000 pii-transform-0.5.1/src/pii_transform/helper/placeholder.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     5655 2023-05-10 18:08:53.000000 pii-transform-0.5.1/src/pii_transform/helper/substitution.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     5078 2023-04-22 10:24:37.000000 pii-transform-0.5.1/src/pii_transform/helper/synthetic.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.169272 pii-transform-0.5.1/src/pii_transform/resources/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1412 2023-03-17 20:33:13.000000 pii-transform-0.5.1/src/pii_transform/resources/placeholder.json
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       73 2023-03-05 21:06:11.000000 pii-transform-0.5.1/src/pii_transform/resources/transform.json
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-12 20:59:06.165272 pii-transform-0.5.1/src/pii_transform.egg-info/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2114 2023-05-12 20:59:06.000000 pii-transform-0.5.1/src/pii_transform.egg-info/PKG-INFO
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1092 2023-05-12 20:59:06.000000 pii-transform-0.5.1/src/pii_transform.egg-info/SOURCES.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-05-12 20:59:06.000000 pii-transform-0.5.1/src/pii_transform.egg-info/dependency_links.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      161 2023-05-12 20:59:06.000000 pii-transform-0.5.1/src/pii_transform.egg-info/entry_points.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       82 2023-05-12 20:59:06.000000 pii-transform-0.5.1/src/pii_transform.egg-info/requires.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       14 2023-05-12 20:59:06.000000 pii-transform-0.5.1/src/pii_transform.egg-info/top_level.txt
```

### Comparing `pii-transform-0.5.0/LICENSE` & `pii-transform-0.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/PKG-INFO` & `pii-transform-0.5.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pii-transform
-Version: 0.5.0
+Version: 0.5.1
 Summary: Transform recognized PII instances in a document
 Home-page: https://github.com/piisa/pii-transform
-Download-URL: https://github.com/piisa/pii-transform/tarball/v0.5.0
+Download-URL: https://github.com/piisa/pii-transform/tarball/v0.5.1
 Author: Paulo Villegas
 Author-email: paulo.vllgs@gmail.com
 License: Apache
 Keywords: PIISA, PII
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Development Status :: 4 - Beta
```

### Comparing `pii-transform-0.5.0/README.md` & `pii-transform-0.5.1/README.md`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/setup.py` & `pii-transform-0.5.1/setup.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/api/e2e/document.py` & `pii-transform-0.5.1/src/pii_transform/api/e2e/document.py`

 * *Files 1% similar despite different names*

```diff
@@ -103,15 +103,15 @@
     meta = doc.metadata
     lang = meta.get("main_lang") or meta.get("lang") or lang
     if not lang:
         raise InvArgException("no language defined in options or document")
 
     # Create a PiiProcessor object for PII detection
     log(". Loading task processor")
-    proc = PiiProcessor(debug=verbose > 1, config=config)
+    proc = PiiProcessor(debug=verbose > 1, languages=lang, config=config)
 
     # Build the task objects
     log(". Building task objects")
     proc.build_tasks(lang, country, pii=tasks)
     if show_tasks:
         print_tasks(lang, proc, sys.stdout)
```

### Comparing `pii-transform-0.5.0/src/pii_transform/api/e2e/multilang.py` & `pii-transform-0.5.1/src/pii_transform/api/e2e/multilang.py`

 * *Files 2% similar despite different names*

```diff
@@ -72,15 +72,15 @@
         }
 
         self.lang = lang
         self.config = load_config(config or [])
         self.policy = default_policy
 
         # Build detectors
-        self._proc = PiiProcessor(config=self.config, debug=debug)
+        self._proc = PiiProcessor(config=self.config, languages=lang, debug=debug)
         num = 0
         for lng in lang:
             ctr = country[lng] if isinstance(country, dict) else country
             self._log(". build-tasks for: %s", lng)
             num += self._proc.build_tasks(lang=lng, country=ctr, pii=tasks)
         self.num_tasks = num
```

### Comparing `pii-transform-0.5.0/src/pii_transform/api/e2e/textchunk.py` & `pii-transform-0.5.1/src/pii_transform/api/e2e/textchunk.py`

 * *Files 2% similar despite different names*

```diff
@@ -48,15 +48,15 @@
         elif Version(PII_EXTRACT_VERSION) < Version(defs.MIN_PII_EXTRACT_VERSION):
             raise ProcException("incompatible pii-extract-base version {}",
                                 PII_EXTRACT_VERSION)
         self._cid = 0
         self.config = load_config(config or [])
         self.lang = lang
         self.policy = default_policy
-        self.proc = PiiProcessor(config=self.config, debug=debug)
+        self.proc = PiiProcessor(config=self.config, languages=lang, debug=debug)
         self.proc.build_tasks(lang=lang, country=country, pii=tasks)
         self.trf = PiiTransformer(default_policy=default_policy,
                                   config=self.config, debug=debug)
 
 
     def __repr__(self) -> str:
         return f"<PiiTextProcessor [{self.policy}]>"
```

### Comparing `pii-transform-0.5.0/src/pii_transform/api/transform.py` & `pii-transform-0.5.1/src/pii_transform/api/transform.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/app/chunk.py` & `pii-transform-0.5.1/src/pii_transform/app/chunk.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/app/multi.py` & `pii-transform-0.5.1/src/pii_transform/app/multi.py`

 * *Files 0% similar despite different names*

```diff
@@ -20,15 +20,15 @@
     g0 = parser.add_argument_group("Input/output paths")
     g0.add_argument("infile", help="JSONL source file")
     g0.add_argument("outfile", help="JSONL destination file")
     g0.add_argument("--out-piic", metavar="OUTFILE",
                     help="output all detected PII instances")
 
     g1 = parser.add_argument_group("Language & data specification")
-    g1.add_argument("--lang", nargs='+', default=["en", "es"],
+    g1.add_argument("--lang", nargs='+', default=["en"],
                     help="processing languages (default: %(default)s)")
     g1.add_argument("--field-lang", nargs="+", default=("lang", "language"),
                     help="document field defining the language (default: %(default)s)")
     g1.add_argument("--field-text", default=("text",), nargs="+",
                     help="document field containing the text data (default: %(default)s)")
```

### Comparing `pii-transform-0.5.0/src/pii_transform/app/process.py` & `pii-transform-0.5.1/src/pii_transform/app/process.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/app/transform.py` & `pii-transform-0.5.1/src/pii_transform/app/transform.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/helper/logger.py` & `pii-transform-0.5.1/src/pii_transform/helper/logger.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/helper/misc.py` & `pii-transform-0.5.1/src/pii_transform/helper/misc.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/helper/placeholder.py` & `pii-transform-0.5.1/src/pii_transform/helper/placeholder.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/helper/substitution.py` & `pii-transform-0.5.1/src/pii_transform/helper/substitution.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/helper/synthetic.py` & `pii-transform-0.5.1/src/pii_transform/helper/synthetic.py`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform/resources/placeholder.json` & `pii-transform-0.5.1/src/pii_transform/resources/placeholder.json`

 * *Files identical despite different names*

### Comparing `pii-transform-0.5.0/src/pii_transform.egg-info/PKG-INFO` & `pii-transform-0.5.1/src/pii_transform.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pii-transform
-Version: 0.5.0
+Version: 0.5.1
 Summary: Transform recognized PII instances in a document
 Home-page: https://github.com/piisa/pii-transform
-Download-URL: https://github.com/piisa/pii-transform/tarball/v0.5.0
+Download-URL: https://github.com/piisa/pii-transform/tarball/v0.5.1
 Author: Paulo Villegas
 Author-email: paulo.vllgs@gmail.com
 License: Apache
 Keywords: PIISA, PII
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Development Status :: 4 - Beta
```

### Comparing `pii-transform-0.5.0/src/pii_transform.egg-info/SOURCES.txt` & `pii-transform-0.5.1/src/pii_transform.egg-info/SOURCES.txt`

 * *Files identical despite different names*

