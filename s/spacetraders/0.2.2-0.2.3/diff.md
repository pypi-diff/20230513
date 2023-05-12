# Comparing `tmp/spacetraders-0.2.2.tar.gz` & `tmp/spacetraders-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spacetraders-0.2.2.tar", max compression
+gzip compressed data, was "spacetraders-0.2.3.tar", max compression
```

## Comparing `spacetraders-0.2.2.tar` & `spacetraders-0.2.3.tar`

### file list

```diff
@@ -1,208 +1,208 @@
--rw-r--r--   0        0        0     3472 2023-05-10 04:00:00.539673 spacetraders-0.2.2/README.md
--rw-r--r--   0        0        0      522 2023-05-11 19:07:36.186983 spacetraders-0.2.2/pyproject.toml
--rw-r--r--   0        0        0      250 2023-05-11 19:02:43.376983 spacetraders-0.2.2/spacetraders/__init__.py
--rw-r--r--   0        0        0       47 2023-05-11 19:02:42.886983 spacetraders-0.2.2/spacetraders/api/__init__.py
--rw-r--r--   0        0        0        0 2023-05-11 19:02:42.936983 spacetraders-0.2.2/spacetraders/api/agents/__init__.py
--rw-r--r--   0        0        0     3818 2023-05-11 19:02:43.436983 spacetraders-0.2.2/spacetraders/api/agents/get_my_agent.py
--rw-r--r--   0        0        0        0 2023-05-11 19:02:42.936983 spacetraders-0.2.2/spacetraders/api/contracts/__init__.py
--rw-r--r--   0        0        0     4290 2023-05-11 19:02:43.446983 spacetraders-0.2.2/spacetraders/api/contracts/accept_contract.py
--rw-r--r--   0        0        0     5161 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/contracts/deliver_contract.py
--rw-r--r--   0        0        0     4308 2023-05-11 19:02:43.446983 spacetraders-0.2.2/spacetraders/api/contracts/fulfill_contract.py
--rw-r--r--   0        0        0     4303 2023-05-11 19:02:43.476983 spacetraders-0.2.2/spacetraders/api/contracts/get_contract.py
--rw-r--r--   0        0        0     5015 2023-05-11 19:02:43.566983 spacetraders-0.2.2/spacetraders/api/contracts/get_contracts.py
--rw-r--r--   0        0        0        0 2023-05-11 19:02:42.896983 spacetraders-0.2.2/spacetraders/api/default/__init__.py
--rw-r--r--   0        0        0     9240 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/default/register.py
--rw-r--r--   0        0        0        0 2023-05-11 19:02:42.936983 spacetraders-0.2.2/spacetraders/api/factions/__init__.py
--rw-r--r--   0        0        0     4361 2023-05-11 19:02:43.446983 spacetraders-0.2.2/spacetraders/api/factions/get_faction.py
--rw-r--r--   0        0        0     4985 2023-05-11 19:02:43.466983 spacetraders-0.2.2/spacetraders/api/factions/get_factions.py
--rw-r--r--   0        0        0        0 2023-05-11 19:02:42.946983 spacetraders-0.2.2/spacetraders/api/fleet/__init__.py
--rw-r--r--   0        0        0     5255 2023-05-11 19:02:43.466983 spacetraders-0.2.2/spacetraders/api/fleet/create_chart.py
--rw-r--r--   0        0        0     4513 2023-05-11 19:02:43.466983 spacetraders-0.2.2/spacetraders/api/fleet/create_ship_ship_scan.py
--rw-r--r--   0        0        0     4566 2023-05-11 19:02:43.466983 spacetraders-0.2.2/spacetraders/api/fleet/create_ship_system_scan.py
--rw-r--r--   0        0        0     4610 2023-05-11 19:02:43.446983 spacetraders-0.2.2/spacetraders/api/fleet/create_ship_waypoint_scan.py
--rw-r--r--   0        0        0     6213 2023-05-11 19:02:43.446983 spacetraders-0.2.2/spacetraders/api/fleet/create_survey.py
--rw-r--r--   0        0        0     5356 2023-05-11 19:02:43.496983 spacetraders-0.2.2/spacetraders/api/fleet/dock_ship.py
--rw-r--r--   0        0        0     5540 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/extract_resources.py
--rw-r--r--   0        0        0     4236 2023-05-11 19:02:43.516983 spacetraders-0.2.2/spacetraders/api/fleet/get_my_ship.py
--rw-r--r--   0        0        0     4338 2023-05-11 19:02:43.526983 spacetraders-0.2.2/spacetraders/api/fleet/get_my_ship_cargo.py
--rw-r--r--   0        0        0     4970 2023-05-11 19:02:43.546983 spacetraders-0.2.2/spacetraders/api/fleet/get_my_ships.py
--rw-r--r--   0        0        0     6390 2023-05-11 19:02:43.536983 spacetraders-0.2.2/spacetraders/api/fleet/get_ship_cooldown.py
--rw-r--r--   0        0        0     4295 2023-05-11 19:02:43.526983 spacetraders-0.2.2/spacetraders/api/fleet/get_ship_nav.py
--rw-r--r--   0        0        0     5002 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/jettison.py
--rw-r--r--   0        0        0     5292 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/jump_ship.py
--rw-r--r--   0        0        0     6936 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/navigate_ship.py
--rw-r--r--   0        0        0     5331 2023-05-11 19:02:43.546983 spacetraders-0.2.2/spacetraders/api/fleet/orbit_ship.py
--rw-r--r--   0        0        0     5154 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/patch_ship_nav.py
--rw-r--r--   0        0        0     5373 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/purchase_cargo.py
--rw-r--r--   0        0        0     4583 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/purchase_ship.py
--rw-r--r--   0        0        0     4302 2023-05-11 19:02:43.566983 spacetraders-0.2.2/spacetraders/api/fleet/refuel_ship.py
--rw-r--r--   0        0        0     5111 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/sell_cargo.py
--rw-r--r--   0        0        0     5599 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/ship_refine.py
--rw-r--r--   0        0        0     5424 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/transfer_cargo.py
--rw-r--r--   0        0        0     6332 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/api/fleet/warp_ship.py
--rw-r--r--   0        0        0        0 2023-05-11 19:02:42.936983 spacetraders-0.2.2/spacetraders/api/systems/__init__.py
--rw-r--r--   0        0        0     4838 2023-05-11 19:02:43.676982 spacetraders-0.2.2/spacetraders/api/systems/get_jump_gate.py
--rw-r--r--   0        0        0     5624 2023-05-11 19:02:43.636983 spacetraders-0.2.2/spacetraders/api/systems/get_market.py
--rw-r--r--   0        0        0     4812 2023-05-11 19:02:43.616983 spacetraders-0.2.2/spacetraders/api/systems/get_shipyard.py
--rw-r--r--   0        0        0     4398 2023-05-11 19:02:43.606983 spacetraders-0.2.2/spacetraders/api/systems/get_system.py
--rw-r--r--   0        0        0     5944 2023-05-11 19:02:43.666983 spacetraders-0.2.2/spacetraders/api/systems/get_system_waypoints.py
--rw-r--r--   0        0        0     4984 2023-05-11 19:02:43.686983 spacetraders-0.2.2/spacetraders/api/systems/get_systems.py
--rw-r--r--   0        0        0     4799 2023-05-11 19:02:43.696983 spacetraders-0.2.2/spacetraders/api/systems/get_waypoint.py
--rw-r--r--   0        0        0     4213 2023-05-11 19:02:43.716983 spacetraders-0.2.2/spacetraders/client.py
--rw-r--r--   0        0        0      470 2023-05-11 19:02:43.576983 spacetraders-0.2.2/spacetraders/errors.py
--rw-r--r--   0        0        0    13081 2023-05-11 19:02:43.746983 spacetraders-0.2.2/spacetraders/models/__init__.py
--rw-r--r--   0        0        0     1216 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/accept_contract_response_200.py
--rw-r--r--   0        0        0     1246 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/accept_contract_response_200_data.py
--rw-r--r--   0        0        0     1397 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/agent.py
--rw-r--r--   0        0        0     1422 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/chart.py
--rw-r--r--   0        0        0     1609 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/connected_system.py
--rw-r--r--   0        0        0     1820 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/contract.py
--rw-r--r--   0        0        0     1649 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/contract_deliver_good.py
--rw-r--r--   0        0        0     1277 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/contract_payment.py
--rw-r--r--   0        0        0     1520 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/contract_terms.py
--rw-r--r--   0        0        0      201 2023-05-11 19:02:43.056983 spacetraders-0.2.2/spacetraders/models/contract_type.py
--rw-r--r--   0        0        0     1675 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/cooldown.py
--rw-r--r--   0        0        0     1198 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_chart_response_201.py
--rw-r--r--   0        0        0     1416 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_chart_response_201_data.py
--rw-r--r--   0        0        0     1251 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_ship_ship_scan_response_201.py
--rw-r--r--   0        0        0     1372 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_ship_ship_scan_response_201_data.py
--rw-r--r--   0        0        0     1263 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_ship_system_scan_response_201.py
--rw-r--r--   0        0        0     1390 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_ship_system_scan_response_201_data.py
--rw-r--r--   0        0        0     1275 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_ship_waypoint_scan_response_201.py
--rw-r--r--   0        0        0     1408 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_ship_waypoint_scan_response_201_data.py
--rw-r--r--   0        0        0     1204 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_survey_response_201.py
--rw-r--r--   0        0        0     1345 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/create_survey_response_201_data.py
--rw-r--r--   0        0        0     1221 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/deliver_contract_json_body.py
--rw-r--r--   0        0        0     1222 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/deliver_contract_response_200.py
--rw-r--r--   0        0        0     1265 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/deliver_contract_response_200_data.py
--rw-r--r--   0        0        0     1239 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/dock_ship_dock_ship_200_response.py
--rw-r--r--   0        0        0     1174 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/dock_ship_dock_ship_200_response_data.py
--rw-r--r--   0        0        0     1285 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/extract_resources_json_body.py
--rw-r--r--   0        0        0     1228 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/extract_resources_response_201.py
--rw-r--r--   0        0        0     1479 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/extract_resources_response_201_data.py
--rw-r--r--   0        0        0     1208 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/extraction.py
--rw-r--r--   0        0        0     1187 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/extraction_yield.py
--rw-r--r--   0        0        0     1404 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/faction.py
--rw-r--r--   0        0        0     1358 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/faction_trait.py
--rw-r--r--   0        0        0     2091 2023-05-11 19:02:43.146983 spacetraders-0.2.2/spacetraders/models/faction_trait_symbol.py
--rw-r--r--   0        0        0     1222 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/fulfill_contract_response_200.py
--rw-r--r--   0        0        0     1248 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/fulfill_contract_response_200_data.py
--rw-r--r--   0        0        0     1122 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_contract_response_200.py
--rw-r--r--   0        0        0     1229 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_contracts_response_200.py
--rw-r--r--   0        0        0     1116 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_faction_response_200.py
--rw-r--r--   0        0        0     1223 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_factions_response_200.py
--rw-r--r--   0        0        0     1123 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_jump_gate_response_200.py
--rw-r--r--   0        0        0     1110 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_market_response_200.py
--rw-r--r--   0        0        0     1108 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_my_agent_response_200.py
--rw-r--r--   0        0        0     1133 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_my_ship_cargo_response_200.py
--rw-r--r--   0        0        0     1109 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_my_ship_response_200.py
--rw-r--r--   0        0        0     1209 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_my_ships_response_200.py
--rw-r--r--   0        0        0     1209 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_ship_cooldown_response_200.py
--rw-r--r--   0        0        0     1157 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_ship_nav_response_200.py
--rw-r--r--   0        0        0     1122 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_shipyard_response_200.py
--rw-r--r--   0        0        0     1110 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_system_response_200.py
--rw-r--r--   0        0        0     1241 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_system_waypoints_response_200.py
--rw-r--r--   0        0        0     1217 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_systems_response_200.py
--rw-r--r--   0        0        0     1213 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/get_waypoint_response_200.py
--rw-r--r--   0        0        0     1114 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/jettison_json_body.py
--rw-r--r--   0        0        0     1179 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/jettison_response_200.py
--rw-r--r--   0        0        0     1132 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/jettison_response_200_data.py
--rw-r--r--   0        0        0     1516 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/jump_gate.py
--rw-r--r--   0        0        0     1105 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/jump_ship_json_body.py
--rw-r--r--   0        0        0     1180 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/jump_ship_response_200.py
--rw-r--r--   0        0        0     1382 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/jump_ship_response_200_data.py
--rw-r--r--   0        0        0     2254 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/market.py
--rw-r--r--   0        0        0     1817 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/market_trade_good.py
--rw-r--r--   0        0        0      224 2023-05-11 19:02:43.066983 spacetraders-0.2.2/spacetraders/models/market_trade_good_supply.py
--rw-r--r--   0        0        0     2093 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/market_transaction.py
--rw-r--r--   0        0        0      170 2023-05-11 19:02:43.076983 spacetraders-0.2.2/spacetraders/models/market_transaction_type.py
--rw-r--r--   0        0        0     1143 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/meta.py
--rw-r--r--   0        0        0     1113 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/navigate_ship_json_body.py
--rw-r--r--   0        0        0     1204 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/navigate_ship_response_200.py
--rw-r--r--   0        0        0     1391 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/navigate_ship_response_200_data.py
--rw-r--r--   0        0        0     1251 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/orbit_ship_orbit_ship_200_response.py
--rw-r--r--   0        0        0     1178 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/orbit_ship_orbit_ship_200_response_data.py
--rw-r--r--   0        0        0     1316 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/patch_ship_nav_json_body.py
--rw-r--r--   0        0        0     1161 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/patch_ship_nav_response_200.py
--rw-r--r--   0        0        0     1299 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/purchase_cargo_purchase_cargo_201_response.py
--rw-r--r--   0        0        0     1431 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/purchase_cargo_purchase_cargo_201_response_data.py
--rw-r--r--   0        0        0     1148 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/purchase_cargo_purchase_cargo_request.py
--rw-r--r--   0        0        0     1270 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/purchase_ship_json_body.py
--rw-r--r--   0        0        0     1204 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/purchase_ship_response_201.py
--rw-r--r--   0        0        0     1394 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/purchase_ship_response_201_data.py
--rw-r--r--   0        0        0     1192 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/refuel_ship_response_200.py
--rw-r--r--   0        0        0     1344 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/refuel_ship_response_200_data.py
--rw-r--r--   0        0        0     1356 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/register_json_body.py
--rw-r--r--   0        0        0      244 2023-05-11 19:02:43.126983 spacetraders-0.2.2/spacetraders/models/register_json_body_faction.py
--rw-r--r--   0        0        0     1179 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/register_response_201.py
--rw-r--r--   0        0        0     1555 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/register_response_201_data.py
--rw-r--r--   0        0        0     2315 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/scanned_ship.py
--rw-r--r--   0        0        0     1081 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/scanned_ship_engine.py
--rw-r--r--   0        0        0     1078 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/scanned_ship_frame.py
--rw-r--r--   0        0        0     1086 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/scanned_ship_mounts_item.py
--rw-r--r--   0        0        0     1084 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/scanned_ship_reactor.py
--rw-r--r--   0        0        0     1429 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/scanned_system.py
--rw-r--r--   0        0        0     2187 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/scanned_waypoint.py
--rw-r--r--   0        0        0     1251 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/sell_cargo_sell_cargo_201_response.py
--rw-r--r--   0        0        0     1415 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/sell_cargo_sell_cargo_201_response_data.py
--rw-r--r--   0        0        0     1132 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/sell_cargo_sell_cargo_request.py
--rw-r--r--   0        0        0     3087 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship.py
--rw-r--r--   0        0        0     1431 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_cargo.py
--rw-r--r--   0        0        0     1447 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_cargo_item.py
--rw-r--r--   0        0        0     2160 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_crew.py
--rw-r--r--   0        0        0      167 2023-05-11 19:02:43.036983 spacetraders-0.2.2/spacetraders/models/ship_crew_rotation.py
--rw-r--r--   0        0        0     1797 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_engine.py
--rw-r--r--   0        0        0      319 2023-05-11 19:02:43.126983 spacetraders-0.2.2/spacetraders/models/ship_engine_symbol.py
--rw-r--r--   0        0        0     2192 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_frame.py
--rw-r--r--   0        0        0      694 2023-05-11 19:02:43.046983 spacetraders-0.2.2/spacetraders/models/ship_frame_symbol.py
--rw-r--r--   0        0        0     1501 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_fuel.py
--rw-r--r--   0        0        0     1324 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_fuel_consumed.py
--rw-r--r--   0        0        0     1830 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_module.py
--rw-r--r--   0        0        0     1033 2023-05-11 19:02:43.076983 spacetraders-0.2.2/spacetraders/models/ship_module_symbol.py
--rw-r--r--   0        0        0     1809 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_mount.py
--rw-r--r--   0        0        0      572 2023-05-11 19:02:43.136983 spacetraders-0.2.2/spacetraders/models/ship_mount_deposits_item.py
--rw-r--r--   0        0        0      854 2023-05-11 19:02:43.136983 spacetraders-0.2.2/spacetraders/models/ship_mount_symbol.py
--rw-r--r--   0        0        0     2034 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_nav.py
--rw-r--r--   0        0        0      206 2023-05-11 19:02:43.046983 spacetraders-0.2.2/spacetraders/models/ship_nav_flight_mode.py
--rw-r--r--   0        0        0     1875 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_nav_route.py
--rw-r--r--   0        0        0     1434 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_nav_route_waypoint.py
--rw-r--r--   0        0        0      196 2023-05-11 19:02:43.076983 spacetraders-0.2.2/spacetraders/models/ship_nav_status.py
--rw-r--r--   0        0        0     1848 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_reactor.py
--rw-r--r--   0        0        0      344 2023-05-11 19:02:43.056983 spacetraders-0.2.2/spacetraders/models/ship_reactor_symbol.py
--rw-r--r--   0        0        0     1183 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_refine_json_body.py
--rw-r--r--   0        0        0      330 2023-05-11 19:02:43.126983 spacetraders-0.2.2/spacetraders/models/ship_refine_json_body_produce.py
--rw-r--r--   0        0        0     1263 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_refine_ship_refine_200_response.py
--rw-r--r--   0        0        0     1994 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_refine_ship_refine_200_response_data.py
--rw-r--r--   0        0        0     1224 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_refine_ship_refine_200_response_data_consumed_item.py
--rw-r--r--   0        0        0     1224 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_refine_ship_refine_200_response_data_produced_item.py
--rw-r--r--   0        0        0     1430 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_registration.py
--rw-r--r--   0        0        0     1406 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/ship_requirements.py
--rw-r--r--   0        0        0      479 2023-05-11 19:02:43.116983 spacetraders-0.2.2/spacetraders/models/ship_role.py
--rw-r--r--   0        0        0      549 2023-05-11 19:02:43.036983 spacetraders-0.2.2/spacetraders/models/ship_type.py
--rw-r--r--   0        0        0     1884 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/shipyard.py
--rw-r--r--   0        0        0     2417 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/shipyard_ship.py
--rw-r--r--   0        0        0     1134 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/shipyard_ship_types_item.py
--rw-r--r--   0        0        0     1682 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/shipyard_transaction.py
--rw-r--r--   0        0        0     2212 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/survey.py
--rw-r--r--   0        0        0     1146 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/survey_deposit.py
--rw-r--r--   0        0        0      181 2023-05-11 19:02:43.056983 spacetraders-0.2.2/spacetraders/models/survey_size.py
--rw-r--r--   0        0        0     1672 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/system.py
--rw-r--r--   0        0        0     1049 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/system_faction.py
--rw-r--r--   0        0        0      405 2023-05-11 19:02:43.056983 spacetraders-0.2.2/spacetraders/models/system_type.py
--rw-r--r--   0        0        0     1289 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/system_waypoint.py
--rw-r--r--   0        0        0     1236 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/trade_good.py
--rw-r--r--   0        0        0     4422 2023-05-11 19:02:43.116983 spacetraders-0.2.2/spacetraders/models/trade_symbol.py
--rw-r--r--   0        0        0     1299 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/transfer_cargo_transfer_cargo_200_response.py
--rw-r--r--   0        0        0     1168 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/transfer_cargo_transfer_cargo_200_response_data.py
--rw-r--r--   0        0        0     1241 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/transfer_cargo_transfer_cargo_request.py
--rw-r--r--   0        0        0     1105 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/warp_ship_json_body.py
--rw-r--r--   0        0        0     1180 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/warp_ship_response_200.py
--rw-r--r--   0        0        0     1383 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/warp_ship_response_200_data.py
--rw-r--r--   0        0        0     2173 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/waypoint.py
--rw-r--r--   0        0        0     1053 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/waypoint_faction.py
--rw-r--r--   0        0        0     1115 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/waypoint_orbital.py
--rw-r--r--   0        0        0     1364 2023-05-11 19:07:21.436983 spacetraders-0.2.2/spacetraders/models/waypoint_trait.py
--rw-r--r--   0        0        0     2200 2023-05-11 19:02:43.146983 spacetraders-0.2.2/spacetraders/models/waypoint_trait_symbol.py
--rw-r--r--   0        0        0      381 2023-05-11 19:02:43.056983 spacetraders-0.2.2/spacetraders/models/waypoint_type.py
--rw-r--r--   0        0        0     1035 2023-05-11 19:02:44.006983 spacetraders-0.2.2/spacetraders/types.py
--rw-r--r--   0        0        0     3951 1970-01-01 00:00:00.000000 spacetraders-0.2.2/PKG-INFO
+-rw-r--r--   0        0        0     3472 2023-05-10 04:00:00.539673 spacetraders-0.2.3/README.md
+-rw-r--r--   0        0        0      522 2023-05-12 20:36:58.757085 spacetraders-0.2.3/pyproject.toml
+-rw-r--r--   0        0        0      250 2023-05-12 20:34:56.637085 spacetraders-0.2.3/spacetraders/__init__.py
+-rw-r--r--   0        0        0       47 2023-05-12 20:34:56.137085 spacetraders-0.2.3/spacetraders/api/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-12 20:34:56.187085 spacetraders-0.2.3/spacetraders/api/agents/__init__.py
+-rw-r--r--   0        0        0     3818 2023-05-12 20:34:56.687085 spacetraders-0.2.3/spacetraders/api/agents/get_my_agent.py
+-rw-r--r--   0        0        0        0 2023-05-12 20:34:56.187085 spacetraders-0.2.3/spacetraders/api/contracts/__init__.py
+-rw-r--r--   0        0        0     4290 2023-05-12 20:34:56.707085 spacetraders-0.2.3/spacetraders/api/contracts/accept_contract.py
+-rw-r--r--   0        0        0     5161 2023-05-12 20:34:56.777085 spacetraders-0.2.3/spacetraders/api/contracts/deliver_contract.py
+-rw-r--r--   0        0        0     4308 2023-05-12 20:34:56.727085 spacetraders-0.2.3/spacetraders/api/contracts/fulfill_contract.py
+-rw-r--r--   0        0        0     4303 2023-05-12 20:34:56.707085 spacetraders-0.2.3/spacetraders/api/contracts/get_contract.py
+-rw-r--r--   0        0        0     5015 2023-05-12 20:34:56.757085 spacetraders-0.2.3/spacetraders/api/contracts/get_contracts.py
+-rw-r--r--   0        0        0        0 2023-05-12 20:34:56.147085 spacetraders-0.2.3/spacetraders/api/default/__init__.py
+-rw-r--r--   0        0        0     9240 2023-05-12 20:34:56.847085 spacetraders-0.2.3/spacetraders/api/default/register.py
+-rw-r--r--   0        0        0        0 2023-05-12 20:34:56.187085 spacetraders-0.2.3/spacetraders/api/factions/__init__.py
+-rw-r--r--   0        0        0     4361 2023-05-12 20:34:56.727085 spacetraders-0.2.3/spacetraders/api/factions/get_faction.py
+-rw-r--r--   0        0        0     4985 2023-05-12 20:34:56.797085 spacetraders-0.2.3/spacetraders/api/factions/get_factions.py
+-rw-r--r--   0        0        0        0 2023-05-12 20:34:56.187085 spacetraders-0.2.3/spacetraders/api/fleet/__init__.py
+-rw-r--r--   0        0        0     5255 2023-05-12 20:34:56.797085 spacetraders-0.2.3/spacetraders/api/fleet/create_chart.py
+-rw-r--r--   0        0        0     4513 2023-05-12 20:34:56.757085 spacetraders-0.2.3/spacetraders/api/fleet/create_ship_ship_scan.py
+-rw-r--r--   0        0        0     4566 2023-05-12 20:34:56.707085 spacetraders-0.2.3/spacetraders/api/fleet/create_ship_system_scan.py
+-rw-r--r--   0        0        0     4610 2023-05-12 20:34:56.757085 spacetraders-0.2.3/spacetraders/api/fleet/create_ship_waypoint_scan.py
+-rw-r--r--   0        0        0     6213 2023-05-12 20:34:56.737085 spacetraders-0.2.3/spacetraders/api/fleet/create_survey.py
+-rw-r--r--   0        0        0     5356 2023-05-12 20:34:56.837085 spacetraders-0.2.3/spacetraders/api/fleet/dock_ship.py
+-rw-r--r--   0        0        0     5540 2023-05-12 20:34:56.767085 spacetraders-0.2.3/spacetraders/api/fleet/extract_resources.py
+-rw-r--r--   0        0        0     4236 2023-05-12 20:34:56.787085 spacetraders-0.2.3/spacetraders/api/fleet/get_my_ship.py
+-rw-r--r--   0        0        0     4338 2023-05-12 20:34:56.807085 spacetraders-0.2.3/spacetraders/api/fleet/get_my_ship_cargo.py
+-rw-r--r--   0        0        0     4970 2023-05-12 20:34:56.827085 spacetraders-0.2.3/spacetraders/api/fleet/get_my_ships.py
+-rw-r--r--   0        0        0     6390 2023-05-12 20:34:56.837085 spacetraders-0.2.3/spacetraders/api/fleet/get_ship_cooldown.py
+-rw-r--r--   0        0        0     4295 2023-05-12 20:34:56.827085 spacetraders-0.2.3/spacetraders/api/fleet/get_ship_nav.py
+-rw-r--r--   0        0        0     5002 2023-05-12 20:34:56.837085 spacetraders-0.2.3/spacetraders/api/fleet/jettison.py
+-rw-r--r--   0        0        0     5292 2023-05-12 20:34:56.847085 spacetraders-0.2.3/spacetraders/api/fleet/jump_ship.py
+-rw-r--r--   0        0        0     6936 2023-05-12 20:34:56.867085 spacetraders-0.2.3/spacetraders/api/fleet/navigate_ship.py
+-rw-r--r--   0        0        0     5331 2023-05-12 20:34:56.857085 spacetraders-0.2.3/spacetraders/api/fleet/orbit_ship.py
+-rw-r--r--   0        0        0     5154 2023-05-12 20:34:56.867085 spacetraders-0.2.3/spacetraders/api/fleet/patch_ship_nav.py
+-rw-r--r--   0        0        0     5373 2023-05-12 20:34:56.877085 spacetraders-0.2.3/spacetraders/api/fleet/purchase_cargo.py
+-rw-r--r--   0        0        0     4583 2023-05-12 20:34:56.877085 spacetraders-0.2.3/spacetraders/api/fleet/purchase_ship.py
+-rw-r--r--   0        0        0     4302 2023-05-12 20:34:56.857085 spacetraders-0.2.3/spacetraders/api/fleet/refuel_ship.py
+-rw-r--r--   0        0        0     5111 2023-05-12 20:34:56.907085 spacetraders-0.2.3/spacetraders/api/fleet/sell_cargo.py
+-rw-r--r--   0        0        0     5599 2023-05-12 20:34:56.877085 spacetraders-0.2.3/spacetraders/api/fleet/ship_refine.py
+-rw-r--r--   0        0        0     5424 2023-05-12 20:34:56.887085 spacetraders-0.2.3/spacetraders/api/fleet/transfer_cargo.py
+-rw-r--r--   0        0        0     6332 2023-05-12 20:34:56.967085 spacetraders-0.2.3/spacetraders/api/fleet/warp_ship.py
+-rw-r--r--   0        0        0        0 2023-05-12 20:34:56.177085 spacetraders-0.2.3/spacetraders/api/systems/__init__.py
+-rw-r--r--   0        0        0     4838 2023-05-12 20:34:56.937085 spacetraders-0.2.3/spacetraders/api/systems/get_jump_gate.py
+-rw-r--r--   0        0        0     5624 2023-05-12 20:34:56.947085 spacetraders-0.2.3/spacetraders/api/systems/get_market.py
+-rw-r--r--   0        0        0     4812 2023-05-12 20:34:56.947085 spacetraders-0.2.3/spacetraders/api/systems/get_shipyard.py
+-rw-r--r--   0        0        0     4398 2023-05-12 20:34:56.937085 spacetraders-0.2.3/spacetraders/api/systems/get_system.py
+-rw-r--r--   0        0        0     5944 2023-05-12 20:34:57.007085 spacetraders-0.2.3/spacetraders/api/systems/get_system_waypoints.py
+-rw-r--r--   0        0        0     4984 2023-05-12 20:34:56.967085 spacetraders-0.2.3/spacetraders/api/systems/get_systems.py
+-rw-r--r--   0        0        0     4799 2023-05-12 20:34:56.937085 spacetraders-0.2.3/spacetraders/api/systems/get_waypoint.py
+-rw-r--r--   0        0        0     4213 2023-05-12 20:34:56.957085 spacetraders-0.2.3/spacetraders/client.py
+-rw-r--r--   0        0        0      470 2023-05-12 20:34:56.877085 spacetraders-0.2.3/spacetraders/errors.py
+-rw-r--r--   0        0        0    13081 2023-05-12 20:34:57.077085 spacetraders-0.2.3/spacetraders/models/__init__.py
+-rw-r--r--   0        0        0     1368 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/accept_contract_response_200.py
+-rw-r--r--   0        0        0     1398 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/accept_contract_response_200_data.py
+-rw-r--r--   0        0        0     1549 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/agent.py
+-rw-r--r--   0        0        0     1661 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/chart.py
+-rw-r--r--   0        0        0     1791 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/connected_system.py
+-rw-r--r--   0        0        0     2023 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/contract.py
+-rw-r--r--   0        0        0     1801 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/contract_deliver_good.py
+-rw-r--r--   0        0        0     1429 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/contract_payment.py
+-rw-r--r--   0        0        0     1696 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/contract_terms.py
+-rw-r--r--   0        0        0      201 2023-05-12 20:34:56.307085 spacetraders-0.2.3/spacetraders/models/contract_type.py
+-rw-r--r--   0        0        0     1827 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/cooldown.py
+-rw-r--r--   0        0        0     1350 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_chart_response_201.py
+-rw-r--r--   0        0        0     1568 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_chart_response_201_data.py
+-rw-r--r--   0        0        0     1403 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_ship_ship_scan_response_201.py
+-rw-r--r--   0        0        0     1524 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_ship_ship_scan_response_201_data.py
+-rw-r--r--   0        0        0     1415 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_ship_system_scan_response_201.py
+-rw-r--r--   0        0        0     1542 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_ship_system_scan_response_201_data.py
+-rw-r--r--   0        0        0     1427 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_ship_waypoint_scan_response_201.py
+-rw-r--r--   0        0        0     1560 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_ship_waypoint_scan_response_201_data.py
+-rw-r--r--   0        0        0     1356 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_survey_response_201.py
+-rw-r--r--   0        0        0     1497 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/create_survey_response_201_data.py
+-rw-r--r--   0        0        0     1373 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/deliver_contract_json_body.py
+-rw-r--r--   0        0        0     1374 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/deliver_contract_response_200.py
+-rw-r--r--   0        0        0     1417 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/deliver_contract_response_200_data.py
+-rw-r--r--   0        0        0     1391 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/dock_ship_dock_ship_200_response.py
+-rw-r--r--   0        0        0     1326 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/dock_ship_dock_ship_200_response_data.py
+-rw-r--r--   0        0        0     1460 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/extract_resources_json_body.py
+-rw-r--r--   0        0        0     1380 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/extract_resources_response_201.py
+-rw-r--r--   0        0        0     1631 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/extract_resources_response_201_data.py
+-rw-r--r--   0        0        0     1360 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/extraction.py
+-rw-r--r--   0        0        0     1339 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/extraction_yield.py
+-rw-r--r--   0        0        0     1556 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/faction.py
+-rw-r--r--   0        0        0     1510 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/faction_trait.py
+-rw-r--r--   0        0        0     2091 2023-05-12 20:34:56.407085 spacetraders-0.2.3/spacetraders/models/faction_trait_symbol.py
+-rw-r--r--   0        0        0     1374 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/fulfill_contract_response_200.py
+-rw-r--r--   0        0        0     1400 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/fulfill_contract_response_200_data.py
+-rw-r--r--   0        0        0     1274 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_contract_response_200.py
+-rw-r--r--   0        0        0     1381 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_contracts_response_200.py
+-rw-r--r--   0        0        0     1268 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_faction_response_200.py
+-rw-r--r--   0        0        0     1375 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_factions_response_200.py
+-rw-r--r--   0        0        0     1275 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_jump_gate_response_200.py
+-rw-r--r--   0        0        0     1262 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_market_response_200.py
+-rw-r--r--   0        0        0     1260 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_my_agent_response_200.py
+-rw-r--r--   0        0        0     1285 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_my_ship_cargo_response_200.py
+-rw-r--r--   0        0        0     1261 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_my_ship_response_200.py
+-rw-r--r--   0        0        0     1361 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_my_ships_response_200.py
+-rw-r--r--   0        0        0     1361 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_ship_cooldown_response_200.py
+-rw-r--r--   0        0        0     1309 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_ship_nav_response_200.py
+-rw-r--r--   0        0        0     1274 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_shipyard_response_200.py
+-rw-r--r--   0        0        0     1262 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_system_response_200.py
+-rw-r--r--   0        0        0     1393 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_system_waypoints_response_200.py
+-rw-r--r--   0        0        0     1369 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_systems_response_200.py
+-rw-r--r--   0        0        0     1365 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/get_waypoint_response_200.py
+-rw-r--r--   0        0        0     1266 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/jettison_json_body.py
+-rw-r--r--   0        0        0     1331 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/jettison_response_200.py
+-rw-r--r--   0        0        0     1284 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/jettison_response_200_data.py
+-rw-r--r--   0        0        0     1698 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/jump_gate.py
+-rw-r--r--   0        0        0     1257 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/jump_ship_json_body.py
+-rw-r--r--   0        0        0     1332 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/jump_ship_response_200.py
+-rw-r--r--   0        0        0     1554 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/jump_ship_response_200_data.py
+-rw-r--r--   0        0        0     2490 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/market.py
+-rw-r--r--   0        0        0     1969 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/market_trade_good.py
+-rw-r--r--   0        0        0      224 2023-05-12 20:34:56.317085 spacetraders-0.2.3/spacetraders/models/market_trade_good_supply.py
+-rw-r--r--   0        0        0     2245 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/market_transaction.py
+-rw-r--r--   0        0        0      170 2023-05-12 20:34:56.317085 spacetraders-0.2.3/spacetraders/models/market_transaction_type.py
+-rw-r--r--   0        0        0     1295 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/meta.py
+-rw-r--r--   0        0        0     1265 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/navigate_ship_json_body.py
+-rw-r--r--   0        0        0     1356 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/navigate_ship_response_200.py
+-rw-r--r--   0        0        0     1543 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/navigate_ship_response_200_data.py
+-rw-r--r--   0        0        0     1403 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/orbit_ship_orbit_ship_200_response.py
+-rw-r--r--   0        0        0     1330 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/orbit_ship_orbit_ship_200_response_data.py
+-rw-r--r--   0        0        0     1509 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/patch_ship_nav_json_body.py
+-rw-r--r--   0        0        0     1313 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/patch_ship_nav_response_200.py
+-rw-r--r--   0        0        0     1451 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/purchase_cargo_purchase_cargo_201_response.py
+-rw-r--r--   0        0        0     1583 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/purchase_cargo_purchase_cargo_201_response_data.py
+-rw-r--r--   0        0        0     1300 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/purchase_cargo_purchase_cargo_request.py
+-rw-r--r--   0        0        0     1422 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/purchase_ship_json_body.py
+-rw-r--r--   0        0        0     1356 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/purchase_ship_response_201.py
+-rw-r--r--   0        0        0     1546 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/purchase_ship_response_201_data.py
+-rw-r--r--   0        0        0     1344 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/refuel_ship_response_200.py
+-rw-r--r--   0        0        0     1496 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/refuel_ship_response_200_data.py
+-rw-r--r--   0        0        0     1508 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/register_json_body.py
+-rw-r--r--   0        0        0      244 2023-05-12 20:34:56.377085 spacetraders-0.2.3/spacetraders/models/register_json_body_faction.py
+-rw-r--r--   0        0        0     1331 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/register_response_201.py
+-rw-r--r--   0        0        0     1707 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/register_response_201_data.py
+-rw-r--r--   0        0        0     2536 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/scanned_ship.py
+-rw-r--r--   0        0        0     1233 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/scanned_ship_engine.py
+-rw-r--r--   0        0        0     1230 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/scanned_ship_frame.py
+-rw-r--r--   0        0        0     1238 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/scanned_ship_mounts_item.py
+-rw-r--r--   0        0        0     1236 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/scanned_ship_reactor.py
+-rw-r--r--   0        0        0     1581 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/scanned_system.py
+-rw-r--r--   0        0        0     2385 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/scanned_waypoint.py
+-rw-r--r--   0        0        0     1403 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/sell_cargo_sell_cargo_201_response.py
+-rw-r--r--   0        0        0     1567 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/sell_cargo_sell_cargo_201_response_data.py
+-rw-r--r--   0        0        0     1284 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/sell_cargo_sell_cargo_request.py
+-rw-r--r--   0        0        0     3239 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship.py
+-rw-r--r--   0        0        0     1583 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_cargo.py
+-rw-r--r--   0        0        0     1599 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_cargo_item.py
+-rw-r--r--   0        0        0     2337 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_crew.py
+-rw-r--r--   0        0        0      167 2023-05-12 20:34:56.277085 spacetraders-0.2.3/spacetraders/models/ship_crew_rotation.py
+-rw-r--r--   0        0        0     1975 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_engine.py
+-rw-r--r--   0        0        0      319 2023-05-12 20:34:56.387085 spacetraders-0.2.3/spacetraders/models/ship_engine_symbol.py
+-rw-r--r--   0        0        0     2370 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_frame.py
+-rw-r--r--   0        0        0      694 2023-05-12 20:34:56.297085 spacetraders-0.2.3/spacetraders/models/ship_frame_symbol.py
+-rw-r--r--   0        0        0     1678 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_fuel.py
+-rw-r--r--   0        0        0     1476 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_fuel_consumed.py
+-rw-r--r--   0        0        0     2057 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_module.py
+-rw-r--r--   0        0        0     1033 2023-05-12 20:34:56.317085 spacetraders-0.2.3/spacetraders/models/ship_module_symbol.py
+-rw-r--r--   0        0        0     2039 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_mount.py
+-rw-r--r--   0        0        0      572 2023-05-12 20:34:56.387085 spacetraders-0.2.3/spacetraders/models/ship_mount_deposits_item.py
+-rw-r--r--   0        0        0      854 2023-05-12 20:34:56.387085 spacetraders-0.2.3/spacetraders/models/ship_mount_symbol.py
+-rw-r--r--   0        0        0     2213 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_nav.py
+-rw-r--r--   0        0        0      206 2023-05-12 20:34:56.297085 spacetraders-0.2.3/spacetraders/models/ship_nav_flight_mode.py
+-rw-r--r--   0        0        0     2027 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_nav_route.py
+-rw-r--r--   0        0        0     1586 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_nav_route_waypoint.py
+-rw-r--r--   0        0        0      196 2023-05-12 20:34:56.317085 spacetraders-0.2.3/spacetraders/models/ship_nav_status.py
+-rw-r--r--   0        0        0     2026 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_reactor.py
+-rw-r--r--   0        0        0      344 2023-05-12 20:34:56.297085 spacetraders-0.2.3/spacetraders/models/ship_reactor_symbol.py
+-rw-r--r--   0        0        0     1335 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_refine_json_body.py
+-rw-r--r--   0        0        0      330 2023-05-12 20:34:56.377085 spacetraders-0.2.3/spacetraders/models/ship_refine_json_body_produce.py
+-rw-r--r--   0        0        0     1415 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_refine_ship_refine_200_response.py
+-rw-r--r--   0        0        0     2146 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_refine_ship_refine_200_response_data.py
+-rw-r--r--   0        0        0     1426 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_refine_ship_refine_200_response_data_consumed_item.py
+-rw-r--r--   0        0        0     1426 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_refine_ship_refine_200_response_data_produced_item.py
+-rw-r--r--   0        0        0     1612 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_registration.py
+-rw-r--r--   0        0        0     1623 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/ship_requirements.py
+-rw-r--r--   0        0        0      479 2023-05-12 20:34:56.367085 spacetraders-0.2.3/spacetraders/models/ship_role.py
+-rw-r--r--   0        0        0      549 2023-05-12 20:34:56.287085 spacetraders-0.2.3/spacetraders/models/ship_type.py
+-rw-r--r--   0        0        0     2101 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/shipyard.py
+-rw-r--r--   0        0        0     2590 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/shipyard_ship.py
+-rw-r--r--   0        0        0     1307 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/shipyard_ship_types_item.py
+-rw-r--r--   0        0        0     1834 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/shipyard_transaction.py
+-rw-r--r--   0        0        0     2364 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/survey.py
+-rw-r--r--   0        0        0     1298 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/survey_deposit.py
+-rw-r--r--   0        0        0      181 2023-05-12 20:34:56.307085 spacetraders-0.2.3/spacetraders/models/survey_size.py
+-rw-r--r--   0        0        0     1824 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/system.py
+-rw-r--r--   0        0        0     1201 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/system_faction.py
+-rw-r--r--   0        0        0      405 2023-05-12 20:34:56.297085 spacetraders-0.2.3/spacetraders/models/system_type.py
+-rw-r--r--   0        0        0     1441 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/system_waypoint.py
+-rw-r--r--   0        0        0     1388 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/trade_good.py
+-rw-r--r--   0        0        0     4422 2023-05-12 20:34:56.377085 spacetraders-0.2.3/spacetraders/models/trade_symbol.py
+-rw-r--r--   0        0        0     1451 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/transfer_cargo_transfer_cargo_200_response.py
+-rw-r--r--   0        0        0     1320 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/transfer_cargo_transfer_cargo_200_response_data.py
+-rw-r--r--   0        0        0     1393 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/transfer_cargo_transfer_cargo_request.py
+-rw-r--r--   0        0        0     1257 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/warp_ship_json_body.py
+-rw-r--r--   0        0        0     1332 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/warp_ship_response_200.py
+-rw-r--r--   0        0        0     1535 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/warp_ship_response_200_data.py
+-rw-r--r--   0        0        0     2371 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/waypoint.py
+-rw-r--r--   0        0        0     1205 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/waypoint_faction.py
+-rw-r--r--   0        0        0     1267 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/waypoint_orbital.py
+-rw-r--r--   0        0        0     1516 2023-05-12 20:36:34.927085 spacetraders-0.2.3/spacetraders/models/waypoint_trait.py
+-rw-r--r--   0        0        0     2200 2023-05-12 20:34:56.407085 spacetraders-0.2.3/spacetraders/models/waypoint_trait_symbol.py
+-rw-r--r--   0        0        0      381 2023-05-12 20:34:56.307085 spacetraders-0.2.3/spacetraders/models/waypoint_type.py
+-rw-r--r--   0        0        0     1035 2023-05-12 20:34:57.397085 spacetraders-0.2.3/spacetraders/types.py
+-rw-r--r--   0        0        0     3951 1970-01-01 00:00:00.000000 spacetraders-0.2.3/PKG-INFO
```

### Comparing `spacetraders-0.2.2/README.md` & `spacetraders-0.2.3/README.md`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/pyproject.toml` & `spacetraders-0.2.3/pyproject.toml`

 * *Files 24% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "spacetraders"
