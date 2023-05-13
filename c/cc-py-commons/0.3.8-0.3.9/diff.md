# Comparing `tmp/cc_py_commons-0.3.8.tar.gz` & `tmp/cc_py_commons-0.3.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/cc_py_commons-0.3.8.tar", last modified: Wed Jan 18 20:44:59 2023, max compression
+gzip compressed data, was "dist/cc_py_commons-0.3.9.tar", last modified: Wed Jan 25 06:38:46 2023, max compression
```

## Comparing `cc_py_commons-0.3.8.tar` & `cc_py_commons-0.3.9.tar`

### file list

```diff
@@ -1,116 +1,116 @@
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/
--rw-rw-r--   0 rof       (1001) rof       (1001)       38 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/setup.cfg
--rw-rw-r--   0 rof       (1001) rof       (1001)      265 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/PKG-INFO
--rw-rw-r--   0 rof       (1001) rof       (1001)      427 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/setup.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1118 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/README.md
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons.egg-info/
--rw-rw-r--   0 rof       (1001) rof       (1001)       14 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons.egg-info/top_level.txt
--rw-rw-r--   0 rof       (1001) rof       (1001)       61 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons.egg-info/requires.txt
--rw-rw-r--   0 rof       (1001) rof       (1001)        1 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons.egg-info/dependency_links.txt
--rw-rw-r--   0 rof       (1001) rof       (1001)     3526 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons.egg-info/SOURCES.txt
--rw-rw-r--   0 rof       (1001) rof       (1001)      265 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons.egg-info/PKG-INFO
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/
--rw-rw-r--   0 rof       (1001) rof       (1001)    12897 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/geolocate.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/utils/
--rw-rw-r--   0 rof       (1001) rof       (1001)      175 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/temperature_utils.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     2364 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/s3_file.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1044 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/redis.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1057 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/price_utils.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     2792 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/pc_miler_utils.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      931 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/logger.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1048 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/local_file.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      508 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/get_delivery_date.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      575 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/dimension_utils.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      759 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/datetimes.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1519 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/case_conversion.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/utils/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/
--rw-rw-r--   0 rof       (1001) rof       (1001)     4935 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/transaction_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     4759 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/transaction.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     2685 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/map_transaction.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      540 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/equipment_mapping_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      289 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/equipment_mapping.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      213 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/equipment_class.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      442 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/equipment_clas_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/transactions/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/tests/
--rw-rw-r--   0 rof       (1001) rof       (1001)      475 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/tests/test_temperature_utils.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1944 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/tests/test_map_transaction.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      844 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/tests/test_case_conversion.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/tests/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/sqs/
--rw-rw-r--   0 rof       (1001) rof       (1001)      440 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sqs/sqs_service.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1022 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sqs/booking_assistant_flow_event.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sqs/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/sns/
--rw-rw-r--   0 rof       (1001) rof       (1001)      269 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sns/sns_service.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      827 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sns/parsed_carrier_notification.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      751 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sns/import_movements_notification.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      984 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sns/booking_assistant_flow_notification.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      929 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sns/book_load_notification.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/sns/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/services/
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/services/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/services/mercury/
--rw-rw-r--   0 rof       (1001) rof       (1001)      560 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/services/mercury/get_lane_price_for_bulk.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      550 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/services/mercury/get_lane_price.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/services/mercury/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/services/freight_hub/
--rw-rw-r--   0 rof       (1001) rof       (1001)      474 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/services/freight_hub/post_freight_hub_load.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/services/freight_hub/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/services/c4/
--rw-rw-r--   0 rof       (1001) rof       (1001)      708 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/services/c4/get_users_for_account.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/services/c4/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/schemas/
--rw-rw-r--   0 rof       (1001) rof       (1001)      439 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/schemas/camel_case_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/schemas/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/rfp/
--rw-rw-r--   0 rof       (1001) rof       (1001)      145 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/rfp/rfp_status.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/rfp/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/quotes/
--rw-rw-r--   0 rof       (1001) rof       (1001)      501 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/quotes/quote_status.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     2390 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/quotes/quote_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1767 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/quotes/quote.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/quotes/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/loads/
--rw-rw-r--   0 rof       (1001) rof       (1001)      751 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/map_load_response.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      463 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/location_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      286 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/location.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      501 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/load_status.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     3512 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/load_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     3092 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/load.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      442 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/freighthub_contact_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      338 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/freighthub_contact.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      625 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/equipment_types.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      384 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/equipment_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      154 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/equipment.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/loads/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/lanes/
--rw-rw-r--   0 rof       (1001) rof       (1001)      941 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/lanes/lane_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      663 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/lanes/lane.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1251 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/lanes/carrier_lane_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      972 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/lanes/carrier_lane.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/lanes/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/db/
--rw-rw-r--   0 rof       (1001) rof       (1001)      573 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/db/connection.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/db/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/config/
--rw-rw-r--   0 rof       (1001) rof       (1001)     1455 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/config/pc_miler_config.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     1310 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/config/mcleod_load_fields.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     5442 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/config/env.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/config/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/carriers/
--rw-rw-r--   0 rof       (1001) rof       (1001)      698 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/carriers/contact_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      381 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/carriers/contact.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     2671 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/carriers/carrier_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)     3033 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/carriers/carrier.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      687 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/carriers/account_carrier_map_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      233 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/carriers/account_carrier_map.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/carriers/__init__.py
-drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:59.000000 cc_py_commons-0.3.8/cc_py_commons/bids/
--rw-rw-r--   0 rof       (1001) rof       (1001)     1245 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/bids/bid_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      471 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/bids/bid_history_schema.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      300 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/bids/bid_history.py
--rw-rw-r--   0 rof       (1001) rof       (1001)      676 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/bids/bid.py
--rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-18 20:44:41.000000 cc_py_commons-0.3.8/cc_py_commons/bids/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/
+-rw-rw-r--   0 rof       (1001) rof       (1001)       38 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/setup.cfg
+-rw-rw-r--   0 rof       (1001) rof       (1001)      265 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/PKG-INFO
+-rw-rw-r--   0 rof       (1001) rof       (1001)      427 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/setup.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1118 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/README.md
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons.egg-info/
+-rw-rw-r--   0 rof       (1001) rof       (1001)       14 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons.egg-info/top_level.txt
+-rw-rw-r--   0 rof       (1001) rof       (1001)       61 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons.egg-info/requires.txt
+-rw-rw-r--   0 rof       (1001) rof       (1001)        1 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons.egg-info/dependency_links.txt
+-rw-rw-r--   0 rof       (1001) rof       (1001)     3526 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons.egg-info/SOURCES.txt
+-rw-rw-r--   0 rof       (1001) rof       (1001)      265 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons.egg-info/PKG-INFO
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/
+-rw-rw-r--   0 rof       (1001) rof       (1001)    12897 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/geolocate.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/utils/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      175 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/temperature_utils.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     2364 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/s3_file.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1044 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/redis.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1057 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/price_utils.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     2792 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/pc_miler_utils.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      931 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/logger.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1048 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/local_file.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      508 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/get_delivery_date.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      575 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/dimension_utils.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      759 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/datetimes.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1519 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/case_conversion.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/utils/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/
+-rw-rw-r--   0 rof       (1001) rof       (1001)     4935 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/transaction_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     4759 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/transaction.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     2685 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/map_transaction.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      540 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/equipment_mapping_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      289 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/equipment_mapping.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      213 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/equipment_class.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      442 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/equipment_clas_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/transactions/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/tests/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      475 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/tests/test_temperature_utils.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1944 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/tests/test_map_transaction.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      844 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/tests/test_case_conversion.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/tests/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/sqs/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      440 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sqs/sqs_service.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1022 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sqs/booking_assistant_flow_event.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sqs/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/sns/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      269 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sns/sns_service.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      827 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sns/parsed_carrier_notification.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      751 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sns/import_movements_notification.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      984 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sns/booking_assistant_flow_notification.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      929 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sns/book_load_notification.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/sns/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/services/
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/services/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/services/mercury/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      560 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/services/mercury/get_lane_price_for_bulk.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      550 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/services/mercury/get_lane_price.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/services/mercury/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/services/freight_hub/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      474 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/services/freight_hub/post_freight_hub_load.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/services/freight_hub/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/services/c4/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      708 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/services/c4/get_users_for_account.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/services/c4/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/schemas/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      439 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/schemas/camel_case_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/schemas/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/rfp/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      145 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/rfp/rfp_status.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/rfp/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/quotes/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      501 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/quotes/quote_status.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     2391 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/quotes/quote_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1803 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/quotes/quote.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/quotes/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/loads/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      751 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/map_load_response.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      463 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/location_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      286 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/location.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      501 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/load_status.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     3513 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/load_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     3092 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/load.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      442 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/freighthub_contact_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      338 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/freighthub_contact.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      625 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/equipment_types.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      384 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/equipment_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      154 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/equipment.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/loads/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/lanes/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      941 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/lanes/lane_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      663 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/lanes/lane.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1251 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/lanes/carrier_lane_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      972 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/lanes/carrier_lane.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/lanes/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/db/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      573 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/db/connection.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/db/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/config/
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1455 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/config/pc_miler_config.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1310 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/config/mcleod_load_fields.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     5442 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/config/env.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/config/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/carriers/
+-rw-rw-r--   0 rof       (1001) rof       (1001)      698 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/carriers/contact_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      381 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/carriers/contact.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     2671 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/carriers/carrier_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)     3033 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/carriers/carrier.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      687 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/carriers/account_carrier_map_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      233 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/carriers/account_carrier_map.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/carriers/__init__.py
+drwxrwxr-x   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:46.000000 cc_py_commons-0.3.9/cc_py_commons/bids/
+-rw-rw-r--   0 rof       (1001) rof       (1001)     1245 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/bids/bid_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      471 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/bids/bid_history_schema.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      300 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/bids/bid_history.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)      676 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/bids/bid.py
+-rw-rw-r--   0 rof       (1001) rof       (1001)        0 2023-01-25 06:38:29.000000 cc_py_commons-0.3.9/cc_py_commons/bids/__init__.py
```

### Comparing `cc_py_commons-0.3.8/README.md` & `cc_py_commons-0.3.9/README.md`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons.egg-info/SOURCES.txt` & `cc_py_commons-0.3.9/cc_py_commons.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/geolocate.py` & `cc_py_commons-0.3.9/cc_py_commons/geolocate.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/s3_file.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/s3_file.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/redis.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/redis.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/price_utils.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/price_utils.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/pc_miler_utils.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/pc_miler_utils.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/logger.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/logger.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/local_file.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/local_file.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/dimension_utils.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/dimension_utils.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/datetimes.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/datetimes.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/utils/case_conversion.py` & `cc_py_commons-0.3.9/cc_py_commons/utils/case_conversion.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/transactions/transaction_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/transactions/transaction_schema.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/transactions/transaction.py` & `cc_py_commons-0.3.9/cc_py_commons/transactions/transaction.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/transactions/map_transaction.py` & `cc_py_commons-0.3.9/cc_py_commons/transactions/map_transaction.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/transactions/equipment_mapping_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/transactions/equipment_mapping_schema.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/tests/test_map_transaction.py` & `cc_py_commons-0.3.9/cc_py_commons/tests/test_map_transaction.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/tests/test_case_conversion.py` & `cc_py_commons-0.3.9/cc_py_commons/tests/test_case_conversion.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/sqs/booking_assistant_flow_event.py` & `cc_py_commons-0.3.9/cc_py_commons/sqs/booking_assistant_flow_event.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/sns/parsed_carrier_notification.py` & `cc_py_commons-0.3.9/cc_py_commons/sns/parsed_carrier_notification.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/sns/import_movements_notification.py` & `cc_py_commons-0.3.9/cc_py_commons/sns/import_movements_notification.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/sns/booking_assistant_flow_notification.py` & `cc_py_commons-0.3.9/cc_py_commons/sns/booking_assistant_flow_notification.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/sns/book_load_notification.py` & `cc_py_commons-0.3.9/cc_py_commons/sns/book_load_notification.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/services/mercury/get_lane_price_for_bulk.py` & `cc_py_commons-0.3.9/cc_py_commons/services/mercury/get_lane_price_for_bulk.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/services/mercury/get_lane_price.py` & `cc_py_commons-0.3.9/cc_py_commons/services/mercury/get_lane_price.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/services/c4/get_users_for_account.py` & `cc_py_commons-0.3.9/cc_py_commons/services/c4/get_users_for_account.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/quotes/quote_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/quotes/quote_schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -44,12 +44,12 @@
     max_temperature= fields.Float(allow_none=True)
     tarp_size = fields.Integer(allow_none=True)
     team_service_required= fields.Boolean(missing=False, default=False)
     # generated by server and returned
     id = fields.UUID(allow_none=True)
     # generated by server and returned
     load_number = fields.String(allow_none=True)
-    max_pay = fields.String(allow_none=True)
+    max_pay = fields.Integer(allow_none=True)
 
     @post_load
     def make_quote(self, data, **kwargs):
         return Quote(**data)
```

