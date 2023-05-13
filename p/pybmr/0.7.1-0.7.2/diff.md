# Comparing `tmp/pybmr-0.7.1.tar.gz` & `tmp/pybmr-0.7.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/pybmr-0.7.1.tar", last modified: Sun Jul 12 07:30:17 2020, max compression
+gzip compressed data, was "pybmr-0.7.2.tar", last modified: Sat May 13 15:45:11 2023, max compression
```

## Comparing `pybmr-0.7.1.tar` & `pybmr-0.7.2.tar`

### file list

```diff
@@ -1,20 +1,21 @@
-drwxr-xr-x   0 jslesing  (1000) jslesing  (1000)        0 2020-07-12 07:30:17.000000 pybmr-0.7.1/
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)       55 2020-07-12 07:29:15.000000 pybmr-0.7.1/MANIFEST.in
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)     5342 2020-07-12 07:30:17.000000 pybmr-0.7.1/PKG-INFO
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)     3373 2020-07-12 06:46:10.000000 pybmr-0.7.1/README.md
-drwxr-xr-x   0 jslesing  (1000) jslesing  (1000)        0 2020-07-12 07:30:17.000000 pybmr-0.7.1/pybmr/
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)    23478 2020-07-12 06:46:10.000000 pybmr-0.7.1/pybmr/__init__.py
-drwxr-xr-x   0 jslesing  (1000) jslesing  (1000)        0 2020-07-12 07:30:17.000000 pybmr-0.7.1/pybmr.egg-info/
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)     5342 2020-07-12 07:30:17.000000 pybmr-0.7.1/pybmr.egg-info/PKG-INFO
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)      287 2020-07-12 07:30:17.000000 pybmr-0.7.1/pybmr.egg-info/SOURCES.txt
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)        1 2020-07-12 07:30:17.000000 pybmr-0.7.1/pybmr.egg-info/dependency_links.txt
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)      120 2020-07-12 07:30:17.000000 pybmr-0.7.1/pybmr.egg-info/requires.txt
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)       12 2020-07-12 07:30:17.000000 pybmr-0.7.1/pybmr.egg-info/top_level.txt
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)      468 2020-07-12 06:48:40.000000 pybmr-0.7.1/requirements.txt
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)       38 2020-07-12 07:30:17.000000 pybmr-0.7.1/setup.cfg
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)      969 2020-07-12 07:24:36.000000 pybmr-0.7.1/setup.py
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)      653 2020-07-12 06:46:10.000000 pybmr-0.7.1/test-requirements.txt
-drwxr-xr-x   0 jslesing  (1000) jslesing  (1000)        0 2020-07-12 07:30:17.000000 pybmr-0.7.1/tests/
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)        0 2020-07-12 06:46:10.000000 pybmr-0.7.1/tests/__init__.py
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)     2838 2020-07-12 06:46:10.000000 pybmr-0.7.1/tests/conftest.py
--rw-r--r--   0 jslesing  (1000) jslesing  (1000)     3822 2020-07-12 06:46:10.000000 pybmr-0.7.1/tests/test_pybmr.py
+drwxrwxr-x   0 honza     (1000) honza     (1000)        0 2023-05-13 15:45:11.771673 pybmr-0.7.2/
+-rw-rw-r--   0 honza     (1000) honza     (1000)    11356 2023-05-13 15:38:50.000000 pybmr-0.7.2/LICENSE.md
+-rw-rw-r--   0 honza     (1000) honza     (1000)       55 2023-05-13 15:38:50.000000 pybmr-0.7.2/MANIFEST.in
+-rw-rw-r--   0 honza     (1000) honza     (1000)     4154 2023-05-13 15:45:11.771673 pybmr-0.7.2/PKG-INFO
+-rw-rw-r--   0 honza     (1000) honza     (1000)     3696 2023-05-13 15:38:50.000000 pybmr-0.7.2/README.md
+drwxrwxr-x   0 honza     (1000) honza     (1000)        0 2023-05-13 15:45:11.771673 pybmr-0.7.2/pybmr/
+-rw-rw-r--   0 honza     (1000) honza     (1000)    23824 2023-05-13 15:38:50.000000 pybmr-0.7.2/pybmr/__init__.py
+drwxrwxr-x   0 honza     (1000) honza     (1000)        0 2023-05-13 15:45:11.771673 pybmr-0.7.2/pybmr.egg-info/
+-rw-rw-r--   0 honza     (1000) honza     (1000)     4154 2023-05-13 15:45:11.000000 pybmr-0.7.2/pybmr.egg-info/PKG-INFO
+-rw-rw-r--   0 honza     (1000) honza     (1000)      298 2023-05-13 15:45:11.000000 pybmr-0.7.2/pybmr.egg-info/SOURCES.txt
+-rw-rw-r--   0 honza     (1000) honza     (1000)        1 2023-05-13 15:45:11.000000 pybmr-0.7.2/pybmr.egg-info/dependency_links.txt
+-rw-rw-r--   0 honza     (1000) honza     (1000)      132 2023-05-13 15:45:11.000000 pybmr-0.7.2/pybmr.egg-info/requires.txt
+-rw-rw-r--   0 honza     (1000) honza     (1000)       12 2023-05-13 15:45:11.000000 pybmr-0.7.2/pybmr.egg-info/top_level.txt
+-rw-rw-r--   0 honza     (1000) honza     (1000)      478 2023-05-13 15:41:33.000000 pybmr-0.7.2/requirements.txt
+-rw-rw-r--   0 honza     (1000) honza     (1000)       38 2023-05-13 15:45:11.771673 pybmr-0.7.2/setup.cfg
+-rw-rw-r--   0 honza     (1000) honza     (1000)      969 2023-05-13 15:44:49.000000 pybmr-0.7.2/setup.py
+-rw-rw-r--   0 honza     (1000) honza     (1000)      656 2023-05-13 15:38:50.000000 pybmr-0.7.2/test-requirements.txt
+drwxrwxr-x   0 honza     (1000) honza     (1000)        0 2023-05-13 15:45:11.771673 pybmr-0.7.2/tests/
+-rw-rw-r--   0 honza     (1000) honza     (1000)        0 2023-05-13 15:38:50.000000 pybmr-0.7.2/tests/__init__.py
+-rw-rw-r--   0 honza     (1000) honza     (1000)     2838 2023-05-13 15:38:50.000000 pybmr-0.7.2/tests/conftest.py
+-rw-rw-r--   0 honza     (1000) honza     (1000)     3822 2023-05-13 15:38:50.000000 pybmr-0.7.2/tests/test_pybmr.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `pybmr-0.7.1/README.md` & `pybmr-0.7.2/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 # PyBmr
 
 Python library for communication with BMR HC64 Heating Controller units.
 
-Product website: https://bmr.cz/produkty/regulace-topeni/rnet
-
+Product website: 
+ - https://bmr.cz/produkty/regulace-topeni/rnet
+ - https://bmr.cz/produkty/regulace-topeni/rt64
 
 ## Install:
 
 ```
 python3 -m pip install pybmr
 ```
 
@@ -29,15 +30,15 @@
 numCircuits = bmr.getNumCircuits()
 ```
 
 Load circuit status:
 
 ```
 circuit = bmr.getCircuit(0)
-print(f"Circuit {circuit['name']}: temperature is {circuit['temperature']} °C, target temperature is {circuit['target_temperature'} °C")
+print(f"Circuit {circuit['name']}: temperature is {circuit['temperature']} °C, target temperature is {circuit['target_temperature']} °C")
 ```
 
 Load circuit schedules (what schedule is assigned to what day). It is possible to assign a different schedule for up to 21 days.
 
 ```
 circuit_schedules = bmr.getCircuitSchedules(0)
 print(f"Circuit 0 schedule for the first day is {circuit_schedules['day_schedules'][0]}")
@@ -180,7 +181,11 @@
 ```
 hdo = bmr.getHDO()
 if hdo:
   print("HDO is currently ON")
 else:
   print("HDO is currently OFF")
 ```
+
+## Backup of BMR Controler Unit Configuration
+
+There is a CLI tool that can be used to backup configuration of actual BMR Controler Unit. It can be used in automations or just as a remote management tool. For more information refer to https://github.com/dankeder/bmrcli
```

