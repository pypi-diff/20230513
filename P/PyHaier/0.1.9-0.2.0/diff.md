# Comparing `tmp/PyHaier-0.1.9.tar.gz` & `tmp/PyHaier-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyHaier-0.1.9.tar", last modified: Fri May 12 18:41:02 2023, max compression
+gzip compressed data, was "PyHaier-0.2.0.tar", last modified: Sat May 13 20:31:42 2023, max compression
```

## Comparing `PyHaier-0.1.9.tar` & `PyHaier-0.2.0.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 jacekb    (1000) jacekb    (1000)        0 2023-05-12 18:41:02.857036 PyHaier-0.1.9/
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)     6051 2023-05-12 18:41:02.857036 PyHaier-0.1.9/PKG-INFO
-drwxr-xr-x   0 jacekb    (1000) jacekb    (1000)        0 2023-05-12 18:41:02.857036 PyHaier-0.1.9/PyHaier/
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      164 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/GetCHTemp.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)       24 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/GetCompFreq.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      174 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/GetDHWCurTemp.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      155 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/GetDHWTemp.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      271 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/GetMode.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      776 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/GetState.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      570 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/GetTwiTwo.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      458 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/SetCHTemp.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      463 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/SetDHWTemp.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      248 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/SetMode.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)     1346 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/SetState.py
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      399 2023-05-12 18:40:49.000000 PyHaier-0.1.9/PyHaier/__init__.py
-drwxr-xr-x   0 jacekb    (1000) jacekb    (1000)        0 2023-05-12 18:41:02.857036 PyHaier-0.1.9/PyHaier.egg-info/
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)     6051 2023-05-12 18:41:02.000000 PyHaier-0.1.9/PyHaier.egg-info/PKG-INFO
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      401 2023-05-12 18:41:02.000000 PyHaier-0.1.9/PyHaier.egg-info/SOURCES.txt
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)        1 2023-05-12 18:41:02.000000 PyHaier-0.1.9/PyHaier.egg-info/dependency_links.txt
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)        8 2023-05-12 18:41:02.000000 PyHaier-0.1.9/PyHaier.egg-info/top_level.txt
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)     5444 2023-05-12 18:40:49.000000 PyHaier-0.1.9/README.md
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)      608 2023-05-12 18:40:49.000000 PyHaier-0.1.9/pyproject.toml
--rw-r--r--   0 jacekb    (1000) jacekb    (1000)       38 2023-05-12 18:41:02.857036 PyHaier-0.1.9/setup.cfg
+drwxr-xr-x   0 jacekb    (1000) jacekb    (1000)        0 2023-05-13 20:31:42.107125 PyHaier-0.2.0/
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)     6164 2023-05-13 20:31:42.107125 PyHaier-0.2.0/PKG-INFO
+drwxr-xr-x   0 jacekb    (1000) jacekb    (1000)        0 2023-05-13 20:31:42.107125 PyHaier-0.2.0/PyHaier/
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      164 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/GetCHTemp.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)       24 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/GetCompFreq.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      174 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/GetDHWCurTemp.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      155 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/GetDHWTemp.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      270 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/GetMode.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      776 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/GetState.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      570 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/GetTwiTwo.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      458 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/SetCHTemp.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      463 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/SetDHWTemp.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      247 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/SetMode.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)     1346 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/SetState.py
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      399 2023-05-13 20:31:25.000000 PyHaier-0.2.0/PyHaier/__init__.py
+drwxr-xr-x   0 jacekb    (1000) jacekb    (1000)        0 2023-05-13 20:31:42.107125 PyHaier-0.2.0/PyHaier.egg-info/
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)     6164 2023-05-13 20:31:42.000000 PyHaier-0.2.0/PyHaier.egg-info/PKG-INFO
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      401 2023-05-13 20:31:42.000000 PyHaier-0.2.0/PyHaier.egg-info/SOURCES.txt
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)        1 2023-05-13 20:31:42.000000 PyHaier-0.2.0/PyHaier.egg-info/dependency_links.txt
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)        8 2023-05-13 20:31:42.000000 PyHaier-0.2.0/PyHaier.egg-info/top_level.txt
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)     5557 2023-05-13 20:31:25.000000 PyHaier-0.2.0/README.md
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)      608 2023-05-13 20:31:25.000000 PyHaier-0.2.0/pyproject.toml
+-rw-r--r--   0 jacekb    (1000) jacekb    (1000)       38 2023-05-13 20:31:42.108126 PyHaier-0.2.0/setup.cfg
```

### Comparing `PyHaier-0.1.9/PKG-INFO` & `PyHaier-0.2.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyHaier
-Version: 0.1.9
+Version: 0.2.0
 Summary: Very simple library to manipulate the basic parameters of the Haier heat pump.
 Author-email: Jacek Brzozowski <jacekbrzozowski.pld@gmail.com>
 Project-URL: Homepage, https://github.com/ktostam/PyHaier
 Project-URL: Bug Tracker, https://github.com/ktostam/PyHaier/issues
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
@@ -25,14 +25,17 @@
 
 [<img width="150px" src="https://buycoffee.to/btn/buycoffeeto-btn-primary.svg">](https://buycoffee.to/jacekbrzozz)
 
 ## Support
 For support, join our Discord channel https://discord.gg/7aF38puD
 
 ## Version
+### 0.2.0
+- rename 'silent' to 'quiet' in GetMode and SetMode function to be consistent with haier nomenclature
+
 ### 0.1.9
 - fix for SetState. Now turning on/off emulate "leaf" button on YR-e27
 
 ### 0.1.8
 - fix for previous fix :D
 
 ### 0.1.7
```

### Comparing `PyHaier-0.1.9/PyHaier/GetState.py` & `PyHaier-0.2.0/PyHaier/GetState.py`

 * *Files identical despite different names*

### Comparing `PyHaier-0.1.9/PyHaier/GetTwiTwo.py` & `PyHaier-0.2.0/PyHaier/GetTwiTwo.py`

 * *Files identical despite different names*

### Comparing `PyHaier-0.1.9/PyHaier/SetState.py` & `PyHaier-0.2.0/PyHaier/SetState.py`

 * *Files identical despite different names*

### Comparing `PyHaier-0.1.9/PyHaier.egg-info/PKG-INFO` & `PyHaier-0.2.0/PyHaier.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyHaier
-Version: 0.1.9
+Version: 0.2.0
 Summary: Very simple library to manipulate the basic parameters of the Haier heat pump.
 Author-email: Jacek Brzozowski <jacekbrzozowski.pld@gmail.com>
 Project-URL: Homepage, https://github.com/ktostam/PyHaier
 Project-URL: Bug Tracker, https://github.com/ktostam/PyHaier/issues
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
@@ -25,14 +25,17 @@
 
 [<img width="150px" src="https://buycoffee.to/btn/buycoffeeto-btn-primary.svg">](https://buycoffee.to/jacekbrzozz)
 
 ## Support
 For support, join our Discord channel https://discord.gg/7aF38puD
 
 ## Version
+### 0.2.0
+- rename 'silent' to 'quiet' in GetMode and SetMode function to be consistent with haier nomenclature
+
 ### 0.1.9
 - fix for SetState. Now turning on/off emulate "leaf" button on YR-e27
 
 ### 0.1.8
 - fix for previous fix :D
 
 ### 0.1.7
```

### Comparing `PyHaier-0.1.9/README.md` & `PyHaier-0.2.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -11,14 +11,17 @@
 
 [<img width="150px" src="https://buycoffee.to/btn/buycoffeeto-btn-primary.svg">](https://buycoffee.to/jacekbrzozz)
 
 ## Support
 For support, join our Discord channel https://discord.gg/7aF38puD
 
 ## Version
+### 0.2.0
+- rename 'silent' to 'quiet' in GetMode and SetMode function to be consistent with haier nomenclature
+
 ### 0.1.9
 - fix for SetState. Now turning on/off emulate "leaf" button on YR-e27
 
 ### 0.1.8
 - fix for previous fix :D
 
 ### 0.1.7
```

### Comparing `PyHaier-0.1.9/pyproject.toml` & `PyHaier-0.2.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "PyHaier"
-version = "0.1.9"
+version = "0.2.0"
 authors = [
   { name="Jacek Brzozowski", email="jacekbrzozowski.pld@gmail.com" },
 ]
 description = "Very simple library to manipulate the basic parameters of the Haier heat pump."
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

