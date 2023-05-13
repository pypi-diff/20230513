# Comparing `tmp/simple-simon-0.0.3.tar.gz` & `tmp/simple-simon-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simple-simon-0.0.3.tar", last modified: Sat May 13 14:47:18 2023, max compression
+gzip compressed data, was "simple-simon-0.0.5.tar", last modified: Sat May 13 15:01:28 2023, max compression
```

## Comparing `simple-simon-0.0.3.tar` & `simple-simon-0.0.5.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:47:18.476905 simple-simon-0.0.3/
--rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simple-simon-0.0.3/LICENSE
--rw-rw-rw-   0        0        0     5856 2023-05-13 14:47:18.476905 simple-simon-0.0.3/PKG-INFO
--rw-rw-rw-   0        0        0     5552 2023-05-13 14:25:47.000000 simple-simon-0.0.3/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 14:47:18.476905 simple-simon-0.0.3/setup.cfg
--rw-rw-rw-   0        0        0     1239 2023-05-13 14:47:15.000000 simple-simon-0.0.3/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:47:18.461284 simple-simon-0.0.3/simon/
--rw-rw-rw-   0        0        0    29858 2023-05-13 14:45:40.000000 simple-simon-0.0.3/simon/simon.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:47:18.476905 simple-simon-0.0.3/simon/simple_simon.egg-info/
--rw-rw-rw-   0        0        0     5856 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      250 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       11 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 15:01:28.194393 simple-simon-0.0.5/
+-rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simple-simon-0.0.5/LICENSE
+-rw-rw-rw-   0        0        0     5838 2023-05-13 15:01:28.194393 simple-simon-0.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0     5534 2023-05-13 15:00:05.000000 simple-simon-0.0.5/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 15:01:28.194393 simple-simon-0.0.5/setup.cfg
+-rw-rw-rw-   0        0        0     1239 2023-05-13 15:00:21.000000 simple-simon-0.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:01:28.194393 simple-simon-0.0.5/simon/
+-rw-rw-rw-   0        0        0    29858 2023-05-13 14:45:40.000000 simple-simon-0.0.5/simon/simon.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:01:28.194393 simple-simon-0.0.5/simon/simple_simon.egg-info/
+-rw-rw-rw-   0        0        0     5838 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      250 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        6 2023-05-13 15:01:28.000000 simple-simon-0.0.5/simon/simple_simon.egg-info/top_level.txt
```

### Comparing `simple-simon-0.0.3/LICENSE` & `simple-simon-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `simple-simon-0.0.3/PKG-INFO` & `simple-simon-0.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-simon
-Version: 0.0.3
+Version: 0.0.5
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -35,15 +35,15 @@
 pip install simple-simon
 ```
 
 ## Usage
 Here's a quick example of the `Monitor` class used to track a moving object simulation:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 # create Monitor - this already opens an output directory and a toggle-buttons control window
 mon = Monitor('Example Monitor')
 
 # add a new 'tracker' to track variables
 tr = mon.tracker('time', 'velocity')
 
@@ -112,15 +112,15 @@
 ```
 
 ### About toggles
 The 'Toggles' window is opened from the moment a Monitor is created and until `finalize()` is called.
 Some toggles are added by default. Custom toggles can be added in a very simple way:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 # after this, the toggles window is opened
 mon = Monitor('Custom Toggles Example')
 
 # add a toggle button that quits the simulation
 quit_toggle = mon.add_toggle(desc='Quit simulation')
 
@@ -139,15 +139,15 @@
 
 ### Loading Monitor data
 Finally, another cool feature of the Monitor class, is that all the data stored in 
 an output directory, can later be loaded into a Monitor object. This way, a simulation 
 that's been terminated can be resumed, and the data will keep streaming to the same place:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 mon = Monitor('Example Monitor')
 mon.load_from_dir()  # this loads all the data from the 'Example Monitor' output directory
 
 # now all data has been loaded back to the Monitor
 print(len(mon.trackers))  # a list of all trackers
 mon.plot(mon.trackers[0])  # same data can be plotted
```