-version = "0.2.2"
+version = "0.2.3"
 description = "Python API for Space Traders"
 authors = ["Marco Ceppi <marco@ceppi.net>"]
 license = "Apache-2.0"
 readme = "README.md"
 packages = [{include = "spacetraders"}]
 
 [tool.poetry.dependencies]
```

### Comparing `spacetraders-0.2.2/spacetraders/api/agents/get_my_agent.py` & `spacetraders-0.2.3/spacetraders/api/agents/get_my_agent.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/contracts/accept_contract.py` & `spacetraders-0.2.3/spacetraders/api/contracts/accept_contract.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/contracts/deliver_contract.py` & `spacetraders-0.2.3/spacetraders/api/contracts/deliver_contract.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/contracts/fulfill_contract.py` & `spacetraders-0.2.3/spacetraders/api/contracts/fulfill_contract.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/contracts/get_contract.py` & `spacetraders-0.2.3/spacetraders/api/contracts/get_contract.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/contracts/get_contracts.py` & `spacetraders-0.2.3/spacetraders/api/contracts/get_contracts.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/default/register.py` & `spacetraders-0.2.3/spacetraders/api/default/register.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/factions/get_faction.py` & `spacetraders-0.2.3/spacetraders/api/factions/get_faction.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/factions/get_factions.py` & `spacetraders-0.2.3/spacetraders/api/factions/get_factions.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/create_chart.py` & `spacetraders-0.2.3/spacetraders/api/fleet/create_chart.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/create_ship_ship_scan.py` & `spacetraders-0.2.3/spacetraders/api/fleet/create_ship_ship_scan.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/create_ship_system_scan.py` & `spacetraders-0.2.3/spacetraders/api/fleet/create_ship_system_scan.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/create_ship_waypoint_scan.py` & `spacetraders-0.2.3/spacetraders/api/fleet/create_ship_waypoint_scan.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/create_survey.py` & `spacetraders-0.2.3/spacetraders/api/fleet/create_survey.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/dock_ship.py` & `spacetraders-0.2.3/spacetraders/api/fleet/dock_ship.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/extract_resources.py` & `spacetraders-0.2.3/spacetraders/api/fleet/extract_resources.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/get_my_ship.py` & `spacetraders-0.2.3/spacetraders/api/fleet/get_my_ship.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/get_my_ship_cargo.py` & `spacetraders-0.2.3/spacetraders/api/fleet/get_my_ship_cargo.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/get_my_ships.py` & `spacetraders-0.2.3/spacetraders/api/fleet/get_my_ships.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/get_ship_cooldown.py` & `spacetraders-0.2.3/spacetraders/api/fleet/get_ship_cooldown.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/get_ship_nav.py` & `spacetraders-0.2.3/spacetraders/api/fleet/get_ship_nav.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/jettison.py` & `spacetraders-0.2.3/spacetraders/api/fleet/jettison.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/jump_ship.py` & `spacetraders-0.2.3/spacetraders/api/fleet/jump_ship.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/navigate_ship.py` & `spacetraders-0.2.3/spacetraders/api/fleet/navigate_ship.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/orbit_ship.py` & `spacetraders-0.2.3/spacetraders/api/fleet/orbit_ship.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/patch_ship_nav.py` & `spacetraders-0.2.3/spacetraders/api/fleet/patch_ship_nav.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/purchase_cargo.py` & `spacetraders-0.2.3/spacetraders/api/fleet/purchase_cargo.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/purchase_ship.py` & `spacetraders-0.2.3/spacetraders/api/fleet/purchase_ship.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/refuel_ship.py` & `spacetraders-0.2.3/spacetraders/api/fleet/refuel_ship.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/sell_cargo.py` & `spacetraders-0.2.3/spacetraders/api/fleet/sell_cargo.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/ship_refine.py` & `spacetraders-0.2.3/spacetraders/api/fleet/ship_refine.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/transfer_cargo.py` & `spacetraders-0.2.3/spacetraders/api/fleet/transfer_cargo.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/fleet/warp_ship.py` & `spacetraders-0.2.3/spacetraders/api/fleet/warp_ship.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/systems/get_jump_gate.py` & `spacetraders-0.2.3/spacetraders/api/systems/get_jump_gate.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/systems/get_market.py` & `spacetraders-0.2.3/spacetraders/api/systems/get_market.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/systems/get_shipyard.py` & `spacetraders-0.2.3/spacetraders/api/systems/get_shipyard.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/systems/get_system.py` & `spacetraders-0.2.3/spacetraders/api/systems/get_system.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/systems/get_system_waypoints.py` & `spacetraders-0.2.3/spacetraders/api/systems/get_system_waypoints.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/systems/get_systems.py` & `spacetraders-0.2.3/spacetraders/api/systems/get_systems.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/api/systems/get_waypoint.py` & `spacetraders-0.2.3/spacetraders/api/systems/get_waypoint.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/client.py` & `spacetraders-0.2.3/spacetraders/client.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/__init__.py` & `spacetraders-0.2.3/spacetraders/models/__init__.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/accept_contract_response_200.py` & `spacetraders-0.2.3/spacetraders/models/create_chart_response_201.py`

 * *Files 12% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.accept_contract_response_200_data import AcceptContractResponse200Data
+from ..models.create_chart_response_201_data import CreateChartResponse201Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="AcceptContractResponse200")
+T = TypeVar("T", bound="CreateChartResponse201")
 
 
-class AcceptContractResponse200(BaseModel):
+class CreateChartResponse201(BaseModel):
     """
     Attributes:
-        data (AcceptContractResponse200Data):
+        data (CreateChartResponse201Data):
     """
 
-    data: "AcceptContractResponse200Data" = Field(alias="data")
+    data: "CreateChartResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/accept_contract_response_200_data.py` & `spacetraders-0.2.3/spacetraders/models/extraction.py`

 * *Files 12% similar despite different names*

