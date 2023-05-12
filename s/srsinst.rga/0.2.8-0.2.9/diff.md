# Comparing `tmp/srsinst.rga-0.2.8.tar.gz` & `tmp/srsinst.rga-0.2.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "C:\PyPI\instrument_library\rga100\dist\.tmp-yfrrc932\srsinst.rga-0.2.8.tar", last modified: Wed Feb  8 18:31:27 2023, max compression
+gzip compressed data, was "C:\PyPI\instrument_library\rga100\dist\.tmp-j3yq1dge\srsinst.rga-0.2.9.tar", last modified: Tue Apr 11 18:35:49 2023, max compression
```

## Comparing `srsinst.rga-0.2.8.tar` & `srsinst.rga-0.2.9.tar`

### file list

```diff
@@ -1,49 +1,50 @@
-drwxrwxrwx   0        0        0        0 2023-02-08 18:31:27.245626 srsinst.rga-0.2.8/
--rw-rw-rw-   0        0        0     1107 2022-11-01 00:07:51.000000 srsinst.rga-0.2.8/LICENSE.txt
--rw-rw-rw-   0        0        0       58 2022-12-12 16:43:23.000000 srsinst.rga-0.2.8/MANIFEST.in
--rw-rw-rw-   0        0        0     5889 2023-02-08 18:31:27.245626 srsinst.rga-0.2.8/PKG-INFO
--rw-rw-rw-   0        0        0     5083 2023-01-31 01:59:37.000000 srsinst.rga-0.2.8/README.md
--rw-rw-rw-   0        0        0       42 2023-02-08 18:31:27.245626 srsinst.rga-0.2.8/setup.cfg
--rw-rw-rw-   0        0        0     2149 2023-01-24 17:04:48.000000 srsinst.rga-0.2.8/setup.py
-drwxrwxrwx   0        0        0        0 2023-02-08 18:31:27.189435 srsinst.rga-0.2.8/srsinst/
-drwxrwxrwx   0        0        0        0 2023-02-08 18:31:27.207095 srsinst.rga-0.2.8/srsinst/rga/
--rw-rw-rw-   0        0        0      345 2023-02-08 18:31:10.000000 srsinst.rga-0.2.8/srsinst/rga/__init__.py
--rw-rw-rw-   0        0        0      483 2022-12-12 16:43:23.000000 srsinst.rga-0.2.8/srsinst/rga/__main__.py
--rw-rw-rw-   0        0        0    10602 2023-01-31 00:04:05.000000 srsinst.rga-0.2.8/srsinst/rga/gaslib.dat
-drwxrwxrwx   0        0        0        0 2023-02-08 18:31:27.209440 srsinst.rga-0.2.8/srsinst/rga/instruments/
--rw-rw-rw-   0        0        0        0 2022-12-02 00:09:02.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/__init__.py
--rw-rw-rw-   0        0        0      711 2022-12-13 17:19:57.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/get_instruments.py
-drwxrwxrwx   0        0        0        0 2023-02-08 18:31:27.221699 srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/
--rw-rw-rw-   0        0        0        0 2022-12-02 00:09:02.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/__init__.py
--rw-rw-rw-   0        0        0     3543 2022-12-12 23:26:55.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/commands.py
--rw-rw-rw-   0        0        0     6521 2023-01-05 01:11:19.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/components.py
--rw-rw-rw-   0        0        0     4391 2022-12-02 00:09:02.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/errors.py
--rw-rw-rw-   0        0        0     8033 2023-02-03 16:56:32.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/rga.py
--rw-rw-rw-   0        0        0    10823 2023-01-19 23:23:51.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/scans.py
--rw-rw-rw-   0        0        0     9403 2022-12-09 20:23:49.000000 srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/sicp.py
-drwxrwxrwx   0        0        0        0 2023-02-08 18:31:27.228636 srsinst.rga-0.2.8/srsinst/rga/plots/
--rw-rw-rw-   0        0        0        0 2023-01-24 22:29:13.000000 srsinst.rga-0.2.8/srsinst/rga/plots/__init__.py
--rw-rw-rw-   0        0        0     3222 2023-02-01 17:41:16.000000 srsinst.rga-0.2.8/srsinst/rga/plots/analogscanplot.py
--rw-rw-rw-   0        0        0     2093 2023-01-30 21:23:01.000000 srsinst.rga-0.2.8/srsinst/rga/plots/analysis.py
--rw-rw-rw-   0        0        0     3120 2023-02-08 18:25:56.000000 srsinst.rga-0.2.8/srsinst/rga/plots/basescanplot.py
--rw-rw-rw-   0        0        0     3165 2023-01-19 20:12:20.000000 srsinst.rga-0.2.8/srsinst/rga/plots/histogramscanplot.py
--rw-rw-rw-   0        0        0     7927 2023-02-08 18:25:56.000000 srsinst.rga-0.2.8/srsinst/rga/plots/timeplot.py
--rw-rw-rw-   0        0        0     2180 2023-01-27 17:09:59.000000 srsinst.rga-0.2.8/srsinst/rga/rga.taskconfig
-drwxrwxrwx   0        0        0        0 2023-02-08 18:31:27.244599 srsinst.rga-0.2.8/srsinst/rga/tasks/
--rw-rw-rw-   0        0        0        0 2022-12-02 00:09:02.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/__init__.py
--rw-rw-rw-   0        0        0     3859 2023-01-03 17:25:41.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/analogscantask.py
--rw-rw-rw-   0        0        0     2374 2022-12-13 17:36:16.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/cemcontroltask.py
--rw-rw-rw-   0        0        0     8479 2022-12-14 02:12:33.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/cemgaintask.py
--rw-rw-rw-   0        0        0     9294 2023-02-08 18:25:56.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/compositionanalysistask.py
--rw-rw-rw-   0        0        0     5093 2023-02-01 17:32:06.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/derivedpvstscantask.py
--rw-rw-rw-   0        0        0     2588 2022-12-22 22:24:12.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/filamentcontroltask.py
--rw-rw-rw-   0        0        0     3629 2022-12-12 22:53:32.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/histogramscantask.py
--rw-rw-rw-   0        0        0     2439 2023-01-19 18:03:06.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/pvstscantask.py
--rw-rw-rw-   0        0        0     1975 2022-12-13 18:32:59.000000 srsinst.rga-0.2.8/srsinst/rga/tasks/searchlan.py
-drwxrwxrwx   0        0        0        0 2023-02-08 18:31:27.200918 srsinst.rga-0.2.8/srsinst.rga.egg-info/
--rw-rw-rw-   0        0        0     5889 2023-02-08 18:31:27.000000 srsinst.rga-0.2.8/srsinst.rga.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1295 2023-02-08 18:31:27.000000 srsinst.rga-0.2.8/srsinst.rga.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-02-08 18:31:27.000000 srsinst.rga-0.2.8/srsinst.rga.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       50 2023-02-08 18:31:27.000000 srsinst.rga-0.2.8/srsinst.rga.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       54 2023-02-08 18:31:27.000000 srsinst.rga-0.2.8/srsinst.rga.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-02-08 18:31:27.000000 srsinst.rga-0.2.8/srsinst.rga.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-04-11 18:35:49.806633 srsinst.rga-0.2.9/
+-rw-rw-rw-   0        0        0     1107 2022-11-01 00:07:51.000000 srsinst.rga-0.2.9/LICENSE.txt
+-rw-rw-rw-   0        0        0       58 2022-12-12 16:43:23.000000 srsinst.rga-0.2.9/MANIFEST.in
+-rw-rw-rw-   0        0        0     5877 2023-04-11 18:35:49.806633 srsinst.rga-0.2.9/PKG-INFO
+-rw-rw-rw-   0        0        0     5071 2023-02-09 19:05:11.000000 srsinst.rga-0.2.9/README.md
+-rw-rw-rw-   0        0        0       42 2023-04-11 18:35:49.806633 srsinst.rga-0.2.9/setup.cfg
+-rw-rw-rw-   0        0        0     2148 2023-04-07 00:41:50.000000 srsinst.rga-0.2.9/setup.py
+drwxrwxrwx   0        0        0        0 2023-04-11 18:35:49.564245 srsinst.rga-0.2.9/srsinst/
+drwxrwxrwx   0        0        0        0 2023-04-11 18:35:49.654178 srsinst.rga-0.2.9/srsinst/rga/
+-rw-rw-rw-   0        0        0      345 2023-04-11 18:35:07.000000 srsinst.rga-0.2.9/srsinst/rga/__init__.py
+-rw-rw-rw-   0        0        0      483 2023-04-07 00:54:15.000000 srsinst.rga-0.2.9/srsinst/rga/__main__.py
+-rw-rw-rw-   0        0        0    10602 2023-01-31 00:04:05.000000 srsinst.rga-0.2.9/srsinst/rga/gaslib.dat
+drwxrwxrwx   0        0        0        0 2023-04-11 18:35:49.654178 srsinst.rga-0.2.9/srsinst/rga/instruments/
+-rw-rw-rw-   0        0        0       38 2023-03-16 16:49:16.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/__init__.py
+-rw-rw-rw-   0        0        0      729 2023-04-06 22:14:12.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/get_instruments.py
+drwxrwxrwx   0        0        0        0 2023-04-11 18:35:49.674125 srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/
+-rw-rw-rw-   0        0        0        0 2022-12-02 00:09:02.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/__init__.py
+-rw-rw-rw-   0        0        0     3966 2023-04-05 21:37:14.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/commands.py
+-rw-rw-rw-   0        0        0     6316 2023-04-07 00:33:39.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/components.py
+-rw-rw-rw-   0        0        0     4391 2022-12-02 00:09:02.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/errors.py
+-rw-rw-rw-   0        0        0     8005 2023-04-06 22:55:39.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/rga.py
+-rw-rw-rw-   0        0        0    10815 2023-04-05 21:37:14.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/scans.py
+-rw-rw-rw-   0        0        0     9751 2023-03-23 22:12:18.000000 srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/sicp.py
+drwxrwxrwx   0        0        0        0 2023-04-11 18:35:49.710541 srsinst.rga-0.2.9/srsinst/rga/plots/
+-rw-rw-rw-   0        0        0        0 2023-01-24 22:29:13.000000 srsinst.rga-0.2.9/srsinst/rga/plots/__init__.py
+-rw-rw-rw-   0        0        0     3490 2023-04-06 22:14:36.000000 srsinst.rga-0.2.9/srsinst/rga/plots/analogscanplot.py
+-rw-rw-rw-   0        0        0     2093 2023-01-30 21:23:01.000000 srsinst.rga-0.2.9/srsinst/rga/plots/analysis.py
+-rw-rw-rw-   0        0        0     3115 2023-04-06 22:16:35.000000 srsinst.rga-0.2.9/srsinst/rga/plots/basescanplot.py
+-rw-rw-rw-   0        0        0     3160 2023-04-06 22:17:17.000000 srsinst.rga-0.2.9/srsinst/rga/plots/histogramscanplot.py
+-rw-rw-rw-   0        0        0     7982 2023-04-06 22:17:27.000000 srsinst.rga-0.2.9/srsinst/rga/plots/timeplot.py
+-rw-rw-rw-   0        0        0     2180 2023-04-05 16:04:47.000000 srsinst.rga-0.2.9/srsinst/rga/rga.taskconfig
+drwxrwxrwx   0        0        0        0 2023-04-11 18:35:49.806633 srsinst.rga-0.2.9/srsinst/rga/tasks/
+-rw-rw-rw-   0        0        0        0 2022-12-02 00:09:02.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/__init__.py
+-rw-rw-rw-   0        0        0     3870 2023-04-11 00:37:02.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/analogscantask.py
+-rw-rw-rw-   0        0        0     2436 2023-04-06 22:17:56.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/cemcontroltask.py
+-rw-rw-rw-   0        0        0     8541 2023-04-06 22:18:09.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/cemgaintask.py
+-rw-rw-rw-   0        0        0     9453 2023-04-11 00:37:45.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/compositionanalysistask.py
+-rw-rw-rw-   0        0        0     5104 2023-04-11 00:38:06.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/derivedpvstscantask.py
+-rw-rw-rw-   0        0        0     2632 2023-04-06 22:18:58.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/filamentcontroltask.py
+-rw-rw-rw-   0        0        0     3642 2023-04-11 00:38:30.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/histogramscantask.py
+-rw-rw-rw-   0        0        0    11350 2023-04-11 00:39:33.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/peaktuningtask.py
+-rw-rw-rw-   0        0        0     2438 2023-04-11 00:39:52.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/pvstscantask.py
+-rw-rw-rw-   0        0        0     1968 2023-04-06 22:19:58.000000 srsinst.rga-0.2.9/srsinst/rga/tasks/searchlan.py
+drwxrwxrwx   0        0        0        0 2023-04-11 18:35:49.634140 srsinst.rga-0.2.9/srsinst.rga.egg-info/
+-rw-rw-rw-   0        0        0     5877 2023-04-11 18:35:49.000000 srsinst.rga-0.2.9/srsinst.rga.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1331 2023-04-11 18:35:49.000000 srsinst.rga-0.2.9/srsinst.rga.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-04-11 18:35:49.000000 srsinst.rga-0.2.9/srsinst.rga.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       50 2023-04-11 18:35:49.000000 srsinst.rga-0.2.9/srsinst.rga.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       53 2023-04-11 18:35:49.000000 srsinst.rga-0.2.9/srsinst.rga.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-04-11 18:35:49.000000 srsinst.rga-0.2.9/srsinst.rga.egg-info/top_level.txt
```

### Comparing `srsinst.rga-0.2.8/LICENSE.txt` & `srsinst.rga-0.2.9/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `srsinst.rga-0.2.8/PKG-INFO` & `srsinst.rga-0.2.9/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: srsinst.rga
-Version: 0.2.8
+Version: 0.2.9
 Summary: Instrument library and GUI application for SRS RGA
 Author: Chulhoon Kim
 License: MIT license
 Keywords: RGA,residual gas analyzer,SRS,Stanford Research Systems
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: MIT License
@@ -36,15 +36,15 @@
 
 To use its full GUI application, create a virtual environment and install:
 
     python -m pip install srsinst.rga[full]
 
 
 ## Run `srsinst.rga` as GUI application
-if the Python Scripts directory is in PATH environment variable,
+If the Python Scripts directory is in PATH environment variable,
 Start the application by typing from the command line:
 
     rga
 
 If not,
 
     python -m srsinst.rga
@@ -53,18 +53,18 @@
 
 Connect to an RGA from the Instruments menu.
 Select a task from the Task menu.
 Press the green arrow to run the selected task. 
 
 You can write your own task or modify an existing one and run it from the application, too.
 
-## Use `srsinst.rga` as instument driver
+## Use `srsinst.rga` as instrument driver
 * Start the Python program, or an editor of your choice to write a Python script.
-* import the **RGA** class from `rga` package
-* Initialize of an **RGA** instance to connect to an SRS RGA.
+* import the **RGA** class from `rga` package.
+* Instantiate **RGA** to connect to an SRS RGA.
 
         from srsinst.rga import RGA100 as RGA
 
         # for TCPIP communication
         ip_address = '192.168.1.100'
         user_id = 'admin'
         password = 'admin'
```

### Comparing `srsinst.rga-0.2.8/README.md` & `srsinst.rga-0.2.9/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 
 To use its full GUI application, create a virtual environment and install:
 
     python -m pip install srsinst.rga[full]
 
 
 ## Run `srsinst.rga` as GUI application
-if the Python Scripts directory is in PATH environment variable,
+If the Python Scripts directory is in PATH environment variable,
 Start the application by typing from the command line:
 
     rga
 
 If not,
 
     python -m srsinst.rga
@@ -32,18 +32,18 @@
 
 Connect to an RGA from the Instruments menu.
 Select a task from the Task menu.
 Press the green arrow to run the selected task. 
 
 You can write your own task or modify an existing one and run it from the application, too.
 
-## Use `srsinst.rga` as instument driver
+## Use `srsinst.rga` as instrument driver
 * Start the Python program, or an editor of your choice to write a Python script.
-* import the **RGA** class from `rga` package
-* Initialize of an **RGA** instance to connect to an SRS RGA.
+* import the **RGA** class from `rga` package.
+* Instantiate **RGA** to connect to an SRS RGA.
 
         from srsinst.rga import RGA100 as RGA
 
         # for TCPIP communication
         ip_address = '192.168.1.100'
         user_id = 'admin'
         password = 'admin'
