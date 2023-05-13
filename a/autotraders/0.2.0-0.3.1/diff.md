# Comparing `tmp/autotraders-0.2.0.tar.gz` & `tmp/autotraders-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "autotraders-0.2.0.tar", last modified: Fri May 12 19:45:27 2023, max compression
+gzip compressed data, was "autotraders-0.3.1.tar", last modified: Fri May 12 22:29:28 2023, max compression
```

## Comparing `autotraders-0.2.0.tar` & `autotraders-0.3.1.tar`

### file list

```diff
@@ -1,20 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 19:45:27.100387 autotraders-0.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-12 19:45:14.000000 autotraders-0.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1315 2023-05-12 19:45:27.100387 autotraders-0.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-12 19:45:14.000000 autotraders-0.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 19:45:27.100387 autotraders-0.2.0/autotraders/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      778 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/agent.py
--rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/contract.py
--rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/marketplace.py
--rw-r--r--   0 runner    (1001) docker     (123)     6004 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/ships.py
--rw-r--r--   0 runner    (1001) docker     (123)      753 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/shipyard.py
--rw-r--r--   0 runner    (1001) docker     (123)     1122 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/system.py
--rw-r--r--   0 runner    (1001) docker     (123)     1771 2023-05-12 19:45:14.000000 autotraders-0.2.0/autotraders/waypoint.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 19:45:27.100387 autotraders-0.2.0/autotraders.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1315 2023-05-12 19:45:27.000000 autotraders-0.2.0/autotraders.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      359 2023-05-12 19:45:27.000000 autotraders-0.2.0/autotraders.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 19:45:27.000000 autotraders-0.2.0/autotraders.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-12 19:45:27.000000 autotraders-0.2.0/autotraders.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-12 19:45:14.000000 autotraders-0.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 19:45:27.100387 autotraders-0.2.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:29:28.796717 autotraders-0.3.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-12 22:29:13.000000 autotraders-0.3.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1819 2023-05-12 22:29:28.796717 autotraders-0.3.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1227 2023-05-12 22:29:13.000000 autotraders-0.3.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:29:28.792716 autotraders-0.3.1/autotraders/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      777 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/agent.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/contract.py
+-rw-r--r--   0 runner    (1001) docker     (123)      989 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/faction.py
+-rw-r--r--   0 runner    (1001) docker     (123)      945 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/marketplace.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6816 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/ship.py
+-rw-r--r--   0 runner    (1001) docker     (123)      960 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/shipyard.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1122 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/system.py
+-rw-r--r--   0 runner    (1001) docker     (123)      209 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/trait.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1598 2023-05-12 22:29:13.000000 autotraders-0.3.1/autotraders/waypoint.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:29:28.796717 autotraders-0.3.1/autotraders.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1819 2023-05-12 22:29:28.000000 autotraders-0.3.1/autotraders.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      402 2023-05-12 22:29:28.000000 autotraders-0.3.1/autotraders.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:29:28.000000 autotraders-0.3.1/autotraders.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-12 22:29:28.000000 autotraders-0.3.1/autotraders.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      760 2023-05-12 22:29:13.000000 autotraders-0.3.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 22:29:28.796717 autotraders-0.3.1/setup.cfg
```

### Comparing `autotraders-0.2.0/LICENSE` & `autotraders-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `autotraders-0.2.0/PKG-INFO` & `autotraders-0.3.1/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 Metadata-Version: 2.1
 Name: autotraders
-Version: 0.2.0
+Version: 0.3.1
 Summary: A powerful spacetraders API
 Author-email: Ashwin Naren <arihant2math@gmail.com>
-Project-URL: Homepage, https://github.com/arihant2math/autotraders
+Project-URL: Homepage, https://arihant2math.github.io/autotraders/
+Project-URL: Documentation, https://arihant2math.github.io/autotraders/
 Project-URL: Bug Tracker, https://github.com/arihant2math/autotraders/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -33,15 +34,29 @@
 s.auth = BearerAuth(token)
 ```
 And now you're all set to use they actual API.
 
 ## Ships
 
 ```python
-from autotraders.ships import Ship
+from autotraders.ship import Ship, get_all_ships
+
 # create a session here
-ship = Ship("SYMBOL-Here", session) # This makes an API request
+ship = Ship("SYMBOL-Here", session)  # This makes an API request
+ships = get_all_ships(session)  # This also only makes one API request
 ship.dock()
 ship.refuel()
-ship.orbit() # All these functions make API calls (one each), but the line below doesn't
+ship.orbit()  # All these functions make API calls (one each), but the line below doesn't
 print(ship.fuel.current + "/" + ship.fuel.total)
 ```