### Comparing `simple-simon-0.0.3/README.md` & `simple-simon-0.0.5/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -24,15 +24,15 @@
 pip install simple-simon
 ```
 
 ## Usage
 Here's a quick example of the `Monitor` class used to track a moving object simulation:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 # create Monitor - this already opens an output directory and a toggle-buttons control window
 mon = Monitor('Example Monitor')
 
 # add a new 'tracker' to track variables
 tr = mon.tracker('time', 'velocity')
 
@@ -101,15 +101,15 @@
 ```
 
 ### About toggles
 The 'Toggles' window is opened from the moment a Monitor is created and until `finalize()` is called.
 Some toggles are added by default. Custom toggles can be added in a very simple way:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 # after this, the toggles window is opened
 mon = Monitor('Custom Toggles Example')
 
 # add a toggle button that quits the simulation
 quit_toggle = mon.add_toggle(desc='Quit simulation')
 
@@ -128,15 +128,15 @@
 
 ### Loading Monitor data
 Finally, another cool feature of the Monitor class, is that all the data stored in 
 an output directory, can later be loaded into a Monitor object. This way, a simulation 
 that's been terminated can be resumed, and the data will keep streaming to the same place:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 mon = Monitor('Example Monitor')
 mon.load_from_dir()  # this loads all the data from the 'Example Monitor' output directory
 
 # now all data has been loaded back to the Monitor
 print(len(mon.trackers))  # a list of all trackers
 mon.plot(mon.trackers[0])  # same data can be plotted
```

### Comparing `simple-simon-0.0.3/setup.py` & `simple-simon-0.0.5/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="simple-simon",                           # This is the name of the package
-    version="0.0.3",                               # The initial release version
+    version="0.0.5",                               # The initial release version
     author="Roie Zemel",                           # Full name of the author
     description="A simple simulation monitor",
     long_description=long_description,             # Long description read from the the readme file
     long_description_content_type="text/markdown",
     packages=setuptools.find_packages(),           # List of all python modules to be installed
     classifiers=[
         "Programming Language :: Python :: 3",
```

### Comparing `simple-simon-0.0.3/simon/simon.py` & `simple-simon-0.0.5/simon/simon.py`

 * *Files identical despite different names*

### Comparing `simple-simon-0.0.3/simon/simple_simon.egg-info/PKG-INFO` & `simple-simon-0.0.5/simon/simple_simon.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-simon
-Version: 0.0.3
+Version: 0.0.5
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -35,15 +35,15 @@
 pip install simple-simon
 ```
 
 ## Usage
 Here's a quick example of the `Monitor` class used to track a moving object simulation:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 # create Monitor - this already opens an output directory and a toggle-buttons control window
 mon = Monitor('Example Monitor')
 
 # add a new 'tracker' to track variables
 tr = mon.tracker('time', 'velocity')
 
@@ -112,15 +112,15 @@
 ```
 
 ### About toggles
 The 'Toggles' window is opened from the moment a Monitor is created and until `finalize()` is called.
 Some toggles are added by default. Custom toggles can be added in a very simple way:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 # after this, the toggles window is opened
 mon = Monitor('Custom Toggles Example')
 
 # add a toggle button that quits the simulation
 quit_toggle = mon.add_toggle(desc='Quit simulation')
 
@@ -139,15 +139,15 @@
 
 ### Loading Monitor data
 Finally, another cool feature of the Monitor class, is that all the data stored in 
 an output directory, can later be loaded into a Monitor object. This way, a simulation 
 that's been terminated can be resumed, and the data will keep streaming to the same place:
 
 ```python
-from simon.simon import Monitor
+from simon import Monitor
 
 mon = Monitor('Example Monitor')
 mon.load_from_dir()  # this loads all the data from the 'Example Monitor' output directory
 
 # now all data has been loaded back to the Monitor
 print(len(mon.trackers))  # a list of all trackers
 mon.plot(mon.trackers[0])  # same data can be plotted
```

