# Comparing `tmp/abstract_instrument_interface-0.8.tar.gz` & `tmp/abstract_instrument_interface-0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "abstract_instrument_interface-0.8.tar", last modified: Wed Jan 18 16:16:45 2023, max compression
+gzip compressed data, was "abstract_instrument_interface-0.9.tar", last modified: Sat May 13 19:04:01 2023, max compression
```

## Comparing `abstract_instrument_interface-0.8.tar` & `abstract_instrument_interface-0.9.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-01-18 16:16:45.931119 abstract_instrument_interface-0.8/
--rw-rw-rw-   0        0        0       94 2022-09-05 13:46:34.000000 abstract_instrument_interface-0.8/MANIFEST.in
--rw-rw-rw-   0        0        0      960 2023-01-18 16:16:45.890884 abstract_instrument_interface-0.8/PKG-INFO
--rw-rw-rw-   0        0        0      559 2023-01-18 16:12:16.000000 abstract_instrument_interface-0.8/README.md
-drwxrwxrwx   0        0        0        0 2023-01-18 16:16:45.599093 abstract_instrument_interface-0.8/abstract_instrument_interface/
--rw-rw-rw-   0        0        0       52 2022-10-05 01:37:55.000000 abstract_instrument_interface-0.8/abstract_instrument_interface/__init__.py
--rw-rw-rw-   0        0        0    13314 2023-01-17 20:25:13.000000 abstract_instrument_interface-0.8/abstract_instrument_interface/abstract_classes.py
-drwxrwxrwx   0        0        0        0 2023-01-18 16:16:45.810361 abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/
--rw-rw-rw-   0        0        0     7799 2021-08-31 16:42:50.000000 abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/pause.png
--rw-rw-rw-   0        0        0     9320 2021-08-31 16:41:45.000000 abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/play.png
--rw-rw-rw-   0        0        0     3439 2021-08-29 03:28:31.000000 abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/refresh.png
--rw-rw-rw-   0        0        0     7522 2021-08-31 16:43:00.000000 abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/stop.png
--rw-rw-rw-   0        0        0    29053 2022-10-27 02:09:13.000000 abstract_instrument_interface-0.8/abstract_instrument_interface/ramp.py
-drwxrwxrwx   0        0        0        0 2023-01-18 16:16:45.643462 abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/
--rw-rw-rw-   0        0        0      960 2023-01-18 16:16:44.000000 abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      672 2023-01-18 16:16:44.000000 abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-01-18 16:16:44.000000 abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-01-18 16:16:44.000000 abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       14 2023-01-18 16:16:44.000000 abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/requires.txt
--rw-rw-rw-   0        0        0       30 2023-01-18 16:16:44.000000 abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-01-18 16:16:45.932095 abstract_instrument_interface-0.8/setup.cfg
--rw-rw-rw-   0        0        0      927 2023-01-18 16:13:09.000000 abstract_instrument_interface-0.8/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:04:01.870367 abstract_instrument_interface-0.9/
+-rw-rw-rw-   0        0        0       94 2022-09-05 13:46:34.000000 abstract_instrument_interface-0.9/MANIFEST.in
+-rw-rw-rw-   0        0        0      960 2023-05-13 19:04:01.868374 abstract_instrument_interface-0.9/PKG-INFO
+-rw-rw-rw-   0        0        0      559 2023-01-18 16:12:16.000000 abstract_instrument_interface-0.9/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 19:04:01.771205 abstract_instrument_interface-0.9/abstract_instrument_interface/
+-rw-rw-rw-   0        0        0       52 2022-10-05 01:37:55.000000 abstract_instrument_interface-0.9/abstract_instrument_interface/__init__.py
+-rw-rw-rw-   0        0        0    13751 2023-05-07 18:04:39.000000 abstract_instrument_interface-0.9/abstract_instrument_interface/abstract_classes.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:04:01.821043 abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/
+-rw-rw-rw-   0        0        0     7799 2021-08-31 16:42:50.000000 abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/pause.png
+-rw-rw-rw-   0        0        0     9320 2021-08-31 16:41:45.000000 abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/play.png
+-rw-rw-rw-   0        0        0     3439 2021-08-29 03:28:31.000000 abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/refresh.png
+-rw-rw-rw-   0        0        0     7522 2021-08-31 16:43:00.000000 abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/stop.png
+-rw-rw-rw-   0        0        0    29053 2022-10-27 02:09:13.000000 abstract_instrument_interface-0.9/abstract_instrument_interface/ramp.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:04:01.793117 abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/
+-rw-rw-rw-   0        0        0      960 2023-05-13 19:04:01.000000 abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      672 2023-05-13 19:04:01.000000 abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 19:04:01.000000 abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-05-13 19:04:01.000000 abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       14 2023-05-13 19:04:01.000000 abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       30 2023-05-13 19:04:01.000000 abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 19:04:01.870367 abstract_instrument_interface-0.9/setup.cfg
+-rw-rw-rw-   0        0        0      927 2023-05-13 19:00:33.000000 abstract_instrument_interface-0.9/setup.py
```

### Comparing `abstract_instrument_interface-0.8/PKG-INFO` & `abstract_instrument_interface-0.9/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: abstract_instrument_interface
-Version: 0.8
+Version: 0.9
 Summary: This package contains abstract classes for interfaces and GUIs which are used by all instruments compatible with Ergastirio
 Home-page: https://github.com/MicheleCotrufo/
 Author: Michele Cotrufo
 Author-email: michele.cotrufo@gmail.com
 License: MIT
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

