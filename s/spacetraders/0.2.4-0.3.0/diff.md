# Comparing `tmp/spacetraders-0.2.4.tar.gz` & `tmp/spacetraders-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spacetraders-0.2.4.tar", max compression
+gzip compressed data, was "spacetraders-0.3.0.tar", max compression
```

## Comparing `spacetraders-0.2.4.tar` & `spacetraders-0.3.0.tar`

### file list

```diff
@@ -1,208 +1,208 @@
--rw-r--r--   0        0        0     3472 2023-05-10 04:00:00.539673 spacetraders-0.2.4/README.md
--rw-r--r--   0        0        0      568 2023-05-12 23:11:29.017096 spacetraders-0.2.4/pyproject.toml
--rw-r--r--   0        0        0      250 2023-05-12 23:10:29.867096 spacetraders-0.2.4/spacetraders/__init__.py
--rw-r--r--   0        0        0       47 2023-05-12 23:10:29.397096 spacetraders-0.2.4/spacetraders/api/__init__.py
--rw-r--r--   0        0        0        0 2023-05-12 23:10:29.447096 spacetraders-0.2.4/spacetraders/api/agents/__init__.py
--rw-r--r--   0        0        0     3818 2023-05-12 23:10:29.927096 spacetraders-0.2.4/spacetraders/api/agents/get_my_agent.py
--rw-r--r--   0        0        0        0 2023-05-12 23:10:29.447096 spacetraders-0.2.4/spacetraders/api/contracts/__init__.py
--rw-r--r--   0        0        0     4290 2023-05-12 23:10:29.937096 spacetraders-0.2.4/spacetraders/api/contracts/accept_contract.py
--rw-r--r--   0        0        0     5161 2023-05-12 23:10:29.947096 spacetraders-0.2.4/spacetraders/api/contracts/deliver_contract.py
--rw-r--r--   0        0        0     4308 2023-05-12 23:10:29.927096 spacetraders-0.2.4/spacetraders/api/contracts/fulfill_contract.py
--rw-r--r--   0        0        0     4303 2023-05-12 23:10:29.927096 spacetraders-0.2.4/spacetraders/api/contracts/get_contract.py
--rw-r--r--   0        0        0     5015 2023-05-12 23:10:29.957096 spacetraders-0.2.4/spacetraders/api/contracts/get_contracts.py
--rw-r--r--   0        0        0        0 2023-05-12 23:10:29.407096 spacetraders-0.2.4/spacetraders/api/default/__init__.py
--rw-r--r--   0        0        0     9240 2023-05-12 23:10:29.927096 spacetraders-0.2.4/spacetraders/api/default/register.py
--rw-r--r--   0        0        0        0 2023-05-12 23:10:29.447096 spacetraders-0.2.4/spacetraders/api/factions/__init__.py
--rw-r--r--   0        0        0     4361 2023-05-12 23:10:29.937096 spacetraders-0.2.4/spacetraders/api/factions/get_faction.py
--rw-r--r--   0        0        0     4985 2023-05-12 23:10:29.947096 spacetraders-0.2.4/spacetraders/api/factions/get_factions.py
--rw-r--r--   0        0        0        0 2023-05-12 23:10:29.447096 spacetraders-0.2.4/spacetraders/api/fleet/__init__.py
--rw-r--r--   0        0        0     5255 2023-05-12 23:10:29.927096 spacetraders-0.2.4/spacetraders/api/fleet/create_chart.py
--rw-r--r--   0        0        0     4513 2023-05-12 23:10:29.937096 spacetraders-0.2.4/spacetraders/api/fleet/create_ship_ship_scan.py
--rw-r--r--   0        0        0     4566 2023-05-12 23:10:29.947096 spacetraders-0.2.4/spacetraders/api/fleet/create_ship_system_scan.py
--rw-r--r--   0        0        0     4610 2023-05-12 23:10:29.947096 spacetraders-0.2.4/spacetraders/api/fleet/create_ship_waypoint_scan.py
--rw-r--r--   0        0        0     6213 2023-05-12 23:10:29.937096 spacetraders-0.2.4/spacetraders/api/fleet/create_survey.py
--rw-r--r--   0        0        0     5356 2023-05-12 23:10:29.947096 spacetraders-0.2.4/spacetraders/api/fleet/dock_ship.py
--rw-r--r--   0        0        0     5540 2023-05-12 23:10:29.947096 spacetraders-0.2.4/spacetraders/api/fleet/extract_resources.py
--rw-r--r--   0        0        0     4236 2023-05-12 23:10:29.987096 spacetraders-0.2.4/spacetraders/api/fleet/get_my_ship.py
--rw-r--r--   0        0        0     4338 2023-05-12 23:10:29.987096 spacetraders-0.2.4/spacetraders/api/fleet/get_my_ship_cargo.py
--rw-r--r--   0        0        0     4970 2023-05-12 23:10:30.007096 spacetraders-0.2.4/spacetraders/api/fleet/get_my_ships.py
--rw-r--r--   0        0        0     6390 2023-05-12 23:10:30.007096 spacetraders-0.2.4/spacetraders/api/fleet/get_ship_cooldown.py
--rw-r--r--   0        0        0     4295 2023-05-12 23:10:29.997096 spacetraders-0.2.4/spacetraders/api/fleet/get_ship_nav.py
--rw-r--r--   0        0        0     5002 2023-05-12 23:10:30.017096 spacetraders-0.2.4/spacetraders/api/fleet/jettison.py
--rw-r--r--   0        0        0     5292 2023-05-12 23:10:30.047096 spacetraders-0.2.4/spacetraders/api/fleet/jump_ship.py
--rw-r--r--   0        0        0     6936 2023-05-12 23:10:30.017096 spacetraders-0.2.4/spacetraders/api/fleet/navigate_ship.py
--rw-r--r--   0        0        0     5331 2023-05-12 23:10:30.027096 spacetraders-0.2.4/spacetraders/api/fleet/orbit_ship.py
--rw-r--r--   0        0        0     5154 2023-05-12 23:10:30.047096 spacetraders-0.2.4/spacetraders/api/fleet/patch_ship_nav.py
--rw-r--r--   0        0        0     5373 2023-05-12 23:10:30.037096 spacetraders-0.2.4/spacetraders/api/fleet/purchase_cargo.py
--rw-r--r--   0        0        0     4583 2023-05-12 23:10:30.057096 spacetraders-0.2.4/spacetraders/api/fleet/purchase_ship.py
--rw-r--r--   0        0        0     4302 2023-05-12 23:10:30.017096 spacetraders-0.2.4/spacetraders/api/fleet/refuel_ship.py
--rw-r--r--   0        0        0     5111 2023-05-12 23:10:30.017096 spacetraders-0.2.4/spacetraders/api/fleet/sell_cargo.py
--rw-r--r--   0        0        0     5599 2023-05-12 23:10:30.067096 spacetraders-0.2.4/spacetraders/api/fleet/ship_refine.py
--rw-r--r--   0        0        0     5424 2023-05-12 23:10:30.047096 spacetraders-0.2.4/spacetraders/api/fleet/transfer_cargo.py
--rw-r--r--   0        0        0     6332 2023-05-12 23:10:30.067096 spacetraders-0.2.4/spacetraders/api/fleet/warp_ship.py
--rw-r--r--   0        0        0        0 2023-05-12 23:10:29.437096 spacetraders-0.2.4/spacetraders/api/systems/__init__.py
--rw-r--r--   0        0        0     4838 2023-05-12 23:10:30.067096 spacetraders-0.2.4/spacetraders/api/systems/get_jump_gate.py
--rw-r--r--   0        0        0     5624 2023-05-12 23:10:30.087096 spacetraders-0.2.4/spacetraders/api/systems/get_market.py
--rw-r--r--   0        0        0     4812 2023-05-12 23:10:30.097096 spacetraders-0.2.4/spacetraders/api/systems/get_shipyard.py
--rw-r--r--   0        0        0     4398 2023-05-12 23:10:30.087096 spacetraders-0.2.4/spacetraders/api/systems/get_system.py
--rw-r--r--   0        0        0     5944 2023-05-12 23:10:30.127096 spacetraders-0.2.4/spacetraders/api/systems/get_system_waypoints.py
--rw-r--r--   0        0        0     4984 2023-05-12 23:10:30.127096 spacetraders-0.2.4/spacetraders/api/systems/get_systems.py
--rw-r--r--   0        0        0     4799 2023-05-12 23:10:30.107096 spacetraders-0.2.4/spacetraders/api/systems/get_waypoint.py
--rw-r--r--   0        0        0     4213 2023-05-12 23:10:30.107096 spacetraders-0.2.4/spacetraders/client.py
--rw-r--r--   0        0        0      470 2023-05-12 23:10:30.027096 spacetraders-0.2.4/spacetraders/errors.py
--rw-r--r--   0        0        0    13081 2023-05-12 23:10:30.197096 spacetraders-0.2.4/spacetraders/models/__init__.py
--rw-r--r--   0        0        0     1378 2023-05-12 23:10:30.077096 spacetraders-0.2.4/spacetraders/models/accept_contract_response_200.py
--rw-r--r--   0        0        0     1408 2023-05-12 23:10:30.077096 spacetraders-0.2.4/spacetraders/models/accept_contract_response_200_data.py
--rw-r--r--   0        0        0     1559 2023-05-12 23:10:30.077096 spacetraders-0.2.4/spacetraders/models/agent.py
--rw-r--r--   0        0        0     1671 2023-05-12 23:10:30.077096 spacetraders-0.2.4/spacetraders/models/chart.py
--rw-r--r--   0        0        0     1801 2023-05-12 23:10:30.097096 spacetraders-0.2.4/spacetraders/models/connected_system.py
--rw-r--r--   0        0        0     2033 2023-05-12 23:10:30.107096 spacetraders-0.2.4/spacetraders/models/contract.py
--rw-r--r--   0        0        0     1811 2023-05-12 23:10:30.117096 spacetraders-0.2.4/spacetraders/models/contract_deliver_good.py
--rw-r--r--   0        0        0     1439 2023-05-12 23:10:30.107096 spacetraders-0.2.4/spacetraders/models/contract_payment.py
--rw-r--r--   0        0        0     1706 2023-05-12 23:10:30.117096 spacetraders-0.2.4/spacetraders/models/contract_terms.py
--rw-r--r--   0        0        0      201 2023-05-12 23:10:29.567096 spacetraders-0.2.4/spacetraders/models/contract_type.py
--rw-r--r--   0        0        0     1837 2023-05-12 23:10:30.127096 spacetraders-0.2.4/spacetraders/models/cooldown.py
--rw-r--r--   0        0        0     1360 2023-05-12 23:10:30.117096 spacetraders-0.2.4/spacetraders/models/create_chart_response_201.py
--rw-r--r--   0        0        0     1578 2023-05-12 23:10:30.147096 spacetraders-0.2.4/spacetraders/models/create_chart_response_201_data.py
--rw-r--r--   0        0        0     1413 2023-05-12 23:10:30.137096 spacetraders-0.2.4/spacetraders/models/create_ship_ship_scan_response_201.py
--rw-r--r--   0        0        0     1534 2023-05-12 23:10:30.137096 spacetraders-0.2.4/spacetraders/models/create_ship_ship_scan_response_201_data.py
--rw-r--r--   0        0        0     1425 2023-05-12 23:10:30.137096 spacetraders-0.2.4/spacetraders/models/create_ship_system_scan_response_201.py
--rw-r--r--   0        0        0     1552 2023-05-12 23:10:30.157096 spacetraders-0.2.4/spacetraders/models/create_ship_system_scan_response_201_data.py
--rw-r--r--   0        0        0     1437 2023-05-12 23:10:30.167096 spacetraders-0.2.4/spacetraders/models/create_ship_waypoint_scan_response_201.py
--rw-r--r--   0        0        0     1570 2023-05-12 23:10:30.167096 spacetraders-0.2.4/spacetraders/models/create_ship_waypoint_scan_response_201_data.py
--rw-r--r--   0        0        0     1366 2023-05-12 23:10:30.147096 spacetraders-0.2.4/spacetraders/models/create_survey_response_201.py
--rw-r--r--   0        0        0     1507 2023-05-12 23:10:30.167096 spacetraders-0.2.4/spacetraders/models/create_survey_response_201_data.py
--rw-r--r--   0        0        0     1383 2023-05-12 23:10:30.147096 spacetraders-0.2.4/spacetraders/models/deliver_contract_json_body.py
--rw-r--r--   0        0        0     1384 2023-05-12 23:10:30.177096 spacetraders-0.2.4/spacetraders/models/deliver_contract_response_200.py
--rw-r--r--   0        0        0     1427 2023-05-12 23:10:30.197096 spacetraders-0.2.4/spacetraders/models/deliver_contract_response_200_data.py
--rw-r--r--   0        0        0     1401 2023-05-12 23:10:30.177096 spacetraders-0.2.4/spacetraders/models/dock_ship_dock_ship_200_response.py
--rw-r--r--   0        0        0     1336 2023-05-12 23:10:30.157096 spacetraders-0.2.4/spacetraders/models/dock_ship_dock_ship_200_response_data.py
--rw-r--r--   0        0        0     1470 2023-05-12 23:10:30.157096 spacetraders-0.2.4/spacetraders/models/extract_resources_json_body.py
--rw-r--r--   0        0        0     1390 2023-05-12 23:10:30.187096 spacetraders-0.2.4/spacetraders/models/extract_resources_response_201.py
--rw-r--r--   0        0        0     1641 2023-05-12 23:10:30.187096 spacetraders-0.2.4/spacetraders/models/extract_resources_response_201_data.py
--rw-r--r--   0        0        0     1370 2023-05-12 23:10:30.197096 spacetraders-0.2.4/spacetraders/models/extraction.py
--rw-r--r--   0        0        0     1349 2023-05-12 23:10:30.177096 spacetraders-0.2.4/spacetraders/models/extraction_yield.py
--rw-r--r--   0        0        0     1566 2023-05-12 23:10:30.207096 spacetraders-0.2.4/spacetraders/models/faction.py
--rw-r--r--   0        0        0     1520 2023-05-12 23:10:30.177096 spacetraders-0.2.4/spacetraders/models/faction_trait.py
--rw-r--r--   0        0        0     2091 2023-05-12 23:10:29.647096 spacetraders-0.2.4/spacetraders/models/faction_trait_symbol.py
--rw-r--r--   0        0        0     1384 2023-05-12 23:10:30.187096 spacetraders-0.2.4/spacetraders/models/fulfill_contract_response_200.py
--rw-r--r--   0        0        0     1410 2023-05-12 23:10:30.197096 spacetraders-0.2.4/spacetraders/models/fulfill_contract_response_200_data.py
--rw-r--r--   0        0        0     1284 2023-05-12 23:10:30.187096 spacetraders-0.2.4/spacetraders/models/get_contract_response_200.py
--rw-r--r--   0        0        0     1391 2023-05-12 23:10:30.207096 spacetraders-0.2.4/spacetraders/models/get_contracts_response_200.py
--rw-r--r--   0        0        0     1278 2023-05-12 23:10:30.197096 spacetraders-0.2.4/spacetraders/models/get_faction_response_200.py
--rw-r--r--   0        0        0     1385 2023-05-12 23:10:30.217096 spacetraders-0.2.4/spacetraders/models/get_factions_response_200.py
--rw-r--r--   0        0        0     1285 2023-05-12 23:10:30.227096 spacetraders-0.2.4/spacetraders/models/get_jump_gate_response_200.py
--rw-r--r--   0        0        0     1272 2023-05-12 23:10:30.207096 spacetraders-0.2.4/spacetraders/models/get_market_response_200.py
--rw-r--r--   0        0        0     1270 2023-05-12 23:10:30.217096 spacetraders-0.2.4/spacetraders/models/get_my_agent_response_200.py
--rw-r--r--   0        0        0     1295 2023-05-12 23:10:30.217096 spacetraders-0.2.4/spacetraders/models/get_my_ship_cargo_response_200.py
--rw-r--r--   0        0        0     1271 2023-05-12 23:10:30.227096 spacetraders-0.2.4/spacetraders/models/get_my_ship_response_200.py
--rw-r--r--   0        0        0     1371 2023-05-12 23:10:30.227096 spacetraders-0.2.4/spacetraders/models/get_my_ships_response_200.py
--rw-r--r--   0        0        0     1371 2023-05-12 23:10:30.247096 spacetraders-0.2.4/spacetraders/models/get_ship_cooldown_response_200.py
--rw-r--r--   0        0        0     1319 2023-05-12 23:10:30.227096 spacetraders-0.2.4/spacetraders/models/get_ship_nav_response_200.py
--rw-r--r--   0        0        0     1284 2023-05-12 23:10:30.227096 spacetraders-0.2.4/spacetraders/models/get_shipyard_response_200.py
--rw-r--r--   0        0        0     1272 2023-05-12 23:10:30.217096 spacetraders-0.2.4/spacetraders/models/get_system_response_200.py
--rw-r--r--   0        0        0     1403 2023-05-12 23:10:30.237096 spacetraders-0.2.4/spacetraders/models/get_system_waypoints_response_200.py
--rw-r--r--   0        0        0     1379 2023-05-12 23:10:30.227096 spacetraders-0.2.4/spacetraders/models/get_systems_response_200.py
--rw-r--r--   0        0        0     1375 2023-05-12 23:10:30.237096 spacetraders-0.2.4/spacetraders/models/get_waypoint_response_200.py
--rw-r--r--   0        0        0     1276 2023-05-12 23:10:30.227096 spacetraders-0.2.4/spacetraders/models/jettison_json_body.py
--rw-r--r--   0        0        0     1341 2023-05-12 23:10:30.237096 spacetraders-0.2.4/spacetraders/models/jettison_response_200.py
--rw-r--r--   0        0        0     1294 2023-05-12 23:10:30.237096 spacetraders-0.2.4/spacetraders/models/jettison_response_200_data.py
--rw-r--r--   0        0        0     1708 2023-05-12 23:10:30.247096 spacetraders-0.2.4/spacetraders/models/jump_gate.py
--rw-r--r--   0        0        0     1267 2023-05-12 23:10:30.237096 spacetraders-0.2.4/spacetraders/models/jump_ship_json_body.py
--rw-r--r--   0        0        0     1342 2023-05-12 23:10:30.257096 spacetraders-0.2.4/spacetraders/models/jump_ship_response_200.py
--rw-r--r--   0        0        0     1564 2023-05-12 23:10:30.257096 spacetraders-0.2.4/spacetraders/models/jump_ship_response_200_data.py
--rw-r--r--   0        0        0     2500 2023-05-12 23:10:30.277096 spacetraders-0.2.4/spacetraders/models/market.py
--rw-r--r--   0        0        0     1979 2023-05-12 23:10:30.267096 spacetraders-0.2.4/spacetraders/models/market_trade_good.py
--rw-r--r--   0        0        0      224 2023-05-12 23:10:29.567096 spacetraders-0.2.4/spacetraders/models/market_trade_good_supply.py
--rw-r--r--   0        0        0     2255 2023-05-12 23:10:30.297096 spacetraders-0.2.4/spacetraders/models/market_transaction.py
--rw-r--r--   0        0        0      170 2023-05-12 23:10:29.577096 spacetraders-0.2.4/spacetraders/models/market_transaction_type.py
--rw-r--r--   0        0        0     1305 2023-05-12 23:10:30.287096 spacetraders-0.2.4/spacetraders/models/meta.py
--rw-r--r--   0        0        0     1275 2023-05-12 23:10:30.277096 spacetraders-0.2.4/spacetraders/models/navigate_ship_json_body.py
--rw-r--r--   0        0        0     1366 2023-05-12 23:10:30.257096 spacetraders-0.2.4/spacetraders/models/navigate_ship_response_200.py
--rw-r--r--   0        0        0     1553 2023-05-12 23:10:30.267096 spacetraders-0.2.4/spacetraders/models/navigate_ship_response_200_data.py
--rw-r--r--   0        0        0     1413 2023-05-12 23:10:30.277096 spacetraders-0.2.4/spacetraders/models/orbit_ship_orbit_ship_200_response.py
--rw-r--r--   0        0        0     1340 2023-05-12 23:10:30.267096 spacetraders-0.2.4/spacetraders/models/orbit_ship_orbit_ship_200_response_data.py
--rw-r--r--   0        0        0     1519 2023-05-12 23:10:30.277096 spacetraders-0.2.4/spacetraders/models/patch_ship_nav_json_body.py
--rw-r--r--   0        0        0     1323 2023-05-12 23:10:30.267096 spacetraders-0.2.4/spacetraders/models/patch_ship_nav_response_200.py
--rw-r--r--   0        0        0     1461 2023-05-12 23:10:30.287096 spacetraders-0.2.4/spacetraders/models/purchase_cargo_purchase_cargo_201_response.py
--rw-r--r--   0        0        0     1593 2023-05-12 23:10:30.287096 spacetraders-0.2.4/spacetraders/models/purchase_cargo_purchase_cargo_201_response_data.py
--rw-r--r--   0        0        0     1310 2023-05-12 23:10:30.297096 spacetraders-0.2.4/spacetraders/models/purchase_cargo_purchase_cargo_request.py
--rw-r--r--   0        0        0     1432 2023-05-12 23:10:30.287096 spacetraders-0.2.4/spacetraders/models/purchase_ship_json_body.py
--rw-r--r--   0        0        0     1366 2023-05-12 23:10:30.297096 spacetraders-0.2.4/spacetraders/models/purchase_ship_response_201.py
--rw-r--r--   0        0        0     1556 2023-05-12 23:10:30.297096 spacetraders-0.2.4/spacetraders/models/purchase_ship_response_201_data.py
--rw-r--r--   0        0        0     1354 2023-05-12 23:10:30.297096 spacetraders-0.2.4/spacetraders/models/refuel_ship_response_200.py
--rw-r--r--   0        0        0     1506 2023-05-12 23:10:30.307096 spacetraders-0.2.4/spacetraders/models/refuel_ship_response_200_data.py
--rw-r--r--   0        0        0     1518 2023-05-12 23:10:30.307096 spacetraders-0.2.4/spacetraders/models/register_json_body.py
--rw-r--r--   0        0        0      244 2023-05-12 23:10:29.627096 spacetraders-0.2.4/spacetraders/models/register_json_body_faction.py
--rw-r--r--   0        0        0     1341 2023-05-12 23:10:30.327096 spacetraders-0.2.4/spacetraders/models/register_response_201.py
--rw-r--r--   0        0        0     1717 2023-05-12 23:10:30.317096 spacetraders-0.2.4/spacetraders/models/register_response_201_data.py
--rw-r--r--   0        0        0     2546 2023-05-12 23:10:30.327096 spacetraders-0.2.4/spacetraders/models/scanned_ship.py
--rw-r--r--   0        0        0     1243 2023-05-12 23:10:30.307096 spacetraders-0.2.4/spacetraders/models/scanned_ship_engine.py
--rw-r--r--   0        0        0     1240 2023-05-12 23:10:30.327096 spacetraders-0.2.4/spacetraders/models/scanned_ship_frame.py
--rw-r--r--   0        0        0     1248 2023-05-12 23:10:30.317096 spacetraders-0.2.4/spacetraders/models/scanned_ship_mounts_item.py
--rw-r--r--   0        0        0     1246 2023-05-12 23:10:30.317096 spacetraders-0.2.4/spacetraders/models/scanned_ship_reactor.py
--rw-r--r--   0        0        0     1591 2023-05-12 23:10:30.337096 spacetraders-0.2.4/spacetraders/models/scanned_system.py
--rw-r--r--   0        0        0     2395 2023-05-12 23:10:30.367096 spacetraders-0.2.4/spacetraders/models/scanned_waypoint.py
--rw-r--r--   0        0        0     1413 2023-05-12 23:10:30.327096 spacetraders-0.2.4/spacetraders/models/sell_cargo_sell_cargo_201_response.py
--rw-r--r--   0        0        0     1577 2023-05-12 23:10:30.337096 spacetraders-0.2.4/spacetraders/models/sell_cargo_sell_cargo_201_response_data.py
--rw-r--r--   0        0        0     1294 2023-05-12 23:10:30.327096 spacetraders-0.2.4/spacetraders/models/sell_cargo_sell_cargo_request.py
--rw-r--r--   0        0        0     3249 2023-05-12 23:10:30.357096 spacetraders-0.2.4/spacetraders/models/ship.py
--rw-r--r--   0        0        0     1593 2023-05-12 23:10:30.347096 spacetraders-0.2.4/spacetraders/models/ship_cargo.py
--rw-r--r--   0        0        0     1609 2023-05-12 23:10:30.337096 spacetraders-0.2.4/spacetraders/models/ship_cargo_item.py
--rw-r--r--   0        0        0     2347 2023-05-12 23:10:30.347096 spacetraders-0.2.4/spacetraders/models/ship_crew.py
--rw-r--r--   0        0        0      167 2023-05-12 23:10:29.537096 spacetraders-0.2.4/spacetraders/models/ship_crew_rotation.py
--rw-r--r--   0        0        0     1985 2023-05-12 23:10:30.367096 spacetraders-0.2.4/spacetraders/models/ship_engine.py
--rw-r--r--   0        0        0      319 2023-05-12 23:10:29.627096 spacetraders-0.2.4/spacetraders/models/ship_engine_symbol.py
--rw-r--r--   0        0        0     2380 2023-05-12 23:10:30.357096 spacetraders-0.2.4/spacetraders/models/ship_frame.py
--rw-r--r--   0        0        0      694 2023-05-12 23:10:29.557096 spacetraders-0.2.4/spacetraders/models/ship_frame_symbol.py
--rw-r--r--   0        0        0     1688 2023-05-12 23:10:30.357096 spacetraders-0.2.4/spacetraders/models/ship_fuel.py
--rw-r--r--   0        0        0     1486 2023-05-12 23:10:30.357096 spacetraders-0.2.4/spacetraders/models/ship_fuel_consumed.py
--rw-r--r--   0        0        0     2067 2023-05-12 23:10:30.367096 spacetraders-0.2.4/spacetraders/models/ship_module.py
--rw-r--r--   0        0        0     1033 2023-05-12 23:10:29.577096 spacetraders-0.2.4/spacetraders/models/ship_module_symbol.py
--rw-r--r--   0        0        0     2049 2023-05-12 23:10:30.367096 spacetraders-0.2.4/spacetraders/models/ship_mount.py
--rw-r--r--   0        0        0      572 2023-05-12 23:10:29.627096 spacetraders-0.2.4/spacetraders/models/ship_mount_deposits_item.py
--rw-r--r--   0        0        0      854 2023-05-12 23:10:29.637096 spacetraders-0.2.4/spacetraders/models/ship_mount_symbol.py
--rw-r--r--   0        0        0     2223 2023-05-12 23:10:30.377096 spacetraders-0.2.4/spacetraders/models/ship_nav.py
--rw-r--r--   0        0        0      206 2023-05-12 23:10:29.557096 spacetraders-0.2.4/spacetraders/models/ship_nav_flight_mode.py
--rw-r--r--   0        0        0     2037 2023-05-12 23:10:30.367096 spacetraders-0.2.4/spacetraders/models/ship_nav_route.py
--rw-r--r--   0        0        0     1596 2023-05-12 23:10:30.367096 spacetraders-0.2.4/spacetraders/models/ship_nav_route_waypoint.py
--rw-r--r--   0        0        0      196 2023-05-12 23:10:29.577096 spacetraders-0.2.4/spacetraders/models/ship_nav_status.py
--rw-r--r--   0        0        0     2036 2023-05-12 23:10:30.377096 spacetraders-0.2.4/spacetraders/models/ship_reactor.py
--rw-r--r--   0        0        0      344 2023-05-12 23:10:29.557096 spacetraders-0.2.4/spacetraders/models/ship_reactor_symbol.py
--rw-r--r--   0        0        0     1345 2023-05-12 23:10:30.367096 spacetraders-0.2.4/spacetraders/models/ship_refine_json_body.py
--rw-r--r--   0        0        0      330 2023-05-12 23:10:29.627096 spacetraders-0.2.4/spacetraders/models/ship_refine_json_body_produce.py
--rw-r--r--   0        0        0     1425 2023-05-12 23:10:30.377096 spacetraders-0.2.4/spacetraders/models/ship_refine_ship_refine_200_response.py
--rw-r--r--   0        0        0     2156 2023-05-12 23:10:30.397096 spacetraders-0.2.4/spacetraders/models/ship_refine_ship_refine_200_response_data.py
--rw-r--r--   0        0        0     1436 2023-05-12 23:10:30.387096 spacetraders-0.2.4/spacetraders/models/ship_refine_ship_refine_200_response_data_consumed_item.py
--rw-r--r--   0        0        0     1436 2023-05-12 23:10:30.387096 spacetraders-0.2.4/spacetraders/models/ship_refine_ship_refine_200_response_data_produced_item.py
--rw-r--r--   0        0        0     1622 2023-05-12 23:10:30.397096 spacetraders-0.2.4/spacetraders/models/ship_registration.py
--rw-r--r--   0        0        0     1633 2023-05-12 23:10:30.397096 spacetraders-0.2.4/spacetraders/models/ship_requirements.py
--rw-r--r--   0        0        0      479 2023-05-12 23:10:29.617096 spacetraders-0.2.4/spacetraders/models/ship_role.py
--rw-r--r--   0        0        0      549 2023-05-12 23:10:29.547096 spacetraders-0.2.4/spacetraders/models/ship_type.py
--rw-r--r--   0        0        0     2111 2023-05-12 23:10:30.407096 spacetraders-0.2.4/spacetraders/models/shipyard.py
--rw-r--r--   0        0        0     2600 2023-05-12 23:10:30.417096 spacetraders-0.2.4/spacetraders/models/shipyard_ship.py
--rw-r--r--   0        0        0     1317 2023-05-12 23:10:30.397096 spacetraders-0.2.4/spacetraders/models/shipyard_ship_types_item.py
--rw-r--r--   0        0        0     1844 2023-05-12 23:10:30.407096 spacetraders-0.2.4/spacetraders/models/shipyard_transaction.py
--rw-r--r--   0        0        0     2374 2023-05-12 23:10:30.417096 spacetraders-0.2.4/spacetraders/models/survey.py
--rw-r--r--   0        0        0     1308 2023-05-12 23:10:30.397096 spacetraders-0.2.4/spacetraders/models/survey_deposit.py
--rw-r--r--   0        0        0      181 2023-05-12 23:10:29.557096 spacetraders-0.2.4/spacetraders/models/survey_size.py
--rw-r--r--   0        0        0     1834 2023-05-12 23:10:30.417096 spacetraders-0.2.4/spacetraders/models/system.py
--rw-r--r--   0        0        0     1211 2023-05-12 23:10:30.397096 spacetraders-0.2.4/spacetraders/models/system_faction.py
--rw-r--r--   0        0        0      405 2023-05-12 23:10:29.557096 spacetraders-0.2.4/spacetraders/models/system_type.py
--rw-r--r--   0        0        0     1451 2023-05-12 23:10:30.417096 spacetraders-0.2.4/spacetraders/models/system_waypoint.py
--rw-r--r--   0        0        0     1398 2023-05-12 23:10:30.417096 spacetraders-0.2.4/spacetraders/models/trade_good.py
--rw-r--r--   0        0        0     4422 2023-05-12 23:10:29.617096 spacetraders-0.2.4/spacetraders/models/trade_symbol.py
--rw-r--r--   0        0        0     1461 2023-05-12 23:10:30.427096 spacetraders-0.2.4/spacetraders/models/transfer_cargo_transfer_cargo_200_response.py
--rw-r--r--   0        0        0     1330 2023-05-12 23:10:30.417096 spacetraders-0.2.4/spacetraders/models/transfer_cargo_transfer_cargo_200_response_data.py
--rw-r--r--   0        0        0     1403 2023-05-12 23:10:30.427096 spacetraders-0.2.4/spacetraders/models/transfer_cargo_transfer_cargo_request.py
--rw-r--r--   0        0        0     1267 2023-05-12 23:10:30.417096 spacetraders-0.2.4/spacetraders/models/warp_ship_json_body.py
--rw-r--r--   0        0        0     1342 2023-05-12 23:10:30.427096 spacetraders-0.2.4/spacetraders/models/warp_ship_response_200.py
--rw-r--r--   0        0        0     1545 2023-05-12 23:10:30.427096 spacetraders-0.2.4/spacetraders/models/warp_ship_response_200_data.py
--rw-r--r--   0        0        0     2381 2023-05-12 23:10:30.437096 spacetraders-0.2.4/spacetraders/models/waypoint.py
--rw-r--r--   0        0        0     1215 2023-05-12 23:10:30.427096 spacetraders-0.2.4/spacetraders/models/waypoint_faction.py
--rw-r--r--   0        0        0     1277 2023-05-12 23:10:30.427096 spacetraders-0.2.4/spacetraders/models/waypoint_orbital.py
--rw-r--r--   0        0        0     1526 2023-05-12 23:10:30.427096 spacetraders-0.2.4/spacetraders/models/waypoint_trait.py
--rw-r--r--   0        0        0     2200 2023-05-12 23:10:29.647096 spacetraders-0.2.4/spacetraders/models/waypoint_trait_symbol.py
--rw-r--r--   0        0        0      381 2023-05-12 23:10:29.567096 spacetraders-0.2.4/spacetraders/models/waypoint_type.py
--rw-r--r--   0        0        0     1035 2023-05-12 23:10:30.427096 spacetraders-0.2.4/spacetraders/types.py
--rw-r--r--   0        0        0     4031 1970-01-01 00:00:00.000000 spacetraders-0.2.4/PKG-INFO
+-rw-r--r--   0        0        0     3472 2023-05-10 04:00:00.539673 spacetraders-0.3.0/README.md
+-rw-r--r--   0        0        0      664 2023-05-13 04:32:06.857117 spacetraders-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0      250 2023-05-13 04:23:44.257117 spacetraders-0.3.0/spacetraders/__init__.py
+-rw-r--r--   0        0        0       47 2023-05-13 04:23:43.767117 spacetraders-0.3.0/spacetraders/api/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:23:43.817117 spacetraders-0.3.0/spacetraders/api/agents/__init__.py
+-rw-r--r--   0        0        0     4139 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/agents/get_my_agent.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:23:43.817117 spacetraders-0.3.0/spacetraders/api/contracts/__init__.py
+-rw-r--r--   0        0        0     4425 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/contracts/accept_contract.py
+-rw-r--r--   0        0        0     5022 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/contracts/deliver_contract.py
+-rw-r--r--   0        0        0     4437 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/contracts/fulfill_contract.py
+-rw-r--r--   0        0        0     4420 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/contracts/get_contract.py
+-rw-r--r--   0        0        0     4900 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/contracts/get_contracts.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:23:43.777117 spacetraders-0.3.0/spacetraders/api/default/__init__.py
+-rw-r--r--   0        0        0     6960 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/default/register.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:23:43.817117 spacetraders-0.3.0/spacetraders/api/factions/__init__.py
+-rw-r--r--   0        0        0     4427 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/factions/get_faction.py
+-rw-r--r--   0        0        0     4853 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/factions/get_factions.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:23:43.827117 spacetraders-0.3.0/spacetraders/api/fleet/__init__.py
+-rw-r--r--   0        0        0     4900 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/fleet/create_chart.py
+-rw-r--r--   0        0        0     4550 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/fleet/create_ship_ship_scan.py
+-rw-r--r--   0        0        0     4587 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/create_ship_system_scan.py
+-rw-r--r--   0        0        0     4615 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/fleet/create_ship_waypoint_scan.py
+-rw-r--r--   0        0        0     5382 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/create_survey.py
+-rw-r--r--   0        0        0     4961 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/dock_ship.py
+-rw-r--r--   0        0        0     5217 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/extract_resources.py
+-rw-r--r--   0        0        0     4373 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/fleet/get_my_ship.py
+-rw-r--r--   0        0        0     4447 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/get_my_ship_cargo.py
+-rw-r--r--   0        0        0     4871 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/get_my_ships.py
+-rw-r--r--   0        0        0     5562 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/get_ship_cooldown.py
+-rw-r--r--   0        0        0     4414 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/fleet/get_ship_nav.py
+-rw-r--r--   0        0        0     4905 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/jettison.py
+-rw-r--r--   0        0        0     5049 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/jump_ship.py
+-rw-r--r--   0        0        0     5893 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/navigate_ship.py
+-rw-r--r--   0        0        0     4954 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/fleet/orbit_ship.py
+-rw-r--r--   0        0        0     5001 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/patch_ship_nav.py
+-rw-r--r--   0        0        0     5192 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/purchase_cargo.py
+-rw-r--r--   0        0        0     4680 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/purchase_ship.py
+-rw-r--r--   0        0        0     4419 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/refuel_ship.py
+-rw-r--r--   0        0        0     5010 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/sell_cargo.py
+-rw-r--r--   0        0        0     5244 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/ship_refine.py
+-rw-r--r--   0        0        0     5215 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/transfer_cargo.py
+-rw-r--r--   0        0        0     5569 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/fleet/warp_ship.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:23:43.807117 spacetraders-0.3.0/spacetraders/api/systems/__init__.py
+-rw-r--r--   0        0        0     4735 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/systems/get_jump_gate.py
+-rw-r--r--   0        0        0     5121 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/systems/get_market.py
+-rw-r--r--   0        0        0     4721 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/systems/get_shipyard.py
+-rw-r--r--   0        0        0     4469 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/systems/get_system.py
+-rw-r--r--   0        0        0     5421 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/api/systems/get_system_waypoints.py
+-rw-r--r--   0        0        0     4877 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/systems/get_systems.py
+-rw-r--r--   0        0        0     4710 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/api/systems/get_waypoint.py
+-rw-r--r--   0        0        0     4384 2023-05-13 04:23:44.617117 spacetraders-0.3.0/spacetraders/client.py
+-rw-r--r--   0        0        0      470 2023-05-13 04:23:44.557117 spacetraders-0.3.0/spacetraders/errors.py
+-rw-r--r--   0        0        0    13081 2023-05-13 04:23:44.717117 spacetraders-0.3.0/spacetraders/models/__init__.py
+-rw-r--r--   0        0        0     1269 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/accept_contract_response_200.py
+-rw-r--r--   0        0        0     1299 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/accept_contract_response_200_data.py
+-rw-r--r--   0        0        0     1460 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/agent.py
+-rw-r--r--   0        0        0     1532 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/chart.py
+-rw-r--r--   0        0        0     1709 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/connected_system.py
+-rw-r--r--   0        0        0     1887 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/contract.py
+-rw-r--r--   0        0        0     1712 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/contract_deliver_good.py
+-rw-r--r--   0        0        0     1340 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/contract_payment.py
+-rw-r--r--   0        0        0     1567 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/contract_terms.py
+-rw-r--r--   0        0        0      201 2023-05-13 04:23:43.937117 spacetraders-0.3.0/spacetraders/models/contract_type.py
+-rw-r--r--   0        0        0     1691 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/cooldown.py
+-rw-r--r--   0        0        0     1251 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/create_chart_response_201.py
+-rw-r--r--   0        0        0     1469 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/create_chart_response_201_data.py
+-rw-r--r--   0        0        0     1304 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/create_ship_ship_scan_response_201.py
+-rw-r--r--   0        0        0     1425 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/create_ship_ship_scan_response_201_data.py
+-rw-r--r--   0        0        0     1316 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/create_ship_system_scan_response_201.py
+-rw-r--r--   0        0        0     1443 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/create_ship_system_scan_response_201_data.py
+-rw-r--r--   0        0        0     1328 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/create_ship_waypoint_scan_response_201.py
+-rw-r--r--   0        0        0     1461 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/create_ship_waypoint_scan_response_201_data.py
+-rw-r--r--   0        0        0     1257 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/create_survey_response_201.py
+-rw-r--r--   0        0        0     1398 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/create_survey_response_201_data.py
+-rw-r--r--   0        0        0     1284 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/deliver_contract_json_body.py
+-rw-r--r--   0        0        0     1275 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/deliver_contract_response_200.py
+-rw-r--r--   0        0        0     1318 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/deliver_contract_response_200_data.py
+-rw-r--r--   0        0        0     1292 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/dock_ship_dock_ship_200_response.py
+-rw-r--r--   0        0        0     1227 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/dock_ship_dock_ship_200_response_data.py
+-rw-r--r--   0        0        0     1368 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/extract_resources_json_body.py
+-rw-r--r--   0        0        0     1281 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/extract_resources_response_201.py
+-rw-r--r--   0        0        0     1532 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/extract_resources_response_201_data.py
+-rw-r--r--   0        0        0     1261 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/extraction.py
+-rw-r--r--   0        0        0     1250 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/extraction_yield.py
+-rw-r--r--   0        0        0     1457 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/faction.py
+-rw-r--r--   0        0        0     1421 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/faction_trait.py
+-rw-r--r--   0        0        0     2091 2023-05-13 04:23:44.017117 spacetraders-0.3.0/spacetraders/models/faction_trait_symbol.py
+-rw-r--r--   0        0        0     1275 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/fulfill_contract_response_200.py
+-rw-r--r--   0        0        0     1301 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/fulfill_contract_response_200_data.py
+-rw-r--r--   0        0        0     1175 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_contract_response_200.py
+-rw-r--r--   0        0        0     1282 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/get_contracts_response_200.py
+-rw-r--r--   0        0        0     1169 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/get_faction_response_200.py
+-rw-r--r--   0        0        0     1276 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/get_factions_response_200.py
+-rw-r--r--   0        0        0     1176 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/get_jump_gate_response_200.py
+-rw-r--r--   0        0        0     1163 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_market_response_200.py
+-rw-r--r--   0        0        0     1161 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/get_my_agent_response_200.py
+-rw-r--r--   0        0        0     1186 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_my_ship_cargo_response_200.py
+-rw-r--r--   0        0        0     1162 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_my_ship_response_200.py
+-rw-r--r--   0        0        0     1262 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_my_ships_response_200.py
+-rw-r--r--   0        0        0     1262 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/get_ship_cooldown_response_200.py
+-rw-r--r--   0        0        0     1210 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_ship_nav_response_200.py
+-rw-r--r--   0        0        0     1175 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_shipyard_response_200.py
+-rw-r--r--   0        0        0     1163 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/get_system_response_200.py
+-rw-r--r--   0        0        0     1294 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/get_system_waypoints_response_200.py
+-rw-r--r--   0        0        0     1270 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_systems_response_200.py
+-rw-r--r--   0        0        0     1266 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/get_waypoint_response_200.py
+-rw-r--r--   0        0        0     1177 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/jettison_json_body.py
+-rw-r--r--   0        0        0     1232 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/jettison_response_200.py
+-rw-r--r--   0        0        0     1185 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/jettison_response_200_data.py
+-rw-r--r--   0        0        0     1606 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/jump_gate.py
+-rw-r--r--   0        0        0     1168 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/jump_ship_json_body.py
+-rw-r--r--   0        0        0     1233 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/jump_ship_response_200.py
+-rw-r--r--   0        0        0     1462 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/jump_ship_response_200_data.py
+-rw-r--r--   0        0        0     2398 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/market.py
+-rw-r--r--   0        0        0     1880 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/market_trade_good.py
+-rw-r--r--   0        0        0      224 2023-05-13 04:23:43.937117 spacetraders-0.3.0/spacetraders/models/market_trade_good_supply.py
+-rw-r--r--   0        0        0     2109 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/market_transaction.py
+-rw-r--r--   0        0        0      170 2023-05-13 04:23:43.947117 spacetraders-0.3.0/spacetraders/models/market_transaction_type.py
+-rw-r--r--   0        0        0     1206 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/meta.py
+-rw-r--r--   0        0        0     1176 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/navigate_ship_json_body.py
+-rw-r--r--   0        0        0     1257 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/navigate_ship_response_200.py
+-rw-r--r--   0        0        0     1444 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/navigate_ship_response_200_data.py
+-rw-r--r--   0        0        0     1304 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/orbit_ship_orbit_ship_200_response.py
+-rw-r--r--   0        0        0     1231 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/orbit_ship_orbit_ship_200_response_data.py
+-rw-r--r--   0        0        0     1420 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/patch_ship_nav_json_body.py
+-rw-r--r--   0        0        0     1214 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/patch_ship_nav_response_200.py
+-rw-r--r--   0        0        0     1352 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/purchase_cargo_purchase_cargo_201_response.py
+-rw-r--r--   0        0        0     1484 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/purchase_cargo_purchase_cargo_201_response_data.py
+-rw-r--r--   0        0        0     1211 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/purchase_cargo_purchase_cargo_request.py
+-rw-r--r--   0        0        0     1333 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/purchase_ship_json_body.py
+-rw-r--r--   0        0        0     1257 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/purchase_ship_response_201.py
+-rw-r--r--   0        0        0     1447 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/purchase_ship_response_201_data.py
+-rw-r--r--   0        0        0     1245 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/refuel_ship_response_200.py
+-rw-r--r--   0        0        0     1397 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/refuel_ship_response_200_data.py
+-rw-r--r--   0        0        0     1419 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/register_json_body.py
+-rw-r--r--   0        0        0      244 2023-05-13 04:23:43.997117 spacetraders-0.3.0/spacetraders/models/register_json_body_faction.py
+-rw-r--r--   0        0        0     1232 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/register_response_201.py
+-rw-r--r--   0        0        0     1608 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/register_response_201_data.py
+-rw-r--r--   0        0        0     2444 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/scanned_ship.py
+-rw-r--r--   0        0        0     1144 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/scanned_ship_engine.py
+-rw-r--r--   0        0        0     1141 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/scanned_ship_frame.py
+-rw-r--r--   0        0        0     1149 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/scanned_ship_mounts_item.py
+-rw-r--r--   0        0        0     1147 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/scanned_ship_reactor.py
+-rw-r--r--   0        0        0     1492 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/scanned_system.py
+-rw-r--r--   0        0        0     2293 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/scanned_waypoint.py
+-rw-r--r--   0        0        0     1304 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/sell_cargo_sell_cargo_201_response.py
+-rw-r--r--   0        0        0     1468 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/sell_cargo_sell_cargo_201_response_data.py
+-rw-r--r--   0        0        0     1195 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/sell_cargo_sell_cargo_request.py
+-rw-r--r--   0        0        0     3140 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship.py
+-rw-r--r--   0        0        0     1484 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_cargo.py
+-rw-r--r--   0        0        0     1510 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_cargo_item.py
+-rw-r--r--   0        0        0     2248 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_crew.py
+-rw-r--r--   0        0        0      167 2023-05-13 04:23:43.907117 spacetraders-0.3.0/spacetraders/models/ship_crew_rotation.py
+-rw-r--r--   0        0        0     1883 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_engine.py
+-rw-r--r--   0        0        0      319 2023-05-13 04:23:43.997117 spacetraders-0.3.0/spacetraders/models/ship_engine_symbol.py
+-rw-r--r--   0        0        0     2278 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_frame.py
+-rw-r--r--   0        0        0      694 2023-05-13 04:23:43.927117 spacetraders-0.3.0/spacetraders/models/ship_frame_symbol.py
+-rw-r--r--   0        0        0     1586 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_fuel.py
+-rw-r--r--   0        0        0     1340 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_fuel_consumed.py
+-rw-r--r--   0        0        0     1965 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_module.py
+-rw-r--r--   0        0        0     1033 2023-05-13 04:23:43.947117 spacetraders-0.3.0/spacetraders/models/ship_module_symbol.py
+-rw-r--r--   0        0        0     1947 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_mount.py
+-rw-r--r--   0        0        0      572 2023-05-13 04:23:44.007117 spacetraders-0.3.0/spacetraders/models/ship_mount_deposits_item.py
+-rw-r--r--   0        0        0      854 2023-05-13 04:23:44.007117 spacetraders-0.3.0/spacetraders/models/ship_mount_symbol.py
+-rw-r--r--   0        0        0     2114 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_nav.py
+-rw-r--r--   0        0        0      206 2023-05-13 04:23:43.927117 spacetraders-0.3.0/spacetraders/models/ship_nav_flight_mode.py
+-rw-r--r--   0        0        0     1891 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_nav_route.py
+-rw-r--r--   0        0        0     1497 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_nav_route_waypoint.py
+-rw-r--r--   0        0        0      196 2023-05-13 04:23:43.947117 spacetraders-0.3.0/spacetraders/models/ship_nav_status.py
+-rw-r--r--   0        0        0     1934 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_reactor.py
+-rw-r--r--   0        0        0      344 2023-05-13 04:23:43.927117 spacetraders-0.3.0/spacetraders/models/ship_reactor_symbol.py
+-rw-r--r--   0        0        0     1246 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_refine_json_body.py
+-rw-r--r--   0        0        0      330 2023-05-13 04:23:43.997117 spacetraders-0.3.0/spacetraders/models/ship_refine_json_body_produce.py
+-rw-r--r--   0        0        0     1316 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_refine_ship_refine_200_response.py
+-rw-r--r--   0        0        0     2047 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_refine_ship_refine_200_response_data.py
+-rw-r--r--   0        0        0     1344 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_refine_ship_refine_200_response_data_consumed_item.py
+-rw-r--r--   0        0        0     1344 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_refine_ship_refine_200_response_data_produced_item.py
+-rw-r--r--   0        0        0     1530 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/ship_registration.py
+-rw-r--r--   0        0        0     1541 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/ship_requirements.py
+-rw-r--r--   0        0        0      479 2023-05-13 04:23:43.987117 spacetraders-0.3.0/spacetraders/models/ship_role.py
+-rw-r--r--   0        0        0      549 2023-05-13 04:23:43.917117 spacetraders-0.3.0/spacetraders/models/ship_type.py
+-rw-r--r--   0        0        0     2009 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/shipyard.py
+-rw-r--r--   0        0        0     2498 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/shipyard_ship.py
+-rw-r--r--   0        0        0     1225 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/shipyard_ship_types_item.py
+-rw-r--r--   0        0        0     1698 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/shipyard_transaction.py
+-rw-r--r--   0        0        0     2228 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/survey.py
+-rw-r--r--   0        0        0     1209 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/survey_deposit.py
+-rw-r--r--   0        0        0      181 2023-05-13 04:23:43.927117 spacetraders-0.3.0/spacetraders/models/survey_size.py
+-rw-r--r--   0        0        0     1725 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/system.py
+-rw-r--r--   0        0        0     1112 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/system_faction.py
+-rw-r--r--   0        0        0      405 2023-05-13 04:23:43.927117 spacetraders-0.3.0/spacetraders/models/system_type.py
+-rw-r--r--   0        0        0     1352 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/system_waypoint.py
+-rw-r--r--   0        0        0     1299 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/trade_good.py
+-rw-r--r--   0        0        0     4422 2023-05-13 04:23:43.987117 spacetraders-0.3.0/spacetraders/models/trade_symbol.py
+-rw-r--r--   0        0        0     1352 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/transfer_cargo_transfer_cargo_200_response.py
+-rw-r--r--   0        0        0     1221 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/transfer_cargo_transfer_cargo_200_response_data.py
+-rw-r--r--   0        0        0     1304 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/transfer_cargo_transfer_cargo_request.py
+-rw-r--r--   0        0        0     1168 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/warp_ship_json_body.py
+-rw-r--r--   0        0        0     1233 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/warp_ship_response_200.py
+-rw-r--r--   0        0        0     1436 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/warp_ship_response_200_data.py
+-rw-r--r--   0        0        0     2279 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/waypoint.py
+-rw-r--r--   0        0        0     1116 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/waypoint_faction.py
+-rw-r--r--   0        0        0     1178 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/models/waypoint_orbital.py
+-rw-r--r--   0        0        0     1427 2023-05-13 04:23:44.997117 spacetraders-0.3.0/spacetraders/models/waypoint_trait.py
+-rw-r--r--   0        0        0     2200 2023-05-13 04:23:44.017117 spacetraders-0.3.0/spacetraders/models/waypoint_trait_symbol.py
+-rw-r--r--   0        0        0      381 2023-05-13 04:23:43.927117 spacetraders-0.3.0/spacetraders/models/waypoint_type.py
+-rw-r--r--   0        0        0     1341 2023-05-13 04:23:45.007117 spacetraders-0.3.0/spacetraders/types.py
+-rw-r--r--   0        0        0     4031 1970-01-01 00:00:00.000000 spacetraders-0.3.0/PKG-INFO
```

### Comparing `spacetraders-0.2.4/README.md` & `spacetraders-0.3.0/README.md`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/api/agents/get_my_agent.py` & `spacetraders-0.3.0/spacetraders/api/agents/get_my_agent.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,16 +1,17 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.get_my_agent_response_200 import GetMyAgentResponse200
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
     url = "{}/my/agent".format(_client.base_url)
@@ -51,14 +52,15 @@
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[GetMyAgentResponse200]:
     """My Agent Details
 
      Fetch your agent's details.
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
@@ -73,41 +75,45 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetMyAgentResponse200]:
-    """My Agent Details
-
-     Fetch your agent's details.
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        GetMyAgentResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[GetMyAgentResponse200]:
     """My Agent Details
 
      Fetch your agent's details.
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
@@ -120,31 +126,32 @@
     kwargs = _get_kwargs(
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetMyAgentResponse200]:
-    """My Agent Details
-
-     Fetch your agent's details.
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMyAgentResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/contracts/accept_contract.py` & `spacetraders-0.3.0/spacetraders/api/contracts/get_contract.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,173 +1,170 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.accept_contract_response_200 import AcceptContractResponse200
-from ...types import UNSET, Response
+from ...models.get_contract_response_200 import GetContractResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
-    url = "{}/my/contracts/{contractId}/accept".format(
+    url = "{}/my/contracts/{contractId}".format(
         _client.base_url, contractId=contract_id
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     return {
-        "method": "post",
+        "method": "get",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[AcceptContractResponse200]:
+) -> Optional[GetContractResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = AcceptContractResponse200(**response.json())
+        response_200 = GetContractResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[AcceptContractResponse200]:
+) -> Response[GetContractResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[AcceptContractResponse200]:
-    """Accept Contract
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetContractResponse200]:
+    """Get Contract
 
-     Accept a contract.
+     Get the details of a contract by ID.
 
     Args:
         contract_id (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[AcceptContractResponse200]
+        Response[GetContractResponse200]
     """
 
     kwargs = _get_kwargs(
         contract_id=contract_id,
         _client=_client,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    contract_id: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[AcceptContractResponse200]:
-    """Accept Contract
-
-     Accept a contract.
-
-    Args:
-        contract_id (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        AcceptContractResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        contract_id=contract_id,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[AcceptContractResponse200]:
-    """Accept Contract
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetContractResponse200]:
+    """Get Contract
 
-     Accept a contract.
+     Get the details of a contract by ID.
 
     Args:
         contract_id (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[AcceptContractResponse200]
+        Response[GetContractResponse200]
     """
 
     kwargs = _get_kwargs(
         contract_id=contract_id,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
+    resp = _build_response(client=_client, response=response)
 
-async def asyncio(
-    contract_id: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[AcceptContractResponse200]:
-    """Accept Contract
-
-     Accept a contract.
-
-    Args:
-        contract_id (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        AcceptContractResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            contract_id=contract_id,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/contracts/deliver_contract.py` & `spacetraders-0.3.0/spacetraders/api/fleet/extract_resources.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,27 +1,28 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.deliver_contract_json_body import DeliverContractJsonBody
-from ...models.deliver_contract_response_200 import DeliverContractResponse200
-from ...types import UNSET, Response
+from ...models.extract_resources_json_body import ExtractResourcesJsonBody
+from ...models.extract_resources_response_201 import ExtractResourcesResponse201
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
-    contract_id: str,
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    json_body: DeliverContractJsonBody,
+    json_body: ExtractResourcesJsonBody,
 ) -> Dict[str, Any]:
-    url = "{}/my/contracts/{contractId}/deliver".format(
-        _client.base_url, contractId=contract_id
+    url = "{}/my/ships/{shipSymbol}/extract".format(
+        _client.base_url, shipSymbol=ship_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     json_json_body = json_body.dict(by_alias=True)
 
@@ -34,161 +35,153 @@
         "follow_redirects": _client.follow_redirects,
         "json": json_json_body,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[DeliverContractResponse200]:
-    if response.status_code == HTTPStatus.OK:
-        response_200 = DeliverContractResponse200(**response.json())
+) -> Optional[ExtractResourcesResponse201]:
+    if response.status_code == HTTPStatus.CREATED:
+        response_201 = ExtractResourcesResponse201(**response.json())
 
-        return response_200
+        return response_201
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[DeliverContractResponse200]:
+) -> Response[ExtractResourcesResponse201]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
-    contract_id: str,
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: DeliverContractJsonBody,
-) -> Response[DeliverContractResponse200]:
-    """Deliver Contract
+    raise_on_error: Optional[bool] = None,
+    **json_body: ExtractResourcesJsonBody,
+) -> Response[ExtractResourcesResponse201]:
+    """Extract Resources
 
-     Deliver cargo on a given contract.
+     Extract resources from the waypoint into your ship. Send an optional survey as the payload to target
+    specific yields.
 
     Args:
-        contract_id (str):
-        json_body (DeliverContractJsonBody):
+        ship_symbol (str):
+        json_body (ExtractResourcesJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[DeliverContractResponse200]
+        Response[ExtractResourcesResponse201]
     """
 
-    json_body = DeliverContractJsonBody.parse_obj(json_body)
+    json_body = ExtractResourcesJsonBody.parse_obj(json_body)
 
     kwargs = _get_kwargs(
-        contract_id=contract_id,
+        ship_symbol=ship_symbol,
         _client=_client,
         json_body=json_body,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    contract_id: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: DeliverContractJsonBody,
-) -> Optional[DeliverContractResponse200]:
-    """Deliver Contract
-
-     Deliver cargo on a given contract.
-
-    Args:
-        contract_id (str):
-        json_body (DeliverContractJsonBody):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        DeliverContractResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        contract_id=contract_id,
-        _client=_client,
-        json_body=json_body,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
-    contract_id: str,
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: DeliverContractJsonBody,
-) -> Response[DeliverContractResponse200]:
-    """Deliver Contract
+    raise_on_error: Optional[bool] = None,
+    **json_body: ExtractResourcesJsonBody,
+) -> Response[ExtractResourcesResponse201]:
+    """Extract Resources
 
-     Deliver cargo on a given contract.
+     Extract resources from the waypoint into your ship. Send an optional survey as the payload to target
+    specific yields.
 
     Args:
-        contract_id (str):
-        json_body (DeliverContractJsonBody):
+        ship_symbol (str):
+        json_body (ExtractResourcesJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[DeliverContractResponse200]
+        Response[ExtractResourcesResponse201]
     """
 
-    json_body = DeliverContractJsonBody.parse_obj(json_body)
+    json_body = ExtractResourcesJsonBody.parse_obj(json_body)
 
     kwargs = _get_kwargs(
-        contract_id=contract_id,
+        ship_symbol=ship_symbol,
         _client=_client,
         json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    contract_id: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: DeliverContractJsonBody,
-) -> Optional[DeliverContractResponse200]:
-    """Deliver Contract
-
-     Deliver cargo on a given contract.
-
-    Args:
-        contract_id (str):
-        json_body (DeliverContractJsonBody):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        DeliverContractResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            contract_id=contract_id,
-            _client=_client,
-            json_body=json_body,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/contracts/fulfill_contract.py` & `spacetraders-0.3.0/spacetraders/api/contracts/fulfill_contract.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,16 +1,17 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.fulfill_contract_response_200 import FulfillContractResponse200
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
@@ -55,14 +56,15 @@
     )
 
 
 def sync_detailed(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[FulfillContractResponse200]:
     """Fulfill Contract
 
      Fulfill a contract
 
     Args:
         contract_id (str):
@@ -81,47 +83,46 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    contract_id: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[FulfillContractResponse200]:
-    """Fulfill Contract
-
-     Fulfill a contract
-
-    Args:
-        contract_id (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        FulfillContractResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        contract_id=contract_id,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[FulfillContractResponse200]:
     """Fulfill Contract
 
      Fulfill a contract
 
     Args:
         contract_id (str):
@@ -138,36 +139,32 @@
         contract_id=contract_id,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    contract_id: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[FulfillContractResponse200]:
-    """Fulfill Contract
-
-     Fulfill a contract
-
-    Args:
-        contract_id (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        FulfillContractResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            contract_id=contract_id,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/contracts/get_contract.py` & `spacetraders-0.3.0/spacetraders/api/contracts/accept_contract.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,173 +1,170 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_contract_response_200 import GetContractResponse200
-from ...types import UNSET, Response
+from ...models.accept_contract_response_200 import AcceptContractResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
-    url = "{}/my/contracts/{contractId}".format(
+    url = "{}/my/contracts/{contractId}/accept".format(
         _client.base_url, contractId=contract_id
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     return {
-        "method": "get",
+        "method": "post",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetContractResponse200]:
+) -> Optional[AcceptContractResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetContractResponse200(**response.json())
+        response_200 = AcceptContractResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetContractResponse200]:
+) -> Response[AcceptContractResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetContractResponse200]:
-    """Get Contract
+    raise_on_error: Optional[bool] = None,
+) -> Response[AcceptContractResponse200]:
+    """Accept Contract
 
-     Get the details of a contract by ID.
+     Accept a contract.
 
     Args:
         contract_id (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetContractResponse200]
+        Response[AcceptContractResponse200]
     """
 
     kwargs = _get_kwargs(
         contract_id=contract_id,
         _client=_client,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    contract_id: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetContractResponse200]:
-    """Get Contract
-
-     Get the details of a contract by ID.
-
-    Args:
-        contract_id (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        GetContractResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        contract_id=contract_id,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     contract_id: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetContractResponse200]:
-    """Get Contract
+    raise_on_error: Optional[bool] = None,
+) -> Response[AcceptContractResponse200]:
+    """Accept Contract
 
-     Get the details of a contract by ID.
+     Accept a contract.
 
     Args:
         contract_id (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetContractResponse200]
+        Response[AcceptContractResponse200]
     """
 
     kwargs = _get_kwargs(
         contract_id=contract_id,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
+    resp = _build_response(client=_client, response=response)
 
-async def asyncio(
-    contract_id: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetContractResponse200]:
-    """Get Contract
-
-     Get the details of a contract by ID.
-
-    Args:
-        contract_id (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetContractResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            contract_id=contract_id,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/contracts/get_contracts.py` & `spacetraders-0.3.0/spacetraders/api/contracts/get_contracts.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,16 +1,17 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional, Union
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.get_contracts_response_200 import GetContractsResponse200
-from ...types import UNSET, Response, Unset
+from ...types import UNSET, ApiError, Error, Response, Unset
 
 
 def _get_kwargs(
     *,
     _client: AuthenticatedClient,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
@@ -61,14 +62,15 @@
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
 ) -> Response[GetContractsResponse200]:
     """List Contracts
 
      List all of your contracts.
 
@@ -91,49 +93,45 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    *,
-    _client: AuthenticatedClient,
-    page: Union[Unset, None, int] = UNSET,
-    limit: Union[Unset, None, int] = UNSET,
-) -> Optional[GetContractsResponse200]:
-    """List Contracts
-
-     List all of your contracts.
-
-    Args:
-        page (Union[Unset, None, int]):
-        limit (Union[Unset, None, int]):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    Returns:
-        GetContractsResponse200
-    """
-
-    return sync_detailed(
-        _client=_client,
-        page=page,
-        limit=limit,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
 ) -> Response[GetContractsResponse200]:
     """List Contracts
 
      List all of your contracts.
 
@@ -154,39 +152,32 @@
         page=page,
         limit=limit,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    *,
-    _client: AuthenticatedClient,
-    page: Union[Unset, None, int] = UNSET,
-    limit: Union[Unset, None, int] = UNSET,
-) -> Optional[GetContractsResponse200]:
-    """List Contracts
-
-     List all of your contracts.
+    resp = _build_response(client=_client, response=response)
 
-    Args:
-        page (Union[Unset, None, int]):
-        limit (Union[Unset, None, int]):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetContractsResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            _client=_client,
-            page=page,
-            limit=limit,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/factions/get_faction.py` & `spacetraders-0.3.0/spacetraders/api/fleet/get_ship_nav.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,25 +1,26 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_faction_response_200 import GetFactionResponse200
-from ...types import UNSET, Response
+from ...models.get_ship_nav_response_200 import GetShipNavResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
-    faction_symbol: str = "CGR",
+    ship_symbol: str,
     *,
-    _client: Client,
+    _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
-    url = "{}/factions/{factionSymbol}".format(
-        _client.base_url, factionSymbol=faction_symbol
+    url = "{}/my/ships/{shipSymbol}/nav".format(
+        _client.base_url, shipSymbol=ship_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     return {
         "method": "get",
@@ -29,145 +30,141 @@
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetFactionResponse200]:
+) -> Optional[GetShipNavResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetFactionResponse200(**response.json())
+        response_200 = GetShipNavResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetFactionResponse200]:
+) -> Response[GetShipNavResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
-    faction_symbol: str = "CGR",
+    ship_symbol: str,
     *,
-    _client: Client,
-) -> Response[GetFactionResponse200]:
-    """Get Faction
+    _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetShipNavResponse200]:
+    """Get Ship Nav
 
-     View the details of a faction.
+     Get the current nav status of a ship.
 
     Args:
-        faction_symbol (str):  Default: 'CGR'.
+        ship_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetFactionResponse200]
+        Response[GetShipNavResponse200]
     """
 
     kwargs = _get_kwargs(
-        faction_symbol=faction_symbol,
+        ship_symbol=ship_symbol,
         _client=_client,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    faction_symbol: str = "CGR",
-    *,
-    _client: Client,
-) -> Optional[GetFactionResponse200]:
-    """Get Faction
-
-     View the details of a faction.
-
-    Args:
-        faction_symbol (str):  Default: 'CGR'.
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        GetFactionResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        faction_symbol=faction_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
-    faction_symbol: str = "CGR",
+    ship_symbol: str,
     *,
-    _client: Client,
-) -> Response[GetFactionResponse200]:
-    """Get Faction
+    _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetShipNavResponse200]:
+    """Get Ship Nav
 
-     View the details of a faction.
+     Get the current nav status of a ship.
 
     Args:
-        faction_symbol (str):  Default: 'CGR'.
+        ship_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetFactionResponse200]
+        Response[GetShipNavResponse200]
     """
 
     kwargs = _get_kwargs(
-        faction_symbol=faction_symbol,
+        ship_symbol=ship_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    faction_symbol: str = "CGR",
-    *,
-    _client: Client,
-) -> Optional[GetFactionResponse200]:
-    """Get Faction
-
-     View the details of a faction.
-
-    Args:
-        faction_symbol (str):  Default: 'CGR'.
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetFactionResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            faction_symbol=faction_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/factions/get_factions.py` & `spacetraders-0.3.0/spacetraders/api/fleet/get_my_ships.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,25 +1,26 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional, Union
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_factions_response_200 import GetFactionsResponse200
-from ...types import UNSET, Response, Unset
+from ...models.get_my_ships_response_200 import GetMyShipsResponse200
+from ...types import UNSET, ApiError, Error, Response, Unset
 
 
 def _get_kwargs(
     *,
-    _client: Client,
+    _client: AuthenticatedClient,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
 ) -> Dict[str, Any]:
-    url = "{}/factions".format(_client.base_url)
+    url = "{}/my/ships".format(_client.base_url)
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     params: Dict[str, Any] = {}
     params["page"] = page
 
@@ -36,157 +37,147 @@
         "follow_redirects": _client.follow_redirects,
         "params": params,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetFactionsResponse200]:
+) -> Optional[GetMyShipsResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetFactionsResponse200(**response.json())
+        response_200 = GetMyShipsResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetFactionsResponse200]:
+) -> Response[GetMyShipsResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     *,
-    _client: Client,
+    _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
-) -> Response[GetFactionsResponse200]:
-    """List Factions
+) -> Response[GetMyShipsResponse200]:
+    """List Ships
 
-     List all discovered factions in the game.
+     Retrieve all of your ships.
 
     Args:
         page (Union[Unset, None, int]):
         limit (Union[Unset, None, int]):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetFactionsResponse200]
+        Response[GetMyShipsResponse200]
     """
 
     kwargs = _get_kwargs(
         _client=_client,
         page=page,
         limit=limit,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    *,
-    _client: Client,
-    page: Union[Unset, None, int] = UNSET,
-    limit: Union[Unset, None, int] = UNSET,
-) -> Optional[GetFactionsResponse200]:
-    """List Factions
-
-     List all discovered factions in the game.
-
-    Args:
-        page (Union[Unset, None, int]):
-        limit (Union[Unset, None, int]):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        GetFactionsResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        _client=_client,
-        page=page,
-        limit=limit,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     *,
-    _client: Client,
+    _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
-) -> Response[GetFactionsResponse200]:
-    """List Factions
+) -> Response[GetMyShipsResponse200]:
+    """List Ships
 
-     List all discovered factions in the game.
+     Retrieve all of your ships.
 
     Args:
         page (Union[Unset, None, int]):
         limit (Union[Unset, None, int]):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetFactionsResponse200]
+        Response[GetMyShipsResponse200]
     """
 
     kwargs = _get_kwargs(
         _client=_client,
         page=page,
         limit=limit,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    *,
-    _client: Client,
-    page: Union[Unset, None, int] = UNSET,
-    limit: Union[Unset, None, int] = UNSET,
-) -> Optional[GetFactionsResponse200]:
-    """List Factions
-
-     List all discovered factions in the game.
+    resp = _build_response(client=_client, response=response)
 
-    Args:
-        page (Union[Unset, None, int]):
-        limit (Union[Unset, None, int]):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetFactionsResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            _client=_client,
-            page=page,
-            limit=limit,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/create_chart.py` & `spacetraders-0.3.0/spacetraders/api/fleet/create_chart.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,16 +1,17 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.create_chart_response_201 import CreateChartResponse201
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
@@ -55,14 +56,15 @@
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[CreateChartResponse201]:
     """Create Chart
 
      Command a ship to chart the current waypoint.
 
     Waypoints in the universe are uncharted by default. These locations will not show up in the API
     until they have been charted by a ship.
@@ -86,52 +88,46 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[CreateChartResponse201]:
-    """Create Chart
-
-     Command a ship to chart the current waypoint.
-
-    Waypoints in the universe are uncharted by default. These locations will not show up in the API
-    until they have been charted by a ship.
-
-    Charting a location will record your agent as the one who created the chart.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        CreateChartResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[CreateChartResponse201]:
     """Create Chart
 
      Command a ship to chart the current waypoint.
 
     Waypoints in the universe are uncharted by default. These locations will not show up in the API
     until they have been charted by a ship.
@@ -153,41 +149,32 @@
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[CreateChartResponse201]:
-    """Create Chart
-
-     Command a ship to chart the current waypoint.
-
-    Waypoints in the universe are uncharted by default. These locations will not show up in the API
-    until they have been charted by a ship.
+    resp = _build_response(client=_client, response=response)
 
-    Charting a location will record your agent as the one who created the chart.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        CreateChartResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/create_ship_ship_scan.py` & `spacetraders-0.3.0/spacetraders/api/fleet/create_ship_ship_scan.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,16 +1,17 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.create_ship_ship_scan_response_201 import CreateShipShipScanResponse201
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
@@ -55,14 +56,15 @@
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[CreateShipShipScanResponse201]:
     """Scan Ships
 
      Activate your ship's sensor arrays to scan for ship information.
 
     Args:
         ship_symbol (str):
@@ -81,47 +83,46 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[CreateShipShipScanResponse201]:
-    """Scan Ships
-
-     Activate your ship's sensor arrays to scan for ship information.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        CreateShipShipScanResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[CreateShipShipScanResponse201]:
     """Scan Ships
 
      Activate your ship's sensor arrays to scan for ship information.
 
     Args:
         ship_symbol (str):
@@ -138,36 +139,32 @@
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[CreateShipShipScanResponse201]:
-    """Scan Ships
-
-     Activate your ship's sensor arrays to scan for ship information.
-
-    Args:
-        ship_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        CreateShipShipScanResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/create_ship_system_scan.py` & `spacetraders-0.3.0/spacetraders/api/fleet/get_my_ship_cargo.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,175 +1,170 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.create_ship_system_scan_response_201 import (
-    CreateShipSystemScanResponse201,
-)
-from ...types import UNSET, Response
+from ...models.get_my_ship_cargo_response_200 import GetMyShipCargoResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}/scan/systems".format(
+    url = "{}/my/ships/{shipSymbol}/cargo".format(
         _client.base_url, shipSymbol=ship_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     return {
-        "method": "post",
+        "method": "get",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[CreateShipSystemScanResponse201]:
-    if response.status_code == HTTPStatus.CREATED:
-        response_201 = CreateShipSystemScanResponse201(**response.json())
+) -> Optional[GetMyShipCargoResponse200]:
+    if response.status_code == HTTPStatus.OK:
+        response_200 = GetMyShipCargoResponse200(**response.json())
 
-        return response_201
+        return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[CreateShipSystemScanResponse201]:
+) -> Response[GetMyShipCargoResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[CreateShipSystemScanResponse201]:
-    """Scan Systems
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetMyShipCargoResponse200]:
+    """Get Ship Cargo
 
-     Activate your ship's sensor arrays to scan for system information.
+     Retrieve the cargo of your ship.
 
     Args:
         ship_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[CreateShipSystemScanResponse201]
+        Response[GetMyShipCargoResponse200]
     """
 
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[CreateShipSystemScanResponse201]:
-    """Scan Systems
-
-     Activate your ship's sensor arrays to scan for system information.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        CreateShipSystemScanResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[CreateShipSystemScanResponse201]:
-    """Scan Systems
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetMyShipCargoResponse200]:
+    """Get Ship Cargo
 
-     Activate your ship's sensor arrays to scan for system information.
+     Retrieve the cargo of your ship.
 
     Args:
         ship_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[CreateShipSystemScanResponse201]
+        Response[GetMyShipCargoResponse200]
     """
 
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
+    resp = _build_response(client=_client, response=response)
 
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[CreateShipSystemScanResponse201]:
-    """Scan Systems
-
-     Activate your ship's sensor arrays to scan for system information.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        CreateShipSystemScanResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/create_ship_waypoint_scan.py` & `spacetraders-0.3.0/spacetraders/api/fleet/create_ship_waypoint_scan.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,18 +1,19 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.create_ship_waypoint_scan_response_201 import (
     CreateShipWaypointScanResponse201,
 )
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
@@ -57,14 +58,15 @@
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[CreateShipWaypointScanResponse201]:
     """Scan Waypoints
 
      Activate your ship's sensor arrays to scan for waypoint information.
 
     Args:
         ship_symbol (str):
@@ -83,47 +85,46 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[CreateShipWaypointScanResponse201]:
-    """Scan Waypoints
-
-     Activate your ship's sensor arrays to scan for waypoint information.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        CreateShipWaypointScanResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[CreateShipWaypointScanResponse201]:
     """Scan Waypoints
 
      Activate your ship's sensor arrays to scan for waypoint information.
 
     Args:
         ship_symbol (str):
@@ -140,36 +141,32 @@
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[CreateShipWaypointScanResponse201]:
-    """Scan Waypoints
-
-     Activate your ship's sensor arrays to scan for waypoint information.
-
-    Args:
-        ship_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        CreateShipWaypointScanResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/dock_ship.py` & `spacetraders-0.3.0/spacetraders/api/fleet/dock_ship.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,16 +1,17 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.dock_ship_dock_ship_200_response import DockShipDockShip200Response
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
@@ -55,14 +56,15 @@
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[DockShipDockShip200Response]:
     """Dock Ship
 
      Attempt to dock your ship at it's current location. Docking will only succeed if the waypoint is a
     dockable location, and your ship is capable of docking at the time of the request.
 
     The endpoint is idempotent - successive calls will succeed even if the ship is already docked.
@@ -84,50 +86,46 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[DockShipDockShip200Response]:
-    """Dock Ship
-
-     Attempt to dock your ship at it's current location. Docking will only succeed if the waypoint is a
-    dockable location, and your ship is capable of docking at the time of the request.
-
-    The endpoint is idempotent - successive calls will succeed even if the ship is already docked.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        DockShipDockShip200Response
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[DockShipDockShip200Response]:
     """Dock Ship
 
      Attempt to dock your ship at it's current location. Docking will only succeed if the waypoint is a
     dockable location, and your ship is capable of docking at the time of the request.
 
     The endpoint is idempotent - successive calls will succeed even if the ship is already docked.
@@ -147,39 +145,32 @@
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[DockShipDockShip200Response]:
-    """Dock Ship
-
-     Attempt to dock your ship at it's current location. Docking will only succeed if the waypoint is a
-    dockable location, and your ship is capable of docking at the time of the request.
+    resp = _build_response(client=_client, response=response)
 
-    The endpoint is idempotent - successive calls will succeed even if the ship is already docked.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        DockShipDockShip200Response
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/extract_resources.py` & `spacetraders-0.3.0/spacetraders/api/fleet/jettison.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,26 +1,27 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.extract_resources_json_body import ExtractResourcesJsonBody
-from ...models.extract_resources_response_201 import ExtractResourcesResponse201
-from ...types import UNSET, Response
+from ...models.jettison_json_body import JettisonJsonBody
+from ...models.jettison_response_200 import JettisonResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    json_body: ExtractResourcesJsonBody,
+    json_body: JettisonJsonBody,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}/extract".format(
+    url = "{}/my/ships/{shipSymbol}/jettison".format(
         _client.base_url, shipSymbol=ship_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     json_json_body = json_body.dict(by_alias=True)
@@ -34,165 +35,151 @@
         "follow_redirects": _client.follow_redirects,
         "json": json_json_body,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[ExtractResourcesResponse201]:
-    if response.status_code == HTTPStatus.CREATED:
-        response_201 = ExtractResourcesResponse201(**response.json())
+) -> Optional[JettisonResponse200]:
+    if response.status_code == HTTPStatus.OK:
+        response_200 = JettisonResponse200(**response.json())
 
-        return response_201
+        return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[ExtractResourcesResponse201]:
+) -> Response[JettisonResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: ExtractResourcesJsonBody,
-) -> Response[ExtractResourcesResponse201]:
-    """Extract Resources
+    raise_on_error: Optional[bool] = None,
+    **json_body: JettisonJsonBody,
+) -> Response[JettisonResponse200]:
+    """Jettison Cargo
 
-     Extract resources from the waypoint into your ship. Send an optional survey as the payload to target
-    specific yields.
+     Jettison cargo from your ship's cargo hold.
 
     Args:
         ship_symbol (str):
-        json_body (ExtractResourcesJsonBody):
+        json_body (JettisonJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[ExtractResourcesResponse201]
+        Response[JettisonResponse200]
     """
 
-    json_body = ExtractResourcesJsonBody.parse_obj(json_body)
+    json_body = JettisonJsonBody.parse_obj(json_body)
 
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
         json_body=json_body,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: ExtractResourcesJsonBody,
-) -> Optional[ExtractResourcesResponse201]:
-    """Extract Resources
-
-     Extract resources from the waypoint into your ship. Send an optional survey as the payload to target
-    specific yields.
-
-    Args:
-        ship_symbol (str):
-        json_body (ExtractResourcesJsonBody):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        ExtractResourcesResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-        json_body=json_body,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: ExtractResourcesJsonBody,
-) -> Response[ExtractResourcesResponse201]:
-    """Extract Resources
+    raise_on_error: Optional[bool] = None,
+    **json_body: JettisonJsonBody,
+) -> Response[JettisonResponse200]:
+    """Jettison Cargo
 
-     Extract resources from the waypoint into your ship. Send an optional survey as the payload to target
-    specific yields.
+     Jettison cargo from your ship's cargo hold.
 
     Args:
         ship_symbol (str):
-        json_body (ExtractResourcesJsonBody):
+        json_body (JettisonJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[ExtractResourcesResponse201]
+        Response[JettisonResponse200]
     """
 
-    json_body = ExtractResourcesJsonBody.parse_obj(json_body)
+    json_body = JettisonJsonBody.parse_obj(json_body)
 
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
         json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: ExtractResourcesJsonBody,
-) -> Optional[ExtractResourcesResponse201]:
-    """Extract Resources
-
-     Extract resources from the waypoint into your ship. Send an optional survey as the payload to target
-    specific yields.
-
-    Args:
-        ship_symbol (str):
-        json_body (ExtractResourcesJsonBody):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        ExtractResourcesResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
-            json_body=json_body,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/get_my_ship.py` & `spacetraders-0.3.0/spacetraders/api/fleet/patch_ship_nav.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,171 +1,185 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_my_ship_response_200 import GetMyShipResponse200
-from ...types import UNSET, Response
+from ...models.patch_ship_nav_json_body import PatchShipNavJsonBody
+from ...models.patch_ship_nav_response_200 import PatchShipNavResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    json_body: PatchShipNavJsonBody,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}".format(_client.base_url, shipSymbol=ship_symbol)
+    url = "{}/my/ships/{shipSymbol}/nav".format(
+        _client.base_url, shipSymbol=ship_symbol
+    )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
+    json_json_body = json_body.dict(by_alias=True)
+
     return {
-        "method": "get",
+        "method": "patch",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
+        "json": json_json_body,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetMyShipResponse200]:
+) -> Optional[PatchShipNavResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetMyShipResponse200(**response.json())
+        response_200 = PatchShipNavResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetMyShipResponse200]:
+) -> Response[PatchShipNavResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetMyShipResponse200]:
-    """Get Ship
+    raise_on_error: Optional[bool] = None,
+    **json_body: PatchShipNavJsonBody,
+) -> Response[PatchShipNavResponse200]:
+    """Patch Ship Nav
 
-     Retrieve the details of your ship.
+     Update the nav data of a ship, such as the flight mode.
 
     Args:
         ship_symbol (str):
+        json_body (PatchShipNavJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetMyShipResponse200]
+        Response[PatchShipNavResponse200]
     """
 
+    json_body = PatchShipNavJsonBody.parse_obj(json_body)
+
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
+        json_body=json_body,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
-
-
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetMyShipResponse200]:
-    """Get Ship
-
-     Retrieve the details of your ship.
-
-    Args:
-        ship_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMyShipResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetMyShipResponse200]:
-    """Get Ship
+    raise_on_error: Optional[bool] = None,
+    **json_body: PatchShipNavJsonBody,
+) -> Response[PatchShipNavResponse200]:
+    """Patch Ship Nav
 
-     Retrieve the details of your ship.
+     Update the nav data of a ship, such as the flight mode.
 
     Args:
         ship_symbol (str):
+        json_body (PatchShipNavJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetMyShipResponse200]
+        Response[PatchShipNavResponse200]
     """
 
+    json_body = PatchShipNavJsonBody.parse_obj(json_body)
+
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
+        json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetMyShipResponse200]:
-    """Get Ship
+    resp = _build_response(client=_client, response=response)
 
-     Retrieve the details of your ship.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMyShipResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/get_my_ship_cargo.py` & `spacetraders-0.3.0/spacetraders/api/fleet/get_my_ship.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,26 +1,25 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_my_ship_cargo_response_200 import GetMyShipCargoResponse200
-from ...types import UNSET, Response
+from ...models.get_my_ship_response_200 import GetMyShipResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}/cargo".format(
-        _client.base_url, shipSymbol=ship_symbol
-    )
+    url = "{}/my/ships/{shipSymbol}".format(_client.base_url, shipSymbol=ship_symbol)
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     return {
         "method": "get",
         "url": url,
@@ -29,145 +28,141 @@
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetMyShipCargoResponse200]:
+) -> Optional[GetMyShipResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetMyShipCargoResponse200(**response.json())
+        response_200 = GetMyShipResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetMyShipCargoResponse200]:
+) -> Response[GetMyShipResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetMyShipCargoResponse200]:
-    """Get Ship Cargo
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetMyShipResponse200]:
+    """Get Ship
 
-     Retrieve the cargo of your ship.
+     Retrieve the details of your ship.
 
     Args:
         ship_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetMyShipCargoResponse200]
+        Response[GetMyShipResponse200]
     """
 
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
-
-
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetMyShipCargoResponse200]:
-    """Get Ship Cargo
-
-     Retrieve the cargo of your ship.
-
-    Args:
-        ship_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMyShipCargoResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetMyShipCargoResponse200]:
-    """Get Ship Cargo
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetMyShipResponse200]:
+    """Get Ship
 
-     Retrieve the cargo of your ship.
+     Retrieve the details of your ship.
 
     Args:
         ship_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetMyShipCargoResponse200]
+        Response[GetMyShipResponse200]
     """
 
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetMyShipCargoResponse200]:
-    """Get Ship Cargo
-
-     Retrieve the cargo of your ship.
-
-    Args:
-        ship_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMyShipCargoResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/get_my_ships.py` & `spacetraders-0.3.0/spacetraders/api/systems/get_system_waypoints.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,25 +1,29 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional, Union
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_my_ships_response_200 import GetMyShipsResponse200
-from ...types import UNSET, Response, Unset
+from ...models.get_system_waypoints_response_200 import GetSystemWaypointsResponse200
+from ...types import UNSET, ApiError, Error, Response, Unset
 
 
 def _get_kwargs(
+    system_symbol: str,
     *,
     _client: AuthenticatedClient,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships".format(_client.base_url)
+    url = "{}/systems/{systemSymbol}/waypoints".format(
+        _client.base_url, systemSymbol=system_symbol
+    )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     params: Dict[str, Any] = {}
     params["page"] = page
 
@@ -36,157 +40,155 @@
         "follow_redirects": _client.follow_redirects,
         "params": params,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetMyShipsResponse200]:
+) -> Optional[GetSystemWaypointsResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetMyShipsResponse200(**response.json())
+        response_200 = GetSystemWaypointsResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetMyShipsResponse200]:
+) -> Response[GetSystemWaypointsResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
+    system_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
-) -> Response[GetMyShipsResponse200]:
-    """List Ships
+) -> Response[GetSystemWaypointsResponse200]:
+    """List Waypoints
 
-     Retrieve all of your ships.
+     Fetch all of the waypoints for a given system. System must be charted or a ship must be present to
+    return waypoint details.
 
     Args:
+        system_symbol (str):
         page (Union[Unset, None, int]):
         limit (Union[Unset, None, int]):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetMyShipsResponse200]
+        Response[GetSystemWaypointsResponse200]
     """
 
     kwargs = _get_kwargs(
+        system_symbol=system_symbol,
         _client=_client,
         page=page,
         limit=limit,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
-
+    resp = _build_response(client=_client, response=response)
 
-def sync(
-    *,
-    _client: AuthenticatedClient,
-    page: Union[Unset, None, int] = UNSET,
-    limit: Union[Unset, None, int] = UNSET,
-) -> Optional[GetMyShipsResponse200]:
-    """List Ships
-
-     Retrieve all of your ships.
-
-    Args:
-        page (Union[Unset, None, int]):
-        limit (Union[Unset, None, int]):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMyShipsResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        _client=_client,
-        page=page,
-        limit=limit,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
+    system_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     page: Union[Unset, None, int] = UNSET,
     limit: Union[Unset, None, int] = UNSET,
-) -> Response[GetMyShipsResponse200]:
-    """List Ships
+) -> Response[GetSystemWaypointsResponse200]:
+    """List Waypoints
 
-     Retrieve all of your ships.
+     Fetch all of the waypoints for a given system. System must be charted or a ship must be present to
+    return waypoint details.
 
     Args:
+        system_symbol (str):
         page (Union[Unset, None, int]):
         limit (Union[Unset, None, int]):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetMyShipsResponse200]
+        Response[GetSystemWaypointsResponse200]
     """
 
     kwargs = _get_kwargs(
+        system_symbol=system_symbol,
         _client=_client,
         page=page,
         limit=limit,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    *,
-    _client: AuthenticatedClient,
-    page: Union[Unset, None, int] = UNSET,
-    limit: Union[Unset, None, int] = UNSET,
-) -> Optional[GetMyShipsResponse200]:
-    """List Ships
-
-     Retrieve all of your ships.
-
-    Args:
-        page (Union[Unset, None, int]):
-        limit (Union[Unset, None, int]):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMyShipsResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            _client=_client,
-            page=page,
-            limit=limit,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/get_ship_cooldown.py` & `spacetraders-0.3.0/spacetraders/api/fleet/navigate_ship.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,200 +1,199 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_ship_cooldown_response_200 import GetShipCooldownResponse200
-from ...types import UNSET, Response
+from ...models.navigate_ship_json_body import NavigateShipJsonBody
+from ...models.navigate_ship_response_200 import NavigateShipResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    json_body: NavigateShipJsonBody,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}/cooldown".format(
+    url = "{}/my/ships/{shipSymbol}/navigate".format(
         _client.base_url, shipSymbol=ship_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
+    json_json_body = json_body.dict(by_alias=True)
+
     return {
-        "method": "get",
+        "method": "post",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
+        "json": json_json_body,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[Union[Any, GetShipCooldownResponse200]]:
+) -> Optional[NavigateShipResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetShipCooldownResponse200(**response.json())
+        response_200 = NavigateShipResponse200(**response.json())
 
         return response_200
-    if response.status_code == HTTPStatus.NO_CONTENT:
-        response_204 = cast(Any, None)
-        return response_204
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[Union[Any, GetShipCooldownResponse200]]:
+) -> Response[NavigateShipResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[Union[Any, GetShipCooldownResponse200]]:
-    """Get Ship Cooldown
-
-     Retrieve the details of your ship's reactor cooldown. Some actions such as activating your jump
-    drive, scanning, or extracting resources taxes your reactor and results in a cooldown.
+    raise_on_error: Optional[bool] = None,
+    **json_body: NavigateShipJsonBody,
+) -> Response[NavigateShipResponse200]:
+    """Navigate Ship
+
+     Navigate to a target destination. The destination must be located within the same system as the
+    ship. Navigating will consume the necessary fuel and supplies from the ship's manifest, and will pay
+    out crew wages from the agent's account.
 
-    Your ship cannot perform additional actions until your cooldown has expired. The duration of your
-    cooldown is relative to the power consumption of the related modules or mounts for the action taken.
+    The returned response will detail the route information including the expected time of arrival. Most
+    ship actions are unavailable until the ship has arrived at it's destination.
 
-    Response returns a 204 status code (no-content) when the ship has no cooldown.
+    To travel between systems, see the ship's warp or jump actions.
 
     Args:
         ship_symbol (str):
+        json_body (NavigateShipJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[Union[Any, GetShipCooldownResponse200]]
+        Response[NavigateShipResponse200]
     """
 
+    json_body = NavigateShipJsonBody.parse_obj(json_body)
+
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
+        json_body=json_body,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
-
-
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[Union[Any, GetShipCooldownResponse200]]:
-    """Get Ship Cooldown
-
-     Retrieve the details of your ship's reactor cooldown. Some actions such as activating your jump
-    drive, scanning, or extracting resources taxes your reactor and results in a cooldown.
-
-    Your ship cannot perform additional actions until your cooldown has expired. The duration of your
-    cooldown is relative to the power consumption of the related modules or mounts for the action taken.
-
-    Response returns a 204 status code (no-content) when the ship has no cooldown.
+    resp = _build_response(client=_client, response=response)
 
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        Union[Any, GetShipCooldownResponse200]
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[Union[Any, GetShipCooldownResponse200]]:
-    """Get Ship Cooldown
-
-     Retrieve the details of your ship's reactor cooldown. Some actions such as activating your jump
-    drive, scanning, or extracting resources taxes your reactor and results in a cooldown.
+    raise_on_error: Optional[bool] = None,
+    **json_body: NavigateShipJsonBody,
+) -> Response[NavigateShipResponse200]:
+    """Navigate Ship
+
+     Navigate to a target destination. The destination must be located within the same system as the
+    ship. Navigating will consume the necessary fuel and supplies from the ship's manifest, and will pay
+    out crew wages from the agent's account.
 
-    Your ship cannot perform additional actions until your cooldown has expired. The duration of your
-    cooldown is relative to the power consumption of the related modules or mounts for the action taken.
+    The returned response will detail the route information including the expected time of arrival. Most
+    ship actions are unavailable until the ship has arrived at it's destination.
 
-    Response returns a 204 status code (no-content) when the ship has no cooldown.
+    To travel between systems, see the ship's warp or jump actions.
 
     Args:
         ship_symbol (str):
+        json_body (NavigateShipJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[Union[Any, GetShipCooldownResponse200]]
+        Response[NavigateShipResponse200]
     """
 
+    json_body = NavigateShipJsonBody.parse_obj(json_body)
+
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
+        json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[Union[Any, GetShipCooldownResponse200]]:
-    """Get Ship Cooldown
-
-     Retrieve the details of your ship's reactor cooldown. Some actions such as activating your jump
-    drive, scanning, or extracting resources taxes your reactor and results in a cooldown.
-
-    Your ship cannot perform additional actions until your cooldown has expired. The duration of your
-    cooldown is relative to the power consumption of the related modules or mounts for the action taken.
+    resp = _build_response(client=_client, response=response)
 
-    Response returns a 204 status code (no-content) when the ship has no cooldown.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        Union[Any, GetShipCooldownResponse200]
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/get_ship_nav.py` & `spacetraders-0.3.0/spacetraders/api/systems/get_shipyard.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,25 +1,27 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_ship_nav_response_200 import GetShipNavResponse200
-from ...types import UNSET, Response
+from ...models.get_shipyard_response_200 import GetShipyardResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
-    ship_symbol: str,
+    system_symbol: str,
+    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}/nav".format(
-        _client.base_url, shipSymbol=ship_symbol
+    url = "{}/systems/{systemSymbol}/waypoints/{waypointSymbol}/shipyard".format(
+        _client.base_url, systemSymbol=system_symbol, waypointSymbol=waypoint_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     return {
         "method": "get",
@@ -29,145 +31,147 @@
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetShipNavResponse200]:
+) -> Optional[GetShipyardResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetShipNavResponse200(**response.json())
+        response_200 = GetShipyardResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetShipNavResponse200]:
+) -> Response[GetShipyardResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
-    ship_symbol: str,
+    system_symbol: str,
+    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetShipNavResponse200]:
-    """Get Ship Nav
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetShipyardResponse200]:
+    """Get Shipyard
 
-     Get the current nav status of a ship.
+     Get the shipyard for a waypoint.
 
     Args:
-        ship_symbol (str):
+        system_symbol (str):
+        waypoint_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetShipNavResponse200]
+        Response[GetShipyardResponse200]
     """
 
     kwargs = _get_kwargs(
-        ship_symbol=ship_symbol,
+        system_symbol=system_symbol,
+        waypoint_symbol=waypoint_symbol,
         _client=_client,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetShipNavResponse200]:
-    """Get Ship Nav
-
-     Get the current nav status of a ship.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        GetShipNavResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
-    ship_symbol: str,
+    system_symbol: str,
+    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetShipNavResponse200]:
-    """Get Ship Nav
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetShipyardResponse200]:
+    """Get Shipyard
 
-     Get the current nav status of a ship.
+     Get the shipyard for a waypoint.
 
     Args:
-        ship_symbol (str):
+        system_symbol (str):
+        waypoint_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetShipNavResponse200]
+        Response[GetShipyardResponse200]
     """
 
     kwargs = _get_kwargs(
-        ship_symbol=ship_symbol,
+        system_symbol=system_symbol,
+        waypoint_symbol=waypoint_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetShipNavResponse200]:
-    """Get Ship Nav
-
-     Get the current nav status of a ship.
-
-    Args:
-        ship_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetShipNavResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/jettison.py` & `spacetraders-0.3.0/spacetraders/api/fleet/jump_ship.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,26 +1,27 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.jettison_json_body import JettisonJsonBody
-from ...models.jettison_response_200 import JettisonResponse200
-from ...types import UNSET, Response
+from ...models.jump_ship_json_body import JumpShipJsonBody
+from ...models.jump_ship_response_200 import JumpShipResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    json_body: JettisonJsonBody,
+    json_body: JumpShipJsonBody,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}/jettison".format(
+    url = "{}/my/ships/{shipSymbol}/jump".format(
         _client.base_url, shipSymbol=ship_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     json_json_body = json_body.dict(by_alias=True)
@@ -34,161 +35,153 @@
         "follow_redirects": _client.follow_redirects,
         "json": json_json_body,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[JettisonResponse200]:
+) -> Optional[JumpShipResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = JettisonResponse200(**response.json())
+        response_200 = JumpShipResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[JettisonResponse200]:
+) -> Response[JumpShipResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: JettisonJsonBody,
-) -> Response[JettisonResponse200]:
-    """Jettison Cargo
+    raise_on_error: Optional[bool] = None,
+    **json_body: JumpShipJsonBody,
+) -> Response[JumpShipResponse200]:
+    """Jump Ship
 
-     Jettison cargo from your ship's cargo hold.
+     Jump your ship instantly to a target system. Unlike other forms of navigation, jumping requires a
+    unit of antimatter.
 
     Args:
         ship_symbol (str):
-        json_body (JettisonJsonBody):
+        json_body (JumpShipJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[JettisonResponse200]
+        Response[JumpShipResponse200]
     """
 
-    json_body = JettisonJsonBody.parse_obj(json_body)
+    json_body = JumpShipJsonBody.parse_obj(json_body)
 
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
         json_body=json_body,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: JettisonJsonBody,
-) -> Optional[JettisonResponse200]:
-    """Jettison Cargo
-
-     Jettison cargo from your ship's cargo hold.
-
-    Args:
-        ship_symbol (str):
-        json_body (JettisonJsonBody):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        JettisonResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-        json_body=json_body,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: JettisonJsonBody,
-) -> Response[JettisonResponse200]:
-    """Jettison Cargo
+    raise_on_error: Optional[bool] = None,
+    **json_body: JumpShipJsonBody,
+) -> Response[JumpShipResponse200]:
+    """Jump Ship
 
-     Jettison cargo from your ship's cargo hold.
+     Jump your ship instantly to a target system. Unlike other forms of navigation, jumping requires a
+    unit of antimatter.
 
     Args:
         ship_symbol (str):
-        json_body (JettisonJsonBody):
+        json_body (JumpShipJsonBody):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[JettisonResponse200]
+        Response[JumpShipResponse200]
     """
 
-    json_body = JettisonJsonBody.parse_obj(json_body)
+    json_body = JumpShipJsonBody.parse_obj(json_body)
 
     kwargs = _get_kwargs(
         ship_symbol=ship_symbol,
         _client=_client,
         json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: JettisonJsonBody,
-) -> Optional[JettisonResponse200]:
-    """Jettison Cargo
-
-     Jettison cargo from your ship's cargo hold.
-
-    Args:
-        ship_symbol (str):
-        json_body (JettisonJsonBody):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        JettisonResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
-            json_body=json_body,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/jump_ship.py` & `spacetraders-0.3.0/spacetraders/api/systems/get_waypoint.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,198 +1,177 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.jump_ship_json_body import JumpShipJsonBody
-from ...models.jump_ship_response_200 import JumpShipResponse200
-from ...types import UNSET, Response
+from ...models.get_waypoint_response_200 import GetWaypointResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
-    ship_symbol: str,
+    system_symbol: str,
+    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
-    json_body: JumpShipJsonBody,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}/jump".format(
-        _client.base_url, shipSymbol=ship_symbol
+    url = "{}/systems/{systemSymbol}/waypoints/{waypointSymbol}".format(
+        _client.base_url, systemSymbol=system_symbol, waypointSymbol=waypoint_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
-    json_json_body = json_body.dict(by_alias=True)
-
     return {
-        "method": "post",
+        "method": "get",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
-        "json": json_json_body,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[JumpShipResponse200]:
+) -> Optional[GetWaypointResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = JumpShipResponse200(**response.json())
+        response_200 = GetWaypointResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[JumpShipResponse200]:
+) -> Response[GetWaypointResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
-    ship_symbol: str,
+    system_symbol: str,
+    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: JumpShipJsonBody,
-) -> Response[JumpShipResponse200]:
-    """Jump Ship
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetWaypointResponse200]:
+    """Get Waypoint
 
-     Jump your ship instantly to a target system. Unlike other forms of navigation, jumping requires a
-    unit of antimatter.
+     View the details of a waypoint.
 
     Args:
-        ship_symbol (str):
-        json_body (JumpShipJsonBody):
+        system_symbol (str):
+        waypoint_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[JumpShipResponse200]
+        Response[GetWaypointResponse200]
     """
 
-    json_body = JumpShipJsonBody.parse_obj(json_body)
-
     kwargs = _get_kwargs(
-        ship_symbol=ship_symbol,
+        system_symbol=system_symbol,
+        waypoint_symbol=waypoint_symbol,
         _client=_client,
-        json_body=json_body,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
-
-
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: JumpShipJsonBody,
-) -> Optional[JumpShipResponse200]:
-    """Jump Ship
-
-     Jump your ship instantly to a target system. Unlike other forms of navigation, jumping requires a
-    unit of antimatter.
-
-    Args:
-        ship_symbol (str):
-        json_body (JumpShipJsonBody):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        JumpShipResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-        json_body=json_body,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
-    ship_symbol: str,
+    system_symbol: str,
+    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: JumpShipJsonBody,
-) -> Response[JumpShipResponse200]:
-    """Jump Ship
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetWaypointResponse200]:
+    """Get Waypoint
 
-     Jump your ship instantly to a target system. Unlike other forms of navigation, jumping requires a
-    unit of antimatter.
+     View the details of a waypoint.
 
     Args:
-        ship_symbol (str):
-        json_body (JumpShipJsonBody):
+        system_symbol (str):
+        waypoint_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[JumpShipResponse200]
+        Response[GetWaypointResponse200]
     """
 
-    json_body = JumpShipJsonBody.parse_obj(json_body)
-
     kwargs = _get_kwargs(
-        ship_symbol=ship_symbol,
+        system_symbol=system_symbol,
+        waypoint_symbol=waypoint_symbol,
         _client=_client,
-        json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: JumpShipJsonBody,
-) -> Optional[JumpShipResponse200]:
-    """Jump Ship
-
-     Jump your ship instantly to a target system. Unlike other forms of navigation, jumping requires a
-    unit of antimatter.
-
-    Args:
-        ship_symbol (str):
-        json_body (JumpShipJsonBody):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        JumpShipResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
-            json_body=json_body,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/orbit_ship.py` & `spacetraders-0.3.0/spacetraders/api/fleet/orbit_ship.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,16 +1,17 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.orbit_ship_orbit_ship_200_response import OrbitShipOrbitShip200Response
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
@@ -55,14 +56,15 @@
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[OrbitShipOrbitShip200Response]:
     """Orbit Ship
 
      Attempt to move your ship into orbit at it's current location. The request will only succeed if your
     ship is capable of moving into orbit at the time of the request.
 
     The endpoint is idempotent - successive calls will succeed even if the ship is already in orbit.
@@ -84,50 +86,46 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[OrbitShipOrbitShip200Response]:
-    """Orbit Ship
-
-     Attempt to move your ship into orbit at it's current location. The request will only succeed if your
-    ship is capable of moving into orbit at the time of the request.
-
-    The endpoint is idempotent - successive calls will succeed even if the ship is already in orbit.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        OrbitShipOrbitShip200Response
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[OrbitShipOrbitShip200Response]:
     """Orbit Ship
 
      Attempt to move your ship into orbit at it's current location. The request will only succeed if your
     ship is capable of moving into orbit at the time of the request.
 
     The endpoint is idempotent - successive calls will succeed even if the ship is already in orbit.
@@ -147,39 +145,32 @@
         ship_symbol=ship_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[OrbitShipOrbitShip200Response]:
-    """Orbit Ship
-
-     Attempt to move your ship into orbit at it's current location. The request will only succeed if your
-    ship is capable of moving into orbit at the time of the request.
+    resp = _build_response(client=_client, response=response)
 
-    The endpoint is idempotent - successive calls will succeed even if the ship is already in orbit.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        OrbitShipOrbitShip200Response
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/purchase_ship.py` & `spacetraders-0.3.0/spacetraders/api/fleet/refuel_ship.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,179 +1,170 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.purchase_ship_json_body import PurchaseShipJsonBody
-from ...models.purchase_ship_response_201 import PurchaseShipResponse201
-from ...types import UNSET, Response
+from ...models.refuel_ship_response_200 import RefuelShipResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    json_body: PurchaseShipJsonBody,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships".format(_client.base_url)
+    url = "{}/my/ships/{shipSymbol}/refuel".format(
+        _client.base_url, shipSymbol=ship_symbol
+    )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
-    json_json_body = json_body.dict(by_alias=True)
-
     return {
         "method": "post",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
-        "json": json_json_body,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[PurchaseShipResponse201]:
-    if response.status_code == HTTPStatus.CREATED:
-        response_201 = PurchaseShipResponse201(**response.json())
+) -> Optional[RefuelShipResponse200]:
+    if response.status_code == HTTPStatus.OK:
+        response_200 = RefuelShipResponse200(**response.json())
 
-        return response_201
+        return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[PurchaseShipResponse201]:
+) -> Response[RefuelShipResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: PurchaseShipJsonBody,
-) -> Response[PurchaseShipResponse201]:
-    """Purchase Ship
+    raise_on_error: Optional[bool] = None,
+) -> Response[RefuelShipResponse200]:
+    """Refuel Ship
 
-     Purchase a ship
+     Refuel your ship from the local market.
 
     Args:
-        json_body (PurchaseShipJsonBody):
+        ship_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[PurchaseShipResponse201]
+        Response[RefuelShipResponse200]
     """
 
-    json_body = PurchaseShipJsonBody.parse_obj(json_body)
-
     kwargs = _get_kwargs(
+        ship_symbol=ship_symbol,
         _client=_client,
-        json_body=json_body,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    *,
-    _client: AuthenticatedClient,
-    **json_body: PurchaseShipJsonBody,
-) -> Optional[PurchaseShipResponse201]:
-    """Purchase Ship
-
-     Purchase a ship
-
-    Args:
-        json_body (PurchaseShipJsonBody):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        PurchaseShipResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        _client=_client,
-        json_body=json_body,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-    **json_body: PurchaseShipJsonBody,
-) -> Response[PurchaseShipResponse201]:
-    """Purchase Ship
+    raise_on_error: Optional[bool] = None,
+) -> Response[RefuelShipResponse200]:
+    """Refuel Ship
 
-     Purchase a ship
+     Refuel your ship from the local market.
 
     Args:
-        json_body (PurchaseShipJsonBody):
+        ship_symbol (str):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[PurchaseShipResponse201]
+        Response[RefuelShipResponse200]
     """
 
-    json_body = PurchaseShipJsonBody.parse_obj(json_body)
-
     kwargs = _get_kwargs(
+        ship_symbol=ship_symbol,
         _client=_client,
-        json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-async def asyncio(
-    *,
-    _client: AuthenticatedClient,
-    **json_body: PurchaseShipJsonBody,
-) -> Optional[PurchaseShipResponse201]:
-    """Purchase Ship
-
-     Purchase a ship
-
-    Args:
-        json_body (PurchaseShipJsonBody):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        PurchaseShipResponse201
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            _client=_client,
-            json_body=json_body,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/refuel_ship.py` & `spacetraders-0.3.0/spacetraders/api/systems/get_system.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,173 +1,170 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.refuel_ship_response_200 import RefuelShipResponse200
-from ...types import UNSET, Response
+from ...models.get_system_response_200 import GetSystemResponse200
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
-    ship_symbol: str,
+    system_symbol: str = "X1-OE",
     *,
     _client: AuthenticatedClient,
 ) -> Dict[str, Any]:
-    url = "{}/my/ships/{shipSymbol}/refuel".format(
-        _client.base_url, shipSymbol=ship_symbol
+    url = "{}/systems/{systemSymbol}".format(
+        _client.base_url, systemSymbol=system_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
     return {
-        "method": "post",
+        "method": "get",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[RefuelShipResponse200]:
+) -> Optional[GetSystemResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = RefuelShipResponse200(**response.json())
+        response_200 = GetSystemResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[RefuelShipResponse200]:
+) -> Response[GetSystemResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
-    ship_symbol: str,
+    system_symbol: str = "X1-OE",
     *,
     _client: AuthenticatedClient,
-) -> Response[RefuelShipResponse200]:
-    """Refuel Ship
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetSystemResponse200]:
+    """Get System
 
-     Refuel your ship from the local market.
+     Get the details of a system.
 
     Args:
-        ship_symbol (str):
+        system_symbol (str):  Default: 'X1-OE'.
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[RefuelShipResponse200]
+        Response[GetSystemResponse200]
     """
 
     kwargs = _get_kwargs(
-        ship_symbol=ship_symbol,
+        system_symbol=system_symbol,
         _client=_client,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[RefuelShipResponse200]:
-    """Refuel Ship
-
-     Refuel your ship from the local market.
-
-    Args:
-        ship_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        RefuelShipResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
-    ship_symbol: str,
+    system_symbol: str = "X1-OE",
     *,
     _client: AuthenticatedClient,
-) -> Response[RefuelShipResponse200]:
-    """Refuel Ship
+    raise_on_error: Optional[bool] = None,
+) -> Response[GetSystemResponse200]:
+    """Get System
 
-     Refuel your ship from the local market.
+     Get the details of a system.
 
     Args:
-        ship_symbol (str):
+        system_symbol (str):  Default: 'X1-OE'.
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[RefuelShipResponse200]
+        Response[GetSystemResponse200]
     """
 
     kwargs = _get_kwargs(
-        ship_symbol=ship_symbol,
+        system_symbol=system_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[RefuelShipResponse200]:
-    """Refuel Ship
-
-     Refuel your ship from the local market.
-
-    Args:
-        ship_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        RefuelShipResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/ship_refine.py` & `spacetraders-0.3.0/spacetraders/api/fleet/ship_refine.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,19 +1,20 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.ship_refine_json_body import ShipRefineJsonBody
 from ...models.ship_refine_ship_refine_200_response import (
     ShipRefineShipRefine200Response,
 )
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
     json_body: ShipRefineJsonBody,
@@ -62,14 +63,15 @@
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     **json_body: ShipRefineJsonBody,
 ) -> Response[ShipRefineShipRefine200Response]:
     """Ship Refine
 
      Attempt to refine the raw materials on your ship. The request will only succeed if your ship is
     capable of refining at the time of the request.
 
@@ -94,51 +96,46 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: ShipRefineJsonBody,
-) -> Optional[ShipRefineShipRefine200Response]:
-    """Ship Refine
-
-     Attempt to refine the raw materials on your ship. The request will only succeed if your ship is
-    capable of refining at the time of the request.
-
-    Args:
-        ship_symbol (str):
-        json_body (ShipRefineJsonBody):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        ShipRefineShipRefine200Response
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-        json_body=json_body,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     **json_body: ShipRefineJsonBody,
 ) -> Response[ShipRefineShipRefine200Response]:
     """Ship Refine
 
      Attempt to refine the raw materials on your ship. The request will only succeed if your ship is
     capable of refining at the time of the request.
 
@@ -161,40 +158,32 @@
         _client=_client,
         json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: ShipRefineJsonBody,
-) -> Optional[ShipRefineShipRefine200Response]:
-    """Ship Refine
-
-     Attempt to refine the raw materials on your ship. The request will only succeed if your ship is
-    capable of refining at the time of the request.
-
-    Args:
-        ship_symbol (str):
-        json_body (ShipRefineJsonBody):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        ShipRefineShipRefine200Response
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
-            json_body=json_body,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/fleet/warp_ship.py` & `spacetraders-0.3.0/spacetraders/api/fleet/warp_ship.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,17 +1,18 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.warp_ship_json_body import WarpShipJsonBody
 from ...models.warp_ship_response_200 import WarpShipResponse200
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
     json_body: WarpShipJsonBody,
@@ -60,14 +61,15 @@
     )
 
 
 def sync_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     **json_body: WarpShipJsonBody,
 ) -> Response[WarpShipResponse200]:
     """Warp Ship
 
      Warp your ship to a target destination in another system. Warping will consume the necessary fuel
     and supplies from the ship's manifest, and will pay out crew wages from the agent's account.
 
@@ -95,54 +97,46 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: WarpShipJsonBody,
-) -> Optional[WarpShipResponse200]:
-    """Warp Ship
-
-     Warp your ship to a target destination in another system. Warping will consume the necessary fuel
-    and supplies from the ship's manifest, and will pay out crew wages from the agent's account.
-
-    The returned response will detail the route information including the expected time of arrival. Most
-    ship actions are unavailable until the ship has arrived at it's destination.
-
-    Args:
-        ship_symbol (str):
-        json_body (WarpShipJsonBody):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        WarpShipResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        ship_symbol=ship_symbol,
-        _client=_client,
-        json_body=json_body,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
     **json_body: WarpShipJsonBody,
 ) -> Response[WarpShipResponse200]:
     """Warp Ship
 
      Warp your ship to a target destination in another system. Warping will consume the necessary fuel
     and supplies from the ship's manifest, and will pay out crew wages from the agent's account.
 
@@ -168,43 +162,32 @@
         _client=_client,
         json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    ship_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-    **json_body: WarpShipJsonBody,
-) -> Optional[WarpShipResponse200]:
-    """Warp Ship
-
-     Warp your ship to a target destination in another system. Warping will consume the necessary fuel
-    and supplies from the ship's manifest, and will pay out crew wages from the agent's account.
+    resp = _build_response(client=_client, response=response)
 
-    The returned response will detail the route information including the expected time of arrival. Most
-    ship actions are unavailable until the ship has arrived at it's destination.
-
-    Args:
-        ship_symbol (str):
-        json_body (WarpShipJsonBody):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        WarpShipResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            ship_symbol=ship_symbol,
-            _client=_client,
-            json_body=json_body,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/systems/get_jump_gate.py` & `spacetraders-0.3.0/spacetraders/api/systems/get_jump_gate.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,16 +1,17 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
 from ...models.get_jump_gate_response_200 import GetJumpGateResponse200
-from ...types import UNSET, Response
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
     system_symbol: str,
     waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
@@ -57,14 +58,15 @@
 
 
 def sync_detailed(
     system_symbol: str,
     waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[GetJumpGateResponse200]:
     """Get Jump Gate
 
      Get jump gate details for a waypoint.
 
     Args:
         system_symbol (str):
@@ -85,51 +87,47 @@
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-def sync(
-    system_symbol: str,
-    waypoint_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetJumpGateResponse200]:
-    """Get Jump Gate
-
-     Get jump gate details for a waypoint.
-
-    Args:
-        system_symbol (str):
-        waypoint_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    Returns:
-        GetJumpGateResponse200
-    """
-
-    return sync_detailed(
-        system_symbol=system_symbol,
-        waypoint_symbol=waypoint_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
     system_symbol: str,
     waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
+    raise_on_error: Optional[bool] = None,
 ) -> Response[GetJumpGateResponse200]:
     """Get Jump Gate
 
      Get jump gate details for a waypoint.
 
     Args:
         system_symbol (str):
@@ -148,39 +146,32 @@
         waypoint_symbol=waypoint_symbol,
         _client=_client,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    system_symbol: str,
-    waypoint_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetJumpGateResponse200]:
-    """Get Jump Gate
-
-     Get jump gate details for a waypoint.
+    resp = _build_response(client=_client, response=response)
 
-    Args:
-        system_symbol (str):
-        waypoint_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetJumpGateResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            system_symbol=system_symbol,
-            waypoint_symbol=waypoint_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/systems/get_market.py` & `spacetraders-0.3.0/spacetraders/api/fleet/purchase_cargo.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,194 +1,189 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_market_response_200 import GetMarketResponse200
-from ...types import UNSET, Response
+from ...models.purchase_cargo_purchase_cargo_201_response import (
+    PurchaseCargoPurchaseCargo201Response,
+)
+from ...models.purchase_cargo_purchase_cargo_request import (
+    PurchaseCargoPurchaseCargoRequest,
+)
+from ...types import ApiError, Error, Response
 
 
 def _get_kwargs(
-    system_symbol: str,
-    waypoint_symbol: str,
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
+    json_body: PurchaseCargoPurchaseCargoRequest,
 ) -> Dict[str, Any]:
-    url = "{}/systems/{systemSymbol}/waypoints/{waypointSymbol}/market".format(
-        _client.base_url, systemSymbol=system_symbol, waypointSymbol=waypoint_symbol
+    url = "{}/my/ships/{shipSymbol}/purchase".format(
+        _client.base_url, shipSymbol=ship_symbol
     )
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
+    json_json_body = json_body.dict(by_alias=True)
+
     return {
-        "method": "get",
+        "method": "post",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
+        "json": json_json_body,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetMarketResponse200]:
-    if response.status_code == HTTPStatus.OK:
-        response_200 = GetMarketResponse200(**response.json())
+) -> Optional[PurchaseCargoPurchaseCargo201Response]:
+    if response.status_code == HTTPStatus.CREATED:
+        response_201 = PurchaseCargoPurchaseCargo201Response(**response.json())
 
-        return response_200
+        return response_201
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetMarketResponse200]:
+) -> Response[PurchaseCargoPurchaseCargo201Response]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
-    system_symbol: str,
-    waypoint_symbol: str,
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetMarketResponse200]:
-    """Get Market
+    raise_on_error: Optional[bool] = None,
+    **json_body: PurchaseCargoPurchaseCargoRequest,
+) -> Response[PurchaseCargoPurchaseCargo201Response]:
+    """Purchase Cargo
 
-     Retrieve imports, exports and exchange data from a marketplace. Imports can be sold, exports can be
-    purchased, and exchange goods can be purchased or sold. Send a ship to the waypoint to access trade
-    good prices and recent transactions.
+     Purchase cargo.
 
     Args:
-        system_symbol (str):
-        waypoint_symbol (str):
+        ship_symbol (str):
+        json_body (PurchaseCargoPurchaseCargoRequest):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetMarketResponse200]
+        Response[PurchaseCargoPurchaseCargo201Response]
     """
 
+    json_body = PurchaseCargoPurchaseCargoRequest.parse_obj(json_body)
+
     kwargs = _get_kwargs(
-        system_symbol=system_symbol,
-        waypoint_symbol=waypoint_symbol,
+        ship_symbol=ship_symbol,
         _client=_client,
+        json_body=json_body,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
-
-
-def sync(
-    system_symbol: str,
-    waypoint_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetMarketResponse200]:
-    """Get Market
-
-     Retrieve imports, exports and exchange data from a marketplace. Imports can be sold, exports can be
-    purchased, and exchange goods can be purchased or sold. Send a ship to the waypoint to access trade
-    good prices and recent transactions.
-
-    Args:
-        system_symbol (str):
-        waypoint_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMarketResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        system_symbol=system_symbol,
-        waypoint_symbol=waypoint_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
-    system_symbol: str,
-    waypoint_symbol: str,
+    ship_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetMarketResponse200]:
-    """Get Market
+    raise_on_error: Optional[bool] = None,
+    **json_body: PurchaseCargoPurchaseCargoRequest,
+) -> Response[PurchaseCargoPurchaseCargo201Response]:
+    """Purchase Cargo
 
-     Retrieve imports, exports and exchange data from a marketplace. Imports can be sold, exports can be
-    purchased, and exchange goods can be purchased or sold. Send a ship to the waypoint to access trade
-    good prices and recent transactions.
+     Purchase cargo.
 
     Args:
-        system_symbol (str):
-        waypoint_symbol (str):
+        ship_symbol (str):
+        json_body (PurchaseCargoPurchaseCargoRequest):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetMarketResponse200]
+        Response[PurchaseCargoPurchaseCargo201Response]
     """
 
+    json_body = PurchaseCargoPurchaseCargoRequest.parse_obj(json_body)
+
     kwargs = _get_kwargs(
-        system_symbol=system_symbol,
-        waypoint_symbol=waypoint_symbol,
+        ship_symbol=ship_symbol,
         _client=_client,
+        json_body=json_body,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
-
-
-async def asyncio(
-    system_symbol: str,
-    waypoint_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetMarketResponse200]:
-    """Get Market
-
-     Retrieve imports, exports and exchange data from a marketplace. Imports can be sold, exports can be
-    purchased, and exchange goods can be purchased or sold. Send a ship to the waypoint to access trade
-    good prices and recent transactions.
-
-    Args:
-        system_symbol (str):
-        waypoint_symbol (str):
+    resp = _build_response(client=_client, response=response)
 
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetMarketResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            system_symbol=system_symbol,
-            waypoint_symbol=waypoint_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/api/systems/get_shipyard.py` & `spacetraders-0.3.0/spacetraders/api/systems/get_systems.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,186 +1,183 @@
+import json
 from http import HTTPStatus
-from typing import Any, Dict, List, Optional, Union, cast
+from typing import Any, Dict, Optional, Union
 
 import httpx
 
 from ... import errors
 from ...client import AuthenticatedClient, Client
-from ...models.get_shipyard_response_200 import GetShipyardResponse200
-from ...types import UNSET, Response
+from ...models.get_systems_response_200 import GetSystemsResponse200
+from ...types import UNSET, ApiError, Error, Response, Unset
 
 
 def _get_kwargs(
-    system_symbol: str,
-    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
+    page: Union[Unset, None, int] = UNSET,
+    limit: Union[Unset, None, int] = UNSET,
 ) -> Dict[str, Any]:
-    url = "{}/systems/{systemSymbol}/waypoints/{waypointSymbol}/shipyard".format(
-        _client.base_url, systemSymbol=system_symbol, waypointSymbol=waypoint_symbol
-    )
+    url = "{}/systems".format(_client.base_url)
 
     headers: Dict[str, str] = _client.get_headers()
     cookies: Dict[str, Any] = _client.get_cookies()
 
+    params: Dict[str, Any] = {}
+    params["page"] = page
+
+    params["limit"] = limit
+
+    params = {k: v for k, v in params.items() if v is not UNSET and v is not None}
+
     return {
         "method": "get",
         "url": url,
         "headers": headers,
         "cookies": cookies,
         "timeout": _client.get_timeout(),
         "follow_redirects": _client.follow_redirects,
+        "params": params,
     }
 
 
 def _parse_response(
     *, client: Client, response: httpx.Response
-) -> Optional[GetShipyardResponse200]:
+) -> Optional[GetSystemsResponse200]:
     if response.status_code == HTTPStatus.OK:
-        response_200 = GetShipyardResponse200(**response.json())
+        response_200 = GetSystemsResponse200(**response.json())
 
         return response_200
     if client.raise_on_unexpected_status:
         raise errors.UnexpectedStatus(response.status_code, response.content)
     else:
         return None
 
 
 def _build_response(
     *, client: Client, response: httpx.Response
-) -> Response[GetShipyardResponse200]:
+) -> Response[GetSystemsResponse200]:
     return Response(
         status_code=HTTPStatus(response.status_code),
         content=response.content,
         headers=response.headers,
         parsed=_parse_response(client=client, response=response),
     )
 
 
 def sync_detailed(
-    system_symbol: str,
-    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetShipyardResponse200]:
-    """Get Shipyard
+    raise_on_error: Optional[bool] = None,
+    page: Union[Unset, None, int] = UNSET,
+    limit: Union[Unset, None, int] = UNSET,
+) -> Response[GetSystemsResponse200]:
+    """List Systems
 
-     Get the shipyard for a waypoint.
+     Return a list of all systems.
 
     Args:
-        system_symbol (str):
-        waypoint_symbol (str):
+        page (Union[Unset, None, int]):
+        limit (Union[Unset, None, int]):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetShipyardResponse200]
+        Response[GetSystemsResponse200]
     """
 
     kwargs = _get_kwargs(
-        system_symbol=system_symbol,
-        waypoint_symbol=waypoint_symbol,
         _client=_client,
+        page=page,
+        limit=limit,
     )
 
     response = httpx.request(
         verify=_client.verify_ssl,
         **kwargs,
     )
 
-    return _build_response(client=_client, response=response)
-
-
-def sync(
-    system_symbol: str,
-    waypoint_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetShipyardResponse200]:
-    """Get Shipyard
-
-     Get the shipyard for a waypoint.
+    resp = _build_response(client=_client, response=response)
 
-    Args:
-        system_symbol (str):
-        waypoint_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-    Returns:
-        GetShipyardResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return sync_detailed(
-        system_symbol=system_symbol,
-        waypoint_symbol=waypoint_symbol,
-        _client=_client,
-    ).parsed
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
+        )
+    )
 
 
 async def asyncio_detailed(
-    system_symbol: str,
-    waypoint_symbol: str,
     *,
     _client: AuthenticatedClient,
-) -> Response[GetShipyardResponse200]:
-    """Get Shipyard
+    raise_on_error: Optional[bool] = None,
+    page: Union[Unset, None, int] = UNSET,
+    limit: Union[Unset, None, int] = UNSET,
+) -> Response[GetSystemsResponse200]:
+    """List Systems
 
-     Get the shipyard for a waypoint.
+     Return a list of all systems.
 
     Args:
-        system_symbol (str):
-        waypoint_symbol (str):
+        page (Union[Unset, None, int]):
+        limit (Union[Unset, None, int]):
 
     Raises:
         errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
         httpx.TimeoutException: If the request takes longer than Client.timeout.
 
     Returns:
-        Response[GetShipyardResponse200]
+        Response[GetSystemsResponse200]
     """
 
     kwargs = _get_kwargs(
-        system_symbol=system_symbol,
-        waypoint_symbol=waypoint_symbol,
         _client=_client,
+        page=page,
+        limit=limit,
     )
 
     async with httpx.AsyncClient(verify=_client.verify_ssl) as c:
         response = await c.request(**kwargs)
 
-    return _build_response(client=_client, response=response)
+    resp = _build_response(client=_client, response=response)
 
+    raise_on_error = (
+        raise_on_error if raise_on_error is not None else _client.raise_on_error
+    )
+    if not raise_on_error:
+        return resp
 
-async def asyncio(
-    system_symbol: str,
-    waypoint_symbol: str,
-    *,
-    _client: AuthenticatedClient,
-) -> Optional[GetShipyardResponse200]:
-    """Get Shipyard
-
-     Get the shipyard for a waypoint.
-
-    Args:
-        system_symbol (str):
-        waypoint_symbol (str):
-
-    Raises:
-        errors.UnexpectedStatus: If the server returns an undocumented status code and Client.raise_on_unexpected_status is True.
-        httpx.TimeoutException: If the request takes longer than Client.timeout.
-
-    Returns:
-        GetShipyardResponse200
-    """
+    if resp.status_code < 300:
+        return resp.parsed.data
 
-    return (
-        await asyncio_detailed(
-            system_symbol=system_symbol,
-            waypoint_symbol=waypoint_symbol,
-            _client=_client,
+    try:
+        error = json.loads(resp.content)
+        details = error.get("error", {})
+    except Exception:
+        details = {"message": resp.content}
+    raise ApiError(
+        Error(
+            status_code=resp.status_code,
+            message=details.get("message"),
+            code=details.get("code"),
+            data=details.get("data"),
+            headers=resp.headers,
         )
-    ).parsed
+    )
```