```diff
@@ -11,36 +11,39 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..models.contract import Contract
+from ..models.extraction_yield import ExtractionYield
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="AcceptContractResponse200Data")
+T = TypeVar("T", bound="Extraction")
 
 
-class AcceptContractResponse200Data(BaseModel):
+class Extraction(BaseModel):
     """
     Attributes:
-        agent (Agent):
-        contract (Contract):
+        ship_symbol (str):
+        yield_ (ExtractionYield):
     """
 
-    agent: "Agent" = Field(alias="agent")
-    contract: "Contract" = Field(alias="contract")
+    ship_symbol: str = Field(alias="shipSymbol")
+    yield_: "ExtractionYield" = Field(alias="yield")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/agent.py` & `spacetraders-0.2.3/spacetraders/models/faction.py`

 * *Files 12% similar despite different names*

```diff
@@ -5,44 +5,51 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
+from ..models.faction_trait import FactionTrait
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="Agent")
+T = TypeVar("T", bound="Faction")
 
 
-class Agent(BaseModel):
+class Faction(BaseModel):
     """
     Attributes:
-        account_id (str):
         symbol (str):
-        headquarters (str): The headquarters of the agent.
-        credits_ (int): The number of credits the agent has available. Credits can be negative if funds have been
-            overdrawn.
+        name (str):
+        description (str):
+        headquarters (str):
+        traits (List['FactionTrait']):
     """
 
-    account_id: str = Field(alias="accountId")
     symbol: str = Field(alias="symbol")
+    name: str = Field(alias="name")
+    description: str = Field(alias="description")
     headquarters: str = Field(alias="headquarters")
-    credits_: int = Field(alias="credits")
+    traits: List["FactionTrait"] = Field(alias="traits")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/chart.py` & `spacetraders-0.2.3/spacetraders/models/jump_ship_json_body.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,50 +1,45 @@
-import datetime
 from typing import (
     TYPE_CHECKING,
     Any,
     BinaryIO,
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
-    cast,
 )
 
 import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="Chart")
+T = TypeVar("T", bound="JumpShipJsonBody")
 
 
-class Chart(BaseModel):
-    """The chart of a system or waypoint, which makes the location visible to other agents.
-
+class JumpShipJsonBody(BaseModel):
+    """
     Attributes:
-        waypoint_symbol (Union[Unset, str]):
-        submitted_by (Union[Unset, str]):
-        submitted_on (Union[Unset, datetime.datetime]):
+        system_symbol (str): The system symbol to jump to.
     """
 
-    waypoint_symbol: Union[Unset, str] = UNSET
-    submitted_by: Union[Unset, str] = UNSET
-    submitted_on: Union[Unset, datetime.datetime] = UNSET
+    system_symbol: str = Field(alias="systemSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/connected_system.py` & `spacetraders-0.2.3/spacetraders/models/connected_system.py`

 * *Files 5% similar despite different names*

