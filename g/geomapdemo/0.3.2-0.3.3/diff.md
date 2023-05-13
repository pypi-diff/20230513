# Comparing `tmp/geomapdemo-0.3.2.tar.gz` & `tmp/geomapdemo-0.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "geomapdemo-0.3.2.tar", last modified: Sun May  7 19:17:29 2023, max compression
+gzip compressed data, was "geomapdemo-0.3.3.tar", last modified: Sat May 13 01:52:06 2023, max compression
```

## Comparing `geomapdemo-0.3.2.tar` & `geomapdemo-0.3.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:17:29.477797 geomapdemo-0.3.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      122 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2222 2023-05-07 19:17:29.477797 geomapdemo-0.3.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1398 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:17:29.473797 geomapdemo-0.3.2/geomapdemo/
--rw-r--r--   0 runner    (1001) docker     (123)      159 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/geomapdemo/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4275 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/geomapdemo/chart.py
--rw-r--r--   0 runner    (1001) docker     (123)     8555 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/geomapdemo/foliumap.py
--rw-r--r--   0 runner    (1001) docker     (123)    15629 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/geomapdemo/geomapdemo.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-07 19:17:29.477797 geomapdemo-0.3.2/geomapdemo.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2222 2023-05-07 19:17:29.000000 geomapdemo-0.3.2/geomapdemo.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      358 2023-05-07 19:17:29.000000 geomapdemo-0.3.2/geomapdemo.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)       78 2023-05-07 19:17:29.000000 geomapdemo-0.3.2/geomapdemo.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-07 19:17:29.000000 geomapdemo-0.3.2/geomapdemo.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       77 2023-05-07 19:17:29.000000 geomapdemo-0.3.2/geomapdemo.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-07 19:17:29.000000 geomapdemo-0.3.2/geomapdemo.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       77 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-07 19:17:29.477797 geomapdemo-0.3.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1807 2023-05-07 19:17:19.000000 geomapdemo-0.3.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:52:06.511928 geomapdemo-0.3.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      122 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     2222 2023-05-13 01:52:06.511928 geomapdemo-0.3.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1398 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:52:06.507928 geomapdemo-0.3.3/geomapdemo/
+-rw-r--r--   0 runner    (1001) docker     (123)      159 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/geomapdemo/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7828 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/geomapdemo/chart.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8788 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/geomapdemo/foliumap.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17194 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/geomapdemo/geomapdemo.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 01:52:06.511928 geomapdemo-0.3.3/geomapdemo.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2222 2023-05-13 01:52:06.000000 geomapdemo-0.3.3/geomapdemo.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      358 2023-05-13 01:52:06.000000 geomapdemo-0.3.3/geomapdemo.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       78 2023-05-13 01:52:06.000000 geomapdemo-0.3.3/geomapdemo.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 01:52:06.000000 geomapdemo-0.3.3/geomapdemo.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       77 2023-05-13 01:52:06.000000 geomapdemo-0.3.3/geomapdemo.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-13 01:52:06.000000 geomapdemo-0.3.3/geomapdemo.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       77 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-13 01:52:06.511928 geomapdemo-0.3.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1807 2023-05-13 01:51:56.000000 geomapdemo-0.3.3/setup.py
```

### Comparing `geomapdemo-0.3.2/LICENSE` & `geomapdemo-0.3.3/LICENSE`

 * *Files identical despite different names*

### Comparing `geomapdemo-0.3.2/PKG-INFO` & `geomapdemo-0.3.3/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: geomapdemo
-Version: 0.3.2
+Version: 0.3.3
 Summary: A python package for interactive mapping.
 Home-page: https://github.com/zyang91/geomapdemo
 Author: Zhanchao Yang
 Author-email: zyang91@binghamton.edu
 License: MIT license
 Keywords: geomapdemo
 Classifier: Development Status :: 2 - Pre-Alpha
```

### Comparing `geomapdemo-0.3.2/README.md` & `geomapdemo-0.3.3/README.md`

 * *Files identical despite different names*

### Comparing `geomapdemo-0.3.2/geomapdemo/chart.py` & `geomapdemo-0.3.3/geomapdemo/chart.py`

 * *Files 23% similar despite different names*

```diff
@@ -9,89 +9,156 @@
     '''Set the aesthetic style of the plots.
     Args:
         style (str): darkgrid, darkgrid, dark, white, ticks
         kwargs: Additional parameters to control the aesthetics of the grid.'''
     sns.set_theme(style=style, **kwargs)
 
 def scatter_plot(data, x, y, hue= None, **kwargs):