### Comparing `spacetraders-0.2.4/spacetraders/client.py` & `spacetraders-0.3.0/spacetraders/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -36,23 +36,25 @@
         headers: A dictionary of headers to be sent with every request
         timeout: The maximum amount of a time in seconds a request can take. API functions will raise
             httpx.TimeoutException if this is exceeded.
         verify_ssl: Whether or not to verify the SSL certificate of the API server. This should be True in production,
             but can be set to False for testing purposes.
         raise_on_unexpected_status: Whether or not to raise an errors.UnexpectedStatus if the API returns a
             status code that was not documented in the source OpenAPI document.
+        raise_on_error: Whether or not to raise an HTTPStatus >= 300 and return a parsed object or a full Response
         follow_redirects: Whether or not to follow redirects. Default value is False.
     """
 
     base_url: str
     cookies: Dict[str, str] = attr.ib(factory=dict, kw_only=True)
     headers: Dict[str, str] = attr.ib(factory=dict, kw_only=True)
     timeout: float = attr.ib(5.0, kw_only=True)
     verify_ssl: Union[str, bool, ssl.SSLContext] = attr.ib(True, kw_only=True)
     raise_on_unexpected_status: bool = attr.ib(False, kw_only=True)
+    raise_on_error: bool = attr.ib(False, kw_only=True)
     follow_redirects: bool = attr.ib(False, kw_only=True)
 
     def get_headers(self) -> Dict[str, str]:
         """Get headers to be used in all endpoints"""
         return {**self.headers}
 
     def with_headers(self, headers: Dict[str, str]) -> "Client":
```

### Comparing `spacetraders-0.2.4/spacetraders/models/__init__.py` & `spacetraders-0.3.0/spacetraders/models/__init__.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/models/accept_contract_response_200.py` & `spacetraders-0.3.0/spacetraders/models/accept_contract_response_200.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.accept_contract_response_200_data import AcceptContractResponse200Data
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="AcceptContractResponse200")
 
 
 class AcceptContractResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/accept_contract_response_200_data.py` & `spacetraders-0.3.0/spacetraders/models/deliver_contract_response_200_data.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,40 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
 from ..models.contract import Contract
-from ..types import UNSET, Unset
+from ..models.ship_cargo import ShipCargo
+from ..types import Unset
 
-T = TypeVar("T", bound="AcceptContractResponse200Data")
+T = TypeVar("T", bound="DeliverContractResponse200Data")
 
 
-class AcceptContractResponse200Data(BaseModel):
+class DeliverContractResponse200Data(BaseModel):
     """
     Attributes:
-        agent (Agent):
         contract (Contract):
+        cargo (ShipCargo):
     """
 
-    agent: "Agent" = Field(alias="agent")
     contract: "Contract" = Field(alias="contract")
+    cargo: "ShipCargo" = Field(alias="cargo")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/agent.py` & `spacetraders-0.3.0/spacetraders/models/agent.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,24 +1,17 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="Agent")
 
 
 class Agent(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/chart.py` & `spacetraders-0.3.0/spacetraders/models/chart.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,25 +1,16 @@
 import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="Chart")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/connected_system.py` & `spacetraders-0.3.0/spacetraders/models/connected_system.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,22 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.system_type import SystemType
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ConnectedSystem")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/contract.py` & `spacetraders-0.3.0/spacetraders/models/contract.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,29 +1,20 @@
 import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
 from ..models.contract_terms import ContractTerms
 from ..models.contract_type import ContractType
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="Contract")
 
 
 class Contract(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/contract_deliver_good.py` & `spacetraders-0.3.0/spacetraders/models/contract_deliver_good.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,24 +1,17 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ContractDeliverGood")
 
 
 class ContractDeliverGood(BaseModel):
     """The details of a delivery contract. Includes the type of good, units needed, and the destination.
```

### Comparing `spacetraders-0.2.4/spacetraders/models/contract_payment.py` & `spacetraders-0.3.0/spacetraders/models/create_ship_system_scan_response_201_data.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,37 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.cooldown import Cooldown
+from ..models.scanned_system import ScannedSystem
+from ..types import Unset
 