```diff
@@ -35,21 +35,25 @@
 
     symbol: str = Field(alias="symbol")
     sector_symbol: str = Field(alias="sectorSymbol")
     type: SystemType = Field(alias="type")
     x: int = Field(alias="x")
     y: int = Field(alias="y")
     distance: int = Field(alias="distance")
-    faction_symbol: Union[Unset, str] = UNSET
+    faction_symbol: Union[Unset, str] = Field(UNSET, alias="factionSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/contract.py` & `spacetraders-0.2.3/spacetraders/models/contract.py`

 * *Files 9% similar despite different names*

```diff
@@ -37,22 +37,26 @@
     """
 
     id: str = Field(alias="id")
     faction_symbol: str = Field(alias="factionSymbol")
     type: ContractType = Field(alias="type")
     terms: "ContractTerms" = Field(alias="terms")
     expiration: datetime.datetime = Field(alias="expiration")
-    accepted: bool = False
-    fulfilled: bool = False
+    accepted: bool = Field(False, alias="accepted")
+    fulfilled: bool = Field(False, alias="fulfilled")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/contract_deliver_good.py` & `spacetraders-0.2.3/spacetraders/models/contract_deliver_good.py`

 * *Files 4% similar despite different names*

```diff
@@ -35,14 +35,18 @@
     units_fulfilled: int = Field(alias="unitsFulfilled")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/contract_payment.py` & `spacetraders-0.2.3/spacetraders/models/scanned_ship_engine.py`

 * *Files 12% similar despite different names*

```diff
@@ -12,32 +12,35 @@
 )
 
 import attr
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ContractPayment")
+T = TypeVar("T", bound="ScannedShipEngine")
 
 
-class ContractPayment(BaseModel):
-    """
+class ScannedShipEngine(BaseModel):
+    """The engine of the ship.
+
     Attributes:
-        on_accepted (int): The amount of credits received up front for accepting the contract.
-        on_fulfilled (int): The amount of credits received when the contract is fulfilled.
+        symbol (str):
     """
 
-    on_accepted: int = Field(alias="onAccepted")
-    on_fulfilled: int = Field(alias="onFulfilled")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/contract_terms.py` & `spacetraders-0.2.3/spacetraders/models/contract_terms.py`

 * *Files 11% similar despite different names*

```diff
@@ -31,21 +31,25 @@
         deadline (datetime.datetime): The deadline for the contract.
         payment (ContractPayment):
         deliver (Union[Unset, List['ContractDeliverGood']]):
     """
 
     deadline: datetime.datetime = Field(alias="deadline")
     payment: "ContractPayment" = Field(alias="payment")
-    deliver: Union[Unset, List["ContractDeliverGood"]] = UNSET
+    deliver: Union[Unset, List["ContractDeliverGood"]] = Field(UNSET, alias="deliver")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/cooldown.py` & `spacetraders-0.2.3/spacetraders/models/cooldown.py`

 * *Files 17% similar despite different names*

```diff
@@ -38,14 +38,18 @@
     expiration: datetime.datetime = Field(alias="expiration")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_chart_response_201.py` & `spacetraders-0.2.3/spacetraders/models/sell_cargo_sell_cargo_201_response.py`

 * *Files 26% similar despite different names*

```diff
@@ -11,33 +11,39 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.create_chart_response_201_data import CreateChartResponse201Data
+from ..models.sell_cargo_sell_cargo_201_response_data import (
+    SellCargoSellCargo201ResponseData,
+)
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="CreateChartResponse201")
+T = TypeVar("T", bound="SellCargoSellCargo201Response")
 
 
-class CreateChartResponse201(BaseModel):
+class SellCargoSellCargo201Response(BaseModel):
     """
     Attributes:
-        data (CreateChartResponse201Data):
+        data (SellCargoSellCargo201ResponseData):
     """
 
-    data: "CreateChartResponse201Data" = Field(alias="data")
+    data: "SellCargoSellCargo201ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_chart_response_201_data.py` & `spacetraders-0.2.3/spacetraders/models/create_chart_response_201_data.py`

 * *Files 8% similar despite different names*

```diff
@@ -33,14 +33,18 @@
     waypoint: "Waypoint" = Field(alias="waypoint")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_ship_ship_scan_response_201.py` & `spacetraders-0.2.3/spacetraders/models/get_shipyard_response_200.py`

 * *Files 14% similar despite different names*

```diff
@@ -11,35 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.create_ship_ship_scan_response_201_data import (
-    CreateShipShipScanResponse201Data,
-)
+from ..models.shipyard import Shipyard
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="CreateShipShipScanResponse201")
+T = TypeVar("T", bound="GetShipyardResponse200")
 
 
-class CreateShipShipScanResponse201(BaseModel):
+class GetShipyardResponse200(BaseModel):
     """
     Attributes:
-        data (CreateShipShipScanResponse201Data):
+        data (Shipyard):
     """
 
-    data: "CreateShipShipScanResponse201Data" = Field(alias="data")
+    data: "Shipyard" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_ship_ship_scan_response_201_data.py` & `spacetraders-0.2.3/spacetraders/models/get_market_response_200.py`

 * *Files 14% similar despite different names*

```diff
@@ -11,36 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.cooldown import Cooldown
-from ..models.scanned_ship import ScannedShip
+from ..models.market import Market
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="CreateShipShipScanResponse201Data")
+T = TypeVar("T", bound="GetMarketResponse200")
 
 
-class CreateShipShipScanResponse201Data(BaseModel):
+class GetMarketResponse200(BaseModel):
     """
     Attributes:
-        cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
-        ships (List['ScannedShip']):
+        data (Market):
     """
 
-    cooldown: "Cooldown" = Field(alias="cooldown")
-    ships: List["ScannedShip"] = Field(alias="ships")
+    data: "Market" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_ship_system_scan_response_201.py` & `spacetraders-0.2.3/spacetraders/models/create_ship_system_scan_response_201.py`

 * *Files 12% similar despite different names*

```diff
@@ -32,14 +32,18 @@
     data: "CreateShipSystemScanResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_ship_system_scan_response_201_data.py` & `spacetraders-0.2.3/spacetraders/models/create_ship_system_scan_response_201_data.py`

 * *Files 11% similar despite different names*

```diff
@@ -33,14 +33,18 @@
     systems: List["ScannedSystem"] = Field(alias="systems")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_ship_waypoint_scan_response_201.py` & `spacetraders-0.2.3/spacetraders/models/create_ship_waypoint_scan_response_201.py`

 * *Files 12% similar despite different names*

```diff
@@ -32,14 +32,18 @@
     data: "CreateShipWaypointScanResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_ship_waypoint_scan_response_201_data.py` & `spacetraders-0.2.3/spacetraders/models/create_ship_waypoint_scan_response_201_data.py`

 * *Files 11% similar despite different names*

```diff
@@ -33,14 +33,18 @@
     waypoints: List["ScannedWaypoint"] = Field(alias="waypoints")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_survey_response_201.py` & `spacetraders-0.2.3/spacetraders/models/create_survey_response_201.py`

 * *Files 16% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     data: "CreateSurveyResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/create_survey_response_201_data.py` & `spacetraders-0.2.3/spacetraders/models/get_my_ships_response_200.py`

 * *Files 15% similar despite different names*

```diff
@@ -11,36 +11,40 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.cooldown import Cooldown
-from ..models.survey import Survey
+from ..models.meta import Meta
+from ..models.ship import Ship
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="CreateSurveyResponse201Data")
+T = TypeVar("T", bound="GetMyShipsResponse200")
 
 
-class CreateSurveyResponse201Data(BaseModel):
+class GetMyShipsResponse200(BaseModel):
     """
     Attributes:
-        cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
-        surveys (List['Survey']):
+        data (List['Ship']):
+        meta (Meta):
     """
 
-    cooldown: "Cooldown" = Field(alias="cooldown")
-    surveys: List["Survey"] = Field(alias="surveys")
+    data: List["Ship"] = Field(alias="data")
+    meta: "Meta" = Field(alias="meta")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/deliver_contract_json_body.py` & `spacetraders-0.2.3/spacetraders/models/get_my_ship_response_200.py`

 * *Files 11% similar despite different names*

```diff
@@ -5,41 +5,43 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
+from ..models.ship import Ship
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="DeliverContractJsonBody")
+T = TypeVar("T", bound="GetMyShipResponse200")
 
 
-class DeliverContractJsonBody(BaseModel):
+class GetMyShipResponse200(BaseModel):
     """
     Attributes:
-        ship_symbol (str):
-        trade_symbol (str):
-        units (int):
+        data (Ship): A ship
     """
 
-    ship_symbol: str = Field(alias="shipSymbol")
-    trade_symbol: str = Field(alias="tradeSymbol")
-    units: int = Field(alias="units")
+    data: "Ship" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/deliver_contract_response_200.py` & `spacetraders-0.2.3/spacetraders/models/system_faction.py`

 * *Files 20% similar despite different names*

```diff
@@ -5,39 +5,41 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.deliver_contract_response_200_data import DeliverContractResponse200Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="DeliverContractResponse200")
+T = TypeVar("T", bound="SystemFaction")
 
 
-class DeliverContractResponse200(BaseModel):
+class SystemFaction(BaseModel):
     """
     Attributes:
-        data (DeliverContractResponse200Data):
+        symbol (str):
     """
 
-    data: "DeliverContractResponse200Data" = Field(alias="data")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/deliver_contract_response_200_data.py` & `spacetraders-0.2.3/spacetraders/models/get_contract_response_200.py`

 * *Files 16% similar despite different names*

```diff
@@ -12,35 +12,36 @@
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
 from ..models.contract import Contract
-from ..models.ship_cargo import ShipCargo
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="DeliverContractResponse200Data")
+T = TypeVar("T", bound="GetContractResponse200")
 
 
-class DeliverContractResponse200Data(BaseModel):
+class GetContractResponse200(BaseModel):
     """
     Attributes:
-        contract (Contract):
-        cargo (ShipCargo):
+        data (Contract):
     """
 
-    contract: "Contract" = Field(alias="contract")
-    cargo: "ShipCargo" = Field(alias="cargo")
+    data: "Contract" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/dock_ship_dock_ship_200_response.py` & `spacetraders-0.2.3/spacetraders/models/dock_ship_dock_ship_200_response.py`

 * *Files 7% similar despite different names*

```diff
@@ -32,14 +32,18 @@
     data: "DockShipDockShip200ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/dock_ship_dock_ship_200_response_data.py` & `spacetraders-0.2.3/spacetraders/models/get_my_ship_cargo_response_200.py`

 * *Files 10% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_nav import ShipNav
+from ..models.ship_cargo import ShipCargo
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="DockShipDockShip200ResponseData")
+T = TypeVar("T", bound="GetMyShipCargoResponse200")
 
 
-class DockShipDockShip200ResponseData(BaseModel):
+class GetMyShipCargoResponse200(BaseModel):
     """
     Attributes:
-        nav (ShipNav): The navigation information of the ship.
+        data (ShipCargo):
     """
 
-    nav: "ShipNav" = Field(alias="nav")
+    data: "ShipCargo" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/extract_resources_json_body.py` & `spacetraders-0.2.3/spacetraders/models/navigate_ship_json_body.py`

 * *Files 12% similar despite different names*

```diff
@@ -5,41 +5,41 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.survey import Survey
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ExtractResourcesJsonBody")
+T = TypeVar("T", bound="NavigateShipJsonBody")
 
 
-class ExtractResourcesJsonBody(BaseModel):
+class NavigateShipJsonBody(BaseModel):
     """
     Attributes:
-        survey (Union[Unset, Survey]): A resource survey of a waypoint, detailing a specific extraction location and the
-            types of resources that can be found there.
+        waypoint_symbol (str): The target destination.
     """
 
-    survey: Union[Unset, "Survey"] = UNSET
+    waypoint_symbol: str = Field(alias="waypointSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/extract_resources_response_201.py` & `spacetraders-0.2.3/spacetraders/models/jettison_response_200.py`

 * *Files 14% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.extract_resources_response_201_data import ExtractResourcesResponse201Data
+from ..models.jettison_response_200_data import JettisonResponse200Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ExtractResourcesResponse201")
+T = TypeVar("T", bound="JettisonResponse200")
 
 
-class ExtractResourcesResponse201(BaseModel):
+class JettisonResponse200(BaseModel):
     """
     Attributes:
-        data (ExtractResourcesResponse201Data):
+        data (JettisonResponse200Data):
     """
 
-    data: "ExtractResourcesResponse201Data" = Field(alias="data")
+    data: "JettisonResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/extract_resources_response_201_data.py` & `spacetraders-0.2.3/spacetraders/models/extract_resources_response_201_data.py`

 * *Files 12% similar despite different names*

```diff
@@ -36,14 +36,18 @@
     cargo: "ShipCargo" = Field(alias="cargo")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/extraction.py` & `spacetraders-0.2.3/spacetraders/models/ship_requirements.py`

 * *Files 21% similar despite different names*

```diff
@@ -5,41 +5,47 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
+    Union,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.extraction_yield import ExtractionYield
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="Extraction")
+T = TypeVar("T", bound="ShipRequirements")
 
 
-class Extraction(BaseModel):
-    """
+class ShipRequirements(BaseModel):
+    """The requirements for installation on a ship
+
     Attributes:
-        ship_symbol (str):
-        yield_ (ExtractionYield):
+        power (Union[Unset, int]): The amount of power required from the reactor.
+        crew (Union[Unset, int]): The number of crew required for operation.
+        slots (Union[Unset, int]): The number of module slots required for installation.
     """
 
-    ship_symbol: str = Field(alias="shipSymbol")
-    yield_: "ExtractionYield" = Field(alias="yield")
+    power: Union[Unset, int] = Field(UNSET, alias="power")
+    crew: Union[Unset, int] = Field(UNSET, alias="crew")
+    slots: Union[Unset, int] = Field(UNSET, alias="slots")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/extraction_yield.py` & `spacetraders-0.2.3/spacetraders/models/extraction_yield.py`

 * *Files 16% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/faction.py` & `spacetraders-0.2.3/spacetraders/models/ship_registration.py`

 * *Files 20% similar despite different names*

```diff
@@ -5,47 +5,48 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
+    Union,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.faction_trait import FactionTrait
+from ..models.ship_role import ShipRole
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="Faction")
+T = TypeVar("T", bound="ShipRegistration")
 
 
-class Faction(BaseModel):
-    """
+class ShipRegistration(BaseModel):
+    """The public registration information of the ship
+
     Attributes:
