# Comparing `tmp/astrotraders-1.0.0.tar.gz` & `tmp/astrotraders-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "astrotraders-1.0.0.tar", max compression
+gzip compressed data, was "astrotraders-1.0.1.tar", max compression
```

## Comparing `astrotraders-1.0.0.tar` & `astrotraders-1.0.1.tar`

### file list

```diff
@@ -1,19 +1,18 @@
--rw-r--r--   0        0        0       56 2023-05-12 20:52:18.679327 astrotraders-1.0.0/astrotraders/__init__.py
--rw-r--r--   0        0        0        0 2023-05-12 19:47:31.879410 astrotraders-1.0.0/astrotraders/api/__init__.py
--rw-r--r--   0        0        0     1219 2023-05-12 23:29:41.212209 astrotraders-1.0.0/astrotraders/api/client.py
--rw-r--r--   0        0        0      693 2023-05-12 23:17:21.140711 astrotraders-1.0.0/astrotraders/api/exceptions.py
--rw-r--r--   0        0        0      190 2023-05-12 20:46:41.786968 astrotraders-1.0.0/astrotraders/api/resources/__init__.py
--rw-r--r--   0        0        0      327 2023-05-12 21:53:20.054870 astrotraders-1.0.0/astrotraders/api/resources/agents.py
--rw-r--r--   0        0        0      166 2023-05-12 20:46:41.721439 astrotraders-1.0.0/astrotraders/api/resources/base.py
--rw-r--r--   0        0        0     1834 2023-05-12 21:57:13.740349 astrotraders-1.0.0/astrotraders/api/resources/contracts.py
--rw-r--r--   0        0        0      703 2023-05-12 21:57:39.759783 astrotraders-1.0.0/astrotraders/api/resources/factions.py
--rw-r--r--   0        0        0    11757 2023-05-12 23:29:41.310477 astrotraders-1.0.0/astrotraders/api/resources/fleet.py
--rw-r--r--   0        0        0     3324 2023-05-12 22:04:13.250467 astrotraders-1.0.0/astrotraders/api/resources/systems.py
--rw-r--r--   0        0        0    38492 2023-05-12 23:29:41.811438 astrotraders-1.0.0/astrotraders/api/schemas.py
--rw-r--r--   0        0        0      528 2023-05-12 23:12:54.081583 astrotraders-1.0.0/astrotraders/api/utils.py
--rw-r--r--   0        0        0     3114 2023-05-12 23:29:41.266963 astrotraders-1.0.0/astrotraders/api/wrapper.py
--rw-r--r--   0        0        0        0 2023-05-12 21:21:52.305976 astrotraders-1.0.0/astrotraders/py.typed
--rw-r--r--   0        0        0     1022 2023-05-12 23:45:26.354630 astrotraders-1.0.0/pyproject.toml
--rw-r--r--   0        0        0      953 2023-05-13 00:06:10.805560 astrotraders-1.0.0/README.md
--rw-r--r--   0        0        0     1700 1970-01-01 00:00:00.000000 astrotraders-1.0.0/setup.py
--rw-r--r--   0        0        0     1427 1970-01-01 00:00:00.000000 astrotraders-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0      917 2023-05-13 12:25:45.027449 astrotraders-1.0.1/README.md
+-rw-r--r--   0        0        0       55 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/__init__.py
+-rw-r--r--   0        0        0     1181 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/client.py
+-rw-r--r--   0        0        0      670 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/exceptions.py
+-rw-r--r--   0        0        0      185 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/resources/__init__.py
+-rw-r--r--   0        0        0      317 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/resources/agents.py
+-rw-r--r--   0        0        0      160 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/resources/base.py
+-rw-r--r--   0        0        0     1776 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/resources/contracts.py
+-rw-r--r--   0        0        0      682 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/resources/factions.py
+-rw-r--r--   0        0        0    11413 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/resources/fleet.py
+-rw-r--r--   0        0        0     3227 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/resources/systems.py
+-rw-r--r--   0        0        0    37202 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/schemas.py
+-rw-r--r--   0        0        0      509 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/utils.py
+-rw-r--r--   0        0        0     3020 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/api/wrapper.py
+-rw-r--r--   0        0        0        0 2023-05-13 12:25:45.027449 astrotraders-1.0.1/astrotraders/py.typed
+-rw-r--r--   0        0        0     1146 2023-05-13 12:25:45.027449 astrotraders-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0     1735 1970-01-01 00:00:00.000000 astrotraders-1.0.1/PKG-INFO
```

### Comparing `astrotraders-1.0.0/astrotraders/api/client.py` & `astrotraders-1.0.1/astrotraders/api/client.py`

 * *Ordering differences only*

 * *Files 13% similar despite different names*

```diff
@@ -1,38 +1,38 @@
-from typing import TYPE_CHECKING, cast
-
-from httpx import Client
-
-from astrotraders.api.resources import (
-    AgentsResource,
-    SystemsResource,
-    ContractsResource,
-    FactionsResource,
-    FleetResource,
-)
-from astrotraders.api.exceptions import exception_hook
-from astrotraders.api.wrapper import HttpxClientWrapper
-
-
-class AstroTradersClient:
-    def __init__(self, httpx_instance: Client):
-        self._httpx_instance = httpx_instance
-        self._client = HttpxClientWrapper(self._httpx_instance)
-        self.agents = AgentsResource(self._client)
-        self.systems = SystemsResource(self._client)
-        self.contracts = ContractsResource(self._client)
-        self.factions = FactionsResource(self._client)
-        self.fleet = FleetResource(self._client)
-
-    @classmethod
-    def set_up(
-        cls, token: str, url: str = "https://api.spacetraders.io/v2"
-    ) -> "AstroTradersClient":
-        client = Client(
-            base_url=url,
-            event_hooks={"response": [exception_hook]},
-            headers={"Authorization": f"Bearer {token}"},
-        )
-        return cls(client)
-
-    def close(self) -> "None":
-        self._httpx_instance.close()
+from typing import TYPE_CHECKING, cast
+
+from httpx import Client
+
+from astrotraders.api.resources import (
+    AgentsResource,
+    SystemsResource,
+    ContractsResource,
+    FactionsResource,
+    FleetResource,
+)
+from astrotraders.api.exceptions import exception_hook
+from astrotraders.api.wrapper import HttpxClientWrapper
+
+
+class AstroTradersClient:
+    def __init__(self, httpx_instance: Client):
+        self._httpx_instance = httpx_instance
+        self._client = HttpxClientWrapper(self._httpx_instance)
+        self.agents = AgentsResource(self._client)
+        self.systems = SystemsResource(self._client)
+        self.contracts = ContractsResource(self._client)
+        self.factions = FactionsResource(self._client)
+        self.fleet = FleetResource(self._client)
+
+    @classmethod
+    def set_up(
+        cls, token: str, url: str = "https://api.spacetraders.io/v2"
+    ) -> "AstroTradersClient":
+        client = Client(
+            base_url=url,
+            event_hooks={"response": [exception_hook]},
+            headers={"Authorization": f"Bearer {token}"},
+        )
+        return cls(client)
+
+    def close(self) -> "None":
+        self._httpx_instance.close()
```

### Comparing `astrotraders-1.0.0/astrotraders/api/resources/factions.py` & `astrotraders-1.0.1/astrotraders/api/resources/factions.py`

 * *Ordering differences only*

 * *Files 25% similar despite different names*

```diff
@@ -1,21 +1,21 @@
-from astrotraders.api.resources.base import BaseResource
-from astrotraders.api.schemas import PaginatedObject, Faction
-
-
-class FactionsResource(BaseResource):
-    def list(self, limit: int = 20, page: int = 1) -> PaginatedObject[Faction]:
-        """
-        List all discovered factions in the game.
-        """
-        return self._client.request_to_paginated(
-            "GET",
-            "/factions",
-            Faction,
-            params={"limit": limit, "page": page},
-        )
-
-    def get(self, faction: str) -> Faction:
-        """
-        View the details of a faction.
-        """
-        return self._client.request_to_model("GET", f"/factions/{faction}", Faction)
+from astrotraders.api.resources.base import BaseResource
+from astrotraders.api.schemas import PaginatedObject, Faction
+
+
+class FactionsResource(BaseResource):
+    def list(self, limit: int = 20, page: int = 1) -> PaginatedObject[Faction]:
+        """
+        List all discovered factions in the game.
+        """
+        return self._client.request_to_paginated(
+            "GET",
+            "/factions",
+            Faction,
+            params={"limit": limit, "page": page},
+        )
+
+    def get(self, faction: str) -> Faction:
+        """
+        View the details of a faction.
+        """
+        return self._client.request_to_model("GET", f"/factions/{faction}", Faction)
```

### Comparing `astrotraders-1.0.0/astrotraders/api/resources/fleet.py` & `astrotraders-1.0.1/astrotraders/api/resources/fleet.py`

 * *Ordering differences only*

 * *Files 23% similar despite different names*

```diff
@@ -1,344 +1,344 @@
-from typing import Optional, cast, Any
-
-from astrotraders.api.resources.base import BaseResource
-from astrotraders.api.schemas import (
-    PaginatedObject,
-    ShipSchema,
-    ShipType,
-    PurchaseShipResult,
-    ShipCargo,
-    ShipNav,
-    Produce,
-    ShipRefineResult,
-    ChartShipResult,
-    Cooldown,
-    CreateSurveyResult,
-    ExtractResourcesResult,
-    Survey,
-    ShipJumpResult,
-    ShipNavigateResult,
-    ShipNavFlightMode,
-    SellCargoResult,
-    ScanSystemsResult,
-    ScanWaypointsResult,
-    ScanShipsResult,
-    RefuelShipResult,
-    PurchaseCargoResult,
-    TradeSymbol,
-)
-from astrotraders.api.wrapper import HttpxClientWrapper
-
-
-class CargoResource(BaseResource):
-    def get(self, ship: str) -> ShipCargo:
-        """
-        Retrieve the cargo of your ship.
-        """
-        return self._client.request_to_model(
-            "GET",
-            f"/my/ships/{ship}/cargo",
-            ShipCargo,
-        )
-
-    def jettison(self, ship: str, cargo: str, units: int) -> ShipCargo:
-        """
-        Jettison cargo from your ship's cargo hold.
-        """
-        result = cast(
-            dict[str, Any],
-            self._client.raw_request(
-                "POST",
-                f"/my/ships/{ship}/jettison",
-                json={"symbol": cargo, "units": units},
-            ),
-        )
-        return ShipCargo(**result["data"]["cargo"])
-
-    def sell(self, ship: str, cargo: str, units: int) -> SellCargoResult:
-        """
-        Sell cargo.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/sell",
-            SellCargoResult,
-            json={"symbol": cargo, "units": units},
-        )
-
-    def purchase(self, ship: str, cargo: str, units: int) -> PurchaseCargoResult:
-        """
-        Purchase cargo.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/purchase",
-            PurchaseCargoResult,
-            json={"symbol": cargo, "units": units},
-        )
-
-    def transfer(
-        self, from_ship: str, to_ship: str, cargo: TradeSymbol, units: int
-    ) -> ShipCargo:
-        """
-        Transfer cargo between ships.
-        """
-        result = cast(
-            dict[str, Any],
-            self._client.raw_request(
-                "POST",
-                f"/my/ships/{from_ship}/transfer",
-                json={"tradeSymbol": cargo, "units": units, "shipSymbol": to_ship},
-            ),
-        )
-        return ShipCargo(**result["data"]["cargo"])
-
-
-class ScanResource(BaseResource):
-    def systems(self, ship: str) -> ScanSystemsResult:
-        """
-        Activate your ship's sensor arrays to scan for system information.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/scan/systems",
-            ScanSystemsResult,
-        )
-
-    def waypoints(self, ship: str) -> ScanWaypointsResult:
-        """
-        Activate your ship's sensor arrays to scan for waypoint information.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/scan/waypoints",
-            ScanWaypointsResult,
-        )
-
-    def ships(self, ship: str) -> ScanShipsResult:
-        """
-        Activate your ship's sensor arrays to scan for ship information.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/scan/ships",
-            ScanShipsResult,
-        )
-
-
-class FleetResource(BaseResource):
-    def __init__(self, client: HttpxClientWrapper):
-        super().__init__(client)
-        self.scan = ScanResource(client)
-        self.cargo = CargoResource(client)
-
-    def list(self, limit: int = 20, page: int = 1) -> PaginatedObject[ShipSchema]:
-        """
-        Retrieve all of your ships.
-        """
-        return self._client.request_to_paginated(
-            "GET",
-            "/my/ships",
-            ShipSchema,
-            params={"limit": limit, "page": page},
-        )
-
-    def get(self, name: str) -> ShipSchema:
-        """
-        Retrieve the details of your ship.
-        """
-        return self._client.request_to_model("GET", f"/my/ships/{name}", ShipSchema)
-
-    def purchase(self, ship_type: ShipType, waypoint: str) -> PurchaseShipResult:
-        """
-        Purchase a ship
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships",
-            PurchaseShipResult,
-            json={"shipType": ship_type, "waypointSymbol": waypoint},
-        )
-
-    def orbit(self, ship: str) -> ShipNav:
-        """
-        Attempt to move your ship into orbit at it's current location.
-
-        The request will only succeed if your ship is capable of moving into orbit at the time of the request.
-        The endpoint is idempotent - successive calls will succeed even if the ship is already in orbit.
-        """
-        result = cast(
-            dict[str, Any],
-            self._client.raw_request(
-                "POST",
-                f"/my/ships/{ship}/orbit",
-            ),
-        )
-        return ShipNav(**result["data"]["nav"])
-
-    def refine(self, ship: str, produce: Produce) -> ShipRefineResult:
-        """
-        Attempt to refine the raw materials on your ship.
-
-        The request will only succeed if your ship is capable of refining at the time of the request.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/refine",
-            ShipRefineResult,
-            json={"produce": produce},
-        )
-
-    def chart(self, ship: str) -> ChartShipResult:
-        """
-        Command a ship to chart the current waypoint.
-
-        Waypoints in the universe are uncharted by default.
-        These locations will not show up in the API until they have been charted by a ship.
-        Charting a location will record your agent as the one who created the chart.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/chart",
-            ChartShipResult,
-        )
-
-    def cooldown(self, ship: str) -> Optional[Cooldown]:
-        """
-        Retrieve the details of your ship's reactor cooldown.
-        Some actions such as activating your jump drive, scanning,
-        or extracting resources taxes your reactor and results in a cooldown.
-
-        Your ship cannot perform additional actions until your cooldown has expired.
-        The duration of your cooldown is relative to the power consumption
-        of the related modules or mounts for the action taken.
-        None returns when the ship has no cooldown.
-        """
-        return self._client.request_to_model_optioned(
-            "GET",
-            f"/my/ships/{ship}/cooldown",
-            Cooldown,
-        )
-
-    def dock(self, ship: str) -> ShipNav:
-        """
-        Attempt to dock your ship at it's current location.
-
-        Docking will only succeed if the waypoint is a dockable location,
-        and your ship is capable of docking at the time of the request.
-        The endpoint is idempotent - successive calls will succeed even if the ship is already docked.
-        """
-        result = cast(
-            dict[str, Any],
-            self._client.raw_request(
-                "POST",
-                f"/my/ships/{ship}/dock",
-            ),
-        )
-        return ShipNav(**result["data"]["nav"])
-
-    def survey(self, ship: str) -> CreateSurveyResult:
-        """
-        If you want to target specific yields for an extraction,
-        you can survey a waypoint, such as an asteroid field,
-        and send the survey in the body of the extract request.
-        Each survey may have multiple deposits, and if a symbol
-        shows up more than once, that indicates a higher chance of extracting that resource.
-
-        Your ship will enter a cooldown between consecutive survey requests.
-        Surveys will eventually expire after a period of time.
-        Multiple ships can use the same survey for extraction.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/survey",
-            CreateSurveyResult,
-        )
-
-    def extract(
-        self, ship: str, survey: Optional[Survey] = None
-    ) -> ExtractResourcesResult:
-        """
-        Extract resources from the waypoint into your ship.
-        Send an optional survey as the payload to target specific yields.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/extract",
-            ExtractResourcesResult,
-            json={"survey": survey.dict()} if survey else {},
-        )
-
-    def jump(self, ship: str, system: str) -> ShipJumpResult:
-        """
-        Jump your ship instantly to a target system.
-        Unlike other forms of navigation, jumping requires a unit of antimatter.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/jump",
-            ShipJumpResult,
-            json={"systemSymbol": system},
-        )
-
-    def navigate(self, ship: str, waypoint: str) -> ShipNavigateResult:
-        """
-        Navigate to a target destination.
-
-        The destination must be located within the same system as the ship.
-        Navigating will consume the necessary fuel and supplies from the ship's manifest,
-        and will pay out crew wages from the agent's account.
-        The returned response will detail the route information including the expected time of arrival.
-        Most ship actions are unavailable until the ship has arrived at it's destination.
-        To travel between systems, see the ship's warp or jump actions.
-        """
-
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/navigate",
-            ShipNavigateResult,
-            json={"waypointSymbol": waypoint},
-        )
-
-    def flight_mode(self, ship: str, mode: ShipNavFlightMode) -> ShipNav:
-        """
-        Update the nav data of a ship, such as the flight mode.
-        """
-        return self._client.request_to_model(
-            "PATCH", f"/my/ships/{ship}/nav", ShipNav, json={"flightMode": mode}
-        )
-
-    def nav(self, ship: str) -> ShipNav:
-        """
-        Get the current nav status of a ship.
-        """
-        return self._client.request_to_model(
-            "GET",
-            f"/my/ships/{ship}/nav",
-            ShipNav,
-        )
-
-    def warp(self, ship: str, waypoint: str) -> ShipNavigateResult:
-        """
-        Warp your ship to a target destination in another system.
-        Warping will consume the necessary fuel and supplies
-        from the ship's manifest, and will pay out crew wages from the agent's account.
-
-        The returned response will detail the route information including the expected time of arrival.
-        Most ship actions are unavailable until the ship has arrived at it's destination.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/warp",
-            ShipNavigateResult,
-            json={"waypointSymbol": waypoint},
-        )
-
-    def refuel(self, ship: str) -> RefuelShipResult:
-        """
-        Refuel your ship from the local market.
-        """
-        return self._client.request_to_model(
-            "POST",
-            f"/my/ships/{ship}/refuel",
-            RefuelShipResult,
-        )
+from typing import Optional, cast, Any
+
+from astrotraders.api.resources.base import BaseResource
+from astrotraders.api.schemas import (
+    PaginatedObject,
+    ShipSchema,
+    ShipType,
+    PurchaseShipResult,
+    ShipCargo,
+    ShipNav,
+    Produce,
+    ShipRefineResult,
+    ChartShipResult,
+    Cooldown,
+    CreateSurveyResult,
+    ExtractResourcesResult,
+    Survey,
+    ShipJumpResult,
+    ShipNavigateResult,
+    ShipNavFlightMode,
+    SellCargoResult,
+    ScanSystemsResult,
+    ScanWaypointsResult,
+    ScanShipsResult,
+    RefuelShipResult,
+    PurchaseCargoResult,
+    TradeSymbol,
+)
+from astrotraders.api.wrapper import HttpxClientWrapper
+
+
+class CargoResource(BaseResource):
+    def get(self, ship: str) -> ShipCargo:
+        """
+        Retrieve the cargo of your ship.
+        """
+        return self._client.request_to_model(
+            "GET",
+            f"/my/ships/{ship}/cargo",
+            ShipCargo,
+        )
+
+    def jettison(self, ship: str, cargo: str, units: int) -> ShipCargo:
+        """
+        Jettison cargo from your ship's cargo hold.
+        """
+        result = cast(
+            dict[str, Any],
+            self._client.raw_request(
+                "POST",
+                f"/my/ships/{ship}/jettison",
+                json={"symbol": cargo, "units": units},
+            ),
+        )
+        return ShipCargo(**result["data"]["cargo"])
+
+    def sell(self, ship: str, cargo: str, units: int) -> SellCargoResult:
+        """
+        Sell cargo.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/sell",
+            SellCargoResult,
+            json={"symbol": cargo, "units": units},
+        )
+
+    def purchase(self, ship: str, cargo: str, units: int) -> PurchaseCargoResult:
+        """
+        Purchase cargo.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/purchase",
+            PurchaseCargoResult,
+            json={"symbol": cargo, "units": units},
+        )
+
+    def transfer(
+        self, from_ship: str, to_ship: str, cargo: TradeSymbol, units: int
+    ) -> ShipCargo:
+        """
+        Transfer cargo between ships.
+        """
+        result = cast(
+            dict[str, Any],
+            self._client.raw_request(
+                "POST",
+                f"/my/ships/{from_ship}/transfer",
+                json={"tradeSymbol": cargo, "units": units, "shipSymbol": to_ship},
+            ),
+        )
+        return ShipCargo(**result["data"]["cargo"])
+
+
+class ScanResource(BaseResource):
+    def systems(self, ship: str) -> ScanSystemsResult:
+        """
+        Activate your ship's sensor arrays to scan for system information.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/scan/systems",
+            ScanSystemsResult,
+        )
+
+    def waypoints(self, ship: str) -> ScanWaypointsResult:
+        """
+        Activate your ship's sensor arrays to scan for waypoint information.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/scan/waypoints",
+            ScanWaypointsResult,
+        )
+
+    def ships(self, ship: str) -> ScanShipsResult:
+        """
+        Activate your ship's sensor arrays to scan for ship information.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/scan/ships",
+            ScanShipsResult,
+        )
+
+
+class FleetResource(BaseResource):
+    def __init__(self, client: HttpxClientWrapper):
+        super().__init__(client)
+        self.scan = ScanResource(client)
+        self.cargo = CargoResource(client)
+
+    def list(self, limit: int = 20, page: int = 1) -> PaginatedObject[ShipSchema]:
+        """
+        Retrieve all of your ships.
+        """
+        return self._client.request_to_paginated(
+            "GET",
+            "/my/ships",
+            ShipSchema,
+            params={"limit": limit, "page": page},
+        )
+
+    def get(self, name: str) -> ShipSchema:
+        """
+        Retrieve the details of your ship.
+        """
+        return self._client.request_to_model("GET", f"/my/ships/{name}", ShipSchema)
+
+    def purchase(self, ship_type: ShipType, waypoint: str) -> PurchaseShipResult:
+        """
+        Purchase a ship
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships",
+            PurchaseShipResult,
+            json={"shipType": ship_type, "waypointSymbol": waypoint},
+        )
+
+    def orbit(self, ship: str) -> ShipNav:
+        """
+        Attempt to move your ship into orbit at it's current location.
+
+        The request will only succeed if your ship is capable of moving into orbit at the time of the request.
+        The endpoint is idempotent - successive calls will succeed even if the ship is already in orbit.
+        """
+        result = cast(
+            dict[str, Any],
+            self._client.raw_request(
+                "POST",
+                f"/my/ships/{ship}/orbit",
+            ),
+        )
+        return ShipNav(**result["data"]["nav"])
+
+    def refine(self, ship: str, produce: Produce) -> ShipRefineResult:
+        """
+        Attempt to refine the raw materials on your ship.
+
+        The request will only succeed if your ship is capable of refining at the time of the request.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/refine",
+            ShipRefineResult,
+            json={"produce": produce},
+        )
+
+    def chart(self, ship: str) -> ChartShipResult:
+        """
+        Command a ship to chart the current waypoint.
+
+        Waypoints in the universe are uncharted by default.
+        These locations will not show up in the API until they have been charted by a ship.
+        Charting a location will record your agent as the one who created the chart.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/chart",
+            ChartShipResult,
+        )
+
+    def cooldown(self, ship: str) -> Optional[Cooldown]:
+        """
+        Retrieve the details of your ship's reactor cooldown.
+        Some actions such as activating your jump drive, scanning,
+        or extracting resources taxes your reactor and results in a cooldown.
+
+        Your ship cannot perform additional actions until your cooldown has expired.
+        The duration of your cooldown is relative to the power consumption
+        of the related modules or mounts for the action taken.
+        None returns when the ship has no cooldown.
+        """
+        return self._client.request_to_model_optioned(
+            "GET",
+            f"/my/ships/{ship}/cooldown",
+            Cooldown,
+        )
+
+    def dock(self, ship: str) -> ShipNav:
+        """
+        Attempt to dock your ship at it's current location.
+
+        Docking will only succeed if the waypoint is a dockable location,
+        and your ship is capable of docking at the time of the request.
+        The endpoint is idempotent - successive calls will succeed even if the ship is already docked.
+        """
+        result = cast(
+            dict[str, Any],
+            self._client.raw_request(
+                "POST",
+                f"/my/ships/{ship}/dock",
+            ),
+        )
+        return ShipNav(**result["data"]["nav"])
+
+    def survey(self, ship: str) -> CreateSurveyResult:
+        """
+        If you want to target specific yields for an extraction,
+        you can survey a waypoint, such as an asteroid field,
+        and send the survey in the body of the extract request.
+        Each survey may have multiple deposits, and if a symbol
+        shows up more than once, that indicates a higher chance of extracting that resource.
+
+        Your ship will enter a cooldown between consecutive survey requests.
+        Surveys will eventually expire after a period of time.
+        Multiple ships can use the same survey for extraction.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/survey",
+            CreateSurveyResult,
+        )
+
+    def extract(
+        self, ship: str, survey: Optional[Survey] = None
+    ) -> ExtractResourcesResult:
+        """
+        Extract resources from the waypoint into your ship.
+        Send an optional survey as the payload to target specific yields.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/extract",
+            ExtractResourcesResult,
+            json={"survey": survey.dict()} if survey else {},
+        )
+
+    def jump(self, ship: str, system: str) -> ShipJumpResult:
+        """
+        Jump your ship instantly to a target system.
+        Unlike other forms of navigation, jumping requires a unit of antimatter.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/jump",
+            ShipJumpResult,
+            json={"systemSymbol": system},
+        )
+
+    def navigate(self, ship: str, waypoint: str) -> ShipNavigateResult:
+        """
+        Navigate to a target destination.
+
+        The destination must be located within the same system as the ship.
+        Navigating will consume the necessary fuel and supplies from the ship's manifest,
+        and will pay out crew wages from the agent's account.
+        The returned response will detail the route information including the expected time of arrival.
+        Most ship actions are unavailable until the ship has arrived at it's destination.
+        To travel between systems, see the ship's warp or jump actions.
+        """
+
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/navigate",
+            ShipNavigateResult,
+            json={"waypointSymbol": waypoint},
+        )
+
+    def flight_mode(self, ship: str, mode: ShipNavFlightMode) -> ShipNav:
+        """
+        Update the nav data of a ship, such as the flight mode.
+        """
+        return self._client.request_to_model(
+            "PATCH", f"/my/ships/{ship}/nav", ShipNav, json={"flightMode": mode}
+        )
+
+    def nav(self, ship: str) -> ShipNav:
+        """
+        Get the current nav status of a ship.
+        """
+        return self._client.request_to_model(
+            "GET",
+            f"/my/ships/{ship}/nav",
+            ShipNav,
+        )
+
+    def warp(self, ship: str, waypoint: str) -> ShipNavigateResult:
+        """
+        Warp your ship to a target destination in another system.
+        Warping will consume the necessary fuel and supplies
+        from the ship's manifest, and will pay out crew wages from the agent's account.
+
+        The returned response will detail the route information including the expected time of arrival.
+        Most ship actions are unavailable until the ship has arrived at it's destination.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/warp",
+            ShipNavigateResult,
+            json={"waypointSymbol": waypoint},
+        )
+
+    def refuel(self, ship: str) -> RefuelShipResult:
+        """
+        Refuel your ship from the local market.
+        """
+        return self._client.request_to_model(
+            "POST",
+            f"/my/ships/{ship}/refuel",
+            RefuelShipResult,
+        )
```

### Comparing `astrotraders-1.0.0/astrotraders/api/resources/systems.py` & `astrotraders-1.0.1/astrotraders/api/resources/systems.py`

 * *Ordering differences only*

 * *Files 16% similar despite different names*

```diff
@@ -1,97 +1,97 @@
-from astrotraders.api.resources.base import BaseResource
-from astrotraders.api.schemas import (
-    PaginatedObject,
-    System,
-    Waypoint,
-    Market,
-    Shipyard,
-    JumpGate,
-)
-from astrotraders.api.wrapper import HttpxClientWrapper
-
-
-class SystemsResource(BaseResource):
-    def __init__(self, client: HttpxClientWrapper):
-        super().__init__(client)
-        self.waypoints = WaypointsResource(client)
-
-    def list(self, limit: int = 20, page: int = 1) -> PaginatedObject[System]:
-        """
-        Return a list of all systems.
-        """
-        return self._client.request_to_paginated(
-            "GET",
-            "/systems",
-            System,
-            params={"limit": limit, "page": page},
-        )
-
-    def get(self, name: str) -> System:
-        """
-        Get the details of a system.
-        """
-        return self._client.request_to_model("GET", f"/systems/{name}", System)
-
-
-class WaypointsResource(BaseResource):
-    def list(
-        self, system: str, limit: int = 20, page: int = 1
-    ) -> PaginatedObject[Waypoint]:
-        """
-        Fetch all waypoints for a given system.
-        System must be charted or a ship must be present to return waypoint details.
-        """
-        return self._client.request_to_paginated(
-            "GET",
-            f"/systems/{system}/waypoints",
-            Waypoint,
-            params={"limit": limit, "page": page, "systemSymbol": system},
-        )
-
-    def get(self, system: str, waypoint: str) -> Waypoint:
-        """
-        View the details of a waypoint.
-        """
-        return self._client.request_to_model(
-            "GET",
-            f"/systems/{system}/waypoints/{waypoint}",
-            Waypoint,
-            params={"waypointSymbol": waypoint, "systemSymbol": system},
-        )
-
-    def market(self, system: str, waypoint: str) -> Market:
-        """
-        Retrieve imports, exports and exchange data from a marketplace.
-        Imports can be sold, exports can be purchased,
-        and exchange goods can be purchased or sold.
-        Send a ship to the waypoint to access trade good prices and recent transactions.
-        """
-        return self._client.request_to_model(
-            "GET",
-            f"/systems/{system}/waypoints/{waypoint}/market",
-            Market,
-            params={"waypointSymbol": waypoint, "systemSymbol": system},
-        )
-
-    def shipyard(self, system: str, waypoint: str) -> Shipyard:
-        """
-        Get the shipyard for a waypoint.
-        Send a ship to the waypoint to access ships that are currently available for purchase and recent transactions.
-        """
-        return self._client.request_to_model(
-            "GET",
-            f"/systems/{system}/waypoints/{waypoint}/shipyard",
-            Shipyard,
-            params={"waypointSymbol": waypoint, "systemSymbol": system},
-        )
-
-    def jump_gate(self, system: str, waypoint: str) -> JumpGate:
-        """
-        Get jump gate details for a waypoint.
-        """
-        return self._client.request_to_model(
-            "GET",
-            f"/systems/{system}/waypoints/{waypoint}/jump-gate",
-            JumpGate,
-            params={"waypointSymbol": waypoint, "systemSymbol": system},
-        )
+from astrotraders.api.resources.base import BaseResource
+from astrotraders.api.schemas import (
+    PaginatedObject,
+    System,
+    Waypoint,
+    Market,
+    Shipyard,
+    JumpGate,
+)
+from astrotraders.api.wrapper import HttpxClientWrapper
+
+
+class SystemsResource(BaseResource):
+    def __init__(self, client: HttpxClientWrapper):
+        super().__init__(client)
+        self.waypoints = WaypointsResource(client)
+
+    def list(self, limit: int = 20, page: int = 1) -> PaginatedObject[System]:
+        """
+        Return a list of all systems.
+        """
+        return self._client.request_to_paginated(
+            "GET",
+            "/systems",
+            System,
+            params={"limit": limit, "page": page},
+        )
+
+    def get(self, name: str) -> System:
+        """
+        Get the details of a system.
+        """
+        return self._client.request_to_model("GET", f"/systems/{name}", System)
+
+
+class WaypointsResource(BaseResource):
+    def list(
+        self, system: str, limit: int = 20, page: int = 1
+    ) -> PaginatedObject[Waypoint]:
+        """
+        Fetch all waypoints for a given system.
+        System must be charted or a ship must be present to return waypoint details.
+        """
+        return self._client.request_to_paginated(
+            "GET",
+            f"/systems/{system}/waypoints",
+            Waypoint,
+            params={"limit": limit, "page": page, "systemSymbol": system},
+        )
+
+    def get(self, system: str, waypoint: str) -> Waypoint:
+        """
+        View the details of a waypoint.
+        """
+        return self._client.request_to_model(
+            "GET",
+            f"/systems/{system}/waypoints/{waypoint}",
+            Waypoint,
+            params={"waypointSymbol": waypoint, "systemSymbol": system},
+        )
+
+    def market(self, system: str, waypoint: str) -> Market:
+        """
+        Retrieve imports, exports and exchange data from a marketplace.
+        Imports can be sold, exports can be purchased,
+        and exchange goods can be purchased or sold.
+        Send a ship to the waypoint to access trade good prices and recent transactions.
+        """
+        return self._client.request_to_model(
+            "GET",
+            f"/systems/{system}/waypoints/{waypoint}/market",
+            Market,
+            params={"waypointSymbol": waypoint, "systemSymbol": system},
+        )
+
+    def shipyard(self, system: str, waypoint: str) -> Shipyard:
+        """
+        Get the shipyard for a waypoint.
+        Send a ship to the waypoint to access ships that are currently available for purchase and recent transactions.
+        """
+        return self._client.request_to_model(
+            "GET",
+            f"/systems/{system}/waypoints/{waypoint}/shipyard",
+            Shipyard,
+            params={"waypointSymbol": waypoint, "systemSymbol": system},
+        )
+
+    def jump_gate(self, system: str, waypoint: str) -> JumpGate:
+        """
+        Get jump gate details for a waypoint.
+        """
+        return self._client.request_to_model(
+            "GET",
+            f"/systems/{system}/waypoints/{waypoint}/jump-gate",
+            JumpGate,
+            params={"waypointSymbol": waypoint, "systemSymbol": system},
+        )
```

### Comparing `astrotraders-1.0.0/astrotraders/api/schemas.py` & `astrotraders-1.0.1/astrotraders/api/schemas.py`

 * *Ordering differences only*

 * *Files 25% similar despite different names*

```diff
@@ -1,1290 +1,1290 @@
-from __future__ import annotations
-
-from datetime import datetime
-from enum import Enum
-from typing import List, Optional, TypeVar, Generic, Annotated
-
-from pydantic import Field, confloat, conint, BaseModel, ConstrainedStr, NonNegativeInt
-from pydantic.generics import GenericModel
-
-T = TypeVar("T")
-
-
-class NonEmptyStr(ConstrainedStr):
-    strict = True
-    min_length = 1
-
-
-class Meta(BaseModel):
-    total: int
-    page: int
-    limit: int
-
-
-class PaginatedObject(GenericModel, Generic[T]):
-    objects: list[T] = Field(alias="data")
-    meta: Meta
-
-
-class FactionsEnum(str, Enum):
-    cosmic = "COSMIC"
-    void = "VOID"
-    galactic = "GALACTIC"
-    quantum = "QUANTUM"
-    dominion = "DOMINION"
-
-
-class RegisterRequestData(BaseModel):
-    faction: FactionsEnum = Field(
-        ..., description="The faction you choose determines your headquarters."
-    )
-    symbol: Annotated[
-        str,
-        constr(min_length=3, max_length=14),
-        Field(
-            ...,
-            description="How other agents will see your ships and information.",
-            example="BADGER",
-        ),
-    ]
-
-
-class AgentSchema(BaseModel):
-    account_id: NonEmptyStr = Field(..., alias="accountId")
-    symbol: NonEmptyStr
-    headquarters: NonEmptyStr = Field(..., description="The headquarters of the agent.")
-    credits: int = Field(
-        ...,
-        description=(
-            "The number of credits the agent has available. Credits can be negative if"
-            " funds have been overdrawn."
-        ),
-    )
-
-
-class ContractType(str, Enum):
-    procurement = "PROCUREMENT"
-    transport = "TRANSPORT"
-    shuttle = "SHUTTLE"
-
-
-class ContractPayment(BaseModel):
-    on_accepted: int = Field(
-        ...,
-        alias="onAccepted",
-        description=(
-            "The amount of credits received up front for accepting the contract."
-        ),
-    )
-    on_fulfilled: int = Field(
-        ...,
-        alias="onFulfilled",
-        description="The amount of credits received when the contract is fulfilled.",
-    )
-
-
-class ContractDeliverGood(BaseModel):
-    trade_symbol: NonEmptyStr = Field(
-        ..., alias="tradeSymbol", description="The symbol of the trade good to deliver."
-    )
-    destination_symbol: NonEmptyStr = Field(
-        ...,
-        alias="destinationSymbol",
-        description="The destination where goods need to be delivered.",
-    )
-    units_required: int = Field(
-        ...,
-        alias="unitsRequired",
-        description="The number of units that need to be delivered on this contract.",
-    )
-    units_fulfilled: int = Field(
-        ...,
-        alias="unitsFulfilled",
-        description="The number of units fulfilled on this contract.",
-    )
-
-
-class FactionTraitEnum(str, Enum):
-    bureaucratic = "BUREAUCRATIC"
-    secretive = "SECRETIVE"
-    capitalistic = "CAPITALISTIC"
-    industrious = "INDUSTRIOUS"
-    peaceful = "PEACEFUL"
-    distrustful = "DISTRUSTFUL"
-    welcoming = "WELCOMING"
-    anarchist = "ANARCHIST"
-    conflicted = "CONFLICTED"
-    authoritarian = "AUTHORITARIAN"
-    oligarchical = "OLIGARCHICAL"
-    dynastic = "DYNASTIC"
-    democractic = "DEMOCRACTIC"
-    decentralized = "DECENTRALIZED"
-    smugglers = "SMUGGLERS"
-    scavengers = "SCAVENGERS"
-    rebellious = "REBELLIOUS"
-    exiles = "EXILES"
-    pirates = "PIRATES"
-    raiders = "RAIDERS"
-    clan = "CLAN"
-    guild = "GUILD"
-    dominion = "DOMINION"
-    fringe = "FRINGE"
-    forsaken = "FORSAKEN"
-    isolated = "ISOLATED"
-    localized = "LOCALIZED"
-    established = "ESTABLISHED"
-    notable = "NOTABLE"
-    dominant = "DOMINANT"
-    inescapable = "INESCAPABLE"
-    innovative = "INNOVATIVE"
-    bold = "BOLD"
-    visionary = "VISIONARY"
-    curious = "CURIOUS"
-    daring = "DARING"
-    exploratory = "EXPLORATORY"
-    resourceful = "RESOURCEFUL"
-    flexible = "FLEXIBLE"
-    cooperative = "COOPERATIVE"
-    united = "UNITED"
-    strategic = "STRATEGIC"
-    intelligent = "INTELLIGENT"
-    research_focused = "RESEARCH_FOCUSED"
-    collaborative = "COLLABORATIVE"
-    progressive = "PROGRESSIVE"
-    militaristic = "MILITARISTIC"
-    technologically_advanced = "TECHNOLOGICALLY_ADVANCED"
-    aggressive = "AGGRESSIVE"
-    imperialistic = "IMPERIALISTIC"
-    treasure_hunters = "TREASURE_HUNTERS"
-    dexterous = "DEXTEROUS"
-    unpredictable = "UNPREDICTABLE"
-    brutal = "BRUTAL"
-    fleeting = "FLEETING"
-    adaptable = "ADAPTABLE"
-    self_sufficient = "SELF_SUFFICIENT"
-    defensive = "DEFENSIVE"
-    proud = "PROUD"
-    diverse = "DIVERSE"
-    independent = "INDEPENDENT"
-    self_interested = "SELF_INTERESTED"
-    fragmented = "FRAGMENTED"
-    commercial = "COMMERCIAL"
-    free_markets = "FREE_MARKETS"
-    entrepreneurial = "ENTREPRENEURIAL"
-
-
-class FactionTrait(BaseModel):
-    symbol: FactionTraitEnum = Field(
-        ..., description="The unique identifier of the trait."
-    )
-    name: str = Field(..., description="The name of the trait.")
-    description: str = Field(..., description="A description of the trait.")
-
-
-class ShipRole(str, Enum):
-    fabricator = "FABRICATOR"
-    harvester = "HARVESTER"
-    hauler = "HAULER"
-    interceptor = "INTERCEPTOR"
-    excavator = "EXCAVATOR"
-    transport = "TRANSPORT"
-    repair = "REPAIR"
-    surveyor = "SURVEYOR"
-    command = "COMMAND"
-    carrier = "CARRIER"
-    patrol = "PATROL"
-    satellite = "SATELLITE"
-    explorer = "EXPLORER"
-    refinery = "REFINERY"
-
-
-class WaypointType(str, Enum):
-    planet = "PLANET"
-    gas_giant = "GAS_GIANT"
-    moon = "MOON"
-    orbital_station = "ORBITAL_STATION"
-    jump_gate = "JUMP_GATE"
-    asteroid_field = "ASTEROID_FIELD"
-    nebula = "NEBULA"
-    debris_field = "DEBRIS_FIELD"
-    gravity_well = "GRAVITY_WELL"
-
-
-class ShipNavStatus(str, Enum):
-    in_transit = "IN_TRANSIT"
-    in_orbit = "IN_ORBIT"
-    docked = "DOCKED"
-
-
-class ShipNavFlightMode(str, Enum):
-    drift = "DRIFT"
-    stealth = "STEALTH"
-    cruise = "CRUISE"
-    burn = "BURN"
-
-
-class Rotation(str, Enum):
-    strict = "STRICT"
-    relaxed = "RELAXED"
-
-
-class ShipCrew(BaseModel):
-    current: int = Field(
-        ..., description="The current number of crew members on the ship."
-    )
-    required: int = Field(
-        ...,
-        description="The minimum number of crew members required to maintain the ship.",
-    )
-    capacity: int = Field(
-        ..., description="The maximum number of crew members the ship can support."
-    )
-    rotation: Rotation = Field(
-        ...,
-        description=(
-            "The rotation of crew shifts. A stricter shift improves the ship's"
-            " performance. A more relaxed shift improves the crew's morale."
-        ),
-    )
-    morale: Annotated[
-        int,
-        conint(ge=0, le=100),
-        Field(
-            ...,
-            description=(
-                "A rough measure of the crew's morale. A higher morale means the crew is"
-                " happier and more productive. A lower morale means the ship is more prone"
-                " to accidents."
-            ),
-        ),
-    ]
-    wages: NonNegativeInt = Field(
-        ...,
-        description=(
-            "The amount of credits per crew member paid per hour. Wages are paid when a"
-            " ship docks at a civilized waypoint."
-        ),
-    )
-
-
-class FramesEnum(str, Enum):
-    frame_probe = "FRAME_PROBE"
-    frame_drone = "FRAME_DRONE"
-    frame_interceptor = "FRAME_INTERCEPTOR"
-    frame_racer = "FRAME_RACER"
-    frame_fighter = "FRAME_FIGHTER"
-    frame_frigate = "FRAME_FRIGATE"
-    frame_shuttle = "FRAME_SHUTTLE"
-    frame_explorer = "FRAME_EXPLORER"
-    frame_miner = "FRAME_MINER"
-    frame_light_freighter = "FRAME_LIGHT_FREIGHTER"
-    frame_heavy_freighter = "FRAME_HEAVY_FREIGHTER"
-    frame_transport = "FRAME_TRANSPORT"
-    frame_destroyer = "FRAME_DESTROYER"
-    frame_cruiser = "FRAME_CRUISER"
-    frame_carrier = "FRAME_CARRIER"
-
-
-class ShipCondition(BaseModel):
-    __root__: Annotated[
-        int,
-        conint(ge=0, le=100),
-        Field(
-            ...,
-            description=(
-                "Condition is a range of 0 to 100 where 0 is completely worn out and 100 is"
-                " brand new."
-            ),
-        ),
-    ]
-
-
-class ShipRequirements(BaseModel):
-    power: Optional[int] = Field(
-        None, description="The amount of power required from the reactor."
-    )
-    crew: Optional[int] = Field(
-        None, description="The number of crew required for operation."
-    )
-    slots: Optional[int] = Field(
-        None, description="The number of module slots required for installation."
-    )
-
-
-class ReactorsEnum(str, Enum):
-    reactor_solar_i = "REACTOR_SOLAR_I"
-    reactor_fusion_i = "REACTOR_FUSION_I"
-    reactor_fission_i = "REACTOR_FISSION_I"
-    reactor_chemical_i = "REACTOR_CHEMICAL_I"
-    reactor_antimatter_i = "REACTOR_ANTIMATTER_I"
-
-
-class ShipReactor(BaseModel):
-    symbol: ReactorsEnum
-    name: str
-    description: str
-    condition: Optional[ShipCondition] = None
-    power_output: Annotated[int, conint(ge=1), Field(..., alias="powerOutput")]
-    requirements: ShipRequirements
-
-
-class EnginesEnum(str, Enum):
-    engine_impulse_drive_i = "ENGINE_IMPULSE_DRIVE_I"
-    engine_ion_drive_i = "ENGINE_ION_DRIVE_I"
-    engine_ion_drive_ii = "ENGINE_ION_DRIVE_II"
-    engine_hyper_drive_i = "ENGINE_HYPER_DRIVE_I"
-
-
-class ShipEngine(BaseModel):
-    symbol: EnginesEnum
-    name: str
-    description: str
-    condition: Optional[ShipCondition] = None
-    speed: Annotated[float, confloat(ge=1.0)]
-    requirements: ShipRequirements
-
-
-class ShipModules(str, Enum):
-    module_mineral_processor_i = "MODULE_MINERAL_PROCESSOR_I"
-    module_cargo_hold_i = "MODULE_CARGO_HOLD_I"
-    module_crew_quarters_i = "MODULE_CREW_QUARTERS_I"
-    module_envoy_quarters_i = "MODULE_ENVOY_QUARTERS_I"
-    module_passenger_cabin_i = "MODULE_PASSENGER_CABIN_I"
-    module_micro_refinery_i = "MODULE_MICRO_REFINERY_I"
-    module_ore_refinery_i = "MODULE_ORE_REFINERY_I"
-    module_fuel_refinery_i = "MODULE_FUEL_REFINERY_I"
-    module_science_lab_i = "MODULE_SCIENCE_LAB_I"
-    module_jump_drive_i = "MODULE_JUMP_DRIVE_I"
-    module_jump_drive_ii = "MODULE_JUMP_DRIVE_II"
-    module_jump_drive_iii = "MODULE_JUMP_DRIVE_III"
-    module_warp_drive_i = "MODULE_WARP_DRIVE_I"
-    module_warp_drive_ii = "MODULE_WARP_DRIVE_II"
-    module_warp_drive_iii = "MODULE_WARP_DRIVE_III"
-    module_shield_generator_i = "MODULE_SHIELD_GENERATOR_I"
-    module_shield_generator_ii = "MODULE_SHIELD_GENERATOR_II"
-
-
-class ShipModule(BaseModel):
-    symbol: ShipModules
-    capacity: Optional[NonNegativeInt] = None
-    range: Optional[NonNegativeInt] = None
-    name: str
-    description: Optional[str] = None
-    requirements: ShipRequirements
-
-
-class ShipMounts(str, Enum):
-    mount_gas_siphon_i = "MOUNT_GAS_SIPHON_I"
-    mount_gas_siphon_ii = "MOUNT_GAS_SIPHON_II"
-    mount_gas_siphon_iii = "MOUNT_GAS_SIPHON_III"
-    mount_surveyor_i = "MOUNT_SURVEYOR_I"
-    mount_surveyor_ii = "MOUNT_SURVEYOR_II"
-    mount_surveyor_iii = "MOUNT_SURVEYOR_III"
-    mount_sensor_array_i = "MOUNT_SENSOR_ARRAY_I"
-    mount_sensor_array_ii = "MOUNT_SENSOR_ARRAY_II"
-    mount_sensor_array_iii = "MOUNT_SENSOR_ARRAY_III"
-    mount_mining_laser_i = "MOUNT_MINING_LASER_I"
-    mount_mining_laser_ii = "MOUNT_MINING_LASER_II"
-    mount_mining_laser_iii = "MOUNT_MINING_LASER_III"
-    mount_laser_cannon_i = "MOUNT_LASER_CANNON_I"
-    mount_missile_launcher_i = "MOUNT_MISSILE_LAUNCHER_I"
-    mount_turret_i = "MOUNT_TURRET_I"
-
-
-class Deposit(str, Enum):
-    quartz_sand = "QUARTZ_SAND"
-    silicon_crystals = "SILICON_CRYSTALS"
-    precious_stones = "PRECIOUS_STONES"
-    ice_water = "ICE_WATER"
-    ammonia_ice = "AMMONIA_ICE"
-    iron_ore = "IRON_ORE"
-    copper_ore = "COPPER_ORE"
-    silver_ore = "SILVER_ORE"
-    aluminum_ore = "ALUMINUM_ORE"
-    gold_ore = "GOLD_ORE"
-    platinum_ore = "PLATINUM_ORE"
-    diamonds = "DIAMONDS"
-    uranite_ore = "URANITE_ORE"
-    meritium_ore = "MERITIUM_ORE"
-
-
-class ShipMount(BaseModel):
-    symbol: ShipMounts
-    name: str
-    description: Optional[str] = None
-    strength: Optional[NonNegativeInt] = None
-    deposits: Optional[List[Deposit]] = None
-    requirements: ShipRequirements
-
-
-class ShipCargoItem(BaseModel):
-    symbol: str = Field(
-        ..., description="The unique identifier of the cargo item type."
-    )
-    name: str = Field(..., description="The name of the cargo item type.")
-    description: str = Field(..., description="The description of the cargo item type.")
-    units: Annotated[
-        int,
-        conint(ge=1),
-        Field(..., description="The number of units of the cargo item."),
-    ]
-
-
-class Consumed(BaseModel):
-    amount: NonNegativeInt = Field(
-        ...,
-        description="The amount of fuel consumed by the most recent transit or action.",
-    )
-    timestamp: datetime = Field(
-        ..., description="The time at which the fuel was consumed."
-    )
-
-
-class ShipFuel(BaseModel):
-    current: NonNegativeInt = Field(
-        ..., description="The current amount of fuel in the ship's tanks."
-    )
-    capacity: NonNegativeInt = Field(
-        ..., description="The maximum amount of fuel the ship's tanks can hold."
-    )
-    consumed: Optional[Consumed] = None
-
-
-class SystemType(str, Enum):
-    neutron_star = "NEUTRON_STAR"
-    red_star = "RED_STAR"
-    orange_star = "ORANGE_STAR"
-    blue_star = "BLUE_STAR"
-    young_star = "YOUNG_STAR"
-    white_dwarf = "WHITE_DWARF"
-    black_hole = "BLACK_HOLE"
-    hypergiant = "HYPERGIANT"
-    nebula = "NEBULA"
-    unstable = "UNSTABLE"
-
-
-class SystemWaypoint(BaseModel):
-    symbol: str
-    type: WaypointType
-    x: int
-    y: int
-
-
-class SystemFaction(BaseModel):
-    symbol: NonEmptyStr
-
-
-class WaypointOrbital(BaseModel):
-    symbol: NonEmptyStr
-
-
-class WaypointFaction(BaseModel):
-    symbol: NonEmptyStr
-
-
-class WaypointTraitEnum(str, Enum):
-    uncharted = "UNCHARTED"
-    marketplace = "MARKETPLACE"
-    shipyard = "SHIPYARD"
-    outpost = "OUTPOST"
-    scattered_settlements = "SCATTERED_SETTLEMENTS"
-    sprawling_cities = "SPRAWLING_CITIES"
-    mega_structures = "MEGA_STRUCTURES"
-    overcrowded = "OVERCROWDED"
-    high_tech = "HIGH_TECH"
-    corrupt = "CORRUPT"
-    bureaucratic = "BUREAUCRATIC"
-    trading_hub = "TRADING_HUB"
-    industrial = "INDUSTRIAL"
-    black_market = "BLACK_MARKET"
-    research_facility = "RESEARCH_FACILITY"
-    military_base = "MILITARY_BASE"
-    surveillance_outpost = "SURVEILLANCE_OUTPOST"
-    exploration_outpost = "EXPLORATION_OUTPOST"
-    mineral_deposits = "MINERAL_DEPOSITS"
-    common_metal_deposits = "COMMON_METAL_DEPOSITS"
-    precious_metal_deposits = "PRECIOUS_METAL_DEPOSITS"
-    rare_metal_deposits = "RARE_METAL_DEPOSITS"
-    methane_pools = "METHANE_POOLS"
-    ice_crystals = "ICE_CRYSTALS"
-    explosive_gases = "EXPLOSIVE_GASES"
-    strong_magnetosphere = "STRONG_MAGNETOSPHERE"
-    vibrant_auroras = "VIBRANT_AURORAS"
-    salt_flats = "SALT_FLATS"
-    canyons = "CANYONS"
-    perpetual_daylight = "PERPETUAL_DAYLIGHT"
-    perpetual_overcast = "PERPETUAL_OVERCAST"
-    dry_seabeds = "DRY_SEABEDS"
-    magma_seas = "MAGMA_SEAS"
-    supervolcanoes = "SUPERVOLCANOES"
-    ash_clouds = "ASH_CLOUDS"
-    vast_ruins = "VAST_RUINS"
-    mutated_flora = "MUTATED_FLORA"
-    terraformed = "TERRAFORMED"
-    extreme_temperatures = "EXTREME_TEMPERATURES"
-    extreme_pressure = "EXTREME_PRESSURE"
-    diverse_life = "DIVERSE_LIFE"
-    scarce_life = "SCARCE_LIFE"
-    fossils = "FOSSILS"
-    weak_gravity = "WEAK_GRAVITY"
-    strong_gravity = "STRONG_GRAVITY"
-    crushing_gravity = "CRUSHING_GRAVITY"
-    toxic_atmosphere = "TOXIC_ATMOSPHERE"
-    corrosive_atmosphere = "CORROSIVE_ATMOSPHERE"
-    breathable_atmosphere = "BREATHABLE_ATMOSPHERE"
-    jovian = "JOVIAN"
-    rocky = "ROCKY"
-    volcanic = "VOLCANIC"
-    frozen = "FROZEN"
-    swamp = "SWAMP"
-    barren = "BARREN"
-    temperate = "TEMPERATE"
-    jungle = "JUNGLE"
-    ocean = "OCEAN"
-    stripped = "STRIPPED"
-
-
-class WaypointTrait(BaseModel):
-    symbol: WaypointTraitEnum = Field(
-        ..., description="The unique identifier of the trait."
-    )
-    name: str = Field(..., description="The name of the trait.")
-    description: str = Field(..., description="A description of the trait.")
-
-
-class Chart(BaseModel):
-    waypoint_symbol: Optional[str] = Field(None, alias="waypointSymbol")
-    submitted_by: Optional[str] = Field(None, alias="submittedBy")
-    submitted_on: Optional[datetime] = Field(None, alias="submittedOn")
-
-
-class TradeSymbol(str, Enum):
-    precious_stones = "PRECIOUS_STONES"
-    quartz_sand = "QUARTZ_SAND"
-    silicon_crystals = "SILICON_CRYSTALS"
-    ammonia_ice = "AMMONIA_ICE"
-    liquid_hydrogen = "LIQUID_HYDROGEN"
-    liquid_nitrogen = "LIQUID_NITROGEN"
-    ice_water = "ICE_WATER"
-    exotic_matter = "EXOTIC_MATTER"
-    advanced_circuitry = "ADVANCED_CIRCUITRY"
-    graviton_emitters = "GRAVITON_EMITTERS"
-    iron = "IRON"
-    iron_ore = "IRON_ORE"
-    copper = "COPPER"
-    copper_ore = "COPPER_ORE"
-    aluminum = "ALUMINUM"
-    aluminum_ore = "ALUMINUM_ORE"
-    silver = "SILVER"
-    silver_ore = "SILVER_ORE"
-    gold = "GOLD"
-    gold_ore = "GOLD_ORE"
-    platinum = "PLATINUM"
-    platinum_ore = "PLATINUM_ORE"
-    diamonds = "DIAMONDS"
-    uranite = "URANITE"
-    uranite_ore = "URANITE_ORE"
-    meritium = "MERITIUM"
-    meritium_ore = "MERITIUM_ORE"
-    hydrocarbon = "HYDROCARBON"
-    antimatter = "ANTIMATTER"
-    fertilizers = "FERTILIZERS"
-    fabrics = "FABRICS"
-    food = "FOOD"
-    jewelry = "JEWELRY"
-    machinery = "MACHINERY"
-    firearms = "FIREARMS"
-    assault_rifles = "ASSAULT_RIFLES"
-    military_equipment = "MILITARY_EQUIPMENT"
-    explosives = "EXPLOSIVES"
-    lab_instruments = "LAB_INSTRUMENTS"
-    ammunition = "AMMUNITION"
-    electronics = "ELECTRONICS"
-    ship_plating = "SHIP_PLATING"
-    equipment = "EQUIPMENT"
-    fuel = "FUEL"
-    medicine = "MEDICINE"
-    drugs = "DRUGS"
-    clothing = "CLOTHING"
-    microprocessors = "MICROPROCESSORS"
-    plastics = "PLASTICS"
-    polynucleotides = "POLYNUCLEOTIDES"
-    biocomposites = "BIOCOMPOSITES"
-    nanobots = "NANOBOTS"
-    ai_mainframes = "AI_MAINFRAMES"
-    quantum_drives = "QUANTUM_DRIVES"
-    robotic_drones = "ROBOTIC_DRONES"
-    cyber_implants = "CYBER_IMPLANTS"
-    gene_therapeutics = "GENE_THERAPEUTICS"
-    neural_chips = "NEURAL_CHIPS"
-    mood_regulators = "MOOD_REGULATORS"
-    viral_agents = "VIRAL_AGENTS"
-    micro_fusion_generators = "MICRO_FUSION_GENERATORS"
-    supergrains = "SUPERGRAINS"
-    laser_rifles = "LASER_RIFLES"
-    holographics = "HOLOGRAPHICS"
-    ship_salvage = "SHIP_SALVAGE"
-    relic_tech = "RELIC_TECH"
-    novel_lifeforms = "NOVEL_LIFEFORMS"
-    botanical_specimens = "BOTANICAL_SPECIMENS"
-    cultural_artifacts = "CULTURAL_ARTIFACTS"
-    reactor_solar_i = "REACTOR_SOLAR_I"
-    reactor_fusion_i = "REACTOR_FUSION_I"
-    reactor_fission_i = "REACTOR_FISSION_I"
-    reactor_chemical_i = "REACTOR_CHEMICAL_I"
-    reactor_antimatter_i = "REACTOR_ANTIMATTER_I"
-    engine_impulse_drive_i = "ENGINE_IMPULSE_DRIVE_I"
-    engine_ion_drive_i = "ENGINE_ION_DRIVE_I"
-    engine_ion_drive_ii = "ENGINE_ION_DRIVE_II"
-    engine_hyper_drive_i = "ENGINE_HYPER_DRIVE_I"
-    module_mineral_processor_i = "MODULE_MINERAL_PROCESSOR_I"
-    module_cargo_hold_i = "MODULE_CARGO_HOLD_I"
-    module_crew_quarters_i = "MODULE_CREW_QUARTERS_I"
-    module_envoy_quarters_i = "MODULE_ENVOY_QUARTERS_I"
-    module_passenger_cabin_i = "MODULE_PASSENGER_CABIN_I"
-    module_micro_refinery_i = "MODULE_MICRO_REFINERY_I"
-    module_ore_refinery_i = "MODULE_ORE_REFINERY_I"
-    module_fuel_refinery_i = "MODULE_FUEL_REFINERY_I"
-    module_science_lab_i = "MODULE_SCIENCE_LAB_I"
-    module_jump_drive_i = "MODULE_JUMP_DRIVE_I"
-    module_jump_drive_ii = "MODULE_JUMP_DRIVE_II"
-    module_jump_drive_iii = "MODULE_JUMP_DRIVE_III"
-    module_warp_drive_i = "MODULE_WARP_DRIVE_I"
-    module_warp_drive_ii = "MODULE_WARP_DRIVE_II"
-    module_warp_drive_iii = "MODULE_WARP_DRIVE_III"
-    module_shield_generator_i = "MODULE_SHIELD_GENERATOR_I"
-    module_shield_generator_ii = "MODULE_SHIELD_GENERATOR_II"
-    mount_gas_siphon_i = "MOUNT_GAS_SIPHON_I"
-    mount_gas_siphon_ii = "MOUNT_GAS_SIPHON_II"
-    mount_gas_siphon_iii = "MOUNT_GAS_SIPHON_III"
-    mount_surveyor_i = "MOUNT_SURVEYOR_I"
-    mount_surveyor_ii = "MOUNT_SURVEYOR_II"
-    mount_surveyor_iii = "MOUNT_SURVEYOR_III"
-    mount_sensor_array_i = "MOUNT_SENSOR_ARRAY_I"
-    mount_sensor_array_ii = "MOUNT_SENSOR_ARRAY_II"
-    mount_sensor_array_iii = "MOUNT_SENSOR_ARRAY_III"
-    mount_mining_laser_i = "MOUNT_MINING_LASER_I"
-    mount_mining_laser_ii = "MOUNT_MINING_LASER_II"
-    mount_mining_laser_iii = "MOUNT_MINING_LASER_III"
-    mount_laser_cannon_i = "MOUNT_LASER_CANNON_I"
-    mount_missile_launcher_i = "MOUNT_MISSILE_LAUNCHER_I"
-    mount_turret_i = "MOUNT_TURRET_I"
-
-
-class Type1(str, Enum):
-    purchase = "PURCHASE"
-    sell = "SELL"
-
-
-class MarketTransaction(BaseModel):
-    waypoint_symbol: str = Field(
-        ...,
-        alias="waypointSymbol",
-        description="The symbol of the waypoint where the transaction took place.",
-    )
-    ship_symbol: str = Field(
-        ...,
-        alias="shipSymbol",
-        description="The symbol of the ship that made the transaction.",
-    )
-    trade_symbol: str = Field(
-        ..., alias="tradeSymbol", description="The symbol of the trade good."
-    )
-    type: Type1 = Field(..., description="The type of transaction.")
-    units: Annotated[
-        int,
-        conint(ge=1),
-        Field(..., description="The number of units of the transaction."),
-    ]
-    price_per_unit: Annotated[
-        int,
-        conint(ge=1),
-        Field(
-            ...,
-            alias="pricePerUnit",
-            description="The price per unit of the transaction.",
-        ),
-    ]
-    total_price: Annotated[
-        int,
-        conint(ge=1),
-        Field(
-            ..., alias="totalPrice", description="The total price of the transaction."
-        ),
-    ]
-    timestamp: datetime = Field(..., description="The timestamp of the transaction.")
-
-
-class Supply(str, Enum):
-    scarce = "SCARCE"
-    limited = "LIMITED"
-    moderate = "MODERATE"
-    abundant = "ABUNDANT"
-
-
-class MarketTradeGood(BaseModel):
-    symbol: str = Field(..., description="The symbol of the trade good.")
-    trade_volume: Annotated[
-        int,
-        conint(ge=1),
-        Field(
-            ...,
-            alias="tradeVolume",
-            description=(
-                "The typical volume flowing through the market for this type of good. The"
-                " larger the trade volume, the more stable prices will be."
-            ),
-        ),
-    ]
-    supply: Supply = Field(
-        ...,
-        description=(
-            "A rough estimate of the total supply of this good in the marketplace."
-        ),
-    )
-    purchase_price: NonNegativeInt = Field(
-        ...,
-        alias="purchasePrice",
-        description="The price at which this good can be purchased from the market.",
-    )
-    sell_price: NonNegativeInt = Field(
-        ...,
-        alias="sellPrice",
-        description="The price at which this good can be sold to the market.",
-    )
-
-
-class ShipType(str, Enum):
-    ship_probe = "SHIP_PROBE"
-    ship_mining_drone = "SHIP_MINING_DRONE"
-    ship_interceptor = "SHIP_INTERCEPTOR"
-    ship_light_hauler = "SHIP_LIGHT_HAULER"
-    ship_command_frigate = "SHIP_COMMAND_FRIGATE"
-    ship_explorer = "SHIP_EXPLORER"
-    ship_heavy_freighter = "SHIP_HEAVY_FREIGHTER"
-    ship_light_shuttle = "SHIP_LIGHT_SHUTTLE"
-    ship_ore_hound = "SHIP_ORE_HOUND"
-    ship_refining_freighter = "SHIP_REFINING_FREIGHTER"
-
-
-class ShipyardTransaction(BaseModel):
-    waypoint_symbol: str = Field(
-        ...,
-        alias="waypointSymbol",
-        description="The symbol of the waypoint where the transaction took place.",
-    )
-    ship_symbol: str = Field(
-        ...,
-        alias="shipSymbol",
-        description="The symbol of the ship that was purchased.",
-    )
-    price: Annotated[
-        int, conint(ge=1), Field(..., description="The price of the transaction.")
-    ]
-    agent_symbol: str = Field(
-        ...,
-        alias="agentSymbol",
-        description="The symbol of the agent that made the transaction.",
-    )
-    timestamp: datetime = Field(..., description="The timestamp of the transaction.")
-
-
-class ConnectedSystem(BaseModel):
-    symbol: NonEmptyStr
-    sector_symbol: NonEmptyStr = Field(..., alias="sectorSymbol")
-    type: SystemType
-    faction_symbol: Optional[str] = Field(
-        None,
-        alias="factionSymbol",
-        description=(
-            "The symbol of the faction that owns the connected jump gate in the system."
-        ),
-    )
-    x: int
-    y: int
-    distance: int
-
-
-class Produce(str, Enum):
-    iron = "IRON"
-    copper = "COPPER"
-    silver = "SILVER"
-    gold = "GOLD"
-    aluminum = "ALUMINUM"
-    platinum = "PLATINUM"
-    uranite = "URANITE"
-    meritium = "MERITIUM"
-    fuel = "FUEL"
-
-
-class ProducedItem(BaseModel):
-    trade_symbol: Optional[str] = Field(None, alias="tradeSymbol")
-    units: Optional[int] = None
-
-
-class ConsumedItem(BaseModel):
-    trade_symbol: Optional[str] = Field(None, alias="tradeSymbol")
-    units: Optional[int] = None
-
-
-class Cooldown(BaseModel):
-    ship_symbol: NonEmptyStr = Field(
-        ...,
-        alias="shipSymbol",
-        description="The symbol of the ship that is on cooldown",
-    )
-    total_seconds: NonNegativeInt = Field(
-        ...,
-        alias="totalSeconds",
-        description="The total duration of the cooldown in seconds",
-    )
-    remaining_seconds: NonNegativeInt = Field(
-        ...,
-        alias="remainingSeconds",
-        description="The remaining duration of the cooldown in seconds",
-    )
-    expiration: datetime = Field(
-        ...,
-        description="The date and time when the cooldown expires in ISO 8601 format",
-    )
-
-
-class Size(str, Enum):
-    small = "SMALL"
-    moderate = "MODERATE"
-    large = "LARGE"
-
-
-class SurveyDeposit(BaseModel):
-    symbol: str = Field(..., description="The symbol of the deposit.")
-
-
-class ExtractionYield(BaseModel):
-    symbol: NonEmptyStr
-    units: int = Field(
-        ...,
-        description=(
-            "The number of units extracted that were placed into the ship's cargo hold."
-        ),
-    )
-
-
-class ScannedSystem(BaseModel):
-    symbol: NonEmptyStr
-    sector_symbol: NonEmptyStr = Field(..., alias="sectorSymbol")
-    type: SystemType
-    x: int
-    y: int
-    distance: int
-
-
-class Frame(BaseModel):
-    symbol: str
-
-
-class Reactor(BaseModel):
-    symbol: str
-
-
-class Engine(BaseModel):
-    symbol: str
-
-
-class Mount(BaseModel):
-    symbol: str
-
-
-class ContractTerms(BaseModel):
-    deadline: datetime = Field(..., description="The deadline for the contract.")
-    payment: ContractPayment
-    deliver: Optional[List[ContractDeliverGood]] = None
-
-
-class Faction(BaseModel):
-    symbol: NonEmptyStr
-    name: NonEmptyStr
-    description: NonEmptyStr
-    headquarters: NonEmptyStr
-    traits: List[FactionTrait]
-
-
-class ShipRegistration(BaseModel):
-    name: NonEmptyStr = Field(
-        ..., description="The agent's registered name of the ship"
-    )
-    faction_symbol: Optional[NonEmptyStr] = Field(
-        None,
-        alias="factionSymbol",
-        description="The symbol of the faction the ship is registered with",
-    )
-    role: ShipRole
-
-
-class ShipNavRouteWaypoint(BaseModel):
-    symbol: NonEmptyStr
-    type: WaypointType
-    system_symbol: NonEmptyStr = Field(..., alias="systemSymbol")
-    x: int
-    y: int
-
-
-class ShipFrame(BaseModel):
-    symbol: FramesEnum
-    name: str
-    description: str
-    condition: Optional[ShipCondition] = None
-    module_slots: NonNegativeInt = Field(..., alias="moduleSlots")
-    mounting_points: NonNegativeInt = Field(..., alias="mountingPoints")
-    fuel_capacity: NonNegativeInt = Field(..., alias="fuelCapacity")
-    requirements: ShipRequirements
-
-
-class ShipCargo(BaseModel):
-    capacity: NonNegativeInt = Field(
-        ..., description="The max number of items that can be stored in the cargo hold."
-    )
-    units: NonNegativeInt = Field(
-        ..., description="The number of items currently stored in the cargo hold."
-    )
-    inventory: List[ShipCargoItem] = Field(
-        ..., description="The items currently in the cargo hold."
-    )
-
-
-class System(BaseModel):
-    symbol: NonEmptyStr
-    sector_symbol: NonEmptyStr = Field(..., alias="sectorSymbol")
-    type: SystemType
-    x: int
-    y: int
-    waypoints: List[SystemWaypoint]
-    factions: List[SystemFaction]
-
-
-class Waypoint(BaseModel):
-    symbol: NonEmptyStr
-    type: WaypointType
-    system_symbol: NonEmptyStr = Field(..., alias="systemSymbol")
-    x: int
-    y: int
-    orbitals: List[WaypointOrbital]
-    faction: Optional[WaypointFaction] = None
-    traits: List[WaypointTrait] = Field(..., description="The traits of the waypoint.")
-    chart: Optional[Chart] = None
-
-
-class TradeGood(BaseModel):
-    symbol: TradeSymbol
-    name: str
-    description: str
-
-
-class ShipTypeModel(BaseModel):
-    type: Optional[ShipType] = None
-
-
-class ShipyardShip(BaseModel):
-    type: Optional[ShipType] = None
-    name: str
-    description: str
-    purchase_price: int = Field(..., alias="purchasePrice")
-    frame: ShipFrame
-    reactor: ShipReactor
-    engine: ShipEngine
-    modules: List[ShipModule]
-    mounts: List[ShipMount]
-
-
-class JumpGate(BaseModel):
-    jump_range: float = Field(
-        ..., alias="jumpRange", description="The maximum jump range of the gate."
-    )
-    faction_symbol: Optional[str] = Field(
-        None,
-        alias="factionSymbol",
-        description="The symbol of the faction that owns the gate.",
-    )
-    connected_systems: List[ConnectedSystem] = Field(
-        ...,
-        alias="connectedSystems",
-        description=(
-            "The systems within range of the gate that have a corresponding gate."
-        ),
-    )
-
-
-class ShipRefineResult(BaseModel):
-    cargo: ShipCargo
-    cooldown: Cooldown
-    produced: List[ProducedItem]
-    consumed: List[ConsumedItem]
-
-
-class ChartShipResult(BaseModel):
-    chart: Chart
-    waypoint: Waypoint
-
-
-class Survey(BaseModel):
-    signature: NonEmptyStr = Field(
-        ...,
-        description=(
-            "A unique signature for the location of this survey. This signature is"
-            " verified when attempting an extraction using this survey."
-        ),
-    )
-    symbol: NonEmptyStr = Field(
-        ..., description="The symbol of the waypoint that this survey is for."
-    )
-    deposits: List[SurveyDeposit] = Field(
-        ..., description="A list of deposits that can be found at this location."
-    )
-    expiration: datetime = Field(
-        ...,
-        description=(
-            "The date and time when the survey expires. After this date and time, the"
-            " survey will no longer be available for extraction."
-        ),
-    )
-    size: Size = Field(
-        ...,
-        description=(
-            "The size of the deposit. This value indicates how much can be extracted"
-            " from the survey before it is exhausted."
-        ),
-    )
-
-
-class Extraction(BaseModel):
-    ship_symbol: NonEmptyStr = Field(..., alias="shipSymbol")
-    yield_: ExtractionYield = Field(..., alias="yield")
-
-
-class SellCargoResult(BaseModel):
-    agent: AgentSchema
-    cargo: ShipCargo
-    transaction: MarketTransaction
-
-
-class RefuelShipResult(BaseModel):
-    agent: AgentSchema
-    fuel: ShipFuel
-
-
-class ScanSystemsResult(BaseModel):
-    cooldown: Cooldown
-    systems: List[ScannedSystem]
-
-
-class ScanWaypointsResult(BaseModel):
-    cooldown: Cooldown
-    waypoints: List[Waypoint]
-
-
-class PurchaseCargoResult(BaseModel):
-    agent: AgentSchema
-    cargo: ShipCargo
-    transaction: MarketTransaction
-
-
-class ContractSchema(BaseModel):
-    id: NonEmptyStr
-    faction_symbol: NonEmptyStr = Field(
-        ...,
-        alias="factionSymbol",
-        description="The symbol of the faction that this contract is for.",
-    )
-    type: ContractType
-    terms: ContractTerms
-    accepted: bool = Field(
-        ..., description="Whether the contract has been accepted by the agent"
-    )
-    fulfilled: bool = Field(..., description="Whether the contract has been fulfilled")
-    expiration: datetime = Field(
-        ..., description="The time at which the contract expires"
-    )
-
-
-class ShipNavRoute(BaseModel):
-    destination: ShipNavRouteWaypoint
-    departure: ShipNavRouteWaypoint
-    departure_time: datetime = Field(
-        ..., alias="departureTime", description="The date time of the ship's departure."
-    )
-    arrival: datetime = Field(
-        ...,
-        description=(
-            "The date time of the ship's arrival. If the ship is in-transit, this is"
-            " the expected time of arrival."
-        ),
-    )
-
-
-class Market(BaseModel):
-    symbol: str = Field(
-        ...,
-        description=(
-            "The symbol of the market. The symbol is the same as the waypoint where the"
-            " market is located."
-        ),
-    )
-    exports: List[TradeGood] = Field(
-        ..., description="The list of goods that are exported from this market."
-    )
-    imports: List[TradeGood] = Field(
-        ..., description="The list of goods that are sought as imports in this market."
-    )
-    exchange: List[TradeGood] = Field(
-        ...,
-        description=(
-            "The list of goods that are bought and sold between agents at this market."
-        ),
-    )
-    transactions: Optional[List[MarketTransaction]] = Field(
-        None,
-        description=(
-            "The list of recent transactions at this market. Visible only when a ship"
-            " is present at the market."
-        ),
-    )
-    trade_goods: Optional[List[MarketTradeGood]] = Field(
-        None,
-        alias="tradeGoods",
-        description=(
-            "The list of goods that are traded at this market. Visible only when a ship"
-            " is present at the market."
-        ),
-    )
-
-
-class Shipyard(BaseModel):
-    symbol: NonEmptyStr = Field(
-        ...,
-        description=(
-            "The symbol of the shipyard. The symbol is the same as the waypoint where"
-            " the shipyard is located."
-        ),
-    )
-    ship_types: List[ShipTypeModel] = Field(
-        ...,
-        alias="shipTypes",
-        description="The list of ship types available for purchase at this shipyard.",
-    )
-    transactions: Optional[List[ShipyardTransaction]] = Field(
-        None, description="The list of recent transactions at this shipyard."
-    )
-    ships: Optional[List[ShipyardShip]] = Field(
-        None,
-        description=(
-            "The ships that are currently available for purchase at the shipyard."
-        ),
-    )
-
-
-class AcceptContractResult(BaseModel):
-    agent: AgentSchema
-    contract: ContractSchema
-
-
-class DeliverContractResult(BaseModel):
-    contract: ContractSchema
-    cargo: ShipCargo
-
-
-class FullfillContractResult(AcceptContractResult):
-    pass
-
-
-class CreateSurveyResult(BaseModel):
-    cooldown: Cooldown
-    surveys: List[Survey]
-
-
-class ExtractResourcesResult(BaseModel):
-    cooldown: Cooldown
-    extraction: Extraction
-    cargo: ShipCargo
-
-
-class ShipNav(BaseModel):
-    system_symbol: str = Field(
-        ...,
-        alias="systemSymbol",
-        description="The system symbol of the ship's current location.",
-    )
-    waypoint_symbol: str = Field(
-        ...,
-        alias="waypointSymbol",
-        description=(
-            "The waypoint symbol of the ship's current location, or if the ship is"
-            " in-transit, the waypoint symbol of the ship's destination."
-        ),
-    )
-    route: ShipNavRoute
-    status: ShipNavStatus
-    flight_mode: ShipNavFlightMode = Field(..., alias="flightMode")
-
-
-class ShipJumpResult(BaseModel):
-    cooldown: Cooldown
-    nav: Optional[ShipNav] = None
-
-
-class ShipNavigateResult(BaseModel):
-    fuel: ShipFuel
-    nav: ShipNav
-
-
-class ScannedShip(BaseModel):
-    symbol: str = Field(..., description="The globally unique identifier of the ship.")
-    registration: ShipRegistration
-    nav: ShipNav
-    frame: Optional[Frame] = Field(None, description="The frame of the ship.")
-    reactor: Optional[Reactor] = Field(None, description="The reactor of the ship.")
-    engine: Engine = Field(..., description="The engine of the ship.")
-    mounts: Optional[List[Mount]] = None
-
-
-class ShipSchema(BaseModel):
-    symbol: str = Field(
-        ...,
-        description=(
-            "The globally unique identifier of the ship in the following format:"
-            " `[AGENT_SYMBOL]_[HEX_ID]`"
-        ),
-    )
-    registration: ShipRegistration
-    nav: ShipNav
-    crew: ShipCrew
-    frame: ShipFrame
-    reactor: ShipReactor
-    engine: ShipEngine
-    modules: List[ShipModule]
-    mounts: List[ShipMount]
-    cargo: ShipCargo
-    fuel: ShipFuel
-
-
-class PurchaseShipResult(BaseModel):
-    agent: AgentSchema
-    ship: ShipSchema
-    transaction: ShipyardTransaction
-
-
-class ScanShipsResult(BaseModel):
-    cooldown: Cooldown
-    ships: List[ScannedShip]
-
-
-class RegisterData(BaseModel):
-    agent: AgentSchema
-    contract: ContractSchema
-    faction: Faction
-    ship: ShipSchema
-    token: str = Field(
-        ..., description="A Bearer token for accessing secured API endpoints."
-    )
-
-
-class RegisterResponse(BaseModel):
-    data: RegisterData
+from __future__ import annotations
+
+from datetime import datetime
+from enum import Enum
+from typing import List, Optional, TypeVar, Generic, Annotated
+
+from pydantic import Field, confloat, conint, BaseModel, ConstrainedStr, NonNegativeInt
+from pydantic.generics import GenericModel
+
+T = TypeVar("T")
+
+
+class NonEmptyStr(ConstrainedStr):
+    strict = True
+    min_length = 1
+
+
+class Meta(BaseModel):
+    total: int
+    page: int
+    limit: int
+
+
+class PaginatedObject(GenericModel, Generic[T]):
+    objects: list[T] = Field(alias="data")
+    meta: Meta
+
+
+class FactionsEnum(str, Enum):
+    cosmic = "COSMIC"
+    void = "VOID"
+    galactic = "GALACTIC"
+    quantum = "QUANTUM"
+    dominion = "DOMINION"
+
+
+class RegisterRequestData(BaseModel):
+    faction: FactionsEnum = Field(
+        ..., description="The faction you choose determines your headquarters."
+    )
+    symbol: Annotated[
+        str,
+        constr(min_length=3, max_length=14),
+        Field(
+            ...,
+            description="How other agents will see your ships and information.",
+            example="BADGER",
+        ),
+    ]
+
+
+class AgentSchema(BaseModel):
+    account_id: NonEmptyStr = Field(..., alias="accountId")
+    symbol: NonEmptyStr
+    headquarters: NonEmptyStr = Field(..., description="The headquarters of the agent.")
+    credits: int = Field(
+        ...,
+        description=(
+            "The number of credits the agent has available. Credits can be negative if"
+            " funds have been overdrawn."
+        ),
+    )
+
+
+class ContractType(str, Enum):
+    procurement = "PROCUREMENT"
+    transport = "TRANSPORT"
+    shuttle = "SHUTTLE"
+
+
+class ContractPayment(BaseModel):
+    on_accepted: int = Field(
+        ...,
+        alias="onAccepted",
+        description=(
+            "The amount of credits received up front for accepting the contract."
+        ),
+    )
+    on_fulfilled: int = Field(
+        ...,
+        alias="onFulfilled",
+        description="The amount of credits received when the contract is fulfilled.",
+    )
+
+
+class ContractDeliverGood(BaseModel):
+    trade_symbol: NonEmptyStr = Field(
+        ..., alias="tradeSymbol", description="The symbol of the trade good to deliver."
+    )
+    destination_symbol: NonEmptyStr = Field(
+        ...,
+        alias="destinationSymbol",
+        description="The destination where goods need to be delivered.",
+    )
+    units_required: int = Field(
+        ...,
+        alias="unitsRequired",
+        description="The number of units that need to be delivered on this contract.",
+    )
+    units_fulfilled: int = Field(
+        ...,
+        alias="unitsFulfilled",
+        description="The number of units fulfilled on this contract.",
+    )
+
+
+class FactionTraitEnum(str, Enum):
+    bureaucratic = "BUREAUCRATIC"
+    secretive = "SECRETIVE"
+    capitalistic = "CAPITALISTIC"
+    industrious = "INDUSTRIOUS"
+    peaceful = "PEACEFUL"
+    distrustful = "DISTRUSTFUL"
+    welcoming = "WELCOMING"
+    anarchist = "ANARCHIST"
+    conflicted = "CONFLICTED"
+    authoritarian = "AUTHORITARIAN"
+    oligarchical = "OLIGARCHICAL"
+    dynastic = "DYNASTIC"
+    democractic = "DEMOCRACTIC"
+    decentralized = "DECENTRALIZED"
+    smugglers = "SMUGGLERS"
+    scavengers = "SCAVENGERS"
+    rebellious = "REBELLIOUS"
+    exiles = "EXILES"
+    pirates = "PIRATES"
+    raiders = "RAIDERS"
+    clan = "CLAN"
+    guild = "GUILD"
+    dominion = "DOMINION"
+    fringe = "FRINGE"
+    forsaken = "FORSAKEN"
+    isolated = "ISOLATED"
+    localized = "LOCALIZED"
+    established = "ESTABLISHED"
+    notable = "NOTABLE"
+    dominant = "DOMINANT"
+    inescapable = "INESCAPABLE"
+    innovative = "INNOVATIVE"
+    bold = "BOLD"
+    visionary = "VISIONARY"
+    curious = "CURIOUS"
+    daring = "DARING"
+    exploratory = "EXPLORATORY"
+    resourceful = "RESOURCEFUL"
+    flexible = "FLEXIBLE"
+    cooperative = "COOPERATIVE"
+    united = "UNITED"
+    strategic = "STRATEGIC"
+    intelligent = "INTELLIGENT"
+    research_focused = "RESEARCH_FOCUSED"
+    collaborative = "COLLABORATIVE"
+    progressive = "PROGRESSIVE"
+    militaristic = "MILITARISTIC"
+    technologically_advanced = "TECHNOLOGICALLY_ADVANCED"
+    aggressive = "AGGRESSIVE"
+    imperialistic = "IMPERIALISTIC"
+    treasure_hunters = "TREASURE_HUNTERS"
+    dexterous = "DEXTEROUS"
+    unpredictable = "UNPREDICTABLE"
+    brutal = "BRUTAL"
+    fleeting = "FLEETING"
+    adaptable = "ADAPTABLE"
+    self_sufficient = "SELF_SUFFICIENT"
+    defensive = "DEFENSIVE"
+    proud = "PROUD"
+    diverse = "DIVERSE"
+    independent = "INDEPENDENT"
+    self_interested = "SELF_INTERESTED"
+    fragmented = "FRAGMENTED"
+    commercial = "COMMERCIAL"
+    free_markets = "FREE_MARKETS"
+    entrepreneurial = "ENTREPRENEURIAL"
+
+
+class FactionTrait(BaseModel):
+    symbol: FactionTraitEnum = Field(
+        ..., description="The unique identifier of the trait."
+    )
+    name: str = Field(..., description="The name of the trait.")
+    description: str = Field(..., description="A description of the trait.")
+
+
+class ShipRole(str, Enum):
+    fabricator = "FABRICATOR"
+    harvester = "HARVESTER"
+    hauler = "HAULER"
+    interceptor = "INTERCEPTOR"
+    excavator = "EXCAVATOR"
+    transport = "TRANSPORT"
+    repair = "REPAIR"
+    surveyor = "SURVEYOR"
+    command = "COMMAND"
+    carrier = "CARRIER"
+    patrol = "PATROL"
+    satellite = "SATELLITE"
+    explorer = "EXPLORER"
+    refinery = "REFINERY"
+
+
+class WaypointType(str, Enum):
+    planet = "PLANET"
+    gas_giant = "GAS_GIANT"
+    moon = "MOON"
+    orbital_station = "ORBITAL_STATION"
+    jump_gate = "JUMP_GATE"
+    asteroid_field = "ASTEROID_FIELD"
+    nebula = "NEBULA"
+    debris_field = "DEBRIS_FIELD"
+    gravity_well = "GRAVITY_WELL"
+
+
+class ShipNavStatus(str, Enum):
+    in_transit = "IN_TRANSIT"
+    in_orbit = "IN_ORBIT"
+    docked = "DOCKED"
+
+
+class ShipNavFlightMode(str, Enum):
+    drift = "DRIFT"
+    stealth = "STEALTH"
+    cruise = "CRUISE"
+    burn = "BURN"
+
+
+class Rotation(str, Enum):
+    strict = "STRICT"
+    relaxed = "RELAXED"
+
+
+class ShipCrew(BaseModel):
+    current: int = Field(
+        ..., description="The current number of crew members on the ship."
+    )
+    required: int = Field(
+        ...,
+        description="The minimum number of crew members required to maintain the ship.",
+    )
+    capacity: int = Field(
+        ..., description="The maximum number of crew members the ship can support."
+    )
+    rotation: Rotation = Field(
+        ...,
+        description=(
+            "The rotation of crew shifts. A stricter shift improves the ship's"
+            " performance. A more relaxed shift improves the crew's morale."
+        ),
+    )
+    morale: Annotated[
+        int,
+        conint(ge=0, le=100),
+        Field(
+            ...,
+            description=(
+                "A rough measure of the crew's morale. A higher morale means the crew is"
+                " happier and more productive. A lower morale means the ship is more prone"
+                " to accidents."
+            ),
+        ),
+    ]
+    wages: NonNegativeInt = Field(
+        ...,
+        description=(
+            "The amount of credits per crew member paid per hour. Wages are paid when a"
+            " ship docks at a civilized waypoint."
+        ),
+    )
+
+
+class FramesEnum(str, Enum):
+    frame_probe = "FRAME_PROBE"
+    frame_drone = "FRAME_DRONE"
+    frame_interceptor = "FRAME_INTERCEPTOR"
+    frame_racer = "FRAME_RACER"
+    frame_fighter = "FRAME_FIGHTER"
+    frame_frigate = "FRAME_FRIGATE"
+    frame_shuttle = "FRAME_SHUTTLE"
+    frame_explorer = "FRAME_EXPLORER"
+    frame_miner = "FRAME_MINER"
+    frame_light_freighter = "FRAME_LIGHT_FREIGHTER"
+    frame_heavy_freighter = "FRAME_HEAVY_FREIGHTER"
+    frame_transport = "FRAME_TRANSPORT"
+    frame_destroyer = "FRAME_DESTROYER"
+    frame_cruiser = "FRAME_CRUISER"
+    frame_carrier = "FRAME_CARRIER"
+
+
+class ShipCondition(BaseModel):
+    __root__: Annotated[
+        int,
+        conint(ge=0, le=100),
+        Field(
+            ...,
+            description=(
+                "Condition is a range of 0 to 100 where 0 is completely worn out and 100 is"
+                " brand new."
+            ),
+        ),
+    ]
+
+
+class ShipRequirements(BaseModel):
+    power: Optional[int] = Field(
+        None, description="The amount of power required from the reactor."
+    )
+    crew: Optional[int] = Field(
+        None, description="The number of crew required for operation."
+    )
+    slots: Optional[int] = Field(
+        None, description="The number of module slots required for installation."
+    )
+
+
+class ReactorsEnum(str, Enum):
+    reactor_solar_i = "REACTOR_SOLAR_I"
+    reactor_fusion_i = "REACTOR_FUSION_I"
+    reactor_fission_i = "REACTOR_FISSION_I"
+    reactor_chemical_i = "REACTOR_CHEMICAL_I"
+    reactor_antimatter_i = "REACTOR_ANTIMATTER_I"
+
+
+class ShipReactor(BaseModel):
+    symbol: ReactorsEnum
+    name: str
+    description: str
+    condition: Optional[ShipCondition] = None
+    power_output: Annotated[int, conint(ge=1), Field(..., alias="powerOutput")]
+    requirements: ShipRequirements
+
+
+class EnginesEnum(str, Enum):
+    engine_impulse_drive_i = "ENGINE_IMPULSE_DRIVE_I"
+    engine_ion_drive_i = "ENGINE_ION_DRIVE_I"
+    engine_ion_drive_ii = "ENGINE_ION_DRIVE_II"
+    engine_hyper_drive_i = "ENGINE_HYPER_DRIVE_I"
+
+
+class ShipEngine(BaseModel):
+    symbol: EnginesEnum
+    name: str
+    description: str
+    condition: Optional[ShipCondition] = None
+    speed: Annotated[float, confloat(ge=1.0)]
+    requirements: ShipRequirements
+
+
+class ShipModules(str, Enum):
+    module_mineral_processor_i = "MODULE_MINERAL_PROCESSOR_I"
+    module_cargo_hold_i = "MODULE_CARGO_HOLD_I"
+    module_crew_quarters_i = "MODULE_CREW_QUARTERS_I"
+    module_envoy_quarters_i = "MODULE_ENVOY_QUARTERS_I"
+    module_passenger_cabin_i = "MODULE_PASSENGER_CABIN_I"
+    module_micro_refinery_i = "MODULE_MICRO_REFINERY_I"
+    module_ore_refinery_i = "MODULE_ORE_REFINERY_I"
+    module_fuel_refinery_i = "MODULE_FUEL_REFINERY_I"
+    module_science_lab_i = "MODULE_SCIENCE_LAB_I"
+    module_jump_drive_i = "MODULE_JUMP_DRIVE_I"
+    module_jump_drive_ii = "MODULE_JUMP_DRIVE_II"
+    module_jump_drive_iii = "MODULE_JUMP_DRIVE_III"
+    module_warp_drive_i = "MODULE_WARP_DRIVE_I"
+    module_warp_drive_ii = "MODULE_WARP_DRIVE_II"
+    module_warp_drive_iii = "MODULE_WARP_DRIVE_III"
+    module_shield_generator_i = "MODULE_SHIELD_GENERATOR_I"
+    module_shield_generator_ii = "MODULE_SHIELD_GENERATOR_II"
+
+
+class ShipModule(BaseModel):
+    symbol: ShipModules
+    capacity: Optional[NonNegativeInt] = None
+    range: Optional[NonNegativeInt] = None
+    name: str
+    description: Optional[str] = None
+    requirements: ShipRequirements
+
+
+class ShipMounts(str, Enum):
+    mount_gas_siphon_i = "MOUNT_GAS_SIPHON_I"
+    mount_gas_siphon_ii = "MOUNT_GAS_SIPHON_II"
+    mount_gas_siphon_iii = "MOUNT_GAS_SIPHON_III"
+    mount_surveyor_i = "MOUNT_SURVEYOR_I"
+    mount_surveyor_ii = "MOUNT_SURVEYOR_II"
+    mount_surveyor_iii = "MOUNT_SURVEYOR_III"
+    mount_sensor_array_i = "MOUNT_SENSOR_ARRAY_I"
+    mount_sensor_array_ii = "MOUNT_SENSOR_ARRAY_II"
+    mount_sensor_array_iii = "MOUNT_SENSOR_ARRAY_III"
+    mount_mining_laser_i = "MOUNT_MINING_LASER_I"
+    mount_mining_laser_ii = "MOUNT_MINING_LASER_II"
+    mount_mining_laser_iii = "MOUNT_MINING_LASER_III"
+    mount_laser_cannon_i = "MOUNT_LASER_CANNON_I"
+    mount_missile_launcher_i = "MOUNT_MISSILE_LAUNCHER_I"
+    mount_turret_i = "MOUNT_TURRET_I"
+
+
+class Deposit(str, Enum):
+    quartz_sand = "QUARTZ_SAND"
+    silicon_crystals = "SILICON_CRYSTALS"
+    precious_stones = "PRECIOUS_STONES"
+    ice_water = "ICE_WATER"
+    ammonia_ice = "AMMONIA_ICE"
+    iron_ore = "IRON_ORE"
+    copper_ore = "COPPER_ORE"
+    silver_ore = "SILVER_ORE"
+    aluminum_ore = "ALUMINUM_ORE"
+    gold_ore = "GOLD_ORE"
+    platinum_ore = "PLATINUM_ORE"
+    diamonds = "DIAMONDS"
+    uranite_ore = "URANITE_ORE"
+    meritium_ore = "MERITIUM_ORE"
+
+
+class ShipMount(BaseModel):
+    symbol: ShipMounts
+    name: str
+    description: Optional[str] = None
+    strength: Optional[NonNegativeInt] = None
+    deposits: Optional[List[Deposit]] = None
+    requirements: ShipRequirements
+
+
+class ShipCargoItem(BaseModel):
+    symbol: str = Field(
+        ..., description="The unique identifier of the cargo item type."
+    )
+    name: str = Field(..., description="The name of the cargo item type.")
+    description: str = Field(..., description="The description of the cargo item type.")
+    units: Annotated[
+        int,
+        conint(ge=1),
+        Field(..., description="The number of units of the cargo item."),
+    ]
+
+
+class Consumed(BaseModel):
+    amount: NonNegativeInt = Field(
+        ...,
+        description="The amount of fuel consumed by the most recent transit or action.",
+    )
+    timestamp: datetime = Field(
+        ..., description="The time at which the fuel was consumed."
+    )
+
+
+class ShipFuel(BaseModel):
+    current: NonNegativeInt = Field(
+        ..., description="The current amount of fuel in the ship's tanks."
+    )
+    capacity: NonNegativeInt = Field(
+        ..., description="The maximum amount of fuel the ship's tanks can hold."
+    )
+    consumed: Optional[Consumed] = None
+
+
+class SystemType(str, Enum):
+    neutron_star = "NEUTRON_STAR"
+    red_star = "RED_STAR"
+    orange_star = "ORANGE_STAR"
+    blue_star = "BLUE_STAR"
+    young_star = "YOUNG_STAR"
+    white_dwarf = "WHITE_DWARF"
+    black_hole = "BLACK_HOLE"
+    hypergiant = "HYPERGIANT"
+    nebula = "NEBULA"
+    unstable = "UNSTABLE"
+
+
+class SystemWaypoint(BaseModel):
+    symbol: str
+    type: WaypointType
+    x: int
+    y: int
+
+
+class SystemFaction(BaseModel):
+    symbol: NonEmptyStr
+
+
+class WaypointOrbital(BaseModel):
+    symbol: NonEmptyStr
+
+
+class WaypointFaction(BaseModel):
+    symbol: NonEmptyStr
+
+
+class WaypointTraitEnum(str, Enum):
+    uncharted = "UNCHARTED"
+    marketplace = "MARKETPLACE"
+    shipyard = "SHIPYARD"
+    outpost = "OUTPOST"
+    scattered_settlements = "SCATTERED_SETTLEMENTS"
+    sprawling_cities = "SPRAWLING_CITIES"
+    mega_structures = "MEGA_STRUCTURES"
+    overcrowded = "OVERCROWDED"
+    high_tech = "HIGH_TECH"
+    corrupt = "CORRUPT"
+    bureaucratic = "BUREAUCRATIC"
+    trading_hub = "TRADING_HUB"
+    industrial = "INDUSTRIAL"
+    black_market = "BLACK_MARKET"
+    research_facility = "RESEARCH_FACILITY"
+    military_base = "MILITARY_BASE"
+    surveillance_outpost = "SURVEILLANCE_OUTPOST"
+    exploration_outpost = "EXPLORATION_OUTPOST"
+    mineral_deposits = "MINERAL_DEPOSITS"
+    common_metal_deposits = "COMMON_METAL_DEPOSITS"
+    precious_metal_deposits = "PRECIOUS_METAL_DEPOSITS"
+    rare_metal_deposits = "RARE_METAL_DEPOSITS"
+    methane_pools = "METHANE_POOLS"
+    ice_crystals = "ICE_CRYSTALS"
+    explosive_gases = "EXPLOSIVE_GASES"
+    strong_magnetosphere = "STRONG_MAGNETOSPHERE"
+    vibrant_auroras = "VIBRANT_AURORAS"
+    salt_flats = "SALT_FLATS"
+    canyons = "CANYONS"
+    perpetual_daylight = "PERPETUAL_DAYLIGHT"
+    perpetual_overcast = "PERPETUAL_OVERCAST"
+    dry_seabeds = "DRY_SEABEDS"
+    magma_seas = "MAGMA_SEAS"
+    supervolcanoes = "SUPERVOLCANOES"
+    ash_clouds = "ASH_CLOUDS"
+    vast_ruins = "VAST_RUINS"
+    mutated_flora = "MUTATED_FLORA"
+    terraformed = "TERRAFORMED"
+    extreme_temperatures = "EXTREME_TEMPERATURES"
+    extreme_pressure = "EXTREME_PRESSURE"
+    diverse_life = "DIVERSE_LIFE"
+    scarce_life = "SCARCE_LIFE"
+    fossils = "FOSSILS"
+    weak_gravity = "WEAK_GRAVITY"
+    strong_gravity = "STRONG_GRAVITY"
+    crushing_gravity = "CRUSHING_GRAVITY"
+    toxic_atmosphere = "TOXIC_ATMOSPHERE"
+    corrosive_atmosphere = "CORROSIVE_ATMOSPHERE"
+    breathable_atmosphere = "BREATHABLE_ATMOSPHERE"
+    jovian = "JOVIAN"
+    rocky = "ROCKY"
+    volcanic = "VOLCANIC"
+    frozen = "FROZEN"
+    swamp = "SWAMP"
+    barren = "BARREN"
+    temperate = "TEMPERATE"
+    jungle = "JUNGLE"
+    ocean = "OCEAN"
+    stripped = "STRIPPED"
+
+
+class WaypointTrait(BaseModel):
+    symbol: WaypointTraitEnum = Field(
+        ..., description="The unique identifier of the trait."
+    )
+    name: str = Field(..., description="The name of the trait.")
+    description: str = Field(..., description="A description of the trait.")
+
+
+class Chart(BaseModel):
+    waypoint_symbol: Optional[str] = Field(None, alias="waypointSymbol")
+    submitted_by: Optional[str] = Field(None, alias="submittedBy")
+    submitted_on: Optional[datetime] = Field(None, alias="submittedOn")
+
+
+class TradeSymbol(str, Enum):
+    precious_stones = "PRECIOUS_STONES"
+    quartz_sand = "QUARTZ_SAND"
+    silicon_crystals = "SILICON_CRYSTALS"
+    ammonia_ice = "AMMONIA_ICE"
+    liquid_hydrogen = "LIQUID_HYDROGEN"
+    liquid_nitrogen = "LIQUID_NITROGEN"
+    ice_water = "ICE_WATER"
+    exotic_matter = "EXOTIC_MATTER"
+    advanced_circuitry = "ADVANCED_CIRCUITRY"
+    graviton_emitters = "GRAVITON_EMITTERS"
+    iron = "IRON"
+    iron_ore = "IRON_ORE"
+    copper = "COPPER"
+    copper_ore = "COPPER_ORE"
+    aluminum = "ALUMINUM"
+    aluminum_ore = "ALUMINUM_ORE"
+    silver = "SILVER"
+    silver_ore = "SILVER_ORE"
+    gold = "GOLD"
+    gold_ore = "GOLD_ORE"
+    platinum = "PLATINUM"
+    platinum_ore = "PLATINUM_ORE"
+    diamonds = "DIAMONDS"
+    uranite = "URANITE"
+    uranite_ore = "URANITE_ORE"
+    meritium = "MERITIUM"
+    meritium_ore = "MERITIUM_ORE"
+    hydrocarbon = "HYDROCARBON"
+    antimatter = "ANTIMATTER"
+    fertilizers = "FERTILIZERS"
+    fabrics = "FABRICS"
+    food = "FOOD"
+    jewelry = "JEWELRY"
+    machinery = "MACHINERY"
+    firearms = "FIREARMS"
+    assault_rifles = "ASSAULT_RIFLES"
+    military_equipment = "MILITARY_EQUIPMENT"
+    explosives = "EXPLOSIVES"
+    lab_instruments = "LAB_INSTRUMENTS"
+    ammunition = "AMMUNITION"
+    electronics = "ELECTRONICS"
+    ship_plating = "SHIP_PLATING"
+    equipment = "EQUIPMENT"
+    fuel = "FUEL"
+    medicine = "MEDICINE"
+    drugs = "DRUGS"
+    clothing = "CLOTHING"
+    microprocessors = "MICROPROCESSORS"
+    plastics = "PLASTICS"
+    polynucleotides = "POLYNUCLEOTIDES"
+    biocomposites = "BIOCOMPOSITES"
+    nanobots = "NANOBOTS"
+    ai_mainframes = "AI_MAINFRAMES"
+    quantum_drives = "QUANTUM_DRIVES"
+    robotic_drones = "ROBOTIC_DRONES"
+    cyber_implants = "CYBER_IMPLANTS"
+    gene_therapeutics = "GENE_THERAPEUTICS"
+    neural_chips = "NEURAL_CHIPS"
+    mood_regulators = "MOOD_REGULATORS"
+    viral_agents = "VIRAL_AGENTS"
+    micro_fusion_generators = "MICRO_FUSION_GENERATORS"
+    supergrains = "SUPERGRAINS"
+    laser_rifles = "LASER_RIFLES"
+    holographics = "HOLOGRAPHICS"
+    ship_salvage = "SHIP_SALVAGE"
+    relic_tech = "RELIC_TECH"
+    novel_lifeforms = "NOVEL_LIFEFORMS"
+    botanical_specimens = "BOTANICAL_SPECIMENS"
+    cultural_artifacts = "CULTURAL_ARTIFACTS"
+    reactor_solar_i = "REACTOR_SOLAR_I"
+    reactor_fusion_i = "REACTOR_FUSION_I"
+    reactor_fission_i = "REACTOR_FISSION_I"
+    reactor_chemical_i = "REACTOR_CHEMICAL_I"
+    reactor_antimatter_i = "REACTOR_ANTIMATTER_I"
+    engine_impulse_drive_i = "ENGINE_IMPULSE_DRIVE_I"
+    engine_ion_drive_i = "ENGINE_ION_DRIVE_I"
+    engine_ion_drive_ii = "ENGINE_ION_DRIVE_II"
+    engine_hyper_drive_i = "ENGINE_HYPER_DRIVE_I"
+    module_mineral_processor_i = "MODULE_MINERAL_PROCESSOR_I"
+    module_cargo_hold_i = "MODULE_CARGO_HOLD_I"
+    module_crew_quarters_i = "MODULE_CREW_QUARTERS_I"
+    module_envoy_quarters_i = "MODULE_ENVOY_QUARTERS_I"
+    module_passenger_cabin_i = "MODULE_PASSENGER_CABIN_I"
+    module_micro_refinery_i = "MODULE_MICRO_REFINERY_I"
+    module_ore_refinery_i = "MODULE_ORE_REFINERY_I"
+    module_fuel_refinery_i = "MODULE_FUEL_REFINERY_I"
+    module_science_lab_i = "MODULE_SCIENCE_LAB_I"
+    module_jump_drive_i = "MODULE_JUMP_DRIVE_I"
+    module_jump_drive_ii = "MODULE_JUMP_DRIVE_II"
+    module_jump_drive_iii = "MODULE_JUMP_DRIVE_III"
+    module_warp_drive_i = "MODULE_WARP_DRIVE_I"
+    module_warp_drive_ii = "MODULE_WARP_DRIVE_II"
+    module_warp_drive_iii = "MODULE_WARP_DRIVE_III"
+    module_shield_generator_i = "MODULE_SHIELD_GENERATOR_I"
+    module_shield_generator_ii = "MODULE_SHIELD_GENERATOR_II"
+    mount_gas_siphon_i = "MOUNT_GAS_SIPHON_I"
+    mount_gas_siphon_ii = "MOUNT_GAS_SIPHON_II"
+    mount_gas_siphon_iii = "MOUNT_GAS_SIPHON_III"
+    mount_surveyor_i = "MOUNT_SURVEYOR_I"
+    mount_surveyor_ii = "MOUNT_SURVEYOR_II"
+    mount_surveyor_iii = "MOUNT_SURVEYOR_III"
+    mount_sensor_array_i = "MOUNT_SENSOR_ARRAY_I"
+    mount_sensor_array_ii = "MOUNT_SENSOR_ARRAY_II"
+    mount_sensor_array_iii = "MOUNT_SENSOR_ARRAY_III"
+    mount_mining_laser_i = "MOUNT_MINING_LASER_I"
+    mount_mining_laser_ii = "MOUNT_MINING_LASER_II"
+    mount_mining_laser_iii = "MOUNT_MINING_LASER_III"
+    mount_laser_cannon_i = "MOUNT_LASER_CANNON_I"
+    mount_missile_launcher_i = "MOUNT_MISSILE_LAUNCHER_I"
+    mount_turret_i = "MOUNT_TURRET_I"
+
+
+class Type1(str, Enum):
+    purchase = "PURCHASE"
+    sell = "SELL"
+
+
+class MarketTransaction(BaseModel):
+    waypoint_symbol: str = Field(
+        ...,
+        alias="waypointSymbol",
+        description="The symbol of the waypoint where the transaction took place.",
+    )
+    ship_symbol: str = Field(
+        ...,
+        alias="shipSymbol",
+        description="The symbol of the ship that made the transaction.",
+    )
+    trade_symbol: str = Field(
+        ..., alias="tradeSymbol", description="The symbol of the trade good."
+    )
+    type: Type1 = Field(..., description="The type of transaction.")
+    units: Annotated[
+        int,
+        conint(ge=1),
+        Field(..., description="The number of units of the transaction."),
+    ]
+    price_per_unit: Annotated[
+        int,
+        conint(ge=1),
+        Field(
+            ...,
+            alias="pricePerUnit",
+            description="The price per unit of the transaction.",
+        ),
+    ]
+    total_price: Annotated[
+        int,
+        conint(ge=1),
+        Field(
+            ..., alias="totalPrice", description="The total price of the transaction."
+        ),
+    ]
+    timestamp: datetime = Field(..., description="The timestamp of the transaction.")
+
+
+class Supply(str, Enum):
+    scarce = "SCARCE"
+    limited = "LIMITED"
+    moderate = "MODERATE"
+    abundant = "ABUNDANT"
+
+
+class MarketTradeGood(BaseModel):
+    symbol: str = Field(..., description="The symbol of the trade good.")
+    trade_volume: Annotated[
+        int,
+        conint(ge=1),
+        Field(
+            ...,
+            alias="tradeVolume",
+            description=(
+                "The typical volume flowing through the market for this type of good. The"
+                " larger the trade volume, the more stable prices will be."
+            ),
+        ),
+    ]
+    supply: Supply = Field(
+        ...,
+        description=(
+            "A rough estimate of the total supply of this good in the marketplace."
+        ),
+    )
+    purchase_price: NonNegativeInt = Field(
+        ...,
+        alias="purchasePrice",
+        description="The price at which this good can be purchased from the market.",
+    )
+    sell_price: NonNegativeInt = Field(
+        ...,
+        alias="sellPrice",
+        description="The price at which this good can be sold to the market.",
+    )
+
+
+class ShipType(str, Enum):
+    ship_probe = "SHIP_PROBE"
+    ship_mining_drone = "SHIP_MINING_DRONE"
+    ship_interceptor = "SHIP_INTERCEPTOR"
+    ship_light_hauler = "SHIP_LIGHT_HAULER"
+    ship_command_frigate = "SHIP_COMMAND_FRIGATE"
+    ship_explorer = "SHIP_EXPLORER"
+    ship_heavy_freighter = "SHIP_HEAVY_FREIGHTER"
+    ship_light_shuttle = "SHIP_LIGHT_SHUTTLE"
+    ship_ore_hound = "SHIP_ORE_HOUND"
+    ship_refining_freighter = "SHIP_REFINING_FREIGHTER"
+
+
+class ShipyardTransaction(BaseModel):
+    waypoint_symbol: str = Field(
+        ...,
+        alias="waypointSymbol",
+        description="The symbol of the waypoint where the transaction took place.",
+    )
+    ship_symbol: str = Field(
+        ...,
+        alias="shipSymbol",
+        description="The symbol of the ship that was purchased.",
+    )
+    price: Annotated[
+        int, conint(ge=1), Field(..., description="The price of the transaction.")
+    ]
+    agent_symbol: str = Field(
+        ...,
+        alias="agentSymbol",
+        description="The symbol of the agent that made the transaction.",
+    )
+    timestamp: datetime = Field(..., description="The timestamp of the transaction.")
+
+
+class ConnectedSystem(BaseModel):
+    symbol: NonEmptyStr
+    sector_symbol: NonEmptyStr = Field(..., alias="sectorSymbol")
+    type: SystemType
+    faction_symbol: Optional[str] = Field(
+        None,
+        alias="factionSymbol",
+        description=(
+            "The symbol of the faction that owns the connected jump gate in the system."
+        ),
+    )
+    x: int
+    y: int
+    distance: int
+
+
+class Produce(str, Enum):
+    iron = "IRON"
+    copper = "COPPER"
+    silver = "SILVER"
+    gold = "GOLD"
+    aluminum = "ALUMINUM"
+    platinum = "PLATINUM"
+    uranite = "URANITE"
+    meritium = "MERITIUM"
+    fuel = "FUEL"
+
+
+class ProducedItem(BaseModel):
+    trade_symbol: Optional[str] = Field(None, alias="tradeSymbol")
+    units: Optional[int] = None
+
+
+class ConsumedItem(BaseModel):
+    trade_symbol: Optional[str] = Field(None, alias="tradeSymbol")
+    units: Optional[int] = None
+
+
+class Cooldown(BaseModel):
+    ship_symbol: NonEmptyStr = Field(
+        ...,
+        alias="shipSymbol",
+        description="The symbol of the ship that is on cooldown",
+    )
+    total_seconds: NonNegativeInt = Field(
+        ...,
+        alias="totalSeconds",
+        description="The total duration of the cooldown in seconds",
+    )
+    remaining_seconds: NonNegativeInt = Field(
+        ...,
+        alias="remainingSeconds",
+        description="The remaining duration of the cooldown in seconds",
+    )
+    expiration: datetime = Field(
+        ...,
+        description="The date and time when the cooldown expires in ISO 8601 format",
+    )
+
+
+class Size(str, Enum):
+    small = "SMALL"
+    moderate = "MODERATE"
+    large = "LARGE"
+
+
+class SurveyDeposit(BaseModel):
+    symbol: str = Field(..., description="The symbol of the deposit.")
+
+
+class ExtractionYield(BaseModel):
+    symbol: NonEmptyStr
+    units: int = Field(
+        ...,
+        description=(
+            "The number of units extracted that were placed into the ship's cargo hold."
+        ),
+    )
+
+
+class ScannedSystem(BaseModel):
+    symbol: NonEmptyStr
+    sector_symbol: NonEmptyStr = Field(..., alias="sectorSymbol")
+    type: SystemType
+    x: int
+    y: int
+    distance: int
+
+
+class Frame(BaseModel):
+    symbol: str
+
+
+class Reactor(BaseModel):
+    symbol: str
+
+
+class Engine(BaseModel):
+    symbol: str
+
+
+class Mount(BaseModel):
+    symbol: str
+
+
+class ContractTerms(BaseModel):
+    deadline: datetime = Field(..., description="The deadline for the contract.")
+    payment: ContractPayment
+    deliver: Optional[List[ContractDeliverGood]] = None
+
+
+class Faction(BaseModel):
+    symbol: NonEmptyStr
+    name: NonEmptyStr
+    description: NonEmptyStr
+    headquarters: NonEmptyStr
+    traits: List[FactionTrait]
+
+
+class ShipRegistration(BaseModel):
+    name: NonEmptyStr = Field(
+        ..., description="The agent's registered name of the ship"
+    )
+    faction_symbol: Optional[NonEmptyStr] = Field(
+        None,
+        alias="factionSymbol",
+        description="The symbol of the faction the ship is registered with",
+    )
+    role: ShipRole
+
+
+class ShipNavRouteWaypoint(BaseModel):
+    symbol: NonEmptyStr
+    type: WaypointType
+    system_symbol: NonEmptyStr = Field(..., alias="systemSymbol")
+    x: int
+    y: int
+
+
+class ShipFrame(BaseModel):
+    symbol: FramesEnum
+    name: str
+    description: str
+    condition: Optional[ShipCondition] = None
+    module_slots: NonNegativeInt = Field(..., alias="moduleSlots")
+    mounting_points: NonNegativeInt = Field(..., alias="mountingPoints")
+    fuel_capacity: NonNegativeInt = Field(..., alias="fuelCapacity")
+    requirements: ShipRequirements
+
+
+class ShipCargo(BaseModel):
+    capacity: NonNegativeInt = Field(
+        ..., description="The max number of items that can be stored in the cargo hold."
+    )
+    units: NonNegativeInt = Field(
+        ..., description="The number of items currently stored in the cargo hold."
+    )
+    inventory: List[ShipCargoItem] = Field(
+        ..., description="The items currently in the cargo hold."
+    )
+
+
+class System(BaseModel):
+    symbol: NonEmptyStr
+    sector_symbol: NonEmptyStr = Field(..., alias="sectorSymbol")
+    type: SystemType
+    x: int
+    y: int
+    waypoints: List[SystemWaypoint]
+    factions: List[SystemFaction]
+
+
+class Waypoint(BaseModel):
+    symbol: NonEmptyStr
+    type: WaypointType
+    system_symbol: NonEmptyStr = Field(..., alias="systemSymbol")
+    x: int
+    y: int
+    orbitals: List[WaypointOrbital]
+    faction: Optional[WaypointFaction] = None
+    traits: List[WaypointTrait] = Field(..., description="The traits of the waypoint.")
+    chart: Optional[Chart] = None
+
+
+class TradeGood(BaseModel):
+    symbol: TradeSymbol
+    name: str
+    description: str
+
+
+class ShipTypeModel(BaseModel):
+    type: Optional[ShipType] = None
+
+
+class ShipyardShip(BaseModel):
+    type: Optional[ShipType] = None
+    name: str
+    description: str
+    purchase_price: int = Field(..., alias="purchasePrice")
+    frame: ShipFrame
+    reactor: ShipReactor
+    engine: ShipEngine
+    modules: List[ShipModule]
+    mounts: List[ShipMount]
+
+
+class JumpGate(BaseModel):
+    jump_range: float = Field(
+        ..., alias="jumpRange", description="The maximum jump range of the gate."
+    )
+    faction_symbol: Optional[str] = Field(
+        None,
+        alias="factionSymbol",
+        description="The symbol of the faction that owns the gate.",
+    )
+    connected_systems: List[ConnectedSystem] = Field(
+        ...,
+        alias="connectedSystems",
+        description=(
+            "The systems within range of the gate that have a corresponding gate."
+        ),
+    )
+
+
+class ShipRefineResult(BaseModel):
+    cargo: ShipCargo
+    cooldown: Cooldown
+    produced: List[ProducedItem]
+    consumed: List[ConsumedItem]
+
+
+class ChartShipResult(BaseModel):
+    chart: Chart
+    waypoint: Waypoint
+
+
+class Survey(BaseModel):
+    signature: NonEmptyStr = Field(
+        ...,
+        description=(
+            "A unique signature for the location of this survey. This signature is"
+            " verified when attempting an extraction using this survey."
+        ),
+    )
+    symbol: NonEmptyStr = Field(
+        ..., description="The symbol of the waypoint that this survey is for."
+    )
+    deposits: List[SurveyDeposit] = Field(
+        ..., description="A list of deposits that can be found at this location."
+    )
+    expiration: datetime = Field(
+        ...,
+        description=(
+            "The date and time when the survey expires. After this date and time, the"
+            " survey will no longer be available for extraction."
+        ),
+    )
+    size: Size = Field(
+        ...,
+        description=(
+            "The size of the deposit. This value indicates how much can be extracted"
+            " from the survey before it is exhausted."
+        ),
+    )
+
+
+class Extraction(BaseModel):
+    ship_symbol: NonEmptyStr = Field(..., alias="shipSymbol")
+    yield_: ExtractionYield = Field(..., alias="yield")
+
+
+class SellCargoResult(BaseModel):
+    agent: AgentSchema
+    cargo: ShipCargo
+    transaction: MarketTransaction
+
+
+class RefuelShipResult(BaseModel):
+    agent: AgentSchema
+    fuel: ShipFuel
+
+
+class ScanSystemsResult(BaseModel):
+    cooldown: Cooldown
+    systems: List[ScannedSystem]
+
+
+class ScanWaypointsResult(BaseModel):
+    cooldown: Cooldown
+    waypoints: List[Waypoint]
+
+
+class PurchaseCargoResult(BaseModel):
+    agent: AgentSchema
+    cargo: ShipCargo
+    transaction: MarketTransaction
+
+
+class ContractSchema(BaseModel):
+    id: NonEmptyStr
+    faction_symbol: NonEmptyStr = Field(
+        ...,
+        alias="factionSymbol",
+        description="The symbol of the faction that this contract is for.",
+    )
+    type: ContractType
+    terms: ContractTerms
+    accepted: bool = Field(
+        ..., description="Whether the contract has been accepted by the agent"
+    )
+    fulfilled: bool = Field(..., description="Whether the contract has been fulfilled")
+    expiration: datetime = Field(
+        ..., description="The time at which the contract expires"
+    )
+
+
+class ShipNavRoute(BaseModel):
+    destination: ShipNavRouteWaypoint
+    departure: ShipNavRouteWaypoint
+    departure_time: datetime = Field(
+        ..., alias="departureTime", description="The date time of the ship's departure."
+    )
+    arrival: datetime = Field(
+        ...,
+        description=(
+            "The date time of the ship's arrival. If the ship is in-transit, this is"
+            " the expected time of arrival."
+        ),
+    )
+
+
+class Market(BaseModel):
+    symbol: str = Field(
+        ...,
+        description=(
+            "The symbol of the market. The symbol is the same as the waypoint where the"
+            " market is located."
+        ),
+    )
+    exports: List[TradeGood] = Field(
+        ..., description="The list of goods that are exported from this market."
+    )
+    imports: List[TradeGood] = Field(
+        ..., description="The list of goods that are sought as imports in this market."
+    )
+    exchange: List[TradeGood] = Field(
+        ...,
+        description=(
+            "The list of goods that are bought and sold between agents at this market."
+        ),
+    )
+    transactions: Optional[List[MarketTransaction]] = Field(
+        None,
+        description=(
+            "The list of recent transactions at this market. Visible only when a ship"
+            " is present at the market."
+        ),
+    )
+    trade_goods: Optional[List[MarketTradeGood]] = Field(
+        None,
+        alias="tradeGoods",
+        description=(
+            "The list of goods that are traded at this market. Visible only when a ship"
+            " is present at the market."
+        ),
+    )
+
+
+class Shipyard(BaseModel):
+    symbol: NonEmptyStr = Field(
+        ...,
+        description=(
+            "The symbol of the shipyard. The symbol is the same as the waypoint where"
+            " the shipyard is located."
+        ),
+    )
+    ship_types: List[ShipTypeModel] = Field(
+        ...,
+        alias="shipTypes",
+        description="The list of ship types available for purchase at this shipyard.",
+    )
+    transactions: Optional[List[ShipyardTransaction]] = Field(
+        None, description="The list of recent transactions at this shipyard."
+    )
+    ships: Optional[List[ShipyardShip]] = Field(
+        None,
+        description=(
+            "The ships that are currently available for purchase at the shipyard."
+        ),
+    )
+
+
+class AcceptContractResult(BaseModel):
+    agent: AgentSchema
+    contract: ContractSchema
+
+
+class DeliverContractResult(BaseModel):
+    contract: ContractSchema
+    cargo: ShipCargo
+
+
+class FullfillContractResult(AcceptContractResult):
+    pass
+
+
+class CreateSurveyResult(BaseModel):
+    cooldown: Cooldown
+    surveys: List[Survey]
+
+
+class ExtractResourcesResult(BaseModel):
+    cooldown: Cooldown
+    extraction: Extraction
+    cargo: ShipCargo
+
+
+class ShipNav(BaseModel):
+    system_symbol: str = Field(
+        ...,
+        alias="systemSymbol",
+        description="The system symbol of the ship's current location.",
+    )
+    waypoint_symbol: str = Field(
+        ...,
+        alias="waypointSymbol",
+        description=(
+            "The waypoint symbol of the ship's current location, or if the ship is"
+            " in-transit, the waypoint symbol of the ship's destination."
+        ),
+    )
+    route: ShipNavRoute
+    status: ShipNavStatus
+    flight_mode: ShipNavFlightMode = Field(..., alias="flightMode")
+
+
+class ShipJumpResult(BaseModel):
+    cooldown: Cooldown
+    nav: Optional[ShipNav] = None
+
+
+class ShipNavigateResult(BaseModel):
+    fuel: ShipFuel
+    nav: ShipNav
+
+
+class ScannedShip(BaseModel):
+    symbol: str = Field(..., description="The globally unique identifier of the ship.")
+    registration: ShipRegistration
+    nav: ShipNav
+    frame: Optional[Frame] = Field(None, description="The frame of the ship.")
+    reactor: Optional[Reactor] = Field(None, description="The reactor of the ship.")
+    engine: Engine = Field(..., description="The engine of the ship.")
+    mounts: Optional[List[Mount]] = None
+
+
+class ShipSchema(BaseModel):
+    symbol: str = Field(
+        ...,
+        description=(
+            "The globally unique identifier of the ship in the following format:"
+            " `[AGENT_SYMBOL]_[HEX_ID]`"
+        ),
+    )
+    registration: ShipRegistration
+    nav: ShipNav
+    crew: ShipCrew
+    frame: ShipFrame
+    reactor: ShipReactor
+    engine: ShipEngine
+    modules: List[ShipModule]
+    mounts: List[ShipMount]
+    cargo: ShipCargo
+    fuel: ShipFuel
+
+
+class PurchaseShipResult(BaseModel):
+    agent: AgentSchema
+    ship: ShipSchema
+    transaction: ShipyardTransaction
+
+
+class ScanShipsResult(BaseModel):
+    cooldown: Cooldown
+    ships: List[ScannedShip]
+
+
+class RegisterData(BaseModel):
+    agent: AgentSchema
+    contract: ContractSchema
+    faction: Faction
+    ship: ShipSchema
+    token: str = Field(
+        ..., description="A Bearer token for accessing secured API endpoints."
+    )
+
+
+class RegisterResponse(BaseModel):
+    data: RegisterData
```

### Comparing `astrotraders-1.0.0/astrotraders/api/wrapper.py` & `astrotraders-1.0.1/astrotraders/api/wrapper.py`

 * *Ordering differences only*

 * *Files 16% similar despite different names*

```diff
@@ -1,94 +1,94 @@
-from typing import TypeVar, Optional, Union, TYPE_CHECKING, Type, Any, Mapping, cast
-
-from pydantic import BaseModel
-from typing_extensions import Unpack
-
-import orjson
-
-from astrotraders.api.schemas import PaginatedObject
-from astrotraders.api.utils import ORJSONDecoder
-
-if TYPE_CHECKING:
-    from typing import TypedDict
-    from httpx import Client
-    from httpx._client import UseClientDefault
-    from httpx._types import (
-        RequestContent,
-        RequestData,
-        RequestFiles,
-        QueryParamTypes,
-        HeaderTypes,
-        CookieTypes,
-        AuthTypes,
-        TimeoutTypes,
-        RequestExtensions,
-    )
-
-    class HttpxRequestParams(TypedDict, total=False):
-        content: Optional[RequestContent]
-        data: Optional[RequestData]
-        files: Optional[RequestFiles]
-        json: Optional[Any]
-        params: Optional[QueryParamTypes]
-        headers: Optional[HeaderTypes]
-        cookies: Optional[CookieTypes]
-        auth: Union[AuthTypes, UseClientDefault, None]
-        follow_redirects: Union[bool, UseClientDefault]
-        timeout: Union[TimeoutTypes, UseClientDefault]
-        extensions: Optional[RequestExtensions]
-
-
-T = TypeVar("T", bound=BaseModel)
-
-
-class HttpxClientWrapper:
-    def __init__(self, client: "Client"):
-        self._client = client
-
-    def raw_request(
-        self, method: str, uri: str, **params: Unpack["HttpxRequestParams"]
-    ) -> Optional[dict[Any, Any]]:
-        # because httpx doesn't have default way to change json encoder
-        if json_obj := params.get("json"):
-            # it works as well with bytes
-            params["data"] = orjson.dumps(json_obj)  # type: ignore[typeddict-item]
-            params["headers"] = {"Content-Type": "application/json"}
-            del params["json"]
-        result = self._client.request(method, uri, **params)
-        # in a few requests we get 204, so we should handle this
-        if result.status_code == 204:
-            return None
-        return result.json(cls=ORJSONDecoder)
-
-    def request_to_model(
-        self,
-        method: str,
-        uri: str,
-        to_type: Type[T],
-        **params: Unpack["HttpxRequestParams"],
-    ) -> T:
-        data = cast(Mapping[str, Any], self.raw_request(method, uri, **params))
-        return to_type(**data["data"])
-
-    def request_to_model_optioned(
-        self,
-        method: str,
-        uri: str,
-        to_type: Type[T],
-        **params: Unpack["HttpxRequestParams"],
-    ) -> Optional[T]:
-        data = cast(Mapping[str, Any], self.raw_request(method, uri, **params))
-        if data:
-            return to_type(**data["data"])
-        return None
-
-    def request_to_paginated(
-        self,
-        method: str,
-        uri: str,
-        to_type: Type[T],
-        **params: Unpack["HttpxRequestParams"],
-    ) -> PaginatedObject[T]:
-        data = cast(Mapping[str, Any], self.raw_request(method, uri, **params))
-        # TODO: fix mypy error
-        return PaginatedObject[to_type](**data)  # type: ignore[valid-type]
+from typing import TypeVar, Optional, Union, TYPE_CHECKING, Type, Any, Mapping, cast
+
+from pydantic import BaseModel
+from typing_extensions import Unpack
+
+import orjson
+
+from astrotraders.api.schemas import PaginatedObject
+from astrotraders.api.utils import ORJSONDecoder
+
+if TYPE_CHECKING:
+    from typing import TypedDict
+    from httpx import Client
+    from httpx._client import UseClientDefault
+    from httpx._types import (
+        RequestContent,
+        RequestData,
+        RequestFiles,
+        QueryParamTypes,
+        HeaderTypes,
+        CookieTypes,
+        AuthTypes,
+        TimeoutTypes,
+        RequestExtensions,
+    )
+
+    class HttpxRequestParams(TypedDict, total=False):
+        content: Optional[RequestContent]
+        data: Optional[RequestData]
+        files: Optional[RequestFiles]
+        json: Optional[Any]
+        params: Optional[QueryParamTypes]
+        headers: Optional[HeaderTypes]
+        cookies: Optional[CookieTypes]
+        auth: Union[AuthTypes, UseClientDefault, None]
+        follow_redirects: Union[bool, UseClientDefault]
+        timeout: Union[TimeoutTypes, UseClientDefault]
+        extensions: Optional[RequestExtensions]
+
+
+T = TypeVar("T", bound=BaseModel)
+
+
+class HttpxClientWrapper:
+    def __init__(self, client: "Client"):
+        self._client = client
+
+    def raw_request(
+        self, method: str, uri: str, **params: Unpack["HttpxRequestParams"]
+    ) -> Optional[dict[Any, Any]]:
+        # because httpx doesn't have default way to change json encoder
+        if json_obj := params.get("json"):
+            # it works as well with bytes
+            params["data"] = orjson.dumps(json_obj)  # type: ignore[typeddict-item]
+            params["headers"] = {"Content-Type": "application/json"}
+            del params["json"]
+        result = self._client.request(method, uri, **params)
+        # in a few requests we get 204, so we should handle this
+        if result.status_code == 204:
+            return None
+        return result.json(cls=ORJSONDecoder)
+
+    def request_to_model(
+        self,
+        method: str,
+        uri: str,
+        to_type: Type[T],
+        **params: Unpack["HttpxRequestParams"],
+    ) -> T:
+        data = cast(Mapping[str, Any], self.raw_request(method, uri, **params))
+        return to_type(**data["data"])
+
+    def request_to_model_optioned(
+        self,
+        method: str,
+        uri: str,
+        to_type: Type[T],
+        **params: Unpack["HttpxRequestParams"],
+    ) -> Optional[T]:
+        data = cast(Mapping[str, Any], self.raw_request(method, uri, **params))
+        if data:
+            return to_type(**data["data"])
+        return None
+
+    def request_to_paginated(
+        self,
+        method: str,
+        uri: str,
+        to_type: Type[T],
+        **params: Unpack["HttpxRequestParams"],
+    ) -> PaginatedObject[T]:
+        data = cast(Mapping[str, Any], self.raw_request(method, uri, **params))
+        # TODO: fix mypy error
+        return PaginatedObject[to_type](**data)  # type: ignore[valid-type]
```

### Comparing `astrotraders-1.0.0/PKG-INFO` & `astrotraders-1.0.1/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,20 +1,27 @@
 Metadata-Version: 2.1
 Name: astrotraders
-Version: 1.0.0
+Version: 1.0.1
 Summary: A typed, handwrited and powerful spacetraders API wrapper
+Home-page: https://github.com/kiriharu/astrotraders
+Keywords: spacetraders,spacetraders.io
 Author: kiriharu
 Author-email: me@kiriha.ru
 Requires-Python: >=3.10,<4.0
+Classifier: Intended Audience :: Developers
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
+Classifier: Programming Language :: Python :: 3
+Classifier: Topic :: Utilities
+Classifier: Typing :: Typed
 Requires-Dist: httpx (>=0.24.0,<0.25.0)
 Requires-Dist: orjson (>=3.8.12,<4.0.0)
 Requires-Dist: pydantic (>=1.10.7,<2.0.0)
+Project-URL: Repository, https://github.com/kiriharu/astrotraders
 Description-Content-Type: text/markdown
 
 # astrotraders
 
 A typed, handwrited and powerful library for spacetraders.io game.
 
 SpaceTraders is an API-based game where you acquire and manage a fleet of ships to explore, trade, and fight your way across the galaxy.
```

