# Comparing `tmp/carto_reader-0.0.8.tar.gz` & `tmp/carto_reader-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/Users/josselin.duchateau/Dropbox/OngoingProjects/CartoReader/dist/.tmp-iapjjsqc/carto_reader-0.0.8.tar", last modified: Wed May  3 12:48:58 2023, max compression
+gzip compressed data, was "/Users/josselin.duchateau/Dropbox/OngoingProjects/CartoReader/dist/.tmp-36zqyw7k/carto_reader-0.0.9.tar", last modified: Sat May 13 19:06:46 2023, max compression
```

## Comparing `carto_reader-0.0.8.tar` & `carto_reader-0.0.9.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 josselin.duchateau (1149608237) 1632634153        0 2023-05-03 12:48:58.000000 carto_reader-0.0.8/
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153    35148 2021-09-10 16:33:24.000000 carto_reader-0.0.8/LICENSE
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     4097 2023-05-03 12:48:58.000000 carto_reader-0.0.8/PKG-INFO
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     3650 2021-09-15 10:10:24.000000 carto_reader-0.0.8/README.md
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153      104 2021-09-10 16:28:39.000000 carto_reader-0.0.8/pyproject.toml
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153      637 2023-05-03 12:48:58.000000 carto_reader-0.0.8/setup.cfg
-drwxr-xr-x   0 josselin.duchateau (1149608237) 1632634153        0 2023-05-03 12:48:58.000000 carto_reader-0.0.8/src/
-drwxr-xr-x   0 josselin.duchateau (1149608237) 1632634153        0 2023-05-03 12:48:58.000000 carto_reader-0.0.8/src/carto_reader/
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153       86 2021-09-16 13:43:05.000000 carto_reader-0.0.8/src/carto_reader/__init__.py
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     1806 2021-12-06 08:58:29.000000 carto_reader-0.0.8/src/carto_reader/archive.py
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     9411 2023-01-12 20:34:53.000000 carto_reader-0.0.8/src/carto_reader/carto_data.py
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     8131 2023-01-12 20:35:52.000000 carto_reader-0.0.8/src/carto_reader/mesh.py
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     4895 2021-09-17 20:00:27.000000 carto_reader-0.0.8/src/carto_reader/old.py
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     9271 2023-01-12 20:31:19.000000 carto_reader-0.0.8/src/carto_reader/points.py
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     4299 2023-01-12 20:32:01.000000 carto_reader-0.0.8/src/carto_reader/signals.py
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     2586 2021-12-07 10:08:06.000000 carto_reader-0.0.8/src/carto_reader/utils.py
-drwxr-xr-x   0 josselin.duchateau (1149608237) 1632634153        0 2023-05-03 12:48:58.000000 carto_reader-0.0.8/src/carto_reader.egg-info/
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     4097 2023-05-03 12:48:58.000000 carto_reader-0.0.8/src/carto_reader.egg-info/PKG-INFO
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153      459 2023-05-03 12:48:58.000000 carto_reader-0.0.8/src/carto_reader.egg-info/SOURCES.txt
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153        1 2023-05-03 12:48:58.000000 carto_reader-0.0.8/src/carto_reader.egg-info/dependency_links.txt
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153       37 2023-05-03 12:48:58.000000 carto_reader-0.0.8/src/carto_reader.egg-info/requires.txt
--rw-r--r--   0 josselin.duchateau (1149608237) 1632634153       13 2023-05-03 12:48:58.000000 carto_reader-0.0.8/src/carto_reader.egg-info/top_level.txt
+drwxr-xr-x   0 josselin.duchateau (1149608237) 1632634153        0 2023-05-13 19:06:46.000000 carto_reader-0.0.9/
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153    35148 2021-09-10 16:33:24.000000 carto_reader-0.0.9/LICENSE
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     4097 2023-05-13 19:06:46.000000 carto_reader-0.0.9/PKG-INFO
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     3650 2021-09-15 10:10:24.000000 carto_reader-0.0.9/README.md
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153      104 2021-09-10 16:28:39.000000 carto_reader-0.0.9/pyproject.toml
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153      637 2023-05-13 19:06:46.000000 carto_reader-0.0.9/setup.cfg
+drwxr-xr-x   0 josselin.duchateau (1149608237) 1632634153        0 2023-05-13 19:06:46.000000 carto_reader-0.0.9/src/
+drwxr-xr-x   0 josselin.duchateau (1149608237) 1632634153        0 2023-05-13 19:06:46.000000 carto_reader-0.0.9/src/carto_reader/
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153       86 2021-09-16 13:43:05.000000 carto_reader-0.0.9/src/carto_reader/__init__.py
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     1806 2021-12-06 08:58:29.000000 carto_reader-0.0.9/src/carto_reader/archive.py
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     9411 2023-01-12 20:34:53.000000 carto_reader-0.0.9/src/carto_reader/carto_data.py
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     9484 2023-05-13 19:05:23.000000 carto_reader-0.0.9/src/carto_reader/mesh.py
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     4895 2021-09-17 20:00:27.000000 carto_reader-0.0.9/src/carto_reader/old.py
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     9271 2023-01-12 20:31:19.000000 carto_reader-0.0.9/src/carto_reader/points.py
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     4299 2023-01-12 20:32:01.000000 carto_reader-0.0.9/src/carto_reader/signals.py
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     2586 2021-12-07 10:08:06.000000 carto_reader-0.0.9/src/carto_reader/utils.py
+drwxr-xr-x   0 josselin.duchateau (1149608237) 1632634153        0 2023-05-13 19:06:46.000000 carto_reader-0.0.9/src/carto_reader.egg-info/
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153     4097 2023-05-13 19:06:46.000000 carto_reader-0.0.9/src/carto_reader.egg-info/PKG-INFO
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153      459 2023-05-13 19:06:46.000000 carto_reader-0.0.9/src/carto_reader.egg-info/SOURCES.txt
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153        1 2023-05-13 19:06:46.000000 carto_reader-0.0.9/src/carto_reader.egg-info/dependency_links.txt
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153       37 2023-05-13 19:06:46.000000 carto_reader-0.0.9/src/carto_reader.egg-info/requires.txt
+-rw-r--r--   0 josselin.duchateau (1149608237) 1632634153       13 2023-05-13 19:06:46.000000 carto_reader-0.0.9/src/carto_reader.egg-info/top_level.txt
```

### Comparing `carto_reader-0.0.8/LICENSE` & `carto_reader-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `carto_reader-0.0.8/PKG-INFO` & `carto_reader-0.0.9/src/carto_reader.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: carto_reader
-Version: 0.0.8
+Name: carto-reader
+Version: 0.0.9
 Summary: Package to read Carto datasets
 Author: Josselin Duchateau
 Author-email: josselin.duchateau@ihu-liryc.fr
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
```