-    '''Plot data and regression model fits across a FacetGrid.
+    '''Plot data and regression model fits across a FacetGrid. Used to plot a scatter chart
     Args:
         data (DataFrame): CSV file path or DataFrame object.
         x, y (str): Variables that specify positions on the x and y axes.
         hue (str): Variable in data to map plot aspects to different colors.
         kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
     '''
     if isinstance(data, str):
         df = pd.read_csv(data)
     else:
         df = data
     sns.catplot(data=df, x=x, y=y, hue=hue, **kwargs)
 
 def violin_plot(data, x, y, hue= None, **kwargs):
-    '''Plot data and regression model fits across a FacetGrid.
+    '''Plot data and regression model fits across a FacetGrid. Used to plot a violin chart
     Args:
         data (DataFrame): CSV file path or DataFrame object.
         x, y (str): Variables that specify positions on the x and y axes.
         hue (str): Variable in data to map plot aspects to different colors.
         kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
     '''
     if isinstance(data, str):
         df = pd.read_csv(data)
     else:
         df = data
     sns.violinplot(data=df, x=x, y=y, hue=hue, **kwargs)
 
 def violin_spilt(data, x, y, hue, spilt= True, **kwargs):
-    '''Plot data and regression model fits across a FacetGrid.
+    '''Plot data and regression model fits across a FacetGrid. Used to plot a spilt violin chart
     Args:
         data (DataFrame): CSV file path or DataFrame object.
         x, y (str): Variables that specify positions on the x and y axes.
         hue (str): Variable in data to map plot aspects to different colors.
         spilt (bool): Whether to draw half of a violin for each hue level or allow them to overlap.
         kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
     '''
     if isinstance(data, str):
         df = pd.read_csv(data)
     else:
         df = data
     sns.violinplot(data=df, x=x, y=y, hue=hue, split=spilt, **kwargs)
 
 def single_violin(data, variable, **kwargs):
-    '''Plot data and regression model fits across a FacetGrid.
+    '''Plot data and regression model fits across a FacetGrid. Used to plot a single violin chart
     Args:
         data (DataFrame): CSV file path or DataFrame object.
         variable (str): Variables that specify positions on the x and y axes.
         kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
     '''
     if isinstance(data, str):
         df = pd.read_csv(data)
     else:
         df = data
     sns.violinplot(x=df[variable], **kwargs)
 
 def box_plot(data, x, y, hue= None, **kwargs):
-    '''Plot data and regression model fits across a FacetGrid.
+    '''Plot data and regression model fits across a FacetGrid. Used to plot a box chart
     Args:
         data (DataFrame): CSV file path or DataFrame object.
         x, y (str): Variables that specify positions on the x and y axes.
         hue (str): Variable in data to map plot aspects to different colors.
         kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
     '''
     if isinstance(data, str):
         df = pd.read_csv(data)
     else:
         df = data
     sns.boxplot(data=df, x=x, y=y, hue=hue, **kwargs)
 
 def single_box_plot(data, variable, **kwargs):
-    '''Plot data and regression model fits across a FacetGrid.
+    '''Plot data and regression model fits across a FacetGrid. Used to plot a single box chart
     Aegs:
         data (DataFrame): CSV file path or DataFrame object.
         variable (str): Variables that specify positions on the x and y axes.
         kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
     '''
     if isinstance(data, str):
         df = pd.read_csv(data)
     else:
         df = data
     sns.boxplot(data=df,x=df[variable], **kwargs)
 
+def bar_plot(data, x, y, hue= None, **kwargs):
+    '''Plot data and regression model fits across a FacetGrid. Used to plot a bar chart 
+    Args:
+        data (DataFrame): CSV file path or DataFrame object.
+        x, y (str): Variables that specify positions on the x and y axes.
+        hue (str): Variable in data to map plot aspects to different colors.
+        kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
+    '''
+    if isinstance(data, str):
+        df = pd.read_csv(data)
+    else:
+        df = data
+    sns.barplot(data=df, x=x, y=y, hue=hue, **kwargs)
+
+def single_bar_plot(data, variable, **kwargs):
+    '''Plot data and regression model fits across a FacetGrid. Can be used to plot a single bar chart variable.(changable to bar_plot)
+    Args:
+        data (DataFrame): CSV file path or DataFrame object.
+        variable (str): Variables that specify positions on the x and y axes.
+        kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
+    '''
+    if isinstance(data, str):
+        df = pd.read_csv(data)
+    else:
+        df = data
+    sns.barplot(data=df,y=df[variable], **kwargs)
+
+def count_plot(data, x, hue= None, **kwargs):
+    '''Plot data and regression model fits across a FacetGrid. Can be used to plot a single variable.(changable to single_count_plot)
+    Args:
+        data (DataFrame): CSV file path or DataFrame object.
+        x (str): Variables that specify positions on the x and y axes.
+        hue (str): Variable in data to map plot aspects to different colors.
+        kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
+    '''
+    if isinstance(data, str):
+        df = pd.read_csv(data)
+    else:
+        df = data
+    sns.countplot(data=df, x=x, hue=hue, **kwargs)
+
+def single_count_plot(data, variable, **kwargs):
+    '''Plot data and regression model fits across a FacetGrid. Can be used to plot a single variable.(changable to count_plot)
+    Args:
+        data (DataFrame): CSV file path or DataFrame object.
+        variable (str): Variables that specify positions on the x and y axes.
+        kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
+    '''
+    if isinstance(data, str):
+        df = pd.read_csv(data)
+    else:
+        df = data
+    sns.countplot(data=df,x=df[variable], **kwargs)
+
+def point_plot(data, x, y, hue= None, **kwargs):
+    '''Plot data and regression model fits across a FacetGrid. Can be used to plot a single variable.(changable to single_point_plot)
+    Args:
+        data (DataFrame): CSV file path or DataFrame object.
+        x, y (str): Variables that specify positions on the x and y axes.
+        hue (str): Variable in data to map plot aspects to different colors.
+        kwargs: Additional keyword arguments are passed to the function used to draw the plot on the joint Axes, superseding items in the joint_kws dictionary.
+    '''
+    if isinstance(data, str):
+        df = pd.read_csv(data)
+    else:
+        df = data
+    sns.pointplot(data=df, x=x, y=y, hue=hue, **kwargs)
```

### Comparing `geomapdemo-0.3.2/geomapdemo/foliumap.py` & `geomapdemo-0.3.3/geomapdemo/foliumap.py`

 * *Files 6% similar despite different names*

```diff
@@ -232,8 +232,14 @@
     
     def add_layer(self, layer):
         """Adds a layer to the map
         Args:
             layer (TileLayer): A TileLayer instance.
         """       
         layer.add_to(self)
