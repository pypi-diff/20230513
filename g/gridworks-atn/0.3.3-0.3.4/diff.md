# Comparing `tmp/gridworks_atn-0.3.3.tar.gz` & `tmp/gridworks_atn-0.3.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gridworks_atn-0.3.3.tar", max compression
+gzip compressed data, was "gridworks_atn-0.3.4.tar", max compression
```

## Comparing `gridworks_atn-0.3.3.tar` & `gridworks_atn-0.3.4.tar`

### file list

```diff
@@ -1,91 +1,91 @@
--rw-r--r--   0        0        0     1065 2023-05-12 13:49:29.851996 gridworks_atn-0.3.3/LICENSE
--rw-r--r--   0        0        0     3002 2023-05-12 13:49:29.851996 gridworks_atn-0.3.3/README.md
--rw-r--r--   0        0        0     2193 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/pyproject.toml
--rw-r--r--   0        0        0      681 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/src/gwatn/__init__.py
--rw-r--r--   0        0        0      226 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/__main__.py
--rw-r--r--   0        0        0    13411 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/api_types.py
--rw-r--r--   0        0        0    21728 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/atn_actor_base.py
--rw-r--r--   0        0        0     1655 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/atn_utils.py
--rw-r--r--   0        0        0    19478 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/atn.py
--rw-r--r--   0        0        0       98 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/dev_atn_params_data.csv
--rw-r--r--   0        0        0      867 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/edge.py
--rw-r--r--   0        0        0     7536 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/flo.py
--rw-r--r--   0        0        0    18484 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/flo_output.py
--rw-r--r--   0        0        0     2014 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/make_dev_input_data.py
--rw-r--r--   0        0        0      841 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/node.py
--rw-r--r--   0        0        0     6963 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/simple_scada_sim.py
--rw-r--r--   0        0        0     2472 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/strategy_utils.py
--rw-r--r--   0        0        0     4575 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/src/gwatn/config.py
--rw-r--r--   0        0        0       43 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/src/gwatn/conversion_factors.py
--rw-r--r--   0        0        0     6148 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/data_classes/.DS_Store
--rw-r--r--   0        0        0      677 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/src/gwatn/data_classes/__init__.py
--rw-r--r--   0        0        0      577 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/src/gwatn/data_classes/d_edge.py
--rw-r--r--   0        0        0     7812 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/data_classes/d_graph.py
--rw-r--r--   0        0        0     1508 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/src/gwatn/data_classes/d_node.py
--rw-r--r--   0        0        0    14466 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/demo_methods.py
--rw-r--r--   0        0        0      276 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dev_utils/__init__.py
--rw-r--r--   0        0        0     1792 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dev_utils/dev_discoverer.py
--rw-r--r--   0        0        0    11883 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dev_utils/dev_ta_owner.py
--rw-r--r--   0        0        0    10994 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dev_utils/dev_validator.py
--rw-r--r--   0        0        0     1171 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dev_utils/make_plants.py
--rw-r--r--   0        0        0    11409 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dispatch_contract.py
--rw-r--r--   0        0        0    12463 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dispatch_contract_artifacts/application.json
--rw-r--r--   0        0        0     5229 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dispatch_contract_artifacts/approval.teal
--rw-r--r--   0        0        0       40 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dispatch_contract_artifacts/clear.teal
--rw-r--r--   0        0        0     3937 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/dispatch_contract_artifacts/contract.json
--rw-r--r--   0        0        0     2069 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/src/gwatn/enums/__init__.py
--rw-r--r--   0        0        0      700 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/enums/distribution_tariff.py
--rw-r--r--   0        0        0      614 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/enums/energy_supply_type.py
--rw-r--r--   0        0        0      947 2023-05-12 13:49:49.623992 gridworks_atn-0.3.3/src/gwatn/enums/recognized_irradiance_type.py
--rw-r--r--   0        0        0      570 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/enums/recognized_temperature_unit.py
--rw-r--r--   0        0        0      122 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/errors.py
--rw-r--r--   0        0        0        0 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/py.typed
--rw-r--r--   0        0        0     7945 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/python_ta_daemon.json
--rw-r--r--   0        0        0    12518 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/python_ta_daemon.py
--rw-r--r--   0        0        0      834 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/scada_codec.py
--rw-r--r--   0        0        0     4870 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/simple_atn_actor.py
--rw-r--r--   0        0        0    26139 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/simple_scada_sim_actor_base.py
--rw-r--r--   0        0        0     3169 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/ta_daemon_rest_api.py
--rw-r--r--   0        0        0      460 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/ta_validator_rest_api.py
--rw-r--r--   0        0        0    47761 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/two_channel_actor_base.py
--rw-r--r--   0        0        0    13145 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/types/__init__.py
--rw-r--r--   0        0        0     7868 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/types/accepted_bid.py
--rw-r--r--   0        0        0    20222 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/types/atn_bid.py
--rw-r--r--   0        0        0     4288 2023-05-12 13:49:29.863996 gridworks_atn-0.3.3/src/gwatn/types/atn_params.py
--rw-r--r--   0        0        0    22335 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/atn_params_brickstorageheater.py
--rw-r--r--   0        0        0     8144 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/atn_params_report.py
--rw-r--r--   0        0        0     8321 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/basegnode_scada_create.py
--rw-r--r--   0        0        0    11106 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/csv_distp_sync.py
--rw-r--r--   0        0        0    11354 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/csv_eprt_sync.py
--rw-r--r--   0        0        0    21761 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/csv_weather_forecast_sync.py
--rw-r--r--   0        0        0     1067 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/data_channel.py
--rw-r--r--   0        0        0     9885 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/discoverycert_algo_create.py
--rw-r--r--   0        0        0     8092 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/dispatch_contract_confirmed.py
--rw-r--r--   0        0        0     7648 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/flo_params.py
--rw-r--r--   0        0        0    22826 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/flo_params_brickstorageheater.py
--rw-r--r--   0        0        0     8827 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/flo_params_report.py
--rw-r--r--   0        0        0     8206 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/gt_dispatch_boolean.py
--rw-r--r--   0        0        0     9155 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/heartbeat_b.py
--rw-r--r--   0        0        0     6154 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/initial_tadeed_algo_create.py
--rw-r--r--   0        0        0     7610 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/initial_tadeed_algo_optin.py
--rw-r--r--   0        0        0     8932 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/initial_tadeed_algo_transfer.py
--rw-r--r--   0        0        0     7959 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/join_dispatch_contract.py
--rw-r--r--   0        0        0    12429 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/latest_price.py
--rw-r--r--   0        0        0     5028 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/market_slot.py
--rw-r--r--   0        0        0    17161 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/market_type_gt.py
--rw-r--r--   0        0        0     5294 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/new_tadeed_algo_optin.py
--rw-r--r--   0        0        0     5196 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/new_tadeed_send.py
--rw-r--r--   0        0        0     5024 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/old_tadeed_algo_return.py
--rw-r--r--   0        0        0     8461 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/price_quantity.py
--rw-r--r--   0        0        0     2492 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/price_quantity_unitless.py
--rw-r--r--   0        0        0     5004 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/scada_cert_transfer.py
--rw-r--r--   0        0        0     3682 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/simplesim_driver_data.py
--rw-r--r--   0        0        0     4166 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/simplesim_driver_data_bsh.py
--rw-r--r--   0        0        0     6534 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/simplesim_driver_report.py
--rw-r--r--   0        0        0     6774 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/simplesim_snapshot_brickstorageheater.py
--rw-r--r--   0        0        0     3220 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/sla_enter.py
--rw-r--r--   0        0        0     4101 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/tadeed_specs_hack.py
--rw-r--r--   0        0        0     5734 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/tavalidatorcert_algo_create.py
--rw-r--r--   0        0        0     6371 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/tavalidatorcert_algo_transfer.py
--rw-r--r--   0        0        0     5242 2023-05-12 13:49:29.867996 gridworks_atn-0.3.3/src/gwatn/types/terminalasset_certify_hack.py
--rw-r--r--   0        0        0     3949 1970-01-01 00:00:00.000000 gridworks_atn-0.3.3/PKG-INFO
+-rw-r--r--   0        0        0     1065 2023-05-13 12:50:21.758958 gridworks_atn-0.3.4/LICENSE
+-rw-r--r--   0        0        0     3002 2023-05-13 12:50:21.758958 gridworks_atn-0.3.4/README.md
+-rw-r--r--   0        0        0     2193 2023-05-13 12:50:40.230938 gridworks_atn-0.3.4/pyproject.toml
+-rw-r--r--   0        0        0      681 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/__init__.py
+-rw-r--r--   0        0        0      226 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/__main__.py
+-rw-r--r--   0        0        0    13411 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/api_types.py
+-rw-r--r--   0        0        0    21728 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/atn_actor_base.py
+-rw-r--r--   0        0        0     3114 2023-05-13 12:50:40.230938 gridworks_atn-0.3.4/src/gwatn/atn_utils.py
+-rw-r--r--   0        0        0    19478 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/atn.py
+-rw-r--r--   0        0        0       98 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/dev_atn_params_data.csv
+-rw-r--r--   0        0        0      867 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/edge.py
+-rw-r--r--   0        0        0     7536 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/flo.py
+-rw-r--r--   0        0        0    18484 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/flo_output.py
+-rw-r--r--   0        0        0     2014 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/make_dev_input_data.py
+-rw-r--r--   0        0        0      841 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/node.py
+-rw-r--r--   0        0        0     6963 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/simple_scada_sim.py
+-rw-r--r--   0        0        0     2472 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/strategy_utils.py
+-rw-r--r--   0        0        0     4575 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/config.py
+-rw-r--r--   0        0        0       43 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/conversion_factors.py
+-rw-r--r--   0        0        0     6148 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/data_classes/.DS_Store
+-rw-r--r--   0        0        0      677 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/data_classes/__init__.py
+-rw-r--r--   0        0        0      577 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/data_classes/d_edge.py
+-rw-r--r--   0        0        0     7812 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/data_classes/d_graph.py
+-rw-r--r--   0        0        0     1508 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/data_classes/d_node.py
+-rw-r--r--   0        0        0    14466 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/demo_methods.py
+-rw-r--r--   0        0        0      276 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/dev_utils/__init__.py
+-rw-r--r--   0        0        0     1792 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/dev_utils/dev_discoverer.py
+-rw-r--r--   0        0        0    11883 2023-05-13 12:50:21.766958 gridworks_atn-0.3.4/src/gwatn/dev_utils/dev_ta_owner.py
+-rw-r--r--   0        0        0    10994 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/dev_utils/dev_validator.py
+-rw-r--r--   0        0        0     1171 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/dev_utils/make_plants.py
+-rw-r--r--   0        0        0    11409 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/dispatch_contract.py
+-rw-r--r--   0        0        0    12463 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/dispatch_contract_artifacts/application.json
+-rw-r--r--   0        0        0     5229 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/dispatch_contract_artifacts/approval.teal
+-rw-r--r--   0        0        0       40 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/dispatch_contract_artifacts/clear.teal
+-rw-r--r--   0        0        0     3937 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/dispatch_contract_artifacts/contract.json
+-rw-r--r--   0        0        0     2069 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/enums/__init__.py
+-rw-r--r--   0        0        0      700 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/enums/distribution_tariff.py
+-rw-r--r--   0        0        0      614 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/enums/energy_supply_type.py
+-rw-r--r--   0        0        0      947 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/enums/recognized_irradiance_type.py
+-rw-r--r--   0        0        0      570 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/enums/recognized_temperature_unit.py
+-rw-r--r--   0        0        0      122 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/errors.py
+-rw-r--r--   0        0        0        0 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/py.typed
+-rw-r--r--   0        0        0     7945 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/python_ta_daemon.json
+-rw-r--r--   0        0        0    12518 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/python_ta_daemon.py
+-rw-r--r--   0        0        0      834 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/scada_codec.py
+-rw-r--r--   0        0        0     4870 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/simple_atn_actor.py
+-rw-r--r--   0        0        0    26139 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/simple_scada_sim_actor_base.py
+-rw-r--r--   0        0        0     3169 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/ta_daemon_rest_api.py
+-rw-r--r--   0        0        0      460 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/ta_validator_rest_api.py
+-rw-r--r--   0        0        0    47761 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/two_channel_actor_base.py
+-rw-r--r--   0        0        0    13145 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/__init__.py
+-rw-r--r--   0        0        0     7868 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/accepted_bid.py
+-rw-r--r--   0        0        0    20222 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/atn_bid.py
+-rw-r--r--   0        0        0     4288 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/atn_params.py
+-rw-r--r--   0        0        0    22335 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/atn_params_brickstorageheater.py
+-rw-r--r--   0        0        0     8144 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/atn_params_report.py
+-rw-r--r--   0        0        0     8321 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/basegnode_scada_create.py
+-rw-r--r--   0        0        0    11106 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/csv_distp_sync.py
+-rw-r--r--   0        0        0    11354 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/csv_eprt_sync.py
+-rw-r--r--   0        0        0    21761 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/csv_weather_forecast_sync.py
+-rw-r--r--   0        0        0     1067 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/data_channel.py
+-rw-r--r--   0        0        0     9885 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/discoverycert_algo_create.py
+-rw-r--r--   0        0        0     8092 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/dispatch_contract_confirmed.py
+-rw-r--r--   0        0        0     7648 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/flo_params.py
+-rw-r--r--   0        0        0    22826 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/flo_params_brickstorageheater.py
+-rw-r--r--   0        0        0     8827 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/flo_params_report.py
+-rw-r--r--   0        0        0     8206 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/gt_dispatch_boolean.py
+-rw-r--r--   0        0        0     9155 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/heartbeat_b.py
+-rw-r--r--   0        0        0     6154 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/initial_tadeed_algo_create.py
+-rw-r--r--   0        0        0     7610 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/initial_tadeed_algo_optin.py
+-rw-r--r--   0        0        0     8932 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/initial_tadeed_algo_transfer.py
+-rw-r--r--   0        0        0     7959 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/join_dispatch_contract.py
+-rw-r--r--   0        0        0    12429 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/latest_price.py
+-rw-r--r--   0        0        0     5028 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/market_slot.py
+-rw-r--r--   0        0        0    17161 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/market_type_gt.py
+-rw-r--r--   0        0        0     5294 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/new_tadeed_algo_optin.py
+-rw-r--r--   0        0        0     5196 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/new_tadeed_send.py
+-rw-r--r--   0        0        0     5024 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/old_tadeed_algo_return.py
+-rw-r--r--   0        0        0     8461 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/price_quantity.py
+-rw-r--r--   0        0        0     2492 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/price_quantity_unitless.py
+-rw-r--r--   0        0        0     5004 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/scada_cert_transfer.py
+-rw-r--r--   0        0        0     3682 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/simplesim_driver_data.py
+-rw-r--r--   0        0        0     4166 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/simplesim_driver_data_bsh.py
+-rw-r--r--   0        0        0     6534 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/simplesim_driver_report.py
+-rw-r--r--   0        0        0     6774 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/simplesim_snapshot_brickstorageheater.py
+-rw-r--r--   0        0        0     3220 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/sla_enter.py
+-rw-r--r--   0        0        0     4101 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/tadeed_specs_hack.py
+-rw-r--r--   0        0        0     5734 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/tavalidatorcert_algo_create.py
+-rw-r--r--   0        0        0     6371 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/tavalidatorcert_algo_transfer.py
+-rw-r--r--   0        0        0     5242 2023-05-13 12:50:21.770959 gridworks_atn-0.3.4/src/gwatn/types/terminalasset_certify_hack.py
+-rw-r--r--   0        0        0     3949 1970-01-01 00:00:00.000000 gridworks_atn-0.3.4/PKG-INFO
```

### Comparing `gridworks_atn-0.3.3/LICENSE` & `gridworks_atn-0.3.4/LICENSE`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/README.md` & `gridworks_atn-0.3.4/README.md`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/pyproject.toml` & `gridworks_atn-0.3.4/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "gridworks-atn"
-version = "0.3.3"
+version = "0.3.4"
 description = "Gridworks Atn Spaceheat"
 authors = ["Jessica Millar <jmillar@gridworks-consulting.com>"]
 license = "None"
 readme = "README.md"
 homepage = "https://github.com/thegridelectric/gridworks-atn"
 repository = "https://github.com/thegridelectric/gridworks-atn"
 documentation = "https://gridworks-atn.readthedocs.io"