+## Contract
+```python
+from autotraders.contract import Contract, get_all_contracts
+# create a session here
+contract = Contract("id-here", session)
+contracts = get_all_contracts(session)
+contract.accept()
+print(contract.accepted) # True
+contract.deliver("SHIP_SYMBOL", "ALUMINUM_ORE", 30)
+contract.fulfill()
+print(contract.fulfilled) # True
+```
```

### Comparing `autotraders-0.2.0/autotraders/agent.py` & `autotraders-0.3.1/autotraders/agent.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from autotraders.ships import get_all_ships
+from autotraders.ship import get_all_ships
 from autotraders.contract import get_all_contracts
 
 
 class Agent:
     def __init__(self, session, update=True):
         self.session = session
         if update:
```

### Comparing `autotraders-0.2.0/autotraders/contract.py` & `autotraders-0.3.1/autotraders/contract.py`

 * *Files identical despite different names*

### Comparing `autotraders-0.2.0/autotraders/marketplace.py` & `autotraders-0.3.1/autotraders/marketplace.py`

 * *Files 22% similar despite different names*

```diff
@@ -8,18 +8,17 @@
     def update(self, data: dict = None):
         if data is None:
             split = self.location.split("-")
             system_symbol = split[0] + "-" + split[1]
             waypoint_symbol = self.location
             data = self.session.get("https://api.spacetraders.io/v2/systems/"
                                     + system_symbol + "/waypoints/"
-                                    + waypoint_symbol + "/marketplace").json()["data"]
-            print(data)
+                                    + waypoint_symbol + "/market").json()["data"]
         self.imports = []
         for i in data["imports"]:
-            self.imports.append(data["imports"]["symbol"])
+            self.imports.append(i["symbol"])
         self.exports = []
         for i in data["exports"]:
-            self.exports.append(data["exports"]["symbol"])
+            self.exports.append(i["symbol"])
         self.exchange = []
         for i in data["exchange"]:
-            self.exchange.append(data["exchange"]["symbol"])
+            self.exchange.append(i["symbol"])
```

### Comparing `autotraders-0.2.0/autotraders/ships.py` & `autotraders-0.3.1/autotraders/ship.py`

 * *Files 19% similar despite different names*

```diff
@@ -51,28 +51,38 @@
             self.location = data["nav"]["waypointSymbol"]
         if "fuel" in data:
             self.fuel = Fuel(data["fuel"]["current"], data["fuel"]["capacity"])
         if "cargo" in data:
             self.cargo = Cargo(data["cargo"])
 
     async def move_async(self, waypoint):
+        """Attempts to move ship to the provided waypoint.
+        If the request succeeds, this function waits for the ship to arrive.
+            :raise:
+                IOError: if a server error occurs
+        """
         r = self.session.post(
             "https://api.spacetraders.io/v2/my/ships/" + self.symbol + "/navigate",
             data={"waypointSymbol": waypoint},
         )
         j = r.json()
         if "error" in j:
             raise j["error"]["message"]
         await asyncio.sleep(5)
         self.update()
         while self.status == "IN_TRANSIT":
             await asyncio.sleep(5)
             self.update()
 
     def move(self, waypoint):
+        """Attempts to move ship to the provided waypoint.
+        If the request succeeds, this function exits immediately, and does not wait the ship to arrive.
+            :raise:
+                IOError: if a server error occurs
+        """
         r = self.session.post(
             "https://api.spacetraders.io/v2/my/ships/" + self.symbol + "/navigate",
             data={"waypointSymbol": waypoint},
         )
         j = r.json()
         if "error" in j:
             raise IOError(j["error"]["message"])
@@ -172,14 +182,23 @@
                 "waypointSymbol": destination,
             },
         ).json()
         if "error" in j:
             raise IOError(j["error"]["message"])
         self.update()
 