-T = TypeVar("T", bound="ContractPayment")
+T = TypeVar("T", bound="CreateShipSystemScanResponse201Data")
 
 
-class ContractPayment(BaseModel):
+class CreateShipSystemScanResponse201Data(BaseModel):
     """
     Attributes:
-        on_accepted (int): The amount of credits received up front for accepting the contract.
-        on_fulfilled (int): The amount of credits received when the contract is fulfilled.
+        cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
+        systems (List['ScannedSystem']):
     """
 
-    on_accepted: int = Field(alias="onAccepted")
-    on_fulfilled: int = Field(alias="onFulfilled")
+    cooldown: "Cooldown" = Field(alias="cooldown")
+    systems: List["ScannedSystem"] = Field(alias="systems")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/contract_terms.py` & `spacetraders-0.3.0/spacetraders/models/contract_terms.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,25 +1,16 @@
 import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
 from ..models.contract_deliver_good import ContractDeliverGood
 from ..models.contract_payment import ContractPayment
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ContractTerms")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/cooldown.py` & `spacetraders-0.3.0/spacetraders/models/cooldown.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,27 +1,18 @@
 import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="Cooldown")
 
 
 class Cooldown(BaseModel):
     """A cooldown is a period of time in which a ship cannot perform certain actions.
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_chart_response_201.py` & `spacetraders-0.3.0/spacetraders/models/jump_ship_response_200.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.create_chart_response_201_data import CreateChartResponse201Data
-from ..types import UNSET, Unset
+from ..models.jump_ship_response_200_data import JumpShipResponse200Data
+from ..types import Unset
 
-T = TypeVar("T", bound="CreateChartResponse201")
+T = TypeVar("T", bound="JumpShipResponse200")
 
 
-class CreateChartResponse201(BaseModel):
+class JumpShipResponse200(BaseModel):
     """
     Attributes:
-        data (CreateChartResponse201Data):
+        data (JumpShipResponse200Data):
     """
 
-    data: "CreateChartResponse201Data" = Field(alias="data")
+    data: "JumpShipResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_chart_response_201_data.py` & `spacetraders-0.3.0/spacetraders/models/create_chart_response_201_data.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,27 +1,19 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.chart import Chart
 from ..models.waypoint import Waypoint
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="CreateChartResponse201Data")
 
 
 class CreateChartResponse201Data(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_ship_ship_scan_response_201.py` & `spacetraders-0.3.0/spacetraders/models/create_ship_waypoint_scan_response_201.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,39 +1,31 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.create_ship_ship_scan_response_201_data import (
-    CreateShipShipScanResponse201Data,
+from ..models.create_ship_waypoint_scan_response_201_data import (
+    CreateShipWaypointScanResponse201Data,
 )
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="CreateShipShipScanResponse201")
+T = TypeVar("T", bound="CreateShipWaypointScanResponse201")
 
 
-class CreateShipShipScanResponse201(BaseModel):
+class CreateShipWaypointScanResponse201(BaseModel):
     """
     Attributes:
-        data (CreateShipShipScanResponse201Data):
+        data (CreateShipWaypointScanResponse201Data):
     """
 
-    data: "CreateShipShipScanResponse201Data" = Field(alias="data")
+    data: "CreateShipWaypointScanResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_ship_ship_scan_response_201_data.py` & `spacetraders-0.3.0/spacetraders/models/create_survey_response_201_data.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,40 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.cooldown import Cooldown
-from ..models.scanned_ship import ScannedShip
-from ..types import UNSET, Unset
+from ..models.survey import Survey
+from ..types import Unset
 
-T = TypeVar("T", bound="CreateShipShipScanResponse201Data")
+T = TypeVar("T", bound="CreateSurveyResponse201Data")
 
 
-class CreateShipShipScanResponse201Data(BaseModel):
+class CreateSurveyResponse201Data(BaseModel):
     """
     Attributes:
         cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
