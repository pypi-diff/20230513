# Comparing `tmp/ergastirio-0.8.tar.gz` & `tmp/ergastirio-0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ergastirio-0.8.tar", last modified: Mon Mar  7 21:55:20 2022, max compression
+gzip compressed data, was "ergastirio-0.9.tar", last modified: Mon Mar  7 21:58:15 2022, max compression
```

## Comparing `ergastirio-0.8.tar` & `ergastirio-0.9.tar`

### file list

```diff
@@ -1,29 +1,29 @@
-drwxrwxrwx   0        0        0        0 2022-03-07 21:55:20.572774 ergastirio-0.8/
--rw-rw-rw-   0        0        0       82 2022-02-28 02:17:42.000000 ergastirio-0.8/MANIFEST.in
--rw-rw-rw-   0        0        0      342 2022-03-07 21:55:20.539827 ergastirio-0.8/PKG-INFO
--rw-rw-rw-   0        0        0        0 2022-02-28 23:29:45.000000 ergastirio-0.8/README.md
-drwxrwxrwx   0        0        0        0 2022-03-07 21:55:20.359078 ergastirio-0.8/ergastirio/
--rw-rw-rw-   0        0        0       36 2022-03-05 04:35:39.000000 ergastirio-0.8/ergastirio/__init__.py
--rw-rw-rw-   0        0        0      258 2022-03-06 16:54:54.000000 ergastirio-0.8/ergastirio/config_default.json
--rw-rw-rw-   0        0        0    18398 2022-03-07 21:55:01.000000 ergastirio-0.8/ergastirio/experiment.py
--rw-rw-rw-   0        0        0    15237 2022-03-06 16:54:47.000000 ergastirio-0.8/ergastirio/experiment_initializer.py
-drwxrwxrwx   0        0        0        0 2022-03-07 21:55:20.536836 ergastirio-0.8/ergastirio/graphics/
--rw-rw-rw-   0        0        0    63387 2022-02-25 03:30:04.000000 ergastirio-0.8/ergastirio/graphics/home.png
--rw-rw-rw-   0        0        0     7799 2021-08-31 16:42:47.000000 ergastirio-0.8/ergastirio/graphics/pause.png
--rw-rw-rw-   0        0        0     9320 2021-08-31 16:41:38.000000 ergastirio-0.8/ergastirio/graphics/play.png
--rw-rw-rw-   0        0        0    43382 2022-02-25 03:20:02.000000 ergastirio-0.8/ergastirio/graphics/settings.png
--rw-rw-rw-   0        0        0     8088 2022-03-06 16:56:47.000000 ergastirio-0.8/ergastirio/main.py
--rw-rw-rw-   0        0        0    19185 2022-03-07 21:54:09.000000 ergastirio-0.8/ergastirio/panels.py
--rw-rw-rw-   0        0        0    17214 2022-02-25 03:33:01.000000 ergastirio-0.8/ergastirio/plots.py
--rw-rw-rw-   0        0        0      681 2022-03-01 17:28:59.000000 ergastirio-0.8/ergastirio/utils.py
--rw-rw-rw-   0        0        0    12511 2022-03-05 04:56:25.000000 ergastirio-0.8/ergastirio/widgets.py
-drwxrwxrwx   0        0        0        0 2022-03-07 21:55:20.440094 ergastirio-0.8/ergastirio.egg-info/
--rw-rw-rw-   0        0        0      342 2022-03-07 21:55:20.000000 ergastirio-0.8/ergastirio.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      608 2022-03-07 21:55:20.000000 ergastirio-0.8/ergastirio.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-03-07 21:55:20.000000 ergastirio-0.8/ergastirio.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       53 2022-03-07 21:55:20.000000 ergastirio-0.8/ergastirio.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0        2 2022-03-07 16:51:19.000000 ergastirio-0.8/ergastirio.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       45 2022-03-07 21:55:20.000000 ergastirio-0.8/ergastirio.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2022-03-07 21:55:20.000000 ergastirio-0.8/ergastirio.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2022-03-07 21:55:20.573775 ergastirio-0.8/setup.cfg
--rw-rw-rw-   0        0        0      943 2022-03-07 21:55:12.000000 ergastirio-0.8/setup.py
+drwxrwxrwx   0        0        0        0 2022-03-07 21:58:15.037657 ergastirio-0.9/
+-rw-rw-rw-   0        0        0       82 2022-02-28 02:17:42.000000 ergastirio-0.9/MANIFEST.in
+-rw-rw-rw-   0        0        0      342 2022-03-07 21:58:14.989278 ergastirio-0.9/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2022-02-28 23:29:45.000000 ergastirio-0.9/README.md
+drwxrwxrwx   0        0        0        0 2022-03-07 21:58:14.873518 ergastirio-0.9/ergastirio/
+-rw-rw-rw-   0        0        0       36 2022-03-05 04:35:39.000000 ergastirio-0.9/ergastirio/__init__.py
+-rw-rw-rw-   0        0        0      258 2022-03-06 16:54:54.000000 ergastirio-0.9/ergastirio/config_default.json
+-rw-rw-rw-   0        0        0    18400 2022-03-07 21:56:22.000000 ergastirio-0.9/ergastirio/experiment.py
+-rw-rw-rw-   0        0        0    15237 2022-03-06 16:54:47.000000 ergastirio-0.9/ergastirio/experiment_initializer.py
+drwxrwxrwx   0        0        0        0 2022-03-07 21:58:14.986281 ergastirio-0.9/ergastirio/graphics/
+-rw-rw-rw-   0        0        0    63387 2022-02-25 03:30:04.000000 ergastirio-0.9/ergastirio/graphics/home.png
+-rw-rw-rw-   0        0        0     7799 2021-08-31 16:42:47.000000 ergastirio-0.9/ergastirio/graphics/pause.png
+-rw-rw-rw-   0        0        0     9320 2021-08-31 16:41:38.000000 ergastirio-0.9/ergastirio/graphics/play.png
+-rw-rw-rw-   0        0        0    43382 2022-02-25 03:20:02.000000 ergastirio-0.9/ergastirio/graphics/settings.png
+-rw-rw-rw-   0        0        0     8088 2022-03-06 16:56:47.000000 ergastirio-0.9/ergastirio/main.py
+-rw-rw-rw-   0        0        0    19245 2022-03-07 21:57:57.000000 ergastirio-0.9/ergastirio/panels.py
+-rw-rw-rw-   0        0        0    17214 2022-02-25 03:33:01.000000 ergastirio-0.9/ergastirio/plots.py
+-rw-rw-rw-   0        0        0      681 2022-03-01 17:28:59.000000 ergastirio-0.9/ergastirio/utils.py
+-rw-rw-rw-   0        0        0    12511 2022-03-05 04:56:25.000000 ergastirio-0.9/ergastirio/widgets.py
+drwxrwxrwx   0        0        0        0 2022-03-07 21:58:14.974314 ergastirio-0.9/ergastirio.egg-info/
+-rw-rw-rw-   0        0        0      342 2022-03-07 21:58:14.000000 ergastirio-0.9/ergastirio.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      608 2022-03-07 21:58:14.000000 ergastirio-0.9/ergastirio.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2022-03-07 21:58:14.000000 ergastirio-0.9/ergastirio.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       53 2022-03-07 21:58:14.000000 ergastirio-0.9/ergastirio.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0        2 2022-03-07 16:51:19.000000 ergastirio-0.9/ergastirio.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       45 2022-03-07 21:58:14.000000 ergastirio-0.9/ergastirio.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2022-03-07 21:58:14.000000 ergastirio-0.9/ergastirio.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2022-03-07 21:58:15.039668 ergastirio-0.9/setup.cfg
+-rw-rw-rw-   0        0        0      943 2022-03-07 21:58:11.000000 ergastirio-0.9/setup.py
```

### Comparing `ergastirio-0.8/ergastirio/experiment.py` & `ergastirio-0.9/ergastirio/experiment.py`

 * *Files 1% similar despite different names*

```diff
@@ -183,18 +183,18 @@
         #self.data = np.append(self.data,[current_data] ,axis=0)
         self.data.append(current_data)
         self.data_std.append([0]*(len(current_data)-1))
 
     def set_trigger_modality(self,modality):
         if modality == 'internal':
             self.triggered_acquisition = False