+    def jettison(self, cargo_symbol: str, quantity: int):
+        j = self.session.post(
+            "https://api.spacetraders.io/v2/my/ships/" + self.symbol + "/jettison",
+            data={"symbol": cargo_symbol, "units": quantity},
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

### Comparing `autotraders-0.2.0/autotraders/shipyard.py` & `autotraders-0.3.1/autotraders/shipyard.py`

 * *Files 16% similar despite different names*

```diff
@@ -12,7 +12,13 @@
             waypoint_symbol = self.location
             data = self.session.get("https://api.spacetraders.io/v2/systems/"
                                     + system_symbol + "/waypoints/"
                                     + waypoint_symbol + "/shipyard").json()["data"]
         self.ship_types = []
         for ship_type in data["shipTypes"]:
             self.ship_types.append(ship_type["type"])
+
+    def purchase(self, ship_type: str):
+        self.session.post("https://api.spacetraders.io/v2/my/ships", data={
+            "shipType": ship_type,
+            "waypointSymbol": self.location
+        })
```

### Comparing `autotraders-0.2.0/autotraders/system.py` & `autotraders-0.3.1/autotraders/system.py`

 * *Files identical despite different names*

### Comparing `autotraders-0.2.0/autotraders/waypoint.py` & `autotraders-0.3.1/autotraders/waypoint.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,15 +1,8 @@
-class Trait:
-    def __init__(self, data):
-        self.symbol = data["symbol"]
-        self.name = data["name"]
-        self.description = data["description"]
-
-    def __str__(self):
-        return self.name
+from autotraders.trait import Trait
 
 
 class Waypoint:
     def __init__(self, symbol, session, update=True):
         self.session = session
         self.symbol = symbol
         self.marketplace = False
```

### Comparing `autotraders-0.2.0/autotraders.egg-info/PKG-INFO` & `autotraders-0.3.1/autotraders.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 Metadata-Version: 2.1
 Name: autotraders
-Version: 0.2.0
+Version: 0.3.1
 Summary: A powerful spacetraders API
 Author-email: Ashwin Naren <arihant2math@gmail.com>
-Project-URL: Homepage, https://github.com/arihant2math/autotraders
+Project-URL: Homepage, https://arihant2math.github.io/autotraders/
+Project-URL: Documentation, https://arihant2math.github.io/autotraders/
 Project-URL: Bug Tracker, https://github.com/arihant2math/autotraders/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -33,15 +34,29 @@
 s.auth = BearerAuth(token)
 ```
 And now you're all set to use they actual API.
 
 ## Ships
 
 ```python
-from autotraders.ships import Ship
+from autotraders.ship import Ship, get_all_ships
+
 # create a session here
-ship = Ship("SYMBOL-Here", session) # This makes an API request
+ship = Ship("SYMBOL-Here", session)  # This makes an API request
+ships = get_all_ships(session)  # This also only makes one API request
 ship.dock()
 ship.refuel()
-ship.orbit() # All these functions make API calls (one each), but the line below doesn't
+ship.orbit()  # All these functions make API calls (one each), but the line below doesn't
 print(ship.fuel.current + "/" + ship.fuel.total)
 ```
+## Contract
+```python
+from autotraders.contract import Contract, get_all_contracts
+# create a session here
+contract = Contract("id-here", session)
+contracts = get_all_contracts(session)
+contract.accept()
+print(contract.accepted) # True
+contract.deliver("SHIP_SYMBOL", "ALUMINUM_ORE", 30)
+contract.fulfill()
+print(contract.fulfilled) # True
+```
```

### Comparing `autotraders-0.2.0/pyproject.toml` & `autotraders-0.3.1/pyproject.toml`

 * *Files 22% similar despite different names*

```diff
@@ -1,23 +1,28 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
+
 [project]
 name = "autotraders"
-version = "0.2.0"
+version = "0.3.1"
 authors = [
   { name="Ashwin Naren", email="arihant2math@gmail.com" },
 ]
 description = "A powerful spacetraders API"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 
+[tool.setuptools.packages.find]
+include = ["autotraders*"]
+exclude = ["source*", "tests*", "venv*"]
 
 [project.urls]
-"Homepage" = "https://github.com/arihant2math/autotraders"
+"Homepage" = "https://arihant2math.github.io/autotraders/"
+"Documentation" = "https://arihant2math.github.io/autotraders/"
 "Bug Tracker" = "https://github.com/arihant2math/autotraders/issues"
```

