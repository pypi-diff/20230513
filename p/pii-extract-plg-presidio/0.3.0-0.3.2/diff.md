# Comparing `tmp/pii-extract-plg-presidio-0.3.0.tar.gz` & `tmp/pii-extract-plg-presidio-0.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pii-extract-plg-presidio-0.3.0.tar", last modified: Wed May 10 18:10:16 2023, max compression
+gzip compressed data, was "pii-extract-plg-presidio-0.3.2.tar", last modified: Sat May 13 09:18:18 2023, max compression
```

## Comparing `pii-extract-plg-presidio-0.3.0.tar` & `pii-extract-plg-presidio-0.3.2.tar`

### file list

```diff
@@ -1,31 +1,31 @@
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)    11357 2021-11-20 15:10:50.000000 pii-extract-plg-presidio-0.3.0/LICENSE
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       79 2023-01-23 13:23:53.000000 pii-extract-plg-presidio-0.3.0/MANIFEST.in
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4227 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/PKG-INFO
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4298 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/README.md
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       89 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/requirements.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/setup.cfg
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2749 2023-01-23 13:23:53.000000 pii-extract-plg-presidio-0.3.0/setup.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/src/
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       18 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/__init__.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/app/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 13:23:53.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/app/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     6387 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/app/info.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      431 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/defs.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2391 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/plugin_loader.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/resources/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     1591 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/resources/plugin-config.json
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      124 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/__init__.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2309 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/analyzer.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     2968 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/collector.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4952 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/task.py
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      716 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/utils.py
-drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-10 18:10:16.325338 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/
--rw-rw-r--   0 paulo     (1000) paulo     (1000)     4227 2023-05-10 18:10:16.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/PKG-INFO
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      861 2023-05-10 18:10:16.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/SOURCES.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-05-10 18:10:16.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/dependency_links.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      197 2023-05-10 18:10:16.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/entry_points.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)      109 2023-05-10 18:10:16.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/requires.txt
--rw-rw-r--   0 paulo     (1000) paulo     (1000)       25 2023-05-10 18:10:16.000000 pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/top_level.txt
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-13 09:18:18.138916 pii-extract-plg-presidio-0.3.2/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)    11357 2021-11-20 15:10:50.000000 pii-extract-plg-presidio-0.3.2/LICENSE
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       79 2023-01-23 13:23:53.000000 pii-extract-plg-presidio-0.3.2/MANIFEST.in
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     4651 2023-05-13 09:18:18.138916 pii-extract-plg-presidio-0.3.2/PKG-INFO
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     4724 2023-05-13 09:12:49.000000 pii-extract-plg-presidio-0.3.2/README.md
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       89 2023-05-12 20:53:14.000000 pii-extract-plg-presidio-0.3.2/requirements.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       38 2023-05-13 09:18:18.138916 pii-extract-plg-presidio-0.3.2/setup.cfg
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2749 2023-01-23 13:23:53.000000 pii-extract-plg-presidio-0.3.2/setup.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-13 09:18:18.134916 pii-extract-plg-presidio-0.3.2/src/
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-13 09:18:18.134916 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       18 2023-05-13 09:12:49.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/__init__.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-13 09:18:18.138916 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/app/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        0 2023-01-23 13:23:53.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/app/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     6537 2023-05-13 09:12:49.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/app/info.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      431 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/defs.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2440 2023-05-12 20:53:14.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/plugin_loader.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-13 09:18:18.138916 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/resources/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     1591 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/resources/plugin-config.json
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-13 09:18:18.138916 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      124 2023-05-10 16:29:55.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/__init__.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2632 2023-05-13 09:12:49.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/analyzer.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     2993 2023-05-13 09:12:49.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/collector.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     5143 2023-05-12 20:53:14.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/task.py
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      716 2023-05-11 09:27:22.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/utils.py
+drwxrwxr-x   0 paulo     (1000) paulo     (1000)        0 2023-05-13 09:18:18.138916 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)     4651 2023-05-13 09:18:18.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/PKG-INFO
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      861 2023-05-13 09:18:18.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/SOURCES.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)        1 2023-05-13 09:18:18.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/dependency_links.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      197 2023-05-13 09:18:18.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/entry_points.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)      109 2023-05-13 09:18:18.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/requires.txt
+-rw-rw-r--   0 paulo     (1000) paulo     (1000)       25 2023-05-13 09:18:18.000000 pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/top_level.txt
```

### Comparing `pii-extract-plg-presidio-0.3.0/LICENSE` & `pii-extract-plg-presidio-0.3.2/LICENSE`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-presidio-0.3.0/PKG-INFO` & `pii-extract-plg-presidio-0.3.2/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pii-extract-plg-presidio
-Version: 0.3.0
+Version: 0.3.2
 Summary: Presidio plugin for PII detection
 Home-page: https://github.com/piisa/pii-extract-plg-presidio
-Download-URL: https://github.com/piisa/pii-extract-plg-presidio/tarball/v0.3.0
+Download-URL: https://github.com/piisa/pii-extract-plg-presidio/tarball/v0.3.2
 Author: Paulo Villegas
 Author-email: paulo.vllgs@gmail.com
 License: Apache
 Keywords: PIISA, PII
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Development Status :: 4 - Beta
@@ -55,35 +55,45 @@
    `nlp_config` element in the plugin configuration file must be
    adjusted accordingly.
 
 
 ## Usage
 
 The package does not have any user-facing entry points (except for one console
-script `pii-extract-presidio-info`, which provides information about its
-capabilities).
+information script, see below(#info-script)). Instead, upon installation it
+defines a plugin entry point. This plugin is automatically picked up by the
+scripts and classes in pii-extract-base, and thus its functionality is exposed
+to them.
 
-Instead, upon installation it defines a plugin entry point. This plugin is
-automatically picked up by executing scripts and classes in pii-extract-base,
-and thus its functionality is exposed to it.
-
-Runtime behaviour is governed by a configuration file, which sets up what
-recognizers from Presidio will be instantiated and used. Note that the
+Runtime behaviour is governed by a configuration file, which sets up which
+recognizers from Presidio will be instantiated and used (note that the
 configuration defines which languages are available for detection, but the
-plugin can also be initialized with a _subset_ of those languages.
+plugin can also be initialized with a _subset_ of those languages).
 
 The task created from the plugin is a standard PII task object, using the
 `pii_extract.build.task.MultiPiiTask` class definition. It will be called,
 as all PII task objects, with a `DocumentChunk` object containing the data to
 analyze. The chunk **must** contain language specification in its metadata, so
 that Presidio knows which language to use (unless the plugin task has been
 built with *only one* language; in that case if the chunk does not contain
 a language specification, it will use that single language).
 
 
+## info script
+
+`pii-extract-presidio-info` is a command-line script  which provides
+information about the plugin capabilities: 
+  * `version`: installed package versions
+  * `presidio-recognizers`: list of recognizers in Presidio
+  * `presidio-entities`: the total list of entities Presidio can generate
+  * `pii-entities`: the PIISA tasks that this plugin will create, by translating
+	from the entities detected by Presidio (this depends on the PIISA config
+	used)
+
+
 ## Building
 
 The provided Makefile can be used to process the package:
  * `make pkg` will build the Python package, creating a file that can be
    installed with `pip`
  * `make unit` will launch all unit tests (using pytest, so pytest must be
    available)
```