-        symbol (str):
-        name (str):
-        description (str):
-        headquarters (str):
-        traits (List['FactionTrait']):
+        name (str): The agent's registered name of the ship
+        role (ShipRole): The registered role of the ship
+        faction_symbol (Union[Unset, str]): The symbol of the faction the ship is registered with
     """
 
-    symbol: str = Field(alias="symbol")
     name: str = Field(alias="name")
-    description: str = Field(alias="description")
-    headquarters: str = Field(alias="headquarters")
-    traits: List["FactionTrait"] = Field(alias="traits")
+    role: ShipRole = Field(alias="role")
+    faction_symbol: Union[Unset, str] = Field(UNSET, alias="factionSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/faction_trait.py` & `spacetraders-0.2.3/spacetraders/models/patch_ship_nav_response_200.py`

 * *Files 12% similar despite different names*

```diff
@@ -5,42 +5,43 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.faction_trait_symbol import FactionTraitSymbol
+from ..models.ship_nav import ShipNav
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="FactionTrait")
+T = TypeVar("T", bound="PatchShipNavResponse200")
 
 
-class FactionTrait(BaseModel):
+class PatchShipNavResponse200(BaseModel):
     """
     Attributes:
-        symbol (FactionTraitSymbol): The unique identifier of the trait.
-        name (str): The name of the trait.
-        description (str): A description of the trait.
+        data (ShipNav): The navigation information of the ship.
     """
 
-    symbol: FactionTraitSymbol = Field(alias="symbol")
-    name: str = Field(alias="name")
-    description: str = Field(alias="description")
+    data: "ShipNav" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/faction_trait_symbol.py` & `spacetraders-0.2.3/spacetraders/models/faction_trait_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/fulfill_contract_response_200.py` & `spacetraders-0.2.3/spacetraders/models/fulfill_contract_response_200.py`

 * *Files 9% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     data: "FulfillContractResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/fulfill_contract_response_200_data.py` & `spacetraders-0.2.3/spacetraders/models/waypoint_faction.py`

 * *Files 21% similar despite different names*

```diff
@@ -5,42 +5,41 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..models.contract import Contract
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="FulfillContractResponse200Data")
+T = TypeVar("T", bound="WaypointFaction")
 
 
-class FulfillContractResponse200Data(BaseModel):
+class WaypointFaction(BaseModel):
     """
     Attributes:
-        agent (Agent):
-        contract (Contract):
+        symbol (str):
     """
 
-    agent: "Agent" = Field(alias="agent")
-    contract: "Contract" = Field(alias="contract")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_contract_response_200.py` & `spacetraders-0.2.3/spacetraders/models/ship_engine.py`

 * *Files 26% similar despite different names*

```diff
@@ -5,39 +5,57 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    Union,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.contract import Contract
+from ..models.ship_engine_symbol import ShipEngineSymbol
+from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetContractResponse200")
+T = TypeVar("T", bound="ShipEngine")
 
 
-class GetContractResponse200(BaseModel):
-    """
+class ShipEngine(BaseModel):
+    """The engine determines how quickly a ship travels between waypoints.
+
     Attributes:
-        data (Contract):
+        symbol (ShipEngineSymbol):
+        name (str):
+        description (str):
+        speed (float):
+        requirements (ShipRequirements): The requirements for installation on a ship
+        condition (Union[Unset, int]): Condition is a range of 0 to 100 where 0 is completely worn out and 100 is brand
+            new.
     """
 
-    data: "Contract" = Field(alias="data")
+    symbol: ShipEngineSymbol = Field(alias="symbol")
+    name: str = Field(alias="name")
+    description: str = Field(alias="description")
+    speed: float = Field(alias="speed")
+    requirements: "ShipRequirements" = Field(alias="requirements")
+    condition: Union[Unset, int] = Field(UNSET, alias="condition")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_contracts_response_200.py` & `spacetraders-0.2.3/spacetraders/models/scanned_ship_frame.py`

 * *Files 17% similar despite different names*

```diff
@@ -5,42 +5,42 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.contract import Contract
-from ..models.meta import Meta
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetContractsResponse200")
+T = TypeVar("T", bound="ScannedShipFrame")
 
 
-class GetContractsResponse200(BaseModel):
-    """
+class ScannedShipFrame(BaseModel):
+    """The frame of the ship.
+
     Attributes:
-        data (List['Contract']):
-        meta (Meta):
+        symbol (str):
     """
 
-    data: List["Contract"] = Field(alias="data")
-    meta: "Meta" = Field(alias="meta")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_faction_response_200.py` & `spacetraders-0.2.3/spacetraders/models/get_faction_response_200.py`

 * *Files 15% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     data: "Faction" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_factions_response_200.py` & `spacetraders-0.2.3/spacetraders/models/purchase_ship_response_201_data.py`

 * *Files 18% similar despite different names*

```diff
@@ -11,36 +11,43 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.faction import Faction
-from ..models.meta import Meta
+from ..models.agent import Agent
+from ..models.ship import Ship
+from ..models.shipyard_transaction import ShipyardTransaction
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetFactionsResponse200")
+T = TypeVar("T", bound="PurchaseShipResponse201Data")
 
 
-class GetFactionsResponse200(BaseModel):
+class PurchaseShipResponse201Data(BaseModel):
     """
     Attributes:
-        data (List['Faction']):
-        meta (Meta):
+        agent (Agent):
+        ship (Ship): A ship
+        transaction (ShipyardTransaction):
     """
 
-    data: List["Faction"] = Field(alias="data")
-    meta: "Meta" = Field(alias="meta")
+    agent: "Agent" = Field(alias="agent")
+    ship: "Ship" = Field(alias="ship")
+    transaction: "ShipyardTransaction" = Field(alias="transaction")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_jump_gate_response_200.py` & `spacetraders-0.2.3/spacetraders/models/fulfill_contract_response_200_data.py`

 * *Files 25% similar despite different names*

```diff
@@ -11,33 +11,40 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.jump_gate import JumpGate
+from ..models.agent import Agent
+from ..models.contract import Contract
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetJumpGateResponse200")
+T = TypeVar("T", bound="FulfillContractResponse200Data")
 
 
-class GetJumpGateResponse200(BaseModel):
+class FulfillContractResponse200Data(BaseModel):
     """
     Attributes:
-        data (JumpGate):
+        agent (Agent):
+        contract (Contract):
     """
 
-    data: "JumpGate" = Field(alias="data")
+    agent: "Agent" = Field(alias="agent")
+    contract: "Contract" = Field(alias="contract")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_market_response_200.py` & `spacetraders-0.2.3/spacetraders/models/register_response_201.py`

 * *Files 17% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.market import Market
+from ..models.register_response_201_data import RegisterResponse201Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetMarketResponse200")
+T = TypeVar("T", bound="RegisterResponse201")
 
 
-class GetMarketResponse200(BaseModel):
+class RegisterResponse201(BaseModel):
     """
     Attributes:
-        data (Market):
+        data (RegisterResponse201Data):
     """
 
-    data: "Market" = Field(alias="data")
+    data: "RegisterResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_my_ship_cargo_response_200.py` & `spacetraders-0.2.3/spacetraders/models/shipyard_ship_types_item.py`

 * *Files 18% similar despite different names*

```diff
@@ -5,39 +5,43 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
+    Union,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_cargo import ShipCargo
+from ..models.ship_type import ShipType
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetMyShipCargoResponse200")
+T = TypeVar("T", bound="ShipyardShipTypesItem")
 
 
-class GetMyShipCargoResponse200(BaseModel):
+class ShipyardShipTypesItem(BaseModel):
     """
     Attributes:
-        data (ShipCargo):
+        type (Union[Unset, ShipType]):
     """
 
-    data: "ShipCargo" = Field(alias="data")
+    type: Union[Unset, ShipType] = Field(UNSET, alias="type")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_my_ship_response_200.py` & `spacetraders-0.2.3/spacetraders/models/get_my_agent_response_200.py`

 * *Files 20% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship import Ship
+from ..models.agent import Agent
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetMyShipResponse200")
+T = TypeVar("T", bound="GetMyAgentResponse200")
 
 
-class GetMyShipResponse200(BaseModel):
+class GetMyAgentResponse200(BaseModel):
     """
     Attributes:
-        data (Ship): A ship
+        data (Agent):
     """
 
-    data: "Ship" = Field(alias="data")
+    data: "Agent" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_my_ships_response_200.py` & `spacetraders-0.2.3/spacetraders/models/survey_deposit.py`

 * *Files 26% similar despite different names*

```diff
@@ -5,42 +5,42 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.meta import Meta
-from ..models.ship import Ship
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetMyShipsResponse200")
+T = TypeVar("T", bound="SurveyDeposit")
 
 
-class GetMyShipsResponse200(BaseModel):
-    """
+class SurveyDeposit(BaseModel):
+    """A surveyed deposit of a mineral or resource available for extraction.
+
     Attributes:
-        data (List['Ship']):
-        meta (Meta):
+        symbol (str): The symbol of the deposit.
     """
 
-    data: List["Ship"] = Field(alias="data")
-    meta: "Meta" = Field(alias="meta")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_ship_cooldown_response_200.py` & `spacetraders-0.2.3/spacetraders/models/warp_ship_response_200.py`

 * *Files 11% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.cooldown import Cooldown
+from ..models.warp_ship_response_200_data import WarpShipResponse200Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetShipCooldownResponse200")
+T = TypeVar("T", bound="WarpShipResponse200")
 
 
-class GetShipCooldownResponse200(BaseModel):
+class WarpShipResponse200(BaseModel):
     """
     Attributes:
-        data (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
+        data (WarpShipResponse200Data):
     """
 
-    data: "Cooldown" = Field(alias="data")
+    data: "WarpShipResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_ship_nav_response_200.py` & `spacetraders-0.2.3/spacetraders/models/get_system_response_200.py`

 * *Files 14% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_nav import ShipNav
+from ..models.system import System
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetShipNavResponse200")
+T = TypeVar("T", bound="GetSystemResponse200")
 
 
-class GetShipNavResponse200(BaseModel):
+class GetSystemResponse200(BaseModel):
     """
     Attributes:
-        data (ShipNav): The navigation information of the ship.
+        data (System):
     """
 
-    data: "ShipNav" = Field(alias="data")
+    data: "System" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_system_response_200.py` & `spacetraders-0.2.3/spacetraders/models/waypoint_orbital.py`

 * *Files 20% similar despite different names*

```diff
@@ -5,39 +5,42 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.system import System
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetSystemResponse200")
+T = TypeVar("T", bound="WaypointOrbital")
 
 
-class GetSystemResponse200(BaseModel):
-    """
+class WaypointOrbital(BaseModel):
+    """An orbital is another waypoint that orbits a parent waypoint.
+
     Attributes:
-        data (System):
+        symbol (str):
     """
 
-    data: "System" = Field(alias="data")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_system_waypoints_response_200.py` & `spacetraders-0.2.3/spacetraders/models/get_system_waypoints_response_200.py`

 * *Files 9% similar despite different names*

```diff
@@ -33,14 +33,18 @@
     meta: "Meta" = Field(alias="meta")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_systems_response_200.py` & `spacetraders-0.2.3/spacetraders/models/meta.py`

 * *Files 14% similar despite different names*

```diff
@@ -5,42 +5,45 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.meta import Meta
-from ..models.system import System
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetSystemsResponse200")
+T = TypeVar("T", bound="Meta")
 
 
-class GetSystemsResponse200(BaseModel):
+class Meta(BaseModel):
     """
     Attributes:
-        data (List['System']):
-        meta (Meta):
+        total (int):
+        page (int):
+        limit (int):
     """
 
-    data: List["System"] = Field(alias="data")
-    meta: "Meta" = Field(alias="meta")
+    total: int = Field(alias="total")
+    page: int = Field(alias="page")
+    limit: int = Field(alias="limit")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/get_waypoint_response_200.py` & `spacetraders-0.2.3/spacetraders/models/get_factions_response_200.py`

 * *Files 13% similar despite different names*

```diff
@@ -11,33 +11,40 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.waypoint import Waypoint
+from ..models.faction import Faction
+from ..models.meta import Meta
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="GetWaypointResponse200")
+T = TypeVar("T", bound="GetFactionsResponse200")
 
 
-class GetWaypointResponse200(BaseModel):
+class GetFactionsResponse200(BaseModel):
     """
     Attributes:
-        data (Waypoint): A waypoint is a location that ships can travel to such as a Planet, Moon or Space Station.
+        data (List['Faction']):
+        meta (Meta):
     """
 
-    data: "Waypoint" = Field(alias="data")
+    data: List["Faction"] = Field(alias="data")
+    meta: "Meta" = Field(alias="meta")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/jettison_json_body.py` & `spacetraders-0.2.3/spacetraders/models/jettison_json_body.py`

 * *Files 15% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/jettison_response_200_data.py` & `spacetraders-0.2.3/spacetraders/models/sell_cargo_sell_cargo_request.py`

 * *Files 20% similar despite different names*

```diff
@@ -5,39 +5,43 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_cargo import ShipCargo
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="JettisonResponse200Data")
+T = TypeVar("T", bound="SellCargoSellCargoRequest")
 
 
-class JettisonResponse200Data(BaseModel):
+class SellCargoSellCargoRequest(BaseModel):
     """
     Attributes:
-        cargo (ShipCargo):
+        symbol (str):
+        units (int):
     """
 
-    cargo: "ShipCargo" = Field(alias="cargo")
+    symbol: str = Field(alias="symbol")
+    units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/jump_gate.py` & `spacetraders-0.2.3/spacetraders/models/jump_gate.py`

 * *Files 12% similar despite different names*

```diff
@@ -29,21 +29,25 @@
         connected_systems (List['ConnectedSystem']): The systems within range of the gate that have a corresponding
             gate.
         faction_symbol (Union[Unset, str]): The symbol of the faction that owns the gate.
     """
 
     jump_range: float = Field(alias="jumpRange")
     connected_systems: List["ConnectedSystem"] = Field(alias="connectedSystems")
-    faction_symbol: Union[Unset, str] = UNSET
+    faction_symbol: Union[Unset, str] = Field(UNSET, alias="factionSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/jump_ship_json_body.py` & `spacetraders-0.2.3/spacetraders/models/purchase_cargo_purchase_cargo_request.py`

 * *Files 21% similar despite different names*

```diff
@@ -12,30 +12,36 @@
 )
 
 import attr
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="JumpShipJsonBody")
+T = TypeVar("T", bound="PurchaseCargoPurchaseCargoRequest")
 
 
-class JumpShipJsonBody(BaseModel):
+class PurchaseCargoPurchaseCargoRequest(BaseModel):
     """
     Attributes:
-        system_symbol (str): The system symbol to jump to.
+        symbol (str):
+        units (int):
     """
 
-    system_symbol: str = Field(alias="systemSymbol")
+    symbol: str = Field(alias="symbol")
+    units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/jump_ship_response_200.py` & `spacetraders-0.2.3/spacetraders/models/jump_ship_response_200.py`

 * *Files 11% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     data: "JumpShipResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/jump_ship_response_200_data.py` & `spacetraders-0.2.3/spacetraders/models/jump_ship_response_200_data.py`

 * *Files 11% similar despite different names*

```diff
@@ -27,21 +27,25 @@
     """
     Attributes:
         cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
         nav (Union[Unset, ShipNav]): The navigation information of the ship.
     """
 
     cooldown: "Cooldown" = Field(alias="cooldown")
-    nav: Union[Unset, "ShipNav"] = UNSET
+    nav: Union[Unset, "ShipNav"] = Field(UNSET, alias="nav")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/market.py` & `spacetraders-0.2.3/spacetraders/models/market.py`

 * *Files 7% similar despite different names*

```diff
@@ -37,22 +37,30 @@
             only when a ship is present at the market.
     """
 
     symbol: str = Field(alias="symbol")
     exports: List["TradeGood"] = Field(alias="exports")
     imports: List["TradeGood"] = Field(alias="imports")
     exchange: List["TradeGood"] = Field(alias="exchange")
-    transactions: Union[Unset, List["MarketTransaction"]] = UNSET
-    trade_goods: Union[Unset, List["MarketTradeGood"]] = UNSET
+    transactions: Union[Unset, List["MarketTransaction"]] = Field(
+        UNSET, alias="transactions"
+    )
+    trade_goods: Union[Unset, List["MarketTradeGood"]] = Field(
+        UNSET, alias="tradeGoods"
+    )
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/market_trade_good.py` & `spacetraders-0.2.3/spacetraders/models/market_trade_good.py`

 * *Files 14% similar despite different names*

```diff
@@ -38,14 +38,18 @@
     sell_price: int = Field(alias="sellPrice")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/market_transaction.py` & `spacetraders-0.2.3/spacetraders/models/market_transaction.py`

 * *Files 9% similar despite different names*

```diff
@@ -46,14 +46,18 @@
     timestamp: datetime.datetime = Field(alias="timestamp")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/meta.py` & `spacetraders-0.2.3/spacetraders/models/scanned_ship_mounts_item.py`

 * *Files 22% similar despite different names*

```diff
@@ -12,34 +12,35 @@
 )
 
 import attr
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="Meta")
+T = TypeVar("T", bound="ScannedShipMountsItem")
 
 
-class Meta(BaseModel):
-    """
+class ScannedShipMountsItem(BaseModel):
+    """A mount on the ship.
+
     Attributes:
-        total (int):
-        page (int):
-        limit (int):
+        symbol (str):
     """
 
-    total: int = Field(alias="total")
-    page: int = Field(alias="page")
-    limit: int = Field(alias="limit")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/navigate_ship_json_body.py` & `spacetraders-0.2.3/spacetraders/models/register_response_201_data.py`

 * *Files 23% similar despite different names*

```diff
@@ -5,37 +5,54 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
+from ..models.agent import Agent
+from ..models.contract import Contract
+from ..models.faction import Faction
+from ..models.ship import Ship
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="NavigateShipJsonBody")
+T = TypeVar("T", bound="RegisterResponse201Data")
 
 
-class NavigateShipJsonBody(BaseModel):
+class RegisterResponse201Data(BaseModel):
     """
     Attributes:
-        waypoint_symbol (str): The target destination.
+        agent (Agent):
+        contract (Contract):
+        faction (Faction):
+        ship (Ship): A ship
+        token (str): A Bearer token for accessing secured API endpoints.
     """
 
-    waypoint_symbol: str = Field(alias="waypointSymbol")
+    agent: "Agent" = Field(alias="agent")
+    contract: "Contract" = Field(alias="contract")
+    faction: "Faction" = Field(alias="faction")
+    ship: "Ship" = Field(alias="ship")
+    token: str = Field(alias="token")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/navigate_ship_response_200.py` & `spacetraders-0.2.3/spacetraders/models/refuel_ship_response_200.py`

 * *Files 11% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.navigate_ship_response_200_data import NavigateShipResponse200Data
+from ..models.refuel_ship_response_200_data import RefuelShipResponse200Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="NavigateShipResponse200")
+T = TypeVar("T", bound="RefuelShipResponse200")
 
 
-class NavigateShipResponse200(BaseModel):
+class RefuelShipResponse200(BaseModel):
     """
     Attributes:
-        data (NavigateShipResponse200Data):
+        data (RefuelShipResponse200Data):
     """
 
