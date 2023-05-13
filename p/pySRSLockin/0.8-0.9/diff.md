# Comparing `tmp/pySRSLockin-0.8.tar.gz` & `tmp/pySRSLockin-0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pySRSLockin-0.8.tar", last modified: Sun Mar  6 16:48:44 2022, max compression
+gzip compressed data, was "pySRSLockin-0.9.tar", last modified: Mon Mar  7 16:59:29 2022, max compression
```

## Comparing `pySRSLockin-0.8.tar` & `pySRSLockin-0.9.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxrwxrwx   0        0        0        0 2022-03-06 16:48:44.548947 pySRSLockin-0.8/
--rw-rw-rw-   0        0        0       57 2022-02-28 02:13:02.000000 pySRSLockin-0.8/MANIFEST.in
--rw-rw-rw-   0        0        0      361 2022-03-06 16:48:44.547950 pySRSLockin-0.8/PKG-INFO
--rw-rw-rw-   0        0        0        0 2022-02-28 02:12:11.000000 pySRSLockin-0.8/README.md
-drwxrwxrwx   0        0        0        0 2022-03-06 16:48:44.421290 pySRSLockin-0.8/pySRSLockin/
--rw-rw-rw-   0        0        0       35 2022-02-24 02:53:34.000000 pySRSLockin-0.8/pySRSLockin/__init__.py
--rw-rw-rw-   0        0        0     3753 2022-03-06 16:37:08.000000 pySRSLockin-0.8/pySRSLockin/abstract_interface.py
--rw-rw-rw-   0        0        0     3167 2022-02-16 00:51:46.000000 pySRSLockin-0.8/pySRSLockin/config.py
--rw-rw-rw-   0        0        0    11998 2022-03-03 04:07:57.000000 pySRSLockin-0.8/pySRSLockin/driver.py
-drwxrwxrwx   0        0        0        0 2022-03-06 16:48:44.546953 pySRSLockin-0.8/pySRSLockin/graphics/
--rw-rw-rw-   0        0        0     7799 2022-02-16 02:37:29.000000 pySRSLockin-0.8/pySRSLockin/graphics/pause.png
--rw-rw-rw-   0        0        0     9320 2022-02-16 02:37:33.000000 pySRSLockin-0.8/pySRSLockin/graphics/play.png
--rw-rw-rw-   0        0        0     3439 2022-02-16 02:37:35.000000 pySRSLockin-0.8/pySRSLockin/graphics/refresh.png
--rw-rw-rw-   0        0        0     7522 2022-02-16 02:37:39.000000 pySRSLockin-0.8/pySRSLockin/graphics/stop.png
--rw-rw-rw-   0        0        0    26489 2022-03-06 16:40:33.000000 pySRSLockin-0.8/pySRSLockin/main.py
--rw-rw-rw-   0        0        0    16385 2022-02-16 00:39:14.000000 pySRSLockin-0.8/pySRSLockin/plots.py
--rw-rw-rw-   0        0        0       29 2022-02-16 03:00:09.000000 pySRSLockin-0.8/pySRSLockin/settings.ini
-drwxrwxrwx   0        0        0        0 2022-03-06 16:48:44.456195 pySRSLockin-0.8/pySRSLockin.egg-info/
--rw-rw-rw-   0        0        0      361 2022-03-06 16:48:43.000000 pySRSLockin-0.8/pySRSLockin.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      568 2022-03-06 16:48:44.000000 pySRSLockin-0.8/pySRSLockin.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-03-06 16:48:43.000000 pySRSLockin-0.8/pySRSLockin.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       55 2022-03-06 16:48:43.000000 pySRSLockin-0.8/pySRSLockin.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0        2 2022-03-06 16:48:43.000000 pySRSLockin-0.8/pySRSLockin.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       37 2022-03-06 16:48:43.000000 pySRSLockin-0.8/pySRSLockin.egg-info/requires.txt
--rw-rw-rw-   0        0        0       12 2022-03-06 16:48:43.000000 pySRSLockin-0.8/pySRSLockin.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2022-03-06 16:48:44.548947 pySRSLockin-0.8/setup.cfg
--rw-rw-rw-   0        0        0      965 2022-03-06 16:48:37.000000 pySRSLockin-0.8/setup.py
+drwxrwxrwx   0        0        0        0 2022-03-07 16:59:29.965407 pySRSLockin-0.9/
+-rw-rw-rw-   0        0        0       57 2022-02-28 02:13:02.000000 pySRSLockin-0.9/MANIFEST.in
+-rw-rw-rw-   0        0        0      361 2022-03-07 16:59:29.964406 pySRSLockin-0.9/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2022-02-28 02:12:11.000000 pySRSLockin-0.9/README.md
+drwxrwxrwx   0        0        0        0 2022-03-07 16:59:29.881741 pySRSLockin-0.9/pySRSLockin/
+-rw-rw-rw-   0        0        0       35 2022-02-24 02:53:34.000000 pySRSLockin-0.9/pySRSLockin/__init__.py
+-rw-rw-rw-   0        0        0     4103 2022-03-07 04:36:02.000000 pySRSLockin-0.9/pySRSLockin/abstract_interface.py
+-rw-rw-rw-   0        0        0     3167 2022-02-16 00:51:46.000000 pySRSLockin-0.9/pySRSLockin/config.py
+-rw-rw-rw-   0        0        0    11998 2022-03-03 04:07:57.000000 pySRSLockin-0.9/pySRSLockin/driver.py
+drwxrwxrwx   0        0        0        0 2022-03-07 16:59:29.962875 pySRSLockin-0.9/pySRSLockin/graphics/
+-rw-rw-rw-   0        0        0     7799 2022-02-16 02:37:29.000000 pySRSLockin-0.9/pySRSLockin/graphics/pause.png
+-rw-rw-rw-   0        0        0     9320 2022-02-16 02:37:33.000000 pySRSLockin-0.9/pySRSLockin/graphics/play.png
+-rw-rw-rw-   0        0        0     3439 2022-02-16 02:37:35.000000 pySRSLockin-0.9/pySRSLockin/graphics/refresh.png
+-rw-rw-rw-   0        0        0     7522 2022-02-16 02:37:39.000000 pySRSLockin-0.9/pySRSLockin/graphics/stop.png
+-rw-rw-rw-   0        0        0    26373 2022-03-07 04:36:45.000000 pySRSLockin-0.9/pySRSLockin/main.py
+-rw-rw-rw-   0        0        0    16385 2022-02-16 00:39:14.000000 pySRSLockin-0.9/pySRSLockin/plots.py
+-rw-rw-rw-   0        0        0       29 2022-02-16 03:00:09.000000 pySRSLockin-0.9/pySRSLockin/settings.ini
+drwxrwxrwx   0        0        0        0 2022-03-07 16:59:29.934564 pySRSLockin-0.9/pySRSLockin.egg-info/
+-rw-rw-rw-   0        0        0      361 2022-03-07 16:59:29.000000 pySRSLockin-0.9/pySRSLockin.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      568 2022-03-07 16:59:29.000000 pySRSLockin-0.9/pySRSLockin.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2022-03-07 16:59:29.000000 pySRSLockin-0.9/pySRSLockin.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       55 2022-03-07 16:59:29.000000 pySRSLockin-0.9/pySRSLockin.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0        2 2022-03-07 16:59:29.000000 pySRSLockin-0.9/pySRSLockin.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       37 2022-03-07 16:59:29.000000 pySRSLockin-0.9/pySRSLockin.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2022-03-07 16:59:29.000000 pySRSLockin-0.9/pySRSLockin.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2022-03-07 16:59:29.965437 pySRSLockin-0.9/setup.cfg
+-rw-rw-rw-   0        0        0      965 2022-03-07 16:58:21.000000 pySRSLockin-0.9/setup.py
```

### Comparing `pySRSLockin-0.8/pySRSLockin/abstract_interface.py` & `pySRSLockin-0.9/pySRSLockin/abstract_interface.py`

 * *Files 4% similar despite different names*

```diff
@@ -73,11 +73,21 @@
         self.logger.info(f"Creating a trigger for this device...")
         self.trigger = [external_function, delay]
 
     def send_trigger(self,external_function,delay=0):
         self.logger.info(f"Trigger Sent.")
         QtCore.QTimer.singleShot(int(self.trigger[1]*1e3), self.trigger[0]) 
 