### Comparing `pii-extract-plg-presidio-0.3.0/README.md` & `pii-extract-plg-presidio-0.3.2/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -36,35 +36,45 @@
    `nlp_config` element in the plugin [configuration file] must be
    adjusted accordingly.
 
 
 ## Usage
 
 The package does not have any user-facing entry points (except for one console
-script `pii-extract-presidio-info`, which provides information about its
-capabilities).
+information script, see [below](#info-script)). Instead, upon installation it
+defines a plugin entry point. This plugin is automatically picked up by the
+scripts and classes in [pii-extract-base], and thus its functionality is exposed
+to them.
 
-Instead, upon installation it defines a plugin entry point. This plugin is
-automatically picked up by executing scripts and classes in [pii-extract-base],
-and thus its functionality is exposed to it.
-
-Runtime behaviour is governed by a [configuration file], which sets up what
-recognizers from Presidio will be instantiated and used. Note that the
+Runtime behaviour is governed by a [configuration file], which sets up which
+recognizers from Presidio will be instantiated and used (note that the
 configuration defines which languages are available for detection, but the
-plugin can also be initialized with a _subset_ of those languages.
+plugin can also be initialized with a _subset_ of those languages).
 
 The task created from the plugin is a standard [PII task] object, using the
 `pii_extract.build.task.MultiPiiTask` class definition. It will be called,
 as all PII task objects, with a `DocumentChunk` object containing the data to
 analyze. The chunk **must** contain language specification in its metadata, so
 that Presidio knows which language to use (unless the plugin task has been
 built with *only one* language; in that case if the chunk does not contain
 a language specification, it will use that single language).
 
 
+## info script
+
+`pii-extract-presidio-info` is a command-line script  which provides
+information about the plugin capabilities: 
+  * `version`: installed package versions
+  * `presidio-recognizers`: list of recognizers in Presidio
+  * `presidio-entities`: the total list of entities Presidio can generate
+  * `pii-entities`: the PIISA tasks that this plugin will create, by translating
+	from the entities detected by Presidio (this depends on the PIISA config
+	used)
+
+
 ## Building
 
 The provided [Makefile] can be used to process the package:
  * `make pkg` will build the Python package, creating a file that can be
    installed with `pip`
  * `make unit` will launch all unit tests (using [pytest], so pytest must be
    available)
```

### Comparing `pii-extract-plg-presidio-0.3.0/setup.py` & `pii-extract-plg-presidio-0.3.2/setup.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/app/info.py` & `pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/app/info.py`

 * *Files 12% similar despite different names*

```diff
@@ -9,35 +9,40 @@
 from typing import List, TextIO
 
 from presidio_analyzer import RemoteRecognizer, PatternRecognizer
 
 from pii_data import VERSION as VERSION_DATA
 from pii_data.helper.exception import ProcException
 from pii_extract import VERSION as VERSION_EXTRACT
-from pii_extract.gather.parser import parse_task_descriptor, RawTaskDefaults
-from pii_extract.build.collection.task_collection import filter_piid
+from pii_extract.gather.parser import parse_task_descriptor
+from pii_extract.gather.collection.sources.utils import RawTaskDefaults
+from pii_extract.gather.collection.task_collection import filter_piid
 from pii_extract.build.build import build_task
 
 from .. import VERSION
 from ..plugin_loader import load_presidio_plugin_config
-from ..analyzer import presidio_version, presidio_analyzer
+from ..task.analyzer import presidio_analyzer
+from ..task.utils import presidio_version
 from ..task import PresidioTaskCollector
 
 
 class Processor:
 
     def __init__(self, args: argparse.Namespace, debug: bool = False):
         self.args = args
         self.debug = debug
 
 
     def _init_presidio(self):
+        """
+        Initialize the Presidio recognizer object
+        """
         config = load_presidio_plugin_config(self.args.config)
         try:
-            return presidio_analyzer(config)
+            return presidio_analyzer(config, languages=self.args.lang)
         except Exception as e:
             raise ProcException("cannot create Presidio Analyzer engine: {}",
                                 e) from e
 
 
     def proc_version(self, out: TextIO):
         """
@@ -83,15 +88,16 @@
     def proc_pii_entities(self, out: TextIO):
         """
         Print entity recognizers in presidio
         """
         config = load_presidio_plugin_config(self.args.config)
 
         # Get the Presidio task descriptor
-        tc = PresidioTaskCollector(config, debug=self.debug)
+        tc = PresidioTaskCollector(config, languages=self.args.lang,
+                                   debug=self.debug)
         raw_tdesc = tc.gather_tasks()
 
         # Ensure it is normalized
         reformat = RawTaskDefaults()
         tdesc = reformat(raw_tdesc)
 
         print(f". PII entities defined from Presidio (lang={self.args.lang})")
@@ -120,30 +126,28 @@
         description=f"Show information about usable PII tasks (version {VERSION})")
 
     opt_com1 = argparse.ArgumentParser(add_help=False)
     c1 = opt_com1.add_argument_group('Configuration options')
     c1.add_argument("--config", nargs="+",
                     help="add PIISA configuration file(s)")
     c1.add_argument("--lang", nargs='+', help="language to select")
-    c1.add_argument("--country", nargs="+", help="countries to select")
 
     opt_com2 = argparse.ArgumentParser(add_help=False)
     c1 = opt_com2.add_argument_group('Task selection options')
 
     opt_com3 = argparse.ArgumentParser(add_help=False)
     c2 = opt_com3.add_argument_group("Other")
     c2.add_argument("--debug", action="store_true", help="debug mode")
     c2.add_argument('--reraise', action='store_true',
                     help='re-raise exceptions on errors')
 
     subp = parser.add_subparsers(help='command', dest='cmd')
 
-    subp0 = subp.add_parser('version',
-                            help='version information',
-                            parents=[opt_com1, opt_com3])
+    subp.add_parser('version', help='show version information for components',
+                    parents=[opt_com1, opt_com3])
 
     subp1 = subp.add_parser('presidio-recognizers',
                             help='information about recognizers available in presidio',
                             parents=[opt_com1, opt_com3])
     subp1.add_argument("--entities", action="store_true")
 
     subp1 = subp.add_parser('presidio-entities',
```

### Comparing `pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/plugin_loader.py` & `pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/plugin_loader.py`

 * *Files 3% similar despite different names*

```diff
@@ -46,21 +46,22 @@
     """
     source = defs.TASK_SOURCE
     version = VERSION
     description = defs.TASK_DESCRIPTION
 
 
     def __init__(self, config: Union[str, Dict] = None, debug: bool = False,
-                 languages: List[str] = None, **kwargs):
+                 languages: Iterable[str] = None, **kwargs):
         """
           :param config: either a configuration for the plugin, or a filename
             containing that configuration
           :param debug: activate debug mode
           :param languages: restrict the Presidio config to those languages
         """