### Comparing `abstract_instrument_interface-0.8/README.md` & `abstract_instrument_interface-0.9/README.md`

 * *Files identical despite different names*

### Comparing `abstract_instrument_interface-0.8/abstract_instrument_interface/abstract_classes.py` & `abstract_instrument_interface-0.9/abstract_instrument_interface/abstract_classes.py`

 * *Files 2% similar despite different names*

```diff
@@ -181,14 +181,22 @@
         else:
             self._send_trigger()
 
     def _send_trigger(self):
         self.logger.info(f"Trigger sent.")
         self.trigger[0]()
 
+    def receive_trigger(self,**kwargs):
+        '''
+        This method allows the device to receive a trigger from an external script (for example, when the device is used inside Ergastirio). 
+        The function defined here in the abstract class is just a placeholder. The specific action that happens when the instrument
+        is triggered will be coded in the corresponding instrument interface
+        '''
+        pass
+
     def update(self):
         if hasattr(self,'trigger'):
             if not(self.trigger==None):
                 self.send_trigger()
                 
     @staticmethod
     def check_property_until(property_to_check, values_list, actions_list, refresh_time=0.1):
```

### Comparing `abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/pause.png` & `abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/pause.png`

 * *Files identical despite different names*

### Comparing `abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/play.png` & `abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/play.png`

 * *Files identical despite different names*

### Comparing `abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/refresh.png` & `abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/refresh.png`

 * *Files identical despite different names*

### Comparing `abstract_instrument_interface-0.8/abstract_instrument_interface/graphics/stop.png` & `abstract_instrument_interface-0.9/abstract_instrument_interface/graphics/stop.png`

 * *Files identical despite different names*

### Comparing `abstract_instrument_interface-0.8/abstract_instrument_interface/ramp.py` & `abstract_instrument_interface-0.9/abstract_instrument_interface/ramp.py`

 * *Files identical despite different names*

### Comparing `abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/PKG-INFO` & `abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: abstract-instrument-interface
-Version: 0.8
+Version: 0.9
 Summary: This package contains abstract classes for interfaces and GUIs which are used by all instruments compatible with Ergastirio
 Home-page: https://github.com/MicheleCotrufo/
 Author: Michele Cotrufo
 Author-email: michele.cotrufo@gmail.com
 License: MIT
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

### Comparing `abstract_instrument_interface-0.8/abstract_instrument_interface.egg-info/SOURCES.txt` & `abstract_instrument_interface-0.9/abstract_instrument_interface.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `abstract_instrument_interface-0.8/setup.py` & `abstract_instrument_interface-0.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 with open(path.join(this_directory, 'README.md'),encoding ='unicode_escape') as f:
     long_description = f.read()
 
 with open("requirements.txt") as f:
     required_packages = f.read().splitlines()
 
 setuptools.setup(name='abstract_instrument_interface',
-      version='0.8',
+      version='0.9',
       description='This package contains abstract classes for interfaces and GUIs which are used by all instruments compatible with Ergastirio',
       long_description=long_description,
       long_description_content_type='text/markdown',
       url='https://github.com/MicheleCotrufo/',
       author='Michele Cotrufo',
       author_email='michele.cotrufo@gmail.com',
       license='MIT',
```