### Comparing `cc_py_commons-0.3.8/cc_py_commons/quotes/quote.py` & `cc_py_commons-0.3.9/cc_py_commons/quotes/quote.py`

 * *Files 5% similar despite different names*

```diff
@@ -43,8 +43,9 @@
     min_temperature: float = field(default=None)
     max_temperature: float = field(default=None)
     tarp_size: int = field(default=None)
     team_service_required: bool = field(default=False)
     # generated by server and returned
     id: uuid.UUID = field(default=None)
     # generated by server and returned
-    load_number: str = field(default=None)    
+    load_number: str = field(default=None)
+    max_pay: int = field(default=None)
```

### Comparing `cc_py_commons-0.3.8/cc_py_commons/loads/map_load_response.py` & `cc_py_commons-0.3.9/cc_py_commons/loads/map_load_response.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/loads/load_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/loads/load_schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -63,12 +63,12 @@
     origin_location_name = fields.String(allow_none=True)
     destination_location_id = fields.String(allow_none=True)
     destination_location_name = fields.String(allow_none=True)
     customer_equipment_id = fields.String(allow_none=True)
     partial_load = fields.Boolean(allow_none=True)
     pieces = fields.Integer(allow_none=True)
     available_time = fields.DateTime(allow_none=True)
-    max_pay = fields.String(allow_none=True)
+    max_pay = fields.Integer(allow_none=True)
 
     @post_load
     def make_load(self, data, **kwargs):
         return Load(**data)