-        ships (List['ScannedShip']):
+        surveys (List['Survey']):
     """
 
     cooldown: "Cooldown" = Field(alias="cooldown")
-    ships: List["ScannedShip"] = Field(alias="ships")
+    surveys: List["Survey"] = Field(alias="surveys")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_ship_system_scan_response_201.py` & `spacetraders-0.3.0/spacetraders/models/create_ship_system_scan_response_201.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.create_ship_system_scan_response_201_data import (
     CreateShipSystemScanResponse201Data,
 )
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="CreateShipSystemScanResponse201")
 
 
 class CreateShipSystemScanResponse201(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_ship_system_scan_response_201_data.py` & `spacetraders-0.3.0/spacetraders/models/create_ship_waypoint_scan_response_201_data.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,40 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.cooldown import Cooldown
-from ..models.scanned_system import ScannedSystem
-from ..types import UNSET, Unset
+from ..models.scanned_waypoint import ScannedWaypoint
+from ..types import Unset
 
-T = TypeVar("T", bound="CreateShipSystemScanResponse201Data")
+T = TypeVar("T", bound="CreateShipWaypointScanResponse201Data")
 
 
-class CreateShipSystemScanResponse201Data(BaseModel):
+class CreateShipWaypointScanResponse201Data(BaseModel):
     """
     Attributes:
         cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
-        systems (List['ScannedSystem']):
+        waypoints (List['ScannedWaypoint']):
     """
 
     cooldown: "Cooldown" = Field(alias="cooldown")
-    systems: List["ScannedSystem"] = Field(alias="systems")
+    waypoints: List["ScannedWaypoint"] = Field(alias="waypoints")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_ship_waypoint_scan_response_201.py` & `spacetraders-0.3.0/spacetraders/models/create_ship_ship_scan_response_201.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,39 +1,31 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.create_ship_waypoint_scan_response_201_data import (
-    CreateShipWaypointScanResponse201Data,
+from ..models.create_ship_ship_scan_response_201_data import (
+    CreateShipShipScanResponse201Data,
 )
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="CreateShipWaypointScanResponse201")
+T = TypeVar("T", bound="CreateShipShipScanResponse201")
 
 
-class CreateShipWaypointScanResponse201(BaseModel):
+class CreateShipShipScanResponse201(BaseModel):
     """
     Attributes:
-        data (CreateShipWaypointScanResponse201Data):
+        data (CreateShipShipScanResponse201Data):
     """
 
-    data: "CreateShipWaypointScanResponse201Data" = Field(alias="data")
+    data: "CreateShipShipScanResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_ship_waypoint_scan_response_201_data.py` & `spacetraders-0.3.0/spacetraders/models/create_ship_ship_scan_response_201_data.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,40 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.cooldown import Cooldown
-from ..models.scanned_waypoint import ScannedWaypoint
-from ..types import UNSET, Unset
+from ..models.scanned_ship import ScannedShip
+from ..types import Unset
 
-T = TypeVar("T", bound="CreateShipWaypointScanResponse201Data")
+T = TypeVar("T", bound="CreateShipShipScanResponse201Data")
 
 
-class CreateShipWaypointScanResponse201Data(BaseModel):
+class CreateShipShipScanResponse201Data(BaseModel):
     """
     Attributes:
         cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
-        waypoints (List['ScannedWaypoint']):
+        ships (List['ScannedShip']):
     """
 
     cooldown: "Cooldown" = Field(alias="cooldown")
-    waypoints: List["ScannedWaypoint"] = Field(alias="waypoints")
+    ships: List["ScannedShip"] = Field(alias="ships")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_survey_response_201.py` & `spacetraders-0.3.0/spacetraders/models/create_survey_response_201.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.create_survey_response_201_data import CreateSurveyResponse201Data
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="CreateSurveyResponse201")
 
 
 class CreateSurveyResponse201(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/create_survey_response_201_data.py` & `spacetraders-0.3.0/spacetraders/models/get_faction_response_200.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,40 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.cooldown import Cooldown
-from ..models.survey import Survey
-from ..types import UNSET, Unset
+from ..models.faction import Faction
+from ..types import Unset
 
-T = TypeVar("T", bound="CreateSurveyResponse201Data")
+T = TypeVar("T", bound="GetFactionResponse200")
 
 
-class CreateSurveyResponse201Data(BaseModel):
+class GetFactionResponse200(BaseModel):
     """
     Attributes:
-        cooldown (Cooldown): A cooldown is a period of time in which a ship cannot perform certain actions.
-        surveys (List['Survey']):
+        data (Faction):
     """
 
-    cooldown: "Cooldown" = Field(alias="cooldown")
-    surveys: List["Survey"] = Field(alias="surveys")
+    data: "Faction" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/deliver_contract_json_body.py` & `spacetraders-0.3.0/spacetraders/models/deliver_contract_json_body.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,24 +1,17 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="DeliverContractJsonBody")
 
 
 class DeliverContractJsonBody(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/deliver_contract_response_200.py` & `spacetraders-0.3.0/spacetraders/models/deliver_contract_response_200.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.deliver_contract_response_200_data import DeliverContractResponse200Data
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="DeliverContractResponse200")
 
 
 class DeliverContractResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/deliver_contract_response_200_data.py` & `spacetraders-0.3.0/spacetraders/models/get_contract_response_200.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,40 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.contract import Contract
-from ..models.ship_cargo import ShipCargo
-from ..types import UNSET, Unset
+from ..types import Unset
 
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
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/dock_ship_dock_ship_200_response.py` & `spacetraders-0.3.0/spacetraders/models/dock_ship_dock_ship_200_response_data.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,39 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.dock_ship_dock_ship_200_response_data import (
-    DockShipDockShip200ResponseData,
-)
-from ..types import UNSET, Unset
+from ..models.ship_nav import ShipNav
+from ..types import Unset
 
-T = TypeVar("T", bound="DockShipDockShip200Response")
+T = TypeVar("T", bound="DockShipDockShip200ResponseData")
 
 
-class DockShipDockShip200Response(BaseModel):
+class DockShipDockShip200ResponseData(BaseModel):
     """
     Attributes:
-        data (DockShipDockShip200ResponseData):
+        nav (ShipNav): The navigation information of the ship.
     """
 
-    data: "DockShipDockShip200ResponseData" = Field(alias="data")
+    nav: "ShipNav" = Field(alias="nav")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/dock_ship_dock_ship_200_response_data.py` & `spacetraders-0.3.0/spacetraders/models/scanned_ship_frame.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_nav import ShipNav
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="DockShipDockShip200ResponseData")
+T = TypeVar("T", bound="ScannedShipFrame")
 
 
-class DockShipDockShip200ResponseData(BaseModel):
-    """
+class ScannedShipFrame(BaseModel):
+    """The frame of the ship.
+
     Attributes:
-        nav (ShipNav): The navigation information of the ship.
+        symbol (str):
     """
 
-    nav: "ShipNav" = Field(alias="nav")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/extract_resources_json_body.py` & `spacetraders-0.3.0/spacetraders/models/purchase_cargo_purchase_cargo_request.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,39 +1,30 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.survey import Survey
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="ExtractResourcesJsonBody")
+T = TypeVar("T", bound="PurchaseCargoPurchaseCargoRequest")
 
 
-class ExtractResourcesJsonBody(BaseModel):
+class PurchaseCargoPurchaseCargoRequest(BaseModel):
     """
     Attributes:
-        survey (Union[Unset, Survey]): A resource survey of a waypoint, detailing a specific extraction location and the
-            types of resources that can be found there.
+        symbol (str):
+        units (int):
     """
 
-    survey: Union[Unset, "Survey"] = Field(UNSET, alias="survey")
+    symbol: str = Field(alias="symbol")
+    units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/extract_resources_response_201.py` & `spacetraders-0.3.0/spacetraders/models/extract_resources_response_201.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.extract_resources_response_201_data import ExtractResourcesResponse201Data
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ExtractResourcesResponse201")
 
 
 class ExtractResourcesResponse201(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/extract_resources_response_201_data.py` & `spacetraders-0.3.0/spacetraders/models/extract_resources_response_201_data.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.cooldown import Cooldown
 from ..models.extraction import Extraction
 from ..models.ship_cargo import ShipCargo
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ExtractResourcesResponse201Data")
 
 
 class ExtractResourcesResponse201Data(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/extraction.py` & `spacetraders-0.3.0/spacetraders/models/extraction.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.extraction_yield import ExtractionYield
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="Extraction")
 
 
 class Extraction(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/extraction_yield.py` & `spacetraders-0.3.0/spacetraders/models/extraction_yield.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,24 +1,17 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ExtractionYield")
 
 
 class ExtractionYield(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/faction.py` & `spacetraders-0.3.0/spacetraders/models/faction.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.faction_trait import FactionTrait
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="Faction")
 
 
 class Faction(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/faction_trait.py` & `spacetraders-0.3.0/spacetraders/models/faction_trait.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,25 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.faction_trait_symbol import FactionTraitSymbol
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="FactionTrait")
 
 
 class FactionTrait(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/faction_trait_symbol.py` & `spacetraders-0.3.0/spacetraders/models/faction_trait_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/models/fulfill_contract_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_my_agent_response_200.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.fulfill_contract_response_200_data import FulfillContractResponse200Data
-from ..types import UNSET, Unset
+from ..models.agent import Agent
+from ..types import Unset
 
-T = TypeVar("T", bound="FulfillContractResponse200")
+T = TypeVar("T", bound="GetMyAgentResponse200")
 
 
-class FulfillContractResponse200(BaseModel):
+class GetMyAgentResponse200(BaseModel):
     """
     Attributes:
-        data (FulfillContractResponse200Data):
+        data (Agent):
     """
 
-    data: "FulfillContractResponse200Data" = Field(alias="data")
+    data: "Agent" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/fulfill_contract_response_200_data.py` & `spacetraders-0.3.0/spacetraders/models/accept_contract_response_200_data.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,32 +1,24 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.agent import Agent
 from ..models.contract import Contract
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="FulfillContractResponse200Data")
+T = TypeVar("T", bound="AcceptContractResponse200Data")
 
 
-class FulfillContractResponse200Data(BaseModel):
+class AcceptContractResponse200Data(BaseModel):
     """
     Attributes:
         agent (Agent):
         contract (Contract):
     """
 
     agent: "Agent" = Field(alias="agent")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_contract_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_system_response_200.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.contract import Contract
-from ..types import UNSET, Unset
+from ..models.system import System
+from ..types import Unset
 
-T = TypeVar("T", bound="GetContractResponse200")
+T = TypeVar("T", bound="GetSystemResponse200")
 
 
-class GetContractResponse200(BaseModel):
+class GetSystemResponse200(BaseModel):
     """
     Attributes:
-        data (Contract):
+        data (System):
     """
 
-    data: "Contract" = Field(alias="data")
+    data: "System" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_contracts_response_200.py` & `spacetraders-0.3.0/spacetraders/models/meta.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,40 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.contract import Contract
-from ..models.meta import Meta
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="GetContractsResponse200")
+T = TypeVar("T", bound="Meta")
 
 
-class GetContractsResponse200(BaseModel):
+class Meta(BaseModel):
     """
     Attributes:
-        data (List['Contract']):
-        meta (Meta):
+        total (int):
+        page (int):
+        limit (int):
     """
 
-    data: List["Contract"] = Field(alias="data")
-    meta: "Meta" = Field(alias="meta")
+    total: int = Field(alias="total")
+    page: int = Field(alias="page")
+    limit: int = Field(alias="limit")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_faction_response_200.py` & `spacetraders-0.3.0/spacetraders/models/jettison_json_body.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,37 +1,30 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.faction import Faction
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="GetFactionResponse200")
+T = TypeVar("T", bound="JettisonJsonBody")
 
 
-class GetFactionResponse200(BaseModel):
+class JettisonJsonBody(BaseModel):
     """
     Attributes:
-        data (Faction):
+        symbol (str):
+        units (int):
     """
 
-    data: "Faction" = Field(alias="data")
+    symbol: str = Field(alias="symbol")
+    units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_factions_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_my_ships_response_200.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,39 +1,31 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.faction import Faction
 from ..models.meta import Meta
-from ..types import UNSET, Unset
+from ..models.ship import Ship
+from ..types import Unset
 
-T = TypeVar("T", bound="GetFactionsResponse200")
+T = TypeVar("T", bound="GetMyShipsResponse200")
 
 
-class GetFactionsResponse200(BaseModel):
+class GetMyShipsResponse200(BaseModel):
     """
     Attributes:
-        data (List['Faction']):
+        data (List['Ship']):
         meta (Meta):
     """
 
-    data: List["Faction"] = Field(alias="data")
+    data: List["Ship"] = Field(alias="data")
     meta: "Meta" = Field(alias="meta")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_jump_gate_response_200.py` & `spacetraders-0.3.0/spacetraders/models/scanned_ship_mounts_item.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.jump_gate import JumpGate
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="GetJumpGateResponse200")
+T = TypeVar("T", bound="ScannedShipMountsItem")
 
 
-class GetJumpGateResponse200(BaseModel):
-    """
+class ScannedShipMountsItem(BaseModel):
+    """A mount on the ship.
+
     Attributes:
-        data (JumpGate):
+        symbol (str):
     """
 
-    data: "JumpGate" = Field(alias="data")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_market_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_market_response_200.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.market import Market
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetMarketResponse200")
 
 
 class GetMarketResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_my_agent_response_200.py` & `spacetraders-0.3.0/spacetraders/models/waypoint_faction.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,37 +1,28 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="GetMyAgentResponse200")
+T = TypeVar("T", bound="WaypointFaction")
 
 
-class GetMyAgentResponse200(BaseModel):
+class WaypointFaction(BaseModel):
     """
     Attributes:
-        data (Agent):
+        symbol (str):
     """
 
-    data: "Agent" = Field(alias="data")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_my_ship_cargo_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_my_ship_cargo_response_200.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_cargo import ShipCargo
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetMyShipCargoResponse200")
 
 
 class GetMyShipCargoResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_my_ship_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_my_ship_response_200.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship import Ship
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetMyShipResponse200")
 
 
 class GetMyShipResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_my_ships_response_200.py` & `spacetraders-0.3.0/spacetraders/models/warp_ship_json_body.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,40 +1,28 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.meta import Meta
-from ..models.ship import Ship
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="GetMyShipsResponse200")
+T = TypeVar("T", bound="WarpShipJsonBody")
 
 
-class GetMyShipsResponse200(BaseModel):
+class WarpShipJsonBody(BaseModel):
     """
     Attributes:
