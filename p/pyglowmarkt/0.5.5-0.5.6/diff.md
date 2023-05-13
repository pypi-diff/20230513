# Comparing `tmp/pyglowmarkt-0.5.5.tar.gz` & `tmp/pyglowmarkt-0.5.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyglowmarkt-0.5.5.tar", last modified: Tue Jan 10 08:17:25 2023, max compression
+gzip compressed data, was "pyglowmarkt-0.5.6.tar", last modified: Sat May 13 09:06:58 2023, max compression
```

## Comparing `pyglowmarkt-0.5.5.tar` & `pyglowmarkt-0.5.6.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 mark      (1000) mark      (1000)        0 2023-01-10 08:17:25.078699 pyglowmarkt-0.5.5/
--rw-rw-r--   0 mark      (1000) mark      (1000)    11357 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.5/LICENSE
--rw-r--r--   0 mark      (1000) mark      (1000)     8985 2023-01-10 08:17:25.078699 pyglowmarkt-0.5.5/PKG-INFO
--rw-r--r--   0 mark      (1000) mark      (1000)     8329 2022-12-03 12:35:15.000000 pyglowmarkt-0.5.5/README.md
-drwxr-xr-x   0 mark      (1000) mark      (1000)        0 2023-01-10 08:17:25.076699 pyglowmarkt-0.5.5/glowmarkt/
--rw-rw-r--   0 mark      (1000) mark      (1000)       26 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.5/glowmarkt/__init__.py
--rw-r--r--   0 mark      (1000) mark      (1000)    11818 2022-12-03 12:35:15.000000 pyglowmarkt-0.5.5/glowmarkt/glowmarkt.py
-drwxr-xr-x   0 mark      (1000) mark      (1000)        0 2023-01-10 08:17:25.077699 pyglowmarkt-0.5.5/pyglowmarkt.egg-info/
--rw-rw-r--   0 mark      (1000) mark      (1000)     8985 2023-01-10 08:17:24.000000 pyglowmarkt-0.5.5/pyglowmarkt.egg-info/PKG-INFO
--rw-rw-r--   0 mark      (1000) mark      (1000)      337 2023-01-10 08:17:24.000000 pyglowmarkt-0.5.5/pyglowmarkt.egg-info/SOURCES.txt
--rw-rw-r--   0 mark      (1000) mark      (1000)        1 2023-01-10 08:17:24.000000 pyglowmarkt-0.5.5/pyglowmarkt.egg-info/dependency_links.txt
--rw-rw-r--   0 mark      (1000) mark      (1000)       19 2023-01-10 08:17:24.000000 pyglowmarkt-0.5.5/pyglowmarkt.egg-info/requires.txt
--rw-rw-r--   0 mark      (1000) mark      (1000)       10 2023-01-10 08:17:24.000000 pyglowmarkt-0.5.5/pyglowmarkt.egg-info/top_level.txt
-drwxr-xr-x   0 mark      (1000) mark      (1000)        0 2023-01-10 08:17:25.078699 pyglowmarkt-0.5.5/scripts/
--rwxrwxr-x   0 mark      (1000) mark      (1000)     2328 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.5/scripts/glowmarkt-csv
--rwxrwxr-x   0 mark      (1000) mark      (1000)     2321 2022-07-18 10:20:48.000000 pyglowmarkt-0.5.5/scripts/glowmarkt-dump
--rwxrwxr-x   0 mark      (1000) mark      (1000)     2212 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.5/scripts/glowmarkt-mqtt
--rwxrwxr-x   0 mark      (1000) mark      (1000)     1757 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.5/scripts/glowmarkt-today
--rw-r--r--   0 mark      (1000) mark      (1000)       38 2023-01-10 08:17:25.078699 pyglowmarkt-0.5.5/setup.cfg
--rw-rw-r--   0 mark      (1000) mark      (1000)     1061 2023-01-10 08:16:46.000000 pyglowmarkt-0.5.5/setup.py
+drwxr-xr-x   0 mark      (1000) mark      (1000)        0 2023-05-13 09:06:58.194583 pyglowmarkt-0.5.6/
+-rw-rw-r--   0 mark      (1000) mark      (1000)    11357 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.6/LICENSE
+-rw-r--r--   0 mark      (1000) mark      (1000)     8985 2023-05-13 09:06:58.193583 pyglowmarkt-0.5.6/PKG-INFO
+-rw-r--r--   0 mark      (1000) mark      (1000)     8329 2022-12-03 12:35:15.000000 pyglowmarkt-0.5.6/README.md
+drwxr-xr-x   0 mark      (1000) mark      (1000)        0 2023-05-13 09:06:58.191583 pyglowmarkt-0.5.6/glowmarkt/
+-rw-rw-r--   0 mark      (1000) mark      (1000)       26 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.6/glowmarkt/__init__.py
+-rw-r--r--   0 mark      (1000) mark      (1000)    11940 2023-05-13 09:06:21.000000 pyglowmarkt-0.5.6/glowmarkt/glowmarkt.py
+drwxr-xr-x   0 mark      (1000) mark      (1000)        0 2023-05-13 09:06:58.192583 pyglowmarkt-0.5.6/pyglowmarkt.egg-info/
+-rw-rw-r--   0 mark      (1000) mark      (1000)     8985 2023-05-13 09:06:58.000000 pyglowmarkt-0.5.6/pyglowmarkt.egg-info/PKG-INFO
+-rw-rw-r--   0 mark      (1000) mark      (1000)      337 2023-05-13 09:06:58.000000 pyglowmarkt-0.5.6/pyglowmarkt.egg-info/SOURCES.txt
+-rw-rw-r--   0 mark      (1000) mark      (1000)        1 2023-05-13 09:06:58.000000 pyglowmarkt-0.5.6/pyglowmarkt.egg-info/dependency_links.txt
+-rw-rw-r--   0 mark      (1000) mark      (1000)       19 2023-05-13 09:06:58.000000 pyglowmarkt-0.5.6/pyglowmarkt.egg-info/requires.txt
+-rw-rw-r--   0 mark      (1000) mark      (1000)       10 2023-05-13 09:06:58.000000 pyglowmarkt-0.5.6/pyglowmarkt.egg-info/top_level.txt
+drwxr-xr-x   0 mark      (1000) mark      (1000)        0 2023-05-13 09:06:58.193583 pyglowmarkt-0.5.6/scripts/
+-rwxrwxr-x   0 mark      (1000) mark      (1000)     2328 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.6/scripts/glowmarkt-csv
+-rwxrwxr-x   0 mark      (1000) mark      (1000)     2321 2022-07-18 10:20:48.000000 pyglowmarkt-0.5.6/scripts/glowmarkt-dump
+-rwxrwxr-x   0 mark      (1000) mark      (1000)     2212 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.6/scripts/glowmarkt-mqtt
+-rwxrwxr-x   0 mark      (1000) mark      (1000)     1757 2022-03-05 15:05:24.000000 pyglowmarkt-0.5.6/scripts/glowmarkt-today
+-rw-r--r--   0 mark      (1000) mark      (1000)       38 2023-05-13 09:06:58.194583 pyglowmarkt-0.5.6/setup.cfg
+-rw-rw-r--   0 mark      (1000) mark      (1000)     1061 2023-05-13 09:06:48.000000 pyglowmarkt-0.5.6/setup.py
```

### Comparing `pyglowmarkt-0.5.5/LICENSE` & `pyglowmarkt-0.5.6/LICENSE`

 * *Files identical despite different names*

### Comparing `pyglowmarkt-0.5.5/PKG-INFO` & `pyglowmarkt-0.5.6/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: pyglowmarkt
-Version: 0.5.5
+Version: 0.5.6
 Summary: Python API for accessing Hildebrand/Glowmarkt/Bright API to smart meter data
 Home-page: https://github.com/cybermaggedon/pyglowmarkt
 Author: Cybermaggedon
 Author-email: mark@cyberapocalypse.co.uk
 License: UNKNOWN
