# Comparing `tmp/reixs-0.5.8.tar.gz` & `tmp/reixs-0.5.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "reixs-0.5.8.tar", last modified: Thu May 11 18:34:55 2023, max compression
+gzip compressed data, was "reixs-0.5.9.tar", last modified: Fri May 12 22:16:50 2023, max compression
```

## Comparing `reixs-0.5.8.tar` & `reixs-0.5.9.tar`

### file list

```diff
@@ -1,31 +1,31 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 18:34:55.929800 reixs-0.5.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1077 2023-05-11 18:34:40.000000 reixs-0.5.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    11128 2023-05-11 18:34:55.929800 reixs-0.5.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    10479 2023-05-11 18:34:40.000000 reixs-0.5.8/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-11 18:34:40.000000 reixs-0.5.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      856 2023-05-11 18:34:55.929800 reixs-0.5.8/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 18:34:55.925800 reixs-0.5.8/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 18:34:55.929800 reixs-0.5.8/src/reixs/
--rw-r--r--   0 runner    (1001) docker     (123)    59604 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/LoadData.py
--rw-r--r--   0 runner    (1001) docker     (123)    33022 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/ReadData.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15932 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/add_subtract.py
--rw-r--r--   0 runner    (1001) docker     (123)     2497 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/beamline_info.py
--rw-r--r--   0 runner    (1001) docker     (123)      101 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/edges.py
--rw-r--r--   0 runner    (1001) docker     (123)     3543 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/mca.py
--rw-r--r--   0 runner    (1001) docker     (123)     7352 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/mesh.py
--rw-r--r--   0 runner    (1001) docker     (123)     3233 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     5113 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/rixs_readutil.py
--rw-r--r--   0 runner    (1001) docker     (123)     3266 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/rsxs_mcp.py
--rw-r--r--   0 runner    (1001) docker     (123)     5891 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/rsxs_readutil.py
--rw-r--r--   0 runner    (1001) docker     (123)    11929 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/sca.py
--rw-r--r--   0 runner    (1001) docker     (123)     8514 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/simplemath.py
--rw-r--r--   0 runner    (1001) docker     (123)     1702 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/spec_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     6784 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/util.py
--rw-r--r--   0 runner    (1001) docker     (123)     4795 2023-05-11 18:34:40.000000 reixs-0.5.8/src/reixs/xeol.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 18:34:55.929800 reixs-0.5.8/src/reixs.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    11128 2023-05-11 18:34:55.000000 reixs-0.5.8/src/reixs.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      577 2023-05-11 18:34:55.000000 reixs-0.5.8/src/reixs.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 18:34:55.000000 reixs-0.5.8/src/reixs.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       66 2023-05-11 18:34:55.000000 reixs-0.5.8/src/reixs.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-11 18:34:55.000000 reixs-0.5.8/src/reixs.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:16:50.313173 reixs-0.5.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1077 2023-05-12 22:16:39.000000 reixs-0.5.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    11128 2023-05-12 22:16:50.313173 reixs-0.5.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    10479 2023-05-12 22:16:39.000000 reixs-0.5.9/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-12 22:16:39.000000 reixs-0.5.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      856 2023-05-12 22:16:50.313173 reixs-0.5.9/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:16:50.309173 reixs-0.5.9/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:16:50.313173 reixs-0.5.9/src/reixs/
+-rw-r--r--   0 runner    (1001) docker     (123)    57479 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/LoadData.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33022 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/ReadData.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15932 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/add_subtract.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2497 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/beamline_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)      101 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/edges.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3543 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/mca.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7352 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/mesh.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3233 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5113 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/rixs_readutil.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3266 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/rsxs_mcp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5891 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/rsxs_readutil.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11929 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/sca.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8514 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/simplemath.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1702 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/spec_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6784 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4795 2023-05-12 22:16:39.000000 reixs-0.5.9/src/reixs/xeol.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:16:50.313173 reixs-0.5.9/src/reixs.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    11128 2023-05-12 22:16:50.000000 reixs-0.5.9/src/reixs.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      577 2023-05-12 22:16:50.000000 reixs-0.5.9/src/reixs.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:16:50.000000 reixs-0.5.9/src/reixs.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       66 2023-05-12 22:16:50.000000 reixs-0.5.9/src/reixs.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-12 22:16:50.000000 reixs-0.5.9/src/reixs.egg-info/top_level.txt
```

### Comparing `reixs-0.5.8/LICENSE` & `reixs-0.5.9/LICENSE`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/PKG-INFO` & `reixs-0.5.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: reixs
-Version: 0.5.8
+Version: 0.5.9
 Summary: Library to analyse, plot, and export data taken at the REIXS Beamline at the Canadian Light Source, Saskatoon, Canada.
 Home-page: https://github.com/pmb399/REIXSAnalysis
 Author: Patrick Braun
 Author-email: patrick.braun@usask.ca
 Project-URL: Bug Tracker, https://github.com/pmb399/REIXSAnalysis
 Project-URL: Beamline Information, https://reixs.lightsource.ca
 Classifier: Programming Language :: Python :: 3
```

