# Comparing `tmp/simple-simon-0.0.2.tar.gz` & `tmp/simple-simon-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simple-simon-0.0.2.tar", last modified: Sat May 13 14:28:58 2023, max compression
+gzip compressed data, was "simple-simon-0.0.3.tar", last modified: Sat May 13 14:47:18 2023, max compression
```

## Comparing `simple-simon-0.0.2.tar` & `simple-simon-0.0.3.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 14:28:58.910947 simple-simon-0.0.2/
--rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simple-simon-0.0.2/LICENSE
--rw-rw-rw-   0        0        0     5856 2023-05-13 14:28:58.910947 simple-simon-0.0.2/PKG-INFO
--rw-rw-rw-   0        0        0     5552 2023-05-13 14:25:47.000000 simple-simon-0.0.2/README.md
--rw-rw-rw-   0        0        0       42 2023-05-13 14:28:58.910947 simple-simon-0.0.2/setup.cfg
--rw-rw-rw-   0        0        0     1239 2023-05-13 14:28:35.000000 simple-simon-0.0.2/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:28:58.910947 simple-simon-0.0.2/simon/
--rw-rw-rw-   0        0        0    29618 2023-05-13 14:07:05.000000 simple-simon-0.0.2/simon/simon.py
-drwxrwxrwx   0        0        0        0 2023-05-13 14:28:58.910947 simple-simon-0.0.2/simon/simple_simon.egg-info/
--rw-rw-rw-   0        0        0     5856 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      250 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       11 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2023-05-13 14:28:58.000000 simple-simon-0.0.2/simon/simple_simon.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 14:47:18.476905 simple-simon-0.0.3/
+-rw-rw-rw-   0        0        0     1086 2023-05-13 12:49:09.000000 simple-simon-0.0.3/LICENSE
+-rw-rw-rw-   0        0        0     5856 2023-05-13 14:47:18.476905 simple-simon-0.0.3/PKG-INFO
+-rw-rw-rw-   0        0        0     5552 2023-05-13 14:25:47.000000 simple-simon-0.0.3/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:47:18.476905 simple-simon-0.0.3/setup.cfg
+-rw-rw-rw-   0        0        0     1239 2023-05-13 14:47:15.000000 simple-simon-0.0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:47:18.461284 simple-simon-0.0.3/simon/
+-rw-rw-rw-   0        0        0    29858 2023-05-13 14:45:40.000000 simple-simon-0.0.3/simon/simon.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:47:18.476905 simple-simon-0.0.3/simon/simple_simon.egg-info/
+-rw-rw-rw-   0        0        0     5856 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      250 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        6 2023-05-13 14:47:18.000000 simple-simon-0.0.3/simon/simple_simon.egg-info/top_level.txt
```

### Comparing `simple-simon-0.0.2/LICENSE` & `simple-simon-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `simple-simon-0.0.2/PKG-INFO` & `simple-simon-0.0.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-simon
-Version: 0.0.2
+Version: 0.0.3
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `simple-simon-0.0.2/README.md` & `simple-simon-0.0.3/README.md`

 * *Files identical despite different names*

### Comparing `simple-simon-0.0.2/setup.py` & `simple-simon-0.0.3/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="simple-simon",                           # This is the name of the package
-    version="0.0.2",                               # The initial release version
+    version="0.0.3",                               # The initial release version
     author="Roie Zemel",                           # Full name of the author
     description="A simple simulation monitor",
     long_description=long_description,             # Long description read from the the readme file
     long_description_content_type="text/markdown",
     packages=setuptools.find_packages(),           # List of all python modules to be installed
     classifiers=[
         "Programming Language :: Python :: 3",
```

### Comparing `simple-simon-0.0.2/simon/simon.py` & `simple-simon-0.0.3/simon/simon.py`

 * *Files 1% similar despite different names*

```diff
@@ -99,19 +99,23 @@
 
     def plot(self, *args):
         """
         Plot all trackers or groups of trackers in a single figure.
         :param args: either titles, Tracker objects, or iterables of Tracker objects.
         :return: a matplotlib figure, only if return_figure is True.
         """
+        # save current backend
+        backend = matplotlib.get_backend()
+        matplotlib.use('TkAgg')
         if len(args) > 9:  # if more than 9 plots, divide into multiple figures
             _monitor_plot(self, *args[:9])
             self.plot(*args[9:])
         else:
             _monitor_plot(self, *args)
+        matplotlib.use(backend)
 
     def open_live_view(self, update_rate=2):
         """
         Open a live view of the monitor in a different process.
         :param update_rate: how many graph updates to perform in a second.
         """
         # make self less recursive by removing monitor
@@ -443,14 +447,16 @@
     This is the live view process.
     It creates and updates the live view figure.
     :param monitor: a monitor clone object (pickled and un-pickled).
     :param data_q: a data queue to send data to the process.
     :param update_rate: how many updates per second.
     """
     plt.ion()
+    backend = matplotlib.get_backend()
+    matplotlib.use('TkAgg')
 
     figure = None
     active = True
 
     # create an id_to_tracker dictionary
     id_to_tracker = dict()
     for trackers in monitor.titled_trackers.values():
@@ -496,14 +502,15 @@
             figure.canvas.draw()
             figure.canvas.flush_events()
             _custom_pause_live_view(10 ** -36)
 
         # wait for next update
         time.sleep(1 / update_rate)
 
+    matplotlib.use(backend)
     plt.ioff()
 
 
 def _custom_pause_live_view(interval):
     backend = plt.rcParams['backend']
     if backend in matplotlib.rcsetup.interactive_bk:
         fig_manager = matplotlib._pylab_helpers.Gcf.get_active()
```

### Comparing `simple-simon-0.0.2/simon/simple_simon.egg-info/PKG-INFO` & `simple-simon-0.0.3/simon/simple_simon.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simple-simon
-Version: 0.0.2
+Version: 0.0.3
 Summary: A simple simulation monitor
 Author: Roie Zemel
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