-    data: "NavigateShipResponse200Data" = Field(alias="data")
+    data: "RefuelShipResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/navigate_ship_response_200_data.py` & `spacetraders-0.2.3/spacetraders/models/jettison_response_200_data.py`

 * *Files 11% similar despite different names*

```diff
@@ -11,37 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_fuel import ShipFuel
-from ..models.ship_nav import ShipNav
+from ..models.ship_cargo import ShipCargo
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="NavigateShipResponse200Data")
+T = TypeVar("T", bound="JettisonResponse200Data")
 
 
-class NavigateShipResponse200Data(BaseModel):
+class JettisonResponse200Data(BaseModel):
     """
     Attributes:
-        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
-            or action.
-        nav (ShipNav): The navigation information of the ship.
+        cargo (ShipCargo):
     """
 
-    fuel: "ShipFuel" = Field(alias="fuel")
-    nav: "ShipNav" = Field(alias="nav")
+    cargo: "ShipCargo" = Field(alias="cargo")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/orbit_ship_orbit_ship_200_response.py` & `spacetraders-0.2.3/spacetraders/models/orbit_ship_orbit_ship_200_response.py`

 * *Files 23% similar despite different names*

```diff
@@ -32,14 +32,18 @@
     data: "OrbitShipOrbitShip200ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/orbit_ship_orbit_ship_200_response_data.py` & `spacetraders-0.2.3/spacetraders/models/orbit_ship_orbit_ship_200_response_data.py`

 * *Files 7% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     nav: "ShipNav" = Field(alias="nav")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/patch_ship_nav_json_body.py` & `spacetraders-0.2.3/spacetraders/models/ship_refine_json_body.py`

 * *Files 18% similar despite different names*

```diff
@@ -5,40 +5,42 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_nav_flight_mode import ShipNavFlightMode
+from ..models.ship_refine_json_body_produce import ShipRefineJsonBodyProduce
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="PatchShipNavJsonBody")
+T = TypeVar("T", bound="ShipRefineJsonBody")
 
 
-class PatchShipNavJsonBody(BaseModel):
+class ShipRefineJsonBody(BaseModel):
     """
     Attributes:
-        flight_mode (Union[Unset, ShipNavFlightMode]): The ship's set speed when traveling between waypoints or systems.
-            Default: ShipNavFlightMode.CRUISE.
+        produce (ShipRefineJsonBodyProduce):
     """
 
-    flight_mode: Union[Unset, ShipNavFlightMode] = ShipNavFlightMode.CRUISE
+    produce: ShipRefineJsonBodyProduce = Field(alias="produce")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/patch_ship_nav_response_200.py` & `spacetraders-0.2.3/spacetraders/models/get_ship_nav_response_200.py`

 * *Files 9% similar despite different names*

```diff
@@ -14,30 +14,34 @@
 
 import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_nav import ShipNav
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="PatchShipNavResponse200")
+T = TypeVar("T", bound="GetShipNavResponse200")
 
 
-class PatchShipNavResponse200(BaseModel):
+class GetShipNavResponse200(BaseModel):
     """
     Attributes:
         data (ShipNav): The navigation information of the ship.
     """
 
     data: "ShipNav" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/purchase_cargo_purchase_cargo_201_response.py` & `spacetraders-0.2.3/spacetraders/models/purchase_cargo_purchase_cargo_201_response.py`

 * *Files 11% similar despite different names*

```diff
@@ -32,14 +32,18 @@
     data: "PurchaseCargoPurchaseCargo201ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/purchase_cargo_purchase_cargo_201_response_data.py` & `spacetraders-0.2.3/spacetraders/models/sell_cargo_sell_cargo_201_response_data.py`

 * *Files 9% similar despite different names*

```diff
@@ -16,18 +16,18 @@
 from pydantic import BaseModel, Field
 
 from ..models.agent import Agent
 from ..models.market_transaction import MarketTransaction
 from ..models.ship_cargo import ShipCargo
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="PurchaseCargoPurchaseCargo201ResponseData")
+T = TypeVar("T", bound="SellCargoSellCargo201ResponseData")
 
 
-class PurchaseCargoPurchaseCargo201ResponseData(BaseModel):
+class SellCargoSellCargo201ResponseData(BaseModel):
     """
     Attributes:
         agent (Agent):
         cargo (ShipCargo):
         transaction (MarketTransaction):
     """
 
@@ -36,14 +36,18 @@
     transaction: "MarketTransaction" = Field(alias="transaction")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/purchase_cargo_purchase_cargo_request.py` & `spacetraders-0.2.3/spacetraders/models/register_json_body.py`

 * *Files 27% similar despite different names*

```diff
@@ -10,34 +10,39 @@
     Type,
     TypeVar,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
+from ..models.register_json_body_faction import RegisterJsonBodyFaction
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="PurchaseCargoPurchaseCargoRequest")
+T = TypeVar("T", bound="RegisterJsonBody")
 
 
-class PurchaseCargoPurchaseCargoRequest(BaseModel):
+class RegisterJsonBody(BaseModel):
     """
     Attributes:
-        symbol (str):
-        units (int):
+        faction (RegisterJsonBodyFaction): The faction you choose determines your headquarters.
+        symbol (str): How other agents will see your ships and information. Example: BADGER.
     """
 
+    faction: RegisterJsonBodyFaction = Field(alias="faction")
     symbol: str = Field(alias="symbol")
-    units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/purchase_ship_json_body.py` & `spacetraders-0.2.3/spacetraders/models/purchase_ship_json_body.py`

 * *Files 10% similar despite different names*

```diff
@@ -31,14 +31,18 @@
     waypoint_symbol: str = Field(alias="waypointSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/purchase_ship_response_201.py` & `spacetraders-0.2.3/spacetraders/models/purchase_ship_response_201.py`

 * *Files 17% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     data: "PurchaseShipResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/purchase_ship_response_201_data.py` & `spacetraders-0.2.3/spacetraders/models/scanned_ship_reactor.py`

 * *Files 22% similar despite different names*

```diff
@@ -5,45 +5,42 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..models.ship import Ship
-from ..models.shipyard_transaction import ShipyardTransaction
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="PurchaseShipResponse201Data")
+T = TypeVar("T", bound="ScannedShipReactor")
 
 
-class PurchaseShipResponse201Data(BaseModel):
-    """
+class ScannedShipReactor(BaseModel):
+    """The reactor of the ship.
+
     Attributes:
-        agent (Agent):
-        ship (Ship): A ship
-        transaction (ShipyardTransaction):
+        symbol (str):
     """
 
-    agent: "Agent" = Field(alias="agent")
-    ship: "Ship" = Field(alias="ship")
-    transaction: "ShipyardTransaction" = Field(alias="transaction")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/refuel_ship_response_200.py` & `spacetraders-0.2.3/spacetraders/models/extract_resources_response_201.py`

 * *Files 22% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.refuel_ship_response_200_data import RefuelShipResponse200Data
+from ..models.extract_resources_response_201_data import ExtractResourcesResponse201Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="RefuelShipResponse200")
+T = TypeVar("T", bound="ExtractResourcesResponse201")
 
 
-class RefuelShipResponse200(BaseModel):
+class ExtractResourcesResponse201(BaseModel):
     """
     Attributes:
-        data (RefuelShipResponse200Data):
+        data (ExtractResourcesResponse201Data):
     """
 
-    data: "RefuelShipResponse200Data" = Field(alias="data")
+    data: "ExtractResourcesResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/refuel_ship_response_200_data.py` & `spacetraders-0.2.3/spacetraders/models/transfer_cargo_transfer_cargo_request.py`

 * *Files 13% similar despite different names*

```diff
@@ -5,43 +5,45 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..models.ship_fuel import ShipFuel
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="RefuelShipResponse200Data")
+T = TypeVar("T", bound="TransferCargoTransferCargoRequest")
 
 
-class RefuelShipResponse200Data(BaseModel):
+class TransferCargoTransferCargoRequest(BaseModel):
     """
     Attributes:
-        agent (Agent):
-        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
-            or action.
+        trade_symbol (str):
+        units (int):
+        ship_symbol (str):
     """
 
-    agent: "Agent" = Field(alias="agent")
-    fuel: "ShipFuel" = Field(alias="fuel")
+    trade_symbol: str = Field(alias="tradeSymbol")
+    units: int = Field(alias="units")
+    ship_symbol: str = Field(alias="shipSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/register_json_body.py` & `spacetraders-0.2.3/spacetraders/models/trade_good.py`

 * *Files 18% similar despite different names*

```diff
@@ -10,35 +10,41 @@
     Type,
     TypeVar,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.register_json_body_faction import RegisterJsonBodyFaction
+from ..models.trade_symbol import TradeSymbol
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="RegisterJsonBody")
+T = TypeVar("T", bound="TradeGood")
 
 
-class RegisterJsonBody(BaseModel):
+class TradeGood(BaseModel):
     """
     Attributes:
-        faction (RegisterJsonBodyFaction): The faction you choose determines your headquarters.
-        symbol (str): How other agents will see your ships and information. Example: BADGER.
+        symbol (TradeSymbol):
+        name (str):
+        description (str):
     """
 
-    faction: RegisterJsonBodyFaction = Field(alias="faction")
-    symbol: str = Field(alias="symbol")
+    symbol: TradeSymbol = Field(alias="symbol")
+    name: str = Field(alias="name")
+    description: str = Field(alias="description")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/register_response_201_data.py` & `spacetraders-0.2.3/spacetraders/models/ship_frame.py`

 * *Files 21% similar despite different names*

```diff
@@ -5,50 +5,63 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    Union,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..models.contract import Contract
-from ..models.faction import Faction
-from ..models.ship import Ship
+from ..models.ship_frame_symbol import ShipFrameSymbol
+from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="RegisterResponse201Data")
+T = TypeVar("T", bound="ShipFrame")
 
 
-class RegisterResponse201Data(BaseModel):
-    """
-    Attributes:
-        agent (Agent):
-        contract (Contract):
-        faction (Faction):
-        ship (Ship): A ship
-        token (str): A Bearer token for accessing secured API endpoints.
+class ShipFrame(BaseModel):
+    """The frame of the ship. The frame determines the number of modules and mounting points of the ship, as well as base
+    fuel capacity. As the condition of the frame takes more wear, the ship will become more sluggish and less
+    maneuverable.
+
+        Attributes:
+            symbol (ShipFrameSymbol):
+            name (str):
+            description (str):
+            module_slots (int):
+            mounting_points (int):
+            fuel_capacity (int):
+            requirements (ShipRequirements): The requirements for installation on a ship
+            condition (Union[Unset, int]): Condition is a range of 0 to 100 where 0 is completely worn out and 100 is brand
+                new.
     """
 
-    agent: "Agent" = Field(alias="agent")
-    contract: "Contract" = Field(alias="contract")
-    faction: "Faction" = Field(alias="faction")
-    ship: "Ship" = Field(alias="ship")
-    token: str = Field(alias="token")
+    symbol: ShipFrameSymbol = Field(alias="symbol")
+    name: str = Field(alias="name")
+    description: str = Field(alias="description")
+    module_slots: int = Field(alias="moduleSlots")
+    mounting_points: int = Field(alias="mountingPoints")
+    fuel_capacity: int = Field(alias="fuelCapacity")
+    requirements: "ShipRequirements" = Field(alias="requirements")
+    condition: Union[Unset, int] = Field(UNSET, alias="condition")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/scanned_ship.py` & `spacetraders-0.2.3/spacetraders/models/scanned_ship.py`

 * *Files 6% similar despite different names*

```diff
@@ -40,23 +40,27 @@
         mounts (Union[Unset, List['ScannedShipMountsItem']]):
     """
 
     symbol: str = Field(alias="symbol")
     registration: "ShipRegistration" = Field(alias="registration")
     nav: "ShipNav" = Field(alias="nav")
     engine: "ScannedShipEngine" = Field(alias="engine")
-    frame: Union[Unset, "ScannedShipFrame"] = UNSET
-    reactor: Union[Unset, "ScannedShipReactor"] = UNSET
-    mounts: Union[Unset, List["ScannedShipMountsItem"]] = UNSET
+    frame: Union[Unset, "ScannedShipFrame"] = Field(UNSET, alias="frame")
+    reactor: Union[Unset, "ScannedShipReactor"] = Field(UNSET, alias="reactor")
+    mounts: Union[Unset, List["ScannedShipMountsItem"]] = Field(UNSET, alias="mounts")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/scanned_ship_mounts_item.py` & `spacetraders-0.2.3/spacetraders/models/deliver_contract_response_200_data.py`

 * *Files 25% similar despite different names*

```diff
@@ -5,38 +5,46 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
+from ..models.contract import Contract
+from ..models.ship_cargo import ShipCargo
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ScannedShipMountsItem")
+T = TypeVar("T", bound="DeliverContractResponse200Data")
 
 
-class ScannedShipMountsItem(BaseModel):
-    """A mount on the ship.
-
+class DeliverContractResponse200Data(BaseModel):
+    """
     Attributes:
-        symbol (str):
+        contract (Contract):
+        cargo (ShipCargo):
     """
 
-    symbol: str = Field(alias="symbol")
+    contract: "Contract" = Field(alias="contract")
+    cargo: "ShipCargo" = Field(alias="cargo")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/scanned_ship_reactor.py` & `spacetraders-0.2.3/spacetraders/models/dock_ship_dock_ship_200_response_data.py`

 * *Files 25% similar despite different names*

```diff
@@ -5,38 +5,43 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
+from ..models.ship_nav import ShipNav
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ScannedShipReactor")
+T = TypeVar("T", bound="DockShipDockShip200ResponseData")
 
 
-class ScannedShipReactor(BaseModel):
-    """The reactor of the ship.
-
+class DockShipDockShip200ResponseData(BaseModel):
+    """
     Attributes:
-        symbol (str):
+        nav (ShipNav): The navigation information of the ship.
     """
 
-    symbol: str = Field(alias="symbol")
+    nav: "ShipNav" = Field(alias="nav")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/scanned_system.py` & `spacetraders-0.2.3/spacetraders/models/scanned_system.py`

 * *Files 10% similar despite different names*

```diff
@@ -39,14 +39,18 @@
     distance: int = Field(alias="distance")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/scanned_waypoint.py` & `spacetraders-0.2.3/spacetraders/models/scanned_waypoint.py`

 * *Files 10% similar despite different names*