-    def update():
+    def update(self):
         if hasattr(self,'trigger'):
             if not(self.trigger==None):
-                self.send_trigger()
+                self.send_trigger()
+
+    def close(self):     
+        try:
+            if (self.instrument.connected == True):
+                self.disconnect_device()
+        except Exception as e:
+            self.logger.error(f"{e}")
+            if hasattr(self,'plot_window'):
+                if self.gui.plot_window:
+                    self.gui.plot_window.close()
```

### Comparing `pySRSLockin-0.8/pySRSLockin/config.py` & `pySRSLockin-0.9/pySRSLockin/config.py`

 * *Files identical despite different names*

### Comparing `pySRSLockin-0.8/pySRSLockin/driver.py` & `pySRSLockin-0.9/pySRSLockin/driver.py`

 * *Files identical despite different names*

### Comparing `pySRSLockin-0.8/pySRSLockin/graphics/pause.png` & `pySRSLockin-0.9/pySRSLockin/graphics/pause.png`

 * *Files identical despite different names*

### Comparing `pySRSLockin-0.8/pySRSLockin/graphics/play.png` & `pySRSLockin-0.9/pySRSLockin/graphics/play.png`

 * *Files identical despite different names*

### Comparing `pySRSLockin-0.8/pySRSLockin/graphics/refresh.png` & `pySRSLockin-0.9/pySRSLockin/graphics/refresh.png`

 * *Files identical despite different names*

### Comparing `pySRSLockin-0.8/pySRSLockin/graphics/stop.png` & `pySRSLockin-0.9/pySRSLockin/graphics/stop.png`

 * *Files identical despite different names*

### Comparing `pySRSLockin-0.8/pySRSLockin/main.py` & `pySRSLockin-0.9/pySRSLockin/main.py`

 * *Files 1% similar despite different names*

```diff
@@ -465,20 +465,15 @@
                 try:
                     self.edit_Output[k].setText(f"{self.output[k]:.2e}")
                 except:
                     self.edit_Output[k].setText(f"nan")
             QtCore.QTimer.singleShot(int(self.refresh_time*1e3), self.update)
            
         return