### Comparing `pybmr-0.7.1/pybmr/__init__.py` & `pybmr-0.7.2/pybmr/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -201,38 +201,47 @@
             "id": circuit_id,
             "enabled": bool(int(room_status["enabled"])),
             "name": room_status["name"].rstrip(),
             "temperature": None,
             "target_temperature": None,
             "user_offset": None,
             "max_offset": None,
-            "heating": bool(int(room_status["heating"])),
-            "warning": int(room_status["warning"]),
-            "cooling": bool(int(room_status["cooling"])),
-            "low_mode": bool(int(room_status["low_mode"])),
-            "summer_mode": bool(int(room_status["summer_mode"])),
+            "heating": False,
+            "warning": 0,
+            "cooling": False,
+            "low_mode": False,
+            "summer_mode": False,
         }
 
-        try:
-            result["temperature"] = float(room_status["temperature"])
-        except ValueError:
-            pass
-
-        try:
-            result["target_temperature"] = float(room_status["target_temperature"])
-        except ValueError:
-            pass
-
-        try:
-            result["user_offset"] = float(room_status["user_offset"])
-        except ValueError:
-            pass
+        for key in (
+            "temperature",
+            "heating",
+            "cooling",
+            "warning",
+            "low_mode",
+            "summer_mode",
+            "user_offset",
+            "max_offset",
+        ):
+            try:
+                result[key] = float(room_status[key])
+            except ValueError:
+                pass
 
         try:
-            result["max_offset"] = float(room_status["max_offset"])
+            # If summer mode is turned on (which means the system is powered
+            # down) we will return target temperature as `None`, not 0 degrees
+            #
+            # Also ignore and set it to None if target temperature is 0
+            # degrees. That is most likely a nonsense reported when the
+            # heating controller is reloading configuration.
+            if not bool(int(room_status["summer_mode"])):
+                result["target_temperature"] = float(room_status["target_temperature"]) or None
+            else:
+                result["target_temperature"] = None
         except ValueError:
             pass
 
         return result
 
     @ttl_cache(maxsize=CACHE_DEFAULT_MAXSIZE, ttl=CACHE_DEFAULT_TTL)
     @authenticated
```

### Comparing `pybmr-0.7.1/setup.py` & `pybmr-0.7.2/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -7,15 +7,15 @@
     install_requires = [line for line in fh if line and line[0] not in "#-"]
 
 with open("test-requirements.txt") as fh:
     tests_require = [line for line in fh if line and line[0] not in "#-"]
 
 setuptools.setup(
     name="pybmr",
-    version="0.7.1",
+    version="0.7.2",
     author="Honza Slesinger",
     author_email="slesinger@gmail.com",
     description="Python library for communication with BMR HC64 Heating Controller units",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/slesinger/pybmr",
     packages=setuptools.find_packages(),
```

### Comparing `pybmr-0.7.1/tests/conftest.py` & `pybmr-0.7.2/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `pybmr-0.7.1/tests/test_pybmr.py` & `pybmr-0.7.2/tests/test_pybmr.py`

 * *Files identical despite different names*