```diff
@@ -45,22 +45,26 @@
     symbol: str = Field(alias="symbol")
     type: WaypointType = Field(alias="type")
     system_symbol: str = Field(alias="systemSymbol")
     x: int = Field(alias="x")
     y: int = Field(alias="y")
     orbitals: List["WaypointOrbital"] = Field(alias="orbitals")
     traits: List["WaypointTrait"] = Field(alias="traits")
-    faction: Union[Unset, "WaypointFaction"] = UNSET
-    chart: Union[Unset, "Chart"] = UNSET
+    faction: Union[Unset, "WaypointFaction"] = Field(UNSET, alias="faction")
+    chart: Union[Unset, "Chart"] = Field(UNSET, alias="chart")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/sell_cargo_sell_cargo_201_response_data.py` & `spacetraders-0.2.3/spacetraders/models/transfer_cargo_transfer_cargo_200_response.py`

 * *Files 20% similar despite different names*

```diff
@@ -11,39 +11,39 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..models.market_transaction import MarketTransaction
-from ..models.ship_cargo import ShipCargo
+from ..models.transfer_cargo_transfer_cargo_200_response_data import (
+    TransferCargoTransferCargo200ResponseData,
+)
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="SellCargoSellCargo201ResponseData")
+T = TypeVar("T", bound="TransferCargoTransferCargo200Response")
 
 
-class SellCargoSellCargo201ResponseData(BaseModel):
+class TransferCargoTransferCargo200Response(BaseModel):
     """
     Attributes:
-        agent (Agent):
-        cargo (ShipCargo):
-        transaction (MarketTransaction):
+        data (TransferCargoTransferCargo200ResponseData):
     """
 
-    agent: "Agent" = Field(alias="agent")
-    cargo: "ShipCargo" = Field(alias="cargo")
-    transaction: "MarketTransaction" = Field(alias="transaction")
+    data: "TransferCargoTransferCargo200ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship.py` & `spacetraders-0.2.3/spacetraders/models/ship.py`

 * *Files 4% similar despite different names*

```diff
@@ -64,14 +64,18 @@
     fuel: "ShipFuel" = Field(alias="fuel")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_cargo.py` & `spacetraders-0.2.3/spacetraders/models/ship_cargo.py`

 * *Files 16% similar despite different names*

```diff
@@ -34,14 +34,18 @@
     inventory: List["ShipCargoItem"] = Field(alias="inventory")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_cargo_item.py` & `spacetraders-0.2.3/spacetraders/models/ship_cargo_item.py`

 * *Files 14% similar despite different names*

```diff
@@ -35,14 +35,18 @@
     units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_crew.py` & `spacetraders-0.2.3/spacetraders/models/ship_crew.py`

 * *Files 4% similar despite different names*

```diff
@@ -36,21 +36,25 @@
     """
 
     current: int = Field(alias="current")
     required: int = Field(alias="required")
     capacity: int = Field(alias="capacity")
     morale: int = Field(alias="morale")
     wages: int = Field(alias="wages")
-    rotation: ShipCrewRotation = ShipCrewRotation.STRICT
+    rotation: ShipCrewRotation = Field(ShipCrewRotation.STRICT, alias="rotation")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_engine.py` & `spacetraders-0.2.3/spacetraders/models/warp_ship_response_200_data.py`

 * *Files 20% similar despite different names*

```diff
@@ -5,53 +5,47 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_engine_symbol import ShipEngineSymbol
-from ..models.ship_requirements import ShipRequirements
+from ..models.ship_fuel import ShipFuel
+from ..models.ship_nav import ShipNav
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipEngine")
+T = TypeVar("T", bound="WarpShipResponse200Data")
 
 
-class ShipEngine(BaseModel):
-    """The engine determines how quickly a ship travels between waypoints.
-
+class WarpShipResponse200Data(BaseModel):
+    """
     Attributes:
-        symbol (ShipEngineSymbol):
-        name (str):
-        description (str):
-        speed (float):
-        requirements (ShipRequirements): The requirements for installation on a ship
-        condition (Union[Unset, int]): Condition is a range of 0 to 100 where 0 is completely worn out and 100 is brand
-            new.
+        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
+            or action.
+        nav (ShipNav): The navigation information of the ship.
     """
 
-    symbol: ShipEngineSymbol = Field(alias="symbol")
-    name: str = Field(alias="name")
-    description: str = Field(alias="description")
-    speed: float = Field(alias="speed")
-    requirements: "ShipRequirements" = Field(alias="requirements")
-    condition: Union[Unset, int] = UNSET
+    fuel: "ShipFuel" = Field(alias="fuel")
+    nav: "ShipNav" = Field(alias="nav")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_frame.py` & `spacetraders-0.2.3/spacetraders/models/shipyard_ship.py`

 * *Files 16% similar despite different names*

```diff
@@ -12,52 +12,61 @@
     Union,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_frame_symbol import ShipFrameSymbol
-from ..models.ship_requirements import ShipRequirements
+from ..models.ship_engine import ShipEngine
+from ..models.ship_frame import ShipFrame
+from ..models.ship_module import ShipModule
+from ..models.ship_mount import ShipMount
+from ..models.ship_reactor import ShipReactor
+from ..models.ship_type import ShipType
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipFrame")
+T = TypeVar("T", bound="ShipyardShip")
 
 
-class ShipFrame(BaseModel):
-    """The frame of the ship. The frame determines the number of modules and mounting points of the ship, as well as base
-    fuel capacity. As the condition of the frame takes more wear, the ship will become more sluggish and less
-    maneuverable.
-
-        Attributes:
-            symbol (ShipFrameSymbol):
-            name (str):
-            description (str):
-            module_slots (int):
-            mounting_points (int):
-            fuel_capacity (int):
-            requirements (ShipRequirements): The requirements for installation on a ship
-            condition (Union[Unset, int]): Condition is a range of 0 to 100 where 0 is completely worn out and 100 is brand
-                new.
+class ShipyardShip(BaseModel):
+    """
+    Attributes:
+        name (str):
+        description (str):
+        purchase_price (int):
+        frame (ShipFrame): The frame of the ship. The frame determines the number of modules and mounting points of the
+            ship, as well as base fuel capacity. As the condition of the frame takes more wear, the ship will become more
+            sluggish and less maneuverable.
+        reactor (ShipReactor): The reactor of the ship. The reactor is responsible for powering the ship's systems and
+            weapons.
+        engine (ShipEngine): The engine determines how quickly a ship travels between waypoints.
+        modules (List['ShipModule']):
+        mounts (List['ShipMount']):
+        type (Union[Unset, ShipType]):
     """
 
-    symbol: ShipFrameSymbol = Field(alias="symbol")
     name: str = Field(alias="name")
     description: str = Field(alias="description")
-    module_slots: int = Field(alias="moduleSlots")
-    mounting_points: int = Field(alias="mountingPoints")
-    fuel_capacity: int = Field(alias="fuelCapacity")
-    requirements: "ShipRequirements" = Field(alias="requirements")
-    condition: Union[Unset, int] = UNSET
+    purchase_price: int = Field(alias="purchasePrice")
+    frame: "ShipFrame" = Field(alias="frame")
+    reactor: "ShipReactor" = Field(alias="reactor")
+    engine: "ShipEngine" = Field(alias="engine")
+    modules: List["ShipModule"] = Field(alias="modules")
+    mounts: List["ShipMount"] = Field(alias="mounts")
+    type: Union[Unset, ShipType] = Field(UNSET, alias="type")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_frame_symbol.py` & `spacetraders-0.2.3/spacetraders/models/ship_frame_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_fuel.py` & `spacetraders-0.2.3/spacetraders/models/ship_fuel.py`

 * *Files 6% similar despite different names*

```diff
@@ -29,21 +29,25 @@
         current (int): The current amount of fuel in the ship's tanks.
         capacity (int): The maximum amount of fuel the ship's tanks can hold.
         consumed (Union[Unset, ShipFuelConsumed]):
     """
 
     current: int = Field(alias="current")
     capacity: int = Field(alias="capacity")
-    consumed: Union[Unset, "ShipFuelConsumed"] = UNSET
+    consumed: Union[Unset, "ShipFuelConsumed"] = Field(UNSET, alias="consumed")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_module.py` & `spacetraders-0.2.3/spacetraders/models/ship_mount.py`

 * *Files 12% similar despite different names*

```diff
@@ -12,46 +12,50 @@
     Union,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_module_symbol import ShipModuleSymbol
+from ..models.ship_mount_deposits_item import ShipMountDepositsItem
+from ..models.ship_mount_symbol import ShipMountSymbol
 from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipModule")
+T = TypeVar("T", bound="ShipMount")
 
 
-class ShipModule(BaseModel):
-    """A module can be installed in a ship and provides a set of capabilities such as storage space or quarters for crew.
-    Module installations are permanent.
-
-        Attributes:
-            symbol (ShipModuleSymbol):
-            name (str):
-            requirements (ShipRequirements): The requirements for installation on a ship
-            capacity (Union[Unset, int]):
-            range_ (Union[Unset, int]):
-            description (Union[Unset, str]):
+class ShipMount(BaseModel):
+    """A mount is installed on the exterier of a ship.
+
+    Attributes:
+        symbol (ShipMountSymbol):
+        name (str):
+        requirements (ShipRequirements): The requirements for installation on a ship
+        description (Union[Unset, str]):
+        strength (Union[Unset, int]):
+        deposits (Union[Unset, List[ShipMountDepositsItem]]):
     """
 
-    symbol: ShipModuleSymbol = Field(alias="symbol")
+    symbol: ShipMountSymbol = Field(alias="symbol")
     name: str = Field(alias="name")
     requirements: "ShipRequirements" = Field(alias="requirements")
-    capacity: Union[Unset, int] = UNSET
-    range_: Union[Unset, int] = UNSET
-    description: Union[Unset, str] = UNSET
+    description: Union[Unset, str] = Field(UNSET, alias="description")
+    strength: Union[Unset, int] = Field(UNSET, alias="strength")
+    deposits: Union[Unset, List[ShipMountDepositsItem]] = Field(UNSET, alias="deposits")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_module_symbol.py` & `spacetraders-0.2.3/spacetraders/models/ship_module_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_mount.py` & `spacetraders-0.2.3/spacetraders/models/ship_module.py`

 * *Files 24% similar despite different names*

```diff
@@ -12,46 +12,50 @@
     Union,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_mount_deposits_item import ShipMountDepositsItem
-from ..models.ship_mount_symbol import ShipMountSymbol
+from ..models.ship_module_symbol import ShipModuleSymbol
 from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipMount")
+T = TypeVar("T", bound="ShipModule")
 
 
-class ShipMount(BaseModel):
-    """A mount is installed on the exterier of a ship.
-
-    Attributes:
-        symbol (ShipMountSymbol):
-        name (str):
-        requirements (ShipRequirements): The requirements for installation on a ship
-        description (Union[Unset, str]):
-        strength (Union[Unset, int]):
-        deposits (Union[Unset, List[ShipMountDepositsItem]]):
+class ShipModule(BaseModel):
+    """A module can be installed in a ship and provides a set of capabilities such as storage space or quarters for crew.
+    Module installations are permanent.
+
+        Attributes:
+            symbol (ShipModuleSymbol):
+            name (str):
+            requirements (ShipRequirements): The requirements for installation on a ship
+            capacity (Union[Unset, int]):
+            range_ (Union[Unset, int]):
+            description (Union[Unset, str]):
     """
 
-    symbol: ShipMountSymbol = Field(alias="symbol")
+    symbol: ShipModuleSymbol = Field(alias="symbol")
     name: str = Field(alias="name")
     requirements: "ShipRequirements" = Field(alias="requirements")
-    description: Union[Unset, str] = UNSET
-    strength: Union[Unset, int] = UNSET
-    deposits: Union[Unset, List[ShipMountDepositsItem]] = UNSET
+    capacity: Union[Unset, int] = Field(UNSET, alias="capacity")
+    range_: Union[Unset, int] = Field(UNSET, alias="range")
+    description: Union[Unset, str] = Field(UNSET, alias="description")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_mount_deposits_item.py` & `spacetraders-0.2.3/spacetraders/models/ship_mount_deposits_item.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_mount_symbol.py` & `spacetraders-0.2.3/spacetraders/models/ship_mount_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_nav.py` & `spacetraders-0.2.3/spacetraders/models/ship_nav.py`

 * *Files 4% similar despite different names*

```diff
@@ -36,21 +36,25 @@
             ShipNavFlightMode.CRUISE.
     """
 
     system_symbol: str = Field(alias="systemSymbol")
     waypoint_symbol: str = Field(alias="waypointSymbol")
     route: "ShipNavRoute" = Field(alias="route")
     status: ShipNavStatus = Field(alias="status")
-    flight_mode: ShipNavFlightMode = ShipNavFlightMode.CRUISE
+    flight_mode: ShipNavFlightMode = Field(ShipNavFlightMode.CRUISE, alias="flightMode")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_nav_route.py` & `spacetraders-0.2.3/spacetraders/models/ship_nav_route.py`

 * *Files 12% similar despite different names*

```diff
@@ -40,14 +40,18 @@
     arrival: datetime.datetime = Field(alias="arrival")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_nav_route_waypoint.py` & `spacetraders-0.2.3/spacetraders/models/ship_nav_route_waypoint.py`

 * *Files 8% similar despite different names*

```diff
@@ -38,14 +38,18 @@
     y: int = Field(alias="y")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_reactor.py` & `spacetraders-0.2.3/spacetraders/models/waypoint_trait.py`

 * *Files 18% similar despite different names*

```diff
@@ -5,53 +5,46 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
-    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_reactor_symbol import ShipReactorSymbol
-from ..models.ship_requirements import ShipRequirements
+from ..models.waypoint_trait_symbol import WaypointTraitSymbol
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipReactor")
+T = TypeVar("T", bound="WaypointTrait")
 
 
-class ShipReactor(BaseModel):
-    """The reactor of the ship. The reactor is responsible for powering the ship's systems and weapons.
-
+class WaypointTrait(BaseModel):
+    """
     Attributes:
-        symbol (ShipReactorSymbol):
-        name (str):
-        description (str):
-        power_output (int):
-        requirements (ShipRequirements): The requirements for installation on a ship
-        condition (Union[Unset, int]): Condition is a range of 0 to 100 where 0 is completely worn out and 100 is brand
-            new.
+        symbol (WaypointTraitSymbol): The unique identifier of the trait.
+        name (str): The name of the trait.
+        description (str): A description of the trait.
     """
 
-    symbol: ShipReactorSymbol = Field(alias="symbol")
+    symbol: WaypointTraitSymbol = Field(alias="symbol")
     name: str = Field(alias="name")
     description: str = Field(alias="description")
-    power_output: int = Field(alias="powerOutput")
-    requirements: "ShipRequirements" = Field(alias="requirements")
-    condition: Union[Unset, int] = UNSET
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_refine_json_body.py` & `spacetraders-0.2.3/spacetraders/models/get_contracts_response_200.py`

 * *Files 27% similar despite different names*

```diff
@@ -5,38 +5,46 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_refine_json_body_produce import ShipRefineJsonBodyProduce
+from ..models.contract import Contract
+from ..models.meta import Meta
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipRefineJsonBody")
+T = TypeVar("T", bound="GetContractsResponse200")
 
 
-class ShipRefineJsonBody(BaseModel):
+class GetContractsResponse200(BaseModel):
     """
     Attributes:
-        produce (ShipRefineJsonBodyProduce):
+        data (List['Contract']):
+        meta (Meta):
     """
 
-    produce: ShipRefineJsonBodyProduce = Field(alias="produce")
+    data: List["Contract"] = Field(alias="data")
+    meta: "Meta" = Field(alias="meta")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_refine_ship_refine_200_response.py` & `spacetraders-0.2.3/spacetraders/models/ship_refine_ship_refine_200_response.py`

 * *Files 8% similar despite different names*

```diff
@@ -32,14 +32,18 @@
     data: "ShipRefineShipRefine200ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_refine_ship_refine_200_response_data.py` & `spacetraders-0.2.3/spacetraders/models/ship_refine_ship_refine_200_response_data.py`

 * *Files 7% similar despite different names*

```diff
@@ -47,14 +47,18 @@
     )
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_refine_ship_refine_200_response_data_consumed_item.py` & `spacetraders-0.2.3/spacetraders/models/ship_refine_ship_refine_200_response_data_consumed_item.py`

 * *Files 9% similar despite different names*

```diff
@@ -23,22 +23,26 @@
 class ShipRefineShipRefine200ResponseDataConsumedItem(BaseModel):
     """
     Attributes:
         trade_symbol (Union[Unset, str]):
         units (Union[Unset, int]):
     """
 
-    trade_symbol: Union[Unset, str] = UNSET
-    units: Union[Unset, int] = UNSET
+    trade_symbol: Union[Unset, str] = Field(UNSET, alias="tradeSymbol")
+    units: Union[Unset, int] = Field(UNSET, alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_refine_ship_refine_200_response_data_produced_item.py` & `spacetraders-0.2.3/spacetraders/models/ship_refine_ship_refine_200_response_data_produced_item.py`

 * *Files 8% similar despite different names*