-        data (List['Ship']):
-        meta (Meta):
+        waypoint_symbol (str): The target destination.
     """
 
-    data: List["Ship"] = Field(alias="data")
-    meta: "Meta" = Field(alias="meta")
+    waypoint_symbol: str = Field(alias="waypointSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_ship_cooldown_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_ship_cooldown_response_200.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.cooldown import Cooldown
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetShipCooldownResponse200")
 
 
 class GetShipCooldownResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_ship_nav_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_ship_nav_response_200.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_nav import ShipNav
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetShipNavResponse200")
 
 
 class GetShipNavResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_shipyard_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_shipyard_response_200.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.shipyard import Shipyard
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetShipyardResponse200")
 
 
 class GetShipyardResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_system_response_200.py` & `spacetraders-0.3.0/spacetraders/models/sell_cargo_sell_cargo_request.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,37 +1,30 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.system import System
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="GetSystemResponse200")
+T = TypeVar("T", bound="SellCargoSellCargoRequest")
 
 
-class GetSystemResponse200(BaseModel):
+class SellCargoSellCargoRequest(BaseModel):
     """
     Attributes:
-        data (System):
+        symbol (str):
+        units (int):
     """
 
-    data: "System" = Field(alias="data")
+    symbol: str = Field(alias="symbol")
+    units: int = Field(alias="units")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_system_waypoints_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_system_waypoints_response_200.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,27 +1,19 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.meta import Meta
 from ..models.waypoint import Waypoint
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetSystemWaypointsResponse200")
 
 
 class GetSystemWaypointsResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_systems_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_systems_response_200.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,27 +1,19 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.meta import Meta
 from ..models.system import System
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetSystemsResponse200")
 
 
 class GetSystemsResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/get_waypoint_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_waypoint_response_200.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.waypoint import Waypoint
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="GetWaypointResponse200")
 
 
 class GetWaypointResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/jettison_json_body.py` & `spacetraders-0.3.0/spacetraders/models/scanned_system.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,37 +1,39 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.system_type import SystemType
+from ..types import Unset
 
-T = TypeVar("T", bound="JettisonJsonBody")
+T = TypeVar("T", bound="ScannedSystem")
 
 
-class JettisonJsonBody(BaseModel):
+class ScannedSystem(BaseModel):
     """
     Attributes:
         symbol (str):
-        units (int):
+        sector_symbol (str):
+        type (SystemType): The type of waypoint.
+        x (int):
+        y (int):
+        distance (int):
     """
 
     symbol: str = Field(alias="symbol")
-    units: int = Field(alias="units")
+    sector_symbol: str = Field(alias="sectorSymbol")
+    type: SystemType = Field(alias="type")
+    x: int = Field(alias="x")
+    y: int = Field(alias="y")
+    distance: int = Field(alias="distance")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/jettison_response_200.py` & `spacetraders-0.3.0/spacetraders/models/jettison_response_200.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.jettison_response_200_data import JettisonResponse200Data
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="JettisonResponse200")
 
 
 class JettisonResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/jettison_response_200_data.py` & `spacetraders-0.3.0/spacetraders/models/navigate_ship_json_body.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,37 +1,28 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_cargo import ShipCargo
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="JettisonResponse200Data")
+T = TypeVar("T", bound="NavigateShipJsonBody")
 
 
-class JettisonResponse200Data(BaseModel):
+class NavigateShipJsonBody(BaseModel):
     """
     Attributes:
-        cargo (ShipCargo):
+        waypoint_symbol (str): The target destination.
     """
 
-    cargo: "ShipCargo" = Field(alias="cargo")
+    waypoint_symbol: str = Field(alias="waypointSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/jump_gate.py` & `spacetraders-0.3.0/spacetraders/models/patch_ship_nav_response_200.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,43 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.connected_system import ConnectedSystem
-from ..types import UNSET, Unset
+from ..models.ship_nav import ShipNav
+from ..types import Unset
 
-T = TypeVar("T", bound="JumpGate")
+T = TypeVar("T", bound="PatchShipNavResponse200")
 
 
-class JumpGate(BaseModel):
+class PatchShipNavResponse200(BaseModel):
     """
     Attributes:
-        jump_range (float): The maximum jump range of the gate.
-        connected_systems (List['ConnectedSystem']): The systems within range of the gate that have a corresponding
-            gate.
-        faction_symbol (Union[Unset, str]): The symbol of the faction that owns the gate.
+        data (ShipNav): The navigation information of the ship.
     """
 
-    jump_range: float = Field(alias="jumpRange")
-    connected_systems: List["ConnectedSystem"] = Field(alias="connectedSystems")
-    faction_symbol: Union[Unset, str] = Field(UNSET, alias="factionSymbol")
+    data: "ShipNav" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/jump_ship_json_body.py` & `spacetraders-0.3.0/spacetraders/models/purchase_ship_json_body.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,35 +1,31 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.ship_type import ShipType
+from ..types import Unset
 
-T = TypeVar("T", bound="JumpShipJsonBody")
+T = TypeVar("T", bound="PurchaseShipJsonBody")
 
 
-class JumpShipJsonBody(BaseModel):
+class PurchaseShipJsonBody(BaseModel):
     """
     Attributes:
-        system_symbol (str): The system symbol to jump to.
+        ship_type (ShipType):
+        waypoint_symbol (str): The symbol of the waypoint you want to purchase the ship at.
     """
 
-    system_symbol: str = Field(alias="systemSymbol")
+    ship_type: ShipType = Field(alias="shipType")
+    waypoint_symbol: str = Field(alias="waypointSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/jump_ship_response_200.py` & `spacetraders-0.3.0/spacetraders/models/dock_ship_dock_ship_200_response.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,37 +1,31 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.jump_ship_response_200_data import JumpShipResponse200Data
-from ..types import UNSET, Unset
+from ..models.dock_ship_dock_ship_200_response_data import (
+    DockShipDockShip200ResponseData,
+)
+from ..types import Unset
 
-T = TypeVar("T", bound="JumpShipResponse200")
+T = TypeVar("T", bound="DockShipDockShip200Response")
 
 
-class JumpShipResponse200(BaseModel):
+class DockShipDockShip200Response(BaseModel):
     """
     Attributes:
-        data (JumpShipResponse200Data):
+        data (DockShipDockShip200ResponseData):
     """
 
-    data: "JumpShipResponse200Data" = Field(alias="data")
+    data: "DockShipDockShip200ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/jump_ship_response_200_data.py` & `spacetraders-0.3.0/spacetraders/models/jump_ship_response_200_data.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.cooldown import Cooldown
 from ..models.ship_nav import ShipNav
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="JumpShipResponse200Data")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/market.py` & `spacetraders-0.3.0/spacetraders/models/market.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.market_trade_good import MarketTradeGood
 from ..models.market_transaction import MarketTransaction
 from ..models.trade_good import TradeGood
 from ..types import UNSET, Unset
```

### Comparing `spacetraders-0.2.4/spacetraders/models/market_trade_good.py` & `spacetraders-0.3.0/spacetraders/models/market_trade_good.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,25 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.market_trade_good_supply import MarketTradeGoodSupply
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="MarketTradeGood")
 
 
 class MarketTradeGood(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/market_transaction.py` & `spacetraders-0.3.0/spacetraders/models/market_transaction.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,28 +1,19 @@
 import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
 from ..models.market_transaction_type import MarketTransactionType
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="MarketTransaction")
 
 
 class MarketTransaction(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/meta.py` & `spacetraders-0.3.0/spacetraders/models/jump_gate.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,39 +1,35 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
+    Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
+from ..models.connected_system import ConnectedSystem
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="Meta")
+T = TypeVar("T", bound="JumpGate")
 
 
-class Meta(BaseModel):
+class JumpGate(BaseModel):
     """
     Attributes:
-        total (int):
-        page (int):
-        limit (int):
+        jump_range (float): The maximum jump range of the gate.
+        connected_systems (List['ConnectedSystem']): The systems within range of the gate that have a corresponding
+            gate.
+        faction_symbol (Union[Unset, str]): The symbol of the faction that owns the gate.
     """
 
-    total: int = Field(alias="total")
-    page: int = Field(alias="page")
-    limit: int = Field(alias="limit")
+    jump_range: float = Field(alias="jumpRange")
+    connected_systems: List["ConnectedSystem"] = Field(alias="connectedSystems")
+    faction_symbol: Union[Unset, str] = Field(UNSET, alias="factionSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/navigate_ship_json_body.py` & `spacetraders-0.3.0/spacetraders/models/scanned_ship_engine.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,35 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="NavigateShipJsonBody")
+T = TypeVar("T", bound="ScannedShipEngine")
 
 
-class NavigateShipJsonBody(BaseModel):
-    """
+class ScannedShipEngine(BaseModel):
+    """The engine of the ship.
+
     Attributes:
-        waypoint_symbol (str): The target destination.
+        symbol (str):
     """
 
-    waypoint_symbol: str = Field(alias="waypointSymbol")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/navigate_ship_response_200.py` & `spacetraders-0.3.0/spacetraders/models/navigate_ship_response_200.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.navigate_ship_response_200_data import NavigateShipResponse200Data
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="NavigateShipResponse200")
 
 
 class NavigateShipResponse200(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/navigate_ship_response_200_data.py` & `spacetraders-0.3.0/spacetraders/models/orbit_ship_orbit_ship_200_response_data.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,40 +1,28 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_fuel import ShipFuel
 from ..models.ship_nav import ShipNav
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="NavigateShipResponse200Data")
+T = TypeVar("T", bound="OrbitShipOrbitShip200ResponseData")
 
 
-class NavigateShipResponse200Data(BaseModel):
+class OrbitShipOrbitShip200ResponseData(BaseModel):
     """
     Attributes:
-        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
-            or action.
         nav (ShipNav): The navigation information of the ship.
     """
 
-    fuel: "ShipFuel" = Field(alias="fuel")
     nav: "ShipNav" = Field(alias="nav")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
```

### Comparing `spacetraders-0.2.4/spacetraders/models/orbit_ship_orbit_ship_200_response.py` & `spacetraders-0.3.0/spacetraders/models/orbit_ship_orbit_ship_200_response.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.orbit_ship_orbit_ship_200_response_data import (
     OrbitShipOrbitShip200ResponseData,
 )
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="OrbitShipOrbitShip200Response")
 
 
 class OrbitShipOrbitShip200Response(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/orbit_ship_orbit_ship_200_response_data.py` & `spacetraders-0.3.0/spacetraders/models/get_jump_gate_response_200.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_nav import ShipNav
-from ..types import UNSET, Unset
+from ..models.jump_gate import JumpGate
+from ..types import Unset
 
-T = TypeVar("T", bound="OrbitShipOrbitShip200ResponseData")
+T = TypeVar("T", bound="GetJumpGateResponse200")
 
 
-class OrbitShipOrbitShip200ResponseData(BaseModel):
+class GetJumpGateResponse200(BaseModel):
     """
     Attributes:
-        nav (ShipNav): The navigation information of the ship.
+        data (JumpGate):
     """
 
-    nav: "ShipNav" = Field(alias="nav")
+    data: "JumpGate" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/patch_ship_nav_json_body.py` & `spacetraders-0.3.0/spacetraders/models/patch_ship_nav_json_body.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,26 +1,19 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_nav_flight_mode import ShipNavFlightMode
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="PatchShipNavJsonBody")
 
 
 class PatchShipNavJsonBody(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/patch_ship_nav_response_200.py` & `spacetraders-0.3.0/spacetraders/models/system_faction.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,37 +1,28 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_nav import ShipNav
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="PatchShipNavResponse200")
+T = TypeVar("T", bound="SystemFaction")
 
 
-class PatchShipNavResponse200(BaseModel):
+class SystemFaction(BaseModel):
     """
     Attributes:
-        data (ShipNav): The navigation information of the ship.
+        symbol (str):
     """
 
-    data: "ShipNav" = Field(alias="data")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/purchase_cargo_purchase_cargo_201_response.py` & `spacetraders-0.3.0/spacetraders/models/purchase_cargo_purchase_cargo_201_response.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.purchase_cargo_purchase_cargo_201_response_data import (
     PurchaseCargoPurchaseCargo201ResponseData,
 )
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="PurchaseCargoPurchaseCargo201Response")
 
 
 class PurchaseCargoPurchaseCargo201Response(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/purchase_cargo_purchase_cargo_201_response_data.py` & `spacetraders-0.3.0/spacetraders/models/purchase_cargo_purchase_cargo_201_response_data.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.agent import Agent
 from ..models.market_transaction import MarketTransaction
 from ..models.ship_cargo import ShipCargo
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="PurchaseCargoPurchaseCargo201ResponseData")
 
 
 class PurchaseCargoPurchaseCargo201ResponseData(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/purchase_cargo_purchase_cargo_request.py` & `spacetraders-0.3.0/spacetraders/models/transfer_cargo_transfer_cargo_request.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,37 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="PurchaseCargoPurchaseCargoRequest")
+T = TypeVar("T", bound="TransferCargoTransferCargoRequest")
 
 
-class PurchaseCargoPurchaseCargoRequest(BaseModel):
+class TransferCargoTransferCargoRequest(BaseModel):
     """
     Attributes:
-        symbol (str):
+        trade_symbol (str):
         units (int):
+        ship_symbol (str):
     """
 
-    symbol: str = Field(alias="symbol")
+    trade_symbol: str = Field(alias="tradeSymbol")
     units: int = Field(alias="units")
+    ship_symbol: str = Field(alias="shipSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/purchase_ship_json_body.py` & `spacetraders-0.3.0/spacetraders/models/jettison_response_200_data.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,38 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_type import ShipType
-from ..types import UNSET, Unset
+from ..models.ship_cargo import ShipCargo
+from ..types import Unset
 
-T = TypeVar("T", bound="PurchaseShipJsonBody")
+T = TypeVar("T", bound="JettisonResponse200Data")
 
 
-class PurchaseShipJsonBody(BaseModel):
+class JettisonResponse200Data(BaseModel):
     """
     Attributes:
-        ship_type (ShipType):
-        waypoint_symbol (str): The symbol of the waypoint you want to purchase the ship at.
+        cargo (ShipCargo):
     """
 
-    ship_type: ShipType = Field(alias="shipType")
-    waypoint_symbol: str = Field(alias="waypointSymbol")
+    cargo: "ShipCargo" = Field(alias="cargo")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/purchase_ship_response_201.py` & `spacetraders-0.3.0/spacetraders/models/register_response_201.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.purchase_ship_response_201_data import PurchaseShipResponse201Data
-from ..types import UNSET, Unset
+from ..models.register_response_201_data import RegisterResponse201Data
+from ..types import Unset
 
-T = TypeVar("T", bound="PurchaseShipResponse201")
+T = TypeVar("T", bound="RegisterResponse201")
 
 
-class PurchaseShipResponse201(BaseModel):
+class RegisterResponse201(BaseModel):
     """
     Attributes:
-        data (PurchaseShipResponse201Data):
+        data (RegisterResponse201Data):
     """
 
-    data: "PurchaseShipResponse201Data" = Field(alias="data")
+    data: "RegisterResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/purchase_ship_response_201_data.py` & `spacetraders-0.3.0/spacetraders/models/purchase_ship_response_201_data.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.agent import Agent
 from ..models.ship import Ship
 from ..models.shipyard_transaction import ShipyardTransaction
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="PurchaseShipResponse201Data")
 
 
 class PurchaseShipResponse201Data(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/refuel_ship_response_200.py` & `spacetraders-0.3.0/spacetraders/models/get_factions_response_200.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,37 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.refuel_ship_response_200_data import RefuelShipResponse200Data
-from ..types import UNSET, Unset
+from ..models.faction import Faction
+from ..models.meta import Meta
+from ..types import Unset
 
-T = TypeVar("T", bound="RefuelShipResponse200")
+T = TypeVar("T", bound="GetFactionsResponse200")
 
 
-class RefuelShipResponse200(BaseModel):
+class GetFactionsResponse200(BaseModel):
     """
     Attributes:
-        data (RefuelShipResponse200Data):
+        data (List['Faction']):
+        meta (Meta):
     """
 
-    data: "RefuelShipResponse200Data" = Field(alias="data")
+    data: List["Faction"] = Field(alias="data")
+    meta: "Meta" = Field(alias="meta")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/refuel_ship_response_200_data.py` & `spacetraders-0.3.0/spacetraders/models/waypoint_orbital.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,41 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..models.ship_fuel import ShipFuel
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="RefuelShipResponse200Data")
+T = TypeVar("T", bound="WaypointOrbital")
 
 
-class RefuelShipResponse200Data(BaseModel):
-    """
+class WaypointOrbital(BaseModel):
+    """An orbital is another waypoint that orbits a parent waypoint.
+
     Attributes:
-        agent (Agent):
-        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
-            or action.
+        symbol (str):
     """
 
-    agent: "Agent" = Field(alias="agent")
-    fuel: "ShipFuel" = Field(alias="fuel")
+    symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/register_json_body.py` & `spacetraders-0.3.0/spacetraders/models/register_json_body.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.register_json_body_faction import RegisterJsonBodyFaction
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="RegisterJsonBody")
 
 
 class RegisterJsonBody(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/register_response_201.py` & `spacetraders-0.3.0/spacetraders/models/ship_fuel_consumed.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,37 +1,31 @@
+import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.register_response_201_data import RegisterResponse201Data
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="RegisterResponse201")
+T = TypeVar("T", bound="ShipFuelConsumed")
 
 
-class RegisterResponse201(BaseModel):
+class ShipFuelConsumed(BaseModel):
     """
     Attributes:
-        data (RegisterResponse201Data):
+        amount (int): The amount of fuel consumed by the most recent transit or action.
+        timestamp (datetime.datetime): The time at which the fuel was consumed.
     """
 
-    data: "RegisterResponse201Data" = Field(alias="data")
+    amount: int = Field(alias="amount")
+    timestamp: datetime.datetime = Field(alias="timestamp")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/register_response_201_data.py` & `spacetraders-0.3.0/spacetraders/models/ship_refine_json_body.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,48 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.agent import Agent
-from ..models.contract import Contract
-from ..models.faction import Faction
-from ..models.ship import Ship
-from ..types import UNSET, Unset
+from ..models.ship_refine_json_body_produce import ShipRefineJsonBodyProduce
+from ..types import Unset
 
-T = TypeVar("T", bound="RegisterResponse201Data")
+T = TypeVar("T", bound="ShipRefineJsonBody")
 
 
-class RegisterResponse201Data(BaseModel):
+class ShipRefineJsonBody(BaseModel):
     """
     Attributes:
-        agent (Agent):
-        contract (Contract):
-        faction (Faction):
-        ship (Ship): A ship
-        token (str): A Bearer token for accessing secured API endpoints.
+        produce (ShipRefineJsonBodyProduce):
     """
 
-    agent: "Agent" = Field(alias="agent")
-    contract: "Contract" = Field(alias="contract")
-    faction: "Faction" = Field(alias="faction")
-    ship: "Ship" = Field(alias="ship")
-    token: str = Field(alias="token")
+    produce: ShipRefineJsonBodyProduce = Field(alias="produce")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/scanned_ship.py` & `spacetraders-0.3.0/spacetraders/models/scanned_ship.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.scanned_ship_engine import ScannedShipEngine
 from ..models.scanned_ship_frame import ScannedShipFrame
 from ..models.scanned_ship_mounts_item import ScannedShipMountsItem
 from ..models.scanned_ship_reactor import ScannedShipReactor
 from ..models.ship_nav import ShipNav
```

### Comparing `spacetraders-0.2.4/spacetraders/models/scanned_ship_engine.py` & `spacetraders-0.3.0/spacetraders/models/ship_nav_route_waypoint.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,36 +1,38 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.waypoint_type import WaypointType
+from ..types import Unset
 
-T = TypeVar("T", bound="ScannedShipEngine")
+T = TypeVar("T", bound="ShipNavRouteWaypoint")
 
 
-class ScannedShipEngine(BaseModel):
-    """The engine of the ship.
+class ShipNavRouteWaypoint(BaseModel):
+    """The destination or departure of a ships nav route.
 
     Attributes:
         symbol (str):
+        type (WaypointType): The type of waypoint.
+        system_symbol (str):
+        x (int):
+        y (int):
     """
 
     symbol: str = Field(alias="symbol")
+    type: WaypointType = Field(alias="type")
+    system_symbol: str = Field(alias="systemSymbol")
+    x: int = Field(alias="x")
+    y: int = Field(alias="y")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/scanned_ship_frame.py` & `spacetraders-0.3.0/spacetraders/models/shipyard_ship_types_item.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,36 +1,30 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
+    Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
+from ..models.ship_type import ShipType
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="ScannedShipFrame")
+T = TypeVar("T", bound="ShipyardShipTypesItem")
 
 
-class ScannedShipFrame(BaseModel):
-    """The frame of the ship.
-
+class ShipyardShipTypesItem(BaseModel):
+    """
     Attributes:
-        symbol (str):
+        type (Union[Unset, ShipType]):
     """
 
-    symbol: str = Field(alias="symbol")
+    type: Union[Unset, ShipType] = Field(UNSET, alias="type")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/scanned_ship_mounts_item.py` & `spacetraders-0.3.0/spacetraders/models/scanned_ship_reactor.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,30 +1,23 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="ScannedShipMountsItem")
+T = TypeVar("T", bound="ScannedShipReactor")
 
 
-class ScannedShipMountsItem(BaseModel):
-    """A mount on the ship.
+class ScannedShipReactor(BaseModel):
+    """The reactor of the ship.
 
     Attributes:
         symbol (str):
     """
 
     symbol: str = Field(alias="symbol")
     additional_properties: Dict[str, Any] = {}
```

### Comparing `spacetraders-0.2.4/spacetraders/models/scanned_ship_reactor.py` & `spacetraders-0.3.0/spacetraders/models/sell_cargo_sell_cargo_201_response.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,36 +1,31 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
-
-T = TypeVar("T", bound="ScannedShipReactor")
+from ..models.sell_cargo_sell_cargo_201_response_data import (
+    SellCargoSellCargo201ResponseData,
+)
+from ..types import Unset
 
+T = TypeVar("T", bound="SellCargoSellCargo201Response")
 
-class ScannedShipReactor(BaseModel):
-    """The reactor of the ship.
 
+class SellCargoSellCargo201Response(BaseModel):
+    """
     Attributes:
-        symbol (str):
+        data (SellCargoSellCargo201ResponseData):
     """
 
-    symbol: str = Field(alias="symbol")
+    data: "SellCargoSellCargo201ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/scanned_system.py` & `spacetraders-0.3.0/spacetraders/models/system_waypoint.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,46 +1,35 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.system_type import SystemType
-from ..types import UNSET, Unset
+from ..models.waypoint_type import WaypointType
+from ..types import Unset
 
-T = TypeVar("T", bound="ScannedSystem")
+T = TypeVar("T", bound="SystemWaypoint")
 
 
-class ScannedSystem(BaseModel):
+class SystemWaypoint(BaseModel):
     """
     Attributes:
         symbol (str):
-        sector_symbol (str):
-        type (SystemType): The type of waypoint.
+        type (WaypointType): The type of waypoint.
         x (int):
         y (int):
-        distance (int):
     """
 
     symbol: str = Field(alias="symbol")
-    sector_symbol: str = Field(alias="sectorSymbol")
-    type: SystemType = Field(alias="type")
+    type: WaypointType = Field(alias="type")
     x: int = Field(alias="x")
     y: int = Field(alias="y")
-    distance: int = Field(alias="distance")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/scanned_waypoint.py` & `spacetraders-0.3.0/spacetraders/models/scanned_waypoint.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.chart import Chart
 from ..models.waypoint_faction import WaypointFaction
 from ..models.waypoint_orbital import WaypointOrbital
 from ..models.waypoint_trait import WaypointTrait
 from ..models.waypoint_type import WaypointType
```

### Comparing `spacetraders-0.2.4/spacetraders/models/sell_cargo_sell_cargo_201_response.py` & `spacetraders-0.3.0/spacetraders/models/transfer_cargo_transfer_cargo_200_response.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,39 +1,31 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.sell_cargo_sell_cargo_201_response_data import (
-    SellCargoSellCargo201ResponseData,
+from ..models.transfer_cargo_transfer_cargo_200_response_data import (
+    TransferCargoTransferCargo200ResponseData,
 )
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="SellCargoSellCargo201Response")
+T = TypeVar("T", bound="TransferCargoTransferCargo200Response")
 
 
-class SellCargoSellCargo201Response(BaseModel):
+class TransferCargoTransferCargo200Response(BaseModel):
     """
     Attributes:
-        data (SellCargoSellCargo201ResponseData):
+        data (TransferCargoTransferCargo200ResponseData):
     """
 
-    data: "SellCargoSellCargo201ResponseData" = Field(alias="data")
+    data: "TransferCargoTransferCargo200ResponseData" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/sell_cargo_sell_cargo_201_response_data.py` & `spacetraders-0.3.0/spacetraders/models/sell_cargo_sell_cargo_201_response_data.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.agent import Agent
 from ..models.market_transaction import MarketTransaction
 from ..models.ship_cargo import ShipCargo
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="SellCargoSellCargo201ResponseData")
 
 
 class SellCargoSellCargo201ResponseData(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/sell_cargo_sell_cargo_request.py` & `spacetraders-0.3.0/spacetraders/models/create_chart_response_201.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.create_chart_response_201_data import CreateChartResponse201Data
+from ..types import Unset
 
-T = TypeVar("T", bound="SellCargoSellCargoRequest")
+T = TypeVar("T", bound="CreateChartResponse201")
 
 
-class SellCargoSellCargoRequest(BaseModel):
+class CreateChartResponse201(BaseModel):
     """
     Attributes:
-        symbol (str):
-        units (int):
+        data (CreateChartResponse201Data):
     """
 
-    symbol: str = Field(alias="symbol")
-    units: int = Field(alias="units")
+    data: "CreateChartResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship.py` & `spacetraders-0.3.0/spacetraders/models/ship.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,35 +1,27 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_cargo import ShipCargo
 from ..models.ship_crew import ShipCrew
 from ..models.ship_engine import ShipEngine
 from ..models.ship_frame import ShipFrame
 from ..models.ship_fuel import ShipFuel
 from ..models.ship_module import ShipModule
 from ..models.ship_mount import ShipMount
 from ..models.ship_nav import ShipNav
 from ..models.ship_reactor import ShipReactor
 from ..models.ship_registration import ShipRegistration
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="Ship")
 
 
 class Ship(BaseModel):
     """A ship
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_cargo.py` & `spacetraders-0.3.0/spacetraders/models/ship_cargo.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_cargo_item import ShipCargoItem
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ShipCargo")
 
 
 class ShipCargo(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_cargo_item.py` & `spacetraders-0.3.0/spacetraders/models/ship_cargo_item.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,24 +1,17 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ShipCargoItem")
 
 
 class ShipCargoItem(BaseModel):
     """The type of cargo item and the number of units.
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_crew.py` & `spacetraders-0.3.0/spacetraders/models/ship_crew.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,25 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_crew_rotation import ShipCrewRotation
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ShipCrew")
 
 
 class ShipCrew(BaseModel):
     """The ship's crew service and maintain the ship's systems and equipment.
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_engine.py` & `spacetraders-0.3.0/spacetraders/models/ship_engine.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_engine_symbol import ShipEngineSymbol
 from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ShipEngine")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_frame.py` & `spacetraders-0.3.0/spacetraders/models/ship_frame.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_frame_symbol import ShipFrameSymbol
 from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ShipFrame")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_frame_symbol.py` & `spacetraders-0.3.0/spacetraders/models/ship_frame_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_fuel.py` & `spacetraders-0.3.0/spacetraders/models/ship_fuel.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_fuel_consumed import ShipFuelConsumed
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ShipFuel")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_fuel_consumed.py` & `spacetraders-0.3.0/spacetraders/models/jump_ship_json_body.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,40 +1,28 @@
-import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="ShipFuelConsumed")
+T = TypeVar("T", bound="JumpShipJsonBody")
 
 
-class ShipFuelConsumed(BaseModel):
+class JumpShipJsonBody(BaseModel):
     """
     Attributes:
-        amount (int): The amount of fuel consumed by the most recent transit or action.
-        timestamp (datetime.datetime): The time at which the fuel was consumed.
+        system_symbol (str): The system symbol to jump to.
     """
 
-    amount: int = Field(alias="amount")
-    timestamp: datetime.datetime = Field(alias="timestamp")
+    system_symbol: str = Field(alias="systemSymbol")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_module.py` & `spacetraders-0.3.0/spacetraders/models/ship_module.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_module_symbol import ShipModuleSymbol
 from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ShipModule")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_module_symbol.py` & `spacetraders-0.3.0/spacetraders/models/ship_module_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_mount.py` & `spacetraders-0.3.0/spacetraders/models/ship_mount.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_mount_deposits_item import ShipMountDepositsItem
 from ..models.ship_mount_symbol import ShipMountSymbol
 from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_mount_deposits_item.py` & `spacetraders-0.3.0/spacetraders/models/ship_mount_deposits_item.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_mount_symbol.py` & `spacetraders-0.3.0/spacetraders/models/ship_mount_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_nav.py` & `spacetraders-0.3.0/spacetraders/models/ship_nav.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_nav_flight_mode import ShipNavFlightMode
 from ..models.ship_nav_route import ShipNavRoute
 from ..models.ship_nav_status import ShipNavStatus
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ShipNav")
 
 
 class ShipNav(BaseModel):
     """The navigation information of the ship.
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_nav_route.py` & `spacetraders-0.3.0/spacetraders/models/ship_nav_route.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,28 +1,19 @@
 import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
 from ..models.ship_nav_route_waypoint import ShipNavRouteWaypoint
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ShipNavRoute")
 
 
 class ShipNavRoute(BaseModel):
     """The routing information for the ship's most recent transit or current location.
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_nav_route_waypoint.py` & `spacetraders-0.3.0/spacetraders/models/system.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,45 +1,43 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.waypoint_type import WaypointType
-from ..types import UNSET, Unset
+from ..models.system_faction import SystemFaction
+from ..models.system_type import SystemType
+from ..models.system_waypoint import SystemWaypoint
+from ..types import Unset
 
-T = TypeVar("T", bound="ShipNavRouteWaypoint")
+T = TypeVar("T", bound="System")
 
 
-class ShipNavRouteWaypoint(BaseModel):
-    """The destination or departure of a ships nav route.
-
+class System(BaseModel):
+    """
     Attributes:
         symbol (str):
-        type (WaypointType): The type of waypoint.
-        system_symbol (str):
+        sector_symbol (str):
+        type (SystemType): The type of waypoint.
         x (int):
         y (int):
+        waypoints (List['SystemWaypoint']):
+        factions (List['SystemFaction']):
     """
 
     symbol: str = Field(alias="symbol")
-    type: WaypointType = Field(alias="type")
-    system_symbol: str = Field(alias="systemSymbol")
+    sector_symbol: str = Field(alias="sectorSymbol")
+    type: SystemType = Field(alias="type")
     x: int = Field(alias="x")
     y: int = Field(alias="y")
+    waypoints: List["SystemWaypoint"] = Field(alias="waypoints")
+    factions: List["SystemFaction"] = Field(alias="factions")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_reactor.py` & `spacetraders-0.3.0/spacetraders/models/ship_reactor.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_reactor_symbol import ShipReactorSymbol
 from ..models.ship_requirements import ShipRequirements
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ShipReactor")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_refine_ship_refine_200_response.py` & `spacetraders-0.3.0/spacetraders/models/ship_refine_ship_refine_200_response.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_refine_ship_refine_200_response_data import (
     ShipRefineShipRefine200ResponseData,
 )
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ShipRefineShipRefine200Response")
 
 
 class ShipRefineShipRefine200Response(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_refine_ship_refine_200_response_data.py` & `spacetraders-0.3.0/spacetraders/models/ship_refine_ship_refine_200_response_data.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,33 +1,25 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.cooldown import Cooldown
 from ..models.ship_cargo import ShipCargo
 from ..models.ship_refine_ship_refine_200_response_data_consumed_item import (
     ShipRefineShipRefine200ResponseDataConsumedItem,
 )
 from ..models.ship_refine_ship_refine_200_response_data_produced_item import (
     ShipRefineShipRefine200ResponseDataProducedItem,
 )
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ShipRefineShipRefine200ResponseData")
 
 
 class ShipRefineShipRefine200ResponseData(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_refine_ship_refine_200_response_data_consumed_item.py` & `spacetraders-0.3.0/spacetraders/models/ship_refine_ship_refine_200_response_data_consumed_item.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,22 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ShipRefineShipRefine200ResponseDataConsumedItem")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_refine_ship_refine_200_response_data_produced_item.py` & `spacetraders-0.3.0/spacetraders/models/ship_refine_ship_refine_200_response_data_produced_item.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,22 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ShipRefineShipRefine200ResponseDataProducedItem")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_registration.py` & `spacetraders-0.3.0/spacetraders/models/ship_registration.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,22 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_role import ShipRole
 from ..types import UNSET, Unset
 
 T = TypeVar("T", bound="ShipRegistration")
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_requirements.py` & `spacetraders-0.3.0/spacetraders/models/navigate_ship_response_200_data.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,41 +1,33 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.ship_fuel import ShipFuel
+from ..models.ship_nav import ShipNav
+from ..types import Unset
 
-T = TypeVar("T", bound="ShipRequirements")
+T = TypeVar("T", bound="NavigateShipResponse200Data")
 
 
-class ShipRequirements(BaseModel):
-    """The requirements for installation on a ship
-
+class NavigateShipResponse200Data(BaseModel):
+    """
     Attributes:
-        power (Union[Unset, int]): The amount of power required from the reactor.
-        crew (Union[Unset, int]): The number of crew required for operation.
-        slots (Union[Unset, int]): The number of module slots required for installation.
+        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
+            or action.
+        nav (ShipNav): The navigation information of the ship.
     """
 
-    power: Union[Unset, int] = Field(UNSET, alias="power")
-    crew: Union[Unset, int] = Field(UNSET, alias="crew")
-    slots: Union[Unset, int] = Field(UNSET, alias="slots")
+    fuel: "ShipFuel" = Field(alias="fuel")
+    nav: "ShipNav" = Field(alias="nav")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/ship_type.py` & `spacetraders-0.3.0/spacetraders/models/ship_type.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/models/shipyard.py` & `spacetraders-0.3.0/spacetraders/models/shipyard.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.shipyard_ship import ShipyardShip
 from ..models.shipyard_ship_types_item import ShipyardShipTypesItem
 from ..models.shipyard_transaction import ShipyardTransaction
 from ..types import UNSET, Unset
```

### Comparing `spacetraders-0.2.4/spacetraders/models/shipyard_ship.py` & `spacetraders-0.3.0/spacetraders/models/shipyard_ship.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_engine import ShipEngine
 from ..models.ship_frame import ShipFrame
 from ..models.ship_module import ShipModule
 from ..models.ship_mount import ShipMount
 from ..models.ship_reactor import ShipReactor
```

### Comparing `spacetraders-0.2.4/spacetraders/models/shipyard_ship_types_item.py` & `spacetraders-0.3.0/spacetraders/models/purchase_ship_response_201.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.ship_type import ShipType
-from ..types import UNSET, Unset
+from ..models.purchase_ship_response_201_data import PurchaseShipResponse201Data
+from ..types import Unset
 
-T = TypeVar("T", bound="ShipyardShipTypesItem")
+T = TypeVar("T", bound="PurchaseShipResponse201")
 
 
-class ShipyardShipTypesItem(BaseModel):
+class PurchaseShipResponse201(BaseModel):
     """
     Attributes:
-        type (Union[Unset, ShipType]):
+        data (PurchaseShipResponse201Data):
     """
 
-    type: Union[Unset, ShipType] = Field(UNSET, alias="type")
+    data: "PurchaseShipResponse201Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/shipyard_transaction.py` & `spacetraders-0.3.0/spacetraders/models/shipyard_transaction.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,27 +1,18 @@
 import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="ShipyardTransaction")
 
 
 class ShipyardTransaction(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/survey.py` & `spacetraders-0.3.0/spacetraders/models/survey.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,29 +1,20 @@
 import datetime
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
-from dateutil.parser import isoparse
 from pydantic import BaseModel, Field
 
 from ..models.survey_deposit import SurveyDeposit
 from ..models.survey_size import SurveySize
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="Survey")
 
 
 class Survey(BaseModel):
     """A resource survey of a waypoint, detailing a specific extraction location and the types of resources that can be
     found there.
```

### Comparing `spacetraders-0.2.4/spacetraders/models/survey_deposit.py` & `spacetraders-0.3.0/spacetraders/models/survey_deposit.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,24 +1,17 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="SurveyDeposit")
 
 
 class SurveyDeposit(BaseModel):
     """A surveyed deposit of a mineral or resource available for extraction.
```

### Comparing `spacetraders-0.2.4/spacetraders/models/system.py` & `spacetraders-0.3.0/spacetraders/models/trade_good.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,51 +1,33 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.system_faction import SystemFaction
-from ..models.system_type import SystemType
-from ..models.system_waypoint import SystemWaypoint
-from ..types import UNSET, Unset
+from ..models.trade_symbol import TradeSymbol
+from ..types import Unset
 
-T = TypeVar("T", bound="System")
+T = TypeVar("T", bound="TradeGood")
 
 
-class System(BaseModel):
+class TradeGood(BaseModel):
     """
     Attributes:
-        symbol (str):
-        sector_symbol (str):
-        type (SystemType): The type of waypoint.
-        x (int):
-        y (int):
-        waypoints (List['SystemWaypoint']):
-        factions (List['SystemFaction']):
+        symbol (TradeSymbol):
+        name (str):
+        description (str):
     """
 
-    symbol: str = Field(alias="symbol")
-    sector_symbol: str = Field(alias="sectorSymbol")
-    type: SystemType = Field(alias="type")
-    x: int = Field(alias="x")
-    y: int = Field(alias="y")
-    waypoints: List["SystemWaypoint"] = Field(alias="waypoints")
-    factions: List["SystemFaction"] = Field(alias="factions")
+    symbol: TradeSymbol = Field(alias="symbol")
+    name: str = Field(alias="name")
+    description: str = Field(alias="description")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/system_faction.py` & `spacetraders-0.3.0/spacetraders/models/extract_resources_json_body.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,35 +1,31 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
+    Union,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
+from ..models.survey import Survey
 from ..types import UNSET, Unset
 
-T = TypeVar("T", bound="SystemFaction")
+T = TypeVar("T", bound="ExtractResourcesJsonBody")
 
 
-class SystemFaction(BaseModel):
+class ExtractResourcesJsonBody(BaseModel):
     """
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
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/system_waypoint.py` & `spacetraders-0.3.0/spacetraders/models/waypoint_trait.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,42 +1,33 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.waypoint_type import WaypointType
-from ..types import UNSET, Unset
+from ..models.waypoint_trait_symbol import WaypointTraitSymbol
+from ..types import Unset
 
-T = TypeVar("T", bound="SystemWaypoint")
+T = TypeVar("T", bound="WaypointTrait")
 
 
-class SystemWaypoint(BaseModel):
+class WaypointTrait(BaseModel):
     """
     Attributes:
-        symbol (str):
-        type (WaypointType): The type of waypoint.
-        x (int):
-        y (int):
+        symbol (WaypointTraitSymbol): The unique identifier of the trait.
+        name (str): The name of the trait.
+        description (str): A description of the trait.
     """
 
-    symbol: str = Field(alias="symbol")
-    type: WaypointType = Field(alias="type")
-    x: int = Field(alias="x")
-    y: int = Field(alias="y")
+    symbol: WaypointTraitSymbol = Field(alias="symbol")
+    name: str = Field(alias="name")
+    description: str = Field(alias="description")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/trade_good.py` & `spacetraders-0.3.0/spacetraders/models/contract_payment.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,40 +1,30 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.trade_symbol import TradeSymbol
-from ..types import UNSET, Unset
+from ..types import Unset
 
-T = TypeVar("T", bound="TradeGood")
+T = TypeVar("T", bound="ContractPayment")
 
 
-class TradeGood(BaseModel):
+class ContractPayment(BaseModel):
     """
     Attributes:
-        symbol (TradeSymbol):
-        name (str):
-        description (str):
+        on_accepted (int): The amount of credits received up front for accepting the contract.
+        on_fulfilled (int): The amount of credits received when the contract is fulfilled.
     """
 
-    symbol: TradeSymbol = Field(alias="symbol")
-    name: str = Field(alias="name")
-    description: str = Field(alias="description")
+    on_accepted: int = Field(alias="onAccepted")
+    on_fulfilled: int = Field(alias="onFulfilled")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/trade_symbol.py` & `spacetraders-0.3.0/spacetraders/models/trade_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/models/transfer_cargo_transfer_cargo_200_response.py` & `spacetraders-0.3.0/spacetraders/models/register_response_201_data.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,39 +1,40 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.transfer_cargo_transfer_cargo_200_response_data import (
-    TransferCargoTransferCargo200ResponseData,
-)
-from ..types import UNSET, Unset
+from ..models.agent import Agent
+from ..models.contract import Contract
+from ..models.faction import Faction
+from ..models.ship import Ship
+from ..types import Unset
 
-T = TypeVar("T", bound="TransferCargoTransferCargo200Response")
+T = TypeVar("T", bound="RegisterResponse201Data")
 
 
-class TransferCargoTransferCargo200Response(BaseModel):
+class RegisterResponse201Data(BaseModel):
     """
     Attributes:
-        data (TransferCargoTransferCargo200ResponseData):
+        agent (Agent):
+        contract (Contract):
+        faction (Faction):
+        ship (Ship): A ship
+        token (str): A Bearer token for accessing secured API endpoints.
     """
 
-    data: "TransferCargoTransferCargo200ResponseData" = Field(alias="data")
+    agent: "Agent" = Field(alias="agent")
+    contract: "Contract" = Field(alias="contract")
+    faction: "Faction" = Field(alias="faction")
+    ship: "Ship" = Field(alias="ship")
+    token: str = Field(alias="token")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/transfer_cargo_transfer_cargo_200_response_data.py` & `spacetraders-0.3.0/spacetraders/models/transfer_cargo_transfer_cargo_200_response_data.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,18 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_cargo import ShipCargo
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="TransferCargoTransferCargo200ResponseData")
 
 
 class TransferCargoTransferCargo200ResponseData(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/transfer_cargo_transfer_cargo_request.py` & `spacetraders-0.3.0/spacetraders/models/fulfill_contract_response_200.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,39 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.fulfill_contract_response_200_data import FulfillContractResponse200Data
+from ..types import Unset
 
-T = TypeVar("T", bound="TransferCargoTransferCargoRequest")
+T = TypeVar("T", bound="FulfillContractResponse200")
 
 
-class TransferCargoTransferCargoRequest(BaseModel):
+class FulfillContractResponse200(BaseModel):
     """
     Attributes:
-        trade_symbol (str):
-        units (int):
-        ship_symbol (str):
+        data (FulfillContractResponse200Data):
     """
 
-    trade_symbol: str = Field(alias="tradeSymbol")
-    units: int = Field(alias="units")
-    ship_symbol: str = Field(alias="shipSymbol")
+    data: "FulfillContractResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/warp_ship_json_body.py` & `spacetraders-0.3.0/spacetraders/models/warp_ship_response_200.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,35 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.warp_ship_response_200_data import WarpShipResponse200Data
+from ..types import Unset
 
-T = TypeVar("T", bound="WarpShipJsonBody")
+T = TypeVar("T", bound="WarpShipResponse200")
 
 
-class WarpShipJsonBody(BaseModel):
+class WarpShipResponse200(BaseModel):
     """
     Attributes:
-        waypoint_symbol (str): The target destination.
+        data (WarpShipResponse200Data):
     """
 
-    waypoint_symbol: str = Field(alias="waypointSymbol")
+    data: "WarpShipResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/warp_ship_response_200.py` & `spacetraders-0.3.0/spacetraders/models/refuel_ship_response_200.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,37 +1,29 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.warp_ship_response_200_data import WarpShipResponse200Data
-from ..types import UNSET, Unset
+from ..models.refuel_ship_response_200_data import RefuelShipResponse200Data
+from ..types import Unset
 
-T = TypeVar("T", bound="WarpShipResponse200")
+T = TypeVar("T", bound="RefuelShipResponse200")
 
 
-class WarpShipResponse200(BaseModel):
+class RefuelShipResponse200(BaseModel):
     """
     Attributes:
-        data (WarpShipResponse200Data):
+        data (RefuelShipResponse200Data):
     """
 
-    data: "WarpShipResponse200Data" = Field(alias="data")
+    data: "RefuelShipResponse200Data" = Field(alias="data")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/warp_ship_response_200_data.py` & `spacetraders-0.3.0/spacetraders/models/warp_ship_response_200_data.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,27 +1,19 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.ship_fuel import ShipFuel
 from ..models.ship_nav import ShipNav
-from ..types import UNSET, Unset
+from ..types import Unset
 
 T = TypeVar("T", bound="WarpShipResponse200Data")
 
 
 class WarpShipResponse200Data(BaseModel):
     """
     Attributes:
```

### Comparing `spacetraders-0.2.4/spacetraders/models/waypoint.py` & `spacetraders-0.3.0/spacetraders/models/waypoint.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,23 +1,15 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
     Union,
-    cast,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
 from ..models.chart import Chart
 from ..models.waypoint_faction import WaypointFaction
 from ..models.waypoint_orbital import WaypointOrbital
 from ..models.waypoint_trait import WaypointTrait
 from ..models.waypoint_type import WaypointType
```

### Comparing `spacetraders-0.2.4/spacetraders/models/waypoint_faction.py` & `spacetraders-0.3.0/spacetraders/models/refuel_ship_response_200_data.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,35 +1,33 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..types import UNSET, Unset
+from ..models.agent import Agent
+from ..models.ship_fuel import ShipFuel
+from ..types import Unset
 
-T = TypeVar("T", bound="WaypointFaction")
+T = TypeVar("T", bound="RefuelShipResponse200Data")
 
 
-class WaypointFaction(BaseModel):
+class RefuelShipResponse200Data(BaseModel):
     """
     Attributes:
-        symbol (str):
+        agent (Agent):
+        fuel (ShipFuel): Details of the ship's fuel tanks including how much fuel was consumed during the last transit
+            or action.
     """
 
-    symbol: str = Field(alias="symbol")
+    agent: "Agent" = Field(alias="agent")
+    fuel: "ShipFuel" = Field(alias="fuel")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/waypoint_trait.py` & `spacetraders-0.3.0/spacetraders/models/get_contracts_response_200.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,40 +1,32 @@
 from typing import (
-    TYPE_CHECKING,
     Any,
-    BinaryIO,
     Dict,
     List,
-    Optional,
-    TextIO,
-    Tuple,
-    Type,
     TypeVar,
 )
 
-import attr
 from pydantic import BaseModel, Field
 
-from ..models.waypoint_trait_symbol import WaypointTraitSymbol
-from ..types import UNSET, Unset
+from ..models.contract import Contract
+from ..models.meta import Meta
+from ..types import Unset
 
-T = TypeVar("T", bound="WaypointTrait")
+T = TypeVar("T", bound="GetContractsResponse200")
 
 
-class WaypointTrait(BaseModel):
+class GetContractsResponse200(BaseModel):
     """
     Attributes:
-        symbol (WaypointTraitSymbol): The unique identifier of the trait.
-        name (str): The name of the trait.
-        description (str): A description of the trait.
+        data (List['Contract']):
+        meta (Meta):
     """
 
-    symbol: WaypointTraitSymbol = Field(alias="symbol")
-    name: str = Field(alias="name")
-    description: str = Field(alias="description")
+    data: List["Contract"] = Field(alias="data")
+    meta: "Meta" = Field(alias="meta")
     additional_properties: Dict[str, Any] = {}
 
     class Config:
         arbitrary_types_allowed = True
         allow_population_by_field_name = True
 
     def dict(self, *args, **kwargs):
```

### Comparing `spacetraders-0.2.4/spacetraders/models/waypoint_trait_symbol.py` & `spacetraders-0.3.0/spacetraders/models/waypoint_trait_symbol.py`

 * *Files identical despite different names*

### Comparing `spacetraders-0.2.4/spacetraders/types.py` & `spacetraders-0.3.0/spacetraders/types.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 """ Contains some shared types for properties """
 from http import HTTPStatus
 from typing import (
-    Any,
     BinaryIO,
     Generic,
     Literal,
     MutableMapping,
     Optional,
     Tuple,
     TypeVar,
 )
 
 import attr
+from pydantic import BaseModel
 
 
 class Unset:
     def __bool__(self) -> Literal[False]:
         return False
 
 
@@ -46,8 +46,22 @@
 
     status_code: HTTPStatus
     content: bytes
     headers: MutableMapping[str, str]
     parsed: Optional[T]
 
 
-__all__ = ["File", "Response", "FileJsonType"]
+class Error(BaseModel):
+    """API Error Model"""
+
+    status_code: HTTPStatus
+    message: str
+    code: Optional[str] = None
+    data: Optional[dict] = None
+    headers: MutableMapping[str, str]
+
+
+class ApiError(Exception):
+    """An API Error has occured"""
+
+
+__all__ = ["File", "Response", "FileJsonType", "ApiError", "Error"]
```

### Comparing `spacetraders-0.2.4/PKG-INFO` & `spacetraders-0.3.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spacetraders
-Version: 0.2.4
+Version: 0.3.0
 Summary: Python API for Space Traders
 License: Apache-2.0
 Author: Marco Ceppi
 Author-email: marco@ceppi.net
 Requires-Python: >=3.11,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3
```