+        #print("PRESIDIO LOADER", languages)
         self.cfg = load_presidio_plugin_config(config)
         self.obj = PresidioTaskCollector(self.cfg, languages=languages,
                                          debug=debug)
 
 
     def __repr__(self) -> str:
         return f'<PiiExtractPluginLoader: presidio {VERSION}>'
```

### Comparing `pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/resources/plugin-config.json` & `pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/resources/plugin-config.json`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/collector.py` & `pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/collector.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 """
-A collector for the presidio detection task
+A collector for the Presidio detection task
 """
 
 from pii_extract.helper.utils import taskd_field
 from pii_extract.helper.logger import PiiLogger
 
 from typing import Iterable, Dict, Union, Set
 
@@ -79,11 +79,11 @@
         # Prepare the raw task descriptor
         task = {
             "class": "PiiTask",
             "source": defs.TASK_SOURCE,
             "version": VERSION,
             "doc": defs.TASK_DESCRIPTION,
             "task": PresidioTask,
-            "kwargs": {"cfg": cfg, "log": self._log},
+            "kwargs": {"cfg": cfg, "log": self._log, "model_lang": task_lang},
             "pii": pii_list(self.cfg, task_lang)
         }
         yield task
```

### Comparing `pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/task.py` & `pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/task.py`

 * *Files 13% similar despite different names*