```diff
@@ -23,22 +23,26 @@
 class ShipRefineShipRefine200ResponseDataProducedItem(BaseModel):
     """
     Attributes:
         trade_symbol (Union[Unset, str]):
         units (Union[Unset, int]):
     """
 
-    trade_symbol: Union[Unset, str] = UNSET
-    units: Union[Unset, int] = UNSET
+    trade_symbol: Union[Unset, str] = Field(UNSET, alias="tradeSymbol")
+    units: Union[Unset, int] = Field(UNSET, alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_registration.py` & `spacetraders-0.2.3/spacetraders/models/navigate_ship_response_200_data.py`

 * *Files 17% similar despite different names*

```diff
@@ -5,44 +5,47 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_role import ShipRole
+from ..models.ship_fuel import ShipFuel
+from ..models.ship_nav import ShipNav
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipRegistration")
+T = TypeVar("T", bound="NavigateShipResponse200Data")
 
 
-class ShipRegistration(BaseModel):
-    """The public registration information of the ship
-
+class NavigateShipResponse200Data(BaseModel):
+    """
     Attributes:
-        name (str): The agent's registered name of the ship
-        role (ShipRole): The registered role of the ship
-        faction_symbol (Union[Unset, str]): The symbol of the faction the ship is registered with
+        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
+            or action.
+        nav (ShipNav): The navigation information of the ship.
     """
 
-    name: str = Field(alias="name")
-    role: ShipRole = Field(alias="role")
-    faction_symbol: Union[Unset, str] = UNSET
+    fuel: "ShipFuel" = Field(alias="fuel")
+    nav: "ShipNav" = Field(alias="nav")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_requirements.py` & `spacetraders-0.2.3/spacetraders/models/purchase_cargo_purchase_cargo_201_response_data.py`

 * *Files 24% similar despite different names*

```diff
@@ -5,43 +5,49 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
+from ..models.agent import Agent
+from ..models.market_transaction import MarketTransaction
+from ..models.ship_cargo import ShipCargo
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipRequirements")
+T = TypeVar("T", bound="PurchaseCargoPurchaseCargo201ResponseData")
 
 
-class ShipRequirements(BaseModel):
-    """The requirements for installation on a ship
-
+class PurchaseCargoPurchaseCargo201ResponseData(BaseModel):
+    """
     Attributes:
-        power (Union[Unset, int]): The amount of power required from the reactor.
-        crew (Union[Unset, int]): The number of crew required for operation.
-        slots (Union[Unset, int]): The number of module slots required for installation.
+        agent (Agent):
+        cargo (ShipCargo):
+        transaction (MarketTransaction):
     """
 
-    power: Union[Unset, int] = UNSET
-    crew: Union[Unset, int] = UNSET
-    slots: Union[Unset, int] = UNSET
+    agent: "Agent" = Field(alias="agent")
+    cargo: "ShipCargo" = Field(alias="cargo")
+    transaction: "MarketTransaction" = Field(alias="transaction")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/ship_type.py` & `spacetraders-0.2.3/spacetraders/models/ship_type.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/shipyard.py` & `spacetraders-0.2.3/spacetraders/models/shipyard.py`

 * *Files 7% similar despite different names*

```diff
@@ -31,22 +31,28 @@
         ship_types (List['ShipyardShipTypesItem']): The list of ship types available for purchase at this shipyard.
         transactions (Union[Unset, List['ShipyardTransaction']]): The list of recent transactions at this shipyard.
         ships (Union[Unset, List['ShipyardShip']]): The ships that are currently available for purchase at the shipyard.
     """
 
     symbol: str = Field(alias="symbol")
     ship_types: List["ShipyardShipTypesItem"] = Field(alias="shipTypes")
-    transactions: Union[Unset, List["ShipyardTransaction"]] = UNSET
-    ships: Union[Unset, List["ShipyardShip"]] = UNSET
+    transactions: Union[Unset, List["ShipyardTransaction"]] = Field(
+        UNSET, alias="transactions"
+    )
+    ships: Union[Unset, List["ShipyardShip"]] = Field(UNSET, alias="ships")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/shipyard_ship.py` & `spacetraders-0.2.3/spacetraders/models/create_ship_ship_scan_response_201_data.py`

 * *Files 24% similar despite different names*

```diff
@@ -5,64 +5,46 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_engine import ShipEngine
-from ..models.ship_frame import ShipFrame
-from ..models.ship_module import ShipModule
-from ..models.ship_mount import ShipMount
-from ..models.ship_reactor import ShipReactor
-from ..models.ship_type import ShipType
+from ..models.cooldown import Cooldown
+from ..models.scanned_ship import ScannedShip
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipyardShip")
+T = TypeVar("T", bound="CreateShipShipScanResponse201Data")
 
 
-class ShipyardShip(BaseModel):
+class CreateShipShipScanResponse201Data(BaseModel):
     """
     Attributes:
-        name (str):
-        description (str):
-        purchase_price (int):
-        frame (ShipFrame): The frame of the ship. The frame determines the number of modules and mounting points of the
-            ship, as well as base fuel capacity. As the condition of the frame takes more wear, the ship will become more
-            sluggish and less maneuverable.
-        reactor (ShipReactor): The reactor of the ship. The reactor is responsible for powering the ship's systems and
-            weapons.
-        engine (ShipEngine): The engine determines how quickly a ship travels between waypoints.
-        modules (List['ShipModule']):
-        mounts (List['ShipMount']):
-        type (Union[Unset, ShipType]):
+        cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
+        ships (List['ScannedShip']):
     """
 
-    name: str = Field(alias="name")
-    description: str = Field(alias="description")
-    purchase_price: int = Field(alias="purchasePrice")
-    frame: "ShipFrame" = Field(alias="frame")
-    reactor: "ShipReactor" = Field(alias="reactor")
-    engine: "ShipEngine" = Field(alias="engine")
-    modules: List["ShipModule"] = Field(alias="modules")
-    mounts: List["ShipMount"] = Field(alias="mounts")
-    type: Union[Unset, ShipType] = UNSET
+    cooldown: "Cooldown" = Field(alias="cooldown")
+    ships: List["ScannedShip"] = Field(alias="ships")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/shipyard_ship_types_item.py` & `spacetraders-0.2.3/spacetraders/models/accept_contract_response_200.py`

 * *Files 24% similar despite different names*

```diff
@@ -5,39 +5,43 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
-    Union,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_type import ShipType
+from ..models.accept_contract_response_200_data import AcceptContractResponse200Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ShipyardShipTypesItem")
+T = TypeVar("T", bound="AcceptContractResponse200")
 
 
-class ShipyardShipTypesItem(BaseModel):
+class AcceptContractResponse200(BaseModel):
     """
     Attributes:
-        type (Union[Unset, ShipType]):
+        data (AcceptContractResponse200Data):
     """
 
-    type: Union[Unset, ShipType] = UNSET
+    data: "AcceptContractResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/shipyard_transaction.py` & `spacetraders-0.2.3/spacetraders/models/shipyard_transaction.py`

 * *Files 13% similar despite different names*

```diff
@@ -39,14 +39,18 @@
     timestamp: datetime.datetime = Field(alias="timestamp")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/survey.py` & `spacetraders-0.2.3/spacetraders/models/survey.py`

 * *Files 14% similar despite different names*

```diff
@@ -46,14 +46,18 @@
     size: SurveySize = Field(alias="size")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/survey_deposit.py` & `spacetraders-0.2.3/spacetraders/models/warp_ship_json_body.py`

 * *Files 22% similar despite different names*

```diff
@@ -12,31 +12,34 @@
 )
 
 import attr
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="SurveyDeposit")
+T = TypeVar("T", bound="WarpShipJsonBody")
 
 
-class SurveyDeposit(BaseModel):
-    """A surveyed deposit of a mineral or resource available for extraction.
-
+class WarpShipJsonBody(BaseModel):
+    """
     Attributes:
-        symbol (str): The symbol of the deposit.
+        waypoint_symbol (str): The target destination.
     """
 
-    symbol: str = Field(alias="symbol")
+    waypoint_symbol: str = Field(alias="waypointSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/system.py` & `spacetraders-0.2.3/spacetraders/models/get_systems_response_200.py`

 * *Files 18% similar despite different names*

```diff
@@ -11,47 +11,40 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.system_faction import SystemFaction
-from ..models.system_type import SystemType
-from ..models.system_waypoint import SystemWaypoint
+from ..models.meta import Meta
+from ..models.system import System
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="System")
+T = TypeVar("T", bound="GetSystemsResponse200")
 
 
-class System(BaseModel):
+class GetSystemsResponse200(BaseModel):
     """
     Attributes:
-        symbol (str):
-        sector_symbol (str):
-        type (SystemType): The type of waypoint.
-        x (int):
-        y (int):
-        waypoints (List['SystemWaypoint']):
-        factions (List['SystemFaction']):
+        data (List['System']):
+        meta (Meta):
     """
 
-    symbol: str = Field(alias="symbol")
-    sector_symbol: str = Field(alias="sectorSymbol")
-    type: SystemType = Field(alias="type")
-    x: int = Field(alias="x")
-    y: int = Field(alias="y")
-    waypoints: List["SystemWaypoint"] = Field(alias="waypoints")
-    factions: List["SystemFaction"] = Field(alias="factions")
+    data: List["System"] = Field(alias="data")
+    meta: "Meta" = Field(alias="meta")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/system_faction.py` & `spacetraders-0.2.3/spacetraders/models/contract_payment.py`

 * *Files 26% similar despite different names*

```diff
@@ -12,30 +12,36 @@
 )
 
 import attr
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="SystemFaction")
+T = TypeVar("T", bound="ContractPayment")
 
 
-class SystemFaction(BaseModel):
+class ContractPayment(BaseModel):
     """
     Attributes:
-        symbol (str):
+        on_accepted (int): The amount of credits received up front for accepting the contract.
+        on_fulfilled (int): The amount of credits received when the contract is fulfilled.
     """
 
-    symbol: str = Field(alias="symbol")
+    on_accepted: int = Field(alias="onAccepted")
+    on_fulfilled: int = Field(alias="onFulfilled")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/system_waypoint.py` & `spacetraders-0.2.3/spacetraders/models/get_jump_gate_response_200.py`

 * *Files 25% similar despite different names*

```diff
@@ -5,44 +5,43 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.waypoint_type import WaypointType
+from ..models.jump_gate import JumpGate
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="SystemWaypoint")
+T = TypeVar("T", bound="GetJumpGateResponse200")
 
 
-class SystemWaypoint(BaseModel):
+class GetJumpGateResponse200(BaseModel):
     """
     Attributes:
-        symbol (str):
-        type (WaypointType): The type of waypoint.
-        x (int):
-        y (int):
+        data (JumpGate):
     """
 
-    symbol: str = Field(alias="symbol")
-    type: WaypointType = Field(alias="type")
-    x: int = Field(alias="x")
-    y: int = Field(alias="y")
+    data: "JumpGate" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/trade_symbol.py` & `spacetraders-0.2.3/spacetraders/models/trade_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/models/transfer_cargo_transfer_cargo_200_response_data.py` & `spacetraders-0.2.3/spacetraders/models/transfer_cargo_transfer_cargo_200_response_data.py`

 * *Files 4% similar despite different names*

```diff
@@ -30,14 +30,18 @@
     cargo: "ShipCargo" = Field(alias="cargo")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/warp_ship_response_200.py` & `spacetraders-0.2.3/spacetraders/models/deliver_contract_response_200.py`

 * *Files 26% similar despite different names*

```diff
@@ -11,33 +11,37 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.warp_ship_response_200_data import WarpShipResponse200Data
+from ..models.deliver_contract_response_200_data import DeliverContractResponse200Data
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="WarpShipResponse200")
+T = TypeVar("T", bound="DeliverContractResponse200")
 
 
-class WarpShipResponse200(BaseModel):
+class DeliverContractResponse200(BaseModel):
     """
     Attributes:
-        data (WarpShipResponse200Data):
+        data (DeliverContractResponse200Data):
     """
 
-    data: "WarpShipResponse200Data" = Field(alias="data")
+    data: "DeliverContractResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/warp_ship_response_200_data.py` & `spacetraders-0.2.3/spacetraders/models/accept_contract_response_200_data.py`

 * *Files 16% similar despite different names*

```diff
@@ -11,37 +11,40 @@
     TypeVar,
     cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_fuel import ShipFuel
-from ..models.ship_nav import ShipNav
+from ..models.agent import Agent
+from ..models.contract import Contract
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="WarpShipResponse200Data")
+T = TypeVar("T", bound="AcceptContractResponse200Data")
 
 
-class WarpShipResponse200Data(BaseModel):
+class AcceptContractResponse200Data(BaseModel):
     """
     Attributes:
-        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
-            or action.
-        nav (ShipNav): The navigation information of the ship.
+        agent (Agent):
+        contract (Contract):
     """
 
-    fuel: "ShipFuel" = Field(alias="fuel")
-    nav: "ShipNav" = Field(alias="nav")
+    agent: "Agent" = Field(alias="agent")
+    contract: "Contract" = Field(alias="contract")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/waypoint.py` & `spacetraders-0.2.3/spacetraders/models/waypoint.py`

 * *Files 14% similar despite different names*

```diff
@@ -45,22 +45,26 @@
     symbol: str = Field(alias="symbol")
     type: WaypointType = Field(alias="type")
     system_symbol: str = Field(alias="systemSymbol")
     x: int = Field(alias="x")
     y: int = Field(alias="y")
     orbitals: List["WaypointOrbital"] = Field(alias="orbitals")
     traits: List["WaypointTrait"] = Field(alias="traits")
-    faction: Union[Unset, "WaypointFaction"] = UNSET
-    chart: Union[Unset, "Chart"] = UNSET
+    faction: Union[Unset, "WaypointFaction"] = Field(UNSET, alias="faction")
+    chart: Union[Unset, "Chart"] = Field(UNSET, alias="chart")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/waypoint_orbital.py` & `spacetraders-0.2.3/spacetraders/models/extract_resources_json_body.py`

 * *Files 24% similar despite different names*

```diff
@@ -5,38 +5,45 @@
     Dict,
     List,
     Optional,
     TextIO,
     Tuple,
     Type,
     TypeVar,
+    Union,
+    cast,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
+from ..models.survey import Survey
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="WaypointOrbital")
+T = TypeVar("T", bound="ExtractResourcesJsonBody")
 
 
-class WaypointOrbital(BaseModel):
-    """An orbital is another waypoint that orbits a parent waypoint.
-
+class ExtractResourcesJsonBody(BaseModel):
+    """
     Attributes:
-        symbol (str):
+        survey (Union[Unset, Survey]): A resource survey of a waypoint, detailing a specific extraction location and the
+            types of resources that can be found there.
     """
 
-    symbol: str = Field(alias="symbol")
+    survey: Union[Unset, "Survey"] = Field(UNSET, alias="survey")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/waypoint_trait.py` & `spacetraders-0.2.3/spacetraders/models/deliver_contract_json_body.py`

 * *Files 19% similar despite different names*

```diff
@@ -10,37 +10,40 @@
     Type,
     TypeVar,
 )
 
 import attr
 from pydantic import BaseModel, Field
 
-from ..models.waypoint_trait_symbol import WaypointTraitSymbol
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="WaypointTrait")
+T = TypeVar("T", bound="DeliverContractJsonBody")
 
 
-class WaypointTrait(BaseModel):
+class DeliverContractJsonBody(BaseModel):
     """
     Attributes:
-        symbol (WaypointTraitSymbol): The unique identifier of the trait.
-        name (str): The name of the trait.
-        description (str): A description of the trait.
+        ship_symbol (str):
+        trade_symbol (str):
+        units (int):
     """
 
-    symbol: WaypointTraitSymbol = Field(alias="symbol")
-    name: str = Field(alias="name")
-    description: str = Field(alias="description")
+    ship_symbol: str = Field(alias="shipSymbol")
+    trade_symbol: str = Field(alias="tradeSymbol")
+    units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
+    def dict(self, *args, **kwargs):
+        output = super().dict(*args, **kwargs)
+        return {k: v for k, v in output.items() if v is not UNSET}
+
     @property
     def additional_keys(self) -> List[str]:
         return list(self.additional_properties.keys())
 
     def __getitem__(self, key: str) -> Any:
         return self.additional_properties[key]
```

### Comparing `spacetraders-0.2.2/spacetraders/models/waypoint_trait_symbol.py` & `spacetraders-0.2.3/spacetraders/models/waypoint_trait_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/spacetraders/types.py` & `spacetraders-0.2.3/spacetraders/types.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.2/PKG-INFO` & `spacetraders-0.2.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spacetraders
-Version: 0.2.2
+Version: 0.2.3
 Summary: Python API for Space Traders
 License: Apache-2.0
 Author: Marco Ceppi
 Author-email: marco@ceppi.net
 Requires-Python: >=3.11,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3
```