```

### Comparing `cc_py_commons-0.3.8/cc_py_commons/loads/load.py` & `cc_py_commons-0.3.9/cc_py_commons/loads/load.py`

 * *Files 0% similar despite different names*

```diff
@@ -70,8 +70,8 @@
     destination_location_name: str = field(default=None)
     special_instructions: dict = field(default=None)
     customer_equipment_id: str = field(default=None)
     partial_load: bool = field(default=False)
     pieces: int = field(default=None)
     available_time: datetime.datetime = field(default=None)
     account_id: int = field(default=None)
-    max_pay: str = field(default=None)
+    max_pay: int = field(default=None)
```

### Comparing `cc_py_commons-0.3.8/cc_py_commons/loads/equipment_types.py` & `cc_py_commons-0.3.9/cc_py_commons/loads/equipment_types.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/lanes/lane_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/lanes/lane_schema.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/lanes/lane.py` & `cc_py_commons-0.3.9/cc_py_commons/lanes/lane.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/lanes/carrier_lane_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/lanes/carrier_lane_schema.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/lanes/carrier_lane.py` & `cc_py_commons-0.3.9/cc_py_commons/lanes/carrier_lane.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/db/connection.py` & `cc_py_commons-0.3.9/cc_py_commons/db/connection.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/config/pc_miler_config.py` & `cc_py_commons-0.3.9/cc_py_commons/config/pc_miler_config.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/config/mcleod_load_fields.py` & `cc_py_commons-0.3.9/cc_py_commons/config/mcleod_load_fields.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/config/env.py` & `cc_py_commons-0.3.9/cc_py_commons/config/env.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/carriers/contact_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/carriers/contact_schema.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/carriers/carrier_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/carriers/carrier_schema.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/carriers/carrier.py` & `cc_py_commons-0.3.9/cc_py_commons/carriers/carrier.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/carriers/account_carrier_map_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/carriers/account_carrier_map_schema.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/bids/bid_schema.py` & `cc_py_commons-0.3.9/cc_py_commons/bids/bid_schema.py`

 * *Files identical despite different names*

### Comparing `cc_py_commons-0.3.8/cc_py_commons/bids/bid.py` & `cc_py_commons-0.3.9/cc_py_commons/bids/bid.py`

 * *Files identical despite different names*