-
-    def close(self):
-        if (self.instrument.connected == True):
-            self.disconnect_device()
-    
-
+ 
 class MainWindow(Qt.QWidget):
     def __init__(self):
         super().__init__()
         self.setWindowTitle(__package__)
         # Set the central widget of the Window.
         # self.setCentralWidget(self.container)
     def closeEvent(self, event):
```

### Comparing `pySRSLockin-0.8/pySRSLockin/plots.py` & `pySRSLockin-0.9/pySRSLockin/plots.py`

 * *Files identical despite different names*

### Comparing `pySRSLockin-0.8/pySRSLockin.egg-info/SOURCES.txt` & `pySRSLockin-0.9/pySRSLockin.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pySRSLockin-0.8/setup.py` & `pySRSLockin-0.9/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 with open(path.join(this_directory, 'README.md'),encoding ='unicode_escape') as f:
     long_description = f.read()
 
 with open("requirements.txt") as f:
     required_packages = f.read().splitlines()
 
 setuptools.setup(name='pySRSLockin',
-      version='0.8',
+      version='0.9',
       description='A python library/GUI to access and control different models of lock-in amplifiers made by SRS.',
       long_description=long_description,
       long_description_content_type='text/markdown',
       url='https://github.com/MicheleCotrufo/',
       author='Michele Cotrufo',
       author_email='michele.cotrufo@gmail.com',
       license='MIT',
```

