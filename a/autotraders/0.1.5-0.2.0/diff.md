# Comparing `tmp/autotraders-0.1.5.tar.gz` & `tmp/autotraders-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "autotraders-0.1.5.tar", last modified: Fri May 12 17:33:13 2023, max compression
+gzip compressed data, was "autotraders-0.2.0.tar", last modified: Fri May 12 19:45:27 2023, max compression
```

## Comparing `autotraders-0.1.5.tar` & `autotraders-0.2.0.tar`

### file list

```diff
@@ -1,18 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:33:13.556688 autotraders-0.1.5/
--rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-12 17:33:01.000000 autotraders-0.1.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1315 2023-05-12 17:33:13.556688 autotraders-0.1.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-12 17:33:01.000000 autotraders-0.1.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:33:13.552688 autotraders-0.1.5/autotraders/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 17:33:01.000000 autotraders-0.1.5/autotraders/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      778 2023-05-12 17:33:01.000000 autotraders-0.1.5/autotraders/agent.py
--rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-05-12 17:33:01.000000 autotraders-0.1.5/autotraders/contract.py
--rw-r--r--   0 runner    (1001) docker     (123)     5318 2023-05-12 17:33:01.000000 autotraders-0.1.5/autotraders/ships.py
--rw-r--r--   0 runner    (1001) docker     (123)     1122 2023-05-12 17:33:01.000000 autotraders-0.1.5/autotraders/system.py
--rw-r--r--   0 runner    (1001) docker     (123)     1510 2023-05-12 17:33:01.000000 autotraders-0.1.5/autotraders/waypoint.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 17:33:13.556688 autotraders-0.1.5/autotraders.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1315 2023-05-12 17:33:13.000000 autotraders-0.1.5/autotraders.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      308 2023-05-12 17:33:13.000000 autotraders-0.1.5/autotraders.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 17:33:13.000000 autotraders-0.1.5/autotraders.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-12 17:33:13.000000 autotraders-0.1.5/autotraders.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-12 17:33:01.000000 autotraders-0.1.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 17:33:13.556688 autotraders-0.1.5/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 19:45:27.100387 autotraders-0.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-12 19:45:14.000000 autotraders-0.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1315 2023-05-12 19:45:27.100387 autotraders-0.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-12 19:45:14.000000 autotraders-0.2.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 19:45:27.100387 autotraders-0.2.0/autotraders/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      778 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/agent.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/contract.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/marketplace.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6004 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/ships.py
+-rw-r--r--   0 runner    (1001) docker     (123)      753 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/shipyard.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1122 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/system.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1771 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/waypoint.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 19:45:27.100387 autotraders-0.2.0/autotraders.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1315 2023-05-12 19:45:27.000000 autotraders-0.2.0/autotraders.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      359 2023-05-12 19:45:27.000000 autotraders-0.2.0/autotraders.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 19:45:27.000000 autotraders-0.2.0/autotraders.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-12 19:45:27.000000 autotraders-0.2.0/autotraders.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-12 19:45:14.000000 autotraders-0.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 19:45:27.100387 autotraders-0.2.0/setup.cfg
```

### Comparing `autotraders-0.1.5/LICENSE` & `autotraders-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `autotraders-0.1.5/PKG-INFO` & `autotraders-0.2.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: autotraders
-Version: 0.1.5
+Version: 0.2.0
 Summary: A powerful spacetraders API
 Author-email: Ashwin Naren <arihant2math@gmail.com>
 Project-URL: Homepage, https://github.com/arihant2math/autotraders
 Project-URL: Bug Tracker, https://github.com/arihant2math/autotraders/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `autotraders-0.1.5/README.md` & `autotraders-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `autotraders-0.1.5/autotraders/agent.py` & `autotraders-0.2.0/autotraders/agent.py`

 * *Files identical despite different names*

### Comparing `autotraders-0.1.5/autotraders/contract.py` & `autotraders-0.2.0/autotraders/contract.py`

 * *Files identical despite different names*

### Comparing `autotraders-0.1.5/autotraders/ships.py` & `autotraders-0.2.0/autotraders/ships.py`

 * *Files 4% similar despite different names*

```diff
@@ -150,14 +150,36 @@
                 "shipSymbol": destination,
             },
         ).json()
         if "error" in j:
             raise IOError(j["error"]["message"])
         self.update()
 
+    def jump(self, destination: str):
+        j = self.session.post(
+            "https://api.spacetraders.io/v2/my/ships/" + self.symbol + "/jump",
+            data={
+                "systemSymbol": destination,
+            },
+        ).json()
+        if "error" in j:
+            raise IOError(j["error"]["message"])
+        self.update()
+
+    def warp(self, destination: str):
+        j = self.session.post(
+            "https://api.spacetraders.io/v2/my/ships/" + self.symbol + "/warp",
+            data={
+                "waypointSymbol": destination,
+            },
+        ).json()
+        if "error" in j:
+            raise IOError(j["error"]["message"])
+        self.update()
+
 
 def get_all_ships(session):
     r = session.get("https://api.spacetraders.io/v2/my/ships")
     j = r.json()
     if "error" in j:
         raise IOError(j["error"]["message"])
     ships = []
```

### Comparing `autotraders-0.1.5/autotraders/system.py` & `autotraders-0.2.0/autotraders/system.py`

 * *Files identical despite different names*

### Comparing `autotraders-0.1.5/autotraders/waypoint.py` & `autotraders-0.2.0/autotraders/waypoint.py`

 * *Files 16% similar despite different names*

```diff
@@ -8,14 +8,16 @@
         return self.name
 
 
 class Waypoint:
     def __init__(self, symbol, session, update=True):
         self.session = session
         self.symbol = symbol
+        self.marketplace = False
+        self.shipyard = False
         if update:
             self.update()
 
     def update(self, data=None):
         if data is None:
             split = self.symbol.split("-")
             system_symbol = split[0] + "-" + split[1]
@@ -33,14 +35,16 @@
             self.faction = data["faction"]["symbol"]
         else:
             self.faction = None
         self.traits = []
         if "traits" in data:
             for trait in data["traits"]:
                 self.traits.append(Trait(trait))
+        self.marketplace = len([trait for trait in self.traits if trait.symbol == "MARKETPLACE"]) > 0
+        self.shipyard = len([trait for trait in self.traits if trait.symbol == "SHIPYARD"]) > 0
 
 
 def get_all_waypoints(system, session):
     r = session.get("https://api.spacetraders.io/v2/systems/" + system + "/waypoints")
     data = r.json()["data"]
     waypoints = []
     for w in data:
```

### Comparing `autotraders-0.1.5/autotraders.egg-info/PKG-INFO` & `autotraders-0.2.0/autotraders.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: autotraders
-Version: 0.1.5
+Version: 0.2.0
 Summary: A powerful spacetraders API
 Author-email: Ashwin Naren <arihant2math@gmail.com>
 Project-URL: Homepage, https://github.com/arihant2math/autotraders
 Project-URL: Bug Tracker, https://github.com/arihant2math/autotraders/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `autotraders-0.1.5/pyproject.toml` & `autotraders-0.2.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 [project]
 name = "autotraders"
-version = "0.1.5"
+version = "0.2.0"
 authors = [
   { name="Ashwin Naren", email="arihant2math@gmail.com" },
 ]
 description = "A powerful spacetraders API"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