```diff
@@ -38,22 +38,23 @@
     """
     pii_source = "microsoft:presidio"
     pii_name = "Presidio wrapper"
     pii_version = presidio_version
 
 
     def __init__(self, task: Dict, pii: List[Dict], cfg: Dict,
-                 log: PiiLogger, **kwargs):
+                 model_lang: Iterable[str], log: PiiLogger, **kwargs):
         """
           :param task: the PII task info dict
           :param pii: the list of descriptors for the PII entities to include
           :param cfg: the plugin configuration
+          :param model_lang: languages to instantiate models for
           :param log: a logger object
         """
-        #print("\nPresidioTask INIT", pii)
+        #print("\nPresidioTask INIT", model_lang, pii)
 
         # Use the "extra" field in the PII dict to build a map (by language)
         # of Presidio entities to PIISA entities
         # (before parent constructor, which will strip away "extra" fields)
         self._ent_map = defaultdict(dict)
         pii_lang = set()
         if isinstance(pii, dict):
@@ -68,21 +69,22 @@
                 raise ConfigException("invalid Presidio config: missing field '{}' in: {}", e, p)
 
         # Initialize
         super().__init__(task=task, pii=pii)
         self._log = log
 
         # Decide a default language for this task (possible if we have only one)
-        self.lang = pii_lang.pop() if len(pii_lang) == 1 else None
+        self.lang = next(iter(pii_lang)) if len(pii_lang) == 1 else None
         self._log(".. PresidioTask (%s): lang=%s tasks=#%d", VERSION,
                   self.lang, len(pii))
 
         # Set up the Presidio Analyzer engine
         try:
-            self.analyzer = presidio_analyzer(cfg, log)
+            self.analyzer = presidio_analyzer(cfg, languages=model_lang,
+                                              logger=self._log)
         except Exception as e:
             raise ProcException("cannot create Presidio Analyzer engine: {}",
                                 e) from e
 
         # Check that all Presidio entities we want are actually supported
         entities = set(self.analyzer.get_supported_entities())
         missing = {pname for edict in self._ent_map.values() for pname in edict
```