### Comparing `carto_reader-0.0.8/README.md` & `carto_reader-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `carto_reader-0.0.8/setup.cfg` & `carto_reader-0.0.9/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = carto_reader
-version = 0.0.8
+version = 0.0.9
 author = Josselin Duchateau
 author_email = josselin.duchateau@ihu-liryc.fr
 description = Package to read Carto datasets
 long_description = file: README.md
 long_description_content_type = text/markdown
 classifiers = 
 	Programming Language :: Python :: 3
```

### Comparing `carto_reader-0.0.8/src/carto_reader/archive.py` & `carto_reader-0.0.9/src/carto_reader/archive.py`

 * *Files identical despite different names*

### Comparing `carto_reader-0.0.8/src/carto_reader/carto_data.py` & `carto_reader-0.0.9/src/carto_reader/carto_data.py`

 * *Files identical despite different names*

### Comparing `carto_reader-0.0.8/src/carto_reader/mesh.py` & `carto_reader-0.0.9/src/carto_reader/mesh.py`

 * *Files 12% similar despite different names*

```diff
@@ -154,20 +154,20 @@
                 map_name = f'UNNAMED {i_map}'
 
         self._maps[map_name] = map
 
     @property
     def num_v(self):
         """ Number of vertices """
-        return self.v.shape[0]
+        return len(self.v)
 
     @property
     def num_t(self):
         """ Number of triangles (simplexes) """
-        return self.t.shape[0]
+        return len(self.t)
 
     def __len__(self):
         return self._maps.__len__()
 
     def __getitem__(self, item):
         if isinstance(item, int):
             item = list(self.keys())[item]
@@ -191,47 +191,84 @@
 
     def __iter__(self):
         return self._maps.__iter__()
 
     def __repr__(self):
         return f'<Mesh ({self.num_v} x {self.num_t}), {len(self)} Maps>'
 