```

### Comparing `gridworks_atn-0.3.3/src/gwatn/__init__.py` & `gridworks_atn-0.3.4/src/gwatn/__init__.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/api_types.py` & `gridworks_atn-0.3.4/src/gwatn/api_types.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/atn_actor_base.py` & `gridworks_atn-0.3.4/src/gwatn/atn_actor_base.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/atn_utils.py` & `gridworks_atn-0.3.4/src/gwatn/atn_utils.py`

 * *Files 24% similar despite different names*

```diff
@@ -38,7 +38,49 @@
     market_type_dc = MarketType.by_id[market_type_name]
     market_type = MarketTypeGt_Maker.dc_to_tuple(market_type_dc)
     market_maker_alias = ".".join(words[1:-1])
     slot_start = int(words[-1])
     return MarketSlot(
         Type=market_type, MarketMakerAlias=market_maker_alias, StartUnixS=slot_start
     )
+
+
+def market_name_from_market_slot_name(market_slot_name: str) -> str:
+    """
+    Returns market name from market slot name.
+
+    Raises ValueError if market_slot_name has incorrect format.
+
+    E.g takes rt60gate30b.d1.isone.ver.keene.1577836800 and returns rt60gate30b.d1.isone.ver.keene
+    """
+    try:
+        property_format.check_is_market_slot_name_lrd_format(market_slot_name)
+    except ValueError as e:
+        raise Exception(
+            f"market_slot_name {market_slot_name} does not have correct format!"
+        )
+    words = market_slot_name.split(".")
+    market_type_name = MarketTypeName(words[0])
+    market_type = MarketType.by_id[market_type_name]
+    market_maker_alias = ".".join(words[1:-1])
+    return f"{market_type.name.value}.{market_maker_alias}"
+
+
+def slot_start_s_from_market_slot_name(market_slot_name: str) -> int:
+    """
+    E.g takes rt60gate30b.d1.isone.ver.keene.1577836800 and returns 1577836800
+    Args:
+        market_slot_name (str): candidate string for market slot name
+
+    Raises: ValueError if market_slot_name has incorrect format.
+
+    Returns: slot start time in seconds
+    """
+    try:
+        property_format.check_is_market_slot_name_lrd_format(market_slot_name)
+    except ValueError as e:
+        raise Exception(
+            f"market_slot_name  {market_slot_name} does not correct format!"
+        )
+    x = market_slot_name.split(".")
+    slot_start_utc_s = x[-1]
+    return int(slot_start_utc_s)
```

### Comparing `gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/atn.py` & `gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/atn.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/edge.py` & `gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/edge.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/flo.py` & `gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/flo.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/flo_output.py` & `gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/flo_output.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/make_dev_input_data.py` & `gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/make_dev_input_data.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/node.py` & `gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/node.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/simple_scada_sim.py` & `gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/simple_scada_sim.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/brick_storage_heater/strategy_utils.py` & `gridworks_atn-0.3.4/src/gwatn/brick_storage_heater/strategy_utils.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/config.py` & `gridworks_atn-0.3.4/src/gwatn/config.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/data_classes/.DS_Store` & `gridworks_atn-0.3.4/src/gwatn/data_classes/.DS_Store`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/data_classes/__init__.py` & `gridworks_atn-0.3.4/src/gwatn/data_classes/__init__.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/data_classes/d_edge.py` & `gridworks_atn-0.3.4/src/gwatn/data_classes/d_edge.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/data_classes/d_graph.py` & `gridworks_atn-0.3.4/src/gwatn/data_classes/d_graph.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/data_classes/d_node.py` & `gridworks_atn-0.3.4/src/gwatn/data_classes/d_node.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/demo_methods.py` & `gridworks_atn-0.3.4/src/gwatn/demo_methods.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/dev_utils/dev_discoverer.py` & `gridworks_atn-0.3.4/src/gwatn/dev_utils/dev_discoverer.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/dev_utils/dev_ta_owner.py` & `gridworks_atn-0.3.4/src/gwatn/dev_utils/dev_ta_owner.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/dev_utils/dev_validator.py` & `gridworks_atn-0.3.4/src/gwatn/dev_utils/dev_validator.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/dev_utils/make_plants.py` & `gridworks_atn-0.3.4/src/gwatn/dev_utils/make_plants.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/dispatch_contract.py` & `gridworks_atn-0.3.4/src/gwatn/dispatch_contract.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/dispatch_contract_artifacts/application.json` & `gridworks_atn-0.3.4/src/gwatn/dispatch_contract_artifacts/application.json`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/dispatch_contract_artifacts/approval.teal` & `gridworks_atn-0.3.4/src/gwatn/dispatch_contract_artifacts/approval.teal`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/dispatch_contract_artifacts/contract.json` & `gridworks_atn-0.3.4/src/gwatn/dispatch_contract_artifacts/contract.json`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/enums/__init__.py` & `gridworks_atn-0.3.4/src/gwatn/enums/__init__.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/enums/distribution_tariff.py` & `gridworks_atn-0.3.4/src/gwatn/enums/distribution_tariff.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/enums/energy_supply_type.py` & `gridworks_atn-0.3.4/src/gwatn/enums/energy_supply_type.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/enums/recognized_irradiance_type.py` & `gridworks_atn-0.3.4/src/gwatn/enums/recognized_irradiance_type.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/enums/recognized_temperature_unit.py` & `gridworks_atn-0.3.4/src/gwatn/enums/recognized_temperature_unit.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/python_ta_daemon.json` & `gridworks_atn-0.3.4/src/gwatn/python_ta_daemon.json`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/python_ta_daemon.py` & `gridworks_atn-0.3.4/src/gwatn/python_ta_daemon.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/scada_codec.py` & `gridworks_atn-0.3.4/src/gwatn/scada_codec.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/simple_atn_actor.py` & `gridworks_atn-0.3.4/src/gwatn/simple_atn_actor.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/simple_scada_sim_actor_base.py` & `gridworks_atn-0.3.4/src/gwatn/simple_scada_sim_actor_base.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/ta_daemon_rest_api.py` & `gridworks_atn-0.3.4/src/gwatn/ta_daemon_rest_api.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/two_channel_actor_base.py` & `gridworks_atn-0.3.4/src/gwatn/two_channel_actor_base.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/__init__.py` & `gridworks_atn-0.3.4/src/gwatn/types/__init__.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/accepted_bid.py` & `gridworks_atn-0.3.4/src/gwatn/types/accepted_bid.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/atn_bid.py` & `gridworks_atn-0.3.4/src/gwatn/types/atn_bid.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/atn_params.py` & `gridworks_atn-0.3.4/src/gwatn/types/atn_params.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/atn_params_brickstorageheater.py` & `gridworks_atn-0.3.4/src/gwatn/types/atn_params_brickstorageheater.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/atn_params_report.py` & `gridworks_atn-0.3.4/src/gwatn/types/atn_params_report.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/basegnode_scada_create.py` & `gridworks_atn-0.3.4/src/gwatn/types/basegnode_scada_create.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/csv_distp_sync.py` & `gridworks_atn-0.3.4/src/gwatn/types/csv_distp_sync.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/csv_eprt_sync.py` & `gridworks_atn-0.3.4/src/gwatn/types/csv_eprt_sync.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/csv_weather_forecast_sync.py` & `gridworks_atn-0.3.4/src/gwatn/types/csv_weather_forecast_sync.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/data_channel.py` & `gridworks_atn-0.3.4/src/gwatn/types/data_channel.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/discoverycert_algo_create.py` & `gridworks_atn-0.3.4/src/gwatn/types/discoverycert_algo_create.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/dispatch_contract_confirmed.py` & `gridworks_atn-0.3.4/src/gwatn/types/dispatch_contract_confirmed.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/flo_params.py` & `gridworks_atn-0.3.4/src/gwatn/types/flo_params.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/flo_params_brickstorageheater.py` & `gridworks_atn-0.3.4/src/gwatn/types/flo_params_brickstorageheater.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/flo_params_report.py` & `gridworks_atn-0.3.4/src/gwatn/types/flo_params_report.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/gt_dispatch_boolean.py` & `gridworks_atn-0.3.4/src/gwatn/types/gt_dispatch_boolean.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/heartbeat_b.py` & `gridworks_atn-0.3.4/src/gwatn/types/heartbeat_b.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/initial_tadeed_algo_create.py` & `gridworks_atn-0.3.4/src/gwatn/types/initial_tadeed_algo_create.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/initial_tadeed_algo_optin.py` & `gridworks_atn-0.3.4/src/gwatn/types/initial_tadeed_algo_optin.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/initial_tadeed_algo_transfer.py` & `gridworks_atn-0.3.4/src/gwatn/types/initial_tadeed_algo_transfer.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/join_dispatch_contract.py` & `gridworks_atn-0.3.4/src/gwatn/types/join_dispatch_contract.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/latest_price.py` & `gridworks_atn-0.3.4/src/gwatn/types/latest_price.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/market_slot.py` & `gridworks_atn-0.3.4/src/gwatn/types/market_slot.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/market_type_gt.py` & `gridworks_atn-0.3.4/src/gwatn/types/market_type_gt.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/new_tadeed_algo_optin.py` & `gridworks_atn-0.3.4/src/gwatn/types/new_tadeed_algo_optin.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/new_tadeed_send.py` & `gridworks_atn-0.3.4/src/gwatn/types/new_tadeed_send.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/old_tadeed_algo_return.py` & `gridworks_atn-0.3.4/src/gwatn/types/old_tadeed_algo_return.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/price_quantity.py` & `gridworks_atn-0.3.4/src/gwatn/types/price_quantity.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/price_quantity_unitless.py` & `gridworks_atn-0.3.4/src/gwatn/types/price_quantity_unitless.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/scada_cert_transfer.py` & `gridworks_atn-0.3.4/src/gwatn/types/scada_cert_transfer.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/simplesim_driver_data.py` & `gridworks_atn-0.3.4/src/gwatn/types/simplesim_driver_data.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/simplesim_driver_data_bsh.py` & `gridworks_atn-0.3.4/src/gwatn/types/simplesim_driver_data_bsh.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/simplesim_driver_report.py` & `gridworks_atn-0.3.4/src/gwatn/types/simplesim_driver_report.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/simplesim_snapshot_brickstorageheater.py` & `gridworks_atn-0.3.4/src/gwatn/types/simplesim_snapshot_brickstorageheater.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/sla_enter.py` & `gridworks_atn-0.3.4/src/gwatn/types/sla_enter.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/tadeed_specs_hack.py` & `gridworks_atn-0.3.4/src/gwatn/types/tadeed_specs_hack.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/tavalidatorcert_algo_create.py` & `gridworks_atn-0.3.4/src/gwatn/types/tavalidatorcert_algo_create.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/tavalidatorcert_algo_transfer.py` & `gridworks_atn-0.3.4/src/gwatn/types/tavalidatorcert_algo_transfer.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/src/gwatn/types/terminalasset_certify_hack.py` & `gridworks_atn-0.3.4/src/gwatn/types/terminalasset_certify_hack.py`

 * *Files identical despite different names*

### Comparing `gridworks_atn-0.3.3/PKG-INFO` & `gridworks_atn-0.3.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gridworks-atn
-Version: 0.3.3
+Version: 0.3.4
 Summary: Gridworks Atn Spaceheat
 Home-page: https://github.com/thegridelectric/gridworks-atn
 License: None
 Author: Jessica Millar
 Author-email: jmillar@gridworks-consulting.com
 Requires-Python: >=3.10,<4.0
 Classifier: Development Status :: 2 - Pre-Alpha
```

