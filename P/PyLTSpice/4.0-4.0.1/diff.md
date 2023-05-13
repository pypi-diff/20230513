# Comparing `tmp/PyLTSpice-4.0.tar.gz` & `tmp/PyLTSpice-4.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "C:\sandbox\PySpice\dist\.tmp-dascasfp\PyLTSpice-4.0.tar", last modified: Sun Apr 30 22:32:38 2023, max compression
+gzip compressed data, was "C:\sandbox\PySpice\dist\.tmp-mwba322e\PyLTSpice-4.0.1.tar", last modified: Fri May 12 20:47:58 2023, max compression
```

## Comparing `PyLTSpice-4.0.tar` & `PyLTSpice-4.0.1.tar`

### file list

```diff
@@ -1,47 +1,60 @@
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.998312 PyLTSpice-4.0/
--rw-rw-rw-   0        0        0    35823 2022-12-04 12:18:59.000000 PyLTSpice-4.0/LICENSE
--rw-rw-rw-   0        0        0    56547 2023-04-30 22:32:37.997314 PyLTSpice-4.0/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.935480 PyLTSpice-4.0/PyLTSpice/
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.948445 PyLTSpice-4.0/PyLTSpice/PyLTSpice.egg-info/
--rw-rw-rw-   0        0        0    56547 2023-04-30 22:32:37.000000 PyLTSpice-4.0/PyLTSpice/PyLTSpice.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1122 2023-04-30 22:32:37.000000 PyLTSpice-4.0/PyLTSpice/PyLTSpice.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-30 22:32:37.000000 PyLTSpice-4.0/PyLTSpice/PyLTSpice.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      159 2023-04-30 22:32:37.000000 PyLTSpice-4.0/PyLTSpice/PyLTSpice.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       34 2023-04-30 22:32:37.000000 PyLTSpice-4.0/PyLTSpice/PyLTSpice.egg-info/requires.txt
--rw-rw-rw-   0        0        0       32 2023-04-30 22:32:37.000000 PyLTSpice-4.0/PyLTSpice/PyLTSpice.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.955426 PyLTSpice-4.0/PyLTSpice/client_server/
--rw-rw-rw-   0        0        0        0 2023-04-08 17:08:22.000000 PyLTSpice-4.0/PyLTSpice/client_server/__init__.py
--rw-rw-rw-   0        0        0     8400 2023-04-19 21:29:58.000000 PyLTSpice-4.0/PyLTSpice/client_server/sim_client.py
--rw-rw-rw-   0        0        0     5427 2023-04-23 11:45:04.000000 PyLTSpice-4.0/PyLTSpice/client_server/sim_server.py
--rw-rw-rw-   0        0        0     4737 2023-04-23 11:45:04.000000 PyLTSpice-4.0/PyLTSpice/client_server/srv_sim_runner.py
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.959417 PyLTSpice-4.0/PyLTSpice/log/
--rw-rw-rw-   0        0        0        0 2023-04-08 22:49:34.000000 PyLTSpice-4.0/PyLTSpice/log/__init__.py
--rw-rw-rw-   0        0        0    29860 2023-02-23 16:46:29.000000 PyLTSpice-4.0/PyLTSpice/log/ltsteps.py
--rw-rw-rw-   0        0        0     6047 2023-04-30 22:25:50.000000 PyLTSpice-4.0/PyLTSpice/log/semi_dev_op_reader.py
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.966398 PyLTSpice-4.0/PyLTSpice/raw/
--rw-rw-rw-   0        0        0        0 2023-04-08 22:49:18.000000 PyLTSpice-4.0/PyLTSpice/raw/__init__.py
--rw-rw-rw-   0        0        0    14667 2023-04-30 20:34:58.000000 PyLTSpice-4.0/PyLTSpice/raw/raw_classes.py
--rw-rw-rw-   0        0        0     5609 2023-04-30 17:57:03.000000 PyLTSpice-4.0/PyLTSpice/raw/raw_convert.py
--rw-rw-rw-   0        0        0    39972 2023-04-30 22:25:50.000000 PyLTSpice-4.0/PyLTSpice/raw/raw_read.py
--rw-rw-rw-   0        0        0    16752 2023-04-30 22:29:26.000000 PyLTSpice-4.0/PyLTSpice/raw/raw_write.py
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.989336 PyLTSpice-4.0/PyLTSpice/sim/
--rw-rw-rw-   0        0        0        0 2023-02-12 22:11:29.000000 PyLTSpice-4.0/PyLTSpice/sim/__init__.py
--rw-rw-rw-   0        0        0     8568 2023-04-30 18:47:14.000000 PyLTSpice-4.0/PyLTSpice/sim/ltspice_simulator.py
--rw-rw-rw-   0        0        0     4636 2023-04-26 20:04:46.000000 PyLTSpice-4.0/PyLTSpice/sim/ngspice_simulator.py
--rw-rw-rw-   0        0        0     1505 2023-04-23 16:20:26.000000 PyLTSpice-4.0/PyLTSpice/sim/process_callback.py
--rw-rw-rw-   0        0        0     6059 2023-04-23 21:06:11.000000 PyLTSpice-4.0/PyLTSpice/sim/run_task.py
--rw-rw-rw-   0        0        0     4809 2023-04-26 21:05:36.000000 PyLTSpice-4.0/PyLTSpice/sim/sim_analysis.py
--rw-rw-rw-   0        0        0    10749 2023-04-23 14:18:49.000000 PyLTSpice-4.0/PyLTSpice/sim/sim_batch.py
--rw-rw-rw-   0        0        0    23686 2023-04-30 18:47:14.000000 PyLTSpice-4.0/PyLTSpice/sim/sim_runner.py
--rw-rw-rw-   0        0        0     9221 2023-04-26 21:05:36.000000 PyLTSpice-4.0/PyLTSpice/sim/sim_stepping.py
--rw-rw-rw-   0        0        0     4652 2023-04-08 19:00:33.000000 PyLTSpice-4.0/PyLTSpice/sim/simulator.py
--rw-rw-rw-   0        0        0    46608 2023-04-30 22:25:50.000000 PyLTSpice-4.0/PyLTSpice/sim/spice_editor.py
--rw-rw-rw-   0        0        0     7384 2023-04-07 13:28:50.000000 PyLTSpice-4.0/PyLTSpice/sim/xyce_simulator.py
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.993327 PyLTSpice-4.0/PyLTSpice/utils/
--rw-rw-rw-   0        0        0     2678 2023-04-29 18:03:58.000000 PyLTSpice-4.0/PyLTSpice/utils/detect_encoding.py
--rw-rw-rw-   0        0        0    11563 2023-01-15 18:28:54.000000 PyLTSpice-4.0/PyLTSpice/utils/sweep_iterators.py
--rw-rw-rw-   0        0        0    14768 2023-04-30 22:25:50.000000 PyLTSpice-4.0/README.md
--rw-rw-rw-   0        0        0     1179 2023-04-30 18:15:46.000000 PyLTSpice-4.0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-04-30 22:32:37.999311 PyLTSpice-4.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-04-30 22:32:37.995320 PyLTSpice-4.0/tests/
--rw-rw-rw-   0        0        0      801 2023-04-23 17:09:47.000000 PyLTSpice-4.0/tests/test_ltsteps.py
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.091843 PyLTSpice-4.0.1/
+-rw-rw-rw-   0        0        0    35823 2022-12-04 12:18:59.000000 PyLTSpice-4.0.1/LICENSE
+-rw-rw-rw-   0        0        0    56621 2023-05-12 20:47:58.089849 PyLTSpice-4.0.1/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.032316 PyLTSpice-4.0.1/PyLTSpice/
+-rw-rw-rw-   0        0        0     9679 2023-05-12 18:44:35.000000 PyLTSpice-4.0.1/PyLTSpice/Histogram.py
+-rw-rw-rw-   0        0        0      362 2023-02-12 22:14:27.000000 PyLTSpice-4.0.1/PyLTSpice/LTSpiceBatch.py
+-rw-rw-rw-   0        0        0      333 2023-02-12 22:14:27.000000 PyLTSpice-4.0.1/PyLTSpice/LTSpice_RawRead.py
+-rw-rw-rw-   0        0        0      332 2023-02-12 22:14:27.000000 PyLTSpice-4.0.1/PyLTSpice/LTSpice_RawWrite.py
+-rw-rw-rw-   0        0        0     6615 2023-05-12 19:45:12.000000 PyLTSpice-4.0.1/PyLTSpice/LTSteps.py
+-rw-rw-rw-   0        0        0      337 2023-04-30 19:07:01.000000 PyLTSpice-4.0.1/PyLTSpice/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.046279 PyLTSpice-4.0.1/PyLTSpice/client_server/
+-rw-rw-rw-   0        0        0        0 2023-04-08 17:08:22.000000 PyLTSpice-4.0.1/PyLTSpice/client_server/__init__.py
+-rw-rw-rw-   0        0        0     8400 2023-04-19 21:29:58.000000 PyLTSpice-4.0.1/PyLTSpice/client_server/sim_client.py
+-rw-rw-rw-   0        0        0     5427 2023-04-23 11:45:04.000000 PyLTSpice-4.0.1/PyLTSpice/client_server/sim_server.py
+-rw-rw-rw-   0        0        0     4737 2023-04-23 11:45:04.000000 PyLTSpice-4.0.1/PyLTSpice/client_server/srv_sim_runner.py
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.049954 PyLTSpice-4.0.1/PyLTSpice/log/
+-rw-rw-rw-   0        0        0        0 2023-04-08 22:49:34.000000 PyLTSpice-4.0.1/PyLTSpice/log/__init__.py
+-rw-rw-rw-   0        0        0    29860 2023-02-23 16:46:29.000000 PyLTSpice-4.0.1/PyLTSpice/log/ltsteps.py
+-rw-rw-rw-   0        0        0     6047 2023-04-30 22:25:50.000000 PyLTSpice-4.0.1/PyLTSpice/log/semi_dev_op_reader.py
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.056938 PyLTSpice-4.0.1/PyLTSpice/raw/
+-rw-rw-rw-   0        0        0        0 2023-04-08 22:49:18.000000 PyLTSpice-4.0.1/PyLTSpice/raw/__init__.py
+-rw-rw-rw-   0        0        0    14667 2023-04-30 20:34:58.000000 PyLTSpice-4.0.1/PyLTSpice/raw/raw_classes.py
+-rw-rw-rw-   0        0        0     5609 2023-04-30 17:57:03.000000 PyLTSpice-4.0.1/PyLTSpice/raw/raw_convert.py
+-rw-rw-rw-   0        0        0    36023 2023-05-12 19:54:20.000000 PyLTSpice-4.0.1/PyLTSpice/raw/raw_read.py
+-rw-rw-rw-   0        0        0    16752 2023-04-30 22:29:26.000000 PyLTSpice-4.0.1/PyLTSpice/raw/raw_write.py
+-rw-rw-rw-   0        0        0     4236 2023-05-12 20:33:51.000000 PyLTSpice-4.0.1/PyLTSpice/rawplot.py
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.075886 PyLTSpice-4.0.1/PyLTSpice/sim/
+-rw-rw-rw-   0        0        0        0 2023-02-12 22:11:29.000000 PyLTSpice-4.0.1/PyLTSpice/sim/__init__.py
+-rw-rw-rw-   0        0        0     8568 2023-04-30 18:47:14.000000 PyLTSpice-4.0.1/PyLTSpice/sim/ltspice_simulator.py
+-rw-rw-rw-   0        0        0     4636 2023-04-26 20:04:46.000000 PyLTSpice-4.0.1/PyLTSpice/sim/ngspice_simulator.py
+-rw-rw-rw-   0        0        0     1505 2023-04-23 16:20:26.000000 PyLTSpice-4.0.1/PyLTSpice/sim/process_callback.py
+-rw-rw-rw-   0        0        0     6059 2023-04-23 21:06:11.000000 PyLTSpice-4.0.1/PyLTSpice/sim/run_task.py
+-rw-rw-rw-   0        0        0     4809 2023-04-26 21:05:36.000000 PyLTSpice-4.0.1/PyLTSpice/sim/sim_analysis.py
+-rw-rw-rw-   0        0        0    10749 2023-04-23 14:18:49.000000 PyLTSpice-4.0.1/PyLTSpice/sim/sim_batch.py
+-rw-rw-rw-   0        0        0    23686 2023-04-30 18:47:14.000000 PyLTSpice-4.0.1/PyLTSpice/sim/sim_runner.py
+-rw-rw-rw-   0        0        0     9221 2023-04-26 21:05:36.000000 PyLTSpice-4.0.1/PyLTSpice/sim/sim_stepping.py
+-rw-rw-rw-   0        0        0     4652 2023-04-08 19:00:33.000000 PyLTSpice-4.0.1/PyLTSpice/sim/simulator.py
+-rw-rw-rw-   0        0        0    46608 2023-04-30 22:25:50.000000 PyLTSpice-4.0.1/PyLTSpice/sim/spice_editor.py
+-rw-rw-rw-   0        0        0     7384 2023-04-07 13:28:50.000000 PyLTSpice-4.0.1/PyLTSpice/sim/xyce_simulator.py
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.079875 PyLTSpice-4.0.1/PyLTSpice/utils/
+-rw-rw-rw-   0        0        0     2935 2023-05-12 19:51:10.000000 PyLTSpice-4.0.1/PyLTSpice/utils/detect_encoding.py
+-rw-rw-rw-   0        0        0    11563 2023-01-15 18:28:54.000000 PyLTSpice-4.0.1/PyLTSpice/utils/sweep_iterators.py
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.040296 PyLTSpice-4.0.1/PyLTSpice.egg-info/
+-rw-rw-rw-   0        0        0    56621 2023-05-12 20:47:57.000000 PyLTSpice-4.0.1/PyLTSpice.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1338 2023-05-12 20:47:58.000000 PyLTSpice-4.0.1/PyLTSpice.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-12 20:47:57.000000 PyLTSpice-4.0.1/PyLTSpice.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      165 2023-05-12 20:47:57.000000 PyLTSpice-4.0.1/PyLTSpice.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       40 2023-05-12 20:47:57.000000 PyLTSpice-4.0.1/PyLTSpice.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       41 2023-05-12 20:47:57.000000 PyLTSpice-4.0.1/PyLTSpice.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0    14840 2023-05-12 20:39:59.000000 PyLTSpice-4.0.1/README.md
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.081870 PyLTSpice-4.0.1/doc/
+-rw-rw-rw-   0        0        0     2448 2023-01-15 08:45:40.000000 PyLTSpice-4.0.1/doc/conf.py
+-rw-rw-rw-   0        0        0     1185 2023-05-12 20:39:59.000000 PyLTSpice-4.0.1/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-12 20:47:58.091843 PyLTSpice-4.0.1/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.083865 PyLTSpice-4.0.1/tests/
+-rw-rw-rw-   0        0        0      801 2023-04-23 17:09:47.000000 PyLTSpice-4.0.1/tests/test_ltsteps.py
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.085860 PyLTSpice-4.0.1/tests/unittest/
+drwxrwxrwx   0        0        0        0 2023-05-12 20:47:58.087855 PyLTSpice-4.0.1/tests/unittest/sweep_iterators/
+-rw-rw-rw-   0        0        0     6014 2023-02-23 17:53:15.000000 PyLTSpice-4.0.1/tests/unittest/sweep_iterators/sweep_iterators_unittest.py
+-rw-rw-rw-   0        0        0    19229 2023-04-30 22:25:50.000000 PyLTSpice-4.0.1/tests/unittest/test_pyltspice.py
```

### Comparing `PyLTSpice-4.0/LICENSE` & `PyLTSpice-4.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PKG-INFO` & `PyLTSpice-4.0.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyLTSpice
-Version: 4.0
+Version: 4.0.1
 Summary: A set of tools to Automate LTSpice simulations
 Author-email: Nuno Brum <me@nunobrum.com>
 License:                     GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -954,14 +954,16 @@
 ## To whom do I talk to? ##
 
 * Tools website : [https://www.nunobrum.com/pyltspice.html](https://www.nunobrum.com/pyltspice.html)
 * Repo owner : [me@nunobrum.com](me@nunobrum.com)
 * Alternative contact : nuno.brum@gmail.com
 
 ## History ##
+* Version 4.0.1\
+  Bug fix on CLI for the Histogram.py and LTSteps.py
 
 * Version 4.0.0\
   Separating the SimCommander into two separate classes, one for the spice netlist editing (SpiceEditor) and another for
   the simulation execution (SimRunner).\
   Implementing simulation server to allow for remote simulation execution and the respective client.\
   Supporting Wiggler element in the new LTSpiceXVII.\
   Renaming all files into lowercase.\
```

### Comparing `PyLTSpice-4.0/PyLTSpice/PyLTSpice.egg-info/PKG-INFO` & `PyLTSpice-4.0.1/PyLTSpice.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyLTSpice
-Version: 4.0
+Version: 4.0.1
 Summary: A set of tools to Automate LTSpice simulations
 Author-email: Nuno Brum <me@nunobrum.com>
 License:                     GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -954,14 +954,16 @@
 ## To whom do I talk to? ##
 
 * Tools website : [https://www.nunobrum.com/pyltspice.html](https://www.nunobrum.com/pyltspice.html)
 * Repo owner : [me@nunobrum.com](me@nunobrum.com)
 * Alternative contact : nuno.brum@gmail.com
 
 ## History ##
+* Version 4.0.1\
+  Bug fix on CLI for the Histogram.py and LTSteps.py
 
 * Version 4.0.0\
   Separating the SimCommander into two separate classes, one for the spice netlist editing (SpiceEditor) and another for
   the simulation execution (SimRunner).\
   Implementing simulation server to allow for remote simulation execution and the respective client.\
   Supporting Wiggler element in the new LTSpiceXVII.\
   Renaming all files into lowercase.\
```

### Comparing `PyLTSpice-4.0/PyLTSpice/client_server/sim_client.py` & `PyLTSpice-4.0.1/PyLTSpice/client_server/sim_client.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/client_server/sim_server.py` & `PyLTSpice-4.0.1/PyLTSpice/client_server/sim_server.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/client_server/srv_sim_runner.py` & `PyLTSpice-4.0.1/PyLTSpice/client_server/srv_sim_runner.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/log/ltsteps.py` & `PyLTSpice-4.0.1/PyLTSpice/log/ltsteps.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/log/semi_dev_op_reader.py` & `PyLTSpice-4.0.1/PyLTSpice/log/semi_dev_op_reader.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/raw/raw_classes.py` & `PyLTSpice-4.0.1/PyLTSpice/raw/raw_classes.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/raw/raw_convert.py` & `PyLTSpice-4.0.1/PyLTSpice/raw/raw_convert.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/raw/raw_read.py` & `PyLTSpice-4.0.1/PyLTSpice/raw/raw_read.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,8 +1,7 @@
-#!/usr/bin/env python
 # coding=utf-8
 
 # -------------------------------------------------------------------------------
 #    ____        _   _____ ____        _
 #   |  _ \ _   _| | |_   _/ ___| _ __ (_) ___ ___
 #   | |_) | | | | |   | | \___ \| '_ \| |/ __/ _ \
 #   |  __/| |_| | |___| |  ___) | |_) | | (_|  __/
@@ -866,124 +865,7 @@
                               "Use 'pip install pandas' to install it.")
         df = self.to_dataframe(columns=columns, step=step)
         df.to_excel(filename, **kwargs)
 
 
 # Backward compatibility naming
 LTSpiceRawRead = RawRead
-
-
-def main():
-    """Uses matplotlib to plot the data in the raw file"""
-    import sys
-    import matplotlib.pyplot as plt
-    import os
-    from os.path import split as path_split
-    from os.path import join as path_join
-    from numpy import abs as mag
-
-    def what_to_units(whattype):
-        """Determines the unit to display on the plot Y axis"""
-        if 'voltage' in whattype:
-            return 'V'
-        if 'current' in whattype:
-            return 'A'
-
-    directory = os.getcwd()
-
-    if len(sys.argv) > 1:
-        raw_filename = sys.argv[1]
-        trace_names = sys.argv[2:]
-        if len(trace_names) == 0:
-            trace_names = '*'
-    else:
-        test_directory = path_join(path_split(directory)[0], 'tests')
-        filename = 'DC sweep.raw'
-        # filename = 'tran.raw'
-        # filename = 'tran - step.raw'
-        # filename = 'ac.raw'
-        # filename = 'AC - STEP.raw'
-        # filename = 'PI_Filter_tf.raw'
-        # filename = 'DC op point - STEP_1.raw'
-        # filename = 'Noise.raw'
-        filename = "test2_gs_000.raw"
-        trace_names = ("run", "V(out)", "V(err)")
-        # trace_names = '*' # 'V(out)',
-        raw_filename = path_join(test_directory, filename)
-
-    LTR = RawRead(raw_filename, trace_names, verbose=True)
-    for param, value in LTR.raw_params.items():
-        print("{}: {}{}".format(param, " " * (20 - len(param)), str(value).strip()))
-
-    if trace_names == '*':
-        print("Reading all the traces in the raw file")
-        trace_names = LTR.get_trace_names()
-
-    traces = [LTR.get_trace(trace) for trace in trace_names]
-    if LTR.axis is not None:
-        steps_data = LTR.get_steps()
-    else:
-        steps_data = [0]
-    print("Steps read are :", list(steps_data))
-
-    if 'complex' in LTR.flags:
-        n_axis = len(traces) * 2
-    else:
-        n_axis = len(traces)
-
-    fig, axis_set = plt.subplots(n_axis, 1, sharex='all')
-    write_labels = True
-
-    for i, trace in enumerate(traces):
-        if 'complex' in LTR.flags:
-            axis_set = axis_set[2 * i: 2 * i + 2]  # Returns two axis
-        else:
-            if n_axis == 1:
-                axis_set = [axis_set]  # Needs to return a list
-            else:
-                axis_set = axis_set[i:i + 1]  # Returns just one axis but enclosed in a list
-        magnitude = True
-        for ax in axis_set:
-            ax.grid(True)
-            if 'log' in LTR.flags:
-                ax.set_xscale('log')
-            for step_i in steps_data:
-                if LTR.axis:
-                    x = LTR.get_axis(step_i)
-                else:
-                    x = np.arange(LTR.nPoints)
-                y = traces[i].get_wave(step_i)
-                if 'complex' in LTR.flags:
-                    x = mag(x)
-                    if magnitude:
-                        ax.set_yscale('log')
-                        y = mag(y)
-                    else:
-                        y = angle(y, deg=True)
-                if write_labels:
-                    ax.plot(x, y, label=str(steps_data[step_i]))
-                else:
-                    ax.plot(x, y)
-            write_labels = False
-
-            if 'complex' in LTR.flags:
-                if magnitude:
-                    title = f"{trace.name} Mag [db{what_to_units(trace.whattype)}]"
-                    magnitude = False
-                else:
-                    title = f"{trace.name} Phase [deg]"
-            else:
-                title = f"{trace.name} [{what_to_units(trace.whattype)}]"
-            ax.set_title(title)
-
-    plt.figlegend()
-    plt.show()
-'''
-'''
-# out = open("RAW_TEST_out_test1.txt", 'w')
-#
-# for step in LTR.get_steps():
-#     for x in range(len(LTR[0].data)):
-#         out.write("%s, %e, %e\n" % (step, LTR[0].data[x], LTR[2].data[x]))
-# out.close()
-if __name__ == "__main__":
-    main()
```

### Comparing `PyLTSpice-4.0/PyLTSpice/raw/raw_write.py` & `PyLTSpice-4.0.1/PyLTSpice/raw/raw_write.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/ltspice_simulator.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/ltspice_simulator.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/ngspice_simulator.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/ngspice_simulator.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/process_callback.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/process_callback.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/run_task.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/run_task.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/sim_analysis.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/sim_analysis.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/sim_batch.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/sim_batch.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/sim_runner.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/sim_runner.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/sim_stepping.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/sim_stepping.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/simulator.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/simulator.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/spice_editor.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/spice_editor.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/sim/xyce_simulator.py` & `PyLTSpice-4.0.1/PyLTSpice/sim/xyce_simulator.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/PyLTSpice/utils/detect_encoding.py` & `PyLTSpice-4.0.1/PyLTSpice/utils/detect_encoding.py`

 * *Files 12% similar despite different names*

```diff
@@ -21,14 +21,20 @@
 International Support functions
 Not using other known unicode detection libraries because we don't need something so complicated. LTSpice only supports
 for the time being a reduced set of encodings.
 """
 from pathlib import Path
 from typing import Union
 
+class EncodingDetectError(Exception):
+    """
+    Exception raised when the encoding of a file cannot be detected
+    """
+    pass
+
 
 def detect_encoding(file_path: Union[str, Path], expected_str: str = '') -> str:
     """
     Simple strategy to detect file encoding.  If an expected_str is given the function will scan through the possible
     encodings and return a match.
     If an expected string is not given, it will use the second character is null, high chances are that this file has an
     'utf_16_le' encoding, otherwise it is assuming that it is 'utf-8'.
@@ -44,20 +50,23 @@
             with open(file_path, 'r', encoding=encoding) as f:
                 lines = f.readlines()
                 f.seek(0)
         except UnicodeDecodeError:
             # This encoding didn't work, let's try again
             continue
         else:
+            if len(lines) == 0:
+                # Empty file
+                continue
             if expected_str:
                 if not lines[0].startswith(expected_str):
                     # File did not start with expected string
                     # Try again with a different encoding (This is unlikely to resolve the issue)
                     continue
             if encoding == 'utf-8' and lines[0][1] == '\x00':
                 continue
             return encoding
     else:
         if expected_str:
-            raise UnicodeError(f"Expected string \"{expected_str}\" not found in file:{file_path}")
+            raise EncodingDetectError(f"Expected string \"{expected_str}\" not found in file:{file_path}")
         else:
-            raise UnicodeError(f"Unable to detect log file encoding")
+            raise EncodingDetectError(f"Unable to detect encoding on log file: {file_path}")
```

### Comparing `PyLTSpice-4.0/PyLTSpice/utils/sweep_iterators.py` & `PyLTSpice-4.0.1/PyLTSpice/utils/sweep_iterators.py`

 * *Files identical despite different names*

### Comparing `PyLTSpice-4.0/README.md` & `PyLTSpice-4.0.1/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -265,14 +265,16 @@
 ## To whom do I talk to? ##
 
 * Tools website : [https://www.nunobrum.com/pyltspice.html](https://www.nunobrum.com/pyltspice.html)
 * Repo owner : [me@nunobrum.com](me@nunobrum.com)
 * Alternative contact : nuno.brum@gmail.com
 
 ## History ##
+* Version 4.0.1\
+  Bug fix on CLI for the Histogram.py and LTSteps.py
 
 * Version 4.0.0\
   Separating the SimCommander into two separate classes, one for the spice netlist editing (SpiceEditor) and another for
   the simulation execution (SimRunner).\
   Implementing simulation server to allow for remote simulation execution and the respective client.\
   Supporting Wiggler element in the new LTSpiceXVII.\
   Renaming all files into lowercase.\
```

### Comparing `PyLTSpice-4.0/pyproject.toml` & `PyLTSpice-4.0.1/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -2,44 +2,44 @@
 requires = [
     "setuptools>=42",
     "wheel"
 ]
 build-backend = "setuptools.build_meta"
 [project]
 name = "PyLTSpice"
-version = "4.0"
+version = "4.0.1"
 authors = [
   { name="Nuno Brum", email="me@nunobrum.com" },
 ]
 description = "A set of tools to Automate LTSpice simulations"
 readme = "README.md"
 license = { file="LICENSE" }
 requires-python = ">=3.7"
 dependencies = [
-    "numpy",
+    "numpy==1.21",
     "psutil",
     "clipboard",
     "matplotlib"
 ]
 classifiers=[
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
     "Operating System :: OS Independent",
 ]
 
 [tool.setuptools.packages.find]
 # All the following settings are optional:
-where = ["PyLTSpice"]  # ["."] by default
+where = ["."]  # ["."] by default
 include = ["*"]  # ["*"] by default
 exclude = ["tests"]  # empty by default
 namespaces = true  # true by default
 
 
 [project.scripts]
-ltsteps = "PyLTSpice.ltsteps"
-histogram = "PyLTSpice.Histogram"
-rawplot = "PyLTSpice.raw.rawread:main"
+ltsteps = "PyLTSpice.LTSteps:main"
+histogram = "PyLTSpice.Histogram:main"
+rawplot = "PyLTSpice.rawplot:main"
 rawconvert = "PyLTSpice.raw.raw_convert:main"
 
 [project.urls]
 "Homepage" = "https://github.com/nunobrum/PyLTSpice"
 "Bug Tracker" = "https://github.com/nunobrum/PyLTSpice/issues"
```

### Comparing `PyLTSpice-4.0/tests/test_ltsteps.py` & `PyLTSpice-4.0.1/tests/test_ltsteps.py`

 * *Files identical despite different names*