-    def pv_mesh(self):
+    def pv_mesh(self, cutouts=True, all_maps=False):
+        """
+        Get a pyvista mesh version of the current Mesh object.
+        Requires a working installation of pyvista.
+        :param cutouts: remove the cutouts
+        :param all_maps: add all maps as scalar fields to the object
+        :return:
+        """
         pv = load_pv()
-        tris = np.hstack(np.concatenate((3 * np.ones((self.num_t, 1), dtype=int), self.t), 1))
-        poly_data = pv.PolyData(self.v, tris)
+        t = self.t
+        if cutouts:
+            try:
+                t = self.t[self['GroupID'] == 0]
+            except KeyError:
+                pass
+        poly_data = pv.PolyData(self.v, np.hstack((np.full((len(t), 1), 3, int), t)))
+        if all_maps:
+            for map_name, map_data in self.items():
+                if cutouts and len(map_data) == self.num_t:
+                    try:
+                        map_data = map_data[self['GroupID'] == 0]
+                    except KeyError:
+                        pass
+                poly_data[map_name] = map_data
+
         return poly_data
 
-    def plot(self, _map=None):
-        """ Plot the mesh """
+    def plot(self, _map=None, cutouts=True):
+        """ Plot the mesh
+        :param _map: The map to plot (optional) - can be either a map name/index or a numpy array
+        :param cutouts: remove cutouts (default is True) or display the full mesh
+        :return:
+        """
         pv = load_pv()
-        poly_data = self.pv_mesh()
+        poly_data = self.pv_mesh(cutouts)
         plotter = pv.Plotter()
         i = -1
         cmap, clim = None, None
         if _map is None:
             _map = np.zeros((self.num_v,))
         elif isinstance(_map, (str, int)):
             if isinstance(map, int):
                 _map = list(self.keys())[_map]
             cmap, clim = DEFAULT_COLORMAPS.get(_map.lower(), (None, None))
             _map = self[_map]
 
+        if cutouts and len(_map) == self.num_t:
+            try:
+                _map = _map[self['GroupID'] == 0]
+            except KeyError:
+                pass
+
         curr_mesh = plotter.add_mesh(poly_data, scalars=_map, cmap=cmap, clim=clim)
         curr_text = plotter.add_text('')
 
         def change_map(increment):
             """ Callback function to change map """
             def plot_map():
                 nonlocal i, curr_text, curr_mesh
                 i = (i + increment + len(self)) % len(self)
                 map_name = list(self.keys())[i]
                 cmap, clim = DEFAULT_COLORMAPS.get(map_name.lower(), (None, None))
                 plotter.remove_actor(curr_mesh)
-                curr_mesh = plotter.add_mesh(poly_data, scalars=self[i], cmap=cmap, clim=clim)
+                _map = self[i]
+                if cutouts and len(_map) == self.num_t:
+                    try:
+                        _map = _map[self['GroupID'] == 0]
+                    except KeyError:
+                        pass
+                curr_mesh = plotter.add_mesh(poly_data, scalars=_map, cmap=cmap, clim=clim)
                 plotter.remove_actor(curr_text)
                 curr_text = plotter.add_text(map_name)
             return plot_map
 
         plotter.add_key_event('Left', change_map(-1))
         plotter.add_key_event('Right', change_map(1))
         plotter.show()
```

### Comparing `carto_reader-0.0.8/src/carto_reader/old.py` & `carto_reader-0.0.9/src/carto_reader/old.py`

 * *Files identical despite different names*

### Comparing `carto_reader-0.0.8/src/carto_reader/points.py` & `carto_reader-0.0.9/src/carto_reader/points.py`

 * *Files identical despite different names*

### Comparing `carto_reader-0.0.8/src/carto_reader/signals.py` & `carto_reader-0.0.9/src/carto_reader/signals.py`

 * *Files identical despite different names*

### Comparing `carto_reader-0.0.8/src/carto_reader/utils.py` & `carto_reader-0.0.9/src/carto_reader/utils.py`

 * *Files identical despite different names*

### Comparing `carto_reader-0.0.8/src/carto_reader.egg-info/PKG-INFO` & `carto_reader-0.0.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: carto-reader
-Version: 0.0.8
+Name: carto_reader
+Version: 0.0.9
 Summary: Package to read Carto datasets
 Author: Josselin Duchateau
 Author-email: josselin.duchateau@ihu-liryc.fr
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
```