### Comparing `pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio/task/utils.py` & `pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio/task/utils.py`

 * *Files identical despite different names*

### Comparing `pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/PKG-INFO` & `pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pii-extract-plg-presidio
-Version: 0.3.0
+Version: 0.3.2
 Summary: Presidio plugin for PII detection
 Home-page: https://github.com/piisa/pii-extract-plg-presidio
-Download-URL: https://github.com/piisa/pii-extract-plg-presidio/tarball/v0.3.0
+Download-URL: https://github.com/piisa/pii-extract-plg-presidio/tarball/v0.3.2
 Author: Paulo Villegas
 Author-email: paulo.vllgs@gmail.com
 License: Apache
 Keywords: PIISA, PII
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Development Status :: 4 - Beta
@@ -55,35 +55,45 @@
    `nlp_config` element in the plugin configuration file must be
    adjusted accordingly.
 
 
 ## Usage
 
 The package does not have any user-facing entry points (except for one console
-script `pii-extract-presidio-info`, which provides information about its
-capabilities).
+information script, see below(#info-script)). Instead, upon installation it
+defines a plugin entry point. This plugin is automatically picked up by the
+scripts and classes in pii-extract-base, and thus its functionality is exposed
+to them.
 
-Instead, upon installation it defines a plugin entry point. This plugin is
-automatically picked up by executing scripts and classes in pii-extract-base,
-and thus its functionality is exposed to it.
-
-Runtime behaviour is governed by a configuration file, which sets up what
-recognizers from Presidio will be instantiated and used. Note that the
+Runtime behaviour is governed by a configuration file, which sets up which
+recognizers from Presidio will be instantiated and used (note that the
 configuration defines which languages are available for detection, but the
-plugin can also be initialized with a _subset_ of those languages.
+plugin can also be initialized with a _subset_ of those languages).
 
 The task created from the plugin is a standard PII task object, using the
 `pii_extract.build.task.MultiPiiTask` class definition. It will be called,
 as all PII task objects, with a `DocumentChunk` object containing the data to
 analyze. The chunk **must** contain language specification in its metadata, so
 that Presidio knows which language to use (unless the plugin task has been
 built with *only one* language; in that case if the chunk does not contain
 a language specification, it will use that single language).
 
 
+## info script
+
+`pii-extract-presidio-info` is a command-line script  which provides
+information about the plugin capabilities: 
+  * `version`: installed package versions
+  * `presidio-recognizers`: list of recognizers in Presidio
+  * `presidio-entities`: the total list of entities Presidio can generate
+  * `pii-entities`: the PIISA tasks that this plugin will create, by translating
+	from the entities detected by Presidio (this depends on the PIISA config
+	used)
+
+
 ## Building
 
 The provided Makefile can be used to process the package:
  * `make pkg` will build the Python package, creating a file that can be
    installed with `pip`
  * `make unit` will launch all unit tests (using pytest, so pytest must be
    available)
```

### Comparing `pii-extract-plg-presidio-0.3.0/src/pii_extract_plg_presidio.egg-info/SOURCES.txt` & `pii-extract-plg-presidio-0.3.2/src/pii_extract_plg_presidio.egg-info/SOURCES.txt`

 * *Files identical despite different names*