-        
+
+    def export(self, outfile="map.html"):
+        """Saves the map to a file
+        Args:
+            outfile (str, optional): The output file path to the HTML file. Defaults to "map.html".
+        """        
+        self.save(outfile)
```

### Comparing `geomapdemo-0.3.2/geomapdemo/geomapdemo.py` & `geomapdemo-0.3.3/geomapdemo/geomapdemo.py`

 * *Files 7% similar despite different names*

```diff
@@ -329,15 +329,20 @@
         from ipyleaflet import WidgetControl
         logo = widgets.HTML(f'<img src="{url}" alt="Logo" width="{width}" height="{height}">')
         control = WidgetControl(widget=logo, position=position)
         self.add_control(control)
 
 
     def add_toolbar(self, position='topright', widget_width='250px'):
-        '''adds a toolbar to the map'''
+        '''adds a toolbar to the map
+        Args:
+            position (str, optional): The position of the toolbar. Defaults to 'topright'.
+            widget_width (str, optional): The width of the toolbar. Defaults to '250px'.
+        '''
+        
         from ipyleaflet import WidgetControl
         padding= '0px 0px 0px 4px'
         
         toolbar_button=widgets.ToggleButton(
             value=False,
             tooltip='Toolbar',
             icon='wrench',
@@ -368,14 +373,49 @@
         toolbar_widget.children = [
             widgets.HBox([close_button, toolbar_button]),
             int_slider,
         ]       
         toolbar_control = WidgetControl(widget=toolbar_widget, position= position)
         self.add_control(toolbar_control)
 
+    def export(self, filepath='map.html', close_map=True):
+        """Exports the map to an HTML file
+        Args:
+            filepath (str): The output filepath. Defaults to 'map.html'.
+            close_map (bool, optional): Whether to close the map after exporting. Defaults to True.
+        """ 
+        import time
+        from ipywidgets.embed import embed_minimal_html
+        time.sleep(1)
+        embed_minimal_html(fp=filepath, views=[self], title='Map')
+        if close_map:
+            self.close()
+    
+    def add_linked_map(self, zoom=4, position= "bottomright"):
+        '''Adds a linked map to the map
+        Args:
+            zoom (int, optional): The zoom level of the linked map. Defaults to 4.
+            position (str, optional): The position of the linked map. Defaults to "bottomright".
+        '''
+
+        from ipyleaflet import WidgetControl
+        minimap =ipyleaflet.Map(
+            zoom_control=False,
+            attribution_control=False, 
+            zoom=zoom,
+            center=self.center,
+            layers=[self.layers[0]]
+        )
+        minimap.layout.width = '150px'
+        minimap.layout.height = '150px'
+        ipyleaflet.link((minimap, 'center'), (self, 'center'))
+        minimap_control = WidgetControl(widget=minimap, position=position)
+        self.add_control(minimap_control)
+        
+    
 
 
 
 
 def generate_random_string(length=10, upper=False, punctuations=False, digits=False):
     """Generates a random string of fixed length
```

### Comparing `geomapdemo-0.3.2/geomapdemo.egg-info/PKG-INFO` & `geomapdemo-0.3.3/geomapdemo.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: geomapdemo
-Version: 0.3.2
+Version: 0.3.3
 Summary: A python package for interactive mapping.
 Home-page: https://github.com/zyang91/geomapdemo
 Author: Zhanchao Yang
 Author-email: zyang91@binghamton.edu
 License: MIT license
 Keywords: geomapdemo
 Classifier: Development Status :: 2 - Pre-Alpha
```

### Comparing `geomapdemo-0.3.2/setup.py` & `geomapdemo-0.3.3/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -50,10 +50,10 @@
     keywords='geomapdemo',
     name='geomapdemo',
     packages=find_packages(include=['geomapdemo', 'geomapdemo.*']),
     setup_requires=setup_requirements,
     test_suite='tests',
     tests_require=test_requirements,
     url='https://github.com/zyang91/geomapdemo',
-    version='0.3.2',
+    version='0.3.3',
     zip_safe=False,
 )
```