-Download-URL: https://github.com/cybermaggedon/pyglowmarkt/archive/refs/tags/v0.5.5.tar.gz
+Download-URL: https://github.com/cybermaggedon/pyglowmarkt/archive/refs/tags/v0.5.6.tar.gz
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `pyglowmarkt-0.5.5/README.md` & `pyglowmarkt-0.5.6/README.md`

 * *Files identical despite different names*

### Comparing `pyglowmarkt-0.5.5/glowmarkt/glowmarkt.py` & `pyglowmarkt-0.5.6/glowmarkt/glowmarkt.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,23 +14,23 @@
 class Rate:
     pass
 
 class Pence:
     def __init__(self, value):
         self.value = value
     def __str__(self):
-        return "%.2f p" % self.value
+        return ("%s p" % self.value) if isinstance(self.value, str) else ("%.2f p" % self.value)
     def unit(self):
         return "pence"
 
 class KWH:
     def __init__(self, value):
         self.value = value
     def __str__(self):
-        return "%.3f kWh" % self.value
+        return ("%s kWh" % self.value) if isinstance(self.value, str) else ("%.3f kWh" % self.value)
     def unit(self):
         return "kWh"
 
 class Unknown:
     def __init__(self, value):
         self.value = value
     def __str__(self):
```

### Comparing `pyglowmarkt-0.5.5/pyglowmarkt.egg-info/PKG-INFO` & `pyglowmarkt-0.5.6/pyglowmarkt.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: pyglowmarkt
-Version: 0.5.5
+Version: 0.5.6
 Summary: Python API for accessing Hildebrand/Glowmarkt/Bright API to smart meter data
 Home-page: https://github.com/cybermaggedon/pyglowmarkt
 Author: Cybermaggedon
 Author-email: mark@cyberapocalypse.co.uk
 License: UNKNOWN
