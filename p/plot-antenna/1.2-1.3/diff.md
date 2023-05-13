# Comparing `tmp/plot-antenna-1.2.tar.gz` & `tmp/plot-antenna-1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "plot-antenna-1.2.tar", last modified: Fri May  5 19:04:30 2023, max compression
+gzip compressed data, was "plot-antenna-1.3.tar", last modified: Sat May 13 14:56:25 2023, max compression
```

## Comparing `plot-antenna-1.2.tar` & `plot-antenna-1.3.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-05 19:04:30.617696 plot-antenna-1.2/
--rw-r--r--   0 ralf      (1000) priv      (1011)     9911 2023-05-05 19:04:30.613696 plot-antenna-1.2/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)     7927 2023-05-05 19:01:31.000000 plot-antenna-1.2/README.rst
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-05 19:04:30.585696 plot-antenna-1.2/plot_antenna/
--rw-r--r--   0 ralf      (1000) priv      (1011)       14 2023-05-05 19:03:56.000000 plot-antenna-1.2/plot_antenna/Version.py
--rw-r--r--   0 ralf      (1000) priv      (1011)        0 2022-09-11 10:43:22.000000 plot-antenna-1.2/plot_antenna/__init__.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    48197 2023-05-05 18:55:35.000000 plot-antenna-1.2/plot_antenna/plot_antenna.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-05 19:04:30.605696 plot-antenna-1.2/plot_antenna.egg-info/
--rw-r--r--   0 ralf      (1000) priv      (1011)     9911 2023-05-05 19:04:30.000000 plot-antenna-1.2/plot_antenna.egg-info/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)      333 2023-05-05 19:04:30.000000 plot-antenna-1.2/plot_antenna.egg-info/SOURCES.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-05-05 19:04:30.000000 plot-antenna-1.2/plot_antenna.egg-info/dependency_links.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       65 2023-05-05 19:04:30.000000 plot-antenna-1.2/plot_antenna.egg-info/entry_points.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       17 2023-05-05 19:04:30.000000 plot-antenna-1.2/plot_antenna.egg-info/requires.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       13 2023-05-05 19:04:30.000000 plot-antenna-1.2/plot_antenna.egg-info/top_level.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-05-05 19:04:30.617696 plot-antenna-1.2/setup.cfg
--rw-r--r--   0 ralf      (1000) priv      (1011)     2716 2022-09-13 14:27:54.000000 plot-antenna-1.2/setup.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-05 19:04:30.609696 plot-antenna-1.2/test/
--rw-r--r--   0 ralf      (1000) priv      (1011)     7225 2022-09-13 13:39:50.000000 plot-antenna-1.2/test/test_plot.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-13 14:56:25.095480 plot-antenna-1.3/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    10183 2023-05-13 14:56:25.091480 plot-antenna-1.3/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)     8151 2023-05-13 14:54:56.000000 plot-antenna-1.3/README.rst
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-13 14:56:25.063480 plot-antenna-1.3/plot_antenna/
+-rw-r--r--   0 ralf      (1000) priv      (1011)       14 2023-05-13 14:55:53.000000 plot-antenna-1.3/plot_antenna/Version.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)        0 2022-09-11 10:43:22.000000 plot-antenna-1.3/plot_antenna/__init__.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    48877 2023-05-09 18:37:00.000000 plot-antenna-1.3/plot_antenna/plot_antenna.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-13 14:56:25.087480 plot-antenna-1.3/plot_antenna.egg-info/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    10183 2023-05-13 14:56:24.000000 plot-antenna-1.3/plot_antenna.egg-info/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)      333 2023-05-13 14:56:25.000000 plot-antenna-1.3/plot_antenna.egg-info/SOURCES.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-05-13 14:56:24.000000 plot-antenna-1.3/plot_antenna.egg-info/dependency_links.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       65 2023-05-13 14:56:24.000000 plot-antenna-1.3/plot_antenna.egg-info/entry_points.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       17 2023-05-13 14:56:24.000000 plot-antenna-1.3/plot_antenna.egg-info/requires.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       13 2023-05-13 14:56:24.000000 plot-antenna-1.3/plot_antenna.egg-info/top_level.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-05-13 14:56:25.095480 plot-antenna-1.3/setup.cfg
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2716 2022-09-13 14:27:54.000000 plot-antenna-1.3/setup.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-13 14:56:25.087480 plot-antenna-1.3/test/
+-rw-r--r--   0 ralf      (1000) priv      (1011)     7225 2022-09-13 13:39:50.000000 plot-antenna-1.3/test/test_plot.py
```

### Comparing `plot-antenna-1.2/PKG-INFO` & `plot-antenna-1.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: plot-antenna
-Version: 1.2
+Version: 1.3
 Summary: Antenna plotting program for plotting antenna simulation results
 Home-page: https://github.com/schlatterbeck/plot-antenna
 Author: Ralf Schlatterbeck
 Author-email: rsc@runtux.com
 License: MIT License
 Description: Antenna Plotting Program
         ========================
@@ -153,14 +153,20 @@
         .. _matplotlib: https://matplotlib.org/
         .. _plotly: https://github.com/plotly/plotly.py
         .. _pandas: https://pandas.pydata.org/
         
         Release Notes
         -------------
         