-            self.logger.info(f"Set the experiment in 'internal trigger modality.")
+            self.logger.info(f"Set the experiment to 'internal trigger modality'.")
         if modality == 'external':
             self.triggered_acquisition = True
-            self.logger.info(f"Set the experiment in 'external trigger modality.")
+            self.logger.info(f"Set the experiment to 'external trigger modality'.")
 
     def take_single_acquisition(self):
         self.store_current_data_from_all_instruments()
 
     def take_single_set_of_acquisitions(self,counter):
         ''' Takes a sequence of acquisitions. The number of acquisitions is counter, separated by a time self.refresh_time_multiple_acquisitions.
             This function calls take_single_acquisition() and then calls itself after a time specified by self.refresh_time_multiple_acquisitions,
```

### Comparing `ergastirio-0.8/ergastirio/experiment_initializer.py` & `ergastirio-0.9/ergastirio/experiment_initializer.py`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio/graphics/home.png` & `ergastirio-0.9/ergastirio/graphics/home.png`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio/graphics/pause.png` & `ergastirio-0.9/ergastirio/graphics/pause.png`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio/graphics/play.png` & `ergastirio-0.9/ergastirio/graphics/play.png`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio/graphics/settings.png` & `ergastirio-0.9/ergastirio/graphics/settings.png`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio/main.py` & `ergastirio-0.9/ergastirio/main.py`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio/panels.py` & `ergastirio-0.9/ergastirio/panels.py`

 * *Files 0% similar despite different names*

```diff
@@ -214,14 +214,15 @@
 
     def value_changed_spinbox_NumbAcquisitions(self):
         self.experiment.numb_acquisitions_per_trigger = self.spinbox_NumbAcquisitions.value()
 
     def click_radio_global_instrument(self):
         if self.radio_TriggerGlobal.isChecked():
             self.experiment.set_trigger_modality('internal')
+            self.press_enter_edit_AcquisitionRefreshTime()
             ergastirio.utils.enable_widget([self.edit_RefreshTime,self.label_RefreshTime])
             ergastirio.utils.disable_widget([self.combo_TriggerInstruments,self.edit_TriggerInstrumentDelay,self.label_TriggerInstrument,self.label_TriggerInstrumentDelay])
         if self.radio_TriggerInstrument.isChecked():
             self.experiment.set_trigger_modality('external')
             self.change_combo_TriggerInstruments()
             ergastirio.utils.disable_widget([self.edit_RefreshTime,self.label_RefreshTime])
             ergastirio.utils.enable_widget([self.combo_TriggerInstruments,self.edit_TriggerInstrumentDelay,self.label_TriggerInstrument,self.label_TriggerInstrumentDelay])
```

### Comparing `ergastirio-0.8/ergastirio/plots.py` & `ergastirio-0.9/ergastirio/plots.py`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio/utils.py` & `ergastirio-0.9/ergastirio/utils.py`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio/widgets.py` & `ergastirio-0.9/ergastirio/widgets.py`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/ergastirio.egg-info/SOURCES.txt` & `ergastirio-0.9/ergastirio.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `ergastirio-0.8/setup.py` & `ergastirio-0.9/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 with open(path.join(this_directory, 'README.md'),encoding ='unicode_escape') as f:
     long_description = f.read()
 
 with open("requirements.txt") as f:
     required_packages = f.read().splitlines()
 
 setuptools.setup(name='ergastirio',
-      version='0.8',
+      version='0.9',
       description='A python GUI connect several devices and automatize acquisition data in lab.',
       long_description=long_description,
       long_description_content_type='text/markdown',
       url='https://github.com/MicheleCotrufo/',
       author='Michele Cotrufo',
       author_email='michele.cotrufo@gmail.com',
       license='MIT',
```