```

### Comparing `srsinst.rga-0.2.8/setup.py` & `srsinst.rga-0.2.9/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -32,15 +32,15 @@
     # include_package_data=True,
     long_description=description,
     long_description_content_type='text/markdown',
     python_requires='>=3.7',
     install_requires=[
         'numpy',
         'scipy',
-        "srsgui>=0.1.12"
+        "srsgui>=0.2.4"
     ],
     extras_require={
         'full': ['matplotlib', 'pyside6'],
     },
     entry_points={
         'console_scripts': [
             'rga = srsinst.rga.__main__:main'
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/gaslib.dat` & `srsinst.rga-0.2.9/srsinst/rga/gaslib.dat`

 * *Files identical despite different names*

### Comparing `srsinst.rga-0.2.8/srsinst/rga/instruments/get_instruments.py` & `srsinst.rga-0.2.9/srsinst/rga/instruments/get_instruments.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import logging
-from srsgui.task import Task
-from srsinst.rga import RGA100
+from srsgui import Task
+from srsinst.rga.instruments.rga100.rga import RGA100
 
 logger = logging.getLogger(__name__)
 
 
 def get_rga(task: Task, name=None) -> RGA100:
     """
     Instead of using task.get_instrument() directly in a Task subclass,
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/commands.py` & `srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/commands.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,14 +1,30 @@
 
 from srsgui.inst.exceptions import InstCommunicationError, InstSetError, InstQueryError
 
-from srsgui.inst.commands import IntCommand, IntGetCommand, FloatCommand
+from srsgui.inst.commands import IntCommand, IntGetCommand, FloatCommand, \
+                                 BoolSetCommand
 
+# RGA100 does not allow space between a set command and the following parameter.
+SetCommandFormat = '{}{}'
 
-class RgaIntCommand(IntCommand):
+
+class IntNSCommand(IntCommand):
+    _set_command_format = SetCommandFormat
+
+
+class FloatNSCommand(FloatCommand):
+    _set_command_format = SetCommandFormat
+
+
+class BoolSetNSCommand(BoolSetCommand):
+    _set_command_format = SetCommandFormat
+
+
+class RgaIntCommand(IntNSCommand):
     """
     Descriptor for an RGA100 remote command to
     **set** and **query** an **integer** value.
     Setting a value returns a status byte, which is stored as last_set_status
     """
 
     def __set__(self, instance, value):
@@ -61,30 +77,30 @@
 class RgaTotalPressureCommand(IntGetCommand):
     """
     Descriptor for a RGA100 remote command to **query** total pressure value
     returned as a binary long integer. To set a value is not allowed.
    """
 
     def __get__(self, instance, instance_type):
-        query_string = self.get_command_format.format(self.remote_command)
+        query_string = self._get_command_format.format(self.remote_command)
         reply = None
         try:
             with instance.comm.get_lock():
                 instance.comm._send(query_string)
                 intensity = instance.comm._read_long()
             self._value = intensity
         except InstCommunicationError:
             raise InstQueryError('Error during querying: CMD: {}'.format(query_string))
         except ValueError:
             raise InstQueryError('Error during conversion CMD: {} Reply: {}'
                                  .format(query_string, reply))
         return self._value
 
 
-class RgaStoredCEMGainCommand(FloatCommand):
+class RgaStoredCEMGainCommand(FloatNSCommand):
     """
     Descriptor for a RGA100 remote command
     to  **set**  and **query** Cem gain stored.
     The raw data is stored as the gain divided by 1000.
     And the descriptor converts back to the original value
    """
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/components.py` & `srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/components.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,22 +1,18 @@
 
-from srsgui.inst.exceptions import InstException
-from srsgui.inst.component import Component
-from srsgui.inst.commands import Command, IntGetCommand,\
-                                  FloatCommand, BoolSetCommand, \
-                                  GetCommand
+from srsgui import InstException
+from srsgui import Component
+from srsgui import GetCommand, IntGetCommand
 
-from .commands import RgaIntCommand, RgaFloatCommand, \
+from .commands import FloatNSCommand, BoolSetNSCommand,\
+                      RgaIntCommand, RgaFloatCommand, \
                       RgaIonEnergyCommand, RgaTotalPressureCommand, \
                       RgaStoredCEMGainCommand
 from .errors import query_errors, fetch_error_descriptions
 
-# RGA100 does not allow space between a set command and the following parameter.
-Command._set_command_format = '{}{}'
-
 
 class Ionizer(Component):
     electron_energy = RgaIntCommand('EE')
     ion_energy = RgaIonEnergyCommand('IE')
     focus_voltage = RgaIntCommand('VF')
     emission_current = RgaFloatCommand('FL')
     """
@@ -109,15 +105,15 @@
     stored_gain = RgaStoredCEMGainCommand('MG')
     """ 
     Stored CEM gain. Underlying remote command 'MG' returns 
     the gain divided by 1000. This descriptor generates
     the original value,  1000 times of the raw remote command value.    
      """
 
-    stored_voltage = FloatCommand('MV')
+    stored_voltage = FloatNSCommand('MV')
     voltage = RgaIntCommand('HV')
 
     def turn_on(self):
         """
         Set CEM HV to the stored CEM voltage
         """
         self.voltage = self.stored_voltage
@@ -126,29 +122,29 @@
         """
         Set CEM HV to the stored CEM voltage
         """
         self.voltage = 0
 
 
 class Pressure(Component):
-    partial_pressure_sensitivity = FloatCommand('SP')
+    partial_pressure_sensitivity = FloatNSCommand('SP')
     """
     Partial pressure sensitivity is used to convert a spectrum 
     in current unit to partial pressure unit. 
     The partial pressure sensitivity in the unit of mA/Torr        
     """
 
-    total_pressure_sensitivity = FloatCommand('ST')
+    total_pressure_sensitivity = FloatNSCommand('ST')
     """
     Total pressure sensitivity is used to convert total pressure measured   
     in current unit to pressure unit. 
     The total pressure sensitivity in the unit of mA/Torr
     """
 
-    total_pressure_enable = BoolSetCommand('TP')
+    total_pressure_enable = BoolSetNSCommand('TP')
     total_pressure = RgaTotalPressureCommand('TP')
     """
     Total pressure measured in  ion current in 0.1 fA 
     """
 
     def get_total_pressure_in_torr(self):
         factor = 1e-13 / self.total_pressure_sensitivity
@@ -161,20 +157,20 @@
         if self._parent.cem.voltage > 10:
             factor /= self._parent.cem.stored_gain
         return factor
 
 
 class QMF(Component):
     class RF(Component):
-        offset = FloatCommand('RI')
-        slope = FloatCommand('RS')
+        offset = FloatNSCommand('RI')
+        slope = FloatNSCommand('RS')
 
     class DC(Component):
-        offset = FloatCommand('DI')
-        slope = FloatCommand('DS')
+        offset = FloatNSCommand('DI')
+        slope = FloatNSCommand('DS')
 
     def __init__(self, parent):
         super().__init__(parent)
         self.rf = QMF.RF(self)
         self.dc = QMF.DC(self)
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/errors.py` & `srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/errors.py`

 * *Files identical despite different names*

### Comparing `srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/rga.py` & `srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/rga.py`

 * *Files 3% similar despite different names*

```diff
@@ -6,498 +6,496 @@
 00000050: 4520 666f 7220 6d6f 7265 2064 6574 6169  E for more detai
 00000060: 6c73 2e0d 0a23 0d0a 0d0a 2222 220d 0a4d  ls...#...."""..M
 00000070: 6f64 756c 6520 636f 6e74 6169 6e73 2074  odule contains t
 00000080: 6865 206d 6169 6e20 636c 6173 7320 666f  he main class fo
 00000090: 7220 6f70 6572 6174 696f 6e20 6f66 2053  r operation of S
 000000a0: 5253 2052 4741 3130 3020 7365 7269 6573  RS RGA100 series
 000000b0: 0d0a 2222 220d 0a0d 0a66 726f 6d20 7372  .."""....from sr
-000000c0: 7367 7569 2e69 6e73 742e 696e 7374 7275  sgui.inst.instru
-000000d0: 6d65 6e74 2069 6d70 6f72 7420 496e 7374  ment import Inst
-000000e0: 7275 6d65 6e74 0d0a 6672 6f6d 2073 7273  rument..from srs
-000000f0: 6775 692e 696e 7374 2e65 7863 6570 7469  gui.inst.excepti
-00000100: 6f6e 7320 696d 706f 7274 2049 6e73 7443  ons import InstC
-00000110: 6f6d 6d75 6e69 6361 7469 6f6e 4572 726f  ommunicationErro
-00000120: 722c 205c 0d0a 2020 2020 2020 2020 2020  r, \..          
-00000130: 2020 2020 2020 2020 2020 2020 2020 2049                 I
-00000140: 6e73 744c 6f67 696e 4661 696c 7572 6545  nstLoginFailureE
-00000150: 7272 6f72 2c20 496e 7374 4964 4572 726f  rror, InstIdErro
-00000160: 720d 0a0d 0a66 726f 6d20 7372 7367 7569  r....from srsgui
-00000170: 2e69 6e73 742e 636f 6d6d 756e 6963 6174  .inst.communicat
-00000180: 696f 6e73 2069 6d70 6f72 7420 5365 7269  ions import Seri
-00000190: 616c 496e 7465 7266 6163 652c 2054 6370  alInterface, Tcp
-000001a0: 6970 496e 7465 7266 6163 650d 0a66 726f  ipInterface..fro
-000001b0: 6d20 7372 7367 7569 2e74 6173 6b2e 696e  m srsgui.task.in
-000001c0: 7075 7473 2069 6d70 6f72 7420 4669 6e64  puts import Find
-000001d0: 4c69 7374 496e 7075 742c 2049 7034 496e  ListInput, Ip4In
-000001e0: 7075 742c 2053 7472 696e 6749 6e70 7574  put, StringInput
-000001f0: 2c20 5061 7373 776f 7264 496e 7075 742c  , PasswordInput,
-00000200: 2049 6e74 6567 6572 496e 7075 740d 0a0d   IntegerInput...
-00000210: 0a66 726f 6d20 2e73 6361 6e73 2069 6d70  .from .scans imp
-00000220: 6f72 7420 5363 616e 730d 0a66 726f 6d20  ort Scans..from 
-00000230: 2e63 6f6d 706f 6e65 6e74 7320 696d 706f  .components impo
-00000240: 7274 2051 4d46 2c20 496f 6e69 7a65 722c  rt QMF, Ionizer,
-00000250: 2046 696c 616d 656e 742c 2043 454d 2c20   Filament, CEM, 
-00000260: 5072 6573 7375 7265 2c20 5374 6174 7573  Pressure, Status
-00000270: 0d0a 0d0a 0d0a 636c 6173 7320 4465 6661  ......class Defa
-00000280: 756c 7473 3a0d 0a20 2020 2022 2222 0d0a  ults:..    """..
-00000290: 2020 2020 5352 5320 5247 4120 6465 6661      SRS RGA defa
-000002a0: 756c 7420 7661 6c75 6573 2061 6674 6572  ult values after
-000002b0: 2072 6573 6574 0d0a 2020 2020 2222 220d   reset..    """.
-000002c0: 0a20 2020 2045 6c65 6374 726f 6e45 6e65  .    ElectronEne
-000002d0: 7267 7920 3d20 3730 0d0a 2020 2020 496f  rgy = 70..    Io
-000002e0: 6e45 6e65 7267 7920 3d20 3132 0d0a 2020  nEnergy = 12..  
-000002f0: 2020 466f 6375 7356 6f6c 7461 6765 203d    FocusVoltage =
-00000300: 2039 300d 0a20 2020 2049 6e69 7469 616c   90..    Initial
-00000310: 4d61 7373 203d 2031 0d0a 2020 2020 5363  Mass = 1..    Sc
-00000320: 616e 5370 6565 6420 3d20 340d 0a20 2020  anSpeed = 4..   
-00000330: 2053 7465 7073 5065 7241 6d75 203d 2031   StepsPerAmu = 1
-00000340: 300d 0a0d 0a0d 0a63 6c61 7373 2052 4741  0......class RGA
-00000350: 3130 3028 496e 7374 7275 6d65 6e74 293a  100(Instrument):
-00000360: 0d0a 2020 2020 2222 220d 0a20 2020 2043  ..    """..    C
-00000370: 6c61 7373 2074 6f20 636f 6e74 726f 6c20  lass to control 
-00000380: 616e 6420 6163 7175 6972 6520 6461 7461  and acquire data
-00000390: 2077 6974 680d 0a20 2020 2060 5352 5320   with..    `SRS 
-000003a0: 5247 4131 3030 2c20 3230 302c 2033 3030  RGA100, 200, 300
-000003b0: 2073 6572 6965 7320 3c68 7474 7073 3a2f   series <https:/
-000003c0: 2f77 7777 2e74 6869 6e6b 7372 732e 636f  /www.thinksrs.co
-000003d0: 6d2f 7072 6f64 7563 7473 2f72 6761 2e68  m/products/rga.h
-000003e0: 746d 6c3e 605f 2e0d 0a0d 0a20 2020 2041  tml>`_.....    A
-000003f0: 206e 6174 6976 6520 5352 5320 5247 4120   native SRS RGA 
-00000400: 6861 7320 6120 5253 3233 3220 7365 7269  has a RS232 seri
-00000410: 616c 2070 6f72 7420 7468 6174 2063 6f6e  al port that con
-00000420: 6e65 6374 7320 7769 7468 0d0a 2020 2020  nects with..    
-00000430: 6261 7564 2072 6174 6520 6f66 2032 3838  baud rate of 288
-00000440: 3030 2c20 6f6e 6520 7374 6f70 2062 6974  00, one stop bit
-00000450: 2c20 6e6f 2070 6172 6974 792c 2077 6974  , no parity, wit
-00000460: 6820 5254 532f 4354 5320 666c 6f77 2063  h RTS/CTS flow c
-00000470: 6f6e 7472 6f6c 2e0d 0a0d 0a20 2020 2054  ontrol.....    T
-00000480: 6865 7265 2069 7320 616e 206f 7074 696f  here is an optio
-00000490: 6e20 746f 2061 6464 2045 7468 6572 6e65  n to add Etherne
-000004a0: 7420 636f 6d6d 756e 6963 6174 696f 6e20  t communication 
-000004b0: 7573 696e 670d 0a20 2020 2060 5247 4120  using..    `RGA 
-000004c0: 6574 6865 726e 6574 2061 6461 7074 6572  ethernet adapter
-000004d0: 203c 6874 7470 733a 2f2f 7468 696e 6b73   <https://thinks
-000004e0: 7273 2e63 6f6d 2f64 6f77 6e6c 6f61 6473  rs.com/downloads
-000004f0: 2f70 6466 732f 6d61 6e75 616c 732f 5245  /pdfs/manuals/RE
-00000500: 416d 2e70 6466 3e60 5f0d 0a0d 0a20 2020  Am.pdf>`_....   
-00000510: 2052 4741 3130 3020 636c 6173 7320 7072   RGA100 class pr
-00000520: 6f76 6964 6573 206d 6574 686f 6473 2066  ovides methods f
-00000530: 6f72 2065 7374 6162 6c69 7368 696e 6720  or establishing 
-00000540: 636f 6d6d 756e 6963 6174 696f 6e2c 0d0a  communication,..
-00000550: 2020 2020 6261 7369 6320 6f70 6572 6174      basic operat
-00000560: 696f 6e20 616e 6420 7363 616e 7320 746f  ion and scans to
-00000570: 2061 6371 7569 7265 206d 6173 7320 7370   acquire mass sp
-00000580: 6563 7472 612e 0d0a 0d0a 2020 2020 4578  ectra.....    Ex
-00000590: 616d 706c 650d 0a20 2020 202d 2d2d 2d2d  ample..    -----
-000005a0: 2d2d 2d2d 0d0a 2020 2020 2e2e 2063 6f64  ----..    .. cod
-000005b0: 652d 626c 6f63 6b3a 3a20 7079 7468 6f6e  e-block:: python
-000005c0: 0d0a 0d0a 2020 2020 2020 2020 6672 6f6d  ....        from
-000005d0: 2073 7273 696e 7374 2e72 6761 2069 6d70   srsinst.rga imp
-000005e0: 6f72 7420 5247 4131 3030 0d0a 2020 2020  ort RGA100..    
-000005f0: 2020 2020 7231 203d 2052 4741 3130 3028      r1 = RGA100(
-00000600: 2773 6572 6961 6c27 2c20 2743 4f4d 3327  'serial', 'COM3'
-00000610: 2c20 3238 3830 3029 0d0a 0d0a 2020 2020  , 28800)....    
-00000620: 2020 2020 2320 6966 2045 7468 6572 6e65      # if Etherne
-00000630: 7420 636f 6e6e 6563 7469 6f6e 2069 7320  t connection is 
-00000640: 7573 6564 2c0d 0a20 2020 2020 2020 2023  used,..        #
-00000650: 2072 3120 3d20 5247 4131 3030 2827 7463   r1 = RGA100('tc
-00000660: 7069 7027 2c20 2731 3932 2e31 3638 2e31  pip', '192.168.1
-00000670: 2e31 3030 272c 2027 7573 6572 6964 272c  .100', 'userid',
-00000680: 2027 7061 7373 776f 7264 2729 0d0a 0d0a   'password')....
-00000690: 2020 2020 2020 2020 7231 2e73 6574 5f65          r1.set_e
-000006a0: 6d69 7373 696f 6e5f 6375 7272 656e 7428  mission_current(
-000006b0: 312e 3029 0d0a 2020 2020 2020 2020 7231  1.0)..        r1
-000006c0: 2e73 6574 5f73 6361 6e5f 7061 7261 6d65  .set_scan_parame
-000006d0: 7465 7273 2829 0d0a 0d0a 2020 2020 2020  ters()....      
-000006e0: 2020 7873 203d 2072 312e 6765 745f 6d61    xs = r1.get_ma
-000006f0: 7373 5f61 7869 7328 290d 0a20 2020 2020  ss_axis()..     
-00000700: 2020 2079 7320 3d20 7231 2e67 6574 5f61     ys = r1.get_a
-00000710: 6e61 6c6f 675f 7363 616e 2829 0d0a 0d0a  nalog_scan()....
-00000720: 2020 2020 2020 2020 666f 7220 782c 2079          for x, y
-00000730: 2069 6e20 7a69 7028 7873 2c20 7973 293a   in zip(xs, ys):
-00000740: 0d0a 2020 2020 2020 2020 2020 2020 7072  ..            pr
-00000750: 696e 7428 782c 2079 290d 0a0d 0a20 2020  int(x, y)....   
-00000760: 2020 2020 2072 312e 7365 745f 656d 6973       r1.set_emis
-00000770: 7369 6f6e 5f63 7572 7265 6e74 2830 2e30  sion_current(0.0
-00000780: 290d 0a20 2020 2020 2020 2072 312e 6469  )..        r1.di
-00000790: 7363 6f6e 6e65 6374 2829 0d0a 0d0a 2020  sconnect()....  
-000007a0: 2020 2222 220d 0a0d 0a20 2020 205f 4964    """....    _Id
-000007b0: 5374 7269 6e67 203d 2027 5352 5352 4741  String = 'SRSRGA
-000007c0: 270d 0a20 2020 205f 7465 726d 5f63 6861  '..    _term_cha
-000007d0: 7220 3d20 6227 5c72 270d 0a20 2020 200d  r = b'\r'..    .
-000007e0: 0a20 2020 2061 7661 696c 6162 6c65 5f69  .    available_i
-000007f0: 6e74 6572 6661 6365 7320 3d20 5b0d 0a20  nterfaces = [.. 
-00000800: 2020 2020 2020 205b 2020 2053 6572 6961         [   Seria
-00000810: 6c49 6e74 6572 6661 6365 2c0d 0a20 2020  lInterface,..   
-00000820: 2020 2020 2020 2020 207b 0d0a 2020 2020           {..    
-00000830: 2020 2020 2020 2020 2020 2020 2770 6f72              'por
-00000840: 7427 3a20 4669 6e64 4c69 7374 496e 7075  t': FindListInpu
-00000850: 7428 292c 0d0a 2020 2020 2020 2020 2020  t(),..          
-00000860: 2020 2020 2020 2762 6175 645f 7261 7465        'baud_rate
-00000870: 273a 2032 3838 3030 2c0d 0a20 2020 2020  ': 28800,..     
-00000880: 2020 2020 2020 2020 2020 2027 6861 7264             'hard
-00000890: 7761 7265 5f66 6c6f 775f 636f 6e74 726f  ware_flow_contro
-000008a0: 6c27 3a20 5472 7565 0d0a 2020 2020 2020  l': True..      
-000008b0: 2020 2020 2020 7d0d 0a20 2020 2020 2020        }..       
-000008c0: 205d 2c0d 0a20 2020 2020 2020 205b 2020   ],..        [  
-000008d0: 2054 6370 6970 496e 7465 7266 6163 652c   TcpipInterface,
-000008e0: 0d0a 2020 2020 2020 2020 2020 2020 7b0d  ..            {.
-000008f0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
-00000900: 2027 6970 5f61 6464 7265 7373 273a 2049   'ip_address': I
-00000910: 7034 496e 7075 7428 2731 3932 2e31 3638  p4Input('192.168
-00000920: 2e31 2e31 3027 292c 0d0a 2020 2020 2020  .1.10'),..      
-00000930: 2020 2020 2020 2020 2020 2775 7365 725f            'user_
-00000940: 6964 273a 2053 7472 696e 6749 6e70 7574  id': StringInput
-00000950: 2827 6164 6d69 6e27 292c 0d0a 2020 2020  ('admin'),..    
-00000960: 2020 2020 2020 2020 2020 2020 2770 6173              'pas
-00000970: 7377 6f72 6427 3a20 5061 7373 776f 7264  sword': Password
-00000980: 496e 7075 7428 2761 646d 696e 2729 2c0d  Input('admin'),.
-00000990: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
-000009a0: 2027 706f 7274 273a 2038 3138 0d0a 2020   'port': 818..  
-000009b0: 2020 2020 2020 2020 2020 7d0d 0a20 2020            }..   
-000009c0: 2020 2020 205d 2c0d 0a20 2020 205d 0d0a       ],..    ]..
-000009d0: 0d0a 2020 2020 6465 6620 5f5f 696e 6974  ..    def __init
-000009e0: 5f5f 2873 656c 662c 2069 6e74 6572 6661  __(self, interfa
-000009f0: 6365 5f74 7970 653d 4e6f 6e65 2c20 2a61  ce_type=None, *a
-00000a00: 7267 7329 3a0d 0a0d 0a20 2020 2020 2020  rgs):....       
-00000a10: 2073 7570 6572 2829 2e5f 5f69 6e69 745f   super().__init_
-00000a20: 5f28 696e 7465 7266 6163 655f 7479 7065  _(interface_type
-00000a30: 2c20 2a61 7267 7329 0d0a 2020 2020 2020  , *args)..      
-00000a40: 2020 7365 6c66 2e73 6574 5f74 6572 6d5f    self.set_term_
-00000a50: 6368 6172 2862 275c 7227 290d 0a20 2020  char(b'\r')..   
-00000a60: 2020 2020 2073 656c 662e 5f6d 5f6d 6178       self._m_max
-00000a70: 203d 2031 3030 0d0a 0d0a 2020 2020 2020   = 100....      
-00000a80: 2020 2320 4164 6420 636f 6d70 6f6e 656e    # Add componen
-00000a90: 7473 0d0a 2020 2020 2020 2020 7365 6c66  ts..        self
-00000aa0: 2e73 6361 6e20 3d20 5363 616e 7328 7365  .scan = Scans(se
-00000ab0: 6c66 290d 0a20 2020 2020 2020 2073 656c  lf)..        sel
-00000ac0: 662e 696f 6e69 7a65 7220 3d20 496f 6e69  f.ionizer = Ioni
-00000ad0: 7a65 7228 7365 6c66 290d 0a20 2020 2020  zer(self)..     
-00000ae0: 2020 2073 656c 662e 6669 6c61 6d65 6e74     self.filament
-00000af0: 203d 2046 696c 616d 656e 7428 7365 6c66   = Filament(self
-00000b00: 290d 0a20 2020 2020 2020 2073 656c 662e  )..        self.
-00000b10: 6365 6d20 3d20 4345 4d28 7365 6c66 290d  cem = CEM(self).
-00000b20: 0a20 2020 2020 2020 2073 656c 662e 716d  .        self.qm
-00000b30: 6620 3d20 514d 4628 7365 6c66 290d 0a20  f = QMF(self).. 
-00000b40: 2020 2020 2020 2073 656c 662e 7072 6573         self.pres
-00000b50: 7375 7265 203d 2050 7265 7373 7572 6528  sure = Pressure(
-00000b60: 7365 6c66 290d 0a20 2020 2020 2020 2073  self)..        s
-00000b70: 656c 662e 7374 6174 7573 203d 2053 7461  elf.status = Sta
-00000b80: 7475 7328 7365 6c66 290d 0a0d 0a20 2020  tus(self)....   
-00000b90: 2064 6566 2063 6f6e 6e65 6374 2873 656c   def connect(sel
-00000ba0: 662c 2069 6e74 6572 6661 6365 5f74 7970  f, interface_typ
-00000bb0: 652c 202a 6172 6773 293a 0d0a 2020 2020  e, *args):..    
-00000bc0: 2020 2020 2222 220d 0a20 2020 2020 2020      """..       
-00000bd0: 2043 6f6e 6e65 6374 2074 6f20 616e 2069   Connect to an i
-00000be0: 6e73 7472 756d 656e 7420 6f76 6572 2074  nstrument over t
-00000bf0: 6865 2073 7065 6369 6669 6564 2063 6f6d  he specified com
-00000c00: 6d75 6e69 6361 7469 6f6e 2069 6e74 6572  munication inter
-00000c10: 6661 6365 0d0a 0d0a 2020 2020 2020 2020  face....        
-00000c20: 4966 2069 6e74 6572 6661 6365 5f74 7970  If interface_typ
-00000c30: 6520 6973 2027 7365 7269 616c 272c 0d0a  e is 'serial',..
-00000c40: 0d0a 2020 2020 2020 2020 5061 7261 6d65  ..        Parame
-00000c50: 7465 7273 0d0a 2020 2020 2020 2020 2d2d  ters..        --
-00000c60: 2d2d 2d2d 2d2d 2d2d 2d0d 0a20 2020 2020  ---------..     
-00000c70: 2020 2020 2020 2069 6e74 6572 6661 6365         interface
-00000c80: 5f74 7970 653a 2073 7472 0d0a 2020 2020  _type: str..    
-00000c90: 2020 2020 2020 2020 2020 2020 5573 6520              Use 
-00000ca0: 2a2a 2773 6572 6961 6c27 2a2a 2066 6f72  **'serial'** for
-00000cb0: 2073 6572 6961 6c20 636f 6d6d 756e 6963   serial communic
-00000cc0: 6174 696f 6e0d 0a20 2020 2020 2020 2020  ation..         
-00000cd0: 2020 2070 6f72 7420 3a20 7374 7269 6e67     port : string
-00000ce0: 0d0a 2020 2020 2020 2020 2020 2020 2020  ..              
-00000cf0: 2020 7365 7269 616c 2070 6f72 742c 2020    serial port,  
-00000d00: 7375 6368 2061 7320 2743 4f4d 3327 206f  such as 'COM3' o
-00000d10: 7220 272f 6465 762f 7474 7955 5342 3027  r '/dev/ttyUSB0'
-00000d20: 0d0a 2020 2020 2020 2020 2020 2020 6261  ..            ba
-00000d30: 7564 5f72 6174 6520 3a20 696e 742c 206f  ud_rate : int, o
-00000d40: 7074 696f 6e61 6c0d 0a20 2020 2020 2020  ptional..       
-00000d50: 2020 2020 2020 2020 2062 6175 6420 7261           baud ra
-00000d60: 7465 206f 6620 7468 6520 7365 7269 616c  te of the serial
-00000d70: 2070 6f72 742c 2064 6566 6175 6c74 2069   port, default i
-00000d80: 7320 3131 3432 3030 2c20 616e 6420 5352  s 114200, and SR
-00000d90: 5320 5247 4120 7573 6573 2032 3838 3030  S RGA uses 28800
-00000da0: 2e0d 0a20 2020 2020 2020 2020 2020 2068  ...            h
-00000db0: 6172 6477 6172 655f 666c 6f77 5f63 6f6e  ardware_flow_con
-00000dc0: 7472 6f6c 3a20 626f 6f6c 2c20 6f70 7469  trol: bool, opti
-00000dd0: 6f6e 616c 0d0a 2020 2020 2020 2020 2020  onal..          
-00000de0: 2020 2020 2020 5254 532f 4354 5320 7365        RTS/CTS se
-00000df0: 7474 696e 672e 2054 6865 2064 6566 6175  tting. The defau
-00000e00: 6c74 2069 7320 4661 6c73 652c 2053 5253  lt is False, SRS
-00000e10: 2052 4741 2072 6571 7569 7265 7320 2a2a   RGA requires **
-00000e20: 5472 7565 2a2a 2e0d 0a0d 0a20 2020 2020  True**.....     
-00000e30: 2020 2049 6620 696e 7465 7266 6163 655f     If interface_
-00000e40: 7479 7065 2069 7320 2774 6370 6970 272c  type is 'tcpip',
-00000e50: 0d0a 0d0a 2020 2020 2020 2020 5061 7261  ....        Para
-00000e60: 6d65 7465 7273 0d0a 2020 2020 2020 2020  meters..        
-00000e70: 2d2d 2d2d 2d2d 2d2d 2d2d 2d0d 0a20 2020  -----------..   
-00000e80: 2020 2020 2020 2020 2069 6e74 6572 6661           interfa
-00000e90: 6365 5f74 7970 653a 2073 7472 0d0a 2020  ce_type: str..  
-00000ea0: 2020 2020 2020 2020 2020 2020 2020 5573                Us
-00000eb0: 6520 2a2a 2774 6370 6970 272a 2a20 666f  e **'tcpip'** fo
-00000ec0: 7220 4574 6865 726e 6574 2063 6f6d 6d75  r Ethernet commu
-00000ed0: 6e69 6361 7469 6f6e 0d0a 2020 2020 2020  nication..      
-00000ee0: 2020 2020 2020 6970 5f61 6464 7265 7373        ip_address
+000000c0: 7367 7569 2069 6d70 6f72 7420 496e 7374  sgui import Inst
+000000d0: 7275 6d65 6e74 0d0a 6672 6f6d 2073 7273  rument..from srs
+000000e0: 6775 6920 696d 706f 7274 2049 6e73 7443  gui import InstC
+000000f0: 6f6d 6d75 6e69 6361 7469 6f6e 4572 726f  ommunicationErro
+00000100: 722c 205c 0d0a 2020 2020 2020 2020 2020  r, \..          
+00000110: 2020 2020 2020 2020 2049 6e73 744c 6f67           InstLog
+00000120: 696e 4661 696c 7572 6545 7272 6f72 2c20  inFailureError, 
+00000130: 496e 7374 4964 4572 726f 720d 0a0d 0a66  InstIdError....f
+00000140: 726f 6d20 7372 7367 7569 2069 6d70 6f72  rom srsgui impor
+00000150: 7420 5365 7269 616c 496e 7465 7266 6163  t SerialInterfac
+00000160: 652c 2054 6370 6970 496e 7465 7266 6163  e, TcpipInterfac
+00000170: 650d 0a66 726f 6d20 7372 7367 7569 2069  e..from srsgui i
+00000180: 6d70 6f72 7420 4669 6e64 4c69 7374 496e  mport FindListIn
+00000190: 7075 742c 2049 7034 496e 7075 742c 2053  put, Ip4Input, S
+000001a0: 7472 696e 6749 6e70 7574 2c20 5061 7373  tringInput, Pass
+000001b0: 776f 7264 496e 7075 742c 2049 6e74 6567  wordInput, Integ
+000001c0: 6572 496e 7075 740d 0a0d 0a66 726f 6d20  erInput....from 
+000001d0: 2e73 6361 6e73 2069 6d70 6f72 7420 5363  .scans import Sc
+000001e0: 616e 730d 0a66 726f 6d20 2e63 6f6d 706f  ans..from .compo
+000001f0: 6e65 6e74 7320 696d 706f 7274 2051 4d46  nents import QMF
+00000200: 2c20 496f 6e69 7a65 722c 2046 696c 616d  , Ionizer, Filam
+00000210: 656e 742c 2043 454d 2c20 5072 6573 7375  ent, CEM, Pressu
+00000220: 7265 2c20 5374 6174 7573 0d0a 0d0a 0d0a  re, Status......
+00000230: 636c 6173 7320 4465 6661 756c 7473 3a0d  class Defaults:.
+00000240: 0a20 2020 2022 2222 0d0a 2020 2020 5352  .    """..    SR
+00000250: 5320 5247 4120 6465 6661 756c 7420 7661  S RGA default va
+00000260: 6c75 6573 2061 6674 6572 2072 6573 6574  lues after reset
+00000270: 0d0a 2020 2020 2222 220d 0a20 2020 2045  ..    """..    E
+00000280: 6c65 6374 726f 6e45 6e65 7267 7920 3d20  lectronEnergy = 
+00000290: 3730 0d0a 2020 2020 496f 6e45 6e65 7267  70..    IonEnerg
+000002a0: 7920 3d20 3132 0d0a 2020 2020 466f 6375  y = 12..    Focu
+000002b0: 7356 6f6c 7461 6765 203d 2039 300d 0a20  sVoltage = 90.. 
+000002c0: 2020 2049 6e69 7469 616c 4d61 7373 203d     InitialMass =
+000002d0: 2031 0d0a 2020 2020 5363 616e 5370 6565   1..    ScanSpee
+000002e0: 6420 3d20 340d 0a20 2020 2053 7465 7073  d = 4..    Steps
+000002f0: 5065 7241 6d75 203d 2031 300d 0a0d 0a0d  PerAmu = 10.....
+00000300: 0a63 6c61 7373 2052 4741 3130 3028 496e  .class RGA100(In
+00000310: 7374 7275 6d65 6e74 293a 0d0a 2020 2020  strument):..    
+00000320: 2222 220d 0a20 2020 2043 6c61 7373 2074  """..    Class t
+00000330: 6f20 636f 6e74 726f 6c20 616e 6420 6163  o control and ac
+00000340: 7175 6972 6520 6461 7461 2077 6974 680d  quire data with.
+00000350: 0a20 2020 2060 5352 5320 5247 4131 3030  .    `SRS RGA100
+00000360: 2c20 3230 302c 2033 3030 2073 6572 6965  , 200, 300 serie
+00000370: 7320 3c68 7474 7073 3a2f 2f77 7777 2e74  s <https://www.t
+00000380: 6869 6e6b 7372 732e 636f 6d2f 7072 6f64  hinksrs.com/prod
+00000390: 7563 7473 2f72 6761 2e68 746d 6c3e 605f  ucts/rga.html>`_
+000003a0: 2e0d 0a0d 0a20 2020 2041 206e 6174 6976  .....    A nativ
+000003b0: 6520 5352 5320 5247 4120 6861 7320 6120  e SRS RGA has a 
+000003c0: 5253 3233 3220 7365 7269 616c 2070 6f72  RS232 serial por
+000003d0: 7420 7468 6174 2063 6f6e 6e65 6374 7320  t that connects 
+000003e0: 7769 7468 0d0a 2020 2020 6261 7564 2072  with..    baud r
+000003f0: 6174 6520 6f66 2032 3838 3030 2c20 6f6e  ate of 28800, on
+00000400: 6520 7374 6f70 2062 6974 2c20 6e6f 2070  e stop bit, no p
+00000410: 6172 6974 792c 2077 6974 6820 5254 532f  arity, with RTS/
+00000420: 4354 5320 666c 6f77 2063 6f6e 7472 6f6c  CTS flow control
+00000430: 2e0d 0a0d 0a20 2020 2054 6865 7265 2069  .....    There i
+00000440: 7320 616e 206f 7074 696f 6e20 746f 2061  s an option to a
+00000450: 6464 2045 7468 6572 6e65 7420 636f 6d6d  dd Ethernet comm
+00000460: 756e 6963 6174 696f 6e20 7573 696e 670d  unication using.
+00000470: 0a20 2020 2060 5247 4120 6574 6865 726e  .    `RGA ethern
+00000480: 6574 2061 6461 7074 6572 203c 6874 7470  et adapter <http
+00000490: 733a 2f2f 7468 696e 6b73 7273 2e63 6f6d  s://thinksrs.com
+000004a0: 2f64 6f77 6e6c 6f61 6473 2f70 6466 732f  /downloads/pdfs/
+000004b0: 6d61 6e75 616c 732f 5245 416d 2e70 6466  manuals/REAm.pdf
+000004c0: 3e60 5f0d 0a0d 0a20 2020 2052 4741 3130  >`_....    RGA10
+000004d0: 3020 636c 6173 7320 7072 6f76 6964 6573  0 class provides
+000004e0: 206d 6574 686f 6473 2066 6f72 2065 7374   methods for est
+000004f0: 6162 6c69 7368 696e 6720 636f 6d6d 756e  ablishing commun
+00000500: 6963 6174 696f 6e2c 0d0a 2020 2020 6261  ication,..    ba
+00000510: 7369 6320 6f70 6572 6174 696f 6e20 616e  sic operation an
+00000520: 6420 7363 616e 7320 746f 2061 6371 7569  d scans to acqui
+00000530: 7265 206d 6173 7320 7370 6563 7472 612e  re mass spectra.
+00000540: 0d0a 0d0a 2020 2020 4578 616d 706c 650d  ....    Example.
+00000550: 0a20 2020 202d 2d2d 2d2d 2d2d 2d2d 0d0a  .    ---------..
+00000560: 2020 2020 2e2e 2063 6f64 652d 626c 6f63      .. code-bloc
+00000570: 6b3a 3a20 7079 7468 6f6e 0d0a 0d0a 2020  k:: python....  
+00000580: 2020 2020 2020 6672 6f6d 2073 7273 696e        from srsin
+00000590: 7374 2e72 6761 2069 6d70 6f72 7420 5247  st.rga import RG
+000005a0: 4131 3030 0d0a 2020 2020 2020 2020 7231  A100..        r1
+000005b0: 203d 2052 4741 3130 3028 2773 6572 6961   = RGA100('seria
+000005c0: 6c27 2c20 2743 4f4d 3327 2c20 3238 3830  l', 'COM3', 2880
+000005d0: 3029 0d0a 0d0a 2020 2020 2020 2020 2320  0)....        # 
+000005e0: 6966 2045 7468 6572 6e65 7420 636f 6e6e  if Ethernet conn
+000005f0: 6563 7469 6f6e 2069 7320 7573 6564 2c0d  ection is used,.
+00000600: 0a20 2020 2020 2020 2023 2072 3120 3d20  .        # r1 = 
+00000610: 5247 4131 3030 2827 7463 7069 7027 2c20  RGA100('tcpip', 
+00000620: 2731 3932 2e31 3638 2e31 2e31 3030 272c  '192.168.1.100',
+00000630: 2027 7573 6572 6964 272c 2027 7061 7373   'userid', 'pass
+00000640: 776f 7264 2729 0d0a 0d0a 2020 2020 2020  word')....      
+00000650: 2020 7231 2e73 6574 5f65 6d69 7373 696f    r1.set_emissio
+00000660: 6e5f 6375 7272 656e 7428 312e 3029 0d0a  n_current(1.0)..
+00000670: 2020 2020 2020 2020 7231 2e73 6574 5f73          r1.set_s
+00000680: 6361 6e5f 7061 7261 6d65 7465 7273 2829  can_parameters()
+00000690: 0d0a 0d0a 2020 2020 2020 2020 7873 203d  ....        xs =
+000006a0: 2072 312e 6765 745f 6d61 7373 5f61 7869   r1.get_mass_axi
+000006b0: 7328 290d 0a20 2020 2020 2020 2079 7320  s()..        ys 
+000006c0: 3d20 7231 2e67 6574 5f61 6e61 6c6f 675f  = r1.get_analog_
+000006d0: 7363 616e 2829 0d0a 0d0a 2020 2020 2020  scan()....      
+000006e0: 2020 666f 7220 782c 2079 2069 6e20 7a69    for x, y in zi
+000006f0: 7028 7873 2c20 7973 293a 0d0a 2020 2020  p(xs, ys):..    
+00000700: 2020 2020 2020 2020 7072 696e 7428 782c          print(x,
+00000710: 2079 290d 0a0d 0a20 2020 2020 2020 2072   y)....        r
+00000720: 312e 7365 745f 656d 6973 7369 6f6e 5f63  1.set_emission_c
+00000730: 7572 7265 6e74 2830 2e30 290d 0a20 2020  urrent(0.0)..   
+00000740: 2020 2020 2072 312e 6469 7363 6f6e 6e65       r1.disconne
+00000750: 6374 2829 0d0a 0d0a 2020 2020 2222 220d  ct()....    """.
+00000760: 0a0d 0a20 2020 205f 4964 5374 7269 6e67  ...    _IdString
+00000770: 203d 2027 5352 5352 4741 270d 0a20 2020   = 'SRSRGA'..   
+00000780: 205f 7465 726d 5f63 6861 7220 3d20 6227   _term_char = b'
+00000790: 5c72 270d 0a20 2020 200d 0a20 2020 2061  \r'..    ..    a
+000007a0: 7661 696c 6162 6c65 5f69 6e74 6572 6661  vailable_interfa
+000007b0: 6365 7320 3d20 5b0d 0a20 2020 2020 2020  ces = [..       
+000007c0: 205b 2020 2053 6572 6961 6c49 6e74 6572   [   SerialInter
+000007d0: 6661 6365 2c0d 0a20 2020 2020 2020 2020  face,..         
+000007e0: 2020 207b 0d0a 2020 2020 2020 2020 2020     {..          
+000007f0: 2020 2020 2020 2770 6f72 7427 3a20 4669        'port': Fi
+00000800: 6e64 4c69 7374 496e 7075 7428 292c 0d0a  ndListInput(),..
+00000810: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000820: 2762 6175 645f 7261 7465 273a 2032 3838  'baud_rate': 288
+00000830: 3030 2c0d 0a20 2020 2020 2020 2020 2020  00,..           
+00000840: 2020 2020 2027 6861 7264 7761 7265 5f66       'hardware_f
+00000850: 6c6f 775f 636f 6e74 726f 6c27 3a20 5472  low_control': Tr
+00000860: 7565 0d0a 2020 2020 2020 2020 2020 2020  ue..            
+00000870: 7d0d 0a20 2020 2020 2020 205d 2c0d 0a20  }..        ],.. 
+00000880: 2020 2020 2020 205b 2020 2054 6370 6970         [   Tcpip
+00000890: 496e 7465 7266 6163 652c 0d0a 2020 2020  Interface,..    
+000008a0: 2020 2020 2020 2020 7b0d 0a20 2020 2020          {..     
+000008b0: 2020 2020 2020 2020 2020 2027 6970 5f61             'ip_a
+000008c0: 6464 7265 7373 273a 2049 7034 496e 7075  ddress': Ip4Inpu
+000008d0: 7428 2731 3932 2e31 3638 2e31 2e31 3027  t('192.168.1.10'
+000008e0: 292c 0d0a 2020 2020 2020 2020 2020 2020  ),..            
+000008f0: 2020 2020 2775 7365 725f 6964 273a 2053      'user_id': S
+00000900: 7472 696e 6749 6e70 7574 2827 6164 6d69  tringInput('admi
+00000910: 6e27 292c 0d0a 2020 2020 2020 2020 2020  n'),..          
+00000920: 2020 2020 2020 2770 6173 7377 6f72 6427        'password'
+00000930: 3a20 5061 7373 776f 7264 496e 7075 7428  : PasswordInput(
+00000940: 2761 646d 696e 2729 2c0d 0a20 2020 2020  'admin'),..     
+00000950: 2020 2020 2020 2020 2020 2027 706f 7274             'port
+00000960: 273a 2038 3138 0d0a 2020 2020 2020 2020  ': 818..        
+00000970: 2020 2020 7d0d 0a20 2020 2020 2020 205d      }..        ]
+00000980: 2c0d 0a20 2020 205d 0d0a 0d0a 2020 2020  ,..    ]....    
+00000990: 6465 6620 5f5f 696e 6974 5f5f 2873 656c  def __init__(sel
+000009a0: 662c 2069 6e74 6572 6661 6365 5f74 7970  f, interface_typ
+000009b0: 653d 4e6f 6e65 2c20 2a61 7267 7329 3a0d  e=None, *args):.
+000009c0: 0a0d 0a20 2020 2020 2020 2073 7570 6572  ...        super
+000009d0: 2829 2e5f 5f69 6e69 745f 5f28 696e 7465  ().__init__(inte
+000009e0: 7266 6163 655f 7479 7065 2c20 2a61 7267  rface_type, *arg
+000009f0: 7329 0d0a 2020 2020 2020 2020 7365 6c66  s)..        self
+00000a00: 2e73 6574 5f74 6572 6d5f 6368 6172 2862  .set_term_char(b
+00000a10: 275c 7227 290d 0a20 2020 2020 2020 2073  '\r')..        s
+00000a20: 656c 662e 5f6d 5f6d 6178 203d 2031 3030  elf._m_max = 100
+00000a30: 0d0a 0d0a 2020 2020 2020 2020 2320 4164  ....        # Ad
+00000a40: 6420 636f 6d70 6f6e 656e 7473 0d0a 2020  d components..  
+00000a50: 2020 2020 2020 7365 6c66 2e73 6361 6e20        self.scan 
+00000a60: 3d20 5363 616e 7328 7365 6c66 290d 0a20  = Scans(self).. 
+00000a70: 2020 2020 2020 2073 656c 662e 696f 6e69         self.ioni
+00000a80: 7a65 7220 3d20 496f 6e69 7a65 7228 7365  zer = Ionizer(se
+00000a90: 6c66 290d 0a20 2020 2020 2020 2073 656c  lf)..        sel
+00000aa0: 662e 6669 6c61 6d65 6e74 203d 2046 696c  f.filament = Fil
+00000ab0: 616d 656e 7428 7365 6c66 290d 0a20 2020  ament(self)..   
+00000ac0: 2020 2020 2073 656c 662e 6365 6d20 3d20       self.cem = 
+00000ad0: 4345 4d28 7365 6c66 290d 0a20 2020 2020  CEM(self)..     
+00000ae0: 2020 2073 656c 662e 716d 6620 3d20 514d     self.qmf = QM
+00000af0: 4628 7365 6c66 290d 0a20 2020 2020 2020  F(self)..       
+00000b00: 2073 656c 662e 7072 6573 7375 7265 203d   self.pressure =
+00000b10: 2050 7265 7373 7572 6528 7365 6c66 290d   Pressure(self).
+00000b20: 0a20 2020 2020 2020 2073 656c 662e 7374  .        self.st
+00000b30: 6174 7573 203d 2053 7461 7475 7328 7365  atus = Status(se
+00000b40: 6c66 290d 0a0d 0a20 2020 2064 6566 2063  lf)....    def c
+00000b50: 6f6e 6e65 6374 2873 656c 662c 2069 6e74  onnect(self, int
+00000b60: 6572 6661 6365 5f74 7970 652c 202a 6172  erface_type, *ar
+00000b70: 6773 293a 0d0a 2020 2020 2020 2020 2222  gs):..        ""
+00000b80: 220d 0a20 2020 2020 2020 2043 6f6e 6e65  "..        Conne
+00000b90: 6374 2074 6f20 616e 2069 6e73 7472 756d  ct to an instrum
+00000ba0: 656e 7420 6f76 6572 2074 6865 2073 7065  ent over the spe
+00000bb0: 6369 6669 6564 2063 6f6d 6d75 6e69 6361  cified communica
+00000bc0: 7469 6f6e 2069 6e74 6572 6661 6365 0d0a  tion interface..
+00000bd0: 0d0a 2020 2020 2020 2020 4966 2069 6e74  ..        If int
+00000be0: 6572 6661 6365 5f74 7970 6520 6973 2027  erface_type is '
+00000bf0: 7365 7269 616c 272c 0d0a 0d0a 2020 2020  serial',....    
+00000c00: 2020 2020 5061 7261 6d65 7465 7273 0d0a      Parameters..
+00000c10: 2020 2020 2020 2020 2d2d 2d2d 2d2d 2d2d          --------
+00000c20: 2d2d 2d0d 0a20 2020 2020 2020 2020 2020  ---..           
+00000c30: 2069 6e74 6572 6661 6365 5f74 7970 653a   interface_type:
+00000c40: 2073 7472 0d0a 2020 2020 2020 2020 2020   str..          
+00000c50: 2020 2020 2020 5573 6520 2a2a 2773 6572        Use **'ser
+00000c60: 6961 6c27 2a2a 2066 6f72 2073 6572 6961  ial'** for seria
+00000c70: 6c20 636f 6d6d 756e 6963 6174 696f 6e0d  l communication.
+00000c80: 0a20 2020 2020 2020 2020 2020 2070 6f72  .            por
+00000c90: 7420 3a20 7374 7269 6e67 0d0a 2020 2020  t : string..    
+00000ca0: 2020 2020 2020 2020 2020 2020 7365 7269              seri
+00000cb0: 616c 2070 6f72 742c 2020 7375 6368 2061  al port,  such a
+00000cc0: 7320 2743 4f4d 3327 206f 7220 272f 6465  s 'COM3' or '/de
+00000cd0: 762f 7474 7955 5342 3027 0d0a 2020 2020  v/ttyUSB0'..    
+00000ce0: 2020 2020 2020 2020 6261 7564 5f72 6174          baud_rat
+00000cf0: 6520 3a20 696e 742c 206f 7074 696f 6e61  e : int, optiona
+00000d00: 6c0d 0a20 2020 2020 2020 2020 2020 2020  l..             
+00000d10: 2020 2062 6175 6420 7261 7465 206f 6620     baud rate of 
+00000d20: 7468 6520 7365 7269 616c 2070 6f72 742c  the serial port,
+00000d30: 2064 6566 6175 6c74 2069 7320 3131 3432   default is 1142
+00000d40: 3030 2c20 616e 6420 5352 5320 5247 4120  00, and SRS RGA 
+00000d50: 7573 6573 2032 3838 3030 2e0d 0a20 2020  uses 28800...   
+00000d60: 2020 2020 2020 2020 2068 6172 6477 6172           hardwar
+00000d70: 655f 666c 6f77 5f63 6f6e 7472 6f6c 3a20  e_flow_control: 
+00000d80: 626f 6f6c 2c20 6f70 7469 6f6e 616c 0d0a  bool, optional..
+00000d90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000da0: 5254 532f 4354 5320 7365 7474 696e 672e  RTS/CTS setting.
+00000db0: 2054 6865 2064 6566 6175 6c74 2069 7320   The default is 
+00000dc0: 4661 6c73 652c 2053 5253 2052 4741 2072  False, SRS RGA r
+00000dd0: 6571 7569 7265 7320 2a2a 5472 7565 2a2a  equires **True**
+00000de0: 2e0d 0a0d 0a20 2020 2020 2020 2049 6620  .....        If 
+00000df0: 696e 7465 7266 6163 655f 7479 7065 2069  interface_type i
+00000e00: 7320 2774 6370 6970 272c 0d0a 0d0a 2020  s 'tcpip',....  
+00000e10: 2020 2020 2020 5061 7261 6d65 7465 7273        Parameters
+00000e20: 0d0a 2020 2020 2020 2020 2d2d 2d2d 2d2d  ..        ------
+00000e30: 2d2d 2d2d 2d0d 0a20 2020 2020 2020 2020  -----..         
+00000e40: 2020 2069 6e74 6572 6661 6365 5f74 7970     interface_typ
+00000e50: 653a 2073 7472 0d0a 2020 2020 2020 2020  e: str..        
+00000e60: 2020 2020 2020 2020 5573 6520 2a2a 2774          Use **'t
+00000e70: 6370 6970 272a 2a20 666f 7220 4574 6865  cpip'** for Ethe
+00000e80: 726e 6574 2063 6f6d 6d75 6e69 6361 7469  rnet communicati
+00000e90: 6f6e 0d0a 2020 2020 2020 2020 2020 2020  on..            
+00000ea0: 6970 5f61 6464 7265 7373 3a20 7374 720d  ip_address: str.
+00000eb0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00000ec0: 2049 5020 6164 6472 6573 7320 6f66 2061   IP address of a
+00000ed0: 2069 6e73 7472 756d 656e 740d 0a20 2020   instrument..   
+00000ee0: 2020 2020 2020 2020 2075 7365 725f 6964           user_id
 00000ef0: 3a20 7374 720d 0a20 2020 2020 2020 2020  : str..         
-00000f00: 2020 2020 2020 2049 5020 6164 6472 6573         IP addres
-00000f10: 7320 6f66 2061 2069 6e73 7472 756d 656e  s of a instrumen
-00000f20: 740d 0a20 2020 2020 2020 2020 2020 2075  t..            u
-00000f30: 7365 725f 6964 3a20 7374 720d 0a20 2020  ser_id: str..   
-00000f40: 2020 2020 2020 2020 2020 2020 2075 7365               use
-00000f50: 7220 6e61 6d65 2066 6f72 206c 6f67 696e  r name for login
-00000f60: 2e0d 0a20 2020 2020 2020 2020 2020 2070  ...            p
-00000f70: 6173 7377 6f72 6420 3a20 7374 720d 0a20  assword : str.. 
-00000f80: 2020 2020 2020 2020 2020 2020 2020 2070                 p
-00000f90: 6173 7377 6f72 6420 666f 7220 6c6f 6769  assword for logi
-00000fa0: 6e2e 0d0a 2020 2020 2020 2020 2020 2020  n...            
-00000fb0: 706f 7274 203a 2069 6e74 2c20 6f70 7469  port : int, opti
-00000fc0: 6f6e 616c 0d0a 2020 2020 2020 2020 2020  onal..          
-00000fd0: 2020 2020 2020 5443 5020 706f 7274 206e        TCP port n
-00000fe0: 756d 6265 722e 2054 6865 2064 6566 6175  umber. The defau
-00000ff0: 6c74 2069 7320 3831 382c 2077 6869 6368  lt is 818, which
-00001000: 2053 5253 2052 4741 2075 7365 730d 0a0d   SRS RGA uses...
-00001010: 0a20 2020 2020 2020 2022 2222 0d0a 2020  .        """..  
-00001020: 2020 2020 2020 7375 7065 7228 292e 636f        super().co
-00001030: 6e6e 6563 7428 696e 7465 7266 6163 655f  nnect(interface_
-00001040: 7479 7065 2c20 2a61 7267 7329 0d0a 2020  type, *args)..  
-00001050: 2020 2020 2020 6966 2074 7970 6528 7365        if type(se
-00001060: 6c66 2e63 6f6d 6d29 203d 3d20 5365 7269  lf.comm) == Seri
-00001070: 616c 496e 7465 7266 6163 653a 0d0a 2020  alInterface:..  
-00001080: 2020 2020 2020 2020 2020 2320 4d61 6b65            # Make
-00001090: 2073 7572 6520 7468 6520 6861 7264 7761   sure the hardwa
-000010a0: 7265 2066 6c6f 7720 636f 6e74 726f 6c20  re flow control 
-000010b0: 6973 2073 6574 0d0a 2020 2020 2020 2020  is set..        
-000010c0: 2020 2020 7365 6c66 2e63 6f6d 6d2e 5f73      self.comm._s
-000010d0: 6572 6961 6c2e 7274 7363 7473 203d 2054  erial.rtscts = T
-000010e0: 7275 650d 0a0d 0a20 2020 2064 6566 2063  rue....    def c
-000010f0: 6865 636b 5f69 6428 7365 6c66 293a 0d0a  heck_id(self):..
-00001100: 0d0a 2020 2020 2020 2020 7365 6c66 2e5f  ..        self._
-00001110: 6d5f 6d61 7820 3d20 3130 300d 0a20 2020  m_max = 100..   
-00001120: 2020 2020 2069 6620 6e6f 7420 7365 6c66       if not self
-00001130: 2e69 735f 636f 6e6e 6563 7465 6428 293a  .is_connected():
-00001140: 0d0a 2020 2020 2020 2020 2020 2020 7265  ..            re
-00001150: 7475 726e 204e 6f6e 652c 204e 6f6e 652c  turn None, None,
-00001160: 204e 6f6e 650d 0a0d 0a20 2020 2020 2020   None....       
-00001170: 2072 6570 6c79 203d 2073 656c 662e 7175   reply = self.qu
-00001180: 6572 795f 7465 7874 2827 4944 3f27 292e  ery_text('ID?').
-00001190: 7374 7269 7028 290d 0a0d 0a20 2020 2020  strip()....     
-000011a0: 2020 2069 6620 6c65 6e28 7265 706c 7929     if len(reply)
-000011b0: 203c 2032 303a 0d0a 2020 2020 2020 2020   < 20:..        
-000011c0: 2020 2020 7265 7475 726e 204e 6f6e 652c      return None,
-000011d0: 204e 6f6e 652c 204e 6f6e 650d 0a0d 0a20   None, None.... 
-000011e0: 2020 2020 2020 206d 6f64 656c 5f6e 616d         model_nam
-000011f0: 6520 3d20 7265 706c 795b 303a 395d 0d0a  e = reply[0:9]..
-00001200: 2020 2020 2020 2020 6669 726d 7761 7265          firmware
-00001210: 5f76 6572 7369 6f6e 203d 2072 6570 6c79  _version = reply
-00001220: 5b31 323a 3136 5d0d 0a20 2020 2020 2020  [12:16]..       
-00001230: 2073 6572 6961 6c5f 6e75 6d62 6572 203d   serial_number =
-00001240: 2072 6570 6c79 5b31 383a 5d0d 0a0d 0a20   reply[18:].... 
-00001250: 2020 2020 2020 2069 6620 7365 6c66 2e5f         if self._
-00001260: 4964 5374 7269 6e67 206e 6f74 2069 6e20  IdString not in 
-00001270: 7265 706c 793a 0d0a 2020 2020 2020 2020  reply:..        
-00001280: 2020 2020 7261 6973 6520 496e 7374 4964      raise InstId
-00001290: 4572 726f 7228 2249 6e76 616c 6964 2069  Error("Invalid i
-000012a0: 6e73 7472 756d 656e 743a 207b 7d20 6e6f  nstrument: {} no
-000012b0: 7420 696e 207b 7d22 0d0a 2020 2020 2020  t in {}"..      
-000012c0: 2020 2020 2020 2020 2020 2020 2e66 6f72              .for
-000012d0: 6d61 7428 7365 6c66 2e5f 4964 5374 7269  mat(self._IdStri
-000012e0: 6e67 2c20 6d6f 6465 6c5f 6e61 6d65 2929  ng, model_name))
-000012f0: 0d0a 2020 2020 2020 2020 7365 6c66 2e5f  ..        self._
-00001300: 6964 5f73 7472 696e 6720 3d20 7265 706c  id_string = repl
-00001310: 790d 0a0d 0a20 2020 2020 2020 2074 7279  y....        try
-00001320: 3a0d 0a20 2020 2020 2020 2020 2020 2073  :..            s
-00001330: 656c 662e 5f6d 5f6d 6178 203d 2069 6e74  elf._m_max = int
-00001340: 2872 6570 6c79 5b36 3a39 5d29 2020 2320  (reply[6:9])  # 
-00001350: 756e 696e 6974 6961 6c69 7a65 6420 756e  uninitialized un
-00001360: 6974 2068 6173 2027 3f3f 3f27 0d0a 2020  it has '???'..  
-00001370: 2020 2020 2020 6578 6365 7074 2056 616c        except Val
-00001380: 7565 4572 726f 723a 0d0a 2020 2020 2020  ueError:..      
-00001390: 2020 2020 2020 7365 6c66 2e5f 6d5f 6d61        self._m_ma
-000013a0: 7820 3d20 3130 300d 0a0d 0a20 2020 2020  x = 100....     
-000013b0: 2020 2073 656c 662e 5f6d 6f64 656c 5f6e     self._model_n
-000013c0: 616d 6520 3d20 6d6f 6465 6c5f 6e61 6d65  ame = model_name
-000013d0: 0d0a 2020 2020 2020 2020 7365 6c66 2e5f  ..        self._
-000013e0: 7365 7269 616c 5f6e 756d 6265 7220 3d20  serial_number = 
-000013f0: 7365 7269 616c 5f6e 756d 6265 720d 0a20  serial_number.. 
-00001400: 2020 2020 2020 2073 656c 662e 5f66 6972         self._fir
-00001410: 6d77 6172 655f 7665 7273 696f 6e20 3d20  mware_version = 
-00001420: 6669 726d 7761 7265 5f76 6572 7369 6f6e  firmware_version
-00001430: 0d0a 2020 2020 2020 2020 7265 7475 726e  ..        return
-00001440: 2073 656c 662e 5f6d 6f64 656c 5f6e 616d   self._model_nam
-00001450: 652c 2073 656c 662e 5f73 6572 6961 6c5f  e, self._serial_
-00001460: 6e75 6d62 6572 2c20 7365 6c66 2e5f 6669  number, self._fi
-00001470: 726d 7761 7265 5f76 6572 7369 6f6e 0d0a  rmware_version..
-00001480: 0d0a 2020 2020 6465 6620 6765 745f 7374  ..    def get_st
-00001490: 6174 7573 2873 656c 6629 3a0d 0a20 2020  atus(self):..   
-000014a0: 2020 2020 2073 7461 7475 735f 7374 7269       status_stri
-000014b0: 6e67 203d 2027 456d 6973 7369 6f6e 2063  ng = 'Emission c
-000014c0: 7572 7265 6e74 3a20 7b3a 2e32 667d 206d  urrent: {:.2f} m
-000014d0: 415c 6e27 2e66 6f72 6d61 7428 7365 6c66  A\n'.format(self
-000014e0: 2e69 6f6e 697a 6572 2e65 6d69 7373 696f  .ionizer.emissio
-000014f0: 6e5f 6375 7272 656e 7429 0d0a 2020 2020  n_current)..    
-00001500: 2020 2020 7374 6174 7573 5f73 7472 696e      status_strin
-00001510: 6720 2b3d 2027 4345 4d20 4856 3a20 7b3a  g += 'CEM HV: {:
-00001520: 2e30 667d 2056 5c6e 272e 666f 726d 6174  .0f} V\n'.format
-00001530: 2873 656c 662e 6365 6d2e 766f 6c74 6167  (self.cem.voltag
-00001540: 6529 0d0a 2020 2020 2020 2020 7374 6174  e)..        stat
-00001550: 7573 5f73 7472 696e 6720 2b3d 2073 656c  us_string += sel
-00001560: 662e 7374 6174 7573 2e67 6574 5f65 7272  f.status.get_err
-00001570: 6f72 5f74 6578 7428 290d 0a20 2020 2020  or_text()..     
-00001580: 2020 2072 6574 7572 6e20 7374 6174 7573     return status
-00001590: 5f73 7472 696e 670d 0a0d 0a20 2020 2064  _string....    d
-000015a0: 6566 2068 616e 646c 655f 636f 6d6d 616e  ef handle_comman
-000015b0: 6428 7365 6c66 2c20 636d 645f 7374 7269  d(self, cmd_stri
-000015c0: 6e67 3a20 7374 7229 3a0d 0a20 2020 2020  ng: str):..     
-000015d0: 2020 2063 6d64 203d 2063 6d64 5f73 7472     cmd = cmd_str
-000015e0: 696e 672e 7570 7065 7228 290d 0a20 2020  ing.upper()..   
-000015f0: 2020 2020 2072 6570 6c79 203d 2027 270d       reply = ''.
-00001600: 0a20 2020 2020 2020 2069 6620 273f 2720  .        if '?' 
-00001610: 696e 2063 6d64 206f 7220 636d 642e 7374  in cmd or cmd.st
-00001620: 6172 7473 7769 7468 2822 464c 2229 206f  artswith("FL") o
-00001630: 7220 636d 642e 7374 6172 7473 7769 7468  r cmd.startswith
-00001640: 2822 4856 2229 206f 7220 5c0d 0a20 2020  ("HV") or \..   
-00001650: 2020 2020 2020 2020 2020 2020 2063 6d64               cmd
-00001660: 2e73 7461 7274 7377 6974 6828 2256 4622  .startswith("VF"
-00001670: 2920 6f72 2063 6d64 2e73 7461 7274 7377  ) or cmd.startsw
-00001680: 6974 6828 2245 4522 2920 6f72 2063 6d64  ith("EE") or cmd
-00001690: 2e73 7461 7274 7377 6974 6828 2249 4522  .startswith("IE"
-000016a0: 293a 0d0a 2020 2020 2020 2020 2020 2020  ):..            
-000016b0: 7265 706c 7920 3d20 7365 6c66 2e71 7565  reply = self.que
-000016c0: 7279 5f74 6578 7428 636d 6429 2e73 7472  ry_text(cmd).str
-000016d0: 6970 2829 0d0a 2020 2020 2020 2020 656c  ip()..        el
-000016e0: 6966 2063 6d64 2e73 7461 7274 7377 6974  if cmd.startswit
-000016f0: 6828 224d 5222 293a 0d0a 2020 2020 2020  h("MR"):..      
-00001700: 2020 2020 2020 2320 7365 6c66 2e73 656e        # self.sen
-00001710: 6428 636d 6429 0d0a 2020 2020 2020 2020  d(cmd)..        
-00001720: 2020 2020 7472 793a 0d0a 2020 2020 2020      try:..      
-00001730: 2020 2020 2020 2020 2020 6d61 7373 203d            mass =
-00001740: 2069 6e74 2863 6d64 5b32 3a5d 2e73 7472   int(cmd[2:].str
-00001750: 6970 2829 290d 0a20 2020 2020 2020 2020  ip())..         
-00001760: 2020 2020 2020 2069 6e74 656e 7369 7479         intensity
-00001770: 203d 2073 656c 662e 7363 616e 2e67 6574   = self.scan.get
-00001780: 5f73 696e 676c 655f 6d61 7373 5f73 6361  _single_mass_sca
-00001790: 6e28 6d61 7373 2920 2023 2072 6561 645f  n(mass)  # read_
-000017a0: 6c6f 6e67 2829 0d0a 2020 2020 2020 2020  long()..        
-000017b0: 2020 2020 2020 2020 7265 706c 7920 3d20          reply = 
-000017c0: 7374 7228 696e 7465 6e73 6974 7929 0d0a  str(intensity)..
-000017d0: 2020 2020 2020 2020 2020 2020 6578 6365              exce
-000017e0: 7074 3a0d 0a20 2020 2020 2020 2020 2020  pt:..           
-000017f0: 2020 2020 2070 6173 730d 0a20 2020 2020       pass..     
-00001800: 2020 2065 6c69 6620 636d 642e 7374 6172     elif cmd.star
-00001810: 7473 7769 7468 2822 5343 2229 2061 6e64  tswith("SC") and
-00001820: 206c 656e 2863 6d64 2920 3c20 3130 3a0d   len(cmd) < 10:.
-00001830: 0a20 2020 2020 2020 2020 2020 2073 656c  .            sel
-00001840: 662e 7363 616e 2e67 6574 5f61 6e61 6c6f  f.scan.get_analo
-00001850: 675f 7363 616e 2829 0d0a 2020 2020 2020  g_scan()..      
-00001860: 2020 2020 2020 7265 706c 7920 3d20 2253        reply = "S
-00001870: 6361 6e20 436f 6d70 6c65 7465 6422 0d0a  can Completed"..
-00001880: 2020 2020 2020 2020 656c 6966 2063 6d64          elif cmd
-00001890: 2e73 7461 7274 7377 6974 6828 2248 5322  .startswith("HS"
-000018a0: 293a 0d0a 2020 2020 2020 2020 2020 2020  ):..            
-000018b0: 7365 6c66 2e73 6361 6e2e 6765 745f 6869  self.scan.get_hi
-000018c0: 7374 6f67 7261 6d5f 7363 616e 2829 0d0a  stogram_scan()..
-000018d0: 2020 2020 2020 2020 2020 2020 7265 706c              repl
-000018e0: 7920 3d20 2253 6361 6e20 436f 6d70 6c65  y = "Scan Comple
-000018f0: 7465 6422 0d0a 2020 2020 2020 2020 656c  ted"..        el
-00001900: 7365 3a0d 0a20 2020 2020 2020 2020 2020  se:..           
-00001910: 2073 656c 662e 7365 6e64 2863 6d64 290d   self.send(cmd).
-00001920: 0a20 2020 2020 2020 2072 6574 7572 6e20  .        return 
-00001930: 7265 706c 790d 0a0d 0a20 2020 2064 6566  reply....    def
-00001940: 2072 6573 6574 2873 656c 6629 3a0d 0a20   reset(self):.. 
-00001950: 2020 2020 2020 2073 656c 662e 7175 6572         self.quer
-00001960: 795f 7465 7874 2822 494e 3222 290d 0a0d  y_text("IN2")...
-00001970: 0a20 2020 2023 2046 6f72 2052 4741 3130  .    # For RGA10
-00001980: 302c 2020 5253 3233 3220 4453 5220 6c69  0,  RS232 DSR li
-00001990: 6e65 2073 686f 756c 6420 6265 2068 6967  ne should be hig
-000019a0: 6820 6966 2052 5332 3332 2063 6162 6c65  h if RS232 cable
-000019b0: 2069 7320 636f 6e6e 6563 7465 640d 0a20   is connected.. 
-000019c0: 2020 2064 6566 2063 6865 636b 5f68 6561     def check_hea
-000019d0: 645f 6f6e 6c69 6e65 2873 656c 6629 3a0d  d_online(self):.
-000019e0: 0a20 2020 2020 2020 2022 2222 0d0a 2020  .        """..  
-000019f0: 2020 2020 2020 4368 6563 6b20 6966 2053        Check if S
-00001a00: 5253 2052 4741 2069 7320 636f 6e6e 6563  RS RGA is connec
-00001a10: 7465 6420 746f 2061 2063 6f6d 6d75 6e69  ted to a communi
-00001a20: 6361 7469 6f6e 2069 6e73 7465 7266 6163  cation insterfac
-00001a30: 650d 0a0d 0a20 2020 2020 2020 2046 6f72  e....        For
-00001a40: 2073 6572 6961 6c20 636f 6d6d 756e 6963   serial communic
-00001a50: 6174 696f 6e2c 2069 7420 6368 6563 6b20  ation, it check 
-00001a60: 666f 7220 4453 5220 6c69 6e65 2066 726f  for DSR line fro
-00001a70: 6d20 5352 5320 5247 4120 6973 2073 6574  m SRS RGA is set
-00001a80: 2068 6967 682e 0d0a 2020 2020 2020 2020   high...        
-00001a90: 466f 7220 4574 6865 726e 6574 2063 6f6d  For Ethernet com
-00001aa0: 6d75 6e69 6361 7469 6f6e 2c20 6974 2063  munication, it c
-00001ab0: 6865 636b 2069 6620 7468 6520 5443 5020  heck if the TCP 
-00001ac0: 736f 636b 6574 2069 7320 6f70 656e 2e0d  socket is open..
-00001ad0: 0a20 2020 2020 2020 2022 2222 0d0a 2020  .        """..  
-00001ae0: 2020 2020 2020 6966 2073 656c 662e 636f        if self.co
-00001af0: 6d6d 2e74 7970 6520 3d3d 2049 6e74 6572  mm.type == Inter
-00001b00: 6661 6365 2e53 4552 4941 4c3a 0d0a 2020  face.SERIAL:..  
-00001b10: 2020 2020 2020 2020 2020 7265 7475 726e            return
-00001b20: 2073 656c 662e 636f 6d6d 2e5f 7365 7269   self.comm._seri
-00001b30: 616c 2e64 7372 0d0a 2020 2020 2020 2020  al.dsr..        
-00001b40: 656c 7365 3a0d 0a20 2020 2020 2020 2020  else:..         
-00001b50: 2020 2072 6574 7572 6e20 7365 6c66 2e69     return self.i
-00001b60: 735f 636f 6e6e 6563 7465 6428 290d 0a0d  s_connected()...
-00001b70: 0a20 2020 2064 6566 2067 6574 5f6d 6178  .    def get_max
-00001b80: 5f6d 6173 7328 7365 6c66 293a 0d0a 2020  _mass(self):..  
-00001b90: 2020 2020 2020 2222 220d 0a20 2020 2020        """..     
-00001ba0: 2020 2047 6574 206d 6178 696d 756d 206d     Get maximum m
-00001bb0: 6173 7320 7468 6174 2063 616e 2062 6520  ass that can be 
-00001bc0: 7573 6564 2066 6f72 2061 2073 6361 6e0d  used for a scan.
-00001bd0: 0a0d 0a20 2020 2020 2020 2053 5253 2052  ...        SRS R
-00001be0: 4741 3130 3020 6d6f 6465 6c20 6861 7320  GA100 model has 
-00001bf0: 7468 6520 6d61 7869 6d75 6d20 6d61 7373  the maximum mass
-00001c00: 206f 6620 3130 3020 414d 553b 0d0a 2020   of 100 AMU;..  
-00001c10: 2020 2020 2020 5352 5320 5247 4132 3030        SRS RGA200
-00001c20: 2c20 3230 3020 414d 553b 2061 6e64 2053  , 200 AMU; and S
-00001c30: 5253 2052 4741 3330 302c 2033 3030 2041  RS RGA300, 300 A
-00001c40: 4d55 2e0d 0a0d 0a20 2020 2020 2020 2052  MU.....        R
-00001c50: 6574 7572 6e73 0d0a 2020 2020 2020 2020  eturns..        
-00001c60: 2d2d 2d2d 2d2d 2d2d 0d0a 2020 2020 2020  --------..      
-00001c70: 2020 2020 2020 696e 740d 0a20 2020 2020        int..     
-00001c80: 2020 2020 2020 2020 2020 206d 6178 696d             maxim
-00001c90: 756d 206d 6173 730d 0a20 2020 2020 2020  um mass..       
-00001ca0: 2022 2222 0d0a 2020 2020 2020 2020 7265   """..        re
-00001cb0: 7475 726e 2073 656c 662e 5f6d 5f6d 6178  turn self._m_max
-00001cc0: 0d0a 0d0a 2020 2020 6465 6620 6361 6c69  ....    def cali
-00001cd0: 6272 6174 655f 616c 6c28 7365 6c66 293a  brate_all(self):
-00001ce0: 0d0a 2020 2020 2020 2020 2222 220d 0a20  ..        """.. 
-00001cf0: 2020 2020 2020 2043 616c 6962 7261 7465         Calibrate
-00001d00: 2061 6c6c 0d0a 0d0a 2020 2020 2020 2020   all....        
-00001d10: 7265 7475 726e 730d 0a20 2020 2020 2020  returns..       
-00001d20: 202d 2d2d 2d2d 2d2d 2d0d 0a20 2020 2020   --------..     
-00001d30: 2020 2020 2020 2069 6e74 0d0a 2020 2020         int..    
-00001d40: 2020 2020 2020 2020 2020 2020 4572 726f              Erro
-00001d50: 7220 7374 6174 7573 2062 7974 6520 6166  r status byte af
-00001d60: 7465 7220 6361 6c69 6272 6174 696f 6e0d  ter calibration.
-00001d70: 0a20 2020 2020 2020 2022 2222 0d0a 2020  .        """..  
-00001d80: 2020 2020 2020 7265 706c 7920 3d20 7365        reply = se
-00001d90: 6c66 2e63 6f6d 6d2e 7175 6572 795f 7465  lf.comm.query_te
-00001da0: 7874 5f77 6974 685f 6c6f 6e67 5f74 696d  xt_with_long_tim
-00001db0: 656f 7574 2822 4341 222c 2031 3230 290d  eout("CA", 120).
-00001dc0: 0a20 2020 2020 2020 2065 7272 6f72 5f73  .        error_s
-00001dd0: 7461 7475 7320 3d20 696e 7428 7265 706c  tatus = int(repl
-00001de0: 7929 0d0a 2020 2020 2020 2020 7265 7475  y)..        retu
-00001df0: 726e 2065 7272 6f72 5f73 7461 7475 730d  rn error_status.
-00001e00: 0a0d 0a20 2020 2064 6566 2063 616c 6962  ...    def calib
-00001e10: 7261 7465 5f65 6c65 6374 726f 6d65 7465  rate_electromete
-00001e20: 7228 7365 6c66 293a 0d0a 2020 2020 2020  r(self):..      
-00001e30: 2020 2222 220d 0a20 2020 2020 2020 2043    """..        C
-00001e40: 616c 6962 7261 7465 2065 6c65 6374 726f  alibrate electro
-00001e50: 6d65 7465 7227 7320 492d 5620 7265 7370  meter's I-V resp
-00001e60: 6f6e 7365 0d0a 0d0a 2020 2020 2020 2020  onse....        
-00001e70: 7265 7475 726e 730d 0a20 2020 2020 2020  returns..       
-00001e80: 202d 2d2d 2d2d 2d2d 2d0d 0a20 2020 2020   --------..     
-00001e90: 2020 2020 2020 2069 6e74 0d0a 2020 2020         int..    
-00001ea0: 2020 2020 2020 2020 2020 2020 4572 726f              Erro
-00001eb0: 7220 7374 6174 7573 2062 7974 6520 6166  r status byte af
-00001ec0: 7465 7220 6361 6c69 6272 6174 696f 6e0d  ter calibration.
-00001ed0: 0a20 2020 2020 2020 2022 2222 0d0a 2020  .        """..  
-00001ee0: 2020 2020 2020 7265 706c 7920 3d20 7365        reply = se
-00001ef0: 6c66 2e63 6f6d 6d2e 7175 6572 795f 7465  lf.comm.query_te
-00001f00: 7874 5f77 6974 685f 6c6f 6e67 5f74 696d  xt_with_long_tim
-00001f10: 656f 7574 2822 434c 222c 2031 3230 290d  eout("CL", 120).
-00001f20: 0a20 2020 2020 2020 2065 7272 6f72 5f73  .        error_s
-00001f30: 7461 7475 7320 3d20 696e 7428 7265 706c  tatus = int(repl
-00001f40: 7929 0d0a 2020 2020 2020 2020 7265 7475  y)..        retu
-00001f50: 726e 2065 7272 6f72 5f73 7461 7475 730d  rn error_status.
-00001f60: 0a                                       .
+00000f00: 2020 2020 2020 2075 7365 7220 6e61 6d65         user name
+00000f10: 2066 6f72 206c 6f67 696e 2e0d 0a20 2020   for login...   
+00000f20: 2020 2020 2020 2020 2070 6173 7377 6f72           passwor
+00000f30: 6420 3a20 7374 720d 0a20 2020 2020 2020  d : str..       
+00000f40: 2020 2020 2020 2020 2070 6173 7377 6f72           passwor
+00000f50: 6420 666f 7220 6c6f 6769 6e2e 0d0a 2020  d for login...  
+00000f60: 2020 2020 2020 2020 2020 706f 7274 203a            port :
+00000f70: 2069 6e74 2c20 6f70 7469 6f6e 616c 0d0a   int, optional..
+00000f80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000f90: 5443 5020 706f 7274 206e 756d 6265 722e  TCP port number.
+00000fa0: 2054 6865 2064 6566 6175 6c74 2069 7320   The default is 
+00000fb0: 3831 382c 2077 6869 6368 2053 5253 2052  818, which SRS R
+00000fc0: 4741 2075 7365 730d 0a0d 0a20 2020 2020  GA uses....     
+00000fd0: 2020 2022 2222 0d0a 2020 2020 2020 2020     """..        
+00000fe0: 7375 7065 7228 292e 636f 6e6e 6563 7428  super().connect(
+00000ff0: 696e 7465 7266 6163 655f 7479 7065 2c20  interface_type, 
+00001000: 2a61 7267 7329 0d0a 2020 2020 2020 2020  *args)..        
+00001010: 6966 2074 7970 6528 7365 6c66 2e63 6f6d  if type(self.com
+00001020: 6d29 203d 3d20 5365 7269 616c 496e 7465  m) == SerialInte
+00001030: 7266 6163 653a 0d0a 2020 2020 2020 2020  rface:..        
+00001040: 2020 2020 2320 4d61 6b65 2073 7572 6520      # Make sure 
+00001050: 7468 6520 6861 7264 7761 7265 2066 6c6f  the hardware flo
+00001060: 7720 636f 6e74 726f 6c20 6973 2073 6574  w control is set
+00001070: 0d0a 2020 2020 2020 2020 2020 2020 7365  ..            se
+00001080: 6c66 2e63 6f6d 6d2e 5f73 6572 6961 6c2e  lf.comm._serial.
+00001090: 7274 7363 7473 203d 2054 7275 650d 0a0d  rtscts = True...
+000010a0: 0a20 2020 2064 6566 2063 6865 636b 5f69  .    def check_i
+000010b0: 6428 7365 6c66 293a 0d0a 0d0a 2020 2020  d(self):....    
+000010c0: 2020 2020 7365 6c66 2e5f 6d5f 6d61 7820      self._m_max 
+000010d0: 3d20 3130 300d 0a20 2020 2020 2020 2069  = 100..        i
+000010e0: 6620 6e6f 7420 7365 6c66 2e69 735f 636f  f not self.is_co
+000010f0: 6e6e 6563 7465 6428 293a 0d0a 2020 2020  nnected():..    
+00001100: 2020 2020 2020 2020 7265 7475 726e 204e          return N
+00001110: 6f6e 652c 204e 6f6e 652c 204e 6f6e 650d  one, None, None.
+00001120: 0a0d 0a20 2020 2020 2020 2072 6570 6c79  ...        reply
+00001130: 203d 2073 656c 662e 7175 6572 795f 7465   = self.query_te
+00001140: 7874 2827 4944 3f27 292e 7374 7269 7028  xt('ID?').strip(
+00001150: 290d 0a0d 0a20 2020 2020 2020 2069 6620  )....        if 
+00001160: 6c65 6e28 7265 706c 7929 203c 2032 303a  len(reply) < 20:
+00001170: 0d0a 2020 2020 2020 2020 2020 2020 7265  ..            re
+00001180: 7475 726e 204e 6f6e 652c 204e 6f6e 652c  turn None, None,
+00001190: 204e 6f6e 650d 0a0d 0a20 2020 2020 2020   None....       
+000011a0: 206d 6f64 656c 5f6e 616d 6520 3d20 7265   model_name = re
+000011b0: 706c 795b 303a 395d 0d0a 2020 2020 2020  ply[0:9]..      
+000011c0: 2020 6669 726d 7761 7265 5f76 6572 7369    firmware_versi
+000011d0: 6f6e 203d 2072 6570 6c79 5b31 323a 3136  on = reply[12:16
+000011e0: 5d0d 0a20 2020 2020 2020 2073 6572 6961  ]..        seria
+000011f0: 6c5f 6e75 6d62 6572 203d 2072 6570 6c79  l_number = reply
+00001200: 5b31 383a 5d0d 0a0d 0a20 2020 2020 2020  [18:]....       
+00001210: 2069 6620 7365 6c66 2e5f 4964 5374 7269   if self._IdStri
+00001220: 6e67 206e 6f74 2069 6e20 7265 706c 793a  ng not in reply:
+00001230: 0d0a 2020 2020 2020 2020 2020 2020 7261  ..            ra
+00001240: 6973 6520 496e 7374 4964 4572 726f 7228  ise InstIdError(
+00001250: 2249 6e76 616c 6964 2069 6e73 7472 756d  "Invalid instrum
+00001260: 656e 743a 207b 7d20 6e6f 7420 696e 207b  ent: {} not in {
+00001270: 7d22 0d0a 2020 2020 2020 2020 2020 2020  }"..            
+00001280: 2020 2020 2020 2e66 6f72 6d61 7428 7365        .format(se
+00001290: 6c66 2e5f 4964 5374 7269 6e67 2c20 6d6f  lf._IdString, mo
+000012a0: 6465 6c5f 6e61 6d65 2929 0d0a 2020 2020  del_name))..    
+000012b0: 2020 2020 7365 6c66 2e5f 6964 5f73 7472      self._id_str
+000012c0: 696e 6720 3d20 7265 706c 790d 0a0d 0a20  ing = reply.... 
+000012d0: 2020 2020 2020 2074 7279 3a0d 0a20 2020         try:..   
+000012e0: 2020 2020 2020 2020 2073 656c 662e 5f6d           self._m
+000012f0: 5f6d 6178 203d 2069 6e74 2872 6570 6c79  _max = int(reply
+00001300: 5b36 3a39 5d29 2020 2320 756e 696e 6974  [6:9])  # uninit
+00001310: 6961 6c69 7a65 6420 756e 6974 2068 6173  ialized unit has
+00001320: 2027 3f3f 3f27 0d0a 2020 2020 2020 2020   '???'..        
+00001330: 6578 6365 7074 2056 616c 7565 4572 726f  except ValueErro
+00001340: 723a 0d0a 2020 2020 2020 2020 2020 2020  r:..            
+00001350: 7365 6c66 2e5f 6d5f 6d61 7820 3d20 3130  self._m_max = 10
+00001360: 300d 0a0d 0a20 2020 2020 2020 2073 656c  0....        sel
+00001370: 662e 5f6d 6f64 656c 5f6e 616d 6520 3d20  f._model_name = 
+00001380: 6d6f 6465 6c5f 6e61 6d65 0d0a 2020 2020  model_name..    
+00001390: 2020 2020 7365 6c66 2e5f 7365 7269 616c      self._serial
+000013a0: 5f6e 756d 6265 7220 3d20 7365 7269 616c  _number = serial
+000013b0: 5f6e 756d 6265 720d 0a20 2020 2020 2020  _number..       
+000013c0: 2073 656c 662e 5f66 6972 6d77 6172 655f   self._firmware_
+000013d0: 7665 7273 696f 6e20 3d20 6669 726d 7761  version = firmwa
+000013e0: 7265 5f76 6572 7369 6f6e 0d0a 2020 2020  re_version..    
+000013f0: 2020 2020 7265 7475 726e 2073 656c 662e      return self.
+00001400: 5f6d 6f64 656c 5f6e 616d 652c 2073 656c  _model_name, sel
+00001410: 662e 5f73 6572 6961 6c5f 6e75 6d62 6572  f._serial_number
+00001420: 2c20 7365 6c66 2e5f 6669 726d 7761 7265  , self._firmware
+00001430: 5f76 6572 7369 6f6e 0d0a 0d0a 2020 2020  _version....    
+00001440: 6465 6620 6765 745f 7374 6174 7573 2873  def get_status(s
+00001450: 656c 6629 3a0d 0a20 2020 2020 2020 2073  elf):..        s
+00001460: 7461 7475 735f 7374 7269 6e67 203d 2027  tatus_string = '
+00001470: 456d 6973 7369 6f6e 2063 7572 7265 6e74  Emission current
+00001480: 3a20 7b3a 2e32 667d 206d 415c 6e27 2e66  : {:.2f} mA\n'.f
+00001490: 6f72 6d61 7428 7365 6c66 2e69 6f6e 697a  ormat(self.ioniz
+000014a0: 6572 2e65 6d69 7373 696f 6e5f 6375 7272  er.emission_curr
+000014b0: 656e 7429 0d0a 2020 2020 2020 2020 7374  ent)..        st
+000014c0: 6174 7573 5f73 7472 696e 6720 2b3d 2027  atus_string += '
+000014d0: 4345 4d20 4856 3a20 7b3a 2e30 667d 2056  CEM HV: {:.0f} V
+000014e0: 5c6e 272e 666f 726d 6174 2873 656c 662e  \n'.format(self.
+000014f0: 6365 6d2e 766f 6c74 6167 6529 0d0a 2020  cem.voltage)..  
+00001500: 2020 2020 2020 7374 6174 7573 5f73 7472        status_str
+00001510: 696e 6720 2b3d 2073 656c 662e 7374 6174  ing += self.stat
+00001520: 7573 2e67 6574 5f65 7272 6f72 5f74 6578  us.get_error_tex
+00001530: 7428 290d 0a20 2020 2020 2020 2072 6574  t()..        ret
+00001540: 7572 6e20 7374 6174 7573 5f73 7472 696e  urn status_strin
+00001550: 670d 0a0d 0a20 2020 2064 6566 2068 616e  g....    def han
+00001560: 646c 655f 636f 6d6d 616e 6428 7365 6c66  dle_command(self
+00001570: 2c20 636d 645f 7374 7269 6e67 3a20 7374  , cmd_string: st
+00001580: 7229 3a0d 0a20 2020 2020 2020 2063 6d64  r):..        cmd
+00001590: 203d 2063 6d64 5f73 7472 696e 672e 7570   = cmd_string.up
+000015a0: 7065 7228 290d 0a20 2020 2020 2020 2072  per()..        r
+000015b0: 6570 6c79 203d 2027 270d 0a20 2020 2020  eply = ''..     
+000015c0: 2020 2069 6620 273f 2720 696e 2063 6d64     if '?' in cmd
+000015d0: 206f 7220 636d 642e 7374 6172 7473 7769   or cmd.startswi
+000015e0: 7468 2822 464c 2229 206f 7220 636d 642e  th("FL") or cmd.
+000015f0: 7374 6172 7473 7769 7468 2822 4856 2229  startswith("HV")
+00001600: 206f 7220 5c0d 0a20 2020 2020 2020 2020   or \..         
+00001610: 2020 2020 2020 2063 6d64 2e73 7461 7274         cmd.start
+00001620: 7377 6974 6828 2256 4622 2920 6f72 2063  swith("VF") or c
+00001630: 6d64 2e73 7461 7274 7377 6974 6828 2245  md.startswith("E
+00001640: 4522 295c 0d0a 2020 2020 2020 2020 2020  E")\..          
+00001650: 2020 2020 2020 6f72 2063 6d64 2e73 7461        or cmd.sta
+00001660: 7274 7377 6974 6828 2249 4522 2920 6f72  rtswith("IE") or
+00001670: 2063 6d64 2e73 7461 7274 7377 6974 6828   cmd.startswith(
+00001680: 2249 4e22 293a 0d0a 2020 2020 2020 2020  "IN"):..        
+00001690: 2020 2020 7265 706c 7920 3d20 7365 6c66      reply = self
+000016a0: 2e71 7565 7279 5f74 6578 7428 636d 6429  .query_text(cmd)
+000016b0: 2e73 7472 6970 2829 0d0a 2020 2020 2020  .strip()..      
+000016c0: 2020 656c 6966 2063 6d64 2e73 7461 7274    elif cmd.start
+000016d0: 7377 6974 6828 224d 5222 293a 0d0a 2020  swith("MR"):..  
+000016e0: 2020 2020 2020 2020 2020 2320 7365 6c66            # self
+000016f0: 2e73 656e 6428 636d 6429 0d0a 2020 2020  .send(cmd)..    
+00001700: 2020 2020 2020 2020 7472 793a 0d0a 2020          try:..  
+00001710: 2020 2020 2020 2020 2020 2020 2020 6d61                ma
+00001720: 7373 203d 2069 6e74 2863 6d64 5b32 3a5d  ss = int(cmd[2:]
+00001730: 2e73 7472 6970 2829 290d 0a20 2020 2020  .strip())..     
+00001740: 2020 2020 2020 2020 2020 2069 6e74 656e             inten
+00001750: 7369 7479 203d 2073 656c 662e 7363 616e  sity = self.scan
+00001760: 2e67 6574 5f73 696e 676c 655f 6d61 7373  .get_single_mass
+00001770: 5f73 6361 6e28 6d61 7373 2920 2023 2072  _scan(mass)  # r
+00001780: 6561 645f 6c6f 6e67 2829 0d0a 2020 2020  ead_long()..    
+00001790: 2020 2020 2020 2020 2020 2020 7265 706c              repl
+000017a0: 7920 3d20 7374 7228 696e 7465 6e73 6974  y = str(intensit
+000017b0: 7929 0d0a 2020 2020 2020 2020 2020 2020  y)..            
+000017c0: 6578 6365 7074 3a0d 0a20 2020 2020 2020  except:..       
+000017d0: 2020 2020 2020 2020 2070 6173 730d 0a20           pass.. 
+000017e0: 2020 2020 2020 2065 6c69 6620 636d 642e         elif cmd.
+000017f0: 7374 6172 7473 7769 7468 2822 5343 2229  startswith("SC")
+00001800: 2061 6e64 206c 656e 2863 6d64 2920 3c20   and len(cmd) < 
+00001810: 3130 3a0d 0a20 2020 2020 2020 2020 2020  10:..           
+00001820: 2073 656c 662e 7363 616e 2e67 6574 5f61   self.scan.get_a
+00001830: 6e61 6c6f 675f 7363 616e 2829 0d0a 2020  nalog_scan()..  
+00001840: 2020 2020 2020 2020 2020 7265 706c 7920            reply 
+00001850: 3d20 2253 6361 6e20 436f 6d70 6c65 7465  = "Scan Complete
+00001860: 6422 0d0a 2020 2020 2020 2020 656c 6966  d"..        elif
+00001870: 2063 6d64 2e73 7461 7274 7377 6974 6828   cmd.startswith(
+00001880: 2248 5322 293a 0d0a 2020 2020 2020 2020  "HS"):..        
+00001890: 2020 2020 7365 6c66 2e73 6361 6e2e 6765      self.scan.ge
+000018a0: 745f 6869 7374 6f67 7261 6d5f 7363 616e  t_histogram_scan
+000018b0: 2829 0d0a 2020 2020 2020 2020 2020 2020  ()..            
+000018c0: 7265 706c 7920 3d20 2253 6361 6e20 436f  reply = "Scan Co
+000018d0: 6d70 6c65 7465 6422 0d0a 2020 2020 2020  mpleted"..      
+000018e0: 2020 656c 7365 3a0d 0a20 2020 2020 2020    else:..       
+000018f0: 2020 2020 2073 656c 662e 7365 6e64 2863       self.send(c
+00001900: 6d64 290d 0a20 2020 2020 2020 2072 6574  md)..        ret
+00001910: 7572 6e20 7265 706c 790d 0a0d 0a20 2020  urn reply....   
+00001920: 2064 6566 2072 6573 6574 2873 656c 6629   def reset(self)
+00001930: 3a0d 0a20 2020 2020 2020 2073 656c 662e  :..        self.
+00001940: 7175 6572 795f 7465 7874 2822 494e 3222  query_text("IN2"
+00001950: 290d 0a0d 0a20 2020 2023 2046 6f72 2052  )....    # For R
+00001960: 4741 3130 302c 2020 5253 3233 3220 4453  GA100,  RS232 DS
+00001970: 5220 6c69 6e65 2073 686f 756c 6420 6265  R line should be
+00001980: 2068 6967 6820 6966 2052 5332 3332 2063   high if RS232 c
+00001990: 6162 6c65 2069 7320 636f 6e6e 6563 7465  able is connecte
+000019a0: 640d 0a20 2020 2064 6566 2063 6865 636b  d..    def check
+000019b0: 5f68 6561 645f 6f6e 6c69 6e65 2873 656c  _head_online(sel
+000019c0: 6629 3a0d 0a20 2020 2020 2020 2022 2222  f):..        """
+000019d0: 0d0a 2020 2020 2020 2020 4368 6563 6b20  ..        Check 
+000019e0: 6966 2053 5253 2052 4741 2069 7320 636f  if SRS RGA is co
+000019f0: 6e6e 6563 7465 6420 746f 2061 2063 6f6d  nnected to a com
+00001a00: 6d75 6e69 6361 7469 6f6e 2069 6e73 7465  munication inste
+00001a10: 7266 6163 650d 0a0d 0a20 2020 2020 2020  rface....       
+00001a20: 2046 6f72 2073 6572 6961 6c20 636f 6d6d   For serial comm
+00001a30: 756e 6963 6174 696f 6e2c 2069 7420 6368  unication, it ch
+00001a40: 6563 6b20 666f 7220 4453 5220 6c69 6e65  eck for DSR line
+00001a50: 2066 726f 6d20 5352 5320 5247 4120 6973   from SRS RGA is
+00001a60: 2073 6574 2068 6967 682e 0d0a 2020 2020   set high...    
+00001a70: 2020 2020 466f 7220 4574 6865 726e 6574      For Ethernet
+00001a80: 2063 6f6d 6d75 6e69 6361 7469 6f6e 2c20   communication, 
+00001a90: 6974 2063 6865 636b 2069 6620 7468 6520  it check if the 
+00001aa0: 5443 5020 736f 636b 6574 2069 7320 6f70  TCP socket is op
+00001ab0: 656e 2e0d 0a20 2020 2020 2020 2022 2222  en...        """
+00001ac0: 0d0a 2020 2020 2020 2020 6966 2073 656c  ..        if sel
+00001ad0: 662e 636f 6d6d 2e74 7970 6520 3d3d 2049  f.comm.type == I
+00001ae0: 6e74 6572 6661 6365 2e53 4552 4941 4c3a  nterface.SERIAL:
+00001af0: 0d0a 2020 2020 2020 2020 2020 2020 7265  ..            re
+00001b00: 7475 726e 2073 656c 662e 636f 6d6d 2e5f  turn self.comm._
+00001b10: 7365 7269 616c 2e64 7372 0d0a 2020 2020  serial.dsr..    
+00001b20: 2020 2020 656c 7365 3a0d 0a20 2020 2020      else:..     
+00001b30: 2020 2020 2020 2072 6574 7572 6e20 7365         return se
+00001b40: 6c66 2e69 735f 636f 6e6e 6563 7465 6428  lf.is_connected(
+00001b50: 290d 0a0d 0a20 2020 2064 6566 2067 6574  )....    def get
+00001b60: 5f6d 6178 5f6d 6173 7328 7365 6c66 293a  _max_mass(self):
+00001b70: 0d0a 2020 2020 2020 2020 2222 220d 0a20  ..        """.. 
+00001b80: 2020 2020 2020 2047 6574 206d 6178 696d         Get maxim
+00001b90: 756d 206d 6173 7320 7468 6174 2063 616e  um mass that can
+00001ba0: 2062 6520 7573 6564 2066 6f72 2061 2073   be used for a s
+00001bb0: 6361 6e0d 0a0d 0a20 2020 2020 2020 2053  can....        S
+00001bc0: 5253 2052 4741 3130 3020 6d6f 6465 6c20  RS RGA100 model 
+00001bd0: 6861 7320 7468 6520 6d61 7869 6d75 6d20  has the maximum 
+00001be0: 6d61 7373 206f 6620 3130 3020 414d 553b  mass of 100 AMU;
+00001bf0: 0d0a 2020 2020 2020 2020 5352 5320 5247  ..        SRS RG
+00001c00: 4132 3030 2c20 3230 3020 414d 553b 2061  A200, 200 AMU; a
+00001c10: 6e64 2053 5253 2052 4741 3330 302c 2033  nd SRS RGA300, 3
+00001c20: 3030 2041 4d55 2e0d 0a0d 0a20 2020 2020  00 AMU.....     
+00001c30: 2020 2052 6574 7572 6e73 0d0a 2020 2020     Returns..    
+00001c40: 2020 2020 2d2d 2d2d 2d2d 2d2d 0d0a 2020      --------..  
+00001c50: 2020 2020 2020 2020 2020 696e 740d 0a20            int.. 
+00001c60: 2020 2020 2020 2020 2020 2020 2020 206d                 m
+00001c70: 6178 696d 756d 206d 6173 730d 0a20 2020  aximum mass..   
+00001c80: 2020 2020 2022 2222 0d0a 2020 2020 2020       """..      
+00001c90: 2020 7265 7475 726e 2073 656c 662e 5f6d    return self._m
+00001ca0: 5f6d 6178 0d0a 0d0a 2020 2020 6465 6620  _max....    def 
+00001cb0: 6361 6c69 6272 6174 655f 616c 6c28 7365  calibrate_all(se
+00001cc0: 6c66 293a 0d0a 2020 2020 2020 2020 2222  lf):..        ""
+00001cd0: 220d 0a20 2020 2020 2020 2043 616c 6962  "..        Calib
+00001ce0: 7261 7465 2061 6c6c 0d0a 0d0a 2020 2020  rate all....    
+00001cf0: 2020 2020 7265 7475 726e 730d 0a20 2020      returns..   
+00001d00: 2020 2020 202d 2d2d 2d2d 2d2d 2d0d 0a20       --------.. 
+00001d10: 2020 2020 2020 2020 2020 2069 6e74 0d0a             int..
+00001d20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001d30: 4572 726f 7220 7374 6174 7573 2062 7974  Error status byt
+00001d40: 6520 6166 7465 7220 6361 6c69 6272 6174  e after calibrat
+00001d50: 696f 6e0d 0a20 2020 2020 2020 2022 2222  ion..        """
+00001d60: 0d0a 2020 2020 2020 2020 7265 706c 7920  ..        reply 
+00001d70: 3d20 7365 6c66 2e63 6f6d 6d2e 7175 6572  = self.comm.quer
+00001d80: 795f 7465 7874 5f77 6974 685f 6c6f 6e67  y_text_with_long
+00001d90: 5f74 696d 656f 7574 2822 4341 222c 2031  _timeout("CA", 1
+00001da0: 3230 290d 0a20 2020 2020 2020 2065 7272  20)..        err
+00001db0: 6f72 5f73 7461 7475 7320 3d20 696e 7428  or_status = int(
+00001dc0: 7265 706c 7929 0d0a 2020 2020 2020 2020  reply)..        
+00001dd0: 7265 7475 726e 2065 7272 6f72 5f73 7461  return error_sta
+00001de0: 7475 730d 0a0d 0a20 2020 2064 6566 2063  tus....    def c
+00001df0: 616c 6962 7261 7465 5f65 6c65 6374 726f  alibrate_electro
+00001e00: 6d65 7465 7228 7365 6c66 293a 0d0a 2020  meter(self):..  
+00001e10: 2020 2020 2020 2222 220d 0a20 2020 2020        """..     
+00001e20: 2020 2043 616c 6962 7261 7465 2065 6c65     Calibrate ele
+00001e30: 6374 726f 6d65 7465 7227 7320 492d 5620  ctrometer's I-V 
+00001e40: 7265 7370 6f6e 7365 0d0a 0d0a 2020 2020  response....    
+00001e50: 2020 2020 7265 7475 726e 730d 0a20 2020      returns..   
+00001e60: 2020 2020 202d 2d2d 2d2d 2d2d 2d0d 0a20       --------.. 
+00001e70: 2020 2020 2020 2020 2020 2069 6e74 0d0a             int..
+00001e80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001e90: 4572 726f 7220 7374 6174 7573 2062 7974  Error status byt
+00001ea0: 6520 6166 7465 7220 6361 6c69 6272 6174  e after calibrat
+00001eb0: 696f 6e0d 0a20 2020 2020 2020 2022 2222  ion..        """
+00001ec0: 0d0a 2020 2020 2020 2020 7265 706c 7920  ..        reply 
+00001ed0: 3d20 7365 6c66 2e63 6f6d 6d2e 7175 6572  = self.comm.quer
+00001ee0: 795f 7465 7874 5f77 6974 685f 6c6f 6e67  y_text_with_long
+00001ef0: 5f74 696d 656f 7574 2822 434c 222c 2031  _timeout("CL", 1
+00001f00: 3230 290d 0a20 2020 2020 2020 2065 7272  20)..        err
+00001f10: 6f72 5f73 7461 7475 7320 3d20 696e 7428  or_status = int(
+00001f20: 7265 706c 7929 0d0a 2020 2020 2020 2020  reply)..        
+00001f30: 7265 7475 726e 2065 7272 6f72 5f73 7461  return error_sta
+00001f40: 7475 730d 0a                             tus..
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/scans.py` & `srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/scans.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,26 @@
 
 import time
 import numpy as np
 
 from srsgui.inst.communications import Interface, SerialInterface, TcpipInterface
 from srsgui.inst.component import Component
-from srsgui.inst.commands import IntCommand, IntGetCommand
+from srsgui.inst.commands import IntGetCommand
 
+from .commands import IntNSCommand
 
 class Scans(Component):
     """
     It contains implementation of setup and data acquisition from SRS RGAs
     """
 
-    initial_mass = IntCommand('MI')
-    final_mass = IntCommand('MF')
-    speed = IntCommand('NF')
-    resolution = IntCommand('SA')
+    initial_mass = IntNSCommand('MI')
+    final_mass = IntNSCommand('MF')
+    speed = IntNSCommand('NF')
+    resolution = IntNSCommand('SA')
     total_points_analog = IntGetCommand('AP')
     total_points_histogram = IntGetCommand('HP')
 
     def __init__(self, parent):
         super().__init__(parent)
 
         self.scan_type = None
@@ -30,14 +31,15 @@
         self.total_current = 0
 
         self.analog_scan_command = 'SC1'
         self.histogram_scan_command = 'HS1'
         self.single_mass_scan_command = 'MR{}'
         self.scan_read = self.read_long
         self.scan_convert = self.convert_to_long
+        self.check_buffer_overrun = True
 
         self._data_callback_period = 0.25
         self.set_callbacks()
 
     def set_callbacks(self, data_available=None, scan_started=None, scan_finished=None):
         """
         Set callback functions to be called when data is available, when a scan is started,
@@ -152,15 +154,15 @@
             step = 1.0 / self.resolution
         else:
             step = 1.0
 
         self.mass_axis = np.arange(self.initial_mass, self.final_mass + step / 2.0, step)
         return self.mass_axis
 
-    def get_analog_scan(self, uga_reset=False):
+    def get_analog_scan(self):
         """
         Run an analog scan
 
         Set_scan_parameters() before running
         """
         self.scan_type = 'analog_scan'
         try:
@@ -178,23 +180,23 @@
             start_time = time.time()
             for index in range(total_points):
                 self.spectrum[index] = self.scan_read()
                 current_time = time.time()
                 if self._data_available_callback and current_time - start_time > self._data_callback_period:
                     self._data_available_callback(index)
                     start_time = current_time
-            if uga_reset:
+            if self.check_buffer_overrun:
                 self.total_current = 0  # if the total current is 0, there are missing bytes.
                 last_data = self.comm._recv()  # Read the last
             else:
                 self.total_current = 0
                 self.total_current = self.scan_read()
 
         # fix RGA100 comm buffer overflow bug
-        if uga_reset:
+        if self.check_buffer_overrun:
             length = len(last_data)
             # print('final word: {}'.format(length))
             if length > 4:
                 print('Communication buffer reset')
                 self.comm.query_text('IN0')    # if there is extra bytes, reset the RGA
             elif length == 4:
                 self.total_current = self.convert_to_long(last_data)
@@ -240,16 +242,14 @@
         :rtype: NumPy array
         """
 
         self.scan_type = 'multiple_mass_scan'
         self.spectrum = np.zeros(len(mass_list))
         for index, amu in enumerate(mass_list):
             intensity = self.get_single_mass_scan(amu)
-            # self.comm.send("MR " + str(amu))
-            # intensity = self.comm.read_long()
             self.spectrum[index] = intensity
         return self.spectrum
 
     def get_single_mass_scan(self, mass):
         """
         Measure ion intensity for a single mass
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/instruments/rga100/sicp.py` & `srsinst.rga-0.2.9/srsinst/rga/instruments/rga100/sicp.py`

 * *Files 8% similar despite different names*

```diff
@@ -47,14 +47,23 @@
     SICP_SEQ_CALL = 0x01
     SICP_SEQ_REPLY = 0x02
     SICP_SEQ_SET = 0x03
     SICP_SEQ_DHCP = 0x04
 
     PacketSize = 100
 
+    # Status from packet
+    ST_CONNECTED = 'Connected'
+    ST_CONFIGURABLE = 'Configurable'
+    ST_IP_CONFLICT = 'IP_conflict'
+    ST_DHCP_RUNNING = 'DHCP running'
+    ST_DHCP_FAILED = 'DHCP failed'
+    ST_DATA_LENGTH_INVALID = 'Error during SICP'
+    ST_AVAILABLE = 'Available'
+
     def __init__(self, data):
         self.input_data = data
         self.data = bytearray(self.input_data)
         if len(self.data) != Packet.PacketSize:
             raise ValueError(f'Packet size is not {Packet.PacketSize}, but {len(self.data)}')
         self.decode()
 
@@ -173,27 +182,27 @@
         print("IP address conflict    : {}".format(self.is_ip_conflicted()))
         print("Invalid packet length  : {}".format(self.is_data_length_invalid()))
         print("Device status : {}".format(self.device_status))
         print("===============================")
 
     def get_short_status_from_packet(self):
         if self.is_connected():
-            return 'Connected'
+            return Packet.ST_CONNECTED
         elif self.is_configurable():
-            return 'Configurable'
+            return Packet.ST_CONFIGURABLE
         elif self.is_ip_conflicted():
-            return 'IP_conflict'
+            return Packet.ST_IP_CONFLICT
         elif self.is_dhcp_running():
-            return 'DHCP running'
+            return Packet.ST_DHCP_RUNNING
         elif self.is_dhcp_failed():
-            return 'DHCP failed'
+            return Packet.ST_DHCP_FAILED
         elif self.is_data_length_invalid():
-            return 'Error during SICP'
+            return Packet.ST_DATA_LENGTH_INVALID
         else:
-            return 'Available'
+            return Packet.ST_AVAILABLE
 
     def set_sequence_number(self, number: int):
         if number == Packet.SICP_SEQ_SET or number == Packet.SICP_SEQ_DHCP:
             self.data[8:10] = 0x0, number
         else:
             raise ValueError(f'Invalid sequence number: {number}')
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/plots/analogscanplot.py` & `srsinst.rga-0.2.9/srsinst/rga/plots/analogscanplot.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import time
 import logging
 from matplotlib.axes import Axes
-from srsgui.task import Task
+from srsgui import Task
 from srsinst.rga.plots.basescanplot import BaseScanPlot
 from srsinst.rga.plots.analysis import calculate_baseline
 from srsinst.rga.instruments.rga100.scans import Scans
 
 logger = logging.getLogger(__name__)
 
 
@@ -13,15 +13,15 @@
     def __init__(self, parent: Task, ax: Axes, scan: Scans, plot_name='', save_to_file=True):
         if not issubclass(type(parent), Task):
             raise TypeError('Invalid parent {} is not a Task subclass'.format(type(parent)))
         if not hasattr(ax, 'figure'):
             raise TypeError('ax has no figure attribute. type: "{}"'.format(type(ax)))
 
         super().__init__(parent, ax, plot_name, save_to_file)
-
+        self.first_scan = True
         self.conversion_factor = 0.1
         self.unit = 'fA'
 
         self.scan = scan
         self.data = {'x': [], 'y': [], 'prev_x': [], 'prev_y': [], 'prev_baseline': []}
 
         self.ax.set_xlabel("Mass (AMU)")
@@ -31,14 +31,15 @@
         self.prev_baseline, = self.ax.plot(self.data['x'], self.data['y'], label='Prev. baseline')
 
         self.ax.set_ylim(1, 10000)
 
         self.reset()
 
     def reset(self):
+        self.first_scan = True
         self.initial_mass = self.scan.initial_mass
         self.final_mass = self.scan.final_mass
         self.resolution = self.scan.resolution
         self.set_x_axis(self.scan.get_mass_axis(True))
 
         self.ax.set_xlim(self.initial_mass, self.final_mass, auto=False)
         self.scan.set_callbacks(self.scan_data_available_callback,
@@ -55,24 +56,31 @@
         self.parent.request_figure_update(self.ax.figure)
 
     def scan_finished_callback(self):
         self.data['x'] = self.x_axis
         self.data['y'] = self.scan.spectrum * self.conversion_factor
         self.data['prev_x'] = self.data['x']
         self.data['prev_y'] = self.data['y']
-        self.data['prev_baseline'] = calculate_baseline(self.data['y'], 1e-5, 5e5)
+        self.data['prev_baseline'] = calculate_baseline(self.data['y'], 1e-5, 1e6)
 
         self.line.set_xdata(self.data['x'])
         self.line.set_ydata(self.data['y'])
         self.prev_line.set_xdata(self.data['prev_x'])
         self.prev_line.set_ydata(self.data['prev_y'])
 
         self.prev_baseline.set_xdata(self.data['prev_x'])
         self.prev_baseline.set_ydata(self.data['prev_baseline'])
 
+        if self.first_scan:
+            self.first_scan = False
+            self.ax.margins(x=0.0, y=0.1)
+            self.ax.relim()
+            self.ax.autoscale()
+            self.ax.autoscale_view()
+
         # Tell GUI to redraw the plot
         self.parent.request_figure_update(self.ax.figure)
         self.save_scan_data(self.scan.spectrum)
 
     def cleanup(self):
         """
         callback functions should be disconnected when task is finished
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/plots/analysis.py` & `srsinst.rga-0.2.9/srsinst/rga/plots/analysis.py`

 * *Files identical despite different names*

### Comparing `srsinst.rga-0.2.8/srsinst/rga/plots/basescanplot.py` & `srsinst.rga-0.2.9/srsinst/rga/plots/basescanplot.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 
 import time
 import logging
 from matplotlib.axes import Axes
-from srsgui.task import Task
+from srsgui import Task
 
 logger = logging.getLogger(__name__)
 
 
 class BaseScanPlot:
     def __init__(self, parent: Task, ax: Axes, plot_name='', save_to_file=False):
         self.type = self.__class__.__name__
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/plots/histogramscanplot.py` & `srsinst.rga-0.2.9/srsinst/rga/plots/histogramscanplot.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 
 import logging
 import numpy
 from matplotlib.axes import Axes
-from srsgui.task import Task
+from srsgui import Task
 from srsinst.rga.plots.basescanplot import BaseScanPlot
 
 from srsinst.rga.instruments.rga100.scans import Scans
 
 
 
 logger = logging.getLogger(__name__)
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/plots/timeplot.py` & `srsinst.rga-0.2.9/srsinst/rga/plots/timeplot.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,20 +1,23 @@
 
 import time
 import logging
 import numpy as np
 from datetime import datetime, timedelta
 from matplotlib.axes import Axes
-from srsgui.task import Task
+from srsgui import Task
 
 logger = logging.getLogger(__name__)
 
 
 class TimePlot:
-    def __init__(self, parent: Task, ax: Axes, plot_name='', data_names=('Y',), save_to_file=True, use_datetime=True):
+    def __init__(self, parent: Task, ax: Axes, plot_name='', data_names=('Y',), save_to_file=True,
+                 use_datetime=True, plot_options=None):
+        if plot_options is None:
+            plot_options = {}
         if not issubclass(type(parent), Task):
             raise TypeError('Invalid parent {} is not a Task subclass'.format(type(parent)))
         # if type(ax) is not Axes or AxesSubplot:
         #    raise TypeError('ax is not a Matplotlib Axes class, but "{}"'.format(type(ax)))
 
         self.type = self.__class__.__name__
         self.parent = parent
@@ -120,45 +123,44 @@
         else:
             self.time[self.data_points] = time.time() - self.initial_time
 
         for key, point in zip(self.data_keys, data_list):
             self.data[key][self.data_points] = point * self.conversion_factor
         self.data_points += 1
 
-        if len(self.time) == 1:
+        if self.data_points == 1:
             min_value = min(data_list)
             max_value = max(data_list)
             if min_value == 0 and max_value == 0:
                 min_value = -1.0
                 max_value = 1.0
             min_value *= self.conversion_factor
             max_value *= self.conversion_factor
             self.ax.set_ylim(min_value - abs(min_value)/2, max_value + abs(max_value)/2)
         if update_figure:
             self.update_plot()
-        self.save_data(data_list)
+        self.save_data(self.time[self.data_points - 1], data_list)
 
-    def save_data(self, data_list):
+    def save_data(self, timestamp, data_list):
         if not self.save_to_file:
             return
         if not self.header_saved:
             self.parent.session_handler.add_dict_to_file(self.name, self.get_plot_info())
             if self.use_datetime:
                 self.parent.create_table_in_file(self.name, 'Date time', *self.data_keys)
             else:
                 self.parent.create_table_in_file(self.name, 'Elapsed time', *self.data_keys)
             self.header_saved = True
         # write the spectrum in to the data file
         if self.use_datetime:
-            timestamp = datetime.now().isoformat()
-            # timestamp = datetime.now().strftime('%H:%M:%S')
+            ts = str(timestamp)  # datetime.now().isoformat()
         else:
-            timestamp = self.round_float(time.time() - self.initial_time)
+            ts = self.round_float(timestamp)
 
-        self.parent.add_to_table_in_file(self.name, timestamp, *map(self.round_float, data_list))
+        self.parent.add_to_table_in_file(self.name, ts, *map(self.round_float, data_list))
 
     def round_float(self, number):
         # set the resolution of the number with self.round_float_resolution
         fmt = '{{:.{}e}}'.format(self.round_float_resolution)
         return float(fmt.format(number))
 
     def get_plot_info(self):
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/rga.taskconfig` & `srsinst.rga-0.2.9/srsinst/rga/rga.taskconfig`

 * *Files identical despite different names*

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/analogscantask.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/analogscantask.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,15 @@
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import ListInput, IntegerInput, InstrumentInput
 
 from srsinst.rga.plots.analogscanplot import AnalogScanPlot
-from srsinst.rga import get_rga
+
+# get_rga is imported from the path relative to the .taskconfig file
+from instruments import get_rga
 
 
 class AnalogScanTask(Task):
     """Task to run analog scans.
     """
     InstrumentName = 'instrument to control'
     StartMass = 'start mass'
@@ -59,18 +61,15 @@
                                      self.params[self.ScanSpeed],
                                      self.params[self.StepSize])
 
     def test(self):
         self.set_task_passed(True)
         self.add_details('{}'.format(self.id_string), key='ID')
 
-        while True:
-            if not self.is_running():
-                break
-
+        while self.is_running():
             try:
                 self.rga.scan.get_analog_scan()
             except Exception as e:
                 self.set_task_passed(False)
                 self.logger.error('{}: {}'.format(e.__class__.__name__, e))
                 if not self.rga.is_connected():
                     self.logger.error('"{}" is disconnected'.format(self.params[self.InstrumentName]))
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/cemcontroltask.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/cemcontroltask.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,13 @@
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import ListInput, InstrumentInput
-from srsinst.rga import get_rga
+
+# get_rga is imported from the path relative to the .taskconfig file
+from instruments import get_rga
 
 
 class CEMControlTask(Task):
     """Task to set CEM voltage
     """
     InstrumentName = 'instrument to control'
     CEMState = 'cem high voltage'
@@ -39,15 +41,15 @@
             self.logger.info('Setting CEM voltage to {} V'.format(set_voltage))
             self.add_details('{} V for gain {:.0f}'.format(set_voltage, set_gain))
 
             status_byte = None
             try:
                 print('Previous errors: {}'.format(self.rga.status.get_error_text()))
                 self.rga.cem.voltage = set_voltage
-                status_byte = self.rga.cem.last_set_status
+                status_byte = self.rga.status.error_status
                 self.logger.info('Errors after setting CEM voltage to {} V:  {}'
                                  .format(set_voltage,  self.rga.status.get_error_text(status_byte)))
             except Exception as e:
                 self.logger.error('Error while setting CEM voltage to {} V: {}'.format(set_voltage, e))
 
             if status_byte:
                 self.set_task_passed(False)
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/cemgaintask.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/cemgaintask.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,16 +1,18 @@
 import sys
 import math
 import time
 import math
 import numpy as np
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import FloatInput, IntegerInput, InstrumentInput
-from srsinst.rga import get_rga
+
+# get_rga is imported from the path relative to the .taskconfig file
+from instruments import get_rga
 
 
 class CEMGainTask(Task):
     """Task to measure CEM gain at different CEM voltage
     """
 
     InstrumentName = 'instrument to control'
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/compositionanalysistask.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/compositionanalysistask.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,20 @@
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import StringInput, IntegerInput, InstrumentInput
 
 from srsinst.rga.plots.analysis import get_peak_from_analog_scan
 from srsinst.rga.plots.analogscanplot import AnalogScanPlot
 from srsinst.rga.plots.timeplot import TimePlot
 
 import numpy as np
 from scipy.optimize import nnls
-from srsinst.rga import get_rga
+
+# get_rga is imported from the path relative to the .taskconfig file
+from instruments import get_rga
 
 
 class CompositionAnalysisTask(Task):
     """
 Task to run analog scans and analyze composition with a list of gas name \
 from a gas library file.
     """
@@ -50,14 +52,15 @@
         self.init_scan()
 
         self.lib = self.read_gas_library()
         self.mat = self.build_coeff_matrix(self.lib, self.params[self.StartMass], 
                                            self.params[self.StopMass], self.gas_list)
 
         # Set up an derived P vs T plot
+        self.init_plot = True
         self.ax_pvst = self.get_figure(self.DerivedPvsTPlot).add_subplot(111)
         self.pvst_plot = TimePlot(self, self.ax_pvst, 'PP vs T', self.gas_list)
         self.pvst_plot.ax.set_yscale('log')
 
         # Set up a composition analysis plot for the last full analog scan
         self.ax_comp = self.get_figure(self.CompPlot).add_subplot(111)
         self.ax_comp.set_title('Composition analysis')
@@ -114,32 +117,31 @@
                                      self.params[self.ScanSpeed],
                                      self.params[self.StepSize])
 
     def test(self):
         self.set_task_passed(True)
         self.add_details('{}'.format(self.id_string), key='ID')
 
-        while True:
-            if not self.is_running():
-                break
-
+        while self.is_running():
             try:
                 self.rga.scan.get_analog_scan()
             except Exception as e:
                 self.set_task_passed(False)
                 self.logger.error('{}: {}'.format(e.__class__.__name__, e))
                 if not self.rga.is_connected():
                     self.logger.error('"{}" is disconnected'.format(self.params[self.InstrumentName]))
                     break
 
             # manually update self.line_comp
             self.line_comp.set_xdata(self.plot.data['prev_x'])
             corrected_y = self.plot.data['prev_y'] - self.plot.data['prev_baseline']
             self.line_comp.set_ydata(corrected_y)
-            
+            if self.init_plot:
+                self.ax_comp.set_ylim(self.ax.get_ylim())
+                self.init_plot = False
             ys = np.array([get_peak_from_analog_scan(self.plot.data['prev_x'],
                                                      corrected_y, mass)
                           for mass in self.bar_x])
 
             # Non-negative least square fit
             c, res = nnls(self.mat, ys)
             # c, res, _, _ = np.linalg.lstsq(self.mat, ys, rcond=None)
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/derivedpvstscantask.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/derivedpvstscantask.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import ListInput, IntegerInput, StringInput, InstrumentInput
 
 from srsinst.rga.plots.timeplot import TimePlot
 from srsinst.rga.plots.analogscanplot import AnalogScanPlot
-from srsinst.rga import get_rga
+
+# get_rga is imported from the path relative to the .taskconfig file
+from instruments import get_rga
 
 
 class DerivedPvsTScanTask(Task):
     """Task to run analog scans wide enough to cover all the specified masses
 and extract ion intensity for the masses from the analog scans.
     """
     InstrumentName = 'instrument to control'
@@ -80,18 +82,15 @@
         self.ax_log.set_xlabel("Mass (AMU)")
         self.ax_log.set_ylabel('Intensity')
         self.line_log, = self.ax_log.plot([1], [1])
         self.ax_log.set_yscale('log')
 
     def test(self):
         self.set_task_passed(True)
-        while True:
-            if not self.is_running():
-                break
-
+        while self.is_running():
             try:
                 self.rga.scan.get_analog_scan()
 
                 # manually update self.plot_log
                 self.line_log.set_xdata(self.plot_analog.data['prev_x'])
                 self.line_log.set_ydata(self.plot_analog.data['prev_y']
                                         - self.plot_analog.data['prev_baseline'])
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/filamentcontroltask.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/filamentcontroltask.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,13 @@
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import FloatInput, InstrumentInput
-from srsinst.rga import get_rga
+
+# get_rga is imported from the path relative to the .taskconfig file
+from instruments import get_rga
 
 
 class FilamentControlTask(Task):
     """
     Task to set filament emission current
     """
     # Input parameter name
@@ -25,19 +27,18 @@
         # Get the input parameters from GUI
         self.params = self.get_all_input_parameters()
 
         # Get rga from the instrument
         self.rga = get_rga(self, self.params[self.InstrumentName])
 
     def test(self):
-        self.logger.info('Filament emission current before change: {} mA'.format(self.rga.ionizer.emission_current))
-        self.logger.info('Setting emission current to {} mA'.format(self.params[self.EmissionCurrent]))
-
-        error_bites = ''
         try:
+            self.logger.info('Filament emission current before change: {} mA'.format(self.rga.ionizer.emission_current))
+            self.logger.info('Setting emission current to {} mA'.format(self.params[self.EmissionCurrent]))
+
             # Clear filament error before changing emission current
             print('Previous errors: {}'.format(self.rga.status.get_error_text()))
 
             self.rga.ionizer.emission_current = self.params[self.EmissionCurrent]
             error_bits = self.rga.status.get_errors()
             self.logger.info('Errors after setting emission current:  {}'
                              .format(self.rga.status.get_error_text(error_bits)))
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/histogramscantask.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/histogramscantask.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,17 @@
 
 import numpy
 from datetime import datetime
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import ListInput, IntegerInput, InstrumentInput
 from srsinst.rga.plots.histogramscanplot import HistogramScanPlot
-from srsinst.rga import get_rga
+
+# get_rga is imported from the path relative to the .taskconfig file
+from instruments import get_rga
 
 
 class HistogramScanTask(Task):
     """Task to run histogram scans.
     """
 
     InstrumentName = 'instrument to control'
@@ -63,17 +65,15 @@
                                      self.params[self.StopMass],
                                      self.params[self.ScanSpeed])
 
     def test(self):
         self.set_task_passed(True)
         self.add_details('{}'.format(self.rga.status.id_string), key='ID')
 
-        while True:
-            if not self.is_running():
-                break
+        while self.is_running():
             try:
                 self.rga.scan.get_histogram_scan()
             except Exception as e:
                 self.set_task_passed(False)
                 self.logger.error('{}: {}'.format(e.__class__.__name__, e))
                 if not self.rga.is_connected():
                     break
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/pvstscantask.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/pvstscantask.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,15 @@
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import ListInput, IntegerInput, StringInput, InstrumentInput
 
 from srsinst.rga.plots.timeplot import TimePlot
-from srsinst.rga import get_rga
+
+# get_rga is imported from the path relative to the .taskconfig file
+from instruments import get_rga
 
 
 class PvsTScanTask(Task):
     """Task to measure continuously ion intensity for multiple masses
     """
     InstrumentName = 'instrument to control'
     MassesToMeasure = 'masses to measure'
@@ -47,17 +49,14 @@
             self.conversion_factor = 0.1
             self.plot.set_conversion_factor(self.conversion_factor, 'fA')
         else:
             self.conversion_factor = self.rga.pressure.get_partial_pressure_sensitivity_in_torr()
             self.plot.set_conversion_factor(self.conversion_factor, 'Torr')
 
     def test(self):
-        while True:
-            if not self.is_running():
-                break
+        while self.is_running():
             intensity_list = self.rga.scan.get_multiple_mass_scan(*self.mass_list)
-            
             self.plot.add_data(intensity_list, True)
 
     def cleanup(self):
         pass
```

### Comparing `srsinst.rga-0.2.8/srsinst/rga/tasks/searchlan.py` & `srsinst.rga-0.2.9/srsinst/rga/tasks/searchlan.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 
-from srsgui.task.task import Task
+from srsgui import Task
 from srsgui.task.inputs import ListInput
 from srsinst.rga import SICP
 
 
 class SearchLanTask(Task):
     """Search for RGAs on the local area network (LAN) using SICP.
 It may not work if a computer firewall blocks UDP port 818 used for broadcast.
@@ -41,15 +41,15 @@
                 self.logger.info('Name: {:20s}, SN: {}, IP: {}, Status: {}'
                                  .format(p.device_name, p.serial_number,
                                          p.convert_to_ip_format(p.ip_address),
                                          p.get_short_status_from_packet()))
             else:
                 p.print_info()
 
-            if p.get_short_status_from_packet() == 'Available':
+            if p.get_short_status_from_packet() == p.ST_AVAILABLE:
                 self.display_result('Name: {:20s}, SN: {:10d}, IP: {:16s}'
                                     .format(p.device_name, p.serial_number,
                                             p.convert_to_ip_format(p.ip_address)))
         self.set_task_passed(True)
 
     def cleanup(self):
         self.logger.info('Search completed')
```

### Comparing `srsinst.rga-0.2.8/srsinst.rga.egg-info/PKG-INFO` & `srsinst.rga-0.2.9/srsinst.rga.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: srsinst.rga
-Version: 0.2.8
+Version: 0.2.9
 Summary: Instrument library and GUI application for SRS RGA
 Author: Chulhoon Kim
 License: MIT license
 Keywords: RGA,residual gas analyzer,SRS,Stanford Research Systems
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: MIT License
@@ -36,15 +36,15 @@
 
 To use its full GUI application, create a virtual environment and install:
 
     python -m pip install srsinst.rga[full]
 
 
 ## Run `srsinst.rga` as GUI application
-if the Python Scripts directory is in PATH environment variable,
+If the Python Scripts directory is in PATH environment variable,
 Start the application by typing from the command line:
 
     rga
 
 If not,
 
     python -m srsinst.rga
@@ -53,18 +53,18 @@
 
 Connect to an RGA from the Instruments menu.
 Select a task from the Task menu.
 Press the green arrow to run the selected task. 
 
 You can write your own task or modify an existing one and run it from the application, too.
 
-## Use `srsinst.rga` as instument driver
+## Use `srsinst.rga` as instrument driver
 * Start the Python program, or an editor of your choice to write a Python script.
-* import the **RGA** class from `rga` package
-* Initialize of an **RGA** instance to connect to an SRS RGA.
+* import the **RGA** class from `rga` package.
+* Instantiate **RGA** to connect to an SRS RGA.
 
         from srsinst.rga import RGA100 as RGA
 
         # for TCPIP communication
         ip_address = '192.168.1.100'
         user_id = 'admin'
         password = 'admin'
```

### Comparing `srsinst.rga-0.2.8/srsinst.rga.egg-info/SOURCES.txt` & `srsinst.rga-0.2.9/srsinst.rga.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -32,9 +32,10 @@
 srsinst/rga/tasks/analogscantask.py
 srsinst/rga/tasks/cemcontroltask.py
 srsinst/rga/tasks/cemgaintask.py
 srsinst/rga/tasks/compositionanalysistask.py
 srsinst/rga/tasks/derivedpvstscantask.py
 srsinst/rga/tasks/filamentcontroltask.py
 srsinst/rga/tasks/histogramscantask.py
+srsinst/rga/tasks/peaktuningtask.py
 srsinst/rga/tasks/pvstscantask.py
 srsinst/rga/tasks/searchlan.py
```