-Download-URL: https://github.com/cybermaggedon/pyglowmarkt/archive/refs/tags/v0.5.5.tar.gz
+Download-URL: https://github.com/cybermaggedon/pyglowmarkt/archive/refs/tags/v0.5.6.tar.gz
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `pyglowmarkt-0.5.5/scripts/glowmarkt-csv` & `pyglowmarkt-0.5.6/scripts/glowmarkt-csv`

 * *Files identical despite different names*

### Comparing `pyglowmarkt-0.5.5/scripts/glowmarkt-dump` & `pyglowmarkt-0.5.6/scripts/glowmarkt-dump`

 * *Files identical despite different names*

### Comparing `pyglowmarkt-0.5.5/scripts/glowmarkt-mqtt` & `pyglowmarkt-0.5.6/scripts/glowmarkt-mqtt`

 * *Files identical despite different names*

### Comparing `pyglowmarkt-0.5.5/scripts/glowmarkt-today` & `pyglowmarkt-0.5.6/scripts/glowmarkt-today`

 * *Files identical despite different names*

### Comparing `pyglowmarkt-0.5.5/setup.py` & `pyglowmarkt-0.5.6/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,29 +1,29 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="pyglowmarkt",
-    version="0.5.5",
+    version="0.5.6",
     author="Cybermaggedon",
     author_email="mark@cyberapocalypse.co.uk",
     description="Python API for accessing Hildebrand/Glowmarkt/Bright API to smart meter data",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/cybermaggedon/pyglowmarkt",
     packages=setuptools.find_packages(),
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)",
         "Operating System :: OS Independent",
     ],
     python_requires='>=3.6',
-    download_url = "https://github.com/cybermaggedon/pyglowmarkt/archive/refs/tags/v0.5.5.tar.gz",
+    download_url = "https://github.com/cybermaggedon/pyglowmarkt/archive/refs/tags/v0.5.6.tar.gz",
     install_requires=[
         "requests", "paho-mqtt"
     ],
     scripts=[
         "scripts/glowmarkt-dump",
         "scripts/glowmarkt-csv",
         "scripts/glowmarkt-today",
```