### Comparing `reixs-0.5.8/README.md` & `reixs-0.5.9/README.md`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/setup.cfg` & `reixs-0.5.9/setup.cfg`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = reixs
-version = 0.5.8
+version = 0.5.9
 author = Patrick Braun
 author_email = patrick.braun@usask.ca
 description = Library to analyse, plot, and export data taken at the REIXS Beamline at the Canadian Light Source, Saskatoon, Canada.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/pmb399/REIXSAnalysis
 project_urls =
```

### Comparing `reixs-0.5.8/src/reixs/LoadData.py` & `reixs-0.5.9/src/reixs/LoadData.py`

 * *Files 3% similar despite different names*

```diff
@@ -738,15 +738,15 @@
         pos_y : float
         text : string
         **kwargs : dict, optional
             See bokeh manual for available options.
         """
         self.plot_labels.append([pos_x, pos_y, text, kwargs])
 
-    def plot(self, title=None, xlabel=None, ylabel=None, plot_height=600, plot_width=600):
+    def plot(self, title=None, kind='Image', xlabel=None, ylabel=None, plot_height=600, plot_width=600):
         """Plot all data assosciated with class instance/object."""
 
         # Iterate over the one (1) scan in object - this is for legacy reason and shall be removed in the future.
         for i, val in enumerate(self.data):
             for k, v in val.items():
 
                 # Create the figure
@@ -801,15 +801,15 @@
                         label = Label(
                             x=label_props[0], y=label_props[1], text=label_props[2], **label_props[3])
                         p.add_layout(label)
 
             if title != None:
                 p.title.text = str(title)
             else:
-                p.title.text = f'{self.detector[i]} Image for Scan {k}'
+                p.title.text = f'{self.detector[i]} {kind} for Scan {k}'
             if xlabel != None:
                 p.xaxis.axis_label = str(xlabel)
             else:
                 p.xaxis.axis_label = str(self.x_stream[i])
             if ylabel != None:
                 p.yaxis.axis_label = str(ylabel)
             else:
@@ -952,23 +952,31 @@
         y_stream = self.get_scale(detector)
 
         super().subtract(basedir, file, x_stream, y_stream, detector, *args, **kwargs)
 
 #########################################################################################
 
 
-class LoadMesh:
+class LoadMesh(Load2d):
     """Class to display (x,y,z) scatter data."""
 
     def __init__(self):
         self.data = list()
         self.x_stream = list()
         self.y_stream = list()
         self.z_stream = list()
         self.filename = list()
+        self.plot_lim_x = [":", ":"]
+        self.plot_lim_y = [":", ":"]
+        self.plot_vlines = list()
+        self.plot_hlines = list()
+        self.plot_labels = list()
+
+        # Use this so we can inherit from Load2d for plotting
+        self.detector = self.z_stream
 
     def load(self, basedir, file, x_stream, y_stream, z_stream, *args, **kwargs):
 
         # Set the defaults if not specified in **kwargs.
         kwargs.setdefault("norm", False)
         kwargs.setdefault("xoffset", None)
         kwargs.setdefault("xcoffset", None)
@@ -981,57 +989,24 @@
         self.data.append(loadMeshScans(basedir, file, x_stream,
                          y_stream, z_stream, *args, **kwargs))
         self.x_stream.append(x_stream)
         self.y_stream.append(y_stream)
         self.z_stream.append(z_stream)
         self.filename.append(file)
 
-    def plot(self, title=None, xlabel=None, ylabel=None, plot_height=600, plot_width=600):
-
-        for i, val in enumerate(self.data):
-            for k, v in val.items():
-
-                p = figure(height=plot_height, width=plot_width, tooltips=[("x", "$x"), ("y", "$y"), ("value", "@image")],
-                           tools="pan,wheel_zoom,box_zoom,reset,hover,crosshair,save")
-                p.x_range.range_padding = p.y_range.range_padding = 0
-
-                # Have the gridded data ready now from loader
-
-                # must give a vector of image data for image parameter
-                color_mapper = LinearColorMapper(palette="Viridis256",
-                                                 low=v.zmin,
-                                                 high=v.zmax)
-
-                p.image(image=[v.new_z], x=v.xmin, y=v.ymin, dw=v.xmax-v.xmin,
-                        dh=v.ymax-v.ymin, color_mapper=color_mapper, level="image")
-                p.grid.grid_line_width = 0.5
-
-                # Defining properties of color mapper
-                color_bar = ColorBar(color_mapper=color_mapper,
-                                     label_standoff=12,
-                                     location=(0, 0),
-                                     title='Counts')
-                p.add_layout(color_bar, 'right')
-
-                p.toolbar.logo = None
+    def add(self):
+        raise UserWarning("Functionality not yet implemented.")
+    
+    def subtract(self):
+        raise UserWarning("Functionality not yet implemented.")
+    
+    def plot(self, *args, **kwargs):
+        kwargs.setdefault('kind', "Histogram")
 
-                if title != None:
-                    p.title.text = str(title)
-                else:
-                    p.title.text = f'{self.z_stream[i]} Histogram for Scan {k}'
-                if xlabel != None:
-                    p.xaxis.axis_label = str(xlabel)
-                else:
-                    p.xaxis.axis_label = str(self.x_stream[i])
-                if ylabel != None:
-                    p.yaxis.axis_label = str(ylabel)
-                else:
-                    p.yaxis.axis_label = f"{self.y_stream[i]}"
-
-                show(p)
+        super().plot(*args, **kwargs)
 
     def get_data(self):
         f = io.StringIO()
         g = io.StringIO()
         for i, val in enumerate(self.data):
             for k, v in val.items():
                 # Have the gridded data ready now from loader
@@ -1041,18 +1016,18 @@
                 f.write("========================\n")
 
                 g.write("========================\n")
                 g.write(
                     f"F~{self.filename[i]}_S{v.scan}_{self.z_stream[i]}_{self.x_stream[i]}_{self.y_stream[i]}\n")
                 g.write("========================\n")
 
-                f.write("=== x-axis bins ===\n")
-                np.savetxt(f, v.new_x)
-                f.write("=== y-axis bins ===\n")
-                np.savetxt(f, v.new_y)
+                f.write("=== x-axis bin edges ===\n")
+                np.savetxt(f, v.xedge)
+                f.write("=== y-axis bin edges ===\n")
+                np.savetxt(f, v.yedge)
                 g.write("=== Histogram ===\n")
                 np.savetxt(g, v.new_z, fmt="%.9g")
         return f, g
 
     def export(self, filename):
 
         f, g, = self.get_data()
@@ -1063,38 +1038,14 @@
 
         with open(f"{filename}.txt_matrix", "a") as matrix:
             g.seek(0)
             shutil.copyfileobj(g, matrix)
 
         print(f"Successfully wrote Histogram data to {filename}.txt")
 
-    def exporter(self):
-        current_dir = os.path.dirname(os.path.realpath("__file__"))
-
-        self.exportfile = FileChooser(current_dir)
-        self.exportfile.use_dir_icons = True
-        #self.exportfile.filter_pattern = '*.txt'
-
-        button = widgets.Button(
-            description='Save data file',
-            disabled=False,
-            button_style='info',  # 'success', 'info', 'warning', 'danger' or ''
-            tooltip='Save data to file',
-            icon='save'  # (FontAwesome names without the `fa-` prefix)
-        )
-
-        button.on_click(self.exportWidgetStep)
-        display(self.exportfile, button)
-
-    def exportWidgetStep(self, my):
-        file = os.path.join(self.exportfile.selected_path,
-                            self.exportfile.selected_filename)
-        self.export(file)
-
-
 class MeshLoader(LoadMesh):
     pass
 
 #########################################################################################
 
 
 class ImageROILoader():
```

### Comparing `reixs-0.5.8/src/reixs/ReadData.py` & `reixs-0.5.9/src/reixs/ReadData.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/add_subtract.py` & `reixs-0.5.9/src/reixs/add_subtract.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/beamline_info.py` & `reixs-0.5.9/src/reixs/beamline_info.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/mca.py` & `reixs-0.5.9/src/reixs/mca.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/mesh.py` & `reixs-0.5.9/src/reixs/mesh.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/parser.py` & `reixs-0.5.9/src/reixs/parser.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/rixs_readutil.py` & `reixs-0.5.9/src/reixs/rixs_readutil.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/rsxs_mcp.py` & `reixs-0.5.9/src/reixs/rsxs_mcp.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/rsxs_readutil.py` & `reixs-0.5.9/src/reixs/rsxs_readutil.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/sca.py` & `reixs-0.5.9/src/reixs/sca.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/simplemath.py` & `reixs-0.5.9/src/reixs/simplemath.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/spec_config.py` & `reixs-0.5.9/src/reixs/spec_config.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/util.py` & `reixs-0.5.9/src/reixs/util.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs/xeol.py` & `reixs-0.5.9/src/reixs/xeol.py`

 * *Files identical despite different names*

### Comparing `reixs-0.5.8/src/reixs.egg-info/PKG-INFO` & `reixs-0.5.9/src/reixs.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: reixs
-Version: 0.5.8
+Version: 0.5.9
 Summary: Library to analyse, plot, and export data taken at the REIXS Beamline at the Canadian Light Source, Saskatoon, Canada.
 Home-page: https://github.com/pmb399/REIXSAnalysis
 Author: Patrick Braun
 Author-email: patrick.braun@usask.ca
 Project-URL: Bug Tracker, https://github.com/pmb399/REIXSAnalysis
 Project-URL: Beamline Information, https://reixs.lightsource.ca
 Classifier: Programming Language :: Python :: 3
```

### Comparing `reixs-0.5.8/src/reixs.egg-info/SOURCES.txt` & `reixs-0.5.9/src/reixs.egg-info/SOURCES.txt`

 * *Files identical despite different names*