+        v1.3: Add a reset button to plotly polar plots
+        
+        - The polar plots, when zoomed in, could only be reset to the unzoomed
+          view with a double-click. All other plots do have a reset button, add
+          one for the polar plots, too.
+        
         v1.2: Allow specification of title (legend) font size in plotly version
         
         - For some application (e.g. when using the plotly graphics inside a
           html iframe) the title (or we may want to call it legend) of the
           graphics may collide with the graphics itself. We can now specify the
           font size with ``--title-font-size``. This option currently works only
           with plotly graphics.
```

### Comparing `plot-antenna-1.2/README.rst` & `plot-antenna-1.3/README.rst`

 * *Files 2% similar despite different names*

```diff
@@ -145,14 +145,20 @@
 .. _matplotlib: https://matplotlib.org/
 .. _plotly: https://github.com/plotly/plotly.py
 .. _pandas: https://pandas.pydata.org/
 
 Release Notes
 -------------
 
+v1.3: Add a reset button to plotly polar plots
+
+- The polar plots, when zoomed in, could only be reset to the unzoomed
+  view with a double-click. All other plots do have a reset button, add
+  one for the polar plots, too.
+
 v1.2: Allow specification of title (legend) font size in plotly version
 
 - For some application (e.g. when using the plotly graphics inside a
   html iframe) the title (or we may want to call it legend) of the
   graphics may collide with the graphics itself. We can now specify the
   font size with ``--title-font-size``. This option currently works only
   with plotly graphics.
```

### Comparing `plot-antenna-1.2/plot_antenna/plot_antenna.py` & `plot-antenna-1.3/plot_antenna/plot_antenna.py`

 * *Files 1% similar despite different names*

```diff
@@ -775,14 +775,31 @@
             or getattr (self.args, 'show_in_browser', None)
             ):
             self.polarplot_plotly (name)
         else:
             self.polarplot_matplotlib (name)
     # end def polarplot
 
+    plotly_polar_script = """
+            var myPlot = document.getElementById('{plot_id}');
+            Plotly.relayout (myPlot,
+                {'modebar':
+                    { 'add' :
+                        [   { 'name'  : 'Reset'
+                            , 'icon'  : Plotly.Icons.home
+                            , 'click' : function (gd)
+                              { Plotly.relayout
+                                (gd, {'polar.radialaxis.range': [0,1]});
+                              }
+                            }
+                        ]
+                    }
+                });
+            """
+
     def polarplot_plotly (self, name):
         fig = self.plotly_fig
         nm  = self.angle_name
         df = dict \
             ( r       = self.polargains
             , theta   = (self.angles / np.pi * 180) % 360
             , name    = "f=%.3f MHz" % self.frequency
@@ -827,15 +844,15 @@
 #                    , x         = 0.5
 #                    , y         = 1.1
 #                    , showarrow = False
 #                    , align     = 'center'
 #                    , text      = self.labels [1]
 #                    , font      = dict (size = 18)
 #                    )
-            self.show_plotly (fig, name)
+            self.show_plotly (fig, name, script = self.plotly_polar_script)
     # end def polarplot_plotly
 
     def polarplot_matplotlib (self, name):
         if name not in self.gui_objects:
             self.gui_objects [name] = {}
         ax = self.axes [name]
         ax.set_rmax (1)
@@ -1244,15 +1261,16 @@
     cmd.add_argument \
         ( '--plot-vswr', '--swr', '--vswr', '--plot-swr'
         , help    = 'Plot voltage standing wave ratio (VSWR)'
         , action  = 'store_true'
         )
     cmd.add_argument \
         ( '--title-font-size'
-        , help    = 'Title/legend font size (currently only used in plotly)'
+        , help    = 'Title/legend font size in pt '
+                    '(currently only used in plotly)'
         , type    = int
         )
     cmd.add_argument \
         ( '--wireframe'
         , help    = 'Show 3d plot as a wireframe (not solid)'
         , action  = 'store_true'
         )
```

### Comparing `plot-antenna-1.2/plot_antenna.egg-info/PKG-INFO` & `plot-antenna-1.3/plot_antenna.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: plot-antenna
-Version: 1.2
+Version: 1.3
 Summary: Antenna plotting program for plotting antenna simulation results
 Home-page: https://github.com/schlatterbeck/plot-antenna
 Author: Ralf Schlatterbeck
 Author-email: rsc@runtux.com
 License: MIT License
 Description: Antenna Plotting Program
         ========================
@@ -153,14 +153,20 @@
         .. _matplotlib: https://matplotlib.org/
         .. _plotly: https://github.com/plotly/plotly.py
         .. _pandas: https://pandas.pydata.org/
         
         Release Notes
         -------------
         
+        v1.3: Add a reset button to plotly polar plots
+        
+        - The polar plots, when zoomed in, could only be reset to the unzoomed
+          view with a double-click. All other plots do have a reset button, add
+          one for the polar plots, too.
+        
         v1.2: Allow specification of title (legend) font size in plotly version
         
         - For some application (e.g. when using the plotly graphics inside a
           html iframe) the title (or we may want to call it legend) of the
           graphics may collide with the graphics itself. We can now specify the
           font size with ``--title-font-size``. This option currently works only
           with plotly graphics.
```

### Comparing `plot-antenna-1.2/setup.py` & `plot-antenna-1.3/setup.py`

 * *Files identical despite different names*

### Comparing `plot-antenna-1.2/test/test_plot.py` & `plot-antenna-1.3/test/test_plot.py`

 * *Files identical despite different names*

